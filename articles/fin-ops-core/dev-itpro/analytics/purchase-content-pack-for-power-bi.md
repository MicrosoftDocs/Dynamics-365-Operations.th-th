---
title: เนื้อหา Power BI เกี่ยวกับการวิเคราะห์การซื้อและการใช้จ่าย
description: หัวข้อนี้อธิบายถึงสิ่งที่จะรวมอยู่ในเนื้อหา Power BI เกี่ยวกับการวิเคราะห์การซื้อและการใช้จ่าย และยังอธิบายถึงวิธีการเข้าถึงรายงานที่รวมอยู่ในชุดเนื้อหานี้ และแสดงข้อมูลเกี่ยวกับแบบจำลองข้อมูลและเอนทิตี้ที่ใช้ในการสร้างชุดเนื้อหานี้
author: FrankDahl
manager: AnnBe
ms.date: 04/24/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: PurchaseSpendAnalysisPowerBI
audience: Application User, IT Pro
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 265434
ms.assetid: 3cd9dfce-2687-4303-bc78-349e7cb5ea75
ms.search.region: global
ms.author: fdahl
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 571f443b02268cbee8fe787f25419e046ba99aeb
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 09/27/2019
ms.locfileid: "2182864"
---
# <a name="purchase-spend-analysis-power-bi-content"></a><span data-ttu-id="b4885-104">เนื้อหา Power BI เกี่ยวกับการวิเคราะห์การซื้อและการใช้จ่าย</span><span class="sxs-lookup"><span data-stu-id="b4885-104">Purchase spend analysis Power BI content</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="b4885-105">หัวข้อนี้อธิบายถึงสิ่งที่จะรวมอยู่ในเนื้อหา Microsoft Power BI เกี่ยวกับ **การวิเคราะห์การซื้อและการใช้จ่าย**</span><span class="sxs-lookup"><span data-stu-id="b4885-105">This topic describes what is included in the **Purchase spend analysis** Microsoft Power BI content.</span></span> <span data-ttu-id="b4885-106">และยังอธิบายถึงวิธีการเข้าถึงรายงาน Power BI และแสดงข้อมูลเกี่ยวกับแบบจำลองข้อมูลและเอนทิตี้ที่ใช้ในการสร้างเนื้อหานี้</span><span class="sxs-lookup"><span data-stu-id="b4885-106">It explains how to access the Power BI reports, and provides information about the data model and entities that are used to build the content.</span></span>

## <a name="overview"></a><span data-ttu-id="b4885-107">ภาพรวม</span><span class="sxs-lookup"><span data-stu-id="b4885-107">Overview</span></span>

<span data-ttu-id="b4885-108">เนื้อหา Power BI **การวิเคราะห์การใช้จ่ายของการซื้อ** ถูกออกแบบมาเพื่อช่วยให้ผู้จัดการฝ่ายจัดซื้อและผู้จัดการที่รับผิดชอบสำหรับงบประมาณคอยติดตามการใช้จ่ายของการซื้อ</span><span class="sxs-lookup"><span data-stu-id="b4885-108">The **Purchase spend analysis** Power BI content was designed to help purchasing managers and managers who are responsible for budgets keep track of purchase spending.</span></span> <span data-ttu-id="b4885-109">ผู้จัดการสามารถวิเคราะห์การซื้อและการใช้จ่ายโดยใช้วิธีต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="b4885-109">Managers can analyze purchase spending in the following ways:</span></span>

- <span data-ttu-id="b4885-110">การซื้อตั้งแต่ต้นปีจนถึงปัจจุบัน (โดยเรียงตามกลุ่มผู้จัดจำหน่ายและแต่ละผู้จัดจำหน่าย ประเภทการจัดซื้อและแต่ละผลิตภัณฑ์ และที่ตั้งของผู้จัดจำหน่าย)</span><span class="sxs-lookup"><span data-stu-id="b4885-110">Year-to-date purchase (by vendor group and individual vendors, procurement category and individual products, and vendor location)</span></span>
- <span data-ttu-id="b4885-111">การเปลี่ยนแปลงการซื้อตั้งแต่ต้นปีจนถึงปัจจุบัน (โดยเรียงตามกลุ่มผู้จัดจำหน่ายและประเภทการจัดซื้อ)</span><span class="sxs-lookup"><span data-stu-id="b4885-111">Year-over-year purchase change (by vendor group and procurement category)</span></span>

