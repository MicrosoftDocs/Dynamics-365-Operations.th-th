---
title: ดาวน์โหลดการตั้งค่าคอนฟิก ER จากที่เก็บส่วนกลางของบริการตั้งค่าคอนฟิก
description: หัวข้อนี้จะอธิบายถึงวิธีการดาวน์โหลดการตั้งค่าคอนฟิกการรายงานทางอิเล็กทรอนิกส์ (ER) จากที่เก็บส่วนกลางของบริการตั้งค่าคอนฟิก
author: NickSelin
manager: AnnBe
ms.date: 06/02/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ERSolutionImport, ERWorkspace, ERSolutionRepositoryTable
audience: Application User, IT Pro
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 105843
ms.assetid: dc44dea2-22ce-401e-98b9-d289e0e2825b
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-05-31
ms.dyn365.ops.version: AX 10.0.5
ms.openlocfilehash: ed31cdee74c9db26ba76ed263b5e0578cd04bc3d
ms.sourcegitcommit: 7816902b59aa61d9183d54b50a86e282661e3971
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 06/02/2020
ms.locfileid: "3421713"
---
# <a name="download-er-configurations-from-the-global-repository-of-configuration-service"></a><span data-ttu-id="f28a8-103">ดาวน์โหลดการตั้งค่าคอนฟิก ER จากที่เก็บส่วนกลางของบริการตั้งค่าคอนฟิก</span><span class="sxs-lookup"><span data-stu-id="f28a8-103">Download ER configurations from the Global repository of Configuration service</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="f28a8-104">หัวข้อนี้จะอธิบายถึงวิธีการดาวน์โหลด [การตั้งค่าคอนฟิกการรายงานทางอิเล็กทรอนิกส์ (ER)](general-electronic-reporting.md#Configuration) จากที่เก็บส่วนกลางของบริการตั้งค่าคอนฟิก</span><span class="sxs-lookup"><span data-stu-id="f28a8-104">This topic explains how to download [Electronic reporting (ER) configurations](general-electronic-reporting.md#Configuration) from the Global repository of configuration service.</span></span> <span data-ttu-id="f28a8-105">สำหรับข้อมูลเพิ่มเติม ให้ดูที่ [Microsoft Dynamics 365 for Finance and Operations - Regulatory Services, Configuration service](https://docs.microsoft.com/business-applications-release-notes/october18/dynamics365-finance-operations/regulatory-service-configuration)</span><span class="sxs-lookup"><span data-stu-id="f28a8-105">For more information, see [Microsoft Dynamics 365 for Finance and Operations - Regulatory Services, Configuration service](https://docs.microsoft.com/business-applications-release-notes/october18/dynamics365-finance-operations/regulatory-service-configuration).</span></span>

## <a name="open-configurations-repository"></a><span data-ttu-id="f28a8-106">เปิดที่เก็บการตั้งค่าคอนฟิก</span><span class="sxs-lookup"><span data-stu-id="f28a8-106">Open configurations repository</span></span>

1. <span data-ttu-id="f28a8-107">ลงชื่อเข้าใช้ในแอปพลิเคชัน Dynamics 365 Finance โดยใช้หนึ่งในบทบาทต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="f28a8-107">Sign in to the Dynamics 365 Finance application using one of the following roles:</span></span>

    - <span data-ttu-id="f28a8-108">นักพัฒนาการรายงานทางอิเล็กทรอนิกส์</span><span class="sxs-lookup"><span data-stu-id="f28a8-108">Electronic reporting developer</span></span>
    - <span data-ttu-id="f28a8-109">ที่ปรึกษาด้านการทำงานของการรายงานทางอิเล็กทรอนิกส์</span><span class="sxs-lookup"><span data-stu-id="f28a8-109">Electronic reporting functional consultant</span></span>
    - <span data-ttu-id="f28a8-110">ผู้ดูแลระบบ</span><span class="sxs-lookup"><span data-stu-id="f28a8-110">System administrator</span></span>

