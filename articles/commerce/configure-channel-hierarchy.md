---
title: ตั้งค่าคอนฟิกช่องทางเพื่อใช้ลำดับชั้นการนำทางของช่องทาง
description: หัวข้อนี้จะอธิบายวิธีการตั้งค่าคอนฟิกช่องทางเพื่อใช้ลำดับชั้นการนำทางของช่องทางใน Microsoft Dynamics 365 Commerce
author: samjarawan
manager: annbe
ms.date: 01/27/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: samjar
ms.search.validFrom: 2020-01-20
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: 3dcba743e6557b1bd366ac79ecb49ead831dceb4
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 01/15/2021
ms.locfileid: "5001036"
---
# <a name="configure-a-channel-to-use-a-channel-navigation-hierarchy"></a><span data-ttu-id="9875c-103">ตั้งค่าคอนฟิกช่องทางเพื่อใช้ลำดับชั้นการนำทางของช่องทาง</span><span class="sxs-lookup"><span data-stu-id="9875c-103">Configure a channel to use a channel navigation hierarchy</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="9875c-104">หัวข้อนี้จะอธิบายวิธีการตั้งค่าคอนฟิกช่องทางเพื่อใช้ลำดับชั้นการนำทางของช่องทางใน Microsoft Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="9875c-104">This topic describes how to configure a channel to use a channel navigation hierarchy in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="9875c-105">ภาพรวม</span><span class="sxs-lookup"><span data-stu-id="9875c-105">Overview</span></span>

<span data-ttu-id="9875c-106">ลำดับชั้นการนำทางช่องทางจัดระเบียบผลิตภัณฑ์ให้เป็นประเภท เพื่อให้สามารถเรียกดูผลิตภัณฑ์บนไซต์อีคอมเมิร์ซหรือที่จุดขาย (POS)</span><span class="sxs-lookup"><span data-stu-id="9875c-106">Channel navigation hierarchies organize products into categories so that the products can be browsed on an e-Commerce site or at points of sale (POS).</span></span> <span data-ttu-id="9875c-107">ต้องมีการตั้งค่าคอนฟิกช่องทาง Retail และออนไลน์ด้วยลำดับชั้นการนำทางช่องทาง</span><span class="sxs-lookup"><span data-stu-id="9875c-107">Retail and online channels must be configured with channel navigation hierarchies.</span></span>

## <a name="configure-the-channel"></a><span data-ttu-id="9875c-108">ตั้งค่าคอนฟิกช่องทาง</span><span class="sxs-lookup"><span data-stu-id="9875c-108">Configure the channel</span></span>

<span data-ttu-id="9875c-109">ในการตั้งค่าคอนฟิกช่องทางเพื่อใช้ลำดับชั้นการนำทางของช่องทาง ให้ทำตามขั้นตอนเหล่านี้</span><span class="sxs-lookup"><span data-stu-id="9875c-109">To configure a channel to use a channel navigation hierarchy, follow these steps.</span></span>

1. <span data-ttu-id="9875c-110">ในบานหน้าต่างนำทาง ไปยัง **โมดูล \> Retail และการค้า \> การตั้งค่าช่องทาง \> ประเภทช่องทางและคุณลักษณะของผลิตภัณฑ์**</span><span class="sxs-lookup"><span data-stu-id="9875c-110">In the navigation pane, go to **Modules \> Retail and commerce \> Channel setup \> Channel categories and product attributes**.</span></span>
1. <span data-ttu-id="9875c-111">เลือกช่องทางเพื่อตั้งค่าคอนฟิก</span><span class="sxs-lookup"><span data-stu-id="9875c-111">Select the channel to configure.</span></span>
1. <span data-ttu-id="9875c-112">บนบานหน้าต่างการดำเนินการ เลือก **ตั้งค่าข้อมูลเมตาของแอททริบิวต์**</span><span class="sxs-lookup"><span data-stu-id="9875c-112">On the action pane, select **Set attribute metadata**.</span></span>
1. <span data-ttu-id="9875c-113">ในรายการแบบหล่นลง **การจัดประเภทตามลำดับชั้น** ให้เลือกลำดับชั้นการนำทางช่องทางที่เหมาะสม</span><span class="sxs-lookup"><span data-stu-id="9875c-113">In the **Category hierarchy** drop-down list, select the appropriate channel navigation hierarchy.</span></span>
1. <span data-ttu-id="9875c-114">บนบานหน้าต่างการดำเนินการ เลือก **บันทึก**</span><span class="sxs-lookup"><span data-stu-id="9875c-114">On the action pane, select **Save**.</span></span>
1. <span data-ttu-id="9875c-115">ภายใต้ **กลุ่มแอตทริบิวต์** ให้เพิ่มกลุ่มแอตทริบิวต์ใดๆ ที่จะเป็นแอตทริบิวต์ส่วนกลางสำหรับโหนดทั้งหมด</span><span class="sxs-lookup"><span data-stu-id="9875c-115">Under **Attribute group**, add any attribute groups that will be global attributes for all nodes.</span></span>

<span data-ttu-id="9875c-116">ภาพต่อไปนี้แสดงวิธีการตั้งค่าคอนฟิกช่องทางเพื่อใช้ลำดับชั้นการนำทางของช่องทาง</span><span class="sxs-lookup"><span data-stu-id="9875c-116">The following image shows how to configure a channel to use a channel navigation hierarchy.</span></span>

![การตั้งค่าคอนฟิกช่องทางตัวอย่าง](media/configure-channel-hierarchy-1.png)

