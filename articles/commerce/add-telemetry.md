---
title: เพิ่มโค้ดสคริปต์ให้กับหน้าไซต์เพื่อสนับสนุนการตรวจวัดระยะไกล
description: หัวข้อนี้อธิบายวิธีการเพิ่มรหัสสคริปต์ฝั่งไคลเอนต์ไปยังหน้าไซต์ของคุณ เพื่อสนับสนุนการเรียกเก็บเงินของการตรวจวัดระยะไกลฝั่งไคลเอนต์
author: bicyclingfool
ms.date: 09/29/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: StuHarg
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: fb1773ab10b23a586eb6a8286f145181818585b9
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 03/31/2021
ms.locfileid: "5797442"
---
# <a name="add-script-code-to-site-pages-to-support-telemetry"></a><span data-ttu-id="7c0c9-103">เพิ่มโค้ดสคริปต์ให้กับหน้าไซต์เพื่อสนับสนุนการตรวจวัดระยะไกล</span><span class="sxs-lookup"><span data-stu-id="7c0c9-103">Add script code to site pages to support telemetry</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="7c0c9-104">หัวข้อนี้อธิบายวิธีการเพิ่มรหัสสคริปต์ฝั่งไคลเอนต์ไปยังหน้าไซต์ของคุณ เพื่อสนับสนุนการเรียกเก็บเงินของการตรวจวัดระยะไกลฝั่งไคลเอนต์</span><span class="sxs-lookup"><span data-stu-id="7c0c9-104">This topic describes how to add client-side script code to your site pages to support the collection of client-side telemetry.</span></span>

<span data-ttu-id="7c0c9-105">Web analytics เป็นเครื่องมือที่จำเป็น เมื่อคุณต้องการทำความเข้าใจวิธีการที่ลูกค้าของคุณโต้ตอบกับไซต์ของคุณ และตัดสินใจที่จะช่วยปรับปรุงประสบการณ์สำหรับการแปลงสูงสุด</span><span class="sxs-lookup"><span data-stu-id="7c0c9-105">Web analytics are an essential tool when you want to understand how your customers interact with your site and make decisions that will help optimize the experience for maximum conversion.</span></span> <span data-ttu-id="7c0c9-106">แพคเกจการวิเคราะห์เว็บจำนวนมากพร้อมให้ความช่วยเหลือในการบรรลุเป้าหมายเหล่านี้ เช่น Google Analytics, Clicky, Moz Analytics และ KISSMetrics</span><span class="sxs-lookup"><span data-stu-id="7c0c9-106">Many web analytics packages are available to help you achieve these goals, such as Google Analytics, Clicky, Moz Analytics, and KISSMetrics.</span></span> <span data-ttu-id="7c0c9-107">แพคเกจการวิเคราะห์เว็บส่วนใหญ่กำหนดให้คุณต้องเพิ่มรหัสสคริปต์ฝั่งไคลเอนต์ในองค์ประกอบที่เป็น **\<head\>** ของ HTML สำหรับทุกเพจของไซต์ของคุณ</span><span class="sxs-lookup"><span data-stu-id="7c0c9-107">Most web analytics packages require that you add client-side script code in the **\<head\>** element of the HTML for all pages of your site.</span></span>

> [!NOTE]
> <span data-ttu-id="7c0c9-108">คำแนะนำในหัวข้อนี้จะใช้กับฟังก์ชัน client-side แบบกำหนดเองอื่นๆ ที่ Microsoft Microsoft Dynamics 365 Commerce ไม่ได้กล่าวถึง</span><span class="sxs-lookup"><span data-stu-id="7c0c9-108">The instructions in this topic also apply to other custom client-side functionality that Microsoft Dynamics 365 Commerce doesn't natively offer.</span></span>

## <a name="create-a-reusable-fragment-for-your-script-code"></a><span data-ttu-id="7c0c9-109">สร้างส่วนที่สามารถใช้ซ้ำได้สำหรับรหัสสคริปต์ของคุณ</span><span class="sxs-lookup"><span data-stu-id="7c0c9-109">Create a reusable fragment for your script code</span></span>

