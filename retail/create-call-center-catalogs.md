---
title: "สร้างแค็ตตาล็อกของศูนย์บริการ"
description: "บทความนี้แสดงภาพรวมของกระบวนการสร้างแค็ตตาล็อกสำหรับศูนย์บริการ"
author: josaw1
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations, Retail
ms.custom: 16212
ms.assetid: c9d1b9df-82e8-4b3a-a13c-166df8b9718e
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.translationtype: Human Translation
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: 94ff6d74d4a11b3b04be6b69f85e778c3b45de92
ms.contentlocale: th-th
ms.lasthandoff: 08/29/2017

---

# <a name="create-a-call-center-catalog"></a><span data-ttu-id="21157-103">สร้างแค็ตตาล็อกของศูนย์บริการ</span><span class="sxs-lookup"><span data-stu-id="21157-103">Create a call center catalog</span></span>

[!include[banner](includes/banner.md)]


<span data-ttu-id="21157-104">บทความนี้แสดงภาพรวมของกระบวนการสร้างแค็ตตาล็อกสำหรับศูนย์บริการ</span><span class="sxs-lookup"><span data-stu-id="21157-104">This article provides an overview of the process for creating a catalog for a call center.</span></span> 

<span data-ttu-id="21157-105">ในศูนย์บริการทางโทรศัพท์ คุณสามารถใช้แค็ตตาล็อกผลิตภัณฑ์เพื่อระบุผลิตภัณฑ์ที่คุณต้องการเสนอให้แก่ลูกค้า </span><span class="sxs-lookup"><span data-stu-id="21157-105">In a call center, you can use product catalogs to identify the products that you want to offer to customers.</span></span> <span data-ttu-id="21157-106">ศูนย์บริการโดยทั่วไปใช้แค็ตตาล็อกที่พิมพ์</span><span class="sxs-lookup"><span data-stu-id="21157-106">Call centers typically use printed catalogs.</span></span> <span data-ttu-id="21157-107">การออกแบบและการผลิตของแค็ตตาล็อกที่พิมพ์จะถูกจัดการนอก Microsoft Dynamics 365 for Retail</span><span class="sxs-lookup"><span data-stu-id="21157-107">The design and production of a printed catalog is handled outside Microsoft Dynamics 365 for Retail.</span></span> <span data-ttu-id="21157-108">อย่างไรก็ตาม คุณสามารถสร้างและจัดเก็บแค็ตตาล็อกในรูปแบบดิจิทัลได้โดยการใช้แบบฟอร์มเดียวกันกับที่คุณใช้การตั้งค่าแค็ตตาล็อกการขายปลีกออนไลน์</span><span class="sxs-lookup"><span data-stu-id="21157-108">However, you can create and store a digital form of a catalog by using the same forms that you use to set up online retail catalogs.</span></span> <span data-ttu-id="21157-109">ก่อนที่คุณสามารถสร้างแค็ตตาล็อกได้ คุณต้องตั้งค่าการจัดประเภทผลิตภัณฑ์และมอบการจัดประเภทให้กับศูนย์บริการ</span><span class="sxs-lookup"><span data-stu-id="21157-109">Before you can create a catalog, you must set up product assortments and assign the assortments to a call center.</span></span> <span data-ttu-id="21157-110">จากนั้นคุณเพิ่มผลิตภัณฑ์ไปยังแค็ตตาล็อกได้โดยการเลือกผลิตภัณฑ์จากการจัดประเภทเหล่านี้</span><span class="sxs-lookup"><span data-stu-id="21157-110">You then add products to the catalog by selecting products from these assortments.</span></span> <span data-ttu-id="21157-111">หลังจากที่ได้เพิ่มผลิตภัณฑ์ลงในแค็ตตาล็อกจนแค็ตตาล็อกเสร็จสมบูรณ์แล้ว คุณต้องตรวจสอบความถูกต้องของแค็ตตาล็อกเพื่อตรวจสอบความถูกต้องของข้อมูล</span><span class="sxs-lookup"><span data-stu-id="21157-111">After products have been added to the catalog, and the catalog is complete, you must validate the catalog to verify the data.</span></span> <span data-ttu-id="21157-112">จากนั้นคุณต้องส่งแค็ตตาล็อกเพื่อตรวจทานและอนุมัติ</span><span class="sxs-lookup"><span data-stu-id="21157-112">You must then submit the catalog for review and approval.</span></span> <span data-ttu-id="21157-113">หลังจากที่มีอนุมัติแค็ตตาล็อก จึงจะสามารถเผยแพร่ได้</span><span class="sxs-lookup"><span data-stu-id="21157-113">After the catalog is approved, it can be published.</span></span> <span data-ttu-id="21157-114">เมื่อสร้างแค็ตตาล็อกศูนย์บริการแล้ว คุณสามารถทำสแนปช็อตของข้อมูลแค็ตตาล็อกในเวลาที่มีการเผยแพร่แค็ตตาล็อก</span><span class="sxs-lookup"><span data-stu-id="21157-114">When a call center catalog is created, you can take a snapshot of the catalog data at the time when the catalog is published.</span></span> <span data-ttu-id="21157-115">ฟังก์ชันสแนปช็อตนี้ช่วยให้คุณเข้าถึงแค็ตตาล็อกรุ่นใดรุ่นหนึ่งได้แม้ว่าแค็ตตาล็อกนั้นจะมีการเปลี่ยนแปลงและอัพเดตในภายหลัง</span><span class="sxs-lookup"><span data-stu-id="21157-115">This snapshot functionality lets you access a particular version of the catalog even if the catalog is later changed and updated.</span></span> <span data-ttu-id="21157-116">แค็ตตาล็อกของศูนย์บริการสามารถตั้งค่าเพื่อให้รวมคุณสมบัติเสริมเหล่านี้เข้าไปด้วยได้</span><span class="sxs-lookup"><span data-stu-id="21157-116">Call center catalogs can also be set up to include the following optional features.</span></span>

