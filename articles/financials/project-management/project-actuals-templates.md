---
title: "ซิงโครไนส์รายการจริงของโครงการจาก Project Service Automation โดยตรงไปยังสมุดรายวันการรวมโครงการสำหรับการลงรายการบัญชีใน Finance and Operations"
description: "หัวข้อนี้อธิบายเท็มเพลตและงานพื้นฐานที่จะใช้ในการซิงโครไนส์รายการจริงของโครงการโดยตรงจาก Microsoft Dynamics 365 for Project Service Automation ไปยัง Dynamics 365 for Finance and Operations"
author: KimANelson
manager: AnnBe
ms.date: 05/21/2018
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
ms.sourcegitcommit: bd8feff598cf80ca675c7d2b5dda636799b19e29
ms.openlocfilehash: 85ff049852e0b00623f47a12fb66e2c9bb9c4151
ms.contentlocale: th-th
ms.lasthandoff: 05/29/2018

---
# <a name="synchronize-project-actuals-from-project-service-automation-directly-to-the-project-integration-journal-for-posting-in-finance-and-operations"></a>ซิงโครไนส์รายการจริงของโครงการจาก Project Service Automation โดยตรงไปยังสมุดรายวันการรวมโครงการสำหรับการลงรายการบัญชีใน Finance and Operations

หัวข้อนี้อธิบายเท็มเพลตและงานพื้นฐานที่จะใช้ในการซิงโครไนส์รายการจริงของโครงการโดยตรงจาก Microsoft Dynamics 365 for Project Service Automation ไปยัง Dynamics 365 for Finance and Operations

เท็มเพลตซิงค์ธุรกรรมจาก Project Service Automation ลงในตารางการจัดเตรียมใน Finance and Operations หลังจากการซิงโครไนส์เสร็จสมบูรณ์ คุณต้องนำเข้าจากตารางการจัดเตรียมลงในสมุดรายวันการรวม

> [!NOTE]
> การรวมรายการจริงของโครงการจะพร้อมใช้งานใน Dynamics 365 for Finance and Operations รุ่น 8.01

> [!NOTE]
> ถ้าคุณกำลังป้อนยอดภาษีขายในธุรกรรมเวลาหรือค่าใช้จ่ายใน Project Service Automation คุณต้องติดตั้ง Project Service Automation การอัพเดต 7 ถ้าไม่ได้ติดตั้งการอัพเดตนี้ ภาษีจริงจะไม่สามารถเชื่อมโยงกับเวลาที่เชื่อมโยงหรือค่าใช้จ่ายจริงได้ และจะไม่มีการซิงค์กับ Finance and Operations ติดต่อฝ่ายสนับสนุนสำหรับข้อมูลเพิ่มเติม


## <a name="data-flow-for-project-service-automation-to-finance-and-operations"></a>โฟลว์ข้อมูลสำหรับ Project Service Automation ไปยัง Finance and Operations

โซลูชันการรวม Project Service Automation ไปยัง Finance and Operations ใช้คุณลักษณะการรวมข้อมูล เพื่อซิงโครไนส์ข้อมูลระหว่างอินสแตนซ์ของ Project Service Automation และ Finance and Operations เท็มเพลตการรวมที่พร้อมใช้งานกับคุณลักษณะการรวมข้อมูล เปิดใช้งานโฟลว์ของข้อมูลเกี่ยวกับรายการจริงของโครงการจาก Project Service Automation ไปยัง Finance and Operations

ภาพประกอบต่อไปนี้แสดงวิธีการซิงโครไนส์ข้อมูลระหว่าง Project Service Automation และ Finance and Operations

[![โฟลว์ข้อมูลสำหรับการรวม Project Service Automation กับ Finance and Operations](./media/ProjectActualsFlow.jpg)](./media/ProjectActualsFlow.jpg)


## <a name="templates-and-tasks"></a>เท็มเพลตและงาน

เมื่อต้องการเข้าถึงเท็มเพลตที่พร้อมใช้งาน ในศูนย์การจัดการ Microsoft PowerApps เลือก **โครงการ** และจากนั้น ในมุมบนด้านขวา เลือก **โครงการใหม่** เพื่อเลือกเท็มเพลตสาธารณะ

เท็มเพลตและงานพื้นฐานต่อไปนี้จะถูกใช้ในการซิงโครไนส์รายการจริงของโครงการจาก Project Service Automation ไปยัง Finance and Operations:

-  **ชื่อของเท็มเพลตในการรวมข้อมูล:** รายการจริงของโครงการ (PSA ไปยัง Fin and Ops)

-  **ชื่อของงานในโครงการ:** 
    - จริง 
    - TransactionConnections

## <a name="entity-set"></a>การตั้งค่าเอนทิตี้

| Project Service Automation      | Finance and Operations                                      |
|---------------------------------|-------------------------------------------------------------|
| จริง                         | เอนทิตี้การรวมสำหรับการนำเข้าจริงของโครงการ                      |
| การเชื่อมต่อธุรกรรม         | เอนทิตี้การรวมสำหรับความสัมพันธ์ของธุรกรรมของโครงการ    |

