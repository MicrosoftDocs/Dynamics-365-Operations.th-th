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
ms.openlocfilehash: c9e1cadae97bd8f0dea270deaa1a8e09bb28eb4b
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 05/11/2021
ms.locfileid: "6020494"
---
# <a name="rebate-management-groups"></a><span data-ttu-id="c6130-104">กลุ่มการจัดการเงินคืน</span><span class="sxs-lookup"><span data-stu-id="c6130-104">Rebate management groups</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="c6130-105">การคํานวณเงินคืนและการหักลดสามารถควบคุมโดยกลุ่มได้</span><span class="sxs-lookup"><span data-stu-id="c6130-105">Rebate and deduction calculations can be driven by groups.</span></span> <span data-ttu-id="c6130-106">คุณสามารถสร้างกลุ่มการจัดการเงินคืนให้กับลูกค้า ผู้จัดจำหน่าย และสินค้าได้</span><span class="sxs-lookup"><span data-stu-id="c6130-106">Rebate management groups can be created for customers, vendors, and items.</span></span> <span data-ttu-id="c6130-107">สามารถแนบกับเรกคอร์ดหลักได้</span><span class="sxs-lookup"><span data-stu-id="c6130-107">They can be attached to a master record.</span></span>

## <a name="rebate-management-customer-groups"></a><span data-ttu-id="c6130-108">กลุ่มการจัดการเงินคืนให้กับลูกค้า</span><span class="sxs-lookup"><span data-stu-id="c6130-108">Rebate management customer groups</span></span>

<span data-ttu-id="c6130-109">การคํานวณกลุ่มลูกค้ามักสร้างขึ้นเป็นกลุ่มบริษัท เช่น ซุปเปอร์มาร์เก็ตลูกโซ่ หรือบริษัทแฟรนไซส์</span><span class="sxs-lookup"><span data-stu-id="c6130-109">The calculation for a group of customers is often created for a chain of companies, such as a supermarket chain or a franchise company.</span></span> <span data-ttu-id="c6130-110">การคํานวณชนิดนี้มักเกี่ยวข้องกับเงินคืน</span><span class="sxs-lookup"><span data-stu-id="c6130-110">This type of calculation is usually related to a rebate.</span></span>

<span data-ttu-id="c6130-111">การหักลดมักจะได้รับการคํานวณโดยไม่พิจารณาว่าขายใบสั่งคัดเลือกให้ใคร</span><span class="sxs-lookup"><span data-stu-id="c6130-111">A deduction is often calculated without considering who the qualifying order was sold to.</span></span> <span data-ttu-id="c6130-112">อย่างไรก็ตาม มีข้อยกเว้น</span><span class="sxs-lookup"><span data-stu-id="c6130-112">However, there are exceptions.</span></span> <span data-ttu-id="c6130-113">ตัวอย่างเช่น ผู้ได้รับลิขสิทธิ์อาจสร้างแผนงานการหักลดที่กลุ่มลูกค้า A จะได้รับ 4 เปอร์เซ็นต์ แต่กลุ่มลูกค้า B จะได้รับ 3 เปอร์เซ็นต์เท่านั้น</span><span class="sxs-lookup"><span data-stu-id="c6130-113">For example, a licensee might create a deduction scheme where customer group A will receive 4 percent, but customer group B will receive only 3 percent.</span></span>

### <a name="set-up-customer-groups"></a><span data-ttu-id="c6130-114">ตั้งค่ากลุ่มลูกค้า</span><span class="sxs-lookup"><span data-stu-id="c6130-114">Set up customer groups</span></span>

<span data-ttu-id="c6130-115">เมื่อต้องการใช้งานกลุ่มการจัดการเงินคืนให้กับกลุ่มลูกค้า ให้ไปที่ **การจัดการเงินคืน \> การตั้งค่ากลุ่มการจัดการเงินคืน \> กลุ่มลูกค้า**</span><span class="sxs-lookup"><span data-stu-id="c6130-115">To work with Rebate management customer groups, go to **Rebate management \> Rebate management groups setup \> Customer groups**.</span></span> <span data-ttu-id="c6130-116">คุณสามารถใช้ปุ่มในบานหน้าต่างการดำเนินการเพื่อเพิ่มและลบกลุ่มตามที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="c6130-116">You can use the buttons on the Action Pane to add and remove groups as required.</span></span> <span data-ttu-id="c6130-117">สำหรับแต่ละกลุ่ม ตั้งค่าฟิลด์ต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="c6130-117">For each group, set the following fields:</span></span>

