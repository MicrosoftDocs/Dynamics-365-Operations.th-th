---
title: นำฝากการชำระเงินของลูกค้า
description: 'ฝากการชำระเงินของลูกค้า '
author: ShivamPandey-msft
manager: AnnBe
ms.date: 07/18/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerJournalTable, LedgerJournalTransCustPaym, CustTableLookup
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 7357683e46df04c3dedd7e22607748512c9de94a
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 02/15/2021
ms.locfileid: "5220262"
---
# <a name="deposit-customer-payments"></a><span data-ttu-id="912c0-103">นำฝากการชำระเงินของลูกค้า</span><span class="sxs-lookup"><span data-stu-id="912c0-103">Deposit customer payments</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="912c0-104">ฝากการชำระเงินของลูกค้า </span><span class="sxs-lookup"><span data-stu-id="912c0-104">Deposit customer payments.</span></span> <span data-ttu-id="912c0-105">งานนี้ใช้บริษัทสาธิต USMF </span><span class="sxs-lookup"><span data-stu-id="912c0-105">This task uses the USMF demo company.</span></span>

1. <span data-ttu-id="912c0-106">ไปที่ **บานหน้าต่างนำทาง > โมดูล > บัญชีลูกหนี้ > การชำระเงิน > สมุดรายวันการชำระเงิน**</span><span class="sxs-lookup"><span data-stu-id="912c0-106">Go to **Navigation pane > Modules > Accounts receivable > Payments > Payment journal**.</span></span>
2. <span data-ttu-id="912c0-107">เลือก **ใหม่**</span><span class="sxs-lookup"><span data-stu-id="912c0-107">Select **New**.</span></span>
3. <span data-ttu-id="912c0-108">ในฟิลด์ **ชื่อ** ให้เลือก **CustPay** ในเมนูแบบหล่นลง</span><span class="sxs-lookup"><span data-stu-id="912c0-108">In the **Name** field, select **CustPay** in the drop-down menu.</span></span>
4. <span data-ttu-id="912c0-109">เลือก **รายการ**</span><span class="sxs-lookup"><span data-stu-id="912c0-109">Select **Lines**.</span></span>
5. <span data-ttu-id="912c0-110">ในฟิลด์ **บัญชี** เลือกลูกค้าที่คุณกำลังบันทึกการชำระเงิน</span><span class="sxs-lookup"><span data-stu-id="912c0-110">In the **Account** field, select the customer for whom you are recording the payment.</span></span>
6. <span data-ttu-id="912c0-111">ในฟิลด์ **เครดิต** ป้อนยอดเงินของการชำระเงิน</span><span class="sxs-lookup"><span data-stu-id="912c0-111">In the **Credit** field, enter the amount of the payment.</span></span> <span data-ttu-id="912c0-112">คุณสามารถเลือกที่จะข้ามช่องยอดเงิน และให้ระบบคำนวณให้โดยการเลือกใบแจ้งหนี้ที่ชำระเงิน</span><span class="sxs-lookup"><span data-stu-id="912c0-112">You can choose to leave the amount blank, and have the system calculate it by selecting the invoices which were paid.</span></span>  
7. <span data-ttu-id="912c0-113">ในฟิลด์ **การอ้างอิงการชำระเงิน** ให้พิมพ์ค่า</span><span class="sxs-lookup"><span data-stu-id="912c0-113">In the **Payment reference** field, type a value.</span></span> <span data-ttu-id="912c0-114">การอ้างอิงการชำระเงินอาจเป็นหมายเลขเช็คสำหรับการชำระเงินที่คุณป้อน </span><span class="sxs-lookup"><span data-stu-id="912c0-114">The payment reference could be the check number for the payment you are entering.</span></span> <span data-ttu-id="912c0-115">การอ้างอิงการชำระเงินต้องระบุเพื่อจะรวมการชำระเงินบนใบนำฝากธนาคาร</span><span class="sxs-lookup"><span data-stu-id="912c0-115">The payment reference is required in order to include the payment on a deposit slip.</span></span>  
8. <span data-ttu-id="912c0-116">ทำเครื่องหมายที่กล่องนี้ใช้ใบนำฝากธนาคาร</span><span class="sxs-lookup"><span data-stu-id="912c0-116">Mark the box Use a deposit slip.</span></span> <span data-ttu-id="912c0-117">ถ้าการชำระเงินควรรวมอยู่ในเงินฝาก เปลี่ยนการตั้งค่านี้เป็น ใช่</span><span class="sxs-lookup"><span data-stu-id="912c0-117">If the payment should be included in the deposit, change this setting to Yes.</span></span>  
9. <span data-ttu-id="912c0-118">เลือก **ใหม่**</span><span class="sxs-lookup"><span data-stu-id="912c0-118">Select **New**.</span></span>
10. <span data-ttu-id="912c0-119">ในฟิลด์ **บัญชี** เลือกลูกค้าสำหรับการชำระเงินครั้งต่อไป</span><span class="sxs-lookup"><span data-stu-id="912c0-119">In the **Account** field, select the customer for the next payment.</span></span>
11. <span data-ttu-id="912c0-120">ในฟิลด์ **เครดิต** ป้อนยอดเงินของการชำระเงิน</span><span class="sxs-lookup"><span data-stu-id="912c0-120">In the **Credit** field, enter the payment amount.</span></span>
12. <span data-ttu-id="912c0-121">ในฟิลด์ **การอ้างอิงการชำระเงิน** ให้พิมพ์ค่า</span><span class="sxs-lookup"><span data-stu-id="912c0-121">In the **Payment reference** field, type a value.</span></span>
13. <span data-ttu-id="912c0-122">ทำเครื่องหมายที่กล่อง **ใช้ใบนำฝากธนาคาร**</span><span class="sxs-lookup"><span data-stu-id="912c0-122">Mark the box **Use a deposit slip**.</span></span>
14. <span data-ttu-id="912c0-123">เลือก **ลงรายการบัญชี**</span><span class="sxs-lookup"><span data-stu-id="912c0-123">Select **Post**.</span></span> <span data-ttu-id="912c0-124">การชำระเงินต้องลงรายการก่อนที่จะสร้างใบนำฝากธนาคาร </span><span class="sxs-lookup"><span data-stu-id="912c0-124">Payments must be posted before the deposit slip can be generated.</span></span> <span data-ttu-id="912c0-125">ทั้งนี้เพื่อให้แน่ใจว่า การชำระเงินจะไม่เปลี่ยนแปลงหลังจากใบนำฝากธนาคารถูกสร้าง</span><span class="sxs-lookup"><span data-stu-id="912c0-125">This is to ensure that the payments don't change after the deposit slip is generated.</span></span>  
15. <span data-ttu-id="912c0-126">เลือก **ฟังก์ชัน**</span><span class="sxs-lookup"><span data-stu-id="912c0-126">Select **Functions**.</span></span>
16. <span data-ttu-id="912c0-127">เลือก **ใบนำฝาก**</span><span class="sxs-lookup"><span data-stu-id="912c0-127">Select **Deposit slip**.</span></span>
17. <span data-ttu-id="912c0-128">เลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="912c0-128">Select **OK**.</span></span> <span data-ttu-id="912c0-129">หน้าแรกใช้สำหรับสร้างใบนำฝากธนาคาร</span><span class="sxs-lookup"><span data-stu-id="912c0-129">The first page is used to create the deposit slip.</span></span>  
18. <span data-ttu-id="912c0-130">เลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="912c0-130">Select **OK**.</span></span> <span data-ttu-id="912c0-131">ขั้นตอนที่สองคือการพิมพ์ใบนำฝากธนาคาร แต่ขั้นตอนนี้ไม่จำเป็น</span><span class="sxs-lookup"><span data-stu-id="912c0-131">The second step is to print the deposit slip, but this step is not required.</span></span>  



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]