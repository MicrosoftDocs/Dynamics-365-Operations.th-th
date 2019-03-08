---
title: เนื้อหา Power BI เกี่ยวกับการวิเคราะห์การซื้อและการใช้จ่าย
description: หัวข้อนี้อธิบายถึงสิ่งที่จะรวมอยู่ในเนื้อหา Power BI เกี่ยวกับการวิเคราะห์การซื้อและการใช้จ่าย และยังอธิบายถึงวิธีการเข้าถึงรายงานที่รวมอยู่ในชุดเนื้อหานี้ และแสดงข้อมูลเกี่ยวกับแบบจำลองข้อมูลและเอนทิตี้ที่ใช้ในการสร้างชุดเนื้อหานี้
author: FrankDahl
manager: AnnBe
ms.date: 12/18/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: PurchaseSpendAnalysisPowerBI
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.custom: 265434
ms.assetid: 3cd9dfce-2687-4303-bc78-349e7cb5ea75
ms.search.region: global
ms.author: fdahl
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 069c4dc21959ab603ba6ca3da0ac68ef20325265
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 01/29/2019
ms.locfileid: "313853"
---
# <a name="purchase-spend-analysis-power-bi-content"></a><span data-ttu-id="7c143-104">เนื้อหา Power BI เกี่ยวกับการวิเคราะห์การซื้อและการใช้จ่าย</span><span class="sxs-lookup"><span data-stu-id="7c143-104">Purchase spend analysis Power BI content</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="7c143-105">หัวข้อนี้อธิบายถึงสิ่งที่จะรวมอยู่ในเนื้อหา Microsoft Power BI เกี่ยวกับ **การวิเคราะห์การซื้อและการใช้จ่าย**</span><span class="sxs-lookup"><span data-stu-id="7c143-105">This topic describes what is included in the **Purchase spend analysis** Microsoft Power BI content.</span></span> <span data-ttu-id="7c143-106">และยังอธิบายถึงวิธีการเข้าถึงรายงาน Power BI และแสดงข้อมูลเกี่ยวกับแบบจำลองข้อมูลและเอนทิตี้ที่ใช้ในการสร้างเนื้อหานี้</span><span class="sxs-lookup"><span data-stu-id="7c143-106">It explains how to access the Power BI reports, and provides information about the data model and entities that are used to build the content.</span></span>

## <a name="overview"></a><span data-ttu-id="7c143-107">ภาพรวม</span><span class="sxs-lookup"><span data-stu-id="7c143-107">Overview</span></span>

<span data-ttu-id="7c143-108">เนื้อหา Power BI **การวิเคราะห์การซื้อและการใช้จ่าย** ถูกออกแบบมาเพื่อช่วยให้ผู้จัดการฝ่ายจัดซื้อและผู้จัดการที่รับผิดชอบสำหรับงบประมาณเฝ้าระวังในการซื้อและการใช้จ่าย</span><span class="sxs-lookup"><span data-stu-id="7c143-108">The **Purchase spend analysis** Power BI content was designed to help purchasing managers and managers who are responsible for budgets keep an eye on purchase spending.</span></span> <span data-ttu-id="7c143-109">ผู้จัดการสามารถวิเคราะห์การซื้อและการใช้จ่ายโดยใช้วิธีต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="7c143-109">Managers can analyze purchase spending in the following ways:</span></span>

- <span data-ttu-id="7c143-110">การซื้อตั้งแต่ต้นปีจนถึงปัจจุบัน (โดยเรียงตามกลุ่มผู้จัดจำหน่ายและแต่ละผู้จัดจำหน่าย ประเภทการจัดซื้อและแต่ละผลิตภัณฑ์ และที่ตั้งของผู้จัดจำหน่าย)</span><span class="sxs-lookup"><span data-stu-id="7c143-110">Year-to-date purchase (by vendor group and individual vendors, procurement category and individual products, and vendor location)</span></span>
- <span data-ttu-id="7c143-111">การเปลี่ยนแปลงการซื้อตั้งแต่ต้นปีจนถึงปัจจุบัน (โดยเรียงตามกลุ่มผู้จัดจำหน่ายและประเภทการจัดซื้อ)</span><span class="sxs-lookup"><span data-stu-id="7c143-111">Year-over-year purchase change (by vendor group and procurement category)</span></span>