- <span data-ttu-id="c6130-118">**กลุ่มการจัดการเงินคืน** – ป้อนชื่อเฉพาะสำหรับกลุ่ม</span><span class="sxs-lookup"><span data-stu-id="c6130-118">**Rebate management group** – Enter a unique name for the group.</span></span>
- <span data-ttu-id="c6130-119">**คำอธิบาย** – ป้อนอธิบายเกี่ยวกับกลุ่ม เพื่อดูข้อมูลเพิ่มเติมเกี่ยวกับวิธีการใช้</span><span class="sxs-lookup"><span data-stu-id="c6130-119">**Description** – Enter a description of the group to provide more information about how it should be used.</span></span>

### <a name="manage-customer-group-assignments"></a><span data-ttu-id="c6130-120">จัดการการมอบหมายกลุ่มลูกค้า</span><span class="sxs-lookup"><span data-stu-id="c6130-120">Manage customer group assignments</span></span>

<span data-ttu-id="c6130-121">ลูกค้าแต่ละคนสามารถอยู่ในกลุ่มการจัดการเงินคืนได้หลายกลุ่ม</span><span class="sxs-lookup"><span data-stu-id="c6130-121">Each customer can belong to any number of Rebate management groups.</span></span> <span data-ttu-id="c6130-122">เมื่อต้องการดูและกําหนดสมาชิกกลุ่ม คุณสามารถเริ่มต้นจากรายการกลุ่มหรือรายชื่อลูกค้า</span><span class="sxs-lookup"><span data-stu-id="c6130-122">To view and assign group members, you can start from either the group list or the customer list.</span></span>

<span data-ttu-id="c6130-123">เมื่อต้องการดู เพิ่ม หรือลบลูกค้าของกลุ่มที่เลือก ให้ปฏิบัติตามขั้นตอนต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="c6130-123">To view, add, or remove customers for a selected group, follow these steps.</span></span>

1. <span data-ttu-id="c6130-124">ไปที่ **การจัดการเงินคืน \> การตั้งค่ากลุ่มการจัดการเงินคืน \> กลุ่มลูกค้า**</span><span class="sxs-lookup"><span data-stu-id="c6130-124">Go to **Rebate management \> Rebate management groups setup \> Customer groups**.</span></span>
1. <span data-ttu-id="c6130-125">เลือกกลุ่มเพื่อจัดการ</span><span class="sxs-lookup"><span data-stu-id="c6130-125">Select the group to manage.</span></span>
1. <span data-ttu-id="c6130-126">บนบานหน้าต่างการดำเนินการ เลือก **ลูกค้า**</span><span class="sxs-lookup"><span data-stu-id="c6130-126">On the Action Pane, select **Customers**.</span></span> <span data-ttu-id="c6130-127">หน้า **กลุ่มการจัดการเงินคืน** จะปรากฏขึ้นและแสดงรายชื่อลูกค้าที่เป็นสมาชิกของกลุ่มที่เลือกแล้ว</span><span class="sxs-lookup"><span data-stu-id="c6130-127">The **Rebate management groups** page appears and shows a list of customers that are already members of the selected group.</span></span>
1. <span data-ttu-id="c6130-128">หากต้องการเพิ่มลูกค้าให้แก่กลุ่ม เลือก **สร้าง** ในบานหน้าต่างการดำเนินการเพื่อเพิ่มแถวไปยังกริด</span><span class="sxs-lookup"><span data-stu-id="c6130-128">To add a new customer to the group, select **New** on the Action Pane to add a row to the grid.</span></span> <span data-ttu-id="c6130-129">จากนั้นให้กำหนดฟิลด์ดังต่อไปนี้สำหรับแถวใหม่:</span><span class="sxs-lookup"><span data-stu-id="c6130-129">Then set the following fields for the new row:</span></span>

    - <span data-ttu-id="c6130-130">**บัญชีลูกค้า** – เลือกรหัสบัญชีลูกค้า</span><span class="sxs-lookup"><span data-stu-id="c6130-130">**Customer account** – Select the customer account ID.</span></span>
    - <span data-ttu-id="c6130-131">**ชื่อ** – ป้อนชื่อและ/หรือคำอธิบายเกี่ยวกับลูกค้า</span><span class="sxs-lookup"><span data-stu-id="c6130-131">**Name** – Enter a name and/or description of the customer.</span></span>

1. <span data-ttu-id="c6130-132">เมื่อต้องการลบลูกค้าออกจากกลุ่ม ให้เลือกลูกค้า แล้วเลือก **ลบ** ในบานหน้าต่างการดำเนินการ</span><span class="sxs-lookup"><span data-stu-id="c6130-132">To remove a customer from the group, select the customer, and then select **Delete** on the Action Pane.</span></span>

<span data-ttu-id="c6130-133">เมื่อต้องการดู เพิ่ม หรือลบการกำหนดกลุ่มของลูกค้าที่เลือก ให้ปฏิบัติตามขั้นตอนต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="c6130-133">To view, add, or remove group assignments for a selected customer, follow these steps.</span></span>

