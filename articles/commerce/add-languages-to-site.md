---
title: เพิ่มภาษาลงในไซต์ของคุณ
description: หัวข้อนี้อธิบายถึงวิธีการเพิ่มการสนับสนุนสำหรับภาษาเพิ่มเติมให้กับไซต์ Microsoft Dynamics 365 Commerce
author: bicyclingfool
manager: annbe
ms.date: 12/12/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: StuHarg
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: fa3029387d5f1ca605fc9559c4272c8dfebcddaf
ms.sourcegitcommit: 81a647904dd305c4be2e4b683689f128548a872d
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 02/01/2020
ms.locfileid: "3001426"
---
# <a name="add-languages-to-your-site"></a><span data-ttu-id="d7c8b-103">เพิ่มภาษาลงในไซต์ของคุณ</span><span class="sxs-lookup"><span data-stu-id="d7c8b-103">Add languages to your site</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="d7c8b-104">หัวข้อนี้อธิบายถึงวิธีการเพิ่มการสนับสนุนสำหรับภาษาเพิ่มเติมให้กับไซต์ Microsoft Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="d7c8b-104">This topic explains how to add support for additional languages to a Microsoft Dynamics 365 Commerce site.</span></span>

## <a name="overview"></a><span data-ttu-id="d7c8b-105">ภาพรวม</span><span class="sxs-lookup"><span data-stu-id="d7c8b-105">Overview</span></span>

<span data-ttu-id="d7c8b-106">คุณสามารถแปลเว็บไซต์ของคุณเป็นภาษาใดก็ได้ที่ Commerce สนับสนุน</span><span class="sxs-lookup"><span data-stu-id="d7c8b-106">You can localize your website into any language that Commerce supports.</span></span> <span data-ttu-id="d7c8b-107">(รายการภาษาที่สนับสนุนจะปรากฏในภายหลังในหัวข้อนี้) เมื่อต้องการเพิ่มภาษาบนเว็บไซต์ของคุณ คุณต้องเพิ่มภาษานั้นในร้านค้าออนไลน์ที่ผูกกับไซต์ของคุณก่อน</span><span class="sxs-lookup"><span data-stu-id="d7c8b-107">(The list of supported languages appears later in this topic.) To add a language on your website, you must first add it to an online store that is bound to your site.</span></span>

## <a name="add-a-language-to-an-online-store"></a><span data-ttu-id="d7c8b-108">เพิ่มภาษาลงในร้านค้าออนไลน์</span><span class="sxs-lookup"><span data-stu-id="d7c8b-108">Add a language to an online store</span></span>

<span data-ttu-id="d7c8b-109">ในการเพิ่มภาษาในร้านค้าออนไลน์ ให้ทำตามขั้นตอนเหล่านี้</span><span class="sxs-lookup"><span data-stu-id="d7c8b-109">To add a language to an online store, follow these steps.</span></span>

1. <span data-ttu-id="d7c8b-110">เปิดสภาพแวดล้อม Dynamics 365 Commerce สำหรับไซต์ของคุณ</span><span class="sxs-lookup"><span data-stu-id="d7c8b-110">Open the Dynamics 365 Commerce environment for your site.</span></span>
1. <span data-ttu-id="d7c8b-111">ไปที่ **Retail และ Commerce \> ช่องทาง \> ร้านค้าออนไลน์** เพื่อเข้าถึงรายการร้านค้าออนไลน์ที่ได้รับการตั้งค่าคอนฟิกสำหรับสภาพแวดล้อมของคุณ</span><span class="sxs-lookup"><span data-stu-id="d7c8b-111">Go to **Retail and Commerce \> Channels \> Online stores** to access the list of online stores that are configured for your environment.</span></span> <span data-ttu-id="d7c8b-112">หรือ ป้อน **ร้านค้าออนไลน์** เป็นคำที่ใช้ค้นหา</span><span class="sxs-lookup"><span data-stu-id="d7c8b-112">Alternatively, enter **online stores** as a search term.</span></span>
1. <span data-ttu-id="d7c8b-113">เลือกร้านค้าออนไลน์เพื่อเพิ่มภาษา</span><span class="sxs-lookup"><span data-stu-id="d7c8b-113">Select the online store to add a language for.</span></span>
1. <span data-ttu-id="d7c8b-114">บนแท็บด่วน **ภาษา** ให้เลือก **เพิ่ม**</span><span class="sxs-lookup"><span data-stu-id="d7c8b-114">On the **Languages** FastTab, select **Add**.</span></span>
1. <span data-ttu-id="d7c8b-115">ในฟิลด์ **ภาษา** เลือกภาษาที่จะเพิ่ม</span><span class="sxs-lookup"><span data-stu-id="d7c8b-115">In the **Language** field, select the language to add.</span></span>

