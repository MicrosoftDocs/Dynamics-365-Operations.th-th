---
title: เนื้อหา Power BI เกี่ยวกับการวิเคราะห์การซื้อและการใช้จ่าย
description: หัวข้อนี้อธิบายถึงสิ่งที่จะรวมอยู่ในเนื้อหา Power BI เกี่ยวกับการวิเคราะห์การซื้อและการใช้จ่าย
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
ms.custom: 265434
ms.assetid: 3cd9dfce-2687-4303-bc78-349e7cb5ea75
ms.search.region: global
ms.author: fdahl
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 5914abaafab509e278d7a85441928feddb0b5164
ms.sourcegitcommit: 5192cfaedfd861faea63d8954d7bcc500608a225
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 01/30/2021
ms.locfileid: "5093453"
---
# <a name="purchase-spend-analysis-power-bi-content"></a><span data-ttu-id="42b2e-103">เนื้อหา Power BI เกี่ยวกับการวิเคราะห์การซื้อและการใช้จ่าย</span><span class="sxs-lookup"><span data-stu-id="42b2e-103">Purchase spend analysis Power BI content</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="42b2e-104">หัวข้อนี้อธิบายถึงสิ่งที่จะรวมอยู่ในเนื้อหา Microsoft Power BI เกี่ยวกับ **การวิเคราะห์การซื้อและการใช้จ่าย**</span><span class="sxs-lookup"><span data-stu-id="42b2e-104">This topic describes what is included in the **Purchase spend analysis** Microsoft Power BI content.</span></span> <span data-ttu-id="42b2e-105">และยังอธิบายถึงวิธีการเข้าถึงรายงาน Power BI และแสดงข้อมูลเกี่ยวกับแบบจำลองข้อมูลและเอนทิตี้ที่ใช้ในการสร้างเนื้อหานี้</span><span class="sxs-lookup"><span data-stu-id="42b2e-105">It explains how to access the Power BI reports, and provides information about the data model and entities that are used to build the content.</span></span>

## <a name="overview"></a><span data-ttu-id="42b2e-106">ภาพรวม</span><span class="sxs-lookup"><span data-stu-id="42b2e-106">Overview</span></span>

<span data-ttu-id="42b2e-107">เนื้อหา Power BI **การวิเคราะห์การใช้จ่ายของการซื้อ** ถูกออกแบบมาเพื่อช่วยให้ผู้จัดการฝ่ายจัดซื้อและผู้จัดการที่รับผิดชอบสำหรับงบประมาณคอยติดตามการใช้จ่ายของการซื้อ</span><span class="sxs-lookup"><span data-stu-id="42b2e-107">The **Purchase spend analysis** Power BI content was designed to help purchasing managers and managers who are responsible for budgets keep track of purchase spending.</span></span> <span data-ttu-id="42b2e-108">ผู้จัดการสามารถวิเคราะห์การซื้อและการใช้จ่ายโดยใช้วิธีต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="42b2e-108">Managers can analyze purchase spending in the following ways:</span></span>

- <span data-ttu-id="42b2e-109">การซื้อตั้งแต่ต้นปีจนถึงปัจจุบัน (โดยเรียงตามกลุ่มผู้จัดจำหน่ายและแต่ละผู้จัดจำหน่าย ประเภทการจัดซื้อและแต่ละผลิตภัณฑ์ และที่ตั้งของผู้จัดจำหน่าย)</span><span class="sxs-lookup"><span data-stu-id="42b2e-109">Year-to-date purchase (by vendor group and individual vendors, procurement category and individual products, and vendor location)</span></span>
- <span data-ttu-id="42b2e-110">การเปลี่ยนแปลงการซื้อตั้งแต่ต้นปีจนถึงปัจจุบัน (โดยเรียงตามกลุ่มผู้จัดจำหน่ายและประเภทการจัดซื้อ)</span><span class="sxs-lookup"><span data-stu-id="42b2e-110">Year-over-year purchase change (by vendor group and procurement category)</span></span>