1. <span data-ttu-id="c6130-134">ไปที่ **บัญชีลูกหนี้ \> ลูกค้า \> ลูกค้าทั้งหมด**</span><span class="sxs-lookup"><span data-stu-id="c6130-134">Go to **Accounts receivable \> Customers \> All customers**.</span></span>
1. <span data-ttu-id="c6130-135">เลือกลูกค้าที่จะทำงานด้วย</span><span class="sxs-lookup"><span data-stu-id="c6130-135">Select the customer to work with.</span></span>
1. <span data-ttu-id="c6130-136">บนบานหน้าต่างการดำเนินการ บนแท็บ **ลูกค้า** ในกลุ่ม **การจัดการเงินคืน** ให้เลือก **กลุ่มการจัดการเงินคืน**</span><span class="sxs-lookup"><span data-stu-id="c6130-136">On the Action Pane, on the **Customer** tab, in the **Rebate management** group, select **Rebate management groups**.</span></span> <span data-ttu-id="c6130-137">หน้า **กลุ่มการจัดการเงินคืน** จะปรากฏขึ้นและแสดงรายชื่อกลุ่มที่เป็นลูกค้าที่เลือกที่เป็นสมาชิกแล้ว</span><span class="sxs-lookup"><span data-stu-id="c6130-137">The **Rebate management groups** page appears and shows a list of groups that the selected customer already belongs to.</span></span>
1. <span data-ttu-id="c6130-138">หากต้องการเพิ่มลูกค้าให้แก่กลุ่มใหม่ เลือก **สร้าง** ในบานหน้าต่างการดำเนินการเพื่อเพิ่มแถวไปยังกริด</span><span class="sxs-lookup"><span data-stu-id="c6130-138">To add the customer to a new group, select **New** on the Action Pane to add a row to the grid.</span></span> <span data-ttu-id="c6130-139">จากนั้นให้กำหนดฟิลด์ดังต่อไปนี้สำหรับแถวใหม่:</span><span class="sxs-lookup"><span data-stu-id="c6130-139">Then set the following fields for the new row:</span></span>

    - <span data-ttu-id="c6130-140">**กลุ่มการจัดการเงินคืน** – เลือกกลุ่มที่จะเพิ่มลูกค้า</span><span class="sxs-lookup"><span data-stu-id="c6130-140">**Rebate management group** – Select the group to add the customer to.</span></span>
    - <span data-ttu-id="c6130-141">**คำอธิบาย** – ป้อนคำอธิบายของกลุ่ม (ตัวอย่างเช่น เพื่ออธิบายเหตุผลที่ลูกค้าเป็นสมาชิกของกลุ่ม)</span><span class="sxs-lookup"><span data-stu-id="c6130-141">**Description** – Enter a description of the group (for example, to explain why the customer is a member of it).</span></span>

1. <span data-ttu-id="c6130-142">เมื่อต้องการลบลูกค้าออกจากกลุ่ม ให้เลือกกลุ่ม แล้วเลือก **ลบ** ในบานหน้าต่างการดำเนินการ</span><span class="sxs-lookup"><span data-stu-id="c6130-142">To remove a customer from a group, select the group, and then select **Delete** on the Action Pane.</span></span>

## <a name="rebate-management-vendor-groups"></a><span data-ttu-id="c6130-143">กลุ่มการจัดการเงินคืนให้กับผู้จัดจำหน่าย</span><span class="sxs-lookup"><span data-stu-id="c6130-143">Rebate management vendor groups</span></span>

<span data-ttu-id="c6130-144">การคํานวณกลุ่มผู้จัดจำหน่ายมักจะถูกสร้างขึ้นมาให้กับกลุ่มจุดจัดส่ง</span><span class="sxs-lookup"><span data-stu-id="c6130-144">The calculation for a group of vendors is often created for a group of delivery points.</span></span> <span data-ttu-id="c6130-145">การคํานวณชนิดนี้มักเกี่ยวข้องกับเงินคืน</span><span class="sxs-lookup"><span data-stu-id="c6130-145">This type of calculation is usually related to a rebate.</span></span>

### <a name="set-up-vendor-groups"></a><span data-ttu-id="c6130-146">ตั้งค่ากลุ่มผู้จัดจำหน่าย</span><span class="sxs-lookup"><span data-stu-id="c6130-146">Set up vendor groups</span></span>

<span data-ttu-id="c6130-147">เมื่อต้องการใช้งานกลุ่มการจัดการเงินคืนให้กับผู้จัดจำหน่าย ให้ไปที่ **การจัดการเงินคืน \> การตั้งค่ากลุ่มการจัดการเงินคืน \> กลุ่มผู้จัดจำหน่าย**</span><span class="sxs-lookup"><span data-stu-id="c6130-147">To work with Rebate management vendor groups, go to **Rebate management \> Rebate management groups setup \> Vendor groups**.</span></span> <span data-ttu-id="c6130-148">คุณสามารถใช้ปุ่มในบานหน้าต่างการดำเนินการเพื่อเพิ่มและลบกลุ่มตามที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="c6130-148">You can use the buttons on the Action Pane to add and remove groups as required.</span></span> <span data-ttu-id="c6130-149">สำหรับแต่ละกลุ่ม ตั้งค่าฟิลด์ต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="c6130-149">For each group, set the following fields:</span></span>

