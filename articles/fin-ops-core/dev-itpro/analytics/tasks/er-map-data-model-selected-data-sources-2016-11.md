---
title: แม็ปแบบจำลองข้อมูลไปยังแหล่งข้อมูลที่เลือกของ ER
description: ขั้นตอนต่อไปนี้อธิบายวิธีการที่ผู้ใช้ในบทบาทผู้ดูแลระบบหรือนักพัฒนาการรายงานทางอิเล็กทรอนิกส์ สามารถแม็ปแบบจำลองข้อมูลการรายงานทางอิเล็กทรอนิกส์ (ER) ไปยังแหล่งข้อมูล Microsoft Dynamics 365 Finance ที่เลือก
author: NickSelin
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ERWorkspace, ERSolutionTable, ERDataModelDesigner, ERModelMappingTable, ERModelMappingDesigner
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: d2d09370b0e08897799d40c41c20c21b58e885dc
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 12/05/2020
ms.locfileid: "4684318"
---
# <a name="er-map-data-model-to-selected-data-sources"></a><span data-ttu-id="b1e06-103">แม็ปแบบจำลองข้อมูลไปยังแหล่งข้อมูลที่เลือกของ ER</span><span class="sxs-lookup"><span data-stu-id="b1e06-103">ER Map data model to selected data sources</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="b1e06-104">ขั้นตอนต่อไปนี้อธิบายวิธีการที่ผู้ใช้ในบทบาทผู้ดูแลระบบหรือนักพัฒนาการรายงานทางอิเล็กทรอนิกส์ สามารถแม็ปแบบจำลองข้อมูลการรายงานทางอิเล็กทรอนิกส์ (ER) ไปยังแหล่งข้อมูลที่เลือก</span><span class="sxs-lookup"><span data-stu-id="b1e06-104">The following steps explain how a user in the System Administrator or Electronic Reporting Developer role can map an Electronic reporting (ER) data model to selected data sources.</span></span> <span data-ttu-id="b1e06-105">การแม็ปแบบจำลองนี้จะถูกใช้เป็นแหล่งข้อมูลภายหลังในการตั้งค่าคอนฟิกรูปแบบที่จะจัดการเอกสารการชำระเงินทางอิเล็กทรอนิกส์</span><span class="sxs-lookup"><span data-stu-id="b1e06-105">This model mapping will later be used as a data source in a format configuration that will be used to manage electronic payment documents.</span></span> <span data-ttu-id="b1e06-106">ในตัวอย่างนี้ คุณแม็ปแบบจำลองข้อมูลสำหรับบริษัทตัวอย่าง Litware, Inc. ไปยังแหล่งข้อมูล </span><span class="sxs-lookup"><span data-stu-id="b1e06-106">In this example, you map a data model for sample company, Litware, Inc. to data sources.</span></span> <span data-ttu-id="b1e06-107">เพื่อทำขั้นตอนเหล่านี้ให้เสร็จสมบูรณ์ ก่อนอื่นคุณต้องทำขั้นตอนให้เสร็จสมบูรณ์ในกระบวนงาน "เลือกแหล่งข้อมูลสำหรับการแม็ปแบบจำลอง"</span><span class="sxs-lookup"><span data-stu-id="b1e06-107">To complete these steps, you must first complete the steps in the "Select data sources for model mapping" procedure.</span></span>


## <a name="open-er-configurations-tree"></a><span data-ttu-id="b1e06-108">เปิดแผนภูมิการตั้งค่าคอนฟิก ER</span><span class="sxs-lookup"><span data-stu-id="b1e06-108">Open ER configurations tree</span></span>
1. <span data-ttu-id="b1e06-109">ไปที่การจัดการองค์กร > พื้นที่ทำงาน > การรายงานทางอิเล็กทรอนิกส์</span><span class="sxs-lookup"><span data-stu-id="b1e06-109">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
2. <span data-ttu-id="b1e06-110">คลิกการตั้งค่าคอนฟลิก</span><span class="sxs-lookup"><span data-stu-id="b1e06-110">Click Configurations.</span></span>

