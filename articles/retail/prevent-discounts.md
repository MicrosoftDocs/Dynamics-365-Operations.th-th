---
title: ตัวเลือกสำหรับการป้องกันไม่ให้มีส่วนลดสำหรับผลิตภัณฑ์ Retail
description: มีเหตุผลต่าง ๆ ว่าเพราะเหตุใดผู้ค้าปลีกอาจต้องการป้องกันไม่ให้ได้รับส่วนลด จากโปรโมชัน หรือ ระหว่างการขายที่ POS
author: jblucher
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: RetailPeriodicDiscount
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 85183
ms.assetid: e8c5a24f-7edd-4fd6-af80-5e0ac9f03127
ms.search.region: Global
ms.search.industry: Retail
ms.author: jeffbl
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: c9d3e7af95dffddfddc34059d93a2a5a350d08e5
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 01/29/2019
ms.locfileid: "346076"
---
# <a name="options-for-preventing-discounts-for-retail-products"></a><span data-ttu-id="dc3be-103">ตัวเลือกสำหรับการป้องกันไม่ให้มีส่วนลดสำหรับผลิตภัณฑ์ Retail</span><span class="sxs-lookup"><span data-stu-id="dc3be-103">Options for preventing discounts for retail products</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="dc3be-104">มีเหตุผลต่าง ๆ ว่าเพราะเหตุใดผู้ค้าปลีกอาจต้องการป้องกันไม่ให้ได้รับส่วนลด จากโปรโมชัน หรือ ระหว่างการขายที่ POS</span><span class="sxs-lookup"><span data-stu-id="dc3be-104">There are various reasons why retailers may want to prevent some products from being discounted, either from a promotion or during the sale at the POS.</span></span>

<span data-ttu-id="dc3be-105">ตัวเลือกต่อไปนี้ ซึ่งสามารถดูได้บนแท็บ **การขายปลีก** ของผลิตภัณฑ์ที่นำออกใช้ จะทำให้สามารถตั้งค่าคอนฟิกผลิตภัณฑ์ให้ป้องกันส่วนลดทั้งหมดหรือที่กำหนดด้วยตนเองได้</span><span class="sxs-lookup"><span data-stu-id="dc3be-105">The following options, which can be found on the **Retail** tab of released products, will allow the product to be configured to prevent all or manual discounts.</span></span> <span data-ttu-id="dc3be-106">คุณสามารถระบุการตั้งค่าได้ที่ระดับประเภทจากลำดับชั้นประเภทการขายปลีก</span><span class="sxs-lookup"><span data-stu-id="dc3be-106">The settings can also be specified at the category level from the retail category hierarchy.</span></span>

- <span data-ttu-id="dc3be-107">**ป้องกันส่วนลดทั้งหมด** – เลือกตัวเลือกนี้เพื่อป้องกันไม่ให้มีการนำส่วนลดทุกประเภททั้งหมดไปใช้กับผลิตภัณฑ์นี้</span><span class="sxs-lookup"><span data-stu-id="dc3be-107">**Prevent all discounts** – Select this option to prevent all types of discounts from being applied to this product.</span></span> <span data-ttu-id="dc3be-108">ซึ่งรวมถึงโปรโมชันต่าง ๆ เช่น การซื้อคละกัน ส่วนลดตามปริมาณและส่วนลดจำกัด รวมทั้งส่วนลดต่อรายการสินค้าที่กำหนดเองและส่วนลดของธุรกรรมที่ใช้ในระหว่างการขายโดยผู้ใช้ POS</span><span class="sxs-lookup"><span data-stu-id="dc3be-108">This includes promotions such as mix and match, quantity and threshold discounts, as well as manual line and transaction discounts that are applied during a sale by a POS user.</span></span>
- <span data-ttu-id="dc3be-109">**ป้องกันส่วนลดที่กำหนดเอง** – เลือกตัวเลือกนี้เพื่อป้องกันเฉพาะส่วนลดต่อรายการสินค้าที่กำหนดเอง หรือส่วนลดของธุรกรรมที่ใช้ในระหว่างการขายโดยผู้ใช้ POS</span><span class="sxs-lookup"><span data-stu-id="dc3be-109">**Prevent manual discounts** – Select this option to only prevent the manual line or transaction discounts that are applied during a sale by a POS user.</span></span> <span data-ttu-id="dc3be-110">ผลิตภัณฑ์ที่มีการเลือกตัวเลือกนี้จะยังคงมีสิทธิ์สำหรับการส่งเสริมการขาย เช่น ส่วนลดสำหรับการซื้อคละกัน และส่วนลดตามปริมาณและส่วนลดจำกัด</span><span class="sxs-lookup"><span data-stu-id="dc3be-110">Products with this option selected are still eligible for promotions, such as mix and match and quantity and threshold discounts.</span></span>

> [!NOTE]
> <span data-ttu-id="dc3be-111">การตั้งค่าเหล่านี้ไม่จำกัดการดำเนินการแทนที่ราคา เนื่องจากจะเป็นการกำหนดราคาพื้นฐานและไม่ถือว่าเป็นส่วนลด</span><span class="sxs-lookup"><span data-stu-id="dc3be-111">These settings do not restrict the price override operation, because that sets the base price and is not treated as a discount.</span></span>

<span data-ttu-id="dc3be-112">[![ฟิลด์ป้องกันไม่ให้มีส่วนลด](./media/prevent-discounts.png)](./media/prevent-discounts.png)</span><span class="sxs-lookup"><span data-stu-id="dc3be-112">[![prevent discounts field](./media/prevent-discounts.png)](./media/prevent-discounts.png)</span></span>