- <span data-ttu-id="c6130-150">**กลุ่มการจัดการเงินคืน** – ป้อนชื่อเฉพาะสำหรับกลุ่ม</span><span class="sxs-lookup"><span data-stu-id="c6130-150">**Rebate management group** – Enter a unique name for the group.</span></span>
- <span data-ttu-id="c6130-151">**คำอธิบาย** – ป้อนอธิบายเกี่ยวกับกลุ่ม เพื่อดูข้อมูลเพิ่มเติมเกี่ยวกับวิธีการใช้</span><span class="sxs-lookup"><span data-stu-id="c6130-151">**Description** – Enter a description of the group to provide more information about how it should be used.</span></span>

### <a name="manage-vendor-group-assignments"></a><span data-ttu-id="c6130-152">จัดการการมอบหมายกลุ่มผู้จัดจำหน่าย</span><span class="sxs-lookup"><span data-stu-id="c6130-152">Manage vendor group assignments</span></span>

<span data-ttu-id="c6130-153">ผู้จัดจำหน่ายแต่ละคนสามารถอยู่ในกลุ่มการจัดการเงินคืนได้หลายกลุ่ม</span><span class="sxs-lookup"><span data-stu-id="c6130-153">Each vendor can belong to any number of Rebate management groups.</span></span> <span data-ttu-id="c6130-154">เมื่อต้องการดูและกําหนดสมาชิกกลุ่ม คุณสามารถเริ่มต้นจากรายการกลุ่มหรือรายชื่อผู้จัดจำหน่าย</span><span class="sxs-lookup"><span data-stu-id="c6130-154">To view and assign group members, you can start from either the group list or the vendor list.</span></span>

<span data-ttu-id="c6130-155">เมื่อต้องการดู เพิ่ม หรือลบผู้จัดจำหน่ายของกลุ่มที่เลือก ให้ปฏิบัติตามขั้นตอนต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="c6130-155">To view, add, or remove vendors for a selected group, follow these steps.</span></span>

1. <span data-ttu-id="c6130-156">ไปที่ **การจัดการเงินคืน \> การตั้งค่ากลุ่มการจัดการเงินคืน \> กลุ่มผู้จัดจำหน่าย**</span><span class="sxs-lookup"><span data-stu-id="c6130-156">Go to **Rebate management \> Rebate management groups setup \> Vendor groups**.</span></span>
1. <span data-ttu-id="c6130-157">เลือกกลุ่มเพื่อจัดการ</span><span class="sxs-lookup"><span data-stu-id="c6130-157">Select the group to manage.</span></span>
1. <span data-ttu-id="c6130-158">ในบานหน้าต่างการดำเนินการ เลือก **ผู้จัดจำหน่าย**</span><span class="sxs-lookup"><span data-stu-id="c6130-158">On the Action Pane, select **Vendors**.</span></span> <span data-ttu-id="c6130-159">หน้า **กลุ่มการจัดการเงินคืน** จะปรากฏขึ้นและแสดงรายชื่อผู้จัดจำหน่ายที่เป็นสมาชิกของกลุ่มที่เลือกแล้ว</span><span class="sxs-lookup"><span data-stu-id="c6130-159">The **Rebate management groups** page appears and shows a list of vendors that are already members of the selected group.</span></span>
1. <span data-ttu-id="c6130-160">หากต้องการเพิ่มผู้จัดจำหน่ายใหม่ให้แก่กลุ่ม เลือก **สร้าง** ในบานหน้าต่างการดำเนินการเพื่อเพิ่มแถวไปยังกริด</span><span class="sxs-lookup"><span data-stu-id="c6130-160">To add a new vendor to the group, select **New** on the Action Pane to add a row to the grid.</span></span> <span data-ttu-id="c6130-161">จากนั้นให้กำหนดฟิลด์ดังต่อไปนี้สำหรับแถวใหม่:</span><span class="sxs-lookup"><span data-stu-id="c6130-161">Then set the following fields for the new row:</span></span>

    - <span data-ttu-id="c6130-162">**บัญชีผู้จัดจำหน่าย** – เลือกรหัสบัญชีผู้จัดจำหน่าย</span><span class="sxs-lookup"><span data-stu-id="c6130-162">**Vendor account** – Select the vendor account ID.</span></span>
    - <span data-ttu-id="c6130-163">**ชื่อ** – ป้อนชื่อและ/หรือคำอธิบายเกี่ยวกับผู้จัดจำหน่าย</span><span class="sxs-lookup"><span data-stu-id="c6130-163">**Name** – Enter a name and/or description of the vendor.</span></span>