## <a name="select-created-model-mapping"></a><span data-ttu-id="b1e06-111">เลือก การแม็ปแบบจำลองที่สร้างขึ้น</span><span class="sxs-lookup"><span data-stu-id="b1e06-111">Select created model mapping</span></span>
1. <span data-ttu-id="b1e06-112">ในแผนภูมิ เลือก 'การชำระเงิน(แบบจำลองอย่างง่าย)'</span><span class="sxs-lookup"><span data-stu-id="b1e06-112">In the tree, select 'Payments (simplified model)'.</span></span>
    * <span data-ttu-id="b1e06-113">ตรวจสอบให้แน่ใจว่าการตั้งค่าคอนฟิกแบบจำลอง "การชำระเงิน (แบบจำลองแบบง่าย)" ถูกสร้างไว้ล่วงหน้า</span><span class="sxs-lookup"><span data-stu-id="b1e06-113">Make sure that the model configuration "Payments (simplified model)" has been created in advance.</span></span> <span data-ttu-id="b1e06-114">มิฉะนั้น ให้หยุดทันทีและกลับมาใหม่หลังจากที่อ่านคู่มืองานเสร็จสิ้นแล้ว 'สร้างการตั้งค่าคอนฟิกใหม่พร้อมกับแบบจำลองข้อมูลของโดเมนที่เลือก'</span><span class="sxs-lookup"><span data-stu-id="b1e06-114">Otherwise, stop now and return after completion of the task guide 'Create a new configuration with data model of the selected domain'.</span></span>  
2. <span data-ttu-id="b1e06-115">คลิก ตัวออกแบบจำลอง</span><span class="sxs-lookup"><span data-stu-id="b1e06-115">Click Model designer.</span></span>
3. <span data-ttu-id="b1e06-116">คลิก แม็ปแบบจำลองกับแหล่งข้อมูล</span><span class="sxs-lookup"><span data-stu-id="b1e06-116">Click Map model to datasource.</span></span>
4. <span data-ttu-id="b1e06-117">เลือก เรกคอร์ด 'การแม็ป CT'</span><span class="sxs-lookup"><span data-stu-id="b1e06-117">Select the 'CT mapping' record.</span></span>
    * <span data-ttu-id="b1e06-118">การแม็ป CT</span><span class="sxs-lookup"><span data-stu-id="b1e06-118">CT mapping</span></span>  

