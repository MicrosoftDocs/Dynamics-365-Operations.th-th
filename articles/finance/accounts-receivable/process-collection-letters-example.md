---
title: ตัวอย่างจดหมายเรียกเก็บเงิน
description: หัวข้อนี้อธิบายถึงตัวอย่างที่แสดงกระบวนการสร้าง การพิมพ์ และการลงรายการบัญชีจดหมายเรียกเก็บเงิน
author: JodiChristiansen
ms.date: 02/03/2021
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: CustPosting, CustCollectionLetterNote
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: jchrist
ms.search.validFrom: 2021-02-03
ms.dyn365.ops.version: 10.0.16
ms.openlocfilehash: fb2651644efd2cadfccb91e48c34dfddc8383e1f
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 05/11/2021
ms.locfileid: "6021427"
---
# <a name="process-collection-letters-example"></a><span data-ttu-id="491c5-103">ตัวอย่างจดหมายเรียกเก็บเงิน</span><span class="sxs-lookup"><span data-stu-id="491c5-103">Process collection letters example</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="491c5-104">หัวข้อนี้อธิบายถึงตัวอย่างที่แสดงกระบวนการสร้าง การพิมพ์ และการลงรายการบัญชีจดหมายเรียกเก็บเงิน</span><span class="sxs-lookup"><span data-stu-id="491c5-104">This topic goes through an example that shows the process of creating, printing, and posting collection letters.</span></span> <span data-ttu-id="491c5-105">ตัวอย่างจะยึดตามตัวเลือก **ละเว้นการชำระเงินและใบลดหนี้ เมื่อคํานวณรหัสจดหมายเรียกเก็บเงิน** ในสินเชื่อและการเรียกเก็บเงิน</span><span class="sxs-lookup"><span data-stu-id="491c5-105">The example is based on the **Ignore payments and credit memos when calculating collection letter code** option in Credit and collections.</span></span> <span data-ttu-id="491c5-106">โดยจะใช้ข้อมูลในบริษัทสาธิต USMF และลูกค้ารายใหม่ US-045</span><span class="sxs-lookup"><span data-stu-id="491c5-106">It uses data in the USMF demo company and a new customer, US-045.</span></span>

<span data-ttu-id="491c5-107">ในขั้นแรก ให้ไปที่ **บัญชีลูกหนี้ \> ลูกค้า \> ลูกค้าทั้งหมด** เลือก **ใหม่** จากนั้นป้อนข้อมูลที่จำเป็นในการสร้างลูกค้า US-045</span><span class="sxs-lookup"><span data-stu-id="491c5-107">To begin, go to **Accounts receivable \> Customers \> All customers**, select **New**, and then enter the required information to create customer US-045.</span></span>

<span data-ttu-id="491c5-108">เมื่อคุณดำเนินการสำเร็จแล้ว ให้ทำตามขั้นตอนเหล่านี้</span><span class="sxs-lookup"><span data-stu-id="491c5-108">When you've finished, follow these steps.</span></span>

1. <span data-ttu-id="491c5-109">ไปที่ **สินเชื่อและการเรียกเก็บเงิน \> จดหมายเรียกเก็บเงิน \> การตั้งค่าลำดับของจดหมายเรียกเก็บเงิน** และตั้งค่าลำดับของจดหมายเรียกเก็บเงิน ตามที่แสดงอยู่ในตารางต่อไปนี้ที่กำหนดให้กับโพรไฟล์การลงบัญชีของลูกค้า</span><span class="sxs-lookup"><span data-stu-id="491c5-109">Go to **Credit and collections \> Collection letter \> Setup collection letter sequence**, and set up the collection letter sequence as shown in the following table that is assigned to the customer posting profile.</span></span>

