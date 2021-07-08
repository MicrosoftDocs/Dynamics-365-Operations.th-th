---
title: กลุ่มการจัดการเงินคืน
description: หัวข้อนี้จะอธิบายวิธีการตั้งค่าข้อมูลสำหรับกลุ่มการจัดการเงินคืน กลุ่มการจัดการเงินคืนสามารถใช้ในระหว่างการคํานวณเงินคืนและสามารถแนบกับเรกคอร์ดหลักได้
author: sherry-zheng
ms.date: 02/19/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: TAMRebateGroup
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: chuzheng
ms.search.validFrom: 2021-02-19
ms.dyn365.ops.version: Release 10.0.18
ms.openlocfilehash: ee5a195b3d2881ff70fb1f0d4063ed681e874648
ms.sourcegitcommit: dc4898aa32f381620c517bf89c7856e693563ace
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 06/17/2021
ms.locfileid: "6271088"
---
# <a name="rebate-management-groups"></a><span data-ttu-id="9c482-104">กลุ่มการจัดการเงินคืน</span><span class="sxs-lookup"><span data-stu-id="9c482-104">Rebate management groups</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="9c482-105">การคํานวณการจัดการเงินคืนสามารถควบคุมโดยกลุ่มได้</span><span class="sxs-lookup"><span data-stu-id="9c482-105">Rebate management calculations can be driven by groups.</span></span> <span data-ttu-id="9c482-106">คุณสามารถสร้างกลุ่มการจัดการเงินคืนให้กับลูกค้า ผู้จัดจำหน่าย และสินค้าได้</span><span class="sxs-lookup"><span data-stu-id="9c482-106">Rebate management groups can be created for customers, vendors, and items.</span></span> <span data-ttu-id="9c482-107">สามารถแนบกับเรกคอร์ดหลักได้</span><span class="sxs-lookup"><span data-stu-id="9c482-107">They can be attached to a master record.</span></span>

## <a name="rebate-management-customer-groups"></a><span data-ttu-id="9c482-108">กลุ่มการจัดการเงินคืนให้กับลูกค้า</span><span class="sxs-lookup"><span data-stu-id="9c482-108">Rebate management customer groups</span></span>

<span data-ttu-id="9c482-109">การคํานวณกลุ่มลูกค้ามักสร้างขึ้นเป็นกลุ่มบริษัท เช่น ซุปเปอร์มาร์เก็ตลูกโซ่ หรือบริษัทแฟรนไซส์</span><span class="sxs-lookup"><span data-stu-id="9c482-109">The calculation for a group of customers is often created for a chain of companies, such as a supermarket chain or a franchise company.</span></span> <span data-ttu-id="9c482-110">การคํานวณชนิดนี้มักเกี่ยวข้องกับเงินคืน</span><span class="sxs-lookup"><span data-stu-id="9c482-110">This type of calculation is usually related to a rebate.</span></span>

<span data-ttu-id="9c482-111">การหักลดมักจะได้รับการคํานวณโดยไม่พิจารณาว่าขายใบสั่งคัดเลือกให้ใคร</span><span class="sxs-lookup"><span data-stu-id="9c482-111">A deduction is often calculated without considering who the qualifying order was sold to.</span></span> <span data-ttu-id="9c482-112">อย่างไรก็ตาม มีข้อยกเว้น</span><span class="sxs-lookup"><span data-stu-id="9c482-112">However, there are exceptions.</span></span> <span data-ttu-id="9c482-113">ตัวอย่างเช่น ผู้ได้รับลิขสิทธิ์อาจสร้างแผนงานการหักลดที่กลุ่มลูกค้า A จะได้รับ 4 เปอร์เซ็นต์ แต่กลุ่มลูกค้า B จะได้รับ 3 เปอร์เซ็นต์เท่านั้น</span><span class="sxs-lookup"><span data-stu-id="9c482-113">For example, a licensee might create a deduction scheme where customer group A will receive 4 percent, but customer group B will receive only 3 percent.</span></span>

### <a name="set-up-customer-groups"></a><span data-ttu-id="9c482-114">ตั้งค่ากลุ่มลูกค้า</span><span class="sxs-lookup"><span data-stu-id="9c482-114">Set up customer groups</span></span>

