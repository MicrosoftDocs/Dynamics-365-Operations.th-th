---
title: นำฝากการชำระเงินของลูกค้า
description: 'ฝากการชำระเงินของลูกค้า '
author: ShivamPandey-msft
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerJournalTable, LedgerJournalTransCustPaym, CustTableLookup
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: f58cebce20e8516dc918e0bad1e020ffd7f791ee
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 05/15/2019
ms.locfileid: "1565496"
---
# <a name="deposit-customer-payments"></a><span data-ttu-id="638ac-103">นำฝากการชำระเงินของลูกค้า</span><span class="sxs-lookup"><span data-stu-id="638ac-103">Deposit customer payments</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="638ac-104">ฝากการชำระเงินของลูกค้า </span><span class="sxs-lookup"><span data-stu-id="638ac-104">Deposit customer payments.</span></span> <span data-ttu-id="638ac-105">งานนี้ใช้บริษัทสาธิต USMF </span><span class="sxs-lookup"><span data-stu-id="638ac-105">This task uses the USMF demo company.</span></span>

1. <span data-ttu-id="638ac-106">ไปที่บัญชีเจ้าหนี้ > การชำระเงิน > สมุดรายวันการชำระเงิน</span><span class="sxs-lookup"><span data-stu-id="638ac-106">Go to Accounts receivable > Payments > Payment journal.</span></span>
2. <span data-ttu-id="638ac-107">คลิก สร้าง</span><span class="sxs-lookup"><span data-stu-id="638ac-107">Click New.</span></span>
3. <span data-ttu-id="638ac-108">ในฟิลด์ชื่อ ให้คลิกปุ่มดรอปดาวน์เพื่อเปิดการค้นหา</span><span class="sxs-lookup"><span data-stu-id="638ac-108">In the Name field, click the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="638ac-109">เลือกสมุดรายวันการชำระเงิน</span><span class="sxs-lookup"><span data-stu-id="638ac-109">Select the payment journal.</span></span> 
5. <span data-ttu-id="638ac-110">คลิกรายการ</span><span class="sxs-lookup"><span data-stu-id="638ac-110">Click Lines.</span></span>
6. <span data-ttu-id="638ac-111">ในฟิลด์บัญชี เลือกลูกค้าที่คุณกำลังบันทึกการชำระเงิน</span><span class="sxs-lookup"><span data-stu-id="638ac-111">In the Account field, select the Customer for whom you are recording the payment.</span></span>
7. <span data-ttu-id="638ac-112">ในฟิลด์เครดิต ป้อนยอดเงินของการชำระเงิน</span><span class="sxs-lookup"><span data-stu-id="638ac-112">In the Credit field, enter the amount of the payment.</span></span>
    * <span data-ttu-id="638ac-113">คุณสามารถเลือกที่จะข้ามช่องยอดเงิน และให้ระบบคำนวณให้โดยการเลือกใบแจ้งหนี้ที่ชำระเงิน</span><span class="sxs-lookup"><span data-stu-id="638ac-113">You can choose to leave the amount blank, and have the system calculate it by selecting the invoices which were paid.</span></span>  
8. <span data-ttu-id="638ac-114">ในฟิลด์ข้อมูลอ้างอิงการชำระเงิน ให้พิมพ์ค่า</span><span class="sxs-lookup"><span data-stu-id="638ac-114">In the Payment reference field, type a value.</span></span>
    * <span data-ttu-id="638ac-115">การอ้างอิงการชำระเงินอาจเป็นหมายเลขเช็คสำหรับการชำระเงินที่คุณป้อน </span><span class="sxs-lookup"><span data-stu-id="638ac-115">The payment reference could be the check number for the payment you are entering.</span></span> <span data-ttu-id="638ac-116">การอ้างอิงการชำระเงินต้องระบุเพื่อจะรวมการชำระเงินบนใบนำฝากธนาคาร</span><span class="sxs-lookup"><span data-stu-id="638ac-116">The payment reference is required in order to include the payment on a deposit slip.</span></span>  