|     <span data-ttu-id="491c5-110">รหัสจดหมายเรียกเก็บเงิน</span><span class="sxs-lookup"><span data-stu-id="491c5-110">Collection   letter code</span></span>      |     <span data-ttu-id="491c5-111">คำอธิบาย</span><span class="sxs-lookup"><span data-stu-id="491c5-111">Description</span></span>                           |     <span data-ttu-id="491c5-112">สกุลเงิน</span><span class="sxs-lookup"><span data-stu-id="491c5-112">Currency</span></span>      |     <span data-ttu-id="491c5-113">บัญชีหลัก</span><span class="sxs-lookup"><span data-stu-id="491c5-113">Main   account</span></span>        |     <span data-ttu-id="491c5-114">ค่าธรรมเนียมในสกุลเงิน</span><span class="sxs-lookup"><span data-stu-id="491c5-114">Fee   in currency</span></span>     |     <span data-ttu-id="491c5-115">ต่ำกว่า</span><span class="sxs-lookup"><span data-stu-id="491c5-115">Minimum   over</span></span>        |     <span data-ttu-id="491c5-116">บล็อควัน</span><span class="sxs-lookup"><span data-stu-id="491c5-116">Days   Block</span></span>      |
|---------------------------------  |---------------------------------------    |-----------------  |-----------------------    |-------------------------- |-----------------------    |---------------------  |
|     <span data-ttu-id="491c5-117">จดหมายเรียกเก็บเงิน 1</span><span class="sxs-lookup"><span data-stu-id="491c5-117">Collection   letter 1</span></span>         |     <span data-ttu-id="491c5-118">การแจ้งเตือนครั้งที่สองพร้อมค่าธรรมเนียม</span><span class="sxs-lookup"><span data-stu-id="491c5-118">Second   notification with fee</span></span>        |     <span data-ttu-id="491c5-119">USD</span><span class="sxs-lookup"><span data-stu-id="491c5-119">USD</span></span>           |                           |     <span data-ttu-id="491c5-120">0.00</span><span class="sxs-lookup"><span data-stu-id="491c5-120">0.00</span></span>                  |     <span data-ttu-id="491c5-121">0.00</span><span class="sxs-lookup"><span data-stu-id="491c5-121">0.00</span></span>                  |     <span data-ttu-id="491c5-122">2</span><span class="sxs-lookup"><span data-stu-id="491c5-122">2</span></span>                 |
|     <span data-ttu-id="491c5-123">จดหมายเรียกเก็บเงิน 2</span><span class="sxs-lookup"><span data-stu-id="491c5-123">Collection   letter 2</span></span>         |     <span data-ttu-id="491c5-124">การแจ้งเตือนครั้งที่สองพร้อมค่าธรรมเนียม</span><span class="sxs-lookup"><span data-stu-id="491c5-124">Second   notification with fee</span></span>        |     <span data-ttu-id="491c5-125">USC</span><span class="sxs-lookup"><span data-stu-id="491c5-125">USC</span></span>           |     <span data-ttu-id="491c5-126">403150</span><span class="sxs-lookup"><span data-stu-id="491c5-126">403150</span></span>                |     <span data-ttu-id="491c5-127">20.00</span><span class="sxs-lookup"><span data-stu-id="491c5-127">20.00</span></span>                 |     <span data-ttu-id="491c5-128">10.00</span><span class="sxs-lookup"><span data-stu-id="491c5-128">10.00</span></span>                 |     <span data-ttu-id="491c5-129">3</span><span class="sxs-lookup"><span data-stu-id="491c5-129">3</span></span>                 |
|     <span data-ttu-id="491c5-130">การเรียกเก็บ</span><span class="sxs-lookup"><span data-stu-id="491c5-130">Collection</span></span>                    |     <span data-ttu-id="491c5-131">การแจ้งเตือนครั้งสุดท้ายพร้อมค่าธรรมเนียม</span><span class="sxs-lookup"><span data-stu-id="491c5-131">Final   notification with fee</span></span>         |     <span data-ttu-id="491c5-132">USD</span><span class="sxs-lookup"><span data-stu-id="491c5-132">USD</span></span>           |     <span data-ttu-id="491c5-133">403150</span><span class="sxs-lookup"><span data-stu-id="491c5-133">403150</span></span>                |     <span data-ttu-id="491c5-134">50.00</span><span class="sxs-lookup"><span data-stu-id="491c5-134">50.00</span></span>                 |     <span data-ttu-id="491c5-135">100.00</span><span class="sxs-lookup"><span data-stu-id="491c5-135">100.00</span></span>                |     <span data-ttu-id="491c5-136">วันที่ 15 ก.ย.</span><span class="sxs-lookup"><span data-stu-id="491c5-136">15</span></span>                |

