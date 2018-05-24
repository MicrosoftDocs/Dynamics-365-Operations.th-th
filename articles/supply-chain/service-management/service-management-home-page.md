---
title: "การจัดการงานบริการ"
description: "ใช้การจัดการงานบริการเพื่อกำหนดข้อตกลงการให้บริการและการบอกรับเป็นสมาชิกการบริการ จัดการใบสั่งบริการและการสอบถามของลูกค้า และเพื่อจัดการและวิเคราะห์การจัดส่งบริการให้แก่ลูกค้า"
author: YuyuScheller
manager: AnnBe
ms.date: 05/09/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: SMAServiceOrderTable
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 
ms.assetid: 
ms.search.region: Global
ms.author: YuyuScheller
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 02cdf4615e2071f2b7de2e86b6f9e6637c6e5d8d
ms.openlocfilehash: 236ab21b2d1c5a4e82270e5381d163e97437cb7f
ms.contentlocale: th-th
ms.lasthandoff: 05/09/2018

---


# <a name="service-management"></a><span data-ttu-id="0dacb-103">การจัดการงานบริการ</span><span class="sxs-lookup"><span data-stu-id="0dacb-103">Service management</span></span> 

[!include [banner](../includes/banner.md)]


<span data-ttu-id="0dacb-104">ใช้ **การจัดการงานบริการ** เพื่อกำหนดข้อตกลงการให้บริการและการบอกรับเป็นสมาชิกการบริการ จัดการใบสั่งบริการและการสอบถามของลูกค้า และเพื่อจัดการและวิเคราะห์การจัดส่งบริการให้แก่ลูกค้า</span><span class="sxs-lookup"><span data-stu-id="0dacb-104">Use **Service management** to establish service agreements and service subscriptions, handle service orders and customer inquiries, and to manage and analyze the delivery of services to customers.</span></span> <span data-ttu-id="0dacb-105">คุณสามารถใช้ข้อตกลงการให้บริการเพื่อกำหนดทรัพยากรที่ใช้ในการไปเยี่ยมเพื่อให้บริการตามปกติ </span><span class="sxs-lookup"><span data-stu-id="0dacb-105">You can use service agreements to define the resources that are used in a typical service visit.</span></span> <span data-ttu-id="0dacb-106">คุณยังสามารถใช้ข้อตกลงการให้บริการเพื่อดูว่าทรัพยากรดังกล่าวจะออกอินวอยซ์ให้กับลูกค้า </span><span class="sxs-lookup"><span data-stu-id="0dacb-106">You can also use service agreements to view how those resources are invoiced to the customer.</span></span> <span data-ttu-id="0dacb-107">ข้อตกลงการให้บริการยังสามารถรวมข้อตกลงระดับการบริการที่ระบุเวลาการตอบสนองมาตรฐาน และมีเครื่องมือต่างๆ เพื่อบันทึกเวลาเกิดขึ้นจริง</span><span class="sxs-lookup"><span data-stu-id="0dacb-107">A service agreement can also include a service level agreement that specifies standard response times, and offers tools to record the actual time.</span></span>

<span data-ttu-id="0dacb-108">คุณสามารถสร้างใบสั่งบริการเพื่อจัดการข้อมูลเกี่ยวกับการจัดกำหนดการ และไม่ได้จัดกำหนดการเข้าใช้โดยช่างเทคนิคบริการไปไซต์ของลูกค้า </span><span class="sxs-lookup"><span data-stu-id="0dacb-108">You can create service orders to manage information about scheduled and unscheduled visits by a service technician to a customer site.</span></span> <span data-ttu-id="0dacb-109">ใบสั่งบริการรวมถึงข้อมูลเช่น:</span><span class="sxs-lookup"><span data-stu-id="0dacb-109">Service orders include information such as:</span></span>

1.  <span data-ttu-id="0dacb-110">จำนวนชั่วโมงของงานที่จะดำเนินการที่ช่างเทคนิคบริการ</span><span class="sxs-lookup"><span data-stu-id="0dacb-110">The hours of work that the service technician will perform</span></span>

2.  <span data-ttu-id="0dacb-111">ชนิดของการบริการหรือการซ่อมแซม</span><span class="sxs-lookup"><span data-stu-id="0dacb-111">The type of service or repair</span></span>

