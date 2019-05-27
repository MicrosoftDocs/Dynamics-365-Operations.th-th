---
title: การดำเนินการค้นหา
description: บทความนี้อธิบายฟังก์ชันการค้นหาการดำเนินการใน Microsoft Dynamics 365 for Finance and Operations การดำเนินการค้นหาจะช่วยคุณค้นหาและดำเนินการที่เรียกใช้บนหน้า
author: jasongre
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.custom: 62303
ms.assetid: 62c70de0-fdde-4417-8e08-0583fb095a40
ms.search.region: Global
ms.author: jasongre
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 960c715c487fbda5d93630327f07380e6d8fbd3c
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 05/15/2019
ms.locfileid: "1547042"
---
# <a name="action-search"></a><span data-ttu-id="48928-104">การค้นหาการดำเนินการ</span><span class="sxs-lookup"><span data-stu-id="48928-104">Action search</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="48928-105">บทความนี้อธิบายฟังก์ชันการค้นหาการดำเนินการใน Microsoft Dynamics 365 for Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="48928-105">This article describes the action search functionality in Microsoft Dynamics 365 for Finance and Operations.</span></span> <span data-ttu-id="48928-106">การดำเนินการค้นหาจะช่วยคุณค้นหาและดำเนินการที่เรียกใช้บนหน้า</span><span class="sxs-lookup"><span data-stu-id="48928-106">Action search will help you find and run actions on a page.</span></span>

## <a name="introduction"></a><span data-ttu-id="48928-107">คำนำ</span><span class="sxs-lookup"><span data-stu-id="48928-107">Introduction</span></span>

<span data-ttu-id="48928-108">หน้าใน Microsoft Dynamics 365 for Finance and Operations แสดงคำสั่งเป็นหลักในหน้าต่างการดำเนินการ ทั้งหน้าต่างการดำเนินการมาตรฐานที่ปรากฏที่ด้านบนของหน้าและแถบเครื่องมือที่ปรากฏในส่วนต่างๆ ของหน้า</span><span class="sxs-lookup"><span data-stu-id="48928-108">Pages in Microsoft Dynamics 365 for Finance and Operations primarily expose commands on Action Panes, both the standard Action Pane that appears at the top of a page and the toolbars that appear in various sections of the page.</span></span> <span data-ttu-id="48928-109">ในเวอร์ชันก่อนหน้า คุณลักษณะคำแนะนำของคีย์ช่วยให้คุณสามารถเข้าถึงปุ่มใดๆ บนหน้าต่างการดำเนินการได้อย่างรวดเร็ว โดยการกดคีย์ Alt แล้วกดชุดของตัวอักษร</span><span class="sxs-lookup"><span data-stu-id="48928-109">In previous versions, a Key Tips feature let you quickly access any button on an Action Pane by pressing the Alt key and then a series of letters.</span></span>

<span data-ttu-id="48928-110">[![keyTipsAX6](./media/keytipsax6.png)](./media/keytipsax6.png)</span><span class="sxs-lookup"><span data-stu-id="48928-110">[![keyTipsAX6](./media/keytipsax6.png)](./media/keytipsax6.png)</span></span>

<span data-ttu-id="48928-111">อย่างไรก็ตาม ในเวอร์ชันปัจจุบันของ Finance and Operations คำแนะนำของคีย์ไม่สามารถใช้งานอีกต่อไป แต่ถูกแทนที่โดยคุณลักษณะการค้นหาการดำเนินการ</span><span class="sxs-lookup"><span data-stu-id="48928-111">However, in the current version of Finance and Operations, Key Tips are no longer available but have been replaced by the action search feature.</span></span> <span data-ttu-id="48928-112">คุณลักษณะใหม่นี้ช่วยให้คุณค้นหาและเรียกใช้งานปุ่มจากบานหน้าต่างการดำเนินการที่มองเห็นได้ได้ๆได้อย่างรวดเร็ว</span><span class="sxs-lookup"><span data-stu-id="48928-112">This new feature lets you quickly search for and run a button from any visible Action Pane.</span></span>

## <a name="using-action-search"></a><span data-ttu-id="48928-113">การใช้การดำเนินการค้นหา</span><span class="sxs-lookup"><span data-stu-id="48928-113">Using action search</span></span>

