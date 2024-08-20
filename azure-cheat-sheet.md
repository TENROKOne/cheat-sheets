Cheatsheet with the most common Microsoft Azure PowerShell commands with examples.

`code`
# title
## title 2
### title 3
**bold**
*cursive*

# Azure Role-Based Access Control
Section about Role-Based Acces Control (RBAC) commands

## Custom Roles
### Create new custom role based on exsisting policy
Link: https://learn.microsoft.com/en-us/azure/role-based-access-control/tutorial-custom-role-powershell

- Copy base policy to Json
    - `Get-AzRoleDefinition -Name "Reader" | ConvertTo-Json`
- Change json output
- Add new role based on Json
    -`New-AzRoleDefinition -InputFile "C:\CustomRoles\ReaderSupportRole.json"`

### Get all custom roles
`Get-AzRoleDefinition | ? {$_.IsCustom -eq $true} | FT Name, IsCustom`
