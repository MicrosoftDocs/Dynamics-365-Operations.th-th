---
title: การลงรายการบัญชีการขายออนไลน์และการชำระเงิน
description: 'กระบวนการนี้นำไปสู่การตั้งค่าคอนฟิกและการรันงานในชุดงานที่เกิดซ้ำ เพื่อการคำนวณใบสั่งขายและการชำระเงินสำหรับธุรกรรมของร้านค้าออนไลน์ '
author: psimolin
ms.date: 08/06/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: RetailChannelOperationsWorkspace, RetailOperatingUnitPicker, SysRecurrence
audience: Application User
ms.reviewer: josaw
ms.search.region: Global
ms.search.industry: Retail
ms.author: jashanno
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: a2e482b0fb5f2cf67e687c2b278bc5b54ad09839
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 03/31/2021
ms.locfileid: "5802682"
---
# <a name="posting-of-online-sales-and-payments"></a><span data-ttu-id="d1bd9-103">การลงรายการบัญชีการขายออนไลน์และการชำระเงิน</span><span class="sxs-lookup"><span data-stu-id="d1bd9-103">Posting of online sales and payments</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="d1bd9-104">กระบวนการนี้นำไปสู่การตั้งค่าคอนฟิกและการรันงานในชุดงานที่เกิดซ้ำ เพื่อการคำนวณใบสั่งขายและการชำระเงินสำหรับธุรกรรมของร้านค้าออนไลน์ </span><span class="sxs-lookup"><span data-stu-id="d1bd9-104">This procedure walks through configuring and running a recurrent batch job to create sales orders and payments for online store transactions.</span></span>

<span data-ttu-id="d1bd9-105">การลงรายการบัญชีการขายและการชำระเงินออนไลน์เป็นกระบวนการสองขั้นตอน</span><span class="sxs-lookup"><span data-stu-id="d1bd9-105">Posting online sales and payments is a two-stage process.</span></span>

- <span data-ttu-id="d1bd9-106">ดึงข้อมูลธุรกรรมการค้าออนไลน์ใน HQ</span><span class="sxs-lookup"><span data-stu-id="d1bd9-106">Pulling the online commerce transaction data in HQ.</span></span>
- <span data-ttu-id="d1bd9-107">การซิงโครไนส์ใบสั่งเพื่อสร้างใบสั่งขายใน HQ</span><span class="sxs-lookup"><span data-stu-id="d1bd9-107">Synchronizing orders to create sales orders in HQ.</span></span>

<span data-ttu-id="d1bd9-108">การดึงข้อมูลธุรกรรมออนไลน์สามารถทำได้โดยใช้งาน P-job ด้วยตนเองหรือสร้างชุดงานที่เกิดซ้ำ</span><span class="sxs-lookup"><span data-stu-id="d1bd9-108">Pulling the online transaction data can be done either by manually running the P-job or by creating a recurrent batch job.</span></span>

### <a name="manually-running-the-p-job"></a><span data-ttu-id="d1bd9-109">การรันงาน P ด้วยตนเอง</span><span class="sxs-lookup"><span data-stu-id="d1bd9-109">Manually running the P-job</span></span>

1. <span data-ttu-id="d1bd9-110">ไปยัง พื้นที่ทำงานทั้งหมด > การขายปลีกและไอทีเชิงพาณิชย์</span><span class="sxs-lookup"><span data-stu-id="d1bd9-110">Go to All workspaces > Retail and Commerce IT.</span></span>
2. <span data-ttu-id="d1bd9-111">คลิกกำหนดการการกระจาย</span><span class="sxs-lookup"><span data-stu-id="d1bd9-111">Click Distribution schedule.</span></span>
3. <span data-ttu-id="d1bd9-112">เลือก P-0001</span><span class="sxs-lookup"><span data-stu-id="d1bd9-112">Select P-0001.</span></span>
4. <span data-ttu-id="d1bd9-113">ปรับปรุงกลุ่มฐานข้อมูลช่องทาง ถ้าจำเป็น</span><span class="sxs-lookup"><span data-stu-id="d1bd9-113">Adjust channel database groups, if required.</span></span>
5. <span data-ttu-id="d1bd9-114">คลิก รันทันที</span><span class="sxs-lookup"><span data-stu-id="d1bd9-114">Click Run now.</span></span>
6. <span data-ttu-id="d1bd9-115">คลิก ใช่</span><span class="sxs-lookup"><span data-stu-id="d1bd9-115">Click Yes.</span></span>