<span data-ttu-id="b4885-112">เนื้อหานี้ใช้ข้อมูลเกี่ยวกับธุรกรรมการซื้อ และให้ทั้งมุมมองรวมของตัวเลขการซื้อของทั้งบริษัทและการแบ่งรายละเอียดของการซื้อและการใช้จ่ายโดยเรียงตามผู้จัดจำหน่ายและผลิตภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="b4885-112">The content uses purchase transactional data, and provides both an aggregate view of the company-wide purchase figures and a breakdown of purchase spending by vendor and product.</span></span> <span data-ttu-id="b4885-113">รายงานเน้นการเปลี่ยนแปลงในการซื้อและการใช้จ่ายเมื่อเวลาผ่านไป</span><span class="sxs-lookup"><span data-stu-id="b4885-113">Reports highlight changes in purchase spending over time.</span></span> <span data-ttu-id="b4885-114">ดังนั้น สามารถใช้การรายงานเพื่อจัดการการแจ้งเตือนเกี่ยวกับแนวโน้มการใช้จ่ายค่าบวกและค่าลบสำหรับแต่ละผู้จัดจำหน่ายและผลิตภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="b4885-114">Therefore, the reports can be used to alert managers about positive and negative spending trends for individual vendors and products.</span></span> <span data-ttu-id="b4885-115">นอกจากนี้ แผนภูมิแสดงการซื้อและการใช้จ่ายสำหรับประเภทการจัดซื้อและกลุ่มผู้จัดจำหน่ายที่แตกต่างกัน</span><span class="sxs-lookup"><span data-stu-id="b4885-115">Additionally, charts show purchase spending for different procurement categories and vendor groups.</span></span> <span data-ttu-id="b4885-116">ดังนั้น ประเภทและผู้จัดการภูมิภาคสามารถใช้แผนภูมิเหล่านี้เพื่อช่วยในการระบุการเปลี่ยนแปลงลักษณะการใช้จ่าย</span><span class="sxs-lookup"><span data-stu-id="b4885-116">Therefore, category and regional managers can use the charts to help identify changes in spending behavior.</span></span>

## <a name="accessing-the-power-bi-content"></a><span data-ttu-id="b4885-117">การเข้าถึงเนื้อหา Power BI</span><span class="sxs-lookup"><span data-stu-id="b4885-117">Accessing the Power BI content</span></span>
<span data-ttu-id="b4885-118">เนื้อหา Power BI เกี่ยวกับ **การวิเคราะห์การซื้อและการใช้จ่าย** จะแสดงบนหน้า **การวิเคราะห์การซื้อและการใช้จ่าย** (**การจัดซื้อและการจัดหา** \> **การสอบถามและรายงาน** \> **การวิเคราะห์ประสิทธิภาพซื้อ** \> **การวิเคราะห์การซื้อและการใช้จ่าย**)</span><span class="sxs-lookup"><span data-stu-id="b4885-118">The **Purchase spend analysis** Power BI content is shown on the **Purchase and spend analysis** page (**Procurement and sourcing** \> **Inquiries and reports** \> **Purchase performance analysis** \> **Purchase and spend analysis**).</span></span>

## <a name="metrics-that-are-included-in-the-power-bi-content"></a><span data-ttu-id="b4885-119">เมตริกที่รวมอยู่ในชุดเนื้อหา Power BI</span><span class="sxs-lookup"><span data-stu-id="b4885-119">Metrics that are included in the Power BI content</span></span>
<span data-ttu-id="b4885-120">ชุดเนื้อหา Power BI เกี่ยวกับ **การวิเคราะห์การซื้อและการใช้จ่าย** รวมรายงานที่ประกอบด้วยชุดของเมตริก</span><span class="sxs-lookup"><span data-stu-id="b4885-120">The **Purchase spend analysis** Power BI content includes a report that consists of a set of metrics.</span></span> <span data-ttu-id="b4885-121">เมตริกเหล่านี้จะถูกแสดงภาพข้อมูลโดยเป็นแผนภูมิ ไทล์ และตาราง</span><span class="sxs-lookup"><span data-stu-id="b4885-121">These metrics are visualized as charts, tiles, and tables.</span></span> 

