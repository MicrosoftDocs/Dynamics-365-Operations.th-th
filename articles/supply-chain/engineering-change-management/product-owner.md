---
title: เจ้าของผลิตภัณฑ์
description: หัวข้อนี้มีข้อมูลเกี่ยวกับเจ้าของผลิตภัณฑ์ เจ้าของผลิตภัณฑ์คือกลุ่มของผู้ใช้ที่รับผิดชอบผลิตภัณฑ์เฉพาะ เฉพาะสมาชิกของกลุ่มเท่านั้นที่สามารถนำผลิตภัณฑ์ดังกล่าวไปใช้ได้ เจ้าของผลิตภัณฑ์สามารถใช้ในลำดับงานการอนุมัติได้ด้วย
author: t-benebo
manager: tfehr
ms.date: 09/28/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EngChgProductOwner
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2020-09-28
ms.dyn365.ops.version: Release 10.0.15
ms.openlocfilehash: 4308020d66995d857e547be47216cb82caacf035
ms.sourcegitcommit: 5f21cfde36c43887ec209bba4a12b830a1746fcf
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 10/29/2020
ms.locfileid: "4438932"
---
# <a name="product-owners"></a><span data-ttu-id="aa286-106">เจ้าของผลิตภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="aa286-106">Product owners</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="aa286-107">เจ้าของผลิตภัณฑ์คือกลุ่มของผู้ใช้ที่รับผิดชอบผลิตภัณฑ์เฉพาะ</span><span class="sxs-lookup"><span data-stu-id="aa286-107">The product owner is a group of users who are responsible for specific products.</span></span> <span data-ttu-id="aa286-108">เมื่อมีการกำหนดกลุ่มเจ้าของผลิตภัณฑ์ให้กับผลิตภัณฑ์ เฉพาะสมาชิกของกลุ่มนั้นเท่านั้นที่สามารถนำผลิตภัณฑ์ออกใช้ได้</span><span class="sxs-lookup"><span data-stu-id="aa286-108">When a product owner group is assigned to a product, only the members of that group can release the product.</span></span> <span data-ttu-id="aa286-109">เจ้าของผลิตภัณฑ์สามารถใช้ในลำดับงานการอนุมัติได้ในการจัดการการเปลี่ยนแปลงวิศวกรรม</span><span class="sxs-lookup"><span data-stu-id="aa286-109">The product owner can also be used in the approval workflow in engineering change management.</span></span>

<span data-ttu-id="aa286-110">เจ้าของผลิตภัณฑ์คือการตั้งค่าแบบครอบคลุม</span><span class="sxs-lookup"><span data-stu-id="aa286-110">Product owners are global settings.</span></span> <span data-ttu-id="aa286-111">ดังนั้น จึงจะพร้อมใช้งานสำหรับนิติบุคคลทั้งหมด</span><span class="sxs-lookup"><span data-stu-id="aa286-111">Therefore, they are available to all legal entities.</span></span>

## <a name="create-a-product-owner-group"></a><span data-ttu-id="aa286-112">สร้างกลุ่มเจ้าของผลิตภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="aa286-112">Create a product owner group</span></span>

<span data-ttu-id="aa286-113">เมื่อต้องการสร้างกลุ่มเจ้าของผลิตภัณฑ์และเพิ่มสมาชิก ให้ทำตามขั้นตอนต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="aa286-113">To create a product owner group and add members to it, follow these steps.</span></span>

1. <span data-ttu-id="aa286-114">ไปที่ **การจัดการการเปลี่ยนแปลงวิศวกรรม \> การตั้งค่า \> เจ้าของผลิตภัณฑ์**</span><span class="sxs-lookup"><span data-stu-id="aa286-114">Go to **Engineering change management \> Setup \> Product owners**.</span></span>
2. <span data-ttu-id="aa286-115">บนบานหน้าต่างการดำเนินการ เลือก **สร้าง**</span><span class="sxs-lookup"><span data-stu-id="aa286-115">On the Action Pane, select **New**.</span></span>
3. <span data-ttu-id="aa286-116">ในฟิลด์ **เจ้าของผลิตภัณฑ์** ให้ป้อนชื่อสำหรับกลุ่ม</span><span class="sxs-lookup"><span data-stu-id="aa286-116">In the **Product owner** field, enter a name for the group.</span></span>
4. <span data-ttu-id="aa286-117">ในฟิลด์  **ชื่อ** ให้ป้อนคำอธิบายโดยย่อของกลุ่ม</span><span class="sxs-lookup"><span data-stu-id="aa286-117">In the **Name** field, enter a description of the group.</span></span>
5. <span data-ttu-id="aa286-118">บนแท็บด่วน **สมาชิก** ให้เพิ่มผู้ปฏิบัติงานที่ควรเป็นสมาชิกของกลุ่ม</span><span class="sxs-lookup"><span data-stu-id="aa286-118">On the **Members** FastTab, add the workers who should be members of the group.</span></span>

