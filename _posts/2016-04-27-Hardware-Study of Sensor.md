---
layout: single
title: "Hardware: Study of sensors"
header:
  image: 
  teaser: 
tag: sensor
categories:
  - Hardware
author_profile: true
---

{% include toc %}

To develope products using sensors, it is essential to have a knowledge of variety of sensors. This page lists type of sensors, demonstrates about its characteristics and how they can be applied to the real world.

# Distance Sensor

|             |  Ultrasonic           | Infrared             | Laser    |
|-------------| --------------------- | -------------------- |--------- |
|**Method**   | Sound                 | Light                | Light    |
|**Frequency**| High                  | Low                  | -        |
|**Cons**     | measurement accuracy  | Object recognition   | accuracy |
|**Pros**     | environmental factors | measurement accuracy | cost     |


*Laser beam is often used to measure long distance.

## Ultrasonic

Ultrasonic sensors often enhances **distance measurement** to the object very accurately.

| PARTS          | Datasheet | 
|----------------|-----------|
| parallax: PING |[![Foo](/images/adobe_PDF_file_icon_32x32.png)](https://www.parallax.com/sites/default/files/downloads/28015-PING-Sensor-Product-Guide-v2.0.pdf) |



## Infrared 

One of the great features of using infrared sensor is thermal emission. This enhances object come and go by thermal emission. However, thermal emission should be taken carefully depends on environmental factors. the sensor only able to detect object within a range but cannot accurately sense distnace.

| PARTS          | Datasheet | 
|----------------|-----------|
|  |[![Foo](/images/adobe_PDF_file_icon_32x32.png)]() |

**Types:**

- Passive infrared sensor: 
Senses thermal radiation transferred to infrared.
    
  
- Active infrared distance sensor:
Detects returned sent light from infrared. This notifies distance in a range.

**Applications:**

Hand Dryer, Water tab, rubish bin.
