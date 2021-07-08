---
title: สร้างผลิตภัณฑ์ย่อยที่กำหนดไว้ล่วงหน้า
description: 'กระบวนงานนี้จะแนะนำวิธีการสร้างผลิตภัณฑ์ย่อยสำหรับผลิตภัณฑ์หลัก โดยใช้ชุดของมิติของผลิตภัณฑ์ '
author: t-benebo
ms.date: 04/22/2021
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: EcoResProductListPage, EcoResProductCreate, EcoResProductDetails, EcoResProductMasterDimension, EcoResProductVariants, EcoResProductVariantSuggestions, EcoResProductVariantsPendingReleaseFormPart, EcoResProductVariantSuggestionsEnhanced
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: 442a5f5b321833c170cfecc4069e62a1254605cd
ms.sourcegitcommit: dc4898aa32f381620c517bf89c7856e693563ace
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 06/17/2021
ms.locfileid: "6270491"
---
# <a name="predefined-product-variants"></a><span data-ttu-id="7bc88-103">ผลิตภัณฑ์ย่อยที่กำหนดไว้ล่วงหน้า</span><span class="sxs-lookup"><span data-stu-id="7bc88-103">Predefined product variants</span></span>

[!include [banner](../../includes/banner.md)]

## <a name="example-scenario-create-predefined-product-variants"></a><span data-ttu-id="7bc88-104">สถานการณ์จำลองตัวอย่าง: สร้างผลิตภัณฑ์ย่อยที่กำหนดไว้ล่วงหน้า</span><span class="sxs-lookup"><span data-stu-id="7bc88-104">Example scenario: Create predefined product variants</span></span>

<span data-ttu-id="7bc88-105">สถานการณ์จำลองตัวอย่างนี้แสดงวิธีการสร้างผลิตภัณฑ์ย่อยสำหรับผลิตภัณฑ์หลัก โดยใช้ชุดของมิติของผลิตภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="7bc88-105">This example scenario shows how to create product variants for a product master using a combinations of product dimensions.</span></span>

### <a name="make-demo-data-available"></a><span data-ttu-id="7bc88-106">ทำให้ข้อมูลสาธิตพร้อมใช้งาน</span><span class="sxs-lookup"><span data-stu-id="7bc88-106">Make demo data available</span></span>

<span data-ttu-id="7bc88-107">เพื่อติดตามสถานการณ์จำลองนี้โดยใช้ค่าที่แนะนำที่นี่ คุณต้องมีการติดตั้งข้อมูลสาธิต และคุณต้องเลือกนิติบุคคล *USMF*</span><span class="sxs-lookup"><span data-stu-id="7bc88-107">To follow this scenario using the values suggested here, you must have demo data installed, and you must select the *USMF* legal entity.</span></span>

### <a name="step-1-create-a-product-master"></a><span data-ttu-id="7bc88-108">ขั้นตอนที่ 1: สร้างผลิตภัณฑ์หลัก</span><span class="sxs-lookup"><span data-stu-id="7bc88-108">Step 1: Create a product master</span></span>

<span data-ttu-id="7bc88-109">เพื่อสร้างผลิตภัณฑ์หลัก:</span><span class="sxs-lookup"><span data-stu-id="7bc88-109">To create a product master:</span></span>