<span data-ttu-id="42b2e-111">เนื้อหานี้ใช้ข้อมูลเกี่ยวกับธุรกรรมการซื้อ และให้ทั้งมุมมองรวมของตัวเลขการซื้อของทั้งบริษัทและการแบ่งรายละเอียดของการซื้อและการใช้จ่ายโดยเรียงตามผู้จัดจำหน่ายและผลิตภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="42b2e-111">The content uses purchase transactional data, and provides both an aggregate view of the company-wide purchase figures and a breakdown of purchase spending by vendor and product.</span></span> <span data-ttu-id="42b2e-112">รายงานเน้นการเปลี่ยนแปลงในการซื้อและการใช้จ่ายเมื่อเวลาผ่านไป</span><span class="sxs-lookup"><span data-stu-id="42b2e-112">Reports highlight changes in purchase spending over time.</span></span> <span data-ttu-id="42b2e-113">ดังนั้น สามารถใช้การรายงานเพื่อจัดการการแจ้งเตือนเกี่ยวกับแนวโน้มการใช้จ่ายค่าบวกและค่าลบสำหรับแต่ละผู้จัดจำหน่ายและผลิตภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="42b2e-113">Therefore, the reports can be used to alert managers about positive and negative spending trends for individual vendors and products.</span></span> <span data-ttu-id="42b2e-114">นอกจากนี้ แผนภูมิแสดงการซื้อและการใช้จ่ายสำหรับประเภทการจัดซื้อและกลุ่มผู้จัดจำหน่ายที่แตกต่างกัน</span><span class="sxs-lookup"><span data-stu-id="42b2e-114">Additionally, charts show purchase spending for different procurement categories and vendor groups.</span></span> <span data-ttu-id="42b2e-115">ดังนั้น ประเภทและผู้จัดการภูมิภาคสามารถใช้แผนภูมิเหล่านี้เพื่อช่วยในการระบุการเปลี่ยนแปลงลักษณะการใช้จ่าย</span><span class="sxs-lookup"><span data-stu-id="42b2e-115">Therefore, category and regional managers can use the charts to help identify changes in spending behavior.</span></span>

## <a name="accessing-the-power-bi-content"></a><span data-ttu-id="42b2e-116">การเข้าถึงเนื้อหา Power BI</span><span class="sxs-lookup"><span data-stu-id="42b2e-116">Accessing the Power BI content</span></span>
<span data-ttu-id="42b2e-117">เนื้อหา Power BI เกี่ยวกับ **การวิเคราะห์การซื้อและการใช้จ่าย** จะแสดงบนหน้า **การวิเคราะห์การซื้อและการใช้จ่าย** (**การจัดซื้อและการจัดหา** \> **การสอบถามและรายงาน** \> **การวิเคราะห์ประสิทธิภาพซื้อ** \> **การวิเคราะห์การซื้อและการใช้จ่าย**)</span><span class="sxs-lookup"><span data-stu-id="42b2e-117">The **Purchase spend analysis** Power BI content is shown on the **Purchase and spend analysis** page (**Procurement and sourcing** \> **Inquiries and reports** \> **Purchase performance analysis** \> **Purchase and spend analysis**).</span></span>

## <a name="metrics-that-are-included-in-the-power-bi-content"></a><span data-ttu-id="42b2e-118">เมตริกที่รวมอยู่ในชุดเนื้อหา Power BI</span><span class="sxs-lookup"><span data-stu-id="42b2e-118">Metrics that are included in the Power BI content</span></span>
<span data-ttu-id="42b2e-119">ชุดเนื้อหา Power BI เกี่ยวกับ **การวิเคราะห์การซื้อและการใช้จ่าย** รวมรายงานที่ประกอบด้วยชุดของเมตริก</span><span class="sxs-lookup"><span data-stu-id="42b2e-119">The **Purchase spend analysis** Power BI content includes a report that consists of a set of metrics.</span></span> <span data-ttu-id="42b2e-120">เมตริกเหล่านี้จะถูกแสดงภาพข้อมูลโดยเป็นแผนภูมิ ไทล์ และตาราง</span><span class="sxs-lookup"><span data-stu-id="42b2e-120">These metrics are visualized as charts, tiles, and tables.</span></span> 

