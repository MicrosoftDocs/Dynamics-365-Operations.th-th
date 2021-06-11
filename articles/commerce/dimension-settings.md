---
title: ใช้การตั้งค่าการแสดงบนมิติของผลิตภัณฑ์
description: หัวข้อนี้ครอบคลุมการตั้งค่าการแสดงของมิติของผลิตภัณฑ์และอธิบายวิธีการใช้มิติใน Microsoft Dynamics 365 Commerce
author: anupamar-ms
ms.date: 05/28/2021
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
ms.openlocfilehash: b901622bbfc8d6b3066879f6456a4ab618ca4076
ms.sourcegitcommit: 53b797ff1b524f581046b48cdde42f50b37495bc
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 05/28/2021
ms.locfileid: "6117249"
---
# <a name="apply-display-settings-for-product-dimensions"></a><span data-ttu-id="547b7-103">ใช้การตั้งค่าการแสดงบนมิติของผลิตภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="547b7-103">Apply display settings for product dimensions</span></span>

[!include [banner](includes/banner.md)]
[!include [banner](includes/preview-banner.md)]

<span data-ttu-id="547b7-104">หัวข้อนี้ครอบคลุมการตั้งค่าการแสดงของมิติของผลิตภัณฑ์และอธิบายวิธีการใช้มิติใน Microsoft Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="547b7-104">This topic covers the display settings for product dimensions and describes how to apply them in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="547b7-105">Dynamics 365 Commerce สนับสนุนมิติ ขนาด ลักษณะ และสีเพื่อแยกผลิตภัณฑ์ย่อย</span><span class="sxs-lookup"><span data-stu-id="547b7-105">Dynamics 365 Commerce supports size, style, and color dimensions to distinguish product variants.</span></span> <span data-ttu-id="547b7-106">โดยทั่วไป มิติจะแสดงเป็นค่าข้อความ เช่น "เล็ก" "ปานกลาง" และ "ใหญ่" เป็นขนาด และ "ดำ" และ "น้ำตาล" เป็นสี</span><span class="sxs-lookup"><span data-stu-id="547b7-106">Dimensions are typically shown as text values, such as "Small," "Medium," and "Large" for sizes, and "Black" and "Brown" for colors.</span></span> <span data-ttu-id="547b7-107">อย่างไรก็ตาม ถ้าผลิตภัณฑ์สนับสนุนการเปลี่ยนแปลงหลายอย่าง ซึ่งอาจยากที่จะเรียกดูผลิตภัณฑ์ย่อย เนื่องจากการเลือกหลายรายการจะต้องดูรูปภาพของแต่ละผลิตภัณฑ์ย่อย</span><span class="sxs-lookup"><span data-stu-id="547b7-107">However, if a product supports many variations, it can be difficult to browse product variants, because multiple selections are required to view the image for each variant.</span></span> <span data-ttu-id="547b7-108">เพื่อให้สามารถเลือกดูผลิตภัณฑ์ย่อยได้ง่ายขึ้น การนำออกใช้รุ่น 10.0.20 ของ Commerce จึงสามารถใช้รูปภาพและรหัสเลขฐานสิบหก (ฐานสิบหก) เพื่อแสดงมิติเป็นตัวอย่างสีใหม่</span><span class="sxs-lookup"><span data-stu-id="547b7-108">To make it easier to browse product variants, the version 10.0.20 release of Commerce can use images and hexadecimal (hex) codes to show dimensions as swatches.</span></span>

<span data-ttu-id="547b7-109">ในโปรแกรมสร้างไซต์ Commerce การตั้งค่ามิติจะถูกกำหนดใน **การตั้งค่าไซต์ \> ส่วนขยาย \> การตั้งค่ามิติ**</span><span class="sxs-lookup"><span data-stu-id="547b7-109">In Commerce site builder, dimension settings are defined at **Site Settings \> Extensions \> Dimension Settings**.</span></span> <span data-ttu-id="547b7-110">ในภาพต่อไปนี้จะแสดงตัวอย่างของการตั้งค่ามิติในตัวสร้างไซต์</span><span class="sxs-lookup"><span data-stu-id="547b7-110">The following illustration shows an example of dimension settings in site builder.</span></span>