<span data-ttu-id="9c482-115">เมื่อต้องการใช้งานกลุ่มการจัดการเงินคืนให้กับกลุ่มลูกค้า ให้ไปที่ **การจัดการเงินคืน \> การตั้งค่ากลุ่มการจัดการเงินคืน \> กลุ่มลูกค้า**</span><span class="sxs-lookup"><span data-stu-id="9c482-115">To work with Rebate management customer groups, go to **Rebate management \> Rebate management groups setup \> Customer groups**.</span></span> <span data-ttu-id="9c482-116">คุณสามารถใช้ปุ่มในบานหน้าต่างการดำเนินการเพื่อเพิ่มและลบกลุ่มตามที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="9c482-116">You can use the buttons on the Action Pane to add and remove groups as required.</span></span> <span data-ttu-id="9c482-117">สำหรับแต่ละกลุ่ม ตั้งค่าฟิลด์ต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="9c482-117">For each group, set the following fields:</span></span>

- <span data-ttu-id="9c482-118">**กลุ่มการจัดการเงินคืน** – ป้อนชื่อเฉพาะสำหรับกลุ่ม</span><span class="sxs-lookup"><span data-stu-id="9c482-118">**Rebate management group** – Enter a unique name for the group.</span></span>
- <span data-ttu-id="9c482-119">**คำอธิบาย** – ป้อนอธิบายเกี่ยวกับกลุ่ม เพื่อดูข้อมูลเพิ่มเติมเกี่ยวกับวิธีการใช้</span><span class="sxs-lookup"><span data-stu-id="9c482-119">**Description** – Enter a description of the group to provide more information about how it should be used.</span></span>

### <a name="manage-customer-group-assignments"></a><span data-ttu-id="9c482-120">จัดการการมอบหมายกลุ่มลูกค้า</span><span class="sxs-lookup"><span data-stu-id="9c482-120">Manage customer group assignments</span></span>

<span data-ttu-id="9c482-121">ลูกค้าแต่ละคนสามารถอยู่ในกลุ่มการจัดการเงินคืนได้หลายกลุ่ม</span><span class="sxs-lookup"><span data-stu-id="9c482-121">Each customer can belong to any number of Rebate management groups.</span></span> <span data-ttu-id="9c482-122">เมื่อต้องการดูและกําหนดสมาชิกกลุ่ม คุณสามารถเริ่มต้นจากรายการกลุ่มหรือรายชื่อลูกค้า</span><span class="sxs-lookup"><span data-stu-id="9c482-122">To view and assign group members, you can start from either the group list or the customer list.</span></span>

<span data-ttu-id="9c482-123">เมื่อต้องการดู เพิ่ม หรือลบลูกค้าของกลุ่มที่เลือก ให้ปฏิบัติตามขั้นตอนต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="9c482-123">To view, add, or remove customers for a selected group, follow these steps.</span></span>

1. <span data-ttu-id="9c482-124">ไปที่ **การจัดการเงินคืน \> การตั้งค่ากลุ่มการจัดการเงินคืน \> กลุ่มลูกค้า**</span><span class="sxs-lookup"><span data-stu-id="9c482-124">Go to **Rebate management \> Rebate management groups setup \> Customer groups**.</span></span>
1. <span data-ttu-id="9c482-125">เลือกกลุ่มเพื่อจัดการ</span><span class="sxs-lookup"><span data-stu-id="9c482-125">Select the group to manage.</span></span>
1. <span data-ttu-id="9c482-126">บนบานหน้าต่างการดำเนินการ เลือก **ลูกค้า**</span><span class="sxs-lookup"><span data-stu-id="9c482-126">On the Action Pane, select **Customers**.</span></span> <span data-ttu-id="9c482-127">หน้า **กลุ่มการจัดการเงินคืน** จะปรากฏขึ้นและแสดงรายชื่อลูกค้าที่เป็นสมาชิกของกลุ่มที่เลือกแล้ว</span><span class="sxs-lookup"><span data-stu-id="9c482-127">The **Rebate management groups** page appears and shows a list of customers that are already members of the selected group.</span></span>
1. <span data-ttu-id="9c482-128">หากต้องการเพิ่มลูกค้าให้แก่กลุ่ม เลือก **สร้าง** ในบานหน้าต่างการดำเนินการเพื่อเพิ่มแถวไปยังกริด</span><span class="sxs-lookup"><span data-stu-id="9c482-128">To add a new customer to the group, select **New** on the Action Pane to add a row to the grid.</span></span> <span data-ttu-id="9c482-129">จากนั้นให้กำหนดฟิลด์ดังต่อไปนี้สำหรับแถวใหม่:</span><span class="sxs-lookup"><span data-stu-id="9c482-129">Then set the following field for the new row:</span></span>

    - <span data-ttu-id="9c482-130">**บัญชีลูกค้า** – เลือกรหัสบัญชีลูกค้า</span><span class="sxs-lookup"><span data-stu-id="9c482-130">**Customer account** – Select the customer account ID.</span></span>

