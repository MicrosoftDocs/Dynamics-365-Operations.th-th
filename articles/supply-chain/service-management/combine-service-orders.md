---
title: รวมใบสั่งบริการ
description: คุณสามารถรวมใบสั่งบริการได้
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
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 17fbed59b1fe7bec80f25f74451872efd61bed62
ms.sourcegitcommit: 708ca25687a4e48271cdcd6d2d22d99fb94cf140
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 10/10/2020
ms.locfileid: "3977011"
---
# <a name="combine-service-orders"></a>รวมใบสั่งบริการ   

[!include [banner](../includes/banner.md)]


เมื่อคุณสร้างรายการใบสั่งบริการได้โดยอัตโนมัติในแบบฟอร์ม **ข้อตกลงการให้บริการ** คุณสามารถเลือกหนึ่งในตัวเลือกต่อไปนี้เพื่อระบุวิธีที่คุณต้องการจัดกลุ่ม:

  - **โดยเรียงตามข้อตกลงการให้บริการ**

  - **โดยเรียงตามงานบริการ**

  - **โดยเรียงตามพนักงาน**

  - **โดยเรียงตามวัตถุที่ให้บริการ**

## <a name="example"></a>ตัวอย่าง

คุณสร้างข้อตกลงการให้บริการที่มีวันที่เริ่มต้นในวันที่ 31-03-2007 ในฟิลด์ **รวมใบสั่งบริการ** คุณระบุ **ตามวัตถุที่ให้บริการ** จากนั้นคุณก็สร้างบรรทัดข้อตกลงการให้บริการต่อไปนี้

<table style="width:100%;">
<colgroup>
<col style="width: 16%" />
<col style="width: 16%" />
<col style="width: 16%" />
<col style="width: 16%" />
<col style="width: 16%" />
<col style="width: 16%" />
</colgroup>
<thead>
<tr class="header">
<th><p>หมายเลขรายการข้อตกลง</p></th>
<th><p>ชนิดธุรกรรม</p></th>
<th><p>คำอธิบาย</p></th>
<th><p>ช่วงเวลา</p></th>
<th><p>วัตถุที่ให้บริการ</p></th>
<th><p>วันที่เริ่มต้น</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>1</p></td>
<td><p><strong>ชั่วโมง</strong></p></td>
<td><p>SAL1</p></td>
<td><p>รายสัปดาห์</p></td>
<td><p>X-1</p></td>
<td><p>วันที่ 04-01-2007</p></td>
</tr>
<tr class="even">
<td><p>2</p></td>
<td><p><strong>ชั่วโมง</strong></p></td>
<td><p>SAL2</p></td>
<td><p>ทุกสองสัปดาห์</p></td>
<td><p>X-2</p></td>
<td><p>วันที่ 04-01-2007</p></td>
</tr>
<tr class="odd">
<td><p>3</p></td>
<td><p><strong>ชั่วโมง</strong></p></td>
<td><p>SAL3</p></td>
<td><p>รายสัปดาห์</p></td>
<td><p>X-2</p></td>
<td><p>วันที่ 04-01-2007</p></td>
</tr>
</tbody>
</table>


คุณไม่ได้ระบุหน้าต่างเวลาสำหรับบรรทัดใดๆ ของข้อตกลงการให้บริการ  ดังนั้น รายการใบสั่งบริการจะไม่ย้ายจากวันที่ที่คำนวณไว้ซึ่งมีรายการเหล่านั้นอยู่

จากนั้น คุณสร้างรายการใบสั่งบริการจากแบบฟอร์ม **สร้างใบสั่งบริการ** ตั้งแต่วันที่ 01-04-2007 จนถึงวันที่ 30-04-2007

คุณสร้างใบสั่งบริการรวมทั้งสิ้น 10 ฉบับ  เนื่องจากการตั้งค่ารวมที่คุณเลือกไว้คือ **โดยเรียงตามวัตถุที่ให้บริการ** ใบสั่งบริการทั้งหมดที่ถูกสร้างขึ้นจึงมีเฉพาะรายการใบสั่งบริการที่มีวัตถุที่ให้บริการรายการเดียว รายการใบสั่งบริการที่ถูกสร้างขึ้นจากข้อตกลงการให้บริการ และมีวันที่ให้บริการเดียวกัน และวัตถุที่ให้บริการจะถูกรวมไว้ในใบสั่งบริการเดียวกัน


> [!NOTE]
> <P>ในตัวอย่างนี้ ปฏิทินที่ถูกระบุไว้ในแบบฟอร์ม <STRONG>พารามิเตอร์การจัดการงานบริการ</STRONG> ไม่มีวันที่ปิด</P>



การจัดกลุ่มรายการใบสั่งบริการเพิ่มเติมเป็นใบสั่งบริการ จะเกิดขึ้นตามกรอบเวลาใดๆ ที่คุณระบุในรายการข้อตกลงการให้บริการ

## <a name="see-also"></a>ดูเพิ่มเติมที่

[สร้างใบสั่งบริการโดยอัตโนมัติ](create-service-orders-automatically.md)

  


