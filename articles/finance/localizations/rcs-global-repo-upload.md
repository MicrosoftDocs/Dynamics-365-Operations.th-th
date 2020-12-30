---
title: สร้างการตั้งค่าคอนฟิก ER ใน RCS และอัปโหลดไปยังที่เก็บส่วนกลาง
description: หัวข้อนี้จะอธิบายถึงวิธีการสร้างการตั้งค่าคอนฟิกการรายงานทางอิเล็กทรอนิกส์ (ER) ใน Microsoft Regulatory Configuration Services (RCS) และอัปโหลดไปยังที่เก็บส่วนกลาง
author: JaneA07
manager: AnnBe
ms.date: 09/21/2020
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
ms.openlocfilehash: 5b2b8f35b9931f8fd1824c20e9045da68af33ad5
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 10/13/2020
ms.locfileid: "4448470"
---
# <a name="create-er-configurations-in-regulatory-configuration-services-rcs-and-upload-them-to-the-global-repository"></a><span data-ttu-id="27b1a-103">สร้างการตั้งค่าคอนฟิก ER ใน Regulatory Configuration Services (RCS) และอัปโหลดไปยังที่เก็บส่วนกลาง</span><span class="sxs-lookup"><span data-stu-id="27b1a-103">Create ER configurations in Regulatory Configuration Services (RCS) and upload them to the Global repository</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="27b1a-104">คุณสามารถใช้ Microsoft Regulatory Configuration Services (RCS) เพื่อออกแบบการตั้งค่าคอนฟิกการรายงานทางอิเล็กทรอนิกส์ (ER) และเผยแพร่เพื่อให้สามารถใช้ในองค์กรของคุณได้</span><span class="sxs-lookup"><span data-stu-id="27b1a-104">You can use Microsoft Regulatory Configuration Services (RCS) to design Electronic reporting (ER) configurations and publish them so that they can be used in your organization.</span></span>

<span data-ttu-id="27b1a-105">ขั้นตอนต่อไปนี้จะอธิบายวิธีการที่ผู้ใช้ในบทบาทของผู้ดูแลระบบหรือผู้พัฒนาการรายงานทางอิเล็กทรอนิกส์สามารถสร้างเวอร์ชันที่ได้รับมาจากการตั้งค่าคอนฟิก ER ซึ่งถูกตั้งค่าคอนฟิกในอินสแตนซ์ RCS แล้วอัปโหลดการตั้งค่าคอนฟิกที่ได้รับไปยังที่เก็บส่วนกลาง</span><span class="sxs-lookup"><span data-stu-id="27b1a-105">The following procedures explain how a user in the System Administrator or Electronic Reporting Developer role can create a derived version of an ER configuration that has been configured in an RCS instance, and then upload the derived configuration to the Global repository.</span></span> 

<span data-ttu-id="27b1a-106">ก่อนที่คุณจะสามารถดำเนินกระบวนงานเหล่านั้นให้เสร็จสมบูรณ์ คุณจะต้องดำเนินการตามข้อกำหนดเบื้องต้นต่อไปนี้ให้เสร็จสมบูรณ์:</span><span class="sxs-lookup"><span data-stu-id="27b1a-106">Before you can complete those procedures, you must complete the following prerequisites:</span></span>

- <span data-ttu-id="27b1a-107">เข้าถึงอินสแตนซ์ RCS</span><span class="sxs-lookup"><span data-stu-id="27b1a-107">Access an RCS instance.</span></span>
- <span data-ttu-id="27b1a-108">สร้างผู้ให้บริการการตั้งค่าคอนฟิกที่ใช้งานอยู่</span><span class="sxs-lookup"><span data-stu-id="27b1a-108">Create an active configuration provider.</span></span> <span data-ttu-id="27b1a-109">สำหรับข้อมูลเพิ่มเติม ให้ดูที่ [สร้างผู้ให้บริการการตั้งค่าคอนฟิก และทำเครื่องหมายเป็นใช้งานอยู่](../../fin-ops-core/dev-itpro/analytics/tasks/er-configuration-provider-mark-it-active-2016-11.md)</span><span class="sxs-lookup"><span data-stu-id="27b1a-109">For more information, see [Create configuration providers and mark them as active](../../fin-ops-core/dev-itpro/analytics/tasks/er-configuration-provider-mark-it-active-2016-11.md).</span></span>

