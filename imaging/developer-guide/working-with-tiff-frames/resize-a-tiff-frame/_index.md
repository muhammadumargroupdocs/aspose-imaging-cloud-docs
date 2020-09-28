---
title: "Resize a TIFF Frame"
type: docs
url: /resize-a-tiff-frame/
weight: 20
---

## **Introduction**
This article explains how to extract a frame from a Tiff image, resize it and save it separately on the storage. Resize operation requires new dimensions (Width & Height) for a specified TIFF Frame.

The API takes an image name as a path in the URL, therefore, you first need to upload the image to Cloud Storage. After updating the image parameters, the API returns the updated image in the response. If you would like to save the updated image on the Cloud Storage, you explicitly need to call [Upload File](https://apireference.aspose.cloud/imaging/#/File/UploadFile) API as shown in the below examples.
## **Resource URI**
[Aspose.Imaging Cloud APIs Swagger UI](https://apireference.aspose.cloud/imaging/#/Frames/GetImageFrame) lets you call this REST API directly from the browser. The description of all API parameters is also given there.
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

// cURL example to resize a TIFF frame

curl -v "https://api.aspose.cloud/v3/imaging/Sample.tiff/frames/0?newWidth=300&newHeight=300&saveOtherFrames=false" \
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
Using an SDK (API client) is the quickest way for a developer to speed up the development. An SDK takes care of a lot of low-level details of making requests and handling responses and lets you focus on writing code specific to your particular project. Checkout our [GitHub repository](https://github.com/aspose-imaging-cloud) for a complete list of Aspose.Imaging Cloud SDKs along with working examples, to get you started in no time. Please check [Available SDKs](/imaging/available-sdks/) article to learn how to add an SDK to your project.
## **SDK Examples**
{{< tabs tabTotal="2" tabID="4" tabName1=".NET" tabName2="Java" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cloud" "5910fdfab9704199ec83a715ff8b065b" "ResizeATIFFFrame.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cloud" "d66d31a62aa65f7dee66a6a655153f47" "ResizeATIFFFrame.java" >}}

{{< /tab >}}

{{< /tabs >}}
