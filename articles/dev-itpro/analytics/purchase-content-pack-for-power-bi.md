---
title: "เนื้อหาการวิเคราะห์การซื้อและการใช้จ่ายใน Power BI"
description: "หัวข้อนี้อธิบายถึงสิ่งที่จะรวมอยู่ในเนื้อหาการวิเคราะห์การซื้อและการใช้จ่ายใน Power BI และยังอธิบายถึงวิธีการเข้าถึงรายงานที่รวมอยู่ในชุดเนื้อหานี้ และแสดงข้อมูลเกี่ยวกับแบบจำลองข้อมูลและเอนทิตี้ที่ใช้ในการสร้างชุดเนื้อหานี้"
author: FrankDahl
manager: AnnBe
ms.date: 06/16/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.scope: Core, Operations, UnifiedOperations
ms.custom: 265434
ms.assetid: 3cd9dfce-2687-4303-bc78-349e7cb5ea75
ms.search.region: global
ms.author: fdahl
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 3e42746329b1194c0ce0e2fb5c476742259a5b43
ms.contentlocale: th-th
ms.lasthandoff: 09/29/2017

---

# <a name="purchase-spend-analysis-power-bi-content"></a><span data-ttu-id="98cb3-104">เนื้อหาการวิเคราะห์การซื้อและการใช้จ่ายใน Power BI</span><span class="sxs-lookup"><span data-stu-id="98cb3-104">Purchase spend analysis Power BI content</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="98cb3-105">หัวข้อนี้อธิบายถึงสิ่งที่จะรวมอยู่ในเนื้อหา Microsoft Power BI **การวิเคราะห์การซื้อและการใช้จ่าย**</span><span class="sxs-lookup"><span data-stu-id="98cb3-105">This topic describes what is included in the **Purchase spend analysis** Microsoft Power BI content.</span></span> <span data-ttu-id="98cb3-106">และยังอธิบายถึงวิธีการเข้าถึงรายงาน Power BI และแสดงข้อมูลเกี่ยวกับแบบจำลองข้อมูลและเอนทิตี้ที่ใช้ในการสร้างเนื้อหานี้</span><span class="sxs-lookup"><span data-stu-id="98cb3-106">It explains how to access the Power BI reports, and provides information about the data model and entities that are used to build the content.</span></span>

## <a name="overview"></a><span data-ttu-id="98cb3-107">ภาพรวม</span><span class="sxs-lookup"><span data-stu-id="98cb3-107">Overview</span></span>

<span data-ttu-id="98cb3-108">เนื้อหา Power BI **การวิเคราะห์การซื้อและการใช้จ่าย** ถูกออกแบบมาเพื่อช่วยให้ผู้จัดการฝ่ายจัดซื้อและผู้จัดการที่รับผิดชอบสำหรับงบประมาณเฝ้าระวังในการซื้อและการใช้จ่าย</span><span class="sxs-lookup"><span data-stu-id="98cb3-108">The **Purchase spend analysis** Power BI content was designed to help purchasing managers and managers who are responsible for budgets keep an eye on purchase spending.</span></span> <span data-ttu-id="98cb3-109">ผู้จัดการสามารถวิเคราะห์การซื้อและการใช้จ่ายโดยใช้วิธีต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="98cb3-109">Managers can analyze purchase spending in the following ways:</span></span>

-   <span data-ttu-id="98cb3-110">การซื้อตั้งแต่ต้นปีจนถึงปัจจุบัน (โดยเรียงตามกลุ่มผู้จัดจำหน่ายและแต่ละผู้จัดจำหน่าย ประเภทการจัดซื้อและแต่ละผลิตภัณฑ์ และที่ตั้งของผู้จัดจำหน่าย)</span><span class="sxs-lookup"><span data-stu-id="98cb3-110">Year-to-date purchase (by vendor group and individual vendors, procurement category and individual products, and vendor location)</span></span>
-   <span data-ttu-id="98cb3-111">การเปลี่ยนแปลงการซื้อตั้งแต่ต้นปีจนถึงปัจจุบัน (โดยเรียงตามกลุ่มผู้จัดจำหน่ายและประเภทการจัดซื้อ)</span><span class="sxs-lookup"><span data-stu-id="98cb3-111">Year-over-year purchase change (by vendor group and procurement category)</span></span>

