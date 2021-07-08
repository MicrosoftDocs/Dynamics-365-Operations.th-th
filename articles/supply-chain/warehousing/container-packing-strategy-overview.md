---
title: กลยุทธ์การบรรจุคอนเทนเนอร์
description: หัวข้อนี้อธิบายความแตกต่างระหว่างกลยุทธ์การบรรจุคอนเทนเนอร์และให้ตัวอย่าง
author: GalynaFedorova
ms.date: 06/11/2021
ms.topic: article
ms.search.form: WHSWaveTemplateTable, InventLocationIdLookup, WHSContainerType, WHSContainerGroup, WHSContainerizationTable, WHSContainerizationBreak, WHSCreateContainerBreak, WHSContainerStructure, WHSContainerTable
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: v-gfedorova
ms.search.validFrom: 2021-06-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: f481f6ca047ee0285fe0e81d8fa96665e9d27cee
ms.sourcegitcommit: 8e846b52763f90d2232ec7d427839f4722570bce
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 06/22/2021
ms.locfileid: "6292772"
---
# <a name="container-packing-strategies"></a><span data-ttu-id="8528f-103">กลยุทธ์การบรรจุคอนเทนเนอร์</span><span class="sxs-lookup"><span data-stu-id="8528f-103">Container packing strategies</span></span>

<span data-ttu-id="8528f-104">*กลยุทธ์การบรรจุคอนเทนเนอร์* คือกลยุทธ์ที่คุณสามารถใช้ในการกําหนดการปันส่วนสินค้าทั่วทั้งคอนเทนเนอร์</span><span class="sxs-lookup"><span data-stu-id="8528f-104">A *container packing strategy* is a strategy that you can use to define item allocations across containers.</span></span> <span data-ttu-id="8528f-105">หัวข้อนี้อธิบายความแตกต่างระหว่างกลยุทธ์ *บรรจุลงในคอนเทนเนอร์ที่เปิดอยู่ทั้งหมด* และ *บรรจุลงในเฉพาะคอนเทนเนอร์ปัจจุบันเท่านั้น*</span><span class="sxs-lookup"><span data-stu-id="8528f-105">This topic explains the differences between the *Pack into all open containers* and *Pack into current container only* strategies.</span></span>

- <span data-ttu-id="8528f-106">**บรรจุลงในคอนเทนเนอร์ที่เปิดอยู่ทั้งหมด** – ระบบต้องตรวจสอบคอนเทนเนอร์ที่เปิดทั้งหมดซึ่งสร้างขึ้นแล้วในระหว่างวงจรของการบรรจุลงตู้บรรจุสินค้า เพื่อให้แน่ใจว่าสินค้าจะพอดีกับคอนเทนเนอร์หนึ่ง</span><span class="sxs-lookup"><span data-stu-id="8528f-106">**Pack into all open containers** – The system must check all open containers that have already been created during the containerization cycle, to make sure that the item will fit into one of them.</span></span> <span data-ttu-id="8528f-107">ในระหว่างการบรรจุ ระบบจะตรวจสอบสินค้าแต่ละรายการเพื่อกําหนดว่าสินค้าจะพอดีกับคอนเทนเนอร์ที่สร้างขึ้นก่อนหน้านี้หรือไม่</span><span class="sxs-lookup"><span data-stu-id="8528f-107">During packing, the system checks each item to determine whether it will fit into any of the previously created containers.</span></span> <span data-ttu-id="8528f-108">ถ้าสินค้าไม่พอดีกับคอนเทนเนอร์ที่มีอยู่ ระบบจะสร้างคอนเทนเนอร์ใหม่และทำต่อจนกว่าจะเสร็จสิ้นการบรรจุใบสั่งทั้งหมดแล้ว</span><span class="sxs-lookup"><span data-stu-id="8528f-108">If the item won't fit into an existing container, the system creates a new container and continues until it has finished packing the whole order.</span></span>

    <span data-ttu-id="8528f-109">ตัวอย่างเช่น สินค้าลำดับที่ *n* ต้องมีการบรรจุลงตู้บรรจุสินค้า</span><span class="sxs-lookup"><span data-stu-id="8528f-109">For example, *n* ordered items require containerization.</span></span> <span data-ttu-id="8528f-110">ในกรณีที่แย่ที่สุด ทุกครั้งที่ระบบประมวลผลสินค้าที่ไม่พอดีกับคอนเทนเนอร์ที่มีอยู่ใดๆ ระบบจะตรวจสอบ (\[(*n* – 1) × (*n* + 1)\] ÷ 2) ทั้งหมดเพื่อประเมินว่าสินค้านั้นพอดีกับคอนเทนเนอร์ที่มีอยู่หรือไม่</span><span class="sxs-lookup"><span data-stu-id="8528f-110">In the worst case, every time that the system processes an item that doesn't fit into any existing container, it will do a total of (\[(*n* – 1) × (*n* + 1)\] ÷ 2) checks to evaluate whether the item fits into the existing containers.</span></span>

- <span data-ttu-id="8528f-111">**บรรจุลงตู้บรรจุสินค้าปัจจุบันเท่านั้น** – ระบบต้องตรวจสอบเฉพาะคอนเทนเนอร์ที่สร้างขึ้นล่าสุดเท่านั้นเพื่อให้แน่ใจว่าสินค้าจะพอดีกับคอนเทนเนอร์</span><span class="sxs-lookup"><span data-stu-id="8528f-111">**Pack into current container only** – The system must check only the most recently created container to make sure that the item will fit into it.</span></span> <span data-ttu-id="8528f-112">ในระหว่างการบรรจุ ระบบจะตรวจสอบสินค้าแต่ละรายการเพื่อกําหนดว่าสินค้าจะพอดีกับคอนเทนเนอร์ที่สร้างขึ้นล่าสุดหรือไม่</span><span class="sxs-lookup"><span data-stu-id="8528f-112">During packing, the system checks each item to determine whether it will fit into the most recently created container.</span></span> <span data-ttu-id="8528f-113">ถ้าสินค้าไม่พอดีกับคอนเทนเนอร์ ระบบจะสร้างคอนเทนเนอร์ใหม่และทำต่อจนกว่าจะเสร็จสิ้นการบรรจุใบสั่งทั้งหมดแล้ว</span><span class="sxs-lookup"><span data-stu-id="8528f-113">If the item won't fit into that container, the system creates a new container and continues until it has finished packing the whole order.</span></span>

    <span data-ttu-id="8528f-114">ตัวอย่างเช่น สินค้าลำดับที่ *n* ต้องมีการบรรจุลงตู้บรรจุสินค้า</span><span class="sxs-lookup"><span data-stu-id="8528f-114">For example, *n* ordered items require containerization.</span></span> <span data-ttu-id="8528f-115">ในกรณีที่แย่ที่สุด ระบบจะตรวจสอบทั้งหมด (*n* – 1) เพื่อประเมินว่าสินค้าพอดีกับคอนเทนเนอร์หรือไม่</span><span class="sxs-lookup"><span data-stu-id="8528f-115">In the worst case, the system will do a total of (*n* – 1) checks to evaluate whether the item fits into the containers.</span></span>

## <a name="example-of-the-flow-for-container-packing-strategies"></a><span data-ttu-id="8528f-116">ตัวอย่างของขั้นตอนของกลยุทธ์การบรรจุคอนเทนเนอร์</span><span class="sxs-lookup"><span data-stu-id="8528f-116">Example of the flow for container packing strategies</span></span>

<span data-ttu-id="8528f-117">คุณเตรียมสินค้าต่อไปนี้สำหรับการบรรจุลงตู้บรรจุสินค้า</span><span class="sxs-lookup"><span data-stu-id="8528f-117">You set up the following items for containerization.</span></span>

| <span data-ttu-id="8528f-118">สินค้า</span><span class="sxs-lookup"><span data-stu-id="8528f-118">Item</span></span> | <span data-ttu-id="8528f-119">มิติทางกายภาพ (ความกว้าง × ความลึก × ความสูง)</span><span class="sxs-lookup"><span data-stu-id="8528f-119">Physical dimensions (width × depth × height)</span></span> | <span data-ttu-id="8528f-120">น้ำหนัก</span><span class="sxs-lookup"><span data-stu-id="8528f-120">Weight</span></span> |
|---|---|---|
| <span data-ttu-id="8528f-121">สายไฟ HDMI 6'</span><span class="sxs-lookup"><span data-stu-id="8528f-121">HDMI Cable 6'</span></span> | <span data-ttu-id="8528f-122">1 × 1 × 1</span><span class="sxs-lookup"><span data-stu-id="8528f-122">1 × 1 × 1</span></span> | <span data-ttu-id="8528f-123">1</span><span class="sxs-lookup"><span data-stu-id="8528f-123">1</span></span> |
| <span data-ttu-id="8528f-124">สายไฟ HDMI 12'</span><span class="sxs-lookup"><span data-stu-id="8528f-124">HDMI Cable 12'</span></span> | <span data-ttu-id="8528f-125">2 × 1 × 1</span><span class="sxs-lookup"><span data-stu-id="8528f-125">2 × 1 × 1</span></span> | <span data-ttu-id="8528f-126">1</span><span class="sxs-lookup"><span data-stu-id="8528f-126">1</span></span> |
| <span data-ttu-id="8528f-127">สายไฟ HDMI 18'</span><span class="sxs-lookup"><span data-stu-id="8528f-127">HDMI Cable 18'</span></span> | <span data-ttu-id="8528f-128">3 × 1 × 1</span><span class="sxs-lookup"><span data-stu-id="8528f-128">3 × 1 × 1</span></span> | <span data-ttu-id="8528f-129">2</span><span class="sxs-lookup"><span data-stu-id="8528f-129">2</span></span> |

<span data-ttu-id="8528f-130">คุณยังตั้งค่ากล่องต่อไปนี้ที่จะใช้กับบรรจุภัณฑ์ด้วย</span><span class="sxs-lookup"><span data-stu-id="8528f-130">You also set up the following box that will be used for packaging.</span></span>

