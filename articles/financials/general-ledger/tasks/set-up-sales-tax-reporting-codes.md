---
title: ตั้งค่ารหัสการรายงานภาษีขาย
description: รหัสการรายงานภาษีขายอ้างอิงหมายเลขของฟิลด์ในรายงานภาษีขาย l
author: twheeloc
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TaxReportCollection
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: vstehman
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 4543cf7eaa0b1ef8e32d3fdafa2c354cd3739256
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 05/15/2019
ms.locfileid: "1554238"
---
# <a name="set-up-sales-tax-reporting-codes"></a>ตั้งค่ารหัสการรายงานภาษีขาย

[!include [task guide banner](../../includes/task-guide-banner.md)]

รหัสการรายงานภาษีขายอ้างอิงหมายเลขของฟิลด์ในรายงานภาษีขาย l รหัสนี้จะใช้โครงร่างรายงานเฉพาะประเทศและการชำระภาษีขายตามรหัสการรายงาน เพื่อพิมพ์ยอดเงินภาษีขายสำหรับรอบระยะเวลาการชำระเงินที่มีการสรุปสำหรับแต่ละรหัสการรายงาน  หลังจากที่คุณสร้างรหัสการรายงานภาษีขาย คุณสามารถอ้างอิงรหัสนี้กับแท็บด่วนการตั้งค่ารายงานในหน้ารหัสภาษีขาย  

บันทึกนี้ใช้บริษัทสาธิต DEMF 



1. ไปที่ ภาษี > การตั้งค่า > ภาษีขาย > รหัสการรายงานภาษีขาย
2. คลิก สร้าง
3. เลือกโครงร่างรายงานที่เป็นของรหัสการรายงาน
    * โครงร่างนี้จะใช้เพื่อกรองข้อมูลรหัสการรายงานที่พร้อมใช้งานสำหรับรหัสภาษีขาย  แต่ละรหัสภาษีขายนั้นเป็นของรอบระยะเวลาการชำระซึ่งเป็นของหน่วยงานจัดเก็บภาษีขายซึ่งใช้โครงร่างรายงาน  
4. ป้อนหมายเลขฟิลด์ที่อ้างถึงฟิลด์ในรายงานภาษีขาย
5. ในฟิลด์ข้อความในรายงาน ให้ป้อนคำอธิบายที่จะแสดงในรายงาน
6. ในฟิลด์คำอธิบายย่อ ให้ป้อนคำอธิบายสำหรับจุดประสงค์ภายใน
7. คลิก บันทึก

