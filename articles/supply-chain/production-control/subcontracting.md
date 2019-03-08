---
title: การรับเหมารายย่อย
description: หัวข้อนี้จะช่วยให้คุณสามารถสร้างการฝึกปฏิบัติของการทำสัญญาย่อยในการผลิตใน Microsoft Dynamics 365 for Finance and Operations
author: christophernread
manager: AnnBe
ms.date: 09/28/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: ''
ms.search.region: Global
ms.author: josaw
ms.search.validFrom: 2018-09-30
ms.dyn365.ops.version: ''
ms.openlocfilehash: 55b516f928eadea9b7ddbb1192db79f3ab7fa204
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 01/29/2019
ms.locfileid: "336715"
---
# <a name="subcontracting"></a><span data-ttu-id="01da9-103">การรับเหมารายย่อย</span><span class="sxs-lookup"><span data-stu-id="01da9-103">Subcontracting</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="01da9-104">หัวข้อนี้จะช่วยให้คุณสามารถสร้างการฝึกปฏิบัติของการทำสัญญาย่อยในการผลิตใน Microsoft Dynamics 365 for Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="01da9-104">This topic will help you build a walkthrough of subcontracting in manufacturing in Microsoft Dynamics 365 for Finance and Operations.</span></span> <span data-ttu-id="01da9-105">ส่วนแรกของหัวข้อนี้อธิบายถึงการตั้งค่าของข้อมูล</span><span class="sxs-lookup"><span data-stu-id="01da9-105">The first part of this topic describes the setup of the data.</span></span> <span data-ttu-id="01da9-106">ส่วนที่สองจะนำคุณผ่านขั้นตอนต่างๆ ในการฝึกปฏิบัตินี้</span><span class="sxs-lookup"><span data-stu-id="01da9-106">The second part takes you through the steps in the walkthrough.</span></span>

## <a name="target-audience"></a><span data-ttu-id="01da9-107">ผู้ชมเป้าหมาย</span><span class="sxs-lookup"><span data-stu-id="01da9-107">Target audience</span></span>

<span data-ttu-id="01da9-108">ในหัวข้อนี้ คุณจะได้เรียนรู้วิธีการตั้งค่าการรับเหมารายย่อยในการผลิต</span><span class="sxs-lookup"><span data-stu-id="01da9-108">In this topic, you will learn how to set up subcontracting in manufacturing.</span></span> <span data-ttu-id="01da9-109">คุณจะใช้ข้อมูลที่มีอยู่ในนิติบุคคล HQUS เพื่อทำการตั้งค่าพื้นฐานของโฟลว์กิจกรรมการรับเหมารายย่อย</span><span class="sxs-lookup"><span data-stu-id="01da9-109">You will use existing data in the HQUS legal entity to do the basic setup of a subcontracting activity flow.</span></span> <span data-ttu-id="01da9-110">ข้อมูลสาธิตในนิติบุคคล HQUS จะรวมถึงพารามิเตอร์การตั้งค่าที่ได้ถูกกำหนดไว้ล่วงหน้า เพื่อสนับสนุนขั้นตอนต่างๆ ในการฝึกปฏิบัตินี้</span><span class="sxs-lookup"><span data-stu-id="01da9-110">The demo data in the HQUS legal entity includes setup parameters that have been preset to support the steps in the walkthrough.</span></span> <span data-ttu-id="01da9-111">ถึงแม้ว่าการฝึกปฏิบัติจะระบุจุดบอดที่สำคัญและความท้าทายสำหรับบทบาทต่างๆ แต่สามารถดำเนินการให้เสร็จสิ้นได้โดยผู้ดูแลระบบ</span><span class="sxs-lookup"><span data-stu-id="01da9-111">Even though the walkthrough addresses key pain points and challenges for various roles, it can be completed by the system admin.</span></span>

## <a name="demo-scenario"></a><span data-ttu-id="01da9-112">สถานการณ์จำลองการสาธิต</span><span class="sxs-lookup"><span data-stu-id="01da9-112">Demo scenario</span></span>

<span data-ttu-id="01da9-113">ในนิติบุคคล HQUS ลำโพงคุณภาพสูงถูกผลิต</span><span class="sxs-lookup"><span data-stu-id="01da9-113">In the HQUS legal entity, high-end speakers are manufactured.</span></span> <span data-ttu-id="01da9-114">ในระหว่างกระบวนการผลิต ลำโพงจะผ่านการดำเนินงานสามรายการต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="01da9-114">During the manufacturing process, speakers go through the following three operations.</span></span>

- <span data-ttu-id="01da9-115">**แอสเซมบลีล่วงหน้า** – แคบิเนตลำโพงจะถูกรวบรวม</span><span class="sxs-lookup"><span data-stu-id="01da9-115">**Pre-assembly** – The speaker cabinet is assembled.</span></span> <span data-ttu-id="01da9-116">วัสดุสำหรับแคบิเนตจะถูกเบิกสินค้าในคลังสินค้าวัสดุ ก่อนที่จะเริ่มการดำเนินงาน</span><span class="sxs-lookup"><span data-stu-id="01da9-116">The material for the cabinet is picked in the material warehouse before the operation is started.</span></span>
- <span data-ttu-id="01da9-117">**การเคลือบ** – หลังจากมีการประกอบแคบิเนตลำโพง จะต้องมีการเคลือบ</span><span class="sxs-lookup"><span data-stu-id="01da9-117">**Coating** – After the speaker cabinet has been assembled, it must be coated.</span></span> <span data-ttu-id="01da9-118">การดำเนินงานนี้เสร็จสมบูรณ์โดยผู้จัดจำหน่าย (ผู้รับเหมาย่อย)</span><span class="sxs-lookup"><span data-stu-id="01da9-118">This operation is completed by a vendor (subcontractor).</span></span> <span data-ttu-id="01da9-119">แคบิเนตลำโพงที่แอสเซมบลีล่วงหน้า ถูกจัดส่งไปที่ผู้รับเหมาย่อยที่จะเคลือบ พร้อมกับวัสดุสองรายการ</span><span class="sxs-lookup"><span data-stu-id="01da9-119">The pre-assembled speaker cabinet is shipped to the coating subcontractor together with two materials.</span></span>
- <span data-ttu-id="01da9-120">**เสร็จสิ้น** – หลังจากแคบิเนตลำโพงที่มีการแอสเซมบลีล่วงหน้าได้ถูกเคลือบโดยผู้รับเหมาย่อย จะมีการส่งกลับไปยังนิติบุคคล HQUS เพื่อให้แอสเซมบลีขั้นสุดท้ายของลำโพงสามารถทำให้เสร็จสมบูรณ์ได้</span><span class="sxs-lookup"><span data-stu-id="01da9-120">**Finish** – After the pre-assembled speaker cabinet has been coated by the subcontractor, it's returned to the HQUS legal entity so that final assembly of the speaker can be completed.</span></span>

<span data-ttu-id="01da9-121">ภาพประกอบต่อไปนี้แสดงการดำเนินงานสามรายการและวัสดุที่จะใช้</span><span class="sxs-lookup"><span data-stu-id="01da9-121">The following illustration shows the three operations and the materials that they consume.</span></span>

![แอสเซมบลีล่วงหน้า การเคลือบ และเสร็จสิ้นการดำเนินงาน และวัสดุที่จะใช้](./media/subcontract01_operations-materials.png)

