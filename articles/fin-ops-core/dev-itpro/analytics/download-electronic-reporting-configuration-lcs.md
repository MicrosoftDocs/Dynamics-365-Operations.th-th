---
title: ดาวน์โหลดการตั้งค่าคอนฟิกการรายงานแบบอิเล็กทรอนิกส์จาก Lifecycle Services
description: หัวข้อนี้อธิบายวิธีการดาวน์โหลดการตั้งค่าคอนฟิกการรายงานทางอิเล็กทรอนิกส์ (ER) จาก Microsoft Dynamics Lifecycle Services (LCS)
author: NickSelin
manager: AnnBe
ms.date: 06/20/2017
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
ms.openlocfilehash: 561187343073a84b152151abe8770e89196eaa56
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 09/27/2019
ms.locfileid: "2174132"
---
# <a name="download-electronic-reporting-configurations-from-lifecycle-services"></a><span data-ttu-id="ad553-103">ดาวน์โหลดการตั้งค่าคอนฟิกการรายงานแบบอิเล็กทรอนิกส์จาก Lifecycle Services</span><span class="sxs-lookup"><span data-stu-id="ad553-103">Download Electronic reporting configurations from Lifecycle Services</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="ad553-104">หัวข้อนี้อธิบายวิธีการดาวน์โหลดการตั้งค่าคอนฟิกการรายงานทางอิเล็กทรอนิกส์ (ER) จาก Microsoft Dynamics Lifecycle Services (LCS)</span><span class="sxs-lookup"><span data-stu-id="ad553-104">This topic explains how to download Electronic reporting (ER) configurations from Microsoft Dynamics Lifecycle Services (LCS).</span></span>

<span data-ttu-id="ad553-105">บทช่วยสอนนี้แนะนำกระบวนการของการดาวน์โหลดรุ่นใหม่ที่สุดของการตั้งค่าคอนฟิกการรายงานทางอิเล็กทรอนิกส์ (ER) จาก Microsoft Dynamics Lifecycle Services (LCS)</span><span class="sxs-lookup"><span data-stu-id="ad553-105">This tutorial guides you through the process of downloading the newest version of Electronic reporting (ER) configurations from Microsoft Dynamics Lifecycle Services (LCS).</span></span>

1. <span data-ttu-id="ad553-106">ลงชื่อเข้าใช้ในแอพลิเคชันโดยใช้หนึ่งในบทบาทต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="ad553-106">Sign in to the application by using one of the following roles:</span></span>

    - <span data-ttu-id="ad553-107">นักพัฒนาการรายงานทางอิเล็กทรอนิกส์</span><span class="sxs-lookup"><span data-stu-id="ad553-107">Electronic reporting developer</span></span>
    - <span data-ttu-id="ad553-108">ที่ปรึกษาด้านการทำงานของการรายงานทางอิเล็กทรอนิกส์</span><span class="sxs-lookup"><span data-stu-id="ad553-108">Electronic reporting functional consultant</span></span>
    - <span data-ttu-id="ad553-109">ผู้ดูแลระบบ</span><span class="sxs-lookup"><span data-stu-id="ad553-109">System administrator</span></span>

2. <span data-ttu-id="ad553-110">ไปที่ **การจัดการองค์กร** &gt; **การรายงานทางอิเล็กทรอนิกส์**</span><span class="sxs-lookup"><span data-stu-id="ad553-110">Go to **Organization administration** &gt; **Electronic reporting**.</span></span>
3. <span data-ttu-id="ad553-111">ในส่วน **ผู้ให้บริการการตั้งค่าคอนฟิก** เลือกไทล์ **Microsoft**</span><span class="sxs-lookup"><span data-stu-id="ad553-111">In the **Configuration providers** section, select the **Microsoft** tile.</span></span>
4. <span data-ttu-id="ad553-112">บนไทล์ **Microsoft** คลิก **ที่เก็บ**</span><span class="sxs-lookup"><span data-stu-id="ad553-112">On the **Microsoft** tile, click **Repositories**.</span></span>

    <span data-ttu-id="ad553-113">[![อัพเดต ER จาก LCS สำหรับ MS - เปิดรายการที่เก็บ MS](./media/update-er-from-lcs-for-ms-open-ms-repositories-list.png)](./media/update-er-from-lcs-for-ms-open-ms-repositories-list.png)</span><span class="sxs-lookup"><span data-stu-id="ad553-113">[![update-er-from-lcs-for-ms-open-ms-repositories-list](./media/update-er-from-lcs-for-ms-open-ms-repositories-list.png)](./media/update-er-from-lcs-for-ms-open-ms-repositories-list.png)</span></span>

