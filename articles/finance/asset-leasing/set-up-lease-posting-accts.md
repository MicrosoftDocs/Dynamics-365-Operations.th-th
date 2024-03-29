---
title: ตั้งค่าบัญชีการลงรายการบัญชีสัญญาเช่า
description: บทความนี้แสดงรายการบัญชีการลงรายการบัญชีที่จำเป็นสำหรับธุรกรรมการเช่าสินทรัพย์ และอธิบายวิธีการกำหนดบัญชีการลงรายการบัญชีในหน้าพารามิเตอร์การลงรายการบัญชีสัญญาเช่า
author: moaamer
ms.date: 04/12/2021
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
ms.openlocfilehash: 6e3a0d8dd3bb3e58ca10b2efce0cc88a2f48d2de
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 06/03/2022
ms.locfileid: "8859927"
---
# <a name="set-up-lease-posting-accounts"></a>ตั้งค่าบัญชีการลงรายการบัญชีสัญญาเช่า

[!include [banner](../includes/banner.md)]

บทความนี้แสดงรายการบัญชีการลงรายการบัญชีที่จำเป็นสำหรับธุรกรรมการเช่าสินทรัพย์ และอธิบายวิธีการกำหนดบัญชีการลงรายการบัญชีในหน้า **พารามิเตอร์การลงรายการบัญชีสัญญาเช่า**

เพื่อให้เป็นไปตามการเข้ารหัสมาตรฐานทางบัญชี หัวข้อ 842 (ASC 842) และ มาตรฐาน Financial Reporting ระหว่างประเทศ 16 (IFRS 16) คุณอาจต้องสร้างบัญชีในผังบัญชีของคุณ อย่างไรก็ตาม บัญชีใด ๆ ที่คุณสร้างเพื่อให้เป็นไปตามมาตรฐาน ASC และ IFRS ไม่ใช่บัญชีสินทรัพย์ถาวร ภายใต้ ASC 842 สิทธิ์การใช้สินทรัพย์ (ROU) ด้านขวาจะถูกบันทึกไว้สำหรับทั้งสัญญาเช่าดำเนินงานและการเงิน สัญญาเช่าเหล่านี้แยกต่างหากจากสินทรัพย์ถาวร (คุณยังคงสามารถรักษาสิทธิ์การใช้สินทรัพย์โดยใช้สินทรัพย์ถาวร)

สำหรับข้อมูลเกี่ยวกับวิธีการสร้างโครงสร้างทางบัญชี ให้ดูที่ [สร้างโครงสร้างทางบัญชี](../general-ledger/tasks/create-account-structures.md) สำหรับข้อมูลเกี่ยวกับวิธีการสร้างบัญชีหลัก ให้ดูที่ [สร้างบัญชีหลัก](../general-ledger/tasks/create-main-account.md)

ตารางต่อไปนี้แสดงตัวอย่างของบัญชีที่คุณต้องสร้างสำหรับธุรกรรมสินทรัพย์ที่ให้เช่า ถ้ายังไม่ได้สร้างใบแจ้งหนี้ ภายใต้ IFRS 16 ความสัมพันธ์ของสัญญาเช่าดำเนินงานยังคงใช้สำหรับสัญญาเช่ามูลค่าต่ำและระยะสั้น

| หมายเลขบัญชีแยกประเภท | ชนิดบัญชี  | ชื่อบัญชี                                          |
|-----------------------|---------------|-------------------------------------------------------|
| 180150                | แอสเซท         | สิทธิ์การใช้สินทรัพย์พาหนะ                                     |
| 180160                | แอสเซท         | สิทธิ์การใช้สินทรัพย์อาคาร                                    |
| 180250                | แอสเซท         | ค่าเสื่อมราคาสะสม - พาหนะ                   |
| 180260                | แอสเซท         | ค่าเสื่อมราคาสะสม - อาคาร                  |
| 222300                | หนี้สิน     | ข้อผูกมัดระยะสั้น - สัญญาเช่าการเงิน                |
| 222310                | งบดุล | ข้อผูกมัดระยะสั้น - สัญญาเช่าดำเนินงาน              |
| 250200                | หนี้สิน     | ตั๋วเงินจ่าย                                         |
| 250601                | งบดุล | ข้อผูกมัดระยะยาว - สัญญาเช่าการเงิน                 |
| 250602                | งบดุล | ข้อผูกมัดระยะยาว - สัญญาเช่าดำเนินงาน               |
| 250606                | งบดุล | ค่าเช่ารอตัดบัญชี                                         |
| 300160                | งบดุล | กำไรสะสม                                     |
| 604500                | Expense       | ค่าใช้จ่ายของสัญญาเช่า                                         |
| 604501                | Expense       | ค่าใช้จ่ายสัญญาเช่าดำเนินงานพาหนะ - การรวมดอกเบี้ย  |
| 604502                | Expense       | ค่าใช้จ่ายสัญญาเช่าดำเนินงานพาหนะ - การตัดบัญชี        |
| 605200                | Expense       | ค่าใช้จ่ายสัญญาเช่าดำเนินงานอาคาร - การรวมดอกเบี้ย |
| 605201                | Expense       | ค่าใช้จ่ายสัญญาเช่าดำเนินงานอาคาร - การตัดบัญชี       |
| 607101                | Expense       | ค่าใช้จ่ายการตัดบัญชีสัญญาเช่าพาหนะ                    |
| 607102                | Expense       | ค่าใช้จ่ายการตัดบัญชีสัญญาเช่าอาคาร                   |
| 607103                | Expense       | ค่าใช้จ่ายการด้อยค่าของสินทรัพย์ - สัญญาเช่าการเงิน                   |
| 607104                | Expense       | ค่าใช้จ่ายการด้อยค่าของสินทรัพย์ - สัญญาเช่าดำเนินงาน                 |
| 618910                | Expense       | ค่าใช้จ่ายสัญญาเช่า - สัญญาเช่าการเงิน                        |
| 618920                | Expense       | การชำระเงินแปรผัน - สัญญาเช่าการเงิน                    |
| 618930                | Expense       | การชำระเงินแปรผัน - สัญญาเช่าดำเนินงาน                  |
| 800600                | Expense       | ค่าใช้จ่ายดอกเบี้ยสัญญาเช่าพาหนะ                        |
| 800601                | Expense       | ค่าใช้จ่ายดอกเบี้ยสัญญาเช่าอาคาร                       |
| 801201                | งบดุล | กำไรและขาดทุน - การปรับเปลี่ยนสัญญาเช่า                      |

