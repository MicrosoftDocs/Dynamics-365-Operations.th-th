---
title: ธุรกรรมภาษีหัก ณ ที่จ่าย ในการขาย
description: บทความนี้แสดงรายการขั้นตอนเพื่อหลีกเลี่ยงการคํานวณภาษีหัก ณ ที่จ่ายของลูกค้าที่เลือก สำหรับลูกค้าที่ระบุภาษีหัก ณ ที่จ่ายในการชำระเงินให้คุณ คุณสามารถกําหนดกลุ่มภาษีหัก ณ ที่จ่ายเริ่มต้นได้
author: kailiang
ms.date: 01/12/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.custom: 15721
ms.assetid: b4b406fa-b772-44ec-8dd8-8eb818a921ef
ms.search.region: Global
ms.author: kailiang
ms.search.validFrom: 2020-01-12
ms.dyn365.ops.version: AX 10.0.16
ms.openlocfilehash: 75a7fc62c1d493007f3aa88a723465828c557df7
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 06/03/2022
ms.locfileid: "8910097"
---
# <a name="withholding-tax-in-sales-transactions"></a>ธุรกรรมภาษีหัก ณ ที่จ่าย ในการขาย

บทความนี้แสดงรายการขั้นตอนเพื่อหลีกเลี่ยงการคํานวณภาษีหัก ณ ที่จ่ายของลูกค้าที่เลือก สำหรับลูกค้าที่ระบุภาษีหัก ณ ที่จ่ายในการชำระเงินให้คุณ คุณสามารถกําหนด **กลุ่มภาษีหัก ณ ที่จ่าย** บนหน้า **ลูกค้า** 

1. ไปที่ **บานหน้าต่างนำทาง > โมดูล > บัญชีลูกหนี้ > ลูกค้า > ลูกค้าทั้งหมด**

2. คลิกรหัสลูกค้าที่เกี่ยวข้อง ให้คลิก **แก้ไข**

3. ในแท็บ **ใบแจ้งหนี้และการจัดส่ง** ให้ตั้งค่าฟิลด์ **คํานวณภาษีหัก ณ ที่จ่าย** เป็น **ใช่**

   > [!NOTE] 
   > จะไม่คํานวณภาษีหัก ณ ที่จ่ายถ้าไม่ได้สลับ **การคํานวณภาษีหัก ณ ที่จ่าย** กับลูกค้ารายนี้ในข้อมูลหลัก

4. เลือกกลุ่มภาษีหัก ณ ที่จ่ายตามประเภทสินค้าใน **กลุ่มภาษีหัก ณ ที่จ่าย**

5. คลิก **บันทึก**

ดูสินค้า/บริการที่ต้องเสียภาษีหัก ณ ที่จ่าย คุณสามารถกําหนด **กลุ่มภาษีหัก ณ ที่จ่ายตามสินค้า** เริ่มต้น **ในผลิตภัณฑ์ที่ออกใช้แล้ว** ได้

1. ไปยัง **บานหน้าต่างนำทาง > โมดูล > การจัดการข้อมูลผลิตภัณฑ์ >ผลิตภัณฑ์ > ผลิตภัณฑ์ที่นำออกใช้**

2. คลิกหมายเลขสินค้าที่เกี่ยวข้อง ให้คลิก **แก้ไข**

3. ในแท็บ **ขาย** ให้คลิก **คํานวณภาษีหัก ณ ที่จ่าย**

   > [!NOTE] 
   > ระบบจะไม่คํานวณภาษีหัก ณ ที่จ่าย ถ้าไม่มีการตั้งค่า **คํานวณภาษีหัก ณ ที่จ่าย** เป็น **ใช่** ให้กับสินค้านี้บนแท็บ **ผลิตภัณฑ์ที่ออกใช้แล้ว** ในหน้า **ผลิตภัณฑ์**

4. เลือกกลุ่มภาษีหัก ณ ที่จ่ายตามประเภทสินค้าในรายการ **กลุ่มภาษีหัก ณ ที่จ่ายตามประเภทสินค้า**

5. คลิก **บันทึก**

คุณสามารถมอบหมายกลุ่มภาษีหัก ณ ที่จ่ายและกลุ่มภาษีหัก ณ ที่จ่ายตามประเภทสินค้าได้โดยใช้หน้า **ใบสั่งขาย** 

กลุ่มภาษีหัก ณ ที่จ่ายเริ่มต้นและกลุ่มภาษีหัก ณ ที่จ่ายตามประเภทสินค้าจะถูกใช้เป็นรายการเริ่มต้นในบรรทัดใบสั่งขาย เมื่อคุณสร้างใบสั่งขายใหม่

การคํานวณภาษีหัก ณ ที่จ่ายและลงรายการบัญชีโดยใช้ **สมุดรายวันการจ่ายของลูกค้า** คุณสามารถปรับปรุงรหัสภาษีหัก ณ ที่จ่ายที่ใช้ได้ด้วยตนเอง รวมทั้งยอดภาษีหัก ณ ที่จ่ายจริงบนแท็บ **ภาษีหัก ณ ที่จ่าย** บนหน้า **ชำระเงินธุรกรรม**

จํานวนเงินภาษีหัก ณ ที่จ่ายที่คํานวณได้จะถูกหักออกจากการจ่ายของลูกค้า และลงรายการบัญชีที่บัญชี **การชดเชยภาษีหัก ณ ที่จ่าย** ในใบแจ้งนี้


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
