---
title: ดูและจัดการการเปลี่ยนแปลงที่อยู่
description: หัวข้อนี้จะอธิบายถึงวิธีการที่คุณสามารถดูและจัดการการเปลี่ยนแปลงที่อยู่ใน Dynamics 365 Human Resources
author: andreabichsel
manager: tfehr
ms.date: 08/07/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-human-resources
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 269074
ms.assetid: 426c6127-42ee-4163-8dd0-b2867f95581d
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-08-07
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 8746f449f2b30b2e2119446c1912842c420acbfc
ms.sourcegitcommit: 2190be6c205d7d9e43bdb99b9190cc0112f9f093
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 02/10/2021
ms.locfileid: "5152064"
---
# <a name="view-and-manage-address-changes"></a>ดูและจัดการการเปลี่ยนแปลงที่อยู่

หัวข้อนี้จะอธิบายวิธีการที่คุณสามารถดูและจัดการการเปลี่ยนแปลงที่อยู่ในหน้า **แก้ไขรายละเอียดส่วนบุคคล** ของระบบบริการตนเองของพนักงาน หรือหน้ารายละเอียดของ **ผู้ปฏิบัติงาน** ใน Dynamics 365 Human Resources

องค์กรหลายแห่งต้องการให้พนักงานจัดการรายละเอียดส่วนตัวของตนเองผ่านการใช้ระบบบริการตนเอง คุณสามารถอนุญาตให้ผู้ใช้อัปเดตที่อยู่ของตนในพื้นที่ทำงาน **ระบบบริการตนเองของพนักงาน** คุณสามารถตรวจสอบการเปลี่ยนแปลงเหล่านี้ได้ในพื้นที่ทำงาน **การจัดการบุคลากร** เมื่อต้องการใช้คุณลักษณะนี้ คุณต้องระบุจำนวนวันที่คุณต้องการดูการเปลี่ยนแปลงในหน้า **พารามิเตอร์ทรัพยากรบุคคล**

## <a name="configure-address-change-parameters"></a>ตั้งค่าคอนฟิกพารามิเตอร์การเปลี่ยนแปลงที่อยู่

เมื่อต้องการตั้งค่าคอนฟิกจำนวนวันที่คุณต้องการให้การเปลี่ยนแปลงที่อยู่แสดงในพื้นที่ทำงาน **การจัดการบุคลากร** ให้ทำตามขั้นตอนต่อไปนี้

1. ในบานหน้าต่างนำทาง ให้เลือก **การจัดการบุคลากร**

2. เลือก **ลิงก์**

3. เลือก **พารามิเตอร์ทรัพยากรบุคคล**

4. ในฟิลด์ **จำนวนวัน** ที่อยู่ภายใต้ **การเปลี่ยนแปลงที่อยู่** ให้ป้อนจำนวนวันที่คุณต้องการให้การเปลี่ยนแปลงที่อยู่ปรากฏในพื้นที่ทำงาน **การจัดการบุคลากร**

5. ปิดหน้า

## <a name="create-or-change-an-employee-address"></a>การสร้างหรือเปลี่ยนที่อยู่ของพนักงาน

พนักงานสามารถอัพเดตที่อยู่ของตนในพื้นที่ทำงาน **ระบบบริการตนเองของพนักงาน** ทำตามขั้นตอนเหล่านี้เพื่อสร้างหรือเปลี่ยนที่อยู่

1. เลือกไทล์ **ระบบบริการตนเองของพนักงาน** บนโฮมเพจของคุณ

2. เลือก **แก้ไขรายละเอียดส่วนตัว**

3. หากต้องการเพิ่มที่อยู่ ให้เลือก **เพิ่ม** ถ้าต้องการอัพเดตที่อยู่ที่มีอยู่ ให้เลือกที่อยู่จากรายการ และจากนั้นเลือก **แก้ไข**

4. ป้อน **ชื่อหรือคำอธิบาย**

5. เลือกกล่องแบบหล่นลงของ **วัตถุประสงค์** แล้วเลือกชนิดของที่อยู่

6. ป้อน **ประเทศ/ภูมิภาค**

7. ป้อน **รหัสไปรษณีย์**

8. ป้อน **ถนน**

9. ป้อน **เมือง**, **รัฐ** และ **เขต** โดยทั่วไปแล้วจะมีการตั้งค่าฟิลด์เหล่านี้โดยอัตโนมัติตามฟิลด์ **รหัสไปรษณีย์**

10. อีกทางหนึ่งคือเลือกฟิลด์ **หลัก** เพื่อระบุที่อยู่หลัก คุณสามารถทำเครื่องหมายที่อยู่ได้เพียงรายการเดียวเป็นที่อยู่หลัก ถ้ามีการทำเครื่องหมายที่อยู่อื่นเป็นที่อยู่หลักอยู่แล้ว คุณต้องยืนยันว่าคุณต้องการใช้ที่อยู่นี้เป็นที่อยู่หลัก

11. อีกทางหนึ่งคือเลือกฟิลด์ **ส่วนตัว** เพื่อระบุที่อยู่เป็นแบบส่วนตัว เฉพาะผู้ใช้ที่มีสิทธิอย่างชัดแจ้งในการดูข้อมูลที่อยู่ส่วนตัวเท่านั้นที่สามารถดูที่อยู่นี้ได้

12. เลือก **ตกลง**

## <a name="create-or-change-a-worker-address"></a>สร้างหรือเปลี่ยนที่อยู่ของผู้ปฏิบัติงาน

คุณสามารถอัปเดตที่อยู่ในพื้นที่ทำงาน **การจัดการบุคลากร** ได้ ทำตามขั้นตอนเหล่านี้เพื่อสร้างหรือเปลี่ยนที่อยู่

