---
title: รวม Dynamics 365 Supply Chain Management (การจัดการสินทรัพย์) ด้วย Dynamics 365 Guides
description: หัวข้อนี้อธิบายถึงวิธีการรวมโมดูลการจัดการสินทรัพย์ใน Microsoft  Dynamics 365 Supply Chain Management ด้วย Dynamics 365 Guides เพื่อใช้ประโยชน์จากคู่มือแบบผสมความจริงในการให้บริการและลำดับงานการบำรุงรักษาในแต่ละวัน
author: kamaybac
manager: tfehr
ms.date: 04/28/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: dabourq
ms.search.validFrom: 2020-04-28
ms.dyn365.ops.version: Release 10.0.12
ms.openlocfilehash: f9ee7f1af8e88f56589c84bfaa063ea005aa353a
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 10/13/2020
ms.locfileid: "4438312"
---
# <a name="integrate-dynamics-365-supply-chain-management-asset-management-with-dynamics-365-guides"></a><span data-ttu-id="3b1ad-103">รวม Dynamics 365 Supply Chain Management (การจัดการสินทรัพย์) ด้วย Dynamics 365 Guides</span><span class="sxs-lookup"><span data-stu-id="3b1ad-103">Integrate Dynamics 365 Supply Chain Management (Asset management) with Dynamics 365 Guides</span></span>

<span data-ttu-id="3b1ad-104">คุณสามารถรวมโมดูล **การจัดการสินทรัพย์** ใน Microsoft Dynamics 365 Supply Chain Management ด้วย Dynamics 365 Guides เพื่อใช้ประโยชน์จากคู่มือแบบผสมความจริงในการให้บริการและลำดับงานการบำรุงรักษาในแต่ละวัน</span><span class="sxs-lookup"><span data-stu-id="3b1ad-104">You can integrate the **Asset management** module in Microsoft Dynamics 365 Supply Chain Management with Dynamics 365 Guides to take advantage of mixed-reality guides in your day-to-day service and maintenance workflows.</span></span> <span data-ttu-id="3b1ad-105">ถ้าคู่มือเชื่อมโยงกับใบสั่งงานการจัดการสินทรัพย์ ผู้ปฏิบัติงานที่เปิดรายการตรวจสอบการบำรุงรักษาของใบสั่งงานในแอป Supply Chain Management (Dynamics 365) สำหรับอุปกรณ์เคลื่อนที่เห็นว่าคู่มือจะพร้อมใช้งาน</span><span class="sxs-lookup"><span data-stu-id="3b1ad-105">If a guide is associated with an Asset Management work order, a worker who opens the work order's maintenance checklist in the Supply Chain Management (Dynamics 365) mobile app sees that a guide is available.</span></span> <span data-ttu-id="3b1ad-106">ผู้ปฏิบัติงานสามารถค้นหา และเปิดคู่มือในแอป Dynamics 365 Guides HoloLens</span><span class="sxs-lookup"><span data-stu-id="3b1ad-106">The worker can then find and open the guide in the Dynamics 365 Guides HoloLens app.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="3b1ad-107">ข้อกำหนดเบื้องต้น</span><span class="sxs-lookup"><span data-stu-id="3b1ad-107">Prerequisites</span></span>

<span data-ttu-id="3b1ad-108">ก่อนที่คุณจะสามารถแนบคู่มือกับใบสั่งงานการจัดการสินทรัพย์ คุณต้องดำเนินการข้อกำหนดเบื้องต้นต่อไปนี้ให้สมบูรณ์:</span><span class="sxs-lookup"><span data-stu-id="3b1ad-108">Before you can attach guides to Asset management work orders, you must complete these prerequisites:</span></span>

