---
title: คำถามที่ถามบ่อยเกี่ยวกับใบสั่งขาย
description: หน้านี้ระบุคำถามที่ถามบ่อยซึ่งเกิดขึ้นเมื่อใช้งานใบสั่งขายใน Dynamics 365 Supply Chain Management
author: Henrikan
ms.date: 06/24/2021
ms.topic: troubleshooting
ms.search.form: SalesTable, SalesTableListPage, SalesTableListPage_SalesCancelOrder
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: henrikan
ms.search.validFrom: 2021-06-24
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 3cee75b1d740e7cb414c674157dde0146e8faa50
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 09/29/2021
ms.locfileid: "7571628"
---
# <a name="sales-order-faqs"></a>คำถามที่ถามบ่อยเกี่ยวกับใบสั่งขาย

หน้านี้ระบุคำถามที่ถามบ่อยซึ่งเกิดขึ้นเมื่อใช้งานใบสั่งขายใน Dynamics 365 Supply Chain Management

## <a name="can-i-link-a-purchase-order-to-a-sales-order-to-fulfill-demand"></a>ฉันสามารถเชื่อมโยงใบสั่งซื้อกับใบสั่งขายเพื่อตอบสนองความต้องการได้หรือไม่

คุณสามารถสร้างใบสั่งซื้อจากใบสั่งขาย สำหรับข้อมูลเพิ่มเติม ดูที่ [สร้างใบสั่งซื้อจากใบสั่งขาย](/dynamics365/supply-chain/sales-marketing/tasks/create-purchase-order-sales-order)

## <a name="can-i-cancel-or-delete-a-sales-order-or-return-order"></a>ฉันสามารถยกเลิกหรือลบใบสั่งขายหรือใบสั่งส่งคืนสินค้าได้หรือไม่

คุณสามารถยกเลิกได้เฉพาะใบสั่งขายและใบสั่งส่งคืนสินค้าที่อยู่ในสถานะ *สร้างแล้ว* เท่านั้น สำหรับข้อมูลเพิ่มเติม ให้ดูที่ [ยกเลิกใบสั่งส่งคืน](/dynamics365/supply-chain/service-management/cancel-return-order)

## <a name="can-i-restore-an-invoiced-sales-order-that-was-deleted"></a>ฉันสามารถเรียกคืนใบสั่งขายที่ออกใบแจ้งหนี้แล้วได้หรือไม่

หากใบสั่งขายที่ออกใบแจ้งหนี้แล้วถูกลบออกโดยไม่ได้ตั้งใจ คุณสามารถคืนค่าหรือดูรายละเอียดของใบสั่งขายนั้น

ไปที่ **บัญชีของลูกค้า \> ธุรกรรม \> เอกสารต้นฉบับ \> ดูรายละเอียด** ค้นหาใบแจ้งหนี้ที่คุณกำลังค้นหา และเลือกเพื่อดูรายละเอียดของใบแจ้งหนี้ รายละเอียดเหล่านี้รวมถึงการอ้างอิงใบสั่งขาย นอกจากนี้คุณยังสามารถเข้าถึงรายละเอียดใบสั่งขายจากหน้าดังกล่าวได้ด้วย

## <a name="how-do-i-delete-orphaned-sales-order-records"></a>ฉันจะลบเรกคอร์ดใบสั่งขายที่ไม่ได้ใช้งานอย่างไร

เมื่อต้องการล้างข้อมูลเรกคอร์ดใบสั่งขายที่ไม่ได้ใช้งานอยู่ ให้รันงานประจำงวดของ *การลบใบสั่งขาย* โดยไปที่สถานที่ต่อไปนี้:

- การขายและการตลาด \> งานประจำงวด \> ล้าง \> ลบใบสั่งขาย
- การขายปลีกและการค้า \> การขายปลีก และ COMMERCE IT \> ล้างข้อมูลการ \> ลบใบสั่งขาย

## <a name="is-there-a-way-to-calculate-commissions-on-invoices-that-have-already-been-posted"></a>มีวิธีการคำนวณค่าคอมมิชชันสำหรับใบแจ้งหนี้ที่มีการลงรายการบัญชีแล้วหรือไม่

ปัจจุบัน Supply Chain Management ไม่สนับสนุนการคำนวณค่าคอมมิชชันสำหรับใบแจ้งหนี้ที่ลงรายการบัญชีแล้ว
