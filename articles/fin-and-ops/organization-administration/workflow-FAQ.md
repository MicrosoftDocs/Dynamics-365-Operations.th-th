---
title: FAQ เกี่ยวกับลำดับงาน
description: หัวข้อนี้ตอบคำถามที่ถามบ่อยเกี่ยวกับระบบลำดับงานใน Microsoft Dynamics 365 for Finance and Operations
author: ChrisGarty
manager: AnnBe
ms.date: 02/28/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: cgarty
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: f058a450eb18e688efbc5306a42b4efef6aa91e7
ms.sourcegitcommit: 9a723737565ac78c884e40f7129d0f5aad747524
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 03/01/2019
ms.locfileid: "773235"
---
# <a name="workflow-system"></a>ระบบลำดับงาน

[!include [banner](../includes/banner.md)]

หัวข้อนี้ตอบคำถามที่ถามบ่อยเกี่ยวกับระบบลำดับงานใน Microsoft Dynamics 365 for Finance and Operations

## <a name="notifications"></a>การแจ้งเตือน

### <a name="why-are-multiple-notifications-received-when-a-work-item-is-rejected"></a>ทำไมได้รับการแจ้งเตือนจำนวนมากเมื่อรายการงานถูกปฏิเสธ?
เมื่อรายการงานถูกปฏิเสธ รายการงานถูกทำให้เสร็จสมบูรณ์เป็นถูกปฏิเสธ รายการงานอีกรายการถูกสร้างขึ้น และถูกกำหนดให้กับผู้ริเริ่ม นี่หมายความว่า มีการแจ้งเตือนไปยังผู้ริเริ่มสำหรับรายการงานที่ถูกปฏิเสธ และการแจ้งเตือนแบบแยกต่างหากของผู้ใช้ที่กำหนดให้กับรายการงาน "การเปลี่ยนแปลงที่ร้องขอ" ใหม่ 

การแจ้งเตือนแต่ละรายการมีไว้สำหรับรายการงานที่แตกต่างกัน แต่ความคล้ายคลึงอาจก่อให้เกิดความสับสน เรากำลังดูที่วิธีการปรับปรุงรายการนี้ในรุ่นต่อไป
