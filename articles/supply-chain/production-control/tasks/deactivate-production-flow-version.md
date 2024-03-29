---
title: ยกเลิกการเรียกใช้เวอร์ชันขั้นตอนการผลิต
description: 'เมื่อไม่ต้องการรุ่นของขั้นตอนการผลิตที่ใช้งานอยู่แล้ว สามารถถูกปิดใช้งานได้ '
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
ms.openlocfilehash: 1691dc644e2e191a9e74980784d6dcf741dcd598
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 09/29/2021
ms.locfileid: "7576771"
---
# <a name="deactivate-a-production-flow-version"></a>ยกเลิกการเรียกใช้เวอร์ชันขั้นตอนการผลิต

[!include [banner](../../includes/banner.md)]

เมื่อไม่ต้องการรุ่นของขั้นตอนการผลิตที่ใช้งานอยู่แล้ว สามารถถูกปิดใช้งานได้  คุณควรใช้ตัวเลือกนี้หากกฎคัมบังและกิจกรรมทั้งหมดสิ้นแล้ว และจะไม่ทำงานอีกครั้งเท่านั้น โปรดทราบว่า วันที่หมดอายุของกฎคัมบังทั้งหมดที่เกี่ยวข้องกับเวอร์ชันขั้นตอนการผลิตนี้จะถูกปรับปรุงด้วยวันที่ปัจจุบันและเวลา 

เมื่อต้องการแก้ไขเวอร์ชันขั้นตอนการผลิตที่ใช้งานอยู่ พิจารณาการตั้งค่าวันหมดอายุสำหรับเวอร์ชันที่ใช้งานอยู่ และสร้างเวอร์ชันใหม่ ซึ่งจะอนุญาตให้คุณดำเนินต่อการดำเนินงานผลิตต่อขณะกำลังเตรียมเวอร์ชันใหม่และกฎคัมบังที่เกี่ยวข้องได้ 

เมื่อต้องทำให้เวอร์ชันขั้นตอนการผลิตที่ใช้งานอยู่หมดอายุ ต้องตั้งค่าวันหมดอายุ ในแง่นั้น การปิดใช้งานจะเหมือนกับข้อยกเว้นมากกว่ากฎ 

สำหรับขั้นตอนนี้ คุณต้องการขั้นตอนการผลิตเวอร์ชันที่สามารถปิดใช้งานได้ อย่าลองทำสิ่งนี้ในสภาพแวดล้อมการผลิต เว้นแต่คุณจะแน่ใจ 100% ว่ารุ่นดังกล่าวล้าสมัยแล้วโดยสมบูรณ์


## <a name="deactivate-a-production-flow-version"></a>ยกเลิกการเรียกใช้เวอร์ชันขั้นตอนการผลิต
1. ไปที่การควบคุมการผลิต > การตั้งค่า > ขั้นตอนการผลิตแบบ lean > ขั้นตอนการผลิต
2. ในรายการนี้ ให้ค้นหาและเลือกเรกคอร์ดที่ต้องการ
3. ในรายการนี้ ให้คลิกลิงค์ในแถวที่เลือก
4. ในรายการนี้ ให้ค้นหาและเลือกเรกคอร์ดที่ต้องการ
5. คลิก ปิดใช้งาน
    * อย่าดำเนินการต่อ หากคุณไม่มั่นใจ 100% ว่ารุ่นของขั้นตอนการผลิตนี้ล้าสมัย  เมื่อคลิก ตกลง หมายความว่ากฎคัมบังที่ใช้งานอยู่ทั้งหมดจะหมดอายุลง และกิจกรรมการผลิตและการเติมสินค้าของรุ่นของขั้นตอนการผลิตนี้จะหยุดทันที  
6. คลิก ตกลง



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]