<span data-ttu-id="b4885-122">ส่วนต่อไปนี้จะแสดงภาพรวมของการแสดงภาพ</span><span class="sxs-lookup"><span data-stu-id="b4885-122">The following sections provide an overview of the visualizations.</span></span>

### <a name="purchase-by-vendor-report-page"></a><span data-ttu-id="b4885-123">การซื้อโดยเรียงตามหน้ารายงานของผู้จัดจำหน่าย</span><span class="sxs-lookup"><span data-stu-id="b4885-123">Purchase by vendor report page</span></span>
<span data-ttu-id="b4885-124">**แผนภูมิ**</span><span class="sxs-lookup"><span data-stu-id="b4885-124">**Charts**</span></span>
- <span data-ttu-id="b4885-125">ผู้จัดจำหน่าย 10 อันดับแรกโดยเรียงตามการซื้อ (แผนภูมิแท่งแบบเรียงซ้อน)</span><span class="sxs-lookup"><span data-stu-id="b4885-125">Top 10 vendors by purchase (stacked bar chart)</span></span>
- <span data-ttu-id="b4885-126">ยอดรวมการซื้อโดยเรียงตามกลุ่มผู้จัดจำหน่าย/ ประเทศ / ชื่อ (แผนภูมิวงกลม)</span><span class="sxs-lookup"><span data-stu-id="b4885-126">Total purchase by vendor group / country / name (pie chart)</span></span>
- <span data-ttu-id="b4885-127">การซื้อโดยเรียงตามกลุ่มผู้จัดจำหน่าย/ ประเทศ / ชื่อ (แผนภูมิคอลัมน์)</span><span class="sxs-lookup"><span data-stu-id="b4885-127">Purchase by vendor group / country / name (column chart)</span></span>
- <span data-ttu-id="b4885-128">การซื้อเฉลี่ยโดยเรียงตามกลุ่มผู้จัดจำหน่าย/ ประเทศ / ชื่อ (แผนภูมิคอลัมน์)</span><span class="sxs-lookup"><span data-stu-id="b4885-128">Average purchase by vendor group / country / name (column chart)</span></span>

<span data-ttu-id="b4885-129">**ไทล์**</span><span class="sxs-lookup"><span data-stu-id="b4885-129">**Tiles**</span></span>
- <span data-ttu-id="b4885-130">การซื้อรวม</span><span class="sxs-lookup"><span data-stu-id="b4885-130">Total purchase</span></span>
- <span data-ttu-id="b4885-131">การเติบโตการซื้อ YOY</span><span class="sxs-lookup"><span data-stu-id="b4885-131">YOY purchase growth</span></span>
- <span data-ttu-id="b4885-132"># ผู้จัดจำหน่ายรวม</span><span class="sxs-lookup"><span data-stu-id="b4885-132">Total # vendors</span></span>
- <span data-ttu-id="b4885-133"># ผู้จัดจำหน่ายที่ใช้งานอยู่รวม</span><span class="sxs-lookup"><span data-stu-id="b4885-133">Total # of active vendors</span></span>

<span data-ttu-id="b4885-134">**ตัวอย่าง**</span><span class="sxs-lookup"><span data-stu-id="b4885-134">**Example**</span></span>
<img src="media/spend1.PNG" alt="Purchase by vendor">

### <a name="purchase-by-product-report-page"></a><span data-ttu-id="b4885-135">การซื้อโดยเรียงตามหน้ารายงานของผลิตภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="b4885-135">Purchase by product report page</span></span>

