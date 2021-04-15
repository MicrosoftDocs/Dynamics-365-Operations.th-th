---
title: โมดูล iFrame
description: หัวข้อนี้ครอบคลุมถึงโมดูล iFrame และอธิบายวิธีการเพิ่มลงในเพจของไซต์ใน Microsoft Dynamics 365 Commerce
author: anupamar-ms
ms.date: 09/15/2020
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
ms.search.validFrom: 2020-02-10
ms.dyn365.ops.version: Release 10.0.13
ms.openlocfilehash: 7b397b91d1b8a45347ef2d05f42fb7c610ab3912
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 03/31/2021
ms.locfileid: "5797081"
---
# <a name="iframe-module"></a><span data-ttu-id="c503a-103">โมดูล iFrame</span><span class="sxs-lookup"><span data-stu-id="c503a-103">Iframe module</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="c503a-104">หัวข้อนี้ครอบคลุมถึงโมดูล iFrame และอธิบายวิธีการเพิ่มลงในเพจของไซต์ใน Microsoft Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="c503a-104">This topic covers the iframe module and describes how to add it to site pages in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="c503a-105">โมดูล iFrame มี iFrame (เฟรมอินไลน์) ที่โฮสต์เนื้อหาภายนอกบนไซต์</span><span class="sxs-lookup"><span data-stu-id="c503a-105">An iframe module provides an iframe (inline frame) that hosts external content on a site.</span></span> <span data-ttu-id="c503a-106">ตัวอย่างเช่น คุณสามารถใช้เพื่อโฮสต์วิดีโอ YouTube หรือตัวแสดงไฟล์ PDF บนหน้าไซต์ใดๆ</span><span class="sxs-lookup"><span data-stu-id="c503a-106">For example, it can be used to host a YouTube video or a PDF file viewer on any site page.</span></span> 

<span data-ttu-id="c503a-107">โมดูล iFrame ต้องใช้ URL เป้าหมาย</span><span class="sxs-lookup"><span data-stu-id="c503a-107">An iframe module requires a target URL.</span></span> <span data-ttu-id="c503a-108">จากนั้นจะโฮสต์เนื้อหาของหน้าเป้าหมายภายในองค์ประกอบของ **iFrame** HTML</span><span class="sxs-lookup"><span data-stu-id="c503a-108">It then hosts the content of the target page inside an HTML **iframe** element.</span></span> <span data-ttu-id="c503a-109">URL ภายนอก ต้องอยู่ในรายการอนุญาตสำหรับคำสั่งนโยบายความปลอดภัยของเนื้อหา (CSP) ของไซต์แต่ละรายการ</span><span class="sxs-lookup"><span data-stu-id="c503a-109">External URLs must be on the allow list per the site's content security policy (CSP) directives.</span></span> <span data-ttu-id="c503a-110">สำหรับเนื้อหา iFrame ควรอนุญาตให้ใช้ URL โดยใช้คำสั่ง **frame-ancestor**</span><span class="sxs-lookup"><span data-stu-id="c503a-110">For iframe content, URLs should be allowed by using the **frame-ancestor** directive.</span></span> <span data-ttu-id="c503a-111">สำหรับข้อมูลเพิ่มเติม ให้ดู [จัดการนโยบายความปลอดภัยของเนื้อหา (CSP)](manage-csp.md)</span><span class="sxs-lookup"><span data-stu-id="c503a-111">For more information, see [Manage Content Security Policy (CSP)](manage-csp.md).</span></span>

> [!NOTE]
> <span data-ttu-id="c503a-112">โมดูล iframe มีอยู่ใน Dynamics 365 Commerce รุ่น10.0.13</span><span class="sxs-lookup"><span data-stu-id="c503a-112">The iframe module is available in the Dynamics 365 Commerce 10.0.13 release.</span></span>

<span data-ttu-id="c503a-113">รูปภาพต่อไปนี้แสดงตัวอย่างของโมดูล iFrame ซึ่งแสดงวิดีโอภายนอกในบนหน้าไซต์</span><span class="sxs-lookup"><span data-stu-id="c503a-113">The following image shows examples of iframe modules that showcase external videos on site pages.</span></span>

![ตัวอย่างของโมดูล iFrame ที่แสดงวิดีโอภายนอก](./media/ecommerce-iframe.PNG)

## <a name="iframe-module-properties"></a><span data-ttu-id="c503a-115">คุณลักษณะโมดูล iFrame</span><span class="sxs-lookup"><span data-stu-id="c503a-115">Iframe module properties</span></span>

