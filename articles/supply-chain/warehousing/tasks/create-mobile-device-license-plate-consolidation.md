--- 
title: "สร้างรายการเมนูอุปกรณ์เคลื่อนที่สำหรับการรวมป้ายทะเบียน"
description: "กระบวนงานนี้แสดงวิธีการสร้างรายการเมนูอุปกรณ์เคลื่อนที่สำหรับงานการรวมป้ายทะเบียน "
author: ShylaThompson
manager: AnnBe
ms.date: 8/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: WHSRFMenuItem
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: mirzaab
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 7b8d20561ff092bd64c17c5d9335e9f54a1d191b
ms.contentlocale: th-th
ms.lasthandoff: 09/29/2017

---
# <a name="create-a-mobile-device-menu-item-for-license-plate-consolidation"></a>สร้างรายการเมนูอุปกรณ์เคลื่อนที่สำหรับการรวมป้ายทะเบียน

[!include [task guide banner](../../includes/task-guide-banner.md)]

กระบวนงานนี้แสดงวิธีการสร้างรายการเมนูอุปกรณ์เคลื่อนที่สำหรับงานการรวมป้ายทะเบียน  ซึ่งช่วยให้ผู้ปฏิบัติงานคลังสินค้าสามารถรวมรายการต่างๆ ได้ในป้ายทะเบียนเดียว โดยมีรายการต่างๆ ในป้ายทะเบียนอื่นที่อยู่ในสถานที่เดียวกัน ตัวอย่างเช่น พวกเขาอาจใช้สิ่งนี้ถ้าขั้นตอนการแบ่งระยะถัดไปในใบสั่งงานทั้งสองเหมือนกัน เพื่อให้จำเป็นต้องดำเนินงานเพียงหนึ่งครั้งสำหรับสินค้าผสม คุณสามารถใช้กระบวนงานนี้ในบริษัทข้อมูลสาธิต USMF โดยทั่วไปงานเหล่านี้จะถูกดำเนินการโดยผู้จัดการคลังสินค้า ขั้นตอนนี้ใช้สำหรับคุณลักษณะที่ถูกเพิ่มเข้ามาใน Dynamics 365 for Operations version 1611

1. ไปที่การจัดการคลังสินค้า > การตั้งค่า > อุปกรณ์เคลื่อนที่ > รายการเมนูอุปกรณ์เคลื่อนที่
2. คลิก สร้าง
3. ในฟิลด์ชื่อเมนูสินค้า ให้พิมพ์ค่า
4. ในฟิลด์หัวข้อ ให้พิมพ์ค่าใดค่าหนึ่ง
5. ในฟิลด์โหมด เลือก 'ทางอ้อม'
6. ในฟิลด์รหัสกิจกรรม เลือก 'รวมป้ายทะเบียน'


