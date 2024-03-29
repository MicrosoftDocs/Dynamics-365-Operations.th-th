---
title: เกี่ยวกับการปรับปรุงข้อมูลทางการเงินตามจริง
description: ในบทความนี้จะแสดงภาพรวมของชนิดธุรกรรมที่เพิ่มหรือลดปริมาณสินค้าคงคลัง
author: JennySong-SH
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: InventTrans, InventTransVoucher
audience: Application User
ms.reviewer: kamaybac
ms.custom: 75023
ms.assetid: 128340e1-c573-48e6-b835-6c350d8dd0fb
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: yanansong
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 345f07e7ba55f567c9956539241c080db958c848
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 06/03/2022
ms.locfileid: "8895857"
---
# <a name="physical-and-financial-updates"></a>เกี่ยวกับการปรับปรุงข้อมูลทางการเงินตามจริง

[!include [banner](../includes/banner.md)]

ในบทความนี้จะแสดงภาพรวมของชนิดธุรกรรมที่เพิ่มหรือลดปริมาณสินค้าคงคลัง 

ธุรกรรมสินค้าคงคลังสามารถถูกปรับปรุงทางกายภาพและถูกปรับปรุงทางการเงินได้ใน Dynamics 365 Supply Chain Management ธุรกรรมทางกายภาพ และทางการเงินบางอย่างเพิ่มปริมาณสินค้าคงคลัง ในขณะที่ธุรกรรมบางอย่างจะลดปริมาณสินค้าคงเหลือลง

## <a name="physical-increases"></a>การเพิ่มขึ้นทางกายภาพ
เมื่อมีการลงบัญชีธุรกรรมนั้นแล้ว สถานะของบันทึกธุรกรรมจะเป็น **ได้รับแล้ว** ธุรกรรมต่อไปนี้จะถือว่าเป็นการเพิ่มขึ้นทางกายภาพ

-   การรับสินค้าตามใบสั่งซื้อ
-   การส่งคืนบันทึกการจัดส่งของใบสั่งขาย
-   รายงานการการผลิตสินค้าที่เสร็จสิ้น
-   ผลผลอยได้ในบันทึกการจัดส่งของใบสั่งผลิต

## <a name="financial-increases"></a>การเพิ่มขึ้นทางการเงิน
รายการทางการค้าเกิดขึ้นเมื่อมีการออกใบเสร็จรับเงิน สถานะของบันทึกธุรกรรมที่เพิ่มปริมาณจะเป็น **ซื้อแล้ว** ธุรกรรมต่อไปมีผลให้การเงินเปลี่ยนแปลง

-   ใบแจ้งหนี้ของผู้จัดจำหน่าย
-   ใบแจ้งหนี้ใบสั่งขายสำหรับการส่งคืน
-   การคำนวณต้นทุนใบสั่งผลิต
-   ยอดของสินค้าคงเหลือในสมุดบันชีรายวัน บอกความเคลื่นไหว กำไรและขาดทุน การนับจำนวน รายการวัสดุและส่วนประกอบ   และการโอนย้าย

## <a name="transactions-that-increase-quantity"></a>ธุรกรรมที่เพิ่มปริมาณ
รายการค้าที่เกิดขึ้นถูกโอนไปที่เป็นต้นทุนโดยวิธีการเฉลี่ย Dynamics AX ใช้การคำนวณราคาต้นทุนเฉลี่ยเมื่อมีเกิดรายการค้าที่ทำให้สินค้าคงเหลือลดจำนวนลง โดยไม่คำนึงถึงแบบจำลองสินค้าคงคลังที่เกี่ยวข้องกับสินค้าคงคลังนั้น สามารถดูข้อมูลเกี่ยวกับราคาต้นทุนเฉลี่ยที่นี่ [ราคาต้นทุนเฉลี่ยปัจจุบัน](running-average-cost-price.md)

## <a name="transactions-that-decrease-quantity"></a>ธุรกรรมที่ลดปริมาณ
ราคาต้นทุนเฉลี่ยที่รันการคำนวณอยู่ถูกใช้เมื่อธุรกรรมลดจำนวนลงรายการลง โดยไม่คำนึงถึงแบบจำลองสินค้าคงคลังที่เกี่ยวข้องกับสินค้าคงคลังนั้น รายการค้าที่ลดจำนวนลงจะไม่ถูกลงบัญชีจนกว่ารายการค้าที่เกิดขึ้นก่อนหน้านั้นลงบัญชี หากสินค้าคงคลังที่พร้อมใช้งานจริงกลายเป็นติดลบ ต้นทุนสินค้าคงคลังที่ถูกกำหนดสำหรับรายการในหน้า **รายการ** จะถูกใช้งาน 

> [!NOTE]
> หากฟังก์ชันหลายไซต์ถูกเปิดใช้งาน ต้นทุนนี้จะเป็นต้นทุนสินค้าคงคลังที่กำหนดสำหรับไซต์ในหน้า **การตั้งค่าใบสั่งเริ่มต้น**

## <a name="physical-issues-vs-financial-issues"></a>การตัดสินค้าตามจริงเทียบกับการตัดสินค้าทางการเงิน
เมื่อมีการลงบัญชีธุรกรรมนั้นแล้ว สถานะของบันทึกธุรกรรมนี้เป็น **หักแล้ว** ธุรกรรมต่อไปนี้ได้รับพิจารณาว่าเป็นปัญหาทางกายภาพ:

-   สมุดรายวันรายการเบิกสินค้าของใบสั่งผลิต
-   บันทึกการจัดส่งของใบสั่งขาย
-   การส่งคืนบันทึกการจัดส่งของใบสั่งซื้อ

เมื่อมีการลงบัญชีธุรกรรมนั้นแล้ว สถานะของบันทึกธุรกรรมนี้เป็น **ขายแล้ว** ธุรกรรมต่อไปนี้ได้รับพิจารณาว่าเป็นปัญหาทางการเงิน:

-   ผลิตสินค้าตามใบสั่งผลิต
-   ใบแจ้งหนี้ของใบสั่งขาย
-   ส่งคืนใบแจ้งหนี้ของผู้จัดจำหน่าย
-   ยอดของสินค้าคงเหลือในสมุดบันชีรายวัน บอกความเคลื่นไหว กำไรและขาดทุน การนับจำนวน รายการวัสดุและส่วนประกอบ   และการโอนย้าย

รายการค้าที่ทำให้สินค้าลดลง ถูกโอนไปที่เป็นต้นทุนโดยวิธีการเฉลี่ย กระบวนการตรวจนับสินค้าคงคลัง คือ จับคู่ธุรกรรมการค้าที่เกิดขึ้นกับใบเสร็จ ขึ้นอยู่กับวิธีการที่ใช่้ในการจัดการสินค้าคงเหลือ


[!INCLUDE[footer-include](../../includes/footer-banner.md)]