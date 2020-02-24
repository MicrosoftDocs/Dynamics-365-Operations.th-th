---
title: สร้างรายงานช่องทางออนไลน์
description: หัวข้อนี้จะอธิบายวิธีการสร้างรายงานสำหรับช่องทางออนไลน์ของคุณใน Microsoft Dynamics 365 Commerce
author: psimolin
manager: annbe
ms.date: 10/01/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: samjar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: fd40aabdf40e0f2bb257b914326df5595a0e6945
ms.sourcegitcommit: 81a647904dd305c4be2e4b683689f128548a872d
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 02/01/2020
ms.locfileid: "3003015"
---
# <a name="generate-online-channel-reports"></a><span data-ttu-id="ba267-103">สร้างรายงานช่องทางออนไลน์</span><span class="sxs-lookup"><span data-stu-id="ba267-103">Generate online channel reports</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="ba267-104">หัวข้อนี้จะอธิบายวิธีการสร้างรายงานสำหรับช่องทางออนไลน์ของคุณใน Microsoft Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="ba267-104">This topic describes how to generate reports for your online channel in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="ba267-105">ภาพรวม</span><span class="sxs-lookup"><span data-stu-id="ba267-105">Overview</span></span>

<span data-ttu-id="ba267-106">คุณสามารถสร้างและดูรายงานต่างๆใน Commerce เพื่อดูว่าช่องทางออนไลน์ของคุณกำลังดำเนินการเป็นอย่างไร</span><span class="sxs-lookup"><span data-stu-id="ba267-106">You can generate and view several reports in Commerce to see how your online channel is performing.</span></span>

## <a name="channel-summary-report"></a><span data-ttu-id="ba267-107">รายงานสรุปช่องทาง</span><span class="sxs-lookup"><span data-stu-id="ba267-107">Channel summary report</span></span>

<span data-ttu-id="ba267-108">รายงาน **สรุปช่องทาง** แสดงสรุปของธุรกรรมต่อไปนี้สำหรับช่องทางที่เลือกดังนี้</span><span class="sxs-lookup"><span data-stu-id="ba267-108">The **Channel summary** report shows a summary of the following transactions for the selected channel:</span></span>

- <span data-ttu-id="ba267-109">ธุรกรรมการขาย</span><span class="sxs-lookup"><span data-stu-id="ba267-109">Sales transactions</span></span>
- <span data-ttu-id="ba267-110">ธุรกรรมการชำระเงิน</span><span class="sxs-lookup"><span data-stu-id="ba267-110">Payment transactions</span></span>
- <span data-ttu-id="ba267-111">ธุรกรรมภาษี</span><span class="sxs-lookup"><span data-stu-id="ba267-111">Tax transactions</span></span>
- <span data-ttu-id="ba267-112">ธุรกรรมที่ลดราคา</span><span class="sxs-lookup"><span data-stu-id="ba267-112">Discounted transactions</span></span>

<span data-ttu-id="ba267-113">หากต้องการสร้างรายงาน **สรุปช่องทาง** ให้ดำเนินการตามขั้นตอนต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="ba267-113">To generate a **Channel summary** report, follow these steps.</span></span>

1. <span data-ttu-id="ba267-114">ไปที่ **Retail และ Commerce \> การสอบถามและรายงาน \> รายงานการขาย \> รายงานสรุปช่องทาง**</span><span class="sxs-lookup"><span data-stu-id="ba267-114">Go to **Retail and Commerce \> Inquiries and reports \> Sales reports \> Channel summary report**.</span></span>
1. <span data-ttu-id="ba267-115">ในฟิลด์ **วันที่เริ่มต้น** ให้ป้อนวันที่</span><span class="sxs-lookup"><span data-stu-id="ba267-115">In the **From date** field, enter a date.</span></span>
1. <span data-ttu-id="ba267-116">ในฟิลด์ **วันที่สิ้นสุด** ให้ป้อนวันที่</span><span class="sxs-lookup"><span data-stu-id="ba267-116">In the **To date** field, enter a date.</span></span>
1. <span data-ttu-id="ba267-117">ในฟิลด์ **ช่องทาง** ให้เลือกช่องทางออนไลน์</span><span class="sxs-lookup"><span data-stu-id="ba267-117">In the **Channel** field, select the online channel.</span></span>
1. <span data-ttu-id="ba267-118">เลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="ba267-118">Select **OK**.</span></span>
 
