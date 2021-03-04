---
title: การระบุวิธีการตัดจำหน่ายสินค้าที่ส่งคืน
description: ระบุวิธีการตัดจำหน่ายสินค้าที่ส่งคืน
author: ShylaThompson
manager: tfehr
ms.date: 05/07/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventQuarantineOrder
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: b2b1468328433a67253bafc21ac9c9b3a2398872
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 10/13/2020
ms.locfileid: "4438152"
---
# <a name="specify-how-to-dispose-of-returned-items"></a>การระบุวิธีการตัดจำหน่ายสินค้าที่ส่งคืน 

[!include [banner](../includes/banner.md)]


เมื่อคุณจัดการใบสั่งส่งคืนสินค้า คุณต้องระบุรหัสเหตุผลการส่งคืนเพื่อระบุสาเหตุที่ส่งคืนผลิตภัณฑ์  และคุณยังต้องระบุรหัสการโอนการครอบครองและการดำเนินการจัดการต่อรายการสินค้าเพื่อกำหนดสิ่งที่ควรจะดำเนินการกับตัวสินค้าที่ส่งคืน

รหัสการโอนการครอบครองสามารถใช้ได้เมื่อคุณสร้างใบสั่งส่งคืนสินค้า ลงทะเบียนการมาถึงของสินค้า หรืออัพเดตบันทึกการจัดส่งตามการมาถึงของสินค้า และเมื่อสิ้นสุดใบสั่งตรวจสอบสินค้า

คุณสามารถกำหนดรหัสการโอนการครอบครองใดๆ ที่คุณต้องใช้เพื่อสนับสนุนกระบวนการทางธุรกิจได้  ตารางต่อไปนี้แสดงชุดของรหัสที่ใช้กันโดยทั่วไปเพื่อกำหนดการโอนการครอบครองสินค้าที่ส่งคืน

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p>ชนิดการโอนการครอบครอง</p></th>
<th><p>รหัสทั่วไป</p></th>
<th><p>คำอธิบาย</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>การตัดจำหน่าย</p></td>
<td><p>SC</p></td>
<td><p>การกำจัดเป็นเศษซาก/ทำลาย</p></td>
</tr>
<tr class="even">
<td><p>การตัดจำหน่าย</p></td>
<td><p>DC</p></td>
<td><p>การบริจาค</p></td>
</tr>
<tr class="odd">
<td><p>การตัดจำหน่าย</p></td>
<td><p>TD</p></td>
<td><p>การตัดจำหน่ายให้แก่บุคคลที่สาม</p></td>
</tr>
<tr class="even">
<td><p>การตัดจำหน่าย</p></td>
<td><p>SL</p></td>
<td><p>เศษซาก</p></td>
</tr>
<tr class="odd">
<td><p>การตัดจำหน่าย</p></td>
<td><p>TS</p></td>
<td><p>การขายให้แก่บุคคลที่สาม (ตลาดสินค้ามือสอง)</p></td>
</tr>
<tr class="even">
<td><p>การซ่อมแซม/ปรับเปลี่ยน</p></td>
<td><p>RW</p></td>
<td><p>การทำใหม่</p></td>
</tr>
<tr class="odd">
<td><p>การซ่อมแซม/ปรับเปลี่ยน</p></td>
<td><p>RF</p></td>
<td><p>การผลิตใหม่/ตกแต่งใหม่</p></td>
</tr>
<tr class="even">
<td><p>การซ่อมแซม/ปรับเปลี่ยน</p></td>
<td><p>MD</p></td>
<td><p>การปรับเปลี่ยน</p></td>
</tr>
<tr class="odd">
<td><p>การซ่อมแซม/ปรับเปลี่ยน</p></td>
<td><p>RP</p></td>
<td><p>การซ่อมแซม</p></td>
</tr>
<tr class="even">
<td><p>การซ่อมแซม/ปรับเปลี่ยน</p></td>
<td><p>RV</p></td>
<td><p>การส่งคืนให้แก่ผู้จัดจำหน่าย</p></td>
</tr>
<tr class="odd">
<td><p>อื่นๆ</p></td>
<td><p>AI</p></td>
<td><p>การใช้ตามสภาพ</p></td>
</tr>
<tr class="even">
<td><p>อื่นๆ</p></td>
<td><p>RS</p></td>
<td><p>การขายใหม่</p></td>
</tr>
<tr class="odd">
<td><p>อื่นๆ</p></td>
<td><p>EX</p></td>
<td><p>แลกเปลี่ยน</p></td>
</tr>
<tr class="even">
<td><p>อื่นๆ</p></td>
<td><p>MS</p></td>
<td><p>เบ็ดเตล็ด</p></td>
</tr>
</tbody>
</table>


