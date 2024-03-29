---
title: โพรไฟล์การลงรายการบัญชีผู้จัดจำหน่าย
description: โพรไฟล์การลงรายการบัญชีผู้จัดจำหน่ายควบคุมการลงรายการบัญชีของธุรกรรมผู้จัดจำหน่ายที่บัญชีแยกประเภททั่วไป
author: abruer
ms.date: 11/21/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: twheeloc
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.custom: 24691
ms.assetid: 18def866-7655-4f0b-b299-eec83098d23a
ms.search.form: VendPosting
ms.openlocfilehash: 09f27ef510f38c10fc265b682a492ba5872b6d3e
ms.sourcegitcommit: fb9b6969218f2b82f0a4c72bfad75387fe00395c
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 11/22/2022
ms.locfileid: "9799611"
---
# <a name="vendor-posting-profiles"></a>โพรไฟล์การลงรายการบัญชีผู้จัดจำหน่าย

[!include [banner](../includes/banner.md)]

โพรไฟล์การลงรายการบัญชีผู้จัดจำหน่ายควบคุมการลงรายการบัญชีของธุรกรรมผู้จัดจำหน่ายที่บัญชีแยกประเภททั่วไป

## <a name="vendor-posting-profiles"></a>โพรไฟล์การลงรายการบัญชีผู้จัดจำหน่าย

โพรไฟล์การลงรายการบัญชีผู้จัดจำหน่ายช่วยให้คุณสามารถกำหนดบัญชีแยกประเภททั่วไปและการตั้งค่าเอกสารให้กับผู้จัดจำหน่ายทั้งหมด กลุ่มผู้จัดจำหน่าย หรือผู้จัดจำหน่ายรายเดียวได้ การตั้งค่าเหล่านี้จะถูกใช้เมื่อคุณสร้างใบสั่งซื้อ ใบแจ้งหนี้ของผู้จัดจำหน่าย และการชำระเงินสด สำหรับบางธุรกรรม คุณสามารถเลือกโพรไฟล์การลงรายการบัญชีที่แตกต่าง และมีระดับความสำคัญเหนือกว่าโพรไฟล์การลงรายการบัญชีที่ตั้งค่าไว้สำหรับธุรกรรมในหน้านี้ โพรไฟล์การลงรายการบัญชีเริ่มต้นจะถูกกำหนดไว้ใน FastTab **บัญชีแยกประเภทและภาษีขาย** บนหน้า **พารามิเตอร์บัญชีเจ้าหนี้** จากนั้น โพรไฟล์การลงรายการบัญชีเริ่มต้นจะถูกรวมอยู่ในส่วนหัวของเอกสารใหม่โดยอัตโนมัติ ที่ซึ่งคุณสามารถเปลี่ยนเป็นโพรไฟล์การลงรายการบัญชีอื่นได้ หากจำเป็น

นอกจากนี้ คุณยังสามารถเชื่อมโยงข้อกำหนดการลงรายการบัญชีกับชนิดการลงรายการบัญชีธุรกรรมในหน้า **ข้อกำหนดการลงรายการบัญชีของธุรกรรม** ข้อกำหนดการลงรายการบัญชีจะควบคุมการลงรายการบัญชีขอธุรกรรมผู้จัดจำหน่ายไปยังบัญชีแยกประเภททั่วไปแทนข้อกำหนดการลงรายการบัญชี

## <a name="creating-a-posting-profile"></a>การสร้างการลงรายการบัญชี
### <a name="setup"></a>**การตั้งค่า**

ระบุบัญชีแยกประเภทที่จะใช้ในการลงรายการบัญชีธุรกรรมที่มีโพรไฟล์การลงบัญชีที่เลือกไว้ เลือกรหัสบัญชี และหากเป็นไปได้ เลือกหมายเลขบัญชีหรือหมายเลขกลุ่มสำหรับโพรไฟล์การลงบัญชีที่เลือกไว้ ในกระบวนการลงรายการบัญชี ข้อมูลโพรไฟล์การลงรายการบัญชีที่เหมาะสมที่สุดสำหรับธุรกรรมแต่ละรายการจะถูกระบุโดยการค้นหารหัสบัญชี หมายเลขบัญชี หรือส่วนผสมระหว่างกลุ่มและหมายเลขที่เจาะจงที่สุด ตามระดับความสำคัญดังต่อไปนี้

| ค่าฟิลด์ **รหัสบัญชี** | ค่าฟิลด์ **หมายเลขบัญชี/กลุ่ม**        | ระดับความสำคัญของการค้นหา |
|------------------------------|---------------------------------------------|-----------------|
| **ตาราง**                    | บัญชีผู้จัดจำหน่ายที่ระบุ                     | 1               |
| **กลุ่ม**                    | กลุ่มผู้จัดจำหน่ายที่ถูกกำหนดให้แก่ผู้จัดจำหน่าย | 2               |
| **ทั้งหมด**                      | ว่างเปล่า                                       | 3               |

