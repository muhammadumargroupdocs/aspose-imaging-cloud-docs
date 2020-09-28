---
title: "Grayscale an Image"
type: docs
url: /grayscale-an-image/
weight: 80
---

## **Introduction**
Grayscale method allows to turn all colors of an image to a shades of gray

There are two APIs to crop an image:

- [GET /imaging/{name}/grayscale](https://apireference.aspose.cloud/imaging/#/Grayscale/GrayscaleImage)
- [POST /imaging/grayscale](https://apireference.aspose.cloud/imaging/#/Grayscale/CreateGrayscaledImage)

The first API expects you to first upload an image to Cloud Storage then pass its name in the API URL. After updating the image parameters, the API returns the updated image in the response. If you would like to save the updated image on the Cloud Storage, you explicitly need to do this as shown in the below examples.
On the other hand, with the second API, you can directly pass the image in the request body. It also lets you save the updated image on the Cloud Storage by specifying the outPath parameter value. However, if you do not specify the value, the response contains a streamed image.

Please check Common Operations Format Support Map to know the supported conversion formats.
## **Resource URI**
[Aspose.Imaging Cloud APIs Swagger UI](https://apireference.aspose.cloud/imaging/#/Grayscale) lets you call REST APIs directly from the browser. The description of the API and its parameters are also given there.
## **cURL Example**
- **With Storage**

{{< tabs tabTotal="2" tabID="1" tabName1="Request" tabName2="Response" >}}

{{< tab tabNum="1" >}}

```java

/// First get JSON Web Token

// Get App Key and App SID from https://dashboard.aspose.cloud/

curl -v "https://api.aspose.cloud/connect/token" \
-X POST \
-d 'grant_type=client_credentials&client_id=xxxx&client_secret=xxxx' \
-H "Content-Type: application/x-www-form-urlencoded" \
-H "Accept: application/json"

// cURL example to grayscale an image

curl -v "https://api.aspose.cloud/v3/imaging/WaterMark.bmp/grayscale" \
-X GET \
-H "Content-Type: application/json" \
-H "Accept: application/json" \
-H "Authorization: Bearer " \
-o WaterMark_out.pdf

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

// cURL example to grayscale an existing image

curl -v "https://api.aspose.cloud/v3/imaging/grayscale" \
-X POST \
-T WaterMark.bmp \
-H "Content-Type: application/json" \
-H "Accept: multipart/form-data" \
-H "Authorization: Bearer <jwt token>" \
-o WaterMark_out.png

```

{{< /tab >}}

{{< tab tabNum="2" >}}

```java

{image-data}

```

{{< /tab >}}

{{< /tabs >}}
## **SDKs**
Using an SDK (API client) is the quickest way for a developer to speed up the development. An SDK takes care of a lot of low-level details of making requests and handling responses and lets you focus on writing code specific to your particular project. Check out our [GitHub repository](https://github.com/aspose-imaging-cloud) for a complete list of Aspose.Imaging Cloud SDKs along with working examples, to get you started in no time. Please check [Available SDKs](/imaging/available-sdks/) article to learn how to add an SDK to your project.
## **SDK Examples**
- **With Storage**

{{< tabs tabTotal="2" tabID="7" tabName1=".NET" tabName2="Java" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cloud" "d446e6b63987c39e5a69b0ad49ec303a" "GrayscaleAnImageInCloud.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}



{{< gist "aspose-cloud" "097cdd41e676a6134558af4b61d9d5bc" "GrayscaleAnImageInCloud.java" >}}

{{< /tab >}}

{{< /tabs >}}

- **Without Storage**

{{< tabs tabTotal="2" tabID="8" tabName1=".NET" tabName2="Java" >}}

{{< tab tabNum="1" >}}



{{< gist "aspose-cloud" "d446e6b63987c39e5a69b0ad49ec303a" "GrayscaleAnImageInRequestBody.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}



{{< gist "aspose-cloud" "097cdd41e676a6134558af4b61d9d5bc" "GrayscaleAnImageInRequestBody.java" >}}

{{< /tab >}}

{{< /tabs >}}