<span data-ttu-id="42b2e-121">ส่วนต่อไปนี้จะแสดงภาพรวมของการแสดงภาพ</span><span class="sxs-lookup"><span data-stu-id="42b2e-121">The following sections provide an overview of the visualizations.</span></span>

### <a name="purchase-by-vendor-report-page"></a><span data-ttu-id="42b2e-122">การซื้อโดยเรียงตามหน้ารายงานของผู้จัดจำหน่าย</span><span class="sxs-lookup"><span data-stu-id="42b2e-122">Purchase by vendor report page</span></span>
<span data-ttu-id="42b2e-123">**แผนภูมิ**</span><span class="sxs-lookup"><span data-stu-id="42b2e-123">**Charts**</span></span>
- <span data-ttu-id="42b2e-124">ผู้จัดจำหน่าย 10 อันดับแรกโดยเรียงตามการซื้อ (แผนภูมิแท่งแบบเรียงซ้อน)</span><span class="sxs-lookup"><span data-stu-id="42b2e-124">Top 10 vendors by purchase (stacked bar chart)</span></span>
- <span data-ttu-id="42b2e-125">ยอดรวมการซื้อโดยเรียงตามกลุ่มผู้จัดจำหน่าย / ประเทศ / ชื่อ (แผนภูมิวงกลม)</span><span class="sxs-lookup"><span data-stu-id="42b2e-125">Total purchase by vendor group / country / name (pie chart)</span></span>
- <span data-ttu-id="42b2e-126">การซื้อโดยเรียงตามกลุ่มผู้จัดจำหน่าย / ประเทศ / ชื่อ (แผนภูมิคอลัมน์)</span><span class="sxs-lookup"><span data-stu-id="42b2e-126">Purchase by vendor group / country / name (column chart)</span></span>
- <span data-ttu-id="42b2e-127">การซื้อเฉลี่ยโดยเรียงตามกลุ่มผู้จัดจำหน่าย / ประเทศ / ชื่อ (แผนภูมิคอลัมน์)</span><span class="sxs-lookup"><span data-stu-id="42b2e-127">Average purchase by vendor group / country / name (column chart)</span></span>

<span data-ttu-id="42b2e-128">**ไทล์**</span><span class="sxs-lookup"><span data-stu-id="42b2e-128">**Tiles**</span></span>
- <span data-ttu-id="42b2e-129">การซื้อรวม</span><span class="sxs-lookup"><span data-stu-id="42b2e-129">Total purchase</span></span>
- <span data-ttu-id="42b2e-130">การเติบโตการซื้อ YOY</span><span class="sxs-lookup"><span data-stu-id="42b2e-130">YOY purchase growth</span></span>
- <span data-ttu-id="42b2e-131"># ผู้จัดจำหน่ายรวม</span><span class="sxs-lookup"><span data-stu-id="42b2e-131">Total # vendors</span></span>
- <span data-ttu-id="42b2e-132"># ผู้จัดจำหน่ายที่ใช้งานอยู่รวม</span><span class="sxs-lookup"><span data-stu-id="42b2e-132">Total # of active vendors</span></span>

<span data-ttu-id="42b2e-133">**ตัวอย่าง**</span><span class="sxs-lookup"><span data-stu-id="42b2e-133">**Example**</span></span>
<img src="media/spend1.png" alt="Purchase by vendor">

### <a name="purchase-by-product-report-page"></a><span data-ttu-id="42b2e-134">การซื้อโดยเรียงตามหน้ารายงานของผลิตภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="42b2e-134">Purchase by product report page</span></span>

<span data-ttu-id="42b2e-135">**แผนภูมิ**</span><span class="sxs-lookup"><span data-stu-id="42b2e-135">**Charts**</span></span>
- <span data-ttu-id="42b2e-136">การซื้อโดยเรียงตามประเภทการจัดซื้อ / ชื่อผลิตภัณฑ์ (แผนภูมิคอลัมน์)</span><span class="sxs-lookup"><span data-stu-id="42b2e-136">Purchase by procurement category / product name (column chart)</span></span>
- <span data-ttu-id="42b2e-137">ยอดการซื้อโดยเรียงตามประเภทการจัดซื้อ / ชื่อผลิตภัณฑ์ (แผนภูมิวงกลม)</span><span class="sxs-lookup"><span data-stu-id="42b2e-137">Total purchase by procurement category / product name (pie chart)</span></span>
- <span data-ttu-id="42b2e-138">ผลิตภัณฑ์ 10 อันดับแรกโดยเรียงตามการซื้อ (แผนภูมิแท่งแบบเรียงซ้อน)</span><span class="sxs-lookup"><span data-stu-id="42b2e-138">Top 10 products by purchase (stacked bar chart)</span></span>

