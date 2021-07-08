---
title: นำเข้าการตั้งค่าคอนฟิกจาก Lifecycle Services
description: หัวข้อนี้อธิบายวิธีการนําเข้าการตั้งค่าคอนฟิกการรายงานทางอิเล็กทรอนิกส์ (ER) เวอร์ชันใหม่ จาก Microsoft Dynamics Lifecycle Services (LCS)
author: NickSelin
ms.date: 06/17/2021
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: ERWorkspace, ERSolutionTable, ERSolutionRepositoryTable, ERSolutionImport
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: b58ecb8a7d6f52631dbca7642a4acbcf6ff895a3
ms.sourcegitcommit: dc4898aa32f381620c517bf89c7856e693563ace
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 06/17/2021
ms.locfileid: "6270848"
---
# <a name="import-a-configuration-from-lifecycle-services"></a><span data-ttu-id="b69c8-103">นำเข้าการตั้งค่าคอนฟิกจาก Lifecycle Services</span><span class="sxs-lookup"><span data-stu-id="b69c8-103">Import a configuration from Lifecycle Services</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="b69c8-104">หัวข้อนี้อธิบายวิธีที่ผู้ใช้ในบทบาทผู้ดูแลระบบ หรือนักพัฒนาการรายงานทางอิเล็กทรอนิกส์ สามารถนำเข้า [การตั้งค่าคอนฟิกการรายงานทางอิเล็กทรอนิกส์ (ER)](../general-electronic-reporting.md#Configuration) รุ่นใหม่จาก [แอสเซทไลบรารีระดับโครงการ](../../lifecycle-services/asset-library.md) ใน Microsoft Dynamics Lifecycle Services (LCS)</span><span class="sxs-lookup"><span data-stu-id="b69c8-104">This topic explains how a user in the System administrator or Electronic reporting developer role can import a new version of an [Electronic reporting (ER) configuration](../general-electronic-reporting.md#Configuration) from the [project-level Asset library](../../lifecycle-services/asset-library.md) in Microsoft Dynamics Lifecycle Services (LCS).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="b69c8-105">การใช้ LCS เป็นที่เก็บหน่วยจัดเก็บเพื่อการตั้งค่าคอนฟิก ER [ไม่ได้รับการสนับสนุน](../../../../finance/get-started/removed-deprecated-features-finance.md#features-removed-or-deprecated-in-the-finance-10017-release)</span><span class="sxs-lookup"><span data-stu-id="b69c8-105">The use of LCS as a storage repository for ER configurations is being [deprecated](../../../../finance/get-started/removed-deprecated-features-finance.md#features-removed-or-deprecated-in-the-finance-10017-release).</span></span> <span data-ttu-id="b69c8-106">สำหรับข้อมูลเพิ่มเติม ให้ดู [Regulatory Configuration Service (RCS) – การเลิกใช้ที่เก็บข้อมูล Lifecycle Services (LCS)](../../../../finance/localizations/rcs-lcs-repo-dep-faq.md)</span><span class="sxs-lookup"><span data-stu-id="b69c8-106">For more information, see [Regulatory Configuration Service (RCS) – Lifecycle Services (LCS) storage deprecation](../../../../finance/localizations/rcs-lcs-repo-dep-faq.md).</span></span>