<span data-ttu-id="491c5-137">รูปภาพประกอบต่อไปนี้จะแสดงข้อมูลในตารางตามที่จะปรากฏในหน้า **จดหมายเรียกเก็บเงิน**</span><span class="sxs-lookup"><span data-stu-id="491c5-137">The following illustration shows the information that's in the table as it would appear on the **Collection letters** page.</span></span> 

<span data-ttu-id="491c5-138">[![การตั้งค่าลำดับของจดหมายเรียกเก็บเงิน](./media/Ignore-payments-creditmemos-1.PNG)](./media/Ignore-payments-creditmemos-1.PNG)</span><span class="sxs-lookup"><span data-stu-id="491c5-138">[![Setting up a collection letter sequence](./media/Ignore-payments-creditmemos-1.PNG)](./media/Ignore-payments-creditmemos-1.PNG)</span></span>

 <span data-ttu-id="491c5-139">ตอนนี้คุณต้องตั้งค่าพารามิเตอร์สองตัวที่จำเป็นสำหรับตัวอย่างนี้</span><span class="sxs-lookup"><span data-stu-id="491c5-139">You must now set the two parameters that are required for this example.</span></span>

2. <span data-ttu-id="491c5-140">ไปยัง **สินเชื่อและการเรียกเก็บเงิน \> การตั้งค่า \> พารามิเตอร์บัญชีลูกหนี้** และปฏิบัติตามขั้นตอนเหล่านี้</span><span class="sxs-lookup"><span data-stu-id="491c5-140">Go to **Credit and collections \> Setup \> Accounts receivable parameters**, and follow these steps:</span></span>

    1. <span data-ttu-id="491c5-141">บนแท็บ **การเรียกเก็บเงิน** ตั้งค่าตัวเลือก **ละเว้นการชำระเงินและใบลดหนี้ เมื่อคํานวณรหัสจดหมายเรียกเก็บเงิน** เป็น **ใช่**</span><span class="sxs-lookup"><span data-stu-id="491c5-141">On the **Collections** tab, set the **Ignore payments and credit memos when calculating collection letter code** option to **Yes**.</span></span>
    2. <span data-ttu-id="491c5-142">ตรวจสอบให้แน่ใจว่าตั้งค่าฟิลด์ **สร้างจดหมายเรียกเก็บเงินสำหรับ** เป็น **ลูกค้า**</span><span class="sxs-lookup"><span data-stu-id="491c5-142">Make sure that the **Create collection letter per** field is set to **Customer**.</span></span>

    <span data-ttu-id="491c5-143">[![ตั้งค่าพารามิเตอร์บัญชีลูกหนี้สำหรับสินเชื่อและการเรียกเก็บเงิน](./media/Ignore-payments-creditmemos-2.PNG)](./media/Ignore-payments-creditmemos-2.PNG)</span><span class="sxs-lookup"><span data-stu-id="491c5-143">[![Setting Accounts receivable parameters for Credit collections](./media/Ignore-payments-creditmemos-2.PNG)](./media/Ignore-payments-creditmemos-2.PNG)</span></span>

