---
title: Managing access for Copilot in your organization
intro: 'Learn how to manage access to {% ifversion ghec %}{% data variables.product.prodname_copilot_enterprise_short %} and{% endif %} {% data variables.product.prodname_copilot_business_short %} in your organization, and review usage data to inform your decisions.'
permissions: '{% ifversion ghec %} Enterprise owners can administer access to {% data variables.product.prodname_copilot %} for organizations within the enterprise.{% endif %} Organization owners can configure access to {% data variables.product.prodname_copilot %} for members of their organization. Organization owners can also access usage data relating to {% data variables.product.prodname_copilot %} in their organization and use that data to make informed decisions about seat assignment.'
versions:
  feature: copilot
redirect_from:
  - /copilot/managing-github-copilot-in-your-organization/managing-access-for-copilot-business-in-your-organization
  - /copilot/managing-copilot-for-business/managing-access-for-copilot-for-business-in-your-organization
  - /copilot/managing-copilot-business/managing-access-for-copilot-business-in-your-organization
topics:
  - Copilot
shortTitle: Managing access
---

## About managing access to {% data variables.product.prodname_copilot %} in your organization

{% ifversion ghec %}{% data variables.product.prodname_copilot_enterprise %} and {% endif %}{% data variables.product.prodname_copilot_for_business %} {% ifversion ghec %}are{% else %}is a{% endif %} {% data variables.product.prodname_copilot %} subscription{% ifversion ghec %}s{% endif %}, billed and administered at the organization {% ifversion ghec %}or enterprise {% endif %}level. {% ifversion ghec %}

Enterprise owners can enable or disable {% data variables.product.prodname_copilot %} for organizations within their enterprise. For more information, see "[AUTOTITLE](/admin/policies/enforcing-policies-for-your-enterprise/enforcing-policies-for-github-copilot-in-your-enterprise#managing-access-to-github-copilot-in-your-enterprise)."

{% endif %}Organization owners can administer access to {% data variables.product.prodname_copilot_short %} for teams and individuals within the organization. Organization owners can also access usage data relating to {% data variables.product.prodname_copilot %} in their organization, and use that data to make informed decisions about seat assignment.

Organization{% ifversion ghec %} and enterprise{% endif %} owners can manage various policies for {% data variables.product.prodname_copilot_short %}, such as whether to allow or block suggestions that match public code. For more information{% ifversion ghec %} about managing policies at the organization level{% endif %}, see "[AUTOTITLE](/copilot/managing-github-copilot-in-your-organization/managing-policies-and-features-for-copilot-in-your-organization)."{% ifversion ghec %} For more information about managing policies at the enterprise level, see "[AUTOTITLE](/enterprise-cloud@latest/admin/policies/enforcing-policies-for-your-enterprise/enforcing-policies-for-github-copilot-in-your-enterprise)" {% endif %}

## Configuring access to {% data variables.product.prodname_copilot %} in your organization

{% ifversion ghec %}After a {% data variables.product.prodname_dotcom %} enterprise owner has enabled a {% data variables.product.prodname_copilot_enterprise_short %} or {% data variables.product.prodname_copilot_business_short %} subscription for an organization, an owner of that organization can assign {% data variables.product.prodname_copilot %} seats to individuals and teams in the organization.{% else %}After setting up a {% data variables.product.prodname_copilot_business_short %} subscription, an organization owner can manage their organization members' access to {% data variables.product.prodname_copilot %}.{% endif %} Granting access to {% data variables.product.prodname_copilot %} requires a seat for each organization member you want to include.

### Enabling access to {% data variables.product.prodname_copilot %} for all current and future users in your organization

{% data reusables.profile.access_org %}
{% data reusables.profile.org_settings %}
{% data reusables.copilot.access-settings %}
1. Under "{% data variables.product.prodname_copilot_short %} in your organization," to enable {% data variables.product.prodname_copilot %} for all current and future users in your organization, select **Enabled For: All members of the organization**.
1. In the "Confirm seat assignment" dialog, to confirm that you want to enable {% data variables.product.prodname_copilot %} for all current and future users in your organization, click **Confirm**.
1. To save your changes, click **Save**.

### Enabling access to {% data variables.product.prodname_copilot %} for specific users in your organization

{% ifversion ghec %}
{% note %}

**Note:** You can automatically enable access for every member of a group in your identity provider (IdP) by synchronizing that group with a {% data variables.product.prodname_dotcom %} team, then giving that team access to {% data variables.product.prodname_copilot %}.  For more information, see "[AUTOTITLE](/organizations/organizing-members-into-teams/synchronizing-a-team-with-an-identity-provider-group)."

{% endnote %}
{% endif %}