2. <span data-ttu-id="f28a8-111">ไปที่ **การจัดการองค์กร > พื้นที่ทำงาน > การรายงานทางอิเล็กทรอนิกส์**</span><span class="sxs-lookup"><span data-stu-id="f28a8-111">Go to **Organization administration > Workspaces > Electronic reporting**.</span></span>
3. <span data-ttu-id="f28a8-112">ในส่วน **ผู้ให้บริการการตั้งค่าคอนฟิก** เลือกไทล์ **Microsoft**</span><span class="sxs-lookup"><span data-stu-id="f28a8-112">In the **Configuration providers** section, select the **Microsoft** tile.</span></span>
3. <span data-ttu-id="f28a8-113">บนไทล์ **Microsoft** เลือก **ที่เก็บ**</span><span class="sxs-lookup"><span data-stu-id="f28a8-113">On the **Microsoft** tile, select **Repositories**.</span></span>

    ![พื้นที่ทำงานการรายงานทางอิเล็กทรอนิกส์](./media/er-download-configurations-global-repo-er-workspace.png)

4. <span data-ttu-id="f28a8-115">บนหน้า **ที่เก็บการตั้งค่าคอนฟิก** ในกริด เลือกที่เก็บที่มีอยู่ของชนิด **ส่วนกลาง**</span><span class="sxs-lookup"><span data-stu-id="f28a8-115">On the **Configuration repositories** page, in the grid, select the existing repository of the **Global** type.</span></span> <span data-ttu-id="f28a8-116">ถ้าที่เก็บนี้ไม่ปรากฏในกริด ให้ทำตามขั้นตอนเหล่านี้:</span><span class="sxs-lookup"><span data-stu-id="f28a8-116">If this repository doesn't appear in the grid, follow these steps:</span></span>

    1. <span data-ttu-id="f28a8-117">เลือก **เพิ่ม** เพื่อเพิ่มที่เก็บใหม่</span><span class="sxs-lookup"><span data-stu-id="f28a8-117">Select **Add** to add a new repository.</span></span>
    2. <span data-ttu-id="f28a8-118">เลือก **ส่วนกลาง** เป็นชนิดที่เก็บ แล้วจากนั้น เลือก **สร้างที่เก็บ**</span><span class="sxs-lookup"><span data-stu-id="f28a8-118">Select **Global** as the repository type, and then select **Create repository**.</span></span>
    3. <span data-ttu-id="f28a8-119">หากได้รับการแจ้ง ให้ทำตามคำแนะนำการตรวจสอบ</span><span class="sxs-lookup"><span data-stu-id="f28a8-119">If prompted, follow the authorization instructions.</span></span>
    4. <span data-ttu-id="f28a8-120">ป้อนชื่อและคำอธิบายสำหรับที่เก็บ แล้วจากนั้น เลือก **ตกลง** เพื่อยืนยันรายการที่เก็บใหม่</span><span class="sxs-lookup"><span data-stu-id="f28a8-120">Enter a name and description for the repository and then select **OK** to confirm the new repository entry.</span></span>
    5. <span data-ttu-id="f28a8-121">ในกริด เลือกที่เก็บใหม่ของชนิด **ส่วนกลาง**</span><span class="sxs-lookup"><span data-stu-id="f28a8-121">In the grid, select the new repository of the **Global** type.</span></span>

5. <span data-ttu-id="f28a8-122">เลือก **เปิด** เพื่อดูรายการของการตั้งค่าคอนฟิก ER สำหรับที่เก็บที่เลือก</span><span class="sxs-lookup"><span data-stu-id="f28a8-122">Select **Open** to view the list of ER configurations for the selected repository.</span></span>

    ![หน้าที่เก็บการตั้งค่าคอนฟิก](./media/er-download-configurations-global-repo-repositories-list.png)

## <a name="import-a-single-configuration"></a><span data-ttu-id="f28a8-124">นำเข้าการตั้งค่าคอนฟิกเดียว</span><span class="sxs-lookup"><span data-stu-id="f28a8-124">Import a single configuration</span></span>