<span data-ttu-id="48928-114">เพื่อใช้คุณลักษณะการดำเนินการค้นหา ให้ปฏิบัติดังนี้</span><span class="sxs-lookup"><span data-stu-id="48928-114">To use the action search feature, follow these steps.</span></span>

1. <span data-ttu-id="48928-115">ในบานหน้าต่างการดำเนินการ ให้คลิกในฟิลด์ **การดำเนินการค้นหา**</span><span class="sxs-lookup"><span data-stu-id="48928-115">On the Action Pane, click in the **action search** field.</span></span> <span data-ttu-id="48928-116">(ฟิลด์ **การดำเนินการค้นหา** ประกอบด้วยไอคอนแว่นขยาย)</span><span class="sxs-lookup"><span data-stu-id="48928-116">(The **action search** field contains a magnifying glass icon.)</span></span>
2. <span data-ttu-id="48928-117">พิมพ์ชื่อของปุ่มทั้งหมดหรือบางส่วนที่คุณต้องการดำเนินงาน</span><span class="sxs-lookup"><span data-stu-id="48928-117">Type all or part of the name of the button that you want to run.</span></span> <span data-ttu-id="48928-118">คุณยังสามารถค้นหาโดยการใช้คำจากปุ่ม "เส้นทาง" ได้อีกด้วย</span><span class="sxs-lookup"><span data-stu-id="48928-118">You can also search by using words from the button's "path."</span></span> <span data-ttu-id="48928-119">(สำหรับข้อมูลเพิ่มเติม ให้ดูที่ส่วนถัดไปของบทความนี้) โดยทั่วไป ปุ่มจะปรากฏขึ้นใกล้กับด้านบนของรายการผลลัพธ์หลังจากที่คุณได้พิมพ์อักขระสองถึงสี่ตัว</span><span class="sxs-lookup"><span data-stu-id="48928-119">(For more information, see the next section of this article.) Typically, a button will appear near the top of the results list after you've typed two to four characters.</span></span>
3. <span data-ttu-id="48928-120">ค้นหาและเรียกใช้ปุ่มในรายการผลลัพธ์ (โดยการใช้เมาส์หรือแป้นพิมพ์ของคุณ)</span><span class="sxs-lookup"><span data-stu-id="48928-120">Find and run the button in the results list (by using your mouse or keyboard).</span></span>

<span data-ttu-id="48928-121">หลังจากเรียกใช้ปุ่ม โฟกัสจะถูกส่งกลับไปยังตำแหน่งสุดท้ายของคุณบนหน้า เพื่อให้คุณสามารถทำงานต่อไปได้</span><span class="sxs-lookup"><span data-stu-id="48928-121">After the button is run, the focus is returned to your last position on the page, so that you can continue to work.</span></span>

<span data-ttu-id="48928-122">[![ฟิลด์การดำเนินการค้นหา](./media/action-search-field.png)](./media/action-search-field.png)</span><span class="sxs-lookup"><span data-stu-id="48928-122">[![action-search-field](./media/action-search-field.png)](./media/action-search-field.png)</span></span>

<span data-ttu-id="48928-123">คุณยังสามารถเริ่มต้นการดำเนินการค้นหา ด้วยการกด Ctrl+/ or Alt+Q ได้</span><span class="sxs-lookup"><span data-stu-id="48928-123">You can also start action search by pressing Ctrl+/ or Alt+Q.</span></span> <span data-ttu-id="48928-124">กดแป้นพิมพ์ลัดอีกครั้งเพื่อกลับโฟกัสไปยังตำแหน่งสุดท้ายของคุณบนหน้า</span><span class="sxs-lookup"><span data-stu-id="48928-124">Press the keyboard shortcut again to return the focus to your last position on the page.</span></span>

## <a name="understanding-the-results-list"></a><span data-ttu-id="48928-125">การทำความเข้าใจเกี่ยวกับรายการผลลัพธ์</span><span class="sxs-lookup"><span data-stu-id="48928-125">Understanding the results list</span></span>