3. <span data-ttu-id="491c5-144">ไปที่ **บัญชีลูกหนี้ \> ใบแจ้งหนี้ \> ใบแจ้งหนี้ข้อความอิสระทั้งหมด** เลือก **ใหม่** แล้วปฏิบัติตามขั้นตอนเหล่านี้</span><span class="sxs-lookup"><span data-stu-id="491c5-144">Go to **Accounts receivable \> Invoices \> All free text invoices**, select **New**, and then follow these steps:</span></span>

    1. <span data-ttu-id="491c5-145">ในฟิลด์ **บัญชีลูกค้า** เลือก **US-045**</span><span class="sxs-lookup"><span data-stu-id="491c5-145">In the **Customer account** field select **US-045**.</span></span>
    2. <span data-ttu-id="491c5-146">ในฟิลด์ **วันที่ในใบแจ้งหนี้** ให้ป้อน **1/15/2021**</span><span class="sxs-lookup"><span data-stu-id="491c5-146">In the **Invoice date** field, enter **1/15/2021**.</span></span>
    3. <span data-ttu-id="491c5-147">ในฟิลด์ **วันที่ครบกำหนด** ให้ป้อน **1/16/2021**</span><span class="sxs-lookup"><span data-stu-id="491c5-147">In the **Due date** field, enter **1/16/2021**.</span></span>
    4. <span data-ttu-id="491c5-148">บนแท็บ **บรรทัดใบแจ้งหนี้** ในฟิลด์ **บัญชีหลัก** ให้ป้อน **401100**</span><span class="sxs-lookup"><span data-stu-id="491c5-148">On the **Invoice lines** FastTab, in the **Main account** field, enter **401100**.</span></span>
    5. <span data-ttu-id="491c5-149">ในฟิลด์ **ราคาต่อหน่วย** ให้ป้อน **500.00**</span><span class="sxs-lookup"><span data-stu-id="491c5-149">In the **Unit price** field, enter **500.00**.</span></span>
    6. <span data-ttu-id="491c5-150">เลือก **ลงรายการบัญชี**</span><span class="sxs-lookup"><span data-stu-id="491c5-150">Select **Post**.</span></span>

    <span data-ttu-id="491c5-151">ขณะนี้คุณต้องป้อนใบลดหนี้สองรายการของลูกค้า</span><span class="sxs-lookup"><span data-stu-id="491c5-151">You must now enter two credit notes for the customer.</span></span>

4. <span data-ttu-id="491c5-152">เลือก **ใหม่** แล้วปฏิบัติตามขั้นตอนเหล่านี้</span><span class="sxs-lookup"><span data-stu-id="491c5-152">Select **New**, and then follow these steps:</span></span>

    1. <span data-ttu-id="491c5-153">ในฟิลด์ **บัญชีลูกค้า** เลือก **US-045**</span><span class="sxs-lookup"><span data-stu-id="491c5-153">In the **Customer account** field, select **US-045**.</span></span>
    2. <span data-ttu-id="491c5-154">ในฟิลด์ **วันที่ในใบแจ้งหนี้** ให้ป้อน **1/15/2021**</span><span class="sxs-lookup"><span data-stu-id="491c5-154">In the **Invoice date** field, enter **1/15/2021**.</span></span>
    3. <span data-ttu-id="491c5-155">ในฟิลด์ **วันที่ครบกำหนด** ให้ป้อน **1/16/2021**</span><span class="sxs-lookup"><span data-stu-id="491c5-155">In the **Due date** field, enter **1/16/2021**.</span></span>
    4. <span data-ttu-id="491c5-156">บนแท็บ **บรรทัดใบแจ้งหนี้** ในฟิลด์ **บัญชีหลัก** ให้ป้อน **401100**</span><span class="sxs-lookup"><span data-stu-id="491c5-156">On the **Invoice lines** FastTab, in the **Main account** field, enter **401100**.</span></span>
    5. <span data-ttu-id="491c5-157">ในฟิลด์ **ราคาต่อหน่วย** ให้ป้อน **-100.00**</span><span class="sxs-lookup"><span data-stu-id="491c5-157">In the **Unit price** field, enter **-100.00**.</span></span>
    6. <span data-ttu-id="491c5-158">เลือก **ลงรายการบัญชี**</span><span class="sxs-lookup"><span data-stu-id="491c5-158">Select **Post**.</span></span>

