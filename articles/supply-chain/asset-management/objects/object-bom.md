---
title: BOM สินทรัพย์
description: หัวข้อนี้อธิบายสูตรการผลิตสินทรัพย์ (BOMs) ในการจัดการสินทรัพย์
author: josaw1
manager: tfehr
ms.date: 06/26/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CatProcureCatalogEdit, CatProcureCatalogListPage
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 2214
ms.assetid: 2f3e0441-414d-402b-b28b-7ab0d650d658
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 32bb95445a31c1de949c6aa1821bf84d42198acb
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 04/02/2020
ms.locfileid: "3214814"
---
# <a name="asset-boms"></a><span data-ttu-id="9fd92-103">BOM สินทรัพย์</span><span class="sxs-lookup"><span data-stu-id="9fd92-103">Asset BOMs</span></span>

[!include [banner](../../includes/banner.md)]

 

<span data-ttu-id="9fd92-104">หัวข้อนี้อธิบายสูตรการผลิตสินทรัพย์ (BOMs) ในการจัดการสินทรัพย์</span><span class="sxs-lookup"><span data-stu-id="9fd92-104">This topic describes asset bills of materials (BOMs) in Asset Management.</span></span> <span data-ttu-id="9fd92-105">หน้า **BOM สินทรัพย์** แสดงรายการของสินค้าทั้งหมด (อะไหล่และสินค้าอื่นๆ) ที่ใช้ในสินทรัพย์ในระหว่างอายุงานทั้งหมด</span><span class="sxs-lookup"><span data-stu-id="9fd92-105">The **Asset BOM** page shows a list of all items (spare parts and other items) that are used on an asset during its whole lifetime.</span></span> <span data-ttu-id="9fd92-106">เมื่อคุณสร้างสินทรัพย์ใหม่ คุณควรพิจารณาการตั้งค่า BOM สินทรัพย์เป็นส่วนหนึ่งของกระบวนงานการตั้งค่า</span><span class="sxs-lookup"><span data-stu-id="9fd92-106">When you create a new asset, you should consider setting up an asset BOM as a part of the setup procedure.</span></span> <span data-ttu-id="9fd92-107">ด้วยวิธีนี้ คุณสามารถติดตามประวัติสินค้าสำหรับสินทรัพย์จากวันที่สร้าง</span><span class="sxs-lookup"><span data-stu-id="9fd92-107">In this way, you can track item history for the asset from the creation date.</span></span>

<span data-ttu-id="9fd92-108">หลังจากที่คุณได้ทำงานการบำรุงรักษาเสร็จสมบูรณ์แล้ว และมีการลงทะเบียนปริมาณการใช้สินค้าในใบสั่งงานแล้ว คุณสามารถติดตามปริมาณการใช้อะไหล่และสินค้าอื่นที่ใช้ในสินทรัพย์</span><span class="sxs-lookup"><span data-stu-id="9fd92-108">After you've completed a maintenance job, and item consumption has been registered on a work order, you can track consumption of spare parts and other items that are used on the asset.</span></span> <span data-ttu-id="9fd92-109">ฟังก์ชันนี้ช่วยให้คุณสามารถเก็บเรกคอร์ดการใช้สินค้าที่สมบูรณ์สำหรับสินทรัพย์ทั้งหมดของคุณ</span><span class="sxs-lookup"><span data-stu-id="9fd92-109">This functionality lets you keep a complete item consumption record for all your assets.</span></span> <span data-ttu-id="9fd92-110">ตัวอย่างเช่น คุณสามารถใช้เรกคอร์ดเพื่อตรวจสอบว่าอะไหล่สำรองเฉพาะมักจะถูกแทนที่ หรือเพื่อติดตามอะไหล่สำรองหรือสินค้าอื่นๆ ที่ถูกใช้ในปัจจุบันในสินทรัพย์</span><span class="sxs-lookup"><span data-stu-id="9fd92-110">For example, you can use the record to monitor whether a specific spare part is often replaced, or to keep track of the spare parts or other items that are currently used on an asset.</span></span>

