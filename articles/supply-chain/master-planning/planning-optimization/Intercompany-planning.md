---
title: การวางแผนระหว่างบริษัท
description: หัวข้อนี้จะอธิบายการวางแผนระหว่างบริษัทและอธิบายวิธีการตั้งค่าคอนฟิกการวางแผนระหว่างบริษัทโดยมีการเพิ่มประสิทธิภาพการวางแผนใน Microsoft Dynamics 365 Supply Chain Management
author: ChristianRytt
ms.date: 12/02/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ReqCreatePlanWorkspace
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2020-12-02
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 5c9ab724034a9bb40cfe155b748a0c7e25978add
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 04/01/2021
ms.locfileid: "5833364"
---
# <a name="intercompany-planning"></a><span data-ttu-id="edf7e-103">การวางแผนระหว่างบริษัท</span><span class="sxs-lookup"><span data-stu-id="edf7e-103">Intercompany planning</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="edf7e-104">สำหรับบางองค์กร การดำเนินงานลอจิสติกส์จะขึ้นอยู่กับนิติบุคคลอื่นๆ (บริษัท) ในองค์กร</span><span class="sxs-lookup"><span data-stu-id="edf7e-104">For some organizations, logistics operations depend on other legal entities (companies) in the organization.</span></span> <span data-ttu-id="edf7e-105">การดำเนินงานเหล่านี้จะได้รับการจัดการโดยใช้การขายและการซื้อระหว่างบริษัท เนื่องจากนิติบุคคลแต่ละแห่งจะมีผังบัญชีที่แยกต่างหาก</span><span class="sxs-lookup"><span data-stu-id="edf7e-105">These operations are handled by using intercompany sales and purchases, because each legal entity has a separate chart of accounts.</span></span>

<span data-ttu-id="edf7e-106">หัวข้อนี้จะอธิบายการวางแผนระหว่างบริษัทและอธิบายวิธีการตั้งค่าคอนฟิกการวางแผนระหว่างบริษัทโดยมีการเพิ่มประสิทธิภาพการวางแผนใน Microsoft Dynamics 365 Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="edf7e-106">This topic describes intercompany planning and explains how to configure intercompany planning with Planning Optimization in Microsoft Dynamics 365 Supply Chain Management.</span></span>

<span data-ttu-id="edf7e-107">หัวข้อนี้ใช้เงื่อนไขระหว่างบริษัทที่สำคัญต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="edf7e-107">This topic uses the following important intercompany terms:</span></span>

- <span data-ttu-id="edf7e-108">**ต้นน้ำ** – การอ้างอิงแบบสัมพัทธ์ในบริษัทหรือห่วงโซ่อุปทาน</span><span class="sxs-lookup"><span data-stu-id="edf7e-108">**Upstream** – A relative reference in a firm or supply chain.</span></span> <span data-ttu-id="edf7e-109">ซึ่งบ่งชี้การเคลื่อนย้ายในทิศทางของผู้จัดจำหน่ายวัตถุดิบ</span><span class="sxs-lookup"><span data-stu-id="edf7e-109">It indicates movement in the direction of the raw material supplier.</span></span>
- <span data-ttu-id="edf7e-110">**ปลายน้ำ** – การอ้างอิงแบบสัมพัทธ์ในบริษัทหรือห่วงโซ่อุปทาน</span><span class="sxs-lookup"><span data-stu-id="edf7e-110">**Downstream** – A relative reference in a firm or supply chain.</span></span> <span data-ttu-id="edf7e-111">ซึ่งบ่งชี้การเคลื่อนย้ายในทิศทางของลูกค้า</span><span class="sxs-lookup"><span data-stu-id="edf7e-111">It indicates movement in the direction of the customer.</span></span>
- <span data-ttu-id="edf7e-112">**ความต้องการระหว่างบริษัทที่วางแผนไว้** –ความต้องการที่วางแผนไว้สำหรับผลิตภัณฑ์ในบริษัท โดยขึ้นอยู่กับความต้องการที่วางแผนไว้สำหรับผลิตภัณฑ์จากบริษัทปลายน้ำ</span><span class="sxs-lookup"><span data-stu-id="edf7e-112">**Planned intercompany demand** – Planned demand for a product in a company, based on planned demand for the product from a downstream company.</span></span>