5. <span data-ttu-id="491c5-159">ทําซ้ำขั้นตอนที่ 4 แต่ป้อน **-200.00** ในฟิลด์ **ราคาต่อหน่วย**</span><span class="sxs-lookup"><span data-stu-id="491c5-159">Repeat step 4, but enter **-200.00** in the **Unit price** field.</span></span>
6. <span data-ttu-id="491c5-160">ไปที่ **บัญชีลูกหนี้ \> ลูกค้า \> ทั้งหมด** และเลือกลูกค้า **US-045**</span><span class="sxs-lookup"><span data-stu-id="491c5-160">Go to **Accounts receivable \> Customers \> All customers**, and select customer **US-045**.</span></span> <span data-ttu-id="491c5-161">จากนั้น ในบานหน้าต่างการดำเนินการ ให้เลือก **ธุรกรรม \> ธุรกรรม** เพื่อรีวิวธุรกรรมของลูกค้าที่คุณลงรายการบัญชีไปก่อนหน้านี้</span><span class="sxs-lookup"><span data-stu-id="491c5-161">Then, on the Action Pane, select **Transactions \> Transactions** to review the customer transactions that you posted earlier.</span></span>

    <span data-ttu-id="491c5-162">[![การตรวจทานธุรกรรมลูกค้าที่ลงรายการบัญชี](./media/Ignore-payments-creditmemos-3.PNG)](./media/Ignore-payments-creditmemos-3.PNG)</span><span class="sxs-lookup"><span data-stu-id="491c5-162">[![Reviewing the posted customer transactions](./media/Ignore-payments-creditmemos-3.PNG)](./media/Ignore-payments-creditmemos-3.PNG)</span></span>

    <span data-ttu-id="491c5-163">คุณต้องสร้างจดหมายเรียกเก็บเงินสำหรับลูกค้า US-045</span><span class="sxs-lookup"><span data-stu-id="491c5-163">You must now create collection letters for customer US-045.</span></span>

7. <span data-ttu-id="491c5-164">ไปที่ **สินเชื่อและการเรียกเก็บเงิน \> จดหมายเรียกเก็บเงิน \> สร้างจดหมายเรียกเก็บเงิน** และปฏิบัติตามขั้นตอนต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="491c5-164">Go to **Credit and collections \> Collection letter \> Create collection letters**, and follow these steps:</span></span>

    1. <span data-ttu-id="491c5-165">ตั้งค่าตัวเลือก **ใบแจ้งหนี้** และ **ใบลดหนี้** เป็น **ใช่**</span><span class="sxs-lookup"><span data-stu-id="491c5-165">Set the **Invoice** and **Credit note** options to **Yes**.</span></span>

        <span data-ttu-id="491c5-166">โดยค่าเริ่มต้น ควรมีการตั้งค่าฟิลด์ **จดหมายเรียกเก็บเงิน** เป็น **การเรียกเก็บเงินต่อลูกค้า**</span><span class="sxs-lookup"><span data-stu-id="491c5-166">By default, the **Collection letter** field should be set to **Collection per customer**.</span></span>

    2. <span data-ttu-id="491c5-167">ในฟิลด์ **วันที่ในจดหมายเรียกเก็บเงิน** ให้ป้อน **1/19/2021**</span><span class="sxs-lookup"><span data-stu-id="491c5-167">In the **Collection letter date** field, enter **1/19/2021**.</span></span>
    3. <span data-ttu-id="491c5-168">บนแท็บด่วน **เรกคอร์ดที่จะรวม** ให้เลือก **ตัวกรอง** จากนั้นในฟิลด์ **รหัสลูกค้า** เพิ่มลูกค้า **US-045**</span><span class="sxs-lookup"><span data-stu-id="491c5-168">On the **Records to include** FastTab, select **Filter**, and then, in the **Customer account** field, add customer **US-045**.</span></span>
    4. <span data-ttu-id="491c5-169">เลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="491c5-169">Select **OK**.</span></span>
    5. <span data-ttu-id="491c5-170">เลือก **ตกลง** เพื่อสร้างจดหมายเรียกเก็บเงิน</span><span class="sxs-lookup"><span data-stu-id="491c5-170">Select **OK** to create collection letters.</span></span>