- <span data-ttu-id="3b1ad-109">[ตั้งค่า Dynamics 365 Supply Chain Management](../../fin-ops-core/fin-ops/index.md) รุ่น 10.0.9 หรือใหม่กว่า</span><span class="sxs-lookup"><span data-stu-id="3b1ad-109">[Set up Dynamics 365 Supply Chain Management](../../fin-ops-core/fin-ops/index.md) version 10.0.9 or later.</span></span>
- <span data-ttu-id="3b1ad-110">[เปิดใช้งานการรวมแบบสองทิศทางสำหรับแอป Supply Chain Management](../../fin-ops-core/dev-itpro/data-entities/dual-write/enable-dual-write.md)</span><span class="sxs-lookup"><span data-stu-id="3b1ad-110">[Turn on dual-write for Supply Chain Management apps](../../fin-ops-core/dev-itpro/data-entities/dual-write/enable-dual-write.md).</span></span>
- <span data-ttu-id="3b1ad-111">[เปิดใช้งานการบิน](../../fin-ops-core/dev-itpro/data-entities/data-entities-data-packages.md#features-flighted-in-data-management-and-enabling-flighted-features) สำหรับคุณลักษณะ  **MRGuidesFeature**</span><span class="sxs-lookup"><span data-stu-id="3b1ad-111">[Turn on flight](../../fin-ops-core/dev-itpro/data-entities/data-entities-data-packages.md#features-flighted-in-data-management-and-enabling-flighted-features) for the **MRGuidesFeature** feature.</span></span> <span data-ttu-id="3b1ad-112">(สำหรับสภาพแวดล้อมการผลิต คุณต้องส่งตั๋วสนับสนุน เพื่อให้ผู้เช่าของคุณถูกเพิ่มลงในกลุ่มการบิน)</span><span class="sxs-lookup"><span data-stu-id="3b1ad-112">(For production environments, you must first submit a support ticket to have your tenant added to the flighting group.)</span></span>
- <span data-ttu-id="3b1ad-113">[เปิดใช้งานคีย์การตั้งค่าคอนฟิกต่อไปนี้](https://docs.microsoft.com/dynamicsax-2012/appuser-itpro/license-code-and-configuration-key-reference) บนหน้า **การตั้งค่าคอนฟิกลิขสิทธิ์** :</span><span class="sxs-lookup"><span data-stu-id="3b1ad-113">[Turn on the following configuration keys](https://docs.microsoft.com/dynamicsax-2012/appuser-itpro/license-code-and-configuration-key-reference) on the **License configuration** page:</span></span>

    - <span data-ttu-id="3b1ad-114">การบริหารสินทรัพย์ \> การบริหารสินทรัพย์ความเป็นจริงผสม</span><span class="sxs-lookup"><span data-stu-id="3b1ad-114">Asset management \> Asset management mixed reality</span></span>
    - <span data-ttu-id="3b1ad-115">ความเป็นจริงผสม \> คู่มือความเป็นจริงผสม</span><span class="sxs-lookup"><span data-stu-id="3b1ad-115">Mixed reality \> Mixed reality guide</span></span>

- <span data-ttu-id="3b1ad-116">[ตั้งค่า Dynamics 365 Guides](https://docs.microsoft.com/dynamics365/mixed-reality/guides/setup#step-2-create-a-common-data-service-environment-and-install-the-dynamics-365-guides-solution) รุ่น 200.0.0.96 หรือใหม่กว่า</span><span class="sxs-lookup"><span data-stu-id="3b1ad-116">[Set up Dynamics 365 Guides](https://docs.microsoft.com/dynamics365/mixed-reality/guides/setup#step-2-create-a-common-data-service-environment-and-install-the-dynamics-365-guides-solution) version 200.0.0.96 or later.</span></span>

## <a name="use-dynamics-365-guides-with-asset-management"></a><span data-ttu-id="3b1ad-117">ใช้ Dynamics 365 Guides กับการจัดการสินทรัพย์</span><span class="sxs-lookup"><span data-stu-id="3b1ad-117">Use Dynamics 365 Guides with Asset management</span></span>

<span data-ttu-id="3b1ad-118">เมื่อต้องการเชื่อมโยงคู่มือ ให้คุณใช้บรรทัดรายการตรวจสอบการบำรุงรักษาในการบริหารสินทรัพย์</span><span class="sxs-lookup"><span data-stu-id="3b1ad-118">To associate a guide, you use a maintenance checklist line in Asset management.</span></span> <span data-ttu-id="3b1ad-119">คุณสามารถสร้างความสัมพันธ์ผ่านแม่แบบใบสั่งรายการตรวจสอบการบำรุงรักษา ชนิดงานการบำรุงรักษา หรือใบสั่งงาน เนื่องจากมีบรรทัดรายการตรวจสอบการบำรุงรักษาทั้งสามรายการ</span><span class="sxs-lookup"><span data-stu-id="3b1ad-119">You can create the association through a maintenance checklist template, a maintenance job type, or a work order, because all three contain maintenance checklist lines.</span></span> <span data-ttu-id="3b1ad-120">คุณสามารถประหยัดเวลาโดยใช้แม่แบบได้ เนื่องจากแม่แบบจะเชื่อมโยงกับชนิดงานการบำรุงรักษาทั้งหมดที่ใช้</span><span class="sxs-lookup"><span data-stu-id="3b1ad-120">You can save time by using a template, because a template can be associated with all the maintenance job types that use it.</span></span> <span data-ttu-id="3b1ad-121">ตัวอย่างเช่น คู่มือที่เชื่อมโยงกับชนิดงานการบำรุงรักษาจะเชื่อมโยงกับใบสั่งงานทั้งหมดที่ระบุชนิดงานนั้นโดยอัตโนมัติ</span><span class="sxs-lookup"><span data-stu-id="3b1ad-121">For example, a guide that is associated with a maintenance job type is automatically associated with all work orders that specify that job type.</span></span> <span data-ttu-id="3b1ad-122">ในทางกลับกัน คู่มือที่เชื่อมโยงกับโดยตรงกับใบสั่งงานมีอยู่เฉพาะในใบสั่งงานนั้นเท่านั้น</span><span class="sxs-lookup"><span data-stu-id="3b1ad-122">On the other hand, a guide that is associated directly with a work order exists only for that work order.</span></span>

### <a name="associate-a-guide-with-a-maintenance-checklist-template"></a><span data-ttu-id="3b1ad-123">เชื่อมโยงคู่มือกับแม่แบบรายการตรวจสอบการบำรุงรักษา</span><span class="sxs-lookup"><span data-stu-id="3b1ad-123">Associate a guide with a maintenance checklist template</span></span>

<span data-ttu-id="3b1ad-124">เมื่อต้องการเชื่อมโยงคู่มือกับแม่แบบรายการตรวจสอบการบำรุงรักษา ให้ทำตามขั้นตอนต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="3b1ad-124">To associate a guide with a maintenance checklist template, follow these steps.</span></span>

1. <span data-ttu-id="3b1ad-125">สร้างคู่มือโดยใช้แอป Dynamics 365 Guides PC และแอป HoloLens</span><span class="sxs-lookup"><span data-stu-id="3b1ad-125">Create a guide by using the Dynamics 365 Guides PC and HoloLens apps.</span></span> <span data-ttu-id="3b1ad-126">สำหรับข้อมูลเกี่ยวกับวิธีสร้างคูมือ ให้ดูหัวข้อต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="3b1ad-126">For information about how to create a guide, see the following topics:</span></span>

    - [<span data-ttu-id="3b1ad-127">ใช้แอป PC เพื่อสร้างคู่มือ</span><span class="sxs-lookup"><span data-stu-id="3b1ad-127">Use the PC app to create a guide</span></span>](https://docs.microsoft.com/dynamics365/mixed-reality/guides/pc-app-overview)
    - [<span data-ttu-id="3b1ad-128">ใช้แอป HoloLens เพื่อวางโฮโลแกรมของคุณ</span><span class="sxs-lookup"><span data-stu-id="3b1ad-128">Use the HoloLens app to place your holograms</span></span>](https://docs.microsoft.com/dynamics365/mixed-reality/guides/hololens-app-overview)

1. <span data-ttu-id="3b1ad-129">ใน Supply Chain Management ให้ [สร้างแม่แบบรายการตรวจสอบการบำรุงรักษา](setup-for-work-orders/job-groups-and-job-types-variants-trades-and-checklists.md#create-a-maintenance-checklist-template)</span><span class="sxs-lookup"><span data-stu-id="3b1ad-129">In Supply Chain Management, [create a maintenance checklist template](setup-for-work-orders/job-groups-and-job-types-variants-trades-and-checklists.md#create-a-maintenance-checklist-template).</span></span>
1. <span data-ttu-id="3b1ad-130">เชื่อมโยงคู่มือที่คุณสร้างด้วยบรรทัดรายการตรวจสอบการบำรุงรักษาในแม่แบบรายการตรวจสอบการบำรุงรักษาใหม่:</span><span class="sxs-lookup"><span data-stu-id="3b1ad-130">Associate the guide that you created with a maintenance checklist line in the new maintenance checklist template:</span></span>

    1. <span data-ttu-id="3b1ad-131">บนแท็บด่วน **บรรทัดรายการตรวจสอบการบำรุงรักษา** ให้เลือกรายการที่คุณต้องการเชื่อมโยงกับคู่มือ</span><span class="sxs-lookup"><span data-stu-id="3b1ad-131">On the **Maintenance checklist lines** FastTab, select the line that you want to associate the guide with.</span></span>
    1. <span data-ttu-id="3b1ad-132">บนแท็บด่วน **คู่มือที่เชื่อมโยง** ให้เลือก **เพิ่มคู่มือ**</span><span class="sxs-lookup"><span data-stu-id="3b1ad-132">On the **Associated guides** FastTab, select **Add Guide**.</span></span>

        <span data-ttu-id="3b1ad-133">![เชื่อมโยงคู่มือกับบรรทัดรายการตรวจสอบการบำรุงรักษา](media/am-guides-integration-add-guide.png "เชื่อมโยงคู่มือกับบรรทัดรายการตรวจสอบการบำรุงรักษา")</span><span class="sxs-lookup"><span data-stu-id="3b1ad-133">![Associate a guide with a maintenance checklist line](media/am-guides-integration-add-guide.png "Associate a guide with a maintenance checklist line")</span></span>

    1. <span data-ttu-id="3b1ad-134">ในฟิลด์ **ชื่อ** ให้เลือกคู่มือ แล้วเลือก **บันทึก**</span><span class="sxs-lookup"><span data-stu-id="3b1ad-134">In the **Name** field, select a guide, and then select **Save**.</span></span>

        <span data-ttu-id="3b1ad-135">![เลือกคู่มือในฟิลด์ชื่อ](media/am-guides-integration-select-guide.png "เลือกคู่มือในฟิลด์ชื่อ")</span><span class="sxs-lookup"><span data-stu-id="3b1ad-135">![Select a guide in the Name field](media/am-guides-integration-select-guide.png "Select a guide in the Name field")</span></span>

1. <span data-ttu-id="3b1ad-136">เชื่อมโยงแม่แบบรายการตรวจสอบการบำรุงรักษากับชนิดงาน:</span><span class="sxs-lookup"><span data-stu-id="3b1ad-136">Associate the maintenance checklist template with a job type:</span></span>

    1. <span data-ttu-id="3b1ad-137">[สร้างชนิดงานการบำรุงรักษา](setup-for-work-orders/job-groups-and-job-types-variants-trades-and-checklists.md#create-a-maintenance-job-type) หรือเลือกชนิดงานบำรุงรักษาที่มีอยู่</span><span class="sxs-lookup"><span data-stu-id="3b1ad-137">[Create a maintenance job type](setup-for-work-orders/job-groups-and-job-types-variants-trades-and-checklists.md#create-a-maintenance-job-type), or select an existing maintenance job type.</span></span>
    1. <span data-ttu-id="3b1ad-138">บนบานหน้าต่างการดำเนินการ ให้เลือก **ค่าเริ่มต้นของชนิดงานการบำรุงรักษา**</span><span class="sxs-lookup"><span data-stu-id="3b1ad-138">On the Action Pane, select **Maintenance job type defaults**.</span></span>

        <span data-ttu-id="3b1ad-139">![ปุ่มค่าเริ่มต้นของชนิดงานการบำรุงรักษา](media/am-guides-integration-job-defaults.png "ปุ่มค่าเริ่มต้นของชนิดงานการบำรุงรักษา")</span><span class="sxs-lookup"><span data-stu-id="3b1ad-139">![Maintenance job type defaults button](media/am-guides-integration-job-defaults.png "Maintenance job type defaults button")</span></span>

    1. <span data-ttu-id="3b1ad-140">สร้างบรรทัด แล้วเลือก **บันทึก**</span><span class="sxs-lookup"><span data-stu-id="3b1ad-140">Create a line, and then select **Save**.</span></span>

        <span data-ttu-id="3b1ad-141">![สร้างบรรทัด](media/am-guides-integration-add-line.png "สร้างบรรทัด")</span><span class="sxs-lookup"><span data-stu-id="3b1ad-141">![Create a line](media/am-guides-integration-add-line.png "Create a line")</span></span>

    1. <span data-ttu-id="3b1ad-142">ในบานหน้าต่างการดำเนินการ เลือก **รายการตรวจสอบการบำรุงรักษา**</span><span class="sxs-lookup"><span data-stu-id="3b1ad-142">On the Action Pane, select **Maintenance checklist**.</span></span>

        <span data-ttu-id="3b1ad-143">![ปุ่มรายการตรวจสอบการบำรุงรักษา](media/am-guides-integration-maintenance-checklist.png "ปุ่มรายการตรวจสอบการบำรุงรักษา")</span><span class="sxs-lookup"><span data-stu-id="3b1ad-143">![Maintenance checklist button](media/am-guides-integration-maintenance-checklist.png "Maintenance checklist button")</span></span>

    1. <span data-ttu-id="3b1ad-144">บนแท็บด่วน **บรรทัดรายการตรวจสอบการบำรุงรักษา** เพิ่มบรรทัด แล้วเปลี่ยนค่าของฟิลด์ **ชนิด** เป็น **แม่แบบ**</span><span class="sxs-lookup"><span data-stu-id="3b1ad-144">On the **Maintenance checklist lines** FastTab, add a line, and then change the value of the **Type** field to **Template**.</span></span>

        <span data-ttu-id="3b1ad-145">![เปลี่ยนค่าชนิด](media/am-guides-integration-checklist-lines.png "เปลี่ยนค่าชนิด")</span><span class="sxs-lookup"><span data-stu-id="3b1ad-145">![Change the Type value](media/am-guides-integration-checklist-lines.png "Change the Type value")</span></span>

    1. <span data-ttu-id="3b1ad-146">บนแท็บด่วน **รายละเอียดของรายการ** ในฟิลด์ **แม่แบบ** ให้เลือกแม่แบบที่คุณเชื่อมโยงคู่มือด้วย แล้วเลือก **บันทึก**</span><span class="sxs-lookup"><span data-stu-id="3b1ad-146">On the **Line details** FastTab, in the **Template** field, select the template that you associated the guide with, and then select **Save**.</span></span>

        <span data-ttu-id="3b1ad-147">![เลือกแม่แบบ](media/am-guides-integration-checklist-line-details.png "เลือกแม่แบบ")</span><span class="sxs-lookup"><span data-stu-id="3b1ad-147">![Select the template](media/am-guides-integration-checklist-line-details.png "Select the template")</span></span>

1. <span data-ttu-id="3b1ad-148">[สร้างใบสั่งงาน](work-orders/manually-created-workorders.md#create-work-order) แล้วเลือกชนิดงานการบำรุงรักษาที่ใช้แม่แบบรายการตรวจสอบการบำรุงรักษาที่คุณเชื่อมโยงกับคู่มือ</span><span class="sxs-lookup"><span data-stu-id="3b1ad-148">[Create a work order](work-orders/manually-created-workorders.md#create-work-order), and then select the maintenance job type that uses the maintenance checklist template that you associated the guide with.</span></span> <span data-ttu-id="3b1ad-149">คู่มือถูกเชื่อมโยงกับใบสั่งงานโดยอัตโนมัติ</span><span class="sxs-lookup"><span data-stu-id="3b1ad-149">The guide is automatically associated with the work order.</span></span>

    <span data-ttu-id="3b1ad-150">![เลือกชนิดของงานบำรุงรักษา](media/am-guides-integration-create-work-order.png "เลือกชนิดของงานบำรุงรักษา")</span><span class="sxs-lookup"><span data-stu-id="3b1ad-150">![Select a maintenance job type](media/am-guides-integration-create-work-order.png "Select a maintenance job type")</span></span>

1. <span data-ttu-id="3b1ad-151">ดูคู่มือที่เชื่อมโยงกับใบสั่งงานและผู้ปฏิบัติงาน</span><span class="sxs-lookup"><span data-stu-id="3b1ad-151">View the guide that is associated with the work order and workers:</span></span>

    1. <span data-ttu-id="3b1ad-152">เปิด [พื้นที่ทำงานแบบเคลื่อนที่ในการจัดการสินทรัพย์](asset-management-mobile-workspace.md) เพื่อเข้าถึงใบสั่งงาน</span><span class="sxs-lookup"><span data-stu-id="3b1ad-152">Open the [Asset management mobile workspace](asset-management-mobile-workspace.md) to access the work order.</span></span>
    1. <span data-ttu-id="3b1ad-153">[เปิดรายการตรวจสอบการบำรุงรักษา](asset-management-mobile-workspace.md#view-maintenance-checklist-on-a-work-order-job) สำหรับใบสั่งงาน</span><span class="sxs-lookup"><span data-stu-id="3b1ad-153">[Open the maintenance checklist](asset-management-mobile-workspace.md#view-maintenance-checklist-on-a-work-order-job) for the work order.</span></span>
    1. <span data-ttu-id="3b1ad-154">เลือกรายการตรวจสอบเพื่อดูคู่มือที่เกี่ยวข้อง</span><span class="sxs-lookup"><span data-stu-id="3b1ad-154">Select a checklist line to see the associated guide.</span></span>

        <span data-ttu-id="3b1ad-155">![คู่มือที่เชื่อมโยงกับรายการตรวจสอบ](media/am-guides-integration-show-guide.png "คู่มือที่เชื่อมโยงกับรายการตรวจสอบ")</span><span class="sxs-lookup"><span data-stu-id="3b1ad-155">![Guide associated with a checklist line](media/am-guides-integration-show-guide.png "Guide associated with a checklist line")</span></span>

    1. <span data-ttu-id="3b1ad-156">เปิดคู่มือบน HoloLens</span><span class="sxs-lookup"><span data-stu-id="3b1ad-156">Open the guide on HoloLens.</span></span>

        <span data-ttu-id="3b1ad-157">![เปิดคู่มือบน HoloLens](media/am-guides-integration-hololens-select.png "เปิดคู่มือบน HoloLens")</span><span class="sxs-lookup"><span data-stu-id="3b1ad-157">![Open the guide on HoloLens](media/am-guides-integration-hololens-select.png "Open the guide on HoloLens")</span></span>

> [!NOTE]
> <span data-ttu-id="3b1ad-158">นอกจากนี้คุณยังสามารถเชื่อมโยงคู่มือในรายการตรวจสอบการบำรุงรักษาของใบสั่งงานหรือชนิดงานได้โดยตรง</span><span class="sxs-lookup"><span data-stu-id="3b1ad-158">You can also associate a guide directly in the maintenance checklist of a work order or a job type.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="3b1ad-159">มีปัญหาที่ทราบ ซึ่งเมื่อคุณเชื่อมโยแม่แบบรายการตรวจสอบการบำรุงรักษากับชนิดงานการบำรุงรักษาเริ่มต้น คู่มือที่เชื่อมโยงกับเแม่แบบจะไม่แสดงอยู่บนแท็บด่วน **คู่มือที่เชื่อมโยง** ของหน้า **ค่าเริ่มต้นของชนิดงานการบำรุงรักษา**</span><span class="sxs-lookup"><span data-stu-id="3b1ad-159">There is a known issue where, when you associate a maintenance checklist template with a default maintenance job type, the guide that is linked to the template doesn't appear on the **Associated guides** FastTab of the **Maintenance job type defaults** page.</span></span> <span data-ttu-id="3b1ad-160">อย่างไรก็ตาม คู่มือจะปรากฏขึ้นหลังจากชนิดงานนั้นถูกนำไปใช้กับใบสั่งงานบนแท็บด่วน **คู่มือที่เชื่อมโยง**</span><span class="sxs-lookup"><span data-stu-id="3b1ad-160">However, the guide will appear after that job type is applied to a work order on the **Associated guides** FastTab.</span></span>

## <a name="see-also"></a><span data-ttu-id="3b1ad-161">ดูเพิ่มเติมที่</span><span class="sxs-lookup"><span data-stu-id="3b1ad-161">See also</span></span>

- [<span data-ttu-id="3b1ad-162">ภาพรวมของการรวมแบบสองทิศทาง</span><span class="sxs-lookup"><span data-stu-id="3b1ad-162">Dual-write overview</span></span>](../../fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-overview.md)
- [<span data-ttu-id="3b1ad-163">ภาพรวมของการจัดการสินทรัพย์</span><span class="sxs-lookup"><span data-stu-id="3b1ad-163">Asset management overview</span></span>](index.md)
