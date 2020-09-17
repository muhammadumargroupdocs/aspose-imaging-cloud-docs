---
title: "Detects objects and draw it on the image"
type: docs
url: /detects-objects-and-draw-it-on-the-image/
weight: 20
---

## **Introduction**
This article explains how to detect objects and show them an existing image.

The **visualbounds** method parameters :

- name (string, required): image name. Currently, 3 image formats are supported: bmp, jpeg, and jpeg2000
- method (string, optional, ["ssd"], default "ssd"): object detection method
- threshold (number, optional, [0 - 100], default 50): minimum objects' probability in percents that will be included in the result
- includeLabel (boolean, optional, default false): whether to include detected object labels in the response
- includeScore (boolean, optional, default false): whether to include detected object probabilities in the response
- color (string, optional): custom color of the detected object bounds and info. If equals to null, objects of different labels have bounds of different colors
- folder (string, optional): folder
- storage (string, optional): storage

You can detect objects an image using one of the following two APIs:

- [GET /imaging/ai/{name}/](https://apireference.aspose.cloud/imaging/#/RotateFlip/RotateFlipImage)[visualbounds](https://apireference.aspose.cloud/imaging/#/ObjectDetection/GetVisualObjectBounds)
- [POST /imaging/ai/](https://apireference.aspose.cloud/imaging/#/RotateFlip/CreateRotateFlippedImage)[visualbounds](https://apireference.aspose.cloud/imaging/#/ObjectDetection/GetVisualObjectBounds)

The first API expects you to first upload an image to Cloud Storage then pass its name in the API URL. After the object detection, the API returns the resulting image in the response. If you would like to save the resulting image on the Cloud Storage, you explicitly need to do this as shown in the below examples.

On the other hand, with the second API, you can directly pass the image in the request body. It also lets you save the resulting image on the Cloud Storage by specifying the **outPath** parameter value. However, if you do not specify the value, the response contains a streamed image.
## **Resource URI**
[Aspose.Imaging Cloud APIs Swagger UI](https://apireference.aspose.cloud/imaging/#/RotateFlip) lets you call REST APIs directly from the browser. The description of the API and its parameters are also given there.
## **cURL Example**
- **With Storage**

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

// cURL example to detect objects an existing image

curl -v "https://api.aspose.cloud/v3/imaging/ai/object_detection_image.jpg/visualbounds?method=ssd&threshold=50&includeLabel=true&includeScore=true" \
-X GET \
-H "Content-Type: application/json" \
-H "Accept: multipart/form-data" \
-H "Authorization: Bearer <jwt token>" \
-o object_detection_image_out.jpg

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
-d 'grant_type=client_credentials&client_id=xxxx&client_secret=xxxx' \
-H "Content-Type: application/x-www-form-urlencoded" \
-H "Accept: application/json"

// cURL example to detect objects an existing image

curl -v "https://api.aspose.cloud/v3/imaging/ai/visualbounds?method=ssd&threshold=50&includeLabel=true&includeScore=true" \
-X POST \
-T object_detection_image.jpg \
-H "Content-Type: application/json" \
-H "Accept: multipart/form-data" \
-H "Authorization: Bearer <jwt token>" \
-o object_detection_image_out.jpg

```

{{< /tab >}}

{{< tab tabNum="2" >}}

```java

{image-data}

```

{{< /tab >}}

{{< /tabs >}}
## **SDKs**
Using an SDK (API client) is the quickest way for a developer to speed up the development. An SDK takes care of a lot of low-level details of making requests and handling responses and lets you focus on writing code specific to your particular project. Check out our [GitHub repository](https://github.com/aspose-imaging-cloud) for a complete list of Aspose.Imaging Cloud SDKs along with working examples, to get you started in no time. Please check [Available SDKs](/available-sdks/) article to learn how to add an SDK to your project.
## **SDK Examples**
- **With Storage**

{{< tabs tabTotal="2" tabID="7" tabName1=".NET" tabName2="Java" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cloud" "d446e6b63987c39e5a69b0ad49ec303a" "VisualBoundsAnImageInCloud.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cloud" "097cdd41e676a6134558af4b61d9d5bc" "VisualBoundsAnImageInCloud.java" >}}

{{< /tab >}}

{{< /tabs >}}

- **Without Storage**

{{< tabs tabTotal="2" tabID="8" tabName1=".NET" tabName2="Java" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cloud" "d446e6b63987c39e5a69b0ad49ec303a" "VisualBoundsAnImageInRequestBody.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cloud" "097cdd41e676a6134558af4b61d9d5bc" "VisualBoundsAnImageInRequestBody.java" >}}

{{< /tab >}}

{{< /tabs >}}
