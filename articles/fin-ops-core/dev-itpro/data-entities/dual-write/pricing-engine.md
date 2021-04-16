---
title: ซิงค์ตามต้องการกับกลไกจัดการการกำหนดราคา Supply Chain Management
description: หัวข้อนี้จะอธิบายวิธีการใช้กลไกการกำหนดราคาใน Microsoft Dynamics 365 Supply Chain Management จาก Dynamics 365 Sales
author: RamaKrishnamoorthy
ms.date: 03/10/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-03-10
ms.openlocfilehash: bf4154816f01040a236dde77b92ee69396158614
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 03/31/2021
ms.locfileid: "5750775"
---
# <a name="sync-on-demand-with-the-supply-chain-management-pricing-engine"></a>ซิงค์ตามต้องการกับกลไกจัดการการกำหนดราคา Supply Chain Management

[!include [banner](../../includes/banner.md)]



Microsoft Dynamics 365 Supply Chain Management รวมกลไกการกำหนดราคาที่จัดการข้อตกลงทางการค้า รายการราคา โปรแกรมตอบแทนลูกค้าสมาชิก โปรโมชัน และส่วนลด กลไกการกำหนดราคาจะใช้กฎที่ซับซ้อนเพื่อกำหนดราคาที่ดีที่สุดสำหรับใบเสนอราคาหรือใบสั่งที่กำหนด เมื่อคุณใช้การรวมแบบสองทิศทาง คุณใช้การกำหนดราคาแบบคงที่ หรือกลไกจัดการการกำหนดราคาจาก Dynamics 365 Supply Chain Management บนหน้าใบเสนอราคาและใบสั่งใน Dynamics 365 Sales

## <a name="use-the-pricing-engine-from-supply-chain-management-in-sales"></a>ใช้กลไกการกำหนดราคาจาก Supply Chain Management ใน Sales

1. ใน Sales ให้ไปที่ **Sales \> ใบสั่ง**
2. เลือก **สร้าง** เพื่อสร้างใบสั่งใหม่ หรือเลือกใบสั่งที่มีอยู่แล้วในรายการ **ใบสั่งของฉัน**
3. เพิ่มรายการในใบสั่งใหม่
4. ถ้าคุณกำลังสร้างใบสั่งใหม่ ให้เลือก **ใบสั่งราคา** ในบานหน้าต่างการดำเนินการ ถ้าคุณกำลังปรับปรุงใบสั่งที่มีอยู่ ให้เลือก **คำนวณใหม่** ในบานหน้าต่างการดำเนินการ

    คอลัมน์ต่อไปนี้จะถูกเติมโดยอัตโนมัติใน:

    + ยอดรายละเอียด
    + % ส่วนลด
    + ส่วนลด
    + ยอดเงินก่อนการขนส่ง
    + ยอดเงินค่าขนส่ง
    + ภาษีรวม
    + ยอดเงินรวม
    
5. เพื่อให้แน่ใจว่าระบบจะพิจารณาข้อตกลงทางการค้าและการขายเพื่อคำนวณราคา:
    1. นำทางไปยังสภาพแวดล้อม Supply Chain Management ของคุณ
    2. นำทางไปยัง **บัญชีลูกหนี้ \> การตั้งค่า \> พารามิเตอร์บัญชีลูกหนี้**
    3. เลือกแท็บ **ราคา** ในแถบนำทางด้านข้าง
    4. ภายใต้ fastab **การประเมินข้อตกลงทางการค้า** ให้ยกเลิกการเลือกตัวเลือก **การป้อนข้อมูลด้วยตนเอง**

## <a name="how-it-works"></a>วิธีการทำงาน

เมื่อคุณเลือก **ใบสั่งราคา** ในการขาย ฟังก์ชัน **ยอดรวม** บนแท็บ **ใบสั่งขาย \> มุมมอง** ใน Supply Chain Management ถูกเรียกสำหรับใบสั่งขายที่เกี่ยวข้อง ค่าในยอดรวมของใบสั่งใน Sales จะใช้ในการกรอกข้อมูลในคอลัมน์ที่เกี่ยวข้องใน Supply Chain Management

เมื่อมีการคำนวณผลรวมของใบสั่งขายใน Supply Chain Management การคำนวณจะประเมินข้อตกลงทางการค้าที่มีอยู่และข้อตกลงการขายสำหรับลูกค้าและผลิตภัณฑ์ที่แสดงรายการอยู่ในใบสั่งขาย ข้อมูลนี้จะใช้เพื่อคำนวณผลรวม เมื่อมีการเลือก **ใบสั่งราคา** Sales จะสะท้อนถึงการตั้งค่าทั้งหมดที่มีการดำเนินการใน Supply Chain Management

## <a name="limitations"></a>การจำกัด

เมื่อมีการกรอกข้อมูลในคอลัมน์ใน Sales จะมีการใช้ข้อจำกัดต่อไปนี้:

+ การตั้งค่าค่าธรรมเนียมและการปันส่วนค่าธรรมเนียมใน Supply Chain Management ไม่ถูกคัดลอกใน Sales
+ การกำหนดราคาไม่ได้พิจารณาการกำหนดราคาขายปลีกพิเศษที่ระบุไว้ในคอลัมน์ **ช่องทางการขายปลีก** บนหน้ารายการใบสั่งขายใน Supply Chain Management
+ ส่วนลดที่กำหนดในส่วน **การจัดการการให้ส่วนลดทางการค้า** ของ Supply Chain Management ไม่ได้รับการพิจารณา


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]