| <span data-ttu-id="8528f-131">Container</span><span class="sxs-lookup"><span data-stu-id="8528f-131">Container</span></span> | <span data-ttu-id="8528f-132">มิติทางกายภาพ (ความยาว × ความกว้าง × ความสูง)</span><span class="sxs-lookup"><span data-stu-id="8528f-132">Physical dimensions (length × width × height)</span></span> | <span data-ttu-id="8528f-133">น้ำหนัก</span><span class="sxs-lookup"><span data-stu-id="8528f-133">Weight</span></span> | <span data-ttu-id="8528f-134">ปริมาตร</span><span class="sxs-lookup"><span data-stu-id="8528f-134">Volume</span></span> |
|---|---|---|---|
| <span data-ttu-id="8528f-135">กล่องขนาดกลาง</span><span class="sxs-lookup"><span data-stu-id="8528f-135">Medium Box</span></span> | <span data-ttu-id="8528f-136">6 × 3 × 2</span><span class="sxs-lookup"><span data-stu-id="8528f-136">6 × 3 × 2</span></span> | <span data-ttu-id="8528f-137">10</span><span class="sxs-lookup"><span data-stu-id="8528f-137">10</span></span> | <span data-ttu-id="8528f-138">100</span><span class="sxs-lookup"><span data-stu-id="8528f-138">100</span></span> |

<span data-ttu-id="8528f-139">สุดท้าย ให้คุณตั้งค่าใบสั่งที่มีผลิตภัณฑ์และปริมาณต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="8528f-139">Finally, you set up an order that has the following products and quantities.</span></span>

| <span data-ttu-id="8528f-140">รายการใบสั่งขาย</span><span class="sxs-lookup"><span data-stu-id="8528f-140">Sales order line</span></span> | <span data-ttu-id="8528f-141">ปริมาณ</span><span class="sxs-lookup"><span data-stu-id="8528f-141">Quantity</span></span> |
|---|---|
| <span data-ttu-id="8528f-142">สายไฟ HDMI 12'</span><span class="sxs-lookup"><span data-stu-id="8528f-142">HDMI Cable 12'</span></span> | <span data-ttu-id="8528f-143">9</span><span class="sxs-lookup"><span data-stu-id="8528f-143">9</span></span> |
| <span data-ttu-id="8528f-144">สายไฟ HDMI 18'</span><span class="sxs-lookup"><span data-stu-id="8528f-144">HDMI Cable 18'</span></span> | <span data-ttu-id="8528f-145">8</span><span class="sxs-lookup"><span data-stu-id="8528f-145">8</span></span> |
| <span data-ttu-id="8528f-146">สายไฟ HDMI 6'</span><span class="sxs-lookup"><span data-stu-id="8528f-146">HDMI Cable 6'</span></span> | <span data-ttu-id="8528f-147">13</span><span class="sxs-lookup"><span data-stu-id="8528f-147">13</span></span> |

<span data-ttu-id="8528f-148">ตารางต่อไปนี้สรุปวิธีการใช้งานการบรรจุลงตู้บรรจุสินค้าเมื่อคุณใช้กลยุทธ์ *บรรจุลงในคอนเทนเนอร์ที่เปิดอยู่ทั้งหมด* และเมื่อคุณใช้กลยุทธ์ *บรรจุลงในเฉพาะคอนเทนเนอร์ปัจจุบันเท่านั้น*</span><span class="sxs-lookup"><span data-stu-id="8528f-148">The following table summarizes how containerization works when you use the *Pack into all open containers* strategy and when you use the *Pack into current container only* strategy.</span></span>

| <span data-ttu-id="8528f-149">บรรจุลงในตู้บรรจุสินค้าที่เปิดทั้งหมด</span><span class="sxs-lookup"><span data-stu-id="8528f-149">Pack into all open containers</span></span> | <span data-ttu-id="8528f-150">บรรจุลงในคอนเทนเนอร์ปัจจุบัน</span><span class="sxs-lookup"><span data-stu-id="8528f-150">Pack into current container</span></span> |
|---|---|
| <p><span data-ttu-id="8528f-151">สายไฟ HDMI 12':</span><span class="sxs-lookup"><span data-stu-id="8528f-151">HDMI Cable 12':</span></span></p><ol><li><span data-ttu-id="8528f-152">สร้างคอนเทนเนอร์ใหม่ CONT0001</span><span class="sxs-lookup"><span data-stu-id="8528f-152">Create a new container, CONT0001.</span></span></li><li><span data-ttu-id="8528f-153">ใส่ 9 ชิ้นลงในคอนเทนเนอร์ CONT0001</span><span class="sxs-lookup"><span data-stu-id="8528f-153">Put 9 ea into container CONT0001.</span></span></li></ol> | <p><span data-ttu-id="8528f-154">สายไฟ HDMI 12':</span><span class="sxs-lookup"><span data-stu-id="8528f-154">HDMI Cable 12':</span></span></p><ol><li><span data-ttu-id="8528f-155">สร้างคอนเทนเนอร์ใหม่ CONT0001</span><span class="sxs-lookup"><span data-stu-id="8528f-155">Create a new container, CONT0001.</span></span></li><li><span data-ttu-id="8528f-156">ใส่ 9 ชิ้นลงในคอนเทนเนอร์ CONT0001</span><span class="sxs-lookup"><span data-stu-id="8528f-156">Put 9 ea into container CONT0001.</span></span></li></ol> |
| <p><span data-ttu-id="8528f-157">สายไฟ HDMI 18':</span><span class="sxs-lookup"><span data-stu-id="8528f-157">HDMI Cable 18':</span></span></p><ol><li><span data-ttu-id="8528f-158">ตรวจสอบว่าสินค้าสามารถบรรจุลงในคอนเทนเนอร์ CONT0001 ได้หรือไม่</span><span class="sxs-lookup"><span data-stu-id="8528f-158">Check whether the item can fit into container CONT0001.</span></span></li><li><span data-ttu-id="8528f-159">สร้างคอนเทนเนอร์ใหม่ CONT0002</span><span class="sxs-lookup"><span data-stu-id="8528f-159">Create a new container, CONT0002.</span></span></li><li><span data-ttu-id="8528f-160">ใส่ 5 ชิ้นลงในคอนเทนเนอร์ CONT0002</span><span class="sxs-lookup"><span data-stu-id="8528f-160">Put 5 ea into container CONT0002.</span></span></li><li><span data-ttu-id="8528f-161">สร้างคอนเทนเนอร์ใหม่ CONT0003</span><span class="sxs-lookup"><span data-stu-id="8528f-161">Create a new container, CONT0003.</span></span></li><li><span data-ttu-id="8528f-162">ใส่ 3 ชิ้นลงในคอนเทนเนอร์ CONT0003</span><span class="sxs-lookup"><span data-stu-id="8528f-162">Put 3 ea into container CONT0003.</span></span></li></ol> | <p><span data-ttu-id="8528f-163">สายไฟ HDMI 18':</span><span class="sxs-lookup"><span data-stu-id="8528f-163">HDMI Cable 18':</span></span></p><ol><li><span data-ttu-id="8528f-164">ตรวจสอบว่าสินค้าสามารถบรรจุลงในคอนเทนเนอร์ CONT0001 ได้หรือไม่</span><span class="sxs-lookup"><span data-stu-id="8528f-164">Check whether the item can fit into container CONT0001.</span></span></li><li><span data-ttu-id="8528f-165">สร้างคอนเทนเนอร์ใหม่ CONT0002</span><span class="sxs-lookup"><span data-stu-id="8528f-165">Create a new container, CONT0002.</span></span></li><li><span data-ttu-id="8528f-166">ใส่ 5 ชิ้นลงในคอนเทนเนอร์ CONT0002</span><span class="sxs-lookup"><span data-stu-id="8528f-166">Put 5 ea into container CONT0002.</span></span></li><li><span data-ttu-id="8528f-167">สร้างคอนเทนเนอร์ใหม่ CONT0003</span><span class="sxs-lookup"><span data-stu-id="8528f-167">Create a new container, CONT0003.</span></span></li><li><span data-ttu-id="8528f-168">ใส่ 3 ชิ้นลงในคอนเทนเนอร์ CONT0003</span><span class="sxs-lookup"><span data-stu-id="8528f-168">Put 3 ea into container CONT0003.</span></span></li></ol> |
| <p><span data-ttu-id="8528f-169">สายไฟ HDMI 6':</span><span class="sxs-lookup"><span data-stu-id="8528f-169">HDMI Cable 6':</span></span></p><ol><li><span data-ttu-id="8528f-170">ตรวจสอบว่าสินค้าสามารถบรรจุลงในคอนเทนเนอร์ CONT0001 ได้หรือไม่</span><span class="sxs-lookup"><span data-stu-id="8528f-170">Check whether the item can fit into container CONT0001.</span></span></li><li><span data-ttu-id="8528f-171">ใส่ 1 ชิ้นลงในคอนเทนเนอร์ CONT0001</span><span class="sxs-lookup"><span data-stu-id="8528f-171">Put 1 ea into container CONT0001.</span></span></li><li><span data-ttu-id="8528f-172">ตรวจสอบว่าสินค้าสามารถบรรจุลงในคอนเทนเนอร์ CONT0002 ได้หรือไม่</span><span class="sxs-lookup"><span data-stu-id="8528f-172">Check whether the item can fit into container CONT0002.</span></span></li><li><span data-ttu-id="8528f-173">ตรวจสอบว่าสินค้าสามารถบรรจุลงในคอนเทนเนอร์ CONT0003 ได้หรือไม่</span><span class="sxs-lookup"><span data-stu-id="8528f-173">Check whether the item can fit into container CONT0003.</span></span></li><li><span data-ttu-id="8528f-174">ใส่ 4 ชิ้นลงในคอนเทนเนอร์ CONT0003</span><span class="sxs-lookup"><span data-stu-id="8528f-174">Put 4 ea into container CONT0003.</span></span></li><li><span data-ttu-id="8528f-175">สร้างคอนเทนเนอร์ใหม่ CONT0004</span><span class="sxs-lookup"><span data-stu-id="8528f-175">Create a new container, CONT0004.</span></span></li><li><span data-ttu-id="8528f-176">ใส่ 8 ชิ้นลงในคอนเทนเนอร์ CONT0004</span><span class="sxs-lookup"><span data-stu-id="8528f-176">Put 8 ea into container CONT0004.</span></span></li></ol> | <p><span data-ttu-id="8528f-177">สายไฟ HDMI 6':</span><span class="sxs-lookup"><span data-stu-id="8528f-177">HDMI Cable 6':</span></span></p><ol><li><span data-ttu-id="8528f-178">ตรวจสอบว่าสินค้าสามารถบรรจุลงในคอนเทนเนอร์ CONT0003 ได้หรือไม่</span><span class="sxs-lookup"><span data-stu-id="8528f-178">Check whether the item can fit into container CONT0003.</span></span></li><li><span data-ttu-id="8528f-179">ใส่ 4 ชิ้นลงในคอนเทนเนอร์ CONT0003</span><span class="sxs-lookup"><span data-stu-id="8528f-179">Put 4 ea into container CONT0003.</span></span></li><li><span data-ttu-id="8528f-180">สร้างคอนเทนเนอร์ใหม่ CONT0004</span><span class="sxs-lookup"><span data-stu-id="8528f-180">Create a new container, CONT0004.</span></span></li><li><span data-ttu-id="8528f-181">ใส่ 9 ชิ้นลงในคอนเทนเนอร์ CONT0004</span><span class="sxs-lookup"><span data-stu-id="8528f-181">Put 9 ea into container CONT0004.</span></span></li></ol> |

