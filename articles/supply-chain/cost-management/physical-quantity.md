---
title: "ค่าออบเจ็กต์สินค้าคงคลัง"
description: "บทความนี้แสดงข้อมูลเกี่ยวกับวิธีคำนวณมูลค่าออบเจ็กต์สินค้าคงคลัง"
author: AndersGirke
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: InventCostOnhandItem
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 19111
ms.assetid: 56a7c8ba-bf4a-4b1d-918d-56bb96926c4f
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: yuyus
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 69eeb90387ca5765c163c7d482295ea104cc078c
ms.openlocfilehash: e4892223d1e92e0483a67b1b473ef20c3f68bbfa
ms.contentlocale: th-th
ms.lasthandoff: 09/29/2017

---

# <a name="inventory-object-values"></a>ค่าออบเจ็กต์สินค้าคงคลัง

[!include[banner](../includes/banner.md)]


บทความนี้แสดงข้อมูลเกี่ยวกับวิธีคำนวณมูลค่าออบเจ็กต์สินค้าคงคลัง 

ฟังก์ชันแบบใหม่ที่ชื่อ **ปริมาณทางกายภาพ**ช่วยให้คุณเห็นมูลค่าของสินค้าคงคลังเฉพาะออบเจ็กต์ 

ออบเจ็กต์ต้นทุนแสดงถึงระดับของเอนทิตี้ที่ทำการลงบัญชีสินค้าคงคลัง สำหรับข้อมูลเพิ่มเติมเกี่ยวกับต้นทุนวัตถุ ดูที่ [ต้นทุนวัตถุ](cost-object.md) 

เมื่เมื่อต้องการดูค่าของสินค้าคงคลังเฉพาะออบเจ็กต์ คลิก **ปริมาณทางกายภาพ** ในหน้า **ออบเจ็กต์ต้นทุน** นี่เป็นวิธีคำนวณมูลค่าของสินค้าคงคลังวัตถุ: 

วัตถุสินค้าคงคลัง มูลค่า = ออบเจ็กต์ต้นทุน.ต้นทุนเฉลี่ยต่อหน่วยxออบเจ็กต์สินค้าคงคลัง.ปริมาณ 

ตัวอย่างต่อไปนี้แสดงวิธีคำนวณค่าของออบเจ็กต์สินค้าคงคลังและต้นทุนวัตถุ เหตุการณ์ใบรับสินค้าสองใบถูกลงทะเบียนในสินค้า A:

-   ใบรับสินค้า 1: ปริมาณ = 100 ชิ้น จำนวนเงิน = $1,000.00 ไซต์ = 1 คลังสินค้า = 11 หมายเลขชุดงาน = B1
-   ใบรับสินค้า 2: ปริมาณ = 50 ชิ้น จำนวนเงิน = $8,00.00 ไซต์ = 1 คลังสินค้า = 11 หมายเลขชุดงาน = B2

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

[ออบเจ็กต์ต้นทุน](cost-object.md)

[รายการต้นทุน](cost-entries.md)

[มีอะไรใหม่และมีการเปลี่ยนแปลง](../../fin-and-ops/get-started/whats-new-changed.md)