ถ้าคุณต้องการให้ธุรกรรมของผู้จัดจำหน่ายทั้งหมดมีโพรไฟล์การลงรายการบัญชีเหมือนกัน ให้ตั้งค่าโพรไฟล์การลงรายการบัญชีเพียงหนึ่งรายการด้วย **ทั้งหมด** ในฟิลด์ **รหัสบัญชี** ระบุค่าต่อไปนี้เพื่อตั้งค่าโพรไฟล์การลงรายการบัญชีของคุณ

<table>
<thead>
<tr class="header">
<th>ฟิลด์</th>
<th>คำอธิบาย</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><strong>โพรไฟล์การลงรายการบัญชี</strong></td>
<td>ป้อนรหัสสำหรับโพรไฟล์การลงบัญชี ตัวอย่างเช่น คุณสามารถสร้างโพรไฟล์การลงบัญชี 2 โพรไฟล์ เพื่อให้มีหนึ่งบัญชีสำหรับยอดดุลผู้จัดจำหน่ายในสกุลเงินในประเทศ และอีกบัญชีหนึ่งสำหรับยอดดุลผู้จัดจำหน่ายในสกุลเงินต่างประเทศ คุณสามารถเรียกบัญชีหนึ่งว่าในประเทศ และอีกบัญชีหนึ่งว่าต่างประเทศ</td>
</tr>
<tr class="even">
<td><strong>คำอธิบาย</strong></td>
<td>ป้อนคำอธิบายเกี่ยวโพรไฟล์การลงรายการบัญชี</td>
</tr>
<tr class="odd">
<td><strong>รหัสบัญชี</strong></td>
<td>ระบุว่าจะใช้โพรไฟล์การลงบัญชีกับผู้จัดจำหน่ายเฉพาะราย กลุ่มของผู้จัดจำหน่าย หรือผู้จัดจำหน่ายทั้งหมด:
<ul>
<li><strong>ตาราง</strong> – กฎการลงรายการบัญชีที่ใช้กับผู้จัดจำหน่ายรายเดียว เลือกบัญชีผู้จัดจำหน่ายในฟิลด์ <strong>หมายเลขบัญชี/กลุ่ม</strong></li>
<li><strong>กลุ่ม</strong> – กฎการลงรายการบัญชีที่ใช้กับกลุ่มผู้จัดจำหน่าย เลือกกลุ่มผู้จัดจำหน่ายในฟิลด์ <strong>หมายเลขบัญชี/กลุ่ม</strong></li>
<li><strong>ทั้งหมด</strong> – กฎการลงรายการบัญชีที่ใช้กับผู้จัดจำหน่ายทั้งหมด ปล่อยฟิลด์ <strong>หมายเลขบัญชี/กลุ่ม</strong> ว่างไว้</li>
</ul></td>
</tr>
<tr class="even">
<td><strong>หมายเลขบัญชี/กลุ่ม</strong></td>
<td>ถ้ามีการเลือก <strong>ตาราง</strong> ในฟิลด์ <strong>รหัสบัญชี</strong> ให้เลือกหมายเลขบัญชีของผู้จัดจำหน่ายที่เชื่อมโยงกับโพรไฟล์การลงรายการบัญชี ถ้ามีการเลือก <strong>กลุ่ม</strong> ให้เลือกกลุ่มผู้จัดจำหน่าย ถ้ามีการเลือก <strong>ทั้งหมด</strong> ให้ปล่อยฟิลด์นี้ว่างไว้</td>
</tr>
<tr class="odd">
<td><strong>บัญชีสรุป</strong></td>
<td>เลือกรหัสบัญชีที่จะใช้เป็นบัญชีสรุปสำหรับผู้จัดจำหน่ายที่เกี่ยวข้องกับโพรไฟล์การลงบัญชี จะมีการทำเครื่องหมายพารามิเตอร์ <strong>ไม่อนุญาตให้มีการป้อนข้อมูลด้วยตนเอง</strong> สำหรับบัญชีหลักนี้ ถ้าคุณลบบัญชีนี้ออกจากโพรไฟล์การลงรายการบัญชีในเวลาต่อมา ให้ตรวจสอบความถูกต้องการตั้งค่า <strong>ไม่อนุญาตให้มีการตั้งค่าการป้อนข้อมูลด้วยตนเอง</strong> บนหน้า <strong>บัญชีหลัก</strong> 
<p><strong>หมายเหตุ:</strong> ถ้าตัวเลือก <strong>ใช้ข้อกำหนดการลงรายการบัญชี</strong> ถูกเลือกในหน้า <strong>พารามิเตอร์บัญชีแยกประเภททั่วไป</strong> ข้อกำหนดการลงรายการบัญชีธุรกรรมสำหรับใบแจ้งหนี้ของผู้จัดจำหน่ายจะถูกใช้แทนบัญชีสรุป</p>
</td>
</tr>
<tr class="even">
<td><strong>ตัดรายการบัญชี</strong></td>
<td>เลือกบัญชีแยกประเภทที่มีสภาพคล่องที่ใช้สำหรับการคาดการณ์กระแสเงินสด ฟิลด์นี้จะพร้อมใช้งานเฉพาะเมื่อการคาดการณ์กระแสเงินสดถูกเปิดใช้งานเท่านั้น</td>
</tr>
<tr class="odd">
<td><strong>การชำระภาษีขายล่วงหน้า</strong></td>
<td>เลือกหมายเลขบัญชีสำหรับการชำระภาษีขายที่ได้รับล่วงหน้า
<p><strong>หมายเหตุ:</strong> โพรไฟล์การลงรายการบัญชีที่ใช้งานเมื่อมีการทำเครื่องหมายการชำระเงินเป็นการชำระเงินล่วงหน้า จะถูกเลือกในโพรไฟล์ <strong>การลงรายการบัญชี</strong> ที่มีฟิลด์ <strong>ใบสำคัญสมุดรายวันการชำระเงินล่วงหน้า</strong> ในพื้นที่ <strong>บัญชีแยกประเภทและภาษีขาย</strong> ในหน้า <strong>พารามิเตอร์บัญชีเจ้าหนี้</strong></p>
</td>
</tr>
<tr class="even">
<td><strong>บัญชีขาเข้า</strong></td>
<td>เลือกรหัสบัญชีที่ลงรายการบัญชีข้อมูลเกี่ยวกับใบแจ้งหนี้ของผู้จัดจำหน่ายที่ยังไม่ได้อนุมัติ ข้อมูลจะถูกป้อนใน <strong>สมุดรายวันทะเบียนใบแจ้งหนี้</strong> ตัวอย่างเช่น ผู้ใช้ป้อนข้อมูลพื้นฐานเกี่ยวกับใบแจ้งหนี้ของผู้จัดจำหน่ายเมื่อได้รับในทะเบียนใบแจ้งหนี้ เมื่อลงรายการบัญชีทะเบียนใบแจ้งหนี้แล้ว ธุรกรรมจะถูกลงรายการบัญชีในบัญชีที่ป้อนไว้ที่นี่ และในฟิลด์ <strong>บัญชีตรงข้าม</strong> เมื่อมีการอนุมัติใบแจ้งหนี้แล้ว หนี้สินจะถูกโอนย้ายจากบัญชีการมาถึงไปยังบัญชีสรุปผู้จัดจำหน่าย</td>
</tr>
<tr class="odd">
<td><strong>บัญชีตรงข้าม</strong></td>
<td>เลือกรหัสบัญชีที่ใช้สำหรับการออฟเซ็ตใบแจ้งหนี้ของผู้จัดจำหน่ายที่ยังไม่ได้อนุมัติ ซึ่งจะอัพเดตโดยใช้ทะเบียนใบแจ้งหนี้ บัญชีตรงข้ามทำหน้าที่เป็นบัญชีตรงข้ามสำหรับธุรกรรมที่ลงรายการบัญชีในบัญชีการมาถึง ดังนั้น บัญชีประกอบด้วยการสั่งซื้อของผู้จัดจำหน่ายที่ยังไม่ได้รับการอนุมัติ</td>
</tr>
</tbody>
</table>


