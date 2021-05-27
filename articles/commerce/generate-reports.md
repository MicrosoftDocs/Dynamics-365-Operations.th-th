---
title: สร้างรายงานช่องทางออนไลน์
description: หัวข้อนี้จะอธิบายวิธีการสร้างรายงานสำหรับช่องทางออนไลน์ของคุณใน Microsoft Dynamics 365 Commerce
author: psimolin
ms.date: 10/01/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: samjar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 80d62b29fcc95a3153c604512e1ee6b3e55ba840
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 05/11/2021
ms.locfileid: "6019798"
---
# <a name="generate-online-channel-reports"></a><span data-ttu-id="cb0a1-103">สร้างรายงานช่องทางออนไลน์</span><span class="sxs-lookup"><span data-stu-id="cb0a1-103">Generate online channel reports</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="cb0a1-104">หัวข้อนี้จะอธิบายวิธีการสร้างรายงานสำหรับช่องทางออนไลน์ของคุณใน Microsoft Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="cb0a1-104">This topic describes how to generate reports for your online channel in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="cb0a1-105">คุณสามารถสร้างและดูรายงานต่างๆใน Commerce เพื่อดูว่าช่องทางออนไลน์ของคุณกำลังดำเนินการเป็นอย่างไร</span><span class="sxs-lookup"><span data-stu-id="cb0a1-105">You can generate and view several reports in Commerce to see how your online channel is performing.</span></span>

## <a name="channel-summary-report"></a><span data-ttu-id="cb0a1-106">รายงานสรุปช่องทาง</span><span class="sxs-lookup"><span data-stu-id="cb0a1-106">Channel summary report</span></span>

<span data-ttu-id="cb0a1-107">รายงาน **สรุปช่องทาง** แสดงสรุปของธุรกรรมต่อไปนี้สำหรับช่องทางที่เลือกดังนี้</span><span class="sxs-lookup"><span data-stu-id="cb0a1-107">The **Channel summary** report shows a summary of the following transactions for the selected channel:</span></span>

- <span data-ttu-id="cb0a1-108">ธุรกรรมการขาย</span><span class="sxs-lookup"><span data-stu-id="cb0a1-108">Sales transactions</span></span>
- <span data-ttu-id="cb0a1-109">ธุรกรรมการชำระเงิน</span><span class="sxs-lookup"><span data-stu-id="cb0a1-109">Payment transactions</span></span>
- <span data-ttu-id="cb0a1-110">ธุรกรรมภาษี</span><span class="sxs-lookup"><span data-stu-id="cb0a1-110">Tax transactions</span></span>
- <span data-ttu-id="cb0a1-111">ธุรกรรมที่ลดราคา</span><span class="sxs-lookup"><span data-stu-id="cb0a1-111">Discounted transactions</span></span>

<span data-ttu-id="cb0a1-112">หากต้องการสร้างรายงาน **สรุปช่องทาง** ให้ดำเนินการตามขั้นตอนต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="cb0a1-112">To generate a **Channel summary** report, follow these steps.</span></span>

1. <span data-ttu-id="cb0a1-113">ไปที่ **Retail และ Commerce \> การสอบถามและรายงาน \> รายงานการขาย \> รายงานสรุปช่องทาง**</span><span class="sxs-lookup"><span data-stu-id="cb0a1-113">Go to **Retail and Commerce \> Inquiries and reports \> Sales reports \> Channel summary report**.</span></span>
1. <span data-ttu-id="cb0a1-114">ในฟิลด์ **วันที่เริ่มต้น** ให้ป้อนวันที่</span><span class="sxs-lookup"><span data-stu-id="cb0a1-114">In the **From date** field, enter a date.</span></span>
1. <span data-ttu-id="cb0a1-115">ในฟิลด์ **วันที่สิ้นสุด** ให้ป้อนวันที่</span><span class="sxs-lookup"><span data-stu-id="cb0a1-115">In the **To date** field, enter a date.</span></span>
1. <span data-ttu-id="cb0a1-116">ในฟิลด์ **ช่องทาง** ให้เลือกช่องทางออนไลน์</span><span class="sxs-lookup"><span data-stu-id="cb0a1-116">In the **Channel** field, select the online channel.</span></span>
1. <span data-ttu-id="cb0a1-117">เลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="cb0a1-117">Select **OK**.</span></span>
 
