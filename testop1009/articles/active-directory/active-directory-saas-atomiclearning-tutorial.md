---
title: 'Tutorial: Azure Active Directory integration with Atomic Learning | Microsoft Azure'
description: Learn how to configure single sign-on between Azure Active Directory and Atomic Learning.
services: active-directory
documentationcenter: ''
author: jeevansd
manager: femila
editor: ''

ms.service: active-directory
ms.workload: identity
ms.tgt_pltfrm: na
ms.devlang: na
ms.topic: article
ms.date: 08/31/2016
ms.author: jeedes

---
# Tutorial: Azure Active Directory integration with Atomic Learning
In this tutorial, you learn how to integrate Atomic Learning with Azure Active Directory (Azure AD).

Integrating Atomic Learning with Azure AD provides you with the following benefits:

* You can control in Azure AD who has access to Atomic Learning
* You can enable your users to automatically get signed-on to Atomic Learning (Single Sign-On) with their Azure AD accounts
* You can manage your accounts in one central location - the Azure classic portal

If you want to know more details about SaaS app integration with Azure AD, see [What is application access and single sign-on with Azure Active Directory](active-directory-appssoaccess-whatis.md).

## Prerequisites
To configure Azure AD integration with Atomic Learning, you need the following items:

* An Azure AD subscription
* A **Atomic Learning** single-sign on enabled subscription

> [!NOTE]
> To test the steps in this tutorial, we do not recommend using a production environment.
> 
> 

To test the steps in this tutorial, you should follow these recommendations:

* You should not use your production environment, unless this is necessary.
* If you don't have an Azure AD trial environment, you can get a one-month trial [here](https://azure.microsoft.com/pricing/free-trial/).

## Scenario description
In this tutorial, you test Azure AD single sign-on in a test environment. 
The scenario outlined in this tutorial consists of two main building blocks:

1. Adding Atomic Learning from the gallery
2. Configuring and testing Azure AD single sign-on

## Adding Atomic Learning from the gallery
To configure the integration of Atomic Learning into Azure AD, you need to add Atomic Learning from the gallery to your list of managed SaaS apps.

**To add Atomic Learning from the gallery, perform the following steps:**

1. In the **Azure classic portal**, on the left navigation pane, click **Active Directory**. 
   
    ![Active Directory][1]
2. From the **Directory** list, select the directory for which you want to enable directory integration.
3. To open the applications view, in the directory view, click **Applications** in the top menu.
   
    ![Applications][2]
4. Click **Add** at the bottom of the page.
   
    ![Applications][3]
5. On the **What do you want to do** dialog, click **Add an application from the gallery**.
   
    ![Applications][4]
6. In the search box, type **Atomic Learning**.
   
    ![Creating an Azure AD test user](./media/active-directory-saas-atomiclearning-tutorial/tutorial_atomiclearning_01.png)
7. In the results pane, select **Atomic Learning**, and then click **Complete** to add the application.
   
    ![Creating an Azure AD test user](./media/active-directory-saas-atomiclearning-tutorial/tutorial_atomiclearning_02.png)

## Configuring and testing Azure AD single sign-on
In this section, you configure and test Azure AD single sign-on with Atomic Learning based on a test user called "Britta Simon".

For single sign-on to work, Azure AD needs to know what the counterpart user in Atomic Learning is to a user in Azure AD. In other words, a link relationship between an Azure AD user and the related user in Atomic Learning needs to be established.
This link relationship is established by assigning the value of the **user name** in Azure AD as the value of the **Username** in Atomic Learning.

To configure and test Azure AD single sign-on with Atomic Learning, you need to complete the following building blocks:

