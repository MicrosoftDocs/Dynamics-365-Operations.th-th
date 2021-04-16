---
title: การจับคู่ธุรกรรมระหว่างรหัสบัญชี
description: 'กระบวนงานนี้แสดงวิธีการชำระธุรกรรมระหว่างบัญชีแยกประเภท และการยกเลิกการชำระบัญชีแยกประเภท '
author: aprilolson
ms.date: 10/03/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: LedgerTransSettlement, LedgerTrialBalanceListPage, LedgerTrialBalanceListPageBalanceParms, LedgerTransAccount, LedgerTransSettled
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: b2594b90ed58a1e7f12c8a94d3c48266faef557f
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 04/01/2021
ms.locfileid: "5817064"
---
# <a name="settle-transactions-between-ledger-accounts"></a>การจับคู่ธุรกรรมระหว่างรหัสบัญชี

[!include [banner](../../includes/banner.md)]

กระบวนงานนี้แสดงวิธีการชำระธุรกรรมระหว่างบัญชีแยกประเภท และการยกเลิกการชำระบัญชีแยกประเภท  กระบวนงานนี้ใช้บริษัทข้อมูลสาธิต USMF


## <a name="settle-transaction-between-ledger-accounts"></a>ชำระธุรกรรมระหว่างบัญชีแยกประเภท
1. ไปที่บัญชีแยกประเภททั่วไป > งานประจำงวด > การชำระบัญชีแยกประเภท
2. ในรายการ ให้หาธุรกรรมที่คุณต้องการชำระ
   > [!NOTE]
   > จำนวนยอดดุลต้องมากกว่าศูนย์  
3. คลิกรวม
4. คลิกยอมรับ

## <a name="cancel-a-ledger-settlement"></a>การยกเลิกการชำระตามบัญชีแยกประเภท

1. ไปที่บัญชีแยกประเภททั่วไป > การสอบถามและการรายงาน > งบทดลอง
2. คลิกพารามิเตอร์เพื่อเปิดกล่องโต้ตอบการวาง
3. คลิก อัพเดต ข้อมูลเพิ่มเติมจะแสดงขึ้น
4. ในรายการ ให้หาบัญชีที่ได้มีการชำระธุรกรรมแล้ว
5. คลิกธุรกรรมทั้งหมด
6. ใช้ตัวกรองข้อมูลเพื่อค้นหาธุรกรรมในรายการได้อย่างง่ายดาย
7. คลิกการชำระบัญชีแยกประเภท
8. ในรายการนี้ ให้ทำเครื่องหมายแถวที่เลือก



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]