## <a name="assign-a-product-owner-to-a-product"></a><span data-ttu-id="aa286-119">กำหนดสเจ้าของผลิตภัณฑ์ให้กับผลิตภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="aa286-119">Assign a product owner to a product</span></span>

<span data-ttu-id="aa286-120">ในการกำหนดเจ้าของผลิตภัณฑ์ให้กับผลิตภัณฑ์ ให้ทำตามขั้นตอนเหล่านี้</span><span class="sxs-lookup"><span data-stu-id="aa286-120">To assign a product owner to a product, follow these steps.</span></span>

1. <span data-ttu-id="aa286-121">เปิดหน้า **รายละเอียดของผลิตภัณฑ์** สำหรับผลิตภัณฑ์หลักหรือผลิตภัณฑ์หลักที่เกี่ยวข้อง</span><span class="sxs-lookup"><span data-stu-id="aa286-121">Open the **Product details** page for the relevant product or product master.</span></span>
1. <span data-ttu-id="aa286-122">บนแท็บด่วน **ทั่วไป** ให้ตั้งค่าฟิลด์ **เจ้าของผลิตภัณฑ์** เป็นชื่อของกลุ่มเจ้าของผลิตภัณฑ์ที่เกี่ยวข้อง</span><span class="sxs-lookup"><span data-stu-id="aa286-122">On the **General** FastTab, set the **Product owner** field to the name of the relevant product owner group.</span></span>

<span data-ttu-id="aa286-123">ในขณะที่เจ้าของผลิตภัณฑ์ได้รับการกำหนดให้กับผลิตภัณฑ์ เฉพาะสมาชิกของกลุ่มเจ้าของผลิตภัณฑ์เท่านั้นที่สามารถแก้ไขการตั้งค่า **เจ้าของผลิตภัณฑ์** ได้</span><span class="sxs-lookup"><span data-stu-id="aa286-123">While a product owner is assigned to a product, only the members of the product owner group can edit the **Product owner** setting.</span></span>

<span data-ttu-id="aa286-124">เจ้าของผลิตภัณฑ์ยังมองเห็นได้บนหน้า **ผลิตภัณฑ์ที่นำออกใช้**</span><span class="sxs-lookup"><span data-stu-id="aa286-124">The product owner is also visible on the **Released products** page.</span></span>

## <a name="product-owners-and-product-releases"></a><span data-ttu-id="aa286-125">เจ้าของผลิตภัณฑ์และผลิตภัณฑ์ที่นำออกใช้</span><span class="sxs-lookup"><span data-stu-id="aa286-125">Product owners and product releases</span></span>

<span data-ttu-id="aa286-126">เฉพาะผู้ใช้จากกลุ่มเจ้าของผลิตภัณฑ์ของผลิตภัณฑ์เท่านั้นที่สามารถนำผลิตภัณฑ์ดังกล่าวไปใช้ได้</span><span class="sxs-lookup"><span data-stu-id="aa286-126">Only users from a product's product owner group can release that product.</span></span> <span data-ttu-id="aa286-127">อย่างไรก็ตาม มีข้อยกเว้นเมื่อผลิตภัณฑ์เป็นสินค้ารอง และข้อมูลหลักของผู้ใช้จะถูกนำออกใช้โดยเจ้าของหลัก</span><span class="sxs-lookup"><span data-stu-id="aa286-127">However, there is an exception when the product is a child item, and its parent is released by the parent's owner.</span></span> <span data-ttu-id="aa286-128">กล่าวอีกอย่างหนึ่งคือ ถ้าผลิตภัณฑ์เป็นส่วนหนึ่งของ BOM ของผลิตภัณฑ์อื่น ระบบจะไม่ตรวจสอบเจ้าของผลิตภัณฑ์ของสินค้าแต่ละรายการใน BOM</span><span class="sxs-lookup"><span data-stu-id="aa286-128">In other words, if the product is part of the BOM of another product, the system doesn't check the product owner of each item in the BOM.</span></span> <span data-ttu-id="aa286-129">โดยจะตรวจสอบเฉพาะเจ้าของผลิตภัณฑ์ของสินค้าหลักเท่านั้น</span><span class="sxs-lookup"><span data-stu-id="aa286-129">It checks only the product owner of the parent item.</span></span>

