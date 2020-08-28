---
title: เพิ่มโค้ดสคริปต์ให้กับหน้าไซต์เพื่อสนับสนุนการตรวจวัดระยะไกล
description: หัวข้อนี้อธิบายวิธีการเพิ่มรหัสสคริปต์ฝั่งไคลเอนต์ไปยังหน้าไซต์ของคุณ เพื่อสนับสนุนการเรียกเก็บเงินของการตรวจวัดระยะไกลฝั่งไคลเอนต์
author: bicyclingfool
manager: annbe
ms.date: 03/20/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.search.scope: Operations, Retail, Core
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: StuHarg
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 4f26ed5b6674566f579e801f4b7be63c2d0dc38d
ms.sourcegitcommit: 81f162f2d50557d7afe292c8d326618ba0bc3259
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 08/11/2020
ms.locfileid: "3686825"
---
# <a name="add-script-code-to-site-pages-to-support-telemetry"></a><span data-ttu-id="cde96-103">เพิ่มโค้ดสคริปต์ให้กับหน้าไซต์เพื่อสนับสนุนการตรวจวัดระยะไกล</span><span class="sxs-lookup"><span data-stu-id="cde96-103">Add script code to site pages to support telemetry</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="cde96-104">หัวข้อนี้อธิบายวิธีการเพิ่มรหัสสคริปต์ฝั่งไคลเอนต์ไปยังหน้าไซต์ของคุณ เพื่อสนับสนุนการเรียกเก็บเงินของการตรวจวัดระยะไกลฝั่งไคลเอนต์</span><span class="sxs-lookup"><span data-stu-id="cde96-104">This topic describes how to add client-side script code to your site pages to support the collection of client-side telemetry.</span></span>

## <a name="overview"></a><span data-ttu-id="cde96-105">ภาพรวม</span><span class="sxs-lookup"><span data-stu-id="cde96-105">Overview</span></span>

<span data-ttu-id="cde96-106">Web analytics เป็นเครื่องมือที่จำเป็น เมื่อคุณต้องการทำความเข้าใจวิธีการที่ลูกค้าของคุณโต้ตอบกับไซต์ของคุณ และตัดสินใจที่จะช่วยปรับปรุงประสบการณ์สำหรับการแปลงสูงสุด</span><span class="sxs-lookup"><span data-stu-id="cde96-106">Web analytics are an essential tool when you want to understand how your customers interact with your site and make decisions that will help optimize the experience for maximum conversion.</span></span> <span data-ttu-id="cde96-107">แพคเกจการวิเคราะห์เว็บจำนวนมากพร้อมให้ความช่วยเหลือในการบรรลุเป้าหมายเหล่านี้ เช่น Google Analytics, Clicky, Moz Analytics และ KISSMetrics</span><span class="sxs-lookup"><span data-stu-id="cde96-107">Many web analytics packages are available to help you achieve these goals, such as Google Analytics, Clicky, Moz Analytics, and KISSMetrics.</span></span> <span data-ttu-id="cde96-108">แพคเกจการวิเคราะห์เว็บส่วนใหญ่กำหนดให้คุณต้องเพิ่มรหัสสคริปต์ฝั่งไคลเอนต์ในองค์ประกอบที่เป็น **\<head\>** ของ HTML สำหรับทุกเพจของไซต์ของคุณ</span><span class="sxs-lookup"><span data-stu-id="cde96-108">Most web analytics packages require that you add client-side script code in the **\<head\>** element of the HTML for all pages of your site.</span></span>

> [!NOTE]
> <span data-ttu-id="cde96-109">คำแนะนำในหัวข้อนี้จะใช้กับฟังก์ชันฝั่งไคลเอนต์แบบกำหนดเองอื่นๆ ที่ Microsoft Dynamics 365 Commerce ไม่มีข้อเสนอโดยไม่ได้กล่าวถึง</span><span class="sxs-lookup"><span data-stu-id="cde96-109">The instructions in this topic also apply to other custom client-side functionality that Microsoft Dynamics 365 Commerce doesn't natively offer.</span></span>