1. <span data-ttu-id="7bc88-110">ไปที่ **การจัดการข้อมูลผลิตภัณฑ์ > ผลิตภัณฑ์ > ผลิตภัณฑ์หลัก**</span><span class="sxs-lookup"><span data-stu-id="7bc88-110">Go to **Product information management > Products > Product masters**.</span></span>
1. <span data-ttu-id="7bc88-111">เลือก **ใหม่**</span><span class="sxs-lookup"><span data-stu-id="7bc88-111">Select **New**.</span></span>
1. <span data-ttu-id="7bc88-112">ถ้าฟิลด์ **หมายเลขผลิตภัณฑ์** ยังไม่ได้แสดงหมายเลข ให้ป้อนค่า</span><span class="sxs-lookup"><span data-stu-id="7bc88-112">If the **Product number** field doesn't already show a number, then enter a value.</span></span> <span data-ttu-id="7bc88-113">ต้องทำเช่นนี้ในกรณีที่ไม่มีการตั้งค่าลำดับหมายเลขสำหรับฟิลด์นี้เท่านั้น</span><span class="sxs-lookup"><span data-stu-id="7bc88-113">This is only required if no number sequence has been set for this field.</span></span>
1. <span data-ttu-id="7bc88-114">ป้อนชื่อในฟิลด์ **ชื่อผลิตภัณฑ์**</span><span class="sxs-lookup"><span data-stu-id="7bc88-114">Enter a name in the **Product name** field.</span></span>
1. <span data-ttu-id="7bc88-115">ในฟิลด์ **กลุ่มมิติของผลิตภัณฑ์** ให้เลือกกลุ่มมิติของผลิตภัณฑ์ *SizeCol* (ขนาดและสี)</span><span class="sxs-lookup"><span data-stu-id="7bc88-115">In the **Product dimension group** field, select the product dimension group *SizeCol* (Size and Color).</span></span>
1. <span data-ttu-id="7bc88-116">เลือก **ตกลง** เพื่อสร้างและเปิดผลิตภัณฑ์หลักใหม่</span><span class="sxs-lookup"><span data-stu-id="7bc88-116">Select **OK** to create and open the new product master.</span></span>

### <a name="step-2-add-product-dimensions"></a><span data-ttu-id="7bc88-117">ขั้นตอนที่ 2: เพิ่มมิติของผลิตภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="7bc88-117">Step 2: Add product dimensions</span></span>

<span data-ttu-id="7bc88-118">ตัวอย่างนี้แสดงวิธีการป้อนมิติของผลิตภัณฑ์ด้วยตนเอง </span><span class="sxs-lookup"><span data-stu-id="7bc88-118">This example shows how to manually enter product dimensions.</span></span> <span data-ttu-id="7bc88-119">นอกจากนี้ คุณยังสามารถเลือกกลุ่มขนาด สี หรือลักษณะที่รวมค่ามิติของผลิตภัณฑ์ที่คุณต้องการใช้ได้</span><span class="sxs-lookup"><span data-stu-id="7bc88-119">You can also choose to select a size, color, or style group that includes the product dimension values you want to use.</span></span>

<span data-ttu-id="7bc88-120">เพื่อเพิ่มมิติของผลิตภัณฑ์:</span><span class="sxs-lookup"><span data-stu-id="7bc88-120">To add product dimensions:</span></span>

1. <span data-ttu-id="7bc88-121">เมื่อผลิตภัณฑ์หลักใหม่ของคุณยังคงเปิดอยู่ ให้เลือก **มิติของผลิตภัณฑ์** ในบานหน้าต่างการดำเนินการ</span><span class="sxs-lookup"><span data-stu-id="7bc88-121">With your new product master still open, select **Product dimensions** on the Action Pane.</span></span>
1. <span data-ttu-id="7bc88-122">เปิดแท็บ **ขนาด** และเลือก **สร้าง** บนแถบเครื่องมือ เพื่อเพิ่มแถวลงในกริด</span><span class="sxs-lookup"><span data-stu-id="7bc88-122">Open the **Size** tab and select **New** on the toolbar to add a row to the grid.</span></span> <span data-ttu-id="7bc88-123">ทำการตั้งค่าต่อไปนี้สำหรับแถวใหม่:</span><span class="sxs-lookup"><span data-stu-id="7bc88-123">Make the following settings for the new row:</span></span>
    - <span data-ttu-id="7bc88-124">**ขนาด:** เลือกค่าขนาด</span><span class="sxs-lookup"><span data-stu-id="7bc88-124">**Size:** Select a size value.</span></span>
    - <span data-ttu-id="7bc88-125">**ชื่อ:** ป้อนชื่อสำหรับขนาด</span><span class="sxs-lookup"><span data-stu-id="7bc88-125">**Name:** Enter a name for the size.</span></span>