<span data-ttu-id="27b1a-110">นอกจากนี้คุณต้องตรวจสอบให้แน่ใจว่ามีการเตรียมใช้งานสภาพแวดล้อม RCS สำหรับบริษัทของคุณ</span><span class="sxs-lookup"><span data-stu-id="27b1a-110">You must also make sure that an RCS environment is provisioned for your company.</span></span>

1. <span data-ttu-id="27b1a-111">ในแอป Finance and Operations ไปที่ **การจัดการองค์กร** \> **พื้นที่ทำงาน** \> **การรายงานทางอิเล็กทรอนิกส์**</span><span class="sxs-lookup"><span data-stu-id="27b1a-111">In a Finance and Operations app, go to **Organization administration** \> **Workspaces** \> **Electronic reporting**.</span></span>
2. <span data-ttu-id="27b1a-112">ถ้าไม่มีสภาพแวดล้อม RCS ที่จัดเตรียมสำหรับบริษัทของคุณ ให้เลือก **Regulatory services – การตั้งค่าคอนฟิกภายนอก** และทำตามคำแนะนำเพื่อจัดเตรียมสภาพแวดล้อม</span><span class="sxs-lookup"><span data-stu-id="27b1a-112">If no RCS environment is provisioned for your company, select **Regulatory services – Configuration external**, and then follow the instructions to provision one.</span></span>

<span data-ttu-id="27b1a-113">ถ้ามีการจัดเตรียมสภาพแวดล้อม RCS ให้กับบริษัทของคุณแล้ว ให้ใช้ URL ของหน้าเพื่อเข้าถึงโดยเลือกตัวเลือกการลงชื่อเข้าใช้</span><span class="sxs-lookup"><span data-stu-id="27b1a-113">If an RCS environment has been already provisioned for your company, use the page URL to access it by selecting the sign-in option.</span></span>

## <a name="create-a-derived-version-of-a-configuration-in-rcs"></a><span data-ttu-id="27b1a-114">สร้างเวอร์ชันที่ได้รับมาจากการตั้งค่าคอนฟิกใน RCS</span><span class="sxs-lookup"><span data-stu-id="27b1a-114">Create a derived version of a configuration in RCS</span></span>

1. <span data-ttu-id="27b1a-115">ในพื้นที่ทำงาน **การรายงานทางอิเล็กทรอนิกส์** ให้ตรวจสอบว่าคุณมีผู้ให้บริการการตั้งค่าคอนฟิกที่ใช้งานอยู่สำหรับองค์กรของคุณ</span><span class="sxs-lookup"><span data-stu-id="27b1a-115">In the **Electronic reporting** workspace, verify that you have an active configuration provider for your organization.</span></span> 
2. <span data-ttu-id="27b1a-116">เลือก **การตั้งค่าคอนฟิกการรายงาน**</span><span class="sxs-lookup"><span data-stu-id="27b1a-116">Select **Reporting configurations**.</span></span>
3. <span data-ttu-id="27b1a-117">เลือกการตั้งค่าคอนฟิกที่คุณต้องการรับมาจากเวอร์ชันใหม่</span><span class="sxs-lookup"><span data-stu-id="27b1a-117">Select the configuration that you want to derive a new version from.</span></span> <span data-ttu-id="27b1a-118">คุณสามารถใช้ฟิลด์ตัวกรองข้อมูลด้านบนของแผนภูมิลำดับชั้นเพื่อจำกัดการค้นหาของคุณให้แคบลง</span><span class="sxs-lookup"><span data-stu-id="27b1a-118">You can use the filter field above the tree to narrow your search.</span></span>
4. <span data-ttu-id="27b1a-119">เลือก **สร้างการตั้งค่าคอนฟิก** \> **ได้รับมาจากชื่อ**</span><span class="sxs-lookup"><span data-stu-id="27b1a-119">Select **Create configuration** \> **Derive from Name**.</span></span>
5. <span data-ttu-id="27b1a-120">ป้อนชื่อและคำอธิบาย แล้วเลือก **สร้างการตั้งค่าคอนฟิก** เพื่อสร้างเวอร์ชันที่รับมาใหม่</span><span class="sxs-lookup"><span data-stu-id="27b1a-120">Enter a name and description, and then select **Create configuration** to create a new derived version.</span></span>
6. <span data-ttu-id="27b1a-121">เลือกการตั้งค่าคอนฟิกที่สืบทอดมาใหม่ เพิ่มคำอธิบายของเวอร์ชัน แล้วเลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="27b1a-121">Select the newly derived configuration, add a description of the version, and then select **OK**.</span></span> <span data-ttu-id="27b1a-122">สถานะของธุรกรรมการตั้งค่าคอนฟิกเปลี่ยนเป็น **เสร็จสมบูรณ์**</span><span class="sxs-lookup"><span data-stu-id="27b1a-122">The status of the configuration to is changed to **Completed**.</span></span>

