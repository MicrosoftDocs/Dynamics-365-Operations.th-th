---
title: ER ใช้มิติทางการเงินเป็นแหล่งข้อมูล (ส่วนที่ 2 - การแม็ปแบบจำลอง)
description: หัวข้อนี้อธิบายวิธีการตั้งค่าคอนฟิกแบบโมเดลการรายงานทางอิเล็กทรอนิกส์ (ER) เพื่อใช้มิติทางการเงินเป็นแหล่งข้อมูลของรายงาน ER (ส่วนที่ 2)
author: NickSelin
ms.date: 05/27/2020
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: ERSolutionTable, ERDataModelDesigner, ERModelMappingTable, ERModelMappingDesigner, ERExpressionDesignerFormula
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 1e6f5ffbebdfcd9f945e6237904d80e8734b0220
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 03/31/2021
ms.locfileid: "5752447"
---
# <a name="er-use-financial-dimensions-as-a-data-source-part-2---model-mapping"></a><span data-ttu-id="fafb0-104">ER ใช้มิติทางการเงินเป็นแหล่งข้อมูล (ส่วนที่ 2 - การแม็ปแบบจำลอง)</span><span class="sxs-lookup"><span data-stu-id="fafb0-104">ER Use financial dimensions as a data source (Part 2 - Model mapping)</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="fafb0-105">ขั้นตอนต่อไปนี้อธิบายวิธีการที่ผู้ใช้ที่ถูกกำหนดบทบาทผู้ดูแลระบบหรือนักพัฒนาการรายงานทางอิเล็กทรอนิกส์สามารถตั้งค่าคอนฟิกแบบจำลองการรายงานทางอิเล็กทรอนิกส์ (ER) (ER) เพื่อใช้มิติทางการเงินเป็นแหล่งข้อมูลสำหรับรายงาน ER </span><span class="sxs-lookup"><span data-stu-id="fafb0-105">The following steps explain how a user assigned to the system administrator or electronic reporting developer role can configure an Electronic reporting (ER) model to use financial dimensions as a data source for ER reports.</span></span> <span data-ttu-id="fafb0-106">สามารถดำเนินการขั้นตอนเหล่านี้ได้ในบริษัทใดก็ได้ </span><span class="sxs-lookup"><span data-stu-id="fafb0-106">These steps can be performed in any company.</span></span>

<span data-ttu-id="fafb0-107">เพื่อทำขั้นตอนเหล่านี้ให้เสร็จสมบูรณ์ อันดับแรกคุณต้องทำขั้นตอนต่างๆ ในกระบวนงาน "ER ใช้มิติทางการเงินเป็นแหล่งข้อมูล (ส่วนที่ 1: แบบจำลองข้อมูล)"</span><span class="sxs-lookup"><span data-stu-id="fafb0-107">To complete these steps, you must first complete the steps in the "ER Use financial dimensions as a data source (Part 1: Design data model" procedure.</span></span>


