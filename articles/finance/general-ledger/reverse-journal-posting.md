---
title: กลับรายการการลงรายการบัญชีสมุดรายวัน
description: หัวข้อนี้อธิบายความสามารถเรื่องที่อนุญาตให้คุณกลับรายการใบสำคัญจากรายการธุรกรรมใบสำคัญหรือจากบัญชีสมุดรายวันทางการเงิน
author: MikeFalkner
manager: AnnBe
ms.date: 10/08/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerTransVoucher, LedgerJournalTable
audience: Application User
ms.reviewer: roschloma
ms.custom: 15721
ms.assetid: b4b406fa-b772-44ec-8dd8-8eb818a921ef
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 19f7ea540035a3bc9eba445c508cb6f29e4bd20f
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 02/15/2021
ms.locfileid: "5205013"
---
# <a name="reverse-journal-posting"></a><span data-ttu-id="b9976-103">กลับรายการการลงรายการบัญชีสมุดรายวัน</span><span class="sxs-lookup"><span data-stu-id="b9976-103">Reverse journal posting</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="b9976-104">หัวข้อนี้จะอธิบายความสามารถของ Microsoft Dynamics 365 Finance ซึ่งช่วยให้คุณสามารถย้อนกลับสมุดรายวันทั้งหมด หรือกลับรายการใบสำคัญหนึ่งใบขึ้นไปจากรายการธุรกรรมใบสำคัญได้ โดยไม่คำนึงถึงจุดเริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="b9976-104">This topic describes capabilities Microsoft Dynamics 365 Finance that allows you to reverse an entire journal, or reverse one or more vouchers from the voucher transaction list, regardless of their origin.</span></span> 

## <a name="reversing-journals"></a><span data-ttu-id="b9976-105">การกลับรายการสมุดรายวัน</span><span class="sxs-lookup"><span data-stu-id="b9976-105">Reversing journals</span></span>

<span data-ttu-id="b9976-106">คุณสามารถกลับรายการสมุดรายวันแต่ละบรรทัดได้</span><span class="sxs-lookup"><span data-stu-id="b9976-106">You can reverse journal lines individually.</span></span> <span data-ttu-id="b9976-107">เมื่อมีการกลับรายการการลงบัญชีสมุดรายวันคุณยังสามารถกลับรายการสมุดรายวันทางการเงินทั้งหมดได้ด้วย</span><span class="sxs-lookup"><span data-stu-id="b9976-107">With reverse journal posting, you can also reverse an entire financial journal.</span></span> <span data-ttu-id="b9976-108">เมื่อต้องการกลับรายการสมุดรายวัน:</span><span class="sxs-lookup"><span data-stu-id="b9976-108">To reverse a journal:</span></span> 

- <span data-ttu-id="b9976-109">เปิดสมุดรายวันทางการเงินและกรองข้อมูลในสมุดรายวันที่ลงรายการบัญชี</span><span class="sxs-lookup"><span data-stu-id="b9976-109">Open the financial journal and filter on posted journals.</span></span>
- <span data-ttu-id="b9976-110">เลือกเมนู **กลับรายการ** ที่ด้านบนของหน้า</span><span class="sxs-lookup"><span data-stu-id="b9976-110">Select the **Reverse** menu at the top of the page.</span></span>
- <span data-ttu-id="b9976-111">คุณจะเห็นจำนวนรวมของใบสำคัญและบรรทัดใบสำคัญรวมทั้งยอดรวมของรายการที่มีการกลับรายการ</span><span class="sxs-lookup"><span data-stu-id="b9976-111">You will see the total number of vouchers and voucher lines as well as the total amount of the lines being reversed</span></span>
- <span data-ttu-id="b9976-112">เลือก **ใช่** เพื่อใช้วันที่ของธุรกรรมที่มีอยู่ หรือ **ไม่ใช่** เพื่อป้อนวันที่ใหม่</span><span class="sxs-lookup"><span data-stu-id="b9976-112">Select **Yes** to use the existing transaction dates or **No** to enter a new one.</span></span> <span data-ttu-id="b9976-113">ในบางกรณี รอบระยะเวลาของธุรกรรมเดิมอาจปิดแล้ว และคุณต้องป้อนวันที่ธุรกรรมใหม่สำหรับการกลับรายการ</span><span class="sxs-lookup"><span data-stu-id="b9976-113">In some cases, the period of the original transaction may be closed and you must enter a new transaction date for the reversal.</span></span>
- <span data-ttu-id="b9976-114">ถ้าคุณเลือก **ไม่ใช่** ให้ป้อนวันที่ธุรกรรมสำหรับการกลับรายการ</span><span class="sxs-lookup"><span data-stu-id="b9976-114">If you select **No**, enter a transaction date for the reversal.</span></span> 
- <span data-ttu-id="b9976-115">ป้อนข้อคิดเห็นที่คุณต้องการให้เพิ่มลงในธุรกรรมการกลับรายการ</span><span class="sxs-lookup"><span data-stu-id="b9976-115">Enter a comment that you want added to the reversal transaction.</span></span>
- <span data-ttu-id="b9976-116">เลือกปุ่ม **กลับรายการ**</span><span class="sxs-lookup"><span data-stu-id="b9976-116">Select the **Reverse** button.</span></span>