## <a name="setup"></a><span data-ttu-id="01da9-123">การตั้งค่า</span><span class="sxs-lookup"><span data-stu-id="01da9-123">Setup</span></span>

<span data-ttu-id="01da9-124">ก่อนที่คุณจะเริ่มต้นการฝึกปฏิบัติ คุณต้องตั้งค่าข้อมูล</span><span class="sxs-lookup"><span data-stu-id="01da9-124">Before you start the walkthrough, you must set up the data.</span></span>

### <a name="set-up-the-finished-product"></a><span data-ttu-id="01da9-125">ตั้งค่าผลิตภัณฑ์สำเร็จรูป</span><span class="sxs-lookup"><span data-stu-id="01da9-125">Set up the finished product</span></span>

<span data-ttu-id="01da9-126">กระบวนงานนี้นำคุณผ่านการตั้งค่าของผลิตภัณฑ์ที่นำออกใช้ D8100 "แคบิเนตที่เคลือบ"</span><span class="sxs-lookup"><span data-stu-id="01da9-126">This procedure takes you through the setup of released product D8100, "Coated Cabinet."</span></span>

1. <span data-ttu-id="01da9-127">เลือก **การจัดการข้อมูลผลิตภัณฑ์ \> ผลิตภัณฑ์ \> ผลิตภัณฑ์ที่นำออกใช้** เพื่อเปิดหน้า **รายละเอียดผลิตภัณฑ์ที่นำออกใช้**</span><span class="sxs-lookup"><span data-stu-id="01da9-127">Select **Product information management \> Products \> Released products** to open the **Released product details** page.</span></span>
2. <span data-ttu-id="01da9-128">ในฟิลด์ตัวกรองด่วน ป้อน **D8100** เพื่อค้นหาผลิตภัณฑ์ที่นำออกใช้ที่มีอยู่</span><span class="sxs-lookup"><span data-stu-id="01da9-128">In the quick filter field, enter **D8100** to find the existing released product.</span></span>

    ![การกรองข้อมูลสำหรับผลิตภัณฑ์ที่นำออกใช้ D8100 บนหน้ารายละเอียดผลิตภัณฑ์ที่นำออกใช้](./media/subcontract02_filtering-released-products.png)

3. <span data-ttu-id="01da9-130">ในบานหน้าต่างการดำเนินการ บนแท็บ **วิศวกรรม** เลือก **กระบวนการผลิต** เพื่อเปิดหน้า **กระบวนการผลิต**</span><span class="sxs-lookup"><span data-stu-id="01da9-130">On the Action Pane, on the **Engineer** tab, select **Route** to open the **Route** page.</span></span>

    <span data-ttu-id="01da9-131">หน้า **กระบวนการผลิต** แสดงเวอร์ชันกระบวนการผลิตทั้งแปดเวอร์ชันสำหรับผลิตภัณฑ์ที่นำออกใช้ D8100</span><span class="sxs-lookup"><span data-stu-id="01da9-131">The **Route** page shows the eight route versions for released product D8100.</span></span> <span data-ttu-id="01da9-132">เวอร์ชันกระบวนการผลิตแปดกระบวนจะถูกแบ่งในกระบวนการผลิตสี่รายการบนไซต์ 1 และไซต์ 5</span><span class="sxs-lookup"><span data-stu-id="01da9-132">The eight route versions are divided among four routes on site 1 and site 5.</span></span> <span data-ttu-id="01da9-133">มีการใช้กระบวนการผลิตสำหรับการคิดต้นทุน กระบวนการผลิต 00041 ถูกใช้เมื่อการดำเนินงานการเคลือบเป็นการดำเนินงานภายใน และมีการใช้กระบวนการผลิต 00042 เมื่อการดำเนินงานการเคลือบเป็นการดำเนินงานภายนอก</span><span class="sxs-lookup"><span data-stu-id="01da9-133">Route 000400 is used for costing, route 00041 is used when the Coating operation is an internal operation, and route 00042 is used when the Coating operation is an external operation.</span></span>

    ![เวอร์ชันกระบวนการผลิตแปดกระบวนการบนหน้ากระบวนการผลิต](./media/subcontract03_route-page.png)

4. <span data-ttu-id="01da9-135">ในบานหน้าต่างด้านบน ในกริด **รุ่น** เลือกรุ่นกระบวนการผลิต **00042** สำหรับไซต์ **5**</span><span class="sxs-lookup"><span data-stu-id="01da9-135">In the upper pane, in the **Versions** grid, select route version **00042** for site **5**.</span></span>
5. <span data-ttu-id="01da9-136">ในบานหน้าต่างด้านล่าง บนแท็บ **ภาพรวม** เลือกการดำเนินงาน **20** (**Cbnt CtSc**) ในกริด</span><span class="sxs-lookup"><span data-stu-id="01da9-136">In the lower pane, on the **Overview** tab, select operation **20** (**Cbnt CtSc**) in the grid.</span></span>

    ![การดำเนินงาน 20 สำหรับรุ่นกระบวนการผลิต 00042 สำหรับไซต์ 5 ที่เลือก](./media/subcontract04_route-version-operation.png)

6. <span data-ttu-id="01da9-138">เลือกแท็บ **ทั่วไป**</span><span class="sxs-lookup"><span data-stu-id="01da9-138">Select the **General** tab.</span></span>

    <span data-ttu-id="01da9-139">สังเกตว่า ฟิลด์ **ชนิดกระบวนการผลิต** ของฟิลด์ ถูกกำหนดเป็น **ผู้จัดจำหน่าย**</span><span class="sxs-lookup"><span data-stu-id="01da9-139">Notice that the field **Route type** field is set to **Vendor**.</span></span> <span data-ttu-id="01da9-140">ค่านี้บ่งชี้ว่า การดำเนินงาน 20 (Cbnt CtSc) เป็นการดำเนินงานที่รับเหมารายย่อย</span><span class="sxs-lookup"><span data-stu-id="01da9-140">This value indicates that operation 20 (Cbnt CtSc) is a subcontracted operation.</span></span>

    ![ฟิลด์ชนิดของกระบวนการผลิตที่ตั้งค่าเป็นผู้จัดจำหน่ายบนแท็บทั่วไป](./media/subcontract05_general-tab.png)

7. <span data-ttu-id="01da9-142">เลือกแท็บ **ความต้องการทรัพยากร**</span><span class="sxs-lookup"><span data-stu-id="01da9-142">Select the **Resource requirements** tab.</span></span>

    <span data-ttu-id="01da9-143">จะมีการใช้ความสามารถในการค้นหาทรัพยากรที่เกี่ยวข้องในระหว่างการจัดตารางการผลิต</span><span class="sxs-lookup"><span data-stu-id="01da9-143">Capabilities will be used to find an applicable resource during production scheduling.</span></span> <span data-ttu-id="01da9-144">สำหรับการดำเนินงาน 20 (Cbnt CtSc) ให้สังเกตว่า ทรัพยากรที่มีความสามารถสองรายการ **การเคลือบ** และ **แคบิเนตที่เคลือบ** มีความจำเป็น</span><span class="sxs-lookup"><span data-stu-id="01da9-144">For operation 20 (Cbnt CtSc), notice that a resource that has two capabilities, **Coating** and **Coated cabinets**, is required.</span></span>

    ![ความสามารถในการเคลือบและแคบิเนตที่เคลือบบนแท็บความต้องการทรัพยากร](./media/subcontract06_resource-requirements-tab.png)

