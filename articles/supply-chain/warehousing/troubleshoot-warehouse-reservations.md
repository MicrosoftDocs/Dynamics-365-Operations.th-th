---
title: แก้ไขการจองสินค้าในการจัดการคลังสินค้า
description: หัวข้อนี้อธิบายวิธีการแก้ไขปัญหาทั่วไปที่คุณอาจพบในระหว่างที่คุณทำงานการจองในคลังสินค้าใน Microsoft Dynamics 365 Supply Chain Management
author: perlynne
manager: tfehr
ms.date: 10/19/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application user
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2020-10-19
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: a1ea23059d56ebf387a95a1378e2a3cd47556d5f
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 01/15/2021
ms.locfileid: "4993895"
---
# <a name="troubleshoot-reservations-in-warehouse-management"></a>แก้ไขการจองสินค้าในการจัดการคลังสินค้า

[!include [banner](../includes/banner.md)]

หัวข้อนี้อธิบายวิธีการแก้ไขปัญหาทั่วไปที่คุณอาจพบในระหว่างที่คุณทำงานการจองในคลังสินค้าใน Microsoft Dynamics 365 Supply Chain Management

## <a name="i-receive-the-following-error-message-reservations-cannot-be-removed-because-there-is-work-created-which-relies-on-the-reservations"></a>ฉันได้รับข้อความแสดงข้อผิดพลาดต่อไปนี้: "ไม่สามารถลบการจองได้เนื่องจากมีงานที่สร้างขึ้นซึ่งอาศัยการจอง"

### <a name="issue-description"></a>คำอธิบายปัญหา

คุณไม่สามารถยกเลิกการจองสินค้าคงคลังในรายการขายได้ เนื่องจากมีงานที่เปิดอยู่กับรายการ

### <a name="issue-resolution"></a>การแก้ไขปัญหา

ตรวจสอบว่างานกลุ่มการบรรจุเปิดอยู่เพื่อนำสินค้าจากสถานีบรรจุไปยังที่ตั้งอื่น (เช่น *Baydoor*) ตรวจทานเรกคอร์ดในหน้า **ล็อกประวัติการสร้างงาน** และ **รายละเอียดงาน** เพื่อตรวจสอบว่ามีการจองสินค้าคงคลังทางกายภาพอย่างไร แล้วทำให้เสร็จสมบูรณ์หรือลบงานเพื่อเพิ่มความสะดวกในการจอง

## <a name="i-receive-the-following-error-message-inventory-quantity--1-could-not-be-updated-due-to-insufficient-inventory-transactions-for-item-2"></a>ฉันได้รับข้อความแสดงข้อผิดพลาดต่อไปนี้: "ปริมาณสินค้าคงคลัง -%1 ไม่สามารถอัพเดตได้เนื่องจากมีรายการความเคลื่อนไหวของสินค้าคงคลังไม่เพียงพอสำหรับสินค้า %2...."

### <a name="issue-description"></a>คำอธิบายปัญหา

ปัญหานี้อาจเกิดขึ้นได้ถ้าระบบไม่สามารถอัพเดตปริมาณสินค้าคงคลังได้ เนื่องจากมีรายการความเคลื่อนไหวของสินค้าคงคลังที่มีมิติที่ระบุอยู่ไม่เพียงพอ นี่เป็นข้อความแบบเต็มของข้อความแสดงข้อผิดพลาดทั้งหมด

> ปริมาณสินค้าคงคลัง -%1 ไม่สามารถอัพเดตได้เนื่องจากมีรายการความเคลื่อนไหวของสินค้าคงคลังที่ไม่เพียงพอสำหรับสินค้า %2 ที่มีขนาดมิติ=%3 สี=%4 เพิ่ม=%5 ไซต์=%6 คลังสินค้า=%7 ที่ตั้ง=%8 สถานะของสินค้าคงคลัง=พร้อมใช้งาน ป้ายทะเบียน=%9 หมายเลขชุดงาน=%10 สำหรับรหัสการอ้างอิง %11 บนรหัสล็อต %12

### <a name="issue-resolution"></a>การแก้ไขปัญหา

ตรวจสอบให้แน่ใจว่าไม่มีรายการความเคลื่อนไหวของสินค้าคงคลังที่มีการจองปริมาณทางกายภาพ ตัวอย่างเช่น ธุรกรรมเหล่านี้อาจเปิดใบสั่งตรวจสอบคุณภาพ เรกคอร์ดการบล็อคสินค้าคงคลัง หรือใบสั่งเอาพุต

