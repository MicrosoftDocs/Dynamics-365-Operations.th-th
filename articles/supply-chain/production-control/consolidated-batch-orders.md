---
title: ใบสั่งชุดงานแบบรวม
description: บทความนี้อธิบายแนวคิดเกี่ยวกับใบสั่งชุดงานแบบรวม
author: ShylaThompson
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
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
ms.openlocfilehash: e8d7656889b69cfd1dcffb45b52eb649bce59629
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 04/01/2021
ms.locfileid: "5809241"
---
# <a name="consolidated-batch-orders"></a><span data-ttu-id="7274a-103">ใบสั่งชุดงานแบบรวม</span><span class="sxs-lookup"><span data-stu-id="7274a-103">Consolidated batch orders</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="7274a-104">บทความนี้อธิบายแนวคิดเกี่ยวกับใบสั่งชุดงานแบบรวม</span><span class="sxs-lookup"><span data-stu-id="7274a-104">This article describes the concept of consolidated batch orders.</span></span>

<span data-ttu-id="7274a-105">สินค้าจำนวนมากที่ผลิตจะถือว่าเป็นสินค้าหลัก ในขณะที่สินค้ารวบรวมไว้จะถือว่าเป็นสินค้ารอง</span><span class="sxs-lookup"><span data-stu-id="7274a-105">A bulk item that is produced is considered a parent item, whereas a packed item is considered a child item.</span></span> <span data-ttu-id="7274a-106">ความสัมพันธ์ระหว่างสินค้าจำนวนมากและสินค้ารวบรวมไว้จะแสดงในการแปลงสินค้าจำนวนมาก</span><span class="sxs-lookup"><span data-stu-id="7274a-106">The relation between the bulk item and the packed item is expressed in a bulk item conversion.</span></span> <span data-ttu-id="7274a-107">การแปลงสินค้าจำนวนมากนี้ถูกกำหนดด้วยสินค้าจำนวนมากเอง</span><span class="sxs-lookup"><span data-stu-id="7274a-107">This bulk item conversion is defined on the bulk item itself.</span></span>  

<span data-ttu-id="7274a-108">นับสินค้าที่บรรจุลงในตู้บรรจุสินค้ามีขนาดเดียวหรือหลายขนาดที่จะถือว่าเป็นหนึ่งหน่วย</span><span class="sxs-lookup"><span data-stu-id="7274a-108">Packed items can be packaged into containers of either a single size or multiple sizes that are considered one unit.</span></span> <span data-ttu-id="7274a-109">โดยการรวมบัญชีใบสั่งสำหรับสินค้าจำนวนมาก คุณสามารถดูใบสั่งชุดงานที่เกี่ยวข้องในมุมมองเดียวซึ่งช่วยให้คุณกำหนดงานใด ๆ ที่เหลืออยู่ซึ่งต้องเสร็จสมบูรณ์ทั้งหมด</span><span class="sxs-lookup"><span data-stu-id="7274a-109">By consolidating the orders for a bulk item, you can see all the related batch orders in a single view that can help you determine any remaining work that must be completed.</span></span>  

<span data-ttu-id="7274a-110">ใบสั่งชุดงานแบบรวมสามารถประกอบด้วยชุดข้อมูลของใบสั่งต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="7274a-110">A consolidated batch order can contain any combination of the following orders:</span></span>

-   <span data-ttu-id="7274a-111">ใบสั่งจำนวนมากหนึ่งใบและใบสั่งรวมหลายใบ</span><span class="sxs-lookup"><span data-stu-id="7274a-111">A single bulk order and multiple packed orders</span></span>
-   <span data-ttu-id="7274a-112">ใบสั่งจำนวนมากหลายใบและใบสั่งรวมหลายใบ</span><span class="sxs-lookup"><span data-stu-id="7274a-112">Multiple bulk orders and multiple packed orders</span></span>
-   <span data-ttu-id="7274a-113">ใบสั่งจำนวนมากหลายใบและใบสั่งรวมหนึ่งใบ</span><span class="sxs-lookup"><span data-stu-id="7274a-113">Multiple bulk orders and a single packed order</span></span>
-   <span data-ttu-id="7274a-114">เฉพาะใบสั่งรวม</span><span class="sxs-lookup"><span data-stu-id="7274a-114">Only packed orders</span></span>






[!INCLUDE[footer-include](../../includes/footer-banner.md)]