## <a name="entity-flow"></a>ขั้นตอนเอนทิตี้

มีการจัดการรายการจริงของโครงการใน Project Service Automation และมีการซิงโครไนส์ไปยัง Finance and Operations ไปที่สมุดรายวันการรวมของโครงการ การลงบัญชีจะถูกใช้โดยขึ้นอยู่กับการตั้งค่าการลงรายการบัญชีและมิติทางการเงินเริ่มต้น

## <a name="preconditions"></a>เงื่อนไขเบื้องต้น

ก่อนที่การซิงโครไนส์ของรายการจริงจะเกิดขึ้นได้ คุณต้องตั้งค่าคอนฟิกพารามิเตอร์การรวม Project Service Automation และซิงโครไนส์โครงการ งานโครงการ และประเภทธุรกรรมค่าใช้จ่ายโครงการ

## <a name="power-query"></a>Power Query

คุณต้องใช้ Microsoft Power Query ในเท็มเพลตรายการจริงของโครงการกับ:
- แปลง Project Service Automation **ชนิดของธุรกรรม** เป็น **ชนิดของธุรกรรม** ที่ถูกต้องใน Finance and Operations เท็มเพลตรายการจริงของโครงการ (PSA ไปยัง Fin and Ops) ได้กำหนดการแปลงนี้แล้ว
- แปลง Project Service Automation **ชนิดของการเรียกเก็บเงิน** เป็น **ชนิดของการเรียกเก็บเงิน** ที่ถูกต้องใน Finance and Operations เท็มเพลตรายการจริงของโครงการ (PSA ไปยัง Fin and Ops) ได้กำหนดการแปลงนี้แล้ว จากนั้น ชนิดการเรียกเก็บเงินจะถูกแม็ปไปยัง **ลักษณะของรายการ** ตามการตั้งค่าคอนฟิกในแบบฟอร์มพารามิเตอร์การรวม Dynamics 365 for Project Service Automation
- กรองเฉพาะ **หน่วยงานในองค์กรทรัพยากร** ที่จะถูกซิงค์กับเท็มเพลตนี้
- ถ้า **รายการจริงของเวลาระหว่างบริษัทหรือค่าใช้จ่ายระหว่างบริษัท** จะถูกซิงค์กับ Finance and Operations คุณต้องแปลง **หน่วยงานในองค์กรในสัญญา** เป็น **นิติบุคคล** ที่ถูกต้องใน Finance and Operations เท็มเพลตรายการจริงของโครงการ (PSA ไปยัง Fin and Ops) มีคอลัมน์ที่เป็นเงื่อนไขที่กำหนดโดยยึดตามข้อมูลสาธิต คุณต้องอัพเดตคอลัมน์เงื่อนไขที่แทรกล่าสุดไปยังนิติบุคคลที่ถูกต้อง ความล้มเหลวในการทำเช่นนี้อาจส่งผลให้มีข้อผิดพลาดในการรวม หรือธุรกรรมจริงที่ไม่ถูกต้องซึ่งนำเข้าไปยัง Finance and Operations
- ถ้า **รายการจริงของเวลาระหว่างบริษัทหรือค่าใช้จ่ายระหว่างบริษัท** จะไม่ถูกซิงค์กับ Finance and Operations คุณต้องลบคอลัมน์เงื่อนไขที่แทรกล่าสุดจากเท็มเพลตของคุณ ความล้มเหลวในการทำเช่นนี้อาจส่งผลให้มีข้อผิดพลาดในการรวม หรือธุรกรรมจริงที่ไม่ถูกต้องซึ่งนำเข้าไปยัง Finance and Operations

### <a name="contract-organizational-unit"></a>หน่วยงานในองค์กรในสัญญา
ในการอัพเดตคอลัมน์เงื่อนไขที่แทรกในเท็มเพลต คลิกที่ลูกศร **แม็ป** เพื่อเปิดการแม็ป เลือกที่จะเปิดการกรองข้อมูลและแบบสอบถามขั้นสูง
- ถ้าคุณกำลังใช้เท็มเพลตรายการจริงของ Microsoft Project เริ่มต้น (PSA ไปยัง Fin and Ops) เลือกส่วน **เงื่อนไขที่แทรก** lasat ในส่วน **ขั้นตอนที่ใช้** ในรายการ **ฟังก์ชัน** แทนที่ **USSI** ด้วยชื่อของ **นิติบุคคล** ที่ควรจะใช้กับการรวม เพิ่มเงื่อนไขเพิ่มเติมตามความจำเป็นไปยังรายการ **ฟังก์ชัน** และปรับปรุงเงื่อนไข **อื่น** จาก **USMF** เพื่อแก้ไข **นิติบุคคล**
- ถ้าคุณกำลังสร้างเท็มเพลตใหม่ คุณต้องเพิ่มคอลัมน์นี้เพื่อสนับสนุนเวลาและค่าใช้จ่ายระหว่างบริษัท เลือก **เพิ่มคอลัมน์แบบมีเงื่อนไข** และตั้งชื่อคอลัมน์ เช่น LegalEntity ป้อนเงื่อนไขสำหรับคอลัมน์ ที่ซึ่งถ้า msdyn_contractorganizationalunitid.msdyn_name เป็น <organizational unit> แล้ว <enter the Legal entity>; อื่นๆ เป็น null

