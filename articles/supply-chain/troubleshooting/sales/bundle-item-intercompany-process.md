---
title: สินค้าของการขายรวมไม่ได้รับการสนับสนุนในกระบวนการระหว่างบริษัท
description: สินค้าของการขายรวมไม่พร้อมให้ทำการซื้อ ใบสั่งขายซื้อเฉพาะส่วนประกอบของสินค้าของการขายรวมเท่านั้น ไม่ใช่ตัวสินค้าของการขายรวมเอง
author: SmithaNataraj
ms.date: 06/24/2021
ms.topic: troubleshooting
ms.search.form: SalesTable, SalesTableListPage, SalesTableListPage_SalesCancelOrder
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: smnatara
ms.search.validFrom: 2021-06-24
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 21adc7d071837b762157364f6f8ed370c69c7fd3
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 09/07/2021
ms.locfileid: "7477742"
---
# <a name="a-bundle-item-isnt-supported-in-an-intercompany-process"></a>สินค้าของการขายรวมไม่ได้รับการสนับสนุนในกระบวนการระหว่างบริษัท

## <a name="symptoms"></a>อาการ

สินค้าที่มีการขายรวมจะไม่พร้อมใช้งานสำหรับใบสั่งซื้อเนื่องจากถ้าคุณตรวจสอบบรรทัดใบสั่งขายสำหรับสินค้าที่มีการขายรวม คุณจะสังเกตเห็นว่าปริมาณเป็น *0* (ศูนย์) และสถานะคือ *ยกเลิก*

## <a name="resolution"></a>การแก้ปัญหา

ลักษณะการทำงานนี้เกิดจากการออกแบบ ใบสั่งขายจะซื้อเฉพาะส่วนประกอบของสินค้าที่มีการขายรวมเท่านั้น ไม่มีการซื้อสินค้าที่มีการขายรวม ถ้าคุณต้องการซื้อกลุ่มงาน ให้พิจารณาว่าคุณต้องทำเครื่องหมายเป็นสินค้าที่มีการขายรวม เนื่องจากฟังก์ชันนี้ได้รับการออกแบบมาสำหรับสถานการณ์การรับรู้รายได้จริงหรือไม่ สำหรับข้อมูลเพิ่มเติมเกี่ยวกับสินค้าที่มีการขายรวม ให้ดูที่ [การขายรวม](/dynamics365/finance/accounts-receivable/revenue-recognition-setup)