![เวอร์ชันการตั้งค่าคอนฟิกใหม่ใน RCS](media/RCS_CompleteConfig.JPG)

> [!NOTE]
> <span data-ttu-id="27b1a-124">เมื่อสถานะของการตั้งค่าคอนฟิกมีการเปลี่ยนแปลง คุณอาจได้รับข้อความแสดงข้อผิดพลาดของการตรวจสอบความถูกต้องที่เกี่ยวข้องกับแอปพลิเคชันที่เชื่อมต่อ</span><span class="sxs-lookup"><span data-stu-id="27b1a-124">When the configuration status is changed, you might receive a validation error message that is related to the connected applications.</span></span> <span data-ttu-id="27b1a-125">เมื่อต้องการปิดใช้งานการตรวจสอบความถูกต้อง ในบานหน้าต่างการดำเนินการบนแท็บ **การตั้งค่าคอนฟิก** ให้เลือก **พารามิเตอร์ผู้ใช้** แล้วตั้งค่าตัวเลือก **ข้ามการตรวจสอบความถูกต้องของการเปลี่ยนแปลงสถานะและการปรับใช้ซ้ำของการตั้งค่าคอนฟิก** เป็น **ใช่**</span><span class="sxs-lookup"><span data-stu-id="27b1a-125">To turn off the validation, on the Action Pane on the **Configurations** tab, select **User parameters**, and then set the **Skip validation at configuration's status change and rebase** option to **Yes**</span></span> 

## <a name="upload-a-configuration-to-the-global-repository"></a><span data-ttu-id="27b1a-126">อัปโหลดการตั้งค่าคอนฟิกไปยังที่เก็บสากล</span><span class="sxs-lookup"><span data-stu-id="27b1a-126">Upload a configuration to the Global repository</span></span>

<span data-ttu-id="27b1a-127">เมื่อต้องการใช้การตั้งค่าคอนฟิกใหม่หรือที่ได้รับมาร่วมกับองค์กรของคุณ คุณสามารถอัปโหลดไปยังที่เก็บส่วนกลางได้</span><span class="sxs-lookup"><span data-stu-id="27b1a-127">To share a new or derived configuration with your organization, you can upload it to the Global repository.</span></span>

1. <span data-ttu-id="27b1a-128">เลือกเวอร์ชันที่เสร็จสมบูรณ์ของการตั้งค่าคอนฟิก แล้วเลือก **อัปโหลดลงในที่เก็บ**</span><span class="sxs-lookup"><span data-stu-id="27b1a-128">Select the completed version of the configuration, and then select **Upload into repository**.</span></span>
2. <span data-ttu-id="27b1a-129">เลือกตัวเลือก **สากล (Microsoft)** แล้วเลือก **อัปโหลด**</span><span class="sxs-lookup"><span data-stu-id="27b1a-129">Select the **Global (Microsoft)** option, and then select **Upload**.</span></span>

    ![อัปโหลดไปยังตัวเลือกของที่เก็บ](media/RCS_Upload_to_GlobalRepo_options.JPG)

