---
title: ตรวจสอบคุณภาพของสินค้า
description: 'ขั้นตอนนี้แสดงให้คุณเห็นถึงวิธีการประมวลผลใบสั่งตรวจสอบคุณภาพ '
author: perlynne
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventQualityOrderTable, InventQualityOrderLineResults, HcmWorkerLookUp
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: f9e9d750f116db62519ac7148f19bf62050430e9
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 05/15/2019
ms.locfileid: "1545416"
---
# <a name="inspect-the-quality-of-goods"></a>ตรวจสอบคุณภาพของสินค้า

[!include [task guide banner](../../includes/task-guide-banner.md)]

ขั้นตอนนี้แสดงให้คุณเห็นถึงวิธีการประมวลผลใบสั่งตรวจสอบคุณภาพ  คุณสามารถรันคำแนะนำนี้ในบริษัทข้อมูลสาธิต USMF  ก่อนที่คุณเริ่มกระบวนการตัวอย่างนี้ คุณจำเป็นต้องยืนยันใบสั่งซื้อ "000016" และลงรายการบัญชีใบรับสินค้า ซึ่งจะสร้างใบสั่งตรวจสอบคุณภาพโดยอัตโนมัติ ตรวจสอบคุณภาพจะโดยทั่วไปจะดำเนินการโดยเจ้าหน้าที่ตรวจสอบคุณภาพ


## <a name="select-a-quality-order"></a>เลือกใบสั่งตรวจสอบคุณภาพ
1. ไปที่การบริหารสินค้าคงคลัง > งานประจำงวด > การจัดการคุณภาพ > ใบสั่งตรวจสอบคุณภาพ
2. ในรายการนี้ ให้ทำเครื่องหมายแถวที่เลือก
    * เลือกใบสั่งตรวจสอบคุณภาพที่สร้างขึ้นก่อนที่คุณเริ่มต้นขั้นตอนนี้  

## <a name="record-test-results"></a>บันทึกผลการทดสอบ
1. คลิก ผลลัพธ์
2. คลิก แก้ไข
3. ในฟิลด์ปริมาณผลลัพธ์ ให้ป้อนตัวเลข
4. ในรายการนี้ ให้ทำเครื่องหมายแถวที่เลือก
5. ในฟิลด์ผลที่ได้ ให้คลิกปุ่มดรอปดาวน์เพื่อเปิดการค้นหา
6. ในรายการนี้ ให้ค้นหาและเลือกเรกคอร์ดที่ต้องการ
    * ในตัวอย่างนี้ ผลลัพธ์จะขึ้นอยู่กับผลลัพธ์กำหนดไว้  โดยปกติแล้วคุณจะบันทึกผลการทดสอบเฉพาะเจาะจงยิ่งขึ้น ตัวอย่างเช่นขนาดหรือมิติอื่น  
7. ในรายการนี้ ให้คลิกลิงค์ในแถวที่เลือก
8. คลิก บันทึก
9. ปิดหน้า

## <a name="validate-the-quality-order"></a>ตรวจสอบความถูกต้องของใบสั่งตรวจสอบคุณภาพ
1. คลิก ตรวจสอบความถูกต้อง
2. ในฟิลด์ตรวจสอบความถูกต้อง ให้คลิกปุ่มดรอปดาวน์เพื่อเปิดการค้นหา
    * เลือกผู้ดำเนินการตรวจสอบ  
3. ในรายการนี้ ให้คลิกลิงค์ในแถวที่เลือก
4. คลิกเลือก 
5. คลิก ตกลง
6. ปิดหน้า

