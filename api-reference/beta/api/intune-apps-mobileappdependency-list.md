---
title: "List mobileAppDependencies"
description: "List properties and relationships of the mobileAppDependency objects."
author: "tfitzmac"
localization_priority: Normal
ms.prod: "Intune"
---

# List mobileAppDependencies

> **Important:** Microsoft Graph APIs under the /beta version are subject to change; production use is not supported.

> **Note:** The Microsoft Graph API for Intune requires an [active Intune license](https://go.microsoft.com/fwlink/?linkid=839381) for the tenant.

List properties and relationships of the [mobileAppDependency](../resources/intune-apps-mobileappdependency.md) objects.

## Prerequisites
One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).

|Permission type|Permissions (from most to least privileged)|
|:---|:---|
|Delegated (work or school account)|DeviceManagementApps.ReadWrite.All, DeviceManagementApps.Read.All|
|Delegated (personal Microsoft account)|Not supported.|
|Application|Not supported.|

## HTTP Request
<!-- {
  "blockType": "ignored"
}
-->
``` http
GET /deviceAppManagement/mobileApps/{mobileAppId}/relationships
```

## Request headers
|Header|Value|
|:---|:---|
|Authorization|Bearer &lt;token&gt; Required.|
|Accept|application/json|

## Request body
Do not supply a request body for this method.

## Response
If successful, this method returns a `200 OK` response code and a collection of [mobileAppDependency](../resources/intune-apps-mobileappdependency.md) objects in the response body.

## Example

### Request
Here is an example of the request.
``` http
GET https://graph.microsoft.com/beta/deviceAppManagement/mobileApps/{mobileAppId}/relationships
```

### Response
Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.
``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 317

{
  "value": [
    {
      "@odata.type": "#microsoft.graph.mobileAppDependency",
      "id": "c7f6f9ab-f9ab-c7f6-abf9-f6c7abf9f6c7",
      "targetId": "Target Id value",
      "targetDisplayName": "Target Display Name value",
      "dependencyType": "autoInstall",
      "dependentAppCount": 1
    }
  ]
}
```