5. <span data-ttu-id="ad553-114">บนหน้า **ที่เก็บการตั้งค่าคอนฟิก** ในกริด เลือกที่เก็บที่มีอยู่ของชนิด **LCS**</span><span class="sxs-lookup"><span data-stu-id="ad553-114">On the **Configuration repositories** page, in the grid, select the existing repository of the **LCS** type.</span></span> <span data-ttu-id="ad553-115">ถ้าที่เก็บนี้ไม่ปรากฏในกริด ให้ทำตามขั้นตอนเหล่านี้:</span><span class="sxs-lookup"><span data-stu-id="ad553-115">If this repository doesn't appear in the grid, follow these steps:</span></span>

    1. <span data-ttu-id="ad553-116">คลิก **เพิ่ม** เพื่อเพิ่มที่เก็บใหม่</span><span class="sxs-lookup"><span data-stu-id="ad553-116">Click **Add** to add a new repository.</span></span>
    2. <span data-ttu-id="ad553-117">เลือก **LCS** เป็นชนิดที่เก็บ</span><span class="sxs-lookup"><span data-stu-id="ad553-117">Select **LCS** as the repository type.</span></span>
    3. <span data-ttu-id="ad553-118">คลิก **สร้างที่เก็บ**</span><span class="sxs-lookup"><span data-stu-id="ad553-118">Click **Create repository**.</span></span>
    4. <span data-ttu-id="ad553-119">หากได้รับการแจ้ง ให้ทำตามคำแนะนำการตรวจสอบ</span><span class="sxs-lookup"><span data-stu-id="ad553-119">If prompted, follow the authorization instructions.</span></span>
    5. <span data-ttu-id="ad553-120">ป้อนชื่อและคำอธิบายสำหรับที่เก็บ</span><span class="sxs-lookup"><span data-stu-id="ad553-120">Enter a name and description for the repository.</span></span>
    6. <span data-ttu-id="ad553-121">คลิก **ตกลง** เพื่อยืนยันรายการที่เก็บใหม่</span><span class="sxs-lookup"><span data-stu-id="ad553-121">Click **OK** to confirm the new repository entry.</span></span>
    7. <span data-ttu-id="ad553-122">ในกริด เลือกที่เก็บใหม่ของชนิด **LCS**</span><span class="sxs-lookup"><span data-stu-id="ad553-122">In the grid, select the new repository of the **LCS** type.</span></span>

6. <span data-ttu-id="ad553-123">คลิก **เปิด** เพื่อดูรายการของการตั้งค่าคอนฟิก ER สำหรับที่เก็บที่เลือก</span><span class="sxs-lookup"><span data-stu-id="ad553-123">Click **Open** to view the list of ER configurations for the selected repository.</span></span>

    <span data-ttu-id="ad553-124">[![อัพเดต ER จาก LCS สำหรับ MS - สร้างที่เก็บ LCS](./media/update-er-from-lcs-for-ms-make-lcs-repository.png)](./media/update-er-from-lcs-for-ms-make-lcs-repository.png)</span><span class="sxs-lookup"><span data-stu-id="ad553-124">[![update-er-from-lcs-for-ms-make-lcs-repository](./media/update-er-from-lcs-for-ms-make-lcs-repository.png)](./media/update-er-from-lcs-for-ms-make-lcs-repository.png)</span></span>

