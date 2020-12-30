---
title: นำเข้าการตั้งค่าคอนฟิก ER รุ่นที่อัปเดตแล้ว
description: หัวข้อนี้จะอธิบายถึงวิธีการนำเข้ารุ่นที่อัปเดตของการตั้งค่าคอนฟิกการรายงานทางอิเล็กทรอนิกส์ (ER) จากที่เก็บส่วนกลางของบริการตั้งค่าคอนฟิก
author: NickSelin
manager: AnnBe
ms.date: 06/09/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ERSolutionImport, ERWorkspace, ERSolutionRepositoryTable
audience: Application User, IT Pro
ms.reviewer: kfend
ms.custom: 105843
ms.assetid: dc44dea2-22ce-401e-98b9-d289e0e2825b
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-05-31
ms.dyn365.ops.version: AX 10.0.5
ms.openlocfilehash: 897663998c6c95ff6d7172de2abc4d4dd6ec5f12
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 12/05/2020
ms.locfileid: "4679521"
---
# <a name="import-updated-versions-of-er-configurations"></a><span data-ttu-id="0cb58-103">นำเข้าการตั้งค่าคอนฟิก ER รุ่นที่อัปเดตแล้ว</span><span class="sxs-lookup"><span data-stu-id="0cb58-103">Import updated versions of ER configurations</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="0cb58-104">[การจัดเก็บ](general-electronic-reporting.md#Repository) การรายงานทางอิเล็กทรอนิกส์ (ER) ที่ใช้ในการแชร์ [การตั้งค่าคอนฟิก ER](general-electronic-reporting.md#Configuration)</span><span class="sxs-lookup"><span data-stu-id="0cb58-104">Electronic reporting (ER) [repositories](general-electronic-reporting.md#Repository) are used to share [ER configurations](general-electronic-reporting.md#Configuration).</span></span> <span data-ttu-id="0cb58-105">คุณสามารถ [นำเข้า](download-electronic-reporting-configuration-lcs.md) การตั้งค่าคอนฟิก ER จากคลังที่แตกต่างกันเข้ากับอินสแตนซ์ของ Microsoft Dynamics 365 Finance</span><span class="sxs-lookup"><span data-stu-id="0cb58-105">You can [import](download-electronic-reporting-configuration-lcs.md) ER configurations from different repositories into your instance of Microsoft Dynamics 365 Finance.</span></span> <span data-ttu-id="0cb58-106">เมื่อคุณนำเข้าการตั้งค่าคอนฟิก ER [ผู้ให้บริการการตั้งค่าคอนฟิก](general-electronic-reporting.md#Provider) สามารถเผยแพร่การจัดเก็บ [รุ่น](general-electronic-reporting.md#component-versioning) ใหม่เพื่อให้สามารถใช้ร่วมกันได้</span><span class="sxs-lookup"><span data-stu-id="0cb58-106">When you import ER configurations, [configuration providers](general-electronic-reporting.md#Provider) can publish new [versions](general-electronic-reporting.md#component-versioning) repositories so that they can be shared.</span></span>

