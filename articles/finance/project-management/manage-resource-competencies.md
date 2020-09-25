---
title: จัดการความสามารถของทรัพยากร
description: หัวข้อนี้แสดงข้อมูลเกี่ยวกับการตั้งค่าความสามารถสำหรับทรัพยากรโครงการ
author: Yowelle
manager: AnnBe
ms.date: 09/01/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProjProjectsListPage
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 82022
ms.assetid: bd2fb375-84c6-428a-8e54-f0f719045898
ms.search.region: Global
ms.author: knelson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 877317886e0c0480339eb308d15d1b2099323c56
ms.sourcegitcommit: 241ada0945c72d769eaa70ae35aedbb6a3233fdf
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 09/02/2020
ms.locfileid: "3760670"
---
# <a name="manage-resource-competencies"></a><span data-ttu-id="4d1c0-103">จัดการความสามารถของทรัพยากร</span><span class="sxs-lookup"><span data-stu-id="4d1c0-103">Manage resource competencies</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="4d1c0-104">ความสามารถของทรัพยากรคือส่วนที่สำคัญของการจัดการทรัพยากร</span><span class="sxs-lookup"><span data-stu-id="4d1c0-104">Resource competencies are an essential part of resource management.</span></span> <span data-ttu-id="4d1c0-105">ความสามารถสามารถถูกใช้เป็นพื้นฐานในการกำหนดทรัพยากรที่มียอดดุลที่ถูกต้องของทักษะ การศึกษา ใบรับรอง และประสบการณ์โครงการ </span><span class="sxs-lookup"><span data-stu-id="4d1c0-105">Competencies can be used as a baseline to determine resources that have the correct balance of skills, education, certification, and project experience.</span></span> <span data-ttu-id="4d1c0-106">คุณควรตั้งค่าข้อมูลนี้สำหรับทรัพยากรแต่ละรายการ และอัปเดตเป็นประจำ</span><span class="sxs-lookup"><span data-stu-id="4d1c0-106">You should set up this information for each resource and update it on a regular basis.</span></span> <span data-ttu-id="4d1c0-107">ด้วยวิธีนี้ คุณสามารถขยายความสามารถ เมื่อความสามารถของทรัพยากรที่ระบุถูกจับคู่ในระหว่างการกำหนดทรัพยากรโครงการ</span><span class="sxs-lookup"><span data-stu-id="4d1c0-107">In this way, you can maximize capabilities when specific resource competencies are matched during project resource assignment.</span></span>

<span data-ttu-id="4d1c0-108">[![ตัวอย่างของทักษะ ใบรับรอง การศึกษา และประสบการณ์โครงการ](./media/projectresourcing06-1024x383.jpg)](./media/projectresourcing06.jpg)</span><span class="sxs-lookup"><span data-stu-id="4d1c0-108">[![Examples of skills, certifications, education, and project experience](./media/projectresourcing06-1024x383.jpg)](./media/projectresourcing06.jpg)</span></span>

<span data-ttu-id="4d1c0-109">กระบวนงานต่อไปนี้อธิบายวิธีการตั้งค่าบางอย่างของความสามารถสำหรับทรัพยากร</span><span class="sxs-lookup"><span data-stu-id="4d1c0-109">The following procedures explain how to set up some of the competencies for a resource.</span></span>

<span data-ttu-id="4d1c0-110">เพื่อตั้งค่าความสามารถสำหรับผู้ปฏิบัติงาน คุณสามารถใช้หน้ารายการ **ผู้ปฏิบัติงาน** ในทรัพยากรบุคคล หรือหน้ารายการ **ทรัพยากร** ในการจัดการโครงการและการบัญชีได้อย่างใดอย่างหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="4d1c0-110">To set up competencies for a worker, you can use either the **Workers** list page in Human resources or the **Resources** list page in Project management and accounting.</span></span> <span data-ttu-id="4d1c0-111">สำหรับกระบวนงานต่อไปนี้ เราจะใช้หน้ารายการ **ผู้ปฏิบัติงาน** ในทรัพยากรบุคคล</span><span class="sxs-lookup"><span data-stu-id="4d1c0-111">For the following procedures, the **Workers** list page in Human resources is used.</span></span>