<span data-ttu-id="42b2e-139">**ไทล์**</span><span class="sxs-lookup"><span data-stu-id="42b2e-139">**Tiles**</span></span>
- <span data-ttu-id="42b2e-140"># ผลิตภัณฑ์รวม</span><span class="sxs-lookup"><span data-stu-id="42b2e-140">Total # of products</span></span></li>
- <span data-ttu-id="42b2e-141">เปอร์เซ็นต์ของผลิตภัณฑ์ที่ใช้งานอยู่ทั้งหมดของ # ผลิตภัณฑ์รวม</span><span class="sxs-lookup"><span data-stu-id="42b2e-141">Total active products percentage of total # of products</span></span>
- <span data-ttu-id="42b2e-142">จำนวนของผลิตภัณฑ์ที่ลงบัญชีสำหรับการซื้อ 80%</span><span class="sxs-lookup"><span data-stu-id="42b2e-142">Number of products accounting for 80% purchase</span></span>

<span data-ttu-id="42b2e-143">**ตัวอย่าง**</span><span class="sxs-lookup"><span data-stu-id="42b2e-143">**Example**</span></span>


<img src="media/purchaseByProduct.png" alt="Purchase by Product">

### <a name="purchase-by-period-report-page"></a><span data-ttu-id="42b2e-144">การซื้อโดยเรียงตามหน้ารายงานของรอบระยะเวลา</span><span class="sxs-lookup"><span data-stu-id="42b2e-144">Purchase by period report page</span></span>
<span data-ttu-id="42b2e-145">หน้านี้แสดงการซื้อปีนี้และปีที่แล้ว และการเติบโตโดยเรียงตามประเภทการจัดซื้อ</span><span class="sxs-lookup"><span data-stu-id="42b2e-145">This page shows purchases this year and last year, and growth by procurement category.</span></span>

<span data-ttu-id="42b2e-146">**แผนภูมิ**</span><span class="sxs-lookup"><span data-stu-id="42b2e-146">**Charts**</span></span> 
- <span data-ttu-id="42b2e-147">การซื้อโดยเรียงตามเดือน / วัน (แผนภูมิคอลัมน์)</span><span class="sxs-lookup"><span data-stu-id="42b2e-147">Purchase by month / day (column chart)</span></span>
- <span data-ttu-id="42b2e-148">ค่าความแปรปรวน YOY การซื้อสะสม (แผนภูมิน้ำตก)</span><span class="sxs-lookup"><span data-stu-id="42b2e-148">Cumulative purchase YOY variance (waterfall chart)</span></span>
- <span data-ttu-id="42b2e-149">การเติบโต YOY การซื้อรวม (แผนภูมิคอลัมน์)</span><span class="sxs-lookup"><span data-stu-id="42b2e-149">Total purchase YOY growth (column chart)</span></span>
- <span data-ttu-id="42b2e-150">รายงานการจัดซื้อ (เมทริกซ์)</span><span class="sxs-lookup"><span data-stu-id="42b2e-150">Procurement statement (matrix)</span></span>

<span data-ttu-id="42b2e-151">**ไทล์**</span><span class="sxs-lookup"><span data-stu-id="42b2e-151">**Tiles**</span></span>
- <span data-ttu-id="42b2e-152">การเติบโตการซื้อ YOY</span><span class="sxs-lookup"><span data-stu-id="42b2e-152">YOY purchase growth</span></span>
- <span data-ttu-id="42b2e-153">% การเติบโตการซื้อ YOY</span><span class="sxs-lookup"><span data-stu-id="42b2e-153">YOY purchase growth %</span></span>