## <a name="i-receive-the-following-error-message-physical-on-handcannot-be-reserved-because-only-000-are-available-in-the-inventory"></a>ฉันได้รับข้อความแสดงข้อผิดพลาดต่อไปนี้: "ปริมาณคงคลังคงเหลือที่มีอยู่จริง... ไม่สามารถจองได้เนื่องจากมีเพียง 0.00 เท่านั้นที่พร้อมใช้งานในสินค้าคงคลัง

### <a name="issue-description"></a>คำอธิบายปัญหา

ปัญหานี้อาจเกิดขึ้นได้ถ้าระบบไม่สามารถอัพเดตปริมาณสินค้าคงคลังได้ เนื่องจากมีรายการความเคลื่อนไหวของสินค้าคงคลังที่มีมิติที่ระบุอยู่ไม่เพียงพอ นี่เป็นข้อความแบบเต็มของข้อความแสดงข้อผิดพลาดทั้งหมด

> ไซต์คงคลังคงเหลือที่มีอยู่จริง=%1คลังสินค้า=%2 สถานะของสินค้าคงคลัง = พร้อมใช้งานหมายเลขชุดงาน=%3 เจ้าของ=%4: %5 ไม่สามารถจองได้เนื่องจากมีเฉพาะ๐.๐๐เท่านั้นที่พร้อมใช้งานในสินค้าคงคลัง

### <a name="issue-resolution"></a>การแก้ไขปัญหา

ปัญหานี้อาจเกิดจากการเปิดงาน ทำงานให้เสร็จสมบูรณ์หรือได้รับโดยไม่มีการสร้างงาน ตรวจสอบให้แน่ใจว่าไม่มีรายการความเคลื่อนไหวของสินค้าคงคลังที่มีการจองปริมาณทางกายภาพ ตัวอย่างเช่น ธุรกรรมเหล่านี้อาจเปิดใบสั่งตรวจสอบคุณภาพ เรกคอร์ดการบล็อคสินค้าคงคลัง หรือใบสั่งเอาพุต

## <a name="i-receive-the-following-error-message-to-be-assigned-to-wave-load-lines-must-specify-the-dimensions-above-the-location-to-assign-these-dimensions-reserve-and-recreate-the-load-line"></a>ฉันได้รับข้อความแสดงข้อผิดพลาดต่อไปนี้: "หากต้องการให้กำหนดให้กับเวฟ บรรทัดการโหลดต้องระบุมิติเหนือสถานที่ ถ้าต้องการกำหนดมิติเหล่านี้ ให้จองและสร้างรายการจำนวนงานในศูนย์การผลิตใหม่"

### <a name="issue-description"></a>คำอธิบายปัญหา

เมื่อคุณใช้สินค้าที่มีลำดับชั้นการจอง "ชุดงานข้างบน" (โดยมีมิติ **หมายเลขชุดงาน** ที่อยู่ *ด้านบน* มิติ **สถานที่เก็บ**) คำสั่ง **นำออกใช้ไปยังคลังสินค้า** บนหน้า **เวิร์กเบนช์การวางแผนการบรรทุก** สำหรับปริมาณบางส่วนไม่ทำงาน คุณได้รับข้อความแสดงข้อความแสดงข้อผิดพลาดนี้และไม่มีการสร้างงานสำหรับปริมาณบางส่วน

อย่างไรก็ตาม ถ้าคุณใช้สินค้าที่มีลำดับชั้นการจอง "ชุดงานด้านล่าง" (โดยมีมิติ **หมายเลขชุดงาน** ที่อยู่ *ด้านล่าง* มิติ **สถานที่เก็บ**) คุณจึงสามารถนำโหลดออกใช้ได้จากหน้า **เวิร์กเบนช์การวางแผน** สำหรับปริมาณบางส่วนไม่ทำงาน

### <a name="issue-resolution"></a>การแก้ไขปัญหา

ลักษณะการทำงานนี้เกิดจากการออกแบบ ถ้าคุณกำหนดมิติที่อยู่ด้านบนของมิติ **สถานที่** ในลำดับชั้นการจอง ต้องระบุก่อนการนำออกใช้ไปยังคลังสินค้า Microsoft ได้ประเมินปัญหานี้แล้ว และระบุว่าเป็นข้อจำกัดของลักษณะการทำงานในระหว่างการนำออกใช้ไปยังคลังสินค้าจากเวิร์กเบนช์การวางแผนการบรรทุก ไม่สามารถปล่อยปริมาณบางส่วนได้ ถ้าไม่ได้ระบุอย่างน้อยหนึ่งมิติข้างบน **สถานที่เก็บ**

สำหรับข้อมูลเพิ่มเติม ให้ดูที่ [นโยบายการจองในมิติระดับคลังสินค้าที่ยืดหยุ่น](flexible-warehouse-level-dimension-reservation.md)
