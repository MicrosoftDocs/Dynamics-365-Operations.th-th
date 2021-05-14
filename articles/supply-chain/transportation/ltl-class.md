---
title: ระดับชั้นการบรรทุกแบบไม่เต็มคันรถ (LTL)
description: หัวข้อนี้อธิบายว่าคลาสอะไรน้อยกว่าคลาส truckload (LTL) และอธิบายวิธีการตั้งค่าใน Microsoft Dynamics 365 Supply Chain Management
author: Henrikan
ms.date: 04/05/2021
ms.topic: article
ms.search.form: WHSLTLClass
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: henrikan
ms.search.validFrom: 2021-04-05
ms.dyn365.ops.version: 10.0.8
ms.openlocfilehash: 295006cac0a67cd577809a1b62566de043ea55fb
ms.sourcegitcommit: 636c1bf096a8666a551b67e898da1f48feb9a187
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 04/26/2021
ms.locfileid: "5941821"
---
# <a name="less-than-truckload-ltl-classes"></a><span data-ttu-id="13fcc-103">ระดับชั้นการบรรทุกแบบไม่เต็มคันรถ (LTL)</span><span class="sxs-lookup"><span data-stu-id="13fcc-103">Less than truckload (LTL) classes</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="13fcc-104">คลาสน้อยกว่าที่มีการบรรทุก (LTL) เป็นคลาสการจัดส่งการขนส่งที่ใช้จัดประเภทสินค้าที่สามารถจัดส่งได้</span><span class="sxs-lookup"><span data-stu-id="13fcc-104">A less than truckload (LTL) class is a freight shipping class that is used to classify items that can be shipped.</span></span> <span data-ttu-id="13fcc-105">โดยทั่วไปแล้ว ผลิตภัณฑ์หรือโภคภัณฑ์ทุกชนิดจะมีรหัสการจัดประเภทการขนส่งด้วยรถยนต์ระดับชาติ (NMFC) ที่สอดคล้องกับหมายเลขคลาสการขนส่งเฉพาะของการจัดส่ง LTL</span><span class="sxs-lookup"><span data-stu-id="13fcc-105">Generally, every type of product or commodity has a National Motor Freight Classification (NMFC) code that corresponds to a specific freight class number for LTL shipments.</span></span> <span data-ttu-id="13fcc-106">คลาสการขนส่ง LTL แสดงถึงประเภทของรายการ ในขณะที่รหัส NMFC เกี่ยวข้องกับชุดสินค้าที่เฉพาะเจาะจงในแต่ละคลาสการขนส่ง 18 ประเภท</span><span class="sxs-lookup"><span data-stu-id="13fcc-106">LTL freight classes represent categories of items, whereas NMFC codes are related to specific commodities in each of the 18 freight classes.</span></span>

<span data-ttu-id="13fcc-107">คุณลักษณะนี้ช่วยให้คุณสามารถใช้ระบบของคุณเพื่อดำเนินงานต่อไปนี้ได้:</span><span class="sxs-lookup"><span data-stu-id="13fcc-107">This feature lets you use your system to perform the following tasks:</span></span>

- <span data-ttu-id="13fcc-108">กําหนดคลาสการขนส่ง LTL ที่ใช้ในบริษัทของคุณ</span><span class="sxs-lookup"><span data-stu-id="13fcc-108">Define the LTL freight classes that are used at your company.</span></span>
- <span data-ttu-id="13fcc-109">กําหนดคลาส LTL แต่ละคลาสให้กับรหัส NMFC ในหน้า **รหัส NMFC**</span><span class="sxs-lookup"><span data-stu-id="13fcc-109">Assign each LTL class to an NMFC code on the **NMFC Codes** page.</span></span> <span data-ttu-id="13fcc-110">สำหรับข้อมูลเพิ่มเติม ดูที่ [รหัสการจัดประเภทการขนส่งด้วยรถยนต์ระดับชาติ (NMFC)](nmfc-codes.md)</span><span class="sxs-lookup"><span data-stu-id="13fcc-110">For more information, see [National Motor Freight Classification (NMFC) codes](nmfc-codes.md).</span></span>
- <span data-ttu-id="13fcc-111">กําหนดรหัส NMFC (ดังนั้นจึงมีรหัส LTL ที่เชื่อมโยง) ให้กับผลิตภัณฑ์แต่ละรายการในหน้า **ผลิตภัณฑ์**</span><span class="sxs-lookup"><span data-stu-id="13fcc-111">Assign an NMFC code (and therefore its associated LTL code) to each product on the **Products** page.</span></span>
- <span data-ttu-id="13fcc-112">ประเมินคลาส LTL ของแต่ละผลิตภัณฑ์ที่การมอบหมายรหัส NMFC ให้ถูกต้อง</span><span class="sxs-lookup"><span data-stu-id="13fcc-112">Accurately assess the LTL class of each product that an NMFC code is assigned to.</span></span>
- <span data-ttu-id="13fcc-113">กําหนดข้อกําหนดการบรรจุของแต่ละคลาส LTL โดยการตรวจสอบมาตรฐาน LTL ระหว่างประเทศ</span><span class="sxs-lookup"><span data-stu-id="13fcc-113">Determine packing requirements for each LTL class by checking the international LTL standards.</span></span> <span data-ttu-id="13fcc-114">ด้วยวิธีนี้ คุณจึงมั่นใจว่าผลิตภัณฑ์ของคุณจะได้รับการป้องกันและจัดส่งอย่างปลอดภัย</span><span class="sxs-lookup"><span data-stu-id="13fcc-114">In this way, you ensure that your products will be well protected and safely shipped.</span></span>
- <span data-ttu-id="13fcc-115">ได้รับการประเมินการจัดส่งที่ถูกต้องตามคลาสการขนส่ง LTL ของแต่ละผลิตภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="13fcc-115">Get accurate shipping estimates, based on the LTL freight class for each product.</span></span>

