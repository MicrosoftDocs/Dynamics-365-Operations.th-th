---
title: สร้างลำดับชั้นองค์กร
description: 'ใช้กระบวนงานต่อไปนี้เพื่อสร้างลำดับชั้นองค์กร '
author: sericks007
manager: AnnBe
ms.date: 07/01/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: OMHierarchyManager, OMHierarchyPurposeAssociation, OMHierarchySelection, HierarchyDesigner
audience: Application User
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: sericks
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: dde06f758be57fb646696c861218565476abcadc
ms.sourcegitcommit: 57e1dafa186fec77ddd8ba9425d238e36e0f0998
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 03/18/2020
ms.locfileid: "3140570"
---
# <a name="create-an-organization-hierarchy"></a><span data-ttu-id="ace4e-103">สร้างลำดับชั้นองค์กร</span><span class="sxs-lookup"><span data-stu-id="ace4e-103">Create an organization hierarchy</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="ace4e-104">ใช้กระบวนงานต่อไปนี้เพื่อสร้างลำดับชั้นองค์กร </span><span class="sxs-lookup"><span data-stu-id="ace4e-104">Use the following procedure to create an organizational hierarchy.</span></span> <span data-ttu-id="ace4e-105">คุณสามารถใช้ลำดับชั้นองค์กรเพื่อดู และรายงานในบธุรกิจของคุณจากมุมมองต่างๆได้</span><span class="sxs-lookup"><span data-stu-id="ace4e-105">You can use organizational hierarchies to view and report on your business from various perspectives.</span></span> <span data-ttu-id="ace4e-106">ตัวอย่างเช่น คุณสามารถตั้งค่าหนึ่งลำดับชั้นสำหรับภาษี ทางกฎหมาย หรือการรายงานตามกฎหมาย</span><span class="sxs-lookup"><span data-stu-id="ace4e-106">For example, you can set up one hierarchy for tax, legal, or statutory reporting.</span></span> <span data-ttu-id="ace4e-107">จากนั้นคุณสามารถตั้งค่าอีกลำดับชั้นได้เพื่อรายงานข้อมูลทางการเงินที่ไม่จำเป็นทางกฎหมาย แต่ถูกใช้เป็นการรายงานภายใน</span><span class="sxs-lookup"><span data-stu-id="ace4e-107">You can then set up another hierarchy to report financial information that is not legally required, but that is used for internal reporting.</span></span> 

<span data-ttu-id="ace4e-108">ก่อนที่คุณจะสร้างลำดับชั้นองค์กร คุณต้องสร้างองค์กร</span><span class="sxs-lookup"><span data-stu-id="ace4e-108">Before you create an organizational hierarchy, you must create organizations.</span></span> <span data-ttu-id="ace4e-109">สำหรับข้อมูลเพิ่มเติม ให้ดูงาน "สร้างนิติบุคคล" หรืองาน "สร้างหน่วยปฏิบัติงาน"</span><span class="sxs-lookup"><span data-stu-id="ace4e-109">For more information, see the "Create a legal entity" or "Create an operating unit" tasks.</span></span> <span data-ttu-id="ace4e-110">คุณยังสามารถสร้างทีมและแผนกได้ด้วย</span><span class="sxs-lookup"><span data-stu-id="ace4e-110">You can also create departments and teams.</span></span> 

<span data-ttu-id="ace4e-111">บริษัทข้อมูลสาธิตที่เคยสร้างกระบวนงานนี้คือ USMF</span><span class="sxs-lookup"><span data-stu-id="ace4e-111">The demo data company used to create this procedure is USMF.</span></span>

