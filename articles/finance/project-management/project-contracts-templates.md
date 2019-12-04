---
title: ซิงโครไนส์สัญญาโครงการและโครงการโดยตรงจาก Project Service Automation ไปยัง Finance and Operations
description: หัวข้อนี้อธิบายเท็มเพลตและงานพื้นฐานที่ใช้ซิงโครไนส์สัญญาโครงการและโครงการโดยตรงจาก Microsoft Dynamics 365 Project Service Automation ไปยัง Dynamics 365 Finance
author: KimANelson
manager: AnnBe
ms.date: 09/09/2019
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
ms.search.validFrom: 2017-12-13
ms.dyn365.ops.version: AX 7.3.0
ms.openlocfilehash: b44fc116f1dcaa1275b2262487ef9114bce639c6
ms.sourcegitcommit: fbc106af09bdadb860677f590464fb93223cbf65
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 11/06/2019
ms.locfileid: "2773865"
---
# <a name="synchronize-project-contracts-and-projects-directly-from-project-service-automation-to-finance-and-operations"></a>ซิงโครไนส์สัญญาโครงการและโครงการโดยตรงจาก Project Service Automation ไปยัง Finance and Operations

[!include[banner](../includes/banner.md)]

หัวข้อนี้อธิบายเท็มเพลตและงานพื้นฐานที่ใช้ในการทำให้ข้อมูลสัญญาโครงการและโครงการจาก Dynamics 365 Project Service Automation ไปยัง Dynamics 365 Finance ตรงกันโดยตรง

> [!NOTE] 
> ถ้าคุณกำลังจะใช้ Enterprise edition 7.3.0 คุณต้องติดตั้ง KB 4074835

## <a name="data-flow-for-project-service-automation-to-finance"></a>โฟลว์ข้อมูลสำหรับ Project Service Automation ไปยัง Finance

> [!NOTE]
> ก่อนที่คุณจะสามารถใช้ Project Service Automation ไปยัง Finance integration solution คุณควรคุ้นเคยกับคุณลักษณะการรวมข้อมูลของ Dynamics 365

การรวมโซลูชั่นจาก Project Service Automation ไปยัง Finance ใช้คุณลักษณะการรวมข้อมูลเพื่อซิงโครไนส์ข้อมูลระหว่างอินสแตนซ์ของ Project Service Automation และ Finance เท็มเพลตการรวมที่พร้อมใช้งานกับคุณลักษณะการรวมข้อมูลเปิดใช้งานลำดับงานของข้อมูลเกี่ยวกับสัญญาโครงการ โครงการ รายการสัญญาโครงการ และเหตุการณ์สำคัญของรายการสัญญาโครงการจาก Project Service Automation ไปยัง Finance

ภาพประกอบต่อไปนี้แสดงวิธีการซิงโครไนส์ข้อมูลระหว่าง Project Service Automation และ Finance

[![ลำดับข้อมูลสำหรับการรวม Project Service Automation กับ Finance](./media/ProjectsAndContractsFlow_upd.JPG)](./media/ProjectsAndContractsFlow.JPG)

## <a name="templates-and-tasks"></a>เท็มเพลตและงาน

เพื่อเข้าถึงเท็มเพลตที่พร้อมใช้งาน ในศูนย์การจัดการ Microsoft Power Apps เลือก **โครงการ** และจากนั้น ที่มุมขวาบน เลือก **โครงการใหม่** เพื่อเลือกเท็มเพลตสาธารณะ

เท็มเพลตและงานพื้นฐานต่อไปนี้จะถูกใช้ซิงโครไนส์สัญญาโครงการและโครงการจาก Project Service Automation ไปยัง Finance:

### <a name="integrating-with-dynamics-365-project-service-automation-v2x"></a>การผสานรวมกับ Dynamics 365 Project Service Automation v2 x
- **ชื่อของเท็มเพลตในการรวมข้อมูล:** โครงการและสัญญา (PSA ไปยัง Fin and Ops)
- **ชื่อของงานในโครงการ:**

    - สัญญาโครงการ PSA ไปยัง Fin and Ops
    - โครงการ PSA ไปยัง Fin and Ops
    - รายการสัญญาโครงการ PSA ไปยัง Fin and Ops
    - เหตุการณ์สำคัญของรายการสัญญาโครงการ PSA ไปยัง Fin and Ops
  
