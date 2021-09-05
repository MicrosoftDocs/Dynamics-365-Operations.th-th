---
title: ทรัพยากรบุคคลไม่มีอยู่ในแอป Microsoft Dynamics 365
description: หัวข้อนี้จะอธิบายสิ่งที่ต้องแก้ไขหาก Microsoft Dynamics 365 Human Resources ไม่ได้อยู่ในรายการในบรรดาแอป Microsoft Dynamics 365
author: twheeloc
ms.date: 08/19/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.search.scope: Human Resources
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: dfed82463eece882bed66c7b2dac1dd30e04720e
ms.sourcegitcommit: 7e32e5e39e762a4b1606161cb603a450d13b5251
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 08/23/2021
ms.locfileid: "7413412"
---
# <a name="human-resources-app-doesnt-appear-in-microsoft-dynamics-365-apps"></a>แอป Human Resources ไม่ปรากฏในแอป Microsoft Dynamics 365

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

**ปัญหา**

ลูกค้าไม่เห็น Dynamics 365 Human Resources ในแอป Microsoft Dynamics 365

**ความละเอียด**

ต้องมีการเพิ่มผู้ใช้ให้กับบทบาทผู้สร้างสภาพแวดล้อมสำหรับสภาพแวดล้อมใน Microsoft Power Apps

1. ผู้ใช้ที่เป็นผู้ดูแลระบบที่มีลิขสิทธิ์ Power Apps Plan 2 ต้องเปิด [พอร์ทัลผู้ดูแลระบบ Power Apps](https://preview.admin.powerapps.com/)

2. เลือก **สภาพแวดล้อม** และเลือกสภาพแวดล้อมที่ถูกต้องสำหรับทรัพยากรบุคคล

3. บนแท็บ **ความปลอดภัย** บนแท็บ **บทบาทสภาพแวดล้อม** เลือก **ผู้ผู้สร้างสภาพแวดล้อม**

    ![แท็บบทบาทสภาพแวดล้อม](media/environment-roles.png)

4. บนแท็บ **ผู้ใช้** เพิ่มผู้ใช้หรือองค์กรของคุณ

    ![แท็บผู้ใช้](media/environment-maker.png)

5. เลือก **บันทึก**

6. ขณะนี้ ผู้ใช้ต้องลงชื่อเข้าใช้ใน [Microsoft Dynamics 365](https://home.dynamics.com/)

7. เลือก **ซิงค์** เพื่ออัพเดตแอปผู้ใช้

    ![ซิงค์ปุ่ม](media/get-more.png)

    หลังจากการซิงโครไนส์เสร็จสมบูรณ์ ทรัพยากรบุคคลจะปรากฏขึ้นบนโฮมเพจ


[!INCLUDE[footer-include](../includes/footer-banner.md)]
