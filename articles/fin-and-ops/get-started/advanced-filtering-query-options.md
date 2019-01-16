---
title: "ตัวเลือกในการกรองข้อมูลและไวยากรณ์แบบสอบถาม"
description: "บทความนี้อธิบายถึงตัวเลือกในการกรองข้อมูลและการสอบถามที่พร้อมใช้งาน เมื่อคุณใช้กล่องโต้ตอบตัวกรอง/เรียงลำดับขั้นสูง หรือตัวดำเนินการ การจับคู่ ในตัวกรองบานหน้าต่างตัวกรองหรือส่วนหัวของคอลัมน์ในกริด"
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
ms.sourcegitcommit: 3ee5334c87b2b0acae2afa6882feca63e3b9cc8e
ms.openlocfilehash: 01a508e97721099f92b9167dfdfa1b9669b9341c
ms.contentlocale: th-th
ms.lasthandoff: 12/18/2018

---

# <a name="advanced-filtering-and-query-syntax"></a>ตัวเลือกในการกรองข้อมูลและไวยากรณ์แบบสอบถาม

[!include [banner](../includes/banner.md)]

บทความนี้อธิบายถึงตัวเลือกในการกรองข้อมูลและการสอบถามที่พร้อมใช้งาน เมื่อคุณใช้กล่องโต้ตอบตัวกรอง/เรียงลำดับขั้นสูง หรือตัวดำเนินการ **การจับคู่** ในตัวกรองบานหน้าต่างตัวกรองหรือส่วนหัวของคอลัมน์ในกริด

## <a name="advanced-query-syntax"></a>ไวยากรณ์แบบสอบถามขั้นสูง

