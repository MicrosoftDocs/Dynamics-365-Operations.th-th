---
title: การแก้ไขปัญหาประสิทธิภาพของ Store Commerce
description: บทความนี้จะอธิบายวิธีการแก้ไขปัญหาประสิทธิภาพในแอป Store Commerce ของ Microsoft Dynamics 365 Commerce
author: mugunthanm
ms.date: 06/01/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.search.industry: Retail
ms.author: rassadi
ms.search.validFrom: 2022-05-12
ms.dyn365.ops.version: 10.0.25
ms.openlocfilehash: fef4eb7063f4acdbca5fab2ad33ec10e0cb603bd
ms.sourcegitcommit: c271b2edc4bf777f7194b09139ccbd174a359c75
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 07/16/2022
ms.locfileid: "9169058"
---
# <a name="troubleshoot-store-commerce-performance-issues"></a>การแก้ไขปัญหาประสิทธิภาพของ Store Commerce

[!include [banner](../includes/banner.md)]

บทความนี้จะอธิบายวิธีการแก้ไขปัญหาประสิทธิภาพในแอป Store Commerce ของ Microsoft Dynamics 365 Commerce

- เมื่อคุณแก้ไขปัญหาประสิทธิภาพการเกิดปัญหาใน Store Commerce ให้หลีกเลี่ยงการลงชื่อเข้าใช้ระยะไกล แต่ให้ลงชื่อเข้าใช้ไปยังอุปกรณ์ Store Commerce โดยตรง
- หากแอป Store Commerce ช้า ให้ตรวจสอบ GT; หน่วยความจํา เครือข่าย และการใช้งานดิสก์โดยใช้โปรแกรมจัดการงานหรือตัวตรวจสอบทรัพยากร ตรวจสอบให้แน่ใจว่าไม่มีปริมาณการใช้ทรัพยากรอุปกรณ์ที่สําคัญ
- ตรวจสอบสถานะการเชื่อมต่อเครือข่ายของคุณ และยืนยันว่าคำขอ/การตอบสนอง HTTPS ไม่ใช้เวลานานกว่า 2-3 วินาที