8. <span data-ttu-id="01da9-146">เลือก **ทรัพยากรที่ใช้ได้** เพื่อเปิดกล่องโต้ตอบ **ทรัพยากรที่ใช้ได้**</span><span class="sxs-lookup"><span data-stu-id="01da9-146">Select **Applicable resources** to open the **Applicable resources** dialog box.</span></span>

    <span data-ttu-id="01da9-147">พบทรัพยากรสามรายการที่ตรงกับความต้องการทรัพยากรสำหรับการดำเนินงาน</span><span class="sxs-lookup"><span data-stu-id="01da9-147">Three resources are found that match the resource requirements for the operation.</span></span> <span data-ttu-id="01da9-148">โปรดสังเกตว่า ทรัพยากร 8851 และ 8852 ของชนิด **ผู้จัดจำหน่าย**</span><span class="sxs-lookup"><span data-stu-id="01da9-148">Notice that resources 8851 and 8852 are of the **Vendor** type.</span></span>

    ![ทรัพยากรที่เหมาะสมสามรายการในกล่องโต้ตอบทรัพยากรที่ใช้ได้](./media/subcontract07_applicable-resources-dialog.png)

9. <span data-ttu-id="01da9-150">เลือก **ตกลง** เพื่อปิดกล่องโต้ตอบ **ทรัพยากรที่ใช้ได้** และกลับไปยังหน้า **กระบวนการผลิต**</span><span class="sxs-lookup"><span data-stu-id="01da9-150">Select **OK** to close the **Applicable resources** dialog box and return to the **Route** page.</span></span>
10. <span data-ttu-id="01da9-151">ปิดหน้า **กระบวนการผลิต** เพื่อกลับไปยังหน้า **รายละเอียดผลิตภัณฑ์ที่นำออกใช้**</span><span class="sxs-lookup"><span data-stu-id="01da9-151">Close the **Route** page to return to the **Released product details** page.</span></span>

    ![หน้ารายละเอียดผลิตภัณฑ์ที่นำออกใช้](./media/subcontract08_released-product-details-page.png)

11. <span data-ttu-id="01da9-153">ในบานหน้าต่างการดำเนินการ บนแท็บ **วิศวกรรม** เลือก **รุ่น BOM** เพื่อเปิดหน้า **รุ่น BOM**</span><span class="sxs-lookup"><span data-stu-id="01da9-153">On the Action Pane, on the **Engineer** tab, select **BOM versions** to open the **BOM versions** page.</span></span>

    <span data-ttu-id="01da9-154">หน้า **รุ่น BOM** แสดงรุ่นของสูตรการผลิต (BOM) สี่รายการสำหรับผลิตภัณฑ์ที่นำออกใช้ D8100</span><span class="sxs-lookup"><span data-stu-id="01da9-154">The **BOM versions** page shows the four bill of materials (BOM) versions for released product D8100.</span></span> <span data-ttu-id="01da9-155">BOM 000040 จะใช้สำหรับการคิดต้นทุน และการวางแผน BOM 000041 จะถูกใช้ ถ้าทำการดำเนินงานการเคลือบเสร็จสิ้นภายในบริษัท และ BOMs 000042 และ 000043 จะใช้ ถ้ามีการรับเหมารายย่อยดำเนินการเคลือบ</span><span class="sxs-lookup"><span data-stu-id="01da9-155">BOM 000040 is used for costing and planning, BOM 000041 is used if the Coating operation is done in-house, and BOMs 000042 and 000043 are used if the Coating operation is subcontracted.</span></span>

    <span data-ttu-id="01da9-156">โปรดสังเกตว่า สินค้า S8050 เป็นผลิตภัณฑ์ของชนิดสินค้า **บริการ**</span><span class="sxs-lookup"><span data-stu-id="01da9-156">Notice that item S8050 is a product of the **Service** item type.</span></span> <span data-ttu-id="01da9-157">รายการนี้แสดงถึงงานรับเหมารายย่อย</span><span class="sxs-lookup"><span data-stu-id="01da9-157">This item represents the subcontracted work.</span></span>

    ![รุ่น BOM สี่รายการบนหน้ารุ่น BOM](./media/subcontract09_bom-versions-page.png)

12. <span data-ttu-id="01da9-159">บน FastTab **รายการสูตรการผลิต** เลือก **แก้ไข** เพื่อเปิดกล่องโต้ตอบ **แก้ไขรายการ BOM**</span><span class="sxs-lookup"><span data-stu-id="01da9-159">On the **Bill of materials lines** FastTab, select **Edit** to open the **Edit BOM line** dialog box.</span></span>

    <span data-ttu-id="01da9-160">เมื่อใบสั่งผลิตถูกสร้างขึ้น และถูกประเมินไว้สำหรับผลิตภัณฑ์ที่นำออกใช้ D8100 ใบสั่งซื้อจะถูกสร้างขึ้นโดยอัตโนมัติสำหรับสินค้า S8050</span><span class="sxs-lookup"><span data-stu-id="01da9-160">When a production order is created and estimated for released product D8100, a purchase order will be automatically generated for item S8050.</span></span> <span data-ttu-id="01da9-161">ใบสั่งซื้อนี้จะเชื่อมโยงกับใบสั่งผลิต</span><span class="sxs-lookup"><span data-stu-id="01da9-161">This purchase order will be linked to the production order.</span></span> <span data-ttu-id="01da9-162">สำหรับใบสั่งซื้อที่จะถูกสร้างขึ้นโดยอัตโนมัติ ต้องตั้งค่าฟิลด์ **ชนิดรายการ** เป็น **ผู้จัดจำหน่าย** และต้องเลือกบัญชีผู้จัดจำหน่ายสำหรับการรับเหมารายย่อย</span><span class="sxs-lookup"><span data-stu-id="01da9-162">For purchase orders to be automatically generated, the **Line type** field must be set to **Vendor**, and the vendor account for the subcontractor must be selected.</span></span> <span data-ttu-id="01da9-163">ในกรณีนี้ บัญชีผู้จัดจำหน่ายคือ US-801</span><span class="sxs-lookup"><span data-stu-id="01da9-163">In this case, the vendor account is US-801.</span></span>

    <span data-ttu-id="01da9-164">โปรดสังเกตว่า รายการ BOM เชื่อมต่อไปยังขั้นตอนการเคลือบโดยใช้หมายเลขการดำเนินงาน (ในกรณีนี้ 20)</span><span class="sxs-lookup"><span data-stu-id="01da9-164">Notice that the BOM line is connected to the Coating operation through the operation number (in this case, 20).</span></span>

    ![แก้ไขกล่องโต้ตอบของรายการ BOM](./media/subcontract10_edit-bom-line-dialog.png)

### <a name="create-a-password-for-warehouse-workers"></a><span data-ttu-id="01da9-166">สร้างรหัสผ่านสำหรับผู้ปฏิบัติงานคลังสินค้า</span><span class="sxs-lookup"><span data-stu-id="01da9-166">Create a password for warehouse workers</span></span>

<span data-ttu-id="01da9-167">คุณต้องกำหนดรหัสผ่านสำหรับผู้ปฏิบัติงานคลังสินค้าที่ใช้อุปกรณ์แฮนด์เฮลด์</span><span class="sxs-lookup"><span data-stu-id="01da9-167">You must define a password for the warehouse workers who use the hand-held device.</span></span>

