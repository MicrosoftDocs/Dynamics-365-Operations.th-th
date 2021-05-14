---
title: สร้างและประมวลผลความไม่สอดคล้องกัน
description: หัวข้อนี้อธิบายวิธีการดำเนินการจัดการความไม่สอดคล้องกัน โดยขึ้นอยู่กับใบสั่งตรวจสอบคุณภาพที่มีอยู่
author: perlynne
ms.date: 03/23/2021
ms.topic: business-process
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 06a56a694f7a80d65cb46d08744e78d8361cee3b
ms.sourcegitcommit: 8362f3bd32ce8b9a5af93c8e57daef732a93b19e
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 04/28/2021
ms.locfileid: "5956217"
---
# <a name="create-and-process-nonconformances"></a><span data-ttu-id="b42c9-103">สร้างและประมวลผลความไม่สอดคล้องกัน</span><span class="sxs-lookup"><span data-stu-id="b42c9-103">Create and process nonconformances</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="b42c9-104">หัวข้อนี้อธิบายวิธีการดำเนินการจัดการความไม่สอดคล้องกัน โดยขึ้นอยู่กับใบสั่งตรวจสอบคุณภาพที่มีอยู่</span><span class="sxs-lookup"><span data-stu-id="b42c9-104">This topic describes how to perform nonconformance management based on an existing quality order.</span></span> <span data-ttu-id="b42c9-105">โดยทั่วไป การจัดการความไม่สอดคล้องกันจะถูกดำเนินการโดยเจ้าหน้าที่ตรวจสอบคุณภาพ</span><span class="sxs-lookup"><span data-stu-id="b42c9-105">Typically, nonconformance management is done by a quality clerk.</span></span> <span data-ttu-id="b42c9-106">คุณต้องมีใบสั่งตรวจสอบคุณภาพที่พร้อมใช้งาน ตามข้อกำหนดเบื้องต้น</span><span class="sxs-lookup"><span data-stu-id="b42c9-106">As a prerequisite, you must have a quality order available.</span></span> <span data-ttu-id="b42c9-107">(สำหรับข้อมูลเกี่ยวกับวิธีการสร้างใบสั่งตรวจสอบคุณภาพ ดูที่ [ตรวจสอบคุณภาพของสินค้า](inspect-quality-goods.md))</span><span class="sxs-lookup"><span data-stu-id="b42c9-107">(For information about how to create a quality order, see [Inspect the quality of goods](inspect-quality-goods.md).)</span></span>

<span data-ttu-id="b42c9-108">ก่อนที่ผู้ใช้จะสามารถประมวลผลการอนุมัติความไม่สอดคล้องกันได้ ต้องมอบหมายผู้ปฏิบัติงานให้กับผู้ปฏิบัติงานในฟิลด์ **บุคคล** ในหน้า **ผู้ใช้**</span><span class="sxs-lookup"><span data-stu-id="b42c9-108">Before a user can process the approval of a nonconformance, a worker must be assigned to them in the **Person** field on the **Users** page.</span></span> <span data-ttu-id="b42c9-109">นอกจากนี้ ก่อนที่ผู้ใช้สามารถใช้บันทึกเอกสารได้ ต้องตั้งค่าตัวเลือก **เปิดใช้งานการจัดการเอกสาร** เป็น *ใช่* ในตัวเลือกผู้ใช้</span><span class="sxs-lookup"><span data-stu-id="b42c9-109">Additionally, before the user can use the document notes, the **Enable document handling** option must be set to *Yes* in their user options.</span></span>

## <a name="create-a-nonconformance"></a><span data-ttu-id="b42c9-110">สร้างความไม่สอดคล้องกัน</span><span class="sxs-lookup"><span data-stu-id="b42c9-110">Create a nonconformance</span></span>

<span data-ttu-id="b42c9-111">เมื่อต้องการสร้างความไม่สอดคล้องกัน ให้ทำตามขั้นตอนเหล่านี้</span><span class="sxs-lookup"><span data-stu-id="b42c9-111">To create a nonconformance, follow these steps.</span></span>

1. <span data-ttu-id="b42c9-112">ไปที่ **การจัดการสินค้าคงคลัง \> งานประจำงวด \> การจัดการคุณภาพ \> ความไม่สอดคล้องกัน**</span><span class="sxs-lookup"><span data-stu-id="b42c9-112">Go to **Inventory management \> Periodic tasks \> Quality management \> Non conformances**.</span></span>
1. <span data-ttu-id="b42c9-113">บนหน้าต่างการดำเนินการ เลือก **สร้าง**</span><span class="sxs-lookup"><span data-stu-id="b42c9-113">On the Action pane, select **New**.</span></span>
1. <span data-ttu-id="b42c9-114">ในกล่องโต้ตอบ **สร้างความไม่สอดคล้องกัน** ในฟิลด์ **ชนิดของปัญหา** ให้เลือกชนิดของปัญหาที่พบในระหว่างกระบวนการตรวจสอบ</span><span class="sxs-lookup"><span data-stu-id="b42c9-114">In the **Create non conformance** dialog box, in **Problem type** field, select the type of problem that was found during the inspection process.</span></span>
1. <span data-ttu-id="b42c9-115">เลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="b42c9-115">Select **OK**.</span></span>

## <a name="approve-or-reject-a-nonconformance"></a><span data-ttu-id="b42c9-116">อนุมัติหรือปฏิเสธความไม่สอดคล้องกัน</span><span class="sxs-lookup"><span data-stu-id="b42c9-116">Approve or reject a nonconformance</span></span>

<span data-ttu-id="b42c9-117">ในการอนุมัติหรือปฏิเสธความไม่สอดคล้องกัน ทำตามขั้นตอนเหล่านี้</span><span class="sxs-lookup"><span data-stu-id="b42c9-117">To approve or reject a nonconformance, follow these steps.</span></span>

1. <span data-ttu-id="b42c9-118">ไปที่ **การจัดการสินค้าคงคลัง \> งานประจำงวด \> การจัดการคุณภาพ \> ความไม่สอดคล้องกัน**</span><span class="sxs-lookup"><span data-stu-id="b42c9-118">Go to **Inventory management \> Periodic tasks \> Quality management \> Non conformances**.</span></span>
1. <span data-ttu-id="b42c9-119">ในรายการ เลือกความไม่สอดคล้องกันที่คุณต้องการจะอัพเดต</span><span class="sxs-lookup"><span data-stu-id="b42c9-119">In the list, select the nonconformance that you want to update.</span></span>

    > [!NOTE]
    > <span data-ttu-id="b42c9-120">คุณสามารถเพิ่มการแก้ไขไปยังความไม่สอดคล้องกันที่ได้รับอนุมัติได้เท่านั้น</span><span class="sxs-lookup"><span data-stu-id="b42c9-120">You can add a correction only to nonconformances that are approved.</span></span>

