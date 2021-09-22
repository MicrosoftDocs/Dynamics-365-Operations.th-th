---
title: ไม่สามารถตั้งค่าปริมาณสินค้าบริการในรายการของใบเสนอราคาขาย
description: เมื่อใช้งานใบเสนอราคาขาย คุณไม่สามารถตั้งค่าปริมาณการขายสำหรับผลิตภัณฑ์ที่เป็นสินค้าบริการ เนื่องจากไม่มีสินค้าที่มีอยู่จริงที่จะตรวจนับ
author: SmithaNataraj
ms.date: 06/24/2021
ms.topic: troubleshooting
ms.search.form: SalesQuotationTable, SalesQuotationTableListPage
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: smnatara
ms.search.validFrom: 2021-06-24
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: ea0f8f246e95f90b6ac5e78ee63950c9ca836a0e
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 09/07/2021
ms.locfileid: "7477781"
---
# <a name="cant-change-the-sales-quantity-of-a-service-item-on-a-sales-quotation-line"></a>ไม่สามารถเปลี่ยนแปลงปริมาณการขายของสินค้าบริการในรายการใบเสนอราคาขายได้

## <a name="symptoms"></a>อาการ

ถ้าคุณพยายามกำหนดปริมาณการขาย (ฟิลด์ **SalesQty**) สำหรับสินค้าของชนิด *บริการ* ในรายการใบเสนอราคาขาย คุณจะได้รับข้อความต่อไปนี้:

> ไม่อนุญาตให้อัพเดตฟิลด์ ปริมาณ

## <a name="cause"></a>สาเหตุ

นี่เกิดจากการออกแบบ คุณไม่สามารถกำหนดปริมาณการขายสำหรับผลิตภัณฑ์ที่เป็นสินค้าบริการได้ ตัวอย่างเช่น ถ้าคุณเสนอบริการในการติดตั้งสินค้า ไม่ควรบันทึกปริมาณไว้เนื่องจากไม่มีสินค้าที่มีอยู่จริงที่จะตรวจนับ มีเพียงบริการเท่านั้น
