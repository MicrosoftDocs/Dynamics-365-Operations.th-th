---
title: การคํานวณ TDS ในใบแจ้งหนี้
description: บทความนี้มีการอ้างอิงสำหรับธุรกรรมซึ่งมีการคํานวณภาษีหักที่ต้นทาง (TDS) ที่ระดับใบแจ้งหนี้
author: kailiang
ms.date: 02/12/2021
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
ms.search.validFrom: 2021-02-12
ms.dyn365.ops.version: AX 10.0.17
ms.openlocfilehash: efc12e0839fe87e9db435f481ce1fd733c286d6c
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 06/03/2022
ms.locfileid: "8855376"
---
# <a name="tds-calculation-on-invoices"></a>การคํานวณ TDS ในใบแจ้งหนี้

[!include [banner](../includes/banner.md)]

บทความนี้มีการอ้างอิงสำหรับธุรกรรมซึ่งมีการคํานวณภาษีหักที่ต้นทาง (TDS) ที่ระดับใบแจ้งหนี้

| หมายเลขลำดับประจำสินค้า | ชนิดธุรกรรม                                 | ยอดเงินในธุรกรรม | ชื่อหน้าและพาธการเลือก                                 | ชนิดบัญชีและชนิดบัญชีตรงข้าม                         |
| ------------- | ------------------------------------------------ | ------------------ | ------------------------------------------------------------ | ------------------------------------------------------------ |
| 1            | การซื้อที่สร้างจากผู้จัดจำหน่าย / การบันทึกค่าใช้จ่าย   | เดบิตหรือเครดิต  | หน้าสมุดรายวันทั่วไป (บัญชีแยกประเภททั่วไป > รายการสมุดรายวัน > สมุดรายวันทั่วไป), หน้าสมุดรายวันการอนุมัติใบแจ้งหนี้ (บัญชีเจ้าหนี้ > ใบแจ้งหนี้ > การอนุมัติใบแจ้งหนี้), หน้าสมุดรายวันใบแจ้งหนี้ (บัญชีเจ้าหนี้ > ใบแจ้งหนี้ > สมุดรายวันใบแจ้งหนี้) | บัญชีแยกประเภท (Dr.) ผู้จัดจำหน่าย (Cr.)  มีการคํานวณภาษีหัก ณ ที่จ่ายสำหรับชุดผู้จัดจำหน่าย-บัญชีแยกประเภท เฉพาะเมื่อบัญชีแยกประเภทมีชนิดการลงรายการบัญชีเป็น **การซื้อ**  **เงินสด** เท่านั้น |
| 2            | การซื้อที่สร้างจากลูกค้า / การบันทึกค่าใช้จ่าย | เดบิตหรือเครดิต  | หน้าสมุดรายวันทั่วไป (บัญชีแยกประเภททั่วไป > รายการสมุดรายวัน > สมุดรายวันทั่วไป), หน้าสมุดรายวันใบแจ้งหนี้ (บัญชีเจ้าหนี้ > ใบแจ้งหนี้ > สมุดรายวันใบแจ้งหนี้) | บัญชีแยกประเภท (Dr.) ลูกค้า (Cr.)                                 |
| 3            | การซื้อสินทรัพย์ถาวรจากผู้จัดจำหน่าย              | เดบิตหรือเครดิต  | หน้าสมุดรายวันทั่วไป (บัญชีแยกประเภททั่วไป > รายการสมุดรายวัน > สมุดรายวันทั่วไป), หน้าสมุดรายวันทะเบียนใบแจ้งหนี้ (บัญชีเจ้าหนี้ > ใบแจ้งหนี้ > ทะเบียนใบแจ้งหนี้), หน้าสมุดรายวันใบแจ้งหนี้ (บัญชีเจ้าหนี้ > ใบแจ้งหนี้ > สมุดรายวันใบแจ้งหนี้) | สินทรัพย์ถาวร (Dr.) ผู้จัดจำหน่าย (Cr.)                             |
| 4            | การซื้อสินทรัพย์ถาวรจากลูกค้า            | เดบิตหรือเครดิต  | หน้าสมุดรายวันทั่วไป (บัญชีแยกประเภททั่วไป > รายการสมุดรายวัน > สมุดรายวันทั่วไป), หน้าสมุดรายวันใบแจ้งหนี้ (บัญชีเจ้าหนี้ > ใบแจ้งหนี้ > สมุดรายวันใบแจ้งหนี้) | สินทรัพย์ถาวร (Dr.) ลูกค้า (Cr.)                           |
| 5.            | ใบแจ้งหนี้การซื้อ (เจ้าหนี้ TDS)                  |                    | หน้าใบสั่งซื้อ (บัญชีเจ้าหนี้ > ใบสั่งซื้อ > ใบสั่งซื้อทั้งหมด) |                                                              |
| 6.            | ใบแจ้งหนี้การขาย (ลูกหนี้ TDS)                  |                    | หน้าใบสั่งขาย (บัญชีลูกหนี้ > ใบสั่ง > ใบสั่งขายทั้งหมด), หน้าใบแจ้งหนี้ข้อความอิสระ (บัญชีลูกหนี้ > ใบแจ้งหนี้ > ใบแจ้งหนี้ข้อความอิสระทั้งหมด) |                                                              |
