# Automated-Compliance-Checks
A set of scripts to perform automated compliance checks on Azure AD and Intune configurations, ensuring that settings adhere to organizational policies.


Project Outline:
•	README.md: Instructions on how to use the compliance check scripts.
•	Scripts:
o	CheckAzureADCompliance.ps1: Script to check Azure AD settings.
o	CheckIntuneCompliance.ps1: Script to check Intune configurations.
o	GenerateComplianceReport.ps1: Script to generate a compliance report.

# Connect to Azure AD
Connect-AzureAD

# Check for compliance with password policies
$passwordPolicies = Get-AzureADPasswordPolicy
if ($passwordPolicies.MinLength -lt 8) {
    Write-Output "Non-compliant: Password minimum length is less than 8 characters."
} else {
    Write-Output "Compliant: Password minimum length is 8 characters or more."
}

# Additional compliance checks...
