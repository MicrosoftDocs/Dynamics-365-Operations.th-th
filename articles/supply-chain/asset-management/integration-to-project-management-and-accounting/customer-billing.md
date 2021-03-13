---
title: เรียกเก็บเงินสำหรับการบํารุงรักษาสินทรัพย์ที่ลูกค้าเป็นเจ้าของ
description: หัวข้อนี้อธิบายวิธีการสร้าง ประมวลผล และเรียกเก็บเงินงานการบํารุงรักษาที่เสร็จสิ้นในสินทรัพย์ที่ลูกค้าของคุณเป็นเจ้าของ
author: johanhoffmann
manager: tfehr
ms.date: 01/28/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EntAssetWorkOrderProjCostInfoPart
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2021-01-28
ms.dyn365.ops.version: 10.0.17
ms.openlocfilehash: 643e59f082949ed51ab61d79648a98b83a7f0b03
ms.sourcegitcommit: 1e615288db245f83c5d5e0cd45315400f8946beb
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 02/08/2021
ms.locfileid: "5131852"
---
# <a name="bill-for-maintenance-on-customer-owned-assets"></a><span data-ttu-id="e9881-103">เรียกเก็บเงินสำหรับการบํารุงรักษาสินทรัพย์ที่ลูกค้าเป็นเจ้าของ</span><span class="sxs-lookup"><span data-stu-id="e9881-103">Bill for maintenance on customer-owned assets</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="e9881-104">คุณลักษณะ *การเรียกเก็บเงินตามใบสั่งงาน* ช่วยให้คุณสามารถสร้าง ประมวลผล และเรียกเก็บเงินงานการบํารุงรักษาที่เสร็จสิ้นในสินทรัพย์ที่ลูกค้าของคุณเป็นเจ้าของได้</span><span class="sxs-lookup"><span data-stu-id="e9881-104">The *Work order billing* feature lets you create, process, and bill maintenance work that is done on assets that your customers own.</span></span> <span data-ttu-id="e9881-105">คุณลักษณะนี้ช่วยให้คุณสามารถดำเนินงานต่อไปนี้ได้:</span><span class="sxs-lookup"><span data-stu-id="e9881-105">This feature lets you perform the following tasks:</span></span>

- <span data-ttu-id="e9881-106">เชื่อมโยงลูกค้ากับสินทรัพย์ที่ลูกค้าเป็นเจ้าของ</span><span class="sxs-lookup"><span data-stu-id="e9881-106">Connect customers to the assets that they own.</span></span>
- <span data-ttu-id="e9881-107">เลือกลูกค้าและดูสินทรัพย์ที่ลูกค้าเป็นเจ้าของ เมื่อคุณสร้างใบสั่งงาน</span><span class="sxs-lookup"><span data-stu-id="e9881-107">Select a customer and view the assets that customer owns when you create a work order.</span></span>
- <span data-ttu-id="e9881-108">ตั้งค่าโครงการหลักสำหรับลูกค้าแต่ละราย</span><span class="sxs-lookup"><span data-stu-id="e9881-108">Set up a parent project for each customer.</span></span>
- <span data-ttu-id="e9881-109">ลงทะเบียนชั่วโมง สินค้า ค่าใช้จ่าย และค่าธรรมเนียม โดยเทียบกับใบสั่งงาน แล้วจากนั้น สร้างข้อเสนอใบแจ้งหนี้ให้กับลูกค้าในภายหลัง</span><span class="sxs-lookup"><span data-stu-id="e9881-109">Register hours, items, expenses, and fees against the work order, and then create an invoice proposal for the customer later.</span></span>

<span data-ttu-id="e9881-110">นอกจากนี้ คุณลักษณะจะมีฟังก์ชันดังต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="e9881-110">In addition, the feature provides the following functionality:</span></span>

- <span data-ttu-id="e9881-111">สัญญาโครงการจากโครงการหลักของลูกค้าจะถูกคัดลอกไปยังโครงการใบสั่งงานที่เกี่ยวข้องโดยอัตโนมัติ</span><span class="sxs-lookup"><span data-stu-id="e9881-111">The project contract from a customer's parent project is automatically copied to the relevant work order project.</span></span>
- <span data-ttu-id="e9881-112">ขณะนี้การจัดการสินทรัพย์สามารถใช้ชนิดธุรกรรมโครงการ *ค่าธรรมเนียม* ในทั้งการคาดการณ์ใบสั่งงานและสมุดรายวันใบสั่งงาน</span><span class="sxs-lookup"><span data-stu-id="e9881-112">Asset management can now use the *fee* project transaction type on both work order forecasts and work order journals.</span></span>

