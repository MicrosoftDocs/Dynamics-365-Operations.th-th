---
title: ปรับปรุงการติดตามผลของรายงานการรายงานทางอิเล็กทรอนิกส์ที่จัดทำเพื่อเปรียบเทียบกับค่าพื้นฐาน
description: บทความนี้จะอธิบายถึงการปรับปรุงคุณลักษณะเกณฑ์พื้นฐานของ ER ใน Microsoft Dynamics 365 Finance รุ่น 10.0.3 (มิถุนายน 2019)
author: kfend
ms.date: 06/19/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.search.region: Global
ms.author: filatovm
ms.search.validFrom: 2018-04-01
ms.dyn365.ops.version: Release 8.0
ms.custom: 220314
ms.assetid: 2685df16-5ec8-4fd7-9495-c0f653e82567
ms.openlocfilehash: d0f64c459ee72ffa2b0e540d4194ca887502780f
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 08/12/2022
ms.locfileid: "9279074"
---
# <a name="improve-tracing-the-results-of-generated-er-reports-to-compare-with-baseline-values"></a>ปรับปรุงการติดตามผลของรายงานการรายงานทางอิเล็กทรอนิกส์ที่จัดทำเพื่อเปรียบเทียบกับค่าพื้นฐาน

[!include[banner](../includes/banner.md)]

บทความนี้จะอธิบายถึงชุดของการปรับปรุงแรกที่ได้ทำไว้กับคุณลักษณะพื้นฐานของกรอบงานการรายงานทางอิเล็กทรอนิกส์ (ER) การปรับปรุงเหล่านี้พร้อมใช้งานใน Microsoft Dynamics 365 Finance รุ่น 10.0.3 (มิถุนายน 2019) และใหม่กว่า

## <a name="automate-the-setting-of-baseline-rules"></a>ทำให้การตั้งค่าของกฎพื้นฐานเป็นแบบอัตโนมัติ

บทความ [สืบค้นกลับผลลัพธ์ของรายงานที่สร้างและเปรียบเทียบกับข้อมูลพื้นฐาน](er-trace-reports-compare-baseline.md) อธิบายถึงวิธีการตั้งค่าคอนฟิกกรอบงาน ER เพื่อรวบรวมข้อมูลเกี่ยวกับการดำเนินการรูปแบบ ER และประเมินผลลัพธ์ของการดำเนินการเหล่านั้น ตัวอย่างของบทความนี้ แสดงขั้นตอนที่ต้องทำให้เสร็จสมบูรณ์

ต่อไปนี้เป็นขั้นตอนบางรายการ:

- รันรูปแบบ ER เพื่อสร้างไฟล์ขาออก และจัดเก็บไฟล์เฉพาะที่
- เพิ่มไฟล์ที่จัดเก็บเฉพาะที่เป็นเอกสารแนบของข้อมูลพื้นฐานที่ถูกเพิ่มสำหรับรูปแบบ ER
- ตั้งค่าคอนฟิกกฎพื้นฐานสำหรับข้อมูลพื้นฐานที่เพิ่ม การตั้งค่าคอนฟิกนี้ประกอบด้วยขั้นตอนต่อไปนี้:

    - ระบุองค์ประกอบรูปแบบ ER ซึ่งใช้ในการสร้างไฟล์ขาออก
    - เลือกเอกสารแนบซึ่งอ้างอิงถึงไฟล์ขาออกที่สร้างขึ้น

> [!NOTE]
> ขั้นตอนเหล่านี้ต้องดำเนินการด้วยตนเอง ถึงแม้ว่าความสามารถของ ER ใหม่จะเปิดใช้งานให้เป็นระบบอัตโนมัติ เมื่อต้องการเรียนรู้เพิ่มเติมเกี่ยวกับคุณลักษณะนี้ ให้ดำเนินการตัวอย่างต่อไปนี้ให้เสร็จสมบูรณ์

## <a name="example-automate-the-setting-of-baseline-rules"></a>ตัวอย่าง: ทำให้การตั้งค่าของกฎพื้นฐานเป็นแบบอัตโนมัติ

