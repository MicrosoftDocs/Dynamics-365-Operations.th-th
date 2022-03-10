---
title: รายงานการวิเคราะห์การแก้ไขปัญหา
description: หัวข้อนี้อธิบายการวิเคราะห์การแก้ไขปัญหา ถ้าการเปลี่ยนแปลงข้อมูลของลูกค้าไม่ปรากฏในพื้นที่ทำงานใดๆ ของลูกค้า
author: twheeloc
ms.date: 08/19/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.search.scope: Human Resources
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 6ea04c06858cc98b0e233b9133d9dfbebfe59fd6
ms.sourcegitcommit: 3a7f1fe72ac08e62dda1045e0fb97f7174b69a25
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 01/31/2022
ms.locfileid: "8067740"
---
# <a name="troubleshoot-analytic-reports"></a>รายงานการวิเคราะห์การแก้ไขปัญหา


[!INCLUDE [PEAP](../includes/peap-2.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

**ออกใช้**

การเปลี่ยนแปลงข้อมูลของลูกค้าไม่ปรากฏขึ้นบนแท็บ **การวิเคราะห์** ของพื้นที่ทำงานใดๆ ของลูกค้า

**สาเหตุ**

โดยค่าเริ่มต้น รายงาน Microsoft Power BI ถูกรีเฟรชทุกๆ สี่ชั่วโมง ตามกำหนดการของชุดงานการปรับใช้การวัด

**การแก้ปัญหา**

ปัญหานี้อาจจะเป็นแค่เรื่องของช่วงเวลา ทำตามขั้นตอนเหล่านี้เพื่อเริ่มต้นชุดงาน และอัปเดตพื้นที่ทำงานการวิเคราะห์

1. เปิดหน้า **ชุดงาน** ที่ **การจัดการระบบ \> ลิงค์ \> ชุดงาน \> ชุดงาน** อีกทางหนึ่งคือ ใช้ค้นหา และป้อน **ชุดงาน**
1. ค้นหางาน **ปรับใช้การวัด** ในรายการ
1. เลือก **แก้ไข** ที่ด้านบนของหน้า และตั้งค่าวันที่/เวลาเริ่มต้นตามกำหนดการเป็นค่าที่จะรีเฟรชการวิเคราะห์ให้ใกล้กับเวลาปัจจุบันมากขึ้น

![ชุดงาน](media/batch-jobs.png)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
