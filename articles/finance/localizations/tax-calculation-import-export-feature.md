---
title: นําเข้าและส่งออกการคํานวณภาษี
description: บทความนี้มีข้อมูลเกี่ยวกับฟังก์ชันการนําเข้าและส่งออกของบริการคํานวณภาษี
author: Kai-Cloud
ms.date: 10/17/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application user
ms.reviewer: kfend
ms.custom: ''
ms.search.region: Global
ms.author: kailiang
ms.search.validFrom: 2021-11-15
ms.dyn365.ops.version: 10.0.23
ms.openlocfilehash: 8666d4971e36279ebd2b1396de7cab37680980e6
ms.sourcegitcommit: 40c80a617b903c2b26e44b41147e0021c5cb680d
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 10/18/2022
ms.locfileid: "9690245"
---
# <a name="import-and-export-tax-calculations"></a>นําเข้าและส่งออกการคํานวณภาษี

บทความนี้มีข้อมูลเกี่ยวกับฟังก์ชันการนําเข้าและส่งออกของบริการคํานวณภาษี ฟังก์ชันนี้ช่วยให้มั่นใจถึงประสบการณ์ใช้งานการตั้งค่าคอนฟิกแบบยืดหยุ่นและมีประสิทธิภาพ

## <a name="import-and-export-tax-codes"></a>นําเข้าและส่งออกรหัสภาษี

### <a name="export-templates"></a>ส่งออกเทมเพลต

