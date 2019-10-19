---
title: ซิงโครไนส์การปรับปรุงสินค้าคงคลังจาก Supply Chain Management ไปยัง Field Service
description: หัวข้อนี้อธิบายเท็มเพลตและงานพื้นฐานที่ใช้ในการทำให้โครงการจาก Dynamics 365 Supply Chain Management ไปยัง Dynamics 365 Field Service
author: ChristianRytt
manager: AnnBe
ms.date: 03/13/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: crytt
ms.dyn365.ops.version: 8.1.3
ms.search.validFrom: 2018-12-01
ms.openlocfilehash: b74a7f0445b3bdad671da4c61e561bc0d9d80cd1
ms.sourcegitcommit: 2460d0da812c45fce67a061386db52e0ae46b0f3
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 09/30/2019
ms.locfileid: "2251603"
---
# <a name="synchronize-project-list-from-supply-chain-management-to-field-service"></a>ซิงโครไนส์การปรับปรุงสินค้าคงคลังจาก Supply Chain Management ไปยัง Field Service

[!include[banner](../includes/banner.md)]

หัวข้อนี้อธิบายเท็มเพลตและงานพื้นฐานที่ใช้ในการทำให้โครงการจาก Dynamics 365 Supply Chain Management ไปยัง Dynamics 365 Field Service

[![การซิงโครไนส์ของกระบวนการทางธุรกิจระหว่าง Supply Chain Management และ Field Service](./media/FSProjectOW.png)](./media/FSProjectOW.png)

## <a name="templates-and-tasks"></a>เท็มเพลตและงาน
เท็มเพลตและงานพื้นฐานต่อไปนี้จะถูกใช้ในการเรียกใช้การซิงโครไนส์โครงการจาก Supply Chain Management ไปยัง Field Service

**เท็มเพลตในการรวมข้อมูล**
- ผลิตภัณฑ์ (Supply Chain Management ไปยัง Field Service)

**งานในโครงการการรวมข้อมูล**
- โครงการ

จำเป็นต้องทำงานการซิงโครไนส์ต่อไปนี้ ก่อนที่การซิงโครไนส์ขอโครงการจะเกิดขึ้นได้:
- บัญชี (Sales ไปยัง Supply Chain Management) 

## <a name="entity-set"></a>การตั้งค่าเอนทิตี้
| Field Service           | Supply Chain Management  |
|-------------------------|-------------------------|
|msdynce_externalprojects | โครงการ                |

## <a name="entity-flow"></a>ขั้นตอนเอนทิตี้
โครงการถูกสร้างใน Supply Chain Management โครงการที่มี **ชนิดโครงการ** ถูกตั้งค่าเป็น **เวลาและวัสดุ** และ **ขั้นตอนโครงการ** ถูกตั้งค่าเป็น **อยู่ระหว่างดำเนินการ** จะทำให้ข้อมูลตรงกันไปยังเอนทิตี **โครงการภายนอก** ใน Field Service ซึ่งรวมหมายเลขโครงการ ชื่อโครงการ ลำดับขั้นโครงการ และข้อมูลบัญชีลูกค้า รายการ **โครงการภายนอก** ถูกใช้เพื่อจับคู่ใบสั่งขาย Field service กับโครงการ Supply Chain Management

## <a name="field-service-crm-solution"></a>โซลูชัน CRM ของ Field Service
เอนทิตี **โครงการภายนอก** รับโครงการทั้งหมดจาก Supply Chain Management ฟิลด์ **โครงการภายนอก** ได้ถูกเพิ่มไปยังเอนทิตี **ใบสั่งงาน** นี่คือฟิลด์การค้นหา ดังนั้นโดยการแท็กใบสั่งงานของคุณกับโครงการ ใบสั่งขายจะถูกเชื่อมต่อไปยังโครงการภายใน Supply Chain Management หลังจาก **สถานะระบบ** เปลี่ยนแปลง **เปิด – อยู่ระหว่างดำเนินการ(690,970,000)** ไปยังสถานะที่สูงกว่า ฟิลด์ **โครงการภายนอก** จะถูกล็อคและคุณไม่สามารถเพิ่ม ลบ หรือเปลี่ยนแปลงค่าได้อีก

## <a name="prerequisites-and-mapping-setup"></a>การตั้งค่าการแม็ปและข้อกำหนดเบื้องต้น
### <a name="supply-chain-management"></a>Supply Chain Management
เปิดใช้งานการติดตามการเปลี่ยนแปลงสำหรับโครงการเอนทิตีข้อมูล

## <a name="template-mapping-in-data-integration"></a>การแม็ปเท็มเพลตในการรวมข้อมูล


### <a name="projects-supply-chain-management-to-field-service-projects"></a>โครงการ (Supply Chain Management ไปยัง Field Service): โครงการ

[![การแม็ปเท็มเพลตในการรวมข้อมูล](./media/FSProject1.png)](./media/FSProject1.png)