### <a name="integrating-with-dynamics-365-project-service-automation-v3x"></a>การผสานรวมกับ Dynamics 365 Project Service Automation v3.x
มีการเปลี่ยนแปลงเค้าร่างใน Project Service Automation ซึ่งส่งผลกระทบต่อเท็มเพลตเหตุการณ์สำคัญของรายการสัญญาของโครงการและการใช้รุ่น v2 ของเท็มเพลตที่ต้องใช้เพื่อรวม Project Service Automation v3.x กับ Dynamics 365

- **ชื่อของเท็มเพลตในการรวมข้อมูล:** โครงการและสัญญา (PSA 3.x ไปยัง Fin and Ops) - v2
- **ชื่อของงานในโครงการ:**

    - สัญญาโครงการ PSA ไปยัง Fin and Ops
    - โครงการ PSA ไปยัง Fin and Ops
    - รายการสัญญาโครงการ PSA ไปยัง Fin and Ops
    - เหตุการณ์สำคัญของรายการสัญญาโครงการ PSA ไปยัง Fin and Ops

ก่อนที่การซิงโครไนส์ของสัญญาโครงการและโครงการจะสามารถเกิดขึ้นได้ คุณต้องซิงโครไนส์บัญชี

## <a name="entity-set"></a>การตั้งค่าเอนทิตี้

| Project Service Automation       | การเงิน                                                |
|----------------------------------|--------------------------------------------------------|
| ใบสั่ง                           | เอนทิตี้การรวมสำหรับสัญญาของโครงการ                |
| โครงการ                         | เอนทิตี้การรวมสำหรับโครงการ                         |
| รายการใบสั่ง                      | เอนทิตี้การรวมสำหรับรายการสัญญาของโครงการ           |
| เหตุการณ์สำคัญของรายการสัญญาของโครงการ | เอนทิตี้การรวมสำหรับเหตุการณ์สำคัญของรายการสัญญาของโครงการ |

## <a name="entity-flow"></a>ขั้นตอนเอนทิตี้

มีการจัดการสัญญาโครงการใน Project Service Automation และจะมีการซิงโครไนส์ไปยัง Finance เป็นสัญญาโครงการ ในฐานะที่เป็นส่วนหนึ่งของเท็มเพลตการรวม คุณสามารถกำหนดแหล่งที่มารวมใน Finance สำหรับสัญญาโครงการได้

มีการจัดการโครงการเวลาและวัสดุและโครงการที่มีราคาคงที่ใน Project Service Automation และมีการซิงโครไนส์ไปยัง Finance เป็นโครงการ ในฐานะที่เป็นส่วนหนึ่งของการรวมเท็มเพลต คุณสามารถกำหนดแหล่งที่มารวมใน Finance สำหรับโครงการได้

มีการจัดการรายการสัญญาโครงการใน Project Service Automation และมีการซิงโครไนส์ไปยัง Finance เป็นกฎการเรียกเก็บเงินสำหรับสัญญาโครงการ ถ้าวิธีการเรียกเก็บเงินแตกต่างจากชนิดโครงการเริ่มต้น การซิงโครไนส์จะปรับปรุงชนิดโครงการสำหรับโครงการรายการในสัญญาและกลุ่มโครงการ

มีการจัดการเหตุการณ์สำคัญของรายการสัญญาของโครงการใน Project Service Automation และมีการซิงโครไนส์ไปยัง Finance เป็นเหตุการณ์สำคัญของกฎการเรียกเก็บเงินสำหรับสัญญาโครงการ

## <a name="project-service-automation-to-finance-integration-solution"></a>Project Service Automation ไปยัง Finance intergration solution

ฟิลด์ **รหัสสัญญาโครงการ** จะพร้อมใช้งานบนหน้า **สัญญาโครงการ** ฟิลด์นี้ได้ถูกทำให้เป็นคีย์เฉพาะและธรรมชาติ เพื่อสนับสนุนการรวม

เมื่อมีการสร้างสัญญาโครงการใหม่ ถ้าค่า **รหัสสัญญาโครงการ** ไม่ได้มีอยู่แล้ว ระบบจะสร้างขึ้นโดยอัตโนมัติโดยใช้ลำดับหมายเลข ค่าประกอบด้วย **ORD** ตามด้วยลำดับหมายเลขที่เพิ่มขึ้น แล้วจึงตามด้วยคำต่อท้ายหกอักขระ นี่คือตัวอย่าง: **ORD-01022-Z4M9Q0**

