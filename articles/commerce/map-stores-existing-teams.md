---
title: แม็ปร้านค้าและทีมงานถ้ามีทีมงานที่มีอยู่ก่อนใน Microsoft Teams
description: หัวข้อนี้ครอบคลุมวิธีการแม็ปร้านค้าและทีมงานที่สอดคล้องกันในศูนย์ควบคุม Dynamics 365 Commerce ถ้าองค์กรของคุณสร้างทีมงานไว้แล้วใน Microsoft Teams ก่อนการรวม Commerce
author: gvrmohanreddy
manager: annbe
ms.date: 03/31/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.search.region: Global
ms.author: gmohanv
ms.search.validFrom: 2021-01-15
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: 3edd176788b24a5f5246e9b7bcb3c6fbcdca2254
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 04/01/2021
ms.locfileid: "5842753"
---
# <a name="map-stores-and-teams-if-there-are-pre-existing-teams-in-microsoft-teams"></a><span data-ttu-id="cfe21-103">แม็ปร้านค้าและทีมงานถ้ามีทีมงานที่มีอยู่ก่อนใน Microsoft Teams</span><span class="sxs-lookup"><span data-stu-id="cfe21-103">Map stores and teams if there are pre-existing teams in Microsoft Teams</span></span>

[!include [banner](includes/banner.md)]
[!include [banner](includes/preview-banner.md)]

<span data-ttu-id="cfe21-104">หัวข้อนี้ครอบคลุมวิธีการแม็ปร้านค้าและทีมงานที่สอดคล้องกันในศูนย์ควบคุม Dynamics 365 Commerce ถ้าองค์กรของคุณสร้างทีมงานไว้แล้วใน Microsoft Teams ก่อนการรวม Commerce</span><span class="sxs-lookup"><span data-stu-id="cfe21-104">This topic covers how to map stores and corresponding teams in Dynamics 365 Commerce headquarters if your organization has already created teams in Microsoft Teams before Commerce integration.</span></span>

<span data-ttu-id="cfe21-105">องค์กรของคุณอาจสร้างทีมงานให้กับร้านค้าของคุณบางส่วนหรือทั้งหมดก่อนที่จะรวม Dynamics 365 Commerce และ Microsoft Teams</span><span class="sxs-lookup"><span data-stu-id="cfe21-105">Your organization may have teams created for some or all of your stores before integrating Dynamics 365 Commerce and Microsoft Teams.</span></span> <span data-ttu-id="cfe21-106">ในกรณีนี้ ให้สร้างการซิงโครไนส์งานระหว่าง Commerce POS และ Microsoft Teams คุณต้องระบุการแม็ปร้านค้าและทีมงานที่สอดคล้องกันในศูนย์ควบคุม Commerce</span><span class="sxs-lookup"><span data-stu-id="cfe21-106">If this is the case, to establish task synchronization between Commerce POS and Microsoft Teams you must provide the mapping of stores and corresponding team in Commerce headquarters.</span></span>

## <a name="map-stores-and-corresponding-teams-in-commerce-headquarters"></a><span data-ttu-id="cfe21-107">แม็ปร้านค้าและทีมงานที่สอดคล้องกันในศูนย์ควบคุม Commerce</span><span class="sxs-lookup"><span data-stu-id="cfe21-107">Map stores and corresponding teams in Commerce headquarters</span></span> 

<span data-ttu-id="cfe21-108">หากต้องการแม็ปร้านค้าและทีมงานที่สอดคล้องกันในศูนย์ควบคุม Commerce ให้ทำตามขั้นตอนต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="cfe21-108">To map stores and corresponding teams in Commerce headquarters, follow these steps.</span></span>