<span data-ttu-id="b4885-136">**แผนภูมิ**</span><span class="sxs-lookup"><span data-stu-id="b4885-136">**Charts**</span></span>
- <span data-ttu-id="b4885-137">การซื้อโดยเรียงตามประเภทการจัดซื้อ / ชื่อผลิตภัณฑ์ (แผนภูมิคอลัมน์)</span><span class="sxs-lookup"><span data-stu-id="b4885-137">Purchase by procurement category / product name (column chart)</span></span>
- <span data-ttu-id="b4885-138">ยอดการซื้อโดยเรียงตามประเภทการจัดซื้อ / ชื่อผลิตภัณฑ์ (แผนภูมิวงกลม)</span><span class="sxs-lookup"><span data-stu-id="b4885-138">Total purchase by procurement category / product name (pie chart)</span></span>
- <span data-ttu-id="b4885-139">ผลิตภัณฑ์ 10 อันดับแรกโดยเรียงตามการซื้อ (แผนภูมิแท่งแบบเรียงซ้อน)</span><span class="sxs-lookup"><span data-stu-id="b4885-139">Top 10 products by purchase (stacked bar chart)</span></span>

<span data-ttu-id="b4885-140">**ไทล์**</span><span class="sxs-lookup"><span data-stu-id="b4885-140">**Tiles**</span></span>
- <span data-ttu-id="b4885-141"># ผลิตภัณฑ์รวม</span><span class="sxs-lookup"><span data-stu-id="b4885-141">Total # of products</span></span></li>
- <span data-ttu-id="b4885-142">เปอร์เซ็นต์ของผลิตภัณฑ์ที่ใช้งานอยู่ทั้งหมดของ # ผลิตภัณฑ์รวม</span><span class="sxs-lookup"><span data-stu-id="b4885-142">Total active products percentage of total # of products</span></span>
- <span data-ttu-id="b4885-143">จำนวนของผลิตภัณฑ์ที่ลงบัญชีสำหรับการซื้อ 80%</span><span class="sxs-lookup"><span data-stu-id="b4885-143">Number of products accounting for 80% purchase</span></span>

<span data-ttu-id="b4885-144">**ตัวอย่าง**</span><span class="sxs-lookup"><span data-stu-id="b4885-144">**Example**</span></span>


<img src="media/purchaseByProduct.PNG" alt="Purchase by Product">

### <a name="purchase-by-period-report-page"></a><span data-ttu-id="b4885-145">การซื้อโดยเรียงตามหน้ารายงานของรอบระยะเวลา</span><span class="sxs-lookup"><span data-stu-id="b4885-145">Purchase by period report page</span></span>
<span data-ttu-id="b4885-146">หน้านี้แสดงการซื้อปีนี้และปีที่แล้ว และการเติบโตโดยเรียงตามประเภทการจัดซื้อ</span><span class="sxs-lookup"><span data-stu-id="b4885-146">This page shows purchases this year and last year, and growth by procurement category.</span></span>

<span data-ttu-id="b4885-147">**แผนภูมิ**</span><span class="sxs-lookup"><span data-stu-id="b4885-147">**Charts**</span></span> 
- <span data-ttu-id="b4885-148">การซื้อโดยเรียงตามเดือน / วัน (แผนภูมิคอลัมน์)</span><span class="sxs-lookup"><span data-stu-id="b4885-148">Purchase by month / day (column chart)</span></span>
- <span data-ttu-id="b4885-149">ค่าความแปรปรวน YOY การซื้อสะสม (แผนภูมิน้ำตก)</span><span class="sxs-lookup"><span data-stu-id="b4885-149">Cumulative purchase YOY variance (waterfall chart)</span></span>
- <span data-ttu-id="b4885-150">การเติบโต YOY การซื้อรวม (แผนภูมิคอลัมน์)</span><span class="sxs-lookup"><span data-stu-id="b4885-150">Total purchase YOY growth (column chart)</span></span>
- <span data-ttu-id="b4885-151">รายงานการจัดซื้อ (เมทริกซ์)</span><span class="sxs-lookup"><span data-stu-id="b4885-151">Procurement statement (matrix)</span></span>

<span data-ttu-id="b4885-152">**ไทล์**</span><span class="sxs-lookup"><span data-stu-id="b4885-152">**Tiles**</span></span>
- <span data-ttu-id="b4885-153">การเติบโตการซื้อ YOY</span><span class="sxs-lookup"><span data-stu-id="b4885-153">YOY purchase growth</span></span>
- <span data-ttu-id="b4885-154">% การเติบโตการซื้อ YOY</span><span class="sxs-lookup"><span data-stu-id="b4885-154">YOY purchase growth %</span></span>

