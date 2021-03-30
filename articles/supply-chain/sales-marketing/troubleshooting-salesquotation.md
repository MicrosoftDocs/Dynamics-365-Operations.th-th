---
title: การแก้ไขปัญหาใบเสนอราคาขาย
description: หัวข้อนี้จะอธิบายวิธีการแก้ไขปัญหาที่คุณอาจพบขณะทำงานกับใบเสนอราคาขาย
author: SmithaNataraj
manager: tfehr
ms.date: 09/16/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
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
ms.openlocfilehash: 9a9cc821d2fe9accad1dae210271682cdd2ce4ba
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 02/15/2021
ms.locfileid: "5232217"
---
# <a name="troubleshoot-sales-quotations"></a>การแก้ไขปัญหาใบเสนอราคาขาย

หัวข้อนี้จะอธิบายวิธีการแก้ไขปัญหาที่คุณอาจพบขณะทำงานกับใบเสนอราคาขาย

## <a name="i-cant-change-the-sales-quantity-of-a-sales-quotation-for-a-service-item"></a>ฉันไม่สามารถเปลี่ยนแปลงปริมาณการขายของใบเสนอราคาขายสำหรับสินค้าบริการได้

### <a name="issue-description"></a>คำอธิบายปัญหา

ถ้าคุณพยายามกำหนดปริมาณการขาย (ฟิลด์ **SalesQty**) สำหรับสินค้าของประเภท *การบริการ* ในบรรทัดใบเสนอราคาขาย คุณจะได้รับข้อความแสดงข้อความต่อไปนี้: "ไม่อนุญาตให้ใช้การอัปเดตสำหรับปริมาณของฟิลด์"

### <a name="issue-resolution"></a>การแก้ไขปัญหา

คุณไม่สามารถกำหนดปริมาณการขายสำหรับผลิตภัณฑ์ที่เป็นสินค้าบริการได้ ตัวอย่างเช่น ถ้าคุณมีบริการที่จะติดตั้งสินค้า จะไม่มีการบันทึกปริมาณไว้เนื่องจากไม่มีสินค้าที่มีอยู่จริง มีเพียงบริการเท่านั้น



[!INCLUDE[footer-include](../../includes/footer-banner.md)]