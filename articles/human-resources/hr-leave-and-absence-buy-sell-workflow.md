---
title: สร้างลำดับงานคำขอซื้อและขายวันลา
description: สร้างลำดับงานคำขอซื้อและขายวันลาเพื่อจัดการคำขอซื้อและขายวันลาอย่างสอดคล้องกันใน Dynamics 365 Human Resources
author: andreabichsel
manager: AnnBe
ms.date: 08/20/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: LeavePlanFormPart, LeaveAbsenceWorkspace
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-08-20
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: d490e0c36ea0e854c5d7afc5b3bf75f6b65e542c
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 10/13/2020
ms.locfileid: "4420819"
---
# <a name="create-a-buy-and-sell-leave-request-workflow"></a>สร้างลำดับงานคำขอซื้อและขายวันลา

คุณสามารถสร้างลำดับงานใน Dynamics 365 Human Resources เพื่อจัดการคำขอซื้อและขายวันลาอย่างสอดคล้องกัน ลำดับงาน **ซื้อและขายวันลา** ให้คุณสามารถ:

- กำหนดงาน
- กำหนดว่าใครต้องทำงานให้เสร็จสมบูรณ์
- ระบุว่าใครสามารถอนุมัติหรือปฏิเสธคำขอได้

## <a name="create-a-buy-and-sell-leave-request-workflow"></a>สร้างลำดับงานคำขอซื้อและขายวันลา

1. ในหน้า **การขาดงานและการลางาน** โปรดเลือกแท็บ **ลิงค์**

2. ภายใต้ **ตั้งค่า** โปรดเลือก **ลำดับงานของฝ่ายทรัพยากรบุคคล**

3. โปรดเลือก **สร้าง** แล้วเลือก **คำขอซื้อและขายวันลา** 

4. เมื่อกล่องข้อความ **เปิดไฟล์นี้หรือไม่** ปรากฏขึ้น โปรดเลือก **เปิด** และล็อกอินด้วยข้อมูลประจำตัวของบริษัทของคุณ

5. ใช้โปรแกรมแก้ไขลำดับงานเพื่อสร้างลำดับงานสำหรับคำขอลางานของคุณ สำหรับข้อมูลเพิ่มเติมเกี่ยวกับการทำงานกับลำดับงาน โปรดดูที่ [ภาพรวมของการสร้างลำดับงาน](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/organization-administration/create-workflow?toc=/dynamics365/commerce/toc.json.)

## <a name="leave-and-absence-request-workflow-data-elements"></a>องค์ประกอบข้อมูลลำดับงานคำขอลางานและขาดงาน

คุณสามารถใช้องค์ประกอบข้อมูลต่อไปนี้ในการสร้างการอนุมัติแบบมีเงื่อนไขหรือการอนุมัติโดยอัตโนมัติในลำดับงานสำหรับคำขอซื้อและขายวันลา:

- **จำนวนเงิน**
- **นโยบายการซื้อและขายวันลางาน**
- **บริษัท**
- **สร้างโดย**
- **วันที่และเวลาที่สร้าง**
- **วันที่สิ้นสุด**
- **ชนิดของการลางาน**
- **ปรับเปลี่ยนโดย**
- **วันที่และเวลาที่แก้ไข**
- **รหัสคำขอ**
- **วันที่เริ่มต้น**
- **สถานะ** 
- **วันที่ส่ง**
- **ส่งโดย**
- **ส่งโดยฝ่ายทรัพยากรบุคคล**
- **ส่งโดยผู้จัดการ**
- **ส่งในนามของ**
- **ผู้ปฏิบัติงาน**

## <a name="workflow-examples"></a>ตัวอย่างลำดับงาน

ตัวอย่างเหล่านี้แสดงวิธีการที่คุณสามารถสร้างเงื่อนไขลำดับงานชนิดต่างๆ โดยใช้องค์ประกอบข้อมูลเหล่านี้:

- ใช้ **ส่งโดยฝ่ายทรัพยากรบุคคล** และ **ส่งโดยผู้จัดการ** ในการดำเนินการอัตโนมัติ เพื่ออนุมัติคำขอซื้อและขายวันลาโดยอัตโนมัติซึ่งบทบาทเหล่านี้ส่งในนามของพนักงาน สำหรับข้อมูลเพิ่มเติมเกี่ยวกับการดำเนินการอัตโนมัติ ให้ดู [ตั้งค่าคอนฟิกกระบวนการอนุมัติในลำดับงาน](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/organization-administration/configure-approval-process-workflow)

- ใช้ **ชนิดการลางาน** ในรายงานแบบมีเงื่อนไข หรือการดำเนินการอัตโนมัติ เพื่อควบคุมวิธีลำดับงานกำหนดเส้นทางคำขอที่มีชนิดการลางานเฉพาะ

## <a name="see-also"></a>ดูเพิ่มเติมที่

[ภาพรวมการลางานและการขาดงาน](hr-leave-and-absence-overview.md)<br>
[จัดการนโยบายซื้อและขายวันลางาน](hr-leave-and-absence-manage-buy-and-sell-leave-policies.md)



[!INCLUDE[footer-include](../includes/footer-banner.md)]