<span data-ttu-id="edf7e-113">ในการวางแผนหลัก แผนในหนึ่งบริษัทสามารถรวมความต้องการระหว่างบริษัทที่วางแผนไว้ซึ่งเกี่ยวข้องกับแผนการใบสั่งจากแผนในบริษัทอื่น</span><span class="sxs-lookup"><span data-stu-id="edf7e-113">In master planning, a plan in one company can include planned intercompany demand that is related to planned orders from a plan in another company.</span></span> <span data-ttu-id="edf7e-114">ความสามารถนี้มีประโยชน์ เนื่องจากมีความสามารถในการมองเห็นแผนการใบสั่งทั้งหมดในบริษัทต่างๆ</span><span class="sxs-lookup"><span data-stu-id="edf7e-114">This capability is useful, because it provides full visibility into planned orders across companies.</span></span> <span data-ttu-id="edf7e-115">นอกจากนี้ ยังช่วยให้มั่นใจว่าจะมีการสร้างแผนการใบสั่งการจัดหาวัสดุที่จำเป็นทั้งหมด แต่ไม่จำเป็นต้องมีการยืนยันแผนการใบสั่งสำหรับความต้องการระหว่างบริษัท</span><span class="sxs-lookup"><span data-stu-id="edf7e-115">It also ensures that all required planned supply orders are created, but without requiring that planned orders be firmed for the intercompany demand.</span></span>

<span data-ttu-id="edf7e-116">ถ้าคุณรันการวางแผนหลักจากแผนหลักที่รวมความต้องการปลายน้ำที่วางแผนไว้ แผนการใบสั่งซื้อจากผู้จัดจำหน่ายระหว่างบริษัทที่เกี่ยวข้องจะถูกรวมอยู่ในแผนตามความต้องการ</span><span class="sxs-lookup"><span data-stu-id="edf7e-116">If you run master planning from a master plan that includes planned downstream demand, planned purchase orders from the related intercompany vendors will be included in the plan as demand.</span></span>

## <a name="required-setup"></a><span data-ttu-id="edf7e-117">การตั้งค่าที่จำเป็น</span><span class="sxs-lookup"><span data-stu-id="edf7e-117">Required setup</span></span>

<span data-ttu-id="edf7e-118">เมื่อต้องการใช้การวางแผนระหว่างบริษัท คุณต้องเตรียมระบบของคุณในลักษณะต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="edf7e-118">To use intercompany planning, you must prepare your system in the following way:</span></span>

