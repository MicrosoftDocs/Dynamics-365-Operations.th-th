---
title: คำนวณ BOM โดยใช้โครงสร้างระดับเดียว (กุมภาพันธ์ 2016)
description: กระบวนงานนี้แสดงวิธีการคำนวณต้นทุนของผลิตภัณฑ์สำเร็จรูปโดยใช้การกระจายระดับเดียวจากในแผ่นงานการคิดต้นทุน
author: ShylaThompson
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: EcoResProductDetailsExtended, InventItemPrice, BOMCalcDialog
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 22ed277d6f4dca3ab0a5be4ddba8982350c7e05ccbb6ade7313ac22b45fbecb1
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 08/05/2021
ms.locfileid: "6772555"
---
# <a name="calculate-a-bom-by-using-a-single-level-structure-february-2016"></a>คำนวณ BOM โดยใช้โครงสร้างระดับเดียว (กุมภาพันธ์ 2016)

[!include [banner](../../includes/banner.md)]

กระบวนงานนี้แสดงวิธีการคำนวณต้นทุนของผลิตภัณฑ์สำเร็จรูปโดยใช้การกระจายระดับเดียวจากในแผ่นงานการคิดต้นทุน นี่คืองานที่หกในลำดับการคำนวณ BOM ข้อมูลสาธิตของบริษัทที่ใช้ในการสร้างงานนี้คือ USMF

1. ไปที่ผลิตภัณฑ์ที่จะนำออกใช้
2. ในรายการนี้ ให้ค้นหาและเลือกเรกคอร์ดที่ต้องการ
    * เลือก ผลิตภัณฑ์ BOM_1  
3. ในบานหน้าต่างการดำเนินการ คลิกการจัดการต้นทุน
4. คลิก ราคาสินค้า
5. คลิก คำนวณต้นทุนสินค้า
    * คุณอาจต้องคลิกจุดไข่ปลา (...) เพื่อดูตัวเลือกนี้ในเมนูด้านบน  
6. ในฟิลด์เวอร์ชันการคิดต้นทุน ให้คลิกปุ่มดรอปดาวน์เพื่อเปิดการค้นหา
    * สำหรับการสาธิตนี้ ให้เลือก 10 นี่คือเวอร์ชันการคิดต้นทุนเดียวกันซึ่งใช้สำหรับการเพิ่มราคาต้นทุนไปยังส่วนประกอบ  
7. คลิก ตกลง
8. คลิกดูรายละเอียดการคำนวณ
    * คุณอาจต้องคลิกจุดไข่ปลา (...) เพื่อดูตัวเลือกนี้ในเมนูด้านบน    นี่คือส่วนประกอบของต้นทุน:  *    10 ได้รับมาจาก ITEM_A 10 จาก ITEM_B 10 จาก BOM_2 ในกรณีนี้ ไม่มีรายละเอียดสำหรับ BOM_2 เนื่องจากมีการป้อนเป็นต้นทุนมาตรฐานของ 10 แต่ไม่ได้ดำเนินการโดยใช้การคำนวณ  *    7 ได้รับมาจากเวลาเซ็ตอัพ ซึ่งเป็นต้นทุนคงที่ และอีก 7 ได้รับมาจากการดำเนินงานเวลาที่ใช้ในการผลิต (กระบวนการ)  *    นอกจากนี้ยังมียอดเงินอื่นๆ ที่เกี่ยวข้องกับต้นทุนทางอ้อม  
9. @SysTaskRecorder:_RequestClose



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]