1. <span data-ttu-id="c6130-164">เมื่อต้องการลบผู้จัดจำหน่ายออกจากกลุ่ม ให้เลือกผู้จัดจำหน่าย แล้วเลือก **ลบ** ในบานหน้าต่างการดำเนินการ</span><span class="sxs-lookup"><span data-stu-id="c6130-164">To remove a vendor from the group, select the vendor, and then select **Delete** on the Action Pane.</span></span>

<span data-ttu-id="c6130-165">เมื่อต้องการดู เพิ่ม หรือลบการกำหนดกลุ่มของผู้จัดจำหน่ายที่เลือก ให้ปฏิบัติตามขั้นตอนต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="c6130-165">To view, add, or remove group assignments for a selected vendor, follow these steps.</span></span>

1. <span data-ttu-id="c6130-166">ไปที่ **บัญชีเจ้าหนี้ \> ผู้จัดจำหน่าย \> ผู้จัดจำหน่ายทั้งหมด**</span><span class="sxs-lookup"><span data-stu-id="c6130-166">Go to **Accounts payable \> Vendors \> All vendors**.</span></span>
1. <span data-ttu-id="c6130-167">เลือกผู้จัดจำหน่ายที่จะทำงานด้วย</span><span class="sxs-lookup"><span data-stu-id="c6130-167">Select the vendor to work with.</span></span>
1. <span data-ttu-id="c6130-168">บนบานหน้าต่างการดำเนินการ บนแท็บ **ผู้จัดจำหน่าย** ในกลุ่ม **การจัดการเงินคืน** ให้เลือก **กลุ่มการจัดการเงินคืน**</span><span class="sxs-lookup"><span data-stu-id="c6130-168">On the Action Pane, on the **Vendor** tab, in the **Rebate management** group, select **Rebate management groups**.</span></span> <span data-ttu-id="c6130-169">หน้า **กลุ่มการจัดการเงินคืน** จะปรากฏขึ้นและแสดงรายชื่อกลุ่มที่เป็นผู้จัดจำหน่ายที่เลือกที่เป็นสมาชิกแล้ว</span><span class="sxs-lookup"><span data-stu-id="c6130-169">The **Rebate management groups** page appears and shows a list of groups that the selected vendor already belongs to.</span></span>
1. <span data-ttu-id="c6130-170">หากต้องการเพิ่มผู้จัดจำหน่ายให้แก่กลุ่มใหม่ เลือก **สร้าง** ในบานหน้าต่างการดำเนินการเพื่อเพิ่มแถวไปยังกริด</span><span class="sxs-lookup"><span data-stu-id="c6130-170">To add the vendor to a new group, select **New** on the Action Pane to add a row to the grid.</span></span> <span data-ttu-id="c6130-171">จากนั้นให้กำหนดฟิลด์ดังต่อไปนี้สำหรับแถวใหม่:</span><span class="sxs-lookup"><span data-stu-id="c6130-171">Then set the following fields for the new row:</span></span>

    - <span data-ttu-id="c6130-172">**กลุ่มการจัดการเงินคืน** – เลือกกลุ่มที่จะเพิ่มผู้จัดจำหน่าย</span><span class="sxs-lookup"><span data-stu-id="c6130-172">**Rebate management group** – Select the group to add the vendor to.</span></span>
    - <span data-ttu-id="c6130-173">**คำอธิบาย** – ป้อนคำอธิบายของกลุ่ม (ตัวอย่างเช่น เพื่ออธิบายเหตุผลที่ผู้จัดจำหน่ายเป็นสมาชิกของกลุ่ม)</span><span class="sxs-lookup"><span data-stu-id="c6130-173">**Description** – Enter a description of the group (for example, to explain why the vendor is a member of it).</span></span>

1. <span data-ttu-id="c6130-174">เมื่อต้องการลบผู้จัดจำหน่ายออกจากกลุ่ม ให้เลือกกลุ่ม แล้วเลือก **ลบ** ในบานหน้าต่างการดำเนินการ</span><span class="sxs-lookup"><span data-stu-id="c6130-174">To remove a vendor from a group, select the group, and then select **Delete** on the Action Pane.</span></span>

## <a name="item-rebate-groups"></a><span data-ttu-id="c6130-175">กลุ่มเงินคืนของสินค้า</span><span class="sxs-lookup"><span data-stu-id="c6130-175">Item rebate groups</span></span>