<span data-ttu-id="7c143-112">เนื้อหานี้ใช้ข้อมูลเกี่ยวกับธุรกรรมการซื้อ และให้ทั้งมุมมองรวมของตัวเลขการซื้อของทั้งบริษัทและการแบ่งรายละเอียดของการซื้อและการใช้จ่ายโดยเรียงตามผู้จัดจำหน่ายและผลิตภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="7c143-112">The content uses purchase transactional data, and provides both an aggregate view of the company-wide purchase figures and a breakdown of purchase spending by vendor and product.</span></span> <span data-ttu-id="7c143-113">รายงานเน้นการเปลี่ยนแปลงในการซื้อและการใช้จ่ายเมื่อเวลาผ่านไป</span><span class="sxs-lookup"><span data-stu-id="7c143-113">Reports highlight changes in purchase spending over time.</span></span> <span data-ttu-id="7c143-114">ดังนั้น สามารถใช้การรายงานเพื่อจัดการการแจ้งเตือนเกี่ยวกับแนวโน้มการใช้จ่ายค่าบวกและค่าลบสำหรับแต่ละผู้จัดจำหน่ายและผลิตภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="7c143-114">Therefore, the reports can be used to alert managers about positive and negative spending trends for individual vendors and products.</span></span> <span data-ttu-id="7c143-115">นอกจากนี้ แผนภูมิแสดงการซื้อและการใช้จ่ายสำหรับประเภทการจัดซื้อและกลุ่มผู้จัดจำหน่ายที่แตกต่างกัน</span><span class="sxs-lookup"><span data-stu-id="7c143-115">Additionally, charts show purchase spending for different procurement categories and vendor groups.</span></span> <span data-ttu-id="7c143-116">ดังนั้น ประเภทและผู้จัดการภูมิภาคสามารถใช้แผนภูมิเหล่านี้เพื่อช่วยในการระบุการเปลี่ยนแปลงลักษณะการใช้จ่าย</span><span class="sxs-lookup"><span data-stu-id="7c143-116">Therefore, category and regional managers can use the charts to help identify changes in spending behavior.</span></span>

## <a name="accessing-the-power-bi-content"></a><span data-ttu-id="7c143-117">การเข้าถึงเนื้อหา Power BI</span><span class="sxs-lookup"><span data-stu-id="7c143-117">Accessing the Power BI content</span></span>
<span data-ttu-id="7c143-118">เนื้อหา Power BI เกี่ยวกับ **การวิเคราะห์การซื้อและการใช้จ่าย** จะแสดงบนหน้า **การวิเคราะห์การซื้อและการใช้จ่าย** (**การจัดซื้อและการจัดหา** \> **การสอบถามและรายงาน** \> **การวิเคราะห์ประสิทธิภาพซื้อ** \> **การวิเคราะห์การซื้อและการใช้จ่าย**)</span><span class="sxs-lookup"><span data-stu-id="7c143-118">The **Purchase spend analysis** Power BI content is shown on the **Purchase and spend analysis** page (**Procurement and sourcing** \> **Inquiries and reports** \> **Purchase performance analysis** \> **Purchase and spend analysis**).</span></span>