1. **[Configuring Azure AD Single Sign-On](#configuring-azure-ad-single-single-sign-on)** - to enable your users to use this feature.
2. **[Creating an Azure AD test user](#creating-an-azure-ad-test-user)** - to test Azure AD single sign-on with Britta Simon.
3. **[Creating an Atomic Learning test user](#creating-an-atomic-learning-test-user)** - to have a counterpart of Britta Simon in Atomic Learning that is linked to the Azure AD representation of her.
4. **[Assigning the Azure AD test user](#assigning-the-azure-ad-test-user)** - to enable Britta Simon to use Azure AD single sign-on.
5. **[Testing Single Sign-On](#testing-single-sign-on)** - to verify whether the configuration works.

### Configuring Azure AD single sign-on
The objective of this section is to enable Azure AD single sign-on in the Azure classic portal and to configure single sign-on in your Atomic Learning application.

**To configure Azure AD single sign-on with Atomic Learning, perform the following steps:**

1. In the menu on the top, click **Quick Start**.
   
    ![Configure Single Sign-On][6]
2. In the classic portal, on the **Atomic Learning** application integration page, click **Configure single sign-on** to open the **Configure Single Sign-On**  dialog.
   
    ![Configure Single Sign-On][7] 
3. On the **How would you like users to sign on to Atomic Learning** page, select **Azure AD Single Sign-On**, and then click **Next**.
   
    ![Configure Single Sign-On](./media/active-directory-saas-atomiclearning-tutorial/tutorial_atomiclearning_06.png)
4. On the **Configure App Settings** dialog page, perform the following steps: 
   
    ![Configure Single Sign-On](./media/active-directory-saas-atomiclearning-tutorial/tutorial_atomiclearning_07.png)

    a. In the Sign On URL text box, type a URL using the following pattern: `https://secure2.atomiclearning.com/sso/shibboleth/<companyname>`.

    b. Click **Next**.

1. On the **Configure single sign-on at Atomic Learning** page, Click **Download metadata**, and then save the file on your computer.
   
    ![Configure Single Sign-On](./media/active-directory-saas-atomiclearning-tutorial/tutorial_atomiclearning_08.png)
2. To get SSO configured for your application, contact Atomic Learning support. They will assist with the proper channel to configure SSO. Please note that you have to send email and attach downloaded metadata file to <mailto:cs@atomiclearning.com>
3. In the classic portal, select the single sign-on configuration confirmation, and then click **Next**.
   
    ![Azure AD Single Sign-On][10]
4. On the **Single sign-on confirmation** page, click **Complete**.  
   
    ![Azure AD Single Sign-On][11]

### Creating an Azure AD test user
In this section, you create a test user in the classic portal called Britta Simon.

![Create Azure AD User][20]

**To create a test user in Azure AD, perform the following steps:**

1. In the **Azure classic portal**, on the left navigation pane, click **Active Directory**.
   
    ![Creating an Azure AD test user](./media/active-directory-saas-atomiclearning-tutorial/create_aaduser_09.png) 
2. From the **Directory** list, select the directory for which you want to enable directory integration.
3. To display the list of users, in the menu on the top, click **Users**.
   
    ![Creating an Azure AD test user](./media/active-directory-saas-atomiclearning-tutorial/create_aaduser_03.png) 
4. To open the **Add User** dialog, in the toolbar on the bottom, click **Add User**.
   
    ![Creating an Azure AD test user](./media/active-directory-saas-atomiclearning-tutorial/create_aaduser_04.png) 
5. On the **Tell us about this user** dialog page, perform the following steps:
   
    ![Creating an Azure AD test user](./media/active-directory-saas-atomiclearning-tutorial/create_aaduser_05.png) 
   
    a. As Type Of User, select New user in your organization.
   
    b. In the User Name **textbox**, type **BrittaSimon**.
   
    c. Click **Next**.
6. On the **User Profile** dialog page, perform the following steps:
   
   ![Creating an Azure AD test user](./media/active-directory-saas-atomiclearning-tutorial/create_aaduser_06.png) 
   
   a. In the **First Name** textbox, type **Britta**.  
   
   b. In the **Last Name** textbox, type, **Simon**.
   
   c. In the **Display Name** textbox, type **Britta Simon**.
   
   d. In the **Role** list, select **User**.
   
   e. Click **Next**.
7. On the **Get temporary password** dialog page, click **create**.
   
    ![Creating an Azure AD test user](./media/active-directory-saas-atomiclearning-tutorial/create_aaduser_07.png) 
8. On the **Get temporary password** dialog page, perform the following steps:
   
    ![Creating an Azure AD test user](./media/active-directory-saas-atomiclearning-tutorial/create_aaduser_08.png) 
   
    a. Write down the value of the **New Password**.
   
    b. Click **Complete**.   

### Creating a Atomic Learning test user
In this section, you create a user called Britta Simon in Atomic Learning. Atomic Learning supports just-in-time provisioning, which is by default enabled. 

There is no action item for you in this section. A new user will be created during an attempt to access Atomic Learning if it doesn't exist yet using the email address for the user.

### Assigning the Azure AD test user
In this section, you enable Britta Simon to use Azure single sign-on by granting her access to Atomic Learning.

![Assign User][200] 

**To assign Britta Simon to Atomic Learning, perform the following steps:**

1. On the classic portal, to open the applications view, in the directory view, click **Applications** in the top menu.
   
    ![Assign User][201] 
2. In the applications list, select **Atomic Learning**.
   
    ![Configure Single Sign-On](./media/active-directory-saas-atomiclearning-tutorial/tutorial_atomiclearning_09.png) 
3. In the menu on the top, click **Users**.
   
    ![Assign User][203] 
4. In the All Users list, select **Britta Simon**.
5. In the toolbar on the bottom, click **Assign**.
   
    ![Assign User][205]

### Testing single sign-on
The objective of this section is to test your Azure AD single sign-on configuration using the Access Panel.

When you click the Atomic Learning tile in the Access Panel, you should get automatically signed-on to your Atomic Learning application.

## Additional resources
* [List of Tutorials on How to Integrate SaaS Apps with Azure Active Directory](active-directory-saas-tutorial-list.md)
* [What is application access and single sign-on with Azure Active Directory?](active-directory-appssoaccess-whatis.md)

<!--Image references-->

[1]: ./media/active-directory-saas-atomiclearning-tutorial/tutorial_general_01.png
[2]: ./media/active-directory-saas-atomiclearning-tutorial/tutorial_general_02.png
[3]: ./media/active-directory-saas-atomiclearning-tutorial/tutorial_general_03.png
[4]: ./media/active-directory-saas-atomiclearning-tutorial/tutorial_general_04.png


[5]: ./media/active-directory-saas-atomiclearning-tutorial/tutorial_general_05.png
[6]: ./media/active-directory-saas-atomiclearning-tutorial/tutorial_general_06.png
[7]:  ./media/active-directory-saas-atomiclearning-tutorial/tutorial_general_050.png
[10]: ./media/active-directory-saas-atomiclearning-tutorial/tutorial_general_060.png
[11]: ./media/active-directory-saas-atomiclearning-tutorial/tutorial_general_070.png
[20]: ./media/active-directory-saas-atomiclearning-tutorial/tutorial_general_100.png

[200]: ./media/active-directory-saas-atomiclearning-tutorial/tutorial_general_200.png
[201]: ./media/active-directory-saas-atomiclearning-tutorial/tutorial_general_201.png
[203]: ./media/active-directory-saas-atomiclearning-tutorial/tutorial_general_203.png
[204]: ./media/active-directory-saas-atomiclearning-tutorial/tutorial_general_204.png
[205]: ./media/active-directory-saas-atomiclearning-tutorial/tutorial_general_205.png
