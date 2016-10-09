---
title: Add users from other directories or partner companies in Azure Active Directory preview | Microsoft Azure
description: Explains how to add users or change user information in Azure Active Directory, including external and guest users.
services: active-directory
documentationcenter: ''
author: curtand
manager: femila
editor: ''

ms.service: active-directory
ms.workload: identity
ms.tgt_pltfrm: na
ms.devlang: na
ms.topic: article
ms.date: 09/12/2016
ms.author: curtand

---
# Add users from other directories or partner companies in Azure Active Directory preview
> [!div class="op_single_selector"]
> * [Azure portal](active-directory-users-create-external-azure-portal.md)
> * [Azure classic portal](active-directory-create-users-external.md)
> 
> 

This article explains how to add users either from other directories in Azure Active Directory (Azure AD) preview or from partner companies. [What's in the preview?](active-directory-preview-explainer.md) For information about adding new users in your organization, and adding users who have Microsoft accounts, see [Add new users to Azure Active Directory](active-directory-users-create-azure-portal.md). Added users don't have administrator permissions by default, but you can assign roles to them at any time.

## Add a user
1. Sign in to the [Azure portal](https://portal.azure.com) with an account that's a global admin for the directory.
2. Select **More services**, enter **Users and groups** in the text box, and then select **Enter**.
   
   ![Opening user management](./media/active-directory-users-create-external-azure-portal/create-users-user-management.png)
3. On the **Users and groups** blade, select **Users**, and then select **Add**.
   
   ![Selecting the Add command](./media/ management](./media/active-directory-users-create-external-azure-portal/create-users-add-command.png)
4. On the **User** blade, provide a display name in **Name** and the user's sign-in name in **User name**.
5. Copy or otherwise note the generated user password so that you can provide it to the user after this process is complete.
6. Optionally, select **Profile** to add the users first and last name, a job title, and a department name.
   
        ![Opening the user profile](./media/ management](./media/active-directory-users-create-external-azure-portal/create-users-user-profile.png)
   
   * Select **Groups** to add the user to one or more groups.
     
       ![Adding a user to groups](./media/ management](./media/active-directory-users-create-external-azure-portal/create-users-user-groups.png)
   * Select **Organizational role** to assign the user to a role from the **Roles** list. For more information about user and administrator roles, see [Assigning administrator roles in Azure AD](active-directory-assign-admin-roles.md).
     
       ![Assigning a user to a role](./media/ management](./media/active-directory-users-create-external-azure-portal/create-users-assign-role.png)
7. Select **Create**.
8. Securely distribute the generated password to the new user so that the user can sign in.

> [!IMPORTANT]
> If your organization uses more than one domain, you should know about the following issues when you add a user account:
> 
> * TO add user accounts with the same user principal name (UPN) across domains, **first** add, for example, geoffgrisso@contoso.onmicrosoft.com, **followed by** geoffgrisso@contoso.com.
> * **Don't** add geoffgrisso@contoso.com before you add geoffgrisso@contoso.onmicrosoft.com. This order is important, and can be cumbersome to undo.
> 
> 

If you change information for a user whose identity is synchronized with your on-premises Active Directory service, you can't change the user information in the Azure classic portal. To change the user information, use your on-premises Active Directory management tools.

## What's next
* [Add a user](active-directory-users-create-azure-portal.md)
* [Reset a user's password in the new Azure portal](active-directory-users-reset-password-azure-portal.md)
* [Assign a user to a role in your Azure AD](active-directory-users-assign-role-azure-portal.md)
* [Change a user's work information](active-directory-users-work-info-azure-portal.md)
* [Manage user profiles](active-directory-users-profile-azure-portal.md)
* [Delete a user in your Azure AD](active-directory-users-delete-user-azure-portal.md)

