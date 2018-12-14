---
title: "บันทึกคู่มืองานไปยัง LCS และเล่นซ้ำ"
description: "หัวข้อนี้อธิบายวิธีการบันทึกคู่มืองานไปยัง Microsoft Dynamics Lifecycle Services (LCS) และจากนั้นเล่นซ้ำ"
author: Darinkramer
manager: AnnBe
ms.date: 11/02/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-365-talent
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Talent
ms.custom: 
ms.assetid: 
ms.search.region: Global
ms.author: dkrame
ms.search.validFrom: 2018-11-02
ms.dyn365.ops.version: Talent
ms.translationtype: HT
ms.sourcegitcommit: d3f974f94b6c327fd70b8098d24f9e1f1e1e8eeb
ms.openlocfilehash: 40b4c3154a04a557b8a670e1f1ae3722c71122fe
ms.contentlocale: th-th
ms.lasthandoff: 12/04/2018

---

# <a name="save-task-guides-to-lcs-and-replay-them"></a><span data-ttu-id="a350c-103">บันทึกคู่มืองานไปยัง LCS และเล่นซ้ำ</span><span class="sxs-lookup"><span data-stu-id="a350c-103">Save task guides to LCS and replay them</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="a350c-104">**รายละเอียดสภาพแวดล้อม**</span><span class="sxs-lookup"><span data-stu-id="a350c-104">**Environment details**</span></span> 

<span data-ttu-id="a350c-105">Microsoft Dynamics 365 for Talent ที่ถูกปรับใช้ผ่านทาง Microsoft Dynamics Lifecycle Services (LCS)</span><span class="sxs-lookup"><span data-stu-id="a350c-105">Microsoft Dynamics 365 for Talent, which was deployed via Microsoft Dynamics Lifecycle Services (LCS)</span></span>

<span data-ttu-id="a350c-106">**ออก**</span><span class="sxs-lookup"><span data-stu-id="a350c-106">**Issue**</span></span>

<span data-ttu-id="a350c-107">ลูกค้าต้องการบันทึกการบันทึกภารกิจใหม่ไปยังโครงการ LCS ของเขาหรือเธอ และจากนั้นเล่นซ้ำคู่มืองานที่บันทึกไว้</span><span class="sxs-lookup"><span data-stu-id="a350c-107">The customer wants to save new task recordings to his or her LCS project, and then replay the saved task guides.</span></span>

<span data-ttu-id="a350c-108">**การแก้ปัญหา**</span><span class="sxs-lookup"><span data-stu-id="a350c-108">**Resolution**</span></span>

<span data-ttu-id="a350c-109">ทำตามขั้นตอนเหล่านี้เพื่อบันทึกการบันทึกงานไปยัง LCS</span><span class="sxs-lookup"><span data-stu-id="a350c-109">Follow these steps to save a task recording to LCS.</span></span>

1. <span data-ttu-id="a350c-110">ลงชื่อเข้าใช้ไปยัง LCS และเลือกโครงการ</span><span class="sxs-lookup"><span data-stu-id="a350c-110">Sign in to LCS, and select the project.</span></span>
2. <span data-ttu-id="a350c-111">เลือกไทล์ **ตัวทำแบบจำลองกระบวนการทางธุรกิจ**</span><span class="sxs-lookup"><span data-stu-id="a350c-111">Select the **Business process modeler** tile.</span></span>
3. <span data-ttu-id="a350c-112">ดูหน้าใน "ประสบการณ์ BPM ที่ปรับปรุงแล้ว"</span><span class="sxs-lookup"><span data-stu-id="a350c-112">View the page in the "Updated BPM experience."</span></span>
4. <span data-ttu-id="a350c-113">เลือกไลบรารี และจากนั้น เลือก **คัดลอก**</span><span class="sxs-lookup"><span data-stu-id="a350c-113">Select a library, and then select **Copy**.</span></span>
5. <span data-ttu-id="a350c-114">ป้อนชื่อสำหรับตัวทำแบบจำลองกระบวนการทางธุรกิจ (BPM)</span><span class="sxs-lookup"><span data-stu-id="a350c-114">Enter a name for the Business process modeler (BPM) model.</span></span>
6. <span data-ttu-id="a350c-115">ลงชื่อเข้าใช้ใน Talent จาก LCS</span><span class="sxs-lookup"><span data-stu-id="a350c-115">Sign in to Talent from LCS.</span></span>
7. <span data-ttu-id="a350c-116">ในฟิลด์ **การค้นหา** ป้อน **วิธีใช้**</span><span class="sxs-lookup"><span data-stu-id="a350c-116">In the **Search** field, enter **help**.</span></span> <span data-ttu-id="a350c-117">วิธีใช้ Lifecycle Services ถูกเปิด</span><span class="sxs-lookup"><span data-stu-id="a350c-117">Lifecycle Services Help is opened.</span></span>
8. <span data-ttu-id="a350c-118">เลือกปุ่ม **รีเฟรช** สำหรับการตั้งค่าคอนฟิกวิธีใช้ Lifecycle Services</span><span class="sxs-lookup"><span data-stu-id="a350c-118">Select the **Refresh** button for Lifecycle Services Help configuration.</span></span>

    <span data-ttu-id="a350c-119">ไลบรารี BPM ใหม่ของคุณ ควรปรากฏอยู่ และควรถูกเปิดใช้งาน</span><span class="sxs-lookup"><span data-stu-id="a350c-119">Your new BPM library should appear, and it should be active.</span></span>

9. <span data-ttu-id="a350c-120">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="a350c-120">Close the page.</span></span>
10. <span data-ttu-id="a350c-121">สร้างการบันทึกงาน</span><span class="sxs-lookup"><span data-stu-id="a350c-121">Create a task recording.</span></span>
11. <span data-ttu-id="a350c-122">เมื่อคุณทำเสร็จสิ้น เลือก **บันทึกไปยัง Lifecycle Services**</span><span class="sxs-lookup"><span data-stu-id="a350c-122">When you've finished, select **Save to Lifecycle Services**.</span></span>

    ![บันทึกไปยัง Lifecycle Services](media/task-guides.png)

12. <span data-ttu-id="a350c-124">เลือกไลบรารี BPM และโหนดเพื่อบันทึกการบันทึกงาน</span><span class="sxs-lookup"><span data-stu-id="a350c-124">Select the BPM library and node to save the task recording to.</span></span>

<span data-ttu-id="a350c-125">ทำตามขั้นตอนเหล่านี้เพื่อเล่นซ้ำการบันทึกงานจาก LCS</span><span class="sxs-lookup"><span data-stu-id="a350c-125">Follow these steps to replay a task guide from LCS.</span></span>

1. <span data-ttu-id="a350c-126">เริ่มต้นตัวบันทึกงาน</span><span class="sxs-lookup"><span data-stu-id="a350c-126">Start Task recorder.</span></span>
2. <span data-ttu-id="a350c-127">เลือก **เปิดจาก LCS**</span><span class="sxs-lookup"><span data-stu-id="a350c-127">Select **Open from LCS**.</span></span>
3. <span data-ttu-id="a350c-128">เลือกไลบรารีและโหนด BPM ที่มีคู่มืองานที่บันทึกไว้</span><span class="sxs-lookup"><span data-stu-id="a350c-128">Select the library and the BPM node that have the saved task guide.</span></span>
4. <span data-ttu-id="a350c-129">เปิดคู่มืองาน</span><span class="sxs-lookup"><span data-stu-id="a350c-129">Open the task guide.</span></span>

