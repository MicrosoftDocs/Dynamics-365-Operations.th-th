---
title: กลุ่มใบสั่งงาน
description: หัวข้อนี้อธิบายวิธีการทำงานกับกลุ่มใบสั่งงานในการจัดการสินทรัพย์
author: josaw1
manager: AnnBe
ms.date: 10/15/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-09-30
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 161244cb4451ddc7b13b579fd02e828a61adeea4
ms.sourcegitcommit: deb87e518a151d8bb084891851a39758938a96e4
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 10/15/2019
ms.locfileid: "2626373"
---
# <a name="work-order-pools"></a><span data-ttu-id="7d667-103">กลุ่มใบสั่งงาน</span><span class="sxs-lookup"><span data-stu-id="7d667-103">Work order pools</span></span>

[!include [banner](../../includes/banner.md)]


<span data-ttu-id="7d667-104">คุณสามารถใช้กลุ่มใบสั่งงานเพื่อจัดกลุ่มใบสั่งงานที่มีบางอย่างร่วมกันได้</span><span class="sxs-lookup"><span data-stu-id="7d667-104">You can use work order pools to group work orders that have something in common.</span></span> <span data-ttu-id="7d667-105">ต่อไปนี้เป็นตัวอย่างของสิ่งที่คุณสามารถสร้างกลุ่มใบสั่งงานให้:</span><span class="sxs-lookup"><span data-stu-id="7d667-105">Here are some examples of things that you can create  work order pools for:</span></span>

- <span data-ttu-id="7d667-106">ทีมผู้ปฏิบัติงาน ตัวอย่างเช่น ทีมงานบำรุงรักษา A หรือทีมงานบำรุงรักษา B</span><span class="sxs-lookup"><span data-stu-id="7d667-106">Work crews, for example, Maintenance Crew A or Maintenance Crew B</span></span>  

- <span data-ttu-id="7d667-107">ทักษะวิชาชีพ เช่น ช่างไฟฟ้า หรือช่างประปา</span><span class="sxs-lookup"><span data-stu-id="7d667-107">Professional skills, such as electricians or plumbers</span></span>  

- <span data-ttu-id="7d667-108">ที่ตั้งทางกายภาพ</span><span class="sxs-lookup"><span data-stu-id="7d667-108">Physical locations</span></span>  

- <span data-ttu-id="7d667-109">กำหนดการเวลา เช่น สัปดาห์ หรือรอบระยะเวลาอื่นๆ</span><span class="sxs-lookup"><span data-stu-id="7d667-109">Time schedules, such as weeks or other periods</span></span>  

<span data-ttu-id="7d667-110">คุณสามารถใส่ใบสั่งงานหนึ่งรายการในกลุ่มใบสั่งงานที่หลากหลายได้ตามที่คุณต้องการ</span><span class="sxs-lookup"><span data-stu-id="7d667-110">As you require, you can put one work order in multiple work order pools.</span></span>


## <a name="create-a-work-order-pool"></a><span data-ttu-id="7d667-111">สร้างกลุ่มใบสั่งงาน</span><span class="sxs-lookup"><span data-stu-id="7d667-111">Create a work order pool</span></span>

<span data-ttu-id="7d667-112">บนหน้ารายการ **กลุ่มใบสั่งงานทั้งหมด** หรือ **กลุ่มใบสั่งงานที่ใช้งานอยู่** คุณสามารถดูภาพรวมของกลุ่มใบสั่งงานของคุณและสร้างกลุ่มใหม่</span><span class="sxs-lookup"><span data-stu-id="7d667-112">On the **All work order pools** or **Active work order pools** list page, you can get an overview of your work order pools and create new pools.</span></span>

1. <span data-ttu-id="7d667-113">เลือก **การจัดการสินทรัพย์** > **ทั่วไป** > **กลุ่มใบสั่งงาน** > **กลุ่มใบสั่งงานทั้งหมด** หรือ **กลุ่มใบสั่งงานที่ใช้งานอยู่**</span><span class="sxs-lookup"><span data-stu-id="7d667-113">Select **Asset management** > **Common** > **Work order pools** > **All work order pools** or **Active work order pools**.</span></span>

