---
title: "ซิงโครไนส์ประเภทค่าใช้จ่ายของโครงการจาก Project Service Automation"
description: "หัวข้อนี้อธิบายเท็มเพลตและงานพื้นฐานที่ถูกใช้ในการซิงโครไนส์ประเภทค่าใช้จ่ายของโครงการระหว่าง Microsoft Dynamics 365 for Finance and Operations และ Dynamics 365 for Project Service Automation"
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
ms.dyn365.ops.version: AX 8.0.0
ms.translationtype: HT
ms.sourcegitcommit: bd8feff598cf80ca675c7d2b5dda636799b19e29
ms.openlocfilehash: dcdb9b6ec296073d511c069cdceb1c61080b6d97
ms.contentlocale: th-th
ms.lasthandoff: 05/29/2018

---

# <a name="synchronize-project-expense-categories-between-finance-and-operations-and-project-service-automation"></a>ปซิงโครไนส์ระเภทค่าใช้จ่ายโครงการระหว่าง Finance and Operations และ Project Service Automation

หัวข้อนี้อธิบายเท็มเพลตและงานพื้นฐานที่ถูกใช้ในการซิงโครไนส์ประเภทค่าใช้จ่ายของโครงการระหว่าง Microsoft Dynamics 365 for Finance and Operations และ Dynamics 365 for Project Service Automation

> [!NOTE]
> การรวมงานโครงการ ประเภทธุรกรรมค่าใช้จ่าย การประเมินชั่วโมง การประเมินค่าใช้จ่าย และการล็อคฟังก์ชัน พร้อมใช้งานใน Dynamics 365 for Finance and Operations รุ่น 8.0

## <a name="data-flow-for-project-service-automation-and-finance-and-operations"></a>โฟลว์ข้อมูลสำหรับ Project Service Automation และ Finance and Operations

โซลูชันการรวม Project Service Automation และ Finance and Operations ใช้คุณลักษณะการรวมข้อมูล เพื่อซิงโครไนส์ข้อมูลระหว่างอินสแตนซ์ของ Project Service Automation และ Finance and Operations เท็มเพลตการรวมที่พร้อมใช้งานกับคุณลักษณะการรวมข้อมูล เปิดใช้งานโฟลว์ของข้อมูลเกี่ยวกับธุรกรรมค่าใช้จ่ายของโครงการระหว่าง Finance and Operations และ Project Service Automation

ถ้าประเภทค่าใช้จ่ายโครงการเป็นต้นฉบับใน Finance and Operations ในตอนแรกโฟลว์การรวมมาจาก Finance and Operations ไปยัง Project Service Automation และจากนั้น อัพเดตรหัสการรวมของประเภทค่าใช้จ่ายโครงการจาก Project Service Automation ไปยัง Finance and Operations

ถ้าประเภทค่าใช้จ่ายโครงการเป็นต้นฉบับใน Project Service Automation ในตอนแรกโฟลว์การรวมมาจาก Project Service Automation ไปยัง Finance and Operations ประเภทโครงการต้องถูกตั้งค่าคอนฟิกใน Finance and Operations อยู่แล้ว ก่อนการซิงโครไนส์จาก Project Service Automation จากนั้น ซิงโครไนส์จาก Finance and Operations กลับไปยัง Project Service Automation และจากนั้นจาก Project Service Automation ไปยัง Finance and Operations อีกครั้ง ซึ่งช่วยให้มั่นใจว่าประเภทจะถูกเชื่อมโยง และไม่มีการสร้างข้อมูลซ้ำ

> [!NOTE]
> โดยทั่วไป ประเภทค่าใช้จ่ายโครงการจะเป็นต้นฉบับใน Finance and Operations ถ้านั่นไม่ใช่สถานการณ์ของคุณ หรือคุณมีประเภทค่าใช้จ่ายที่สร้างขึ้นใน Project Service Automation อยู่แล้ว คุณต้องซิงค์โดยใช้ประเภทธุรกรรมค่าใช้จ่ายของโครงการ (PSA ไปยัง Fin and Ops) และจากนั้น ซิงค์โดยใช้ประเภทธุรกรรมค่าใช้จ่ายโครงการ (Fin and Ops ไปยัง PSA) จากนั้น คุณควรรันการซิงค์จาก PSA ไปยัง Fin and Ops อีกหนึ่งครั้ง

> ถ้าในตอนแรกการซิงโครไนส์มาจาก Project Service Automation ประเภทโครงการต้องถูกตั้งค่าใน Finance and Operations อยู่แล้ว และประเภทโครงการใดๆ ที่จำเป็นต้องซิงค์กับประเภทธุรกรรม Project Service Automation ต้องถูกตั้งค่าเป็น **ใช้งานอยู่ในสมุดรายวัน**

ภาพประกอบต่อไปนี้แสดงวิธีการซิงโครไนส์ข้อมูลระหว่าง Project Service Automation และ Finance and Operations

[![โฟลว์ข้อมูลสำหรับการรวม Project Service Automation กับ Finance and Operations](./media/ProjectExpenseCategoriesFlow.png)](./media/ProjectExpenseCategoriesFlow.png)