1. <span data-ttu-id="f28a8-125">บนหน้า **ที่เก็บการตั้งค่าคอนฟิก** ในแผนภูมิการตั้งค่าคอนฟิก ให้เลือกการตั้งค่าคอนฟิก ER ที่คุณต้องการ</span><span class="sxs-lookup"><span data-stu-id="f28a8-125">On the **Configuration repositories** page, in the configurations tree, select the ER configuration that you want.</span></span>
2. <span data-ttu-id="f28a8-126">บน FastTab **เวอร์ชัน** เลือกเวอร์ชันที่กำหนดของการตั้งค่าคอนฟิก ER ที่เลือก</span><span class="sxs-lookup"><span data-stu-id="f28a8-126">On the **Versions** FastTab, select the required version of the selected ER configuration.</span></span>
3. <span data-ttu-id="f28a8-127">เลือก **นำเข้า** เพื่อดาวน์โหลดเวอร์ชันที่เลือกจากที่เก็บส่วนกลางไปยังอินสแตนซ์ Finance ปัจจุบัน</span><span class="sxs-lookup"><span data-stu-id="f28a8-127">Select **Import** to download the selected version from Global repository to the current Finance instance.</span></span>

    > [!NOTE]
    > <span data-ttu-id="f28a8-128">ปุ่ม **นำเข้า** ใช้งานไม่ได้กับเวอร์ชันการตั้งค่าคอนฟิก ER ที่อยู่ในอินสแตนซ์ Finance ปัจจุบันอยู่แล้ว</span><span class="sxs-lookup"><span data-stu-id="f28a8-128">The **Import** button is unavailable for ER configuration versions that are already present in the current Finance instance.</span></span>

    ![หน้าที่เก็บการตั้งค่าคอนฟิก](./media/er-download-configurations-global-repo-repository-content.png)

## <a name="import-filtered-configurations"></a><span data-ttu-id="f28a8-130">นำเข้าการตั้งค่าคอนฟิกที่มีการกรองข้อมูล</span><span class="sxs-lookup"><span data-stu-id="f28a8-130">Import filtered configurations</span></span>

1. <span data-ttu-id="f28a8-131">บนหน้า **ที่เก็บการตั้งค่าคอนฟิก** ในแผนภูมิการตั้งค่าคอนฟิก ขยาย FastTab **ตัวกรอง**</span><span class="sxs-lookup"><span data-stu-id="f28a8-131">On the **Configuration repositories** page, in the configurations tree, expand the **Filter** FastTab.</span></span>
2. <span data-ttu-id="f28a8-132">ในกริด **แท็ก** ให้เพิ่มแท็กใดๆ ที่จำเป็น</span><span class="sxs-lookup"><span data-stu-id="f28a8-132">In the **Tags** grid, add any tags that are needed.</span></span>
3. <span data-ttu-id="f28a8-133">ในฟิลด์ **ความเกี่ยวข้องของประเทศ/ภูมิภาค** เลือกรหัสประเทศ/ภูมิภาคที่เหมาะสม แล้วจากนั้น เลือก **ใช้ตัวกรอง**</span><span class="sxs-lookup"><span data-stu-id="f28a8-133">In the **Country/region applicability** field, select the appropriate country/region codes, and then select  **Apply filter**.</span></span>

    > [!NOTE]
    > <span data-ttu-id="f28a8-134">FastTab **การตั้งค่าคอนฟิก** จะแสดงการตั้งค่าคอนฟิกทั้งหมดที่เป็นไปตามเงื่อนไขการเลือกที่ระบุ</span><span class="sxs-lookup"><span data-stu-id="f28a8-134">The **Configurations** FastTab shows all the configurations that satisfy the specified selection conditions.</span></span>

