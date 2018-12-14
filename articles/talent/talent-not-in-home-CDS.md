---
title: "Talent ไม่ปรากฏระหว่างแอป Microsoft Dynamics 365 (CDS1.0)"
description: "หัวข้อนี้อธิบายถึงสิ่งที่ต้องทำ ถ้าลูกค้าไม่เห็นแอป Microsoft Dynamics 365 for Talent ระหว่างแอป Microsoft Dynamics 365"
author: Darinkramer
manager: AnnBe
ms.date: 11/02/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-365-talent
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Talent
ms.custom: 
ms.assetid: 
ms.search.region: Global
ms.author: dkrame
ms.search.validFrom: 2018-11-02
ms.dyn365.ops.version: Talent
ms.translationtype: HT
ms.sourcegitcommit: d3f974f94b6c327fd70b8098d24f9e1f1e1e8eeb
ms.openlocfilehash: 32ae0ab807e953bd811a557e6878b9bee79d293c
ms.contentlocale: th-th
ms.lasthandoff: 12/04/2018

---

# <a name="talent-doesnt-appear-among-the-microsoft-dynamics-365-apps-cds10"></a>Talent ไม่ปรากฏระหว่างแอป Microsoft Dynamics 365 (CDS1.0)

[!include [banner](includes/banner.md)]

**ออก**

ลูกค้าไม่เห็นแอป Microsoft Dynamics 365 for Talent ระหว่างแอป Microsoft Dynamics 365

**การแก้ปัญหา**

ต้องมีการเพิ่มผู้ใช้ให้กับบทบาทผู้สร้างสภาพแวดล้อมสำหรับสภาพแวดล้อมใน Microsoft PowerApps

1. ผู้ใช้ที่เป็นผู้ดูแลระบบที่มีลิขสิทธิ์ PowerApps แผน 2 ต้องเปิด [พอร์ทัลผู้ดูแลระบบ PowerApps](https://preview.admin.powerapps.com/)
2. เลือก **สภาพแวดล้อม** และเลือกสภาพแวดล้อมที่ถูกต้องสำหรับ Talent
3. บนแท็บ **ความปลอดภัย** บนแท็บ **บทบาทสภาพแวดล้อม** เลือก **ผู้ผู้สร้างสภาพแวดล้อม**

    ![แท็บบทบาทสภาพแวดล้อม](media/environment-roles.png)

4. บนแท็บ **ผู้ใช้** เพิ่มผู้ใช้หรือองค์กรของคุณ

    ![แท็บผู้ใช้](media/environment-maker.png)

5. เลือก **บันทึก**
6. ขณะนี้ ผู้ใช้ต้องลงชื่อเข้าใช้ใน [Microsoft Dynamics 365](https://home.dynamics.com/)
7. เลือก **ซิงค์** เพื่ออัพเดตแอปผู้ใช้

    ![ซิงค์ปุ่ม](media/get-more.png)

    หลังจากการซิงโครไนส์เสร็จสมบูรณ์ Talent จะปรากฏขึ้นบนโฮมเพจ

