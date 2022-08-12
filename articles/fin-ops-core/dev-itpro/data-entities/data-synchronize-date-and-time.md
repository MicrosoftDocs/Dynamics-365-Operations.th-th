---
title: ซิงโครไนส์วันที่และเวลาในงานการนําเข้า
description: ใช้โซนเวลา UTC ในงานการนําเข้าเพื่อหลีกเลี่ยงปัญหากับการแปลงโซนเวลา
author: peakerbl
ms.date: 12/01/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: sericks
ms.search.region: Global
ms.author: peakerbl
ms.search.validFrom: 2020-12-01
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: b8faa7b73349c48d3a02b685546b47c4969c6027
ms.sourcegitcommit: 3289478a05040910f356baf1995ce0523d347368
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 07/01/2022
ms.locfileid: "9109446"
---
# <a name="synchronize-date-and-time-in-import-jobs"></a>ซิงโครไนส์วันที่และเวลาในงานการนําเข้า

[!include [banner](../includes/banner.md)]

เป็นสิ่งสำคัญที่ต้องตั้งค่าโซนเวลาให้กับงานการนําเข้าของคุณเป็น Coordinated Universal Time (UTC) คุณอาจเห็นวันที่และเวลาที่ไม่คาดคิดในข้อมูลที่นําเข้าของคุณ ถ้าคุณใช้การตั้งค่าอื่น โดยไม่มีการตั้งค่าที่ถูกต้อง กระบวนการนําเข้าจะแปลงวันที่ UTC เป็นรูปแบบเฉพาะที่ และจากนั้น การตั้งค่าระบบจะแปลงค่านั้นอีกครั้ง

การแปลงแบบคู่นี้ส่งผลให้เกิดการเปลี่ยนแปลงวันที่ระหว่างแอปพลิเคชันต่างๆ ตัวอย่างเช่น การแปลงแบบคู่อาจทําให้วันที่เริ่มต้นของพนักงานแตกต่างกันระหว่าง Dynamics 365 Human Resources และ Dynamics 365 Finance เนื่องจากความแตกต่างในโซนเวลาเฉพาะที่ การตั้งค่างานการนําเข้าเป็น UTC จะแก้ไขปัญหานี้

1. ในการเงินและการดําเนินงานของ Dynamics 365 ให้เลือก **การจัดการข้อมูล**

2. เลือก **นําเข้าโครงการ** แล้วจากนั้น เลือกโครงการ

3. ภายใต้ **รูปแบบวันที่ต้นทาง** ให้เลือก **CSV-Unicode**

   [![เปลี่ยนรูปแบบวันที่ต้นทางเป็น UTC](./media/data-source-date-format.png)](./media/data-source-date-format.png)

4. เปลี่ยน **โซนเวลา** เป็น **Coordinated Universal Timezone** และเปลี่ยน **ภาษา** เป็น **En-US**




[!INCLUDE[footer-include](../../../includes/footer-banner.md)]