## <a name="example-scenario-pack-single-orders-per-container"></a><span data-ttu-id="8528f-182">ตัวอย่างสถานการณ์: บรรจุใบสั่งเดียวต่อคอนเทนเนอร์</span><span class="sxs-lookup"><span data-stu-id="8528f-182">Example scenario: Pack single orders per container</span></span>

<span data-ttu-id="8528f-183">ส่วนนี้จะแสดงสถานการณ์ที่ระบบได้รับการตั้งค่าให้รวมบัญชีใบสั่งหลายใบเป็นการจัดส่งครั้งเดียวกัน</span><span class="sxs-lookup"><span data-stu-id="8528f-183">This section presents a scenario where the system is set up to consolidate multiple orders into one shipment.</span></span> <span data-ttu-id="8528f-184">ดังนั้น การบรรจุลงตู้บรรจุสินค้าจะทำจากใบสั่งขายเพื่อให้มั่นใจว่าใบสั่งทุกรายการที่มีผลิตภัณฑ์หลายรายการถูกบรรจุลงในคอนเทนเนอร์ของตนเอง</span><span class="sxs-lookup"><span data-stu-id="8528f-184">Therefore, containerization will be done from the sales order to ensure that every order that contains multiple products is packed into its own container.</span></span>

<span data-ttu-id="8528f-185">ฟังก์ชันนี้ช่วยให้คุณสามารถจัดการสถานการณ์ที่คุณต้องบรรจุใบสั่งขายเพียงใบสั่งเดียวลงในแต่ละคอนเทนเนอร์ เพื่อให้ศูนย์กระจายสินค้าสามารถบรรจุสินค้าแบบเติมสินค้าผ่านศูนย์เปลี่ยนมือระหว่างร้านค้าปลีกต่างๆ ได้</span><span class="sxs-lookup"><span data-stu-id="8528f-185">This functionality lets you handle scenarios where you must pack only one sales order into each container, so that the distribution center can cross-dock full containers between retail stores.</span></span> <span data-ttu-id="8528f-186">นอกจากสถานการณ์การขายปลีกแล้ว (สั่งตามร้านค้าปลีกและการจัดส่งสินค้าไปยังศูนย์กระจายสินค้าเพื่อการส่งสินค้าผ่านศูนย์เปลี่ยนถ่ายสินค้า) เทคนิคนี้ยังสามารถใช้ในห่วงโซ่การผลิตแบบ Lean (ใบสั่งขายต่อสายการผลิตแบบทันเวลา)</span><span class="sxs-lookup"><span data-stu-id="8528f-186">In addition to the retail scenarios (order per retail store and shipping to a distribution center for cross-docking) this technique is also commonly used in lean supply chains (sales order per just-in-time production line).</span></span>

<span data-ttu-id="8528f-187">สถานการณ์นี้แสดงวิธีการลดจํานวนของคอนเทนเนอร์ที่มีการประเมินระหว่างการบรรจุโดยใช้กลยุทธ์ *บรรจุลงในเฉพาะคอนเทนเนอร์ปัจจุบันเท่านั้น* สำหรับการบรรจุลงตู้บรรจุสินค้า</span><span class="sxs-lookup"><span data-stu-id="8528f-187">This scenario shows how you can decrease the number of containers that are evaluated during packing by using the *Pack into current container only* strategy for containerization.</span></span>

### <a name="prerequisites"></a><span data-ttu-id="8528f-188">ข้อกำหนดเบื้องต้น</span><span class="sxs-lookup"><span data-stu-id="8528f-188">Prerequisites</span></span>

#### <a name="turn-on-the-consolidate-shipments-feature-in-your-system"></a><span data-ttu-id="8528f-189">เปิดคุณลักษณะรวมบัญชีการจัดส่งในระบบของคุณ</span><span class="sxs-lookup"><span data-stu-id="8528f-189">Turn on the Consolidate shipments feature in your system</span></span>

<span data-ttu-id="8528f-190">สถานการณ์นี้ใช้คุณลักษณะ *รวมบัญชีการจัดส่ง*</span><span class="sxs-lookup"><span data-stu-id="8528f-190">This scenario uses the *Consolidate shipments* feature.</span></span> <span data-ttu-id="8528f-191">ถ้าคุณลักษณะนั้นไม่พร้อมใช้งานในระบบของคุณอยู่แล้ว คุณต้องเปิดคุณลักษณะนี้โดยใช้ [การจัดการคุณลักษณะ](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md)</span><span class="sxs-lookup"><span data-stu-id="8528f-191">If that feature isn't already available in your system, you must turn it on by using [Feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).</span></span>

#### <a name="make-demo-data-available"></a><span data-ttu-id="8528f-192">ทำให้ข้อมูลสาธิตพร้อมใช้งาน</span><span class="sxs-lookup"><span data-stu-id="8528f-192">Make demo data available</span></span>

<span data-ttu-id="8528f-193">สถานการณ์จำลองนี้อ้างอิงค่าและเรกคอร์ดที่ถูกรวมอยู่ในข้อมูลสาธิตมาตรฐานที่ให้ไว้สำหรับ Microsoft Dynamics 365 Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="8528f-193">This scenario references values and records that are included in the standard demo data that is provided for Microsoft Dynamics 365 Supply Chain Management.</span></span> <span data-ttu-id="8528f-194">ถ้าคุณต้องการใช้ค่าที่ระบุไว้ที่นี่เมื่อคุณทำแบบฝึกหัด ควรตรวจสอบให้แน่ใจว่าได้ทำงานในสภาพแวดล้อมที่มีการติดตั้งข้อมูลสาธิต และตั้งค่านิติบุคคลเป็น **USMF** ก่อนที่คุณจะเริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="8528f-194">If you want to use the values that are provided here as you do the exercises, be sure to work in an environment where the demo data is installed, and set the legal entity to **USMF** before you begin.</span></span>

### <a name="inspect-or-create-container-types"></a><span data-ttu-id="8528f-195">ตรวจสอบหรือสร้างชนิดคอนเทนเนอร์</span><span class="sxs-lookup"><span data-stu-id="8528f-195">Inspect or create container types</span></span>

<span data-ttu-id="8528f-196">หากต้องการตรวจสอบชนิดคอนเทนเนอร์ของคุณ หรือสร้างชนิดคอนเทนเนอร์ใหม่หากคอนเทนเนอร์ชนิดใดที่ต้องการ ให้ปฏิบัติตามขั้นตอนเหล่านี้</span><span class="sxs-lookup"><span data-stu-id="8528f-196">To inspect your container types, or to create new container types if they are required, follow these steps.</span></span>

1. <span data-ttu-id="8528f-197">ไปที่ **Warehouse Management** \> **การตั้งค่า** \> **คอนเทนเนอร์** \> **ชนิดของคอนเทนเนอร์**</span><span class="sxs-lookup"><span data-stu-id="8528f-197">Go to **Warehouse management** \> **Setup** \> **Containers** \> **Container types**.</span></span>
1. <span data-ttu-id="8528f-198">ตรวจสอบให้แน่ใจว่าชนิดคอนเทนเนอร์แต่ละชนิดต่อไปนี้พร้อมใช้งานในข้อมูลสาธิตของคุณ</span><span class="sxs-lookup"><span data-stu-id="8528f-198">Make sure that each of the following container types is available in your demo data.</span></span> <span data-ttu-id="8528f-199">แก้ไขหรือสร้างชนิดคอนเทนเนอร์ตามที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="8528f-199">Edit or create container types as required.</span></span>

    - <span data-ttu-id="8528f-200">ชนิดคอนเทนเนอร์ 1:</span><span class="sxs-lookup"><span data-stu-id="8528f-200">Container type 1:</span></span>

        - <span data-ttu-id="8528f-201">**รหัสชนิดคอนเทนเนอร์:** *กล่อง-ใหญ่*</span><span class="sxs-lookup"><span data-stu-id="8528f-201">**Container type code:** *Box-Large*</span></span>
        - <span data-ttu-id="8528f-202">**คำอธิบาย:** *กล่องขนาดใหญ่*</span><span class="sxs-lookup"><span data-stu-id="8528f-202">**Description:** *Large Box*</span></span>
        - <span data-ttu-id="8528f-203">**น้ำหนักสุทธิสูงสุด:** *100*</span><span class="sxs-lookup"><span data-stu-id="8528f-203">**Maximum net weight:** *100*</span></span>
        - <span data-ttu-id="8528f-204">**ปริมาตร:** *400*</span><span class="sxs-lookup"><span data-stu-id="8528f-204">**Volume:** *400*</span></span>
        - <span data-ttu-id="8528f-205">**ความยาว:** *4*</span><span class="sxs-lookup"><span data-stu-id="8528f-205">**Length:** *4*</span></span>
        - <span data-ttu-id="8528f-206">**ความกว้าง:** *10*</span><span class="sxs-lookup"><span data-stu-id="8528f-206">**Width:** *10*</span></span>
        - <span data-ttu-id="8528f-207">**ความสูง:** *10*</span><span class="sxs-lookup"><span data-stu-id="8528f-207">**Height:** *10*</span></span>

    - <span data-ttu-id="8528f-208">ชนิดคอนเทนเนอร์ 2:</span><span class="sxs-lookup"><span data-stu-id="8528f-208">Container type 2:</span></span>

        - <span data-ttu-id="8528f-209">**รหัสชนิดคอนเทนเนอร์:** *กล่อง-กลาง*</span><span class="sxs-lookup"><span data-stu-id="8528f-209">**Container type code:** *Box-Medium*</span></span>
        - <span data-ttu-id="8528f-210">**คำอธิบาย:** *กล่องขนาดกลาง*</span><span class="sxs-lookup"><span data-stu-id="8528f-210">**Description:** *Medium Box*</span></span>
        - <span data-ttu-id="8528f-211">**น้ำหนักสุทธิสูงสุด:** *50*</span><span class="sxs-lookup"><span data-stu-id="8528f-211">**Maximum net weight:** *50*</span></span>
        - <span data-ttu-id="8528f-212">**ปริมาตร:** *200*</span><span class="sxs-lookup"><span data-stu-id="8528f-212">**Volume:** *200*</span></span>
        - <span data-ttu-id="8528f-213">**ความยาว:** *2*</span><span class="sxs-lookup"><span data-stu-id="8528f-213">**Length:** *2*</span></span>
        - <span data-ttu-id="8528f-214">**ความกว้าง:** *10*</span><span class="sxs-lookup"><span data-stu-id="8528f-214">**Width:** *10*</span></span>
        - <span data-ttu-id="8528f-215">**ความสูง:** *10*</span><span class="sxs-lookup"><span data-stu-id="8528f-215">**Height:** *10*</span></span>

    - <span data-ttu-id="8528f-216">ชนิดคอนเทนเนอร์ 3:</span><span class="sxs-lookup"><span data-stu-id="8528f-216">Container type 3:</span></span>

        - <span data-ttu-id="8528f-217">**รหัสชนิดคอนเทนเนอร์:** *กล่อง-เล็ก*</span><span class="sxs-lookup"><span data-stu-id="8528f-217">**Container type code:** *Box-Small*</span></span>
        - <span data-ttu-id="8528f-218">**คำอธิบาย:** *กล่องขนาดเล็ก*</span><span class="sxs-lookup"><span data-stu-id="8528f-218">**Description:** *Small Box*</span></span>
        - <span data-ttu-id="8528f-219">**น้ำหนักสุทธิสูงสุด:** *20*</span><span class="sxs-lookup"><span data-stu-id="8528f-219">**Maximum net weight:** *20*</span></span>
        - <span data-ttu-id="8528f-220">**ปริมาตร:** *100*</span><span class="sxs-lookup"><span data-stu-id="8528f-220">**Volume:** *100*</span></span>
        - <span data-ttu-id="8528f-221">**ความยาว:** *1*</span><span class="sxs-lookup"><span data-stu-id="8528f-221">**Length:** *1*</span></span>
        - <span data-ttu-id="8528f-222">**ความกว้าง:** *10*</span><span class="sxs-lookup"><span data-stu-id="8528f-222">**Width:** *10*</span></span>
        - <span data-ttu-id="8528f-223">**ความสูง:** *10*</span><span class="sxs-lookup"><span data-stu-id="8528f-223">**Height:** *10*</span></span>

