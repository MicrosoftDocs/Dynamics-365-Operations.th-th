---
title: ซิงโครไนส์รายการจริงของโครงการโดยตรงจาก Project Service Automation ไปยังสมุดรายวันการรวมโครงการสำหรับการลงรายการบัญชีใน Finance and Operations
description: หัวข้อนี้อธิบายเท็มเพลตและงานพื้นฐานที่ใช้ในการทำให้ข้อมูลมูลค่าจริงของโครงการจาก Microsoft Dynamics 365 for Project Service Automation ไปยัง Microsoft Dynamics 365 for Finance and Operations ตรงกันโดยตรง
author: KimANelson
manager: AnnBe
ms.date: 07/20/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 87983
ms.assetid: b454ad57-2fd6-46c9-a77e-646de4153067
ms.search.region: Global
ms.author: knelson
ms.search.validFrom: 2016-11-28
ms.dyn365.ops.version: AX 7.3.0
ms.openlocfilehash: 0a965e8de596decf39a15977e6df8a6aa9dd35b0
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 05/15/2019
ms.locfileid: "1571111"
---
# <a name="synchronize-project-actuals-directly-from-project-service-automation-to-the-project-integration-journal-for-posting-in-finance-and-operations"></a>ซิงโครไนส์รายการจริงของโครงการโดยตรงจาก Project Service Automation ไปยังสมุดรายวันการรวมโครงการสำหรับการลงรายการบัญชีใน Finance and Operations

[!include[banner](../includes/banner.md)]

หัวข้อนี้อธิบายเท็มเพลตและงานพื้นฐานที่ใช้ในการทำให้ข้อมูลมูลค่าจริงของโครงการจาก Microsoft Dynamics 365 for Project Service Automation ไปยัง Microsoft Dynamics 365 for Finance and Operations ตรงกันโดยตรง

เท็มเพลตซิงโครไนส์ธุรกรรมจาก Project Service Automation ลงในตารางการจัดเตรียมใน Finance and Operations หลังจากการซิงโครไนส์เสร็จสมบูรณ์ คุณ **ต้อง** นำเข้าข้อมูลจากตารางการจัดเตรียมลงในสมุดรายวันการรวม

> [!NOTE]
> - การรวมมูลค่าจริงของโครงการพร้อมใช้งานใน Microsoft Dynamics 365 for Finance and Operations รุ่น 8.0.1 หรือใหม่กว่า
> - ถ้าคุณกำลังใช้ Microsoft Dynamics 365 for Finance and Operations, Enterprise Edition 7.3.0 หลังจากที่คุณติดตั้ง KB 4132657 และ KB 4132660 คุณจะสามารถใช้เท็มเพลตเพื่อรวมงานโครงการ ค่าใช้จ่ายประเภทธุรกรรม การประเมินชั่วโมง การประเมินค่าใช้จ่าย และค่าที่เกิดขึ้นจริงได้ และสามารถตั้งค่าคอนฟิกการล็อคฟังก์ชันได้ ถ้าคุณต้องตั้งค่าการกระจายการลงบัญชี เราขอแนะนำให้ คุณติดตั้ง KB 4131710 ด้วย
> - ถ้าคุณกำลังใช้ Finance and Operations 7.3.0 และคุณกำลังนำธุรกรรมค่าธรรมเนียมมาจาก Project Service Automation คุณต้องติดตั้ง KB 4345320 เพื่อรวมค่าธรรมเนียมดังกล่าวในใบแจ้งหนี้โครงการ
> - ถ้าคุณกำลังป้อนยอดภาษีขายในธุรกรรมเวลาหรือค่าใช้จ่ายใน Project Service Automation คุณต้องติดตั้ง Project Service Automation Update 7 มิฉะนั้น ภาษีจริงจะไม่สามารถเชื่อมโยงกับเวลาที่เชื่อมโยงหรือค่าใช้จ่ายจริงได้ และจะไม่มีการซิงค์กับ Finance and Operations สำหรับข้อมูลเพิ่มเติม ติดต่อฝ่ายสนับสนุน

## <a name="data-flow-for-project-service-automation-to-finance-and-operations"></a>โฟลว์ข้อมูลสำหรับ Project Service Automation ไปยัง Finance and Operations

