---
title: ตั้งค่าบาร์โค้ด
description: บทความนี้อธิบายวิธีการใช้บาร์โค้ดใน Dynamics 365 Commerce
author: jblucher
ms.date: 09/22/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: RetailBarcodeMaskCharacter, RetailBarcodeMaskSetup
audience: Application User
ms.reviewer: josaw
ms.custom: 15971
ms.assetid: 6b4b2ac2-0344-41aa-8818-62c30017d5ac
ms.search.region: global
ms.search.industry: Retail
ms.author: jeffbl
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: 1c395caedfce7efa0a087ff6944052958c72327e
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 03/31/2021
ms.locfileid: "5804196"
---
# <a name="set-up-bar-codes"></a><span data-ttu-id="dce38-103">ตั้งค่าบาร์โค้ด</span><span class="sxs-lookup"><span data-stu-id="dce38-103">Set up bar codes</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="dce38-104">บทความนี้อธิบายวิธีการใช้บาร์โค้ดใน Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="dce38-104">This article describes how to use bar codes in Dynamics 365 Commerce.</span></span>

<span data-ttu-id="dce38-105">คุณสามารถใช้บาร์โค้ดในการซื้อ และขายผลิตภัณฑ์ ติดตามผลิตภัณฑ์ย่อย สร้างลูกค้า และพนักงาน</span><span class="sxs-lookup"><span data-stu-id="dce38-105">You can use bar codes to purchase and sell products, track product variants, and set up customers and employees.</span></span> <span data-ttu-id="dce38-106">คุณยังสามารถใช้บาร์โค้ดเพื่อออก และสลักหลังคูปอง บัตรของขวัญ และใบหักหนี้</span><span class="sxs-lookup"><span data-stu-id="dce38-106">You can also use bar codes to issue and endorse coupons, gift cards, and credit memos.</span></span> <span data-ttu-id="dce38-107">คุณสามารถตั้งค่าผลิตภัณฑ์เพื่อให้มีบาร์โค้ดมาตรฐาน หรือบาร์โค้ดภายในองค์กรที่กำหนดเอง</span><span class="sxs-lookup"><span data-stu-id="dce38-107">You can set up products so that they have standard bar codes or custom, in-house bar codes.</span></span> <span data-ttu-id="dce38-108">ผลิตภัณฑ์สามารถมีได้มากกว่าหนึ่งบาร์โค้ด</span><span class="sxs-lookup"><span data-stu-id="dce38-108">Products can have more than one bar code.</span></span> <span data-ttu-id="dce38-109">ตัวอย่างเช่น ผลิตภัณฑ์อาจมีบาร์โค้ดหลากหลาย หากมาจากผู้ผลิตรายต่าง ๆ หรือ ตัวแปรที่ขึ้นอยู่กับขนาด ลักษณะ หรือสี</span><span class="sxs-lookup"><span data-stu-id="dce38-109">For example, a product might have multiple bar codes if it comes from various manufacturers, or if it has variants that are based on size, style, or color.</span></span> <span data-ttu-id="dce38-110">บาร์โค้ดอาจรวมถึงน้ำหนักหรือราคาของผลิตภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="dce38-110">Bar codes can include the weight or price of the product.</span></span> <span data-ttu-id="dce38-111">บาร์โคดมาสก์ คือแม่แบบที่ใช้สำหรับสร้างบาร์โคด</span><span class="sxs-lookup"><span data-stu-id="dce38-111">Bar code masks are templates that are used to create bar codes.</span></span>

