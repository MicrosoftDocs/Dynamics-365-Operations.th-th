---
title: ตั้งค่าและสร้างไฟล์ Positive Pay โดยใช้การรายงานทางอิเล็กทรอนิกส์
description: บทความนี้อธิบายวิธีการตั้งค่า positive pay โดยใช้การรายงานทางอิเล็กทรอนิกส์
author: panolte
ms.date: 03/20/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: BankPositivePayFormat
audience: Application User
ms.reviewer: twheeloc
ms.custom: 88433
ms.assetid: 73f3dcf6-040a-44ad-9512-7b3e0d17a571
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2016-05-31
ms.dyn365.ops.version: AX 7.0.1
ms.openlocfilehash: 491048c7274ba6bb52e0a4b7a6ea5cd0f5ff4741
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 06/03/2022
ms.locfileid: "8878231"
---
# <a name="set-up-positive-pay-files-by-using-electronic-reporting"></a>ตั้งค่าไฟล์ Positive Pay โดยใช้การรายงานทางอิเล็กทรอนิกส์

บทความนี้อธิบายวิธีการตั้งค่า Positive Pay และสร้างไฟล์ Positive Pay โดยใช้การรายงานทางอิเล็กทรอนิกส์

> [!NOTE] 
> ก่อนใช้ฟังก์ชัน **สร้างไฟล์ Positive Pay ของธนาคาร** คุณจะต้องรีเฟรชรายการเอนทิตีก่อน
> ไปที่ **Data การจัดการข้อมูล > นําเข้า/ส่งออก > พารามิเตอร์ของกรอบงาน** 
> แท็บด่วน **การตั้งค่าเอนทิตี** เลือก **รีเฟรชรายการเอนทิตี**


ตั้งค่า Positive Pay เพื่อสร้างรายการอิเล็กทรอนิกส์ของเช็คที่ได้รับไปยังธนาคาร  เมื่อเช็คถูกนำเสนอให้แก่ธนาคารแล้ว ธนาคารจะเปรียบเทียบเช็คกับรายการของเช็ค ถ้าเช็คตรงกับเช็คในรายการ ธนาคารจะเคลียร์เช็ค  ถ้าเช็คไม่ตรงกัน ธนาคารจะระงับเช็คไว้เพื่อตรวจสอบ

## <a name="security-for-positive-pay-files"></a>ความปลอดภัยสำหรับไฟล์ positive pay
ไฟล์ positive pay สามารถประกอบด้วยข้อมูลที่สำคัญเกี่ยวกับผู้จ่าย และยอดเงินเช็ค  ดังนั้นตรวจสอบให้แน่ใจว่า คุณใช้มาตรการด้านความปลอดภัยที่เหมาะสมจากเวลาที่มีการสร้างไฟล์ จนกระทั่งได้รับโดยธนาคาร  ไฟล์ positive pay ถูกดาวน์โหลดไปยังตำแหน่งที่ระบุโดยเว็บเบราเซอร์ของคุณ  เนื่องจากไฟล์ค่าจ้างเชิงบวกสามารถประกอบด้วยข้อมูลสำคัญ เป็นสิ่งสำคัญที่เฉพาะผู้ใช้ที่ได้รับการรับรองจะมีการเข้าถึงเพื่อสร้างและดูข้อมูลนี้ใน Microsoft Dynamics 365 Finance ใช้ตารางต่อไปนี้เพื่อช่วยให้คุณกำหนดสิทธิ์ที่จำเป็นได้

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th>งาน</th>
<th>สิทธิ์</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>สร้างไฟล์ positive pay จากหน้ารายการ <strong>บัญชีธนาคาร</strong> หรือหน้า <strong>บัญชีธนาคาร</strong></td>
<td><ul>
<li><strong>รักษาข้อมูล positive pay ของธนาคาร</strong> (BankPositivePayProcess)</li>
<li><strong>BankPositivePayExportEntityView</strong> (BankPositivePayExportEntityView)</li>
</ul></td>
</tr>
<tr class="even">
<td>สร้างไฟล์ Positive Pay สำหรับนิติบุคคลหลายรายและบัญชีธนาคารจากหน้า <strong>สร้างไฟล์ positive pay</strong></td>
<td><ul>
<li><strong>รักษาข้อมูล positive pay ของธนาคาร</strong> (BankPositivePayProcess)</li>
<li><strong>BankPositivePayExportEntityView</strong> (BankPositivePayExportEntityView)</li>
</ul></td>
</tr>
<tr class="odd">
<td>ดูไฟล์ positive pay ในหน้า <strong>สรุปไฟล์ positive pay</strong></td>
<td><strong>ดูข้อมูล Positive Pay ของธนาคารสำหรับนิติบุคคลหลายราย</strong> (BankPositivePayView)</td>
</tr>
<tr class="even">
<td>ยืนยันไฟล์ positive pay ของธนาคารในหน้า <strong>สรุปไฟล์ positive pay</strong></td>
<td><strong>ยืนยันไฟล์ positive pay</strong> (BankPositivePayConfirm)</td>
</tr>
<tr class="odd">
<td>เรียกคืนไฟล์ positive pay ของธนาคารในหน้า <strong>สรุปไฟล์ positive pay</strong></td>
<td><strong>เรียกคืนไฟล์ Positive Pay</strong> (BankPositivePayRecall)</td>
</tr>
</tbody>
</table>