<span data-ttu-id="b9976-117"> ธุรกรรมจะถูกกลับรายการ </span><span class="sxs-lookup"><span data-stu-id="b9976-117">The transactions will be reversed.</span></span> 

<span data-ttu-id="b9976-118">ถ้าใบสำคัญประกอบด้วยรายการมากกว่า 100 รายการ กระบวนการกลับรายการจะรันโดยใช้กระบวนการชุดงาน</span><span class="sxs-lookup"><span data-stu-id="b9976-118">If the voucher contains more than 100 lines, the reversal process will run using the batch process.</span></span> <span data-ttu-id="b9976-119">คุณสามารถตรวจสอบผลลัพธ์ได้โดยการดูข้อคิดเห็นในชุดงาน</span><span class="sxs-lookup"><span data-stu-id="b9976-119">You can review the results by viewing the comments in the batch job.</span></span> <span data-ttu-id="b9976-120">ธุรกรรมใดๆ ที่ไม่สามารถกลับรายการได้ จะถูกแสดงรายการอยู่ในประวัติชุดงาน</span><span class="sxs-lookup"><span data-stu-id="b9976-120">Any transactions that couldn't be reversed will be listed in the batch job history.</span></span>

<span data-ttu-id="b9976-121">ถ้าใบสำคัญประกอบด้วยรายการ 100 รายการหรือน้อยกว่า กระบวนการกลับรายการจะรันทันที</span><span class="sxs-lookup"><span data-stu-id="b9976-121">If the voucher contains 100 lines or fewer, the reversal process will run immediately.</span></span> <span data-ttu-id="b9976-122">ผลลัพธ์จะแสดงในกล่องโต้ตอบที่แสดงใบสำคัญใดๆ ที่ไม่สามารถกลับรายการได้ พร้อมกับเหตุผลที่ไม่สามารถกลับรายการได้</span><span class="sxs-lookup"><span data-stu-id="b9976-122">The results will be presented in a dialog box that shows any voucher that could not be reversed, along with the reason why it could not be reversed.</span></span> <span data-ttu-id="b9976-123">เลือก **ตกลง** เพื่อปิดกล่องโต้ตอบ</span><span class="sxs-lookup"><span data-stu-id="b9976-123">Select **OK** to close the dialog box.</span></span>

## <a name="reversing-vouchers-from-the-voucher-transaction-list"></a><span data-ttu-id="b9976-124">กลับรายการใบสำคัญจากรายการธุรกรรมใบสำคัญ</span><span class="sxs-lookup"><span data-stu-id="b9976-124">Reversing vouchers from the voucher transaction list.</span></span> 

<span data-ttu-id="b9976-125">นอกจากนี้คุณยังกลับรายการใบสำคัญจาก **รายการธุรกรรมใบสำคัญ** ผ่านประเภทย่อยทั้งหมดได้ด้วย</span><span class="sxs-lookup"><span data-stu-id="b9976-125">You can also reverse vouchers from the **Voucher transaction list** across all subledgers.</span></span> <span data-ttu-id="b9976-126">นอกจากนี้คุณยังสามารถกลับรายการใบสำคัญได้มากกว่าหนึ่งใบในเวลาเดียวกัน</span><span class="sxs-lookup"><span data-stu-id="b9976-126">In addition, you can reverse more than one voucher at a time.</span></span> 

<span data-ttu-id="b9976-127">เมื่อต้องการกลับรายการใบสำคัญหนึ่งใบขึ้นไปให้ปฏิบัติดังนี้</span><span class="sxs-lookup"><span data-stu-id="b9976-127">To reverse one or more vouchers:</span></span> 