## <a name="bind-created-data-sources-to-data-model-elements"></a><span data-ttu-id="b1e06-119">ผูกแหล่งข้อมูลที่สร้างขึ้นกับองค์ประกอบแบบจำลองข้อมูล</span><span class="sxs-lookup"><span data-stu-id="b1e06-119">Bind created data sources to data model elements</span></span>
1. <span data-ttu-id="b1e06-120">คลิก ตัวออกแบบ</span><span class="sxs-lookup"><span data-stu-id="b1e06-120">Click Designer.</span></span>
2. <span data-ttu-id="b1e06-121">ในแผนภูมิ เลือก 'วันที่ & เวลาที่ประมวลผล(ProcessingDateTime)'</span><span class="sxs-lookup"><span data-stu-id="b1e06-121">In the tree, select 'Processing date & time(ProcessingDateTime)'.</span></span>
3. <span data-ttu-id="b1e06-122">ในแผนภูมิ เลือก 'การประมวลผลวันที่(วันที่และเวลาประมวลผล)'</span><span class="sxs-lookup"><span data-stu-id="b1e06-122">In the tree, select 'Processing date(ProcessingDateTime)'.</span></span>
4. <span data-ttu-id="b1e06-123">คลิก ผูก</span><span class="sxs-lookup"><span data-stu-id="b1e06-123">Click Bind.</span></span>
5. <span data-ttu-id="b1e06-124">ในแผนภูมิ เลือก 'การระบุรหัสประจำตัวข้อความการชำระเงิน(รหัสข้อความ)'</span><span class="sxs-lookup"><span data-stu-id="b1e06-124">In the tree, select 'Payment message identification(MessageIdentification)'.</span></span>
6. <span data-ttu-id="b1e06-125">ในแผนภูมิ ขยาย 'ธุรกรรม'</span><span class="sxs-lookup"><span data-stu-id="b1e06-125">In the tree, expand 'Transactions'.</span></span>
7. <span data-ttu-id="b1e06-126">ในแผนภูมิ เลือก 'ธุรกรรม\หมายเลขชุดงานสมุดรายวัน(JournalNum)'</span><span class="sxs-lookup"><span data-stu-id="b1e06-126">In the tree, select 'Transactions\Journal batch number(JournalNum)'.</span></span>
8. <span data-ttu-id="b1e06-127">คลิก ผูก</span><span class="sxs-lookup"><span data-stu-id="b1e06-127">Click Bind.</span></span>
9. <span data-ttu-id="b1e06-128">ในแผนภูมิ เลือก 'การชำระเงิน'</span><span class="sxs-lookup"><span data-stu-id="b1e06-128">In the tree, select 'Payments'.</span></span>
10. <span data-ttu-id="b1e06-129">ในแผนภูมิ เลือก 'ธุรกรรม'</span><span class="sxs-lookup"><span data-stu-id="b1e06-129">In the tree, select 'Transactions'.</span></span>
11. <span data-ttu-id="b1e06-130">คลิก ผูก</span><span class="sxs-lookup"><span data-stu-id="b1e06-130">Click Bind.</span></span>
12. <span data-ttu-id="b1e06-131">ในแผนภูมิ ขยาย 'การชำระเงิน= ธุรกรรม'</span><span class="sxs-lookup"><span data-stu-id="b1e06-131">In the tree, expand 'Payments= Transactions'.</span></span>
13. <span data-ttu-id="b1e06-132">ในแผนภูมิ ขยาย 'การชำระเงิน= ธุรกรรม\เจ้าหนี้'</span><span class="sxs-lookup"><span data-stu-id="b1e06-132">In the tree, expand 'Payments= Transactions\Creditor'.</span></span>
14. <span data-ttu-id="b1e06-133">ในแผนภูมิ ขยาย 'การชำระเงิน= ธุรกรรม\เจ้าหนี้\บัญชี'</span><span class="sxs-lookup"><span data-stu-id="b1e06-133">In the tree, expand 'Payments= Transactions\Creditor\Account'.</span></span>
15. <span data-ttu-id="b1e06-134">ในแผนภูมิ เลือก ' การชำระเงิน = ธุรกรรม\เจ้าหนี้\บัญชี\รหัสสกุลเงิน(สกุลเงิน)'</span><span class="sxs-lookup"><span data-stu-id="b1e06-134">In the tree, select 'Payments= Transactions\Creditor\Account\Currency code(Currency)'.</span></span>
16. <span data-ttu-id="b1e06-135">ในแผนภูมิ ขยาย 'ธุรกรรม\บัญชีธนาคารของผู้จัดจำหน่ายในบริษัทธุรกรรม()'</span><span class="sxs-lookup"><span data-stu-id="b1e06-135">In the tree, expand 'Transactions\vendBankAccountInTransactionCompany()'.</span></span>
17. <span data-ttu-id="b1e06-136">ในแผนภูมิ เลือก 'ธุรกรรม\บัญชีธนาคารของผู้จัดจำหน่ายในบริษัทธุรกรรม()\สกุลเงิน(รหัสสกุลเงิน)'</span><span class="sxs-lookup"><span data-stu-id="b1e06-136">In the tree, select 'Transactions\vendBankAccountInTransactionCompany()\Currency(CurrencyCode)'.</span></span>
18. <span data-ttu-id="b1e06-137">คลิก ผูก</span><span class="sxs-lookup"><span data-stu-id="b1e06-137">Click Bind.</span></span>
19. <span data-ttu-id="b1e06-138">ในแผนภูมิ เลือก 'การชำระเงิน= ธุรกรรม\เจ้าหนี้\บัญชี\รหัสIBAN(IBAN)'</span><span class="sxs-lookup"><span data-stu-id="b1e06-138">In the tree, select 'Payments= Transactions\Creditor\Account\IBAN code(IBAN)'.</span></span>
20. <span data-ttu-id="b1e06-139">ในแผนภูมิ เลือก 'ธุรกรรม\บัญชีธนาคารของผู้จัดจำหน่ายในบริษัทธุรกรรม()\รหัสIBAN(IBAN)'</span><span class="sxs-lookup"><span data-stu-id="b1e06-139">In the tree, select 'Transactions\vendBankAccountInTransactionCompany()\IBAN(BankIBAN)'.</span></span>
21. <span data-ttu-id="b1e06-140">คลิก ผูก</span><span class="sxs-lookup"><span data-stu-id="b1e06-140">Click Bind.</span></span>
22. <span data-ttu-id="b1e06-141">ในแผนภูมิ เลือก 'การชำระเงิน= ธุรกรรม\เจ้าหนี้\บัญชี\หมายเลข'</span><span class="sxs-lookup"><span data-stu-id="b1e06-141">In the tree, select 'Payments= Transactions\Creditor\Account\Number'.</span></span>
23. <span data-ttu-id="b1e06-142">ในแผนภูมิ เลือก 'ธุรกรรม\บัญชีธนาคารของผู้จัดจำหน่ายในบริษัทธุรกรรม()\หมายเลขบัญชีธนาคาร(AccountNum)'</span><span class="sxs-lookup"><span data-stu-id="b1e06-142">In the tree, select 'Transactions\vendBankAccountInTransactionCompany()\Bank account number(AccountNum)'.</span></span>
24. <span data-ttu-id="b1e06-143">คลิก ผูก</span><span class="sxs-lookup"><span data-stu-id="b1e06-143">Click Bind.</span></span>
25. <span data-ttu-id="b1e06-144">ในแผนภูมิ ขยาย 'การชำระเงิน= ธุรกรรม\เจ้าหนี้\ตัวแทน'</span><span class="sxs-lookup"><span data-stu-id="b1e06-144">In the tree, expand 'Payments= Transactions\Creditor\Agent'.</span></span>
26. <span data-ttu-id="b1e06-145">ในแผนภูมิ เลือก 'การชำระเงิน= ธุรกรรม\เจ้าหนี้\ตัวแทน\ชื่อ'</span><span class="sxs-lookup"><span data-stu-id="b1e06-145">In the tree, select 'Payments= Transactions\Creditor\Agent\Name'.</span></span>
27. <span data-ttu-id="b1e06-146">ในแผนภูมิ เลือก 'ธุรกรรม\บัญชีธนาคารของผู้จัดจำหน่ายในบริษัทธุรกรรม()\ชื่อ'</span><span class="sxs-lookup"><span data-stu-id="b1e06-146">In the tree, select 'Transactions\vendBankAccountInTransactionCompany()\Name'.</span></span>
28. <span data-ttu-id="b1e06-147">คลิก ผูก</span><span class="sxs-lookup"><span data-stu-id="b1e06-147">Click Bind.</span></span>
29. <span data-ttu-id="b1e06-148">ในแผนภูมิ เลือก 'การชำระเงิน= ธุรกรรม\เจ้าหนี้\ตัวแทน\หมายเลขการกำหนดเส้นทาง(หมายเลขการกำหนดเส้นทาง)'</span><span class="sxs-lookup"><span data-stu-id="b1e06-148">In the tree, select 'Payments= Transactions\Creditor\Agent\Routing number(RoutingNumber)'.</span></span>
30. <span data-ttu-id="b1e06-149">ในแผนภูมิ เลือก 'ธุรกรรม\บัญชีธนาคารของผู้จัดจำหน่ายในบริษัทธุรกรรม()\หมายเลขการกำหนดเส้นทาง(หมายเลขการลงทะเบียน)'</span><span class="sxs-lookup"><span data-stu-id="b1e06-149">In the tree, select 'Transactions\vendBankAccountInTransactionCompany()\Routing number(RegistrationNum)'.</span></span>
31. <span data-ttu-id="b1e06-150">คลิก ผูก</span><span class="sxs-lookup"><span data-stu-id="b1e06-150">Click Bind.</span></span>
32. <span data-ttu-id="b1e06-151">ในแผนภูมิ เลือก 'การชำระเงิน= ธุรกรรม\เจ้าหนี้\ตัวแทน\รหัส SWIFT(SWIFT)'</span><span class="sxs-lookup"><span data-stu-id="b1e06-151">In the tree, select 'Payments= Transactions\Creditor\Agent\SWIFT code(SWIFT)'.</span></span>
33. <span data-ttu-id="b1e06-152">ในแผนภูมิ เลือก 'ธุรกรรม\บัญชีธนาคารของผู้จัดจำหน่ายในบริษัทธุรกรรม()\รหัส SWIFT(SWIFTNo)'</span><span class="sxs-lookup"><span data-stu-id="b1e06-152">In the tree, select 'Transactions\vendBankAccountInTransactionCompany()\SWIFT code(SWIFTNo)'.</span></span>
34. <span data-ttu-id="b1e06-153">คลิก ผูก</span><span class="sxs-lookup"><span data-stu-id="b1e06-153">Click Bind.</span></span>
35. <span data-ttu-id="b1e06-154">ในแผนภูมิ เลือก 'การชำระเงิน= ธุรกรรม\เจ้าหนี้\ชื่อ'</span><span class="sxs-lookup"><span data-stu-id="b1e06-154">In the tree, select 'Payments= Transactions\Creditor\Name'.</span></span>
36. <span data-ttu-id="b1e06-155">ในแผนภูมิ ขยาย 'ธุรกรรม\findVendTable()'</span><span class="sxs-lookup"><span data-stu-id="b1e06-155">In the tree, expand 'Transactions\findVendTable()'.</span></span>
37. <span data-ttu-id="b1e06-156">ในแผนภูมิ เลือก 'Transactions\findVendTable()\name()'</span><span class="sxs-lookup"><span data-stu-id="b1e06-156">In the tree, select 'Transactions\findVendTable()\name()'.</span></span>
38. <span data-ttu-id="b1e06-157">คลิก ผูก</span><span class="sxs-lookup"><span data-stu-id="b1e06-157">Click Bind.</span></span>
39. <span data-ttu-id="b1e06-158">ในแผนภูมิ เลือก 'การชำระเงิน= ธุรกรรม\รหัสสกุลเงิน(สกุลเงิน)'</span><span class="sxs-lookup"><span data-stu-id="b1e06-158">In the tree, select 'Payments= Transactions\Currency code(Currency)'.</span></span>
40. <span data-ttu-id="b1e06-159">ในแผนภูมิ ขยาย 'ธุรกรรม\>ความสัมพันธ์'</span><span class="sxs-lookup"><span data-stu-id="b1e06-159">In the tree, expand 'Transactions\>Relations'.</span></span>
41. <span data-ttu-id="b1e06-160">ในแผนภูมิ ขยาย 'ธุรกรรม\>ความสัมพันธ์\ตารางสกุลเงิน(สกุลเงิน)'</span><span class="sxs-lookup"><span data-stu-id="b1e06-160">In the tree, expand 'Transactions\>Relations\Currency table(Currency)'.</span></span>
42. <span data-ttu-id="b1e06-161">ในแผนภูมิ เลือก 'ธุรกรรม\>ความสัมพันธ์\ตารางสกุลเงิน(สกุลเงิน)\รหัสสกุลเงิน(รหัสสกุลเงินISO)'</span><span class="sxs-lookup"><span data-stu-id="b1e06-161">In the tree, select 'Transactions\>Relations\Currency table(Currency)\Currency code(CurrencyCodeISO)'.</span></span>
43. <span data-ttu-id="b1e06-162">คลิก ผูก</span><span class="sxs-lookup"><span data-stu-id="b1e06-162">Click Bind.</span></span>
44. <span data-ttu-id="b1e06-163">ในแผนภูมิ ขยาย 'การชำระเงิน= ธุรกรรม\ลูกหนี้'</span><span class="sxs-lookup"><span data-stu-id="b1e06-163">In the tree, expand 'Payments= Transactions\Debtor'.</span></span>
45. <span data-ttu-id="b1e06-164">ในแผนภูมิ ขยาย 'การชำระเงิน= ธุรกรรม\ลูกหนี้\บัญชี'</span><span class="sxs-lookup"><span data-stu-id="b1e06-164">In the tree, expand 'Payments= Transactions\Debtor\Account'.</span></span>
46. <span data-ttu-id="b1e06-165">ในแผนภูมิ เลือก 'การชำระเงิน= ธุรกรรม\ลูกหนี้\บัญชี\รหัสสกุลเงิน(สกุลเงิน)'</span><span class="sxs-lookup"><span data-stu-id="b1e06-165">In the tree, select 'Payments= Transactions\Debtor\Account\Currency code(Currency)'.</span></span>
47. <span data-ttu-id="b1e06-166">ในแผนภูมิ เลือก 'บัญชีธนาคาร(บัญชีธนาคาร)'</span><span class="sxs-lookup"><span data-stu-id="b1e06-166">In the tree, select 'Bank Account(BankAccount)'.</span></span>
48. <span data-ttu-id="b1e06-167">ในแผนภูมิ ขยาย 'บัญชีธนาคาร(บัญชีธนาคาร)'</span><span class="sxs-lookup"><span data-stu-id="b1e06-167">In the tree, expand 'Bank Account(BankAccount)'.</span></span>
49. <span data-ttu-id="b1e06-168">ในแผนภูมิ เลือก 'บัญชีธนาคาร(บัญชีธนาคาร)\สกุลเงิน(รหัสสกุลเงิน)'</span><span class="sxs-lookup"><span data-stu-id="b1e06-168">In the tree, select 'Bank Account(BankAccount)\Currency(CurrencyCode)'.</span></span>
50. <span data-ttu-id="b1e06-169">คลิก ผูก</span><span class="sxs-lookup"><span data-stu-id="b1e06-169">Click Bind.</span></span>
51. <span data-ttu-id="b1e06-170">ในแผนภูมิ เลือก 'บัญชีธนาคาร(บัญชีธนาคาร)\IBAN'</span><span class="sxs-lookup"><span data-stu-id="b1e06-170">In the tree, select 'Bank Account(BankAccount)\IBAN'.</span></span>
52. <span data-ttu-id="b1e06-171">ในแผนภูมิ เลือก 'การชำระเงิน= ธุรกรรม\ลูกหนี้\บัญชี\รหัสIBAN(IBAN)'</span><span class="sxs-lookup"><span data-stu-id="b1e06-171">In the tree, select 'Payments= Transactions\Debtor\Account\IBAN code(IBAN)'.</span></span>
53. <span data-ttu-id="b1e06-172">คลิก ผูก</span><span class="sxs-lookup"><span data-stu-id="b1e06-172">Click Bind.</span></span>
54. <span data-ttu-id="b1e06-173">ในแผนภูมิ เลือก 'การชำระเงิน= ธุรกรรม\ลูกหนี้\บัญชี\หมายเลข'</span><span class="sxs-lookup"><span data-stu-id="b1e06-173">In the tree, select 'Payments= Transactions\Debtor\Account\Number'.</span></span>
55. <span data-ttu-id="b1e06-174">ในแผนภูมิ เลือก 'บัญชีธนาคาร(บัญชีธนาคาร)\หมายเลขบัญชีธนาคาร(AccountNum)'</span><span class="sxs-lookup"><span data-stu-id="b1e06-174">In the tree, select 'Bank Account(BankAccount)\Bank account number(AccountNum)'.</span></span>
56. <span data-ttu-id="b1e06-175">คลิก ผูก</span><span class="sxs-lookup"><span data-stu-id="b1e06-175">Click Bind.</span></span>
57. <span data-ttu-id="b1e06-176">ในแผนภูมิ ขยาย 'การชำระเงิน= ธุรกรรม\ลูกหนี้\ตัวแทน'</span><span class="sxs-lookup"><span data-stu-id="b1e06-176">In the tree, expand 'Payments= Transactions\Debtor\Agent'.</span></span>
58. <span data-ttu-id="b1e06-177">ในแผนภูมิ เลือก 'การชำระเงิน= ธุรกรรม\ลูกหนี้\ตัวแทน\ชื่อ'</span><span class="sxs-lookup"><span data-stu-id="b1e06-177">In the tree, select 'Payments= Transactions\Debtor\Agent\Name'.</span></span>
59. <span data-ttu-id="b1e06-178">ในแผนภูมิ เลือก 'บัญชีธนาคาร(บัญชีธนาคาร)\ชื่อ'</span><span class="sxs-lookup"><span data-stu-id="b1e06-178">In the tree, select 'Bank Account(BankAccount)\Name'.</span></span>
60. <span data-ttu-id="b1e06-179">คลิก ผูก</span><span class="sxs-lookup"><span data-stu-id="b1e06-179">Click Bind.</span></span>
61. <span data-ttu-id="b1e06-180">ในแผนภูมิ เลือก 'การชำระเงิน= ธุรกรรม\ลูกหนี้\ตัวแทน\หมายเลขการกำหนดเส้นทาง(หมายเลขการกำหนดเส้นทาง)'</span><span class="sxs-lookup"><span data-stu-id="b1e06-180">In the tree, select 'Payments= Transactions\Debtor\Agent\Routing number(RoutingNumber)'.</span></span>
62. <span data-ttu-id="b1e06-181">ในแผนภูมิ เลือก 'บัญชีธนาคาร(บัญชีธนาคาร)\หมายเลขการกำหนดเส้นทาง(หมายเลขการลงทะเบียน)'</span><span class="sxs-lookup"><span data-stu-id="b1e06-181">In the tree, select 'Bank Account(BankAccount)\Routing number(RegistrationNum)'.</span></span>
63. <span data-ttu-id="b1e06-182">คลิก ผูก</span><span class="sxs-lookup"><span data-stu-id="b1e06-182">Click Bind.</span></span>
64. <span data-ttu-id="b1e06-183">ในแผนภูมิ เลือก 'การชำระเงิน= ธุรกรรม\ลูกหนี้\ตัวแทน\รหัส SWIFT(SWIFT)'</span><span class="sxs-lookup"><span data-stu-id="b1e06-183">In the tree, select 'Payments= Transactions\Debtor\Agent\SWIFT code(SWIFT)'.</span></span>
65. <span data-ttu-id="b1e06-184">ในแผนภูมิ เลือก 'บัญชีธนาคาร(บัญชีธนาคาร)\รหัส SWIFT(SWIFTNo)'</span><span class="sxs-lookup"><span data-stu-id="b1e06-184">In the tree, select 'Bank Account(BankAccount)\SWIFT code(SWIFTNo)'.</span></span>
66. <span data-ttu-id="b1e06-185">คลิก ผูก</span><span class="sxs-lookup"><span data-stu-id="b1e06-185">Click Bind.</span></span>
67. <span data-ttu-id="b1e06-186">ในแผนภูมิ เลือก 'การชำระเงิน= ธุรกรรม\ลูกหนี้\ชื่อ'</span><span class="sxs-lookup"><span data-stu-id="b1e06-186">In the tree, select 'Payments= Transactions\Debtor\Name'.</span></span>
68. <span data-ttu-id="b1e06-187">ในแผนภูมิ เลือก 'ข้อมูลบริษัท(บริษัท)'</span><span class="sxs-lookup"><span data-stu-id="b1e06-187">In the tree, select 'Company information(Company)'.</span></span>
69. <span data-ttu-id="b1e06-188">ในแผนภูมิ ขยาย 'ข้อมูลบริษัท(บริษัท)'</span><span class="sxs-lookup"><span data-stu-id="b1e06-188">In the tree, expand 'Company information(Company)'.</span></span>
70. <span data-ttu-id="b1e06-189">ในแผนภูมิ เลือก 'ข้อมูลบริษัท(บริษัท)\ชื่อ'</span><span class="sxs-lookup"><span data-stu-id="b1e06-189">In the tree, select 'Company information(Company)\Name'.</span></span>
71. <span data-ttu-id="b1e06-190">คลิก ผูก</span><span class="sxs-lookup"><span data-stu-id="b1e06-190">Click Bind.</span></span>
72. <span data-ttu-id="b1e06-191">ในแผนภูมิ เลือก 'การชำระเงิน= ธุรกรรม\คำอธิบาย'</span><span class="sxs-lookup"><span data-stu-id="b1e06-191">In the tree, select 'Payments= Transactions\Description'.</span></span>
73. <span data-ttu-id="b1e06-192">ในแผนภูมิ เลือก 'การชำระเงิน= ธุรกรรม\คำอธิบาย(Txt)'</span><span class="sxs-lookup"><span data-stu-id="b1e06-192">In the tree, select 'Transactions\Description(Txt)'.</span></span>
74. <span data-ttu-id="b1e06-193">คลิก ผูก</span><span class="sxs-lookup"><span data-stu-id="b1e06-193">Click Bind.</span></span>
75. <span data-ttu-id="b1e06-194">ในแผนภูมิ เลือก 'การชำระเงิน= ธุรกรรม\การระบุรหัสแบบครอบคลุม(End2EndID)'</span><span class="sxs-lookup"><span data-stu-id="b1e06-194">In the tree, select 'Payments= Transactions\End to end identification code(End2EndID)'.</span></span>
76. <span data-ttu-id="b1e06-195">ในแผนภูมิ เลือก 'ธุรกรรม\$EndToEndID'</span><span class="sxs-lookup"><span data-stu-id="b1e06-195">In the tree, select 'Transactions\$EndToEndID'.</span></span>
77. <span data-ttu-id="b1e06-196">คลิก ผูก</span><span class="sxs-lookup"><span data-stu-id="b1e06-196">Click Bind.</span></span>
78. <span data-ttu-id="b1e06-197">ในแผนภูมิ เลือก 'การชำระเงิน= ธุรกรรม\ยอดเงินที่แนะนำ(ยอดเงินที่แนะนำ)'</span><span class="sxs-lookup"><span data-stu-id="b1e06-197">In the tree, select 'Payments= Transactions\Instructed amount(InstructedAmount)'.</span></span>
79. <span data-ttu-id="b1e06-198">ในแผนภูมิ เลือก 'Transactions\$Amount'</span><span class="sxs-lookup"><span data-stu-id="b1e06-198">In the tree, select 'Transactions\$Amount'.</span></span>
80. <span data-ttu-id="b1e06-199">คลิก ผูก</span><span class="sxs-lookup"><span data-stu-id="b1e06-199">Click Bind.</span></span>
81. <span data-ttu-id="b1e06-200">ในแผนภูมิ เลือก 'การชำระเงิน= ธุรกรรม\วันที่ทำธุรกรรม(วันที่ทำธุรกรรม)'</span><span class="sxs-lookup"><span data-stu-id="b1e06-200">In the tree, select 'Payments= Transactions\Transaction date(TransactionDate)'.</span></span>
82. <span data-ttu-id="b1e06-201">ในแผนภูมิ เลือก 'ธุรกรรม\วันที่(วันที่ธุรกรรม)'</span><span class="sxs-lookup"><span data-stu-id="b1e06-201">In the tree, select 'Transactions\Date(TransDate)'.</span></span>
83. <span data-ttu-id="b1e06-202">คลิก ผูก</span><span class="sxs-lookup"><span data-stu-id="b1e06-202">Click Bind.</span></span>

