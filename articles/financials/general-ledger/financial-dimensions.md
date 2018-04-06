---
title: "มิติทางการเงิน"
description: "หัวข้อนี้อธิบายมิติทางการเงินชนิดต่างๆ และวิธีการตั้งค่า"
author: aprilolson
manager: AnnBe
ms.date: 08/01/2017
ms.topic: article
ems.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: DimensionDetails, DimensionValueDetails, SysTranslationDetail
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 25871
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a0739304723d19b910388893d08e8c36a1f49d13
ms.openlocfilehash: 3e9f00fdc32feda0a62f71a92e503a677dce35cc
ms.contentlocale: th-th
ms.lasthandoff: 03/26/2018

---

# <a name="financial-dimensions"></a><span data-ttu-id="8f25c-103">มิติทางการเงิน</span><span class="sxs-lookup"><span data-stu-id="8f25c-103">Financial dimensions</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="8f25c-104">หัวข้อนี้อธิบายมิติทางการเงินชนิดต่างๆ และวิธีการตั้งค่า</span><span class="sxs-lookup"><span data-stu-id="8f25c-104">This topic explains the various types of financial dimensions and how they are set up.</span></span>

<span data-ttu-id="8f25c-105">ใช้หน้า **มิติทางการเงิน** เพื่อสร้างมิติทางการเงินที่คุณสามารถใช้เป็นเซ็กเมนต์บัญชีสำหรับผังของบัญชี</span><span class="sxs-lookup"><span data-stu-id="8f25c-105">Use the **Financial dimensions** page to create financial dimensions that you can use as account segments for charts of accounts.</span></span> <span data-ttu-id="8f25c-106">มิติทางการเงินมีสองชนิดได้แก่: มิติที่กำหนดเอง และมิติที่สำรองไว้ในเอนทิตี้</span><span class="sxs-lookup"><span data-stu-id="8f25c-106">There are two types of financial dimensions: custom dimensions and entity-backed dimensions.</span></span> <span data-ttu-id="8f25c-107">มิติที่กำหนดเองถูกใช้ร่วมกับนิติบุคคลและค่าจะถูกป้อนไว้และรักษาไว้โดยผู้ใช้</span><span class="sxs-lookup"><span data-stu-id="8f25c-107">Custom dimensions are shared across legal entities, and the values are entered and maintained by users.</span></span> <span data-ttu-id="8f25c-108">สำหรับมิติที่สำรองไว้ในเอนทิตี้ จะถูกกำหนดค่าไว้ที่ใดที่หนึ่งในระบบ เช่น ลูกค้าหรือเอนทิตี้ของร้านค้า</span><span class="sxs-lookup"><span data-stu-id="8f25c-108">For entity-backed dimensions, the values are defined somewhere else in the system, such as Customers or Stores entities.</span></span> <span data-ttu-id="8f25c-109">บางมิติที่สำรองไว้ในเอนทิตี้ถูกใช้ร่วมกับนิติบุคคล ในขณะที่มิติที่สำรองไว้ในเอนทิตี้อื่นเป็นเฉพาะบริษัท</span><span class="sxs-lookup"><span data-stu-id="8f25c-109">Some entity-backed dimensions are shared across legal entities, whereas other entity-backed dimensions are company-specific.</span></span> 

<span data-ttu-id="8f25c-110">หลังจากที่คุณได้สร้างมิติทางการเงินแล้ว ใช้หน้า **ค่ามิติทางการเงิน** เพื่อกำหนดคุณสมบัติเพิ่มเติมให้กับแต่ละมิติทางการเงิน</span><span class="sxs-lookup"><span data-stu-id="8f25c-110">After you've created the financial dimensions, use the **Financial dimension values** page to assign additional properties to each financial dimension.</span></span> 

