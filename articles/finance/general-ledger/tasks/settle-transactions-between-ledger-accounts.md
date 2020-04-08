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
ms.openlocfilehash: bb53e9fee35712343f034389f00f3d4539cc652d
ms.sourcegitcommit: 57e1dafa186fec77ddd8ba9425d238e36e0f0998
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 03/18/2020
ms.locfileid: "3144685"
---
# <a name="settle-transactions-between-ledger-accounts"></a><span data-ttu-id="dbda8-103">การจับคู่ธุรกรรมระหว่างรหัสบัญชี</span><span class="sxs-lookup"><span data-stu-id="dbda8-103">Settle transactions between ledger accounts</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="dbda8-104">กระบวนงานนี้แสดงวิธีการชำระธุรกรรมระหว่างบัญชีแยกประเภท และการยกเลิกการชำระบัญชีแยกประเภท </span><span class="sxs-lookup"><span data-stu-id="dbda8-104">This procedure shows how to settle transactions between ledger accounts and cancel a ledger settlement.</span></span> <span data-ttu-id="dbda8-105">กระบวนงานนี้ใช้บริษัทข้อมูลสาธิต USMF</span><span class="sxs-lookup"><span data-stu-id="dbda8-105">This procedure uses the USMF demo data company.</span></span>


## <a name="settle-transaction-between-ledger-accounts"></a><span data-ttu-id="dbda8-106">ชำระธุรกรรมระหว่างบัญชีแยกประเภท</span><span class="sxs-lookup"><span data-stu-id="dbda8-106">Settle transaction between ledger accounts</span></span>
1. <span data-ttu-id="dbda8-107">ไปที่บัญชีแยกประเภททั่วไป > งานประจำงวด > การชำระบัญชีแยกประเภท</span><span class="sxs-lookup"><span data-stu-id="dbda8-107">Go to General ledger > Periodic tasks > Ledger settlements.</span></span>
2. <span data-ttu-id="dbda8-108">ในรายการ ให้หาธุรกรรมที่คุณต้องการชำระ</span><span class="sxs-lookup"><span data-stu-id="dbda8-108">In the list, find the transaction that you want to settle.</span></span>
   > [!NOTE]
   > <span data-ttu-id="dbda8-109">จำนวนยอดดุลต้องมากกว่าศูนย์</span><span class="sxs-lookup"><span data-stu-id="dbda8-109">The amount balance must be zero.</span></span>  
3. <span data-ttu-id="dbda8-110">คลิกรวม</span><span class="sxs-lookup"><span data-stu-id="dbda8-110">Click Include.</span></span>
4. <span data-ttu-id="dbda8-111">คลิกยอมรับ</span><span class="sxs-lookup"><span data-stu-id="dbda8-111">Click Accept.</span></span>

## <a name="cancel-a-ledger-settlement"></a><span data-ttu-id="dbda8-112">การยกเลิกการชำระตามบัญชีแยกประเภท</span><span class="sxs-lookup"><span data-stu-id="dbda8-112">Cancel a ledger settlement</span></span>

1. <span data-ttu-id="dbda8-113">ไปที่บัญชีแยกประเภททั่วไป > การสอบถามและการรายงาน > งบทดลอง</span><span class="sxs-lookup"><span data-stu-id="dbda8-113">Go to General ledger > Inquiries and reports > Trial balance.</span></span>
2. <span data-ttu-id="dbda8-114">คลิกพารามิเตอร์เพื่อเปิดกล่องโต้ตอบการวาง</span><span class="sxs-lookup"><span data-stu-id="dbda8-114">Click Parameters to open the drop dialog.</span></span>
3. <span data-ttu-id="dbda8-115">คลิก อัพเดต ข้อมูลเพิ่มเติมจะแสดงขึ้น</span><span class="sxs-lookup"><span data-stu-id="dbda8-115">Click Update.</span></span>
4. <span data-ttu-id="dbda8-116">ในรายการ ให้หาบัญชีที่ได้มีการชำระธุรกรรมแล้ว</span><span class="sxs-lookup"><span data-stu-id="dbda8-116">In the list, find the account that has the settled transaction.</span></span>
5. <span data-ttu-id="dbda8-117">คลิกธุรกรรมทั้งหมด</span><span class="sxs-lookup"><span data-stu-id="dbda8-117">Click All transactions.</span></span>
6. <span data-ttu-id="dbda8-118">ใช้ตัวกรองข้อมูลเพื่อค้นหาธุรกรรมในรายการได้อย่างง่ายดาย</span><span class="sxs-lookup"><span data-stu-id="dbda8-118">Use a filter to easily find the transaction in the list.</span></span>
7. <span data-ttu-id="dbda8-119">คลิกการชำระบัญชีแยกประเภท</span><span class="sxs-lookup"><span data-stu-id="dbda8-119">Click Ledger settlements.</span></span>
8. <span data-ttu-id="dbda8-120">ในรายการนี้ ให้ทำเครื่องหมายแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="dbda8-120">In the list, mark the selected row.</span></span>