1. <span data-ttu-id="7bc88-126">เลือก **สร้าง** บนแถบเครื่องมือ และเพิ่มขนาดที่สองในกริดที่มี **ขนาด** และ **ชื่อ** ใหม่</span><span class="sxs-lookup"><span data-stu-id="7bc88-126">Select **New** on the toolbar and add a second size to the grid with a new **Size** and **Name**.</span></span>
1. <span data-ttu-id="7bc88-127">เปิดแท็บ **สี** และเลือก **สร้าง** บนแถบเครื่องมือ เพื่อเพิ่มแถวลงในกริด</span><span class="sxs-lookup"><span data-stu-id="7bc88-127">Open the **Colors** tab and select **New** on the toolbar to add a row to the grid.</span></span> <span data-ttu-id="7bc88-128">ทำการตั้งค่าต่อไปนี้สำหรับแถวใหม่:</span><span class="sxs-lookup"><span data-stu-id="7bc88-128">Make the following settings for the new row:</span></span>
    - <span data-ttu-id="7bc88-129">**สี:** เลือกค่าสี</span><span class="sxs-lookup"><span data-stu-id="7bc88-129">**Color:** Select a color value.</span></span>
    - <span data-ttu-id="7bc88-130">**ชื่อ:** ป้อนชื่อสำหรับสี</span><span class="sxs-lookup"><span data-stu-id="7bc88-130">**Name:** Enter a name for the color.</span></span>
1. <span data-ttu-id="7bc88-131">เลือก **สร้าง** บนแถบเครื่องมือ และเพิ่มสีที่สองในกริดที่มี **สี** และ **ชื่อ** ใหม่</span><span class="sxs-lookup"><span data-stu-id="7bc88-131">Select **New** on the toolbar and add a second color to the grid with a new **Color** and **Name**.</span></span>
1. <span data-ttu-id="7bc88-132">เลือก **บันทึก**</span><span class="sxs-lookup"><span data-stu-id="7bc88-132">Select **Save**.</span></span>
1. <span data-ttu-id="7bc88-133">ปิดหน้าเพื่อกลับไปที่ผลิตภัณฑ์หลักใหม่ของคุณ</span><span class="sxs-lookup"><span data-stu-id="7bc88-133">Close the page to return to your new product master.</span></span>

### <a name="step-3-generate-product-variants"></a><span data-ttu-id="7bc88-134">ขั้นตอนที่ 3: สร้างผลิตภัณฑ์ย่อย</span><span class="sxs-lookup"><span data-stu-id="7bc88-134">Step 3: Generate product variants</span></span>

> [!NOTE]
> <span data-ttu-id="7bc88-135">ส่วนนี้อธิบายวิธีการสร้างผลิตภัณฑ์ย่อย เมื่อไม่ได้เปิดใช้งานคุณลักษณะ *การปรับปรุงหน้าคำแนะนำผลิตภัณฑ์ย่อย*</span><span class="sxs-lookup"><span data-stu-id="7bc88-135">This section describes how to generate product variants when the *Variant suggestions page improvements* feature isn't enabled.</span></span> <span data-ttu-id="7bc88-136">ดูรายละเอียดเพิ่มเติมในส่วนถัดไปเกี่ยวกับวิธีการสร้างผลิตภัณฑ์ย่อยเมื่อคุณลักษณะนั้นพร้อมใช้งาน</span><span class="sxs-lookup"><span data-stu-id="7bc88-136">See the next section for details about how to generate product variants when that feature is available.</span></span>

<span data-ttu-id="7bc88-137">เพื่อสร้างผลิตภัณฑ์ย่อย:</span><span class="sxs-lookup"><span data-stu-id="7bc88-137">To generate product variants:</span></span>