1. <span data-ttu-id="9c482-131">เมื่อต้องการลบลูกค้าออกจากกลุ่ม ให้เลือกลูกค้า แล้วเลือก **ลบ** ในบานหน้าต่างการดำเนินการ</span><span class="sxs-lookup"><span data-stu-id="9c482-131">To remove a customer from the group, select the customer, and then select **Delete** on the Action Pane.</span></span>

<span data-ttu-id="9c482-132">เมื่อต้องการดู เพิ่ม หรือลบการกำหนดกลุ่มของลูกค้าที่เลือก ให้ปฏิบัติตามขั้นตอนต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="9c482-132">To view, add, or remove group assignments for a selected customer, follow these steps.</span></span>

1. <span data-ttu-id="9c482-133">ไปที่ **บัญชีลูกหนี้ \> ลูกค้า \> ลูกค้าทั้งหมด**</span><span class="sxs-lookup"><span data-stu-id="9c482-133">Go to **Accounts receivable \> Customers \> All customers**.</span></span>
1. <span data-ttu-id="9c482-134">เลือกลูกค้าที่จะทำงานด้วย</span><span class="sxs-lookup"><span data-stu-id="9c482-134">Select the customer to work with.</span></span>
1. <span data-ttu-id="9c482-135">บนบานหน้าต่างการดำเนินการ บนแท็บ **ลูกค้า** ในกลุ่ม **การจัดการเงินคืน** ให้เลือก **กลุ่มการจัดการเงินคืน**</span><span class="sxs-lookup"><span data-stu-id="9c482-135">On the Action Pane, on the **Customer** tab, in the **Rebate management** group, select **Rebate management groups**.</span></span> <span data-ttu-id="9c482-136">หน้า **กลุ่มการจัดการเงินคืน** จะปรากฏขึ้นและแสดงรายชื่อกลุ่มที่เป็นลูกค้าที่เลือกที่เป็นสมาชิกแล้ว</span><span class="sxs-lookup"><span data-stu-id="9c482-136">The **Rebate management groups** page appears and shows a list of groups that the selected customer already belongs to.</span></span>
1. <span data-ttu-id="9c482-137">หากต้องการเพิ่มลูกค้าให้แก่กลุ่มใหม่ เลือก **สร้าง** ในบานหน้าต่างการดำเนินการเพื่อเพิ่มแถวไปยังกริด</span><span class="sxs-lookup"><span data-stu-id="9c482-137">To add the customer to a new group, select **New** on the Action Pane to add a row to the grid.</span></span> <span data-ttu-id="9c482-138">จากนั้นให้กำหนดฟิลด์ดังต่อไปนี้สำหรับแถวใหม่:</span><span class="sxs-lookup"><span data-stu-id="9c482-138">Then set the following field for the new row:</span></span>

    - <span data-ttu-id="9c482-139">**กลุ่มการจัดการเงินคืน** – เลือกกลุ่มที่จะเพิ่มลูกค้า</span><span class="sxs-lookup"><span data-stu-id="9c482-139">**Rebate management group** – Select the group to add the customer to.</span></span>

1. <span data-ttu-id="9c482-140">เมื่อต้องการลบลูกค้าออกจากกลุ่ม ให้เลือกกลุ่ม แล้วเลือก **ลบ** ในบานหน้าต่างการดำเนินการ</span><span class="sxs-lookup"><span data-stu-id="9c482-140">To remove a customer from a group, select the group, and then select **Delete** on the Action Pane.</span></span>

## <a name="rebate-management-vendor-groups"></a><span data-ttu-id="9c482-141">กลุ่มการจัดการเงินคืนให้กับผู้จัดจำหน่าย</span><span class="sxs-lookup"><span data-stu-id="9c482-141">Rebate management vendor groups</span></span>

<span data-ttu-id="9c482-142">การคํานวณกลุ่มผู้จัดจำหน่ายมักจะถูกสร้างขึ้นมาให้กับกลุ่มจุดจัดส่ง</span><span class="sxs-lookup"><span data-stu-id="9c482-142">The calculation for a group of vendors is often created for a group of delivery points.</span></span> <span data-ttu-id="9c482-143">การคํานวณชนิดนี้มักเกี่ยวข้องกับเงินคืน</span><span class="sxs-lookup"><span data-stu-id="9c482-143">This type of calculation is usually related to a rebate.</span></span>

### <a name="set-up-vendor-groups"></a><span data-ttu-id="9c482-144">ตั้งค่ากลุ่มผู้จัดจำหน่าย</span><span class="sxs-lookup"><span data-stu-id="9c482-144">Set up vendor groups</span></span>

