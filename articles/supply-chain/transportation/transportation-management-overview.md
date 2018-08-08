---
title: "ภาพรวมการจัดการการขนส่ง"
description: "หัวข้อนี้ให้ภาพรวมของฟังก์ชันการจัดการขนส่งใน Microsoft Dynamics 365 for Finance and Operations"
author: MarkusFogelberg
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: TMSParameters,TMSRateRouteWorkbench, WHSLoadPlanningWorkbench
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 30251
ms.assetid: d4e3550c-bca8-469c-82df-56ac0083e4ac
ms.search.region: Global
ms.author: mafoge
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 1d98cbff30620256c9d13e7b4a90314db150e33e
ms.openlocfilehash: 918167a3ab72b3d3665cf710d8e509417b94a056
ms.contentlocale: th-th
ms.lasthandoff: 08/07/2018

---

# <a name="transportation-management-overview"></a><span data-ttu-id="3dfa5-103">ภาพรวมการจัดการการขนส่ง</span><span class="sxs-lookup"><span data-stu-id="3dfa5-103">Transportation management overview</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="3dfa5-104">หัวข้อนี้ให้ภาพรวมของฟังก์ชันการจัดการขนส่งใน Microsoft Dynamics 365 for Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="3dfa5-104">This topic gives an overview of the transportation management functionality in Microsoft Dynamics 365 for Finance and Operations.</span></span>

<span data-ttu-id="3dfa5-105">การจัดการการขนส่งช่วยให้คุณสามารถจัดการการขนส่งของบริษัทได้ และยังช่วยให้คุณสามารถระบุผู้จัดจำหน่ายและโซลูชันสายงานการผลิตสำหรับใบสั่งขาเข้าและขาออก</span><span class="sxs-lookup"><span data-stu-id="3dfa5-105">Transportation management lets you use your company’s transportation, and also lets you identify vendor and routing solutions for inbound and outbound orders.</span></span> <span data-ttu-id="3dfa5-106">ตัวอย่างเช่น คุณสามารถระบุเส้นทางที่เร็วที่สุดหรืออัตรามีราคาแพงน้อยที่สุดสำหรับการจัดส่ง</span><span class="sxs-lookup"><span data-stu-id="3dfa5-106">For example, you can identify the fastest route or the least expensive rate for a shipment.</span></span> <span data-ttu-id="3dfa5-107">ตารางต่อไปนี้ แสดงสถานการณ์จำลองหลักสำหรับการใช้การจัดการการขนส่งที่มีอยู่ใน Microsoft Dynamics 365 for Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="3dfa5-107">The following table describes the main scenarios for using Transportation management in Microsoft Dynamics 365 for Finance and Operations.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="3dfa5-108">สถานการณ์จำลอง</span><span class="sxs-lookup"><span data-stu-id="3dfa5-108">Scenario</span></span></th>
<th><span data-ttu-id="3dfa5-109">วิธีที่การจัดการการขนส่งสามารถช่วยเหลือได้</span><span class="sxs-lookup"><span data-stu-id="3dfa5-109">How Transportation management can help</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="3dfa5-110">ใช้ตัวให้บริการโลจิสทิกภายนอกสำหรับกิจกรรมการขนส่ง</span><span class="sxs-lookup"><span data-stu-id="3dfa5-110">Use external logistics providers for transportation activities.</span></span></td>
<td><span data-ttu-id="3dfa5-111">ใช้จัดการการขนส่งสำหรับการขนส่งขาเข้าและ/หรือขาออก</span><span class="sxs-lookup"><span data-stu-id="3dfa5-111">Use Transportation management for inbound and/or outbound transportation.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="3dfa5-112">ฟลีทของ&#39;บริษัทเองจะพร้อมใช้งานสำหรับการจัดส่ง/การเบิกสินค้า และจะมีการส่งผ่านค่าธรรมเนียมการจัดส่งให้แก่ลูกค้า</span><span class="sxs-lookup"><span data-stu-id="3dfa5-112">The company&#39;s own fleet is available for delivery/pickup, and delivery charges are passed on to customers.</span></span></td>
<td><span data-ttu-id="3dfa5-113">สำหรับกระบวนการขาออก คุณสามารถใช้การจัดการการขนส่งเพื่อกำหนดค่าธรรมเนียมการขนส่ง และส่งต่อไปที่ลูกค้า</span><span class="sxs-lookup"><span data-stu-id="3dfa5-113">For the outbound processes, you can use Transportation management to determine the transportation charges and pass them on to customers.</span></span> <span data-ttu-id="3dfa5-114">อย่างไรก็ตาม กระบวนการกระทบยอดใบแจ้งหนี้ผู้ขนส่งนั้นไม่&#39;จำเป็น</span><span class="sxs-lookup"><span data-stu-id="3dfa5-114">However, the carrier invoice reconciliation process isn&#39;t required.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="3dfa5-115">ฟลีทของ&#39;บริษัทเองจะพร้อมใช้งานสำหรับการจัดส่ง/การเบิกสินค้า แต่ค่าธรรมเนียมการจัดส่งไม่ได้&#39;ถูกส่งผ่านให้แก่ลูกค้า เนื่องจากราคาผลิตภัณฑ์รวมการขนส่ง</span><span class="sxs-lookup"><span data-stu-id="3dfa5-115">The company&#39;s own fleet is available for delivery/pickup, but delivery charges aren&#39;t passed on to customers, because product prices include transportation.</span></span></td>
<td><span data-ttu-id="3dfa5-116">ฟังก์ชันการจัดการขนส่งจำนวนมากไม่&#39;จำเป็น</span><span class="sxs-lookup"><span data-stu-id="3dfa5-116">A lot of the Transportation management functionality isn&#39;t required.</span></span> <span data-ttu-id="3dfa5-117">อย่างไรก็ตาม คุณสามารถใช้จัดการการขนส่งเพื่อกำหนดอัตราการขนส่ง และปรับปรุงราคาขายให้สอดคล้องกัน</span><span class="sxs-lookup"><span data-stu-id="3dfa5-117">However, you can use Transportation management to determine the transportation rates and adjust the sales price accordingly.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="3dfa5-118">บริการโลจิสทิกได้รับจากนิติบุคคลอื่นในบริษัทเดียวกัน</span><span class="sxs-lookup"><span data-stu-id="3dfa5-118">Logistics service is provided by another legal entity in the same company.</span></span></td>
<td><ul>
<li><span data-ttu-id="3dfa5-119">คุณสามารถใช้การจัดการการขนส่ง โดยปฏิบัติต่อนิติบุคคลอื่น ๆ เหมือนกับผู้ขนส่งสินค้าอื่น ๆ</span><span class="sxs-lookup"><span data-stu-id="3dfa5-119">You can use Transportation management by treating the other legal entity like any other shipping carrier.</span></span> <span data-ttu-id="3dfa5-120">คุณไม่&#39;สามารถทำธุรกรรมทางเศรษฐกิจระหว่างนิติบุคคลให้เป็นแบบอัตโนมัติได้</span><span class="sxs-lookup"><span data-stu-id="3dfa5-120">You can&#39;t automate the economic transactions between legal entities.</span></span> <span data-ttu-id="3dfa5-121">ดังนั้น คุณต้องจัดการกับธุรกรรมเหล่านี้ด้วยตนเอง (ตัวอย่างเช่น ด้วยการสร้างใบสั่งซื้อ)</span><span class="sxs-lookup"><span data-stu-id="3dfa5-121">Therefore, you must handle these transactions manually (for example, by creating a purchase order).</span></span></li>
<li><span data-ttu-id="3dfa5-122">ในนิติบุคคลที่ให้บริการโลจิสทิก สามารถใช้การจัดการการขนส่งในการกำหนดอัตราการขนส่งได้</span><span class="sxs-lookup"><span data-stu-id="3dfa5-122">In the legal entity that provides the logistics services, Transportation management can be used to determine transportation rates.</span></span></li>
</ul></td>
</tr>
</tbody>
</table>