| <span data-ttu-id="c503a-116">ชื่อคุณสมบัติ</span><span class="sxs-lookup"><span data-stu-id="c503a-116">Property name</span></span>             | <span data-ttu-id="c503a-117">มูลค่า</span><span class="sxs-lookup"><span data-stu-id="c503a-117">Value</span></span>                 | <span data-ttu-id="c503a-118">คำอธิบาย</span><span class="sxs-lookup"><span data-stu-id="c503a-118">Description</span></span> |
|---------------------------|-----------------------|-------------|
| <span data-ttu-id="c503a-119">หัวข้อ</span><span class="sxs-lookup"><span data-stu-id="c503a-119">Heading</span></span> | <span data-ttu-id="c503a-120">Text</span><span class="sxs-lookup"><span data-stu-id="c503a-120">Text</span></span> | <span data-ttu-id="c503a-121">หัวข้อสำหรับโมดูล</span><span class="sxs-lookup"><span data-stu-id="c503a-121">The heading for the module.</span></span> |
| <span data-ttu-id="c503a-122">URL เป้าหมาย</span><span class="sxs-lookup"><span data-stu-id="c503a-122">Target URL</span></span> | <span data-ttu-id="c503a-123">URL</span><span class="sxs-lookup"><span data-stu-id="c503a-123">URL</span></span> | <span data-ttu-id="c503a-124">URL ที่โฮสต์อยู่ในโมดูล</span><span class="sxs-lookup"><span data-stu-id="c503a-124">The URL that is hosted in the module.</span></span> |
| <span data-ttu-id="c503a-125">ความสูง</span><span class="sxs-lookup"><span data-stu-id="c503a-125">Height</span></span> | <span data-ttu-id="c503a-126">จำนวนหรือเปอร์เซ็นต์</span><span class="sxs-lookup"><span data-stu-id="c503a-126">Number or percentage</span></span> | <span data-ttu-id="c503a-127">ความสูงของโมดูล พิกเซลหรือเป็นเปอร์เซ็นต์</span><span class="sxs-lookup"><span data-stu-id="c503a-127">The height of the module, in pixels or as a percentage.</span></span> <span data-ttu-id="c503a-128">ตัวอย่างเช่น ค่า **100** จะถือว่าเป็นจำนวนพิกเซล และค่า **100%** จะถือเป็นเปอร์เซ็นต์</span><span class="sxs-lookup"><span data-stu-id="c503a-128">For example, the value **100** will be treated as a number of pixels, and the value **100%** will be treated as a percentage.</span></span> |
| <span data-ttu-id="c503a-129">ป้ายกำกับ Aria</span><span class="sxs-lookup"><span data-stu-id="c503a-129">Aria label</span></span> | <span data-ttu-id="c503a-130">Text</span><span class="sxs-lookup"><span data-stu-id="c503a-130">Text</span></span> | <span data-ttu-id="c503a-131">สามารถกำหนดป้ายชื่อ Accessible Rich Internet Applications (ARIA) ได้ เพื่อวัตถุประสงค์ในการเข้าถึง</span><span class="sxs-lookup"><span data-stu-id="c503a-131">An Accessible Rich Internet Applications (ARIA) label can be defined for accessibility purposes.</span></span> |

## <a name="add-an-iframe-module-to-a-page"></a><span data-ttu-id="c503a-132">เพิ่มโมดูล iFrame ไปยังหน้า</span><span class="sxs-lookup"><span data-stu-id="c503a-132">Add an iframe module to a page</span></span>

<span data-ttu-id="c503a-133">การเพิ่มโมดูล iFrame ให้กับหน้าเพื่อแสดงวิดีโอภายนอก ให้ทำตามขั้นตอนต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="c503a-133">To add an iframe module to a page to show an external video, follow these steps.</span></span>

