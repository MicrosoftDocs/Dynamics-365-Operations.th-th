---
title: "ตัวเลือกในการกรองข้อมูลและไวยากรณ์แบบสอบถาม"
description: "บทความนี้อธิบายถึงการกรองข้อมูลและตัวเลือกการสอบถามที่พร้อมใช้งานเมื่อคุณใช้ตัวดำเนินการ \"รายการตรงกัน\" ในกล่องโต้ตอบตัวกรอง/เรียงลำดับขั้นสูง"
author: jasongre
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: SysQueryForm
audience: Application User
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.custom: 3811
ms.assetid: b4969b30-2fe1-4a3c-bbea-725dc37c8b60
ms.search.region: Global
ms.author: jasongre
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 1fe940d2d282a5b4468b3ba572626b5c87839e6d
ms.contentlocale: th-th
ms.lasthandoff: 11/03/2017

---

# <a name="advanced-filtering-and-query-syntax"></a><span data-ttu-id="bc0eb-103">ตัวเลือกในการกรองข้อมูลและไวยากรณ์แบบสอบถาม</span><span class="sxs-lookup"><span data-stu-id="bc0eb-103">Advanced filtering and query syntax</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="bc0eb-104">บทความนี้อธิบายถึงการกรองข้อมูลและตัวเลือกการสอบถามที่พร้อมใช้งานเมื่อคุณใช้ตัวดำเนินการ "รายการตรงกัน" ในกล่องโต้ตอบตัวกรอง/เรียงลำดับขั้นสูง</span><span class="sxs-lookup"><span data-stu-id="bc0eb-104">This article describes the filtering and query options that are available when you use the "matches" operator in the Advanced filter/sort dialog.</span></span>