เมื่อต้องการดำเนินการตามขั้นตอนต่างๆ ในตัวอย่างนี้ให้เสร็จสมบูรณ์ ก่อนอื่นคุณต้องดำเนินการขั้นตอนต่างๆ ในตัวอย่างให้เสร็จสมบูรณ์ในบทความ [สืบค้นกลับรายงานที่สร้างและเปรียบเทียบกับค่าพื้นฐาน](er-trace-reports-compare-baseline.md) จนถึงส่วน "เพิ่มข้อมูลพื้นฐานใหม่สำหรับรูปแบบ ER ที่ได้รับการออกแบบ"

### <a name="review-added-baseline"></a>ตรวจทานพื้นฐานที่เพิ่ม

1. ไปที่ **การจัดการองค์กร** \> **การรายงานทางอิเล็กทรอนิกส์** \> **การตั้งค่าคอนฟิก**
2. เลือก **ข้อมูลพื้นฐาน**

    > [!NOTE]
    > ปุ่ม **ข้อมูลพื้นฐาน** ในบานหน้าต่างการดำเนินการ จะพร้อมใช้งานเฉพาะเมื่อพารามิเตอร์ผู้ใช้ ER **รันในโหมดดีบัก** ถูกเปิดสำหรับบริษัทปัจจุบันเท่านั้น

มีการเพิ่มข้อมูลพื้นฐานสำหรับรูปแบบ **รูปแบบเพื่อเรียนรู้ข้อมูลพื้นฐาน ER** ที่เลือก แต่ยังไม่มีการเพิ่มกฎพื้นฐานสำหรับข้อมูลพื้นฐานนี้

![หน้าเกณฑ์พื้นฐานของรูปแบบการรายงานทางอิเล็กทรอนิกส์ ยังไม่มีกฎ](media/GER-BaselineSample-AddBaseline2.PNG "ภาพหน้าจอของหน้าเกณฑ์พื้นฐานของรูปแบบการรายงานทางอิเล็กทรอนิกส์")

### <a name="make-a-new-baseline-rule"></a>สร้างกฎพื้นฐานใหม่

1. ไปที่ **การจัดการองค์กร** \> **การรายงานทางอิเล็กทรอนิกส์** \> **การตั้งค่าคอนฟิก**
2. ในแผนภูมิ ให้ขยาย **แบบจำลองเพื่อเรียนรู้ข้อมูลพื้นฐาน ER**
3. ในแผนภูมิ ให้เลือก **แบบจำลองเพื่อเรียนรู้ข้อมูลพื้นฐาน ER\\รูปแบบเพื่อเรียนรู้ข้อมูลพื้นฐาน ER**
4. บน FastTab **รุ่น** เลือก **รัน**
5. ในฟิลด์ **ป้อน Id** ป้อน **1**
6. ตั้งค่าตัวเลือก **สร้างไฟล์พื้นฐาน** เป็น **ใช่**
7. เลือก **ตกลง**
8. เลือก **ข้อมูลพื้นฐาน**

    ![หน้าเกณฑ์พื้นฐานของรูปแบบการรายงานทางอิเล็กทรอนิกส์ เกณฑ์พื้นฐานที่เลือก](media/GER-BaselineSample-ReviewAddedBaselineLine.PNG "ภาพหน้าจอของหน้าเกณฑ์พื้นฐานของรูปแบบการรายงานทางอิเล็กทรอนิกส์")

    มีการแนบไฟล์ขาออกที่สร้างขึ้นโดยอัตโนมัติไปยังข้อมูลพื้นฐานของรูปแบบ ER ที่ดำเนินการแล้ว กฎพื้นฐานถูกเพิ่มโดยอัตโนมัติไปยังข้อมูลพื้นฐานนี้ และนอกจากนี้ ยังมีการอ้างอิงไปยังไฟล์ที่แนบด้วย

9. ในฟิลด์ **ชื่อ** ให้ป้อน **พื้นฐาน 1**
10. ในฟิลด์ **ตัวพรางชื่อไฟล์** ป้อน **.xml**
11. เลือก **บันทึก**

### <a name="run-the-format"></a>รันรูปแบบ

ขณะนี้คุณพร้อมที่จะดำเนินการขั้นตอนที่เหลือในตัวอย่างให้เสร็จสมบูรณ์ในบทความ [สืบค้นกลับรายงานผลลัพธ์ที่สร้างและเปรียบเทียบกับค่าพื้นฐาน](er-trace-reports-compare-baseline.md) ซึ่งเริ่มต้นจากส่วน "รันรูปแบบ ER ที่มีการออกแบบ และตรวจสอบล็อกเพื่อวิเคราะห์ผลลัพธ์"

