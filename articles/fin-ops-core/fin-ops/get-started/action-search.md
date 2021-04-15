---
title: การค้นหาการดำเนินการ
description: บทความนี้อธิบายฟังก์ชันการดำเนินการค้นหา การดำเนินการค้นหาจะช่วยคุณค้นหาและดำเนินการที่เรียกใช้บนหน้า
author: jasongre
ms.date: 03/09/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: sericks
ms.custom: 62303
ms.assetid: 62c70de0-fdde-4417-8e08-0583fb095a40
ms.search.region: Global
ms.author: jasongre
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 41313dd1fde51cb84bc971bb7bb98841222259b1
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 03/31/2021
ms.locfileid: "5754837"
---
# <a name="action-search"></a><span data-ttu-id="b9259-104">การค้นหาการดำเนินการ</span><span class="sxs-lookup"><span data-stu-id="b9259-104">Action search</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="b9259-105">บทความนี้อธิบายฟังก์ชันการดำเนินการค้นหา</span><span class="sxs-lookup"><span data-stu-id="b9259-105">This article describes the action search functionality.</span></span> <span data-ttu-id="b9259-106">การดำเนินการค้นหาจะช่วยคุณค้นหาและดำเนินการที่เรียกใช้บนหน้า</span><span class="sxs-lookup"><span data-stu-id="b9259-106">Action search will help you find and run actions on a page.</span></span>

## <a name="introduction"></a><span data-ttu-id="b9259-107">คำนำ</span><span class="sxs-lookup"><span data-stu-id="b9259-107">Introduction</span></span>

<span data-ttu-id="b9259-108">โดยปกติแล้วเพจจะแสดงคำสั่งบนบานหน้าต่างดำเนินการ ทั้งบานหน้าต่างการดำเนินการมาตรฐานที่ปรากฏที่ด้านบนของเพจ และแถบเครื่องมือที่ปรากฏในส่วนต่าง ๆ ของเพจ</span><span class="sxs-lookup"><span data-stu-id="b9259-108">Pages primarily expose commands on Action Panes, both the standard Action Pane that appears at the top of a page and the toolbars that appear in various sections of the page.</span></span> <span data-ttu-id="b9259-109">ในเวอร์ชันก่อนหน้า คุณลักษณะคำแนะนำของคีย์ช่วยให้คุณสามารถเข้าถึงปุ่มใดๆ บนหน้าต่างการดำเนินการได้อย่างรวดเร็ว โดยการกดคีย์ Alt แล้วกดชุดของตัวอักษร</span><span class="sxs-lookup"><span data-stu-id="b9259-109">In previous versions, a Key Tips feature let you quickly access any button on an Action Pane by pressing the Alt key and then a series of letters.</span></span>

<span data-ttu-id="b9259-110">[![keyTipsAX6](./media/keytipsax6.png)](./media/keytipsax6.png)</span><span class="sxs-lookup"><span data-stu-id="b9259-110">[![keyTipsAX6](./media/keytipsax6.png)](./media/keytipsax6.png)</span></span>

<span data-ttu-id="b9259-111">คุณลักษณะการค้นหาการดำเนินจะแทนที่คำแนะนำของคีย์ ซึ่งไม่พร้อมใช้งานอีกต่อไป</span><span class="sxs-lookup"><span data-stu-id="b9259-111">The action search feature replaces Key Tips, which are no longer available.</span></span> <span data-ttu-id="b9259-112">คุณลักษณะใหม่นี้ช่วยให้คุณค้นหาและเรียกใช้งานปุ่มจากบานหน้าต่างการดำเนินการที่มองเห็นได้ได้ๆได้อย่างรวดเร็ว</span><span class="sxs-lookup"><span data-stu-id="b9259-112">This new feature lets you quickly search for and run a button from any visible Action Pane.</span></span>

## <a name="using-action-search"></a><span data-ttu-id="b9259-113">การใช้การดำเนินการค้นหา</span><span class="sxs-lookup"><span data-stu-id="b9259-113">Using action search</span></span>

<span data-ttu-id="b9259-114">เพื่อใช้คุณลักษณะการดำเนินการค้นหา ให้ปฏิบัติดังนี้</span><span class="sxs-lookup"><span data-stu-id="b9259-114">To use the action search feature, follow these steps.</span></span>