1. ลงชื่อเข้าใช้ [Regulatory Configuration Service (RCS)](https://marketing.configure.global.dynamics.com/)
2. ในพื้นที่ทำงาน **คุณลักษณะที่ใช้ทั่วโลก** เลือก **คุณลักษณะ** แล้วเลือกไทล์ **การคํานวณภาษี**
3. เลือกคุณลักษณะที่มีอยู่ หรือ [สร้างคุณลักษณะใหม่](global-get-started-with-tax-calculation-service.md#set-up-tax-calculation-in-rcs)
4. ในตาราง **รุ่น** ให้เลือก **แก้ไข**
5. บนหน้าคุณลักษณะ **การคำนวณภาษี** ให้กําหนด [รุ่นการตั้งค่าคอนฟิก](global-get-started-with-tax-calculation-service.md#set-up-tax-calculation-in-rcs)
6. บนแท็บ **รหัสภาษี** ให้เลือก **นำเข้า**
7. เลือก **ส่งออกเทมเพลตรหัสภาษี** เพื่อดาวน์โหลดไฟล์ **TaxCodesTemplate.zip**
8. แยกไฟล์ **TaxCodesTemplate.zip** เทมเพลตรหัสภาษีจะถูกบีบอัดโดยแยกต่างหากตามค่า **จุดเริ่มต้นการคำนวณ**
9. แยกไฟล์ **By Net Amount.zip** เพื่อรับไฟล์ค่าที่คั่นด้วยเครื่องหมายจุลภาค (CSV) ต่อไปนี้:

    - **TaxCode.csv** – ป้อนรหัสภาษี
    - **TaxLimit.csv** – ป้อนวงเงินภาษีของแต่ละรหัสภาษี
    - **TaxRate.csv** – ป้อนอัตราภาษีของแต่ละรหัสภาษี

> [!NOTE]
> ตามค่าเริ่มต้น รายการต่างๆ ในรหัสภาษี **ตัวอย่าง** จะสามารถใช้งานในเทมเพลตได้ หากรหัสภาษี **ตัวอย่าง** ไม่ถูกลบออกจากไฟล์ CSV ระบบจะนําเข้าไปในคุณลักษณะ

### <a name="import-tax-codes"></a>นำเข้ารหัสภาษี

ปฏิบัติตามขั้นตอนต่อไปนี้เพื่อนําเข้ารหัสภาษี **ตัวอย่าง** ในเทมเพลตลงในคุณลักษณะการคํานวณภาษีของคุณ

1. ใน RCS บนหน้าคุณลักษณะ **การคำนวณภาษี** บนแท็บ **รหัสภาษี** ให้เลือก **นําเข้า**
2. เลือก **เรียกดู** ค้นหาและเลือกไฟล์ **TaxCode.csv** จากนั้นในฟิลด์ **ตารางเป้าหมาย** เลือก **รหัสภาษี**
3. เลือก **ตกลง** เพื่อนำเข้ารหัสภาษี
4. ค้นหาและเลือกไฟล์ **TaxRate.csv** จากนั้นในฟิลด์ **ตารางเป้าหมาย** เลือก **อัตราภาษี**
5. เลือก **ตกลง** เพื่อนำเข้าอัตราภาษี
6. ค้นหาและเลือกไฟล์ **TaxLimit.csv** จากนั้นในฟิลด์ **ตารางเป้าหมาย** เลือก **วงเงินภาษี**
7. เลือก **ตกลง** เพื่อนำเข้าวงเงินภาษี

คุณยังสามารถนําเข้าไฟล์ Zip ที่มีไฟล์ CSV ทั้งสามไฟล์ได้โดยตรง ด้วยวิธีนี้ คุณสามารถนําเข้าข้อมูลได้อย่างรวดเร็วและง่ายดาย

1. ใน RCS บนหน้าคุณลักษณะ **การคำนวณภาษี** บนแท็บ **รหัสภาษี** ให้เลือก **นําเข้า**
2. เลือก **เรียกดู** ค้นหาและเลือกไฟล์ **By Net Amount.zip** แล้วเลือก **ตกลง**

### <a name="export-tax-codes"></a>ส่งออกรหัสภาษี

1. ใน RCS บนหน้าคุณลักษณะ **การคำนวณภาษี** บนแท็บ **รหัสภาษี** เลือก **ส่งออก**

    ปุ่ม **ส่งออก** สามารถใช้ได้เมื่อมีรหัสภาษีอย่างน้อยหนึ่งรายการในตาราง **รหัสภาษี**

2. เลือก **ตกลง** เพื่อส่งออกรหัสภาษีทั้งหมดของคุณลักษณะในไฟล์ Zip

> [!NOTE]
> ใช้ไฟล์ที่ส่งออกเป็นเทมเพลตเพื่อนําเข้ารหัสภาษีไปยังคุณลักษณะที่สอดคล้องกัน

## <a name="import-and-export-applicability-rules"></a>นําเข้าและส่งออกกฎการใช้งาน

### <a name="export-applicability-rules"></a>ส่งออกกฎกฎการใช้งาน

1. ลงชื่อเข้าใช้ [RCS](https://marketing.configure.global.dynamics.com/)
2. ในพื้นที่ทำงาน **คุณลักษณะที่ใช้ทั่วโลก** เลือก **คุณลักษณะ** แล้วเลือกไทล์ **การคํานวณภาษี**
3. เลือกคุณลักษณะที่มีอยู่ หรือ [สร้างคุณลักษณะใหม่](global-get-started-with-tax-calculation-service.md#set-up-tax-calculation-in-rcs)
4. ในตาราง **รุ่น** ให้เลือก **แก้ไข**
5. บนหน้าคุณลักษณะ **การคำนวณภาษี** ให้กําหนด [รุ่นการตั้งค่าคอนฟิก](global-get-started-with-tax-calculation-service.md#set-up-tax-calculation-in-rcs)
6. บนแท็บ **การใช้งานกลุ่มภาษี** ให้เลือกแถวในตาราง **ตั้งค่าการใช้งานกลุ่มภาษี**
7. เลือกปุ่ม **เปิดใน Microsoft Office** แล้วเลือก **เมทริกซ์การใช้งานแบบไดนามิกของบริการภาษี**

    [![ส่งออกกฎการใช้งานไปยัง Microsoft Excel ในหน้าคุณลักษณะการคํานวณภาษี](./media/tax-cal-import-export-1.png)](./media/tax-cal-import-export-1.png)

8. เลือก **ดาวน์โหลด** เพื่อส่งออกแถวที่เลือกไปยังเวิร์กชีต Microsoft Excel

### <a name="import-applicability-rules"></a>นำเข้ากฎการใช้งาน

เวิร์กชีต Excel ที่คุณดาวน์โหลดมีโครงสร้างของตาราง **ตั้งค่าการใช้งานกลุ่มภาษี** คุณสามารถเพิ่มกฎใหม่ได้โดยตรงในเวิร์กชีต เมื่อคุณทำเสร็จสิ้นแล้ว ให้ปฏิบัติตามขั้นตอนเหล่านี้เพื่อนําเข้ากฎใหม่กลับไปยังตาราง **ตั้งค่าการใช้งานกลุ่มภาษี**

1. ในเวิร์กชีต Excel ให้เลือกและคัดลอกแถวที่จะนําเข้า
2. ใน RCS ในหน้าคุณลักษณะ **การคํานวณภาษี** บนแท็บ **การใช้งานของกลุ่มภาษี** ให้เลือก **เพิ่ม** เพื่อแทรกเรกคอร์ดเปล่าที่ด้านล่างของตาราง **ตั้งค่าการใช้งานกลุ่มภาษี**
3. เลือก **Ctrl+V** เพื่อวางแถวที่คัดลอกลงในตาราง
4. เลือก **บันทึก**

## <a name="import-feature-demo-data"></a>นําเข้าข้อมูลสาธิตของคุณลักษณะ

ปฏิบัติตามขั้นตอนต่อไปนี้เพื่อนําเข้าข้อมูลสาธิตของคุณลักษณะ

1. ลงชื่อเข้าใช้ [RCS](https://marketing.configure.global.dynamics.com/)
2. ในพื้นที่ทำงาน **คุณลักษณะที่ใช้ทั่วโลก** เลือก **คุณลักษณะ** แล้วเลือกไทล์ **การคํานวณภาษี**
3. เลือก **นําเข้า** และบนหน้า **นำเข้าคุณลักษณะมาจากที่เก็บส่วนกลาง** ให้เลือก **ซิงโครไนส์** 
4. ในตาราง ให้เลือกคุณลักษณะ **tax-calculation-feature-demo-data** แล้วเลือก **นําเข้า**
5. เลือก **ดู** เพื่อตรวจสอบรหัสภาษี กลุ่ม และกฎการใช้งานที่กําหนดไว้ในคุณลักษณะที่นําเข้า
6. ใน Finance สลับไปที่นิติบุคคล **DEMF** และจากนั้นไปที่ **ภาษีx** \> **ตั้งค่า** \> **การตั้งค่าคอนฟิกภาษี** \> **พารามิเตอร์การคํานวณภาษี**
7. บนแท็บ **ทั่วไป** เลือก **เปิดใช้งานบริการคํานวณภาษี**
8. ในฟิลด์ **ชื่อการตั้งค่าคุณลักษณะ** ให้เลือก **tax-calculation-feature-demo-data**
9. เลือก **รอบระยะเวลาการชำระบัญชี** และ **กลุ่มการลงรายการบัญชีแยกประเภท** สำหรับรหัสภาษีสาธิตใหม่ แล้วเลือก **ยืนยัน**
10. เลือก **บันทึก**

> [!NOTE]
> คุณลักษณะสาธิต **tax-calculation-feature-demo-data** ยึดตามรุ่น **40.54.234** และออกแบบมาเพื่อนิติบุคคลสาธิต **DEMF** ตรวจสอบให้แน่ใจว่า Finance และ RCS ได้รับการอัปเกรดเป็นรุ่น 10.0.26 หรือรุ่นที่ใหม่กว่า
