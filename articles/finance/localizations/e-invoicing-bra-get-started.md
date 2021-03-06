---
title: เริ่มต้นใช้งาน add-on ของใบแจ้งหนี้อิเล็กทรอนิกส์ สำหรับ บราซิล
description: หัวข้อนี้จะให้ข้อมูลซึ่งจะช่วยให้คุณเริ่มต้นใช้งาน add-on ของใบแจ้งหนี้อิเล็กทรอนิกส์ สำหรับบราซิล ใน Microsoft Dynamics 365 Finance และ Dynamics 365 Supply Chain Management
author: gionoder
manager: AnnBe
ms.date: 09/04/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.custom: 97423
ms.assetid: ''
ms.search.region: Global
ms.author: janeaug
ms.search.validFrom: 2020-07-08
ms.dyn365.ops.version: AX 10.0.12
ms.openlocfilehash: 0320bd1d9e93cc30ed75f28e387ac2ec8dbfc226
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 01/15/2021
ms.locfileid: "4962846"
---
# <a name="get-started-with-the-electronic-invoicing-add-on-for-brazil"></a>เริ่มต้นใช้งาน add-on ของใบแจ้งหนี้อิเล็กทรอนิกส์ สำหรับ บราซิล 

[!include [banner](../includes/banner.md)]


> [!IMPORTANT]
> Add-on ของใบแจ้งหนี้อิเล็กทรอนิกส์ สำหรับบราซิล ไม่สนับสนุนฟังก์ชันทั้งหมดที่พร้อมใช้งานใน การรวมเอกสารทางการเงินที่สร้างขึ้นใน Microsoft Dynamics 365 Finance และ Dynamics 365 Supply Chain Management

หัวข้อนี้ให้ข้อมูลซึ่งจะช่วยให้คุณเริ่มต้นใช้งาน add-on ของใบแจ้งหนี้อิเล็กทรอนิกส์ สำหรับเม็บราซิล โดยจะแนะนำให้คุณทราบถึงขั้นตอนการตั้งค่าคอนฟิกที่มีประเทศขึ้นอยู่กับ ใน Regulatory Configuration Services (RCS) และ ใน Finance และ Supply Chain Management นอกจากนี้คุณยังสามารถใช้กระบวนการในการส่งเอกสารทางการเงิน NF-E (แบบจำลองเอกสารทางการเงินอิเล็กทรอนิกส์ 55) โดยผ่านทางบริการ และอธิบายวิธีการตรวจทานผลลัพธ์การประมวลผลและสถานะของเอกสารทางการเงิน

## <a name="prerequisites"></a>ข้อกำหนดเบื้องต้น

ก่อนที่คุณจะดำเนินการขั้นตอนในหัวข้อนี้ให้เสร็จสมบูรณ์ คุณต้องดำเนินการขั้นตอนต่างๆ ใน [การเริ่มต้นใช้งาน add-on ของใบแจ้งหนี้อิเล็กทรอนิกส์](e-invoicing-get-started.md) ให้เสร็จสมบูรณ์ก่อน

## <a name="rcs-setup"></a>การตั้งค่า RCS

ในระหว่างการตั้งค่า RCS คุณจะทำงานเหล่านี้ให้เสร็จสมบูรณ์:

1. นำเข้าคุณลักษณะของใบแจ้งหนี้อิเล็กทรอนิกส์สำหรับเอกสารทางการเงิน NF-E
2. ตรวจทานรูปแบบไฟล์ที่จำเป็นในการส่งเอกสารทางการเงิน NF-E สำหรับการตรวจสอบ
3. ตรวจทานรูปแบบไฟล์ที่จำเป็นสำหรับการร้องขอการยกเลิก NF-E ที่ได้รับอนุมัติ
4. ตั้งค่าคอนฟิกเหตุการณ์ที่จำเป็นในการส่งเอกสารทางการเงิน NF-E สำหรับการตรวจสอบ
5. ตั้งค่าคอนฟิกเหตุการณ์ที่จำเป็นสำหรับการร้องขอการยกเลิก NF-E ที่ได้รับอนุมัติ
6. กำหนดคุณลักษณะของใบแจ้งหนี้อิเล็กทรอนิกส์ให้กับสภาพแวดล้อม add-on ของใบแจ้งหนี้อิเล็กทรอนิกส์
7. เผยแพร่คุณลักษณะใบแจ้งหนี้อิเล็กทรอนิกส์