## <a name="add-required-data-sources-to-model-mapping"></a><span data-ttu-id="fafb0-108">เพิ่มแหล่งข้อมูลที่จำเป็นไปยังการแม็ปแบบจำลอง</span><span class="sxs-lookup"><span data-stu-id="fafb0-108">Add required data sources to model mapping</span></span>
1. <span data-ttu-id="fafb0-109">ไปที่ การจัดการองค์กร > การรายงานทางอิเล็กทรอนิกส์ > การตั้งค่าคอนฟิก</span><span class="sxs-lookup"><span data-stu-id="fafb0-109">Go to Organization administration > Electronic reporting > Configurations.</span></span>
2. <span data-ttu-id="fafb0-110">ในแผนภูมิ เลือก 'แบบจำลองตัวอย่างมิติทางการเงิน'</span><span class="sxs-lookup"><span data-stu-id="fafb0-110">In the tree, select 'Financial dimensions sample model'.</span></span>
3. <span data-ttu-id="fafb0-111">คลิก ตัวออกแบบ</span><span class="sxs-lookup"><span data-stu-id="fafb0-111">Click Designer.</span></span>
4. <span data-ttu-id="fafb0-112">คลิก แม็ปแบบจำลองกับแหล่งข้อมูล</span><span class="sxs-lookup"><span data-stu-id="fafb0-112">Click Map model to datasource.</span></span>
5. <span data-ttu-id="fafb0-113">คลิก สร้าง</span><span class="sxs-lookup"><span data-stu-id="fafb0-113">Click New.</span></span>
6. <span data-ttu-id="fafb0-114">ในฟิลด์คำนิยาม ให้เลือก รายการ</span><span class="sxs-lookup"><span data-stu-id="fafb0-114">In the Definition field, select Entry.</span></span>
7. <span data-ttu-id="fafb0-115">ในฟิลด์ ชื่อ ให้พิมพ์ 'การแม็ปข้อมูลมิติ'</span><span class="sxs-lookup"><span data-stu-id="fafb0-115">In the Name field, type 'Dimensions data mapping'.</span></span>
8. <span data-ttu-id="fafb0-116">ในฟิลด์คำนิยาม ให้พิมพ์ 'การแม็ปข้อมูลมิติ'</span><span class="sxs-lookup"><span data-stu-id="fafb0-116">In the Description field, type 'Dimensions data mapping'.</span></span>
9. <span data-ttu-id="fafb0-117">คลิก บันทึก</span><span class="sxs-lookup"><span data-stu-id="fafb0-117">Click Save.</span></span>
10. <span data-ttu-id="fafb0-118">คลิก ตัวออกแบบ</span><span class="sxs-lookup"><span data-stu-id="fafb0-118">Click Designer.</span></span>
11. <span data-ttu-id="fafb0-119">ในแผนภูมิ ให้เลือก 'Dynamics 365 for Operations\ตาราง'</span><span class="sxs-lookup"><span data-stu-id="fafb0-119">In the tree, select 'Dynamics 365 for Operations\Table'.</span></span>
12. <span data-ttu-id="fafb0-120">คลิก เพิ่มราก</span><span class="sxs-lookup"><span data-stu-id="fafb0-120">Click Add root.</span></span>
13. <span data-ttu-id="fafb0-121">ในฟิลด์ชื่อ พิมพ์ 'บริษัท'</span><span class="sxs-lookup"><span data-stu-id="fafb0-121">In the Name field, type 'Company'.</span></span>
14. <span data-ttu-id="fafb0-122">ในฟิลด์ตาราง พิมพ์ 'CompanyInfo'</span><span class="sxs-lookup"><span data-stu-id="fafb0-122">In the Table field, type 'CompanyInfo'.</span></span>
15. <span data-ttu-id="fafb0-123">คลิก ตกลง ระบบจะนำเข้าข้อมูลการชำระเงิน</span><span class="sxs-lookup"><span data-stu-id="fafb0-123">Click OK.</span></span>
16. <span data-ttu-id="fafb0-124">ในแผนภูมิ เลือก 'ฟังก์ชัน\รายละเอียดมิติทางการเงิน'</span><span class="sxs-lookup"><span data-stu-id="fafb0-124">In the tree, select 'Functions\Financial dimensions details'.</span></span>
17. <span data-ttu-id="fafb0-125">คลิก เพิ่มราก</span><span class="sxs-lookup"><span data-stu-id="fafb0-125">Click Add root.</span></span>
    * <span data-ttu-id="fafb0-126">แหล่งข้อมูลนี้ระบุว่าจะกำหนดขอบเขตของมิติทางการเงินสำหรับรายงานใดๆ ที่จะใช้แบบจำลองนี้เป็นแหล่งข้อมูลอย่างไร</span><span class="sxs-lookup"><span data-stu-id="fafb0-126">This data source specifies how the scope of financial dimensions will be defined for any report that will use this model as a data source.</span></span>  
18. <span data-ttu-id="fafb0-127">ในฟิลด์ชื่อ ให้พิมพ์ค่า </span><span class="sxs-lookup"><span data-stu-id="fafb0-127">In the Name field, type a value.</span></span>
19. <span data-ttu-id="fafb0-128">เลือก ใช่ ในฟิลด์ขอข้อมูลมิติ</span><span class="sxs-lookup"><span data-stu-id="fafb0-128">Select Yes in the Ask for dimensions field.</span></span>
    * <span data-ttu-id="fafb0-129">เลือกใช่เพื่ออนุญาตให้ผู้ใช้สามารถเลือกมิติในเวลาที่ใช้ในการผลิตในแบบฟอร์มกล่องโต้ตอบผู้ใช้ </span><span class="sxs-lookup"><span data-stu-id="fafb0-129">Select Yes to allow the user to select dimensions at run-time on the User dialog form.</span></span> <span data-ttu-id="fafb0-130">ถ้าตั้งค่าเป็นไม่ มิติทางการเงินทั้งหมดของอินสแตนซ์ปัจจุบันจะถูกใช้โดยค่าเริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="fafb0-130">If set to No, all financial dimensions of the current instance will be used by default.</span></span>  