<span data-ttu-id="7c0c9-110">ส่วนย่อยจะช่วยให้คุณสามารถนำสคริปต์อินไลน์หรือภายนอกมาใช้ใหม่ผ่านหน้าทั้งหมดบนไซต์ของคุณได้ โดยไม่ต้องใช้เท็มเพลตที่มีการใช้</span><span class="sxs-lookup"><span data-stu-id="7c0c9-110">A fragment allows you to reuse inline or external script code across all pages on your site, regardless of the template they use.</span></span>

### <a name="create-a-reusable-fragment-for-your-inline-script-code"></a><span data-ttu-id="7c0c9-111">สร้างส่วนย่อยที่สามารถใช้ซ้ำได้สำหรับรหัสสคริปต์อินไลน์ของคุณ</span><span class="sxs-lookup"><span data-stu-id="7c0c9-111">Create a reusable fragment for your inline script code</span></span>

<span data-ttu-id="7c0c9-112">เมื่อต้องการสร้างส่วนย่อยที่สามารถใช้ซ้ำได้สำหรับรหัสสคริปต์แบบอินไลน์ของคุณในโปรแกรมสร้างไซต์ ให้ทำตามขั้นตอนเหล่านี้</span><span class="sxs-lookup"><span data-stu-id="7c0c9-112">To create a reusable fragment for your inline script code in site builder, follow these steps.</span></span>

1. <span data-ttu-id="7c0c9-113">ไปที่ **ส่วนย่อย** และให้เลือก **สร้าง**</span><span class="sxs-lookup"><span data-stu-id="7c0c9-113">Go to **Fragments**, and then select **New**.</span></span>
1. <span data-ttu-id="7c0c9-114">ในกล่องโต้ตอบ **ส่วนย่อยใหม่** ให้เลือก **สคริปต์แบบอินไลน์**</span><span class="sxs-lookup"><span data-stu-id="7c0c9-114">In the **New fragment** dialog box, select **Inline script**.</span></span>
1. <span data-ttu-id="7c0c9-115">ภายใต้ **ชื่อส่วนย่อย** ให้ป้อนชื่อสำหรับส่วน และจากนั้น เลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="7c0c9-115">Under **Fragment name**, enter a name for the fragment, and then select **OK**.</span></span>
1. <span data-ttu-id="7c0c9-116">ภายใต้ส่วนย่อยที่คุณสร้างขึ้น ให้เลือกโมดูล **สคริปต์แบบอินไลน์เริ่มต้น**</span><span class="sxs-lookup"><span data-stu-id="7c0c9-116">Under the fragment that you created, select the **Default inline script** module.</span></span>
1. <span data-ttu-id="7c0c9-117">ในบานหน้าต่างคุณสมบัติทางด้านขวา ภายใต้ **สคริปต์แบบอินไลน์** ให้ป้อนสคริปต์ฝั่งไคลเอนต์ของคุณ</span><span class="sxs-lookup"><span data-stu-id="7c0c9-117">In the property pane on the right, under **Inline script**, enter your client-side script.</span></span> <span data-ttu-id="7c0c9-118">จากนั้น ตั้งค่าคอนฟิกตัวเลือกอื่นๆ ตามที่คุณต้องการ</span><span class="sxs-lookup"><span data-stu-id="7c0c9-118">Then configure other options as you require.</span></span>
1. <span data-ttu-id="7c0c9-119">เลือก **บันทึก** และจากนั้น เลือก **แก้ไขให้เสร็จสิ้น**</span><span class="sxs-lookup"><span data-stu-id="7c0c9-119">Select **Save**, and then select **Finish editing**.</span></span>
1. <span data-ttu-id="7c0c9-120">เลือก **เผยแพร่**</span><span class="sxs-lookup"><span data-stu-id="7c0c9-120">Select **Publish**.</span></span>

### <a name="create-a-reusable-fragment-for-your-external-script-code"></a><span data-ttu-id="7c0c9-121">สร้างส่วนย่อยที่สามารถใช้ซ้ำได้สำหรับรหัสสคริปต์ภายนอกของคุณ</span><span class="sxs-lookup"><span data-stu-id="7c0c9-121">Create a reusable fragment for your external script code</span></span>