<table>
<thead>
<tr>
<th>ไวยากรณ์</th>
<th>คำอธิบายอักขระ</th>
<th>คำอธิบาย</th>
<th>ตัวอย่าง</th>
</tr>
</thead>
<tbody>
<tr>
<td><em>ค่า</em></td>
<td>เท่ากับค่าที่ป้อน</td>
<td>พิมพ์ค่าที่จะค้นหา</td>
<td><strong>Smith</strong> จะค้นหา &quot;Smith&quot;</td>
</tr>
<tr>
<td>!<em>ค่า</em> (เครื่องหมายอัศเจรีย์)</td>
<td>ไม่เท่ากับค่าที่ป้อน</td>
<td>พิมพ์เครื่องหมายอัศเจรีย์หน้าค่าที่คุณจะแยก</td>
<td><strong>!Smith</strong> จะค้นหาค่าทั้งหมด ยกเว้น &quot;Smith&quot;</td>
</tr>
<tr>
<td><em>จากค่า</em>..<em>ถึงค่า</em> (เครื่องหมายมหัพภาคสองเครื่องหมาย)</td>
<td>ระหว่างสองค่าที่ป้อนถูกแยกด้วยเครื่องหมายมหัพภาคสองเครื่องหมาย</td>
<td>พิมพ์ค่าเริ่มต้น ตามด้วยเครื่องหมายมหัพภาคสองเครื่องหมาย แล้วตามด้วยค่าสิ้นสุด</td>
<td><strong>1..10</strong> จะค้นหาค่าทั้งหมดตั้งแต่ 1 จนถึง 10 อย่างไรก็ตาม ในฟิลด์สตริง <strong>A..C</strong>จะค้นหาค่าทั้งหมดที่ขึ้นต้นด้วย &quot;A&quot; และ &quot;B&quot; และค่าเท่ากับ &quot;C&quot; ตัวอย่างเช่น การสอบถามนี้จะไม่ค้นหา &quot;Ca&quot; เมื่อต้องการค่าทั้งหมดตั้งแต่ &quot;A<em>&quot; จนถึง &quot;C</em>&quot; พิมพ์ <strong>A..D</strong></td>
</tr>
<tr>
<td>..<em>ค่า</em> (เครื่องหมายมหัพภาคสองเครื่องหมาย)</td>
<td>น้อยกว่าหรือเท่ากับค่าที่ป้อน</td>
<td>พิมพ์เครื่องหมายมหัพภาคสองเครื่องหมาย แล้วตามด้วยค่า</td>
<td><strong>..1000</strong> จะค้นหาหมายเลขใดๆ ที่น้อยกว่าหรือเท่ากับ 1000 เช่น &quot;100&quot;, &quot;999.95&quot;และ &quot;1,000&quot;</td>
</tr>
<tr>
<td><em>ค่า</em>.. (เครื่องหมายมหัพภาคสองเครื่องหมาย)</td>
<td>มากกว่าหรือเท่ากับค่าที่ป้อน</td>
<td>พิมพ์ค่า แล้วตามด้วยเครื่องหมายมหัพภาคสองเครื่องหมาย</td>
<td><strong>1000..</strong> จะค้นหาหมายเลขใดๆ ที่มากกว่าหรือเท่ากับ 1000 เช่น &quot;1,000&quot;, &quot;1,000.01&quot;และ &quot;1,000,000&quot;</td>
</tr>
<tr>
<td>&gt;<em>ค่า</em> (เครื่องหมายมากกว่า)</td>
<td>มากกว่าค่าที่ป้อน</td>
<td>พิมพ์เครื่องหมายมากกว่า (<strong>&gt;</strong>) แล้วตามด้วยค่า</td>
<td><strong>&gt;1000</strong> จะค้นหาหมายเลขใดๆ ที่มากกว่าหรือเท่ากับ 1000 เช่น &quot;1000.01&quot;, &quot;20,000&quot;และ &quot;1,000,000&quot;</td>
</tr>
<tr>
<td>&lt;<em>ค่า</em> (เครื่องหมายน้อยกว่า)</td>
<td>น้อยกว่าค่าที่ป้อน</td>
<td>พิมพ์เครื่องหมายน้อยกว่า (<strong>&lt;</strong>) แล้วตามด้วยค่า</td>
<td><strong>&lt;1000</strong> จะค้นหาหมายเลขใดๆ ที่น้อยกว่า 1000 เช่น &quot;999.99&quot;, &quot;1&quot;และ &quot;-200&quot;</td>
</tr>
<tr>
<td><em>ค่า</em>* (ดอกจัน)</td>
<td>เริ่มจากค่าที่ป้อน</td>
<td>พิมพ์ค่าเริ่มต้น แล้วตามด้วยเครื่องหมายดอกจัน (<strong>*</strong>)</td>
<td><strong>S*</strong> จะค้นหาสตริงใดๆ ที่เริ่มต้นด้วย &quot;S&quot; เช่น &quot;Stockholm&quot;, &quot;Sydney&quot;และ &quot;San Francisco&quot;</td>
</tr>
<tr>
<td>*<em>ค่า</em> (ดอกจัน)</td>
<td>สิ้นสุดด้วยค่าที่ป้อน</td>
<td>พิมพ์เครื่องหมายดอกจัน แล้วตามด้วยค่าสิ้นสุด</td>
<td><strong>*east</strong> จะค้นหาสตริงใดๆ ที่สิ้นสุดด้วย &quot;east&quot; เช่น &quot;Northeast&quot; และ &quot;Southeast&quot;</td>
</tr>
<tr>
<td>*<em>value</em>* (ดอกจัน)</td>
<td>มีค่าที่ป้อน</td>
<td>พิมพ์เครื่องหมายดอกจัน ตามด้วยค่า แล้วตามด้วยเครื่องหมายดอกจันอีกอันหนึ่ง</td>
<td><strong>*th*</strong> จะค้นหาสตริงใดๆ ที่มี &quot;th&quot; อยู่ เช่น &quot;Northeast&quot; และ &quot;Southeast&quot;</td>
</tr>
<tr>
<td>? (เครื่องหมายคำถาม)</td>
<td>มีอักขระที่ไม่รู้จักหนึ่งอักขระขึ้นไป</td>
<td>พิมพ์เครื่องหมายคำถามที่ตำแหน่งของอักขระที่ไม่รู้จักในค่า</td>
<td><strong>Sm?th</strong> จะค้นหา &quot;Smith&quot; และ &quot;Smyth&quot;</td>
</tr>
<tr>
<td><em>ค่า</em>,<em>ค่า</em> (เครื่องหมายจุลภาค)</td>
<td>จับคู่ค่าที่ถูกแยกด้วยเครื่องหมายจุลภาค</td>
<td>พิมพ์เงื่อนไขทั้งหมดของคุณ และแยกโดยการใช้เครื่องหมายจุลภาค</td>
<td><strong>A, D, F, G</strong> จะค้นหาค่าที่ตรงกับ &quot;A&quot;, &quot;D&quot;, &quot;F&quot; และ &quot;G&quot; พอดี <strong>10, 20, 30, 100</strong> จะค้นหาค่าที่ตรงกับ &quot;10, 20, 30, 100&quot; พอดี</td>
</tr>
<tr>
<td>(<span class="code">คำสั่ง SQL</span>) (คำสั่ง SQL ในวงเล็บ)</td>
<td>จับคู่การสอบถามที่กำหนด</td>
<td>พิมพ์การสอบถามเป็นคำสั่ง SQL ในวงเล็บ</td>
<td><strong><span class="code">(data source.Fieldname != &quot;A&quot;)</span></strong></td>
</tr>
<tr>
<td>อ.</td>
<td>วันที่ของวันนี้</td>
<td>ชนิด <strong>T</strong></td>
<td><strong>T</strong> ตรงกับวันที่ของวันนี้</td>
</tr>
<tr>
<td>(methodName(parameters)) (<strong>SysQueryRangeUtil</strong> วิธีในวงเล็บ)</td>
<td>การจับคู่ค่าหรือช่วงของค่าที่ระบุโดยพารามิเตอร์ของวิธีการ <strong>SysQueryRangeUtil</strong></td>
<td>พิมพ์วิธีการ <strong>SysQueryRangeUtil</strong> ที่มีพารามิเตอร์ที่ระบุค่าหรือช่วงของค่า</td>
<td>
<ol>
<li>คลิก <strong>บัญชีลูกหนี้</strong> &gt; <strong>ใบแจ้งหนี้</strong> &gt; <strong>ใบแจ้งหนี้ลูกค้าที่เปิด</strong></li>
<li>กด Ctrl + Shift + F3 เพื่อเปิดหน้า <strong>การสอบถาม</strong></li>
<li>บนแท็บ <strong>การกำหนดช่วง</strong> ให้คลิก <strong>เพิ่ม</strong></li>
<li>ชำระธุรกรรมที่ค้างอยู่สำหรับลูกค้าที่เลือก ในฟิลด์ <strong>ตาราง</strong> เลือก <strong>ธุรกรรมลูกค้าที่คงค้าง</strong></li>
<li>ในฟิลด์ <strong>ฟิลด์</strong> ให้เลือก <strong>วันที่ครบกำหนด</strong></li>
<li>ในฟิลด์ <strong>เงื่อนไข</strong> , ให้ป้อน <strong>(yearRange(-2,0))</strong></li>
<li>คลิก <strong>ตกลง</strong> ระบบจะนำเข้าข้อมูลการชำระเงิน หน้ารายการมีการปรับปรุง และแสดงรายการใบแจ้งหนี้ที่ตรงกับเงื่อนไขที่คุณป้อน สำหรับตัวอย่างนี้ จะแสดงรายการใบแจ้งหนี้ที่ครบกำหนดชำระเมื่อสองปีก่อน</li>
</ol>
ดูตารางในส่วนถัดไปสำหรับรายละเอียดเพิ่มเติมเกี่ยวกับวันที่และหลาย ๆ ตัวอย่าง <strong>SysQueryRangeUtil</strong></td>
</tr>
</tbody>
</table>

