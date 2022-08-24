---
title: แปลงลูกค้าแบบเอซิงค์เป็นลูกค้าแบบซิงค์
description: บทความนี้อธิบายวิธีการแปลงลูกค้าแบบอะซิงโครนัสเป็นลูกค้าแบบซิงโครนัสใน Microsoft Dynamics 365 Commerce
author: gvrmohanreddy
ms.date: 12/10/2021
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: gmohanv
ms.search.validFrom: 2021-12-17
ms.openlocfilehash: b442bfc0685706359771e4d9e2729565d3652a60
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 08/12/2022
ms.locfileid: "9278204"
---
# <a name="convert-asynchronous-customers-to-synchronous-customers"></a>แปลงลูกค้าแบบเอซิงค์เป็นลูกค้าแบบซิงค์

[!include [banner](includes/banner.md)]

บทความนี้อธิบายวิธีการแปลงลูกค้าแบบอะซิงโครนัสเป็นลูกค้าแบบซิงโครนัสใน Microsoft Dynamics 365 Commerce

วิธีการแปลงลูกค้าแบบอะซิงโครนัสเป็นลูกค้าแบบซิงโครนัส ให้ทำตามขั้นตอนเหล่านี้

1. ใน Commerce Headquarters ให้เรียกใช้ **งาน P** เพื่อส่งลูกค้าแบบอะซิงโครนัสไปยัง Commerce Headquarters
1. เรียกใช้งาน **ซิงโครไนส์ลูกค้าและคู่ค้าธุรกิจจากโหมดเอซิงค์** เพื่อสร้างรหัสบัญชีลูกค้า (ก่อนหน้านี้งานชื่อว่า **ซิงโครไนส์ลูกค้าและคู่ค้าธุรกิจจากโหมดเอซิงค์**)
1. เรียกใช้งาน **1010** เพื่อซิงค์รหัสบัญชีลูกค้าใหม่กับช่องทางการขาย

ถ้าใบสั่งอ้างอิงลูกค้าหรือที่อยู่แบบอะซิงโครนัสที่ยังไม่ได้ซิงค์กับ Commerce Headquarters ลูกค้าหรือที่อยู่จะถูกซิงค์เป็นส่วนหนึ่งของชุดงาน **ซิงโครไนส์ใบสั่ง** ถ้าธุรกรรมเงินสดและการขนส่งอ้างอิงลูกค้าหรือที่อยู่แบบอะซิงโครนัส ลูกค้าหรือที่อยู่จะถูกซิงค์ก่อนการลงรายการบัญชีสิ้นสุดวัน (EOD)

## <a name="additional-resources"></a>ทรัพยากรเพิ่มเติม

[การจัดการลูกค้าหน้าร้าน](customer-mgmt-stores.md)

[โหมดการสร้างลูกค้าแบบอะซิงโครนัส](async-customer-mode.md)

[แอตทริบิวต์สำหรับลูกค้า](dev-itpro/customer-attributes.md)

[การยกเว้นข้อมูลออฟไลน์](dev-itpro/implementation-considerations-cdx.md#offline-data-exclusion)