## <a name="planning-transportation-in-finance-and-operations"></a><span data-ttu-id="3dfa5-123">การวางแผนการขนส่งใน Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="3dfa5-123">Planning transportation in Finance and Operations</span></span>
<span data-ttu-id="3dfa5-124">ในการจัดการการขนส่ง การวางแผนการขนส่งอาจเป็นไปตามใบสั่ง หรือตามการจัดส่งที่ถูกสร้างขึ้นตามใบสั่งเหล่านั้นได้</span><span class="sxs-lookup"><span data-stu-id="3dfa5-124">In Transportation management, transportation planning can be based either on orders or on the shipments that are created based on those orders.</span></span> <span data-ttu-id="3dfa5-125">การจัดส่งจะมีอยู่ ณจุดใดจุดหนึ่งในเวลาเสมอ แต่ไม่จำเป็นสำหรับการวางแผนการขนส่ง</span><span class="sxs-lookup"><span data-stu-id="3dfa5-125">The shipments always exist at some point in time but aren't required for transportation planning.</span></span> <span data-ttu-id="3dfa5-126">ใบสั่งโอนย้ายเป็นส่วนหนึ่งของสถานการณ์จำลองขาออก และสามารถวางแผนร่วมกับใบสั่งขายได้</span><span class="sxs-lookup"><span data-stu-id="3dfa5-126">Transfer orders are part of the outbound scenario and can be planned together with sales orders.</span></span> 

![ภาพร่างของโหลด](./media/Load-drawing1-1024x477.jpg)