<span data-ttu-id="b4885-155">**ตัวอย่าง**</span><span class="sxs-lookup"><span data-stu-id="b4885-155">**Example**</span></span>
<img src="media/purchaseByPeriod.PNG" alt="Purchase by Period">

### <a name="purchase-by-vendor-location-report-page"></a><span data-ttu-id="b4885-156">การซื้อโดยเรียงตามหน้ารายงานของสถานที่ของผู้จัดจำหน่าย</span><span class="sxs-lookup"><span data-stu-id="b4885-156">Purchase by vendor location report page</span></span>

<span data-ttu-id="b4885-157">**แผนภูมิ**</span><span class="sxs-lookup"><span data-stu-id="b4885-157">**Charts**</span></span>
- <span data-ttu-id="b4885-158">การซื้อโดยเรียงตามเมือง</span><span class="sxs-lookup"><span data-stu-id="b4885-158">Purchase by city</span></span>
- <span data-ttu-id="b4885-159">% การเติบโต YOY การซื้อ</span><span class="sxs-lookup"><span data-stu-id="b4885-159">Purchase YOY growth %</span></span>
- <span data-ttu-id="b4885-160">การซื้อโดยเรียงตามประเทศ</span><span class="sxs-lookup"><span data-stu-id="b4885-160">Purchase by country</span></span>

<span data-ttu-id="b4885-161">**ตัวอย่าง**</span><span class="sxs-lookup"><span data-stu-id="b4885-161">**Example**</span></span>
<img src="media/purchByVendorLocation.PNG" alt="Purchase by Vendor Location">

### <a name="purchase-spend-analysis-by-time-report-page"></a><span data-ttu-id="b4885-162">การวิเคราะห์การใช้จ่ายในการซื้อโดยเรียงตามหน้ารายงานเวลา</span><span class="sxs-lookup"><span data-stu-id="b4885-162">Purchase spend analysis by time report page</span></span>

<span data-ttu-id="b4885-163">**แผนภูมิ**</span><span class="sxs-lookup"><span data-stu-id="b4885-163">**Charts**</span></span> 
- <span data-ttu-id="b4885-164">การซื้อตั้งแต่ปีปัจจุบันโดยเรียงตามเดือน / วัน (แผนภูมิเส้น)</span><span class="sxs-lookup"><span data-stu-id="b4885-164">Purchase current year by month / day (line chart)</span></span>
- <span data-ttu-id="b4885-165">การซื้อปัจจุบันและปีที่แล้ว (แผนภูมิคอลัมน์และเส้น)</span><span class="sxs-lookup"><span data-stu-id="b4885-165">Purchase current and last year (line and column chart)</span></span>

<span data-ttu-id="b4885-166">**ตัวอย่าง**</span><span class="sxs-lookup"><span data-stu-id="b4885-166">**Example**</span></span>
<img src="media/PurchByTIme.PNG" alt="Purchase by Time">

### <a name="purchase-spend-analysis-by-vendor-report-page"></a><span data-ttu-id="b4885-167">การวิเคราะห์การใช้จ่ายในการซื้อโดยเรียงตามหน้ารายงานของผู้จัดจำหน่าย</span><span class="sxs-lookup"><span data-stu-id="b4885-167">Purchase spend analysis by vendor report page</span></span>

<span data-ttu-id="b4885-168">**แผนภูมิ**</span><span class="sxs-lookup"><span data-stu-id="b4885-168">**Charts**</span></span> 
- <span data-ttu-id="b4885-169">% การซื้อของผู้จัดจำหน่าย 10 อันดับแรกของการซื้อ (กรวย)</span><span class="sxs-lookup"><span data-stu-id="b4885-169">Top 10 vendor purchase % of purchase (funnel)</span></span>
- <span data-ttu-id="b4885-170">ผู้จัดจำหน่าย 10 อันดับแรกที่มี YOY การใช้จ่ายที่เพิ่มขึ้น</span><span class="sxs-lookup"><span data-stu-id="b4885-170">Top 10 vendors with increased spending YOY</span></span>
- <span data-ttu-id="b4885-171">ผู้จัดจำหน่าย 10 อันดับแรกที่มี YOY การใช้จ่ายที่ลดลง</span><span class="sxs-lookup"><span data-stu-id="b4885-171">Top 10 vendors with decreased spending YOY</span></span>

