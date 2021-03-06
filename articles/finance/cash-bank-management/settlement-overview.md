---
title: ภาพรวมของการชำระเงิน
description: หัวข้อนี้ให้ข้อมูลทั่วไปเกี่ยวกับกระบวนการชำระเงิน การทำเช่นนี้อธิบายถึงชนิดของธุรกรรมที่สามารถชำระเงินได้ และกำหนดเวลาและกระบวนการสำหรับการชำระเงินได้ นอกจากนี้ยังอธิบายถึงผลลัพธ์ของกระบวนการชำระเงิน
author: kweekley
manager: AnnBe
ms.date: 04/10/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CustOpenTrans, LedgerJournalTransCustPaym, LedgerJournalTransVendPaym, VendOpenTrans
audience: Application User
ms.reviewer: roschlom
ms.custom: 14551
ms.assetid: 0968fa71-5984-415b-8689-759a0136d5d1
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2018-10-31
ms.dyn365.ops.version: 8.0999999999999996
ms.openlocfilehash: a4ad8a124b2de2d364e11b6a32f8845ef438e1d1
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 01/15/2021
ms.locfileid: "4989187"
---
# <a name="settlement-overview"></a>ภาพรวมของการชำระเงิน

[!include [banner](../includes/banner.md)]

หัวข้อนี้ให้ข้อมูลทั่วไปเกี่ยวกับกระบวนการชำระเงิน การทำเช่นนี้อธิบายถึงชนิดของธุรกรรมที่สามารถชำระเงินได้ และกำหนดเวลาและกระบวนการสำหรับการชำระเงินได้ นอกจากนี้ยังอธิบายถึงผลลัพธ์ของกระบวนการชำระเงิน

ระหว่างการชำระเงิน ธุรกรรมในเอกสารจะใช้กับธุรกรรมในเอกสารอื่นเพื่อเพิ่มหรือลดยอดดุลของเอกสารแต่ละฉบับ ตัวอย่างเช่น การชำระเงินสามารถใช้กับใบแจ้งหนี้ได้ ชนิดของธุรกรรมต่างๆ สามารถชำระเงินได้ที่ต่างเวลากัน และผ่านวิธีการต่างกัน กระบวนการการชำระเงินยังสามารถสร้างธุรกรรมใหม่ได้

## <a name="what-transactions-can-be-settled"></a>ธุรกรรมใดๆที่สามารถจับคู่ได้

ในบัญชีเจ้าหนี้และบัญชีลูกหนี้ การชำระเงินอาจเกิดขึ้นระหว่างชนิดธุรกรรมใดๆ ที่ส่งผลกระทบต่อยอดดุลผู้จัดจำหน่ายหรือยอดดุลลูกค้า ชนิดของธุรกรรมเหล่านี้อาจรวมถึงใบแจ้งหนี้ การชำระเงิน ใบลดหนี้ และค่าธรรมเนียม ชนิดของธุรกรรมใดๆสามารถจับคู่กับธุรกรรมชนิดอื่นๆได้ ตัวอย่างเช่น คุณสามารถจับคู่การชำระเงินตามใบแจ้งหนี้ ใบลดหนี้กับใบแจ้งหนี้ ใบแจ้งหนี้กับใบแจ้งหนี้อื่น และการชำระเงินกับการชำระเงินอื่น

คุณสามารถจับคู่การชำระเงินกับธุรกรรมในนิติบุคคลเดียวกันหรือในนิติบุคคลอื่น ในองค์กรที่ใช้รูปแบบการชำระเงินส่วนกลาง [การชำระเงินส่วนกลาง](set-up-centralized-payments.md) สามารถช่วยปรับปรุงให้กระบวนการชำระเงินมีประสิทธิภาพขึ้น

## <a name="when-to-settle-transactions"></a>เมื่อไหร่ที่ชำระธุรกรรม

ธุรกรรมสามารถชำระเงินได้เมื่อป้อนการชำระเงิน ตัวอย่างเช่น เมื่อคุณทำการชำระเงินให้ผู้จัดจำหน่าย โดยทั่วไปคุณจะเลือกว่าใบแจ้งหนี้ใดที่จะชำระเงิน โดยการเลือกใบแจ้งหนี้ คุณทำเครื่องหมายสำหรับการชำระหนี้สำหรับการชำระเงิน เมื่อเจ้าหน้าที่การชำระเงินบัญชีลูกหนี้เรกคอร์ดการชำระเงินของลูกค้า พวกเขาสามารถทำเครื่องหมายใบแจ้งหนี้ที่เหมาะสมสำหรับการชำระหนี้ โดยยึดตามข้อมูลที่มาพร้อมกับการชำระเงินของลูกค้าแต่ละราย คุณใช้หน้า **การชำระธุรกรรม** เพื่อทำเครื่องหมายธุรกรรมสำหรับการชำระเงิน คุณสามารถเปิดหน้านี้จากการไม่ลงรายการบัญชีใบแจ้งหนี้หรือการชำระเงิน เมื่อธุรกรรมถูกลงรายการบัญชี การชำระเงินจะถูกลงรายการบัญชีด้วย 

