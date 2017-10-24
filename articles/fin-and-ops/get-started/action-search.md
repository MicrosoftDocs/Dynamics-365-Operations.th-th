---
title: "การดำเนินการค้นหา"
description: "บทความนี้อธิบายถึงฟังก์ชันการดำเนินการค้นหาใน Microsoft Dynamics 365 for Finance and Operations การดำเนินการค้นหาจะช่วยคุณค้นหาและดำเนินการที่เรียกใช้บนหน้า"
author: jasongre
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: sericks
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 62303
ms.assetid: 62c70de0-fdde-4417-8e08-0583fb095a40
ms.search.region: Global
ms.author: jasongre
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 9b9bb0acc6f0dc1722c916f133eed766ffdd4cc8
ms.contentlocale: th-th
ms.lasthandoff: 09/29/2017

---

# <a name="action-search"></a><span data-ttu-id="573a9-104">การดำเนินการค้นหา</span><span class="sxs-lookup"><span data-stu-id="573a9-104">Action search</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="573a9-105">บทความนี้อธิบายถึงฟังก์ชันการดำเนินการค้นหาใน Microsoft Dynamics 365 for Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="573a9-105">This article describes the action search functionality in Microsoft Dynamics 365 for Finance and Operations.</span></span> <span data-ttu-id="573a9-106">การดำเนินการค้นหาจะช่วยคุณค้นหาและดำเนินการที่เรียกใช้บนหน้า</span><span class="sxs-lookup"><span data-stu-id="573a9-106">Action search will help you find and run actions on a page.</span></span>

<a name="introduction"></a><span data-ttu-id="573a9-107">คำนำ</span><span class="sxs-lookup"><span data-stu-id="573a9-107">Introduction</span></span>
------------

<span data-ttu-id="573a9-108">หน้าใน Microsoft Dynamics 365 for Finance and Operations โดยหลักๆ แล้วจะแสดงคำสั่งในบานหน้าต่างการดำเนินการ ทั้งบานหน้าต่างการดำเนินการมาตรฐานที่ปรากฏขึ้นที่ด้านบนของหน้าและแถบเครื่องมือที่ปรากฏในส่วนต่างๆ ของหน้า</span><span class="sxs-lookup"><span data-stu-id="573a9-108">Pages in Microsoft Dynamics 365 for Finance and Operations primarily expose commands on Action Panes, both the standard Action Pane that appears at the top of a page and the toolbars that appear in various sections of the page.</span></span> <span data-ttu-id="573a9-109">ในเวอร์ชันก่อนหน้า คุณลักษณะคำแนะนำของคีย์ช่วยให้คุณสามารถเข้าถึงปุ่มใดๆ บนหน้าต่างการดำเนินการได้อย่างรวดเร็ว โดยการกดคีย์ Alt แล้วกดชุดของตัวอักษร</span><span class="sxs-lookup"><span data-stu-id="573a9-109">In previous versions, a Key Tips feature let you quickly access any button on an Action Pane by pressing the Alt key and then a series of letters.</span></span> 

<span data-ttu-id="573a9-110">[![keyTipsAX6](./media/keytipsax6.png)](./media/keytipsax6.png) อย่างไรก็ตาม ในเวอร์ชันปัจจุบันของ Finance and Operations คำแนะนำของคีย์ไม่มีการใช้งานอีกต่อไป แต่ถูกแทนที่โดยคุณลักษณะการค้นหาการดำเนินการ</span><span class="sxs-lookup"><span data-stu-id="573a9-110">[![keyTipsAX6](./media/keytipsax6.png)](./media/keytipsax6.png) However, in the current version of Finance and Operations, Key Tips are no longer available but have been replaced by the action search feature.</span></span> <span data-ttu-id="573a9-111">คุณลักษณะใหม่นี้ช่วยให้คุณค้นหาและเรียกใช้งานปุ่มจากบานหน้าต่างการดำเนินการที่มองเห็นได้ได้ๆได้อย่างรวดเร็ว</span><span class="sxs-lookup"><span data-stu-id="573a9-111">This new feature lets you quickly search for and run a button from any visible Action Pane.</span></span>

## <a name="using-action-search"></a><span data-ttu-id="573a9-112">การใช้การดำเนินการค้นหา</span><span class="sxs-lookup"><span data-stu-id="573a9-112">Using action search</span></span>
<span data-ttu-id="573a9-113">เพื่อใช้คุณลักษณะการดำเนินการค้นหา ให้ปฏิบัติดังนี้</span><span class="sxs-lookup"><span data-stu-id="573a9-113">To use the action search feature, follow these steps.</span></span>

