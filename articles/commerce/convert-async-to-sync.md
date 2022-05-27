---
title: แปลงลูกค้าแบบเอซิงค์เป็นลูกค้าแบบซิงค์
description: หัวข้อนี้อธิบายวิธีการแปลงลูกค้าแบบอะซิงโครนัสเป็นลูกค้าแบบซิงโครนัสใน Microsoft Dynamics 365 Commerce
author: gvrmohanreddy
ms.date: 12/10/2021
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgri
ms.search.region: Global
ms.author: gmohanv
ms.search.validFrom: 2021-12-17
ms.openlocfilehash: fc1690ff6068317c748bda0d767a10f306f3debe
ms.sourcegitcommit: a58dfb892e43921157014f0784bd411f5c40e454
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 05/04/2022
ms.locfileid: "8691455"
---
# <a name="convert-asynchronous-customers-to-synchronous-customers"></a>แปลงลูกค้าแบบเอซิงค์เป็นลูกค้าแบบซิงค์

[!include [banner](includes/banner.md)]

หัวข้อนี้อธิบายวิธีการแปลงลูกค้าแบบอะซิงโครนัสเป็นลูกค้าแบบซิงโครนัสใน Microsoft Dynamics 365 Commerce

วิธีการแปลงลูกค้าแบบอะซิงโครนัสเป็นลูกค้าแบบซิงโครนัส ให้ทำตามขั้นตอนเหล่านี้

1. ใน Commerce Headquarters ให้เรียกใช้ **งาน P** เพื่อส่งลูกค้าแบบอะซิงโครนัสไปยัง Commerce Headquarters
1. เรียกใช้งาน **ซิงโครไนส์ลูกค้าและคู่ค้าธุรกิจจากโหมดเอซิงค์** เพื่อสร้างรหัสบัญชีลูกค้า (ก่อนหน้านี้งานชื่อว่า **ซิงโครไนส์ลูกค้าและคู่ค้าธุรกิจจากโหมดเอซิงค์**)
1. เรียกใช้งาน **1010** เพื่อซิงค์รหัสบัญชีลูกค้าใหม่กับช่องทางการขาย

ถ้าใบสั่งอ้างอิงลูกค้าหรือที่อยู่แบบอะซิงโครนัสที่ยังไม่ได้ซิงค์กับ Commerce Headquarters ลูกค้าหรือที่อยู่จะถูกซิงค์เป็นส่วนหนึ่งของชุดงาน **ซิงโครไนส์ใบสั่ง** ถ้าธุรกรรมเงินสดและการขนส่งอ้างอิงลูกค้าหรือที่อยู่แบบอะซิงโครนัส ลูกค้าหรือที่อยู่จะถูกซิงค์ก่อนการลงรายการบัญชีสิ้นสุดวัน (EOD)

## <a name="additional-resources"></a>ทรัพยากรเพิ่มเติม

[การจัดการลูกค้าหน้าร้าน](customer-mgmt-stores.md)

[โหมดการสร้างลูกค้าแบบอะซิงโครนัส](async-customer-mode.md)

[แอททริบิวต์สำหรับลูกค้า](dev-itpro/customer-attributes.md)

[การยกเว้นข้อมูลออฟไลน์](dev-itpro/implementation-considerations-cdx.md#offline-data-exclusion)
