---
title: ตั้งค่าชื่อสมุดรายวันสัญญาเช่า
description: บทความนี้จะอธิบายถึงวิธีการกำหนดชื่อสมุดรายวันสัญญาเช่า ชื่อสมุดรายวันสัญญาเช่าระบุสมุดรายวันที่มีการลงรายการบัญชีการชำระบัญชีสินทรัพย์
author: moaamer
ms.date: 12/03/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: AssetLeasePostingAccounts
audience: Application User
ms.reviewer: kfend
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-10-28
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 678587e0846f6ce6d6d8113290a90b3f4d1988cc
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 06/03/2022
ms.locfileid: "8874709"
---
# <a name="set-up-lease-journal-names"></a>ตั้งค่าชื่อสมุดรายวันสัญญาเช่า

[!include [banner](../includes/banner.md)]


ชื่อสมุดรายวันสัญญาเช่าระบุสมุดรายวันที่มีการลงรายการบัญชีธุรกรรมการเช่าสินทรัพย์ เฉพาะชื่อสมุดรายวันที่ได้รับการกำหนดให้กับชนิดสมุดรายวัน **การเช่าสินทรัพย์** เท่านั้นที่จะปรากฏขึ้นในฟิลด์ **การรับรู้เริ่มต้น** และ **ชื่อสมุดรายวันรายเดือน** บนหน้า **พารามิเตอร์การเช่าสินทรัพย์** เฉพาะชนิดสมุดรายวัน **การบันทึกใบแจ้งหนี้ของผู้จัดจำหน่าย** เท่านั้นที่สามารถกำหนดให้กับฟิลด์ **ชื่อสมุดรายวันใบแจ้งหนี้** ได้

ระบบล็อคฟิลด์ทางการเงินบางอย่างไม่ให้มีการแก้ไข เพื่อป้องกันไม่ให้เกิดผลต่างใดๆ ระหว่างธุรกรรมและกำหนดการ ฟิลด์บางฟิลด์ที่ถูกล็อคได้แก่ **บัญชีt** **ยอดเงิน** **มิติทางการเงิน** **สกุลเงิน** และ **ชนิดธุรกรรม** นอกจากนี้ คุณจะไม่สามารถเพิ่มหรือลบรายการสมุดรายวันในรายการสมุดรายวันสินทรัพย์ใดๆ ได้ เนื่องจากอาจทําให้เกิดผลต่างระหว่างกำหนดการและธุรกรรม


เมื่อต้องการตั้งค่าคอนฟิกชื่อสมุดรายวันสัญญาเช่า ให้ทำตามขั้นตอนต่อไปนี้

1. ไปที่ **การเช่าสินทรัพย์ \> การตั้งค่า \> พารามิเตอร์การเช่าสินทรัพย์**
2. บนแท็บ **ทั่วไป** ในฟิลด์ **ชื่อสมุดรายวันการรับรู้เริ่มต้น** และเลือกสมุดรายวัน รายการสมุดรายวันการรับรู้เริ่มต้นทั้งหมดจะถูกลงรายการบัญชีในชื่อสมุดรายวันนี้
3. ในฟิลด์ **ชื่อสมุดรายวันใบแจ้งหนี้** ให้เลือกสมุดรายวัน ถ้าตัวเลือก **ชำระให้แก่ผู้จัดจำหน่าย** ตั้งค่าเป็น **ใช่** สำหรับสมุดบัญชีค่าเช่า สัญญาเช่า และใบแจ้งหนี้การชำระเงินค่าใช้จ่ายจะถูกลงรายการบัญชีในชื่อสมุดรายวันนี้
4. ในฟิลด์ **ชื่อสมุดรายวันสัญญาเช่า** ให้เลือกสมุดรายวัน การคิดค่าเสื่อมราคา ดอกเบี้ย และรายการที่จัดประเภทระยะสั้นทั้งหมดจะมีการลงรายการบัญชีในชื่อสมุดรายวันนี้ ถ้าตัวเลือก **ชำระให้แก่ผู้จัดจำหน่าย** ตั้งค่าเป็น **ไม่** สำหรับสมุดบัญชีค่าเช่า การชำระค่าเช่า และรายการการชำระเงินค่าใช้จ่ายจะถูกลงรายการบัญชีในชื่อสมุดรายวันนี้
5. ในฟิลด์ **ชื่อสมุดรายวันการแก้ไขสัญญาเช่า** ให้เลือกสมุดรายวัน ธุรกรรมการปรับปรุงสัญญาเช่า การยกเลิก และการด้อยค่าของสินทรัพย์จะมีการลงรายการบัญชีไปที่ชื่อสมุดรายวันนี้ ชื่อสมุดรายวันที่คุณเลือกไม่ควรได้รับการกำหนดลำดับงานหรือการอนุมัติ ถ้าไม่ได้กําหนดชื่อสมุดรายวันการแก้ไขสัญญาเช่า ธุรกรรมการปรับปรุงสัญญาเช่า การยกเลิก และการด้อยค่าของสินทรัพย์จะมีการลงรายการบัญชีไปยังชื่อสมุดรายวันที่เลือกไว้ในฟิลด์ **ชื่อสมุดรายวันสัญญาเช่า** 


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
