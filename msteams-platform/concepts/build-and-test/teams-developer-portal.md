---
title: Manage your apps with the Developer Portal
description: Learn how to manage your apps using the Developer Portal for Microsoft Teams.
keywords: getting started developer portal teams
localization_priority: Normal
ms.topic: overview
ms.author: surbhigupta
---

# Manage your apps with the Developer Portal for Microsoft Teams

> [!NOTE]
> The Developer Portal for Teams is currently in [public developer preview](~/resources/dev-preview/developer-preview-intro.md).

The Developer Portal for Teams is the primary tool for configuring, distributing, and managing your Microsoft Teams apps. With the Developer Portal, you can collaborate with colleagues on your app, set up runtime environments, and much more.

:::image type="content" source="../../assets/images/tdp/tdp_home_1.png" alt-text="Screenshot showing the home page of the Developer Portal for Teams.":::

## Register an app

The Developer Portal provides a couple ways to register a Teams app:

* Register a brand new app
* Import an existing app package

> [!NOTE]
> If you create an app using the [Microsoft Teams Toolkit for Visual Studio Code](https://marketplace.visualstudio.com/items?itemName=TeamsDevApp.ms-teams-vscode-extension), you can manage that app in the Developer Portal.

## Set up an environment

You can configure environments and global variables to help transition your app from your local runtime to production. Global variables are used across all environments.

**To set up an environment**

1. In the Developer Portal, select the app you're working on.
2. Go to the **Environments** page and select **+ Add an environment**.
3. Select **+ Add a variable** to create configuration variables for your environment.

**To use variables**

Use the variable names instead of hard-coded values to set your app configurations.

1. Enter `{{` in any field in the Developer Portal. A dropdown with all the variables you've created for the chosen environment along with the global variables appears.  
1. Before downloading your app package (for example, when getting ready to publish to the Teams store), select the environment you want to use. Your app configurations update automatically based on the environment. 

## Identify app owners

Each app includes an **Owners** page, where you can share your app registration with colleagues in your org. The **Contributor** role has the same permissions as the **Owner** role except the ability to delete an app.

## Configure your app's capabilities and other important metadata

A Teams app is a web app. Like all web apps, its source code is typically developed in an IDE or code editor and hosted somewhere in the cloud (like Azure).

To install and render your app in Teams, you must include a set of configurations that Teams recognizes. This has traditionally been done by crafting an app manifest, a JSON file that contains all the metadata Teams needs to display your app content. The Developer Portal abstracts this process and includes new features and tooling to help you be more successful.

## Test your app directly in Teams

The Developer Portal provides options for testing and debugging your app:

* On the **Overview** page, you can see a snapshot of whether your app's configurations validate against Teams store test cases.
* The **Preview in Teams** button lets you launch your app quickly in the Teams client for debugging.

## Distribute your app

From the Developer Portal, use the **Distribute** button to download an app package, publish to your org, or publish to the Teams store.

For more information, see [distribute your Teams app](~/concepts/deploy-and-publish/apps-publish-overview.md).

## Analyze your app's usage

On the **Overview** page, you can see the total number of active users for your app. These metrics are available for apps published to the Teams store or an org's app catalog through Developer Portal and scoped to the app ID.

| Metric | Definition |
| :-----------------------| :------------------------------------------------------------------------------------------------------|
| *Monthly R30* | The default usage metric. It shows you the count of unique active users that used your app within that rolling 30-day window in UTC. |
| *Daily* | Shows you the count of unique active users that used your app in a given day in UTC. |

You can also view the history and latency:

* *History*: Monthly and daily usage is shown for the past seven, 30 days, and 60 days. 
* *Latency*: You should see usage reflected for a given day within 24-48 hours. Usage for new apps can take up to 3-5 days to display.

## Use tools to create app features

The Developer Portal also includes tools to help you build some key features of Teams apps. Some of these tools include:

* **Scene studio**: Design custom Together mode scenes for Teams meetings.
* **Adaptive Cards editor**: Create and preview Adaptive Cards to include with your apps.
* **Microsoft identity platform management**: Register your apps with Azure Active Directory (Azure AD) to help users sign in and provide access to APIs.