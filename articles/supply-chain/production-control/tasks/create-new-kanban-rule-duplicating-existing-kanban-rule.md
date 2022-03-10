---
title: สร้างกฎคัมบังใหม่โดยทำซ้ำกฎคัมบังที่มีอยู่
description: 'ขั้นตอนนี้มุ่งเน้นการสร้างการทำซ้ำของกฎคัมบังที่มีอยู่ '
author: johanhoffmann
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: KanbanRules, KanbanRuleDuplicate, InventItemIdLookupSimple
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 578ce8bfd5a9ede85670ac0e345f428d705f7914
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 09/29/2021
ms.locfileid: "7575038"
---
# <a name="create-a-new-kanban-rule-by-duplicating-an-existing-kanban-rule"></a>สร้างกฎคัมบังใหม่โดยทำซ้ำกฎคัมบังที่มีอยู่

[!include [banner](../../includes/banner.md)]

ขั้นตอนนี้มุ่งเน้นการสร้างการทำซ้ำของกฎคัมบังที่มีอยู่  สิ่งนี้มีประโยชน์ถ้าคุณต้องการจะสร้างกฎคัมบังใหม่โดยอาศัยกฎคัมบังที่มีอยู่  ข้อมูลบริษัทสาธิตที่ใช้ในการสร้างกระบวนงานนี้คือ USMF ขั้นตอนนี้มีไว้สำหรับวิศวกรกระบวนการหรือผู้จัดการสตรีมค่าตามที่พวกเขาจัดเตรียมการผลิตสำหรับผลิตภัณฑ์ใหม่หรือผลิตภัณฑ์ปรับเปลี่ยน


## <a name="select-a-kanban-rule"></a>เลือกกฎคัมบัง
1. ไปที่กฎคัมบัง
2. ในรายการนี้ ให้ค้นหาและเลือกเรกคอร์ดที่ต้องการ
    * เลือกเหตุการณ์กฎคัมบัง 000017 สำหรับ M0006  

## <a name="duplicate-a-kanban-rule"></a>ทำซ้ำกฎคัมบัง
1. คลิกทำซ้ำกฎคัมบัง
    * เมื่อทำซ้ำกฎคัมบัง เป็นไปได้ที่จะเปลี่ยนชนิด วัน กิจกรรม และการเลือกผลิตภัณฑ์  เปลี่ยนผลิตภัณฑ์สำหรับขั้นตอนนี้ในขั้นตอนถัดไป  
2. ในฟิลด์ผลิตภัณฑ์ ให้ป้อนหรือเลือกค่าใดค่าหนึ่ง
    * เลือก M0007  
3. คลิก ตกลง
    * โปรดทราบว่ามีการสร้างซ้ำของกฎคัมบัง 000017    



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]