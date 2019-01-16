---
title: "ซิงโครไนส์รายการโครงการจาก Finance and Operations ไปยัง Field Service"
description: "หัวข้อนี้กล่าวถึงเท็มเพลตและงานพื้นฐานที่จะใช้ในการซิงโครไนส์โครงการจาก Microsoft Dynamics 365 for Finance and Operations ไปยัง Microsoft Dynamics 365 for Field Service"
author: ChristianRytt
manager: AnnBe
ms.date: 12/20/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: 
audience: Application User, IT Pro
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 
ms.assetid: 
ms.search.region: global
ms.search.industry: 
ms.author: crytt
ms.dyn365.ops.version: 8.1.3
ms.search.validFrom: 2018-12-01
ms.translationtype: HT
ms.sourcegitcommit: 8c6cb481f1a3fe48d329c5936118d8df88a4175b
ms.openlocfilehash: adcb1c1b241ce2b073cd26cf2a8a8d64931c8b0f
ms.contentlocale: th-th
ms.lasthandoff: 12/20/2018

---

# <a name="synchronize-project-list-from-finance-and-operations-to-field-service"></a>ซิงโครไนส์รายการโครงการจาก Finance and Operations ไปยัง Field Service

[!include[banner](../includes/banner.md)]

หัวข้อนี้กล่าวถึงเท็มเพลตและงานพื้นฐานที่จะใช้ในการซิงโครไนส์โครงการจาก Microsoft Dynamics 365 for Finance and Operations ไปยัง Microsoft Dynamics 365 for Field Service

[![การซิงโครไนส์ของกระบวนการทางธุรกิจระหว่าง Finance and Operations และ Field Service](./media/FSProjectOW.png)](./media/FSProjectOW.png)

## <a name="templates-and-tasks"></a>เท็มเพลตและงาน
เท็มเพลตและงานพื้นฐานต่อไปนี้ถูกใช้ในการรันการซิงโครไนส์ของโครงการจาก Microsoft Dynamics 365 for Finance and Operations ไปยัง Microsoft Dynamics 365 for Field Service

**ชื่อของเท็มเพลตในการรวมข้อมูล:**
- โครงการ (Finance and Operations ไปยัง Field Service)

**ชื่อของงานในโครงการการรวมข้อมูล:**
- โครงการ

จำเป็นต้องทำงานการซิงโครไนส์ต่อไปนี้ ก่อนที่การซิงโครไนส์ขอโครงการจะเกิดขึ้นได้:
- บัญชี (Sales ไปยัง Finance and Operations) 

## <a name="entity-set"></a>การตั้งค่าเอนทิตี้
Field Service   Finance and Operations

| Field Service           | Finance and Operations  |
|-------------------------|-------------------------|
|msdynce_externalprojects | โครงการ                |

## <a name="entity-flow"></a>ขั้นตอนเอนทิตี้
โครงการถูกสร้างใน Finance and Operations โครงการที่มี **ชนิดโครงการ** เวลาและวัสดุ และ **ระยะโครงการ** ในกระบวนการ จะซิงโครไนซ์กับเอนทิตี **โครงการภายนอก** ใน Field Service ซึ่งรวมถึงหมายเลขโครงการ ชื่อโครงการ ระยะโครงการ และ ข้อมูลบัญชีของลูกค้า รายการของ **โครงการภายนอก** ใช้ในการจับคู่ใบสั่งงาน Field service กับโครงการ Finance and Operations
โซลูชัน CRM ของ Field Service โครงการภายนอกคือเอนทิตีใหม่ที่เรียกดูโครงการทั้งหมดจากการดำเนินการ
มีการเพิ่มฟิลด์โครงการภายนอกไปยังเอนทิตีของใบสั่งงาน ฟิลด์นี้เป็นการค้นหา และซื้อติดป้ายลำดับงานของคุณกับโครงการที่ใบสั่งขายจะถูกเชื่อมต่อกับโครงการภายในการดำเนินงาน เมื่อการเปลี่ยนแปลงสถานะของระบบเปิด – อยู่ระหว่างการดำเนินงาน(690,970,000) ให้เป็นสถานะที่สูงกว่า ฟิลด์โครงการภายนอก จะถูกล็อค และคุณไม่สามารถเพิ่ม ลบ หรือเปลี่ยนแปลงค่าได้

## <a name="prerequisites-and-mapping-setup"></a>การตั้งค่าการแม็ปและข้อกำหนดเบื้องต้น
### <a name="in-finance-and-operations"></a>ใน Finance and Operations
เปิดใช้งานการเปลี่ยนแปลงที่ติดตามสำหรับโครงการเอนทิตีข้อมูล

## <a name="template-mapping-in-data-integration"></a>การแม็ปเท็มเพลตในการรวมข้อมูล


### <a name="projects-finance-and-operations-to-field-service-projects"></a>โครงการ (Finance and Operations ไปยัง Field Service): โครงการ

[![การแม็ปเท็มเพลตในการรวมข้อมูล](./media/FSProject1.png)](./media/FSProject1.png)

