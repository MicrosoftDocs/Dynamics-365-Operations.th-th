---
title: "การสร้างบาร์โค้ด"
description: "บทความนี้อธิบายวิธีใช้บาร์โค้ดใน Microsoft Dynamics 365 for Retail"
author: jblucher
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 15971
ms.assetid: 6b4b2ac2-0344-41aa-8818-62c30017d5ac
ms.search.region: global
ms.search.industry: Retail
ms.author: jeffbl
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: bfb47e653cc3ef36135fd7c4f60771a354699af7
ms.contentlocale: th-th
ms.lasthandoff: 11/03/2017

---

# <a name="set-up-bar-codes"></a><span data-ttu-id="db2c3-103">ตั้งค่าบาร์โค้ด</span><span class="sxs-lookup"><span data-stu-id="db2c3-103">Set up bar codes</span></span>

[!include[banner](includes/banner.md)]


<span data-ttu-id="db2c3-104">บทความนี้อธิบายวิธีใช้บาร์โค้ดใน Microsoft Dynamics 365 for Retail</span><span class="sxs-lookup"><span data-stu-id="db2c3-104">This article describes how to use bar codes in Microsoft Dynamics 365 for Retail.</span></span>

<span data-ttu-id="db2c3-105">คุณสามารถใช้บาร์โค้ดในการซื้อ และขายผลิตภัณฑ์ ติดตามผลิตภัณฑ์ย่อย สร้างลูกค้า และพนักงาน</span><span class="sxs-lookup"><span data-stu-id="db2c3-105">You can use bar codes to purchase and sell products, track product variants, and set up customers and employees.</span></span> <span data-ttu-id="db2c3-106">คุณยังสามารถใช้บาร์โค้ดเพื่อออก และสลักหลังคูปอง บัตรของขวัญ และใบหักหนี้</span><span class="sxs-lookup"><span data-stu-id="db2c3-106">You can also use bar codes to issue and endorse coupons, gift cards, and credit memos.</span></span> <span data-ttu-id="db2c3-107">คุณสามารถตั้งค่าผลิตภัณฑ์ขายปลีกเพื่อให้มีบาร์โค้ดมาตรฐาน หรือบาร์โค้ดภายในองค์กรที่กำหนดเอง</span><span class="sxs-lookup"><span data-stu-id="db2c3-107">You can set up retail products so that they have standard bar codes or custom, in-house bar codes.</span></span> <span data-ttu-id="db2c3-108">ผลิตภัณฑ์สามารถมีได้มากกว่าหนึ่งบาร์โค้ด</span><span class="sxs-lookup"><span data-stu-id="db2c3-108">Products can have more than one bar code.</span></span> <span data-ttu-id="db2c3-109">ตัวอย่างเช่น ผลิตภัณฑ์อาจมีบาร์โค้ดหลากหลาย หากมาจากผู้ผลิตรายต่าง ๆ หรือ ตัวแปรที่ขึ้นอยู่กับขนาด ลักษณะ หรือสี</span><span class="sxs-lookup"><span data-stu-id="db2c3-109">For example, a product might have multiple bar codes if it comes from various manufacturers, or if it has variants that are based on size, style, or color.</span></span> <span data-ttu-id="db2c3-110">บาร์โค้ดอาจรวมถึงน้ำหนักหรือราคาของผลิตภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="db2c3-110">Bar codes can include the weight or price of the product.</span></span> <span data-ttu-id="db2c3-111">บาร์โคดมาสก์ คือแม่แบบที่ใช้สำหรับสร้างบาร์โคด</span><span class="sxs-lookup"><span data-stu-id="db2c3-111">Bar code masks are templates that are used to create bar codes.</span></span> <span data-ttu-id="db2c3-112">**หมายเหตุ:** หากคุณกำหนดบาร์โค้ดให้กับตัวแปรต่างๆ คุณสามารถสแกนบาร์โค้ดที่ข้อมูลทะเบียนและให้โปรแกรมตรวจสอบตัวแปรใดของผลิตภัณฑ์ที่จำหน่ายได้</span><span class="sxs-lookup"><span data-stu-id="db2c3-112">**Note:** If you assign a unique bar code to each variant combination, you can scan the bar code at the register and let the program determine which variant of the product is being sold.</span></span> <span data-ttu-id="db2c3-113">นอกจากนี้คุณยังสามารถรวบรวม และดูสถิติเกี่ยวกับการขายด้วยตัวแปร</span><span class="sxs-lookup"><span data-stu-id="db2c3-113">You can also collect and view statistics about sales by variant.</span></span> <span data-ttu-id="db2c3-114">ขนาด สี และกลุ่มลักษณะต่างๆ สามารถกำหนดหมายเลขเฉพาะที่ระบุถึงกลุ่มดังกล่าวในบาร์โค้ดได้</span><span class="sxs-lookup"><span data-stu-id="db2c3-114">Each size, color, and style group can be assigned a unique number that identifies that group in the bar code.</span></span> <span data-ttu-id="db2c3-115">Dynamics 365 for Retail ใช้บาร์โค้ดมาสก์สร้างบาร์โค้ดสำหรับชุดข้อมูลตัวแปรแต่ละรายการโดยอัตโนมัติ</span><span class="sxs-lookup"><span data-stu-id="db2c3-115">Dynamics 365 for Retail uses the bar code mask to automatically generate bar codes for each variant combination.</span></span> <span data-ttu-id="db2c3-116">ฟังก์ชันนี้จะเป็นประโยชน์หากผลิตภัณฑ์มีหลายขนาด สี และ ลักษณะ เนื่องจากจำนวนของชุดข้อมูลเพิ่มขึ้นตามรหัสตัวแปรแต่ละตัวแปรที่เพิ่มขึ้น</span><span class="sxs-lookup"><span data-stu-id="db2c3-116">This functionality can be useful if there are many sizes, colors, and styles, because the number of combinations increases significantly as each variant code is added.</span></span> <span data-ttu-id="db2c3-117">หากฟังก์ชันนี้ใช้งานไม่ได้ จะต้องกำหนดบาร์โค้ดด้วยตนเองให้กับตัวแปรแต่ละตัวที่แสดงถึงผลิตภัณฑ์ย่อย</span><span class="sxs-lookup"><span data-stu-id="db2c3-117">If this functionality isn't used, bar codes must be manually assigned to each combination that represents a product variant.</span></span> <span data-ttu-id="db2c3-118">คุณสามารถสร้างบาร์โค้ดได้ด้วยตนเอง หรือใช้โปรแกรมอัตโนมัติก็ได้</span><span class="sxs-lookup"><span data-stu-id="db2c3-118">You can create bar codes manually or automatically.</span></span> <span data-ttu-id="db2c3-119">การสร้างบาร์โค้ด ให้ทำตามขั้นตอนดังนี้</span><span class="sxs-lookup"><span data-stu-id="db2c3-119">To create bar codes, complete the following tasks in the order in which they are listed.</span></span>