## <a name="create-a-reusable-page-fragment-for-your-script-code"></a><span data-ttu-id="cde96-110">สร้างส่วนของหน้าที่สามารถใช้ซ้ำได้สำหรับรหัสสคริปต์ของคุณ</span><span class="sxs-lookup"><span data-stu-id="cde96-110">Create a reusable page fragment for your script code</span></span>

<span data-ttu-id="cde96-111">ส่วนของหน้าจะช่วยให้คุณสามารถนำสคริปต์อินไลน์หรือภายนอกมาใช้ใหม่ผ่านหน้าทั้งหมดบนไซต์ของคุณได้ โดยไม่ต้องใช้เท็มเพลตที่มีการใช้</span><span class="sxs-lookup"><span data-stu-id="cde96-111">A page fragment allows you to reuse inline or external script code across all pages on your site, regardless of the template they use.</span></span>

### <a name="create-a-reusable-page-fragment-for-your-inline-script-code"></a><span data-ttu-id="cde96-112">สร้างส่วนของหน้าที่สามารถใช้ซ้ำได้สำหรับรหัสสคริปต์อินไลน์ของคุณ</span><span class="sxs-lookup"><span data-stu-id="cde96-112">Create a reusable page fragment for your inline script code</span></span>

<span data-ttu-id="cde96-113">เมื่อต้องการสร้างส่วนของหน้าที่สามารถใช้ซ้ำได้สำหรับรหัสสคริปต์แบบอินไลน์ของคุณในโปรแกรมสร้างไซต์ ให้ทำตามขั้นตอนเหล่านี้</span><span class="sxs-lookup"><span data-stu-id="cde96-113">To create a reusable page fragment for your inline script code in site builder, follow these steps.</span></span>

1. <span data-ttu-id="cde96-114">ไปที่ **ส่วนย่อย** และให้เลือก **สร้าง**</span><span class="sxs-lookup"><span data-stu-id="cde96-114">Go to **Fragments**, and then select **New**.</span></span>
1. <span data-ttu-id="cde96-115">ในกล่องโต้ตอบ **ส่วนย่อยของหน้าใหม่** ให้เลือก **สคริปต์แบบอินไลน์**</span><span class="sxs-lookup"><span data-stu-id="cde96-115">In the **New page fragment** dialog box, select **Inline script**.</span></span>
1. <span data-ttu-id="cde96-116">ภายใต้ **ชื่อส่วนย่อยของหน้า** ให้ป้อนชื่อสำหรับส่วน และจากนั้น เลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="cde96-116">Under **Page fragment name**, enter a name for the fragment, and then select **OK**.</span></span>
1. <span data-ttu-id="cde96-117">ภายใต้ส่วนของหน้าที่คุณสร้างขึ้น ให้เลือกโมดูล **สคริปต์แบบอินไลน์เริ่มต้น**</span><span class="sxs-lookup"><span data-stu-id="cde96-117">Under the page fragment that you created, select the **Default inline script** module.</span></span>
1. <span data-ttu-id="cde96-118">ในบานหน้าต่างคุณสมบัติทางด้านขวา ภายใต้ **สคริปต์แบบอินไลน์** ให้ป้อนสคริปต์ฝั่งไคลเอนต์ของคุณ</span><span class="sxs-lookup"><span data-stu-id="cde96-118">In the property pane on the right, under **Inline script**, enter your client-side script.</span></span> <span data-ttu-id="cde96-119">จากนั้น ตั้งค่าคอนฟิกตัวเลือกอื่นๆ ตามที่คุณต้องการ</span><span class="sxs-lookup"><span data-stu-id="cde96-119">Then configure other options as you require.</span></span>
1. <span data-ttu-id="cde96-120">เลือก **บันทึก** และจากนั้น เลือก **แก้ไขให้เสร็จสิ้น**</span><span class="sxs-lookup"><span data-stu-id="cde96-120">Select **Save**, and then select **Finish editing**.</span></span>
1. <span data-ttu-id="cde96-121">เลือก **เผยแพร่**</span><span class="sxs-lookup"><span data-stu-id="cde96-121">Select **Publish**.</span></span>

