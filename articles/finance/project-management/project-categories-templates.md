---
title: ปซิงโครไนส์ระเภทค่าใช้จ่ายโครงการระหว่าง Finance and Operations และ Project Service Automation
description: หัวข้อนี้อธิบายเท็มเพลตและงานพื้นฐานที่ใช้ซิงโครไนส์ประเภทค่าใช้จ่ายโครงการระหว่าง Microsoft Dynamics 365 Finance และ Dynamics 365 Project Service Automation
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
ms.dyn365.ops.version: AX 8.0.0
ms.openlocfilehash: 482febc91a04766216f9887ab59d30cc9aed5096
ms.sourcegitcommit: 2460d0da812c45fce67a061386db52e0ae46b0f3
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 09/30/2019
ms.locfileid: "2250518"
---
# <a name="synchronize-project-expense-categories-between-finance-and-operations-and-project-service-automation"></a>ปซิงโครไนส์ระเภทค่าใช้จ่ายโครงการระหว่าง Finance and Operations และ Project Service Automation

[!include[banner](../includes/banner.md)]

หัวข้อนี้อธิบายเท็มเพลตและงานพื้นฐานที่ใช้ในการทำให้ข้อมูลประเภทค่าใช้จ่ายโครงการระหว่าง Dynamics 365 Finance และ Dynamics 365 Project Service Automation ตรงกัน

> [!NOTE]
> - การรวมงานโครงการ ประเภทธุรกรรมค่าใช้จ่าย การประเมินชั่วโมง การประเมินค่าใช้จ่าย และการล็อคฟังก์ชันซึ่งพร้อมใช้งานในรุ่น 8.0
> - การรวมรายการจริงจะพร้อมใช้งานในรุ่น 8.0.1 หรือรุ่นที่ใหม่กว่า
> - ถ้าคุณกำลังใช้ Enterprise Edition 7.3.0 หลังจากที่คุณติดตั้ง KB 4132657 และ KB 4132660 คุณจะสามารถใช้เท็มเพลตเพื่อรวมงานโครงการ ค่าใช้จ่ายประเภทธุรกรรม การประเมินชั่วโมง การประเมินค่าใช้จ่าย และค่าที่เกิดขึ้นจริงได้และสามารถตั้งค่าคอนฟิกฟังก์ชันการล็อคได้ ถ้าคุณต้องตั้งค่าการกระจายการลงบัญชี เราขอแนะนำให้ คุณติดตั้ง KB 4131710 ด้วย

## <a name="data-flow-for-project-service-automation-and-finance"></a>โฟลว์ข้อมูลสำหรับ Project Service Automation และ Finance

Project Service Automation และ Finance integration solution ใช้คุณลักษณะการรวมข้อมูลเพื่อซิงโครไนส์ข้อมูลระหว่างอินสแตนซ์ของ Project Service Automation และ Finance เท็มเพลตการรวมที่พร้อมใช้งานกับคุณลักษณะการรวมข้อมูล เปิดใช้งานโฟลว์ของข้อมูลเกี่ยวกับประเภทธุรกรรมค่าใช้จ่ายของโครงการระหว่าง Finance และ Project Service Automation

ถ้าประเภทค่าใช้จ่ายโครงการเป็นต้นฉบับใน Finance ในตอนแรกโฟลว์การรวมมาจาก Finance ไปยัง Project Service Automation จากนั้น รหัสการรวมของระเภทค่าใช้จ่ายของโครงการถูกปรับปรุงผ่านทางการซิงโครไนส์จาก Project Service Automation ไปยัง Finance

ถ้าประเภทค่าใช้จ่ายโครงการเป็นต้นฉบับใน Project Service Automation ในตอนแรกโฟลว์การรวมมาจาก Project Service Automation ไปยัง Finance ประเภทโครงการต้องถูกตั้งค่าคอนฟิกใน Finance อยู่แล้ว ก่อนการซิงโครไนส์จาก Project Service Automation จากนั้น ซิงโครไนส์จาก Finance กลับไปยัง Project Service Automation และจากนั้นจาก Project Service Automation ไปยัง Finance อีกครั้ง ด้วยวิธีนี้ คุณช่วยรับประกันว่า ประเภทถูกเชื่อมโยง และไม่มีการสร้างข้อมูลซ้ำ