<span data-ttu-id="9c482-145">เมื่อต้องการใช้งานกลุ่มการจัดการเงินคืนให้กับผู้จัดจำหน่าย ให้ไปที่ **การจัดการเงินคืน \> การตั้งค่ากลุ่มการจัดการเงินคืน \> กลุ่มผู้จัดจำหน่าย**</span><span class="sxs-lookup"><span data-stu-id="9c482-145">To work with Rebate management vendor groups, go to **Rebate management \> Rebate management groups setup \> Vendor groups**.</span></span> <span data-ttu-id="9c482-146">คุณสามารถใช้ปุ่มในบานหน้าต่างการดำเนินการเพื่อเพิ่มและลบกลุ่มตามที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="9c482-146">You can use the buttons on the Action Pane to add and remove groups as required.</span></span> <span data-ttu-id="9c482-147">สำหรับแต่ละกลุ่ม ตั้งค่าฟิลด์ต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="9c482-147">For each group, set the following fields:</span></span>

- <span data-ttu-id="9c482-148">**กลุ่มการจัดการเงินคืน** – ป้อนชื่อเฉพาะสำหรับกลุ่ม</span><span class="sxs-lookup"><span data-stu-id="9c482-148">**Rebate management group** – Enter a unique name for the group.</span></span>
- <span data-ttu-id="9c482-149">**คำอธิบาย** – ป้อนอธิบายเกี่ยวกับกลุ่ม เพื่อดูข้อมูลเพิ่มเติมเกี่ยวกับวิธีการใช้</span><span class="sxs-lookup"><span data-stu-id="9c482-149">**Description** – Enter a description of the group to provide more information about how it should be used.</span></span>

### <a name="manage-vendor-group-assignments"></a><span data-ttu-id="9c482-150">จัดการการมอบหมายกลุ่มผู้จัดจำหน่าย</span><span class="sxs-lookup"><span data-stu-id="9c482-150">Manage vendor group assignments</span></span>

<span data-ttu-id="9c482-151">ผู้จัดจำหน่ายแต่ละคนสามารถอยู่ในกลุ่มการจัดการเงินคืนได้หลายกลุ่ม</span><span class="sxs-lookup"><span data-stu-id="9c482-151">Each vendor can belong to any number of Rebate management groups.</span></span> <span data-ttu-id="9c482-152">เมื่อต้องการดูและกําหนดสมาชิกกลุ่ม คุณสามารถเริ่มต้นจากรายการกลุ่มหรือรายชื่อผู้จัดจำหน่าย</span><span class="sxs-lookup"><span data-stu-id="9c482-152">To view and assign group members, you can start from either the group list or the vendor list.</span></span>

<span data-ttu-id="9c482-153">เมื่อต้องการดู เพิ่ม หรือลบผู้จัดจำหน่ายของกลุ่มที่เลือก ให้ปฏิบัติตามขั้นตอนต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="9c482-153">To view, add, or remove vendors for a selected group, follow these steps.</span></span>

1. <span data-ttu-id="9c482-154">ไปที่ **การจัดการเงินคืน \> การตั้งค่ากลุ่มการจัดการเงินคืน \> กลุ่มผู้จัดจำหน่าย**</span><span class="sxs-lookup"><span data-stu-id="9c482-154">Go to **Rebate management \> Rebate management groups setup \> Vendor groups**.</span></span>
1. <span data-ttu-id="9c482-155">เลือกกลุ่มเพื่อจัดการ</span><span class="sxs-lookup"><span data-stu-id="9c482-155">Select the group to manage.</span></span>
1. <span data-ttu-id="9c482-156">ในบานหน้าต่างการดำเนินการ เลือก **ผู้จัดจำหน่าย**</span><span class="sxs-lookup"><span data-stu-id="9c482-156">On the Action Pane, select **Vendors**.</span></span> <span data-ttu-id="9c482-157">หน้า **กลุ่มการจัดการเงินคืน** จะปรากฏขึ้นและแสดงรายชื่อผู้จัดจำหน่ายที่เป็นสมาชิกของกลุ่มที่เลือกแล้ว</span><span class="sxs-lookup"><span data-stu-id="9c482-157">The **Rebate management groups** page appears and shows a list of vendors that are already members of the selected group.</span></span>
1. <span data-ttu-id="9c482-158">หากต้องการเพิ่มผู้จัดจำหน่ายใหม่ให้แก่กลุ่ม เลือก **สร้าง** ในบานหน้าต่างการดำเนินการเพื่อเพิ่มแถวไปยังกริด</span><span class="sxs-lookup"><span data-stu-id="9c482-158">To add a new vendor to the group, select **New** on the Action Pane to add a row to the grid.</span></span> <span data-ttu-id="9c482-159">จากนั้นให้กำหนดฟิลด์ดังต่อไปนี้สำหรับแถวใหม่:</span><span class="sxs-lookup"><span data-stu-id="9c482-159">Then set the following field for the new row:</span></span>

    - <span data-ttu-id="9c482-160">**บัญชีผู้จัดจำหน่าย** – เลือกรหัสบัญชีผู้จัดจำหน่าย</span><span class="sxs-lookup"><span data-stu-id="9c482-160">**Vendor account** – Select the vendor account ID.</span></span>