1. <span data-ttu-id="b42c9-121">ในบานหน้าต่างการดำเนินการ เลือก **ฟังก์ชัน \> อนุมัติความไม่สอดคล้องกัน** เพื่ออนุมัติความไม่สอดคล้องกันหรือ **ฟังก์ชัน \> ปฏิเสธความไม่สอดคล้องกัน** เพื่อปฏิเสธ</span><span class="sxs-lookup"><span data-stu-id="b42c9-121">On the Action Pane, select **Functions \> Approve non conformance** to approve the nonconformance or **Functions \> Refuse non conformance** to reject it.</span></span> <span data-ttu-id="b42c9-122">คุณสามารถเชื่อมโยงความไม่สอดคล้องกันที่อนุมัติแล้วกับ [การดําเนินงานที่เกี่ยวข้อง](../quality-operations.md)</span><span class="sxs-lookup"><span data-stu-id="b42c9-122">You can associate approved nonconformances with [related operations](../quality-operations.md).</span></span> <span data-ttu-id="b42c9-123">ด้วยวิธีนี้ คุณสามารถบันทึกงานที่ได้เสร็จสิ้นเป็นส่วนหนึ่งของการจัดการความไม่สอดคล้องกันและการประมวลผลการจัดการการแก้ไข</span><span class="sxs-lookup"><span data-stu-id="b42c9-123">In this way, you can record work that is done as part of the nonconformance handling and the processing of correction handling.</span></span>
1. <span data-ttu-id="b42c9-124">คุณได้รับพร้อมต์เพื่อยืนยันการเลือกของคุณ</span><span class="sxs-lookup"><span data-stu-id="b42c9-124">You're prompted to confirm your selection.</span></span> <span data-ttu-id="b42c9-125">เลือก **ใช่** เพื่อดำเนินการต่อ</span><span class="sxs-lookup"><span data-stu-id="b42c9-125">Select **Yes** to continue.</span></span>

## <a name="add-operations-and-other-details-to-nonconformances"></a><span data-ttu-id="b42c9-126">เพิ่มการดําเนินงานและรายละเอียดอื่นๆ ให้กับความไม่สอดคล้องกัน</span><span class="sxs-lookup"><span data-stu-id="b42c9-126">Add operations and other details to nonconformances</span></span>

<span data-ttu-id="b42c9-127">หลังจากที่คุณสร้างความไม่สอดคล้องกันแล้ว คุณสามารถเริ่มต้นเพิ่มการดําเนินงานที่เกี่ยวข้องและระบุข้อมูลเพิ่มเติมเกี่ยวกับการดําเนินงานเหล่านั้นได้</span><span class="sxs-lookup"><span data-stu-id="b42c9-127">After you've created a nonconformance, you can start to add related operations and specify additional information about those operations.</span></span> <span data-ttu-id="b42c9-128">คุณสามารถเพิ่มการดําเนินงานที่เกี่ยวข้องไปยังความไม่สอดคล้องกันที่ได้รับอนุมัติได้เท่านั้น</span><span class="sxs-lookup"><span data-stu-id="b42c9-128">You can add related operations only to nonconformances that are approved.</span></span>

<span data-ttu-id="b42c9-129">นอกจากข้อมูลพื้นฐานแล้ว คุณยังสามารถเพิ่มรายละเอียดต่อไปนี้ลงในการดําเนินงานได้:</span><span class="sxs-lookup"><span data-stu-id="b42c9-129">Besides the basic information, you can add the following details to an operation:</span></span>

- <span data-ttu-id="b42c9-130">**สินค้า** – คุณสามารถสร้างรายการสินค้าที่จะใช้ในการดำเนินการแก้ไข</span><span class="sxs-lookup"><span data-stu-id="b42c9-130">**Items** – You can create a list of items that are consumed to perform the correction.</span></span> <span data-ttu-id="b42c9-131">ตัวอย่างเช่น สินค้าอาจเป็นผลิตภัณฑ์ที่ต้องใช้ในการซ่อมแซมอุปกรณ์ หรือส่วนผสมที่ต้องใช้ในการทำผลิตภัณฑ์สำเร็จรูปใหม่อีกครั้ง</span><span class="sxs-lookup"><span data-stu-id="b42c9-131">For example, the items might be products that are required to repair equipment or ingredients that are required to rework a finished product.</span></span>
- <span data-ttu-id="b42c9-132">**ค่าธรรมเนียมคุณภาพ** – คุณสามารถสร้างรายการค่าธรรมเนียมที่เกิดขึ้นหรือถูกเรียกเก็บเงินจากแหล่งที่มาภายนอก</span><span class="sxs-lookup"><span data-stu-id="b42c9-132">**Quality charges** – You can create a list of charges that are incurred or billed out to external sources.</span></span>
- <span data-ttu-id="b42c9-133">**แผ่นเวลา** – คุณสามารถสร้างล็อกเวลาที่ผู้ปฏิบัติงานแต่ละคนใช้ในการดําเนินงาน</span><span class="sxs-lookup"><span data-stu-id="b42c9-133">**Timesheet** – You can create a log of the time that each worker spends on the operation.</span></span>

<span data-ttu-id="b42c9-134">การตั้งค่าที่เหลือไม่จำเป็นต้องระบุ</span><span class="sxs-lookup"><span data-stu-id="b42c9-134">The remaining settings are optional.</span></span> <span data-ttu-id="b42c9-135">ต้นทุนสำหรับสินค้า ค่าธรรมเนียมคุณภาพ และแผ่นเวลาแต่ละรายการ จะถูกบวกรวมและแสดงในการดําเนินงาน</span><span class="sxs-lookup"><span data-stu-id="b42c9-135">The cost for each item, quality charges, and the timesheet are summed and shown on the operation.</span></span> <span data-ttu-id="b42c9-136">คุณไม่สามารถแก้ไขฟิลด์ **ต้นทุน** ในการดําเนินงานได้โดยตรง</span><span class="sxs-lookup"><span data-stu-id="b42c9-136">You can't directly edit the **Cost** field on the operation.</span></span>

### <a name="create-an-operation-for-a-nonconformance"></a><span data-ttu-id="b42c9-137">สร้างการดำเนินงานสำหรับความไม่สอดคล้องกัน</span><span class="sxs-lookup"><span data-stu-id="b42c9-137">Create an operation for a nonconformance</span></span>