## <a name="channel-sales-by-year-report"></a><span data-ttu-id="cb0a1-118">รายงานการขายผ่านช่องทางตามปี</span><span class="sxs-lookup"><span data-stu-id="cb0a1-118">Channel sales by year report</span></span> 

<span data-ttu-id="cb0a1-119">รายงาน **ช่องทางการขายรายปี** แสดงการเปรียบเทียบยอดขายปีต่อปี สำหรับร้านค้าเฉพาะ</span><span class="sxs-lookup"><span data-stu-id="cb0a1-119">The **Channel sales by year** report shows a comparison of year-over-year sales for a specific store.</span></span> <span data-ttu-id="cb0a1-120">คุณเลือกปีที่ต้องการเปรียบเทียบยอดขายด้วย และรายงานจะเปรียบเทียบการขายสำหรับปีที่เลือกกับการขายสำหรับปีก่อนหน้านี้</span><span class="sxs-lookup"><span data-stu-id="cb0a1-120">You select the year to compare the sales against, and the report compares sales for the selected year with sales for the previous year.</span></span>

<span data-ttu-id="cb0a1-121">หากต้องการสร้างรายงาน **ช่องทางการขายรายปี** ให้ดำเนินการตามขั้นตอนต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="cb0a1-121">To generate a **Channel sales by year** report, follow these steps.</span></span>

1. <span data-ttu-id="cb0a1-122">ไปที่ **Retail และ Commerce \> การสอบถามและรายงาน \> รายงานการขาย \> รายงานสรุปช่องทาง**</span><span class="sxs-lookup"><span data-stu-id="cb0a1-122">Go to **Retail and Commerce \> Inquiries and reports \> Sales reports \> Channel sales by year report**.</span></span>
1. <span data-ttu-id="cb0a1-123">ในฟิลด์ **ปีปฏิทินเริ่มต้น** ให้ระบุปี</span><span class="sxs-lookup"><span data-stu-id="cb0a1-123">In the **From calendar year** field, enter a year.</span></span>
1. <span data-ttu-id="cb0a1-124">ในฟิลด์ **ปีปฏิทินสิ้นสุด** ให้ระบุปี</span><span class="sxs-lookup"><span data-stu-id="cb0a1-124">In the **To calendar year** field, enter a year.</span></span>
1. <span data-ttu-id="cb0a1-125">ในฟิลด์ **ช่องทาง** ให้เลือกช่องทางออนไลน์</span><span class="sxs-lookup"><span data-stu-id="cb0a1-125">In the **Channel** field, select the online channel.</span></span>
1. <span data-ttu-id="cb0a1-126">เลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="cb0a1-126">Select **OK**.</span></span>

## <a name="channel-sales-by-hour-report"></a><span data-ttu-id="cb0a1-127">รายงานการขายผ่านช่องทางตามชั่วโมง</span><span class="sxs-lookup"><span data-stu-id="cb0a1-127">Channel sales by hour report</span></span>

<span data-ttu-id="cb0a1-128">รายงาน **ช่องทางการขายรายชั่วโมง** แสดงเมตริกการขายต่อชั่วโมงสำหรับช่องทางหรือหน่วยปฏิบัติงานที่เลือก</span><span class="sxs-lookup"><span data-stu-id="cb0a1-128">The **Channel sales by hour** report shows sales metrics per hour for a selected channel or operating unit.</span></span>

<span data-ttu-id="cb0a1-129">หากต้องการสร้างรายงาน **ช่องทางการขายรายชั่วโมง** ให้ดำเนินการตามขั้นตอนต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="cb0a1-129">To generate a **Channel sales by hour** report, follow these steps.</span></span>

1. <span data-ttu-id="cb0a1-130">ไปที่ **Retail และ Commerce \> การสอบถามและรายงาน \> รายงานการขาย \> รายงานช่องทางการขายตามชั่วโมง**</span><span class="sxs-lookup"><span data-stu-id="cb0a1-130">Go to **Retail and Commerce \> Inquiries and reports \> Sales reports \> Channel sales by hour report**.</span></span>
1. <span data-ttu-id="cb0a1-131">ในฟิลด์ **วันที่เริ่มต้น** ให้ป้อนวันที่</span><span class="sxs-lookup"><span data-stu-id="cb0a1-131">In the **From date** field, enter a date.</span></span>
1. <span data-ttu-id="cb0a1-132">ในฟิลด์ **วันที่สิ้นสุด** ให้ป้อนวันที่</span><span class="sxs-lookup"><span data-stu-id="cb0a1-132">In the **To date** field, enter a date.</span></span>
1. <span data-ttu-id="cb0a1-133">ในฟิลด์ **ช่องทาง** ให้เลือกช่องทางออนไลน์</span><span class="sxs-lookup"><span data-stu-id="cb0a1-133">In the **Channel** field, select the online channel.</span></span>
1. <span data-ttu-id="cb0a1-134">เลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="cb0a1-134">Select **OK**.</span></span>

