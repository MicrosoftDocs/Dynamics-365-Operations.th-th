---
title: ภาพรวมการอัพเกรดของสมุดบัญชีค่าเสื่อมราคา
description: ในรุ่นก่อนหน้า มีแนวคิดการคิดมูลค่าสองรายการสำหรับสินทรัพย์ถาวร - รูปแบบมูลค่าและสมุดบัญชีค่าเสื่อมราคา ใน Microsoft Dynamics 365 for Operations (1611) ฟังก์ชันแบบจำลองค่าและฟังก์ชันหนังสือการคิดค่าเสื่อมราคาได้ถูกผสานเป็นแนวคิดเดียวซึ่งรู้จักกันว่าเป็นหนังสือ หัวข้อนี้อธิบายสิ่งที่ควรพิจารณาสำหรับการอัพเกรด
author: ShylaThompson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User, Developer
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 221624
ms.assetid: cf434099-36f9-4b0f-a7c8-bed091e34f39
ms.search.region: global
ms.author: saraschi
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: ef906393ef07661ecd3ceefdbe62310de5ceff21
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 08/01/2019
ms.locfileid: "1840660"
---
# <a name="depreciation-book-upgrade-overview"></a><span data-ttu-id="03b52-105">ภาพรวมการอัพเกรดของสมุดบัญชีค่าเสื่อมราคา</span><span class="sxs-lookup"><span data-stu-id="03b52-105">Depreciation book upgrade overview</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="03b52-106">ในรุ่นก่อนหน้า มีแนวคิดการคิดมูลค่าสองรายการสำหรับสินทรัพย์ถาวร - รูปแบบมูลค่าและสมุดบัญชีค่าเสื่อมราคา</span><span class="sxs-lookup"><span data-stu-id="03b52-106">In previous releases, there were two valuation concepts for fixed assets -  value models and depreciation books.</span></span> <span data-ttu-id="03b52-107">ใน Microsoft Dynamics 365 for Operations (1611) ฟังก์ชันแบบจำลองค่าและฟังก์ชันหนังสือการคิดค่าเสื่อมราคาได้ถูกผสานเป็นแนวคิดเดียวซึ่งรู้จักกันว่าเป็นหนังสือ</span><span class="sxs-lookup"><span data-stu-id="03b52-107">In Microsoft Dynamics 365 for Operations (1611), the value model functionality and depreciation book functionality have been merged into a single concept that is known as a book.</span></span> <span data-ttu-id="03b52-108">หัวข้อนี้อธิบายสิ่งที่ควรพิจารณาสำหรับการอัพเกรด</span><span class="sxs-lookup"><span data-stu-id="03b52-108">This topic provides some things to consider for the upgrade.</span></span> 

<span data-ttu-id="03b52-109">กระบวนการอัพเกรดจะเปลี่ยนการตั้งค่าที่มีอยู่และธุรกรรมที่มีอยู่ทั้งหมดไปยังโครงสร้างสมุดบัญชีใหม่</span><span class="sxs-lookup"><span data-stu-id="03b52-109">The upgrade process will move your existing setup and all existing transactions to the new book structure.</span></span> <span data-ttu-id="03b52-110">รูปแบบมูลค่าจะยังคงเป็นเช่นปัจจุบัน โดยเป็นสมุดบัญชีที่ลงรายการบัญชีในบัญชีแยกประเภททั่วไป</span><span class="sxs-lookup"><span data-stu-id="03b52-110">Value models will remain as they currently are, as a book that posts to the general ledger.</span></span> <span data-ttu-id="03b52-111">สมุดบัญชีค่าเสื่อมราคาจะถูกย้ายไปยังสมุดบัญชีที่มีตัวเลือก **การลงรายการบัญชีในบัญชีแยกประเภททั่วไป** ที่ตั้งค่าเป็น **ไม่ใช่**</span><span class="sxs-lookup"><span data-stu-id="03b52-111">Depreciation books will be moved to a book that has the **Post to general ledger** option set to **No**.</span></span> <span data-ttu-id="03b52-112">ชื่อสมุดรายวันสมุดบัญชีค่าเสื่อมราคาจะถูกเปลี่ยนชื่อสมุดรายวันบัญชีแยกประเภททั่วไปที่มีชั้นของการลงรายการบัญชีที่ตั้งค่าเป็น **ไม่มี**</span><span class="sxs-lookup"><span data-stu-id="03b52-112">Depreciation book journal names will be moved to a general ledger journal name with the posting layer set to **None**.</span></span> <span data-ttu-id="03b52-113">ธุรกรรมสมุดบัญชีค่าเสื่อมราคาจะถูกย้ายไปยังธุรกรรมสินทรัพย์ถาวร</span><span class="sxs-lookup"><span data-stu-id="03b52-113">Depreciation book transactions will be moved to Fixed asset transactions.</span></span> 

