---
title: เปลี่ยนกฎคัมบังสำหรับงานในกระบวนการ
description: 'กระบวนงานนี้มุ่งเน้นการเปลี่ยนแปลงกฎคัมบังที่ใช้แล้วสำหรับคัมบังที่กำหนด '
author: johanhoffmann
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: KanbanRules, KanbanRuleDuplicate, KanbanJobSchedulingListPage, LeanRuleReassignmentWizard, KanbanReassignRuleLookup
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 13798e3521efacda896ca88a39faf36ac979d42c
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 09/29/2021
ms.locfileid: "7574508"
---
# <a name="change-kanban-rules-for-a-process-job"></a>เปลี่ยนกฎคัมบังสำหรับงานในกระบวนการ

[!include [banner](../../includes/banner.md)]

กระบวนงานนี้มุ่งเน้นการเปลี่ยนแปลงกฎคัมบังที่ใช้แล้วสำหรับคัมบังที่กำหนด  ซึ่งเป็นประโยชน์ในการตั้งระดับปริมาณระดับทรัพยากรหรือในกรณีของการแบ่ง  ข้อมูลบริษัทสาธิตที่ใช้ในการสร้างกระบวนงานนี้คือ USMF กระบวนงานนี้มีไว้สำหรับนักวางแผนซึ่งทำงานในบริษัทการผลิตแบบ Lean ที่มีความรับผิดชอบต่อสายธารคุณค่า


## <a name="copy-kanban-rule"></a>คัดลอกกฎคัมบัง
1. ไปที่กฎคัมบัง
2. ในรายการนี้ ให้ค้นหาและเลือกเรกคอร์ดที่ต้องการ
    * เลือกเหตุการณ์กฎคัมบัง 000022 สำหรับ L0001  
3. คลิกทำซ้ำกฎคัมบัง
4. คลิก ตกลง

## <a name="change-kanban-rule"></a>เปลี่ยนกฎคัมบัง
1. ปิดหน้า
2. ไปที่การกำหนดงานคัมบัง
3. ในรายการนี้ ให้ทำเครื่องหมายแถวที่เลือก
    * เลือกรายการที่มีคัมบัง 000177  
4. คลิกใช้กฎคัมบังสำรอง
5. คลิก ถัดไป
6. ในฟิลด์กฎคัมบัง ให้ป้อนหรือเลือกค่าใดค่าหนึ่ง
    * เลือกกฎคัมบังที่สร้างไว้ก่อนหน้านี้  นี่คือกฎคัมบังที่มีหมายเลขสูงสุด  
7. คลิก Finish
    * ขณะนี้งานคัมบังกำลังใช้กฎคัมบังอื่นอยู่  ซึ่งสามารถใช้เพื่อตั้งระดับปริมาณเซลล์ทำงาน  



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]