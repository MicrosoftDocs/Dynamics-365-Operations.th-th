---
title: สถานะการให้บริการและการโต้ตอบของฟิลด์ความก้าวหน้า
description: ในแบบฟอร์มใบสั่งบริการ ฟิลด์กระบวนการบนส่วนหัวจะแสดงสถานะของใบสั่งบริการทั้งหมด และสถานะจะรายงานสถานะของรายการของใบสั่งบริการแต่ละรายการ
author: ShylaThompson
manager: tfehr
ms.date: 05/01/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SMAServiceOrderTable
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: ShylaThompson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: bd70d00f7ce531b225362065dfd9f1f5c1adc754
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 04/02/2020
ms.locfileid: "3207335"
---
# <a name="service-status-and-progress-field-interaction"></a>สถานะการให้บริการและการโต้ตอบของฟิลด์ความก้าวหน้า 

[!include [banner](../includes/banner.md)]


ในแบบฟอร์ม **ใบสั่งบริการ** ฟิลด์ **กระบวนการ** บนส่วนหัวของใบสั่งบริการ จะแสดงสถานะของใบสั่งบริการทั้งหมด และ **สถานะ** จะรายงานสถานะของรายการของใบสั่งบริการแต่ละรายการ

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p>ความคืบหน้า</p></th>
<th><p>สถานะบรรทัด 1</p></th>
<th><p>สถานะบรรทัด 2</p></th>
<th><p>สถานะบรรทัด 3</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><strong>อยู่ระหว่างดำเนินการ</strong></p></td>
<td><p><strong>สร้างแล้ว</strong></p></td>
<td><p><strong>สร้างแล้ว</strong></p></td>
<td><p><strong>สร้างแล้ว</strong></p></td>
</tr>
<tr class="even">
<td><p><strong>อยู่ระหว่างดำเนินการ</strong></p></td>
<td><p><strong>ยกเลิก</strong></p></td>
<td><p><strong>สร้างแล้ว</strong></p></td>
<td><p><strong>สร้างแล้ว</strong></p></td>
</tr>
<tr class="odd">
<td><p><strong>อยู่ระหว่างดำเนินการ</strong></p></td>
<td><p><strong>สร้างแล้ว</strong></p></td>
<td><p><strong>ยกเลิก</strong></p></td>
<td><p><strong>ประกาศแล้ว</strong></p></td>
</tr>
<tr class="even">
<td><p><strong>ยกเลิก</strong></p></td>
<td><p><strong>ยกเลิก</strong></p></td>
<td><p><strong>ยกเลิก</strong></p></td>
<td><p><strong>ยกเลิก</strong></p></td>
</tr>
<tr class="odd">
<td><p><strong>ประกาศแล้ว</strong></p></td>
<td><p><strong>ประกาศแล้ว</strong></p></td>
<td><p><strong>ประกาศแล้ว</strong></p></td>
<td><p><strong>ประกาศแล้ว</strong></p></td>
</tr>
<tr class="even">
<td><p><strong>ประกาศแล้ว</strong></p></td>
<td><p><strong>ประกาศแล้ว</strong></p></td>
<td><p><strong>ยกเลิก</strong></p></td>
<td><p><strong>ยกเลิก</strong></p></td>
</tr>
</tbody>
</table>


ความก้าวหน้าของใบสั่งบริการอยู่ระหว่างดำเนินการ หากทุกรายการมีสถานะ **สร้างแล้ว**; ใบสั่งนั้นยังอยู่ระหว่างดำเนินการ หากบางรายการมีสถานะเป็น **ยกเลิกแล้ว** หรือ **ลงรายการบัญชีแล้ว**

ถ้าทุกรายการใบสั่งบริการถูกทำเครื่องหมายเป็น **ลงรายการบัญชีแล้ว** ความก้าวหน้าของใบสั่งสถานะจะเป็น **ลงรายการบัญชีแล้ว** ถ้าบางรายการเป็น **ลงรายการบัญชีแล้ว** และบางรายการเป็น **ยกเลิกแล้ว** ความก้าวหน้าจะยังคงเป็น **ลงรายการบัญชีแล้ว**

  