1. <span data-ttu-id="9c482-161">เมื่อต้องการลบผู้จัดจำหน่ายออกจากกลุ่ม ให้เลือกผู้จัดจำหน่าย แล้วเลือก **ลบ** ในบานหน้าต่างการดำเนินการ</span><span class="sxs-lookup"><span data-stu-id="9c482-161">To remove a vendor from the group, select the vendor, and then select **Delete** on the Action Pane.</span></span>

<span data-ttu-id="9c482-162">เมื่อต้องการดู เพิ่ม หรือลบการกำหนดกลุ่มของผู้จัดจำหน่ายที่เลือก ให้ปฏิบัติตามขั้นตอนต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="9c482-162">To view, add, or remove group assignments for a selected vendor, follow these steps.</span></span>

1. <span data-ttu-id="9c482-163">ไปที่ **บัญชีเจ้าหนี้ \> ผู้จัดจำหน่าย \> ผู้จัดจำหน่ายทั้งหมด**</span><span class="sxs-lookup"><span data-stu-id="9c482-163">Go to **Accounts payable \> Vendors \> All vendors**.</span></span>
1. <span data-ttu-id="9c482-164">เลือกผู้จัดจำหน่ายที่จะทำงานด้วย</span><span class="sxs-lookup"><span data-stu-id="9c482-164">Select the vendor to work with.</span></span>
1. <span data-ttu-id="9c482-165">บนบานหน้าต่างการดำเนินการ บนแท็บ **ผู้จัดจำหน่าย** ในกลุ่ม **การจัดการเงินคืน** ให้เลือก **กลุ่มการจัดการเงินคืน**</span><span class="sxs-lookup"><span data-stu-id="9c482-165">On the Action Pane, on the **Vendor** tab, in the **Rebate management** group, select **Rebate management groups**.</span></span> <span data-ttu-id="9c482-166">หน้า **กลุ่มการจัดการเงินคืน** จะปรากฏขึ้นและแสดงรายชื่อกลุ่มที่เป็นผู้จัดจำหน่ายที่เลือกที่เป็นสมาชิกแล้ว</span><span class="sxs-lookup"><span data-stu-id="9c482-166">The **Rebate management groups** page appears and shows a list of groups that the selected vendor already belongs to.</span></span>
1. <span data-ttu-id="9c482-167">หากต้องการเพิ่มผู้จัดจำหน่ายให้แก่กลุ่มใหม่ เลือก **สร้าง** ในบานหน้าต่างการดำเนินการเพื่อเพิ่มแถวไปยังกริด</span><span class="sxs-lookup"><span data-stu-id="9c482-167">To add the vendor to a new group, select **New** on the Action Pane to add a row to the grid.</span></span> <span data-ttu-id="9c482-168">จากนั้นให้กำหนดฟิลด์ดังต่อไปนี้สำหรับแถวใหม่:</span><span class="sxs-lookup"><span data-stu-id="9c482-168">Then set the following field for the new row:</span></span>

    - <span data-ttu-id="9c482-169">**กลุ่มการจัดการเงินคืน** – เลือกกลุ่มที่จะเพิ่มผู้จัดจำหน่าย</span><span class="sxs-lookup"><span data-stu-id="9c482-169">**Rebate management group** – Select the group to add the vendor to.</span></span>

1. <span data-ttu-id="9c482-170">เมื่อต้องการลบผู้จัดจำหน่ายออกจากกลุ่ม ให้เลือกกลุ่ม แล้วเลือก **ลบ** ในบานหน้าต่างการดำเนินการ</span><span class="sxs-lookup"><span data-stu-id="9c482-170">To remove a vendor from a group, select the group, and then select **Delete** on the Action Pane.</span></span>

## <a name="item-rebate-groups"></a><span data-ttu-id="9c482-171">กลุ่มเงินคืนของสินค้า</span><span class="sxs-lookup"><span data-stu-id="9c482-171">Item rebate groups</span></span>