<span data-ttu-id="42b2e-154">**ตัวอย่าง**</span><span class="sxs-lookup"><span data-stu-id="42b2e-154">**Example**</span></span>
<img src="media/purchaseByPeriod.png" alt="Purchase by Period">

### <a name="purchase-by-vendor-location-report-page"></a><span data-ttu-id="42b2e-155">การซื้อโดยเรียงตามหน้ารายงานของสถานที่ของผู้จัดจำหน่าย</span><span class="sxs-lookup"><span data-stu-id="42b2e-155">Purchase by vendor location report page</span></span>

<span data-ttu-id="42b2e-156">**แผนภูมิ**</span><span class="sxs-lookup"><span data-stu-id="42b2e-156">**Charts**</span></span>
- <span data-ttu-id="42b2e-157">การซื้อโดยเรียงตามเมือง</span><span class="sxs-lookup"><span data-stu-id="42b2e-157">Purchase by city</span></span>
- <span data-ttu-id="42b2e-158">% การเติบโต YOY การซื้อ</span><span class="sxs-lookup"><span data-stu-id="42b2e-158">Purchase YOY growth %</span></span>
- <span data-ttu-id="42b2e-159">การซื้อโดยเรียงตามประเทศ</span><span class="sxs-lookup"><span data-stu-id="42b2e-159">Purchase by country</span></span>

<span data-ttu-id="42b2e-160">**ตัวอย่าง**</span><span class="sxs-lookup"><span data-stu-id="42b2e-160">**Example**</span></span>
<img src="media/purchByVendorLocation.png" alt="Purchase by Vendor Location">

### <a name="purchase-spend-analysis-by-time-report-page"></a><span data-ttu-id="42b2e-161">การวิเคราะห์การใช้จ่ายในการซื้อโดยเรียงตามหน้ารายงานเวลา</span><span class="sxs-lookup"><span data-stu-id="42b2e-161">Purchase spend analysis by time report page</span></span>

<span data-ttu-id="42b2e-162">**แผนภูมิ**</span><span class="sxs-lookup"><span data-stu-id="42b2e-162">**Charts**</span></span> 
- <span data-ttu-id="42b2e-163">การซื้อตั้งแต่ปีปัจจุบันโดยเรียงตามเดือน / วัน (แผนภูมิเส้น)</span><span class="sxs-lookup"><span data-stu-id="42b2e-163">Purchase current year by month / day (line chart)</span></span>
- <span data-ttu-id="42b2e-164">การซื้อปัจจุบันและปีที่แล้ว (แผนภูมิคอลัมน์และเส้น)</span><span class="sxs-lookup"><span data-stu-id="42b2e-164">Purchase current and last year (line and column chart)</span></span>

<span data-ttu-id="42b2e-165">**ตัวอย่าง**</span><span class="sxs-lookup"><span data-stu-id="42b2e-165">**Example**</span></span>
<img src="media/PurchByTIme.png" alt="Purchase by Time">

### <a name="purchase-spend-analysis-by-vendor-report-page"></a><span data-ttu-id="42b2e-166">การวิเคราะห์การใช้จ่ายในการซื้อโดยเรียงตามหน้ารายงานของผู้จัดจำหน่าย</span><span class="sxs-lookup"><span data-stu-id="42b2e-166">Purchase spend analysis by vendor report page</span></span>

<span data-ttu-id="42b2e-167">**แผนภูมิ**</span><span class="sxs-lookup"><span data-stu-id="42b2e-167">**Charts**</span></span> 
- <span data-ttu-id="42b2e-168">% การซื้อของผู้จัดจำหน่าย 10 อันดับแรกของการซื้อ (กรวย)</span><span class="sxs-lookup"><span data-stu-id="42b2e-168">Top 10 vendor purchase % of purchase (funnel)</span></span>
- <span data-ttu-id="42b2e-169">ผู้จัดจำหน่าย 10 อันดับแรกที่มี YOY การใช้จ่ายที่เพิ่มขึ้น</span><span class="sxs-lookup"><span data-stu-id="42b2e-169">Top 10 vendors with increased spending YOY</span></span>
- <span data-ttu-id="42b2e-170">ผู้จัดจำหน่าย 10 อันดับแรกที่มี YOY การใช้จ่ายที่ลดลง</span><span class="sxs-lookup"><span data-stu-id="42b2e-170">Top 10 vendors with decreased spending YOY</span></span>