> [!NOTE]
> "คุณลักษณะของใบแจ้งหนี้อิเล็กทรอนิกส์" คือชื่อทั่วไปสำหรับทรัพยากรที่มีการตั้งค่าคอนฟิกและเผยแพร่ เพื่อใช้เซิร์ฟเวอร์ add-on ของใบแจ้งหนี้อิเล็กทรอนิกส์ การตั้งค่าของคุณลักษณะใบแจ้งหนี้อิเล็กทรอนิกส์ ซึ่งรวมถึงการใช้รูปแบบการตั้งค่าคอนฟิกการรายงานอิเล็กทรอนิกส์ (ER) เพื่อสร้างไฟล์การส่งออกและการนำเข้าที่สามารถจัดโครงแบบได้ และการใช้การดำเนินการและการดำเนินการขั้นตอน เพื่อเปิดใช้งานการสร้างกฎที่สามารถจัดโครงแบบได้ เพื่อส่งคำขอ นำเข้าการตอบสนอง และแยกเนื้อหาที่ตอบสนอง

## <a name="import-the-e-invoicing-feature"></a>นำเข้าคุณลักษณะใบแจ้งหนี้อิเล็กทรอนิกส์

1. ลงชื่อเข้าใช้บัญชี RCS ของคุณ
2. ในพื้นที่ทำงาน **คุณลักษณะที่ใช้ทั่วโลก** ในส่วน **คุณลักษณะ** ให้เลือกไทล์ **ใบแจ้งหนี้อิเล็กทรอนิกส์**
3. บนหน้า **คุณลักษณะ e-Invoicing** ให้เลือก **นำเข้า** เพื่อนำเข้าคุณลักษณะใบแจ้งหนี้อิเล็กทรอนิกส์เอกสารทางการเงิน NF-E จากที่เก็บส่วนกลาง

    ![ปุ่มนำเข้า](media/e-Invoicing-services-get-started-BRA-Select-Import-e-Invoicing-feature.png)

4. เลือกคุณลักษณะเอกสารทางการเงิน NF-E แล้วเลือก **นำเข้า**

    ![กำลังนำเข้าคุณลักษณะ NF-E](media/e-Invoicing-services-get-started-BRA-Select-Import-NF-e-feature.png)

### <a name="create-a-new-version-of-the-nf-e-fiscal-document-feature"></a>สร้างคุณลักษณะของเอกสารทางการเงิน NF-E เวอร์ชันใหม่

- บนหน้า **คุณลักษณะ e-Invoicing** บนแท็บ **เวอร์ชัน** ให้เลือก **ใหม่**

![การเพิ่มคุณลักษณะของใบแจ้งหนี้อิเล็กทรอนิกส์เวอร์ชันใหม่](media/e-Invoicing-services-get-started-BRA-Select-New-e-Invoicing-feature-version.png)

### <a name="update-the-configuration-version"></a>อัพเดตเวอร์ชันการตั้งค่าคอนฟิก

1. บนหน้า **คุณลักษณะใบแจ้งหนี้อิเล็กทรอนิกส์** บนแท็บ **การตั้งค่าคอนฟิก** ให้เลือก **เพิ่ม** หรือ **ลบ** เพื่อจัดการเวอร์ชันการตั้งค่าคอนฟิก (การตั้งค่าคอนฟิกรูปแบบไฟล์ ER)

    ![การจัดการการตั้งค่าคอนฟิกคุณลักษณะของใบแจ้งหนี้อิเล็กทรอนิกส์](media/e-Invoicing-services-get-started-BRA-Manage-e-Invoicing-feature-configurations.png)

    - เมื่อคุณสร้างเวอร์ชันใหม่ของคุณลักษณะเอกสารทางการเงิน NF-E เวอร์ชันการตั้งค่าคอนฟิกทั้งหมด (รูปแบบไฟล์ ER) จะถูกสืบทอดมาจากเวอร์ชันล่าสุด
    - ถ้าต้องการส่งเอกสารทางการเงิน NF-E สำหรับการตรวจสอบ ต้องใช้เวอร์ชันการตั้งค่าคอนฟิกต่อไปนี้:

        - รูปแบบการส่งออก NFe
        - การนำเข้าข้อความตอบสนอง NFe
        - การนำเข้าล็อกข้อผิดพลาด NFe

    - เมื่อต้องการส่งการยกเลิก NF-E ต้องใช้เวอร์ชันการตั้งค่าคอนฟิกต่อไปนี้:

        - รูปแบบการส่งออกการยกเลิก NFe

2. ในรายการ ให้เลือกเวอร์ชันการตั้งค่าคอนฟิก แล้วเลือก **แก้ไข** หรือ **ดู** เพื่อเปิดหน้า **ตัวออกแบบรูปแบบ** ซึ่งคุณสามารถแก้ไขหรือดูการตั้งค่าคอนฟิกได้

    ![การเปิดหน้าตัวออกแบบรูปแบบ](media/e-Invoicing-services-get-started-BRA-Configuration-ER-fomat-designer.png)