> [!NOTE]
> <span data-ttu-id="9fd92-111">ในใบสั่งงาน การใช้สินค้าอาจรวมถึงทั้งอะไหล่สำรองและอื่นๆ สินค้าเพิ่มเติม เช่น น้ำมันหล่อลื่น สลักเกลียว และปะเก็น</span><span class="sxs-lookup"><span data-stu-id="9fd92-111">On a work order, item consumption might include both spare parts and other, additional items, such as lubricants, bolts, and gaskets.</span></span>

<span data-ttu-id="9fd92-112">BOM สินทรัพย์สามารถปรับปรุงได้โดยอัตโนมัติตามการตั้งค่าในการจัดการสินทรัพย์</span><span class="sxs-lookup"><span data-stu-id="9fd92-112">An asset BOM can be automatically updated based on the setup in Asset Management.</span></span> <span data-ttu-id="9fd92-113">ถ้ามีการสร้างสถานะของวงจรการใช้ของใบสั่งงานเพื่อจัดการใบสั่งงานที่เสร็จสมบูรณ์หรือที่เสร็จสิ้น และถ้ามีการตั้งค่าตัวเลือก **ปรับปรุง BOM สินทรัพย์** สำหรับสถานะของวงจรการใช้ของใบสั่งงานนั้นเป็น **ใช่** ในหน้า **สถานะของวงจรการใช้ของใบสั่งงาน** สินค้าทั้งหมดที่ใช้ในใบสั่งงานจะถูกปรับปรุงโดยอัตโนมัติบนหน้า **BOM สินทรัพย์** เมื่อใบสั่งงานถูกปรับปรุงเป็นสถานะของวงจรการใช้นั้น</span><span class="sxs-lookup"><span data-stu-id="9fd92-113">If a work order lifecycle state has been created to handle finished or completed work orders, and if the **Update asset BOM** option for that work order lifecycle state is set to **Yes** on the **Work order lifecycle states** page, all items that are used on the work order will be automatically updated on the **Asset BOM** page when the work order is updated to that lifecycle state.</span></span> 


<span data-ttu-id="9fd92-114">นอกจากนี้ คุณยังสามารถปรับปรุง BOM สินทรัพย์ด้วยตนเองได้ด้วยการสร้างรายการสินค้าในหน้า **BOM สินทรัพย์**</span><span class="sxs-lookup"><span data-stu-id="9fd92-114">You can also manually update an asset BOM by creating new item lines on the **Asset BOM** page.</span></span>

<span data-ttu-id="9fd92-115">บนหน้า **BOM สินทรัพย์** คุณสามารถติดตามประวัติชิ้นส่วนอะไหล่สำหรับสินทรัพย์ หลังจากที่มีการลงทะเบียนปริมาณการใช้สินค้าในใบสั่งงาน</span><span class="sxs-lookup"><span data-stu-id="9fd92-115">On the **Asset BOM** page, you can track spare parts history for assets after item consumption is registered on a work order.</span></span> <span data-ttu-id="9fd92-116">เมื่อต้องการใช้ฟังก์ชันนี้ คุณต้องเลือกกลุ่มสินค้าที่ควรจะใช้สำหรับการลงทะเบียนชิ้นส่วนในหน้า **กลุ่มสินค้าสำรอง**</span><span class="sxs-lookup"><span data-stu-id="9fd92-116">To use this functionality, you must select the item groups that should be used for spare parts registration on the **Spare parts item groups** page.</span></span>

<span data-ttu-id="9fd92-117">ในการใช้ฟังก์ชัน BOM สินทรัพย์ อันดับแรก คุณต้องตั้งค่ากลุ่มสินค้าสำรองที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="9fd92-117">To use asset BOM functionality, you must first set up the required spare parts items groups.</span></span> <span data-ttu-id="9fd92-118">จากนั้น ถ้าคุณต้องการให้ BOM สินทรัพย์ถูกปรับปรุงโดยอัตโนมัติ เมื่อใบสั่งงานเสร็จสมบูรณ์ คุณสามารถตั้งค่าสถานะของวงจรการใช้ของใบสั่งงานให้จัดการการปรับปรุงนั้นได้</span><span class="sxs-lookup"><span data-stu-id="9fd92-118">Then, if you want the asset BOM to be automatically updated when a work order is completed, you can set up a work order lifecycle state to handle that update.</span></span> 