<span data-ttu-id="03b52-114">ก่อนที่จะรันการอัพเกรดข้อมูล คุณควรทำความเข้าใจตัวเลือกสองรายการที่พร้อมใช้งานสำหรับการอัพเกรดรายการสมุดรายวันบัญชีค่าเสื่อมราคาเป็นใบสำคัญธุรกรรม และลำดับหมายเลขที่จะใช้สำหรับชุดใบสำคัญ</span><span class="sxs-lookup"><span data-stu-id="03b52-114">Before running the data upgrade, you should understand the two options available for upgrading depreciation book journal lines to transaction vouchers, and the number sequence that will be used for the voucher series.</span></span> 

<span data-ttu-id="03b52-115">ตัวเลือกที่ 1: **ลำดับหมายเลขที่กำหนดโดยระบบ** - นี่คือตัวเลือกเริ่มต้นเพื่อปรับปรุงประสิทธิภาพของการอัพเกรด</span><span class="sxs-lookup"><span data-stu-id="03b52-115">Option 1:  **System-defined number sequence** - This is the default option to optimize upgrade performance.</span></span> <span data-ttu-id="03b52-116">การอัพเกรดจะไม่ใช้กรอบงานลำดับหมายเลข แต่จะปันส่วนใบสำคัญที่มีวิธีการตามการตั้งค่าแทน</span><span class="sxs-lookup"><span data-stu-id="03b52-116">The upgrade will not use the number sequences framework, but instead will allocate vouchers with a set-based approach.</span></span> <span data-ttu-id="03b52-117">หลังจากการอัพเกรด ลำดับหมายเลขใหม่จะถูกสร้างขึ้นโดยมี **การตั้งค่าหมายเลขถัดไป** อย่างเหมาะสมตามธุรกรรมที่อัพเกรด</span><span class="sxs-lookup"><span data-stu-id="03b52-117">After the upgrade, the new number sequence will be created with the **Next number set** appropriately based on the upgraded transactions.</span></span> <span data-ttu-id="03b52-118">โดยค่าเริ่มต้น ลำดับหมายเลขที่ใช้จะอยู่ในรูปแบบ FADBUpgr\#\#\#\#\#\#\#\#\#</span><span class="sxs-lookup"><span data-stu-id="03b52-118">By default, the number sequence used will be in the FADBUpgr\#\#\#\#\#\#\#\#\# format.</span></span> <span data-ttu-id="03b52-119">มีพารามิเตอร์ไม่กี่รายการที่คุณสามารถใช้ได้ในการปรับปรุงรูปแบบเมื่อใช้วิธีการนี้:</span><span class="sxs-lookup"><span data-stu-id="03b52-119">There are a few parameters available to you to adjust the format when using this approach:</span></span>