<span data-ttu-id="7c0c9-122">เมื่อต้องการสร้างส่วนย่อยที่สามารถใช้ซ้ำได้สำหรับรหัสสคริปต์ภายนอกของคุณในโปรแกรมสร้างไซต์ ให้ทำตามขั้นตอนเหล่านี้</span><span class="sxs-lookup"><span data-stu-id="7c0c9-122">To create a reusable fragment for your external script code in site builder, follow these steps.</span></span>

1. <span data-ttu-id="7c0c9-123">ไปที่ **ส่วนย่อย** และให้เลือก **สร้าง**</span><span class="sxs-lookup"><span data-stu-id="7c0c9-123">Go to **Fragments**, and then select **New**.</span></span>
1. <span data-ttu-id="7c0c9-124">ในกล่องโต้ตอบ **ส่วนย่อยใหม่** ให้เลือก **สคริปต์ภายนอก**</span><span class="sxs-lookup"><span data-stu-id="7c0c9-124">In the **New fragment** dialog box, select **External script**.</span></span>
1. <span data-ttu-id="7c0c9-125">ภายใต้ **ชื่อส่วนย่อย** ให้ป้อนชื่อสำหรับส่วน และจากนั้น เลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="7c0c9-125">Under **Fragment name**, enter a name for the fragment, and then select **OK**.</span></span>
1. <span data-ttu-id="7c0c9-126">ภายใต้ส่วนย่อยที่คุณสร้างขึ้น ให้เลือกโมดูล **สคริปต์ภายนอกเริ่มต้น**</span><span class="sxs-lookup"><span data-stu-id="7c0c9-126">Under the fragment that you created, select the **Default external script** module.</span></span>
1. <span data-ttu-id="7c0c9-127">ในบานหน้าต่างคุณสมบัติทางด้านขวา ภายใต้ **แหล่งที่มาของสคริปต์** ให้เพิ่ม URL ภายนอกหรือที่เกี่ยวข้องสำหรับแหล่งที่มาของสคริปต์ภายนอก</span><span class="sxs-lookup"><span data-stu-id="7c0c9-127">In the property pane on the right, under **Script source**, add an external or relative URL for the external script source.</span></span> <span data-ttu-id="7c0c9-128">จากนั้น ตั้งค่าคอนฟิกตัวเลือกอื่นๆ ตามที่คุณต้องการ</span><span class="sxs-lookup"><span data-stu-id="7c0c9-128">Then configure other options as you require.</span></span>
1. <span data-ttu-id="7c0c9-129">เลือก **บันทึก** และจากนั้น เลือก **แก้ไขให้เสร็จสิ้น**</span><span class="sxs-lookup"><span data-stu-id="7c0c9-129">Select **Save**, and then select **Finish editing**.</span></span>
1. <span data-ttu-id="7c0c9-130">เลือก **เผยแพร่**</span><span class="sxs-lookup"><span data-stu-id="7c0c9-130">Select **Publish**.</span></span>

> [!NOTE]
> <span data-ttu-id="7c0c9-131">ถ้ามีการเปิดใช้งานนโยบายความปลอดภัยของเนื้อหา (CSP) สำหรับไซต์ของคุณ ให้ตรวจสอบให้แน่ใจว่ามีการเพิ่ม Url ภายนอกทั้งหมดลงในคำสั่ง CSP **script-src** ในตัวสร้างไซต์ Commerce</span><span class="sxs-lookup"><span data-stu-id="7c0c9-131">If content security policy (CSP) is enabled for your site, ensure that all external URLs are added to the **script-src** CSP directive in Commerce site builder.</span></span> <span data-ttu-id="7c0c9-132">สำหรับข้อมูลเพิ่มเติม ให้ดู [จัดการนโยบายความปลอดภัยของเนื้อหา (CSP)](manage-csp.md)</span><span class="sxs-lookup"><span data-stu-id="7c0c9-132">For more information, see [Manage Content Security Policy (CSP)](manage-csp.md).</span></span>

