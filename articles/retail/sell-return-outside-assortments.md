---
title: "ขายและส่งคืนผลิตภัณฑ์นอกการจัดประเภท"
description: "ด้วย Dynamics 365 for Retail คุณสามารถขายสินค้าและส่งคืนผลิตภัณฑ์ภายนอกการจัดประเภท"
author: pdp1207
manager: AnnBe
ms.date: 05/24/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
ms.search.form: RetailAssortmentDetails
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 
ms.search.region: Global
ms.search.industry: retail
ms.author: prabhup
ms.search.validFrom: 2017-06-30
ms.dyn365.ops.version: July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: 0903879f7fa11c80e695dcb095ce1020984addf6
ms.contentlocale: th-th
ms.lasthandoff: 05/08/2018

---

# <a name="sell-and-return-products-outside-of-an-assortment"></a><span data-ttu-id="e342f-103">ขายและส่งคืนผลิตภัณฑ์นอกการจัดประเภท</span><span class="sxs-lookup"><span data-stu-id="e342f-103">Sell and return products outside of an assortment</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="e342f-104">สถานการณ์ทั่วไปสำหรับผู้ค้าปลีกใด ๆ คือ ในการขายผลิตภัณฑ์ให้ลูกค้าหรือยอมรับสินค้าที่ส่งคืนจากลูกค้าถึงแม้ว่าจะไม่มีผลิตภัณฑ์ที่ระบุในร้านค้า (กล่าวคือ ผลิตภัณฑ์จะไม่จัดประเภทลงในร้านค้า)</span><span class="sxs-lookup"><span data-stu-id="e342f-104">A common scenario for any retailer is to sell products to their customers or accept returns from their customers even if they don’t carry the specific products in their store (in other words, the products are not assorted to the store).</span></span>
<span data-ttu-id="e342f-105">ต่อไปนี้เป็นสถานการณ์ทั่วไปบางส่วน:</span><span class="sxs-lookup"><span data-stu-id="e342f-105">Here are some typical scenarios:</span></span>

+ <span data-ttu-id="e342f-106">ผู้ค้าปลีกไม่มีผลิตภัณฑ์ของบริษัททั้งหมดในร้านค้าเฉพาะ</span><span class="sxs-lookup"><span data-stu-id="e342f-106">A retailer doesn’t carry all its products in a specific store.</span></span> <span data-ttu-id="e342f-107">ผลิตภัณฑ์ที่เหลือจะถูกเก็บในคลังสินค้า</span><span class="sxs-lookup"><span data-stu-id="e342f-107">The remaining products are stored in the warehouse.</span></span> <span data-ttu-id="e342f-108">พนักงานขายประจำร้านสามารถช่วยลูกค้าโดยการค้นหาหรือเรียกดูผลิตภัณฑ์ในคลังสินค้า เพิ่มสินค้าลงในรถเข็น และทำการเช็คเอาท์โดยการเลือกวิธีการจัดส่ง เช่น จัดส่งสินค้าไปยังที่อยู่จากคลังสินค้า หรือการแจ้งให้ลูกค้าที่รับผลิตภัณฑ์จากร้านค้าปัจจุบัน หรือจากร้านค้าอื่น</span><span class="sxs-lookup"><span data-stu-id="e342f-108">The store associate can assist the customer by searching or browsing for the products in the warehouse, add them to the cart, and complete the checkout by selecting a delivery method, such as shipping to an address from the warehouse or letting the customer pick up the product from the current store or from another store.</span></span>
+ <span data-ttu-id="e342f-109">ผู้ค้าปลีกไม่มีผลิตภัณฑ์เฉพาะในร้านค้า หรือไม่มีในสินค้าคงคลังที่ร้านที่ลูกค้าเยี่ยมชม แต่ผลิตภัณฑ์มีอยู่ในร้านค้าอื่น ๆ</span><span class="sxs-lookup"><span data-stu-id="e342f-109">A retailer doesn’t carry specific products in the store or doesn’t have them in stock at the store the customer visited, but the products are available in other stores.</span></span> <span data-ttu-id="e342f-110">พนักงานขายประจำร้านสามารถช่วยลูกค้าโดยการค้นหา หรือเรียกดูผลิตภัณฑ์ในร้านค้าอื่น ๆ เพิ่มสินค้าลงในรถเข็น และเช็คเอาท์ให้เสร็จสมบูรณ์โดยการเลือกวิธีการจัดส่งสินค้า</span><span class="sxs-lookup"><span data-stu-id="e342f-110">The store associate can assist the customer by searching or browsing the products in the other store, add them to the cart, and complete the checkout by selecting a delivery method.</span></span>
+ <span data-ttu-id="e342f-111">ผู้ค้าปลีกมีร้านค้าหลายร้านในและรอบเมืองหรือรหัสไปรษณีย์ และไม่ต้องการบังคับให้ลูกค้าที่ส่งคืนผลิตภัณฑ์ไปยังร้านเดิมที่ซื้อสินค้า</span><span class="sxs-lookup"><span data-stu-id="e342f-111">A retailer has many stores in and around a specific city or zip code and doesn’t want to force the customers to return products to the same store they were purchased in.</span></span> <span data-ttu-id="e342f-112">แทนที่จะทำเช่นนั้น ลูกค้าอาจส่งคืนผลิตภัณฑ์ไปยังร้านค้าใดๆก็ได้</span><span class="sxs-lookup"><span data-stu-id="e342f-112">Instead, customers can return products to any store.</span></span>


