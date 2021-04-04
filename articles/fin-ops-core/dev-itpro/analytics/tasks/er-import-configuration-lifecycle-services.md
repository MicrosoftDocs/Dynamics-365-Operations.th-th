---
title: นำเข้าการตั้งค่าคอนฟิกจาก Lifecycle Services
description: หัวข้อนี้อธิบายวิธีการนําเข้าการตั้งค่าคอนฟิกการรายงานทางอิเล็กทรอนิกส์ (ER) เวอร์ชันใหม่ จาก Microsoft Dynamics Lifecycle Services (LCS)
author: NickSelin
manager: AnnBe
ms.date: 09/14/2020
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
ms.openlocfilehash: 636ed27c157c8322cc1be4ca8eca10ef37eb8bbc
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 03/09/2021
ms.locfileid: "5569520"
---
# <a name="import-a-configuration-from-lifecycle-services"></a><span data-ttu-id="fe089-103">นำเข้าการตั้งค่าคอนฟิกจาก Lifecycle Services</span><span class="sxs-lookup"><span data-stu-id="fe089-103">Import a configuration from Lifecycle Services</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="fe089-104">หัวข้อนี้อธิบายวิธีที่ผู้ใช้ในบทบาทผู้ดูแลระบบ หรือนักพัฒนาการรายงานทางอิเล็กทรอนิกส์ สามารถนำเข้า [การตั้งค่าคอนฟิกการรายงานทางอิเล็กทรอนิกส์ (ER)](../general-electronic-reporting.md#Configuration) รุ่นใหม่จาก [แอสเซทไลบรารีระดับโครงการ](../../lifecycle-services/asset-library.md) ใน Microsoft Dynamics Lifecycle Services (LCS)</span><span class="sxs-lookup"><span data-stu-id="fe089-104">This topic explains how a user in the System administrator or Electronic reporting developer role can import a new version of an [Electronic reporting (ER) configuration](../general-electronic-reporting.md#Configuration) from the [project-level Asset library](../../lifecycle-services/asset-library.md) in Microsoft Dynamics Lifecycle Services (LCS).</span></span>

<span data-ttu-id="fe089-105">ในตัวอย่างนี้ คุณจะสร้างเลือกรุ่นที่ต้องการของการตั้งค่าคอนฟิก ER และนำเข้าสำหรับบริษัทตัวอย่าง ซึ่งคือ Litware, inc ขั้นตอนเหล่านี้สามารถถูกดำเนินการได้ในบริษัทใดๆ เนื่องจากมีการใช้การตั้งค่าคอนฟิก ER ร่วมกันระหว่างบริษัท</span><span class="sxs-lookup"><span data-stu-id="fe089-105">In this example, you will select the desired version of the ER configuration and import it for a sample company that is named Litware, Inc. These steps can be completed in any company, because ER configurations are shared among companies.</span></span> <span data-ttu-id="fe089-106">เมื่อต้องการดำเนินขั้นตอนเหล่านี้ให้เสร็จสมบูรณ์ ลำดับแรกคุณต้องดำเนินงานขั้นตอนใน [อัปโหลดการตั้งค่าคอนฟิก ER ลงใน Lifecycle Services](er-upload-configuration-into-lifecycle-services.md)</span><span class="sxs-lookup"><span data-stu-id="fe089-106">To complete these steps, you must first complete the steps in [Upload a configuration into Lifecycle Services](er-upload-configuration-into-lifecycle-services.md).</span></span> <span data-ttu-id="fe089-107">ต้องมีสิทธิ์เข้าถึง LCS ด้วยเช่นกัน</span><span class="sxs-lookup"><span data-stu-id="fe089-107">Access to LCS is also required.</span></span>

1. <span data-ttu-id="fe089-108">ลงชื่อเข้าใช้ในแอพลิเคชันโดยใช้หนึ่งในบทบาทต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="fe089-108">Sign in to the application by using one of the following roles:</span></span>

    - <span data-ttu-id="fe089-109">นักพัฒนาการรายงานทางอิเล็กทรอนิกส์</span><span class="sxs-lookup"><span data-stu-id="fe089-109">Electronic reporting developer</span></span>
    - <span data-ttu-id="fe089-110">ผู้ดูแลระบบ</span><span class="sxs-lookup"><span data-stu-id="fe089-110">System administrator</span></span>