3. ใช้หน้า **ตัวออกแบบรูปแบบ** เพื่อแก้ไข หรือดูการตั้งค่าคอนฟิกไฟล์รูปแบบ ER สำหรับข้อมูลเพิ่มเติม โปรดดู [สร้างการตั้งค่าคอนฟิกเอกสารอิเล็กทรอนิกส์](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/analytics/electronic-reporting-configuration)

    ![หน้าตัวออกแบบรูปแบบ](media/e-Invoicing-services-get-started-BRA-ER-Format-designer.png)

### <a name="manage-the-e-invoicing-feature-setups"></a>จัดการการตั้งค่าคุณลักษณะของใบแจ้งหนี้อิเล็กทรอนิกส์

- บนหน้า **คุณลักษณะของใบแจ้งหนี้อิเล็กทรอนิกส์** บนแท็บ **การตั้งค่า** ให้เลือก **เพิ่ม** หรือ **ลบ** เพื่อจัดการการตั้งค่าคุณลักษณะของใบแจ้งหนี้อิเล็กทรอนิกส์ (นั่นคือ เหตุการณ์ NF-E)

![การจัดการการตั้งค่าคุณลักษณะของใบแจ้งหนี้อิเล็กทรอนิกส์](media/e-Invoicing-services-get-started-BRA-Manage-e-Invoicing-feature-setup.png)

เมื่อคุณสร้างเวอร์ชันใหม่ของคุณลักษณะเอกสารทางการเงิน NF-E ที่สืบทอดมาจากคุณลักษณะของใบแจ้งหนี้อื่นๆ การตั้งค่าคุณลักษณะทั้งหมด (เหตุการณ์ NF-E) จะถูกสืบทอดมาจากเวอร์ชันล่าสุด

การส่งเอกสารทางการเงิน NF-E สำหรับการตรวจสอบ จำเป็นต้องมีการตั้งค่าคุณลักษณะ **ส่ง**

เมื่อต้องการส่งการยกเลิก NF-E จำเป็นต้องมีการตั้งค่าคุณลักษณะ **การยกเลิก**

#### <a name="configure-the-submit-feature-setup"></a>ตั้งค่าคอนฟิกการตั้งค่าคุณลักษณะส่ง

1. บนหน้า **คุณลักษณะของใบแจ้งหนี้อิเล็กทรอนิกส์** บนแท็บ **การตั้งค่า** ในคอลัมน์ **การตั้งค่าคุณลักษณะ** ให้เลือก **ส่ง**
2. เลือก **แก้ไข**

    ![แก้ไขคุณลักษณะของใบแจ้งหนี้อิเล็กทรอนิกส์](media/e-Invoicing-services-get-started-BRA-Edit-e-Invoicing-feature-setup.png)

3. ในหน้า **การตั้งค่าเวอร์ชันของคุณลักษณะ** ให้เลือกให้เลือกแท็บ **การดำเนินการ** เพื่อจัดการรายการของการดำเนินการ

    ![แท็บการดำเนินการ](media/e-Invoicing-services-get-started-BRA-Select-Actions.png)

4. ตรวจทานการดำเนินการที่จำเป็นในการส่งเอกสารทางการเงิน NF-E สำหรับการตรวจสอบ

    | รหัสการดำเนินการ | ชื่อการดำเนินการ                  | คำอธิบายการดำเนินการ                                                |
    |-----------|------------------------------|-------------------------------------------------------------------|
    | 1         | แปลงเอกสาร           | สร้างไฟล์ XML ของ NF-E สำหรับการส่ง                          |
    | 2         | ลงชื่อในเอกสาร                | ใช้ใบรับรองดิจิทัลกับไฟล์ XML                    |
    | 3         | บริการ Call Brazilian SEFAZ | ส่งไฟล์ XML ที่เซ็นรับรองแล้วไปยังบริการเว็บสำหรับการตรวจสอบ |
    | 4         | ประมวลผลการตอบสนอง             | รับการตอบสนองการบริการเว็บ                                     |
    | 5         | แปลงเอกสาร           | แยกวิเคราะห์เนื้อหาของไฟล์ที่ได้รับเป็นการตอบสนอง     |
    | 6 ชั่วโมง         | แปลงเอกสาร           | สร้างไฟล์ XML เพื่อสอบถามเกี่ยวกับสถานะของการส่ง    |
    | 7         | บริการ Call Brazilian SEFAZ | ส่งไฟล์ XML ที่ร้องขอสถานะการส่ง          |
    | 8         | ประมวลผลการตอบสนอง             | รับการตอบสนองการบริการเว็บ                                     |

#### <a name="set-up-the-url-for-sefaz-web-services"></a>ตั้งค่า URL สำหรับบริการเว็บ SEFAZ 