<span data-ttu-id="b42c9-138">ในการสร้างการดำเนินงานสำหรับความไม่สอดคล้องกัน ให้ทำตามขั้นตอนเหล่านี้</span><span class="sxs-lookup"><span data-stu-id="b42c9-138">To create an operation for a nonconformance, follow these steps.</span></span>

1. <span data-ttu-id="b42c9-139">ไปที่ **การจัดการสินค้าคงคลัง \> งานประจำงวด \> การจัดการคุณภาพ \> ความไม่สอดคล้องกัน**</span><span class="sxs-lookup"><span data-stu-id="b42c9-139">Go to **Inventory management \> Periodic tasks \> Quality management \> Non conformances**.</span></span>
1. <span data-ttu-id="b42c9-140">ในรายการ เลือกความไม่สอดคล้องกันที่คุณต้องการจะอัพเดต</span><span class="sxs-lookup"><span data-stu-id="b42c9-140">In the list, select the nonconformance that you want to update.</span></span>

    > [!NOTE]
    > <span data-ttu-id="b42c9-141">คุณสามารถเพิ่มหรืออัพเดตการดําเนินงานสำหรับความไม่สอดคล้องกันที่ได้รับอนุมัติได้เท่านั้น</span><span class="sxs-lookup"><span data-stu-id="b42c9-141">You can add or update operations only for nonconformances that are approved.</span></span>

1. <span data-ttu-id="b42c9-142">บนบานหน้าต่างการดำเนินการ เลือก **การดําเนินงานที่เกี่ยวข้อง**</span><span class="sxs-lookup"><span data-stu-id="b42c9-142">On the Action Pane, select **Related operations**.</span></span>
1. <span data-ttu-id="b42c9-143">บนหน้า **การดําเนินงานที่เกี่ยวข้อง** ในบานหน้าต่างการดําเนินงาน ให้เลือก **สร้าง** เพื่อเพิ่มแถวลงในกริด</span><span class="sxs-lookup"><span data-stu-id="b42c9-143">On the **Related operations** page, on the Action pane, select **New** to add a row to the grid.</span></span> <span data-ttu-id="b42c9-144">จากนั้นให้กำหนดฟิลด์ดังต่อไปนี้สำหรับแถวใหม่:</span><span class="sxs-lookup"><span data-stu-id="b42c9-144">Then set the following fields for the new row:</span></span>

    - <span data-ttu-id="b42c9-145">**การดําเนินงาน** – เลือกรหัสของการดําเนินงานที่จะดําเนินการสำหรับความไม่สอดคล้องกัน</span><span class="sxs-lookup"><span data-stu-id="b42c9-145">**Operation** – Select the code of the operation that will be performed for the nonconformance.</span></span>
    - <span data-ttu-id="b42c9-146">**เหตุผล** – ป้อนคำอธิบายโดยละเอียดที่อธิบายเหตุผลที่ต้องมีการดําเนินงาน</span><span class="sxs-lookup"><span data-stu-id="b42c9-146">**Reason** – Enter a detailed description that explains why the operation is required.</span></span>
    - <span data-ttu-id="b42c9-147">**ใบสั่งขาย** – ถ้ารหัสการดําเนินงานที่เลือกเกี่ยวข้องกับชนิดใบสั่งขาย ให้เลือกใบสั่งขายที่คุณเชื่อมโยงการดําเนินงานด้วย</span><span class="sxs-lookup"><span data-stu-id="b42c9-147">**Sales order** – If the selected operation code is related to the sales order type, select the sales order that you're linking the operation to.</span></span>
    - <span data-ttu-id="b42c9-148">**ใบสั่งซื้อ** – ถ้ารหัสการดําเนินงานที่เลือกเกี่ยวข้องกับชนิดใบสั่งซื้อ ให้เลือกใบสั่งซื้อที่คุณเชื่อมโยงการดําเนินงานด้วย</span><span class="sxs-lookup"><span data-stu-id="b42c9-148">**Purchase order** – If the selected operation code is related to the purchase order type, select the purchase order that you're linking the operation to.</span></span>

1. <span data-ttu-id="b42c9-149">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="b42c9-149">Close the pages.</span></span>

### <a name="add-items-to-an-operation"></a><span data-ttu-id="b42c9-150">เพิ่มสินค้าในการดําเนินงาน</span><span class="sxs-lookup"><span data-stu-id="b42c9-150">Add items to an operation</span></span>

<span data-ttu-id="b42c9-151">ในการเพิ่มสินค้าลงในการดําเนินงาน ให้ปฏิบัติตามขั้นตอนต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="b42c9-151">To add items to an operation, follow these steps.</span></span>

1. <span data-ttu-id="b42c9-152">ไปที่ **การจัดการสินค้าคงคลัง \> งานประจำงวด \> การจัดการคุณภาพ \> ความไม่สอดคล้องกัน**</span><span class="sxs-lookup"><span data-stu-id="b42c9-152">Go to **Inventory management \> Periodic tasks \> Quality management \> Non conformances**.</span></span>
1. <span data-ttu-id="b42c9-153">ในรายการ เลือกความไม่สอดคล้องกันที่คุณต้องการจะอัพเดต</span><span class="sxs-lookup"><span data-stu-id="b42c9-153">In the list, select the nonconformance that you want to update.</span></span>

    > [!NOTE]
    > <span data-ttu-id="b42c9-154">คุณสามารถเพิ่มหรืออัพเดตการดําเนินงานสำหรับความไม่สอดคล้องกันที่ได้รับอนุมัติได้เท่านั้น</span><span class="sxs-lookup"><span data-stu-id="b42c9-154">You can add or update operations only for nonconformances that are approved.</span></span>