> [!NOTE]
> <span data-ttu-id="dce38-112">หากคุณกำหนดบาร์โค้ดเฉพาะให้กับชุดตัวแปรต่างๆ แต่ละชุด คุณสามารถสแกนบาร์โค้ดที่ทะเบียนและให้โปรแกรมกำหนดว่าตัวแปรใดของผลิตภัณฑ์ที่กำลังจำหน่าย</span><span class="sxs-lookup"><span data-stu-id="dce38-112">If you assign a unique bar code to each variant combination, you can scan the bar code at the register and let the program determine which variant of the product is being sold.</span></span> <span data-ttu-id="dce38-113">นอกจากนี้คุณยังสามารถรวบรวม และดูสถิติเกี่ยวกับการขายด้วยตัวแปร</span><span class="sxs-lookup"><span data-stu-id="dce38-113">You can also collect and view statistics about sales by variant.</span></span> <span data-ttu-id="dce38-114">ขนาด สี และกลุ่มลักษณะต่างๆ สามารถกำหนดหมายเลขเฉพาะที่ระบุถึงกลุ่มดังกล่าวในบาร์โค้ดได้</span><span class="sxs-lookup"><span data-stu-id="dce38-114">Each size, color, and style group can be assigned a unique number that identifies that group in the bar code.</span></span> <span data-ttu-id="dce38-115">Commerce ใช้ตัวพรางบาร์โค้ดเพื่อสร้างบาร์โค้ดโดยอัตโนมัติสำหรับชุดข้อมูลตัวแปรแต่ละชุด</span><span class="sxs-lookup"><span data-stu-id="dce38-115">Commerce uses the bar code mask to automatically generate bar codes for each variant combination.</span></span> <span data-ttu-id="dce38-116">ฟังก์ชันนี้จะเป็นประโยชน์หากผลิตภัณฑ์มีหลายขนาด สี และ ลักษณะ เนื่องจากจำนวนของชุดข้อมูลเพิ่มขึ้นตามรหัสตัวแปรแต่ละตัวแปรที่เพิ่มขึ้น</span><span class="sxs-lookup"><span data-stu-id="dce38-116">This functionality can be useful if there are many sizes, colors, and styles, because the number of combinations increases significantly as each variant code is added.</span></span> <span data-ttu-id="dce38-117">หากฟังก์ชันนี้ใช้งานไม่ได้ จะต้องกำหนดบาร์โค้ดด้วยตนเองให้กับตัวแปรแต่ละตัวที่แสดงถึงผลิตภัณฑ์ย่อย</span><span class="sxs-lookup"><span data-stu-id="dce38-117">If this functionality isn't used, bar codes must be manually assigned to each combination that represents a product variant.</span></span>

<span data-ttu-id="dce38-118">คุณสามารถสร้างบาร์โค้ดได้ด้วยตนเอง หรือใช้โปรแกรมอัตโนมัติก็ได้</span><span class="sxs-lookup"><span data-stu-id="dce38-118">You can create bar codes manually or automatically.</span></span> <span data-ttu-id="dce38-119">การสร้างบาร์โค้ด ให้ทำตามขั้นตอนดังนี้</span><span class="sxs-lookup"><span data-stu-id="dce38-119">To create bar codes, complete the following tasks in the order in which they are listed.</span></span>

1. <span data-ttu-id="dce38-120">[ตั้งค่าตัวอักษรของบาร์โค้ดมาสก์](set-up-bar-code-masks.md).</span><span class="sxs-lookup"><span data-stu-id="dce38-120">[Set up bar code mask characters](set-up-bar-code-masks.md).</span></span>
2. <span data-ttu-id="dce38-121">[ตั้งค่าบาร์โค้ดมาสก์](set-up-bar-code-masks.md)</span><span class="sxs-lookup"><span data-stu-id="dce38-121">[Set up bar code masks](set-up-bar-code-masks.md).</span></span>
3. <span data-ttu-id="dce38-122">ตั้งค่าการตั้งค่าบาร์โค้ด</span><span class="sxs-lookup"><span data-stu-id="dce38-122">Configure bar code setups.</span></span>
4. <span data-ttu-id="dce38-123">[สร้างบาร์โค้ดให้ผลิตภัณฑ์](../supply-chain/pim/tasks/create-bar-code-product.md)</span><span class="sxs-lookup"><span data-stu-id="dce38-123">[Create bar codes for products](../supply-chain/pim/tasks/create-bar-code-product.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="dce38-124">ทรัพยากรเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="dce38-124">Additional resources</span></span>

[<span data-ttu-id="dce38-125">ตั้งค่าบาร์โค้ดมาสก์</span><span class="sxs-lookup"><span data-stu-id="dce38-125">Set up bar code masks</span></span>](set-up-bar-code-masks.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]