<span data-ttu-id="42b2e-171">**ตัวอย่าง** 
</span><span class="sxs-lookup"><span data-stu-id="42b2e-171">**Example** 
</span></span><img src="media/PurchSpendAnalysisByVendor.png" alt="Purchase spend by vendor">


## <a name="data-model-and-entities"></a><span data-ttu-id="42b2e-172">แบบจำลองข้อมูลและเอนทิตี</span><span class="sxs-lookup"><span data-stu-id="42b2e-172">Data model and entities</span></span>
<span data-ttu-id="42b2e-173">ข้อมูลดังต่อไปนี้ถูกใช้ในการกรอกข้อมูลหน้ารายงานในเนื้อหา **การวิเคราะห์การซื้อและการใช้จ่าย** ใน Power BI</span><span class="sxs-lookup"><span data-stu-id="42b2e-173">The following data is used to fill the report pages in the **Purchase spend analysis** Power BI content.</span></span> <span data-ttu-id="42b2e-174">ข้อมูลนี้จะแสดงเป็นหน่วยวัดรวมที่มีการแบ่งระยะในที่จัดเก็บเอนทิตี้</span><span class="sxs-lookup"><span data-stu-id="42b2e-174">This data is represented as aggregate measurements that are staged in the Entity store.</span></span> <span data-ttu-id="42b2e-175">ที่จัดเก็บเอนทิตี้คือฐานข้อมูล Microsoft SQL Server ที่ได้รับการปรับให้เหมาะสมสำหรับการวิเคราะห์</span><span class="sxs-lookup"><span data-stu-id="42b2e-175">The Entity store is a Microsoft SQL Server database that is optimized for analytics.</span></span> <span data-ttu-id="42b2e-176">สำหรับข้อมูลเพิ่มเติม ดู [การรวม Power BI กับร้านค้าเอนทิตี](power-bi-integration-entity-store.md)</span><span class="sxs-lookup"><span data-stu-id="42b2e-176">For more information, see [Power BI integration with Entity store](power-bi-integration-entity-store.md).</span></span>

<span data-ttu-id="42b2e-177">การวัดแบบรวมในชุดเนื้อหานี้คือชุดย่อยของการวัดแบบรวมที่พร้อมใช้งานในคิวบ์การขายใน Microsoft Dynamics AX 2012 และ Microsoft Dynamics AX 2012 R3</span><span class="sxs-lookup"><span data-stu-id="42b2e-177">The aggregate measurements in this content are the subset of aggregate measurements that were available in the Purchase Cube in Microsoft Dynamics AX 2012 and Microsoft Dynamics AX 2012 R3.</span></span> <span data-ttu-id="42b2e-178">เมื่อต้องการแบ่งระยะของการวัดแบบรวมของ Cube ในร้านค้าเอนทิตี คุณจะต้องทำให้สามารถปรับใช้ได้</span><span class="sxs-lookup"><span data-stu-id="42b2e-178">To stage the cube's aggregate measurements in the Entity store, you must make them deployable.</span></span> <span data-ttu-id="42b2e-179">สำหรับข้อมูลเพิ่มเติม ดูกระบวนการสำหรับการแบ่งระยะการวัดแบบรวมในร้านค้าเอนทิตีในการรวม [Power BI กับร้านค้าเอนทิตี](power-bi-integration-entity-store.md)</span><span class="sxs-lookup"><span data-stu-id="42b2e-179">For more information, see the procedure for staging aggregate measurements in the Entity store in [Power BI integration with Entity store](power-bi-integration-entity-store.md).</span></span> <span data-ttu-id="42b2e-180">การวัดแบบรวมหลักต่อไปนี้จะพร้อมใช้งานได้โดยตรงจากเอนทิตีในบรรทัดใบแจ้งหนี้และจะถูกใช้เป็นข้อมูลพื้นฐานของเนื้อหา</span><span class="sxs-lookup"><span data-stu-id="42b2e-180">The following key aggregate measurements are available directly from the Invoice lines entity and are used as the basis of the content.</span></span>