## <a name="add-a-fragment-that-includes-script-code-to-a-template"></a><span data-ttu-id="7c0c9-133">เพิ่มส่วนย่อยซึ่งรวมถึงรหัสสคริปต์ให้กับเท็มเพลต</span><span class="sxs-lookup"><span data-stu-id="7c0c9-133">Add a fragment that includes script code to a template</span></span>

<span data-ttu-id="7c0c9-134">เมื่อต้องการเพิ่มส่วนย่อยที่รวมรหัสสคริปต์ไปยังเท็มเพลตในโปรแกรมสร้างไซต์ ให้ทำตามขั้นตอนเหล่านี้</span><span class="sxs-lookup"><span data-stu-id="7c0c9-134">To add a fragment that includes script code to a template in site builder, follow these steps.</span></span>

1. <span data-ttu-id="7c0c9-135">ไปที่ **แม่แบบ** และเปิดแม่แบบสำหรับเพจที่คุณต้องการเพิ่มรหัสสคริปต์ของคุณ</span><span class="sxs-lookup"><span data-stu-id="7c0c9-135">Go to **Templates**, and open the template for the pages that you want to add your script code to.</span></span>
1. <span data-ttu-id="7c0c9-136">ในบานหน้าต่างด้านซ้าย ให้ขยายลำดับชั้นแม่แบบเพื่อแสดงช่อง **ส่วนหัวของ HTML**</span><span class="sxs-lookup"><span data-stu-id="7c0c9-136">In the left pane, expand the template hierarchy to show the **HTML Head** slot.</span></span>
1. <span data-ttu-id="7c0c9-137">ในช่อง **ส่วนหัวของ HTML** เลือก ปุ่มจุดไข่ปลา (**...**) แล้วจากนั้น เลือก **เพิ่มส่วนย่อย**</span><span class="sxs-lookup"><span data-stu-id="7c0c9-137">In the **HTML Head** slot, select the ellipsis button (**...**), and then select **Add fragment**.</span></span>
1. <span data-ttu-id="7c0c9-138">เลือกส่วนที่คุณสร้างสำหรับรหัสสคริปต์ของคุณ</span><span class="sxs-lookup"><span data-stu-id="7c0c9-138">Select the fragment that you created for your script code.</span></span>
1. <span data-ttu-id="7c0c9-139">เลือก **บันทึก** และจากนั้น เลือก **แก้ไขให้เสร็จสิ้น**</span><span class="sxs-lookup"><span data-stu-id="7c0c9-139">Select **Save**, and then select **Finish editing**.</span></span>
1. <span data-ttu-id="7c0c9-140">เลือก **เผยแพร่**</span><span class="sxs-lookup"><span data-stu-id="7c0c9-140">Select **Publish**.</span></span>

## <a name="add-an-external-script-or-inline-script-directly-to-a-template"></a><span data-ttu-id="7c0c9-141">เพิ่มสคริปต์ภายนอกหรือสคริปต์อินไลน์ไปยังเท็มเพลตโดยตรง</span><span class="sxs-lookup"><span data-stu-id="7c0c9-141">Add an external script or inline script directly to a template</span></span>

<span data-ttu-id="7c0c9-142">ถ้าคุณต้องการแทรกสคริปต์แบบอินไลน์หรือภายนอกโดยตรงลงในชุดของหน้าที่ถูกควบคุมโดยเท็มเพลตเดียว คุณไม่จำเป็นต้องสร้างส่วนย่อยก่อน</span><span class="sxs-lookup"><span data-stu-id="7c0c9-142">If you want to insert an inline or external script directly into a set of pages that are controlled by a single template, you don't have to create a fragment first.</span></span>

### <a name="add-an-inline-script-directly-to-a-template"></a><span data-ttu-id="7c0c9-143">เพิ่มสคริปต์อินไลน์ไปยังเท็มเพลตโดยตรง</span><span class="sxs-lookup"><span data-stu-id="7c0c9-143">Add an inline script directly to a template</span></span>