-   <span data-ttu-id="03b52-120">**รหัสลำดับหมายเลข** – รหัสเพื่อระบุลำดับหมายเลข</span><span class="sxs-lookup"><span data-stu-id="03b52-120">**Number sequence code** – The code to identify the number sequence.</span></span> <span data-ttu-id="03b52-121">ไม่สามารถมีรหัสลำดับหมายเลขนี้อยู่ได้เนื่องจากจะถูกสร้างขึ้นโดยการอัพเกรด</span><span class="sxs-lookup"><span data-stu-id="03b52-121">This number sequence code cannot exist since it will be created by the upgrade.</span></span>
    -   <span data-ttu-id="03b52-122">ชื่อค่าคงที่: **NumberSequenceDefaultCode**</span><span class="sxs-lookup"><span data-stu-id="03b52-122">Constant name: **NumberSequenceDefaultCode**</span></span>
    -   <span data-ttu-id="03b52-123">ค่าเริ่มต้น: "FADBUpgr"</span><span class="sxs-lookup"><span data-stu-id="03b52-123">Default value: "FADBUpgr"</span></span>
-   <span data-ttu-id="03b52-124">**คำนำหน้า** – ค่าสตริงที่คงที่จะถูกใช้เป็นคำนำหน้าสำหรับหมายเลขใบสำคัญ</span><span class="sxs-lookup"><span data-stu-id="03b52-124">**Prefix** – The constant string value that will be used as a prefix for the voucher numbers.</span></span>
    -   <span data-ttu-id="03b52-125">ชื่อค่าคงที่: **NumberSequenceDefaultParameterPrefix**</span><span class="sxs-lookup"><span data-stu-id="03b52-125">Constant name: **NumberSequenceDefaultParameterPrefix**</span></span>
    -   <span data-ttu-id="03b52-126">ค่าเริ่มต้น: "FADBUpgr"</span><span class="sxs-lookup"><span data-stu-id="03b52-126">Default value: "FADBUpgr"</span></span>
-   <span data-ttu-id="03b52-127">**ความยาวของตัวอักษรและตัวเลข** – ความยาวของเซ็กเมนต์ตัวอักษรและตัวเลขของลำดับหมายเลข</span><span class="sxs-lookup"><span data-stu-id="03b52-127">**Alphanumeric length** – The length of the alphanumeric segment of the number sequence.</span></span>
    -   <span data-ttu-id="03b52-128">ชื่อค่าคงที่: \*\*NumberSequenceDefaultParameterAlpanumericLength \*\*</span><span class="sxs-lookup"><span data-stu-id="03b52-128">Constant name: \*\*NumberSequenceDefaultParameterAlpanumericLength \*\*</span></span>
    -   <span data-ttu-id="03b52-129">ค่าเริ่มต้น: 9</span><span class="sxs-lookup"><span data-stu-id="03b52-129">Default value: 9</span></span>
-   <span data-ttu-id="03b52-130">**หมายเลขเริ่มต้น** - หมายเลขเริ่มต้นที่จะใช้ในลำดับหมายเลข</span><span class="sxs-lookup"><span data-stu-id="03b52-130">**Start number** - The first number to be used in the number sequence.</span></span>
    -   <span data-ttu-id="03b52-131">ชื่อค่าคงที่: **NumberSequenceDefaultParameterStartNumber**</span><span class="sxs-lookup"><span data-stu-id="03b52-131">Constant name: \*\*NumberSequenceDefaultParameterStartNumber  \*\*</span></span>
    -   <span data-ttu-id="03b52-132">ค่าเริ่มต้น: 1</span><span class="sxs-lookup"><span data-stu-id="03b52-132">Default value: 1</span></span>

