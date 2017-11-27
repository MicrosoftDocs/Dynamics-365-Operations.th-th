---
title: "ตั้งค่าคอนฟิกสาขาคู่ขนานในลำดับงาน"
description: "เมื่อต้องการตั้งค่าคอนฟิกสาขาคู่ขนาน ให้ดำเนินการกระบวนงานในโปรแกรมแก้ไขลำดับงานต่อไปนี้ให้เสร็จสมบูรณ์"
author: sericks007
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.custom: 196043
ms.assetid: dfdae2b8-6a4f-4760-b339-b755c66f3f89
ms.search.region: Global
ms.author: donaldc
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 41bd03757a347a1b5f189bd50dae2545baaddf20
ms.contentlocale: th-th
ms.lasthandoff: 11/03/2017

---

# <a name="configure-a-parallel-branch-in-a-workflow"></a><span data-ttu-id="bc023-103">ตั้งค่าคอนฟิกสาขาคู่ขนานในลำดับงาน</span><span class="sxs-lookup"><span data-stu-id="bc023-103">Configure a parallel branch in a workflow</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="bc023-104">เมื่อต้องการตั้งค่าคอนฟิกสาขาคู่ขนาน ให้ดำเนินการกระบวนงานในโปรแกรมแก้ไขลำดับงานต่อไปนี้ให้เสร็จสมบูรณ์</span><span class="sxs-lookup"><span data-stu-id="bc023-104">To configure a parallel branch, complete the following procedures in the workflow editor.</span></span>

<span data-ttu-id="bc023-105">โดยพื้นฐานสาขาคู่ขนานคือลำดับงานที่รันในบริบทของลำดับงานหลัก</span><span class="sxs-lookup"><span data-stu-id="bc023-105">A parallel branch is essentially a workflow that runs in the context of a parent workflow.</span></span>

## <a name="name-a-branch"></a><span data-ttu-id="bc023-106">ชื่อสาขา</span><span class="sxs-lookup"><span data-stu-id="bc023-106">Name a branch</span></span>
<span data-ttu-id="bc023-107">ทำตามขั้นตอนเหล่านี้ในการป้อนชื่อสำหรับสาขาคู่ขนาน</span><span class="sxs-lookup"><span data-stu-id="bc023-107">Follow these steps to enter a name for a parallel branch.</span></span>
1.  <span data-ttu-id="bc023-108">คลิกขวาที่สาขาคู่ขนาน แล้วคลิก **คุณสมบัติ**</span><span class="sxs-lookup"><span data-stu-id="bc023-108">Right-click the parallel branch, and then click **Properties**.</span></span> <span data-ttu-id="bc023-109">ปิดใช้งานแบบฟอร์ม **คุณสมบัติ** แล้ว</span><span class="sxs-lookup"><span data-stu-id="bc023-109">The **Properties** form is displayed.</span></span>
2.  <span data-ttu-id="bc023-110">ในบานหน้าต่างทางซ้าย ให้คลิก **การตั้งค่าพื้นฐาน**</span><span class="sxs-lookup"><span data-stu-id="bc023-110">In the left pane, click **Basic Settings**.</span></span>
3.  <span data-ttu-id="bc023-111">ในฟิลด์ **ชื่อ** ป้อนชื่อเฉพาะสำหรับสาขาคู่ขนาน</span><span class="sxs-lookup"><span data-stu-id="bc023-111">In the **Name** field, enter a unique name for the parallel branch.</span></span>
4.  <span data-ttu-id="bc023-112">คลิก **ปิด**</span><span class="sxs-lookup"><span data-stu-id="bc023-112">Click **Close**.</span></span>

## <a name="design-and-configure-the-elements-of-a-branch"></a><span data-ttu-id="bc023-113">ออกแบบและตั้งค่าคอนฟิกองค์ประกอบของสาขา</span><span class="sxs-lookup"><span data-stu-id="bc023-113">Design and configure the elements of a branch</span></span>
<span data-ttu-id="bc023-114">ทำตามขั้นตอนเหล่านี้เพื่อออกแบบตั้งค่าคอนฟิกองค์ประกอบของสาขาคู่ขนาน</span><span class="sxs-lookup"><span data-stu-id="bc023-114">Follow these steps to design and configure the elements of a parallel branch.</span></span>
1.  <span data-ttu-id="bc023-115">ดับเบิลคลิกที่สาขาคู่ขนาน</span><span class="sxs-lookup"><span data-stu-id="bc023-115">Double-click the parallel branch.</span></span>
2.  <span data-ttu-id="bc023-116">ลากองค์ประกอบลำดับงานบนผืนผ้าใบ แล้วตั้งค่าคอนฟิกองค์ประกอบ เช่นเดียวกับการสร้างลำดับงานอื่น</span><span class="sxs-lookup"><span data-stu-id="bc023-116">Drag workflow elements onto the canvas, and then configure the elements, just as you would to create any other workflow.</span></span> <span data-ttu-id="bc023-117">สำหรับข้อมูลเพิ่มเติมให้ดูที่ สร้างลำดับงาน</span><span class="sxs-lookup"><span data-stu-id="bc023-117">For more information, see Create a workflow.</span></span>



<a name="see-also"></a><span data-ttu-id="bc023-118">ดูเพิ่มเติมที่</span><span class="sxs-lookup"><span data-stu-id="bc023-118">See also</span></span>
--------

[<span data-ttu-id="bc023-119">สร้างลำดับงาน</span><span class="sxs-lookup"><span data-stu-id="bc023-119">Create a workflow</span></span>](create-workflow.md)