8. <span data-ttu-id="491c5-171">ไปที่ **สินเชื่อและการเรียกเก็บเงิน \> จดหมายเรียกเก็บเงิน \> ตรวจทานและดำเนินการจดหมายเรียกเก็บเงิน** และปฏิบัติตามขั้นตอนต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="491c5-171">Go to **Credit and collections \> Collection letter \> Review and process collection letters**, and follow these steps:</span></span>

    1. <span data-ttu-id="491c5-172">โปรดสังเกตว่ารหัสจดหมายเรียกเก็บเงินบนทั้งหัวข้อและบรรทัดธุรกรรม คือ **จดหมายเรียกเก็บเงิน 1** เนื่องจากจดหมายเรียกเก็บเงินนี้เป็นจดหมายเรียกเก็บเงินแรกในลำดับ</span><span class="sxs-lookup"><span data-stu-id="491c5-172">Notice that the collection letter code on both the header and the transaction lines is **Collection letter 1**, because this collection letter is the first collection letter in the sequence.</span></span> <span data-ttu-id="491c5-173">(เมื่อต้องการดูบรรทัดธุรกรรม คุณอาจต้องเลือกแท็บด่วน **ธุรกรรม** )</span><span class="sxs-lookup"><span data-stu-id="491c5-173">(To view the transaction lines, you might have to select the **Transactions** FastTab.)</span></span>

   <span data-ttu-id="491c5-174">[![การตรวจสอบว่ารหัสจดหมายเรียกเก็บเงินเดียวกันปรากฏบนส่วนหน้าและบรรทัดต่างๆหรือไม่](./media/Ignore-payments-creditmemos-4.PNG)](./media/Ignore-payments-creditmemos-4.PNG)</span><span class="sxs-lookup"><span data-stu-id="491c5-174">[![Verifying that the same collection letter code appears on the header and the lines](./media/Ignore-payments-creditmemos-4.PNG)](./media/Ignore-payments-creditmemos-4.PNG)</span></span>

    2. <span data-ttu-id="491c5-175">ในบานหน้าต่างการดำเนินการ เลือก **ลงรายการบัญชี**</span><span class="sxs-lookup"><span data-stu-id="491c5-175">On the Action Pane, select **Post**.</span></span>
    3. <span data-ttu-id="491c5-176">ในฟิลด์ **วันที่ลงรายการบัญชี** ให้ป้อน **1/19/2021**</span><span class="sxs-lookup"><span data-stu-id="491c5-176">In the **Posting date** field, enter **1/19/2021**.</span></span>

    <span data-ttu-id="491c5-177">คุณต้องสร้างจดหมายเรียกเก็บเงินอีกครั้งสำหรับลูกค้า US-045</span><span class="sxs-lookup"><span data-stu-id="491c5-177">You must now create collection letters again for customer US-045.</span></span>

9. <span data-ttu-id="491c5-178">ไปที่ **สินเชื่อและการเรียกเก็บเงิน \> จดหมายเรียกเก็บเงิน \> สร้างจดหมายเรียกเก็บเงิน** และปฏิบัติตามขั้นตอนต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="491c5-178">Go to **Credit and collections \> Collection letter \> Create collection letters**, and follow these steps:</span></span>

    1. <span data-ttu-id="491c5-179">ตั้งค่าตัวเลือก **ใบแจ้งหนี้** และ **ใบลดหนี้** เป็น **ใช่**</span><span class="sxs-lookup"><span data-stu-id="491c5-179">Set the **Invoice** and **Credit note** options to **Yes**.</span></span>

        <span data-ttu-id="491c5-180">โดยค่าเริ่มต้น ควรมีการตั้งค่าฟิลด์ **จดหมายเรียกเก็บเงิน** เป็น **การเรียกเก็บเงินต่อลูกค้า**</span><span class="sxs-lookup"><span data-stu-id="491c5-180">By default, the **Collection letter** field should be set to **Collection per customer**.</span></span>

    2. <span data-ttu-id="491c5-181">ในฟิลด์ **วันที่ในจดหมายเรียกเก็บเงิน** ให้ป้อน **1/23/2021**</span><span class="sxs-lookup"><span data-stu-id="491c5-181">In the **Collection letter date** field, enter **1/23/2021**.</span></span>
    3. <span data-ttu-id="491c5-182">บนแท็บด่วน **เรกคอร์ดที่จะรวม** ให้เลือก **ตัวกรอง** จากนั้นในฟิลด์ **รหัสลูกค้า** เพิ่มลูกค้า **US-045**</span><span class="sxs-lookup"><span data-stu-id="491c5-182">On the **Records to include** FastTab, select **Filter**, and then, in the **Customer account** field, add customer **US-045**.</span></span>
    4. <span data-ttu-id="491c5-183">เลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="491c5-183">Select **OK**.</span></span>
    5. <span data-ttu-id="491c5-184">เลือก **ตกลง** เพื่อสร้างจดหมายเรียกเก็บเงิน</span><span class="sxs-lookup"><span data-stu-id="491c5-184">Select **OK** to create collection letters.</span></span>

