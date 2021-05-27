---
title: ใช้การตั้งค่าหน่วยวัด
description: หัวข้อนี้จะครอบคลุมการตั้งค่าหน่วยวัด และอธิบายวิธีการใช้การตั้งค่าสินค้าคงคลังใน Microsoft Dynamics 365 Commerce
author: anupamar-ms
ms.date: 04/23/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: ''
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: ''
ms.openlocfilehash: d1fba966434b80c9b64c1f4d9b6b87993d59c0bf
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 05/11/2021
ms.locfileid: "6022385"
---
# <a name="apply-unit-of-measure-settings"></a><span data-ttu-id="5967b-103">ใช้การตั้งค่าหน่วยวัด</span><span class="sxs-lookup"><span data-stu-id="5967b-103">Apply unit of measure settings</span></span>

[!include [banner](includes/banner.md)]
[!include [banner](includes/preview-banner.md)]

<span data-ttu-id="5967b-104">หัวข้อนี้จะครอบคลุมการตั้งค่าหน่วยวัด และอธิบายวิธีการใช้การตั้งค่าสินค้าคงคลังใน Microsoft Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="5967b-104">This topic covers unit of measure settings and describes how to apply them in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="5967b-105">สามารถขายผลิตภัณฑ์ในหน่วยต่าง ๆ เช่น "แต่ละชิ้น" "คู่" และ "โหล"</span><span class="sxs-lookup"><span data-stu-id="5967b-105">A product can be sold in different units, such as "each," "pair," and "dozen."</span></span> <span data-ttu-id="5967b-106">ในศูนย์ควบคุม Commerce สามารถกําหนดหน่วยวัดการขายตามผลิตภัณฑ์และแสดงบนไซต์อีคอมเมิร์ซได้</span><span class="sxs-lookup"><span data-stu-id="5967b-106">In Commerce headquarters, the sell-by unit of measure can be defined for a product and shown on an e-commerce site.</span></span> <span data-ttu-id="5967b-107">ตัวอย่างเช่น ถ้าผู้ค้าปลีกขายผลิตภัณฑ์ทั้งแยกกันและเป็นโหล หน่วยวัดที่พร้อมใช้งานสามารถแสดงพร้อมกับข้อมูลผลิตภัณฑ์อื่น ๆ ได้</span><span class="sxs-lookup"><span data-stu-id="5967b-107">For example, if a retailer sells a product both individually and in dozens, the available units of measure can be shown together with other product information.</span></span>

<span data-ttu-id="5967b-108">ในตัวอย่างต่อไปนี้ มีการตั้งค่าคอนฟิกหน่วยวัดการขายตาม **ea** (แต่ละชิ้น) ให้กับผลิตภัณฑ์ในศูนย์ควบคุม Commerce</span><span class="sxs-lookup"><span data-stu-id="5967b-108">In the example in the following illustration, a sell-by unit of measure of **ea** (each) has been configured for a product in Commerce headquarters.</span></span>

![ตัวอย่างของผลิตภัณฑ์ที่มีการตั้งค่าคอนฟิกด้วยหน่วยวัดในศูนย์ควบคุม Commerce](./media/Productunit-headquarters.PNG)

> [!NOTE]
> <span data-ttu-id="5967b-110">การสนับสนุนเพื่อใช้และแสดงหน่วยวัดพร้อมใช้งาน ณ การปลดใช้งาน Commerce รุ่น 10.0.19</span><span class="sxs-lookup"><span data-stu-id="5967b-110">Support for applying and showing the unit of measure is available as of the Commerce version 10.0.19 release.</span></span>

## <a name="unit-of-measure-settings"></a><span data-ttu-id="5967b-111">การตั้งค่าหน่วยวัด</span><span class="sxs-lookup"><span data-stu-id="5967b-111">Unit of measure settings</span></span>

<span data-ttu-id="5967b-112">การตั้งค่าการแสดงหน่วยวัดถูกกําหนดในโปรแกรมสร้างไซต์ของ Commerce ที่ **การตั้งค่าไซต์ \> ส่วนขยาย \> แสดงหน่วยวัดของผลิตภัณฑ์**</span><span class="sxs-lookup"><span data-stu-id="5967b-112">Unit of measure display settings are defined in Commerce site builder, at **Site settings \> Extensions \> Display unit of measure for products**.</span></span> <span data-ttu-id="5967b-113">การตั้งค่าที่ได้รับการสนับสนุนมีสามอย่างดังนี้</span><span class="sxs-lookup"><span data-stu-id="5967b-113">There are three supported settings:</span></span>

