---
title: ไม่มีการอัพเดตรายงานการวิเคราะห์
description: หัวข้อนี้อธิบายสิ่งที่ต้องทำ ถ้าการเปลี่ยนแปลงข้อมูลของลูกค้าไม่ปรากฏในพื้นที่ทำงานใดๆ ของลูกค้า
author: andreabichsel
manager: AnnBe
ms.date: 11/02/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2018-11-02
ms.dyn365.ops.version: Talent
ms.openlocfilehash: d6a6487b50908093f876237ffef840a3144b3fe6
ms.sourcegitcommit: 608e68b603afef9eb98d8fb25e90109c2473ef87
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 03/19/2019
ms.locfileid: "857464"
---
# <a name="analytic-reports-are-not-updated"></a>ไม่มีการอัพเดตรายงานการวิเคราะห์

[!include [banner](includes/banner.md)]

**ออก**

การเปลี่ยนแปลงข้อมูลของลูกค้าไม่ปรากฏขึ้นบนแท็บ **การวิเคราะห์** ของพื้นที่ทำงานใดๆ ของลูกค้า

**สาเหตุ**

โดยค่าเริ่มต้น รายงาน Microsoft Power BI ถูกรีเฟรชทุกๆ สี่ชั่วโมง ตามกำหนดการของชุดงานการปรับใช้การวัด

**การแก้ปัญหา**

ปัญหานี้อาจจะเป็นแค่เรื่องของช่วงเวลา ทำตามขั้นตอนเหล่านี้เพื่อเริ่มต้นชุดงาน และอัพเดตพื้นที่ทำงานการวิเคราะห์

1. เปิดหน้า **ชุดงาน** ที่ **การจัดการระบบ \> ลิงค์ \> ชุดงาน \> ชุดงาน** อีกทางหนึ่งคือ ใช้ค้นหา และป้อน **ชุดงาน**
1. ค้นหางาน **ปรับใช้การวัด** ในรายการ
1. เลือก **แก้ไข** ที่ด้านบนของหน้า และตั้งค่าวันที่/เวลาเริ่มต้นตามกำหนดการเป็นค่าที่จะรีเฟรชการวิเคราะห์ให้ใกล้กับเวลาปัจจุบันมากขึ้น

![ชุดงาน](media/batch-jobs.png)