โซลูชันการรวม Project Service Automation ไปยัง Finance and Operations ใช้คุณลักษณะการรวมข้อมูล เพื่อซิงโครไนส์ข้อมูลระหว่างอินสแตนซ์ของ Project Service Automation และ Finance and Operations เท็มเพลตการรวมที่พร้อมใช้งานกับคุณลักษณะการรวมข้อมูล เปิดใช้งานโฟลว์ของข้อมูลเกี่ยวกับรายการจริงของโครงการจาก Project Service Automation ไปยัง Finance and Operations

ภาพประกอบต่อไปนี้แสดงวิธีการซิงโครไนส์ข้อมูลระหว่าง Project Service Automation และ Finance and Operations

[![โฟลว์ข้อมูลสำหรับการรวม Project Service Automation กับ Finance and Operations](./media/ProjectActualsFlow.jpg)](./media/ProjectActualsFlow.jpg)

## <a name="project-actuals-from-project-service-automation"></a>รายการจริงของโครงการจาก Project Service Automation

### <a name="template-and-tasks"></a>เท็มเพลตและงาน

เพื่อเข้าถึงเท็มเพลตที่พร้อมใช้งาน ในศูนย์การจัดการ Microsoft PowerApps เลือก **โครงการ** และจากนั้น ที่มุมขวาบน เลือก **โครงการใหม่** เพื่อเลือกเท็มเพลตสาธารณะ

เท็มเพลตและงานพื้นฐานต่อไปนี้จะถูกใช้ในการซิงโครไนส์รายการจริงของโครงการจาก Project Service Automation ไปยัง Finance and Operations:

- **ชื่อของเท็มเพลตในการรวมข้อมูล:** รายการจริงของโครงการ (PSA ไปยัง Fin and Ops)
- **ชื่อของงานในโครงการ:**

    - จริง
    - TransactionConnections

### <a name="entity-set"></a>การตั้งค่าเอนทิตี้

| Project Service Automation | Finance and Operations                                   |
|----------------------------|----------------------------------------------------------|
| จริง                    | เอนทิตี้การรวมสำหรับการนำเข้าจริงของโครงการ                   |
| การเชื่อมต่อธุรกรรม    | เอนทิตี้การรวมสำหรับความสัมพันธ์ของธุรกรรมของโครงการ |

### <a name="entity-flow"></a>ขั้นตอนเอนทิตี้

มีการจัดการรายการจริงของโครงการใน Project Service Automation และมีการซิงโครไนส์ไปยังสมุดรายวันการรวมของโครงการใน Finance and Operations การบัญชีจะถูกใช้โดยขึ้นอยู่กับการตั้งค่าการลงรายการบัญชีและมิติทางการเงินเริ่มต้น

### <a name="prerequisites"></a>ข้อกำหนดเบื้องต้น

ก่อนที่การซิงโครไนส์ของรายการจริงจะเกิดขึ้นได้ คุณต้องตั้งค่าคอนฟิกพารามิเตอร์การรวม Project Service Automation และซิงโครไนส์โครงการ งานโครงการ และประเภทธุรกรรมค่าใช้จ่ายโครงการ

### <a name="power-query"></a>Power Query

ในเท็มเพลตรายการจริงของโครงการ คุณต้องใช้ Microsoft Power Query for Excel เพื่อทำให้งานเหล่านี้เสร็จสมบูรณ์:

