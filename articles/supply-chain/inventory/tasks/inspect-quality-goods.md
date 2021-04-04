---
title: ตรวจสอบคุณภาพของสินค้า
description: หัวข้อนี้อธิบายวิธีการประมวลผลใบสั่งตรวจสอบคุณภาพ
author: perlynne
manager: tfehr
ms.date: 08/01/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventQualityOrderTable, InventQualityOrderLineResults, HcmWorkerLookUp
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: e37ac8c9320d427b9f9a3ca32b0e4667c7023339
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 02/15/2021
ms.locfileid: "5244434"
---
# <a name="inspect-the-quality-of-goods"></a>ตรวจสอบคุณภาพของสินค้า

[!include [banner](../../includes/banner.md)]

หัวข้อนี้อธิบายวิธีการประมวลผลใบสั่งตรวจสอบคุณภาพ คุณสามารถรันคำแนะนำนี้ในบริษัทข้อมูลสาธิต USMF ก่อนที่คุณเริ่มกระบวนงานตัวอย่างนี้ คุณจำเป็นต้องยืนยันใบสั่งซื้อ "000016" และลงรายการบัญชีใบรับสินค้า ซึ่งจะสร้างใบสั่งตรวจสอบคุณภาพโดยอัตโนมัติ ตรวจสอบคุณภาพจะโดยทั่วไปจะดำเนินการโดยเจ้าหน้าที่ตรวจสอบคุณภาพ


## <a name="select-a-quality-order"></a>เลือกใบสั่งตรวจสอบคุณภาพ
1. ในบานหน้าต่างนำทาง ไปที่ **โมดูล > การจัดการสินค้าคงคลัง > งานประจำงวด > การจัดการคุณภาพ > ใบสั่งตรวจสอบคุณภาพ**
2. เลือกใบสั่งตรวจสอบคุณภาพที่สร้างขึ้นก่อนที่คุณเริ่มต้นขั้นตอนนี้  

## <a name="record-test-results"></a>บันทึกผลการทดสอบ
1. เลือก **ผลลัพธ์**
2. เลือก **แก้ไข**
3. ในฟิลด์ **ปริมาณผลลัพธ์** ให้ป้อนตัวเลข
4. ในฟิลด์ **ผลลัพธ์** ให้เลือกเรกคอร์ดที่ต้องการในเมนูแบบหล่นลง  
- ในตัวอย่างนี้ ผลลัพธ์จะขึ้นอยู่กับผลลัพธ์กำหนดไว้  โดยปกติแล้วคุณจะบันทึกผลการทดสอบเฉพาะเจาะจงยิ่งขึ้น ตัวอย่างเช่นขนาดหรือมิติอื่น  
5. เลือก **บันทึก**
6. ปิดหน้า

## <a name="validate-the-quality-order"></a>ตรวจสอบความถูกต้องของใบสั่งตรวจสอบคุณภาพ
1. เลือก **ตรวจสอบความถูกต้อง**
2. ในฟิลด์ **ตรวจสอบความถูกต้องตาม** ให้เลือกผู้ใช้ที่ดำเนินการตรวจสอบจากเมนูแบบหล่นลง  
3. คลิก **เลือก**
4. เลือก **ตกลง**
5. ปิดหน้า



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]