### <a name="inspect-or-create-container-groups"></a><span data-ttu-id="8528f-224">ตรวจสอบหรือสร้างกลุ่มคอนเทนเนอร์</span><span class="sxs-lookup"><span data-stu-id="8528f-224">Inspect or create container groups</span></span>

<span data-ttu-id="8528f-225">หากต้องการตรวจสอบกลุ่มคอนเทนเนอร์ของคุณ หรือสร้างกลุ่มคอนเทนเนอร์ใหม่หากคอนเทนเนอร์กลุ่มใดที่ต้องการ ให้ปฏิบัติตามขั้นตอนเหล่านี้</span><span class="sxs-lookup"><span data-stu-id="8528f-225">To inspect your container groups, or to create new container groups if they are required, follow these steps.</span></span>

1. <span data-ttu-id="8528f-226">ไปที่ **การจัดการคลังสินค้า** \> **การตั้งค่า** \> **ตู้บรรจุสินค้า** \> **กลุ่มตู้บรรจุสินค้า**</span><span class="sxs-lookup"><span data-stu-id="8528f-226">Go to **Warehouse management** \> **Setup** \> **Containers** \> **Container groups**.</span></span>
1. <span data-ttu-id="8528f-227">ตรวจสอบให้แน่ใจว่ากลุ่มคอนเทนเนอร์ต่อไปนี้พร้อมใช้งานในข้อมูลสาธิตของคุณ</span><span class="sxs-lookup"><span data-stu-id="8528f-227">Make sure that the following container group is available in your demo data.</span></span> <span data-ttu-id="8528f-228">ถ้าไม่มีอยู่ ให้เลือก **สร้าง** เพื่อสร้าง</span><span class="sxs-lookup"><span data-stu-id="8528f-228">If it isn't available, select **New** to create it.</span></span>

    - <span data-ttu-id="8528f-229">**รหัสกลุ่มคอนเทนเนอร์:** *กล่อง*</span><span class="sxs-lookup"><span data-stu-id="8528f-229">**Container group ID:** *Boxes*</span></span>
    - <span data-ttu-id="8528f-230">**คำอธิบาย:** *ขนาดกล่อง*</span><span class="sxs-lookup"><span data-stu-id="8528f-230">**Description:** *Box sizes*</span></span>

1. <span data-ttu-id="8528f-231">บนแท็บด่วน **รายละเอียด** ตัวอย่างเช่น กลุ่มคอนเทนเนอร์ *กล่อง* ให้ตรวจสอบให้แน่ใจว่ามีรายการต่อไปนี้อยู่</span><span class="sxs-lookup"><span data-stu-id="8528f-231">On the **Details** FastTab for the *Boxes* container group, make sure that the following lines exist.</span></span> <span data-ttu-id="8528f-232">ถ้าไม่มีให้เลือก **สร้าง** เพื่อเพิ่ม</span><span class="sxs-lookup"><span data-stu-id="8528f-232">If they don't, select **New** to add them.</span></span>

    - <span data-ttu-id="8528f-233">บรรทัดที่ 1:</span><span class="sxs-lookup"><span data-stu-id="8528f-233">Line 1:</span></span>

        - <span data-ttu-id="8528f-234">**หมายเลขลำดับ:** *1*</span><span class="sxs-lookup"><span data-stu-id="8528f-234">**Sequence number:** *1*</span></span>
        - <span data-ttu-id="8528f-235">**ชนิดคอนเทนเนอร์:** *กล่อง-ใหญ่*</span><span class="sxs-lookup"><span data-stu-id="8528f-235">**Container type:** *Box-Large*</span></span>
        - <span data-ttu-id="8528f-236">**เปอร์เซ็นต์การใช้คอนเทนเนอร์:** *100*</span><span class="sxs-lookup"><span data-stu-id="8528f-236">**Container utilization percentage:** *100*</span></span>

    - <span data-ttu-id="8528f-237">บรรทัดที่ 2:</span><span class="sxs-lookup"><span data-stu-id="8528f-237">Line 2:</span></span>

        - <span data-ttu-id="8528f-238">**หมายเลขลำดับ:** *2*</span><span class="sxs-lookup"><span data-stu-id="8528f-238">**Sequence number:** *2*</span></span>
        - <span data-ttu-id="8528f-239">**ชนิดคอนเทนเนอร์:** *กล่อง-กลาง*</span><span class="sxs-lookup"><span data-stu-id="8528f-239">**Container type:** *Box-Medium*</span></span>
        - <span data-ttu-id="8528f-240">**เปอร์เซ็นต์การใช้คอนเทนเนอร์:** *100*</span><span class="sxs-lookup"><span data-stu-id="8528f-240">**Container utilization percentage:** *100*</span></span>

    - <span data-ttu-id="8528f-241">บรรทัดที่ 3:</span><span class="sxs-lookup"><span data-stu-id="8528f-241">Line 3:</span></span>

        - <span data-ttu-id="8528f-242">**หมายเลขลำดับ:** *3*</span><span class="sxs-lookup"><span data-stu-id="8528f-242">**Sequence number:** *3*</span></span>
        - <span data-ttu-id="8528f-243">**ชนิดคอนเทนเนอร์:** *กล่อง-เล็ก*</span><span class="sxs-lookup"><span data-stu-id="8528f-243">**Container type:** *Box-Small*</span></span>
        - <span data-ttu-id="8528f-244">**เปอร์เซ็นต์การใช้คอนเทนเนอร์:** *100*</span><span class="sxs-lookup"><span data-stu-id="8528f-244">**Container utilization percentage:** *100*</span></span>

### <a name="create-a-new-container-build-template"></a><span data-ttu-id="8528f-245">สร้าแม่แบบการสร้างคอนเทนเนอร์ใหม่</span><span class="sxs-lookup"><span data-stu-id="8528f-245">Create a new container build template</span></span>

<span data-ttu-id="8528f-246">ในการสร้างแม่แบบการสร้างคอนเทนเนอร์ใหม่ ทำตามขั้นตอนเหล่านี้</span><span class="sxs-lookup"><span data-stu-id="8528f-246">To create a new container build template, follow these steps.</span></span>

1. <span data-ttu-id="8528f-247">ไปที่ **การจัดการคลังสินค้า** \> **การตั้งค่า** \> **ตู้บรรจุสินค้า** \> **แม่แบบการสร้างตู้บรรจุสินค้า**</span><span class="sxs-lookup"><span data-stu-id="8528f-247">Go to **Warehouse management** \> **Setup** \> **Containers** \> **Container build template**.</span></span>
1. <span data-ttu-id="8528f-248">เลือก **สร้าง** เพื่อสร้างแม่แบบการสร้างคอนเทนเนอร์ที่มีการตั้งค่าต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="8528f-248">Select **New** to create a container build template that has the following settings:</span></span>

    - <span data-ttu-id="8528f-249">**หมายเลขลำดับ:** *1*</span><span class="sxs-lookup"><span data-stu-id="8528f-249">**Sequence number:** *1*</span></span>
    - <span data-ttu-id="8528f-250">**รหัสแม่แบบคอนเทนเนอร์:** *กล่อง*</span><span class="sxs-lookup"><span data-stu-id="8528f-250">**Container template ID:** *Box*</span></span>
    - <span data-ttu-id="8528f-251">**รหัสกลุ่มคอนเทนเนอร์:** *กล่อง*</span><span class="sxs-lookup"><span data-stu-id="8528f-251">**Container group ID:** *Boxes*</span></span>
    - <span data-ttu-id="8528f-252">**ชนิดการสอบถามพื้นฐาน:** *รายการปันส่วนการขาย*</span><span class="sxs-lookup"><span data-stu-id="8528f-252">**Base query types:** *Sales allocation line*</span></span>
    - <span data-ttu-id="8528f-253">**รหัสขั้นตอนของเวฟ:** *234*</span><span class="sxs-lookup"><span data-stu-id="8528f-253">**Wave step code:** *234*</span></span>
    - <span data-ttu-id="8528f-254">**อนุญาตให้แบ่งการเบิกสินค้าได้:** *ใช่*</span><span class="sxs-lookup"><span data-stu-id="8528f-254">**Allow split picks:** *Yes*</span></span>
    - <span data-ttu-id="8528f-255">**กลยุทธ์การบรรจุคอนเทนเนอร์:** *บรรจุลงในคอนเทนเนอร์ปัจจุบันเท่านั้น*</span><span class="sxs-lookup"><span data-stu-id="8528f-255">**Container packing strategy:** *Pack into current container only*</span></span>
    - <span data-ttu-id="8528f-256">**บรรจุตามหน่วยคำสั่ง:** *ไม่*</span><span class="sxs-lookup"><span data-stu-id="8528f-256">**Pack by directive unit:** *No*</span></span>