> [!NOTE]
> เมื่อคุณลบกฎพื้นฐานที่เพิ่มโดยอัตโนมัติบน FastTab **ข้อมูลพื้นฐาน** เอกสารแนบที่อ้างอิงจะไม่ถูกลบโดยอัตโนมัติ

## <a name="configure-the-baseline-so-that-it-ignores-constantly-changing-parts-of-the-er-output"></a>ตั้งค่าคอนฟิกข้อมูลพื้นฐานเพื่อให้ละเว้นส่วนที่เปลี่ยนแปลงอยู่เสมอของเอาท์พุท ER

เมื่อรูปแบบ ER ได้รับการออกแบบมาเพื่อให้มีข้อมูลที่มีการเปลี่ยนแปลงเมื่อรันรูปแบบ จึงจำเป็นต้องใช้คุณลักษณะพื้นฐานของ ER เพื่อเปรียบเทียบผลลัพธ์ที่สร้างขึ้นกับค่าพื้นฐาน ตัวอย่างเช่น ข้อมูลนี้อาจเป็นวันที่และเวลาที่ใช้ในการประมวลผล หรือตัวระบุเฉพาะของเอกสารที่สร้างขึ้นในรูปแบบที่แตกต่างกัน (ตัวระบุที่ไม่ซ้ำกันส่วนกลาง \[GUID\] และอื่นๆ) ความสามารถของ ER ใหม่ช่วยให้คุณสามารถตั้งค่าคอนฟิกกฎพื้นฐาน เพื่อให้ละเว้นองค์ประกอบที่สามารถเปลี่ยนแปลงได้ของรูปแบบ ER เมื่อมีการรันรูปแบบ โดยมีวัตถุประสงค์ของการเปรียบเทียบค่าพื้นฐานกับผลลัพธ์ของการดำเนินการของรูปแบบ เมื่อต้องการเรียนรู้เพิ่มเติมเกี่ยวกับคุณลักษณะนี้ ให้ดำเนินการตัวอย่างต่อไปนี้ให้เสร็จสมบูรณ์

## <a name="example-configure-the-baseline-so-that-it-ignores-constantly-changing-parts-of-the-er-output"></a>ตัวอย่าง: ตั้งค่าคอนฟิกข้อมูลพื้นฐานเพื่อให้ละเว้นส่วนที่เปลี่ยนแปลงอยู่เสมอของเอาท์พุท ER

เมื่อต้องการดำเนินการขั้นตอนต่างๆ ในตัวอย่างนี้ให้เสร็จสมบูรณ์ ก่อนอื่นคุณต้องดำเนินการขั้นตอนต่างๆ ในตัวอย่างให้เสร็จสมบูรณ์ในบทความ [สืบค้นกลับรายงานที่สร้างและเปรียบเทียบกับค่าพื้นฐาน](er-trace-reports-compare-baseline.md)

### <a name="modify-a-configured-er-format"></a>ปรับเปลี่ยนรูปแบบ ER ที่ตั้งค่าคอนฟิก

1. ไปที่ **การจัดการองค์กร** \> **การรายงานทางอิเล็กทรอนิกส์** \> **การตั้งค่าคอนฟิก**
2. ในแผนภูมิ ให้ขยาย **แบบจำลองเพื่อเรียนรู้ข้อมูลพื้นฐาน ER**
3. ในแผนภูมิ ให้เลือก **แบบจำลองเพื่อเรียนรู้ข้อมูลพื้นฐาน ER\\รูปแบบเพื่อเรียนรู้ข้อมูลพื้นฐาน ER**
4. เลือก **ตัวออกแบบ**
5. ในแผนภูมิ ให้เลือก **เอาท์พุท\\เอกสาร**
6. เลือก **เพิ่ม**
7. ในกล่องโต้ตอบรายการแบบหล่นลง ในแผนภูมิ ให้เลือก **XML\\แอตทริบิวต์**
8. ในฟิลด์ **ชื่อ** ให้ป้อน **ProcessingDateTime**
9. เลือก **ตกลง**
10. บนแท็บ **การแม็ป** ในแผนภูมิ ให้เลือก **เอาท์พุท\\เอกสาร\\ProcessingDateTime**
11. เลือก **แก้ไขสูตร**
12. ในฟิลด์ **สูตร** ให้ป้อนนิพจน์ต่อไปนี้: **DATETIMEFORMAT(NOW(), "O")**
13. เลือก **บันทึก** แล้วจากนั้น เลือก **ทดสอบ**
14. เลือก **ทดสอบ** อีกครั้ง เพื่อทดสอบนิพจน์ที่ตั้งค่าคอนฟิกอีกครั้ง

    ![หน้าโปรแกรมออกแบบสูตร](media/GER-BaselineSample-DefineProcessingDTExpression.PNG "ภาพหน้าจอของหน้าโปรแกรมออกแบบสูตร")

    > [!NOTE]
    > แท็บ **ผลลัพธ์การทดสอบ** แสดงให้เห็นว่านิพจน์ที่ตั้งค่าคอนฟิกจะส่งคืนค่าวันที่และเวลาที่แตกต่างกัน เมื่อใดก็ตามที่มีการเรียก