## <a name="inbound-transportation"></a><span data-ttu-id="3dfa5-128">การขนส่งขาเข้า</span><span class="sxs-lookup"><span data-stu-id="3dfa5-128">Inbound transportation</span></span>
<span data-ttu-id="3dfa5-129">เมื่อคุณสั่งสินค้าจากผู้จัดจำหน่าย และจำเป็นต้องส่งสินค้าไปยังคลังสินค้าของคุณ คุณอาจต้องการจัดเตรียมการขนส่งสินค้าด้วยตัวคุณเอง</span><span class="sxs-lookup"><span data-stu-id="3dfa5-129">When you order items from a vendor, and the items must be delivered to your warehouse, you might want to arrange the transport of the items yourself.</span></span> <span data-ttu-id="3dfa5-130">คุณสามารถใช้ Finance and Operations สำหรับการวางแผนการขนส่งและการรับการบรรทุกขาเข้า</span><span class="sxs-lookup"><span data-stu-id="3dfa5-130">You can use Finance and Operations to plan the transportation and receipt of the inbound load.</span></span> <span data-ttu-id="3dfa5-131">ภาพประกอบต่อไปนี้ แสดงลำดับกระบวนการทางธุรกิจสำหรับการวางแผนการขนส่งการบรรทุกขาเข้า</span><span class="sxs-lookup"><span data-stu-id="3dfa5-131">The following illustration shows the business process flow for planning transportation for an inbound load.</span></span> 

![กระบวนการทางธุรกิจสำหรับการขนส่งการบรรทุกขาเข้า](./media/Businessprocessflowforinboundloadtransportation.jpg)

## <a name="outbound-transportation"></a><span data-ttu-id="3dfa5-133">การขนส่งขาออก</span><span class="sxs-lookup"><span data-stu-id="3dfa5-133">Outbound transportation</span></span>
<span data-ttu-id="3dfa5-134">คุณสามารถวางแผน และดำเนินการบรรทุกขาออกเพื่อจัดส่งสินค้าเฉพาะจากคลังสินค้าของบริษัทให้กับลูกค้า</span><span class="sxs-lookup"><span data-stu-id="3dfa5-134">You can plan and process an outbound load to ship specific items from a company’s warehouse to a customer.</span></span> <span data-ttu-id="3dfa5-135">คุณสามารถใช้ Finance and Operations สำหรับการวางแผนการขนส่งและการจัดส่งสินค้าของโหลดขาออก</span><span class="sxs-lookup"><span data-stu-id="3dfa5-135">You can use Finance and Operations to plan the transportation and shipping of an outbound load.</span></span> <span data-ttu-id="3dfa5-136">ภาพประกอบต่อไปนี้ แสดงลำดับกระบวนการทางธุรกิจสำหรับการวางแผนและการดำเนินการขนส่งการบรรทุกขาออกสำหรับการจัดส่ง</span><span class="sxs-lookup"><span data-stu-id="3dfa5-136">The following illustration shows the business process flow for planning and processing outbound loads for shipping.</span></span> 

![การวางแผนและการประมวลผลโหลดขาออก](./media/Planningandprocessingoutboundloads.jpg)

## <a name="load-building"></a><span data-ttu-id="3dfa5-138">การสร้างการบรรทุก</span><span class="sxs-lookup"><span data-stu-id="3dfa5-138">Load building</span></span>
<span data-ttu-id="3dfa5-139">Finance and Operations แสดงกลยุทธ์การสร้างการบรรทุกที่ชื่อกลยุทธ์การสร้างการบรรทุกตามปริมาตร</span><span class="sxs-lookup"><span data-stu-id="3dfa5-139">Finance and Operations provides a load building strategy that is named the Volume-based load building strategy.</span></span> <span data-ttu-id="3dfa5-140">กลยุทธ์นี้ช่วยให้คุณสามารถใช้ค่าสูงสุดที่ระบุสำหรับความสูงและน้ำหนักในเท็มเพลตของโหลด หรือคุณสามารถแทนที่การตั้งค่าโดยการป้อนค่าใหม่</span><span class="sxs-lookup"><span data-stu-id="3dfa5-140">This strategy lets you use the maximum values that are specified for height and weight in the load template, or you can override the settings by entering new values.</span></span> <span data-ttu-id="3dfa5-141">ในการใช้กลยุทธ์นี้ เลือกฟิลด์ **กลยุทธ์การสร้างการบรรทุก** ในแท็บด่วน **ตั้งค่า** บนหน้า **เวิร์กเบนช์การสร้างการบรรทุก** ได้</span><span class="sxs-lookup"><span data-stu-id="3dfa5-141">To use this strategy, select it in the **Load building strategy** field on the **Setup** FastTab on the **Load building workbench** page.</span></span> <span data-ttu-id="3dfa5-142">นอกจากนี้ คุณสามารถเพิ่มกลยุทธ์การสร้างการบรรทุกด้วยตัวของคุณเองได้ โดยการสร้างคลาสใหม่ใน Application Object Tree (AOT)</span><span class="sxs-lookup"><span data-stu-id="3dfa5-142">In addition, you can add your own load-building strategies by creating a new class in the Application Object Tree (AOT).</span></span>




