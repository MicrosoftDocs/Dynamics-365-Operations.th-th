---
title: จัดเตรียมกระบวนการงานคัมบังเมื่อวัตถุดิบไม่พร้อมใช้งานสำหรับเซลล์ทำงาน
description: 'ขั้นตอนนี้มุ่งเน้นการจัดเตรียมกระบวนการงานคัมบังเมื่อวัสดุและส่วนประกอบบางรายการไม่พร้อมใช้งานสำหรับเซลล์ทำงาน ดังนั้นจึงจำเป็นต้องเบิกวัสดุจากคลังสินค้า '
author: johanhoffmann
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: KanbanBoardWorkCell
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 2f75cdbc6ce6f7e427bf266c90428d73c065eac3
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 09/29/2021
ms.locfileid: "7576747"
---
# <a name="prepare-a-process-kanban-job-when-materials-are-not-available-for-the-work-cell"></a>จัดเตรียมกระบวนการงานคัมบังเมื่อวัตถุดิบไม่พร้อมใช้งานสำหรับเซลล์ทำงาน

[!include [banner](../../includes/banner.md)]

ขั้นตอนนี้มุ่งเน้นการจัดเตรียมกระบวนการงานคัมบังเมื่อวัสดุและส่วนประกอบบางรายการไม่พร้อมใช้งานสำหรับเซลล์ทำงาน ดังนั้นจึงจำเป็นต้องเบิกวัสดุจากคลังสินค้า  ขั้นตอน "การจัดเตรียมกระบวนการงานคัมบังเมื่อวัตถุดิบมีพร้อมใช้งาน" เป็นข้อกำหนดเบื้องต้นสำหรับการสร้างขั้นตอนนี้  กระบวนงานนี้มีไว้สำหรับพนักงานควบคุมเครื่องจักร ข้อมูลบริษัทสาธิตที่ใช้ในการสร้างกระบวนงานนี้คือ USMF

1. ไปที่การควบคุมการผลิต > คัมบัง > บอร์ดคัมบังสำหรับงานกระบวนการ 
2. ในฟิลด์เซลล์ทำงาน ให้คลิกปุ่มดรอปดาวน์เพื่อเปิดการค้นหา 
3. ในรายการนี้ ให้คลิกลิงค์ในแถวที่เลือก
    * เลือกเซลล์ทำงาน 1250  
4. ในรายการนี้ ให้ค้นหาและเลือกเรกคอร์ดที่ต้องการ
    * เลือกคัมบัง 000356  
5. ในรายการนี้ ให้ค้นหาและเลือกเรกคอร์ดที่ต้องการ
    * ในรายการ ยกเลิกการเลือกแถว 4 หรือเลือกแถว 4 ถ้าคุณยังไม่เสร็จงาน "การเตรียมกระบวนการงานคัมบังเมื่อวัตถุดิบมีพร้อมใช้งาน"  
6. สลับการขยายของส่วนรายการเบิกสินค้า
    * ไอคอนไม่พบรายการอยู่ในสถานะการจัดหาวัสดุแสดงว่า ea 48 ของสินค้า P0002 ไม่มีสำหรับเซลล์ทำงาน  

## <a name="transfer-materials-to-work-cell"></a>โอนย้ายวัสดุไปเซลล์ทำงาน
1. สลับการขยายของส่วนงานการโอนย้าย
2. ใช้ตัวกรองด่วนเพื่อกรองฟิลด์ หมายเลขสินค้าด้วยค่า 'P0002'
3. ในรายการนี้ ให้ค้นหาและเลือกเรกคอร์ดที่ต้องการ
4. คลิก เริ่มต้น
    * การโอนย้ายอยู่ระหว่างดำเนินการ  
5. คลิกเสร็จสมบูรณ์
    * สินค้า P0002 จะพร้อมใช้งานในรายการเบิกสินค้าสำหรับงานคัมบัง  ซึ่งหมายความว่าเราสามารถจัดเตรียมคัมบังกับวัสดุที่จำเป็นทั้งหมด  
6. คลิกจัดเตรียม 
    * โปรดสังเกตว่า ไอคอนในสถานะงานแสดงให้เห็นว่า ขณะนี้งานพร้อม  



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]