1. <span data-ttu-id="b9259-115">ในบานหน้าต่างการดำเนินการ ให้คลิกในฟิลด์ **การดำเนินการค้นหา**</span><span class="sxs-lookup"><span data-stu-id="b9259-115">On the Action Pane, click in the **action search** field.</span></span> <span data-ttu-id="b9259-116">(ฟิลด์ **การดำเนินการค้นหา** ประกอบด้วยไอคอนแว่นขยาย)</span><span class="sxs-lookup"><span data-stu-id="b9259-116">(The **action search** field contains a magnifying glass icon.)</span></span>
2. <span data-ttu-id="b9259-117">พิมพ์ชื่อของปุ่มทั้งหมดหรือบางส่วนที่คุณต้องการดำเนินงาน</span><span class="sxs-lookup"><span data-stu-id="b9259-117">Type all or part of the name of the button that you want to run.</span></span> <span data-ttu-id="b9259-118">คุณยังสามารถค้นหาโดยการใช้คำจากปุ่ม "เส้นทาง" ได้อีกด้วย</span><span class="sxs-lookup"><span data-stu-id="b9259-118">You can also search by using words from the button's "path."</span></span> <span data-ttu-id="b9259-119">(สำหรับข้อมูลเพิ่มเติม ให้ดูที่ส่วนถัดไปของบทความนี้) โดยทั่วไป ปุ่มจะปรากฏขึ้นใกล้กับด้านบนของรายการผลลัพธ์หลังจากที่คุณได้พิมพ์อักขระสองถึงสี่ตัว</span><span class="sxs-lookup"><span data-stu-id="b9259-119">(For more information, see the next section of this article.) Typically, a button will appear near the top of the results list after you've typed two to four characters.</span></span>
3. <span data-ttu-id="b9259-120">ค้นหาและเรียกใช้ปุ่มในรายการผลลัพธ์ (โดยการใช้เมาส์หรือแป้นพิมพ์ของคุณ)</span><span class="sxs-lookup"><span data-stu-id="b9259-120">Find and run the button in the results list (by using your mouse or keyboard).</span></span>

<span data-ttu-id="b9259-121">หลังจากเรียกใช้ปุ่ม โฟกัสจะถูกส่งกลับไปยังตำแหน่งสุดท้ายของคุณบนหน้า เพื่อให้คุณสามารถทำงานต่อไปได้</span><span class="sxs-lookup"><span data-stu-id="b9259-121">After the button is run, the focus is returned to your last position on the page, so that you can continue to work.</span></span>

<span data-ttu-id="b9259-122">[![ฟิลด์การดำเนินการค้นหา](./media/action-search-field.png)](./media/action-search-field.png)</span><span class="sxs-lookup"><span data-stu-id="b9259-122">[![action-search-field](./media/action-search-field.png)](./media/action-search-field.png)</span></span>

<span data-ttu-id="b9259-123">คุณยังสามารถเริ่มต้นการดำเนินการค้นหา ด้วยการกด Ctrl+/ or Alt+Q ได้</span><span class="sxs-lookup"><span data-stu-id="b9259-123">You can also start action search by pressing Ctrl+/ or Alt+Q.</span></span> <span data-ttu-id="b9259-124">กดแป้นพิมพ์ลัดอีกครั้งเพื่อกลับโฟกัสไปยังตำแหน่งสุดท้ายของคุณบนหน้า</span><span class="sxs-lookup"><span data-stu-id="b9259-124">Press the keyboard shortcut again to return the focus to your last position on the page.</span></span>

## <a name="understanding-the-results-list"></a><span data-ttu-id="b9259-125">การทำความเข้าใจเกี่ยวกับรายการผลลัพธ์</span><span class="sxs-lookup"><span data-stu-id="b9259-125">Understanding the results list</span></span>

<span data-ttu-id="b9259-126">ส่วนใหญ่แล้ว คุณมักจะต้องทราบทั้งที่ตั้งและบริบทของปุ่ม เพื่อให้เข้าใจถึงวัตถุประสงค์ของปุ่มนั้นอย่างแท้จริง</span><span class="sxs-lookup"><span data-stu-id="b9259-126">Often, you must know both the location and the context of a button to fully understand the purpose of that button.</span></span> <span data-ttu-id="b9259-127">ดังนั้น รายการผลลัพธ์จะแสดงข้อมูลเพิ่มเติมเพื่อช่วยให้คุณเข้าใจทุกประการว่าปุ่มใดปรากฏขึ้นในรายการ</span><span class="sxs-lookup"><span data-stu-id="b9259-127">Therefore, the results list shows additional information to help you understand exactly which buttons appear in the list.</span></span> <span data-ttu-id="b9259-128">โดยเฉพาะอย่างยิ่ง "พาธ"ของปุ่มจะถูกแสดง</span><span class="sxs-lookup"><span data-stu-id="b9259-128">In particular, the "path" of the button is shown.</span></span> <span data-ttu-id="b9259-129">พาธนี้อาจรวมถึงป้ายชื่อขององค์ประกอบ UI ต่อไปนี้ ตามที่เกี่ยวข้อง:</span><span class="sxs-lookup"><span data-stu-id="b9259-129">This path might include the labels of the following UI elements, as relevant:</span></span>