<span data-ttu-id="8f25c-111">คุณสามารถใช้มิติทางการเงินเพื่อที่จะแสดงถึงนิติบุคคล</span><span class="sxs-lookup"><span data-stu-id="8f25c-111">You can use financial dimensions to represent legal entities.</span></span> <span data-ttu-id="8f25c-112">คุณไม่จำเป็นต้องสร้างนิติบุคคลใน Microsoft Dynamics 365 for Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="8f25c-112">You don't have to create the legal entities in Microsoft Dynamics 365 for Finance and Operations.</span></span> <span data-ttu-id="8f25c-113">อย่างไรก็ตาม มิติทางการเงินไม่ได้ออกแบบมาเพื่อกำหนดความต้องการของการดำเนินการหรือความต้องการทางธุรกิจของนิติบุคคล</span><span class="sxs-lookup"><span data-stu-id="8f25c-113">However, financial dimensions aren’t designed to address the operational or business requirements of legal entities.</span></span> <span data-ttu-id="8f25c-114">ฟังก์ชันการบัญชีระหว่างหน่วยใน Finance and Operations ได้รับการออกแบบมาเพื่อจัดการเฉพาะรายการบัญชีที่สร้างขึ้นโดยธุรกรรมแต่ละรายการ</span><span class="sxs-lookup"><span data-stu-id="8f25c-114">The interunit accounting functionality in Finance and Operations is designed to address only the accounting entries that are created by each transaction.</span></span> 

<span data-ttu-id="8f25c-115">ก่อนที่คุณจะตั้งค่ามิติทางการเงินเป็นนิติบุคคล ให้ประเมินกระบวนการทางธุรกิจของคุณในขอบเขตต่อไปนี้เพื่อกำหนดว่าการตั้งค่านี้จะเหมาะกับองค์กรของคุณหรือไม่:</span><span class="sxs-lookup"><span data-stu-id="8f25c-115">Before you set up financial dimensions as legal entities, evaluate your business processes in the following areas to determine whether this setup will work for your organization:</span></span>

- <span data-ttu-id="8f25c-116">สินค้าคงคลัง</span><span class="sxs-lookup"><span data-stu-id="8f25c-116">Inventory</span></span>
- <span data-ttu-id="8f25c-117">การขายและการซื้อระหว่างมิติทางการเงินและนิติบุคคล</span><span class="sxs-lookup"><span data-stu-id="8f25c-117">Sales and purchases between financial dimensions and legal entities</span></span>
- <span data-ttu-id="8f25c-118">คำนวณภาษีขายและการรายงาน</span><span class="sxs-lookup"><span data-stu-id="8f25c-118">Sales tax calculation and reporting</span></span>
- <span data-ttu-id="8f25c-119">การรายงานการดำเนินงาน</span><span class="sxs-lookup"><span data-stu-id="8f25c-119">Operational reporting</span></span>

<span data-ttu-id="8f25c-120">นี่คือบางส่วนของข้อจำกัด:</span><span class="sxs-lookup"><span data-stu-id="8f25c-120">Here are some of the limitations:</span></span>

- <span data-ttu-id="8f25c-121">คุณสามารถใช้ฟังก์ชันภาษีขายกับนิติบุคคลเท่านั้น ไม่สามารถใช้กับมิติทางการเงิน</span><span class="sxs-lookup"><span data-stu-id="8f25c-121">You can use sales tax functionality only with legal entities, not with financial dimensions.</span></span>
- <span data-ttu-id="8f25c-122">บางรายงานไม่รวมถึงมิติทางการเงิน</span><span class="sxs-lookup"><span data-stu-id="8f25c-122">Some reports don't include financial dimensions.</span></span> <span data-ttu-id="8f25c-123">ดังนั้น เมื่อต้องการรายงานตามมิติทางการเงิน คุณอาจต้องปรับเปลี่ยนรายงาน</span><span class="sxs-lookup"><span data-stu-id="8f25c-123">Therefore, to report by financial dimension, you might have to modify the reports.</span></span>

## <a name="custom-dimensions"></a><span data-ttu-id="8f25c-124">มิติที่กำหนดเอง</span><span class="sxs-lookup"><span data-stu-id="8f25c-124">Custom dimensions</span></span>