<span data-ttu-id="d7c8b-116">ในขณะนี้ภาษาที่คุณเพิ่มจะพร้อมใช้งาน เพื่อให้คุณสามารถตั้งค่าคอนฟิกไซต์ของคุณเพื่อใช้งานในสภาพแวดล้อมการสร้างไซต์</span><span class="sxs-lookup"><span data-stu-id="d7c8b-116">The language that you added will now be available so that you can configure your site to use it in the site authoring environment.</span></span>

### <a name="languages-that-are-supported-by-dynamics-365-commerce"></a><span data-ttu-id="d7c8b-117">ภาษาที่ได้รับการสนับสนุนโดย Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="d7c8b-117">Languages that are supported by Dynamics 365 Commerce</span></span>

- <span data-ttu-id="d7c8b-118">af</span><span class="sxs-lookup"><span data-stu-id="d7c8b-118">af</span></span>
- <span data-ttu-id="d7c8b-119">ar</span><span class="sxs-lookup"><span data-stu-id="d7c8b-119">ar</span></span>
- <span data-ttu-id="d7c8b-120">ar-ae</span><span class="sxs-lookup"><span data-stu-id="d7c8b-120">ar-ae</span></span>
- <span data-ttu-id="d7c8b-121">ar-bh</span><span class="sxs-lookup"><span data-stu-id="d7c8b-121">ar-bh</span></span>
- <span data-ttu-id="d7c8b-122">ar-dz</span><span class="sxs-lookup"><span data-stu-id="d7c8b-122">ar-dz</span></span>
- <span data-ttu-id="d7c8b-123">ar-eg</span><span class="sxs-lookup"><span data-stu-id="d7c8b-123">ar-eg</span></span>
- <span data-ttu-id="d7c8b-124">ar-iq</span><span class="sxs-lookup"><span data-stu-id="d7c8b-124">ar-iq</span></span>
- <span data-ttu-id="d7c8b-125">ar-jo</span><span class="sxs-lookup"><span data-stu-id="d7c8b-125">ar-jo</span></span>
- <span data-ttu-id="d7c8b-126">ar-kw</span><span class="sxs-lookup"><span data-stu-id="d7c8b-126">ar-kw</span></span>
- <span data-ttu-id="d7c8b-127">ar-lb</span><span class="sxs-lookup"><span data-stu-id="d7c8b-127">ar-lb</span></span>
- <span data-ttu-id="d7c8b-128">ar-ly</span><span class="sxs-lookup"><span data-stu-id="d7c8b-128">ar-ly</span></span>
- <span data-ttu-id="d7c8b-129">ar-ma</span><span class="sxs-lookup"><span data-stu-id="d7c8b-129">ar-ma</span></span>
- <span data-ttu-id="d7c8b-130">ar-om</span><span class="sxs-lookup"><span data-stu-id="d7c8b-130">ar-om</span></span>
- <span data-ttu-id="d7c8b-131">ar-qa</span><span class="sxs-lookup"><span data-stu-id="d7c8b-131">ar-qa</span></span>
- <span data-ttu-id="d7c8b-132">ar-sa</span><span class="sxs-lookup"><span data-stu-id="d7c8b-132">ar-sa</span></span>
- <span data-ttu-id="d7c8b-133">ar-sy</span><span class="sxs-lookup"><span data-stu-id="d7c8b-133">ar-sy</span></span>
- <span data-ttu-id="d7c8b-134">ar-tn</span><span class="sxs-lookup"><span data-stu-id="d7c8b-134">ar-tn</span></span>
- <span data-ttu-id="d7c8b-135">ar-ye</span><span class="sxs-lookup"><span data-stu-id="d7c8b-135">ar-ye</span></span>
- <span data-ttu-id="d7c8b-136">be</span><span class="sxs-lookup"><span data-stu-id="d7c8b-136">be</span></span>
- <span data-ttu-id="d7c8b-137">bg</span><span class="sxs-lookup"><span data-stu-id="d7c8b-137">bg</span></span>
- <span data-ttu-id="d7c8b-138">ca</span><span class="sxs-lookup"><span data-stu-id="d7c8b-138">ca</span></span>
- <span data-ttu-id="d7c8b-139">cs</span><span class="sxs-lookup"><span data-stu-id="d7c8b-139">cs</span></span>
- <span data-ttu-id="d7c8b-140">da</span><span class="sxs-lookup"><span data-stu-id="d7c8b-140">da</span></span>
- <span data-ttu-id="d7c8b-141">de</span><span class="sxs-lookup"><span data-stu-id="d7c8b-141">de</span></span>
- <span data-ttu-id="d7c8b-142">de-at</span><span class="sxs-lookup"><span data-stu-id="d7c8b-142">de-at</span></span>
- <span data-ttu-id="d7c8b-143">de-ch</span><span class="sxs-lookup"><span data-stu-id="d7c8b-143">de-ch</span></span>
- <span data-ttu-id="d7c8b-144">de-li</span><span class="sxs-lookup"><span data-stu-id="d7c8b-144">de-li</span></span>
- <span data-ttu-id="d7c8b-145">de-lu</span><span class="sxs-lookup"><span data-stu-id="d7c8b-145">de-lu</span></span>
- <span data-ttu-id="d7c8b-146">el</span><span class="sxs-lookup"><span data-stu-id="d7c8b-146">el</span></span>
- <span data-ttu-id="d7c8b-147">en-029</span><span class="sxs-lookup"><span data-stu-id="d7c8b-147">en-029</span></span>
- <span data-ttu-id="d7c8b-148">en-au</span><span class="sxs-lookup"><span data-stu-id="d7c8b-148">en-au</span></span>
- <span data-ttu-id="d7c8b-149">en-bz</span><span class="sxs-lookup"><span data-stu-id="d7c8b-149">en-bz</span></span>
- <span data-ttu-id="d7c8b-150">en-ca</span><span class="sxs-lookup"><span data-stu-id="d7c8b-150">en-ca</span></span>
- <span data-ttu-id="d7c8b-151">en-gb</span><span class="sxs-lookup"><span data-stu-id="d7c8b-151">en-gb</span></span>
- <span data-ttu-id="d7c8b-152">en-ie</span><span class="sxs-lookup"><span data-stu-id="d7c8b-152">en-ie</span></span>
- <span data-ttu-id="d7c8b-153">en-in</span><span class="sxs-lookup"><span data-stu-id="d7c8b-153">en-in</span></span>
- <span data-ttu-id="d7c8b-154">en-jm</span><span class="sxs-lookup"><span data-stu-id="d7c8b-154">en-jm</span></span>
- <span data-ttu-id="d7c8b-155">en-my</span><span class="sxs-lookup"><span data-stu-id="d7c8b-155">en-my</span></span>
- <span data-ttu-id="d7c8b-156">en-nz</span><span class="sxs-lookup"><span data-stu-id="d7c8b-156">en-nz</span></span>
- <span data-ttu-id="d7c8b-157">en-sg</span><span class="sxs-lookup"><span data-stu-id="d7c8b-157">en-sg</span></span>
- <span data-ttu-id="d7c8b-158">en-tt</span><span class="sxs-lookup"><span data-stu-id="d7c8b-158">en-tt</span></span>
- <span data-ttu-id="d7c8b-159">th</span><span class="sxs-lookup"><span data-stu-id="d7c8b-159">en-us</span></span>
- <span data-ttu-id="d7c8b-160">en-za</span><span class="sxs-lookup"><span data-stu-id="d7c8b-160">en-za</span></span>
- <span data-ttu-id="d7c8b-161">es</span><span class="sxs-lookup"><span data-stu-id="d7c8b-161">es</span></span>
- <span data-ttu-id="d7c8b-162">es-ar</span><span class="sxs-lookup"><span data-stu-id="d7c8b-162">es-ar</span></span>
- <span data-ttu-id="d7c8b-163">es-bo</span><span class="sxs-lookup"><span data-stu-id="d7c8b-163">es-bo</span></span>
- <span data-ttu-id="d7c8b-164">es-cl</span><span class="sxs-lookup"><span data-stu-id="d7c8b-164">es-cl</span></span>
- <span data-ttu-id="d7c8b-165">es-co</span><span class="sxs-lookup"><span data-stu-id="d7c8b-165">es-co</span></span>
- <span data-ttu-id="d7c8b-166">es-cr</span><span class="sxs-lookup"><span data-stu-id="d7c8b-166">es-cr</span></span>
- <span data-ttu-id="d7c8b-167">es-do</span><span class="sxs-lookup"><span data-stu-id="d7c8b-167">es-do</span></span>
- <span data-ttu-id="d7c8b-168">es-ec</span><span class="sxs-lookup"><span data-stu-id="d7c8b-168">es-ec</span></span>
- <span data-ttu-id="d7c8b-169">es-gt</span><span class="sxs-lookup"><span data-stu-id="d7c8b-169">es-gt</span></span>
- <span data-ttu-id="d7c8b-170">es-hn</span><span class="sxs-lookup"><span data-stu-id="d7c8b-170">es-hn</span></span>
- <span data-ttu-id="d7c8b-171">es-mx</span><span class="sxs-lookup"><span data-stu-id="d7c8b-171">es-mx</span></span>
- <span data-ttu-id="d7c8b-172">es-ni</span><span class="sxs-lookup"><span data-stu-id="d7c8b-172">es-ni</span></span>
- <span data-ttu-id="d7c8b-173">es-pa</span><span class="sxs-lookup"><span data-stu-id="d7c8b-173">es-pa</span></span>
- <span data-ttu-id="d7c8b-174">es-pe</span><span class="sxs-lookup"><span data-stu-id="d7c8b-174">es-pe</span></span>
- <span data-ttu-id="d7c8b-175">es-pr</span><span class="sxs-lookup"><span data-stu-id="d7c8b-175">es-pr</span></span>
- <span data-ttu-id="d7c8b-176">es-py</span><span class="sxs-lookup"><span data-stu-id="d7c8b-176">es-py</span></span>
- <span data-ttu-id="d7c8b-177">es-sv</span><span class="sxs-lookup"><span data-stu-id="d7c8b-177">es-sv</span></span>
- <span data-ttu-id="d7c8b-178">es-tr</span><span class="sxs-lookup"><span data-stu-id="d7c8b-178">es-tr</span></span>
- <span data-ttu-id="d7c8b-179">es-uy</span><span class="sxs-lookup"><span data-stu-id="d7c8b-179">es-uy</span></span>
- <span data-ttu-id="d7c8b-180">es-ve</span><span class="sxs-lookup"><span data-stu-id="d7c8b-180">es-ve</span></span>
- <span data-ttu-id="d7c8b-181">et</span><span class="sxs-lookup"><span data-stu-id="d7c8b-181">et</span></span>
- <span data-ttu-id="d7c8b-182">eu</span><span class="sxs-lookup"><span data-stu-id="d7c8b-182">eu</span></span>
- <span data-ttu-id="d7c8b-183">fa</span><span class="sxs-lookup"><span data-stu-id="d7c8b-183">fa</span></span>
- <span data-ttu-id="d7c8b-184">fi</span><span class="sxs-lookup"><span data-stu-id="d7c8b-184">fi</span></span>
- <span data-ttu-id="d7c8b-185">fo</span><span class="sxs-lookup"><span data-stu-id="d7c8b-185">fo</span></span>
- <span data-ttu-id="d7c8b-186">fr</span><span class="sxs-lookup"><span data-stu-id="d7c8b-186">fr</span></span>
- <span data-ttu-id="d7c8b-187">fr-be</span><span class="sxs-lookup"><span data-stu-id="d7c8b-187">fr-be</span></span>
- <span data-ttu-id="d7c8b-188">fr-ca</span><span class="sxs-lookup"><span data-stu-id="d7c8b-188">fr-ca</span></span>
- <span data-ttu-id="d7c8b-189">fr-ch</span><span class="sxs-lookup"><span data-stu-id="d7c8b-189">fr-ch</span></span>
- <span data-ttu-id="d7c8b-190">fr-lu</span><span class="sxs-lookup"><span data-stu-id="d7c8b-190">fr-lu</span></span>
- <span data-ttu-id="d7c8b-191">hi</span><span class="sxs-lookup"><span data-stu-id="d7c8b-191">hi</span></span>
- <span data-ttu-id="d7c8b-192">ชั่วโมง</span><span class="sxs-lookup"><span data-stu-id="d7c8b-192">hr</span></span>
- <span data-ttu-id="d7c8b-193">hu</span><span class="sxs-lookup"><span data-stu-id="d7c8b-193">hu</span></span>
- <span data-ttu-id="d7c8b-194">อยู่</span><span class="sxs-lookup"><span data-stu-id="d7c8b-194">is</span></span>
- <span data-ttu-id="d7c8b-195">it</span><span class="sxs-lookup"><span data-stu-id="d7c8b-195">it</span></span>
- <span data-ttu-id="d7c8b-196">it-ch</span><span class="sxs-lookup"><span data-stu-id="d7c8b-196">it-ch</span></span>
- <span data-ttu-id="d7c8b-197">ja</span><span class="sxs-lookup"><span data-stu-id="d7c8b-197">ja</span></span>
- <span data-ttu-id="d7c8b-198">lt</span><span class="sxs-lookup"><span data-stu-id="d7c8b-198">lt</span></span>
- <span data-ttu-id="d7c8b-199">lv</span><span class="sxs-lookup"><span data-stu-id="d7c8b-199">lv</span></span>
- <span data-ttu-id="d7c8b-200">mk</span><span class="sxs-lookup"><span data-stu-id="d7c8b-200">mk</span></span>
- <span data-ttu-id="d7c8b-201">มิลลิวินาที</span><span class="sxs-lookup"><span data-stu-id="d7c8b-201">ms</span></span>
- <span data-ttu-id="d7c8b-202">mt</span><span class="sxs-lookup"><span data-stu-id="d7c8b-202">mt</span></span>
- <span data-ttu-id="d7c8b-203">nb-no</span><span class="sxs-lookup"><span data-stu-id="d7c8b-203">nb-no</span></span>
- <span data-ttu-id="d7c8b-204">nl</span><span class="sxs-lookup"><span data-stu-id="d7c8b-204">nl</span></span>
- <span data-ttu-id="d7c8b-205">nl-be</span><span class="sxs-lookup"><span data-stu-id="d7c8b-205">nl-be</span></span>
- <span data-ttu-id="d7c8b-206">nn-no</span><span class="sxs-lookup"><span data-stu-id="d7c8b-206">nn-no</span></span>
- <span data-ttu-id="d7c8b-207">pl</span><span class="sxs-lookup"><span data-stu-id="d7c8b-207">pl</span></span>
- <span data-ttu-id="d7c8b-208">pt-br</span><span class="sxs-lookup"><span data-stu-id="d7c8b-208">pt-br</span></span>
- <span data-ttu-id="d7c8b-209">ro</span><span class="sxs-lookup"><span data-stu-id="d7c8b-209">ro</span></span>
- <span data-ttu-id="d7c8b-210">ru</span><span class="sxs-lookup"><span data-stu-id="d7c8b-210">ru</span></span>
- <span data-ttu-id="d7c8b-211">ru-ru</span><span class="sxs-lookup"><span data-stu-id="d7c8b-211">ru-ru</span></span>
- <span data-ttu-id="d7c8b-212">sk</span><span class="sxs-lookup"><span data-stu-id="d7c8b-212">sk</span></span>
- <span data-ttu-id="d7c8b-213">sl</span><span class="sxs-lookup"><span data-stu-id="d7c8b-213">sl</span></span>
- <span data-ttu-id="d7c8b-214">sq</span><span class="sxs-lookup"><span data-stu-id="d7c8b-214">sq</span></span>
- <span data-ttu-id="d7c8b-215">sr</span><span class="sxs-lookup"><span data-stu-id="d7c8b-215">sr</span></span>
- <span data-ttu-id="d7c8b-216">sr-la</span><span class="sxs-lookup"><span data-stu-id="d7c8b-216">sr-la</span></span>
- <span data-ttu-id="d7c8b-217">sv</span><span class="sxs-lookup"><span data-stu-id="d7c8b-217">sv</span></span>
- <span data-ttu-id="d7c8b-218">sv-fi</span><span class="sxs-lookup"><span data-stu-id="d7c8b-218">sv-fi</span></span>
- <span data-ttu-id="d7c8b-219">th</span><span class="sxs-lookup"><span data-stu-id="d7c8b-219">th</span></span>
- <span data-ttu-id="d7c8b-220">tn</span><span class="sxs-lookup"><span data-stu-id="d7c8b-220">tn</span></span>
- <span data-ttu-id="d7c8b-221">tr</span><span class="sxs-lookup"><span data-stu-id="d7c8b-221">tr</span></span>
- <span data-ttu-id="d7c8b-222">uk</span><span class="sxs-lookup"><span data-stu-id="d7c8b-222">uk</span></span>
- <span data-ttu-id="d7c8b-223">ur</span><span class="sxs-lookup"><span data-stu-id="d7c8b-223">ur</span></span>
- <span data-ttu-id="d7c8b-224">xh</span><span class="sxs-lookup"><span data-stu-id="d7c8b-224">xh</span></span>
- <span data-ttu-id="d7c8b-225">zh-hans</span><span class="sxs-lookup"><span data-stu-id="d7c8b-225">zh-hans</span></span>
- <span data-ttu-id="d7c8b-226">zh-hk</span><span class="sxs-lookup"><span data-stu-id="d7c8b-226">zh-hk</span></span>
- <span data-ttu-id="d7c8b-227">zh-sg</span><span class="sxs-lookup"><span data-stu-id="d7c8b-227">zh-sg</span></span>
- <span data-ttu-id="d7c8b-228">zu</span><span class="sxs-lookup"><span data-stu-id="d7c8b-228">zu</span></span>

