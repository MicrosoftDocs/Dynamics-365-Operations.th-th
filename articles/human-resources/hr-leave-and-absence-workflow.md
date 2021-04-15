---
title: สร้างลำดับงานคำขอลางาน
description: สร้างลำดับงานคำขอลางานและขาดงานเพื่อจัดการคำขอในการลาอย่างสม่ำเสมอใน Dynamics 365 Human Resources
author: andreabichsel
ms.date: 05/08/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: LeavePlanFormPart, LeaveAbsenceWorkspace
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 218e5a6fc95e92bb631ee568a79b7dfe05f425e6
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 03/31/2021
ms.locfileid: "5794552"
---
# <a name="create-a-leave-request-workflow"></a>สร้างลำดับงานคำขอลางาน

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

คุณสามารถสร้างลำดับงานใน Dynamics 365 Human Resources เพื่อจัดการคำขอลางานและขาดงานอย่างสม่ำเสมอ ลำดับงาน **การลางานและการขาดงาน** ช่วยให้คุณสามารถ:

- กำหนดงาน
- กำหนดว่าใครต้องทำงานให้เสร็จสมบูรณ์
- ระบุว่าใครสามารถอนุมัติหรือปฏิเสธคำขอได้

## <a name="create-a-leave-and-absence-request-workflow"></a>สร้างลำดับงานคำขอลางานและขาดงาน

1. ในหน้า **การขาดงานและการลางาน** โปรดเลือกแท็บ **ลิงค์**

2. ภายใต้ **ตั้งค่า** โปรดเลือก **ลำดับงานของฝ่ายทรัพยากรบุคคล**

3. โปรดเลือก **สร้าง** แล้วเลือก **คำขอลางานและขาดงาน** 

4. เมื่อกล่องข้อความ **เปิดไฟล์นี้หรือไม่** ปรากฏขึ้น โปรดเลือก **เปิด** และล็อกอินด้วยข้อมูลประจำตัวของบริษัทของคุณ

5. ใช้โปรแกรมแก้ไขลำดับงานเพื่อสร้างลำดับงานสำหรับคำขอลางานของคุณ สำหรับข้อมูลเพิ่มเติมเกี่ยวกับการทำงานกับลำดับงาน โปรดดูที่ [ภาพรวมของการสร้างลำดับงาน](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/organization-administration/create-workflow?toc=/dynamics365/commerce/toc.json.)

## <a name="leave-and-absence-request-workflow-data-elements"></a>องค์ประกอบข้อมูลลำดับงานคำขอลางานและขาดงาน

คุณสามารถใช้องค์ประกอบข้อมูลต่อไปนี้ในการสร้างการอนุมัติแบบมีเงื่อนไขหรือการอนุมัติโดยอัตโนมัติในลำดับงานสำหรับคำขอลางานและขาดงานได้:

- **จำนวนเงิน**
- **ข้อคิดเห็น**
- **บริษัท**
- **สร้างโดย**
- **วันที่และเวลาที่สร้าง**
- **วันที่สิ้นสุด**
- **ชนิดของการลางาน**
- **แก้ไขโดย**
- **วันที่และเวลาที่แก้ไข**
- **รหัสเหตุผล**
- **รหัสคำขอ**
- **วันที่เริ่มต้น**
- **สถานะ** 
- **วันที่ส่ง**
- **ส่งโดย**
- **ส่งโดยฝ่ายทรัพยากรบุคคล**
- **ส่งโดยผู้จัดการ**
- **ส่งในนามของ**
- **ผู้ปฏิบัติงาน**
- **ชนิดผู้ปฏิบัติงาน**

ตัวอย่างเหล่านี้แสดงวิธีการที่คุณสามารถสร้างเงื่อนไขลำดับงานชนิดต่างๆ โดยใช้องค์ประกอบข้อมูลเหล่านี้:

- ใช้ **รหัสเหตุผล** ในรายงานแบบมีเงื่อนไขเพื่อกำหนดเส้นทางคำขอการลาป่วยที่มีรหัสเหตุผล **การผ่าตัด** ให้กับ HR เพื่อการอนุมัติ ในขณะที่กำหนดเส้นทางรหัสเหตุผลอื่นๆ ให้กับผู้จัดการ สำหรับข้อมูลเพิ่มเติมเกี่ยวกับรายงานแบบมีเงื่อนไข ให้ดู [ตั้งค่าคอนฟิกการตัดสินใจแบบมีเงื่อนไขในลำดับงาน](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/organization-administration/configure-conditional-decision-workflow) 

- ใช้ **ส่งโดยทรัพยากรบุคคล** และ **ส่งโดยผู้จัดการ** ในการดำเนินการอัตโนมัติ เพื่ออนุมัติคำขอลางานโดยอัตโนมัติซึ่งบทบาทเหล่านี้ส่งในนามของพนักงาน สำหรับข้อมูลเพิ่มเติมเกี่ยวกับการดำเนินการอัตโนมัติ ให้ดู [ตั้งค่าคอนฟิกกระบวนการอนุมัติในลำดับงาน](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/organization-administration/configure-approval-process-workflow)

- ใช้ **ชนิดการลางาน** ในรายงานแบบมีเงื่อนไข หรือการดำเนินการอัตโนมัติ เพื่อควบคุมวิธีลำดับงานกำหนดเส้นทางคำขอที่มีชนิดการลางานเฉพาะ

## <a name="see-also"></a>ดูเพิ่มเติมที่

- [ภาพรวมการลางานและการขาดงาน](hr-leave-and-absence-overview.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]