---
title: คุณไม่สามารถยืนยันการจัดส่งได้เนื่องจากลูกค้าถูกระงับไว้ชั่วคราว
description: คุณไม่สามารถยืนยันการจัดส่งได้เนื่องจากลูกค้าถูกระงับไว้ชั่วคราว
author: GalynaFedorova
ms.date: 07/30/2021
ms.topic: troubleshooting
ms.search.form: WHSLoadTable_WHSShipConfirm,WHSLoadPlanningListPage_WHSShipConfirm,WHSLoadPlanningWorkbench_WHSShipConfirm,WHSTransportLoad_WHSShipConfirm,WHSShipPlanningListPage_WHSShipConfirm,WHSShipmentDetails_WHSShipConfirm,WHSWorkTable_WHSShipConfirm,WHSWorkTableListPage_WHSShipConfirm,Dialog_WHSOutboundShipConfirmController_WHSOutboundShipConfirm
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: v-gfedorova
ms.search.validFrom: 2021-07-30
ms.dyn365.ops.version: 10.0.21
ms.openlocfilehash: 801778fc8f04b106bf168a3dcd5a89767a837740
ms.sourcegitcommit: b9c2798aa994e1526d1c50726f807e6335885e1a
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 08/13/2021
ms.locfileid: "7344275"
---
# <a name="you-cant-confirm-a-shipment-because-the-customer-is-on-hold"></a>คุณไม่สามารถยืนยันการจัดส่งได้เนื่องจากลูกค้าถูกระงับไว้ชั่วคราว

รหัสระบุข้อผิดพลาด: WAX:CustomerOnHoldShipmentCannotBeConfirmed

## <a name="symptoms"></a>อาการ

เมื่อคุณพยายามยืนยันการจัดส่ง ระบบจะแสดงข้อความแสดงข้อผิดพลาดต่อไปนี้:

> ไม่สามารถยืนยันการจัดส่ง %1 ได้ เนื่องจากลูกค้าถูกระงับสำหรับ %2

ดังนั้นคุณจึงไม่สามารถยืนยันการจัดส่งของสินค้าได้

## <a name="cause"></a>สาเหตุ

บัญชีลูกค้าสำหรับการโหลดหรือจัดส่งสินค้าถูกระงับไว้ชั่วคราว ดังนั้นสถานะของลูกค้าทำให้การยืนยันการจัดส่งสินค้าไม่สำเร็จ

## <a name="resolution"></a>การแก้ปัญหา

ใช้ขั้นตอนต่อไปนี้เพื่อยกเลิกการบล็อคบัญชีลูกค้า

1. ไปที่ **บัญชีลูกหนี้ \> ลูกค้า \> ลูกค้าทั้งหมด**
1. เปิดเข้าบัญชีลูกค้าที่ไม่สามารถยืนยันการจัดส่งได้
1. บนแท็บ **เครดิตและการเรียกเก็บเงิน** ให้ตั้งค่าฟิลด์ **ระงับการออกใบแจ้งหนี้และการจัดส่ง** เป็น *ไม่*
1. ทําขั้นตอนแบบเดียวกันกับลูกค้าทั้งหมดที่ถูกระงับการจัดส่ง
