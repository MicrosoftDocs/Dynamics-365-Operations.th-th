---
title: ค้นหาข้อมูลโดยใช้การค้นหา
description: ฟิลด์หลายฟิลด์มีการค้นหาที่สามารถช่วยคุณในการค้นหาค่าที่ถูกต้องหรือที่ต้องการได้อย่างง่ายดาย มีการเพิ่มการส่งเสริมหลายอย่างสำหรับการค้นหาที่จะทำให้ตัวควบคุมเหล่านี้สามารถใช้งานได้มากขึ้น และทำให้ผู้ใช้มีประสิทธิผลมากขึ้น ในหัวข้อนี้ คุณจะได้เรียนรู้เกี่ยวกับคุณลักษณะการค้นหาใหม่เหล่านี้ และจะได้รับเคล็ดลับที่มีประโยชน์บางอย่างเพื่อการใช้งานที่มีประสิทธิภาพสูงสุดจากการค้นหาที่ดีที่สุดในระบบ
author: jasongre
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: sericks
ms.custom: 269934
ms.assetid: f20cbd2c-14e0-47e7-b351-8e60d3537f96
ms.search.region: Global
ms.author: jasongre
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: d75e66e8fb9f1a227c9dd15f92ca5db433c0db4a
ms.sourcegitcommit: b112925c389a460a98c3401cc2c67df7091b066f
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 12/19/2020
ms.locfileid: "4798154"
---
# <a name="find-information-by-using-lookups"></a><span data-ttu-id="cd85e-105">ค้นหาข้อมูลโดยใช้การค้นหา</span><span class="sxs-lookup"><span data-stu-id="cd85e-105">Find information by using lookups</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="cd85e-106">ฟิลด์หลายฟิลด์มีการค้นหาที่สามารถช่วยคุณในการค้นหาค่าที่ถูกต้องหรือที่ต้องการได้อย่างง่ายดาย</span><span class="sxs-lookup"><span data-stu-id="cd85e-106">Many fields have lookups that can help you easily find the correct or desired value.</span></span> <span data-ttu-id="cd85e-107">มีการเพิ่มการส่งเสริมหลายอย่างสำหรับการค้นหาที่จะทำให้ตัวควบคุมเหล่านี้สามารถใช้งานได้มากขึ้น และทำให้ผู้ใช้มีประสิทธิผลมากขึ้น</span><span class="sxs-lookup"><span data-stu-id="cd85e-107">Several enhancements have been added to lookups that make these controls more usable and make users more productive.</span></span> <span data-ttu-id="cd85e-108">ในหัวข้อนี้ คุณจะได้เรียนรู้เกี่ยวกับคุณลักษณะการค้นหาใหม่เหล่านี้ และจะได้รับเคล็ดลับที่มีประโยชน์บางอย่างเพื่อการใช้งานที่มีประสิทธิภาพสูงสุดจากการค้นหาที่ดีที่สุดในระบบ</span><span class="sxs-lookup"><span data-stu-id="cd85e-108">In this topic, you will learn about these new lookup features and will receive some helpful tips to get the optimal use out of lookups in the system.</span></span>

## <a name="responsive-lookups"></a><span data-ttu-id="cd85e-109">การค้นหาแบบตอบสนอง</span><span class="sxs-lookup"><span data-stu-id="cd85e-109">Responsive lookups</span></span>

<span data-ttu-id="cd85e-110">ในรุ่นก่อนหน้า เมื่อมีการโต้ตอบกับตัวควบคุมการค้นหา ผู้ใช้จะต้องดำเนินการอย่างชัดเจนเพื่อเปิดเมนูแบบหล่นลง</span><span class="sxs-lookup"><span data-stu-id="cd85e-110">In previous versions, when interacting with a lookup control, a user would have to take an explicit action to open the drop-down menu.</span></span> <span data-ttu-id="cd85e-111">ซึ่งอาจทำได้โดยการพิมพ์เครื่องหมายดอกจัน (\*) ในตัวควบคุมเพื่อกรองข้อมูลการค้นหาโดยขึ้นอยู่กับค่าปัจจุบันของตัวควบคุม คลิกปุ่มแบบเลื่อนลง หรือใช้แป้นพิมพ์ลัด **Alt**+**ลูกศรลง**</span><span class="sxs-lookup"><span data-stu-id="cd85e-111">This may have been by typing an asterisk (\*) in the control to filter the lookup based on the current value of the control, clicking the drop-down button, or by using the **Alt**+**Down arrow** keyboard shortcut.</span></span> <span data-ttu-id="cd85e-112">มีการปรับเปลี่ยนตัวควบคุมการค้นหาในวิธีการต่อไปนี้เพื่อให้สอดคล้องกับแนวทางปฏิบัติของเว็บปัจจุบันได้ดียิ่งขึ้น:</span><span class="sxs-lookup"><span data-stu-id="cd85e-112">Lookup controls have been modified in the following ways to better align with current web practices:</span></span>