## <a name="templates-and-tasks"></a>เท็มเพลตและงาน

เมื่อต้องการเข้าถึงเท็มเพลตที่พร้อมใช้งาน ในศูนย์การจัดการ Microsoft PowerApps เลือก **โครงการ** และจากนั้น ในมุมบนด้านขวา เลือก **โครงการใหม่** เพื่อเลือกเท็มเพลตสาธารณะ

เท็มเพลตและงานพื้นฐานต่อไปนี้จะถูกใช้ในการซิงโครไนส์ประเภทค่าใช้จ่ายของโครงการจาก Finance and Operations ไปยัง Project Service Automation:

-  **ชื่อของเท็มเพลตในการรวมข้อมูล:** ประเภทธุรกรรมค่าใช้จ่ายของโครงการ (Fin and Ops ไปยัง PSA)
-  **ชื่อของงานในโครงการ:** ซิงค์ประเภทไปยัง PSA

## <a name="entity-set"></a>การตั้งค่าเอนทิตี้

| Finance and Operations               | Project Service Automation    |
|--------------------------------------|-------------------------------|
| เอนทิตี้การรวมสำหรับประเภท    | ประเภทธุรกรรม        |

## <a name="entity-flow"></a>ขั้นตอนเอนทิตี้

มีการจัดการประเภทค่าใช้จ่ายของโครงการใน Finance and Operations และมีการซิงโครไนส์ไปยัง Project Service Automation เป็นประเภทธุรกรรม

## <a name="power-query"></a>Power Query

คุณต้องใช้ Microsoft Power Query เพื่อตั้งค่าชนิดการเรียกเก็บเงินในประเภทธุรกรรม เมื่อซิงโครไนส์กับ Project Service Automation ประเภทธุรกรรมค่าใช้จ่ายโครงการ (Fin and Ops ไปยัง PSA) มีคอลัมน์เริ่มต้นและการแม็ปที่มีอยู่แล้ว ถ้าคุณสร้างเท็มเพลตของคุณเอง คุณต้องเพิ่มคอลัมน์แบบมีเงื่อนไขใน Power Query
- เปิดแบบฟอร์มการสอบถามขั้นสูงและการกรองจากภายในการแม็ปงานประเภทค่าใช้จ่ายโครงการ
- เลือก **เพิ่มคอลัมน์แบบมีเงื่อนไข**
- ตั้งชื่อคอลัมน์ใหม่ เช่น BillingType
- ป้อนเงื่อนไขต่อไปนี้: ถ้า **CATEGORYID ไม่เท่ากับ null แล้ว 19235001 มิฉะนั้น null**
- คลิก **ตกลง** บนคอลัมน์
- ตรวจสอบให้แน่ใจว่าแม็ปคอลัมน์ใหม่นี้ในหน้าการแม็ป

ภาพประกอบต่อไปนี้แสดงตัวอย่างของการแม็ปงานเท็มเพลตในการรวมข้อมูล การแม็ปแสดงข้อมูลฟิลด์ที่จะถูกซิงโครไนส์จาก Finance and Operations ไปยัง Project Service Automation

[![การแม็ปเท็มเพลต](./media/ProjectExpenseCategoriesToPSAMapping.jpg)](./media/ProjectExpenseCategoriesToPSAMapping.jpg)

เท็มเพลตและงานพื้นฐานต่อไปนี้จะถูกใช้ในการซิงโครไนส์ประเภทค่าใช้จ่ายของโครงการจาก Project Service Automation ไปยัง Finance and Operations:

-**ชื่อของเท็มเพลตในการรวมข้อมูล:** ประเภทธุรกรรมค่าใช้จ่ายโครงการ (PSA ไปยัง Fin and Ops) -**ชื่อของงานในโครงการ:** ซิงค์ประเภทไปยัง Fin Ops

## <a name="entity-set"></a>การตั้งค่าเอนทิตี้

| Project Service Automation      | Finance and Operations             |
|---------------------------------|------------------------------------|
| ประเภทธุรกรรม          | เอนทิตี้การรวมสำหรับประเภท  | 

## <a name="entity-flow"></a>ขั้นตอนเอนทิตี้

มีการจัดการประเภทค่าใช้จ่ายของโครงการใน Finance and Operations และมีการซิงโครไนส์ไปยัง Project Service Automation เป็นประเภทธุรกรรม การซิงโครไนส์กลับไปยัง Finance and Operations อัพเดตรหัสการรวมจาก Project Service Automation ในประเภทโครงการ Finance and Operations

ภาพประกอบต่อไปนี้แสดงตัวอย่างของการแม็ปงานเท็มเพลตในการรวมข้อมูล

> [!NOTE]
> การแม็ปแสดงข้อมูลฟิลด์ที่จะถูกซิงโครไนส์จาก Project Service Automation ไปยัง Finance and Operations

[![การแม็ปเท็มเพลต](./media/ProjectExpenseCategoriesToFinOpsMapping.jpg)](./media/ProjectExpenseCategoriesToFinOpsMapping.jpg)