<span data-ttu-id="0cb58-107">หัวข้อนี้จะอธิบายถึงวิธีการนำเข้ารุ่นที่อัปเดตของการตั้งค่าคอนฟิก ER จากที่เก็บส่วนกลางของบริการตั้งค่าคอนฟิก</span><span class="sxs-lookup"><span data-stu-id="0cb58-107">This topic explains how to import updated versions of ER configurations from the Global repository of the Configuration service.</span></span> <span data-ttu-id="0cb58-108">สำหรับข้อมูลเพิ่มเติม ให้ดูที่ [Microsoft Dynamics 365 for Finance and Operations - Regulatory Services, Configuration service](https://docs.microsoft.com/business-applications-release-notes/october18/dynamics365-finance-operations/regulatory-service-configuration)</span><span class="sxs-lookup"><span data-stu-id="0cb58-108">For more information, see [Microsoft Dynamics 365 for Finance and Operations - Regulatory Services, Configuration service](https://docs.microsoft.com/business-applications-release-notes/october18/dynamics365-finance-operations/regulatory-service-configuration).</span></span>

## <a name="review-the-available-updated-versions"></a><span data-ttu-id="0cb58-109">ตรวจทานเวอร์ชันที่อัปเดตที่พร้อมใช้งาน</span><span class="sxs-lookup"><span data-stu-id="0cb58-109">Review the available updated versions</span></span>

1. <span data-ttu-id="0cb58-110">เข้าสู่ระบบการเงินโดยใช้หนึ่งในบทบาทต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="0cb58-110">Sign in to Finance by using one of the following roles:</span></span>

    - <span data-ttu-id="0cb58-111">นักพัฒนาการรายงานทางอิเล็กทรอนิกส์</span><span class="sxs-lookup"><span data-stu-id="0cb58-111">Electronic reporting developer</span></span>
    - <span data-ttu-id="0cb58-112">ที่ปรึกษาด้านการทำงานของการรายงานทางอิเล็กทรอนิกส์</span><span class="sxs-lookup"><span data-stu-id="0cb58-112">Electronic reporting functional consultant</span></span>
    - <span data-ttu-id="0cb58-113">ผู้ดูแลระบบ</span><span class="sxs-lookup"><span data-stu-id="0cb58-113">System administrator</span></span>

2. <span data-ttu-id="0cb58-114">ไปที่ **การจัดการองค์กร** \> **พื้นที่ทำงาน** \> **การรายงานทางอิเล็กทรอนิกส์**</span><span class="sxs-lookup"><span data-stu-id="0cb58-114">Go to **Organization administration** \> **Workspaces** \> **Electronic reporting**.</span></span>
3. <span data-ttu-id="0cb58-115">บนหน้า **การตั้งค่าคอนฟิกเฉพาะ** ในส่วน **ลิงก์ที่เกี่ยวข้อง** ให้เลือก **นำเข้าการอัปเดตรุ่นการตั้งค่าคอนฟิก**</span><span class="sxs-lookup"><span data-stu-id="0cb58-115">On the **Localization configurations** page, in the **Related links** section, select **Import configurations versions updates**.</span></span>

    ![หน้าการตั้งค่าคอนฟิกเฉพาะ](./media/er-download-updated-versions-global-repo1.png)

4. <span data-ttu-id="0cb58-117">ในกล่องโต้ตอบ **นำเข้าการอัปเดตรุ่นการตั้งค่าคอนฟิกการรายงานทางอิเล็กทรอนิกส์** ในฟิลด์ **โหมดการเรียกใช้** ให้เลือก **แสดงเฉพาะการอัปเดตที่พร้อมใช้งานเท่านั้น**</span><span class="sxs-lookup"><span data-stu-id="0cb58-117">In the **Import electronic reporting configurations versions updates** dialog box, in the **Run mode** field, select **Only show available updates**.</span></span> <span data-ttu-id="0cb58-118">จากนั้น เลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="0cb58-118">Then select **OK**.</span></span> 

    ![ตั้งค่าฟิลด์โหมดการเรียกใช้เพื่อแสดงเฉพาะการอัปเดตที่พร้อมใช้งานเท่านั้น](./media/er-download-updated-versions-global-repo2.png)

5. <span data-ttu-id="0cb58-120">ทบทวนข้อความที่คุณได้รับ</span><span class="sxs-lookup"><span data-stu-id="0cb58-120">Review the messages that you receive.</span></span> <span data-ttu-id="0cb58-121">ข้อความเหล่านี้แสดงข้อมูลต่อไปนี้เกี่ยวกับการตั้งค่าคอนฟิก ER ในอินสแตนซ์การเงินปัจจุบันและวิธีเปรียบเทียบกับเนื้อหาของที่เก็บส่วนกลาง:</span><span class="sxs-lookup"><span data-stu-id="0cb58-121">These messages provide the following information about the ER configurations in the current Finance instance and how they compare to the content of the Global repository:</span></span>

    - <span data-ttu-id="0cb58-122">จำนวนรวมของการตั้งค่าคอนฟิกการรายงานทางอิเล็กทรอนิกส์</span><span class="sxs-lookup"><span data-stu-id="0cb58-122">The total number of ER configurations</span></span>
    - <span data-ttu-id="0cb58-123">การตั้งค่าคอนฟิก ER ที่ไม่มีอยู่ในที่เก็บส่วนกลาง</span><span class="sxs-lookup"><span data-stu-id="0cb58-123">ER configurations that aren't present in the Global repository</span></span>
    - <span data-ttu-id="0cb58-124">การตั้งค่าคอนฟิก ER ซึ่งมีรุ่นล่าสุดอยู่แล้วในอินสแตนซ์การเงินปัจจุบัน (เพื่อดูรายการการตั้งค่าคอนฟิก ER เหล่านี้ทั้งหมด ให้เลือกลิงก์ **รายละเอียดของข้อความ**)</span><span class="sxs-lookup"><span data-stu-id="0cb58-124">ER configurations for which the latest version is already available in the current Finance instance (To view the full list of these ER configurations, select the **Message details** link.)</span></span>

        ![ข้อความและรายละเอียดข้อความ "รุ่นล่าสุดของการตั้งค่าคอนฟิกต่อไปนี้ถูกนำเข้าแล้ว"](./media/er-download-updated-versions-global-repo3.png)

    - <span data-ttu-id="0cb58-126">การตั้งค่าคอนฟิก ER ซึ่งมีรุ่นล่าสุดในที่เก็บส่วนกลางและสามารถนำเข้าไปยังอินสแตนซ์การเงินปัจจุบัน (เพื่อดูรายการการตั้งค่าคอนฟิก ER เหล่านี้ทั้งหมด ให้เลือกลิงก์ **รายละเอียดของข้อความ**)</span><span class="sxs-lookup"><span data-stu-id="0cb58-126">ER configurations for which the latest version is available in the Global repository and can be imported into the current Finance instance (To view the full list of these ER configurations, select the **Message details** link.)</span></span>

        ![ข้อความ "การอัปเดตที่พร้อมใช้งาน" และรายละเอียดข้อความ](./media/er-download-updated-versions-global-repo4.png)

## <a name="import-available-updated-versions"></a><span data-ttu-id="0cb58-128">นำเข้ารุ่นการอัปเดตที่พร้อมใช้งาน</span><span class="sxs-lookup"><span data-stu-id="0cb58-128">Import available updated versions</span></span>

1. <span data-ttu-id="0cb58-129">เข้าสู่ระบบการเงินโดยใช้หนึ่งในบทบาทต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="0cb58-129">Sign in to Finance by using one of the following roles:</span></span>

    - <span data-ttu-id="0cb58-130">นักพัฒนาการรายงานทางอิเล็กทรอนิกส์</span><span class="sxs-lookup"><span data-stu-id="0cb58-130">Electronic reporting developer</span></span>
    - <span data-ttu-id="0cb58-131">ที่ปรึกษาด้านการทำงานของการรายงานทางอิเล็กทรอนิกส์</span><span class="sxs-lookup"><span data-stu-id="0cb58-131">Electronic reporting functional consultant</span></span>
    - <span data-ttu-id="0cb58-132">ผู้ดูแลระบบ</span><span class="sxs-lookup"><span data-stu-id="0cb58-132">System administrator</span></span>

2. <span data-ttu-id="0cb58-133">ไปที่ **การจัดการองค์กร** \> **พื้นที่ทำงาน** \> **การรายงานทางอิเล็กทรอนิกส์**</span><span class="sxs-lookup"><span data-stu-id="0cb58-133">Go to **Organization administration** \> **Workspaces** \> **Electronic reporting**.</span></span>
3. <span data-ttu-id="0cb58-134">บนหน้า **การตั้งค่าคอนฟิกเฉพาะ** ในส่วน **ลิงก์ที่เกี่ยวข้อง** ให้เลือก **นำเข้าการอัปเดตรุ่นการตั้งค่าคอนฟิก**</span><span class="sxs-lookup"><span data-stu-id="0cb58-134">On the **Localization configurations** page, in the **Related links** section, select **Import configurations versions updates**.</span></span>
4. <span data-ttu-id="0cb58-135">ในกล่องโต้ตอบ **นำเข้ารุ่นการอัปเดตการตั้งค่าคอนฟิกการรายงานทางอิเล็กทรอนิกส์** ในฟิลด์ **โหมดการเรียกใช้** ให้เลือก **นำเข้าการอัปเดตล่าสุด** เพื่อนำเข้าการตั้งค่าคอนฟิก ER รุ่นล่าสุดจากที่เก็บสากลไปยังอินสแตนซ์การเงินปัจจุบัน</span><span class="sxs-lookup"><span data-stu-id="0cb58-135">In the **Import electronic reporting configurations versions updates** dialog box, in the **Run mode** field, select **Import latest updates** to import the latest versions of ER configurations from the Global repository into the current Finance instance.</span></span>
5. <span data-ttu-id="0cb58-136">เมื่อต้องการจัดกำหนดการชุดงานสำหรับการนำเข้า ในแท็บด่วน **รันในพื้นหลัง** ให้ตั้งค่าตัวเลือก **การประมวลผลชุดงาน** เป็น **ใช่**</span><span class="sxs-lookup"><span data-stu-id="0cb58-136">To schedule a batch job for the import, on the **Run in the background** FastTab, set the **Batch processing** option to **Yes**.</span></span> <span data-ttu-id="0cb58-137">ถ้าคุณต้องการนำเข้าซ้ำเป็นระยะๆ ให้ตั้งค่าคอนฟิกการเกิดซ้ำที่จำเป็น</span><span class="sxs-lookup"><span data-stu-id="0cb58-137">If you want to repeat the import periodically, configure the required recurrence.</span></span>

    ![ตั้งค่าฟิลด์โหมดการเรียกใช้เพื่อนำเข้าการอัปเดตล่าสุด](./media/er-download-updated-versions-global-repo5.png)

6. <span data-ttu-id="0cb58-139">เลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="0cb58-139">Select **OK**.</span></span>
7. <span data-ttu-id="0cb58-140">เมื่อต้องการเรียนรู้ว่ามีการนำเข้าเวอร์ชันการตั้งค่าคอนฟิกใด ให้ทำตามขั้นตอนใดขั้นตอนหนึ่งต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="0cb58-140">To learn what configuration versions have been imported, follow one of these steps:</span></span>

    - <span data-ttu-id="0cb58-141">ถ้าคุณรันการนำเข้าแบบโต้ตอบแทนการใช้ชุดงาน โปรดตรวจทานข้อความที่คุณได้รับ</span><span class="sxs-lookup"><span data-stu-id="0cb58-141">If you run the import interactively instead of using a batch job, review the messages that you receive.</span></span>

        ![ข้อความที่ได้รับระหว่างการรันการนำเข้าแบบโต้ตอบ](./media/er-download-updated-versions-global-repo6.png)

    - <span data-ttu-id="0cb58-143">ถ้าคุณรันการนำเข้าในโหมดชุดงาน ให้ทำตามขั้นตอนเหล่านี้:</span><span class="sxs-lookup"><span data-stu-id="0cb58-143">If you run the import in batch mode, follow these steps:</span></span>

        1. <span data-ttu-id="0cb58-144">ไปยัง **ทั่วไป** \> **การสอบถาม** \> **งานชุดงาน** \> **งานชุดงานของฉัน**</span><span class="sxs-lookup"><span data-stu-id="0cb58-144">Go to **Common** \> **Inquiries** \> **Batch jobs** \> **My batch jobs**.</span></span>
        2. <span data-ttu-id="0cb58-145">ค้นหาและเลือกงาน **นำเข้าการอัปเดตรุ่นการตั้งค่าคอนฟิกการรายงานทางอิเล็กทรอนิกส์** จากนั้นบนบานหน้าต่างการดำเนินการบนแท็บ **ชุดงาน** ให้เลือก **ประวัติชุดงาน** เพื่อดูประวัติงาน</span><span class="sxs-lookup"><span data-stu-id="0cb58-145">Find and select the **Import electronic reporting configurations versions updates** job, and then, on the Action Pane, on the **Batch job** tab, select **Batch job history** to view the job history.</span></span>
        3. <span data-ttu-id="0cb58-146">บนหน้า **ประวัติชุดงาน** ให้เลือก **ล็อก**</span><span class="sxs-lookup"><span data-stu-id="0cb58-146">On the **Batch job history** page, select **Log**.</span></span> <span data-ttu-id="0cb58-147">จากนั้นในข้อความที่คุณได้รับ ให้เลือกลิงก์ **รายละเอียดข้อความ** เพื่อดูล็อกงาน</span><span class="sxs-lookup"><span data-stu-id="0cb58-147">Then, in the message that you receive, select the **Message details** link to view the job log.</span></span>

        ![ล็อกงาน](./media/er-download-updated-versions-global-repo7.png)

> [!IMPORTANT]
> <span data-ttu-id="0cb58-149">เราไม่แนะนำให้คุณจัดกำหนดการงานชุดงานที่เกิดซ้ำเพื่อนำเข้าการตั้งค่าคอนฟิก ER รุ่นที่อัปเดตโดยตรงจากที่เก็บสากลในสภาพแวดล้อมการผลิต เนื่องจากรุ่นที่นำเข้าจะพร้อมใช้งานทันที</span><span class="sxs-lookup"><span data-stu-id="0cb58-149">We don't recommend that you schedule a recurring batch job to import updated versions of ER configurations directly from the Global repository into a production environment, because the imported versions will immediately be available for use.</span></span> <span data-ttu-id="0cb58-150">ใช้วิธีนี้ในการปรับใช้รุ่นการตั้งค่าคอนฟิก ER ไปยังสภาพแวดล้อม Sandbox</span><span class="sxs-lookup"><span data-stu-id="0cb58-150">Instead, use this approach to deploy versions of ER configurations to a sandbox environment.</span></span> <span data-ttu-id="0cb58-151">จากนั้นจะสามารถประเมินได้ในสภาพแวดล้อม Sandbox ก่อนที่จะมีการปรับใช้ไปยังสภาพแวดล้อมการผลิต</span><span class="sxs-lookup"><span data-stu-id="0cb58-151">They can then be evaluated in the sandbox environment before they are deployed to a production environment.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="0cb58-152">ทรัพยากรเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="0cb58-152">Additional resources</span></span>

- [<span data-ttu-id="0cb58-153">ภาพรวมการรายงานทางอิเล็กทรอนิกส์ (ER)</span><span class="sxs-lookup"><span data-stu-id="0cb58-153">Electronic reporting (ER) overview</span></span>](general-electronic-reporting.md)
- [<span data-ttu-id="0cb58-154">ดาวน์โหลดการตั้งค่าคอนฟิก ER จากที่เก็บส่วนกลางของบริการตั้งค่าคอนฟิก</span><span class="sxs-lookup"><span data-stu-id="0cb58-154">Download ER configurations from the Global repository of Configuration service</span></span>](er-download-configurations-global-repo.md)
