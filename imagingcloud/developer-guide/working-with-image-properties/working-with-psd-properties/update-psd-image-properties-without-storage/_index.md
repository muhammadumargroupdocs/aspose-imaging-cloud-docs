---
title: "Update PSD Image Properties Without Storage"
type: docs
url: /update-psd-image-properties-without-storage/
weight: 20
---

## **Introduction**
This article explains how to update parameters of existing PSD image without requiring the image to be present on the Cloud Storage. Instead you pass an image in the request body. You can update image properties such as count of color channels and compression method.

You can save updated image on the Cloud Storage by specifying the **outPath** parameter value. If you do not specify the value, the response contains streamed image.
## **Resource URI**
With [Aspose.Imaging Cloud APIs Swagger UI](https://apireference.aspose.cloud/imaging/#/Psd/CreateModifiedPsd), you can call the REST API directly from the browser. The description of API's parameters is also given there.
## **cURL Example**
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

// cURL example to update parameters of existing PSD image

curl -v "https://api.aspose.cloud/v3/imaging/psd?channelsCount=3&compressionMethod=raw" \

-X POST \

-T sample.psd \

-H "Content-Type: application/json" \

-H "Accept: multipart/form-data" \

-H "Authorization: Bearer <jwt token>" \

-o sample\_out.psd

```

{{< /tab >}}

{{< tab tabNum="2" >}}

```java

{image-date}

```

{{< /tab >}}

{{< /tabs >}}
## **SDKs**
Using an SDK (API client) is the quickest way for a developer to speed up the development. An SDK takes care of a lot of low-level details of making requests and handling responses and lets you focus on writing code specific to your particular project. Check out our [GitHub repository](https://github.com/aspose-imaging-cloud) for a complete list of Aspose.Imaging Cloud SDKs along with working examples, to get you started in no time. Please check [Available SDKs](/available-sdks/) article to learn how to add an SDK to your project.
## **SDK Examples**
{{< tabs tabTotal="2" tabID="4" tabName1=".NET" tabName2="Java" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cloud" "5910fdfab9704199ec83a715ff8b065b" "UpdateParametersOfPSDImageInRequestBody.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cloud" "d66d31a62aa65f7dee66a6a655153f47" "UpdateParametersOfPSDImageInRequestBody.java" >}}

{{< /tab >}}

{{< /tabs >}}
