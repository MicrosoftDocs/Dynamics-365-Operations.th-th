--- 
title: "ตัดจำหน่ายสินทรัพย์ถาวรโดยใช้ใบแจ้งหนี้ข้อความอิสระ"
description: "กระบวนงานนี้แสดงวิธีการรับสินทรัพย์ถาวรโดยใช้ข้อเสนอการซื้อสินทรัพย์ในสมุดรายวันสินทรัพย์ถาวร"
author: saraschi2
manager: AnnBe
ms.date: 8/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: AssetTable, AssetBook, LedgerJournalTable, LedgerJournalTransAsset, SysQueryForm
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 24c7721a1e5467e98e6c4d245f1d8e24a973f5aa
ms.contentlocale: th-th
ms.lasthandoff: 09/29/2017

---
# <a name="dispose-of-a-fixed-asset-using-a-free-text-invoice"></a>ตัดจำหน่ายสินทรัพย์ถาวรโดยใช้ใบแจ้งหนี้ข้อความอิสระ

[!include [task guide banner](../../includes/task-guide-banner.md)]

กระบวนงานนี้แสดงวิธีการรับสินทรัพย์ถาวรโดยใช้ข้อเสนอการซื้อสินทรัพย์ในสมุดรายวันสินทรัพย์ถาวร ซึ่งจะใช้บทบาทของนักบัญชีและข้อมูลสาธิตสำหรับนิติบุคคล USMF

1. ไปที่สินทรัพย์ถาวร > รายการสมุดรายวัน > สมุดรายวันสินทรัพย์ถาวร
2. คลิก สร้าง
3. ในฟิลด์ชื่อ ให้ป้อนหรือเลือกค่าใดค่าหนึ่ง
4. คลิก รายการ
5. คลิกข้อเสนอ
6. คลิกที่ข้อเสนอการซื้อสินทรัพย์
7. คลิกตัวกรอง 
8. คลิกรีเซ็ตเพื่อล้างค่าก่อนหน้านี้
9. เลือกแถวจำนวนสินทรัพย์ถาวร
10. ในฟิลด์เงื่อนไข ให้ป้อนหรือเลือกค่าใดค่าหนึ่ง
    * กำหนดเงื่อนไขที่เหลือสำหรับสินทรัพย์ถาวรที่คุณต้องการได้รับกับข้อเสนอนี้  
11. คลิก ตกลง
12. คลิก ตกลง
    * ตรวจสอบการทำธุรกรรมที่สร้างขึ้น  
    * เฉพาะสินทรัพย์ถาวรที่มีวันที่ซื้อสินทรัพย์ และราคาทุนของสินทรัพย์ที่ตั้งค่าไว้ในสมุดบัญชีจะรวมอยู่ในข้อเสนอการซื้อสินทรัพย์  
13. คลิกแท็บสมุดบัญชี
14. คลิก ลงรายการบัญชี


