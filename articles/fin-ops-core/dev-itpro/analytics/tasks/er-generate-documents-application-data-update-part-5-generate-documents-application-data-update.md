---
title: สร้างเอกสารที่มีข้อมูลแอพลิเคชัน
description: เมื่อต้องการทำขั้นตอนในกระบวนงานนี้ให้เสร็จเรียบร้อย ก่อนอื่นคุณต้องดำเนินกระบวนงาน "ER สร้างเอกสารที่มีการปรับปรุงข้อมูลแอพลิเคชัน (ส่วนที่ 4 - แก้ไขรูปแบบ)" ให้เสร็จเรียบร้อยก่อน
author: NickSelin
manager: AnnBe
ms.date: 06/19/2017
ms.topic: business-process
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 7c474f4bc7940a429ed62870e00302c93581eb9a
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 03/09/2021
ms.locfileid: "5569592"
---
# <a name="generate-documents-that-have-application-data"></a><span data-ttu-id="1a8d1-103">จัดทำเอกสารที่มีข้อมูลแอปพลิเคชัน</span><span class="sxs-lookup"><span data-stu-id="1a8d1-103">Generate documents that have application data</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="1a8d1-104">เมื่อต้องการทำขั้นตอนในกระบวนงานนี้ให้เสร็จเรียบร้อย ก่อนอื่นคุณต้องดำเนินกระบวนงาน "ER สร้างเอกสารที่มีการปรับปรุงข้อมูลแอพลิเคชัน (ส่วนที่ 4: แก้ไขรูปแบบ)" ให้เสร็จเรียบร้อยก่อน</span><span class="sxs-lookup"><span data-stu-id="1a8d1-104">To complete the steps in this procedure, you must first complete the procedure, "ER Generate documents with application data update (Part 4: Modify format)".</span></span>



<span data-ttu-id="1a8d1-105">ขั้นตอนต่าง ๆ ในกระบวนงานนี้อธิบายวิธีการออกแบบการตั้งค่าคอนฟิกการรายงานทางอิเล็กทรอนิกส์ (ER) เพื่อสร้างเอกสารอิเล็กทรอนิกส์ส์และอัพเดตข้อมูลแอพลิเคชัน</span><span class="sxs-lookup"><span data-stu-id="1a8d1-105">The steps in this procedure explain how to design Electronic reporting (ER) configurations to generate an electronic document and update application data.</span></span> <span data-ttu-id="1a8d1-106">ในกระบวนงานนี้ คุณจะต้องดำเนินการตั้งค่าคอนฟิกรูปแบบของ ER เพื่อสร้างรายงานอินทราสแทต และอัพเดตข้อมูลแอพลิเคชันสำหรับการเก็บรายละเอียดของกระบวนการรายงานถาวร</span><span class="sxs-lookup"><span data-stu-id="1a8d1-106">In this procedure, you execute the ER format configuration to generate the Intrastat report and update application data for archiving details of the reporting process.</span></span>



<span data-ttu-id="1a8d1-107">กระบวนงานนี้ถูกสร้างขึ้นสำหรับผู้ใช้ที่มีบทบาทผู้ดูแลระบบหรือนักพัฒนาการรายงานทางอิเล็กทรอนิกส์</span><span class="sxs-lookup"><span data-stu-id="1a8d1-107">This procedure is created for users with the assigned role of system administrator or electronic reporting developer.</span></span> <span data-ttu-id="1a8d1-108">ขั้นตอนเหล่านี้สามารถเสร็จสมบูรณ์ได้โดยใช้ชุดข้อมูล DEMF</span><span class="sxs-lookup"><span data-stu-id="1a8d1-108">These steps can be completed using the DEMF dataset.</span></span> <span data-ttu-id="1a8d1-109">ก่อนที่คุณจะเริ่มต้น ให้ตรวจสอบให้แน่ใจว่าบริบทประเทศสำหรับบริษัท DEMF คือ BEL (เบลเยียม)</span><span class="sxs-lookup"><span data-stu-id="1a8d1-109">Before you begin, make sure that the country context for the DEMF company is BEL (Belgium).</span></span>


