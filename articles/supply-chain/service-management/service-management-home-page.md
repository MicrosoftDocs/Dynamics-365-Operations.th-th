---
title: "การจัดการงานบริการ"
description: "ใช้การจัดการงานบริการเพื่อกำหนดข้อตกลงการให้บริการและการบอกรับเป็นสมาชิกการบริการ จัดการใบสั่งบริการและการสอบถามของลูกค้า และเพื่อจัดการและวิเคราะห์การจัดส่งบริการให้แก่ลูกค้า"
author: ShylaThompson
manager: AnnBe
ms.date: 05/24/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: SMAServiceOrderTable
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 
ms.assetid: 
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 80a3cb74279f72e8cb94f3a2c38230f409067a47
ms.openlocfilehash: 89035687d87c674cca7fa5fd3126100c4c0ad892
ms.contentlocale: th-th
ms.lasthandoff: 08/09/2018

---


# <a name="service-management"></a><span data-ttu-id="b3c01-103">การจัดการงานบริการ</span><span class="sxs-lookup"><span data-stu-id="b3c01-103">Service management</span></span> 

[!include [banner](../includes/banner.md)]


<span data-ttu-id="b3c01-104">ใช้ **การจัดการงานบริการ** เพื่อกำหนดข้อตกลงการให้บริการและการบอกรับเป็นสมาชิกการบริการ จัดการใบสั่งบริการและการสอบถามของลูกค้า และเพื่อจัดการและวิเคราะห์การจัดส่งบริการให้แก่ลูกค้า</span><span class="sxs-lookup"><span data-stu-id="b3c01-104">Use **Service management** to establish service agreements and service subscriptions, handle service orders and customer inquiries, and to manage and analyze the delivery of services to customers.</span></span> <span data-ttu-id="b3c01-105">คุณสามารถใช้ข้อตกลงการให้บริการเพื่อกำหนดทรัพยากรที่ใช้ในการไปเยี่ยมเพื่อให้บริการตามปกติ </span><span class="sxs-lookup"><span data-stu-id="b3c01-105">You can use service agreements to define the resources that are used in a typical service visit.</span></span> <span data-ttu-id="b3c01-106">คุณยังสามารถใช้ข้อตกลงการให้บริการเพื่อดูว่าทรัพยากรดังกล่าวจะออกอินวอยซ์ให้กับลูกค้า </span><span class="sxs-lookup"><span data-stu-id="b3c01-106">You can also use service agreements to view how those resources are invoiced to the customer.</span></span> <span data-ttu-id="b3c01-107">ข้อตกลงการให้บริการยังสามารถรวมข้อตกลงระดับการบริการที่ระบุเวลาการตอบสนองมาตรฐาน และมีเครื่องมือต่างๆ เพื่อบันทึกเวลาเกิดขึ้นจริง</span><span class="sxs-lookup"><span data-stu-id="b3c01-107">A service agreement can also include a service level agreement that specifies standard response times, and offers tools to record the actual time.</span></span>

<span data-ttu-id="b3c01-108">คุณสามารถสร้างใบสั่งบริการเพื่อจัดการข้อมูลเกี่ยวกับการจัดกำหนดการ และไม่ได้จัดกำหนดการเข้าใช้โดยช่างเทคนิคบริการไปไซต์ของลูกค้า </span><span class="sxs-lookup"><span data-stu-id="b3c01-108">You can create service orders to manage information about scheduled and unscheduled visits by a service technician to a customer site.</span></span> <span data-ttu-id="b3c01-109">ใบสั่งบริการรวมถึงข้อมูลเช่น:</span><span class="sxs-lookup"><span data-stu-id="b3c01-109">Service orders include information such as:</span></span>

1.  <span data-ttu-id="b3c01-110">จำนวนชั่วโมงของงานที่จะดำเนินการที่ช่างเทคนิคบริการ</span><span class="sxs-lookup"><span data-stu-id="b3c01-110">The hours of work that the service technician will perform</span></span>

2.  <span data-ttu-id="b3c01-111">ชนิดของการบริการหรือการซ่อมแซม</span><span class="sxs-lookup"><span data-stu-id="b3c01-111">The type of service or repair</span></span>

3.  <span data-ttu-id="b3c01-112">รายการการซ่อมแซม รวมทั้งรายละเอียดเกี่ยวกับอาการและการวินิจฉัย</span><span class="sxs-lookup"><span data-stu-id="b3c01-112">The item to repair, including details about the symptoms and diagnosis</span></span>

4.  <span data-ttu-id="b3c01-113">ค่าใช้จ่ายและค่าธรรมเนียมที่เกี่ยวข้องกับบริการหรือซ่อมแซมใดๆ</span><span class="sxs-lookup"><span data-stu-id="b3c01-113">Any expenses and fees related to the service or repair</span></span>

<span data-ttu-id="b3c01-114">คุณสามารถได้รับ ประมวลผล และจัดส่งคำขอบริการได้</span><span class="sxs-lookup"><span data-stu-id="b3c01-114">You can receive, process, and dispatch service requests.</span></span> <span data-ttu-id="b3c01-115">หลังจากที่คุณได้สร้างใบสั่งบริการ คุณสามารถใช้ขั้นของการบริการติดตามความคืบหน้า และระบุกฎที่ควบคุมการดำเนินการเปิดใช้งานในแต่ละขั้นตอน </span><span class="sxs-lookup"><span data-stu-id="b3c01-115">After you have created a service order, you can use service stages to monitor progress and specify rules that control what actions are enabled in each stage.</span></span> <span data-ttu-id="b3c01-116">เมื่อใบสั่งบริการเสร็จสมบูรณ์แล้ว คุณสามารถออกจากระบบใบสั่งเพื่อยืนยันว่า เสร็จสมบูรณ์แล้ว และใบสั่งที่จะเริ่มต้นกระบวนการใบแจ้งหนี้ที่ลงรายการบัญชีแล้ว</span><span class="sxs-lookup"><span data-stu-id="b3c01-116">When a service order is complete, you can sign off on the order to confirm that it is complete, and then post the order to start the invoice process.</span></span>

