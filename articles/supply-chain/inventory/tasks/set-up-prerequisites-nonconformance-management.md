---
title: ตั้งค่าข้อกำหนดเบื้องต้นสำหรับการจัดการความไม่สอดคล้องกัน
description: ใช้กระบวนงานนี้เพื่อเปิดใช้งานกระบวนการการจัดการความไม่สอดคล้องกัน
author: perlynne
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventParameters, InventTestReportSetup, SysUserManagement, SysUserSetup, InventTestDiagnosticType, InventTestMiscCharges, InventTestOperation, InventProblemType, InventProblemTypeSetup, InventQuarantineZone
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 9094be37e44b978db224b16c255d04a36c5cefff
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 08/01/2019
ms.locfileid: "1845353"
---
# <a name="set-up-prerequisites-for-nonconformance-management"></a><span data-ttu-id="4bde4-103">ตั้งค่าข้อกำหนดเบื้องต้นสำหรับการจัดการความไม่สอดคล้องกัน</span><span class="sxs-lookup"><span data-stu-id="4bde4-103">Set up prerequisites for nonconformance management</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="4bde4-104">ใช้กระบวนงานนี้เพื่อเปิดใช้งานกระบวนการการจัดการความไม่สอดคล้องกัน</span><span class="sxs-lookup"><span data-stu-id="4bde4-104">Use this procedure to enable nonconformance management processes.</span></span> <span data-ttu-id="4bde4-105">ความไม่สอดคล้องกันอธิบายกระบวนงานหรือรายการที่มีปัญหาทางคุณภาพ ที่ข้อมูลคำอธิบายรวมแหล่งที่มาและชนิดของปัญหา</span><span class="sxs-lookup"><span data-stu-id="4bde4-105">A nonconformance describes a procedure or item that has a quality problem, where the descriptive information includes the source and type of problem.</span></span> <span data-ttu-id="4bde4-106">กระบวนงานนี้ใช้บริษัทข้อมูลสาธิต USMF</span><span class="sxs-lookup"><span data-stu-id="4bde4-106">This procedure uses the USMF demo data company.</span></span> <span data-ttu-id="4bde4-107">โดยทั่วไป กระบวนงานนี้จะถูกดำเนินการโดยผู้จัดการด้านคุณภาพ</span><span class="sxs-lookup"><span data-stu-id="4bde4-107">This procedure is typically performed by a quality manager.</span></span>


## <a name="enable-quality-management-processes-within-the-company"></a><span data-ttu-id="4bde4-108">เปิดใช้งานกระบวนการจัดการคุณภาพภายในบริษัท</span><span class="sxs-lookup"><span data-stu-id="4bde4-108">Enable quality management processes within the company</span></span>
1. <span data-ttu-id="4bde4-109">ไปที่การจัดการสินค้าคงคลัง > การตั้งค่า > สินค้าคงคลังและพารามิเตอร์การจัดการคลังสินค้า</span><span class="sxs-lookup"><span data-stu-id="4bde4-109">Go to Inventory management > Setup > Inventory and warehouse management parameters.</span></span>
2. <span data-ttu-id="4bde4-110">คลิกแท็บการจัดการคุณภาพ</span><span class="sxs-lookup"><span data-stu-id="4bde4-110">Click the Quality management tab.</span></span>
3. <span data-ttu-id="4bde4-111">เลือก ใช่ ในฟิลด์ใช้การจัดการคุณภาพ</span><span class="sxs-lookup"><span data-stu-id="4bde4-111">Select Yes in the Use quality management field.</span></span>
    * <span data-ttu-id="4bde4-112">เลือกพารามิเตอร์นี้เพื่อเปิดใช้งานกระบวนการจัดการคุณภาพสำหรับบริษัท</span><span class="sxs-lookup"><span data-stu-id="4bde4-112">Select this parameter to enable quality management processes for the company.</span></span>  
