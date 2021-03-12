---
title: ใบสั่งชุดงานแบบรวม
description: บทความนี้อธิบายแนวคิดเกี่ยวกับใบสั่งชุดงานแบบรวม
author: ShylaThompson
manager: tfehr
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: PmfAddToConsOrder, PmfBulkItemConv, PmfBulkPackOnHand, PmfConsOrderListPage
audience: Application User
ms.reviewer: kamaybac
ms.custom: 19291
ms.assetid: e97f1d3d-1306-4c42-b2bc-d1755fe574d5
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 2098cb458821146f6d1bf029591493ac745626f1
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 01/15/2021
ms.locfileid: "4966466"
---
# <a name="consolidated-batch-orders"></a>ใบสั่งชุดงานแบบรวม

[!include [banner](../includes/banner.md)]

บทความนี้อธิบายแนวคิดเกี่ยวกับใบสั่งชุดงานแบบรวม

สินค้าจำนวนมากที่ผลิตจะถือว่าเป็นสินค้าหลัก ในขณะที่สินค้ารวบรวมไว้จะถือว่าเป็นสินค้ารอง ความสัมพันธ์ระหว่างสินค้าจำนวนมากและสินค้ารวบรวมไว้จะแสดงในการแปลงสินค้าจำนวนมาก การแปลงสินค้าจำนวนมากนี้ถูกกำหนดด้วยสินค้าจำนวนมากเอง  

นับสินค้าที่บรรจุลงในตู้บรรจุสินค้ามีขนาดเดียวหรือหลายขนาดที่จะถือว่าเป็นหนึ่งหน่วย โดยการรวมบัญชีใบสั่งสำหรับสินค้าจำนวนมาก คุณสามารถดูใบสั่งชุดงานที่เกี่ยวข้องในมุมมองเดียวซึ่งช่วยให้คุณกำหนดงานใด ๆ ที่เหลืออยู่ซึ่งต้องเสร็จสมบูรณ์ทั้งหมด  

ใบสั่งชุดงานแบบรวมสามารถประกอบด้วยชุดข้อมูลของใบสั่งต่อไปนี้:

-   ใบสั่งจำนวนมากหนึ่งใบและใบสั่งรวมหลายใบ
-   ใบสั่งจำนวนมากหลายใบและใบสั่งรวมหลายใบ
-   ใบสั่งจำนวนมากหลายใบและใบสั่งรวมหนึ่งใบ
-   เฉพาะใบสั่งรวม




