---
title: คุณไม่สามารถยืนยันการจัดส่งได้ เนื่องจากสินค้ายังไม่ได้รับการเบิก
description: คุณไม่สามารถยืนยันการจัดส่งได้ เนื่องจากสินค้ายังไม่ได้รับการเบิก
author: perlynne
ms.date: 04/21/2021
ms.topic: troubleshooting
ms.search.form: WHSLoadTable_WHSShipConfirm,WHSLoadPlanningListPage_WHSShipConfirm,WHSLoadPlanningWorkbench_WHSShipConfirm,WHSTransportLoad_WHSShipConfirm,WHSShipPlanningListPage_WHSShipConfirm,WHSShipmentDetails_WHSShipConfirm,WHSWorkTable_WHSShipConfirm,WHSWorkTableListPage_WHSShipConfirm,Dialog_WHSOutboundShipConfirmController_WHSOutboundShipConfirm
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: lbc
ms.search.validFrom: 2021-04-21
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: 23a517e7769dc86ebec30e4f17c62172a6ad8801
ms.sourcegitcommit: cd9016e9787169cb800889d335b9c5919ddbe4af
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 04/23/2021
ms.locfileid: "5938560"
---
# <a name="you-cant-confirm-a-shipment-because-items-havent-been-picked"></a>คุณไม่สามารถยืนยันการจัดส่งได้ เนื่องจากสินค้ายังไม่ได้รับการเบิก

รหัสข้อผิดพลาด: LoadNotPickedAndMovedToFinalShippingLocation

## <a name="symptoms"></a>อาการ

เมื่อคุณพยายามยืนยันการจัดส่ง ระบบจะแสดงข้อความแสดงข้อผิดพลาดต่อไปนี้:

> สินค้าบางอย่างที่จำเป็นสำหรับจำนวนงานในศูนย์การผลิต %1 ยังไม่ได้รับการเบิกและเคลื่อนย้ายไปยังสถานที่จัดส่งขั้นสุดท้าย

ดังนั้นคุณจึงไม่สามารถยืนยันการจัดส่งของสินค้าได้

## <a name="cause"></a>สาเหตุ

ไม่สามารถยืนยันสินค้าหรือการจัดส่งในสถานะปัจจุบันได้เนื่องจากอาจมีเงื่อนไขอย่างใดอย่างหนึ่งต่อไปนี้

- ยังไม่ได้เบิกสินค้าและย้ายไปยังสถานที่จัดส่งสุดท้าย
- ปริมาณงานที่เบิกไม่ตรงกับปริมาณงานที่สร้างบนรายการสินค้า

## <a name="resolution"></a>ความละเอียด

ตรวจสอบใบสั่งขายหรือใบสั่งโอนย้ายที่เกี่ยวข้องเกี่ยวกับสินค้าหรือการจัดส่ง ตรวจสอบให้แน่ใจว่างานที่เกี่ยวข้องทั้งหมดเสร็จสมบูรณ์แล้วในสถานที่จัดส่งสุดท้าย และปริมาณตรงกัน

1. ไปที่ **การจัดการคลังสินค้า \> จำนวนงานในศูนย์การผลิต \> จำนวนงานในศูนย์การผลิตทั้งหมด**
1. เลือกสินค้าที่การจัดส่งไม่สามารถยืนยันได้
1. บนแท็บด่วน **รายการสินค้า** ให้เลือกรายการสินค้า
1. บันทึกค่าของฟิลด์ **ปริมาณที่สร้างขึ้นของงาน**
1. บนบานหน้าต่างการดำเนินการ บนแท็บ **สินค้า** ในกลุ่ม **ข้อมูลที่เกี่ยวข้อง** ให้เลือก **งาน**
1. ตรวจสอบว่างานเสร็จสมบูรณ์แล้วที่สถานที่จัดส่งสุดท้าย และปริมาณงานที่เบิกตรงกับปริมาณงานที่สร้างบนรายการสินค้า
1. ทําขั้นตอนนี้ซ้ํากับรายการสินค้าทั้งหมดเพื่อให้แน่ใจว่าตรงตามเกณฑ์ทั้งหมด
