---
title: เปลี่ยนกฎคัมบังสำหรับงานในกระบวนการ
description: 'กระบวนงานนี้มุ่งเน้นการเปลี่ยนแปลงกฎคัมบังที่ใช้แล้วสำหรับคัมบังที่กำหนด '
author: ChristianRytt
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: KanbanRules, KanbanRuleDuplicate, KanbanJobSchedulingListPage, LeanRuleReassignmentWizard, KanbanReassignRuleLookup
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: c036f6aad79e33df6009913d1e21ff6176f22593
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 08/01/2019
ms.locfileid: "1843804"
---
# <a name="change-kanban-rules-for-a-process-job"></a>เปลี่ยนกฎคัมบังสำหรับงานในกระบวนการ

[!include [task guide banner](../../includes/task-guide-banner.md)]

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

