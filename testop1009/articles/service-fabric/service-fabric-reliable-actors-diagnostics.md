---
title: Actors diagnostics and monitoring | Microsoft Azure
description: This article describes the diagnostics and performance monitoring features in the Service Fabric Reliable Actors runtime, including the events and performance counters emitted by it.
services: service-fabric
documentationcenter: .net
author: abhishekram
manager: timlt
editor: vturecek

ms.service: service-fabric
ms.devlang: dotnet
ms.topic: article
ms.tgt_pltfrm: NA
ms.workload: NA
ms.date: 07/05/2016
ms.author: abhisram

---
# Diagnostics and performance monitoring for Reliable Actors
The Reliable Actors runtime emits [EventSource](https://msdn.microsoft.com/library/system.diagnostics.tracing.eventsource.aspx) events and [performance counters](https://msdn.microsoft.com/library/system.diagnostics.performancecounter.aspx). These provide insights into how the runtime is operating and help with troubleshooting and performance monitoring.

## EventSource events
The EventSource provider name for the Reliable Actors runtime is "Microsoft-ServiceFabric-Actors". Events from this event source appear in the [Diagnostics Events](service-fabric-diagnostics-how-to-monitor-and-diagnose-services-locally.md#view-service-fabric-system-events-in-visual-studio) window when the actor application is being [debugged in Visual Studio](service-fabric-debugging-your-application.md).

Examples of tools and technologies that help in collecting and/or viewing EventSource events are [PerfView](http://www.microsoft.com/download/details.aspx?id=28567), [Azure Diagnostics](../cloud-services/cloud-services-dotnet-diagnostics.md), [Semantic Logging](https://msdn.microsoft.com/library/dn774980.aspx), and the [Microsoft TraceEvent Library](http://www.nuget.org/packages/Microsoft.Diagnostics.Tracing.TraceEvent).

### Keywords
All events that belong to the Reliable Actors EventSource are associated with one or more keywords. This enables filtering of events that are collected. The following keyword bits are defined.

| Bit | Description |
| --- | --- |
| 0x1 |Set of important events that summarize the operation of the Fabric Actors runtime. |
| 0x2 |Set of events that describe actor method calls. For more information, see the [introductory topic on actors](service-fabric-reliable-actors-introduction.md#actors). |
| 0x4 |Set of events related to actor state. For more information, see the topic on [actor state management](service-fabric-reliable-actors-state-management.md). |
| 0x8 |Set of events related to turn-based concurrency in the actor. For more information, see the topic on [concurrency](service-fabric-reliable-actors-introduction.md#concurrency). |

## Performance counters
The Reliable Actors runtime defines the following performance counter categories.

| Category | Description |
| --- | --- |
| Service Fabric Actor |Counters specific to Azure Service Fabric actors, e.g. time taken to save actor state |
| Service Fabric Actor Method |Counters specific to methods implemented by Service Fabric actors, e.g. how often an actor method is invoked |

Each of the above categories has one or more counters.

The [Windows Performance Monitor](https://technet.microsoft.com/library/cc749249.aspx) application that is available by default in the Windows operating system can be used to collect and view performance counter data. [Azure Diagnostics](../cloud-services/cloud-services-dotnet-diagnostics.md) is another option for collecting performance counter data and uploading it to Azure tables.

### Performance counter instance names
A cluster that has a large number of actor services or actor service partitions will have a large number of actor performance counter instances. The performance counter instance names can help in identifying the specific [partition](service-fabric-reliable-actors-platform.md#service-fabric-partition-concepts-for-actors) and actor method (if applicable) that the performance counter instance is associated with.

#### Service Fabric Actor category
For the category `Service Fabric Actor`, the counter instance names are in the following format:

`ServiceFabricPartitionID_ActorsRuntimeInternalID`

*ServiceFabricPartitionID* is the string representation of the Service Fabric partition ID that the performance counter instance is associated with. The partition ID is a GUID, and its string representation is generated through the [`Guid.ToString`](https://msdn.microsoft.com/library/97af8hh4.aspx) method with format specifier "D".

*ActorRuntimeInternalID* is the string representation of a 64-bit integer that is generated by the Fabric Actors runtime for its internal use. This is included in the performance counter instance name to ensure its uniqueness and avoid conflict with other performance counter instance names. Users should not try to interpret this portion of the performance counter instance name.

The following is an example of a counter instance name for a counter that belongs to the `Service Fabric Actor` category:

`2740af29-78aa-44bc-a20b-7e60fb783264_635650083799324046`

In the example above, `2740af29-78aa-44bc-a20b-7e60fb783264` is the string representation of the Service Fabric partition ID, and `635650083799324046` is the 64-bit ID that is generated for the runtime's internal use.

#### Service Fabric Actor Method category
For the category `Service Fabric Actor Method`, the counter instance names are in the following format:

`MethodName_ActorsRuntimeMethodId_ServiceFabricPartitionID_ActorsRuntimeInternalID`

*MethodName* is the name of the actor method that the performance counter instance is associated with. The format of the method name is determined based on some logic in the Fabric Actors runtime that balances the readability of the name with constraints on the maximum length of the performance counter instance names on Windows.

*ActorsRuntimeMethodId* is the string representation of a 32-bit integer that is generated by the Fabric Actors runtime for its internal use. This is included in the performance counter instance name to ensure its uniqueness and avoid conflict with other performance counter instance names. Users should not try to interpret this portion of the performance counter instance name.

*ServiceFabricPartitionID* is the string representation of the Service Fabric partition ID that the performance counter instance is associated with. The partition ID is a GUID, and its string representation is generated through the [`Guid.ToString`](https://msdn.microsoft.com/library/97af8hh4.aspx) method with format specifier "D".

*ActorRuntimeInternalID* is the string representation of a 64-bit integer that is generated by the Fabric Actors runtime for its internal use. This is included in the performance counter instance name to ensure its uniqueness and avoid conflict with other performance counter instance names. Users should not try to interpret this portion of the performance counter instance name.

The following is an example of a counter instance name for a counter that belongs to the `Service Fabric Actor Method` category:

`ivoicemailboxactor.leavemessageasync_2_89383d32-e57e-4a9b-a6ad-57c6792aa521_635650083804480486`

In the example above, `ivoicemailboxactor.leavemessageasync` is the method name, `2` is the 32-bit ID generated for the runtime's internal use, `89383d32-e57e-4a9b-a6ad-57c6792aa521` is the string representation of the Service Fabric partition ID, and `635650083804480486` is the 64-bit ID generated for the runtime's internal use.

## List of events and performance counters
### Actor method events and performance counters
The Reliable Actors runtime emits the following events related to [actor methods](service-fabric-reliable-actors-introduction.md#actors).

| Event name | Event ID | Level | Keyword | Description |
| --- | --- | --- | --- | --- |
| ActorMethodStart |7 |Verbose |0x2 |Actors runtime is about to invoke an actor method. |
| ActorMethodStop |8 |Verbose |0x2 |An actor method has finished executing. That is, the runtime's asynchronous call to the actor method has returned, and the task returned by the actor method has finished. |
| ActorMethodThrewException |9 |Warning |0x3 |An exception was thrown during the execution of an actor method, either during the runtime's asynchronous call to the actor method or during the execution of the task returned by the actor method. This event indicates some sort of failure in the actor code that needs investigation. |

The Reliable Actors runtime publishes the following performance counters related to the execution of actor methods.

| Category name | Counter name | Description |
| --- | --- | --- |
| Service Fabric Actor Method |Invocations/Sec |Number of times that the actor service method is invoked per second |
| Service Fabric Actor Method |Average milliseconds per invocation |Time taken to execute the actor service method in milliseconds |
| Service Fabric Actor Method |Exceptions thrown/Sec |Number of times that the actor service method threw an exception per second |

### Concurrency events and performance counters
The Reliable Actors runtime emits the following events related to [concurrency](service-fabric-reliable-actors-introduction.md#concurrency).

| Event name | Event ID | Level | Keyword | Description |
| --- | --- | --- | --- | --- |
| ActorMethodCallsWaitingForLock |12 |Verbose |0x8 |This event is written at the start of each new turn in an actor. It contains  the number of pending actor calls that are waiting to acquire the per-actor lock that enforces turn-based concurrency. |

The Reliable Actors runtime publishes the following performance counters related to concurrency.

| Category name | Counter name | Description |
| --- | --- | --- |
| Service Fabric Actor |# of actor calls waiting for actor lock |Number of pending actor calls waiting to acquire the per-actor lock that enforces turn-based concurrency |
| Service Fabric Actor |Average milliseconds per lock wait |Time taken (in milliseconds) to acquire the per-actor lock that enforces turn-based concurrency |
| Service Fabric Actor |Average milliseconds actor lock held |Time (in milliseconds) for which the per-actor lock is held |

### Actor state management events and performance counters
The Reliable Actors runtime emits the following events related to [actor state management](service-fabric-reliable-actors-state-management.md).

| Event name | Event ID | Level | Keyword | Description |
| --- | --- | --- | --- | --- |
| ActorSaveStateStart |10 |Verbose |0x4 |Actors runtime is about to save the actor state. |
| ActorSaveStateStop |11 |Verbose |0x4 |Actors runtime has finished saving the actor state. |

The Reliable Actors runtime publishes the following performance counters related to actor state management.

| Category name | Counter name | Description |
| --- | --- | --- |
| Service Fabric Actor |Average milliseconds per save state operation |Time taken to save actor state in milliseconds |
| Service Fabric Actor |Average milliseconds per load state operation |Time taken to load actor state in milliseconds |

### Events related to actor replicas
The Reliable Actors runtime emits the following events related to [actor replicas](service-fabric-reliable-actors-platform.md#service-fabric-partition-concepts-for-stateful-actors).

| Event name | Event ID | Level | Keyword | Description |
| --- | --- | --- | --- | --- |
| ReplicaChangeRoleToPrimary |1 |Informational |0x1 |Actor replica changed role to Primary. This implies that the actors for this partition will be created inside this replica. |
| ReplicaChangeRoleFromPrimary |2 |Informational |0x1 |Actor replica changed role to non-Primary. This implies that the actors for this partition will no longer be created inside this replica. No new requests will be delivered to actors already created within this replica. The actors will be destroyed after any in-progress requests are completed. |

### Actor activation and deactivation events and performance counters
The Reliable Actors runtime emits the following events related to [actor activation and deactivation](service-fabric-reliable-actors-lifecycle.md).

| Event name | Event ID | Level | Keyword | Description |
| --- | --- | --- | --- | --- |
| ActorActivated |5 |Informational |0x1 |An actor has been activated. |
| ActorDeactivated |6 |Informational |0x1 |An actor has been deactivated. |

The Reliable Actors runtime publishes the following performance counters related to actor activation and deactivation.

| Category name | Counter name | Description |
| --- | --- | --- |
| Service Fabric Actor |Average OnActivateAsync milliseconds |Time taken to execute OnActivateAsync method in milliseconds |

### Actor request processing performance counters
When a client invokes a method via an actor proxy object, it results in a request message being sent over the network to the actor service. The service processes the request message and sends a response back to the client. The Reliable Actors runtime publishes the following performance counters related to actor request processing.

| Category name | Counter name | Description |
| --- | --- | --- |
| Service Fabric Actor |# of outstanding requests |Number of requests being processed in the service |
| Service Fabric Actor |Average milliseconds per request |Time taken (in milliseconds) by the service to process a request |
| Service Fabric Actor |Average milliseconds for request deserialization |Time taken (in milliseconds) to deserialize actor request message when it is received at the service |
| Service Fabric Actor |Average milliseconds for response serialization |Time taken (in milliseconds) to serialize the actor response message at the service before the response is sent to the client |

## Next steps
* [How Reliable Actors use the Service Fabric platform](service-fabric-reliable-actors-platform.md)
* [Actor API reference documentation](https://msdn.microsoft.com/library/azure/dn971626.aspx)
* [Sample code](https://github.com/Azure/servicefabric-samples)
