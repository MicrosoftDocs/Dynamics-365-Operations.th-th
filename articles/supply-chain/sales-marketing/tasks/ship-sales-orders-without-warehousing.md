---
title: จัดส่งใบสั่งขายโดยไม่มีคลังสินค้า
description: หัวข้อนี้อธิบายวิธีการปรับปรุงใบสั่งขาย เมื่อมีการจัดส่งผลิตภัณฑ์ให้กับลูกค้า
author: omulvad
manager: tfehr
ms.date: 08/20/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SalesTableListPage, SalesTable, SalesEditLines,  SrsReportViewerForm, SalesTableLineQuantity, CustPackingSlipJournal
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: omulvad
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 1cd28e38c0ffbc2cb154cd38cb4aaeea76087bf7
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 04/02/2020
ms.locfileid: "3203199"
---
# <a name="ship-sales-orders-without-warehousing"></a><span data-ttu-id="055d7-103">จัดส่งใบสั่งขายโดยไม่มีคลังสินค้า</span><span class="sxs-lookup"><span data-stu-id="055d7-103">Ship sales orders without warehousing</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="055d7-104">หัวข้อนี้อธิบายวิธีการปรับปรุงใบสั่งขาย เมื่อมีการจัดส่งผลิตภัณฑ์ให้กับลูกค้า</span><span class="sxs-lookup"><span data-stu-id="055d7-104">This topic explains how to update a sales order when products are shipped to the customer.</span></span> <span data-ttu-id="055d7-105">คู่มือจะเกี่ยวข้องกับขั้นตอนการเติมสินค้าที่ไม่ได้ถูกตั้งค่าสำหรับการจัดการคลังสินค้า (ไม่มีคลังสินค้าทั้งแบบพื้นฐานหรือแบบขั้นสูง) และดังนั้นจึงไม่จำเป็นต้องลงทะเบียนผลิตภัณฑ์ก่อนที่จะจัดส่งสินค้า </span><span class="sxs-lookup"><span data-stu-id="055d7-105">The guide is applicable to the fulfillment flow that is not set up for warehouse management (neither basic or advanced warehousing), and therefore does not require product picking to be registered before shipment.</span></span> <span data-ttu-id="055d7-106">คุณสามารถทำตามขั้นตอนเหล่านี้กับข้อมูลของคุณ หรือกับบริษัทข้อมูลสาธิต USMF</span><span class="sxs-lookup"><span data-stu-id="055d7-106">You can run this procedure on your own data or in demo data company USMF.</span></span> <span data-ttu-id="055d7-107">ในทั้งสองกรณี ก่อนที่คุณจะเริ่มงานนี้ ให้สร้างใบสั่งขายสำหรับสินค้าคงคลังที่มีปริมาณมากกว่า 1</span><span class="sxs-lookup"><span data-stu-id="055d7-107">In both cases, before you start this task, create a sales order for an inventoried product with a quantity of greater than 1.</span></span> <span data-ttu-id="055d7-108">เพื่อหลีกเลี่ยงข้อผิดพลาดในการลงรายการบัญชี คุณต้องตรวจสอบว่า ปริมาณผลิตภัณฑ์คงเหลือในไซต์และคลังสินค้าที่คุณเลือกในใบสั่งนั้นครอบคลุมปริมาณในใบสั่ง</span><span class="sxs-lookup"><span data-stu-id="055d7-108">To avoid a posting error, you need to check that the product's on-hand quantity in the site and warehouse that you've selected on the order covers the order quantity.</span></span>