![ตัวอย่างของการตั้งค่าไซต์ในตัวสร้างไซต์ Commerce](./dev-itpro/media/swatch_site_settings.PNG)

<span data-ttu-id="547b7-112">การตั้งค่ามิติมีอยู่สองการตั้งค่าต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="547b7-112">Two dimension settings are available:</span></span>

- <span data-ttu-id="547b7-113">**มิติที่จะแสดงเป็นรูปภาพ** – ระบุว่ามิติใดที่ควรจะปรากฏเป็นตัวอย่างสีบนหน้าไซต์อีคอมเมิร์ซ เช่น หน้ารายละเอียดผลิตภัณฑ์ (PDPs) และหน้ารายการผลการค้นหา</span><span class="sxs-lookup"><span data-stu-id="547b7-113">**Dimensions to display as image** – Specify which dimensions should appear as swatches on e-commerce site pages such as product details pages (PDPs) and search result list pages.</span></span> <span data-ttu-id="547b7-114">ชุดของสี ขนาด และมิติลักษณะใดๆ สามารถแสดงเป็นตัวอย่างสีไว้ได้</span><span class="sxs-lookup"><span data-stu-id="547b7-114">Any combination of color, size, and style dimensions can be shown as a swatch.</span></span> <span data-ttu-id="547b7-115">ถ้าเลือกมิติไว้เพื่อแสดงเป็นตัวอย่างสี การแสดงโมดูล Commerce จะค้นหาการตั้งค่าคอนฟิกที่พร้อมใช้งานของรหัสฐานสิบหก</span><span class="sxs-lookup"><span data-stu-id="547b7-115">If a dimension is selected for display as a swatch, Commerce module rendering will look for an available configuration of a hex code swatch.</span></span> <span data-ttu-id="547b7-116">ถ้าไม่มีการตั้งค่าคอนฟิกรหัสฐานสิบหก ตรรกะของระบบจะค้นหาการตั้งค่าคอนฟิกตัวอย่างสีของ URL รูปภาพ</span><span class="sxs-lookup"><span data-stu-id="547b7-116">If no hex code is configured, system logic will look for a configuration of an image URL swatch.</span></span> <span data-ttu-id="547b7-117">ถ้าไม่มีการตั้งค่าคอนฟิกรหัสฐานสิบหกหรือ URL รูปภาพ ข้อความจะแสดงขึ้น</span><span class="sxs-lookup"><span data-stu-id="547b7-117">If neither a hex code nor an image URL is configured, text will be shown.</span></span>

    <span data-ttu-id="547b7-118">ภาพต่อไปนี้จะแสดงตัวอย่างที่จะปรากฏเป็นตัวอย่างที่ PDP บนไซต์อีคอมเมิร์ซรวมตัวอยย่างสีและขนาด</span><span class="sxs-lookup"><span data-stu-id="547b7-118">The following illustration shows an example where a PDP on an e-commerce site includes color and size swatches.</span></span> <span data-ttu-id="547b7-119">ในตัวอย่างนี้ มีการตั้งค่าคอนฟิกรหัสฐานสิบหกให้กับมิติสี</span><span class="sxs-lookup"><span data-stu-id="547b7-119">In this example, a hex code is configured for the color dimension.</span></span> <span data-ttu-id="547b7-120">ดังนั้นจึงมีตัวอย่างเป็นสี</span><span class="sxs-lookup"><span data-stu-id="547b7-120">Therefore, swatches are shown as colors.</span></span> <span data-ttu-id="547b7-121">อย่างไรก็ตาม ไม่มีการตั้งค่าคอนฟิกรหัสฐานสิบหกหรือ URL รูปภาพให้กับมิติขนาด</span><span class="sxs-lookup"><span data-stu-id="547b7-121">However, neither a hex code nor an image URL is configured for the size dimension.</span></span> <span data-ttu-id="547b7-122">ดังนั้นข้อความจึงถูกแสดง</span><span class="sxs-lookup"><span data-stu-id="547b7-122">Therefore, text is shown.</span></span>

    ![ตัวอย่างของมิติสีที่แสดงเป็นตัวอย่างสีในหน้ารายละเอียดผลิตภัณฑ์อีคอมเมิร์ซ](./dev-itpro/media/swatch_pdp.png)

