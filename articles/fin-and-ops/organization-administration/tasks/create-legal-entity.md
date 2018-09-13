--- 
title: "สร้างนิติบุคคล"
description: "นิติบุคคลเป็นองค์กรที่ได้รับการระบุผ่านการลงทะเบียนกับหน่วยงานทางกฎหมาย "
author: sericks007
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: OMLegalEntity, OMNewLegalEntity
audience: Application User
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: sericks
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: abd59b96a2e5dceb2492c2db2c617485b332fbd3
ms.openlocfilehash: 2b1869afa9ebbfc81ca321c57cc8e01739103d16
ms.contentlocale: th-th
ms.lasthandoff: 09/13/2018

---
# <a name="create-a-legal-entity"></a><span data-ttu-id="97fac-103">สร้างนิติบุคคล</span><span class="sxs-lookup"><span data-stu-id="97fac-103">Create a legal entity</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="97fac-104">นิติบุคคลเป็นองค์กรที่ได้รับการระบุผ่านการลงทะเบียนกับหน่วยงานทางกฎหมาย </span><span class="sxs-lookup"><span data-stu-id="97fac-104">A legal entity is an organization that is identified through registration with a legal authority.</span></span> <span data-ttu-id="97fac-105">นิติบุคคลที่สามารถป้อนลงในสัญญา และจำเป็นต้องใช้เพื่อจัดเตรียมรายงานที่รายงานเกี่ยวกับประสิทธิภาพการทำงานของตน</span><span class="sxs-lookup"><span data-stu-id="97fac-105">Legal entities can enter into contracts and are required to prepare statements that report on their performance.</span></span> <span data-ttu-id="97fac-106">กระบวนงานต่อไปนี้อธิบายวิธีสร้างนิติบุคคล</span><span class="sxs-lookup"><span data-stu-id="97fac-106">The following procedure explains how to create a legal entity.</span></span> <span data-ttu-id="97fac-107">ข้อมูลบริษัทสาธิตที่ใช้ในการสร้างกระบวนงานนี้คือ USMF</span><span class="sxs-lookup"><span data-stu-id="97fac-107">The demo data company used to create this procedure is USMF.</span></span>

1. <span data-ttu-id="97fac-108">ไปที่การจัดการองค์กร > องค์กร > นิติบุคคล</span><span class="sxs-lookup"><span data-stu-id="97fac-108">Go to Organization administration > Organizations > Legal entities.</span></span>
2. <span data-ttu-id="97fac-109">คลิก สร้าง</span><span class="sxs-lookup"><span data-stu-id="97fac-109">Click New.</span></span>
3. <span data-ttu-id="97fac-110">ในฟิลด์ชื่อ ให้พิมพ์ค่า </span><span class="sxs-lookup"><span data-stu-id="97fac-110">In the Name field, type a value.</span></span>
4. <span data-ttu-id="97fac-111">ในฟิลด์บริษัท ให้พิมพ์ค่า</span><span class="sxs-lookup"><span data-stu-id="97fac-111">In the Company field, type a value.</span></span>
5. <span data-ttu-id="97fac-112">ในฟิลด์ประเทศ/ภูมิภาค ให้ป้อนหรือเลือกค่า</span><span class="sxs-lookup"><span data-stu-id="97fac-112">In the Country/region field, enter or select a value.</span></span>
6. <span data-ttu-id="97fac-113">คลิก ตกลง</span><span class="sxs-lookup"><span data-stu-id="97fac-113">Click OK.</span></span>
    * <span data-ttu-id="97fac-114">ในส่วนทั่วไป ป้อนข้อมูลทั่วไปต่อไปนี้เกี่ยวกับนิติบุคคล: ป้อนชื่อสำหรับค้นหา ถ้าจำเป็นต้องมีชื่อสำหรับค้นหา</span><span class="sxs-lookup"><span data-stu-id="97fac-114">In the General section, provide the following general information about the legal entity: Enter a search name, if a search name is required.</span></span> <span data-ttu-id="97fac-115">ชื่อสำหรับค้นหาเป็นชื่ออื่นที่สามารถใช้ในการค้นหาสำหรับนิติบุคคลนี้</span><span class="sxs-lookup"><span data-stu-id="97fac-115">A search name is an alternate name that can be used to search for this legal entity.</span></span> <span data-ttu-id="97fac-116">เลือกว่านิติบุคคลนี้ถูกใช้เป็นบริษัทสำหรับการรวมบัญชีหรือไม่</span><span class="sxs-lookup"><span data-stu-id="97fac-116">Select whether this legal entity is being used as a consolidation company.</span></span> <span data-ttu-id="97fac-117">เลือกว่านิติบุคคลนี้กำลังจะถูกใช้เป็นบริษัทที่ตัดออกหรือไม่</span><span class="sxs-lookup"><span data-stu-id="97fac-117">Select whether this legal entity is being used as an elimination company.</span></span>  
7. <span data-ttu-id="97fac-118">ขยายส่วนที่อยู่</span><span class="sxs-lookup"><span data-stu-id="97fac-118">Expand the Addresses section.</span></span>
    * <span data-ttu-id="97fac-119">ในส่วนที่อยู่ ป้อนที่อยู่ เช่น ชื่อถนนและเลขที่ รหัสไปรษณีย์ และเมือง</span><span class="sxs-lookup"><span data-stu-id="97fac-119">In the Addresses section, enter address information, such as the street name and number, postal code, and city.</span></span>  