| <span data-ttu-id="42b2e-181">เอนทิตี้</span><span class="sxs-lookup"><span data-stu-id="42b2e-181">Entity</span></span>        | <span data-ttu-id="42b2e-182">การวัดแบบรวมหลัก</span><span class="sxs-lookup"><span data-stu-id="42b2e-182">Key aggregate measurements</span></span> | <span data-ttu-id="42b2e-183">แหล่งข้อมูล</span><span class="sxs-lookup"><span data-stu-id="42b2e-183">Data source</span></span>                                 | <span data-ttu-id="42b2e-184">ฟิลด์</span><span class="sxs-lookup"><span data-stu-id="42b2e-184">Field</span></span>              | <span data-ttu-id="42b2e-185">คำอธิบาย</span><span class="sxs-lookup"><span data-stu-id="42b2e-185">Description</span></span>                            |
|---------------|----------------------------|---------------------------------------------|--------------------|----------------------------------------|
| <span data-ttu-id="42b2e-186">รายการในใบแจ้งหนี้</span><span class="sxs-lookup"><span data-stu-id="42b2e-186">Invoice lines</span></span> | <span data-ttu-id="42b2e-187">การซื้อ</span><span class="sxs-lookup"><span data-stu-id="42b2e-187">Purchase</span></span>                   | <span data-ttu-id="42b2e-188">VendInvoiceTrans</span><span class="sxs-lookup"><span data-stu-id="42b2e-188">VendInvoiceTrans</span></span>                            | <span data-ttu-id="42b2e-189">SUM(LineAmountMST)</span><span class="sxs-lookup"><span data-stu-id="42b2e-189">SUM(LineAmountMST)</span></span> | <span data-ttu-id="42b2e-190">ยอดเงินในสกุลเงินทางบัญชี</span><span class="sxs-lookup"><span data-stu-id="42b2e-190">The amount in the accounting currency.</span></span> |

<span data-ttu-id="42b2e-191">ตารางต่อไปนี้แสดงถึงการวัดหลักที่ถูกคำนวณในเนื้อหาที่คำนวณจากเอนทิตีในบรรทัดใบแจ้งหนี้</span><span class="sxs-lookup"><span data-stu-id="42b2e-191">The following table shows the key measurements in the content that are calculated from the Invoice lines entity.</span></span>

| <span data-ttu-id="42b2e-192">การประเมิน</span><span class="sxs-lookup"><span data-stu-id="42b2e-192">Measure</span></span>               | <span data-ttu-id="42b2e-193">การคำนวณ</span><span class="sxs-lookup"><span data-stu-id="42b2e-193">Calculation</span></span>                                                                                         |
|-----------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="42b2e-194">การซื้อปีปัจจุบัน</span><span class="sxs-lookup"><span data-stu-id="42b2e-194">Purchase current year</span></span> | <span data-ttu-id="42b2e-195">การซื้อปีปัจจุบัน = SUM('Invoice lines'\[Purchase\])</span><span class="sxs-lookup"><span data-stu-id="42b2e-195">Purchase current year = SUM('Invoice lines'\[Purchase\])</span></span>                                            |
| <span data-ttu-id="42b2e-196">การซื้อปีที่แล้ว</span><span class="sxs-lookup"><span data-stu-id="42b2e-196">Purchase last year</span></span>    | <span data-ttu-id="42b2e-197">การซื้อปีที่แล้ว = CALCULATE(SUM('Invoice lines'\[Purchase\]), SAMEPERIODLASTYEAR(Dates\[Date\]))</span><span class="sxs-lookup"><span data-stu-id="42b2e-197">Purchase last year = CALCULATE(SUM('Invoice lines'\[Purchase\]), SAMEPERIODLASTYEAR(Dates\[Date\]))</span></span> |
| <span data-ttu-id="42b2e-198">การเติบโตการซื้อ YOY</span><span class="sxs-lookup"><span data-stu-id="42b2e-198">YOY purchase growth</span></span>   | <span data-ttu-id="42b2e-199">การเติบโตการซื้อ YOY = \[Purchase current year\] – \[Purchase last year\]</span><span class="sxs-lookup"><span data-stu-id="42b2e-199">YOY purchase growth = \[Purchase current year\] – \[Purchase last year\]</span></span>                            |

