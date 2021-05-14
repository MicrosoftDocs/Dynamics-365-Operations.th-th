---
title: เรกคอร์ด TaxTrans ไม่ถูกสร้าง
description: หัวข้อนี้มีข้อมูลการแก้ไขปัญหาที่สามารถช่วยเรกคอร์ด TaxTrans ไม่ถูกสร้าง
author: qire
manager: beya
ms.date: 04/13/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application user
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: wangchen
ms.search.validFrom: 2021-04-01
ms.dyn365.ops.version: 10.0.1
ms.openlocfilehash: 0c7414cc39198ff4d5be9b4c41ca62f9c78c9250
ms.sourcegitcommit: 57668404d61359b33e0c0280f2f7c4eb829b1ed2
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 04/27/2021
ms.locfileid: "5947715"
---
# <a name="taxtrans-record-isnt-generated"></a>เรกคอร์ด TaxTrans ไม่ถูกสร้าง

[!include [banner](../includes/banner.md)]

ถ้าคุณเลือก **ภาษีขายที่ลงรายการบัญชีแล้ว** ของธุรกรรม แต่หน้า **ภาษีขายที่ลงรายการบัญชี** ไม่แสดงรายการภาษีหรือไม่มีรายการภาษี แสดงว่าเรกคอร์ด **TaxTrans** อาจไม่ได้ถูกสร้างขึ้น

[![หน้าภาษีขายที่ลงรายการบัญชีที่ไม่มีสินค้าในรายการ](./media/taxtrans-is-not-generated-Picture1.png)](./media/taxtrans-is-not-generated-Picture1.png)

เมื่อต้องการแก้ไขปัญหานี้ ให้ปฏิบัติตามขั้นตอนในส่วนต่อไปนี้ตามต้องการ

## <a name="check-the-sales-tax-before-you-post-the-transaction"></a>ตรวจสอบภาษีขายก่อนที่คุณจะลงรายการบัญชีธุรกรรม

1. ก่อนที่คุณจะลงรายการบัญชีธุรกรรม บนหน้า **การลงรายการบัญชีใบแจ้งหนี้** ให้เลือก **ภาษีขาย** เพื่อตรวจสอบการคํานวณ

    [![ปุ่มภาษีขายบนหน้าการลงรายการบัญชีใบแจ้งหนี้](./media/taxtrans-is-not-generated-Picture2.png)](./media/taxtrans-is-not-generated-Picture2.png)

2. บนหน้า **ธุรกรรมภาษีขายชั่วคราว** ให้ตรวจทานผลลัพธ์ของการคํานวณ ถ้าไม่มีการคํานวณภาษี ให้ดูที่ [ภาษีไม่ได้คํานวณหรือยอดภาษีเป็นศูนย์](sales-tax-troubleshooting-tax-not-calculated-amount-zero.md)

## <a name="find-the-taxtrans-record-in-all-posted-sales-tax"></a>ค้นหาเรกคอร์ด TaxTrans ในภาษีขายที่ลงรายการบัญชีทั้งหมด

1. ไปที่ **ภาษี** \> **การสอบถามและรายงาน** \> **การสอบถามภาษีขาย** > **ภาษีขายที่ลงรายการบัญชีแล้ว**
2. ในหัวข้อคอลัมน์ **ใบสำคัญ** ให้เลือกสัญลักษณ์ตัวกรองข้อมูลเพื่อค้นหาเรกคอร์ด **TaxTrans**
3. ถ้าคุณไม่พบเรกคอร์ดภาษีขายที่คุณค้นหา ให้ตรวจสอบวันที่ ถ้าวันที่แตกต่างจากวันที่ของหัวข้อสมุดรายวัน ให้สร้างคำขอบริการของ Microsoft เพื่อรับการสนับสนุนเพิ่มเติม

    [![หน้าภาษีขายที่ลงรายการบัญชี](./media/taxtrans-is-not-generated-Picture4.png)](./media/taxtrans-is-not-generated-Picture4.png)

## <a name="debug-to-check-details"></a>ดีบักเพื่อตรวจสอบรายละเอียด

1. สำหรับข้อมูลเพิ่มเติมเกี่ยวกับดีบักและระบุว่า **TmpTaxWorkTrans** และ **TaxUncommitted** สร้างขึ้นอย่างถูกต้องหรือไม่ ดู [ค่าฟิลด์ใน TaxTrans ไม่ถูกต้อง](sales-tax-troubleshooting-field-value-taxtrans-incorrect.md)
2. ถ้า **TaxTmpWorkTrans** หรือ **TaxUncommitted** ถูกสร้างขึ้นอย่างถูกต้อง ให้เพิ่มจุดสั่งหยุดที่ **TaxPost::SaveAndPost()** และ **Tax::SaveAndPost** เพื่อดีบักเหตุผลที่ไม่มีการแทรก **TaxTrans**

    [![จุดสั่งหยุดที่เพิ่มในรหัส](./media/taxtrans-is-not-generated-Picture5.png)](./media/taxtrans-is-not-generated-Picture5.png)

    [![ผลลัพธ์ของจุดสั่งหยุดที่เพิ่ม](./media/taxtrans-is-not-generated-Picture6.png)](./media/taxtrans-is-not-generated-Picture6.png)

## <a name="determine-whether-customization-exists"></a>ระบุว่ามีการเลือกเองอยู่หรือไม่

หากคุณได้เสร็จสิ้นขั้นตอนในส่วนก่อนหน้านี้แต่ไม่พบปัญหา ให้ระบุว่ามีการเลือกเองอยู่หรือไม่ ถ้าไม่มีการเลือกเองอยู่ ให้สร้างคำขอบริการของ Microsoft เพื่อขอความช่วยเหลือเพิ่มเติม

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