4. <span data-ttu-id="4bde4-113">ในฟิลด์อัตราต่อชั่วโมง ให้ป้อนตัวเลข</span><span class="sxs-lookup"><span data-stu-id="4bde4-113">In the Hourly rate field, enter a number.</span></span>
    * <span data-ttu-id="4bde4-114">ใช้ฟิลด์อัตราต่อชั่วโมง เพื่อป้อนอัตราแรงงานต่อชั่วโมงในในสกุลเงินท้องถิ่น </span><span class="sxs-lookup"><span data-stu-id="4bde4-114">Use the Hourly rate field to enter an hourly labor rate in the local currency.</span></span> <span data-ttu-id="4bde4-115">อัตราต่อชั่วโมงจะถูกใช้ในการคำนวณต้นทุนสำหรับการดำเนินงานที่เกี่ยวข้องกับความไม่สอดคล้อง</span><span class="sxs-lookup"><span data-stu-id="4bde4-115">The hourly rate is used for calculating costs for operations that are related to a nonconformance.</span></span> <span data-ttu-id="4bde4-116">และไม่ได้สัมพันธ์กับฟังก์ชันอื่น</span><span class="sxs-lookup"><span data-stu-id="4bde4-116">The hourly rate and calculated costs provide reference information for a nonconformance, and they do not interact with other functionality.</span></span>  
5. <span data-ttu-id="4bde4-117">คลิกการตั้งค่ารายงาน</span><span class="sxs-lookup"><span data-stu-id="4bde4-117">Click Report setup.</span></span>
    * <span data-ttu-id="4bde4-118">หน้านี้อนุญาตให้คุณกำหนดชนิดหมายเหตุรายงานตรวจสอบคุณภาพที่จะใช้ในรายงานการจัดการคุณภาพชนิดต่างๆ</span><span class="sxs-lookup"><span data-stu-id="4bde4-118">This page allows you define the quality report note types that will be used on different kinds of quality management reports.</span></span>  
6. <span data-ttu-id="4bde4-119">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="4bde4-119">Close the page.</span></span>
7. <span data-ttu-id="4bde4-120">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="4bde4-120">Close the page.</span></span>

## <a name="enable-user-for-nonconformance-processing"></a><span data-ttu-id="4bde4-121">เปิดใช้งานผู้ใช้สำหรับการประมวลผลความไม่สอดคล้องกัน</span><span class="sxs-lookup"><span data-stu-id="4bde4-121">Enable user for nonconformance processing</span></span>
1. <span data-ttu-id="4bde4-122">ไปที่การดูแลระบบ > ผู้ใช้ > ผู้ใช้</span><span class="sxs-lookup"><span data-stu-id="4bde4-122">Go to System administration > Users > Users.</span></span>
    * <span data-ttu-id="4bde4-123">เพื่อประมวลผลการอนุมัติของความไม่สอดคล้องกัน ผู้ใช้ที่อนุมัติหรือปฏิเสธความไม่สอดคล้องกันต้องมีค่า "ชื่อ" ที่กำหนดไว้ในหน้าผู้ใช้ </span><span class="sxs-lookup"><span data-stu-id="4bde4-123">To process the approval of a nonconformance the user who  approves or rejects nonconformances must have a “Name” value assigned on the Users page.</span></span> <span data-ttu-id="4bde4-124">การใช้บันทึกเอกสาร ผู้ใช้ต้องสามารถเรียกใช้ตัวเลือกผู้ใช้ในการจัดการเอกสาร</span><span class="sxs-lookup"><span data-stu-id="4bde4-124">To use the document notes, the user must also have Document handling activated in the user options.</span></span>  