ธุรกรรมสามารถจับคู่หลังจากที่มีการลงรายการบัญชี คุณสามารถป้อนและลงรายการบัญชีการชำระเงินของลูกค้าโดยไม่มีการชำระเงินตามใบแจ้งหนี้ใด ๆ อย่างไรก็ตาม คุณอาจต้องทำให้แน่ใจว่าการชำระเงินถูกจับคู่กับใบแจ้งหนี้อย่างถูกต้องก่อนที่คุณลงรายการบัญชีการชำระเงิน หน้า **ชำระธุรกรรม** สามารถเปิดได้จากหน้า **ลูกค้าทั้งหมด** หรือ **ผู้จัดจำหน่ายทั้งหมด** หรือจากหน้า **ธุรกรรม** สำหรับลูกค้าหรือผู้จัดจำหน่ายใด ๆ ได้

คุณยังสามารถจองการชำระเงินล่วงหน้าที่ลงรายการบัญชีสำหรับใบแจ้งหนี้ได้ โดยการทำเครื่องหมายการชำระเงินสำหรับการชำระหนี้ตามใบสั่งซื้อหรือใบสั่งขาย ในกรณีนี้ การชำระเงินจะยังคงมียอดดุลยกมา แต่ไม่สามารถจับคู่กับใบแจ้งหนี้อื่น การชำระเงินจะถูกจับคู่กับใบแจ้งหนี้ที่สร้างขึ้นจากใบสั่งซื้อหรือใบสั่งขายโดยอัตโนมัติ

## <a name="how-to-settle-transactions"></a>วิธีการชำระธุรกรรม

คุณสามารถจับคู่ธุรกรรมด้วยตนเอง โดยอัตโนมัติ หรือโดยใช้การรวมกันของสองวิธีก็ได้ การเลือกวิธีการชำระเงินจะขึ้นอยู่กับกระบวนการทางธุรกิจของคุณ บนหน้า **พารามิเตอร์ของบัญชีเจ้าหนี้** และ **พารามิเตอร์ของบัญชีลูกหนี้** คุณสามารถตั้งค่าคอนฟิกกระบวนการชำระเงินเพื่อให้สอดคล้องกับกระบวนการทางธุรกิจเหล่านั้น

คุณสามารถสร้างการชำระเงินของผู้จัดจำหน่ายและการชำระเงินของลูกค้าแบบการหักบัญชีเงินฝากอัตโนมัติโดยใช้ข้อเสนอการชำระ ข้อเสนอการชำระเงินจะใช้ในการเลือกใบแจ้งหนี้ที่จะชำระ การประชุมข้อเสนอการชำระเงินถูกเริ่มต้นด้วยตนเอง และจากนั้น ระบบจะทำเครื่องหมายใบแจ้งหนี้ที่เลือกโดยอัตโนมัติสำหรับการชำระเงิน เมื่อมีการสร้างการชำระเงิน

ถ้าการชำระเงินจะถูกสร้างขึ้นด้วยตนเอง คุณสามารถใช้หน้า **ชำระธุรกรรม** เพื่อเลือกใบแจ้งหนี้สำหรับการชำระเงินได้ คุณสามารถเลือกใบแจ้งหนี้ด้วยตนเองได้ หรือคุณสามารถใช้ตัวเลือก **ทำเครื่องหมายโดยเรียงตามระดับความสำคัญ** เพื่อให้ใบแจ้งหนี้ที่ทำเครื่องหมายสำหรับการชำระเงินโดยอัตโนมัติ ตัวเลือก **ทำเครื่องหมายโดยเรียงตามระดับความสำคัญ** จะพร้อมใช้งานเฉพาะสำหรับบัญชีลูกหนี้ คุณสามารถเปิดใช้งานตัวเลือกนี้ได้บนแท็บ **ระดับความสำคัญของการชำระเงิน** ของหน้า **พารามิเตอร์ของบัญชีลูกหนี้**

ถ้าเจ้าหน้าที่ฝ่ายชำระเงินป้อนการชำระเงิน แต่ไม่ชำระเงินนั้นก่อนที่มีการลงรายการบัญชี การชำระเงินจะสามารถถูกชำระโดยอัตโนมัติได้ คุณสามารถเปิดใช้งานการชำระเงินอัตโนมัติในหน้า **พารามิเตอร์ของบัญชีลูกหนี้** และ **พารามิเตอร์ของบัญชีเจ้าหนี้** ได้ การชำระเงินอัตโนมัติชำระเงินธุรกรรมเฉพาะในนิติบุคคลเดียวกันเท่านั้น ไม่มีการชำระธุรกรรมระหว่างนิติบุคคลหลายราย