## <a name="top-customers-report"></a><span data-ttu-id="cb0a1-135">รายงานลูกค้าอันดับแรก</span><span class="sxs-lookup"><span data-stu-id="cb0a1-135">Top customers report</span></span>

<span data-ttu-id="cb0a1-136">รายงาน **ลูกค้าอันดับแรก** แสดงเมตริกการขายสำหรับลูกค้า *N* รายแรกสำหรับช่องทางหรือหน่วยปฏิบัติงานที่เลือก</span><span class="sxs-lookup"><span data-stu-id="cb0a1-136">The **Top customers** report shows sales metrics for the top *N* customers for a selected channel or operating unit.</span></span> <span data-ttu-id="cb0a1-137">ค่า *N* คือตัวเลขตั้งแต่ 10 ถึง 100 และขึ้นอยู่กับการวัดโดยรวมที่ผู้ใช้เลือก</span><span class="sxs-lookup"><span data-stu-id="cb0a1-137">The value *N* is a number from 10 to 100 and is based on a user-selected aggregate measure.</span></span>

<span data-ttu-id="cb0a1-138">หากต้องการสร้างรายงาน **ลูกค้าอันดับแรก** ให้ดำเนินการตามขั้นตอนต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="cb0a1-138">To generate a **Top customers** report, follow these steps.</span></span>

1. <span data-ttu-id="cb0a1-139">ไปที่ **Retail และ Commerce \> การสอบถามและรายงาน \> รายงานการขาย \> รายงานลูกค้าอันดับแรก**</span><span class="sxs-lookup"><span data-stu-id="cb0a1-139">Go to **Retail and Commerce \> Inquiries and reports \> Sales reports \> Top customers report**.</span></span>
1. <span data-ttu-id="cb0a1-140">ในฟิลด์ **วันที่เริ่มต้น** ให้ป้อนวันที่</span><span class="sxs-lookup"><span data-stu-id="cb0a1-140">In the **From date** field, enter a date.</span></span>
1. <span data-ttu-id="cb0a1-141">ในฟิลด์ **วันที่สิ้นสุด** ให้ป้อนวันที่</span><span class="sxs-lookup"><span data-stu-id="cb0a1-141">In the **To date** field, enter a date.</span></span>
1. <span data-ttu-id="cb0a1-142">ในฟิลด์ **ช่องทาง** ให้เลือกช่องทางออนไลน์</span><span class="sxs-lookup"><span data-stu-id="cb0a1-142">In the **Channel** field, select the online channel.</span></span>
1. <span data-ttu-id="cb0a1-143">เลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="cb0a1-143">Select **OK**.</span></span>

## <a name="top-discounts-report"></a><span data-ttu-id="cb0a1-144">รายงานส่วนลดอันดับแรก</span><span class="sxs-lookup"><span data-stu-id="cb0a1-144">Top discounts report</span></span>

<span data-ttu-id="cb0a1-145">รายงาน **ส่วนลดอันดับแรก** แสดงเมตริกการขายสำหรับส่วนลด *N* ส่วนลดแรกสำหรับช่องทางหรือหน่วยปฏิบัติงานที่เลือก</span><span class="sxs-lookup"><span data-stu-id="cb0a1-145">The **Top discounts** report shows sales metrics for the top *N* discounts for a selected channel or operating unit.</span></span> <span data-ttu-id="cb0a1-146">ค่า *N* คือตัวเลขตั้งแต่ 10 ถึง 100 และขึ้นอยู่กับการวัดโดยรวมที่ผู้ใช้เลือก</span><span class="sxs-lookup"><span data-stu-id="cb0a1-146">The value *N* is a number from 10 to 100 and is based on a user-selected aggregate measure.</span></span>

<span data-ttu-id="cb0a1-147">หากต้องการสร้างรายงาน **ส่วนลดอันดับแรก** ให้ดำเนินการตามขั้นตอนต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="cb0a1-147">To generate a **Top discounts** report, follow these steps.</span></span>

