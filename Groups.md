# GAM Groups

##### Group Moderation Settings
    gam update group <group> message_moderation_level moderate_all_messages|moderate_new_members|moderate_none|moderate_non_members

##### Group Posting Settings
    gam update group <group> who_can_post_message all_in_domain_can_post|all_managers_can_post|all_members_can_post|anyone_can_post|none_can_post

>Format

    gam update group <group email> add owner|member|manager [notsuspended] {user <email address> | group <group address> | ou|ou_and_children <org name> | file <file name> | all users}

    gam print groups [domain <domain>][member <user email>] [maxresults <results>][name] [description] [admincreated] [id] [aliases][members] [owners] [managers] [settings] [todrive][delimiter <delimchar>] [fields <list,of,fields>]

##### Print All Groups (Name,Description,Members)
    gam print groups name description members > Groups.csv

##### Print All Groups, All Fields
    gam print groups allfields todrive

##### Bulk Group Ownership Changes
    gam csv GROUPs.csv gam update group ~Name add owner ~Owner
    gam csv GROUPs.csv gam update group ~Name add owner ~Owner2
    gam csv GROUPs.csv gam update group ~Name add owner ~Owner3

##### Bulk Create Groups
        gam csv todelete.csv gam create group ~Email

##### Bulk Delete Groups
    gam csv todelete.csv gam delete group ~Email
