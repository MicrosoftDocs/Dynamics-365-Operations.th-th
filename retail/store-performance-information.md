---
title: "วิเคราะห์ประสิทธิภาพร้านค้า"
description: "บทความนี้อธิบายวิธีใช้การวิเคราะห์ในหน่วยความจำแบบเรียลไทม์เพื่อเข้าถึง สำรวจ และรับความช่วยเหลือเกี่ยวกับประสิทธิภาพร้านค้าจากข้อมูลของ Microsoft Dynamics 365 for Operations"
author: josaw1
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core, Retail
ms.custom: 57811
ms.assetid: 495a66f0-491a-4688-842d-51c33c37676f
ms.search.region: global
ms.search.industry: Retail
ms.author: asharchw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: 6b1f91f863c8da35362ebb3036e76aa10d95ba65
ms.openlocfilehash: dcd3e20e9e6a979aff8498f542be35ea5813bc99
ms.contentlocale: th-th
ms.lasthandoff: 04/26/2017


---

# <a name="analyze-store-performance"></a>วิเคราะห์ประสิทธิภาพร้านค้า

[!include[banner](includes/banner.md)]


บทความนี้อธิบายวิธีใช้การวิเคราะห์ในหน่วยความจำแบบเรียลไทม์เพื่อเข้าถึง สำรวจ และรับความช่วยเหลือเกี่ยวกับประสิทธิภาพร้านค้าจากข้อมูลของ Microsoft Dynamics 365 for Operations 

เนื่องจากเป็นส่วนหนึ่งของ Microsoft Dynamics 365 for Operations ผู้ใช้สามารถศึกษาประสิทธิภาพการจัดเก็บในเวลาจริงระหว่างลำดับชั้นขององค์กรระดับต่างๆ ณ รอบระยะเวลาที่เลือก โดยการเปิดรายงาน **สรุปช่องทาง** แบบ out-of-box จากที่ตั้งใดๆต่อไปนี้:

-   **การจัดการร้านค้าปลีก** พื้นที่ทำงาน Dynamics 365 for Operations &gt; **การขายปลีกและการค้า** &gt; **ช่องทาง** &gt; **การจัดการร้านค้าปลีก** &gt; **รายงาน** &gt; **รายงานสรุปช่องทาง**
-   **การเงินของร้านค้าปลีก** พื้นที่ทำงาน Dynamics 365 for Operations &gt; **การขายปลีกและการค้า** &gt; **ช่องทาง** &gt; **การเงินของร้านค้าปลีก** &gt; **รายงาน** &gt; **รายงานสรุปช่องทาง**
-   **การสอบถามและรายงาน** ส่วน Dynamics 365 for Operations &gt; **การขายปลีกและการค้า** &gt; **การสอบถามและรายงาน** &gt; **รายงานการขาย** &gt; **รายงานสรุปช่องทาง**

รายงานนี้แสดงสแนปช็อตของข้อสรุปต่อไปนี้ซึ่งเป็นส่วนหนึ่งของประสิทธิภาพการทำงานของร้านค้า:

-   สรุปยอดขายรวม
-   สรุปชนิดการชำระเงิน
-   สรุปภาษี
-   สรุปการแทนที่ราคา
-   สรุปส่วนลด



