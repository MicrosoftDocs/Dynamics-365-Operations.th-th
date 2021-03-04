---
title: อนุมัติผู้จัดจำหน่ายสำหรับประเภทการจัดซื้อเฉพาะ
description: หัวข้อนี้จะอธิบายถึงวิธีการอนุมัติผู้จัดจำหน่ายสำหรับประเภทการจัดซื้อที่เฉพาะเจาะจงใน Dynamics 365 Supply Chain Management
author: mkirknel
manager: tfehr
ms.date: 07/30/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: VendTable, DirPartyEcoResCategory, EcoResCategorySingleLookup, ProcCategoryHierarchyManagement
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: e53102d732e9befcaca183adfd2a756c12e0162b
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 10/13/2020
ms.locfileid: "4438428"
---
# <a name="approve-vendors-for-specific-procurement-categories"></a>อนุมัติผู้จัดจำหน่ายสำหรับประเภทการจัดซื้อเฉพาะ

[!include [banner](../../includes/banner.md)]

หัวข้อนี้จะอธิบายถึงวิธีการอนุมัติผู้จัดจำหน่ายสำหรับประเภทการจัดซื้อที่เฉพาะเจาะจงใน Dynamics 365 Supply Chain Management เมื่อมีการสร้างใบสั่งซื้อ อาจจำเป็นต้องเลือกผู้จัดจำหน่ายที่ได้รับอนุมัติหรือที่ต้องการ โดยขึ้นอยู่กับวิธีตั้งค่านโยบายการจัดซื้อ  กระบวนงานนี้แสดงวิธีการระบุว่าผู้จัดจำหน่ายได้รับอนุมัติหรือเป็นที่ต้องการสำหรับประเภทการจัดซื้อเฉพาะ งานนี้อาจมักจะถูกดำเนินการโดยผู้เชี่ยวชาญด้านการจัดซื้อจัดหา คุณสามารถใช้กระบวนงานนี้ในบริษัทข้อมูลสาธิต USMF

1. ในบานหน้าต่างการนำทาง ไปที่ **โมดูล > การจัดซื้อและการจัดหา > ผู้จัดจำหน่าย > ผู้จัดจำหน่ายทั้งหมด**
2. เลือกผู้จัดจำหน่ายที่คุณต้องการเพื่อกำหนดเป็นผู้จัดจำหน่ายที่ต้องการหรือได้รับอนุมัติสำหรับประเภท
3. ในบานหน้าต่างการดำเนินการ เลือก **ทั่วไป**
4. เลือก **ประเภท**
5. เลือก **เพิ่มประเภท**
6. ในฟิลด์ **ประเภท** เลือก **OFFICE AND DESK ACCESSORIES (OFFICE AND DESK ACCESSORIES)**
7. ในฟิลด์ **สถานะประเภทผู้จัดจำหน่าย** เลือก **เป็นที่ต้องการ** สามารถระบุผู้จัดจำหน่ายที่ต้องการได้มากกว่าหนี่งรายสำหรับหนึ่งประเภท  
8. เลือก **บันทึก**
9. ในบานหน้าต่างนำทาง ไปที่ **โมดูล > การจัดซื้อและการจัดหา > แค็ตตาล็อกการจัดซื้อ**
10. ในแผนภูมิ เลือก **CORP PROCUREMENT CATEGORIES\OFFICE AND DESK ACCESSORIES**
11. ขยายส่วน **ผู้จัดจำหน่าย** ตรวจสอบว่าผู้จัดจำหน่ายที่คุณเลือกปรากฏเป็นผู้จัดจำหน่ายที่ต้องการสำหรับประเภทสำนักงานและโต๊ะเบ็ดเตล็ดหรือไม่ ถ้าคุณกำลังรันกระบวนงานนี้เป็นคู่มืองาน คุณอาจต้องเลือกปุ่ม **ปลดล็อก** เพื่อให้สามารถเลื่อนลงไปยังรายการของผู้จัดจำหน่าย  นอกจากนี้ ยังสามารถเพิ่มผู้จัดจำหน่ายที่ต้องการและผู้จัดจำหน่ายที่ได้รับอนุมัติในหน้านี้อีกด้วย  
12. ในแผนภูมิ ให้ขยาย **OFFICE AND DESK ACCESSORIES** และเลือก **กรรไกร**
13. เลือก **ไม่** ในฟิลด์ **สืบทอดผู้จัดจำหน่ายจากประเภทหลัก:**
14. เลือก **ใช่** ในฟิลด์ **สืบทอดผู้จัดจำหน่ายจากประเภทหลัก:**



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]