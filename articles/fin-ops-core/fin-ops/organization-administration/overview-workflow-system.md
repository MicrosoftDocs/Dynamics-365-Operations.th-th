---
title: ภาพรวมของระบบลำดับงาน
description: หัวข้อนี้อธิบายระบบลำดับงาน
author: ChrisGarty
ms.date: 07/25/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: sericks
ms.custom:
- "56381"
- intro-internal
ms.assetid: 20b78595-e1d9-439a-ae1c-a776a3438919
ms.search.region: Global
ms.author: cgarty
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: dc73f1bde3407c144dc1cd48283385c19713430e
ms.sourcegitcommit: c08a9d19eed1df03f32442ddb65a2adf1473d3b6
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 07/06/2021
ms.locfileid: "6349095"
---
# <a name="workflow-system-overview"></a>ภาพรวมของระบบลำดับงาน

[!include [banner](../includes/banner.md)]

หัวข้อนี้อธิบายระบบลำดับงาน

## <a name="what-is-workflow"></a>ลำดับงานคืออะไร?

คำว่า *ลำดับงาน* สามารถกำหนดได้ในสองวิธี: เป็นระบบ และเป็นกระบวนการทางธุรกิจ

### <a name="workflow-is-a-system"></a>ลำดับงานคือระบบ

การลำดับงานคือระบบที่ปฏิบัติการบน Application Object Server (AOS) ระบบลำดับงานมีฟังก์ชันที่คุณสามารถใช้สร้างลำดับงานหรือกระบวนการทางธุรกิจแต่ละรายการ

### <a name="workflow-is-a-business-process"></a>Workflow คือ กระบวนการทางธุรกิจ

ลำดับงานแสดงถึงกระบวนการทางธุรกิจ โดยจะกำหนดวิธีการที่เอกสารหมุนเวียนในระบบ และระบุว่าใครต้องทำงานให้เสร็จสมบูรณ์หรืออนุมัติเอกสาร ตัวอย่างเช่น แผนภาพต่อไปนี้แสดงลำดับงานสำหรับรายงานค่าใช้จ่าย

![ลำดับงานที่มีองค์ประกอบที่กำหนดให้กับผู้ใช้](./media/workflow_user.gif)

เพื่อให้เข้าใจลำดับงานนี้ได้ดีขึ้น สมมติว่า Sam ส่งรายงานค่าใช้จ่ายที่มีมูลค่า 7,000 เหรียญสหรัฐฯ ในสถานการณ์จำลองนี้ Ivan ต้องตรวจสอบใบเสร็จรับเงินที่ Sam ส่งไปให้ จากนั้น Frank และ Sue ต้องเป็นผู้อนุมัติรายงานค่าใช้จ่าย ตอนนี้ สมมติว่า Sam ส่งรายงานค่าใช้จ่ายจำนวนเงินเป็นจำนวนเงิน 11,000 เหรียญสหรัฐฯ ในสถานการณ์นี้ Ivan ต้องทบทวนการรับสินค้า Frank Sue และ Ann ต้องทำการอนุมัติรายงานค่าใช้จ่าย

## <a name="benefits-of-using-the-workflow-system"></a> ประโยชน์ของการใช้ระบบ Workflow

มีประโยชน์มากมายสำหรับการใช้ระบบลำดับงานในองค์กรของคุณดังเช่นต่อไปนี้

- **กระบวนการที่สอดคล้องกัน** — คุณสามารถกำหนดกระบวนการอนุมัติสำหรับเอกสารเฉพาะ เช่น ใบขอซื้อและรายงานค่าใช้จ่าย การใช้ระบบลำดับงานช่วยให้แน่ใจว่าเอกสารจะได้รับการประมวลผลและอนุมัติในลักษณะที่สอดคล้องกันและมีประสิทธิภาพ
- **การติดตามกระบวนการ** — คุณสามารถติดตามสถานะ ประวัติ และเมตริกประสิทธิภาพของอินสแตนซ์ลำดับงานเฉพาะ ซึ่งจะช่วยคุณกำหนดว่าควรทำการเปลี่ยนแปลงกับลำดับงานเพื่อปรับปรุงประสิทธิภาพหรือไม่
- **รายการงานจากส่วนกลาง** — ผู้ใช้สามารถดูรายการงานจากส่วนกลางเพื่อดูงานในลำดับงานและการอนุมัติที่กำหนดให้กับงานในลำดับงาน


## <a name="workflow-content"></a>บริบทลำดับงาน

+ [สถาปัตยกรรมระบบลำดับงาน](workflow-system-architecture.md)
+ [องค์ประกอบลำดับงาน](workflow-elements.md)
+ [การดำเนินการในกระบวนการอนุมัติในลำดับงาน](workflow-actions.md)
+ [ภาพรวมของการสร้างลำดับงาน](create-workflow.md)
+ [ตั้งค่าคอนฟิกคุณสมบัติของลำดับงาน](configure-workflow-properties.md)
+ [ตั้งค่าคอนฟิกงานแบบกำหนดเองในลำดับงาน](configure-manual-task-workflow.md)
+ [ตั้งค่าคอนฟิกงานอัตโนมัติในลำดับงาน](configure-automated-task-workflow.md)
+ [ตั้งค่าคอนฟิกกระบวนการอนุมัติในลำดับงาน](configure-approval-process-workflow.md)
+ [ตั้งค่าคอนฟิกขั้นตอนการอนุมัติในลำดับงาน](configure-approval-step-workflow.md)
+ [ตั้งค่าคอนฟิกการตัดสินใจด้วยตนเองในลำดับงาน](configure-manual-decision-workflow.md)
+ [ตั้งค่าคอนฟิกการตัดสินใจแบบมีเงื่อนไขในลำดับงาน](configure-conditional-decision-workflow.md)
+ [ตั้งค่าคอนฟิกกิจกรรมคู่ขนานในลำดับงาน](configure-parallel-activity-workflow.md)
+ [ตั้งค่าคอนฟิกสาขาคู่ขนานในลำดับงาน](configure-parallel-branch-workflow.md)
+ [ตั้งค่าคอนฟิกลำดับงานของสินค้าในรายการ](configure-line-item-workflow.md)
+ [FAQ เกี่ยวกับลำดับงาน](workflow-FAQ.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]