<span data-ttu-id="98cb3-112">เนื้อหานี้ใช้ข้อมูลเกี่ยวกับธุรกรรมการซื้อ และให้ทั้งมุมมองรวมของตัวเลขการซื้อของทั้งบริษัทและการแบ่งรายละเอียดของการซื้อและการใช้จ่ายโดยเรียงตามผู้จัดจำหน่ายและผลิตภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="98cb3-112">The content uses purchase transactional data, and provides both an aggregate view of the company-wide purchase figures and a breakdown of purchase spending by vendor and product.</span></span> <span data-ttu-id="98cb3-113">รายงานเน้นการเปลี่ยนแปลงในการซื้อและการใช้จ่ายเมื่อเวลาผ่านไป</span><span class="sxs-lookup"><span data-stu-id="98cb3-113">Reports highlight changes in purchase spending over time.</span></span> <span data-ttu-id="98cb3-114">ดังนั้น สามารถใช้การรายงานเพื่อจัดการการแจ้งเตือนเกี่ยวกับแนวโน้มการใช้จ่ายค่าบวกและค่าลบสำหรับแต่ละผู้จัดจำหน่ายและผลิตภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="98cb3-114">Therefore, the reports can be used to alert managers about positive and negative spending trends for individual vendors and products.</span></span> <span data-ttu-id="98cb3-115">นอกจากนี้ แผนภูมิแสดงการซื้อและการใช้จ่ายสำหรับประเภทการจัดซื้อและกลุ่มผู้จัดจำหน่ายที่แตกต่างกัน</span><span class="sxs-lookup"><span data-stu-id="98cb3-115">Additionally, charts show purchase spending for different procurement categories and vendor groups.</span></span> <span data-ttu-id="98cb3-116">ดังนั้น ประเภทและผู้จัดการภูมิภาคสามารถใช้แผนภูมิเหล่านี้เพื่อช่วยในการระบุการเปลี่ยนแปลงลักษณะการใช้จ่าย</span><span class="sxs-lookup"><span data-stu-id="98cb3-116">Therefore, category and regional managers can use the charts to help identify changes in spending behavior.</span></span>

## <a name="accessing-the-power-bi-content"></a><span data-ttu-id="98cb3-117">การเข้าถึงเนื้อหา Power BI</span><span class="sxs-lookup"><span data-stu-id="98cb3-117">Accessing the Power BI content</span></span>
<span data-ttu-id="98cb3-118">ถ้าคุณกำลังใช้ Microsoft Dynamics 365 for Finance and Operations, Enterprise edition (กรกฎาคม 2017) เนื้อหา Power BI **การวิเคราะห์การซื้อและการใช้จ่าย** จะแสดงบนหน้า **การวิเคราะห์การซื้อและการใช้จ่าย** (**การจัดซื้อและการจัดหา** > **การสอบถามและรายงาน** > **การวิเคราะห์ประสิทธิภาพการซื้อ** > **การวิเคราะห์การซื้อและการใช้จ่าย**)</span><span class="sxs-lookup"><span data-stu-id="98cb3-118">If you're using Microsoft Dynamics 365 for Finance and Operations, Enterprise edition (July 2017), the **Purchase spend analysis** Power BI content is shown on the **Purchase and spend analysis** page (**Procurement and sourcing** > **Inquiries and reports** > **Purchase performance analysis** > **Purchase and spend analysis**).</span></span> 

