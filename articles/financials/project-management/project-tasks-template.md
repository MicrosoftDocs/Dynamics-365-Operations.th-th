---
title: "ซิงโครไนส์งานโครงการจาก Project Service Automation"
description: "หัวข้อนี้อธิบายเท็มเพลตและงานพื้นฐานที่จะใช้ในการซิงโครไนส์งานโดยตรงจาก Microsoft Dynamics 365 for Project Service Automation ไปยัง Microsoft Dynamics 365 for Finance and Operations"
author: KimANelson
manager: AnnBe
ms.date: 04/02/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 87983
ms.assetid: b454ad57-2fd6-46c9-a77e-646de4153067
ms.search.region: Global
ms.author: knelson
ms.search.validFrom: 2016-11-28
ms.dyn365.ops.version: AX 7.3.0
ms.translationtype: HT
ms.sourcegitcommit: 399b519ab0da4de405aeb06f3e7f4bf29a6c5cc3
ms.openlocfilehash: 89df0d99d780441ad08cd6bff3e1fd203694eb8e
ms.contentlocale: th-th
ms.lasthandoff: 05/30/2018

---

# <a name="synchronize-project-tasks-from-project-service-automation-directly-to-project-activities-in-finance-and-operations"></a>ซิงโครไนส์งานโครงการจาก Project Service Automation โดยตรงไปยัง Finance and Operations

หัวข้อนี้อธิบายเท็มเพลตและงานพื้นฐานที่จะใช้ในการซิงโครไนส์งานโดยตรงจาก Microsoft Dynamics 365 for Project Service Automation ไปยัง Microsoft Dynamics 365 for Finance and Operations

> [!NOTE]
> การรวมงานโครงการ ประเภทธุรกรรมค่าใช้จ่าย การประเมินชั่วโมง การประเมินค่าใช้จ่าย และการล็อคฟังก์ชัน พร้อมใช้งานใน Dynamics 365 for Finance and Operations รุ่น 8.0

## <a name="data-flow-for-project-service-automation-to-finance-and-operations"></a>โฟลว์ข้อมูลสำหรับ Project Service Automation ไปยัง Finance and Operations

โซลูชันการรวม Project Service Automation ไปยัง Finance and Operations ใช้คุณลักษณะการรวมข้อมูล เพื่อซิงโครไนส์ข้อมูลระหว่างอินสแตนซ์ของ Project Service Automation และ Finance and Operations เท็มเพลตการรวมที่พร้อมใช้งานกับคุณลักษณะการรวมข้อมูล ช่วยให้ทิศทางของข้อมูลเกี่ยวกับงานโครงการจาก Project Service Automation ไปยัง Finance and Operations

ภาพประกอบต่อไปนี้แสดงวิธีการซิงโครไนส์ข้อมูลระหว่าง Project Service Automation และ Finance and Operations

[![โฟลว์ข้อมูลสำหรับ Project Service Automation กับ Finance and Operations](./media/ProjectTasksFlow.png)](./media/ProjectTasksFlow.png)

## <a name="template-and-task"></a>เท็มเพลตและงาน

เมื่อต้องการเข้าถึงเท็มเพลต ในศูนย์การจัดการ Microsoft PowerApps เลือก **โครงการ** และจากนั้น ในมุมบนด้านขวา เลือก **โครงการใหม่** เพื่อเลือกเท็มเพลตสาธารณะ

เท็มเพลตและงานพื้นฐานต่อไปนี้จะถูกใช้ในการซิงโครไนส์งานโครงการจาก Project Service Automation ไปยัง Finance and Operations:

-**ชื่อของเท็มเพลตในการรวมข้อมูล:** งานโครงการ (PSA ไปยัง Fin and Ops) -**ชื่อของงานในโครงการ:** งานโครงการ

ก่อนที่การซิงโครไนส์ของงานโครงการจะสามารถเกิดขึ้นได้ คุณต้องซิงโครไนส์โครงการและสัญญาโครงการ

## <a name="entity-set"></a>การตั้งค่าเอนทิตี้

|Project Service Automation               | Finance and Operations                |
|-----------------------------------------|---------------------------------------|
| งานโครงการ                           | เอนทิตีการรวมสำหรับงานโครงการ   |

## <a name="entity-flow"></a>ขั้นตอนเอนทิตี้

มีการจัดการงานโครงการใน Project Service Automation และมีการซิงโครไนส์ไปยัง Finance and Operations เป็นกิจกรรมโครงการ

## <a name="prerequisites-and-mapping-setup"></a>การตั้งค่าการแม็ปและข้อกำหนดเบื้องต้น

ก่อนที่การซิงโครไนส์ของงานโครงการจะสามารถเกิดขึ้นได้ คุณต้องซิงโครไนส์โครงการและสัญญาโครงการ

## <a name="power-query"></a>Power Query

คุณต้องใช้ Microsoft Power Query เพื่อกรองข้อมูล ถ้าเป็นไปตามเงื่อนไขเหล่านี้:

- คุณมีเรกคอร์ดเฉพาะของทรัพยากรภายในงานโครงการ

ถ้าคุณต้องใช้ Power Query ให้ทำตามคำแนะนำเหล่านี้:

- เท็มเพลตโครงการงาน (PSA ไปยัง Fin and Ops) มีตัวกรองเริ่มต้น เพื่อแยกเรกคอร์ดเฉพาะของทรัพยากรจากภายในงานโครงการ โดยการตั้งค่าตัวกรองใน **IsLineTask** เป็น **เท็จ** ถ้าคุณสร้างเท็มเพลตของคุณเอง คุณต้องเพิ่มตัวกรองนี้

## <a name="template-mapping-in-data-integration"></a>การแม็ปเท็มเพลตในการรวมข้อมูล

ภาพประกอบต่อไปนี้แสดงตัวอย่างของการแม็ปงานเท็มเพลตในการรวมข้อมูล การแม็ปแสดงข้อมูลฟิลด์ที่จะถูกซิงโครไนส์จาก Project Service Automation ไปยัง Finance and Operations

[![การแม็ปเท็มเพลต](./media/ProjectTasksMapping.png)](./media/ProjectTasksMapping.png)


