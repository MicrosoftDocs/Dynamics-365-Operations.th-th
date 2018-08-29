---
title: "ตัวเลือกสำหรับการป้องกันไม่ให้มีส่วนลดสำหรับผลิตภัณฑ์ Retail"
description: "มีเหตุผลต่าง ๆ ว่าเพราะเหตุใดผู้ค้าปลีกอาจต้องการป้องกันไม่ให้ได้รับส่วนลด จากโปรโมชัน หรือ ระหว่างการขายที่ POS"
author: jblucher
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
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
ms.translationtype: HT
ms.sourcegitcommit: 5098fb3339403b6f2779dfe3bb7ef5c4ca78051f
ms.openlocfilehash: eaee79e2a20ab443cf3779e8499bf29d63ad3dfc
ms.contentlocale: th-th
ms.lasthandoff: 08/29/2018

---

# <a name="options-for-preventing-discounts-for-retail-products"></a><span data-ttu-id="1916f-103">ตัวเลือกสำหรับการป้องกันไม่ให้มีส่วนลดสำหรับผลิตภัณฑ์ Retail</span><span class="sxs-lookup"><span data-stu-id="1916f-103">Options for preventing discounts for retail products</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="1916f-104">มีเหตุผลต่าง ๆ ว่าเพราะเหตุใดผู้ค้าปลีกอาจต้องการป้องกันไม่ให้ได้รับส่วนลด จากโปรโมชัน หรือ ระหว่างการขายที่ POS</span><span class="sxs-lookup"><span data-stu-id="1916f-104">There are various reasons why retailers may want to prevent some products from being discounted, either from a promotion or during the sale at the POS.</span></span>

<span data-ttu-id="1916f-105">ตัวเลือกต่อไปนี้ ซึ่งสามารถดูได้บนแท็บ **การขายปลีก** ของผลิตภัณฑ์ที่นำออกใช้ จะทำให้สามารถตั้งค่าคอนฟิกผลิตภัณฑ์ให้ป้องกันส่วนลดทั้งหมดหรือที่กำหนดด้วยตนเองได้</span><span class="sxs-lookup"><span data-stu-id="1916f-105">The following options, which can be found on the **Retail** tab of released products, will allow the product to be configured to prevent all or manual discounts.</span></span> <span data-ttu-id="1916f-106">คุณสามารถระบุการตั้งค่าได้ที่ระดับประเภทจากลำดับชั้นประเภทการขายปลีก</span><span class="sxs-lookup"><span data-stu-id="1916f-106">The settings can also be specified at the category level from the retail category hierarchy.</span></span>

<span data-ttu-id="1916f-107">**ป้องกันไม่ให้มีส่วนลดทั้งหมด**: เลือกตัวเลือกนี้เพื่อป้องกันไม่ให้มีการนำส่วนลดทุกประเภททั้งหมดไปใช้กับผลิตภัณฑ์นี้</span><span class="sxs-lookup"><span data-stu-id="1916f-107">**Prevent all discounts**: Select this option to prevent all types of discounts from being applied to this product.</span></span> <span data-ttu-id="1916f-108">ซึ่งรวมถึงโปรโมชันต่าง ๆ เช่น การซื้อคละกัน ส่วนลดตามปริมาณและส่วนลดจำกัด รวมทั้งส่วนลดต่อรายการสินค้าที่กำหนดเองและส่วนลดของธุรกรรมที่ใช้ในระหว่างการขายโดยผู้ใช้ POS</span><span class="sxs-lookup"><span data-stu-id="1916f-108">This includes promotions such as mix and match, quantity and threshold discounts, as well as manual line and transaction discounts that are applied during a sale by a POS user.</span></span>

<span data-ttu-id="1916f-109">**ป้องกันไม่ให้มีส่วนลดที่กำหนดเอง**: เลือกตัวเลือกนี้เพื่อป้องกันไม่ให้มีส่วนลดต่อรายการสินค้าที่กำหนดเองหรือส่วนลดของธุรกรรมที่ใช้ในระหว่างการขายโดยผู้ใช้ POS เท่านั้น</span><span class="sxs-lookup"><span data-stu-id="1916f-109">**Prevent manual discounts**: Select this option to only prevent the manual line or transaction discounts that are applied during a sale by a POS user.</span></span> <span data-ttu-id="1916f-110">ผลิตภัณฑ์ที่มีการเลือกตัวเลือกนี้จะยังคงมีสิทธิ์สำหรับการส่งเสริมการขาย เช่น ส่วนลดสำหรับการซื้อคละกัน และส่วนลดตามปริมาณและส่วนลดจำกัด</span><span class="sxs-lookup"><span data-stu-id="1916f-110">Products with this option selected are still eligible for promotions, such as mix and match and quantity and threshold discounts.</span></span>

<span data-ttu-id="1916f-111">**หมายเหตุ**: การตั้งค่าเหล่านี้ไม่จำกัดการดำเนินการแทนที่ราคา เนื่องจากจะเป็นการกำหนดราคาพื้นฐานและไม่ถือว่าเป็นส่วนลด</span><span class="sxs-lookup"><span data-stu-id="1916f-111">**Note**: These settings do not restrict the price override operation, because that sets the base price and is not treated as a discount.</span></span>  

<span data-ttu-id="1916f-112">[![ฟิลด์ป้องกันไม่ให้มีส่วนลด](./media/prevent discounts.png)](./media/prevent discounts.png)</span><span class="sxs-lookup"><span data-stu-id="1916f-112">[![prevent discounts field](./media/prevent discounts.png)](./media/prevent discounts.png)</span></span>