1.  <span data-ttu-id="573a9-114">ในบานหน้าต่างการดำเนินการ ให้คลิกในฟิลด์ **การดำเนินการค้นหา**</span><span class="sxs-lookup"><span data-stu-id="573a9-114">On the Action Pane, click in the **action search** field.</span></span> <span data-ttu-id="573a9-115">(ฟิลด์ **การดำเนินการค้นหา** ประกอบด้วยไอคอนแว่นขยาย)</span><span class="sxs-lookup"><span data-stu-id="573a9-115">(The **action search** field contains a magnifying glass icon.)</span></span>
2.  <span data-ttu-id="573a9-116">พิมพ์ชื่อของปุ่มทั้งหมดหรือบางส่วนที่คุณต้องการดำเนินงาน</span><span class="sxs-lookup"><span data-stu-id="573a9-116">Type all or part of the name of the button that you want to run.</span></span> <span data-ttu-id="573a9-117">คุณยังสามารถค้นหาโดยการใช้คำจากปุ่ม "เส้นทาง" ได้อีกด้วย</span><span class="sxs-lookup"><span data-stu-id="573a9-117">You can also search by using words from the button's "path."</span></span> <span data-ttu-id="573a9-118">(สำหรับข้อมูลเพิ่มเติม ให้ดูที่ส่วนถัดไปของบทความนี้) โดยทั่วไป ปุ่มจะปรากฏขึ้นใกล้กับด้านบนของรายการผลลัพธ์หลังจากที่คุณได้พิมพ์อักขระสองถึงสี่ตัว</span><span class="sxs-lookup"><span data-stu-id="573a9-118">(For more information, see the next section of this article.) Typically, a button will appear near the top of the results list after you've typed two to four characters.</span></span>
3.  <span data-ttu-id="573a9-119">ค้นหาและเรียกใช้ปุ่มในรายการผลลัพธ์ (โดยการใช้เมาส์หรือแป้นพิมพ์ของคุณ)</span><span class="sxs-lookup"><span data-stu-id="573a9-119">Find and run the button in the results list (by using your mouse or keyboard).</span></span>

<span data-ttu-id="573a9-120">หลังจากเรียกใช้ปุ่ม โฟกัสจะถูกส่งกลับไปยังตำแหน่งสุดท้ายของคุณบนหน้า เพื่อให้คุณสามารถทำงานต่อไปได้</span><span class="sxs-lookup"><span data-stu-id="573a9-120">After the button is run, the focus is returned to your last position on the page, so that you can continue to work.</span></span> 

<span data-ttu-id="573a9-121">[![ฟิลด์การดำเนินการค้นหา](./media/action-search-field.png)](./media/action-search-field.png)</span><span class="sxs-lookup"><span data-stu-id="573a9-121">[![action-search-field](./media/action-search-field.png)](./media/action-search-field.png)</span></span>

<span data-ttu-id="573a9-122">คุณยังสามารถเริ่มต้นการดำเนินการค้นหา ด้วยการกด Ctrl+/ or Alt+Q ได้</span><span class="sxs-lookup"><span data-stu-id="573a9-122">You can also start action search by pressing Ctrl+/ or Alt+Q.</span></span> <span data-ttu-id="573a9-123">กดแป้นพิมพ์ลัดอีกครั้งเพื่อกลับโฟกัสไปยังตำแหน่งสุดท้ายของคุณบนหน้า</span><span class="sxs-lookup"><span data-stu-id="573a9-123">Press the keyboard shortcut again to return the focus to your last position on the page.</span></span>