- <span data-ttu-id="cd85e-113">ตอนนี้เมนูแบบหล่นลงของการค้นหาจะเปิดขึ้นโดยอัตโนมัติหลังจากที่หยุดพิมพ์ชั่วคราวชั่วครู่พร้อมกับเนื้อหาเมนูแบบหล่นลงที่ถูกกรองข้อความตามค่าของตัวควบคุมการค้นหา</span><span class="sxs-lookup"><span data-stu-id="cd85e-113">Lookup drop-down menus will now open automatically after a slight pause in typing, with the drop-down menu contents filtered based on the lookup control's value.</span></span>

    <span data-ttu-id="cd85e-114">หมายเหตุว่าลักษณะการทำงานเดิมของการเปิดรายการแบบหล่นลงโดยอัตโนมัติหลังจากที่พิมพ์เครื่องหมายดอกจัน (\*) ได้รับการสนับสนุนแล้ว</span><span class="sxs-lookup"><span data-stu-id="cd85e-114">Note that the old behavior of automatic opening of the dropdown after typing an asterisk (\*) has been deprecated.</span></span>

- <span data-ttu-id="cd85e-115">หลังจากที่มีการเปิดเมนูค้นหาแบบหล่นลง สิ่งต่อไปนี้จะเกิดขึ้น:</span><span class="sxs-lookup"><span data-stu-id="cd85e-115">After the lookup drop-down menu has opened, the following will occur:</span></span>

    - <span data-ttu-id="cd85e-116">เคอร์เซอร์จะยังคงอยู่ในตัวควบคุมการค้นหา (แทนการย้ายโฟกัสไปยังเมนูแบบหล่นลง) ดังนั้นคุณจะยังคงสามารถปรับเปลี่ยนค่าของตัวควบคุมได้</span><span class="sxs-lookup"><span data-stu-id="cd85e-116">The cursor will stay in the lookup control (instead of focus moving into the drop-down menu) so you can continue to make modifications to the control's value.</span></span> <span data-ttu-id="cd85e-117">อย่างไรก็ตาม ผู้ใช้จะยังคงสามารถใช้ **ลูกศรขึ้น** และ **ลูกศรลง** เพื่อเปลี่ยนแถวในเมนูแบบหล่นลง และป้อนเพื่อเลือกแถวปัจจุบันในเมนูแบบหล่นลงได้</span><span class="sxs-lookup"><span data-stu-id="cd85e-117">However, the user can still use the **Up arrow** and **Down arrow** to change rows in the drop-down menu, and enter to select the current row in the drop-down menu.</span></span>
    - <span data-ttu-id="cd85e-118">เนื้อหาของเมนูแบบหล่นลงจะปรับปรุงหลังจากมีการปรับเปลี่ยนค่าของตัวควบคุมการค้นหาใดๆ</span><span class="sxs-lookup"><span data-stu-id="cd85e-118">The contents of the drop-down menu will adjust after any modifications are made to the lookup control's value.</span></span>

<span data-ttu-id="cd85e-119">ตัวอย่างเช่น พิจารณาฟิลด์การค้นหาที่ชื่อว่า **เมือง**</span><span class="sxs-lookup"><span data-stu-id="cd85e-119">For example, consider a lookup field called **City**.</span></span>

<span data-ttu-id="cd85e-120">เมื่อโฟกัสอยู่ที่ฟิลด์ **เมือง** คุณสามารถเริ่มค้นหาเมืองที่คุณต้องการได้โดยการพิมพ์ตัวอักษรเพียงไม่กี่ตัว เช่น "โคโล"</span><span class="sxs-lookup"><span data-stu-id="cd85e-120">When focus is in the **City** field, you can start looking for the city that you want by typing a few letters, like "col."</span></span> <span data-ttu-id="cd85e-121">หลังจากที่คุณหยุดพิมพ์ การค้นหาจะเปิดขึ้นโดยอัตโนมัติโดยมีการกรองข้อมูลสำหรับเมืองเหล่านั้นที่ขึ้นต้นด้วย "โคโล"</span><span class="sxs-lookup"><span data-stu-id="cd85e-121">After you stop typing, the lookup will open automatically, filtered to those cities that begin with "col".</span></span>