2. <span data-ttu-id="4bde4-125">ใช้ตัวกรองข้อมูลด่วนเพื่อค้นหาเรกคอร์ด </span><span class="sxs-lookup"><span data-stu-id="4bde4-125">Use the Quick Filter to find records.</span></span> <span data-ttu-id="4bde4-126">ตัวอย่างเช่น กรองข้อมูลในฟิลด์ชื่อ ด้วยค่า 'Ricardo'</span><span class="sxs-lookup"><span data-stu-id="4bde4-126">For example, filter on the Name field with a value of 'Ricardo'.</span></span>
    * <span data-ttu-id="4bde4-127">ใช้ตัวกรองเพื่อค้นหาผู้ใช้ที่กำลังจะอนุมัติหรือปฏิเสธเรกคอร์ดความไม่สอดคล้องกัน</span><span class="sxs-lookup"><span data-stu-id="4bde4-127">Use the filter to find the user who will be approving or rejecting the nonconformance records.</span></span>  
3. <span data-ttu-id="4bde4-128">ในรายการนี้ ให้คลิกลิงค์ในแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="4bde4-128">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="4bde4-129">เพื่อประมวลผลการอนุมัติของความไม่สอดคล้องกัน ตรวจสอบให้แน่ใจว่าผู้ใช้ที่อนุมัติหรือปฏิเสธความไม่สอดคล้องกันมีค่า "ชื่อ" ที่กำหนดอยู่ในหน้าผู้ใช้</span><span class="sxs-lookup"><span data-stu-id="4bde4-129">To process the approval of a nonconformance, make sure the user who approves or rejects nonconformances has a “Name” value assigned on the Users page.</span></span>  
4. <span data-ttu-id="4bde4-130">คลิกตัวเลือกของผู้ใช้</span><span class="sxs-lookup"><span data-stu-id="4bde4-130">Click User options.</span></span>
5. <span data-ttu-id="4bde4-131">คลิกแท็บการกำหนดลักษณะ</span><span class="sxs-lookup"><span data-stu-id="4bde4-131">Click the Preferences tab.</span></span>
6. <span data-ttu-id="4bde4-132">เลือก ใช่ ในฟิลด์การเปิดใช้งานการจัดการเอกสาร</span><span class="sxs-lookup"><span data-stu-id="4bde4-132">Select Yes in the Enable document handling field.</span></span>
    * <span data-ttu-id="4bde4-133">การใช้บันทึกเอกสาร ผู้ใช้ต้องสามารถเรียกใช้ตัวเลือกผู้ใช้ในการจัดการเอกสาร</span><span class="sxs-lookup"><span data-stu-id="4bde4-133">To use the document notes, the user must also have Document handling activated in the user options.</span></span>  
7. <span data-ttu-id="4bde4-134">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="4bde4-134">Close the page.</span></span>
8. <span data-ttu-id="4bde4-135">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="4bde4-135">Close the page.</span></span>
9. <span data-ttu-id="4bde4-136">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="4bde4-136">Close the page.</span></span>

## <a name="define-diagnostic-types-for-nonconformance-processing"></a><span data-ttu-id="4bde4-137">กำหนดชนิดของการวินิจฉัย สำหรับการประมวลผลความไม่สอดคล้องกัน</span><span class="sxs-lookup"><span data-stu-id="4bde4-137">Define diagnostic types for nonconformance processing</span></span>
1. <span data-ttu-id="4bde4-138">ไปที่การจัดการคลังสินค้า > การตั้งค่า > การจัดการคุณภาพ > ชนิดการวินิจฉัย</span><span class="sxs-lookup"><span data-stu-id="4bde4-138">Go to Inventory management > Setup > Quality management > Diagnostic types.</span></span>
    * <span data-ttu-id="4bde4-139">ใช้หน้าชนิดการวินิจฉัย เพื่อกำหนดการจัดประเภทของการดำเนินการวินิจฉัย </span><span class="sxs-lookup"><span data-stu-id="4bde4-139">Use the Diagnostic types page to define a classification of diagnostic actions.</span></span> <span data-ttu-id="4bde4-140">การแก้ไขระบุชนิดของการดำเนินการวินิจฉัย ซึ่งควรจะดำเนินการกับความไม่สอดคล้องกันที่ได้รับอนุมัติแล้ว บุคคลที่ควรจะเป็นผู้ดำเนินการ และวันที่เสร็จสมบูรณ์ที่ร้องขอและที่วางแผนไว้</span><span class="sxs-lookup"><span data-stu-id="4bde4-140">A correction identifies what type of diagnostic action should be taken on an approved nonconformance, who should perform it, and the requested and planned completion date.</span></span>  