2. <span data-ttu-id="7d667-114">เลือก **ใหม่**</span><span class="sxs-lookup"><span data-stu-id="7d667-114">Select **New**.</span></span>

3. <span data-ttu-id="7d667-115">ในฟิลด์ **กลุ่ม** ให้ป้อนรหัสสำหรับกลุ่มใบสั่งงาน</span><span class="sxs-lookup"><span data-stu-id="7d667-115">In the **Pool** field, enter an ID for the work order pool.</span></span>

4. <span data-ttu-id="7d667-116">ฟิลด์ **ชื่อ** ป้อนชื่อ</span><span class="sxs-lookup"><span data-stu-id="7d667-116">the **Name** field, enter a name.</span></span>

5. <span data-ttu-id="7d667-117">ตั้งค่าตัวเลือก **ใช้งานอยู่** เป็น **ใช่** เพื่อระบุว่ากลุ่มใบสั่งงานเปิดใช้งานอยู่</span><span class="sxs-lookup"><span data-stu-id="7d667-117">Set the **Active** option to **Yes** to indicate that the work order pool is active.</span></span>

6. <span data-ttu-id="7d667-118">ตั้งค่าตัวเลือก **ลบความสัมพันธ์ของใบสั่งงาน** เป็น **ใช่** ถ้าคุณต้องการให้ลบใบสั่งงานออกจากกลุ่มใบสั่งงานโดยอัตโนมัติ</span><span class="sxs-lookup"><span data-stu-id="7d667-118">Set the **Delete work order relations** option to **Yes** if work orders should automatically be removed from the work order pool.</span></span>

7. <span data-ttu-id="7d667-119">ในฟิลด์ **ลบสถานะการใช้** ให้เลือกสถานะการใช้ใบสั่งงาน</span><span class="sxs-lookup"><span data-stu-id="7d667-119">In the **Delete lifecycle state** field, select the work order lifecycle state.</span></span> <span data-ttu-id="7d667-120">ตัวอย่างเช่น สถานะการใช้ใบสั่งงานสำหรับการทำให้ใบสั่งงานเสร็จสมบูรณ์อาจถูกตั้งค่าให้ลบความสัมพันธ์กับกลุ่มใบสั่งงานโดยอัตโนมัติ</span><span class="sxs-lookup"><span data-stu-id="7d667-120">For example, the work order lifecycle state for completing a work order could be set to automatically delete relations to work order pools.</span></span>

    <span data-ttu-id="7d667-121">คุณสามารถเริ่มต้นการเพิ่มใบสั่งงานให้กับกลุ่มใบสั่งงานของคุณได้ทันที</span><span class="sxs-lookup"><span data-stu-id="7d667-121">You can start adding work orders to your work order pool right away.</span></span>

8. <span data-ttu-id="7d667-122">บน FastTab **ใบสั่งงาน** ให้เลือก **เพิ่มรายการ**</span><span class="sxs-lookup"><span data-stu-id="7d667-122">On the **Work orders** FastTab, select **Add line**.</span></span>

9. <span data-ttu-id="7d667-123">ในฟิลด์ **ใบสั่งงาน** เลือกใบสั่งงาน</span><span class="sxs-lookup"><span data-stu-id="7d667-123">In the **Work order** field, select a work order.</span></span> <span data-ttu-id="7d667-124">ฟิลด์ที่เกี่ยวข้องจะมีการอัพเดตโดยอัตโนมัติ</span><span class="sxs-lookup"><span data-stu-id="7d667-124">The related fields are automatically updated.</span></span>

10. <span data-ttu-id="7d667-125">ทำซ้ำขั้นตอนที่ 8 ถึง 9 เพื่อเพิ่มใบสั่งงานเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="7d667-125">Repeat steps 8 through 9 to add more work orders.</span></span>

