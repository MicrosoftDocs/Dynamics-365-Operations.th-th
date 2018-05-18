---
title: "ภาพรวมของลำดับงาน"
description: "หัวข้อนี้อธิบายถึงระบบลำดับงานใน Microsoft Dynamics 365 for Finance and Operations"
author: sericks007
manager: AnnBe
ms.date: 08/17/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.custom: 56381
ms.assetid: 20b78595-e1d9-439a-ae1c-a776a3438919
ms.search.region: Global
ms.author: tjvass
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: f4e2167290618aaf6ad144e7db8274514078388b
ms.contentlocale: th-th
ms.lasthandoff: 11/03/2017

---

# <a name="workflow-overview"></a>ภาพรวมของลำดับงาน

[!include [banner](../includes/banner.md)]

หัวข้อนี้อธิบายถึงระบบลำดับงานใน Microsoft Dynamics 365 for Finance and Operations

<a name="what-is-workflow"></a>ลำดับงานคืออะไร?
-----------------

คำว่า *ลำดับงาน* สามารถกำหนดได้ในสองวิธี: เป็นระบบ และเป็นกระบวนการทางธุรกิจ
### <a name="workflow-is-a-system"></a>ลำดับงานคือระบบ

Workflow คือ ระบบที่ถูกติดตั้งด้วย Finance and Operations และที่ทำงานบน Application Object Server (AOS) ระบบลำดับงานมีฟังก์ชันที่คุณสามารถใช้สร้างลำดับงานหรือกระบวนการทางธุรกิจแต่ละรายการ

### <a name="workflow-is-a-business-process"></a>Workflow คือ กระบวนการทางธุรกิจ

ลำดับงานแสดงถึงกระบวนการทางธุรกิจ โดยจะกำหนดวิธีการที่เอกสารหมุนเวียนในระบบ และระบุว่าใครต้องทำงานให้เสร็จสมบูรณ์หรืออนุมัติเอกสาร ตัวอย่างเช่น แผนภาพต่อไปนี้แสดงลำดับงานสำหรับรายงานค่าใช้จ่าย 

![ลำดับงานที่มีองค์ประกอบที่กำหนดให้กับผู้ใช้](./media/workflow_user.gif) 

เพื่อให้เข้าใจลำดับงานนี้ได้ดีขึ้น สมมติว่า Sam ส่งรายงานค่าใช้จ่ายที่มีมูลค่า 7,000 เหรียญสหรัฐฯ ในสถานการณ์จำลองนี้ Ivan ต้องตรวจสอบใบเสร็จรับเงินที่ Sam ส่งไปให้ จากนั้น Frank และ Sue ต้องเป็นผู้อนุมัติรายงานค่าใช้จ่าย ตอนนี้ สมมติว่า Sam ส่งรายงานค่าใช้จ่ายจำนวนเงินเป็นจำนวนเงิน 11,000 เหรียญสหรัฐฯ ในสถานการณ์นี้ Ivan ต้องทบทวนการรับสินค้า Frank Sue และ Ann ต้องทำการอนุมัติรายงานค่าใช้จ่าย

## <a name="benefits-of-using-the-workflow-system"></a> ประโยชน์ของการใช้ระบบ Workflow

มีประโยชน์มากมายสำหรับการใช้ระบบลำดับงานในองค์กรของคุณดังเช่นต่อไปนี้
-   **กระบวนการที่สอดคล้องกัน** — คุณสามารถกำหนดกระบวนการอนุมัติสำหรับเอกสารเฉพาะ เช่น ใบขอซื้อและรายงานค่าใช้จ่าย การใช้ระบบลำดับงานช่วยให้แน่ใจว่าเอกสารจะได้รับการประมวลผลและอนุมัติในลักษณะที่สอดคล้องกันและมีประสิทธิภาพ
-   **การติดตามกระบวนการ** — คุณสามารถติดตามสถานะ ประวัติ และเมตริกประสิทธิภาพของอินสแตนซ์ลำดับงานเฉพาะ ซึ่งจะช่วยคุณกำหนดว่าควรทำการเปลี่ยนแปลงกับลำดับงานเพื่อปรับปรุงประสิทธิภาพหรือไม่
-   **รายการงานจากส่วนกลาง** — ผู้ใช้สามารถดูรายการงานจากส่วนกลางเพื่อดูงานในลำดับงานและการอนุมัติที่กำหนดให้กับงานในลำดับงาน


## <a name="workflow-content"></a>บริบทลำดับงาน

+ [สถาปัตยกรรมลำดับงาน](workflow-system-architecture.md)
+ [องค์ประกอบลำดับงาน](workflow-elements.md)
+ [การดำเนินการลำดับงาน](workflow-actions.md)
+ [สร้างลำดับงาน](create-workflow.md)
+ [ตั้งค่าคอนฟิกคุณสมบัติของลำดับงาน](configure-workflow-properties.md)
+ [ตั้งค่าคอนฟิกงานที่กำหนดด้วยตนเองในลำดับงาน](configure-manual-task-workflow.md)
+ [ตั้งค่าคอนฟิกงานอัตโนมัติในลำดับงาน](configure-automated-task-workflow.md)
+ [ตั้งค่าคอนฟิกกระบวนการอนุมัติในลำดับงาน](configure-approval-process-workflow.md)
+ [ตั้งค่าคอนฟิกขั้นตอนการอนุมัติในลำดับงาน](configure-approval-step-workflow.md)
+ [ตั้งค่าคอนฟิกการตัดสินใจด้วยตนเองในลำดับงาน](configure-manual-decision-workflow.md)
+ [ตั้งค่าคอนฟิกการตัดสินใจแบบมีเงื่อนไขในลำดับงาน](configure-conditional-decision-workflow.md)
+ [ตั้งค่าคอนฟิกกิจกรรมคู่ขนานในลำดับงาน](configure-parallel-activity-workflow.md)
+ [ตั้งค่าคอนฟิกสาขาคู่ขนานในลำดับงาน](configure-parallel-branch-workflow.md)
+ [ตั้งค่าคอนฟิกลำดับงานของสินค้าในรายการ](configure-line-item-workflow.md)

