---
title: แก้ไขปัญหาข้อมูลผลิตภัณฑ์
description: หัวข้อนี้จะอธิบายวิธีการแก้ไขปัญหาที่คุณอาจพบขณะทำงานกับข้อมูลผลิตภัณฑ์
author: SmithaNataraj
manager: tfehr
ms.date: 11/04/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: smnatara
ms.search.validFrom: 2020-11-04
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: 4c505ccfd1998acd40dbae715c7fa572e315af2e
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 01/15/2021
ms.locfileid: "5007527"
---
# <a name="troubleshoot-product-information"></a><span data-ttu-id="245d1-103">แก้ไขปัญหาข้อมูลผลิตภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="245d1-103">Troubleshoot product information</span></span>

<span data-ttu-id="245d1-104">หัวข้อนี้จะอธิบายวิธีการแก้ไขปัญหาที่คุณอาจพบขณะทำงานกับข้อมูลผลิตภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="245d1-104">This topic describes how to fix issues that you might encounter while you work with product information.</span></span>

## <a name="i-cant-delete-a-released-product"></a><span data-ttu-id="245d1-105">ฉันไม่สามารถลบผลิตภัณฑ์ที่นำออกใช้ได้</span><span class="sxs-lookup"><span data-stu-id="245d1-105">I can't delete a released product.</span></span>

### <a name="issue-description"></a><span data-ttu-id="245d1-106">คำอธิบายปัญหา</span><span class="sxs-lookup"><span data-stu-id="245d1-106">Issue description</span></span>

<span data-ttu-id="245d1-107">คุณสามารถลบผลิตภัณฑ์ที่นำออกใช้และตัวแปรทั้งหมดได้เฉพาะเมื่อผลิตภัณฑ์ที่นำออกใช้ไม่มีธุรกรรมที่เกี่ยวข้องใด ๆ</span><span class="sxs-lookup"><span data-stu-id="245d1-107">You can delete a released product and all its variants only if the released product doesn't have any related transactions.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="245d1-108">การแก้ไขปัญหา</span><span class="sxs-lookup"><span data-stu-id="245d1-108">Issue resolution</span></span>

<span data-ttu-id="245d1-109">ทำตามขั้นตอนต่อไปนี้เมื่อต้องการลบผลิตภัณฑ์หรือผลิตภัณฑ์หลักที่นำออกใช้</span><span class="sxs-lookup"><span data-stu-id="245d1-109">Follow these steps to delete a released product or product master.</span></span>

1. <span data-ttu-id="245d1-110">ปิดธุรกรรมที่เปิดค้างไว้ทั้งหมดสำหรับสินค้า</span><span class="sxs-lookup"><span data-stu-id="245d1-110">Close all open transactions for the items.</span></span>
1. <span data-ttu-id="245d1-111">ลดสินค้าคงคลังเป็น 0 (ศูนย์)</span><span class="sxs-lookup"><span data-stu-id="245d1-111">Reduce the inventory to 0 (zero).</span></span>
1. <span data-ttu-id="245d1-112">ดำเนินการปิดสินค้าคงคลัง</span><span class="sxs-lookup"><span data-stu-id="245d1-112">Perform inventory closing.</span></span>
1. <span data-ttu-id="245d1-113">ลบผลิตภัณฑ์ย่อยทั้งหมดสำหรับผลิตภัณฑ์หลักที่คุณต้องการลบออก</span><span class="sxs-lookup"><span data-stu-id="245d1-113">Delete all product variants for the product master that you want to delete.</span></span>

## <a name="can-i-change-the-item-number-of-a-released-product"></a><span data-ttu-id="245d1-114">ฉันสามารถเปลี่ยนหมายเลขสินค้าของผลิตภัณฑ์ที่นำออกใช้ได้หรือไม่</span><span class="sxs-lookup"><span data-stu-id="245d1-114">Can I change the item number of a released product?</span></span>

