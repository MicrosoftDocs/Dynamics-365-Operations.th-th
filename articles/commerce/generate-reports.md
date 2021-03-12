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
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: samjar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 58342f07233e3c6a6e6a1af87ab23513ad63caf5
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 01/15/2021
ms.locfileid: "4970053"
---
# <a name="generate-online-channel-reports"></a><span data-ttu-id="cfc74-103">สร้างรายงานช่องทางออนไลน์</span><span class="sxs-lookup"><span data-stu-id="cfc74-103">Generate online channel reports</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="cfc74-104">หัวข้อนี้จะอธิบายวิธีการสร้างรายงานสำหรับช่องทางออนไลน์ของคุณใน Microsoft Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="cfc74-104">This topic describes how to generate reports for your online channel in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="cfc74-105">ภาพรวม</span><span class="sxs-lookup"><span data-stu-id="cfc74-105">Overview</span></span>

<span data-ttu-id="cfc74-106">คุณสามารถสร้างและดูรายงานต่างๆใน Commerce เพื่อดูว่าช่องทางออนไลน์ของคุณกำลังดำเนินการเป็นอย่างไร</span><span class="sxs-lookup"><span data-stu-id="cfc74-106">You can generate and view several reports in Commerce to see how your online channel is performing.</span></span>

## <a name="channel-summary-report"></a><span data-ttu-id="cfc74-107">รายงานสรุปช่องทาง</span><span class="sxs-lookup"><span data-stu-id="cfc74-107">Channel summary report</span></span>

<span data-ttu-id="cfc74-108">รายงาน **สรุปช่องทาง** แสดงสรุปของธุรกรรมต่อไปนี้สำหรับช่องทางที่เลือกดังนี้</span><span class="sxs-lookup"><span data-stu-id="cfc74-108">The **Channel summary** report shows a summary of the following transactions for the selected channel:</span></span>

- <span data-ttu-id="cfc74-109">ธุรกรรมการขาย</span><span class="sxs-lookup"><span data-stu-id="cfc74-109">Sales transactions</span></span>
- <span data-ttu-id="cfc74-110">ธุรกรรมการชำระเงิน</span><span class="sxs-lookup"><span data-stu-id="cfc74-110">Payment transactions</span></span>
- <span data-ttu-id="cfc74-111">ธุรกรรมภาษี</span><span class="sxs-lookup"><span data-stu-id="cfc74-111">Tax transactions</span></span>
- <span data-ttu-id="cfc74-112">ธุรกรรมที่ลดราคา</span><span class="sxs-lookup"><span data-stu-id="cfc74-112">Discounted transactions</span></span>

<span data-ttu-id="cfc74-113">หากต้องการสร้างรายงาน **สรุปช่องทาง** ให้ดำเนินการตามขั้นตอนต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="cfc74-113">To generate a **Channel summary** report, follow these steps.</span></span>

1. <span data-ttu-id="cfc74-114">ไปที่ **Retail และ Commerce \> การสอบถามและรายงาน \> รายงานการขาย \> รายงานสรุปช่องทาง**</span><span class="sxs-lookup"><span data-stu-id="cfc74-114">Go to **Retail and Commerce \> Inquiries and reports \> Sales reports \> Channel summary report**.</span></span>
1. <span data-ttu-id="cfc74-115">ในฟิลด์ **วันที่เริ่มต้น** ให้ป้อนวันที่</span><span class="sxs-lookup"><span data-stu-id="cfc74-115">In the **From date** field, enter a date.</span></span>
1. <span data-ttu-id="cfc74-116">ในฟิลด์ **วันที่สิ้นสุด** ให้ป้อนวันที่</span><span class="sxs-lookup"><span data-stu-id="cfc74-116">In the **To date** field, enter a date.</span></span>
1. <span data-ttu-id="cfc74-117">ในฟิลด์ **ช่องทาง** ให้เลือกช่องทางออนไลน์</span><span class="sxs-lookup"><span data-stu-id="cfc74-117">In the **Channel** field, select the online channel.</span></span>
1. <span data-ttu-id="cfc74-118">เลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="cfc74-118">Select **OK**.</span></span>
 
## <a name="channel-sales-by-year-report"></a><span data-ttu-id="cfc74-119">รายงานการขายผ่านช่องทางตามปี</span><span class="sxs-lookup"><span data-stu-id="cfc74-119">Channel sales by year report</span></span> 