<span data-ttu-id="8f25c-125">เพื่อสร้างมิติทางการเงินที่กำหนดโดยผู้ใช้ในฟิลด์ **ใช้ค่าจาก** ให้เลือก **&lt; มิติที่กำหนดเอง &gt;**</span><span class="sxs-lookup"><span data-stu-id="8f25c-125">To create a user-defined financial dimension, in the **Use values from** field, select **&lt; Custom dimension &gt;**.</span></span> <span data-ttu-id="8f25c-126">คุณยังสามารถระบุตัวพรางบัญชีเพื่อจำกัดจำนวนและชนิดของข้อมูลที่คุณสามารถป้อนสำหรับค่ามิติ</span><span class="sxs-lookup"><span data-stu-id="8f25c-126">You can also specify an account mask to limit the amount and type of information that you can enter for dimension values.</span></span> <span data-ttu-id="8f25c-127">คุณสามารถป้อนอักขระที่เหมือนกันสำหรับแต่ละค่ามิติ เช่นตัวอักษรหรือเครื่องหมายยัติภังค์ (-)</span><span class="sxs-lookup"><span data-stu-id="8f25c-127">You can enter characters that remain the same for each dimension value, such as letters or a hyphen (-).</span></span> <span data-ttu-id="8f25c-128">นอกจากนี้ คุณยังสามารถป้อนเครื่องหมายตัวเลข (\#) กับเครื่องหมายและ (&) เป็นตัวยึดตำแหน่งสำหรับตัวอักษรและตัวเลขที่จะเปลี่ยนแปลงทุกครั้งที่มีการสร้างค่ามิติได้ด้วย</span><span class="sxs-lookup"><span data-stu-id="8f25c-128">You can also enter number signs (\#) and ampersands (&) as placeholders for letters and numbers that will change every time that a dimension value is created.</span></span> <span data-ttu-id="8f25c-129">ใช้เครื่องหมายตัวเลข (\#) เป็นตัวยึดตำแหน่งสำหรับตัวเลข และเครื่องหมายและ (&) เป็นตัวยึดตำแหน่งสำหรับตัวอักษร</span><span class="sxs-lookup"><span data-stu-id="8f25c-129">Use a number sign (\#) as a placeholder for a number and an ampersand (&) as a placeholder for a letter.</span></span> <span data-ttu-id="8f25c-130">ฟิลด์สำหรับตัวกำหนดรูปแบบนี้สามารถใช้ได้ก็ต่อเมื่อคุณเลือก **&lt; มิติที่กำหนดเอง &gt;** ในฟิลด์ **ใช้ค่าจาก**</span><span class="sxs-lookup"><span data-stu-id="8f25c-130">The field for the format mask is available only when you select **&lt; Custom dimension &gt;** in the **Use values from** field.</span></span>

<span data-ttu-id="8f25c-131">**ตัวอย่าง**</span><span class="sxs-lookup"><span data-stu-id="8f25c-131">**Example**</span></span>

<span data-ttu-id="8f25c-132">เพื่อจำกัดค่ามิติจะตัวอักษร "CC" และตัวเลขสามตัว คุณต้องป้อน **CC-\#\#\#** เป็นตัวกำหนดรูปแบบ</span><span class="sxs-lookup"><span data-stu-id="8f25c-132">To limit the dimension value to the letters "CC" and three numbers, enter **CC-\#\#\#** as the format mask.</span></span>

## <a name="entity-backed-dimensions"></a><span data-ttu-id="8f25c-133">มิติที่สำรองไว้ในเอนทิตี้</span><span class="sxs-lookup"><span data-stu-id="8f25c-133">Entity-backed dimensions</span></span>

<span data-ttu-id="8f25c-134">เพื่อสร้างมิติทางการเงินสำรองในเอนทิตี้ ในฟิลด์ **ใช้ค่าจาก** ให้เลือกเอนทิตี้ที่กำหนดโดยระบบเพื่อเป็นฐานของมิติทางการเงิน</span><span class="sxs-lookup"><span data-stu-id="8f25c-134">To create an entity-backed financial dimension, in the **Use values from** field, select a system-defined entity to base the financial dimension on.</span></span> <span data-ttu-id="8f25c-135">จากนั้นค่ามิติทางการเงินจะถูกสร้างขึ้นจากเอนทิตี้นี้</span><span class="sxs-lookup"><span data-stu-id="8f25c-135">Financial dimension values are then created from that entity.</span></span> <span data-ttu-id="8f25c-136">ตัวอย่างเช่น เพื่อสร้างค่ามิติสำหรับโครงการ ให้เลือก **โครงการ**</span><span class="sxs-lookup"><span data-stu-id="8f25c-136">For example, to create dimension values for projects, select **Projects**.</span></span> <span data-ttu-id="8f25c-137">จากนั้นมีการสร้างค่ามิติสำหรับแต่ละชื่อโครงการ</span><span class="sxs-lookup"><span data-stu-id="8f25c-137">A dimension value is then created for each project name.</span></span> <span data-ttu-id="8f25c-138">หน้า **ค่ามิติทางการเงิน** แสดงค่าสำหรับเอนทิตี้</span><span class="sxs-lookup"><span data-stu-id="8f25c-138">The **Financial dimension values** page shows the values for the entity.</span></span> <span data-ttu-id="8f25c-139">ถ้าค่านั้นเป็นค่าเฉพาะบริษัท หน้ายังคงแสดงบริษัท</span><span class="sxs-lookup"><span data-stu-id="8f25c-139">If those values are company-specific, the page also shows the company.</span></span>

## <a name="activating-dimensions"></a><span data-ttu-id="8f25c-140">การเรียกใช้งานมิติ</span><span class="sxs-lookup"><span data-stu-id="8f25c-140">Activating dimensions</span></span>

<span data-ttu-id="8f25c-141">เมื่อคุณเรียกใช้งานมิติทางการเงิน ตารางจะมีการอัพเดทเพื่อให้รวมชื่อของมิติทางการเงิน</span><span class="sxs-lookup"><span data-stu-id="8f25c-141">When you activate a financial dimension, the table is updated so that it includes the name of the financial dimension.</span></span> <span data-ttu-id="8f25c-142">มิติที่ถูกลบไปแล้วจะถูกเอาออก</span><span class="sxs-lookup"><span data-stu-id="8f25c-142">Deleted dimensions are removed.</span></span> <span data-ttu-id="8f25c-143">คุณสามารถป้อนค่ามิติ ก่อนที่คุณเรียกใช้งานมิติทางการเงิน</span><span class="sxs-lookup"><span data-stu-id="8f25c-143">You can enter dimension values before you activate a financial dimension.</span></span> <span data-ttu-id="8f25c-144">อย่างไรก็ตาม จะไม่สามารถใช้มิติทางการเงินได้จนกว่าจะมีการเรียกใช้งาน</span><span class="sxs-lookup"><span data-stu-id="8f25c-144">However, a financial dimension can't be consumed anywhere until it's activated.</span></span> <span data-ttu-id="8f25c-145">ตัวอย่างเช่น คุณไม่สามารถเพิ่มมิติทางการเงินไปยังโครงสร้างทางบัญชีจนกว่าจะมีการเรียกใช้งานมิติทางการเงิน</span><span class="sxs-lookup"><span data-stu-id="8f25c-145">For example, you can't add a financial dimension to an account structure until the financial dimension has been activated.</span></span> <span data-ttu-id="8f25c-146">เมื่อคุณคลิก **เปิดใช้งาน** จะอัพเดตมิติทั้งหมดและแสดงการเปลี่ยนแปลงสถานะ</span><span class="sxs-lookup"><span data-stu-id="8f25c-146">When you click **Activate**, all dimensions are updated and show status changes.</span></span> 

## <a name="translations"></a><span data-ttu-id="8f25c-147">การแปล</span><span class="sxs-lookup"><span data-stu-id="8f25c-147">Translations</span></span>

<span data-ttu-id="8f25c-148">ในหน้า **การแปลข้อความ** คุณสามารถป้อนข้อความสำหรับมิติทางการเงินที่เลือกในภาษาต่าง ๆ ได้</span><span class="sxs-lookup"><span data-stu-id="8f25c-148">On the **Text translation** page, you can enter text for the selected financial dimension in various languages.</span></span> <span data-ttu-id="8f25c-149">ในหน้า **การแปลบัญชีหลัก** คุณสามารถป้อนข้อความสำหรับบัญชีหลักในภาษาต่าง ๆ ได้</span><span class="sxs-lookup"><span data-stu-id="8f25c-149">On the **Main account translation** page, you can enter text for the main account in various languages.</span></span> 

## <a name="legal-entity-overrides"></a><span data-ttu-id="8f25c-150">การแทนที่นิติบุคคล</span><span class="sxs-lookup"><span data-stu-id="8f25c-150">Legal entity overrides</span></span>

<span data-ttu-id="8f25c-151">มิติทั้งหมดไม่ใช่ว่าจะถูกต้องสำหรับนิติบุคคลทั้งหมด</span><span class="sxs-lookup"><span data-stu-id="8f25c-151">Not all dimensions are valid for all legal entities.</span></span> <span data-ttu-id="8f25c-152">นอกจากนี้ มิติบางมิติอาจจะเกี่ยวข้องเฉพาะสำหรับรอบระยะเวลาที่ระบุ</span><span class="sxs-lookup"><span data-stu-id="8f25c-152">Additionally, some dimensions might be relevant only for a specific period.</span></span> <span data-ttu-id="8f25c-153">ในกรณีดังกล่าว คุณสามารถใช้ส่วนของ **การแทนที่นิติบุคคล** เพื่อกำหนดบริษัทที่มิติควรจะถูกระงับ เจ้าของ</span><span class="sxs-lookup"><span data-stu-id="8f25c-153">In these cases, you can use the **Legal entity overrides** section to specify the companies that the dimension should be suspended for, the owner, and the period when the dimension is active.</span></span>

## <a name="deleting-financial-dimensions"></a><span data-ttu-id="8f25c-154">การลบมิติทางการเงิน</span><span class="sxs-lookup"><span data-stu-id="8f25c-154">Deleting financial dimensions</span></span>

<span data-ttu-id="8f25c-155">หากต้องการช่วยรักษาความถูกต้องในการอ้างอิงของข้อมูล มิติทางการเงินจะไม่ค่อยถูกลบ</span><span class="sxs-lookup"><span data-stu-id="8f25c-155">To help maintain referential integrity of the data, financial dimensions can rarely be deleted.</span></span> <span data-ttu-id="8f25c-156">ถ้าคุณพยายามที่จะลบมิติทางการเงิน จะมีการประเมินตามเงื่อนไขต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="8f25c-156">If you try to delete a financial dimension, the following criteria are evaluated:</span></span>

- <span data-ttu-id="8f25c-157">มิติทางการเงินถูกใช้ในธุรกรรมที่ลงรายการบัญชีแล้วและที่ยังไม่ได้ลงรายการบัญชีใดๆ หรือประเภทของชุดค่ามิติใดๆ หรือไม่</span><span class="sxs-lookup"><span data-stu-id="8f25c-157">Has the financial dimension been used on any posted or unposted transactions, or any type of dimension value combination?</span></span>
- <span data-ttu-id="8f25c-158">มิติทางการเงินถูกใช้ในโครงสร้างทางบัญชีใดๆ ที่ใช้งานอยู่ โครงสร้างกฎขั้นสูง หรือชุดมิติทางการเงินหรือไม่</span><span class="sxs-lookup"><span data-stu-id="8f25c-158">Is the financial dimension used in any active account structure, advanced rule structure, or financial dimension set?</span></span>
- <span data-ttu-id="8f25c-159">มีมิติทางการเงินเป็นส่วนหนึ่งของรูปแบบการรวมมิติทางการเงินหรือไม่</span><span class="sxs-lookup"><span data-stu-id="8f25c-159">Is the financial dimension part of a default financial dimension integration format?</span></span>
- <span data-ttu-id="8f25c-160">มิติทางการเงินถูกตั้งค่าเป็นมิติเริ่มต้นหรือไม่</span><span class="sxs-lookup"><span data-stu-id="8f25c-160">Has the financial dimension been set up as a default dimension?</span></span>

<span data-ttu-id="8f25c-161">ถ้าเป็นไปตามเงื่อนไขใดๆ ก็ตาม คุณจะไม่สามารถลบมิติทางการเงินได้</span><span class="sxs-lookup"><span data-stu-id="8f25c-161">If any of the criteria are met, you can't delete the financial dimension.</span></span>


<span data-ttu-id="8f25c-162">สำหรับข้อมูลเพิ่มเติม ให้ดูที่หัวข้อต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="8f25c-162">For more information, see the following topics:</span></span>
- [<span data-ttu-id="8f25c-163">กำหนดมิติทางการเงิน</span><span class="sxs-lookup"><span data-stu-id="8f25c-163">Define financial dimensions</span></span>](tasks/define-financial-dimensions.md)
- [<span data-ttu-id="8f25c-164">รักษาเท็มเพลตเริ่มต้นของมิติทางการเงิน</span><span class="sxs-lookup"><span data-stu-id="8f25c-164">Maintain financial dimension default templates</span></span>](tasks/maintain-financial-dimension-default-templates.md)

