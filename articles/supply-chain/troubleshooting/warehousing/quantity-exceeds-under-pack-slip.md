---
title: ปริมาณเกินเปอร์เซ็นต์การจัดส่งน้อยกว่าปริมาณที่สั่งระหว่างการสร้างบันทึกการจัดส่ง
description: เมื่อคุณสร้างบันทึกการจัดส่ง สินค้าขาออกจะประกอบด้วยปริมาณที่เกินเปอร์เซ็นต์การจัดส่งน้อยกว่าปริมาณที่สั่ง
author: GalynaFedorova
ms.date: 5/31/2021
ms.topic: troubleshooting
ms.search.form: WHSLoadTable_WHSSalesPackingSlipPost,WHSLoadPlanningListPage_WHSSalesPackingSlipPost,WHSLoadPlanningWorkbench_WHSSalesPackingSlipPost
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: v-gfedorova
ms.search.validFrom: 2021-05-31
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: ecdd377d12faf40f64736e93671dcf42ff132403
ms.sourcegitcommit: e6437d994c3be0c5bb4a9263af3aa8351020d83a
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 06/14/2021
ms.locfileid: "6249176"
---
# <a name="quantity-exceeds-under-delivery-percentage-during-packing-slip-generation"></a><span data-ttu-id="64fc6-103">ปริมาณเกินเปอร์เซ็นต์การจัดส่งน้อยกว่าปริมาณที่สั่งระหว่างการสร้างบันทึกการจัดส่ง</span><span class="sxs-lookup"><span data-stu-id="64fc6-103">Quantity exceeds under-delivery percentage during packing slip generation</span></span>

<span data-ttu-id="64fc6-104">รหัสข้อผิดพลาด: SYS24921</span><span class="sxs-lookup"><span data-stu-id="64fc6-104">Error code: SYS24921</span></span>

## <a name="symptoms"></a><span data-ttu-id="64fc6-105">อาการ</span><span class="sxs-lookup"><span data-stu-id="64fc6-105">Symptoms</span></span>

<span data-ttu-id="64fc6-106">เมื่อคุณสร้างบันทึกการจัดส่ง สินค้าขาออกจะประกอบด้วยปริมาณที่เกินเปอร์เซ็นต์การจัดส่งน้อยกว่าปริมาณที่สั่ง</span><span class="sxs-lookup"><span data-stu-id="64fc6-106">When you generate a packing slip, the outbound load contains a quantity that exceeds the under-delivery percentage.</span></span>

<span data-ttu-id="64fc6-107">เมื่อคุณพยายามสร้างบันทึกการจัดส่ง ระบบจะแสดงข้อความแสดงข้อผิดพลาดต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="64fc6-107">When you try to generate a packing slip, the system shows the following error message:</span></span>

> <span data-ttu-id="64fc6-108">การจัดส่งน้อยกว่าปริมาณที่กำหนดของรายการคือ %1 เปอร์เซ็นต์ แต่การจัดส่งน้อยกว่าปริมาณที่กำหนดที่อนุญาตคือ %2 เปอร์เซ็นต์เท่านั้น</span><span class="sxs-lookup"><span data-stu-id="64fc6-108">Underdelivery of line is %1 percent, but the allowed underdelivery is only %2 percent.</span></span>

<span data-ttu-id="64fc6-109">ดังนั้นคุณจึงไม่สามารถสร้างบันทึกการจัดส่งของสินค้าได้</span><span class="sxs-lookup"><span data-stu-id="64fc6-109">Therefore, you can't generate the packing slip for the load.</span></span>

## <a name="cause"></a><span data-ttu-id="64fc6-110">สาเหตุ</span><span class="sxs-lookup"><span data-stu-id="64fc6-110">Cause</span></span>

<span data-ttu-id="64fc6-111">ปริมาณที่เบิกแล้วของสินค้าหรือการจัดส่งน้อยกว่าปริมาณที่สั่งและไม่ได้อยู่ภายในช่วงของเปอร์เซ็นต์การจัดส่งน้อยกว่าปริมาณที่สั่ง</span><span class="sxs-lookup"><span data-stu-id="64fc6-111">The picked quantity for the load or shipment is less than the ordered quantity and isn't within the range of the under-delivery percentage.</span></span>

