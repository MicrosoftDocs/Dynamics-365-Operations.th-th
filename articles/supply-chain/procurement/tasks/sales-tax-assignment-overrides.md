---
title: การกำหนดและการแทนที่ภาษีขาย
description: 'ขั้นตอนนี้อธิบายวิธีการกำหนดกลุ่มภาษีขายตามช่องทางการขายปลีก '
author: mkirknel
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: RetailStoreTable, RetailTaxOverrideCode, RetailTaxOverrideGroup
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: a1907b0d0266eaa405ac2b92b40d6a2d310cf07b
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 05/15/2019
ms.locfileid: "1569948"
---
# <a name="sales-tax-assignment-and-overrides"></a><span data-ttu-id="cd2fc-103">การกำหนดและการแทนที่ภาษีขาย</span><span class="sxs-lookup"><span data-stu-id="cd2fc-103">Sales tax assignment and overrides</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="cd2fc-104">ขั้นตอนนี้อธิบายวิธีการกำหนดกลุ่มภาษีขายตามช่องทางการขายปลีก </span><span class="sxs-lookup"><span data-stu-id="cd2fc-104">This procedure demonstrates how to assign sales tax groups to retail channels.</span></span> <span data-ttu-id="cd2fc-105">และยังแนะนำขั้นตอนการสร้างการแทนที่ภาษีขายใหม่ และการกำหนดให้กับกลุ่มแทนที่ภาษีขายที่มีอยู่ </span><span class="sxs-lookup"><span data-stu-id="cd2fc-105">It also walks through the process of creating a new sales tax override and assigning it to an existing sales tax override group.</span></span> <span data-ttu-id="cd2fc-106">กระบวนงานนี้</span><span class="sxs-lookup"><span data-stu-id="cd2fc-106">This procedure</span></span>

<span data-ttu-id="cd2fc-107">ใช้บริษัท USRT ในข้อมูลสาธิต</span><span class="sxs-lookup"><span data-stu-id="cd2fc-107">uses the USRT company in demo data.</span></span>

1. <span data-ttu-id="cd2fc-108">ไปยังการขายปลีกและการค้า > ช่องทาง > ร้านค้าปลีก > ร้านค้าปลีกทั้งหมด</span><span class="sxs-lookup"><span data-stu-id="cd2fc-108">Go to Retail and commerce > Channels > Retail stores > All retail stores.</span></span>
2. <span data-ttu-id="cd2fc-109">ในรายการ ให้คลิกลิงค์รหัสช่องทางการขายปลีกสำหรับ "Houston"</span><span class="sxs-lookup"><span data-stu-id="cd2fc-109">In the list, click the Retail Channel ID link for "Houston."</span></span>
3. <span data-ttu-id="cd2fc-110">คลิก แก้ไข</span><span class="sxs-lookup"><span data-stu-id="cd2fc-110">Click Edit.</span></span>
    * <span data-ttu-id="cd2fc-111">ฟิลด์ "กลุ่มภาษีขาย" ประกอบด้วยรายการของกลุ่มภาษีขายสำหรับบริษัทปัจจุบัน </span><span class="sxs-lookup"><span data-stu-id="cd2fc-111">The "Sales tax group" field contains the list of sales tax groups for the current company.</span></span> <span data-ttu-id="cd2fc-112">กลุ่มที่กำหนดไว้ในปัจจุบันเป็นกลุ่มภาษีขายสำหรับ "Texas" ทั่วไป </span><span class="sxs-lookup"><span data-stu-id="cd2fc-112">The currently assigned group is a generic "Texas" sales tax group.</span></span> <span data-ttu-id="cd2fc-113">จากนั้นยังมีกลุ่มภาษีขายสำหรับ "Washington" และ "Washington, King County" </span><span class="sxs-lookup"><span data-stu-id="cd2fc-113">There are also sales tax groups for "Washington" and "Washington, King County."</span></span> <span data-ttu-id="cd2fc-114">กลุ่มภาษีขายอาจรวมภาษีที่เกี่ยวข้องสำหรับหลายอำเภอ</span><span class="sxs-lookup"><span data-stu-id="cd2fc-114">Sales tax groups can include applicable taxes for multiple municipalities.</span></span>  
    * <span data-ttu-id="cd2fc-115">ฟิลด์ "การแทนที่ภาษีขาย" คือตำแหน่งที่กลุ่มแทนที่ภาษีขายสามารถแม็ปไปยังช่องทาง </span><span class="sxs-lookup"><span data-stu-id="cd2fc-115">The "Sales tax override" field is where sales tax override groups can be mapped to the channel.</span></span> <span data-ttu-id="cd2fc-116">สามารถใช้กลุ่มแทนภาษีขายในการจัดกลุ่มการแทนที่ภาษีขายที่ทำงานสำหรับหลายร้านค้าไว้ด้วยกัน </span><span class="sxs-lookup"><span data-stu-id="cd2fc-116">Sales tax override groups can be used to group together sales tax overrides that work for multiple stores.</span></span> <span data-ttu-id="cd2fc-117">แทนการกำหนดการแทนที่ภาษีขายด้วยตนเองทีละรายการ สามารถสร้างและกำหนดกลุ่มให้กับช่องทางโดยตรงเพื่อประหยัดเวลา</span><span class="sxs-lookup"><span data-stu-id="cd2fc-117">Rather than manually assigning sales tax overrides one by one, the group can be created and assigned directly to the channels to save time.</span></span>  