1. <span data-ttu-id="b42c9-155">บนบานหน้าต่างการดำเนินการ เลือก **การดําเนินงานที่เกี่ยวข้อง**</span><span class="sxs-lookup"><span data-stu-id="b42c9-155">On the Action Pane, select **Related operations**.</span></span>
1. <span data-ttu-id="b42c9-156">บนหน้า **การดําเนินงานที่เกี่ยวข้อง** ให้เลือกการดําเนินงานที่คุณต้องการเพิ่มสินค้าลงไป</span><span class="sxs-lookup"><span data-stu-id="b42c9-156">On the **Related operations** page, select the operation that you want to add items to.</span></span>
1. <span data-ttu-id="b42c9-157">บนบานหน้าต่างการดำเนินการ เลือก **สินค้า**</span><span class="sxs-lookup"><span data-stu-id="b42c9-157">On the Action Pane, select **Items**.</span></span>
1. <span data-ttu-id="b42c9-158">บนหน้า **การดําเนินงานที่เกี่ยวข้อง** ในบานหน้าต่างการดําเนินงาน ให้เลือก **สร้าง** เพื่อเพิ่มแถวลงในกริด</span><span class="sxs-lookup"><span data-stu-id="b42c9-158">On the **Related operations** page, on the Action pane, select **New** to add a row to the grid.</span></span> <span data-ttu-id="b42c9-159">จากนั้น ให้กำหนดฟิลด์ดังต่อไปนี้สำหรับแถวใหม่:</span><span class="sxs-lookup"><span data-stu-id="b42c9-159">Then set the following fields for new row:</span></span>

    - <span data-ttu-id="b42c9-160">**หมายเลขสินค้า** – เลือกผลิตภัณฑ์ที่จะใช้เป็นส่วนหนึ่งของการดําเนินงานที่เลือก</span><span class="sxs-lookup"><span data-stu-id="b42c9-160">**Item number** – Select the product that will be consumed as part of the selected operation.</span></span>
    - <span data-ttu-id="b42c9-161">**ปริมาณ** – ป้อนจํานวนของสินค้าที่จะใช้</span><span class="sxs-lookup"><span data-stu-id="b42c9-161">**Quantity** – Enter the number of items that will be consumed.</span></span>

    > [!NOTE]
    > <span data-ttu-id="b42c9-162">คุณสามารถดูต้นทุนสำหรับสินค้าในฟิลด์ **ต้นทุน** บนแท็บ **ทั่วไป** ต้นทุนที่แสดงที่นั่นจะมาจากต้นทุนที่ตั้งค่าไว้ในหน้า **ผลิตภัณฑ์ที่นำออกใช้**</span><span class="sxs-lookup"><span data-stu-id="b42c9-162">You can view the cost for the item in the **Cost** field on the **General** tab. The cost that is shown there comes from the cost that is set up on the **Released product** page.</span></span> <span data-ttu-id="b42c9-163">ไม่สามารถอัพเดตต้นทุนโดยตรงในหน้า **รายการของการดําเนินงานที่เกี่ยวข้อง**</span><span class="sxs-lookup"><span data-stu-id="b42c9-163">The cost can't be updated directly on the **Related operation item** page.</span></span> <span data-ttu-id="b42c9-164">ต้นทุนของสินค้าทั้งหมดที่เพิ่มในหน้า **รายการของการดําเนินงานที่เกี่ยวข้อง** จะถูกเพิ่มโดยอัตโนมัติในฟิลด์ **ต้นทุน** บนหน้า **การดําเนินงานที่เกี่ยวข้อง**</span><span class="sxs-lookup"><span data-stu-id="b42c9-164">The cost of all items that are added on the **Related operation items** page is automatically added to the **Cost** field on the **Related operations** page.</span></span>

1. <span data-ttu-id="b42c9-165">ทําซ้ำขั้นตอนก่อนหน้านี้สำหรับสินค้าเพิ่มเติมแต่ละรายการที่คุณต้องเพิ่ม</span><span class="sxs-lookup"><span data-stu-id="b42c9-165">Repeat the previous step for each additional item that you must add.</span></span>
1. <span data-ttu-id="b42c9-166">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="b42c9-166">Close the pages.</span></span>

### <a name="add-quality-charges-to-an-operation"></a><span data-ttu-id="b42c9-167">เพิ่มค่าธรรมเนียมคุณภาพในการดําเนินงาน</span><span class="sxs-lookup"><span data-stu-id="b42c9-167">Add quality charges to an operation</span></span>

<span data-ttu-id="b42c9-168">ในการเพิ่มค่าธรรมเนียมคุณภาพลงในการดําเนินงาน ให้ปฏิบัติตามขั้นตอนต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="b42c9-168">To add quality charges to an operation, follow these steps.</span></span>

1. <span data-ttu-id="b42c9-169">ไปที่ **การจัดการสินค้าคงคลัง \> งานประจำงวด \> การจัดการคุณภาพ \> ความไม่สอดคล้องกัน**</span><span class="sxs-lookup"><span data-stu-id="b42c9-169">Go to **Inventory management \> Periodic tasks \> Quality management \> Non conformances**.</span></span>
1. <span data-ttu-id="b42c9-170">ในรายการ เลือกความไม่สอดคล้องกันที่คุณต้องการจะอัพเดต</span><span class="sxs-lookup"><span data-stu-id="b42c9-170">In the list, select the nonconformance that you want to update.</span></span>

    > [!NOTE]
    > <span data-ttu-id="b42c9-171">คุณสามารถเพิ่มหรืออัพเดตการดําเนินงานสำหรับความไม่สอดคล้องกันที่ได้รับอนุมัติได้เท่านั้น</span><span class="sxs-lookup"><span data-stu-id="b42c9-171">You can add or update operations only for nonconformances that are approved.</span></span>

1. <span data-ttu-id="b42c9-172">บนบานหน้าต่างการดำเนินการ เลือก **การดําเนินงานที่เกี่ยวข้อง**</span><span class="sxs-lookup"><span data-stu-id="b42c9-172">On the Action Pane, select **Related operations**.</span></span>
1. <span data-ttu-id="b42c9-173">บนหน้า **การดําเนินงานที่เกี่ยวข้อง** ให้เลือกการดําเนินงานที่คุณต้องการเพิ่มค่าธรรมเนียมคุณภาพลงไป</span><span class="sxs-lookup"><span data-stu-id="b42c9-173">On the **Related operations** page, select the operation that you want to add quality charges to.</span></span>
1. <span data-ttu-id="b42c9-174">บนบานหน้าต่างการดำเนินการ เลือก **ค่าธรรมเนียมคุณภาพ**</span><span class="sxs-lookup"><span data-stu-id="b42c9-174">On the Action Pane, select **Quality charges**.</span></span>
1. <span data-ttu-id="b42c9-175">บนหน้า **ค่าธรรมเนียมของการดําเนินงานที่เกี่ยวข้อง** ในบานหน้าต่างการดําเนินงาน ให้เลือก **สร้าง** เพื่อเพิ่มแถวลงในกริด</span><span class="sxs-lookup"><span data-stu-id="b42c9-175">On the **Related operation charges** page, on the Action pane, select **New** to add a row to the grid.</span></span> <span data-ttu-id="b42c9-176">จากนั้นให้กำหนดฟิลด์ดังต่อไปนี้สำหรับแถวใหม่:</span><span class="sxs-lookup"><span data-stu-id="b42c9-176">Then set the following fields for the new row:</span></span>

    - <span data-ttu-id="b42c9-177">**รหัสค่าธรรมเนียม** – เลือกค่าธรรมเนียมคุณภาพที่คุณต้องการเพิ่ม</span><span class="sxs-lookup"><span data-stu-id="b42c9-177">**Charges code** – Select the quality charge that you want to add.</span></span>
    - <span data-ttu-id="b42c9-178">**คำอธิบาย** – ป้อนคำอธิบายโดยละเอียดของค่าธรรมเนียม</span><span class="sxs-lookup"><span data-stu-id="b42c9-178">**Description** – Enter a detailed description of the charge.</span></span>
    - <span data-ttu-id="b42c9-179">**มูลค่าของค่าธรรมเนียม** – ป้อนยอดเงินของค่าธรรมเนียม</span><span class="sxs-lookup"><span data-stu-id="b42c9-179">**Charges value** – Enter the amount of the charge.</span></span>

