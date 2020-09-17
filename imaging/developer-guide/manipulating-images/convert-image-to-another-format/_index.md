---
title: "Convert Image to Another Format"
type: docs
url: /convert-image-to-another-format/
weight: 40
---

## **Introduction**
This article explains how to convert an existing image to another format. Please check [Common Operations Format Support Map](/supported-file-formats/#supportedfileformats-export-saveas) to know the supported conversion formats.

There are two APIs to convert an image to another format:

- [GET /imaging/{name}/convert](https://apireference.aspose.cloud/imaging/#/SaveAs/SaveImageAs)
- [POST /imaging/convert](https://apireference.aspose.cloud/imaging/#/SaveAs/CreateSavedImageAs)

The first API expects you to first upload an image to Cloud Storage then pass its name in the API URL. After updating the image parameters, the API returns the updated image in the response. If you would like to save the updated image on the Cloud Storage, you explicitly need to do this as shown in the below examples.

On the other hand, with the second API, you can directly pass the image in the request body. It also lets you save the updated image on the Cloud Storage by specifying the **outPath** parameter value. However, if you do not specify the value, the response contains a streamed image.
## **Resource URI**
With [Swagger UI](https://apireference.aspose.cloud/imaging/#/SaveAs) you can call the REST API directly from the browser. Description of API parameters is also given there.
## **cURL Examples**
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

// cURL example to export an image to another format

curl -v "https://api.aspose.cloud/v3/imaging/Sample.psd/convert?format=gif" \
-X GET \
-H "Content-Type: application/json" \
-H "Accept: application/json" \
-H "Authorization: Bearer <jwt token>" \
-o Sample\_out.gif

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

// cURL example to export an image to another format

curl -v "https://api.aspose.cloud/v3/imaging/convert?format=gif" \
-X POST \
-T Sample.psd \
-H "Content-Type: application/json" \
-H "Accept: application/json" \
-H "Authorization: Bearer <jwt token>" \
-o Sample\_out.gif

```

{{< /tab >}}

{{< tab tabNum="2" >}}

```java

{image-data}

```

{{< /tab >}}

{{< /tabs >}}
## **Cloud SDKs**
Using an SDK (API client) is the quickest way for a developer to speed up the development. An SDK takes care of a lot of low-level details of making requests and handling responses and lets you focus on writing code specific to your particular project. Checkout our [GitHub repository](https://github.com/aspose-imaging-cloud) for a complete list of Aspose.Imaging Cloud SDKs along with working examples, to get you started in no time. Please check [Available SDKs](/available-sdks/) article to learn how to add an SDK to your project.
## **SDK Examples**
- **With Storage**

{{< tabs tabTotal="2" tabID="7" tabName1=".NET" tabName2="Java" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cloud" "d446e6b63987c39e5a69b0ad49ec303a" "ExportImageToAnotherFormat.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cloud" "097cdd41e676a6134558af4b61d9d5bc" "ExportImageToAnotherFormat.java" >}}

{{< /tab >}}

{{< /tabs >}}

- **Without Storage**

{{< tabs tabTotal="2" tabID="8" tabName1=".NET" tabName2="Java" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cloud" "d446e6b63987c39e5a69b0ad49ec303a" "ExportImageToAnotherFormatInRequestBody.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cloud" "097cdd41e676a6134558af4b61d9d5bc" "ExportImageToAnotherFormatInRequestBody.java" >}}

{{< /tab >}}

{{< /tabs >}}
