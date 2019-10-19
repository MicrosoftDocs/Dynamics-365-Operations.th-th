---
title: กลับรายการการลงรายการบัญชีสมุดรายวัน
description: หัวข้อนี้อธิบายความสามารถเรื่องที่อนุญาตให้คุณกลับรายการใบสำคัญจากรายการธุรกรรมใบสำคัญหรือจากบัญชีสมุดรายวันทางการเงิน
author: MikeFalkner
manager: AnnBe
ms.date: 08/01/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerTransVoucher, LedgerJournalTable
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 15721
ms.assetid: b4b406fa-b772-44ec-8dd8-8eb818a921ef
ms.search.region: Global
ms.author: mikefalkner
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 5a5456e60f1f3cee5f83ac7f725f7e01ba5bd7a1
ms.sourcegitcommit: 2460d0da812c45fce67a061386db52e0ae46b0f3
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 09/30/2019
ms.locfileid: "2248596"
---
# <a name="reverse-journal-posting"></a><span data-ttu-id="b69de-103">กลับรายการการลงรายการบัญชีสมุดรายวัน</span><span class="sxs-lookup"><span data-stu-id="b69de-103">Reverse journal posting</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="b69de-104">หัวข้อนี้จะอธิบายความสามารถของ Microsoft Dynamics 365 Finance ซึ่งช่วยให้คุณสามารถย้อนกลับสมุดรายวันทั้งหมดหรือกลับรายการใบสำคัญหนึ่งใบขึ้นไปจากรายการธุรกรรมใบสำคัญได้โดยไม่คำนึงถึงจุดเริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="b69de-104">This topic describes capabilities Microsoft Dynamics 365 Finance that allows you to reverse an entire journal or reverse one or more vouchers from the voucher transaction list regardless of their origin.</span></span> 

## <a name="reversing-journals"></a><span data-ttu-id="b69de-105">การกลับรายการสมุดรายวัน</span><span class="sxs-lookup"><span data-stu-id="b69de-105">Reversing journals</span></span>

<span data-ttu-id="b69de-106">คุณสามารถกลับรายการสมุดรายวันแต่ละบรรทัดได้</span><span class="sxs-lookup"><span data-stu-id="b69de-106">You can reverse journal lines individually.</span></span> <span data-ttu-id="b69de-107">เมื่อมีการกลับรายการการลงบัญชีสมุดรายวันคุณยังสามารถกลับรายการสมุดรายวันทางการเงินทั้งหมดได้ด้วย</span><span class="sxs-lookup"><span data-stu-id="b69de-107">With reverse journal posting, you can also reverse an entire financial journal.</span></span> <span data-ttu-id="b69de-108">เมื่อต้องการกลับรายการสมุดรายวัน:</span><span class="sxs-lookup"><span data-stu-id="b69de-108">To reverse a journal:</span></span> 
- <span data-ttu-id="b69de-109">เปิดสมุดรายวันทางการเงินและกรองข้อมูลในสมุดรายวันที่ลงรายการบัญชี</span><span class="sxs-lookup"><span data-stu-id="b69de-109">Open the financial journal and filter on posted journals</span></span>
- <span data-ttu-id="b69de-110">คลิกไปที่เมนูการกลับรายการที่ด้านบนของหน้า</span><span class="sxs-lookup"><span data-stu-id="b69de-110">Click on the Reverse menu at the top of the page</span></span>
- <span data-ttu-id="b69de-111">คุณจะเห็นจำนวนรวมของใบสำคัญและบรรทัดใบสำคัญรวมทั้งยอดรวมของรายการที่มีการกลับรายการ</span><span class="sxs-lookup"><span data-stu-id="b69de-111">You will see the total number of vouchers and voucher lines as well as the total amount of the lines being reversed</span></span>
- <span data-ttu-id="b69de-112">เลือกใช่เพื่อใช้วันที่ของธุรกรรมที่มีอยู่หรือไม่ใช่เพื่อป้อนวันที่ใหม่</span><span class="sxs-lookup"><span data-stu-id="b69de-112">Select Yes to use the existing transaction dates or No to enter a new one.</span></span> <span data-ttu-id="b69de-113">ในบางกรณีรอบระยะเวลาของธุรกรรมเดิมอาจปิดแล้วและคุณต้องการป้อนวันที่ธุรกรรมใหม่สำหรับการกลับรายการ</span><span class="sxs-lookup"><span data-stu-id="b69de-113">In some cases, the period of the original transaction may be closed and you want to enter a new transaction date for the reversal.</span></span>
- <span data-ttu-id="b69de-114">ถ้าคุณเลือกไม่ใช่ให้ป้อนวันที่ธุรกรรมสำหรับการกลับรายการ</span><span class="sxs-lookup"><span data-stu-id="b69de-114">If you selected No, enter a transaction date for the reversal.</span></span> 
- <span data-ttu-id="b69de-115">ป้อนข้อคิดเห็นที่คุณต้องการให้เพิ่มลงในธุรกรรมการกลับรายการ</span><span class="sxs-lookup"><span data-stu-id="b69de-115">Enter a comment that you want added to the reversal transaction</span></span>
- <span data-ttu-id="b69de-116">คลิกที่ปุ่ม Reverse </span><span class="sxs-lookup"><span data-stu-id="b69de-116">Click the Reverse button</span></span>