## <a name="set-up-spare-parts-item-groups"></a><span data-ttu-id="9fd92-119">ตั้งค่ากลุ่มสินค้าสำรอง</span><span class="sxs-lookup"><span data-stu-id="9fd92-119">Set up spare parts item groups</span></span>

<span data-ttu-id="9fd92-120">การตั้งค่าของประวัติชิ้นส่วนอะไหล่จะขึ้นอยู่กับกลุ่มสินค้าที่สร้างขึ้นในโมดูล **การบริหารสินค้าคงคลังและคลังสินค้า**</span><span class="sxs-lookup"><span data-stu-id="9fd92-120">The setup of spare parts history is based on item groups that are created in the **Inventory and warehouse management** module.</span></span> <span data-ttu-id="9fd92-121">ในการจัดการสินทรัพย์ คุณตั้งค่ากลุ่มสินค้าเพื่อให้คุณสามารถติดตามประวัติชิ้นส่วนอะไหล่สำหรับสินค้าในกลุ่มสินค้าที่เลือก</span><span class="sxs-lookup"><span data-stu-id="9fd92-121">In Asset Management, you set up item groups so that you can track spare parts history for the items in the selected item groups.</span></span>

1. <span data-ttu-id="9fd92-122">เลือก **การจัดการสินทรัพย์** \> **การตั้งค่า** \> **สินทรัพย์** \> **กลุ่มสินค้าสำรอง**</span><span class="sxs-lookup"><span data-stu-id="9fd92-122">Select **Asset management** \> **Setup** \> **Asset** \> **Spare parts item groups**.</span></span>
2. <span data-ttu-id="9fd92-123">เลือก **สร้าง** เพื่อตั้งค่ากลุ่มสินค้า</span><span class="sxs-lookup"><span data-stu-id="9fd92-123">Select **New** to set up an item group.</span></span>
3. <span data-ttu-id="9fd92-124">ในฟิลด์ **กลุ่มสินค้า** ให้เลือกกลุ่ม</span><span class="sxs-lookup"><span data-stu-id="9fd92-124">In the **Item group** field, select the group.</span></span> <span data-ttu-id="9fd92-125">ชื่อของกลุ่มจะถูกป้อนลงในฟิลด์ **ชื่อ** โดยอัตโนมัติ</span><span class="sxs-lookup"><span data-stu-id="9fd92-125">The name of the group is automatically entered in the **Name** field.</span></span>

## <a name="view-and-update-asset-boms"></a><span data-ttu-id="9fd92-126">ดูและปรับปรุง BOM สินทรัพย์</span><span class="sxs-lookup"><span data-stu-id="9fd92-126">View and update asset BOMs</span></span>

<span data-ttu-id="9fd92-127">หลังจากที่คุณลงรายการบัญชีการใช้สินค้าในใบสั่งงาน คุณสามารถดูการใช้สินค้าที่ลงทะเบียนแล้วในหน้า **BOM สินทรัพย์**</span><span class="sxs-lookup"><span data-stu-id="9fd92-127">After you post item consumption on a work order, you can view the registered item consumption on the **Asset BOM** page.</span></span>

1. <span data-ttu-id="9fd92-128">เลือก **การจัดการสินทรัพย์** \> **ทั่วไป** \> **สินทรัพย์** \> **สินทรัพย์ที่ใช้งานอยู่**</span><span class="sxs-lookup"><span data-stu-id="9fd92-128">Select **Asset management** \> **Common** \> **Assets** \> **Active assets**.</span></span> <span data-ttu-id="9fd92-129">เลือกสินทรัพย์ในรายการ แล้วจากนั้น เลือก **BOM สินทรัพย์**</span><span class="sxs-lookup"><span data-stu-id="9fd92-129">Select the asset in the list, and then select **Asset BOM**.</span></span>

    > [!NOTE]
    > <span data-ttu-id="9fd92-130">เมื่อต้องการดูการลงทะเบียนปริมาณการใช้สินค้าในสินทรัพย์ทั้งหมด เลือก **การจัดการสินทรัพย์** \> **การสอบถาม** \> **สินทรัพย์** \> **BOM สินทรัพย์**</span><span class="sxs-lookup"><span data-stu-id="9fd92-130">To view all item consumption registrations on all assets, select **Asset management** \> **Inquiries** \> **Assets** \> **Asset BOM**.</span></span>

