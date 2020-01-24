---
title: ฝังแอป Power Apps ใน Dynamics 365 - Core HR
description: หัวข้อนี้อธิบายวิธีการแก้ปัญหาที่ซึ่งรายการเมนู Microsoft Power Apps หายไปจากโมดูลการดูแลระบบ
author: andreabichsel
manager: AnnBe
ms.date: 11/02/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2018-11-02
ms.dyn365.ops.version: Talent
ms.openlocfilehash: b1dd1756be349d85af8e6d7159623a2a95e75526
ms.sourcegitcommit: 871707a3fd236da693a3d51f401eb0cb9d4bae39
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 12/06/2019
ms.locfileid: "2898723"
---
# <a name="embed-power-apps-apps-in-dynamics-365---core-hr"></a>ฝังแอป Power Apps ใน Dynamics 365 - Core HR

**ออกใช้**

รายการเมนู **Power Apps** หายไปจากโมดูล **การดูแลระบบ**

**สาเหตุ**

การออกแบบส่วนติดต่อผู้ใช้ (UI) ได้ถูกเปลี่ยนแปลง และขณะนี้ Microsoft Power Apps ถูกรวมในแบบจำลองการตั้งค่าส่วนบุคคลมาตรฐาน

**ความละเอียด**

วิธีการที่ Power Apps ถูกฝังถูกเปลี่ยนแปลง ขณะนี้ Power Apps ถูกเพิ่มโดยใช้แบบจำลองการตั้งค่าส่วนบุคคล คุณสามารถเพิ่ม Power Apps ไปยังหน้าได้เกือบทั้งหมดใน Microsoft Dynamics 365 Talent

สำหรับข้อมูลเกี่ยวกับวิธีการฝังแอป Power Apps ใน Talent ดู [ฝัง Microsoft Power Apps](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/get-started/embed-power-apps)

ลูกค้า Power Apps ที่ฝังแอปก่อนมีการเปลี่ยนแปลง ที่จะควรมีการอัพเกรดการเปลี่ยนแปลงเป็นแบบจำลองใหม่

ปุ่ม **Power Apps** อยู่ในมุมขวาบนของหน้าเกือบทุกหน้าใน Talent คุณสามารถใช้ปุ่มนี้เพื่อแทรก Power Apps ได้

นี่คือตัวอย่าง

1. ไปยัง **การจัดการบุคลากร \> ลิงค์ \> ผู้ปฏิบัติงาน \> พนักงาน**
2. เลือกปุ่ม **Power Apps** และจากนั้น เลือก **แทรก PowerApp**

    ![ปุ่ม Power Apps](media/png.png)

3. กรอกข้อมูลฟิลด์ในกล่องโต้ตอบ **แทรก PowerApp**

    ![แทรกกล่องโต้ตอบ PowerApp](media/insert-powerapp.png)

หรือทำตามขั้นตอนเหล่านี้

1. บนบานหน้าต่างการดำเนินการของหน้า บนแท็บ **ตัวเลือก** ในกลุ่ม **ตั้งค่าส่วนบุคคล** เลือก **ตั้งค่าแบบฟอร์มนี้ให้เป็นแบบส่วนบุคคล**

    ![ตั้งค่ากลุ่มให้เป็นแบบส่วนบุคคลบนแท็บตัวเลือก](media/options.png)

    แถบเครื่องมือการตั้งค่าส่วนบุคคลปรากฏขึ้น

2. บนแถบเครื่องมือ เลือก **แทรก \> PowerApp**

    ![แทรกแอป Power Apps โดยใช้แถบเครื่องมือการตั้งค่าส่วนบุคคล](media/powerapp-bar.png)