9. <span data-ttu-id="638ac-117">ทำเครื่องหมายที่กล่องนี้ใช้ใบนำฝากธนาคาร</span><span class="sxs-lookup"><span data-stu-id="638ac-117">Mark the box Use a deposit slip.</span></span>
    * <span data-ttu-id="638ac-118">ถ้าการชำระเงินควรรวมอยู่ในเงินฝาก เปลี่ยนการตั้งค่านี้เป็น ใช่</span><span class="sxs-lookup"><span data-stu-id="638ac-118">If the payment should be included in the deposit, change this setting to Yes.</span></span>  
10. <span data-ttu-id="638ac-119">คลิก สร้าง</span><span class="sxs-lookup"><span data-stu-id="638ac-119">Click New.</span></span>
11. <span data-ttu-id="638ac-120">ในฟิลด์บัญชี เลิกลูกค้าสำหรับการชำระเงินครั้งต่อไป</span><span class="sxs-lookup"><span data-stu-id="638ac-120">In the Account field, select the Customer for the next payment.</span></span>
12. <span data-ttu-id="638ac-121">ในฟิลด์เครดิต ป้อนยอดเงินของการชำระเงิน</span><span class="sxs-lookup"><span data-stu-id="638ac-121">In the Credit field, enter the payment amount.</span></span>
13. <span data-ttu-id="638ac-122">ในฟิลด์ข้อมูลอ้างอิงการชำระเงิน ให้พิมพ์ค่า</span><span class="sxs-lookup"><span data-stu-id="638ac-122">In the Payment reference field, type a value.</span></span>
14. <span data-ttu-id="638ac-123">ทำเครื่องหมายที่กล่องนี้ใช้ใบนำฝากธนาคาร</span><span class="sxs-lookup"><span data-stu-id="638ac-123">Mark the box Use a deposit slip.</span></span>
15. <span data-ttu-id="638ac-124">คลิก ลงรายการบัญชี</span><span class="sxs-lookup"><span data-stu-id="638ac-124">Click Post.</span></span>
    * <span data-ttu-id="638ac-125">การชำระเงินต้องลงรายการก่อนที่จะสร้างใบนำฝากธนาคาร </span><span class="sxs-lookup"><span data-stu-id="638ac-125">Payments must be posted before the deposit slip can be generated.</span></span> <span data-ttu-id="638ac-126">ทั้งนี้เพื่อให้แน่ใจว่า การชำระเงินจะไม่เปลี่ยนแปลงหลังจากใบนำฝากธนาคารถูกสร้าง</span><span class="sxs-lookup"><span data-stu-id="638ac-126">This is to ensure that the payments don't change after the deposit slip is generated.</span></span>  
16. <span data-ttu-id="638ac-127">คลิกฟังก์ชัน</span><span class="sxs-lookup"><span data-stu-id="638ac-127">Click Functions.</span></span>
17. <span data-ttu-id="638ac-128">คลิกใบนำฝากธนาคาร</span><span class="sxs-lookup"><span data-stu-id="638ac-128">Click Deposit slip.</span></span>
18. <span data-ttu-id="638ac-129">คลิก ตกลง</span><span class="sxs-lookup"><span data-stu-id="638ac-129">Click OK.</span></span>
    * <span data-ttu-id="638ac-130">หน้าแรกใช้สำหรับสร้างใบนำฝากธนาคาร</span><span class="sxs-lookup"><span data-stu-id="638ac-130">The first page is used to create the deposit slip.</span></span>  
19. <span data-ttu-id="638ac-131">คลิก ตกลง</span><span class="sxs-lookup"><span data-stu-id="638ac-131">Click OK.</span></span>
    * <span data-ttu-id="638ac-132">ขั้นตอนที่สองคือการพิมพ์ใบนำฝากธนาคาร แต่ขั้นตอนนี้ไม่จำเป็น</span><span class="sxs-lookup"><span data-stu-id="638ac-132">The second step is to print the deposit slip, but this step is not required.</span></span>  

