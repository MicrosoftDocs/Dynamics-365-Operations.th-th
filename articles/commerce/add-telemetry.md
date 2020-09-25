---
title: เพิ่มโค้ดสคริปต์ให้กับหน้าไซต์เพื่อสนับสนุนการตรวจวัดระยะไกล
description: หัวข้อนี้อธิบายวิธีการเพิ่มรหัสสคริปต์ฝั่งไคลเอนต์ไปยังหน้าไซต์ของคุณ เพื่อสนับสนุนการเรียกเก็บเงินของการตรวจวัดระยะไกลฝั่งไคลเอนต์
author: bicyclingfool
manager: annbe
ms.date: 08/31/2020
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
ms.openlocfilehash: a88f4f920154aafaa15a48af67365152e21111f7
ms.sourcegitcommit: 420b9e538f706178f8e1f2786e02f4f400bf2336
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 09/02/2020
ms.locfileid: "3761260"
---
# <a name="add-script-code-to-site-pages-to-support-telemetry"></a><span data-ttu-id="2a1a4-103">เพิ่มโค้ดสคริปต์ให้กับหน้าไซต์เพื่อสนับสนุนการตรวจวัดระยะไกล</span><span class="sxs-lookup"><span data-stu-id="2a1a4-103">Add script code to site pages to support telemetry</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="2a1a4-104">หัวข้อนี้อธิบายวิธีการเพิ่มรหัสสคริปต์ฝั่งไคลเอนต์ไปยังหน้าไซต์ของคุณ เพื่อสนับสนุนการเรียกเก็บเงินของการตรวจวัดระยะไกลฝั่งไคลเอนต์</span><span class="sxs-lookup"><span data-stu-id="2a1a4-104">This topic describes how to add client-side script code to your site pages to support the collection of client-side telemetry.</span></span>

## <a name="overview"></a><span data-ttu-id="2a1a4-105">ภาพรวม</span><span class="sxs-lookup"><span data-stu-id="2a1a4-105">Overview</span></span>

<span data-ttu-id="2a1a4-106">Web analytics เป็นเครื่องมือที่จำเป็น เมื่อคุณต้องการทำความเข้าใจวิธีการที่ลูกค้าของคุณโต้ตอบกับไซต์ของคุณ และตัดสินใจที่จะช่วยปรับปรุงประสบการณ์สำหรับการแปลงสูงสุด</span><span class="sxs-lookup"><span data-stu-id="2a1a4-106">Web analytics are an essential tool when you want to understand how your customers interact with your site and make decisions that will help optimize the experience for maximum conversion.</span></span> <span data-ttu-id="2a1a4-107">แพคเกจการวิเคราะห์เว็บจำนวนมากพร้อมให้ความช่วยเหลือในการบรรลุเป้าหมายเหล่านี้ เช่น Google Analytics, Clicky, Moz Analytics และ KISSMetrics</span><span class="sxs-lookup"><span data-stu-id="2a1a4-107">Many web analytics packages are available to help you achieve these goals, such as Google Analytics, Clicky, Moz Analytics, and KISSMetrics.</span></span> <span data-ttu-id="2a1a4-108">แพคเกจการวิเคราะห์เว็บส่วนใหญ่กำหนดให้คุณต้องเพิ่มรหัสสคริปต์ฝั่งไคลเอนต์ในองค์ประกอบที่เป็น **\<head\>** ของ HTML สำหรับทุกเพจของไซต์ของคุณ</span><span class="sxs-lookup"><span data-stu-id="2a1a4-108">Most web analytics packages require that you add client-side script code in the **\<head\>** element of the HTML for all pages of your site.</span></span>

> [!NOTE]
> <span data-ttu-id="2a1a4-109">คำแนะนำในหัวข้อนี้จะใช้กับฟังก์ชันฝั่งไคลเอนต์แบบกำหนดเองอื่นๆ ที่ Microsoft Dynamics 365 Commerce ไม่มีข้อเสนอโดยไม่ได้กล่าวถึง</span><span class="sxs-lookup"><span data-stu-id="2a1a4-109">The instructions in this topic also apply to other custom client-side functionality that Microsoft Dynamics 365 Commerce doesn't natively offer.</span></span>

