---
title: แก้ไขปัญหาการดำเนินงานคลังสินค้าขาเข้า
description: หัวข้อนี้อธิบายวิธีการแก้ไขปัญหาทั่วไปที่คุณอาจพบในระหว่างที่คุณทำงานการดำเนินงานคลังสินค้าขาเข้าใน Microsoft Dynamics 365 Supply Chain Management
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
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2020-10-19
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: 60b6e37ec9d716f635c2d25374ac25a82286660e
ms.sourcegitcommit: deb711c92251ed48cdf20ea514d03461c26a2262
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 11/25/2020
ms.locfileid: "4645983"
---
# <a name="troubleshoot-inbound-warehouse-operations"></a>แก้ไขปัญหาการดำเนินงานคลังสินค้าขาเข้า

[!include [banner](../includes/banner.md)]

หัวข้อนี้อธิบายวิธีการแก้ไขปัญหาทั่วไปที่คุณอาจพบในระหว่างที่คุณทำงานการดำเนินงานคลังสินค้าขาเข้าใน Microsoft Dynamics 365 Supply Chain Management

## <a name="i-receive-the-following-error-message-quality-order-1-has-been-generated-cluster-profile-could-not-be-found-please-check-your-configuration"></a>ฉันได้รับข้อความแสดงข้อผิดพลาดต่อไปนี้: "สร้างใบสั่งตรวจสอบคุณภาพแล้ว %1 ไม่พบโพรไฟล์ของคลัสเตอร์ โปรดตรวจสอบการตั้งค่าคอนฟิกของคุณ"

### <a name="issue-description"></a>คำอธิบายปัญหา

ข้อความแสดงข้อผิดพลาดนี้เกี่ยวข้องกับกระบวนการรับที่มีการเปิดใช้งานการจัดการคุณภาพ (QMS) ขึ้นอยู่กับการตั้งค่าคอนฟิกในสภาพแวดล้อมของคุณ รายละเอียดเพิ่มเติมเกี่ยวกับธุรกรรมที่สร้างข้อความแสดงข้อผิดพลาดอาจช่วยแก้ไขปัญหานี้ได้

### <a name="issue-resolution"></a>การแก้ไขปัญหา

อันดับแรก ให้ตรวจสอบการตั้งค่า [การเบิกสินค้าคลัสเตอร์](set-up-cluster-picking.md) และตรวจสอบให้แน่ใจว่ามีการตั้งค่าโปรไฟล์ของคลัสเตอร์ของคุณอย่างถูกต้อง คุณไม่สามารถใช้รายการเมนูของอุปกรณ์เคลื่อนที่สำหรับการเบิกสินค้าคลัสเตอร์เว้นแต่จะมีการตั้งค่าโปรไฟล์ของคลัสเตอร์ ขึ้นอยู่กับสภาพแวดล้อมของคุณ คุณอาจต้องตรวจทานการตั้งค่าคอนฟิกที่เกี่ยวข้องอื่น ๆ

## <a name="mixed-license-plate-receiving-doesnt-work-for-any-disposition-code-except-credit"></a>การรับป้ายทะเบียนแบบผสมไม่ทำงานสำหรับรหัสการโอนการครอบครองใด ๆ ยกเว้นเครดิต

### <a name="issue-description"></a>คำอธิบายปัญหา

เมื่อฟิลด์ **การดำเนินการ** สำหรับรหัสการโอนการครอบครองถูกตั้งค่าเป็น *เครดิต* หรือ *เสีย* คุณสามารถใช้ได้เฉพาะ [รายการเมนูการรับป้ายทะเบียนแบบผสม](mixed-license-plate-receiving.md) เพื่อประมวลผลสินค้าที่ส่งคืนเท่านั้น

### <a name="issue-resolution"></a>การแก้ไขปัญหา

Microsoft ได้ประเมินปัญหานี้แล้วและได้ระบุว่าเป็นข้อจำกัดของลักษณะการทำงาน ปัจจุบัน เฉพาะ [รหัสการโอนการครอบครอง](../service-management/set-up-disposition-codes.md) ที่มีฟิลด์ **การดำเนินการ** ตั้งค่าเป็น *เครดิต* หรือ *เสีย* ได้รับการสนับสนุนสำหรับการรับป้ายทะเบียนแบบผสม

## <a name="when-i-run-the-update-product-receipts-periodic-task-unconfirmed-purchase-orders-are-confirmed"></a>เมื่อฉันเรียกใช้งานประจำงวดอัปเดตใบรับสินค้า ใบสั่งซื้อที่ยังไม่ได้ยืนยันจะได้รับการยืนยัน

### <a name="issue-description"></a>คำอธิบายปัญหา

หลังจากที่คุณเรียกใช้งานประจำงวด *อัปเดตใบรับสินค้า* ระบบจะยืนยันใบสั่งซื้อที่ยังไม่ได้ยืนยันที่มีสถานะธุรกรรมสินค้าคงคลังที่ *ลงทะเบียน* ไว้โดยอัตโนมัติ

### <a name="issue-resolution"></a>การแก้ไขปัญหา

ลักษณะการทำงานในการจัดการโหลดขาเข้าใหม่ *ผ่านการรับสินค้าในปริมาณการโหลด* ให้แก้ไขปัญหานี้ เมื่อต้องการเปิดคุณลักษณะนี้ ไปที่ [การจัดการคุณลักษณะ](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) และเปิดใช้งานคุณลักษณะต่อไปนี้ (ในใบสั่งที่แสดงในรายการ):

1. เชื่อมโยงธุรกรรมสินค้าคงคลังของใบสั่งซื้อกับการบรรทุก
1. การรับเกินปริมาณของการบรรทุก

สำหรับข้อมูลเพิ่มเติม ให้ดูที่ [ลงรายการบัญชีปริมาณผลิตภัณฑ์ที่ลงทะเบียนสำหรับใบสั่งซื้อ](inbound-load-handling.md#post-registered-quantities)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]