- <span data-ttu-id="5967b-114">**อย่าแสดง** – เมื่อเลือกการตั้งค่านี้ไว้ ไซต์อีคอมเมิร์ซจะไม่แสดงหน่วยวัดของผลิตภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="5967b-114">**Do not display** – When this setting is selected, the e-commerce site won't show the unit of measure for the product.</span></span> <span data-ttu-id="5967b-115">ลักษณะการทำงานนี้เป็นลักษณะการทำงานเริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="5967b-115">This behavior is the default behavior.</span></span>
- <span data-ttu-id="5967b-116">**แสดงประสบการณ์การซื้อผลิตภัณฑ์** – เมื่อเลือกการตั้งค่านี้ หน่วยวัดจะแสดงอยู่ในรายละเอียดผลิตภัณฑ์ รถเข็น เช็คเอาท์ ประวัติใบสั่ง และหน้ารายละเอียดใบสั่ง</span><span class="sxs-lookup"><span data-stu-id="5967b-116">**Display in the product buying experience** – When this setting is selected, the unit of measure is shown on product details, cart, checkout, order history, and order details pages.</span></span>
- <span data-ttu-id="5967b-117">**แสดงในการเรียกดูผลิตภัณฑ์และประสบการณ์การซื้อ** – เมื่อเลือกการตั้งค่านี้ หน่วยวัดจะแสดงขึ้นบนหน้าประสบการณ์การซื้อ ผลิตภัณฑ์ และในระหว่างประสบการณ์การเรียกดูผลิตภัณฑ์ด้วย</span><span class="sxs-lookup"><span data-stu-id="5967b-117">**Display in the product browsing and buying experience** – When this setting is selected, the unit of measure is shown on the product buying experience pages and also during the product browsing experience.</span></span> <span data-ttu-id="5967b-118">เนื่องจากเป็นส่วนหนึ่งของลักษณะการทำงานนี้ หน่วยวัดจะแสดงอยู่ในโมดูลผลการค้นหาและชุดผลิตภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="5967b-118">As part of this behavior, units of measure are shown in search results and product collection modules.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="5967b-119">การตั้งค่าการแสดงหน่วยวัดพร้อมใช้งานเป็ฯการนำออกใช้ Commerce รุ่น 10.0.19</span><span class="sxs-lookup"><span data-stu-id="5967b-119">Unit of measure display settings are available as of the Commerce version 10.0.19 release.</span></span> <span data-ttu-id="5967b-120">ถ้าคุณกำลังอัพปเดตจากเวอร์ชันที่เก่ากว่าของ Commerce คุณต้องอัปเดตไฟล์ appsettings.json ด้วยตนเอง</span><span class="sxs-lookup"><span data-stu-id="5967b-120">If you're updating from an older version of Commerce, you must manually update the appsettings.json file.</span></span> <span data-ttu-id="5967b-121">สำหรับคำแนะนำ โปรดดู [SDK และอัปเดตไลบรารีโมดูล](e-commerce-extensibility/sdk-updates.md#update-the-appsettingsjson-file)</span><span class="sxs-lookup"><span data-stu-id="5967b-121">For instructions, see [SDK and module library updates](e-commerce-extensibility/sdk-updates.md#update-the-appsettingsjson-file).</span></span>

## <a name="modules-that-use-unit-of-measure-settings"></a><span data-ttu-id="5967b-122">โมดูลที่ใช้การตั้งค่าหน่วยวัด</span><span class="sxs-lookup"><span data-stu-id="5967b-122">Modules that use unit of measure settings</span></span>

<span data-ttu-id="5967b-123">โมดูลที่ใช้การตั้งค่าหน่วยวัด ได้แก่ โมดูลกล่องการซื้อ รถเข็น ไอคอนรถเข็น คอนเทนเนอร์ผลการค้นหา ชุดผลิตภัณฑ์ เช็คเอาท์ และโมดูลรายละเอียดใบสั่ง</span><span class="sxs-lookup"><span data-stu-id="5967b-123">Modules that use the unit of measure settings include the buy box, wishlist, cart, cart icon, search results container, product collection, checkout, and order details modules.</span></span>

<span data-ttu-id="5967b-124">ในตัวอย่างในภาพประกอบต่อไปนี้ หน้ารายละเอียดผลิตภัณฑ์ (PDP) แสดงหน่วยวัด (**ea**) ของผลิตภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="5967b-124">In the example in the following illustration, a product details page (PDP) shows the unit of measure (**ea**) for a product.</span></span>

![ตัวอย่างของ PDP ที่แสดงหน่วยวัด](./media/Productunit-PDP.png)

<span data-ttu-id="5967b-126">ในตัวอย่างในภาพประกอบต่อไปนี้ โมดูลการรวบรวมผลิตภัณฑ์ (PDP) แสดงหน่วยวัด (**ea**) ของผลิตภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="5967b-126">In the example in the following illustration, a product collection module shows the unit of measure (**ea**) for a product.</span></span>

![ตัวอย่างของโมดูลการรวบรวมผลิตภัณฑ์ที่แสดงหน่วยวัด](./media/Productunit-productcollection.png)

## <a name="additional-resources"></a><span data-ttu-id="5967b-128">ทรัพยากรเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="5967b-128">Additional resources</span></span>

[<span data-ttu-id="5967b-129">ภาพรวมของไลบรารีโมดูล</span><span class="sxs-lookup"><span data-stu-id="5967b-129">Module library overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="5967b-130">โมดูลรถเข็น</span><span class="sxs-lookup"><span data-stu-id="5967b-130">Cart module</span></span>](add-cart-module.md)

[<span data-ttu-id="5967b-131">โมดูลกล่องการซื้อ</span><span class="sxs-lookup"><span data-stu-id="5967b-131">Buy box module</span></span>](add-buy-box.md)

[<span data-ttu-id="5967b-132">หน้าและโมดูลการจัดการบัญชี</span><span class="sxs-lookup"><span data-stu-id="5967b-132">Account management pages and modules</span></span>](account-management.md)

[<span data-ttu-id="5967b-133">การอัปเดต SDK และไลบรารีโมดูล</span><span class="sxs-lookup"><span data-stu-id="5967b-133">SDK and module library updates</span></span>](e-commerce-extensibility/sdk-updates.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