## <a name="resolution"></a><span data-ttu-id="64fc6-112">การแก้ปัญหา</span><span class="sxs-lookup"><span data-stu-id="64fc6-112">Resolution</span></span>

<span data-ttu-id="64fc6-113">สินค้าหรือการจัดส่งอยู่ในสถานะที่การสร้างบันทึกการจัดส่งล้มเหลว</span><span class="sxs-lookup"><span data-stu-id="64fc6-113">The load or shipment is currently in a state where packing slip generation fails.</span></span> <span data-ttu-id="64fc6-114">เมื่อต้องการแก้ไขปัญหานี้ ให้ทำหนึ่งในงานต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="64fc6-114">To fix this issue, complete one of the following tasks:</span></span>

- <span data-ttu-id="64fc6-115">ปรับเปอร์เซ็นต์การจัดส่งน้อยกว่าปริมาณที่กำหนด</span><span class="sxs-lookup"><span data-stu-id="64fc6-115">Adjust the under-delivery percentage.</span></span>
- <span data-ttu-id="64fc6-116">ย้อนกลับรายการและทำการปรับปรุง</span><span class="sxs-lookup"><span data-stu-id="64fc6-116">Reverse and make adjustments.</span></span>

### <a name="adjust-the-under-delivery-percentage"></a><span data-ttu-id="64fc6-117">ปรับเปอร์เซ็นต์การจัดส่งน้อยกว่าปริมาณที่กำหนด</span><span class="sxs-lookup"><span data-stu-id="64fc6-117">Adjust the under-delivery percentage</span></span>

<span data-ttu-id="64fc6-118">ใช้ขั้นตอนต่อไปนี้เพื่อปรับปรุงปรับเปอร์เซ็นต์การจัดส่งน้อยกว่าปริมาณที่สั่ง</span><span class="sxs-lookup"><span data-stu-id="64fc6-118">Use the following procedure to adjust the under-delivery percentage.</span></span>

1. <span data-ttu-id="64fc6-119">ไปที่ **บัญชีลูกหนี้ \> ใบสั่ง \> ใบสั่งทั้งหมด**</span><span class="sxs-lookup"><span data-stu-id="64fc6-119">Go to **Accounts receivable \> Orders \> All orders**.</span></span>
1. <span data-ttu-id="64fc6-120">เลือกใบสั่งขายที่คุณไม่สามารถลงรายการบัญชีบันทึกการจัดส่งของสินค้าได้</span><span class="sxs-lookup"><span data-stu-id="64fc6-120">Select the sales order for which you can't post a packing slip for the load.</span></span>
1. <span data-ttu-id="64fc6-121">บนแท็บ  **รายการใบสั่งขาย** ให้เลือกรายการใบสั่งขายของสินค้าที่เกินกว่าเปอร์เซ็นต์การจัดส่งน้อยกว่าปริมาณที่กำหนด</span><span class="sxs-lookup"><span data-stu-id="64fc6-121">On the **Sales order lines** tab, select the sales order line for the item that exceeds the under-delivery percentage.</span></span>
1. <span data-ttu-id="64fc6-122">บนแท็บ  **รายละเอียดของรายการ** ให้เลือก **การจัดส่ง**</span><span class="sxs-lookup"><span data-stu-id="64fc6-122">On the  **Line details** tab, select **Delivery**.</span></span>
1. <span data-ttu-id="64fc6-123">ตั้งค่าฟิลด์ **การจัดส่งน้อยกว่าปริมาณที่กำหนด** เป็นเปอร์เซ็นต์ที่มากกว่าปริมาณที่สั่ง ซึ่งสามารถรองรับปริมาณที่เบิกแล้วเทียบกับปริมาณสินค้า เพื่อให้การสร้างบันทึกการจัดส่งสามารถดำเนินได้</span><span class="sxs-lookup"><span data-stu-id="64fc6-123">Set the **Underdelivery** field to a larger percentage that accommodates the quantity that was picked against the load quantity, so that packing slip generation can proceed.</span></span>

