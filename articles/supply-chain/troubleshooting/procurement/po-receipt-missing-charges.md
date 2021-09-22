---
title: ใบรับสินค้าตามใบสั่งซื้อไม่รวมค่าธรรมเนียมทั้งหมด
description: ใบรับสินค้าตามใบสั่งซื้อไม่รวมค่าธรรมเนียมทั้งหมด
author: kamaybac
ms.date: 05/31/2021
ms.topic: troubleshooting
ms.search.form: PurchTable, PurchTablePart, PurchRFQTable
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: yanansong
ms.search.validFrom: 2021-05-31
ms.dyn365.ops.version: 10.0.13
ms.openlocfilehash: bb567e00ef52269db0dc866148a37c73f0a9827c
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 09/07/2021
ms.locfileid: "7477698"
---
# <a name="a-purchase-order-receipt-doesnt-include-all-charges"></a>ใบรับสินค้าตามใบสั่งซื้อไม่รวมค่าธรรมเนียมทั้งหมด

## <a name="symptoms"></a>อาการ

เมื่อคุณได้รับใบสั่งซื้อ ไม่ใช่ค่าธรรมเนียมทั้งหมดจะรวมอยู่ในใบเสร็จ

### <a name="reproduce-the-issue"></a>สร้างปัญหาอีกครั้ง

กระบวนการต่อไปนี้แสดงวิธีหนึ่งที่จะสร้างปัญหาอีกครั้ง

1. บนหน้า **พารามิเตอร์การจัดซื้อและการจัดหา** บนแท็บ **การจัดส่ง** โปรดตรวจสอบให้แน่ใจว่าได้ตั้งค่าตัวเลือก **การสร้างค่าธรรมเนียมบนใบรับสินค้า** เป็น *ใช่*
1. สร้างใบสั่งซื้อที่มีค่าธรรมเนียม
1. ยืนยันใบสั่งซื้อ
1. รับใบสั่งซื้อ
1. ดูยอดรวมการรับสินค้าและเปรียบเทียบกับผลรวมที่คาดไว้
1. โปรดสังเกตว่าค่าธรรมเนียมทั้งหมดจะรวมอยู่ในใบรับสินค้าตามใบสั่งซื้อ

## <a name="resolution"></a>การแก้ปัญหา

การแก้ไขขึ้นอยู่กับวิธีการตั้งค่าค่าธรรมเนียมเบ็ดเตล็ด สำหรับข้อมูลเกี่ยวกับวิธีการตั้งค่าค่าธรรมเนียมเบ็ดเตล็ดเพื่อให้ตรงกับความต้องการของคุณ โปรดดูที่ประกาศบล็อกต่อไปนี้:  [ลงรายการบัญชีค่าธรรมเนียมเบ็ดเตล็ดในเวลาของใบรับสินค้า](https://cloudblogs.microsoft.com/dynamics365/no-audience/2014/11/11/post-misc-charges-at-time-of-product-receipt/)
