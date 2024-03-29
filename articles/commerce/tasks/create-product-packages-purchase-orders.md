---
title: " สร้างบรรจุภัณฑ์ของผลิตภัณฑ์สำหรับใบสั่งซื้อ"
description: 'กระบวนการนี้นำไปสู่การสร้างบรรจุภรรฑ์ของผลิตภัณฑ์ และการใช้บนใบสั่งซื้อ '
author: josaw1
ms.date: 11/14/2017
ms.topic: business-process
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.region: Global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: fb10164be8d7a0828169cf3865f884afaa2e8408472edebe4cb0c7d4db059d8c
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 08/05/2021
ms.locfileid: "6723248"
---
# <a name="create-product-packages-for-purchase-orders"></a> สร้างบรรจุภัณฑ์ของผลิตภัณฑ์สำหรับใบสั่งซื้อ

[!include [banner](../includes/banner.md)]

กระบวนการนี้นำไปสู่การสร้างบรรจุภรรฑ์ของผลิตภัณฑ์ และการใช้บนใบสั่งซื้อ  ใบสั่งซื้อจะถูกใช้เพื่อสร้างใบสั่งสำหรับผลิตภัณฑ์ชุดที่กำหนดไว้ล่วงหน้า  ขั้นตอนนี้ใช้บริษัทข้อมูลสาธิต USRT


## <a name="create-a-product-package"></a>สร้างบรรจุภัณฑ์ของผลิตภัณฑ์
1. ไปยัง การขายปลีกและการค้า > การบริหารสินค้าคงคลัง > การเติมเต็มสินค้า > แพคเกจสินค้า
2. คลิก สร้าง
3. ในฟิลด์หมายเลขบรรจุภรรฑ์ ให้พิมพ์ค่าใดค่าหนึ่ง
4. ในฟิลด์ คำอธิบาย ให้พิมพ์ค่า
5. ในฟิลด์บัญชีผู้จัดจำหน่าย ให้คลิกปุ่มดรอปดาวน์เพื่อเปิดการค้นหา
6. ในรายการนี้ ให้คลิกลิงค์ในแถวที่เลือก
7. คลิก เพิ่ม
8. ในฟิลด์หมายเลขสินค้า ให้พิมพ์ '0160'
9. ในฟิลด์ขนาด ให้คลิกปุ่มดรอปดาวน์เพื่อเปิดการค้นหา
10. ในรายการนี้ ให้คลิกลิงค์ในแถวที่เลือก
11. ในฟิลด์ ปริมาณ ให้ป้อนตัวเลข
12. คลิก เพิ่ม
13. ในฟิลด์หมายเลขสินค้า ให้พิมพ์ '0160'
14. ในฟิลด์หมายเลขตัวแปร ให้คลิกปุ่มดรอปดาวน์เพื่อเปิดการค้นหา
15. ในรายการนี้ ให้คลิกลิงค์ในแถวที่เลือก
16. ในฟิลด์ ปริมาณ ให้ป้อนตัวเลข
17. คลิก เพิ่ม
18. ในฟิลด์หมายเลขสินค้า ให้พิมพ์ '0175'
19. ในฟิลด์ ปริมาณ ให้ป้อนตัวเลข
20. คลิก บันทึก
21. ปิดหน้า

## <a name="add-package-to-purchase-order"></a>เพิ่มแพคเกจในใบสั่งซื้อ
1. ไปที่บัญชีเจ้าหนี้ > ใบสั่งซื้อ > ใบสั่งซื้อทั้งหมด
2. คลิก สร้าง
3. ในฟิลด์บัญชีผู้จัดจำหน่าย ให้คลิกปุ่มดรอปดาวน์เพื่อเปิดการค้นหา
4. ในรายการ ให้เลือกผู้จัดจำหน่ายเดียวกันกับที่บรรจุภัณฑ์ของผลิตภัณฑ์ถูกสร้างไว้ให้ก่อนหน้านี้ ถ้าผู้จัดจำหน่ายถูกเลือก
5. เปิดปิดการขยายของส่วนทั่วไป
6. ในฟิลด์ไซต์ ให้คลิกปุ่มดรอปดาวน์เพื่อเปิดการค้นหา
7. ในรายการนี้ ให้คลิกลิงค์ในแถวที่เลือก
8. ในฟิลด์คลังสินค้า ให้คลิกปุ่มดรอปดาวน์เพื่อเปิดการค้นหา
9. ในรายการนี้ ให้คลิกลิงค์ในแถวที่เลือก
10. คลิก ตกลง ระบบจะนำเข้าข้อมูลการชำระเงิน
11. สลับการขยายของส่วนรายละเอียดรายการ
12. คลิกที่แท็บบรรจุภัณฑ์ของผลิตภัณฑ์
13. คลิก บรรทัดรายการใบสั่งซื้อ
14. คลิก สร้างบรรทัดรายการจากบรรจุภัณฑ์
15. ในรายการ ค้นหาและเลือกบรรจุภรรฑ์ของผลิตภัณฑ์ที่สร้างขึ้นในขั้นตอนก่อนหน้านี้
16. ในฟิลด์ปริมาณ ให้ป้อนตัวเลข
17. คลิก สร้าง
18. คลิก บันทึก



[!INCLUDE[footer-include](../../includes/footer-banner.md)]