1. <span data-ttu-id="01da9-168">เลือก **การบริหารคลังสินค้า \> ตั้งค่า \> ผู้ปฏิบัติงาน** ให้เปิดหน้า **ผู้ใช้ในงาน**</span><span class="sxs-lookup"><span data-stu-id="01da9-168">Select **Warehouse management \> Setup \> Worker** to open the **Work users** page.</span></span>
2. <span data-ttu-id="01da9-169">บน FastTab **ผู้ใช้** เลือกแถวสำหรับผู้ใช้ **51**</span><span class="sxs-lookup"><span data-stu-id="01da9-169">On the **Users** FastTab, select the row for user **51**.</span></span>

    ![หน้าผู้ใช้ในงาน](./media/subcontract11_work-users-page.png)

3. <span data-ttu-id="01da9-171">เลือก **รีเซ็ตรหัสผ่าน**</span><span class="sxs-lookup"><span data-stu-id="01da9-171">Select **Reset password**.</span></span>
4. <span data-ttu-id="01da9-172">ในฟิลด์ **รหัสผ่าน** และ **ยืนยันรหัสผ่าน** ป้อน **1**</span><span class="sxs-lookup"><span data-stu-id="01da9-172">In the **Password** and **Confirm password** fields, enter **1**.</span></span>
5. <span data-ttu-id="01da9-173">เลือก **ตั้งค่าหัสผ่าน**</span><span class="sxs-lookup"><span data-stu-id="01da9-173">Select **Set password**.</span></span>

## <a name="step-by-step-walkthrough"></a><span data-ttu-id="01da9-174">คำแนะนำการใช้งานทีละขั้นตอน</span><span class="sxs-lookup"><span data-stu-id="01da9-174">Step-by-step walkthrough</span></span>

<span data-ttu-id="01da9-175">**สถานการณ์จำลองและเบื้องหลัง**</span><span class="sxs-lookup"><span data-stu-id="01da9-175">**Scenario and background**</span></span>

<span data-ttu-id="01da9-176">มีการสร้างใบสั่งผลิต 10 ชิ้นสำหรับผลิตภัณฑ์ D8100 "แคบิเนตที่เคลือบ"</span><span class="sxs-lookup"><span data-stu-id="01da9-176">A production order of 10 pieces is created for product D8100, "Coated Cabinet."</span></span> <span data-ttu-id="01da9-177">การเคลือบของแคบิเนตเป็นการดำเนินการทำสัญญาย่อยที่ดำเนินการที่ผู้จัดจำหน่าย US-801 Perfect Coating Solutions</span><span class="sxs-lookup"><span data-stu-id="01da9-177">The coating of the cabinets is a sub-contracted operation that is done at vendor US-801, Perfect Coating Solutions.</span></span> <span data-ttu-id="01da9-178">ใบสั่งผลิตประกอบด้วยการดำเนินงานสามรายการ</span><span class="sxs-lookup"><span data-stu-id="01da9-178">The production order consists of three operations.</span></span> <span data-ttu-id="01da9-179">ในการดำเนินงานแรก แคบิเนตถูกประกอบล่วงหน้าเป็นการดำเนินการภายในองค์กร</span><span class="sxs-lookup"><span data-stu-id="01da9-179">In the first operation, the cabinet is pre-assembled as an in-house operation.</span></span> <span data-ttu-id="01da9-180">วัสดุสำหรับแอสเซมบลีล่วงหน้า ถูกนำออกใช้สำหรับการเบิกสินค้าในคลังสินค้าที่จัดหาวัตถุดิบ</span><span class="sxs-lookup"><span data-stu-id="01da9-180">The material for the pre-assembly is released for picking in the raw material warehouse.</span></span> <span data-ttu-id="01da9-181">หลังจากแอสเซมบลีล่วงหน้าเสร็จสมบูรณ์ แคบิเนตที่แอสเซมบลีล่วงหน้าถูกส่งไปยัง Perfect Coating Solutions พร้อมกับวัสดุสองรายการที่จำเป็นสำหรับการดำเนินงานการเคลือบ</span><span class="sxs-lookup"><span data-stu-id="01da9-181">After the pre-assembly is completed, the pre-assembled cabinet is sent to Perfect Coating Solutions together with two materials that are required for the Coating operation.</span></span> <span data-ttu-id="01da9-182">เมื่อแคบิเนตที่เคลือบได้รับกลับมาจากผู้จัดจำหน่าย จะผ่านการดำเนินการแอสเซมบลีภายในองค์กรขั้นสุดท้าย ก่อนที่จะมีการรายงานเป็นเสร็จสมบูรณ์</span><span class="sxs-lookup"><span data-stu-id="01da9-182">When the coated cabinet is received back from the vendor, it goes through a final in-house assembly operation before it's reported as finished.</span></span>

1. <span data-ttu-id="01da9-183">เลือก **การควบคุมการผลิต \> ใบสั่งผลิต \> ใบสั่งผลิตทั้งหมด** เพื่อเปิดหน้า **ใบสั่งผลิตทั้งหมด**</span><span class="sxs-lookup"><span data-stu-id="01da9-183">Select **Production control \> Production orders \> All production orders** to open the **All production orders** page.</span></span>
2. <span data-ttu-id="01da9-184">ในบานหน้าต่างการดำเนินการ เลือก **ใบสั่งผลิตใหม่** เพื่อเปิดกล่องโต้ตอบ **สร้างใบสั่งผลิต**</span><span class="sxs-lookup"><span data-stu-id="01da9-184">On the Action Pane, select **New production order** to open the **Create production order** dialog box.</span></span>

    ![สร้างกล่องโต้ตอบใบสั่งผลิต](./media/subcontract12_create-production-order-dialog.png)

3. <span data-ttu-id="01da9-186">ในฟิลด์ **หมายเลขสินค้า** ให้เลือก **D8100**</span><span class="sxs-lookup"><span data-stu-id="01da9-186">In the **Item number** field, select **D8100**.</span></span>
4. <span data-ttu-id="01da9-187">หลังจากที่คุณเลือกหมายเลขสินค้า ฟิลด์สำหรับมิติสินค้าคงคลังจะปรากฏ</span><span class="sxs-lookup"><span data-stu-id="01da9-187">After you select the item number, fields for the inventory dimensions appear.</span></span> <span data-ttu-id="01da9-188">ในฟิลด์ **สี** ให้เลือก **โครเมียม**</span><span class="sxs-lookup"><span data-stu-id="01da9-188">In the **Color** field, select **Chrome**.</span></span>

    <span data-ttu-id="01da9-189">กล่องข้อความปรากฏขึ้นเพื่อถามว่า ควรแทรกรุ่นที่ใช้งานอยู่สำหรับ BOM และกระบวนการผลิตหรือไม่</span><span class="sxs-lookup"><span data-stu-id="01da9-189">A message box appears that asks whether the active versions for the BOM and route should be inserted.</span></span>

    ![กล่องข้อความ](./media/subcontract13_message-box.png)

