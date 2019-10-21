---
title: ส่งคืนสินค้าสำหรับใบสั่งและใบแจ้งหนี้ของลูกค้าหลายใบ
description: หัวข้อนี้อธิบายถึงฟังก์ชันที่จะช่วยให้สามารถส่งคืนสินค้าสำหรับใบสั่งและใบแจ้งหนี้ของลูกค้าหลายใบใน Dynamics 365 Retail
author: josaw1
manager: AnnBe
ms.date: 03/05/2019
ms.topic: index-page
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: ''
ms.assetid: ed0f77f7-3609-4330-bebd-ca3134575216
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2019-01-15
ms.dyn365.ops.version: 10
ms.openlocfilehash: 25a1081e5f903076e23089c41dda7437f8a70124
ms.sourcegitcommit: f87de0f949b5d60993b19e0f61297f02d42b5bef
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 09/24/2019
ms.locfileid: "2018000"
---
# <a name="return-items-across-multiple-customer-orders-and-invoices"></a>ส่งคืนสินค้าสำหรับใบสั่งและใบแจ้งหนี้ของลูกค้าหลายใบ

[!include [banner](includes/banner.md)]


การส่งคืนสินค้าสามารถดำเนินการกับใบสั่งและใบแจ้งหนี้ของลูกค้าหลายใบ 

## <a name="configure-retail-to-support-returns-across-multiple-customer-order-and-invoices"></a>ตั้งค่าคอนฟิก Retail ให้รองรับการส่งคืนสินค้าสำหรับใบสั่งและใบแจ้งหนี้ของลูกค้าหลายใบ

1. ไปที่ **พารามิเตอร์ Retail \> ใบสั่งของลูกค้า**
1. เปิดพารามิเตอร์ **เปิดใช้งานการส่งคืนสำหรับใบสั่งหลายใบ** 

## <a name="process-returns"></a>ดำเนินการส่งคืนสินค้า

หลังจากเปิดพารามิเตอร์และทำข้อมูลการเปลี่ยนแปลงให้ตรงกับร้านค้า แคชเชียร์ในร้านค้าสามารถเลือกใบสั่งขายหลายใบของลูกค้าสำหรับการส่งคืนสินค้าของพวกเขา

เมื่อเลือกใบสั่งแล้ว รายการของผลิตภัณฑ์ที่สามารถส่งคืนทั้งหมดในใบแจ้งหนี้ทั้งหมดสำหรับใบสั่งนั้นจะปรากฏขึ้น แคชเชียร์สามารถเลือกผลิตภัณฑ์ที่จะส่งคืนได้ โดยจะมีการสร้างใบสั่งส่งคืนสินค้าใบเดียวสำหรับผลิตภัณฑ์ที่เลือกทั้งหมด
