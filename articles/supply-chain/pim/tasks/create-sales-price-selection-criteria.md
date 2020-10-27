---
title: สร้างเกณฑ์การเลือกราคาขาย
description: 'กระบวนงานนี้แสดงวิธีการสร้างเกณฑ์การเลือกราคาขายสำหรับแบบจำลองราคาขายตามแอททริบิวต์ '
author: ShylaThompson
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: DefaultDashboard, EcoResProductVariantMaintainWorkspace, PCProductConfigurationModelListPage, PCPriceModelSelectionCriteria, SysQueryForm, SysQueryTableLookUp, SysQueryFieldLookUp
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 4ae444008e550d808a02d55dad02cc1b52874f0d
ms.sourcegitcommit: 708ca25687a4e48271cdcd6d2d22d99fb94cf140
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 10/10/2020
ms.locfileid: "3985472"
---
# <a name="create-sales-price-selection-criteria"></a>สร้างเกณฑ์การเลือกราคาขาย

[!include [banner](../../includes/banner.md)]

กระบวนงานนี้แสดงวิธีการสร้างเกณฑ์การเลือกราคาขายสำหรับแบบจำลองราคาขายตามแอททริบิวต์  ขั้นตอนนี้จำเป็นต้องใช้แบบจำลองราคาขายที่มีอยู่อย่างน้อยหนึ่งรายการ ตัวอย่างนี้ใช้แบบจำลองราคาสำหรับแบบจำลองราคาขายของโซลูชันลำโพงในบริษัทข้อมูลสาธิต USMF  โดยทั่วไปผู้จัดการผลิตภัณฑ์จะใช้กระบวนงานนี้


## <a name="add-a-new-criterion-for-an-existing-sales-price-model"></a>เพิ่มเกณฑ์ใหม่สำหรับแบบจำลองราคาขายที่มีอยู่
1. คลิก ข้อกำหนดแบบจำลองผลิตภัณฑ์ย่อย
2. คลิก แบบจำลองการตั้งค่าคอนฟิกผลิตภัณฑ์
3. ในรายการ เลือกแถวสำหรับแบบจำลองผลิตภัณฑ์โซลูชันลำโพง แต่อย่าคลิกลิงค์สำหรับชื่อแบบจำลอง
4. ในบานหน้าต่างการดำเนินการ คลิก แบบจำลอง
5. คลิก เกณฑ์แบบจำลองราคา
6. คลิก สร้าง
7. ในฟิลด์ชื่อ ให้พิมพ์ 'กลุ่มลูกค้า 10'
    * ใช้ชื่อของเกณฑ์แบบจำลองราคาเพื่อช่วยในการระบุเกณฑ์การเลือกที่อยู่ภายใต้  
8. ในฟิลด์แบบจำลองราคา ให้ป้อนหรือเลือกค่า
9. ในฟิลด์ชนิดใบสั่ง เลือก ใบสั่งขาย
    * ชนิดใบสั่งกำหนดฟิลด์ฐานข้อมูลที่จะใช้สำหรับการสอบถามเลือก  
10. ในฟิลด์ ใช้ได้ตั้งแต่ ให้ป้อนวันที่
11. ในฟิลด์ หมดอายุวันที่ ให้ป้อนวันที่
12. คลิก บันทึก

## <a name="create-the-query-for-the-selection-criteria"></a>สร้างการสอบถามสำหรับเกณฑ์การเลือก
1. คลิก แก้ไข
2. ในฟิลด์ตาราง ให้เลือก ลูกค้า 
3. ในฟิลด์ ฟิลด์ ให้เลือก กลุ่มลูกค้า
    * ในตัวอย่างนี้ เราจะใช้กลุ่มลูกค้าเฉพาะสำหรับเกณฑ์การเลือก  
4. ในฟิลด์ เกณฑ์ ให้เลือก 'กลุ่มลูกค้า 10' 
5. คลิก ตกลง