ฟิลด์ **หมายเลขโครงการ** จะพร้อมใช้งานบนหน้า **โครงการ** ฟิลด์นี้ได้ถูกทำให้เป็นคีย์เฉพาะและธรรมชาติ เพื่อสนับสนุนการรวม

เมื่อมีการสร้างโครงการใหม่ ถ้าค่า **หมายเลขโครงการ** ไม่ได้มีอยู่แล้ว ระบบจะสร้างขึ้นโดยอัตโนมัติโดยใช้ลำดับหมายเลข ค่าประกอบด้วย **PRJ** ตามด้วยลำดับหมายเลขที่เพิ่มขึ้น แล้วจึงตามด้วยคำต่อท้ายหกอักขระ นี่คือตัวอย่าง: **PRJ-01049-CCNID0**

เมื่อมีการใช้ Project Service Automation ไปยัง Finance integration solution สคริปต์การอัพเกรดจะตั้งค่าฟิลด์ **รหัสสัญญาโครงการ** สำหรับสัญญาโครงการที่มีอยู่ และฟิลด์ **หมายเลขโครงการ** สำหรับโครงการที่มีอยู่ใน Project Service Automation

## <a name="prerequisites-and-mapping-setup"></a>การตั้งค่าการแม็ปและข้อกำหนดเบื้องต้น