### <a name="table-restrictions"></a>**ข้อจำกัด**

สำหรับธุรกรรมที่มีโพรไฟล์การลงบัญชีที่เลือกไว้ ให้ระบุว่าธุรกรรมจะได้รับชำระเงินโดยอัตโนมัติ จะมีการคำนวณดอกเบี้ย และจะออกจดหมายเรียกเก็บเงิน คุณยังสามารถเลือกบัญชีที่จะใช้เมื่อธุรกรรมที่มีโพรไฟล์การลงบัญชีที่เลือกไว้ปิดลง

ระบุค่าต่อไปนี้เพื่อตั้งค่าโพรไฟล์การลงรายการบัญชีของคุณ

| ฟิลด์          | คำอธิบาย             |
|----------------|--------------------------------------------------------------------------|
| **ชำระเงิน** | เลือกตัวเลือกนี้เพื่อเปิดใช้งานการชำระเงินของธุรกรรมที่มีโพรไฟล์การลงรายการบัญชีนี้โดยอัตโนมัติ ถ้าไม่ได้เลือกตัวเลือกนี้ คุณต้องชำระธุรกรรมด้วยตนเองโดยใช้หน้า **ชำระธุรกรรมที่เปิดอยู่** |
| **ยกเลิก**     | เลือกตัวเลือกนี้ ถ้าคุณต้องการที่จะสามารถยกเลิกธุรกรรมที่มีโพรไฟล์การลงรายการบัญชีนี้ได้                              |
| **ปิดบัญชี**      | เลือกโพรไฟล์การลงรายการบัญชีที่จะเปลี่ยนเมื่อธุรกรรมที่มีโพรไฟล์การลงรายการบัญชีนี้ปิดบัญชีแล้ว ธุรกรรมถือว่าปิดบัญชีแล้วเมื่อมีการชำระเต็มจำนวน                                       |


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