2. <span data-ttu-id="4bde4-141">คลิก สร้าง</span><span class="sxs-lookup"><span data-stu-id="4bde4-141">Click New.</span></span>
3. <span data-ttu-id="4bde4-142">ในฟิลด์การวินิจฉัย ให้พิมพ์ค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="4bde4-142">In the Diagnostic field, type a value.</span></span>
4. <span data-ttu-id="4bde4-143">ในฟิลด์ คำอธิบาย ให้พิมพ์ค่า</span><span class="sxs-lookup"><span data-stu-id="4bde4-143">In the Description field, type a value.</span></span>
5. <span data-ttu-id="4bde4-144">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="4bde4-144">Close the page.</span></span>

## <a name="define-quality-charges-for-nonconformance-processing"></a><span data-ttu-id="4bde4-145">กำหนดค่าธรรมเนียมคุณภาพ สำหรับการประมวลผลความไม่สอดคล้องกัน</span><span class="sxs-lookup"><span data-stu-id="4bde4-145">Define quality charges for nonconformance processing</span></span>
1. <span data-ttu-id="4bde4-146">ไปที่การจัดการคลังสินค้า > การตั้งค่า > การจัดการคุณภาพ > ค่าธรรมเนียมเกี่ยวกับคุณภาพ</span><span class="sxs-lookup"><span data-stu-id="4bde4-146">Go to Inventory management > Setup > Quality management > Quality charges.</span></span>
    * <span data-ttu-id="4bde4-147">ใช้หน้าค่าธรรมเนียมเกี่ยวกับคุณภาพ เพื่อกำหนดการจัดประเภทของค่าธรรมเนียมที่จะถูกใช้ในการดำเนินการที่เกี่ยวข้องกับความไม่สอดคล้อง</span><span class="sxs-lookup"><span data-stu-id="4bde4-147">Use the Quality charges page to define a classification of charges that will used in operations related to nonconformances.</span></span>  
2. <span data-ttu-id="4bde4-148">คลิก สร้าง</span><span class="sxs-lookup"><span data-stu-id="4bde4-148">Click New.</span></span>
3. <span data-ttu-id="4bde4-149">ในฟิลด์รหัสค่าธรรมเนียม ให้พิมพ์ค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="4bde4-149">In the Charges code field, type a value.</span></span>
4. <span data-ttu-id="4bde4-150">ในฟิลด์ คำอธิบาย ให้พิมพ์ค่า</span><span class="sxs-lookup"><span data-stu-id="4bde4-150">In the Description field, type a value.</span></span>
5. <span data-ttu-id="4bde4-151">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="4bde4-151">Close the page.</span></span>