1. <span data-ttu-id="7bc88-138">เมื่อผลิตภัณฑ์หลักใหม่ของคุณยังคงเปิดอยู่ ให้เลือก **ผลิตภัณฑ์ย่อย** ในบานหน้าต่างการดำเนินการ</span><span class="sxs-lookup"><span data-stu-id="7bc88-138">With your new product master still open, select **Product variants** on the Action Pane.</span></span>
1. <span data-ttu-id="7bc88-139">เลือก **คำแนะนำผลิตภัณฑ์ย่อย** บนบานหน้าต่างการดำเนินการ</span><span class="sxs-lookup"><span data-stu-id="7bc88-139">Select **Variant suggestions** on the Action Pane.</span></span>
1. <span data-ttu-id="7bc88-140">ระบบจะสร้างรายการโดยที่มีชุดของขนาดและสีต่างๆ ที่เป็นไปได้ทั้งหมดที่คุณกําหนดไว้สำหรับผลิตภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="7bc88-140">The system generates a list with all possible combinations of the sizes and colors you defined for the product.</span></span> <span data-ttu-id="7bc88-141">เลือก **เลือกทั้งหมด** บนแถบเครื่องมือ</span><span class="sxs-lookup"><span data-stu-id="7bc88-141">Select **Select all** on the toolbar.</span></span>
    - <span data-ttu-id="7bc88-142">ในตัวอย่างนี้ เลือกผลิตภัณฑ์ย่อยที่เป็นไปได้ทั้งหมด</span><span class="sxs-lookup"><span data-stu-id="7bc88-142">In this example, select all of the possible variants.</span></span> <span data-ttu-id="7bc88-143">ถ้าคุณต้องการใช้ชุดย่อยของชุดมิติของผลิตภัณฑ์ที่เป็นไปได้เท่านั้น ให้เลือกกล่องกาเครื่องหมายที่ต้องการตามความจำเป็นเท่านั้น</span><span class="sxs-lookup"><span data-stu-id="7bc88-143">If you only want to use a subset of the possible product dimension combinations, select only the required check boxes as needed.</span></span>  
1. <span data-ttu-id="7bc88-144">เลือก **สร้าง**</span><span class="sxs-lookup"><span data-stu-id="7bc88-144">Select **Create**.</span></span>
1. <span data-ttu-id="7bc88-145">เลือก **บันทึก**</span><span class="sxs-lookup"><span data-stu-id="7bc88-145">Select **Save**.</span></span>

## <a name="improved-variant-suggestions"></a><span data-ttu-id="7bc88-146">คำแนะนำผลิตภัณฑ์ย่อยที่ปรับปรุงแล้ว</span><span class="sxs-lookup"><span data-stu-id="7bc88-146">Improved variant suggestions</span></span>

<span data-ttu-id="7bc88-147">คุณลักษณะ *การปรับปรุงหน้าคำแนะนำผลิตภัณฑ์ย่อย* จะปรับปรุงหน้า **คำแนะนำผลิตภัณฑ์ย่อย** เพื่อระบุปัญหาด้านประสิทธิภาพและการใช้งานสำหรับบริษัทที่มีชุดมิติของผลิตภัณฑ์จํานวนมาก</span><span class="sxs-lookup"><span data-stu-id="7bc88-147">The *Variant suggestions page improvements* feature improves the **Variant suggestions** page to address performance and usability issues for companies that have a high number of product dimension combinations.</span></span> <span data-ttu-id="7bc88-148">กระบวนการขั้นสูงสำหรับการเลือกค่ามิติของผลิตภัณฑ์ที่จะสร้างคำแนะนำผลิตภัณฑ์ย่อย ช่วยให้การระบุและการนำออกใช้ชุดของผลิตภัณฑ์ย่อยที่เกี่ยวข้องเร็วขึ้นและง่ายขึ้น</span><span class="sxs-lookup"><span data-stu-id="7bc88-148">The enhanced process for selecting the product dimension values for which to generate variant suggestions makes it faster and easier to identify and release the relevant set of product variants.</span></span>

<span data-ttu-id="7bc88-149">คุณลักษณะนี้จะเพิ่มการปรับปรุงต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="7bc88-149">The following improvements are added by this feature:</span></span>