## <a name="create-a-reusable-fragment-for-your-script-code"></a><span data-ttu-id="2a1a4-110">สร้างส่วนที่สามารถใช้ซ้ำได้สำหรับรหัสสคริปต์ของคุณ</span><span class="sxs-lookup"><span data-stu-id="2a1a4-110">Create a reusable fragment for your script code</span></span>

<span data-ttu-id="2a1a4-111">ส่วนย่อยจะช่วยให้คุณสามารถนำสคริปต์อินไลน์หรือภายนอกมาใช้ใหม่ผ่านหน้าทั้งหมดบนไซต์ของคุณได้ โดยไม่ต้องใช้เท็มเพลตที่มีการใช้</span><span class="sxs-lookup"><span data-stu-id="2a1a4-111">A fragment allows you to reuse inline or external script code across all pages on your site, regardless of the template they use.</span></span>

### <a name="create-a-reusable-fragment-for-your-inline-script-code"></a><span data-ttu-id="2a1a4-112">สร้างส่วนย่อยที่สามารถใช้ซ้ำได้สำหรับรหัสสคริปต์อินไลน์ของคุณ</span><span class="sxs-lookup"><span data-stu-id="2a1a4-112">Create a reusable fragment for your inline script code</span></span>

<span data-ttu-id="2a1a4-113">เมื่อต้องการสร้างส่วนย่อยที่สามารถใช้ซ้ำได้สำหรับรหัสสคริปต์แบบอินไลน์ของคุณในโปรแกรมสร้างไซต์ ให้ทำตามขั้นตอนเหล่านี้</span><span class="sxs-lookup"><span data-stu-id="2a1a4-113">To create a reusable fragment for your inline script code in site builder, follow these steps.</span></span>

1. <span data-ttu-id="2a1a4-114">ไปที่ **ส่วนย่อย** และให้เลือก **สร้าง**</span><span class="sxs-lookup"><span data-stu-id="2a1a4-114">Go to **Fragments**, and then select **New**.</span></span>
1. <span data-ttu-id="2a1a4-115">ในกล่องโต้ตอบ **ส่วนย่อยใหม่** ให้เลือก **สคริปต์แบบอินไลน์**</span><span class="sxs-lookup"><span data-stu-id="2a1a4-115">In the **New fragment** dialog box, select **Inline script**.</span></span>
1. <span data-ttu-id="2a1a4-116">ภายใต้ **ชื่อส่วนย่อย** ให้ป้อนชื่อสำหรับส่วน และจากนั้น เลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="2a1a4-116">Under **Fragment name**, enter a name for the fragment, and then select **OK**.</span></span>
1. <span data-ttu-id="2a1a4-117">ภายใต้ส่วนย่อยที่คุณสร้างขึ้น ให้เลือกโมดูล **สคริปต์แบบอินไลน์เริ่มต้น**</span><span class="sxs-lookup"><span data-stu-id="2a1a4-117">Under the fragment that you created, select the **Default inline script** module.</span></span>
1. <span data-ttu-id="2a1a4-118">ในบานหน้าต่างคุณสมบัติทางด้านขวา ภายใต้ **สคริปต์แบบอินไลน์** ให้ป้อนสคริปต์ฝั่งไคลเอนต์ของคุณ</span><span class="sxs-lookup"><span data-stu-id="2a1a4-118">In the property pane on the right, under **Inline script**, enter your client-side script.</span></span> <span data-ttu-id="2a1a4-119">จากนั้น ตั้งค่าคอนฟิกตัวเลือกอื่นๆ ตามที่คุณต้องการ</span><span class="sxs-lookup"><span data-stu-id="2a1a4-119">Then configure other options as you require.</span></span>
1. <span data-ttu-id="2a1a4-120">เลือก **บันทึก** และจากนั้น เลือก **แก้ไขให้เสร็จสิ้น**</span><span class="sxs-lookup"><span data-stu-id="2a1a4-120">Select **Save**, and then select **Finish editing**.</span></span>
1. <span data-ttu-id="2a1a4-121">เลือก **เผยแพร่**</span><span class="sxs-lookup"><span data-stu-id="2a1a4-121">Select **Publish**.</span></span>

