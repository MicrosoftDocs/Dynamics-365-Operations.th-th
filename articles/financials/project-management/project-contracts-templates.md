---
title: "ซิงโครไนส์สัญญาโครงการและโครงการโดยตรงจาก Project Service Automation ไปยัง Finance and Operations"
description: "หัวข้อนี้อธิบายเท็มเพลตและงานพื้นฐานที่จะใช้ในการซิงโครไนส์สัญญาโครงการและโครงการโดยตรงจาก Microsoft Dynamics 365 for Project Service Automation ไปยัง Microsoft Dynamics 365 for Finance and Operations"
author: KimANelson
manager: AnnBe
ms.date: 07/20/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 87983
ms.assetid: b454ad57-2fd6-46c9-a77e-646de4153067
ms.search.region: Global
ms.author: knelson
ms.search.validFrom: 2017-12-13
ms.dyn365.ops.version: AX 7.3.0
ms.translationtype: HT
ms.sourcegitcommit: 1d98cbff30620256c9d13e7b4a90314db150e33e
ms.openlocfilehash: 65a274323a2d95c9c76727c9e40aa7e649e6350a
ms.contentlocale: th-th
ms.lasthandoff: 08/09/2018

---

# <a name="synchronize-project-contracts-and-projects-directly-from-project-service-automation-to-finance-and-operations"></a>ซิงโครไนส์สัญญาโครงการและโครงการโดยตรงจาก Project Service Automation ไปยัง Finance and Operations

[!include[banner](../includes/banner.md)]

หัวข้อนี้อธิบายเท็มเพลตและงานพื้นฐานที่จะใช้ในการซิงโครไนส์สัญญาโครงการและโครงการโดยตรงจาก Microsoft Dynamics 365 for Project Service Automation ไปยัง Microsoft Dynamics 365 for Finance and Operations

> [!NOTE] 
> ถ้าคุณกำลังใช้ Microsoft Dynamics 365 for Finance and Operations Enterprise Edition 7.3.0 คุณต้องติดตั้ง KB 4074835

## <a name="data-flow-for-project-service-automation-to-finance-and-operations"></a>โฟลว์ข้อมูลสำหรับ Project Service Automation ไปยัง Finance and Operations

> [!NOTE]
> ก่อนที่คุณสามารถใช้โซลูชันการรวม Project Service Automation ไปยัง Finance and Operations ได้ คุณควรจะคุ้นเคยกับลักษณะการทำงานการรวมข้อมูลของ Microsoft Dynamics 365

โซลูชันการรวม Project Service Automation ไปยัง Finance and Operations ใช้คุณลักษณะการรวมข้อมูล เพื่อซิงโครไนส์ข้อมูลระหว่างอินสแตนซ์ของ Project Service Automation และ Finance and Operations เท็มเพลตการรวมที่พร้อมใช้งานกับคุณลักษณะการรวมเปิดใช้งานโฟลว์เกี่ยวกับสัญญาโครงการ โครงการ รายการสัญญาโครงการ และเหตุการณ์สำคัญของรายการสัญญาโครงการจาก Project Service Automation ไปยัง Finance and Operations

ภาพประกอบต่อไปนี้แสดงวิธีการซิงโครไนส์ข้อมูลระหว่าง Project Service Automation และ Finance and Operations

[![โฟลว์ข้อมูลสำหรับการรวม Project Service Automation กับ Finance and Operations](./media/ProjectsAndContractsFlow.JPG)](./media/ProjectsAndContractsFlow.JPG)

## <a name="templates-and-tasks"></a>เท็มเพลตและงาน

เมื่อต้องการเข้าถึงเท็มเพลตที่พร้อมใช้งาน ในศูนย์การจัดการ Microsoft PowerApps เลือก **โครงการ** และจากนั้น ในมุมบนด้านขวา เลือก **โครงการใหม่** เพื่อเลือกเท็มเพลตสาธารณะ

เท็มเพลตและงานพื้นฐานต่อไปนี้จะถูกใช้ในการซิงโครไนส์สัญญาโครงการและโครงการจาก Project Service Automation ไปยัง Finance and Operations:

