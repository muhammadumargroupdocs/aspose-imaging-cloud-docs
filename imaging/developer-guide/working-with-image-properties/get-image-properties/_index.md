---
title: "Get Image Properties"
type: docs
url: /get-image-properties/
weight: 10
---

## **Introduction**
With Aspose.Imaging REST APIs you can get properties of an image. Image properties can be obtained using one of the following two APIs:

- [GET /imaging/{name}/properties](https://apireference.aspose.cloud/imaging/#/Properties/GetImageProperties)
- [POST /imaging/properties](https://apireference.aspose.cloud/imaging/#/Properties/ExtractImageProperties)

The first API expects you to first upload an image to Cloud Storage then pass its name in the API URL. Whereas, with the second API, you can simply pass the image in the request body.
## **Resource URI**
[Aspose.Imaging Cloud APIs Swagger UI](https://apireference.aspose.cloud/imaging/#/Properties) lets you call this REST API directly from the browser. The description of the API and its parameters are also given there.
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

// cURL example to get image properties

curl -v "https://api.aspose.cloud/v3/imaging/WaterMark.bmp/properties" \
-X GET \
-H "Content-Type: application/json" \
-H "Accept: application/json" \
-H "Authorization: Bearer <jwt token>"

```

{{< /tab >}}

{{< tab tabNum="2" >}}

```java

{

  "Height": 500,

  "Width": 500,

  "BitsPerPixel": 24,

  "BmpProperties": {

    "Compression": "Rgb"

  },

  "GifProperties": null,

  "JpegProperties": null,

  "PngProperties": null,

  "TiffProperties": null,

  "PsdProperties": null,

  "DjvuProperties": null,

  "WebPProperties": null,

  "Jpeg2000Properties": null,

  "DicomProperties": null,

  "DngProperties": null,

  "OdgProperties": null,

  "HorizontalResolution": 96.012,

  "VerticalResolution": 96.012,

  "IsCached": false,

  "Code": 200,

  "Status": "OK"

}

```

{{< /tab >}}

{{< /tabs >}}
## **SDKs**
Using an SDK (API client) is the quickest way for a developer to speed up the development. An SDK takes care of a lot of low-level details of making requests and handling responses and lets you focus on writing code specific to your particular project. Check out our [GitHub repository](https://github.com/aspose-imaging-cloud) for a complete list of Aspose.Imaging Cloud SDKs along with working examples, to get you started in no time. Please check [Available SDKs](/available-sdks/) article to learn how to add an SDK to your project.
## **SDK Examples**
- **With Storage**

{{< tabs tabTotal="2" tabID="4" tabName1=".NET" tabName2="Java" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cloud" "5910fdfab9704199ec83a715ff8b065b" "GetPropertiesOfAnImageInCloud.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cloud" "d66d31a62aa65f7dee66a6a655153f47" "GetPropertiesOfAnImageInCloud.java" >}}

{{< /tab >}}

{{< /tabs >}}

- **Without Storage**

{{< tabs tabTotal="2" tabID="5" tabName1=".NET" tabName2="Java" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cloud" "5910fdfab9704199ec83a715ff8b065b" "GetPropertiesOfAnImageInRequestBody.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cloud" "d66d31a62aa65f7dee66a6a655153f47" "GetPropertiesOfAnImageInRequestBody.java" >}}

{{< /tab >}}

{{< /tabs >}}
