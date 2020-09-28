---
title: "Crop a TIFF Frame"
type: docs
url: /crop-a-tiff-frame/
weight: 40
---

## **Introduction**
This article explains how to extract a frame from a TIFF image, crop it and save it separately on the storage. Crop feature requires specifying the cropping rectangle dimensions and its position on the image.

The API takes an image name as a path in the URL, therefore, you first need to upload the image to Cloud Storage. After updating the image parameters, the API returns the updated image in the response. If you would like to save the updated image on the Cloud Storage, you explicitly need to call [Upload File](https://apireference.aspose.cloud/imaging/#/File/UploadFile) API as shown in the below examples.
## **Resource URI**
With [Swagger UI](https://apireference.aspose.cloud/imaging/#/Frames/GetImageFrame) you can call this REST API directly from the browser. Description of the API parameters is also given there.
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

// cURL example to crop a TIFF frame

curl -v "https://api.aspose.cloud/v3/imaging/Sample.tiff/frames/0?x=10&y=10&rectWidth=200&rectHeight=250&saveOtherFrames=false" \
-X GET \
-H "Content-Type: application/json" \
-H "Accept: multipart/form-data" \
-H "Authorization: Bearer <jwt token>" \
-o SingleFrame_out.tiff

```

{{< /tab >}}

{{< tab tabNum="2" >}}

```java

{image-data}

```

{{< /tab >}}

{{< /tabs >}}
## **SDK Source**
Using an SDK (API client) is the quickest way for a developer to speed up the development. An SDK takes care of a lot of low-level details of making requests and handling responses and lets you focus on writing code specific to your particular project. Check out our [GitHub repository](https://github.com/aspose-imaging-cloud) for a complete list of Aspose.Imaging Cloud SDKs along with working examples, to get you started in no time. Please check [Available SDKs](/imaging/available-sdks/) article to learn how to add an SDK to your project.
## **SDK Examples**
{{< tabs tabTotal="2" tabID="4" tabName1=".NET" tabName2="Java" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cloud" "5910fdfab9704199ec83a715ff8b065b" "CropATIFFFrame.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cloud" "d66d31a62aa65f7dee66a6a655153f47" "CropATIFFFrame.java" >}}

{{< /tab >}}

{{< /tabs >}}
