---
title: โมดูลมุมมองด่วน
description: หัวข้อนี้ครอบคลุมถึงโมดูลมุมมองด่วน และอธิบายวิธีการเพิ่มลงในเพจของไซต์ใน Microsoft Dynamics 365 Commerce
author: anupamar-ms
manager: annbe
ms.date: 01/28/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anupamar
ms.search.validFrom: 2020-01-08
ms.dyn365.ops.version: Release 10.0.17
ms.openlocfilehash: 07fbf8d4115561808b7c61489b343e1c72dd1b6d
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 02/15/2021
ms.locfileid: "5243804"
---
# <a name="quick-view-module"></a><span data-ttu-id="58ed3-103">โมดูลการแสดงผลแบบด่วน</span><span class="sxs-lookup"><span data-stu-id="58ed3-103">Quick view module</span></span>

[!include [banner](includes/banner.md)]
[!include [banner](includes/preview-banner.md)]

<span data-ttu-id="58ed3-104">หัวข้อนี้ครอบคลุมถึงโมดูลมุมมองด่วน และอธิบายวิธีการเพิ่มลงในเพจของไซต์ใน Microsoft Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="58ed3-104">This topic covers quick view modules and describes how to add them to site pages in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="58ed3-105">โมดูลมุมมองด่วนช่วยให้ผู้ใช้ดูข้อมูลผลิตภัณฑ์ได้อย่างรวดเร็วเมื่อเลือกดูผลิตภัณฑ์ในหน้ารายการ และเพิ่มผลิตภัณฑ์หนึ่งรายการหรือมากกว่าในรถเข็นจากหน้ารายการ โดยไม่ต้องไปที่หน้ารายละเอียดผลิตภัณฑ์ (PDP)</span><span class="sxs-lookup"><span data-stu-id="58ed3-105">The quick view module lets users quickly view product information when they browse products on a list page, and add one or more products to the cart from the list page, without having to go to the product details page (PDP).</span></span> <span data-ttu-id="58ed3-106">โมดูลมุมมองด่วนแสดงภาพรวมของข้อมูลผลิตภัณฑ์ที่ผู้ใช้ต้องมีในการตัดสินใจ "เพิ่มลงในรถเข็น"</span><span class="sxs-lookup"><span data-stu-id="58ed3-106">The quick view module provides an overview of the product information that users require to make an "add to cart" decision.</span></span> <span data-ttu-id="58ed3-107">นอกจากนี้ ยังให้ลิงค์กับ PDP ด้วย เพื่อให้ผู้ใช้สามารถดูรายละเอียดผลิตภัณฑ์เพิ่มเติมและตัวเลือกการซื้อได้</span><span class="sxs-lookup"><span data-stu-id="58ed3-107">It also provides a link to the PDP, so that users can view additional product details and purchase options.</span></span>

<span data-ttu-id="58ed3-108">โมดูลมุมมองด่วนได้รับการสนับสนุนโดยโมดูล [คอลเลกชันผลิตภัณฑ์](product-collection-module-overview.md) และ [ผลการค้นหา](search-result-module.md)</span><span class="sxs-lookup"><span data-stu-id="58ed3-108">The quick view module is supported by the [product collection](product-collection-module-overview.md) and [search results](search-result-module.md) modules.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="58ed3-109">โมดูลมุมมองด่วนพร้อมใช้งาน ณ การเริ่มใช้งาน Commerce รุ่น 10.0.17</span><span class="sxs-lookup"><span data-stu-id="58ed3-109">The quick view module is available as of the Commerce version 10.0.17 release.</span></span>

<span data-ttu-id="58ed3-110">ภาพประกอบต่อไปนี้แสดงตัวอย่างของโมดูลมุมมองด่วนบนหน้ารายการผลิตภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="58ed3-110">The following illustration shows an example of a quick view module on a product list page.</span></span>

![ตัวอย่างของโมดูลมุมมองด่วนบนหน้ารายการผลิตภัณฑ์](./media/ecommerce-quickview.PNG)

## <a name="module-properties"></a><span data-ttu-id="58ed3-112">คุณสมบัติของโมดูล</span><span class="sxs-lookup"><span data-stu-id="58ed3-112">Module properties</span></span>

<span data-ttu-id="58ed3-113">โมดูลมุมมองด่วนสนับสนุนฟังก์ชันบางอย่างเดียวกับโมดูลกล่องการซื้อ</span><span class="sxs-lookup"><span data-stu-id="58ed3-113">The quick view module supports some of the same functions as the buy box module.</span></span> <span data-ttu-id="58ed3-114">ดังนั้น คุณสมบัติของโมดูลมุมมองด่วนจะคล้ายกับคุณสมบัติของโมดูลกล่องการซื้อ</span><span class="sxs-lookup"><span data-stu-id="58ed3-114">Therefore, the properties of a quick view module resemble the properties of a buy box module.</span></span>