<span data-ttu-id="b69de-117"> ธุรกรรมจะถูกกลับรายการ </span><span class="sxs-lookup"><span data-stu-id="b69de-117">The transactions will be reversed.</span></span> 

<span data-ttu-id="b69de-118">ถ้าหมายเลขของรายการใบสำคัญเกินกว่า 100 บรรทัด กระบวนการกลับรายการจะถูกรันโดยใช้กระบวนการชุดงาน</span><span class="sxs-lookup"><span data-stu-id="b69de-118">If the number of voucher lines exceeds 100 lines, the reversal process will be run using the batch process.</span></span> <span data-ttu-id="b69de-119">คุณสามารถตรวจสอบผลลัพธ์ของการกลับรายการได้โดยดูข้อคิดเห็นในชุดงานที่รันอยู่</span><span class="sxs-lookup"><span data-stu-id="b69de-119">You can review the results of the reversal by viewing the comments in the batch job that was run.</span></span> <span data-ttu-id="b69de-120">ความล้มเหลวทั้งหมดจะได้รับการบันทึกไว้ในประวัติชุดงาน</span><span class="sxs-lookup"><span data-stu-id="b69de-120">All failures will be noted in the batch job history.</span></span>

<span data-ttu-id="b69de-121">ถ้าจำนวนรายการใบสำคัญมี 100 บรรทัดหรือน้อยกว่า กระบวนการกลับรายการจะรันทันที</span><span class="sxs-lookup"><span data-stu-id="b69de-121">If the number of voucher lines is 100 lines or less, the reversal process will run immediately.</span></span> <span data-ttu-id="b69de-122">ผลลัพธ์จะแสดงในกล่องโต้ตอบที่แสดงใบสำคัญใดๆก็ตามที่ไม่สามารถกลับรายการและเหตุผลที่ไม่สามารถกลับรายการได้</span><span class="sxs-lookup"><span data-stu-id="b69de-122">The results will be presented in a dialog that shows any voucher that could not be reversed and the reason why it could not be reversed.</span></span> <span data-ttu-id="b69de-123">คลิกบน Ok เพื่อปิดกล่องโต้ตอบ</span><span class="sxs-lookup"><span data-stu-id="b69de-123">Click on Ok to close the dialog.</span></span>

## <a name="reversing-vouchers-from-the-voucher-transaction-list"></a><span data-ttu-id="b69de-124">กลับรายการใบสำคัญจากรายการธุรกรรมใบสำคัญ</span><span class="sxs-lookup"><span data-stu-id="b69de-124">Reversing vouchers from the voucher transaction list.</span></span> 

<span data-ttu-id="b69de-125">นอกจากนี้คุณยังกลับรายการใบสำคัญจาก **รายการธุรกรรมใบสำคัญ** ผ่านประเภทย่อยทั้งหมดได้ด้วย</span><span class="sxs-lookup"><span data-stu-id="b69de-125">You can also reverse vouchers from the **Voucher transaction list** across all subledgers.</span></span> <span data-ttu-id="b69de-126">นอกจากนี้คุณยังสามารถกลับรายการใบสำคัญได้มากกว่าหนึ่งใบในเวลาเดียวกัน</span><span class="sxs-lookup"><span data-stu-id="b69de-126">In addition, you can reverse more than one voucher at a time.</span></span> 