1. ในหน้า **การตั้งค่าเวอร์ชันของคุณลักษณะ** บนแท็บ **การดำเนินการ** บนแท็บด่วน **การดำเนินการ** ให้เลือก **บริการ Call Brazilian SEFAZ** (ID การดำเนินการ **3**)
2. บนแท็บด่วน **พารามิเตอร์** ในฟิลด์ **พารามิเตอร์ที่อยู่ URL** ให้ป้อน URL ของบริการเว็บ SEFAZ สำหรับการส่ง NF-E
3. บนแท็บด่วน **การดำเนินการ** ให้เลือก **บริการ Call Brazilian SEFAZ** (ID การดำเนินการ **7**)
4. บนแท็บด่วน **พารามิเตอร์** ในฟิลด์ **พารามิเตอร์ที่อยู่ URL** ให้ป้อน URL ของบริการเว็บ SEFAZ สำหรับการส่ง NF-E

#### <a name="configure-the-cancellation-feature-setup"></a>ตั้งค่าคอนฟิกการตั้งค่าคุณลักษณะการยกเลิก

1. บนหน้า **คุณลักษณะของใบแจ้งหนี้อิเล็กทรอนิกส์** บนแท็บ **การตั้งค่า** ในคอลัมน์ **การตั้งค่าคุณลักษณะ** ให้เลือก **การยกเลิก**
2. เลือก **แก้ไข**
3. ในหน้า **การตั้งค่าเวอร์ชันของคุณลักษณะ** ให้เลือกให้เลือกแท็บ **การดำเนินการ** เพื่อจัดการรายการของการดำเนินการ
4. ตรวจทานการดำเนินการที่จำเป็นสำหรับการร้องขอการยกเลิก NF-E ที่ได้รับอนุมัติ

    | รหัสการดำเนินการ | ชื่อการดำเนินการ                  | คำอธิบายการดำเนินการ                                               |
    |-----------|------------------------------|------------------------------------------------------------------|
    | 1         | แปลงเอกสาร           | สร้างไฟล์ XML การยกเลิกของ NF-E สำหรับการส่ง            |
    | 2         | ลงชื่อในเอกสาร                | ใช้ใบรับรองดิจิทัลกับไฟล์ XML                   |
    | 3         | บริการ Call Brazilian SEFAZ | ส่งไฟล์ XML ที่เซ็นรับรองแล้วไปยังบริการเว็บสำหรับการยกเลิก |
    | 4         | ประมวลผลการตอบสนอง             | รับการตอบสนองการบริการเว็บ                                    |

#### <a name="set-up-the-url-for-sefaz-web-services"></a>ตั้งค่า URL สำหรับบริการเว็บ SEFAZ

1. ในหน้า **การตั้งค่าเวอร์ชันของคุณลักษณะ** บนแท็บ **การดำเนินการ** บนแท็บด่วน **การดำเนินการ** ให้เลือก **บริการ Call Brazilian SEFAZ** (ID การดำเนินการ **3**)
2. บนแท็บด่วน **พารามิเตอร์** ในฟิลด์ **พารามิเตอร์ที่อยู่ URL** ให้ป้อน URL ของบริการเว็บ SEFAZ สำหรับการยกเลิก NF-E ที่อนุมัติแล้ว

### <a name="make-an-e-invoicing-environment-available-and-assign-a-draft-version"></a>ทำให้สภาพแวดล้อมของใบแจ้งหนี้อิเล็กทรอนิกส์มีอยู่ และกำหนดเวอร์ชันแบบร่าง

1. บนหน้า **e-Invoicing Features** บนแท็บ **สภาพแวดล้อม** ให้เลือก **เปิดใช้งาน**
2. ในฟิลด์ **สภาพแวดล้อม** ให้เลือกสภาพแวดล้อม
3. ในฟิลด์ **มีผลบังคับใช้ตั้งแต่** ให้เลือกวันที่ที่สภาพแวดล้อมควรจะมีผลบังคับใช้
4. เลือก **เปิดใช้งาน**

![การเปิดใช้งานสภาพแวดล้อมของใบแจ้งหนี้อิเล็กทรอนิกส์](media/e-Invoicing-services-get-started-BRA-Enable-e-Invoicing-environment.png)

### <a name="change-the-status-to-completed"></a>เปลี่ยนสถานะเป็นเสร็จสมบูรณ์

1. บนหน้า **คุณลักษณะของใบแจ้งหนี้อิเล็กทรอนิกส์** บนแท็บ **เวอร์ชัน** ให้เลือกเวอร์ชันของคุณลักษณะของใบแจ้งหนี้อิเล็กทรอนิกส์ที่มีสถานะเป็น **แบบร่าง**
2. เลือก **เปลี่ยนแปลงสถานะ \> เสร็จสมบูรณ์**

### <a name="change-the-status-to-publish"></a>เปลี่ยนสถานะเป็นเผยแพร่

1. บนหน้า **คุณลักษณะของใบแจ้งหนี้อิเล็กทรอนิกส์** บนแท็บ **เวอร์ชัน** ให้เลือกเวอร์ชันของคุณลักษณะของใบแจ้งหนี้อิเล็กทรอนิกส์ที่มีสถานะเป็น **เสร็จสมบูรณ์**
2. เลือก **เปลี่ยนแปลงสถานะ \> เผยแพร่**