<span data-ttu-id="c6130-176">การจัดกลุ่มสินค้าช่วยให้คุณมีความยืดหยุ่นมากขึ้นเมื่อคํานวณเงินคืนและการหักลด</span><span class="sxs-lookup"><span data-stu-id="c6130-176">By grouping items, you have more flexibility when rebates and deductions are calculated.</span></span> <span data-ttu-id="c6130-177">วิธีการนี้มักจะเป็นวิธีที่มีประสิทธิภาพมากกว่าในการตั้งค่าเงินคืนและการหักลดของลูกค้าและผู้จัดจำหน่าย</span><span class="sxs-lookup"><span data-stu-id="c6130-177">This approach is often a more efficient way to set up rebates and deductions for customers and vendors.</span></span>

### <a name="set-up-item-groups"></a><span data-ttu-id="c6130-178">ตั้งค่ากลุ่มสินค้า</span><span class="sxs-lookup"><span data-stu-id="c6130-178">Set up item groups</span></span>

<span data-ttu-id="c6130-179">เมื่อต้องการใช้งานกลุ่มการจัดการเงินคืนให้กับกลุ่มสินค้า ให้ไปที่ **การจัดการเงินคืน \> การตั้งค่ากลุ่มการจัดการเงินคืน \> กลุ่มสินค้า**</span><span class="sxs-lookup"><span data-stu-id="c6130-179">To work with Rebate management item groups, go to **Rebate management \> Rebate management groups setup \> Item groups**.</span></span> <span data-ttu-id="c6130-180">คุณสามารถใช้ปุ่มในบานหน้าต่างการดำเนินการเพื่อเพิ่มและลบกลุ่มตามที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="c6130-180">You can use the buttons on the Action Pane to add and remove groups as required.</span></span> <span data-ttu-id="c6130-181">สำหรับแต่ละกลุ่ม ตั้งค่าฟิลด์ต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="c6130-181">For each group, set the following fields:</span></span>

- <span data-ttu-id="c6130-182">**กลุ่มการจัดการเงินคืน** – ป้อนชื่อเฉพาะสำหรับกลุ่ม</span><span class="sxs-lookup"><span data-stu-id="c6130-182">**Rebate management group** – Enter a unique name for the group.</span></span>
- <span data-ttu-id="c6130-183">**คำอธิบาย** – ป้อนอธิบายเกี่ยวกับกลุ่ม เพื่อดูข้อมูลเพิ่มเติมเกี่ยวกับวิธีการใช้</span><span class="sxs-lookup"><span data-stu-id="c6130-183">**Description** – Enter a description of the group to provide more information about how it should be used.</span></span>

### <a name="manage-item-group-assignments"></a><span data-ttu-id="c6130-184">จัดการการมอบหมายกลุ่มสินค้า</span><span class="sxs-lookup"><span data-stu-id="c6130-184">Manage item group assignments</span></span>

<span data-ttu-id="c6130-185">สินค้าแต่ละชิ้นสามารถอยู่ในกลุ่มการจัดการเงินคืนได้หลายกลุ่ม</span><span class="sxs-lookup"><span data-stu-id="c6130-185">Each item can belong to any number of Rebate management groups.</span></span> <span data-ttu-id="c6130-186">เมื่อต้องการดูและกําหนดสมาชิกกลุ่ม คุณสามารถเริ่มต้นจากรายการกลุ่มหรือรายการสินค้า</span><span class="sxs-lookup"><span data-stu-id="c6130-186">To view and assign group members, you can start from either the group list or the item list.</span></span> <span data-ttu-id="c6130-187">คุณยังสามารถเพิ่มสินค้าตามการจัดประเภทตามลำดับชั้นได้</span><span class="sxs-lookup"><span data-stu-id="c6130-187">You can also add items based on your category hierarchy.</span></span>

<span data-ttu-id="c6130-188">เมื่อต้องการดู เพิ่ม หรือลบสินค้าของกลุ่มที่เลือก ให้ปฏิบัติตามขั้นตอนต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="c6130-188">To view, add, or remove items for a selected group, follow these steps.</span></span>

