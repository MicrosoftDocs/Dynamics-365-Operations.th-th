---
title: อัปโหลดการตั้งค่าคอนฟิกลงใน Lifecycle Services
description: หัวข้อนี้อธิบายวิธีการสร้างการตั้งค่าคอนฟิกการรายงานทางอิเล็กทรอนิกส์ (ER) ใหม่ และอัปโหลดไปยัง Microsoft Dynamics Lifecycle Services (LCS)
author: NickSelin
ms.date: 06/17/2021
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: ERWorkspace, ERSolutionTable, ERSolutionCreateDropDialog, ERDataModelDesigner, ERDataModelContentsItemCreationDialog, ERSolutionRepositoryTable, ERSolutionRepositoryCreateDropDialog, ERSolutionImport
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 41a8fcf2592bde4901aba703e0cd124b1155dac6
ms.sourcegitcommit: dc4898aa32f381620c517bf89c7856e693563ace
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 06/17/2021
ms.locfileid: "6270570"
---
# <a name="upload-a-configuration-into-lifecycle-services"></a><span data-ttu-id="ba314-103">อัปโหลดการตั้งค่าคอนฟิกลงใน Lifecycle Services</span><span class="sxs-lookup"><span data-stu-id="ba314-103">Upload a configuration into Lifecycle Services</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="ba314-104">หัวข้อนี้อธิบายวิธีที่ผู้ใช้ในบทบาทผู้ดูแลระบบ หรือนักพัฒนาการรายงานทางอิเล็กทรอนิกส์ สามารถสร้าง [การตั้งค่าคอนฟิกการรายงานทางอิเล็กทรอนิกส์ (ER)](../general-electronic-reporting.md#Configuration) ใหม่และอัปโหลดลงใน [แอสเซทไลบรารีระดับโครงการ](../../lifecycle-services/asset-library.md) ใน Microsoft Dynamics Lifecycle Services (LCS)</span><span class="sxs-lookup"><span data-stu-id="ba314-104">This topic explains how a user in the System administrator or Electronic reporting developer role can create a new [Electronic reporting (ER) configuration](../general-electronic-reporting.md#Configuration) and upload it into the [project-level Asset library](../../lifecycle-services/asset-library.md) in Microsoft Dynamics Lifecycle Services (LCS).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="ba314-105">การใช้ LCS เป็นที่เก็บหน่วยจัดเก็บเพื่อการตั้งค่าคอนฟิก ER [ไม่ได้รับการสนับสนุน](../../../../finance/get-started/removed-deprecated-features-finance.md#features-removed-or-deprecated-in-the-finance-10017-release)</span><span class="sxs-lookup"><span data-stu-id="ba314-105">The use of LCS as a storage repository for ER configurations is being [deprecated](../../../../finance/get-started/removed-deprecated-features-finance.md#features-removed-or-deprecated-in-the-finance-10017-release).</span></span> <span data-ttu-id="ba314-106">สำหรับข้อมูลเพิ่มเติม ให้ดู [Regulatory Configuration Service (RCS) – การเลิกใช้ที่เก็บข้อมูล Lifecycle Services (LCS)](../../../../finance/localizations/rcs-lcs-repo-dep-faq.md)</span><span class="sxs-lookup"><span data-stu-id="ba314-106">For more information, see [Regulatory Configuration Service (RCS) – Lifecycle Services (LCS) storage deprecation](../../../../finance/localizations/rcs-lcs-repo-dep-faq.md).</span></span>

<span data-ttu-id="ba314-107">ในตัวอย่างนี้ คุณจะสร้างการตั้งค่าคอนฟิกและอัปโหลดไปยัง LCS สำหรับบริษัทตัวอย่างที่ชื่อ Litware, inc ขั้นตอนเหล่านี้สามารถถูกดำเนินการได้ในบริษัทใดๆ เนื่องจากมีการใช้การตั้งค่าคอนฟิก ER ร่วมกันระหว่างบริษัท</span><span class="sxs-lookup"><span data-stu-id="ba314-107">In this example, you will create a configuration and upload it into LCS for a sample company that is named Litware, Inc. These steps can be completed in any company, because ER configurations are shared among companies.</span></span> <span data-ttu-id="ba314-108">เพื่อทำขั้นตอนเหล่านี้ให้เสร็จสมบูรณ์ อันดับแรกคุณต้องทำขั้นตอนต่างๆ ให้เสร็จสมบูรณ์ [สร้างผู้ให้บริการการตั้งค่าคอนฟิก และทำเครื่องหมายเป็น ใช้งานอยู่](er-configuration-provider-mark-it-active-2016-11.md)</span><span class="sxs-lookup"><span data-stu-id="ba314-108">To complete these steps, you must first complete the steps in [Create configuration providers and mark them as active](er-configuration-provider-mark-it-active-2016-11.md).</span></span> <span data-ttu-id="ba314-109">ต้องมีสิทธิ์เข้าถึง LCS ด้วยเช่นกัน</span><span class="sxs-lookup"><span data-stu-id="ba314-109">Access to LCS is also required.</span></span>

