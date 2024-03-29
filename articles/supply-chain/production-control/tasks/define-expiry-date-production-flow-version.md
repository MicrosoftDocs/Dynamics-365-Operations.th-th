---
title: กำหนดวันหมดอายุสำหรับรุ่นขั้นตอนการผลิต
description: 'เมื่อต้องการสิ้นสุดการมีผลบังคับใช้และการประมวลผลรุ่นของขั้นตอนการผลิตในวันที่กำหนด หรือเมื่อต้องการวางแผนการเปลี่ยนรุ่นที่ใช้งานอยู่เป็นรุ่นใหม่ คุณจะต้องกำหนดวันหมดอายุของรุ่น '
author: johanhoffmann
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: LeanProductionFlow
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 9f6ee9177664767c31eaa3e9b65d7559a1a9662f
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 09/29/2021
ms.locfileid: "7574436"
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