<span data-ttu-id="245d1-115">ในกรณีส่วนใหญ่ คุณจะไม่สามารถแก้ไขหมายเลขสินค้าสำหรับผลิตภัณฑ์ที่นำออกใช้ได้ เนื่องจากการเปลี่ยนแปลงดังกล่าวจะทำให้ข้อมูลเกิดความเสียหาย</span><span class="sxs-lookup"><span data-stu-id="245d1-115">In most cases, you can't edit item numbers for released products, because that change will cause data to become corrupted.</span></span> <span data-ttu-id="245d1-116">คุณสามารถแก้ไขหมายเลขสินค้าได้เฉพาะเมื่อคุณต้องซ่อมแซมความเสียหายของข้อมูลที่เกิดขึ้นจากการเปลี่ยนชื่อก่อนหน้านี้ของคีย์หลักของผลิตภัณฑ์ที่นำออกใช้ดังกล่าว ตามที่ระบุไว้ในรายการของ [ลักษณะการทำงานที่ถูกลบหรือไม่ได้รับการสนับสนุนสำหรับ Finance and Operations 10.0.0 กับแพลตฟอร์มการปรับปรุง 24](../../fin-ops-core/dev-itpro/migration-upgrade/deprecated-features.md#finance-and-operations-1000-with-platform-update-24)</span><span class="sxs-lookup"><span data-stu-id="245d1-116">You can edit the item number only if you must repair data corruption that was caused by a previous rename of the primary key of that released product, as mentioned in the list of [removed or deprecated features for Finance and Operations 10.0.0 with Platform update 24](../../fin-ops-core/dev-itpro/migration-upgrade/deprecated-features.md#finance-and-operations-1000-with-platform-update-24).</span></span>