> [!NOTE]
> โดยทั่วไป ประเภทค่าใช้จ่ายโครงการเป็นต้นฉบับใน Finance อย่างไรก็ตาม ถ้าพวกเขาไม่ใช่ต้นฉบับใน Finance หรือถ้ามีการสร้างประเภทค่าใช้จ่ายใน Project Service Automation แล้ว อันดับแรก คุณต้องซิงโครไนส์โดยใช้เท็มเพลตประเภทธุรกรรมค่าใช้จ่ายโครงการ (PSA ไปยัง Fin และ Ops) จากนั้น ซิงโครไนส์โดยใช้เท็มเพลตประเภทธุรกรรมค่าใช้จ่ายของโครงการ (Fin and Ops ไปยัง PSA) จากนั้น คุณควรรันการซิงโครไนส์จาก Project Service Automation ไปยัง Finance อีกหนึ่งครั้ง
>
> หากคุณซิงโครไนส์ครั้งแรกจาก Project Service Automation ต้องเป็นไปตามข้อกำหนดต่อไปนี้ใน Finance ก่อนที่จะรันการซิงโครไนส์:
>
> - ประเภทใช้ร่วมกันที่สอดคล้องกับประเภทโครงการที่ตั้งค่าไว้ใน Project Service Automation ต้องมีอยู่ และต้องถูกเปิดใช้งานสำหรับทั้ง **โครงการ** และ **ค่าใช้จ่าย**
> - สำหรับนิติบุคคล Finance แต่ละรายที่ต้องถูกรวม ต้องมีประเภทโครงการต่อไปนี้อยู่:
>
>     - มี **ประเภทโครงการ** อยู่ 
>     - **ใช้ในค่าใช้จ่าย** ถูกเปิดใช้งาน
>     - **ใช้งานอยู่ในสมุดรายวัน** ถูกเปิดใช้งาน
>     - **ชนิดธุรกรรม** ถูกตั้งค่าเป็น **ค่าใช้จ่าย**

ภาพประกอบต่อไปนี้แสดงวิธีการซิงโครไนส์ข้อมูลระหว่าง Project Service Automation และ Finance

[![โฟลว์ข้อมูลสำหรับการรวม Project Service Automation กับ Finance](./media/ProjectExpenseCategoriesFlow.png)](./media/ProjectExpenseCategoriesFlow.png)

## <a name="project-expense-category-synchronization-from-finance-to-project-service-automation"></a>การซิงโครไนส์ประเภทค่าใช้จ่ายโครงการจาก Finance ไปยัง Project Service Automation

### <a name="template-and-task"></a>เท็มเพลตและงาน

เพื่อเข้าถึงเท็มเพลต ในศูนย์การจัดการ Microsoft PowerApps เลือก **โครงการ** และจากนั้น ที่มุมขวาบน เลือก **โครงการใหม่** เพื่อเลือกเท็มเพลตสาธารณะ

เท็มเพลตและงานพื้นฐานต่อไปนี้ถูกใช้ในการซิงโครไนส์ประเภทค่าใช้จ่ายของโครงการจาก Finance ไปยัง Project Service Automation:

- **ชื่อของเท็มเพลตในการรวมข้อมูล:** ประเภทธุรกรรมค่าใช้จ่ายของโครงการ (Fin and Ops ไปยัง PSA)
- **ชื่อของงานในโครงการ:** ซิงค์ประเภทไปยัง PSA

### <a name="entity-set"></a>การตั้งค่าเอนทิตี้

| การเงิน                           | Project Service Automation |
|-----------------------------------|----------------------------|
| เอนทิตี้การรวมสำหรับประเภท | ประเภทธุรกรรม     |

### <a name="entity-flow"></a>ขั้นตอนเอนทิตี้

มีการจัดการประเภทค่าใช้จ่ายของโครงการใน Finance และมีการซิงโครไนส์ไปยัง Project Service Automation เป็นประเภทธุรกรรม

### <a name="power-query"></a>Power Query