15. ปิดหน้า **ตัวออกแบบสูตร** และจากนั้น เลือก **บันทึก**

    ![หน้าตัวออกแบบรูปแบบ](media/GER-BaselineSample-FormatMappingDesign2.PNG "ภาพหน้าจอของหน้าโปรแกรมออกแบบรูปแบบ")

16. ปิดหน้า **ตัวออกแบบรูปแบบ**

### <a name="remove-an-existing-baseline-rule"></a>ลบกฎพื้นฐานที่มีอยู่

1. ไปที่ **การจัดการองค์กร** \> **การรายงานทางอิเล็กทรอนิกส์** \> **การตั้งค่าคอนฟิก**
2. เลือก **ข้อมูลพื้นฐาน**
3. ในรายการของข้อมูลพื้นฐาน ให้เลือกข้อมูลพื้นฐานที่มีการตั้งค่าคอนฟิกสำหรับรูปแบบ **รูปแบบเพื่อเรียนรู้ข้อมูลพื้นฐาน ER**
4. บน FastTab **ข้อมูลพื้นฐาน** ให้เลือก **ลบ** เพื่อลบกฎพื้นฐานที่คุณตั้งค่าคอนฟิกไว้ก่อนหน้านี้

![หน้าเกณฑ์พื้นฐานของรูปแบบการรายงานทางอิเล็กทรอนิกส์ ที่ลบ](media/GER-BaselineSample-AddBaseline3.PNG "ภาพหน้าจอของหน้าเกณฑ์พื้นฐานของรูปแบบการรายงานทางอิเล็กทรอนิกส์")

### <a name="define-replacements-for-bindings-of-designed-er-format"></a>กำหนดการแทนที่สำหรับการผูกรูปแบบ ER ที่ออกแบบ

1. บนหน้า **การตั้งค่าคอนฟิก** บน FastTab **การแทนที่** ให้เลือก **เลือกส่วนประกอบ**
2. ในแผนภูมิส่วนประกอบของรูปแบบ ขยาย **เอาท์พุท** ขยาย **เอาท์พุท\\เอกสาร** และจากนั้น เลือกกล่องกาเครื่องหมายสำหรับ **เอาท์พุท\\เอกสาร\\ProcessingDateTime**
3. เลือก **ตกลง**

![หน้าเกณฑ์พื้นฐานของรูปแบบการรายงานทางอิเล็กทรอนิกส์ ส่วนประกอบ](media/GER-BaselineSample-AddBaseline4.PNG "ภาพหน้าจอของหน้าเกณฑ์พื้นฐานของรูปแบบการรายงานทางอิเล็กทรอนิกส์")

มีการเพิ่มส่วนประกอบของรูปแบบ ER ที่เลือกลงในรายการของส่วนประกอบบน FastTab **การแทนที่** เมื่อมีการรันรูปแบบ ER ฐานในโหมดดีบัก การผูกข้อมูลของรูปแบบสำหรับแต่ละส่วนประกอบจะถูกแทนที่ด้วยการผูกที่แสดงในคอลัมน์ **การผูก** เมื่อต้องการเปลี่ยนการผูกข้อมูลเริ่มต้นสำหรับส่วนประกอบที่แสดงรายการอยู่บน FastTab **การแทนที่** เลือก **แก้ไข**

### <a name="make-a-new-baseline-rule"></a>สร้างกฎพื้นฐานใหม่

