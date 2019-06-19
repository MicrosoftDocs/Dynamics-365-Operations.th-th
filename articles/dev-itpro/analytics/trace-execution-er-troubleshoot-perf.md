---
title: การดำเนินการติดตามของรูปแบบ ER เพื่อแก้ไขปัญหาประสิทธิภาพการทำงาน
description: หัวข้อนี้จะนำเสนอข้อมูลเกี่ยวกับวิธีการใช้คุณลักษณะการติดตามประสิทธิภาพในการรายงานทางอิเล็กทรอนิกส์ (ER) เพื่อแก้ไขปัญหาประสิทธิภาพการทำงาน
author: NickSelin
manager: AnnBe
ms.date: 05/08/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 220314
ms.assetid: 2685df16-5ec8-4fd7-9495-c0f653e82567
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: ''
ms.dyn365.ops.version: 10.0.1
ms.openlocfilehash: aa71db2752889bc905c22bab1cf2fa46d7ee07c7
ms.sourcegitcommit: 67d00b95952faf0db580d341249d4e50be59119c
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 05/15/2019
ms.locfileid: "1576557"
---
# <a name="trace-the-execution-of-er-formats-to-troubleshoot-performance-issues"></a><span data-ttu-id="327de-103">ติดตามการดำเนินการของรูปแบบ ER เพื่อแก้ไขปัญหาประสิทธิภาพการทำงาน</span><span class="sxs-lookup"><span data-stu-id="327de-103">Trace the execution of ER formats to troubleshoot performance issues</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="327de-104">ในฐานะที่เป็นส่วนหนึ่งของกระบวนการในการออกแบบการตั้งค่าคอนฟิกการรายงานทางอิเล็กทรอนิกส์ (ER) เพื่อสร้างเอกสารอิเล็กทรอนิกส์ คุณกำหนดวิธีการที่จะใช้ในการดึงข้อมูลออกจาก Microsoft Dynamics 365 for Finance and Operations และป้อนข้อมูลในเอาท์พุทที่สร้างขึ้น</span><span class="sxs-lookup"><span data-stu-id="327de-104">As part of the process of designing Electronic reporting (ER) configurations to generate electronic documents, you define the method that is used to get data out of Microsoft Dynamics 365 for Finance and Operations and enter it in the output that is generated.</span></span> <span data-ttu-id="327de-105">คุณลักษณะการติดตามประสิทธิภาพของ ER ช่วยลดเวลาและต้นทุนอย่างมากซึ่งเกี่ยวข้องในการรวบรวมรายละเอียดของการดำเนินการจัดรูปแบบ ER และการใช้เพื่อแก้ไขปัญหาประสิทธิภาพการทำงาน</span><span class="sxs-lookup"><span data-stu-id="327de-105">The ER performance trace feature helps significantly reduce the time and cost that are involved in collecting the details of ER format execution and using them to troubleshoot performance issues.</span></span> <span data-ttu-id="327de-106">บทช่วยสอนนี้จะให้คำแนะนำเกี่ยวกับวิธีการดำเนินการติดตามประสิทธิภาพสำหรับรูปแบบ ER ที่ดำเนินการใน Finance and Operations และวิธีการใช้ข้อมูลจากการติดตามเหล่านี้เพื่อช่วยในการปรับปรุงประสิทธิภาพการทำงาน</span><span class="sxs-lookup"><span data-stu-id="327de-106">This tutorial provides guidelines about how to take performance traces for executed ER formats in Finance and Operations, and how to use the information from these traces to help improve performance.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="327de-107">ข้อกำหนดเบื้องต้น</span><span class="sxs-lookup"><span data-stu-id="327de-107">Prerequisites</span></span>

<span data-ttu-id="327de-108">เพื่อทำตัวอย่างในบทช่วยสอนนี้ให้เสร็จสมบูรณ์ คุณต้องมีการเข้าถึงต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="327de-108">To complete the examples in this tutorial, you must have the following access:</span></span>

- <span data-ttu-id="327de-109">การเข้าถึง Finance and Operations สำหรับหนึ่งในบทบาทต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="327de-109">Access to Finance and Operations for one of the following roles:</span></span>

    - <span data-ttu-id="327de-110">นักพัฒนาการรายงานทางอิเล็กทรอนิกส์</span><span class="sxs-lookup"><span data-stu-id="327de-110">Electronic reporting developer</span></span>
    - <span data-ttu-id="327de-111">ที่ปรึกษาด้านการทำงานของการรายงานทางอิเล็กทรอนิกส์</span><span class="sxs-lookup"><span data-stu-id="327de-111">Electronic reporting functional consultant</span></span>
    - <span data-ttu-id="327de-112">ผู้ดูแลระบบ</span><span class="sxs-lookup"><span data-stu-id="327de-112">System administrator</span></span>

- <span data-ttu-id="327de-113">การเข้าถึงอินสแตนซ์ของ Regulatory Configuration Services (RCS) ที่ได้เตรียมใช้งานสำหรับผู้เช่ารายเดียวกันกับ Finance and Operations สำหรับหนึ่งในบทบาทต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="327de-113">Access to the instance of Regulatory Configuration Services (RCS) that has been provisioned for the same tenant as Finance and Operations, for one of the following roles:</span></span>

    - <span data-ttu-id="327de-114">นักพัฒนาการรายงานทางอิเล็กทรอนิกส์</span><span class="sxs-lookup"><span data-stu-id="327de-114">Electronic reporting developer</span></span>
    - <span data-ttu-id="327de-115">ที่ปรึกษาด้านการทำงานของการรายงานทางอิเล็กทรอนิกส์</span><span class="sxs-lookup"><span data-stu-id="327de-115">Electronic reporting functional consultant</span></span>
    - <span data-ttu-id="327de-116">ผู้ดูแลระบบ</span><span class="sxs-lookup"><span data-stu-id="327de-116">System administrator</span></span>

<span data-ttu-id="327de-117">นอกจากนี้ คุณต้องดาวน์โหลดและจัดเก็บไฟล์ต่อไปนี้โดยเฉพาะ</span><span class="sxs-lookup"><span data-stu-id="327de-117">You must also download and locally store the following files.</span></span>

