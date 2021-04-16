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
# <a name="settle-transactions-between-ledger-accounts"></a><span data-ttu-id="7354b-103">การจับคู่ธุรกรรมระหว่างรหัสบัญชี</span><span class="sxs-lookup"><span data-stu-id="7354b-103">Settle transactions between ledger accounts</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="7354b-104">กระบวนงานนี้แสดงวิธีการชำระธุรกรรมระหว่างบัญชีแยกประเภท และการยกเลิกการชำระบัญชีแยกประเภท </span><span class="sxs-lookup"><span data-stu-id="7354b-104">This procedure shows how to settle transactions between ledger accounts and cancel a ledger settlement.</span></span> <span data-ttu-id="7354b-105">กระบวนงานนี้ใช้บริษัทข้อมูลสาธิต USMF</span><span class="sxs-lookup"><span data-stu-id="7354b-105">This procedure uses the USMF demo data company.</span></span>


## <a name="settle-transaction-between-ledger-accounts"></a><span data-ttu-id="7354b-106">ชำระธุรกรรมระหว่างบัญชีแยกประเภท</span><span class="sxs-lookup"><span data-stu-id="7354b-106">Settle transaction between ledger accounts</span></span>
1. <span data-ttu-id="7354b-107">ไปที่บัญชีแยกประเภททั่วไป > งานประจำงวด > การชำระบัญชีแยกประเภท</span><span class="sxs-lookup"><span data-stu-id="7354b-107">Go to General ledger > Periodic tasks > Ledger settlements.</span></span>
2. <span data-ttu-id="7354b-108">ในรายการ ให้หาธุรกรรมที่คุณต้องการชำระ</span><span class="sxs-lookup"><span data-stu-id="7354b-108">In the list, find the transaction that you want to settle.</span></span>
   > [!NOTE]
   > <span data-ttu-id="7354b-109">จำนวนยอดดุลต้องมากกว่าศูนย์</span><span class="sxs-lookup"><span data-stu-id="7354b-109">The amount balance must be zero.</span></span>  
3. <span data-ttu-id="7354b-110">คลิกรวม</span><span class="sxs-lookup"><span data-stu-id="7354b-110">Click Include.</span></span>
4. <span data-ttu-id="7354b-111">คลิกยอมรับ</span><span class="sxs-lookup"><span data-stu-id="7354b-111">Click Accept.</span></span>

## <a name="cancel-a-ledger-settlement"></a><span data-ttu-id="7354b-112">การยกเลิกการชำระตามบัญชีแยกประเภท</span><span class="sxs-lookup"><span data-stu-id="7354b-112">Cancel a ledger settlement</span></span>

1. <span data-ttu-id="7354b-113">ไปที่บัญชีแยกประเภททั่วไป > การสอบถามและการรายงาน > งบทดลอง</span><span class="sxs-lookup"><span data-stu-id="7354b-113">Go to General ledger > Inquiries and reports > Trial balance.</span></span>
2. <span data-ttu-id="7354b-114">คลิกพารามิเตอร์เพื่อเปิดกล่องโต้ตอบการวาง</span><span class="sxs-lookup"><span data-stu-id="7354b-114">Click Parameters to open the drop dialog.</span></span>
3. <span data-ttu-id="7354b-115">คลิก อัพเดต ข้อมูลเพิ่มเติมจะแสดงขึ้น</span><span class="sxs-lookup"><span data-stu-id="7354b-115">Click Update.</span></span>
4. <span data-ttu-id="7354b-116">ในรายการ ให้หาบัญชีที่ได้มีการชำระธุรกรรมแล้ว</span><span class="sxs-lookup"><span data-stu-id="7354b-116">In the list, find the account that has the settled transaction.</span></span>
5. <span data-ttu-id="7354b-117">คลิกธุรกรรมทั้งหมด</span><span class="sxs-lookup"><span data-stu-id="7354b-117">Click All transactions.</span></span>
6. <span data-ttu-id="7354b-118">ใช้ตัวกรองข้อมูลเพื่อค้นหาธุรกรรมในรายการได้อย่างง่ายดาย</span><span class="sxs-lookup"><span data-stu-id="7354b-118">Use a filter to easily find the transaction in the list.</span></span>
7. <span data-ttu-id="7354b-119">คลิกการชำระบัญชีแยกประเภท</span><span class="sxs-lookup"><span data-stu-id="7354b-119">Click Ledger settlements.</span></span>
8. <span data-ttu-id="7354b-120">ในรายการนี้ ให้ทำเครื่องหมายแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="7354b-120">In the list, mark the selected row.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]