1. <span data-ttu-id="cb0a1-148">ไปที่ **Retail และ Commerce \> การสอบถามและรายงาน \> รายงานการขาย \> รายงานส่วนลดอันดับแรก**</span><span class="sxs-lookup"><span data-stu-id="cb0a1-148">Go to **Retail and Commerce \> Inquiries and reports \> Sales reports \> Top discounts report**.</span></span>
1. <span data-ttu-id="cb0a1-149">ในฟิลด์ **วันที่เริ่มต้น** ให้ป้อนวันที่</span><span class="sxs-lookup"><span data-stu-id="cb0a1-149">In the **From date** field, enter a date.</span></span>
1. <span data-ttu-id="cb0a1-150">ในฟิลด์ **วันที่สิ้นสุด** ให้ป้อนวันที่</span><span class="sxs-lookup"><span data-stu-id="cb0a1-150">In the **To date** field, enter a date.</span></span>
1. <span data-ttu-id="cb0a1-151">ในฟิลด์ **ช่องทาง** ให้เลือกช่องทางออนไลน์</span><span class="sxs-lookup"><span data-stu-id="cb0a1-151">In the **Channel** field, select the online channel.</span></span>
1. <span data-ttu-id="cb0a1-152">เลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="cb0a1-152">Select **OK**.</span></span>

## <a name="top-products-report"></a><span data-ttu-id="cb0a1-153">รายงานผลิตภัณฑ์อันดับแรก</span><span class="sxs-lookup"><span data-stu-id="cb0a1-153">Top products report</span></span>

<span data-ttu-id="cb0a1-154">รายงาน **ผลิตภัณฑ์อันดับแรก** แสดงเมตริกการขายสำหรับผลิตภัณฑ์ *N* ผลิตภัณฑ์แรกสำหรับช่องทางหรือหน่วยปฏิบัติงานที่เลือก</span><span class="sxs-lookup"><span data-stu-id="cb0a1-154">The **Top products** report shows sales metrics for the top *N* products for a selected channel or operating unit.</span></span> <span data-ttu-id="cb0a1-155">ค่า *N* คือตัวเลขตั้งแต่ 10 ถึง 100 และขึ้นอยู่กับการวัดโดยรวมที่ผู้ใช้เลือก</span><span class="sxs-lookup"><span data-stu-id="cb0a1-155">The value *N* is a number from 10 to 100 and is based on a user-selected aggregate measure.</span></span>

<span data-ttu-id="cb0a1-156">หากต้องการสร้างรายงาน **ผลิตภัณฑ์อันดับแรก** ให้ดำเนินการตามขั้นตอนต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="cb0a1-156">To generate a **Top products** report, follow these steps.</span></span>

1. <span data-ttu-id="cb0a1-157">ไปที่ **Retail และ Commerce \> การสอบถามและรายงาน \> รายงานการขาย \> รายงานผลิตภัณฑ์อันดับแรก**</span><span class="sxs-lookup"><span data-stu-id="cb0a1-157">Go to **Retail and Commerce \> Inquiries and reports \> Sales reports \> Top products report**.</span></span>
1. <span data-ttu-id="cb0a1-158">ในฟิลด์ **วันที่เริ่มต้น** ให้ป้อนวันที่</span><span class="sxs-lookup"><span data-stu-id="cb0a1-158">In the **From date** field, enter a date.</span></span>
1. <span data-ttu-id="cb0a1-159">ในฟิลด์ **วันที่สิ้นสุด** ให้ป้อนวันที่</span><span class="sxs-lookup"><span data-stu-id="cb0a1-159">In the **To date** field, enter a date.</span></span>
1. <span data-ttu-id="cb0a1-160">ในฟิลด์ **ช่องทาง** ให้เลือกช่องทางออนไลน์</span><span class="sxs-lookup"><span data-stu-id="cb0a1-160">In the **Channel** field, select the online channel.</span></span>
1. <span data-ttu-id="cb0a1-161">เลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="cb0a1-161">Select **OK**.</span></span>

## <a name="category-sales-report"></a><span data-ttu-id="cb0a1-162">รายงานการขายตามประเภท</span><span class="sxs-lookup"><span data-stu-id="cb0a1-162">Category sales report</span></span>

<span data-ttu-id="cb0a1-163">รายงาน **การขายตามประเภท** แสดงการวัดยอดขายในรอบระยะเวลาที่เลือก สำหรับแต่ละโหนดของการจัดประเภทตามลำดับชั้น สำหรับช่องทางหรือหน่วยปฏิบัติงานที่เลือก</span><span class="sxs-lookup"><span data-stu-id="cb0a1-163">The **Category sales** report shows sales metrics over a selected period for each node of a category hierarchy for a selected channel or operating unit.</span></span>

