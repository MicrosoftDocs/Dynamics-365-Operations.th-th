---
title: การปิดบัญชีลูกหนี้
description: หัวข้อต่อไปนี้แสดงรายการหน้าที่สนับสนุนกระบวนการทางธุรกิจการปิดบัญชีลูกหนี้
author: ShivamPandey-msft
ms.date: 10/26/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 59372
ms.assetid: c18d83e5-4adb-422a-91be-82a665d8288b
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: bc3355f7fa6f72906e427203234de7ece27595e3
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 04/01/2021
ms.locfileid: "5835447"
---
# <a name="close-accounts-receivable"></a><span data-ttu-id="286f5-103">การปิดบัญชีลูกหนี้</span><span class="sxs-lookup"><span data-stu-id="286f5-103">Close Accounts receivable</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="286f5-104">ตารางต่อไปนี้แสดงรายการหน้าที่สนับสนุนกระบวนการทางธุรกิจการปิดบัญชีลูกหนี้</span><span class="sxs-lookup"><span data-stu-id="286f5-104">The following table lists the pages that support the close Accounts receivable business process.</span></span>

> [!NOTE] 
> <span data-ttu-id="286f5-105">เมื่อต้องการเปิดหน้าในตารางต่อไปนี้ คุณต้องป้อนข้อมูลหรือระบุการตั้งค่าพารามิเตอร์</span><span class="sxs-lookup"><span data-stu-id="286f5-105">To open some of the pages in the table, you must enter information or specify parameter settings.</span></span>

<span data-ttu-id="286f5-106">**ภารกิจคอมโพเนนต์กระบวนการทางธุรกิจ**</span><span class="sxs-lookup"><span data-stu-id="286f5-106">**Business process component task**</span></span>                   

<span data-ttu-id="286f5-107">ปิดรอบระยะเวลาในบัญชีแยกประเภททั่วไป</span><span class="sxs-lookup"><span data-stu-id="286f5-107">Close periods in the general ledger</span></span>