## <a name="understanding-the-results-list"></a><span data-ttu-id="573a9-124">การทำความเข้าใจเกี่ยวกับรายการผลลัพธ์</span><span class="sxs-lookup"><span data-stu-id="573a9-124">Understanding the results list</span></span>
<span data-ttu-id="573a9-125">ใน Finance and Operations คุณมักจะต้องทราบทั้งที่ตั้งและบริบทของปุ่มเพื่อให้เข้าใจถึงวัตถุประสงค์ของปุ่มนั้นอย่างแท้จริง</span><span class="sxs-lookup"><span data-stu-id="573a9-125">Often, in Finance and Operations, you must know both the location and the context of a button to fully understand the purpose of that button.</span></span> <span data-ttu-id="573a9-126">ดังนั้น ข้อมูลเพิ่มเติมจะถูกแสดงสำหรับสินค้าแต่ละรายการในรายการผลลัพธ์ เพื่อช่วยให้คุณเข้าใจทุกประการว่าปุ่มใดปรากฏขึ้นในรายการ</span><span class="sxs-lookup"><span data-stu-id="573a9-126">Therefore, additional information is shown for each item in the results list, to help you understand exactly which buttons appear in the list.</span></span> <span data-ttu-id="573a9-127">โดยเฉพาะอย่างยิ่ง "พาธ"ของปุ่มจะถูกแสดง</span><span class="sxs-lookup"><span data-stu-id="573a9-127">In particular, the "path" of the button is shown.</span></span> <span data-ttu-id="573a9-128">พาธนี้อาจรวมถึงป้ายชื่อขององค์ประกอบ UI ต่อไปนี้ ตามที่เกี่ยวข้อง:</span><span class="sxs-lookup"><span data-stu-id="573a9-128">This path might include the labels of the following UI elements, as relevant:</span></span>

-   <span data-ttu-id="573a9-129">แท็บบานหน้าต่างการดำเนินการ</span><span class="sxs-lookup"><span data-stu-id="573a9-129">Action Pane tab</span></span>
-   <span data-ttu-id="573a9-130">กลุ่มของปุ่ม</span><span class="sxs-lookup"><span data-stu-id="573a9-130">Button group</span></span>
-   <span data-ttu-id="573a9-131">ปุ่มเมนู (ถ้าปุ่มอยู่ภายในปุ่มเมนู)</span><span class="sxs-lookup"><span data-stu-id="573a9-131">Menu button (if the button is inside a menu button)</span></span>
-   <span data-ttu-id="573a9-132">ตัวแบ่งเมนู (ถ้ามีปุ่มอยู่ภายในกลุ่มมีชื่อภายในปุ่มเมนู)</span><span class="sxs-lookup"><span data-stu-id="573a9-132">Menu separator (if the button is inside a named group inside a menu button)</span></span>
-   <span data-ttu-id="573a9-133">กลุ่มหรือแท็บบนหน้า (ตัวอย่างเช่น ชื่อของ FastTab)</span><span class="sxs-lookup"><span data-stu-id="573a9-133">Group or tab on the page (for example, the name of a FastTab)</span></span>

<span data-ttu-id="573a9-134">ตัวอย่างเช่น คุณพิมพ์ **tot** ในฟิลด์ **การดำเนินการค้นหา** และขณะนี้กำลังตรวจสอบรายการผลลัพธ์</span><span class="sxs-lookup"><span data-stu-id="573a9-134">For example, you typed **tot** in the **action search** field and are now examining the results list.</span></span> <span data-ttu-id="573a9-135">รายการแรก สำหรับปุ่มที่ชื่อ **ผลรวม** จะถูกเน้น</span><span class="sxs-lookup"><span data-stu-id="573a9-135">The first entry, for a button that is named **Totals**, is highlighted.</span></span> <span data-ttu-id="573a9-136">พาธปุ่มของ **ใบสั่งขาย** &gt; **ดู** ยังจะปรากฏขึ้นด้วย</span><span class="sxs-lookup"><span data-stu-id="573a9-136">A button path of **Sales order** &gt; **View** is also shown.</span></span> <span data-ttu-id="573a9-137">ส่วน **ใบสั่งขาย** ของเส้นทางตรงกับแท็บ **ใบสั่งขาย** บนบานหน้าต่างการดำเนินการ และส่วน **มุมมอง** ของเส้นทางตรงกับกลุ่ม **มุมมอง** บนแท็บนั้น ในทำนองเดียวกัน ส่วนของปุ่ม **ส่วนลดรวม** (**ขาย** &gt; **คำนวณ**) จะแจ้งให้คุณทราบว่าปุ่มนี้อยู่ในกลุ่ม **คำนวณ** บนแท็บ **ขาย** ของบานหน้าต่างการดำเนินการ</span><span class="sxs-lookup"><span data-stu-id="573a9-137">The **Sales order** part of the path corresponds to the **Sales order** tab on the Action Pane, and the **View** part of the path corresponds to the **View** group on that tab. Similarly, the path of the **Total discount** button (**Sell** &gt; **Calculate**) informs you that this button is located in the **Calculate** group on the **Sell** tab of the Action Pane.</span></span> <span data-ttu-id="573a9-138">ดังนั้น ข้อมูลนี้จะช่วยให้คุณเข้าใจอย่างแท้จริงว่าปุ่มใดจะถูกทริกเกอร์โดยการดำเนินการค้นหา (ถ้าคุณเลือกปุ่มนั้นในรายการผลลัพธ์)</span><span class="sxs-lookup"><span data-stu-id="573a9-138">Therefore, this information helps you understand exactly which button will be triggered by action search (if you select that button in the results list).</span></span> 

