---
title: ตั้งค่าลำดับชั้นขององค์กร
description: หัวข้อนี้อธิบายวิธีการตั้งค่าลำดับชั้นขององค์กรใน Microsoft Dynamics 365 Commerce
author: samjarawan
manager: annbe
ms.date: 01/27/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: samjar
ms.search.validFrom: 2020-01-20
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: 29d4b686cbb66715196fca06e4642fbb8a337ace
ms.sourcegitcommit: 141e0239b6310ab4a6a775bc0997120c31634f79
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 03/10/2020
ms.locfileid: "3113862"
---
# <a name="set-up-organization-hierarchies"></a><span data-ttu-id="c34be-103">ตั้งค่าลำดับชั้นขององค์กร</span><span class="sxs-lookup"><span data-stu-id="c34be-103">Set up organization hierarchies</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="c34be-104">หัวข้อนี้อธิบายวิธีการตั้งค่าลำดับชั้นขององค์กรใน Microsoft Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="c34be-104">This topic describes how to set up organization hierarchies in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="c34be-105">ภาพรวม</span><span class="sxs-lookup"><span data-stu-id="c34be-105">Overview</span></span>

<span data-ttu-id="c34be-106">ก่อนที่จะสร้างช่องทาง คุณต้องตรวจสอบให้แน่ใจว่าคุณได้ตั้งค่าลำดับชั้นขององค์กรของคุณแล้ว</span><span class="sxs-lookup"><span data-stu-id="c34be-106">Before creating channels, you'll want to ensure you have set up your organization hierarchies.</span></span>

<span data-ttu-id="c34be-107">คุณสามารถใช้ลำดับชั้นขององค์กรเพื่อดู และรายงานในบธุรกิจของคุณจากมุมมองต่างๆได้</span><span class="sxs-lookup"><span data-stu-id="c34be-107">You can use organization hierarchies to view and report on your business from various perspectives.</span></span> <span data-ttu-id="c34be-108">ตัวอย่างเช่น คุณสามารถตั้งค่าหนึ่งลำดับชั้นสำหรับภาษี ทางกฎหมาย หรือการรายงานตามกฎหมาย</span><span class="sxs-lookup"><span data-stu-id="c34be-108">For example, you can set up one hierarchy for tax, legal, or statutory reporting.</span></span> <span data-ttu-id="c34be-109">จากนั้นคุณสามารถตั้งค่าอีกลำดับชั้นได้เพื่อรายงานข้อมูลทางการเงินที่ไม่จำเป็นทางกฎหมาย แต่ถูกใช้เป็นการรายงานภายใน</span><span class="sxs-lookup"><span data-stu-id="c34be-109">You can then set up another hierarchy to report financial information that is not legally required, but that is used for internal reporting.</span></span>

<span data-ttu-id="c34be-110">ก่อนที่คุณจะสร้างลำดับชั้นขององค์กร คุณต้องสร้างองค์กร</span><span class="sxs-lookup"><span data-stu-id="c34be-110">Before you create an organization hierarchy, you must create organizations.</span></span> <span data-ttu-id="c34be-111">สำหรับข้อมูลเพิ่มเติม ดูที่ [สร้างนิติบุคคล](channels-legal-entities.md) หรือ [สร้างหน่วยปฏิบัติงาน](../fin-ops-core/fin-ops/organization-administration/tasks/create-operating-unit.md?toc=/dynamics365/commerce/toc.json)</span><span class="sxs-lookup"><span data-stu-id="c34be-111">For more information, see [Create legal entities](channels-legal-entities.md) or [Create operating units](../fin-ops-core/fin-ops/organization-administration/tasks/create-operating-unit.md?toc=/dynamics365/commerce/toc.json).</span></span>


<span data-ttu-id="c34be-112">สำหรับข้อมูลเพิ่มเติม ให้ดูหัวข้อต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="c34be-112">For more information, see the following topics.</span></span>
- [<span data-ttu-id="c34be-113">ภาพรวมขององค์กรและลำดับชั้นขององค์กร</span><span class="sxs-lookup"><span data-stu-id="c34be-113">Organizations and organizational hierarchies overview</span></span>](../fin-ops-core/fin-ops/organization-administration/organizations-organizational-hierarchies.md?toc=/dynamics365/commerce/toc.json)
- [<span data-ttu-id="c34be-114">วางแผนลำดับชั้นขององค์กรของคุณ</span><span class="sxs-lookup"><span data-stu-id="c34be-114">Plan your organization hierarchy</span></span>](../fin-ops-core/fin-ops/organization-administration/plan-organizational-hierarchy.md?toc=/dynamics365/commerce/toc.json)
- [<span data-ttu-id="c34be-115">สร้างลำดับชั้นขององค์กร</span><span class="sxs-lookup"><span data-stu-id="c34be-115">Create an organization hierarchy</span></span>](../fin-ops-core/fin-ops/organization-administration/tasks/create-organization-hierarchy.md?toc=/dynamics365/commerce/toc.json)