### <a name="create-a-reusable-page-fragment-for-your-external-script-code"></a><span data-ttu-id="cde96-122">สร้างส่วนของหน้าที่สามารถใช้ซ้ำได้สำหรับรหัสสคริปต์ภายนอกของคุณ</span><span class="sxs-lookup"><span data-stu-id="cde96-122">Create a reusable page fragment for your external script code</span></span>

<span data-ttu-id="cde96-123">เมื่อต้องการสร้างส่วนของหน้าที่สามารถใช้ซ้ำได้สำหรับรหัสสคริปต์ภายนอกของคุณในโปรแกรมสร้างไซต์ ให้ทำตามขั้นตอนเหล่านี้</span><span class="sxs-lookup"><span data-stu-id="cde96-123">To create a reusable page fragment for your external script code in site builder, follow these steps.</span></span>

1. <span data-ttu-id="cde96-124">ไปที่ **ส่วนย่อย** และให้เลือก **สร้าง**</span><span class="sxs-lookup"><span data-stu-id="cde96-124">Go to **Fragments**, and then select **New**.</span></span>
1. <span data-ttu-id="cde96-125">ในกล่องโต้ตอบ **ส่วนย่อยของหน้าใหม่** ให้เลือก **สคริปต์ภายนอก**</span><span class="sxs-lookup"><span data-stu-id="cde96-125">In the **New page fragment** dialog box, select **External script**.</span></span>
1. <span data-ttu-id="cde96-126">ภายใต้ **ชื่อส่วนย่อยของหน้า** ให้ป้อนชื่อสำหรับส่วน และจากนั้น เลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="cde96-126">Under **Page fragment name**, enter a name for the fragment, and then select **OK**.</span></span>
1. <span data-ttu-id="cde96-127">ภายใต้ส่วนของหน้าที่คุณสร้างขึ้น ให้เลือกโมดูล **สคริปต์ภายนอกเริ่มต้น**</span><span class="sxs-lookup"><span data-stu-id="cde96-127">Under the page fragment that you created, select the **Default external script** module.</span></span>
1. <span data-ttu-id="cde96-128">ในบานหน้าต่างคุณสมบัติทางด้านขวา ภายใต้ **แหล่งที่มาของสคริปต์** ให้เพิ่ม URL ภายนอกหรือที่เกี่ยวข้องสำหรับแหล่งที่มาของสคริปต์ภายนอก</span><span class="sxs-lookup"><span data-stu-id="cde96-128">In the property pane on the right, under **Script source**, add an external or relative URL for the external script source.</span></span> <span data-ttu-id="cde96-129">จากนั้น ตั้งค่าคอนฟิกตัวเลือกอื่นๆ ตามที่คุณต้องการ</span><span class="sxs-lookup"><span data-stu-id="cde96-129">Then configure other options as you require.</span></span>
1. <span data-ttu-id="cde96-130">เลือก **บันทึก** และจากนั้น เลือก **แก้ไขให้เสร็จสิ้น**</span><span class="sxs-lookup"><span data-stu-id="cde96-130">Select **Save**, and then select **Finish editing**.</span></span>
1. <span data-ttu-id="cde96-131">เลือก **เผยแพร่**</span><span class="sxs-lookup"><span data-stu-id="cde96-131">Select **Publish**.</span></span>