<span data-ttu-id="b4885-172">**ตัวอย่าง** 
</span><span class="sxs-lookup"><span data-stu-id="b4885-172">**Example** 
</span></span><img src="media/PurchSpendAnalysisByVendor.PNG" alt="Purchase spend by vendor">


## <a name="data-model-and-entities"></a><span data-ttu-id="b4885-173">แบบจำลองข้อมูลและเอนทิตี</span><span class="sxs-lookup"><span data-stu-id="b4885-173">Data model and entities</span></span>
<span data-ttu-id="b4885-174">ข้อมูลดังต่อไปนี้ถูกใช้ในการกรอกข้อมูลหน้ารายงานในเนื้อหา **การวิเคราะห์การซื้อและการใช้จ่าย** ใน Power BI</span><span class="sxs-lookup"><span data-stu-id="b4885-174">The following data is used to fill the report pages in the **Purchase spend analysis** Power BI content.</span></span> <span data-ttu-id="b4885-175">ข้อมูลนี้จะแสดงเป็นหน่วยวัดรวมที่มีการแบ่งระยะในที่จัดเก็บเอนทิตี้</span><span class="sxs-lookup"><span data-stu-id="b4885-175">This data is represented as aggregate measurements that are staged in the Entity store.</span></span> <span data-ttu-id="b4885-176">ที่จัดเก็บเอนทิตี้คือฐานข้อมูล Microsoft SQL Server ที่ได้รับการปรับให้เหมาะสมสำหรับการวิเคราะห์</span><span class="sxs-lookup"><span data-stu-id="b4885-176">The Entity store is a Microsoft SQL Server database that is optimized for analytics.</span></span> <span data-ttu-id="b4885-177">สำหรับข้อมูลเพิ่มเติม ดู [ภาพรวมของการรวม Power BI กับร้านค้าเอนทิตี](power-bi-integration-entity-store.md)</span><span class="sxs-lookup"><span data-stu-id="b4885-177">For more information, see [Overview of Power BI integration with Entity store](power-bi-integration-entity-store.md).</span></span>

<span data-ttu-id="b4885-178">การวัดแบบรวมในชุดเนื้อหานี้คือชุดย่อยของการวัดแบบรวมที่พร้อมใช้งานในคิวบ์การขายใน Microsoft Dynamics AX 2012 และ Microsoft Dynamics AX 2012 R3</span><span class="sxs-lookup"><span data-stu-id="b4885-178">The aggregate measurements in this content are the subset of aggregate measurements that were available in the Purchase Cube in Microsoft Dynamics AX 2012 and Microsoft Dynamics AX 2012 R3.</span></span> <span data-ttu-id="b4885-179">เมื่อต้องการแบ่งระยะของการวัดแบบรวมของ Cube ในร้านค้าเอนทิตี คุณจะต้องทำให้สามารถปรับใช้ได้</span><span class="sxs-lookup"><span data-stu-id="b4885-179">To stage the cube's aggregate measurements in the Entity store, you must make them deployable.</span></span> <span data-ttu-id="b4885-180">สำหรับข้อมูลเพิ่มเติม ดูกระบวนการสำหรับการแบ่งระยะการวัดแบบรวมในร้านค้าเอนทิตีใน [ภาพรวม Power BI กับร้านค้าเอนทิตี](power-bi-integration-entity-store.md)</span><span class="sxs-lookup"><span data-stu-id="b4885-180">For more information, see the procedure for staging aggregate measurements in the Entity store in [Overview of Power BI integration with Entity store](power-bi-integration-entity-store.md).</span></span> <span data-ttu-id="b4885-181">การวัดแบบรวมหลักต่อไปนี้จะพร้อมใช้งานได้โดยตรงจากเอนทิตีในบรรทัดใบแจ้งหนี้และจะถูกใช้เป็นข้อมูลพื้นฐานของเนื้อหา</span><span class="sxs-lookup"><span data-stu-id="b4885-181">The following key aggregate measurements are available directly from the Invoice lines entity and are used as the basis of the content.</span></span>