<span data-ttu-id="aa286-130">ตัวอย่างเช่น มีการกำหนดผลิตภัณฑ์ X ให้กับกลุ่มเจ้าของผลิตภัณฑ์ *การออกแบบตู้*</span><span class="sxs-lookup"><span data-stu-id="aa286-130">For example, product X is assigned to the *Design cabinets* product owner group.</span></span> <span data-ttu-id="aa286-131">ผลิตภัณฑ์ X ยังเป็นส่วนหนึ่งของ BOM ของผลิตภัณฑ์ Y ซึ่งกำหนดให้กับกลุ่มเจ้าของผลิตภัณฑ์ *ออกแบบลำโพง*</span><span class="sxs-lookup"><span data-stu-id="aa286-131">Product X is also part of the BOM of product Y, which is assigned to the *Design Speakers* product owner group.</span></span> <span data-ttu-id="aa286-132">ถ้าผู้ใช้จากกลุ่มเจ้าของผลิตภัณฑ์ *ออกแบบลำโพง* นำออกใช้ผลิตภัณฑ์ Y และ BOM ผลิตภัณฑ์ X จะถูกนำออกใช้ร่วมกับผลิตภัณฑ์ Y</span><span class="sxs-lookup"><span data-stu-id="aa286-132">If a user from the *Design Speakers* product owner group releases product Y and its BOM, product X will be released together with product Y.</span></span>

## <a name="product-owners-and-approvals"></a><span data-ttu-id="aa286-133">เจ้าของผลิตภัณฑ์และการอนุมัติ</span><span class="sxs-lookup"><span data-stu-id="aa286-133">Product owners and approvals</span></span>

<span data-ttu-id="aa286-134">เนื่องจากเจ้าของผลิตภัณฑ์ทราบว่าการเปลี่ยนแปลงทางวิศวกรรมเฉพาะจะเป็นประโยชน์กับผลิตภัณฑ์ของตนบ่อยเพียงใด จึงทำให้เกิดความรู้สึกเพื่อรวมไว้เป็นส่วนหนึ่งของกระบวนการอนุมัติในการจัดการการเปลี่ยนแปลงทางวิศวกรรม</span><span class="sxs-lookup"><span data-stu-id="aa286-134">Because product owners know whether specific engineering changes will benefit their products, it often makes sense to include them as part of the approval process in engineering change management.</span></span> <span data-ttu-id="aa286-135">คุณสามารถใช้วิธีการนี้ได้โดยการตั้งค่าเจ้าของผลิตภัณฑ์เป็นผู้ให้บริการเข้าร่วมในลำดับงานที่ใช้สำหรับการจัดการการเปลี่ยนแปลงทางวิศวกรรม</span><span class="sxs-lookup"><span data-stu-id="aa286-135">You can implement this approach by setting up the product owners as participant providers in the workflows that are used for engineering change management.</span></span> <span data-ttu-id="aa286-136">ระบบจะกำหนดงานการอนุมัติในลำดับงานโดยยึด ตามผลิตภัณฑ์ที่อยู่ในคำขอเปลี่ยนแปลงทางวิศวกรรมและใบสั่งเปลี่ยนแปลงทางวิศวกรรม</span><span class="sxs-lookup"><span data-stu-id="aa286-136">The system will then assign approval tasks in the workflows, based on the products that are in engineering change requests and engineering change orders.</span></span> <span data-ttu-id="aa286-137">สำหรับข้อมูลเพิ่มเติม ให้ดูที่ [จัดการการเปลี่ยนแปลงที่เกิดขึ้นกับผลิตภัณฑ์วิศวกรรม](engineering-change-management.md)</span><span class="sxs-lookup"><span data-stu-id="aa286-137">For more information, see [Manage changes to engineering products](engineering-change-management.md).</span></span>