<span data-ttu-id="b69c8-107">ในตัวอย่างนี้ คุณจะสร้างเลือกรุ่นที่ต้องการของการตั้งค่าคอนฟิก ER และนำเข้าสำหรับบริษัทตัวอย่าง ซึ่งคือ Litware, inc ขั้นตอนเหล่านี้สามารถถูกดำเนินการได้ในบริษัทใดๆ เนื่องจากมีการใช้การตั้งค่าคอนฟิก ER ร่วมกันระหว่างบริษัท</span><span class="sxs-lookup"><span data-stu-id="b69c8-107">In this example, you will select the desired version of the ER configuration and import it for a sample company that is named Litware, Inc. These steps can be completed in any company, because ER configurations are shared among companies.</span></span> <span data-ttu-id="b69c8-108">เมื่อต้องการดำเนินขั้นตอนเหล่านี้ให้เสร็จสมบูรณ์ ลำดับแรกคุณต้องดำเนินงานขั้นตอนใน [อัปโหลดการตั้งค่าคอนฟิก ER ลงใน Lifecycle Services](er-upload-configuration-into-lifecycle-services.md)</span><span class="sxs-lookup"><span data-stu-id="b69c8-108">To complete these steps, you must first complete the steps in [Upload a configuration into Lifecycle Services](er-upload-configuration-into-lifecycle-services.md).</span></span> <span data-ttu-id="b69c8-109">ต้องมีสิทธิ์เข้าถึง LCS ด้วยเช่นกัน</span><span class="sxs-lookup"><span data-stu-id="b69c8-109">Access to LCS is also required.</span></span>

1. <span data-ttu-id="b69c8-110">ลงชื่อเข้าใช้ในแอพลิเคชันโดยใช้หนึ่งในบทบาทต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="b69c8-110">Sign in to the application by using one of the following roles:</span></span>

    - <span data-ttu-id="b69c8-111">นักพัฒนาการรายงานทางอิเล็กทรอนิกส์</span><span class="sxs-lookup"><span data-stu-id="b69c8-111">Electronic reporting developer</span></span>
    - <span data-ttu-id="b69c8-112">ผู้ดูแลระบบ</span><span class="sxs-lookup"><span data-stu-id="b69c8-112">System administrator</span></span>

2. <span data-ttu-id="b69c8-113">ไปที่ **การจัดการองค์กร** \> **พื้นที่ทำงาน** \> **การรายงานทางอิเล็กทรอนิกส์**</span><span class="sxs-lookup"><span data-stu-id="b69c8-113">Go to **Organization administration** \> **Workspaces** \> **Electronic reporting**.</span></span>
3. <span data-ttu-id="b69c8-114">เลือก **การตั้งค่าคอนฟิก**</span><span class="sxs-lookup"><span data-stu-id="b69c8-114">Select **Configurations**.</span></span>

