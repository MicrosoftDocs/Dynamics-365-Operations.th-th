---
title: จัดการการตรวจสอบบัญชีหมายเลขบัญชีธนาคารระหว่างประเทศ (IBAN)
description: บทความนี้อธิบายวิธีการจัดการการตรวจสอบบัญชีหมายเลขบัญชีธนาคารระหว่างประเทศ (IBAN)
author: angelad116
ms.date: 08/24/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: twheeloc
ms.search.region: Global
ms.author: angelading
ms.search.validFrom: 2018-08-30
ms.dyn365.ops.version: 8.0.4
ms.openlocfilehash: 0e64c763cb74362503a3d6dfa184b26df77f30b3
ms.sourcegitcommit: 0b7a034e644f4d93fe55c7baca5a3f89dbe56898
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 07/14/2022
ms.locfileid: "9151804"
---
# <a name="manage-international-bank-account-number-iban-account-validation"></a>จัดการการตรวจสอบบัญชีหมายเลขบัญชีธนาคารระหว่างประเทศ (IBAN)

[!include [banner](../includes/banner.md)]

การตรวจสอบ International Bank Account Number (IBAN) เพิ่มจำนวนการตรวจสอบที่เสร็จสิ้นแล้ว เมื่อคุณเพิ่ม IBAN ไปยังบัญชีธนาคาร

ข้อมูลเกี่ยวกับโครงสร้างของ IBAN จะจัดเก็บอยู่ใน Microsoft Dynamics 365 Finance และโหลดโดยอัตโนมัติเมื่อคุณใช้ IBAN กับบัญชีธนาคารในครั้งแรก ประกอบด้วยความยาวของ IBAN ตำแหน่งเริ่มต้นของหมายเลขบัญชีธนาคาร และหมายเลขเส้นทาง และความยาวของหมายเลขบัญชีธนาคารและหมายเลขเส้นทาง

## <a name="set-up-iban-structures"></a>ตั้งค่าโครงสร้าง IBAN

1. ไปที่ **การจัดการเงินสดและธนาคาร \> การตั้งค่า \> โครงสร้าง IBAN**
2. โปรดสังเกตว่า โครงสร้าง IBAN สำหรับแต่ละประเทศหรือภูมิภาคถูกตั้งค่าไว้โดยอัตโนมัติ
3. เลือกปุ่ม **แก้ไข** ถ้าต้องอัปเดตโครงสร้างเฉพาะประเทศหรือภูมิภาคที่ระบุ
4. คำนิยามโครงสร้างจะเป็นส่วนหนึ่งของรุ่นใหม่แต่ละรุ่น คุณสามารถใช้เมนู **รีเซ็ตโครงสร้าง** เพื่อโหลดนิยามล่าสุด หลังการปรับปรุงแต่ละครั้ง

## <a name="validate-the-iban-structure-in-a-bank-account"></a>ตรวจสอบความถูกต้องของโครงสร้างทางบัญชี IBAN ในบัญชีธนาคาร

1. ไปที่ **การจัดการเงินสดและธนาคาร \> บัญชีธนาคาร \> บัญชีธนาคาร**
2. สร้างบัญชีธนาคาร
3. บน FastTab **ข้อมูลเพิ่มเติม** ป้อน IBAN

    ถ้าความยาวของ IBAN ไม่ตรงกับความยาวที่กำหนดไว้สำหรับแต่ละประเทศหรือภูมิภาค คุณจะได้รับข้อความแจ้งเตือน คุณไม่สามารถทำต่อไปได้ ถ้าความยาวของ IBAN ไม่ตรงกับความยาวที่ระบุในโครงสร้างของ IBAN

    การตรวจสอบจะยังสามารถตรวจสอบว่า หมายเลขบัญชีธนาคารให้ตรงกับส่วนของ IBAN ที่แสดงถึงหมายเลขบัญชีธนาคาร ถ้าหมายเลขบัญชีธนาคารไม่ตรงกัน คุณจะได้รับข้อความแจ้งเตือน ข้อความนี้เป็นเพียงคำเตือนเท่านั้น คุณสามารถดำเนินต่อไปได้ แม้ว่าหมายเลขบัญชีธนาคารจะไม่ตรงกัน

    การตรวจสอบจะยังตรวจสอบว่า หมายเลขการกำหนดเส้นทางธนาคารตรงกับส่วนของ IBAN ที่แสดงถึงหมายเลขการกำหนดเส้นทางธนาคารอีกด้วย หมายเลขการกำหนดเส้นทางรวมหมายเลขธนาคาร และมักจะมีสาขาธนาคารเพิ่มเติม ถ้าหมายเลขการกำหนดเส้นทางธนาคารไม่ตรงกัน คุณจะได้รับข้อความแจ้งเตือน ข้อความนี้เป็นเพียงคำเตือนเท่านั้น คุณสามารถดำเนินต่อไปได้ แม้ว่าหมายเลขการกำหนดเส้นทางธนาคารจะไม่ตรงกัน


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