<span data-ttu-id="cfc74-120">รายงาน **ช่องทางการขายรายปี** แสดงการเปรียบเทียบยอดขายปีต่อปี สำหรับร้านค้าเฉพาะ</span><span class="sxs-lookup"><span data-stu-id="cfc74-120">The **Channel sales by year** report shows a comparison of year-over-year sales for a specific store.</span></span> <span data-ttu-id="cfc74-121">คุณเลือกปีที่ต้องการเปรียบเทียบยอดขายด้วย และรายงานจะเปรียบเทียบการขายสำหรับปีที่เลือกกับการขายสำหรับปีก่อนหน้านี้</span><span class="sxs-lookup"><span data-stu-id="cfc74-121">You select the year to compare the sales against, and the report compares sales for the selected year with sales for the previous year.</span></span>

<span data-ttu-id="cfc74-122">หากต้องการสร้างรายงาน **ช่องทางการขายรายปี** ให้ดำเนินการตามขั้นตอนต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="cfc74-122">To generate a **Channel sales by year** report, follow these steps.</span></span>

1. <span data-ttu-id="cfc74-123">ไปที่ **Retail และ Commerce \> การสอบถามและรายงาน \> รายงานการขาย \> รายงานสรุปช่องทาง**</span><span class="sxs-lookup"><span data-stu-id="cfc74-123">Go to **Retail and Commerce \> Inquiries and reports \> Sales reports \> Channel sales by year report**.</span></span>
1. <span data-ttu-id="cfc74-124">ในฟิลด์ **ปีปฏิทินเริ่มต้น** ให้ระบุปี</span><span class="sxs-lookup"><span data-stu-id="cfc74-124">In the **From calendar year** field, enter a year.</span></span>
1. <span data-ttu-id="cfc74-125">ในฟิลด์ **ปีปฏิทินสิ้นสุด** ให้ระบุปี</span><span class="sxs-lookup"><span data-stu-id="cfc74-125">In the **To calendar year** field, enter a year.</span></span>
1. <span data-ttu-id="cfc74-126">ในฟิลด์ **ช่องทาง** ให้เลือกช่องทางออนไลน์</span><span class="sxs-lookup"><span data-stu-id="cfc74-126">In the **Channel** field, select the online channel.</span></span>
1. <span data-ttu-id="cfc74-127">เลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="cfc74-127">Select **OK**.</span></span>

## <a name="channel-sales-by-hour-report"></a><span data-ttu-id="cfc74-128">รายงานการขายผ่านช่องทางตามชั่วโมง</span><span class="sxs-lookup"><span data-stu-id="cfc74-128">Channel sales by hour report</span></span>

<span data-ttu-id="cfc74-129">รายงาน **ช่องทางการขายรายชั่วโมง** แสดงเมตริกการขายต่อชั่วโมงสำหรับช่องทางหรือหน่วยปฏิบัติงานที่เลือก</span><span class="sxs-lookup"><span data-stu-id="cfc74-129">The **Channel sales by hour** report shows sales metrics per hour for a selected channel or operating unit.</span></span>

<span data-ttu-id="cfc74-130">หากต้องการสร้างรายงาน **ช่องทางการขายรายชั่วโมง** ให้ดำเนินการตามขั้นตอนต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="cfc74-130">To generate a **Channel sales by hour** report, follow these steps.</span></span>

1. <span data-ttu-id="cfc74-131">ไปที่ **Retail และ Commerce \> การสอบถามและรายงาน \> รายงานการขาย \> รายงานช่องทางการขายตามชั่วโมง**</span><span class="sxs-lookup"><span data-stu-id="cfc74-131">Go to **Retail and Commerce \> Inquiries and reports \> Sales reports \> Channel sales by hour report**.</span></span>
1. <span data-ttu-id="cfc74-132">ในฟิลด์ **วันที่เริ่มต้น** ให้ป้อนวันที่</span><span class="sxs-lookup"><span data-stu-id="cfc74-132">In the **From date** field, enter a date.</span></span>
1. <span data-ttu-id="cfc74-133">ในฟิลด์ **วันที่สิ้นสุด** ให้ป้อนวันที่</span><span class="sxs-lookup"><span data-stu-id="cfc74-133">In the **To date** field, enter a date.</span></span>
1. <span data-ttu-id="cfc74-134">ในฟิลด์ **ช่องทาง** ให้เลือกช่องทางออนไลน์</span><span class="sxs-lookup"><span data-stu-id="cfc74-134">In the **Channel** field, select the online channel.</span></span>
1. <span data-ttu-id="cfc74-135">เลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="cfc74-135">Select **OK**.</span></span>

