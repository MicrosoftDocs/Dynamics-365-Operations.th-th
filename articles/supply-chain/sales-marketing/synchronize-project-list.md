---
title: ซิงโครไนส์รายการโครงการจาก Finance and Operations ไปยัง Field Service
description: หัวข้อนี้อธิบายเท็มเพลตและงานพื้นฐานที่ใช้ในการทำให้โครงการจาก Microsoft Dynamics 365 for Finance and Operations ไปยัง Microsoft Dynamics 365 for Field Service
author: ChristianRytt
manager: AnnBe
ms.date: 01/14/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: crytt
ms.dyn365.ops.version: 8.1.3
ms.search.validFrom: 2018-12-01
ms.openlocfilehash: b5aeb4c3925994d7488e8e113e88b9d06ee6b350
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 01/29/2019
ms.locfileid: "312519"
---
# <a name="synchronize-project-list-from-finance-and-operations-to-field-service"></a>ซิงโครไนส์รายการโครงการจาก Finance and Operations ไปยัง Field Service

[!include[banner](../includes/banner.md)]

หัวข้อนี้อธิบายเท็มเพลตและงานพื้นฐานที่ใช้ในการทำให้โครงการจาก Microsoft Dynamics 365 for Finance and Operations ไปยัง Microsoft Dynamics 365 for Field Service

[![การซิงโครไนส์ของกระบวนการทางธุรกิจระหว่าง Finance and Operations และ Field Service](./media/FSProjectOW.png)](./media/FSProjectOW.png)

## <a name="templates-and-tasks"></a>เท็มเพลตและงาน
เท็มเพลตและงานพื้นฐานต่อไปนี้ถูกใช้ในการรันการทำให้ข้อมูลตรงกันของโครงการจาก Microsoft Dynamics 365 for Finance and Operations ไปยัง Microsoft Dynamics 365 for Field Service

**เท็มเพลตในการรวมข้อมูล**
- โครงการ (Finance and Operations ไปยัง Field Service)

**งานในโครงการการรวมข้อมูล**
- โครงการ

จำเป็นต้องทำงานการซิงโครไนส์ต่อไปนี้ ก่อนที่การซิงโครไนส์ขอโครงการจะเกิดขึ้นได้:
- บัญชี (Sales ไปยัง Finance and Operations) 

## <a name="entity-set"></a>การตั้งค่าเอนทิตี้
| Field Service           | Finance and Operations  |
|-------------------------|-------------------------|
|msdynce_externalprojects | โครงการ                |

## <a name="entity-flow"></a>ขั้นตอนเอนทิตี้
โครงการถูกสร้างใน Finance and Operations โครงการที่มี **ชนิดโครงการ** ถูกตั้งค่าเป็น **เวลาและวัสดุ** และ **ขั้นตอนโครงการ** ถูกตั้งค่าเป็น **อยู่ระหว่างดำเนินการ** จะทำให้ข้อมูลตรงกันไปยังเอนทิตี **โครงการภายนอก** ใน Field Service ซึ่งรวมหมายเลขโครงการ ชื่อโครงการ ลำดับขั้นโครงการ และข้อมูลบัญชีลูกค้า รายการ **โครงการภายนอก** ถูกใช้เพื่อจับคู่ใบสั่งขาย Field service กับโครงการ Finance and Operations

## <a name="field-service-crm-solution"></a>โซลูชัน CRM ของ Field Service
เอนทิตี **โครงการภายนอก** รับโครงการทั้งหมดจาก Finance and Operations ฟิลด์ **โครงการภายนอก** ได้ถูกเพิ่มไปยังเอนทิตี **ใบสั่งงาน** นี่คือฟิลด์การค้นหา ดังนั้นโดยการแท็กใบสั่งงานของคุณกับโครงการ ใบสั่งขายจะถูกเชื่อมต่อไปยังโครงการภายใน Finance and Operations หลังจาก **สถานะระบบ** เปลี่ยนแปลง **เปิด – อยู่ระหว่างดำเนินการ(690,970,000)** ไปยังสถานะที่สูงกว่า ฟิลด์ **โครงการภายนอก** จะถูกล็อคและคุณไม่สามารถเพิ่ม ลบ หรือเปลี่ยนแปลงค่าได้อีก

## <a name="prerequisites-and-mapping-setup"></a>การตั้งค่าการแม็ปและข้อกำหนดเบื้องต้น
### <a name="finance-and-operations"></a>Finance and Operations
เปิดใช้งานการติดตามการเปลี่ยนแปลงสำหรับโครงการเอนทิตีข้อมูล

## <a name="template-mapping-in-data-integration"></a>การแม็ปเท็มเพลตในการรวมข้อมูล


### <a name="projects-finance-and-operations-to-field-service-projects"></a>โครงการ (Finance and Operations ไปยัง Field Service): โครงการ

[![การแม็ปเท็มเพลตในการรวมข้อมูล](./media/FSProject1.png)](./media/FSProject1.png)