## <a name="add-a-page-fragment-that-includes-script-code-to-a-template"></a><span data-ttu-id="cde96-132">เพิ่มส่วนของหน้าซึ่งรวมถึงรหัสสคริปต์ให้กับเท็มเพลต</span><span class="sxs-lookup"><span data-stu-id="cde96-132">Add a page fragment that includes script code to a template</span></span>

<span data-ttu-id="cde96-133">เมื่อต้องการเพิ่มส่วนของหน้าที่รวมรหัสสคริปต์ไปยังเท็มเพลตในโปรแกรมสร้างไซต์ ให้ทำตามขั้นตอนเหล่านี้</span><span class="sxs-lookup"><span data-stu-id="cde96-133">To add a page fragment that includes script code to a template in site builder, follow these steps.</span></span>

1. <span data-ttu-id="cde96-134">ไปที่ **แม่แบบ** และเปิดแม่แบบสำหรับเพจที่คุณต้องการเพิ่มรหัสสคริปต์ของคุณ</span><span class="sxs-lookup"><span data-stu-id="cde96-134">Go to **Templates**, and open the template for the pages that you want to add your script code to.</span></span>
1. <span data-ttu-id="cde96-135">ในบานหน้าต่างด้านซ้าย ให้ขยายลำดับชั้นแม่แบบเพื่อแสดงช่อง **ส่วนหัวของ HTML**</span><span class="sxs-lookup"><span data-stu-id="cde96-135">In the left pane, expand the template hierarchy to show the **HTML Head** slot.</span></span>
1. <span data-ttu-id="cde96-136">ในช่อง**ส่วนหัวของ HTML** เลือก ปุ่มจุดไข่ปลา (**...**) แล้วจากนั้น เลือก **เพิ่มส่วนของหน้า**</span><span class="sxs-lookup"><span data-stu-id="cde96-136">In the **HTML Head** slot, select the ellipsis button (**...**), and then select **Add Page Fragment**.</span></span>
1. <span data-ttu-id="cde96-137">เลือกส่วนที่คุณสร้างสำหรับรหัสสคริปต์ของคุณ</span><span class="sxs-lookup"><span data-stu-id="cde96-137">Select the fragment that you created for your script code.</span></span>
1. <span data-ttu-id="cde96-138">เลือก **บันทึก** และจากนั้น เลือก **แก้ไขให้เสร็จสิ้น**</span><span class="sxs-lookup"><span data-stu-id="cde96-138">Select **Save**, and then select **Finish editing**.</span></span>
1. <span data-ttu-id="cde96-139">เลือก **เผยแพร่**</span><span class="sxs-lookup"><span data-stu-id="cde96-139">Select **Publish**.</span></span>

## <a name="add-an-external-script-or-inline-script-directly-to-a-template"></a><span data-ttu-id="cde96-140">เพิ่มสคริปต์ภายนอกหรือสคริปต์อินไลน์ไปยังเท็มเพลตโดยตรง</span><span class="sxs-lookup"><span data-stu-id="cde96-140">Add an external script or inline script directly to a template</span></span>

<span data-ttu-id="cde96-141">ถ้าคุณต้องการแทรกสคริปต์แบบอินไลน์หรือภายนอกโดยตรงลงในชุดของหน้าที่ถูกควบคุมโดยเท็มเพลตเดียว คุณไม่จำเป็นต้องสร้างส่วนของหน้าก่อน</span><span class="sxs-lookup"><span data-stu-id="cde96-141">If you want to insert an inline or external script directly into a set of pages that are controlled by a single template, you don't have to create a page fragment first.</span></span>

### <a name="add-an-inline-script-directly-to-a-template"></a><span data-ttu-id="cde96-142">เพิ่มสคริปต์อินไลน์ไปยังเท็มเพลตโดยตรง</span><span class="sxs-lookup"><span data-stu-id="cde96-142">Add an inline script directly to a template</span></span>

