---
title: งานอัพเดตใบรับสินค้าจะยืนยันใบสั่งที่ยังไม่ได้ยืนยัน
description: หลังจากการรัน อัพเดตใบรับสินค้า ระบบจะยืนยันใบสั่งที่ยังไม่ได้ยืนยันที่มีสถานะเป็น ลงทะเบียนแล้ว เรียนรู้เกี่ยวกับคุณลักษณะที่แก้ไขปัญหานี้
author: perlynne
ms.date: 06/24/2021
ms.topic: troubleshooting
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2021-06-24
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 171a978efc6b55b92f429381e72036cb1b3296c6
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 09/07/2021
ms.locfileid: "7477705"
---
# <a name="unconfirmed-purchase-orders-are-confirmed-after-running-update-product-receipts"></a>ใบสั่งซื้อที่ยังไม่ได้ยืนยันจะได้รับการยืนยัน หลังจากการรัน อัพเดตใบรับสินค้า

## <a name="symptoms"></a>อาการ

หลังจากที่คุณเรียกใช้งานประจำงวด *อัปเดตใบรับสินค้า* ระบบจะยืนยันใบสั่งซื้อที่ยังไม่ได้ยืนยันที่มีสถานะธุรกรรมสินค้าคงคลังที่ *ลงทะเบียน* ไว้โดยอัตโนมัติ

## <a name="resolution"></a>การแก้ปัญหา

ลักษณะการทำงานในการจัดการโหลดขาเข้าใหม่ *ผ่านการรับสินค้าในปริมาณการโหลด* ให้แก้ไขปัญหานี้ เมื่อต้องการเปิดคุณลักษณะนี้ ไปที่พื้นที่ทำงาน [การจัดการคุณลักษณะ](/dynamics365/fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview) และเปิดใช้งานคุณลักษณะต่อไปนี้เพื่อให้แสดงในรายการ:

1. เชื่อมโยงธุรกรรมสินค้าคงคลังของใบสั่งซื้อกับการบรรทุก
2. การรับเกินปริมาณของการบรรทุก

สำหรับข้อมูลเพิ่มเติม ให้ดูที่ [ลงรายการบัญชีปริมาณผลิตภัณฑ์ที่ลงทะเบียนสำหรับใบสั่งซื้อ](/dynamics365/supply-chain/warehousing/inbound-load-handling)