11. <span data-ttu-id="7d667-126">ถ้าใบสั่งงานที่คุณเพิ่มควรทำในใบสั่งเฉพาะ ในฟิลด์ **เรียงลำดับ** คุณสามารถป้อนหมายเลข **1** **2** **3** และอื่นๆ เพื่อระบุใบสั่งนั้นได้</span><span class="sxs-lookup"><span data-stu-id="7d667-126">If the work orders that you added should be done in a specific order, in the **Sort order** field, you can enter the numbers **1**, **2**, **3**, and so on, to specify that order.</span></span>

12. <span data-ttu-id="7d667-127">เมื่อต้องการดูรายการของใบสั่งงานทั้งหมดที่รวมอยู่ในกลุ่มใบสั่งงาน บนบานหน้าต่างการดำเนินการ บนแท็บ **กลุ่มใบสั่งงาน** ในกลุ่ม **ดูกลุ่มใบสั่งงานที่เกี่ยวข้อง** เลือก **ใบสั่งงาน** เพื่อเปิดหน้ารายการ **ใบสั่งงานทั้งหมด**</span><span class="sxs-lookup"><span data-stu-id="7d667-127">To view a list of all the work orders that are included in the work order pool, on the Action Pane, on the **Work order pool** tab, in the **View work order pool related** group, select **Work orders** to open the **All work orders** list page.</span></span>

13. <span data-ttu-id="7d667-128">เมื่อต้องการคำนวณและดูการใช้กำลังการผลิตสำหรับกำหนดการบำรุงรักษา ใบสั่งงานที่ไม่ได้จัดกำหนดการ และใบสั่งงานที่จัดกำหนดการ บนบานหน้าต่างการดำเนินการ บนแท็บ **กลุ่มใบสั่งงาน** ในกลุ่ม **ดูกลุ่มใบสั่งงานที่เกี่ยวข้อง** เลือก **การใช้กำลังการผลิต** เพื่อเปิดกล่องโต้ตอบ **คำนวณการใช้กำลังการผลิต**</span><span class="sxs-lookup"><span data-stu-id="7d667-128">To calculate and view capacity load for the maintenance schedule, unscheduled work orders, and scheduled work orders, on the Action Pane, on the **Work order pool** tab, in the **View work order pool related** group, select **Capacity load** to open the **Calculate capacity load** dialog.</span></span>

14. <span data-ttu-id="7d667-129">เมื่อต้องการคำนวณและดูการคาดการณ์สำหรับสินค้า (อะไหล่สำรองและสินค้าที่ต้องการอื่นๆ) ที่เกี่ยวข้องกับกำหนดการบำรุงรักษา ใบสั่งงานที่ไม่ได้จัดกำหนดการ และใบสั่งงานที่จัดกำหนดการ บนบานหน้าต่างการดำเนินการ บนแท็บ **กลุ่มใบสั่งงาน** ในกลุ่ม **ดูกลุ่มใบสั่งงานที่เกี่ยวข้อง** เลือก **การคาดการณ์สินค้า** เพื่อเปิดกล่องโต้ตอบ **คำนวณการคาดการณ์สินค้า**</span><span class="sxs-lookup"><span data-stu-id="7d667-129">To calculate and view forecasts for items (spare parts and other required items) that are related to maintenance schedule, unscheduled work orders, and scheduled work orders, on the Action Pane, on the **Work order pool** tab, in the **View work order pool related** group, select **Item forecast** to open the **Calculate item forecast** dialog.</span></span>

15. <span data-ttu-id="7d667-130">เมื่อต้องการดูรายการของใบขอซื้อที่เกี่ยวข้องกับใบสั่งงานในกลุ่มใบสั่งงาน บนบานหน้าต่างการดำเนินการ บนแท็บ **กลุ่มใบสั่งงาน** ในกลุ่ม **การจัดซื้อ** เลือก **ใบขอซื้อของใบสั่งงาน** เพื่อเปิดหน้ารายการ **ใบขอซื้อของใบสั่งงาน**</span><span class="sxs-lookup"><span data-stu-id="7d667-130">To view a list of purchase requisitions that are related to the work orders in the work order pool, on the Action Pane, on the **Work order pool** tab, in the **Procurement** group, select **Work order purchase requisition** to open the **Work order purchase requisition** list page.</span></span>