<span data-ttu-id="cd85e-122">[![typeaheadLookupExample](./media/typeaheadlookupexample.png)](./media/typeaheadlookupexample.png)</span><span class="sxs-lookup"><span data-stu-id="cd85e-122">[![typeaheadLookupExample](./media/typeaheadlookupexample.png)](./media/typeaheadlookupexample.png)</span></span>

<span data-ttu-id="cd85e-123">ณ จุดนี้ เคอร์เซอร์จะยังคงอยู่ในฟิลด์การค้นหา</span><span class="sxs-lookup"><span data-stu-id="cd85e-123">At this point, the cursor is still in the lookup field.</span></span> <span data-ttu-id="cd85e-124">ถ้าคุณพิมพ์ต่อไป ค่าจะเป็น "คอลัมน์" เนื้อหาการค้นหาจะปรับปรุงโดยอัตโนมัติเพื่อสะท้อนถึงค่าล่าสุดในตัวควบคุม</span><span class="sxs-lookup"><span data-stu-id="cd85e-124">If you continue typing so the value is "colum," the lookup contents adjust automatically to reflect the latest value in the control.</span></span>

![updateFilterLookupExample](./media/updatefilterlookupexample.png)

<span data-ttu-id="cd85e-126">แม้ว่าโฟกัสจะยังคงอยู่ในตัวควบคุมการค้นหา คุณสามารถใช้คีย์ **ลูกศรขึ้น** หรือ **ลูกศรลง** เพื่อเน้นแถวที่คุณต้องการเลือกได้</span><span class="sxs-lookup"><span data-stu-id="cd85e-126">Even though focus is still in the lookup control, you can also use the **Up arrow** or **Down arrow** keys to highlight the row that you want to select.</span></span> <span data-ttu-id="cd85e-127">ถ้าคุณกด **Enter** แถวที่มีการเน้นจะถูกเลือกจากการค้นหา และค่าของตัวควบคุมจะถูกอัพเดต</span><span class="sxs-lookup"><span data-stu-id="cd85e-127">If you press **Enter** the highlighted row will be selected from the lookup and the control's value will be updated.</span></span>

![changingSelectionLookup](./media/changingselectionlookup.png)

## <a name="typing-in-more-than-ids"></a><span data-ttu-id="cd85e-129">การพิมพ์รหัสมากกว่าหนึ่งรายการ</span><span class="sxs-lookup"><span data-stu-id="cd85e-129">Typing in more than IDs</span></span>

<span data-ttu-id="cd85e-130">เมื่อป้อนข้อมูล ถือเป็นเรื่องปกติที่ผู้ใช้จะต้องพยายามระบุเอนทิตี เช่น ลูกค้าหรือผู้จัดจำหน่าย ในรูปแบบของชื่อแทนตัวระบุที่แสดงถึงเอนทิตี</span><span class="sxs-lookup"><span data-stu-id="cd85e-130">When entering data, it's natural for users to attempt to identify an entity, such as a customer or vendor, in terms of the name rather than an identifier representing the entity.</span></span> <span data-ttu-id="cd85e-131">การค้นหาจำนวนมาก (แต่ไม่ใช่ทั้งหมด) ในขณะนี้จะอนุญาตให้ป้อนข้อมูลในบริบท</span><span class="sxs-lookup"><span data-stu-id="cd85e-131">Many (but not all) lookups now allow contextual data entry.</span></span> <span data-ttu-id="cd85e-132">คุณลักษณะที่มีประสิทธิภาพนี้ช่วยให้ผู้ใช้สามารถพิมพ์รหัสหรือชื่อที่เกี่ยวข้องลงในตัวควบคุมการค้นหา</span><span class="sxs-lookup"><span data-stu-id="cd85e-132">This powerful feature allows the user to type the ID or the corresponding name into the lookup control.</span></span>