## <a name="turn-on-the-customer-billing-feature"></a><span data-ttu-id="e9881-113">เปิดคุณลักษณะการเรียกเก็บเงินลูกค้า</span><span class="sxs-lookup"><span data-stu-id="e9881-113">Turn on the customer billing feature</span></span>

<span data-ttu-id="e9881-114">ก่อนที่คุณจะสามารถใช้คุณลักษณะนี้ได้ คุณต้องเปิดใช้งานในระบบของคุณ</span><span class="sxs-lookup"><span data-stu-id="e9881-114">Before you can use this feature, it must be turned on in your system.</span></span> <span data-ttu-id="e9881-115">ผู้ดูแลระบบสามารถใช้การตั้งค่า [การจัดการคุณลักษณะ](../../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) เพื่อตรวจสอบสถานะของคุณลักษณะและเปิดใช้งาน</span><span class="sxs-lookup"><span data-stu-id="e9881-115">Admins can use the [feature management](../../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) settings to check the status of the feature and turn it on.</span></span> <span data-ttu-id="e9881-116">ในพื้นที่ทำงาน **การจัดการคุณลักษณะ** มีการแสดงรายการคุณลักษณะในวิธีต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="e9881-116">In the **Feature management** workspace, the feature is listed in the following way:</span></span>

- <span data-ttu-id="e9881-117">**โมดูล:** *การจัดการและการบัญชีโครงการ*</span><span class="sxs-lookup"><span data-stu-id="e9881-117">**Module:** *Project management and accounting*</span></span>
- <span data-ttu-id="e9881-118">**ชื่อคุณลักษณะ:** *การเรียกเก็บเงินตามใบสั่งงาน*</span><span class="sxs-lookup"><span data-stu-id="e9881-118">**Feature name:** *Work order billing*</span></span>

## <a name="example-scenario"></a><span data-ttu-id="e9881-119">ตัวอย่างสถานการณ์จำลอง</span><span class="sxs-lookup"><span data-stu-id="e9881-119">Example scenario</span></span>

<span data-ttu-id="e9881-120">หากต้องการเรียนรู้วิธีการใช้งานคุณลักษณะนี้ ให้ดำเนินการผ่านสถานการณ์ตัวอย่างต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="e9881-120">To learn how this feature works, work through the following example scenario.</span></span>

<span data-ttu-id="e9881-121">เมื่อต้องการดำเนินการสถานการณ์นี้โดยใช้เรกคอร์ดและค่าตัวอย่างที่ระบุที่นี่ คุณต้องอยู่ในระบบที่มีการติดตั้ง [ข้อมูลสาธิต](../../../fin-ops-core/dev-itpro/deployment/deploy-demo-environment.md) มาตรฐาน</span><span class="sxs-lookup"><span data-stu-id="e9881-121">To work through this scenario by using the sample records and values that are specified here, you must be on a system where the standard [demo data](../../../fin-ops-core/dev-itpro/deployment/deploy-demo-environment.md) is installed.</span></span> <span data-ttu-id="e9881-122">คุณต้องเลือกนิติบุคคล **USMF** ก่อนที่คุณจะเริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="e9881-122">You must select the **USMF** legal entity before you begin.</span></span>

<span data-ttu-id="e9881-123">นอกจากนี้ คุณยังสามารถใช้สถานการณ์จำลองนี้เป็นคำแนะนำสำหรับการใช้คุณลักษณะ เมื่อคุณทำงานในระบบการผลิต</span><span class="sxs-lookup"><span data-stu-id="e9881-123">You can also use this scenario as guidance for using the feature when you work on a production system.</span></span> <span data-ttu-id="e9881-124">อย่างไรก็ตาม ในกรณีดังกล่าว คุณต้องแทนที่ค่าของคุณเอง และคุณอาจขาดเรกคอร์ดที่จำเป็นบางชนิดที่ข้อมูลสาธิตมาตรฐานมีให้</span><span class="sxs-lookup"><span data-stu-id="e9881-124">However, in that case, you must substitute your own values, and you might be missing some types of required records that the standard demo data provides.</span></span>

