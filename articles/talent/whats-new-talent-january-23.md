---
title: มีอะไรใหม่หรือการเปลี่ยนแปลงอะไรใน Dynamics 365 for Talent Core HR (23 มกราคม 2019)
description: หัวข้อนี้อธิบายคุณลักษณะที่ใหม่หรือเปลี่ยนแปลงใน Microsoft Dynamics 365 for Talent Core HR
author: Darinkramer
manager: AnnBe
ms.date: 01/23/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: dkrame
ms.search.validFrom: 2019-01-23
ms.dyn365.ops.version: Talent
ms.openlocfilehash: f27698c257301f52e5c77eaa8a04ca13a0315825
ms.sourcegitcommit: 608e68b603afef9eb98d8fb25e90109c2473ef87
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 03/19/2019
ms.locfileid: "859639"
---
# <a name="whats-new-or-changed-in-dynamics-365-for-talent-core-hr-january-23-2019"></a>มีอะไรใหม่หรือการเปลี่ยนแปลงอะไรใน Dynamics 365 for Talent Core HR (23 มกราคม 2019)

[!include [banner](includes/banner.md)]

**สร้าง 8.1.2121**

หัวข้อนี้อธิบายถึงคุณลักษณะที่ใหม่หรือที่มีการเปลี่ยนแปลง อย่างใดอย่างหนึ่งใน Core HR

## <a name="changes"></a>การเปลี่ยนแปลง

### <a name="import-of-employee-fixed-compensation-not-working-when-creating-new-fixed-compensation-records"></a>การนำเข้าของค่าตอบแทนคงที่ของพนักงานที่ไม่ทำงานเมื่อสร้างเรกคอร์ดค่าตอบแทนคงที่ใหม่
ทำการเปลี่ยนแปลงกับเอนทิตี้ค่าตอบแทนคงที่ของพนักงานในการดึงข้อมูลระดับค่าตอบแทนเมื่อมีการนำเข้า ก่อนที่จะมีการนำออกใช้นี้ ข้อความที่แสดงบ่งชี้ว่าจำเป็นต้องมีระดับ

### <a name="remove-the-minimum-balance-field-from-the-time-off-request-dialog-box"></a>ลบฟิลด์ยอดดุลต่ำสุดออกจากกล่องโต้ตอบคำขอเวลาหยุดงาน
ฟิลด์ **ยอดดุลต่ำสุด** ถูกลบออกจากกล่องโต้ตอบ **คำขอเวลาหยุดงาน** การเปลี่ยนแปลงนี้มีผลกระทบต่อพื้นที่ทั้งหมดที่สามารถร้องขอเวลาหยุดงานได้

### <a name="data-upgrade-for-compensation-levels-not-updating-in-all-scenarios"></a>การอัพเกรดข้อมูลสำหรับระดับค่าตอบแทนที่ไม่มีการปรับปรุงในสถานการณ์จำลองทั้งหมด
มีการเปลี่ยนแปลงเพื่อปรับปรุงระดับค่าตอบแทนในแผนค่าตอบแทนคงที่ การเปลี่ยนแปลงนี้จะเติมระดับค่าตอบแทนสำหรับแผนคงที่สำหรับงานที่กำหนดให้กับพนักงาน

### <a name="payroll-information-in-the-manage-changes-page-is-only-available-when-logged-in-as-system-administrator"></a>ข้อมูลค่าจ้างในหน้าจัดการการเปลี่ยนแปลงจะพร้อมใช้งานเมื่อล็อกอินเป็นผู้ดูแลระบบเท่านั้น
การเปลี่ยนแปลงนี้อนุญาตให้พนักงานที่มีการเข้าถึงบทบาทของเจ้าหน้าที่ฝ่ายค่าจ้างไปยังข้อมูลค่าจ้างในหน้า **เปลี่ยนแปลงเส้นเวลา > จัดการการเปลี่ยนแปลง** ให้กับตำแหน่งงาน

### <a name="job-fields-default-to-positions"></a>ค่าเริ่มต้นฟิลด์งานในตำแหน่ง
เมื่อเปลี่ยนตำแหน่งงาน ฟิลด์งานจะเริ่มต้นกับตำแหน่งงาน ข้อความแจ้งเตือนจะปรากฏขึ้นเพื่อให้สามารถเลือกที่จะยอมรับค่าเริ่มต้นหรือเก็บค่าที่มีอยู่สำหรับฟิลด์เหล่านั้น

### <a name="probation-period-and-calendar-are-not-displayed-for-future-hired-employees"></a>ปฏิทินและช่วงทดลองงานจะไม่แสดงขึ้นสำหรับพนักงานที่จ้างไว้สำหรับอนาคต
ด้วยการเปลี่ยนแปลงนี้ ฟิลด์ **ช่วงทดลองงาน** และ **ปฏิทิน** ถูกเพิ่มไปยังหน้า **จัดการการเปลี่ยนแปลง** เพื่ออนุญาตให้ป้อนข้อมูลสำหรับพนักงานในอดีตและในอนาคต

### <a name="platform-update-23"></a>แพลตฟอร์ม update 23
การแก้ไขบักรองถูกรวมเป็นส่วนหนึ่งของการปรับปรุงแพลตฟอร์ม 23 ดูข้อมูลเพิ่มเติม ดูที่ [มีอะไรใหม่หรือที่เปลี่ยนแปลงในการปรับปรุงแพลตฟอร์ม Dynamics 365 for Finance and Operations 23 (มกราคม 2019)](https://docs.microsoft.com/en-us/dynamics365/unified-operations/fin-and-ops/get-started/whats-new-platform-update-23) 
