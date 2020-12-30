---
title: ใช้การตั้งค่าคอนฟิก ER ร่วมกันใน RCS/ที่เก็บส่วนกลางร่วมกับองค์กรภายนอก
description: หัวข้อนี้จะอธิบายถึงวิธีการแชร์การตั้งค่าคอนฟิกการรายงานทางอิเล็กทรอนิกส์ (ER) ใน Microsoft Regulatory Configuration Services (RCS) /ที่เก็บส่วนกลางกับองค์กรภายนอกโดยตรง
author: JaneA07
manager: AnnBe
ms.date: 05/04/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ERSolutionTable, ERWorkspace, RCS
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 97423
ms.assetid: ''
ms.search.region: Global
ms.author: janeaug
ms.search.validFrom: 2020-02-01
ms.dyn365.ops.version: AX 10.0.9
ms.openlocfilehash: 04c46824123906eccbfff18a03974c8043729e0a
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 10/13/2020
ms.locfileid: "4448471"
---
# <a name="share-electronic-reporting-er-configurations-in-regulatory-configuration-services-rcs-global-repository-with-external-organizations"></a><span data-ttu-id="b68ca-103">แชร์การตั้งค่าคอนฟิกการรายงานทางอิเล็กทรอนิกส์ (ER) ในที่เก็บส่วนกลาง Regulatory Configuration Services (RCS) กับองค์กรภายนอก</span><span class="sxs-lookup"><span data-stu-id="b68ca-103">Share Electronic reporting (ER) configurations in Regulatory Configuration Services (RCS) Global repository with external organizations</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="b68ca-104">คุณสามารถใช้ Microsoft Regulatory Configuration Services (RCS) เพื่อแชร์การตั้งค่าคอนฟิกการรายงานทางอิเล็กทรอนิกส์ (ER) แล้วเผยแพร่ไปยังองค์กรภายนอก</span><span class="sxs-lookup"><span data-stu-id="b68ca-104">You can use Microsoft Regulatory Configuration Services (RCS) to share Electronic reporting (ER) configurations and then publish them to external organizations.</span></span>

<span data-ttu-id="b68ca-105">ขั้นตอนต่อไปนี้อธิบายวิธีการที่ผู้ใช้ RCS สามารถใช้เวอร์ชันของการตั้งค่าคอนฟิก ER ที่ได้รับการตั้งค่าคอนฟิกในอินสแตนซ์ RCS กับองค์กรภายนอกร่วมกัน</span><span class="sxs-lookup"><span data-stu-id="b68ca-105">The following procedures explain how an RCS user can share a version of an ER configuration that has been configured in an RCS instance with an external organization.</span></span> <span data-ttu-id="b68ca-106">ก่อนที่คุณจะสามารถดำเนินกระบวนงานเหล่านั้นให้เสร็จสมบูรณ์ คุณจะต้องดำเนินการตามข้อกำหนดเบื้องต้นต่อไปนี้ให้เสร็จสมบูรณ์:</span><span class="sxs-lookup"><span data-stu-id="b68ca-106">Before you can complete those procedures, you must complete the following prerequisites:</span></span>

- <span data-ttu-id="b68ca-107">เข้าถึงอินสแตนซ์ RCS</span><span class="sxs-lookup"><span data-stu-id="b68ca-107">Access an RCS instance.</span></span>
- <span data-ttu-id="b68ca-108">สร้างผู้ให้บริการการตั้งค่าคอนฟิกที่ใช้งานอยู่</span><span class="sxs-lookup"><span data-stu-id="b68ca-108">Create an active configuration provider.</span></span> <span data-ttu-id="b68ca-109">สำหรับข้อมูลเพิ่มเติม ให้ดูที่ [สร้างผู้ให้บริการการตั้งค่าคอนฟิก และทำเครื่องหมายเป็นใช้งานอยู่](../../fin-ops-core/dev-itpro/analytics/tasks/er-configuration-provider-mark-it-active-2016-11.md)</span><span class="sxs-lookup"><span data-stu-id="b68ca-109">For more information, see [Create configuration providers and mark them as active](../../fin-ops-core/dev-itpro/analytics/tasks/er-configuration-provider-mark-it-active-2016-11.md).</span></span>
- <span data-ttu-id="b68ca-110">สร้างและอัปโหลดการตั้งค่าคอนฟิก ER เวอร์ชันใหม่</span><span class="sxs-lookup"><span data-stu-id="b68ca-110">Create and upload a new version of an ER configuration.</span></span> <span data-ttu-id="b68ca-111">สำหรับข้อมูลเพิ่มเติม ให้ดูที่ [สร้างและอัปโหลดการตั้งค่าคอนฟิกการรายงานทางอิเล็กทรอนิกส์ (ER) เวอร์ชันใหม่](rcs-global-repo-upload.md)</span><span class="sxs-lookup"><span data-stu-id="b68ca-111">For more information, see [Create and upload a new version of an Electronic reporting (ER) configuration](rcs-global-repo-upload.md).</span></span>