<span data-ttu-id="cb0a1-164">หากต้องการสร้างรายงาน **การขายตามประเภท** ให้ดำเนินการตามขั้นตอนต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="cb0a1-164">To generate a **Category sales** report, follow these steps.</span></span>

1. <span data-ttu-id="cb0a1-165">ไปที่ **Retail และ Commerce \> การสอบถามและรายงาน \> รายงานการขาย \> รายงานการขายตามประเภท**</span><span class="sxs-lookup"><span data-stu-id="cb0a1-165">Go to **Retail and Commerce \> Inquiries and reports \> Sales reports \> Category sales report**.</span></span>
1. <span data-ttu-id="cb0a1-166">ในฟิลด์ **วันที่เริ่มต้น** ให้ป้อนวันที่</span><span class="sxs-lookup"><span data-stu-id="cb0a1-166">In the **From date** field, enter a date.</span></span>
1. <span data-ttu-id="cb0a1-167">ในฟิลด์ **วันที่สิ้นสุด** ให้ป้อนวันที่</span><span class="sxs-lookup"><span data-stu-id="cb0a1-167">In the **To date** field, enter a date.</span></span>
1. <span data-ttu-id="cb0a1-168">ในฟิลด์ **ช่องทาง** ให้เลือกช่องทางออนไลน์</span><span class="sxs-lookup"><span data-stu-id="cb0a1-168">In the **Channel** field, select the online channel.</span></span>
1. <span data-ttu-id="cb0a1-169">เลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="cb0a1-169">Select **OK**.</span></span>

## <a name="organization-sales-report"></a><span data-ttu-id="cb0a1-170">รายงานยอดขายขององค์กร</span><span class="sxs-lookup"><span data-stu-id="cb0a1-170">Organization sales report</span></span>

<span data-ttu-id="cb0a1-171">รายงาน **การขายขององค์กร** จะแสดงประสิทธิภาพร้านค้าของคุณตามหน่วยองค์กร</span><span class="sxs-lookup"><span data-stu-id="cb0a1-171">The **Organization sales** report shows the performance of your stores by organization unit.</span></span> <span data-ttu-id="cb0a1-172">รายงานนี้รวมถึงปริมาณการขายและยอดเงินตามร้านค้าและกำไรขั้นต้นสำหรับร้านค้าแต่ละร้าน</span><span class="sxs-lookup"><span data-stu-id="cb0a1-172">This report includes the sales quantity and amount by store, and the profit margin for each store.</span></span> <span data-ttu-id="cb0a1-173">หน่วยงานจะขึ้นอยู่กับลำดับชั้นการรายงานเริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="cb0a1-173">The organization unit is based on the default reporting hierarchy.</span></span>

<span data-ttu-id="cb0a1-174">หากต้องการสร้างรายงาน **ยอดขายขององค์กร** ให้ดำเนินการตามขั้นตอนต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="cb0a1-174">To generate an **Organization sales** report, follow these steps.</span></span>

1. <span data-ttu-id="cb0a1-175">ไปที่ **Retail และ Commerce \> การสอบถามและรายงาน \> รายงานการขาย \> รายงานยอดขายขององค์กร**</span><span class="sxs-lookup"><span data-stu-id="cb0a1-175">Go to **Retail and Commerce \> Inquiries and reports \> Sales reports \> Organization sales report**.</span></span>
1. <span data-ttu-id="cb0a1-176">ในฟิลด์ **วันที่เริ่มต้น** ให้ป้อนวันที่</span><span class="sxs-lookup"><span data-stu-id="cb0a1-176">In the **From date** field, enter a date.</span></span>
1. <span data-ttu-id="cb0a1-177">ในฟิลด์ **วันที่สิ้นสุด** ให้ป้อนวันที่</span><span class="sxs-lookup"><span data-stu-id="cb0a1-177">In the **To date** field, enter a date.</span></span>
1. <span data-ttu-id="cb0a1-178">เลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="cb0a1-178">Select **OK**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="cb0a1-179">แหล่งข้อมูลเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="cb0a1-179">Additional resources</span></span>

- [<span data-ttu-id="cb0a1-180">โฮมเพจการค้า</span><span class="sxs-lookup"><span data-stu-id="cb0a1-180">Commerce home page</span></span>](./index.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]