<span data-ttu-id="13fcc-116">หัวข้อนี้จะอธิบายวิธีการสร้างคลาส LTL ใน Microsoft Dynamics 365 Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="13fcc-116">This topic describes how to create LTL classes in Microsoft Dynamics 365 Supply Chain Management.</span></span>

## <a name="create-an-ltl-class"></a><span data-ttu-id="13fcc-117">สร้างคลาส LTL</span><span class="sxs-lookup"><span data-stu-id="13fcc-117">Create an LTL class</span></span>

<span data-ttu-id="13fcc-118">หากต้องการสร้างคลาส LTL ทำตามขั้นตอนเหล่านี้</span><span class="sxs-lookup"><span data-stu-id="13fcc-118">To create an LTL class, follow these steps.</span></span>

1. <span data-ttu-id="13fcc-119">ทำตามขั้นตอนเหล่านี้</span><span class="sxs-lookup"><span data-stu-id="13fcc-119">Follow one of these steps:</span></span>

    - <span data-ttu-id="13fcc-120">ไปที่ **การจัดการคลังสินค้า \> การตั้งค่า \> สินค้าคงคลัง \> คลาส LTL**</span><span class="sxs-lookup"><span data-stu-id="13fcc-120">Go to **Warehouse management \> Setup \> Inventory \> LTL classes**.</span></span>
    - <span data-ttu-id="13fcc-121">ไปที่ **การจัดการการขนส่ง \> การตั้งค่า \> มาตรฐานการขนส่ง \> คลาส LTL**</span><span class="sxs-lookup"><span data-stu-id="13fcc-121">Go to **Transportation management \> Setup \> Transportation standards \> LTL classes**.</span></span>

2. <span data-ttu-id="13fcc-122">ในบานหน้าต่างการดำเนินการ เลือก **สร้าง** เพื่อสร้างคลาส LTL</span><span class="sxs-lookup"><span data-stu-id="13fcc-122">On the Action Pane, select **New** to create an LTL class.</span></span> <span data-ttu-id="13fcc-123">จากนั้นตั้งค่าฟิลด์เหล่านี้:</span><span class="sxs-lookup"><span data-stu-id="13fcc-123">Then set the following fields:</span></span>

    - <span data-ttu-id="13fcc-124">**คลาส LTL** – ป้อนรหัสคลาส LTL ภายในของบริษัทของคุณ (รหัส) ของชนิดโภคภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="13fcc-124">**LTL class** – Enter your company's internal LTL class identifier (ID) for the commodity type.</span></span> <span data-ttu-id="13fcc-125">บริษัทส่วนใหญ่ใช้มาตรฐานสากล</span><span class="sxs-lookup"><span data-stu-id="13fcc-125">Most companies use the international standard.</span></span> <span data-ttu-id="13fcc-126">ในกรณีดังกล่าว ค่าของฟิลด์นี้จะตรงกับค่าของฟิลด์ **คลาส**</span><span class="sxs-lookup"><span data-stu-id="13fcc-126">In that case, the value of this field will match the value of the **Class** field.</span></span> <span data-ttu-id="13fcc-127">อย่างไรก็ตาม ถ้าบริษัทของคุณใช้มาตรฐานของบริษัทเอง ให้ป้อนรหัสที่สอดคล้องกับมาตรฐานนั้น</span><span class="sxs-lookup"><span data-stu-id="13fcc-127">However, if your company uses its own standard, enter a code that conforms to that standard.</span></span>
    - <span data-ttu-id="13fcc-128">**ชื่อ** – ป้อนชื่อที่เป็นอธิบายที่จะช่วยคุณและผู้ใช้อื่น ๆ เลือกคลาส LTL ที่ถูกต้องของรหัส NMFC แต่ละรหัส</span><span class="sxs-lookup"><span data-stu-id="13fcc-128">**Name** – Enter a descriptive name that will help you and other users select the correct LTL class for each NMFC code.</span></span>
    - <span data-ttu-id="13fcc-129">**คลาส** – ป้อนรหัสคลาส LTL มาตรฐานสากลของชนิดโภคภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="13fcc-129">**Class** – Enter the international standard LTL class ID for the commodity type.</span></span> <span data-ttu-id="13fcc-130">รหัสที่คุณป้อนที่นี่ต้องเป็นไปตามมาตรฐานที่เป็นทางการ</span><span class="sxs-lookup"><span data-stu-id="13fcc-130">The code that you enter here must conform to the official standard.</span></span>

