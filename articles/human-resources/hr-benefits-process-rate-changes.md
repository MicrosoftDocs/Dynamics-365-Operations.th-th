---
title: การเปลี่ยนแปลงอัตราของกระบวนการ
description: การเปลี่ยนแปลงอัตราของกระบวนการใน Microsoft Dynamics 365 Human Resources เมื่อแผนสวัสดิการใหม่หรือที่มีอยู่มีการเปลี่ยนแปลงการตั้งค่ากฎการมีสิทธิ์
author: andreabichsel
manager: tfehr
ms.date: 04/06/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: BenefitWorkspace, HcmBenefitSummaryPart, BenefitRate, BenefitEligibilityProcessResultViewer
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: f326957d5f33607e434f99563cfeb528c05f258d
ms.sourcegitcommit: ea2d652867b9b83ce6e5e8d6a97d2f9460a84c52
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 02/03/2021
ms.locfileid: "5114444"
---
# <a name="process-rate-changes"></a>การเปลี่ยนแปลงอัตราของกระบวนการ

การเปลี่ยนแปลงอัตราของกระบวนการใน Microsoft Dynamics 365 Human Resources เมื่อแผนสวัสดิการใหม่หรือที่มีอยู่มีการเปลี่ยนแปลงการตั้งค่ากฎการมีสิทธิ์ ถ้ากฎการมีสิทธิ์ใหม่ถูกสร้างขึ้นและกำหนดให้กับแผน จะมีการแจ้งให้ระบบดำเนินการให้สิทธิ์ผู้ปฏิบัติงานใหม่อีกครั้ง เพื่อตรวจสอบว่าผู้ปฏิบัติงานอาจมีสิทธิ์สำหรับแผนตามตัวเลือกการมีสิทธิ์ใหม่นี้หรือไม่ 

1. ในพื้นที่ทำงาน **การจัดการสวัสดิการ** ภายใต้ **กำลังประมวลผล** ให้เลือก **การประมวลผลอัพเดตการเปลี่ยนแปลงอัตรา**

2. ในกล่องโต้ตอบ **ดำเนินกระบวนการอัพเดตอัตราของสวัสดิการ** ให้ระบุค่าสำหรับฟิลด์ต่อไปนี้:

   | ฟิลด์ | คำอธิบาย |
   | --- | --- |
   | **รอบระยะเวลาการลงทะเบียน** | รอบระยะเวลาการลงทะเบียนที่จะประมวลผลการเปลี่ยนแปลงอัตรา |

3. ถ้าคุณต้องการดำเนินการกระบวนการในพื้นหลัง ให้เลือก **ดำเนินการในพื้นหลัง** และงานต่อไปนี้:

   1. ป้อนข้อมูลสำหรับกระบวนการ

   2. หากต้องการตั้งค่าให้มีการรันงานนั้นซ้ำ เลือก **การเกิดซ้ำ** ป้อนข้อมูลการเกิดซ้ำ และเลือก **ตกลง**

   3. เมื่อต้องการตั้งค่าการแจ้งเตือนงาน เลือก **การแจ้งเตือน** เลือกการแจ้งเตือนที่จะรับ และจากนั้นเลือก **ตกลง**

   4. เลือก **ตกลง** กระบวนการจะดำเนินการกับพารามิเตอร์ที่คุณตั้งไว้

4. เลือก **ตกลง**