<span data-ttu-id="cde96-143">เมื่อต้องการเพิ่มสคริปต์แบบอินไลน์ให้กับเท็มเพลตในโปรแกรมสร้างไซต์โดยตรง ให้ทำตามขั้นตอนเหล่านี้</span><span class="sxs-lookup"><span data-stu-id="cde96-143">To add an inline script directly to a template in site builder, follow these steps.</span></span>

1. <span data-ttu-id="cde96-144">ไปที่ **แม่แบบ** และเปิดแม่แบบสำหรับเพจที่คุณต้องการเพิ่มรหัสสคริปต์ของคุณ</span><span class="sxs-lookup"><span data-stu-id="cde96-144">Go to **Templates**, and open the template for the pages that you want to add your script code to.</span></span>
1. <span data-ttu-id="cde96-145">ในบานหน้าต่างด้านซ้าย ให้ขยายลำดับชั้นแม่แบบเพื่อแสดงช่อง **ส่วนหัวของ HTML**</span><span class="sxs-lookup"><span data-stu-id="cde96-145">In the left pane, expand the template hierarchy to show the **HTML Head** slot.</span></span>
1. <span data-ttu-id="cde96-146">ในช่อง **ส่วนหัวของ HTML** เลือก ปุ่มจุดไข่ปลา (**...**) แล้วจากนั้น เลือก **เพิ่มโมดูล**</span><span class="sxs-lookup"><span data-stu-id="cde96-146">In the **HTML Head** slot, select the ellipsis button (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="cde96-147">ในกล่องโต้ตอบ **เพิ่มโมดูล** ให้เลือก **สคริปต์แบบอินไลน์**</span><span class="sxs-lookup"><span data-stu-id="cde96-147">In the **Add Module** dialog box, select **Inline script**.</span></span>
1. <span data-ttu-id="cde96-148">ในบานหน้าต่างคุณสมบัติทางด้านขวา ภายใต้ **สคริปต์แบบอินไลน์** ให้ป้อนสคริปต์ฝั่งไคลเอนต์ของคุณ</span><span class="sxs-lookup"><span data-stu-id="cde96-148">In the property pane on the right, under **Inline script**, enter your client-side script.</span></span> <span data-ttu-id="cde96-149">จากนั้น ตั้งค่าคอนฟิกตัวเลือกอื่นๆ ตามที่คุณต้องการ</span><span class="sxs-lookup"><span data-stu-id="cde96-149">Then configure other options as you require.</span></span>
1. <span data-ttu-id="cde96-150">เลือก **บันทึก** และจากนั้น เลือก **แก้ไขให้เสร็จสิ้น**</span><span class="sxs-lookup"><span data-stu-id="cde96-150">Select **Save**, and then select **Finish editing**.</span></span>
1. <span data-ttu-id="cde96-151">เลือก **เผยแพร่**</span><span class="sxs-lookup"><span data-stu-id="cde96-151">Select **Publish**.</span></span>

### <a name="add-an-external-script-directly-to-a-template"></a><span data-ttu-id="cde96-152">เพิ่มสคริปต์ภายนอกไปยังเท็มเพลตโดยตรง</span><span class="sxs-lookup"><span data-stu-id="cde96-152">Add an external script directly to a template</span></span>

<span data-ttu-id="cde96-153">เมื่อต้องการเพิ่มสคริปต์ภายนอกให้กับเท็มเพลตในโปรแกรมสร้างไซต์โดยตรง ให้ทำตามขั้นตอนเหล่านี้</span><span class="sxs-lookup"><span data-stu-id="cde96-153">To add an external script directly to a template in site builder, follow these steps.</span></span>

1. <span data-ttu-id="cde96-154">ไปที่ **แม่แบบ** และเปิดแม่แบบสำหรับเพจที่คุณต้องการเพิ่มรหัสสคริปต์ของคุณ</span><span class="sxs-lookup"><span data-stu-id="cde96-154">Go to **Templates**, and open the template for the pages that you want to add your script code to.</span></span>
1. <span data-ttu-id="cde96-155">ในบานหน้าต่างด้านซ้าย ให้ขยายลำดับชั้นแม่แบบเพื่อแสดงช่อง **ส่วนหัวของ HTML**</span><span class="sxs-lookup"><span data-stu-id="cde96-155">In the left pane, expand the template hierarchy to show the **HTML Head** slot.</span></span>
1. <span data-ttu-id="cde96-156">ในช่อง **ส่วนหัวของ HTML** เลือก ปุ่มจุดไข่ปลา (**...**) แล้วจากนั้น เลือก **เพิ่มโมดูล**</span><span class="sxs-lookup"><span data-stu-id="cde96-156">In the **HTML Head** slot, select the ellipsis button (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="cde96-157">ในกล่องโต้ตอบ **เพิ่มโมดูล** ให้เลือก **สคริปต์ภายนอก**</span><span class="sxs-lookup"><span data-stu-id="cde96-157">In the **Add Module** dialog box, select **External script**.</span></span>
1. <span data-ttu-id="cde96-158">ในบานหน้าต่างคุณสมบัติทางด้านขวา ภายใต้ **แหล่งที่มาของสคริปต์** ให้เพิ่ม URL ภายนอกหรือที่เกี่ยวข้องสำหรับแหล่งที่มาของสคริปต์ภายนอก</span><span class="sxs-lookup"><span data-stu-id="cde96-158">In the property pane on the right, under **Script source**, add an external or relative URL for the external script source.</span></span> <span data-ttu-id="cde96-159">จากนั้น ตั้งค่าคอนฟิกตัวเลือกอื่นๆ ตามที่คุณต้องการ</span><span class="sxs-lookup"><span data-stu-id="cde96-159">Then configure other options as you require.</span></span>
1. <span data-ttu-id="cde96-160">เลือก **บันทึก** และจากนั้น เลือก **แก้ไขให้เสร็จสิ้น**</span><span class="sxs-lookup"><span data-stu-id="cde96-160">Select **Save**, and then select **Finish editing**.</span></span>
1. <span data-ttu-id="cde96-161">เลือก **เผยแพร่**</span><span class="sxs-lookup"><span data-stu-id="cde96-161">Select **Publish**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="cde96-162">ทรัพยากรเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="cde96-162">Additional resources</span></span>

[<span data-ttu-id="cde96-163">เพิ่มโลโก้</span><span class="sxs-lookup"><span data-stu-id="cde96-163">Add a logo</span></span>](add-logo.md)

[<span data-ttu-id="cde96-164">เลือกธีมของไซต์</span><span class="sxs-lookup"><span data-stu-id="cde96-164">Select a site theme</span></span>](select-site-theme.md)

[<span data-ttu-id="cde96-165">ทำงานกับไฟล์การแก้ไข CSS</span><span class="sxs-lookup"><span data-stu-id="cde96-165">Work with CSS override files</span></span>](css-override-files.md)

[<span data-ttu-id="cde96-166">เพิ่มไอคอนประจำไซต์</span><span class="sxs-lookup"><span data-stu-id="cde96-166">Add a favicon</span></span>](add-favicon.md)

[<span data-ttu-id="cde96-167">เพิ่มข้อความต้อนรับ</span><span class="sxs-lookup"><span data-stu-id="cde96-167">Add a welcome message</span></span>](add-welcome-message.md)

[<span data-ttu-id="cde96-168">เพิ่มข้อความสงวนลิขสิทธิ์</span><span class="sxs-lookup"><span data-stu-id="cde96-168">Add a copyright notice</span></span>](add-copyright-notice.md)

[<span data-ttu-id="cde96-169">เพิ่มภาษาลงในไซต์ของคุณ</span><span class="sxs-lookup"><span data-stu-id="cde96-169">Add languages to your site</span></span>](add-languages-to-site.md)
