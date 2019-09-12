---
title: สร้างเท็มเพลตเรกคอร์ดเพื่อช่วยในการป้อนข้อมูล
description: หัวข้อนี้อธิบายวิธีการสร้างเท็มเพลตเรกคอร์ด เพื่อให้ไม่จำเป็นต้องป้อนค่าในฟิลด์ที่ใช้บ่อยอย่างชัดแจ้งสำหรับเรกคอร์ดใหม่แต่ละรายการ
author: margoc
manager: AnnBe
ms.date: 07/29/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: AssetTable, SysRecordInfo, SysRecordTemplatePromptOnCreate
audience: Application User
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: margoc
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 08ee7d0f0ce7e92eaa85137dcd2761bfd702eb8c
ms.sourcegitcommit: a368682f9cf3897347d155f1a2d4b33e555cc2c4
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 08/08/2019
ms.locfileid: "1866939"
---
# <a name="create-a-record-template-to-facilitate-data-entry"></a>สร้างเท็มเพลตเรกคอร์ดเพื่อช่วยในการป้อนข้อมูล

[!include [task guide banner](../../includes/task-guide-banner.md)]

หัวข้อนี้อธิบายวิธีการสร้างเท็มเพลตเรกคอร์ด เพื่อให้ไม่จำเป็นต้องป้อนค่าในฟิลด์ที่ใช้บ่อยอย่างชัดแจ้งสำหรับเรกคอร์ดใหม่แต่ละรายการ ในกระบวนงานนี้ คุณจะสร้างเรกคอร์ดใหม่สำหรับแล็ปท็อปใหม่ที่ควรถูกเพิ่มในสินทรัพย์ถาวรของคุณ กระบวนงานนี้ใช้บริษัทตัวอย่าง USMF

1. ในบานหน้าต่างนำทาง ไปที่ **โมดูล > สินทรัพย์ถาวร > สินทรัพย์ถาวร > สินทรัพย์ถาวร**
2. เลือก **ใหม่**
3. ในฟิลด์ **กลุ่มสินทรัพย์ถาวร** ให้ป้อนหรือเลือกค่า
4. ในฟิลด์ **ชื่อ** ให้พิมพ์ค่าใดค่าหนึ่ง ตัวอย่างเช่น ป้อน **แล็ปท็อปลูกค้าเป้าหมายองค์กร**  
5. ในฟิลด์ **ชื่อสำหรับค้นหา** ให้พิมพ์ค่าใดค่าหนึ่ง ตัวอย่างเช่น ป้อน **แล็ปท็อป**  
6. ขยายส่วน **ข้อมูลทางเทคนิค**
7. ในฟิลด์ **สร้าง** **แบบจำลอง** และ **ปีแบบจำลอง** ให้พิมพ์ค่า
8. ในบานหน้าต่างการดำเนินการ เลือก **ตัวเลือก**
9. เลือก **ข้อมูลเรกคอร์ด**
10. เลือก **เท็มเพลตผู้ใช้**
11. ในฟิลด์ **ชื่อ** ให้พิมพ์ค่าใดค่าหนึ่ง
12. ในฟิลด์ **คำอธิบาย** ให้พิมพ์ค่าใดค่าหนึ่ง
13. เลือก **ตกลง**
14. เลือก **ปิด**