16. <span data-ttu-id="7d667-131">เมื่อต้องการดูรายการของใบสั่งซื้อที่เกี่ยวข้องกับใบสั่งงานในกลุ่มใบสั่งงาน บนบานหน้าต่างการดำเนินการ บนแท็บ **กลุ่มใบสั่งงาน** ในกลุ่ม **การจัดซื้อ** เลือก **การซื้อในใบสั่งงาน** เพื่อเปิดหน้ารายการ **การซื้อในใบสั่งงาน**</span><span class="sxs-lookup"><span data-stu-id="7d667-131">To view a list of purchase orders that are related to the work orders in the work order pool, on the Action Pane, on the **Work order pool** tab, in the **Procurement** group, select **Work order purchase** to open the **Work order purchase** list page.</span></span>

>[!NOTE]
><span data-ttu-id="7d667-132">เมื่อกลุ่มใบสั่งงานไม่เกี่ยวข้องกับการวางแผนงานของคุณอีกต่อไป ตั้งค่าตัวเลือก **เรียกใช้งาน** สำหรับกลุ่มนั้นให้เป็น **ไม่** ในมุมมองรายการของหน้า **กลุ่มใบสั่งงาน**</span><span class="sxs-lookup"><span data-stu-id="7d667-132">When a work order pool is no longer relevant to your work planning, set the **Active** option for that pool to **No** in the list view of the **Work order pool** page.</span></span>

<span data-ttu-id="7d667-133">ถ้าต้องการลบรายการใบสั่งงานทั้งหมด ตั้งค่าตัวเลือก **ลบความสัมพันธ์ของใบสั่งงาน** เป็น **ใช่**</span><span class="sxs-lookup"><span data-stu-id="7d667-133">To delete all worker order lines, set the **Delete work order relations** option to **Yes**.</span></span> <span data-ttu-id="7d667-134">ตัวเลือกนี้มีประโยชน์ ตัวอย่างเช่น ถ้าคุณต้องการสร้างกลุ่มที่ว่างเปล่าซึ่งคุณสามารถใช้ได้ในภายหลังสำหรับใบสั่งงานอื่นๆ</span><span class="sxs-lookup"><span data-stu-id="7d667-134">This option is useful if, for example, you want to create an empty pool that you can use later for other work orders.</span></span> <span data-ttu-id="7d667-135">เมื่อคุณพร้อมที่จะใช้กลุ่มใบสั่งงานเพื่อสร้างความสัมพันธ์ของใบสั่งงานใหม่ในภายหลัง อย่าลืมตั้งค่าตัวเลือก **ลบความสัมพันธ์ของใบสั่งงาน** เป็น **ไม่**</span><span class="sxs-lookup"><span data-stu-id="7d667-135">When you're ready to use the work order pool to create new work order relations later, remember to set the **Delete work order relations** option to **No**.</span></span>

<span data-ttu-id="7d667-136">ภาพประกอบด้านล่างแสดงตัวอย่างของหน้ารายการ **กลุ่มใบสั่งงาน**</span><span class="sxs-lookup"><span data-stu-id="7d667-136">The illustration below shows an example of the **Work order pool** list page.</span></span>

![รูปที่ 1](media/22-work-orders.png)


## <a name="add-a-work-order-to-a-work-order-pool"></a><span data-ttu-id="7d667-138">เพิ่มใบสั่งงานไปยังกลุ่มใบสั่งงาน</span><span class="sxs-lookup"><span data-stu-id="7d667-138">Add a work order to a work order pool</span></span>

