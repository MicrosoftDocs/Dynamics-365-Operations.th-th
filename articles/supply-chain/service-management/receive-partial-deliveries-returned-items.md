---
title: รับการจัดส่งบางส่วนของสินค้าส่งคืน
description: 'การจัดส่งเป็นบางส่วนมีการกำหนดในรูปแบบของบรรทัดใบสั่งส่งคืนสินค้า ไม่ใช่การจัดส่งของใบสั่งส่งคืนสินค้า '
author: sorenva
ms.date: 05/01/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: sorenand
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 6c0e27e3a5cb6be36a1d69190ce1b01ecada48a6
ms.sourcegitcommit: 9166e531ae5773f5bc3bd02501b67331cf216da4
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 05/03/2022
ms.locfileid: "8677127"
---
# <a name="receive-partial-deliveries-of-returned-items"></a>รับการจัดส่งบางส่วนของสินค้าส่งคืน    

[!include [banner](../includes/banner.md)]


การจัดส่งเป็นบางส่วนมีการกำหนดในรูปแบบของบรรทัดใบสั่งส่งคืนสินค้า ไม่ใช่การจัดส่งของใบสั่งส่งคืนสินค้า 

นี่หมายความว่า ถ้าคุณได้รับปริมาณสินค้าทั้งหมดซึ่งถูกบ่งชี้ไว้ในรายการใบสั่งส่งคืนสินค้าหนึ่งรายการ แต่คุณไม่ได้รับสินค้าจากรายการอื่นในใบสั่งส่งคืนสินค้า การจัดส่งนี้ไม่ใช่การจัดส่งเป็นบางส่วน อย่างไรก็ตาม ถ้ารายการใบสั่งส่งคืนสินค้าต้องการสินค้าเฉพาะ 10 หน่วยให้ถูกส่งคืน แต่คุณได้รับสินค้านั้นเพียงสี่รายการ ถือเป็นการจัดส่งบางส่วน

ถ้าการจัดส่งคืนมีสินค้าน้อยกว่าปริมาณทั้งหมดของบรรทัดใบสั่งส่งคืนสินค้า คุณสามารถตั้งค่าการจัดส่งเพิ่มเติมและรอให้ส่วนที่เหลือของปริมาณที่ส่งคืนมาถึง หรือคุณสามารถลงทะเบียนและลงรายการบัญชีปริมาณบางส่วนก็ได้

## <a name="register-and-post-a-partial-quantity"></a>การลงทะเบียนและลงรายการบัญชีปริมาณบางส่วน

1.  หลังจากที่คุณเลือกใบสั่งส่งคืนสำหรับการมาถึงในฟอร์ม **ภาพรวมการมาถึง - คลังสินค้า: %1 ท่าเรือ: %2 ชื่อสมุดรายวัน: %3** คลิก **เริ่มต้นการมาถึง** เพื่อสร้างสมุดรายวันการมาถึง จากนั้น คลิก **สมุดรายวัน** \> **แสดงการมาถึงจากใบรับ** เพื่อเปิดฟอร์ม **สมุดรายวันสถานที่**

2.  เลือกรายการของสมุดรายวันที่คุณต้องการทำงานด้วย และจากนั้นคลิก **รายการ** เพื่อเปิดแบบฟอร์ม **รายการสมุดรายวัน, สถานที่เก็บ**

3.  เลือกรายการของหมายเลขสินค้า ซึ่งสินค้าได้มาถึงเพียงบางส่วนเท่านั้น แล้วคลิก **ฟังก์ชัน** \> **แบ่ง** เพื่อเปิดแบบฟอร์ม **แบ่ง**

4.  ในฟิลด์ **แบ่งปริมาณ** ให้ป้อนปริมาณสำหรับจำนวนทั้งหมดของสินค้าที่ได้รับ แล้วคลิก **ตกลง**

5.  บนแบบฟอร์ม **รายการสมุดรายวัน, สถานที่เก็บ** ให้เลือกรายการสำหรับปริมาณของสินค้าที่มาถึงแล้ว แล้วคลิก **ลงรายการบัญชี** คุณสามารถลงรายการบัญชีรายการสำหรับปริมาณสินค้าเพิ่มเติม หลังจากที่สินค้ามาถึงได้






[!INCLUDE[footer-include](../../includes/footer-banner.md)]