---
title: ดาวน์โหลดการตั้งค่าคอนฟิกการรายงานแบบอิเล็กทรอนิกส์จาก Lifecycle Services
description: หัวข้อนี้อธิบายวิธีการดาวน์โหลดการตั้งค่าคอนฟิกการรายงานทางอิเล็กทรอนิกส์ (ER) จาก Microsoft Dynamics Lifecycle Services (LCS)
author: NickSelin
ms.date: 08/27/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ERSolutionImport, ERWorkspace
audience: Application User, IT Pro
ms.reviewer: kfend
ms.custom: 105843
ms.assetid: dc44dea2-22ce-401e-98b9-d289e0e2825b
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-05-31
ms.dyn365.ops.version: AX 7.0.1
ms.openlocfilehash: 14f0f2b1a4d63101d432b1361379c61a70ac9345
ms.sourcegitcommit: dc4898aa32f381620c517bf89c7856e693563ace
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 06/17/2021
ms.locfileid: "6271194"
---
# <a name="download-electronic-reporting-configurations-from-lifecycle-services"></a><span data-ttu-id="4acea-103">ดาวน์โหลดการตั้งค่าคอนฟิกการรายงานแบบอิเล็กทรอนิกส์จาก Lifecycle Services</span><span class="sxs-lookup"><span data-stu-id="4acea-103">Download Electronic reporting configurations from Lifecycle Services</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="4acea-104">หัวข้อนี้จะอธิบายวิธีการดาวน์โหลด [การตั้งค่าคอนฟิกการรายงานทางอิเล็กทรอนิกส์ (ER)](general-electronic-reporting.md#Configuration) รุ่นใหม่ล่าสุดจาก [ไลบรารีแอสเซทที่ใช้ร่วมกัน](../lifecycle-services/asset-library.md) ใน Microsoft Dynamics Lifecycle Services (LCS)</span><span class="sxs-lookup"><span data-stu-id="4acea-104">This topic explains how to download the newest version of [Electronic reporting (ER) configurations](general-electronic-reporting.md#Configuration) from the [Shared asset library](../lifecycle-services/asset-library.md) in Microsoft Dynamics Lifecycle Services (LCS).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="4acea-105">การใช้ LCS เป็นที่เก็บหน่วยจัดเก็บเพื่อการตั้งค่าคอนฟิก ER [ไม่ได้รับการสนับสนุน](../../../finance/get-started/removed-deprecated-features-finance.md#features-removed-or-deprecated-in-the-finance-10017-release)</span><span class="sxs-lookup"><span data-stu-id="4acea-105">The use of LCS as a storage repository for ER configurations is being [deprecated](../../../finance/get-started/removed-deprecated-features-finance.md#features-removed-or-deprecated-in-the-finance-10017-release).</span></span> <span data-ttu-id="4acea-106">สำหรับข้อมูลเพิ่มเติม ให้ดู [Regulatory Configuration Service (RCS) – การเลิกใช้ที่เก็บข้อมูล Lifecycle Services (LCS)](../../../finance/localizations/rcs-lcs-repo-dep-faq.md)</span><span class="sxs-lookup"><span data-stu-id="4acea-106">For more information, see [Regulatory Configuration Service (RCS) – Lifecycle Services (LCS) storage deprecation](../../../finance/localizations/rcs-lcs-repo-dep-faq.md).</span></span>

1. <span data-ttu-id="4acea-107">ลงชื่อเข้าใช้ในแอพลิเคชันโดยใช้หนึ่งในบทบาทต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="4acea-107">Sign in to the application by using one of the following roles:</span></span>

    - <span data-ttu-id="4acea-108">นักพัฒนาการรายงานทางอิเล็กทรอนิกส์</span><span class="sxs-lookup"><span data-stu-id="4acea-108">Electronic reporting developer</span></span>
    - <span data-ttu-id="4acea-109">ที่ปรึกษาด้านการทำงานของการรายงานทางอิเล็กทรอนิกส์</span><span class="sxs-lookup"><span data-stu-id="4acea-109">Electronic reporting functional consultant</span></span>
    - <span data-ttu-id="4acea-110">ผู้ดูแลระบบ</span><span class="sxs-lookup"><span data-stu-id="4acea-110">System administrator</span></span>