7. <span data-ttu-id="ad553-125">ในแผนภูมิการตั้งค่าคอนฟิกในบานหน้าต่างด้านซ้าย ให้เลือกการตั้งค่าคอนฟิก ER ที่คุณต้องการ</span><span class="sxs-lookup"><span data-stu-id="ad553-125">In the configurations tree in the left pane, select the ER configuration that you require.</span></span>
8. <span data-ttu-id="ad553-126">บน FastTab **เวอร์ชัน** เลือกเวอร์ชันที่กำหนดของการตั้งค่าคอนฟิก ER ที่เลือก</span><span class="sxs-lookup"><span data-stu-id="ad553-126">On the **Versions** FastTab, select the required version of the selected ER configuration.</span></span>
9. <span data-ttu-id="ad553-127">คลิก **นำเข้า** เพื่อดาวน์โหลดเวอร์ชันที่เลือกจาก LCS ไปยังอินสแตนซ์ปัจจุบัน</span><span class="sxs-lookup"><span data-stu-id="ad553-127">Click **Import** to download the selected version from LCS to the current instance.</span></span>

    > [!NOTE]
    > <span data-ttu-id="ad553-128">ปุ่ม **นำเข้า** ใช้งานไม่ได้กับเวอร์ชันการตั้งค่าคอนฟิก ER ที่อยู่ในอินสแตนซ์ปัจจุบันอยู่แล้ว</span><span class="sxs-lookup"><span data-stu-id="ad553-128">The **Import** button is unavailable for ER configuration versions that are already present in the current instance.</span></span>

    <span data-ttu-id="ad553-129">[![อัพเดต ER จาก LCS สำหรับ MS - ดาวน์โหลดการตั้งค่าคอนฟิก](./media/update-er-from-lcs-for-ms-download-configuration.png)](./media/update-er-from-lcs-for-ms-download-configuration.png)</span><span class="sxs-lookup"><span data-stu-id="ad553-129">[![update-er-from-lcs-for-ms-download-configuration](./media/update-er-from-lcs-for-ms-download-configuration.png)](./media/update-er-from-lcs-for-ms-download-configuration.png)</span></span>

> [!NOTE]
> <span data-ttu-id="ad553-130">โดยขึ้นอยู่กับการตั้งค่า ER การตั้งค่าคอนฟิกจะได้รับการตรวจสอบความถูกต้องหลังจากที่มีการนำเข้าแล้ว</span><span class="sxs-lookup"><span data-stu-id="ad553-130">Depending on the ER settings, configurations are validated after they are imported.</span></span> <span data-ttu-id="ad553-131">คุณอาจได้รับแจ้งเกี่ยวกับปัญหาความไม่สอดคล้องใด ๆ ที่พบ</span><span class="sxs-lookup"><span data-stu-id="ad553-131">You might be notified about any inconsistency issues that are discovered.</span></span> <span data-ttu-id="ad553-132">คุณจะต้องแก้ไขปัญหาเหล่านั้นก่อนที่คุณจะสามารถใช้เวอร์ชันการตั้งค่าคอนฟิกที่นำเข้าได้</span><span class="sxs-lookup"><span data-stu-id="ad553-132">You must resolve those issues before you can use the imported configuration version.</span></span> <span data-ttu-id="ad553-133">สำหรับข้อมูลเพิ่มเติม ดูรายการของบทความที่เกี่ยวข้องของหัวข้อนี้</span><span class="sxs-lookup"><span data-stu-id="ad553-133">For more information, see the list of related articles for this topic.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="ad553-134">ทรัพยากรเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="ad553-134">Additional resources</span></span>

[<span data-ttu-id="ad553-135">ภาพรวมการรายงานทางอิเล็กทรอนิกส์</span><span class="sxs-lookup"><span data-stu-id="ad553-135">Electronic reporting overview</span></span>](general-electronic-reporting.md)