## <a name="channel-sales-by-year-report"></a><span data-ttu-id="ba267-119">รายงานการขายผ่านช่องทางตามปี</span><span class="sxs-lookup"><span data-stu-id="ba267-119">Channel sales by year report</span></span> 

<span data-ttu-id="ba267-120">รายงาน **ช่องทางการขายรายปี** แสดงการเปรียบเทียบยอดขายปีต่อปี สำหรับร้านค้าเฉพาะ</span><span class="sxs-lookup"><span data-stu-id="ba267-120">The **Channel sales by year** report shows a comparison of year-over-year sales for a specific store.</span></span> <span data-ttu-id="ba267-121">คุณเลือกปีที่ต้องการเปรียบเทียบยอดขายด้วย และรายงานจะเปรียบเทียบการขายสำหรับปีที่เลือกกับการขายสำหรับปีก่อนหน้านี้</span><span class="sxs-lookup"><span data-stu-id="ba267-121">You select the year to compare the sales against, and the report compares sales for the selected year with sales for the previous year.</span></span>

<span data-ttu-id="ba267-122">หากต้องการสร้างรายงาน **ช่องทางการขายรายปี** ให้ดำเนินการตามขั้นตอนต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="ba267-122">To generate a **Channel sales by year** report, follow these steps.</span></span>

1. <span data-ttu-id="ba267-123">ไปที่ **Retail และ Commerce \> การสอบถามและรายงาน \> รายงานการขาย \> รายงานสรุปช่องทาง**</span><span class="sxs-lookup"><span data-stu-id="ba267-123">Go to **Retail and Commerce \> Inquiries and reports \> Sales reports \> Channel sales by year report**.</span></span>
1. <span data-ttu-id="ba267-124">ในฟิลด์ **ปีปฏิทินเริ่มต้น** ให้ระบุปี</span><span class="sxs-lookup"><span data-stu-id="ba267-124">In the **From calendar year** field, enter a year.</span></span>
1. <span data-ttu-id="ba267-125">ในฟิลด์ **ปีปฏิทินสิ้นสุด** ให้ระบุปี</span><span class="sxs-lookup"><span data-stu-id="ba267-125">In the **To calendar year** field, enter a year.</span></span>
1. <span data-ttu-id="ba267-126">ในฟิลด์ **ช่องทาง** ให้เลือกช่องทางออนไลน์</span><span class="sxs-lookup"><span data-stu-id="ba267-126">In the **Channel** field, select the online channel.</span></span>
1. <span data-ttu-id="ba267-127">เลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="ba267-127">Select **OK**.</span></span>

## <a name="channel-sales-by-hour-report"></a><span data-ttu-id="ba267-128">รายงานการขายผ่านช่องทางตามชั่วโมง</span><span class="sxs-lookup"><span data-stu-id="ba267-128">Channel sales by hour report</span></span>

<span data-ttu-id="ba267-129">รายงาน **ช่องทางการขายรายชั่วโมง** แสดงเมตริกการขายต่อชั่วโมงสำหรับช่องทางหรือหน่วยปฏิบัติงานที่เลือก</span><span class="sxs-lookup"><span data-stu-id="ba267-129">The **Channel sales by hour** report shows sales metrics per hour for a selected channel or operating unit.</span></span>

<span data-ttu-id="ba267-130">หากต้องการสร้างรายงาน **ช่องทางการขายรายชั่วโมง** ให้ดำเนินการตามขั้นตอนต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="ba267-130">To generate a **Channel sales by hour** report, follow these steps.</span></span>

1. <span data-ttu-id="ba267-131">ไปที่ **Retail และ Commerce \> การสอบถามและรายงาน \> รายงานการขาย \> รายงานช่องทางการขายตามชั่วโมง**</span><span class="sxs-lookup"><span data-stu-id="ba267-131">Go to **Retail and Commerce \> Inquiries and reports \> Sales reports \> Channel sales by hour report**.</span></span>
1. <span data-ttu-id="ba267-132">ในฟิลด์ **วันที่เริ่มต้น** ให้ป้อนวันที่</span><span class="sxs-lookup"><span data-stu-id="ba267-132">In the **From date** field, enter a date.</span></span>
1. <span data-ttu-id="ba267-133">ในฟิลด์ **วันที่สิ้นสุด** ให้ป้อนวันที่</span><span class="sxs-lookup"><span data-stu-id="ba267-133">In the **To date** field, enter a date.</span></span>
1. <span data-ttu-id="ba267-134">ในฟิลด์ **ช่องทาง** ให้เลือกช่องทางออนไลน์</span><span class="sxs-lookup"><span data-stu-id="ba267-134">In the **Channel** field, select the online channel.</span></span>
1. <span data-ttu-id="ba267-135">เลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="ba267-135">Select **OK**.</span></span>