1.  <span data-ttu-id="db2c3-120">[ตั้งค่าตัวอักษรของบาร์โค้ดมาสก์](set-up-bar-code-masks.md).</span><span class="sxs-lookup"><span data-stu-id="db2c3-120">[Set up bar code mask characters](set-up-bar-code-masks.md).</span></span>
2.  <span data-ttu-id="db2c3-121">[ตั้งค่าบาร์โค้ดมาสก์](set-up-bar-code-masks.md)</span><span class="sxs-lookup"><span data-stu-id="db2c3-121">[Set up bar code masks](set-up-bar-code-masks.md).</span></span>
3.  <span data-ttu-id="db2c3-122">ตั้งค่าการตั้งค่าบาร์โค้ด</span><span class="sxs-lookup"><span data-stu-id="db2c3-122">Configure bar code setups.</span></span>
4.  <span data-ttu-id="db2c3-123">สร้างบาร์โค้ดให้ผลิตภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="db2c3-123">Create bar codes for products.</span></span>


<a name="see-also"></a><span data-ttu-id="db2c3-124">ดูเพิ่มเติมที่</span><span class="sxs-lookup"><span data-stu-id="db2c3-124">See also</span></span>
--------

[<span data-ttu-id="db2c3-125">ตั้งค่าบาร์โค้ดมาสก์</span><span class="sxs-lookup"><span data-stu-id="db2c3-125">Set up bar code masks</span></span>](set-up-bar-code-masks.md)