## <a name="create-a-hierarchy"></a><span data-ttu-id="ace4e-112">สร้างลำดับชั้น</span><span class="sxs-lookup"><span data-stu-id="ace4e-112">Create a hierarchy</span></span>
1. <span data-ttu-id="ace4e-113">ไปที่ **บานหน้าต่างนำทาง > โมดูล > การจัดการองค์กร > องค์กร > ลำดับชั้นขององค์กร**</span><span class="sxs-lookup"><span data-stu-id="ace4e-113">Go to **Navigation pane > Modules > Organization administration > Organizations > Organization hierarchies**.</span></span>
2. <span data-ttu-id="ace4e-114">บน **บานหน้าต่างการดำเนินการ** ให้คลิก **สร้าง**</span><span class="sxs-lookup"><span data-stu-id="ace4e-114">On the **Action pane**, click **New**.</span></span>
3. <span data-ttu-id="ace4e-115">ในฟิลด์ **ชื่อ** ให้พิมพ์ค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="ace4e-115">In the **Name** field, type a value.</span></span>
4. <span data-ttu-id="ace4e-116">ในส่วน **วัตถุประสงค์** คลิก **กำหนดวัตถุประสงค์**</span><span class="sxs-lookup"><span data-stu-id="ace4e-116">In the **Purpose** section, click **Assign purpose**.</span></span>
5. <span data-ttu-id="ace4e-117">ในรายการนี้ ให้ค้นหาและเลือกเรกคอร์ดที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="ace4e-117">In the list, find and select the desired record.</span></span> <span data-ttu-id="ace4e-118">เลือกวัตถุประสงค์เพื่อกำหนดให้กับลำดับชั้นขององค์กรของคุณ</span><span class="sxs-lookup"><span data-stu-id="ace4e-118">Select a purpose to assign to your organization hierarchy.</span></span>  
6. <span data-ttu-id="ace4e-119">ในส่วน **ลำดับชั้นที่กำหนด** คลิก **เพิ่ม**</span><span class="sxs-lookup"><span data-stu-id="ace4e-119">In the **Assigned hierarchies** sectiom, click **Add**.</span></span>
7. <span data-ttu-id="ace4e-120">ในรายการนี้ ให้ทำเครื่องหมายแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="ace4e-120">In the list, mark the selected row.</span></span> <span data-ttu-id="ace4e-121">ค้นหาลำดับชั้นที่คุณเพิ่งสร้างขึ้น</span><span class="sxs-lookup"><span data-stu-id="ace4e-121">Find the hierarchy you just created.</span></span>  
8. <span data-ttu-id="ace4e-122">คลิก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="ace4e-122">Click **OK**.</span></span>

## <a name="add-organizations-to-the-hierarchy"></a><span data-ttu-id="ace4e-123">เพิ่มลำดับชั้นให้กับองค์กร</span><span class="sxs-lookup"><span data-stu-id="ace4e-123">Add organizations to the hierarchy</span></span>
1. <span data-ttu-id="ace4e-124">ในรายการนี้ ให้ค้นหาและเลือกเรกคอร์ดที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="ace4e-124">In the list, find and select the desired record.</span></span> <span data-ttu-id="ace4e-125">เลือกลำดับชั้นของคุณ</span><span class="sxs-lookup"><span data-stu-id="ace4e-125">Select your hierarchy.</span></span>  
2. <span data-ttu-id="ace4e-126">ในส่วน **ลำดับชั้นที่กำหนด** ให้คลิก **มุมมองลำดับชั้น**</span><span class="sxs-lookup"><span data-stu-id="ace4e-126">In the **Assigned hierarchies** section, click **View hierarchy**.</span></span>
    - <span data-ttu-id="ace4e-127">เพิ่มองค์กรตามความจำเป็น</span><span class="sxs-lookup"><span data-stu-id="ace4e-127">Add organizations, as necessary.</span></span>  
    - <span data-ttu-id="ace4e-128">เพื่อเพิ่มองค์กร ให้คลิก **แก้ไข** แล้วจากนั้น **แทรก** เพื่อเพิ่มไปที่องค์กร</span><span class="sxs-lookup"><span data-stu-id="ace4e-128">To add an organization, click **Edit** and then **Insert** to add the organization.</span></span> <span data-ttu-id="ace4e-129">เมื่อคุณดำเนินการเปลี่ยนแปลงเสร็จสิ้น คุณสามารถ **บันทึก** แบบร่างและ/หรือ **เผยแพร่** การเปลี่ยนแปลง</span><span class="sxs-lookup"><span data-stu-id="ace4e-129">When you are done making changes you can **Save** a draft and/or **Publish** the changes.</span></span>  