- <span data-ttu-id="547b7-124">**มิติที่จะแสดงในบัตรผลิตภัณฑ์** – ระบุมิติที่ควรปรากฏในบัตรผลิตภัณฑ์ ซึ่งแสดงในรายการและบนหน้ารายการ</span><span class="sxs-lookup"><span data-stu-id="547b7-124">**Dimensions to display in product card** – Specify which dimensions should appear on product cards that are shown in lists and on list pages.</span></span> <span data-ttu-id="547b7-125">ก่อนที่มิติจะปรากฏในบัตรผลิตภัณฑ์ คุณต้องเปิดใช้งานการตั้งค่านี้ของมิตินั้น</span><span class="sxs-lookup"><span data-stu-id="547b7-125">Before a dimension can appear on a product card, this setting must be enabled for that dimension.</span></span> <span data-ttu-id="547b7-126">การตั้งค่า **แสดงมิติเป็นรูปภาพ** ควรเปิดใช้งานด้วย</span><span class="sxs-lookup"><span data-stu-id="547b7-126">The **Dimensions to display as image** setting should also be enabled.</span></span> <span data-ttu-id="547b7-127">พฤติกรรมการเลือกตัวอย่างสีในบัตรผลิตภัณฑ์ได้รับการปรับให้เหมาะสมกับมิติสี</span><span class="sxs-lookup"><span data-stu-id="547b7-127">The swatch selection behavior on product cards is optimized for the color dimension.</span></span> <span data-ttu-id="547b7-128">สำหรับมิติอื่น ส่วนขยายมุมมองอาจจำเป็นเพื่อกำหนดค่าพฤติกรรมการเลือกตัวอย่างสี</span><span class="sxs-lookup"><span data-stu-id="547b7-128">For other dimensions, a view extension might be required to customize swatch selection behavior.</span></span>

    <span data-ttu-id="547b7-129">ตัวอย่างต่อไปนี้จะแสดงตัวอย่างที่หน้ารายการบนไซต์อีคอมเมิร์ซประกอบด้วยบัตรผลิตภัณฑ์ที่มีตัวอย่างสีรวมอยู่ด้วย</span><span class="sxs-lookup"><span data-stu-id="547b7-129">The following illustration shows an example where a list page on an e-commerce site contains product cards that include color swatches.</span></span>

    ![ตัวอย่างของมิติสีที่แสดงเป็นตัวอย่างสีในหน้ารายการอีคอมเมิร์ซ](./dev-itpro/media/swatch_searchresults.PNG)

<span data-ttu-id="547b7-131">สำหรับข้อมูลเกี่ยวกับวิธีตั้งค่าคอนฟิกมิติของผลิตภัณฑ์เพื่อให้มิติของผลิตภัณฑ์แสดงเป็นตัวอย่างสีบนหน้าไซต์ โปรดดูที่ [ตั้งค่าคอนฟิกค่ามิติของผลิตภัณฑ์ที่จะปรากฏเป็นตัวอย่างสี](./dev-itpro/dimensions-swatch.md)</span><span class="sxs-lookup"><span data-stu-id="547b7-131">For information about how to configure product dimensions so that they are shown as swatches on site pages, see [Configure product dimension values to appear as swatches](./dev-itpro/dimensions-swatch.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="547b7-132">ทรัพยากรเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="547b7-132">Additional resources</span></span>

[<span data-ttu-id="547b7-133">ภาพรวมของไลบรารีโมดูล</span><span class="sxs-lookup"><span data-stu-id="547b7-133">Module library overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="547b7-134">โมดูลผลการค้นหา</span><span class="sxs-lookup"><span data-stu-id="547b7-134">Search results module</span></span>](search-result-module.md)

[<span data-ttu-id="547b7-135">โมดูลกล่องการซื้อ</span><span class="sxs-lookup"><span data-stu-id="547b7-135">Buy box module</span></span>](add-buy-box.md)

[<span data-ttu-id="547b7-136">ตั้งค่าคอนฟิกค่ามิติของผลิตภัณฑ์ให้ปรากฏเป็นตัวอย่างสี</span><span class="sxs-lookup"><span data-stu-id="547b7-136">Configure product dimension values to appear as swatches</span></span>](./dev-itpro/dimensions-swatch.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
