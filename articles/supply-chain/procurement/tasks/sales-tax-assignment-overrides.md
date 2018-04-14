--- 
title: "การกำหนดและการแทนที่ภาษีขาย"
description: "ขั้นตอนนี้อธิบายวิธีการกำหนดกลุ่มภาษีขายตามช่องทางการขายปลีก "
author: mkirknel
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: bis
ms.search.scope: Operations
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: 8b3dc0beec17d80f7bbbcf234656a537a445789f
ms.contentlocale: th-th
ms.lasthandoff: 04/13/2018

---
# <a name="sales-tax-assignment-and-overrides"></a><span data-ttu-id="b8218-103">การกำหนดและการแทนที่ภาษีขาย</span><span class="sxs-lookup"><span data-stu-id="b8218-103">Sales tax assignment and overrides</span></span>

[!INCLUDE [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="b8218-104">ขั้นตอนนี้อธิบายวิธีการกำหนดกลุ่มภาษีขายตามช่องทางการขายปลีก </span><span class="sxs-lookup"><span data-stu-id="b8218-104">This procedure demonstrates how to assign sales tax groups to retail channels.</span></span> <span data-ttu-id="b8218-105">และยังแนะนำขั้นตอนการสร้างการแทนที่ภาษีขายใหม่ และการกำหนดให้กับกลุ่มแทนที่ภาษีขายที่มีอยู่ </span><span class="sxs-lookup"><span data-stu-id="b8218-105">It also walks through the process of creating a new sales tax override and assigning it to an existing sales tax override group.</span></span> <span data-ttu-id="b8218-106">กระบวนงานนี้</span><span class="sxs-lookup"><span data-stu-id="b8218-106">This procedure</span></span>

<span data-ttu-id="b8218-107">ใช้บริษัท USRT ในข้อมูลสาธิต</span><span class="sxs-lookup"><span data-stu-id="b8218-107">uses the USRT company in demo data.</span></span>

1. <span data-ttu-id="b8218-108">ไปยังการขายปลีกและการค้า > ช่องทาง > ร้านค้าปลีก > ร้านค้าปลีกทั้งหมด</span><span class="sxs-lookup"><span data-stu-id="b8218-108">Go to Retail and commerce > Channels > Retail stores > All retail stores.</span></span>
2. <span data-ttu-id="b8218-109">ในรายการ ให้คลิกลิงค์รหัสช่องทางการขายปลีกสำหรับ "Houston"</span><span class="sxs-lookup"><span data-stu-id="b8218-109">In the list, click the Retail Channel ID link for "Houston."</span></span>
3. <span data-ttu-id="b8218-110">คลิก แก้ไข</span><span class="sxs-lookup"><span data-stu-id="b8218-110">Click Edit.</span></span>
    * <span data-ttu-id="b8218-111">ฟิลด์ "กลุ่มภาษีขาย" ประกอบด้วยรายการของกลุ่มภาษีขายสำหรับบริษัทปัจจุบัน </span><span class="sxs-lookup"><span data-stu-id="b8218-111">The "Sales tax group" field contains the list of sales tax groups for the current company.</span></span> <span data-ttu-id="b8218-112">กลุ่มที่กำหนดไว้ในปัจจุบันเป็นกลุ่มภาษีขายสำหรับ "Texas" ทั่วไป </span><span class="sxs-lookup"><span data-stu-id="b8218-112">The currently assigned group is a generic "Texas" sales tax group.</span></span> <span data-ttu-id="b8218-113">จากนั้นยังมีกลุ่มภาษีขายสำหรับ "Washington" และ "Washington, King County" </span><span class="sxs-lookup"><span data-stu-id="b8218-113">There are also sales tax groups for "Washington" and "Washington, King County."</span></span> <span data-ttu-id="b8218-114">กลุ่มภาษีขายอาจรวมภาษีที่เกี่ยวข้องสำหรับหลายอำเภอ</span><span class="sxs-lookup"><span data-stu-id="b8218-114">Sales tax groups can include applicable taxes for multiple municipalities.</span></span>  
    * <span data-ttu-id="b8218-115">ฟิลด์ "การแทนที่ภาษีขาย" คือตำแหน่งที่กลุ่มแทนที่ภาษีขายสามารถแม็ปไปยังช่องทาง </span><span class="sxs-lookup"><span data-stu-id="b8218-115">The "Sales tax override" field is where sales tax override groups can be mapped to the channel.</span></span> <span data-ttu-id="b8218-116">สามารถใช้กลุ่มแทนภาษีขายในการจัดกลุ่มการแทนที่ภาษีขายที่ทำงานสำหรับหลายร้านค้าไว้ด้วยกัน </span><span class="sxs-lookup"><span data-stu-id="b8218-116">Sales tax override groups can be used to group together sales tax overrides that work for multiple stores.</span></span> <span data-ttu-id="b8218-117">แทนการกำหนดการแทนที่ภาษีขายด้วยตนเองทีละรายการ สามารถสร้างและกำหนดกลุ่มให้กับช่องทางโดยตรงเพื่อประหยัดเวลา</span><span class="sxs-lookup"><span data-stu-id="b8218-117">Rather than manually assigning sales tax overrides one by one, the group can be created and assigned directly to the channels to save time.</span></span>  
4. <span data-ttu-id="b8218-118">คลิก บันทึก</span><span class="sxs-lookup"><span data-stu-id="b8218-118">Click Save.</span></span>
5. <span data-ttu-id="b8218-119">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="b8218-119">Close the page.</span></span>
6. <span data-ttu-id="b8218-120">ไปที่ การขายปลีกและการค้า > การตั้งค่าช่องทาง > ภาษีขาย > การแทนที่ภาษีขาย</span><span class="sxs-lookup"><span data-stu-id="b8218-120">Go to Retail and commerce > Channel setup > Sales taxes > Sales tax overrides.</span></span>
7. <span data-ttu-id="b8218-121">คลิก สร้าง</span><span class="sxs-lookup"><span data-stu-id="b8218-121">Click New.</span></span>
8. <span data-ttu-id="b8218-122">ในฟิลด์การแทนที่ภาษีขาย ให้ป้อนชื่อสำหรับการแทนที่ใหม่ของคุณ</span><span class="sxs-lookup"><span data-stu-id="b8218-122">In the Sales tax override field, provide a name for your new override.</span></span>
9. <span data-ttu-id="b8218-123">ในฟิลด์คำอธิบาย ป้อนคำอธิบายของการแทนที่</span><span class="sxs-lookup"><span data-stu-id="b8218-123">In the Description field, provide a description of the override.</span></span>
10. <span data-ttu-id="b8218-124">ตั้งค่าสถานะเป็น "เปิดใช้งาน"</span><span class="sxs-lookup"><span data-stu-id="b8218-124">Set the status to "Enable."</span></span>
11. <span data-ttu-id="b8218-125">ขยายหรือยุบส่วนการแทนที่</span><span class="sxs-lookup"><span data-stu-id="b8218-125">Expand or collapse the Override section.</span></span>
12. <span data-ttu-id="b8218-126">ในฟิลด์ชนิด ให้เลือกหนึ่งตัวเลือก</span><span class="sxs-lookup"><span data-stu-id="b8218-126">In the Type field, select an option.</span></span>
    * <span data-ttu-id="b8218-127">สามารถใช้กลุ่มภาษีขายตามประเภทสินค้าแทนภาษีสำหรับสินค้าเฉพาะที่อยู่ในกลุ่มนั้นได้ </span><span class="sxs-lookup"><span data-stu-id="b8218-127">Item sales tax groups can be used to override taxes for specific items that belong to the group.</span></span> <span data-ttu-id="b8218-128">ตัวอย่างเช่น โดยทั่วไปสินค้าอาหารจะคิดภาษีแตกต่างจากครุภัณฑ์ และอาจจะมีกลุ่มภาษีขายของตนเอง </span><span class="sxs-lookup"><span data-stu-id="b8218-128">For example, food items are typically taxed differently from hard goods, and would likely have their own sales tax group.</span></span>     <span data-ttu-id="b8218-129">กลุ่มภาษีขายคือ กลุ่มของภาษีที่สามารถใช้ได้กับช่องทางเฉพาะ </span><span class="sxs-lookup"><span data-stu-id="b8218-129">Sales tax groups are groups of taxes that are applicable to a particular channel.</span></span> <span data-ttu-id="b8218-130">ตัวอย่างเช่น ถ้าช่องทางนั้น ๆ ทั้งขายปลีกและรวมระหว่างธุรกิจ กลุ่มภาษีขายตามประเภทสินค้าที่แตกต่างกันอาจถูกนำมาใช้ได้ </span><span class="sxs-lookup"><span data-stu-id="b8218-130">For example, if a channel sells both retail and business-to-business, different items sales tax groups may be used.</span></span> <span data-ttu-id="b8218-131">ภาษีที่เกี่ยวข้องทั้งหมดจะถูกแมปเข้ากับกลุ่มภาษีขาย</span><span class="sxs-lookup"><span data-stu-id="b8218-131">All the applicable taxes would be mapped to the sales tax group.</span></span>  
    * <span data-ttu-id="b8218-132">ขณะนี้คุณสามารถเลือก "เริ่มต้น" และ "สิ้นสุด" ภาษี หรือ "จากกลุ่มภาษี" และ "เป็นกลุ่มภาษี" เพื่อสร้างการแทนที่ภาษีขายของคุณ </span><span class="sxs-lookup"><span data-stu-id="b8218-132">Now you can select the "From" and "To" taxes or "From tax group" and "To tax group" to create your sales tax override.</span></span>    <span data-ttu-id="b8218-133">ฟิลด์ "เริ่มต้น" บ่งชี้ภาษีหรือกลุ่มภาษีที่จะถูกแทนที่ </span><span class="sxs-lookup"><span data-stu-id="b8218-133">The "From" field indicates the tax or tax group to be overridden.</span></span> <span data-ttu-id="b8218-134">การแทนที่ด้วยกลุ่มภาษีขายสินค้ามีตัวเลือกต่าง ๆ มากกว่าการแทนที่ด้วยกลุ่มภาษีขาย </span><span class="sxs-lookup"><span data-stu-id="b8218-134">Overriding by Item sales tax group provides different options than overriding by sales tax group.</span></span>    <span data-ttu-id="b8218-135">สามารถตั้งค่าการแทนที่ภาษีขายให้แทนที่ภาษีในธุรกรรมทั้งหมดหรือบรรทัดเฉพาะในธุรกรรม</span><span class="sxs-lookup"><span data-stu-id="b8218-135">Sales tax overrides can be set up to override taxes on entire transactions or on particular lines in the transaction.</span></span>  
13. <span data-ttu-id="b8218-136">คลิก บันทึก</span><span class="sxs-lookup"><span data-stu-id="b8218-136">Click Save.</span></span>
14. <span data-ttu-id="b8218-137">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="b8218-137">Close the page.</span></span>
15. <span data-ttu-id="b8218-138">ไปที่ การขายปลีกและการค้า > การตั้งค่าช่องทาง > ภาษีขาย > กลุ่มแทนที่ภาษีขาย</span><span class="sxs-lookup"><span data-stu-id="b8218-138">Go to Retail and commerce > Channel setup > Sales taxes > Sales tax override groups.</span></span>
    * <span data-ttu-id="b8218-139">ในขั้นตอนนี้ คุณจะกำหนดให้แทนภาษีขายที่สร้างขึ้นใหม่กับกลุ่มแทนที่ภาษีขายที่กำหนดไปยังช่องทาง 'Houston'</span><span class="sxs-lookup"><span data-stu-id="b8218-139">In this step you will assigned the newly created sales tax override to the sales tax override group assigned to the Houston channel.</span></span>  
16. <span data-ttu-id="b8218-140">คลิก แก้ไข</span><span class="sxs-lookup"><span data-stu-id="b8218-140">Click Edit.</span></span>
17. <span data-ttu-id="b8218-141">ขยายหรือยุบส่วนการตั้งค่า</span><span class="sxs-lookup"><span data-stu-id="b8218-141">Expand or collapse the Setup section.</span></span>
18. <span data-ttu-id="b8218-142">คลิก เพิ่ม</span><span class="sxs-lookup"><span data-stu-id="b8218-142">Click Add.</span></span>
19. <span data-ttu-id="b8218-143">ในฟิลด์การแทนที่ภาษีขาย ให้คลิกปุ่มดรอปดาวน์เพื่อเปิดการค้นหา</span><span class="sxs-lookup"><span data-stu-id="b8218-143">In the Sales tax override field, click the drop-down button to open the lookup.</span></span>
20. <span data-ttu-id="b8218-144">เลือกการแทนที่ภาษีขายที่สร้างขึ้นก่อนหน้านี้จากรายการ</span><span class="sxs-lookup"><span data-stu-id="b8218-144">Select the previously created sales tax override from the list.</span></span>
21. <span data-ttu-id="b8218-145">ในรายการนี้ ให้คลิกลิงค์ในแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="b8218-145">In the list, click the link in the selected row.</span></span>
22. <span data-ttu-id="b8218-146">คลิก บันทึก</span><span class="sxs-lookup"><span data-stu-id="b8218-146">Click Save.</span></span>