4. <span data-ttu-id="cd2fc-118">คลิก บันทึก</span><span class="sxs-lookup"><span data-stu-id="cd2fc-118">Click Save.</span></span>
5. <span data-ttu-id="cd2fc-119">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="cd2fc-119">Close the page.</span></span>
6. <span data-ttu-id="cd2fc-120">ไปที่ การขายปลีกและการค้า > การตั้งค่าช่องทาง > ภาษีขาย > การแทนที่ภาษีขาย</span><span class="sxs-lookup"><span data-stu-id="cd2fc-120">Go to Retail and commerce > Channel setup > Sales taxes > Sales tax overrides.</span></span>
7. <span data-ttu-id="cd2fc-121">คลิก สร้าง</span><span class="sxs-lookup"><span data-stu-id="cd2fc-121">Click New.</span></span>
8. <span data-ttu-id="cd2fc-122">ในฟิลด์การแทนที่ภาษีขาย ให้ป้อนชื่อสำหรับการแทนที่ใหม่ของคุณ</span><span class="sxs-lookup"><span data-stu-id="cd2fc-122">In the Sales tax override field, provide a name for your new override.</span></span>
9. <span data-ttu-id="cd2fc-123">ในฟิลด์คำอธิบาย ป้อนคำอธิบายของการแทนที่</span><span class="sxs-lookup"><span data-stu-id="cd2fc-123">In the Description field, provide a description of the override.</span></span>
10. <span data-ttu-id="cd2fc-124">ตั้งค่าสถานะเป็น "เปิดใช้งาน"</span><span class="sxs-lookup"><span data-stu-id="cd2fc-124">Set the status to "Enable."</span></span>
11. <span data-ttu-id="cd2fc-125">ขยายหรือยุบส่วนการแทนที่</span><span class="sxs-lookup"><span data-stu-id="cd2fc-125">Expand or collapse the Override section.</span></span>
12. <span data-ttu-id="cd2fc-126">ในฟิลด์ชนิด ให้เลือกหนึ่งตัวเลือก</span><span class="sxs-lookup"><span data-stu-id="cd2fc-126">In the Type field, select an option.</span></span>
    * <span data-ttu-id="cd2fc-127">สามารถใช้กลุ่มภาษีขายตามประเภทสินค้าแทนภาษีสำหรับสินค้าเฉพาะที่อยู่ในกลุ่มนั้นได้ </span><span class="sxs-lookup"><span data-stu-id="cd2fc-127">Item sales tax groups can be used to override taxes for specific items that belong to the group.</span></span> <span data-ttu-id="cd2fc-128">ตัวอย่างเช่น โดยทั่วไปสินค้าอาหารจะคิดภาษีแตกต่างจากครุภัณฑ์ และอาจจะมีกลุ่มภาษีขายของตนเอง </span><span class="sxs-lookup"><span data-stu-id="cd2fc-128">For example, food items are typically taxed differently from hard goods, and would likely have their own sales tax group.</span></span>     <span data-ttu-id="cd2fc-129">กลุ่มภาษีขายคือ กลุ่มของภาษีที่สามารถใช้ได้กับช่องทางเฉพาะ </span><span class="sxs-lookup"><span data-stu-id="cd2fc-129">Sales tax groups are groups of taxes that are applicable to a particular channel.</span></span> <span data-ttu-id="cd2fc-130">ตัวอย่างเช่น ถ้าช่องทางนั้น ๆ ทั้งขายปลีกและรวมระหว่างธุรกิจ กลุ่มภาษีขายตามประเภทสินค้าที่แตกต่างกันอาจถูกนำมาใช้ได้ </span><span class="sxs-lookup"><span data-stu-id="cd2fc-130">For example, if a channel sells both retail and business-to-business, different items sales tax groups may be used.</span></span> <span data-ttu-id="cd2fc-131">ภาษีที่เกี่ยวข้องทั้งหมดจะถูกแมปเข้ากับกลุ่มภาษีขาย</span><span class="sxs-lookup"><span data-stu-id="cd2fc-131">All the applicable taxes would be mapped to the sales tax group.</span></span>  
    * <span data-ttu-id="cd2fc-132">ขณะนี้คุณสามารถเลือก "เริ่มต้น" และ "สิ้นสุด" ภาษี หรือ "จากกลุ่มภาษี" และ "เป็นกลุ่มภาษี" เพื่อสร้างการแทนที่ภาษีขายของคุณ </span><span class="sxs-lookup"><span data-stu-id="cd2fc-132">Now you can select the "From" and "To" taxes or "From tax group" and "To tax group" to create your sales tax override.</span></span>    <span data-ttu-id="cd2fc-133">ฟิลด์ "เริ่มต้น" บ่งชี้ภาษีหรือกลุ่มภาษีที่จะถูกแทนที่ </span><span class="sxs-lookup"><span data-stu-id="cd2fc-133">The "From" field indicates the tax or tax group to be overridden.</span></span> <span data-ttu-id="cd2fc-134">การแทนที่ด้วยกลุ่มภาษีขายสินค้ามีตัวเลือกต่าง ๆ มากกว่าการแทนที่ด้วยกลุ่มภาษีขาย </span><span class="sxs-lookup"><span data-stu-id="cd2fc-134">Overriding by Item sales tax group provides different options than overriding by sales tax group.</span></span>    <span data-ttu-id="cd2fc-135">สามารถตั้งค่าการแทนที่ภาษีขายให้แทนที่ภาษีในธุรกรรมทั้งหมดหรือบรรทัดเฉพาะในธุรกรรม</span><span class="sxs-lookup"><span data-stu-id="cd2fc-135">Sales tax overrides can be set up to override taxes on entire transactions or on particular lines in the transaction.</span></span>  