- แปลงชนิดของธุรกรรมใน Project Service Automation เป็นชนิดของธุรกรรมที่ถูกต้องใน Finance and Operations มีการกำหนดการแปลงนี้ในเท็มเพลตรายการจริงของโครงการ (PSA ไปยัง Fin and Ops)
- แปลงชนิดของการเรียกเก็บเงินใน Project Service Automation เป็นชนิดของการเรียกเก็บเงินที่ถูกต้องใน Finance and Operations มีการกำหนดการแปลงนี้ในเท็มเพลตรายการจริงของโครงการ (PSA ไปยัง Fin and Ops) จากนั้น ชนิดการเรียกเก็บเงินจะถูกแม็ปไปยังลักษณะของรายการตามการตั้งค่าคอนฟิกในหน้า **พารามิเตอร์การรวม Project Service Automation**
- กรองหน่วยงานในองค์กรของทรัพยากรเฉพาะที่จะถูกซิงโครไนส์กับเท็มเพลตนี้
- ถ้ารายการจริงของเวลาระหว่างบริษัทหรือค่าใช้จ่ายระหว่างบริษัท จะถูกซิงโครไนส์กับ Finance and Operations คุณต้องแปลงหน่วยงานในองค์กรในสัญญาเป็นนิติบุคคลที่ถูกต้องใน Finance and Operations ในเท็มเพลตรายการจริงของโครงการ (PSA ไปยัง Fin and Ops) คอลัมน์ที่เป็นเงื่อนไขถูกกำหนดโดยยึดตามข้อมูลสาธิต คุณต้องอัพเดตคอลัมน์แบบมีเงื่อนไขที่แทรกล่าสุดไปยังนิติบุคคลที่ถูกต้อง มิฉะนั้น ความล้มเหลวในการรวมอาจผิดพลาด หรือธุรกรรมจริงที่ไม่ถูกต้องอาจถูกนำเข้าไปยัง Finance and Operations อย่างใดอย่างหนึ่ง
- ถ้ารายการจริงของเวลาระหว่างบริษัทหรือค่าใช้จ่ายระหว่างบริษัท จะไม่ถูกซิงโครไนส์กับ Finance and Operations คุณต้องลบคอลัมน์แบบมีเงื่อนไขที่แทรกล่าสุดจากเท็มเพลตของคุณ มิฉะนั้น ความล้มเหลวในการรวมอาจผิดพลาด หรือธุรกรรมจริงที่ไม่ถูกต้องอาจถูกนำเข้าไปยัง Finance and Operations อย่างใดอย่างหนึ่ง

#### <a name="contract-organizational-unit"></a>หน่วยงานในองค์กรในสัญญา
ในการอัพเดตคอลัมน์แบบมีเงื่อนไขที่แทรกในเท็มเพลต คลิกที่ลูกศร **แม็ป** เพื่อเปิดการแม็ป เลือกลิงก์ **การกรองข้อมูลและแบบสอบถามขั้นสูง** เพื่อเปิด Power Query

- ถ้าคุณกำลังใช้เท็มเพลตรายการจริงของโครงการเริ่มต้น (PSA ไปยัง Fin and Ops) ใน Power Query เลือกส่วน **เงื่อนไขที่แทรก** ล่าสุด จากส่วน **ขั้นตอนที่ใช้** ในรายการ **ฟังก์ชัน** แทนที่ **USSI** ด้วยชื่อของนิติบุคคลที่ควรจะใช้กับการรวม เพิ่มเงื่อนไขเพิ่มเติมไปยังรายการ **ฟังก์ชัน** ตามที่คุณต้องการ และปรับปรุงเงื่อนไข **อื่น** จาก **USMF** เพื่อแก้ไขนิติบุคคล
- ถ้าคุณกำลังสร้างเท็มเพลตใหม่ คุณต้องเพิ่มคอลัมน์เพื่อสนับสนุนเวลาและค่าใช้จ่ายระหว่างบริษัท เลือก **เพิ่มคอลัมน์แบบมีเงื่อนไข** และป้อนชื่อสำหรับคอลัมน์ เช่น **LegalEntity** ป้อนเงื่อนไขสำหรับคอลัมน์ ที่ซึ่งถ้า **msdyn\_contractorganizationalunitid.msdyn\_ชื่อ** คือ \<หน่วยงาน\> แล้ว \<ป้อนนิติบุคคล\>; นอกจากนั้นเป็น null

### <a name="template-mapping-in-data-integration"></a>การแม็ปเท็มเพลตในการรวมข้อมูล

ภาพประกอบต่อไปนี้แสดงตัวอย่างของการแม็ปงานเท็มเพลตในการรวมข้อมูล การแม็ปแสดงข้อมูลฟิลด์ที่จะถูกซิงโครไนส์จาก Project Service Automation ไปยัง Finance and Operations

[![การแม็ปเท็มเพลต](./media/ActualsMapping.jpg)](./media/ActualsMapping.jpg)

[![การแม็ปเท็มเพลต](./media/TransactionConnections.jpg)](./media/TransactionConnections.jpg)

## <a name="import-from-staging-table-after-integration-from-project-service-automation"></a>นำเข้าจากตารางการจัดเตรียมหลังจากการรวมจาก Project Service Automation