<span data-ttu-id="42b2e-200">มิติหลักในเนื้อหาต่อไปนี้จะถูกใช้เป็นตัวกรองเพื่อแบ่งส่วนการวัดแบบรวม เพื่อให้คุณสามารถได้รับส่วนประกอบที่มากขึ้นและได้รับข้อมูลเชิงลึกเชิงวิเคราะห์ที่ละเอียดมากขึ้น</span><span class="sxs-lookup"><span data-stu-id="42b2e-200">The following key dimensions in the content are used as filters to slice the aggregate measurements, so that you can achieve more granularity and gain deeper analytical insights.</span></span>

| <span data-ttu-id="42b2e-201">เอนทิตี้</span><span class="sxs-lookup"><span data-stu-id="42b2e-201">Entity</span></span>                 | <span data-ttu-id="42b2e-202">ตัวอย่างของแอตทริบิวต์</span><span class="sxs-lookup"><span data-stu-id="42b2e-202">Examples of attributes</span></span>                                |
|------------------------|-------------------------------------------------------|
| <span data-ttu-id="42b2e-203">ผู้จัดจำหน่าย</span><span class="sxs-lookup"><span data-stu-id="42b2e-203">Vendors</span></span>                | <span data-ttu-id="42b2e-204">กลุ่มผู้จัดจำหน่าย ประเทศหรือภูมิภาคของผู้จัดจำหน่าย ชื่อผู้จัดจำหน่าย</span><span class="sxs-lookup"><span data-stu-id="42b2e-204">Vendor groups, Vendor country or regions, Vendor name</span></span> |
| <span data-ttu-id="42b2e-205">ผลิตภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="42b2e-205">Products</span></span>               | <span data-ttu-id="42b2e-206">หมายเลขผลิตภัณฑ์ ชื่อผลิตภัณฑ์ ชื่อกลุ่มสินค้า</span><span class="sxs-lookup"><span data-stu-id="42b2e-206">Product number, Product name, Item groups name</span></span>        |
| <span data-ttu-id="42b2e-207">ประเภทการจัดซื้อ</span><span class="sxs-lookup"><span data-stu-id="42b2e-207">Procurement categories</span></span> | <span data-ttu-id="42b2e-208">ประเภทการจัดซื้อ ชื่อประเภทการจัดซื้อ</span><span class="sxs-lookup"><span data-stu-id="42b2e-208">Procurement category, Procurement category names</span></span>      |
| <span data-ttu-id="42b2e-209">นิติบุคคล</span><span class="sxs-lookup"><span data-stu-id="42b2e-209">Legal entities</span></span>         | <span data-ttu-id="42b2e-210">ชื่อนิติบุคคล</span><span class="sxs-lookup"><span data-stu-id="42b2e-210">Legal entity name</span></span>                                     |
| <span data-ttu-id="42b2e-211">วันที่</span><span class="sxs-lookup"><span data-stu-id="42b2e-211">Dates</span></span>                  | <span data-ttu-id="42b2e-212">วันที่ ออฟเซ็ตของปี</span><span class="sxs-lookup"><span data-stu-id="42b2e-212">Dates, Year offset</span></span>                                    |

<span data-ttu-id="42b2e-213">โดยค่าเริ่มต้น เนื้อหาจะแสดงข้อมูลสำหรับปีปฏิทินปัจจุบัน</span><span class="sxs-lookup"><span data-stu-id="42b2e-213">By default, the content shows data for the current calendar year.</span></span> <span data-ttu-id="42b2e-214">อย่างไรก็ตาม คุณสามารถเปลี่ยนตัวกรองวันที่ในส่วนตัวกรองรายงาน</span><span class="sxs-lookup"><span data-stu-id="42b2e-214">However, you can change the date filter in the report filters section.</span></span> <span data-ttu-id="42b2e-215">นอกจากนี้คุณยังสามารถเปลี่ยนตัวกรองของบริษัท</span><span class="sxs-lookup"><span data-stu-id="42b2e-215">You can also change the company filter.</span></span>