### <a name="reverse-and-make-adjustments"></a><span data-ttu-id="64fc6-124">ย้อนกลับรายการและทำการปรับปรุง</span><span class="sxs-lookup"><span data-stu-id="64fc6-124">Reverse and make adjustments</span></span>

<span data-ttu-id="64fc6-125">ย้อนกลับทุกรายการที่ได้ลงรายการบัญชีให้กับสินค้าแล้ว (ตัวอย่างเช่น บันทึกการจัดส่ง การยืนยันการจัดส่ง และงาน) ให้ปรับปรุงใบสั่งขาย ออกใช้ใบสั่งอีกครั้งไปยังคลังสินค้า และปฏิบัติตามขั้นตอนการจัดส่งสินค้าให้เสร็จสมบูรณ์</span><span class="sxs-lookup"><span data-stu-id="64fc6-125">Reverse everything that has been posted for the load (for example, the packing slip, shipment confirmation, and work), make sales order adjustments, re-release the order to the warehouse, and complete the shipment procedure.</span></span>

<span data-ttu-id="64fc6-126">ใช้กระบวนงานต่อไปนี้เพื่อยกเลิกบันทึกการจัดส่ง</span><span class="sxs-lookup"><span data-stu-id="64fc6-126">Use the following procedure to cancel a packing slip.</span></span>

1. <span data-ttu-id="64fc6-127">ไปที่ **การจัดการคลังสินค้า \> จำนวนงานในศูนย์การผลิต \> จำนวนงานในศูนย์การผลิตทั้งหมด**</span><span class="sxs-lookup"><span data-stu-id="64fc6-127">Go to **Warehouse management \> Loads \> All loads**.</span></span>
1. <span data-ttu-id="64fc6-128">ในบานหน้าต่างการดำเนินการ บนแท็บ **จัดส่งและรับ** ในกลุ่ม **กลับรายการ** ให้เลือก **ยกเลิกบันทึกการจัดส่ง**</span><span class="sxs-lookup"><span data-stu-id="64fc6-128">On the Action Pane, on the **Ship and receive** tab, in the **Reverse** group, select **Cancel packing slips**.</span></span>

<span data-ttu-id="64fc6-129">ใช้กระบวนงานต่อไปนี้ในการกลับรายการการยืนยันการจัดส่ง</span><span class="sxs-lookup"><span data-stu-id="64fc6-129">Use the following procedure to reverse a shipment confirmation.</span></span>

1. <span data-ttu-id="64fc6-130">ไปที่ **การจัดการคลังสินค้า \> จำนวนงานในศูนย์การผลิต \> จำนวนงานในศูนย์การผลิตทั้งหมด**</span><span class="sxs-lookup"><span data-stu-id="64fc6-130">Go to **Warehouse management \> Loads \> All loads**.</span></span>
1. <span data-ttu-id="64fc6-131">ในบานหน้าต่างการดำเนินการ บนแท็บ **จัดส่งและรับ** ในกลุ่ม **กลับรายการ** ให้เลือก **กลับรายการการยืนยันการจัดส่ง**</span><span class="sxs-lookup"><span data-stu-id="64fc6-131">On the Action Pane, on the **Ship and receive** tab, in the **Reverse** group, select **Reverse shipment confirmation**.</span></span>

<span data-ttu-id="64fc6-132">ใช้ขั้นตอนต่อไปนี้เพื่อย้อนกลับงาน</span><span class="sxs-lookup"><span data-stu-id="64fc6-132">Use the following procedure to reverse work.</span></span>

1. <span data-ttu-id="64fc6-133">ไปที่ **การจัดการคลังสินค้า \> จำนวนงานในศูนย์การผลิต \> จำนวนงานในศูนย์การผลิตทั้งหมด**</span><span class="sxs-lookup"><span data-stu-id="64fc6-133">Go to **Warehouse management \> Loads \> All loads**.</span></span>
1. <span data-ttu-id="64fc6-134">บนบานหน้าต่างการดำเนินการในแท็บ **สินค้า** ในกลุ่ม **งาน** เลือก **ย้อนกลับงาน**</span><span class="sxs-lookup"><span data-stu-id="64fc6-134">On the Action Pane, on the **Loads** tab, in the **Work** group, select **Reverse work**.</span></span>