<a name="accessconditions"></a>
> [!NOTE]
> <span data-ttu-id="b69c8-115">ตรวจสอบให้แน่ใจว่าผู้ใช้ Dynamics 365 Finance ปัจจุบันเป็นสมาชิกของโครงการ LCS ที่มีแอสเซทไลบรารีที่ผู้ใช้ต้องการสิทธิ์ [เข้าถึง](../../lifecycle-services/asset-library.md#asset-library-support) เพื่อนำเข้าการตั้งค่าคอนฟิก ER</span><span class="sxs-lookup"><span data-stu-id="b69c8-115">Make sure that the current Dynamics 365 Finance user is a member of the LCS project that contains the Asset library that the user wants to [access](../../lifecycle-services/asset-library.md#asset-library-support) to import ER configurations.</span></span>
>
> <span data-ttu-id="b69c8-116">คุณไม่สามารถเข้าถึงโครงการ LCS จากที่เก็บ ER ซึ่งแสดงถึงโดเมนอื่นที่ไม่ใช่โดเมนที่ใช้ใน Finance</span><span class="sxs-lookup"><span data-stu-id="b69c8-116">You can't access an LCS project from an ER repository that represents a different domain than the domain that is used in Finance.</span></span> <span data-ttu-id="b69c8-117">ถ้าคุณพยายาม จะมีการแสดงรายการที่ว่างเปล่าของโครงการ LCS และคุณจะไม่สามารถนำเข้าการตั้งค่าคอนฟิก ER จากแอสเซทไลบรารีระดับโครงการใน LCS</span><span class="sxs-lookup"><span data-stu-id="b69c8-117">If you try, an empty list of LCS projects will be shown, and you won't be able to import ER configurations from the project-level Asset library in LCS.</span></span> <span data-ttu-id="b69c8-118">ถ้าต้องการเข้าถึงแอสเซทไลบรารีระดับโครงการจากที่เก็บ ER ซึ่งใช้ในการนำเข้าการตั้งค่าคอนฟิก ER ให้ลงชื่อเข้าใช้ Finance โดยใช้ข้อมูลประจำตัวของผู้ใช้ที่เป็นสมาชิกของผู้เช่า (โดเมน) ที่มีการเตรียมใช้งานอินสแตนซ์ Finance ในปัจจุบัน</span><span class="sxs-lookup"><span data-stu-id="b69c8-118">To access project-level Asset libraries from an ER repository that is used to import ER configurations, sign in to Finance by using the credentials of a user who belongs to the tenant (domain) that the current Finance instance has been provisioned for.</span></span>

## <a name="delete-a-shared-version-of-a-data-model-configuration"></a><span data-ttu-id="b69c8-119">ลบเวอร์ชันที่ใช้ร่วมกันของการตั้งค่าคอนฟิกรูปแบบข้อมูล</span><span class="sxs-lookup"><span data-stu-id="b69c8-119">Delete a shared version of a data model configuration</span></span>

1. <span data-ttu-id="b69c8-120">บนหน้า **การตั้งค่าคอนฟิก** ในแผนภูมิการตั้งค่าคอนฟิก เลือก **การตั้งค่าคอนฟิกแบบจำลองตัวอย่าง**</span><span class="sxs-lookup"><span data-stu-id="b69c8-120">On the **Configurations** page, in the configurations tree, select **Sample model configuration**.</span></span>

    <span data-ttu-id="b69c8-121">คุณสร้างการตั้งค่าคอนฟิกรูปแบบข้อมูลตัวอย่างรุ่นแรกและเผยแพร่ไปยัง LCS เมื่อคุณทำตามขั้นตอนใน [อัปโหลดการตั้งค่าคอนฟิกไปยัง Lifecycle Services](er-upload-configuration-into-lifecycle-services.md)</span><span class="sxs-lookup"><span data-stu-id="b69c8-121">You created the first version of a sample data model configuration and published it to LCS when you completed the steps in [Upload a configuration into Lifecycle Services](er-upload-configuration-into-lifecycle-services.md).</span></span> <span data-ttu-id="b69c8-122">ในกระบวนงานนี้ คุณจะลบรุ่นนั้นของการตั้งค่าคอนฟิก ER</span><span class="sxs-lookup"><span data-stu-id="b69c8-122">In this procedure, you will delete that version of the ER configuration.</span></span> <span data-ttu-id="b69c8-123">จากนั้นคุณจะนำเข้ารุ่นดังกล่าวจาก LCS ภายหลังในหัวข้อนี้</span><span class="sxs-lookup"><span data-stu-id="b69c8-123">You will then import that version from LCS later in this topic.</span></span>

2. <span data-ttu-id="b69c8-124">ในรายการนี้ ให้ค้นหาและเลือกเรกคอร์ดที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="b69c8-124">In the list, find and select the desired record.</span></span>

    <span data-ttu-id="b69c8-125">สำหรับตัวอย่างนี้ เลือกรุ่นของการตั้งค่าคอนฟิกซึ่งมีสถานะเป็น **ใช้ร่วมกัน**</span><span class="sxs-lookup"><span data-stu-id="b69c8-125">For this example, select the version of the configuration that has a status of **Shared**.</span></span> <span data-ttu-id="b69c8-126">สถานะนี้ระบุว่าการตั้งค่าคอนฟิกได้ถูกเผยแพร่ไปยัง LCS แล้ว</span><span class="sxs-lookup"><span data-stu-id="b69c8-126">This status indicates that the configuration has been published to LCS.</span></span>

3. <span data-ttu-id="b69c8-127">เลือก **เปลี่ยนแปลงสถานะ**</span><span class="sxs-lookup"><span data-stu-id="b69c8-127">Select **Change status**.</span></span>
4. <span data-ttu-id="b69c8-128">เลือก **ยกเลิกการดำเนินการต่อ**</span><span class="sxs-lookup"><span data-stu-id="b69c8-128">Select **Discontinue**.</span></span>

    <span data-ttu-id="b69c8-129">ด้วยการเปลี่ยนสถานะของรุ่นที่เลือกจาก **ใช้ร่วมกัน** เป็น **ยกเลิกการดำเนินการต่อ** คุณจะทำให้พร้อมใช้งานสำหรับการลบ</span><span class="sxs-lookup"><span data-stu-id="b69c8-129">By changing the status of the selected version from **Shared** to **Discontinued**, you make the version available for deletion.</span></span>

5. <span data-ttu-id="b69c8-130">เลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="b69c8-130">Select **OK**.</span></span>
6. <span data-ttu-id="b69c8-131">ในรายการนี้ ให้ค้นหาและเลือกเรกคอร์ดที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="b69c8-131">In the list, find and select the desired record.</span></span>

    <span data-ttu-id="b69c8-132">สำหรับตัวอย่างนี้ เลือกรุ่นของการตั้งค่าคอนฟิกซึ่งมีสถานะเป็น **ยกเลิกการดำเนินการต่อ**</span><span class="sxs-lookup"><span data-stu-id="b69c8-132">For this example, select the version of the configuration that has a status of **Discontinued**.</span></span>

7. <span data-ttu-id="b69c8-133">เลือก **ลบ**</span><span class="sxs-lookup"><span data-stu-id="b69c8-133">Select **Delete**.</span></span>
8. <span data-ttu-id="b69c8-134">เลือก **ใช่**</span><span class="sxs-lookup"><span data-stu-id="b69c8-134">Select **Yes**.</span></span>

    <span data-ttu-id="b69c8-135">สังเกตว่า เฉพาะแบบร่างเวอร์ชัน 2 ของการตั้งค่าคอนฟิกรูปแบบข้อมูลพร้อมใช้งานแล้ว</span><span class="sxs-lookup"><span data-stu-id="b69c8-135">Notice that the only draft version 2 of the selected data model configuration is now available.</span></span>

9. <span data-ttu-id="b69c8-136">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="b69c8-136">Close the page.</span></span>

## <a name="import-a-shared-version-of-a-data-model-configuration-from-lcs"></a><span data-ttu-id="b69c8-137">นำเข้าเวอร์ชันที่ใช้ร่วมกันของการตั้งค่าคอนฟิกรูปแบบข้อมูลจาก LCS</span><span class="sxs-lookup"><span data-stu-id="b69c8-137">Import a shared version of a data model configuration from LCS</span></span>

1. <span data-ttu-id="b69c8-138">ไปที่ **การจัดการองค์กร \> พื้นที่ทำงาน \> การรายงานทางอิเล็กทรอนิกส์**</span><span class="sxs-lookup"><span data-stu-id="b69c8-138">Go to **Organization administration \> Workspaces \> Electronic reporting**.</span></span>

2. <span data-ttu-id="b69c8-139">ในส่วน **ผู้ให้บริการการตั้งค่าคอนฟิก** เลือกไทล์ **Litware, Inc.**</span><span class="sxs-lookup"><span data-stu-id="b69c8-139">In the **Configuration providers** section, select the **Litware, Inc.** tile.</span></span>

3. <span data-ttu-id="b69c8-140">บนไทล์ **Litware, Inc.** เลือก **ที่เก็บ**</span><span class="sxs-lookup"><span data-stu-id="b69c8-140">On the **Litware, Inc.** tile, select **Repositories**.</span></span>

    <span data-ttu-id="b69c8-141">ตอนนี้คุณสามารถเปิดรายการของที่เก็บสำหรับผู้ให้บริการการตั้งค่าคอนฟิก Litware, Inc.</span><span class="sxs-lookup"><span data-stu-id="b69c8-141">You can now open the list of repositories for the Litware, Inc. configuration provider.</span></span>

4. <span data-ttu-id="b69c8-142">เลือก **เปิด**</span><span class="sxs-lookup"><span data-stu-id="b69c8-142">Select **Open**.</span></span>

    <span data-ttu-id="b69c8-143">สำหรับตัวอย่างนี้ ให้เลือกเรกคอร์ดที่เก็บ **LCS** และเปิด</span><span class="sxs-lookup"><span data-stu-id="b69c8-143">For this example, select the **LCS** repository, and open it.</span></span> <span data-ttu-id="b69c8-144">คุณต้องมีสิทธิ์ [เข้าถึง](#accessconditions) โครงการ LCS และไปยังแอสเซทไลบรารีที่มีการเข้าถึงโดยที่เก็บ ER ที่เลือก</span><span class="sxs-lookup"><span data-stu-id="b69c8-144">You must have [access](#accessconditions) to the LCS project and to the Asset library that is accessed by the selected ER repository.</span></span>

5. <span data-ttu-id="b69c8-145">ในรายการนี้ ให้ทำเครื่องหมายแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="b69c8-145">In the list, mark the selected row.</span></span>

    <span data-ttu-id="b69c8-146">สำหรับตัวอย่างนี้ ให้เลือกรุ่นแรกของ **การตั้งค่าคอนฟิกรูปแบบตัวอย่าง** ในรายการรุ่น</span><span class="sxs-lookup"><span data-stu-id="b69c8-146">For this example, select the first version of **Sample model configuration** in the version list.</span></span>

6. <span data-ttu-id="b69c8-147">เลือก **นำเข้า**</span><span class="sxs-lookup"><span data-stu-id="b69c8-147">Select **Import**.</span></span>
7. <span data-ttu-id="b69c8-148">เลือก **ใช่** เพื่อยืนยันการนำเข้ารุ่นที่เลือกจาก LCS</span><span class="sxs-lookup"><span data-stu-id="b69c8-148">Select **Yes** to confirm the import of the selected version from LCS.</span></span>

    <span data-ttu-id="b69c8-149">ข้อความที่ให้ข้อมูลยืนยันว่ามีการนำเข้ารุ่นที่เลือกเสร็จเรียบร้อยแล้ว</span><span class="sxs-lookup"><span data-stu-id="b69c8-149">An informational message confirms that the selected version was successfully imported.</span></span>

8. <span data-ttu-id="b69c8-150">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="b69c8-150">Close the page.</span></span>
9. <span data-ttu-id="b69c8-151">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="b69c8-151">Close the page.</span></span>
10. <span data-ttu-id="b69c8-152">เลือก **การตั้งค่าคอนฟิก**</span><span class="sxs-lookup"><span data-stu-id="b69c8-152">Select **Configurations**.</span></span>
11. <span data-ttu-id="b69c8-153">ในแผนภูมิ เลือก **การตั้งค่าคอนฟิกรูปแบบตัวอย่าง**</span><span class="sxs-lookup"><span data-stu-id="b69c8-153">In the tree, select **Sample model configuration**.</span></span>
12. <span data-ttu-id="b69c8-154">ในรายการนี้ ให้ค้นหาและเลือกเรกคอร์ดที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="b69c8-154">In the list, find and select the desired record.</span></span>

    <span data-ttu-id="b69c8-155">สำหรับตัวอย่างนี้ เลือกรุ่นของการตั้งค่าคอนฟิกซึ่งมีสถานะเป็น **ใช้ร่วมกัน**</span><span class="sxs-lookup"><span data-stu-id="b69c8-155">For this example, select the version of the configuration that has a status of **Shared**.</span></span>

    <span data-ttu-id="b69c8-156">สังเกตว่า รุ่นที่ใช้ร่วมกัน 1 ของการตั้งค่าคอนฟิกรูปแบบข้อมูลที่เลือกพร้อมใช้งานแล้วในขณะนี้</span><span class="sxs-lookup"><span data-stu-id="b69c8-156">Notice that shared version 1 of the selected data model configuration is also available now.</span></span>


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]
