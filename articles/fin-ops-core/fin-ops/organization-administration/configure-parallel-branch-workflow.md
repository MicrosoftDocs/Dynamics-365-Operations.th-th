---
title: ตั้งค่าคอนฟิกสาขาคู่ขนานในลำดับงาน
description: เมื่อต้องการตั้งค่าคอนฟิกสาขาคู่ขนาน ให้ดำเนินการกระบวนงานในโปรแกรมแก้ไขลำดับงานต่อไปนี้ให้เสร็จสมบูรณ์
author: ChrisGarty
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: sericks
ms.custom: 196043
ms.assetid: dfdae2b8-6a4f-4760-b339-b755c66f3f89
ms.search.region: Global
ms.author: cgarty
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: e67a2c7cde3a3b6d1dcfcc2ccdd3255d30ac40b8
ms.sourcegitcommit: f5e31c34640add6d40308ac1365cc0ee60e60e24
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 12/08/2020
ms.locfileid: "4693341"
---
# <a name="configure-parallel-branches-in-a-workflow"></a><span data-ttu-id="21494-103">ตั้งค่าคอนฟิกสาขาคู่ขนานในลำดับงาน</span><span class="sxs-lookup"><span data-stu-id="21494-103">Configure parallel branches in a workflow</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="21494-104">เมื่อต้องการตั้งค่าคอนฟิกสาขาคู่ขนาน ให้ดำเนินการกระบวนงานในโปรแกรมแก้ไขลำดับงานต่อไปนี้ให้เสร็จสมบูรณ์</span><span class="sxs-lookup"><span data-stu-id="21494-104">To configure a parallel branch, complete the following procedures in the workflow editor.</span></span>

<span data-ttu-id="21494-105">โดยพื้นฐานสาขาคู่ขนานคือลำดับงานที่รันในบริบทของลำดับงานหลัก</span><span class="sxs-lookup"><span data-stu-id="21494-105">A parallel branch is essentially a workflow that runs in the context of a parent workflow.</span></span>

## <a name="name-a-branch"></a><span data-ttu-id="21494-106">ชื่อสาขา</span><span class="sxs-lookup"><span data-stu-id="21494-106">Name a branch</span></span>

<span data-ttu-id="21494-107">ทำตามขั้นตอนเหล่านี้ในการป้อนชื่อสำหรับสาขาคู่ขนาน</span><span class="sxs-lookup"><span data-stu-id="21494-107">Follow these steps to enter a name for a parallel branch.</span></span>

1. <span data-ttu-id="21494-108">คลิกขวาที่สาขาคู่ขนาน แล้วคลิก **คุณสมบัติ**</span><span class="sxs-lookup"><span data-stu-id="21494-108">Right-click the parallel branch, and then click **Properties**.</span></span> <span data-ttu-id="21494-109">ปิดใช้งานแบบฟอร์ม **คุณสมบัติ** แล้ว</span><span class="sxs-lookup"><span data-stu-id="21494-109">The **Properties** form is displayed.</span></span>
2. <span data-ttu-id="21494-110">ในบานหน้าต่างทางซ้าย ให้คลิก **การตั้งค่าพื้นฐาน**</span><span class="sxs-lookup"><span data-stu-id="21494-110">In the left pane, click **Basic Settings**.</span></span>
3. <span data-ttu-id="21494-111">ในฟิลด์ **ชื่อ** ป้อนชื่อเฉพาะสำหรับสาขาคู่ขนาน</span><span class="sxs-lookup"><span data-stu-id="21494-111">In the **Name** field, enter a unique name for the parallel branch.</span></span>
4. <span data-ttu-id="21494-112">คลิก **ปิด**</span><span class="sxs-lookup"><span data-stu-id="21494-112">Click **Close**.</span></span>

## <a name="design-and-configure-the-elements-of-a-branch"></a><span data-ttu-id="21494-113">ออกแบบและตั้งค่าคอนฟิกองค์ประกอบของสาขา</span><span class="sxs-lookup"><span data-stu-id="21494-113">Design and configure the elements of a branch</span></span>

<span data-ttu-id="21494-114">ทำตามขั้นตอนเหล่านี้เพื่อออกแบบตั้งค่าคอนฟิกองค์ประกอบของสาขาคู่ขนาน</span><span class="sxs-lookup"><span data-stu-id="21494-114">Follow these steps to design and configure the elements of a parallel branch.</span></span>

1. <span data-ttu-id="21494-115">ดับเบิลคลิกที่สาขาคู่ขนาน</span><span class="sxs-lookup"><span data-stu-id="21494-115">Double-click the parallel branch.</span></span>
2. <span data-ttu-id="21494-116">ลากองค์ประกอบลำดับงานบนผืนผ้าใบ แล้วตั้งค่าคอนฟิกองค์ประกอบ เช่นเดียวกับการสร้างลำดับงานอื่น</span><span class="sxs-lookup"><span data-stu-id="21494-116">Drag workflow elements onto the canvas, and then configure the elements, just as you would to create any other workflow.</span></span> <span data-ttu-id="21494-117">สำหรับข้อมูลเพิ่มเติม ให้ดูที่ [สร้างภาพรวมลำดับงาน](create-workflow.md)</span><span class="sxs-lookup"><span data-stu-id="21494-117">For more information, see [Create workflows overview](create-workflow.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="21494-118">แหล่งข้อมูลเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="21494-118">Additional resources</span></span>

[<span data-ttu-id="21494-119">ภาพรวมของการสร้างลำดับงาน</span><span class="sxs-lookup"><span data-stu-id="21494-119">Create workflows overview</span></span>](create-workflow.md)
