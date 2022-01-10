---
title: บานหน้าต่างตัวกรองในหน้ารายการคงเหลือไม่ทำงานตามที่คาดไว้
description: ตัวกรองในบานหน้าต่างตัวกรองในหน้า "รายการคงเหลือ" ไม่ได้กรองข้อมูลผลลัพธ์ตามที่คุณคาดไว้
author: sherry-zheng
ms.date: 05/31/2021
ms.topic: troubleshooting
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: chuzheng
ms.search.validFrom: 2021-05-31
ms.dyn365.ops.version: 10.0.16
ms.openlocfilehash: 2b2b233e22378c8710a63dce83d168bfd89eba7f
ms.sourcegitcommit: 008779c530798f563fe216810d34b2d56f2c8d3c
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 12/14/2021
ms.locfileid: "7920509"
---
# <a name="the-filter-pane-on-the-on-hand-list-page-doesnt-work-as-expected"></a>บานหน้าต่างตัวกรองในหน้ารายการคงเหลือไม่ทำงานตามที่คาดไว้

## <a name="symptoms"></a>อาการ

ตัวกรองในบานหน้าต่างตัวกรองในหน้า **รายการคงเหลือ** ไม่ได้กรองข้อมูลผลลัพธ์ตามที่คุณคาดไว้

## <a name="resolution"></a>การแก้ปัญหา

หน้า **รายการปริมาณคงคลังคงเหลือ** ประกอบด้วยตารางปริมาณคงคลังคงเหลือที่มีรายละเอียด ซึ่งรวมมิติที่มีอยู่ทั้งหมด อย่างไรก็ตาม รายการบนหน้านี้เป็นข้อมูลสรุป ดังนั้น จึงอาจรวมแถวจากตารางต้นทางตามค่ารวมตามมิติที่แสดง

ตัวกรองที่ตั้งค่าบานหน้าต่างตัวกรองจะนำไปใช้กับตารางต้นทาง ไม่ใช่รายการที่รวม ในบางครั้ง ลักษณะการดําเนินการนี้สามารถให้ผลลัพธ์ที่ไม่คาดคิดได้ ดังที่แสดงใน [ตัวอย่างเหล่านี้](/dynamics365/supply-chain/inventory/inventory-on-hand-list.md#examples)

อย่างไรก็ตาม [ตัวกรองที่ระบุไว้ในกริด](/dynamics365/supply-chain/inventory/inventory-on-hand-list.md#grid-filters) *จะถูก* ใช้กับรายการแบบรวม ตัวกรองเหล่านี้รวมทั้ง QuickFilter ที่ด้านบนของกริด และตัวกรองสำหรับแต่ละส่วนหัวของคอลัมน์
