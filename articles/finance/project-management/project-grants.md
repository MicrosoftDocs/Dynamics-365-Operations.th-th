---
title: เงินช่วยเหลือโครงการ
description: หัวข้อนี้อธิบายวิธีการสร้างหรือปรับเปลี่ยนเงินช่วยเหลือ
author: RadhikaRS
manager: AnnBe
ms.date: 04/22/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: v-radsh
ms.dyn365.ops.version: 7
ms.search.validFrom: 2019-01-15
ms.openlocfilehash: f4f7d347dab9f02fc474656e2f4cfba8e374480d
ms.sourcegitcommit: dfef2faf881b2db1bd0f016df36e2b838105312b
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 04/22/2020
ms.locfileid: "3282852"
---
# <a name="project-grants"></a><span data-ttu-id="3268d-103">เงินช่วยเหลือโครงการ</span><span class="sxs-lookup"><span data-stu-id="3268d-103">Project grants</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="3268d-104">เงินช่วยเหลือเป็นของขวัญของเงินสำหรับวัตถุประสงค์หรือโครงการ เฉพาะ</span><span class="sxs-lookup"><span data-stu-id="3268d-104">A grant is a gift of money for a specific purpose or project.</span></span> <span data-ttu-id="3268d-105">โดยปกติ จะมีข้อจำกัดเกี่ยวกับวิธีการใช้เงินช่วยเหลือ</span><span class="sxs-lookup"><span data-stu-id="3268d-105">Usually, there are restrictions on how a grant can be spent.</span></span> <span data-ttu-id="3268d-106">ในการจัดการและการบัญชีโครงการ คุณสามารถป้อนและติดตามเงินช่วยเหลือ และกำหนดความสัมพันธ์กับโครงการและสัญญาโครงการได้</span><span class="sxs-lookup"><span data-stu-id="3268d-106">In Project management and accounting, you can enter and track grants, and define their relationships to projects and project contracts.</span></span> <span data-ttu-id="3268d-107">ตัวอย่างเช่น คุณสามารถดำเนินงานต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="3268d-107">For example, you can perform the following tasks:</span></span>

- <span data-ttu-id="3268d-108">เชื่อมโยงเงินช่วยเหลือกับโครงการและแหล่งเงินทุนผ่านลิงค์ไปยังหน้า **โครงการ** และ **รายละเอียดของสัญญาโครงการ**</span><span class="sxs-lookup"><span data-stu-id="3268d-108">Associate grants with projects and funding sources through links to the **Project** and **Project contract details** pages.</span></span>
- <span data-ttu-id="3268d-109">ป้อนและติดตามการเปลี่ยนแปลงไปยังเงินช่วยเหลือ เมื่อย้ายจากสถานะหนึ่งไปยังอีกสถานะหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="3268d-109">Enter and track changes to a grant as it moves from one status to another.</span></span>
- <span data-ttu-id="3268d-110">ป้อนและติดตามค่าใช้จ่าย ยอดเงินที่ร้องขอ และยอดเงินที่มอบให้</span><span class="sxs-lookup"><span data-stu-id="3268d-110">Enter and track costs, requested amounts, and awarded amounts.</span></span>
- <span data-ttu-id="3268d-111">สร้างเงินช่วยเหลือหลัก และเชื่อมโยงเงินช่วยเหลือย่อย</span><span class="sxs-lookup"><span data-stu-id="3268d-111">Create master grants, and associate subgrants with them.</span></span>

<span data-ttu-id="3268d-112">คุณสามารถสร้างเงินช่วยเหลือได้โดยการป้อนรายละเอียดทั้งหมดในเรกคอร์ดใหม่ หรือคุณสามารถคัดลอกรายละเอียดจากเงินช่วยเหลือที่มีอยู่ และจากนั้นอัพเดต</span><span class="sxs-lookup"><span data-stu-id="3268d-112">You can create a grant by entering all the details in a new record, or you can copy the details from an existing grant and then update them.</span></span>

## <a name="create-a-new-grant"></a><span data-ttu-id="3268d-113">สร้างเงินช่วยเหลือใหม่</span><span class="sxs-lookup"><span data-stu-id="3268d-113">Create a new grant</span></span>