| <span data-ttu-id="58ed3-115">คุณสมบัติ</span><span class="sxs-lookup"><span data-stu-id="58ed3-115">Property</span></span> | <span data-ttu-id="58ed3-116">มูลค่า</span><span class="sxs-lookup"><span data-stu-id="58ed3-116">Values</span></span> | <span data-ttu-id="58ed3-117">คำอธิบาย</span><span class="sxs-lookup"><span data-stu-id="58ed3-117">Description</span></span> |
|----------------|--------|-------------|
| <span data-ttu-id="58ed3-118">แท็กหัวเรื่อง</span><span class="sxs-lookup"><span data-stu-id="58ed3-118">Heading tag</span></span> | <span data-ttu-id="58ed3-119">**H1**, **H2**, **H3**, **H4**, **H5**, or **H6**</span><span class="sxs-lookup"><span data-stu-id="58ed3-119">**H1**, **H2**, **H3**, **H4**, **H5**, or **H6**</span></span> | <span data-ttu-id="58ed3-120">คุณสมบัตินี้กำหนดป้ายชื่อเรื่องสำหรับชื่อผลิตภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="58ed3-120">This property defines the heading tag for the product title.</span></span> <span data-ttu-id="58ed3-121">ถ้าโมดูลมุมมองด่วนอยู่ที่ด้านบนของหน้าคุณสมบัตินี้ควรถูกตั้งค่าเป็น **H1** เพื่อให้เป็นไปตามมาตรฐานการเข้าถึง</span><span class="sxs-lookup"><span data-stu-id="58ed3-121">If the quick view module is at the top of the page, this property should be set to **H1** to meet accessibility standards.</span></span> |
| <span data-ttu-id="58ed3-122">อนุญาตราคาที่กำหนดเอง</span><span class="sxs-lookup"><span data-stu-id="58ed3-122">Allow custom price</span></span> | <span data-ttu-id="58ed3-123">**จริง** หรือ **เท็จ**</span><span class="sxs-lookup"><span data-stu-id="58ed3-123">**True** or **False**</span></span> | <span data-ttu-id="58ed3-124">ถ้าตั้งค่าคุณสมบัตินี้เป็น **จริง** ผู้ใช้สามารถป้อนราคาแบบกำหนดเองได้</span><span class="sxs-lookup"><span data-stu-id="58ed3-124">If this property is set to **True**, the user can enter a custom price.</span></span> |
| <span data-ttu-id="58ed3-125">ราคาต่ำสุด</span><span class="sxs-lookup"><span data-stu-id="58ed3-125">Minimum price</span></span> | <span data-ttu-id="58ed3-126">เลขจำนวนเต็ม</span><span class="sxs-lookup"><span data-stu-id="58ed3-126">Integer</span></span> | <span data-ttu-id="58ed3-127">คุณสมบัตินี้สามารถใช้ได้เฉพาะเมื่อตั้งค่าคุณสมบัติ **อนุญาตราคาแบบกำหนดเอง** เป็น **จริง** เท่านั้น</span><span class="sxs-lookup"><span data-stu-id="58ed3-127">This property is applicable only if the **Allow custom price** property is set to **True**.</span></span> <span data-ttu-id="58ed3-128">ค่านี้จะกําหนดราคาต่ำสุดที่ผู้ใช้สามารถป้อนได้ ($1)</span><span class="sxs-lookup"><span data-stu-id="58ed3-128">It defines the minimum price that the user can enter (for example, $1).</span></span> |
| <span data-ttu-id="58ed3-129">ราคาสูงสุด</span><span class="sxs-lookup"><span data-stu-id="58ed3-129">Maximum price</span></span> | <span data-ttu-id="58ed3-130">เลขจำนวนเต็ม</span><span class="sxs-lookup"><span data-stu-id="58ed3-130">Integer</span></span> | <span data-ttu-id="58ed3-131">คุณสมบัตินี้สามารถใช้ได้เฉพาะเมื่อตั้งค่าคุณสมบัติ **อนุญาตราคาแบบกำหนดเอง** เป็น **จริง** เท่านั้น</span><span class="sxs-lookup"><span data-stu-id="58ed3-131">This property is applicable only if the **Allow custom price** property is set to **True**.</span></span> <span data-ttu-id="58ed3-132">ค่านี้จะกําหนดราคาสูงสุดที่ผู้ใช้สามารถป้อนได้ ($1,000)</span><span class="sxs-lookup"><span data-stu-id="58ed3-132">It defines the maximum price that the user can enter (for example, $1,000).</span></span> |

## <a name="commerce-site-builder-settings"></a><span data-ttu-id="58ed3-133">การตั้งค่าตัวสร้างไซต์ Commerce</span><span class="sxs-lookup"><span data-stu-id="58ed3-133">Commerce site builder settings</span></span>

