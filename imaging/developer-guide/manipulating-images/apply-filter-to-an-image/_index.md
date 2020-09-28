---
title: "Apply filter to an Image"
type: docs
url: /apply-filter-to-an-image/
weight: 100
---

## **Introduction**
Apply filtering effects to an existing image. 

Following Filter types are supported:

- BigRectangular; 
- SmallRectangular;
- Median;
- GaussWiener;
- MotionWiener;
- GaussianBlur;
- Sharpen;
- BilateralSmoothing.

There are two APIs to crop an image:

- [PUT /imaging/{name}/filterEffect](https://apireference.aspose.cloud/imaging/#/FilterEffect/FilterEffectImage)[](https://apireference.aspose.cloud/imaging/#/Grayscale/GrayscaleImage)

The API expects you to first upload an image to Cloud Storage then pass its name in the API URL. After updating the image parameters, the API returns the updated image in the response. If you would like to save the updated image on the Cloud Storage, you explicitly need to do this as shown in the below examples.


Resource URI

[Aspose.Imaging Cloud APIs Swagger UI](https://apireference.aspose.cloud/imaging/#/Grayscale) lets you call REST APIs directly from the browser. The description of the API and its parameters are also given there.
## **cURL Example**
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

// cURL example applying filters to an image

curl -v "https://api.aspose.cloud/v3/imaging/WaterMark.bmp/filterEffect?format=gif&filterType=GaussianBlur" \
-X PUT \
-H "Content-Type: application/json" \
-H "Accept: application/json" \
-H "Authorization: Bearer " \
-o WaterMark_out.pdf \
-d '<GaussianBlurFilterOptions>

  <Radius>100</Radius>

  <Sigma>1</Sigma>

</GaussianBlurFilterOptions>'

```

{{< /tab >}}

{{< tab tabNum="2" >}}

```java

{image-data}

```

{{< /tab >}}

{{< /tabs >}}

SDKs

Using an SDK (API client) is the quickest way for a developer to speed up the development. An SDK takes care of a lot of low-level details of making requests and handling responses and lets you focus on writing code specific to your particular project. Check out our [GitHub repository](https://github.com/aspose-imaging-cloud) for a complete list of Aspose.Imaging Cloud SDKs along with working examples, to get you started in no time. Please check [Available SDKs](/imaging/available-sdks/) article to learn how to add an SDK to your project.
## **SDK Examples**
{{< tabs tabTotal="2" tabID="4" tabName1=".NET" tabName2="Java" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cloud" "d446e6b63987c39e5a69b0ad49ec303a" "FilterEffectAnImageInCloud.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}



{{< gist "aspose-cloud" "097cdd41e676a6134558af4b61d9d5bc" "FilterEffectAnImageInCloud.java" >}}

{{< /tab >}}

{{< /tabs >}}