| <span data-ttu-id="b4885-182">เอนทิตี้</span><span class="sxs-lookup"><span data-stu-id="b4885-182">Entity</span></span>        | <span data-ttu-id="b4885-183">การวัดแบบรวมหลัก</span><span class="sxs-lookup"><span data-stu-id="b4885-183">Key aggregate measurements</span></span> | <span data-ttu-id="b4885-184">แหล่งข้อมูล</span><span class="sxs-lookup"><span data-stu-id="b4885-184">Data source</span></span>                                 | <span data-ttu-id="b4885-185">ฟิลด์</span><span class="sxs-lookup"><span data-stu-id="b4885-185">Field</span></span>              | <span data-ttu-id="b4885-186">คำอธิบาย</span><span class="sxs-lookup"><span data-stu-id="b4885-186">Description</span></span>                            |
|---------------|----------------------------|---------------------------------------------|--------------------|----------------------------------------|
| <span data-ttu-id="b4885-187">รายการในใบแจ้งหนี้</span><span class="sxs-lookup"><span data-stu-id="b4885-187">Invoice lines</span></span> | <span data-ttu-id="b4885-188">การซื้อ</span><span class="sxs-lookup"><span data-stu-id="b4885-188">Purchase</span></span>                   | <span data-ttu-id="b4885-189">VendInvoiceTrans</span><span class="sxs-lookup"><span data-stu-id="b4885-189">VendInvoiceTrans</span></span>                            | <span data-ttu-id="b4885-190">SUM(LineAmountMST)</span><span class="sxs-lookup"><span data-stu-id="b4885-190">SUM(LineAmountMST)</span></span> | <span data-ttu-id="b4885-191">ยอดเงินในสกุลเงินทางบัญชี</span><span class="sxs-lookup"><span data-stu-id="b4885-191">The amount in the accounting currency.</span></span> |

<span data-ttu-id="b4885-192">ตารางต่อไปนี้แสดงถึงการวัดหลักที่ถูกคำนวณในเนื้อหาที่คำนวณจากเอนทิตีในบรรทัดใบแจ้งหนี้</span><span class="sxs-lookup"><span data-stu-id="b4885-192">The following table shows the key measurements in the content that are calculated from the Invoice lines entity.</span></span>

| <span data-ttu-id="b4885-193">การประเมิน</span><span class="sxs-lookup"><span data-stu-id="b4885-193">Measure</span></span>               | <span data-ttu-id="b4885-194">การคำนวณ</span><span class="sxs-lookup"><span data-stu-id="b4885-194">Calculation</span></span>                                                                                         |
|-----------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b4885-195">การซื้อปีปัจจุบัน</span><span class="sxs-lookup"><span data-stu-id="b4885-195">Purchase current year</span></span> | <span data-ttu-id="b4885-196">การซื้อปีปัจจุบัน = SUM('Invoice lines'\[Purchase\])</span><span class="sxs-lookup"><span data-stu-id="b4885-196">Purchase current year = SUM('Invoice lines'\[Purchase\])</span></span>                                            |
| <span data-ttu-id="b4885-197">การซื้อปีที่แล้ว</span><span class="sxs-lookup"><span data-stu-id="b4885-197">Purchase last year</span></span>    | <span data-ttu-id="b4885-198">การซื้อปีที่แล้ว = CALCULATE(SUM('Invoice lines'\[Purchase\]), SAMEPERIODLASTYEAR(Dates\[Date\]))</span><span class="sxs-lookup"><span data-stu-id="b4885-198">Purchase last year = CALCULATE(SUM('Invoice lines'\[Purchase\]), SAMEPERIODLASTYEAR(Dates\[Date\]))</span></span> |
| <span data-ttu-id="b4885-199">การเติบโตการซื้อ YOY</span><span class="sxs-lookup"><span data-stu-id="b4885-199">YOY purchase growth</span></span>   | <span data-ttu-id="b4885-200">การเติบโตการซื้อ YOY = \[Purchase current year\] – \[Purchase last year\]</span><span class="sxs-lookup"><span data-stu-id="b4885-200">YOY purchase growth = \[Purchase current year\] – \[Purchase last year\]</span></span>                            |