## <a name="create-an-organizational-hierarchy"></a><span data-ttu-id="c34be-116">สร้างลำดับชั้นขององค์กร</span><span class="sxs-lookup"><span data-stu-id="c34be-116">Create an organizational hierarchy</span></span>

<span data-ttu-id="c34be-117">หากต้องการสร้างลำดับชั้นองค์กร ให้ทำตามขั้นตอนต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="c34be-117">To create an organizational hierarchy, follow these steps.</span></span>

1. <span data-ttu-id="c34be-118">ในบานหน้าต่างนำทาง ไปที่ **โมดูล \> การขายปลีกและการค้า \> การตั้งค่าช่องทาง \> ลำดับชั้นขององค์กร**</span><span class="sxs-lookup"><span data-stu-id="c34be-118">In the navigation pane, go to **Modules \> Retail and commerce \> Channel Setup \> Organization hierarchies**.</span></span>
1. <span data-ttu-id="c34be-119">บนหน้าต่างการดำเนินการ เลือก **สร้าง**</span><span class="sxs-lookup"><span data-stu-id="c34be-119">On the action pane, select **New**.</span></span>
1. <span data-ttu-id="c34be-120">ในฟิลด์ **ชื่อ** ให้ป้อนค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="c34be-120">In the **Name** field, enter a value.</span></span>
1. <span data-ttu-id="c34be-121">ในส่วน **วัตถุประสงค์** เลือก **กำหนดวัตถุประสงค์**</span><span class="sxs-lookup"><span data-stu-id="c34be-121">In the **Purpose** section, select **Assign purpose**.</span></span>
1. <span data-ttu-id="c34be-122">ในรายการนี้ ให้ค้นหาและเลือกเรกคอร์ดที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="c34be-122">In the list, find and select the desired record.</span></span> <span data-ttu-id="c34be-123">เลือกวัตถุประสงค์เพื่อกำหนดให้กับลำดับชั้นขององค์กรของคุณ</span><span class="sxs-lookup"><span data-stu-id="c34be-123">Select a purpose to assign to your organization hierarchy.</span></span>
1. <span data-ttu-id="c34be-124">ในส่วน **ลำดับชั้นที่กำหนด** เลือก **เพิ่ม**</span><span class="sxs-lookup"><span data-stu-id="c34be-124">In the **Assigned hierarchies** section, select **Add**.</span></span>
1. <span data-ttu-id="c34be-125">ในรายการนี้ ให้ทำเครื่องหมายแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="c34be-125">In the list, mark the selected row.</span></span> <span data-ttu-id="c34be-126">ค้นหาลำดับชั้นที่คุณเพิ่งสร้างขึ้น</span><span class="sxs-lookup"><span data-stu-id="c34be-126">Find the hierarchy you just created.</span></span>
1. <span data-ttu-id="c34be-127">เลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="c34be-127">Select **OK**.</span></span>

<span data-ttu-id="c34be-128">รูปภาพต่อไปนี้แสดงตัวอย่างของลำดับชั้นขององค์กรที่สร้างขึ้นสำหรับชุดของร้านค้า "Adventure Works" แบบสมมติ</span><span class="sxs-lookup"><span data-stu-id="c34be-128">The following image shows an example organizational hierarchy created for a fictitious "Adventure Works" set of stores.</span></span>

![ตัวอย่างลำดับชั้นขององค์กร](media/organizational-hierarchies.png)

### <a name="add-organizations-to-a-hierarchy"></a><span data-ttu-id="c34be-130">เพิ่มองค์กรให้กับลำดับชั้น</span><span class="sxs-lookup"><span data-stu-id="c34be-130">Add organizations to a hierarchy</span></span>

<span data-ttu-id="c34be-131">หากต้องการเพิ่มองค์กรให้กับลำดับชั้น ให้ทำตามขั้นตอนต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="c34be-131">To add organizations to a hierarchy, follow these steps.</span></span>