1. <span data-ttu-id="c6130-189">ไปที่ **การจัดการเงินคืน \> การตั้งค่ากลุ่มการจัดการเงินคืน \> กลุ่มสินค้า**</span><span class="sxs-lookup"><span data-stu-id="c6130-189">Go to **Rebate management \> Rebate management groups setup \> Item groups**.</span></span>
1. <span data-ttu-id="c6130-190">เลือกกลุ่มเพื่อจัดการ</span><span class="sxs-lookup"><span data-stu-id="c6130-190">Select the group to manage.</span></span>
1. <span data-ttu-id="c6130-191">บนบานหน้าต่างการดำเนินการ เลือก **สินค้า**</span><span class="sxs-lookup"><span data-stu-id="c6130-191">On the Action Pane, select **Items**.</span></span> <span data-ttu-id="c6130-192">หน้า **กลุ่มการจัดการเงินคืน** จะปรากฏขึ้นและแสดงรายชื่อสินค้าที่เป็นสมาชิกของกลุ่มที่เลือกแล้ว</span><span class="sxs-lookup"><span data-stu-id="c6130-192">The **Rebate management groups** page appears and shows a list of items that are already members of the selected group.</span></span>
1. <span data-ttu-id="c6130-193">หากต้องการเพิ่มสินค้าใหม่ให้แก่กลุ่ม เลือก **สร้าง** ในบานหน้าต่างการดำเนินการเพื่อเพิ่มแถวไปยังกริด</span><span class="sxs-lookup"><span data-stu-id="c6130-193">To add a new item to the group, select **New** on the Action Pane to add a row to the grid.</span></span> <span data-ttu-id="c6130-194">จากนั้นให้กำหนดฟิลด์ดังต่อไปนี้สำหรับแถวใหม่:</span><span class="sxs-lookup"><span data-stu-id="c6130-194">Then set the following fields for the new row:</span></span>

    - <span data-ttu-id="c6130-195">**บัญชีสินค้า** – เลือกรหัสบัญชีสินค้า</span><span class="sxs-lookup"><span data-stu-id="c6130-195">**Item account** – Select the item account ID.</span></span>
    - <span data-ttu-id="c6130-196">**ชื่อผลิตภัณฑ์** – ป้อนชื่อและ/หรือคำอธิบายเกี่ยวกับสินค้า</span><span class="sxs-lookup"><span data-stu-id="c6130-196">**Product name** – Enter a name and/or description of the item.</span></span>

1. <span data-ttu-id="c6130-197">เมื่อต้องการลบสินค้าออกจากกลุ่ม ให้เลือกสินค้า แล้วเลือก **ลบ** ในบานหน้าต่างการดำเนินการ</span><span class="sxs-lookup"><span data-stu-id="c6130-197">To remove an item from the group, select the item, and then select **Delete** on the Action Pane.</span></span>

<span data-ttu-id="c6130-198">เมื่อต้องการดู เพิ่ม หรือลบการกำหนดกลุ่มของสินค้าที่เลือก ให้ปฏิบัติตามขั้นตอนต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="c6130-198">To view, add, or remove group assignments for a selected item, follow these steps.</span></span>

1. <span data-ttu-id="c6130-199">ไปยัง **การจัดการข้อมูลผลิตภัณฑ์ \> ผลิตภัณฑ์ \> ผลิตภัณฑ์ที่นำออกใช้**</span><span class="sxs-lookup"><span data-stu-id="c6130-199">Go to **Product information management \> Products \> Released products**.</span></span>
1. <span data-ttu-id="c6130-200">เลือกสินค้าที่จะทำงานด้วย</span><span class="sxs-lookup"><span data-stu-id="c6130-200">Select the item to work with.</span></span>
1. <span data-ttu-id="c6130-201">บนบานหน้าต่างการดำเนินการ บนแท็บ **ผลิตภัณฑ์** ในกลุ่ม **การจัดการเงินคืน** ให้เลือก **กลุ่มการจัดการเงินคืน**</span><span class="sxs-lookup"><span data-stu-id="c6130-201">On the Action Pane, on the **Product** tab, in the **Rebate management** group, select **Rebate management groups**.</span></span> <span data-ttu-id="c6130-202">หน้า **กลุ่มการจัดการเงินคืน** จะปรากฏขึ้นและแสดงรายชื่อกลุ่มที่เป็นสินค้าที่เลือกที่เป็นสมาชิกแล้ว</span><span class="sxs-lookup"><span data-stu-id="c6130-202">The **Rebate management groups** page appears and shows a list of groups that the selected item already belongs to.</span></span>
1. <span data-ttu-id="c6130-203">หากต้องการเพิ่มสินค้าให้แก่กลุ่มใหม่ เลือก **สร้าง** ในบานหน้าต่างการดำเนินการเพื่อเพิ่มแถวไปยังกริด</span><span class="sxs-lookup"><span data-stu-id="c6130-203">To add the item to a new group, select **New** on the Action Pane to add a row to the grid.</span></span> <span data-ttu-id="c6130-204">จากนั้นให้กำหนดฟิลด์ดังต่อไปนี้สำหรับแถวใหม่:</span><span class="sxs-lookup"><span data-stu-id="c6130-204">Then set the following fields for the new row:</span></span>

    - <span data-ttu-id="c6130-205">**กลุ่มการจัดการเงินคืน** – เลือกกลุ่มที่จะเพิ่มสินค้า</span><span class="sxs-lookup"><span data-stu-id="c6130-205">**Rebate management group** – Select the group to add the item to.</span></span>
    - <span data-ttu-id="c6130-206">**คำอธิบาย** – ป้อนคำอธิบายของกลุ่ม (ตัวอย่างเช่น เพื่ออธิบายเหตุผลที่สินค้าเป็นสมาชิกของกลุ่ม)</span><span class="sxs-lookup"><span data-stu-id="c6130-206">**Description** – Enter a description of the group (for example, to explain why the item is a member of it).</span></span>