10. <span data-ttu-id="491c5-185">ไปที่ **สินเชื่อและการเรียกเก็บเงิน \> จดหมายเรียกเก็บเงิน \> ตรวจทานและดำเนินการจดหมายเรียกเก็บเงิน** และปฏิบัติตามขั้นตอนต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="491c5-185">Go to **Credit and collections \> Collection letter \> Review and process collection letters**, and follow these steps:</span></span>

    1. <span data-ttu-id="491c5-186">โปรดสังเกตว่ารหัสจดหมายเรียกเก็บเงินบนหัวข้อ คือ **จดหมายเรียกเก็บเงิน 1**</span><span class="sxs-lookup"><span data-stu-id="491c5-186">Notice that the collection letter code on the header is **Collection letter 1**.</span></span> <span data-ttu-id="491c5-187">อย่างไรก็ตาม รหัสในบรรทัดธุรกรรม คือ **จดหมายเรียกเก็บเงิน 2**</span><span class="sxs-lookup"><span data-stu-id="491c5-187">However, the code on the transaction lines is **Collection letter 2**.</span></span>

   <span data-ttu-id="491c5-188">[![การตรวจสอบว่ารหัสจดหมายเรียกเก็บเงินที่แตกต่างกันปรากฏบนส่วนหน้าและบรรทัดต่างๆหรือไม่](./media/Ignore-payments-creditmemos-5.PNG)](./media/Ignore-payments-creditmemos-5.PNG)</span><span class="sxs-lookup"><span data-stu-id="491c5-188">[![Verifies that different collection letter codes appear on the header and the lines](./media/Ignore-payments-creditmemos-5.PNG)](./media/Ignore-payments-creditmemos-5.PNG)</span></span>

  <span data-ttu-id="491c5-189">รหัสแตกต่างกัน เนื่องจากตัวเลือก **ละเว้นการชำระเงินและใบลดหนี้ เมื่อคํานวณรหัสจดหมายเรียกเก็บเงิน** เป็น **ใช่**</span><span class="sxs-lookup"><span data-stu-id="491c5-189">The codes differ because the **Ignore payments and credit memos when calculating collection letter code** option is to **Yes**.</span></span>

  2. <span data-ttu-id="491c5-190">อย่าลงรายการบัญชีจดหมายเรียกเก็บเงินนี้</span><span class="sxs-lookup"><span data-stu-id="491c5-190">Don't post this collection letter.</span></span>

11. <span data-ttu-id="491c5-191">ไปที่ **สินเชื่อและการเรียกเก็บเงิน \> ตั้งค่า \> พารามิเตอร์บัญชีลูกหนี้** จากนั้นบนแท็บ **การเรียกเก็บเงิน** ให้ตั้งค่าตัวเลือก **ละเว้นการชำระเงินและใบลดหนี้ เมื่อคํานวณรหัสจดหมายเรียกเก็บเงิน** เป็น **ไม่**</span><span class="sxs-lookup"><span data-stu-id="491c5-191">Go to **Credit and collections \> Setup \> Accounts receivable parameters**, and then, on the **Collections** tab, set the **Ignore payments and credit memos when calculating collection letter code** option to **No**.</span></span>

    <span data-ttu-id="491c5-192">[![การตั้งค่าตัวเลือกการละเว้นการชำระเงินและใบลดหนี้ เมื่อมีการคำนวณรหัสจดหมายเรียกเก็บเงินเป็น ไม่](./media/Ignore-payments-creditmemos-6.PNG)](./media/Ignore-payments-creditmemos-6.PNG)</span><span class="sxs-lookup"><span data-stu-id="491c5-192">[![Setting the Ignore payments and credit memos when calculating collection letter code option to No](./media/Ignore-payments-creditmemos-6.PNG)](./media/Ignore-payments-creditmemos-6.PNG)</span></span>

    <span data-ttu-id="491c5-193">คุณต้องสร้างจดหมายเรียกเก็บเงินอีกครั้งสำหรับลูกค้า US-045</span><span class="sxs-lookup"><span data-stu-id="491c5-193">You must now create collection letters again for customer US-045.</span></span>