1. <span data-ttu-id="c503a-134">ไปที่ **เท็มเพลต** และจากนั้น เลือก **สร้าง** เพื่อสร้างเท็มเพลตใหม่</span><span class="sxs-lookup"><span data-stu-id="c503a-134">Go to **Templates**, and select **New** to create a new template.</span></span>
1. <span data-ttu-id="c503a-135">ในกล่องโต้ตอบ **เท็มเพลตใหม่** ภายใต้ **ชื่อเท็มเพลต** ให้ป้อน **เท็มเพลตการตลาด** และจากนั้น เลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="c503a-135">In the **New Template** dialog box, under **Template name**, enter **Marketing template**, and then select **OK**.</span></span>
1. <span data-ttu-id="c503a-136">เลือก **บันทึก** เลือก **แก้ไขให้เสร็จสิ้น** เพื่อตรวจสอบในเท็มเพลต และจากนั้น เลือก **เผยแพร่** เพื่อเผยแพร่</span><span class="sxs-lookup"><span data-stu-id="c503a-136">Select **Save**, select **Finish editing** to check in the template, and then select **Publish** to publish it.</span></span>
1. <span data-ttu-id="c503a-137">ไปที่ **หน้า** และจากนั้น ให้เลือก **สร้าง** เพื่อสร้างหน้าใหม่</span><span class="sxs-lookup"><span data-stu-id="c503a-137">Go to **Pages**, and select **New** to create a new page.</span></span>
1. <span data-ttu-id="c503a-138">ในกล่องโต้ตอบ **เลือกเท็มเพลต** ให้เลือกเท็มเพลตของ **เท็มเพลตการตลาด**</span><span class="sxs-lookup"><span data-stu-id="c503a-138">In the **Choose a template** dialog box, select the **Marketing template** template.</span></span> <span data-ttu-id="c503a-139">ภายใต้ **ชื่อของหน้า** ให้ป้อน **หน้าการตลาด** และจากนั้น เลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="c503a-139">Under **Page name**, enter **Marketing page**, and then select **OK**.</span></span>
1. <span data-ttu-id="c503a-140">ในช่อง **หลัก** ของหน้าใหม่ เลือกปุ่มจุดไข่ปลา (**...**) แล้วเลือก **เพิ่มโมดูล**</span><span class="sxs-lookup"><span data-stu-id="c503a-140">In the **Main** slot of the new page, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="c503a-141">ในกล่องโต้ตอบ **เพิ่มโมดูล** ให้เลือกโมดูล **คอนเทนเนอร์** แล้วเลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="c503a-141">In the **Add Module** dialog box, select the **Container** module, and then select **OK**.</span></span>
1. <span data-ttu-id="c503a-142">ในบานหน้าต่างคุณสมบัติของโมดูล ให้ตั้งค่า **ความกว้าง** เป็น **เติมคอนเทนเนอร์**</span><span class="sxs-lookup"><span data-stu-id="c503a-142">In the module's properties pane, set the **Width** value to **Fill Container**.</span></span>
1. <span data-ttu-id="c503a-143">ในช่อง **คอนเทนเนอร์** เลือกจุดไข่ปลา (**...**) แล้วจากนั้นเลือก **เพิ่มโมดูล**</span><span class="sxs-lookup"><span data-stu-id="c503a-143">In the **Container** slot, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="c503a-144">ในกล่องโต้ตอบ **เพิ่มโมดูล** ให้เลือกโมดูล **iFrame** แล้วเลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="c503a-144">In the **Add Module** dialog box, select the **iframe** module, and then select **OK**.</span></span>
1. <span data-ttu-id="c503a-145">ในบานหน้าต่างคุณสมบัติของโมดูล ให้ตั้งค่า **URL เป้าหมาย** ไปยัง URL ภายนอกสำหรับวิดีโอ</span><span class="sxs-lookup"><span data-stu-id="c503a-145">In the module's properties pane, set the **Target URL** value to an external URL for a video.</span></span>
1. <span data-ttu-id="c503a-146">ตั้งค่าคุณสมบัติอื่นๆ เช่น **ส่วนหัว** และ **ความสูง** ตามที่คุณต้องการ</span><span class="sxs-lookup"><span data-stu-id="c503a-146">Set other properties, such as **Heading** and **Height**, as you require.</span></span>
1. <span data-ttu-id="c503a-147">เลือก **บันทึก** เลือก **แก้ไขให้เสร็จสิ้น** เพื่อตรวจสอบในหน้า และจากนั้น เลือก **เผยแพร่** เพื่อเผยแพร่</span><span class="sxs-lookup"><span data-stu-id="c503a-147">Select **Save**, select **Finish editing** to check in the page, and then select **Publish** to publish it.</span></span>
1. <span data-ttu-id="c503a-148">ไปที่หน้าการตลาดบนไซต์ของคุณ</span><span class="sxs-lookup"><span data-stu-id="c503a-148">Go to the marketing page on your site.</span></span> <span data-ttu-id="c503a-149">คุณควรเห็นว่าวิดีโอแสดงอยู่ในโมดูล iFrame</span><span class="sxs-lookup"><span data-stu-id="c503a-149">You should see that the video is rendered in the iframe module.</span></span>
 
## <a name="additional-resources"></a><span data-ttu-id="c503a-150">ทรัพยากรเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="c503a-150">Additional resources</span></span>

[<span data-ttu-id="c503a-151">ภาพรวมของไลบรารีโมดูล</span><span class="sxs-lookup"><span data-stu-id="c503a-151">Module library overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="c503a-152">จัดการนโยบายความปลอดภัยของเนื้อหา (CSP)</span><span class="sxs-lookup"><span data-stu-id="c503a-152">Manage Content Security Policy (CSP)</span></span>](manage-csp.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]