## <a name="define-the-operations-for-nonconformance-processing"></a><span data-ttu-id="4bde4-152">กำหนดการดำเนินงานสำหรับการประมวลผลความไม่สอดคล้องกัน</span><span class="sxs-lookup"><span data-stu-id="4bde4-152">Define the operations for nonconformance processing</span></span>
1. <span data-ttu-id="4bde4-153">ไปที่การจัดการคลังสินค้า > การตั้งค่า > การจัดการคุณภาพ > การดำเนินการ</span><span class="sxs-lookup"><span data-stu-id="4bde4-153">Go to Inventory management > Setup > Quality management > Operations.</span></span>
    * <span data-ttu-id="4bde4-154">ใช้หน้าการดำเนินงานเพื่อกำหนดการจัดประเภทของงานที่สามารถดำเนินการสำหรับความไม่สอดคล้องที่อนุมัติแล้ว</span><span class="sxs-lookup"><span data-stu-id="4bde4-154">Use the Operations page to define a classification of the work that may be performed for an approved nonconformance.</span></span> <span data-ttu-id="4bde4-155">เมื่อคุณเชื่อมโยงการดำเนินงานกับความไม่สอดคล้อง คุณสามารถกำหนดข้อมูลเกี่ยวกับวัสดุที่เกี่ยวข้อง ชั่วโมงแรงงาน และค่าธรรมเนียมเบ็ดเตล็ดที่จำเป็นเพื่อทำการดำเนินงาน</span><span class="sxs-lookup"><span data-stu-id="4bde4-155">When you relate an operation to a nonconformance, you can define information about the associated material, labor hours, and miscellaneous charges that are required to perform the operation.</span></span> <span data-ttu-id="4bde4-156">ข้อมูลนี้ให้พื้นฐานสำหรับการคำนวณต้นทุนที่ประเมินสำหรับการดำเนินการ</span><span class="sxs-lookup"><span data-stu-id="4bde4-156">This information provides the basis for calculating an estimated cost for performing the operation.</span></span>  
2. <span data-ttu-id="4bde4-157">คลิก สร้าง</span><span class="sxs-lookup"><span data-stu-id="4bde4-157">Click New.</span></span>
3. <span data-ttu-id="4bde4-158">ในฟิลด์การดำเนินการ ให้พิมพ์ค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="4bde4-158">In the Operation field, type a value.</span></span>
4. <span data-ttu-id="4bde4-159">ในฟิลด์ คำอธิบาย ให้พิมพ์ค่า</span><span class="sxs-lookup"><span data-stu-id="4bde4-159">In the Description field, type a value.</span></span>
5. <span data-ttu-id="4bde4-160">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="4bde4-160">Close the page.</span></span>

## <a name="define-problem-types-for-nonconformance-processing"></a><span data-ttu-id="4bde4-161">กำหนดชนิดปัญหาสำหรับการประมวลผลความไม่สอดคล้องกัน</span><span class="sxs-lookup"><span data-stu-id="4bde4-161">Define problem types for nonconformance processing</span></span>
1. <span data-ttu-id="4bde4-162">ไปที่การจัดการคลังสินค้า > การตั้งค่า > การจัดการคุณภาพ > ชนิดปัญหา</span><span class="sxs-lookup"><span data-stu-id="4bde4-162">Go to Inventory management > Setup > Quality management > Problem types.</span></span>
    * <span data-ttu-id="4bde4-163">ใช้หน้าชนิดปัญหาเพื่อกำหนดการจัดประเภทของปัญหาด้านคุณภาพ ซึ่งพบในความไม่สอดคล้องกันชนิดต่างๆ</span><span class="sxs-lookup"><span data-stu-id="4bde4-163">Use the Problem types page to define a classification of quality problems that are encountered in the various nonconformance types.</span></span> <span data-ttu-id="4bde4-164">ชนิดความไม่สอดคล้องประกอบด้วย ภายใน ลูกค้า ผู้จัดจำหน่าย คำขอการบริการ การผลิต และการผลิตสินค้าร่วม</span><span class="sxs-lookup"><span data-stu-id="4bde4-164">The nonconformance types include Internal, Customer, Vendor, Service request, Production, and Co-product production.</span></span> <span data-ttu-id="4bde4-165">ชนิดปัญหาเดี่ยวสามารถถูกเชื่อมโยงได้กับชนิดความไม่สอดคล้องที่หลากหลาย</span><span class="sxs-lookup"><span data-stu-id="4bde4-165">A single problem type can be associated with multiple nonconformance types.</span></span>  