- **ชื่อของเท็มเพลตในการรวมข้อมูล:** โครงการและสัญญา (PSA ไปยัง Fin and Ops)
- **ชื่อของงานในโครงการ:**

    - สัญญาโครงการ PSA ไปยัง Fin and Ops
    - โครงการ PSA ไปยัง Fin and Ops
    - รายการสัญญาโครงการ PSA ไปยัง Fin and Ops
    - เหตุการณ์สำคัญของรายการสัญญาโครงการ PSA ไปยัง Fin and Ops

ก่อนที่การซิงโครไนส์ของสัญญาโครงการและโครงการจะสามารถเกิดขึ้นได้ คุณต้องซิงโครไนส์บัญชี

## <a name="entity-set"></a>การตั้งค่าเอนทิตี้

| Project Service Automation       | Finance and Operations                                 |
|----------------------------------|--------------------------------------------------------|
| ใบสั่ง                           | เอนทิตี้การรวมสำหรับสัญญาของโครงการ                |
| โครงการ                         | เอนทิตี้การรวมสำหรับโครงการ                         |
| รายการใบสั่ง                      | เอนทิตี้การรวมสำหรับรายการสัญญาของโครงการ           |
| เหตุการณ์สำคัญของรายการสัญญาของโครงการ | เอนทิตี้การรวมสำหรับเหตุการณ์สำคัญของรายการสัญญาของโครงการ |

## <a name="entity-flow"></a>ขั้นตอนเอนทิตี้

มีการจัดการสัญญาโครงการใน Project Service Automation และมีการซิงโครไนส์ไปยัง Finance and Operations เป็นสัญญาโครงการ ในฐานะที่เป็นส่วนหนึ่งของเท็มเพลตการรวม คุณสามารถกำหนดแหล่งที่มารวมใน Finance and Operations สำหรับสัญญาโครงการได้

มีการจัดการโครงการเวลาและวัสดุและโครงการที่มีราคาคงที่ใน Project Service Automation และมีการซิงโครไนส์ไปยัง Finance and Operations เป็นโครงการ ในฐานะที่เป็นส่วนหนึ่งของการรวมเท็มเพลต คุณสามารถกำหนดแหล่งที่มารวมใน Finance and Operations สำหรับโครงการได้

มีการจัดการรายการสัญญาโครงการใน Project Service Automation และมีการซิงโครไนส์ไปยัง Finance and Operations เป็นกฎการเรียกเก็บเงินสำหรับสัญญาโครงการ ถ้าวิธีการเรียกเก็บเงินแตกต่างจากชนิดโครงการเริ่มต้น การซิงโครไนส์จะปรับปรุงชนิดโครงการสำหรับโครงการรายการในสัญญาและกลุ่มโครงการ

มีการจัดการเหตุการณ์สำคัญของรายการสัญญาของโครงการใน Project Service Automation และมีการซิงโครไนส์ไปยัง Finance and Operations เป็นเหตุการณ์สำคัญของกฎการเรียกเก็บเงินสำหรับสัญญาโครงการ

## <a name="project-service-automation-to-finance-and-operations-integration-solution"></a>โซลูชันการรวม Project Service Automation ไปยัง Finance and Operations

ฟิลด์ **รหัสสัญญาโครงการ** จะพร้อมใช้งานบนหน้า **สัญญาโครงการ** ฟิลด์นี้ได้ถูกทำให้เป็นคีย์เฉพาะและธรรมชาติ เพื่อสนับสนุนการรวม

เมื่อมีการสร้างสัญญาโครงการใหม่ ถ้าค่า **รหัสสัญญาโครงการ** ไม่ได้มีอยู่แล้ว ระบบจะสร้างขึ้นโดยอัตโนมัติโดยใช้ลำดับหมายเลข ค่าประกอบด้วย **ORD** ตามด้วยลำดับหมายเลขที่เพิ่มขึ้น แล้วจึงตามด้วยคำต่อท้ายหกอักขระ นี่คือตัวอย่าง: **ORD-01022-Z4M9Q0**