ทำตามขั้นตอนในส่วน "ตัวอย่าง: ทำให้การตั้งค่าของกฎพื้นฐานเป็นระบบอัตโนมัติ" ก่อนหน้านี้ในบทความนี้ การแจ้งเตือนจะเตือนคุณว่าไฟล์ขาออกถูกสร้างขึ้นโดยใช้การตั้งค่าพื้นฐาน และมีการแทนที่ที่บังคับของการผูกรูปแบบเกิดขึ้น

![การแจ้งเตือนบนหน้าการตั้งค่าคอนฟิก](media/GER-BaselineSample-FormatRunToMakeBaselineFile4.PNG "ภาพหน้าจอของการแจ้งเตือนบนหน้าการตั้งค่าคอนฟิก")

### <a name="suppress-warnings-about-the-replacement-of-format-bindings"></a>ระงับคำเตือนเกี่ยวกับการแทนที่ของการผูกรูปแบบ

ด้วยการตั้งค่าพารามิเตอร์ ER เฉพาะ คุณสามารถระงับการแจ้งเตือนที่เตือนเกี่ยวกับการแทนที่ของการผูกรูปแบบได้ การระงับนี้อาจเป็นประโยชน์ เมื่อมีการแทนที่การผูกรูปแบบในโหมดการทำงานอัตโนมัติโดยใช้ Regression Suite Automation Tool ในกรณีนี้ การเตือนอาจถือเป็นความล้มเหลวของกรณีทดสอบที่กำลังรันอยู่

1. ในหน้า **การตั้งค่าคอนฟิก** บนบานหน้าต่างการดำเนินการ บนแท็บ **การตั้งค่าคอนฟิก** เลือก **พารามิเตอร์ผู้ใช้**
2. ตั้งค่าตัวเลือก **ระงับคำเตือนพื้นฐาน** เป็น **ใช่** แล้วเลือก **ตกลง**

### <a name="review-the-generated-baseline-file"></a>ตรวจทานไฟล์พื้นฐานที่สร้างขึ้น

1. ไปที่ **การจัดการองค์กร** \> **การรายงานทางอิเล็กทรอนิกส์** \> **การตั้งค่าคอนฟิก**
2. เลือก **ข้อมูลพื้นฐาน**
3. เลือก **เอกสารแนบ**
    > [!NOTE]
    > ไฟล์ที่สร้างขึ้นประกอบด้วย ข้อความการประมวลผลวันที่และเวลา (**"#"**) จากการผูกที่มีการตั้งค่าคอนฟิกในกฎพื้นฐานที่เพิ่มเข้ามา ไม่ใช่จากการผูกข้อมูลของรูปแบบ
    
4. ปิดหน้า **เอกสารแนบ**

### <a name="run-the-designed-er-format-and-review-the-log-to-analyze-the-results"></a>รันรูปแบบ ER ที่ออกแบบ และตรวจสอบล็อกเพื่อวิเคราะห์ผลลัพธ์

1. ไปที่ **การจัดการองค์กร** \> **การรายงานทางอิเล็กทรอนิกส์** \> **การตั้งค่าคอนฟิก**
2. ในแผนภูมิ ให้ขยาย **แบบจำลองเพื่อเรียนรู้ข้อมูลพื้นฐาน ER**
3. ในแผนภูมิ ให้เลือก **แบบจำลองเพื่อเรียนรู้ข้อมูลพื้นฐาน ER\\รูปแบบเพื่อเรียนรู้ข้อมูลพื้นฐาน ER**
4. บน FastTab **รุ่น** เลือก **รัน**
5. ในฟิลด์ **ป้อน Id** พิมพ์ **1**
6. เลือก **ตกลง**
7. ไปที่ **การจัดการองค์กร** \> **การรายงานทางอิเล็กทรอนิกส์** \> **ล็อกดีบักการตั้งค่าคอนฟิก**

ล็อกการดำเนินการประกอบด้วย ข้อมูลเกี่ยวกับผลลัพธ์ของการเปรียบเทียบของไฟล์ที่สร้างขึ้นโดยใช้ข้อมูลพื้นฐานที่ตั้งค่าคอนฟิก ล็อกจะบ่งชี้ว่าไฟล์ที่สร้างและข้อมูลพื้นฐานเท่ากัน ถึงแม้ว่ารูปแบบที่ดำเนินการจะมีการผูกข้อมูลเพื่อป้อนค่าวันที่และเวลาที่เปลี่ยนแปลงอย่างต่อเนื่องในไฟล์ขาออก