8. <span data-ttu-id="97fac-120">ขยายส่วนข้อมูลผู้ติดต่อ</span><span class="sxs-lookup"><span data-stu-id="97fac-120">Expand the Contact information section.</span></span>
    * <span data-ttu-id="97fac-121">ในส่วนข้อมูลผู้ติดต่อ ให้ป้อนข้อมูลเกี่ยวกับวิธีการสื่อสาร เช่น ที่อยู่อีเมล์ URLs และหมายเลขโทรศัพท์</span><span class="sxs-lookup"><span data-stu-id="97fac-121">In the Contact information section, enter information about methods of communication, such as email addresses, URLs, and telephone numbers.</span></span>  
9. <span data-ttu-id="97fac-122">ขยายส่วนการรายงานตามกฎหมาย</span><span class="sxs-lookup"><span data-stu-id="97fac-122">Expand the Statutory reporting section.</span></span>
    * <span data-ttu-id="97fac-123">ในส่วนการรายงานตามกฎหมาย ให้ป้อนหมายเลขการลงทะเบียนที่ใช้สำหรับการรายงานตามกฎหมาย</span><span class="sxs-lookup"><span data-stu-id="97fac-123">In the Statutory reporting section, enter the registration numbers that are used for statutory reporting.</span></span>  
10. <span data-ttu-id="97fac-124">ขยายส่วนหมายเลขของการลงทะเบียน</span><span class="sxs-lookup"><span data-stu-id="97fac-124">Expand the Registration numbers section.</span></span>
    * <span data-ttu-id="97fac-125">ในส่วนหมายเลขการลงทะเบียน ให้ป้อนข้อมูลใดๆที่ต้องการโดยนิติบุคคล</span><span class="sxs-lookup"><span data-stu-id="97fac-125">In the Registration numbers section, enter any information required by the legal entity.</span></span>  
11. <span data-ttu-id="97fac-126">ขยายส่วนของข้อมูลบัญชีธนาคาร</span><span class="sxs-lookup"><span data-stu-id="97fac-126">Expand the Bank account information section.</span></span>
    * <span data-ttu-id="97fac-127">ในส่วนข้อมูลบัญชีธนาคาร ให้ป้อนบัญชีธนาคารและหมายเลขเส้นทางสำหรับนิติบุคคล</span><span class="sxs-lookup"><span data-stu-id="97fac-127">In the Bank account information section, enter bank accounts and routing numbers for the legal entity.</span></span>  
12. <span data-ttu-id="97fac-128">ขยายส่วนการค้าต่างประเทศและลอจิสติกส์</span><span class="sxs-lookup"><span data-stu-id="97fac-128">Expand the Foreign trade and logistics section.</span></span>
    * <span data-ttu-id="97fac-129">ในส่วนการค้าต่างประเทศและลอจิสติกส์ ให้ป้อนข้อมูลการจัดส่งสำหรับนิติบุคคล</span><span class="sxs-lookup"><span data-stu-id="97fac-129">In the Foreign trade and logistics section, enter shipping information for the legal entity.</span></span>  
13. <span data-ttu-id="97fac-130">ขยายส่วนลำดับหมายเลข</span><span class="sxs-lookup"><span data-stu-id="97fac-130">Expand the Number sequences section.</span></span>
    * <span data-ttu-id="97fac-131">ในส่วนลำดับหมายเลข คุณสามารถดูลำดับหมายเลขที่เชื่อมโยงกับนิติบุคคลได้</span><span class="sxs-lookup"><span data-stu-id="97fac-131">In the Number sequences section, you can view the number sequences that are associated with the legal entity.</span></span>  
14. <span data-ttu-id="97fac-132">ขยายส่วนของรูปภาพ </span><span class="sxs-lookup"><span data-stu-id="97fac-132">Expand the Images section.</span></span>
    * <span data-ttu-id="97fac-133">ในส่วนรูปภาพ ดูหรือเปลี่ยนรูปโลโก้และ/หรือแดชบอร์ด ที่เชื่อมโยงกับนิติบุคคลได้</span><span class="sxs-lookup"><span data-stu-id="97fac-133">In the Images section, view or change the logo and/or dashboard image that are associated with the legal entity.</span></span>  
15. <span data-ttu-id="97fac-134">ขยายส่วนลงทะเบียนภาษี</span><span class="sxs-lookup"><span data-stu-id="97fac-134">Expand the Tax registration section.</span></span>
    * <span data-ttu-id="97fac-135">ในส่วนทะเบียนภาษี ให้ป้อนหมายเลขการลงทะเบียนที่ใช้เพื่อรายงานกับหน่วยงานจัดเก็บภาษี</span><span class="sxs-lookup"><span data-stu-id="97fac-135">In the Tax registration section, enter the registration numbers that are used to report to tax authorities.</span></span>  
16. <span data-ttu-id="97fac-136">ขยายส่วนภาษี 1099</span><span class="sxs-lookup"><span data-stu-id="97fac-136">Expand the Tax 1099 section.</span></span>
    * <span data-ttu-id="97fac-137">ในส่วนภาษี 1099 ให้ป้อนข้อมูล 1099 สำหรับนิติบุคคล</span><span class="sxs-lookup"><span data-stu-id="97fac-137">In the Tax 1099 section, enter 1099 information for the legal entity.</span></span>  
17. <span data-ttu-id="97fac-138">คลิก บันทึก</span><span class="sxs-lookup"><span data-stu-id="97fac-138">Click Save.</span></span>