## <a name="example-set-up-ltl-classes"></a><span data-ttu-id="13fcc-131">ตัวอย่าง: ตั้งค่าคลาส LTL</span><span class="sxs-lookup"><span data-stu-id="13fcc-131">Example: Set up LTL classes</span></span>

<span data-ttu-id="13fcc-132">ตัวอย่างต่อไปนี้แสดงวิธีการตั้งค่าคลาส LTL สองรหัสที่แตกต่างกันที่คุณสามารถใช้กับชนิดผลิตภัณฑ์ที่แตกต่างกันได้</span><span class="sxs-lookup"><span data-stu-id="13fcc-132">The following example shows how to set up two different LTL classes that you can use with different types of products.</span></span>

1. <span data-ttu-id="13fcc-133">ไปที่ **การจัดการคลังสินค้า \> การตั้งค่า \> สินค้าคงคลัง \> คลาส LTL**</span><span class="sxs-lookup"><span data-stu-id="13fcc-133">Go to **Warehouse management \> Setup \> Inventory \> LTL classes**.</span></span>
1. <span data-ttu-id="13fcc-134">บนบานหน้าต่างการดำเนินการ เลือก **สร้าง**</span><span class="sxs-lookup"><span data-stu-id="13fcc-134">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="13fcc-135">บนบรรทัดใหม่ ให้ตั้งค่าค่าต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="13fcc-135">On the new line, set the following values:</span></span>

    - <span data-ttu-id="13fcc-136">**คลาส LTL:** *92.5*</span><span class="sxs-lookup"><span data-stu-id="13fcc-136">**LTL class:** *92.5*</span></span>
    - <span data-ttu-id="13fcc-137">**ชื่อ:** *คอมพิวเตอร์ หน้าจอ ตู้เย็น*</span><span class="sxs-lookup"><span data-stu-id="13fcc-137">**Name:** *Computers, monitors, refrigerators*</span></span>
    - <span data-ttu-id="13fcc-138">**คลาส:** *92.5*</span><span class="sxs-lookup"><span data-stu-id="13fcc-138">**Class:** *92.5*</span></span>

1. <span data-ttu-id="13fcc-139">บนบานหน้าต่างการดำเนินการ เลือก **บันทึก**</span><span class="sxs-lookup"><span data-stu-id="13fcc-139">On the Action Pane, select **Save**.</span></span>
1. <span data-ttu-id="13fcc-140">บนบานหน้าต่างการดำเนินการ เลือก **สร้าง**</span><span class="sxs-lookup"><span data-stu-id="13fcc-140">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="13fcc-141">บนบรรทัดใหม่ ให้ตั้งค่าค่าต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="13fcc-141">On the new line, set the following values:</span></span>

    - <span data-ttu-id="13fcc-142">**คลาส LTL:** *125*</span><span class="sxs-lookup"><span data-stu-id="13fcc-142">**LTL class:** *125*</span></span>
    - <span data-ttu-id="13fcc-143">**ชื่อ:** *เครื่องมือเครื่องใช้ในบ้านขนาดเล็ก*</span><span class="sxs-lookup"><span data-stu-id="13fcc-143">**Name:** *Small household appliances*</span></span>
    - <span data-ttu-id="13fcc-144">**คลาส:** *125*</span><span class="sxs-lookup"><span data-stu-id="13fcc-144">**Class:** *125*</span></span>

1. <span data-ttu-id="13fcc-145">บนบานหน้าต่างการดำเนินการ เลือก **บันทึก**</span><span class="sxs-lookup"><span data-stu-id="13fcc-145">On the Action Pane, select **Save**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="13fcc-146">ทรัพยากรเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="13fcc-146">Additional resources</span></span>

- [<span data-ttu-id="13fcc-147">รหัสการจัดประเภทการขนส่งด้วยรถยนต์ระดับชาติ (NMFC)</span><span class="sxs-lookup"><span data-stu-id="13fcc-147">National Motor Freight Classification (NMFC) codes</span></span>](nmfc-codes.md)
- [<span data-ttu-id="13fcc-148">สร้างใบตราส่ง</span><span class="sxs-lookup"><span data-stu-id="13fcc-148">Create a bill of lading</span></span>](create-bill-of-lading.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