## <a name="validate-created-mapping"></a><span data-ttu-id="b1e06-203">การตรวจสอบความถูกต้องการแม็ปที่สร้างขึ้น</span><span class="sxs-lookup"><span data-stu-id="b1e06-203">Validate created mapping</span></span>
1. <span data-ttu-id="b1e06-204">คลิก ตรวจสอบความถูกต้อง</span><span class="sxs-lookup"><span data-stu-id="b1e06-204">Click Validate.</span></span>
    * <span data-ttu-id="b1e06-205">ตรวจสอบการแม็ปใหม่เพื่อให้แน่ใจว่าการเชื่อมโยงข้อมูลทั้งหมดถูกต้อง</span><span class="sxs-lookup"><span data-stu-id="b1e06-205">Validate the new mapping to ensure that all bindings are okay.</span></span>  
2. <span data-ttu-id="b1e06-206">คลิกลูกศรเพื่อขยายหรือยุบส่วนรายการข้อผิดพลาด</span><span class="sxs-lookup"><span data-stu-id="b1e06-206">Click the arrow to expand or collapse the Error List section.</span></span>
3. <span data-ttu-id="b1e06-207">คลิก บันทึก</span><span class="sxs-lookup"><span data-stu-id="b1e06-207">Click Save.</span></span>
4. <span data-ttu-id="b1e06-208">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="b1e06-208">Close the page.</span></span>
5. <span data-ttu-id="b1e06-209">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="b1e06-209">Close the page.</span></span>
6. <span data-ttu-id="b1e06-210">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="b1e06-210">Close the page.</span></span>

