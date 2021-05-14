---
title: รหัสการจัดประเภทการขนส่งด้วยรถยนต์ระดับชาติ (NMFC)
description: หัวข้อนี้อธิบายวิธีการใช้งานรหัสการจัดประเภทการขนส่งด้วยรถยนต์ระดับชาติ (NMFC) ใน Microsoft Dynamics 365 Supply Chain Management
author: Henrikan
ms.date: 04/22/2021
ms.topic: article
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: henrikan
ms.search.validFrom: 2021-04-22
ms.dyn365.ops.version: 10.0.8
ms.openlocfilehash: 0307437d3868f7ac34fa16a0913907a046ac14d4
ms.sourcegitcommit: 636c1bf096a8666a551b67e898da1f48feb9a187
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 04/26/2021
ms.locfileid: "5941893"
---
# <a name="national-motor-freight-classification-nmfc-codes"></a><span data-ttu-id="47b90-103">รหัสการจัดประเภทการขนส่งด้วยรถยนต์ระดับชาติ (NMFC)</span><span class="sxs-lookup"><span data-stu-id="47b90-103">National Motor Freight Classification (NMFC) codes</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="47b90-104">รหัสการจัดประเภทการขนส่งด้วยรถยนต์ระดับชาติ (NMFC) ช่วยคุณในการจัดประเภทสินค้าที่สามารถจัดส่งได้</span><span class="sxs-lookup"><span data-stu-id="47b90-104">National Motor Freight Classification (NMFC) codes help you classify items that can be shipped.</span></span> <span data-ttu-id="47b90-105">รหัส NMFC เป็นชื่อที่ใช้จัดกลุ่มชุดสินค้า</span><span class="sxs-lookup"><span data-stu-id="47b90-105">The NMFC code is a designation that is used to group commodities.</span></span> <span data-ttu-id="47b90-106">ซึ่งช่วยให้บริษัทขนส่งสามารถประเมินสินค้าเพื่อการจัดส่งสินค้าโดยการจัดประเภทสินค้าตามข้อควรพิจารณาต่าง ๆ เช่น รถบรรทุกแบบเข้าพอดี ปัญหาการโหลด ปัญหาการจัดการ และความสามารถในการเน่าเสีย</span><span class="sxs-lookup"><span data-stu-id="47b90-106">It enables transport companies to evaluate goods for shipment by classifying items based on considerations such as truck fit, loading issues, handling issues, and perishability.</span></span> <span data-ttu-id="47b90-107">ชุดสินค้าจะจัดกลุ่มเป็นคลาสค่าขนส่งคลาสหนึ่งจาก 18 ประเภทโดยใช้ช่วงตัวเลขตั้งแต่ 50 ถึง 500</span><span class="sxs-lookup"><span data-stu-id="47b90-107">Commodities are grouped into one of 18 freight classes by using a range of numbers from 50 to 500.</span></span> <span data-ttu-id="47b90-108">คลาสที่มีการจัดกลุ่มโภคภัณฑ์โดยยึดตามการประเมินลักษณะการขนส่งสี่อย่างคือ ความหนาแน่น การความสามารถในการดูแล การจัดการ และหนี้สิน</span><span class="sxs-lookup"><span data-stu-id="47b90-108">The class that a commodity is grouped into is based on an evaluation of four transportation characteristics: density, stowability, handling, and liability.</span></span> <span data-ttu-id="47b90-109">เมื่อรวมกันแล้ว ลักษณะเหล่านี้จะกําหนดความสามารถในการขนส่งของโภคภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="47b90-109">Together, these characteristics establish the commodity's transportability.</span></span>