1. <span data-ttu-id="b42c9-180">ทําซ้ำขั้นตอนก่อนหน้านี้สำหรับค่าธรรมเนียมเพิ่มเติมแต่ละรายการที่คุณต้องเพิ่ม</span><span class="sxs-lookup"><span data-stu-id="b42c9-180">Repeat the previous step for each additional charge that you must add.</span></span>
1. <span data-ttu-id="b42c9-181">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="b42c9-181">Close the pages.</span></span>

> [!NOTE]
> <span data-ttu-id="b42c9-182">จํานวนเงินในฟิลด์ **มูลค่าค่าธรรมเนียม** จะถูกบวกรวมโดยอัตโนมัติสำหรับค่าธรรมเนียมคุณภาพทั้งหมด และถูกเพิ่มในยอดเงินอื่นๆ ในฟิลด์ **ต้นทุน** ในหน้า **การดําเนินงานที่เกี่ยวข้อง**</span><span class="sxs-lookup"><span data-stu-id="b42c9-182">The amount in the **Charges value** field is automatically summed for all quality charges and added to any other amounts in the **Cost** field on the **Related operations** page.</span></span>

### <a name="create-a-timesheet-on-an-operation"></a><span data-ttu-id="b42c9-183">สร้างแผ่นเวลาในการดําเนินงาน</span><span class="sxs-lookup"><span data-stu-id="b42c9-183">Create a timesheet on an operation</span></span>

<span data-ttu-id="b42c9-184">ในการเพิ่มแผ่นเวลาลงในการดําเนินงาน ให้ปฏิบัติตามขั้นตอนต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="b42c9-184">To add a timesheet to an operation, follow these steps.</span></span>

1. <span data-ttu-id="b42c9-185">ไปที่ **การจัดการสินค้าคงคลัง \> งานประจำงวด \> การจัดการคุณภาพ \> ความไม่สอดคล้องกัน**</span><span class="sxs-lookup"><span data-stu-id="b42c9-185">Go to **Inventory management \> Periodic tasks \> Quality management \> Non conformances**.</span></span>
1. <span data-ttu-id="b42c9-186">ในรายการ เลือกความไม่สอดคล้องกันที่คุณต้องการจะอัพเดต</span><span class="sxs-lookup"><span data-stu-id="b42c9-186">In the list, select the nonconformance that you want to update.</span></span>

    > [!NOTE]
    > <span data-ttu-id="b42c9-187">คุณสามารถเพิ่มหรืออัพเดตการดําเนินงานสำหรับความไม่สอดคล้องกันที่ได้รับอนุมัติได้เท่านั้น</span><span class="sxs-lookup"><span data-stu-id="b42c9-187">You can add or update operations only for nonconformances that are approved.</span></span>

1. <span data-ttu-id="b42c9-188">บนบานหน้าต่างการดำเนินการ เลือก **การดําเนินงานที่เกี่ยวข้อง**</span><span class="sxs-lookup"><span data-stu-id="b42c9-188">On the Action Pane, select **Related operations**.</span></span>
1. <span data-ttu-id="b42c9-189">บนหน้า **การดําเนินงานที่เกี่ยวข้อง** ให้เลือกการดําเนินงานที่คุณต้องการเพิ่มแผ่นเวลาลงไป</span><span class="sxs-lookup"><span data-stu-id="b42c9-189">On the **Related operations** page, select the operation that you want to add a timesheet to.</span></span>
1. <span data-ttu-id="b42c9-190">บนบานหน้าต่างการดำเนินการ เลือก **แผ่นเวลา**</span><span class="sxs-lookup"><span data-stu-id="b42c9-190">On the Action Pane, select **Timesheet**.</span></span>
1. <span data-ttu-id="b42c9-191">บนหน้า **แผ่นเวลาของการดําเนินงานที่เกี่ยวข้อง** ในบานหน้าต่างการดําเนินงาน ให้เลือก **สร้าง** เพื่อเพิ่มแถวลงในกริด</span><span class="sxs-lookup"><span data-stu-id="b42c9-191">On the **Related operation time sheets** page, on the Action pane, select **New** to add a row to the grid.</span></span> <span data-ttu-id="b42c9-192">จากนั้นให้กำหนดฟิลด์ดังต่อไปนี้สำหรับแถวใหม่:</span><span class="sxs-lookup"><span data-stu-id="b42c9-192">Then set the following fields for the new row:</span></span>

    - <span data-ttu-id="b42c9-193">**วันที่** – ระบุวันที่เมื่องานเสร็จสิ้น</span><span class="sxs-lookup"><span data-stu-id="b42c9-193">**Date** – Specify the date when work was done.</span></span> <span data-ttu-id="b42c9-194">โดยค่าเริ่มต้น ฟิลด์นี้ถูกตั้งค่าเป็นวันที่ปัจจุบัน</span><span class="sxs-lookup"><span data-stu-id="b42c9-194">By default, this field is set to the current date.</span></span>
    - <span data-ttu-id="b42c9-195">**ผู้ปฏิบัติงาน** – เลือกผู้ปฏิบัติงานที่ทำงาน</span><span class="sxs-lookup"><span data-stu-id="b42c9-195">**Worker** – Select the worker who did the work.</span></span> <span data-ttu-id="b42c9-196">โดยค่าเริ่มต้น ฟิลด์นี้จะถูกตั้งค่าเป็นผู้ปฏิบัติงานที่ได้รับมอบหมายให้กับผู้ใช้ปัจจุบัน</span><span class="sxs-lookup"><span data-stu-id="b42c9-196">By default, this field is set to the worker that is assigned to the current user.</span></span>
    - <span data-ttu-id="b42c9-197">**ชั่วโมงการดําเนินงาน** – ป้อนจํานวนชั่วโมงที่มีการปฏิบัติงานในการดําเนินงานที่เลือก</span><span class="sxs-lookup"><span data-stu-id="b42c9-197">**Operation hours** – Enter the number of hours that were worked on the selected operation.</span></span>
    - <span data-ttu-id="b42c9-198">**ออกใบแจ้งหนี้แล้ว** – เลือกกล่องกาเครื่องหมายนี้ ถ้ามีการคิดค่าธรรมเนียมเวลากับลูกค้าหรือผู้จัดจำหน่ายบนใบแจ้งหนี้</span><span class="sxs-lookup"><span data-stu-id="b42c9-198">**Invoiced** – Select this check box if the time has been charged to a customer or vendor on an invoice.</span></span>

    > [!NOTE]
    > <span data-ttu-id="b42c9-199">คุณสามารถดูต้นทุนในฟิลด์ **ต้นทุน** บนแท็บ **ทั่วไป** ต้นทุนจะถูกคํานวณโดยใช้อัตราที่คุณกําหนดในหน้า **พารามิเตอร์การบริหารสินค้าคงคลัง**</span><span class="sxs-lookup"><span data-stu-id="b42c9-199">You can view the cost in the **Cost** field on the **General** tab. The cost is calculated by using the rate that you define on the **Inventory management parameters** page.</span></span>

