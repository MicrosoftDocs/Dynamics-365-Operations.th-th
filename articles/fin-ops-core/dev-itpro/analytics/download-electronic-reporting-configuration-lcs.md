---
title: ดาวน์โหลดการตั้งค่าคอนฟิกการรายงานแบบอิเล็กทรอนิกส์จาก Lifecycle Services
description: หัวข้อนี้อธิบายวิธีการดาวน์โหลดการตั้งค่าคอนฟิกการรายงานทางอิเล็กทรอนิกส์ (ER) จาก Microsoft Dynamics Lifecycle Services (LCS)
author: NickSelin
manager: AnnBe
ms.date: 08/27/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ERSolutionImport, ERWorkspace
audience: Application User, IT Pro
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 105843
ms.assetid: dc44dea2-22ce-401e-98b9-d289e0e2825b
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-05-31
ms.dyn365.ops.version: AX 7.0.1
ms.openlocfilehash: 8a18427114bddb7c72024a8d96d33f3fbf8dbe17
ms.sourcegitcommit: 9857d5cbdc0ab2fc9db049ac5ad118fc2b29bedc
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 09/14/2020
ms.locfileid: "3810630"
---
# <a name="download-electronic-reporting-configurations-from-lifecycle-services"></a><span data-ttu-id="e9cdd-103">ดาวน์โหลดการตั้งค่าคอนฟิกการรายงานแบบอิเล็กทรอนิกส์จาก Lifecycle Services</span><span class="sxs-lookup"><span data-stu-id="e9cdd-103">Download Electronic reporting configurations from Lifecycle Services</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="e9cdd-104">หัวข้อนี้จะอธิบายวิธีการดาวน์โหลด [การตั้งค่าคอนฟิกการรายงานทางอิเล็กทรอนิกส์ (ER)](general-electronic-reporting.md#Configuration) รุ่นใหม่ล่าสุดจาก [ไลบรารีแอสเซทที่ใช้ร่วมกัน](../lifecycle-services/asset-library.md) ใน Microsoft Dynamics Lifecycle Services (LCS)</span><span class="sxs-lookup"><span data-stu-id="e9cdd-104">This topic explains how to download the newest version of [Electronic reporting (ER) configurations](general-electronic-reporting.md#Configuration) from the [Shared asset library](../lifecycle-services/asset-library.md) in Microsoft Dynamics Lifecycle Services (LCS).</span></span>

1. <span data-ttu-id="e9cdd-105">ลงชื่อเข้าใช้ในแอพลิเคชันโดยใช้หนึ่งในบทบาทต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="e9cdd-105">Sign in to the application by using one of the following roles:</span></span>

    - <span data-ttu-id="e9cdd-106">นักพัฒนาการรายงานทางอิเล็กทรอนิกส์</span><span class="sxs-lookup"><span data-stu-id="e9cdd-106">Electronic reporting developer</span></span>
    - <span data-ttu-id="e9cdd-107">ที่ปรึกษาด้านการทำงานของการรายงานทางอิเล็กทรอนิกส์</span><span class="sxs-lookup"><span data-stu-id="e9cdd-107">Electronic reporting functional consultant</span></span>
    - <span data-ttu-id="e9cdd-108">ผู้ดูแลระบบ</span><span class="sxs-lookup"><span data-stu-id="e9cdd-108">System administrator</span></span>

2. <span data-ttu-id="e9cdd-109">ไปที่ **การจัดการองค์กร** &gt; **พื้นที่ทำงาน** &gt; **การรายงานทางอิเล็กทรอนิกส์**</span><span class="sxs-lookup"><span data-stu-id="e9cdd-109">Go to **Organization administration** &gt; **Workspaces** &gt; **Electronic reporting**.</span></span>
3. <span data-ttu-id="e9cdd-110">ในส่วน **ผู้ให้บริการการตั้งค่าคอนฟิก** เลือกไทล์ **Microsoft**</span><span class="sxs-lookup"><span data-stu-id="e9cdd-110">In the **Configuration providers** section, select the **Microsoft** tile.</span></span>
4. <span data-ttu-id="e9cdd-111">บนไทล์ **Microsoft** เลือก **ที่เก็บ**</span><span class="sxs-lookup"><span data-stu-id="e9cdd-111">On the **Microsoft** tile, select **Repositories**.</span></span>

    <span data-ttu-id="e9cdd-112">[![ไทล์ Microsoft บนหน้าการตั้งค่าคอนฟิกการแปลเป็นภาษาท้องถิ่น](./media/update-er-from-lcs-for-ms-open-ms-repositories-list.png)](./media/update-er-from-lcs-for-ms-open-ms-repositories-list.png)</span><span class="sxs-lookup"><span data-stu-id="e9cdd-112">[![Microsoft tile on the Localization configurations page](./media/update-er-from-lcs-for-ms-open-ms-repositories-list.png)](./media/update-er-from-lcs-for-ms-open-ms-repositories-list.png)</span></span>