1. <span data-ttu-id="ba314-110">ลงชื่อเข้าใช้ในแอพลิเคชันโดยใช้หนึ่งในบทบาทต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="ba314-110">Sign in to the application by using one of the following roles:</span></span>

    - <span data-ttu-id="ba314-111">นักพัฒนาการรายงานทางอิเล็กทรอนิกส์</span><span class="sxs-lookup"><span data-stu-id="ba314-111">Electronic reporting developer</span></span>
    - <span data-ttu-id="ba314-112">ผู้ดูแลระบบ</span><span class="sxs-lookup"><span data-stu-id="ba314-112">System administrator</span></span>

2. <span data-ttu-id="ba314-113">ไปที่ **การจัดการองค์กร** \> **พื้นที่ทำงาน** \> **การรายงานทางอิเล็กทรอนิกส์**</span><span class="sxs-lookup"><span data-stu-id="ba314-113">Go to **Organization administration** \> **Workspaces** \> **Electronic reporting**.</span></span>
3. <span data-ttu-id="ba314-114">เลือก **Litware, Inc.** และทำเครื่องหมายเป็น **ใช้งานอยู่**</span><span class="sxs-lookup"><span data-stu-id="ba314-114">Select **Litware, Inc.**, and mark it as **Active**.</span></span>
4. <span data-ttu-id="ba314-115">เลือก **การตั้งค่าคอนฟิก**</span><span class="sxs-lookup"><span data-stu-id="ba314-115">Select **Configurations**.</span></span>