<span data-ttu-id="cd85e-133">ตัวอย่างเช่น พิจารณาฟิลด์ **บัญชีลูกค้า** เมื่อสร้างใบสั่งขาย</span><span class="sxs-lookup"><span data-stu-id="cd85e-133">For example, consider the **Customer account** field when creating a sales order.</span></span> <span data-ttu-id="cd85e-134">ฟิลด์นี้จะแสดง **รหัสบัญชี** สำหรับลูกค้า แต่โดยทั่วไปผู้ใช้มักจะต้องการป้อน **ชื่อบัญชี** แทน **รหัสบัญชี** สำหรับฟิลด์นี้เมื่อสร้างใบสั่งขาย เช่น "Forest Wholesales" แทน "US-003"</span><span class="sxs-lookup"><span data-stu-id="cd85e-134">This field shows the **Account ID** for the customer, but a user would typically prefer to enter an **Account name** instead of an **Account ID** for this field when creating a sales order, such as "Forest Wholesales" instead of "US-003."</span></span>

<span data-ttu-id="cd85e-135">ถ้าผู้ใช้เริ่มป้อน **รหัสบัญชี** ลงในตัวควบคุมการค้นหา เมนูแบบหล่นลงจะเปิดขึ้นโดยอัตโนมัติตามที่อธิบายไว้ในส่วนก่อนหน้านี้ และผู้ใช้จะเห็นการค้นหาดังที่แสดงด้านล่าง</span><span class="sxs-lookup"><span data-stu-id="cd85e-135">If the user started to enter an **Account ID** into the lookup control, the drop-down menu would automatically open as described in the previous section and the user would see the lookup as shown below.</span></span>

<span data-ttu-id="cd85e-136">[![การค้นหาตามบริบทเมื่อมีการป้อนรหัสของบัญชีลูกค้า](./media/howtocontextuallookups-1.png)](./media/howtocontextuallookups-1.png)</span><span class="sxs-lookup"><span data-stu-id="cd85e-136">[![Contextual lookup when a customer account ID is entered](./media/howtocontextuallookups-1.png)](./media/howtocontextuallookups-1.png)</span></span>

<span data-ttu-id="cd85e-137">อย่างไรก็ตาม ขณะนี้ผู้ใช้สามารถป้อนจุดเริ่มต้นของ **ชื่อบัญชี** ได้แล้ว</span><span class="sxs-lookup"><span data-stu-id="cd85e-137">However, the user can also now enter the beginning of an **Account name** as well.</span></span> <span data-ttu-id="cd85e-138">ถ้ามีการตรวจพบ ผู้ใช้จะเห็นการค้นหาต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="cd85e-138">If this is detected, then the user will see the following lookup.</span></span> <span data-ttu-id="cd85e-139">สังเกตุวิธีการย้ายคอลัมน์ **ชื่อ** ไปเป็นคอลัมน์แรกในการค้นหา และวิธีการเรียงลำดับและการกรองข้อมูลการค้นหาตามคอลัมน์ **ชื่อ**</span><span class="sxs-lookup"><span data-stu-id="cd85e-139">Notice how the **Name** column is moved to be the first column in the lookup, and how the lookup is sorted and filtered based on the **Name** column.</span></span>

<span data-ttu-id="cd85e-140">[![การค้นหาตามบริบทเมื่อมีการป้อนชื่อลูกค้า](./media/howtocontextuallookups-2.png)](./media/howtocontextuallookups-2.png)</span><span class="sxs-lookup"><span data-stu-id="cd85e-140">[![Contextual lookup when a customer name is entered](./media/howtocontextuallookups-2.png)](./media/howtocontextuallookups-2.png)</span></span>

## <a name="using-grid-column-headers-for-more-advanced-filtering-and-sorting"></a><span data-ttu-id="cd85e-141">การใช้ส่วนหัวคอลัมน์กริดเพื่อการกรองและการเรียงลำดับขั้นสูง</span><span class="sxs-lookup"><span data-stu-id="cd85e-141">Using grid column headers for more advanced filtering and sorting</span></span>

