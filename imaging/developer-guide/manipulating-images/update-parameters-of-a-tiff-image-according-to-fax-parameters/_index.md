---
title: "Update Parameters of a TIFF Image According to Fax Parameters"
type: docs
url: /update-parameters-of-a-tiff-image-according-to-fax-parameters/
weight: 60
---

## **Introduction**
This article explains how to update the parameters of an existing TIFF image according to fax parameters. You first need to upload the TIFF image to Cloud Storage then pass the image name in the API URL. After updating the image parameters, the API returns the updated image in the response. If you would like to save the updated image on the Cloud Storage, you explicitly need to call [Upload File](https://apireference.aspose.cloud/imaging/#/File/UploadFile) API as shown in below examples.
## **Resource**
[Aspose.Imaging Cloud APIs Swagger UI](https://apireference.aspose.cloud/imaging/#/Tiff/ConvertTiffToFax) lets you call this REST API directly from the browser. The description of all API parameters is also given there.
## **cURL Example**
{{< tabs tabTotal="2" tabID="1" tabName1="Request" tabName2="Response" >}}

{{< tab tabNum="1" >}}

```java

// First get JSON Web Token

// Get App Key and App SID from https://dashboard.aspose.cloud/

curl -v "https://api.aspose.cloud/connect/token" \
-X POST \
-d 'grant\_type=client\_credentials&client\_id=&client\_secret=' \
-H "Content-Type: application/x-www-form-urlencoded" \
-H "Accept: application/json"

// cURL example to update parameters of existing TIFF image according to fax parameters

curl -v "https://api.aspose.cloud/v3/imaging/tiff/Sample.tiff/toFax" \
-X GET \
-H "Content-Type: application/json" \
-H "Accept: multipart/form-data" \
-H "Authorization: Bearer <jwt token>" \
-o sample\_fax.tiff

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
{{< tabs tabTotal="2" tabID="4" tabName1=".NET" tabName2="Java" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cloud" "5910fdfab9704199ec83a715ff8b065b" "UpdateParametersOfTIFFImageAccordingToFaxParameters.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cloud" "d66d31a62aa65f7dee66a6a655153f47" "UpdateParametersOfTIFFImageAccordingToFaxParameters.java" >}}

{{< /tab >}}

{{< /tabs >}}