<span data-ttu-id="48928-126">ใน Finance and Operations คุณมักจะต้องทราบทั้งที่ตั้งและบริบทของปุ่มเพื่อให้เข้าใจถึงวัตถุประสงค์ของปุ่มนั้นอย่างแท้จริง</span><span class="sxs-lookup"><span data-stu-id="48928-126">Often, in Finance and Operations, you must know both the location and the context of a button to fully understand the purpose of that button.</span></span> <span data-ttu-id="48928-127">ดังนั้น ข้อมูลเพิ่มเติมจะถูกแสดงสำหรับสินค้าแต่ละรายการในรายการผลลัพธ์ เพื่อช่วยให้คุณเข้าใจทุกประการว่าปุ่มใดปรากฏขึ้นในรายการ</span><span class="sxs-lookup"><span data-stu-id="48928-127">Therefore, additional information is shown for each item in the results list, to help you understand exactly which buttons appear in the list.</span></span> <span data-ttu-id="48928-128">โดยเฉพาะอย่างยิ่ง "พาธ"ของปุ่มจะถูกแสดง</span><span class="sxs-lookup"><span data-stu-id="48928-128">In particular, the "path" of the button is shown.</span></span> <span data-ttu-id="48928-129">พาธนี้อาจรวมถึงป้ายชื่อขององค์ประกอบ UI ต่อไปนี้ ตามที่เกี่ยวข้อง:</span><span class="sxs-lookup"><span data-stu-id="48928-129">This path might include the labels of the following UI elements, as relevant:</span></span>

- <span data-ttu-id="48928-130">แท็บบานหน้าต่างการดำเนินการ</span><span class="sxs-lookup"><span data-stu-id="48928-130">Action Pane tab</span></span>
- <span data-ttu-id="48928-131">กลุ่มของปุ่ม</span><span class="sxs-lookup"><span data-stu-id="48928-131">Button group</span></span>
- <span data-ttu-id="48928-132">ปุ่มเมนู (ถ้าปุ่มอยู่ภายในปุ่มเมนู)</span><span class="sxs-lookup"><span data-stu-id="48928-132">Menu button (if the button is inside a menu button)</span></span>
- <span data-ttu-id="48928-133">ตัวแบ่งเมนู (ถ้ามีปุ่มอยู่ภายในกลุ่มมีชื่อภายในปุ่มเมนู)</span><span class="sxs-lookup"><span data-stu-id="48928-133">Menu separator (if the button is inside a named group inside a menu button)</span></span>
- <span data-ttu-id="48928-134">กลุ่มหรือแท็บบนหน้า (ตัวอย่างเช่น ชื่อของ FastTab)</span><span class="sxs-lookup"><span data-stu-id="48928-134">Group or tab on the page (for example, the name of a FastTab)</span></span>

<span data-ttu-id="48928-135">ตัวอย่างเช่น คุณพิมพ์ **tot** ในฟิลด์ **การดำเนินการค้นหา** และขณะนี้กำลังตรวจสอบรายการผลลัพธ์</span><span class="sxs-lookup"><span data-stu-id="48928-135">For example, you typed **tot** in the **action search** field and are now examining the results list.</span></span> <span data-ttu-id="48928-136">รายการแรก สำหรับปุ่มที่ชื่อ **ผลรวม** จะถูกเน้น</span><span class="sxs-lookup"><span data-stu-id="48928-136">The first entry, for a button that is named **Totals**, is highlighted.</span></span> <span data-ttu-id="48928-137">พาธปุ่มของ **ใบสั่งขาย** &gt; **ดู** ยังจะปรากฏขึ้นด้วย</span><span class="sxs-lookup"><span data-stu-id="48928-137">A button path of **Sales order** &gt; **View** is also shown.</span></span> <span data-ttu-id="48928-138">ส่วน **ใบสั่งขาย** ของเส้นทางตรงกับแท็บ **ใบสั่งขาย** บนบานหน้าต่างการดำเนินการ และส่วน **มุมมอง** ของเส้นทางตรงกับกลุ่ม **มุมมอง** บนแท็บนั้น ในทำนองเดียวกัน ส่วนของปุ่ม **ส่วนลดรวม** (**ขาย** &gt; **คำนวณ**) จะแจ้งให้คุณทราบว่าปุ่มนี้อยู่ในกลุ่ม **คำนวณ** บนแท็บ **ขาย** ของบานหน้าต่างการดำเนินการ</span><span class="sxs-lookup"><span data-stu-id="48928-138">The **Sales order** part of the path corresponds to the **Sales order** tab on the Action Pane, and the **View** part of the path corresponds to the **View** group on that tab. Similarly, the path of the **Total discount** button (**Sell** &gt; **Calculate**) informs you that this button is located in the **Calculate** group on the **Sell** tab of the Action Pane.</span></span> <span data-ttu-id="48928-139">ดังนั้น ข้อมูลนี้จะช่วยให้คุณเข้าใจอย่างแท้จริงว่าปุ่มใดจะถูกทริกเกอร์โดยการดำเนินการค้นหา (ถ้าคุณเลือกปุ่มนั้นในรายการผลลัพธ์)</span><span class="sxs-lookup"><span data-stu-id="48928-139">Therefore, this information helps you understand exactly which button will be triggered by action search (if you select that button in the results list).</span></span>