### <a name="step-1-create-a-new-project-contract-for-the-customer"></a><span data-ttu-id="e9881-125">ขั้นตอนที่ 1: สร้างสัญญาโครงการใหม่สำหรับลูกค้า</span><span class="sxs-lookup"><span data-stu-id="e9881-125">Step 1: Create a new project contract for the customer</span></span>

1. <span data-ttu-id="e9881-126">ไปที่ **การจัดการโครงการและการบัญชี \> โครงการ \> สัญญาโครงการ**</span><span class="sxs-lookup"><span data-stu-id="e9881-126">Go to **Project management and accounting \> Projects \> Project contracts**.</span></span>
1. <span data-ttu-id="e9881-127">บนบานหน้าต่างการดำเนินการ เลือก **สร้าง**</span><span class="sxs-lookup"><span data-stu-id="e9881-127">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="e9881-128">ในกล่องโต้ตอบ **สัญญาโครงการใหม่** ตั้งค่าค่าต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="e9881-128">In the **New project contract** dialog box, set the following values:</span></span>

    - <span data-ttu-id="e9881-129">**ชื่อ:** *Pelican Wholesales*</span><span class="sxs-lookup"><span data-stu-id="e9881-129">**Name:** *Pelican Wholesales*</span></span>
    - <span data-ttu-id="e9881-130">**ชนิดของเงินทุน:** *ลูกค้า*</span><span class="sxs-lookup"><span data-stu-id="e9881-130">**Funding type:** *Customer*</span></span>
    - <span data-ttu-id="e9881-131">**แหล่งเงินทุน:** *US-013* (*Pelican Wholesales*)</span><span class="sxs-lookup"><span data-stu-id="e9881-131">**Funding source:** *US-013* (*Pelican Wholesales*)</span></span>

1. <span data-ttu-id="e9881-132">เลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="e9881-132">Select **OK**.</span></span>

### <a name="step-2-create-a-new-parent-project-for-the-customer"></a><span data-ttu-id="e9881-133">ขั้นตอนที่ 2: สร้างโครงการหลักใหม่สำหรับลูกค้า</span><span class="sxs-lookup"><span data-stu-id="e9881-133">Step 2: Create a new parent project for the customer</span></span>

<span data-ttu-id="e9881-134">โครงการหลักที่คุณสร้างที่นี่จะถูกใช้ เมื่อมีการสร้างใบสั่งงานสำหรับลูกค้า</span><span class="sxs-lookup"><span data-stu-id="e9881-134">The parent project that you create here will be used when work orders for the customer are created.</span></span>

1. <span data-ttu-id="e9881-135">ไปที่ **การจัดการโครงการและการบัญชี \> โครงการ \> โครงการทั้งหมด**</span><span class="sxs-lookup"><span data-stu-id="e9881-135">Go to **Project management and accounting \> Projects \> All projects**.</span></span>
1. <span data-ttu-id="e9881-136">บนบานหน้าต่างการดำเนินการ เลือก **สร้าง**</span><span class="sxs-lookup"><span data-stu-id="e9881-136">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="e9881-137">ในกล่องโต้ตอบ **โครงการใหม่** ให้ตั้งค่าค่าดังต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="e9881-137">In the **New project** dialog box, set the following values:</span></span>

    - <span data-ttu-id="e9881-138">**ชนิดของโครงการ:** *เวลาและวัสดุ*</span><span class="sxs-lookup"><span data-stu-id="e9881-138">**Project type:** *Time and material*</span></span>
    - <span data-ttu-id="e9881-139">**ชื่อโครงการ:** *ใบสั่งงาน Pelican Wholesales*</span><span class="sxs-lookup"><span data-stu-id="e9881-139">**Project name:** *Pelican Wholesales work orders*</span></span>
    - <span data-ttu-id="e9881-140">**กลุ่มโครงการ:** *TM*</span><span class="sxs-lookup"><span data-stu-id="e9881-140">**Project group:** *TM*</span></span>
    - <span data-ttu-id="e9881-141">**รหัสสัญญาโครงการ:** *Pelican Wholesales* (สัญญาที่คุณสร้างขึ้นก่อนหน้านี้)</span><span class="sxs-lookup"><span data-stu-id="e9881-141">**Project contract ID:** *Pelican Wholesales* (the contract that you created earlier)</span></span>
    - <span data-ttu-id="e9881-142">**วันที่เริ่มต้น:** เลือกวันที่ของวันนี้</span><span class="sxs-lookup"><span data-stu-id="e9881-142">**Start date:** Select today's date.</span></span>