<span data-ttu-id="573a9-139">[![ฟิลด์การดำเนินการค้นหากับข้อมูล](./media/action-search-field-with-data.png)](./media/action-search-field-with-data.png)</span><span class="sxs-lookup"><span data-stu-id="573a9-139">[![action-search-field-with-data](./media/action-search-field-with-data.png)](./media/action-search-field-with-data.png)</span></span> 

<span data-ttu-id="573a9-140">ในตัวอย่างก่อนหน้านี้ การดำเนินการค้นหาการแสดงข้อมูลผลลัพธ์จากบานหน้าต่างการดำเนินการมาตรฐานที่ด้านบนของหน้า</span><span class="sxs-lookup"><span data-stu-id="573a9-140">In the previous example, action search showed results from the standard Action Pane at the top of a page.</span></span> <span data-ttu-id="573a9-141">อย่างไรก็ตาม การดำเนินการค้นหายังแสดงผลลัพธ์จากแถบเครื่องมือที่สามารถมองเห็นได้ซึ่งตั้งอยู่ในตำแหน่งอื่นๆในหน้าด้วย</span><span class="sxs-lookup"><span data-stu-id="573a9-141">However, action search also shows results from visible toolbars that are located in other places on the page.</span></span> <span data-ttu-id="573a9-142">ตัวอย่างเช่น คุณกำลังค้นหาปุ่ม **สินค้าคงคลังคงเหลือ** ที่ตั้งอยู่บน FastTab **รายการใบสั่งขาย**</span><span class="sxs-lookup"><span data-stu-id="573a9-142">For example, you're searching for the **On-hand inventory** button that is located on the **Sales order lines** FastTab.</span></span> <span data-ttu-id="573a9-143">ในกรณีนี้ พาธปุ่มในรายการผลลัพธ์ (**รายการใบสั่งขาย** &gt; **สินค้าคงคลัง** &gt; **มุมมอง**) จะแจ้งให้คุณทราบว่า ปุ่มนี้อยู่ถูกตั้งอยู่ใต้หัวข้อ **มุมมอง** บนปุ่มเมนู **สินค้าคงคลัง** บน FastTab **รายการใบสั่งขาย**</span><span class="sxs-lookup"><span data-stu-id="573a9-143">In this case, the button path in the results list (**Sales order lines** &gt; **Inventory** &gt; **View**) informs you that this button is located under the **View** heading on the **Inventory** menu button on the **Sales order lines** FastTab.</span></span> 

<span data-ttu-id="573a9-144">[![ปริมาณคงคลังคงเหลือ](./media/on-hand-inventory.png)](./media/on-hand-inventory.png)</span><span class="sxs-lookup"><span data-stu-id="573a9-144">[![on-hand-inventory](./media/on-hand-inventory.png)](./media/on-hand-inventory.png)</span></span>

## <a name="action-search-vs-navigation-search"></a><span data-ttu-id="573a9-145">การดำเนินการค้นหาเปรียบเทียบกับการค้นหาการนำทาง</span><span class="sxs-lookup"><span data-stu-id="573a9-145">Action search vs. Navigation search</span></span>
<span data-ttu-id="573a9-146">ในขณะที่การดำเนินการค้นหามีวัตถุประสงค์เพื่อค้นหาและเรียกใช้การดำเนินการในหน้า มีกลไกการค้นหาที่แยกต่างหากสำหรับการค้นหาและการนำทางไปยังหน้าใน Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="573a9-146">Whereas action search is intended to find and run actions on a page, there is a separate search mechanism for finding and navigating to pages in Finance and Operations.</span></span> <span data-ttu-id="573a9-147">ให้ดูข้อมูลเพิ่มเติมเกี่ยวกับคุณลักษณะนั้นที่บทความ [การค้นหาการนำทาง](navigation-search.md)</span><span class="sxs-lookup"><span data-stu-id="573a9-147">For more information about that feature, see the [Navigation search](navigation-search.md) article.</span></span>