2. <span data-ttu-id="4bde4-166">คลิก สร้าง</span><span class="sxs-lookup"><span data-stu-id="4bde4-166">Click New.</span></span>
3. <span data-ttu-id="4bde4-167">ในฟิลด์ชนิดปัญหา ให้พิมพ์ค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="4bde4-167">In the Problem type field, type a value.</span></span>
4. <span data-ttu-id="4bde4-168">ในฟิลด์ คำอธิบาย ให้พิมพ์ค่า</span><span class="sxs-lookup"><span data-stu-id="4bde4-168">In the Description field, type a value.</span></span>
5. <span data-ttu-id="4bde4-169">คลิกชนิดของความไม่สอดคล้องกัน</span><span class="sxs-lookup"><span data-stu-id="4bde4-169">Click Non conformance types.</span></span>
    * <span data-ttu-id="4bde4-170">ใช้หน้าชนิดความไม่สอดคล้องกัน เพื่ออนุมัติการใช้ชนิดของปัญหาสำหรับความไม่สอดคล้องกันหนึ่งชนิดขึ้นไป </span><span class="sxs-lookup"><span data-stu-id="4bde4-170">Use the Non conformance types page to authorize the use of a problem type for one or more of the nonconformance types.</span></span> <span data-ttu-id="4bde4-171">ตัวอย่างเช่น ชนิดของปัญหาเกี่ยวกับรหัสความบกพร่องสามารถนำไปใช้กับความไม่สอดคล้องกันได้ทุกชนิด ในขณะที่ชนิดของปัญหาเกี่ยวกับคำร้องเรียนของลูกค้าสามารถนำไปใช้กับความไม่สอดคล้องกันชนิดลูกค้าและคำขอการบริการเท่านั้น</span><span class="sxs-lookup"><span data-stu-id="4bde4-171">For example, a problem type regarding a defect code could apply to all nonconformance types, whereas a problem type about customer complaints may only apply to the customer and service request nonconformance types.</span></span>  
6. <span data-ttu-id="4bde4-172">คลิก สร้าง</span><span class="sxs-lookup"><span data-stu-id="4bde4-172">Click New.</span></span>
7. <span data-ttu-id="4bde4-173">ในรายการนี้ ให้ทำเครื่องหมายแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="4bde4-173">In the list, mark the selected row.</span></span>
8. <span data-ttu-id="4bde4-174">ในฟิลด์ชนิดของความไม่สอดคล้องกัน ให้เลือกตัวเลือกหนึ่งตัวเลือก</span><span class="sxs-lookup"><span data-stu-id="4bde4-174">In the Non conformance type field, select an option.</span></span>
9. <span data-ttu-id="4bde4-175">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="4bde4-175">Close the page.</span></span>
10. <span data-ttu-id="4bde4-176">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="4bde4-176">Close the page.</span></span>

## <a name="define-quarantine-zones-for-nonconformance-processing"></a><span data-ttu-id="4bde4-177">กำหนดโซนการตรวจสอบสินค้า สำหรับการประมวลผลความไม่สอดคล้องกัน</span><span class="sxs-lookup"><span data-stu-id="4bde4-177">Define quarantine zones for nonconformance processing</span></span>
1. <span data-ttu-id="4bde4-178">ไปที่การบริหารสินค้าคงคลัง > การตั้งค่า > การจัดการคุณภาพ > เขตการตรวจสอบสินค้า</span><span class="sxs-lookup"><span data-stu-id="4bde4-178">Go to Inventory management > Setup > Quality management > Quarantine zones.</span></span>
2. <span data-ttu-id="4bde4-179">คลิก สร้าง</span><span class="sxs-lookup"><span data-stu-id="4bde4-179">Click New.</span></span>
3. <span data-ttu-id="4bde4-180">ในฟิลด์เขตการตรวจสอบสินค้า ให้พิมพ์ค่า</span><span class="sxs-lookup"><span data-stu-id="4bde4-180">In the Quarantine zone field, type a value.</span></span>
4. <span data-ttu-id="4bde4-181">ในฟิลด์ คำอธิบาย ให้พิมพ์ค่า</span><span class="sxs-lookup"><span data-stu-id="4bde4-181">In the Description field, type a value.</span></span>
5. <span data-ttu-id="4bde4-182">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="4bde4-182">Close the page.</span></span>

