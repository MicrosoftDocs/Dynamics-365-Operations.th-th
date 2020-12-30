---
title: ตั้งค่าคอนฟิกกิจกรรมคู่ขนานในลำดับงาน
description: เมื่อต้องการตั้งค่าคอนฟิกกิจกรรมคู่ขนาน ให้ดำเนินการกระบวนงานในโปรแกรมแก้ไขลำดับงานต่อไปนี้ให้เสร็จสมบูรณ์
author: ChrisGarty
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: sericks
ms.custom: 195753
ms.assetid: 6d0656df-b5af-4001-96e6-6f0fcc44d022
ms.search.region: Global
ms.author: cgarty
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 8043e2854ccc8db0128969ffe36a5517a12c37ac
ms.sourcegitcommit: f5e31c34640add6d40308ac1365cc0ee60e60e24
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 12/08/2020
ms.locfileid: "4693365"
---
# <a name="configure-parallel-activities-in-a-workflow"></a><span data-ttu-id="88339-103">ตั้งค่าคอนฟิกกิจกรรมคู่ขนานในลำดับงาน</span><span class="sxs-lookup"><span data-stu-id="88339-103">Configure parallel activities in a workflow</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="88339-104">เมื่อต้องการตั้งค่าคอนฟิกกิจกรรมคู่ขนาน ให้ดำเนินการกระบวนงานในโปรแกรมแก้ไขลำดับงานต่อไปนี้ให้เสร็จสมบูรณ์</span><span class="sxs-lookup"><span data-stu-id="88339-104">To configure a parallel activity, complete the following procedures in the workflow editor.</span></span>

<span data-ttu-id="88339-105">กิจกรรมคู่ขนานประกอบด้วยสาขาลำดับงานที่รันพร้อมกัน</span><span class="sxs-lookup"><span data-stu-id="88339-105">A parallel activity consists of workflow branches that run at the same time.</span></span>

## <a name="name-a-parallel-activity"></a><span data-ttu-id="88339-106">กำหนดชื่อกิจกรรมคู่ขนาน</span><span class="sxs-lookup"><span data-stu-id="88339-106">Name a parallel activity</span></span>

<span data-ttu-id="88339-107">ทำตามขั้นตอนเหล่านี้ในการป้อนชื่อสำหรับกิจกรรมคู่ขนาน</span><span class="sxs-lookup"><span data-stu-id="88339-107">Follow these steps to enter a name for a parallel activity.</span></span>

1. <span data-ttu-id="88339-108">คลิกขวาที่กิจกรรมคู่ขนาน แล้วคลิก **คุณสมบัติ** เพื่อเปิดแบบฟอร์ม **คุณสมบัติ**</span><span class="sxs-lookup"><span data-stu-id="88339-108">Right-click the parallel activity, and then click **Properties** to open the **Properties** form.</span></span>
2. <span data-ttu-id="88339-109">ในบานหน้าต่างทางซ้าย ให้คลิก **การตั้งค่าพื้นฐาน**</span><span class="sxs-lookup"><span data-stu-id="88339-109">In the left pane, click **Basic Settings**.</span></span>
3. <span data-ttu-id="88339-110">ในฟิลด์ **ชื่อ** ป้อนชื่อเฉพาะสำหรับกิจกรรมคู่ขนาน</span><span class="sxs-lookup"><span data-stu-id="88339-110">In the **Name** field, enter a unique name for the parallel activity.</span></span>
4. <span data-ttu-id="88339-111">คลิก **ปิด**</span><span class="sxs-lookup"><span data-stu-id="88339-111">Click **Close**.</span></span>

## <a name="configure-the-branches-of-a-parallel-activity"></a><span data-ttu-id="88339-112">ตั้งค่าคอนฟิกสาขาของกิจกรรมคู่ขนาน</span><span class="sxs-lookup"><span data-stu-id="88339-112">Configure the branches of a parallel activity</span></span>

<span data-ttu-id="88339-113">ทำตามขั้นตอนเหล่านี้เพื่อเพิ่มและตั้งค่าคอนฟิกสาขาของกิจกรรมคู่ขนานนี้</span><span class="sxs-lookup"><span data-stu-id="88339-113">Follow these steps to add and configure the branches of this parallel activity.</span></span>

1. <span data-ttu-id="88339-114">ดับเบิลคลิกที่กิจกรรมคู่ขนานเพื่อแสดงสาขาของกิจกรรมคู่ขนาน</span><span class="sxs-lookup"><span data-stu-id="88339-114">Double-click the parallel activity to display the branches of the parallel activity.</span></span>
2. <span data-ttu-id="88339-115">เมื่อต้องการเพิ่มสาขา ให้ลากองค์ประกอบ **สาขา** จากพื้นที่ **องค์ประกอบลำดับงาน** ไปยังจุดแทรกบนผืนผ้าใบ</span><span class="sxs-lookup"><span data-stu-id="88339-115">To add a branch, drag the **Branch** element from the **Workflow elements** area to an insertion point on the canvas.</span></span> <span data-ttu-id="88339-116">ภาพต่อไปนี้แสดงจุดแทรก</span><span class="sxs-lookup"><span data-stu-id="88339-116">The following figure shows an insertion point.</span></span>

    ![จุดแทรก](./media/workflow_insertionpoint.gif)

    > [!NOTE]
    > <span data-ttu-id="88339-118">ลำดับของสาขาไม่สำคัญ เพราะสาขาทั้งหมดของกิจกรรมคู่ขนานรันพร้อมกัน</span><span class="sxs-lookup"><span data-stu-id="88339-118">The order of the branches is not important because all the branches of a parallel activity run at the same time.</span></span>

3. <span data-ttu-id="88339-119">การตั้งค่าคอนฟิกแต่ละสาขา ดูที่ [ตั้งค่าคอนฟิกสาขาคู่ขนานในเวิร์กโฟลว์](configure-parallel-branch-workflow.md)</span><span class="sxs-lookup"><span data-stu-id="88339-119">To configure each branch, see [Configure parallel branches in a workflow](configure-parallel-branch-workflow.md).</span></span>
