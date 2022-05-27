---
title: รายงานการวิเคราะห์การแก้ไขปัญหา
description: หัวข้อนี้อธิบายการวิเคราะห์การแก้ไขปัญหา ถ้าการเปลี่ยนแปลงข้อมูลของลูกค้าไม่ปรากฏในพื้นที่ทำงานใดๆ ของลูกค้า
author: twheeloc
ms.date: 08/19/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 7e81bae4d9cb0bb0b77bb57bac16cc67bbbcf9ea
ms.sourcegitcommit: a58dfb892e43921157014f0784bd411f5c40e454
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 05/04/2022
ms.locfileid: "8694073"
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
