---
title: อัพเดตงบประมาณการบำรุงรักษา
description: หัวข้อนี้อธิบายวิธีการอัพเดตงบประมาณการบำรุงรักษาในการจัดการสินทรัพย์
author: josaw1
manager: AnnBe
ms.date: 08/13/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CatProcureCatalogEdit, CatProcureCatalogListPage
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-08-30
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 486782968816cc585d9cf2d753f32e82f85e4f7e
ms.sourcegitcommit: 802dbf0a744d70f9e546632d419415b0993331ab
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 08/13/2019
ms.locfileid: "1874796"
---
# <a name="update-maintenance-budgets"></a><span data-ttu-id="c9f61-103">อัพเดตงบประมาณการบำรุงรักษา</span><span class="sxs-lookup"><span data-stu-id="c9f61-103">Update maintenance budgets</span></span>

[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]

<span data-ttu-id="c9f61-104">หน้า **รายการงบประมาณการบำรุงรักษา** แสดงรายการงบประมาณทั้งหมดที่สร้างขึ้นสำหรับงบประมาณที่เลือกบนหน้า **หน้างบประมาณการบำรุงรักษา**</span><span class="sxs-lookup"><span data-stu-id="c9f61-104">The **Maintenance budget lines** page shows all the budget lines that have been created for the budget that is selected on the **Maintenance budgets** page.</span></span> <span data-ttu-id="c9f61-105">(สำหรับข้อมูลเพิ่มเติม ให้ดู [สร้างงบประมาณการบำรุงรักษา](create-maintenance-budget.md)) คุณสามารถคำนวณใหม่และปรับปรุงรายการงบประมาณการบำรุงรักษาจนกว่าจะมีการอนุมัติงบประมาณการบำรุงรักษา</span><span class="sxs-lookup"><span data-stu-id="c9f61-105">(For more information, see [Create maintenance budgets](create-maintenance-budget.md).) You can recalculate and adjust maintenance budget lines until the maintenance budget is approved.</span></span> <span data-ttu-id="c9f61-106">หลังจากผ่านรอบระยะเวลางบประมาณแล้ว และต้นทุนถูกลงรายการบัญชีในการจัดการสินทรัพย์แล้ว คุณยังสามารถอัพเดตรายการงบประมาณที่มีต้นทุนจริงได้ด้วย</span><span class="sxs-lookup"><span data-stu-id="c9f61-106">After the budget period has passed, and costs have been posted in Asset Management, you can also update the budget lines with actual costs.</span></span>

## <a name="recalculate-a-maintenance-budget"></a><span data-ttu-id="c9f61-107">คำนวณงบประมาณการบำรุงรักษาใหม่</span><span class="sxs-lookup"><span data-stu-id="c9f61-107">Recalculate a maintenance budget</span></span>

<span data-ttu-id="c9f61-108">คุณสามารถคำนวณงบประมาณการบำรุงรักษาใหม่บนหน้า **รายการงบประมาณการบำรุงรักษา**</span><span class="sxs-lookup"><span data-stu-id="c9f61-108">You can recalculate a maintenance budget on the **Maintenance budget lines** page.</span></span> <span data-ttu-id="c9f61-109">เมื่อคุณคำนวณงบประมาณการบำรุงรักษาใหม่ รายการงบประมาณที่มีอยู่จะถูกลบออก และทำการคำนวณใหม่</span><span class="sxs-lookup"><span data-stu-id="c9f61-109">When you recalculate a maintenance budget, the existing budget lines are deleted, and a new calculation is done.</span></span>

1. <span data-ttu-id="c9f61-110">บนหน้า **รายการงบประมาณการบำรุงรักษา** ให้เลือก **คำนวณอีกครั้ง**</span><span class="sxs-lookup"><span data-stu-id="c9f61-110">On the **Maintenance budget lines** page, select **Recalculate**.</span></span>
2. <span data-ttu-id="c9f61-111">ในกล่องโต้ตอบ **การคำนวณงบประมาณใหม่** ให้ทำการเปลี่ยนแปลงที่จำเป็นสำหรับการคำนวณใหม่ แล้วเลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="c9f61-111">In the **Recalculate budget** dialog box, make the required changes for the new calculation, and then select **OK**.</span></span>

<span data-ttu-id="c9f61-112">รายการงบประมาณใหม่จะถูกสร้างขึ้นตามค่าที่คุณกำหนดไว้</span><span class="sxs-lookup"><span data-stu-id="c9f61-112">New budget lines are created according to the values that you set.</span></span>

## <a name="adjust-budget-lines"></a><span data-ttu-id="c9f61-113">ปรับปรุงรายการงบประมาณ</span><span class="sxs-lookup"><span data-stu-id="c9f61-113">Adjust budget lines</span></span>