## <a name="set-attribute-metadata"></a><span data-ttu-id="9875c-118">ตั้งค่าข้อมูลเมตาของแอททริบิวต์</span><span class="sxs-lookup"><span data-stu-id="9875c-118">Set attribute metadata</span></span>

<span data-ttu-id="9875c-119">การตั้งค่าข้อมูลเมตาของแอตทริบิวต์จะอนุญาตการตั้งค่าคอนฟิกของแอตทริบิวต์บนโหนดแต่ละโหนด</span><span class="sxs-lookup"><span data-stu-id="9875c-119">Setting the attribute metadata will allow configuration of attributes on each node.</span></span>

<span data-ttu-id="9875c-120">หากต้องการตั้งค่าข้อมูลเมตาของแอตทริบิวต์ ให้ดำเนินการตามขั้นตอนเหล่านี้</span><span class="sxs-lookup"><span data-stu-id="9875c-120">To set attribute metadata, follow these steps.</span></span>

1. <span data-ttu-id="9875c-121">บนบานหน้าต่างการดำเนินการ เลือก **ตั้งค่าข้อมูลเมตาของแอททริบิวต์**</span><span class="sxs-lookup"><span data-stu-id="9875c-121">On the action pane, select **Set attribute metadata**.</span></span>
1. <span data-ttu-id="9875c-122">สำหรับโหนดแต่ละโหนด เลือก **แอตทริบิวต์ของผลิตภัณฑ์ช่องทาง**</span><span class="sxs-lookup"><span data-stu-id="9875c-122">For each node select **Channel product attributes**.</span></span>
1. <span data-ttu-id="9875c-123">ตั้งค่า **แสดงแอตทริบิวต์บนช่องทาง** เป็น **ใช่** และ **สามารถจำกัดได้** เป็น **ใช่** เพื่อเปิดใช้งานผู้ปรับปรุงบนช่องสัญญาณนั้น</span><span class="sxs-lookup"><span data-stu-id="9875c-123">Set **Show attribute on channel** to **Yes** and **Can be refined** to **Yes**, to enable refiners on that channel.</span></span>
1. <span data-ttu-id="9875c-124">หลังจากการตั้งค่าคอนฟิกโหนดแต่ละโหนดตามต้องการ **บานหน้าต่างการดำเนินการ** เลือกปุ่ม **บันทึก** เพื่อบันทึก</span><span class="sxs-lookup"><span data-stu-id="9875c-124">After configuring each node as desired, on the **Action pane**, select the **Save** button to save.</span></span>
1. <span data-ttu-id="9875c-125">เลือก **X** ที่มุมขวาบนเพื่อออกจากหน้าจอนี้ กลับไปที่หน้า **ประเภทช่องทางและคุณลักษณะของผลิตภัณฑ์**</span><span class="sxs-lookup"><span data-stu-id="9875c-125">Select the **X** in the top right corner to exit this screen back to the **Channel categories and product attributes** page.</span></span>

<span data-ttu-id="9875c-126">รูปภาพต่อไปนี้แสดงชุดตัวอย่างของคุณลักษณะของผลิตภัณฑ์ช่องทางที่ตั้งค่าคอนฟิกบนโหนดประเภทของช่องทาง</span><span class="sxs-lookup"><span data-stu-id="9875c-126">The following image shows an example set of channel product attributes configured on a channel category node.</span></span>

![แอตทริบิวต์ช่องทางบนโหนดประเภทของช่องทาง](media/configure-channel-hierarchy-2.png)

## <a name="publish-changes"></a><span data-ttu-id="9875c-128">เผยแพร่การเปลี่ยนแปลง</span><span class="sxs-lookup"><span data-stu-id="9875c-128">Publish changes</span></span>

<span data-ttu-id="9875c-129">เพื่อให้การเปลี่ยนแปลงของคุณมีผล คุณจะต้องเผยแพร่การเปลี่ยนแปลง</span><span class="sxs-lookup"><span data-stu-id="9875c-129">For changes to take effect, you will need to publish the changes.</span></span>

<span data-ttu-id="9875c-130">หากต้องการเผยแพร่การเปลี่ยนแปลง ทำตามขั้นตอนเหล่านี้</span><span class="sxs-lookup"><span data-stu-id="9875c-130">To publish changes, follow these steps.</span></span>

1. <span data-ttu-id="9875c-131">บนบานหน้าต่างการดำเนินการ ให้เลือก **เผยแพร่การปรับปรุงช่องทาง**</span><span class="sxs-lookup"><span data-stu-id="9875c-131">On the action pane, select **Publish channel updates**.</span></span>
1. <span data-ttu-id="9875c-132">ในบานหน้าต่าง **เผยแพร่การปรับปรุงช่องทาง** เลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="9875c-132">In the **Publish channel updates** pane, select **OK**.</span></span>

<span data-ttu-id="9875c-133">รูปภาพต่อไปนี้แสดงวิธีการเผยแพร่การปรับปรุงช่องทาง</span><span class="sxs-lookup"><span data-stu-id="9875c-133">The following image shows how to publish channel updates.</span></span>

![เผยแพร่การอัพเดตช่องทาง](media/configure-channel-hierarchy-3.png)

## <a name="additional-resources"></a><span data-ttu-id="9875c-135">แหล่งข้อมูลเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="9875c-135">Additional resources</span></span>

[<span data-ttu-id="9875c-136">สร้างลำดับชั้นการนำทางของช่องทาง</span><span class="sxs-lookup"><span data-stu-id="9875c-136">Create a channel navigation hierarchy</span></span>](create-channel-hierarchy.md)


