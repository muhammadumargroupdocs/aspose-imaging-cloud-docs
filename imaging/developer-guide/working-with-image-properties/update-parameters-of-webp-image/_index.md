---
title: "Update Parameters of WEBP Image"
type: docs
url: /update-parameters-of-webp-image/
weight: 80
---

## **Introduction**
This article explains how to update the parameters of existing WEBP image. The API lets you update image properties such as quality, animation loop count, animation background color and lossless. Image parameters can be updated using one of the following two APIs:

- [GET /imaging/{name}/webp](https://apireference.aspose.cloud/imaging/#/WebP/ModifyWebP)
- [POST /imaging/webp](https://apireference.aspose.cloud/imaging/#/WebP/CreateModifiedWebP)

The first API expects you to first upload an image to Cloud Storage then pass its name in the API URL. After updating the image parameters, the API returns the updated image in the response. If you would like to save the updated image on the Cloud Storage, you explicitly need to do this as shown in the below examples.

On the other hand, with the second API, you can directly pass the image in the request body. It also lets you save the updated image on the Cloud Storage by specifying the **outPath** parameter value. However, if you do not specify the value, the response contains a streamed image.
## **Resource URI**
With [Swagger UI](https://apireference.aspose.cloud/imaging/#/WebP) you can call Aspose.Imaging REST APIs directly from the browser. Description of an API and its parameters are also provided there.
## **cURL Example**
- **With Storage**

{{< tabs tabTotal="2" tabID="1" tabName1="Request" tabName2="Response" >}}

{{< tab tabNum="1" >}}

```java

// First get JSON Web Token

// Get App Key and App SID from https://dashboard.aspose.cloud/

curl -v "https://api.aspose.cloud/connect/token" \
-X POST \
-d 'grant\_type=client\_credentials&client\_id=xxxx&client\_secret=xxxx' \
-H "Content-Type: application/x-www-form-urlencoded" \
-H "Accept: application/json"

// cURL example to update parameters of existing WEBP image

curl -v "https://api.aspose.cloud/v3/imaging/asposelogo.webp/webp?lossless=true&quality=90&animLoopCount=5&animBackgroundColor=gray" \
-X GET \
-H "Content-Type: application/json" \
-H "Accept: multipart/form-data" \
-H "Authorization: Bearer <jwt token>" \
-o asposelogo\_out.webp

```

{{< /tab >}}

{{< tab tabNum="2" >}}

```java

{image-data}

```

{{< /tab >}}

{{< /tabs >}}

- **Without Storage**

{{< tabs tabTotal="2" tabID="4" tabName1="Request" tabName2="Response" >}}

{{< tab tabNum="1" >}}

```java

// First get JSON Web Token

// Get App Key and App SID from https://dashboard.aspose.cloud/

curl -v "https://api.aspose.cloud/connect/token" \
-X POST \
-d 'grant\_type=client\_credentials&client\_id=xxxx&client\_secret=xxxx' \
-H "Content-Type: application/x-www-form-urlencoded" \
-H "Accept: application/json"

// cURL example to update parameters of existing WEBP image

curl -v "https://api.aspose.cloud/v3/imaging/webp?lossless=true&quality=90&animLoopCount=5&animBackgroundColor=gray" \
-X POST \
-T asposelogo.webp \
-H "Content-Type: application/json" \
-H "Accept: multipart/form-data" \
-H "Authorization: Bearer <jwt token>" \
-o asposelogo\_out.webp

```

{{< /tab >}}

{{< tab tabNum="2" >}}

```java

{image-data}

```

{{< /tab >}}

{{< /tabs >}}
## **SDKs**
Using an SDK (API client) is the quickest way for a developer to speed up the development. An SDK takes care of a lot of low-level details of making requests and handling responses and lets you focus on writing code specific to your particular project. Check out our [GitHub repository](https://github.com/aspose-imaging-cloud) for a complete list of Aspose.Imaging Cloud SDKs along with working examples, to get you started in no time. Please check [Available SDKs](/available-sdks/) article to learn how to add an SDK to your project.
## **SDK Examples**
- **With Storage**

{{< tabs tabTotal="2" tabID="7" tabName1=".NET" tabName2="Java" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cloud" "5910fdfab9704199ec83a715ff8b065b" "UpdateParametersOfWEBPImageInCloud.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cloud" "d66d31a62aa65f7dee66a6a655153f47" "UpdateParametersOfWEBPImageInCloud.java" >}}

{{< /tab >}}

{{< /tabs >}}

- **Without Storage**

{{< tabs tabTotal="2" tabID="8" tabName1=".NET" tabName2="Java" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cloud" "5910fdfab9704199ec83a715ff8b065b" "UpdateParametersOfWEBPImageInRequestBody.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cloud" "d66d31a62aa65f7dee66a6a655153f47" "UpdateParametersOfWEBPImageInRequestBody.java" >}}

{{< /tab >}}

{{< /tabs >}}