13. <span data-ttu-id="cd2fc-136">คลิก บันทึก</span><span class="sxs-lookup"><span data-stu-id="cd2fc-136">Click Save.</span></span>
14. <span data-ttu-id="cd2fc-137">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="cd2fc-137">Close the page.</span></span>
15. <span data-ttu-id="cd2fc-138">ไปที่ การขายปลีกและการค้า > การตั้งค่าช่องทาง > ภาษีขาย > กลุ่มแทนที่ภาษีขาย</span><span class="sxs-lookup"><span data-stu-id="cd2fc-138">Go to Retail and commerce > Channel setup > Sales taxes > Sales tax override groups.</span></span>
    * <span data-ttu-id="cd2fc-139">ในขั้นตอนนี้ คุณจะกำหนดให้แทนภาษีขายที่สร้างขึ้นใหม่กับกลุ่มแทนที่ภาษีขายที่กำหนดไปยังช่องทาง 'Houston'</span><span class="sxs-lookup"><span data-stu-id="cd2fc-139">In this step you will assigned the newly created sales tax override to the sales tax override group assigned to the Houston channel.</span></span>  
16. <span data-ttu-id="cd2fc-140">คลิก แก้ไข</span><span class="sxs-lookup"><span data-stu-id="cd2fc-140">Click Edit.</span></span>
17. <span data-ttu-id="cd2fc-141">ขยายหรือยุบส่วนการตั้งค่า</span><span class="sxs-lookup"><span data-stu-id="cd2fc-141">Expand or collapse the Setup section.</span></span>
18. <span data-ttu-id="cd2fc-142">คลิก เพิ่ม</span><span class="sxs-lookup"><span data-stu-id="cd2fc-142">Click Add.</span></span>
19. <span data-ttu-id="cd2fc-143">ในฟิลด์การแทนที่ภาษีขาย ให้คลิกปุ่มดรอปดาวน์เพื่อเปิดการค้นหา</span><span class="sxs-lookup"><span data-stu-id="cd2fc-143">In the Sales tax override field, click the drop-down button to open the lookup.</span></span>
20. <span data-ttu-id="cd2fc-144">เลือกการแทนที่ภาษีขายที่สร้างขึ้นก่อนหน้านี้จากรายการ</span><span class="sxs-lookup"><span data-stu-id="cd2fc-144">Select the previously created sales tax override from the list.</span></span>
21. <span data-ttu-id="cd2fc-145">ในรายการนี้ ให้คลิกลิงค์ในแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="cd2fc-145">In the list, click the link in the selected row.</span></span>
22. <span data-ttu-id="cd2fc-146">คลิก บันทึก</span><span class="sxs-lookup"><span data-stu-id="cd2fc-146">Click Save.</span></span>