- <span data-ttu-id="b9259-130">แท็บบานหน้าต่างการดำเนินการ</span><span class="sxs-lookup"><span data-stu-id="b9259-130">Action Pane tab</span></span>
- <span data-ttu-id="b9259-131">กลุ่มของปุ่ม</span><span class="sxs-lookup"><span data-stu-id="b9259-131">Button group</span></span>
- <span data-ttu-id="b9259-132">ปุ่มเมนู (ถ้าปุ่มอยู่ภายในปุ่มเมนู)</span><span class="sxs-lookup"><span data-stu-id="b9259-132">Menu button (if the button is inside a menu button)</span></span>
- <span data-ttu-id="b9259-133">ตัวแบ่งเมนู (ถ้ามีปุ่มอยู่ภายในกลุ่มมีชื่อภายในปุ่มเมนู)</span><span class="sxs-lookup"><span data-stu-id="b9259-133">Menu separator (if the button is inside a named group inside a menu button)</span></span>
- <span data-ttu-id="b9259-134">กลุ่มหรือแท็บบนหน้า (ตัวอย่างเช่น ชื่อของ FastTab)</span><span class="sxs-lookup"><span data-stu-id="b9259-134">Group or tab on the page (for example, the name of a FastTab)</span></span>

<span data-ttu-id="b9259-135">ตัวอย่างเช่น คุณพิมพ์ **tot** ในฟิลด์ **การดำเนินการค้นหา** และขณะนี้กำลังตรวจสอบรายการผลลัพธ์</span><span class="sxs-lookup"><span data-stu-id="b9259-135">For example, you typed **tot** in the **action search** field and are now examining the results list.</span></span> <span data-ttu-id="b9259-136">รายการแรก สำหรับปุ่มที่ชื่อ **ผลรวม** จะถูกเน้น</span><span class="sxs-lookup"><span data-stu-id="b9259-136">The first entry, for a button that is named **Totals**, is highlighted.</span></span> <span data-ttu-id="b9259-137">พาธปุ่มของ **ใบสั่งขาย** &gt; **ดู** ยังจะปรากฏขึ้นด้วย</span><span class="sxs-lookup"><span data-stu-id="b9259-137">A button path of **Sales order** &gt; **View** is also shown.</span></span> <span data-ttu-id="b9259-138">ส่วน **ใบสั่งขาย** ของเส้นทางตรงกับแท็บ **ใบสั่งขาย** บนบานหน้าต่างการดำเนินการ และส่วน **มุมมอง** ของเส้นทางตรงกับกลุ่ม **มุมมอง** บนแท็บนั้น ในทำนองเดียวกัน ส่วนของปุ่ม **ส่วนลดรวม** (**ขาย** &gt; **คำนวณ**) จะแจ้งให้คุณทราบว่าปุ่มนี้อยู่ในกลุ่ม **คำนวณ** บนแท็บ **ขาย** ของบานหน้าต่างการดำเนินการ</span><span class="sxs-lookup"><span data-stu-id="b9259-138">The **Sales order** part of the path corresponds to the **Sales order** tab on the Action Pane, and the **View** part of the path corresponds to the **View** group on that tab. Similarly, the path of the **Total discount** button (**Sell** &gt; **Calculate**) informs you that this button is located in the **Calculate** group on the **Sell** tab of the Action Pane.</span></span> <span data-ttu-id="b9259-139">ดังนั้น ข้อมูลนี้จะช่วยให้คุณเข้าใจอย่างแท้จริงว่าปุ่มใดจะถูกทริกเกอร์โดยการดำเนินการค้นหา (ถ้าคุณเลือกปุ่มนั้นในรายการผลลัพธ์)</span><span class="sxs-lookup"><span data-stu-id="b9259-139">Therefore, this information helps you understand exactly which button will be triggered by action search (if you select that button in the results list).</span></span>