## <a name="top-customers-report"></a><span data-ttu-id="cfc74-136">รายงานลูกค้าอันดับแรก</span><span class="sxs-lookup"><span data-stu-id="cfc74-136">Top customers report</span></span>

<span data-ttu-id="cfc74-137">รายงาน **ลูกค้าอันดับแรก** แสดงเมตริกการขายสำหรับลูกค้า *N* รายแรกสำหรับช่องทางหรือหน่วยปฏิบัติงานที่เลือก</span><span class="sxs-lookup"><span data-stu-id="cfc74-137">The **Top customers** report shows sales metrics for the top *N* customers for a selected channel or operating unit.</span></span> <span data-ttu-id="cfc74-138">ค่า *N* คือตัวเลขตั้งแต่ 10 ถึง 100 และขึ้นอยู่กับการวัดโดยรวมที่ผู้ใช้เลือก</span><span class="sxs-lookup"><span data-stu-id="cfc74-138">The value *N* is a number from 10 to 100 and is based on a user-selected aggregate measure.</span></span>

<span data-ttu-id="cfc74-139">หากต้องการสร้างรายงาน **ลูกค้าอันดับแรก** ให้ดำเนินการตามขั้นตอนต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="cfc74-139">To generate a **Top customers** report, follow these steps.</span></span>

1. <span data-ttu-id="cfc74-140">ไปที่ **Retail และ Commerce \> การสอบถามและรายงาน \> รายงานการขาย \> รายงานลูกค้าอันดับแรก**</span><span class="sxs-lookup"><span data-stu-id="cfc74-140">Go to **Retail and Commerce \> Inquiries and reports \> Sales reports \> Top customers report**.</span></span>
1. <span data-ttu-id="cfc74-141">ในฟิลด์ **วันที่เริ่มต้น** ให้ป้อนวันที่</span><span class="sxs-lookup"><span data-stu-id="cfc74-141">In the **From date** field, enter a date.</span></span>
1. <span data-ttu-id="cfc74-142">ในฟิลด์ **วันที่สิ้นสุด** ให้ป้อนวันที่</span><span class="sxs-lookup"><span data-stu-id="cfc74-142">In the **To date** field, enter a date.</span></span>
1. <span data-ttu-id="cfc74-143">ในฟิลด์ **ช่องทาง** ให้เลือกช่องทางออนไลน์</span><span class="sxs-lookup"><span data-stu-id="cfc74-143">In the **Channel** field, select the online channel.</span></span>
1. <span data-ttu-id="cfc74-144">เลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="cfc74-144">Select **OK**.</span></span>

## <a name="top-discounts-report"></a><span data-ttu-id="cfc74-145">รายงานส่วนลดอันดับแรก</span><span class="sxs-lookup"><span data-stu-id="cfc74-145">Top discounts report</span></span>

<span data-ttu-id="cfc74-146">รายงาน **ส่วนลดอันดับแรก** แสดงเมตริกการขายสำหรับส่วนลด *N* ส่วนลดแรกสำหรับช่องทางหรือหน่วยปฏิบัติงานที่เลือก</span><span class="sxs-lookup"><span data-stu-id="cfc74-146">The **Top discounts** report shows sales metrics for the top *N* discounts for a selected channel or operating unit.</span></span> <span data-ttu-id="cfc74-147">ค่า *N* คือตัวเลขตั้งแต่ 10 ถึง 100 และขึ้นอยู่กับการวัดโดยรวมที่ผู้ใช้เลือก</span><span class="sxs-lookup"><span data-stu-id="cfc74-147">The value *N* is a number from 10 to 100 and is based on a user-selected aggregate measure.</span></span>

<span data-ttu-id="cfc74-148">หากต้องการสร้างรายงาน **ส่วนลดอันดับแรก** ให้ดำเนินการตามขั้นตอนต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="cfc74-148">To generate a **Top discounts** report, follow these steps.</span></span>