<span data-ttu-id="b68ca-112">นอกจากนี้คุณต้องตรวจสอบให้แน่ใจว่ามีการเตรียมใช้งานสภาพแวดล้อม RCS สำหรับบริษัทของคุณ</span><span class="sxs-lookup"><span data-stu-id="b68ca-112">You must also make sure that an RCS environment is provisioned for your company.</span></span>

1. <span data-ttu-id="b68ca-113">ในแอป Finance and Operations ไปที่ **การจัดการองค์กร** \> **พื้นที่ทำงาน** \> **การรายงานทางอิเล็กทรอนิกส์**</span><span class="sxs-lookup"><span data-stu-id="b68ca-113">In a Finance and Operations app, go to **Organization administration** \> **Workspaces** \> **Electronic reporting**.</span></span>
2. <span data-ttu-id="b68ca-114">ถ้าไม่มีสภาพแวดล้อม RCS ที่จัดเตรียมสำหรับบริษัทของคุณ ให้เลือก **Regulatory services – การตั้งค่าคอนฟิกภายนอก** และทำตามคำแนะนำเพื่อจัดเตรียมสภาพแวดล้อม</span><span class="sxs-lookup"><span data-stu-id="b68ca-114">If no RCS environment is provisioned for your company, select **Regulatory services – Configuration external**, and then follow the instructions to provision one.</span></span>

<span data-ttu-id="b68ca-115">ถ้ามีการจัดเตรียมสภาพแวดล้อม RCS ให้กับบริษัทของคุณแล้ว ให้ใช้ URL ของหน้าเพื่อเข้าถึงโดยเลือกตัวเลือกการลงชื่อเข้าใช้</span><span class="sxs-lookup"><span data-stu-id="b68ca-115">If an RCS environment has been already provisioned for your company, use the page URL to access it by selecting the sign-in option.</span></span>

## <a name="verify-the-configuration-that-you-want-to-share"></a><span data-ttu-id="b68ca-116">ตรวจสอบการตั้งค่าคอนฟิกที่คุณต้องการใช้ร่วมกัน</span><span class="sxs-lookup"><span data-stu-id="b68ca-116">Verify the configuration that you want to share</span></span>

<span data-ttu-id="b68ca-117">ให้ทำตามขั้นตอนต่อไปนี้เพื่อตรวจสอบว่าการตั้งค่าคอนฟิกที่คุณต้องการใช้ร่วมกันถูกอัปโหลดไปยังที่เก็บส่วนกลางแล้ว</span><span class="sxs-lookup"><span data-stu-id="b68ca-117">Follow these steps to verify that the configuration that you want to share has already been uploaded to the Global repository.</span></span>