## <a name="set-up-competencies-certificates"></a><span data-ttu-id="4d1c0-112">ตั้งค่าความสามารถ: ใบรับรอง</span><span class="sxs-lookup"><span data-stu-id="4d1c0-112">Set up competencies: Certificates</span></span>

1. <span data-ttu-id="4d1c0-113">ในหน้ารายการ **ผู้ปฏิบัติงาน** เลือกรายการของผู้ปฏิบัติงานเพื่อเพิ่มข้อมูลใบรับรองให้</span><span class="sxs-lookup"><span data-stu-id="4d1c0-113">On the **Workers** list page, select the line for the worker to add certificate information for.</span></span>
2. <span data-ttu-id="4d1c0-114">ในบานหน้าต่างการดำเนินการ บนแท็บ **ผู้ปฏิบัติงาน** ในกลุ่ม **ความสามารถ** ให้เลือก **ใบรับรอง**</span><span class="sxs-lookup"><span data-stu-id="4d1c0-114">On the Action Pane, on the **Worker** tab, in the **Competencies** group, select **Certificates**.</span></span>
3. <span data-ttu-id="4d1c0-115">เลือก **สร้าง** จากนั้นในฟิลด์ **ชนิดของประกาศนียบัตร** เลือก **PMP**</span><span class="sxs-lookup"><span data-stu-id="4d1c0-115">Select **New**, and then, in the **Certificate type** field, select **PMP**.</span></span>
4. <span data-ttu-id="4d1c0-116">ในฟิลด์ **วันที่เริ่มต้น** เลือก **10/1/2015** และเลือก **บันทึก**</span><span class="sxs-lookup"><span data-stu-id="4d1c0-116">In the **Start date** field, select **10/1/2015**, and select **Save**.</span></span>

## <a name="set-up-competencies-skills"></a><span data-ttu-id="4d1c0-117">ตั้งค่าความสามารถ: ทักษะ</span><span class="sxs-lookup"><span data-stu-id="4d1c0-117">Set up competencies: Skills</span></span>

1. <span data-ttu-id="4d1c0-118">ในหน้ารายการ **ผู้ปฏิบัติงาน** ตรวจสอบให้แน่ใจว่า ผู้ปฏิบัติงานที่คุณใช้ในกระบวนงานก่อนหน้านี้ยังคงถูกเลือกไว้</span><span class="sxs-lookup"><span data-stu-id="4d1c0-118">On the **Workers** list page, make sure that the worker that you used in the previous procedure is still selected.</span></span> <span data-ttu-id="4d1c0-119">จากนั้นบนบานหน้าต่างการดำเนินการ บนแท็บ **ผู้ปฏิบัติงาน** ในกลุ่ม **ความสามารถ** ให้เลือก **ทักษะ**</span><span class="sxs-lookup"><span data-stu-id="4d1c0-119">Then, on the Action Pane, on the **Worker** tab, in the **Competencies** group, select **Skills**.</span></span>
2. <span data-ttu-id="4d1c0-120">เลือก **ใหม่**</span><span class="sxs-lookup"><span data-stu-id="4d1c0-120">Select **New**.</span></span>
3. <span data-ttu-id="4d1c0-121">ในฟิลด์ **ทักษะ** เลือก **การจัดการโครงการ**</span><span class="sxs-lookup"><span data-stu-id="4d1c0-121">In the **Skill** field, select **Project management**.</span></span>
4. <span data-ttu-id="4d1c0-122">ในฟิลด์ **ระดับ** ให้เลือก **5 ผู้เชี่ยวชาญ**</span><span class="sxs-lookup"><span data-stu-id="4d1c0-122">In the **Level** field, select **5 Expert**.</span></span>
5. <span data-ttu-id="4d1c0-123">ในฟิลด์ **วันที่ของระดับ** เลือก **1-/14/2014**</span><span class="sxs-lookup"><span data-stu-id="4d1c0-123">In the **Level date** field, select **1-/14/2014**.</span></span>
6. <span data-ttu-id="4d1c0-124">ในฟิลด์ **ปีของประสบการณ์** ป้อน **10**</span><span class="sxs-lookup"><span data-stu-id="4d1c0-124">In the **Years of experience** field, enter **10**.</span></span>
7. <span data-ttu-id="4d1c0-125">เลือก **ตกลง** และจากนั้นปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="4d1c0-125">Select **Save**, and then close the page.</span></span>