## <a name="metrics-that-are-included-in-the-power-bi-content"></a><span data-ttu-id="98cb3-119">เมตริกที่รวมอยู่ในเนื้อหา Power BI</span><span class="sxs-lookup"><span data-stu-id="98cb3-119">Metrics that are included in the Power BI content</span></span>
<span data-ttu-id="98cb3-120">เนื้อหา Power BI **การวิเคราะห์การซื้อและการใช้จ่าย** ประกอบด้วยชุดของเมตริก</span><span class="sxs-lookup"><span data-stu-id="98cb3-120">The **Purchase spend analysis** Power BI content includes a report that consists of a set of metrics.</span></span> <span data-ttu-id="98cb3-121">เมตริกเหล่านี้จะถูกแสดงภาพข้อมูลโดยเป็นแผนภูมิ ไทล์ และตาราง</span><span class="sxs-lookup"><span data-stu-id="98cb3-121">These metrics are visualized as charts, tiles, and tables.</span></span> <span data-ttu-id="98cb3-122">ตารางต่อไปนี้จะแสดงภาพรวมของการแสดงภาพ</span><span class="sxs-lookup"><span data-stu-id="98cb3-122">The following table provides an overview of the visualizations.</span></span>

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="98cb3-123">หน้ารายงาน</span><span class="sxs-lookup"><span data-stu-id="98cb3-123">Report page</span></span></th>
<th><span data-ttu-id="98cb3-124">แผนภูมิ</span><span class="sxs-lookup"><span data-stu-id="98cb3-124">Charts</span></span></th>
<th><span data-ttu-id="98cb3-125">ไทล์</span><span class="sxs-lookup"><span data-stu-id="98cb3-125">Tiles</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="98cb3-126">การซื้อโดยเรียงตามผู้จัดจำหน่าย</span><span class="sxs-lookup"><span data-stu-id="98cb3-126">Purchase by vendor</span></span></td>
<td><ul>
<li><span data-ttu-id="98cb3-127">ผู้จัดจำหน่าย 10 อันดับแรกโดยเรียงตามการซื้อ (แผนภูมิแท่งแบบเรียงซ้อน)</span><span class="sxs-lookup"><span data-stu-id="98cb3-127">Top 10 vendors by purchase (stacked bar chart)</span></span></li>
<li><span data-ttu-id="98cb3-128">ยอดรวมการซื้อโดยเรียงตามกลุ่มผู้จัดจำหน่าย/ ประเทศ / ชื่อ (แผนภูมิวงกลม)</span><span class="sxs-lookup"><span data-stu-id="98cb3-128">Total purchase by vendor group / country / name (pie chart)</span></span></li>
<li><span data-ttu-id="98cb3-129">การซื้อโดยเรียงตามกลุ่มผู้จัดจำหน่าย/ ประเทศ / ชื่อ (แผนภูมิคอลัมน์)</span><span class="sxs-lookup"><span data-stu-id="98cb3-129">Purchase by vendor group / country / name (column chart)</span></span></li>
<li><span data-ttu-id="98cb3-130">การซื้อเฉลี่ยโดยเรียงตามกลุ่มผู้จัดจำหน่าย/ ประเทศ / ชื่อ (แผนภูมิคอลัมน์)</span><span class="sxs-lookup"><span data-stu-id="98cb3-130">Average purchase by vendor group / country / name (column chart)</span></span></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="98cb3-131">การซื้อรวม</span><span class="sxs-lookup"><span data-stu-id="98cb3-131">Total purchase</span></span></li>
<li><span data-ttu-id="98cb3-132">การเติบโตการซื้อ YOY</span><span class="sxs-lookup"><span data-stu-id="98cb3-132">YOY purchase growth</span></span></li>
<li><span data-ttu-id="98cb3-133"># ผู้จัดจำหน่ายรวม</span><span class="sxs-lookup"><span data-stu-id="98cb3-133">Total # vendors</span></span></li>
<li><span data-ttu-id="98cb3-134"># ผู้จัดจำหน่ายที่ใช้งานอยู่รวม</span><span class="sxs-lookup"><span data-stu-id="98cb3-134">Total # of active vendors</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="98cb3-135">การซื้อโดยเรียงตามผลิตภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="98cb3-135">Purchase by product</span></span></td>
<td><ul>
<li><span data-ttu-id="98cb3-136">การซื้อโดยเรียงตามประเภทการจัดซื้อ / ชื่อผลิตภัณฑ์ (แผนภูมิคอลัมน์)</span><span class="sxs-lookup"><span data-stu-id="98cb3-136">Purchase by procurement category / product name (column chart)</span></span></li>
<li><span data-ttu-id="98cb3-137">ยอดการซื้อโดยเรียงตามประเภทการจัดซื้อ / ชื่อผลิตภัณฑ์ (แผนภูมิวงกลม)</span><span class="sxs-lookup"><span data-stu-id="98cb3-137">Total purchase by procurement category / product name (pie chart)</span></span></li>
<li><span data-ttu-id="98cb3-138">ผลิตภัณฑ์ 10 อันดับแรกโดยเรียงตามการซื้อ (แผนภูมิแท่งแบบเรียงซ้อน)</span><span class="sxs-lookup"><span data-stu-id="98cb3-138">Top 10 products by purchase (stacked bar chart)</span></span></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="98cb3-139"># ผลิตภัณฑ์รวม</span><span class="sxs-lookup"><span data-stu-id="98cb3-139">Total # of products</span></span></li>
<li><span data-ttu-id="98cb3-140">เปอร์เซ็นต์ของผลิตภัณฑ์ที่ใช้งานอยู่ทั้งหมดของ # ผลิตภัณฑ์รวม</span><span class="sxs-lookup"><span data-stu-id="98cb3-140">Total active products percentage of total # of products</span></span></li>
<li><span data-ttu-id="98cb3-141">จำนวนของผลิตภัณฑ์ที่ลงบัญชีสำหรับการซื้อ 80%</span><span class="sxs-lookup"><span data-stu-id="98cb3-141">Number of products accounting for 80% purchase</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="98cb3-142">การซื้อโดยเรียงตามรอบระยะเวลา*</span><span class="sxs-lookup"><span data-stu-id="98cb3-142">Purchase by period*</span></span></td>
<td><ul>
<li><span data-ttu-id="98cb3-143">การซื้อโดยเรียงตามเดือน / วัน (แผนภูมิคอลัมน์)</span><span class="sxs-lookup"><span data-stu-id="98cb3-143">Purchase by month / day (column chart)</span></span></li>
<li><span data-ttu-id="98cb3-144">ค่าความแปรปรวน YOY การซื้อสะสม (แผนภูมิน้ำตก)</span><span class="sxs-lookup"><span data-stu-id="98cb3-144">Cumulative purchase YOY variance (waterfall chart)</span></span></li>
<li><span data-ttu-id="98cb3-145">การเติบโต YOY การซื้อรวม (แผนภูมิคอลัมน์)</span><span class="sxs-lookup"><span data-stu-id="98cb3-145">Total purchase YOY growth (column chart)</span></span></li>
<li><span data-ttu-id="98cb3-146">รายงานการจัดซื้อ (เมทริกซ์)</span><span class="sxs-lookup"><span data-stu-id="98cb3-146">Procurement statement (matrix)</span></span></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="98cb3-147">การเติบโตการซื้อ YOY</span><span class="sxs-lookup"><span data-stu-id="98cb3-147">YOY purchase growth</span></span></li>
<li><span data-ttu-id="98cb3-148">% การเติบโตการซื้อ YOY</span><span class="sxs-lookup"><span data-stu-id="98cb3-148">YOY purchase growth %</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="98cb3-149">การซื้อโดยเรียงตามที่ตั้งของผู้จัดจำหน่าย</span><span class="sxs-lookup"><span data-stu-id="98cb3-149">Purchase by vendor location</span></span></td>
<td><ul>
<li><span data-ttu-id="98cb3-150">การซื้อโดยเรียงตามเมือง</span><span class="sxs-lookup"><span data-stu-id="98cb3-150">Purchase by city</span></span></li>
<li><span data-ttu-id="98cb3-151">% การเติบโต YOY การซื้อ</span><span class="sxs-lookup"><span data-stu-id="98cb3-151">Purchase YOY growth %</span></span></li>
<li><span data-ttu-id="98cb3-152">การซื้อโดยเรียงตามประเทศ</span><span class="sxs-lookup"><span data-stu-id="98cb3-152">Purchase by country</span></span></li>
</ul></td>
<td></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="98cb3-153">การวิเคราะห์การซื้อและการใช้จ่ายโดยเรียงตามเวลา</span><span class="sxs-lookup"><span data-stu-id="98cb3-153">Purchase spend analysis by time</span></span></td>
<td><ul>
<li><span data-ttu-id="98cb3-154">การซื้อตั้งแต่ปีปัจจุบันโดยเรียงตามเดือน / วัน (แผนภูมิเส้น)</span><span class="sxs-lookup"><span data-stu-id="98cb3-154">Purchase current year by month / day (line chart)</span></span></li>
<li><span data-ttu-id="98cb3-155">การซื้อปัจจุบันและปีที่แล้ว (แผนภูมิคอลัมน์และเส้น)</span><span class="sxs-lookup"><span data-stu-id="98cb3-155">Purchase current and last year (line and column chart)</span></span></li>
</ul></td>
<td></td>
</tr>
<tr class="even">
<td><span data-ttu-id="98cb3-156">การวิเคราะห์การซื้อและการใช้จ่ายโดยเรียงตามผู้จัดจำหน่าย</span><span class="sxs-lookup"><span data-stu-id="98cb3-156">Purchase spend analysis by vendor</span></span></td>
<td><ul>
<li><span data-ttu-id="98cb3-157">% การซื้อของผู้จัดจำหน่าย 10 อันดับแรกของการซื้อ (กรวย)</span><span class="sxs-lookup"><span data-stu-id="98cb3-157">Top 10 vendor purchase % of purchase (funnel)</span></span></li>
<li><span data-ttu-id="98cb3-158">ผู้จัดจำหน่าย 10 อันดับแรกที่มี YOY การใช้จ่ายที่เพิ่มขึ้น</span><span class="sxs-lookup"><span data-stu-id="98cb3-158">Top 10 vendors with increased spending YOY</span></span></li>
<li><span data-ttu-id="98cb3-159">ผู้จัดจำหน่าย 10 อันดับแรกที่มี YOY การใช้จ่ายที่ลดลง</span><span class="sxs-lookup"><span data-stu-id="98cb3-159">Top 10 vendors with decreased spending YOY</span></span></li>
</ul></td>
<td></td>
</tr>
</tbody>
</table>

