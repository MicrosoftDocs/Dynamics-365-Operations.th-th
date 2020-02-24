---
title: บันทึกคู่มืองานไปยัง LCS แล้วเล่นซ้ำ
description: บทความนี้อธิบายวิธีการบันทึกคู่มืองานไปยัง Microsoft Dynamics Lifecycle Services (LCS) และจากนั้น เล่นซ้ำ
author: andreabichsel
manager: AnnBe
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-human-resources
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: b55937c0867117809471f50f1987f7bf12a4b25d
ms.sourcegitcommit: 40163705a134c9874fd33be80c7ae59ccce22c21
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 02/03/2020
ms.locfileid: "3010802"
---
# <a name="save-task-guides-to-lcs-and-replay-them"></a><span data-ttu-id="6bf5c-103">บันทึกคู่มืองานไปยัง LCS แล้วเล่นซ้ำ</span><span class="sxs-lookup"><span data-stu-id="6bf5c-103">Save task guides to LCS and replay them</span></span>

<span data-ttu-id="6bf5c-104">**รายละเอียดสภาพแวดล้อม**</span><span class="sxs-lookup"><span data-stu-id="6bf5c-104">**Environment details**</span></span> 

<span data-ttu-id="6bf5c-105">Microsoft Dynamics 365 Human Resources ซึ่งถูกปรับใช้ผ่าน Microsoft Dynamics Lifecycle Services (LCS)</span><span class="sxs-lookup"><span data-stu-id="6bf5c-105">Microsoft Dynamics 365 Human Resources, which was deployed via Microsoft Dynamics Lifecycle Services (LCS)</span></span>

<span data-ttu-id="6bf5c-106">**ออกใช้**</span><span class="sxs-lookup"><span data-stu-id="6bf5c-106">**Issue**</span></span>

<span data-ttu-id="6bf5c-107">ลูกค้าต้องการบันทึกการบันทึกภารกิจใหม่ไปยังโครงการ LCS ของเขาหรือเธอ และจากนั้นเล่นซ้ำคู่มืองานที่บันทึกไว้</span><span class="sxs-lookup"><span data-stu-id="6bf5c-107">The customer wants to save new task recordings to his or her LCS project, and then replay the saved task guides.</span></span>

<span data-ttu-id="6bf5c-108">**การแก้ปัญหา**</span><span class="sxs-lookup"><span data-stu-id="6bf5c-108">**Resolution**</span></span>

<span data-ttu-id="6bf5c-109">ทำตามขั้นตอนเหล่านี้เพื่อบันทึกการบันทึกงานไปยัง LCS</span><span class="sxs-lookup"><span data-stu-id="6bf5c-109">Follow these steps to save a task recording to LCS.</span></span>

1. <span data-ttu-id="6bf5c-110">ลงชื่อเข้าใช้ไปยัง LCS และเลือกโครงการ</span><span class="sxs-lookup"><span data-stu-id="6bf5c-110">Sign in to LCS, and select the project.</span></span>
2. <span data-ttu-id="6bf5c-111">เลือกไทล์ **ตัวทำแบบจำลองกระบวนการทางธุรกิจ**</span><span class="sxs-lookup"><span data-stu-id="6bf5c-111">Select the **Business process modeler** tile.</span></span>
3. <span data-ttu-id="6bf5c-112">ดูหน้าใน "ประสบการณ์ BPM ที่ปรับปรุงแล้ว"</span><span class="sxs-lookup"><span data-stu-id="6bf5c-112">View the page in the "Updated BPM experience."</span></span>
4. <span data-ttu-id="6bf5c-113">เลือกไลบรารี และจากนั้น เลือก **คัดลอก**</span><span class="sxs-lookup"><span data-stu-id="6bf5c-113">Select a library, and then select **Copy**.</span></span>
5. <span data-ttu-id="6bf5c-114">ป้อนชื่อสำหรับตัวทำแบบจำลองกระบวนการทางธุรกิจ (BPM)</span><span class="sxs-lookup"><span data-stu-id="6bf5c-114">Enter a name for the Business process modeler (BPM) model.</span></span>
6. <span data-ttu-id="6bf5c-115">ลงชื่อเข้าใช้ทรัพยากรบุคคลจาก LCS</span><span class="sxs-lookup"><span data-stu-id="6bf5c-115">Sign in to Human Resources from LCS.</span></span>
7. <span data-ttu-id="6bf5c-116">ในฟิลด์ **การค้นหา** ป้อน **วิธีใช้**</span><span class="sxs-lookup"><span data-stu-id="6bf5c-116">In the **Search** field, enter **help**.</span></span> <span data-ttu-id="6bf5c-117">วิธีใช้ Lifecycle Services ถูกเปิด</span><span class="sxs-lookup"><span data-stu-id="6bf5c-117">Lifecycle Services Help is opened.</span></span>
8. <span data-ttu-id="6bf5c-118">เลือกปุ่ม **รีเฟรช** สำหรับการตั้งค่าคอนฟิกวิธีใช้ Lifecycle Services</span><span class="sxs-lookup"><span data-stu-id="6bf5c-118">Select the **Refresh** button for Lifecycle Services Help configuration.</span></span>

    <span data-ttu-id="6bf5c-119">ไลบรารี BPM ใหม่ของคุณ ควรปรากฏอยู่ และควรถูกเปิดใช้งาน</span><span class="sxs-lookup"><span data-stu-id="6bf5c-119">Your new BPM library should appear, and it should be active.</span></span>

9. <span data-ttu-id="6bf5c-120">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="6bf5c-120">Close the page.</span></span>
10. <span data-ttu-id="6bf5c-121">สร้างการบันทึกงาน</span><span class="sxs-lookup"><span data-stu-id="6bf5c-121">Create a task recording.</span></span>
11. <span data-ttu-id="6bf5c-122">เมื่อคุณทำเสร็จสิ้น เลือก **บันทึกไปยัง Lifecycle Services**</span><span class="sxs-lookup"><span data-stu-id="6bf5c-122">When you've finished, select **Save to Lifecycle Services**.</span></span>

    ![บันทึกไปยัง Lifecycle Services](media/task-guides.png)

12. <span data-ttu-id="6bf5c-124">เลือกไลบรารี BPM และโหนดเพื่อบันทึกการบันทึกงาน</span><span class="sxs-lookup"><span data-stu-id="6bf5c-124">Select the BPM library and node to save the task recording to.</span></span>

<span data-ttu-id="6bf5c-125">ทำตามขั้นตอนเหล่านี้เพื่อเล่นซ้ำการบันทึกงานจาก LCS</span><span class="sxs-lookup"><span data-stu-id="6bf5c-125">Follow these steps to replay a task guide from LCS.</span></span>

1. <span data-ttu-id="6bf5c-126">เริ่มต้นตัวบันทึกงาน</span><span class="sxs-lookup"><span data-stu-id="6bf5c-126">Start Task recorder.</span></span>
2. <span data-ttu-id="6bf5c-127">เลือก **เปิดจาก LCS**</span><span class="sxs-lookup"><span data-stu-id="6bf5c-127">Select **Open from LCS**.</span></span>
3. <span data-ttu-id="6bf5c-128">เลือกไลบรารีและโหนด BPM ที่มีคู่มืองานที่บันทึกไว้</span><span class="sxs-lookup"><span data-stu-id="6bf5c-128">Select the library and the BPM node that have the saved task guide.</span></span>
4. <span data-ttu-id="6bf5c-129">เปิดคู่มืองาน</span><span class="sxs-lookup"><span data-stu-id="6bf5c-129">Open the task guide.</span></span>
