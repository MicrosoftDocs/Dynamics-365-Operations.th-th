---
title: ตัวอย่างวันในการลด
description: ตัวอย่างวันในการลด
author: ShylaThompson
manager: tfehr
ms.date: 05/01/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SMASubscriptionTable
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 509d1a9e2abd79938376209d8feab1b935394833
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 01/15/2021
ms.locfileid: "5010533"
---
# <a name="reduction-days-example"></a>ตัวอย่างวันในการลด 

[!include [banner](../includes/banner.md)]


คุณได้สร้างธุรกรรมการบอกรับสมัครสมาชิกสำหรับการบอกรับสมัครสมาชิกการบำรุงรักษาของลูกค้า ตามที่อธิบายในตารางดังต่อไปนี้

<table>
<colgroup>
<col style="width: 12%" />
<col style="width: 12%" />
<col style="width: 12%" />
<col style="width: 12%" />
<col style="width: 12%" />
<col style="width: 12%" />
<col style="width: 12%" />
<col style="width: 12%" />
</colgroup>
<thead>
<tr class="header">
<th><p>วันที่เริ่มต้น</p></th>
<th><p>วันที่สิ้นสุด</p></th>
<th><p>การบอกรับเป็นสมาชิก</p></th>
<th><p>ชนิดของการบอกรับเป็นสมาชิก</p></th>
<th><p>Project</p></th>
<th><p>ประเภท</p></th>
<th><p>สกุลเงินที่ใช้ในการขาย</p></th>
<th><p>ราคาขาย</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>01 มีนาคม 2011</p></td>
<td><p>31 มีนาคม 2011</p></td>
<td><p>NR-2</p></td>
<td><p><strong>เป็นประจำ</strong></p></td>
<td><p>9013</p></td>
<td><p>SubCat2</p></td>
<td><p>EUR</p></td>
<td><p>200.00</p></td>
</tr>
</tbody>
</table>


ลูกค้ารายงานว่าไม่จำเป็นต้องใช้การครอบคลุมบริการเป็นเวลาสองวัน (10 มีนาคม และ 11 มีนาคม) คุณตกลงลดการสมัครสมาชิกในเวลาสองวันนี้

คุณสร้างธุรกรรมใหม่ของชนิด **จำนวนวันที่ลด** ดังที่อธิบายในตารางดังต่อไปนี้

<table>
<colgroup>
<col style="width: 12%" />
<col style="width: 12%" />
<col style="width: 12%" />
<col style="width: 12%" />
<col style="width: 12%" />
<col style="width: 12%" />
<col style="width: 12%" />
<col style="width: 12%" />
</colgroup>
<thead>
<tr class="header">
<th><p>วันที่เริ่มต้น</p></th>
<th><p>วันที่สิ้นสุด</p></th>
<th><p>การบอกรับเป็นสมาชิก</p></th>
<th><p>ชนิดของการบอกรับเป็นสมาชิก</p></th>
<th><p>Project</p></th>
<th><p>ประเภท</p></th>
<th><p>สกุลเงินที่ใช้ในการขาย</p></th>
<th><p>ราคาขาย</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>10 มีนาคม 2011</p></td>
<td><p>11 มีนาคม 2011</p></td>
<td><p>NR-2</p></td>
<td><p><strong>จำนวนวันที่ลด</strong></p></td>
<td><p>9013</p></td>
<td><p>SubCat2</p></td>
<td><p>EUR</p></td>
<td><p>-12.90</p></td>
</tr>
</tbody>
</table>


เมื่อธุรกรรมสำหรับเดือนมีนาคม 2011 มีการออกใบแจ้งหนี้แล้ว ราคาขาย EUR 200 จะถูกลดลง EUR 12.90 ราคาขาย EUR 200 จะลดลงจำนวน EUR 12.90 จำนวนที่คิดค่าธรรมเนียมได้ของธุรกรรมการบอกรับการสมัครสมาชิกดังนั้นก็จะเป็น EUR 187.10 และสองธุรกรรมจะออกใบแจ้งหนี้ที่ยอด EUR 187.10

## <a name="see-also"></a>ดูเพิ่มเติมที่

[การลดจำนวนวันของค่าธรรมเนียมการสั่งซื้อโดยบอกรับเป็นสมาชิก](reduce-the-days-on-subscription-fees.md)

  


