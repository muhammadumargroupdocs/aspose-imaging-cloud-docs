---
title: "Detect undesired objects"
type: docs
url: /detect-undesired-objects/
weight: 30
---

Another way to use Aspose Object Detection API is to detect undesired object in secured areas. An application could constantly receive images from CCTV camera and send them to Aspose Object Detection Service to detect anomalies on it. For instance, such software could be used in a hospital or cafes where no pets allowed, and once the Aspose service recognizes clients with animals, it sends an alert signal to the security staff. Another example is that such an application could inform homeowners of burglars. The software can filter detected objects by labels, and therefore prevent false alarms when, for instance, a pet animal enters the dwelling.



![todo:image_alt_text](detect-undesired-objects_1.jpeg)



Further, it is possible to crop the detected object by using Aspose Imaging Cloud service and send the frame by email, for example. 



{{< gist "aspose-cloud" "097cdd41e676a6134558af4b61d9d5bc" "DetectUndesired.java" >}}