1. <span data-ttu-id="e9881-143">เลือก **สร้างโครงการ**</span><span class="sxs-lookup"><span data-stu-id="e9881-143">Select **Create project**.</span></span>
1. <span data-ttu-id="e9881-144">โครงการใหม่ถูกเปิดขึ้น</span><span class="sxs-lookup"><span data-stu-id="e9881-144">The new project is opened.</span></span> <span data-ttu-id="e9881-145">จดบันทึกค่า **รหัสโครงการ**</span><span class="sxs-lookup"><span data-stu-id="e9881-145">Make a note of the **Project ID** value.</span></span> <span data-ttu-id="e9881-146">คุณจะต้องป้อนในภายหลัง</span><span class="sxs-lookup"><span data-stu-id="e9881-146">You will have to enter it later.</span></span>

### <a name="step-3-create-a-new-work-order-type-in-asset-management"></a><span data-ttu-id="e9881-147">ขั้นตอนที่ 3: สร้างชนิดใบสั่งงานใหม่ในการจัดการสินทรัพย์</span><span class="sxs-lookup"><span data-stu-id="e9881-147">Step 3: Create a new work order type in Asset management</span></span>

1. <span data-ttu-id="e9881-148">ไปที่ **การจัดการสินทรัพย์ \> ตั้งค่า \> ใบสั่งงาน \> ชนิดของใบสั่งงาน**</span><span class="sxs-lookup"><span data-stu-id="e9881-148">Go to **Asset management \> Setup \> Work order \> Work order types**.</span></span>
1. <span data-ttu-id="e9881-149">บนบานหน้าต่างการดำเนินการ เลือก **สร้าง**</span><span class="sxs-lookup"><span data-stu-id="e9881-149">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="e9881-150">เรกคอร์ดใหม่จะถูกเพิ่มลงในรายการ</span><span class="sxs-lookup"><span data-stu-id="e9881-150">A new record is added to the list.</span></span> <span data-ttu-id="e9881-151">ตั้งค่าค่าต่อไปนี้สำหรับรายการนี้:</span><span class="sxs-lookup"><span data-stu-id="e9881-151">Set the following values for it:</span></span>

    - <span data-ttu-id="e9881-152">**ชนิดใบสั่งงาน:** *บริการ*</span><span class="sxs-lookup"><span data-stu-id="e9881-152">**Work order type:** *Service*</span></span>
    - <span data-ttu-id="e9881-153">**ชื่อ:** *ใบสั่งงานของบริการ*</span><span class="sxs-lookup"><span data-stu-id="e9881-153">**Name:** *Service work orders*</span></span>
    - <span data-ttu-id="e9881-154">**สถานะของวงจรการใช้ใบสั่งงาน:** *มาตรฐาน*</span><span class="sxs-lookup"><span data-stu-id="e9881-154">**Work order lifecycle state:** *Standard*</span></span>

### <a name="step-4-link-the-customer-account-to-the-parent-project"></a><span data-ttu-id="e9881-155">ขั้นตอนที่ 4: เชื่อมโยงบัญชีลูกค้ากับโครงการหลัก</span><span class="sxs-lookup"><span data-stu-id="e9881-155">Step 4: Link the customer account to the parent project</span></span>

<span data-ttu-id="e9881-156">ตอนนี้ คุณต้องเชื่อมโยงบัญชีลูกค้ากับโครงการหลักในการตั้งค่าโครงการในการจัดการสินทรัพย์</span><span class="sxs-lookup"><span data-stu-id="e9881-156">You must now link the customer account to the parent project in the project setup in Asset management.</span></span>