### <a name="scheduling-a-recurring-p-job"></a><span data-ttu-id="d1bd9-116">การจัดกำหนดการงาน P ที่เกิดซ้ำ</span><span class="sxs-lookup"><span data-stu-id="d1bd9-116">Scheduling a recurring P-job</span></span>

1. <span data-ttu-id="d1bd9-117">ไปยัง พื้นที่ทำงานทั้งหมด > การขายปลีกและไอทีเชิงพาณิชย์</span><span class="sxs-lookup"><span data-stu-id="d1bd9-117">Go to All workspaces > Retail and Commerce IT.</span></span>
2. <span data-ttu-id="d1bd9-118">คลิกกำหนดการการกระจาย</span><span class="sxs-lookup"><span data-stu-id="d1bd9-118">Click Distribution schedule.</span></span>
3. <span data-ttu-id="d1bd9-119">เลือก P-0001</span><span class="sxs-lookup"><span data-stu-id="d1bd9-119">Select P-0001.</span></span>
4. <span data-ttu-id="d1bd9-120">คลิกสร้างชุดงาน</span><span class="sxs-lookup"><span data-stu-id="d1bd9-120">Click Create batch job.</span></span>
5. <span data-ttu-id="d1bd9-121">คลิกรันในเบื้องหลัง</span><span class="sxs-lookup"><span data-stu-id="d1bd9-121">Click Run in the background.</span></span>
5. <span data-ttu-id="d1bd9-122">เปิดใช้งานการประมวลผลชุดงาน</span><span class="sxs-lookup"><span data-stu-id="d1bd9-122">Enable Batch processing.</span></span>
6. <span data-ttu-id="d1bd9-123">คลิกการเกิดซ้ำ..</span><span class="sxs-lookup"><span data-stu-id="d1bd9-123">Click Recurrence..</span></span>
7. <span data-ttu-id="d1bd9-124">เลือกตัวเลือก ไม่มีวันที่สิ้นสุด</span><span class="sxs-lookup"><span data-stu-id="d1bd9-124">Select the No end date option.</span></span>
8. <span data-ttu-id="d1bd9-125">ในฟิลด์ตรวจนับ ให้ป้อนช่วงระหว่างการรันเป็นนาที</span><span class="sxs-lookup"><span data-stu-id="d1bd9-125">In the Count field, enter interval between the runs in minutes.</span></span> <span data-ttu-id="d1bd9-126">โดยทั่วไป จะเป็น 5-10</span><span class="sxs-lookup"><span data-stu-id="d1bd9-126">Typically this would be 5-10.</span></span>
9. <span data-ttu-id="d1bd9-127">คลิก ตกลง </span><span class="sxs-lookup"><span data-stu-id="d1bd9-127">Click OK.</span></span>
10. <span data-ttu-id="d1bd9-128">คลิก ตกลง </span><span class="sxs-lookup"><span data-stu-id="d1bd9-128">Click OK.</span></span>

<span data-ttu-id="d1bd9-129">คุณสามารถซิงโครไนส์ใบสั่งด้วยตนเองได้ด้วยการรันงาน "ซิงโครไนส์ใบสั่ง" หรือโดยการสร้างชุดงานที่เกิดซ้ำ</span><span class="sxs-lookup"><span data-stu-id="d1bd9-129">Orders can be synchronized either by manually running the "Synchronize orders"-job or by creating a recurring batch job.</span></span>

### <a name="manually-running-order-synchronization"></a><span data-ttu-id="d1bd9-130">การรันการซิงโครไนส์ใบสั่งด้วยตนเอง</span><span class="sxs-lookup"><span data-stu-id="d1bd9-130">Manually running order synchronization</span></span> 

<span data-ttu-id="d1bd9-131">ทำตามขั้นตอนต่อไปนี้เพื่อรันงาน "ซิงโครไนส์ใบสั่ง" ด้วยตนเองหนึ่งครั้ง</span><span class="sxs-lookup"><span data-stu-id="d1bd9-131">Follow these steps to manually run "Synchronize orders" job once.</span></span>

