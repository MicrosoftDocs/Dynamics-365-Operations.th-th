---
title: โมดูลการแสดงเส้นทาง
description: หัวข้อนี้ครอบคลุมถึงโมดูลการแสดงเส้นทาง และอธิบายวิธีการเพิ่มลงในหน้าของไซต์ใน Microsoft Dynamics 365 Commerce
author: anupamar-ms
manager: annbe
ms.date: 06/01/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: ''
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: ''
ms.openlocfilehash: 1c6d846686e3214e976a55271694382d7c5973ed
ms.sourcegitcommit: 2683aacb426bfb3b541637edf1f8ec2d6cb5a745
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 06/01/2020
ms.locfileid: "3417403"
---
# <a name="breadcrumb-module"></a><span data-ttu-id="421ae-103">โมดูลการแสดงเส้นทาง</span><span class="sxs-lookup"><span data-stu-id="421ae-103">Breadcrumb module</span></span>

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

<span data-ttu-id="421ae-104">หัวข้อนี้ครอบคลุมถึงโมดูลการแสดงเส้นทาง และอธิบายวิธีการเพิ่มลงในหน้าของไซต์ใน Microsoft Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="421ae-104">This topic covers breadcrumb modules and describes how to add them to site pages in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="421ae-105">ภาพรวม</span><span class="sxs-lookup"><span data-stu-id="421ae-105">Overview</span></span>

<span data-ttu-id="421ae-106">โมดูลการแสดงเส้นทางใช้เพื่อให้การนำทางรองบนหน้าไซต์</span><span class="sxs-lookup"><span data-stu-id="421ae-106">Breadcrumb modules are used to provide secondary navigation on site pages.</span></span> <span data-ttu-id="421ae-107">โดยทั่วไปจะแสดงอยู่ที่ด้านบนของหน้า ด้านล่างของหัวข้อ</span><span class="sxs-lookup"><span data-stu-id="421ae-107">They are typically shown at the top of a page, below the header.</span></span> <span data-ttu-id="421ae-108">ถึงแม้ว่าคุณจะสามารถเพิ่มโมดูลแถบในหน้าใดก็ได้ โดยทั่วไปจะใช้ในหน้ารายละเอียดของผลิตภัณฑ์ (PDPs) เพื่อแสดงการจัดประเภทของผลิตภัณฑ์ตามลำดับชั้นและจัดให้มีวิธีที่รวดเร็วในการเลื่อนดูไซต์</span><span class="sxs-lookup"><span data-stu-id="421ae-108">Although breadcrumb modules can be added to any page, they are most often used on product details pages (PDPs), to show the product category hierarchy and provide a quick way to move around a site.</span></span> <span data-ttu-id="421ae-109">นอกจากนี้ยังสามารถใช้โมดูลการแสดงเส้นทางเพื่อแสดงการเชื่อมโยง "กลับไปที่ผลลัพธ์" เมื่อผู้ใช้เปิด PDP จากการค้นหาหรือหน้ารายการ</span><span class="sxs-lookup"><span data-stu-id="421ae-109">A breadcrumb module can also be used to show a "Back to results" link when users open a PDP from a search or list page.</span></span> <span data-ttu-id="421ae-110">ด้วยวิธีนี้ผู้ใช้สามารถกลับไปยังหน้ารายการที่ถูกกรองของตนเพื่อดำเนินการซื้อของต่อไปได้อย่างรวดเร็ว</span><span class="sxs-lookup"><span data-stu-id="421ae-110">In this way, users can quickly return to their filtered list page to continue shopping.</span></span>