1. <span data-ttu-id="e9881-157">ไปที่ **การจัดการสินทรัพย์ \> ตั้งค่า \> ใบสั่งงาน \> การตั้งค่าโครงการ**</span><span class="sxs-lookup"><span data-stu-id="e9881-157">Go to **Asset management \> Setup \> Work orders \> Project setup**.</span></span>
1. <span data-ttu-id="e9881-158">บนแท็บ **โครงการหลัก** ให้เลือก **เพิ่ม** เพื่อเพิ่มรายการ</span><span class="sxs-lookup"><span data-stu-id="e9881-158">On the **Parent project** tab, select **Add** to add a line.</span></span>
1. <span data-ttu-id="e9881-159">บนบรรทัดใหม่ ให้ตั้งค่าค่าต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="e9881-159">On the new line, set the following values:</span></span>

    - <span data-ttu-id="e9881-160">**บัญชีลูกค้า:** *US-013* (*Pelican Wholesales*)</span><span class="sxs-lookup"><span data-stu-id="e9881-160">**Customer account:** *US-013* (*Pelican Wholesales*)</span></span>
    - <span data-ttu-id="e9881-161">**รหัสโครงการ:** ป้อนรหัสโครงการที่คุณจดบันทึกไว้ก่อนหน้านี้</span><span class="sxs-lookup"><span data-stu-id="e9881-161">**Project ID:** Enter the project ID that you made a note of earlier.</span></span>

### <a name="step-5-link-the-project-group-and-type-to-the-work-order-project"></a><span data-ttu-id="e9881-162">ขั้นตอนที่ 5: เชื่อมโยงกลุ่มโครงการและพิมพ์ไปยังโครงการใบสั่งงาน</span><span class="sxs-lookup"><span data-stu-id="e9881-162">Step 5: Link the project group and type to the work order project</span></span>

<span data-ttu-id="e9881-163">คุณควรจะยังคงอยู่ในหน้า **การตั้งค่าโครงการ** (**การจัดการโครงการ \> การตั้งค่า \> ใบสั่งงาน \> การตั้งค่าโครงการ**)</span><span class="sxs-lookup"><span data-stu-id="e9881-163">You should still be on the **Project setup** page (**Asset management \> Setup \> Work orders \> Project setup**).</span></span>

1. <span data-ttu-id="e9881-164">บนแท็บ **กลุ่มโครงการ** ให้เลือก **เพิ่ม** เพื่อเพิ่มรายการ</span><span class="sxs-lookup"><span data-stu-id="e9881-164">On the **Project group** tab, select **Add** to add a line.</span></span>
1. <span data-ttu-id="e9881-165">บนบรรทัดใหม่ ให้ตั้งค่าค่าต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="e9881-165">On the new line, set the following values:</span></span>

    - <span data-ttu-id="e9881-166">**ชนิดใบสั่งงาน:** *บริการ* (ชนิดใบสั่งงานที่คุณสร้างก่อนหน้านี้)</span><span class="sxs-lookup"><span data-stu-id="e9881-166">**Work order type:** *Service* (the work order type that you created earlier)</span></span>
    - <span data-ttu-id="e9881-167">**กลุ่มโครงการ:** *TM*</span><span class="sxs-lookup"><span data-stu-id="e9881-167">**Project group:** *TM*</span></span>

> [!NOTE]
> <span data-ttu-id="e9881-168">สัญญาโครงการในโครงการใบสั่งงานจะสืบทอดมาจากโครงการหลักเสมอ</span><span class="sxs-lookup"><span data-stu-id="e9881-168">The project contract on the work order project is always inherited from the parent project.</span></span>

### <a name="step-6-link-an-asset-to-the-customer-id"></a><span data-ttu-id="e9881-169">ขั้นตอนที่ 6: เชื่อมโยงสินทรัพย์กับรหัสลูกค้า</span><span class="sxs-lookup"><span data-stu-id="e9881-169">Step 6: Link an asset to the customer ID</span></span>