<span data-ttu-id="47b90-110">รหัส NMFC จะเชื่อมโยงกับรายการจัดส่งสินค้าน้อยกว่าที่มีการบรรทุก (LTL) ทุกรายการ</span><span class="sxs-lookup"><span data-stu-id="47b90-110">An NMFC code is associated with every less than truckload (LTL) shipping item.</span></span> <span data-ttu-id="47b90-111">ตัวอย่างเช่น แล็ปท็อปอาจถูกมอบหมาย NMFC ที่มีคลาสอยู่ที่ 2.5 ในขณะที่สายไฟฟ้าอาจถูกมอบหมาย NMFC ที่มีคลาสที่ 65</span><span class="sxs-lookup"><span data-stu-id="47b90-111">For example, a laptop might be assigned an NMFC that is classed at 2.5, whereas electrical cords might be assigned an NMFC that is classed at 65.</span></span>

<span data-ttu-id="47b90-112">คุณลักษณะนี้สามารถช่วยให้ผู้ปฏิบัติงานใช้รหัส NMFC ในการจัดประเภทรายการจัดส่งสินค้า LTL</span><span class="sxs-lookup"><span data-stu-id="47b90-112">This feature can help workers use NMFC codes to classify LTL shipping items.</span></span> <span data-ttu-id="47b90-113">ยกตัวอย่างเช่น</span><span class="sxs-lookup"><span data-stu-id="47b90-113">Here are some examples:</span></span>

- <span data-ttu-id="47b90-114">หากบริษัทของคุณรวมรายละเอียดการขนส่งสินค้าในใบตราส่ง (BOL) บริษัทขนส่งจะมีแนวคิดว่าค่าขนส่งคือเท่าใด</span><span class="sxs-lookup"><span data-stu-id="47b90-114">If your company includes a freight description on the bill of lading (BOL), the carrier will have some idea what the freight is.</span></span> <span data-ttu-id="47b90-115">ค่าขนส่งเป็นการจัดประเภทที่สําคัญเนื่องจากบริษัทขนส่งส่วนใหญ่ใช้พื้นฐานรูปแบบธุรกิจของพวกเขาทั้งหมดบนชนิดการขนส่งที่พวกเขาจัดส่ง</span><span class="sxs-lookup"><span data-stu-id="47b90-115">Freight is an important classification because many transportation companies base their whole business model on the types of freight that they ship.</span></span>
- <span data-ttu-id="47b90-116">การจัดประเภทนี้อาจจําเป็นต่อบริษัทของคุณ เนื่องจากใช้เพื่อจํากัดต้นทุนของปริมาณงานในศูนย์การผลิตที่มอบ</span><span class="sxs-lookup"><span data-stu-id="47b90-116">This classification might be essential to your company because it's used to determine the cost of a given load.</span></span>
- <span data-ttu-id="47b90-117">บริษัทของคุณสามารถระบุความสามารถในการกําไรของลอจิสติกส์ LTL และบริษัทขนส่ง</span><span class="sxs-lookup"><span data-stu-id="47b90-117">Your company can identify the profitability of an LTL logistics and transportation company.</span></span>

<span data-ttu-id="47b90-118">หัวข้อนี้จะอธิบายวิธีการทำงานกับรหัส NMFC ใน Microsoft Dynamics 365 Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="47b90-118">This topic describes how to work with NMFC codes in Microsoft Dynamics 365 Supply Chain Management.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="47b90-119">ข้อกำหนดเบื้องต้น</span><span class="sxs-lookup"><span data-stu-id="47b90-119">Prerequisites</span></span>

<span data-ttu-id="47b90-120">ก่อนที่คุณจะสามารถสร้างรหัส NMFC คุณต้องตั้งค่าคลาสการขนส่ง LTL ทั้งหมดที่ต้องแม็ปกับรหัสการขนส่งเหล่านั้นก่อน</span><span class="sxs-lookup"><span data-stu-id="47b90-120">Before you can create NMFC codes, you must set up all the LTL freight classes that must be mapped to them.</span></span> <span data-ttu-id="47b90-121">คลาสการขนส่ง LTL แสดงถึงประเภทของรายการ ในขณะที่รหัส NMFC เกี่ยวข้องกับชุดสินค้าที่เฉพาะเจาะจงในแต่ละคลาสการขนส่ง 18 ประเภท</span><span class="sxs-lookup"><span data-stu-id="47b90-121">LTL freight classes represent categories of items, whereas NMFC codes are related to specific commodities in each of the 18 freight classes.</span></span> <span data-ttu-id="47b90-122">สำหรับข้อมูลเพิ่มเติมเกี่ยวกับวิธีใช้งานคลาส LTL โปรดดูที่ [คลาสน้อยกว่าที่มีการบรรทุก (LTL)](ltl-class.md)</span><span class="sxs-lookup"><span data-stu-id="47b90-122">For more information about how to work with LTL classes, see [Less than truckload (LTL) classes](ltl-class.md).</span></span>

