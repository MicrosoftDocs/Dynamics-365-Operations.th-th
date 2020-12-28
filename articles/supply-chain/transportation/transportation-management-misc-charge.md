---
title: ค่าธรรมเนียมเบ็ดเตล็ดสำหรับการจัดการการขนส่ง
description: หัวข้อนี้อธิบายถึงวิธีการที่ต้องเชื่อมโยงค่าธรรมเนียมการขนส่งกับรหัสค่าธรรมเนียม
author: Henrikan
manager: tfehr
ms.date: 10/16/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: henrikan
ms.search.validFrom: 2020-10-16
ms.dyn365.ops.version: Release 10.0.14
ms.openlocfilehash: 2b703d770c7f9ea684716368cf1e7dbe5fec8710
ms.sourcegitcommit: fe7ac653efcb1ac6318083f482394b96ed82b4c7
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 10/29/2020
ms.locfileid: "4438953"
---
# <a name="transportation-management-miscellaneous-charges"></a>ค่าธรรมเนียมเบ็ดเตล็ดสำหรับการจัดการการขนส่ง

[!include [banner](../includes/banner.md)]

ตามด้วยค่าธรรมเนียมเบ็ดเตล็ดทั้งหมด ค่าธรรมเนียมการขนส่งต้องเชื่อมโยงกับรหัสค่าธรรมเนียม มิฉะนั้น จะไม่มีการเพิ่มกลับไปยังใบสั่งเป็นค่าธรรมเนียมเบ็ดเตล็ด **รหัสค่าธรรมเนียม** จะกำหนดวิธีการลงรายการบัญชีค่าธรรมเนียมสัมพันธ์กับใบสั่งและรายการใบสั่งที่มีการเพิ่มค่าธรรมเนียม

ไปที่ **การจัดการการขนส่ง > การตั้งค่า > การจัดอันดับ > ค่าธรรมเนียมเบ็ดเตล็ด** เพื่อกำหนดเกณฑ์การกำหนดคุณสมบัติที่กำหนดเมื่อมีการใช้ **รหัสค่าธรรมเนียม** เฉพาะกับค่าธรรมเนียม

คุณควรติดตั้งอย่างน้อยหนึ่งรายการสำหรับแต่ละการตั้งค่า **โมดูลค่าธรรมเนียม** ที่เกี่ยวข้อง (*ลูกค้า* และ *ผู้จัดจำหน่าย*) ที่มีการตั้งค่า **ชนิดค่าธรรมเนียมเบ็ดเตล็ด** เป็น *ไม่มี* ถ้าขาดหายไป ค่าธรรมเนียมเบ็ดเตล็ดจะ *ไม่* เพิ่มลงในใบสั่ง