-   <span data-ttu-id="21157-117">**รหัสต้นทาง** – รหัสที่ใช้ในการติดตามการตอบสนองของลูกค้าที่มีต่อการส่งเมลแค็ตตาล็อกเฉพาะ</span><span class="sxs-lookup"><span data-stu-id="21157-117">**Source codes** – Codes that are used to track the customer response to particular catalog mailings.</span></span>
-   <span data-ttu-id="21157-118">**ผลิตภัณฑ์ฟรี**– ผลิตภัณฑ์ที่รวมอยู่ในใบสั่งของลูกค้าที่ไม่มีค่าธรรมเนียมเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="21157-118">**Free products** – Products that are included in a customer's order at no additional charge.</span></span> <span data-ttu-id="21157-119">ผลิตภัณฑ์เหล่านี้จะถูกเพิ่มโดยอัตโนมัติไปยังใบสั่งเมื่อรหัสแหล่งที่มาสำหรับแค็ตตาล็อกถูกป้อนลงในใบสั่ง</span><span class="sxs-lookup"><span data-stu-id="21157-119">These products are automatically added to the order when the source code for the catalog is entered into the order.</span></span>
-   <span data-ttu-id="21157-120">**สคริปต์**– ข้อความที่ผู้ปฏิบัติงานของศูนย์บริการอ่านให้ลูกค้าฟังเมื่อมีการสร้างใบสั่งขาย</span><span class="sxs-lookup"><span data-stu-id="21157-120">**Scripts** – Texts that a call center worker reads to a customer when a sales order is being created.</span></span> <span data-ttu-id="21157-121">สคริปต์สามารถรวมคำทักทายหรือคำแนะนำเกี่ยวกับการซื้อได้</span><span class="sxs-lookup"><span data-stu-id="21157-121">Scripts can include greetings or purchase suggestions.</span></span>
-   <span data-ttu-id="21157-122">**การเพิ่มการขายหรือเป็นการขายสินค้าชนิดอื่น** - สินค้าที่แสดงเป็นคำแนะนำเมื่อมีผลิตภัณฑ์เฉพาะถูกเพิ่มในใบสั่ง</span><span class="sxs-lookup"><span data-stu-id="21157-122">**Upsell or cross-sell items** - Items that are displayed as a suggestion when a specific product is added to the order.</span></span>

