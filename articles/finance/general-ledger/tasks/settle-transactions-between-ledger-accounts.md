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
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 6813871a4773d39d4abfdecc896a2aa8b320cbe0
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 02/15/2021
ms.locfileid: "5222106"
---
# <a name="settle-transactions-between-ledger-accounts"></a><span data-ttu-id="cee50-103">การจับคู่ธุรกรรมระหว่างรหัสบัญชี</span><span class="sxs-lookup"><span data-stu-id="cee50-103">Settle transactions between ledger accounts</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="cee50-104">กระบวนงานนี้แสดงวิธีการชำระธุรกรรมระหว่างบัญชีแยกประเภท และการยกเลิกการชำระบัญชีแยกประเภท </span><span class="sxs-lookup"><span data-stu-id="cee50-104">This procedure shows how to settle transactions between ledger accounts and cancel a ledger settlement.</span></span> <span data-ttu-id="cee50-105">กระบวนงานนี้ใช้บริษัทข้อมูลสาธิต USMF</span><span class="sxs-lookup"><span data-stu-id="cee50-105">This procedure uses the USMF demo data company.</span></span>


## <a name="settle-transaction-between-ledger-accounts"></a><span data-ttu-id="cee50-106">ชำระธุรกรรมระหว่างบัญชีแยกประเภท</span><span class="sxs-lookup"><span data-stu-id="cee50-106">Settle transaction between ledger accounts</span></span>
1. <span data-ttu-id="cee50-107">ไปที่บัญชีแยกประเภททั่วไป > งานประจำงวด > การชำระบัญชีแยกประเภท</span><span class="sxs-lookup"><span data-stu-id="cee50-107">Go to General ledger > Periodic tasks > Ledger settlements.</span></span>
2. <span data-ttu-id="cee50-108">ในรายการ ให้หาธุรกรรมที่คุณต้องการชำระ</span><span class="sxs-lookup"><span data-stu-id="cee50-108">In the list, find the transaction that you want to settle.</span></span>
   > [!NOTE]
   > <span data-ttu-id="cee50-109">จำนวนยอดดุลต้องมากกว่าศูนย์</span><span class="sxs-lookup"><span data-stu-id="cee50-109">The amount balance must be zero.</span></span>  
3. <span data-ttu-id="cee50-110">คลิกรวม</span><span class="sxs-lookup"><span data-stu-id="cee50-110">Click Include.</span></span>
4. <span data-ttu-id="cee50-111">คลิกยอมรับ</span><span class="sxs-lookup"><span data-stu-id="cee50-111">Click Accept.</span></span>

## <a name="cancel-a-ledger-settlement"></a><span data-ttu-id="cee50-112">การยกเลิกการชำระตามบัญชีแยกประเภท</span><span class="sxs-lookup"><span data-stu-id="cee50-112">Cancel a ledger settlement</span></span>

1. <span data-ttu-id="cee50-113">ไปที่บัญชีแยกประเภททั่วไป > การสอบถามและการรายงาน > งบทดลอง</span><span class="sxs-lookup"><span data-stu-id="cee50-113">Go to General ledger > Inquiries and reports > Trial balance.</span></span>
2. <span data-ttu-id="cee50-114">คลิกพารามิเตอร์เพื่อเปิดกล่องโต้ตอบการวาง</span><span class="sxs-lookup"><span data-stu-id="cee50-114">Click Parameters to open the drop dialog.</span></span>
3. <span data-ttu-id="cee50-115">คลิก อัพเดต ข้อมูลเพิ่มเติมจะแสดงขึ้น</span><span class="sxs-lookup"><span data-stu-id="cee50-115">Click Update.</span></span>
4. <span data-ttu-id="cee50-116">ในรายการ ให้หาบัญชีที่ได้มีการชำระธุรกรรมแล้ว</span><span class="sxs-lookup"><span data-stu-id="cee50-116">In the list, find the account that has the settled transaction.</span></span>
5. <span data-ttu-id="cee50-117">คลิกธุรกรรมทั้งหมด</span><span class="sxs-lookup"><span data-stu-id="cee50-117">Click All transactions.</span></span>
6. <span data-ttu-id="cee50-118">ใช้ตัวกรองข้อมูลเพื่อค้นหาธุรกรรมในรายการได้อย่างง่ายดาย</span><span class="sxs-lookup"><span data-stu-id="cee50-118">Use a filter to easily find the transaction in the list.</span></span>
7. <span data-ttu-id="cee50-119">คลิกการชำระบัญชีแยกประเภท</span><span class="sxs-lookup"><span data-stu-id="cee50-119">Click Ledger settlements.</span></span>
8. <span data-ttu-id="cee50-120">ในรายการนี้ ให้ทำเครื่องหมายแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="cee50-120">In the list, mark the selected row.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]