<a name="accessconditions"></a>
> [!NOTE]
> <span data-ttu-id="ba314-116">ตรวจสอบให้แน่ใจว่าผู้ใช้ Dynamics 365 Finance ปัจจุบันเป็นสมาชิกของโครงการ LCS ที่มี [แอสเซทไลบรารี](../../lifecycle-services/asset-library.md#asset-library-support) ที่ใช้ในการนำเข้าการตั้งค่าคอนฟิก ER</span><span class="sxs-lookup"><span data-stu-id="ba314-116">Make sure that the current Dynamics 365 Finance user is a member of the LCS project that contains the [Asset library](../../lifecycle-services/asset-library.md#asset-library-support) that is used to import ER configurations.</span></span>
>
> <span data-ttu-id="ba314-117">คุณไม่สามารถเข้าถึงโครงการ LCS จากที่เก็บ ER ซึ่งแสดงถึงโดเมนอื่นที่ไม่ใช่โดเมนที่ใช้ใน Finance</span><span class="sxs-lookup"><span data-stu-id="ba314-117">You can't access an LCS project from an ER repository that represents a different domain than the domain that is used in Finance.</span></span> <span data-ttu-id="ba314-118">ถ้าคุณพยายาม จะมีการแสดงรายการที่ว่างเปล่าของโครงการ LCS และคุณจะไม่สามารถนำเข้าการตั้งค่าคอนฟิก ER จากแอสเซทไลบรารีระดับโครงการใน LCS</span><span class="sxs-lookup"><span data-stu-id="ba314-118">If you try, an empty list of LCS projects will be shown, and you won't be able to import ER configurations from the project-level Asset library in LCS.</span></span> <span data-ttu-id="ba314-119">ถ้าต้องการเข้าถึงแอสเซทไลบรารีระดับโครงการจากที่เก็บ ER ซึ่งใช้ในการนำเข้าการตั้งค่าคอนฟิก ER ให้ลงชื่อเข้าใช้ Finance โดยใช้ข้อมูลประจำตัวของผู้ใช้ที่เป็นสมาชิกของผู้เช่า (โดเมน) ที่มีการเตรียมใช้งานอินสแตนซ์ Finance ในปัจจุบัน</span><span class="sxs-lookup"><span data-stu-id="ba314-119">To access project-level Asset libraries from an ER repository that is used to import ER configurations, sign in to Finance by using the credentials of a user who belongs to the tenant (domain) that the current Finance instance has been provisioned for.</span></span>

## <a name="create-a-new-data-model-configuration"></a><span data-ttu-id="ba314-120">สร้างแบบจำลองการจัดโครงแบบข้อมูลใหม่</span><span class="sxs-lookup"><span data-stu-id="ba314-120">Create a new data model configuration</span></span>

1. <span data-ttu-id="ba314-121">ไปที่ **การจัดการองค์กร \> การรายงานทางอิเล็กทรอนิกส์ \> การตั้งค่าคอนฟิก**</span><span class="sxs-lookup"><span data-stu-id="ba314-121">Go to **Organization administration \> Electronic reporting \> Configurations**.</span></span>
2. <span data-ttu-id="ba314-122">ในหน้า **การตั้งค่าคอนฟิก** เลือก **สร้างการตั้งค่าคอนฟิก** เพื่อเปิดกล่องโต้ตอบแบบหล่นลง</span><span class="sxs-lookup"><span data-stu-id="ba314-122">On the **Configurations** page, select **Create configuration** to open the drop-down dialog box.</span></span>

    <span data-ttu-id="ba314-123">ในตัวอย่างนี้ คุณจะสร้างการตั้งค่าคอนฟิกที่ประกอบด้วย รูปแบบข้อมูลตัวอย่างสำหรับเอกสารทางอิเล็กทรอนิกส์</span><span class="sxs-lookup"><span data-stu-id="ba314-123">In this example, you will create a configuration that contains a sample data model for electronic documents.</span></span> <span data-ttu-id="ba314-124">การตั้งค่าคอนฟิกรูปแบบข้อมูลนี้จะถูกอัปโหลดลงใน LCS ในภายหลัง</span><span class="sxs-lookup"><span data-stu-id="ba314-124">This data model configuration will be uploaded into LCS later.</span></span>

3. <span data-ttu-id="ba314-125">ในฟิลด์ **ชื่อ** ป้อน **การตั้งค่าคอนฟิกแบบจำลองตัวอย่าง**</span><span class="sxs-lookup"><span data-stu-id="ba314-125">In the **Name** field, enter **Sample model configuration**.</span></span>
4. <span data-ttu-id="ba314-126">ในฟิลด์ **คำอธิบาย** ป้อน **การตั้งค่าคอนฟิกแบบจำลองตัวอย่าง**</span><span class="sxs-lookup"><span data-stu-id="ba314-126">In the **Description** field, enter **Sample model configuration**.</span></span>
5. <span data-ttu-id="ba314-127">เลือก **สร้างการตั้งค่าคอนฟิก**</span><span class="sxs-lookup"><span data-stu-id="ba314-127">Select **Create configuration**.</span></span>
6. <span data-ttu-id="ba314-128">เลือก **ตัวออกแบบแบบจำลอง**</span><span class="sxs-lookup"><span data-stu-id="ba314-128">Select **Model designer**.</span></span>
7. <span data-ttu-id="ba314-129">เลือก **ใหม่**</span><span class="sxs-lookup"><span data-stu-id="ba314-129">Select **New**.</span></span>
8. <span data-ttu-id="ba314-130">ในฟิลด์ **ชื่อ** ป้อน **จุดเข้าใช้งาน**</span><span class="sxs-lookup"><span data-stu-id="ba314-130">In the **Name** field, enter **Entry point**.</span></span>
9. <span data-ttu-id="ba314-131">เลือก **เพิ่ม**</span><span class="sxs-lookup"><span data-stu-id="ba314-131">Select **Add**.</span></span>
10. <span data-ttu-id="ba314-132">เลือก **บันทึก**</span><span class="sxs-lookup"><span data-stu-id="ba314-132">Select **Save**.</span></span>
11. <span data-ttu-id="ba314-133">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="ba314-133">Close the page.</span></span>
12. <span data-ttu-id="ba314-134">เลือก **เปลี่ยนแปลงสถานะ**</span><span class="sxs-lookup"><span data-stu-id="ba314-134">Select **Change status**.</span></span>
13. <span data-ttu-id="ba314-135">เลือก **เสร็จสมบูรณ์**</span><span class="sxs-lookup"><span data-stu-id="ba314-135">Select **Complete**.</span></span>
14. <span data-ttu-id="ba314-136">เลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="ba314-136">Select **OK**.</span></span>
15. <span data-ttu-id="ba314-137">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="ba314-137">Close the page.</span></span>

## <a name="register-a-new-repository"></a><span data-ttu-id="ba314-138">ลงทะเบียนที่จัดเก็บใหม่</span><span class="sxs-lookup"><span data-stu-id="ba314-138">Register a new repository</span></span>

1. <span data-ttu-id="ba314-139">ไปที่ **การจัดการองค์กร \> พื้นที่ทำงาน \> การรายงานทางอิเล็กทรอนิกส์**</span><span class="sxs-lookup"><span data-stu-id="ba314-139">Go to **Organization administration \> Workspaces \> Electronic reporting**.</span></span>

2. <span data-ttu-id="ba314-140">ในส่วน **ผู้ให้บริการการตั้งค่าคอนฟิก** เลือกไทล์ **Litware, Inc.**</span><span class="sxs-lookup"><span data-stu-id="ba314-140">In the **Configuration providers** section, select the **Litware, Inc.** tile.</span></span>

3. <span data-ttu-id="ba314-141">บนไทล์ **Litware, Inc.** เลือก **ที่เก็บ**</span><span class="sxs-lookup"><span data-stu-id="ba314-141">On the **Litware, Inc.** tile, select **Repositories**.</span></span>

    <span data-ttu-id="ba314-142">ตอนนี้คุณสามารถเปิดรายการของที่เก็บสำหรับผู้ให้บริการการตั้งค่าคอนฟิก Litware, Inc.</span><span class="sxs-lookup"><span data-stu-id="ba314-142">You can now open the list of repositories for the Litware, Inc. configuration provider.</span></span>

4. <span data-ttu-id="ba314-143">เลือก **เพิ่ม** เพื่อเปิดกล่องโต้ตอบแบบหล่นลง</span><span class="sxs-lookup"><span data-stu-id="ba314-143">Select **Add** to open the drop-down dialog box.</span></span>

    <span data-ttu-id="ba314-144">ขณะนี้คุณสามารถเพิ่มที่เก็บใหม่ได้แล้ว</span><span class="sxs-lookup"><span data-stu-id="ba314-144">You can now add a new repository.</span></span>

5. <span data-ttu-id="ba314-145">ในฟิลด์ **ชนิดที่เก็บการตั้งค่าคอนฟิก** ให้เลือก **LCS**</span><span class="sxs-lookup"><span data-stu-id="ba314-145">In the **Configuration repository enter** field, select **LCS**.</span></span>
6. <span data-ttu-id="ba314-146">เลือก **สร้างที่เก็บ**</span><span class="sxs-lookup"><span data-stu-id="ba314-146">Select **Create repository**.</span></span>
7. <span data-ttu-id="ba314-147">ในฟิลด์ **โครงการ** ให้ป้อนหรือเลือกค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="ba314-147">In the **Project** field, enter or select a value.</span></span>

    <span data-ttu-id="ba314-148">สำหรับตัวอย่างนี้ ให้เลือกโครงการ LCS ที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="ba314-148">For this example, select the desired LCS project.</span></span> <span data-ttu-id="ba314-149">คุณต้องมีสิทธิ์ [เข้าถึง](#accessconditions) โครงการ</span><span class="sxs-lookup"><span data-stu-id="ba314-149">You must have [access](#accessconditions) to the project.</span></span>

8. <span data-ttu-id="ba314-150">เลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="ba314-150">Select **OK**.</span></span>

    <span data-ttu-id="ba314-151">ดำเนินการรายการที่เก็บใหม่ให้เสร็จสมบูรณ์</span><span class="sxs-lookup"><span data-stu-id="ba314-151">Complete a new repository entry.</span></span>

9. <span data-ttu-id="ba314-152">ในรายการนี้ ให้ทำเครื่องหมายแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="ba314-152">In the list, mark the selected row.</span></span>

    <span data-ttu-id="ba314-153">สำหรับตัวอย่างนี้ ให้เลือกเรกคอร์ดที่เก็บ **LCS**</span><span class="sxs-lookup"><span data-stu-id="ba314-153">For this example, select the **LCS** repository record.</span></span>

    <span data-ttu-id="ba314-154">โปรดสังเกตว่ามีการทำเครื่องหมายที่เก็บที่ลงทะเบียนไว้โดยผู้ให้บริการปัจจุบัน</span><span class="sxs-lookup"><span data-stu-id="ba314-154">Note that a registered repository is marked by the current provider.</span></span> <span data-ttu-id="ba314-155">กล่าวคือ การตั้งค่าคอนฟิกเฉพาะที่เป็นของผู้ให้บริการดังกล่าวเท่านั้นที่สามารถวางในที่เก็บนี้และสามารถอัปโหลดไปยังโครงการ LCS ที่เลือก</span><span class="sxs-lookup"><span data-stu-id="ba314-155">In other words, only configurations that are owned by that provider can be put in this repository and therefore uploaded into the selected LCS project.</span></span>

10. <span data-ttu-id="ba314-156">เลือก **เปิด**</span><span class="sxs-lookup"><span data-stu-id="ba314-156">Select **Open**.</span></span>

    <span data-ttu-id="ba314-157">คุณเปิดที่เก็บเพื่อดูรายการของการตั้งค่าคอนฟิก ER</span><span class="sxs-lookup"><span data-stu-id="ba314-157">You open the repository to view the list of ER configurations.</span></span> <span data-ttu-id="ba314-158">ถ้าโครงการที่เลือกยังไม่ได้ใช้สำหรับการใช้การตั้งค่าคอนฟิก ER ร่วมกัน รายการนี้จะว่างเปล่า</span><span class="sxs-lookup"><span data-stu-id="ba314-158">If the selected project hasn't yet been used for ER configurations sharing, the list will be empty.</span></span>

11. <span data-ttu-id="ba314-159">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="ba314-159">Close the page.</span></span>
12. <span data-ttu-id="ba314-160">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="ba314-160">Close the page.</span></span>

## <a name="upload-a-configuration-into-lcs"></a><span data-ttu-id="ba314-161">อัปโหลดการตั้งค่าคอนฟิกไปยัง LCS</span><span class="sxs-lookup"><span data-stu-id="ba314-161">Upload a configuration into LCS</span></span>

1. <span data-ttu-id="ba314-162">ไปที่ **การจัดการองค์กร \> การรายงานทางอิเล็กทรอนิกส์ \> การตั้งค่าคอนฟิก**</span><span class="sxs-lookup"><span data-stu-id="ba314-162">Go to **Organization administration \> Electronic reporting \> Configurations**.</span></span>
2. <span data-ttu-id="ba314-163">บนหน้า **การตั้งค่าคอนฟิก** ในแผนภูมิการตั้งค่าคอนฟิก เลือก **การตั้งค่าคอนฟิกแบบจำลองตัวอย่าง**</span><span class="sxs-lookup"><span data-stu-id="ba314-163">On the **Configurations** page, in the configurations tree, select **Sample model configuration**.</span></span>

    <span data-ttu-id="ba314-164">คุณต้องเลือกการตั้งค่าคอนฟิกที่สร้างขึ้น ซึ่งได้เสร็จสมบูรณ์แล้ว</span><span class="sxs-lookup"><span data-stu-id="ba314-164">You must select a created configuration that has been already completed.</span></span>

3. <span data-ttu-id="ba314-165">ในรายการนี้ ให้ค้นหาและเลือกเรกคอร์ดที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="ba314-165">In the list, find and select the desired record.</span></span>

    <span data-ttu-id="ba314-166">สำหรับตัวอย่างนี้ เลือกรุ่นของการตั้งค่าคอนฟิกที่เลือกที่มีสถานะเป็น **เสร็จสมบูรณ์แล้ว**</span><span class="sxs-lookup"><span data-stu-id="ba314-166">For this example, select the version of the selected configuration that has a status of **Completed**.</span></span>

4. <span data-ttu-id="ba314-167">เลือก **เปลี่ยนแปลงสถานะ**</span><span class="sxs-lookup"><span data-stu-id="ba314-167">Select **Change status**.</span></span>
5. <span data-ttu-id="ba314-168">เลือก **ใช้ร่วมกัน**</span><span class="sxs-lookup"><span data-stu-id="ba314-168">Select **Share**.</span></span>

    <span data-ttu-id="ba314-169">สถานะของการตั้งค่าคอนฟิกมีการเปลี่ยนแปลงจาก **เสร็จสมบูรณ์แล้ว** เป็น **ใช้ร่วมกัน** เมื่อมีการเผยแพร่การตั้งค่าคอนฟิกใน LCS</span><span class="sxs-lookup"><span data-stu-id="ba314-169">The status of the configuration is changed from **Completed** to **Shared** when the configuration is published in LCS.</span></span>

6. <span data-ttu-id="ba314-170">เลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="ba314-170">Select **OK**.</span></span>
7. <span data-ttu-id="ba314-171">ในรายการนี้ ให้ค้นหาและเลือกเรกคอร์ดที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="ba314-171">In the list, find and select the desired record.</span></span>

    <span data-ttu-id="ba314-172">สำหรับตัวอย่างนี้ เลือกรุ่นของการตั้งค่าคอนฟิกซึ่งมีสถานะเป็น **ใช้ร่วมกัน**</span><span class="sxs-lookup"><span data-stu-id="ba314-172">For this example, select the configuration version that has a status of **Shared**.</span></span>

    <span data-ttu-id="ba314-173">หมายเหตุว่า สถานะของรุ่นที่เลือกได้เปลี่ยนจาก **เสร็จสมบูรณ์แล้ว** เป็น **ใช้ร่วมกัน**</span><span class="sxs-lookup"><span data-stu-id="ba314-173">Note that the status of the selected version was changed from **Completed** to **Shared**.</span></span>

8. <span data-ttu-id="ba314-174">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="ba314-174">Close the page.</span></span>
9. <span data-ttu-id="ba314-175">เลือก **ที่เก็บ**</span><span class="sxs-lookup"><span data-stu-id="ba314-175">Select **Repositories**.</span></span>

    <span data-ttu-id="ba314-176">ตอนนี้คุณสามารถเปิดรายการของที่เก็บสำหรับผู้ให้บริการการตั้งค่าคอนฟิก Litware, Inc.</span><span class="sxs-lookup"><span data-stu-id="ba314-176">You can now open the list of repositories for the Litware, Inc. configuration provider.</span></span>

10. <span data-ttu-id="ba314-177">เลือก **เปิด**</span><span class="sxs-lookup"><span data-stu-id="ba314-177">Select **Open**.</span></span>

    <span data-ttu-id="ba314-178">สำหรับตัวอย่างนี้ ให้เลือกเรกคอร์ดที่เก็บ **LCS** และเปิด</span><span class="sxs-lookup"><span data-stu-id="ba314-178">For this example, select the **LCS** repository, and open it.</span></span>

    <span data-ttu-id="ba314-179">โปรดทราบว่า การตั้งค่าคอนฟิกที่เลือกถูกแสดงเป็นสินทรัพย์ของโครงการ LCS ที่เลือก</span><span class="sxs-lookup"><span data-stu-id="ba314-179">Notice that the selected configuration is shown as an asset of the selected LCS project.</span></span>

11. <span data-ttu-id="ba314-180">เปิด LCS โดยไปที่ <https://lcs.dynamics.com></span><span class="sxs-lookup"><span data-stu-id="ba314-180">Open LCS by going to <https://lcs.dynamics.com>.</span></span>
12. <span data-ttu-id="ba314-181">เปิดโครงการที่ใช้ก่อนหน้านี้สำหรับการลงทะเบียนที่จัดเก็บ</span><span class="sxs-lookup"><span data-stu-id="ba314-181">Open a project that was used earlier for repository registration.</span></span>
13. <span data-ttu-id="ba314-182">เปิดแอสเซทไลบรารีของโครงการ</span><span class="sxs-lookup"><span data-stu-id="ba314-182">Open the Asset library of the project.</span></span>
14. <span data-ttu-id="ba314-183">เลือกชนิดแอสเซท **การตั้งค่าคอนฟิก GER**</span><span class="sxs-lookup"><span data-stu-id="ba314-183">Select the **GER configuration** asset type.</span></span>

    <span data-ttu-id="ba314-184">ระบบควรแสดงการตั้งค่าคอนฟิก ER ที่คุณอัปโหลดไว้</span><span class="sxs-lookup"><span data-stu-id="ba314-184">The ER configuration that you uploaded should be listed.</span></span>

    <span data-ttu-id="ba314-185">โปรดทราบว่า การตั้งค่าคอนฟิก LCS ที่อัปโหลดสามารถถูกนำเข้าไปยังอินสแตนซ์อื่นได้ หากผู้ให้บริการมีการเข้าถึงไปยังโครงการ LCS นี้</span><span class="sxs-lookup"><span data-stu-id="ba314-185">Note that the uploaded LCS configuration can be imported into another instance if providers have access to this LCS project.</span></span>


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]