<span data-ttu-id="03b52-133">ตัวเลือกที่ 2: **ลำดับหมายเลขที่ผู้ใช้กำหนดที่มีอยู่** -ตัวเลือกนี้จะช่วยให้คุณสามารถกำหนดลำดับหมายเลขที่จะใช้สำหรับการอัพเกรด</span><span class="sxs-lookup"><span data-stu-id="03b52-133">Option 2: **Existing user-defined number sequence** - This option will allow you to define the number sequence to be used for the upgrade.</span></span> <span data-ttu-id="03b52-134">พิจารณาการใช้ตัวเลือกนี้ถ้าคุณต้องการการตั้งค่าคอนฟิกลำดับหมายเลขขั้นสูง</span><span class="sxs-lookup"><span data-stu-id="03b52-134">Consider using this option if you need advanced number sequence configuration.</span></span> <span data-ttu-id="03b52-135">เมื่อต้องการใช้ลำดับหมายเลข คุณต้องแก้ไขคลาสการอัพเกรด ReleaseUpdateDB70\_FixedAssetJournalDepBookRemovalDepBookJournalTrans กับข้อมูลต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="03b52-135">To use a number sequence, you must modify the upgrade class ReleaseUpdateDB70\_FixedAssetJournalDepBookRemovalDepBookJournalTrans with the following information:</span></span>

-   <span data-ttu-id="03b52-136">**รหัสลำดับหมายเลข** – รหัสของลำดับหมายเลข</span><span class="sxs-lookup"><span data-stu-id="03b52-136">**Number sequence code** – The code of the number sequence.</span></span>
    -   <span data-ttu-id="03b52-137">ชื่อค่าคงที่: \*\*NumberSequenceExistingCode \*\*</span><span class="sxs-lookup"><span data-stu-id="03b52-137">Constant name: \*\*NumberSequenceExistingCode \*\*</span></span>
    -   <span data-ttu-id="03b52-138">ค่าเริ่มต้น: ไม่มีค่าเริ่มต้น ต้จะต้องอัพเดตเป็นรหัสลำดับหมายเลข</span><span class="sxs-lookup"><span data-stu-id="03b52-138">Default value: No default, this must be updated to the number sequence code.</span></span>
-   <span data-ttu-id="03b52-139">**ลำดับหมายเลขที่ใช้ร่วมกัน** – ค่าบูลีนเพื่อระบุขอบเขตของลำดับหมายเลข</span><span class="sxs-lookup"><span data-stu-id="03b52-139">**Shared number sequence** – A boolean value to identify the scope of the number sequence.</span></span> <span data-ttu-id="03b52-140">ใช้ "จริง" สำหรับลำดับหมายเลขที่ใช้ร่วมกันทั่วทั้งบริษัท และ "เท็จ" สำหรับขอบเขตเฉพาะบริษัท</span><span class="sxs-lookup"><span data-stu-id="03b52-140">Use "true" for shared number sequences across all companies, and "false" for a company-specific scope.</span></span> <span data-ttu-id="03b52-141">เมื่อใช้ "เท็จ" ลำดับหมายเลขที่มีชื่อที่ระบุจะต้องมีอยู่ในบริษัททั้งหมดที่มีธุรกรรมสมุดบัญชีค่าเสื่อมราคา</span><span class="sxs-lookup"><span data-stu-id="03b52-141">When using "false", the number sequence with the specified name must exist in every company that contains depreciation book transactions.</span></span> <span data-ttu-id="03b52-142">ลำดับหมายเลขที่ใช้ร่วมกันจะอยู่ในทุกพาร์ติชันที่มีธุรกรรมสมุดบัญชีค่าเสื่อมราคา</span><span class="sxs-lookup"><span data-stu-id="03b52-142">Shared number sequences exist in every partition that contains depreciation book transactions.</span></span>
    -   <span data-ttu-id="03b52-143">ชื่อค่าคงที่: \*\*NumberSequenceExistingIsShared \*\*</span><span class="sxs-lookup"><span data-stu-id="03b52-143">Constant name: \*\*NumberSequenceExistingIsShared \*\*</span></span>
    -   <span data-ttu-id="03b52-144">ค่าเริ่มต้น: จริง</span><span class="sxs-lookup"><span data-stu-id="03b52-144">Default value: true</span></span>

<span data-ttu-id="03b52-145">พารามิเตอร์อยู่ที่จุดเริ่มต้นของคลาส ReleaseUpdateDB70\_FixedAssetJournalDepBookRemovalDepBookJournalTrans</span><span class="sxs-lookup"><span data-stu-id="03b52-145">The parameters are located at the beginning of the ReleaseUpdateDB70\_FixedAssetJournalDepBookRemovalDepBookJournalTrans class.</span></span> 

