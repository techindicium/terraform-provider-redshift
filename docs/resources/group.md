---
# generated by https://github.com/hashicorp/terraform-plugin-docs
page_title: "redshift_group Resource - terraform-provider-redshift"
subcategory: ""
description: |-
  Groups are collections of users who are all granted whatever privileges are associated with the group. You can use groups to assign privileges by role. For example, you can create different groups for sales, administration, and support and give the users in each group the appropriate access to the data they require for their work. You can grant or revoke privileges at the group level, and those changes will apply to all members of the group, except for superusers.
---

# redshift_group (Resource)

Groups are collections of users who are all granted whatever privileges are associated with the group. You can use groups to assign privileges by role. For example, you can create different groups for sales, administration, and support and give the users in each group the appropriate access to the data they require for their work. You can grant or revoke privileges at the group level, and those changes will apply to all members of the group, except for superusers.

## Example Usage

```terraform
resource "redshift_group" "staff" {
  name = "group_users"
  users = [
    redshift_user.user.name,
    redshift_user.other.name,
  ]
}
```

<!-- schema generated by tfplugindocs -->
## Schema

### Required

- **name** (String) Name of the user group. Group names beginning with two underscores are reserved for Amazon Redshift internal use.

### Optional

- **id** (String) The ID of this resource.
- **users** (Set of String) List of the user names to add to the group

