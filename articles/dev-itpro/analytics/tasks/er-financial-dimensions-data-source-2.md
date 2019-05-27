---
title: ER ใช้มิติทางการเงินเป็นแหล่งข้อมูล (ส่วนที่ 2 - การแม็ปแบบจำลอง)
description: 'ขั้นตอนต่อไปนี้อธิบายวิธีการที่ผู้ใช้ที่ถูกกำหนดบทบาทผู้ดูแลระบบหรือนักพัฒนาการรายงานทางอิเล็กทรอนิกส์สามารถตั้งค่าคอนฟิกแบบจำลองการรายงานทางอิเล็กทรอนิกส์ (ER) (ER) เพื่อใช้มิติทางการเงินเป็นแหล่งข้อมูลสำหรับรายงาน ER '
author: NickSelin
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ERSolutionTable, ERDataModelDesigner, ERModelMappingTable, ERModelMappingDesigner, ERExpressionDesignerFormula
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 92efd6a0b36471286c292a80542b81cd14a8eff3
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 05/15/2019
ms.locfileid: "1551356"
---
# <a name="er-use-financial-dimensions-as-a-data-source-part-2-model-mapping"></a><span data-ttu-id="6e02b-103">ER ใช้มิติทางการเงินเป็นแหล่งข้อมูล (ส่วนที่ 2: การแม็ปแบบจำลอง)</span><span class="sxs-lookup"><span data-stu-id="6e02b-103">ER Use financial dimensions as a data source (Part 2: Model mapping)</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="6e02b-104">ขั้นตอนต่อไปนี้อธิบายวิธีการที่ผู้ใช้ที่ถูกกำหนดบทบาทผู้ดูแลระบบหรือนักพัฒนาการรายงานทางอิเล็กทรอนิกส์สามารถตั้งค่าคอนฟิกแบบจำลองการรายงานทางอิเล็กทรอนิกส์ (ER) (ER) เพื่อใช้มิติทางการเงินเป็นแหล่งข้อมูลสำหรับรายงาน ER </span><span class="sxs-lookup"><span data-stu-id="6e02b-104">The following steps explain how a user assigned to the system administrator or electronic reporting developer role can configure an Electronic reporting (ER) model to use financial dimensions as a data source for ER reports.</span></span> <span data-ttu-id="6e02b-105">สามารถดำเนินการขั้นตอนเหล่านี้ได้ในบริษัทใดก็ได้ </span><span class="sxs-lookup"><span data-stu-id="6e02b-105">These steps can be performed in any company.</span></span>

