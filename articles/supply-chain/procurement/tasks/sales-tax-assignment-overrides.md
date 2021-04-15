---
title: การกำหนดและการแทนที่ภาษีขาย
description: ขั้นตอนนี้อธิบายวิธีการกำหนดกลุ่มภาษีขายตามช่องทางการค้า
author: kamaybac
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: RetailStoreTable, RetailTaxOverrideCode, RetailTaxOverrideGroup
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: dabourq
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 28d393dcf727eec7211f6092ea67de2b85359f1a
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 04/01/2021
ms.locfileid: "5811953"
---
# <a name="sales-tax-assignment-and-overrides"></a><span data-ttu-id="3b199-103">การกำหนดและการแทนที่ภาษีขาย</span><span class="sxs-lookup"><span data-stu-id="3b199-103">Sales tax assignment and overrides</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="3b199-104">ขั้นตอนนี้อธิบายวิธีการกำหนดกลุ่มภาษีขายตามช่องทางการค้า</span><span class="sxs-lookup"><span data-stu-id="3b199-104">This procedure demonstrates how to assign sales tax groups to commerce channels.</span></span> <span data-ttu-id="3b199-105">และยังแนะนำขั้นตอนการสร้างการแทนที่ภาษีขายใหม่ และการกำหนดให้กับกลุ่มแทนที่ภาษีขายที่มีอยู่ </span><span class="sxs-lookup"><span data-stu-id="3b199-105">It also walks through the process of creating a new sales tax override and assigning it to an existing sales tax override group.</span></span> <span data-ttu-id="3b199-106">กระบวนงานนี้ใช้บริษัท USRT ในข้อมูลสาธิต</span><span class="sxs-lookup"><span data-stu-id="3b199-106">This procedure uses the USRT company in demo data.</span></span>

1. <span data-ttu-id="3b199-107">ไปยัง การขายปลีกและการค้า > ช่องทาง > ร้านค้า > ร้านค้าทั้งหมด</span><span class="sxs-lookup"><span data-stu-id="3b199-107">Go to Retail and Commerce > Channels > Stores > All stores.</span></span>
2. <span data-ttu-id="3b199-108">ในรายการ ให้คลิกลิงค์รหัสช่องทางสำหรับ "Houston"</span><span class="sxs-lookup"><span data-stu-id="3b199-108">In the list, click the Channel ID link for "Houston."</span></span>
3. <span data-ttu-id="3b199-109">คลิกแก้ไข</span><span class="sxs-lookup"><span data-stu-id="3b199-109">Click Edit.</span></span>
    * <span data-ttu-id="3b199-110">ฟิลด์ "กลุ่มภาษีขาย" ประกอบด้วยรายการของกลุ่มภาษีขายสำหรับบริษัทปัจจุบัน </span><span class="sxs-lookup"><span data-stu-id="3b199-110">The "Sales tax group" field contains the list of sales tax groups for the current company.</span></span> <span data-ttu-id="3b199-111">กลุ่มที่กำหนดไว้ในปัจจุบันเป็นกลุ่มภาษีขายสำหรับ "Texas" ทั่วไป </span><span class="sxs-lookup"><span data-stu-id="3b199-111">The currently assigned group is a generic "Texas" sales tax group.</span></span> <span data-ttu-id="3b199-112">จากนั้นยังมีกลุ่มภาษีขายสำหรับ "Washington" และ "Washington, King County" </span><span class="sxs-lookup"><span data-stu-id="3b199-112">There are also sales tax groups for "Washington" and "Washington, King County."</span></span> <span data-ttu-id="3b199-113">กลุ่มภาษีขายอาจรวมภาษีที่เกี่ยวข้องสำหรับหลายอำเภอ</span><span class="sxs-lookup"><span data-stu-id="3b199-113">Sales tax groups can include applicable taxes for multiple municipalities.</span></span>  
    * <span data-ttu-id="3b199-114">ฟิลด์ "การแทนที่ภาษีขาย" คือตำแหน่งที่กลุ่มแทนที่ภาษีขายสามารถแม็ปไปยังช่องทาง </span><span class="sxs-lookup"><span data-stu-id="3b199-114">The "Sales tax override" field is where sales tax override groups can be mapped to the channel.</span></span> <span data-ttu-id="3b199-115">สามารถใช้กลุ่มแทนภาษีขายในการจัดกลุ่มการแทนที่ภาษีขายที่ทำงานสำหรับหลายร้านค้าไว้ด้วยกัน </span><span class="sxs-lookup"><span data-stu-id="3b199-115">Sales tax override groups can be used to group together sales tax overrides that work for multiple stores.</span></span> <span data-ttu-id="3b199-116">แทนการกำหนดการแทนที่ภาษีขายด้วยตนเองทีละรายการ สามารถสร้างและกำหนดกลุ่มให้กับช่องทางโดยตรงเพื่อประหยัดเวลา</span><span class="sxs-lookup"><span data-stu-id="3b199-116">Rather than manually assigning sales tax overrides one by one, the group can be created and assigned directly to the channels to save time.</span></span>  