2. <span data-ttu-id="fe089-111">ไปที่ **การจัดการองค์กร** \> **พื้นที่ทำงาน** \> **การรายงานทางอิเล็กทรอนิกส์**</span><span class="sxs-lookup"><span data-stu-id="fe089-111">Go to **Organization administration** \> **Workspaces** \> **Electronic reporting**.</span></span>
3. <span data-ttu-id="fe089-112">เลือก **การตั้งค่าคอนฟิก**</span><span class="sxs-lookup"><span data-stu-id="fe089-112">Select **Configurations**.</span></span>

<a name="accessconditions"></a>
> [!NOTE]
> <span data-ttu-id="fe089-113">ตรวจสอบให้แน่ใจว่าผู้ใช้ Dynamics 365 Finance ปัจจุบันเป็นสมาชิกของโครงการ LCS ที่มีแอสเซทไลบรารีที่ผู้ใช้ต้องการสิทธิ์ [เข้าถึง](../../lifecycle-services/asset-library.md#asset-library-support) เพื่อนำเข้าการตั้งค่าคอนฟิก ER</span><span class="sxs-lookup"><span data-stu-id="fe089-113">Make sure that the current Dynamics 365 Finance user is a member of the LCS project that contains the Asset library that the user wants to [access](../../lifecycle-services/asset-library.md#asset-library-support) to import ER configurations.</span></span>
>
> <span data-ttu-id="fe089-114">คุณไม่สามารถเข้าถึงโครงการ LCS จากที่เก็บ ER ซึ่งแสดงถึงโดเมนอื่นที่ไม่ใช่โดเมนที่ใช้ใน Finance</span><span class="sxs-lookup"><span data-stu-id="fe089-114">You can't access an LCS project from an ER repository that represents a different domain than the domain that is used in Finance.</span></span> <span data-ttu-id="fe089-115">ถ้าคุณพยายาม จะมีการแสดงรายการที่ว่างเปล่าของโครงการ LCS และคุณจะไม่สามารถนำเข้าการตั้งค่าคอนฟิก ER จากแอสเซทไลบรารีระดับโครงการใน LCS</span><span class="sxs-lookup"><span data-stu-id="fe089-115">If you try, an empty list of LCS projects will be shown, and you won't be able to import ER configurations from the project-level Asset library in LCS.</span></span> <span data-ttu-id="fe089-116">ถ้าต้องการเข้าถึงแอสเซทไลบรารีระดับโครงการจากที่เก็บ ER ซึ่งใช้ในการนำเข้าการตั้งค่าคอนฟิก ER ให้ลงชื่อเข้าใช้ Finance โดยใช้ข้อมูลประจำตัวของผู้ใช้ที่เป็นสมาชิกของผู้เช่า (โดเมน) ที่มีการเตรียมใช้งานอินสแตนซ์ Finance ในปัจจุบัน</span><span class="sxs-lookup"><span data-stu-id="fe089-116">To access project-level Asset libraries from an ER repository that is used to import ER configurations, sign in to Finance by using the credentials of a user who belongs to the tenant (domain) that the current Finance instance has been provisioned for.</span></span>

## <a name="delete-a-shared-version-of-a-data-model-configuration"></a><span data-ttu-id="fe089-117">ลบเวอร์ชันที่ใช้ร่วมกันของการตั้งค่าคอนฟิกรูปแบบข้อมูล</span><span class="sxs-lookup"><span data-stu-id="fe089-117">Delete a shared version of a data model configuration</span></span>

1. <span data-ttu-id="fe089-118">บนหน้า **การตั้งค่าคอนฟิก** ในแผนภูมิการตั้งค่าคอนฟิก เลือก **การตั้งค่าคอนฟิกแบบจำลองตัวอย่าง**</span><span class="sxs-lookup"><span data-stu-id="fe089-118">On the **Configurations** page, in the configurations tree, select **Sample model configuration**.</span></span>

    <span data-ttu-id="fe089-119">คุณสร้างการตั้งค่าคอนฟิกรูปแบบข้อมูลตัวอย่างรุ่นแรกและเผยแพร่ไปยัง LCS เมื่อคุณทำตามขั้นตอนใน [อัปโหลดการตั้งค่าคอนฟิกไปยัง Lifecycle Services](er-upload-configuration-into-lifecycle-services.md)</span><span class="sxs-lookup"><span data-stu-id="fe089-119">You created the first version of a sample data model configuration and published it to LCS when you completed the steps in [Upload a configuration into Lifecycle Services](er-upload-configuration-into-lifecycle-services.md).</span></span> <span data-ttu-id="fe089-120">ในกระบวนงานนี้ คุณจะลบรุ่นนั้นของการตั้งค่าคอนฟิก ER</span><span class="sxs-lookup"><span data-stu-id="fe089-120">In this procedure, you will delete that version of the ER configuration.</span></span> <span data-ttu-id="fe089-121">จากนั้นคุณจะนำเข้ารุ่นดังกล่าวจาก LCS ภายหลังในหัวข้อนี้</span><span class="sxs-lookup"><span data-stu-id="fe089-121">You will then import that version from LCS later in this topic.</span></span>

2. <span data-ttu-id="fe089-122">ในรายการนี้ ให้ค้นหาและเลือกเรกคอร์ดที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="fe089-122">In the list, find and select the desired record.</span></span>

    <span data-ttu-id="fe089-123">สำหรับตัวอย่างนี้ เลือกรุ่นของการตั้งค่าคอนฟิกซึ่งมีสถานะเป็น **ใช้ร่วมกัน**</span><span class="sxs-lookup"><span data-stu-id="fe089-123">For this example, select the version of the configuration that has a status of **Shared**.</span></span> <span data-ttu-id="fe089-124">สถานะนี้ระบุว่าการตั้งค่าคอนฟิกได้ถูกเผยแพร่ไปยัง LCS แล้ว</span><span class="sxs-lookup"><span data-stu-id="fe089-124">This status indicates that the configuration has been published to LCS.</span></span>

3. <span data-ttu-id="fe089-125">เลือก **เปลี่ยนแปลงสถานะ**</span><span class="sxs-lookup"><span data-stu-id="fe089-125">Select **Change status**.</span></span>
4. <span data-ttu-id="fe089-126">เลือก **ยกเลิกการดำเนินการต่อ**</span><span class="sxs-lookup"><span data-stu-id="fe089-126">Select **Discontinue**.</span></span>

    <span data-ttu-id="fe089-127">ด้วยการเปลี่ยนสถานะของรุ่นที่เลือกจาก **ใช้ร่วมกัน** เป็น **ยกเลิกการดำเนินการต่อ** คุณจะทำให้พร้อมใช้งานสำหรับการลบ</span><span class="sxs-lookup"><span data-stu-id="fe089-127">By changing the status of the selected version from **Shared** to **Discontinued**, you make the version available for deletion.</span></span>

5. <span data-ttu-id="fe089-128">เลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="fe089-128">Select **OK**.</span></span>
6. <span data-ttu-id="fe089-129">ในรายการนี้ ให้ค้นหาและเลือกเรกคอร์ดที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="fe089-129">In the list, find and select the desired record.</span></span>

    <span data-ttu-id="fe089-130">สำหรับตัวอย่างนี้ เลือกรุ่นของการตั้งค่าคอนฟิกซึ่งมีสถานะเป็น **ยกเลิกการดำเนินการต่อ**</span><span class="sxs-lookup"><span data-stu-id="fe089-130">For this example, select the version of the configuration that has a status of **Discontinued**.</span></span>

7. <span data-ttu-id="fe089-131">เลือก **ลบ**</span><span class="sxs-lookup"><span data-stu-id="fe089-131">Select **Delete**.</span></span>
8. <span data-ttu-id="fe089-132">เลือก **ใช่**</span><span class="sxs-lookup"><span data-stu-id="fe089-132">Select **Yes**.</span></span>

    <span data-ttu-id="fe089-133">สังเกตว่า เฉพาะแบบร่างเวอร์ชัน 2 ของการตั้งค่าคอนฟิกรูปแบบข้อมูลพร้อมใช้งานแล้ว</span><span class="sxs-lookup"><span data-stu-id="fe089-133">Notice that the only draft version 2 of the selected data model configuration is now available.</span></span>

9. <span data-ttu-id="fe089-134">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="fe089-134">Close the page.</span></span>

## <a name="import-a-shared-version-of-a-data-model-configuration-from-lcs"></a><span data-ttu-id="fe089-135">นำเข้าเวอร์ชันที่ใช้ร่วมกันของการตั้งค่าคอนฟิกรูปแบบข้อมูลจาก LCS</span><span class="sxs-lookup"><span data-stu-id="fe089-135">Import a shared version of a data model configuration from LCS</span></span>

1. <span data-ttu-id="fe089-136">ไปที่ **การจัดการองค์กร \> พื้นที่ทำงาน \> การรายงานทางอิเล็กทรอนิกส์**</span><span class="sxs-lookup"><span data-stu-id="fe089-136">Go to **Organization administration \> Workspaces \> Electronic reporting**.</span></span>

2. <span data-ttu-id="fe089-137">ในส่วน **ผู้ให้บริการการตั้งค่าคอนฟิก** เลือกไทล์ **Litware, Inc.**</span><span class="sxs-lookup"><span data-stu-id="fe089-137">In the **Configuration providers** section, select the **Litware, Inc.** tile.</span></span>

3. <span data-ttu-id="fe089-138">บนไทล์ **Litware, Inc.** เลือก **ที่เก็บ**</span><span class="sxs-lookup"><span data-stu-id="fe089-138">On the **Litware, Inc.** tile, select **Repositories**.</span></span>

    <span data-ttu-id="fe089-139">ตอนนี้คุณสามารถเปิดรายการของที่เก็บสำหรับผู้ให้บริการการตั้งค่าคอนฟิก Litware, Inc.</span><span class="sxs-lookup"><span data-stu-id="fe089-139">You can now open the list of repositories for the Litware, Inc. configuration provider.</span></span>

4. <span data-ttu-id="fe089-140">เลือก **เปิด**</span><span class="sxs-lookup"><span data-stu-id="fe089-140">Select **Open**.</span></span>

    <span data-ttu-id="fe089-141">สำหรับตัวอย่างนี้ ให้เลือกเรกคอร์ดที่เก็บ **LCS** และเปิด</span><span class="sxs-lookup"><span data-stu-id="fe089-141">For this example, select the **LCS** repository, and open it.</span></span> <span data-ttu-id="fe089-142">คุณต้องมีสิทธิ์ [เข้าถึง](#accessconditions) โครงการ LCS และไปยังแอสเซทไลบรารีที่มีการเข้าถึงโดยที่เก็บ ER ที่เลือก</span><span class="sxs-lookup"><span data-stu-id="fe089-142">You must have [access](#accessconditions) to the LCS project and to the Asset library that is accessed by the selected ER repository.</span></span>

5. <span data-ttu-id="fe089-143">ในรายการนี้ ให้ทำเครื่องหมายแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="fe089-143">In the list, mark the selected row.</span></span>

    <span data-ttu-id="fe089-144">สำหรับตัวอย่างนี้ ให้เลือกรุ่นแรกของ **การตั้งค่าคอนฟิกรูปแบบตัวอย่าง** ในรายการรุ่น</span><span class="sxs-lookup"><span data-stu-id="fe089-144">For this example, select the first version of **Sample model configuration** in the version list.</span></span>

6. <span data-ttu-id="fe089-145">เลือก **นำเข้า**</span><span class="sxs-lookup"><span data-stu-id="fe089-145">Select **Import**.</span></span>
7. <span data-ttu-id="fe089-146">เลือก **ใช่** เพื่อยืนยันการนำเข้ารุ่นที่เลือกจาก LCS</span><span class="sxs-lookup"><span data-stu-id="fe089-146">Select **Yes** to confirm the import of the selected version from LCS.</span></span>

    <span data-ttu-id="fe089-147">ข้อความที่ให้ข้อมูลยืนยันว่ามีการนำเข้ารุ่นที่เลือกเสร็จเรียบร้อยแล้ว</span><span class="sxs-lookup"><span data-stu-id="fe089-147">An informational message confirms that the selected version was successfully imported.</span></span>

8. <span data-ttu-id="fe089-148">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="fe089-148">Close the page.</span></span>
9. <span data-ttu-id="fe089-149">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="fe089-149">Close the page.</span></span>
10. <span data-ttu-id="fe089-150">เลือก **การตั้งค่าคอนฟิก**</span><span class="sxs-lookup"><span data-stu-id="fe089-150">Select **Configurations**.</span></span>
11. <span data-ttu-id="fe089-151">ในแผนภูมิ เลือก **การตั้งค่าคอนฟิกรูปแบบตัวอย่าง**</span><span class="sxs-lookup"><span data-stu-id="fe089-151">In the tree, select **Sample model configuration**.</span></span>
12. <span data-ttu-id="fe089-152">ในรายการนี้ ให้ค้นหาและเลือกเรกคอร์ดที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="fe089-152">In the list, find and select the desired record.</span></span>

    <span data-ttu-id="fe089-153">สำหรับตัวอย่างนี้ เลือกรุ่นของการตั้งค่าคอนฟิกซึ่งมีสถานะเป็น **ใช้ร่วมกัน**</span><span class="sxs-lookup"><span data-stu-id="fe089-153">For this example, select the version of the configuration that has a status of **Shared**.</span></span>

    <span data-ttu-id="fe089-154">สังเกตว่า รุ่นที่ใช้ร่วมกัน 1 ของการตั้งค่าคอนฟิกรูปแบบข้อมูลที่เลือกพร้อมใช้งานแล้วในขณะนี้</span><span class="sxs-lookup"><span data-stu-id="fe089-154">Notice that shared version 1 of the selected data model configuration is also available now.</span></span>


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]