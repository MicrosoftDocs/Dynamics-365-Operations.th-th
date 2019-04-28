---
title: Talent ไม่ปรากฏขึ้นในแอป Microsoft Dynamics 365 (Common Data Service 1.0)
description: หัวข้อนี้อธิบายถึงสิ่งที่ต้องทำ ถ้าลูกค้าไม่เห็นแอป Microsoft Dynamics 365 for Talent ระหว่างแอป Microsoft Dynamics 365
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
ms.openlocfilehash: ad5add2b572ccb6bff175806b965f63b53986152
ms.sourcegitcommit: 45b79d1e587e03f5cde2766cdec4eaa7a2a897a3
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 04/02/2019
ms.locfileid: "949793"
---
# <a name="talent-doesnt-appear-among-the-microsoft-dynamics-365-apps-common-data-service-10"></a>Talent ไม่ปรากฏขึ้นในแอป Microsoft Dynamics 365 (Common Data Service 1.0)

[!include [banner](includes/banner.md)]

**ออกใช้**

ลูกค้าจะไม่เห็นแอป Microsoft Dynamics 365 for Talent ระหว่างแอป Microsoft Dynamics 365

**ความละเอียด**

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