2. <span data-ttu-id="9fd92-131">เลือก **ปรับปรุง BOM สินทรัพย์**</span><span class="sxs-lookup"><span data-stu-id="9fd92-131">Select **Update asset BOM**.</span></span> <span data-ttu-id="9fd92-132">คุณสามารถเพิ่มสินทรัพย์ ชนิดสินทรัพย์ และทรัพยากร ไปยังการปรับปรุงได้ตามที่คุณต้องการโดยการเลือก **เลือก**</span><span class="sxs-lookup"><span data-stu-id="9fd92-132">You can add assets, asset types, and resources to the update as you require by selecting **Select**.</span></span> <span data-ttu-id="9fd92-133">เลือก **ตกลง** เพื่อเริ่มต้นการปรับปรุง</span><span class="sxs-lookup"><span data-stu-id="9fd92-133">Select **OK** to start the update.</span></span> <span data-ttu-id="9fd92-134">นอกจากนี้ คุณยังสามารถตั้งค่าฟังก์ชันปรับปรุงเป็นชุดงานได้</span><span class="sxs-lookup"><span data-stu-id="9fd92-134">You can also set up the Update function as a batch job.</span></span>
3. <span data-ttu-id="9fd92-135">ถ้าคุณต้องการดูข้อมูลเพิ่มเติมที่เกี่ยวข้องกับสินค้า คุณสามารถเพิ่มมิติสินค้าคงคลังได้</span><span class="sxs-lookup"><span data-stu-id="9fd92-135">If you want to see more information that is related to the items, you can add inventory dimensions.</span></span> <span data-ttu-id="9fd92-136">เลือก **สินค้าคงคลัง** \> **การแสดงมิติ** และจากนั้น เลือกกล่องกาเครื่องหมายสำหรับมิติที่คุณต้องการดู</span><span class="sxs-lookup"><span data-stu-id="9fd92-136">Select **Inventory** \> **Dimensions display**, and then select the check boxes for the dimensions that you want to see.</span></span> <span data-ttu-id="9fd92-137">เมื่อต้องการเก็บการตั้งค่านี้สำหรับสินทรัพย์ทั้งหมดในหน้า **BOM สินทรัพย์** ตั้งค่าตัวเลือก **บันทึกการตั้งค่า** เป็น **ใช่**</span><span class="sxs-lookup"><span data-stu-id="9fd92-137">To keep this setup for all assets on the **Asset BOM** page, set the **Save setup** option to **Yes**.</span></span>
4. <span data-ttu-id="9fd92-138">เมื่อต้องการดูภาพรวมของตำแหน่งในการจัดการสินทรัพย์ที่สินค้าในรายการที่เลือกถูกใช้ โดยสัมพันธ์กับสินทรัพย์ ค่าเริ่มต้นของชนิดงาน อะไหล่ และใบสั่งงาน เลือก **สินค้าที่ใช้**</span><span class="sxs-lookup"><span data-stu-id="9fd92-138">To get an overview of where in Asset Management the item on the selected line is used, in relation to assets, job type defaults, spare parts, and work orders, select **Item where used**.</span></span> 
5. <span data-ttu-id="9fd92-139">ถ้าคุณต้องการดูเฉพาะรายการสินค้าที่ใช้งานอยู่ เลือก **มุมมอง** \> **ปัจจุบัน**</span><span class="sxs-lookup"><span data-stu-id="9fd92-139">If you want to see only active item lines, select **View** \> **Current**.</span></span> <span data-ttu-id="9fd92-140">ถ้าต้องการดูรายการสินค้าทั้งหมด ซึ่งรวมทั้งรายการที่มีวันหมดอายุก่อนหน้าวันที่ปัจจุบัน ให้เลือก **มุมมอง** \> **ทั้งหมด**</span><span class="sxs-lookup"><span data-stu-id="9fd92-140">To see all item lines, including lines where the expiration date is earlier than the current date, select **View** \> **All**.</span></span>

