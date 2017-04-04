---
title: "ไวยากรณ์แบบสอบถามและการกรองขั้นสูง"
description: "บทความนี้อธิบายถึงการกรองข้อมูลและตัวเลือกการสอบถามที่พร้อมใช้งานเมื่อคุณใช้ตัวดำเนินการ &quot;รายการตรงกัน&quot; ในกล่องโต้ตอบตัวกรอง/เรียงลำดับขั้นสูง"
author: jasongre
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: SysQueryForm
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 3811
ms.assetid: b4969b30-2fe1-4a3c-bbea-725dc37c8b60
ms.search.region: Global
ms.author: jasongre
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 0c6a7bdc4ba82dd57ab3e395e6dfb0ae4de31fc4
ms.openlocfilehash: 5ee7a04572e350a7c08d0418bade6d332aa920c6
ms.lasthandoff: 03/31/2017


---

# <a name="advanced-filtering-and-query-syntax"></a>ไวยากรณ์แบบสอบถามและการกรองขั้นสูง

บทความนี้อธิบายถึงการกรองข้อมูลและตัวเลือกการสอบถามที่พร้อมใช้งานเมื่อคุณใช้ตัวดำเนินการ "รายการตรงกัน" ในกล่องโต้ตอบตัวกรอง/เรียงลำดับขั้นสูง