2. <span data-ttu-id="4acea-111">ไปที่ **การจัดการองค์กร** &gt; **พื้นที่ทำงาน** &gt; **การรายงานทางอิเล็กทรอนิกส์**</span><span class="sxs-lookup"><span data-stu-id="4acea-111">Go to **Organization administration** &gt; **Workspaces** &gt; **Electronic reporting**.</span></span>
3. <span data-ttu-id="4acea-112">ในส่วน **ผู้ให้บริการการตั้งค่าคอนฟิก** เลือกไทล์ **Microsoft**</span><span class="sxs-lookup"><span data-stu-id="4acea-112">In the **Configuration providers** section, select the **Microsoft** tile.</span></span>
4. <span data-ttu-id="4acea-113">บนไทล์ **Microsoft** เลือก **ที่เก็บ**</span><span class="sxs-lookup"><span data-stu-id="4acea-113">On the **Microsoft** tile, select **Repositories**.</span></span>

    <span data-ttu-id="4acea-114">[![ไทล์ Microsoft บนหน้าการตั้งค่าคอนฟิกการแปลเป็นภาษาท้องถิ่น](./media/update-er-from-lcs-for-ms-open-ms-repositories-list.png)](./media/update-er-from-lcs-for-ms-open-ms-repositories-list.png)</span><span class="sxs-lookup"><span data-stu-id="4acea-114">[![Microsoft tile on the Localization configurations page](./media/update-er-from-lcs-for-ms-open-ms-repositories-list.png)](./media/update-er-from-lcs-for-ms-open-ms-repositories-list.png)</span></span>

5. <span data-ttu-id="4acea-115">บนหน้า **ที่เก็บการตั้งค่าคอนฟิก** ในกริด เลือกที่เก็บที่มีอยู่ของชนิด **LCS**</span><span class="sxs-lookup"><span data-stu-id="4acea-115">On the **Configuration repositories** page, in the grid, select the existing repository of the **LCS** type.</span></span> <span data-ttu-id="4acea-116">ถ้าที่เก็บนี้ไม่ปรากฏในกริด ให้ทำตามขั้นตอนเหล่านี้:</span><span class="sxs-lookup"><span data-stu-id="4acea-116">If this repository doesn't appear in the grid, follow these steps:</span></span>

    1. <span data-ttu-id="4acea-117">เลือก **เพิ่ม** เพื่อเพิ่มที่เก็บ</span><span class="sxs-lookup"><span data-stu-id="4acea-117">Select **Add** to add a repository.</span></span>
    2. <span data-ttu-id="4acea-118">เลือก **LCS** เป็นชนิดที่เก็บ</span><span class="sxs-lookup"><span data-stu-id="4acea-118">Select **LCS** as the repository type.</span></span>
    3. <span data-ttu-id="4acea-119">เลือก **สร้างที่เก็บ**</span><span class="sxs-lookup"><span data-stu-id="4acea-119">Select **Create repository**.</span></span>
    4. <span data-ttu-id="4acea-120">ถ้าคุณได้รับข้อความแจ้งเกี่ยวกับการอนุมัติ ให้ทำตามคำแนะนำบนหน้าจอ</span><span class="sxs-lookup"><span data-stu-id="4acea-120">If you're prompted about authorization, follow the on-screen instructions.</span></span>
    5. <span data-ttu-id="4acea-121">ป้อนชื่อและคำอธิบายสำหรับที่เก็บ</span><span class="sxs-lookup"><span data-stu-id="4acea-121">Enter a name and description for the repository.</span></span>
    6. <span data-ttu-id="4acea-122">เลือก **ตกลง** เพื่อยืนยันรายการที่เก็บใหม่</span><span class="sxs-lookup"><span data-stu-id="4acea-122">Select **OK** to confirm the new repository entry.</span></span>
    7. <span data-ttu-id="4acea-123">ในกริด เลือกที่เก็บใหม่ของชนิด **LCS**</span><span class="sxs-lookup"><span data-stu-id="4acea-123">In the grid, select the new repository of the **LCS** type.</span></span>

6. <span data-ttu-id="4acea-124">เลือก **เปิด** เพื่อดูรายการของการตั้งค่าคอนฟิก ER สำหรับที่เก็บที่เลือก</span><span class="sxs-lookup"><span data-stu-id="4acea-124">Select **Open** to view the list of ER configurations for the selected repository.</span></span>

    <span data-ttu-id="4acea-125">[![หน้าที่เก็บการตั้งค่าคอนฟิก](./media/update-er-from-lcs-for-ms-make-lcs-repository.png)](./media/update-er-from-lcs-for-ms-make-lcs-repository.png)</span><span class="sxs-lookup"><span data-stu-id="4acea-125">[![Configuration repositories page](./media/update-er-from-lcs-for-ms-make-lcs-repository.png)](./media/update-er-from-lcs-for-ms-make-lcs-repository.png)</span></span>

    > [!TIP]
    > <span data-ttu-id="4acea-126">ถ้าคุณมีปัญหาในการเข้าถึงที่เก็บ LCS เพื่อดาวน์โหลดการตั้งค่าคอนฟิกจากไลบรารีแอสเซทที่ใช้ร่วมกันใน LCS คุณสามารถดาวน์โหลดการตั้งค่าคอนฟิกจาก [ที่เก็บส่วนกลาง](er-download-configurations-global-repo.md) แทน</span><span class="sxs-lookup"><span data-stu-id="4acea-126">If you have trouble accessing the LCS repository to download configurations from the Shared asset library in LCS, you can download configurations from the [Global repository](er-download-configurations-global-repo.md) instead.</span></span>