<span data-ttu-id="421ae-111">บนหน้าเว็บที่มีบริบทประเภทของผลิตภัณฑ์ เช่น PDPs และหน้าประเภท โมดูลการแสดงเส้นทางจะแสดงการจัดประเภทตามลำดับชั้น</span><span class="sxs-lookup"><span data-stu-id="421ae-111">On pages that have product category context, such as PDPs and category pages, breadcrumb modules show the category hierarchy.</span></span> <span data-ttu-id="421ae-112">บนหน้าเว็บที่ไม่มีบริบทประเภท โมดูลการแสดงเส้นทางจะแสดง **&lt;รากไซต์&gt; / &lt;หน้าปัจจุบัน&gt;** โดยค่าเริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="421ae-112">On pages that don't have category context, breadcrumb modules show **&lt;Site root&gt; / &lt;Current page&gt;** by default.</span></span> <span data-ttu-id="421ae-113">นอกจากนี้คุณยังสามารถตั้งค่าโมดูลการแสดงเส้นทางด้วยตนเองบนหน้าไซต์ชนิดอื่นเพื่อแสดงลิงก์ไปยังหน้าเฉพาะบนไซต์</span><span class="sxs-lookup"><span data-stu-id="421ae-113">Breadcrumb modules can also be manually configured on other types of site pages to show links to specific pages on the site.</span></span>

<span data-ttu-id="421ae-114">รูปภาพต่อไปนี้แสดงตัวอย่างของโมดูลการแสดงเส้นทางที่แสดงการจัดประเภทตามลำดับชั้นบน PDP</span><span class="sxs-lookup"><span data-stu-id="421ae-114">The following image shows an example of a breadcrumb module that shows the category hierarchy on a PDP.</span></span>

![ตัวอย่างของโมดูลการแสดงเส้นทาง](./media/ecommerce-breadcrumb.PNG)

## <a name="breadcrumb-module-settings"></a><span data-ttu-id="421ae-116">การตั้งค่าโมดูลการแสดงเส้นทาง</span><span class="sxs-lookup"><span data-stu-id="421ae-116">Breadcrumb module settings</span></span>

<span data-ttu-id="421ae-117">โมดูลการแสดงเส้นทางขึ้นอยู่กับการตั้งค่า **ชนิดของการแสดงผลการแสดงเส้นทางใน PDP** ซึ่งกำหนดไว้ที่ **การตั้งค่าไซต์ \> ส่วนขยาย** ในตัวสร้างไซต์</span><span class="sxs-lookup"><span data-stu-id="421ae-117">The breadcrumb module relies on the **Breadcrumb display type on PDP** setting, which is defined at **Site Settings \> Extensions** in site builder.</span></span> <span data-ttu-id="421ae-118">การตั้งค่านี้มีสามค่าที่เป็นไปได้:</span><span class="sxs-lookup"><span data-stu-id="421ae-118">This setting has three possible values:</span></span>

