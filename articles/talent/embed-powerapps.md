---
title: ฝังแอป PowerApps ใน Core HR
description: หัวข้อนี้อธิบายวิธีการแก้ปัญหาที่ซึ่งรายการเมนู PowerApps หายไปจากโมดูลการดูแลระบบ
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
ms.openlocfilehash: 7c0dcdd7e2f407267cf99906b4d0b317858710af
ms.sourcegitcommit: 45f8cea6ac75bd2f4187380546a201c056072c59
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 07/12/2019
ms.locfileid: "1742830"
---
# <a name="embed-powerapps-apps-in-core-hr"></a>ฝังแอป PowerApps ใน Core HR

[!include [banner](includes/banner.md)]

**ออก**

รายการเมนู **PowerApps** หายไปจากโมดูล **การดูแลระบบ**

**สาเหตุ**

การออกแบบส่วนติดต่อผู้ใช้ (UI) ได้ถูกเปลี่ยนแปลง และขณะนี้ Microsoft PowerApps ถูกรวมในแบบจำลองการตั้งค่าส่วนบุคคลมาตรฐาน

**ความละเอียด**

มีการเปลี่ยนแปลงวิธีการที่แอป PowerApps ถูกฝัง ขณะนี้มีการเพิ่มแอป PowerApps โดยใช้แบบจำลองการตั้งค่าส่วนบุคคล คุณสามารถเพิ่มแอป PowerApps ไปยังหน้าได้เกือบทั้งหมดใน Microsoft Dynamics 365 for Talent

สำหรับข้อมูลเกี่ยวกับวิธีการฝังแอป PowerApps ใน Talent ดู [ฝังแอป PowerApps](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/get-started/embed-power-apps)

ลูกค้า PowerApps ใดๆ ที่ฝังแอป ก่อนที่จะควรมีการอัพเกรดการเปลี่ยนแปลงเป็นแบบจำลองใหม่

ปุ่ม **PowerApps** อยู่ในมุมขวาบนของหน้าเกือบทุกหน้าใน Talent คุณสามารถใช้ปุ่มนี้เพื่อแทรกแอป PowerApps ได้

นี่คือตัวอย่าง

1. ไปยัง **การจัดการบุคลากร \> ลิงค์ \> ผู้ปฏิบัติงาน \> พนักงาน**
2. เลือกปุ่ม **PowerApps** และจากนั้น เลือก **แทรก PowerApp**

    ![ปุ่ม PowerApps](media/png.png)

3. กรอกข้อมูลฟิลด์ในกล่องโต้ตอบ **แทรก PowerApp**

    ![แทรกกล่องโต้ตอบ PowerApp](media/insert-powerapp.png)

หรือทำตามขั้นตอนเหล่านี้

1. บนบานหน้าต่างการดำเนินการของหน้า บนแท็บ **ตัวเลือก** ในกลุ่ม **ตั้งค่าส่วนบุคคล** เลือก **ตั้งค่าแบบฟอร์มนี้ให้เป็นแบบส่วนบุคคล**

    ![ตั้งค่ากลุ่มให้เป็นแบบส่วนบุคคลบนแท็บตัวเลือก](media/options.png)

    แถบเครื่องมือการตั้งค่าส่วนบุคคลปรากฏขึ้น

2. บนแถบเครื่องมือ เลือก **แทรก \> PowerApp**

    ![แทรกแอป PowerApps โดยใช้แถบเครื่องมือการตั้งค่าส่วนบุคคล](media/powerapp-bar.png)