5. <span data-ttu-id="e9cdd-113">บนหน้า **ที่เก็บการตั้งค่าคอนฟิก** ในกริด เลือกที่เก็บที่มีอยู่ของชนิด **LCS**</span><span class="sxs-lookup"><span data-stu-id="e9cdd-113">On the **Configuration repositories** page, in the grid, select the existing repository of the **LCS** type.</span></span> <span data-ttu-id="e9cdd-114">ถ้าที่เก็บนี้ไม่ปรากฏในกริด ให้ทำตามขั้นตอนเหล่านี้:</span><span class="sxs-lookup"><span data-stu-id="e9cdd-114">If this repository doesn't appear in the grid, follow these steps:</span></span>

    1. <span data-ttu-id="e9cdd-115">เลือก **เพิ่ม** เพื่อเพิ่มที่เก็บ</span><span class="sxs-lookup"><span data-stu-id="e9cdd-115">Select **Add** to add a repository.</span></span>
    2. <span data-ttu-id="e9cdd-116">เลือก **LCS** เป็นชนิดที่เก็บ</span><span class="sxs-lookup"><span data-stu-id="e9cdd-116">Select **LCS** as the repository type.</span></span>
    3. <span data-ttu-id="e9cdd-117">เลือก **สร้างที่เก็บ**</span><span class="sxs-lookup"><span data-stu-id="e9cdd-117">Select **Create repository**.</span></span>
    4. <span data-ttu-id="e9cdd-118">ถ้าคุณได้รับข้อความแจ้งเกี่ยวกับการอนุมัติ ให้ทำตามคำแนะนำบนหน้าจอ</span><span class="sxs-lookup"><span data-stu-id="e9cdd-118">If you're prompted about authorization, follow the on-screen instructions.</span></span>
    5. <span data-ttu-id="e9cdd-119">ป้อนชื่อและคำอธิบายสำหรับที่เก็บ</span><span class="sxs-lookup"><span data-stu-id="e9cdd-119">Enter a name and description for the repository.</span></span>
    6. <span data-ttu-id="e9cdd-120">เลือก **ตกลง** เพื่อยืนยันรายการที่เก็บใหม่</span><span class="sxs-lookup"><span data-stu-id="e9cdd-120">Select **OK** to confirm the new repository entry.</span></span>
    7. <span data-ttu-id="e9cdd-121">ในกริด เลือกที่เก็บใหม่ของชนิด **LCS**</span><span class="sxs-lookup"><span data-stu-id="e9cdd-121">In the grid, select the new repository of the **LCS** type.</span></span>

6. <span data-ttu-id="e9cdd-122">เลือก **เปิด** เพื่อดูรายการของการตั้งค่าคอนฟิก ER สำหรับที่เก็บที่เลือก</span><span class="sxs-lookup"><span data-stu-id="e9cdd-122">Select **Open** to view the list of ER configurations for the selected repository.</span></span>

    <span data-ttu-id="e9cdd-123">[![หน้าที่เก็บการตั้งค่าคอนฟิก](./media/update-er-from-lcs-for-ms-make-lcs-repository.png)](./media/update-er-from-lcs-for-ms-make-lcs-repository.png)</span><span class="sxs-lookup"><span data-stu-id="e9cdd-123">[![Configuration repositories page](./media/update-er-from-lcs-for-ms-make-lcs-repository.png)](./media/update-er-from-lcs-for-ms-make-lcs-repository.png)</span></span>

    > [!TIP]
    > <span data-ttu-id="e9cdd-124">ถ้าคุณมีปัญหาในการเข้าถึงที่เก็บ LCS เพื่อดาวน์โหลดการตั้งค่าคอนฟิกจากไลบรารีแอสเซทที่ใช้ร่วมกันใน LCS คุณสามารถดาวน์โหลดการตั้งค่าคอนฟิกจาก [ที่เก็บส่วนกลาง](er-download-configurations-global-repo.md) แทน</span><span class="sxs-lookup"><span data-stu-id="e9cdd-124">If you have trouble accessing the LCS repository to download configurations from the Shared asset library in LCS, you can download configurations from the [Global repository](er-download-configurations-global-repo.md) instead.</span></span>

