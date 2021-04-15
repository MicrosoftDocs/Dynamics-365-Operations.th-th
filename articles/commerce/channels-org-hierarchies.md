---
title: ตั้งค่าลำดับชั้นขององค์กร
description: หัวข้อนี้อธิบายวิธีการตั้งค่าลำดับชั้นในองค์กรใน Microsoft Dynamics 365 Commerce
author: samjarawan
ms.date: 01/27/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: samjar
ms.search.validFrom: 2020-01-20
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: 4238d1aa277bf2f1df30825ef20dbf3095d13ebc
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 03/31/2021
ms.locfileid: "5800578"
---
# <a name="set-up-organization-hierarchies"></a><span data-ttu-id="f9ff2-103">ตั้งค่าลำดับชั้นขององค์กร</span><span class="sxs-lookup"><span data-stu-id="f9ff2-103">Set up organization hierarchies</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="f9ff2-104">หัวข้อนี้อธิบายวิธีการตั้งค่าลำดับชั้นในองค์กรใน Microsoft Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="f9ff2-104">This topic describes how to set up organization hierarchies in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="f9ff2-105">ก่อนที่จะสร้างช่องทาง คุณต้องตรวจสอบให้แน่ใจว่าคุณได้ตั้งค่าลำดับชั้นขององค์กรของคุณแล้ว</span><span class="sxs-lookup"><span data-stu-id="f9ff2-105">Before creating channels, you'll want to ensure you have set up your organization hierarchies.</span></span>

<span data-ttu-id="f9ff2-106">คุณสามารถใช้ลำดับชั้นขององค์กรเพื่อดู และรายงานในบธุรกิจของคุณจากมุมมองต่างๆได้</span><span class="sxs-lookup"><span data-stu-id="f9ff2-106">You can use organization hierarchies to view and report on your business from various perspectives.</span></span> <span data-ttu-id="f9ff2-107">ตัวอย่างเช่น คุณสามารถตั้งค่าหนึ่งลำดับชั้นสำหรับภาษี ทางกฎหมาย หรือการรายงานตามกฎหมาย</span><span class="sxs-lookup"><span data-stu-id="f9ff2-107">For example, you can set up one hierarchy for tax, legal, or statutory reporting.</span></span> <span data-ttu-id="f9ff2-108">จากนั้นคุณสามารถตั้งค่าอีกลำดับชั้นได้เพื่อรายงานข้อมูลทางการเงินที่ไม่จำเป็นทางกฎหมาย แต่ถูกใช้เป็นการรายงานภายใน</span><span class="sxs-lookup"><span data-stu-id="f9ff2-108">You can then set up another hierarchy to report financial information that is not legally required, but that is used for internal reporting.</span></span>

<span data-ttu-id="f9ff2-109">ก่อนที่คุณจะสร้างลำดับชั้นขององค์กร คุณต้องสร้างองค์กร</span><span class="sxs-lookup"><span data-stu-id="f9ff2-109">Before you create an organization hierarchy, you must create organizations.</span></span> <span data-ttu-id="f9ff2-110">สำหรับข้อมูลเพิ่มเติม ดูที่ [สร้างนิติบุคคล](channels-legal-entities.md) หรือ [สร้างหน่วยปฏิบัติงาน](../fin-ops-core/fin-ops/organization-administration/tasks/create-operating-unit.md?toc=/dynamics365/commerce/toc.json)</span><span class="sxs-lookup"><span data-stu-id="f9ff2-110">For more information, see [Create legal entities](channels-legal-entities.md) or [Create operating units](../fin-ops-core/fin-ops/organization-administration/tasks/create-operating-unit.md?toc=/dynamics365/commerce/toc.json).</span></span>


<span data-ttu-id="f9ff2-111">สำหรับข้อมูลเพิ่มเติม ให้ดูหัวข้อต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="f9ff2-111">For more information, see the following topics.</span></span>
- [<span data-ttu-id="f9ff2-112">ภาพรวมขององค์กรและลำดับชั้นขององค์กร</span><span class="sxs-lookup"><span data-stu-id="f9ff2-112">Organizations and organizational hierarchies overview</span></span>](../fin-ops-core/fin-ops/organization-administration/organizations-organizational-hierarchies.md?toc=/dynamics365/commerce/toc.json)
- [<span data-ttu-id="f9ff2-113">วางแผนลำดับชั้นขององค์กรของคุณ</span><span class="sxs-lookup"><span data-stu-id="f9ff2-113">Plan your organization hierarchy</span></span>](../fin-ops-core/fin-ops/organization-administration/plan-organizational-hierarchy.md?toc=/dynamics365/commerce/toc.json)
- [<span data-ttu-id="f9ff2-114">สร้างลำดับชั้นขององค์กร</span><span class="sxs-lookup"><span data-stu-id="f9ff2-114">Create an organization hierarchy</span></span>](../fin-ops-core/fin-ops/organization-administration/tasks/create-organization-hierarchy.md?toc=/dynamics365/commerce/toc.json)