1. <span data-ttu-id="d1bd9-132">ไปยังพื้นที่ทำงานทั้งหมด > การเงินของร้านค้า</span><span class="sxs-lookup"><span data-stu-id="d1bd9-132">Go to All workspaces > Store financials.</span></span>
2. <span data-ttu-id="d1bd9-133">คลิกซิงโครไนส์ใบสั่ง</span><span class="sxs-lookup"><span data-stu-id="d1bd9-133">Click Synchronize orders.</span></span>
3. <span data-ttu-id="d1bd9-134">ในฟิลด์ลำดับชั้นองค์กร เลือก 'ร้านค้าตามภูมิภาค'</span><span class="sxs-lookup"><span data-stu-id="d1bd9-134">In the Organization hierarchy field, select 'Stores by Region'.</span></span>
    * <span data-ttu-id="d1bd9-135">เลือกอย่างใดอย่างหนึ่งระหว่างร้านค้าออนไลน์ หรือเลือกโหนด ถ้าคุณต้องการสร้างชุดงานสำหรับกลุ่มร้านค้า</span><span class="sxs-lookup"><span data-stu-id="d1bd9-135">Select either a specific online store, or select a node if you want to create the batch job for a group of stores.</span></span>  
    * <span data-ttu-id="d1bd9-136">คลิกลูกศรเพื่อเพิ่มสิ่งที่คุณเลือก </span><span class="sxs-lookup"><span data-stu-id="d1bd9-136">Click the arrow to add your selection.</span></span>  
4. <span data-ttu-id="d1bd9-137">คลิกรันในแท็บเบื้องหลัง </span><span class="sxs-lookup"><span data-stu-id="d1bd9-137">Click the Run in the background tab.</span></span>
5. <span data-ttu-id="d1bd9-138">ปิดใช้งานการประมวลผลชุดงาน</span><span class="sxs-lookup"><span data-stu-id="d1bd9-138">Disable Batch processing</span></span>
6. <span data-ttu-id="d1bd9-139">คลิกการเกิดซ้ำ</span><span class="sxs-lookup"><span data-stu-id="d1bd9-139">Click Recurrence.</span></span>
7. <span data-ttu-id="d1bd9-140">เลือกตัวเลือก สิ้นสุดหลังจาก</span><span class="sxs-lookup"><span data-stu-id="d1bd9-140">Select End After option</span></span>
8. <span data-ttu-id="d1bd9-141">ในฟิลด์ สิ้นสุดหลังจาก ป้อน 1</span><span class="sxs-lookup"><span data-stu-id="d1bd9-141">In the End After field, enter 1.</span></span>
9. <span data-ttu-id="d1bd9-142">คลิก ตกลง </span><span class="sxs-lookup"><span data-stu-id="d1bd9-142">Click OK.</span></span>
10. <span data-ttu-id="d1bd9-143">คลิก ตกลง </span><span class="sxs-lookup"><span data-stu-id="d1bd9-143">Click OK.</span></span>

### <a name="scheduling-recurring-order-synchronization"></a><span data-ttu-id="d1bd9-144">การจัดกำหนดการซิงโครไนส์ใบสั่งที่เกิดซ้ำ</span><span class="sxs-lookup"><span data-stu-id="d1bd9-144">Scheduling recurring order synchronization</span></span>

<span data-ttu-id="d1bd9-145">กระบวนการนี้นำไปสู่การตั้งค่าคอนฟิกและการรันงานในชุดงานที่เกิดซ้ำ เพื่อการคำนวณใบสั่งขายและการชำระเงินสำหรับธุรกรรมของร้านค้าออนไลน์ </span><span class="sxs-lookup"><span data-stu-id="d1bd9-145">This procedure walks through configuring and running a recurrent batch job to create sales orders and payments for online store transactions.</span></span> <span data-ttu-id="d1bd9-146">กระบวนงานนี้ใช้บริษัท USRT ในข้อมูลสาธิต</span><span class="sxs-lookup"><span data-stu-id="d1bd9-146">This procedure uses the USRT company in demo data.</span></span>

1. <span data-ttu-id="d1bd9-147">ไปยังพื้นที่ทำงานทั้งหมด > การเงินของร้านค้า</span><span class="sxs-lookup"><span data-stu-id="d1bd9-147">Go to All workspaces > Store financials.</span></span>
2. <span data-ttu-id="d1bd9-148">คลิกซิงโครไนส์ใบสั่ง</span><span class="sxs-lookup"><span data-stu-id="d1bd9-148">Click Synchronize orders.</span></span>
3. <span data-ttu-id="d1bd9-149">ในฟิลด์ลำดับชั้นองค์กร เลือก 'ร้านค้าตามภูมิภาค'</span><span class="sxs-lookup"><span data-stu-id="d1bd9-149">In the Organization hierarchy field, select 'Stores by Region'.</span></span>
    * <span data-ttu-id="d1bd9-150">เลือกอย่างใดอย่างหนึ่งระหว่างร้านค้าออนไลน์ หรือเลือกโหนด ถ้าคุณต้องการสร้างชุดงานสำหรับกลุ่มร้านค้า</span><span class="sxs-lookup"><span data-stu-id="d1bd9-150">Select either a specific online store, or select a node if you want to create the batch job for a group of stores.</span></span>  
    * <span data-ttu-id="d1bd9-151">คลิกลูกศรเพื่อเพิ่มสิ่งที่คุณเลือก </span><span class="sxs-lookup"><span data-stu-id="d1bd9-151">Click the arrow to add your selection.</span></span>  