1. <span data-ttu-id="b42c9-200">ทําซ้ำขั้นตอนก่อนหน้านี้สำหรับรายการแผ่นเวลาเพิ่มเติมแต่ละรายการที่คุณต้องเพิ่ม</span><span class="sxs-lookup"><span data-stu-id="b42c9-200">Repeat the previous step for each additional timesheet line that you must add.</span></span>
1. <span data-ttu-id="b42c9-201">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="b42c9-201">Close the pages.</span></span>

> [!NOTE]
> <span data-ttu-id="b42c9-202">จํานวนเงินในฟิลด์ **ต้นทุน** จะถูกบวกรวมสำหรับรายการแผ่นเวลาทั้งหมด และถูกเพิ่มในยอดเงินอื่นๆ ในฟิลด์ **ต้นทุน** ในหน้า **การดําเนินงานที่เกี่ยวข้อง**</span><span class="sxs-lookup"><span data-stu-id="b42c9-202">The amount in the **Cost** field is summed for all timesheet lines and added to any other amounts in the **Cost** field on the **Related operations** page.</span></span>

## <a name="add-a-correction-to-a-nonconformance"></a><span data-ttu-id="b42c9-203">เพิ่มการแก้ไขไปยังความไม่สอดคล้องกัน</span><span class="sxs-lookup"><span data-stu-id="b42c9-203">Add a correction to a nonconformance</span></span>

<span data-ttu-id="b42c9-204">ในการเพิ่มการแก้ไขไปยังความไม่สอดคล้องกัน ให้ทำตามขั้นตอนเหล่านี้</span><span class="sxs-lookup"><span data-stu-id="b42c9-204">To add a correction to a nonconformance, follow these steps.</span></span>

1. <span data-ttu-id="b42c9-205">ไปที่ **การจัดการสินค้าคงคลัง \> งานประจำงวด \> การจัดการคุณภาพ \> ความไม่สอดคล้องกัน**</span><span class="sxs-lookup"><span data-stu-id="b42c9-205">Go to **Inventory management \> Periodic tasks \> Quality management \> Non conformances**.</span></span>
1. <span data-ttu-id="b42c9-206">ในรายการ เลือกความไม่สอดคล้องกันที่คุณต้องการจะอัพเดต</span><span class="sxs-lookup"><span data-stu-id="b42c9-206">In the list, select the nonconformance that you want to update.</span></span>

    > [!NOTE]
    > <span data-ttu-id="b42c9-207">คุณสามารถเพิ่มการแก้ไขไปยังความไม่สอดคล้องกันที่ได้รับอนุมัติได้เท่านั้น</span><span class="sxs-lookup"><span data-stu-id="b42c9-207">You can add a correction only to nonconformances that are approved.</span></span>

1. <span data-ttu-id="b42c9-208">บนบานหน้าต่างการดำเนินการ เลือก **การแก้ไข**</span><span class="sxs-lookup"><span data-stu-id="b42c9-208">On the Action Pane, select **Corrections**.</span></span>
1. <span data-ttu-id="b42c9-209">บนหน้า **การแก้ไข** ในบานหน้าต่างการดำเนินการ ให้เลือก **สร้าง** เพื่อเพิ่มแถวไปยังกริด</span><span class="sxs-lookup"><span data-stu-id="b42c9-209">On the **Corrections** page, on the Action Pane, select **New** to add a row to the grid.</span></span> <span data-ttu-id="b42c9-210">จากนั้นให้กำหนดฟิลด์ดังต่อไปนี้สำหรับแถวใหม่:</span><span class="sxs-lookup"><span data-stu-id="b42c9-210">Then set the following fields for the new row:</span></span>

    - <span data-ttu-id="b42c9-211">**การวินิจฉัย** – เลือกชนิดการวินิจฉัยที่ระบุชนิดของการแก้ไขที่คุณสร้างอยู่</span><span class="sxs-lookup"><span data-stu-id="b42c9-211">**Diagnostic** – Select the diagnostic type that identifies the type of correction that you're creating.</span></span>
    - <span data-ttu-id="b42c9-212">**ผู้ปฏิบัติงาน** – เลือกผู้ที่รับผิดชอบการแก้ไข</span><span class="sxs-lookup"><span data-stu-id="b42c9-212">**Worker** – Select the person who is responsible for the correction.</span></span>
    - <span data-ttu-id="b42c9-213">**ระดับความสำคัญของการแก้ไข** – เลือกตัวเลือกเพื่อบ่งชี้ว่าควรจะจัดระดับความสำคัญของการแก้ไขอย่างไร (*ต่ำ* *ปกติ* หรือ *สูง*)</span><span class="sxs-lookup"><span data-stu-id="b42c9-213">**Correction priority** – Select an option to indicate how the correction should be prioritized (*Low*, *Normal*, or *High*).</span></span>
    - <span data-ttu-id="b42c9-214">**วันที่ร้องขอ** – ป้อนวันที่ที่มีการร้องขอการดำเนินการแก้ไข</span><span class="sxs-lookup"><span data-stu-id="b42c9-214">**Requested date** – Enter the date when the corrective action was requested.</span></span>
    - <span data-ttu-id="b42c9-215">**วันที่วางแผนไว้** – ป้อนวันที่ที่คาดหวังให้การแก้ไขเสร็จสมบูรณ์</span><span class="sxs-lookup"><span data-stu-id="b42c9-215">**Planned date** – Enter the date when the correction is expected to be completed.</span></span>
    - <span data-ttu-id="b42c9-216">**วิธีแก้ไขปัญหาระยะสั้น** – เลือกกล่องกาเครื่องหมายนี้ ถ้าการดำเนินการแก้ไขแก้ไขความไม่สอดคล้องกันในระยะเวลาสั้นๆ เท่านั้น</span><span class="sxs-lookup"><span data-stu-id="b42c9-216">**Short term solution** – Select this check box if the corrective action corrects the nonconformance only for a short time.</span></span>