5. <span data-ttu-id="01da9-191">เลือก **ใช่**</span><span class="sxs-lookup"><span data-stu-id="01da9-191">Select **Yes**.</span></span> 

    <span data-ttu-id="01da9-192">ในกล่องโต้ตอบ **สร้างใบสั่งผลิต** รุ่นของ BOM ที่ใช้งานอยู่และกระบวนการผลิตสำหรับผลิตภัณฑ์ D8100 จะถูกเลือกโดยอัตโนมัติในฟิลด์ **หมายเลข BOM** และ **หมายเลขกระบวนการผลิต** ตามลำดับ</span><span class="sxs-lookup"><span data-stu-id="01da9-192">In the **Create production order** dialog box, the active versions of the BOM and route for product D8100 are automatically selected in the **BOM number** and **Route number** fields, respectively.</span></span> <span data-ttu-id="01da9-193">ในกรณีนี้ BOM **000040** และกระบวนการผลิต **000040** จะถูกเลือกไว้</span><span class="sxs-lookup"><span data-stu-id="01da9-193">In this case, BOM **000040** and route **000040** are selected.</span></span>
    
    > [!NOTE]
    > <span data-ttu-id="01da9-194">สำหรับทั้ง BOM และกระบวนการผลิต รุ่น 000040 จะใช้สำหรับการคิดต้นทุน และการวางแผน</span><span class="sxs-lookup"><span data-stu-id="01da9-194">For both the BOM and the route, version 000040 is used for costing and planning.</span></span>

6. <span data-ttu-id="01da9-195">ในฟิลด์ **ไซต์** ให้เลือก **5**</span><span class="sxs-lookup"><span data-stu-id="01da9-195">In the **Site** field, select **5**.</span></span>
7. <span data-ttu-id="01da9-196">ในฟิลด์  **คลังสินค้า** เลือก **51**</span><span class="sxs-lookup"><span data-stu-id="01da9-196">In the **Warehouse** field, select **51**.</span></span>
8. <span data-ttu-id="01da9-197">ในฟิลด์ **หมายเลข BOM** และ **หมายเลขกระบวนการผลิต** เปลี่ยนค่าที่ถูกเลือกโดยอัตโนมัติเป็น **000042**</span><span class="sxs-lookup"><span data-stu-id="01da9-197">In the **BOM number** and **Route number** fields, change the value that was automatically selected to **000042**.</span></span>

    > [!NOTE]
    > <span data-ttu-id="01da9-198">สำหรับทั้ง BOM และกระบวนการผลิต รุ่น 000042 ถูกใช้เพื่อรับเหมาการเคลือบรายย่อยของแคบิเนตกับผู้จัดจำหน่าย US-801</span><span class="sxs-lookup"><span data-stu-id="01da9-198">For both the BOM and the route, version 000042 is used to subcontract the coating of the cabinet to vendor US-801.</span></span>

    ![การตั้งค่าในกล่องโต้ตอบการสร้างใบสั่งผลิต](./media/subcontract14_create-production-order-dialog-set.png)

9. <span data-ttu-id="01da9-200">เลือก **สร้าง** เพื่อสร้างใบสั่งผลิต และกลับไปยังหน้า **ใบสั่งผลิตทั้งหมด**</span><span class="sxs-lookup"><span data-stu-id="01da9-200">Select **Create** to create the production order and return to the **All production orders** page.</span></span>

    ![ใบสั่งผลิตใหม่บนหน้าใบสั่งผลิตทั้งหมด](./media/subcontract15_new-production-order.png)

10. <span data-ttu-id="01da9-202">ในบานหน้าต่างการดำเนินการ บนแท็บ **ใบสั่งผลิต** เลือก **ประมาณ** เพื่อเปิดกล่องโต้ตอบ **ประมาณ**</span><span class="sxs-lookup"><span data-stu-id="01da9-202">On the Action Pane, on the **Production order** tab, select **Estimate** to open the **Estimate** dialog box.</span></span>

    ![กล่องโต้ตอบการประมาณ](./media/subcontract16_estimate-dialog.png)

11. <span data-ttu-id="01da9-204">เลือก **ตกลง** เพื่อยืนยันการประมาณ และกลับไปยังหน้า **ใบสั่งผลิตทั้งหมด**</span><span class="sxs-lookup"><span data-stu-id="01da9-204">Select **OK** to confirm the estimate and return to the **All production orders** page.</span></span>

    > [!NOTE]
    > <span data-ttu-id="01da9-205">เมื่อประเมินใบสั่งผลิต ใบสั่งซื้อสำหรับสินค้าบริการ S8050 จะถูกสร้างขึ้นสำหรับผู้จัดจำหน่าย 801 US-801</span><span class="sxs-lookup"><span data-stu-id="01da9-205">When the production order is estimated, the purchase order for service item S8050 is generated for vendor US-801.</span></span>

12. <span data-ttu-id="01da9-206">ในบานหน้าต่างการดำเนินการ บนแท็บ **ใบสั่งผลิต** เลือก **BOM** เพื่อเปิดหน้า **BOM** ที่ซึ่งคุณสามารถดูรายการ BOM สำหรับใบสั่งผลิตได้</span><span class="sxs-lookup"><span data-stu-id="01da9-206">On the Action Pane, on the **Production order** tab, select **BOM** to open the **BOM** page, where you can view the BOM lines for the production order.</span></span>

    <span data-ttu-id="01da9-207">สำหรับสินค้าบริการ S8050 โปรดสังเกตว่า มีการอ้างอิงถึงใบสั่งซื้อที่สร้างขึ้นเมื่อมีการประเมินใบสั่งผลิต</span><span class="sxs-lookup"><span data-stu-id="01da9-207">For service item S8050, notice that there is a reference to the purchase order that was generated when the production order was estimated.</span></span>

    ![รายการ BOM ใบสั่งการผลิตบนหน้า BOM](./media/subcontract17_production-order-bom-lines.png)

13. <span data-ttu-id="01da9-209">ปิดหน้า **BOM** เพื่อกลับไปยังหน้า **ใบสั่งผลิตทั้งหมด**</span><span class="sxs-lookup"><span data-stu-id="01da9-209">Close the **BOM** page to return to the **All production orders** page.</span></span>
14. <span data-ttu-id="01da9-210">ในบานหน้าต่างการดำเนินการ บนแท็บ **กำหนดการ** เลือก **งานกำหนดการ** เพื่อเปิดกล่องโต้ตอบ **การจัดกำหนดการงาน**</span><span class="sxs-lookup"><span data-stu-id="01da9-210">On the Action Pane, on the **Schedule** tab, select **Schedule jobs** to open the **Job scheduling** dialog box.</span></span>
15. <span data-ttu-id="01da9-211">ระบุค่าต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="01da9-211">Specify the following values:</span></span>

    - <span data-ttu-id="01da9-212">ในฟิลด์ **ทิศทางการจัดกำหนดการ** ให้เลือก **ไปข้างหน้าตั้งแต่วันพรุ่งนี้**</span><span class="sxs-lookup"><span data-stu-id="01da9-212">In the **Scheduling direction** field, select **Forward from tomorrow**.</span></span>
    - <span data-ttu-id="01da9-213">ตั้งค่าตัวเลือก **กำลังการผลิตที่มีจำกัด** เป็น **ใช่**</span><span class="sxs-lookup"><span data-stu-id="01da9-213">Set the **Finite capacity** option to **Yes**.</span></span>

    ![กล่องโต้ตอบการจัดตารางงาน](./media/subcontract18_job-scheduling-dialog.png)