<a name="advanced-query-syntax"></a><span data-ttu-id="bc0eb-105">ไวยากรณ์แบบสอบถามขั้นสูง</span><span class="sxs-lookup"><span data-stu-id="bc0eb-105">Advanced query syntax</span></span>
---------------------

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="bc0eb-106">ไวยากรณ์</span><span class="sxs-lookup"><span data-stu-id="bc0eb-106">Syntax</span></span></th>
<th><span data-ttu-id="bc0eb-107">คำอธิบายอักขระ</span><span class="sxs-lookup"><span data-stu-id="bc0eb-107">Character description</span></span></th>
<th><span data-ttu-id="bc0eb-108">คำอธิบาย</span><span class="sxs-lookup"><span data-stu-id="bc0eb-108">Description</span></span></th>
<th><span data-ttu-id="bc0eb-109">ตัวอย่าง</span><span class="sxs-lookup"><span data-stu-id="bc0eb-109">Example</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="bc0eb-110"><em>ค่า</em></span><span class="sxs-lookup"><span data-stu-id="bc0eb-110"><em>value</em></span></span></td>
<td><span data-ttu-id="bc0eb-111">เท่ากับค่าที่ป้อน</span><span class="sxs-lookup"><span data-stu-id="bc0eb-111">Equal to the value that is entered</span></span></td>
<td><span data-ttu-id="bc0eb-112">พิมพ์ค่าที่จะค้นหา</span><span class="sxs-lookup"><span data-stu-id="bc0eb-112">Type the value to find.</span></span></td>
<td><span data-ttu-id="bc0eb-113"><strong>Smith</strong> จะค้นหา &quot;Smith&quot;</span><span class="sxs-lookup"><span data-stu-id="bc0eb-113"><strong>Smith</strong> finds &quot;Smith&quot;.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="bc0eb-114">!<em>ค่า</em> (เครื่องหมายอัศเจรีย์)</span><span class="sxs-lookup"><span data-stu-id="bc0eb-114">!<em>value</em> (exclamation point)</span></span></td>
<td><span data-ttu-id="bc0eb-115">ไม่เท่ากับค่าที่ป้อน</span><span class="sxs-lookup"><span data-stu-id="bc0eb-115">Not equal to the value that is entered</span></span></td>
<td><span data-ttu-id="bc0eb-116">พิมพ์เครื่องหมายอัศเจรีย์หน้าค่าที่คุณจะแยก</span><span class="sxs-lookup"><span data-stu-id="bc0eb-116">Type an exclamation point and then the value to exclude.</span></span></td>
<td><span data-ttu-id="bc0eb-117"><strong>!Smith</strong> จะค้นหาค่าทั้งหมด ยกเว้น &quot;Smith&quot;</span><span class="sxs-lookup"><span data-stu-id="bc0eb-117"><strong>!Smith</strong> finds all values except &quot;Smith&quot;.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="bc0eb-118"><em>จากค่า</em>..<em>ถึงค่า</em> (เครื่องหมายมหัพภาคสองเครื่องหมาย)</span><span class="sxs-lookup"><span data-stu-id="bc0eb-118"><em>from-value</em>..<em>to-value</em> (double period)</span></span></td>
<td><span data-ttu-id="bc0eb-119">ระหว่างสองค่าที่ป้อนถูกแยกด้วยเครื่องหมายมหัพภาคสองเครื่องหมาย</span><span class="sxs-lookup"><span data-stu-id="bc0eb-119">Between the two values that are separated by double periods</span></span></td>
<td><span data-ttu-id="bc0eb-120">พิมพ์ค่าเริ่มต้น ตามด้วยเครื่องหมายมหัพภาคสองเครื่องหมาย แล้วตามด้วยค่าสิ้นสุด</span><span class="sxs-lookup"><span data-stu-id="bc0eb-120">Type the from-value, then two periods, and then the to-value.</span></span></td>
<td><span data-ttu-id="bc0eb-121"><strong>1..10</strong> จะค้นหาค่าทั้งหมดตั้งแต่ 1 จนถึง 10</span><span class="sxs-lookup"><span data-stu-id="bc0eb-121"><strong>1..10</strong> finds all values from 1 through 10.</span></span> <span data-ttu-id="bc0eb-122">อย่างไรก็ตาม ในฟิลด์สตริง <strong>A..C</strong>จะค้นหาค่าทั้งหมดที่ขึ้นต้นด้วย &quot;A&quot; และ &quot;B&quot; และค่าเท่ากับ &quot;C&quot;</span><span class="sxs-lookup"><span data-stu-id="bc0eb-122">However, in a string field, <strong>A..C</strong> finds all values that start with &quot;A&quot; and &quot;B&quot;, and values that are exactly equal to &quot;C&quot;.</span></span> <span data-ttu-id="bc0eb-123">ตัวอย่างเช่น การสอบถามนี้จะไม่ค้นหา &quot;Ca&quot;</span><span class="sxs-lookup"><span data-stu-id="bc0eb-123">For example, this query won't find &quot;Ca&quot;.</span></span> <span data-ttu-id="bc0eb-124">เมื่อต้องการค่าทั้งหมดตั้งแต่ &quot;A*&quot; จนถึง &quot;C*&quot; พิมพ์ <strong>A..D</strong></span><span class="sxs-lookup"><span data-stu-id="bc0eb-124">To find all values from &quot;A*&quot; through &quot;C*&quot;, type <strong>A..D</strong>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="bc0eb-125">..<em>ค่า</em> (เครื่องหมายมหัพภาคสองเครื่องหมาย)</span><span class="sxs-lookup"><span data-stu-id="bc0eb-125">..<em>value</em> (double period)</span></span></td>
<td><span data-ttu-id="bc0eb-126">น้อยกว่าหรือเท่ากับค่าที่ป้อน</span><span class="sxs-lookup"><span data-stu-id="bc0eb-126">Less than or equal to the value that is entered</span></span></td>
<td><span data-ttu-id="bc0eb-127">พิมพ์เครื่องหมายมหัพภาคสองเครื่องหมาย แล้วตามด้วยค่า</span><span class="sxs-lookup"><span data-stu-id="bc0eb-127">Type two periods and then the value.</span></span></td>
<td><span data-ttu-id="bc0eb-128"><strong>..1000</strong> จะค้นหาหมายเลขใดๆ ที่น้อยกว่าหรือเท่ากับ 1000 เช่น &quot;100&quot;, &quot;999.95&quot;และ &quot;1,000&quot;</span><span class="sxs-lookup"><span data-stu-id="bc0eb-128"><strong>..1000</strong> finds any number that is less than or equal to 1000, such as &quot;100&quot;, &quot;999.95&quot;, and &quot;1,000&quot;.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="bc0eb-129"><em>ค่า</em>..</span><span class="sxs-lookup"><span data-stu-id="bc0eb-129"><em>value</em>..</span></span> <span data-ttu-id="bc0eb-130">(เครื่องหมายมหัพภาคสองเครื่องหมาย)</span><span class="sxs-lookup"><span data-stu-id="bc0eb-130">(double period)</span></span></td>
<td><span data-ttu-id="bc0eb-131">มากกว่าหรือเท่ากับค่าที่ป้อน</span><span class="sxs-lookup"><span data-stu-id="bc0eb-131">Greater than or equal to the value that is entered</span></span></td>
<td><span data-ttu-id="bc0eb-132">พิมพ์ค่า แล้วตามด้วยเครื่องหมายมหัพภาคสองเครื่องหมาย</span><span class="sxs-lookup"><span data-stu-id="bc0eb-132">Type the value and then two periods.</span></span></td>
<td><span data-ttu-id="bc0eb-133"><strong>1000..</strong></span><span class="sxs-lookup"><span data-stu-id="bc0eb-133"><strong>1000..</strong></span></span> <span data-ttu-id="bc0eb-134">จะค้นหาหมายเลขใดๆ ที่มากกว่าหรือเท่ากับ 1000 เช่น &quot;1,000&quot;, &quot;1,000.01&quot;และ &quot;1,000,000&quot;</span><span class="sxs-lookup"><span data-stu-id="bc0eb-134">finds any number that is greater than or equal to 1000, such as &quot;1,000&quot;, &quot;1,000.01&quot;, and &quot;1,000,000&quot;.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="bc0eb-135">&gt;<em>ค่า</em> (เครื่องหมายมากกว่า)</span><span class="sxs-lookup"><span data-stu-id="bc0eb-135">&gt;<em>value</em> (greater than sign)</span></span></td>
<td><span data-ttu-id="bc0eb-136">มากกว่าค่าที่ป้อน</span><span class="sxs-lookup"><span data-stu-id="bc0eb-136">Greater than the value that is entered</span></span></td>
<td><span data-ttu-id="bc0eb-137">พิมพ์เครื่องหมายมากกว่า (<strong>&gt;</strong>) แล้วตามด้วยค่า</span><span class="sxs-lookup"><span data-stu-id="bc0eb-137">Type a greater than sign (<strong>&gt;</strong>) and then the value.</span></span></td>
<td><span data-ttu-id="bc0eb-138"><strong>&gt;1000</strong> จะค้นหาหมายเลขใดๆ ที่มากกว่าหรือเท่ากับ 1000 เช่น &quot;1000.01&quot;, &quot;20,000&quot;และ &quot;1,000,000&quot;</span><span class="sxs-lookup"><span data-stu-id="bc0eb-138"><strong>&gt;1000</strong> finds any number that is greater than 1000, such as &quot;1000.01&quot;, &quot;20,000&quot;, and &quot;1,000,000&quot;.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="bc0eb-139">&lt;<em>ค่า</em> (เครื่องหมายน้อยกว่า)</span><span class="sxs-lookup"><span data-stu-id="bc0eb-139">&lt;<em>value</em> (less than sign)</span></span></td>
<td><span data-ttu-id="bc0eb-140">น้อยกว่าค่าที่ป้อน</span><span class="sxs-lookup"><span data-stu-id="bc0eb-140">Less than the value that is entered</span></span></td>
<td><span data-ttu-id="bc0eb-141">พิมพ์เครื่องหมายน้อยกว่า (<strong>&lt;</strong>) แล้วตามด้วยค่า</span><span class="sxs-lookup"><span data-stu-id="bc0eb-141">Type a less than sign (<strong>&lt;</strong>) and then the value.</span></span></td>
<td><span data-ttu-id="bc0eb-142"><strong>&lt;1000</strong> จะค้นหาหมายเลขใดๆ ที่น้อยกว่า 1000 เช่น &quot;999.99&quot;, &quot;1&quot;และ &quot;-200&quot;</span><span class="sxs-lookup"><span data-stu-id="bc0eb-142"><strong>&lt;1000</strong> finds any number that is less than 1000, such as &quot;999.99&quot;, &quot;1&quot;, and &quot;-200&quot;.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="bc0eb-143"><em>ค่า</em>* (ดอกจัน)</span><span class="sxs-lookup"><span data-stu-id="bc0eb-143"><em>value</em>* (asterisk)</span></span></td>
<td><span data-ttu-id="bc0eb-144">เริ่มจากค่าที่ป้อน</span><span class="sxs-lookup"><span data-stu-id="bc0eb-144">Starting from the value that is entered</span></span></td>
<td><span data-ttu-id="bc0eb-145">พิมพ์ค่าเริ่มต้น แล้วตามด้วยเครื่องหมายดอกจัน (<strong>*</strong>)</span><span class="sxs-lookup"><span data-stu-id="bc0eb-145">Type the starting value and then an asterisk (<strong>*</strong>).</span></span></td>
<td><span data-ttu-id="bc0eb-146"><strong>S*</strong> จะค้นหาสตริงใดๆ ที่เริ่มต้นด้วย &quot;S&quot; เช่น &quot;Stockholm&quot;, &quot;Sydney&quot;และ &quot;San Francisco&quot;</span><span class="sxs-lookup"><span data-stu-id="bc0eb-146"><strong>S*</strong> finds any string that starts with &quot;S&quot;, such as &quot;Stockholm&quot;, &quot;Sydney&quot;, and &quot;San Francisco&quot;.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="bc0eb-147">*<em>ค่า</em> *(ดอกจัน)</span><span class="sxs-lookup"><span data-stu-id="bc0eb-147">*<em>value</em> (asterisk)</span></span></td>
<td><span data-ttu-id="bc0eb-148">สิ้นสุดด้วยค่าที่ป้อน</span><span class="sxs-lookup"><span data-stu-id="bc0eb-148">Ending with the value that is entered</span></span></td>
<td><span data-ttu-id="bc0eb-149">พิมพ์เครื่องหมายดอกจัน แล้วตามด้วยค่าสิ้นสุด</span><span class="sxs-lookup"><span data-stu-id="bc0eb-149">Type an asterisk and then the ending value.</span></span></td>
<td><span data-ttu-id="bc0eb-150"><strong>*east</strong> จะค้นหาสตริงใดๆ ที่สิ้นสุดด้วย &quot;east&quot; เช่น &quot;Northeast&quot; และ &quot;Southeast&quot;</span><span class="sxs-lookup"><span data-stu-id="bc0eb-150"><strong>*east</strong> finds any string that ends with &quot;east&quot;, such as &quot;Northeast&quot; and &quot;Southeast&quot;.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="bc0eb-151">*<em>value</em>* (ดอกจัน)</span><span class="sxs-lookup"><span data-stu-id="bc0eb-151">*<em>value</em>* (asterisk)</span></span></td>
<td><span data-ttu-id="bc0eb-152">มีค่าที่ป้อน</span><span class="sxs-lookup"><span data-stu-id="bc0eb-152">Containing the value that is entered</span></span></td>
<td><span data-ttu-id="bc0eb-153">พิมพ์เครื่องหมายดอกจัน ตามด้วยค่า แล้วตามด้วยเครื่องหมายดอกจันอีกอันหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="bc0eb-153">Type an asterisk, then a value, and then another asterisk.</span></span></td>
<td><span data-ttu-id="bc0eb-154"><strong>*th*</strong> จะค้นหาสตริงใดๆ ที่มี &quot;th&quot; อยู่ เช่น &quot;Northeast&quot; และ &quot;Southeast&quot;</span><span class="sxs-lookup"><span data-stu-id="bc0eb-154"><strong>*th*</strong> finds any string that contains &quot;th&quot;, such as &quot;Northeast&quot; and &quot;Southeast&quot;.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="bc0eb-155">?</span><span class="sxs-lookup"><span data-stu-id="bc0eb-155">?</span></span> <span data-ttu-id="bc0eb-156">(เครื่องหมายคำถาม)</span><span class="sxs-lookup"><span data-stu-id="bc0eb-156">(question mark)</span></span></td>
<td><span data-ttu-id="bc0eb-157">มีอักขระที่ไม่รู้จักหนึ่งอักขระขึ้นไป</span><span class="sxs-lookup"><span data-stu-id="bc0eb-157">Having one or more unknown characters</span></span></td>
<td><span data-ttu-id="bc0eb-158">พิมพ์เครื่องหมายคำถามที่ตำแหน่งของอักขระที่ไม่รู้จักในค่า</span><span class="sxs-lookup"><span data-stu-id="bc0eb-158">Type a question mark at the position of the unknown character in the value.</span></span></td>
<td><span data-ttu-id="bc0eb-159"><strong>Sm?th</strong> จะค้นหา &quot;Smith&quot; และ &quot;Smyth&quot;</span><span class="sxs-lookup"><span data-stu-id="bc0eb-159"><strong>Sm?th</strong> finds &quot;Smith&quot; and &quot;Smyth&quot;.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="bc0eb-160"><em>ค่า</em>,<em>ค่า</em> (เครื่องหมายจุลภาค)</span><span class="sxs-lookup"><span data-stu-id="bc0eb-160"><em>value</em>,<em>value</em> (comma)</span></span></td>
<td><span data-ttu-id="bc0eb-161">จับคู่ค่าที่ถูกแยกด้วยเครื่องหมายจุลภาค</span><span class="sxs-lookup"><span data-stu-id="bc0eb-161">Matching the values that are separated by commas</span></span></td>
<td><span data-ttu-id="bc0eb-162">พิมพ์เงื่อนไขทั้งหมดของคุณ และแยกโดยการใช้เครื่องหมายจุลภาค</span><span class="sxs-lookup"><span data-stu-id="bc0eb-162">Type all your criteria, and separate them by using commas.</span></span></td>
<td><span data-ttu-id="bc0eb-163"><strong>A, D, F, G</strong> จะค้นหาค่าที่ตรงกับ &quot;A&quot;, &quot;D&quot;, &quot;F&quot; และ &quot;G&quot; พอดี</span><span class="sxs-lookup"><span data-stu-id="bc0eb-163"><strong>A, D, F, G</strong> finds exactly &quot;A&quot;, &quot;D&quot;, &quot;F&quot;, and &quot;G&quot;.</span></span> <span data-ttu-id="bc0eb-164"><strong>10, 20, 30, 100</strong> จะค้นหาค่าที่ตรงกับ &quot;10, 20, 30, 100&quot; พอดี</span><span class="sxs-lookup"><span data-stu-id="bc0eb-164"><strong>10, 20, 30, 100</strong> finds exactly &quot;10, 20, 30, 100&quot;.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="bc0eb-165">(<span class="code">คำสั่ง SQL</span>) (คำสั่ง SQL ในวงเล็บ)</span><span class="sxs-lookup"><span data-stu-id="bc0eb-165">(<span class="code">SQL statement</span>) (SQL statement between parentheses)</span></span></td>
<td><span data-ttu-id="bc0eb-166">จับคู่การสอบถามที่กำหนด</span><span class="sxs-lookup"><span data-stu-id="bc0eb-166">Matching a defined query</span></span></td>
<td><span data-ttu-id="bc0eb-167">พิมพ์การสอบถามเป็นคำสั่ง SQL ในวงเล็บ</span><span class="sxs-lookup"><span data-stu-id="bc0eb-167">Type a query as an SQL statement between parentheses.</span></span></td>
<td><span data-ttu-id="bc0eb-168"><strong><span class="code">(data source.Fieldname != &quot;A&quot;)</span></strong></span><span class="sxs-lookup"><span data-stu-id="bc0eb-168"><strong><span class="code">(data source.Fieldname != &quot;A&quot;)</span></strong></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="bc0eb-169">อ.</span><span class="sxs-lookup"><span data-stu-id="bc0eb-169">T</span></span></td>
<td><span data-ttu-id="bc0eb-170">วันที่ของวันนี้</span><span class="sxs-lookup"><span data-stu-id="bc0eb-170">Today's date</span></span></td>
<td><span data-ttu-id="bc0eb-171">ชนิด <strong>T</strong></span><span class="sxs-lookup"><span data-stu-id="bc0eb-171">Type <strong>T</strong>.</span></span></td>
<td><span data-ttu-id="bc0eb-172"><strong>T</strong> ตรงกับวันที่ของวันนี้</span><span class="sxs-lookup"><span data-stu-id="bc0eb-172"><strong>T</strong> matches today's date.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="bc0eb-173">(methodName(parameters)) (<strong>SysQueryRangeUtil</strong> วิธีในวงเล็บ)</span><span class="sxs-lookup"><span data-stu-id="bc0eb-173">(methodName(parameters)) (<strong>SysQueryRangeUtil</strong> method between parentheses)</span></span></td>
<td><span data-ttu-id="bc0eb-174">การจับคู่ค่าหรือช่วงของค่าที่ระบุโดยพารามิเตอร์ของวิธีการ <strong>SysQueryRangeUtil</strong></span><span class="sxs-lookup"><span data-stu-id="bc0eb-174">Matching the value or range of values that are specified by the parameters of the <strong>SysQueryRangeUtil</strong> method</span></span></td>
<td><span data-ttu-id="bc0eb-175">พิมพ์วิธีการ <strong>SysQueryRangeUtil</strong> ที่มีพารามิเตอร์ที่ระบุค่าหรือช่วงของค่า</span><span class="sxs-lookup"><span data-stu-id="bc0eb-175">Type a <strong>SysQueryRangeUtil</strong> method that has parameters that specify the value or range of values.</span></span></td>
<td><ol>
<li><span data-ttu-id="bc0eb-176">คลิก <strong>บัญชีลูกหนี้</strong> &gt; <strong>ใบแจ้งหนี้</strong> &gt; <strong>ใบแจ้งหนี้ลูกค้าที่เปิด</strong></span><span class="sxs-lookup"><span data-stu-id="bc0eb-176">Click <strong>Accounts receivable</strong> &gt; <strong>Invoices</strong> &gt; <strong>Open customer invoices</strong>.</span></span></li>
<li><span data-ttu-id="bc0eb-177">กด Ctrl + Shift + F3 เพื่อเปิดหน้า <strong>การสอบถาม</strong></span><span class="sxs-lookup"><span data-stu-id="bc0eb-177">Press Ctrl+Shift+F3 to open the <strong>Inquiry</strong> page.</span></span></li>
<li><span data-ttu-id="bc0eb-178">บนแท็บ <strong>การกำหนดช่วง</strong> ให้คลิก <strong>เพิ่ม</strong></span><span class="sxs-lookup"><span data-stu-id="bc0eb-178">On the <strong>Range</strong> tab, click <strong>Add</strong>.</span></span></li>
<li><span data-ttu-id="bc0eb-179">ชำระธุรกรรมที่ค้างอยู่สำหรับลูกค้าที่เลือก ในฟิลด์ <strong>ตาราง</strong> เลือก <strong>ธุรกรรมลูกค้าที่คงค้าง</strong></span><span class="sxs-lookup"><span data-stu-id="bc0eb-179">In the <strong>Table</strong> field, select <strong>Open customer transactions</strong>.</span></span></li>
<li><span data-ttu-id="bc0eb-180">ในฟิลด์ <strong>ฟิลด์</strong> ให้เลือก <strong>วันที่ครบกำหนด</strong></span><span class="sxs-lookup"><span data-stu-id="bc0eb-180">In the <strong>Field</strong> field, select <strong>Due date</strong>.</span></span></li>
<li><span data-ttu-id="bc0eb-181">ในฟิลด์ <strong>เงื่อนไข</strong> , ให้ป้อน <strong>(yearRange(-2,0))</strong></span><span class="sxs-lookup"><span data-stu-id="bc0eb-181">In the <strong>Criteria</strong> field, enter <strong>(yearRange(-2,0))</strong>.</span></span></li>
<li><span data-ttu-id="bc0eb-182">คลิก <strong>ตกลง</strong> ระบบจะนำเข้าข้อมูลการชำระเงิน</span><span class="sxs-lookup"><span data-stu-id="bc0eb-182">Click <strong>OK</strong>.</span></span> <span data-ttu-id="bc0eb-183">หน้ารายการมีการปรับปรุง และแสดงรายการใบแจ้งหนี้ที่ตรงกับเงื่อนไขที่คุณป้อน</span><span class="sxs-lookup"><span data-stu-id="bc0eb-183">The list page is updated and lists the invoices that match the criterion that you entered.</span></span> <span data-ttu-id="bc0eb-184">สำหรับตัวอย่างนี้ จะแสดงรายการใบแจ้งหนี้ที่ครบกำหนดชำระเมื่อสองปีก่อน</span><span class="sxs-lookup"><span data-stu-id="bc0eb-184">For this example, invoices that were due in the previous two years are listed.</span></span></li>
</ol>
<span data-ttu-id="bc0eb-185">ดูตารางในส่วนถัดไปสำหรับรายละเอียดเพิ่มเติมเกี่ยวกับวันที่และหลาย ๆ ตัวอย่าง <strong>SysQueryRangeUtil</strong></span><span class="sxs-lookup"><span data-stu-id="bc0eb-185">See the table in the next section for additional details about <strong>SysQueryRangeUtil</strong> date methods, and several examples.</span></span></td>
</tr>
</tbody>
</table>