7. <span data-ttu-id="4acea-127">ในแผนภูมิการตั้งค่าคอนฟิกในบานหน้าต่างด้านซ้าย ให้เลือกการตั้งค่าคอนฟิก ER ที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="4acea-127">In the configurations tree in the left pane, select the required ER configuration.</span></span>
8. <span data-ttu-id="4acea-128">บน FastTab **เวอร์ชัน** เลือกเวอร์ชันที่กำหนดของการตั้งค่าคอนฟิก ER ที่เลือก</span><span class="sxs-lookup"><span data-stu-id="4acea-128">On the **Versions** FastTab, select the required version of the selected ER configuration.</span></span>
9. <span data-ttu-id="4acea-129">เลือก **นำเข้า** เพื่อดาวน์โหลดเวอร์ชันที่เลือกจาก LCS ไปยังอินสแตนซ์ปัจจุบัน</span><span class="sxs-lookup"><span data-stu-id="4acea-129">Select **Import** to download the selected version from LCS to the current instance.</span></span>

    > [!NOTE]
    > <span data-ttu-id="4acea-130">ปุ่ม **นำเข้า** ใช้งานไม่ได้กับเวอร์ชันการตั้งค่าคอนฟิก ER ที่อยู่ในอินสแตนซ์ปัจจุบันอยู่แล้ว</span><span class="sxs-lookup"><span data-stu-id="4acea-130">The **Import** button is unavailable for ER configuration versions that are already present in the current instance.</span></span>

    <span data-ttu-id="4acea-131">[![หน้าที่เก็บการตั้งค่าคอนฟิก](./media/update-er-from-lcs-for-ms-download-configuration.png)](./media/update-er-from-lcs-for-ms-download-configuration.png)</span><span class="sxs-lookup"><span data-stu-id="4acea-131">[![Configuration repository page](./media/update-er-from-lcs-for-ms-download-configuration.png)](./media/update-er-from-lcs-for-ms-download-configuration.png)</span></span>

> [!NOTE]
> <span data-ttu-id="4acea-132">โดยขึ้นอยู่กับการตั้งค่า ER การตั้งค่าคอนฟิกจะได้รับการตรวจสอบความถูกต้องหลังจากที่มีการนำเข้าแล้ว</span><span class="sxs-lookup"><span data-stu-id="4acea-132">Depending on the ER settings, configurations are validated after they are imported.</span></span> <span data-ttu-id="4acea-133">คุณอาจได้รับแจ้งเกี่ยวกับปัญหาความไม่สอดคล้องใด ๆ ที่พบ</span><span class="sxs-lookup"><span data-stu-id="4acea-133">You might be notified about any inconsistency issues that are discovered.</span></span> <span data-ttu-id="4acea-134">คุณจะต้องแก้ไขปัญหาเหล่านั้นก่อนที่คุณจะสามารถใช้เวอร์ชันการตั้งค่าคอนฟิกที่นำเข้าได้</span><span class="sxs-lookup"><span data-stu-id="4acea-134">You must resolve those issues before you can use the imported configuration version.</span></span> <span data-ttu-id="4acea-135">สำหรับข้อมูลเพิ่มเติม ดูรายการของหัวข้อที่เกี่ยวข้องของหัวข้อนี้</span><span class="sxs-lookup"><span data-stu-id="4acea-135">For more information, see the list of related topics for this topic.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="4acea-136">ทรัพยากรเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="4acea-136">Additional resources</span></span>

[<span data-ttu-id="4acea-137">ภาพรวมการรายงานทางอิเล็กทรอนิกส์ (ER)</span><span class="sxs-lookup"><span data-stu-id="4acea-137">Electronic reporting (ER) overview</span></span>](general-electronic-reporting.md)

[<span data-ttu-id="4acea-138">ดาวน์โหลดการตั้งค่าคอนฟิก ER จากที่เก็บส่วนกลางของบริการตั้งค่าคอนฟิก</span><span class="sxs-lookup"><span data-stu-id="4acea-138">Download ER configurations from the Global repository of Configuration service</span></span>](er-download-configurations-global-repo.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