<span data-ttu-id="9c482-172">การจัดกลุ่มสินค้าช่วยให้คุณมีความยืดหยุ่นมากขึ้นเมื่อคํานวณเงินคืนและการหักลด</span><span class="sxs-lookup"><span data-stu-id="9c482-172">By grouping items, you have more flexibility when rebates and deductions are calculated.</span></span> <span data-ttu-id="9c482-173">วิธีการนี้มักจะเป็นวิธีที่มีประสิทธิภาพมากกว่าในการตั้งค่าเงินคืนและการหักลดของลูกค้าและผู้จัดจำหน่าย</span><span class="sxs-lookup"><span data-stu-id="9c482-173">This approach is often a more efficient way to set up rebates and deductions for customers and vendors.</span></span>

### <a name="set-up-item-groups"></a><span data-ttu-id="9c482-174">ตั้งค่ากลุ่มสินค้า</span><span class="sxs-lookup"><span data-stu-id="9c482-174">Set up item groups</span></span>

<span data-ttu-id="9c482-175">เมื่อต้องการใช้งานกลุ่มการจัดการเงินคืนให้กับกลุ่มสินค้า ให้ไปที่ **การจัดการเงินคืน \> การตั้งค่ากลุ่มการจัดการเงินคืน \> กลุ่มสินค้า**</span><span class="sxs-lookup"><span data-stu-id="9c482-175">To work with Rebate management item groups, go to **Rebate management \> Rebate management groups setup \> Item groups**.</span></span> <span data-ttu-id="9c482-176">คุณสามารถใช้ปุ่มในบานหน้าต่างการดำเนินการเพื่อเพิ่มและลบกลุ่มตามที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="9c482-176">You can use the buttons on the Action Pane to add and remove groups as required.</span></span> <span data-ttu-id="9c482-177">สำหรับแต่ละกลุ่ม ตั้งค่าฟิลด์ต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="9c482-177">For each group, set the following fields:</span></span>

- <span data-ttu-id="9c482-178">**กลุ่มการจัดการเงินคืน** – ป้อนชื่อเฉพาะสำหรับกลุ่ม</span><span class="sxs-lookup"><span data-stu-id="9c482-178">**Rebate management group** – Enter a unique name for the group.</span></span>
- <span data-ttu-id="9c482-179">**คำอธิบาย** – ป้อนอธิบายเกี่ยวกับกลุ่ม เพื่อดูข้อมูลเพิ่มเติมเกี่ยวกับวิธีการใช้</span><span class="sxs-lookup"><span data-stu-id="9c482-179">**Description** – Enter a description of the group to provide more information about how it should be used.</span></span>

### <a name="manage-item-group-assignments"></a><span data-ttu-id="9c482-180">จัดการการมอบหมายกลุ่มสินค้า</span><span class="sxs-lookup"><span data-stu-id="9c482-180">Manage item group assignments</span></span>

<span data-ttu-id="9c482-181">สินค้าแต่ละชิ้นสามารถอยู่ในกลุ่มการจัดการเงินคืนได้หลายกลุ่ม</span><span class="sxs-lookup"><span data-stu-id="9c482-181">Each item can belong to any number of Rebate management groups.</span></span> <span data-ttu-id="9c482-182">เมื่อต้องการดูและกําหนดสมาชิกกลุ่ม คุณสามารถเริ่มต้นจากรายการกลุ่มหรือรายการสินค้า</span><span class="sxs-lookup"><span data-stu-id="9c482-182">To view and assign group members, you can start from either the group list or the item list.</span></span> <span data-ttu-id="9c482-183">คุณยังสามารถเพิ่มสินค้าตามการจัดประเภทตามลำดับชั้นได้</span><span class="sxs-lookup"><span data-stu-id="9c482-183">You can also add items based on your category hierarchy.</span></span>

<span data-ttu-id="9c482-184">เมื่อต้องการดู เพิ่ม หรือลบสินค้าของกลุ่มที่เลือก ให้ปฏิบัติตามขั้นตอนต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="9c482-184">To view, add, or remove items for a selected group, follow these steps.</span></span>