- <span data-ttu-id="7bc88-150">**การสร้างคำแนะนำผลิตภัณฑ์ย่อยที่เลื่อนออกไป:** หน้า **คำแนะนำผลิตภัณฑ์ย่อย** จะไม่แสดงคำแนะนำอีกต่อไป เมื่อคุณเปิดเป็นครั้งแรก</span><span class="sxs-lookup"><span data-stu-id="7bc88-150">**Deferred generation of variant suggestions:** The **Variant suggestions** page no longer shows suggestions when you first open it.</span></span> <span data-ttu-id="7bc88-151">แต่คุณต้องเลือกค่าที่คุณจะต้องใช้อย่างชัดแจ้ง แล้วจากนั้น เลือกปุ่ม **แนะนำ** เพื่อสร้างชุดข้อมูล</span><span class="sxs-lookup"><span data-stu-id="7bc88-151">Instead, you must explicitly choose which values you will need and then select the **Suggest** button to generate the combinations.</span></span> <span data-ttu-id="7bc88-152">ซึ่งช่วยให้กระบวนการมองเห็นได้และเป็นแบบโต้ตอบมากขึ้น</span><span class="sxs-lookup"><span data-stu-id="7bc88-152">This makes the process more visible and interactive.</span></span>
- <span data-ttu-id="7bc88-153">**การเลือกค่ามิติ:** เมื่อคุณมีค่ามิติหลายค่า โดยปกติ คุณสนใจในการสร้างคำแนะนําผลิตภัณฑ์ย่อยที่มีเพียงสองสามค่า (เช่น เมื่อแนะนําชุดของสีหรือลักษณะใหม่)</span><span class="sxs-lookup"><span data-stu-id="7bc88-153">**Selection of dimensions values:** When you have many dimension values, you are typically interested in generating variant suggestions that include just a few of them (such as when introducing a new set of colors or styles).</span></span> <span data-ttu-id="7bc88-154">ด้วยการออกแบบที่พัฒนาขึ้น คุณสามารถเลือกค่ามิติที่คุณต้องการสร้างคำแนะนําผลิตภัณฑ์ย่อย</span><span class="sxs-lookup"><span data-stu-id="7bc88-154">With the improved design, you can select the dimension values for which you want to generate product variant suggestions.</span></span> <span data-ttu-id="7bc88-155">ซึ่งจะเพิ่มความเกี่ยวข้องของตัวแปรที่แนะนำอย่างมาก และปรับปรุงทั้งประสิทธิภาพของระบบและประสิทธิภาพการทำงานของผู้ใช้</span><span class="sxs-lookup"><span data-stu-id="7bc88-155">This greatly increases the relevance of the suggested variants and improves both system performance and user productivity.</span></span>

### <a name="turn-on-the-variant-suggestions-page-improvements-feature"></a><span data-ttu-id="7bc88-156">เปิดคุณลักษณะการปรับปรุงหน้าคำแนะนําผลิตภัณฑ์ย่อย</span><span class="sxs-lookup"><span data-stu-id="7bc88-156">Turn on the Variant suggestions page improvements feature</span></span>

<span data-ttu-id="7bc88-157">ก่อนที่คุณจะสามารถใช้คุณลักษณะ *การปรับปรุงหน้าคำแนะนําผลิตภัณฑ์ย่อย* จะต้องมีการเปิดอยู่ในระบบของคุณ</span><span class="sxs-lookup"><span data-stu-id="7bc88-157">Before you can use *Variant suggestions page improvements* feature, it must be turned on in your system.</span></span> <span data-ttu-id="7bc88-158">ผู้ดูแลระบบสามารถใช้การตั้งค่า [การจัดการคุณลักษณะ](../../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) เพื่อตรวจสอบสถานะของคุณลักษณะและเปิดใช้งาน</span><span class="sxs-lookup"><span data-stu-id="7bc88-158">Admins can use the [feature management](../../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) settings to check the status of the feature and turn it on.</span></span> <span data-ttu-id="7bc88-159">ในพื้นที่ทำงาน **การจัดการคุณลักษณะ** มีการแสดงรายการคุณลักษณะในวิธีต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="7bc88-159">In the **Feature management** workspace, the feature is listed in the following way:</span></span>

