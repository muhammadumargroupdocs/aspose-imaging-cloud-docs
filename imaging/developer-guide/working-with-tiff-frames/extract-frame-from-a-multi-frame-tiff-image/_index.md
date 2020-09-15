---
title: "Extract Frame from a Multi-Frame TIFF Image"
type: docs
url: /extract-frame-from-a-multi-frame-tiff-image/
weight: 10
---

## **Introduction**
This article explains how to get a frame from an existing TIFF image. The API also lets you resize, crop and rotateFlip the extracted frame. Moreover, the boolean parameter **saveOtherFrames** let you specify whether the result will include all other frames or just a specified frame.

The frame can be extracted using one of the following two APIs:

- [GET /imaging/{name}/frames/{frameId}](https://apireference.aspose.cloud/imaging/#/Frames/GetImageFrame)
- [POST /imaging/frames/{frameId}](https://apireference.aspose.cloud/imaging/#/Frames/CreateImageFrame)

The first API expects you to first upload an image to Cloud Storage then pass its name in the API URL. After updating the image parameters, the API returns the updated image in the response. If you would like to save the updated image on the Cloud Storage, you explicitly need to call [Upload File](https://apireference.aspose.cloud/imaging/#/File/UploadFile) API as shown in the below examples.

On the other hand, with the second API, you can directly pass the image in the request body. It also lets you save the updated image on the Cloud Storage by specifying the **outPath** parameter value. However, if you do not specify the value, the response contains a streamed image.
## **Resource URI**
With [Swagger UI](https://apireference.aspose.cloud/imaging/#/Frames/GetImageFrame) you can call Aspose.Imaging REST APIs directly from the browser. Description of an API and its parameters are also provided there.
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

// cURL example to get a frame from existing TIFF image

curl -v "https://api.aspose.cloud/v3/imaging/SampleTiff.tiff/frames/1?newWidth=300&newHeight=450&x=10&y=10&rectWidth=200&rectHeight=300&rotateFlipMethod=Rotate90FlipX&saveOtherFrames=false" \

-X GET \

-H "Content-Type: application/json" \

-H "Accept: multipart/form-data" \

-H "Authorization: Bearer <jwt token>" \

-o SingleFrame\_out.png

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

// cURL example to get a frame from existing TIFF image

curl -v "https://api.aspose.cloud/v3/imaging/frames/1?newWidth=300&newHeight=450&x=10&y=10&rectWidth=200&rectHeight=300&rotateFlipMethod=Rotate90FlipX&saveOtherFrames=false" \

-X POST \

-T SampleTiff.tiff \

-H "Content-Type: application/json" \

-H "Accept: multipart/form-data" \

-H "Authorization: Bearer <jwt token>" \

-o SingleFrame\_out.tiff

```

{{< /tab >}}

{{< tab tabNum="2" >}}

```java

{image-data}

```

{{< /tab >}}

{{< /tabs >}}
## **SDK Source**
Using an SDK (API client) is the quickest way for a developer to speed up the development. An SDK takes care of a lot of low-level details of making requests and handling responses and lets you focus on writing code specific to your particular project. Check out our [GitHub repository](https://github.com/aspose-imaging-cloud) for a complete list of Aspose.Imaging Cloud SDKs along with working examples, to get you started in no time. Please check [Available SDKs](/available-sdks/) article to learn how to add an SDK to your project.
## **SDK Examples**
- **With Storage**

{{< tabs tabTotal="2" tabID="7" tabName1=".NET" tabName2="Java" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cloud" "5910fdfab9704199ec83a715ff8b065b" "GetAFrameFromTIFFImageInCloud.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cloud" "d66d31a62aa65f7dee66a6a655153f47" "GetAFrameFromTIFFImageInCloud.java" >}}

{{< /tab >}}

{{< /tabs >}}

- **Without Storage**

{{< tabs tabTotal="2" tabID="8" tabName1=".NET" tabName2="Java" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cloud" "5910fdfab9704199ec83a715ff8b065b" "GetAFrameFromTIFFImageInRequestBody.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cloud" "d66d31a62aa65f7dee66a6a655153f47" "GetAFrameFromTIFFImageInRequestBody.java" >}}

{{< /tab >}}

{{< /tabs >}}