## <a name="template-mapping-in-data-integration"></a>การแม็ปเท็มเพลตในการรวมข้อมูล

ภาพประกอบต่อไปนี้แสดงตัวอย่างของการแม็ปงานเท็มเพลตในการรวมข้อมูล การแม็ปแสดงข้อมูลฟิลด์ที่จะถูกซิงโครไนส์จาก Project Service Automation ไปยัง Finance and Operations

[![การแม็ปเท็มเพลต](./media/ActualsMapping.jpg)](./media/ActualsMapping.jpg)

[![การแม็ปเท็มเพลต](./media/TransactionConnections.jpg)](./media/TransactionConnections.jpg)

## <a name="import-from-staging-table"></a>นำเข้าจากตารางการแบ่งระยะ

การนำเข้าจากตารางการจัดเตรียม กระบวนการประจำงวดต้องถูกรันหลังจากการซิงโครไนส์ของรายการจริงจาก Project Service Automation ไปยัง Finance and Operations กระบวนการนี้จะนำเข้าธุรกรรมโครงการจากตารางการจัดเตรียมไปยังสมุดรายวันการรวม Project Service Automation ที่มีการใช้การลงบัญชี และสามารถลงรายบัญชีธุรกรรมที่นำเข้าได้ ขอแนะนำให้คุณรันกระบวนการนี้ในโหมดชุดงาน และอาจเลือกที่จะถูกตั้งค่าให้รันเป็นชุดงานที่เกิดซ้ำ

## <a name="update-actuals"></a>อัพเดตรายการจริง

เท็มเพลตและงานพื้นฐานต่อไปนี้จะถูกใช้ในการซิงโครไนส์หมายเลขใบสำคัญและภาษีขายสำหรับธุรกรรมโครงการที่ลงรายการบัญชีจาก Finance and Operations ไปยัง Project Service Automation:

-  **ชื่อของเท็มเพลตในการรวมข้อมูล:** การอัพเดตรายการจริงของโครงการ (Fin Ops ไปยัง PSA)
-  **ชื่อของงานในโครงการ:** 
     - จริง 
     - TransactionConnections

## <a name="entity-set"></a>การตั้งค่าเอนทิตี้

| Finance and Operations                                         | Project Service Automation        |
|----------------------------------------------------------------|-----------------------------------|
| เอนทิตี้การรวมสำหรับการนำเข้าจริงของโครงการ                         | จริง                           |
| เอนทิตี้การรวมสำหรับความสัมพันธ์ของธุรกรรมของโครงการ       | การเชื่อมต่อธุรกรรม           |

## <a name="entity-flow"></a>ขั้นตอนเอนทิตี้

มีการจัดการรายการจริงของโครงการใน Project Service Automation และมีการซิงโครไนส์ไปยัง Finance and Operations ไปที่สมุดรายวันการรวมของโครงการ หลังจากที่ลงรายการบัญชีใน Finance and Operations มีการปรับปรุงรายการจริงใน Project Service Automation ที่มีหมายเลขใบสำคัญจาก Finance and Operations ถ้าภาษีขายถูกเพิ่มลงใน Finance and Operations รายการจริงของภาษีใหม่จะถูกสร้างใน PRoject Service Automation

## <a name="power-query"></a>Power Query

คุณต้องใช้ Microsoft Power Query ในเท็มเพลตการอัพเดตรายการจริงของโครงการกับ:
- แปลง Finance and Operations **ชนิดของธุรกรรม** เป็น **ชนิดของธุรกรรม** ที่ถูกต้องใน Project Service Automation เท็มเพลตการอัพเดตรายการจริงของโครงการ (Fin Ops ไปยัง PSA) ได้กำหนดการแปลงนี้แล้ว
- แปลง Finance and Operations **ชนิดของการเรียกเก็บเงิน** เป็น **ชนิดของการเรียกเก็บเงิน** ที่ถูกต้องใน Project Service Automation เท็มเพลตการอัพเดตรายการจริงของโครงการ (Fin Ops ไปยัง PSA) ได้กำหนดการแปลงนี้แล้ว

## <a name="template-mapping-in-data-integration"></a>การแม็ปเท็มเพลตในการรวมข้อมูล

ภาพประกอบต่อไปนี้แสดงตัวอย่างของการแม็ปงานเท็มเพลตในการรวมข้อมูล การแม็ปแสดงข้อมูลฟิลด์ที่จะถูกซิงโครไนส์จาก Finance and Operations ไปยัง Project Service Automation

[![การแม็ปเท็มเพลต](./media/ActualsUpdateMapping.jpg)](./media/ActualsUpdateMapping.jpg)

[![การแม็ปเท็มเพลต](./media/TransactionConnectionsUpdate.jpg)](./media/TransactionConnectionsUpdate.jpg)




