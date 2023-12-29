
## Credential Permissions

|Role |Permissions|
|---|---|
|owner|Read, Update, Share, Delete|
|manager| Read, Update|
|user| Read|


## Folder Permissions

|Role |Permissions|
|---|---|
|owner|Create, Read, Update, Share, Delete|
|manager|Create, Read, Update|
|user| Read|


We will be following the google drive sharing approach for sharing credentials and folders

Only difference from google driver approach will be that when showing shared credentials we will show it under the folder tree even though the folder is not shared.

If a credential is shared multiple times using different paths, the highest access level is used

when a manger creates a credential they will only have manage  permissions.
why isnt manager given owner role for the credentials created by them?

Scenario:
1). When a person is given role for a credential

| Role | Read | Update | Share | Delete | Can see other/future credentials |  |
| ---- | ---- | ---- | ---- | ---- | ---- | ---- |
| owner | Yes | Yes | Yes | Yes | No |  |
| Manager | Yes | Yes | No | No | No |  |
| User | Yes | No | No | No | No |  |

2). If the credential shared to the person is deleted: the folder disappears?
3). Can a folder manager be made owner of a credential(not created by them) in the same folder?
4). If a user has been made folder user, they cant be made credential owner or manager?
5).If a user is made folder manager and a credential owner tries to make them credential manager, is that possible?