1. ในพื้นที่ทำงาน **การจัดการบุคลากร** ให้เลือก **ลิงก์** แล้วเลือก **ผู้ปฏิบัติงาน**

3. เลือกผู้ปฏิบัติงาน แล้วเลือก **ที่อยู่**

3. หากต้องการเพิ่มที่อยู่ ให้เลือก **เพิ่ม** ถ้าต้องการอัพเดตที่อยู่ที่มีอยู่ ให้เลือกที่อยู่จากรายการ และจากนั้นเลือก **แก้ไข**

4. ป้อน **ชื่อหรือคำอธิบาย**

5. เลือกกล่องแบบหล่นลงของ **วัตถุประสงค์** แล้วเลือกชนิดของที่อยู่

6. ป้อน **ประเทศ/ภูมิภาค**

7. ป้อน **รหัสไปรษณีย์**

8. ป้อน **ถนน**

9. ป้อน **เมือง**, **รัฐ** และ **เขต** โดยทั่วไปแล้วจะมีการตั้งค่าฟิลด์เหล่านี้โดยอัตโนมัติตามฟิลด์ **รหัสไปรษณีย์**

10. อีกทางหนึ่งคือเลือกฟิลด์ **หลัก** เพื่อระบุที่อยู่หลัก คุณสามารถทำเครื่องหมายที่อยู่ได้เพียงรายการเดียวเป็นที่อยู่หลัก ถ้ามีการทำเครื่องหมายที่อยู่อื่นเป็นที่อยู่หลักอยู่แล้ว คุณต้องยืนยันว่าคุณต้องการใช้ที่อยู่นี้เป็นที่อยู่หลัก

11. อีกทางหนึ่งคือเลือกฟิลด์ **ส่วนตัว** เพื่อระบุที่อยู่เป็นแบบส่วนตัว เฉพาะผู้ใช้ที่มีสิทธิอย่างชัดแจ้งในการดูข้อมูลที่อยู่ส่วนตัวเท่านั้นที่สามารถดูที่อยู่นี้ได้

12. เลือก **ตกลง**
 
## <a name="create-a-future-change-for-an-address"></a>สร้างการเปลี่ยนแปลงในอนาคตสำหรับที่อยู่

ในบางกรณี คุณอาจต้องการอัพเดตที่อยู่ที่จะเปลี่ยนในอนาคต ตัวอย่างเช่น การตั้งค่านี้จะเป็นประโยชน์ถ้าพนักงานย้ายในวันที่ 15 ของเดือนถัดไป

1. เปิดหน้า **จัดการที่อยู่** โดยการเลือก **ตัวเลือกเพิ่มเติม > ขั้นสูง** จากตารางที่อยู่

2. เลือก **สร้าง** เพื่อสร้างที่อยู่ใหม่

3. ป้อนรายละเอียดของที่อยู่

4. เลือกแท็บด่วน **ทั่วไป**

5. ในฟิลด์ **วันที่มีผลบังคับใช้** ให้เลือกวันที่ที่อยู่ใหม่จะมีผลบังคับใช้

6. ในฟิลด์ **วันหมดอายุ** เลือกเวลาที่ที่อยู่จะไม่มีผลบังคับใช้อีกต่อไป

7. ปิดหน้า

## <a name="view-and-monitor-address-changes"></a>ดูและตรวจสอบการเปลี่ยนแปลงที่อยู่

บุคลากรฝ่ายบุคคลสามารถดูและตรวจสอบการเปลี่ยนแปลงที่อยู่จากพื้นที่ทำงาน **การจัดการบุคลากร** เมื่อต้องการดูการเปลี่ยนแปลงที่อยู่ ให้เปิดไทล์ **การจัดการบุคลากร** จาก **หน้าแรก** ที่อยู่ที่เปลี่ยนแปลงแสดงอยู่บนไทล์ในมุมบนขวา จำนวนของ **การเปลี่ยนแปลงที่อยู่** ด้านบนแสดงการเปลี่ยนแปลงที่อยู่ที่เกิดขึ้นในจำนวนวันที่ระบุในหน้า **พารามิเตอร์ทรัพยากรบุคคล** 

เมื่อคุณเลือกไทล์ **การเปลี่ยนแปลงที่อยู่** หน้าใหม่จะแสดงรายละเอียดของการเปลี่ยนแปลงที่อยู่ใดๆ คุณสามารถเลือก **รวมการเปลี่ยนแปลงที่อยู่ในอนาคต** ในมุมด้านขวาบนเพื่อแสดงการเปลี่ยนแปลงที่อยู่ด้วยวันที่ในอนาคต

> [!NOTE]
> ถ้าคุณต้องการรับข้อความแจ้งเตือนหรืออีเมลเกี่ยวกับการเปลี่ยนแปลงที่อยู่เหล่านี้ คุณสามารถสร้างกฎการแจ้งเตือนใหม่บนแท็บ **ตัวเลือก** ในบานหน้าต่างการดำเนินการ สำหรับข้อมูลเพิ่มเติมเกี่ยวกับกฎการแจ้งเตือน ให้ดูที่ [สร้างกฎการแจ้งเตือน](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/get-started/create-alerts)<br><br>

> ถ้าคุณต้องการตั้งค่าคอนฟิกลำดับงานสำหรับการเปลี่ยนแปลงที่อยู่ คุณสามารถเลือกตัวเลือก **ส่งจากภายนอก** ในกฎการแจ้งเตือนของคุณ แล้วใช้ Power Automate เพื่อทริกเกอร์เหตุการณ์ทางธุรกิจและตั้งค่าคอนฟิกลำดับงาน สำหรับข้อมูลเพิ่มเติม ให้ดู [การแจ้งเตือนเป็นเหตุการณ์ทางธุรกิจ](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/get-started/create-alerts#alerts-as-business-events)
