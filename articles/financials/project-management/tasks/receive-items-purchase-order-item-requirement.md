--- 
title: "รับสินค้าในใบสั่งซื้อจากความต้องการสินค้า"
description: "กระบวนงานนี้แสดงวิธีการรับสินค้าในใบสั่งซื้อจากความต้องการสินค้า"
author: KimANelson
manager: AnnBe
ms.date: 8/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: ProjProjectsListPage, ProjTable, ProjSalesItemReq, InventItemIdLookupSimple, PurchCreateFromSalesOrder, VendAccountItemLookup, PurchTable, PurchEditLines
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: knelson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: f827b4787506cfdec8b9a91c4a68f3293190158a
ms.openlocfilehash: 0fa70da5e06d1bc82fb9d2419bb0a7c8dd0da467
ms.contentlocale: th-th
ms.lasthandoff: 09/29/2017

---
# <a name="receive-items-on-purchase-order-from-item-requirement"></a>รับสินค้าในใบสั่งซื้อจากความต้องการสินค้า

[!include [task guide banner](../../includes/task-guide-banner.md)]

กระบวนงานนี้แสดงวิธีการรับสินค้าในใบสั่งซื้อจากความต้องการสินค้า

โดยการใช้ข้อกำหนดรายการแทนธุรกรรมรายการ คุณสามารถวางแผนให้กับการส่งมอบก่อนการใช้รายการจริง สร้างใบสั่งซื้อ รวมรายการในโครงงานข้อตกลงการค้า และรวมในข้อกำหนดรายการในการวางแผนการผลิต 

งานนี้ใช้ชุดข้อมูล USSI

1. ไปที่การจัดการโครงการและการบัญชี > โครงการ > โครงการทั้งหมด
2. ในรายการนี้ ให้คลิกลิงค์ในแถวที่เลือก
3. ในบานหน้าต่างการดำเนินการ ให้คลิก วางแผน
4. คลิก ความต้องการสินค้า
5. คลิก สร้าง
6. ในรายการนี้ ให้ทำเครื่องหมายแถวที่เลือก
7. ในฟิลด์หมายเลขสินค้า ให้ป้อนหรือเลือกค่า
8. ในฟิลด์ ปริมาณ ให้ป้อนตัวเลข
9. คลิก บันทึก
10. ในบานหน้าต่างการดำเนินการ คลิก จัดการ
11. คลิกฟังก์ชัน
12. คลิก สร้างใบสั่งซื้อ
13. เลือกกล่องกาเครื่องหมาย รวม
14. ในฟิลด์บัญชีผู้จัดจำหน่าย ให้ป้อนหรือเลือกค่า
15. คลิก ตกลง
16. ไปที่บัญชีเจ้าหนี้ > ใบสั่งซื้อ > ใบสั่งซื้อทั้งหมด
17. ในรายการนี้ ให้คลิกลิงค์ในแถวที่เลือก
18. ในบานหน้าต่างการดำเนินการ ให้คลิก ซื้อ
19. คลิก ยืนยัน
20. ในบานหน้าต่างการดำเนินการ ให้คลิก รับ
21. คลิก ใบรับสินค้า
22. ในรายการนี้ ให้ทำเครื่องหมายแถวที่เลือก
23. ในฟิลด์ใบรับสินค้า ให้พิมพ์ค่า
24. คลิก ตกลง


