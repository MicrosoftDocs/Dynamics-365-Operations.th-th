---
title: วางแผนจำนวนงานโดยใช้การรวมบัญชีฮับ
description: บทความนี้อธิบายคุณลักษณะของการรวมการจัดส่งในฮับเมื่อคุณจัดส่งสินค้าจากคลังสินค้าที่แตกต่างกันให้กับลูกค้าเดียวกัน หรือ เมื่อคุณได้รับสินค้าจากผู้จัดจำหน่ายหลายรายในคลังสินค้าเดียวกัน
author: MarkusFogelberg
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSLoadPlanningWorkbench
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 92273
ms.assetid: d27b0926-a534-4caf-a2a3-acbc7c440bca
ms.search.region: Global
ms.search.industry: Distribution
ms.author: mafoge
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 6743338819da3821cde18ec34a9c79290036ca23
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 05/15/2019
ms.locfileid: "1560989"
---
# <a name="plan-loads-using-hub-consolidation"></a><span data-ttu-id="5befc-103">วางแผนจำนวนงานโดยใช้การรวมบัญชีฮับ</span><span class="sxs-lookup"><span data-stu-id="5befc-103">Plan loads using hub consolidation</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="5befc-104">บทความนี้อธิบายคุณลักษณะของการรวมการจัดส่งในฮับเมื่อคุณจัดส่งสินค้าจากคลังสินค้าที่แตกต่างกันให้กับลูกค้าเดียวกัน หรือ เมื่อคุณได้รับสินค้าจากผู้จัดจำหน่ายหลายรายในคลังสินค้าเดียวกัน</span><span class="sxs-lookup"><span data-stu-id="5befc-104">This article describes the feature for consolidating shipments in a hub when you deliver goods from different warehouses to the same customer, or when you receive goods from multiple vendors in the same warehouse.</span></span>

<span data-ttu-id="5befc-105">มีการใช้ประโยชน์ในการรวมการจัดส่งในฮับเมื่อคุณจัดส่งสินค้าจากคลังสินค้าที่แตกต่างกันให้กับลูกค้าเดียวกัน หรือ เมื่อส่งสินค้าจากผู้จัดจำหน่ายหลายรายไปยังคลังสินค้าเดียวกัน</span><span class="sxs-lookup"><span data-stu-id="5befc-105">It can be useful to consolidate shipments in a hub when you deliver goods from different warehouses to the same customer, or when goods are delivered from multiple vendors to the same warehouse.</span></span>