<span data-ttu-id="245d1-117">ถ้าคุณต้องการให้สามารถแก้ไขหมายเลขสินค้าสำหรับผลิตภัณฑ์ที่นำออกใช้ [ลงคะแนนสำหรับความคิดนี้ในพอร์ทัลแนวคิด](https://experience.dynamics.com/ideas/idea/?ideaid=660fcb15-875d-ea11-b698-0003ff68bc25)</span><span class="sxs-lookup"><span data-stu-id="245d1-117">If you want to be able to edit item numbers for released products, [vote for this idea in Ideas portal](https://experience.dynamics.com/ideas/idea/?ideaid=660fcb15-875d-ea11-b698-0003ff68bc25).</span></span>

## <a name="the-default-flushing-principle-from-the-product-isnt-being-entered-on-the-bill-of-materials-line"></a><span data-ttu-id="245d1-118">ไม่มีการป้อนหลักการลบรายการบัญชีเริ่มต้นจากผลิตภัณฑ์ในรายการสูตรการผลิต</span><span class="sxs-lookup"><span data-stu-id="245d1-118">The default flushing principle from the product isn't being entered on the bill of materials line.</span></span>

### <a name="issue-description"></a><span data-ttu-id="245d1-119">คำอธิบายปัญหา</span><span class="sxs-lookup"><span data-stu-id="245d1-119">Issue description</span></span>

<span data-ttu-id="245d1-120">เมื่อคุณเพิ่มสินค้าลงในรายการสูตรการผลิต (BOM) ระบบจะไม่ใช้ข้อมูลหลักของการล้างข้อมูลเริ่มต้นที่ตั้งค่าไว้สำหรับสินค้า</span><span class="sxs-lookup"><span data-stu-id="245d1-120">When you add an item to a bill of materials (BOM) line, the system doesn't use the default flushing principle information that is set up for the item.</span></span> <span data-ttu-id="245d1-121">กล่าวอีกอย่างหนึ่งคือ หลักการล้างข้อมูลจากสินค้าจะไม่ปรากฏบนหน้า **รายการ BOM**</span><span class="sxs-lookup"><span data-stu-id="245d1-121">In other words, the flushing principle from the item doesn't appear on the **BOM line** page.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="245d1-122">การแก้ไขปัญหา</span><span class="sxs-lookup"><span data-stu-id="245d1-122">Issue resolution</span></span>

<span data-ttu-id="245d1-123">ถ้าคุณระบุหลักการของการล้างบนรายการ BOM จะมีการใช้กับรายการ BOM ดังกล่าว</span><span class="sxs-lookup"><span data-stu-id="245d1-123">If you specify a flushing principle on a BOM line, it will apply to that BOM line.</span></span> <span data-ttu-id="245d1-124">อย่างไรก็ตาม ถ้าหลักการของการล้างว่างเปล่าหรือถ้าไม่ได้ตั้งค่าไว้ในรายการ BOM จะมีการใช้หลักการของการล้างที่ตั้งค่าไว้ในสินค้าจะยังคงใช้กับรายการ BOM ดังกล่าว ถึงแม้ว่าจะไม่มีการแสดงอยู่บนรายการ BOM</span><span class="sxs-lookup"><span data-stu-id="245d1-124">However, if the flushing principle is blank, or if it isn't set on a BOM line, the flushing principle that is set on the item will still apply to that BOM line, even though it isn't shown on the BOM line.</span></span>

<span data-ttu-id="245d1-125">ตรรกะการกำหนดค่าเริ่มต้นสำหรับลักษณะการทำงานอื่น ๆ ใน Microsoft Dynamics 365 Supply Chain Management โดยทั่วไปไม่ทำงานในลักษณะนี้</span><span class="sxs-lookup"><span data-stu-id="245d1-125">The defaulting logic for other features in Microsoft Dynamics 365 Supply Chain Management doesn't usually work in this way.</span></span> <span data-ttu-id="245d1-126">อย่างไรก็ตาม ลักษณะการทำงานปัจจุบันจึงไม่สามารถเปลี่ยนแปลงได้</span><span class="sxs-lookup"><span data-stu-id="245d1-126">However, the current behavior can't be changed.</span></span> <span data-ttu-id="245d1-127">มิฉะนั้น การเลือกกำหนดที่มีอยู่ซึ่งอาจใช้งานได้ไม่ถูกต้อง</span><span class="sxs-lookup"><span data-stu-id="245d1-127">Otherwise, some existing customizations that rely on it might be broken.</span></span>

## <a name="the-system-lets-me-save-duplicate-bar-codes-for-different-items-or-for-the-same-item-that-has-different-dimensions"></a><span data-ttu-id="245d1-128">ระบบช่วยให้ฉันบันทึกบาร์โค้ดที่ซ้ำกันสำหรับสินค้าต่าง ๆ หรือสำหรับสินค้าเดียวกันที่มีมิติที่แตกต่างกัน</span><span class="sxs-lookup"><span data-stu-id="245d1-128">The system lets me save duplicate bar codes for different items or for the same item that has different dimensions.</span></span>

<span data-ttu-id="245d1-129">ระบบไม่ได้บังคับใช้บาร์โค้ดที่ไม่ซ้ำกันในขณะนี้ และการเพิ่มข้อจำกัดนี้จะเป็นการเปลี่ยนแปลงการแบ่ง</span><span class="sxs-lookup"><span data-stu-id="245d1-129">The system doesn't currently enforce unique bar codes, and the addition of this restriction would be a breaking change.</span></span> <span data-ttu-id="245d1-130">ในความเป็นจริง Microsoft มีหลักฐานว่าการติดตั้งลูกค้าที่มีอยู่บางรายการจะถูกแบ่งด้วยการเปลี่ยนแปลงนี้</span><span class="sxs-lookup"><span data-stu-id="245d1-130">In fact, Microsoft has evidence that some existing customer installations would be broken by this change.</span></span> <span data-ttu-id="245d1-131">อย่างไรก็ตาม เราจะพิจารณาการเปลี่ยนแปลงการออกแบบที่กว้างขึ้นเพื่อเปิดใช้งานลักษณะการทำงานนี้ในอนาคต</span><span class="sxs-lookup"><span data-stu-id="245d1-131">However, we will consider a broader design change to enable this feature in the future.</span></span>

## <a name="i-receive-the-following-error-message-when-i-edit-item-record-templates-the-warehouse-location-cannot-be-created-because-the-item-is-not-stocked-to-stock-items-the-stocked-product-option-on-the-associated-item-model-group-must-be-selected"></a><span data-ttu-id="245d1-132">ฉันได้รับข้อความแสดงข้อผิดพลาดต่อไปนี้เมื่อแก้ไขแม่แบบเรกคอร์ดสินค้า: "ไม่สามารถสร้างที่ตั้งคลังสินค้าได้เนื่องจากสินค้าไม่ได้เก็บในคลัง</span><span class="sxs-lookup"><span data-stu-id="245d1-132">I receive the following error message when I edit item record templates: "The warehouse location cannot be created because the item is not stocked.</span></span> <span data-ttu-id="245d1-133">ไปยังสินค้าคงคลัง ตัวเลือกผลิตภัณฑ์ที่เก็บในคลังบนกลุ่มแบบจำลองสินค้าที่เกี่ยวข้องต้องเลือก"</span><span class="sxs-lookup"><span data-stu-id="245d1-133">To stock items, the Stocked product option on the associated item model group must be selected."</span></span>

### <a name="issue-description"></a><span data-ttu-id="245d1-134">คำอธิบายปัญหา</span><span class="sxs-lookup"><span data-stu-id="245d1-134">Issue description</span></span>

<span data-ttu-id="245d1-135">ปัญหานี้จะเกิดขึ้นถ้าคุณทำตามขั้นตอนต่อไปนี้เพื่อพยายามสร้างแม่แบบสำหรับสินค้าที่ไม่ได้เก็บในคลัง</span><span class="sxs-lookup"><span data-stu-id="245d1-135">This issue occurs if you follow these steps to try to create a template for an item that isn't stocked.</span></span>

1. <span data-ttu-id="245d1-136">เปิดผลิตภัณฑ์ที่นำออกใช้ที่ไม่ได้เก็บในคลัง</span><span class="sxs-lookup"><span data-stu-id="245d1-136">Open a released product that isn't stocked.</span></span>
1. <span data-ttu-id="245d1-137">บนบานหน้าต่างการดำเนินการ บนแท็บ **ตัวเลือก** เลือก **ข้อมูลเรกคอร์ด**</span><span class="sxs-lookup"><span data-stu-id="245d1-137">On the Action Pane, on the **Options** tab, select **Record info**.</span></span>
1. <span data-ttu-id="245d1-138">ในกล่องโต้ตอบ **ข้อมูลเรกคอร์ด** ให้เลือก **แม่แบบบัญชีบริษัท**</span><span class="sxs-lookup"><span data-stu-id="245d1-138">In the **Record information** dialog box, select **Company accounts template**.</span></span>

<span data-ttu-id="245d1-139">ในกรณีนี้ คุณจะได้รับข้อความแสดงข้อผิดพลาดต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="245d1-139">In this case, you receive the following error message:</span></span>

> <span data-ttu-id="245d1-140">ไม่สามารถสร้างที่ตั้งคลังสินค้าได้เนื่องจากไม่ได้เก็บในคลังสินค้า</span><span class="sxs-lookup"><span data-stu-id="245d1-140">The warehouse location cannot be created because the item is not stocked.</span></span> <span data-ttu-id="245d1-141">ไปยังสินค้าคงคลัง ตัวเลือกผลิตภัณฑ์ที่เก็บในคลังบนกลุ่มแบบจำลองสินค้าที่เกี่ยวข้องต้องเลือก</span><span class="sxs-lookup"><span data-stu-id="245d1-141">To stock items, the Stocked product option on the associated item model group must be selected.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="245d1-142">การแก้ไขปัญหา</span><span class="sxs-lookup"><span data-stu-id="245d1-142">Issue resolution</span></span>

<span data-ttu-id="245d1-143">กระบวนการสร้างแม่แบบผลิตภัณฑ์ต้องใช้ตรรกะเฉพาะของผลิตภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="245d1-143">The process of creating product templates requires extra product-specific logic.</span></span> <span data-ttu-id="245d1-144">ดังนั้น คุณจึงไม่สามารถใช้ปุ่ม **แม่แบบบัญชีบริษัททั่วไป** สำหรับวัตถุประสงค์นี้</span><span class="sxs-lookup"><span data-stu-id="245d1-144">Therefore, you can't use the generic **Company accounts template** button for this purpose.</span></span> <span data-ttu-id="245d1-145">แทนที่จะทำเช่นนั้น ทำตามขั้นตอนเหล่านี้</span><span class="sxs-lookup"><span data-stu-id="245d1-145">Instead, follow these steps.</span></span>

1. <span data-ttu-id="245d1-146">เปิดผลิตภัณฑ์ที่นำออกใช้</span><span class="sxs-lookup"><span data-stu-id="245d1-146">Open a released product.</span></span>
1. <span data-ttu-id="245d1-147">บนบานหน้าต่างการดำเนินการ บนแท็บ **ผลิตภัณฑ์** ในกลุ่ม **ใหม่** ให้เลือก **แม่แบบ \> สร้างแม่แบบที่ใช้ร่วมกัน**</span><span class="sxs-lookup"><span data-stu-id="245d1-147">On the Action Pane, on the **Product** tab, in the **New** group, select **Template \> Create shared template**.</span></span>

## <a name="default-help-text-that-is-added-in-product-attributes-isnt-entered-in-a-released-product"></a><span data-ttu-id="245d1-148">ข้อความวิธีใช้เริ่มต้นที่มีการเพิ่มในแอททริบิวต์ของผลิตภัณฑ์ไม่ได้ป้อนในผลิตภัณฑ์ที่นำออกใช้</span><span class="sxs-lookup"><span data-stu-id="245d1-148">Default Help text that is added in product attributes isn't entered in a released product.</span></span>

<span data-ttu-id="245d1-149">คำอธิบายและข้อความวิธีใช้ที่มีการเพิ่มในแอททริบิวต์ของผลิตภัณฑ์จะไม่สามารถมองเห็นได้หรือป้อนไว้ตามค่าเริ่มต้นในผลิตภัณฑ์ที่นำออกใช้</span><span class="sxs-lookup"><span data-stu-id="245d1-149">A description and Help text that are added in the product attributes aren't visible or entered by default in the released products.</span></span> <span data-ttu-id="245d1-150">ลักษณะการทำงานนี้เกิดจากการออกแบบ</span><span class="sxs-lookup"><span data-stu-id="245d1-150">This behavior is by design.</span></span>

## <a name="the-default-quantity-that-is-entered-differs-when-its-registered-from-a-bom-and-when-its-registered-from-a-bom-version"></a><span data-ttu-id="245d1-151">ปริมาณเริ่มต้นที่ป้อนแตกต่างกันเมื่อลงทะเบียนจาก BOM และเมื่อมีการลงทะเบียนจากรุ่น BOM</span><span class="sxs-lookup"><span data-stu-id="245d1-151">The default quantity that is entered differs when it's registered from a BOM and when it's registered from a BOM version.</span></span>

### <a name="issue-description"></a><span data-ttu-id="245d1-152">คำอธิบายปัญหา</span><span class="sxs-lookup"><span data-stu-id="245d1-152">Issue description</span></span>

<span data-ttu-id="245d1-153">ตามค่าเริ่มต้น เมื่อคุณเพิ่มสินค้าลงใน BOM ปริมาณถูกตั้งค่าเป็น 1 แทนปริมาณที่กำหนดไว้ในฟิลด์ **ปริมาณในใบสั่งต่ำสุด** ในหน้า **การตั้งค่าใบสั่งเริ่มต้น** สำหรับผลิตภัณฑ์ที่เลือก</span><span class="sxs-lookup"><span data-stu-id="245d1-153">By default, when you add an item to a BOM, the quantity is set to 1 instead of the quantity that is defined in the **Min. order quantity** field on the **Default order settings** page for a selected product.</span></span> <span data-ttu-id="245d1-154">อย่างไรก็ตาม เมื่อคุณเพิ่มสินค้าจากรุ่น BOM และมีการเลือกสินค้าและตัวแปร ปริมาณที่ป้อนไว้โดยค่าเริ่มต้นจะคำนึงถึงปริมาณต่ำสุดที่ตั้งค่าไว้ในการตั้งค่าใบสั่งเริ่มต้นสำหรับมิติที่ระบุ</span><span class="sxs-lookup"><span data-stu-id="245d1-154">However, when you add an item from a BOM version, and the item and variant are selected, the quantity that is entered by default takes into account the minimum quantity that is set in the default order settings for the specific dimensions.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="245d1-155">การแก้ไขปัญหา</span><span class="sxs-lookup"><span data-stu-id="245d1-155">Issue resolution</span></span>

<span data-ttu-id="245d1-156">ลักษณะการทำงานนี้คาดการณ์ไว้</span><span class="sxs-lookup"><span data-stu-id="245d1-156">This behavior is expected.</span></span> <span data-ttu-id="245d1-157">อย่างไรก็ตาม ข้อเท็จจริงที่ว่าตรรกะแตกต่างกันใน BOM และรุ่น BOM เป็นปัญหาที่ทราบ</span><span class="sxs-lookup"><span data-stu-id="245d1-157">However, the fact that the logic differs in the BOM and the BOM version is a known issue.</span></span> <span data-ttu-id="245d1-158">อย่างไรก็ตาม ลักษณะการทำงานนี้จะไม่เปลี่ยนแปลงเนื่องจากการเปลี่ยนแปลงอาจส่งผลกระทบต่อสถานการณ์จำลองลูกค้าต่าง ๆ มากมาย</span><span class="sxs-lookup"><span data-stu-id="245d1-158">Nevertheless, this behavior won't be changed, because a change could affect many different customer scenarios.</span></span>

## <a name="in-the-released-product-details-i-cant-change-the-attached-images-that-were-uploaded-from-the-product-document-attachments-data-entity"></a><span data-ttu-id="245d1-159">ในรายละเอียดผลิตภัณฑ์ที่นำออกใช้ ฉันไม่สามารถเปลี่ยนรูปภาพที่แนบซึ่งถูกอัพโหลดจากเอนทิตีข้อมูลเอกสารแนบของเอกสารผลิตภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="245d1-159">In the released product details, I can't change the attached images that were uploaded from the Product document attachments data entity.</span></span>

### <a name="issue-description"></a><span data-ttu-id="245d1-160">คำอธิบายปัญหา</span><span class="sxs-lookup"><span data-stu-id="245d1-160">Issue description</span></span>

<span data-ttu-id="245d1-161">ปัญหานี้อาจเกิดขึ้นเมื่อคุณแนบรูปภาพเข้ากับสินค้าโดยใช้เอนทิตีข้อมูล *เอกสารแนบเอกสารของผลิตภัณฑ์*</span><span class="sxs-lookup"><span data-stu-id="245d1-161">This issue can occur when you attach an image to an item by using the *Product document attachments* data entity.</span></span> <span data-ttu-id="245d1-162">ในกรณีนี้ จะมีการแสดงรูปภาพของสินค้าสำหรับสินค้า</span><span class="sxs-lookup"><span data-stu-id="245d1-162">In this case, the item image is shown for the item.</span></span> <span data-ttu-id="245d1-163">อย่างไรก็ตาม ถ้าคุณเลือก **เปลี่ยนรูปภาพ** ไม่มีสิ่งใดจะแสดงอยู่ในรายการรูปภาพที่อัพโหลด</span><span class="sxs-lookup"><span data-stu-id="245d1-163">However, if you select **Change image**, nothing is shown in the list of uploaded images.</span></span> <span data-ttu-id="245d1-164">นอกจากนี้ จะไม่มีการแสดงเอกสารแนบสำหรับสินค้า</span><span class="sxs-lookup"><span data-stu-id="245d1-164">Additionally, no attachments are shown for the item.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="245d1-165">การแก้ไขปัญหา</span><span class="sxs-lookup"><span data-stu-id="245d1-165">Issue resolution</span></span>

<span data-ttu-id="245d1-166">เอนทิตี *EcoResProductDocumentAttachmentEntity* (*เอกสารแนบของเอกสารผลิตภัณฑ์*) นำเข้าเอกสารแนบเอกสารสำหรับ *ผลิตภัณฑ์* แต่ไม่ใช่สำหรับ *ผลิตภัณฑ์ที่นำออกใช้*</span><span class="sxs-lookup"><span data-stu-id="245d1-166">The *EcoResProductDocumentAttachmentEntity* entity (*Product document attachments*) imports document attachments for *products* but not for *released products*.</span></span> <span data-ttu-id="245d1-167">(ผลิตภัณฑ์ที่นำออกใช้จะเรียกอีกอย่างว่า *สินค้า*) เมื่อต้องการดูเอกสารแนบสำหรับสินค้าบนหน้า **รายละเอียดผลิตภัณฑ์ที่นำออกใช้** คุณต้องใช้เอนทิตี *EcoResReleasedProductDocumentAttachmentEntity* (*เอกสารแนบเอกสารผลิตภัณฑ์ที่นำออกใช้*) แทน</span><span class="sxs-lookup"><span data-stu-id="245d1-167">(Released products are also known as *items*.) To view the attachments for an item on the **Released product details** page, you must use the *EcoResReleasedProductDocumentAttachmentEntity* entity (*Released product document attachments*) instead.</span></span>

## <a name="the-microsoft-flow-connector-shows-the-following-error-message-update-not-allowed-for-field-productnumber"></a><span data-ttu-id="245d1-168">ตัวเชื่อมต่อ Microsoft Flow แสดงข้อความแสดงข้อผิดพลาดต่อไปนี้: "ไม่อนุญาตให้ใช้การอัพเดตสำหรับฟิลด์ 'ProductNumber'</span><span class="sxs-lookup"><span data-stu-id="245d1-168">The Microsoft Flow connector shows the following error message: "Update not allowed for field 'ProductNumber'."</span></span>

### <a name="issue-description"></a><span data-ttu-id="245d1-169">คำอธิบายปัญหา</span><span class="sxs-lookup"><span data-stu-id="245d1-169">Issue description</span></span>

<span data-ttu-id="245d1-170">ปัญหานี้จะเกิดขึ้นถ้าคุณพยายามที่จะอัพเดตฟิลด์ **หมายเลขผลิตภัณฑ์** โดยใช้เอนทิตี *ผลิตภัณฑ์ที่นำออกใช้* V2 และ Microsoft Flow</span><span class="sxs-lookup"><span data-stu-id="245d1-170">This issue occurs if you try to update the **Product number** field by using the *Released products* entity V2 and Microsoft Flow.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="245d1-171">การแก้ไขปัญหา</span><span class="sxs-lookup"><span data-stu-id="245d1-171">Issue resolution</span></span>

<span data-ttu-id="245d1-172">ลักษณะการทำงานนี้คาดการณ์ไว้</span><span class="sxs-lookup"><span data-stu-id="245d1-172">This behavior is expected.</span></span> <span data-ttu-id="245d1-173">ความสามารถในการแก้ไขหมายเลขผลิตภัณฑ์สำหรับผลิตภัณฑ์ที่นำออกใช้ถูกลบออกใน Dynamics 365 Finance and Operations 10.0.0 กับแพลตฟอร์มที่อัพเดต 24 เพื่อช่วยป้องกันความเสียหายของข้อมูล</span><span class="sxs-lookup"><span data-stu-id="245d1-173">The ability to edit the product number for a released product was removed in Dynamics 365 Finance and Operations 10.0.0 with platform update 24 to help prevent data corruption.</span></span> <span data-ttu-id="245d1-174">ในกรณีพิเศษ เมื่อคุณต้องซ่อมแซมความเสียหายของข้อมูลที่เกิดจากการเปลี่ยนชื่อคีย์หลักของผลิตภัณฑ์ที่นำออกใช้ก่อนหน้านี้ คุณสามารถขอให้ Microsoft Support ลบข้อจำกัดนี้ชั่วคราว</span><span class="sxs-lookup"><span data-stu-id="245d1-174">In exceptional cases, where you must repair data corruption that was caused by a previous rename of the primary key of a released product, you can ask Microsoft Support to temporarily remove this restriction.</span></span>

## <a name="i-cant-create-a-released-product-variant-in-another-legal-entity"></a><span data-ttu-id="245d1-175">ฉันไม่สามารถสร้างผลิตภัณฑ์ย่อยที่นำออกใช้ในนิติบุคคลอื่น</span><span class="sxs-lookup"><span data-stu-id="245d1-175">I can't create a released product variant in another legal entity.</span></span>

### <a name="issue-description"></a><span data-ttu-id="245d1-176">คำอธิบายปัญหา</span><span class="sxs-lookup"><span data-stu-id="245d1-176">Issue description</span></span>

<span data-ttu-id="245d1-177">ถ้าคุณพยายามที่จะปล่อยผลิตภัณฑ์หลักโดยไม่มีผลิตภัณฑ์ย่อย และสร้างผลิตภัณฑ์ย่อยในนิติบุคคลแต่ละแห่ง (บริษัท) เนื่องจากจำเป็นต้องใช้ คุณจะไม่สามารถปล่อยผลิตภัณฑ์ย่อยโดยใช้คำแนะนำของผลิตภัณฑ์ย่อย</span><span class="sxs-lookup"><span data-stu-id="245d1-177">If you try to release a product master without variants, and then create the variants in each legal entity (company) as they are required, you won't be able to release the variants by using variant suggestions.</span></span> <span data-ttu-id="245d1-178">นอกจากนี้คุณจะไม่สามารถสร้างผลิตภัณฑ์ย่อยด้วยตนเองได้</span><span class="sxs-lookup"><span data-stu-id="245d1-178">You also won't be able to manually create the variants.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="245d1-179">การแก้ไขปัญหา</span><span class="sxs-lookup"><span data-stu-id="245d1-179">Issue resolution</span></span>

<span data-ttu-id="245d1-180">ลักษณะการทำงานนี้เกิดจากการออกแบบ</span><span class="sxs-lookup"><span data-stu-id="245d1-180">This behavior is by design.</span></span> <span data-ttu-id="245d1-181">ความสัมพันธ์ของผลิตภัณฑ์หลักและมิติที่สามารถใช้เป็นต้นแบบจะถูกเก็บไว้ในระดับที่ใช้ร่วมกัน</span><span class="sxs-lookup"><span data-stu-id="245d1-181">The relations of a product master and the dimensions that the master can take are kept at a shared level.</span></span> <span data-ttu-id="245d1-182">ดังนั้น คุณจึงไม่สามารถสร้างมิติที่พร้อมใช้งานสำหรับข้อมูลหลักของผลิตภัณฑ์ที่ใช้ร่วมกันในนิติบุคคลเฉพาะที่มีการนำมิติเหล่านี้ออกใช้แล้วทำซ้ำกระบวนการในนิติบุคคลแต่ละแห่งที่ต้องการมิติ</span><span class="sxs-lookup"><span data-stu-id="245d1-182">Therefore, you can't create the available dimensions for a shared product master in the specific legal entity where those dimensions are released and then replicate the process in each legal entity where the dimensions are required.</span></span> <span data-ttu-id="245d1-183">คุณต้องเปลี่ยนกระบวนการนำออกใช้ของคุณให้เหมาะกับกระบวนการที่ออกแบบไว้</span><span class="sxs-lookup"><span data-stu-id="245d1-183">Instead, you must change your release process to adapt to the designed process.</span></span>

<span data-ttu-id="245d1-184">นี่คือกระบวนการสำหรับการปล่อยผลิตภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="245d1-184">Here is the process for releasing products.</span></span>

1. <span data-ttu-id="245d1-185">สร้างผลิตภัณฑ์หลักที่ใช้ร่วมกันและมิติที่สามารถนำออกใช้ที่นิติบุคคล</span><span class="sxs-lookup"><span data-stu-id="245d1-185">Create the shared product master and the dimensions that can be released to the legal entities.</span></span>
1. <span data-ttu-id="245d1-186">นำผลิตภัณฑ์ออกใช้กับนิติบุคคลโดยใช้คำแนะนำผลิตภัณฑ์ย่อยหรือด้วยการเพิ่มชุดที่ควรนำออกใช้ด้วยตนเอง</span><span class="sxs-lookup"><span data-stu-id="245d1-186">Release the products to the legal entities either by using variant suggestions or by manually adding the combinations that should be released.</span></span>

<span data-ttu-id="245d1-187">อีกทางหนึ่งคือ คุณสามารถสร้างผลิตภัณฑ์ที่นำออกใช้โดยตรงได้</span><span class="sxs-lookup"><span data-stu-id="245d1-187">Alternatively, you can directly create the released product.</span></span>

## <a name="when-i-release-a-variant-in-another-company-i-receive-the-following-error-message-product-variant-with-specified-dimensions-has-already-been-created"></a><span data-ttu-id="245d1-188">เมื่อฉันนำออกใช้ผลิตภัณฑ์ย่อยในบริษัทอื่น ฉันจะได้รับข้อความแสดงข้อผิดพลาดต่อไปนี้: "ผลิตภัณฑ์ย่อยที่มีมิติที่ระบุถูกสร้างขึ้นแล้ว"</span><span class="sxs-lookup"><span data-stu-id="245d1-188">When I release a variant in another company, I receive the following error message: "Product variant with specified dimensions has already been created."</span></span>

### <a name="issue-description"></a><span data-ttu-id="245d1-189">คำอธิบายปัญหา</span><span class="sxs-lookup"><span data-stu-id="245d1-189">Issue description</span></span>

<span data-ttu-id="245d1-190">ถ้าผลิตภัณฑ์ย่อยถูกนำออกใช้แล้วในบริษัท A และคุณพยายามนำออกใช้ในบริษัท B โดยใช้ปุ่ม **สร้าง** บนหน้า **ผลิตภัณฑ์ย่อยที่นำออกใช้** คุณจะได้รับข้อความแสดงข้อผิดพลาดต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="245d1-190">If a product variant has already been released in a company A, and you try to release it in company B by using the **New** button on the **Released product variants** page, you will receive the following error message:</span></span>

> <span data-ttu-id="245d1-191">สร้างผลิตภัณฑ์ย่อยที่มีมิติที่ระบุแล้ว</span><span class="sxs-lookup"><span data-stu-id="245d1-191">Product variant with specified dimensions has already been created.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="245d1-192">การแก้ไขปัญหา</span><span class="sxs-lookup"><span data-stu-id="245d1-192">Issue resolution</span></span>

<span data-ttu-id="245d1-193">ปุ่ม **สร้าง** บนหน้า **ผลิตภัณฑ์ย่อยที่นำออกใช้** สร้างผลิตภัณฑ์ย่อยและนำออกใช้ในบริบทของบริษัท</span><span class="sxs-lookup"><span data-stu-id="245d1-193">The **New** button on the **Released product variants** page creates the variant and releases it in the company context.</span></span> <span data-ttu-id="245d1-194">ถ้ามีการสร้างผลิตภัณฑ์ย่อยนี้แล้ว คุณจะไม่สามารถใช้ปุ่ม **สร้าง** เพื่อนำออกใช้ในบริษัทอื่นได้</span><span class="sxs-lookup"><span data-stu-id="245d1-194">If the variant has already been created, you can't use the **New** button to release it in another company.</span></span>

<span data-ttu-id="245d1-195">เมื่อต้องการแก้ไขปัญหานี้ ให้เปิดหน้า **ผลิตภัณฑ์หลัก** แล้วเลือก **นำออกใช้ผลิตภัณฑ์** เพื่อปล่อยผลิตภัณฑ์ย่อยที่มีอยู่ในบริษัทที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="245d1-195">To fix the issue, open the **Product master** page, and select **Release product** to release the existing variant in the desired company.</span></span>