เมื่อคุณใช้การชำระเงินอัตโนมัติ คุณสามารถใช้ระดับความสำคัญการชำระเงินล่วงหน้าได้ หรือคุณสามารถกำหนดระดับความสำคัญของการชำระเงินของคุณเองในหน้า **พารามิเตอร์ของบัญชีลูกหนี้** ได้ ฟังก์ชันนี้จะพร้อมใช้งานเฉพาะสำหรับบัญชีลูกหนี้

## <a name="results-of-settlement"></a>ผลลัพธ์ของการชำระเงิน

เมื่อธุรกรรมมีการชำระ ยอดดุลคงค้างของธุรกรรมแต่ละรายการจะเพิ่มหรือลดตามความเหมาะสม โดยทั่วไป เมื่อใบแจ้งหนี้และการชำระเงินมีการชำระเงิน สถานะและยอดดุลของธุรกรรมแต่ละรายการจะมีการอัพเดตตามกฎต่อไปนี้

- หากยอดการชำระเงินมากกว่ายอดเงินใบแจ้งหนี้ ยอดดุลใบแจ้งหนี้จะลดลงเป็น 0.00 และใบแจ้งหนี้จะถูกปิด การชำระเงินยังคงเปิดอยู่ และยอดดุลเป็นความแตกต่างระหว่างยอดการชำระเงินและยอดใบแจ้งหนี้
- หากยอดการชำระเงินน้อยกว่ายอดเงินใบแจ้งหนี้ ยอดดุลใบแจ้งหนี้จะลดลงเป็น 0.00 และใบแจ้งหนี้จะถูกปิด ใบแจ้งหนี้ยังคงเปิดอยู่ และยอดดุลเป็นความแตกต่างระหว่างยอดใบแจ้งหนี้และยอดการชำระเงิน
- หากยอดการชำระเงินเท่ากับยอดใบแจ้งหนี้ ทั้งการชำระเงินและใบแจ้งหนี้จะถูกปิดไป และยอดดุลของทั้งสองอย่างจะลดลงเป็น 0.00

หาก [ยอดการชำระเงินน้อยกว่ายอดเงินใบแจ้งหนี้](../accounts-payable/vendor-payments-partial-amount.md) เนื่องจากมีส่วนลดเงินสด มีการตัดจ่าย หรือมีการชำระน้อยเกิน ใบแจ้งหนี้และการชำระเงินอาจยังคงปิดอยู่ ขึ้นอยู่กับการตั้งค่าคอนฟิกการชำระเงินในหน้า **พารามิเตอร์ของบัญชีเจ้าหนี้** และ **พารามิเตอร์ของบัญชีลูกหนี้**

การชำระเงินสามารถสร้างธุรกรรมได้ด้วย ตัวอย่างเช่น การชำระหนี้ของใบแจ้งหนี้และการชำระเงินอาจทำให้เกิดส่วนลดเงินสด กำไรที่รับรู้หรือขาดทุน การปรับปรุงภาษีขาย การตัดจ่าย หรือผลต่างเศษสตางค์

## <a name="identifying-marked-transactions-during-settlement"></a>การระบุธุรกรรมที่ทำเครื่องหมายในระหว่างการชำระเงิน

เมื่อคุณพยายามชำระเงินธุรกรรม คุณอาจสังเกตเห็นสัญลักษณ์ที่ระบุว่าธุรกรรมถูกทำเครื่องหมายไว้ในที่ตั้งอื่น ในกรณีนี้ คุณสามารถเลือกธุรกรรมบนหน้า **ธุรกรรมการชำระเงิน** แล้วเลือก **การสอบถาม \> การชำระเงินจากหน้าต่างการชำระเงิน** มุมมองสำหรับการสอบถามนี้แสดงสมุดรายวัน ใบสั่งขาย ใบแจ้งหนี้ ข้อเสนอการชำระเงิน และที่ตั้งลูกค้า ซึ่งอาจบล็อกธุรกรรมจากการชำระเงิน เมื่อต้องการแก้ไขปัญหานี้ คุณสามารถเลือกลิงค์ที่จะไปยังสถานที่ที่ถูกบล็อคโดยตรงจากการสอบถาม คุณสามารถอัพเดตเอกสารที่มีการปรับปรุงที่จำเป็นสำหรับการชำระเงิน นอกจากนี้คุณยังสามารถใช้ตัวบ่งชี้ **ที่ทำเครื่องหมาย** เพื่อระบุเอกสารอื่นๆ ที่รวมอยู่ในที่ตั้งการบล็อคเดียวกันได้อีกด้วย

## <a name="additional-resources"></a>ทรัพยากรเพิ่มเติม

- [ส่วนที่เหลือที่ต้องชำระบัญชี](settle-remainder.md)
