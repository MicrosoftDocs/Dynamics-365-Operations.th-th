---
title: สร้างรายการเมนูอุปกรณ์เคลื่อนที่สำหรับการรวมป้ายทะเบียน
description: 'กระบวนงานนี้แสดงวิธีการสร้างรายการเมนูอุปกรณ์เคลื่อนที่สำหรับงานการรวมป้ายทะเบียน '
author: Mirzaab
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: WHSRFMenuItem
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: mirzaab
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 92c971bef440d9f5ba0949b7ba93c1614e998d39
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 09/29/2021
ms.locfileid: "7574100"
---
# <a name="create-a-mobile-device-menu-item-for-license-plate-consolidation"></a>สร้างรายการเมนูอุปกรณ์เคลื่อนที่สำหรับการรวมป้ายทะเบียน

[!include [banner](../../includes/banner.md)]

กระบวนงานนี้แสดงวิธีการสร้างรายการเมนูอุปกรณ์เคลื่อนที่สำหรับงานการรวมป้ายทะเบียน  ซึ่งช่วยให้ผู้ปฏิบัติงานคลังสินค้าสามารถรวมรายการต่างๆ ได้ในป้ายทะเบียนเดียว โดยมีรายการต่างๆ ในป้ายทะเบียนอื่นที่อยู่ในสถานที่เดียวกัน ตัวอย่างเช่น พวกเขาอาจใช้สิ่งนี้ถ้าขั้นตอนการแบ่งระยะถัดไปในใบสั่งงานทั้งสองเหมือนกัน เพื่อให้จำเป็นต้องดำเนินงานเพียงหนึ่งครั้งสำหรับสินค้าผสม คุณสามารถใช้กระบวนงานนี้ในบริษัทข้อมูลสาธิต USMF โดยทั่วไปงานเหล่านี้จะถูกดำเนินการโดยผู้จัดการคลังสินค้า กระบวนงานนี้ใช้สำหรับลักษณะการทำงานที่ถูกเพิ่มใน Dynamics 365 for Operations รุ่น 1611

1. ไปที่การจัดการคลังสินค้า > การตั้งค่า > อุปกรณ์เคลื่อนที่ > รายการเมนูอุปกรณ์เคลื่อนที่
2. คลิก สร้าง
3. ในฟิลด์ชื่อเมนูสินค้า ให้พิมพ์ค่า
4. ในฟิลด์หัวข้อ ให้พิมพ์ค่าใดค่าหนึ่ง
5. ในฟิลด์โหมด เลือก 'ทางอ้อม'
6. ในฟิลด์รหัสกิจกรรม เลือก 'รวมป้ายทะเบียน'



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]