---
title: ฝังแอป Power Apps ใน Dynamics 365 Human Resources
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
ms.openlocfilehash: 8275a8a7c68fa13d6b9880c4c411deaa2dcbb998
ms.sourcegitcommit: 54baab2a04e5c534fc2d1fd67b67e23a152d4e57
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 02/04/2020
ms.locfileid: "3017884"
---
# <a name="embed-power-apps-apps-in-dynamics-365-human-resources"></a>ฝังแอป Power Apps ใน Dynamics 365 Human Resources

**ออกใช้**

รายการเมนู **Power Apps** หายไปจากโมดูล **การดูแลระบบ**

**สาเหตุ**

การออกแบบส่วนติดต่อผู้ใช้ (UI) ได้ถูกเปลี่ยนแปลง และขณะนี้ Microsoft Power Apps ถูกรวมในแบบจำลองการตั้งค่าส่วนบุคคลมาตรฐาน

**ความละเอียด**

วิธีการที่ Power Apps ถูกฝังถูกเปลี่ยนแปลง ขณะนี้ Power Apps ถูกเพิ่มโดยใช้แบบจำลองการตั้งค่าส่วนบุคคล คุณสามารถเพิ่ม Power Apps ไปยังหน้าได้เกือบทั้งหมดใน Microsoft Dynamics 365 Talent

สำหรับข้อมูลเกี่ยวกับวิธีการฝังแอป Power Apps ใน Talent ดู [ฝัง Power Apps](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/get-started/embed-power-apps)

ลูกค้า Power Apps ที่ฝังแอปก่อนมีการเปลี่ยนแปลง ที่จะควรมีการอัพเกรดการเปลี่ยนแปลงเป็นแบบจำลองใหม่

ปุ่ม **Power Apps** อยู่ในมุมขวาบนของหน้าเกือบทุกหน้าใน Talent คุณสามารถใช้ปุ่มนี้ในการแทรกแอป

นี่คือตัวอย่าง

1. ไปยัง **การจัดการบุคลากร \> ลิงค์ \> ผู้ปฏิบัติงาน \> พนักงาน**
2. เลือกปุ่ม **Power Apps** แล้วเลือก **เพิ่มแอปจาก Power Apps**

    ![ปุ่ม Power Apps](media/png.png)

3. กรอกข้อมูลในฟิลด์ในกล่องโต้ตอบ **เพิ่มแอปจาก Power Apps**

    ![เพิ่มแอปจากกล่องโต้ตอบ Power Apps ](media/insert-powerapp.png)

หรือทำตามขั้นตอนเหล่านี้

1. ที่บานหน้าต่างการดำเนินการของเพจ บนแท็บ **ตัวเลือก** ในกลุ่ม **ปรับให้เป็นแบบส่วนตัว** เลือก **ปรับหน้านี้ให้เป็นแบบส่วนตัว**

    ![ตั้งค่ากลุ่มให้เป็นแบบส่วนบุคคลบนแท็บตัวเลือก](media/options.png)

    แถบเครื่องมือการตั้งค่าส่วนบุคคลปรากฏขึ้น

2. บนแถบเครื่องมือ เลือก **เพิ่มแอปจาก Power Apps**

    ![เพิ่มแอปจาก Power Apps โดยใช้แถบเครื่องมือแบบรายบุคคล](media/powerapp-bar.png)