1. <span data-ttu-id="9c482-185">ไปที่ **การจัดการเงินคืน \> การตั้งค่ากลุ่มการจัดการเงินคืน \> กลุ่มสินค้า**</span><span class="sxs-lookup"><span data-stu-id="9c482-185">Go to **Rebate management \> Rebate management groups setup \> Item groups**.</span></span>
1. <span data-ttu-id="9c482-186">เลือกกลุ่มเพื่อจัดการ</span><span class="sxs-lookup"><span data-stu-id="9c482-186">Select the group to manage.</span></span>
1. <span data-ttu-id="9c482-187">บนบานหน้าต่างการดำเนินการ เลือก **สินค้า**</span><span class="sxs-lookup"><span data-stu-id="9c482-187">On the Action Pane, select **Items**.</span></span> <span data-ttu-id="9c482-188">หน้า **กลุ่มการจัดการเงินคืน** จะปรากฏขึ้นและแสดงรายชื่อสินค้าที่เป็นสมาชิกของกลุ่มที่เลือกแล้ว</span><span class="sxs-lookup"><span data-stu-id="9c482-188">The **Rebate management groups** page appears and shows a list of items that are already members of the selected group.</span></span>
1. <span data-ttu-id="9c482-189">หากต้องการเพิ่มสินค้าใหม่ให้แก่กลุ่ม เลือก **สร้าง** ในบานหน้าต่างการดำเนินการเพื่อเพิ่มแถวไปยังกริด</span><span class="sxs-lookup"><span data-stu-id="9c482-189">To add a new item to the group, select **New** on the Action Pane to add a row to the grid.</span></span> <span data-ttu-id="9c482-190">จากนั้นให้กำหนดฟิลด์ดังต่อไปนี้สำหรับแถวใหม่:</span><span class="sxs-lookup"><span data-stu-id="9c482-190">Then set the following field for the new row:</span></span>

    - <span data-ttu-id="9c482-191">**บัญชีสินค้า** – เลือกรหัสบัญชีสินค้า</span><span class="sxs-lookup"><span data-stu-id="9c482-191">**Item account** – Select the item account ID.</span></span>

1. <span data-ttu-id="9c482-192">เมื่อต้องการลบสินค้าออกจากกลุ่ม ให้เลือกสินค้า แล้วเลือก **ลบ** ในบานหน้าต่างการดำเนินการ</span><span class="sxs-lookup"><span data-stu-id="9c482-192">To remove an item from the group, select the item, and then select **Delete** on the Action Pane.</span></span>

<span data-ttu-id="9c482-193">เมื่อต้องการดู เพิ่ม หรือลบการกำหนดกลุ่มของสินค้าที่เลือก ให้ปฏิบัติตามขั้นตอนต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="9c482-193">To view, add, or remove group assignments for a selected item, follow these steps.</span></span>

1. <span data-ttu-id="9c482-194">ไปยัง **การจัดการข้อมูลผลิตภัณฑ์ \> ผลิตภัณฑ์ \> ผลิตภัณฑ์ที่นำออกใช้**</span><span class="sxs-lookup"><span data-stu-id="9c482-194">Go to **Product information management \> Products \> Released products**.</span></span>
1. <span data-ttu-id="9c482-195">เลือกสินค้าที่จะทำงานด้วย</span><span class="sxs-lookup"><span data-stu-id="9c482-195">Select the item to work with.</span></span>
1. <span data-ttu-id="9c482-196">บนบานหน้าต่างการดำเนินการ บนแท็บ **ผลิตภัณฑ์** ในกลุ่ม **การจัดการเงินคืน** ให้เลือก **กลุ่มการจัดการเงินคืน**</span><span class="sxs-lookup"><span data-stu-id="9c482-196">On the Action Pane, on the **Product** tab, in the **Rebate management** group, select **Rebate management groups**.</span></span> <span data-ttu-id="9c482-197">หน้า **กลุ่มการจัดการเงินคืน** จะปรากฏขึ้นและแสดงรายชื่อกลุ่มที่เป็นสินค้าที่เลือกที่เป็นสมาชิกแล้ว</span><span class="sxs-lookup"><span data-stu-id="9c482-197">The **Rebate management groups** page appears and shows a list of groups that the selected item already belongs to.</span></span>
1. <span data-ttu-id="9c482-198">หากต้องการเพิ่มสินค้าให้แก่กลุ่มใหม่ เลือก **สร้าง** ในบานหน้าต่างการดำเนินการเพื่อเพิ่มแถวไปยังกริด</span><span class="sxs-lookup"><span data-stu-id="9c482-198">To add the item to a new group, select **New** on the Action Pane to add a row to the grid.</span></span> <span data-ttu-id="9c482-199">จากนั้นให้กำหนดฟิลด์ดังต่อไปนี้สำหรับแถวใหม่:</span><span class="sxs-lookup"><span data-stu-id="9c482-199">Then set the following field for the new row:</span></span>

    - <span data-ttu-id="9c482-200">**กลุ่มการจัดการเงินคืน** – เลือกกลุ่มที่จะเพิ่มสินค้า</span><span class="sxs-lookup"><span data-stu-id="9c482-200">**Rebate management group** – Select the group to add the item to.</span></span>

