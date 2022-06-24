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
ms.openlocfilehash: b690e35b2df736f3e277260e6f752ef5240b0938
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 06/03/2022
ms.locfileid: "8870503"
---
# <a name="troubleshoot-store-commerce-performance-issues"></a>การแก้ไขปัญหาประสิทธิภาพของ Store Commerce

[!include [banner](../includes/banner.md)]
[!include [banner](../includes/preview-banner.md)]

บทความนี้จะอธิบายวิธีการแก้ไขปัญหาประสิทธิภาพในแอป Store Commerce ของ Microsoft Dynamics 365 Commerce

- เมื่อคุณแก้ไขปัญหาประสิทธิภาพการเกิดปัญหาใน Store Commerce ให้หลีกเลี่ยงการลงชื่อเข้าใช้ระยะไกล แต่ให้ลงชื่อเข้าใช้ไปยังอุปกรณ์ Store Commerce โดยตรง
- หากแอป Store Commerce ช้า ให้ตรวจสอบ GT; หน่วยความจํา เครือข่าย และการใช้งานดิสก์โดยใช้โปรแกรมจัดการงานหรือตัวตรวจสอบทรัพยากร ตรวจสอบให้แน่ใจว่าไม่มีปริมาณการใช้ทรัพยากรอุปกรณ์ที่สําคัญ
- ตรวจสอบสถานะการเชื่อมต่อเครือข่ายของคุณ และยืนยันว่าคำขอ/การตอบสนอง HTTPS ไม่ใช้เวลานานกว่า 2-3 วินาที