ฟิลด์ **หมายเลขโครงการ** จะพร้อมใช้งานบนหน้า **โครงการ** ฟิลด์นี้ได้ถูกทำให้เป็นคีย์เฉพาะและธรรมชาติ เพื่อสนับสนุนการรวม

เมื่อมีการสร้างโครงการใหม่ ถ้าค่า **หมายเลขโครงการ** ไม่ได้มีอยู่แล้ว ระบบจะสร้างขึ้นโดยอัตโนมัติโดยใช้ลำดับหมายเลข ค่าประกอบด้วย **PRJ** ตามด้วยลำดับหมายเลขที่เพิ่มขึ้น แล้วจึงตามด้วยคำต่อท้ายหกอักขระ นี่คือตัวอย่าง: **PRJ-01049-CCNID0**

เมื่อมีการใช้โซลูชันการรวม Project Service Automation ไปยัง Finance and Operations<TO DO: link in the top level document link where we will be adding the instructions for applying the PSA solution> สคริปต์การอัพเกรดจะตั้งค่าฟิลด์ **รหัสสัญญาโครงการ** สำหรับสัญญาโครงการที่มีอยู่ และฟิลด์ **หมายเลขโครงการ** สำหรับโครงการที่มีอยู่ใน Project Service Automation

## <a name="prerequisites-and-mapping-setup"></a>การตั้งค่าการแม็ปและข้อกำหนดเบื้องต้น