<span data-ttu-id="48928-140">[![ฟิลด์การดำเนินการค้นหากับข้อมูล](./media/action-search-field-with-data.png)](./media/action-search-field-with-data.png)</span><span class="sxs-lookup"><span data-stu-id="48928-140">[![action-search-field-with-data](./media/action-search-field-with-data.png)](./media/action-search-field-with-data.png)</span></span>

<span data-ttu-id="48928-141">ในตัวอย่างก่อนหน้านี้ การดำเนินการค้นหาการแสดงข้อมูลผลลัพธ์จากบานหน้าต่างการดำเนินการมาตรฐานที่ด้านบนของหน้า</span><span class="sxs-lookup"><span data-stu-id="48928-141">In the previous example, action search showed results from the standard Action Pane at the top of a page.</span></span> <span data-ttu-id="48928-142">อย่างไรก็ตาม การดำเนินการค้นหายังแสดงผลลัพธ์จากแถบเครื่องมือที่สามารถมองเห็นได้ซึ่งตั้งอยู่ในตำแหน่งอื่นๆในหน้าด้วย</span><span class="sxs-lookup"><span data-stu-id="48928-142">However, action search also shows results from visible toolbars that are located in other places on the page.</span></span> <span data-ttu-id="48928-143">ตัวอย่างเช่น คุณกำลังค้นหาปุ่ม **สินค้าคงคลังคงเหลือ** ที่ตั้งอยู่บน FastTab **รายการใบสั่งขาย**</span><span class="sxs-lookup"><span data-stu-id="48928-143">For example, you're searching for the **On-hand inventory** button that is located on the **Sales order lines** FastTab.</span></span> <span data-ttu-id="48928-144">ในกรณีนี้ พาธปุ่มในรายการผลลัพธ์ (**รายการใบสั่งขาย** &gt; **สินค้าคงคลัง** &gt; **มุมมอง**) จะแจ้งให้คุณทราบว่า ปุ่มนี้อยู่ถูกตั้งอยู่ใต้หัวข้อ **มุมมอง** บนปุ่มเมนู **สินค้าคงคลัง** บน FastTab **รายการใบสั่งขาย**</span><span class="sxs-lookup"><span data-stu-id="48928-144">In this case, the button path in the results list (**Sales order lines** &gt; **Inventory** &gt; **View**) informs you that this button is located under the **View** heading on the **Inventory** menu button on the **Sales order lines** FastTab.</span></span>

<span data-ttu-id="48928-145">[![ปริมาณคงคลังคงเหลือ](./media/on-hand-inventory.png)](./media/on-hand-inventory.png)</span><span class="sxs-lookup"><span data-stu-id="48928-145">[![on-hand-inventory](./media/on-hand-inventory.png)](./media/on-hand-inventory.png)</span></span>

## <a name="action-search-vs-navigation-search"></a><span data-ttu-id="48928-146">การดำเนินการค้นหาเปรียบเทียบกับการค้นหาการนำทาง</span><span class="sxs-lookup"><span data-stu-id="48928-146">Action search vs. Navigation search</span></span>

<span data-ttu-id="48928-147">ในขณะที่การดำเนินการค้นหามีวัตถุประสงค์เพื่อค้นหาและเรียกใช้การดำเนินการในหน้า มีกลไกการค้นหาที่แยกต่างหากสำหรับการค้นหาและการนำทางไปยังหน้าใน Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="48928-147">Whereas action search is intended to find and run actions on a page, there is a separate search mechanism for finding and navigating to pages in Finance and Operations.</span></span> <span data-ttu-id="48928-148">ให้ดูข้อมูลเพิ่มเติมเกี่ยวกับคุณลักษณะนั้นที่บทความ [การค้นหาการนำทาง](navigation-search.md)</span><span class="sxs-lookup"><span data-stu-id="48928-148">For more information about that feature, see the [Navigation search](navigation-search.md) article.</span></span>