## <a name="top-customers-report"></a><span data-ttu-id="ba267-136">รายงานลูกค้าอันดับแรก</span><span class="sxs-lookup"><span data-stu-id="ba267-136">Top customers report</span></span>

<span data-ttu-id="ba267-137">รายงาน **ลูกค้าอันดับแรก** แสดงเมตริกการขายสำหรับลูกค้า *N* รายแรกสำหรับช่องทางหรือหน่วยปฏิบัติงานที่เลือก</span><span class="sxs-lookup"><span data-stu-id="ba267-137">The **Top customers** report shows sales metrics for the top *N* customers for a selected channel or operating unit.</span></span> <span data-ttu-id="ba267-138">ค่า *N* คือตัวเลขตั้งแต่ 10 ถึง 100 และขึ้นอยู่กับการวัดโดยรวมที่ผู้ใช้เลือก</span><span class="sxs-lookup"><span data-stu-id="ba267-138">The value *N* is a number from 10 to 100 and is based on a user-selected aggregate measure.</span></span>

<span data-ttu-id="ba267-139">หากต้องการสร้างรายงาน **ลูกค้าอันดับแรก** ให้ดำเนินการตามขั้นตอนต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="ba267-139">To generate a **Top customers** report, follow these steps.</span></span>

1. <span data-ttu-id="ba267-140">ไปที่ **Retail และ Commerce \> การสอบถามและรายงาน \> รายงานการขาย \> รายงานลูกค้าอันดับแรก**</span><span class="sxs-lookup"><span data-stu-id="ba267-140">Go to **Retail and Commerce \> Inquiries and reports \> Sales reports \> Top customers report**.</span></span>
1. <span data-ttu-id="ba267-141">ในฟิลด์ **วันที่เริ่มต้น** ให้ป้อนวันที่</span><span class="sxs-lookup"><span data-stu-id="ba267-141">In the **From date** field, enter a date.</span></span>
1. <span data-ttu-id="ba267-142">ในฟิลด์ **วันที่สิ้นสุด** ให้ป้อนวันที่</span><span class="sxs-lookup"><span data-stu-id="ba267-142">In the **To date** field, enter a date.</span></span>
1. <span data-ttu-id="ba267-143">ในฟิลด์ **ช่องทาง** ให้เลือกช่องทางออนไลน์</span><span class="sxs-lookup"><span data-stu-id="ba267-143">In the **Channel** field, select the online channel.</span></span>
1. <span data-ttu-id="ba267-144">เลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="ba267-144">Select **OK**.</span></span>

## <a name="top-discounts-report"></a><span data-ttu-id="ba267-145">รายงานส่วนลดอันดับแรก</span><span class="sxs-lookup"><span data-stu-id="ba267-145">Top discounts report</span></span>

<span data-ttu-id="ba267-146">รายงาน **ส่วนลดอันดับแรก** แสดงเมตริกการขายสำหรับส่วนลด *N* ส่วนลดแรกสำหรับช่องทางหรือหน่วยปฏิบัติงานที่เลือก</span><span class="sxs-lookup"><span data-stu-id="ba267-146">The **Top discounts** report shows sales metrics for the top *N* discounts for a selected channel or operating unit.</span></span> <span data-ttu-id="ba267-147">ค่า *N* คือตัวเลขตั้งแต่ 10 ถึง 100 และขึ้นอยู่กับการวัดโดยรวมที่ผู้ใช้เลือก</span><span class="sxs-lookup"><span data-stu-id="ba267-147">The value *N* is a number from 10 to 100 and is based on a user-selected aggregate measure.</span></span>

<span data-ttu-id="ba267-148">หากต้องการสร้างรายงาน **ส่วนลดอันดับแรก** ให้ดำเนินการตามขั้นตอนต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="ba267-148">To generate a **Top discounts** report, follow these steps.</span></span>