## <a name="create-an-organizational-hierarchy"></a><span data-ttu-id="f9ff2-115">สร้างลำดับชั้นขององค์กร</span><span class="sxs-lookup"><span data-stu-id="f9ff2-115">Create an organizational hierarchy</span></span>

<span data-ttu-id="f9ff2-116">หากต้องการสร้างลำดับชั้นองค์กร ให้ทำตามขั้นตอนต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="f9ff2-116">To create an organizational hierarchy, follow these steps.</span></span>

1. <span data-ttu-id="f9ff2-117">ในบานหน้าต่างนำทาง ไปที่ **โมดูล \> การขายปลีกและการค้า \> การตั้งค่าช่องทาง \> ลำดับชั้นขององค์กร**</span><span class="sxs-lookup"><span data-stu-id="f9ff2-117">In the navigation pane, go to **Modules \> Retail and commerce \> Channel Setup \> Organization hierarchies**.</span></span>
1. <span data-ttu-id="f9ff2-118">บนหน้าต่างการดำเนินการ เลือก **สร้าง**</span><span class="sxs-lookup"><span data-stu-id="f9ff2-118">On the action pane, select **New**.</span></span>
1. <span data-ttu-id="f9ff2-119">ในฟิลด์ **ชื่อ** ให้ป้อนค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="f9ff2-119">In the **Name** field, enter a value.</span></span>
1. <span data-ttu-id="f9ff2-120">ในส่วน **วัตถุประสงค์** เลือก **กำหนดวัตถุประสงค์**</span><span class="sxs-lookup"><span data-stu-id="f9ff2-120">In the **Purpose** section, select **Assign purpose**.</span></span>
1. <span data-ttu-id="f9ff2-121">ในรายการนี้ ให้ค้นหาและเลือกเรกคอร์ดที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="f9ff2-121">In the list, find and select the desired record.</span></span> <span data-ttu-id="f9ff2-122">เลือกวัตถุประสงค์เพื่อกำหนดให้กับลำดับชั้นขององค์กรของคุณ</span><span class="sxs-lookup"><span data-stu-id="f9ff2-122">Select a purpose to assign to your organization hierarchy.</span></span>
1. <span data-ttu-id="f9ff2-123">ในส่วน **ลำดับชั้นที่กำหนด** เลือก **เพิ่ม**</span><span class="sxs-lookup"><span data-stu-id="f9ff2-123">In the **Assigned hierarchies** section, select **Add**.</span></span>
1. <span data-ttu-id="f9ff2-124">ในรายการนี้ ให้ทำเครื่องหมายแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="f9ff2-124">In the list, mark the selected row.</span></span> <span data-ttu-id="f9ff2-125">ค้นหาลำดับชั้นที่คุณเพิ่งสร้างขึ้น</span><span class="sxs-lookup"><span data-stu-id="f9ff2-125">Find the hierarchy you just created.</span></span>
1. <span data-ttu-id="f9ff2-126">เลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="f9ff2-126">Select **OK**.</span></span>

<span data-ttu-id="f9ff2-127">รูปภาพต่อไปนี้แสดงตัวอย่างของลำดับชั้นขององค์กรที่สร้างขึ้นสำหรับชุดของร้านค้า "Adventure Works" แบบสมมติ</span><span class="sxs-lookup"><span data-stu-id="f9ff2-127">The following image shows an example organizational hierarchy created for a fictitious "Adventure Works" set of stores.</span></span>

![ตัวอย่างลำดับชั้นขององค์กร](media/organizational-hierarchies.png)

### <a name="add-organizations-to-a-hierarchy"></a><span data-ttu-id="f9ff2-129">เพิ่มองค์กรให้กับลำดับชั้น</span><span class="sxs-lookup"><span data-stu-id="f9ff2-129">Add organizations to a hierarchy</span></span>

<span data-ttu-id="f9ff2-130">หากต้องการเพิ่มองค์กรให้กับลำดับชั้น ให้ทำตามขั้นตอนต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="f9ff2-130">To add organizations to a hierarchy, follow these steps.</span></span>