## <a name="create-an-nmfc-code"></a><span data-ttu-id="47b90-123">สร้างรหัส NMFC</span><span class="sxs-lookup"><span data-stu-id="47b90-123">Create an NMFC code</span></span>

<span data-ttu-id="47b90-124">หากต้องการสร้างรหัส NMFC ทำตามขั้นตอนเหล่านี้</span><span class="sxs-lookup"><span data-stu-id="47b90-124">To create an NMFC code, follow these steps.</span></span>

1. <span data-ttu-id="47b90-125">ทำตามขั้นตอนเหล่านี้</span><span class="sxs-lookup"><span data-stu-id="47b90-125">Follow one of these steps:</span></span>

    - <span data-ttu-id="47b90-126">ไปที่ **การจัดการคลังสินค้า \> การตั้งค่า \> สินค้าคงคลัง \> รหัส NMFC**</span><span class="sxs-lookup"><span data-stu-id="47b90-126">Go to **Warehouse management \> Setup \> Inventory \> NMFC codes**.</span></span>
    - <span data-ttu-id="47b90-127">ไปที่ **การจัดการการขนส่ง \> การตั้งค่า \> มาตรฐานการขนส่ง \> รหัส NMFC**</span><span class="sxs-lookup"><span data-stu-id="47b90-127">Go to **Transportation management \> Setup \> Transportation standards \> NMFC codes**.</span></span>

1. <span data-ttu-id="47b90-128">เลือก **สร้าง** เพื่อสร้างรหัส NMFC</span><span class="sxs-lookup"><span data-stu-id="47b90-128">Select **New** to create an NMFC code.</span></span> <span data-ttu-id="47b90-129">จากนั้นตั้งค่าฟิลด์เหล่านี้:</span><span class="sxs-lookup"><span data-stu-id="47b90-129">Then set the following fields:</span></span>

    - <span data-ttu-id="47b90-130">**รหัส NMFC** – ป้อนรหัส NMFC สำหรับชนิดโภคภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="47b90-130">**NMFC code** – Enter the NMFC code for the commodity type.</span></span>
    - <span data-ttu-id="47b90-131">**ชื่อ** – ป้อนชื่อสำหรับรหัส NMFC</span><span class="sxs-lookup"><span data-stu-id="47b90-131">**Name** – Enter a name for the NMFC code.</span></span>
    - <span data-ttu-id="47b90-132">**คลาส LTL** – เลือกคลาส LTL ที่สัมพันธ์กับรหัส NMFC</span><span class="sxs-lookup"><span data-stu-id="47b90-132">**LTL class** – Select the LTL class that is associated with the NMFC code.</span></span>
    - <span data-ttu-id="47b90-133">**หน่วยจัดการวัสดุ BOL** – กําหนดชนิดการจัดการเริ่มต้นในการจัดส่งสินค้า</span><span class="sxs-lookup"><span data-stu-id="47b90-133">**BOL handling unit** – Define the default handling type for the shipment.</span></span>

## <a name="example-set-up-nmfc-codes"></a><span data-ttu-id="47b90-134">ตัวอย่าง: ตั้งค่ารหัส NMFC</span><span class="sxs-lookup"><span data-stu-id="47b90-134">Example: Set up NMFC codes</span></span>

<span data-ttu-id="47b90-135">ตัวอย่างต่อไปนี้แสดงวิธีการตั้งค่ารหัส NMFC สองรหัสที่แตกต่างกันซึ่งสามารถใช้กับผลิตภัณฑ์ที่แตกต่างกัน</span><span class="sxs-lookup"><span data-stu-id="47b90-135">The following example shows how to set up two different NMFC codes that can be used with different products.</span></span>