> [!NOTE]
> <span data-ttu-id="9fd92-141">เมื่อคุณดำเนินการใบสั่งงานเสร็จสมบูรณ์แล้ว ถ้าสินค้าบางรายการหรืออะไหล่ที่เกี่ยวข้องกับสินทรัพย์ที่เกี่ยวข้องหมดอายุแล้วหรือถูกแทนที่ด้วยสินค้าอื่นหรืออะไหล่สำรอง เราขอแนะนำให้คุณปรับปรุง BOM สินทรัพย์ให้สอดคล้องกัน</span><span class="sxs-lookup"><span data-stu-id="9fd92-141">When you've completed a work order, if some items or spare parts that are related to the related asset have expired or have been replaced by other items or spare parts, we recommend that you update the asset BOM accordingly.</span></span>

## <a name="create-a-new-item-line-in-an-asset-bom"></a><span data-ttu-id="9fd92-142">การสร้างรายการสินค้าใหม่ใน BOM สินทรัพย์</span><span class="sxs-lookup"><span data-stu-id="9fd92-142">Create a new item line in an asset BOM</span></span>

<span data-ttu-id="9fd92-143">คุณสามารถสร้างรายการสินค้าสำหรับสินทรัพย์ด้วยตนเองได้</span><span class="sxs-lookup"><span data-stu-id="9fd92-143">You can manually create item lines for assets.</span></span>

1. <span data-ttu-id="9fd92-144">ในหน้า **BOM สินทรัพย์** เลือก **สร้าง**</span><span class="sxs-lookup"><span data-stu-id="9fd92-144">On the **Asset BOM** page, select **New**.</span></span>
2. <span data-ttu-id="9fd92-145">ในฟิลด์ **สินทรัพย์** ให้เลือกสินทรัพย์เพื่อเพิ่มรายการสินค้า</span><span class="sxs-lookup"><span data-stu-id="9fd92-145">In the **Asset** field, select the asset to add an item line for.</span></span>
3. <span data-ttu-id="9fd92-146">ในฟิลด์ **หมายเลขรายการ** ให้ป้อนหมายเลขรายการตามลำดับ</span><span class="sxs-lookup"><span data-stu-id="9fd92-146">In the **Line number** field, enter a sequential line number.</span></span>
4. <span data-ttu-id="9fd92-147">ในฟิลด์ **มีผลบังคับใช้** ให้ป้อนวันที่เริ่มต้นสำหรับสินค้า</span><span class="sxs-lookup"><span data-stu-id="9fd92-147">In the **Effective** field, enter a start date for the item.</span></span>
5. <span data-ttu-id="9fd92-148">ถ้าสินค้าจะหมดอายุ ในฟิลด์ **การหมดอายุ** ให้ป้อนวันที่สิ้นสุด</span><span class="sxs-lookup"><span data-stu-id="9fd92-148">If the item will expire, in the **Expiration** field, enter an end date.</span></span>
6. <span data-ttu-id="9fd92-149">ในฟิลด์ **หมายเลขสินค้า** เลือกสินค้า</span><span class="sxs-lookup"><span data-stu-id="9fd92-149">In the **Item number** field, select the item.</span></span> <span data-ttu-id="9fd92-150">ชื่อของไฟล์ถูกป้อนโดยอัตโนมัติลงในฟิลด์ **ชื่อผลิตภัณฑ์**</span><span class="sxs-lookup"><span data-stu-id="9fd92-150">The name is automatically entered in the **Product name** field.</span></span>
7. <span data-ttu-id="9fd92-151">ในฟิลด์ **ปริมาณ** ป้อนปริมาณที่มีการใช้</span><span class="sxs-lookup"><span data-stu-id="9fd92-151">In the **Quantity** field, enter the quantity that is used.</span></span> <span data-ttu-id="9fd92-152">ฟิลด์ **หน่วย** มีการปรับปรุงโดยอัตโนมัติ</span><span class="sxs-lookup"><span data-stu-id="9fd92-152">The **Unit** field is automatically updated.</span></span>