4. <span data-ttu-id="3b199-117">คลิก บันทึก</span><span class="sxs-lookup"><span data-stu-id="3b199-117">Click Save.</span></span>
5. <span data-ttu-id="3b199-118">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="3b199-118">Close the page.</span></span>
6. <span data-ttu-id="3b199-119">ไปที่ การขายปลีกและการค้า > การตั้งค่าช่องทาง > ภาษีขาย > การแทนที่ภาษีขาย</span><span class="sxs-lookup"><span data-stu-id="3b199-119">Go to Retail and Commerce > Channel setup > Sales taxes > Sales tax overrides.</span></span>
7. <span data-ttu-id="3b199-120">คลิก สร้าง</span><span class="sxs-lookup"><span data-stu-id="3b199-120">Click New.</span></span>
8. <span data-ttu-id="3b199-121">ในฟิลด์การแทนที่ภาษีขาย ให้ป้อนชื่อสำหรับการแทนที่ใหม่ของคุณ</span><span class="sxs-lookup"><span data-stu-id="3b199-121">In the Sales tax override field, provide a name for your new override.</span></span>
9. <span data-ttu-id="3b199-122">ในฟิลด์คำอธิบาย ป้อนคำอธิบายของการแทนที่</span><span class="sxs-lookup"><span data-stu-id="3b199-122">In the Description field, provide a description of the override.</span></span>
10. <span data-ttu-id="3b199-123">ตั้งค่าสถานะเป็น "เปิดใช้งาน"</span><span class="sxs-lookup"><span data-stu-id="3b199-123">Set the status to "Enable."</span></span>
11. <span data-ttu-id="3b199-124">ขยายหรือยุบส่วนการแทนที่</span><span class="sxs-lookup"><span data-stu-id="3b199-124">Expand or collapse the Override section.</span></span>
12. <span data-ttu-id="3b199-125">ในฟิลด์ชนิด ให้เลือกหนึ่งตัวเลือก</span><span class="sxs-lookup"><span data-stu-id="3b199-125">In the Type field, select an option.</span></span>
    * <span data-ttu-id="3b199-126">สามารถใช้กลุ่มภาษีขายตามประเภทสินค้าแทนภาษีสำหรับสินค้าเฉพาะที่อยู่ในกลุ่มนั้นได้ </span><span class="sxs-lookup"><span data-stu-id="3b199-126">Item sales tax groups can be used to override taxes for specific items that belong to the group.</span></span> <span data-ttu-id="3b199-127">ตัวอย่างเช่น โดยทั่วไปสินค้าอาหารจะคิดภาษีแตกต่างจากครุภัณฑ์ และอาจจะมีกลุ่มภาษีขายของตนเอง </span><span class="sxs-lookup"><span data-stu-id="3b199-127">For example, food items are typically taxed differently from hard goods, and would likely have their own sales tax group.</span></span> <span data-ttu-id="3b199-128">กลุ่มภาษีขายคือ กลุ่มของภาษีที่สามารถใช้ได้กับช่องทางเฉพาะ </span><span class="sxs-lookup"><span data-stu-id="3b199-128">Sales tax groups are groups of taxes that are applicable to a particular channel.</span></span> <span data-ttu-id="3b199-129">ตัวอย่างเช่น ถ้าช่องทางนั้น ๆ ทั้งขายปลีกและรวมระหว่างธุรกิจ กลุ่มภาษีขายตามประเภทสินค้าที่แตกต่างกันอาจถูกนำมาใช้ได้ </span><span class="sxs-lookup"><span data-stu-id="3b199-129">For example, if a channel sells both retail and business-to-business, different items sales tax groups may be used.</span></span> <span data-ttu-id="3b199-130">ภาษีที่เกี่ยวข้องทั้งหมดจะถูกแมปเข้ากับกลุ่มภาษีขาย</span><span class="sxs-lookup"><span data-stu-id="3b199-130">All the applicable taxes would be mapped to the sales tax group.</span></span>  
    * <span data-ttu-id="3b199-131">ขณะนี้คุณสามารถเลือก "เริ่มต้น" และ "สิ้นสุด" ภาษี หรือ "จากกลุ่มภาษี" และ "เป็นกลุ่มภาษี" เพื่อสร้างการแทนที่ภาษีขายของคุณ </span><span class="sxs-lookup"><span data-stu-id="3b199-131">Now you can select the "From" and "To" taxes or "From tax group" and "To tax group" to create your sales tax override.</span></span> <span data-ttu-id="3b199-132">ฟิลด์ "เริ่มต้น" บ่งชี้ภาษีหรือกลุ่มภาษีที่จะถูกแทนที่ </span><span class="sxs-lookup"><span data-stu-id="3b199-132">The "From" field indicates the tax or tax group to be overridden.</span></span> <span data-ttu-id="3b199-133">การแทนที่ด้วยกลุ่มภาษีขายสินค้ามีตัวเลือกต่าง ๆ มากกว่าการแทนที่ด้วยกลุ่มภาษีขาย </span><span class="sxs-lookup"><span data-stu-id="3b199-133">Overriding by Item sales tax group provides different options than overriding by sales tax group.</span></span> <span data-ttu-id="3b199-134">สามารถตั้งค่าการแทนที่ภาษีขายให้แทนที่ภาษีในธุรกรรมทั้งหมดหรือบรรทัดเฉพาะในธุรกรรม</span><span class="sxs-lookup"><span data-stu-id="3b199-134">Sales tax overrides can be set up to override taxes on entire transactions or on particular lines in the transaction.</span></span>  