สำหรับแต่ละรหัสการโอนการครอบครองที่คุณกำหนด คุณต้องเลือกการดำเนินการโอนการครอบครอง  การดำเนินการโอนการครอบครองจะกำหนดผลกระทบทางกายภาพและทางการเงินของรหัสการโอนการครอบครอง  ตัวอย่างเช่น การดำเนินการโอนการครอบครองจะกำหนดว่าการจัดการที่เกิดขึ้นจริงของสินค้าที่ส่งคืน ผลกระทบทางการเงินของสินค้าที่ส่งคืน และถ้าสินค้าทดแทนต้องถูกส่งไปยังลูกค้า  คุณสามารถกำหนดจำนวนที่ไม่จำกัดของรหัสการโอนการครอบครองตามความต้องการทางธุรกิจของคุณได้ แต่คุณสามารถเลือกการดำเนินการโอนการครอบครองที่กำหนดไว้ล่วงหน้าได้เพียงหกแบบเท่านั้น  ตารางต่อไปนี้แสดงการดำเนินการโอนการครอบครองและคำนิยาม

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>การดำเนินการโอนการครอบครอง</p></th>
<th><p>คำอธิบาย</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><strong>เครดิต</strong></p></td>
<td><p>ส่งคืนสินค้าไปยังสินค้าคงคลังและให้เครดิตลูกค้า</p></td>
</tr>
<tr class="even">
<td><p><strong>เครดิตอย่างเดียว</strong></p></td>
<td><p>ให้เครดิตลูกค้าได้โดยไม่จำเป็นต้องใช้หรือต้องการรับสินค้าคืน</p></td>
</tr>
<tr class="odd">
<td><p><strong>เศษซาก</strong></p></td>
<td><p>คิดสินค้าเป็นของเสีย และให้เครดิตลูกค้า</p></td>
</tr>
<tr class="even">
<td><p><strong>แทนที่และเครดิต</strong></p></td>
<td><p>ส่งคืนสินค้าไปยังสินค้าคงคลัง สร้างใบสั่งเปลี่ยนทดแทน และให้เครดิตลูกค้า</p></td>
</tr>
<tr class="odd">
<td><p><strong>แทนที่และหักของเสีย</strong></p></td>
<td><p>คิดสินค้าเป็นของเสีย สร้างใบสั่งเปลี่ยนทดแทน และให้เครดิตลูกค้า</p></td>
</tr>
<tr class="even">
<td><p><strong>ส่งคืนให้ลูกค้า</strong></p></td>
<td><p>ปฏิเสธสินค้าที่ส่งคืน และส่งคืนสินค้าให้กับลูกค้า</p></td>
</tr>
</tbody>
</table>


## <a name="select-a-disposition-code-for-a-quarantine-order"></a>การเลือกรหัสการโอนการครอบครองสำหรับใบสั่งตรวจสอบสินค้า

1.  คลิก **การบริหารสินค้าคงคลังt** \> **งานประจำงวด** \> **การจัดการคุณภาพ** \> **ใบสั่งตรวจสอบสินค้า**

2.  สำหรับใบสั่งตรวจสอบสินค้าที่มีอยู่ ให้เลือกการดำเนินการจากฟิลด์ **รหัสการโอนการครอบครอง** บนแท็บ **ภาพรวม**



## <a name="see-also"></a>ดูเพิ่มเติมที่

[ใบสั่งตรวจสอบสินค้า (แบบฟอร์ม)](https://technet.microsoft.com/library/aa554073(v=ax.60))

[รหัสการจัดการ (แบบฟอร์ม)](https://technet.microsoft.com/library/hh597113\(v=ax.60\))

  




[!INCLUDE[footer-include](../../includes/footer-banner.md)]