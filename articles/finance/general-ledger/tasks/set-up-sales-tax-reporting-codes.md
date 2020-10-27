---
title: ตั้งค่ารหัสการรายงานภาษีขาย
description: รหัสการรายงานภาษีขายอ้างอิงหมายเลขของฟิลด์ในรายงานภาษีขาย l
author: twheeloc
manager: AnnBe
ms.date: 08/08/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TaxReportCollection
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 6c18f4fb0db31a959647bb10d2b99d940646676e
ms.sourcegitcommit: 708ca25687a4e48271cdcd6d2d22d99fb94cf140
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 10/10/2020
ms.locfileid: "3976804"
---
# <a name="set-up-sales-tax-reporting-codes"></a>ตั้งค่ารหัสการรายงานภาษีขาย

[!include [banner](../../includes/banner.md)]

รหัสการรายงานภาษีขายอ้างอิงหมายเลขของฟิลด์ในรายงานภาษีขาย l รหัสนี้จะใช้โครงร่างรายงานเฉพาะประเทศและการชำระภาษีขายตามรหัสการรายงาน เพื่อพิมพ์ยอดเงินภาษีขายสำหรับรอบระยะเวลาการชำระเงินที่มีการสรุปสำหรับแต่ละรหัสการรายงาน  หลังจากที่คุณสร้างรหัสการรายงานภาษีขาย คุณสามารถอ้างอิงรหัสนี้กับแท็บด่วนการตั้งค่ารายงานในหน้ารหัสภาษีขาย  

บันทึกนี้ใช้บริษัทสาธิต DEMF 

1. ใน **บานหน้าต่างนำทาง** ไปที่ **ภาษี > การตั้งค่า > ภาษีขาย > รหัสการรายงานภาษีขาย**
2. คลิก **สร้าง**
3. เลือกโครงร่างรายงานที่เป็นของรหัสการรายงาน โครงร่างนี้จะใช้เพื่อกรองข้อมูลรหัสการรายงานที่พร้อมใช้งานสำหรับรหัสภาษีขาย  แต่ละรหัสภาษีขายนั้นเป็นของรอบระยะเวลาการชำระซึ่งเป็นของหน่วยงานจัดเก็บภาษีขายซึ่งใช้โครงร่างรายงาน  
4. ในฟิลด์ **รหัสการรายงาน** ให้ป้อนตัวเลข
5. ในฟิลด์ **ข้อความในรายงาน** ให้ป้อนคำอธิบายที่จะแสดงในรายงาน
6. ในฟิลด์ **คำอธิบายย่อ** ให้ป้อนคำอธิบายสำหรับจุดประสงค์ภายใน
7. คลิก **บันทึก**

