---
title: เข้าถึงที่อยู่ส่วนตัวตามบทบาทความปลอดภัย
description: หัวข้อนี้อธิบายวิธีการแก้ปัญหาที่ซึ่งลูกค้าไม่สามารถเข้าถึงที่อยู่ส่วนตัวได้
author: Darinkramer
manager: AnnBe
ms.date: 11/02/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: dkrame
ms.search.validFrom: 2018-11-02
ms.dyn365.ops.version: Talent
ms.openlocfilehash: c1c1c3ce1233408e73d177f9e04f1137f3171a49
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 01/29/2019
ms.locfileid: "306373"
---
# <a name="access-to-private-addresses-by-security-role"></a>เข้าถึงที่อยู่ส่วนตัวตามบทบาทความปลอดภัย

[!include [banner](includes/banner.md)]

**ออก**

หลังจากที่ลูกค้าทำซ้ำบทบาทความปลอดภัยและลงชื่อเข้าใช้ในฐานะบทบาทใหม่นั้น ลูกค้าไม่สามารถดูที่อยู่ที่ถูกทำเครื่องหมายเป็นส่วนตัวได้

**การแก้ปัญหา**

เพื่อแก้ปัญหา ลูกค้าต้องทำตามขั้นตอนเหล่านี้สำหรับบทบาทความปลอดภัยที่ซ้ำกัน

1. ไปที่ **การจัดการองค์กร \> สมุดที่อยู่สากล \> พารามิเตอร์ของสมุดที่อยู่สากล**
2. บนแท็บ **ความปลอดภัยที่ตั้งส่วนตัว** ย้ายบทบาทความปลอดภัยใหม่จากรายการ **บทบาทที่พร้อมใช้งาน** ไปยังรายการ **บทบาทที่เลือก**
3. เลือก **บันทึก**

![พารามิเตอร์สมุดที่อยู่สากล](media/GAD-parameters.png)