1. <span data-ttu-id="8528f-257">ขณะที่ยังคงเลือกแถวสำหรับแม่แบบใหม่อยู่ ให้เลือก **แก้ไขการสอบถาม** ในบานหน้าต่างการดำเนินการ</span><span class="sxs-lookup"><span data-stu-id="8528f-257">While the row for the new template is still selected, select **Edit query** on the Action Pane.</span></span>
1. <span data-ttu-id="8528f-258">กล่องโต้ตอบตัวแก้ไขการสอบถามมาตรฐานจะปรากฏขึ้น</span><span class="sxs-lookup"><span data-stu-id="8528f-258">A standard query editor dialog box appears.</span></span> <span data-ttu-id="8528f-259">บนแท็บ **การเรียงลำดับ** เลือก **เพิ่ม** เพื่อเพิ่มแถวที่มีการตั้งค่าต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="8528f-259">On the **Sorting** tab, select **Add** to add a row that has the following settings:</span></span>

    - <span data-ttu-id="8528f-260">**ตาราง:** *ธุรกรรมงานชั่วคราว*</span><span class="sxs-lookup"><span data-stu-id="8528f-260">**Table:** *Temporary work transactions*</span></span>
    - <span data-ttu-id="8528f-261">**ตารางที่ได้รับมา:** *ธุรกรรมงานชั่วคราว*</span><span class="sxs-lookup"><span data-stu-id="8528f-261">**Derived table:** *Temporary work transactions*</span></span>
    - <span data-ttu-id="8528f-262">**ฟิลด์:** *หมายเลขใบสั่ง*</span><span class="sxs-lookup"><span data-stu-id="8528f-262">**Field:** *Order number*</span></span>
    - <span data-ttu-id="8528f-263">**แนวทางการค้นหา:** *การเรียงจากน้อยไปมาก*</span><span class="sxs-lookup"><span data-stu-id="8528f-263">**Search direction:** *Ascending*</span></span>

    > [!IMPORTANT]
    > <span data-ttu-id="8528f-264">เพื่อหลีกเลี่ยงการหมุนเวียนคอนเทนเนอร์ที่เปิดอยู่ทั้งหมด และเพื่อเพิ่มความเร็วของกระบวนการด้วยการตรวจสอบคอนเทนเนอร์หนึ่งคอนเทนเนอร์ในครั้งหนึ่งๆ ให้ใช้กลยุทธ์ *บรรจุสินค้าลงในคอนเทนเนอร์ปัจจุบัน* นอกเหนือจากการเรียงลำดับตามหมายเลขใบสั่ง</span><span class="sxs-lookup"><span data-stu-id="8528f-264">To avoid cycling over all the other open containers, and to speed up the process by checking one container at a time, use the *Pack into current container only* strategy in addition to sorting by order number.</span></span> <span data-ttu-id="8528f-265">ชุดข้อมูลนี้จะเหมือนหยุดพักงานในแม่แบบงาน</span><span class="sxs-lookup"><span data-stu-id="8528f-265">This combination will work like a work break on a work template.</span></span>

1. <span data-ttu-id="8528f-266">เลือก **ตกลง** เพื่อปิดกล่องโต้ตอบตัวแก้ไขการสอบถาม</span><span class="sxs-lookup"><span data-stu-id="8528f-266">Select **OK** to close the query editor dialog box.</span></span>
1. <span data-ttu-id="8528f-267">ขณะที่ยังคงเลือกแถวสำหรับแม่แบบใหม่อยู่ ให้เลือก **ข้อจำกัดการผสมของคอนเทนเนอร์** ในบานหน้าต่างการดำเนินการ</span><span class="sxs-lookup"><span data-stu-id="8528f-267">While the row for the new template is still selected, select **Container mixing constraints** on the Action Pane.</span></span>

    <span data-ttu-id="8528f-268">ขณะนี้คุณจะเพิ่มข้อจากใบสั่งหนึ่งๆ ลงในคอนเทนเนอร์เดียว</span><span class="sxs-lookup"><span data-stu-id="8528f-268">You will now add a constraint that puts items from a single order into a single container.</span></span> <span data-ttu-id="8528f-269">สินค้าจากใบสั่งอื่นใดจะถูกวางลงในคอนเทนเนอร์แยกต่างหาก</span><span class="sxs-lookup"><span data-stu-id="8528f-269">Items from any other order will be put into a separate container.</span></span>

1. <span data-ttu-id="8528f-270">เลือก **สร้าง** เพื่อสร้างข้อจำกัดการผสมที่มีการตั้งค่าต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="8528f-270">Select **New** to create a mixing constraint that has the following settings:</span></span>

    - <span data-ttu-id="8528f-271">**ตาราง:** *ใบสั่งขาย*</span><span class="sxs-lookup"><span data-stu-id="8528f-271">**Table:** *Sales orders*</span></span>
    - <span data-ttu-id="8528f-272">**ฟิลด์ที่เลือก:** *SalesId* (ฟิลด์จะปรากฏเป็น *ใบสั่งขาย* ในกริด)</span><span class="sxs-lookup"><span data-stu-id="8528f-272">**Field select:** *SalesId* (The field will appear as *Sales order* in the grid.)</span></span>

1. <span data-ttu-id="8528f-273">เลือก **ตกลง** เพื่อเพิ่มข้อจำกัด</span><span class="sxs-lookup"><span data-stu-id="8528f-273">Select **OK** to add the constraint.</span></span>
1. <span data-ttu-id="8528f-274">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="8528f-274">Close the page.</span></span>

### <a name="set-up-a-wave-template-for-containerization"></a><span data-ttu-id="8528f-275">ตั้งค่าเท็มเพลตเวฟสำหรับการบรรจุลงตู้บรรจุสินค้า</span><span class="sxs-lookup"><span data-stu-id="8528f-275">Set up a wave template for containerization</span></span>

<span data-ttu-id="8528f-276">ในการตั้งค่าแม่แบบเวฟ ทำตามขั้นตอนเหล่านี้</span><span class="sxs-lookup"><span data-stu-id="8528f-276">To set up a wave template, follow these steps.</span></span>

1. <span data-ttu-id="8528f-277">ไปที่ **การจัดการคลังสินค้า \> การตั้งค่า \> เวฟ \> เท็มเพลตเวฟ**</span><span class="sxs-lookup"><span data-stu-id="8528f-277">Go to **Warehouse management \> Setup \> Waves \> Wave templates**.</span></span>
1. <span data-ttu-id="8528f-278">ในบานหน้าต่างรายการ ตั้งค่าฟิลด์ **ชนิดแม่แบบเวฟ** เป็น *การจัดส่งสินค้า*</span><span class="sxs-lookup"><span data-stu-id="8528f-278">In the list pane, set the **Wave template type** field to *Shipping*.</span></span>
1. <span data-ttu-id="8528f-279">เลือกแม่แบบ **การบรรจุลงตู้บรรจุสินค้า 63** ในรายการ</span><span class="sxs-lookup"><span data-stu-id="8528f-279">Select the **63 Containerization** template in the list.</span></span>
1. <span data-ttu-id="8528f-280">บนบานหน้าต่างการดำเนินการ เลือก **แก้ไข**</span><span class="sxs-lookup"><span data-stu-id="8528f-280">On the Action Pane, select **Edit**.</span></span>
1. <span data-ttu-id="8528f-281">บนแท็บด่วน **วิธีการ** ในคอลัมน์ **วิธีการที่เลือก** ให้ค้นหารายการต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="8528f-281">On the **Methods** FastTab, in the **Selected methods** column, find the following line:</span></span>

    - <span data-ttu-id="8528f-282">**ชื่อวิธีการ:** *คอนเทนเนอร์*</span><span class="sxs-lookup"><span data-stu-id="8528f-282">**Method name:** *containerization*</span></span>
    - <span data-ttu-id="8528f-283">**ชื่อ:** *การบรรจุลงตู้บรรจุสินค้า*</span><span class="sxs-lookup"><span data-stu-id="8528f-283">**Name:** *Containerization*</span></span>

1. <span data-ttu-id="8528f-284">ตั้งค่าฟิลด์ **รหัสขั้นตอนของเวฟ** สำหรับรายการนี้ไปที่ *234*</span><span class="sxs-lookup"><span data-stu-id="8528f-284">Set the **Wave step code** field for the line to *234*.</span></span>

### <a name="set-up-a-work-template"></a><span data-ttu-id="8528f-285">ตั้งค่าเท็มเพลตงาน</span><span class="sxs-lookup"><span data-stu-id="8528f-285">Set up a work template</span></span>

<span data-ttu-id="8528f-286">ในการตั้งค่าแม่แบบงาน ทำตามขั้นตอนเหล่านี้</span><span class="sxs-lookup"><span data-stu-id="8528f-286">To set up a work template, follow these steps.</span></span>

