---
title: แก้ไขปัญหางานคลังสินค้า
description: หัวข้อนี้อธิบายวิธีการแก้ไขปัญหาทั่วไปที่คุณอาจพบในระหว่างที่คุณทำงานในคลังสินค้าใน Microsoft Dynamics 365 Supply Chain Management
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
ms.openlocfilehash: a00ae517ff583e4231099d8e9f5d5b5a696cf7f7
ms.sourcegitcommit: deb711c92251ed48cdf20ea514d03461c26a2262
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 11/25/2020
ms.locfileid: "4645804"
---
# <a name="troubleshoot-warehouse-work"></a>แก้ไขปัญหางานคลังสินค้า

[!include [banner](../includes/banner.md)]

หัวข้อนี้อธิบายวิธีการแก้ไขปัญหาทั่วไปที่คุณอาจพบในระหว่างที่คุณทำงานในคลังสินค้าใน Microsoft Dynamics 365 Supply Chain Management

## <a name="i-cant-move-license-plates-that-have-serial-number-items-when-blank-issue-and-blank-receipt-are-allowed-on-the-tracking-dimension-group"></a>ฉันไม่สามารถย้ายป้ายทะเบียนที่มีสินค้าหมายเลขลำดับประจำสินค้าเมื่อการตัดสินค้าที่ว่างเปล่าได้และการรับสินค้าที่ว่างเปล่าสามารถทำได้บนกลุ่มมิติการติดตาม

### <a name="issue-description"></a>คำอธิบายปัญหา

คุณไม่สามารถย้ายป้ายทะเบียนได้โดยใช้รายการเมนู **การเคลื่อนย้าย** ถ้าหมายเลขลำดับประจำสินค้ามีการตั้งค่า *การตัดสินค้าที่ว่างเปล่าได้* และ *การรับสินค้าที่ว่างเปล่าได้* บนกลุ่มมิติการติดตาม และถ้ามีป้ายทะเบียนหลายใบในสถานที่เดียวกัน บางรายมีหมายเลขลำดับประจำสินค้าและบางอย่างที่ไม่มีหมายเลขลำดับประจำสินค้า

### <a name="issue-resolution"></a>การแก้ไขปัญหา

ปัญหานี้จะได้รับการแก้ไขโดยการเปลี่ยนแปลงที่มีการปรับใช้ใน [KB 4571546](https://fix.lcs.dynamics.com/Issue/Details?kb=4571546&bugId=467880&dbType=3&qc=5b46d7faa9cc326cebfe9854cb30be8ea30b21ef33d3572c325fbb21202de687) การเปลี่ยนแปลงดังกล่าวจะทำให้ฟิลด์ **หมายเลขประจำสินค้า** ไม่จำเป็นต้องระบุเมื่อการตัดสินค้าที่ว่างเปล่าได้และการรับสินค้าที่ว่างเปล่าสามารถทำได้

## <a name="i-receive-the-following-error-message-in-the-warehouse-app-when-i-process-movements-the-inventory-owner-1-is-not-allowed-in-this-process"></a>ฉันได้รับข้อความแสดงข้อผิดพลาดต่อไปนี้ในแอปคลังสินค้าเมื่อฉันประมวลผลการย้ายสินค้า: "เจ้าของสินค้าคงคลัง %1 ไม่ได้รับอนุญาตในกระบวนการนี้"

### <a name="issue-description"></a>คำอธิบายปัญหา

มิติการติดตาม **เจ้าของ** หายไปเมื่อแอปคลังสินค้าใช้เพื่อทำการเคลื่อนย้าย สมุดรายวันการโอนย้ายสินค้าคงคลังปกติจากไคลเอนต์ Supply Chain Management จะปรากฏขึ้นเพื่อให้คุณสามารถลงรายการบัญชีได้อย่างถูกต้อง และสามารถลงรายการบัญชีได้เฉพาะเมื่อมีการกรอกข้อมูลมิติ **เจ้าของ** ไว้เท่านั้น

### <a name="issue-resolution"></a>การแก้ไขปัญหา

Microsoft ได้ประเมินปัญหานี้แล้วและได้ระบุว่าเป็นข้อจำกัดของลักษณะการทำงาน ขณะนี้ กระบวนการจัดการคลังสินค้าสนับสนุนเฉพาะสินค้าคงคลังที่เป็นของนิติบุคคลเท่านั้น