### <a name="create-a-reusable-fragment-for-your-external-script-code"></a><span data-ttu-id="2a1a4-122">สร้างส่วนย่อยที่สามารถใช้ซ้ำได้สำหรับรหัสสคริปต์ภายนอกของคุณ</span><span class="sxs-lookup"><span data-stu-id="2a1a4-122">Create a reusable fragment for your external script code</span></span>

<span data-ttu-id="2a1a4-123">เมื่อต้องการสร้างส่วนย่อยที่สามารถใช้ซ้ำได้สำหรับรหัสสคริปต์ภายนอกของคุณในโปรแกรมสร้างไซต์ ให้ทำตามขั้นตอนเหล่านี้</span><span class="sxs-lookup"><span data-stu-id="2a1a4-123">To create a reusable fragment for your external script code in site builder, follow these steps.</span></span>

1. <span data-ttu-id="2a1a4-124">ไปที่ **ส่วนย่อย** และให้เลือก **สร้าง**</span><span class="sxs-lookup"><span data-stu-id="2a1a4-124">Go to **Fragments**, and then select **New**.</span></span>
1. <span data-ttu-id="2a1a4-125">ในกล่องโต้ตอบ **ส่วนย่อยใหม่** ให้เลือก **สคริปต์ภายนอก**</span><span class="sxs-lookup"><span data-stu-id="2a1a4-125">In the **New fragment** dialog box, select **External script**.</span></span>
1. <span data-ttu-id="2a1a4-126">ภายใต้ **ชื่อส่วนย่อย** ให้ป้อนชื่อสำหรับส่วน และจากนั้น เลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="2a1a4-126">Under **Fragment name**, enter a name for the fragment, and then select **OK**.</span></span>
1. <span data-ttu-id="2a1a4-127">ภายใต้ส่วนย่อยที่คุณสร้างขึ้น ให้เลือกโมดูล **สคริปต์ภายนอกเริ่มต้น**</span><span class="sxs-lookup"><span data-stu-id="2a1a4-127">Under the fragment that you created, select the **Default external script** module.</span></span>
1. <span data-ttu-id="2a1a4-128">ในบานหน้าต่างคุณสมบัติทางด้านขวา ภายใต้ **แหล่งที่มาของสคริปต์** ให้เพิ่ม URL ภายนอกหรือที่เกี่ยวข้องสำหรับแหล่งที่มาของสคริปต์ภายนอก</span><span class="sxs-lookup"><span data-stu-id="2a1a4-128">In the property pane on the right, under **Script source**, add an external or relative URL for the external script source.</span></span> <span data-ttu-id="2a1a4-129">จากนั้น ตั้งค่าคอนฟิกตัวเลือกอื่นๆ ตามที่คุณต้องการ</span><span class="sxs-lookup"><span data-stu-id="2a1a4-129">Then configure other options as you require.</span></span>
1. <span data-ttu-id="2a1a4-130">เลือก **บันทึก** และจากนั้น เลือก **แก้ไขให้เสร็จสิ้น**</span><span class="sxs-lookup"><span data-stu-id="2a1a4-130">Select **Save**, and then select **Finish editing**.</span></span>
1. <span data-ttu-id="2a1a4-131">เลือก **เผยแพร่**</span><span class="sxs-lookup"><span data-stu-id="2a1a4-131">Select **Publish**.</span></span>

## <a name="add-a-fragment-that-includes-script-code-to-a-template"></a><span data-ttu-id="2a1a4-132">เพิ่มส่วนย่อยซึ่งรวมถึงรหัสสคริปต์ให้กับเท็มเพลต</span><span class="sxs-lookup"><span data-stu-id="2a1a4-132">Add a fragment that includes script code to a template</span></span>

