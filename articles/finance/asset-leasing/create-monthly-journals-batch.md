---
title: สร้างรายการสมุดรายวันรายเดือนในชุดงาน
description: บทความนี้จะอธิบายเกี่ยวกับวิธีการสร้างรายการสมุดรายวันในชุดงานเพื่อช่วยเพิ่มประสิทธิภาพเมื่อมีการบันทึกค่าใช้จ่ายในการเช่ารายเดือน
author: moaamer
ms.date: 08/10/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: Dialog
audience: Application User
ms.reviewer: kfend
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-10-28
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: fb5c65b0a2c982171fa0ae88141d92c2f1ead6ac
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 06/03/2022
ms.locfileid: "8895006"
---
# <a name="create-monthly-journal-entries-in-a-batch"></a>สร้างรายการสมุดรายวันรายเดือนในชุดงาน

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]


บทความนี้จะอธิบายเกี่ยวกับวิธีการสร้างรายการสมุดรายวันในชุดงานเพื่อช่วยเพิ่มประสิทธิภาพเมื่อมีการบันทึกค่าใช้จ่ายในการเช่ารายเดือน การประมวลผลชุดงานสามารถใช้ในการสร้างรายการสมุดรายวันจากหลายกำหนดการ รายการสมุดรายวันเหล่านี้อาจรวมถึงการชำระค่าเช่า การตัดบัญชีหนี้สิน การตัดบัญชีสิทธิ์การใช้สินทรัพย์ (ROU) และค่าใช้จ่ายในการจัดการสินทรัพย์ นอกจากนี้คุณยังสามารถใช้การประมวลผลชุดงานเพื่อทำการรับรู้สัญญาเช่าหลายสัญญาในเวลาเดียวกัน หรือเพื่อสร้างการปรับปรุงการเปลี่ยนแปลงสำหรับสัญญาเช่าหลายสัญญาในเวลาเดียวกัน

เมื่อต้องการตั้งค่าชุดงาน หรือเพื่อประมวลผลใบแจ้งหนี้การชำระเงิน ค่าเสื่อมราคา หรือดอกเบี้ยสำหรับสัญญาเช่าต่าง ๆ ให้ไปที่ **การเช่าสินทรัพย์ \> ประจำงวด \> การสร้างสมุดรายวันชุดงาน** ในกล่องโต้ตอบที่ปรากฏขึ้น คุณสามารถเลือกกำหนดการที่ควรสร้างรายการสมุดรายวัน นอกจากนี้คุณยังสามารถระบุได้ว่าควรรันกระบวนการชุดงานสำหรับเอนทิตีเฉพาะ กลุ่มสัญญาเช่า หรือสมุดบัญชีสัญญาเช่า

> [!NOTE]
> ธุรกรรมลำดับต่อมา เช่น กำหนดการตัดบัญชีหนี้สิน การชำระเงิน ค่าเสื่อมราคา และค่าใช้จ่าย จะถูกลงรายการบัญชีเฉพาะหลังจากที่มีการลงรายการบัญชีการรับรู้ครั้งเริ่มต้นสำหรับสัญญาเช่าที่ตรงกันเท่านั้น
>
> รายการสมุดรายวันจะถูกสร้างขึ้น แต่จะไม่มีการลงรายการบัญชีดังกล่าวจนกว่าคุณจะเลือกคำสั่ง **รัน**

เมื่อต้องการลงรายการบัญชีสมุดรายวันการรับรู้เริ่มต้นในวันที่อื่นที่ไม่ใช่วันที่ของการอนุมัติการเช่า ให้เลือก **การกําหนดวันที่ลงรายการบัญชีการรับรู้เริ่มต้น** ฟิลด์ **วันที่** จะปรากฏขึ้นซึ่งช่วยให้คุณระบุวันที่ลงรายการบัญชีที่ถูกต้องได้

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
