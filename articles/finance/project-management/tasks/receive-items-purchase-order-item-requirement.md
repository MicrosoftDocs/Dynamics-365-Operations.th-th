---
title: รับสินค้าในใบสั่งซื้อจากความต้องการสินค้า
description: หัวข้อนี้อธิบายวิธีการรับสินค้าในใบสั่งซื้อจากความต้องการสินค้า
author: KimANelson
manager: AnnBe
ms.date: 08/06/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProjProjectsListPage, ProjTable, ProjSalesItemReq, InventItemIdLookupSimple, PurchCreateFromSalesOrder, VendAccountItemLookup, PurchTable, PurchEditLines
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: knelson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 7afdae65c5ae7e3196c6b9f142dd87aec39b5ea3
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 09/27/2019
ms.locfileid: "2174431"
---
# <a name="receive-items-on-purchase-order-from-item-requirement"></a>รับสินค้าในใบสั่งซื้อจากความต้องการสินค้า

[!include [task guide banner](../../includes/task-guide-banner.md)]

หัวข้อนี้อธิบายวิธีการรับสินค้าในใบสั่งซื้อจากความต้องการสินค้า

โดยการใช้ข้อกำหนดรายการแทนธุรกรรมรายการ คุณสามารถวางแผนให้กับการส่งมอบก่อนการใช้รายการจริง สร้างใบสั่งซื้อ รวมรายการในโครงงานข้อตกลงการค้า และรวมในข้อกำหนดรายการในการวางแผนการผลิต 

งานนี้ใช้ชุดข้อมูล USSI

1. ในบานหน้าต่างนำทาง ให้ไปที่ **โมดูล > การจัดการโครงการและการบัญชี > โครงการ > โครงการทั้งหมด**
2. ในรายการ ให้เลือกลิงค์ในแถวที่ต้องการ
3. บนบานหน้าต่างการดำเนินการ เลือก **วางแผน**
4. เลือก **ข้อกำหนดสินค้า**
5. เลือก **ใหม่**
6. ในแถวใหม่ ป้อนหรือเลือกค่าในฟิลด์ **หมายเลขสินค้า**
7. ในฟิลด์ **ปริมาณ** ให้ป้อนตัวเลข
8. เลือก **บันทึก**
9. ในบานหน้าต่างการดำเนินการ เลือก **จัดการ**
10. เลือก **ฟังก์ชัน**
11. เลือก **สร้างใบสั่งซื้อ**
12. เลือกกล่องกาเครื่องหมาย **รวมทั้งหมด**
13. ในฟิลด์ **บัญชีผู้จัดจำหน่าย** ให้ป้อนหรือเลือกค่าใดค่าหนึ่ง
14. เลือก **ตกลง**
15. ในบานหน้าต่างนำทาง ไปที่ **โมดูล > บัญชีเจ้าหนี้ > ใบสั่งซื้อ > ใบสั่งซื้อทั้งหมด**
16. ในรายการ ให้เลือกลิงค์ในแถวที่ต้องการ
17. บนบานหน้าต่างการดำเนินการ เลือก **ซื้อ**
18. เลือก **ยืนยัน**
19. ในบานหน้าต่างการดำเนินการ เลือก **รับ**
20. เลือก **ใบรับสินค้า**
21. ในฟิลด์ **ใบรับสินค้า** ให้พิมพ์ค่า
22. เลือก **ตกลง**