<span data-ttu-id="21157-123">ตัวเลือกเหล่านี้ต้องตั้งค่าก่อนที่แค็ตตาล็อกจะถูกอนุมัติให้เผยแพร่</span><span class="sxs-lookup"><span data-stu-id="21157-123">These options must be set up before the catalog is approved and published.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="21157-124">ข้อกำหนดเบื้องต้น</span><span class="sxs-lookup"><span data-stu-id="21157-124">Prerequisites</span></span>
<span data-ttu-id="21157-125">งานต่อไปนี้ต้องเสร็จสมบูรณ์ก่อนที่คุณจะเริ่มต้น:</span><span class="sxs-lookup"><span data-stu-id="21157-125">The following tasks must be completed before you start:</span></span>

-   <span data-ttu-id="21157-126">ตั้งค่าผลิตภัณฑ์และการจัดประเภทผลิตภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="21157-126">Set up products and product assortments.</span></span>
-   <span data-ttu-id="21157-127">ตั้งค่าผลิตภัณฑ์ขายปลีก</span><span class="sxs-lookup"><span data-stu-id="21157-127">Set up retail products.</span></span>
-   <span data-ttu-id="21157-128">ตั้งค่าการจัดประเภท</span><span class="sxs-lookup"><span data-stu-id="21157-128">Set up an assortment.</span></span>
-   <span data-ttu-id="21157-129">สร้างศูนย์บริการ:</span><span class="sxs-lookup"><span data-stu-id="21157-129">Create a call center.</span></span>
-   <span data-ttu-id="21157-130">ตั้งค่าศูนย์บริการ</span><span class="sxs-lookup"><span data-stu-id="21157-130">Set up a call center.</span></span>
-   <span data-ttu-id="21157-131">เพิ่มศูนย์บริการลงในลำดับชั้นขององค์กร:</span><span class="sxs-lookup"><span data-stu-id="21157-131">Add the call center to an organization hierarchy.</span></span>
-   <span data-ttu-id="21157-132">สร้างหรือแก้ไขลำดับชั้นขององค์กร</span><span class="sxs-lookup"><span data-stu-id="21157-132">Create or modify an organization hierarchy.</span></span>

## <a name="create-a-catalog"></a><span data-ttu-id="21157-133">สร้างแค็ตตาล็อก</span><span class="sxs-lookup"><span data-stu-id="21157-133">Create a catalog</span></span>
<span data-ttu-id="21157-134">คุณต้องสร้างแค็ตตาล็อกก่อน เพิ่มผลิตภัณฑ์ลงในแค็ตตาล็อก จากนั้นตรวจทานและอัพเดแอททริบิวต์สำหรับผลิตภัณฑ์นั้น</span><span class="sxs-lookup"><span data-stu-id="21157-134">You must first create a catalog, add products to the catalog, and then review and update the attributes for the products.</span></span>

