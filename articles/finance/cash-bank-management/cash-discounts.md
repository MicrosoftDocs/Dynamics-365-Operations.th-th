---
title: ส่วนลดเงินสด
description: บัญชีเจ้าหนี้และบัญชีลูกหนี้มีการกำหนดและใช้ส่วนลดเงินสดร่วมกัน  ส่วนลดเงินสดสามารถกำหนดในใบแจ้งหนี้ของลูกค้าหรือใบแจ้งหนี้ของผู้จัดจำหน่าย และจะได้รับหากชำระใบแจ้งหนี้ภายในวันที่ให้ส่วนลดเงินสด
author: kweekley
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CashDisc
audience: Application User
ms.reviewer: roschlom
ms.custom: 3741
ms.assetid: c25f9d85-2702-46aa-8e61-0b4886e069b3
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 9d4f6d5bdf4f2fdc4529d9f51515ed2ac4b5b3b5
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 01/15/2021
ms.locfileid: "4985323"
---
# <a name="cash-discounts"></a>ส่วนลดเงินสด

[!include [banner](../includes/banner.md)]

บัญชีเจ้าหนี้และบัญชีลูกหนี้มีการกำหนดและใช้ส่วนลดเงินสดร่วมกัน  ส่วนลดเงินสดสามารถกำหนดในใบแจ้งหนี้ของลูกค้าหรือใบแจ้งหนี้ของผู้จัดจำหน่าย และจะได้รับหากชำระใบแจ้งหนี้ภายในวันที่ให้ส่วนลดเงินสด 

## <a name="cash-discounts"></a>ส่วนลดเงินสด

สามารถสร้างส่วนลดเงินสดสำหรับทั้งลูกค้าหรือผู้จัดจำหน่ายในหน้าส่วนลดเงินสด คุณยังสามารถกำหนด โดยการใช้ฟิลด์รหัสส่วนลดถัดไป ชุดของส่วนลดเงินสดที่สำเร็จอื่นๆตามวันหมดอายุส่วนลดเงินสดก่อนหน้านี้ สำหรับข้อมูลเพิ่มเติม ดู "ตัวอย่าง: ชุดของส่วนลดเงินสด" ภายหลังในหัวข้อนี้ ถ้าใบแจ้งหนี้ ธุรกรรมเครดิต (การชำระเงินหรือใบลดหนี้), หรือทั้งสองอย่างถูกป้อนในสกุลเงินอื่นนอกเหนือจากสกุลเงินทางบัญชีของนิติบุคคล ส่วนลดเงินสดจะถูกคำนวณโดยการใช้อัตราแลกเปลี่ยน ตามวันที่ของการชำระเงินหรือใบลดหนี้ ถ้ามีป้อนเอกสารใบแจ้งหนี้และเครดิตในนิติบุคคลอื่น และถ้าสกุลเงินทางบัญชีสำหรับนิติบุคคลแตกต่างกัน อัตราแลกเปลี่ยนจะนำมาจากนิติบุคคลของใบแจ้งหนี้ ตามวันที่ของเอกสารเครดิต สำหรับข้อมูลเพิ่มเติม ดู "ตัวอย่าง: อัตราแลกเปลี่ยนสำหรับส่วนลดเงินสด" ภายหลังในหัวข้อนี้

## <a name="defaulting-order-of-cash-discount-main-account"></a>ค่าเริ่มต้นใบสั่งของบัญชีหลักของส่วนลดเงินสด

