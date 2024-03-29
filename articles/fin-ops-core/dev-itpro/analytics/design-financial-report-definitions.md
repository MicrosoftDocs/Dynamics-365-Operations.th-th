---
title: ข้อกำหนดของรายงานในผู้ออกแบบรายงานทางการเงิน
description: บทความนี้แสดงข้อมูลเกี่ยวกับข้อกำหนดของรายงาน
author: aprilolson
ms.date: 11/22/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: twheeloc
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.custom: 59131
ms.assetid: 966a3f1d-c59c-4a84-acd4-5bb7e65144c8
ms.search.form: FinancialReports
ms.openlocfilehash: 2ffef335c694af56486ccd7738818c4edda49b9e
ms.sourcegitcommit: d27fef61593c6d1e9e26d5c9fad21411bc52fabc
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 11/23/2022
ms.locfileid: "9802564"
---
# <a name="report-definitions-in-financial-report-designer"></a>ข้อกำหนดของรายงานในผู้ออกแบบรายงานทางการเงิน

[!include [banner](../includes/banner.md)]

บทความนี้แสดงข้อมูลเกี่ยวกับข้อกำหนดของรายงาน ข้อกำหนดของรายงานคือส่วนประกอบของรายงาน (หรือบล็อคส่วนประกอบ) ที่ใช้คำนิยามแถว คำนิยามคอลัมน์ และคำนิยามแผนภูมิรายงานเพิ่มเติมเพื่อสร้างรายงาน ข้อกำหนดของรายงานยังมีตัวเลือกและการตั้งค่าสำหรับการปรับแต่งรายงานด้วยตนเองอีกด้วย 

ข้อกำหนดของรายงานคือส่วนประกอบของรายงาน (หรือบล็อคส่วนประกอบ) ที่ใช้คำนิยามแถว คำนิยามคอลัมน์ และคำนิยามแผนภูมิรายงานเพิ่มเติมเพื่อสร้างรายงาน คำนิยามรายงานยังแสดงตัวเลือก และการตั้งค่าที่คุณสามารถกำหนดรายงานเอง หลังจากที่คุณกำหนดคำนิยามแถวและคำนิยามคอลัมน์ คุณต้องรวมค่าดังกล่าวในข้อกำหนดของรายงาน ณ จุดนี้ คุณยังสามารถกำหนดแง่มุมอื่นๆ ของคำนิยาม เช่นระดับรายละเอียดและวันที่รายงาน จากนั้นคุณสามารถบันทึกและสร้างรายงาน การรายงานทางการเงินมีรายละเอียดในระดับต่าง ๆ ดังต่อไปนี้:

- การเงิน
- การเงินและการบัญชี
- การเงิน การบัญชีและธุรกรรม

อย่างไรก็ตาม โดยขึ้นอยู่กับวิธีการจัดเก็บข้อมูลในระบบ Microsoft Dynamics ERP รายละเอียดธุรกรรมอาจไม่พร้อมใช้งานในรายงาน

## <a name="create-a-report-definition"></a>สร้างข้อกำหนดของรายงาน
1. ใน Report Designer บนเมนู **ไฟล์** คลิก **สร้าง** แล้วเลือก **ข้อกำหนดของรายงาน**
2. ระบุข้อมูลที่เหมาะสมบนแท็บ **รายงาน** **เอาท์พุทและการกระจาย** **ส่วนหัวและส่วนท้าย** และ **การตั้งค่า**

## <a name="contents-of-a-report-definition"></a>เนื้อหาของข้อกำหนดของรายงาน
ตารางต่อไปนี้อธิบายถึงแท็บในข้อกำหนดของรายงานและวิธีใช้ข้อมูล

<table>
<thead>
<tr>
<th>แท็บ</th>
<th>คำอธิบาย</th>
</tr>
</thead>
<tbody>
<tr>
<td>รายงาน</td>
<td>สร้างรายงาน ตั้งค่าคอนฟิกรายงาน หรือปรับแก้รายงานที่มีอยู่</td>
</tr>
<tr>
<td>เอาท์พุทและการกระจาย</td>
<td>เปลี่ยนชนิดของผลที่ได้และปลายทางของรายงาน</td>
</tr>
<tr>
<td>ส่วนหัวและส่วนท้าย</td>
<td>กำหนดและจัดรูปแบบหัวกระดาษและท้ายกระดาษสำหรับรายงาน ตัวอย่างเช่น คุณสามารถเพิ่มรูปภาพหรือข้อความในหัวกระดาษหรือท้ายกระดาษ การรายงานทางการเงินสนับสนุนไฟล์ .bmp, .jpg และ.png สำหรับรูปภาพ คุณยังสามารถเพิ่มรหัสข้อความอัตโนมัติเพื่อแทรกข้อมูลอื่น เช่น ชื่อบริษัท ชื่อรายงาน หรือหมายเลขหน้า</td>
</tr>
<tr>
<td>การตั้งค่า</td>
<td>ระบุการตั้งค่าข้อกำหนดของรายงาน เช่น การตั้งค่าต่อไปนี้:
<ul>
<li>การจัดรูปแบบและการปัดเศษยอดเงิน</li>
<li>จัดรูปแบบรายละเอียดของรายงาน</li>
<li>จัดรูปแบบแผนภูมิการรายงาน</li>
<li>สร้างรายงานข้อยกเว้น</li>
<li>ระบุการแปลงสกุลเงิน</li>
<li>ผลรวมย่อยและรายละเอียดตัวกรองบัญชี</li>
</ul>
</td>
</tr>
</tbody>
</table>

## <a name="additional-resources"></a>ทรัพยากรเพิ่มเติม

[การรายงานทางการเงิน](financial-reporting-intro.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