1. <span data-ttu-id="e9881-170">ไปยัง **การจัดการสินทรัพย์ \> สินทรัพย์ \> สินทรัพย์ที่ใช้งานอยู่**</span><span class="sxs-lookup"><span data-stu-id="e9881-170">Go to **Asset management \> Assets \> Active assets**.</span></span>
1. <span data-ttu-id="e9881-171">ในฟิลด์ **ตัวกรอง** ให้ป้อน *VE-102* และเลือกเพื่อกรองข้อมูลตาม **สินทรัพย์**</span><span class="sxs-lookup"><span data-stu-id="e9881-171">In the **Filter** field, enter *VE-102*, and select to filter by **Asset**.</span></span>
1. <span data-ttu-id="e9881-172">เลือกสินทรัพย์เพื่อเปิดการตั้งค่า</span><span class="sxs-lookup"><span data-stu-id="e9881-172">Select the asset to open its settings.</span></span>
1. <span data-ttu-id="e9881-173">บน FastTab **ลูกค้า** ให้ตั้งค่าฟิลด์ **บัญชีลูกค้า** เป็น *US-013* (*Pelican Wholesales*)</span><span class="sxs-lookup"><span data-stu-id="e9881-173">On the **Customer** FastTab, set the **Customer account** field to *US-013* (*Pelican Wholesales*).</span></span>

    <span data-ttu-id="e9881-174">ฟิลด์ **ชื่อ** จะถูกอัพเดตโดยอัตโนมัติเป็น *Pelican Wholesales*</span><span class="sxs-lookup"><span data-stu-id="e9881-174">The **Name** field is automatically updated to *Pelican Wholesales*.</span></span>

### <a name="step-7-create-a-new-work-order-on-the-asset"></a><span data-ttu-id="e9881-175">ขั้นตอนที่ 7: สร้างใบสั่งงานใหม่ในสินทรัพย์</span><span class="sxs-lookup"><span data-stu-id="e9881-175">Step 7: Create a new work order on the asset</span></span>

1. <span data-ttu-id="e9881-176">ไปที่ **การจัดการสินทรัพย์ \> ใบสั่งงาน \> ใบสั่งงานที่ใช้งานอยู่**</span><span class="sxs-lookup"><span data-stu-id="e9881-176">Go to **Asset management \> Work orders \> Active work orders**.</span></span>
1. <span data-ttu-id="e9881-177">บนบานหน้าต่างการดำเนินการ เลือก **สร้าง**</span><span class="sxs-lookup"><span data-stu-id="e9881-177">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="e9881-178">ในกล่องโต้ตอบ **สร้างใบสั่งงาน** ให้ตั้งค่าค่าต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="e9881-178">In the **Create work order** dialog box, set the following values:</span></span>

    - <span data-ttu-id="e9881-179">**ชนิดใบสั่งงาน:** *บริการ*</span><span class="sxs-lookup"><span data-stu-id="e9881-179">**Work order type:** *Service*</span></span>
    - <span data-ttu-id="e9881-180">**คำอธิบาย:** *ซ่อมแซมรถบรรทุก*</span><span class="sxs-lookup"><span data-stu-id="e9881-180">**Description:** *Repair Truck*</span></span>
    - <span data-ttu-id="e9881-181">**บัญชีลูกค้า:** *US-013* (*Pelican Wholesales*)</span><span class="sxs-lookup"><span data-stu-id="e9881-181">**Customer account:** *US-013* (*Pelican Wholesales*)</span></span>
    - <span data-ttu-id="e9881-182">**สินทรัพย์:** *VE-102*</span><span class="sxs-lookup"><span data-stu-id="e9881-182">**Asset:** *VE-102*</span></span>

        > [!NOTE]
        > <span data-ttu-id="e9881-183">การค้นหาจะแสดงเฉพาะสินทรัพย์ที่เชื่อมโยงกับรหัสลูกค้าที่เลือกเท่านั้น</span><span class="sxs-lookup"><span data-stu-id="e9881-183">The lookup shows only assets that are linked to the selected customer account.</span></span>

    - <span data-ttu-id="e9881-184">**ชนิดงานบำรุงรักษา:** *ซ่อมแซม*</span><span class="sxs-lookup"><span data-stu-id="e9881-184">**Maintenance job type:** *Repair*</span></span>
    - <span data-ttu-id="e9881-185">**การค้า:** *ทางกล*</span><span class="sxs-lookup"><span data-stu-id="e9881-185">**Trade:** *Mechanic*</span></span>
    - <span data-ttu-id="e9881-186">**ระดับการบริการ:** *4*</span><span class="sxs-lookup"><span data-stu-id="e9881-186">**Service level:** *4*</span></span>

