---
ms.localizationpriority: medium
---

<!-- markdownlint-disable MD041 -->

Begin by creating a new Node.js project. Open your command-line interface (CLI) in a directory where you want to create the project. Run the following command.

```bash
npm init
```

Answer the prompts by either supplying your own values or accepting the defaults.

## Install dependencies

Before moving on, add some additional dependencies that you will use later.

- [Azure Identity client library for JavaScript](https://www.npmjs.com/package/@azure/identity)  to authenticate the user and acquire access tokens.
- [Microsoft Graph JavaScript client library](https://www.npmjs.com/package/@microsoft/microsoft-graph-client) to make calls to the Microsoft Graph.
- [isomorphic-fetch](https://www.npmjs.com/package/isomorphic-fetch) to add `fetch` API to Node.js. This is a dependency for the Microsoft Graph JavaScript client library.
- [readline-sync](https://www.npmjs.com/package/readline-sync) for prompting the user for input.

Run the following commands in your CLI to install the dependencies.

```bash
npm install @azure/identity @microsoft/microsoft-graph-client isomorphic-fetch readline-sync
```

## Load application settings

In this section you'll add the details of your app registration to the project.

1. Create a file in the root of your project named **appSettings.js** and add the following code.

    :::code language="javascript" source="./src/user-auth/graphtutorial/appSettings.example.js" id="SettingsSnippet":::

1. Update the values in `settings` according to the following table.

    | Setting | Value |
    |---------|-------|
    | `clientId` | The client ID of your app registration |
    | `tenantId` | If you chose the option to only allow users in your organization to sign in, change this value to your tenant ID. Otherwise leave as `common`. |

## Design the app

In this section you will create a simple console-based menu.

1. Create a file in the root of your project named **graphHelper.js** and add the following placeholder code. You'll add more code this file in later steps.

    ```javascript
    module.exports = {};
    ```

1. Create a file in the root of your project named **index.js** and add the following code.

    :::code language="javascript" source="./src/user-auth/graphtutorial/index.js" id="ProgramSnippet":::

1. Add the following placeholder methods at the end of the file. You'll implement them in later steps.

    ```javascript
    function initializeGraph(settings) {
      // TODO
    }

    async function greetUserAsync() {
      // TODO
    }

    async function displayAccessTokenAsync() {
      // TODO
    }

    async function listInboxAsync() {
      // TODO
    }

    async function sendMailToSelfAsync() {
      // TODO
    }

    async function doGraphCallAsync() {
      // TODO
    }
    ```

This implements a basic menu and reads the user's choice from the command line.