16. <span data-ttu-id="01da9-215">เลือก **ตกลง** เพื่อปิดกล่องโต้ตอบ **การจัดตารางงาน** และกลับไปยังหน้า **ใบสั่งผลิตทั้งหมด**</span><span class="sxs-lookup"><span data-stu-id="01da9-215">Select **OK** to close the **Job scheduling** dialog box and return to the **All production orders** page.</span></span>
17. <span data-ttu-id="01da9-216">ในบานหน้าต่างการดำเนินการ บนแท็บ **กำหนดการ** เลือก **Gantt** เพื่อเปิดหน้า **แผนภูมิ Gantt - มุมมองทรัพยากร**</span><span class="sxs-lookup"><span data-stu-id="01da9-216">On the Action Pane, on the **Schedule** tab, select **Gantt** to open the **Gantt chart - Resource view** page.</span></span>

    <span data-ttu-id="01da9-217">แผนภูมิ Gantt แสดงภาพรวมของวิธีการจัดกำหนดการงานการผลิตบนทรัพยากร</span><span class="sxs-lookup"><span data-stu-id="01da9-217">The Gantt chart provides a visual overview of how the production jobs are scheduled on the resources.</span></span> <span data-ttu-id="01da9-218">สังเกตว่า การดำเนินงานการเคลือบภายนอกประกอบด้วยงาน 3 งาน: งานในกระบวนการ งานขนส่ง และงานเวลาคิว</span><span class="sxs-lookup"><span data-stu-id="01da9-218">Notice that the external Coating operation consists of three jobs: a process job, a transport job, and a queue time job.</span></span>

    ![แผนภูมิ Gantt บนแผนภูมิ Gantt - หน้ามุมมองทรัพยากร](./media/subcontract19_gantt-chart.png)

18. <span data-ttu-id="01da9-220">ปิดหน้า **แผนภูมิ Gantt - มุมมองทรัพยากร** เพื่อกลับไปยังหน้า **ใบสั่งผลิตทั้งหมด**</span><span class="sxs-lookup"><span data-stu-id="01da9-220">Close the **Gantt chart - Resource view** page to return to the **All production orders** page.</span></span>
19. <span data-ttu-id="01da9-221">ในบานหน้าต่างการดำเนินการ บนแท็บ **ใบสั่งผลิต** เลือก **นำออกใช้** เพื่อเปิดกล่องโต้ตอบ **นำออกใช้**</span><span class="sxs-lookup"><span data-stu-id="01da9-221">On the Action Pane, on the **Production order** tab, select **Release** to open the **Release** dialog box.</span></span>

    ![นำกล่องโต้ตอบออกใช้](./media/subcontract20_release-dialog.png)

20. <span data-ttu-id="01da9-223">เลือก **ตกลง** เพื่อปิดกล่องโต้ตอบ **นำออกใช้**</span><span class="sxs-lookup"><span data-stu-id="01da9-223">Select **OK** to close the **Release** dialog box.</span></span>
21. <span data-ttu-id="01da9-224">เลือก **การควบคุมการผลิต \> งานประจำงวด \> นำออกใช้ไปยังคลังสินค้า \> นำ BOM และรายการสูตรออกใช้อัตโนมัติ** เพื่อเปิดกล่องโต้ตอบ **นำ BOM และรายการสูตรออกใช้อัตโนมัติ**</span><span class="sxs-lookup"><span data-stu-id="01da9-224">Select **Production control \> Periodic tasks \> Release to warehouse \> Automatic release of BOM and formula lines** to open the **Automatic release of BOM and formula lines** dialog box.</span></span>

    ![กล่องโต้ตอบการนำ BOM และรายการสูตรออกใช้อัตโนมัติ](./media/subcontract21_auto-release-bom-formula-lines-dialog.png)

22. <span data-ttu-id="01da9-226">เลือก **ตกลง** เพื่อเรียกใช้งานการนำ BOM และรายการสูตรออกใช้อัตโนมัติ</span><span class="sxs-lookup"><span data-stu-id="01da9-226">Select **OK** to run the Automatic release of BOM and formula lines job.</span></span>

    <span data-ttu-id="01da9-227">งานนี้นำออกใช้งานการเบิกสินค้าสำหรับวัตถุดิบไปยังคลังสินค้า</span><span class="sxs-lookup"><span data-stu-id="01da9-227">This job releases pick work for raw materials to the warehouse.</span></span>

23. <span data-ttu-id="01da9-228">เลือก **การควบคุมการผลิต \> ใบสั่งผลิต \> ใบสั่งผลิตทั้งหมด** เพื่อเปิดหน้า **ใบสั่งผลิตทั้งหมด**</span><span class="sxs-lookup"><span data-stu-id="01da9-228">Select **Production control \> Production orders \> All production orders** to open the **All production orders** page.</span></span>
24. <span data-ttu-id="01da9-229">ใช้ฟิลด์ตัวกรองด่วนเพื่อเลือกใบสั่งผลิตที่คุณได้ทำงานอยู่ด้วย</span><span class="sxs-lookup"><span data-stu-id="01da9-229">Use the quick filter field to select the production order that you've been working on.</span></span>
25. <span data-ttu-id="01da9-230">ในบานหน้าต่างการดำเนินการ บนแท็บ **คลังสินค้า** เลือก **รายละเอียดงาน** เพื่อเปิดหน้า **งาน**</span><span class="sxs-lookup"><span data-stu-id="01da9-230">On the Action Pane, on the **Warehouse** tab, select **Work details** to open the **Work** page.</span></span>

    <span data-ttu-id="01da9-231">โปรดสังเกตว่า หน้าแสดงชุดงานสองชุดสำหรับการเบิกวัตถุดิบ</span><span class="sxs-lookup"><span data-stu-id="01da9-231">Notice that the page shows two sets of work for raw material picking.</span></span> <span data-ttu-id="01da9-232">งานแรกสำหรับวัสดุ M8100 และ M8101</span><span class="sxs-lookup"><span data-stu-id="01da9-232">The first work is for materials M8100 and M8101.</span></span> <span data-ttu-id="01da9-233">วัสดุเหล่านี้ถูกใช้ไปในการดำเนินงาน 10</span><span class="sxs-lookup"><span data-stu-id="01da9-233">These materials are consumed by operation 10.</span></span> <span data-ttu-id="01da9-234">งานที่สองสำหรับวัสดุ M8202 และ M8250</span><span class="sxs-lookup"><span data-stu-id="01da9-234">The second work is for materials M8202 and M8250.</span></span> <span data-ttu-id="01da9-235">วัสดุและส่วนประกอบเหล่านี้จะถูกใช้โดยการดำเนินงาน 20 ซึ่งเป็นการดำเนินงานที่รับเหมารายย่อย</span><span class="sxs-lookup"><span data-stu-id="01da9-235">These materials are consumed by operation 20, which is the subcontracted operation.</span></span>

    ![ชุดงานสองชุดสำหรับการเบิกวัตถุดิบในหน้างาน](./media/subcontract22_work-page.png)

26. <span data-ttu-id="01da9-237">เริ่มต้นแอปคลังสินค้าเพื่อดำเนินงานคลังสินค้าสำหรับการดำเนินงาน 10</span><span class="sxs-lookup"><span data-stu-id="01da9-237">Start the warehouse app to process the warehouse work for operation 10.</span></span>

    <!-- TBD – screen shots for processing pick work for the materials. -->

