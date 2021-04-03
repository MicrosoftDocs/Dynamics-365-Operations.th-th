---
title: บันทึกคู่มืองานไปยัง LCS แล้วเล่นซ้ำ
description: บทความนี้อธิบายวิธีการบันทึกคู่มืองานไปยัง Microsoft Dynamics Lifecycle Services (LCS) และจากนั้น เล่นซ้ำ
author: andreabichsel
manager: tfehr
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
ms.openlocfilehash: 7d6102bafc9b55f9eff05bfc4a63c177c6548694
ms.sourcegitcommit: 6affb3316be757c99e1fe9c7c7b312b93c483408
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 02/17/2021
ms.locfileid: "5463273"
---
# <a name="save-task-guides-to-lcs-and-replay-them"></a><span data-ttu-id="ffb18-103">บันทึกคู่มืองานไปยัง LCS แล้วเล่นซ้ำ</span><span class="sxs-lookup"><span data-stu-id="ffb18-103">Save task guides to LCS and replay them</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="ffb18-104">**รายละเอียดสภาพแวดล้อม**</span><span class="sxs-lookup"><span data-stu-id="ffb18-104">**Environment details**</span></span> 

<span data-ttu-id="ffb18-105">Microsoft Dynamics 365 Human Resources ซึ่งถูกปรับใช้ผ่าน Microsoft Dynamics Lifecycle Services (LCS)</span><span class="sxs-lookup"><span data-stu-id="ffb18-105">Microsoft Dynamics 365 Human Resources, which was deployed via Microsoft Dynamics Lifecycle Services (LCS)</span></span>

<span data-ttu-id="ffb18-106">**ออกใช้**</span><span class="sxs-lookup"><span data-stu-id="ffb18-106">**Issue**</span></span>

<span data-ttu-id="ffb18-107">ลูกค้าต้องการบันทึกการบันทึกภารกิจใหม่ไปยังโครงการ LCS ของเขาหรือเธอ และจากนั้นเล่นซ้ำคู่มืองานที่บันทึกไว้</span><span class="sxs-lookup"><span data-stu-id="ffb18-107">The customer wants to save new task recordings to his or her LCS project, and then replay the saved task guides.</span></span>

<span data-ttu-id="ffb18-108">**การแก้ปัญหา**</span><span class="sxs-lookup"><span data-stu-id="ffb18-108">**Resolution**</span></span>

<span data-ttu-id="ffb18-109">ทำตามขั้นตอนเหล่านี้เพื่อบันทึกการบันทึกงานไปยัง LCS</span><span class="sxs-lookup"><span data-stu-id="ffb18-109">Follow these steps to save a task recording to LCS.</span></span>

1. <span data-ttu-id="ffb18-110">ลงชื่อเข้าใช้ไปยัง LCS และเลือกโครงการ</span><span class="sxs-lookup"><span data-stu-id="ffb18-110">Sign in to LCS, and select the project.</span></span>
2. <span data-ttu-id="ffb18-111">เลือกไทล์ **ตัวทำแบบจำลองกระบวนการทางธุรกิจ**</span><span class="sxs-lookup"><span data-stu-id="ffb18-111">Select the **Business process modeler** tile.</span></span>
3. <span data-ttu-id="ffb18-112">ดูหน้าใน "ประสบการณ์ BPM ที่ปรับปรุงแล้ว"</span><span class="sxs-lookup"><span data-stu-id="ffb18-112">View the page in the "Updated BPM experience."</span></span>
4. <span data-ttu-id="ffb18-113">เลือกไลบรารี และจากนั้น เลือก **คัดลอก**</span><span class="sxs-lookup"><span data-stu-id="ffb18-113">Select a library, and then select **Copy**.</span></span>
5. <span data-ttu-id="ffb18-114">ป้อนชื่อสำหรับตัวทำแบบจำลองกระบวนการทางธุรกิจ (BPM)</span><span class="sxs-lookup"><span data-stu-id="ffb18-114">Enter a name for the Business process modeler (BPM) model.</span></span>
6. <span data-ttu-id="ffb18-115">ลงชื่อเข้าใช้ทรัพยากรบุคคลจาก LCS</span><span class="sxs-lookup"><span data-stu-id="ffb18-115">Sign in to Human Resources from LCS.</span></span>
7. <span data-ttu-id="ffb18-116">ในฟิลด์ **การค้นหา** ป้อน **วิธีใช้**</span><span class="sxs-lookup"><span data-stu-id="ffb18-116">In the **Search** field, enter **help**.</span></span> <span data-ttu-id="ffb18-117">วิธีใช้ Lifecycle Services ถูกเปิด</span><span class="sxs-lookup"><span data-stu-id="ffb18-117">Lifecycle Services Help is opened.</span></span>
8. <span data-ttu-id="ffb18-118">เลือกปุ่ม **รีเฟรช** สำหรับการตั้งค่าคอนฟิกวิธีใช้ Lifecycle Services</span><span class="sxs-lookup"><span data-stu-id="ffb18-118">Select the **Refresh** button for Lifecycle Services Help configuration.</span></span>

    <span data-ttu-id="ffb18-119">ไลบรารี BPM ใหม่ของคุณ ควรปรากฏอยู่ และควรถูกเปิดใช้งาน</span><span class="sxs-lookup"><span data-stu-id="ffb18-119">Your new BPM library should appear, and it should be active.</span></span>

9. <span data-ttu-id="ffb18-120">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="ffb18-120">Close the page.</span></span>
10. <span data-ttu-id="ffb18-121">สร้างการบันทึกงาน</span><span class="sxs-lookup"><span data-stu-id="ffb18-121">Create a task recording.</span></span>
11. <span data-ttu-id="ffb18-122">เมื่อคุณทำเสร็จสิ้น เลือก **บันทึกไปยัง Lifecycle Services**</span><span class="sxs-lookup"><span data-stu-id="ffb18-122">When you've finished, select **Save to Lifecycle Services**.</span></span>

    ![บันทึกไปยัง Lifecycle Services](media/task-guides.png)

12. <span data-ttu-id="ffb18-124">เลือกไลบรารี BPM และโหนดเพื่อบันทึกการบันทึกงาน</span><span class="sxs-lookup"><span data-stu-id="ffb18-124">Select the BPM library and node to save the task recording to.</span></span>

<span data-ttu-id="ffb18-125">ทำตามขั้นตอนเหล่านี้เพื่อเล่นซ้ำการบันทึกงานจาก LCS</span><span class="sxs-lookup"><span data-stu-id="ffb18-125">Follow these steps to replay a task guide from LCS.</span></span>

1. <span data-ttu-id="ffb18-126">เริ่มต้นตัวบันทึกงาน</span><span class="sxs-lookup"><span data-stu-id="ffb18-126">Start Task recorder.</span></span>
2. <span data-ttu-id="ffb18-127">เลือก **เปิดจาก LCS**</span><span class="sxs-lookup"><span data-stu-id="ffb18-127">Select **Open from LCS**.</span></span>
3. <span data-ttu-id="ffb18-128">เลือกไลบรารีและโหนด BPM ที่มีคู่มืองานที่บันทึกไว้</span><span class="sxs-lookup"><span data-stu-id="ffb18-128">Select the library and the BPM node that have the saved task guide.</span></span>
4. <span data-ttu-id="ffb18-129">เปิดคู่มืองาน</span><span class="sxs-lookup"><span data-stu-id="ffb18-129">Open the task guide.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]