## <a name="set-up-foreign-trade-parameters"></a><span data-ttu-id="1a8d1-110">ตั้งค่าพารามิเตอร์การค้าต่างประเทศ</span><span class="sxs-lookup"><span data-stu-id="1a8d1-110">Set up foreign trade parameters</span></span>
1. <span data-ttu-id="1a8d1-111">ไปที่ภาษี > การตั้งค่า > การค้าต่างประเทศ > พารามิเตอร์การค้าต่างประเทศ</span><span class="sxs-lookup"><span data-stu-id="1a8d1-111">Go to Tax > Setup > Foreign trade > Foreign trade parameters.</span></span>
2. <span data-ttu-id="1a8d1-112">คลิกแท็บลำดับหมายเลข</span><span class="sxs-lookup"><span data-stu-id="1a8d1-112">Click the Number sequences tab.</span></span>

    <span data-ttu-id="1a8d1-113">ในการเก็บรายละเอียดของกระบวนการรายงานอินทราสแทตถาวร เราจะต้องระบุเรกคอร์ดของที่เก็บถาวรที่เราสร้างขึ้นแต่ละรายการ</span><span class="sxs-lookup"><span data-stu-id="1a8d1-113">Archiving details of Intrastat reporting process, we need to identify records of each archive we created.</span></span> <span data-ttu-id="1a8d1-114">ต้องมีการตั้งค่าคอนฟิกลำดับหมายเลขพิเศษให้รายการดังกล่าว</span><span class="sxs-lookup"><span data-stu-id="1a8d1-114">A special number sequence must be configured for that.</span></span>  

3. <span data-ttu-id="1a8d1-115">เลือกการอ้างอิง 'รหัสที่เก็บถาวรอินทราสแทต'</span><span class="sxs-lookup"><span data-stu-id="1a8d1-115">Select the 'Intrastat archive ID' reference.</span></span>
4. <span data-ttu-id="1a8d1-116">ในฟิลด์รหัสลำดับหมายเลข ให้พิมพ์ค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="1a8d1-116">In the Number sequence code field, type a value.</span></span>

    <span data-ttu-id="1a8d1-117">ในฟิลด์ ‘รหัสลำดับหมายเลข‘ ให้ป้อนหรือเลือกค่า ‘Fore_2’</span><span class="sxs-lookup"><span data-stu-id="1a8d1-117">In the 'Number sequence code' field, enter or select the value 'Fore_2'.</span></span>  

5. <span data-ttu-id="1a8d1-118">แก้ไขการเปลี่ยนแปลงของรหัสลำดับหมายเลข</span><span class="sxs-lookup"><span data-stu-id="1a8d1-118">ResolveChanges the Number sequence code.</span></span>
6. <span data-ttu-id="1a8d1-119">คลิก บันทึก</span><span class="sxs-lookup"><span data-stu-id="1a8d1-119">Click Save.</span></span>
7. <span data-ttu-id="1a8d1-120">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="1a8d1-120">Close the page.</span></span>

## <a name="run-modified-er-format"></a><span data-ttu-id="1a8d1-121">เรียกใช้รูปแบบ ER ที่ปรับเปลี่ยน</span><span class="sxs-lookup"><span data-stu-id="1a8d1-121">Run modified ER format</span></span>
1. <span data-ttu-id="1a8d1-122">ไปที่ การจัดการองค์กร > การรายงานทางอิเล็กทรอนิกส์ > การตั้งค่าคอนฟิก</span><span class="sxs-lookup"><span data-stu-id="1a8d1-122">Go to Organization administration > Electronic reporting > Configurations.</span></span>
2. <span data-ttu-id="1a8d1-123">ในแผนภูมิ ขยาย 'อินทราสแทต (แบบจำลอง)'</span><span class="sxs-lookup"><span data-stu-id="1a8d1-123">In the tree, expand 'Intrastat (model)'.</span></span>
3. <span data-ttu-id="1a8d1-124">ในแผนภูมิ เลือก 'อินทราสแทต (แบบจำลอง)\อินทราสแทต (รูปแบบ)'</span><span class="sxs-lookup"><span data-stu-id="1a8d1-124">In the tree, select 'Intrastat (model)\Intrastat (format)'.</span></span>
4. <span data-ttu-id="1a8d1-125">คลิกดำเนินการ</span><span class="sxs-lookup"><span data-stu-id="1a8d1-125">Click Run.</span></span>
5. <span data-ttu-id="1a8d1-126">ในฟิลด์ป้อนชื่อไฟล์ พิมพ์ 'intrastat2.xml'</span><span class="sxs-lookup"><span data-stu-id="1a8d1-126">In the Enter file name field, type 'intrastat2.xml'.</span></span>
6. <span data-ttu-id="1a8d1-127">คลิก ตกลง </span><span class="sxs-lookup"><span data-stu-id="1a8d1-127">Click OK.</span></span>