<span data-ttu-id="2a1a4-133">เมื่อต้องการเพิ่มส่วนย่อยที่รวมรหัสสคริปต์ไปยังเท็มเพลตในโปรแกรมสร้างไซต์ ให้ทำตามขั้นตอนเหล่านี้</span><span class="sxs-lookup"><span data-stu-id="2a1a4-133">To add a fragment that includes script code to a template in site builder, follow these steps.</span></span>

1. <span data-ttu-id="2a1a4-134">ไปที่ **แม่แบบ** และเปิดแม่แบบสำหรับเพจที่คุณต้องการเพิ่มรหัสสคริปต์ของคุณ</span><span class="sxs-lookup"><span data-stu-id="2a1a4-134">Go to **Templates**, and open the template for the pages that you want to add your script code to.</span></span>
1. <span data-ttu-id="2a1a4-135">ในบานหน้าต่างด้านซ้าย ให้ขยายลำดับชั้นแม่แบบเพื่อแสดงช่อง **ส่วนหัวของ HTML**</span><span class="sxs-lookup"><span data-stu-id="2a1a4-135">In the left pane, expand the template hierarchy to show the **HTML Head** slot.</span></span>
1. <span data-ttu-id="2a1a4-136">ในช่อง**ส่วนหัวของ HTML** เลือก ปุ่มจุดไข่ปลา (**...**) แล้วจากนั้น เลือก **เพิ่มส่วนย่อย**</span><span class="sxs-lookup"><span data-stu-id="2a1a4-136">In the **HTML Head** slot, select the ellipsis button (**...**), and then select **Add fragment**.</span></span>
1. <span data-ttu-id="2a1a4-137">เลือกส่วนที่คุณสร้างสำหรับรหัสสคริปต์ของคุณ</span><span class="sxs-lookup"><span data-stu-id="2a1a4-137">Select the fragment that you created for your script code.</span></span>
1. <span data-ttu-id="2a1a4-138">เลือก **บันทึก** และจากนั้น เลือก **แก้ไขให้เสร็จสิ้น**</span><span class="sxs-lookup"><span data-stu-id="2a1a4-138">Select **Save**, and then select **Finish editing**.</span></span>
1. <span data-ttu-id="2a1a4-139">เลือก **เผยแพร่**</span><span class="sxs-lookup"><span data-stu-id="2a1a4-139">Select **Publish**.</span></span>

## <a name="add-an-external-script-or-inline-script-directly-to-a-template"></a><span data-ttu-id="2a1a4-140">เพิ่มสคริปต์ภายนอกหรือสคริปต์อินไลน์ไปยังเท็มเพลตโดยตรง</span><span class="sxs-lookup"><span data-stu-id="2a1a4-140">Add an external script or inline script directly to a template</span></span>

<span data-ttu-id="2a1a4-141">ถ้าคุณต้องการแทรกสคริปต์แบบอินไลน์หรือภายนอกโดยตรงลงในชุดของหน้าที่ถูกควบคุมโดยเท็มเพลตเดียว คุณไม่จำเป็นต้องสร้างส่วนย่อยก่อน</span><span class="sxs-lookup"><span data-stu-id="2a1a4-141">If you want to insert an inline or external script directly into a set of pages that are controlled by a single template, you don't have to create a fragment first.</span></span>

### <a name="add-an-inline-script-directly-to-a-template"></a><span data-ttu-id="2a1a4-142">เพิ่มสคริปต์อินไลน์ไปยังเท็มเพลตโดยตรง</span><span class="sxs-lookup"><span data-stu-id="2a1a4-142">Add an inline script directly to a template</span></span>