<span data-ttu-id="b3c01-117">ใช้เครื่องมือรายงานเพื่อตรวจสอบกำไรขั้นต้นของใบสั่งบริการ และธุรกรรมการบอกรับเป็นสมาชิก และคำอธิบายเกี่ยวกับงานพิมพ์ และงานใบรับสินค้า</span><span class="sxs-lookup"><span data-stu-id="b3c01-117">Use the reporting tools to monitor service order margins and subscription transactions, and print work descriptions and work receipts.</span></span>

## <a name="business-processes"></a><span data-ttu-id="b3c01-118">กระบวนการทางธุรกิจ</span><span class="sxs-lookup"><span data-stu-id="b3c01-118">Business processes</span></span>

<span data-ttu-id="b3c01-119">แผนภาพต่อไปนี้แสดงให้เห็นถึงกระบวนการทางธุรกิจระดับสูงสำหรับ **การจัดการงานบริการ** และแสดงที่ซึ่งกระบวนการบริการที่รวมเข้ากับโมดูลอื่นใน Microsoft Dynamics 365 for Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="b3c01-119">The following diagram illustrates the high level business processes for **Service management**, and shows where service processes integrate with other modules in Microsoft Dynamics 365 for Finance and Operations.</span></span>

<span data-ttu-id="b3c01-120">[![แผนภาพกระบวนการทางธุรกิจเกี่ยวกับการจัดการบริการ](./media/sm_home_page.gif)](./media/sm_home_page.gif)</span><span class="sxs-lookup"><span data-stu-id="b3c01-120">[![Service management business process diagram](./media/sm_home_page.gif)](./media/sm_home_page.gif)</span></span>

## <a name="service-management-at-a-glance"></a><span data-ttu-id="b3c01-121">จัดการการบริการ</span><span class="sxs-lookup"><span data-stu-id="b3c01-121">Service management at a glance</span></span>

|<span data-ttu-id="b3c01-122">งานที่สำคัญ</span><span class="sxs-lookup"><span data-stu-id="b3c01-122">Important tasks</span></span>           | <span data-ttu-id="b3c01-123">หน้าหลัก</span><span class="sxs-lookup"><span data-stu-id="b3c01-123">Primary pages</span></span>                         |<span data-ttu-id="b3c01-124">รายงานที่ได้รับความนิยม</span><span class="sxs-lookup"><span data-stu-id="b3c01-124">Popular reports</span></span>              |
|--------------------------|---------------------------------------|-----------------------------|
|<span data-ttu-id="b3c01-125">เติมเต็มข้อตกลงการให้บริการ</span><span class="sxs-lookup"><span data-stu-id="b3c01-125">Fulfill service agreements</span></span>|<span data-ttu-id="b3c01-126">ข้อตกลงการให้บริการ</span><span class="sxs-lookup"><span data-stu-id="b3c01-126">Service agreements</span></span>                     |<span data-ttu-id="b3c01-127">ค่าเผื่อในใบสั่งบริการ</span><span class="sxs-lookup"><span data-stu-id="b3c01-127">Service order margin</span></span>         |
|<span data-ttu-id="b3c01-128">จัดการการสอบถามของลูกค้า</span><span class="sxs-lookup"><span data-stu-id="b3c01-128">Handle customer inquiries</span></span> |<span data-ttu-id="b3c01-129">ใบสั่งบริการ</span><span class="sxs-lookup"><span data-stu-id="b3c01-129">Service orders</span></span>                         |<span data-ttu-id="b3c01-130">คำอธิบายงาน</span><span class="sxs-lookup"><span data-stu-id="b3c01-130">Work description</span></span>             |
|                          |<span data-ttu-id="b3c01-131">บอร์ดการจัดส่ง</span><span class="sxs-lookup"><span data-stu-id="b3c01-131">Dispatch board</span></span>                         |<span data-ttu-id="b3c01-132">ธุรกรรม - การบอกรับเป็นสมาชิก</span><span class="sxs-lookup"><span data-stu-id="b3c01-132">Transaction - subscription</span></span>   |
|                          |                                       |<span data-ttu-id="b3c01-133">ธุรกรรมค่าธรรมเนียมการบอกรับเป็นสมาชิก</span><span class="sxs-lookup"><span data-stu-id="b3c01-133">Subscription fee transactions</span></span>|


## <a name="integration-of-service-management"></a><span data-ttu-id="b3c01-134">การรวมการจัดการงานบริการ</span><span class="sxs-lookup"><span data-stu-id="b3c01-134">Integration of Service management</span></span>

<span data-ttu-id="b3c01-135">สามารถรวมการจัดการบริการกับโมดูลต่อไปนี้ได้ใน:</span><span class="sxs-lookup"><span data-stu-id="b3c01-135">Service management can be integrated with the following modules:</span></span>

  - [<span data-ttu-id="b3c01-136">การขายและการตลาด</span><span class="sxs-lookup"><span data-stu-id="b3c01-136">Sales and marketing</span></span>](../sales-marketing/overview-sales-marketing.md)
  - [<span data-ttu-id="b3c01-137">ทรัพยากรบุคคล</span><span class="sxs-lookup"><span data-stu-id="b3c01-137">Human resources</span></span>](https://docs.microsoft.com/en-us/dynamics365/unified-operations/talent/index)

  