<span data-ttu-id="b69de-127">เมื่อต้องการกลับรายการใบสำคัญหนึ่งใบขึ้นไปให้ปฏิบัติดังนี้</span><span class="sxs-lookup"><span data-stu-id="b69de-127">To reverse one or more vouchers:</span></span> 
- <span data-ttu-id="b69de-128">คลิกไปที่เมนูการกลับรายการที่ด้านบนของหน้า</span><span class="sxs-lookup"><span data-stu-id="b69de-128">Click on the Reverse menu at the top of the page</span></span>
- <span data-ttu-id="b69de-129">คุณจะเห็นจำนวนรวมของใบสำคัญและบรรทัดใบสำคัญรวมทั้งยอดรวมของรายการที่มีการกลับรายการ</span><span class="sxs-lookup"><span data-stu-id="b69de-129">You will see the total number of vouchers and voucher lines as well as the total amount of the lines being reversed</span></span>
- <span data-ttu-id="b69de-130">เลือกใช่เพื่อใช้วันที่ของธุรกรรมที่มีอยู่หรือไม่ใช่เพื่อป้อนวันที่ใหม่</span><span class="sxs-lookup"><span data-stu-id="b69de-130">Select Yes to use the existing transaction dates or No to enter a new one.</span></span> <span data-ttu-id="b69de-131">ในบางกรณีรอบระยะเวลาของธุรกรรมเดิมอาจปิดแล้วและคุณต้องการป้อนวันที่ธุรกรรมใหม่สำหรับการกลับรายการ</span><span class="sxs-lookup"><span data-stu-id="b69de-131">In some cases, the period of the original transaction may be closed and you want to enter a new transaction date for the reversal.</span></span>
- <span data-ttu-id="b69de-132">ถ้าคุณเลือกไม่ใช่ให้ป้อนวันที่ธุรกรรมสำหรับการกลับรายการ</span><span class="sxs-lookup"><span data-stu-id="b69de-132">If you selected No, enter a transaction date for the reversal.</span></span> 
- <span data-ttu-id="b69de-133">ป้อนข้อคิดเห็นที่คุณต้องการให้เพิ่มลงในธุรกรรมการกลับรายการ</span><span class="sxs-lookup"><span data-stu-id="b69de-133">Enter a comment that you want added to the reversal transaction</span></span>
- <span data-ttu-id="b69de-134">คลิกที่ปุ่ม Reverse </span><span class="sxs-lookup"><span data-stu-id="b69de-134">Click the Reverse button</span></span>

<span data-ttu-id="b69de-135"> ธุรกรรมจะถูกกลับรายการ </span><span class="sxs-lookup"><span data-stu-id="b69de-135">The transactions will be reversed.</span></span> 

<span data-ttu-id="b69de-136">ถ้าหมายเลขของรายการใบสำคัญเกินกว่า 100 บรรทัด กระบวนการกลับรายการจะถูกรันโดยใช้กระบวนการชุดงาน</span><span class="sxs-lookup"><span data-stu-id="b69de-136">If the number of voucher lines exceeds 100 lines, the reversal process will be run using the batch process.</span></span> <span data-ttu-id="b69de-137">คุณสามารถตรวจสอบผลลัพธ์ของการกลับรายการได้โดยดูข้อคิดเห็นในชุดงานที่รันอยู่</span><span class="sxs-lookup"><span data-stu-id="b69de-137">You can review the results of the reversal by viewing the comments in the batch job that was run.</span></span> <span data-ttu-id="b69de-138">ความล้มเหลวทั้งหมดจะได้รับการบันทึกไว้ในประวัติชุดงาน</span><span class="sxs-lookup"><span data-stu-id="b69de-138">All failures will be noted in the batch job history.</span></span>

<span data-ttu-id="b69de-139">ถ้าจำนวนรายการใบสำคัญมี 100 บรรทัดหรือน้อยกว่า กระบวนการกลับรายการจะรันทันที</span><span class="sxs-lookup"><span data-stu-id="b69de-139">If the number of voucher lines is 100 lines or less, the reversal process will run immediately.</span></span> <span data-ttu-id="b69de-140">ผลลัพธ์จะแสดงในกล่องโต้ตอบที่แสดงใบสำคัญใดๆก็ตามที่ไม่สามารถกลับรายการและเหตุผลที่ไม่สามารถกลับรายการได้</span><span class="sxs-lookup"><span data-stu-id="b69de-140">The results will be presented in a dialog that shows any voucher that could not be reversed and the reason why it could not be reversed.</span></span> <span data-ttu-id="b69de-141">คลิกบน Ok เพื่อปิดกล่องโต้ตอบ</span><span class="sxs-lookup"><span data-stu-id="b69de-141">Click on Ok to close the dialog.</span></span>

