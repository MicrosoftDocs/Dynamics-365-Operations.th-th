---
title: ตำแหน่งเงินสด (พรีวิว)
description: หัวข้อนี้จะอธิบายถึงวิธีที่คุณลักษณะของการคาดการณ์กระแสเงินสดจะคาดการณ์ตำแหน่งเงินสดขององค์กรสำหรับเวลาที่ระบุ นอกจากนี้ ยังอธิบายถึงตัวเลือกที่พร้อมใช้งานสำหรับการแสดงการคาดการณ์สำหรับรอบระยะเวลาที่แตกต่างกัน
author: ShivamPandey-msft
manager: AnnBe
ms.date: 05/26/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 14151
ms.assetid: 3d43ba40-780c-459a-a66f-9a01d556e674
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2019-11-06
ms.dyn365.ops.version: AX 10.0.8
ms.openlocfilehash: 5cf1ac4de07cb6357493a0b2c84f6a6ee591d4bc
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 01/15/2021
ms.locfileid: "4990575"
---
# <a name="cash-position-preview"></a>ตำแหน่งเงินสด (พรีวิว)

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

ตำแหน่งเงินสดคือการคาดการณ์ของกระแสเงินสดที่เป็นการคาดการณ์สำหรับเงื่อนไขที่อยู่ใกล้ โดยขึ้นอยู่กับการคาดการณ์ของใบเสร็จรับเงินจากลูกค้าที่ชำระใบแจ้งหนี้และใบสั่งที่ค้างชำระ และยังขึ้นกับการเบิกจ่ายเงินสดของการคาดการณ์ที่มีการชำระเงินให้แก่ผู้จัดจำหน่ายสำหรับใบแจ้งหนี้และใบสั่งซื้อ

เมื่อระบบคาดการณ์การชำระเงินของลูกค้า จะใช้การคาดการณ์การชำระเงินจากคุณลักษณะการคาดการณ์การชำระเงินของลูกค้า โดยไม่มีการคาดการณ์การชำระเงิน เวลาโดยเฉลี่ยที่จำเป็นต้องใช้ในการแปลงใบแจ้งหนี้ของลูกค้าเป็นการชำระเงินสำหรับลูกค้าแต่ละราย จะใช้ในการคำนวณวันที่ชำระเงิน สำหรับใบสั่งของลูกค้าที่เปิดค้างไว้ ระบบจะคำนวณวันที่ในใบแจ้งหนี้โดยใช้จำนวนวันเฉลี่ยสำหรับบรรทัดใบสั่งสำหรับลูกค้าแต่ละรายที่จะออกใบแจ้งหนี้ จากนั้น จะใช้วันที่ในใบแจ้งหนี้เป็นข้อมูลป้อนเข้าสำหรับฟังก์ชันการคาดการณ์การชำระเงิน ฟังก์ชันการคาดการณ์การชำระเงินของลูกค้า จะคำนวณวันที่ชำระเงินสำหรับบรรทัดใบสั่งแต่ละบรรทัด 

<*ต้องการข้อความจาก Jarek หรือ Dave เกี่ยวกับวิธีการแปลงการคาดคะเนการชำระเงินเป็นวันที่*> มีการประมาณวันที่ชำระเงินสำหรับใบแจ้งหนี้ที่ค้างชำระ [*ประมาณ*] จากการคาดการณ์การชำระเงินโดยการเลือกวันที่ที่สอดคล้องกับห้าสิบเปอร์เซ็นต์ของฟังก์ชันการกระจายสะสมที่ได้รับมาจากความน่าจะเป็นของกลุ่มที่คาดการณ์ไว้

วิธีการที่คล้ายกันถูกใช้เพื่อคาดการณ์การชำระเงินให้แก่ผู้จัดจำหน่าย สำหรับผู้จัดจำหน่ายแต่ละราย ระบบจะคำนวณเวลาโดยเฉลี่ยที่จำเป็นต้องใช้ในการแปลงใบแจ้งหนี้ของผู้จัดจำหน่ายเป็นการชำระเงิน จากนั้น จำนวนวันถูกใช้ในการคำนวณวันที่ชำระเงิน สำหรับใบสั่งของผู้จัดจำหน่ายที่เปิดค้างไว้ ระบบจะคำนวณวันที่ในใบแจ้งหนี้โดยพิจารณาจำนวนวันเฉลี่ยที่จำเป็นต้องใช้ในการแปลงบรรทัดใบสั่งเป็นใบแจ้งหนี้สำหรับผู้จัดจำหน่ายแต่ละราย จากนั้น ระบบจะคำนวณวันที่ชำระเงินโดยใช้เวลาเฉลี่ยในการแปลงใบแจ้งหนี้ของผู้จัดจำหน่ายเป็นการชำระเงินสำหรับผู้จัดจำหน่ายแต่ละราย