1. <span data-ttu-id="b42c9-217">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="b42c9-217">Close the pages.</span></span>

## <a name="mark-a-correction-as-completed"></a><span data-ttu-id="b42c9-218">ทำเครื่องหมายการแก้ไขเป็นเสร็จสมบูรณ์แล้ว</span><span class="sxs-lookup"><span data-stu-id="b42c9-218">Mark a correction as completed</span></span>

<span data-ttu-id="b42c9-219">ในการทำเครื่องหมายการแก้ไขความไม่สอดคล้องกันเป็นเสร็จสมบูรณ์แล้ว ให้ทำตามขั้นตอนเหล่านี้</span><span class="sxs-lookup"><span data-stu-id="b42c9-219">To mark a nonconformance correction as completed, follow these steps.</span></span>

1. <span data-ttu-id="b42c9-220">ไปที่ **การจัดการสินค้าคงคลัง \> งานประจำงวด \> การจัดการคุณภาพ \> ความไม่สอดคล้องกัน**</span><span class="sxs-lookup"><span data-stu-id="b42c9-220">Go to **Inventory management \> Periodic tasks \> Quality management \> Non conformances**.</span></span>
1. <span data-ttu-id="b42c9-221">ในรายการ เลือกความไม่สอดคล้องกันที่คุณต้องการจะอัพเดต</span><span class="sxs-lookup"><span data-stu-id="b42c9-221">In the list, select the nonconformance that you want to update.</span></span>

    > [!NOTE]
    > <span data-ttu-id="b42c9-222">คุณสามารถเพิ่มการแก้ไขไปยังความไม่สอดคล้องกันที่ได้รับอนุมัติได้เท่านั้น</span><span class="sxs-lookup"><span data-stu-id="b42c9-222">You can add a correction only to nonconformances that are approved.</span></span>

1. <span data-ttu-id="b42c9-223">บนบานหน้าต่างการดำเนินการ เลือก **การแก้ไข**</span><span class="sxs-lookup"><span data-stu-id="b42c9-223">On the Action Pane, select **Corrections**.</span></span>
1. <span data-ttu-id="b42c9-224">บนหน้า **การแก้ไข** ในกริด ให้เลือกการแก้ไขที่คุณต้องการทำเครื่องหมายเป็นเสร็จสมบูรณ์แล้ว</span><span class="sxs-lookup"><span data-stu-id="b42c9-224">On the **Corrections** page, in the grid, select the correction that you want to mark as completed.</span></span>
1. <span data-ttu-id="b42c9-225">ในบานหน้าต่างการดำเนินการ เลือก **ทำเครื่องหมายเป็นเสร็จสมบูรณ์**</span><span class="sxs-lookup"><span data-stu-id="b42c9-225">On the Action Pane, select **Mark complete**.</span></span>
1. <span data-ttu-id="b42c9-226">คุณได้รับพร้อมต์เพื่อยืนยันการเลือกของคุณ</span><span class="sxs-lookup"><span data-stu-id="b42c9-226">You're prompted to confirm your selection.</span></span> <span data-ttu-id="b42c9-227">เลือก **ตกลง** เพื่อดำเนินการต่อ</span><span class="sxs-lookup"><span data-stu-id="b42c9-227">Select **OK** to continue.</span></span> <span data-ttu-id="b42c9-228">มีการตั้งค่าฟิลด์ **วันที่และเวลาที่เสร็จสมบูรณ์** เป็นวันที่และเวลาปัจจุบัน และมีการเลือกกล่องกาเครื่องหมาย **เสร็จสมบูรณ์แล้ว**</span><span class="sxs-lookup"><span data-stu-id="b42c9-228">The **Completion date and time** field is set to the current date and time, and the **Completed** check box is selected.</span></span>
1. <span data-ttu-id="b42c9-229">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="b42c9-229">Close the page.</span></span>

## <a name="reopen-a-completed-correction"></a><span data-ttu-id="b42c9-230">เปิดการแก้ไขที่เสร็จสมบูรณ์แล้วใหม่</span><span class="sxs-lookup"><span data-stu-id="b42c9-230">Reopen a completed correction</span></span>

<span data-ttu-id="b42c9-231">ในการเปิดการแก้ไขที่เสร็จสมบูรณ์แล้วใหม่ ให้ทำตามขั้นตอนเหล่านี้</span><span class="sxs-lookup"><span data-stu-id="b42c9-231">To reopen a completed correction, follow these steps.</span></span>

1. <span data-ttu-id="b42c9-232">ไปที่ **การจัดการสินค้าคงคลัง \> งานประจำงวด \> การจัดการคุณภาพ \> ความไม่สอดคล้องกัน**</span><span class="sxs-lookup"><span data-stu-id="b42c9-232">Go to **Inventory management \> Periodic tasks \> Quality management \> Non conformances**.</span></span>
1. <span data-ttu-id="b42c9-233">ในรายการ เลือกความไม่สอดคล้องกันที่คุณต้องการจะอัพเดต</span><span class="sxs-lookup"><span data-stu-id="b42c9-233">In the list, select the nonconformance that you want to update.</span></span>
1. <span data-ttu-id="b42c9-234">บนบานหน้าต่างการดำเนินการ เลือก **การแก้ไข**</span><span class="sxs-lookup"><span data-stu-id="b42c9-234">On the Action pane, select **Corrections**.</span></span>
1. <span data-ttu-id="b42c9-235">บนหน้า **การแก้ไข** ในกริด ให้เลือกการแก้ไขที่คุณต้องการเปิดใหม่</span><span class="sxs-lookup"><span data-stu-id="b42c9-235">On the **Corrections** page, in the grid, select the correction that you want to reopen.</span></span>
1. <span data-ttu-id="b42c9-236">บนบานหน้าต่างการดำเนินการ เลือก **เปิดใหม่**</span><span class="sxs-lookup"><span data-stu-id="b42c9-236">On the Action Pane, select **Reopen**.</span></span>
1. <span data-ttu-id="b42c9-237">คุณได้รับพร้อมต์เพื่อยืนยันการเลือกของคุณ</span><span class="sxs-lookup"><span data-stu-id="b42c9-237">You're prompted to confirm your selection.</span></span> <span data-ttu-id="b42c9-238">เลือก **ตกลง** เพื่อดำเนินการต่อ</span><span class="sxs-lookup"><span data-stu-id="b42c9-238">Select **OK** to continue.</span></span> <span data-ttu-id="b42c9-239">ค่านี้จะถูกล้างข้อมูลจากฟิลด์ **วันที่และเวลาที่เสร็จสมบูรณ์** และมีการยกเลิกการเลือกกล่องกาเครื่องหมาย **เสร็จสมบูรณ์แล้ว**</span><span class="sxs-lookup"><span data-stu-id="b42c9-239">The value is cleared from the **Completion date and time** field, and the **Completed** check box is cleared.</span></span>
1. <span data-ttu-id="b42c9-240">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="b42c9-240">Close the page.</span></span>