1. <span data-ttu-id="3268d-114">ไปยัง **การจัดการและการบัญชีโครงการ** \> **เงินช่วยเหลือ** \> **เงินช่วยเหลือ**</span><span class="sxs-lookup"><span data-stu-id="3268d-114">Go to **Project management and accounting** \> **Grants** \> **Grants**.</span></span>
2. <span data-ttu-id="3268d-115">เลือก **สร้าง** \> **เงินช่วยเหลือ**</span><span class="sxs-lookup"><span data-stu-id="3268d-115">Select **New** \> **Grant**.</span></span>
3. <span data-ttu-id="3268d-116">บนหน้ารายละเอียดเงินช่วยเหลือ บน FastTab **ทั่วไป** ในฟิลด์ **รหัสเงินช่วยเหลือ** ให้ป้อนตัวระบุที่เป็นตัวอักษรและตัวเลขสำหรับเงินช่วยเหลือ</span><span class="sxs-lookup"><span data-stu-id="3268d-116">On the grant details page, on the **General** FastTab, in the **Grant ID** field, enter an alphanumeric identifier for the grant.</span></span>
4. <span data-ttu-id="3268d-117">ในฟิลด์ **ชื่อเงินช่วยเหลือ** ให้ป้อนชื่อสำหรับเงินช่วยเหลือ</span><span class="sxs-lookup"><span data-stu-id="3268d-117">In the **Grant name** field, enter a name for the grant.</span></span>
5. <span data-ttu-id="3268d-118">ในฟิลด์ **คำอธิบาย** ให้เพิ่มรายละเอียดเกี่ยวกับเงินช่วยเหลือใหม่</span><span class="sxs-lookup"><span data-stu-id="3268d-118">In the **Description** field, add details about the new grant.</span></span>

    <span data-ttu-id="3268d-119">ไม่จำเป็นต้องระบุรฟิลด์อื่นๆ ส่วนใหญ่บนหน้า และคุณสามารถป้อนข้อมูลมากหรือน้อยได้เท่าที่คุณต้องการ</span><span class="sxs-lookup"><span data-stu-id="3268d-119">Most of the other fields on the page are optional, and you can enter as little or as much information as you want.</span></span>

    <span data-ttu-id="3268d-120">รายการต่อไปนี้อธิบายข้อมูลที่ระบุไว้ใน FastTab แต่ละแท็บของหน้ารายละเอียดเงินช่วยเหลือ:</span><span class="sxs-lookup"><span data-stu-id="3268d-120">The following list describes the information that is specified on each FastTab of the grant details page:</span></span>

    - <span data-ttu-id="3268d-121">**ทั่วไป** – ป้อนชื่อเงินช่วยเหลือ สถานะ คำอธิบาย วัตถุประสงค์ และจำนวน</span><span class="sxs-lookup"><span data-stu-id="3268d-121">**General** – Enter the grant name, status, description, purpose, and amount.</span></span>
    - <span data-ttu-id="3268d-122">**ข้อมูลผู้ติดต่อ** – ป้อนรายละเอียดเกี่ยวกับพนักงาน แผนกที่จัดการเงินช่วยเหลือ และลูกค้าที่รับเงินช่วยเหลือ หรือองค์กรที่เป็นแหล่งของเงินช่วยเหลือ</span><span class="sxs-lookup"><span data-stu-id="3268d-122">**Contact information** – Enter details about staff members, the department that manages the grant, and the grant customer or organization source of the grant.</span></span> <span data-ttu-id="3268d-123">นอกจากนี้ คุณยังสามารถระบุว่าองค์กรของคุณเป็นเอนทิตีแบบส่งผ่านที่ได้รับเงินช่วยเหลือ และจากนั้น ส่งผ่านไปยังผู้รับอื่น</span><span class="sxs-lookup"><span data-stu-id="3268d-123">You can also indicate whether your organization is a pass-through entity that receives the grant and then passes it on to another recipient.</span></span> <span data-ttu-id="3268d-124">เลือก **เพิ่ม** เมื่อต้องการเพิ่มข้อมูลผู้ติดต่อ เช่น หมายเลขโทรศัพท์ และที่อยู่อีเมล สำหรับองค์กรที่ให้เงินช่วยเหลือ</span><span class="sxs-lookup"><span data-stu-id="3268d-124">Select **Add** to add contact information such as telephone numbers and email addresses for the organization that provides the grant.</span></span>
    - <span data-ttu-id="3268d-125">**วันที่และกำหนดเวลาสิ้นสุด** – ป้อนวันที่ที่สัมพันธ์กับเงินช่วยเหลือและใบสมัครขอรับเงินช่วยเหลือ</span><span class="sxs-lookup"><span data-stu-id="3268d-125">**Dates and deadlines** – Enter dates that are related to the grant and the grant application.</span></span> <span data-ttu-id="3268d-126">ตัวอย่างรวมถึงวันที่ครบกำหนดของใบสมัคร วันที่ส่ง และวันที่ได้รับอนุมัติหรือปฏิเสธเงินช่วยเหลือ</span><span class="sxs-lookup"><span data-stu-id="3268d-126">Examples include the application due date, the submission date, and the date when the grant is approved or rejected.</span></span>
    - <span data-ttu-id="3268d-127">**โครงการที่เกี่ยวข้องและสัญญาโครงการ** – คุณสามารถป้อนข้อมูลบน FastTab นี้ได้เฉพาะเมื่อฟิลด์ **สถานะเงินช่วยเหลือ** บน FastTab **ทั่วไป** ถูกตั้งค่าเป็น **ใช้งานอยู่** **ได้รับรางวัล**</span><span class="sxs-lookup"><span data-stu-id="3268d-127">**Associated projects and project contracts** – You can enter information on this FastTab only if the **Grant status** field on the **General** FastTab is set to **Active** or **Awarded**.</span></span> <span data-ttu-id="3268d-128">เลือกจากตัวเลือกต่อไปนี้เพื่อดำเนินงานที่เกี่ยวข้องให้เสร็จสมบูรณ์:</span><span class="sxs-lookup"><span data-stu-id="3268d-128">Select among the following options to complete the related task:</span></span>

        - <span data-ttu-id="3268d-129">**เพิ่มแหล่งเงินทุน** – เพิ่มแหล่งเงินทุนใหม่สำหรับเงินช่วยเหลือ</span><span class="sxs-lookup"><span data-stu-id="3268d-129">**Add funding source** – Add a new funding source for the grant.</span></span> <span data-ttu-id="3268d-130">คุณสามารถป้อนรายละเอียดทั้งหมดในขณะนี้ หรือคุณสามารถใช้ข้อมูลเริ่มต้น และจากนั้นอัพเดตในภายหลัง</span><span class="sxs-lookup"><span data-stu-id="3268d-130">You can enter all the details now, or you can use default information and then update it later.</span></span>
        - <span data-ttu-id="3268d-131">**เพิ่มสัญญาโครงการ** – เพิ่มหรืออัพเดตข้อมูลสัญญาโครงการ</span><span class="sxs-lookup"><span data-stu-id="3268d-131">**Add project contract** – Add or update project contract information.</span></span>
        - <span data-ttu-id="3268d-132">**เพิ่มโครงการ** – เพิ่มหรืออัพเดตรายละเอียดโครงการ</span><span class="sxs-lookup"><span data-stu-id="3268d-132">**Add project** – Add or update project details.</span></span>

    - <span data-ttu-id="3268d-133">**การตั้งค่า** – ป้อนรายละเอียดเกี่ยวกับเงินทุนที่ตรงกัน ถ้าจำเป็นต้องใช้ข้อมูลนี้</span><span class="sxs-lookup"><span data-stu-id="3268d-133">**Setup** – Enter details about matching funds, if this information is required.</span></span> <span data-ttu-id="3268d-134">องค์กรหลายๆ แห่งที่มอบเงินช่วยเหลือกำหนดให้ผู้รับใช้เงินหรือทรัพยากรของตนจำนวนหนึ่ง เพื่อให้ตรงกับยอดเงินที่ได้รับในเงินช่วยเหลือ</span><span class="sxs-lookup"><span data-stu-id="3268d-134">Many organizations that award grants require that recipients spend a specific amount of their own money or resources, to match the amount that is awarded in the grant.</span></span> <span data-ttu-id="3268d-135">ในฟิลด์ **โครงการท้องถิ่นหรือรหัสการติดตาม** คุณสามารถป้อนตัวระบุที่แตกต่างจากตัวระบุโครงการได้</span><span class="sxs-lookup"><span data-stu-id="3268d-135">In the **Local project or tracking ID** field, you can enter an identifier that differs from the project identifier.</span></span>

        > [!NOTE]
        > <span data-ttu-id="3268d-136">ถ้าเงินช่วยเหลือบางส่วนจะถูกมอบให้กับองค์กรอื่น ให้ตั้งค่าตัวเลือก **ผู้มอบเงินช่วยเหลือย่อย** เป็น **ใช่**</span><span class="sxs-lookup"><span data-stu-id="3268d-136">If part of the grant will be awarded to a different organization, set the **Subgrantor** option to **Yes**.</span></span> <span data-ttu-id="3268d-137">สำหรับเงินช่วยเหลือที่ได้รับในสหรัฐอเมริกา คุณสามารถระบุว่าจะรับเงินช่วยเหลือภายใต้ข้อบังคับของรัฐหรือสหพันธรัฐ</span><span class="sxs-lookup"><span data-stu-id="3268d-137">For grants that are awarded in the United States, you can specify whether a grant will be awarded under a state mandate or a federal mandate.</span></span>

    - <span data-ttu-id="3268d-138">**รายละเอียดในการเบิกเงิน** – เพิ่มหรืออัพเดตข้อมูลเกี่ยวกับความถี่ที่สามารถถอน เรียกเก็บเงิน หรือใช้เงินช่วยเหลือ</span><span class="sxs-lookup"><span data-stu-id="3268d-138">**Drawdown details** – Add or update information about how often grant funds can be withdrawn, billed for, or spent.</span></span>

