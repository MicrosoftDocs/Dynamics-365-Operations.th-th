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
ms.openlocfilehash: 98011dbf22ff55b7651ce63557fa4a360130b6af
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 01/15/2021
ms.locfileid: "4974771"
---
# <a name="troubleshoot-sales-quotations"></a>การแก้ไขปัญหาใบเสนอราคาขาย

หัวข้อนี้จะอธิบายวิธีการแก้ไขปัญหาที่คุณอาจพบขณะทำงานกับใบเสนอราคาขาย

## <a name="i-cant-change-the-sales-quantity-of-a-sales-quotation-for-a-service-item"></a>ฉันไม่สามารถเปลี่ยนแปลงปริมาณการขายของใบเสนอราคาขายสำหรับสินค้าบริการได้

### <a name="issue-description"></a>คำอธิบายปัญหา

ถ้าคุณพยายามกำหนดปริมาณการขาย (ฟิลด์ **SalesQty**) สำหรับสินค้าของประเภท *การบริการ* ในบรรทัดใบเสนอราคาขาย คุณจะได้รับข้อความแสดงข้อความต่อไปนี้: "ไม่อนุญาตให้ใช้การอัปเดตสำหรับปริมาณของฟิลด์"

### <a name="issue-resolution"></a>การแก้ไขปัญหา

คุณไม่สามารถกำหนดปริมาณการขายสำหรับผลิตภัณฑ์ที่เป็นสินค้าบริการได้ ตัวอย่างเช่น ถ้าคุณมีบริการที่จะติดตั้งสินค้า จะไม่มีการบันทึกปริมาณไว้เนื่องจากไม่มีสินค้าที่มีอยู่จริง มีเพียงบริการเท่านั้น