<span data-ttu-id="03b52-146">*// ระบุวิธีการที่ต้องการสำหรับการปันส่วนใบสำคัญ* 
 *// จริง ถ้าคุณต้องการใช้รหัสลำดับหมายเลขที่มีอยู่* 
 *// เท็จ ถ้าคุณต้องการใช้ลำดับหมายเลขที่ระบบกำหนด (ค่าเริ่มต้น)* const boolean NumberSequenceUseExistingCode = false;</span><span class="sxs-lookup"><span data-stu-id="03b52-146">*// Specify a preferable approach of vouchers allocation* 
 *// true, if you want to use an existing number sequence code* 
 *// false, if you intend to use the system-defined number sequence (default)* const boolean NumberSequenceUseExistingCode = false;</span></span>  

<span data-ttu-id="03b52-147">*// ถ้าใช้วิธีการของลำดับหมายเลขที่ระบบกำหนด ให้ระบุพารามิเตอร์สำหรับลำดับหมายเลข*
 *// จะมีการสร้างลำดับหมายเลขใหม่โดยใช้พารามิเตอร์เหล่านี้*</span><span class="sxs-lookup"><span data-stu-id="03b52-147">*// If using the system-defined number sequence approach, specify the parameters for the number sequence.*
 *// A new number sequence will be created with these parameters.*</span></span> <span data-ttu-id="03b52-148">const str NumberSequenceDefaultCode = 'FADBUpgr'; const str NumberSequenceDefaultParameterPrefix = 'FADBUpgr'; const int NumberSequenceDefaultParameterAlpanumericLength = 9; const int NumberSequenceDefaultParameterStartNumber = 1;</span><span class="sxs-lookup"><span data-stu-id="03b52-148">const str NumberSequenceDefaultCode = 'FADBUpgr'; const str NumberSequenceDefaultParameterPrefix = 'FADBUpgr'; const int NumberSequenceDefaultParameterAlpanumericLength = 9; const int NumberSequenceDefaultParameterStartNumber = 1;</span></span>   

<span data-ttu-id="03b52-149">*// ถ้าใช้วิธีการของลำดับหมายเลขที่มีอยู่ ให้ระบุรหัสลำดับหมายเลขที่มีอยู่* 
 *// การปันส่วนใบสำคัญจะดำเนินการทีละแถวสำหรับลำดับหมายเลขที่มีอยู่*</span><span class="sxs-lookup"><span data-stu-id="03b52-149">*// If using the existing number sequence approach, specify the existing number sequence code.* 
 *// Voucher allocation will go row-by-row for existing number sequences.*</span></span> <span data-ttu-id="03b52-150">const str NumberSequenceExistingCode = ''; *// ระบุขอบเขตของรหัสลำดับหมายเลขที่มีอยู่* 
 *// จริง ถ้ามีการใช้ลำดับหมายเลขที่ระบุร่วมกัน* 
 *// เท็จ ถ้าลำดับหมายเลขที่ระบุสำหรับแต่ละบริษัท* 
 *// ลำดับหมายเลขที่ระบบกำหนดเริ่มต้นจะถูกใช้ถ้าไม่พบรหัสลำดับหมายเลขที่มีขอบเขตที่ระบุ*</span><span class="sxs-lookup"><span data-stu-id="03b52-150">const str NumberSequenceExistingCode = ''; *// Specify the scope of the existing number sequence code* 
 *// true, if the specified number sequence is shared* 
 *// false, if the specified number sequence is per-company* 
 *// The default system-defined number sequence will be used if a number sequence code with the specified scope is not found.*</span></span> <span data-ttu-id="03b52-151">const boolean NumberSequenceExistingIsShared = true;</span><span class="sxs-lookup"><span data-stu-id="03b52-151">const boolean NumberSequenceExistingIsShared = true;</span></span> 

