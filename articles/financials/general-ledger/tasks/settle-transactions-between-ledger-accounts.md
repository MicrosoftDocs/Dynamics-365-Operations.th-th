--- 
title: "การจับคู่ธุรกรรมระหว่างรหัสบัญชี"
description: "กระบวนงานนี้แสดงวิธีการชำระธุรกรรมระหว่างบัญชีแยกประเภท และการยกเลิกการชำระบัญชีแยกประเภท "
author: aprilolson
manager: AnnBe
ms.date: 8/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: LedgerTransSettlement, LedgerTrialBalanceListPage, LedgerTrialBalanceListPageBalanceParms, LedgerTransAccount, LedgerTransSettled
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 32d71167fdad65cb1dec37671999a497759ca484
ms.openlocfilehash: 479da79142baf8d60eabf1f6c7db5687b4595234
ms.contentlocale: th-th
ms.lasthandoff: 09/11/2018

---
# <a name="settle-transactions-between-ledger-accounts"></a><span data-ttu-id="9b412-103">การจับคู่ธุรกรรมระหว่างรหัสบัญชี</span><span class="sxs-lookup"><span data-stu-id="9b412-103">Settle transactions between ledger accounts</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="9b412-104">กระบวนงานนี้แสดงวิธีการชำระธุรกรรมระหว่างบัญชีแยกประเภท และการยกเลิกการชำระบัญชีแยกประเภท </span><span class="sxs-lookup"><span data-stu-id="9b412-104">This procedure shows how to settle transactions between ledger accounts and cancel a ledger settlement.</span></span> <span data-ttu-id="9b412-105">กระบวนงานนี้ใช้บริษัทข้อมูลสาธิต USMF</span><span class="sxs-lookup"><span data-stu-id="9b412-105">This procedure uses the USMF demo data company.</span></span>


## <a name="settle-transaction-between-ledger-accounts"></a><span data-ttu-id="9b412-106">ชำระธุรกรรมระหว่างบัญชีแยกประเภท</span><span class="sxs-lookup"><span data-stu-id="9b412-106">Settle transaction between ledger accounts</span></span>
1. <span data-ttu-id="9b412-107">ไปที่บัญชีแยกประเภททั่วไป > งานประจำงวด > การชำระบัญชีแยกประเภท</span><span class="sxs-lookup"><span data-stu-id="9b412-107">Go to General ledger > Periodic tasks > Ledger settlements.</span></span>
2. <span data-ttu-id="9b412-108">ในรายการ ให้หาธุรกรรมที่คุณต้องการชำระ</span><span class="sxs-lookup"><span data-stu-id="9b412-108">In the list, find the transaction that you want to settle.</span></span>
    * <span data-ttu-id="9b412-109">จำนวนยอดดุลต้องมากกว่าศูนย์</span><span class="sxs-lookup"><span data-stu-id="9b412-109">The amount balance must be zero.</span></span>  
3. <span data-ttu-id="9b412-110">คลิกรวม</span><span class="sxs-lookup"><span data-stu-id="9b412-110">Click Include.</span></span>
4. <span data-ttu-id="9b412-111">คลิกยอมรับ</span><span class="sxs-lookup"><span data-stu-id="9b412-111">Click Accept.</span></span>

## <a name="cancel-a-ledger-settlement"></a><span data-ttu-id="9b412-112">การยกเลิกการชำระตามบัญชีแยกประเภท</span><span class="sxs-lookup"><span data-stu-id="9b412-112">Cancel a ledger settlement</span></span>
1. <span data-ttu-id="9b412-113">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="9b412-113">Close the page.</span></span>
2. <span data-ttu-id="9b412-114">ไปที่บัญชีแยกประเภททั่วไป > การสอบถามและการรายงาน > งบทดลอง</span><span class="sxs-lookup"><span data-stu-id="9b412-114">Go to General ledger > Inquiries and reports > Trial balance.</span></span>
3. <span data-ttu-id="9b412-115">คลิกพารามิเตอร์เพื่อเปิดกล่องโต้ตอบการวาง</span><span class="sxs-lookup"><span data-stu-id="9b412-115">Click Parameters to open the drop dialog.</span></span>
4. <span data-ttu-id="9b412-116">คลิก อัพเดต ข้อมูลเพิ่มเติมจะแสดงขึ้น</span><span class="sxs-lookup"><span data-stu-id="9b412-116">Click Update.</span></span>
5. <span data-ttu-id="9b412-117">ในรายการ ให้หาบัญชีที่ได้มีการชำระธุรกรรมแล้ว</span><span class="sxs-lookup"><span data-stu-id="9b412-117">In the list, find the account that has the settled transaction.</span></span>
6. <span data-ttu-id="9b412-118">คลิกธุรกรรมทั้งหมด</span><span class="sxs-lookup"><span data-stu-id="9b412-118">Click All transactions.</span></span>
7. <span data-ttu-id="9b412-119">ใช้ตัวกรองข้อมูลเพื่อค้นหาธุรกรรมในรายการได้อย่างง่ายดาย</span><span class="sxs-lookup"><span data-stu-id="9b412-119">Use a filter to easily find the transaction in the list.</span></span>
8. <span data-ttu-id="9b412-120">คลิกการชำระบัญชีแยกประเภท</span><span class="sxs-lookup"><span data-stu-id="9b412-120">Click Ledger settlements.</span></span>
9. <span data-ttu-id="9b412-121">ในรายการนี้ ให้ทำเครื่องหมายแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="9b412-121">In the list, mark the selected row.</span></span>


