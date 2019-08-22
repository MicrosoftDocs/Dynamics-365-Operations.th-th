---
title: ซิงโครไนส์งานโครงการโดยตรงจาก Project Service Automation ไปยัง Finance and Operations
description: หัวข้อนี้อธิบายเท็มเพลตและงานพื้นฐานที่ใช้ในการทำให้ข้อมูลงานโครงการจาก Microsoft Dynamics 365 for Project Service Automation ไปยัง Microsoft Dynamics 365 for Finance and Operations ตรงกันโดยตรง
author: KimANelson
manager: AnnBe
ms.date: 07/20/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 87983
ms.assetid: b454ad57-2fd6-46c9-a77e-646de4153067
ms.search.region: Global
ms.author: knelson
ms.search.validFrom: 2016-11-28
ms.dyn365.ops.version: AX 7.3.0
ms.openlocfilehash: f7ea5036682ad5b61fe56acd20a591cccc01f2cb
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 08/01/2019
ms.locfileid: "1838330"
---
# <a name="synchronize-project-tasks-directly-from-project-service-automation-to-finance-and-operations"></a>ซิงโครไนส์งานโครงการโดยตรงจาก Project Service Automation ไปยัง Finance and Operations

[!include[banner](../includes/banner.md)]

หัวข้อนี้อธิบายเท็มเพลตและงานพื้นฐานที่ใช้ในการทำให้ข้อมูลงานโครงการจาก Microsoft Dynamics 365 for Project Service Automation ไปยัง Microsoft Dynamics 365 for Finance and Operations ตรงกันโดยตรง

> [!NOTE]
> - การรวมงานโครงการ ประเภทธุรกรรมค่าใช้จ่าย การประเมินชั่วโมง การประเมินค่าใช้จ่าย และการล็อคฟังก์ชัน พร้อมใช้งานใน Microsoft Dynamics 365 for Finance and Operations รุ่น 8.0
> - ถ้าคุณกำลังใช้ Microsoft Dynamics 365 for Finance and Operations, Enterprise Edition 7.3.0 หลังจากที่คุณติดตั้ง KB 4132657 และ KB 4132660 คุณจะสามารถใช้เท็มเพลตเพื่อรวมงานโครงการ ค่าใช้จ่ายประเภทธุรกรรม การประเมินชั่วโมง การประเมินค่าใช้จ่าย และค่าที่เกิดขึ้นจริงได้ และสามารถตั้งค่าคอนฟิกการล็อคฟังก์ชันได้ ถ้าคุณต้องรีเซ็ตการกระจายการลงบัญชี เราขอแนะนำให้ คุณติดตั้ง KB 4131710 ด้วย
> - การรวมรายการจริงพร้อมใช้งานใน Microsoft Dynamics 365 for Finance and Operations รุ่น 8.0.1 หรือรุ่นที่ใหม่กว่า

## <a name="data-flow-for-project-service-automation-to-finance-and-operations"></a>โฟลว์ข้อมูลสำหรับ Project Service Automation ไปยัง Finance and Operations

โซลูชันการรวม Project Service Automation ไปยัง Finance and Operations ใช้คุณลักษณะการรวมข้อมูล เพื่อซิงโครไนส์ข้อมูลระหว่างอินสแตนซ์ของ Project Service Automation และ Finance and Operations เท็มเพลตการรวมที่พร้อมใช้งานกับคุณลักษณะการรวมข้อมูล ช่วยให้ทิศทางของข้อมูลเกี่ยวกับงานโครงการจาก Project Service Automation ไปยัง Finance and Operations

ภาพประกอบต่อไปนี้แสดงวิธีการซิงโครไนส์ข้อมูลระหว่าง Project Service Automation และ Finance and Operations

[![โฟลว์ข้อมูลสำหรับ Project Service Automation กับ Finance and Operations](./media/ProjectTasksFlow.png)](./media/ProjectTasksFlow.png)

## <a name="template-and-task"></a>เท็มเพลตและงาน

เพื่อเข้าถึงเท็มเพลต ในศูนย์การจัดการ Microsoft PowerApps เลือก **โครงการ** และจากนั้น ที่มุมขวาบน เลือก **โครงการใหม่** เพื่อเลือกเท็มเพลตสาธารณะ

เท็มเพลตและงานพื้นฐานต่อไปนี้ถูกใช้ในการซิงโครไนส์งานโครงการจาก Project Service Automation ไปยัง Finance and Operations:

- **ชื่อของเท็มเพลตในการรวมข้อมูล:** งานของโครงการ (PSA ไปยัง Fin and Ops)
- **ชื่อของงานในโครงการ:** งานของโครงการ

ก่อนที่การซิงโครไนส์ของงานโครงการจะสามารถเกิดขึ้นได้ คุณต้องซิงโครไนส์โครงการและสัญญาโครงการ

## <a name="entity-set"></a>การตั้งค่าเอนทิตี้

| Project Service Automation | Finance and Operations              |
|----------------------------|-------------------------------------|
| งานโครงการ              | เอนทิตี้การรวมสำหรับงานของโครงการ |

## <a name="entity-flow"></a>ขั้นตอนเอนทิตี้

มีการจัดการงานโครงการใน Project Service Automation และมีการซิงโครไนส์ไปยัง Finance and Operations เป็นกิจกรรมโครงการ

## <a name="prerequisites-and-mapping-setup"></a>การตั้งค่าการแม็ปและข้อกำหนดเบื้องต้น

ก่อนที่การซิงโครไนส์ของงานโครงการจะสามารถเกิดขึ้นได้ คุณต้องซิงโครไนส์โครงการและสัญญาโครงการ

## <a name="power-query"></a>Power Query

คุณต้องใช้ Microsoft Power Query for Excel เพื่อกรองข้อมูล ถ้าเป็นไปตามเงื่อนไขนี้:

- คุณมีเรกคอร์ดเฉพาะทรัพยากรในงานโครงการ

ถ้าคุณต้องใช้ Power Query ให้ทำตามคำแนะนำนี้:

- เท็มเพลตงานโครงการ (PSA ไปยัง Fin and Ops) มีตัวกรองเริ่มต้นที่แยกเรกคอร์ดเฉพาะทรัพยากรจากงานโครงการ โดยการตั้งค่าตัวกรองใน **IsLineTask** เป็น **เท็จ** ถ้าคุณสร้างเท็มเพลตของคุณเอง คุณต้องเพิ่มตัวกรองนี้

## <a name="template-mapping-in-data-integration"></a>การแม็ปเท็มเพลตในการรวมข้อมูล

ภาพประกอบต่อไปนี้แสดงตัวอย่างของการแม็ปงานเท็มเพลตในการรวมข้อมูล การแม็ปแสดงข้อมูลฟิลด์ที่จะถูกซิงโครไนส์จาก Project Service Automation ไปยัง Finance and Operations

[![การแม็ปเท็มเพลต](./media/ProjectTasksMapping.png)](./media/ProjectTasksMapping.png)