1. <span data-ttu-id="8528f-287">ไปที่ **การจัดการคลังสินค้า \> การตั้งค่า \> งาน \> เท็มเพลตงาน**</span><span class="sxs-lookup"><span data-stu-id="8528f-287">Go to **Warehouse management \> Setup \> Work \> Work templates**.</span></span>
1. <span data-ttu-id="8528f-288">ตั้งค่าฟิลด์ **ชนิดใบสั่งงาน** เป็น *ใบสั่งขาย*</span><span class="sxs-lookup"><span data-stu-id="8528f-288">Set the **Work order type** field to *Sales orders*.</span></span>
1. <span data-ttu-id="8528f-289">ในกริด **ภาพรวม** ให้ค้นหาและเลือกแม่แบบงานที่ควรใช้สำหรับการบรรจุใบสั่งเดี่ยวต่อคอนเทนเนอร์</span><span class="sxs-lookup"><span data-stu-id="8528f-289">In the **Overview** grid, find and select the work template that should be used for packing single orders per container.</span></span> <span data-ttu-id="8528f-290">สำหรับสถานการณ์นี้ เลือกแม่แบบ **63 คอนเทนเนอร์การเบิกสินค้า**</span><span class="sxs-lookup"><span data-stu-id="8528f-290">For this scenario, select the **63 Pick to container** template.</span></span>
1. <span data-ttu-id="8528f-291">บนบานหน้าต่างการดำเนินการ เลือก **แก้ไขการสอบถาม**</span><span class="sxs-lookup"><span data-stu-id="8528f-291">On the Action Pane, select **Edit query**.</span></span>
1. <span data-ttu-id="8528f-292">กล่องโต้ตอบตัวแก้ไขการสอบถามมาตรฐานจะปรากฏขึ้น</span><span class="sxs-lookup"><span data-stu-id="8528f-292">A standard query editor dialog box appears.</span></span> <span data-ttu-id="8528f-293">บนแท็บ **การเรียงลำดับ** เพิ่มรายการต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="8528f-293">On the **Sorting** tab, add the following lines:</span></span>

    - <span data-ttu-id="8528f-294">บรรทัดที่ 1:</span><span class="sxs-lookup"><span data-stu-id="8528f-294">Line 1:</span></span>

        - <span data-ttu-id="8528f-295">**ตาราง:** *ธุรกรรมงานชั่วคราว*</span><span class="sxs-lookup"><span data-stu-id="8528f-295">**Table:** *Temporary work transactions*</span></span>
        - <span data-ttu-id="8528f-296">**ตารางที่ได้รับมา:** *ธุรกรรมงานชั่วคราว*</span><span class="sxs-lookup"><span data-stu-id="8528f-296">**Derived table:** *Temporary work transactions*</span></span>
        - <span data-ttu-id="8528f-297">**ฟิลด์:** *รหัสการจัดส่ง*</span><span class="sxs-lookup"><span data-stu-id="8528f-297">**Field:** *Shipment ID*</span></span>
        - <span data-ttu-id="8528f-298">**แนวทางการค้นหา:** *การเรียงจากน้อยไปมาก*</span><span class="sxs-lookup"><span data-stu-id="8528f-298">**Search direction:** *Ascending*</span></span>

    - <span data-ttu-id="8528f-299">บรรทัดที่ 2:</span><span class="sxs-lookup"><span data-stu-id="8528f-299">Line 2:</span></span>

        - <span data-ttu-id="8528f-300">**ตาราง:** *ธุรกรรมงานชั่วคราว*</span><span class="sxs-lookup"><span data-stu-id="8528f-300">**Table:** *Temporary work transactions*</span></span>
        - <span data-ttu-id="8528f-301">**ตารางที่ได้รับมา:** *ธุรกรรมงานชั่วคราว*</span><span class="sxs-lookup"><span data-stu-id="8528f-301">**Derived table:** *Temporary work transactions*</span></span>
        - <span data-ttu-id="8528f-302">**ฟิลด์:** *หมายเลขใบสั่ง*</span><span class="sxs-lookup"><span data-stu-id="8528f-302">**Field:** *Order number*</span></span>
        - <span data-ttu-id="8528f-303">**แนวทางการค้นหา:** *การเรียงจากน้อยไปมาก*</span><span class="sxs-lookup"><span data-stu-id="8528f-303">**Search direction:** *Ascending*</span></span>

    - <span data-ttu-id="8528f-304">บรรทัดที่ 3:</span><span class="sxs-lookup"><span data-stu-id="8528f-304">Line 3:</span></span>

        - <span data-ttu-id="8528f-305">**ตาราง:** *ธุรกรรมงานชั่วคราว*</span><span class="sxs-lookup"><span data-stu-id="8528f-305">**Table:** *Temporary work transactions*</span></span>
        - <span data-ttu-id="8528f-306">**ตารางที่ได้รับมา:** *ธุรกรรมงานชั่วคราว*</span><span class="sxs-lookup"><span data-stu-id="8528f-306">**Derived table:** *Temporary work transactions*</span></span>
        - <span data-ttu-id="8528f-307">**ฟิลด์:** *รหัสคอนเทนเนอร์*</span><span class="sxs-lookup"><span data-stu-id="8528f-307">**Field:** *Container ID*</span></span>
        - <span data-ttu-id="8528f-308">**แนวทางการค้นหา:** *การเรียงจากน้อยไปมาก*</span><span class="sxs-lookup"><span data-stu-id="8528f-308">**Search direction:** *Ascending*</span></span>

1. <span data-ttu-id="8528f-309">เลือก **ตกลง** เพื่อปิดกล่องโต้ตอบตัวแก้ไขการสอบถาม</span><span class="sxs-lookup"><span data-stu-id="8528f-309">Select **OK** to close the query editor dialog box.</span></span>
1. <span data-ttu-id="8528f-310">คุณจะได้รับข้อความแสดงข้อความต่อไปนี้: "การจัดกลุ่มจะถูกรีเซ็ต ดำเนินการต่อหรือไม่"</span><span class="sxs-lookup"><span data-stu-id="8528f-310">You receive the following message: "Grouping will be reset, continue?"</span></span> <span data-ttu-id="8528f-311">เลือก **ใช่** เพื่อดำเนินการต่อ</span><span class="sxs-lookup"><span data-stu-id="8528f-311">Select **Yes** to continue.</span></span>
1. <span data-ttu-id="8528f-312">ในขณะที่เลือกแม่แบบ **63 คอนเทนเนอร์การเบิกสินค้า** ให้เลือก **การแบ่งหัวข้องาน** ในบานหน้าต่างการดำเนินการ</span><span class="sxs-lookup"><span data-stu-id="8528f-312">While the **63 Pick to container** template is still selected, select **Work header breaks** on the Action Pane.</span></span>

    <span data-ttu-id="8528f-313">ขณะนี้คุณจะใช้การตั้งค่าเพื่อแบ่งงานเพื่อให้แต่คอนเทนเนอร์ในลำดับที่เชื่อมโยงกับใบสั่งงานหนึ่งรายการ</span><span class="sxs-lookup"><span data-stu-id="8528f-313">You will now apply settings to break the work so that each container in the order is linked to one work order.</span></span>

1. <span data-ttu-id="8528f-314">เลือกกล่องกาเครื่องหมาย **จัดกลุ่มตามฟิลด์นี้** ให้กับแต่ละแถวบนหน้า **การแบ่งหัวข้องาน** (**รหัสการจัดส่ง** **หมายเลขใบสั่ง** และ **รหัสคอนเทนเนอร์**)</span><span class="sxs-lookup"><span data-stu-id="8528f-314">Select the **Group by this field** checkbox for each row on the **Work header breaks** page (**Shipment ID**, **Order number**, and **Container ID**).</span></span>
1. <span data-ttu-id="8528f-315">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="8528f-315">Close the page.</span></span>

### <a name="set-up-shipment-consolidation-policies"></a><span data-ttu-id="8528f-316">ตั้งค่านโยบายการรวมบัญชีการจัดส่ง</span><span class="sxs-lookup"><span data-stu-id="8528f-316">Set up shipment consolidation policies</span></span>

<span data-ttu-id="8528f-317">หากต้องการตั้งค่านโยบายการรวมบัญชีการจัดส่ง ให้ทำตามขั้นตอนเหล่านี้</span><span class="sxs-lookup"><span data-stu-id="8528f-317">To set up a shipment consolidation policy, follow these steps.</span></span>

1. <span data-ttu-id="8528f-318">ไปที่ **การจัดการคลังสินค้า \> การตั้งค่า \> การนำออกใช้ไปยังคลังสินค้า \> นโยบายการรวมบัญชีการจัดส่ง**</span><span class="sxs-lookup"><span data-stu-id="8528f-318">Go to **Warehouse management \> Setup \> Release to warehouse \> Shipment consolidation policies**.</span></span>
1. <span data-ttu-id="8528f-319">ในบานหน้าต่างรายการ ให้ตั้งค่าฟิลด์ **ชนิดนโยบาย** เป็น *ใบสั่งขาย*</span><span class="sxs-lookup"><span data-stu-id="8528f-319">In the list pane, set the **Policy type** field to *Sales orders*.</span></span>
1. <span data-ttu-id="8528f-320">เลือกนโยบาย **เริ่มต้น** ในรายการ</span><span class="sxs-lookup"><span data-stu-id="8528f-320">Select the **Default** policy in the list.</span></span>
1. <span data-ttu-id="8528f-321">บนบานหน้าต่างการดำเนินการ เลือก **แก้ไข**</span><span class="sxs-lookup"><span data-stu-id="8528f-321">On the Action Pane, select **Edit**.</span></span>
1. <span data-ttu-id="8528f-322">บน FastTab **ฟิลด์การรวมบัญชี** ในรายการ **ฟิลด์ที่เลือก** ให้เลือกแถวที่ฟิลด์ **ชื่อฟิลด์** ถูกตั้งค่าเป็น *หมายเลขใบสั่ง*</span><span class="sxs-lookup"><span data-stu-id="8528f-322">On the **Consolidation fields** FastTab, in the **Selected fields** list, select the row where the **Field name** field is set to *Order number*.</span></span>
1. <span data-ttu-id="8528f-323">เลือกปุ่ม **เอาออก** ![ลูกศรซ้าย](media/backward-button.png) เพื่อย้ายฟิลด์ไปยังรายการ **ฟิลด์ที่เหลือ**</span><span class="sxs-lookup"><span data-stu-id="8528f-323">Select the **Remove** button ![Left arrow](media/backward-button.png) to move the field to the **Remaining fields** list.</span></span>
1. <span data-ttu-id="8528f-324">บนบานหน้าต่างการดำเนินการ เลือก **บันทึก**</span><span class="sxs-lookup"><span data-stu-id="8528f-324">On the Action Pane, select **Save**.</span></span>

### <a name="set-up-physical-dimensions-for-the-product"></a><span data-ttu-id="8528f-325">ตั้งค่ามิติทางกายภาพสำหรับผลิตภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="8528f-325">Set up physical dimensions for the product</span></span>

<span data-ttu-id="8528f-326">หากต้องการตั้งค่ามิติทางกายภาพให้กับผลิตภัณฑ์ที่จะใช้ในสถานการณ์นี้ ให้ปฏิบัติตามขั้นตอนต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="8528f-326">To set up physical dimensions for the products that will be used in this scenario, follow these steps.</span></span>