1. <span data-ttu-id="b68ca-118">ในพื้นที่ทำงาน **การรายงานอิเล็กทรอนิกส์** ให้เลือก **ที่เก็บ** สำหรับผู้ให้บริการการตั้งค่าคอนฟิกของคุณ</span><span class="sxs-lookup"><span data-stu-id="b68ca-118">In the **Electronic reporting** workspace, select **Repositories** for your configuration provider.</span></span>

    ![ผู้ให้บริการการตั้งค่าคอนฟิก](https://github.com/MicrosoftDocs/Dynamics-365-Operations/blob/Janeaug_RCSdocs/articles/finance/localizations/media/1_RCS_Repo_for_config_provider.JPG)

2. <span data-ttu-id="b68ca-120">เลือก **ที่เก็บส่วนกลาง** \> **เปิด**</span><span class="sxs-lookup"><span data-stu-id="b68ca-120">Select **Global repository** \> **Open**.</span></span>
3. <span data-ttu-id="b68ca-121">ค้นหาการตั้งค่าคอนฟิกที่คุณต้องการใช้ร่วมกัน</span><span class="sxs-lookup"><span data-stu-id="b68ca-121">Search for the configuration that you want to share.</span></span> <span data-ttu-id="b68ca-122">คุณสามารถใช้ฟิลด์ตัวกรองเพื่อจำกัดการค้นหาของคุณให้แคบลง</span><span class="sxs-lookup"><span data-stu-id="b68ca-122">You can use the filter field to narrow your search.</span></span> <span data-ttu-id="b68ca-123">ถ้าคุณไม่พบการตั้งค่าคอนฟิกในที่เก็บส่วนกลาง ให้ทำตามขั้นตอนใน [สร้างและอัปโหลดการตั้งค่าคอนฟิกการรายงานทางอิเล็กทรอนิกส์ (ER) เวอร์ชันใหม่](rcs-global-repo-upload.md)</span><span class="sxs-lookup"><span data-stu-id="b68ca-123">If you can't find the configuration in the Global repository, follow the steps in [Create and upload a new version of an Electronic reporting (ER) configuration](rcs-global-repo-upload.md).</span></span>

## <a name="share-er-configurations-with-external-organizations"></a><span data-ttu-id="b68ca-124">ใช้การตั้งค่าคอนฟิก ER ในกับกับองค์กรภายนอก</span><span class="sxs-lookup"><span data-stu-id="b68ca-124">Share ER configurations with external organizations</span></span>

<span data-ttu-id="b68ca-125">หลังจากที่มีการสร้างการตั้งค่าคอนฟิกภายใต้ผู้ให้บริการการตั้งค่าคอนฟิกของคุณแล้ว คุณสามารถใช้ร่วมกันโดยตรงกับองค์กรภายนอกโดยใช้แท็บด่วน **ใช้ร่วมกันกับ** บนหน้า **ที่เก็บการตั้งค่าคอนฟิกส่วนกลาง**</span><span class="sxs-lookup"><span data-stu-id="b68ca-125">After a configuration has been created under your configuration provider, you can share it directly with external organizations by using the **Shared with** FastTab on the **Global configuration repository** page.</span></span>

1. <span data-ttu-id="b68ca-126">ในพื้นที่ทำงาน **การรายงานอิเล็กทรอนิกส์** ให้เลือก **ที่เก็บ** สำหรับผู้ให้บริการการตั้งค่าคอนฟิกของคุณ</span><span class="sxs-lookup"><span data-stu-id="b68ca-126">In the **Electronic reporting** workspace, select **Repositories** for your configuration provider.</span></span>
2. <span data-ttu-id="b68ca-127">เลือก **ที่เก็บส่วนกลาง** \> **เปิด**</span><span class="sxs-lookup"><span data-stu-id="b68ca-127">Select **Global repository** \> **Open**.</span></span> 
3. <span data-ttu-id="b68ca-128">เลือกการตั้งค่าคอนฟิกที่คุณต้องการใช้ร่วมกัน</span><span class="sxs-lookup"><span data-stu-id="b68ca-128">Select the configuration that you want to share.</span></span>
4. <span data-ttu-id="b68ca-129">บนแท็บด่วน **ใช้ร่วมกันกับ** ให้เลือก **องค์กร**</span><span class="sxs-lookup"><span data-stu-id="b68ca-129">On the **Shared with** FastTab, select **Organization**.</span></span>

    ![แท็บด่วนใช้ร่วมกันกับ](https://github.com/MicrosoftDocs/Dynamics-365-Operations/blob/Janeaug_RCSdocs/articles/finance/localizations/media/1_RCS_Repo_for_Share_with_org.JPG)

5. <span data-ttu-id="b68ca-131">ในกล่องโต้ตอบ ให้ป้อนชื่อโดเมนสำหรับองค์กรภายนอก แล้วเลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="b68ca-131">In the dialog box, enter the domain name for the external organization, and then select **OK**.</span></span>

    ![การใช้เวอร์ชันการตั้งค่าคอนฟิกร่วมกันกับกล่องโต้ตอบองค์กรภายนอก](https://github.com/MicrosoftDocs/Dynamics-365-Operations/blob/Janeaug_RCSdocs/articles/finance/localizations/media/1_RCS_Repo_for_Share_with_form.JPG)

<span data-ttu-id="b68ca-133">การตั้งค่าคอนฟิกที่ใช้ร่วมกันกับองค์กรภายนอกและพร้อมใช้งานสำหรับองค์กรนั้นในที่เก็บส่วนกลาง</span><span class="sxs-lookup"><span data-stu-id="b68ca-133">The configuration is shared with the external organization and is available to that organization in the Global repository.</span></span> <span data-ttu-id="b68ca-134">จากที่นั่น สามารถนำเข้าไปยังอินสแตนซ์ขององค์กรของ RCS หรืออินสแตนซ์ของแอป Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="b68ca-134">From there, it can be imported into the organization's instance of RCS or into its instances of Finance and Operations apps.</span></span>

![การตั้งค่าคอนฟิกที่ใช้ร่วมกันกับองค์กรภายนอก](https://github.com/MicrosoftDocs/Dynamics-365-Operations/blob/Janeaug_RCSdocs/articles/finance/localizations/media/1_RCS_Repo_for_Share_with_test.com)

6. <span data-ttu-id="b68ca-136">เมื่อต้องการยกเลิกการใช้ร่วมกันของการตั้งค่าคอนฟิกร่วมกับองค์กรภายนอกก่อนหน้านี้ โปรดเลือกการตั้งค่าคอนฟิก แล้วคลิก **ยกเลิกการใช้ร่วมกัน** แล้วเลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="b68ca-136">To unshare a configuration that has been previously shared with an external organization, select the configuration and click **Unshare**, and then select **OK**</span></span>