## <a name="advanced-date-queries-that-use-sysqueryrangeutil-methods"></a>การสอบถามขั้นสูงวันที่ใช้วิธีการ SysQueryRangeUtil

<table>
<thead>
<tr>
<th>วิธีการ</th>
<th>คำอธิบาย</th>
<th>ตัวอย่าง</th>
</tr>
</thead>
<tbody>
<tr>
<td>วัน (_relativeDays = 0)</td>
<td>ค้นหาวันทีที่สัมพันธ์กับวันรอบเวลา ค่าบวกระบุถึง วันที่ในอนาคต และค่าลบระบุวันที่ในอดีต</td>
<td>
<ul>
<li><strong>วันพรุงนี้</strong> – ป้อน <strong>(Day(1))</strong></li>
<li><strong>วันนี้</strong> – ป้อน <strong>(Day(0))</strong></li>
<li><strong>เมื่อวานนี้</strong> – ป้อน <strong>(Day(-1))</strong></li>
</ul>
</td>
</tr>
<tr>
<td>ช่วงวัน (_relativeDaysFrom = 0, _relativeDaysTo = 0)</td>
<td>ค้นหาช่วงวันทีที่สัมพันธ์กับวันรอบเวลา ค่าบวกระบุถึง วันที่ในอนาคต และค่าลบระบุวันที่ในอดีต</td>
<td>
<ul>
<li><strong>30 วันที่ผ่านมา</strong> – ป้อน <strong>(DayRange(-30,0))</strong>.</li>
<li><strong>30 วันก่อนหน้านี้และในอนาคต 30 วัน</strong> – ป้อน <strong>(DayRange(-30,30))</strong></li>
</ul>
</td>
</tr>
<tr>
<td>GreaterThanDate (_relativeDays = 0) GreaterThanUtcDate (_relativeDays = 0)</td>
<td>ค้นหาวันที่ทั้งหมดหลังจากวันที่สัมพัทธ์ถูกระบุ</td>
<td>
<ul>
<li><strong>มากกว่า 30 วันถัดไป</strong>– ป้อน <strong>(GreaterThanDate(30))</strong></li>
</ul>
</td>
</tr>
<tr>
<td>GreaterThanUtcNow ()</td>
<td>ค้นหารายการวันที่ / เวลาทั้งหมดหลังเวลาปัจจุบัน</td>
<td>
<ul>
<li><strong>วัน / เวลาในอนาคตทั้งหมด</strong>– ป้อน <strong>(GreaterThanUtcNow())</strong></li>
</ul>
</td>
</tr>
<tr>
<td>GreaterThanDate (_relativeDays = 0) GreaterThanUtcDate (_relativeDays = 0)</td>
<td>ค้นหาวันที่ทั้งหมดก่อนวันที่สัมพัทธ์ถูกระบุ</td>
<td>
<ul>
<li><strong>น้อยกว่าเจ็ดวันถัดไป</strong>– ป้อน <strong>(LessThanDate(7))</strong></li>
</ul>
</td>
</tr>
<tr>
<td>LessThanUtcNow ()</td>
<td>ค้นหารายการวันที่ / เวลาทั้งหมดก่อนเวลาปัจจุบัน</td>
<td>
<ul>
<li><strong>วัน / เวลาในอดีตทั้งหมด</strong>– ป้อน <strong>(LessThanUtcNow())</strong></li>
</ul>
</td>
</tr>
<tr>
<td>MonthRange (_relativeFrom = 0, _relativeTo = 0)</td>
<td>ค้นหาช่วงวันที่ ตามเดือนที่สัมพันธ์กับเดือนปัจจุบัน</td>
<td>
<ul>
<li><strong>สองเดือนก่อนหน้านี้</strong>– ป้อน <strong>(MonthRange(-2,0))</strong></li>
<li><strong>สามเดือนถัดไป</strong>– ป้อน <strong>(MonthRange(0,3))</strong></li>
</ul>
</td>
</tr>
<tr>
<td>YearRange (_relativeFrom = 0, _relativeTo = 0)</td>
<td>ค้นหาช่วงวันที่ ตามปีที่สัมพันธ์กับปีปัจจุบัน</td>
<td>
<ul>
<li><strong>ปีถัดไป</strong>– ป้อน <strong>(YearRange (0, 1))</strong></li>
<li><strong>ปีก่อนหน้า</strong>– ป้อน <strong>(YearRange (-1,0))</strong></li>
</ul>
</td>
</tr>
</tbody>
</table>