## <a name="create-a-new-grant-from-a-copy"></a><span data-ttu-id="3268d-139">สร้างเงินช่วยเหลือใหม่จากสำเนา</span><span class="sxs-lookup"><span data-stu-id="3268d-139">Create a new grant from a copy</span></span>

1. <span data-ttu-id="3268d-140">ไปยัง **การจัดการและการบัญชีโครงการ** \> **เงินช่วยเหลือ** \> **เงินช่วยเหลือ**</span><span class="sxs-lookup"><span data-stu-id="3268d-140">Go to **Project management and accounting** \> **Grants** \> **Grants**.</span></span>
2. <span data-ttu-id="3268d-141">เลือก **สร้าง** \> **คัดลอกจากเงินช่วยเหลือ**</span><span class="sxs-lookup"><span data-stu-id="3268d-141">Select **New** \> **Copy from grant**.</span></span>
3. <span data-ttu-id="3268d-142">ป้อนตัวระบุที่เป็นตัวอักษรและตัวเลขและชื่อสำหรับเงินช่วยเหลือใหม่ และจากนั้น เลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="3268d-142">Enter an alphanumeric identifier and a name for the new grant, and then select **OK**.</span></span>
4. <span data-ttu-id="3268d-143">บนหน้ารายละเอียดเงินช่วยเหลือ ให้ทบทวนรายละเอียดของเงินช่วยเหลือที่คัดลอกมา และทำการเปลี่ยนแปลงใดๆ ที่จำเป็น</span><span class="sxs-lookup"><span data-stu-id="3268d-143">On the grant details page, review the details of the copied grant, and make any changes that are required.</span></span> <span data-ttu-id="3268d-144">ฟิลด์ส่วนใหญ่บนหน้าเป็นฟิลด์ที่ไม่จำเป็นต้องระบุ</span><span class="sxs-lookup"><span data-stu-id="3268d-144">Most of the fields on the page are optional.</span></span>