ถ้ามีการชำระเงินตามใบแจ้งหนี้ภายในเวลาที่จะได้รับส่วนลดเงินสด จะมีการลงรายการบัญชีส่วนลดเงินสดโดยอัตโนมัติที่บัญชีหลักของส่วนลดเงินสดตามระดับความสำคัญของค่าเริ่มต้นต่อไปนี้
1.  บัญชีหลักที่ระบุในฟิลด์บัญชีส่วนลดเงินสดอื่นบนหน้าชำระธุรกรรมที่ค้างอยู่ของลูกค้าหรือหน้าชำระธุรกรรมที่ค้างอยู่ของผู้จัดจำหน่าย
2.  บัญชีหลักที่ระบุในฟิลด์ส่วนลดเงินสดสำหรับลูกค้าหรือฟิลด์ส่วนลดเงินสดของผู้จัดจำหน่ายของกลุ่มการลงรายการบัญชีแยกประเภทที่กำหนดให้กับรหัสภาษีขายของใบแจ้งหนี้ ตั้งค่ากลุ่มการลงรายการบัญชีแยกประเภทบนหน้ากลุ่มการลงรายการบัญชีแยกประเภทและกำหนดให้กับรหัสภาษีขายในหน้ารหัสภาษีขาย
3.  บัญชีลงรายการบัญชีหลักบนหน้าส่วนลดเงินสดในบัญชีหลักสำหรับฟิลด์ส่วนลดของลูกค้าหรือบัญชีหลักสำหรับฟิลด์ส่วนลดของผู้จัดจำหน่ายสำหรับรหัสส่วนลดเงินสดที่อยู่บนใบแจ้งหนี้ที่ชำระแล้ว
4.  บัญชีหลักสำหรับส่วนลดเงินสด ตามที่กำหนดไว้ในหน้าบัญชีสำหรับธุรกรรมอัตโนมัติ

## <a name="example-series-of-cash-discounts"></a> ตัวอย่าง: ชุดของส่วนลดเงินสด
ตั้งค่ารหัสส่วนลดเงินสดสามรหัสดังต่อไปนี้
-   รหัส 5D10% - ส่วนลดเงินสด 10% เมื่อชำระเงินภายใน 5 วัน
-   รหัส 10D5% - ส่วนลดเงินสด 5% เมื่อชำระเงินภายใน 10 วัน
-   รหัส 14D2% - ส่วนลดเงินสด 2% เมื่อชำระเงินภายใน 14 วัน

ในฟิลด์รหัสส่วนลดถัดไป:
-   สำหรับรหัส 5D10% ให้เลือก 10D5%
-   สำหรับรหัส 10D5% ให้เลือก 14D2%
-   สำหรับรหัส 14D2% ให้ปล่อยให้ฟิลด์รหัสส่วนลดถัดไปเว้นว่างไว้

ส่วนลดเงินสดทั้งสามจะต่อเนื่องกันตามวันชำระเงินเกินวันส่วนลดเงินสดก่อนหน้านี้บนใบแจ้งหนี้ มีการให้ส่วนลดเงินสดเพียงส่วนลดเดียวเท่านั้นเมื่อมีการชำระเงินตามใบแจ้งหนี้ ตามวันของส่วนลดเงินสดที่จะเป็นไปตามลำดับส่วนลดเงินสด

## <a name="example-exchange-rates-for-cash-discounts"></a> ตัวอย่าง: อัตราแลกเปลี่ยนสำหรับส่วนลดเงินสด
สกุลเงินทางบัญชีนิติบุคคลของคุณคือ EUR และอัตราแลกเปลี่ยนต่อไปนี้จะระบุสำหรับ USD:
-   กุมภาพันธ์ 1 = 110
-   1 มีนาคม = 80

ใบแจ้งหนี้สำหรับ USD 1000 กับเงื่อนไขส่วนลดเงินสดของ 20D2% ที่ลงรายการบัญชีในวันที่ 15 กุมภาพันธ์ ยอดเงินสกุลเงินทางบัญชีของใบแจ้งหนี้เป็น 1100 EUR การชำระเงินสำหรับ USD 980 ที่มีการชำระด้วยใบแจ้งหนี้ในวันที่ 1 มีนาคม ยอดส่วนลดเงินสดคือ USD 20 ยอดเงินในสกุลเงินทางบัญชีของการชำระเงินคือ 784 EUR ยอดเงินในสกุลเงินทางบัญชีของส่วนลดเงินสดจะคำนวณโดยการใช้อัตราแลกเปลี่ยน ณ วันที่ 1 มีนาคม: 20 \* 80 / 100 = 16 EUR.

> [!NOTE]
> คำนวณส่วนลดเงินสดสำหรับตัวเลือกการชำระเงินบางส่วนที่ถูกเลือกในหน้าพารามิเตอร์บัญชีลูกหนี้หรือพารามิเตอร์บัญชีเจ้าหนี้ อัตราแลกเปลี่ยนที่มีผลบังคับในวันที่ของ แต่ละการชำระเงินบางส่วนจะถูกใช้ 