## <a name="metrics-that-are-included-in-the-power-bi-content"></a><span data-ttu-id="7c143-119">เมตริกที่รวมอยู่ในชุดเนื้อหา Power BI</span><span class="sxs-lookup"><span data-stu-id="7c143-119">Metrics that are included in the Power BI content</span></span>
<span data-ttu-id="7c143-120">ชุดเนื้อหา Power BI เกี่ยวกับ **การวิเคราะห์การซื้อและการใช้จ่าย** รวมรายงานที่ประกอบด้วยชุดของเมตริก</span><span class="sxs-lookup"><span data-stu-id="7c143-120">The **Purchase spend analysis** Power BI content includes a report that consists of a set of metrics.</span></span> <span data-ttu-id="7c143-121">เมตริกเหล่านี้จะถูกแสดงภาพข้อมูลโดยเป็นแผนภูมิ ไทล์ และตาราง</span><span class="sxs-lookup"><span data-stu-id="7c143-121">These metrics are visualized as charts, tiles, and tables.</span></span> <span data-ttu-id="7c143-122">ตารางต่อไปนี้จะแสดงภาพรวมของการแสดงภาพ</span><span class="sxs-lookup"><span data-stu-id="7c143-122">The following table provides an overview of the visualizations.</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="7c143-123">หน้ารายงาน</span><span class="sxs-lookup"><span data-stu-id="7c143-123">Report page</span></span></th>
<th><span data-ttu-id="7c143-124">แผนภูมิ</span><span class="sxs-lookup"><span data-stu-id="7c143-124">Charts</span></span></th>
<th><span data-ttu-id="7c143-125">ไทล์</span><span class="sxs-lookup"><span data-stu-id="7c143-125">Tiles</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="7c143-126">การซื้อโดยเรียงตามผู้จัดจำหน่าย</span><span class="sxs-lookup"><span data-stu-id="7c143-126">Purchase by vendor</span></span></td>
<td><ul>
<li><span data-ttu-id="7c143-127">ผู้จัดจำหน่าย 10 อันดับแรกโดยเรียงตามการซื้อ (แผนภูมิแท่งแบบเรียงซ้อน)</span><span class="sxs-lookup"><span data-stu-id="7c143-127">Top 10 vendors by purchase (stacked bar chart)</span></span></li>
<li><span data-ttu-id="7c143-128">ยอดรวมการซื้อโดยเรียงตามกลุ่มผู้จัดจำหน่าย/ ประเทศ / ชื่อ (แผนภูมิวงกลม)</span><span class="sxs-lookup"><span data-stu-id="7c143-128">Total purchase by vendor group / country / name (pie chart)</span></span></li>
<li><span data-ttu-id="7c143-129">การซื้อโดยเรียงตามกลุ่มผู้จัดจำหน่าย/ ประเทศ / ชื่อ (แผนภูมิคอลัมน์)</span><span class="sxs-lookup"><span data-stu-id="7c143-129">Purchase by vendor group / country / name (column chart)</span></span></li>
<li><span data-ttu-id="7c143-130">การซื้อเฉลี่ยโดยเรียงตามกลุ่มผู้จัดจำหน่าย/ ประเทศ / ชื่อ (แผนภูมิคอลัมน์)</span><span class="sxs-lookup"><span data-stu-id="7c143-130">Average purchase by vendor group / country / name (column chart)</span></span></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="7c143-131">การซื้อรวม</span><span class="sxs-lookup"><span data-stu-id="7c143-131">Total purchase</span></span></li>
<li><span data-ttu-id="7c143-132">การเติบโตการซื้อ YOY</span><span class="sxs-lookup"><span data-stu-id="7c143-132">YOY purchase growth</span></span></li>
<li><span data-ttu-id="7c143-133"># ผู้จัดจำหน่ายรวม</span><span class="sxs-lookup"><span data-stu-id="7c143-133">Total # vendors</span></span></li>
<li><span data-ttu-id="7c143-134"># ผู้จัดจำหน่ายที่ใช้งานอยู่รวม</span><span class="sxs-lookup"><span data-stu-id="7c143-134">Total # of active vendors</span></span></li>
</ul></td>
</tr>
<tr>
<td><span data-ttu-id="7c143-135">การซื้อโดยเรียงตามผลิตภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="7c143-135">Purchase by product</span></span></td>
<td><ul>
<li><span data-ttu-id="7c143-136">การซื้อโดยเรียงตามประเภทการจัดซื้อ / ชื่อผลิตภัณฑ์ (แผนภูมิคอลัมน์)</span><span class="sxs-lookup"><span data-stu-id="7c143-136">Purchase by procurement category / product name (column chart)</span></span></li>
<li><span data-ttu-id="7c143-137">ยอดการซื้อโดยเรียงตามประเภทการจัดซื้อ / ชื่อผลิตภัณฑ์ (แผนภูมิวงกลม)</span><span class="sxs-lookup"><span data-stu-id="7c143-137">Total purchase by procurement category / product name (pie chart)</span></span></li>
<li><span data-ttu-id="7c143-138">ผลิตภัณฑ์ 10 อันดับแรกโดยเรียงตามการซื้อ (แผนภูมิแท่งแบบเรียงซ้อน)</span><span class="sxs-lookup"><span data-stu-id="7c143-138">Top 10 products by purchase (stacked bar chart)</span></span></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="7c143-139"># ผลิตภัณฑ์รวม</span><span class="sxs-lookup"><span data-stu-id="7c143-139">Total # of products</span></span></li>
<li><span data-ttu-id="7c143-140">เปอร์เซ็นต์ของผลิตภัณฑ์ที่ใช้งานอยู่ทั้งหมดของ # ผลิตภัณฑ์รวม</span><span class="sxs-lookup"><span data-stu-id="7c143-140">Total active products percentage of total # of products</span></span></li>
<li><span data-ttu-id="7c143-141">จำนวนของผลิตภัณฑ์ที่ลงบัญชีสำหรับการซื้อ 80%</span><span class="sxs-lookup"><span data-stu-id="7c143-141">Number of products accounting for 80% purchase</span></span></li>
</ul></td>
</tr>
<tr>
<td><span data-ttu-id="7c143-142">การซื้อโดยเรียงตามรอบระยะเวลา\*</span><span class="sxs-lookup"><span data-stu-id="7c143-142">Purchase by period\*</span></span></td>
<td><ul>
<li><span data-ttu-id="7c143-143">การซื้อโดยเรียงตามเดือน / วัน (แผนภูมิคอลัมน์)</span><span class="sxs-lookup"><span data-stu-id="7c143-143">Purchase by month / day (column chart)</span></span></li>
<li><span data-ttu-id="7c143-144">ค่าความแปรปรวน YOY การซื้อสะสม (แผนภูมิน้ำตก)</span><span class="sxs-lookup"><span data-stu-id="7c143-144">Cumulative purchase YOY variance (waterfall chart)</span></span></li>
<li><span data-ttu-id="7c143-145">การเติบโต YOY การซื้อรวม (แผนภูมิคอลัมน์)</span><span class="sxs-lookup"><span data-stu-id="7c143-145">Total purchase YOY growth (column chart)</span></span></li>
<li><span data-ttu-id="7c143-146">รายงานการจัดซื้อ (เมทริกซ์)</span><span class="sxs-lookup"><span data-stu-id="7c143-146">Procurement statement (matrix)</span></span></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="7c143-147">การเติบโตการซื้อ YOY</span><span class="sxs-lookup"><span data-stu-id="7c143-147">YOY purchase growth</span></span></li>
<li><span data-ttu-id="7c143-148">% การเติบโตการซื้อ YOY</span><span class="sxs-lookup"><span data-stu-id="7c143-148">YOY purchase growth %</span></span></li>
</ul></td>
</tr>
<tr>
<td><span data-ttu-id="7c143-149">การซื้อโดยเรียงตามที่ตั้งของผู้จัดจำหน่าย</span><span class="sxs-lookup"><span data-stu-id="7c143-149">Purchase by vendor location</span></span></td>
<td><ul>
<li><span data-ttu-id="7c143-150">การซื้อโดยเรียงตามเมือง</span><span class="sxs-lookup"><span data-stu-id="7c143-150">Purchase by city</span></span></li>
<li><span data-ttu-id="7c143-151">% การเติบโต YOY การซื้อ</span><span class="sxs-lookup"><span data-stu-id="7c143-151">Purchase YOY growth %</span></span></li>
<li><span data-ttu-id="7c143-152">การซื้อโดยเรียงตามประเทศ</span><span class="sxs-lookup"><span data-stu-id="7c143-152">Purchase by country</span></span></li>
</ul></td>
<td></td>
</tr>
<tr>
<td><span data-ttu-id="7c143-153">การวิเคราะห์การซื้อและการใช้จ่ายโดยเรียงตามเวลา</span><span class="sxs-lookup"><span data-stu-id="7c143-153">Purchase spend analysis by time</span></span></td>
<td><ul>
<li><span data-ttu-id="7c143-154">การซื้อตั้งแต่ปีปัจจุบันโดยเรียงตามเดือน / วัน (แผนภูมิเส้น)</span><span class="sxs-lookup"><span data-stu-id="7c143-154">Purchase current year by month / day (line chart)</span></span></li>
<li><span data-ttu-id="7c143-155">การซื้อปัจจุบันและปีที่แล้ว (แผนภูมิคอลัมน์และเส้น)</span><span class="sxs-lookup"><span data-stu-id="7c143-155">Purchase current and last year (line and column chart)</span></span></li>
</ul></td>
<td></td>
</tr>
<tr>
<td><span data-ttu-id="7c143-156">การวิเคราะห์การซื้อและการใช้จ่ายโดยเรียงตามผู้จัดจำหน่าย</span><span class="sxs-lookup"><span data-stu-id="7c143-156">Purchase spend analysis by vendor</span></span></td>
<td><ul>
<li><span data-ttu-id="7c143-157">% การซื้อของผู้จัดจำหน่าย 10 อันดับแรกของการซื้อ (กรวย)</span><span class="sxs-lookup"><span data-stu-id="7c143-157">Top 10 vendor purchase % of purchase (funnel)</span></span></li>
<li><span data-ttu-id="7c143-158">ผู้จัดจำหน่าย 10 อันดับแรกที่มี YOY การใช้จ่ายที่เพิ่มขึ้น</span><span class="sxs-lookup"><span data-stu-id="7c143-158">Top 10 vendors with increased spending YOY</span></span></li>
<li><span data-ttu-id="7c143-159">ผู้จัดจำหน่าย 10 อันดับแรกที่มี YOY การใช้จ่ายที่ลดลง</span><span class="sxs-lookup"><span data-stu-id="7c143-159">Top 10 vendors with decreased spending YOY</span></span></li>
</ul></td>
<td></td>
</tr>
</tbody>
</table>