- <span data-ttu-id="b9976-128">เลือกเมนู **กลับรายการ** ที่ด้านบนของหน้า</span><span class="sxs-lookup"><span data-stu-id="b9976-128">Select the **Reverse** menu at the top of the page</span></span>
- <span data-ttu-id="b9976-129">คุณจะเห็นจำนวนรวมของใบสำคัญและรายการใบสำคัญ รวมทั้งยอดรวมของรายการที่มีการกลับรายการ</span><span class="sxs-lookup"><span data-stu-id="b9976-129">You will see the total number of vouchers and voucher lines as well as the total amount of the lines being reversed.</span></span>
- <span data-ttu-id="b9976-130">เลือก **ใช่** เพื่อใช้วันที่ของธุรกรรมที่มีอยู่ หรือ **ไม่ใช่** เพื่อป้อนวันที่ใหม่</span><span class="sxs-lookup"><span data-stu-id="b9976-130">Select **Yes** to use the existing transaction dates or **No** to enter a new one.</span></span> <span data-ttu-id="b9976-131">ในบางกรณี รอบระยะเวลาของธุรกรรมเดิมอาจปิดแล้ว และคุณต้องป้อนวันที่ธุรกรรมใหม่เพื่อกลับรายการ</span><span class="sxs-lookup"><span data-stu-id="b9976-131">In some cases, the period of the original transaction may be closed and you must enter a new transaction date to reverse it.</span></span>
- <span data-ttu-id="b9976-132">ถ้าคุณเลือก **ไม่ใช่** ให้ป้อนวันที่ธุรกรรมสำหรับการกลับรายการ</span><span class="sxs-lookup"><span data-stu-id="b9976-132">If you select **No**, enter a transaction date for the reversal.</span></span> 
- <span data-ttu-id="b9976-133">ป้อนข้อคิดเห็นเพื่ออธิบายธุรกรรมที่กลับรายการ</span><span class="sxs-lookup"><span data-stu-id="b9976-133">Enter a comment to describe the reversal transaction.</span></span>
- <span data-ttu-id="b9976-134">เลือกปุ่ม **กลับรายการ**</span><span class="sxs-lookup"><span data-stu-id="b9976-134">Select the **Reverse** button.</span></span>

<span data-ttu-id="b9976-135"> ธุรกรรมจะถูกกลับรายการ </span><span class="sxs-lookup"><span data-stu-id="b9976-135">The transactions will be reversed.</span></span> 

<span data-ttu-id="b9976-136">ถ้ามีรายการใบสำคัญมากกว่า 100 รายการ กระบวนการกลับรายการจะรันโดยใช้กระบวนการชุดงาน</span><span class="sxs-lookup"><span data-stu-id="b9976-136">If there are more than 100 voucher lines, the reversal process will run using the batch process.</span></span> <span data-ttu-id="b9976-137">คุณสามารถตรวจสอบผลลัพธ์ได้โดยการดูข้อคิดเห็นในชุดงาน</span><span class="sxs-lookup"><span data-stu-id="b9976-137">You can review the results by viewing the comments in the batch job.</span></span> <span data-ttu-id="b9976-138">ธุรกรรมใดๆ ที่ไม่สามารถกลับรายการได้ จะถูกบันทึกในประวัติชุดงาน</span><span class="sxs-lookup"><span data-stu-id="b9976-138">Any transactions that couldn't be reversed will be noted in the batch job history.</span></span>

<span data-ttu-id="b9976-139">ถ้าจำนวนของรายการใบสำคัญเท่ากับ 100 รายการหรือน้อยกว่า กระบวนการกลับรายการจะรันทันที</span><span class="sxs-lookup"><span data-stu-id="b9976-139">If the number of voucher lines is 100 lines or fewer, the reversal process will run immediately.</span></span> <span data-ttu-id="b9976-140">ผลลัพธ์จะแสดงในกล่องโต้ตอบที่แสดงใบสำคัญใดๆ ที่ไม่สามารถกลับรายการได้ พร้อมกับเหตุผล</span><span class="sxs-lookup"><span data-stu-id="b9976-140">The results will display in a dialog box that shows any voucher that couldn't be reversed, along with the reason why.</span></span> <span data-ttu-id="b9976-141">เลือก **ตกลง** เพื่อปิดกล่องโต้ตอบ</span><span class="sxs-lookup"><span data-stu-id="b9976-141">Select **OK** to close the dialog box.</span></span>

<span data-ttu-id="b9976-142">คุณสามารถกลับรายการธุรกรรมได้ก็ต่อเมื่อเป็นไปตามกฎทางธุรกิจสำหรับการกลับรายการ</span><span class="sxs-lookup"><span data-stu-id="b9976-142">Transactions can be reversed only if they meet the business rules for reversing them.</span></span> <span data-ttu-id="b9976-143">ไม่สามารถกลับรายการการชำระเงินให้แก่ผู้จัดจำหน่ายโดยใช้ความสามารถที่อธิบายไว้ในหัวข้อนี้</span><span class="sxs-lookup"><span data-stu-id="b9976-143">Vendor payments cannot be reversed using the capability described in this topic.</span></span> <span data-ttu-id="b9976-144">ต้องกลับรายการการชำระเงินให้แก่ผู้จัดจำหน่ายโดยปฏิบัติตามขั้นตอนที่แสดงรายการใน [กลับรายการการชำระเงินให้แก่ผู้จัดจำหน่าย](https://docs.microsoft.com/dynamics365/finance/accounts-payable/reverse-vendor-payment)</span><span class="sxs-lookup"><span data-stu-id="b9976-144">Vendor payments must be reversed by following the steps listed in [Reverse a vendor payment](https://docs.microsoft.com/dynamics365/finance/accounts-payable/reverse-vendor-payment).</span></span>



[!INCLUDE[footer-include](../../includes/footer-banner.md)]