| <span data-ttu-id="286f5-108">ชื่อหน้า</span><span class="sxs-lookup"><span data-stu-id="286f5-108">Page name</span></span>                            | <span data-ttu-id="286f5-109">การใช้</span><span class="sxs-lookup"><span data-stu-id="286f5-109">Usage</span></span>                                                                                      |
|--------------------------------------|--------------------------------------------------------------------------------------------|
|<span data-ttu-id="286f5-110">ชุดงาน</span><span class="sxs-lookup"><span data-stu-id="286f5-110">Batch job</span></span>                             | <span data-ttu-id="286f5-111">ดูหรือสร้างชุดงาน</span><span class="sxs-lookup"><span data-stu-id="286f5-111">View or create batch jobs.</span></span> <span data-ttu-id="286f5-112">ชุดงานอาจไม่เสร็จสมบูรณ์ และคุณต้องตรวจสอบให้แน่ใจว่าการลงรายการบัญชีทั้งหมดเสร็จสมบูรณ์แล้ว</span><span class="sxs-lookup"><span data-stu-id="286f5-112">Batch jobs might not be completed, and you want to make sure that all posting is completed.</span></span>                                                                                                               |
|<span data-ttu-id="286f5-113">ยืนยันใบสั่งขาย</span><span class="sxs-lookup"><span data-stu-id="286f5-113">Confirm sales order</span></span>                   | <span data-ttu-id="286f5-114">อัพเดตใบสั่งขาย</span><span class="sxs-lookup"><span data-stu-id="286f5-114">Update sales orders.</span></span>                                                                       |
|<span data-ttu-id="286f5-115">การประเมินค่าใหม่ตามสกุลเงินต่างประเทศ</span><span class="sxs-lookup"><span data-stu-id="286f5-115">Foreign currency revaluation</span></span>          | <span data-ttu-id="286f5-116">สร้างธุรกรรมที่อัพเดตมูลค่าของธุรกรรมลูกค้าที่เปิดค้างไว้ในสกุลเงินต่างประเทศ</span><span class="sxs-lookup"><span data-stu-id="286f5-116">Generate transactions that update the value of open customer transactions in foreign currencies.</span></span>                                                                                                                         |
| <span data-ttu-id="286f5-117">สมุดรายวัน</span><span class="sxs-lookup"><span data-stu-id="286f5-117">Journal</span></span>                              | <span data-ttu-id="286f5-118">ลงรายการบัญชีใบแจ้งหนี้ การชำระเงิน และตั๋วสัญญาใช้เงิน</span><span class="sxs-lookup"><span data-stu-id="286f5-118">Post invoices, payments, and promissory notes.</span></span>                                             |
| <span data-ttu-id="286f5-119">ใบสำคัญสมุดรายวัน</span><span class="sxs-lookup"><span data-stu-id="286f5-119">Journal voucher</span></span>                      |<ul><li><span data-ttu-id="286f5-120">**สมุดรายวันการชำระเงิน** – สร้าง ประมวลผล และลงรายการบัญชีการชำระเงิน</span><span class="sxs-lookup"><span data-stu-id="286f5-120">**Payment journal** – Generate, process, and post payments.</span></span></li><li><span data-ttu-id="286f5-121">**สมุดรายวันการออกตั๋วแลกเงิน** – ลงรายการบัญชีตั๋วแลกเงิน</span><span class="sxs-lookup"><span data-stu-id="286f5-121">**Draw bill of exchange journal** – Post bills of exchange.</span></span></li><li><span data-ttu-id="286f5-122">**สมุดรายวันการปฏิเสธตั๋วแลกเงิน** – ลงรายการบัญชีตั๋วแลกเงินที่ปฏิเสธการจ่าย</span><span class="sxs-lookup"><span data-stu-id="286f5-122">**Protest bill of exchange journal** – Post protested bills of exchange.</span></span></li><li><span data-ttu-id="286f5-123">**สมุดรายวันการออกตั๋วแลกเงินใหม่** – ลงรายการบัญชีตั๋วแลกเงินที่ออกใหม่</span><span class="sxs-lookup"><span data-stu-id="286f5-123">**Redraw bill of exchange journal** – Post redrawn bills of exchange.</span></span></li><li><span data-ttu-id="286f5-124">**สมุดรายวันการชำระเงินผ่านธนาคาร** – ลงรายการบัญชีการชำระเงินผ่านธนาคาร</span><span class="sxs-lookup"><span data-stu-id="286f5-124">**Remittance journal** – Post remittances.</span></span></li><li><span data-ttu-id="286f5-125">**สมุดรายวันการชำระตั๋วแลกเงิน** – ลงรายการบัญชีตั๋วแลกเงินที่ชำระเงินแล้ว</span><span class="sxs-lookup"><span data-stu-id="286f5-125">**Settle bill of exchange journal** – Post settled bills of exchange</span></span></li></ul>                   |
| <span data-ttu-id="286f5-126">การลงรายการบัญชีบันทึกการจัดส่ง</span><span class="sxs-lookup"><span data-stu-id="286f5-126">Packing slip posting</span></span>                 | <span data-ttu-id="286f5-127">อัพเดตบันทึกการจัดส่งสำหรับใบสั่งขาย</span><span class="sxs-lookup"><span data-stu-id="286f5-127">Update packing slips for sales orders.</span></span>                                                     |
| <span data-ttu-id="286f5-128">ลงรายการบัญชีใบแจ้งหนี้ข้อความอิสระ</span><span class="sxs-lookup"><span data-stu-id="286f5-128">Post free text invoice</span></span>               | <span data-ttu-id="286f5-129">ลงรายการบัญชีใบแจ้งหนี้ข้อความอิสระ</span><span class="sxs-lookup"><span data-stu-id="286f5-129">Post free text invoices.</span></span>                                                                   |
| <span data-ttu-id="286f5-130">การลงรายการบัญชีใบแจ้งหนี้</span><span class="sxs-lookup"><span data-stu-id="286f5-130">Posting invoice</span></span>                      | <span data-ttu-id="286f5-131">ลงรายการบัญชีใบแจ้งหนี้สำหรับใบสั่งขาย</span><span class="sxs-lookup"><span data-stu-id="286f5-131">Post invoices for sales orders.</span></span>                                                            |
| <span data-ttu-id="286f5-132">การลงรายการบัญชีรายการเบิกสินค้า</span><span class="sxs-lookup"><span data-stu-id="286f5-132">Posting picking list</span></span>                 |<span data-ttu-id="286f5-133">อัพเดตรายการเบิกสินค้าสำหรับใบสั่งขาย</span><span class="sxs-lookup"><span data-stu-id="286f5-133">Update picking lists for sales orders.</span></span>                                                      |

<span data-ttu-id="286f5-134">**ภารกิจคอมโพเนนต์กระบวนการทางธุรกิจ**</span><span class="sxs-lookup"><span data-stu-id="286f5-134">**Business process component task**</span></span>   

<span data-ttu-id="286f5-135">การสร้างและการส่งรายการขายใน EU</span><span class="sxs-lookup"><span data-stu-id="286f5-135">Create and submit the EU sales list</span></span>

| <span data-ttu-id="286f5-136">ชื่อหน้า</span><span class="sxs-lookup"><span data-stu-id="286f5-136">Page name</span></span>                            | <span data-ttu-id="286f5-137">การใช้</span><span class="sxs-lookup"><span data-stu-id="286f5-137">Usage</span></span>                                                                                      |
|--------------------------------------|--------------------------------------------------------------------------------------------|
|<span data-ttu-id="286f5-138">รายการขายใน EU</span><span class="sxs-lookup"><span data-stu-id="286f5-138">EU sales list</span></span>                         | <span data-ttu-id="286f5-139">รายงานการขายในสหภาพยุโรป (EU) ไปยังหน่วยงานจัดเก็บภาษีสำหรับวัตถุประสงค์การรายงานภาษีมูลค่าเพิ่ม (VAT)</span><span class="sxs-lookup"><span data-stu-id="286f5-139">Report on European Union (EU) sales to the tax authority for value-added tax (VAT) declaration purposes.</span></span>                                                                                                                           |








[!INCLUDE[footer-include](../../includes/footer-banner.md)]