---
titleSuffix: Azure Cognitive Services
services: cognitive-services
author: aahill
manager: nitinme
ms.service: cognitive-services
ms.subservice: language-service
ms.topic: include
ms.date: 05/13/2022
ms.author: aahi
---


To get your project details, submit a **GET** request using the following URL and headers. Replace the placeholder values with your own values.   

```rest
{ENDPOINT}/language/authoring/analyze-conversations/projects/{PROJECT-NAME}?api-version={API-VERSION}
```

|Placeholder  |Value  | Example |
|---------|---------|---------|
|`{ENDPOINT}`     | The endpoint for authenticating your API request.   | `https://<your-custom-subdomain>.cognitiveservices.azure.com` |
|`{PROJECT-NAME}`     | The name for your project. This value is case-sensitive.  | `myProject` |
|`{API-VERSION}`     | The version of the API you are calling. The value referenced here is for the latest released [model version](../../../concepts/model-lifecycle.md#choose-the-model-version-used-on-your-data).  | `2022-03-01-preview` |

### Headers

Use the following header to authenticate your request. 

|Key|Value|
|--|--|
|`Ocp-Apim-Subscription-Key`| The key to your resource. Used for authenticating your API requests.|

### Response Body

Once you send the request, you will get the following response.

```json
{
  "createdDateTime": "{CREATED-TIME}",
  "lastModifiedDateTime": "{CREATED-TIME}",
  "lastTrainedDateTime": "{CREATED-TIME}",
  "lastDeployedDateTime": "{CREATED-TIME}",
  "projectKind": "conversation",
  "settings": {
    "confidenceThreshold": 0
  },
  "projectName": "{PROJECT-NAME}",
  "multilingual": true,
  "description": "string",
  "language": "{LANGUAGE-CODE}"
}

```

Once you send your API request, you will receive a `202` response indicating success and JSON response body with your project details.