1. <span data-ttu-id="e9881-187">เลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="e9881-187">Select **OK**.</span></span>

### <a name="step-8-review-the-work-order-and-start-to-work-on-it"></a><span data-ttu-id="e9881-188">ขั้นตอนที่ 8: รีวิวใบสั่งงานและเริ่มต้นทำงาน</span><span class="sxs-lookup"><span data-stu-id="e9881-188">Step 8: Review the work order and start to work on it</span></span>

<span data-ttu-id="e9881-189">ในส่วนนี้ คุณจะทำงานกับใบสั่งงานที่คุณสร้างไว้ในส่วนก่อนหน้านี้</span><span class="sxs-lookup"><span data-stu-id="e9881-189">In this section, you will work on the work order that you created in the previous section.</span></span>

1. <span data-ttu-id="e9881-190">ปฏิบัติตามขั้นตอนต่อไปนี้เพื่อตรวจสอบว่าโครงการหลักเป็นโครงการ *ใบสั่งงานของ Pelican wholesales*:</span><span class="sxs-lookup"><span data-stu-id="e9881-190">Follow these steps to verify that the parent project is the *Pelican wholesales Work order* project:</span></span>

    1. <span data-ttu-id="e9881-191">ในส่วน **งานการบํารุงรักษาในใบสั่งงาน** ให้เลือกรายการ</span><span class="sxs-lookup"><span data-stu-id="e9881-191">In the **Work order maintenance jobs** section, select a line.</span></span>
    1. <span data-ttu-id="e9881-192">บน FastTab **รายละเอียดรายการ** ให้ตรวจสอบค่า **รหัสโครงการ**</span><span class="sxs-lookup"><span data-stu-id="e9881-192">On the **Line details** FastTab, inspect the **Project ID** value.</span></span> <span data-ttu-id="e9881-193">ซึ่งควรจะเป็นหมายเลขที่เชื่อมด้วยยติภังค์ในฟอร์ม *\<Parent-Project-ID\>-\<Project-ID\>*</span><span class="sxs-lookup"><span data-stu-id="e9881-193">It should be a hyphenated number in the form *\<Parent-Project-ID\>-\<Project-ID\>*.</span></span> <span data-ttu-id="e9881-194">ค่านี้เป็นลิงค์</span><span class="sxs-lookup"><span data-stu-id="e9881-194">This value is a link.</span></span>
    1. <span data-ttu-id="e9881-195">เลือกลิงค์รหัสโครงการเพื่อเปิดหน้าที่คุณสามารถดูโครงการหลักและชื่อโครงการ</span><span class="sxs-lookup"><span data-stu-id="e9881-195">Select the project ID link to open a page where you can view the parent project and project names.</span></span>

1. <span data-ttu-id="e9881-196">บนบานหน้าต่างการดำเนินการ บนแท็บ **ใบสั่งงาน** ในกลุ่ม **สถานะของวงจรการใช้** ให้เลือก **อัพเดตสถานะใบสั่งงาน**</span><span class="sxs-lookup"><span data-stu-id="e9881-196">On the Action Pane, on the **Work order** tab, in the **Lifecycle state** group, select **Update work order state**.</span></span>
1. <span data-ttu-id="e9881-197">ในกล่องโต้ตอบ **อัพเดตสถานะใบสั่งงาน** ในคอลัมน์ **เลือก** ให้เลือกกล่องกาเครื่องหมายสำหรับแถวที่มีการตั้งค่าฟิลด์ **สถานะของวงจรการใช้** เป็น *อยู่ระหว่างดำเนินการ*</span><span class="sxs-lookup"><span data-stu-id="e9881-197">In the **Update work order state** dialog box, in the **Select** column, select the check box for the row where the **Lifecycle state** field is set to *In progress*.</span></span>
1. <span data-ttu-id="e9881-198">เลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="e9881-198">Select **OK**.</span></span>
1. <span data-ttu-id="e9881-199">ในกล่องโต้ตอบ **สถานะของวงจรการใช้: อยู่ระหว่างดำเนินการ** ให้เลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="e9881-199">In the **Lifecycle state: InProgress** dialog box, select **OK**.</span></span>