<span data-ttu-id="cd85e-142">การเพิ่มประสิทธิภาพการค้นหาที่อธิบายไว้ในสองหัวข้อก่อนหน้านี้ช่วยปรับปรุงความสามารถของผู้ใช้ในการนำทางไปยังแถวในการค้นหาตามการค้นหา "ขึ้นต้นด้วย" ของฟิลด์ **รหัส** หรือ **ชื่อ** ในการค้นหาได้อย่างมาก</span><span class="sxs-lookup"><span data-stu-id="cd85e-142">The lookup enhancements discussed in the previous two sections greatly improve a user's ability to navigate the rows in a lookup based on a "begins with" search of the **ID** or **Name** field in the lookup.</span></span> <span data-ttu-id="cd85e-143">อย่างไรก็ตาม มีบางกรณีที่จำเป็นต้องใช้การกรอง (หรือการเรียงลำดับ) ขั้นสูงในการค้นหาแถวที่ถูกต้อง</span><span class="sxs-lookup"><span data-stu-id="cd85e-143">However, there are situations in which more advanced filtering (or sorting) is needed to find the correct row.</span></span> <span data-ttu-id="cd85e-144">ในสถานการณ์เหล่านี้ ผู้ใช้อาจต้องใช้ตัวเลือกการกรองข้อมูลและการเรียงลำดับในส่วนหัวของคอลัมน์กริดภายในการค้นหา</span><span class="sxs-lookup"><span data-stu-id="cd85e-144">In these situations, the user needs to use the filtering and sorting options in the grid column headers inside the lookup.</span></span> <span data-ttu-id="cd85e-145">ตัวอย่างเช่น พิจารณาพนักงานที่ป้อนบรรทัดใบสั่งขายที่ต้องการค้นหา "เคเบิล" ที่ถูกต้องโดยเป็นผลิตภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="cd85e-145">For example, consider an employee entering a sales order line who needs to locate the right "cable" as the product.</span></span> <span data-ttu-id="cd85e-146">การพิมพ์ "เคเบิล" ลงในตัวควบคุม **หมายเลขสินค้า** ไม่มีประโยชน์ เนื่องจากไม่มีชื่อผลิตภัณฑ์ที่ขึ้นต้นด้วย "เคเบิล"</span><span class="sxs-lookup"><span data-stu-id="cd85e-146">Typing "cable" into the **Item number** control isn't helpful, as there are no product names that begin with "cable."</span></span>

![emptyitemlookup](./media/emptyitemlookup.png)

<span data-ttu-id="cd85e-148">ในทางกลับกัน ผู้ใช้จำเป็นต้องล้างค่าตัวควบคุมการค้นหา เปิดเมนูการค้นหาแบบหล่นลง และกรองเมนูแบบหล่นลงโดยใช้ส่วนหัวของคอลัมน์กริด ดังแสดงด้านล่าง</span><span class="sxs-lookup"><span data-stu-id="cd85e-148">Instead, the user needs to clear the value of the lookup control, open the lookup drop-down menu, and filter the drop-down menu using the grid column header, as shown below.</span></span> <span data-ttu-id="cd85e-149">เมาส์ (หรือสัมผัส) ผู้ใช้สามารถเพียงแค่คลิก (หรือสัมผัส) ส่วนหัวของคอลัมน์ใด ๆ เพื่อเข้าถึงตัวเลือกการกรองข้อมูลและการเรียงลำดับสำหรับคอลัมน์นั้น</span><span class="sxs-lookup"><span data-stu-id="cd85e-149">A mouse (or touch) user can simply click (or touch) any column header to access the filtering and sorting options for that column.</span></span> <span data-ttu-id="cd85e-150">สำหรับผู้ใช้แป้นพิมพ์ ผู้ใช้เพียงแค่กด **Alt**+**ลูกศร** **ลง** เป็นครั้งที่สองเพื่อย้ายโฟกัสไปยังเมนูแบบหล่นลง หลังจากที่ผู้ใช้สามารถแตะที่คอลัมน์ที่ถูกต้อง และจากนั้นกด **Ctrl**+**G** เพื่อเปิดเมนูแบบหล่นลงที่ส่วนหัวของคอลัมน์กริด</span><span class="sxs-lookup"><span data-stu-id="cd85e-150">For a keyboard user, the user simply needs to press **Alt**+**Down** **arrow** a second time to move focus into the drop-down menu, after which the user can tab to the correct column, and then press **Ctrl**+**G** to open the grid column header drop-down menu.</span></span>

<span data-ttu-id="cd85e-151">[![gridfilteritemlookup](./media/gridfilteritemlookup.png)](./media/gridfilteritemlookup.png)</span><span class="sxs-lookup"><span data-stu-id="cd85e-151">[![gridfilteritemlookup](./media/gridfilteritemlookup.png)](./media/gridfilteritemlookup.png)</span></span>

<span data-ttu-id="cd85e-152">หลังจากที่ได้นำตัวกรองมาใช้ (ดูรูปภาพด้านล่าง) ผู้ใช้สามารถค้นหาและเลือกแถวได้ตามปกติ</span><span class="sxs-lookup"><span data-stu-id="cd85e-152">After the filter has been applied (see the image below), the user can find and select the row as usual.</span></span>

![filtereditemlookup](./media/filtereditemlookup.png)