- <span data-ttu-id="7bc88-160">**โมดูล:** *การจัดการข้อมูลผลิตภัณฑ์*</span><span class="sxs-lookup"><span data-stu-id="7bc88-160">**Module:** *Product information management*</span></span>
- <span data-ttu-id="7bc88-161">**ชื่อคุณลักษณะ:** *การปรับปรุงหน้าคำแนะนําผลิตภัณฑ์ย่อย*</span><span class="sxs-lookup"><span data-stu-id="7bc88-161">**Feature name:** *Variant suggestions page improvements*</span></span>

### <a name="work-with-the-improved-variant-suggestions"></a><span data-ttu-id="7bc88-162">ทำงานกับคำแนะนําผลิตภัณฑ์ย่อยที่ปรับปรุง</span><span class="sxs-lookup"><span data-stu-id="7bc88-162">Work with the improved variant suggestions</span></span>

<span data-ttu-id="7bc88-163">เพื่อสร้างคำแนะนําผลิตภัณฑ์ย่อย เมื่อเปิดใช้งานคุณลักษณะ *การปรับปรุงหน้าคำแนะนำผลิตภัณฑ์ย่อย*:</span><span class="sxs-lookup"><span data-stu-id="7bc88-163">To generate product variant suggestions when the *Variant suggestions page improvements* feature is enabled:</span></span>

1. <span data-ttu-id="7bc88-164">เปิดหรือสร้างผลิตภัณฑ์หลักและเพิ่มมิติของผลิตภัณฑ์ที่ต้องการลงในผลิตภัณฑ์หลัก ตามที่อธิบายไว้ในส่วนก่อนหน้านี้</span><span class="sxs-lookup"><span data-stu-id="7bc88-164">Open or create a product master and add the required product dimensions to it, as described in the previous section.</span></span>
1. <span data-ttu-id="7bc88-165">เมื่อผลิตภัณฑ์หลักเปิดขึ้น ให้เลือก **ผลิตภัณฑ์ย่อย** ในบานหน้าต่างการดำเนินการ</span><span class="sxs-lookup"><span data-stu-id="7bc88-165">With the product master open, select **Product variants** on the Action Pane.</span></span>
1. <span data-ttu-id="7bc88-166">เลือก **คำแนะนำผลิตภัณฑ์ย่อย** บนบานหน้าต่างการดำเนินการ</span><span class="sxs-lookup"><span data-stu-id="7bc88-166">Select **Variant suggestions** on the Action Pane.</span></span>
1. <span data-ttu-id="7bc88-167">เลือกค่าที่คุณต้องการใช้สำหรับแต่ละมิติ</span><span class="sxs-lookup"><span data-stu-id="7bc88-167">Select the values that you want to use for each of the dimensions.</span></span>
1. <span data-ttu-id="7bc88-168">บนแถบเครื่องมือบนสุด ให้เลือก **แนะนำ**</span><span class="sxs-lookup"><span data-stu-id="7bc88-168">On the top toolbar, select **Suggest**.</span></span>
1. <span data-ttu-id="7bc88-169">ระบบจะสร้างรายการโดยที่มีชุดของขนาดและสีต่างๆ ที่เป็นไปได้ทั้งหมดที่คุณเลือก</span><span class="sxs-lookup"><span data-stu-id="7bc88-169">The system generates a list with all possible combinations of the sizes and colors you selected.</span></span> <span data-ttu-id="7bc88-170">บน FastTab **ตัวแปรที่แนะนำ** ให้เลือกกล่องกาเครื่องหมายสำหรับชุดมิติของผลิตภัณฑ์แต่ละชุดที่คุณต้องการใช้ หรือเลือก **เลือกทั้งหมด** บนแถบเครื่องมือเพื่อเลือกทั้งหมด</span><span class="sxs-lookup"><span data-stu-id="7bc88-170">On the **Suggested variants** FastTab, select the check box for each product dimension combination that you want to use, or select **Select all** on the toolbar to select all of them.</span></span>  
1. <span data-ttu-id="7bc88-171">เลือก **สร้าง** เพื่อเพิ่มตัวแปรในผลิตภัณฑ์หลักปัจจุบัน</span><span class="sxs-lookup"><span data-stu-id="7bc88-171">Select **Create** to add the variants to the current product master.</span></span>

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