- ก่อนที่การซิงโครไนส์ของสัญญาโครงการและโครงการจะสามารถเกิดขึ้นได้ คุณต้องซิงโครไนส์บัญชี
- ในชุดการเชื่อมต่อของคุณ เพิ่มการแม็ปฟิลด์คีย์รวมสำหรับ **msdyn\_organizationalunits** ไปยัง **msdyn\_ชื่อ \[ชื่อ\]** อันดับแรก คุณอาจต้องเพิ่มโครงการไปยังชุดของการเชื่อมต่อ สำหรับข้อมูลเพิ่มเติม ดู [รวมข้อมูลลงใน Common Data Service สำหรับแอป](https://docs.microsoft.com/powerapps/administrator/data-integrator)
- ในชุดการเชื่อมต่อของคุณ เพิ่มการแม็ปฟิลด์คีย์รวมสำหรับ **msdyn\_โครงการ** ไปยัง **msdynce\_projectnumber \[หมายเลขโครงการ\]** อันดับแรก คุณอาจต้องเพิ่มโครงการไปยังชุดของการเชื่อมต่อ สำหรับข้อมูลเพิ่มเติม ดู [รวมข้อมูลลงใน Common Data Service สำหรับแอป](https://docs.microsoft.com/powerapps/administrator/data-integrator)
- **SourceDataID** สำหรับสัญญาโครงการและโครงการ สามารถปรับปรุงเป็นค่าอื่น หรือลบออกจากการแม็ปได้ ค่าเท็มเพลตเริ่มต้นคือ **Project Service Automation**
- การแม็ป **PaymentTerms** ต้องถูกปรับปรุง เพื่อให้สะท้อนถึงเงื่อนไขที่ถูกต้องของการชำระเงินใน Finance คุณยังสามารถลบการแม็ปจากภารกิจของโครงการได้ด้วย แม็ปค่าเริ่มต้นมีค่าเริ่มต้นสำหรับข้อมูลสาธิต ตารางต่อไปนี้แสดงค่าใน Project Service Automation

    | มูลค่า | คำอธิบาย   |
    |-------|---------------|
    | 1     | สุทธิ 30        |
    | 2     | 2% 10, สุทธิ 30 |
    | 3     | สุทธิ 45        |
    | 4     | สุทธิ 60        |

## <a name="power-query"></a>Power Query

คุณต้องใช้ Microsoft Power Query for Excel เพื่อกรองข้อมูล ถ้าเป็นไปตามเงื่อนไขต่อไปนี้:

- คุณมีใบสั่งขายใน Dynamics 365 Sales
- คุณมีหน่วยงานขององค์กรหลายหน่วยใน Project Service Automation และหน่วยงานขององค์กรเหล่านี้จะถูกแม็ปกับนิติบุคคลหลายรายใน Finance

ถ้าคุณต้องใช้ Power Query ให้ทำตามคำแนะนำเหล่านี้:

- เท็มเพลตโครงการและสัญญา (PSA ไปยัง Fin and Ops) มีตัวกรองเริ่มต้นที่รวมเฉพาะใบสั่งขายของชนิด **รายการงาน (msdyn\_ordertype = 192350001)** ตัวกรองข้อมูลนี้ช่วยรับประกันว่า จะไม่มีการสร้างสัญญาโครงการสำหรับใบสั่งขายใน Finance ถ้าคุณสร้างเท็มเพลตของคุณเอง คุณต้องเพิ่มตัวกรองนี้
- คุณต้องสร้างตัวกรอง Power Query ที่รวมเฉพาะองค์กรในสัญญาที่ควรถูกซิงโครไนส์กับนิติบุคคลของชุดการเชื่อมต่อแบบรวม ตัวอย่างเช่น โครงการสัญญาที่คุณมีกับหน่วยงานในองค์กรในสัญญาของ Contoso US ควรถูกซิงโครไนส์กับนิติบุคคลที่ USSI แต่สัญญาโครงการที่คุณมีกับหน่วยงานในองค์กรในสัญญาของ Contoso Global ควรถูกซิงโครไนส์กับนิติบุคคล USMF ถ้าคุณไม่เพิ่มตัวกรองข้อมูลนี้ไปยังการแม็ปงานของคุณ สัญญาโครงการทั้งหมดจะถูกซิงโครไนส์กับนิติบุคคลที่กำหนดไว้สำหรับชุดการเชื่อมต่อ โดยไม่คำนึงถึงหน่วยงานในองค์กรในสัญญา

## <a name="template-mapping-in-data-integration"></a>การแม็ปเท็มเพลตในการรวมข้อมูล

> [!NOTE] 
> ฟิลด์ **CustomerReference** **AddressCity** **AddressCountryRegionID** **AddressDescription** **AddressLine1** **AddressLine2** **AddressState** และ **AddressZipCode** ไม่ได้รวมอยู่ในการแม็ปค่าเริ่มต้นสำหรับสัญญาโครงการ คุณสามารถเพิ่มการแม็ปได้ หากคุณต้องการให้ข้อมูลนี้ถูกซิงโครไนส์สำหรับสัญญาโครงการ
>
> ฟิลด์ **คำอธิบาย** **ParentID** **ProjectGroup** **ProjectManagerPersonnelNumber** และ **ProjectType** ไม่ได้รวมอยู่ในการแม็ปค่าเริ่มต้นสำหรับโครงการ คุณสามารถเพิ่มการแม็ปได้ หากคุณต้องการให้ข้อมูลนี้ถูกซิงโครไนส์สำหรับโครงการ

ภาพประกอบต่อไปนี้แสดงตัวอย่างของการแม็ปงานเท็มเพลตในการรวมข้อมูล การแม็ปแสดงข้อมูลฟิลด์ที่จะถูกซิงโครไนส์จาก Project Service Automation ไปยัง Finance

[![การแม็ปเท็มเพลต](./media/ProjectContractTemplateMapping.JPG)](./media/ProjectContractTemplateMapping.JPG)

[![การแม็ปเท็มเพลต](./media/ProjectTemplateMapping.JPG)](./media/ProjectTemplateMapping.JPG)

[![การแม็ปเท็มเพลต](./media/ProjectContractLinesMapping.JPG)](./media/ProjectContractLinesMapping.JPG)

[![การแม็ปเท็มเพลต](./media/ProjectContractLineMilestonesMapping.JPG)](./media/ProjectContractLineMilestonesMapping.JPG)

#### <a name="project-contract-line-milestone-mapping-in-the-projects-and-contracts-psa-3x-to-dynamics---v2-template"></a>การแม็ปเหตุการณ์ของบรรทัดสัญญาโครงการในโครงการและสัญญา (PSA 3.x x เป็น Dynamics)-เท็มเพลต v2:

[![การแม็ปเท็มเพลต](./media/ProjectContractLineMilestoneMapping_v2.jpg)](./media/ProjectContractLineMilestoneMapping_v2.jpg)