3. <span data-ttu-id="27b1a-131">ในกล่องข้อความยืนยัน เลือก **ใช่**</span><span class="sxs-lookup"><span data-stu-id="27b1a-131">In the confirmation message box, select **Yes**.</span></span> 
4. <span data-ttu-id="27b1a-132">อัปเดตคำอธิบายของเวอร์ชันตามต้องการ แล้วเลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="27b1a-132">Update the description of the version as required, and then select **OK**.</span></span> 

<span data-ttu-id="27b1a-133">สถานะของการตั้งค่าคอนฟิกถูกอัปเดตเป็น **ใช้ร่วมกัน** และมีการอัปโหลดการตั้งค่าคอนฟิกไปยังที่เก็บสากล</span><span class="sxs-lookup"><span data-stu-id="27b1a-133">The status of the configuration is updated to **Share**, and the configuration is uploaded to the Global repository.</span></span> <span data-ttu-id="27b1a-134">จากที่นั่นคุณสามารถทำงานด้วยวิธีการดังต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="27b1a-134">From there, you can work with it in the following ways:</span></span>

- <span data-ttu-id="27b1a-135">นำเข้าไปในอินสแตนซ์ของ Dynamics 365 ของคุณ</span><span class="sxs-lookup"><span data-stu-id="27b1a-135">Import it into your Dynamics 365 instance.</span></span> <span data-ttu-id="27b1a-136">สำหรับข้อมูลเพิ่มเติม โปรดดู [(ER) นำเข้าการตั้งค่าคอนฟิกจาก RCS](../../fin-ops-core/dev-itpro/analytics/tasks/import-configuration-rcs.md)</span><span class="sxs-lookup"><span data-stu-id="27b1a-136">For more information, see [(ER) Import configurations from RCS](../../fin-ops-core/dev-itpro/analytics/tasks/import-configuration-rcs.md).</span></span>
- <span data-ttu-id="27b1a-137">ใช้ร่วมกันกับบุคคลที่สามหรือองค์กรภายนอก ให้ดูที่ [การตั้งค่าคอนฟิกการรายงานทางอิเล็กทรอนิกส์ (ER) ของ RCS ร่วมกับองค์กรภายนอก](rcs-global-repo-share-configuration.md)</span><span class="sxs-lookup"><span data-stu-id="27b1a-137">Share it with a third party or an external organization, see [RCS Share Electronic reporting (ER) configurations with external organizations](rcs-global-repo-share-configuration.md)</span></span>

    ![เวอร์ชันการตั้งค่าคอนฟิก Contoso อินทราสแทตที่ได้รับมาในที่เก็บสากล](media/RCS_Config_upload_GlobalRepo.JPG)

## <a name="delete-a-configuration-from-the-global-repository"></a><span data-ttu-id="27b1a-139">อัปโหลดการตั้งค่าคอนฟิกจากที่เก็บสากล</span><span class="sxs-lookup"><span data-stu-id="27b1a-139">Delete a configuration from the Global repository</span></span>
<span data-ttu-id="27b1a-140">ดำเนินการขั้นตอนต่อไปนี้ให้เสร็จสมบูรณ์เพื่อลบการตั้งค่าคอนฟิกที่องค์กรของคุณสร้างขึ้น</span><span class="sxs-lookup"><span data-stu-id="27b1a-140">Complete the following steps to delete a configuration that your organization has created.</span></span>