## <a name="post-packing-slip-for-an-order"></a><span data-ttu-id="055d7-109">ลงรายการบัญชีบันทึกการจัดส่งสำหรับใบสั่ง</span><span class="sxs-lookup"><span data-stu-id="055d7-109">Post packing slip for an order</span></span>
1. <span data-ttu-id="055d7-110">ในบานหน้าต่างนำทาง ไปยัง **โมดูล > การขายและการตลาด > ใบสั่งขาย > ใบสั่งขายทั้งหมด**</span><span class="sxs-lookup"><span data-stu-id="055d7-110">In the navigation pane, go to **Modules > Sales and marketing > Sales orders > All sales orders**.</span></span>
2. <span data-ttu-id="055d7-111">ในรายการ ให้ค้นหาและเลือกใบสั่งคุณได้สร้างขึ้นสำหรับงานนี้</span><span class="sxs-lookup"><span data-stu-id="055d7-111">In the list, find and select the order you have created for this task.</span></span>
3. <span data-ttu-id="055d7-112">บนบานหน้าต่างการดำเนินการ เลือก **เบิกสินค้าและจัดส่ง**</span><span class="sxs-lookup"><span data-stu-id="055d7-112">On the Action Pane, select **Pick and pack**.</span></span>
4. <span data-ttu-id="055d7-113">เลือก **ลงรายการบัญชีบันทึกการจัดส่ง**</span><span class="sxs-lookup"><span data-stu-id="055d7-113">Select **Post packing slip**.</span></span>
5. <span data-ttu-id="055d7-114">ขยายหรือยุบส่วน **พารามิเตอร์**</span><span class="sxs-lookup"><span data-stu-id="055d7-114">Expand or collapse the **Parameters** section.</span></span>
6. <span data-ttu-id="055d7-115">ในฟิลด์ **ปริมาณ** ให้เลือก **ทั้งหมด**</span><span class="sxs-lookup"><span data-stu-id="055d7-115">In the **Quantity** field, select **All**.</span></span>
    - <span data-ttu-id="055d7-116">ตัวเลือกอื่นๆ ได้แก่ **จัดส่งทันที** และ **เบิกสินค้าแล้ว**</span><span class="sxs-lookup"><span data-stu-id="055d7-116">Other options include **Deliver now** and **Picked**.</span></span> <span data-ttu-id="055d7-117">ถ้ารายการในใบสั่งจะถูกจัดส่งเป็นบางส่วน และฟิลด์ **จัดส่งทันที** บนรายการในใบสั่งที่ประกอบด้วยปริมาณ คุณอาจเลือก **จัดส่งทันที**</span><span class="sxs-lookup"><span data-stu-id="055d7-117">If the order line is to be shipped partially and the **Deliver now** field on the order line contains a quantity, you would select **Deliver now**.</span></span> <span data-ttu-id="055d7-118">ถ้าขั้นตอนการเติมสินค้าขององค์กรของคุณมีการเบิกสินค้าเป็นกระบวนการแยกต่างหาก ซึ่งมีการจัดการและมีการลงทะเบียนด้วยรายการเบิกสินค้า คุณอาจเลือก **เบิกสินค้าแล้ว**</span><span class="sxs-lookup"><span data-stu-id="055d7-118">If your organization's fulfillment flow includes picking as a separate process that is managed by and registered with a picking list, you would select **Picked**.</span></span>  
    - <span data-ttu-id="055d7-119">ตรวจสอบว่าตัวเลือก **การลงรายการบัญชี** ได้ถูกตั้งค่าเป็น **ใช่**</span><span class="sxs-lookup"><span data-stu-id="055d7-119">Check that the **Posting** option is set to **Yes**.</span></span>  