## <a name="review-er-format-executions-results"></a><span data-ttu-id="1a8d1-128">ตรวจทานผลลัพธ์ของการดำเนินการรูปแบบของ ER</span><span class="sxs-lookup"><span data-stu-id="1a8d1-128">Review ER format execution's results</span></span>
<span data-ttu-id="1a8d1-129">ตรวจทานไฟล์ XML ที่สร้างขึ้น</span><span class="sxs-lookup"><span data-stu-id="1a8d1-129">Review the generated XML file.</span></span>  
1. <span data-ttu-id="1a8d1-130">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="1a8d1-130">Close the page.</span></span>
2. <span data-ttu-id="1a8d1-131">ไปที่ภาษี > ประกาศต่างๆ > การค้าต่างประเทศ > อินทราสแทต</span><span class="sxs-lookup"><span data-stu-id="1a8d1-131">Go to Tax > Declarations > Foreign trade > Intrastat.</span></span>

    <span data-ttu-id="1a8d1-132">เปิดแบบฟอร์มที่ประกอบด้วยธุรกรรมอินทราสแทตที่รวมอยู่ในเอกสารทางอิเล็กทรอนิกส์ที่สร้างขึ้นนี้</span><span class="sxs-lookup"><span data-stu-id="1a8d1-132">Open this form containing Intrastat transactions that have been included to the generated electronic document.</span></span>  

3. <span data-ttu-id="1a8d1-133">คลิก ที่เก็บถาวรของอินทราสแทต</span><span class="sxs-lookup"><span data-stu-id="1a8d1-133">Click Intrastat archive.</span></span>

    <span data-ttu-id="1a8d1-134">เนื่องจากในขณะนี้รูปแบบ ER ที่มีการดำเนินการประกอบด้วยการตั้งค่าสำหรับการอัพเดตข้อมูลแอพลิเคชัน รายละเอียดของการรายงานอินทราสแทตที่เสร็จสมบูรณ์แล้วจึงถูกเก็บไว้</span><span class="sxs-lookup"><span data-stu-id="1a8d1-134">Since the executed ER format contains now settings for application data update, the details of the completed Intrastat reporting have been archived.</span></span> <span data-ttu-id="1a8d1-135">ในแบบฟอร์มนี้ คุณสามารถดูเรกคอร์ดส่วนหัวของที่เก็บถาวรที่สร้างขึ้น</span><span class="sxs-lookup"><span data-stu-id="1a8d1-135">In this form, you can see the header record of the created archive.</span></span>  

4. <span data-ttu-id="1a8d1-136">คลิก รายละเอียด</span><span class="sxs-lookup"><span data-stu-id="1a8d1-136">Click Details.</span></span>

    <span data-ttu-id="1a8d1-137">ในแบบฟอร์มนี้ คุณสามารถดูรายละเอียดสำหรับที่เก็บถาวรที่สร้างขึ้น</span><span class="sxs-lookup"><span data-stu-id="1a8d1-137">In this form, you can see the details for the created archive.</span></span>  

5. <span data-ttu-id="1a8d1-138">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="1a8d1-138">Close the page.</span></span>
6. <span data-ttu-id="1a8d1-139">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="1a8d1-139">Close the page.</span></span>
7. <span data-ttu-id="1a8d1-140">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="1a8d1-140">Close the page.</span></span>



[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]