เมื่อคุณต้องซิงโครไนส์กับ Project Service Automation คุณต้องใช้ Microsoft Power Query for Excel เพื่อตั้งค่าชนิดการเรียกเก็บเงินในประเภทธุรกรรม ประเภทธุรกรรมค่าใช้จ่ายโครงการ (Fin and Ops ไปยัง PSA) มีคอลัมน์เริ่มต้นและการแม็ป ถ้าคุณสร้างเท็มเพลตของคุณเอง คุณต้องเพิ่มคอลัมน์แบบมีเงื่อนไขใน Power Query ทำตามขั้นตอนเหล่านี้

1. คลิกลูกศรเพื่อเปิดการแม็ปของงานประเภทค่าใช้จ่ายโครงการงานในเท็มเพลตประเภทของธุรกรรมค่าใช้จ่ายโครงการ (Fin and Ops ไปยัง PSA)
2. คลิกลิงก์ **การกรองข้อมูลและแบบสอบถามขั้นสูง** เพื่อเปิด Power Query
2. เลือก **เพิ่มคอลัมน์แบบมีเงื่อนไข**
3. ป้อนชื่อสำหรับคอลัมน์ใหม่ เช่น **BillingType**
4. ป้อนเงื่อนไขต่อไปนี้: **ถ้า CATEGORYID ไม่เท่ากับ null แล้ว 19235001 มิฉะนั้น null**
5. คลิก **ตกลง** บนคอลัมน์
6. ตรวจสอบให้แน่ใจว่าได้แม็ปคอลัมน์ใหม่นี้ในหน้าการแม็ป

ภาพประกอบต่อไปนี้แสดงตัวอย่างของการแม็ปงานเท็มเพลตในการรวมข้อมูล การแม็ปแสดงข้อมูลฟิลด์ที่จะถูกซิงโครไนส์จาก Finance ไปยัง Project Service Automation

[![การแม็ปเท็มเพลต](./media/ProjectExpenseCategoriesToPSAMapping.jpg)](./media/ProjectExpenseCategoriesToPSAMapping.jpg)

## <a name="project-expense-category-synchronization-from-project-service-automation-to-finance"></a>การซิงโครไนส์ประเภทค่าใช้จ่ายโครงการจาก Project Service Automation ไปยัง Finance

### <a name="template-and-task"></a>เท็มเพลตและงาน

เท็มเพลตและงานพื้นฐานต่อไปนี้ถูกใช้ในการซิงโครไนส์ประเภทค่าใช้จ่ายของโครงการจาก Project Service Automation ไปยัง Finance

- **ชื่อของเท็มเพลตในการรวมข้อมูล:** ประเภทธุรกรรมค่าใช้จ่ายของโครงการ (PSA ไปยัง Fin and Ops)
- **ชื่อของงานในโครงการ:** ซิงค์ประเภทไปยัง Fin Ops

### <a name="entity-set"></a>การตั้งค่าเอนทิตี้

| Project Service Automation | การเงิน                           |
|----------------------------|-----------------------------------|
| ประเภทธุรกรรม     | เอนทิตี้การรวมสำหรับประเภท |

### <a name="entity-flow"></a>ขั้นตอนเอนทิตี้

มีการจัดการประเภทค่าใช้จ่ายของโครงการใน Finance และมีการซิงโครไนส์ไปยัง Project Service Automation เป็นประเภทธุรกรรม การซิงโครไนส์กลับไปยัง Finance จะอัพเดตประเภทโครงการใน Finance and Operations ด้วยรหัสการรวมจาก Project Service Automation

### <a name="template-mapping-in-data-integration"></a>การแม็ปเท็มเพลตในการรวมข้อมูล

ภาพประกอบต่อไปนี้แสดงตัวอย่างของการแม็ปงานเท็มเพลตในการรวมข้อมูล

> [!NOTE]
> การแม็ปแสดงข้อมูลฟิลด์ที่จะถูกซิงโครไนส์จาก Project Service Automation ไปยัง Finance

[![การแม็ปเท็มเพลต](./media/ProjectExpenseCategoriesToFinOpsMapping.jpg)](./media/ProjectExpenseCategoriesToFinOpsMapping.jpg)
