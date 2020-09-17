---
title: "Perform Several Operations on Image"
type: docs
url: /perform-several-operations-on-image/
weight: 70
---

## **Introduction**
This article explains how to perform scaling, cropping, flipping and exporting of an image in a single API call. The said operations can be performed using one of the following two APIs:

- [GET /imaging/{name}/updateImage](https://apireference.aspose.cloud/imaging/#/UpdateImage/UpdateImage)
- [POST /imaging/updateImage](https://apireference.aspose.cloud/imaging/#/UpdateImage/CreateUpdatedImage)

The first API expects you to first upload an image to Cloud Storage then pass its name in the API URL. After updating the image parameters, the API returns the updated image in the response. If you would like to save the updated image on the Cloud Storage, you explicitly need to call [Upload File](https://apireference.aspose.cloud/imaging/#/File/UploadFile) API as shown in the below examples.

On the other hand, with the second API, you can directly pass the image in the request body. It also lets you save the updated image on the Cloud Storage by specifying the **outPath** parameter value. However, if you do not specify the value, the response contains a streamed image.
## **Resource URI**
[Aspose.Imaging Cloud APIs Swagger UI](https://apireference.aspose.cloud/imaging/#/UpdateImage) lets you call this REST API directly from the browser. The description of the API and its parameters are also given there.
## **cURL Example**
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

// cURL example to perform scaling, cropping and flipping of an existing image in a single request

curl -v "https://api.aspose.cloud/v3/imaging/Sample.psd/updateImage?format=png&newWidth=300&newHeight=300&x=10&y=10&rectWidth=200&rectHeight=200&rotateFlipMethod=Rotate90FlipX" \
-X GET \
-H "Content-Type: application/json" \
-H "Accept: multipart/form-data" \
-H "Authorization: Bearer <jwt token>" \
-o Sample\_out.png

```

{{< /tab >}}

{{< tab tabNum="2" >}}

```java

{Image File}

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

// cURL example to perform scaling, cropping and flipping of an existing image in a single request

curl -v "https://api.aspose.cloud/v3/imaging/updateImage?format=png&newWidth=300&newHeight=300&x=10&y=10&rectWidth=200&rectHeight=200&rotateFlipMethod=Rotate90FlipX" \
-X POST \
-T Sample.psd \
-H "Content-Type: application/json" \
-H "Accept: multipart/form-data" \
-H "Authorization: Bearer <jwt token>" \
-o Sample\_out.png

```

{{< /tab >}}

{{< tab tabNum="2" >}}

```java

{Image File}

```

{{< /tab >}}

{{< /tabs >}}
## **SDKs**
Using an SDK (API client) is the quickest way for a developer to speed up the development. An SDK takes care of a lot of low-level details of making requests and handling responses and lets you focus on writing code specific to your particular project. Checkout our [GitHub repository](https://github.com/aspose-imaging-cloud) for a complete list of Aspose.Imaging Cloud SDKs along with working examples, to get you started in no time. Please check [Available SDKs](/available-sdks/) article to learn how to add an SDK to your project.
## **SDK Examples**
- **With Storage**

{{< tabs tabTotal="2" tabID="7" tabName1=".NET" tabName2="Java" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cloud" "5910fdfab9704199ec83a715ff8b065b" "UpdateImageInCloud.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cloud" "d66d31a62aa65f7dee66a6a655153f47" "UpdateImageInCloud.java" >}}

{{< /tab >}}

{{< /tabs >}}

- **Without Storage**

{{< tabs tabTotal="2" tabID="8" tabName1=".NET" tabName2="Java" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cloud" "5910fdfab9704199ec83a715ff8b065b" "UpdateImageInRequestBody.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cloud" "d66d31a62aa65f7dee66a6a655153f47" "UpdateImageInRequestBody.java" >}}

{{< /tab >}}

{{< /tabs >}}