<span data-ttu-id="6e02b-106">เพื่อทำขั้นตอนเหล่านี้ให้เสร็จสมบูรณ์ อันดับแรกคุณต้องทำขั้นตอนต่างๆ ในกระบวนงาน "ER ใช้มิติทางการเงินเป็นแหล่งข้อมูล (ส่วนที่ 1: แบบจำลองข้อมูล)"</span><span class="sxs-lookup"><span data-stu-id="6e02b-106">To complete these steps, you must first complete the steps in the “ER Use financial dimensions as a data source (Part 1: Design data model” procedure.</span></span>


## <a name="add-required-data-sources-to-model-mapping"></a><span data-ttu-id="6e02b-107">เพิ่มแหล่งข้อมูลที่จำเป็นไปยังการแม็ปแบบจำลอง</span><span class="sxs-lookup"><span data-stu-id="6e02b-107">Add required data sources to model mapping</span></span>
1. <span data-ttu-id="6e02b-108">ไปที่ การจัดการองค์กร > การรายงานทางอิเล็กทรอนิกส์ > การตั้งค่าคอนฟิก</span><span class="sxs-lookup"><span data-stu-id="6e02b-108">Go to Organization administration > Electronic reporting > Configurations.</span></span>
2. <span data-ttu-id="6e02b-109">ในแผนภูมิ เลือก 'แบบจำลองตัวอย่างมิติทางการเงิน'</span><span class="sxs-lookup"><span data-stu-id="6e02b-109">In the tree, select 'Financial dimensions sample model'.</span></span>
3. <span data-ttu-id="6e02b-110">คลิก ตัวออกแบบ</span><span class="sxs-lookup"><span data-stu-id="6e02b-110">Click Designer.</span></span>
4. <span data-ttu-id="6e02b-111">คลิก แม็ปแบบจำลองกับแหล่งข้อมูล</span><span class="sxs-lookup"><span data-stu-id="6e02b-111">Click Map model to datasource.</span></span>
5. <span data-ttu-id="6e02b-112">คลิก สร้าง</span><span class="sxs-lookup"><span data-stu-id="6e02b-112">Click New.</span></span>
6. <span data-ttu-id="6e02b-113">ในฟิลด์คำนิยาม ให้เลือก รายการ</span><span class="sxs-lookup"><span data-stu-id="6e02b-113">In the Definition field, select Entry.</span></span>
7. <span data-ttu-id="6e02b-114">ในฟิลด์ ชื่อ ให้พิมพ์ 'การแม็ปข้อมูลมิติ'</span><span class="sxs-lookup"><span data-stu-id="6e02b-114">In the Name field, type 'Dimensions data mapping'.</span></span>
8. <span data-ttu-id="6e02b-115">ในฟิลด์คำนิยาม ให้พิมพ์ 'การแม็ปข้อมูลมิติ'</span><span class="sxs-lookup"><span data-stu-id="6e02b-115">In the Description field, type 'Dimensions data mapping'.</span></span>
9. <span data-ttu-id="6e02b-116">คลิก บันทึก</span><span class="sxs-lookup"><span data-stu-id="6e02b-116">Click Save.</span></span>
10. <span data-ttu-id="6e02b-117">คลิก ตัวออกแบบ</span><span class="sxs-lookup"><span data-stu-id="6e02b-117">Click Designer.</span></span>
11. <span data-ttu-id="6e02b-118">ในแผนภูมิ ให้เลือก 'Dynamics 365 for Operations\ตาราง'</span><span class="sxs-lookup"><span data-stu-id="6e02b-118">In the tree, select 'Dynamics 365 for Operations\Table'.</span></span>
12. <span data-ttu-id="6e02b-119">คลิก เพิ่มราก</span><span class="sxs-lookup"><span data-stu-id="6e02b-119">Click Add root.</span></span>
13. <span data-ttu-id="6e02b-120">ในฟิลด์ชื่อ พิมพ์ 'บริษัท'</span><span class="sxs-lookup"><span data-stu-id="6e02b-120">In the Name field, type 'Company'.</span></span>
14. <span data-ttu-id="6e02b-121">ในฟิลด์ตาราง พิมพ์ 'CompanyInfo'</span><span class="sxs-lookup"><span data-stu-id="6e02b-121">In the Table field, type 'CompanyInfo'.</span></span>
15. <span data-ttu-id="6e02b-122">คลิก ตกลง ระบบจะนำเข้าข้อมูลการชำระเงิน</span><span class="sxs-lookup"><span data-stu-id="6e02b-122">Click OK.</span></span>
16. <span data-ttu-id="6e02b-123">ในแผนภูมิ เลือก 'ฟังก์ชัน\รายละเอียดมิติทางการเงิน'</span><span class="sxs-lookup"><span data-stu-id="6e02b-123">In the tree, select 'Functions\Financial dimensions details'.</span></span>
17. <span data-ttu-id="6e02b-124">คลิก เพิ่มราก</span><span class="sxs-lookup"><span data-stu-id="6e02b-124">Click Add root.</span></span>
    * <span data-ttu-id="6e02b-125">แหล่งข้อมูลนี้ระบุว่าจะกำหนดขอบเขตของมิติทางการเงินสำหรับรายงานใดๆ ที่จะใช้แบบจำลองนี้เป็นแหล่งข้อมูลอย่างไร</span><span class="sxs-lookup"><span data-stu-id="6e02b-125">This data source specifies how the scope of financial dimensions will be defined for any report that will use this model as a data source.</span></span>  
18. <span data-ttu-id="6e02b-126">ในฟิลด์ชื่อ ให้พิมพ์ค่า </span><span class="sxs-lookup"><span data-stu-id="6e02b-126">In the Name field, type a value.</span></span>
19. <span data-ttu-id="6e02b-127">เลือก ใช่ ในฟิลด์ขอข้อมูลมิติ</span><span class="sxs-lookup"><span data-stu-id="6e02b-127">Select Yes in the Ask for dimensions field.</span></span>
    * <span data-ttu-id="6e02b-128">เลือกใช่เพื่ออนุญาตให้ผู้ใช้สามารถเลือกมิติในเวลาที่ใช้ในการผลิตในแบบฟอร์มกล่องโต้ตอบผู้ใช้ </span><span class="sxs-lookup"><span data-stu-id="6e02b-128">Select Yes to allow the user to select dimensions at run-time on the User dialog form.</span></span> <span data-ttu-id="6e02b-129">ถ้าตั้งค่าเป็นไม่ มิติทางการเงินทั้งหมดของอินสแตนซ์ปัจจุบันจะถูกใช้โดยค่าเริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="6e02b-129">If set to No, all financial dimensions of the current instance will be used by default.</span></span>  
20. <span data-ttu-id="6e02b-130">ในฟิลด์การเลือกมิติทางการเงิน เลือก 'นิติบุคคล'</span><span class="sxs-lookup"><span data-stu-id="6e02b-130">In the Financial dimensions selection field, select 'Legal entity'.</span></span>
    * <span data-ttu-id="6e02b-131">เลือกทั้งหมดเพื่ออนุญาตให้ผู้ใช้สามารถเลือกมิติที่ต้องการสำหรับอินสแตนซ์ปัจจุบันในฟิลด์การค้นหา </span><span class="sxs-lookup"><span data-stu-id="6e02b-131">Select All to allow the user to select desire dimensions for the current  instance in the Lookup field.</span></span>  <span data-ttu-id="6e02b-132">เลือกนิติบุคคลที่จะอนุญาตให้ผู้ใช้สามารถเลือกมิติสำหรับบริษัทในฟิลด์การค้นหา </span><span class="sxs-lookup"><span data-stu-id="6e02b-132">Select Legal entity to allow the user to select dimensions for the company in the Lookup field.</span></span>  <span data-ttu-id="6e02b-133">เลือกมิติเพื่ออนุญาตให้ผู้ใช้สามารถเลือกมิติโดยใช้ชุดมิติเดียว</span><span class="sxs-lookup"><span data-stu-id="6e02b-133">Select Dimension to allow the user to select dimensions using a single dimension set.</span></span>  
21. <span data-ttu-id="6e02b-134">เลือก ใช่ ในฟิลด์ขอข้อมูลบัญชีหลัก</span><span class="sxs-lookup"><span data-stu-id="6e02b-134">Select Yes in the Ask for main account field.</span></span>
    * <span data-ttu-id="6e02b-135">ตั้งค่า 'ขอข้อมูลบัญชีหลัก' เป็น 'ใช่' เพื่ออนุญาตให้ผู้ใช้สามารถเลือกบัญชีหลักเป็นส่วนหนึ่งของรายการของมิติ </span><span class="sxs-lookup"><span data-stu-id="6e02b-135">Set ‘Ask for main account’ to Yes to allow users to select the main account as part of the list of dimensions.</span></span>   <span data-ttu-id="6e02b-136">ถ้าตั้งค่าเป็น ไม่ บัญชีหลักจะไม่ถูกรวมเข้าในรายการของมิติ และตัวเลือก 'บัญชีหลักเป็นข้อมูลบังคับ' จะถูกเปิดใช้งาน </span><span class="sxs-lookup"><span data-stu-id="6e02b-136">If set to No, the main account will not be included to the list of dimensions and the ‘Is main account mandatory’ option is enabled.</span></span> <span data-ttu-id="6e02b-137">ถ้า "บัญชีหลักเป็นข้อมูลบังคับ ' ถูกตั้งค่าเป็น ใช่ ให้รวมบัญชีหลักในรายการของมิติโดยไม่คำนึงถึงการเลือกของผู้ใช้</span><span class="sxs-lookup"><span data-stu-id="6e02b-137">If “Is main account mandatory’ is set to Yes, include the main account in the list of dimensions regardless of the user’s selection.</span></span>  
22. <span data-ttu-id="6e02b-138">คลิก ตกลง</span><span class="sxs-lookup"><span data-stu-id="6e02b-138">Click OK.</span></span>
23. <span data-ttu-id="6e02b-139">ในแผนภูมิ ให้เลือก 'Dynamics 365 for Operations\เรกคอร์ดตาราง'</span><span class="sxs-lookup"><span data-stu-id="6e02b-139">In the tree, select 'Dynamics 365 for Operations\Table records'.</span></span>
24. <span data-ttu-id="6e02b-140">คลิก เพิ่มราก</span><span class="sxs-lookup"><span data-stu-id="6e02b-140">Click Add root.</span></span>
25. <span data-ttu-id="6e02b-141">ในฟิลด์ชื่อ ให้พิมพ์ 'LedgerJournal'</span><span class="sxs-lookup"><span data-stu-id="6e02b-141">In the Name field, type 'LedgerJournal'.</span></span>
26. <span data-ttu-id="6e02b-142">เลือก ใช่ในการขอฟิลด์การสอบถาม</span><span class="sxs-lookup"><span data-stu-id="6e02b-142">Select Yes in the Ask for query field.</span></span>
27. <span data-ttu-id="6e02b-143">ในฟิลด์ตาราง พิมพ์ 'LedgerJournalTable'</span><span class="sxs-lookup"><span data-stu-id="6e02b-143">In the Table field, type 'LedgerJournalTable'.</span></span>
28. <span data-ttu-id="6e02b-144">คลิก ตกลง</span><span class="sxs-lookup"><span data-stu-id="6e02b-144">Click OK.</span></span>

## <a name="map-data-model-elements-to-added-data-sources"></a><span data-ttu-id="6e02b-145">แม็ปองค์ประกอบแบบจำลองข้อมูลไปยังแหล่งข้อมูลที่เพิ่ม</span><span class="sxs-lookup"><span data-stu-id="6e02b-145">Map data model elements to added data sources</span></span>
1. <span data-ttu-id="6e02b-146">ในแผนภูมิ ให้ขยาย 'สมุดบัญชี'</span><span class="sxs-lookup"><span data-stu-id="6e02b-146">In the tree, expand 'Journal'.</span></span>
2. <span data-ttu-id="6e02b-147">ในแผนภูมิ ให้ขยาย 'สมุดรายวัน\ธุรกรรม'</span><span class="sxs-lookup"><span data-stu-id="6e02b-147">In the tree, expand 'Journal\Transaction'.</span></span>
3. <span data-ttu-id="6e02b-148">ในแผนภูมิ ให้ขยาย 'สมุดรายวัน\ธุรกรรม\ข้อมูลมิติ'</span><span class="sxs-lookup"><span data-stu-id="6e02b-148">In the tree, expand 'Journal\Transaction\Dimensions data'.</span></span>
4. <span data-ttu-id="6e02b-149">ในแผนภูมิ ขยาย 'การตั้งค่ามิติ'</span><span class="sxs-lookup"><span data-stu-id="6e02b-149">In the tree, expand 'Dimensions setting'.</span></span>
5. <span data-ttu-id="6e02b-150">ในแผนภูมิ ขยาย 'LedgerJournal'</span><span class="sxs-lookup"><span data-stu-id="6e02b-150">In the tree, expand 'LedgerJournal'.</span></span>
6. <span data-ttu-id="6e02b-151">ในแผนภูมิ ขยาย 'LedgerJournal\<Relations'</span><span class="sxs-lookup"><span data-stu-id="6e02b-151">In the tree, expand 'LedgerJournal\<Relations'.</span></span>
7. <span data-ttu-id="6e02b-152">ในแผนภูมิ ขยาย 'LedgerJournal\<Relations\LedgerJournalTrans'</span><span class="sxs-lookup"><span data-stu-id="6e02b-152">In the tree, expand 'LedgerJournal\<Relations\LedgerJournalTrans'.</span></span>
8. <span data-ttu-id="6e02b-153">ในแผนภูมิ เลือก 'LedgerJournal\<Relations\LedgerJournalTrans\Voucher'</span><span class="sxs-lookup"><span data-stu-id="6e02b-153">In the tree, select 'LedgerJournal\<Relations\LedgerJournalTrans\Voucher'.</span></span>
9. <span data-ttu-id="6e02b-154">ในแผนภูมิ เลือก 'สมุดรายวัน\ธุรกรรม\ใบสำคัญ'</span><span class="sxs-lookup"><span data-stu-id="6e02b-154">In the tree, select 'Journal\Transaction\Voucher'.</span></span>
10. <span data-ttu-id="6e02b-155">คลิก ผูก</span><span class="sxs-lookup"><span data-stu-id="6e02b-155">Click Bind.</span></span>
11. <span data-ttu-id="6e02b-156">ในแผนภูมิ เลือก 'LedgerJournal\<Relations\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension)'</span><span class="sxs-lookup"><span data-stu-id="6e02b-156">In the tree, select 'LedgerJournal\<Relations\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension)'.</span></span>
    * <span data-ttu-id="6e02b-157">โปรดทราบว่าสำหรับการอ้างอิงใดๆ ของมิติทางการเงินที่ตั้งค่าเป็น ตัวอย่างเช่น LedgerDimension รายการแหล่งข้อมูลที่เกี่ยวข้องจะพร้อมใช้งาน (LedgerDimension.Dimension) </span><span class="sxs-lookup"><span data-stu-id="6e02b-157">Note that for any reference to financial dimensions that is set to, for instance, LedgerDimension, a corresponding data source item is available (LedgerDimension.Dimension).</span></span> <span data-ttu-id="6e02b-158">รายการแหล่งข้อมูลนี้เสนอให้ตั้งค่ามิติทางการเงินของมิตินั้นเป็นรายการของเรกคอร์ด</span><span class="sxs-lookup"><span data-stu-id="6e02b-158">This data source item offers the financial dimensions of that dimensions set as the record’s list.</span></span>  
12. <span data-ttu-id="6e02b-159">ในแผนภูมิ ขยาย 'LedgerJournal\<Relations\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension)'</span><span class="sxs-lookup"><span data-stu-id="6e02b-159">In the tree, expand 'LedgerJournal\<Relations\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension)'.</span></span>
13. <span data-ttu-id="6e02b-160">ในแผนภูมิ ขยาย 'LedgerJournal\<Relations\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension)\บัญชีหลักและมิติ'</span><span class="sxs-lookup"><span data-stu-id="6e02b-160">In the tree, expand 'LedgerJournal\<Relations\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension)\Main account and dimensions'.</span></span>
14. <span data-ttu-id="6e02b-161">ในแผนภูมิ ขยาย 'LedgerJournal\<Relations\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension)\บัญชีหลักและมิติ\ค่า'</span><span class="sxs-lookup"><span data-stu-id="6e02b-161">In the tree, expand 'LedgerJournal\<Relations\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension)\Main account and dimensions\Value'.</span></span>
15. <span data-ttu-id="6e02b-162">ในแผนภูมิ ขยาย 'LedgerJournal\<Relations\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension)\บัญชีหลักและมิติ\การกำหนด'</span><span class="sxs-lookup"><span data-stu-id="6e02b-162">In the tree, expand 'LedgerJournal\<Relations\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension)\Main account and dimensions\Definition'.</span></span>
16. <span data-ttu-id="6e02b-163">ในแผนภูมิ เลือก 'LedgerJournal\<Relations\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension)\บัญชีหลักและมิติ\การกำหนด\ชื่อ'</span><span class="sxs-lookup"><span data-stu-id="6e02b-163">In the tree, select 'LedgerJournal\<Relations\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension)\Main account and dimensions\Definition\Name'.</span></span>
17. <span data-ttu-id="6e02b-164">ในแผนภูมิ เลือก 'สมุดรายวัน\ธุรกรรม\ข้อมูลมิติ\ชื่อ'</span><span class="sxs-lookup"><span data-stu-id="6e02b-164">In the tree, select 'Journal\Transaction\Dimensions data\Name'.</span></span>
18. <span data-ttu-id="6e02b-165">คลิก ผูก</span><span class="sxs-lookup"><span data-stu-id="6e02b-165">Click Bind.</span></span>
19. <span data-ttu-id="6e02b-166">ในแผนภูมิ เลือก 'LedgerJournal\<Relations\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension)\บัญชีหลักและมิติ\ค่า\คำอธิบาย'</span><span class="sxs-lookup"><span data-stu-id="6e02b-166">In the tree, select 'LedgerJournal\<Relations\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension)\Main account and dimensions\Value\Description'.</span></span>
20. <span data-ttu-id="6e02b-167">ในแผนภูมิ เลือก 'สมุดรายวัน\ธุรกรรม\ข้อมูลมิติ\คำอธิบาย'</span><span class="sxs-lookup"><span data-stu-id="6e02b-167">In the tree, select 'Journal\Transaction\Dimensions data\Description'.</span></span>
21. <span data-ttu-id="6e02b-168">คลิก ผูก</span><span class="sxs-lookup"><span data-stu-id="6e02b-168">Click Bind.</span></span>
22. <span data-ttu-id="6e02b-169">ในแผนภูมิ เลือก 'LedgerJournal\<Relations\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension)\บัญชีหลักและมิติ\ค่า\รหัส'</span><span class="sxs-lookup"><span data-stu-id="6e02b-169">In the tree, select 'LedgerJournal\<Relations\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension)\Main account and dimensions\Value\Code'.</span></span>
23. <span data-ttu-id="6e02b-170">ในแผนภูมิ เลือก 'สมุดรายวัน\ธุรกรรม\ข้อมูลมิติ\รหัส'</span><span class="sxs-lookup"><span data-stu-id="6e02b-170">In the tree, select 'Journal\Transaction\Dimensions data\Code'.</span></span>
24. <span data-ttu-id="6e02b-171">คลิก ผูก</span><span class="sxs-lookup"><span data-stu-id="6e02b-171">Click Bind.</span></span>
25. <span data-ttu-id="6e02b-172">ในแผนภูมิ เลือก 'LedgerJournal\<Relations\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension)\บัญชีหลักและมิติ'</span><span class="sxs-lookup"><span data-stu-id="6e02b-172">In the tree, select 'LedgerJournal\<Relations\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension)\Main account and dimensions'.</span></span>
26. <span data-ttu-id="6e02b-173">ในแผนภูมิ เลือก 'สมุดรายวัน\ธุรกรรม\ข้อมูลมิติ'</span><span class="sxs-lookup"><span data-stu-id="6e02b-173">In the tree, select 'Journal\Transaction\Dimensions data'.</span></span>
27. <span data-ttu-id="6e02b-174">คลิก ผูก</span><span class="sxs-lookup"><span data-stu-id="6e02b-174">Click Bind.</span></span>
28. <span data-ttu-id="6e02b-175">ในแผนภูมิ เลือก 'LedgerJournal\<Relations\LedgerJournalTrans\Debit(AmountCurDebit)'</span><span class="sxs-lookup"><span data-stu-id="6e02b-175">In the tree, select 'LedgerJournal\<Relations\LedgerJournalTrans\Debit(AmountCurDebit)'.</span></span>
29. <span data-ttu-id="6e02b-176">ในแผนภูมิ เลือก 'สมุดรายวัน\ธุรกรรม\เดบิต'</span><span class="sxs-lookup"><span data-stu-id="6e02b-176">In the tree, select 'Journal\Transaction\Debit'.</span></span>
30. <span data-ttu-id="6e02b-177">คลิก ผูก</span><span class="sxs-lookup"><span data-stu-id="6e02b-177">Click Bind.</span></span>
31. <span data-ttu-id="6e02b-178">ในแผนภูมิ เลือก 'LedgerJournal\<Relations\LedgerJournalTrans\Date(TransDate)'</span><span class="sxs-lookup"><span data-stu-id="6e02b-178">In the tree, select 'LedgerJournal\<Relations\LedgerJournalTrans\Date(TransDate)'.</span></span>
32. <span data-ttu-id="6e02b-179">ในแผนภูมิ เลือก 'สมุดรายวัน\ธุรกรรม\วันที่'</span><span class="sxs-lookup"><span data-stu-id="6e02b-179">In the tree, select 'Journal\Transaction\Date'.</span></span>
33. <span data-ttu-id="6e02b-180">คลิก ผูก</span><span class="sxs-lookup"><span data-stu-id="6e02b-180">Click Bind.</span></span>
34. <span data-ttu-id="6e02b-181">ในแผนภูมิ เลือก 'LedgerJournal\<Relations\LedgerJournalTrans\Currency(CurrencyCode)'</span><span class="sxs-lookup"><span data-stu-id="6e02b-181">In the tree, select 'LedgerJournal\<Relations\LedgerJournalTrans\Currency(CurrencyCode)'.</span></span>
35. <span data-ttu-id="6e02b-182">ในแผนภูมิ เลือก 'สมุดรายวัน\ธุรกรรม\สกุลเงิน'</span><span class="sxs-lookup"><span data-stu-id="6e02b-182">In the tree, select 'Journal\Transaction\Currency'.</span></span>
36. <span data-ttu-id="6e02b-183">คลิก ผูก</span><span class="sxs-lookup"><span data-stu-id="6e02b-183">Click Bind.</span></span>
37. <span data-ttu-id="6e02b-184">ในแผนภูมิ เลือก 'LedgerJournal\<Relations\LedgerJournalTrans\Credit(AmountCurCredit)'</span><span class="sxs-lookup"><span data-stu-id="6e02b-184">In the tree, select 'LedgerJournal\<Relations\LedgerJournalTrans\Credit(AmountCurCredit)'.</span></span>
38. <span data-ttu-id="6e02b-185">ในแผนภูมิ เลือก 'สมุดรายวัน\ธุรกรรม\เครดิต'</span><span class="sxs-lookup"><span data-stu-id="6e02b-185">In the tree, select 'Journal\Transaction\Credit'.</span></span>
39. <span data-ttu-id="6e02b-186">คลิก ผูก</span><span class="sxs-lookup"><span data-stu-id="6e02b-186">Click Bind.</span></span>
40. <span data-ttu-id="6e02b-187">ในแผนภูมิ เลือก 'LedgerJournal\<Relations\LedgerJournalTrans'</span><span class="sxs-lookup"><span data-stu-id="6e02b-187">In the tree, select 'LedgerJournal\<Relations\LedgerJournalTrans'.</span></span>
41. <span data-ttu-id="6e02b-188">ในแผนภูมิ เลือก 'สมุดรายวัน\ธุรกรรม'</span><span class="sxs-lookup"><span data-stu-id="6e02b-188">In the tree, select 'Journal\Transaction'.</span></span>
42. <span data-ttu-id="6e02b-189">คลิก ผูก</span><span class="sxs-lookup"><span data-stu-id="6e02b-189">Click Bind.</span></span>
43. <span data-ttu-id="6e02b-190">ในแผนภูมิ เลือก 'LedgerJournal\Journal batch number(JournalNum)'</span><span class="sxs-lookup"><span data-stu-id="6e02b-190">In the tree, select 'LedgerJournal\Journal batch number(JournalNum)'.</span></span>
44. <span data-ttu-id="6e02b-191">ในแผนภูมิ เลือก 'สมุดรายวัน\ชุดงาน'</span><span class="sxs-lookup"><span data-stu-id="6e02b-191">In the tree, select 'Journal\Batch'.</span></span>
45. <span data-ttu-id="6e02b-192">คลิก ผูก</span><span class="sxs-lookup"><span data-stu-id="6e02b-192">Click Bind.</span></span>
46. <span data-ttu-id="6e02b-193">ในแผนภูมิ ให้เลือก 'LedgerJournal'</span><span class="sxs-lookup"><span data-stu-id="6e02b-193">In the tree, select 'LedgerJournal'.</span></span>
47. <span data-ttu-id="6e02b-194">ในแผนภูมิ ให้เลือก 'สมุดบัญชี'</span><span class="sxs-lookup"><span data-stu-id="6e02b-194">In the tree, select 'Journal'.</span></span>
48. <span data-ttu-id="6e02b-195">คลิก ผูก</span><span class="sxs-lookup"><span data-stu-id="6e02b-195">Click Bind.</span></span>
49. <span data-ttu-id="6e02b-196">ในแผนภูมิ ขยาย 'มิติ'</span><span class="sxs-lookup"><span data-stu-id="6e02b-196">In the tree, expand 'Dimensions'.</span></span>
50. <span data-ttu-id="6e02b-197">ในแผนภูมิ ขยาย 'มิติ\บัญชีหลักและมิติ'</span><span class="sxs-lookup"><span data-stu-id="6e02b-197">In the tree, expand 'Dimensions\Main account and dimensions'.</span></span>
51. <span data-ttu-id="6e02b-198">ในแผนภูมิ ขยาย 'มิติ\บัญชีหลักและมิติ'\การกำหนด'</span><span class="sxs-lookup"><span data-stu-id="6e02b-198">In the tree, expand 'Dimensions\Main account and dimensions\Definition'.</span></span>
52. <span data-ttu-id="6e02b-199">ในแผนภูมิ เลือก 'มิติ\บัญชีหลักและมิติ'\การกำหนด\ชื่อ'</span><span class="sxs-lookup"><span data-stu-id="6e02b-199">In the tree, select 'Dimensions\Main account and dimensions\Definition\Name'.</span></span>
53. <span data-ttu-id="6e02b-200">ในแผนภูมิ เลือก 'การตั้งค่ามิติ\รหัส'</span><span class="sxs-lookup"><span data-stu-id="6e02b-200">In the tree, select 'Dimensions setting\Code'.</span></span>
54. <span data-ttu-id="6e02b-201">คลิก ผูก</span><span class="sxs-lookup"><span data-stu-id="6e02b-201">Click Bind.</span></span>
55. <span data-ttu-id="6e02b-202">ในแผนภูมิ เลือก 'มิติ\บัญชีหลักและมิติ'\การกำหนด\ชื่อคอลัมน์รายงาน'</span><span class="sxs-lookup"><span data-stu-id="6e02b-202">In the tree, select 'Dimensions\Main account and dimensions\Definition\Report column name'.</span></span>
56. <span data-ttu-id="6e02b-203">ในแผนภูมิ เลือก 'การตั้งค่ามิติ\ชื่อ'</span><span class="sxs-lookup"><span data-stu-id="6e02b-203">In the tree, select 'Dimensions setting\Name'.</span></span>
57. <span data-ttu-id="6e02b-204">คลิก ผูก</span><span class="sxs-lookup"><span data-stu-id="6e02b-204">Click Bind.</span></span>
58. <span data-ttu-id="6e02b-205">ในแผนภูมิ เลือก 'มิติ\บัญชีหลักและมิติ'</span><span class="sxs-lookup"><span data-stu-id="6e02b-205">In the tree, select 'Dimensions\Main account and dimensions'.</span></span>
59. <span data-ttu-id="6e02b-206">ในแผนภูมิ เลือก 'การตั้งค่ามิติ'</span><span class="sxs-lookup"><span data-stu-id="6e02b-206">In the tree, select 'Dimensions setting'.</span></span>
60. <span data-ttu-id="6e02b-207">คลิก ผูก</span><span class="sxs-lookup"><span data-stu-id="6e02b-207">Click Bind.</span></span>
61. <span data-ttu-id="6e02b-208">ในแผนภูมิ ให้เลือก 'บริษัท'</span><span class="sxs-lookup"><span data-stu-id="6e02b-208">In the tree, select 'Company'.</span></span>
62. <span data-ttu-id="6e02b-209">คลิก แก้ไข</span><span class="sxs-lookup"><span data-stu-id="6e02b-209">Click Edit.</span></span>
63. <span data-ttu-id="6e02b-210">ในฟิลด์ expressionAsStringText ให้ป้อน 'Company.'find()'.'name()''</span><span class="sxs-lookup"><span data-stu-id="6e02b-210">In the expressionAsStringText field, enter 'Company.'find()'.'name()''.</span></span>
    * <span data-ttu-id="6e02b-211">Company.'find()'.'name()'</span><span class="sxs-lookup"><span data-stu-id="6e02b-211">Company.'find()'.'name()'</span></span>  
64. <span data-ttu-id="6e02b-212">คลิก บันทึก</span><span class="sxs-lookup"><span data-stu-id="6e02b-212">Click Save.</span></span>
65. <span data-ttu-id="6e02b-213">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="6e02b-213">Close the page.</span></span>
66. <span data-ttu-id="6e02b-214">คลิก บันทึก</span><span class="sxs-lookup"><span data-stu-id="6e02b-214">Click Save.</span></span>
67. <span data-ttu-id="6e02b-215">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="6e02b-215">Close the page.</span></span>

## <a name="complete-this-draft-models-version"></a><span data-ttu-id="6e02b-216">ทำรุ่นของแบบจำลองร่างนี้ให้เสร็จสมบูรณ์</span><span class="sxs-lookup"><span data-stu-id="6e02b-216">Complete this draft model’s version</span></span>
1. <span data-ttu-id="6e02b-217">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="6e02b-217">Close the page.</span></span>
2. <span data-ttu-id="6e02b-218">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="6e02b-218">Close the page.</span></span>
3. <span data-ttu-id="6e02b-219">คลิก เปลี่ยนแปลงสถานะ</span><span class="sxs-lookup"><span data-stu-id="6e02b-219">Click Change status.</span></span>
4. <span data-ttu-id="6e02b-220">คลิกเสร็จสมบูรณ์</span><span class="sxs-lookup"><span data-stu-id="6e02b-220">Click Complete.</span></span>
5. <span data-ttu-id="6e02b-221">คลิก ตกลง</span><span class="sxs-lookup"><span data-stu-id="6e02b-221">Click OK.</span></span>