12. <span data-ttu-id="491c5-194">ไปที่ **สินเชื่อและการเรียกเก็บเงิน \> จดหมายเรียกเก็บเงิน \> สร้างจดหมายเรียกเก็บเงิน** และปฏิบัติตามขั้นตอนต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="491c5-194">Go to **Credit and collections \> Collection letter \> Create collection letters**, and follow these steps:</span></span>

    1. <span data-ttu-id="491c5-195">ตั้งค่าตัวเลือก **ใบแจ้งหนี้** และ **ใบลดหนี้** เป็น **ใช่**</span><span class="sxs-lookup"><span data-stu-id="491c5-195">Set the **Invoice** and **Credit note** options to **Yes**.</span></span>

        <span data-ttu-id="491c5-196">โดยค่าเริ่มต้น ควรมีการตั้งค่าฟิลด์ **จดหมายเรียกเก็บเงิน** เป็น **การเรียกเก็บเงินต่อลูกค้า**</span><span class="sxs-lookup"><span data-stu-id="491c5-196">By default, the **Collection letter** field should be set to **Collection per customer**.</span></span>

    2. <span data-ttu-id="491c5-197">ในฟิลด์ **วันที่ในจดหมายเรียกเก็บเงิน** ให้ป้อน **1/23/2021**</span><span class="sxs-lookup"><span data-stu-id="491c5-197">In the **Collection letter date** field, enter **1/23/2021**.</span></span>
    3. <span data-ttu-id="491c5-198">บนแท็บด่วน **เรกคอร์ดที่จะรวม** ให้เลือก **ตัวกรอง** จากนั้นในฟิลด์ **รหัสลูกค้า** เพิ่มลูกค้า **US-045**</span><span class="sxs-lookup"><span data-stu-id="491c5-198">On the **Records to include** FastTab, select **Filter**, and then, in the **Customer account** field, add customer **US-045**.</span></span>
    4. <span data-ttu-id="491c5-199">เลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="491c5-199">Select **OK**.</span></span>
    5. <span data-ttu-id="491c5-200">เลือก **ตกลง** เพื่อสร้างจดหมายเรียกเก็บเงิน</span><span class="sxs-lookup"><span data-stu-id="491c5-200">Select **OK** to create collection letters.</span></span>

13. <span data-ttu-id="491c5-201">ไปที่ **สินเชื่อและการเรียกเก็บเงิน \> จดหมายเรียกเก็บเงิน \> ตรวจทานและดำเนินการจดหมายเรียกเก็บเงิน** และโปรดสังเกตว่ารหัสจดหมายเรียกเก็บเงินบนทั้งหัวข้อและบรรทัดธุรกรรม คือ **จดหมายเรียกเก็บเงิน 2**</span><span class="sxs-lookup"><span data-stu-id="491c5-201">Go to **Credit and collections \> Collection letter \> Review and process collection letters**, and notice that the collection letter code on both the header and the transaction lines is **Collection letter 2**.</span></span>

    <span data-ttu-id="491c5-202">[![การแสดงอีกครั้งว่ารหัสจดหมายเรียกเก็บเงินเดียวกันปรากฏบนส่วนหน้าและบรรทัดต่างๆหรือไม่](./media/Ignore-payments-creditmemos-7.PNG)](./media/Ignore-payments-creditmemos-7.PNG)</span><span class="sxs-lookup"><span data-stu-id="491c5-202">[![Showing again that the same collection letter code appears on the header and the lines](./media/Ignore-payments-creditmemos-7.PNG)](./media/Ignore-payments-creditmemos-7.PNG)</span></span>

    <span data-ttu-id="491c5-203">รหัสเดียวกันปรากฏในทั้งสองแห่ง เนื่องจากตัวเลือก **ละเว้นการชำระเงินและใบลดหนี้ เมื่อคํานวณรหัสจดหมายเรียกเก็บเงิน** ได้รับการตั้งค่าเป็น **ไม่**</span><span class="sxs-lookup"><span data-stu-id="491c5-203">The same code appears in both places because the **Ignore payments and credit memos when calculating collection letter code** option is now set to **No**.</span></span>