1. <span data-ttu-id="ba267-149">ไปที่ **Retail และ Commerce \> การสอบถามและรายงาน \> รายงานการขาย \> รายงานส่วนลดอันดับแรก**</span><span class="sxs-lookup"><span data-stu-id="ba267-149">Go to **Retail and Commerce \> Inquiries and reports \> Sales reports \> Top discounts report**.</span></span>
1. <span data-ttu-id="ba267-150">ในฟิลด์ **วันที่เริ่มต้น** ให้ป้อนวันที่</span><span class="sxs-lookup"><span data-stu-id="ba267-150">In the **From date** field, enter a date.</span></span>
1. <span data-ttu-id="ba267-151">ในฟิลด์ **วันที่สิ้นสุด** ให้ป้อนวันที่</span><span class="sxs-lookup"><span data-stu-id="ba267-151">In the **To date** field, enter a date.</span></span>
1. <span data-ttu-id="ba267-152">ในฟิลด์ **ช่องทาง** ให้เลือกช่องทางออนไลน์</span><span class="sxs-lookup"><span data-stu-id="ba267-152">In the **Channel** field, select the online channel.</span></span>
1. <span data-ttu-id="ba267-153">เลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="ba267-153">Select **OK**.</span></span>

## <a name="top-products-report"></a><span data-ttu-id="ba267-154">รายงานผลิตภัณฑ์อันดับแรก</span><span class="sxs-lookup"><span data-stu-id="ba267-154">Top products report</span></span>

<span data-ttu-id="ba267-155">รายงาน **ผลิตภัณฑ์อันดับแรก** แสดงเมตริกการขายสำหรับผลิตภัณฑ์ *N* ผลิตภัณฑ์แรกสำหรับช่องทางหรือหน่วยปฏิบัติงานที่เลือก</span><span class="sxs-lookup"><span data-stu-id="ba267-155">The **Top products** report shows sales metrics for the top *N* products for a selected channel or operating unit.</span></span> <span data-ttu-id="ba267-156">ค่า *N* คือตัวเลขตั้งแต่ 10 ถึง 100 และขึ้นอยู่กับการวัดโดยรวมที่ผู้ใช้เลือก</span><span class="sxs-lookup"><span data-stu-id="ba267-156">The value *N* is a number from 10 to 100 and is based on a user-selected aggregate measure.</span></span>

<span data-ttu-id="ba267-157">หากต้องการสร้างรายงาน **ผลิตภัณฑ์อันดับแรก** ให้ดำเนินการตามขั้นตอนต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="ba267-157">To generate a **Top products** report, follow these steps.</span></span>

1. <span data-ttu-id="ba267-158">ไปที่ **Retail และ Commerce \> การสอบถามและรายงาน \> รายงานการขาย \> รายงานผลิตภัณฑ์อันดับแรก**</span><span class="sxs-lookup"><span data-stu-id="ba267-158">Go to **Retail and Commerce \> Inquiries and reports \> Sales reports \> Top products report**.</span></span>
1. <span data-ttu-id="ba267-159">ในฟิลด์ **วันที่เริ่มต้น** ให้ป้อนวันที่</span><span class="sxs-lookup"><span data-stu-id="ba267-159">In the **From date** field, enter a date.</span></span>
1. <span data-ttu-id="ba267-160">ในฟิลด์ **วันที่สิ้นสุด** ให้ป้อนวันที่</span><span class="sxs-lookup"><span data-stu-id="ba267-160">In the **To date** field, enter a date.</span></span>
1. <span data-ttu-id="ba267-161">ในฟิลด์ **ช่องทาง** ให้เลือกช่องทางออนไลน์</span><span class="sxs-lookup"><span data-stu-id="ba267-161">In the **Channel** field, select the online channel.</span></span>
1. <span data-ttu-id="ba267-162">เลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="ba267-162">Select **OK**.</span></span>

## <a name="category-sales-report"></a><span data-ttu-id="ba267-163">รายงานการขายตามประเภท</span><span class="sxs-lookup"><span data-stu-id="ba267-163">Category sales report</span></span>

<span data-ttu-id="ba267-164">รายงาน **การขายตามประเภท** แสดงการวัดยอดขายในรอบระยะเวลาที่เลือก สำหรับแต่ละโหนดของการจัดประเภทตามลำดับชั้น สำหรับช่องทางหรือหน่วยปฏิบัติงานที่เลือก</span><span class="sxs-lookup"><span data-stu-id="ba267-164">The **Category sales** report shows sales metrics over a selected period for each node of a category hierarchy for a selected channel or operating unit.</span></span>

