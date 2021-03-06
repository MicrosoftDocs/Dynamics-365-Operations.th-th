---
title: จัดการหน่วยวัด
description: 'ขั้นตอนนี้แสดงวิธีการกำหนดหน่วยวัด ระบุการแปลและคำอธิบายสำหรับหน่วย และกำหนดกฎการแปลงสำหรับหน่วยที่เกี่ยวข้อง '
author: sorenva
manager: tfehr
ms.date: 07/08/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EcoResProductMaintainWorkspace, EcoResProductOpenCasesFormPart, UnitOfMeasure, UnitOfMeasureReportingTranslation, UnitOfMeasureTranslation, UnitOfMeasureConversion, UnitOfMeasureConversionEditOrCreate, UnitOfMeasureLookup, UnitOfMeasureCalculator, UnitOfMeasureWizard, UnitOfMeasureLookupTest
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: sorenand
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 71b478ca294719c20af9de16c27139aeca36bf07
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 01/15/2021
ms.locfileid: "4992306"
---
# <a name="manage-unit-of-measure"></a>จัดการหน่วยวัด

[!include [banner](../../includes/banner.md)]

ขั้นตอนนี้แสดงวิธีการกำหนดหน่วยวัด ระบุการแปลและคำอธิบายสำหรับหน่วย และกำหนดกฎการแปลงสำหรับหน่วยที่เกี่ยวข้อง  คุณสามารถแนะนำขั้นตอนนี้โดยใช้ข้อมูลสาธิต หรือใช้ข้อมูลของคุณเองได้

1. ไปยัง **บานหน้าต่างนำทาง > โมดูล > การจัดการข้อมูลผลิตภัณฑ์ > การบำรุงรักษาผลิตภัณฑ์ที่นำออกใช้**
2. คลิก **หน่วย**

## <a name="create-a-unit-of-measure"></a>สร้างหน่วยวัด
1. คลิก **สร้าง**
2. ในฟิลด์ **หน่วย** ให้พิมพ์ค่า ป้อนรหัสหรือสัญลักษณ์ที่จะใช้เมื่ออ้างอิงถึงหน่วยวัด   
3. ในฟิลด์ **คำอธิบาย** ให้พิมพ์ค่าใดค่าหนึ่ง ป้อนชื่ออธิบายสำหรับหน่วยวัดในภาษาของระบบ  
4. ในฟิลด์ **ประเภทของหน่วย** ให้เลือกหนึ่งตัวเลือก ประเภทของหน่วยกำหนดตรรกะการจัดกลุ่ม เช่นพื้นที่ มวล หรือปริมาณ หน่วยวัดก็เป็นส่วนหนึ่ง  
5. ในฟิลด์ **ความละเอียดทศนิยม** ให้ป้อนตัวเลข ระบุจำนวนของทศนิยมที่แปลงหน่วยวัดต้องปัดเศษเมื่อเสร็จสิ้นการคำนวณสำหรับหน่วยวัด   
6. คลิก **บันทึก**

## <a name="define-unit-translations"></a>กำหนดการแปลหน่วย
1. ใน **บานหน้าต่างการดำเนินการ** คลิก **ข้อความหน่วย**
2. คลิก **สร้าง** ใช้ข้อความหน่วยเพื่อสร้างการแปล ID หรือสัญลักษณ์ที่แสดงถึงหน่วยวัดสำหรับใช้ในเอกสารภายนอกในภาษาเฉพาะของลูกค้า หรือผู้จัดจำหน่าย   
3. ในฟิลด์ **ภาษา** ให้ป้อนหรือเลือกค่า
4. ในฟิลด์ **ข้อความ** ให้พิมพ์ค่า
5. คลิก **บันทึก**
6. ปิดหน้า
7. ใน **บานหน้าต่างการดำเนินการ** คลิก **คำอธิบายหน่วยที่แปล**
8. คลิก **สร้าง** กำหนดคำอธิบายภาษาเฉพาะสำหรับหน่วยวัด   
9. ในฟิลด์ **ภาษา** ให้ป้อนหรือเลือกค่า
10. ในฟิลด์ **คำอธิบาย** ให้พิมพ์ค่าใดค่าหนึ่ง
11. คลิก **บันทึก**
12. ปิดหน้า

## <a name="define-unit-conversion-rules"></a>กำหนดกฎการแปลงหน่วย
1. ใน **บานหน้าต่างการดำเนินการ** คลิก **การแปลงหน่วย** กำหนดกฎสำหรับการแปลงหน่วยวัดไปยังหน่วยวัดอื่นและจากหน่วยวัดอื่นในประเภทของหน่วยที่เลือก   
2. คลิก **สร้าง** เพื่อเปิดกล่องโต้ตอบการวาง
3. ในฟิลด์ **ปัจจัย** ให้ป้อนตัวเลข ตัวแปลงระหว่าง "หน่วยต้นทาง" และ "หน่วยปลายทาง"  ตัวอย่างเช่น ตัวแปลงจากเซนติเมตรเป็นเมตรคือ 100 เนื่องจาก 100 เซนติเมตรเป็น 1 เมตร  
4. ในฟิลด์ **หน่วยปลายทาง** ให้ป้อนหรือเลือกค่า
5. ในฟิลด์ **การปัดเศษ** ให้เลือกหนึ่งตัวเลือก กำหนดวิธีการปัดเศษค่าที่แปลง   
6. คลิก **ตกลง**
7. ปิดหน้า