## <a name="view-or-modify-grant-details"></a><span data-ttu-id="3268d-145">ดูหรือปรับเปลี่ยนรายละเอียดเงินช่วยเหลือ</span><span class="sxs-lookup"><span data-stu-id="3268d-145">View or modify grant details</span></span>

1. <span data-ttu-id="3268d-146">ไปยัง **การจัดการและการบัญชีโครงการ** \> **เงินช่วยเหลือ** \> **เงินช่วยเหลือ**</span><span class="sxs-lookup"><span data-stu-id="3268d-146">Go to **Project management and accounting** \> **Grants** \> **Grants**.</span></span>
2. <span data-ttu-id="3268d-147">เลือกเงินช่วยเหลือที่จะปรับเปลี่ยน</span><span class="sxs-lookup"><span data-stu-id="3268d-147">Select the grant to modify.</span></span>
3. <span data-ttu-id="3268d-148">ในบานหน้าต่างการดำเนินการ บนแท็บ **เงินช่วยเหลือ** ในกลุ่ม **รักษา** ให้เลือก **แก้ไข**</span><span class="sxs-lookup"><span data-stu-id="3268d-148">On the Action Pane, on the **Grant** tab, in the **Maintain** group, select **Edit**.</span></span>
4. <span data-ttu-id="3268d-149">ตรวจทานรายละเอียดเงินช่วยเหลือ และทำการเปลี่ยนแปลงใดๆ ที่จำเป็น</span><span class="sxs-lookup"><span data-stu-id="3268d-149">Review the grant details, and make any changes that are required.</span></span>
