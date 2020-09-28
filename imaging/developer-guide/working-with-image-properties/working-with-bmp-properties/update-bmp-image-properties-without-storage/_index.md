---
title: "Update BMP Image Properties Without Storage"
type: docs
url: /update-bmp-image-properties-without-storage/
weight: 10
---

## **Introduction**
This article explains how to update BMP specific properties without requiring the image to be present on the Cloud Storage. Instead you pass an image in the request body. You can update bitmap image properties such as color depth, horizontal resolution and vertical resolution. Moreover, the API also supports the Device Independent Bitmap (DIP) file format.

You can save updated image on the Cloud Storage by specifying the **outPath** parameter value. However, if you do not specify the value, the response contains streamed image.
## **Resource URI**
[Aspose.Imaging Cloud APIs Swagger UI](https://apireference.aspose.cloud/imaging/#/Bmp/CreateModifiedBmp) lets you call this REST API directly from the browser. The description of the API and its parameters are also given there.
## **cURL Example**
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

// cURL example to update parameters of BMP image

curl -v "https://api.aspose.cloud/v3/imaging/bmp?bitsPerPixel=32&horizontalResolution=300&verticalResolution=300" \
-X POST \
-T WaterMark.bmp \
-H "Content-Type: application/json" \
-H "Accept: application/json" \
-H "Authorization: Bearer <jwt token>" \
-o WaterMark_out.bmp

```

{{< /tab >}}

{{< tab tabNum="2" >}}

```java

Updated BMP Image

```

{{< /tab >}}

{{< /tabs >}}
## **SDKs**
Using an SDK (API client) is the quickest way for a developer to speed up the development. An SDK takes care of a lot of low-level details of making requests and handling responses and lets you focus on writing code specific to your particular project. Checkout our [GitHub repository](https://github.com/aspose-imaging-cloud) for a complete list of Aspose.Imaging Cloud SDKs along with working examples, to get you started in no time. Please check [Available SDKs](/imaging/available-sdks/) article to learn how to add an SDK to your project.
## **SDK Examples**
{{< tabs tabTotal="2" tabID="4" tabName1=".NET" tabName2="Java" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cloud" "5910fdfab9704199ec83a715ff8b065b" "UpdateParametersOfBMPImageInRequestBody.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cloud" "d66d31a62aa65f7dee66a6a655153f47" "UpdateParametersOfBMPImageInRequestBody.java" >}}

{{< /tab >}}

{{< /tabs >}}
