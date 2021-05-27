---
title: งานของตําแหน่งในบัญชีเงินเดือน
description: หัวข้อนี้แสดงรายละเอียดและตัวอย่างการสอบถามสำหรับเอนทิตีงานของตําแหน่งในบัญชีเงินเดือนใน Dynamics 365 Human Resources
author: jcart
ms.date: 04/07/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: jcart
ms.search.validFrom: 2021-04-07
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 9444a36f5ddf92bd41008c83ec77ab7ff5191fa3
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 05/11/2021
ms.locfileid: "6019357"
---
# <a name="payroll-position-job"></a>งานของตําแหน่งในบัญชีเงินเดือน

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

หัวข้อนี้แสดงรายละเอียดและตัวอย่างการสอบถามสำหรับเอนทิตีความสัมพันธ์งานของตําแหน่งในบัญชีเงินเดือนใน Dynamics 365 Human Resources

## <a name="properties"></a>คุณสมบัติ

| คุณสมบัติ<br>**ชื่อทางกายภาพ**<br>**_ชนิด_** | ใช้ | คำอธิบาย |
| --- | --- | --- |
| **รหัสงาน**<br>mshr_jobid<br>*สตริง* | อ่านอย่างเดียว<br>ต้องระบุ |รหัสของงาน |
| **มีผลใช้ตั้งแต่**<br>mshr_validto<br>*ออฟเซ็ตเวลา วันที่* | อ่านอย่างเดียว <br>ต้องระบุ | วันที่เริ่มต้นการมีผลใช้ของความสัมพันธ์ตำแหน่งและงาน |
| **มีผลใช้ถึง**<br>mshr_validto<br>*ออฟเซ็ตเวลา วันที่* | อ่านอย่างเดียว <br>ต้องระบุ | วันที่สิ้นสุดการมีผลใช้ของความสัมพันธ์ตำแหน่งและงาน  |
| **รหัสตำแหน่ง**<br>mshr_positionid<br>*สตริง* | อ่านอย่างเดียว<br>ต้องระบุ | รหัสของตำแหน่ง |
| **ฟิลด์หลัก**<br>mshr_primaryfield<br>*สตริง* | ต้องระบุ<br>ระบบสร้างขึ้น |  |
| **ค่ารหัสตําแหน่งงาน**<br>_mshr_fk_positionjob_id_value<br>*GUID* | อ่านอย่างเดียว<br>ต้องระบุ<br>คีย์นอก:mshr_PayrollPositionJobEntity:mshr_payrollpositionjobentity |รหัสของงานที่เชื่อมโยงกับตำแหน่ง|
| **ค่ารหัสแผนค่าตอบแทนคงที่**<br>_mshr_fk_fixedcompplan_id_value<br>*GUID* | อ่านอย่างเดียว<br>ต้องระบุ<br>คีย์นอก: mshr_FixedCompPlan_id of mshr_payrollfixedcompensationplanentity  | รหัสของแผนค่าตอบแทนคงที่ที่เชื่อมโยงกับตำแหน่ง |
| **รหัสเอนทิตีงานของตําแหน่งในบัญชีเงินเดือน**<br>mshr_payrollpositionjobentityid<br>*Guid* | ต้องระบุ<br>ระบบถูกสร้างขึ้น | ค่า GUID ที่ระบบสร้างขึ้นเพื่อระบุถึงงานเฉพาะ  |

