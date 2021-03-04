---
title: แก้ไขปัญหาการดำเนินงานคลังสินค้าขาออก
description: หัวข้อนี้อธิบายวิธีการแก้ไขปัญหาทั่วไปที่คุณอาจพบในระหว่างที่คุณทำงานการดำเนินงานคลังสินค้าขาออกใน Microsoft Dynamics 365 Supply Chain Management
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
ms.openlocfilehash: 56bd91d8a6fe895317021d806e180df3a2db302b
ms.sourcegitcommit: deb711c92251ed48cdf20ea514d03461c26a2262
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 11/25/2020
ms.locfileid: "4645464"
---
# <a name="troubleshoot-outbound-warehouse-operations"></a>แก้ไขปัญหาการดำเนินงานคลังสินค้าขาออก

[!include [banner](../includes/banner.md)]

หัวข้อนี้อธิบายวิธีการแก้ไขปัญหาทั่วไปที่คุณอาจพบในระหว่างที่คุณทำงานการดำเนินงานคลังสินค้าขาออกใน Microsoft Dynamics 365 Supply Chain Management

## <a name="i-receive-the-following-error-message-sales-order-could-not-be-released"></a>ฉันได้รับข้อความแสดงข้อผิดพลาดต่อไปนี้: "ใบสั่งขายไม่สามารถนำออกใช้ได้"

### <a name="issue-description"></a>คำอธิบายปัญหา

ปัญหานี้อาจเกิดขึ้นจากสาเหตุหลายประการ ตัวอย่างเช่น ใบสั่งอยู่ระหว่างการระงับการบริหารเครดิต และไม่สามารถสร้างการจัดส่งจนกว่าจะมีการป้อนที่อยู่ไปรษณีย์ที่ถูกต้องสำหรับรายการการขายทั้งหมดที่เชื่อมโยงกับใบสั่งขาย อีกทางหนึ่งคือ มีการระงับใบสั่งที่ต้องมีการแก้ไขก่อนจึงจะสามารถนำใบสั่งออกใช้ไปยังคลังสินค้าได้ การระงับนี้อาจเป็นใบสั่งเฉพาะ หรืออาจอยู่ในรหัสลูกค้า

### <a name="issue-resolution"></a>การแก้ไขปัญหา

เพิ่มหรืออัพเดตที่อยู่ในใบสั่งขายและรายการใบสั่ง แล้วปล่อยใบสั่งไปยังคลังสินค้า คุณสามารถนำใบสั่งออกใช้ไปยังคลังสินค้าได้เฉพาะเมื่อมีที่อยู่ที่จัดส่งที่ถูกต้อง (ตามการตั้งค่ารูปแบบที่อยู่ในโมดูล **การจัดการองค์กร**)

ตรวจสอบการระงับใบสั่ง และแก้ปัญหา ลบการระงับจากใบสั่งหรือลูกค้า แล้วปล่อยใบสั่งไปยังคลังสินค้า

## <a name="i-receive-the-following-message-the-shipment-for-load-1-has-been-confirmed-however-no-lines-are-posted"></a>ฉันได้รับข้อความแสดงข้อความต่อไปนี้: "การจัดส่งสำหรับจำนวนงานในศูนย์การผลิต 1% ถูกยืนยันแล้ว" อย่างไรก็ตาม จะไม่มีการลงรายการบัญชีรายการใด ๆ

### <a name="issue-description"></a>คำอธิบายปัญหา

การจัดส่งสินค้าในจำนวนงานในศูนย์การผลิตได้รับการยืนยันแล้ว แต่ยังไม่มีการลงรายการบัญชีเพิ่มเติม

### <a name="issue-resolution"></a>การแก้ไขปัญหา

การยืนยันการจัดส่งไม่มีผลกระทบต่อการลงรายการบัญชี อัพเดตสถานะการจัดส่งและโหลดเท่านั้น การลงรายการบัญชีต้องเกิดขึ้นในกระบวนการแยกต่างหาก

## <a name="i-receive-the-following-error-message-direct-delivery-is-not-able-to-process-for-warehouse-1-as-it-has-warehouse-management-enabled-please-specify-another-warehouse-that-is-not-enabled-for-warehouse-management"></a>ฉันได้รับข้อความแสดงข้อผิดพลาดต่อไปนี้: "การจัดส่งสินค้าโดยตรงไม่สามารถดำเนินการสำหรับคลังสินค้า 1% เนื่องจากมีการเปิดใช้งานการจัดการคลังสินค้า โปรดระบุคลังสินค้าอื่นที่ไม่ได้เปิดใช้งานสำหรับการจัดการคลังสินค้า"

### <a name="issue-description"></a>คำอธิบายปัญหา

มีการเพิ่มสินค้าในรายการขายสำหรับการจัดส่งสินค้าโดยตรงจากคลังสินค้าที่เปิดใช้งานสำหรับการจัดการคลังสินค้า (WMS) คุณได้รับข้อความแสดงข้อความแสดงข้อผิดพลาดนี้เมื่อมีการอัพเดตรายการการขาย 

### <a name="issue-resolution"></a>การแก้ไขปัญหา

Microsoft ได้ประเมินปัญหานี้แล้วและได้ระบุว่าเป็นข้อจำกัดของลักษณะการทำงาน ปัจจุบัน WMS ไม่สนับสนุนการจัดส่งสินค้าโดยตรง เมื่อต้องการใช้การจัดส่งสินค้าโดยตรง คุณต้องเลือกสินค้าที่ไม่ใช่ WMS และคลังสินค้า


[!INCLUDE[footer-include](../../includes/footer-banner.md)]