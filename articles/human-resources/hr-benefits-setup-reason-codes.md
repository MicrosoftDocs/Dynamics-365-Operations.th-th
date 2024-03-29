---
title: ตั้งค่ารหัสเหตุผล
description: Dynamics 365 Human Resources ใช้รหัสเหตุผลเพื่ออธิบายว่าเหตุใดสวัสดิการของพนักงานจึงเปลี่ยนไป
author: twheeloc
ms.date: 08/25/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: BenefitWorkspace, HcmBenefitSummaryPart
audience: Application User
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 692bd5acd574492526644849fb555e5856b4463f
ms.sourcegitcommit: 66d129874635d34a8b29c57762ecf1564e4dc233
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 08/23/2022
ms.locfileid: "9323433"
---
# <a name="set-up-reason-codes"></a>ตั้งค่ารหัสเหตุผล

Dynamics 365 Human Resources ใช้รหัสเหตุผลเพื่ออธิบายว่าเหตุใดสวัสดิการของพนักงานจึงเปลี่ยนไป

> [!NOTE]
> ณ เดือนมกราคม 2021 รหัสเหตุผลย้ายไปยังพื้นที่ทำงาน **การจัดการบุคลากร** แทนพื้นที่ทำงาน **การจัดการสวัสดิการ** สำหรับข้อมูลเพิ่มเติม ให้ดู [ย้ายรหัสเหตุผลไปยังการจัดการบุคลากรด้วยตนเอง](hr-benefits-setup-reason-codes.md#manually-migrate-reason-codes-to-personnel-management)

## <a name="create-reason-codes"></a>สร้างรหัสเหตุผล

1. ในพื้นที่ทำงาน **การจัดการบุคลากร** (หรือพื้นที่ทำงาน **การจัดการสวัสดิการ** ถ้ารหัสเหตุผลของคุณยังไม่ได้ย้าย) เลือก **ลิงค์** แล้วเลือก **รหัสเหตุผล**

2. เลือก **ใหม่**

3. ระบุค่าสำหรับฟิลด์ต่อไปนี้

   | ฟิลด์ | คำอธิบาย |
   | --- | --- |
   | **รหัสเหตุผล** | ชื่อเฉพาะเพื่อระบุเหตุผลที่พนักงานจะเปลี่ยนแปลงการลงทะเบียนแผนสวัสดิการ |
   | **คำอธิบาย** | คำอธิบายเกี่ยวกับรหัสเหตุผล |

4. ภายใต้ **สถานการณ์ที่ใช้ได้** ให้ตั้งค่า **การจัดการสวัสดิการ** เป็น **ใช่** (ไม่เกี่ยวข้องถ้ารหัสเหตุผลของคุณยังไม่ได้ย้ายไปยังพื้นที่ทำงาน **การจัดการบุคลากร**)

5. เลือก **บันทึก**

## <a name="manually-migrate-reason-codes-to-personnel-management"></a>ย้ายรหัสเหตุผลไปยังการจัดการบุคลากรด้วยตนเอง

ในเดือนมกราคม 2021 รหัสเหตุผลย้ายไปยังพื้นที่ทำงาน **การจัดการบุคลากร** แทนพื้นที่ทำงาน **การจัดการสวัสดิการ** ข้อมูลรหัสเหตุผลส่วนใหญ่จะย้ายโดยอัตโนมัติในสภาพแวดล้อมของคุณ ข้อมูลรหัสเหตุผลบางอย่างอาจไม่ย้าย ตัวอย่างเช่น ขณะนี้รหัสเหตุผลมีอักขระสูงสุด 15 อักขระ ดังนั้น รหัสเหตุผลที่ยาวกว่า 15 อักขระจะไม่ย้ายโดยอัตโนมัติ

คุณจะเห็นพนักงานทั่วไปในหน้า **ลิงค์** ของพื้นที่ทำงาน **การจัดการสวัสดิการ** เพื่อแจ้งให้ทราบเกี่ยวกับการย้ายข้อมูลและรหัสเหตุผลไม่ได้ย้ายหรือไม่

1. เลือก **รหัสเหตุผล** เพื่อดูรายละเอียดเกี่ยวกับสถานะการย้าย

   [![รหัสเหตุผล](./media/hr-benefits-setup-reason-codes-link.png)](./media/hr-benefits-setup-reason-codes-link.png)

2. เลือกรหัสเหตุผลที่ไม่สามารถย้ายได้

   [![สถานะการย้ายรหัสเหตุผล](./media/hr-benefits-setup-reason-codes-status.png)](./media/hr-benefits-setup-reason-codes-status.png)

3. เลือก **ย้ายรหัสเหตุผล**

   [![ย้ายรหัสเหตุผล](./media/hr-benefits-setup-reason-codes-migrate.png)](./media/hr-benefits-setup-reason-codes-migrate.png)

4. ในบานหน้าต่าง **การย้ายรหัสเหตุผลของสวัสดิการ** คุณมีตัวเลือกสองตัวเลือกในการแมปกับรหัสเหตุผลของการจัดการบุคลากร:

   - เมื่อต้องการใช้รหัสเหตุผลที่มีอยู่ในการจัดการบุคลากร ให้เลือกรหัสเหตุผลใดรหัสหนึ่งจากรายการแบบหล่นลง **ใช้รหัสเหตุผลที่มีอยู่**
     > [!NOTE]
     > คุณสามารถใช้รหัสเหตุผลที่มีอยู่ในการจัดการบุคลากรได้เฉพาะเมื่อรหัสเหตุผลของการจัดการสวัสดิการอื่นยังไม่ได้ย้ายไปยังรหัสนั้นแล้ว
   - เมื่อต้องการสร้างรหัสเหตุผลใหม่ในการจัดการบุคลากร ให้ป้อนรหัสใหม่ใน **เหตุผลใหม่** แล้วป้อนอธิบายใน **คำอธิบายใหม่**

   [![แมปกับรหัสเหตุผลในการจัดการบุคลากร](./media/hr-benefits-setup-reason-codes-mapping.png)](./media/hr-benefits-setup-reason-codes-mapping.png)

หลังจากรหัสเหตุผลย้ายไปยังการจัดการบุคลากร ตัวเลือกในการใช้รหัสเหตุผลในการจัดการสวัสดิการจะถูกตั้งค่าเป็น **ใช่** โดยอัตโนมัติ

[![ใช้รหัสเหตุผลของการจัดการสวัสดิการ](./media/hr-benefits-setup-reason-codes-use.png)](./media/hr-benefits-setup-reason-codes-use.png)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