<span data-ttu-id="b42c9-241">ขณะนี้ คุณสามารถทำการแก้ไขหรืออัพเดตเพิ่มเติมไปยังการแก้ไขได้</span><span class="sxs-lookup"><span data-stu-id="b42c9-241">You can now make additional edits or updates to the correction.</span></span> <span data-ttu-id="b42c9-242">เมื่อคุณเสร็จสิ้นแล้ว คุณสามารถทำเครื่องหมายการแก้ไขเป็นเสร็จสมบูรณ์แล้วได้อีกครั้ง</span><span class="sxs-lookup"><span data-stu-id="b42c9-242">When you've finished, you can mark the correction as completed again.</span></span>

## <a name="close-a-nonconformance"></a><span data-ttu-id="b42c9-243">ปิดความไม่สอดคล้องกัน</span><span class="sxs-lookup"><span data-stu-id="b42c9-243">Close a nonconformance</span></span>

<span data-ttu-id="b42c9-244">เมื่อต้องการปิดความไม่สอดคล้องกัน ให้ทำตามขั้นตอนเหล่านี้</span><span class="sxs-lookup"><span data-stu-id="b42c9-244">To close a nonconformance, follow these steps.</span></span>

1. <span data-ttu-id="b42c9-245">ไปที่ **การจัดการสินค้าคงคลัง \> งานประจำงวด \> การจัดการคุณภาพ \> ใบสั่งตรวจสอบคุณภาพ**</span><span class="sxs-lookup"><span data-stu-id="b42c9-245">Go to **Inventory management \> Periodic tasks \> Quality management \> Quality orders**.</span></span>
1. <span data-ttu-id="b42c9-246">เลือกใบสั่งตรวจสอบคุณภาพในกริด</span><span class="sxs-lookup"><span data-stu-id="b42c9-246">Select a quality order in the grid.</span></span>
1. <span data-ttu-id="b42c9-247">บนบานหน้าต่างการดำเนินการ เลือก **การสอบถาม \> ความไม่สอดคล้องกัน**</span><span class="sxs-lookup"><span data-stu-id="b42c9-247">On the Action Pane, select **Inquiries \> Non conformances**.</span></span>
1. <span data-ttu-id="b42c9-248">บนหน้า **ความไม่สอดคล้องกัน** ให้เลือกความไม่สอดคล้องกันของเป้าหมายในกริด</span><span class="sxs-lookup"><span data-stu-id="b42c9-248">On the **Non conformances** page, select the target nonconformance in the grid.</span></span>
1. <span data-ttu-id="b42c9-249">บนบานหน้าต่างการดำเนินการ เลือก **ฟังก์ชัน \> ปิดความไม่สอดคล้องกัน**</span><span class="sxs-lookup"><span data-stu-id="b42c9-249">On the Action Pane, select **Functions \> Close non conformance**.</span></span>
1. <span data-ttu-id="b42c9-250">คุณได้รับพร้อมต์เพื่อยืนยันการเลือกของคุณ</span><span class="sxs-lookup"><span data-stu-id="b42c9-250">You're prompted to confirm your selection.</span></span> <span data-ttu-id="b42c9-251">เลือก **ใช่** เพื่อดำเนินการต่อ</span><span class="sxs-lookup"><span data-stu-id="b42c9-251">Select **Yes** to continue.</span></span>
1. <span data-ttu-id="b42c9-252">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="b42c9-252">Close the pages.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="b42c9-253">ทรัพยากรเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="b42c9-253">Additional resources</span></span>

- [<span data-ttu-id="b42c9-254">ภาพรวมของการจัดการคุณภาพ</span><span class="sxs-lookup"><span data-stu-id="b42c9-254">Quality management overview</span></span>](../quality-management-processes.md)
- [<span data-ttu-id="b42c9-255">เปิดใช้งานการจัดการคุณภาพและความไม่สอดคล้องกัน</span><span class="sxs-lookup"><span data-stu-id="b42c9-255">Enable quality and nonconformance management</span></span>](../enable-quality-management.md)
- [<span data-ttu-id="b42c9-256">ผู้ปฏิบัติงานที่รับผิดชอบการอนุมัติความไม่สอดคล้องกัน</span><span class="sxs-lookup"><span data-stu-id="b42c9-256">Workers responsible for approving nonconformances</span></span>](../quality-responsible-workers.md)
- [<span data-ttu-id="b42c9-257">โซนตรวจสอบสินค้าสำหรับความไม่สอดคล้องกัน</span><span class="sxs-lookup"><span data-stu-id="b42c9-257">Quarantine zones for nonconformances</span></span>](../quality-quarantine-zones.md)
- [<span data-ttu-id="b42c9-258">ชนิดของการวินิจฉัยสำหรับความไม่สอดคล้องกัน</span><span class="sxs-lookup"><span data-stu-id="b42c9-258">Diagnostic types for nonconformances</span></span>](../quality-diagnostic-types.md)
- [<span data-ttu-id="b42c9-259">ค่าธรรมเนียมคุณภาพสำหรับความไม่สอดคล้องกัน</span><span class="sxs-lookup"><span data-stu-id="b42c9-259">Quality charges for nonconformances</span></span>](../quality-charges.md)
- [<span data-ttu-id="b42c9-260">การดำเนินงานสำหรับความไม่สอดคล้องกัน</span><span class="sxs-lookup"><span data-stu-id="b42c9-260">Operations for nonconformances</span></span>](../quality-operations.md)
- [<span data-ttu-id="b42c9-261">การจัดการคุณภาพสำหรับกระบวนการคลังสินค้า</span><span class="sxs-lookup"><span data-stu-id="b42c9-261">Quality management for warehouse processes</span></span>](../quality-management-for-warehouses-processes.md)

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