<span data-ttu-id="98cb3-160">\* การซื้อปีนี้และปีที่แล้ว และการเติบโตโดยเรียงตามประเภทการจัดซื้อ</span><span class="sxs-lookup"><span data-stu-id="98cb3-160">\* Purchase this year and last year, and growth by procurement category</span></span>

## <a name="extending-the-power-bi-content"></a><span data-ttu-id="98cb3-161">การขยายเนื้อหา Power BI</span><span class="sxs-lookup"><span data-stu-id="98cb3-161">Extending the Power BI content</span></span>
<span data-ttu-id="98cb3-162">โดยการใช้ชุดเนื้อหาที่พร้อมใช้งานใน Microsoft Dynamics Lifecycle Services (LCS) คุณสามารถให้ข้อมูลการวิเคราะห์ที่ยอดเยี่ยมแก่ผู้ที่ไม่ได้ลงชื่อเข้าใช้ Microsoft Dynamics 365</span><span class="sxs-lookup"><span data-stu-id="98cb3-162">By using the content packs that are available in Microsoft Dynamics Lifecycle Services (LCS), you can provide great analytics to people who don't sign in to Microsoft Dynamics 365.</span></span> <span data-ttu-id="98cb3-163">คุณสามารถแก้ไขชุดเนื้อหาเหล่านี้ เพื่อรวมกับการรายงานหรือสิ่งที่มองเห็นได้อื่น ๆ และจากนั้นเผยแพร่ชุดเนื้อหานี้ไปยังผู้เช่า Power BI.com ของคุณสำหรับการวิเคราะห์</span><span class="sxs-lookup"><span data-stu-id="98cb3-163">You can modify these content packs so that they include other reports or visuals, and then publish the content packs to your Power BI.com tenant for analysis.</span></span> 

