---
title: "ค่าวัตถุสินค้าคงคลัง"
description: "บทความนี้แสดงข้อมูลเกี่ยวกับวิธีคำนวณมูลค่าออบเจ็กต์สินค้าคงคลัง"
author: YuyuScheller
manager: AnnBe
ms.date: 2015-12-07 09 - 09 - 05
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: InventCostOnhandItem
audience: Application User
ms.reviewer: YuyuScheller
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 19111
ms.assetid: 56a7c8ba-bf4a-4b1d-918d-56bb96926c4f
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: yuyus
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 7a0a2af2094e3e5be757d3dd82255769677b96ea
ms.openlocfilehash: 8898d5d91ffb4f73ea68f1251e1a99440e81bcd4
ms.lasthandoff: 03/29/2017


---

# <a name="inventory-object-values"></a>ค่าวัตถุสินค้าคงคลัง

บทความนี้แสดงข้อมูลเกี่ยวกับวิธีคำนวณมูลค่าออบเจ็กต์สินค้าคงคลัง 

การทำงานใหม่ ๆ ที่ชื่อ ** ปริมาณทางกายภาพ ** ช่วยให้คุณสามารถดูค่าของสินค้าคงคลังเฉพาะวัตถุ ออบเจ็กต์ต้นทุนแสดงถึงระดับของเอนทิตี้ที่ทำการลงบัญชีสินค้าคงคลัง สำหรับข้อมูลเพิ่มเติมเกี่ยวกับต้นทุนวัตถุ ดูที่ [ต้นทุนวัตถุ](cost-object.md) เมื่อต้องการดูค่าของสินค้าคงคลังเฉพาะวัตถุ คลิ**ปริมาณทางกายภาพ**ในการ**ต้นทุนวัตถุ**หน้า ต่อไปนี้คือวิธีคำนวณมูลค่าของสินค้าคงคลังวัตถุ: วัตถุที่มีสินค้าคงคลัง มูลค่า =ต้นทุนวัตถุ เฉลี่ยวัตถุสินค้าคงคลังในต้นทุนต่อหน่วย ปริมาณตัวอย่างต่อไปนี้แสดงวิธีคำนวณค่าของสินค้าคงคลังวัตถุและวัตถุที่เป็นต้นทุน เหตุการณ์ใบรับสินค้าสองใบถูกลงทะเบียนในสินค้า A:

-   รับผลิตภัณฑ์ 1: ปริมาณ = 100 ชิ้น ยอดเงิน = $1,000.00 ไซต์ = 1 คลังสินค้า = 11 หมายเลขชุดงาน = B1
-   รับสินค้า 2: ปริมาณ = 50 ชิ้น ยอดเงิน = $800.00 ไซต์ = 1 คลังสินค้า = 11 หมายเลขชุดงาน = B2

ตารางต่อไปนี้แสดงผลลัพธ์การคำนวณสำหรับออบเจ็กต์ต้นทุน คุณสามารถดูผลลัพธ์ในหน้า **ออบเจ็กต์ต้นทุน**

<table style="width:100%;">
<colgroup>
<col width="14%" />
<col width="14%" />
<col width="14%" />
<col width="14%" />
<col width="14%" />
<col width="14%" />
<col width="14%" />
</colgroup>
<thead>
<tr class="header">
<th>ชนิดออบเจ็กต์</th>
<th>หมายเลขสินค้า</th>
<th>ไซต์</th>
<th>ปริมาณ</th>
<th>หน่วยสินค้าคงคลัง</th>
<th>มูลค่า</th>
<th>ต้นทุนเฉลี่ยต่อหน่วย</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>ออบเจ็กต์ต้นทุน</td>
<td>A</td>
<td>1</td>
<td>150</td>
<td>หน่วย</td>
<td><p>$1800.00</p></td>
<td><p>$12.00</p></td>
</tr>
</tbody>
</table>

ตารางต่อไปนี้แสดงผลลัพธ์การคำนวณสำหรับออบเจ็กต์สินค้าคงคลัง คุณสามารถดูผลลัพธ์โดยการคลิก **ปริมาณกายภาพ** บนหน้า **ออบเจ็กต์ต้นทุน**

<table style="width:100%;">
<colgroup>
<col width="11%" />
<col width="11%" />
<col width="11%" />
<col width="11%" />
<col width="11%" />
<col width="11%" />
<col width="11%" />
<col width="11%" />
<col width="11%" />
</colgroup>
<thead>
<tr class="header">
<th>ชนิดออบเจ็กต์</th>
<th>หมายเลขสินค้า</th>
<th>ไซต์</th>
<th>คลังสินค้า</th>
<th>หมายเลขชุดงาน</th>
<th>ปริมาณ</th>
<th>หน่วยสินค้าคงคลัง</th>
<th>มูลค่า</th>
<th>ต้นทุนเฉลี่ยต่อหน่วย</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>ออบเจ็กต์สินค้าคงคลัง</td>
<td>A</td>
<td>1</td>
<td>11</td>
<td>B1</td>
<td>100</td>
<td>หน่วย</td>
<td><p>$1200.00</p></td>
<td><p>$12.00</p></td>
</tr>
<tr class="even">
<td>ออบเจ็กต์สินค้าคงคลัง</td>
<td>A</td>
<td>1</td>
<td>11</td>
<td>B2</td>
<td>50</td>
<td>หน่วย</td>
<td><p>$600.00</p></td>
<td><p>$12.00</p></td>
</tr>
</tbody>
</table>



<a name="see-also"></a>ดูเพิ่มเติมที่
--------

[Cost objects](cost-object.md)

[Cost entries](cost-entries.md)

[มีอะไรใหม่ และที่เปลี่ยนแปลงใน Microsoft Dynamics AX](/dynamics365/operations/dev-itpro/get-started/whats-new-changed)