การนำเข้าจากกระบวนการประจำงวดของตารางการจัดเตรียม ต้องถูกรันหลังจากการซิงโครไนส์ของรายการจริงจาก Project Service Automation ไปยัง Finance and Operations กระบวนการนี้จะนำเข้าธุรกรรมโครงการจากตารางการจัดเตรียมไปยังสมุดรายวันการรวม Project Service Automation ที่มีการใช้การลงบัญชี และสามารถลงรายบัญชีธุรกรรมที่นำเข้าได้ เราขอแนะนำให้คุณรันกระบวนการนี้ในโหมดชุดงาน และอาจเลือกที่จะถูกตั้งค่าให้รันเป็นชุดงานที่เกิดซ้ำ

## <a name="update-actuals-from-finance-and-operations"></a>ปรับปรุงรายการจริงจาก Finance and Operations

### <a name="template-and-tasks"></a>เท็มเพลตและงาน

เท็มเพลตและงานพื้นฐานต่อไปนี้จะถูกใช้ในการซิงโครไนส์หมายเลขใบสำคัญและภาษีขายสำหรับธุรกรรมโครงการที่ลงรายการบัญชีจาก Finance and Operations ไปยัง Project Service Automation:

- **ชื่อของเท็มเพลตในการรวมข้อมูล:** การอัพเดตรายการจริงของโครงการ (Fin Ops ไปยัง PSA)
- **ชื่อของงานในโครงการ:**

    - จริง 
    - TransactionConnections

### <a name="entity-set"></a>การตั้งค่าเอนทิตี้

| Finance and Operations                                   | Project Service Automation |
|----------------------------------------------------------|----------------------------|
| เอนทิตี้การรวมสำหรับการนำเข้าจริงของโครงการ                   | จริง                    |
| เอนทิตี้การรวมสำหรับความสัมพันธ์ของธุรกรรมของโครงการ | การเชื่อมต่อธุรกรรม    |

### <a name="entity-flow"></a>ขั้นตอนเอนทิตี้

มีการจัดการรายการจริงของโครงการใน Project Service Automation และมีการซิงโครไนส์ไปยังสมุดรายวันการรวมของโครงการใน Finance and Operations หลังจากที่ลงรายการบัญชีรายการจริงใน Finance and Operations จะมีการปรับปรุงใน Project Service Automation ที่มีหมายเลขใบสำคัญจาก Finance and Operations ถ้าภาษีขายถูกเพิ่มลงใน Finance and Operations รายการจริงของภาษีใหม่จะถูกสร้างใน Project Service Automation

### <a name="power-query"></a>Power Query

ในเท็มเพลตการปรับปรุงรายการจริงของโครงการ คุณต้องใช้ Power Query เพื่อทำให้งานเหล่านี้เสร็จสมบูรณ์:

- แปลงชนิดของธุรกรรมใน Finance and Operations เป็นชนิดของธุรกรรมที่ถูกต้องใน Project Service Automation มีการกำหนดการแปลงนี้แล้วในเท็มเพลตการปรับปรุงรายการจริงของโครงการ (Fin and Ops ไปยัง PSA)
- แปลงชนิดของการเรียกเก็บเงินใน Finance and Operations เป็นชนิดของการเรียกเก็บเงินที่ถูกต้องใน Project Service Automation มีการกำหนดการแปลงนี้แล้วในเท็มเพลตการปรับปรุงรายการจริงของโครงการ (Fin and Ops ไปยัง PSA)

### <a name="template-mapping-in-data-integration"></a>การแม็ปเท็มเพลตในการรวมข้อมูล

ภาพประกอบต่อไปนี้แสดงตัวอย่างของการแม็ปงานเท็มเพลตในการรวมข้อมูล การแม็ปแสดงข้อมูลฟิลด์ที่จะถูกซิงโครไนส์จาก Finance and Operations ไปยัง Project Service Automation

[![การแม็ปเท็มเพลต](./media/ActualsUpdateMapping.jpg)](./media/ActualsUpdateMapping.jpg)

[![การแม็ปเท็มเพลต](./media/TransactionConnectionsUpdate.jpg)](./media/TransactionConnectionsUpdate.jpg)
