# EXOAntiPhishRule

## Description

This resource configures an Anti-Phish Rule in Exchange Online.
Reference: https://docs.microsoft.com/en-us/powershell/module/exchange/advanced-threat-protection/new-antiphishRule?view=exchange-ps

## Parameters

AntiPhishPolicy

- Required: Yes
- Description: The Identity of the AntiPhish Policy to associate with
  this AntiPhish Rule.

Ensure

- Required: No (Defaults to 'Present')
- Description: Specifies if the configuration should be `Present` or `Absent`

Credential

- Required: Yes
- Description: Credentials of the account to authenticate with

Identity

- Required: Yes
- Description: Name of the Anti-Phish Rule

## Example

```PowerShell
        EXOAntiPhishRule TestPhishRule {
            Ensure = 'Present'
            Identity = 'TestRule'
            Credential = $Credential
            AntiPhishPolicy = 'TestPolicy'
            Enabled = $true
            Priority = 0
            RecipientDomainIs = @('contoso.com')
        }
```