20. <span data-ttu-id="fafb0-131">ในฟิลด์การเลือกมิติทางการเงิน เลือก 'นิติบุคคล'</span><span class="sxs-lookup"><span data-stu-id="fafb0-131">In the Financial dimensions selection field, select 'Legal entity'.</span></span>
    * <span data-ttu-id="fafb0-132">เลือกทั้งหมดเพื่ออนุญาตให้ผู้ใช้สามารถเลือกมิติที่ต้องการสำหรับอินสแตนซ์ปัจจุบันในฟิลด์การค้นหา </span><span class="sxs-lookup"><span data-stu-id="fafb0-132">Select All to allow the user to select desire dimensions for the current  instance in the Lookup field.</span></span>  <span data-ttu-id="fafb0-133">เลือกนิติบุคคลที่จะอนุญาตให้ผู้ใช้สามารถเลือกมิติสำหรับบริษัทในฟิลด์การค้นหา </span><span class="sxs-lookup"><span data-stu-id="fafb0-133">Select Legal entity to allow the user to select dimensions for the company in the Lookup field.</span></span>  <span data-ttu-id="fafb0-134">เลือกมิติเพื่ออนุญาตให้ผู้ใช้สามารถเลือกมิติโดยใช้ชุดมิติเดียว</span><span class="sxs-lookup"><span data-stu-id="fafb0-134">Select Dimension to allow the user to select dimensions using a single dimension set.</span></span>  
21. <span data-ttu-id="fafb0-135">เลือก ใช่ ในฟิลด์ขอข้อมูลบัญชีหลัก</span><span class="sxs-lookup"><span data-stu-id="fafb0-135">Select Yes in the Ask for main account field.</span></span>
    * <span data-ttu-id="fafb0-136">ตั้งค่า 'ขอข้อมูลบัญชีหลัก' เป็น 'ใช่' เพื่ออนุญาตให้ผู้ใช้สามารถเลือกบัญชีหลักเป็นส่วนหนึ่งของรายการของมิติ</span><span class="sxs-lookup"><span data-stu-id="fafb0-136">Set 'Ask for main account' to Yes to allow users to select the main account as part of the list of dimensions.</span></span>   <span data-ttu-id="fafb0-137">ถ้าตั้งค่าเป็น ไม่ บัญชีหลักจะไม่ถูกรวมเข้าในรายการของมิติ และตัวเลือก 'บัญชีหลักเป็นข้อมูลบังคับ' จะถูกเปิดใช้งาน</span><span class="sxs-lookup"><span data-stu-id="fafb0-137">If set to No, the main account will not be included to the list of dimensions and the 'Is main account mandatory' option is enabled.</span></span> <span data-ttu-id="fafb0-138">ถ้า 'บัญชีหลักเป็นข้อมูลบังคับ' ถูกตั้งค่าเป็น ใช่ ให้รวมบัญชีหลักในรายการของมิติโดยไม่คำนึงถึงการเลือกของผู้ใช้</span><span class="sxs-lookup"><span data-stu-id="fafb0-138">If "Is main account mandatory' is set to Yes, include the main account in the list of dimensions regardless of the user's selection.</span></span>  
22. <span data-ttu-id="fafb0-139">คลิก ตกลง </span><span class="sxs-lookup"><span data-stu-id="fafb0-139">Click OK.</span></span>
<span data-ttu-id="fafb0-140">![เพจตัวออกแบบการแม็ปแบบจำลอง ER](../media/er-financial-dimensions-guides-model-mapping1.png)</span><span class="sxs-lookup"><span data-stu-id="fafb0-140">![ER model mapping designer page](../media/er-financial-dimensions-guides-model-mapping1.png)</span></span>
23. <span data-ttu-id="fafb0-141">ในแผนภูมิ ให้เลือก 'Dynamics 365 for Operations\เรกคอร์ดตาราง'</span><span class="sxs-lookup"><span data-stu-id="fafb0-141">In the tree, select 'Dynamics 365 for Operations\Table records'.</span></span>
24. <span data-ttu-id="fafb0-142">คลิก เพิ่มราก</span><span class="sxs-lookup"><span data-stu-id="fafb0-142">Click Add root.</span></span>
25. <span data-ttu-id="fafb0-143">ในฟิลด์ชื่อ ให้พิมพ์ 'LedgerJournal'</span><span class="sxs-lookup"><span data-stu-id="fafb0-143">In the Name field, type 'LedgerJournal'.</span></span>
26. <span data-ttu-id="fafb0-144">เลือก ใช่ในการขอฟิลด์การสอบถาม</span><span class="sxs-lookup"><span data-stu-id="fafb0-144">Select Yes in the Ask for query field.</span></span>
27. <span data-ttu-id="fafb0-145">ในฟิลด์ตาราง พิมพ์ 'LedgerJournalTable'</span><span class="sxs-lookup"><span data-stu-id="fafb0-145">In the Table field, type 'LedgerJournalTable'.</span></span>
28. <span data-ttu-id="fafb0-146">คลิก ตกลง </span><span class="sxs-lookup"><span data-stu-id="fafb0-146">Click OK.</span></span>
<span data-ttu-id="fafb0-147">![เพจตัวออกแบบการแม็ปแบบจำลอง ER](../media/er-financial-dimensions-guides-model-mapping2.png)</span><span class="sxs-lookup"><span data-stu-id="fafb0-147">![ER model mapping designer page](../media/er-financial-dimensions-guides-model-mapping2.png)</span></span>

