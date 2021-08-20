---
title: กำหนดวันหมดอายุสำหรับรุ่นขั้นตอนการผลิต
description: 'เมื่อต้องการสิ้นสุดการมีผลบังคับใช้และการประมวลผลรุ่นของขั้นตอนการผลิตในวันที่กำหนด หรือเมื่อต้องการวางแผนการเปลี่ยนรุ่นที่ใช้งานอยู่เป็นรุ่นใหม่ คุณจะต้องกำหนดวันหมดอายุของรุ่น '
author: cvocph
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: LeanProductionFlow
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: f6dfb830b3180ecf4cc2bf6ccc4112581bee0da8cbe793bf53e61fd2828f51fe
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 08/05/2021
ms.locfileid: "6754619"
---
# <a name="define-an-expiry-date-for-a-production-flow-version"></a>กำหนดวันหมดอายุสำหรับรุ่นขั้นตอนการผลิต

[!include [banner](../../includes/banner.md)]

เมื่อต้องการสิ้นสุดการมีผลบังคับใช้และการประมวลผลรุ่นของขั้นตอนการผลิตในวันที่กำหนด หรือเมื่อต้องการวางแผนการเปลี่ยนรุ่นที่ใช้งานอยู่เป็นรุ่นใหม่ คุณจะต้องกำหนดวันหมดอายุของรุ่น  โดยที่คุณไม่จำเป็นต้องปิดใช้งานรุ่นนั้นๆ


## <a name="set-an-expiration-date-to-end-a-production-flow-version"></a>กำหนดวันหมดอายุเพื่อสิ้นสุดรุ่นของขั้นตอนการผลิต
1. ไปที่การควบคุมการผลิต > การตั้งค่า > ขั้นตอนการผลิตแบบ lean > ขั้นตอนการผลิต
2. ในรายการนี้ ให้ค้นหาและเลือกเรกคอร์ดที่ต้องการ
    * เลือกขั้นตอนการผลิตที่มีรุ่นที่กำหนดแล้ว  
3. ในรายการนี้ ให้คลิกลิงค์ในแถวที่เลือก
4. คลิก แก้ไข
5. ในรายการนี้ ให้ทำเครื่องหมายแถวที่เลือก
6. ในฟิลด์วันหมดอายุ ให้ป้อนวันที่และเวลา
    * สำหรับวันหมดอายุ รุ่นใหม่จะไม่เริ่มต้นหรือกลายเป็น เรียกใช้แล้ว  จะไม่สามารถสร้างหรือเริ่มต้นงานสำหรับขั้นตอนการผลิตนี้ได้อีกต่อไป คุณยังคงสามารถทำงานที่เริ่มต้นแล้วให้เสร็จสิ้นได้หลังจากวันหมดอายุ  



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]