1. <span data-ttu-id="cfc74-149">ไปที่ **Retail และ Commerce \> การสอบถามและรายงาน \> รายงานการขาย \> รายงานส่วนลดอันดับแรก**</span><span class="sxs-lookup"><span data-stu-id="cfc74-149">Go to **Retail and Commerce \> Inquiries and reports \> Sales reports \> Top discounts report**.</span></span>
1. <span data-ttu-id="cfc74-150">ในฟิลด์ **วันที่เริ่มต้น** ให้ป้อนวันที่</span><span class="sxs-lookup"><span data-stu-id="cfc74-150">In the **From date** field, enter a date.</span></span>
1. <span data-ttu-id="cfc74-151">ในฟิลด์ **วันที่สิ้นสุด** ให้ป้อนวันที่</span><span class="sxs-lookup"><span data-stu-id="cfc74-151">In the **To date** field, enter a date.</span></span>
1. <span data-ttu-id="cfc74-152">ในฟิลด์ **ช่องทาง** ให้เลือกช่องทางออนไลน์</span><span class="sxs-lookup"><span data-stu-id="cfc74-152">In the **Channel** field, select the online channel.</span></span>
1. <span data-ttu-id="cfc74-153">เลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="cfc74-153">Select **OK**.</span></span>

## <a name="top-products-report"></a><span data-ttu-id="cfc74-154">รายงานผลิตภัณฑ์อันดับแรก</span><span class="sxs-lookup"><span data-stu-id="cfc74-154">Top products report</span></span>

<span data-ttu-id="cfc74-155">รายงาน **ผลิตภัณฑ์อันดับแรก** แสดงเมตริกการขายสำหรับผลิตภัณฑ์ *N* ผลิตภัณฑ์แรกสำหรับช่องทางหรือหน่วยปฏิบัติงานที่เลือก</span><span class="sxs-lookup"><span data-stu-id="cfc74-155">The **Top products** report shows sales metrics for the top *N* products for a selected channel or operating unit.</span></span> <span data-ttu-id="cfc74-156">ค่า *N* คือตัวเลขตั้งแต่ 10 ถึง 100 และขึ้นอยู่กับการวัดโดยรวมที่ผู้ใช้เลือก</span><span class="sxs-lookup"><span data-stu-id="cfc74-156">The value *N* is a number from 10 to 100 and is based on a user-selected aggregate measure.</span></span>

<span data-ttu-id="cfc74-157">หากต้องการสร้างรายงาน **ผลิตภัณฑ์อันดับแรก** ให้ดำเนินการตามขั้นตอนต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="cfc74-157">To generate a **Top products** report, follow these steps.</span></span>

1. <span data-ttu-id="cfc74-158">ไปที่ **Retail และ Commerce \> การสอบถามและรายงาน \> รายงานการขาย \> รายงานผลิตภัณฑ์อันดับแรก**</span><span class="sxs-lookup"><span data-stu-id="cfc74-158">Go to **Retail and Commerce \> Inquiries and reports \> Sales reports \> Top products report**.</span></span>
1. <span data-ttu-id="cfc74-159">ในฟิลด์ **วันที่เริ่มต้น** ให้ป้อนวันที่</span><span class="sxs-lookup"><span data-stu-id="cfc74-159">In the **From date** field, enter a date.</span></span>
1. <span data-ttu-id="cfc74-160">ในฟิลด์ **วันที่สิ้นสุด** ให้ป้อนวันที่</span><span class="sxs-lookup"><span data-stu-id="cfc74-160">In the **To date** field, enter a date.</span></span>
1. <span data-ttu-id="cfc74-161">ในฟิลด์ **ช่องทาง** ให้เลือกช่องทางออนไลน์</span><span class="sxs-lookup"><span data-stu-id="cfc74-161">In the **Channel** field, select the online channel.</span></span>
1. <span data-ttu-id="cfc74-162">เลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="cfc74-162">Select **OK**.</span></span>

## <a name="category-sales-report"></a><span data-ttu-id="cfc74-163">รายงานการขายตามประเภท</span><span class="sxs-lookup"><span data-stu-id="cfc74-163">Category sales report</span></span>

<span data-ttu-id="cfc74-164">รายงาน **การขายตามประเภท** แสดงการวัดยอดขายในรอบระยะเวลาที่เลือก สำหรับแต่ละโหนดของการจัดประเภทตามลำดับชั้น สำหรับช่องทางหรือหน่วยปฏิบัติงานที่เลือก</span><span class="sxs-lookup"><span data-stu-id="cfc74-164">The **Category sales** report shows sales metrics over a selected period for each node of a category hierarchy for a selected channel or operating unit.</span></span>

