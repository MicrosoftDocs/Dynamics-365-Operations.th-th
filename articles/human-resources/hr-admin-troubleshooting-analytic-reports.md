---
title: รายงานการวิเคราะห์การแก้ไขปัญหา
description: บทความนี้อธิบายสิ่งที่ต้องทำ ถ้าการเปลี่ยนแปลงข้อมูลของลูกค้าไม่ปรากฏในพื้นที่ทำงานใด ๆ ของลูกค้า
author: andreabichsel
manager: tfehr
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-human-resources
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: e0befe1a35aa46b2eabb4516559fe07ce27e9f18
ms.sourcegitcommit: 6affb3316be757c99e1fe9c7c7b312b93c483408
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 02/17/2021
ms.locfileid: "5466675"
---
# <a name="troubleshoot-analytic-reports"></a>รายงานการวิเคราะห์การแก้ไขปัญหา

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

**ออกใช้**

การเปลี่ยนแปลงข้อมูลของลูกค้าไม่ปรากฏขึ้นบนแท็บ **การวิเคราะห์** ของพื้นที่ทำงานใดๆ ของลูกค้า

**สาเหตุ**

โดยค่าเริ่มต้น รายงาน Microsoft Power BI ถูกรีเฟรชทุกๆ สี่ชั่วโมง ตามกำหนดการของชุดงานการปรับใช้การวัด

**การแก้ปัญหา**

ปัญหานี้อาจจะเป็นแค่เรื่องของช่วงเวลา ทำตามขั้นตอนเหล่านี้เพื่อเริ่มต้นชุดงาน และอัพเดตพื้นที่ทำงานการวิเคราะห์

1. เปิดหน้า **ชุดงาน** ที่ **การจัดการระบบ \> ลิงค์ \> ชุดงาน \> ชุดงาน** อีกทางหนึ่งคือ ใช้ค้นหา และป้อน **ชุดงาน**
1. ค้นหางาน **ปรับใช้การวัด** ในรายการ
1. เลือก **แก้ไข** ที่ด้านบนของหน้า และตั้งค่าวันที่/เวลาเริ่มต้นตามกำหนดการเป็นค่าที่จะรีเฟรชการวิเคราะห์ให้ใกล้กับเวลาปัจจุบันมากขึ้น

![ชุดงาน](media/batch-jobs.png)


[!INCLUDE[footer-include](../includes/footer-banner.md)]