---
title: ทรัพยากรบุคคลไม่มีอยู่ในแอป Microsoft Dynamics 365
description: บทความนี้อธิบายถึงสิ่งที่ต้องทำ ถ้าลูกค้าไม่เห็นแอป Microsoft Dynamics 365 Human Resources ระหว่างแอป Microsoft Dynamics 365
author: andreabichsel
manager: tfehr
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-human-resources
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 9be1c2b862a01d6f14ad98dbcb01e061649c6af0
ms.sourcegitcommit: 6affb3316be757c99e1fe9c7c7b312b93c483408
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 02/17/2021
ms.locfileid: "5463995"
---
# <a name="human-resources-doesnt-appear-in-microsoft-dynamics-365-apps"></a>ทรัพยากรบุคคลไม่มีอยู่ในแอป Microsoft Dynamics 365

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

**ออกใช้**

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