1. <span data-ttu-id="cfe21-109">ไปที่ **การจัดการระบบ \> พื้นที่ทำงาน \> การจัดการข้อมูล**</span><span class="sxs-lookup"><span data-stu-id="cfe21-109">Go to **System Administration \> Workspace \> Data management**.</span></span>
1. <span data-ttu-id="cfe21-110">เลือก **ส่งออก**</span><span class="sxs-lookup"><span data-stu-id="cfe21-110">Select **Export**.</span></span> 
1. <span data-ttu-id="cfe21-111">บนบานหน้าต่างการดำเนินการ เลือก **สร้าง**</span><span class="sxs-lookup"><span data-stu-id="cfe21-111">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="cfe21-112">ภายใต้ **ชื่อกลุ่ม** ให้ป้อน "การแม็ป Teams ส่งออก"</span><span class="sxs-lookup"><span data-stu-id="cfe21-112">Under **Group name**, enter "Export Teams mapping".</span></span>
1. <span data-ttu-id="cfe21-113">ในแท็บด่วน **เอนทิตีที่เลือก** ให้เลือก **เพิ่มเอนทิตี**</span><span class="sxs-lookup"><span data-stu-id="cfe21-113">On the **Selected entities** FastTab, select **Add entity**.</span></span> <span data-ttu-id="cfe21-114">กล่องโต้ตอบ **เพิ่มเอนทิตี** จะปรากฏขึ้น</span><span class="sxs-lookup"><span data-stu-id="cfe21-114">The **Add entity** dialog box appears.</span></span>  
1. <span data-ttu-id="cfe21-115">ในรายการแบบหล่นลงของ **ชื่อเอนทิตี** ให้เลือก **การแม็ป Teams ระหว่างต้นทางและทีมงาน**</span><span class="sxs-lookup"><span data-stu-id="cfe21-115">In the **Entity name** drop-down list, select **Teams mapping between source and team**.</span></span>
1. <span data-ttu-id="cfe21-116">ในรายการแบบหล่นลงของ **รูปแบบข้อมูลเป้าหมาย** ให้เลือก **CSV**</span><span class="sxs-lookup"><span data-stu-id="cfe21-116">In the **Target data format** drop-down list, select **CSV**.</span></span>
1. <span data-ttu-id="cfe21-117">เลือก **เพิ่ม** แล้วเลือก **ปิด**</span><span class="sxs-lookup"><span data-stu-id="cfe21-117">Select **Add**, and then select **Close**.</span></span>
1. <span data-ttu-id="cfe21-118">ที่ด้านบนซ้ายภายใต้บานหน้าต่างการกิจกรรม ให้เลือก **ส่งออกทันที**</span><span class="sxs-lookup"><span data-stu-id="cfe21-118">On the top left under the Action Pane, select **Export now**.</span></span>
1. <span data-ttu-id="cfe21-119">ภายใต้ **สถานะการประมวลผลเอนทิตี** ให้เลือก **ดาวน์โหลดไฟล์**</span><span class="sxs-lookup"><span data-stu-id="cfe21-119">Under **Entity processing status**, select **Download file**.</span></span>
1. <span data-ttu-id="cfe21-120">ในไฟล์ CSV ที่ส่งออก ให้ป้อนค่าให้กับ **SOURCETYPE** **SOURCEID** และ **TEAMID** ดังนี้:</span><span class="sxs-lookup"><span data-stu-id="cfe21-120">In the exported CSV file, enter values for **SOURCETYPE**, **SOURCEID**, and **TEAMID** as follows:</span></span>
    - <span data-ttu-id="cfe21-121">เช่น **SOURCETYPE** ป้อน "RetailStore"</span><span class="sxs-lookup"><span data-stu-id="cfe21-121">For **SOURCETYPE**, enter "RetailStore".</span></span> 
    - <span data-ttu-id="cfe21-122">ตัวอย่างเช่น **SOURCEID** ป้อนหมายเลขร้านค้า (ตัวอย่างเช่น "000135" สำหรับร้านค้าซานฟรานซิสโก)</span><span class="sxs-lookup"><span data-stu-id="cfe21-122">For **SOURCEID**, enter the store number (for example, "000135" for the San Francisco store).</span></span> <span data-ttu-id="cfe21-123">คุณสามารถค้นหาหมายเลขร้านค้าที่ **Retail และ Commerce \> ช่องทาง \> ร้านค้า**</span><span class="sxs-lookup"><span data-stu-id="cfe21-123">You can find store numbers at **Retail and Commerce \> Channels \> Stores**.</span></span>
    - <span data-ttu-id="cfe21-124">เพื่อ **TEAMID** ให้ป้อนรหัสทีมงานที่เกี่ยวข้องจาก Microsoft Teams (ตัวอย่างเช่น "5f8bc92b-6aa8-451e-85d1-3949c01ddc6c")</span><span class="sxs-lookup"><span data-stu-id="cfe21-124">For **TEAMID**, enter the corresponding team ID from Microsoft Teams (for example, "5f8bc92b-6aa8-451e-85d1-3949c01ddc6c").</span></span> <span data-ttu-id="cfe21-125">คุณสามารถค้นหาข้อมูลรหัสทีมงานที่ [admin.teams.microsoft.com](https://admin.teams.microsoft.com) ได้</span><span class="sxs-lookup"><span data-stu-id="cfe21-125">You can find team ID information at [admin.teams.microsoft.com](https://admin.teams.microsoft.com).</span></span>
1. <span data-ttu-id="cfe21-126">บันทึกไฟล์ CSV ลงในเครื่องคอมพิวเตอร์ของคุณ</span><span class="sxs-lookup"><span data-stu-id="cfe21-126">Save the CSV file to your local machine.</span></span>
1. <span data-ttu-id="cfe21-127">ไปที่ **การจัดการระบบ \> พื้นที่ทำงาน \> การจัดการข้อมูล** และจากนั้นเลือก **ส่งออก**</span><span class="sxs-lookup"><span data-stu-id="cfe21-127">Go to **System Administration \> Workspace \> Data management**, and then select **Import**.</span></span>
1. <span data-ttu-id="cfe21-128">ในแท็บด่วน **เอนทิตีที่เลือก** ให้เลือก **เพิ่มไฟล์**</span><span class="sxs-lookup"><span data-stu-id="cfe21-128">On the **Selected entities** FastTab, select **Add file**.</span></span> <span data-ttu-id="cfe21-129">กล่องโต้ตอบ **เพิ่มไฟล์** จะปรากฏขึ้น</span><span class="sxs-lookup"><span data-stu-id="cfe21-129">The **Add file** dialog box appears.</span></span>
1. <span data-ttu-id="cfe21-130">ในรายการแบบหล่นลงของ **ชื่อเอนทิตี** ให้เลือก **การแม็ป Teams ระหว่างต้นทางและทีมงาน**</span><span class="sxs-lookup"><span data-stu-id="cfe21-130">In the **Entity name** drop-down list, select **Teams mapping between source and team**.</span></span>
1. <span data-ttu-id="cfe21-131">ในรายการแบบหล่นลงของ **รูปแบบข้อมูลต้นทาง** ให้เลือก **CSV**</span><span class="sxs-lookup"><span data-stu-id="cfe21-131">In the **Source data format** drop-down list, select **CSV**.</span></span>
1. <span data-ttu-id="cfe21-132">เลือก **อัพโหลดและเพิ่ม** เลือกไฟล์ CSV ที่คุณบันทึกก่อนหน้านี้ แล้วเลือก **เปิด**</span><span class="sxs-lookup"><span data-stu-id="cfe21-132">Select **Upload and add**, select the CSV file that you saved previously, and then select **Open**.</span></span>
1. <span data-ttu-id="cfe21-133">ในกล่องโต้ตอบ **เพิ่มไฟล์** ให้เลือก **ปิด**</span><span class="sxs-lookup"><span data-stu-id="cfe21-133">In the **Add file** dialog box, select **Close**.</span></span>
1. <span data-ttu-id="cfe21-134">ในบานหน้าต่างการดำเนินการ ให้เลือก **บันทึก** แล้วจากนั้น เลือก **นำเข้า**</span><span class="sxs-lookup"><span data-stu-id="cfe21-134">On the Action Pane, select **Save** , and then select **Import**.</span></span>

<span data-ttu-id="cfe21-135">รูปภาพตัวอย่างต่อไปนี้จะแสดงกลุ่ม **การแม็ปทีมงานส่งออก** ใน Commerce ที่มีองค์ประกอบ **เพิ่มเอนทิตี** และส่วนหัวของไฟล์ CSV ที่ส่งออกถูกเน้น</span><span class="sxs-lookup"><span data-stu-id="cfe21-135">The following example image shows the **Export teams mapping** group in Commerce with **Add entity** elements and the exported CSV file headers highlighted.</span></span>

![การแม็ปทีมงานส่งออก ใน Commerce ที่มีองค์ประกอบเพิ่มเอนทิตี และส่วนหัวของไฟล์ CSV ที่ส่งออกถูกเน้น](media/d365-commerce-data-mgmt-export-entity.png)

> [!NOTE]
> <span data-ttu-id="cfe21-137">หลังจากที่คุณปฏิบัติตามขั้นตอนต่างๆ ที่เตรียมการล่วงหน้าแล้ว ให้ปฏิบัติตามขั้นตอนต่างๆ ใน [การซิงโครไนส์การจัดการงานระหว่าง Microsoft Teams กับ POS](synchronize-tasks-teams-pos.md) เพื่อซิงโครไนส์การจัดการงาน</span><span class="sxs-lookup"><span data-stu-id="cfe21-137">After you complete the preceeding steps, follow the steps in [Synchronize task management between Microsoft Teams and POS](synchronize-tasks-teams-pos.md) to synchronize task management.</span></span> 

## <a name="additional-resources"></a><span data-ttu-id="cfe21-138">ทรัพยากรเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="cfe21-138">Additional resources</span></span>

[<span data-ttu-id="cfe21-139">ภาพรวมของการรวม Dynamics 365 Commerce และ Microsoft Teams</span><span class="sxs-lookup"><span data-stu-id="cfe21-139">Dynamics 365 Commerce and Microsoft Teams integration overview</span></span>](commerce-teams-integration.md)

[<span data-ttu-id="cfe21-140">เปิดใช้งานการรวม Dynamics 365 Commerce และ Microsoft Teams</span><span class="sxs-lookup"><span data-stu-id="cfe21-140">Enable Dynamics 365 Commerce and Microsoft Teams integration</span></span>](enable-teams-integration.md)

[<span data-ttu-id="cfe21-141">สํารอง Microsoft Teams จาก Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="cfe21-141">Provision Microsoft Teams from Dynamics 365 Commerce</span></span>](provision-teams-from-commerce.md)

[<span data-ttu-id="cfe21-142">ซิงโครไนส์การจัดการงานระหว่าง Microsoft Teams และ Dynamics 365 Commerce POS</span><span class="sxs-lookup"><span data-stu-id="cfe21-142">Synchronize task management between Microsoft Teams and Dynamics 365 Commerce POS</span></span>](synchronize-tasks-teams-pos.md)

[<span data-ttu-id="cfe21-143">จัดการบทบาทผู้ใช้ใน Microsoft Teams</span><span class="sxs-lookup"><span data-stu-id="cfe21-143">Manage user roles in Microsoft Teams</span></span>](manage-user-roles-teams.md)

[<span data-ttu-id="cfe21-144">คำถามที่พบบ่อยเกี่ยวกับการรวม Dynamics 365 Commerce และ Microsoft Teams</span><span class="sxs-lookup"><span data-stu-id="cfe21-144">Dynamics 365 Commerce and Microsoft Teams integration FAQ</span></span>](teams-integration-faq.md)