<span data-ttu-id="7c143-160">\* การซื้อปีนี้และปีที่แล้ว และการเติบโตโดยเรียงตามประเภทการจัดซื้อ</span><span class="sxs-lookup"><span data-stu-id="7c143-160">\* Purchase this year and last year, and growth by procurement category</span></span>

## <a name="data-model-and-entities"></a><span data-ttu-id="7c143-161">แบบจำลองข้อมูลและเอนทิตี</span><span class="sxs-lookup"><span data-stu-id="7c143-161">Data model and entities</span></span>
<span data-ttu-id="7c143-162">ข้อมูลดังต่อไปนี้ถูกใช้ในการกรอกข้อมูลหน้ารายงานในเนื้อหา **การวิเคราะห์การซื้อและการใช้จ่าย** ใน Power BI</span><span class="sxs-lookup"><span data-stu-id="7c143-162">The following data is used to fill the report pages in the **Purchase spend analysis** Power BI content.</span></span> <span data-ttu-id="7c143-163">ข้อมูลนี้จะแสดงเป็นหน่วยวัดรวมที่มีการแบ่งระยะในที่จัดเก็บเอนทิตี้</span><span class="sxs-lookup"><span data-stu-id="7c143-163">This data is represented as aggregate measurements that are staged in the Entity store.</span></span> <span data-ttu-id="7c143-164">ที่จัดเก็บเอนทิตี้คือฐานข้อมูล Microsoft SQL Server ที่ได้รับการปรับให้เหมาะสมสำหรับการวิเคราะห์</span><span class="sxs-lookup"><span data-stu-id="7c143-164">The Entity store is a Microsoft SQL Server database that is optimized for analytics.</span></span> <span data-ttu-id="7c143-165">สำหรับข้อมูลเพิ่มเติม ดู [ภาพรวมของการรวม Power BI กับร้านค้าเอนทิตี](power-bi-integration-entity-store.md)</span><span class="sxs-lookup"><span data-stu-id="7c143-165">For more information, see [Overview of Power BI integration with Entity store](power-bi-integration-entity-store.md).</span></span>