7. <span data-ttu-id="055d7-120">ตั้งค่าตัวเลือก **พิมพ์บันทึกการจัดส่ง** เป็น **ใช่**</span><span class="sxs-lookup"><span data-stu-id="055d7-120">Set the **Print packing slip** option to **Yes**.</span></span> <span data-ttu-id="055d7-121">แท็บ **ภาพรวม** ประกอบด้วยรายการของบันทึกการจัดส่งที่จะมีการสร้างขึ้นในการลงรายการบัญชีนี้</span><span class="sxs-lookup"><span data-stu-id="055d7-121">The **Overview** tab contains a list of packing slips to be generated in this posting.</span></span> <span data-ttu-id="055d7-122">ถ้าคุณจัดส่งใบสั่งแต่ละใบ โดยทั่วไปจะมีหนึ่งบันทึกการจัดส่ง </span><span class="sxs-lookup"><span data-stu-id="055d7-122">If you are shipping an individual order, there will typically be one packing slip.</span></span> <span data-ttu-id="055d7-123">อย่างไรก็ตาม ถ้ารายการของใบสั่งนั้นจะถูกจัดส่งจากไซต์อื่น การลงรายการบัญชีจะถูกแบ่งออกโดยอัตโนมัติเป็นจำนวนเอกสารที่เหมาะสม </span><span class="sxs-lookup"><span data-stu-id="055d7-123">However, if that order's lines are to be shipped from different sites, posting will automatically be split into the appropriate number of documents.</span></span> <span data-ttu-id="055d7-124">ซึ่งเป็นเงื่อนไขบังคับที่ไม่สามารถเปลี่ยนแปลงได้ </span><span class="sxs-lookup"><span data-stu-id="055d7-124">This is a mandatory condition that cannot be changed.</span></span> <span data-ttu-id="055d7-125">ในทำนองเดียวกัน การลงรายการบัญชีจะยังสามารถถูกแบ่งออกเป็นเอกสารหลายรายการ ถ้ารายการของใบสั่งจะถูกจัดส่งไปที่ที่อยู่การจัดส่งที่แตกต่างกัน และมีการตั้งค่านโยบายการจัดส่งให้ต้องการการแบ่ง</span><span class="sxs-lookup"><span data-stu-id="055d7-125">Similarly, the posting will also be split into multiple documents if the order's lines are to be shipped to different delivery addresses, and the shipping policy is set up to require a split.</span></span>  
8. <span data-ttu-id="055d7-126">บนแท็บ **รายการ** ให้เลือกแถวสำหรับรายการในใบสั่งที่จะมีการจัดส่ง</span><span class="sxs-lookup"><span data-stu-id="055d7-126">On the **Lines** tab, select the row for the order line to be shipped.</span></span>
9. <span data-ttu-id="055d7-127">ในฟิลด์ **ปรับปรุง** ป้อนหมายเลขที่ต่ำกว่าปริมาณเดิม</span><span class="sxs-lookup"><span data-stu-id="055d7-127">In the **Update** field, enter a number lower than the original quantity.</span></span>
10. <span data-ttu-id="055d7-128">เลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="055d7-128">Select **OK**.</span></span>
11. <span data-ttu-id="055d7-129">เลือก **ใช่**</span><span class="sxs-lookup"><span data-stu-id="055d7-129">Select **Yes**.</span></span>
12. <span data-ttu-id="055d7-130">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="055d7-130">Close the page.</span></span>
13. <span data-ttu-id="055d7-131">ในบานหน้าต่างการดำเนินการ เลือก **ตัวเลือก**</span><span class="sxs-lookup"><span data-stu-id="055d7-131">On the Action Pane, select **Options**.</span></span>
14. <span data-ttu-id="055d7-132">เลือก **เปลี่ยนมุมมอง**</span><span class="sxs-lookup"><span data-stu-id="055d7-132">Select **Change view**.</span></span>
15. <span data-ttu-id="055d7-133">เลือก **มุมมองส่วนหัว**</span><span class="sxs-lookup"><span data-stu-id="055d7-133">Select **Header view**.</span></span>
    - <span data-ttu-id="055d7-134">ถ้ารายการในใบสั่งทั้งหมดมีการจัดส่งทั้งหมดแล้ว สถานะใบสั่งจะเปลี่ยนจาก เปิด เป็น จัดส่งแล้ว</span><span class="sxs-lookup"><span data-stu-id="055d7-134">If all of the lines on the order have been fully shipped, the order status changes from Open to Delivered.</span></span>  
    - <span data-ttu-id="055d7-135">ในตัวอย่างนี้ รายการใบสั่งได้ถูกจัดส่งเป็นบางส่วน </span><span class="sxs-lookup"><span data-stu-id="055d7-135">In this example, the order line has been shipped partially.</span></span> <span data-ttu-id="055d7-136">นี่เป็นเหตุผลว่าทำไมสถานะใบสั่งยังคงเป็น เปิดอยู่</span><span class="sxs-lookup"><span data-stu-id="055d7-136">This is why the the order status remains Open.</span></span>     
    - <span data-ttu-id="055d7-137">มีการตั้งค่าฟิลด์ **สถานะเอกสาร** เป็นบันทึกการจัดส่ง เนื่องจากมีรายการใบสั่งอย่างน้อยหนึ่งรายการได้ถูกจัดส่ง</span><span class="sxs-lookup"><span data-stu-id="055d7-137">The **Document status** field is set to Packing slip because at least one of the order lines have been shipped.</span></span>  
16. <span data-ttu-id="055d7-138">ในบานหน้าต่างการดำเนินการ เลือก **ทั่วไป**</span><span class="sxs-lookup"><span data-stu-id="055d7-138">On the Action Pane, select **General**.</span></span>
17. <span data-ttu-id="055d7-139">เลือก **ปริมาณในรายการ**</span><span class="sxs-lookup"><span data-stu-id="055d7-139">Select **Line quantity**.</span></span>
18. <span data-ttu-id="055d7-140">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="055d7-140">Close the page.</span></span>
19. <span data-ttu-id="055d7-141">บนบานหน้าต่างการดำเนินการ เลือก **เบิกสินค้าและจัดส่ง**</span><span class="sxs-lookup"><span data-stu-id="055d7-141">On the Action Pane, select **Pick and pack**.</span></span>
20. <span data-ttu-id="055d7-142">เลือก **บันทึกการจัดส่ง**</span><span class="sxs-lookup"><span data-stu-id="055d7-142">Select **Packing slip**.</span></span> <span data-ttu-id="055d7-143">หน้า **สมุดรายวันบันทึกการจัดส่ง** ประกอบด้วย เอกสารบันทึกการจัดส่งทั้งหมดที่ถูกสร้างขึ้นสำหรับใบสั่งของคุณ</span><span class="sxs-lookup"><span data-stu-id="055d7-143">The **Packing slip journal** page contains all the packing slip documents that were generated for your order.</span></span> <span data-ttu-id="055d7-144">คุณสามารถตรวจทานรายละเอียดของแต่ละเอกสาร และพิมพ์เอกสารเหล่านั้น ถ้าคุณต้องการ</span><span class="sxs-lookup"><span data-stu-id="055d7-144">You can review details of each document and print them, if you wish.</span></span>  

