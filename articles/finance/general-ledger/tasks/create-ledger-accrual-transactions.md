---
title: การสร้างธุรกรรมค้างรับค้างจ่ายในบัญชีแยกประเภท
description: คู่มืองานนี้ดำเนินงานโดยการสร้างธุรกรรมคงค้างในบัญชีแยกประเภท ที่ขึ้นอยู่กับแผนงานการค้างรับค้างจ่าย
author: aprilolson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerJournalTable, LedgerJournalTransDaily, LedgerJournalTransAccrual, LedgerJournalTransAccrualTrans
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: c1722c72ebc5ea7c0f8704ba3761f971f5075744
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 02/15/2021
ms.locfileid: "5216460"
---
# <a name="create-ledger-accrual-transactions"></a><span data-ttu-id="374e2-103">การสร้างธุรกรรมค้างรับค้างจ่ายในบัญชีแยกประเภท</span><span class="sxs-lookup"><span data-stu-id="374e2-103">Create ledger accrual transactions</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="374e2-104">คำแนะนำงานนี้ระบุขั้นตอนสร้างธุรกรรมคงค้างในบัญชีแยกประเภทที่ขึ้นอยู่กับแผนงานการค้างรับค้างจ่าย</span><span class="sxs-lookup"><span data-stu-id="374e2-104">This task guide steps through generating ledger accrual transactions that are based on accrual schemes</span></span>

1. <span data-ttu-id="374e2-105">ไปที่บัญชีแยกประเภททั่วไป > รายการสมุดรายวัน > สมุดรายวันทั่วไป</span><span class="sxs-lookup"><span data-stu-id="374e2-105">Go to General ledger > Journal entries > General journals.</span></span>
2. <span data-ttu-id="374e2-106">ในรายการ ให้ค้นหาและเลือกการหักค่าเสื่อมราคาที่ต้องการและสร้างใหม่</span><span class="sxs-lookup"><span data-stu-id="374e2-106">In the list, find and select the desired journal or create a new one.</span></span>
3. <span data-ttu-id="374e2-107">คลิกเพื่อติดตามลิงค์ในฟิลด์หมายเลขชุดงานสมุดรายวัน </span><span class="sxs-lookup"><span data-stu-id="374e2-107">Click to follow the link in the Journal batch number field.</span></span>
4. <span data-ttu-id="374e2-108">ในรายการนี้ ให้ทำเครื่องหมายแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="374e2-108">In the list, mark the selected row.</span></span>
5. <span data-ttu-id="374e2-109">ในฟิลด์บัญชี ให้ระบุค่าที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="374e2-109">In the Account field, specify the desired values.</span></span>
    * <span data-ttu-id="374e2-110">ในตัวอย่างนี้ เรากำลังกำหนดค่าใช้จ่ายสำหรับการประกันภัย </span><span class="sxs-lookup"><span data-stu-id="374e2-110">In this example, we are defining the expense for the insurance.</span></span> <span data-ttu-id="374e2-111">ซึ่งจะกลายเป็นยอดค่าใช้จ่ายประจำ</span><span class="sxs-lookup"><span data-stu-id="374e2-111">It will be come periodic expense amount.</span></span>  
6. <span data-ttu-id="374e2-112">ในฟิลด์ คำอธิบาย ให้พิมพ์ค่า</span><span class="sxs-lookup"><span data-stu-id="374e2-112">In the Description field, type a value.</span></span>
7. <span data-ttu-id="374e2-113">ในฟิลด์เดบิต ให้ป้อนตัวเลข</span><span class="sxs-lookup"><span data-stu-id="374e2-113">In the Debit field, enter a number.</span></span>
8. <span data-ttu-id="374e2-114">ในฟิลด์บัญชีตรงข้าม ให้ระบุค่าที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="374e2-114">In the Offset account field, specify the desired values.</span></span>
9. <span data-ttu-id="374e2-115">คลิกฟังก์ชัน</span><span class="sxs-lookup"><span data-stu-id="374e2-115">Click Functions.</span></span>
10. <span data-ttu-id="374e2-116">คลิกการรับรู้บัญชีแยกประเภท</span><span class="sxs-lookup"><span data-stu-id="374e2-116">Click Ledger accruals.</span></span>
11. <span data-ttu-id="374e2-117">ในฟิลด์การระบุรายการค้างรับค้างจ่าย ให้คลิกปุ่มดรอปดาวน์เพื่อเปิดการค้นหา</span><span class="sxs-lookup"><span data-stu-id="374e2-117">In the Accrual identification field, click the drop-down button to open the lookup.</span></span>
12. <span data-ttu-id="374e2-118">ในรายการ ให้ค้นหาและเลือกแบบแผนการรับรู้ที่คุณต้องการนำไปใช้</span><span class="sxs-lookup"><span data-stu-id="374e2-118">In the list, find and select the accural scheme you want to apply.</span></span>
13. <span data-ttu-id="374e2-119">ในรายการนี้ ให้คลิกลิงค์ในแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="374e2-119">In the list, click the link in the selected row.</span></span>
14. <span data-ttu-id="374e2-120">ในฟิลด์วันที่เริ่มต้น ให้ป้อนวันที่ </span><span class="sxs-lookup"><span data-stu-id="374e2-120">In the Start date field, enter a date.</span></span>
15. <span data-ttu-id="374e2-121">คลิกธุรกรรม</span><span class="sxs-lookup"><span data-stu-id="374e2-121">Click Transactions.</span></span>
16. <span data-ttu-id="374e2-122">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="374e2-122">Close the page.</span></span>
17. <span data-ttu-id="374e2-123">คลิก ตกลง</span><span class="sxs-lookup"><span data-stu-id="374e2-123">Click OK.</span></span>
18. <span data-ttu-id="374e2-124">คลิก ลงรายการบัญชี</span><span class="sxs-lookup"><span data-stu-id="374e2-124">Click Post.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]