<span data-ttu-id="7c143-166">การวัดแบบรวมในชุดเนื้อหานี้คือชุดย่อยของการวัดแบบรวมที่พร้อมใช้งานในคิวบ์การขายใน Microsoft Dynamics AX 2012 และ Microsoft Dynamics AX 2012 R3</span><span class="sxs-lookup"><span data-stu-id="7c143-166">The aggregate measurements in this content are the subset of aggregate measurements that were available in the Purchase Cube in Microsoft Dynamics AX 2012 and Microsoft Dynamics AX 2012 R3.</span></span> <span data-ttu-id="7c143-167">เมื่อต้องการแบ่งระยะของการวัดแบบรวมของ Cube ในร้านค้าเอนทิตี คุณจะต้องทำให้สามารถปรับใช้ได้</span><span class="sxs-lookup"><span data-stu-id="7c143-167">To stage the cube's aggregate measurements in the Entity store, you must make them deployable.</span></span> <span data-ttu-id="7c143-168">สำหรับข้อมูลเพิ่มเติม ดูกระบวนการสำหรับการแบ่งระยะการวัดแบบรวมในร้านค้าเอนทิตีใน [ภาพรวม Power BI กับร้านค้าเอนทิตี](power-bi-integration-entity-store.md)</span><span class="sxs-lookup"><span data-stu-id="7c143-168">For more information, see the procedure for staging aggregate measurements in the Entity store in [Overview of Power BI integration with Entity store](power-bi-integration-entity-store.md).</span></span> <span data-ttu-id="7c143-169">การวัดแบบรวมหลักต่อไปนี้จะพร้อมใช้งานได้โดยตรงจากเอนทิตีในบรรทัดใบแจ้งหนี้และจะถูกใช้เป็นข้อมูลพื้นฐานของเนื้อหา</span><span class="sxs-lookup"><span data-stu-id="7c143-169">The following key aggregate measurements are available directly from the Invoice lines entity and are used as the basis of the content.</span></span>

