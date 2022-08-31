---
title: ดำเนินการกับการเปลี่ยนแปลงเหตุการณ์ของชีวิต
description: บทความนี้อธิบายวิธีการประมวลผลการเปลี่ยนแปลงเหตุการณ์ของชีวิตใน Microsoft Dynamics 365 Human Resources
author: twheeloc
ms.date: 08/23/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: BenefitWorkspace, HcmBenefitSummaryPart, BenefitLifeEventTypes, BenefitEligibilityProcessResultViewer
audience: Application User
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: f3d8fbe0270606688944b4465cb5846b8c8f9900
ms.sourcegitcommit: 66d129874635d34a8b29c57762ecf1564e4dc233
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 08/23/2022
ms.locfileid: "9323519"
---
# <a name="process-life-event-changes"></a>ดำเนินการกับการเปลี่ยนแปลงเหตุการณ์ของชีวิต

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

ประมวลผลการเปลี่ยนแปลงในเหตุการณ์ของชีวิตใน Microsoft Dynamics 365 Human Resources สำหรับสองการเปลี่ยนแปลงเหตุการณ์ของชีวิต

- การเปลี่ยนแปลงวันเกิด
- กฎการใช้สิทธิ์แทนที่การเปลี่ยนการหมดอายุ 

1. ในพื้นที่ทำงาน **การจัดการสวัสดิการ** ภายใต้ **กำลังประมวลผล** ให้เลือก **กำลังประมวลผลการเปลี่ยนแปลงในเหตุการณ์ของชีวิต**

2. ในกล่องโต้ตอบ **ดำเนินการประมวลผลการเปลี่ยนแปลงเหตุการณ์ของชีวิต** ให้ระบุค่าสำหรับฟิลด์ต่อไปนี้:

   | ฟิลด์ | คำอธิบาย |
   | --- | --- |
   | รอบระยะเวลาการลงทะเบียน | รอบระยะเวลาการลงทะเบียนที่จะประมวลผลการเปลี่ยนแปลงในเหตุการณ์ของชีวิต |
   | นิติบุคคล | นิติบุคคลที่จะประมวลผลการเปลี่ยนแปลงในเหตุการณ์ของชีวิต |

3. ถ้าคุณต้องการดำเนินการกระบวนการในพื้นหลัง ให้เลือก **ดำเนินการในพื้นหลัง** และงานต่อไปนี้:

   1. ป้อนข้อมูลสำหรับกระบวนการ

   2. หากต้องการตั้งค่าให้มีการเรียกใช้งานนั้นซ้ำ เลือก **การเกิดซ้ำ** ป้อนข้อมูลการเกิดซ้ำ และเลือก **ตกลง**

   3. เมื่อต้องการตั้งค่าการแจ้งเตือนงาน เลือก **การแจ้งเตือน** เลือกการแจ้งเตือนที่จะรับ และจากนั้นเลือก **ตกลง**

   4. เลือก **ตกลง** กระบวนการจะดำเนินการกับพารามิเตอร์ที่คุณตั้งไว้

4. เลือก **ตกลง**


[!INCLUDE[footer-include](../includes/footer-banner.md)]