ส่วนบนของแท็บ **ตำแหน่งเงินสด** มีแผนภูมิตำแหน่งเงินสด แผนภูมินี้แสดงรายรับเงินสดและรายจ่ายเงินสด และผลกระทบต่อยอดดุลสภาพคล่องรวม รายละเอียดในแผนภูมิตำแหน่งเงินสดสามารถดูได้ในรอบระยะเวลารายวัน รายสัปดาห์ รายเดือน หรือรายไตรมาส เมื่อคุณเลือก **รายวัน** คุณสามารถดูการคาดการณ์สำหรับ 21 วันถัดไป เมื่อคุณเลือก **รายสัปดาห์** คุณสามารถดูการคาดการณ์สำหรับ 20 สัปดาห์ถัดไป เมื่อคุณเลือก **รายเดือน** คุณสามารถดูการคาดการณ์สำหรับ 12 เดือนถัดไป เมื่อคุณเลือก **รายไตรมาส** คุณสามารถดูการคาดการณ์สำหรับ 12 ไตรมาสถัดไป คุณสามารถซ่อนแผนภูมิได้ ถ้าคุณต้องการพื้นที่เพิ่มเติมบนหน้าจอของคุณเพื่อดูเนื้อหาบนแท็บ **ตำแหน่งเงินสด**

ส่วนล่างของแท็บ **ตำแหน่งเงินสด** จะแสดงรายละเอียดสำหรับตำแหน่ง กระแสเงินสด การชำระเงินที่คาดการณ์ และบัญชีธนาคาร

- ข้อมูลในกริด **รายละเอียดตำแหน่ง** แสดงอยู่ในสามส่วน: รายการของบัญชีสภาพคล่อง รายการของเอกสารที่ประกอบเป็นรายรับเงินสด และรายการของเอกสารที่ประกอบเป็นรายจ่ายเงินสด นอกจากนี้ กริดยังแสดงยอดดุลของตำแหน่งเงินสดอีกด้วย สำหรับรอบระยะเวลาแรกที่คุณกำลังดู ยอดดุลสำหรับบัญชีสภาพคล่องเป็นยอดดุลยกมา สำหรับรอบระยะเวลาต่อมา ยอดดุลสำหรับบัญชีสภาพคล่องจะถูกคำนวณตามการเพิ่มของรายรับเงินสดและการลบของรายจ่ายเงินสดจากรอบระยะเวลาก่อนหน้านี้ ถ้าต้องการดูรายละเอียดของธุรกรรมที่ประกอบเป็นยอดดุล ให้เลือกลิงค์ **ยอดดุล**
- กริด **กระแสเงินสด** จะแสดงรายรับเงินสด รายจ่ายเงินสดที่รวมสำหรับแต่ละรอบระยะเวลา และผลกระทบต่อยอดดุลบัญชีสภาพคล่อง สำหรับรอบระยะเวลาแรก ยอดดุลสำหรับบัญชีสภาพคล่องเป็นยอดดุลยกมา สำหรับรอบระยะเวลาต่อมา ยอดดุลสำหรับบัญชีสภาพคล่องจะถูกคำนวณตามการเพิ่มของรายรับเงินสดและการลบของรายจ่ายเงินสดจากรอบระยะเวลาก่อนหน้านี้
- กริด **ยอดดุลธนาคารที่คาดการณ์** แสดงรายจ่ายเงินสดที่คาดไว้และผลกระทบต่อบัญชีสภาพคล่อง
- กริด **บัญชีธนาคาร** แสดงผลกระทบของรายรับเงินสดที่และรายจ่ายเงินสดที่คาดไว้ในยอดดุลธนาคาร

เมื่อต้องการบันทึกและแก้ไขตำแหน่งเงินสด ให้สร้างสแนปช็อต สำหรับข้อมูลเพิ่มเติมเกี่ยวกับวิธีการทำงานกับสแนปช็อต โปรดดูที่ [ภาพรวมสแนปช็อต](payment-snapshots.md)

#### <a name="privacy-notice"></a>ประกาศความเป็นส่วนตัว
การแสดงตัวอย่าง (1) อาจใช้วิธีการที่มีความปลอดภัยและความเป็นส่วนตัวที่น้อยลงกว่าบริการ Dynamics 365 Finance and Operations (2) ไม่ถูกรวมอยู่ในข้อตกลงระดับการให้บริการ (SLA) สำหรับบริการนี้ (3) ไม่ควรถูกใช้เพื่อประมวลผลข้อมูลส่วนบุคคลหรือข้อมูลอื่นที่อยู่ภายใต้ข้อกำหนดการปฏิบัติตามกฎหมายหรือระเบียบข้อบังคับ และ (4) มีการสนับสนุนที่จำกัด
