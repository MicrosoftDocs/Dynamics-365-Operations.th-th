---
title: เพิ่มช่องทางในลำดับชั้นขององค์กร
description: หัวข้อนี้จะอธิบายวิธีการเพิ่มช่องทางในลำดับชั้นขององค์กรใน Microsoft Dynamics 365 Commerce
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
ms.openlocfilehash: c7ff6d8ee7e526e45975cfa500b5e6d6079054dc
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 03/31/2021
ms.locfileid: "5800698"
---
# <a name="add-a-channel-to-an-organizational-hierarchy"></a><span data-ttu-id="f9bd7-103">เพิ่มช่องทางในลำดับชั้นขององค์กร</span><span class="sxs-lookup"><span data-stu-id="f9bd7-103">Add a channel to an organizational hierarchy</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="f9bd7-104">หัวข้อนี้จะอธิบายวิธีการเพิ่มช่องทางในลำดับชั้นขององค์กรใน Microsoft Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="f9bd7-104">This topic describes how to add a channel to an organizational hierarchy in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="f9bd7-105">ภาพรวม</span><span class="sxs-lookup"><span data-stu-id="f9bd7-105">Overview</span></span>

<span data-ttu-id="f9bd7-106">ช่องทางต้องเชื่อมโยงกับลำดับชั้นขององค์กรหนึ่งลำดับชั้นขึ้นไป</span><span class="sxs-lookup"><span data-stu-id="f9bd7-106">Channels need to be associated with one or more organizational hierarchies.</span></span> <span data-ttu-id="f9bd7-107">ก่อนที่จะสร้างช่องทาง คุณต้องตรวจสอบให้แน่ใจว่าคุณได้ตั้งค่าลำดับชั้นขององค์กรของคุณแล้ว</span><span class="sxs-lookup"><span data-stu-id="f9bd7-107">Before creating channels, you need to confirm that your organizational hierarchies have been set up.</span></span>  

<span data-ttu-id="f9bd7-108">ดู [ลำดับชั้นขององค์กร](channels-org-hierarchies.md) สำหรับรายละเอียดเพิ่มเติมเกี่ยวกับวิธีการสร้างลำดับชั้นขององค์กร</span><span class="sxs-lookup"><span data-stu-id="f9bd7-108">See [Organizational hierarchies](channels-org-hierarchies.md) for more details on how to create organizational hierarchies.</span></span>

## <a name="select-a-hierarchy"></a><span data-ttu-id="f9bd7-109">เลือกลำดับชั้น</span><span class="sxs-lookup"><span data-stu-id="f9bd7-109">Select a hierarchy</span></span>

<span data-ttu-id="f9bd7-110">ในการเลือกลำดับชั้น ให้ดำเนินการตามขั้นตอนเหล่านี้:</span><span class="sxs-lookup"><span data-stu-id="f9bd7-110">To select a hierarchy, follow these steps.</span></span>

1. <span data-ttu-id="f9bd7-111">ในบานหน้าต่างนำทาง ไปที่ **โมดูล \> การขายปลีกและการค้า \> การตั้งค่าช่องทาง \> ลำดับชั้นขององค์กร**</span><span class="sxs-lookup"><span data-stu-id="f9bd7-111">In the navigation pane, go to **Modules \> Retail and commerce \> Channel Setup \> Organization hierarchies**.</span></span>
1. <span data-ttu-id="f9bd7-112">จากรายการ ให้เลือกลำดับชั้นขององค์กรที่คุณจะเพิ่มช่องทางให้</span><span class="sxs-lookup"><span data-stu-id="f9bd7-112">From the list, select the organization hierarchy that you'll be adding the channel to.</span></span>
1. <span data-ttu-id="f9bd7-113">ในบานหน้าต่างการดำเนินการ ให้เลือก **มุมมอง** เพื่อดูรายละเอียดของลำดับชั้น</span><span class="sxs-lookup"><span data-stu-id="f9bd7-113">On the action pane, select **View** to view hierarchy details.</span></span>

<span data-ttu-id="f9bd7-114">รูปภาพต่อไปนี้แสดงรายละเอียดลำดับชั้นขององค์กรสำหรับลำดับชั้นที่เลือก</span><span class="sxs-lookup"><span data-stu-id="f9bd7-114">The following image shows organizational hierarchy details for the selected hierarchy.</span></span>

![รายละเอียดลำดับชั้นขององค์กรสำหรับลำดับชั้นที่เลือก](media/channel-add-to-org-hierarchy-1.png)

## <a name="add-a-channel-to-a-hierachy-node"></a><span data-ttu-id="f9bd7-116">การเพิ่มช่องทางลงในโหนดลำดับชั้น</span><span class="sxs-lookup"><span data-stu-id="f9bd7-116">Add a channel to a hierachy node</span></span>