## <a name="set-up-the-electronic-reporting-configuration"></a>สร้างการตั้งค่าคอนฟิกการรายงานทางอิเล็กทรอนิกส์

1. ไปที่ **พื้นที่ทำงาน \> การรายงานทางอิเล็กทรอนิกส์**
2. บนไทล์สำหรับผู้ให้บริการตั้งค่าคอนฟิก **Microsoft** ให้เลือก **ที่เก็บ**
3. เลือก **ส่วนกลาง** แล้วเลือก **เปิด**
4. ถ้าต้องสร้างการเชื่อมต่อกับที่เก็บ ให้เลือกลิงก์สีเงินในกล่องโต้ตอบ
5. ในรายการ การตั้งค่าคอนฟิก ให้ค้นหาและเลือก **รูปแบบ Positive pay \> รูปแบบ Positive pay**
6. บนแท็บด่วน **รุ่น** ให้เลือกรุ่นล่าสุด แล้วเลือก **นำเข้า**

## <a name="set-up-a-positive-pay-format"></a>ตั้งค่ารูปแบบของ Positive Pay

1. ไปที่ **การจัดการเงินสดและธนาคาร \> การตั้งค่า \> รูปแบบ Positive pay**
2. เลือก **ใหม่**
3. ตั้งค่าฟิลด์ **รูปแบบการชำระเงิน** และ **คำอธิบาย**
4. เลือกกล่องกาเครื่องหมาย **รูปแบบการส่งออกทางอิเล็กทรอนิกส์ทั่วไป**
5. ตั้งค่าฟิลด์ **ส่งออกการตั้งค่าคอนฟิกรูปแบบ** เป็นรูปแบบ **รูปแบบ Positive pay**

## <a name="assign-a-positive-pay-format-to-a-bank-account"></a>กำหนดรูปแบบ Positve Pay ให้กับบัญชีธนาคาร
สำหรับแต่ละบัญชีธนาคารที่คุณต้องการสร้างข้อมูล positive pay ให้ คุณต้องกำหนดรูปแบบ positive pay ที่คุณระบุไว้ในส่วนก่อนหน้านี้  ในหน้า บัญชีธนาคาร เลือกรูปแบบ positive pay ที่สอดคล้องกับบัญชีธนาคาร ในฟิลด์ **วันที่เริ่มต้น Positive pay** ป้อนวันที่แรกในการสร้างไฟล์ Positive pay 

>[!Important]
> ป้อนวันที่ในฟิลด์ **วันที่เริ่มต้นของ Positive pay** ถ้าปล่อยว่างไว้ ไฟล์ positive pay แรกที่สร้างขึ้นจะรวมเช็คทั้งหมดที่เคยสร้างไว้สำหรับบัญชีธนาคารนี้

1. ไปที่ **การจัดการเงินสดและธนาคาร \> บัญชีธนาคาร \> บัญชีธนาคาร**
2. เปิดบัญชีธนาคาร
3. บนแท็บด่วน **ทั่วไป** ให้ตั้งค่าฟิลด์ **รูปแบบ Positive pay** เป็นรูปแบบที่สร้างไว้ก่อนหน้านี้
4. ตั้งค่าฟิลด์ **วันที่เริ่มต้นของ Positive pay** เป็นวันที่ปัจจุบัน

## <a name="assign-a-number-sequence-for-positive-pay-files"></a>มอบหมายลำดับหมายเลขสำหรับไฟล์ Positve Pay
แต่ละไฟล์ positive pay ต้องมีหมายเลขเฉพาะ  บนหน้า **พารามิเตอร์การจัดการเงินสดและธนาคาร** สร้างลำดับหมายเลขสำหรับไฟล์ Positive pay บนแท็บ **ลำดับหมายเลข**

