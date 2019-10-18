---
title: การจับคู่ธุรกรรมระหว่างรหัสบัญชี
description: 'กระบวนงานนี้แสดงวิธีการชำระธุรกรรมระหว่างบัญชีแยกประเภท และการยกเลิกการชำระบัญชีแยกประเภท '
author: aprilolson
manager: AnnBe
ms.date: 10/03/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerTransSettlement, LedgerTrialBalanceListPage, LedgerTrialBalanceListPageBalanceParms, LedgerTransAccount, LedgerTransSettled
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 6ed76f82532d43a3c05b60b12176fe851e327956
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 09/27/2019
ms.locfileid: "2175649"
---
# <a name="settle-transactions-between-ledger-accounts"></a>การจับคู่ธุรกรรมระหว่างรหัสบัญชี

[!include [task guide banner](../../includes/task-guide-banner.md)]

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

