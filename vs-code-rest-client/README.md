# Visual Studio Code extension: REST Client

Postman is a great tool to showcase how our APIs work. The collections are very sophisticated and provide all the details you need in order to demo our capabilities.

However, sometimes it is just great to know alternative ways to demo certain aspects. Especially from a developer perspective, Visual Studio Code seems to be the de-facto standard nowadays. VS Code has a huge ecosystem of extensions available ... and one of these is [REST Client](https://marketplace.visualstudio.com/items?itemName=humao.rest-client) created by Huachao Mao. Here is the link to the [GitHub project](https://github.com/Huachao/vscode-restclient) also with documentation and additional examples. REST Client allows you to send HTTP request and view the response in Visual Studio Code directly.

You can easily create your own scripts/documents (for the lack of a better word, I'll use scripts from now on) that include all the necessary steps that you want to focus on. Specific environments can be configured and used during the execution of these scripts. Thus making the script independent from the commercetools project that you want these requests to execute against.

An example script can be found [here](https://github.com/harrykimpel/commercetools-random/blob/main/vs-code-rest-client/vscode%20demo.http) or in the section below. In addition to API it also allows you to specify GraphQL requests. Results from an API call can be stored in variables so that you can use these in subsequent calls (see access token variable @accesssToken as an example).

As you will see, this script uses variables from an environment. This environment can be set-up in the VS Code settings.json. Please find a sample environment snippet below:

```
...
    "rest-client.environmentVariables": {  
        "$shared": {},
        "harry-kimpel-sunrise": {
            "baseAuthUrl": "https://auth.europe-west1.gcp.commercetools.com",
            "baseUrl": "https://api.europe-west1.gcp.commercetools.com",
            "project-key": "harry-kimpel-sunrise",
            "clientId": "<CLIENT-ID>",
            "clientSecret": "<CLIENT-SECRET>",
            "clientIdUser": "<CLIENT-ID>",
            "clientSecretUser": "<CLIENT-SECRET>",
            "customerUsername": "<USERNAME>",
            "customerPassword": "<PASSWORD>"
        }
    }
...
```
