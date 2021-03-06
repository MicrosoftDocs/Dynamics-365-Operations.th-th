---
title: แบบแผนการเช่าสินทรัพย์
description: หัวข้อนี้อธิบายแบบแผนสินทรัพย์ที่ให้เช่า
author: moaamer
manager: Ann Beebe
ms.date: 1/14/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: AssetLease
audience: Application User
ms.reviewer: roschlom
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2021-1-28
ms.dyn365.ops.version: 10.0.17
ms.openlocfilehash: ea89d54f1ce3a1e971d41623bf44f909f7dfdf09
ms.sourcegitcommit: f8bac7ca2803913fd236adbc3806259a17a110f4
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 02/06/2021
ms.locfileid: "5131309"
---
# <a name="asset-leasing-conventions"></a>แบบแผนการเช่าสินทรัพย์

[!include [banner](../includes/banner.md)]

หัวข้อนี้อธิบายแบบแผนสินทรัพย์ที่ให้เช่า แบบแผนการเช่าใช้ในการระบุวันที่เริ่มต้นของสมุดบัญชีการเช่า หากแบบแผนการเช่าได้รับการตั้งค่าเป็น **ไม่มี** วันที่เริ่มต้นจะเหมือนกับวันที่เริ่มต้นของการเช่า (กล่าวคือ ค่าของฟิลด์ **วันที่เริ่มต้นการเช่า** ) หากแบบแผนการเช่าได้รับการตั้งค่าเป็น **เต็มเดือน** วันที่เริ่มต้นคือวันแรกของเดือนที่เป็นวันที่เริ่มต้นของสัญญาเช่า

วันที่เริ่มต้นจะระบุวันที่เริ่มต้นของรอบระยะเวลาที่ตัดบัญชีหนี้สินและการจัดกำหนดการการคิดค่าเสื่อมราคาสินทรัพย์ ดอกเบี้ยจ่ายและค่าเสื่อมราคาจะลงรายการบัญชีในวันที่สิ้นสุดรอบระยะเวลาของกำหนดการที่เกี่ยวข้อง การรับรู้เบื้องต้นและการปรับปรุงรายการสมุดรายวันมีการลงรายการบัญชีไว้ในวันที่เริ่มต้น

> [!NOTE]
> ลักษณะการทำงานของแบบแผนการเช่าจะต้องเปิดใช้งานผ่านการจัดการคุณลักษณะ ในพื้นที่ทำงาน **การจัดการคุณลักษณะ** ให้ค้นหาและเลือกคุณลักษณะที่ชื่อคุณลักษณะ **แบบแผนการเช่าสำหรับการเช่าสินทรัพย์** แล้วเลือก **เปิดใช้งานตอนนี้**

มีการกำหนดแบบแผนการเช่าให้กับการตั้งค่าของสมุดบัญชีสินทรัพย์การเช่า

เมื่อต้องการดูหรือกําหนดแบบแผนการเช่า ให้ปฏิบัติตามขั้นตอนเหล่านี้

1. ไปที่ **การเช่าสินทรัพย์ \> การตั้งค่า \> สมุดบัญชีสัญญาเช่า**
2. ในฟิลด์ **แบบแผนการเช่า** ให้เลือกหนึ่งในค่าต่อไปนี้

    | ข้อตกลงการเช่า | คำอธิบาย |
    |--------------------|-------------|
    | None               | การตัดบัญชีหนี้สินและกำหนดการคิดค่าเสื่อมราคาสินทรัพย์จะเริ่มต้นในวันที่เริ่มต้นของการเช่า เนื่องจากวันที่เริ่มต้นจะเท่ากับวันที่เริ่มต้นการเช่า วันที่สิ้นสุดคือหนึ่งเดือนหลังจากนั้น แบบแผนการเช่านี้ไม่ได้รับประกันว่าจะมีการลงรายการบัญชีดอกเบี้ยในวันสุดท้ายของแต่ละเดือน |
    | เต็มเดือน         | สำหรับสัญญาเช่าที่มีวันที่เริ่มต้นที่เกิดขึ้นเมื่อใดก็ได้ในระหว่างเดือน การตัดบัญชีหนี้สินและกำหนดการการคิดค่าเสื่อมราคาสินทรัพย์จะเริ่มต้นค่าใช้จ่ายค้างจ่ายในวันแรกของเดือนนั้น แบบแผนการเช่านี้ช่วยให้มั่นใจว่าจะมีการตั้งค้างรับดอกเบี้ยในวันสุดท้ายของแต่ละเดือนตลอดทั้งเดือน |

3. เลือก **บันทึก**

เมื่อมีการสร้างสัญญาเช่า วันที่เริ่มต้นของสมุดบัญชีแต่ละเล่มจะมีการป้อนข้อมูลโดยอัตโนมัติตามวันที่เริ่มต้นที่ป้อนไว้ให้กับสัญญาเช่าและแบบแผนการเช่าที่ระบุไว้ในสมุดบัญชี