1. <span data-ttu-id="9c482-201">เมื่อต้องการลบสินค้าออกจากกลุ่ม ให้เลือกกลุ่ม แล้วเลือก **ลบ** ในบานหน้าต่างการดำเนินการ</span><span class="sxs-lookup"><span data-stu-id="9c482-201">To remove an item from a group, select the group, and then select **Delete** on the Action Pane.</span></span>

<span data-ttu-id="9c482-202">ในการเพิ่มสินค้าลงในกลุ่มตามการจัดประเภทตามลำดับชั้นของคุณ ให้ปฏิบัติตามขั้นตอนต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="9c482-202">To add items to a group based on your category hierarchy, follow these steps.</span></span>

1. <span data-ttu-id="9c482-203">ไปที่ **การจัดการเงินคืน \> การตั้งค่ากลุ่มการจัดการเงินคืน \> กลุ่มสินค้า**</span><span class="sxs-lookup"><span data-stu-id="9c482-203">Go to **Rebate management \> Rebate management groups setup \> Item groups**.</span></span>
1. <span data-ttu-id="9c482-204">เลือกกลุ่มเพื่อจัดการ</span><span class="sxs-lookup"><span data-stu-id="9c482-204">Select the group to manage.</span></span>
1. <span data-ttu-id="9c482-205">บนบานหน้าต่างการดำเนินการ เลือก **เพิ่มสินค้า**</span><span class="sxs-lookup"><span data-stu-id="9c482-205">On the Action Pane, select **Add items**.</span></span>
1. <span data-ttu-id="9c482-206">ในกล่องโต้ตอบ **เพิ่มสินค้า** ในฟิลด์ **การจัดประเภทตามลำดับชั้น** ให้เลือกประเภทระดับบนสุด</span><span class="sxs-lookup"><span data-stu-id="9c482-206">In the **Add items** dialog box, in the **Category hierarchy** field, select a top-level category.</span></span>
1. <span data-ttu-id="9c482-207">ลำดับชั้นสินค้าจะปรากฏในบานหน้าต่างด้านซ้าย</span><span class="sxs-lookup"><span data-stu-id="9c482-207">The item hierarchy is opened in the left pane.</span></span> <span data-ttu-id="9c482-208">เลือกระดับลำดับชั้นที่คุณค้นหา</span><span class="sxs-lookup"><span data-stu-id="9c482-208">Select the hierarchy level that you're looking for.</span></span> 
1. <span data-ttu-id="9c482-209">ขณะนี้รายการจากลำดับชั้นและระดับลำดับชั้นที่เลือกจะแสดงรายการอยู่ในบานหน้าต่างด้านขวา</span><span class="sxs-lookup"><span data-stu-id="9c482-209">Items from the selected hierarchy and hierarchy level are now listed in the right pane.</span></span> <span data-ttu-id="9c482-210">ปฏิบัติตามขั้นตอนต่อไปนี้เพื่อใช้งานบานหน้าต่าง:</span><span class="sxs-lookup"><span data-stu-id="9c482-210">Follow these steps to work with the pane:</span></span>

    - <span data-ttu-id="9c482-211">เลือกกล่องกาเครื่องหมายของแต่ละสินค้าที่คุณต้องการใส่ไว้ในลำดับขั้นดังกล่าว</span><span class="sxs-lookup"><span data-stu-id="9c482-211">Select the check box for each item that you want to add.</span></span>
    - <span data-ttu-id="9c482-212">เลือกกล่องกาเครื่องหมายบนส่วนหน้าของกริด เพื่อเลือกรายการทั้งหมดที่จะแสดงรายการ</span><span class="sxs-lookup"><span data-stu-id="9c482-212">Select the check box on the grid header to select all the items that are listed.</span></span>
    - <span data-ttu-id="9c482-213">เลือกปุ่ม **แสดงที่เลือก** เพื่อกรองข้อมูลกริด เพื่อให้แสดงเฉพาะรายการที่คุณเลือกจนถึงขณะนี้</span><span class="sxs-lookup"><span data-stu-id="9c482-213">Select the **Show selected** button to filter the grid so that it shows only the items that you've selected so far.</span></span> <span data-ttu-id="9c482-214">เลือกปุ่มอีกครั้งเพื่อกลับไปที่รายการทั้งหมด</span><span class="sxs-lookup"><span data-stu-id="9c482-214">Select the button again to return to the full list.</span></span>

1. <span data-ttu-id="9c482-215">เลือก **ตกลง** เพื่อใช้การเลือกสินค้าของคุณกับกลุ่มที่เลือก</span><span class="sxs-lookup"><span data-stu-id="9c482-215">Select **OK** to apply your item selection to the selected group.</span></span>