1. <span data-ttu-id="edf7e-119">ผลิตภัณฑ์ที่เกี่ยวข้องต้องถูกนำออกใช้ในบริษัทที่เกี่ยวข้องทั้งหมด</span><span class="sxs-lookup"><span data-stu-id="edf7e-119">The relevant products must be released in all the relevant companies.</span></span> <span data-ttu-id="edf7e-120">สำหรับข้อมูลเพิ่มเติม โปรดดู [ตั้งค่าคอนฟิกและใช้การค้าระหว่างบริษัทใน Dynamics 365 Supply Chain Management ](https://docs.microsoft.com/learn/modules/configure-use-intercompany-trade-dyn365-supply-chain-mgmt/) บน Microsoft Learn</span><span class="sxs-lookup"><span data-stu-id="edf7e-120">For more information, see [Configure and use intercompany trade in Dynamics 365 Supply Chain Management ](https://docs.microsoft.com/learn/modules/configure-use-intercompany-trade-dyn365-supply-chain-mgmt/) on Microsoft Learn.</span></span>
1. <span data-ttu-id="edf7e-121">ต้องครอบคลุมความต้องการปลายน้ำโดยการซื้อจากผู้จัดจำหน่ายที่มีความสัมพันธ์ระหว่างบริษัทกับบริษัทต้นน้ำและมิติสินค้าคงคลังเริ่มต้นที่เกี่ยวข้อง (ไซต์และคลังสินค้า) ของลูกค้า</span><span class="sxs-lookup"><span data-stu-id="edf7e-121">Downstream demand must be covered by purchases from a vendor that has an intercompany relation to the upstream company and relevant default inventory dimensions (site and warehouse) on the customer.</span></span> <span data-ttu-id="edf7e-122">สำหรับข้อมูลเพิ่มเติม โปรดดู [ตั้งค่าคอนฟิกและใช้การค้าระหว่างบริษัทใน Dynamics 365 Supply Chain Management ](https://docs.microsoft.com/learn/modules/configure-use-intercompany-trade-dyn365-supply-chain-mgmt/) บน Microsoft Learn</span><span class="sxs-lookup"><span data-stu-id="edf7e-122">For more information, see [Configure and use intercompany trade in Dynamics 365 Supply Chain Management ](https://docs.microsoft.com/learn/modules/configure-use-intercompany-trade-dyn365-supply-chain-mgmt/) on Microsoft Learn.</span></span>
1. <span data-ttu-id="edf7e-123">แผนหลักในบริษัทต้นน้ำต้องรวมความต้องการที่วางแผนไว้ล่วงหน้า และต้องระบุบริษัทและแผนหลักที่เกี่ยวข้องในแผนปลายน้ำ</span><span class="sxs-lookup"><span data-stu-id="edf7e-123">The master plan in the upstream company must include planned downstream demand, and the relevant company and master plan must be specified in the downstream plans.</span></span>

## <a name="include-planned-downstream-demand"></a><span data-ttu-id="edf7e-124">รวมความต้องการขั้นปลายน้ำที่วางแผนไว้</span><span class="sxs-lookup"><span data-stu-id="edf7e-124">Include planned downstream demand</span></span>

<span data-ttu-id="edf7e-125">ทำตามขั้นตอนต่อไปนี้เพื่อตั้งค่าคอนฟิกแผนหลักของคุณ เพื่อให้รวมความต้องการปลายน้ำที่วางแผนไว้</span><span class="sxs-lookup"><span data-stu-id="edf7e-125">Follow these steps to configure your master plan so that it includes planned downstream demand.</span></span>

1. <span data-ttu-id="edf7e-126">ไปที่ **การวางแผนหลัก \> การตั้งค่า \> แผน \> แผนหลัก**</span><span class="sxs-lookup"><span data-stu-id="edf7e-126">Go to **Master planning \> Setup \> Plans \> Master plans**.</span></span>
1. <span data-ttu-id="edf7e-127">เลือกหรือสร้างแผนหลัก</span><span class="sxs-lookup"><span data-stu-id="edf7e-127">Select or create a master plan.</span></span>
1. <span data-ttu-id="edf7e-128">บน FastTab **การวางแผนระหว่างบริษัท** ตั้งค่าฟิลด์ต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="edf7e-128">On the **Intercompany planning** FastTab, set the following fields:</span></span>

    - <span data-ttu-id="edf7e-129">**รวมความต้องการปลายน้ำที่วางแผนไว้** – กำหนดตัวเลือกนี้เป็น *ใช่* เพื่อเปิดใช้งานการวางแผนระหว่างบริษัทสำหรับแผนหลัก</span><span class="sxs-lookup"><span data-stu-id="edf7e-129">**Include planned downstream demand** – Set this option to *Yes* to enable intercompany planning for the master plan.</span></span>
    - <span data-ttu-id="edf7e-130">**แผนปลายน้ำ** – ถ้าคุณตั้งค่าตัวเลือก **รวมความต้องการปลายน้ำที่วางแผนไว้** เป็น *ใช่* ให้ใช้แถบเครื่องมือและกริดเพื่อเพิ่มแผนหลักที่ต้องการจากบริษัทอื่น</span><span class="sxs-lookup"><span data-stu-id="edf7e-130">**Downstream plans** – If you set the **Include planned downstream demand** option to *Yes*, use the toolbar and grid to add the desired master plans from other companies.</span></span>

## <a name="peg-across-companies-by-using-multilevel-pegging"></a><span data-ttu-id="edf7e-131">เชื่อมโยงระหว่างบริษัทโดยใช้การเชื่อมโยงความต้องการกับการจัดซื้อแบบหลายระดับ</span><span class="sxs-lookup"><span data-stu-id="edf7e-131">Peg across companies by using multilevel pegging</span></span>

<span data-ttu-id="edf7e-132">ในการเชื่อมโยงความต้องการกับการจัดซื้อแบบหลายระดับ คุณสามารถดูการเชื่อมโยงความต้องการกับการจัดซื้อในบริษัทต่างๆ เพื่อดูแหล่งที่มาของความต้องการเริ่มต้นที่ครอบคลุมโดยการจัดหาวัสดุ</span><span class="sxs-lookup"><span data-stu-id="edf7e-132">In multilevel pegging, you can view pegging across companies to see the initial source of demand that is being covered by a supply.</span></span>

<span data-ttu-id="edf7e-133">เมื่อต้องการดูข้อมูลการเชื่อมโยงความต้องการกับการจัดซื้อแบบหลายระดับ ให้ทำตามขั้นตอนต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="edf7e-133">To view multilevel pegging information, follow these steps.</span></span>

1. <span data-ttu-id="edf7e-134">ไปที่ **การวางแผนหลัก \> การวางแผนหลัก \> แผนการใบสั่ง**</span><span class="sxs-lookup"><span data-stu-id="edf7e-134">Go to **Master planning \> Master planning \> Planned orders**.</span></span>
1. <span data-ttu-id="edf7e-135">เลือกหรือเปิดแผนการใบสั่ง</span><span class="sxs-lookup"><span data-stu-id="edf7e-135">Select or open a planned order.</span></span>
1. <span data-ttu-id="edf7e-136">บนบานหน้าต่างการดำเนินการ บนแท็บ **มุมมอง** ในกลุ่ม **ความต้องการ** ให้เลือก **การเชื่อมโยงความต้องการกับการจัดซื้อแบบหลายระดับ**</span><span class="sxs-lookup"><span data-stu-id="edf7e-136">On the Action Pane, on the **View** tab, in the **Requirements** group, select **Multilevel pegging**.</span></span>

### <a name="intercompany-example-that-involves-two-companies"></a><span data-ttu-id="edf7e-137">ตัวอย่างระหว่างบริษัทที่เกี่ยวข้องกับบริษัทสองแห่ง</span><span class="sxs-lookup"><span data-stu-id="edf7e-137">Intercompany example that involves two companies</span></span>

<span data-ttu-id="edf7e-138">สำหรับตัวอย่างนี้ แผนการใบสั่งผลิตจะถูกสร้างขึ้นในบริษัท USMF เพื่อครอบคลุมใบสั่งขายในบริษัท DEMF</span><span class="sxs-lookup"><span data-stu-id="edf7e-138">For this example, a planned production order is created in the USMF company to cover a sales order in the DEMF company.</span></span> <span data-ttu-id="edf7e-139">ใน USMF ความต้องการโดยตรงคือความต้องการระหว่างบริษัทที่วางแผนไว้</span><span class="sxs-lookup"><span data-stu-id="edf7e-139">In USMF, the direct demand is planned intercompany demand.</span></span> <span data-ttu-id="edf7e-140">เมื่อต้องการทำให้ความต้องการนี้ปรากฏขึ้นใน USMF การวางแผนหลักจะรันเป็นอันดับแรกใน DEMF แล้วจากนั้นใน USMF</span><span class="sxs-lookup"><span data-stu-id="edf7e-140">To make this demand appear in USMF, master planning is run first in DEMF and then in USMF.</span></span>

<span data-ttu-id="edf7e-141">ภาพประกอบต่อไปนี้แสดงลักษณะที่ปรากฏของตัวอย่างนี้บนหน้า **การเชื่อมโยงความต้องการกับการจัดซื้อแบบหลายระดับ** สำหรับแผนการใบสั่งผลิต</span><span class="sxs-lookup"><span data-stu-id="edf7e-141">The following illustration shows how this example might appear on the **Multilevel pegging** page for the planned production order.</span></span>

![ตัวอย่างระหว่างบริษัทที่เกี่ยวข้องกับบริษัทสองแห่ง](media/IntercompanyPlanning1.png)

### <a name="intercompany-example-that-involves-three-companies"></a><span data-ttu-id="edf7e-143">ตัวอย่างระหว่างบริษัทที่เกี่ยวข้องกับบริษัทสามแห่ง</span><span class="sxs-lookup"><span data-stu-id="edf7e-143">Intercompany example that involves three companies</span></span>

<span data-ttu-id="edf7e-144">สำหรับตัวอย่างนี้ แผนการใบสั่งซื้อจะถูกสร้างขึ้นในบริษัท USMF เพื่อครอบคลุมใบสั่งขายในบริษัท FRRT</span><span class="sxs-lookup"><span data-stu-id="edf7e-144">For this example, a planned purchase order is created in the USMF company to cover a sales order in the FRRT company.</span></span> <span data-ttu-id="edf7e-145">ในบริษัท DEMF และ USMF ความต้องการโดยตรงคือความต้องการระหว่างบริษัทที่วางแผนไว้</span><span class="sxs-lookup"><span data-stu-id="edf7e-145">In the DEMF and USMF companies, the direct demand is planned intercompany demand.</span></span> <span data-ttu-id="edf7e-146">เมื่อต้องการทำให้ความต้องการนี้ปรากฏขึ้นใน USMF การวางแผนหลักจะรันเป็นอันดับแรกใน FRRT แล้วจากนั้นใน DEMF และสุดท้ายใน USMF</span><span class="sxs-lookup"><span data-stu-id="edf7e-146">To make this demand appear in USMF, master planning is run first in FRRT, then in DEMF, and finally in USMF.</span></span>

<span data-ttu-id="edf7e-147">ภาพประกอบต่อไปนี้แสดงลักษณะที่ปรากฏของตัวอย่างนี้บนหน้า **การเชื่อมโยงความต้องการกับการจัดซื้อแบบหลายระดับ** สำหรับแผนการใบสั่งผลิต</span><span class="sxs-lookup"><span data-stu-id="edf7e-147">The following illustration shows how this example might appear on the **Multilevel pegging** page for the planned production order.</span></span>

![ตัวอย่างระหว่างบริษัทที่เกี่ยวข้องกับบริษัทสามแห่ง](media/IntercompanyPlanning2.png)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]