{% data reusables.profile.access_org %}
{% data reusables.profile.org_settings %}
{% data reusables.copilot.access-settings %}
1. Under "{% data variables.product.prodname_copilot_short %} in your organization," to enable {% data variables.product.prodname_copilot %} for selected teams or users in your organization, select **Enabled For: Selected members**.
1. If you are updating user access from the **Enabled For: All members of the organization** setting, in the "Confirm seat assignment" dialog, select how you want to start assigning access.
    - To unassign all members and then select those who should have access, select **Start from scratch**.
    - To keep all members who currently have access and then select those who should not have access, select **Keep all users**.
1. If you selected **Start from scratch**, click **Add seats**.
1. If you selected **Add seats**, in the "Enable {% data variables.product.prodname_copilot %} access to users and teams" dialog, you can either search for and add individual users or teams, or you can click **Upload CSV** to add members in bulk by uploading a CSV file.

   ![Screenshot of the "enable access for selected members" dialog.](/assets/images/help/copilot/enable-access-for-selected-members.png)

    - To search for users, type their username or full name in the search bar. If you select a user who is not currently a member of your organization, they will be invited to join your organization when you click **Continue to purchase** followed by **Purchase seats**.
    - To add members in bulk, click **Upload CSV**, and then upload a CSV file including either the username or email address for each member you want to add, separated by a comma. The file can contain a mixture of usernames and email addresses.

        {% warning %}

      **Warning:** When you upload a CSV file, {% data variables.product.prodname_copilot %} will search all users on {% data variables.product.prodname_dotcom_the_website %} for matches. If the CSV includes users who are not members of your organization, they will be invited to join your organization when you click **Continue to purchase** followed by **Purchase seats**.

      {% endwarning %}

    - Review the list of users generated from your CSV file. To confirm that you want to grant access to the listed users, click **Continue to purchase** followed by **Purchase seats**. To reject the list, click **Cancel**.

1. If you selected **Keep all users**, review the full list of your organization members and select the individuals whose {% data variables.product.prodname_copilot %} you want to revoke.
1. To confirm the revocation of access for the selected members, at the top of the list of members, click **Cancel seat**.

### Revoking access to {% data variables.product.prodname_copilot %} for your whole organization

{% data reusables.copilot.disable-copilot-organization %}

### Revoking access to {% data variables.product.prodname_copilot %} for specific users in your organization

Removing a user from the organization(s) that had assigned them a {% data variables.product.prodname_copilot %} seat will automatically unassign the seat from them. Alternatively, you can unassign a member's {% data variables.product.prodname_copilot %} seat while preserving their membership. These changes will take effect at the beginning of the next billing cycle.

{% data reusables.profile.access_org %}
{% data reusables.profile.org_settings %}
{% data reusables.copilot.access-settings %}
1. Under "{% data variables.product.prodname_copilot_short %} in your organization," select **Enabled For: selected members**.

    - In the "Confirm seat assignment" dialog, click **Keep all users**.

1. Under "Access for users and teams," in the search bar, type the member's username or full name.
1. To remove the member from the list of users who have access to {% data variables.product.prodname_copilot %}, select the checkbox to the left of their username, then click **Cancel seat**.
1. In the "Confirm seat removal" dialog, click **Remove seats**.

## Reviewing usage data for {% data variables.product.prodname_copilot %} in your organization

You can review usage data for {% data variables.product.prodname_copilot %} in your organization to help you make informed decisions about seat assignment.

{% data reusables.profile.access_org %}
{% data reusables.profile.org_settings %}
{% data reusables.copilot.access-settings %}
1. At the top of the page, under "{% data variables.product.prodname_copilot %}," you can see an overview of your organization's {% data variables.product.prodname_copilot %} usage. You can see the number seats assigned through your {% ifversion ghec %}{% data variables.product.prodname_copilot_enterprise_short %} or {% endif %}{% data variables.product.prodname_copilot_business_short %} subscription, and the estimated monthly cost.

   {% ifversion ghec %}
   ![Screenshot of the {% data variables.product.prodname_copilot %} usage overview.](/assets/images/help/copilot/copilot-usage-overview-enterprise.png)
   {% else %}
   ![Screenshot of the {% data variables.product.prodname_copilot %} usage overview.](/assets/images/help/copilot/copilot-usage-overview.png)
   {% endif %}

1. For more detailed information, next to "Access for users and teams," click **Get report**.
    - {% data variables.product.prodname_dotcom %} will generate a report for you, which you can download as a CSV file.
1. Alternatively, under "Access for users and teams," you can use the **Sort** options to sort the list of users by when they last used {% data variables.product.prodname_copilot %}.

## Further reading

- "[AUTOTITLE](/free-pro-team@latest/site-policy/privacy-policies/github-copilot-for-business-privacy-statement)"