1. <span data-ttu-id="27b1a-141">ในพื้นที่ทำงาน **การรายงานอิเล็กทรอนิกส์** ให้ตรวจสอบว่าผู้ให้บริการการตั้งค่าคอนฟิกของคุณ **เปิดใช้งาน**</span><span class="sxs-lookup"><span data-stu-id="27b1a-141">In the **Electronic reporting** workspace, verify that your configuration provider is **Active**.</span></span> <span data-ttu-id="27b1a-142">สำหรับข้อมูลเพิ่มเติม ให้ดูที่ [สร้างผู้ให้บริการการตั้งค่าคอนฟิก และทำเครื่องหมายเป็นใช้งานอยู่](../../fin-ops-core/dev-itpro/analytics/tasks/er-configuration-provider-mark-it-active-2016-11.md)</span><span class="sxs-lookup"><span data-stu-id="27b1a-142">For more information, see [Create configuration providers and mark them as active](../../fin-ops-core/dev-itpro/analytics/tasks/er-configuration-provider-mark-it-active-2016-11.md).</span></span>
2. <span data-ttu-id="27b1a-143">บนตัวให้บริการการตั้งค่าคอนฟิกที่ใช้งานอยู่ ให้เลือก **ที่เก็บข้อมูล**</span><span class="sxs-lookup"><span data-stu-id="27b1a-143">On your active configuration provider, select **repository**.</span></span>
3. <span data-ttu-id="27b1a-144">เลือกชนิดของที่เก็บ **สากล** และเลือก **เปิด**</span><span class="sxs-lookup"><span data-stu-id="27b1a-144">Select the repository type **Global**, and select **Open**.</span></span>
4. <span data-ttu-id="27b1a-145">บนแท็บด่วน **ตัวกรอง** ให้ค้นหาการตั้งค่าคอนฟิกที่คุณต้องการลบโดยใช้ฟังก์ชัน **ตัวกรอง**</span><span class="sxs-lookup"><span data-stu-id="27b1a-145">On the **Filter** FastTab, find the configuration that you want to delete by using the **Filter** functionality.</span></span>
5. <span data-ttu-id="27b1a-146">บนแท็บด่วน **เวอร์ชัน** ให้เลือกเวอร์ชันของการตั้งค่าคอนฟิกที่คุณต้องการลบแล้วเลือก **ลบ**:</span><span class="sxs-lookup"><span data-stu-id="27b1a-146">On the **Version** FastTab, select the version of the configuration that you want to delete, and then select **Delete**:</span></span>

    ![ลบการตั้งค่าคอนฟิกจากที่เก็บสากล](media/RCS_Delete_from_GlobalRepo.JPG)

6. <span data-ttu-id="27b1a-148">ในกล่องข้อความยืนยัน เลือก **ใช่**</span><span class="sxs-lookup"><span data-stu-id="27b1a-148">In the confirmation message box, select **Yes**.</span></span>

    ![ลบข้อความยืนยันเวอร์ชันของการตั้งค่าคอนฟิก](media/RCS_Delete_from_GlobalRepo_Msg.JPG)
 
<span data-ttu-id="27b1a-150">มีการลบเวอร์ชันของการตั้งค่าคอนฟิกและข้อความยืนยันจะแสดงขึ้น</span><span class="sxs-lookup"><span data-stu-id="27b1a-150">The configuration version is deleted, and confirmation message is shown.</span></span> 

> [!NOTE]
> <span data-ttu-id="27b1a-151">การตั้งค่าคอนฟิกสามารถลบออกได้โดยผู้ให้บริการการตั้งค่าคอนฟิกที่สร้างขึ้นเท่านั้น</span><span class="sxs-lookup"><span data-stu-id="27b1a-151">Configurations can only be deleted by the Configuration provider that created them.</span></span> <span data-ttu-id="27b1a-152">ถ้ามีการใช้การตั้งค่าคอนฟิกร่วมกับองค์กรอื่น การตั้งค่าคอนฟิกจะต้องได้รับการยกเลิกหารใช้ร่วมกันก่อนที่จะลบ</span><span class="sxs-lookup"><span data-stu-id="27b1a-152">If the configuration has been shared with another organization, the configuration will need to be unshared before you delete it.</span></span>
 