3.  <span data-ttu-id="0dacb-112">รายการการซ่อมแซม รวมทั้งรายละเอียดเกี่ยวกับอาการและการวินิจฉัย</span><span class="sxs-lookup"><span data-stu-id="0dacb-112">The item to repair, including details about the symptoms and diagnosis</span></span>

4.  <span data-ttu-id="0dacb-113">ค่าใช้จ่ายและค่าธรรมเนียมที่เกี่ยวข้องกับบริการหรือซ่อมแซมใดๆ</span><span class="sxs-lookup"><span data-stu-id="0dacb-113">Any expenses and fees related to the service or repair</span></span>

<span data-ttu-id="0dacb-114">ลูกค้าสามารถส่งคำขอการบริการผ่านอินเทอร์เน็ตได้โดยใช้เว็บไซต์องค์กร</span><span class="sxs-lookup"><span data-stu-id="0dacb-114">Customers can submit service requests through the Internet by using the Enterprise Portal.</span></span> <span data-ttu-id="0dacb-115">คุณสามารถได้รับ ประมวลผล และจัดส่งคำขอ </span><span class="sxs-lookup"><span data-stu-id="0dacb-115">You can receive, process, and dispatch these requests.</span></span> <span data-ttu-id="0dacb-116">หลังจากที่คุณได้สร้างใบสั่งบริการ คุณสามารถใช้ขั้นของการบริการติดตามความคืบหน้า และระบุกฎที่ควบคุมการดำเนินการเปิดใช้งานในแต่ละขั้นตอน </span><span class="sxs-lookup"><span data-stu-id="0dacb-116">After you have created a service order, you can use service stages to monitor progress and specify rules that control what actions are enabled in each stage.</span></span> <span data-ttu-id="0dacb-117">เมื่อใบสั่งบริการเสร็จสมบูรณ์แล้ว คุณสามารถออกจากระบบใบสั่งเพื่อยืนยันว่า เสร็จสมบูรณ์แล้ว และใบสั่งที่จะเริ่มต้นกระบวนการใบแจ้งหนี้ที่ลงรายการบัญชีแล้ว</span><span class="sxs-lookup"><span data-stu-id="0dacb-117">When a service order is complete, you can sign off on the order to confirm that it is complete, and then post the order to start the invoice process.</span></span>

<span data-ttu-id="0dacb-118">ใช้เครื่องมือรายงานเพื่อตรวจสอบกำไรขั้นต้นของใบสั่งบริการ และธุรกรรมการบอกรับเป็นสมาชิก และคำอธิบายเกี่ยวกับงานพิมพ์ และงานใบรับสินค้า</span><span class="sxs-lookup"><span data-stu-id="0dacb-118">Use the reporting tools to monitor service order margins and subscription transactions, and print work descriptions and work receipts.</span></span>

## <a name="business-processes"></a><span data-ttu-id="0dacb-119">กระบวนการทางธุรกิจ</span><span class="sxs-lookup"><span data-stu-id="0dacb-119">Business processes</span></span>

<span data-ttu-id="0dacb-120">แผนภาพต่อไปนี้แสดงให้เห็นถึงกระบวนการทางธุรกิจระดับสูงสำหรับ **การจัดการงานบริการ** และแสดงที่ซึ่งกระบวนการบริการที่รวมเข้ากับโมดูลอื่นใน Microsoft Dynamics 365 for Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="0dacb-120">The following diagram illustrates the high level business processes for **Service management**, and shows where service processes integrate with other modules in Microsoft Dynamics 365 for Finance and Operations.</span></span>

<span data-ttu-id="0dacb-121">[![แผนภาพกระบวนการทางธุรกิจเกี่ยวกับการจัดการบริการ](./media/sm_home_page.gif)](./media/sm_home_page.gif)</span><span class="sxs-lookup"><span data-stu-id="0dacb-121">[![Service management business process diagram](./media/sm_home_page.gif)](./media/sm_home_page.gif)</span></span>

## <a name="service-management-at-a-glance"></a><span data-ttu-id="0dacb-122">จัดการการบริการ</span><span class="sxs-lookup"><span data-stu-id="0dacb-122">Service management at a glance</span></span>

