---
title: วิเคราะห์ประสิทธิภาพร้านค้า
description: บทความนี้อธิบายวิธีที่คุณสามารถใช้การวิเคราะห์แบบในหน่วยความจำหรือแบบเรียลไทม์เพื่อเข้าถึง สำรวจ และรับข้อมูลเชิงลึกเกี่ยวกับประสิทธิภาพร้านค้า โดยขึ้นกับ Microsoft Dynamics 365 for Retail ของคุณ
author: ashishmsft
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: RetailChannelReport, RetailChannelManagementWorkspace
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 57811
ms.assetid: 495a66f0-491a-4688-842d-51c33c37676f
ms.search.region: global
ms.search.industry: Retail
ms.author: asharchw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: c975c021b6db49d1e25fd036f4955c7223e438ea
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 01/29/2019
ms.locfileid: "346191"
---
# <a name="analyze-store-performance"></a>วิเคราะห์ประสิทธิภาพร้านค้า

[!include [banner](includes/banner.md)]

บทความนี้อธิบายวิธีที่คุณสามารถใช้การวิเคราะห์แบบในหน่วยความจำหรือแบบเรียลไทม์เพื่อเข้าถึง สำรวจ และรับข้อมูลเชิงลึกเกี่ยวกับประสิทธิภาพร้านค้า โดยขึ้นกับ Microsoft Dynamics 365 for Retail ของคุณ

ในฐานะที่เป็นส่วนหนึ่งของ Dynamics 365 for Retail ผู้ใช้สามารถศึกษาประสิทธิภาพร้านค้าได้แบบเรียลไทม์ในระดับต่างๆ ของลำดับชั้นองค์กรตลอดช่วงเวลาที่เลือกโดยการเปิดรายงาน **สรุปช่องทาง** แบบสำเร็จรูปจากสถานที่ใดๆ ต่อไปนี้:

- **การจัดการร้านค้าปลีก** พื้นที่ทำงาน&gt; **Retail** &gt; **ช่องทาง** &gt; **การจัดการร้านค้าปลีก** &gt; **Reports** &gt; **รายงานสรุปช่องทาง**
- **การเงินของร้านค้าปลีก** พื้นที่ทำงาน &gt; **Retail** &gt; **ช่องทาง** &gt; **การเงินของร้านค้าปลีก** &gt; **รายงาน** &gt; **รายงานสรุปช่องทาง**
- **การสอบถามและรายงาน** ส่วน &gt; **การขายปลีก** &gt; **การสอบถามและรายงาน** &gt; **รายงานการขาย** &gt; **รายงานสรุปช่องทาง**

รายงานนี้แสดงสแนปช็อตของข้อสรุปต่อไปนี้ซึ่งเป็นส่วนหนึ่งของประสิทธิภาพการทำงานของร้านค้า:

- สรุปยอดขายรวม
- สรุปชนิดการชำระเงิน
- สรุปภาษี
- สรุปการแทนที่ราคา
- สรุปส่วนลด