1. <span data-ttu-id="8528f-327">ไปยัง **การจัดการข้อมูลผลิตภัณฑ์ \> ผลิตภัณฑ์ \> ผลิตภัณฑ์ที่นำออกใช้**</span><span class="sxs-lookup"><span data-stu-id="8528f-327">Go to **Product information management \> Products \> Released products**.</span></span>
1. <span data-ttu-id="8528f-328">เลือกผลิตภัณฑ์ที่มีการตั้งค่าฟิลด์ **หมายเลขสินค้า** เป็น *A0001*</span><span class="sxs-lookup"><span data-stu-id="8528f-328">Select the product where the **Item number** field is set to *A0001*.</span></span>
1. <span data-ttu-id="8528f-329">บนบานหน้าต่างการดำเนินการ บนแท็บ **จัดการสินค้าคงคลัง** ในกลุ่ม **คลังสินค้า** เลือก **มิติทางกายภาพ**</span><span class="sxs-lookup"><span data-stu-id="8528f-329">On the Action Pane, on the **Manage inventory** tab, in the **Warehouse** group, select **Physical dimensions**.</span></span>
1. <span data-ttu-id="8528f-330">บนหน้า **มิติทางกายภาพ** คุณควรจะเห็นรายการต่อไปนี้ในกริด:</span><span class="sxs-lookup"><span data-stu-id="8528f-330">On the **Physical dimensions** page, you should see the following line in the grid:</span></span>

    - <span data-ttu-id="8528f-331">**หน่วย:** *ชิ้น*</span><span class="sxs-lookup"><span data-stu-id="8528f-331">**Unit:** *pcs*</span></span>
    - <span data-ttu-id="8528f-332">**น้ำหนักรวม:** *3.00*</span><span class="sxs-lookup"><span data-stu-id="8528f-332">**Gross weight:** *3.00*</span></span>
    - <span data-ttu-id="8528f-333">**ความกว้าง:** *2.00*</span><span class="sxs-lookup"><span data-stu-id="8528f-333">**Width:** *2.00*</span></span>
    - <span data-ttu-id="8528f-334">**ความลึก:** *2.00*</span><span class="sxs-lookup"><span data-stu-id="8528f-334">**Depth:** *2.00*</span></span>
    - <span data-ttu-id="8528f-335">**ความสูง:** *4.00*</span><span class="sxs-lookup"><span data-stu-id="8528f-335">**Height:** *4.00*</span></span>
    - <span data-ttu-id="8528f-336">**ปริมาตร:** *16.00*</span><span class="sxs-lookup"><span data-stu-id="8528f-336">**Volume:** *16.00*</span></span>

1. <span data-ttu-id="8528f-337">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="8528f-337">Close the page.</span></span>
1. <span data-ttu-id="8528f-338">เลือกผลิตภัณฑ์ที่มีการตั้งค่าฟิลด์ **หมายเลขสินค้า** เป็น *A0002*</span><span class="sxs-lookup"><span data-stu-id="8528f-338">Select the product where the **Item number** field is set to *A0002*.</span></span>
1. <span data-ttu-id="8528f-339">บนบานหน้าต่างการดำเนินการ บนแท็บ **จัดการสินค้าคงคลัง** ในกลุ่ม **คลังสินค้า** เลือก **มิติทางกายภาพ**</span><span class="sxs-lookup"><span data-stu-id="8528f-339">On the Action Pane, on the **Manage inventory** tab, in the **Warehouse** group, select **Physical dimensions**.</span></span>
1. <span data-ttu-id="8528f-340">บนหน้า **มิติทางกายภาพ** คุณควรจะเห็นรายการต่อไปนี้ในกริด:</span><span class="sxs-lookup"><span data-stu-id="8528f-340">On the **Physical dimensions** page, you should see the following line in the grid:</span></span>

    - <span data-ttu-id="8528f-341">**หน่วย:** *ชิ้น*</span><span class="sxs-lookup"><span data-stu-id="8528f-341">**Unit:** *pcs*</span></span>
    - <span data-ttu-id="8528f-342">**น้ำหนักรวม:** *4.00*</span><span class="sxs-lookup"><span data-stu-id="8528f-342">**Gross weight:** *4.00*</span></span>
    - <span data-ttu-id="8528f-343">**ความกว้าง:** *3.00*</span><span class="sxs-lookup"><span data-stu-id="8528f-343">**Width:** *3.00*</span></span>
    - <span data-ttu-id="8528f-344">**ความลึก:** *1.00*</span><span class="sxs-lookup"><span data-stu-id="8528f-344">**Depth:** *1.00*</span></span>
    - <span data-ttu-id="8528f-345">**ความสูง:** *3.00*</span><span class="sxs-lookup"><span data-stu-id="8528f-345">**Height:** *3.00*</span></span>
    - <span data-ttu-id="8528f-346">**ปริมาตร:** *9.00*</span><span class="sxs-lookup"><span data-stu-id="8528f-346">**Volume:** *9.00*</span></span>

### <a name="create-sales-order-1"></a><span data-ttu-id="8528f-347">สร้างใบสั่งขาย 1</span><span class="sxs-lookup"><span data-stu-id="8528f-347">Create sales order 1</span></span>

<span data-ttu-id="8528f-348">ในการสร้างใบสั่งขาย ให้ปฏิบัติตามขั้นตอนเหล่านี้</span><span class="sxs-lookup"><span data-stu-id="8528f-348">To create a sales order, follow these steps.</span></span>

1. <span data-ttu-id="8528f-349">ไปยัง **การขายและการตลาด \> ใบสั่งขาย \> ใบสั่งขายทั้งหมด**</span><span class="sxs-lookup"><span data-stu-id="8528f-349">Go to **Sales and marketing \> Sales orders \> All sales orders**.</span></span>
1. <span data-ttu-id="8528f-350">บนบานหน้าต่างการดำเนินการ เลือก **สร้าง**</span><span class="sxs-lookup"><span data-stu-id="8528f-350">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="8528f-351">กล่องโต้ตอบเกี่ยวกับการสร้างใบสั่งขายใหม่จะปรากฏขึ้น</span><span class="sxs-lookup"><span data-stu-id="8528f-351">A dialog box for creating a new sales order appears.</span></span> <span data-ttu-id="8528f-352">ตั้งค่าดังต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="8528f-352">Set the following values:</span></span>

    - <span data-ttu-id="8528f-353">**บัญชีลูกค้า:** *US-001*</span><span class="sxs-lookup"><span data-stu-id="8528f-353">**Customer account:** *US-001*</span></span>
    - <span data-ttu-id="8528f-354">**คลังสินค้า:** *63*</span><span class="sxs-lookup"><span data-stu-id="8528f-354">**Warehouse:** *63*</span></span>

1. <span data-ttu-id="8528f-355">เลือก **ตกลง** เพื่อสร้างใบสั่งขาย และปิดกล่องโต้ตอบ</span><span class="sxs-lookup"><span data-stu-id="8528f-355">Select **OK** to create the sales order and close the dialog box.</span></span>
1. <span data-ttu-id="8528f-356">มีการเปิดใบสั่งขายใหม่</span><span class="sxs-lookup"><span data-stu-id="8528f-356">The new sales order is opened.</span></span> <span data-ttu-id="8528f-357">บนแท็บด่วน **รายการใบสั่งขาย** เพิ่มรายการขายต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="8528f-357">On the **Sales order lines** FastTab, add the following sales lines:</span></span>

    - <span data-ttu-id="8528f-358">บรรทัดที่ 1:</span><span class="sxs-lookup"><span data-stu-id="8528f-358">Line 1:</span></span>

        - <span data-ttu-id="8528f-359">**หมายเลขสินค้า:** *A0001*</span><span class="sxs-lookup"><span data-stu-id="8528f-359">**Item number:** *A0001*</span></span>
        - <span data-ttu-id="8528f-360">**ปริมาณ:** *2*</span><span class="sxs-lookup"><span data-stu-id="8528f-360">**Quantity:** *2*</span></span>

    - <span data-ttu-id="8528f-361">บรรทัดที่ 2:</span><span class="sxs-lookup"><span data-stu-id="8528f-361">Line 2:</span></span>

        - <span data-ttu-id="8528f-362">**หมายเลขสินค้า:** *A0002*</span><span class="sxs-lookup"><span data-stu-id="8528f-362">**Item number:** *A0002*</span></span>
        - <span data-ttu-id="8528f-363">**ปริมาณ:** *2*</span><span class="sxs-lookup"><span data-stu-id="8528f-363">**Quantity:** *2*</span></span>

1. <span data-ttu-id="8528f-364">เลือกรายการแรก แล้วเลือก **สินค้าคงคลัง \> การจอง**</span><span class="sxs-lookup"><span data-stu-id="8528f-364">Select the first line, and then select **Inventory \> Reservation**.</span></span>
1. <span data-ttu-id="8528f-365">บนหน้า **การจองสินค้า** ให้เลือก **จองล็อต**</span><span class="sxs-lookup"><span data-stu-id="8528f-365">On the **Reservation** page, select **Reserve lot**.</span></span> <span data-ttu-id="8528f-366">จากนั้น ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="8528f-366">Then close the page.</span></span>
1. <span data-ttu-id="8528f-367">ทําซ้ําสองขั้นตอนก่อนหน้านี้ของรายการที่สอง</span><span class="sxs-lookup"><span data-stu-id="8528f-367">Repeat the previous two steps for the second line.</span></span>
1. <span data-ttu-id="8528f-368">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="8528f-368">Close the page.</span></span>

### <a name="create-sales-order-2"></a><span data-ttu-id="8528f-369">สร้างใบสั่งขาย 2</span><span class="sxs-lookup"><span data-stu-id="8528f-369">Create sales order 2</span></span>

<span data-ttu-id="8528f-370">หากต้องการสร้างใบสั่งขายที่สอง ให้ทำตามขั้นตอนต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="8528f-370">To create a second sales order, follow these steps.</span></span>