1. <span data-ttu-id="c6130-207">เมื่อต้องการลบสินค้าออกจากกลุ่ม ให้เลือกกลุ่ม แล้วเลือก **ลบ** ในบานหน้าต่างการดำเนินการ</span><span class="sxs-lookup"><span data-stu-id="c6130-207">To remove an item from a group, select the group, and then select **Delete** on the Action Pane.</span></span>

<span data-ttu-id="c6130-208">ในการเพิ่มสินค้าลงในกลุ่มตามการจัดประเภทตามลำดับชั้นของคุณ ให้ปฏิบัติตามขั้นตอนต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="c6130-208">To add items to a group based on your category hierarchy, follow these steps.</span></span>

1. <span data-ttu-id="c6130-209">ไปที่ **การจัดการเงินคืน \> การตั้งค่ากลุ่มการจัดการเงินคืน \> กลุ่มสินค้า**</span><span class="sxs-lookup"><span data-stu-id="c6130-209">Go to **Rebate management \> Rebate management groups setup \> Item groups**.</span></span>
1. <span data-ttu-id="c6130-210">เลือกกลุ่มเพื่อจัดการ</span><span class="sxs-lookup"><span data-stu-id="c6130-210">Select the group to manage.</span></span>
1. <span data-ttu-id="c6130-211">บนบานหน้าต่างการดำเนินการ เลือก **เพิ่มสินค้า**</span><span class="sxs-lookup"><span data-stu-id="c6130-211">On the Action Pane, select **Add items**.</span></span>
1. <span data-ttu-id="c6130-212">ในกล่องโต้ตอบ **เพิ่มสินค้า** ในฟิลด์ **การจัดประเภทตามลำดับชั้น** ให้เลือกประเภทระดับบนสุด</span><span class="sxs-lookup"><span data-stu-id="c6130-212">In the **Add items** dialog box, in the **Category hierarchy** field, select a top-level category.</span></span>
1. <span data-ttu-id="c6130-213">ลำดับชั้นสินค้าจะปรากฏในบานหน้าต่างด้านซ้าย</span><span class="sxs-lookup"><span data-stu-id="c6130-213">The item hierarchy is opened in the left pane.</span></span> <span data-ttu-id="c6130-214">เลือกระดับลำดับชั้นที่คุณค้นหา</span><span class="sxs-lookup"><span data-stu-id="c6130-214">Select the hierarchy level that you're looking for.</span></span> 
1. <span data-ttu-id="c6130-215">ขณะนี้รายการจากลำดับชั้นและระดับลำดับชั้นที่เลือกจะแสดงรายการอยู่ในบานหน้าต่างด้านขวา</span><span class="sxs-lookup"><span data-stu-id="c6130-215">Items from the selected hierarchy and hierarchy level are now listed in the right pane.</span></span> <span data-ttu-id="c6130-216">ปฏิบัติตามขั้นตอนต่อไปนี้เพื่อใช้งานบานหน้าต่าง:</span><span class="sxs-lookup"><span data-stu-id="c6130-216">Follow these steps to work with the pane:</span></span>

    - <span data-ttu-id="c6130-217">เลือกกล่องกาเครื่องหมายของแต่ละสินค้าที่คุณต้องการใส่ไว้ในลำดับขั้นดังกล่าว</span><span class="sxs-lookup"><span data-stu-id="c6130-217">Select the check box for each item that you want to add.</span></span>
    - <span data-ttu-id="c6130-218">เลือกกล่องกาเครื่องหมายบนส่วนหน้าของกริด เพื่อเลือกรายการทั้งหมดที่จะแสดงรายการ</span><span class="sxs-lookup"><span data-stu-id="c6130-218">Select the check box on the grid header to select all the items that are listed.</span></span>
    - <span data-ttu-id="c6130-219">เลือกปุ่ม **แสดงที่เลือก** เพื่อกรองข้อมูลกริด เพื่อให้แสดงเฉพาะรายการที่คุณเลือกจนถึงขณะนี้</span><span class="sxs-lookup"><span data-stu-id="c6130-219">Select the **Show selected** button to filter the grid so that it shows only the items that you've selected so far.</span></span> <span data-ttu-id="c6130-220">เลือกปุ่มอีกครั้งเพื่อกลับไปที่รายการทั้งหมด</span><span class="sxs-lookup"><span data-stu-id="c6130-220">Select the button again to return to the full list.</span></span>

1. <span data-ttu-id="c6130-221">เลือก **ตกลง** เพื่อใช้การเลือกสินค้าของคุณกับกลุ่มที่เลือก</span><span class="sxs-lookup"><span data-stu-id="c6130-221">Select **OK** to apply your item selection to the selected group.</span></span>