<a name="advanced-query-syntax"></a>ไวยากรณ์แบบสอบถามขั้นสูง
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
<th>ไวยากรณ์</th>
<th>คำอธิบายอักขระ</th>
<th>คำอธิบาย</th>
<th>ตัวอย่าง</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><em>ค่า</em></td>
<td>เท่ากับค่าที่ป้อน</td>
<td>พิมพ์ค่าที่จะค้นหา</td>
<td><strong>Smith</strong>ค้นหา&quot;Smith&quot;</td>
</tr>
<tr class="even">
<td>! <em>ค่า</em>(เครื่องหมายอัศเจรีย์)</td>
<td>ไม่เท่ากับค่าที่ป้อน</td>
<td>พิมพ์เครื่องหมายอัศเจรีย์หน้าค่าที่คุณจะแยก</td>
<td><strong>! Smith</strong>ค้นหาค่าทั้งหมดยกเว้น&quot;Smith&quot;</td>
</tr>
<tr class="odd">
<td><em>จากค่า</em>..<em>ถึงค่า</em> (เครื่องหมายมหัพภาคสองเครื่องหมาย)</td>
<td>ระหว่างสองค่าที่ป้อนถูกแยกด้วยเครื่องหมายมหัพภาคสองเครื่องหมาย</td>
<td>พิมพ์ค่าเริ่มต้น ตามด้วยเครื่องหมายมหัพภาคสองเครื่องหมาย แล้วตามด้วยค่าสิ้นสุด</td>
<td><strong>1..10</strong>ค้นหาค่าทั้งหมดตั้งแต่ 1 ถึง 10 อย่างไรก็ตาม ในเขตข้อมูลสตริง<strong>A. C</strong>ค้นหาค่าทั้งหมดที่ขึ้นต้นด้วย&quot;A&quot;และ&quot;B&quot;และค่าที่แน่นอนเท่ากับ&quot;C&quot; ตัวอย่างเช่น แบบสอบถามนี้จะไม่พบ&quot;Ca&quot; เมื่อต้องการค้นหาค่าทั้งหมดจาก&quot;A*&quot;ผ่าน&quot;C*&quot;ชนิด<strong>A. D</strong>.</td>
</tr>
<tr class="even">
<td>..<em>ค่า</em> (เครื่องหมายมหัพภาคสองเครื่องหมาย)</td>
<td>น้อยกว่าหรือเท่ากับค่าที่ป้อน</td>
<td>พิมพ์เครื่องหมายมหัพภาคสองเครื่องหมาย แล้วตามด้วยค่า</td>
<td><strong>.. 1000</strong>ค้นหาหมายเลขใด ๆ ที่น้อยกว่า หรือเท่ากับ 1000 เช่น&quot;100&quot;, &quot;999.95&quot;และ&quot;1000&quot;</td>
</tr>
<tr class="odd">
<td><em>ค่า</em>.. (เครื่องหมายมหัพภาคสองเครื่องหมาย)</td>
<td>มากกว่าหรือเท่ากับค่าที่ป้อน</td>
<td>พิมพ์ค่า แล้วตามด้วยเครื่องหมายมหัพภาคสองเครื่องหมาย</td>
<td><strong>1000..</strong> ค้นหาหมายเลขใด ๆ ที่มากกว่า หรือเท่ากับ 1000 เช่น&quot;1000&quot;, &quot;1,000.01&quot;และ&quot;1000000&quot;</td>
</tr>
<tr class="even">
<td>&gt;<em>ค่า</em>(เครื่องหมายมากกว่า)</td>
<td>มากกว่าค่าที่ป้อน</td>
<td>พิมพ์เครื่องหมายมากกว่า (<strong>&gt;</strong>) และจากนั้นค่า</td>
<td><strong>&gt;1000</strong>ค้นหาหมายเลขใด ๆ ที่มากกว่า 1000 เช่น&quot;1000.01&quot;, &quot;20000&quot;และ&quot;1000000&quot;</td>
</tr>
<tr class="odd">
<td>&lt;<em>ค่า</em>(เครื่องหมายน้อยกว่า)</td>
<td>น้อยกว่าค่าที่ป้อน</td>
<td>พิมพ์น้อยกว่า (<strong>&lt;</strong>) และจากนั้นค่า</td>
<td><strong>&lt;1000</strong>ค้นหาหมายเลขใด ๆ ที่น้อยกว่า 1000 เช่น&quot;999.99&quot;, &quot;1&quot;และ&quot;-200&quot;</td>
</tr>
<tr class="even">
<td><em>ค่า</em>* (เครื่องหมายดอกจัน)</td>
<td>เริ่มจากค่าที่ป้อน</td>
<td>พิมพ์ค่าเริ่มต้น และเครื่องหมายดอกจัน (<strong>*</strong>)</td>
<td><strong>S *</strong>ใด ๆ ที่สายอักขระการค้นหาเริ่มต้นด้วย&quot;S&quot;เช่น&quot;Stockholm&quot;,&quot;ซิดนีย์&quot;และ&quot;ซานฟรานซิสโก&quot;</td>
</tr>
<tr class="odd">
<td>*<em>value</em> (asterisk)</td>
<td>สิ้นสุดด้วยค่าที่ป้อน</td>
<td>พิมพ์เครื่องหมายดอกจัน แล้วตามด้วยค่าสิ้นสุด</td>
<td><strong>* ตะวันออก</strong>ค้นหาที่มีสายอักขระที่จบด้วย&quot;ตะวันออก&quot;เช่น&quot;Northeast&quot;และ&quot;ตะวันออกเฉียงใต้&quot;</td>
</tr>
<tr class="even">
<td>*<em>ค่า</em>* (เครื่องหมายดอกจัน)</td>
<td>มีค่าที่ป้อน</td>
<td>พิมพ์เครื่องหมายดอกจัน ตามด้วยค่า แล้วตามด้วยเครื่องหมายดอกจันอีกอันหนึ่ง</td>
<td><strong>*th*</strong>ประกอบด้วยการค้นหาใด ๆ ที่สตริ&quot;th&quot;เช่น&quot;Northeast&quot;และ&quot;ตะวันออกเฉียงใต้&quot;</td>
</tr>
<tr class="odd">
<td>? (เครื่องหมายคำถาม)</td>
<td>มีอักขระที่ไม่รู้จักหนึ่งอักขระขึ้นไป</td>
<td>พิมพ์เครื่องหมายคำถามที่ตำแหน่งของอักขระที่ไม่รู้จักในค่า</td>
<td><strong>Sm ? th</strong>ค้นหา&quot;Smith&quot;และ&quot;Smyth&quot;</td>
</tr>
<tr class="even">
<td><em>ค่า</em>,<em>ค่า</em> (เครื่องหมายจุลภาค)</td>
<td>จับคู่ค่าที่ถูกแยกด้วยเครื่องหมายจุลภาค</td>
<td>พิมพ์เงื่อนไขทั้งหมดของคุณ และแยกโดยการใช้เครื่องหมายจุลภาค</td>
<td><strong>A, D, F, G</strong> finds exactly &quot;A&quot;, &quot;D&quot;, &quot;F&quot;, and &quot;G&quot;. <strong>10, 20, 30, 100</strong>ค้นหาอย่างแน่นอน&quot;10, 20, 30, 100&quot;</td>
</tr>
<tr class="odd">
<td>(<span class="code">คำสั่ง SQL</span>) (คำสั่ง SQL ในวงเล็บ)</td>
<td>จับคู่การสอบถามที่กำหนด</td>
<td>พิมพ์การสอบถามเป็นคำสั่ง SQL ในวงเล็บ</td>
<td><strong><span class="code">(แหล่งข้อมูล ชื่อเขตข้อมูล! = &quot;A&quot;)</span></strong></td>
</tr>
<tr class="even">
<td>อ.</td>
<td>วันที่ของวันนี้</td>
<td>ชนิด <strong>T</strong></td>
<td><strong>T</strong> ตรงกับวันที่ของวันนี้</td>
</tr>
<tr class="odd">
<td>(methodName(parameters)) (<strong>SysQueryRangeUtil</strong> วิธีในวงเล็บ)</td>
<td>การจับคู่ค่าหรือช่วงของค่าที่ระบุโดยพารามิเตอร์ของวิธีการ <strong>SysQueryRangeUtil</strong></td>
<td>พิมพ์วิธีการ <strong>SysQueryRangeUtil</strong> ที่มีพารามิเตอร์ที่ระบุค่าหรือช่วงของค่า</td>
<td><ol>
<li>คลิ<strong>บัญชีลูกหนี้</strong>&gt;<strong>ใบแจ้งหนี้</strong>&gt;<strong>เปิดใบแจ้งหนี้ลูกค้า</strong></li>
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
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th>วิธีการ</th>
<th>คำอธิบาย</th>
<th>ตัวอย่าง</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>วัน (_relativeDays = 0)</td>
<td>ค้นหาวันทีที่สัมพันธ์กับวันรอบเวลา ค่าบวกระบุถึง วันที่ในอนาคต และค่าลบระบุวันที่ในอดีต</td>
<td><ul>
<li><strong>วันพรุงนี้</strong> – ป้อน <strong>(Day(1))</strong></li>
<li><strong>วันนี้</strong> – ป้อน <strong>(Day(0))</strong></li>
<li><strong>เมื่อวานนี้</strong> – ป้อน <strong>(Day(-1))</strong></li>
</ul></td>
</tr>
<tr class="even">
<td>ช่วงวัน (_relativeDaysFrom = 0, _relativeDaysTo = 0)</td>
<td>ค้นหาช่วงวันทีที่สัมพันธ์กับวันรอบเวลา ค่าบวกระบุถึง วันที่ในอนาคต และค่าลบระบุวันที่ในอดีต</td>
<td><ul>
<li><strong>30 วันที่ผ่านมา</strong> – ป้อน <strong>(DayRange(-30,0))</strong>.</li>
<li><strong>30 วันก่อนหน้านี้และในอนาคต 30 วัน</strong> – ป้อน <strong>(DayRange(-30,30))</strong></li>
</ul></td>
</tr>
<tr class="odd">
<td>GreaterThanDate (_relativeDays = 0) GreaterThanUtcDate (_relativeDays = 0)</td>
<td>ค้นหาวันที่ทั้งหมดหลังจากวันที่สัมพัทธ์ถูกระบุ</td>
<td><ul>
<li><strong>มากกว่า 30 วันถัดไป</strong>– ป้อน <strong>(GreaterThanDate(30))</strong></li>
</ul></td>
</tr>
<tr class="even">
<td>GreaterThanUtcNow ()</td>
<td>ค้นหารายการวันที่ / เวลาทั้งหมดหลังเวลาปัจจุบัน</td>
<td><ul>
<li><strong>วัน / เวลาในอนาคตทั้งหมด</strong>– ป้อน <strong>(GreaterThanUtcNow())</strong></li>
</ul></td>
</tr>
<tr class="odd">
<td>GreaterThanDate (_relativeDays = 0) GreaterThanUtcDate (_relativeDays = 0)</td>
<td>ค้นหาวันที่ทั้งหมดก่อนวันที่สัมพัทธ์ถูกระบุ</td>
<td><ul>
<li><strong>น้อยกว่าเจ็ดวันถัดไป</strong>– ป้อน <strong>(LessThanDate(7))</strong></li>
</ul></td>
</tr>
<tr class="even">
<td>LessThanUtcNow ()</td>
<td>ค้นหารายการวันที่ / เวลาทั้งหมดก่อนเวลาปัจจุบัน</td>
<td><ul>
<li><strong>วัน / เวลาในอดีตทั้งหมด</strong>– ป้อน <strong>(LessThanUtcNow())</strong></li>
</ul></td>
</tr>
<tr class="odd">
<td>MonthRange (_relativeFrom = 0, _relativeTo = 0)</td>
<td>ค้นหาช่วงวันที่ ตามเดือนที่สัมพันธ์กับเดือนปัจจุบัน</td>
<td><ul>
<li><strong>สองเดือนก่อนหน้านี้</strong>– ป้อน <strong>(MonthRange(-2,0))</strong></li>
<li><strong>สามเดือนถัดไป</strong>– ป้อน <strong>(MonthRange(0,3))</strong></li>
</ul></td>
</tr>
<tr class="even">
<td>YearRange (_relativeFrom = 0, _relativeTo = 0)</td>
<td>ค้นหาช่วงวันที่ ตามปีที่สัมพันธ์กับปีปัจจุบัน</td>
<td><ul>
<li><strong>ปีถัดไป</strong>– ป้อน <strong>(YearRange (0, 1))</strong></li>
<li><strong>ปีก่อนหน้า</strong>– ป้อน <strong>(YearRange (-1,0))</strong></li>
</ul></td>
</tr>
</tbody>
</table>




