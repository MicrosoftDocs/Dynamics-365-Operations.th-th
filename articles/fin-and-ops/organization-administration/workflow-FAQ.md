---
title: FAQ เกี่ยวกับลำดับงาน
description: หัวข้อนี้ตอบคำถามที่ถามบ่อยเกี่ยวกับระบบลำดับงานใน Microsoft Dynamics 365 for Finance and Operations
author: ChrisGarty
manager: AnnBe
ms.date: 05/07/2019
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
ms.openlocfilehash: f6240b1b5136937aa47f455547fed6f0c7c08e2c
ms.sourcegitcommit: 2b890cd7a801055ab0ca24398efc8e4e777d4d8c
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 05/07/2019
ms.locfileid: "1509302"
---
# <a name="workflow-system"></a>ระบบลำดับงาน

[!include [banner](../includes/banner.md)]

หัวข้อนี้ตอบคำถามที่ถามบ่อยเกี่ยวกับระบบลำดับงานใน Microsoft Dynamics 365 for Finance and Operations

## <a name="notifications"></a>การแจ้งเตือน

### <a name="why-are-multiple-notifications-received-when-a-work-item-is-rejected"></a>ทำไมได้รับการแจ้งเตือนจำนวนมากเมื่อรายการงานถูกปฏิเสธ?
เมื่อรายการงานถูกปฏิเสธ รายการงานถูกทำให้เสร็จสมบูรณ์เป็นถูกปฏิเสธ รายการงานอีกรายการถูกสร้างขึ้น และถูกกำหนดให้กับผู้ริเริ่ม นี่หมายความว่า มีการแจ้งเตือนไปยังผู้ริเริ่มสำหรับรายการงานที่ถูกปฏิเสธ และการแจ้งเตือนแบบแยกต่างหากของผู้ใช้ที่กำหนดให้กับรายการงาน "การเปลี่ยนแปลงที่ร้องขอ" ใหม่ 

การแจ้งเตือนแต่ละรายการมีไว้สำหรับรายการงานที่แตกต่างกัน แต่ความคล้ายคลึงอาจก่อให้เกิดความสับสน เรากำลังดูที่วิธีการปรับปรุงรายการนี้ในรุ่นต่อไป

### <a name="why-are-my-workflow-exports-failing"></a>เหตุใดการส่งออกลำดับงานของฉันจึงล้มเหลว?
ขณะนี้มีข้อจำกัดในลักษณะการทำงานในการส่งออกลำดับงานที่ป้องกันไม่ให้ชื่อลำดับงานเกิน 48 อักขระ การใช้ชื่อที่ยาวกว่า 48 อักขระอาจส่งผลให้เกิดข้อผิดพลาด "เซิร์ฟเวอร์ล้มเหลวในการรับรองความถูกต้องคำขอ" และ/หรือ ป้องกันไม่ให้ไฟล์ถูกส่งออกโดยไม่มีชนิดของไฟล์ โพสต์บล็อกต่อไปนี้ให้รายละเอียดเพิ่มเติม [การแก้ไขปัญหาการส่งออกลำดับงาน](https://community.dynamics.com/ax/b/elandaxdynamicsaxupgradesanddevelopment/archive/2019/04/10/workflow-export-troubleshooting)