7. <span data-ttu-id="e9cdd-125">ในแผนภูมิการตั้งค่าคอนฟิกในบานหน้าต่างด้านซ้าย ให้เลือกการตั้งค่าคอนฟิก ER ที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="e9cdd-125">In the configurations tree in the left pane, select the required ER configuration.</span></span>
8. <span data-ttu-id="e9cdd-126">บน FastTab **เวอร์ชัน** เลือกเวอร์ชันที่กำหนดของการตั้งค่าคอนฟิก ER ที่เลือก</span><span class="sxs-lookup"><span data-stu-id="e9cdd-126">On the **Versions** FastTab, select the required version of the selected ER configuration.</span></span>
9. <span data-ttu-id="e9cdd-127">เลือก **นำเข้า** เพื่อดาวน์โหลดเวอร์ชันที่เลือกจาก LCS ไปยังอินสแตนซ์ปัจจุบัน</span><span class="sxs-lookup"><span data-stu-id="e9cdd-127">Select **Import** to download the selected version from LCS to the current instance.</span></span>

    > [!NOTE]
    > <span data-ttu-id="e9cdd-128">ปุ่ม **นำเข้า** ใช้งานไม่ได้กับเวอร์ชันการตั้งค่าคอนฟิก ER ที่อยู่ในอินสแตนซ์ปัจจุบันอยู่แล้ว</span><span class="sxs-lookup"><span data-stu-id="e9cdd-128">The **Import** button is unavailable for ER configuration versions that are already present in the current instance.</span></span>

    <span data-ttu-id="e9cdd-129">[![หน้าที่เก็บการตั้งค่าคอนฟิก](./media/update-er-from-lcs-for-ms-download-configuration.png)](./media/update-er-from-lcs-for-ms-download-configuration.png)</span><span class="sxs-lookup"><span data-stu-id="e9cdd-129">[![Configuration repository page](./media/update-er-from-lcs-for-ms-download-configuration.png)](./media/update-er-from-lcs-for-ms-download-configuration.png)</span></span>

> [!NOTE]
> <span data-ttu-id="e9cdd-130">โดยขึ้นอยู่กับการตั้งค่า ER การตั้งค่าคอนฟิกจะได้รับการตรวจสอบความถูกต้องหลังจากที่มีการนำเข้าแล้ว</span><span class="sxs-lookup"><span data-stu-id="e9cdd-130">Depending on the ER settings, configurations are validated after they are imported.</span></span> <span data-ttu-id="e9cdd-131">คุณอาจได้รับแจ้งเกี่ยวกับปัญหาความไม่สอดคล้องใด ๆ ที่พบ</span><span class="sxs-lookup"><span data-stu-id="e9cdd-131">You might be notified about any inconsistency issues that are discovered.</span></span> <span data-ttu-id="e9cdd-132">คุณจะต้องแก้ไขปัญหาเหล่านั้นก่อนที่คุณจะสามารถใช้เวอร์ชันการตั้งค่าคอนฟิกที่นำเข้าได้</span><span class="sxs-lookup"><span data-stu-id="e9cdd-132">You must resolve those issues before you can use the imported configuration version.</span></span> <span data-ttu-id="e9cdd-133">สำหรับข้อมูลเพิ่มเติม ดูรายการของหัวข้อที่เกี่ยวข้องของหัวข้อนี้</span><span class="sxs-lookup"><span data-stu-id="e9cdd-133">For more information, see the list of related topics for this topic.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="e9cdd-134">ทรัพยากรเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="e9cdd-134">Additional resources</span></span>

[<span data-ttu-id="e9cdd-135">ภาพรวมการรายงานทางอิเล็กทรอนิกส์ (ER)</span><span class="sxs-lookup"><span data-stu-id="e9cdd-135">Electronic reporting (ER) overview</span></span>](general-electronic-reporting.md)

[<span data-ttu-id="e9cdd-136">ดาวน์โหลดการตั้งค่าคอนฟิก ER จากที่เก็บส่วนกลางของบริการตั้งค่าคอนฟิก</span><span class="sxs-lookup"><span data-stu-id="e9cdd-136">Download ER configurations from the Global repository of Configuration service</span></span>](er-download-configurations-global-repo.md)