1. <span data-ttu-id="c34be-132">ในรายการนี้ ให้ค้นหาและเลือกเรกคอร์ดที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="c34be-132">In the list, find and select the desired record.</span></span> <span data-ttu-id="c34be-133">เลือกลำดับชั้นของคุณ</span><span class="sxs-lookup"><span data-stu-id="c34be-133">Select your hierarchy.</span></span>
1. <span data-ttu-id="c34be-134">บนบานหน้าต่างการดำเนินการ เลือก **ดู**</span><span class="sxs-lookup"><span data-stu-id="c34be-134">On the action pane, select **View**.</span></span>
1. <span data-ttu-id="c34be-135">เพิ่มองค์กรตามความจำเป็น</span><span class="sxs-lookup"><span data-stu-id="c34be-135">Add organizations, as necessary.</span></span>
1. <span data-ttu-id="c34be-136">เมื่อต้องการเพิ่มองค์กร ให้เลือก **แก้ไข** และจากนั้นเลือก **แทรก**</span><span class="sxs-lookup"><span data-stu-id="c34be-136">To add an organization, select **Edit** and then select **Insert**.</span></span> <span data-ttu-id="c34be-137">เมื่อคุณดำเนินการเปลี่ยนแปลงเสร็จสิ้น คุณสามารถบันทึกแบบร่างและเผยแพร่การเปลี่ยนแปลงได้</span><span class="sxs-lookup"><span data-stu-id="c34be-137">When you are done making changes you can save a draft and publish the changes.</span></span>

<span data-ttu-id="c34be-138">รูปภาพต่อไปนี้แสดงนิติบุคคลที่เพิ่มที่รากลำดับชั้นกับศูนย์ต้นทุนสี่ศูนย์ที่เพิ่มสำหรับช่องทาง "ขนาดเล็ก" "ช่องระบาย" "ออนไลน์" และ "ศูนย์บริการ"</span><span class="sxs-lookup"><span data-stu-id="c34be-138">The following image shows a legal entity added at the hierarchy root with four cost centers added for "Mall", "Outlet", "Online" and "Call Center" channels.</span></span> <span data-ttu-id="c34be-139">คุณสามารถเพิ่มร้านค้าปลีก ศูนย์บริการ และช่องทางออนไลน์ต่าง ๆ เข้าในแต่ละที่ได้</span><span class="sxs-lookup"><span data-stu-id="c34be-139">Various retail, call center and online channels can then be added to each.</span></span>

![ตัวอย่างของตัวออกแบบลำดับชั้น](media/hierarchy-designer.png)

## <a name="additional-resources"></a><span data-ttu-id="c34be-141">แหล่งข้อมูลเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="c34be-141">Additional resources</span></span>

[<span data-ttu-id="c34be-142">ภาพรวมขององค์กรและลำดับชั้นขององค์กร</span><span class="sxs-lookup"><span data-stu-id="c34be-142">Organizations and organizational hierarchies overview</span></span>](../fin-ops-core/fin-ops/organization-administration/organizations-organizational-hierarchies.md?toc=/dynamics365/commerce/toc.json)

[<span data-ttu-id="c34be-143">วางแผนลำดับชั้นขององค์กรของคุณ</span><span class="sxs-lookup"><span data-stu-id="c34be-143">Plan your organizational hierarchy</span></span>](../fin-ops-core/fin-ops/organization-administration/plan-organizational-hierarchy.md?toc=/dynamics365/commerce/toc.json)

[<span data-ttu-id="c34be-144">สร้างนิติบุคคล</span><span class="sxs-lookup"><span data-stu-id="c34be-144">Create legal entities</span></span>](channels-legal-entities.md)

[<span data-ttu-id="c34be-145">สร้างหน่วยปฏิบัติงาน</span><span class="sxs-lookup"><span data-stu-id="c34be-145">Create operating units</span></span>](../fin-ops-core/fin-ops/organization-administration/tasks/create-operating-unit.md?toc=/dynamics365/commerce/toc.json)

[<span data-ttu-id="c34be-146">ภาพรวมของช่องทาง</span><span class="sxs-lookup"><span data-stu-id="c34be-146">Channels overview</span></span>](channels-overview.md)

[<span data-ttu-id="c34be-147">ข้อกำหนดเบื้องต้นในการตั้งค่าช่องทาง</span><span class="sxs-lookup"><span data-stu-id="c34be-147">Channel setup prerequisites</span></span>](channels-prerequisites.md)