## <a name="map-data-model-elements-to-added-data-sources"></a><span data-ttu-id="fafb0-148">แม็ปองค์ประกอบแบบจำลองข้อมูลไปยังแหล่งข้อมูลที่เพิ่ม</span><span class="sxs-lookup"><span data-stu-id="fafb0-148">Map data model elements to added data sources</span></span>
1. <span data-ttu-id="fafb0-149">ในแผนภูมิ ให้ขยาย 'สมุดบัญชี'</span><span class="sxs-lookup"><span data-stu-id="fafb0-149">In the tree, expand 'Journal'.</span></span>
2. <span data-ttu-id="fafb0-150">ในแผนภูมิ ให้ขยาย 'สมุดรายวัน\ธุรกรรม'</span><span class="sxs-lookup"><span data-stu-id="fafb0-150">In the tree, expand 'Journal\Transaction'.</span></span>
3. <span data-ttu-id="fafb0-151">ในแผนภูมิ ให้ขยาย 'สมุดรายวัน\ธุรกรรม\ข้อมูลมิติ'</span><span class="sxs-lookup"><span data-stu-id="fafb0-151">In the tree, expand 'Journal\Transaction\Dimensions data'.</span></span>
4. <span data-ttu-id="fafb0-152">ในแผนภูมิ ขยาย 'การตั้งค่ามิติ'</span><span class="sxs-lookup"><span data-stu-id="fafb0-152">In the tree, expand 'Dimensions setting'.</span></span>
5. <span data-ttu-id="fafb0-153">ในแผนภูมิ ขยาย 'LedgerJournal'</span><span class="sxs-lookup"><span data-stu-id="fafb0-153">In the tree, expand 'LedgerJournal'.</span></span>
6. <span data-ttu-id="fafb0-154">ในแผนภูมิ ขยาย 'LedgerJournal\<Relations'</span><span class="sxs-lookup"><span data-stu-id="fafb0-154">In the tree, expand 'LedgerJournal\<Relations'.</span></span>
7. <span data-ttu-id="fafb0-155">ในแผนภูมิ ขยาย 'LedgerJournal\<Relations\LedgerJournalTrans'</span><span class="sxs-lookup"><span data-stu-id="fafb0-155">In the tree, expand 'LedgerJournal\<Relations\LedgerJournalTrans'.</span></span>
8. <span data-ttu-id="fafb0-156">ในแผนภูมิ เลือก 'LedgerJournal\<Relations\LedgerJournalTrans\Voucher'</span><span class="sxs-lookup"><span data-stu-id="fafb0-156">In the tree, select 'LedgerJournal\<Relations\LedgerJournalTrans\Voucher'.</span></span>
9. <span data-ttu-id="fafb0-157">ในแผนภูมิ เลือก 'สมุดรายวัน\ธุรกรรม\ใบสำคัญ'</span><span class="sxs-lookup"><span data-stu-id="fafb0-157">In the tree, select 'Journal\Transaction\Voucher'.</span></span>
10. <span data-ttu-id="fafb0-158">คลิก ผูก</span><span class="sxs-lookup"><span data-stu-id="fafb0-158">Click Bind.</span></span>
11. <span data-ttu-id="fafb0-159">ในแผนภูมิ เลือก 'LedgerJournal\<Relations\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension)'</span><span class="sxs-lookup"><span data-stu-id="fafb0-159">In the tree, select 'LedgerJournal\<Relations\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension)'.</span></span>
    * <span data-ttu-id="fafb0-160">โปรดทราบว่าสำหรับการอ้างอิงใดๆ ของมิติทางการเงินที่ตั้งค่าเป็น ตัวอย่างเช่น LedgerDimension รายการแหล่งข้อมูลที่เกี่ยวข้องจะพร้อมใช้งาน (LedgerDimension.Dimension) </span><span class="sxs-lookup"><span data-stu-id="fafb0-160">Note that for any reference to financial dimensions that is set to, for instance, LedgerDimension, a corresponding data source item is available (LedgerDimension.Dimension).</span></span> <span data-ttu-id="fafb0-161">รายการแหล่งข้อมูลนี้เสนอให้ตั้งค่ามิติทางการเงินของมิตินั้นเป็นรายการของเรกคอร์ด</span><span class="sxs-lookup"><span data-stu-id="fafb0-161">This data source item offers the financial dimensions of that dimensions set as the record's list.</span></span>  
