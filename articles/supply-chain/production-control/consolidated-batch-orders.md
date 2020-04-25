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
ms.search.scope: Core, Operations
ms.custom: 19291
ms.assetid: e97f1d3d-1306-4c42-b2bc-d1755fe574d5
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: shylaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 7e8b017455c0821d97f9039d4ebf00d2dfa28eaa
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 04/02/2020
ms.locfileid: "3211663"
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




