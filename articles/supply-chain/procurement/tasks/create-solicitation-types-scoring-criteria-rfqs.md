---
title: สร้างชนิดการร้องขอ และเกณฑ์การให้คะแนนสำหรับ RFQ
description: 'คำแนะนำนี้แสดงวิธีการสร้างชนิดการร้องขอ และการเชื่อมโยงกับวิธีการให้คะแนน '
author: RichardLuan
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: PurchRFQSolicitationType, PurchRFQCaseTableListPage, PurchCreateRFQCase, PurchRFQCaseTable, PurchRFQScoringRFQCaseCriteria, PurchRFQScoringCriteriaCopy
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: riluan
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 40625152a579bb269411d026d77d449902c8d4bc
ms.sourcegitcommit: deac22ba5377a912d93fe408c5ae875706378c2d
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 01/16/2021
ms.locfileid: "5016817"
---
# <a name="create-solicitation-types-and-scoring-criteria-for-rfqs"></a>สร้างชนิดการร้องขอ และเกณฑ์การให้คะแนนสำหรับ RFQ

[!include [banner](../../includes/banner.md)]

คำแนะนำนี้แสดงวิธีการสร้างชนิดการร้องขอ และการเชื่อมโยงกับวิธีการให้คะแนน  นอกจากนี้ยังแสดงวิธีการใช้ชนิดการร้องขอในคำขอใบเสนอราคา (RFQ) ซึ่งจะกำหนดวิธีการให้คะแนนเริ่มต้น โดยทั่วไปงานเหล่านี้จะดำเนินการโดยผู้จัดการฝ่ายจัดซื้อ คุณสามารถใช้กระบวนงานนี้ในบริษัทข้อมูลสาธิต USMF หรือข้อมูลของคุณเองได้ คุณต้องมีวิธีการให้คะแนนที่พร้อมใช้ก่อนที่จะเริ่มต้น


## <a name="create-a-solicitation-type"></a>สร้างชนิดการร้องขอ
1. ไปที่การจัดซื้อและการจัดหา > การตั้งค่า > คำขอใบเสนอราคา > ชนิดการร้องขอ
2. คลิก สร้าง
3. ในฟิลด์ชื่อ ให้พิมพ์ค่า 
4. ในฟิลด์ คำอธิบาย ให้พิมพ์ค่า
5. ในฟิลด์วิธีการให้คะแนน เลือกวิธีการให้คะแนนที่คุณต้องการใช้สำหรับชนิดการร้องขอนี้
6. คลิก บันทึก
7. ปิดหน้า

## <a name="use-the-solicitation-type"></a>ใช้ชนิดของการร้องขอ
1. ไปที่การจัดซื้อและการจัดหา > คำขอใบเสนอราคา > คำขอใบเสนอราคาทั้งหมด
2. คลิก สร้าง
3. ในฟิลด์ชนิดการร้องขอ เลือกชนิดการร้องขอที่คุณเพิ่งสร้างขึ้น 
    *   
4. คลิก ตกลง
5. คลิกเกณฑ์การให้คะแนน
    * เกณฑ์การให้คะแนนที่แสดงมาจากวิธีการให้คะแนนที่คุณเชื่อมโยงกับชนิดการร้องขอ  คุณสามารถเลือกที่จะเพิ่ม หรือลบเงื่อนไขบนหน้านี้ และยังสามารถเพิ่มเงื่อนไขใหม่ได้โดยการคัดลอกออกจากวิธีการให้คะแนนอื่น ๆ  
6. คลิกคัดลอกเกณฑ์
7. ในฟิลด์วิธีการให้คะแนน ให้ป้อนหรือเลือกค่าใดค่าหนึ่ง
8. คลิก ตกลง
9. ปิดหน้า

