---
title: การแก้ไขปัญหาใบเสนอราคาขาย
description: หัวข้อนี้จะอธิบายวิธีการแก้ไขปัญหาที่คุณอาจพบขณะทำงานกับใบเสนอราคาขาย
author: SmithaNataraj
ms.date: 09/16/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: SalesQuotationTable, SalesQuotationTableListPage
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: smnatara
ms.search.validFrom: 2020-9-16
ms.dyn365.ops.version: Release 10.0.14
ms.openlocfilehash: 09529ba729170be7281e2ae04008d3ba4a58e060
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 04/01/2021
ms.locfileid: "5824761"
---
# <a name="troubleshoot-sales-quotations"></a>การแก้ไขปัญหาใบเสนอราคาขาย

หัวข้อนี้จะอธิบายวิธีการแก้ไขปัญหาที่คุณอาจพบขณะทำงานกับใบเสนอราคาขาย

## <a name="i-cant-change-the-sales-quantity-of-a-sales-quotation-for-a-service-item"></a>ฉันไม่สามารถเปลี่ยนแปลงปริมาณการขายของใบเสนอราคาขายสำหรับสินค้าบริการได้

### <a name="issue-description"></a>คำอธิบายปัญหา

ถ้าคุณพยายามกำหนดปริมาณการขาย (ฟิลด์ **SalesQty**) สำหรับสินค้าของประเภท *การบริการ* ในบรรทัดใบเสนอราคาขาย คุณจะได้รับข้อความแสดงข้อความต่อไปนี้: "ไม่อนุญาตให้ใช้การอัปเดตสำหรับปริมาณของฟิลด์"

### <a name="issue-resolution"></a>การแก้ไขปัญหา

คุณไม่สามารถกำหนดปริมาณการขายสำหรับผลิตภัณฑ์ที่เป็นสินค้าบริการได้ ตัวอย่างเช่น ถ้าคุณมีบริการที่จะติดตั้งสินค้า จะไม่มีการบันทึกปริมาณไว้เนื่องจากไม่มีสินค้าที่มีอยู่จริง มีเพียงบริการเท่านั้น



[!INCLUDE[footer-include](../../includes/footer-banner.md)]