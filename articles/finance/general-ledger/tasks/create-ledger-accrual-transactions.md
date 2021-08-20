---
title: การสร้างธุรกรรมค้างรับค้างจ่ายในบัญชีแยกประเภท
description: คู่มืองานนี้ดำเนินงานโดยการสร้างธุรกรรมคงค้างในบัญชีแยกประเภท ที่ขึ้นอยู่กับแผนงานการค้างรับค้างจ่าย
author: aprilolson
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: LedgerJournalTable, LedgerJournalTransDaily, LedgerJournalTransAccrual, LedgerJournalTransAccrualTrans
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 6500da88424ea71aa8f8836dfdb7d42ef444637b50efe4401a6f76a876e3e0cf
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 08/05/2021
ms.locfileid: "6750399"
---
# <a name="create-ledger-accrual-transactions"></a>การสร้างธุรกรรมค้างรับค้างจ่ายในบัญชีแยกประเภท

[!include [banner](../../includes/banner.md)]

คำแนะนำงานนี้ระบุขั้นตอนสร้างธุรกรรมคงค้างในบัญชีแยกประเภทที่ขึ้นอยู่กับแผนงานการค้างรับค้างจ่าย

1. ไปที่บัญชีแยกประเภททั่วไป > รายการสมุดรายวัน > สมุดรายวันทั่วไป
2. ในรายการ ให้ค้นหาและเลือกการหักค่าเสื่อมราคาที่ต้องการและสร้างใหม่
3. คลิกเพื่อติดตามลิงค์ในฟิลด์หมายเลขชุดงานสมุดรายวัน 
4. ในรายการนี้ ให้ทำเครื่องหมายแถวที่เลือก
5. ในฟิลด์บัญชี ให้ระบุค่าที่ต้องการ
    * ในตัวอย่างนี้ เรากำลังกำหนดค่าใช้จ่ายสำหรับการประกันภัย  ซึ่งจะกลายเป็นยอดค่าใช้จ่ายประจำ  
6. ในฟิลด์ คำอธิบาย ให้พิมพ์ค่า
7. ในฟิลด์เดบิต ให้ป้อนตัวเลข
8. ในฟิลด์บัญชีตรงข้าม ให้ระบุค่าที่ต้องการ
9. คลิกฟังก์ชัน
10. คลิกการรับรู้บัญชีแยกประเภท
11. ในฟิลด์การระบุรายการค้างรับค้างจ่าย ให้คลิกปุ่มดรอปดาวน์เพื่อเปิดการค้นหา
12. ในรายการ ให้ค้นหาและเลือกแบบแผนการรับรู้ที่คุณต้องการนำไปใช้
13. ในรายการนี้ ให้คลิกลิงค์ในแถวที่เลือก
14. ในฟิลด์วันที่เริ่มต้น ให้ป้อนวันที่ 
15. คลิกธุรกรรม
16. ปิดหน้า
17. คลิก ตกลง
18. คลิก ลงรายการบัญชี



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]