1. <span data-ttu-id="47b90-136">ไปที่ **การจัดการคลังสินค้า \> การตั้งค่า \> สินค้าคงคลัง \> รหัส NMFC**</span><span class="sxs-lookup"><span data-stu-id="47b90-136">Go to **Warehouse management \> Setup \> Inventory \> NMFC codes**.</span></span>
1. <span data-ttu-id="47b90-137">บนบานหน้าต่างการดำเนินการ เลือก **สร้าง**</span><span class="sxs-lookup"><span data-stu-id="47b90-137">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="47b90-138">บนบรรทัดใหม่ ให้ตั้งค่าค่าต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="47b90-138">On the new line, set the following values:</span></span>

    - <span data-ttu-id="47b90-139">**รหัส NMFC:** *92.5*</span><span class="sxs-lookup"><span data-stu-id="47b90-139">**NMFC code:** *92.5*</span></span>
    - <span data-ttu-id="47b90-140">**ชื่อ:** *คอมพิวเตอร์*</span><span class="sxs-lookup"><span data-stu-id="47b90-140">**Name:** *Computers*</span></span>
    - <span data-ttu-id="47b90-141">**คลาส LTL:** *92.5*</span><span class="sxs-lookup"><span data-stu-id="47b90-141">**LTL class:** *92.5*</span></span>
    - <span data-ttu-id="47b90-142">**หน่วยจัดการวัสดุ BOL:** *หน่วย*</span><span class="sxs-lookup"><span data-stu-id="47b90-142">**BOL handling unit:** *Unit*</span></span>

1. <span data-ttu-id="47b90-143">บนบานหน้าต่างการดำเนินการ เลือก **บันทึก**</span><span class="sxs-lookup"><span data-stu-id="47b90-143">On the Action Pane, select **Save**.</span></span>
1. <span data-ttu-id="47b90-144">บนบานหน้าต่างการดำเนินการ เลือก **สร้าง**</span><span class="sxs-lookup"><span data-stu-id="47b90-144">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="47b90-145">บนบรรทัดใหม่ ให้ตั้งค่าค่าต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="47b90-145">On the new line, set the following values:</span></span>

    - <span data-ttu-id="47b90-146">**รหัส NMFC:** *125*</span><span class="sxs-lookup"><span data-stu-id="47b90-146">**NMFC code:** *125*</span></span>
    - <span data-ttu-id="47b90-147">**ชื่อ:** *โทรศัพท์เคลื่อนที่*</span><span class="sxs-lookup"><span data-stu-id="47b90-147">**Name:** *Phones*</span></span>
    - <span data-ttu-id="47b90-148">**คลาส LTL:** *125*</span><span class="sxs-lookup"><span data-stu-id="47b90-148">**LTL class:** *125*</span></span>
    - <span data-ttu-id="47b90-149">**หน่วยจัดการวัสดุ BOL:** *หน่วย*</span><span class="sxs-lookup"><span data-stu-id="47b90-149">**BOL handling unit:** *Unit*</span></span>

1. <span data-ttu-id="47b90-150">บนบานหน้าต่างการดำเนินการ เลือก **บันทึก**</span><span class="sxs-lookup"><span data-stu-id="47b90-150">On the Action Pane, select **Save**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="47b90-151">ทรัพยากรเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="47b90-151">Additional resources</span></span>

- [<span data-ttu-id="47b90-152">ระดับชั้นการบรรทุกแบบไม่เต็มคันรถ (LTL)</span><span class="sxs-lookup"><span data-stu-id="47b90-152">Less than truckload (LTL) classes</span></span>](ltl-class.md)
- [<span data-ttu-id="47b90-153">สร้างใบตราส่ง</span><span class="sxs-lookup"><span data-stu-id="47b90-153">Create a bill of landing</span></span>](create-bill-of-lading.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