| <span data-ttu-id="7c143-170">เอนทิตี้</span><span class="sxs-lookup"><span data-stu-id="7c143-170">Entity</span></span>        | <span data-ttu-id="7c143-171">การวัดแบบรวมหลัก</span><span class="sxs-lookup"><span data-stu-id="7c143-171">Key aggregate measurements</span></span> | <span data-ttu-id="7c143-172">แหล่งข้อมูล</span><span class="sxs-lookup"><span data-stu-id="7c143-172">Data source</span></span>                                 | <span data-ttu-id="7c143-173">ฟิลด์</span><span class="sxs-lookup"><span data-stu-id="7c143-173">Field</span></span>              | <span data-ttu-id="7c143-174">คำอธิบาย</span><span class="sxs-lookup"><span data-stu-id="7c143-174">Description</span></span>                            |
|---------------|----------------------------|---------------------------------------------|--------------------|----------------------------------------|
| <span data-ttu-id="7c143-175">รายการในใบแจ้งหนี้</span><span class="sxs-lookup"><span data-stu-id="7c143-175">Invoice lines</span></span> | <span data-ttu-id="7c143-176">การซื้อ</span><span class="sxs-lookup"><span data-stu-id="7c143-176">Purchase</span></span>                   | <span data-ttu-id="7c143-177">VendInvoiceTrans</span><span class="sxs-lookup"><span data-stu-id="7c143-177">VendInvoiceTrans</span></span>                            | <span data-ttu-id="7c143-178">SUM(LineAmountMST)</span><span class="sxs-lookup"><span data-stu-id="7c143-178">SUM(LineAmountMST)</span></span> | <span data-ttu-id="7c143-179">ยอดเงินในสกุลเงินทางบัญชี</span><span class="sxs-lookup"><span data-stu-id="7c143-179">The amount in the accounting currency.</span></span> |

<span data-ttu-id="7c143-180">ตารางต่อไปนี้แสดงถึงการวัดหลักที่ถูกคำนวณในเนื้อหาที่คำนวณจากเอนทิตีในบรรทัดใบแจ้งหนี้</span><span class="sxs-lookup"><span data-stu-id="7c143-180">The following table shows the key measurements in the content that are calculated from the Invoice lines entity.</span></span>

| <span data-ttu-id="7c143-181">การประเมิน</span><span class="sxs-lookup"><span data-stu-id="7c143-181">Measure</span></span>               | <span data-ttu-id="7c143-182">การคำนวณ</span><span class="sxs-lookup"><span data-stu-id="7c143-182">Calculation</span></span>                                                                                         |
|-----------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7c143-183">การซื้อปีปัจจุบัน</span><span class="sxs-lookup"><span data-stu-id="7c143-183">Purchase current year</span></span> | <span data-ttu-id="7c143-184">การซื้อปีปัจจุบัน = SUM('Invoice lines'\[Purchase\])</span><span class="sxs-lookup"><span data-stu-id="7c143-184">Purchase current year = SUM('Invoice lines'\[Purchase\])</span></span>                                            |
| <span data-ttu-id="7c143-185">การซื้อปีที่แล้ว</span><span class="sxs-lookup"><span data-stu-id="7c143-185">Purchase last year</span></span>    | <span data-ttu-id="7c143-186">การซื้อปีที่แล้ว = CALCULATE(SUM('Invoice lines'\[Purchase\]), SAMEPERIODLASTYEAR(Dates\[Date\]))</span><span class="sxs-lookup"><span data-stu-id="7c143-186">Purchase last year = CALCULATE(SUM('Invoice lines'\[Purchase\]), SAMEPERIODLASTYEAR(Dates\[Date\]))</span></span> |
| <span data-ttu-id="7c143-187">การเติบโตการซื้อ YOY</span><span class="sxs-lookup"><span data-stu-id="7c143-187">YOY purchase growth</span></span>   | <span data-ttu-id="7c143-188">การเติบโตการซื้อ YOY = \[Purchase current year\] – \[Purchase last year\]</span><span class="sxs-lookup"><span data-stu-id="7c143-188">YOY purchase growth = \[Purchase current year\] – \[Purchase last year\]</span></span>                            |