<span data-ttu-id="2a1a4-143">เมื่อต้องการเพิ่มสคริปต์แบบอินไลน์ให้กับเท็มเพลตในโปรแกรมสร้างไซต์โดยตรง ให้ทำตามขั้นตอนเหล่านี้</span><span class="sxs-lookup"><span data-stu-id="2a1a4-143">To add an inline script directly to a template in site builder, follow these steps.</span></span>

1. <span data-ttu-id="2a1a4-144">ไปที่ **แม่แบบ** และเปิดแม่แบบสำหรับเพจที่คุณต้องการเพิ่มรหัสสคริปต์ของคุณ</span><span class="sxs-lookup"><span data-stu-id="2a1a4-144">Go to **Templates**, and open the template for the pages that you want to add your script code to.</span></span>
1. <span data-ttu-id="2a1a4-145">ในบานหน้าต่างด้านซ้าย ให้ขยายลำดับชั้นแม่แบบเพื่อแสดงช่อง **ส่วนหัวของ HTML**</span><span class="sxs-lookup"><span data-stu-id="2a1a4-145">In the left pane, expand the template hierarchy to show the **HTML Head** slot.</span></span>
1. <span data-ttu-id="2a1a4-146">ในช่อง **ส่วนหัวของ HTML** เลือก ปุ่มจุดไข่ปลา (**...**) แล้วจากนั้น เลือก **เพิ่มโมดูล**</span><span class="sxs-lookup"><span data-stu-id="2a1a4-146">In the **HTML Head** slot, select the ellipsis button (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="2a1a4-147">ในกล่องโต้ตอบ **เพิ่มโมดูล** ให้เลือก **สคริปต์แบบอินไลน์**</span><span class="sxs-lookup"><span data-stu-id="2a1a4-147">In the **Add Module** dialog box, select **Inline script**.</span></span>
1. <span data-ttu-id="2a1a4-148">ในบานหน้าต่างคุณสมบัติทางด้านขวา ภายใต้ **สคริปต์แบบอินไลน์** ให้ป้อนสคริปต์ฝั่งไคลเอนต์ของคุณ</span><span class="sxs-lookup"><span data-stu-id="2a1a4-148">In the property pane on the right, under **Inline script**, enter your client-side script.</span></span> <span data-ttu-id="2a1a4-149">จากนั้น ตั้งค่าคอนฟิกตัวเลือกอื่นๆ ตามที่คุณต้องการ</span><span class="sxs-lookup"><span data-stu-id="2a1a4-149">Then configure other options as you require.</span></span>
1. <span data-ttu-id="2a1a4-150">เลือก **บันทึก** และจากนั้น เลือก **แก้ไขให้เสร็จสิ้น**</span><span class="sxs-lookup"><span data-stu-id="2a1a4-150">Select **Save**, and then select **Finish editing**.</span></span>
1. <span data-ttu-id="2a1a4-151">เลือก **เผยแพร่**</span><span class="sxs-lookup"><span data-stu-id="2a1a4-151">Select **Publish**.</span></span>

### <a name="add-an-external-script-directly-to-a-template"></a><span data-ttu-id="2a1a4-152">เพิ่มสคริปต์ภายนอกไปยังเท็มเพลตโดยตรง</span><span class="sxs-lookup"><span data-stu-id="2a1a4-152">Add an external script directly to a template</span></span>

<span data-ttu-id="2a1a4-153">เมื่อต้องการเพิ่มสคริปต์ภายนอกให้กับเท็มเพลตในโปรแกรมสร้างไซต์โดยตรง ให้ทำตามขั้นตอนเหล่านี้</span><span class="sxs-lookup"><span data-stu-id="2a1a4-153">To add an external script directly to a template in site builder, follow these steps.</span></span>

1. <span data-ttu-id="2a1a4-154">ไปที่ **แม่แบบ** และเปิดแม่แบบสำหรับเพจที่คุณต้องการเพิ่มรหัสสคริปต์ของคุณ</span><span class="sxs-lookup"><span data-stu-id="2a1a4-154">Go to **Templates**, and open the template for the pages that you want to add your script code to.</span></span>
1. <span data-ttu-id="2a1a4-155">ในบานหน้าต่างด้านซ้าย ให้ขยายลำดับชั้นแม่แบบเพื่อแสดงช่อง **ส่วนหัวของ HTML**</span><span class="sxs-lookup"><span data-stu-id="2a1a4-155">In the left pane, expand the template hierarchy to show the **HTML Head** slot.</span></span>
1. <span data-ttu-id="2a1a4-156">ในช่อง **ส่วนหัวของ HTML** เลือก ปุ่มจุดไข่ปลา (**...**) แล้วจากนั้น เลือก **เพิ่มโมดูล**</span><span class="sxs-lookup"><span data-stu-id="2a1a4-156">In the **HTML Head** slot, select the ellipsis button (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="2a1a4-157">ในกล่องโต้ตอบ **เพิ่มโมดูล** ให้เลือก **สคริปต์ภายนอก**</span><span class="sxs-lookup"><span data-stu-id="2a1a4-157">In the **Add Module** dialog box, select **External script**.</span></span>
1. <span data-ttu-id="2a1a4-158">ในบานหน้าต่างคุณสมบัติทางด้านขวา ภายใต้ **แหล่งที่มาของสคริปต์** ให้เพิ่ม URL ภายนอกหรือที่เกี่ยวข้องสำหรับแหล่งที่มาของสคริปต์ภายนอก</span><span class="sxs-lookup"><span data-stu-id="2a1a4-158">In the property pane on the right, under **Script source**, add an external or relative URL for the external script source.</span></span> <span data-ttu-id="2a1a4-159">จากนั้น ตั้งค่าคอนฟิกตัวเลือกอื่นๆ ตามที่คุณต้องการ</span><span class="sxs-lookup"><span data-stu-id="2a1a4-159">Then configure other options as you require.</span></span>
1. <span data-ttu-id="2a1a4-160">เลือก **บันทึก** และจากนั้น เลือก **แก้ไขให้เสร็จสิ้น**</span><span class="sxs-lookup"><span data-stu-id="2a1a4-160">Select **Save**, and then select **Finish editing**.</span></span>
1. <span data-ttu-id="2a1a4-161">เลือก **เผยแพร่**</span><span class="sxs-lookup"><span data-stu-id="2a1a4-161">Select **Publish**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="2a1a4-162">ทรัพยากรเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="2a1a4-162">Additional resources</span></span>

[<span data-ttu-id="2a1a4-163">เพิ่มโลโก้</span><span class="sxs-lookup"><span data-stu-id="2a1a4-163">Add a logo</span></span>](add-logo.md)

[<span data-ttu-id="2a1a4-164">เลือกชุดรูปแบบของไซต์</span><span class="sxs-lookup"><span data-stu-id="2a1a4-164">Select a site theme</span></span>](select-site-theme.md)

[<span data-ttu-id="2a1a4-165">ทำงานกับไฟล์การแก้ไข CSS</span><span class="sxs-lookup"><span data-stu-id="2a1a4-165">Work with CSS override files</span></span>](css-override-files.md)

[<span data-ttu-id="2a1a4-166">เพิ่มไอคอนประจำไซต์</span><span class="sxs-lookup"><span data-stu-id="2a1a4-166">Add a favicon</span></span>](add-favicon.md)

[<span data-ttu-id="2a1a4-167">เพิ่มข้อความต้อนรับ</span><span class="sxs-lookup"><span data-stu-id="2a1a4-167">Add a welcome message</span></span>](add-welcome-message.md)

[<span data-ttu-id="2a1a4-168">เพิ่มข้อความสงวนลิขสิทธิ์</span><span class="sxs-lookup"><span data-stu-id="2a1a4-168">Add a copyright notice</span></span>](add-copyright-notice.md)

[<span data-ttu-id="2a1a4-169">เพิ่มภาษาลงในไซต์ของคุณ</span><span class="sxs-lookup"><span data-stu-id="2a1a4-169">Add languages to your site</span></span>](add-languages-to-site.md)