## <a name="generate-a-positive-pay-file-for-a-single-bank-account"></a>สร้างไฟล์ positive pay สำหรับบัญชีธนาคารเดี่ยว
คุณสามารถสร้างไฟล์ positive pay สำหรับนิติบุคคลเดียวและบัญชีธนาคารหนึ่งๆ  สำหรับข้อมูลเกี่ยวกับวิธีการสร้างไฟล์ positive pay สำหรับนิติบุคคลและบัญชีธนาคารหลายรายการพร้อมกัน ให้ดูส่วนถัดไป  เพื่อสร้างไฟล์ Positive pay สำหรับนิติบุคคลเดียวและบัญชีธนาคารเดียว ให้เปิดกล่องโต้ตอบ **สร้างไฟล์ Positive pay** จากหน้า **บัญชีธนาคาร** ในฟิลด์ **วันที่ตัดยอด** ป้อนวันที่ของเช็คล่าสุดเพื่อรวมไว้ในไฟล์ Positive pay เช็คทั้งหมดที่ยังไม่ได้ถูกรวมอยู่ในไฟล์ positive pay ภายในวันที่สิ้นสุดของเช็คนี้จะถุกรวมอยู่ในไฟล์

1. ไปที่ **การจัดการเงินสดและธนาคาร \> บัญชีธนาคาร \> บัญชีธนาคาร**
2. เปิดบัญชีธนาคารที่มีการตั้งค่า Positive Pay
3. เลือก **จัดการการชำระเงิน \> Positive pay \> ไฟล์ Positive pay**
4. ตั้งค่าฟิลด์ **วันที่ตัดยอด** ตรวจสอบว่ามีการสร้างขึ้นก่อนวันที่นี้จะถูกรวมไว้

## <a name="generate-a-positive-pay-file-for-multiple-bank-accounts"></a>สร้างไฟล์ positive pay สำหรับบัญชีธนาคารหลายรายการ
เพื่อสร้างไฟล์ Positive pay สำหรับบัญชีธนาคารหลายรายการ ใช้งานประจำงวด **ไฟล์ Positive pay** เลือกรูปแบบ positive pay สำหรับไฟล์ และระบุว่าจะสร้างไฟล์สำหรับนิติบุคคลทั้งหมด หรือสำหรับนิติบุคคลที่เลือก  คุณสามารถสร้างไฟล์ positive pay สำหรับบัญชีธนาคารทั้งหมดที่ใช้รูปแบบ positive pay หรือสำหรับบัญชีธนาคารที่เลือก  ในฟิลด์ **วันที่ตัดยอด** ป้อนวันที่ของเช็คล่าสุดเพื่อรวมไว้ในไฟล์ Positive pay เช็คทั้งหมดที่ยังไม่ได้ถูกรวมอยู่ในไฟล์ positive pay ภายในวันที่สิ้นสุดของเช็คนี้จะถุกรวมอยู่ในไฟล์

## <a name="view-the-results-of-positive-pay-file-generation"></a>ดูผลลัพธ์ของการสร้างไฟล์ positive pay
หลังจากที่มีสร้างไฟล์ Positive pay คุณสามารถดูผลลัพธ์ในหน้า  **สรุปไฟล์ Positive pay** ได้  เมื่อต้องการดูรายละเอียดของเช็คแต่ละรายการ ไปที่หน้า **รายละเอียดไฟล์ Positive pay**

## <a name="confirm-a-positive-pay-file"></a>ยืนยันไฟล์ Positive Pay
หลังจากที่เช็คที่ถูกรายการในไฟล์ positive pay ได้ถูกชำระ คุณจะได้รับหมายเลขการยืนยันจากธนาคารของคุณ  จากนั้น คุณสามารถยืนยันไฟล์ positive pay ได้  บนหน้า **สรุปไฟล์ Positive pay** ให้เลือกไฟล์ Positive pay ที่มีสถานะเป็น **สร้างแล้ว** และจากนั้นเลือกการดำเนินการ **ป้อนการยืนยัน** เมื่อคุณยืนยันไฟล์ positive pay จะมีการบันทึกหมายเลขใบยืนยันที่คุณได้รับจากธนาคาร

## <a name="recall-a-positive-pay-file"></a>เรียกคืนไฟล์ Positive Pay
ถ้าคุณต้องเปลี่ยนไฟล์ positive pay คุณสามารถเรียกคืนได้  ในหน้า **สรุปไฟล์ Positive pay** เลือกไฟล์ Positive pay ที่มีสถานะเป็น **สร้างแล้ว** และจากนั้นเลือกการดำเนินการ **เรียกคืน** สำหรับเช็คแต่ละรายการในไฟล์ positive pay ฟิลด์จะบ่งชี้ว่า เช็คที่ได้ถูกรวมในไฟล์ positive pay จะถูกรีเซ็ตหรือไม่  จากนั้นคุณสามารถสร้างไฟล์ positive pay ใหม่ที่รวมเช็คที่ถูกเรียกคืน


ไฟล์ XML ที่ได้จะถูกดาวน์โหลด