<span data-ttu-id="7c143-189">มิติหลักในเนื้อหาต่อไปนี้จะถูกใช้เป็นตัวกรองเพื่อแบ่งส่วนการวัดแบบรวม เพื่อให้คุณสามารถได้รับส่วนประกอบที่มากขึ้นและได้รับข้อมูลเชิงลึกเชิงวิเคราะห์ที่ละเอียดมากขึ้น</span><span class="sxs-lookup"><span data-stu-id="7c143-189">The following key dimensions in the content are used as filters to slice the aggregate measurements, so that you can achieve more granularity and gain deeper analytical insights.</span></span>

| <span data-ttu-id="7c143-190">เอนทิตี้</span><span class="sxs-lookup"><span data-stu-id="7c143-190">Entity</span></span>                 | <span data-ttu-id="7c143-191">ตัวอย่างของแอตทริบิวต์</span><span class="sxs-lookup"><span data-stu-id="7c143-191">Examples of attributes</span></span>                                |
|------------------------|-------------------------------------------------------|
| <span data-ttu-id="7c143-192">ผู้จัดจำหน่าย</span><span class="sxs-lookup"><span data-stu-id="7c143-192">Vendors</span></span>                | <span data-ttu-id="7c143-193">กลุ่มผู้จัดจำหน่าย ประเทศหรือภูมิภาคของผู้จัดจำหน่าย ชื่อผู้จัดจำหน่าย</span><span class="sxs-lookup"><span data-stu-id="7c143-193">Vendor groups, Vendor country or regions, Vendor name</span></span> |
| <span data-ttu-id="7c143-194">ผลิตภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="7c143-194">Products</span></span>               | <span data-ttu-id="7c143-195">หมายเลขผลิตภัณฑ์ ชื่อผลิตภัณฑ์ ชื่อกลุ่มสินค้า</span><span class="sxs-lookup"><span data-stu-id="7c143-195">Product number, Product name, Item groups name</span></span>        |
| <span data-ttu-id="7c143-196">ประเภทการจัดซื้อ</span><span class="sxs-lookup"><span data-stu-id="7c143-196">Procurement categories</span></span> | <span data-ttu-id="7c143-197">ประเภทการจัดซื้อ ชื่อประเภทการจัดซื้อ</span><span class="sxs-lookup"><span data-stu-id="7c143-197">Procurement category, Procurement category names</span></span>      |
| <span data-ttu-id="7c143-198">นิติบุคคล</span><span class="sxs-lookup"><span data-stu-id="7c143-198">Legal entities</span></span>         | <span data-ttu-id="7c143-199">ชื่อนิติบุคคล</span><span class="sxs-lookup"><span data-stu-id="7c143-199">Legal entity name</span></span>                                     |
| <span data-ttu-id="7c143-200">วันที่</span><span class="sxs-lookup"><span data-stu-id="7c143-200">Dates</span></span>                  | <span data-ttu-id="7c143-201">วันที่ ออฟเซ็ตของปี</span><span class="sxs-lookup"><span data-stu-id="7c143-201">Dates, Year offset</span></span>                                    |

<span data-ttu-id="7c143-202">โดยค่าเริ่มต้น เนื้อหาจะแสดงข้อมูลสำหรับปีปฏิทินปัจจุบัน</span><span class="sxs-lookup"><span data-stu-id="7c143-202">By default, the content shows data for the current calendar year.</span></span> <span data-ttu-id="7c143-203">อย่างไรก็ตาม คุณสามารถเปลี่ยนตัวกรองวันที่ในส่วนตัวกรองรายงาน</span><span class="sxs-lookup"><span data-stu-id="7c143-203">However, you can change the date filter in the report filters section.</span></span> <span data-ttu-id="7c143-204">นอกจากนี้คุณยังสามารถเปลี่ยนตัวกรองของบริษัท</span><span class="sxs-lookup"><span data-stu-id="7c143-204">You can also change the company filter.</span></span>