<span data-ttu-id="03b52-152">สร้างโครงการที่มีคลาสใหม่หลังจากที่มีการแก้ไขค่าคงที่</span><span class="sxs-lookup"><span data-stu-id="03b52-152">Rebuild the project that contains the class after the constants have been modified.</span></span> 

<span data-ttu-id="03b52-153">เมื่อใช้วิธีการของลำดับหมายเลขที่ระบบสร้าง (ตัวเลือกที่ 1) การอัพเกรดจะใช้การประมวลผลตามการตั้งค่าในการปันส่วนหมายเลขใบสำคัญตามที่ระบุในพารามิเตอร์สคริปต์การอัพเกรด</span><span class="sxs-lookup"><span data-stu-id="03b52-153">When using the system-generated number sequence approach (option 1), the upgrade will use set-based processing to allocate the voucher numbers as specified in the upgrade script parameters.</span></span> <span data-ttu-id="03b52-154">ซึ่งจะสร้างลำดับหมายเลขใหม่ที่มีพารามิเตอร์ที่ระบุหลังจากการปันส่วน</span><span class="sxs-lookup"><span data-stu-id="03b52-154">It will also create a new number sequence with specified parameters after the allocation.</span></span> 

<span data-ttu-id="03b52-155">เมื่อใช้วิธีการของลำดับหมายเลขที่มีอยู่ที่ผู้ใช้กำหนด (ตัวเลือกที่ 2) การอัพเกรดข้อมูลจะตรวจสอบว่าลำดับหมายเลขที่มีขอบเขตที่ระบุอยู่ในฐานข้อมูลสำหรับแต่ละพาร์ติชันและบริษัทที่มีธุรกรรมสมุดบัญชีค่าเสื่อมราคาหรือไม่</span><span class="sxs-lookup"><span data-stu-id="03b52-155">When using the user-defined existing number sequence approach (option 2), the data upgrade checks whether the number sequence with the specified scope exists in the database for each partition and company with depreciation book transactions.</span></span> <span data-ttu-id="03b52-156">ถ้าไม่มี การอัพเกรดจะใช้การประมวลผลทีละแถวในการปันส่วนหมายเลขใบสำคัญที่ระบุไว้ตามลำดับหมายเลขโดยใช้กรอบงานลำดับหมายเลข</span><span class="sxs-lookup"><span data-stu-id="03b52-156">If it does exist, the upgrade will use row-by-row processing to allocate the voucher numbers as specified by the number sequence using the number sequence framework.</span></span> <span data-ttu-id="03b52-157">ถ้าไม่มีลำดับหมายเลขที่มีขอบเขตที่ระบุ การอัพเกรดจะใช้วิธีการของลำดับหมายเลขที่ระบบกำหนดเริ่มต้นในการปันส่วนหมายเลขใบสำคัญ และจะสร้างลำดับหมายเลขใหม่ที่มีพารามิเตอร์เริ่มต้นที่ระบุหลังจากการปันส่วน</span><span class="sxs-lookup"><span data-stu-id="03b52-157">If the number sequence does not exist with the specified scope, the upgrade will use the default system-defined number sequence approach to allocate the voucher numbers, and will create a new number sequence with specified default parameters after the allocation.</span></span>

<span data-ttu-id="03b52-158">ไม่ว่าจะด้วยวิธีการใด สคริปต์การอัพเกรดข้อมูลจะใช้ลำดับหมายเลขสำหรับฟิลด์ **ชุดใบสำคัญ** ในชื่อใหม่ของสมุดรายวันบัญชีแยกประเภททั่วไปซึ่งสร้างขึ้นสำหรับชื่อสมุดรายวันสมุดบัญชีค่าเสื่อมราคาก่อนหน้านี้</span><span class="sxs-lookup"><span data-stu-id="03b52-158">With either approach, the data upgrade script will also use the number sequence for the **Voucher series** field on the new general ledger journal names created for the former depreciation book journal names.</span></span>