## <a name="validate-the-catalog"></a><span data-ttu-id="21157-135">ตรวจสอบความถูกต้องของแค็ตตาล็อก</span><span class="sxs-lookup"><span data-stu-id="21157-135">Validate the catalog</span></span>
<span data-ttu-id="21157-136">หลังจากที่คุณตั้งค่าแค็ตตาล็อกเสร็จสิ้นแล้ว คุณต้องทำการตรวจสอบ</span><span class="sxs-lookup"><span data-stu-id="21157-136">After you've finished setting up the catalog, you must validate it.</span></span> <span data-ttu-id="21157-137">กระบวนการตรวจสอบที่มีข้อมูลที่ต้องการสำหรับแอททริบิวต์ช่องทางและแอททริบิวต์ผลิตภัณฑ์นั้นครบถ้วนและถูกต้องแล้ว และแค็ตตาล็อกนั้นสามารถเผยแพร่ได้</span><span class="sxs-lookup"><span data-stu-id="21157-137">The validation process verifies that the data that is required for channel attributes and product attributes is complete and valid, and that the catalog can be published.</span></span>

## <a name="submit-the-catalog-for-review-and-approval"></a><span data-ttu-id="21157-138">ส่งแค็ตตาล็อกเพื่อตรวจทานและอนุมัติ</span><span class="sxs-lookup"><span data-stu-id="21157-138">Submit the catalog for review and approval</span></span>
<span data-ttu-id="21157-139">หลังจากที่มีการตรวจสอบแค็ตตาล็อก คุณสามารถส่งแค็ตตาล็อกเพื่อตรวจทานและอนุมัติ</span><span class="sxs-lookup"><span data-stu-id="21157-139">After a catalog is validated, you can submit the catalog for review and approval.</span></span> <span data-ttu-id="21157-140">แค็ตตาล็อกต้องได้รับอนุมัติก่อนจึงจะสามารถเผยแพร่ได้</span><span class="sxs-lookup"><span data-stu-id="21157-140">A catalog must be approved before it can be published.</span></span> <span data-ttu-id="21157-141">คุณสามารถตั้งค่าลำดับงานเพื่อให้แค็ตตาล็อกถูกอนุมัติโดยอัตโนมัติ หรือต้องอนุมัติด้วยตนเอง</span><span class="sxs-lookup"><span data-stu-id="21157-141">You can configure a workflow so that catalogs either are automatically approved or require manual approval.</span></span>

## <a name="optional-add-source-codes-free-products-and-scripts"></a><span data-ttu-id="21157-142">ไม่จำเป็น: เพิ่มรหัสต้นทาง ผลิตภัณฑ์ฟรี และสคริปต์</span><span class="sxs-lookup"><span data-stu-id="21157-142">Optional: Add source codes, free products, and scripts</span></span>
<span data-ttu-id="21157-143">คุณยังสามารถเพิ่มรายการต่อไปนี้ไปที่แค็ตตาล็อกของศูนย์บริการ</span><span class="sxs-lookup"><span data-stu-id="21157-143">You can also add the following items to a call center catalog.</span></span> <span data-ttu-id="21157-144">สินค้าเหล่านี้เลือกกำหนดได้</span><span class="sxs-lookup"><span data-stu-id="21157-144">These items are optional.</span></span>