![เผยแพร่คุณลักษณะใบแจ้งหนี้อิเล็กทรอนิกส์](media/e-Invoicing-services-get-started-BRA-Publish-e-Invoicing-feature.png)

## <a name="set-up-electronic-invoicing-add-on-integration-in-finance-or-supply-chain-management"></a>ตั้งค่าการรวม add-on ของใบแจ้งหนี้อิเล็กทรอนิกส์ใน Finance หรือ Supply Chain Management

ในระหว่างขั้นตอน คุณจะทำงานเหล่านี้ให้เสร็จสมบูรณ์:

1. เปิดใช้งานคุณลักษณะของ NF-E ของรัฐบาลกลางสำหรับบราซิล
2. นำเข้าแบบจำลองข้อมูล ER เฉพาะ การแม็ปแบบจำลองข้อมูล ER และรูปแบบที่จำเป็นสำหรับเอกสารทางการเงิน NF-e
3. นำเข้าการตั้งค่าคอนฟิก ER และตั้งค่าชนิดของการตอบสนองที่จำเป็นในการอัพเดตสถานะของเอกสารทางการเงิน หลังจากกระบวนการส่งถูกส่งคืน

### <a name="turn-on-the-nf-e-federal-feature-for-brazil"></a>เปิดใช้งานคุณลักษณะของ NF-E สำหรับบราซิล

1. ไปที่ **การจัดการองค์กร \> การตั้งค่า \> พารามิเตอร์เอกสารอิเล็กทรอนิกส์**
2. บนแท็บ **คุณลักษณะ** ให้เลือกกล่องกาเครื่องหมาย **เปิดใช้งาน** ในแถวสำหรับการอ้างอิงคุณลักษณะ **BR00053**

### <a name="import-the-er-data-model-mapping-required-for-nf-e-fiscal-documents"></a>นำเข้าการแม็ปแบบจำลองข้อมูล ER ที่จำเป็นสำหรับเอกสารทางการเงิน NF-E

1. เข้าสู่ระบบ Finance
2. ในพื้นที่ทำงาน **รายงานอิเล็กทรอนิกส์** ในส่วน **ผู้ให้บริการการตั้งค่าคอนฟิก** ให้เลือก **Microsoft** ตรวจสอบให้แน่ใจว่ามีการตั้งค่าผู้ให้บริการการตั้งค่าคอนฟิกนี้เป็น **ใช้งานอยู่** สำหรับข้อมูลเพิ่มเติมเกี่ยวกับวิธีการตั้งค่าผู้ให้บริการเป็น **ใช้งานอยู่** ให้ดู [สร้างผู้ให้บริการการตั้งค่าคอนฟิก และทำเครื่องหมายเป็นใช้งานอยู่](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/analytics/tasks/er-configuration-provider-mark-it-active-2016-11)
3. เลือก **ที่เก็บ**
4. เลือก **ทรัพยากรส่วนกลาง \> เปิด**
5. นำเข้าการตั้งค่าคอนฟิก **การแม็ปเอกสารทางการเงิน**

### <a name="import-er-configurations-and-set-up-the-response-types-for-fiscal-documents"></a>นำเข้าการตั้งค่าคอนฟิก ER และตั้งค่าชนิดของการตอบสนองสำหรับเอกสารทางการเงิน

1. ในพื้นที่ทำงาน **รายงานอิเล็กทรอนิกส์** ในส่วน **ผู้ให้บริการการตั้งค่าคอนฟิก** ให้เลือก **Microsoft**
2. เลือก **ที่เก็บ**
3. เลือก **ทรัพยากรส่วนกลาง \> เปิด**
4. นำเข้า **การนำเข้าล็อกข้อผิดพลาด NF-e (BR)** **รูปแบบการนำเข้าข้อมูลการตอบสนอง NF-e (BR)** และ **การนำเข้าข้อความตอบสนอง NF-e (BR)**
5. ไปที่ **การจัดการองค์กร \> การตั้งค่า \> พารามิเตอร์เอกสารอิเล็กทรอนิกส์**
6. บนแท็บ **เอกสารอิเล็กทรอนิกส์** ให้เลือก **เพิ่ม**
6. ในฟิลด์ **ชื่อตาราง** ให้ป้อน **ส่วนหัวของเอกสารทางการเงิน**
7. ในฟิลด์ **บริบทของเอกสาร** ให้เลือก **รูปแบบบริบทของใบแจ้งหนี้ของลูกค้า – บริบทเอกสารทางการเงิน**
8. เลือก **ชนิดของการตอบสนอง**
9. เลือก **สร้าง** จากนั้น ในฟิลด์ **ชนิดของการตอบสนอง** เลือก **การตอบสนอง**
10. ในฟิลด์ **สถานะการส่ง** ให้เลือก **ค้างอยู่**
11. ในฟิลด์ **การแม็ปแบบจำลอง** ให้เลือก **รูปแบบการนำเข้าข้อความตอบสนอง – การแม็ปแบบจำลองจากข้อความตอบสนอง**
12. เลือก **บันทึก**
13. เลือก **สร้าง** จากนั้น ในฟิลด์ **ชนิดของการตอบสนอง** ป้อน **ResponseData**
14. ในฟิลด์ **สถานะการส่ง** ให้เลือก **ค้างอยู่**
15. ในฟิลด์ **การแม็ปแบบจำลอง** ให้เลือก **รูปแบบการนำเข้าข้อมูลการตอบสนอง NFe – การนำเข้าข้อมูลการตอบสนอง**
16. เลือก **บันทึก**

