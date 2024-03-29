---
title: " สร้างค่ามิติทางการเงินสำหรับเครื่องบันทึกเงินสด POS และตั้งค่าคอนฟิกค่ามิติบนเครื่องบันทึกเงินสด"
description: 'กระบวนการนี้นำไปสู่การสร้างมิติทางการเงินสำหรับการลงทะเบียนการขายหน้าร้าน (POS) และแสดงวิธีการตั้งค่าคอนฟิกค่ามิติทางการเงินบนเครื่องบันทึกเงินสด '
author: jashanno
ms.date: 11/14/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.region: Global
ms.search.industry: Retail
ms.author: jashanno
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: e85756a2b7cdd3627c7a3fffa8dc97e0db13641a
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 06/03/2022
ms.locfileid: "8884801"
---
# <a name="create-financial-dimensions-for-pos-registers-and-configure-dimension-values-on-registers"></a> สร้างค่ามิติทางการเงินสำหรับเครื่องบันทึกเงินสด POS และตั้งค่าคอนฟิกค่ามิติบนเครื่องบันทึกเงินสด

[!include [banner](../includes/banner.md)]

กระบวนการนี้นำไปสู่การสร้างมิติทางการเงินสำหรับการลงทะเบียนการขายหน้าร้าน (POS) และแสดงวิธีการตั้งค่าคอนฟิกค่ามิติทางการเงินบนเครื่องบันทึกเงินสด  กระบวนงานนี้ไม่รวมขั้นตอนที่เกี่ยวข้องอื่นๆ เช่น การสร้างชุดมิติและโครงสร้างทางบัญชี งานเหล่านั้นจะถูกพบได้ในบทความอื่นๆ บันทึกนี้ใช้บริษัทสาธิต USRT

1. ไปที่บัญชีแยกประเภททั่วไป > ผังบัญชี > มิติ > มิติทางการเงิน
2. คลิก สร้าง
3. ในฟิลด์ ใช้ค่าจาก เลือกตัวเลือก
4. ในฟิลด์ชื่อมิติ ให้พิมพ์ค่าใดค่าหนึ่ง
5. คลิกเรียกใช้
6. คลิก ปิด
7. คลิกเรียกใช้
8. คลิกค่ามิติ
9. ปิดหน้า
10. คลิก บันทึก
11. ปิดหน้า
12. ไปยัง Retail และ Commerce > การตั้งค่าช่องทาง > การตั้งค่า POS > การลงทะเบียน
13. ในรายการนี้ ให้ค้นหาและเลือกเรกคอร์ดที่ต้องการ
14. สลับการขยายของส่วนมิติการเงิน
15. คลิกแก้ไข
16. ในฟิลด์ เทอร์มินัล คลิกปุ่มดรอปดาวน์เพื่อเปิดการค้นหา
17. ในรายการ ให้ค้นหาและเลือกค่ามิติสำหรับการลงทะเบียนที่กำลังถูกอัพเดต
18. คลิก บันทึก



[!INCLUDE[footer-include](../../includes/footer-banner.md)]