4. <span data-ttu-id="f28a8-135">บน FastTab **การตั้งค่าคอนฟิก** ให้เลือก **นำเข้า** เพื่อดึงข้อมูลการตั้งค่าคอนฟิกที่ถูกกรองจากที่เก็บส่วนกลางไปยังอินสแตนซ์ปัจจุบัน</span><span class="sxs-lookup"><span data-stu-id="f28a8-135">On the **Configurations** FastTab, select **Import** to download the filtered configurations from the Global repository to the current instance.</span></span>
5. <span data-ttu-id="f28a8-136">บน FastTab **การตั้งค่าคอนฟิก** ให้เลือก **รีเซ็ตตัวกรอง** เพื่อล้างเงื่อนไขการเลือกที่ระบุ</span><span class="sxs-lookup"><span data-stu-id="f28a8-136">On the **Configurations** FastTab, select **Reset filter** to clean up the specified selection conditions.</span></span>

    ![หน้าที่เก็บการตั้งค่าคอนฟิก](./media/er-download-configurations-global-repo-filtered-configurations.png)

> [!NOTE]
> <span data-ttu-id="f28a8-138">โดยขึ้นอยู่กับการตั้งค่า ER การตั้งค่าคอนฟิกจะได้รับการตรวจสอบความถูกต้องหลังจากที่มีการนำเข้าแล้ว</span><span class="sxs-lookup"><span data-stu-id="f28a8-138">Depending on the ER settings, configurations are validated after they are imported.</span></span> <span data-ttu-id="f28a8-139">คุณอาจได้รับแจ้งเกี่ยวกับปัญหาความไม่สอดคล้องใด ๆ ที่พบ</span><span class="sxs-lookup"><span data-stu-id="f28a8-139">You might be notified about any inconsistency issues that are discovered.</span></span> <span data-ttu-id="f28a8-140">ก่อนที่คุณจะสามารถใช้เวอร์ชันการตั้งค่าคอนฟิกที่นำเข้าได้ คุณจะต้องแก้ไขปัญหา</span><span class="sxs-lookup"><span data-stu-id="f28a8-140">Before you can use the imported configuration version, you must resolve the issues.</span></span> <span data-ttu-id="f28a8-141">สำหรับข้อมูลเพิ่มเติม ดูรายการของทรัพยากรที่เกี่ยวข้องสำหรับหัวข้อนี้</span><span class="sxs-lookup"><span data-stu-id="f28a8-141">For more information, see the list of related resources for this topic.</span></span>

> [!NOTE]
> <span data-ttu-id="f28a8-142">คุณสามารถตั้งค่าคอนฟิก ER โดยขึ้นอยู่กับการตั้งค่าคอนฟิกอื่นๆ</span><span class="sxs-lookup"><span data-stu-id="f28a8-142">ER configurations can be configured as being dependent on other configurations.</span></span> <span data-ttu-id="f28a8-143">ดังนั้น พร้อมด้วยการตั้งค่าคอนฟิกที่เลือก การตั้งค่าคอนฟิกอื่นๆ อาจได้รับการนำเข้าไปโดยอัตโนมัติ</span><span class="sxs-lookup"><span data-stu-id="f28a8-143">Therefore, along with a selected configuration, other configurations might be automatically imported.</span></span> <span data-ttu-id="f28a8-144">สำหรับข้อมูลเพิ่มเติมเกี่ยวกับการขึ้นต่อกันของการตั้งค่าคอนฟิก ให้ดูที่ [กำหนดการขึ้นต่อกันของการตั้งค่าคอนฟิก ER ในส่วนประกอบอื่นๆ](tasks/er-define-dependency-er-configurations-from-other-components-july-2017.md)</span><span class="sxs-lookup"><span data-stu-id="f28a8-144">For more about configuration dependencies, see [Define the dependency of ER configurations on other components](tasks/er-define-dependency-er-configurations-from-other-components-july-2017.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="f28a8-145">ทรัพยากรเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="f28a8-145">Additional resources</span></span>

[<span data-ttu-id="f28a8-146">ภาพรวมการรายงานทางอิเล็กทรอนิกส์ (ER)</span><span class="sxs-lookup"><span data-stu-id="f28a8-146">Electronic reporting (ER) overview</span></span>](general-electronic-reporting.md)