## <a name="electronic-invoice-processing"></a>การประมวลผลใบแจ้งหนี้อิเล็กทรอนิกส์

ในระหว่างการประมวลผลใน Finance คุณจะทำงานเหล่านี้ให้เสร็จสมบูรณ์:

1. ส่งเอกสารทางการเงินผ่านทาง add-on ของใบแจ้งหนี้อิเล็กทรอนิกส์
2. ดูล็อกการดำเนินการการส่งและตรวจสอบผลลัพธ์ของการประมวลผล
3. ส่งการยกเลิกของเอกสารทางการเงินผ่านทาง add-on ของใบแจ้งหนี้อิเล็กทรอนิกส์

### <a name="submit-nf-e-fiscal-documents-for-sefaz-authorization"></a>ส่งเอกสารทางการเงิน NF-E สำหรับการตรวจสอบ SEFAZ 

หลังจากที่คุณเปิดใช้งานคุณลักษณะ **การรวม add-on ใบแจ้งหนี้อิเล็กทรอนิกส์ที่จัดโครงแบบ** กระบวนการเก่าสำหรับการส่งเอกสารทางการเงิน NF-e สำหรับการตรวจสอบ (**กระบวนการ NF-e ส่งออก/นำเข้า**) จะไม่สามารถใช้ได้อีกต่อไป ซึ่งถูกแทนที่โดยกระบวนการใหม่ที่ชื่อ **ส่งเอกสารอิเล็กทรอนิกส์**

