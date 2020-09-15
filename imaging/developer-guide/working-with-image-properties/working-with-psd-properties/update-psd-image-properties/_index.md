---
title: "Update PSD Image Properties"
type: docs
url: /update-psd-image-properties/
weight: 10
---

## **Introduction**
This article explains how to update the parameters of existing PSD image. You can update properties such as count of color channels and compression method of a PSD file residing on the storage.

The API takes an image name as a path in the URL, therefore, you first need to upload the image to Cloud Storage. After updating the image parameters, the API returns the updated image in the response. If you would like to save the updated image on the Cloud Storage, you explicitly need to do this as shown in the below examples.
## **Resource URI**
[Aspose.Imaging Cloud APIs Swagger UI](https://apireference.aspose.cloud/imaging/#/Psd/ModifyPsd) lets you call this REST API directly from the browser. The description of the API and its parameters are also given there.
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

curl -v "https://api.aspose.cloud/v3/imaging/sample.psd/psd?channelsCount=3&compressionMethod=raw" \

-X GET \

-H "Content-Type: application/json" \

-H "Accept: multipart/form-data" \

-H "Authorization: Bearer <jwt token>" \

-o sample\_out.psd

```

{{< /tab >}}

{{< tab tabNum="2" >}}

```java

{image-data} 

```

{{< /tab >}}

{{< /tabs >}}
## **SDKs**
Using an SDK (API client) is the quickest way for a developer to speed up the development. An SDK takes care of a lot of low-level details of making requests and handling responses and lets you focus on writing code specific to your particular project. Checkout our [GitHub repository](https://github.com/aspose-imaging-cloud) for a complete list of Aspose.Imaging Cloud SDKs along with working examples, to get you started in no time. Please check [Available SDKs](/available-sdks/) article to learn how to add an SDK to your project.
## **SDK Examples**
{{< tabs tabTotal="2" tabID="4" tabName1=".NET" tabName2="Java" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cloud" "5910fdfab9704199ec83a715ff8b065b" "UpdateParametersOfPSDImageInCloud.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cloud" "d66d31a62aa65f7dee66a6a655153f47" "UpdateParametersOfPSDImageInCloud.java" >}}

{{< /tab >}}

{{< /tabs >}}