<span data-ttu-id="98cb3-164">คุณสามารถค้นหาเนื้อหา Power BI **การวิเคราะห์การซื้อและการใช้จ่าย** ได้ในไลบรารีสินทรัพย์ที่ใช้ร่วมกันใน LCS</span><span class="sxs-lookup"><span data-stu-id="98cb3-164">You can find the **Purchase spend analysis** Power BI content in the Shared assets library in LCS.</span></span> <span data-ttu-id="98cb3-165">สำหรับข้อมูลเพิ่มเติมเกี่ยวกับวิธีการดาวน์โหลดเนื้อหา Power BI และนำไปใช้ในองค์กรของคุณ ให้ดูที่ [เนื้อหา Power BI ใน LCS จาก Microsoft และคู่ค้าของคุณ](power-bi-content-microsoft-partners.md)</span><span class="sxs-lookup"><span data-stu-id="98cb3-165">For more information about how to download the content and implement it in your organization, see [Power BI content in LCS from Microsoft and your partners](power-bi-content-microsoft-partners.md).</span></span> <span data-ttu-id="98cb3-166">เมื่อต้องการดูการสาธิตที่แสดงวิธีใช้เนื้อหา Power BI ให้ดูที่ Office Mix [เนื้อหา Power BI จาก Microsoft และคู่ค้าของคุณใน Dynamics Lifecycle Services](https://mix.office.com/watch/9puyb1b2xs1w)</span><span class="sxs-lookup"><span data-stu-id="98cb3-166">To watch a demo that shows how to implement the Power BI content, see the [Power BI content from Microsoft and your partners in Dynamics Lifecycle Services](https://mix.office.com/watch/9puyb1b2xs1w) Office Mix.</span></span>

<span data-ttu-id="98cb3-167">ตรวจสอบให้แน่ใจว่าได้ดาวน์โหลดเนื้อหา **การวิเคราะห์การซื้อและการใช้จ่าย** ที่ใช้กับเวอร์ชันของ Microsoft Dynamics 365 ที่คุณกำลังใช้อยู่</span><span class="sxs-lookup"><span data-stu-id="98cb3-167">Be sure to download the **Purchase spend analysis** content that applies to the version of Dynamics 365 that you're using.</span></span>

> [!NOTE]
> <span data-ttu-id="98cb3-168">ถ้าคุณกำลังใช้ Microsoft Dynamics 365 สำหรับเวอร์ชันการดำเนินงาน 1611 KB 4011327 เป็นข้อกำหนดเบื้องต้นสำหรับเนื้อหา Power BI นี้</span><span class="sxs-lookup"><span data-stu-id="98cb3-168">If you're using Microsoft Dynamics 365 for Operations version 1611, KB 4011327 is a prerequisite for this Power BI content.</span></span> <span data-ttu-id="98cb3-169">หลังจากที่คุณลงชื่อเข้าใช้ไปยัง LCS คุณสามารถเข้าถึง KB ได้ที่ https://fix.lcs.dynamics.com/issue/results/?q=kb4011327</span><span class="sxs-lookup"><span data-stu-id="98cb3-169">After you sign in to LCS, you can access the KB at https://fix.lcs.dynamics.com/issue/results/?q=kb4011327.</span></span>

## <a name="data-model-and-entities"></a><span data-ttu-id="98cb3-170">แบบจำลองข้อมูลและเอนทิตี</span><span class="sxs-lookup"><span data-stu-id="98cb3-170">Data model and entities</span></span>
<span data-ttu-id="98cb3-171">ข้อมูลดังต่อไปนี้ถูกใช้ในการกรอกข้อมูลหน้ารายงานในเนื้อหา **การวิเคราะห์การซื้อและการใช้จ่าย** ใน Power BI</span><span class="sxs-lookup"><span data-stu-id="98cb3-171">The following data is used to fill the report pages in the **Purchase spend analysis** Power BI content.</span></span> <span data-ttu-id="98cb3-172">ข้อมูลนี้จะแสดงเป็นหน่วยวัดรวมที่มีการแบ่งระยะในที่จัดเก็บเอนทิตี้</span><span class="sxs-lookup"><span data-stu-id="98cb3-172">This data is represented as aggregate measurements that are staged in the Entity store.</span></span> <span data-ttu-id="98cb3-173">ที่จัดเก็บเอนทิตี้คือฐานข้อมูลเซิร์ฟเวอร์ Microsoft SQL ที่ได้รับการปรับให้เหมาะสมสำหรับการวิเคราะห์</span><span class="sxs-lookup"><span data-stu-id="98cb3-173">The Entity store is a Microsoft SQL Server database that is optimized for analytics.</span></span> <span data-ttu-id="98cb3-174">สำหรับข้อมูลเพิ่มเติม ดู [ภาพรวมของการรวม Power BI กับร้านค้าเอนทิตี](power-bi-integration-entity-store.md)</span><span class="sxs-lookup"><span data-stu-id="98cb3-174">For more information, see [Overview of Power BI integration with Entity store](power-bi-integration-entity-store.md).</span></span>

<span data-ttu-id="98cb3-175">การวัดแบบรวมในเนื้อหานี้คือชุดย่อยของการวัดแบบรวมที่พร้อมใช้งานในคิวบ์การซื้อใน Microsoft Dynamics AX 2012 และ Microsoft Dynamics AX 2012 R3</span><span class="sxs-lookup"><span data-stu-id="98cb3-175">The aggregate measurements in this content are the subset of aggregate measurements that were available in the Purchase Cube in Microsoft Dynamics AX 2012 and Microsoft Dynamics AX 2012 R3.</span></span> <span data-ttu-id="98cb3-176">เมื่อต้องการแบ่งระยะของการวัดแบบรวมของ Cube ในร้านค้าเอนทิตี คุณจะต้องทำให้สามารถปรับใช้ได้</span><span class="sxs-lookup"><span data-stu-id="98cb3-176">To stage the cube’s aggregate measurements in the Entity store, you must make them deployable.</span></span> <span data-ttu-id="98cb3-177">สำหรับข้อมูลเพิ่มเติม ดูกระบวนการสำหรับการแบ่งระยะการวัดแบบรวมในร้านค้าเอนทิตีใน [ภาพรวม Power BI กับร้านค้าเอนทิตี](power-bi-integration-entity-store.md)</span><span class="sxs-lookup"><span data-stu-id="98cb3-177">For more information, see the procedure for staging aggregate measurements in the Entity store in [Overview of Power BI integration with Entity store](power-bi-integration-entity-store.md).</span></span> <span data-ttu-id="98cb3-178">การวัดแบบรวมหลักต่อไปนี้จะพร้อมใช้งานได้โดยตรงจากเอนทิตีในบรรทัดใบแจ้งหนี้และจะถูกใช้เป็นข้อมูลพื้นฐานของเนื้อหา</span><span class="sxs-lookup"><span data-stu-id="98cb3-178">The following key aggregate measurements are available directly from the Invoice lines entity and are used as the basis of the content.</span></span>

| <span data-ttu-id="98cb3-179">เอนทิตี้</span><span class="sxs-lookup"><span data-stu-id="98cb3-179">Entity</span></span>        | <span data-ttu-id="98cb3-180">การวัดแบบรวมหลัก</span><span class="sxs-lookup"><span data-stu-id="98cb3-180">Key aggregate measurements</span></span> | <span data-ttu-id="98cb3-181">แหล่งข้อมูล</span><span class="sxs-lookup"><span data-stu-id="98cb3-181">Data source</span></span>                                 | <span data-ttu-id="98cb3-182">ฟิลด์</span><span class="sxs-lookup"><span data-stu-id="98cb3-182">Field</span></span>              | <span data-ttu-id="98cb3-183">คำอธิบาย</span><span class="sxs-lookup"><span data-stu-id="98cb3-183">Description</span></span>                            |
|---------------|----------------------------|---------------------------------------------|--------------------|----------------------------------------|
| <span data-ttu-id="98cb3-184">รายการในใบแจ้งหนี้</span><span class="sxs-lookup"><span data-stu-id="98cb3-184">Invoice lines</span></span> | <span data-ttu-id="98cb3-185">การซื้อ</span><span class="sxs-lookup"><span data-stu-id="98cb3-185">Purchase</span></span>                   | <span data-ttu-id="98cb3-186">VendInvoiceTrans</span><span class="sxs-lookup"><span data-stu-id="98cb3-186">VendInvoiceTrans</span></span>                            | <span data-ttu-id="98cb3-187">SUM(LineAmountMST)</span><span class="sxs-lookup"><span data-stu-id="98cb3-187">SUM(LineAmountMST)</span></span> | <span data-ttu-id="98cb3-188">ยอดเงินในสกุลเงินทางบัญชี</span><span class="sxs-lookup"><span data-stu-id="98cb3-188">The amount in the accounting currency.</span></span> |

<span data-ttu-id="98cb3-189">ตารางต่อไปนี้แสดงถึงการวัดหลักที่ถูกคำนวณในเนื้อหาที่คำนวณจากเอนทิตีในบรรทัดใบแจ้งหนี้</span><span class="sxs-lookup"><span data-stu-id="98cb3-189">The following table shows the key measurements in the content that are calculated from the Invoice lines entity.</span></span>

| <span data-ttu-id="98cb3-190">การประเมิน</span><span class="sxs-lookup"><span data-stu-id="98cb3-190">Measure</span></span>               | <span data-ttu-id="98cb3-191">การคำนวณ</span><span class="sxs-lookup"><span data-stu-id="98cb3-191">Calculation</span></span>                                                                                         |
|-----------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="98cb3-192">การซื้อปีปัจจุบัน</span><span class="sxs-lookup"><span data-stu-id="98cb3-192">Purchase current year</span></span> | <span data-ttu-id="98cb3-193">การซื้อปีปัจจุบัน = SUM('Invoice lines'\[Purchase\])</span><span class="sxs-lookup"><span data-stu-id="98cb3-193">Purchase current year = SUM('Invoice lines'\[Purchase\])</span></span>                                            |
| <span data-ttu-id="98cb3-194">การซื้อปีที่แล้ว</span><span class="sxs-lookup"><span data-stu-id="98cb3-194">Purchase last year</span></span>    | <span data-ttu-id="98cb3-195">การซื้อปีที่แล้ว = CALCULATE(SUM('Invoice lines'\[Purchase\]), SAMEPERIODLASTYEAR(Dates\[Date\]))</span><span class="sxs-lookup"><span data-stu-id="98cb3-195">Purchase last year = CALCULATE(SUM('Invoice lines'\[Purchase\]), SAMEPERIODLASTYEAR(Dates\[Date\]))</span></span> |
| <span data-ttu-id="98cb3-196">การเติบโตการซื้อ YOY</span><span class="sxs-lookup"><span data-stu-id="98cb3-196">YOY purchase growth</span></span>   | <span data-ttu-id="98cb3-197">การเติบโตการซื้อ YOY = \[Purchase current year\] – \[Purchase last year\]</span><span class="sxs-lookup"><span data-stu-id="98cb3-197">YOY purchase growth = \[Purchase current year\] – \[Purchase last year\]</span></span>                            |

<span data-ttu-id="98cb3-198">มิติหลักในเนื้อหาต่อไปนี้จะถูกใช้เป็นตัวกรองเพื่อแบ่งส่วนการวัดแบบรวม เพื่อให้คุณสามารถได้รับส่วนประกอบที่มากขึ้นและได้รับข้อมูลเชิงลึกเชิงวิเคราะห์ที่ละเอียดมากขึ้น</span><span class="sxs-lookup"><span data-stu-id="98cb3-198">The following key dimensions in the content are used as filters to slice the aggregate measurements, so that you can achieve more granularity and gain deeper analytical insights.</span></span>

| <span data-ttu-id="98cb3-199">เอนทิตี้</span><span class="sxs-lookup"><span data-stu-id="98cb3-199">Entity</span></span>                 | <span data-ttu-id="98cb3-200">ตัวอย่างของแอตทริบิวต์</span><span class="sxs-lookup"><span data-stu-id="98cb3-200">Examples of attributes</span></span>                                |
|------------------------|-------------------------------------------------------|
| <span data-ttu-id="98cb3-201">ผู้จัดจำหน่าย</span><span class="sxs-lookup"><span data-stu-id="98cb3-201">Vendors</span></span>                | <span data-ttu-id="98cb3-202">กลุ่มผู้จัดจำหน่าย ประเทศหรือภูมิภาคของผู้จัดจำหน่าย ชื่อผู้จัดจำหน่าย</span><span class="sxs-lookup"><span data-stu-id="98cb3-202">Vendor groups, Vendor country or regions, Vendor name</span></span> |
| <span data-ttu-id="98cb3-203">ผลิตภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="98cb3-203">Products</span></span>               | <span data-ttu-id="98cb3-204">หมายเลขผลิตภัณฑ์ ชื่อผลิตภัณฑ์ ชื่อกลุ่มสินค้า</span><span class="sxs-lookup"><span data-stu-id="98cb3-204">Product number, Product name, Item groups name</span></span>        |
| <span data-ttu-id="98cb3-205">ประเภทการจัดซื้อ</span><span class="sxs-lookup"><span data-stu-id="98cb3-205">Procurement categories</span></span> | <span data-ttu-id="98cb3-206">ประเภทการจัดซื้อ ชื่อประเภทการจัดซื้อ</span><span class="sxs-lookup"><span data-stu-id="98cb3-206">Procurement category, Procurement category names</span></span>      |
| <span data-ttu-id="98cb3-207">นิติบุคคล</span><span class="sxs-lookup"><span data-stu-id="98cb3-207">Legal entities</span></span>         | <span data-ttu-id="98cb3-208">ชื่อนิติบุคคล</span><span class="sxs-lookup"><span data-stu-id="98cb3-208">Legal entity name</span></span>                                     |
| <span data-ttu-id="98cb3-209">วันที่</span><span class="sxs-lookup"><span data-stu-id="98cb3-209">Dates</span></span>                  | <span data-ttu-id="98cb3-210">วันที่ ออฟเซ็ตของปี</span><span class="sxs-lookup"><span data-stu-id="98cb3-210">Dates, Year offset</span></span>                                    |

<span data-ttu-id="98cb3-211">โดยค่าเริ่มต้น เนื้อหาจะแสดงข้อมูลสำหรับปีปฏิทินปัจจุบัน</span><span class="sxs-lookup"><span data-stu-id="98cb3-211">By default, the content shows data for the current calendar year.</span></span> <span data-ttu-id="98cb3-212">อย่างไรก็ตาม คุณสามารถเปลี่ยนตัวกรองวันที่ในส่วนตัวกรองรายงาน</span><span class="sxs-lookup"><span data-stu-id="98cb3-212">However, you can change the date filter in the report filters section.</span></span> <span data-ttu-id="98cb3-213">นอกจากนี้คุณยังสามารถเปลี่ยนตัวกรองของบริษัท</span><span class="sxs-lookup"><span data-stu-id="98cb3-213">You can also change the company filter.</span></span>