4. <span data-ttu-id="d1bd9-152">คลิกรันในแท็บเบื้องหลัง </span><span class="sxs-lookup"><span data-stu-id="d1bd9-152">Click the Run in the background tab.</span></span>
5. <span data-ttu-id="d1bd9-153">เปิดใช้งานการประมวลผลชุดงาน</span><span class="sxs-lookup"><span data-stu-id="d1bd9-153">Enable Batch processing</span></span>
6. <span data-ttu-id="d1bd9-154">คลิกการเกิดซ้ำ</span><span class="sxs-lookup"><span data-stu-id="d1bd9-154">Click Recurrence.</span></span>
7. <span data-ttu-id="d1bd9-155">เลือกตัวเลือก ไม่มีวันที่สิ้นสุด</span><span class="sxs-lookup"><span data-stu-id="d1bd9-155">Select the No end date option.</span></span>
8. <span data-ttu-id="d1bd9-156">ในฟิลด์ตรวจนับ ให้ป้อนช่วงระหว่างการรันเป็นนาที</span><span class="sxs-lookup"><span data-stu-id="d1bd9-156">In the Count field, enter interval between the runs in minutes.</span></span> <span data-ttu-id="d1bd9-157">โดยทั่วไป จะเป็น 2-20</span><span class="sxs-lookup"><span data-stu-id="d1bd9-157">Typically this would be 2-20</span></span>
9. <span data-ttu-id="d1bd9-158">คลิก ตกลง </span><span class="sxs-lookup"><span data-stu-id="d1bd9-158">Click OK.</span></span>
10. <span data-ttu-id="d1bd9-159">คลิก ตกลง </span><span class="sxs-lookup"><span data-stu-id="d1bd9-159">Click OK.</span></span>

## <a name="data-entities-involved-in-the-process"></a><span data-ttu-id="d1bd9-160">เอนทิตีข้อมูลที่เกี่ยวข้องในกระบวนการ</span><span class="sxs-lookup"><span data-stu-id="d1bd9-160">Data entities involved in the process</span></span>

- <span data-ttu-id="d1bd9-161">RetailTransactionTable</span><span class="sxs-lookup"><span data-stu-id="d1bd9-161">RetailTransactionTable</span></span>
- <span data-ttu-id="d1bd9-162">RetailTransactionAddressTrans</span><span class="sxs-lookup"><span data-stu-id="d1bd9-162">RetailTransactionAddressTrans</span></span>
- <span data-ttu-id="d1bd9-163">RetailTransactionInfocodeTrans</span><span class="sxs-lookup"><span data-stu-id="d1bd9-163">RetailTransactionInfocodeTrans</span></span>
- <span data-ttu-id="d1bd9-164">RetailTransactionTaxTrans</span><span class="sxs-lookup"><span data-stu-id="d1bd9-164">RetailTransactionTaxTrans</span></span>
- <span data-ttu-id="d1bd9-165">RetailTransactionSalesTrans</span><span class="sxs-lookup"><span data-stu-id="d1bd9-165">RetailTransactionSalesTrans</span></span>
- <span data-ttu-id="d1bd9-166">RetailTransactionTaxMeasure</span><span class="sxs-lookup"><span data-stu-id="d1bd9-166">RetailTransactionTaxMeasure</span></span>
- <span data-ttu-id="d1bd9-167">RetailTransactionDiscountTrans</span><span class="sxs-lookup"><span data-stu-id="d1bd9-167">RetailTransactionDiscountTrans</span></span>
- <span data-ttu-id="d1bd9-168">RetailTransactionTaxTransGTE</span><span class="sxs-lookup"><span data-stu-id="d1bd9-168">RetailTransactionTaxTransGTE</span></span>
- <span data-ttu-id="d1bd9-169">RetailTransactionMarkupTrans</span><span class="sxs-lookup"><span data-stu-id="d1bd9-169">RetailTransactionMarkupTrans</span></span>
- <span data-ttu-id="d1bd9-170">RetailTransactionPaymentTrans</span><span class="sxs-lookup"><span data-stu-id="d1bd9-170">RetailTransactionPaymentTrans</span></span>
- <span data-ttu-id="d1bd9-171">RetailTransactionAttributeTrans</span><span class="sxs-lookup"><span data-stu-id="d1bd9-171">RetailTransactionAttributeTrans</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]