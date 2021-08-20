---
title: ใบรับสินค้าที่ยกเลิกจะไม่อัปเดตสถานะธุรกรรมเป็น ลงทะเบียนแล้ว
description: หลังจากที่คุณยกเลิกใบรับสินค้าสินค้าขาเข้าแล้ว ระบบจะอัปเดตสถานะรายการความเคลื่อนไหวของสินค้าคงคลังจาก ได้รับแล้ว เป็น สั่งแล้ว โดยอัตโนมัติ
author: GalynaFedorova
ms.date: 06/11/2021
ms.topic: troubleshooting
ms.search.form: WMSPickingRegistration
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: v-gfedorova
ms.search.validFrom: 2021-06-11
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: eae703ce0b2c981518b18c4badd4f90031b902ece62f3ca0837427b306d618b1
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 08/05/2021
ms.locfileid: "6731114"
---
# <a name="canceled-product-receipts-dont-update-transaction-status-to-registered"></a>ใบรับสินค้าที่ยกเลิกจะไม่อัปเดตสถานะธุรกรรมเป็น ลงทะเบียนแล้ว

## <a name="symptoms"></a>อาการ

หลังจากที่คุณเรียกใช้การดำเนินการ **ยกเลิกใบรับสินค้าสินค้าขาเข้า** ระบบจะอัปเดตสถานะรายการความเคลื่อนไหวของธุรกรรมสินค้าคงคลังจาก *ได้รับแล้ว* เป็น *สั่งแล้ว* โดยอัตโนมัติ

## <a name="resolution"></a>การแก้ปัญหา

เมื่อบันทึกการจัดส่งถูกยกเลิกสำหรับสินค้าขาออก สถานะของรายการความเคลื่อนไหวของสินค้าคงคลังจะยังคงเป็น *เบิกสินค้าแล้ว* อย่างไรก็ตาม เมื่อใบรับสินค้าจากสินค้าขาเข้าถูกยกเลิก สถานะของรายการความเคลื่อนไหวของสินค้าคงคลังจะไม่ได้รับการคืนค่าเป็น *ลงทะเบียนแล้ว* ดังนั้นหลังจากที่ใบรับสินค้าจากจํานวนงานในคลังถูกยกเลิก พนักงานคลังสินค้าต้องลงทะเบียนปริมาณสินค้าอีกครั้งให้กับจํานวนสินค้าในคลัง

สำหรับข้อมูลเพิ่มเติม ให้ดู [ลงทะเบียนปริมาณสินค้าที่มาถึงในสินค้าขาเข้า](/dynamics365/supply-chain/warehousing/inbound-load-handling#register-item-quantities-arriving)