## <a name="advanced-date-queries-that-use-sysqueryrangeutil-methods"></a><span data-ttu-id="bc0eb-186">การสอบถามขั้นสูงวันที่ใช้วิธีการ SysQueryRangeUtil</span><span class="sxs-lookup"><span data-stu-id="bc0eb-186">Advanced date queries that use SysQueryRangeUtil methods</span></span>
<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="bc0eb-187">วิธีการ</span><span class="sxs-lookup"><span data-stu-id="bc0eb-187">Method</span></span></th>
<th><span data-ttu-id="bc0eb-188">คำอธิบาย</span><span class="sxs-lookup"><span data-stu-id="bc0eb-188">Description</span></span></th>
<th><span data-ttu-id="bc0eb-189">ตัวอย่าง</span><span class="sxs-lookup"><span data-stu-id="bc0eb-189">Example</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="bc0eb-190">วัน (_relativeDays = 0)</span><span class="sxs-lookup"><span data-stu-id="bc0eb-190">Day (_relativeDays=0)</span></span></td>
<td><span data-ttu-id="bc0eb-191">ค้นหาวันทีที่สัมพันธ์กับวันรอบเวลา</span><span class="sxs-lookup"><span data-stu-id="bc0eb-191">Find a date relative to the session date.</span></span> <span data-ttu-id="bc0eb-192">ค่าบวกระบุถึง วันที่ในอนาคต และค่าลบระบุวันที่ในอดีต</span><span class="sxs-lookup"><span data-stu-id="bc0eb-192">Positive values indicate future dates, and negative values indicate past dates.</span></span></td>
<td><ul>
<li><span data-ttu-id="bc0eb-193"><strong>วันพรุงนี้</strong> – ป้อน <strong>(Day(1))</strong></span><span class="sxs-lookup"><span data-stu-id="bc0eb-193"><strong>Tomorrow</strong> – Enter <strong>(Day(1))</strong>.</span></span></li>
<li><span data-ttu-id="bc0eb-194"><strong>วันนี้</strong> – ป้อน <strong>(Day(0))</strong></span><span class="sxs-lookup"><span data-stu-id="bc0eb-194"><strong>Today</strong> – Enter <strong>(Day(0))</strong>.</span></span></li>
<li><span data-ttu-id="bc0eb-195"><strong>เมื่อวานนี้</strong> – ป้อน <strong>(Day(-1))</strong></span><span class="sxs-lookup"><span data-stu-id="bc0eb-195"><strong>Yesterday</strong> – Enter <strong>(Day(-1))</strong>.</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="bc0eb-196">ช่วงวัน (_relativeDaysFrom = 0, _relativeDaysTo = 0)</span><span class="sxs-lookup"><span data-stu-id="bc0eb-196">DayRange (_relativeDaysFrom=0, _relativeDaysTo=0)</span></span></td>
<td><span data-ttu-id="bc0eb-197">ค้นหาช่วงวันทีที่สัมพันธ์กับวันรอบเวลา</span><span class="sxs-lookup"><span data-stu-id="bc0eb-197">Find a range of dates relative to the session date.</span></span> <span data-ttu-id="bc0eb-198">ค่าบวกระบุถึง วันที่ในอนาคต และค่าลบระบุวันที่ในอดีต</span><span class="sxs-lookup"><span data-stu-id="bc0eb-198">Positive values indicate future dates, and negative values indicate past dates.</span></span></td>
<td><ul>
<li><span data-ttu-id="bc0eb-199"><strong>30 วันที่ผ่านมา</strong> – ป้อน <strong>(DayRange(-30,0))</strong>.</span><span class="sxs-lookup"><span data-stu-id="bc0eb-199"><strong>Last 30 days</strong> – Enter <strong>(DayRange(-30,0))</strong>.</span></span></li>
<li><span data-ttu-id="bc0eb-200"><strong>30 วันก่อนหน้านี้และในอนาคต 30 วัน</strong> – ป้อน <strong>(DayRange(-30,30))</strong></span><span class="sxs-lookup"><span data-stu-id="bc0eb-200"><strong>Previous 30 days and next 30 days</strong> – Enter <strong>(DayRange(-30,30))</strong>.</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="bc0eb-201">GreaterThanDate (_relativeDays = 0) GreaterThanUtcDate (_relativeDays = 0)</span><span class="sxs-lookup"><span data-stu-id="bc0eb-201">GreaterThanDate (_relativeDays=0) GreaterThanUtcDate (_relativeDays=0)</span></span></td>
<td><span data-ttu-id="bc0eb-202">ค้นหาวันที่ทั้งหมดหลังจากวันที่สัมพัทธ์ถูกระบุ</span><span class="sxs-lookup"><span data-stu-id="bc0eb-202">Find all dates after the specified relative date.</span></span></td>
<td><ul>
<li><span data-ttu-id="bc0eb-203"><strong>มากกว่า 30 วันถัดไป</strong>– ป้อน <strong>(GreaterThanDate(30))</strong></span><span class="sxs-lookup"><span data-stu-id="bc0eb-203"><strong>More than 30 days from now</strong> – Enter <strong>(GreaterThanDate(30))</strong>.</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="bc0eb-204">GreaterThanUtcNow ()</span><span class="sxs-lookup"><span data-stu-id="bc0eb-204">GreaterThanUtcNow ()</span></span></td>
<td><span data-ttu-id="bc0eb-205">ค้นหารายการวันที่ / เวลาทั้งหมดหลังเวลาปัจจุบัน</span><span class="sxs-lookup"><span data-stu-id="bc0eb-205">Find all date/time entries after the current time.</span></span></td>
<td><ul>
<li><span data-ttu-id="bc0eb-206"><strong>วัน / เวลาในอนาคตทั้งหมด</strong>– ป้อน <strong>(GreaterThanUtcNow())</strong></span><span class="sxs-lookup"><span data-stu-id="bc0eb-206"><strong>All future date/times</strong> – Enter <strong>(GreaterThanUtcNow())</strong>.</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="bc0eb-207">GreaterThanDate (_relativeDays = 0) GreaterThanUtcDate (_relativeDays = 0)</span><span class="sxs-lookup"><span data-stu-id="bc0eb-207">LessThanDate (_relativeDays=0) LessThanUtcDate (_relativeDays=0)</span></span></td>
<td><span data-ttu-id="bc0eb-208">ค้นหาวันที่ทั้งหมดก่อนวันที่สัมพัทธ์ถูกระบุ</span><span class="sxs-lookup"><span data-stu-id="bc0eb-208">Find all dates before the specified relative date.</span></span></td>
<td><ul>
<li><span data-ttu-id="bc0eb-209"><strong>น้อยกว่าเจ็ดวันถัดไป</strong>– ป้อน <strong>(LessThanDate(7))</strong></span><span class="sxs-lookup"><span data-stu-id="bc0eb-209"><strong>Less than seven days from now</strong> – Enter <strong>(LessThanDate(7))</strong>.</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="bc0eb-210">LessThanUtcNow ()</span><span class="sxs-lookup"><span data-stu-id="bc0eb-210">LessThanUtcNow ()</span></span></td>
<td><span data-ttu-id="bc0eb-211">ค้นหารายการวันที่ / เวลาทั้งหมดก่อนเวลาปัจจุบัน</span><span class="sxs-lookup"><span data-stu-id="bc0eb-211">Find all date/time entries before the current time.</span></span></td>
<td><ul>
<li><span data-ttu-id="bc0eb-212"><strong>วัน / เวลาในอดีตทั้งหมด</strong>– ป้อน <strong>(LessThanUtcNow())</strong></span><span class="sxs-lookup"><span data-stu-id="bc0eb-212"><strong>All past date/times</strong> – Enter <strong>(LessThanUtcNow())</strong>.</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="bc0eb-213">MonthRange (_relativeFrom = 0, _relativeTo = 0)</span><span class="sxs-lookup"><span data-stu-id="bc0eb-213">MonthRange (_relativeFrom=0, _relativeTo=0)</span></span></td>
<td><span data-ttu-id="bc0eb-214">ค้นหาช่วงวันที่ ตามเดือนที่สัมพันธ์กับเดือนปัจจุบัน</span><span class="sxs-lookup"><span data-stu-id="bc0eb-214">Find a range of dates, based on months relative to the current month.</span></span></td>
<td><ul>
<li><span data-ttu-id="bc0eb-215"><strong>สองเดือนก่อนหน้านี้</strong>– ป้อน <strong>(MonthRange(-2,0))</strong></span><span class="sxs-lookup"><span data-stu-id="bc0eb-215"><strong>Previous two months</strong> – Enter <strong>(MonthRange(-2,0))</strong>.</span></span></li>
<li><span data-ttu-id="bc0eb-216"><strong>สามเดือนถัดไป</strong>– ป้อน <strong>(MonthRange(0,3))</strong></span><span class="sxs-lookup"><span data-stu-id="bc0eb-216"><strong>Next three months</strong> – Enter <strong>(MonthRange(0,3))</strong>.</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="bc0eb-217">YearRange (_relativeFrom = 0, _relativeTo = 0)</span><span class="sxs-lookup"><span data-stu-id="bc0eb-217">YearRange (_relativeFrom=0, _relativeTo=0)</span></span></td>
<td><span data-ttu-id="bc0eb-218">ค้นหาช่วงวันที่ ตามปีที่สัมพันธ์กับปีปัจจุบัน</span><span class="sxs-lookup"><span data-stu-id="bc0eb-218">Find a range of dates, based on years relative to the current year.</span></span></td>
<td><ul>
<li><span data-ttu-id="bc0eb-219"><strong>ปีถัดไป</strong>– ป้อน <strong>(YearRange (0, 1))</strong></span><span class="sxs-lookup"><span data-stu-id="bc0eb-219"><strong>Next year</strong> – Enter <strong>(YearRange(0, 1))</strong>.</span></span></li>
<li><span data-ttu-id="bc0eb-220"><strong>ปีก่อนหน้า</strong>– ป้อน <strong>(YearRange (-1,0))</strong></span><span class="sxs-lookup"><span data-stu-id="bc0eb-220"><strong>Previous year</strong> – Enter <strong>(YearRange(-1,0))</strong>.</span></span></li>
</ul></td>
</tr>
</tbody>
</table>