27. <span data-ttu-id="01da9-238">เลือก **การควบคุมการผลิต \> ใบสั่งผลิต \> ใบสั่งผลิตทั้งหมด** เพื่อเปิดหน้า **ใบสั่งผลิตทั้งหมด**</span><span class="sxs-lookup"><span data-stu-id="01da9-238">Select **Production control \> Production orders \> All production orders** to open the **All production orders** page.</span></span>
28. <span data-ttu-id="01da9-239">ใช้ฟิลด์ตัวกรองด่วนเพื่อเลือกใบสั่งผลิตที่คุณได้ทำงานอยู่ด้วย</span><span class="sxs-lookup"><span data-stu-id="01da9-239">Use the quick filter field to select the production order that you've been working on.</span></span>
29. <span data-ttu-id="01da9-240">ในบานหน้าต่างการดำเนินการ บนแท็บ **ใบสั่งผลิต** เลือก **เริ่มต้น** เพื่อเปิดกล่องโต้ตอบ **เริ่มต้น**</span><span class="sxs-lookup"><span data-stu-id="01da9-240">On the Action Pane, on the **Production order** tab, select **Start** to open the **Start** dialog box.</span></span>
30. <span data-ttu-id="01da9-241">บนแท็บ **ทั่วไป** ระบุค่าต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="01da9-241">On the **General** tab, specify the following values:</span></span>

    - <span data-ttu-id="01da9-242">ใน **หมายเลขการดำเนินงานเริ่มต้น**</span><span class="sxs-lookup"><span data-stu-id="01da9-242">In the **From Oper. No.**</span></span> <span data-ttu-id="01da9-243">ฟิลด์ เลือก **10**</span><span class="sxs-lookup"><span data-stu-id="01da9-243">field, select **10**.</span></span>
    - <span data-ttu-id="01da9-244">ใน **ไปที่หมายเลขการดำเนินงาน**</span><span class="sxs-lookup"><span data-stu-id="01da9-244">In the **To Oper. No.**</span></span> <span data-ttu-id="01da9-245">ฟิลด์ เลือก **10**</span><span class="sxs-lookup"><span data-stu-id="01da9-245">field, select **10**.</span></span>

    ![การตั้งค่าบนแท็บทั่วไป](./media/subcontract23_start-dialog.png)

31. <span data-ttu-id="01da9-247">เลือก **ตกลง** เพื่อปิดกล่องโต้ตอบ **เริ่มต้น** และกลับไปยังหน้า **ใบสั่งผลิตทั้งหมด**</span><span class="sxs-lookup"><span data-stu-id="01da9-247">Select **OK** to close the **Start** dialog box and return to the **All production orders** page.</span></span>

    <span data-ttu-id="01da9-248">ขอให้สังเกตว่าขณะนี้สถานะของใบสั่งผลิตเป็น **เริ่มต้นแล้ว**</span><span class="sxs-lookup"><span data-stu-id="01da9-248">Notice that the status of the production order is now **Started**.</span></span> <span data-ttu-id="01da9-249">มีการใช้วัสดุสำหรับการดำเนินงาน 10 โดยการลงรายการบัญชีโดยอัตโนมัติของสมุดรายวันรายการเบิกสินค้า</span><span class="sxs-lookup"><span data-stu-id="01da9-249">The materials for operation 10 are consumed by an automatic posting of the picking list journal.</span></span> <span data-ttu-id="01da9-250">ปริมาณการใช้เวลาสำหรับการดำเนินงาน 10 ถูกนำมาพิจารณา โดยการลงรายการของสมุดรายวันบัตรกระบวนการผลิตอัตโนมัติ</span><span class="sxs-lookup"><span data-stu-id="01da9-250">Time consumption for operation 10 is accounted for by an automatic posting of a route card journal.</span></span>

32. <span data-ttu-id="01da9-251">เริ่มต้นแอปคลังสินค้าเพื่อดำเนินงานคลังสินค้าสำหรับการดำเนินงาน 20</span><span class="sxs-lookup"><span data-stu-id="01da9-251">Start the warehouse app to process the warehouse work for operation 20.</span></span>

    <!-- TBD – screen shots for processing pick work for the materials. -->

33. <span data-ttu-id="01da9-252">ในบานหน้าต่างการดำเนินการ บนแท็บ **ใบสั่งผลิต** เลือก **เริ่มต้น** เพื่อเปิดกล่องโต้ตอบ **เริ่มต้น**</span><span class="sxs-lookup"><span data-stu-id="01da9-252">On the Action Pane, on the **Production order** tab, select **Start** to open the **Start** dialog box.</span></span>
34. <span data-ttu-id="01da9-253">บนแท็บ **ทั่วไป** ระบุค่าต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="01da9-253">On the **General** tab, specify the following values:</span></span>

    - <span data-ttu-id="01da9-254">ใน **หมายเลขการดำเนินงานเริ่มต้น**</span><span class="sxs-lookup"><span data-stu-id="01da9-254">In the **From Oper. No.**</span></span> <span data-ttu-id="01da9-255">ฟิลด์ เลือก **20**</span><span class="sxs-lookup"><span data-stu-id="01da9-255">field, select **20**.</span></span>
    - <span data-ttu-id="01da9-256">ใน **ไปที่หมายเลขการดำเนินงาน**</span><span class="sxs-lookup"><span data-stu-id="01da9-256">In the **To Oper. No.**</span></span> <span data-ttu-id="01da9-257">ฟิลด์ เลือก **20**</span><span class="sxs-lookup"><span data-stu-id="01da9-257">field, select **20**.</span></span>
    - <span data-ttu-id="01da9-258">ในฟิลด์ **ปริมาณ** ให้ป้อน **10**</span><span class="sxs-lookup"><span data-stu-id="01da9-258">In the **Quantity** field, enter **10**.</span></span>
    - <span data-ttu-id="01da9-259">ตั้งค่าตัวเลือก **ลงรายการบัญชีรายการเบิกสินค้าทันที** เป็น **ไม่**</span><span class="sxs-lookup"><span data-stu-id="01da9-259">Set the **Post picking list now** option to **No**.</span></span>

    ![การตั้งค่าบนแท็บทั่วไป](./media/subcontract24_general-tab.png)

35. <span data-ttu-id="01da9-261">เลือก **ตกลง** เพื่อปิดกล่องโต้ตอบ **เริ่มต้น** และกลับไปยังหน้า **ใบสั่งผลิตทั้งหมด**</span><span class="sxs-lookup"><span data-stu-id="01da9-261">Select **OK** to close the **Start** dialog box and return to the **All production orders** page.</span></span>

    <span data-ttu-id="01da9-262">มีการสร้างรายการเบิกสินค้าสำหรับวัสดุที่จะใช้ สำหรับการดำเนินการเคลือบ และสำหรับสินค้าบริการ</span><span class="sxs-lookup"><span data-stu-id="01da9-262">A picking list is created for the materials that are used for the Coating operation, and for the service item.</span></span> <span data-ttu-id="01da9-263">สินค้าบริการแสดงถึงต้นทุนของการดำเนินงานที่รับเหมารายย่อย</span><span class="sxs-lookup"><span data-stu-id="01da9-263">The service item represents the cost of the subcontracted operation.</span></span>

36. <span data-ttu-id="01da9-264">ในบานหน้าต่างการดำเนินการ บนแท็บ **มุมมอง** เลือก **รายการเบิกสินค้า** เพื่อเปิดหน้า **รายการเบิกสินค้า**</span><span class="sxs-lookup"><span data-stu-id="01da9-264">On the Action Pane, on the **View** tab, select **Picking list** to open the **Picking list** page.</span></span>
37. <span data-ttu-id="01da9-265">เลือกรายการเบิกสินค้าที่ไม่ได้ลงรายการบัญชี และจากนั้น เลือกหมายเลขสมุดรายวันเพื่อดูรายการสมุดรายวัน</span><span class="sxs-lookup"><span data-stu-id="01da9-265">Select the picking list that isn't posted, and then select the journal number to view the journal lines.</span></span>

    ![รายการสมุดรายวันในหน้ารายการเบิกสินค้า](./media/subcontract25_picking-list.png)

