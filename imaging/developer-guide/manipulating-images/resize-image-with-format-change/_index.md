---
title: "Resize Image with Format Change"
type: docs
url: /resize-image-with-format-change/
weight: 10
---

## **Introduction**
This article explains how to resize an existing image and save it in another format. You can resize an image by specifying the value of new width and new height parameters. There are two APIs to resize an image:

- [GET /imaging/{name}/resize](https://apireference.aspose.cloud/imaging/#/Resize/ResizeImage)
- [POST /imaging/resize](https://apireference.aspose.cloud/imaging/#/Resize/CreateResizedImage)

The first API expects you to first upload an image to Cloud Storage then pass its name in the API URL. After updating the image parameters, the API returns the updated image in the response. If you would like to save the updated image on the Cloud Storage, you explicitly need to do this as shown in the below examples.

On the other hand, with the second API, you can directly pass the image in the request body. It also lets you save the updated image on the Cloud Storage by specifying the **outPath** parameter value. However, if you do not specify the value, the response contains a streamed image.

Please check [Common Operations Format Support Map](/supported-file-formats/#supportedfileformats-resize) to know the supported conversion formats.
## **Resource URL**
With [Swagger UI](https://apireference.aspose.cloud/imaging/#/Resize) you can call the REST API directly from the browser. Description of API parameters are also given there.
## **cURL Examples**
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

// cURL example to resize an image

curl -v "https://api.aspose.cloud/v3/imaging/WaterMark.bmp/resize?format=pdf&newWidth=400&newHeight=400" \
-X GET \
-H "Content-Type: application/json" \
-H "Accept: application/json" \
-H "Authorization: Bearer <jwt token>" \
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

// cURL example to resize an image

curl -v "https://api.aspose.cloud/v3/imaging/resize?format=pdf&newWidth=400&newHeight=400" \
-X POST \
-T WaterMark.bmp \
-H "Content-Type: application/json" \
-H "Accept: application/json" \
-H "Authorization: Bearer eyJhbGciOiJSUzI1NiIsInR5cCI6IkpXVCJ9.eyJuYmYiOjE1NTY3OTc0MzQsImV4cCI6MTU1Njg4MzgzNCwiaXNzIjoiaHR0cHM6Ly9hcGkuYXNwb3NlLmNsb3VkIiwiYXVkIjpbImh0dHBzOi8vYXBpLmFzcG9zZS5jbG91ZC9yZXNvdXJjZXMiLCJhcGkucGxhdGZvcm0iLCJhcGkucHJvZHVjdHMiXSwiY2xpZW50X2lkIjoiQjAxQTE1RTUtMUI4My00QjlBLThFQjMtMEYyQkZBNkFDNzY2Iiwic2NvcGUiOlsiYXBpLnBsYXRmb3JtIiwiYXBpLnByb2R1Y3RzIl19.Z2JrRPVvfRgbpER0tgz2216pSVLr_2OLFfUtniyIHGz3EXkDCE_Mo3EeY_vavhp5xU2q7H6UDaHILxl86ZZs_1gBEvRaEIbTrh65HjWafH61GReFgXyUYWIYjJK6C428KEU1as4yZNn98StB8X9lFGor4s6aGwhzbJQsowSKJb3eH_3nmcmfw1OgvJVLSUw8yf9VI_2Jfj6_qqzp-ICNvMGMnJAfZkcp0PP3KtzXytf-bQFnwFpvdSKBwbm03kaYbSwdMnPDKLG1OwWXx5bkIpaRL9SuvqDs8Bmy3gjylJdOUB7_OlB2dCVrSa-e46TBvOjxHJsPpe0S6MuI0POmow" \
-o WaterMark_out.pdf

```

{{< /tab >}}

{{< tab tabNum="2" >}}

```java

{image-data}

```

{{< /tab >}}

{{< /tabs >}}
## **Cloud SDKs**
Using an SDK (API client) is the quickest way for a developer to speed up the development. An SDK takes care of a lot of low-level details of making requests and handling responses and lets you focus on writing code specific to your particular project. Check out our [GitHub repository](https://github.com/aspose-imaging-cloud) for a complete list of Aspose.Imaging Cloud SDKs along with working examples, to get you started in no time. Please check [Available SDKs](/available-sdks/) article to learn how to add an SDK to your project.
## **SDK Examples**
- **With Storage**

{{< tabs tabTotal="2" tabID="7" tabName1=".NET" tabName2="Java" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cloud" "5910fdfab9704199ec83a715ff8b065b" "ResizeAnImageInCloud.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cloud" "d66d31a62aa65f7dee66a6a655153f47" "ResizeAnImageInCloud.java" >}}

{{< /tab >}}

{{< /tabs >}}

- **Without Storage**

{{< tabs tabTotal="2" tabID="8" tabName1=".NET" tabName2="Java" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cloud" "5910fdfab9704199ec83a715ff8b065b" "ResizeAnImageInRequestBody.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}



{{< gist "aspose-cloud" "d66d31a62aa65f7dee66a6a655153f47" "ResizeAnImageInRequestBody.java" >}}

{{< /tab >}}

{{< /tabs >}}