1. <span data-ttu-id="f9ff2-131">ในรายการนี้ ให้ค้นหาและเลือกเรกคอร์ดที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="f9ff2-131">In the list, find and select the desired record.</span></span> <span data-ttu-id="f9ff2-132">เลือกลำดับชั้นของคุณ</span><span class="sxs-lookup"><span data-stu-id="f9ff2-132">Select your hierarchy.</span></span>
1. <span data-ttu-id="f9ff2-133">บนบานหน้าต่างการดำเนินการ เลือก **ดู**</span><span class="sxs-lookup"><span data-stu-id="f9ff2-133">On the action pane, select **View**.</span></span>
1. <span data-ttu-id="f9ff2-134">เพิ่มองค์กรตามความจำเป็น</span><span class="sxs-lookup"><span data-stu-id="f9ff2-134">Add organizations, as necessary.</span></span>
1. <span data-ttu-id="f9ff2-135">เมื่อต้องการเพิ่มองค์กร ให้เลือก **แก้ไข** และจากนั้นเลือก **แทรก**</span><span class="sxs-lookup"><span data-stu-id="f9ff2-135">To add an organization, select **Edit** and then select **Insert**.</span></span> <span data-ttu-id="f9ff2-136">เมื่อคุณดำเนินการเปลี่ยนแปลงเสร็จสิ้น คุณสามารถบันทึกแบบร่างและเผยแพร่การเปลี่ยนแปลงได้</span><span class="sxs-lookup"><span data-stu-id="f9ff2-136">When you are done making changes you can save a draft and publish the changes.</span></span>

<span data-ttu-id="f9ff2-137">รูปภาพต่อไปนี้แสดงนิติบุคคลที่เพิ่มที่รากลำดับชั้นกับศูนย์ต้นทุนสี่ศูนย์ที่เพิ่มสำหรับช่องทาง "ขนาดเล็ก" "ช่องระบาย" "ออนไลน์" และ "ศูนย์บริการ"</span><span class="sxs-lookup"><span data-stu-id="f9ff2-137">The following image shows a legal entity added at the hierarchy root with four cost centers added for "Mall", "Outlet", "Online" and "Call Center" channels.</span></span> <span data-ttu-id="f9ff2-138">คุณสามารถเพิ่มร้านค้าปลีก ศูนย์บริการ และช่องทางออนไลน์ต่าง ๆ เข้าในแต่ละที่ได้</span><span class="sxs-lookup"><span data-stu-id="f9ff2-138">Various retail, call center and online channels can then be added to each.</span></span>

![ตัวอย่างของตัวออกแบบลำดับชั้น](media/hierarchy-designer.png)

## <a name="additional-resources"></a><span data-ttu-id="f9ff2-140">แหล่งข้อมูลเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="f9ff2-140">Additional resources</span></span>

[<span data-ttu-id="f9ff2-141">ภาพรวมขององค์กรและลำดับชั้นขององค์กร</span><span class="sxs-lookup"><span data-stu-id="f9ff2-141">Organizations and organizational hierarchies overview</span></span>](../fin-ops-core/fin-ops/organization-administration/organizations-organizational-hierarchies.md?toc=/dynamics365/commerce/toc.json)

[<span data-ttu-id="f9ff2-142">วางแผนลำดับชั้นขององค์กรของคุณ</span><span class="sxs-lookup"><span data-stu-id="f9ff2-142">Plan your organizational hierarchy</span></span>](../fin-ops-core/fin-ops/organization-administration/plan-organizational-hierarchy.md?toc=/dynamics365/commerce/toc.json)

[<span data-ttu-id="f9ff2-143">สร้างนิติบุคคล</span><span class="sxs-lookup"><span data-stu-id="f9ff2-143">Create legal entities</span></span>](channels-legal-entities.md)

[<span data-ttu-id="f9ff2-144">สร้างหน่วยปฏิบัติงาน</span><span class="sxs-lookup"><span data-stu-id="f9ff2-144">Create operating units</span></span>](../fin-ops-core/fin-ops/organization-administration/tasks/create-operating-unit.md?toc=/dynamics365/commerce/toc.json)

[<span data-ttu-id="f9ff2-145">ภาพรวมของช่องทาง</span><span class="sxs-lookup"><span data-stu-id="f9ff2-145">Channels overview</span></span>](channels-overview.md)

[<span data-ttu-id="f9ff2-146">ข้อกำหนดเบื้องต้นในการตั้งค่าช่องทาง</span><span class="sxs-lookup"><span data-stu-id="f9ff2-146">Channel setup prerequisites</span></span>](channels-prerequisites.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