<span data-ttu-id="7c0c9-144">เมื่อต้องการเพิ่มสคริปต์แบบอินไลน์ให้กับเท็มเพลตในโปรแกรมสร้างไซต์โดยตรง ให้ทำตามขั้นตอนเหล่านี้</span><span class="sxs-lookup"><span data-stu-id="7c0c9-144">To add an inline script directly to a template in site builder, follow these steps.</span></span>

1. <span data-ttu-id="7c0c9-145">ไปที่ **แม่แบบ** และเปิดแม่แบบสำหรับเพจที่คุณต้องการเพิ่มรหัสสคริปต์ของคุณ</span><span class="sxs-lookup"><span data-stu-id="7c0c9-145">Go to **Templates**, and open the template for the pages that you want to add your script code to.</span></span>
1. <span data-ttu-id="7c0c9-146">ในบานหน้าต่างด้านซ้าย ให้ขยายลำดับชั้นแม่แบบเพื่อแสดงช่อง **ส่วนหัวของ HTML**</span><span class="sxs-lookup"><span data-stu-id="7c0c9-146">In the left pane, expand the template hierarchy to show the **HTML Head** slot.</span></span>
1. <span data-ttu-id="7c0c9-147">ในช่อง **ส่วนหัวของ HTML** เลือก ปุ่มจุดไข่ปลา (**...**) แล้วจากนั้น เลือก **เพิ่มโมดูล**</span><span class="sxs-lookup"><span data-stu-id="7c0c9-147">In the **HTML Head** slot, select the ellipsis button (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="7c0c9-148">ในกล่องโต้ตอบ **เพิ่มโมดูล** ให้เลือก **สคริปต์แบบอินไลน์**</span><span class="sxs-lookup"><span data-stu-id="7c0c9-148">In the **Add Module** dialog box, select **Inline script**.</span></span>
1. <span data-ttu-id="7c0c9-149">ในบานหน้าต่างคุณสมบัติทางด้านขวา ภายใต้ **สคริปต์แบบอินไลน์** ให้ป้อนสคริปต์ฝั่งไคลเอนต์ของคุณ</span><span class="sxs-lookup"><span data-stu-id="7c0c9-149">In the property pane on the right, under **Inline script**, enter your client-side script.</span></span> <span data-ttu-id="7c0c9-150">จากนั้น ตั้งค่าคอนฟิกตัวเลือกอื่นๆ ตามที่คุณต้องการ</span><span class="sxs-lookup"><span data-stu-id="7c0c9-150">Then configure other options as you require.</span></span>
1. <span data-ttu-id="7c0c9-151">เลือก **บันทึก** และจากนั้น เลือก **แก้ไขให้เสร็จสิ้น**</span><span class="sxs-lookup"><span data-stu-id="7c0c9-151">Select **Save**, and then select **Finish editing**.</span></span>
1. <span data-ttu-id="7c0c9-152">เลือก **เผยแพร่**</span><span class="sxs-lookup"><span data-stu-id="7c0c9-152">Select **Publish**.</span></span>

### <a name="add-an-external-script-directly-to-a-template"></a><span data-ttu-id="7c0c9-153">เพิ่มสคริปต์ภายนอกไปยังเท็มเพลตโดยตรง</span><span class="sxs-lookup"><span data-stu-id="7c0c9-153">Add an external script directly to a template</span></span>

<span data-ttu-id="7c0c9-154">เมื่อต้องการเพิ่มสคริปต์ภายนอกให้กับเท็มเพลตในโปรแกรมสร้างไซต์โดยตรง ให้ทำตามขั้นตอนเหล่านี้</span><span class="sxs-lookup"><span data-stu-id="7c0c9-154">To add an external script directly to a template in site builder, follow these steps.</span></span>

1. <span data-ttu-id="7c0c9-155">ไปที่ **แม่แบบ** และเปิดแม่แบบสำหรับเพจที่คุณต้องการเพิ่มรหัสสคริปต์ของคุณ</span><span class="sxs-lookup"><span data-stu-id="7c0c9-155">Go to **Templates**, and open the template for the pages that you want to add your script code to.</span></span>
1. <span data-ttu-id="7c0c9-156">ในบานหน้าต่างด้านซ้าย ให้ขยายลำดับชั้นแม่แบบเพื่อแสดงช่อง **ส่วนหัวของ HTML**</span><span class="sxs-lookup"><span data-stu-id="7c0c9-156">In the left pane, expand the template hierarchy to show the **HTML Head** slot.</span></span>
1. <span data-ttu-id="7c0c9-157">ในช่อง **ส่วนหัวของ HTML** เลือก ปุ่มจุดไข่ปลา (**...**) แล้วจากนั้น เลือก **เพิ่มโมดูล**</span><span class="sxs-lookup"><span data-stu-id="7c0c9-157">In the **HTML Head** slot, select the ellipsis button (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="7c0c9-158">ในกล่องโต้ตอบ **เพิ่มโมดูล** ให้เลือก **สคริปต์ภายนอก**</span><span class="sxs-lookup"><span data-stu-id="7c0c9-158">In the **Add Module** dialog box, select **External script**.</span></span>
1. <span data-ttu-id="7c0c9-159">ในบานหน้าต่างคุณสมบัติทางด้านขวา ภายใต้ **แหล่งที่มาของสคริปต์** ให้เพิ่ม URL ภายนอกหรือที่เกี่ยวข้องสำหรับแหล่งที่มาของสคริปต์ภายนอก</span><span class="sxs-lookup"><span data-stu-id="7c0c9-159">In the property pane on the right, under **Script source**, add an external or relative URL for the external script source.</span></span> <span data-ttu-id="7c0c9-160">จากนั้น ตั้งค่าคอนฟิกตัวเลือกอื่นๆ ตามที่คุณต้องการ</span><span class="sxs-lookup"><span data-stu-id="7c0c9-160">Then configure other options as you require.</span></span>
1. <span data-ttu-id="7c0c9-161">เลือก **บันทึก** และจากนั้น เลือก **แก้ไขให้เสร็จสิ้น**</span><span class="sxs-lookup"><span data-stu-id="7c0c9-161">Select **Save**, and then select **Finish editing**.</span></span>
1. <span data-ttu-id="7c0c9-162">เลือก **เผยแพร่**</span><span class="sxs-lookup"><span data-stu-id="7c0c9-162">Select **Publish**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="7c0c9-163">ทรัพยากรเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="7c0c9-163">Additional resources</span></span>

[<span data-ttu-id="7c0c9-164">เพิ่มโลโก้</span><span class="sxs-lookup"><span data-stu-id="7c0c9-164">Add a logo</span></span>](add-logo.md)

[<span data-ttu-id="7c0c9-165">เลือกชุดรูปแบบของไซต์</span><span class="sxs-lookup"><span data-stu-id="7c0c9-165">Select a site theme</span></span>](select-site-theme.md)

[<span data-ttu-id="7c0c9-166">ทำงานกับไฟล์การแก้ไข CSS</span><span class="sxs-lookup"><span data-stu-id="7c0c9-166">Work with CSS override files</span></span>](css-override-files.md)

[<span data-ttu-id="7c0c9-167">เพิ่มไอคอนประจำไซต์</span><span class="sxs-lookup"><span data-stu-id="7c0c9-167">Add a favicon</span></span>](add-favicon.md)

[<span data-ttu-id="7c0c9-168">เพิ่มข้อความต้อนรับ</span><span class="sxs-lookup"><span data-stu-id="7c0c9-168">Add a welcome message</span></span>](add-welcome-message.md)

[<span data-ttu-id="7c0c9-169">เพิ่มข้อความสงวนลิขสิทธิ์</span><span class="sxs-lookup"><span data-stu-id="7c0c9-169">Add a copyright notice</span></span>](add-copyright-notice.md)

[<span data-ttu-id="7c0c9-170">เพิ่มภาษาลงในไซต์ของคุณ</span><span class="sxs-lookup"><span data-stu-id="7c0c9-170">Add languages to your site</span></span>](add-languages-to-site.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
