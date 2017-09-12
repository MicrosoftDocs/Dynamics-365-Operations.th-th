---
title: "การปิดบัญชีลูกหนี้"
description: 
author: ShivamPandey-msft
manager: AnnBe
ms.date: 08/22/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 59372
ms.assetid: c18d83e5-4adb-422a-91be-82a665d8288b
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: 2b2e827df0c679855af9624f8a2fb36cb23f359a
ms.contentlocale: th-th
ms.lasthandoff: 08/29/2017

---

# <a name="close-accounts-receivable"></a><span data-ttu-id="7bf2c-102">การปิดบัญชีลูกหนี้</span><span class="sxs-lookup"><span data-stu-id="7bf2c-102">Close Accounts receivable</span></span>

[!include[banner](../includes/banner.md)]




<span data-ttu-id="7bf2c-103">ตารางต่อไปนี้แสดงรายการหน้าที่สนับสนุนกระบวนการทางธุรกิจการปิดบัญชีลูกหนี้</span><span class="sxs-lookup"><span data-stu-id="7bf2c-103">The following table lists the pages that support the close Accounts receivable business process.</span></span>

> [!NOTE] 
> <span data-ttu-id="7bf2c-104">เมื่อต้องการเปิดหน้าในตารางต่อไปนี้ คุณต้องป้อนข้อมูลหรือระบุการตั้งค่าพารามิเตอร์</span><span class="sxs-lookup"><span data-stu-id="7bf2c-104">To open some of the pages in the table, you must enter information or specify parameter settings.</span></span>

<span data-ttu-id="7bf2c-105">**ภารกิจคอมโพเนนต์กระบวนการทางธุรกิจ**</span><span class="sxs-lookup"><span data-stu-id="7bf2c-105">**Business process component task**</span></span>                   

<span data-ttu-id="7bf2c-106">ปิดรอบระยะเวลาในบัญชีแยกประเภททั่วไป</span><span class="sxs-lookup"><span data-stu-id="7bf2c-106">Close periods in the general ledger</span></span>