> [!NOTE]
> ก่อนที่คุณจะดำเนินการต่อไป โปรดตรวจสอบให้แน่ใจว่าคุณมีเอกสารทางการเงินของลูกค้ารุ่น 55 อย่างน้อยหนึ่งรายการ ซึ่งออกโดยสถานที่จัดทำงบประมาณของลูกค้า ต้องมีการตั้งค่าทิศทางสำหรับเอกสารทางการเงินเหล่านี้เป็น **ขาออก** และต้องมีการ **สร้าง** สถานะ สำหรับข้อมูลเพิ่มเติม ให้ดู [การออกเอกสารทางการเงินของลูกค้า (บราซิล)](https://docs.microsoft.com/dynamics365/finance/localizations/tasks/br-00038-issuing-customer-fiscal-document)

1. ไปที่ **การจัดการองค์กร \> ประจำงวด \> เอกสารอิเล็กทรอนิกส์ \> ส่งเอกสารอิเล็กทรอนิกส์**
2. สำหรับการส่งเอกสารฉบับแรกของเอกสารใดๆ ให้ตั้งค่าตัวเลือก **ส่งเอกสารใหม่** เป็น **ไม่** เสมอ ถ้าคุณต้องส่งเอกสารผ่านทางบริการอีกครั้ง ให้กำหนดตัวเลือกนี้เป็น **ใช่**
3. บนแท็บด่วน **เรกคอร์ดที่จะรวม** ให้เลือก **ตัวกรอง** เพื่อเปิดกล่องโต้ตอบ **การสอบถาม** ซึ่งคุณสามารถสร้างการสอบถามเพื่อเลือกเอกสารสำหรับการส่งได้
4. บนแท็บ **การกำหนดช่วง** ให้เลือก **เพิ่ม**
5. ในฟิลด์ **ตาราง** ให้เลือก **ส่วนหัวของเอกสารทางการเงิน**
6. ในฟิลด์ **ตารางสืบทอด** ให้เลือก **ส่วนหัวของเอกสารทางการเงิน**
6. ในฟิลด์ **ฟิลด์** ให้เลือก **หมายเลข**
7. ในฟิลด์ **เงื่อนไข** ให้ป้อนหมายเลขของเอกสารทางการเงินที่ควรจะส่ง
8. เลือก **ตกลง** เพื่อปิดกล่องโต้ตอบ **การสอบถาม**
8. เลือก **ตกลง** เพื่อส่งเอกสารที่เลือก

> [!NOTE]
> ในระหว่างความพยายามครั้งแรกของคุณในการส่งเอกสารผ่านทางบริการ คุณจะได้รับพร้อมท์ให้ยืนยันการเชื่อมต่อกับ add-on ของใบแจ้งหนี้อิเล็กทรอนิกส์ เลือก **คลิกที่นี่เพื่อเชื่อมต่อกับ Electronic Document Submission Service**

### <a name="view-all-submission-logs"></a>ดูล็อกการส่งทั้งหมด

หลังจากที่คุณเปิดใช้คุณลักษณะ **การรวม add-on ใบแจ้งหนี้อิเล็กทรอนิกส์ที่จัดโครงแบบ** หน้าใหม่จะพร้อมใช้งาน ซึ่งช่วยให้คุณสามารถติดตามผลในกระบวนการส่งเอกสารได้ คุณสามารถใช้หน้านี้เพื่อดูล็อกการส่งสำหรับเอกสารที่ส่งแล้วทั้งหมด

1. ไปที่ **การจัดการองค์กร \> ประจำงวด \> เอกสารอิเล็กทรอนิกส์ \> ล็อกการส่งเอกสารอิเล็กทรอนิกส์**
2. ในฟิลด์ **ชนิดเอกสาร** ให้เลือก **ส่วนหัวของเอกสารทางการเงิน** ที่จะกรองข้อมูลสำหรับเอกสารทางการเงินเท่านั้น
3. ในบานหน้าต่างการดำเนินการ ให้เลือก **การสอบถาม \> รายละเอียดการส่ง** เพื่อดูรายละเอียดของล็อกการดำเนินการส่ง

![การดูรายละเอียดล็อกการส่ง](media/e-Invoicing-services-get-started-BRA-View-Submission-log-details.png)

> [!NOTE] 
> สำหรับเอกสารทางการเงิน NF-e คอลัมน์ **รหัสข้อผิดพลาด** จะแสดงรหัสส่งคืน ที่ส่งคืนโดยบริการเว็บ SEFAZ

### <a name="view-submission-logs-through-the-fiscal-document-page"></a>ดูล็อกการส่งผ่านหน้าเอกสารทางการเงิน

หลังจากที่คุณเปิดใช้คุณลักษณะ **การรวม add-on ของการออกใบแจ้งหนี้ทางอิเล็กทรอนิกส์ที่จัดโครงแบบ** คุณยังสามารถดูล็อกการส่งผ่านทางหน้าเอกสารทางการเงิน

1. ไปที่ **บัญชีแยกประเภททั่วไป \> การสอบถามและรายงาน \> เอกสารทางการเงิน \> เอกสารทางการเงินทั้งหมด**
2. เลือกเอกสารทางการเงินที่มีการส่งมาก่อนหน้านี้บน add-on ของใบแจ้งหนี้อิเล็กทรอนิกส์
3. บนบานหน้าต่างการดำเนินการ บนแท็บ **ภาครัฐ NF-e** เลือก **ล็อกเอกสารอิเล็กทรอนิกส์**

![การดูล็อกการส่งจากหน้าเอกสารทางการเงิน](media/e-Invoicing-services-get-started-BRA-View-Submission-log-from-Fiscal-document-viewer.png)

### <a name="submit-approved-nf-e-fiscal-documents-for-sefaz-cancellation"></a>ส่งเอกสารทางการเงิน NF-E ที่อนุมัติ สำหรับการยกเลิก SEFAZ

หลังจากที่คุณเปิดใช้งานคุณลักษณะ **การรวม add-on ของใบแจ้งหนี้ทางอิเล็กทรอนิกส์ที่จัดโครงแบบ** กระบวนการเก่าสำหรับการยกเลิกเอกสารทางการเงิน NF-e จะไม่สามารถใช้ได้อีกต่อไป ซึ่งจะถูกแทนที่โดยกระบวนการยกเลิกใหม่ที่ฝังอยู่บนหน้า **ล็อกการส่งเอกสารอิเล็กทรอนิกส์**

> [!NOTE]
> ตรวจสอบให้แน่ใจว่าคุณได้รันการยกเลิกเอกสารทางการเงินของลูกค้าสำหรับเอกสารทางการเงิน NF-E ที่ได้รับอนุมัติแล้ว สำหรับข้อมูลเพิ่มเติม ให้ดู [ยกเลิกเอกสารทางการเงินของลูกค้า (บราซิล)](https://docs.microsoft.com/dynamics365/finance/localizations/latam-bra-cancel-customer-fiscal-documents)

1. ไปที่ **การจัดการองค์กร \> ประจำงวด \> เอกสารอิเล็กทรอนิกส์ \> ล็อกการส่งเอกสารอิเล็กทรอนิกส์**
2. เลือกเอกสารทางการเงิน แล้วเลือก **ฟังก์ชัน \> ส่งการส่งที่เกี่ยวข้อง**
3. ป้อนคำอธิบายสำหรับการส่งที่เกี่ยวข้อง แล้วเลือก **ตกลง**

### <a name="view-cancellation-submission-logs"></a>ดูล็อกการส่งการยกเลิก

1. ไปที่ **การจัดการองค์กร \> ประจำงวด \> เอกสารอิเล็กทรอนิกส์ \> ล็อกการส่งเอกสารอิเล็กทรอนิกส์**
2. ในฟิลด์ **ชนิดเอกสาร** ให้เลือก **ส่วนหัวของเอกสารทางการเงิน** ที่จะกรองข้อมูลสำหรับเอกสารทางการเงินเท่านั้น
3. เลือกเอกสารทางการเงิน จากนั้น ในบานหน้าต่างการดำเนินการ ให้เลือก **การสอบถาม \> การส่งที่เกี่ยวข้อง**

    การส่งที่เกี่ยวข้องจะมีการส่งที่เกี่ยวข้องกับการส่งหลักที่ทำก่อน ตัวอย่างเช่น การส่งที่อนุมัติ NF-E เฉพาะคือการส่งหลัก การส่งที่ร้องขอการยกเลิก NF-E เดียวกันใน SEFAZ เป็นการส่งที่เกี่ยวข้อง ซึ่งมีอยู่เนื่องจากกำลังร้องขอการยกเลิกงานที่ทำเสร็จแล้วผ่านการส่งอื่น

    หน้า **การส่งที่เกี่ยวข้อง** จะแสดงการส่งที่เกี่ยวข้องทั้งหมด และสถานะการส่ง สำหรับเอกสารทางการเงินที่ให้ ในภาพประกอบต่อไปนี้ บรรทัดแรกแสดงถึงการส่งที่ร้องขอการอนุมัติของเอกสารทางการเงิน บรรทัดที่สองแสดงถึงการส่งที่ยกเลิกเอกสารทางการเงินนั้น

    ![การดูล็อกการส่งการยกเลิก](media/e-Invoicing-services-get-started-BRA-View-Cancellation-Submission-log.png)

4. ในบานหน้าต่างการดำเนินการ ให้เลือก **การสอบถาม \> รายละเอียดการส่ง** เพื่อดูรายละเอียดของล็อกการดำเนินการส่ง

    ![การดูรายละเอียดล็อกการส่งการยกเลิก](media/e-Invoicing-services-get-started-BRA-View-Cancellation-Submission-log-details.png)

## <a name="privacy-notice"></a>ประกาศความเป็นส่วนตัว
การเปิดใช้งานคุณลักษณะ BR-00053 (NF-e Federal) อาจจำเป็นต้องใช้การส่งข้อมูลที่จำกัด ซึ่งรวมถึงรหัสทะเบียนภาษีขององค์กร การทำเช่นนี้จะถูกส่งไปยังหน่วยงานของบุคคลที่สามที่ได้รับอนุมัติจากหน่วยงานจัดเก็บภาษี เพื่อวัตถุประสงค์ในการส่งใบแจ้งหนี้อิเล็กทรอนิกส์ให้กับหน่วยงานจัดเก็บภาษี ในรูปแบบที่กำหนดไว้ล่วงหน้าซึ่งจำเป็นสำหรับการรวมกับเว็บเซอร์วิสของรัฐ ผู้ดูแลระบบสามารถเปิดใช้งานและปิดใช้งานคุณลักษณะ BR-00053 (NF-e Federal) โดยนำทางไปยัง **การจัดการองค์กร \> การตั้งค่า \> พารามิเตอร์เอกสารอิเล็กทรอนิกส์** เลือกแท็บ **คุณลักษณะ** เลือกแถวที่มีคุณลักษณะของ BR-00053 แล้วทำการเลือกที่เหมาะสม ข้อมูลที่นำเข้าจากระบบภายนอกเหล่านี้ไปยังบริการออนไลน์ของ Dynamics 365 อยู่ภายใต้ [คำชี้แจงสิทธิส่วนบุคคล](https://go.microsoft.com/fwlink/?LinkId=512132) ของเรา กรุณาดูที่หัวข้อประกาศเกี่ยวกับความเป็นส่วนตัวในเอกสารประกอบลักษณะเฉพาะของประเทศ สำหรับข้อมูลเพิ่มเติม


## <a name="additional-resources"></a>ทรัพยากรเพิ่มเติม

- [ภาพรวมของ add-on ของใบแจ้งหนี้อิเล็กทรอนิกส์](e-invoicing-service-overview.md)
- [เริ่มต้นใช้งาน add-on ของใบแจ้งหนี้อิเล็กทรอนิกส์](e-invoicing-get-started.md)
- [ตั้งค่า add-on ของใบแจ้งหนี้อิเล็กทรอนิกส์](e-invoicing-setup.md)