<span data-ttu-id="e342f-113">สถานการณ์เหล่านั้นจะพร้อมใช้งานสำหรับผู้ค้าปลีกโดยการใช้ Dynamics 365 for Retail</span><span class="sxs-lookup"><span data-stu-id="e342f-113">Those common scenarios are available for retailers using Dynamics 365 for Retail.</span></span> <span data-ttu-id="e342f-114">ด้วยการค้าปลีก คุณสามารถทำงานกับสิ่งต่อไปนี้ได้:</span><span class="sxs-lookup"><span data-stu-id="e342f-114">With Retail, you can:</span></span>
+ <span data-ttu-id="e342f-115">ค้นหา หรือเรียกดูผลิตภัณฑ์ในร้านค้าอื่น ๆ</span><span class="sxs-lookup"><span data-stu-id="e342f-115">Search or browse products at other stores.</span></span>
+ <span data-ttu-id="e342f-116">ค้นหา หรือเรียกดูผลิตภัณฑ์ที่นำออกใช้ทั้งหมด</span><span class="sxs-lookup"><span data-stu-id="e342f-116">Search or browse all released products.</span></span>
+ <span data-ttu-id="e342f-117">สร้างธุรกรรมเงินสดและการขนส่งหรือใบสั่งของลูกค้า</span><span class="sxs-lookup"><span data-stu-id="e342f-117">Create cash-and-carry transactions or customer orders.</span></span>
+ <span data-ttu-id="e342f-118">เลือกตัวเลือกการจัดส่งสำหรับใบสั่งของลูกค้า</span><span class="sxs-lookup"><span data-stu-id="e342f-118">Select delivery options for customer orders.</span></span>
+ <span data-ttu-id="e342f-119">เบิกผลิตภัณฑ์ในร้านค้าปัจจุบันหรือร้านค้าอื่น</span><span class="sxs-lookup"><span data-stu-id="e342f-119">Pick up products at the current store or another store.</span></span>
+ <span data-ttu-id="e342f-120">ยกเลิกใบสั่งผลิตภัณฑ์ในร้านค้าปัจจุบันหรือร้านค้าอื่น</span><span class="sxs-lookup"><span data-stu-id="e342f-120">Cancel an order at the current store or another store.</span></span>
+ <span data-ttu-id="e342f-121">ส่งใบสั่งส่งคืนสินค้าหรือไม่มีใบเสร็จของร้านค้าปัจจุบันหรือร้านค้าอื่น</span><span class="sxs-lookup"><span data-stu-id="e342f-121">Return an order with or without the receipt at the current store or another store.</span></span>