| <span data-ttu-id="7bf2c-107">ชื่อหน้า</span><span class="sxs-lookup"><span data-stu-id="7bf2c-107">Page name</span></span>                            | <span data-ttu-id="7bf2c-108">การใช้</span><span class="sxs-lookup"><span data-stu-id="7bf2c-108">Usage</span></span>                                                                                      |
|--------------------------------------|--------------------------------------------------------------------------------------------|
|<span data-ttu-id="7bf2c-109">ชุดงาน</span><span class="sxs-lookup"><span data-stu-id="7bf2c-109">Batch job</span></span>                             | <span data-ttu-id="7bf2c-110">ดูหรือสร้างชุดงาน</span><span class="sxs-lookup"><span data-stu-id="7bf2c-110">View or create batch jobs.</span></span> <span data-ttu-id="7bf2c-111">ชุดงานอาจไม่เสร็จสมบูรณ์ และคุณต้องตรวจสอบให้แน่ใจว่าการลงรายการบัญชีทั้งหมดเสร็จสมบูรณ์แล้ว</span><span class="sxs-lookup"><span data-stu-id="7bf2c-111">Batch jobs might not be completed, and you want make sure that all posting is completed.</span></span>                                                                                                               |
|<span data-ttu-id="7bf2c-112">ยืนยันใบสั่งขาย</span><span class="sxs-lookup"><span data-stu-id="7bf2c-112">Confirm sales order</span></span>                   | <span data-ttu-id="7bf2c-113">อัพเดตใบสั่งขาย</span><span class="sxs-lookup"><span data-stu-id="7bf2c-113">Update sales orders.</span></span>                                                                       |
|<span data-ttu-id="7bf2c-114">การประเมินค่าใหม่ตามสกุลเงินต่างประเทศ</span><span class="sxs-lookup"><span data-stu-id="7bf2c-114">Foreign currency revaluation</span></span>          | <span data-ttu-id="7bf2c-115">สร้างธุรกรรมที่อัพเดตมูลค่าของธุรกรรมลูกค้าที่เปิดค้างไว้ในสกุลเงินต่างประเทศ</span><span class="sxs-lookup"><span data-stu-id="7bf2c-115">Generate transactions that update the value of open customer transactions in foreign currencies.</span></span>                                                                                                                         |
| <span data-ttu-id="7bf2c-116">สมุดรายวัน</span><span class="sxs-lookup"><span data-stu-id="7bf2c-116">Journal</span></span>                              | <span data-ttu-id="7bf2c-117">ลงรายการบัญชีใบแจ้งหนี้ การชำระเงิน และตั๋วสัญญาใช้เงิน</span><span class="sxs-lookup"><span data-stu-id="7bf2c-117">Post invoices, payments, and promissory notes.</span></span>                                             |
| <span data-ttu-id="7bf2c-118">ใบสำคัญสมุดรายวัน</span><span class="sxs-lookup"><span data-stu-id="7bf2c-118">Journal voucher</span></span>                      |<ul><li><span data-ttu-id="7bf2c-119">**สมุดรายวันการชำระเงิน** – สร้าง ประมวลผล และลงรายการบัญชีการชำระเงิน</span><span class="sxs-lookup"><span data-stu-id="7bf2c-119">**Payment journal** – Generate, process, and post payments.</span></span></li><li><span data-ttu-id="7bf2c-120">**สมุดรายวันการออกตั๋วแลกเงิน** – ลงรายการบัญชีตั๋วแลกเงิน</span><span class="sxs-lookup"><span data-stu-id="7bf2c-120">**Draw bill of exchange journal** – Post bills of exchange.</span></span></li><li><span data-ttu-id="7bf2c-121">**สมุดรายวันการปฏิเสธตั๋วแลกเงิน** – ลงรายการบัญชีตั๋วแลกเงินที่ปฏิเสธการจ่าย</span><span class="sxs-lookup"><span data-stu-id="7bf2c-121">**Protest bill of exchange journal** – Post protested bills of exchange.</span></span></li><li><span data-ttu-id="7bf2c-122">**สมุดรายวันการออกตั๋วแลกเงินใหม่** – ลงรายการบัญชีตั๋วแลกเงินที่ออกใหม่</span><span class="sxs-lookup"><span data-stu-id="7bf2c-122">**Redraw bill of exchange journal** – Post redrawn bills of exchange.</span></span></li><li><span data-ttu-id="7bf2c-123">**สมุดรายวันการชำระเงินผ่านธนาคาร** – ลงรายการบัญชีการชำระเงินผ่านธนาคาร</span><span class="sxs-lookup"><span data-stu-id="7bf2c-123">**Remittance journal** – Post remittances.</span></span></li><li><span data-ttu-id="7bf2c-124">**สมุดรายวันการชำระตั๋วแลกเงิน** – ลงรายการบัญชีตั๋วแลกเงินที่ชำระเงินแล้ว</span><span class="sxs-lookup"><span data-stu-id="7bf2c-124">**Settle bill of exchange journal** – Post settled bills of exchange</span></span></li></ul>                   |
| <span data-ttu-id="7bf2c-125">การลงรายการบัญชีบันทึกการจัดส่ง</span><span class="sxs-lookup"><span data-stu-id="7bf2c-125">Packing slip posting</span></span>                 | <span data-ttu-id="7bf2c-126">อัพเดตบันทึกการจัดส่งสำหรับใบสั่งขาย</span><span class="sxs-lookup"><span data-stu-id="7bf2c-126">Update packing slips for sales orders.</span></span>                                                     |
| <span data-ttu-id="7bf2c-127">ลงรายการบัญชีใบแจ้งหนี้ข้อความอิสระ</span><span class="sxs-lookup"><span data-stu-id="7bf2c-127">Post free text invoice</span></span>               | <span data-ttu-id="7bf2c-128">ลงรายการบัญชีใบแจ้งหนี้ข้อความอิสระ</span><span class="sxs-lookup"><span data-stu-id="7bf2c-128">Post free text invoices.</span></span>                                                                   |
| <span data-ttu-id="7bf2c-129">การลงรายการบัญชีใบแจ้งหนี้</span><span class="sxs-lookup"><span data-stu-id="7bf2c-129">Posting invoice</span></span>                      | <span data-ttu-id="7bf2c-130">ลงรายการบัญชีใบแจ้งหนี้สำหรับใบสั่งขาย</span><span class="sxs-lookup"><span data-stu-id="7bf2c-130">Post invoices for sales orders.</span></span>                                                            |
| <span data-ttu-id="7bf2c-131">การลงรายการบัญชีรายการเบิกสินค้า</span><span class="sxs-lookup"><span data-stu-id="7bf2c-131">Posting picking list</span></span>                 |<span data-ttu-id="7bf2c-132">อัพเดตรายการเบิกสินค้าสำหรับใบสั่งขาย</span><span class="sxs-lookup"><span data-stu-id="7bf2c-132">Update picking lists for sales orders.</span></span>                                                      |

<span data-ttu-id="7bf2c-133">**ภารกิจคอมโพเนนต์กระบวนการทางธุรกิจ**</span><span class="sxs-lookup"><span data-stu-id="7bf2c-133">**Business process component task**</span></span>   

<span data-ttu-id="7bf2c-134">การสร้างและการส่งรายการขายใน EU</span><span class="sxs-lookup"><span data-stu-id="7bf2c-134">Create and submit the EU sales list</span></span>

| <span data-ttu-id="7bf2c-135">ชื่อหน้า</span><span class="sxs-lookup"><span data-stu-id="7bf2c-135">Page name</span></span>                            | <span data-ttu-id="7bf2c-136">การใช้</span><span class="sxs-lookup"><span data-stu-id="7bf2c-136">Usage</span></span>                                                                                      |
|--------------------------------------|--------------------------------------------------------------------------------------------|
|<span data-ttu-id="7bf2c-137">รายการขายใน EU</span><span class="sxs-lookup"><span data-stu-id="7bf2c-137">EU sales list</span></span>                         | <span data-ttu-id="7bf2c-138">รายงานการขายในสหภาพยุโรป (EU) ไปยังหน่วยงานจัดเก็บภาษีสำหรับวัตถุประสงค์การรายงานภาษีมูลค่าเพิ่ม (VAT)</span><span class="sxs-lookup"><span data-stu-id="7bf2c-138">Report on European Union (EU) sales to the tax authority for value-added tax (VAT) declaration purposes.</span></span>                                                                                                                           |







