---
title: คุณไม่สามารถยืนยันการจัดส่งได้ เนื่องจากมีปริมาณเป็นศูนย์
description: คุณไม่สามารถยืนยันการจัดส่งได้ เนื่องจากมีปริมาณเป็นศูนย์
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
ms.openlocfilehash: 7a06f0651db741a867e1e9fe7dbab841a928c22b
ms.sourcegitcommit: cd9016e9787169cb800889d335b9c5919ddbe4af
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 04/23/2021
ms.locfileid: "5938559"
---
# <a name="you-cant-confirm-a-shipment-because-there-is-zero-quantity"></a>คุณไม่สามารถยืนยันการจัดส่งได้ เนื่องจากมีปริมาณเป็นศูนย์

รหัสข้อผิดพลาด: LoadLineWarningUpdatedToZero

## <a name="symptoms"></a>อาการ

เมื่อคุณพยายามยืนยันการจัดส่ง ระบบจะแสดงข้อความแสดงข้อผิดพลาดต่อไปนี้:

> รายการบรรทุกสำหรับสินค้า %1 และการจัดส่ง %2 ได้รับการอัพเดตให้มีปริมาณเป็นศูนย์ เนื่องจากการตั้งค่าการจัดส่งน้อยกว่าปริมาณที่สั่งทำให้ไม่สามารถจัดส่งด้วยปริมาณใดๆ สำหรับสินค้านี้

ดังนั้นคุณจึงไม่สามารถยืนยันการจัดส่งของสินค้าได้

## <a name="cause"></a>สาเหตุ

ระบบประเมินว่าปริมาณที่เบิกอยู่ภายในขีดจํากัดที่คาดไว้หรือไม่ ตามปริมาณที่เบิก สินค้าตามปริมาณรายการโหลด และเปอร์เซ็นต์การจัดส่งน้อยกว่าปริมาณที่สั่ง หากระบบพบว่าปริมาณที่เบิกในรายการสินค้าคือ 0 (ศูนย์) คุณไม่สามารถยืนยันการจัดส่งได้ ตัวอย่างเช่น ปัญหานี้อาจเกิดขึ้นหากงานถูกยกเลิกและเปอร์เซ็นต์การจัดส่งน้อยกว่าปริมาณที่สั่งในรายการสินค้าคือ 100 เปอร์เซ็นต์

## <a name="resolution"></a>ความละเอียด

ตรวจสอบรายการสินค้าของคุณเพื่อให้แน่ใจว่าเปอร์เซ็นต์และปริมาณการจัดส่งน้อยกว่าปริมาณที่สั่งเกินสอดคล้องกับงานที่เบิกสินค้าแล้ว

1. ไปที่ **การจัดการคลังสินค้า \> จำนวนงานในศูนย์การผลิต \> จำนวนงานในศูนย์การผลิตทั้งหมด**
1. เลือกสินค้าที่การจัดส่งไม่สามารถยืนยันได้
1. บนแท็บด่วน **รายการสินค้า** ให้เลือกรายการสินค้าที่เกินกว่าเปอร์เซ็นต์การจัดส่งน้อยกว่าปริมาณที่กำหนด
1. ปรับปรุงค่าของฟิลด์ **การจัดส่งน้อยกว่าปริมาณที่สั่ง** หรือฟิลด์ **ปริมาณ** ตามที่ต้องการ

> [!TIP]
> ถ้าปัญหายังไม่ได้รับการแก้ไข คุณอาจต้องกรอกฟอร์มงานการเบิกสินค้าเพิ่มเติมให้กับใบสั่งขายหรือใบสั่งโอนย้ายที่เกี่ยวข้องจนกว่าปริมาณที่พร้อมใช้งานจะสอดคล้องกับรายการสินค้าหรือการจัดส่ง