<span data-ttu-id="f9bd7-117">เมื่อต้องการเพิ่มช่องไปยังโหนดลำดับชั้น ให้ทำตามขั้นตอนเหล่านี้</span><span class="sxs-lookup"><span data-stu-id="f9bd7-117">To add a channel to a hierachy node, follow these steps.</span></span>

1. <span data-ttu-id="f9bd7-118">บนบานหน้าต่างการดำเนินการ เลือก **แก้ไข**</span><span class="sxs-lookup"><span data-stu-id="f9bd7-118">On the action pane, select **Edit**.</span></span>
1. <span data-ttu-id="f9bd7-119">เลือกโหนดลำดับชั้น ที่คุณต้องการเพิ่มช่องทางเข้าไป จากนั้นใน **แทรก** ให้เลือก **ช่องทางการขายปลีก**</span><span class="sxs-lookup"><span data-stu-id="f9bd7-119">Select the hierachy node you want the channel added to, then from the **Insert** drop-down list, select **Retail Channel**.</span></span> 
1. <span data-ttu-id="f9bd7-120">เลือกช่องทางที่จะเพิ่มแล้วเลือกปุ่ม **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="f9bd7-120">Select the channel to add, then select the **OK** button.</span></span>
1. <span data-ttu-id="f9bd7-121">บนบานหน้าต่างการดำเนินการ เลือก **บันทึก**</span><span class="sxs-lookup"><span data-stu-id="f9bd7-121">On the action pane, select **Save**.</span></span>
1. <span data-ttu-id="f9bd7-122">ในบานหน้าต่างการดำเนินการ ให้เลือก **เผยแพร่** และระบุ **วันที่มีผลบังคับใช้** ในอดีตเพื่อให้การดำเนินการนี้เกิดผลทันที</span><span class="sxs-lookup"><span data-stu-id="f9bd7-122">On the action pane, select **Publish** and provide an **Effective date** in the past to have this action go into effect immediately.</span></span>

<span data-ttu-id="f9bd7-123">ภาพต่อไปนี้แสดงวิธีการเลือกช่องทาง เพื่อเพิ่มไปยังโหนดลำดับชั้น</span><span class="sxs-lookup"><span data-stu-id="f9bd7-123">The following image shows how to select a channel to add to a hierarchy node.</span></span>

![เลือกช่องทางเพื่อเพิ่มในโหนดลำดับชั้น](media/channel-add-to-org-hierarchy-2.png)

<span data-ttu-id="f9bd7-125">รูปภาพต่อไปนี้แสดงลำดับชั้นที่มีการเพิ่มช่องทางต่าง ๆ แล้ว</span><span class="sxs-lookup"><span data-stu-id="f9bd7-125">The following image shows a hierarchy with various channels added.</span></span>

![ลำดับชั้นที่มีการเพิ่มช่องทางต่าง ๆ แล้ว](media/channel-add-to-org-hierarchy-3.png)

## <a name="additional-resources"></a><span data-ttu-id="f9bd7-127">แหล่งข้อมูลเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="f9bd7-127">Additional resources</span></span>

[<span data-ttu-id="f9bd7-128">ภาพรวมของช่องทาง</span><span class="sxs-lookup"><span data-stu-id="f9bd7-128">Channels overview</span></span>](channels-overview.md)

[<span data-ttu-id="f9bd7-129">ข้อกำหนดเบื้องต้นในการตั้งค่าช่องทาง</span><span class="sxs-lookup"><span data-stu-id="f9bd7-129">Channel setup prerequisites</span></span>](channels-prerequisites.md)

[<span data-ttu-id="f9bd7-130">ภาพรวมขององค์กรและลำดับชั้นขององค์กร</span><span class="sxs-lookup"><span data-stu-id="f9bd7-130">Organizations and organizational hierarchies overview</span></span>](../fin-ops-core/fin-ops/organization-administration/organizations-organizational-hierarchies.md?toc=/dynamics365/commerce/toc.json)

[<span data-ttu-id="f9bd7-131">วางแผนลำดับชั้นขององค์กรของคุณ</span><span class="sxs-lookup"><span data-stu-id="f9bd7-131">Plan your organizational hierarchy</span></span>](../fin-ops-core/fin-ops/organization-administration/plan-organizational-hierarchy.md?toc=/dynamics365/commerce/toc.json)

[<span data-ttu-id="f9bd7-132">ลำดับชั้นขององค์กร</span><span class="sxs-lookup"><span data-stu-id="f9bd7-132">Organization hierarchies</span></span>](channels-org-hierarchies.md)

[<span data-ttu-id="f9bd7-133">ตั้งค่าช่องทางการขายปลีก</span><span class="sxs-lookup"><span data-stu-id="f9bd7-133">Set up a retail channel</span></span>](channel-setup-retail.md)
    
[<span data-ttu-id="f9bd7-134">ตั้งค่าช่องทางออนไลน์</span><span class="sxs-lookup"><span data-stu-id="f9bd7-134">Set up an online channel</span></span>](channel-setup-online.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]