## <a name="additional-resources"></a><span data-ttu-id="d7c8b-229">แหล่งข้อมูลเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="d7c8b-229">Additional resources</span></span>

[<span data-ttu-id="d7c8b-230">เพิ่มโลโก้</span><span class="sxs-lookup"><span data-stu-id="d7c8b-230">Add a logo</span></span>](add-logo.md)

[<span data-ttu-id="d7c8b-231">เลือกธีมของไซต์</span><span class="sxs-lookup"><span data-stu-id="d7c8b-231">Select a site theme</span></span>](select-site-theme.md)

[<span data-ttu-id="d7c8b-232">ทำงานกับไฟล์การแก้ไข CSS</span><span class="sxs-lookup"><span data-stu-id="d7c8b-232">Work with CSS override files</span></span>](css-override-files.md)

[<span data-ttu-id="d7c8b-233">เพิ่มไอคอนประจำไซต์</span><span class="sxs-lookup"><span data-stu-id="d7c8b-233">Add a favicon</span></span>](add-favicon.md)

[<span data-ttu-id="d7c8b-234">เพิ่มข้อความต้อนรับ</span><span class="sxs-lookup"><span data-stu-id="d7c8b-234">Add a welcome message</span></span>](add-welcome-message.md)

[<span data-ttu-id="d7c8b-235">เพิ่มข้อความสงวนลิขสิทธิ์</span><span class="sxs-lookup"><span data-stu-id="d7c8b-235">Add a copyright notice</span></span>](add-copyright-notice.md)

[<span data-ttu-id="d7c8b-236">เพิ่มโค้ดสคริปต์ให้กับหน้าไซต์เพื่อสนับสนุนการตรวจวัดระยะไกล</span><span class="sxs-lookup"><span data-stu-id="d7c8b-236">Add script code to site pages to support telemetry</span></span>](add-telemetry.md)