13. <span data-ttu-id="3b199-135">คลิก บันทึก</span><span class="sxs-lookup"><span data-stu-id="3b199-135">Click Save.</span></span>
14. <span data-ttu-id="3b199-136">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="3b199-136">Close the page.</span></span>
15. <span data-ttu-id="3b199-137">ไปที่ การขายปลีกและการค้า > การตั้งค่าช่องทาง > ภาษีขาย > กลุ่มแทนที่ภาษีขาย</span><span class="sxs-lookup"><span data-stu-id="3b199-137">Go to Retail and Commerce > Channel setup > Sales taxes > Sales tax override groups.</span></span>
    * <span data-ttu-id="3b199-138">ในขั้นตอนนี้ คุณจะกำหนดให้แทนภาษีขายที่สร้างขึ้นใหม่กับกลุ่มแทนที่ภาษีขายที่กำหนดไปยังช่องทาง 'Houston'</span><span class="sxs-lookup"><span data-stu-id="3b199-138">In this step you will assigned the newly created sales tax override to the sales tax override group assigned to the Houston channel.</span></span>  
16. <span data-ttu-id="3b199-139">คลิก แก้ไข</span><span class="sxs-lookup"><span data-stu-id="3b199-139">Click Edit.</span></span>
17. <span data-ttu-id="3b199-140">ขยายหรือยุบส่วนการตั้งค่า</span><span class="sxs-lookup"><span data-stu-id="3b199-140">Expand or collapse the Setup section.</span></span>
18. <span data-ttu-id="3b199-141">คลิก เพิ่ม</span><span class="sxs-lookup"><span data-stu-id="3b199-141">Click Add.</span></span>
19. <span data-ttu-id="3b199-142">ในฟิลด์การแทนที่ภาษีขาย ให้คลิกปุ่มดรอปดาวน์เพื่อเปิดการค้นหา</span><span class="sxs-lookup"><span data-stu-id="3b199-142">In the Sales tax override field, click the drop-down button to open the lookup.</span></span>
20. <span data-ttu-id="3b199-143">เลือกการแทนที่ภาษีขายที่สร้างขึ้นก่อนหน้านี้จากรายการ</span><span class="sxs-lookup"><span data-stu-id="3b199-143">Select the previously created sales tax override from the list.</span></span>
21. <span data-ttu-id="3b199-144">ในรายการนี้ ให้คลิกลิงค์ในแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="3b199-144">In the list, click the link in the selected row.</span></span>
22. <span data-ttu-id="3b199-145">คลิก บันทึก</span><span class="sxs-lookup"><span data-stu-id="3b199-145">Click Save.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]