<span data-ttu-id="ba267-165">หากต้องการสร้างรายงาน **การขายตามประเภท** ให้ดำเนินการตามขั้นตอนต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="ba267-165">To generate a **Category sales** report, follow these steps.</span></span>

1. <span data-ttu-id="ba267-166">ไปที่ **Retail และ Commerce \> การสอบถามและรายงาน \> รายงานการขาย \> รายงานการขายตามประเภท**</span><span class="sxs-lookup"><span data-stu-id="ba267-166">Go to **Retail and Commerce \> Inquiries and reports \> Sales reports \> Category sales report**.</span></span>
1. <span data-ttu-id="ba267-167">ในฟิลด์ **วันที่เริ่มต้น** ให้ป้อนวันที่</span><span class="sxs-lookup"><span data-stu-id="ba267-167">In the **From date** field, enter a date.</span></span>
1. <span data-ttu-id="ba267-168">ในฟิลด์ **วันที่สิ้นสุด** ให้ป้อนวันที่</span><span class="sxs-lookup"><span data-stu-id="ba267-168">In the **To date** field, enter a date.</span></span>
1. <span data-ttu-id="ba267-169">ในฟิลด์ **ช่องทาง** ให้เลือกช่องทางออนไลน์</span><span class="sxs-lookup"><span data-stu-id="ba267-169">In the **Channel** field, select the online channel.</span></span>
1. <span data-ttu-id="ba267-170">เลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="ba267-170">Select **OK**.</span></span>

## <a name="organization-sales-report"></a><span data-ttu-id="ba267-171">รายงานยอดขายขององค์กร</span><span class="sxs-lookup"><span data-stu-id="ba267-171">Organization sales report</span></span>

<span data-ttu-id="ba267-172">รายงาน **การขายขององค์กร** จะแสดงประสิทธิภาพร้านค้าของคุณตามหน่วยองค์กร</span><span class="sxs-lookup"><span data-stu-id="ba267-172">The **Organization sales** report shows the performance of your stores by organization unit.</span></span> <span data-ttu-id="ba267-173">รายงานนี้รวมถึงปริมาณการขายและยอดเงินตามร้านค้าและกำไรขั้นต้นสำหรับร้านค้าแต่ละร้าน</span><span class="sxs-lookup"><span data-stu-id="ba267-173">This report includes the sales quantity and amount by store, and the profit margin for each store.</span></span> <span data-ttu-id="ba267-174">หน่วยงานจะขึ้นอยู่กับลำดับชั้นการรายงานเริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="ba267-174">The organization unit is based on the default reporting hierarchy.</span></span>

<span data-ttu-id="ba267-175">หากต้องการสร้างรายงาน **ยอดขายขององค์กร** ให้ดำเนินการตามขั้นตอนต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="ba267-175">To generate an **Organization sales** report, follow these steps.</span></span>

1. <span data-ttu-id="ba267-176">ไปที่ **Retail และ Commerce \> การสอบถามและรายงาน \> รายงานการขาย \> รายงานยอดขายขององค์กร**</span><span class="sxs-lookup"><span data-stu-id="ba267-176">Go to **Retail and Commerce \> Inquiries and reports \> Sales reports \> Organization sales report**.</span></span>
1. <span data-ttu-id="ba267-177">ในฟิลด์ **วันที่เริ่มต้น** ให้ป้อนวันที่</span><span class="sxs-lookup"><span data-stu-id="ba267-177">In the **From date** field, enter a date.</span></span>
1. <span data-ttu-id="ba267-178">ในฟิลด์ **วันที่สิ้นสุด** ให้ป้อนวันที่</span><span class="sxs-lookup"><span data-stu-id="ba267-178">In the **To date** field, enter a date.</span></span>
1. <span data-ttu-id="ba267-179">เลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="ba267-179">Select **OK**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="ba267-180">แหล่งข้อมูลเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="ba267-180">Additional resources</span></span>

- [<span data-ttu-id="ba267-181">แหล่งข้อมูลความช่วยเหลือสำหรับ Dynamics 365 Retail</span><span class="sxs-lookup"><span data-stu-id="ba267-181">Help resources for Dynamics 365 Retail</span></span>](../retail/index.md)
