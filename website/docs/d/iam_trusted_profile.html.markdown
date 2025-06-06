---
layout: "ibm"
page_title: "IBM : ibm_iam_trusted_profile"
description: |-
  Get information about iam_trusted_profile
subcategory: "IAM Identity Services"
---

# ibm_iam_trusted_profile

Provides a read-only data source to retrieve information about an iam_trusted_profile. You can then reference the fields of the data source in other resources within the same configuration by using interpolation syntax.

## Example Usage

```hcl
data "ibm_iam_trusted_profile" "iam_trusted_profile" {
	profile_id = "profile_id"
}
```

## Argument Reference

You can specify the following arguments for this data source.

* `profile_id` - (Required, Forces new resource, String) ID of the trusted profile to get.

## Attribute Reference

After your data source is created, you can read values from the following attributes.

* `id` - The unique identifier of the iam_trusted_profile.
* `account_id` - (String) ID of the account that this trusted profile belong to.
* `assignment_id` - (String) ID of the assignment that was used to create an enterprise-managed trusted profile in your account. When returned, this indicates that the trusted profile is created from and managed by a template in the root enterprise account.
* `created_at` - (String) If set contains a date time string of the creation date in ISO format.
* `crn` - (String) Cloud Resource Name of the item. Example Cloud Resource Name: 'crn:v1:bluemix:public:iam-identity:us-south:a/myaccount::profile:Profile-94497d0d-2ac3-41bf-a993-a49d1b14627c'.
* `description` - (String) The optional description of the trusted profile. The 'description' property is only available if a description was provided during a create of a trusted profile.
* `entity_tag` - (String) Version of the trusted profile details object. You need to specify this value when updating the trusted profile to avoid stale updates.
* `history` - (List) History of the trusted profile.
Nested schema for **history**:
	* `action` - (String) Action of the history entry.
	* `iam_id` - (String) IAM ID of the identity which triggered the action.
	* `iam_id_account` - (String) Account of the identity which triggered the action.
	* `message` - (String) Message which summarizes the executed action.
	* `params` - (List) Params of the history entry.
	* `timestamp` - (String) Timestamp when the action was triggered.
* `iam_id` - (String) The iam_id of this trusted profile.
* `ims_account_id` - (Integer) IMS acount ID of the trusted profile.
* `ims_user_id` - (Integer) IMS user ID of the trusted profile.
* `modified_at` - (String) If set contains a date time string of the last modification date in ISO format.
* `name` - (String) Name of the trusted profile. The name is checked for uniqueness. Therefore trusted profiles with the same names can not exist in the same account.
* `template_id` - (String) ID of the IAM template that was used to create an enterprise-managed trusted profile in your account. When returned, this indicates that the trusted profile is created from and managed by a template in the root enterprise account.