### <a name="step-9-post-the-hours-that-were-spent-on-the-work-order-and-create-a-new-invoice-proposal"></a><span data-ttu-id="e9881-200">ขั้นตอนที่ 9: ลงรายการบัญชีชั่วโมงที่ใช้ในใบสั่งงาน และสร้างข้อเสนอใบแจ้งหนี้ใหม่</span><span class="sxs-lookup"><span data-stu-id="e9881-200">Step 9: Post the hours that were spent on the work order and create a new invoice proposal</span></span>

<span data-ttu-id="e9881-201">ในส่วนนี้ คุณจะทำงานต่อในใบสั่งงานที่คุณเคยทำงานในส่วนก่อนหน้านี้</span><span class="sxs-lookup"><span data-stu-id="e9881-201">In this section, you will continue to work on the work order that you worked on in the previous section.</span></span>

1. <span data-ttu-id="e9881-202">บนบานหน้าต่างการดำเนินการ บนแท็บ **ใบสั่งงาน** ในกลุ่ม **โครงการ** เลือก **สมุดรายวัน**</span><span class="sxs-lookup"><span data-stu-id="e9881-202">On the Action Pane, on the **Work order** tab, in the **Project** group, select **Journals**.</span></span>

    <span data-ttu-id="e9881-203">หน้า **สมุดรายวันใบสั่งงาน** จะปรากฏขึ้น</span><span class="sxs-lookup"><span data-stu-id="e9881-203">The **Work order journals** page appears.</span></span> <span data-ttu-id="e9881-204">ที่นี่ คุณสามารถลงทะเบียนเวลาที่คุณใช้ในใบสั่งงานได้</span><span class="sxs-lookup"><span data-stu-id="e9881-204">Here, you can register the time that you spent on the work order.</span></span>

1. <span data-ttu-id="e9881-205">บน FastTab **ชั่วโมง** เลือก **เพิ่มรายการ**</span><span class="sxs-lookup"><span data-stu-id="e9881-205">On the **Hours** FastTab, select **Add line**.</span></span>
1. <span data-ttu-id="e9881-206">บนรายการใหม่ ให้ตั้งค่าฟิลด์ **ชั่วโมง** เป็น *4*</span><span class="sxs-lookup"><span data-stu-id="e9881-206">On the new, line, set the **Hours** field to *4*.</span></span>
1. <span data-ttu-id="e9881-207">ในบานหน้าต่างการดำเนินการ เลือก **ลงรายการบัญชีสมุดรายวัน**</span><span class="sxs-lookup"><span data-stu-id="e9881-207">On the Action Pane, select **Post journals**.</span></span>
1. <span data-ttu-id="e9881-208">ปิดหน้า **สมุดรายวันใบสั่งงาน** เพื่อกลับไปที่ใบสั่งงาน</span><span class="sxs-lookup"><span data-stu-id="e9881-208">Close the **Work order journals** page to return to the work order.</span></span>
1. <span data-ttu-id="e9881-209">บนบานหน้าต่างการดำเนินการ บนแท็บ **การออกใบแจ้งหนี้** เลือก **ข้อเสนอใบแจ้งหนี้ใหม่**</span><span class="sxs-lookup"><span data-stu-id="e9881-209">On the Action Pane, on the **Invoicing** tab, select **New invoice proposal**.</span></span>
1. <span data-ttu-id="e9881-210">ในกล่องโต้ตอบ **สร้างข้อเสนอใบแจ้งหนี้** ในส่วน **ธุรกรรมโครงการ** ให้เลือกกล่องกาเครื่องหมาย **เลือก** สำหรับทุกรายการที่คุณต้องการออกใบแจ้งหนี้</span><span class="sxs-lookup"><span data-stu-id="e9881-210">In the **Create invoice proposal** dialog box, in the **Project transactions** section, select the **Select** check box for every line  that you want to invoice.</span></span>
1. <span data-ttu-id="e9881-211">เลือก **ตกลง** เพื่อปิดกล่องโต้ตอบและดูข้อเสนอใบแจ้งหนี้ใหม่</span><span class="sxs-lookup"><span data-stu-id="e9881-211">Select **OK** to close the dialog box and view the new invoice proposal.</span></span>
