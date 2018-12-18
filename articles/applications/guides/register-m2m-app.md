---
description: Learn to register and configure machine-to-machine (M2M) apps using the Auth0 Dashboard.
toc: true
topics:
  - applications
  - m2m
contentType: 
    - how-to
useCase:
  - build-an-app
  - add-login
  - call-api
---
# Register a Machine-to-Machine Application

To integrate Auth0 with an machine-to-machine (M2M) application, you must first register your app as an M2M App.

<%= include('./_configure', { application_type: 'M2M App', application_type_create: 'Machine to Machine Applications' }) %>

## Settings

By default, most of the settings will be created for you. However, for an M2M application, you must:

- For **Application Type**, choose Machine-to-Machine Application.

You can explore all available settings at [Dashboard Reference: Application Settings](/reference/dashboard/settings-applications). 

### Advanced Settings

By default, most of the settings will be created for you. However, for an M2M application, you must:

- Be sure that **Trust Token Endpoint IP Header** is enabled to protect against brute-force attacks on the token endpoint.

You can explore all available settings at [Dashboard Reference: Advanced Application Settings](/reference/dashboard/settings-applications-advanced). 


----

# Machine to Machine Applications

You can use machine-to-machine applications when you want to invoke an API using a non-interactive application, such as a service, command line tool, or IoT device using the [OAuth 2.0 Client Credentials Grant](/api-auth/grant/client-credentials).

## Create a new Machine to Machine Application

To create a new Machine to Machine Application:

1. Log in to the Dashboard and navigate to [Applications](${manage_url}/#/applications).

2. Click **Create Application**. When asked what type of application you'd like to create, select **Machine to Machine Application**. Click **Create** to proceed.

![Create an Application](/media/articles/applications/m2m-create.png)

2. Select the API you want to call from the application.

*If you haven't created an API yet, learn [how to configure an API in Auth0](/apis#how-to-configure-an-api-in-auth0).*

::: note
There will already be an **Auth0 Management API** that represents Auth0's APIv2. You can authorize applications to request tokens from this API.
:::

![Select an API](/media/articles/applications/m2m-select-api.png)

3. Select the scopes you want to grant to the Machine to Machine Application.

A **scope** is a claim that may be issued as part of the Access Token. With this information, the API can enforce fine-grained authorization. You can define scopes in the [API's scopes tab](/scopes/current#define-scopes-using-the-dashboard).

![Select Scopes](/media/articles/applications/m2m-select-scopes.png)

At this point, you're ready to call your API using the Machine to Machine Application. The Quick Start tab will show you how you can call your API using technologies.

![M2M Quickstarts](/media/articles/applications/m2m-quickstart.png)

To learn how to accept and validate Access Tokens in your API implementation, see the [Backend Quickstarts](/quickstart/backend).

## Settings

The Settings tab lets you edit different application settings:

- **Application Type**: The type of application you are implementing. Select **Machine to Machine Application**.