<span data-ttu-id="b9259-140">[![ฟิลด์การดำเนินการค้นหากับข้อมูล](./media/action-search-field-with-data.png)](./media/action-search-field-with-data.png)</span><span class="sxs-lookup"><span data-stu-id="b9259-140">[![action-search-field-with-data](./media/action-search-field-with-data.png)](./media/action-search-field-with-data.png)</span></span>

<span data-ttu-id="b9259-141">ในตัวอย่างก่อนหน้านี้ การดำเนินการค้นหาการแสดงข้อมูลผลลัพธ์จากบานหน้าต่างการดำเนินการมาตรฐานที่ด้านบนของหน้า</span><span class="sxs-lookup"><span data-stu-id="b9259-141">In the previous example, action search showed results from the standard Action Pane at the top of a page.</span></span> <span data-ttu-id="b9259-142">อย่างไรก็ตาม การค้นหาการดำเนินยังแสดงผลลัพธ์จากแถบเครื่องมือที่สามารถมองเห็นได้ ซึ่งอยู่ในตำแหน่งอื่นๆ ในหน้าด้วย</span><span class="sxs-lookup"><span data-stu-id="b9259-142">However, action search also shows results from visible toolbars that are in other places on the page.</span></span> <span data-ttu-id="b9259-143">ตัวอย่างเช่น คุณกำลังค้นหาปุ่ม **สินค้าคงคลังคงเหลือ** ที่อยู่บน FastTab **รายการใบสั่งขาย**</span><span class="sxs-lookup"><span data-stu-id="b9259-143">For example, you're searching for the **On-hand inventory** button that is on the **Sales order lines** FastTab.</span></span> <span data-ttu-id="b9259-144">ในกรณีนี้ พาธปุ่มในรายการผลลัพธ์ (**รายการใบสั่งขาย** &gt; **สินค้าคงคลัง** &gt; **มุมมอง**) จะแจ้งให้คุณทราบว่า ปุ่มนี้อยู่อยู่ใต้หัวข้อ **มุมมอง** บนปุ่มเมนู **สินค้าคงคลัง** บน FastTab **รายการใบสั่งขาย**</span><span class="sxs-lookup"><span data-stu-id="b9259-144">In this case, the button path in the results list (**Sales order lines** &gt; **Inventory** &gt; **View**) informs you that this button is under the **View** heading on the **Inventory** menu button on the **Sales order lines** FastTab.</span></span>

<span data-ttu-id="b9259-145">[![ปริมาณคงคลังคงเหลือ](./media/on-hand-inventory.png)](./media/on-hand-inventory.png)</span><span class="sxs-lookup"><span data-stu-id="b9259-145">[![on-hand-inventory](./media/on-hand-inventory.png)](./media/on-hand-inventory.png)</span></span>

> [!NOTE]
> <span data-ttu-id="b9259-146">มีปุ่มบางปุ่มที่ไม่แสดงในการค้นหาการดำเนินการ</span><span class="sxs-lookup"><span data-stu-id="b9259-146">There are some buttons that do not show up in Action search.</span></span> <span data-ttu-id="b9259-147">ซึ่งรวมถึงปุ่มกล่องโต้ตอบและปุ่มต่างๆ จากฟอร์มย่อย</span><span class="sxs-lookup"><span data-stu-id="b9259-147">These include drop dialog buttons and buttons from subforms.</span></span> 

## <a name="action-search-vs-navigation-search"></a><span data-ttu-id="b9259-148">การดำเนินการค้นหาเปรียบเทียบกับการค้นหาการนำทาง</span><span class="sxs-lookup"><span data-stu-id="b9259-148">Action search vs. Navigation search</span></span>

<span data-ttu-id="b9259-149">ในขณะที่การดำเนินการค้นหามีวัตถุประสงค์เพื่อค้นหาและเรียกใช้การดำเนินการในเพจ มีกลไกการค้นหาที่แยกต่างหาก สำหรับการค้นหาและการนำทางไปยังเพจต่าง ๆ</span><span class="sxs-lookup"><span data-stu-id="b9259-149">Whereas action search is intended to find and run actions on a page, there is a separate search mechanism for finding and navigating to pages.</span></span> <span data-ttu-id="b9259-150">ให้ดูข้อมูลเพิ่มเติมเกี่ยวกับคุณลักษณะนั้นที่บทความ [การค้นหาการนำทาง](navigation-search.md)</span><span class="sxs-lookup"><span data-stu-id="b9259-150">For more information about that feature, see the [Navigation search](navigation-search.md) article.</span></span>


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]