<span data-ttu-id="7d667-139">ตามที่อธิบายไว้ในส่วนก่อนหน้านี้ คุณสามารถเพิ่มใบสั่งงานให้กับกลุ่มใบสั่งงานได้ เมื่อคุณสร้างกลุ่มนั้น</span><span class="sxs-lookup"><span data-stu-id="7d667-139">As described in the previous section, you can add work orders to a work order pool when you create that pool.</span></span> <span data-ttu-id="7d667-140">นอกจากนี้ คุณยังสามารถเพิ่มใบสั่งงานให้กับกลุ่มใบสั่งงานได้ในหน้ารายการ **ใบสั่งงานทั้งหมด** หรือ **ใบสั่งงานที่ใช้งานอยู่**</span><span class="sxs-lookup"><span data-stu-id="7d667-140">You can also add work orders to a work order pool on the **All work orders** or **Active work orders** list page.</span></span>

1. <span data-ttu-id="7d667-141">เลือกใบสั่งงาน และจากนั้น บนบานหน้าต่างการดำเนินการ บนแท็บ **ใบสั่งงาน** ในกลุ่ม **รักษา** ให้เลือก **กลุ่มใบสั่งงาน**</span><span class="sxs-lookup"><span data-stu-id="7d667-141">Select the work order, and then, on the Action Pane, on the **Work order** tab, in the **Maintain** group, select **Work order pool**.</span></span>

2. <span data-ttu-id="7d667-142">เลือกใบสั่งงานในรายการ และคลิก **กลุ่มใบสั่งงาน**</span><span class="sxs-lookup"><span data-stu-id="7d667-142">Select the work order in the list, and click **Work order pool**.</span></span>

3. <span data-ttu-id="7d667-143">ในกล่องโต้ตอบ **รักษากลุ่มใบสั่งงาน** ในฟิลด์ **เพิ่ม/ลบ** ให้เลือก **เพิ่ม**</span><span class="sxs-lookup"><span data-stu-id="7d667-143">In the **Maintain work order pool** dialog, in the **Add/remove** field, select **Add**.</span></span>

4. <span data-ttu-id="7d667-144">ในฟิลด์ **กลุ่ม** เลือกกลุ่มใบสั่งงาน</span><span class="sxs-lookup"><span data-stu-id="7d667-144">In the **Pool** field, select the work order pool.</span></span>

5. <span data-ttu-id="7d667-145">เลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="7d667-145">Select **OK**.</span></span>

6. <span data-ttu-id="7d667-146">เมื่อต้องการย้ายใบสั่งงานที่คุณได้เพิ่มเข้าไปในใบสั่งที่ระบุในกลุ่มใบสั่งงาน บนหน้ารายการ **กลุ่มใบสั่งงานทั้งหมด** หรือ **กลุ่มใบสั่งงานที่ใช้งานอยู่** ให้เลือกกลุ่ม และจากนั้น เลือก **แก้ไข**</span><span class="sxs-lookup"><span data-stu-id="7d667-146">To put the work order that you added in a specific order in the work order pool, on the **All work order pools** or **Active work order pools** list page, select the pool, and then select **Edit**.</span></span> <span data-ttu-id="7d667-147">จากนั้น บนหน้า **กลุ่มใบสั่งงาน** บน FastTab **ใบสั่งงาน** ให้ใช้ฟิลด์ **เรียงลำดับ** เพื่อปรับปรุงลำดับการจัดเรียงของใบสั่งงานที่รวมอยู่ในกลุ่ม</span><span class="sxs-lookup"><span data-stu-id="7d667-147">Then, on the **Work order pool** page, on the **Work orders** FastTab, use the **Sort order** field to adjust the sort order of the work orders that are included in pool.</span></span>

<span data-ttu-id="7d667-148">เพื่อลบใบสั่งงานออกจากกลุ่มใบสั่งงาน ให้ทำซ้ำขั้นตอนเหล่านี้ แต่เลือก **ลบ** ในขั้นตอนที่ 3</span><span class="sxs-lookup"><span data-stu-id="7d667-148">To remove a work order from a work order pool, repeat these steps, but select **Remove** in step 3.</span></span>

