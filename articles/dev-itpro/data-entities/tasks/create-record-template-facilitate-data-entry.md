---
title: สร้างเท็มเพลตเรกคอร์ดเพื่อช่วยในการป้อนข้อมูล
description: กระบวนงานนี้อธิบายวิธีการสร้างเท็มเพลตเรกคอร์ดเพื่อให้ไม่จำเป็นต้องป้อนค่าในฟิลด์ที่ใช้บ่อยอย่างชัดแจ้งสำหรับแต่ละเรกคอร์ดใหม่
author: margoc
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: AssetTable, SysRecordInfo, SysRecordTemplatePromptOnCreate
audience: Application User
ms.reviewer: margoc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: margoc
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 36d14c386322adab0cc0ba9b7b47c874aefbe519
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 05/15/2019
ms.locfileid: "1544263"
---
# <a name="create-a-record-template-to-facilitate-data-entry"></a>สร้างเท็มเพลตเรกคอร์ดเพื่อช่วยในการป้อนข้อมูล

[!include [task guide banner](../../includes/task-guide-banner.md)]

กระบวนงานนี้อธิบายวิธีการสร้างเท็มเพลตเรกคอร์ดเพื่อให้ไม่จำเป็นต้องป้อนค่าในฟิลด์ที่ใช้บ่อยอย่างชัดแจ้งสำหรับแต่ละเรกคอร์ดใหม่ ในกระบวนงานนี้ คุณจะสร้างเรกคอร์ดใหม่สำหรับแล็ปท็อปใหม่ที่ควรถูกเพิ่มในสินทรัพย์ถาวรของคุณ กระบวนงานนี้ใช้บริษัทตัวอย่าง USMF

1. ไปที่ สินทรัพย์ถาวร > สินทรัพย์ถาวร > สินทรัพย์ถาวร
2. คลิก สร้าง
3. ในฟิลด์กลุ่มสินทรัพย์ถาวร ให้ป้อนหรือเลือกค่า
4. ในฟิลด์ชื่อ ให้พิมพ์ค่า 
    * ตัวอย่างเช่น ป้อน 'Corporate lead laptop'  
5. ในฟิลด์ชื่อสำหรับค้นหา ให้พิมพ์ค่าใดค่าหนึ่ง
    * ตัวอย่างเช่น ป้อน 'laptop'  
6. ขยายส่วนข้อมูลทางเทคนิค
7. ในฟิลด์ยี่ห้อ ให้พิมพ์ค่าใดค่าหนึ่ง
8. ในฟิลด์แบบจำลอง ให้พิมพ์ค่าใดค่าหนึ่ง
9. ในฟิลด์ปีของรุ่น ให้พิมพ์ค่าใดค่าหนึ่ง
10. ในบานหน้าต่างการดำเนินการ คลิกที่ตัวเลือก
11. คลิก ข้อมูลของเรกคอร์ด
12. คลิก เท็มเพลตผู้ใช้
13. ในฟิลด์ชื่อ ให้พิมพ์ค่า 
    * ตัวอย่างเช่น ป้อน 'Corporate laptop'  
14. ในฟิลด์ คำอธิบาย ให้พิมพ์ค่า
    * ตัวอย่างเช่น ป้อน 'Corporate laptop'  
15. คลิก ตกลง
16. คลิก ปิด