> [!NOTE]
> ถึงแม้ว่าไฟล์ขาออกถูกสร้างขึ้นโดยใช้การตั้งค่าพื้นฐานที่บังคับการแทนที่ของการผูกของรูปแบบ คุณจะไม่ได้รับคำเตือนใดๆ เกี่ยวกับการแทนที่

## <a name="exchange-baseline-settings-between-environments"></a>แลกเปลี่ยนการตั้งค่าพื้นฐานระหว่างสภาพแวดล้อม

### <a name="export-baseline-settings"></a>ส่งออกการตั้งค่าพื้นฐาน

ความสามารถ ER ใหม่ช่วยให้คุณสามารถส่งออกการตั้งค่าพื้นฐานสำหรับรูปแบบ ER ที่เลือกจากสภาพแวดล้อมปัจจุบัน และจัดเก็บเป็นไฟล์ XML 

เมื่อต้องการส่งออกการตั้งค่าพื้นฐานบนหน้า **ข้อมูลพื้นฐานรูปแบบการรายงานทางอิเล็กทรอนิกส์** เลือก **ส่งออก**

### <a name="import-baseline-settings"></a>การตั้งค่านำเข้าเกณฑ์พื้นฐาน

มีการนำเข้าการตั้งค่าพื้นฐานที่ส่งออกไปยังสภาพแวดล้อมที่แตกต่างกัน ต้องมีการนำเข้าสภาพแวดล้อมเป็นรูปแบบ ER ก่อน จากนั้น คุณสามารถนำเข้าการตั้งค่าพื้นฐาน

เมื่อต้องการนำเข้าการตั้งค่าพื้นฐานจากไฟล์ XML ที่จัดเก็บไว้เฉพาะที่ บนหน้า **ข้อมูลพื้นฐานรูปแบบการรายงานทางอิเล็กทรอนิกส์** เลือก **นำเข้า** และจากนั้น เลือก **เรียกดู** เพื่อเลือกไฟล์ XML

![นำเข้ากล่องโต้ตอบการตั้งค่าเกณฑ์พื้นฐาน](media/GER-BaselineSample-ImportBaseline1.PNG "ภาพหน้าจอของกล่องโต้ตอบการตั้งค่านำเข้าเกณฑ์พื้นฐาน")

เมื่อต้องการนำเข้าการตั้งค่าพื้นฐานจากไฟล์ XML ที่จัดเก็บบน Microsoft SharePoint Server ตามการตั้งค่าการจัดการเอกสารปัจจุบัน และชนิดเอกสารที่เลือก บนหน้า **ข้อมูลพื้นฐานรูปแบบการรายงานทางอิเล็กทรอนิกส์** ให้เลือก **นำเข้าจากแหล่งที่มา** จากนั้น เลือกชนิดเอกสารและไฟล์ XML ต้องมีการตั้งค่าคอนฟิกชนิดเอกสารที่จำเป็นต้องใช้ในการเข้าถึงโฟลเดอร์ SharePoint ไว้ล่วงหน้า

![นำเข้าจากกล่องโต้ตอบแหล่งที่มา](media/GER-BaselineSample-ImportBaseline2.PNG "ภาพหน้าจอของกล่องโต้ตอบนำเข้าจากแหล่งที่มา")

> [!NOTE]
> คุณสามารถใช้ตัวบันทึกงานเพื่อบันทึกขั้นตอนสำหรับการเลือกชนิดเอกสารที่จำเป็นและชื่อไฟล์ในกล่องโต้ตอบ **นำเข้าจากแหล่งที่มา** ด้วยวิธีนี้ คุณสามารถรักษาการตั้งค่าพื้นฐานที่จำเป็นบน SharePoint Server แล้วนำเข้าโดยอัตโนมัติโดยการใช้การบันทึกงาน เมื่อคุณรันการทดสอบแบบอัตโนมัติโดยใช้ Regression Suite Automation Tool

## <a name="additional-resources"></a>แหล่งข้อมูลเพิ่มเติม

- [ติดตามผลของรายงานที่จัดทำและเปรียบเทียบผลกับค่าพื้นฐาน](er-trace-reports-compare-baseline.md)
- [ทรัพยากรตัวบันทึกงาน](../user-interface/task-recorder.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]

