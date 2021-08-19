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
ms.openlocfilehash: 711e2f445e043dc74cba0ee11f1ab2dc22215ff30f495e06dce1f6f3ab4a0a09
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 08/05/2021
ms.locfileid: "6723810"
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