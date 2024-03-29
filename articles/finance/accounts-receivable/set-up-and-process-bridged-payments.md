---
title: ตั้งค่าและดำเนินการกับการชำระเงินระหว่างกาล
description: บทความนี้จะอธิบายวิธีการตั้งและดำเนินการกับการชำระเงินระหว่างกาลของลูกค้า การชำระเงินระหว่างกาลคือการชำระเงินที่มีการลงรายการบัญชีในบัญชีแยกประเภททั่วไปในสองขั้นตอน
author: rachel-profitt
ms.date: 12/03/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: CustPaymMode, VendPaymMode, LedgerJournalTable, LedgerJournalTransCustPaym, LedgerJournalTransVendPaym, LedgerJournalTransDaily
audience: Application User
ms.reviewer: twheeloc
ms.custom: ''
ms.assetid: c64eed1d-df17-448e-8bb6-d94d63b14607
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2022-01-03
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: bb563008f156e1bfa6e4e9a705e9170342719ce7
ms.sourcegitcommit: 9740f9b41a7dcf1821c6baccb2e05b9865ac2966
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 11/15/2022
ms.locfileid: "9775180"
---
# <a name="set-up-and-process-bridged-payments"></a>ตั้งค่าและดำเนินการกับการชำระเงินระหว่างกาล

[!include [banner](../includes/banner.md)]

การชำระเงินระหว่างกาลคือการชำระเงินที่มีการลงรายการบัญชีในบัญชีแยกประเภททั่วไปในสองขั้นตอน โดยทั่วไป วิธีการนี้จะใช้เมื่อตั้งค่าวิธีการชำระเงินเป็น **ธนาคาร** และคุณต้องลงรายการบัญชีธุรกรรมในบัญชีธนาคารเฉพาะเมื่อธุรกรรมได้รับการโอนจากธนาคารแล้วเท่านั้น แต่คุณยังสามารถใช้การชำระเงินระหว่างกาลสำหรับบัญชีแยกประเภทได้ด้วย ในกรณีนี้ ยอดเงินจะถูกย้ายจากบัญชีหลักหนึ่งไปยังบัญชีหลักอื่นเมื่อดำเนินการกับการลงรายการบัญชีระหว่างกาล

คุณสามารถสร้างการชําระเงินระหว่างกาลจากบัญชีเจ้าหนี้หรือบัญชีลูกหนี้ได้ แม้ว่าบทความนี้จะอธิบายวิธีการตั้งค่าคอนฟิกการลงรายการบัญชีระหว่างกาลของบัญชีลูกหนี้ แต่ขั้นตอนของธุรกรรมบัญชีเจ้าหนี้จะคล้ายกัน

## <a name="set-up-bridging-posting"></a>การตั้งค่าการลงรายการบัญชีระหว่างกาล

เมื่อต้องการใช้การลงรายการบัญชีระหว่างกาล คุณต้องตั้งค่าวิธีการชำระเงินหนึ่งวิธีขึ้นไป เพื่อให้ใช้วิธี **การลงรายการบัญชีระหว่างกาล** จากนั้นคุณต้องเลือกบัญชีระหว่างกาล

1. ไปที่ **บัญชีลูกหนี้ &gt; การตั้งค่าการชำระเงิน &gt; วิธีการชำระเงิน**
2. เลือกวิธีการชำระเงินที่มีอยู่เพื่อเปิดใช้งานการลงรายการบัญชีระหว่างกาล หรือสร้างวิธีการชำระเงินใหม่
3. เลือกกล่องกาเครื่องหมาย **การลงรายการบัญชีระหว่างกาล**
4. ในฟิลด์ **บัญชีระหว่างกาล** ให้เลือกบัญชีหลักที่ควรใช้ในการลงรายการบัญชีการชำระเงินก่อนที่จะโอนยอดเงินไปยังบัญชีธนาคาร
5. ปิดหน้า

## <a name="process-and-transfer-bridging-posting"></a>ดำเนินการและโอนย้ายการลงรายการบัญชีระหว่างกาล

ทำตามขั้นตอนเหล่านี้ เมื่อต้องการสร้างและดำเนินการกับการลงรายการบัญชีระหว่างกาล

1. ไปที่ **บัญชีเจ้าหนี้ &gt; การชำระเงิน &gt; สมุดรายวันการชำระเงินล่วงหน้าของลูกค้า**
2. เลือก **สร้าง** เพื่อสร้างสมุดรายวัน
3. ในฟิลด์ **ชื่อ** เลือกชื่อ
4. เพิ่มรายการลงในสมุดรายวันการชำระเงินของลูกค้า และเลือกวิธีการชำระเงินที่ตั้งค่าคอนฟิกไว้ให้กับการลงรายการบัญชีระหว่างกาล
5. ลงรายการบัญชีสมุดรายวัน ธุรกรรมจะมีการลงรายการบัญชีไปยังบัญชีหลักที่คุณเลือกไว้ในฟิลด์ **บัญชีระหว่างกาล** ในขั้นตอนก่อนหน้านี้

เมื่อธุรกรรมได้โอนยอดไปยังธนาคารแล้ว และคุณต้องการโอนย้ายการชำระเงินจากบัญชีระหว่างกาลไปยังบัญชีการชำระเงินที่ระบุไว้ของวิธีการชำระเงิน ให้ปฏิบัติตามขั้นตอนต่อไปนี้

1. ไปที่ **บัญชีแยกประเภททั่วไป &gt; รายการสมุดรายวัน &gt; สมุดรายวันทั่วไป**
2. เลือก **สร้าง** เพื่อสร้างสมุดรายวัน
3. ในฟิลด์ **ชื่อ** เลือกชื่อ
4. เลือก **รายการ** เพื่อเปิดรายละเอียดสมุดรายวัน
5. เลือก **ฟังก์ชัน &gt; เลือกธุรกรรมระหว่างกาล**
6. เลือกการชำระเงินแต่ละรายการที่โอนยอดแล้ว แล้วเลือก **ยอมรับ**
7. ลงรายการบัญชีสมุดรายวัน