38. <span data-ttu-id="01da9-267">ในบานหน้าต่างการดำเนินการ เลือก **พิมพ์** \> **รายงานรายการเบิกสินค้า** เพื่อเปิดกล่องโต้ตอบ **รายงานรายการเบิกสินค้า**</span><span class="sxs-lookup"><span data-stu-id="01da9-267">On the Action Pane, select **Print** \> **Picking list report** to open the **Picking list report** dialog box.</span></span>
39. <span data-ttu-id="01da9-268">ตั้งค่าตัวเลือก **ใช้โครงร่างของบันทึกการจัดส่ง** เป็น **ใช่**</span><span class="sxs-lookup"><span data-stu-id="01da9-268">Set the **Use delivery note layout** option to **Yes**.</span></span>

    ![กล่องโต้ตอบรายงานรายการเบิกสินค้า](./media/subcontract26_picking-list-report-dialog.png)

40. <span data-ttu-id="01da9-270">เลือก **ตกลง** เพื่อสร้างรายงาน **รายการเบิกสินค้า**</span><span class="sxs-lookup"><span data-stu-id="01da9-270">Select **OK** to generate a **Picking list** report.</span></span>

    <span data-ttu-id="01da9-271">ในกรณีนี้ มีการพิมพ์บันทึกการจัดส่งของผู้จัดจำหน่ายจากสมุดรายวันรายการเบิกสินค้าสำหรับการผลิต</span><span class="sxs-lookup"><span data-stu-id="01da9-271">In this case, a vendor delivery note is printed from the production picking list journal.</span></span> <span data-ttu-id="01da9-272">บันทึกการจัดส่งระบุวัสดุที่มีการจัดส่งไปยังผู้จัดจำหน่ายที่จะทำการดำเนินการเคลือบ</span><span class="sxs-lookup"><span data-stu-id="01da9-272">The delivery note specifies the materials that are shipped to the vendor who will do the Coating operation.</span></span>

    ![รายงานรายการเบิกสินค้า](./media/subcontract27_picking-list-report.png)

41. <span data-ttu-id="01da9-274">ปิดรายงาน **รายการเบิกสินค้า** เพื่อกลับไปหน้า **รายการเบิกสินค้า**</span><span class="sxs-lookup"><span data-stu-id="01da9-274">Close the **Picking list** report to return to the **Picking list** page.</span></span>
42. <span data-ttu-id="01da9-275">ในบานหน้าต่างการดำเนินการ เลือก **ลงรายการบัญชี** เพื่อเปิดกล่องโต้ตอบ **ลงรายการบัญชีสมุดรายวัน**</span><span class="sxs-lookup"><span data-stu-id="01da9-275">On the Action Pane, select **Post** to open the **Post journal** dialog box.</span></span>

    ![กล่องโต้ตอบการลงรายการบัญชีสมุดรายวัน](./media/subcontract28_post-journal-dialog.png)

43. <span data-ttu-id="01da9-277">เลือก **ตกลง** เพื่อปิดกล่องโต้ตอบ **ลงรายการบัญชีสมุดรายวัน**</span><span class="sxs-lookup"><span data-stu-id="01da9-277">Select **OK** to close the **Post journal** dialog box.</span></span>
44. <span data-ttu-id="01da9-278">เปิดใบสั่งซื้อ</span><span class="sxs-lookup"><span data-stu-id="01da9-278">Open the purchase order.</span></span>

    ![หน้าใบสั่งซื้อ](./media/subcontract29_purchase-order-page.png)

45. <span data-ttu-id="01da9-280">ในบานหน้าต่างการดำเนินการ บนแท็บ **ซื้อ** เลือก **ยืนยัน**</span><span class="sxs-lookup"><span data-stu-id="01da9-280">On the Action Pane, on the **Purchase** tab, select **Confirm**.</span></span>
46. <span data-ttu-id="01da9-281">เลือก **ลงรายการบัญชี** เพื่อเปิดกล่องโต้ตอบ **ลงรายการบัญชีสมุดรายวัน**</span><span class="sxs-lookup"><span data-stu-id="01da9-281">Select **Post** to open the **Post journal** dialog box.</span></span>
47. <span data-ttu-id="01da9-282">เลือก **ตกลง** เพื่อปิดกล่องโต้ตอบ **ลงรายการบัญชีสมุดรายวัน** และกลับไปยังหน้า **ใบสั่งซื้อ**</span><span class="sxs-lookup"><span data-stu-id="01da9-282">Select **OK** to close the **Post journal** dialog box and return to the **Purchase order** page.</span></span>
48. <span data-ttu-id="01da9-283">เปลี่ยนราคาต่อหน่วยจาก **33** เป็น **40**</span><span class="sxs-lookup"><span data-stu-id="01da9-283">Change the unit price from **33** to **40**.</span></span>

    ![ราคาต่อหน่วยเปลี่ยนแปลงบนหน้าใบสั่งซื้อ](./media/subcontract30_unit-price.png)

49. <span data-ttu-id="01da9-285">ยืนยันใบสั่งซื้ออีกครั้ง</span><span class="sxs-lookup"><span data-stu-id="01da9-285">Confirm the purchase order again.</span></span>
50. <span data-ttu-id="01da9-286">ใบรับสินค้า</span><span class="sxs-lookup"><span data-stu-id="01da9-286">Product receipt.</span></span>

    ![กล่องโต้ตอบการลงรายการบัญชีใบรับสินค้า](./media/subcontract31_posting-product-receipt-dialog.png)

51. <span data-ttu-id="01da9-288">ใบแจ้งหนี้การซื้อ</span><span class="sxs-lookup"><span data-stu-id="01da9-288">Purchase invoice.</span></span>
52. <span data-ttu-id="01da9-289">อัพเดตสถานะการจับคู่</span><span class="sxs-lookup"><span data-stu-id="01da9-289">Update the match status.</span></span>

    ![หน้าใบแจ้งหนี้ของผู้จัดจำหน่าย](./media/subcontract32_vendor-invoice-page.png)

53. <span data-ttu-id="01da9-291">รายงานเป็นเสร็จสิ้น</span><span class="sxs-lookup"><span data-stu-id="01da9-291">Report as finished.</span></span>

    ![กล่องโต้ตอบการรายงานเป็นเสร็จสิ้น](./media/subcontract33_report-as-finished-dialog.png)

54. <span data-ttu-id="01da9-293">สิ้นสุด</span><span class="sxs-lookup"><span data-stu-id="01da9-293">End.</span></span>

    ![กล่องโต้ตอบการสิ้นสุด](./media/subcontract34_end-dialog.png)

55. <span data-ttu-id="01da9-295">การเปรียบเทียบต้นทุน</span><span class="sxs-lookup"><span data-stu-id="01da9-295">Cost comparison.</span></span>

    ![แผนภูมิการเปรียบเทียบต้นทุน](./media/subcontract35_cost-comparison-charts.png)

<span data-ttu-id="01da9-297">การตั้งค่าที่ขาดหายไปในข้อมูล</span><span class="sxs-lookup"><span data-stu-id="01da9-297">Missing setup in data.</span></span>