<span data-ttu-id="58ed3-134">เช่นเดียวกับโมดูลกล่องการซื้อ โมดูลมุมมองด่วนจะมีลักษณะการตั้งค่าที่ **การตั้งค่าไซต์ \> ส่วนขยาย \> เพิ่มผลิตภัณฑ์ลงในรถเข็น**</span><span class="sxs-lookup"><span data-stu-id="58ed3-134">Like the buy box module, the quick view module respects the settings at **Site Settings \> Extensions \> Add product to cart**.</span></span> <span data-ttu-id="58ed3-135">อย่างไรก็ตาม การตั้งค่า **นําทางไปยังหน้ารถเข็น** จะถูกละเว้น เนื่องจากไม่สอดคล้องกันกับวัตถุประสงค์ของโมดูลมุมมองด่วน ซึ่งเป็นการอนุญาตให้ผู้ใช้เรียกดูผลิตภัณฑ์หลายรายการในหน้ารายการและเพิ่มผลิตภัณฑ์เหล่านั้นลงในรถเข็นโดยไม่ย้ายออกจากหน้ารายการ</span><span class="sxs-lookup"><span data-stu-id="58ed3-135">However, the **Navigate to cart page** setting is ignored, because it's inconsistent with the purpose of the quick view module, which is to enable users to browse multiple products on a list page and add them to the cart without moving away from the list page.</span></span>

## <a name="add-a-quick-view-module-to-a-product-collection-module"></a><span data-ttu-id="58ed3-136">เพิ่มโมดูลมุมมองด่วนไปยังโมดูลการรวบรวมผลิตภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="58ed3-136">Add a quick view module to a product collection module</span></span>

<span data-ttu-id="58ed3-137">โมดูลมุมมองด่วนสามารถเพิ่มไปโมดูลคอลเลกชันผลิตภัณฑ์และผลการค้นหา</span><span class="sxs-lookup"><span data-stu-id="58ed3-137">A quick view module can be added to the product collection and search results modules.</span></span>

<span data-ttu-id="58ed3-138">เมื่อต้องการเพิ่มโมดูลมุมมองด่วนไปโมดูลคอลเลกชันผลิตภัณฑ์ในโปรแกรมสร้างไซต์ Commerce ให้ทำตามขั้นตอนต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="58ed3-138">To add a quick view module to a product collection module in Commerce site builder, follow these steps.</span></span>

1. <span data-ttu-id="58ed3-139">ไปที่ **หน้า** แล้วเลือกโฮมเพจสำหรับไซต์ Fabrikam</span><span class="sxs-lookup"><span data-stu-id="58ed3-139">Go to **Pages**, and then select the home page for the Fabrikam site.</span></span>
1. <span data-ttu-id="58ed3-140">ไปที่โมดูล **คอลเลกชันผลิตภัณฑ์** ใดๆ บนโฮมเพจ เลือกจุดไข่ปลา (**...**) แล้วเลือก **เพิ่มโมดูล**</span><span class="sxs-lookup"><span data-stu-id="58ed3-140">Go to any **Product Collection** module on the homepage, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="58ed3-141">ในกล่องโต้ตอบ **เพิ่มโมดูล** ให้เลือกโมดูล **มุมมองด่วน** แล้วเลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="58ed3-141">In the **Add Module** dialog box, select the **Quick View** module, and then select **OK**.</span></span>
1. <span data-ttu-id="58ed3-142">ในบานหน้าต่างคุณสมบัติของโมดูล **มุมมองด่วน** ให้เลือก **หัวข้อ**</span><span class="sxs-lookup"><span data-stu-id="58ed3-142">In the properties pane of the **Quick View** module, select **Heading**.</span></span> <span data-ttu-id="58ed3-143">ในกล่องโต้ตอบ **หัวข้อ** ให้ตั้งค่าฟิลด์ **ระดับหัวข้อ** เป็น **H2** แล้วเลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="58ed3-143">In the **Heading** dialog box, set the **Heading Level** field to **H2**, and then select **OK**.</span></span>
1. <span data-ttu-id="58ed3-144">เลือก **บันทึก** เลือก **แก้ไขให้เสร็จสิ้น** เพื่อตรวจสอบในหน้า และจากนั้น เลือก **เผยแพร่** เพื่อเผยแพร่</span><span class="sxs-lookup"><span data-stu-id="58ed3-144">Select **Save**, select **Finish editing** to check in the page, and then select **Publish** to publish it.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="58ed3-145">ทรัพยากรเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="58ed3-145">Additional resources</span></span>

[<span data-ttu-id="58ed3-146">ภาพรวมของไลบรารีโมดูล</span><span class="sxs-lookup"><span data-stu-id="58ed3-146">Module library overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="58ed3-147">โมดูลกล่องการซื้อ</span><span class="sxs-lookup"><span data-stu-id="58ed3-147">Buy box module</span></span>](add-buy-box.md)

[<span data-ttu-id="58ed3-148">โมดูลการรวบรวมผลิตภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="58ed3-148">Product collection module</span></span>](product-collection-module-overview.md)

[<span data-ttu-id="58ed3-149">โมดูลผลการค้นหา</span><span class="sxs-lookup"><span data-stu-id="58ed3-149">Search results module</span></span>](search-result-module.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]