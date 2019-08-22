---
title: สร้างระบบการตั้งชื่อแบบหมายเลขผลิตภัณฑ์สำหรับผลิตภัณฑ์ย่อยที่กำหนดไว้ล่วงหน้า
description: 'คู่มือนี้แสดงวิธีการตั้งค่าระบบการตั้งชื่อสำหรับหมายเลขผลิตภัณฑ์สำหรับผลิตภัณฑ์ย่อยที่กำหนดไว้ล่วงหน้า และวิธีการกำหนดให้กับกลุ่มมิติของผลิตภัณฑ์ที่เหมาะสม '
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: DefaultDashboard, EcoResProductVariantMaintainWorkspace, EcoResNomenclature, EcoResProductDimensionGroup
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 6a2e61fd99cb80a1a9cc3d8e985fb0f14e3c2fc2
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 08/01/2019
ms.locfileid: "1844692"
---
# <a name="create-a-product-number-nomenclature-for-predefined-product-variants"></a>สร้างระบบการตั้งชื่อแบบหมายเลขผลิตภัณฑ์สำหรับผลิตภัณฑ์ย่อยที่กำหนดไว้ล่วงหน้า

[!include [task guide banner](../../includes/task-guide-banner.md)]

คู่มือนี้แสดงวิธีการตั้งค่าระบบการตั้งชื่อสำหรับหมายเลขผลิตภัณฑ์สำหรับผลิตภัณฑ์ย่อยที่กำหนดไว้ล่วงหน้า และวิธีการกำหนดให้กับกลุ่มมิติของผลิตภัณฑ์ที่เหมาะสม  บริษัทข้อมูลสาธิตที่เคยสร้างกระบวนงานนี้คือ USMF ระบบการตั้งชื่อสำหรับหมายเลขผลิตภัณฑ์ใหม่ถูกกำหนดให้กับกลุ่มมิติของผลิตภัณฑ์สีและขนาด  โดยทั่วไปงานนี้อาจดำเนินการโดยผู้ออกแบบผลิตภัณฑ์


## <a name="create-a-product-number-nomenclature"></a>สร้างระบบการตั้งชื่อสำหรับหมายเลขผลิตภัณฑ์
1. คลิก ข้อกำหนดแบบจำลองผลิตภัณฑ์ย่อย
2. คลิก ระบบการตั้งชื่อผลิตภัณฑ์
3. คลิก สร้าง
4. ในฟิลด์ชื่อ ป้อนชื่อระบบการตั้งชื่อที่ช่วยในการระบุเป้าหมายกลุ่มมิติของผลิตภัณฑ์ ตัวอย่างเช่น ColorSize
5. ในฟิลด์ คำอธิบาย ให้พิมพ์ค่า
6. คลิก เพิ่ม
7. คลิก หมายเลขผลิตภัณฑ์หลัก
8. คลิก เพิ่ม
9. คลิก ค่าคงที่ของข้อความ
10. ในฟิลด์ข้อความ ให้พิมพ์ค่า 
11. คลิก เพิ่ม
12. คลิก สี
13. คลิก เพิ่ม
14. คลิก ค่าคงที่ของข้อความ
15. ในฟิลด์ข้อความ ให้พิมพ์ค่า 
16. คลิก เพิ่ม
17. คลิก ขนาด
18. ปิดหน้า

## <a name="assign-the-nomenclature-to-a-product-master"></a>กำหนดระบบการตั้งชื่อให้กับผลิตภัณฑ์หลัก
1. คลิก กลุ่มมิติของผลิตภัณฑ์
2. เลือกกลุ่มมิติของผลิตภัณฑ์ SizeCol
3. คลิกแก้ไข
4. เลือก ใช่ ในฟิลด์ใช้ระบบการตั้งชื่อ
5. ในฟิลด์ ระบบการตั้งชื่อหมายเลขผลิตภัณฑ์ย่อย ให้ป้อนหรือเลือกค่า
6. ปิดหน้า