<span data-ttu-id="b4885-201">มิติหลักในเนื้อหาต่อไปนี้จะถูกใช้เป็นตัวกรองเพื่อแบ่งส่วนการวัดแบบรวม เพื่อให้คุณสามารถได้รับส่วนประกอบที่มากขึ้นและได้รับข้อมูลเชิงลึกเชิงวิเคราะห์ที่ละเอียดมากขึ้น</span><span class="sxs-lookup"><span data-stu-id="b4885-201">The following key dimensions in the content are used as filters to slice the aggregate measurements, so that you can achieve more granularity and gain deeper analytical insights.</span></span>

| <span data-ttu-id="b4885-202">เอนทิตี้</span><span class="sxs-lookup"><span data-stu-id="b4885-202">Entity</span></span>                 | <span data-ttu-id="b4885-203">ตัวอย่างของแอตทริบิวต์</span><span class="sxs-lookup"><span data-stu-id="b4885-203">Examples of attributes</span></span>                                |
|------------------------|-------------------------------------------------------|
| <span data-ttu-id="b4885-204">ผู้จัดจำหน่าย</span><span class="sxs-lookup"><span data-stu-id="b4885-204">Vendors</span></span>                | <span data-ttu-id="b4885-205">กลุ่มผู้จัดจำหน่าย ประเทศหรือภูมิภาคของผู้จัดจำหน่าย ชื่อผู้จัดจำหน่าย</span><span class="sxs-lookup"><span data-stu-id="b4885-205">Vendor groups, Vendor country or regions, Vendor name</span></span> |
| <span data-ttu-id="b4885-206">ผลิตภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="b4885-206">Products</span></span>               | <span data-ttu-id="b4885-207">หมายเลขผลิตภัณฑ์ ชื่อผลิตภัณฑ์ ชื่อกลุ่มสินค้า</span><span class="sxs-lookup"><span data-stu-id="b4885-207">Product number, Product name, Item groups name</span></span>        |
| <span data-ttu-id="b4885-208">ประเภทการจัดซื้อ</span><span class="sxs-lookup"><span data-stu-id="b4885-208">Procurement categories</span></span> | <span data-ttu-id="b4885-209">ประเภทการจัดซื้อ ชื่อประเภทการจัดซื้อ</span><span class="sxs-lookup"><span data-stu-id="b4885-209">Procurement category, Procurement category names</span></span>      |
| <span data-ttu-id="b4885-210">นิติบุคคล</span><span class="sxs-lookup"><span data-stu-id="b4885-210">Legal entities</span></span>         | <span data-ttu-id="b4885-211">ชื่อนิติบุคคล</span><span class="sxs-lookup"><span data-stu-id="b4885-211">Legal entity name</span></span>                                     |
| <span data-ttu-id="b4885-212">วันที่</span><span class="sxs-lookup"><span data-stu-id="b4885-212">Dates</span></span>                  | <span data-ttu-id="b4885-213">วันที่ ออฟเซ็ตของปี</span><span class="sxs-lookup"><span data-stu-id="b4885-213">Dates, Year offset</span></span>                                    |

<span data-ttu-id="b4885-214">โดยค่าเริ่มต้น เนื้อหาจะแสดงข้อมูลสำหรับปีปฏิทินปัจจุบัน</span><span class="sxs-lookup"><span data-stu-id="b4885-214">By default, the content shows data for the current calendar year.</span></span> <span data-ttu-id="b4885-215">อย่างไรก็ตาม คุณสามารถเปลี่ยนตัวกรองวันที่ในส่วนตัวกรองรายงาน</span><span class="sxs-lookup"><span data-stu-id="b4885-215">However, you can change the date filter in the report filters section.</span></span> <span data-ttu-id="b4885-216">นอกจากนี้คุณยังสามารถเปลี่ยนตัวกรองของบริษัท</span><span class="sxs-lookup"><span data-stu-id="b4885-216">You can also change the company filter.</span></span>