- <span data-ttu-id="421ae-119">**แสดงการจัดประเภทตามลำดับชั้น** – เมื่อเลือกค่านี้ โมดูลการแสดงเส้นทางจะแสดงการจัดประเภทตามลำดับชั้นทั้งหมดของผลิตภัณฑ์ที่มีการดูบน PDP</span><span class="sxs-lookup"><span data-stu-id="421ae-119">**Show category hierarchy** – When this value is selected, the breadcrumb module will show the full category hierarchy of the product that is viewed on the PDP.</span></span>
- <span data-ttu-id="421ae-120">**แสดงกลับไปที่ผลลัพธ์** – เมื่อมีการเลือกค่านี้ โมดูลการแสดงเส้นทางแถบจะแสดงลิงก์ "กลับไปที่ผลลัพธ์" บน PDP ถ้าผู้ใช้เปิด PDP จากโมดูลที่อนุญาตลิงก์ "กลับไปที่ผลลัพธ์"</span><span class="sxs-lookup"><span data-stu-id="421ae-120">**Show back to results** – When this value is selected, the breadcrumb module will show a "Back to results" link on a PDP if the user opened the PDP from a module that allows for a "Back to results" link.</span></span> <span data-ttu-id="421ae-121">ฟังก์ชันนี้จะพร้อมใช้งานเมื่อผู้ใช้นำทางจากประเภท รายการการค้นหา และหน้ารายการคำแนะนำ</span><span class="sxs-lookup"><span data-stu-id="421ae-121">This functionality is available when users navigate from category, search, list, and recommendation lists pages.</span></span> <span data-ttu-id="421ae-122">เมื่อต้องการสนับสนุนฟังก์ชันการทำงานนี้ ชุดเก็บรวบรวมผลิตภัณฑ์และโมดูลผลการค้นหามีคุณสมบัติที่ชื่อ **อนุญาตให้กลับไปยังผลลัพธ์บน PDP**</span><span class="sxs-lookup"><span data-stu-id="421ae-122">To support this functionality, product collection and search results modules have a property that is named **Allow back to results on PDP**.</span></span> <span data-ttu-id="421ae-123">คุณสมบัตินี้จะช่วยให้คุณมีสามารถที่ยืดหยุ่นในการกำหนดโมดูลที่ควรสนับสนุนฟังก์ชันลิงก์ "กลับไปยังผลลัพธ์" บน PDP</span><span class="sxs-lookup"><span data-stu-id="421ae-123">This property gives you the flexibility to define which modules should support the "Back to results" link functionality on the PDP.</span></span> <span data-ttu-id="421ae-124">ตัวอย่างเช่น เมื่อมีการเลือก **แสดงกลับไปยังผลลัพธ์** สำหรับการตั้งค่า **ชนิดการแสดงผลการแสดงเส้นทางบน PDP** ของโมดูลการแสดงเส้นทาง และมีการเลือก **อนุญาตให้กลับไปยังผลลัพธ์บน PDP** สำหรับโมดูลของผลการค้นหาหน้าการค้นหา การเชื่อมโยง "กลับไปที่ผลลัพธ์" จะแสดงขึ้นเมื่อผู้ใช้นำทางจากหน้าค้นหาไปยัง PDP</span><span class="sxs-lookup"><span data-stu-id="421ae-124">For example, when **Show back to results** is selected for the **Breadcrumb display type on PDP** setting of the breadcrumb module, and **Allow back to results on PDP** is selected for the search page search results module, a "Back to results" link will be shown when users navigate from the search page to a PDP.</span></span>
- <span data-ttu-id="421ae-125">**แสดงการจัดประเภทตามลำดับชั้นและกลับไปที่ผลลัพธ์** – ค่านี้เป็นหารรวมของสองรายการก่อนหน้านี้</span><span class="sxs-lookup"><span data-stu-id="421ae-125">**Show category hierarchy and back to results** – This value is a combination of the previous two.</span></span> <span data-ttu-id="421ae-126">เมื่อมีการเลือกค่านี้ โมดูลการแสดงเส้นทางจะแสดงทั้งการจัดประเภทตามลำดับชั้นทั้งหมดและลิงก์ "กลับไปที่ผลลัพธ์" บน PDP (ถ้ามีการตั้งค่าคอนฟิก)</span><span class="sxs-lookup"><span data-stu-id="421ae-126">When this value is selected, the breadcrumb module will show both the full category hierarchy and a "Back to results" link (if it's configured) on a PDP.</span></span>

## <a name="breadcrumb-module-properties"></a><span data-ttu-id="421ae-127">คุณสมบัติโมดูลการแสดงเส้นทาง</span><span class="sxs-lookup"><span data-stu-id="421ae-127">Breadcrumb module properties</span></span>

| <span data-ttu-id="421ae-128">ชื่อคุณสมบัติ</span><span class="sxs-lookup"><span data-stu-id="421ae-128">Property name</span></span> | <span data-ttu-id="421ae-129">มูลค่า</span><span class="sxs-lookup"><span data-stu-id="421ae-129">Values</span></span> | <span data-ttu-id="421ae-130">คำอธิบาย</span><span class="sxs-lookup"><span data-stu-id="421ae-130">Description</span></span> |
|---------------|--------|-------------|
| <span data-ttu-id="421ae-131">ราก</span><span class="sxs-lookup"><span data-stu-id="421ae-131">Root</span></span> | <span data-ttu-id="421ae-132">ข้อความหรือลิงก์</span><span class="sxs-lookup"><span data-stu-id="421ae-132">Text or link</span></span>| <span data-ttu-id="421ae-133">คุณสมบัติที่เป็นตัวเลือกนี้จะระบุลิงก์ข้อความและเป้าหมายลิงก์สำหรับรากของไซต์การแสดงเส้นทาง</span><span class="sxs-lookup"><span data-stu-id="421ae-133">This optional property specifies link text and a link target for the breadcrumb site root.</span></span> <span data-ttu-id="421ae-134">ถ้าคุณสมบัตินี้ไม่ได้รับการตั้งค่าคอนฟิก จะไม่มีการกำหนดราก</span><span class="sxs-lookup"><span data-stu-id="421ae-134">If this property isn't configured, no root will be defined.</span></span> |
| <span data-ttu-id="421ae-135">ลิงก์การแสดงเส้นทาง</span><span class="sxs-lookup"><span data-stu-id="421ae-135">Breadcrumb link</span></span> | <span data-ttu-id="421ae-136">เชื่อมโยง</span><span class="sxs-lookup"><span data-stu-id="421ae-136">Link</span></span> | <span data-ttu-id="421ae-137">คุณสมบัติที่เป็นตัวเลือกนี้จะระบุลิงก์สำหรับการแสดงเส้นทางที่ตั้งค่าคอนฟิกด้วยตนเอง ถ้าจำเป็นต้องมีลิงก์เหล่านี้</span><span class="sxs-lookup"><span data-stu-id="421ae-137">This optional property specifies links for a manually configured breadcrumb, if these links are required.</span></span> <span data-ttu-id="421ae-138">ลิงก์จะปรากฏขึ้นตามลำดับรายการที่แสดงอยู่</span><span class="sxs-lookup"><span data-stu-id="421ae-138">Links appear in the order that they are listed in.</span></span> |

## <a name="add-a-breadcrumb-module-to-a-new-page"></a><span data-ttu-id="421ae-139">เพิ่มโมดูลการแสดงเส้นทางไปยังหน้าใหม่</span><span class="sxs-lookup"><span data-stu-id="421ae-139">Add a breadcrumb module to a new page</span></span>

<span data-ttu-id="421ae-140">การเพิ่มโมดูลการแสดงเส้นทางไปยัง PDP และตั้งค่าคุณสมบัติที่จำเป็น ให้ทำตามขั้นตอนต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="421ae-140">To add a breadcrumb module to a PDP and set the required properties, follow these steps.</span></span>

1. <span data-ttu-id="421ae-141">ไปที่ **การตั้งค่าไซต์/> ส่วนขยาย** จากนั้น สำหรับการตั้งค่า **ชนิดของการแสดงผลของการแสดงเส้นทางบน PDP** เลือก **แสดงการจัดประเภทตามลำดับชั้น**</span><span class="sxs-lookup"><span data-stu-id="421ae-141">Go to **Site Settings /> Extensions**, and then, for the **Breadcrumb display type on PDP** setting, select **Show category hierarchy**.</span></span>
1. <span data-ttu-id="421ae-142">ไปที่ **เท็มเพลต** และเลือกเท็มเพลต PDP</span><span class="sxs-lookup"><span data-stu-id="421ae-142">Go to **Templates**, and select the PDP template.</span></span>
1. <span data-ttu-id="421ae-143">ในช่อง **คอนเทนเนอร์** ที่มีโมดูลกล่องการซื้อ ให้เลือกจุดไข่ปลา (**...**) แล้วเลือก **เพิ่มโมดูล**</span><span class="sxs-lookup"><span data-stu-id="421ae-143">In the **Container** slot that contains the buy box module, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="421ae-144">ในกล่องโต้ตอบ **เพิ่มโมดูล** ให้เลือกโมดูล **การแสดงเส้นทาง** แล้วเลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="421ae-144">In the **Add Module** dialog box, select the **Breadcrumb** module, and then select **OK**.</span></span>
1. <span data-ttu-id="421ae-145">เลือก **บันทึก** เลือก **แก้ไขให้เสร็จสิ้น** เพื่อตรวจสอบในเท็มเพลต และจากนั้น เลือก **เผยแพร่** เพื่อเผยแพร่</span><span class="sxs-lookup"><span data-stu-id="421ae-145">Select **Save**, select **Finish editing** to check in the template, and then select **Publish** to publish it.</span></span>
1. <span data-ttu-id="421ae-146">ไปที่ **หน้า** และเปิด PDP ที่ใช้เท็มเพลต PDP</span><span class="sxs-lookup"><span data-stu-id="421ae-146">Go to **Pages**, and open a PDP that uses the PDP template.</span></span> <span data-ttu-id="421ae-147">ถ้ายังไม่มี PDP ให้สร้างขึ้น</span><span class="sxs-lookup"><span data-stu-id="421ae-147">If a PDP doesn't yet exist, create one.</span></span>
1. <span data-ttu-id="421ae-148">ในช่อง **คอนเทนเนอร์** ที่มีโมดูลกล่องการซื้อ ให้เลือกจุดไข่ปลา (**...**) แล้วเลือก **เพิ่มโมดูล**</span><span class="sxs-lookup"><span data-stu-id="421ae-148">In the **Container** slot that contains the buy box module, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="421ae-149">ในกล่องโต้ตอบ **เพิ่มโมดูล** ให้เลือกโมดูล **การแสดงเส้นทาง** แล้วเลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="421ae-149">In the **Add Module** dialog box, select the **Breadcrumb** module, and then select **OK**.</span></span>
1. <span data-ttu-id="421ae-150">ในบานหน้าต่างคุณสมบัติของ **การแสดงเส้นทาง** ภายใต้ **ราก** ให้เลือก **ข้อความลิงก์**</span><span class="sxs-lookup"><span data-stu-id="421ae-150">In the properties pane of the **Breadcrumb** slot, under **Root**, select **Link text**.</span></span>
1. <span data-ttu-id="421ae-151">ในกล่องโต้ตอบ **ข้อความลิงก์** ให้ป้อน **หน้าแรก** จากนั้นภายใต้ **เป้าหมายลิงก์** ให้เลือก **เพิ่มลิงก์**</span><span class="sxs-lookup"><span data-stu-id="421ae-151">In the **Link text** dialog box, enter **Home**, and then, under **Link target**, select **Add a link**.</span></span>
1. <span data-ttu-id="421ae-152">ในกล่องโต้ตอบ **เพิ่มลิงก์** ให้เลือกลิงก์สำหรับรากการแสดงเส้นทาง แล้วเลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="421ae-152">In the **Add a link** dialog box, select a link for the breadcrumb root, and then select **OK**.</span></span>
1. <span data-ttu-id="421ae-153">เลือก **บันทึก** และจากนั้น เลือก **แสดงตัวอย่าง** เพื่อแสดงตัวอย่างหน้า</span><span class="sxs-lookup"><span data-stu-id="421ae-153">Select **Save**, and then select **Preview** to preview the page.</span></span>
1. <span data-ttu-id="421ae-154">เลือก **แก้ไขให้เสร็จสิ้น** เพื่อตรวจสอบในเท็มเพลต และจากนั้น เลือก **เผยแพร่** เพื่อเผยแพร่</span><span class="sxs-lookup"><span data-stu-id="421ae-154">Select **Finish editing** to check in the template, and then select **Publish** to publish it.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="421ae-155">ทรัพยากรเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="421ae-155">Additional resources</span></span>

[<span data-ttu-id="421ae-156">ภาพรวมของชุดเริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="421ae-156">Starter kit overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="421ae-157">ภาพรวมของหน้าเริ่มต้นของประเภทและหน้าผลการค้นหาค่าเริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="421ae-157">Overview of default category landing page and search results page</span></span>](category-search-page-overview.md)

[<span data-ttu-id="421ae-158">โมดูลคอลเลกชันผลิตภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="421ae-158">Product collection modules</span></span>](product-collection-module-overview.md)

[<span data-ttu-id="421ae-159">โมดูลกล่องการซื้อ</span><span class="sxs-lookup"><span data-stu-id="421ae-159">Buy box module</span></span>](add-buy-box.md)