<span data-ttu-id="c9f61-114">แทนที่จะคำนวณงบประมาณการบำรุงรักษาใหม่ทั้งหมด คุณสามารถปรับปรุงรายการที่เลือกที่เกี่ยวข้องกับต้นทุนงบประมาณได้</span><span class="sxs-lookup"><span data-stu-id="c9f61-114">Instead of recalculating the whole maintenance budget, you can adjust selected lines that are related to budget costs.</span></span>

1. <span data-ttu-id="c9f61-115">บนหน้า **รายการงบประมาณการบำรุงรักษา** ให้เลือกรายการที่จะอัพเดตต้นทุนงบประมาณ</span><span class="sxs-lookup"><span data-stu-id="c9f61-115">On the **Maintenance budget lines** page, select the lines to update the budget cost for.</span></span>
2. <span data-ttu-id="c9f61-116">เลือก **ปรับปรุง**</span><span class="sxs-lookup"><span data-stu-id="c9f61-116">Select **Adjust**.</span></span>
3. <span data-ttu-id="c9f61-117">ถ้าต้องการเพิ่มจำนวนรายการที่เลือก ให้เลือกกล่องกาเครื่องหมาย **เพิ่มต้นทุน** แล้วป้อนค่าในฟิลด์ **เพิ่มค่า**</span><span class="sxs-lookup"><span data-stu-id="c9f61-117">To add an amount to the selected lines, select the **Add cost** check box, and then enter the value in the **Add value** field.</span></span>
4. <span data-ttu-id="c9f61-118">ถ้าต้องการคูณต้นทุนงบประมาณในรายการงบประมาณที่เลือกตามสัดส่วน ให้เลือกกล่องกาเครื่องหมาย **คูณต้นทุน** และป้อนตัวคูณในฟิลด์ **ค่าการคูณ**</span><span class="sxs-lookup"><span data-stu-id="c9f61-118">To multiply the budget cost on the selected budget lines by a factor, select the **Multiply cost** check box, and enter the factor in the **Multiply value** field.</span></span>

    <span data-ttu-id="c9f61-119">ตัวอย่างเช่น ถ้าคุณป้อน **1.2** ในฟิลด์ **ค่าการคูณ** คุณจะเพิ่มต้นทุนงบประมาณในรายการที่เลือก 20 เปอร์เซ็นต์</span><span class="sxs-lookup"><span data-stu-id="c9f61-119">For example, if you enter **1.2** in the **Multiply value** field, you increase the budget cost on the selected lines by 20 percent.</span></span> <span data-ttu-id="c9f61-120">ถ้าคุณป้อน **0.7** คุณลดต้นทุนงบประมาณในรายการที่เลือก 30 เปอร์เซ็นต์</span><span class="sxs-lookup"><span data-stu-id="c9f61-120">If you enter **0.7**, you reduce the budget cost on the selected lines by 30 percent.</span></span>

5. <span data-ttu-id="c9f61-121">เลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="c9f61-121">Select **OK**.</span></span>

<span data-ttu-id="c9f61-122">รายการงบประมาณที่เลือกมีการอัพเดตตามค่าที่คุณกำหนดไว้ในขั้นตอนที่ 3 หรือ 4</span><span class="sxs-lookup"><span data-stu-id="c9f61-122">The selected budget lines are updated according to the values that you set in step 3 or 4.</span></span>

## <a name="update-actual-costs"></a><span data-ttu-id="c9f61-123">อัพเดตต้นทุนจริง</span><span class="sxs-lookup"><span data-stu-id="c9f61-123">Update actual costs</span></span>

<span data-ttu-id="c9f61-124">หลังจากผ่านวันทีรายการงบประมาณแล้ว และต้นทุนจริงถูกลงรายการบัญชีในการจัดการสินทรัพย์แล้ว คุณสามารถอัพเดตต้นทุนจริงบนงบประมาณการบำรุงรักษา</span><span class="sxs-lookup"><span data-stu-id="c9f61-124">After the dates on the budget lines have passed, and actual costs have been posted in Asset Management, you can update the actual costs on the maintenance budget.</span></span>

1. <span data-ttu-id="c9f61-125">บนหน้า **รายการงบประมาณการบำรุงรักษา** ให้เลือก **อัพเดตต้นทุน**</span><span class="sxs-lookup"><span data-stu-id="c9f61-125">On the **Maintenance budget lines** page, select **Update cost**.</span></span>
2. <span data-ttu-id="c9f61-126">ในกล่องโต้ตอบ **คำนวณต้นทุนจริง** ให้เลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="c9f61-126">In the **Calculate actual cost** dialog box, select **OK**.</span></span>