## <a name="building-loads"></a><span data-ttu-id="5befc-106">การสร้างการบรรทุก</span><span class="sxs-lookup"><span data-stu-id="5befc-106">Building loads</span></span>
<span data-ttu-id="5befc-107">ก่อนที่คุณสามารถใช้การรวมบัญชีฮับ คุณต้องเปิดใช้งานตัวเลือก **การวางแผนในการส่งต่อ**ในหน้า **พารามิเตอร์การจัดการการขนส่ง**</span><span class="sxs-lookup"><span data-stu-id="5befc-107">Before you can use hub consolidation, you must enable the **In transit planning** option on the **Transportation management parameters** page.</span></span> <span data-ttu-id="5befc-108">นอกจากนี้คุณยังต้องสร้างฮับที่จะเกิดการรวมบัญชีขึ้น</span><span class="sxs-lookup"><span data-stu-id="5befc-108">You must also create the hubs where consolidation will occur.</span></span> <span data-ttu-id="5befc-109">ไดอะแกรมต่อไปนี้แสดงตัวอย่างของการรวมบัญชีฮับ</span><span class="sxs-lookup"><span data-stu-id="5befc-109">The following diagram shows an example of hub consolidation.</span></span> <span data-ttu-id="5befc-110">ในกรณีนี้ ใบสั่งขายจากคลังสินค้าที่แตกต่างกันจะไปยังลูกค้าเดียวกัน</span><span class="sxs-lookup"><span data-stu-id="5befc-110">In this case, sales orders from different warehouses are going to the same customer.</span></span> <span data-ttu-id="5befc-111">โหลดแบบพื้นฐานถูกสร้างขึ้นตามใบสั่งขายในลักษณะปกติ โดยใช้หน้า **เวิร์กเบนช์การวางแผนการบรรทุก**</span><span class="sxs-lookup"><span data-stu-id="5befc-111">The basic loads are created based on sales orders in the usual way, by using the **Load planning workbench** page.</span></span> <span data-ttu-id="5befc-112">เมื่อต้องการรวมโหลดสองรายการในฮับก่อนที่จะส่งไปยังลูกค้า ในหน้า **เวิร์กเบนช์การวางแผนการบรรทุก** ในฟิลด์ **การขนส่ง** เลือก **การรวมบัญชีฮับ**</span><span class="sxs-lookup"><span data-stu-id="5befc-112">To consolidate the two loads in a hub before they are delivered to the customer, on the **Load planning workbench** page, in the **Transportation** field, select **Hub consolidation**.</span></span> <span data-ttu-id="5befc-113">เมื่อคุณเลือกฮับถูกต้องสำหรับการโหลดแต่ละ ปริมาณที่จะมีฮับเป็นปลายทาง "ส่ง"</span><span class="sxs-lookup"><span data-stu-id="5befc-113">When you select the correct hub for each load, the loads will have the hub as the “drop off” destination.</span></span> <span data-ttu-id="5befc-114">นอกจากนี้คุณจะมี "บรรทัดคำขอการขนส่ง" สองรายการในส่วน **อุปสงค์และอุปทาน** ในหน้า **เวิร์กเบนช์การวางแผนการบรรทุก**</span><span class="sxs-lookup"><span data-stu-id="5befc-114">You will also have two “transportation request lines” in the **Supply and Demand** section on the **Load planning workbench** page.</span></span> <span data-ttu-id="5befc-115">จากนั้นคุณสามารถเพิ่มสองบรรทัดนี้ไปยังโหลดใหม่ได้</span><span class="sxs-lookup"><span data-stu-id="5befc-115">You can then add these two lines to a new load.</span></span> <span data-ttu-id="5befc-116">โหลดใหม่นี้จะมีทั้งบรรทัดใบสั่งขายและจะยังมีฮับเป็นที่อยู่สำหรับ "เบิกสินค้า" และลูกค้า A เป็นปลายทาง "ส่ง"</span><span class="sxs-lookup"><span data-stu-id="5befc-116">This new load will have both sales order lines, and will also have the hub as the “pick up” address and customer A as the “drop off” destination.</span></span> <span data-ttu-id="5befc-117">โหลดทั้งสามรายการจะพร้อมสำหรับการจัดอันดับและจัดเส้นทางเช่นเดียวกับโหลดอื่น ๆ</span><span class="sxs-lookup"><span data-stu-id="5befc-117">The three loads are then ready to be rated and routed like any other load.</span></span> <span data-ttu-id="5befc-118">คุณสามารถเลือกผู้ขนส่งสินค้าใดก็ได้ที่ระบบแนะนำสำหรับแต่ละโหลด</span><span class="sxs-lookup"><span data-stu-id="5befc-118">You can select whatever shipping carrier the system suggests for each load.</span></span> <span data-ttu-id="5befc-119">[![การรวมบัญชีฮับ](./media/hubconsol.jpg)](./media/hubconsol.jpg) คุณยังสามารถใช้วิธีการเดียวกันในการรวมโหลดสำหรับใบสั่งโอนย้ายหลายรายการอีกด้วย</span><span class="sxs-lookup"><span data-stu-id="5befc-119">[![Hub consolidation](./media/hubconsol.jpg)](./media/hubconsol.jpg) You can also use the same method to consolidate loads for multiple transfer orders.</span></span> <span data-ttu-id="5befc-120">ในกรณีนี้ ลูกค้า A ในแผนภาพก่อนหน้านี้คือคลังสินค้า</span><span class="sxs-lookup"><span data-stu-id="5befc-120">In this case, customer A in the preceding diagram is a warehouse.</span></span> <span data-ttu-id="5befc-121">หรือคุณสามารถรวมโหลดสำหรับใบสั่งซื้อหลายรายการ โดยที่โหลดถูกส่งจากผู้จัดจำหน่ายที่แตกต่างกันไปยังคลังสินค้าเดียวกัน</span><span class="sxs-lookup"><span data-stu-id="5befc-121">Alternatively, you can consolidate loads for multiple purchase orders, where the loads are delivered from different vendors to the same warehouse.</span></span> <span data-ttu-id="5befc-122">คุณสามารถมีฮับการรวมได้มากกว่าหนึ่งรายการ และสามารถรวมฮับหลายรายการสำหรับโหลดที่มากขึ้นที่มาจากคลังสินค้าที่แตกต่างกัน</span><span class="sxs-lookup"><span data-stu-id="5befc-122">You can have more than one consolidation hub, and can consolidate in multiple hubs for more loads that come from different warehouses.</span></span> <span data-ttu-id="5befc-123">หลังจากที่คุณสร้างโหลดพื้นฐานของคุณและใช้ตัวเลือกการรวมฮับแล้ว คุณสามารถสร้างโหลดใหม่โดยใช้บรรทัดคำขอการขนส่งแบบรวมได้</span><span class="sxs-lookup"><span data-stu-id="5befc-123">After you build your basic loads and use the hub consolidation option, you build the new loads by using the consolidated transportation request lines.</span></span> <span data-ttu-id="5befc-124">จากนั้นคุณสามารถจัดอันดับและจัดเส้นทางโหลดของคุณ</span><span class="sxs-lookup"><span data-stu-id="5befc-124">You then rate and route your loads.</span></span>



