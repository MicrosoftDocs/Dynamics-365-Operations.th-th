---
title: ข้อมูลจำเพาะเกี่ยวกับภาษีขายโดยเรียงตามรายงานธุรกรรมบัญชีแยกประเภท
description: บทความนี้จะอธิบายวิธีการใช้ข้อมูลจำเพาะเกี่ยวกับภาษีขายโดยเรียงตามธุรกรรมบัญชีแยกประเภทเพื่อดูและพิมพ์ข้อมูลเกี่ยวกับธุรกรรมบัญชีแยกประเภทที่มีการคำนวณภาษีขาย
author: EricWang
ms.date: 08/19/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: TaxTable
audience: Application User
ms.reviewer: kfend
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: wangchen
ms.search.validFrom: 2019-08-19
ms.dyn365.ops.version: 10.0.6
ms.openlocfilehash: c96f457a0ea24aef1769f370c3c0657ada31eebf
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 06/03/2022
ms.locfileid: "8898104"
---
# <a name="sales-tax-specification-by-ledger-transaction-report"></a>ข้อมูลจำเพาะเกี่ยวกับภาษีขายโดยเรียงตามรายงานธุรกรรมบัญชีแยกประเภท
[!include [banner](../includes/banner.md)]

บทความนี้จะอธิบายวิธีการใช้ข้อมูลรายงานจำเพาะเกี่ยวกับ **ภาษีขายโดยเรียงตามธุรกรรมบัญชีแยกประเภท** เพื่อดูและพิมพ์ข้อมูลเกี่ยวกับธุรกรรมบัญชีแยกประเภทที่มีการคำนวณภาษีขาย

## <a name="tax-accounts-vs-non-tax-accounts"></a>บัญชีภาษี เปรียบเทียบกับ บัญชีที่ไม่ใช่ภาษี

รายงาน **ข้อมูลจำเพาะภาษีขายของธุรกรรมบัญชีแยกประเภท** จะแสดงธุรกรรมภาษีสำหรับทั้งบัญชีภาษีและบัญชีที่ไม่ใช่ภาษี บัญชีเหล่านี้ถูกจัดประเภทในลักษณะต่อไปนี้:

- **บัญชีภาษี** – บัญชีจะถือว่าเป็นบัญชีภาษีก็ต่อเมื่อมีการลงรายการบัญชีธุรกรรมภาษี และบัญชีหลักในรายการสมุดประจำวันของ **ภาษีขาย** เป็นบัญชีภาษี เช่น บัญชีเจ้าหนี้ภาษีขาย หรือบัญชีลูกหนี้ภาษีขาย
- **บัญชีที่ไม่ใช่ภาษี** – บัญชีจะถือว่าเป็นบัญชีที่ไม่ใช่ภาษีก็ต่อเมือมีการลงรายการธุรกรรมภาษี และบัญชีหลักของธุรกรรมเดิมเป็นบัญชีที่ไม่ใช่ภาษี เช่น บัญชีรายได้ หรือ บัญชีรายจ่าย

สำหรับบัญชีภาษี คอลัมน์ **จุดเริ่มต้น**, **ลูกหนี้ภาษีขาย** และ **เจ้าหนี้ภาษีขาย** แสดงค่าเป็น **0** (ศูนย์). สำหรับบัญชีที่ไม่ใช่ภาษี คอลัมน์เหล่านั้นจะแสดงยอดปกติ

## <a name="filtering-the-data-on-the-report"></a>การกรองข้อมูลที่อยู่ในรายงาน

เมื่อคุณสร้างรายงานนี้ ฟิลด์เริ่มต้นต่อไปนี้จะพร้อมใช้งาน คุณสามารถใช้ฟิลด์เหล่านี้เพื่อกรองข้อมูลที่จะแสดงในรายงาน

| ฟิลด์                      | คำอธิบาย |
|----------------------------|-------------|
| วัน เดือน                       | ใช้ฟิลด์ในส่วนของ **จาก** และ **ถึง** เพื่อกำหนดช่วงวันที่สำหรับธุรกรรมภาษี |
| บัญชีหลัก               | ใช้ฟิลด์ในส่วนของ **จาก** และ **ถึง** เพื่อกำหนดช่วงของบัญชีหลัก |
| รหัสภาษีขาย             | ใช้ฟิลด์ในส่วนของ **จาก** และ **ถึง** เพื่อกำหนดช่วงของรหัสภาษีขาย |
| การจัดกลุ่ม                   | เลือกว่าจะให้จัดกลุ่มรายงานตามบัญชีแยกประเภท หรือตามรหัสภาษีขาย |
| ผลรวมย่อยตามรหัสภาษีขาย | กำหนดตัวเลือกนี้เป็น **ใช่** เพื่อแสดงผลรวมย่อยตามรหัสภาษีขาย |
| เฉพาะผลรวม                | กำหนดตัวเลือกนี้เป็น **ใช่** เพื่อแสดงเฉพาะผลรวม |
| บัญชีหลักเท่านั้น         | กำหนดตัวเลือกนี้เป็น **ใช่** เพื่อรวมเฉพาะบัญชีหลักบนรายงาน |

## <a name="showing-only-non-tax-accounts-on-the-report"></a>แสดงเฉพาะบัญชีที่ไม่ใช่ภาษีในรายงาน

เมื่อต้องการแสดงเฉพาะบัญชีที่ไม่ใช่ภาษีในรายงาน ให้ตั้งค่าเงื่อนไขตัวกรองข้อมูล เช่น เครื่องหมายดอกจัน (\*) ดังที่แสดงในภาพประกอบต่อไปนี้

![รายงานที่แสดงบัญชีที่ไม่ใช่ภาษี](media/taxspecperledgertrans.png)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