<span data-ttu-id="c9f61-127">ฟิลด์ **ต้นทุนจริง** ในรายการงบประมาณจะถูกอัพเดตเมื่อมีการลงรายการบัญชีต้นทุนจริง</span><span class="sxs-lookup"><span data-stu-id="c9f61-127">The **Actual cost** fields on the budget lines are updated if actual costs have been posted.</span></span> <span data-ttu-id="c9f61-128">รายการบประมาณใหม่อาจมีการสร้างขึ้น ถ้ามีการสร้างชนิดสินทรัพย์ใหม่ตั้งแต่คุณสร้างงบประมาณ และถ้ามีการใช้ชนิดสินทรัพย์เหล่านั้นกับสินทรัพย์ที่มีการสร้างใบสั่งงานแล้ว และมีการลงรายการบัญชีต้นทุนที่เกี่ยวข้อง</span><span class="sxs-lookup"><span data-stu-id="c9f61-128">New budget lines might be generated if new asset types have been created since you created the budget, and if those asset types have been used on assets that work orders have been created for and related costs have been posted for.</span></span> <span data-ttu-id="c9f61-129">รายการงบประมาณใหม่แสดงเฉพาะต้นทุนจริงเท่านั้น เนื่องจากไม่มีการคำนวณต้นทุนงบประมาณดังกล่าว</span><span class="sxs-lookup"><span data-stu-id="c9f61-129">New budget lines show only actual costs, because no budget costs were calculated for them.</span></span>

> [!NOTE]
> <span data-ttu-id="c9f61-130">เมื่อต้องการดูภาพรวมของต้นทุนจริงที่แบ่งเป็นต้นทุนเชิงป้องกัน ต้นทุนที่แก้ไข และต้นทุนการลงทุน คุณสามารถคำนวณสำหรับรอบระยะเวลาเดียวกันบนหน้า **การควบคุมต้นทุนสินทรัพย์** ได้</span><span class="sxs-lookup"><span data-stu-id="c9f61-130">To see an overview of actual costs divided into preventive, corrective, and investment costs, you can do a calculation for the same period on the **Asset cost control** page.</span></span> 

## <a name="manually-add-budget-lines"></a><span data-ttu-id="c9f61-131">เพิ่มรายการงบประมาณด้วยตนเอง</span><span class="sxs-lookup"><span data-stu-id="c9f61-131">Manually add budget lines</span></span>

<span data-ttu-id="c9f61-132">บนหน้า **รายการงบประมาณการบำรุงรักษา** คุณสามารถเพิ่มรายการงบประมาณใหม่ด้วยตนเองได้ด้วยการเลือก **สร้าง** แล้วทำการเลือกบนรายการ</span><span class="sxs-lookup"><span data-stu-id="c9f61-132">On the **Maintenance budget lines** page, you can manually add a new budget line by selecting **New** and then making selections on the line.</span></span> <span data-ttu-id="c9f61-133">ต่อไปนี้เป็นตัวอย่างของสถานการณ์ที่วิธีการนี้อาจเป็นประโยชน์</span><span class="sxs-lookup"><span data-stu-id="c9f61-133">Here are some examples of situations where this approach might be useful:</span></span>

- <span data-ttu-id="c9f61-134">คุณทราบว่ามีการปรับปรุงสินทรัพย์บางอย่างในขณะนี้อยู่ในระยะการวางแผน แต่ยังไม่ได้มีการสร้างงานที่เกี่ยวข้องในการจัดการสินทรัพย์</span><span class="sxs-lookup"><span data-stu-id="c9f61-134">You know that refurbishment of some assets is currently in the planning phase, but related jobs haven't yet been created in Asset Management.</span></span> <span data-ttu-id="c9f61-135">อย่างไรก็ตาม คุณต้องการต้นทุนงบประมาณสำหรับงานเหล่านั้นเพื่อรวมในงบประมาณการบำรุงรักษา</span><span class="sxs-lookup"><span data-stu-id="c9f61-135">However, you want budget costs for those jobs to be included in the maintenance budget.</span></span>
- <span data-ttu-id="c9f61-136">สินทรัพย์หรือชนิดสินทรัพย์ใหม่ถูกสร้างขึ้นตั้งแต่คุณทำงบประมาณการบำรุงรักษา แต่ยังไม่มีการตั้งค่าแผนการบำรุงรักษาในสินทรัพย์หรือชนิดสินทรัพย์เหล่านั้น</span><span class="sxs-lookup"><span data-stu-id="c9f61-136">New assets or asset types have been created since you made the maintenance budget, but maintenance plans haven't yet been set up on those assets or asset types.</span></span> <span data-ttu-id="c9f61-137">อย่างไรก็ตาม คุณต้องการต้นทุนงบประมาณสำหรับชนิดสินทรัพย์เหล่านั้นเพื่อรวมในงบประมาณการบำรุงรักษา</span><span class="sxs-lookup"><span data-stu-id="c9f61-137">However, you want budget costs for those asset types to be included in the maintenance budget.</span></span>
