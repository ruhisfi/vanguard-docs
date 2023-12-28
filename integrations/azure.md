# Integration: Azure

## Overview

Azure integration allows you to manage users and groups in Azure AD from Entra ID.

## Playbook Actions

- `azureResetPassword` - Reset user password

## Setup

1. Open [Azure portal](https://portal.azure.com) and go to Entra ID
1. Go to **App registrations** and click **New registration**
1. Enter a name for the app and click **Register**. You can leave the other fields default.
1. Open the app and go to **Certificates & secrets** and click **New client secret**
1. Enter a description of your choosing and click **Add**
1. Copy the value of the secret and save it somewhere safe. You will not be able to see it again.
1. Go to **API permissions** and click **Add a permission**
1. Click **Microsoft Graph** and then **Application permissions**
1. Search for **User.ManageIdentities.All**, **Directory.Read.All**, **Policy.Read.All**, **AuditLog.Read.All** and **User.ReadWrite.All** and select them
1. Click **Grant admin consent for [your tenant]**, choose **Yes** and make sure the status changes to **Granted for [your tenant]**
1. Go to **Overview** and copy the **Application (client) ID** and **Directory (tenant) ID**. You will need these later.
1. Go back to Entra ID home page and click **Roles and administrators** on the left side menu
1. Click **Password Administator**
1. Click **Add assignment** and type the name of the app you just created in the search field
1. Select the app and click **Add**
1. Go back to **Roles and administrators** and click **Security Administator**
1. Click **Add assignment** and type the name of the app you just created in the search field
1. Select the app and click **Add**
1. Go to Vanguard Integrations page
1. Copy the **Client ID**, **Client Secret** and **Tenant ID** from Entra ID to the corresponding fields in Vanguard
1. Click **Save**
1. Set up the Cloud Agent
   - Copy the credentials to the configuration file on the Cloud Agent