-   <span data-ttu-id="21157-145">**รหัสต้นทาง** สามารถใช้ได้โดยบริษัทที่ให้แค็ตตาล็อกที่พิมพ์ออกมาเพื่อติดตามการตอบสนองลูกค้ากับแค็ตตาล็อกเฉพาะ</span><span class="sxs-lookup"><span data-stu-id="21157-145">**Source codes** can be used by companies that provide printed catalogs to track the customer response to particular catalogs.</span></span> <span data-ttu-id="21157-146">รหัสต้นทางมักจะมีพิมพ์บนด้านหลังของแค็ตตาล็อก และถูกป้อนลงในใบสั่งขายเมื่อลูกค้าทำการซื้อ</span><span class="sxs-lookup"><span data-stu-id="21157-146">Source codes are often printed on the back of a catalog and are entered into the sales order when a customer makes a purchase.</span></span> <span data-ttu-id="21157-147">เมื่อต้องการเพิ่มรหัสแหล่งที่มาลงในแค็ตตาล็อก คุณต้องสร้างตลาดเป้าหมายก่อน</span><span class="sxs-lookup"><span data-stu-id="21157-147">To add a source code to the catalog, you must first create a target market.</span></span> <span data-ttu-id="21157-148">ตลาดเป้าหมายโดยปกติจะถูกแม็ปไปยังรายการส่งเมล์ที่เป็นเจ้าของหรือเช่า</span><span class="sxs-lookup"><span data-stu-id="21157-148">The target market is usually mapped to an owned or rented mailing list.</span></span>
-   <span data-ttu-id="21157-149">**ผลิตภัณฑ์ฟรี** เป็นสินค้าส่งเสริมการขายที่จะรวมการคิดค่าธรรมเนียมในใบสั่งของลูกค้าเมื่อมีการอ้างอิงในแค็ตตาล็อก</span><span class="sxs-lookup"><span data-stu-id="21157-149">**Free products** are promotional items that are included free of charge with the customer's order when the catalog is referenced.</span></span>
-   <span data-ttu-id="21157-150">**สคริปต์** สามารถใช้เพื่อแนะนำการโต้ตอบของผู้ปฏิบัติงานกับลูกค้าในบริบทของแค็ตตาล็อกผลิตภัณฑ์ในแค็ตตาล็อกได้</span><span class="sxs-lookup"><span data-stu-id="21157-150">**Scripts** can be used to guide the worker's interactions with customers in the context of a catalog or a product within a catalog.</span></span>

## <a name="publish-the-catalog"></a><span data-ttu-id="21157-151">เผยแพร่แค็ตตาล็อก</span><span class="sxs-lookup"><span data-stu-id="21157-151">Publish the catalog</span></span>
<span data-ttu-id="21157-152">โดยการเผยแพร่แค็ตตาล็อกสำหรับศูนย์บริการทั้งหมด คุณสรุปข้อมูลผลิตภัณฑ์ในแค็ตตาล็อก</span><span class="sxs-lookup"><span data-stu-id="21157-152">By publishing a catalog for a call center, you finalize the product information in the catalog.</span></span> <span data-ttu-id="21157-153">สิ่งพิมพ์จะบ่งชี้ด้วยว่า แค็ตตาล็อกนั้นพร้อมสำหรับการดำเนินการเพิ่มเติมใด ๆ ที่คุณต้องการดำเนินการ</span><span class="sxs-lookup"><span data-stu-id="21157-153">Publication also indicates that the catalog is ready for any additional actions that you want to perform.</span></span> <span data-ttu-id="21157-154">ตัวอย่างเช่น คุณสามารถสร้างแค็ตตาล็อกที่พิมพ์ออกมา</span><span class="sxs-lookup"><span data-stu-id="21157-154">For example, you can create a printed catalog.</span></span> <span data-ttu-id="21157-155">คุณสามารถเผยแพร่แค็ตตาล็อกของคุณด้วยตนเอง หรือคุณสามารถใช้กระบวนการชุดงานเพื่อเผยแพร่ตามกำหนดการ</span><span class="sxs-lookup"><span data-stu-id="21157-155">You can publish your catalogs manually, or you can use a batch process to publish according to a schedule.</span></span> <span data-ttu-id="21157-156">ก่อนที่คุณจะเผยแพร่แค็ตตาล็อก แค็ตตาล็อกต้องถูกตรวจสอบและอนุมัติแล้ว</span><span class="sxs-lookup"><span data-stu-id="21157-156">Before you can publish a catalog, the catalog must be validated and approved.</span></span> <span data-ttu-id="21157-157">เพื่อเปลี่ยนแค็ตตาล็อกหลังจากมีการเผยแพร่แล้ว คุณสามารถถอนแค็ตตาล็อก และเผยแพร่ใหม่</span><span class="sxs-lookup"><span data-stu-id="21157-157">To change the catalog after it's published, you can retract the catalog and then republish it.</span></span>




