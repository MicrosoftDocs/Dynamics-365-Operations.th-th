---
title: สร้างบาร์โค้ดให้ผลิตภัณฑ์
description: 'กระบวนงานนี้แสดงวิธีการสร้างบาร์โค้ดด้วยตนเองโดยใช้หมายเลขสินค้า M0001 เป็นตัวอย่าง '
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: DefaultDashboard, EcoResProductMaintainWorkspace, EcoResProductOpenCasesFormPart, EcoResProductDetailsExtended, InventItemBarcode, InventItemBarcodeLookup
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 2ae2765a125045d60566267d01e380069d5d527c
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 01/29/2019
ms.locfileid: "329401"
---
# <a name="create-a-bar-code-for-a-product"></a>สร้างบาร์โค้ดให้ผลิตภัณฑ์

[!include [task guide banner](../../includes/task-guide-banner.md)]

กระบวนงานนี้แสดงวิธีการสร้างบาร์โค้ดด้วยตนเองโดยใช้หมายเลขสินค้า M0001 เป็นตัวอย่าง  ข้อมูลบริษัทสาธิตที่ใช้ในการสร้างกระบวนงานนี้คือ USMF

1. คลิก การบำรุงรักษาผลิตภัณฑ์ที่นำออกใช้
2. คลิกผลิตภัณฑ์ต่างๆที่นำออกใช้
3. ในรายการนี้ ให้ค้นหาและเลือกเรกคอร์ดที่ต้องการ
4. ในบานหน้าต่างการดำเนินการ คลิกจัดการสินค้าคงคลัง
5. คลิก บาร์โคด
6. คลิก สร้าง
7. ในรายการนี้ ให้ทำเครื่องหมายแถวที่เลือก
8. ในฟิลด์การตั้งค่าบาร์โค้ด ให้ป้อนหรือเลือกค่าใดค่าหนึ่ง
9. ในฟิลด์รหัสบาร์ ให้ป้อนหรือเลือกค่า
10. ในฟิลด์รหัสบาร์ ให้พิมพ์ค่า
    * กดคีย์ Tab  
11. ปิดหน้า
12. ในฟิลด์ ปริมาณ ให้ป้อนตัวเลข
13. คลิก บันทึก
    * เมื่อคุณคลิก บันทึก ระบบจะดำเนินการตรวจสอบบาร์โค้ด ในกรณีนี้ จะแสดงข้อผิดพลาดที่ระบุว่าตัวเลขการตรวจสอบที่คาดไว้คือ 8 แต่พบเป็น 3  ให้ปรับปรุงหมายเลขบาร์โค้ดด้วยตนเองเพื่อให้ 8 อยู่ในตำแหน่งท้ายสุด  
14. ในฟิลด์รหัสบาร์ ให้ป้อนหรือเลือกค่า
15. ในฟิลด์รหัสบาร์ ให้พิมพ์ค่า
    * กดคีย์ Tab  
16. ปิดหน้า
17. คลิก บันทึก
18. ปิดหน้า