12. <span data-ttu-id="fafb0-162">ในแผนภูมิ ขยาย 'LedgerJournal\<Relations\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension)'</span><span class="sxs-lookup"><span data-stu-id="fafb0-162">In the tree, expand 'LedgerJournal\<Relations\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension)'.</span></span>
13. <span data-ttu-id="fafb0-163">ในแผนภูมิ ขยาย 'LedgerJournal\<Relations\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension)\บัญชีหลักและมิติ'</span><span class="sxs-lookup"><span data-stu-id="fafb0-163">In the tree, expand 'LedgerJournal\<Relations\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension)\Main account and dimensions'.</span></span>
14. <span data-ttu-id="fafb0-164">ในแผนภูมิ ขยาย 'LedgerJournal\<Relations\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension)\บัญชีหลักและมิติ\ค่า'</span><span class="sxs-lookup"><span data-stu-id="fafb0-164">In the tree, expand 'LedgerJournal\<Relations\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension)\Main account and dimensions\Value'.</span></span>
15. <span data-ttu-id="fafb0-165">ในแผนภูมิ ขยาย 'LedgerJournal\<Relations\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension)\บัญชีหลักและมิติ\การกำหนด'</span><span class="sxs-lookup"><span data-stu-id="fafb0-165">In the tree, expand 'LedgerJournal\<Relations\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension)\Main account and dimensions\Definition'.</span></span>
16. <span data-ttu-id="fafb0-166">ในแผนภูมิ เลือก 'LedgerJournal\<Relations\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension)\บัญชีหลักและมิติ\การกำหนด\ชื่อ'</span><span class="sxs-lookup"><span data-stu-id="fafb0-166">In the tree, select 'LedgerJournal\<Relations\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension)\Main account and dimensions\Definition\Name'.</span></span>
17. <span data-ttu-id="fafb0-167">ในแผนภูมิ เลือก 'สมุดรายวัน\ธุรกรรม\ข้อมูลมิติ\ชื่อ'</span><span class="sxs-lookup"><span data-stu-id="fafb0-167">In the tree, select 'Journal\Transaction\Dimensions data\Name'.</span></span>
18. <span data-ttu-id="fafb0-168">คลิก ผูก</span><span class="sxs-lookup"><span data-stu-id="fafb0-168">Click Bind.</span></span>
19. <span data-ttu-id="fafb0-169">ในแผนภูมิ เลือก 'LedgerJournal\<Relations\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension)\บัญชีหลักและมิติ\ค่า\คำอธิบาย'</span><span class="sxs-lookup"><span data-stu-id="fafb0-169">In the tree, select 'LedgerJournal\<Relations\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension)\Main account and dimensions\Value\Description'.</span></span>
20. <span data-ttu-id="fafb0-170">ในแผนภูมิ เลือก 'สมุดรายวัน\ธุรกรรม\ข้อมูลมิติ\คำอธิบาย'</span><span class="sxs-lookup"><span data-stu-id="fafb0-170">In the tree, select 'Journal\Transaction\Dimensions data\Description'.</span></span>
21. <span data-ttu-id="fafb0-171">คลิก ผูก</span><span class="sxs-lookup"><span data-stu-id="fafb0-171">Click Bind.</span></span>
22. <span data-ttu-id="fafb0-172">ในแผนภูมิ เลือก 'LedgerJournal\<Relations\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension)\บัญชีหลักและมิติ\ค่า\รหัส'</span><span class="sxs-lookup"><span data-stu-id="fafb0-172">In the tree, select 'LedgerJournal\<Relations\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension)\Main account and dimensions\Value\Code'.</span></span>
23. <span data-ttu-id="fafb0-173">ในแผนภูมิ เลือก 'สมุดรายวัน\ธุรกรรม\ข้อมูลมิติ\รหัส'</span><span class="sxs-lookup"><span data-stu-id="fafb0-173">In the tree, select 'Journal\Transaction\Dimensions data\Code'.</span></span>
24. <span data-ttu-id="fafb0-174">คลิก ผูก</span><span class="sxs-lookup"><span data-stu-id="fafb0-174">Click Bind.</span></span>
25. <span data-ttu-id="fafb0-175">ในแผนภูมิ เลือก 'LedgerJournal\<Relations\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension)\บัญชีหลักและมิติ'</span><span class="sxs-lookup"><span data-stu-id="fafb0-175">In the tree, select 'LedgerJournal\<Relations\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension)\Main account and dimensions'.</span></span>
26. <span data-ttu-id="fafb0-176">ในแผนภูมิ เลือก 'สมุดรายวัน\ธุรกรรม\ข้อมูลมิติ'</span><span class="sxs-lookup"><span data-stu-id="fafb0-176">In the tree, select 'Journal\Transaction\Dimensions data'.</span></span>
27. <span data-ttu-id="fafb0-177">คลิก ผูก</span><span class="sxs-lookup"><span data-stu-id="fafb0-177">Click Bind.</span></span>
<span data-ttu-id="fafb0-178">![เพจตัวออกแบบการแม็ปแบบจำลอง ER](../media/er-financial-dimensions-guides-model-mapping3.png)</span><span class="sxs-lookup"><span data-stu-id="fafb0-178">![ER model mapping designer page](../media/er-financial-dimensions-guides-model-mapping3.png)</span></span>
28. <span data-ttu-id="fafb0-179">ในแผนภูมิ เลือก 'LedgerJournal\<Relations\LedgerJournalTrans\Debit(AmountCurDebit)'</span><span class="sxs-lookup"><span data-stu-id="fafb0-179">In the tree, select 'LedgerJournal\<Relations\LedgerJournalTrans\Debit(AmountCurDebit)'.</span></span>
29. <span data-ttu-id="fafb0-180">ในแผนภูมิ เลือก 'สมุดรายวัน\ธุรกรรม\เดบิต'</span><span class="sxs-lookup"><span data-stu-id="fafb0-180">In the tree, select 'Journal\Transaction\Debit'.</span></span>
30. <span data-ttu-id="fafb0-181">คลิก ผูก</span><span class="sxs-lookup"><span data-stu-id="fafb0-181">Click Bind.</span></span>
31. <span data-ttu-id="fafb0-182">ในแผนภูมิ เลือก 'LedgerJournal\<Relations\LedgerJournalTrans\Date(TransDate)'</span><span class="sxs-lookup"><span data-stu-id="fafb0-182">In the tree, select 'LedgerJournal\<Relations\LedgerJournalTrans\Date(TransDate)'.</span></span>
32. <span data-ttu-id="fafb0-183">ในแผนภูมิ เลือก 'สมุดรายวัน\ธุรกรรม\วันที่'</span><span class="sxs-lookup"><span data-stu-id="fafb0-183">In the tree, select 'Journal\Transaction\Date'.</span></span>
33. <span data-ttu-id="fafb0-184">คลิก ผูก</span><span class="sxs-lookup"><span data-stu-id="fafb0-184">Click Bind.</span></span>
34. <span data-ttu-id="fafb0-185">ในแผนภูมิ เลือก 'LedgerJournal\<Relations\LedgerJournalTrans\Currency(CurrencyCode)'</span><span class="sxs-lookup"><span data-stu-id="fafb0-185">In the tree, select 'LedgerJournal\<Relations\LedgerJournalTrans\Currency(CurrencyCode)'.</span></span>
35. <span data-ttu-id="fafb0-186">ในแผนภูมิ เลือก 'สมุดรายวัน\ธุรกรรม\สกุลเงิน'</span><span class="sxs-lookup"><span data-stu-id="fafb0-186">In the tree, select 'Journal\Transaction\Currency'.</span></span>
36. <span data-ttu-id="fafb0-187">คลิก ผูก</span><span class="sxs-lookup"><span data-stu-id="fafb0-187">Click Bind.</span></span>
37. <span data-ttu-id="fafb0-188">ในแผนภูมิ เลือก 'LedgerJournal\<Relations\LedgerJournalTrans\Credit(AmountCurCredit)'</span><span class="sxs-lookup"><span data-stu-id="fafb0-188">In the tree, select 'LedgerJournal\<Relations\LedgerJournalTrans\Credit(AmountCurCredit)'.</span></span>
38. <span data-ttu-id="fafb0-189">ในแผนภูมิ เลือก 'สมุดรายวัน\ธุรกรรม\เครดิต'</span><span class="sxs-lookup"><span data-stu-id="fafb0-189">In the tree, select 'Journal\Transaction\Credit'.</span></span>
39. <span data-ttu-id="fafb0-190">คลิก ผูก</span><span class="sxs-lookup"><span data-stu-id="fafb0-190">Click Bind.</span></span>
40. <span data-ttu-id="fafb0-191">ในแผนภูมิ เลือก 'LedgerJournal\<Relations\LedgerJournalTrans'</span><span class="sxs-lookup"><span data-stu-id="fafb0-191">In the tree, select 'LedgerJournal\<Relations\LedgerJournalTrans'.</span></span>
41. <span data-ttu-id="fafb0-192">ในแผนภูมิ เลือก 'สมุดรายวัน\ธุรกรรม'</span><span class="sxs-lookup"><span data-stu-id="fafb0-192">In the tree, select 'Journal\Transaction'.</span></span>
42. <span data-ttu-id="fafb0-193">คลิก ผูก</span><span class="sxs-lookup"><span data-stu-id="fafb0-193">Click Bind.</span></span>
43. <span data-ttu-id="fafb0-194">ในแผนภูมิ เลือก 'LedgerJournal\Journal batch number(JournalNum)'</span><span class="sxs-lookup"><span data-stu-id="fafb0-194">In the tree, select 'LedgerJournal\Journal batch number(JournalNum)'.</span></span>
44. <span data-ttu-id="fafb0-195">ในแผนภูมิ เลือก 'สมุดรายวัน\ชุดงาน'</span><span class="sxs-lookup"><span data-stu-id="fafb0-195">In the tree, select 'Journal\Batch'.</span></span>
45. <span data-ttu-id="fafb0-196">คลิก ผูก</span><span class="sxs-lookup"><span data-stu-id="fafb0-196">Click Bind.</span></span>
46. <span data-ttu-id="fafb0-197">ในแผนภูมิ ให้เลือก 'LedgerJournal'</span><span class="sxs-lookup"><span data-stu-id="fafb0-197">In the tree, select 'LedgerJournal'.</span></span>
47. <span data-ttu-id="fafb0-198">ในแผนภูมิ ให้เลือก 'สมุดบัญชี'</span><span class="sxs-lookup"><span data-stu-id="fafb0-198">In the tree, select 'Journal'.</span></span>
48. <span data-ttu-id="fafb0-199">คลิก ผูก</span><span class="sxs-lookup"><span data-stu-id="fafb0-199">Click Bind.</span></span>
49. <span data-ttu-id="fafb0-200">ในแผนภูมิ ขยาย 'มิติ'</span><span class="sxs-lookup"><span data-stu-id="fafb0-200">In the tree, expand 'Dimensions'.</span></span>
50. <span data-ttu-id="fafb0-201">ในแผนภูมิ ขยาย 'มิติ\บัญชีหลักและมิติ'</span><span class="sxs-lookup"><span data-stu-id="fafb0-201">In the tree, expand 'Dimensions\Main account and dimensions'.</span></span>
51. <span data-ttu-id="fafb0-202">ในแผนภูมิ ขยาย 'มิติ\บัญชีหลักและมิติ'\การกำหนด'</span><span class="sxs-lookup"><span data-stu-id="fafb0-202">In the tree, expand 'Dimensions\Main account and dimensions\Definition'.</span></span>
52. <span data-ttu-id="fafb0-203">ในแผนภูมิ เลือก 'มิติ\บัญชีหลักและมิติ'\การกำหนด\ชื่อ'</span><span class="sxs-lookup"><span data-stu-id="fafb0-203">In the tree, select 'Dimensions\Main account and dimensions\Definition\Name'.</span></span>
53. <span data-ttu-id="fafb0-204">ในแผนภูมิ เลือก 'การตั้งค่ามิติ\รหัส'</span><span class="sxs-lookup"><span data-stu-id="fafb0-204">In the tree, select 'Dimensions setting\Code'.</span></span>
54. <span data-ttu-id="fafb0-205">คลิก ผูก</span><span class="sxs-lookup"><span data-stu-id="fafb0-205">Click Bind.</span></span>
55. <span data-ttu-id="fafb0-206">ในแผนภูมิ เลือก 'มิติ\บัญชีหลักและมิติ'\การกำหนด\ชื่อคอลัมน์รายงาน'</span><span class="sxs-lookup"><span data-stu-id="fafb0-206">In the tree, select 'Dimensions\Main account and dimensions\Definition\Report column name'.</span></span>
56. <span data-ttu-id="fafb0-207">ในแผนภูมิ เลือก 'การตั้งค่ามิติ\ชื่อ'</span><span class="sxs-lookup"><span data-stu-id="fafb0-207">In the tree, select 'Dimensions setting\Name'.</span></span>
57. <span data-ttu-id="fafb0-208">คลิก ผูก</span><span class="sxs-lookup"><span data-stu-id="fafb0-208">Click Bind.</span></span>
58. <span data-ttu-id="fafb0-209">ในแผนภูมิ เลือก 'มิติ\บัญชีหลักและมิติ'</span><span class="sxs-lookup"><span data-stu-id="fafb0-209">In the tree, select 'Dimensions\Main account and dimensions'.</span></span>
59. <span data-ttu-id="fafb0-210">ในแผนภูมิ เลือก 'การตั้งค่ามิติ'</span><span class="sxs-lookup"><span data-stu-id="fafb0-210">In the tree, select 'Dimensions setting'.</span></span>
60. <span data-ttu-id="fafb0-211">คลิก ผูก</span><span class="sxs-lookup"><span data-stu-id="fafb0-211">Click Bind.</span></span>
61. <span data-ttu-id="fafb0-212">ในแผนภูมิ ให้เลือก 'บริษัท'</span><span class="sxs-lookup"><span data-stu-id="fafb0-212">In the tree, select 'Company'.</span></span>
62. <span data-ttu-id="fafb0-213">คลิก แก้ไข</span><span class="sxs-lookup"><span data-stu-id="fafb0-213">Click Edit.</span></span>
63. <span data-ttu-id="fafb0-214">ในฟิลด์ expressionAsStringText ให้ป้อน 'Company.'find()'.'name()''</span><span class="sxs-lookup"><span data-stu-id="fafb0-214">In the expressionAsStringText field, enter 'Company.'find()'.'name()''.</span></span>
    * <span data-ttu-id="fafb0-215">Company.'find()'.'name()'</span><span class="sxs-lookup"><span data-stu-id="fafb0-215">Company.'find()'.'name()'</span></span>  