## <a name="change-the-status-of-the-current-version-of-model-configuration"></a><span data-ttu-id="b1e06-211">เปลี่ยนสถานะของรุ่นปัจจุบันของการตั้งค่าคอนฟิกแบบจำลอง</span><span class="sxs-lookup"><span data-stu-id="b1e06-211">Change the status of the current version of model configuration</span></span>
1. <span data-ttu-id="b1e06-212">คลิก เปลี่ยนแปลงสถานะ</span><span class="sxs-lookup"><span data-stu-id="b1e06-212">Click Change status.</span></span>
    * <span data-ttu-id="b1e06-213">เปลี่ยนสถานะของการตั้งค่าคอนฟิกแบบจำลองที่ออกแบบแล้ว – จากแบบร่างเป็นแบบที่เสร็จสมบูรณ์ เพื่อทำให้พร้อมใช้งานสำหรับการออกแบบรูปแบบการชำระเงิน</span><span class="sxs-lookup"><span data-stu-id="b1e06-213">Change the status of designed model configuration – from Draft to Completed to make it available for payment format design.</span></span>  
2. <span data-ttu-id="b1e06-214">คลิกเสร็จสมบูรณ์</span><span class="sxs-lookup"><span data-stu-id="b1e06-214">Click Complete.</span></span>
    * <span data-ttu-id="b1e06-215">เลือกเสร็จสมบูรณ์</span><span class="sxs-lookup"><span data-stu-id="b1e06-215">Select Complete.</span></span>  
3. <span data-ttu-id="b1e06-216">ในฟิลด์ คำอธิบาย ให้พิมพ์ค่า</span><span class="sxs-lookup"><span data-stu-id="b1e06-216">In the Description field, type a value.</span></span>
    * <span data-ttu-id="b1e06-217">ตัวอย่างเช่น 'version 1'</span><span class="sxs-lookup"><span data-stu-id="b1e06-217">For example, 'version 1'.</span></span>  
4. <span data-ttu-id="b1e06-218">คลิก ตกลง</span><span class="sxs-lookup"><span data-stu-id="b1e06-218">Click OK.</span></span>
5. <span data-ttu-id="b1e06-219">เลือกเวอร์ชันที่สมบูรณ์ของการตั้งค่าคอนฟิกปัจจุบัน</span><span class="sxs-lookup"><span data-stu-id="b1e06-219">Select the completed version of the current configuration.</span></span>
    * <span data-ttu-id="b1e06-220">หมายเหตุว่า โครงแบบที่สร้างขึ้นถูกบันทึกเป็นเวอร์ชัน 1เสร็จสมบูรณ์</span><span class="sxs-lookup"><span data-stu-id="b1e06-220">Note that the created configuration is saved as completed version 1.</span></span>  

