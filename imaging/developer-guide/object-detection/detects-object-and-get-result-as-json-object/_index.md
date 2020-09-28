---
title: "Detects object and get result as json object"
type: docs
url: /detects-object-and-get-result-as-json-object/
weight: 10
---

## **Introduction**
This article explains how to detect objects in an existing image.

The **bounds** method parameters :

- name (string, required): image name. Currently, 3 image formats are supported: bmp, jpeg, and jpeg2000
- method (string, optional, ["ssd"], default "ssd"): object detection method
- threshold (number, optional, [0 - 100], default 50): minimum objects' probability in percents that will be included in the result
- includeLabel (boolean, optional, default false): whether to include detected object labels in the response
- includeScore (boolean, optional, default false): whether to include detected object probabilities in the response
- folder (string, optional): folder
- storage (string, optional): storage

You can detect objects an image using one of the following two APIs:

- [GET /imaging/ai/{name}/](https://apireference.aspose.cloud/imaging/#/RotateFlip/RotateFlipImage)[bounds](https://apireference.aspose.cloud/imaging/#/ObjectDetection/GetVisualObjectBounds)
- [POST /imaging/ai/](https://apireference.aspose.cloud/imaging/#/RotateFlip/CreateRotateFlippedImage)[bounds](https://apireference.aspose.cloud/imaging/#/ObjectDetection/GetVisualObjectBounds)

The first API expects you to first upload an image to Cloud Storage then pass its name in the API URL. After the object detection, the API returns the result as a json object in the response. 

On the other hand, with the second API, you can directly pass the image in the request body. It also lets you save the loaded image on the Cloud Storage by specifying the **outPath** parameter value. The response contains the result as a json object.
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

curl -v "https://api.aspose.cloud/v3/imaging/ai/object_detection_image.jpg/bounds?method=ssd&threshold=50&includeLabel=true&includeScore=true" \
-X GET \
-H "Content-Type: application/json" \
-H "Accept: multipart/form-data" \
-H "Authorization: Bearer <jwt token>" \
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```java

{

   "detectedObjects": [

       {

           "score": 0.599537253,

           "label": "dog",

           "bounds": {

               "x": 33.0,

               "y": -1.0,

               "width": 510.0,

               "height": 352.0

           }

       },

       {

           "score": 0.66614604,

            "label": "cat",

           "bounds": {

               "x": 37.0,

               "y": 3.0,

               "width": 493.0,

               "height": 344.0

           }

       }

   ]

}

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

curl -v "https://api.aspose.cloud/v3/imaging/ai/bounds?method=ssd&threshold=50&includeLabel=true&includeScore=true" \
-X POST \
-T object_detection_image.jpg \
-H "Content-Type: application/json" \
-H "Accept: multipart/form-data" \
-H "Authorization: Bearer <jwt token>" \
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```java

{

   "detectedObjects": [

       {

           "score": 0.599537253,

           "label": "dog",

           "bounds": {

               "x": 33.0,

               "y": -1.0,

               "width": 510.0,

               "height": 352.0

           }

       },

       {

           "score": 0.66614604,

            "label": "cat",

           "bounds": {

               "x": 37.0,

               "y": 3.0,

               "width": 493.0,

               "height": 344.0

           }

       }

   ]

}

```

{{< /tab >}}

{{< /tabs >}}
## **SDKs**
Using an SDK (API client) is the quickest way for a developer to speed up the development. An SDK takes care of a lot of low-level details of making requests and handling responses and lets you focus on writing code specific to your particular project. Check out our [GitHub repository](https://github.com/aspose-imaging-cloud) for a complete list of Aspose.Imaging Cloud SDKs along with working examples, to get you started in no time. Please check [Available SDKs](/imaging/available-sdks/) article to learn how to add an SDK to your project.
## **SDK Examples**
- **With Storage**

{{< tabs tabTotal="2" tabID="7" tabName1=".NET" tabName2="Java" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cloud" "d446e6b63987c39e5a69b0ad49ec303a" "BoundsAnImageInCloud.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cloud" "097cdd41e676a6134558af4b61d9d5bc" "BoundsAnImageInCloud.java" >}}

{{< /tab >}}

{{< /tabs >}}

- **Without Storage**

{{< tabs tabTotal="2" tabID="8" tabName1=".NET" tabName2="Java" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cloud" "d446e6b63987c39e5a69b0ad49ec303a" "BoundsAnImageInRequestBody.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cloud" "097cdd41e676a6134558af4b61d9d5bc" "BoundsAnImageInRequestBody.java" >}}

{{< /tab >}}

{{< /tabs >}}