64. <span data-ttu-id="fafb0-216">คลิก บันทึก</span><span class="sxs-lookup"><span data-stu-id="fafb0-216">Click Save.</span></span>
<span data-ttu-id="fafb0-217">![เพจตัวออกแบบการแม็ปแบบจำลอง ER](../media/er-financial-dimensions-guides-model-mapping4.png)</span><span class="sxs-lookup"><span data-stu-id="fafb0-217">![ER model mapping designer page](../media/er-financial-dimensions-guides-model-mapping4.png)</span></span>
65. <span data-ttu-id="fafb0-218">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="fafb0-218">Close the page.</span></span>
66. <span data-ttu-id="fafb0-219">คลิก บันทึก</span><span class="sxs-lookup"><span data-stu-id="fafb0-219">Click Save.</span></span>
67. <span data-ttu-id="fafb0-220">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="fafb0-220">Close the page.</span></span>

## <a name="complete-this-draft-models-version"></a><span data-ttu-id="fafb0-221">ทำรุ่นของแบบจำลองร่างนี้ให้เสร็จสมบูรณ์</span><span class="sxs-lookup"><span data-stu-id="fafb0-221">Complete this draft model's version</span></span>
1. <span data-ttu-id="fafb0-222">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="fafb0-222">Close the page.</span></span>
2. <span data-ttu-id="fafb0-223">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="fafb0-223">Close the page.</span></span>
3. <span data-ttu-id="fafb0-224">คลิก เปลี่ยนแปลงสถานะ</span><span class="sxs-lookup"><span data-stu-id="fafb0-224">Click Change status.</span></span>
4. <span data-ttu-id="fafb0-225">คลิกเสร็จสมบูรณ์</span><span class="sxs-lookup"><span data-stu-id="fafb0-225">Click Complete.</span></span>
5. <span data-ttu-id="fafb0-226">คลิก ตกลง </span><span class="sxs-lookup"><span data-stu-id="fafb0-226">Click OK.</span></span>
<span data-ttu-id="fafb0-227">![เพจตัวออกแบบการแม็ปแบบจำลอง ER](../media/er-financial-dimensions-guides-model-mapping5.png)</span><span class="sxs-lookup"><span data-stu-id="fafb0-227">![ER model mapping designer page](../media/er-financial-dimensions-guides-model-mapping5.png)</span></span>


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]