## <a name="configure-posting-accounts"></a>ตั้งค่าคอนฟิกการลงรายการบัญชี

เมื่อต้องการกำหนดบัญชีให้กับสมุดบัญชีเช่าและกลุ่มที่ได้สร้างขึ้นแล้ว คุณต้องตั้งค่าคอนฟิกพารามิเตอร์สำหรับการเช่าสินทรัพย์

1. ไปที่ **การเช่าสินทรัพย์ \> การตั้งค่า \> พารามิเตอร์การลงรายการบัญชีสัญญาเช่า**
2. บนแท็บ **บัญชี** ให้เปิดแท็บด่วน **บัญชีสัญญาเช่า** กำหนดบัญชีหลักสำหรับการให้เช่าการเงินและการดำเนินงานกับ **ชนิดการลงรายการบัญชี** ที่สอดคล้องกัน ตารางก่อนหน้านี้แสดงบัญชีที่เกี่ยวข้องกับสัญญาเช่าดำเนินงานและการเงิน

    > [!NOTE]
    > ขั้นตอนนี้กำหนดให้คุณตั้งค่าบัญชีแยกต่างหากสำหรับทั้งสัญญาเช่าทั้งการดำเนินงานและการเงินสำหรับแต่ละชนิดการลงรายการบัญชียกเว้น **บัญชีตรงข้ามค่าใช้จ่ายของสัญญาเช่า** และ **การเพิ่ม/ลดสัญญาเช่า** บริษัทที่เป็นไปตามกรอบงานการบัญชี IFRS 16 ต้องเพิ่มบัญชีหลักสำหรับสัญญาเช่าดำเนินงาน แต่ระบบจะไม่ใช้บัญชีนี้ถึงแม้ว่าจะเป็นฟิลด์ที่จำเป็นเนื่องจากสัญญาเช่าทั้งหมดภายใต้ IFRS 16 จะจัดประเภทเป็นสัญญาเช่าทางการเงิน
    >[!NOTE]
    > **การเพิ่ม/การลดสัญญาเช่า** จะใช้เป็นชนิดการลงรายการบัญชีสำหรับการพิจารณาสินทรัพย์เพิ่มเติม รวมถึง **ต้นทุนทางตรงเบื้องต้น สิ่งจูงใจในการทำสัญญาเช่า การชำระเงินสัญญาเช่าล่วงหน้าและต้นทุนการรื้อถอน** แต่การลงรายการบัญชีไปยังบัญชีหลักของสิทธิ์การใช้สินทรัพย์อยู่ด้านขวาซึ่งเป็นค่าเริ่มต้น **สินทรัพย์สัญญาเช่า**        
    
3. ถ้าต้องการเลือกกลุ่มสัญญาเช่าเฉพาะที่เกี่ยวข้องกับบัญชีหลัก ในฟิลด์ **รหัสบัญชี** ให้เลือก **กลุ่ม** ในฟิลด์ **หมายเลขบัญชี/กลุ่ม** ให้เลือกกลุ่มสัญญาเช่าที่จะกำหนดให้กับบัญชีหลัก
4. เมื่อต้องการกำหนดรหัสบัญชีให้กับต้นทุนของผู้ดูแลซึ่งตั้งค่าไว้ในระบบ บนแท็บด่วน **ค่าใช้จ่ายในการจัดการสินทรัพย์** ในฟิลด์ **ชนิดค่าใช้จ่าย** ให้เลือกค่าใช้จ่าย จากนั้นกำหนดบัญชีการเงินและการดำเนินงานที่จะใช้สำหรับสมุดบัญชีแต่ละเล่ม

    > [!NOTE]
    > บัญชีการเงินหรือบัญชีการดำเนินงานที่เลือกจะถูกเดบิตเมื่อมีการลงรายการบัญชีใบแจ้งหนี้สำหรับค่าใช้จ่ายที่จัดกำหนดการไว้
    > **บัญชีตรงข้ามค่าใช้จ่ายของสัญญาเช่า** จะใช้เป็นชนิดการลงรายการบัญชีสำหรับธุรกรรมค่าใช้จ่ายในการจัดการสินทรัพย์ แต่ลงรายการบัญชีไปที่ **บัญชีตรงข้าม** ที่กำหนดไว้ใน **รายการกำหนดการชำระเงินค่าใช้จ่ายในการจัดการสินทรัพย์** ในฟอร์มรายละเอียดสัญญาเช่าหรือฟอร์มสมุดบัญชีสัญญาเช่า   


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
