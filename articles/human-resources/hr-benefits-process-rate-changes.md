---
title: ดำเนินการกับการเปลี่ยนแปลงอัตรา
description: หัวข้อนี้อธิบายวิธีการประมวลผลการเปลี่ยนแปลงอัตราสวัสดิการใน Microsoft Dynamics 365 Human Resources
author: twheeloc
ms.date: 08/23/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: BenefitWorkspace, HcmBenefitSummaryPart, BenefitRate, BenefitEligibilityProcessResultViewer
audience: Application User
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: c1eea61df6dd5fbe0b52a21944deba69928b5125
ms.sourcegitcommit: a58dfb892e43921157014f0784bd411f5c40e454
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 05/04/2022
ms.locfileid: "8696139"
---
# <a name="process-rate-changes"></a>ดำเนินการกับการเปลี่ยนแปลงอัตรา


[!INCLUDE [PEAP](../includes/peap-2.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

หัวข้อนี้อธิบายวิธีการประมวลผลการเปลี่ยนแปลงอัตราสวัสดิการใน Microsoft Dynamics 365 Human Resources เมื่อแผนสวัสดิการใหม่หรือที่มีอยู่มีการเปลี่ยนแปลงการตั้งค่ากฎการมีสิทธิ์ ถ้ากฎการมีสิทธิ์ใหม่ถูกสร้างขึ้นและกำหนดให้กับแผน จะมีการแจ้งให้ระบบดำเนินการให้สิทธิ์ผู้ปฏิบัติงานใหม่อีกครั้ง เพื่อตรวจสอบว่าผู้ปฏิบัติงานอาจมีสิทธิ์สำหรับแผนตามตัวเลือกการมีสิทธิ์ใหม่นี้หรือไม่ 

1. ในพื้นที่ทำงาน **การจัดการสวัสดิการ** ภายใต้ **กำลังประมวลผล** ให้เลือก **การประมวลผลอัปเดตการเปลี่ยนแปลงอัตรา**

2. ในกล่องโต้ตอบ **ดำเนินกระบวนการอัปเดตอัตราของสวัสดิการ** ให้ระบุค่าสำหรับฟิลด์ต่อไปนี้:

   | ฟิลด์ | คำอธิบาย |
   | --- | --- |
   | **รอบระยะเวลาการลงทะเบียน** | รอบระยะเวลาการลงทะเบียนที่จะประมวลผลการเปลี่ยนแปลงอัตรา |

3. ถ้าคุณต้องการดำเนินการกระบวนการในพื้นหลัง ให้เลือก **ดำเนินการในพื้นหลัง** และงานต่อไปนี้:

   1. ป้อนข้อมูลสำหรับกระบวนการ

   2. หากต้องการตั้งค่าให้มีการเรียกใช้งานนั้นซ้ำ เลือก **การเกิดซ้ำ** ป้อนข้อมูลการเกิดซ้ำ และเลือก **ตกลง**

   3. เมื่อต้องการตั้งค่าการแจ้งเตือนงาน เลือก **การแจ้งเตือน** เลือกการแจ้งเตือนที่จะรับ และจากนั้นเลือก **ตกลง**

   4. เลือก **ตกลง** กระบวนการจะดำเนินการกับพารามิเตอร์ที่คุณตั้งไว้

4. เลือก **ตกลง**


[!INCLUDE[footer-include](../includes/footer-banner.md)]