<span data-ttu-id="cfc74-165">หากต้องการสร้างรายงาน **การขายตามประเภท** ให้ดำเนินการตามขั้นตอนต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="cfc74-165">To generate a **Category sales** report, follow these steps.</span></span>

1. <span data-ttu-id="cfc74-166">ไปที่ **Retail และ Commerce \> การสอบถามและรายงาน \> รายงานการขาย \> รายงานการขายตามประเภท**</span><span class="sxs-lookup"><span data-stu-id="cfc74-166">Go to **Retail and Commerce \> Inquiries and reports \> Sales reports \> Category sales report**.</span></span>
1. <span data-ttu-id="cfc74-167">ในฟิลด์ **วันที่เริ่มต้น** ให้ป้อนวันที่</span><span class="sxs-lookup"><span data-stu-id="cfc74-167">In the **From date** field, enter a date.</span></span>
1. <span data-ttu-id="cfc74-168">ในฟิลด์ **วันที่สิ้นสุด** ให้ป้อนวันที่</span><span class="sxs-lookup"><span data-stu-id="cfc74-168">In the **To date** field, enter a date.</span></span>
1. <span data-ttu-id="cfc74-169">ในฟิลด์ **ช่องทาง** ให้เลือกช่องทางออนไลน์</span><span class="sxs-lookup"><span data-stu-id="cfc74-169">In the **Channel** field, select the online channel.</span></span>
1. <span data-ttu-id="cfc74-170">เลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="cfc74-170">Select **OK**.</span></span>

## <a name="organization-sales-report"></a><span data-ttu-id="cfc74-171">รายงานยอดขายขององค์กร</span><span class="sxs-lookup"><span data-stu-id="cfc74-171">Organization sales report</span></span>

<span data-ttu-id="cfc74-172">รายงาน **การขายขององค์กร** จะแสดงประสิทธิภาพร้านค้าของคุณตามหน่วยองค์กร</span><span class="sxs-lookup"><span data-stu-id="cfc74-172">The **Organization sales** report shows the performance of your stores by organization unit.</span></span> <span data-ttu-id="cfc74-173">รายงานนี้รวมถึงปริมาณการขายและยอดเงินตามร้านค้าและกำไรขั้นต้นสำหรับร้านค้าแต่ละร้าน</span><span class="sxs-lookup"><span data-stu-id="cfc74-173">This report includes the sales quantity and amount by store, and the profit margin for each store.</span></span> <span data-ttu-id="cfc74-174">หน่วยงานจะขึ้นอยู่กับลำดับชั้นการรายงานเริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="cfc74-174">The organization unit is based on the default reporting hierarchy.</span></span>

<span data-ttu-id="cfc74-175">หากต้องการสร้างรายงาน **ยอดขายขององค์กร** ให้ดำเนินการตามขั้นตอนต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="cfc74-175">To generate an **Organization sales** report, follow these steps.</span></span>

1. <span data-ttu-id="cfc74-176">ไปที่ **Retail และ Commerce \> การสอบถามและรายงาน \> รายงานการขาย \> รายงานยอดขายขององค์กร**</span><span class="sxs-lookup"><span data-stu-id="cfc74-176">Go to **Retail and Commerce \> Inquiries and reports \> Sales reports \> Organization sales report**.</span></span>
1. <span data-ttu-id="cfc74-177">ในฟิลด์ **วันที่เริ่มต้น** ให้ป้อนวันที่</span><span class="sxs-lookup"><span data-stu-id="cfc74-177">In the **From date** field, enter a date.</span></span>
1. <span data-ttu-id="cfc74-178">ในฟิลด์ **วันที่สิ้นสุด** ให้ป้อนวันที่</span><span class="sxs-lookup"><span data-stu-id="cfc74-178">In the **To date** field, enter a date.</span></span>
1. <span data-ttu-id="cfc74-179">เลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="cfc74-179">Select **OK**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="cfc74-180">แหล่งข้อมูลเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="cfc74-180">Additional resources</span></span>

- [<span data-ttu-id="cfc74-181">โฮมเพจการค้า</span><span class="sxs-lookup"><span data-stu-id="cfc74-181">Commerce home page</span></span>](../retail/index.md)