- ก่อนที่การซิงโครไนส์ของสัญญาโครงการและโครงการจะสามารถเกิดขึ้นได้ คุณต้องซิงโครไนส์บัญชี
- ในชุดการเชื่อมต่อของคุณ เพิ่มการแม็ปฟิลด์คีย์รวมสำหรับ **msdyn\_organizationalunits** ไปยัง **msdyn\_ชื่อ \[ชื่อ\]** อันดับแรก คุณอาจต้องเพิ่มโครงการไปยังชุดของการเชื่อมต่อ สำหรับข้อมูลเพิ่มเติมเกี่ยวกับคีย์การรวม ดู [การรวมข้อมูล Dynamics 365](https://docs.microsoft.com/en-us/common-data-service/entity-reference/dynamics-365-integration)
- ในชุดการเชื่อมต่อของคุณ เพิ่มการแม็ปฟิลด์คีย์รวมสำหรับ **msdyn\_โครงการ** ไปยัง **msdynce\_projectnumber \[หมายเลขโครงการ\]** อันดับแรก คุณอาจต้องเพิ่มโครงการไปยังชุดของการเชื่อมต่อ สำหรับข้อมูลเพิ่มเติมเกี่ยวกับคีย์การรวม ดู [การรวมข้อมูล Dynamics 365](https://docs.microsoft.com/en-us/common-data-service/entity-reference/dynamics-365-integration)
- **SourceDataID** สำหรับสัญญาโครงการและโครงการ สามารถปรับปรุงเป็นค่าอื่น หรือลบออกจากการแม็ปได้ ค่าเท็มเพลตเริ่มต้นคือ **Project Service Automation**
- การแม็ป **PaymentTerms** ต้องถูกปรับปรุง เพื่อให้สะท้อนถึงเงื่อนไขที่ถูกต้องของการชำระเงินใน Finance and Operations คุณยังสามารถลบการแม็ปจากภารกิจของโครงการได้ด้วย แม็ปค่าเริ่มต้นมีค่าเริ่มต้นสำหรับข้อมูลสาธิต ตารางต่อไปนี้แสดงค่าใน Project Service Automation

    | มูลค่า | คำอธิบาย   |
    |-------|---------------|
    | 1     | สุทธิ 30        |
    | 2     | 2%10 สุทธิ 30 |
    | 3     | สุทธิ 45        |
    | 4     | สุทธิ 60        |

## <a name="power-query"></a>Power Query

คุณต้องใช้ Microsoft Power Query for Excel เพื่อกรองข้อมูล ถ้าเป็นไปตามเงื่อนไขต่อไปนี้:

- คุณมีใบสั่งขายใน Microsoft Dynamics 365 for Sales
- คุณมีหน่วยงานขององค์กรหลายหน่วยใน Project Service Automation และหน่วยงานขององค์กรเหล่านี้จะถูกแม็ปกับนิติบุคคลหลายรายใน Finance and Operations

ถ้าคุณต้องใช้ Power Query ให้ทำตามคำแนะนำเหล่านี้:

- เท็มเพลตโครงการและสัญญา (PSA ไปยัง Fin and Ops) มีตัวกรองเริ่มต้นที่รวมเฉพาะใบสั่งขายของชนิด **รายการงาน (msdyn\_ordertype = 192350001)** ตัวกรองข้อมูลนี้ช่วยรับประกันว่า จะไม่มีการสร้างสัญญาโครงการสำหรับใบสั่งขายใน Finance and Operations ถ้าคุณสร้างเท็มเพลตของคุณเอง คุณต้องเพิ่มตัวกรองนี้
- คุณต้องสร้างตัวกรอง Power Query ที่รวมเฉพาะองค์กรในสัญญาที่ควรถูกซิงโครไนส์กับนิติบุคคลของชุดการเชื่อมต่อแบบรวม ตัวอย่างเช่น โครงการสัญญาที่คุณมีกับหน่วยงานในองค์กรในสัญญาของ Contoso US ควรถูกซิงโครไนส์กับนิติบุคคลที่ USSI แต่สัญญาโครงการที่คุณมีกับหน่วยงานในองค์กรในสัญญาของ Contoso Global ควรถูกซิงโครไนส์กับนิติบุคคล USMF ถ้าคุณไม่เพิ่มตัวกรองข้อมูลนี้ไปยังการแม็ปงานของคุณ สัญญาโครงการทั้งหมดจะถูกซิงโครไนส์กับนิติบุคคลที่กำหนดไว้สำหรับชุดการเชื่อมต่อ โดยไม่คำนึงถึงหน่วยงานในองค์กรในสัญญา

## <a name="template-mapping-in-data-integration"></a>การแม็ปเท็มเพลตในการรวมข้อมูล

> [!NOTE] 
> ฟิลด์ **CustomerReference** **AddressCity** **AddressCountryRegionID** **AddressDescription** **AddressLine1** **AddressLine2** **AddressState** และ **AddressZipCode** ไม่ได้รวมอยู่ในการแม็ปค่าเริ่มต้นสำหรับสัญญาโครงการ คุณสามารถเพิ่มการแม็ปได้ หากคุณต้องการให้ข้อมูลนี้ถูกซิงโครไนส์สำหรับสัญญาโครงการ
>
> ฟิลด์ **คำอธิบาย** **ParentID** **ProjectGroup** **ProjectManagerPersonnelNumber** และ **ProjectType** ไม่ได้รวมอยู่ในการแม็ปค่าเริ่มต้นสำหรับโครงการ คุณสามารถเพิ่มการแม็ปได้ หากคุณต้องการให้ข้อมูลนี้ถูกซิงโครไนส์สำหรับโครงการ

ภาพประกอบต่อไปนี้แสดงตัวอย่างของการแม็ปงานเท็มเพลตในการรวมข้อมูล การแม็ปแสดงข้อมูลฟิลด์ที่จะถูกซิงโครไนส์จาก Project Service Automation ไปยัง Finance and Operations

[![การแม็ปเท็มเพลต](./media/ProjectContractTemplateMapping.JPG)](./media/ProjectContractTemplateMapping.JPG)

[![การแม็ปเท็มเพลต](./media/ProjectTemplateMapping.JPG)](./media/ProjectTemplateMapping.JPG)

[![การแม็ปเท็มเพลต](./media/ProjectContractLinesMapping.JPG)](./media/ProjectContractLinesMapping.JPG)

[![การแม็ปเท็มเพลต](./media/ProjectContractLineMilestonesMapping.JPG)](./media/ProjectContractLineMilestonesMapping.JPG)