1. <span data-ttu-id="8528f-371">ไปยัง **การขายและการตลาด \> ใบสั่งขาย \> ใบสั่งขายทั้งหมด**</span><span class="sxs-lookup"><span data-stu-id="8528f-371">Go to **Sales and marketing \> Sales orders \> All sales orders**.</span></span>
1. <span data-ttu-id="8528f-372">บนบานหน้าต่างการดำเนินการ เลือก **สร้าง**</span><span class="sxs-lookup"><span data-stu-id="8528f-372">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="8528f-373">กล่องโต้ตอบเกี่ยวกับการสร้างใบสั่งขายใหม่จะปรากฏขึ้น</span><span class="sxs-lookup"><span data-stu-id="8528f-373">A dialog box for creating a new sales order appears.</span></span> <span data-ttu-id="8528f-374">ตั้งค่าดังต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="8528f-374">Set the following values:</span></span>

    - <span data-ttu-id="8528f-375">**บัญชีลูกค้า:** *US-001*</span><span class="sxs-lookup"><span data-stu-id="8528f-375">**Customer account:** *US-001*</span></span>
    - <span data-ttu-id="8528f-376">**คลังสินค้า:** *63*</span><span class="sxs-lookup"><span data-stu-id="8528f-376">**Warehouse:** *63*</span></span>

1. <span data-ttu-id="8528f-377">เลือก **ตกลง** เพื่อสร้างใบสั่งขาย และปิดกล่องโต้ตอบ</span><span class="sxs-lookup"><span data-stu-id="8528f-377">Select **OK** to create the sales order and close the dialog box.</span></span>
1. <span data-ttu-id="8528f-378">มีการเปิดใบสั่งขายใหม่</span><span class="sxs-lookup"><span data-stu-id="8528f-378">The new sales order is opened.</span></span> <span data-ttu-id="8528f-379">บนแท็บด่วน **รายการใบสั่งขาย** เพิ่มรายการขายต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="8528f-379">On the **Sales order lines** FastTab, add the following sales lines:</span></span>

    - <span data-ttu-id="8528f-380">บรรทัดที่ 1:</span><span class="sxs-lookup"><span data-stu-id="8528f-380">Line 1:</span></span>

        - <span data-ttu-id="8528f-381">**หมายเลขสินค้า:** *A0001*</span><span class="sxs-lookup"><span data-stu-id="8528f-381">**Item number:** *A0001*</span></span>
        - <span data-ttu-id="8528f-382">**ปริมาณ:** *4*</span><span class="sxs-lookup"><span data-stu-id="8528f-382">**Quantity:** *4*</span></span>

    - <span data-ttu-id="8528f-383">บรรทัดที่ 2:</span><span class="sxs-lookup"><span data-stu-id="8528f-383">Line 2:</span></span>

        - <span data-ttu-id="8528f-384">**หมายเลขสินค้า:** *A0002*</span><span class="sxs-lookup"><span data-stu-id="8528f-384">**Item number:** *A0002*</span></span>
        - <span data-ttu-id="8528f-385">**ปริมาณ:** *4*</span><span class="sxs-lookup"><span data-stu-id="8528f-385">**Quantity:** *4*</span></span>

1. <span data-ttu-id="8528f-386">เลือกรายการแรก แล้วเลือก **สินค้าคงคลัง \> การจอง**</span><span class="sxs-lookup"><span data-stu-id="8528f-386">Select the first line, and then select **Inventory \> Reservation**.</span></span>
1. <span data-ttu-id="8528f-387">บนหน้า **การจองสินค้า** ให้เลือก **จองล็อต**</span><span class="sxs-lookup"><span data-stu-id="8528f-387">On the **Reservation** page, select **Reserve lot**.</span></span> <span data-ttu-id="8528f-388">จากนั้น ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="8528f-388">Then close the page.</span></span>
1. <span data-ttu-id="8528f-389">ทําซ้ําสองขั้นตอนก่อนหน้านี้ของรายการที่สอง</span><span class="sxs-lookup"><span data-stu-id="8528f-389">Repeat the previous two steps for the second line.</span></span>
1. <span data-ttu-id="8528f-390">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="8528f-390">Close the page.</span></span>

### <a name="create-the-load"></a><span data-ttu-id="8528f-391">สร้างจำนวนงานในศูนย์การผลิต</span><span class="sxs-lookup"><span data-stu-id="8528f-391">Create the load</span></span>

<span data-ttu-id="8528f-392">หากต้องการสร้างจำนวนงานในศูนย์การผลิตสำหรับใบสั่งแต่ละชุดที่คุณสร้างไว้สำหรับสถานการณ์จำลองนี้ และจากนั้น นำออกใช้ไปยังคลังสินค้า ทำตามขั้นตอนต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="8528f-392">To create a load for each order that you created for this scenario and then release it to the warehouse, follow these steps.</span></span>

1. <span data-ttu-id="8528f-393">ไปที่ **การจัดการคลังสินค้า \> จำนวนงานในศูนย์การผลิต \> เวิร์กเบนช์การวางแผนการบรรทุก**</span><span class="sxs-lookup"><span data-stu-id="8528f-393">Go to **Warehouse management \> Loads \> Load planning workbench**.</span></span>
1. <span data-ttu-id="8528f-394">บนแท็บ **รายการขาย** ให้ค้นหาและเลือกรายการใบสั่งขายทั้งหมดจาใบสั่งขายที่คุณสร้างขึ้นสำหรับสถานการณ์นี้</span><span class="sxs-lookup"><span data-stu-id="8528f-394">On the **Sales lines** tab, find and select all the sales order lines from the sales orders that you created for this scenario.</span></span>
1. <span data-ttu-id="8528f-395">บนบานหน้าต่างการดำเนินการ บนแท็บ **การจัดหาและความต้องการ** ในกลุ่ม **เพิ่ม** เลือก **ไปยังการบรรทุกใหม่**</span><span class="sxs-lookup"><span data-stu-id="8528f-395">On the Action Pane, on the **Supply and demand** tab, in the **Add** group, select **To new load**.</span></span> <span data-ttu-id="8528f-396">บรรทัดใบสั่งที่เลือกจะถูกเพิ่มไปยังโหลดใหม่</span><span class="sxs-lookup"><span data-stu-id="8528f-396">The selected order lines are added to a new load.</span></span>
1. <span data-ttu-id="8528f-397">ในกล่องโต้ตอบ **การกำหนดแม่แบบจำนวนงานในศูนย์การผลิต** ในฟิลด์ **รหัสแม่แบบจำนวนงานในศูนย์การผลิต** ให้เลือกแม่แบบจำนวนงานในศูนย์การผลิต เช่น *คอนเทนเนอร์ 40'*</span><span class="sxs-lookup"><span data-stu-id="8528f-397">In the **Load template assignment** dialog box, in the **Load template ID** field, select a load template, such as *40' Container*.</span></span>
1. <span data-ttu-id="8528f-398">เลือก **ตกลง** เพื่อปิดกล่องโต้ตอบ</span><span class="sxs-lookup"><span data-stu-id="8528f-398">Select **OK** to close the dialog box.</span></span>
1. <span data-ttu-id="8528f-399">ในส่วน **จำนวนงานในศูนย์การผลิต** และเลือกจำนวนงานในศูนย์การผลิตที่คุณเพิ่งสร้างขึ้น</span><span class="sxs-lookup"><span data-stu-id="8528f-399">In the **Loads** section, find and select the load that you just created.</span></span>
1. <span data-ttu-id="8528f-400">เลือก **นำออกใช้ \> นำออกใช้ที่คลังสินค้า**</span><span class="sxs-lookup"><span data-stu-id="8528f-400">Select **Release \> Release to warehouse**.</span></span>
1. <span data-ttu-id="8528f-401">ในกล่องโต้ตอบ **นำออกใช้ไปยังคลังสินค้า** เลือก **ตกลง** เพื่อนำจำนวนงานในศูนย์การผลิตที่เลือกออกใช้ไปยังคลังสินค้า</span><span class="sxs-lookup"><span data-stu-id="8528f-401">In the **Release to warehouse** dialog box, select **OK** to release the selected load to the warehouse.</span></span>

### <a name="verify-the-shipments-and-containers"></a><span data-ttu-id="8528f-402">ตรวจสอบการจัดส่งและคอนเทนเนอร์</span><span class="sxs-lookup"><span data-stu-id="8528f-402">Verify the shipments and containers</span></span>

<span data-ttu-id="8528f-403">ขั้นตอนต่อไปนี้จะช่วยให้คุณสามารถตรวจสอบการจัดส่งสินค้าที่สร้างขึ้นแล้วได้</span><span class="sxs-lookup"><span data-stu-id="8528f-403">The following procedure lets you verify the shipments that have been created.</span></span> <span data-ttu-id="8528f-404">ใช้ข้อมูลดังกล่าวเพื่อทบทวนใบสั่งที่คุณสร้างไว้เพื่อสถานการณ์นี้ เพื่อให้แน่ใจว่าคุณได้ผลลัพธ์ที่คาดไว้แล้ว</span><span class="sxs-lookup"><span data-stu-id="8528f-404">Use it to review the order that you created for this scenario, to make sure that you've obtained the expected results.</span></span>

1. <span data-ttu-id="8528f-405">ไปที่ **การจัดการคลังสินค้า \> การจัดส่ง \> การจัดส่งทั้งหมด**</span><span class="sxs-lookup"><span data-stu-id="8528f-405">Go to **Warehouse management \> Shipments \> All shipments**.</span></span>
1. <span data-ttu-id="8528f-406">ค้นหาและเลือกการจัดส่งที่สร้างขึ้นเพื่อโหลดที่คุณเพิ่งจะออกใช้</span><span class="sxs-lookup"><span data-stu-id="8528f-406">Find and select the shipment that was created for the load that you just released.</span></span>
1. <span data-ttu-id="8528f-407">ในบานหน้าต่างการดำเนินการ บนแท็บ **การขนส่ง** เลือก **ดูคอนเทนเนอร์**</span><span class="sxs-lookup"><span data-stu-id="8528f-407">On the Action Pane, on the **Transportation** tab, select **View containers**.</span></span>
1. <span data-ttu-id="8528f-408">ยืนยันว่าสินค้าจากใบสั่งขายถูกบรรจุลงในคอนเทนเนอร์สองคอนเทนเนอร์ที่แตกต่างกัน</span><span class="sxs-lookup"><span data-stu-id="8528f-408">Confirm that the items from the sales orders were containerized into two different containers.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="8528f-409">ทรัพยากรเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="8528f-409">Additional resources</span></span>

- [<span data-ttu-id="8528f-410">การบรรจุลงตู้บรรจุสินค้า</span><span class="sxs-lookup"><span data-stu-id="8528f-410">Containerization</span></span>](wave-containerization.md)