<table>
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="0dacb-123">งานที่สำคัญ</span><span class="sxs-lookup"><span data-stu-id="0dacb-123">Important tasks</span></span></p></th>
<th><p><span data-ttu-id="0dacb-124">ฟอร์มหลัก</span><span class="sxs-lookup"><span data-stu-id="0dacb-124">Primary forms</span></span></p></th>
<th><p><span data-ttu-id="0dacb-125">รายงานที่ได้รับความนิยม</span><span class="sxs-lookup"><span data-stu-id="0dacb-125">Popular reports</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="0dacb-126">เติมเต็มข้อตกลงการให้บริการ</span><span class="sxs-lookup"><span data-stu-id="0dacb-126">Fulfill service agreements</span></span></a></p></td>
<td><p><span data-ttu-id="0dacb-127"><a href="https://technet.microsoft.com/en-us/library/aa617823(v=ax.60)">ข้อตกลงการให้บริการ (แบบฟอร์ม)</a></span><span class="sxs-lookup"><span data-stu-id="0dacb-127"><a href="https://technet.microsoft.com/en-us/library/aa617823(v=ax.60)">Service agreements (form)</a></span></span></p></td>
<td><p><span data-ttu-id="0dacb-128"><strong>ค่าเผื่อในใบสั่งบริการ</strong></span><span class="sxs-lookup"><span data-stu-id="0dacb-128"><strong>Service order margin</strong></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0dacb-129">จัดการการสอบถามของลูกค้า</span><span class="sxs-lookup"><span data-stu-id="0dacb-129">Handle customer inquiries</span></span></a></p></td>
<td><p><span data-ttu-id="0dacb-130"><a href="https://technet.microsoft.com/en-us/library/aa554361(v=ax.60)">ใบสั่งบริการ (แบบฟอร์ม)</a></span><span class="sxs-lookup"><span data-stu-id="0dacb-130"><a href="https://technet.microsoft.com/en-us/library/aa554361(v=ax.60)">Service orders (form)</a></span></span></p></td>
<td><p><span data-ttu-id="0dacb-131"><strong>คำอธิบายงาน</strong></span><span class="sxs-lookup"><span data-stu-id="0dacb-131"><strong>Work description</strong></span></span></p></td>
</tr>
<tr class="odd">
<td><p></p></td>
<td><p><span data-ttu-id="0dacb-132"><a href="https://technet.microsoft.com/en-us/library/hh242789(v=ax.60)">บอร์ดการจัดส่ง (แบบฟอร์ม)</a></span><span class="sxs-lookup"><span data-stu-id="0dacb-132"><a href="https://technet.microsoft.com/en-us/library/hh242789(v=ax.60)">Dispatch board (form)</a></span></span></p></td>
<td><p><span data-ttu-id="0dacb-133"><strong>ธุรกรรม - การบอกรับเป็นสมาชิก</strong></span><span class="sxs-lookup"><span data-stu-id="0dacb-133"><strong>Transaction - subscription</strong></span></span></p></td>
</tr>
<tr class="even">
<td><p></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="0dacb-134"><strong>ธุรกรรมค่าธรรมเนียมการบอกรับเป็นสมาชิก</strong></span><span class="sxs-lookup"><span data-stu-id="0dacb-134"><strong>Subscription fee transactions</strong></span></span></p></td>
</tr>
</tbody>
</table>


## <a name="integration-of-service-management"></a><span data-ttu-id="0dacb-135">การรวมการจัดการงานบริการ</span><span class="sxs-lookup"><span data-stu-id="0dacb-135">Integration of Service management</span></span>

<span data-ttu-id="0dacb-136">การจัดการงานบริการสามารถรวมกับโมดูลดังต่อไปนี้ได้ใน Microsoft Dynamics 365 for Finance and Operations:</span><span class="sxs-lookup"><span data-stu-id="0dacb-136">Service management can be integrated with the following modules in Microsoft Dynamics 365 for Finance and Operations:</span></span>

  - [<span data-ttu-id="0dacb-137">การขายและการตลาด</span><span class="sxs-lookup"><span data-stu-id="0dacb-137">Sales and marketing</span></span>](../sales-marketing/overview-sales-marketing.md)

  - [<span data-ttu-id="0dacb-138">ทรัพยากรบุคคล</span><span class="sxs-lookup"><span data-stu-id="0dacb-138">Human resources</span></span>](https://docs.microsoft.com/en-us/dynamics365/unified-operations/talent/index)

  


