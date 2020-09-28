---
title: "Update TIFF Image Properties Without Storage"
type: docs
url: /update-tiff-image-properties-without-storage/
weight: 10
---

## **Introduction**
This article explains how to update parameters of existing TIFF image without requiring the image to be present on the Cloud Storage. Instead you pass an image in the request body. The API updates properties such as compression, resolution unit, bit depth, horizontal and vertical resolution.

You can save updated image on the Cloud Storage by specifying the **outPath** parameter value. However, if you do not specify the value, the response contains streamed image.
## **Resource URI**
[Aspose.Imaging Cloud APIs Swagger UI](https://apireference.aspose.cloud/imaging/#/Tiff/CreateModifiedTiff) lets you call this REST API directly from the browser. The description of the API and its parameters are also given there.
## **cURL Examples**
{{< tabs tabTotal="2" tabID="1" tabName1="Request" tabName2="Response" >}}

{{< tab tabNum="1" >}}

```java

// First get JSON Web Token

// Get App Key and App SID from https://dashboard.aspose.cloud/

curl -v "https://api.aspose.cloud/connect/token" \
-X POST \
-d 'grant_type=client_credentials&client_id=xxxx&client_secret=xxxx' \
-H "Content-Type: application/x-www-form-urlencoded" \
-H "Accept: application/json"

// cURL example to update parameters of existing TIFF image

curl -v "https://api.aspose.cloud/v3/imaging/tiff?compression=adobedeflate&resolutionUnit=inch&bitDepth=1&horizontalResolution=150&verticalResolution=150" \
-X POST \
-T SampleTiff.tiff \
-H "Content-Type: application/json" \
-H "Accept: multipart/form-data" \
-H "Authorization: Bearer <jwt token>" \
-o sample_out.tiff

```

{{< /tab >}}

{{< tab tabNum="2" >}}

```java

{image-data}

```

{{< /tab >}}

{{< /tabs >}}
## **SDKs**
Using an SDK (API client) is the quickest way for a developer to speed up the development. An SDK takes care of a lot of low-level details of making requests and handling responses and lets you focus on writing code specific to your particular project. Check out our [GitHub repository](https://github.com/aspose-imaging-cloud) for a complete list of Aspose.Imaging Cloud SDKs along with working examples, to get you started in no time. Please check [Available SDKs](/imaging/available-sdks/) article to learn how to add an SDK to your project.
## **SDK Examples**
{{< tabs tabTotal="2" tabID="4" tabName1=".NET" tabName2="Java" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cloud" "5910fdfab9704199ec83a715ff8b065b" "UpdateParametersOfTIFFImageInRequestBody.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cloud" "d66d31a62aa65f7dee66a6a655153f47" "UpdateParametersOfTIFFImageInRequestBody.java" >}}

{{< /tab >}}

{{< /tabs >}}