| <span data-ttu-id="327de-118">ไฟล์</span><span class="sxs-lookup"><span data-stu-id="327de-118">File</span></span>                                  | <span data-ttu-id="327de-119">ปริมาณความจุ</span><span class="sxs-lookup"><span data-stu-id="327de-119">Content</span></span>                               |
|---------------------------------------|---------------------------------------|
| <span data-ttu-id="327de-120">แบบจำลองการติดตามประสิทธิภาพการทำงาน รุ่น 1</span><span class="sxs-lookup"><span data-stu-id="327de-120">Performance trace model.version.1</span></span>     | [<span data-ttu-id="327de-121">การตั้งค่าคอนฟิกแบบจำลองข้อมูล ER ตัวอย่าง</span><span class="sxs-lookup"><span data-stu-id="327de-121">Sample ER data model configuration</span></span>](https://mbs.microsoft.com/customersource/Global/AX/downloads/hot-fixes/365optelecrepeg)    |
| <span data-ttu-id="327de-122">ข้อมูลเมตาการติดตามประสิทธิภาพการทำงาน รุ่น 1</span><span class="sxs-lookup"><span data-stu-id="327de-122">Performance trace metadata.version.1</span></span>  | [<span data-ttu-id="327de-123">การตั้งค่าคอนฟิกข้อมูลเมตา ER ตัวอย่าง</span><span class="sxs-lookup"><span data-stu-id="327de-123">Sample ER metadata configuration</span></span>](https://mbs.microsoft.com/customersource/Global/AX/downloads/hot-fixes/365optelecrepeg)      |
| <span data-ttu-id="327de-124">การแม็ปการติดตามประสิทธิภาพการทำงาน รุ่น 1.1</span><span class="sxs-lookup"><span data-stu-id="327de-124">Performance trace mapping.version.1.1</span></span> | [<span data-ttu-id="327de-125">การตั้งค่าคอนฟิกการแม็ปแบบจำลองข้อมูล ER ตัวอย่าง</span><span class="sxs-lookup"><span data-stu-id="327de-125">Sample ER model mapping configuration</span></span>](https://mbs.microsoft.com/customersource/Global/AX/downloads/hot-fixes/365optelecrepeg) |
| <span data-ttu-id="327de-126">รูปแบบการติดตามประสิทธิภาพการทำงาน รุ่น 1.1</span><span class="sxs-lookup"><span data-stu-id="327de-126">Performance trace format.version.1.1</span></span>  | [<span data-ttu-id="327de-127">การตั้งค่าคอนฟิกรูปแบบ ER ตัวอย่าง</span><span class="sxs-lookup"><span data-stu-id="327de-127">Sample ER format configuration</span></span>](https://mbs.microsoft.com/customersource/Global/AX/downloads/hot-fixes/365optelecrepeg)       |

### <a name="configure-er-parameters"></a><span data-ttu-id="327de-128">ตั้งค่าคอนฟิกพารามิเตอร์ ER</span><span class="sxs-lookup"><span data-stu-id="327de-128">Configure ER parameters</span></span>

<span data-ttu-id="327de-129">การติดตามประสิทธิภาพ ER แต่ละรายการที่สร้างขึ้นใน Finance and Operations จะถูกจัดเก็บเป็นเอกสารแนบของเรกคอร์ดล็อกการดำเนินการ</span><span class="sxs-lookup"><span data-stu-id="327de-129">Each ER performance trace that is generated in Finance and Operations is stored as an attachment of the execution log record.</span></span> <span data-ttu-id="327de-130">กรอบงานการจัดการเอกสาร (DM) ของ Finance and Operations ถูกใช้ในการจัดการเอกสารแนบเหล่านี้</span><span class="sxs-lookup"><span data-stu-id="327de-130">The Document management (DM) framework of Finance and Operations is used to manage these attachments.</span></span> <span data-ttu-id="327de-131">คุณต้องตั้งค่าคอนฟิกพารามิเตอร์ ER ล่วงหน้า เพื่อระบุชนิดเอกสาร DM ที่ควรใช้เพื่อแนบการติดตามประสิทธิภาพ</span><span class="sxs-lookup"><span data-stu-id="327de-131">You must configure ER parameters in advance, to specify the DM document type that should be used to attach performance traces.</span></span> <span data-ttu-id="327de-132">ใน Finance and Operation พื้นที่ทำงาน**การรายงานทางอิเล็กทรอนิกส์** ให้เลือก **พารามิเตอร์การรายงานทางอิเล็กทรอนิกส์**</span><span class="sxs-lookup"><span data-stu-id="327de-132">In Finance and Operation, in the **Electronic reporting** workspace, select **Electronic reporting parameters**.</span></span> <span data-ttu-id="327de-133">จากนั้น บนหน้า **พารามิเตอร์การรายงานทางอิเล็กทรอนิกส์** บนแท็บ **เอกสารแนบ** ในฟิลด์ **อื่นๆ** ให้เลือกชนิดเอกสาร DM เพื่อใช้สำหรับการติดตามประสิทธิภาพ</span><span class="sxs-lookup"><span data-stu-id="327de-133">Then, on the **Electronic reporting parameters** page, on the **Attachments** tab, in the **Others** field, select the DM document type to use for performance traces.</span></span>

![หน้าพารามิเตอร์การรายงานทางอิเล็กทรอนิกส์ใน Finance and Operations](./media/GER-PerfTrace-GER-Parameters-DocumentType.png)

<span data-ttu-id="327de-135">เพื่อให้พร้อมใช้งานในฟิลด์การค้นหา **อื่นๆ** ชนิดเอกสาร DM ต้องมีการตั้งค่าคอนฟิกในลักษณะต่อไปนี้บนหน้า **ชนิดเอกสาร** (**การจัดการองค์กร \> การจัดการเอกสาร \> ชนิดเอกสาร**):</span><span class="sxs-lookup"><span data-stu-id="327de-135">To be available in the **Others** lookup field, a DM document type must be configured in the following manner on the **Document types** page (**Organization administration \> Document management \> Document types**):</span></span>

- <span data-ttu-id="327de-136">**คลาส:** แนบไฟล์</span><span class="sxs-lookup"><span data-stu-id="327de-136">**Class:** Attach file</span></span>
- <span data-ttu-id="327de-137">**กลุ่ม:** ไฟล์</span><span class="sxs-lookup"><span data-stu-id="327de-137">**Group:** File</span></span>

![หน้าชนิดเอกสารใน Finance and Operations](./media/GER-PerfTrace-DM-DocumentType.png)

> [!NOTE]
> <span data-ttu-id="327de-139">ชนิดเอกสารที่เลือกต้องพร้อมใช้งานในทุกๆ บริษัทของอินสแตนซ์ Finance and Operations ปัจจุบัน เพราะไฟล์แนบ DM เป็นแบบเฉพาะบริษัท</span><span class="sxs-lookup"><span data-stu-id="327de-139">The selected document type must be available in every company of the current Finance and Operations instance, because DM attachments are company-specific.</span></span>

### <a name="configure-rcs-parameters"></a><span data-ttu-id="327de-140">ตั้งค่าคอนฟิกพารามิเตอร์ RCS</span><span class="sxs-lookup"><span data-stu-id="327de-140">Configure RCS parameters</span></span>

<span data-ttu-id="327de-141">การติดตามประสิทธิภาพ ER ซึ่งสร้างขึ้นใน Finance and Operations จะถูกนำเข้าไปยัง RCS สำหรับการวิเคราะห์ โดยใช้ตัวออกแบบรูปแบบ ER และตัวออกแบบการแม็ป ER</span><span class="sxs-lookup"><span data-stu-id="327de-141">ER performance traces that are generated in Finance and Operations will be imported into RCS for analysis by using the ER format designer and the ER mapping designer.</span></span> <span data-ttu-id="327de-142">เนื่องจากมีการจัดเก็บการติดตามประสิทธิภาพ ER เป็นเอกสารแนบของเรกคอร์ดบันทึกการดำเนินการที่เกี่ยวข้องกับรูปแบบ ER คุณต้องตั้งค่าคอนฟิกพารามิเตอร์ RCS ล่วงหน้า เพื่อระบุชนิดของเอกสาร DM ที่ควรใช้เพื่อแนบการติดตามประสิทธิภาพ</span><span class="sxs-lookup"><span data-stu-id="327de-142">Because ER performance traces are stored as attachments of the execution log record that is related to the ER format, you must configure RCS parameters in advance, to specify the DM document type that should be used to attach performance traces.</span></span> <span data-ttu-id="327de-143">ในอินสแตนซ์ของ RCS ที่จัดเตรียมให้กับบริษัทของคุณ ในพื้นที่ทำงาน **การรายงานทางอิเล็กทรอนิกส์** ให้เลือก **พารามิเตอร์การรายงานทางอิเล็กทรอนิกส์**</span><span class="sxs-lookup"><span data-stu-id="327de-143">In the instance of RCS that has been provisioned for your company, in the **Electronic reporting** workspace, select **Electronic reporting parameters**.</span></span> <span data-ttu-id="327de-144">จากนั้น บนหน้า **พารามิเตอร์การรายงานทางอิเล็กทรอนิกส์** บนแท็บ **เอกสารแนบ** ในฟิลด์ **อื่นๆ** ให้เลือกชนิดเอกสาร DM เพื่อใช้สำหรับการติดตามประสิทธิภาพ</span><span class="sxs-lookup"><span data-stu-id="327de-144">Then, on the **Electronic reporting parameters** page, on the **Attachments** tab, in the **Others** field, select the DM document type to use for performance traces.</span></span>

![หน้าพารามิเตอร์การรายงานทางอิเล็กทรอนิกส์ใน RCS](./media/GER-PerfTrace-RCS-Parameters-DocumentType.png)

<span data-ttu-id="327de-146">เพื่อให้พร้อมใช้งานในฟิลด์การค้นหา **อื่นๆ** ชนิดเอกสาร DM ต้องมีการตั้งค่าคอนฟิกในลักษณะต่อไปนี้บนหน้า **ชนิดเอกสาร** (**การจัดการองค์กร \> การจัดการเอกสาร \> ชนิดเอกสาร**):</span><span class="sxs-lookup"><span data-stu-id="327de-146">To be available in the **Others** lookup field, a DM document type must be configured in the following manner on the **Document types** page (**Organization administration \> Document management \> Document types**):</span></span>

- <span data-ttu-id="327de-147">**คลาส:** แนบไฟล์</span><span class="sxs-lookup"><span data-stu-id="327de-147">**Class:** Attach file</span></span>
- <span data-ttu-id="327de-148">**กลุ่ม:** ไฟล์</span><span class="sxs-lookup"><span data-stu-id="327de-148">**Group:** File</span></span>

## <a name="design-an-er-solution"></a><span data-ttu-id="327de-149">ออกแบบโซลูชัน ER</span><span class="sxs-lookup"><span data-stu-id="327de-149">Design an ER solution</span></span>

<span data-ttu-id="327de-150">สมมติว่าคุณได้เริ่มต้นการออกแบบโซลูชัน ER ใหม่เพื่อสร้างรายงานใหม่ที่แสดงธุรกรรมผู้จัดจำหน่าย</span><span class="sxs-lookup"><span data-stu-id="327de-150">Assume that you've started to design a new ER solution to generate a new report that presents vendor transactions.</span></span> <span data-ttu-id="327de-151">ในปัจจุบัน คุณสามารถค้นหาธุรกรรมสำหรับผู้จัดจำหน่ายที่เลือกบนหน้า **ธุรกรรมผู้จัดจำหน่าย** (ไปยัง **บัญชีเจ้าหนี้ \> ผู้จัดจำหน่าย \> ผู้จัดจำหน่ายทั้งหมด** ให้เลือกผู้จัดจำหน่าย และจากนั้น ในบานหน้าต่างการดำเนินการ บนแท็บ **ผู้จัดจำหน่าย** ในกลุ่ม **ธุรกรรม** ให้เลือก **ธุรกรรม**)</span><span class="sxs-lookup"><span data-stu-id="327de-151">Currently, you can find the transactions for a selected vendor on the **Vendor transactions** page (go to **Account payable \> Vendors \> All vendors**, select a vendor, and then, on the Action Pane, on the **Vendor** tab, in the **Transactions** group, select **Transactions**).</span></span> <span data-ttu-id="327de-152">อย่างไรก็ตาม คุณต้องการให้มีธุรกรรมผู้จัดจำหน่ายทั้งหมดในเวลาเดียวกันในเอกสารอิเล็กทรอนิกส์หนึ่งรายการในรูปแบบ XML</span><span class="sxs-lookup"><span data-stu-id="327de-152">However, you want to have all vendor transaction at the same time in one electronic document in XML format.</span></span> <span data-ttu-id="327de-153">โซลูชันนี้จะประกอบด้วยการตั้งค่าคอนฟิก ER ต่างๆ ที่มีรูปแบบข้อมูลที่จำเป็นต้องใช้ ข้อมูลเมตา การแม็ปแบบจำลอง และส่วนประกอบรูปแบบ</span><span class="sxs-lookup"><span data-stu-id="327de-153">This solution will consist of several ER configurations that contain the required data model, metadata, model mapping, and format components.</span></span>

1. <span data-ttu-id="327de-154">ลงชื่อเข้าใช้อินสแตนซ์ของ RCS ที่ได้เตรียมใช้งานสำหรับบริษัทของคุณ</span><span class="sxs-lookup"><span data-stu-id="327de-154">Sign in to the instance of RCS that has been provisioned for your company.</span></span>
2. <span data-ttu-id="327de-155">ในบทช่วยสอนนี้ คุณจะสร้างและปรับเปลี่ยนการตั้งค่าคอนฟิกสำหรับบริษัทตัวอย่าง **Litware, Inc.**</span><span class="sxs-lookup"><span data-stu-id="327de-155">In this tutorial, you will create and modify configurations for the **Litware, Inc.** sample company.</span></span> <span data-ttu-id="327de-156">ดังนั้น โปรดตรวจสอบให้แน่ใจว่าได้เพิ่มตัวให้บริการการตั้งค่าคอนฟิกนี้ลงใน RCS และได้เลือกเป็นใช้งานอยู่</span><span class="sxs-lookup"><span data-stu-id="327de-156">Therefore, make sure that this configuration provider has been added to RCS and selected as active.</span></span> <span data-ttu-id="327de-157">สำหรับคำแนะนำ ให้ดูที่กระบวนงาน [สร้างตัวให้บริการการตั้งค่าคอนฟิก และทำเครื่องหมายเป็นใช้งานอยู่](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/analytics/tasks/er-configuration-provider-mark-it-active-2016-11)</span><span class="sxs-lookup"><span data-stu-id="327de-157">For instructions, see the [Create configuration providers and mark them as active](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/analytics/tasks/er-configuration-provider-mark-it-active-2016-11) procedure.</span></span>
3. <span data-ttu-id="327de-158">ในพื้นที่ทำงาน **การรายงานทางอิเล็กทรอนิกส์** เลือกไทล์ **การตั้งค่าคอนฟิกการรายงาน**</span><span class="sxs-lookup"><span data-stu-id="327de-158">In the **Electronic reporting** workspace, select the **Reporting configurations** tile.</span></span>
4. <span data-ttu-id="327de-159">ในหน้า **การตั้งค่าคอนฟิก** นำเข้าการตั้งค่าคอนฟิก ER ที่คุณดาวน์โหลดเป็นข้อกำหนดเบื้องต้นลงใน RCS ตามลำดับต่อไปนี้: รูปแบบข้อมูล ข้อมูลเมตา การแม็ปแบบจำลอง รูปแบบ</span><span class="sxs-lookup"><span data-stu-id="327de-159">On the **Configurations** page, import the ER configurations that you downloaded as a prerequisite into RCS, in the following order: data model, metadata, model mapping, format.</span></span> <span data-ttu-id="327de-160">สำหรับการตั้งค่าคอนฟิกแต่ละรายการ ทำตามขั้นตอนเหล่านี้:</span><span class="sxs-lookup"><span data-stu-id="327de-160">For each configuration, follow these steps:</span></span>

    1. <span data-ttu-id="327de-161">ในบานหน้าต่างการดำเนินการ เลือก **แลกเปลี่ยน \> โหลดจากไฟล์ XML**</span><span class="sxs-lookup"><span data-stu-id="327de-161">On the Action Pane, select **Exchange \> Load from XML file**.</span></span>
    2. <span data-ttu-id="327de-162">เลือก **เรียกดู** เพื่อเลือกไฟล์ที่เหมาะสมสำหรับการตั้งค่าคอนฟิก ER ที่จำเป็นในรูปแบบ XML</span><span class="sxs-lookup"><span data-stu-id="327de-162">Select **Browse** to select the appropriate file for the required ER configuration in XML format.</span></span>
    3. <span data-ttu-id="327de-163">เลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="327de-163">Select **OK**.</span></span>

    ![หน้าการตั้งค่าคอนฟิกใน RCS](./media/GER-PerfTrace-RCS-ImportedConfigurations.png)

## <a name="run-the-er-solution-to-trace-execution"></a><span data-ttu-id="327de-165">รันโซลูชัน ER เพื่อติดตามการดำเนินการ</span><span class="sxs-lookup"><span data-stu-id="327de-165">Run the ER solution to trace execution</span></span>

<span data-ttu-id="327de-166">สมมติว่าคุณได้ออกแบบโซลูชัน ER รุ่นแรกเสร็จเรียบร้อยแล้ว</span><span class="sxs-lookup"><span data-stu-id="327de-166">Assume that you've finished designing the first version of the ER solution.</span></span> <span data-ttu-id="327de-167">ขณะนี้คุณต้องการทดสอบในอินสแตนซ์ Finance and Operations ของคุณ และวิเคราะห์ประสิทธิภาพในการดำเนินงาน</span><span class="sxs-lookup"><span data-stu-id="327de-167">You now want to test it in your Finance and Operations instance and analyze execution performance.</span></span>

### <a id='import-configuration'></a><span data-ttu-id="327de-168">นำเข้าการตั้งค่าคอนฟิก ER จาก RCS ไปยัง Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="327de-168">Import an ER configuration from RCS into Finance and Operations</span></span>

1. <span data-ttu-id="327de-169">ลงชื่อเข้าใช้อินสแตนซ์การเงินและการดำเนินงานของคุณ</span><span class="sxs-lookup"><span data-stu-id="327de-169">Sign in to your Finance and Operations instance.</span></span>
2. <span data-ttu-id="327de-170">สำหรับบทช่วยสอนนี้ คุณจะนำเข้าการตั้งค่าคอนฟิกจากอินสแตนซ์ RCS ของคุณ (ที่ซึ่งคุณออกแบบส่วนประกอบ ER ของคุณ) ลงในอินสแตนซ์ Finance and Operations ของคุณ (ที่ซึ่งคุณทดสอบและใช้งานในที่สุด)</span><span class="sxs-lookup"><span data-stu-id="327de-170">For this tutorial, you will import configurations from your RCS instance (where you design your ER components) into your Finance and Operations instance (where you test and finally use them).</span></span> <span data-ttu-id="327de-171">ดังนั้น คุณต้องตรวจสอบให้แน่ใจว่ามีการจัดเตรียมอาร์ทิแฟกต์ที่จำเป็นทั้งหมดแล้ว</span><span class="sxs-lookup"><span data-stu-id="327de-171">Therefore, you must make sure that all the required artifacts have been prepared.</span></span> <span data-ttu-id="327de-172">สำหรับคำแนะนำ โปรดดูกระบวนงาน [นำเข้าการตั้งค่าคอนฟิกการรายงานทางอิเล็กทรอนิกส์ (ER) จาก Regulatory Configuration Services (RCS)](https://docs.microsoft.com/en-us/dynamics365/unified-operations/dev-itpro/analytics/rcs-download-configurations)</span><span class="sxs-lookup"><span data-stu-id="327de-172">For instructions, see the [Import Electronic reporting (ER) configurations from Regulatory Configuration Services (RCS)](https://docs.microsoft.com/en-us/dynamics365/unified-operations/dev-itpro/analytics/rcs-download-configurations) procedure.</span></span>
3. <span data-ttu-id="327de-173">ทำตามขั้นตอนต่อไปนี้เพื่อนำเข้าการตั้งค่าคอนฟิกจาก RCS ไปยัง Finance and Operations:</span><span class="sxs-lookup"><span data-stu-id="327de-173">Follow these steps to import the configurations from RCS into Finance and Operations:</span></span>

    1. <span data-ttu-id="327de-174">ในพื้นที่ทำงาน **การรายงานทางอิเล็กทรอนิกส์** บนไทล์สำหรับผู้ให้บริการ การตั้งค่าคอนฟิก **Litware, Inc.** เลือก **ที่เก็บ**</span><span class="sxs-lookup"><span data-stu-id="327de-174">In the **Electronic reporting** workspace, on the tile for the **Litware, Inc.** configuration provider, select **Repositories**.</span></span>
    2. <span data-ttu-id="327de-175">บนหน้า **ที่เก็บการตั้งค่าคอนฟิก** เลือกที่เก็บของชนิด **RCS** และจากนั้นเลือก **เปิด**</span><span class="sxs-lookup"><span data-stu-id="327de-175">On the **Configuration repository** page, select the repository of the **RCS** type, and then select **Open**.</span></span>
    3. <span data-ttu-id="327de-176">บน FastTab **การตั้งค่าคอนฟิก** เลือกการตั้งค่าคอนฟิก **รูปแบบการติดตามประสิทธิภาพ**</span><span class="sxs-lookup"><span data-stu-id="327de-176">On the **Configurations** FastTab, select the **Performance trace format** configuration.</span></span>
    4. <span data-ttu-id="327de-177">บน FastTab **รุ่น** เลือกรุ่น **1.1** ของการตั้งค่าคอนฟิกที่เลือก และจากนั้น เลือก **นำเข้า**</span><span class="sxs-lookup"><span data-stu-id="327de-177">On the **Versions** FastTab, select version **1.1** of the selected configuration, and then select **Import**.</span></span>

    ![หน้าที่เก็บการตั้งค่าคอนฟิกใน Finance and Operations](./media/GER-PerfTrace-GER-ImportedConfigurations.png)

<span data-ttu-id="327de-179">รุ่นที่สอดคล้องกันของรูปแบบข้อมูลและการตั้งค่าคอนฟิกการแม็ปแบบจำลอง จะถูกนำเข้าโดยอัตโนมัติเป็นข้อกำหนดเบื้องต้นสำหรับการตั้งค่าคอนฟิกรูปแบบ ER ที่นำเข้า</span><span class="sxs-lookup"><span data-stu-id="327de-179">The corresponding versions of the data model and model mapping configurations are automatically imported as prerequisites for the imported ER format configuration.</span></span>

### <a name="turn-on-the-er-performance-trace"></a><span data-ttu-id="327de-180">เปิดการติดตามประสิทธิภาพ ER</span><span class="sxs-lookup"><span data-stu-id="327de-180">Turn on the ER performance trace</span></span>

1. <span data-ttu-id="327de-181">ใน Finance and Operations ไปที่ **การจัดการองค์กร \> การรายงานทางอิเล็กทรอนิกส์ \> การตั้งค่าคอนฟิก**</span><span class="sxs-lookup"><span data-stu-id="327de-181">In Finance and Operations, go to **Organization administration \> Electronic reporting \> Configurations**.</span></span>
2. <span data-ttu-id="327de-182">ในหน้า **การตั้งค่าคอนฟิก** บนบานหน้าต่างการดำเนินการ บนแท็บ **การตั้งค่าคอนฟิก** ในกลุ่ม **การตั้งค่าล่วงหน้า** เลือก **พารามิเตอร์ผู้ใช้**</span><span class="sxs-lookup"><span data-stu-id="327de-182">On the **Configurations** page, on the Action Pane, on the **Configurations** tab, in the **Advanced settings** group, select **User parameters**.</span></span>
3. <span data-ttu-id="327de-183">ในกล่องโต้ตอบ **พารามิเตอร์ผู้ใช้** ในส่วน **การติดตามการดำเนินการ** ให้ทำตามขั้นตอนเหล่านี้:</span><span class="sxs-lookup"><span data-stu-id="327de-183">In the **User parameters** dialog box, in the **Execution tracing** section, follow these steps:</span></span>

    1. <span data-ttu-id="327de-184">ในฟิลด์ **รูปแบบการติดตามการดำเนินการ** เลือก **ดีบักรูปแบบการติดตาม** เมื่อต้องการรวบรวมรายละเอียดของการดำเนินการรูปแบบ ER</span><span class="sxs-lookup"><span data-stu-id="327de-184">In the **Execution trace format** field, select **Debug trace format** to start to collect the details of ER format execution.</span></span> <span data-ttu-id="327de-185">เมื่อมีการเลือกค่านี้ การติดตามประสิทธิภาพจะเก็บรวบรวมข้อมูลเกี่ยวกับเวลาที่ใช้ในการดำเนินการต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="327de-185">When this value is selected, the performance trace will collect information about the time that is spent on the following actions:</span></span>

        - <span data-ttu-id="327de-186">การรันแหล่งข้อมูลแต่ละแหล่งในการแม็ปแบบจำลองถูกเรียกเพื่อดึงข้อมูล</span><span class="sxs-lookup"><span data-stu-id="327de-186">Running each data source in the model mapping that is called to get data</span></span>
        - <span data-ttu-id="327de-187">การประมวลผลรายการรูปแบบแต่ละรายการที่จะป้อนข้อมูลในเอาท์พุทที่ถูกสร้างขึ้น</span><span class="sxs-lookup"><span data-stu-id="327de-187">Processing each format item to enter data in the output that is generated</span></span>

        <span data-ttu-id="327de-188">คุณใช้ฟิลด์ **รูปแบบการติดตามการดำเนินการ** เพื่อระบุรูปแบบของการติดตามประสิทธิภาพที่สร้างขึ้น ซึ่งมีการจัดเก็บรายละเอียดการดำเนินการในรูปแบบ ER และองค์ประกอบของการแม็ป</span><span class="sxs-lookup"><span data-stu-id="327de-188">You use the **Execution trace format** field to specify the format of the generated performance trace that the execution details are stored in for ER format and mapping elements.</span></span> <span data-ttu-id="327de-189">โดยการเลือก **ดีบักรูปแบบการติดตาม** คุณจะสามารถวิเคราะห์เนื้อหาของการติดตามในตัวออกแบบการดำเนินงาน ER และดูรูปแบบ ER หรือองค์ประกอบของการแม็ปที่กล่าวถึงในการติดตาม</span><span class="sxs-lookup"><span data-stu-id="327de-189">By selecting **Debug trace format** as the value, you will be able to analyze the content of the trace in ER Operation designer, and see the ER format or mapping elements that are mentioned in the trace.</span></span>

    2. <span data-ttu-id="327de-190">ตั้งค่าตัวเลือกต่อไปนี้เป็น **ใช่** เพื่อรวบรวมรายละเอียดเฉพาะของการดำเนินการของการแม็ปแบบจำลอง ER และส่วนประกอบรูปแบบ ER:</span><span class="sxs-lookup"><span data-stu-id="327de-190">Set the following options to **Yes** to collect specific details of the execution of the ER model mapping and ER format components:</span></span>

        - <span data-ttu-id="327de-191">**รวบรวมสถิติการสอบถาม** – เมื่อเปิดตัวเลือกนี้ การติดตามประสิทธิภาพจะรวบรวมข้อมูลต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="327de-191">**Collect query statistics** – When this option is turned on, the performance trace will collect the following information:</span></span>

            - <span data-ttu-id="327de-192">จำนวนของการเรียกฐานข้อมูลที่ทำโดยแหล่งข้อมูล</span><span class="sxs-lookup"><span data-stu-id="327de-192">The number of database calls that were made by data sources</span></span>
            - <span data-ttu-id="327de-193">จำนวนครั้งของการเรียกการทำซ้ำไปยังฐานข้อมูล</span><span class="sxs-lookup"><span data-stu-id="327de-193">The number of duplicate calls to the database</span></span>
            - <span data-ttu-id="327de-194">รายละเอียดของคำสั่ง SQL ที่ใช้เพื่อทำการเรียกฐานข้อมูล</span><span class="sxs-lookup"><span data-stu-id="327de-194">Details of the SQL statements that were used to make database calls</span></span>

        - <span data-ttu-id="327de-195">**ติดตามการเข้าถึงการแคช** – เมื่อเปิดตัวเลือกนี้ การติดตามประสิทธิภาพจะรวบรวมข้อมูลเกี่ยวกับการใช้แคชของการแม็ปแบบจำลอง ER</span><span class="sxs-lookup"><span data-stu-id="327de-195">**Trace access of caching** – When this option is turned on, the performance trace will collect information about the ER model mapping's cache usage.</span></span>
        - <span data-ttu-id="327de-196">**ติดตามข้อมูลการเข้าถึง** – เมื่อเปิดตัวเลือกนี้ การติดตามประสิทธิภาพจะรวบรวมข้อมูลเกี่ยวกับจำนวนของการเรียกไปยังฐานข้อมูลสำหรับแหล่งข้อมูลที่ดำเนินการของชนิดรายการเรกคอร์ด</span><span class="sxs-lookup"><span data-stu-id="327de-196">**Trace data access** – When this option is turned on, the performance trace will collect information about the number of calls to the database for executed data sources of the record list type.</span></span>
        - <span data-ttu-id="327de-197">**การแจงนับรายการติดตาม** – เมื่อเปิดตัวเลือกนี้ การติดตามประสิทธิภาพจะรวบรวมข้อมูลเกี่ยวกับจำนวนของเรกคอร์ดที่ถูกร้องขอจากแหล่งข้อมูลของชนิดรายการเรกคอร์ด</span><span class="sxs-lookup"><span data-stu-id="327de-197">**Trace list enumeration** – When this option is turned on, the performance trace will collect information about the number of records that are requested from data sources of the record list type.</span></span>

    > [!NOTE]
    > <span data-ttu-id="327de-198">พารามิเตอร์ในกล่องโต้ตอบ **พารามิเตอร์ของผู้ใช้** ที่เฉพาะเจาะจงสำหรับผู้ใช้และบริษัทปัจจุบัน</span><span class="sxs-lookup"><span data-stu-id="327de-198">The parameters in the **User parameters** dialog box are specific to the user and the current company.</span></span>

    ![กล่องโต้ตอบพารามิเตอร์ของผู้ใช้ใน Finance and Operations](./media/GER-PerfTrace-GER-UserParameters.png)

### <a id='run-format'></a><span data-ttu-id="327de-200">รันรูปแบบ ER</span><span class="sxs-lookup"><span data-stu-id="327de-200">Run the ER format</span></span>

1. <span data-ttu-id="327de-201">ใน Finance and Operations เลือกบริษัท **DEMF**</span><span class="sxs-lookup"><span data-stu-id="327de-201">In Finance and Operations, select the **DEMF** company.</span></span>
2. <span data-ttu-id="327de-202">ไปที่ **การจัดการองค์กร \> การรายงานทางอิเล็กทรอนิกส์ \> การตั้งค่าคอนฟิก**</span><span class="sxs-lookup"><span data-stu-id="327de-202">Go to **Organization administration \> Electronic reporting \> Configurations**.</span></span>
3. <span data-ttu-id="327de-203">บนหน้า **การตั้งค่าคอนฟิก** ในแผนภูมิการตั้งค่าคอนฟิก เลือกรายการ **รูปแบบการติดตามประสิทธิภาพ**</span><span class="sxs-lookup"><span data-stu-id="327de-203">On the **Configurations** page, in the configuration tree, select the **Performance trace format** item.</span></span>
4. <span data-ttu-id="327de-204">บนบานหน้าต่างการดำเนินการ เลือก **รัน**</span><span class="sxs-lookup"><span data-stu-id="327de-204">On the Action Pane, select **Run**.</span></span>

<span data-ttu-id="327de-205">โปรดสังเกตว่าไฟล์ที่สร้างขึ้นแสดงข้อมูลเกี่ยวกับธุรกรรม 265 รายการสำหรับผู้จัดจำหน่ายหกราย</span><span class="sxs-lookup"><span data-stu-id="327de-205">Notice that the file that is generated presents information about 265 transactions for six vendors.</span></span>

## <a name="review-the-execution-trace"></a><span data-ttu-id="327de-206">ตรวจทานการติดตามการดำเนินการ</span><span class="sxs-lookup"><span data-stu-id="327de-206">Review the execution trace</span></span>

### <a id='export-trace'></a><span data-ttu-id="327de-207">ส่งออกการติดตามที่สร้างขึ้นจาก Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="327de-207">Export the generated trace from Finance and Operations</span></span>

<span data-ttu-id="327de-208">การติดตามประสิทธิภาพถูกแยกจากรูปแบบ ER ต้นทาง และสามารถทำให้เป็นแบบอนุกรมกับไฟล์ zip ภายนอก</span><span class="sxs-lookup"><span data-stu-id="327de-208">Performance traces are decoupled from the source ER format and can be serialized to an external zip file.</span></span>

1. <span data-ttu-id="327de-209">ใน Finance and Operations ไปที่ **การจัดการองค์กร \> การรายงานทางอิเล็กทรอนิกส์ \> บันทึกดีบักของการตั้งค่าคอนฟิก**</span><span class="sxs-lookup"><span data-stu-id="327de-209">In Finance and Operations, go to **Organization administration \> Electronic reporting \> Configuration debug logs**.</span></span>
2. <span data-ttu-id="327de-210">บนหน้า **บันทึกการรันการรายงานทางอิเล็กทรอนิกส์** ในบานหน้าต่างด้านซ้าย ในฟิลด์ **ชื่อการตั้งค่าคอนฟิก** เลือก **รูปแบบการติดตามประสิทธิภาพ** เพื่อค้นหาเรกคอร์ดล็อกที่สร้างขึ้นโดยการดำเนินการของการตั้งค่าคอนฟิก **รูปแบบการติดตามประสิทธิภาพ**</span><span class="sxs-lookup"><span data-stu-id="327de-210">On the **Electronic reporting run logs** page, in the left pane, in the **Configuration name** field, select **Performance trace format** to find the log records that have been generated by the execution of the **Performance trace format** configuration.</span></span>
3. <span data-ttu-id="327de-211">เลือกปุ่ม **เอกสารแนบ** (สัญลักษณ์คลิปหนีบกระดาษ) ในมุมขวาบนของหน้า หรือกด **Ctrl+Shift+A**</span><span class="sxs-lookup"><span data-stu-id="327de-211">Select the **Attachments** button (the paper clip symbol) in the upper-right corner of the page, or press **Ctrl+Shift+A**.</span></span>

    ![ปุ่มเอกสารแนบในหน้าบันทึกการรันการรายงานทางอิเล็กทรอนิกส์ใน Finance and Operations](./media/GER-PerfTrace-GER-DebugLog.png)

4. <span data-ttu-id="327de-213">บนหน้า **เอกสารแนบสำหรับบันทึกการรันการรายงานทางอิเล็กทรอนิกส์** ในบานหน้าต่างการดำเนินการ ให้เลือก **เปิด** เพื่อรับการติดตามประสิทธิภาพเป็นไฟล์ zip และจัดเก็บไว้ภายใน</span><span class="sxs-lookup"><span data-stu-id="327de-213">On the **Attachments for Electronic reporting run logs** page, on the Action Pane, select **Open** to get the performance trace as a zip file and store it locally.</span></span>

    ![เอกสารแนบสำหรับหน้าบันทึกการรันการรายงานทางอิเล็กทรอนิกส์ใน Finance and Operations](./media/GER-PerfTrace-GER-DebugLog-AttachedTrace.png)

> [!NOTE]
> <span data-ttu-id="327de-215">การติดตามที่สร้างขึ้นมีการอ้างอิงไปยังรายงาน ER ของแหล่งข้อมูลผ่านตัวระบุรายงานที่ไม่ซ้ำกันในรูปแบบ **GUID** เท่านั้น</span><span class="sxs-lookup"><span data-stu-id="327de-215">The trace that is generated has a reference to the source ER report via a unique report identifier in **GUID** format only.</span></span> <span data-ttu-id="327de-216">การกำหนดหมายเลขรุ่นของรูปแบบไม่ได้รับการพิจารณา</span><span class="sxs-lookup"><span data-stu-id="327de-216">The version numbering of the format isn't considered.</span></span>

<span data-ttu-id="327de-217">โปรดสังเกตว่าความสัมพันธ์ระหว่างการติดตามประสิทธิภาพที่ถูกสร้างขึ้นสำหรับรูปแบบ ER ที่ดำเนินการ และการแม็ปแบบจำลอง ER จะขึ้นอยู่กับตัวอธิบายรากที่ใช้และแบบจำลองข้อมูลทั่วไป</span><span class="sxs-lookup"><span data-stu-id="327de-217">Notice that the association between the performance trace that has been generated for the executed ER format and the ER model mapping is based on the root descriptor that was used and the common data model.</span></span> <span data-ttu-id="327de-218">การกำหนดหมายเลขรุ่นของรูปแบบและการแม็ปแบบจำลองไม่ได้รับการพิจารณา</span><span class="sxs-lookup"><span data-stu-id="327de-218">The version numbering of the format and model mapping isn't considered.</span></span> <span data-ttu-id="327de-219">นอกจากนี้ จะไม่มีการพิจารณาการตั้งค่าของแฟล็ก **ค่าเริ่มต้นสำหรับการแม็ปแบบจำลอง** สำหรับการแม็ปแบบจำลอง</span><span class="sxs-lookup"><span data-stu-id="327de-219">The setting of the **Default for model mapping** flag for the model mapping also isn't considered.</span></span>

### <a id='import-trace'></a><span data-ttu-id="327de-220">นำเข้าการติดตามที่สร้างลงใน RCS</span><span class="sxs-lookup"><span data-stu-id="327de-220">Import the generated trace into RCS</span></span>

1. <span data-ttu-id="327de-221">ใน RCS พื้นที่ทำงาน **การรายงานทางอิเล็กทรอนิกส์** เลือกไทล์ **การตั้งค่าคอนฟิกการรายงาน**</span><span class="sxs-lookup"><span data-stu-id="327de-221">In RCS, in the **Electronic reporting** workspace, select the **Reporting configurations** tile.</span></span>
2. <span data-ttu-id="327de-222">ในหน้า **การตั้งค่าคอนฟิก** ในแผนภูมิการตั้งค่าคอนฟิก ให้ขยายรายการ **แบบจำลองการติดตามประสิทธิภาพ** และเลือกรายการ **รูปแบบการติดตามประสิทธิภาพ**</span><span class="sxs-lookup"><span data-stu-id="327de-222">On the **Configurations** page, in the configuration tree, expand the **Performance trace model** item, and select the **Performance trace format** item.</span></span>
3. <span data-ttu-id="327de-223">บนบานหน้าต่างการดำเนินการ เลือก **ตัวออกแบบ**</span><span class="sxs-lookup"><span data-stu-id="327de-223">On the Action Pane, select **Designer**.</span></span>
4. <span data-ttu-id="327de-224">บนหน้า **ตัวออกแบบรูปแบบ** บนบานหน้าต่างการดำเนินการ ให้เลือก **การติดตามประสิทธิภาพ**</span><span class="sxs-lookup"><span data-stu-id="327de-224">On the **Format designer** page, on the Action Pane, select **Performance trace**.</span></span>
5. <span data-ttu-id="327de-225">ในกล่องโต้ตอบ **การตั้งค่าผลการติดตามประสิทธิภาพ** ให้เลือก **นำเข้าการติดตามประสิทธิภาพ**</span><span class="sxs-lookup"><span data-stu-id="327de-225">In the **Performance trace result settings** dialog box, select **Import performance trace**.</span></span>
6. <span data-ttu-id="327de-226">เลือก **เรียกดู** เพื่อเลือกไฟล์ zip ที่คุณส่งออกจาก Finance and Operations ก่อนหน้านี้</span><span class="sxs-lookup"><span data-stu-id="327de-226">Select **Browse** to select the zip file that you exported from Finance and Operations earlier.</span></span>
7. <span data-ttu-id="327de-227">เลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="327de-227">Select **OK**.</span></span>

    ![กล่องโต้ตอบการตั้งค่าผลการติดตามประสิทธิภาพใน RCS](./media/GER-PerfTrace-RCS-ImportedPerfTrace.png)

### <a name="use-the-performance-trace-for-analysis-in-rcs--format-execution"></a><span data-ttu-id="327de-229">ใช้การติดตามประสิทธิภาพสำหรับการวิเคราะห์ใน RCS – การดำเนินการรูปแบบ</span><span class="sxs-lookup"><span data-stu-id="327de-229">Use the performance trace for analysis in RCS – Format execution</span></span>

1. <span data-ttu-id="327de-230">ใน RCS บนหน้า **ตัวออกแบบรูปแบบ** ให้เลือก **ขยาย/ยุบ** เพื่อขยายเนื้อหาของรายการรูปแบบทั้งหมด</span><span class="sxs-lookup"><span data-stu-id="327de-230">In RCS, on the **Format designer** page, select **Expand/collapse** to expand the content of all format items.</span></span>

    <span data-ttu-id="327de-231">โปรดสังเกตว่ามีการแสดงข้อมูลเพิ่มเติมสำหรับบางรายการของรูปแบบปัจจุบัน:</span><span class="sxs-lookup"><span data-stu-id="327de-231">Notice that additional information is shown for some items of the current format:</span></span>

    - <span data-ttu-id="327de-232">เวลาจริงที่ใช้ในการป้อนข้อมูลในเอาท์พุทที่สร้างขึ้นโดยใช้รายการรูปแบบ</span><span class="sxs-lookup"><span data-stu-id="327de-232">The actual time that was spent entering data in the generated output by using the format item</span></span>
    - <span data-ttu-id="327de-233">เวลาเดียวกันที่แสดงเป็นเปอร์เซ็นต์ของเวลาทั้งหมดที่ใช้ในการสร้างเอาท์พุททั้งหมด</span><span class="sxs-lookup"><span data-stu-id="327de-233">The same time expressed as a percentage of the total time that was spent generating the whole output</span></span>

    ![หน้าตัวออกแบบรูปแบบใน RCS](./media/GER-PerfTrace-RCS-TraceInfoInFormat.png)

2. <span data-ttu-id="327de-235">ปิดหน้า **ตัวออกแบบรูปแบบ**</span><span class="sxs-lookup"><span data-stu-id="327de-235">Close **Format designer** page.</span></span>

### <a id='use-trace'></a><span data-ttu-id="327de-236">ใช้การติดตามประสิทธิภาพสำหรับการวิเคราะห์ใน RCS – การแม็ปรูปแบบ</span><span class="sxs-lookup"><span data-stu-id="327de-236">Use the performance trace for analysis in RCS – Model mapping</span></span>

1. <span data-ttu-id="327de-237">ใน RCS บนหน้า **การตั้งค่าคอนฟิก** ในแผนภูมิการตั้งค่าคอนฟิก ให้เลือกรายการ **การแม็ปการติดตามประสิทธิภาพ**</span><span class="sxs-lookup"><span data-stu-id="327de-237">In RCS, on the **Configurations** page, in the configuration tree, select the **Performance trace mapping** item.</span></span>
2. <span data-ttu-id="327de-238">บนบานหน้าต่างการดำเนินการ เลือก **ตัวออกแบบ**</span><span class="sxs-lookup"><span data-stu-id="327de-238">On the Action Pane, select **Designer**.</span></span>
3. <span data-ttu-id="327de-239">เลือก **ตัวออกแบบ**</span><span class="sxs-lookup"><span data-stu-id="327de-239">Select **Designer**.</span></span>
4. <span data-ttu-id="327de-240">บนหน้า **ตัวออกแบบการแม็ปแบบจำลอง** บนบานหน้าต่างการดำเนินการ ให้เลือก **การติดตามประสิทธิภาพ**</span><span class="sxs-lookup"><span data-stu-id="327de-240">On the **Model mapping designer** page, on the Action Pane, select **Performance trace**.</span></span>
5. <span data-ttu-id="327de-241">เลือกการติดตามที่คุณนำเข้าก่อนหน้านี้</span><span class="sxs-lookup"><span data-stu-id="327de-241">Select the trace that you imported earlier.</span></span>
6. <span data-ttu-id="327de-242">เลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="327de-242">Select **OK**.</span></span>

<span data-ttu-id="327de-243">โปรดสังเกตว่าข้อมูลใหม่จะกลายเป็นพร้อมใช้งานสำหรับรายการแหล่งข้อมูลบางอย่างของการแม็ปแบบจำลองปัจจุบัน:</span><span class="sxs-lookup"><span data-stu-id="327de-243">Notice that new information becomes available for some data source items of the current model mapping:</span></span>

- <span data-ttu-id="327de-244">เวลาจริงที่ใช้ในการเรียกข้อมูลโดยใช้แหล่งข้อมูล</span><span class="sxs-lookup"><span data-stu-id="327de-244">The actual time that was spent getting data by using the data source</span></span>
- <span data-ttu-id="327de-245">เวลาเดียวกันที่แสดงเป็นเปอร์เซ็นต์ของเวลาทั้งหมดที่ใช้ในการรันการแม็ปแบบจำลองทั้งหมด</span><span class="sxs-lookup"><span data-stu-id="327de-245">The same time expressed as a percentage of the total time that was spent running the whole model mapping</span></span>

<span data-ttu-id="327de-246">โปรดสังเกตว่า ER แจ้งให้คุณทราบว่าการแม็ปแบบจำลองปัจจุบันจะทำซ้ำคำขอฐานข้อมูล ในขณะที่แหล่งข้อมูล VendTable/\<Relations/VendTrans.VendTable\_AccountNum ถูกรัน</span><span class="sxs-lookup"><span data-stu-id="327de-246">Notice that ER informs you that the current model mapping duplicates database requests while the VendTable/\<Relations/VendTrans.VendTable\_AccountNum data source is run.</span></span> <span data-ttu-id="327de-247">การทำซ้ำนี้เกิดขึ้นเนื่องจากรายการของธุรกรรมผู้จัดจำหน่ายถูกเรียกสองครั้งสำหรับเรกคอร์ดผู้จัดจำหน่ายที่ทำซ้ำแต่ละรายการ:</span><span class="sxs-lookup"><span data-stu-id="327de-247">This duplication occurs because the list of vendor transactions is called two times for each iterated vendor record:</span></span>

- <span data-ttu-id="327de-248">มีการเรียกหนึ่งครั้งเพื่อป้อนรายละเอียดของแต่ละธุรกรรมในแบบจำลองข้อมูล ซึ่งขึ้นกับการผูกข้อมูลที่ตั้งค่าคอนฟิก</span><span class="sxs-lookup"><span data-stu-id="327de-248">One call is made to enter details of each transaction in the data model, based on configured bindings.</span></span>
- <span data-ttu-id="327de-249">มีการทำการเรียกหนึ่งครั้งเพื่อป้อนจำนวนของธุรกรรมที่คำนวณได้สำหรับผู้จัดจำหน่ายแต่ละรายในแบบจำลองข้อมูล</span><span class="sxs-lookup"><span data-stu-id="327de-249">One call is made to enter the calculated number of transactions per vendor in the data model.</span></span>

![ข้อความเกี่ยวกับการร้องขอฐานข้อมูลที่ซ้ำกันบนหน้าตัวออกแบบการแม็ปแบบจำลองใน RCS](./media/GER-PerfTrace-RCS-TraceInfoInMapping1.png)

<span data-ttu-id="327de-251">ค่า **\[Q:530\]** บ่งชี้ว่าตาราง VendTrans ถูกเรียก 530 ครั้งเพื่อส่งคืนเรกคอร์ดจากตารางนั้นไปยังแหล่งข้อมูล VendTable/\<Relations/VendTrans.VendTable\_AccountNum</span><span class="sxs-lookup"><span data-stu-id="327de-251">The value **\[Q:530\]** indicates that the VendTrans table was called 530 times to return a record from that table to the VendTable/\<Relations/VendTrans.VendTable\_AccountNum data source.</span></span> <span data-ttu-id="327de-252">ค่า **\[530\]** บ่งชี้ว่ามีการเรียกแหล่งข้อมูล VendTable/\<Relations/VendTrans.VendTable\_AccountNum ถูกเรียก 530 ครั้ง เพื่อส่งคืนเรกคอร์ดจากแหล่งข้อมูลนั้นและป้อนรายละเอียดจากรายการนั้นในแบบจำลองข้อมูล</span><span class="sxs-lookup"><span data-stu-id="327de-252">The value **\[530\]** indicates that the VendTable/\<Relations/VendTrans.VendTable\_AccountNum data source was called 530 times to return a record from that data source and enter the details from it in the data model.</span></span>

<span data-ttu-id="327de-253">เราขอแนะนำให้คุณใช้การแคชสำหรับแหล่งข้อมูล VendTable/\<Relations/VendTrans.VendTable\_AccountNum เพื่อลดจำนวนของการเรียกที่ถูกทำเพื่อดูรายละเอียดสำหรับธุรกรรม 265 รายการ และช่วยปรับปรุงประสิทธิภาพการทำงานของการแม็ปแบบจำลอง</span><span class="sxs-lookup"><span data-stu-id="327de-253">We recommend that you use caching for the VendTable/\<Relations/VendTrans.VendTable\_AccountNum data source, to reduce the number of calls that are made to get the details for 265 transactions and help improve the performance of the model mapping.</span></span>

<span data-ttu-id="327de-254">นอกจากนี้ ยังอาจเป็นประโยชน์ในการลดจำนวนการเรียกที่ทำไปยังแหล่งข้อมูล LedgerTransTypeList</span><span class="sxs-lookup"><span data-stu-id="327de-254">It can also be useful to reduce the number of calls that are made to the LedgerTransTypeList data source.</span></span> <span data-ttu-id="327de-255">แหล่งข้อมูลนี้ใช้ในการเชื่อมโยงค่าแต่ละค่าของการแจงนับ **LedgerTransType** กับป้ายชื่อ</span><span class="sxs-lookup"><span data-stu-id="327de-255">This data source is used to associate each value of the **LedgerTransType** enumeration with its label.</span></span> <span data-ttu-id="327de-256">โดยใช้แหล่งข้อมูลนี้ คุณสามารถค้นหาป้ายชื่อที่เหมาะสม และป้อนในรูปแบบข้อมูลสำหรับธุรกรรมผู้จัดจำหน่ายแต่ละราย</span><span class="sxs-lookup"><span data-stu-id="327de-256">By using this data source, you can find an appropriate label and enter it in the data model for each vendor transaction.</span></span> <span data-ttu-id="327de-257">จำนวนครั้งปัจจุบันของการเรียกไปยังแหล่งข้อมูลนี้ (9,027) ค่อนข้างสูงสำหรับธุรกรรม 265 รายการ</span><span class="sxs-lookup"><span data-stu-id="327de-257">The current number of calls to this data source (9,027) is quite high for 265 transactions.</span></span>

![หน้าตัวออกแบบการแม็ปแบบจำลองใน RCS ซึ่งแสดงการเรียก 9,027 รายการไปยังแหล่งข้อมูล](./media/GER-PerfTrace-RCS-TraceInfoInMapping1a.png)

## <a name="improve-the-model-mapping-based-on-information-from-the-execution-trace"></a><span data-ttu-id="327de-259">ปรับปรุงการแม็ปแบบจำลองตามข้อมูลจากการติดตามการดำเนินการ</span><span class="sxs-lookup"><span data-stu-id="327de-259">Improve the model mapping based on information from the execution trace</span></span>

### <a name="modify-the-logic-of-the-model-mapping"></a><span data-ttu-id="327de-260">ปรับเปลี่ยนตรรกะของการแม็ปแบบจำลอง</span><span class="sxs-lookup"><span data-stu-id="327de-260">Modify the logic of the model mapping</span></span>

1. <span data-ttu-id="327de-261">ทำตามขั้นตอนต่อไปนี้เพื่อใช้การแม็ปการติดตามประสิทธิภาพ เพื่อช่วยป้องกันการเรียกซ้ำไปยังฐานข้อมูล:</span><span class="sxs-lookup"><span data-stu-id="327de-261">Follow these steps to use caching, to help prevent duplicate calls to the database:</span></span>

    1. <span data-ttu-id="327de-262">ใน RCS บนหน้า **ตัวออกแบบการแม็ปแบบจำลอง** ในบานหน้าต่าง **แหล่งข้อมูล** ให้เลือกรายการ **VendTable**</span><span class="sxs-lookup"><span data-stu-id="327de-262">In RCS, on the **Model mapping designer** page, in the **Data sources** pane, select the **VendTable** item.</span></span>
    2. <span data-ttu-id="327de-263">เลือก **แคช**</span><span class="sxs-lookup"><span data-stu-id="327de-263">Select **Cache**.</span></span>
    3. <span data-ttu-id="327de-264">ขยายรายการ **VendTable** ขยายรายการของความสัมพันธ์แบบหนึ่งต่อกลุ่มสำหรับแหล่งข้อมูล VendTable (รายการ **\<ความสัมพันธ์**) และเลือกรายการ **VendTrans.VendTable\_AccountNum**</span><span class="sxs-lookup"><span data-stu-id="327de-264">Expand the **VendTable** item, expand the list of one-to-many relations for the VendTable data source (the **\<Relations** item), and select the **VendTrans.VendTable\_AccountNum** item.</span></span>
    4. <span data-ttu-id="327de-265">เลือก **แคช**</span><span class="sxs-lookup"><span data-stu-id="327de-265">Select **Cache**.</span></span>

    ![การแคชการตั้งค่าเพื่อช่วยป้องกันการเรียกซ้ำ](./media/GER-PerfTrace-RCS-ChangeMapping-Cache.png)

2. <span data-ttu-id="327de-267">ทำตามขั้นตอนต่อไปนี้เพื่อนำแหล่งข้อมูล LedgerTransTypeList เข้าไปในขอบเขตของแหล่งข้อมูล VendTable:</span><span class="sxs-lookup"><span data-stu-id="327de-267">Follow these steps to bring the LedgerTransTypeList data source into the scope of the VendTable data source:</span></span>

    1. <span data-ttu-id="327de-268">ในบานหน้าต่าง **ชนิดแหล่งข้อมูล** ให้ขยายรายการ **ฟังก์ชัน** และเลือกรายการ **ฟิลด์ที่คำนวณได้**</span><span class="sxs-lookup"><span data-stu-id="327de-268">In the **Data source types** pane, expand the **Functions** item, and select the **Calculated field** item.</span></span>
    2. <span data-ttu-id="327de-269">ในบานหน้าต่าง **แหล่งข้อมูล** ให้เลือกรายการ **VendTable**</span><span class="sxs-lookup"><span data-stu-id="327de-269">In the **Data sources** pane, select the **VendTable** item.</span></span>
    3. <span data-ttu-id="327de-270">เลือก **เพิ่ม**</span><span class="sxs-lookup"><span data-stu-id="327de-270">Select **Add**.</span></span>
    4. <span data-ttu-id="327de-271">ในฟิลด์ **ชื่อ** ให้ป้อน **\$TransType**</span><span class="sxs-lookup"><span data-stu-id="327de-271">In the **Name** field, enter **\$TransType**.</span></span>
    5. <span data-ttu-id="327de-272">เลือก **แก้ไขสูตร**</span><span class="sxs-lookup"><span data-stu-id="327de-272">Select **Edit formula**.</span></span>
    6. <span data-ttu-id="327de-273">ในฟิลด์ **สูตร** ให้ป้อน **LedgerTransTypeList**</span><span class="sxs-lookup"><span data-stu-id="327de-273">In the **Formula** field, enter **LedgerTransTypeList**.</span></span>
    7. <span data-ttu-id="327de-274">เลือก **บันทึก**</span><span class="sxs-lookup"><span data-stu-id="327de-274">Select **Save**.</span></span>
    8. <span data-ttu-id="327de-275">ปิดหน้า **ตัวแก้ไขสูตร**</span><span class="sxs-lookup"><span data-stu-id="327de-275">Close the **Formula editor** page.</span></span>
    9. <span data-ttu-id="327de-276">คลิก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="327de-276">Click **OK**.</span></span>

3. <span data-ttu-id="327de-277">ทำตามขั้นตอนต่อไปนี้เพื่อทำการแคชของฟิลด์ **\$TransType**:</span><span class="sxs-lookup"><span data-stu-id="327de-277">Follow these steps to do caching of the **\$TransType** field:</span></span>

    1. <span data-ttu-id="327de-278">เลือกรายการ **LedgerTransTypeList**</span><span class="sxs-lookup"><span data-stu-id="327de-278">Select the **LedgerTransTypeList** item.</span></span>
    2. <span data-ttu-id="327de-279">เลือก **แคช**</span><span class="sxs-lookup"><span data-stu-id="327de-279">Select **Cache**.</span></span>
    3. <span data-ttu-id="327de-280">เลือกรายการ **VendTable.\$TransType**</span><span class="sxs-lookup"><span data-stu-id="327de-280">Select the **VendTable.\$TransType** item.</span></span>
    4. <span data-ttu-id="327de-281">เลือก **แคช**</span><span class="sxs-lookup"><span data-stu-id="327de-281">Select **Cache**.</span></span>

    ![การแคชการตั้งค่าสำหรับฟิลด์ $TransType](./media/GER-PerfTrace-RCS-ChangeMapping-Cache2.png)

4. <span data-ttu-id="327de-283">ทำตามขั้นตอนเหล่านี้เพื่อเปลี่ยนแปลงฟิลด์ **\$TransTypeRecord** เพื่อให้เริ่มต้นการใช้ฟิลด์ **\$TransType** ที่แคช:</span><span class="sxs-lookup"><span data-stu-id="327de-283">Follow these steps to change the **\$TransTypeRecord** field so that it starts to use the cached **\$TransType** field:</span></span>

    1. <span data-ttu-id="327de-284">ในบานหน้าต่าง **แหล่งข้อมูล** ให้ขยายรายการ **VendTable** ขยายรายการ **\<ความสัมพันธ์** ขยายรายการ **VendTrans.VendTable\_AccountNum** และเลือกรายการ **VendTable. VendTrans.VendTable\_AccountNum.\$TransTypeRecord**</span><span class="sxs-lookup"><span data-stu-id="327de-284">In the **Data sources** pane, expand the **VendTable** item, expand the **\<Relations** item, expand the **VendTrans.VendTable\_AccountNum** item, and select the **VendTable. VendTrans.VendTable\_AccountNum.\$TransTypeRecord** item.</span></span>
    2. <span data-ttu-id="327de-285">เลือก **แก้ไข**</span><span class="sxs-lookup"><span data-stu-id="327de-285">Select **Edit**.</span></span>
    3. <span data-ttu-id="327de-286">เลือก **แก้ไขสูตร**</span><span class="sxs-lookup"><span data-stu-id="327de-286">Select **Edit formula**.</span></span>
    4. <span data-ttu-id="327de-287">ในฟิลด์ **สูตร** ให้ค้นหานิพจน์ต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="327de-287">In the **Formula** field, find the following expression:</span></span>

        <span data-ttu-id="327de-288">FIRSTORNULL (WHERE (LedgerTransTypeList, LedgerTransTypeList.Enum = \@.TransType))</span><span class="sxs-lookup"><span data-stu-id="327de-288">FIRSTORNULL (WHERE (LedgerTransTypeList, LedgerTransTypeList.Enum = \@.TransType))</span></span>

    5. <span data-ttu-id="327de-289">ในฟิลด์ **สูตร** ให้ป้อนนิพจน์ต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="327de-289">In the **Formula** field, enter the following expression:</span></span>

        <span data-ttu-id="327de-290">FIRSTORNULL (WHERE (VendTable.'\$TransType', VendTable.'\$TransType'.Enum = \@.TransType))</span><span class="sxs-lookup"><span data-stu-id="327de-290">FIRSTORNULL (WHERE (VendTable.'\$TransType', VendTable.'\$TransType'.Enum = \@.TransType)).</span></span>

    6. <span data-ttu-id="327de-291">เลือก **บันทึก**</span><span class="sxs-lookup"><span data-stu-id="327de-291">Select **Save**.</span></span>
    7. <span data-ttu-id="327de-292">ปิดหน้า **ตัวแก้ไขสูตร**</span><span class="sxs-lookup"><span data-stu-id="327de-292">Close the **Formula editor** page.</span></span>
    8. <span data-ttu-id="327de-293">เลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="327de-293">Select **OK**.</span></span>

5. <span data-ttu-id="327de-294">เลือก **บันทึก**</span><span class="sxs-lookup"><span data-stu-id="327de-294">Select **Save**.</span></span>
6. <span data-ttu-id="327de-295">ปิดหน้า **ตัวออกแบบการแม็ปแบบจำลอง**</span><span class="sxs-lookup"><span data-stu-id="327de-295">Close the **Model mapping designer** page.</span></span>
7. <span data-ttu-id="327de-296">ปิดหน้า **การแม็ปแบบจำลอง**</span><span class="sxs-lookup"><span data-stu-id="327de-296">Close the **Model mappings** page.</span></span>

### <a name="complete-the-modified-version-of-the-er-model-mapping"></a><span data-ttu-id="327de-297">ดำเนินการรุ่นที่แก้ไขของการแม็ปแบบจำลอง ER ให้เสร็จสมบูรณ์</span><span class="sxs-lookup"><span data-stu-id="327de-297">Complete the modified version of the ER model mapping</span></span>

1. <span data-ttu-id="327de-298">ใน RCS บนหน้า **การตั้งค่าคอนฟิก** บน FastTab **รุ่น** ให้เลือกรุ่น **1.2** ของการตั้งค่าคอนฟิก **การแม็ปการติดตามประสิทธิภาพ**</span><span class="sxs-lookup"><span data-stu-id="327de-298">In RCS, on the **Configurations** page, on the **Versions** FastTab, select version **1.2** of the **Performance trace mapping** configuration.</span></span>
2. <span data-ttu-id="327de-299">เลือก **เปลี่ยนแปลงสถานะ**</span><span class="sxs-lookup"><span data-stu-id="327de-299">Select **Change status**.</span></span>
3. <span data-ttu-id="327de-300">เลือก **เสร็จสมบูรณ์**</span><span class="sxs-lookup"><span data-stu-id="327de-300">Select **Complete**.</span></span>

### <a name="import-the-modified-er-model-mapping-configuration-from-rcs-into-finance-and-operations"></a><span data-ttu-id="327de-301">นำเข้าการตั้งค่าคอนฟิกการแม็ปแบบจำลอง ER ที่แก้ไขจาก RCS ไปยัง Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="327de-301">Import the modified ER model mapping configuration from RCS into Finance and Operations</span></span>

<span data-ttu-id="327de-302">ทำซ้ำขั้นตอนในส่วน [นำเข้าการตั้งค่าคอนฟิก ER จาก RCS ไปยัง Finance and Operations](#import-configuration) ก่อนหน้านี้ในหัวข้อนี้ เพื่อนำเข้ารุ่น 1.2 ของการตั้งค่าคอนฟิก **การแม็ปการติดตามประสิทธิภาพ** ไปยัง Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="327de-302">Repeat the steps in the [Import an ER configuration from RCS into Finance and Operations](#import-configuration) section earlier in this topic to import version 1.2 of the **Performance trace mapping** configuration into Finance and Operations.</span></span>

## <a name="run-the-modified-er-solution-to-trace-execution"></a><span data-ttu-id="327de-303">รันโซลูชัน ER ที่แก้ไขเพื่อติดตามการดำเนินการ</span><span class="sxs-lookup"><span data-stu-id="327de-303">Run the modified ER solution to trace execution</span></span>

### <a name="run-the-er-format"></a><span data-ttu-id="327de-304">รันรูปแบบ ER</span><span class="sxs-lookup"><span data-stu-id="327de-304">Run the ER format</span></span>

<span data-ttu-id="327de-305">ทำซ้ำขั้นตอนในส่วน [รันรูปแบบ ER](#run-format) ก่อนหน้าในหัวข้อนี้ เพื่อสร้างการติดตามประสิทธิภาพใหม่</span><span class="sxs-lookup"><span data-stu-id="327de-305">Repeat the steps in the [Run the ER format](#run-format) section earlier in this topic to generate a new performance trace.</span></span>

## <a name="review-the-execution-trace"></a><span data-ttu-id="327de-306">ตรวจทานการติดตามการดำเนินการ</span><span class="sxs-lookup"><span data-stu-id="327de-306">Review the execution trace</span></span>

### <a name="export-the-generated-trace-from-finance-and-operations"></a><span data-ttu-id="327de-307">ส่งออกการติดตามที่สร้างขึ้นจาก Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="327de-307">Export the generated trace from Finance and Operations</span></span>

<span data-ttu-id="327de-308">ทำซ้ำขั้นตอนในส่วน [ส่งออกการติดตามที่สร้างขึ้นจาก Finance and Operations](#export-trace) ก่อนหน้านี้ในหัวข้อนี้ เพื่อบันทึกการติดตามประสิทธิภาพใหม่ภายในเครื่อง</span><span class="sxs-lookup"><span data-stu-id="327de-308">Repeat the steps in the [Export the generated trace from Finance and Operations](#export-trace) section earlier in this topic to save a new performance trace locally.</span></span>

### <a name="import-the-generated-trace-into-rcs"></a><span data-ttu-id="327de-309">นำเข้าการติดตามที่สร้างลงใน RCS</span><span class="sxs-lookup"><span data-stu-id="327de-309">Import the generated trace into RCS</span></span>

<span data-ttu-id="327de-310">ทำซ้ำขั้นตอนในส่วน [นำเข้าการติดตามที่สร้างขึ้นใน RCS](#import-trace) ก่อนหน้าในหัวข้อนี้ เพื่อนำเข้าการติดตามประสิทธิภาพใหม่ไปยัง RCS</span><span class="sxs-lookup"><span data-stu-id="327de-310">Repeat the steps in the [Import the generated trace into RCS](#import-trace) section earlier in this topic to import the new performance trace into RCS.</span></span>

### <a name="use-the-performance-trace-for-analysis-in-rcs--model-mapping"></a><span data-ttu-id="327de-311">ใช้การติดตามประสิทธิภาพสำหรับการวิเคราะห์ใน RCS – การแม็ปรูปแบบ</span><span class="sxs-lookup"><span data-stu-id="327de-311">Use the performance trace for analysis in RCS – Model mapping</span></span>

<span data-ttu-id="327de-312">ทำซ้ำขั้นตอนในส่วน [ใช้การติดตามประสิทธิภาพสำหรับการวิเคราะห์ใน RCS – การแม็ปแบบจำลอง](#use-trace) ก่อนหน้านี้ในหัวข้อนี้ เพื่อวิเคราะห์การติดตามประสิทธิภาพล่าสุด</span><span class="sxs-lookup"><span data-stu-id="327de-312">Repeat the steps in the [Use the performance trace for analysis in RCS – Model mapping](#use-trace) section earlier in this topic to analyze the latest performance trace.</span></span>

<span data-ttu-id="327de-313">โปรดสังเกตว่าการปรับปรุงที่คุณทำไปยังการแม็ปแบบจำลอง มีการตัดการสอบถามที่ซ้ำกันไปยังฐานข้อมูล</span><span class="sxs-lookup"><span data-stu-id="327de-313">Notice that the adjustments that you made to the model mapping have eliminated duplicate queries to database.</span></span> <span data-ttu-id="327de-314">นอกจากนี้ ยังมีการลดจำนวนของการเรียกไปยังตารางฐานข้อมูลและแหล่งข้อมูลสำหรับการแม็ปแบบจำลองนี้ด้วย</span><span class="sxs-lookup"><span data-stu-id="327de-314">The number of calls to database tables and data sources for this model mapping has been also reduced.</span></span> <span data-ttu-id="327de-315">ดังนั้น ประสิทธิภาพการทำงานของโซลูชัน ER ทั้งหมดได้รับการปรับปรุง</span><span class="sxs-lookup"><span data-stu-id="327de-315">Therefore, the performance of the whole ER solution has improved.</span></span>

![ข้อมูลการติดตามสำหรับแหล่งข้อมูล VendTable ในหน้าตัวออกแบบการแม็ปแบบจำลองใน RCS](./media/GER-PerfTrace-RCS-TraceInfoInMapping2.png)

<span data-ttu-id="327de-317">ในข้อมูลการติดตาม ค่า **\[12\]** สำหรับแหล่งข้อมูล VendTable บ่งชี้ว่าแหล่งข้อมูลนี้ถูกเรียก 12 ครั้ง</span><span class="sxs-lookup"><span data-stu-id="327de-317">In the trace information, the value **\[12\]** for the VendTable data source indicates that this data source was called 12 times.</span></span> <span data-ttu-id="327de-318">ค่า **\[Q:6\]** บ่งชี้ว่ามีการแปลการเรียก 6 ครั้งเป็นการเรียกฐานข้อมูลไปยังตาราง VendTable</span><span class="sxs-lookup"><span data-stu-id="327de-318">The value **\[Q:6\]** indicates that six calls were translated to database calls to the VendTable table.</span></span> <span data-ttu-id="327de-319">ค่า **\[C:6\]** บ่งชี้ว่าเรกคอร์ดที่นำมาใช้จากฐานข้อมูลถูกแคช และมีการประมวลผลการเรียกอีกหกครั้งโดยใช้แคช</span><span class="sxs-lookup"><span data-stu-id="327de-319">The value **\[C:6\]** indicates that the records that were fetched from the database were cached, and six other calls were processed by using the cache.</span></span>

<span data-ttu-id="327de-320">โปรดสังเกตว่ามีการลดจำนวนการเรียกไปยังแหล่งข้อมูล LedgerTransTypeList จาก 9,027 เป็น 240</span><span class="sxs-lookup"><span data-stu-id="327de-320">Notice that the number of calls to the LedgerTransTypeList data source has been reduced from 9,027 to 240.</span></span>

![ข้อมูลการติดตามสำหรับแหล่งข้อมูล LedgerTransTypeList ในหน้าตัวออกแบบการแม็ปแบบจำลองใน RCS](./media/GER-PerfTrace-RCS-TraceInfoInMapping2a.png)

## <a name="review-the-execution-trace-in-finance-and-operations"></a><span data-ttu-id="327de-322">ตรวจทานการติดตามการดำเนินการใน Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="327de-322">Review the execution trace in Finance and Operations</span></span>

<span data-ttu-id="327de-323">นอกจาก RCS รุ่นบางรุ่นของ Finance and Operations อาจมีความสามารถสำหรับประสบการณ์นักออกแบบกรอบงาน ER</span><span class="sxs-lookup"><span data-stu-id="327de-323">In addition to RCS, some versions of Finance and Operations might offer capabilities for an ER framework designer experience.</span></span> <span data-ttu-id="327de-324">รุ่นของ Finance and Operations มีตัวเลือก **เปิดใช้งานโหมดการออกแบบ** ที่สามารถเปิดได้</span><span class="sxs-lookup"><span data-stu-id="327de-324">These versions of Finance and Operations have an **Enable design mode** option that can be turned on.</span></span> <span data-ttu-id="327de-325">คุณสามารถค้นหาตัวเลือกนี้บนแท็บ **ทั่วไป** ของหน้า **พารามิเตอร์การรายงานทางอิเล็กทรอนิกส์** ซึ่งคุณสามารถเปิดได้จากพื้นที่ทำงาน **การรายงานทางอิเล็กทรอนิกส์**</span><span class="sxs-lookup"><span data-stu-id="327de-325">You can find this option on the **General** tab of the **Electronic reporting parameters** page, which you can open from the **Electronic reporting** workspace.</span></span>

![เปิดใช้งานตัวเลือกโหมดการออกแบบในหน้าพารามิเตอร์การรายงานทางอิเล็กทรอนิกส์ใน Finance and Operations](./media/GER-PerfTrace-GER-Parameters-DesignMode.png)

<span data-ttu-id="327de-327">ถ้าคุณใช้ Finance and Operations รุ่นใดรุ่นหนึ่งต่อไปนี้ คุณสามารถวิเคราะห์รายละเอียดของการติดตามประสิทธิภาพที่สร้างขึ้นโดยตรงใน Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="327de-327">If you use one of these versions of Finance and Operations, you can analyze the details of generated performance traces directly in Finance and Operations.</span></span> <span data-ttu-id="327de-328">คุณไม่จำเป็นต้องส่งออกจาก Finance and Operations และนำเข้าไปยัง RCS</span><span class="sxs-lookup"><span data-stu-id="327de-328">You don't have to export them from Finance and Operation and import them into RCS.</span></span>

## <a name="review-the-execution-trace-by-using-external-tools"></a><span data-ttu-id="327de-329">ตรวจทานการติดตามการดำเนินการโดยใช้เครื่องมือภายนอก</span><span class="sxs-lookup"><span data-stu-id="327de-329">Review the execution trace by using external tools</span></span>

### <a name="configure-user-parameters"></a><span data-ttu-id="327de-330">ตั้งค่าคอนฟิกพารามิเตอร์ผู้ใช้</span><span class="sxs-lookup"><span data-stu-id="327de-330">Configure user parameters</span></span>

1. <span data-ttu-id="327de-331">ใน Finance and Operations ไปที่ **การจัดการองค์กร \> การรายงานทางอิเล็กทรอนิกส์ \> การตั้งค่าคอนฟิก**</span><span class="sxs-lookup"><span data-stu-id="327de-331">In Finance and Operations, go to **Organization administration \> Electronic reporting \> Configurations**.</span></span>
2. <span data-ttu-id="327de-332">ในหน้า **การตั้งค่าคอนฟิก** บนบานหน้าต่างการดำเนินการ บนแท็บ **การตั้งค่าคอนฟิก** ในกลุ่ม **การตั้งค่าล่วงหน้า** เลือก **พารามิเตอร์ผู้ใช้**</span><span class="sxs-lookup"><span data-stu-id="327de-332">On the **Configurations** page, on the Action Pane, on the **Configurations** tab, in the **Advanced settings** group, select **User parameters**.</span></span>
3. <span data-ttu-id="327de-333">ในกล่องโต้ตอบ **พารามิเตอร์ผู้ใช้** ในส่วน **การติดตามการดำเนินการ** ในฟิลด์ **รูปแบบการติดตามการดำเนินการ** เลือก **PerfView XML**</span><span class="sxs-lookup"><span data-stu-id="327de-333">In the **User parameters** dialog box, in the **Execution tracing** section, in the **Execution trace format** field, select **PerfView XML**.</span></span>

### <a name="run-the-er-format"></a><span data-ttu-id="327de-334">รันรูปแบบ ER</span><span class="sxs-lookup"><span data-stu-id="327de-334">Run the ER format</span></span>

<span data-ttu-id="327de-335">ทำซ้ำขั้นตอนในส่วน [รันรูปแบบ ER](#run-format) ก่อนหน้าในหัวข้อนี้ เพื่อสร้างการติดตามประสิทธิภาพใหม่</span><span class="sxs-lookup"><span data-stu-id="327de-335">Repeat the steps in the [Run the ER format](#run-format) section earlier in this topic to generate a new performance trace.</span></span>

<span data-ttu-id="327de-336">โปรดสังเกตว่าเว็บเบราเซอร์มีไฟล์ซิปสำหรับการดาวน์โหลด</span><span class="sxs-lookup"><span data-stu-id="327de-336">Notice that the web browser offers a zip file for download.</span></span> <span data-ttu-id="327de-337">ไฟล์นี้มีการติดตามประสิทธิภาพในรูปแบบ PerfView</span><span class="sxs-lookup"><span data-stu-id="327de-337">This file contains the performance trace in PerfView format.</span></span> <span data-ttu-id="327de-338">จากนั้น คุณสามารถใช้เครื่องมือวิเคราะห์ประสิทธิภาพ PerfView เพื่อวิเคราะห์รายละเอียดของการดำเนินการของรูปแบบ ER</span><span class="sxs-lookup"><span data-stu-id="327de-338">You can then use the PerfView performance analysis tool to analyze the details of ER format execution.</span></span>
