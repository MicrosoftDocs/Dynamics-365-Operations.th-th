---
title: "ข้อตกลงการให้บริการ"
description: "ข้อตกลงการให้บริการอนุญาตให้คุณสามารถกำหนดทรัพยากรที่ใช้ในการให้บริการตามปกติ และวิธีการออกใบแจ้งหนี้ทรัพยากรดังกล่าวให้แก่ลูกค้า"
author: YuyuScheller
manager: AnnBe
ms.date: 02/19/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: SMAAgreementTable
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
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: dfb8d101c69e9bfdb918dca5cf48da1f6d2564b8
ms.contentlocale: th-th
ms.lasthandoff: 04/13/2018

---

# <a name="service-agreements"></a><span data-ttu-id="bd0cf-103">ข้อตกลงการให้บริการ</span><span class="sxs-lookup"><span data-stu-id="bd0cf-103">Service agreements</span></span>

[!INCLUDE [banner](../includes/banner.md)]

<span data-ttu-id="bd0cf-104">ข้อตกลงการให้บริการอนุญาตให้คุณสามารถกำหนดทรัพยากรที่ใช้ในการให้บริการตามปกติ และวิธีการออกใบแจ้งหนี้ทรัพยากรดังกล่าวให้แก่ลูกค้า</span><span class="sxs-lookup"><span data-stu-id="bd0cf-104">Service agreements let you define the resources that are used in a typical service visit and how those resources are invoiced to the customer.</span></span>

<span data-ttu-id="bd0cf-105">ข้อตกลงการให้บริการทุกฉบับจะถูกแนบกับโครงการ ผ่านทางธุรกรรมซึ่งมีการลงรายการบัญชีและออกใบแจ้งหนี้</span><span class="sxs-lookup"><span data-stu-id="bd0cf-105">Every service agreement is attached to a project through which transactions are posted and invoiced.</span></span> <span data-ttu-id="bd0cf-106">อย่างไรก็ตาม คุณยังสามารถออกใบแจ้งหนี้ธุรกรรมใบสั่งบริการผ่านทางโครงการได้โดยตรง โดยไม่ต้องเชื่อมโยงใบสั่งบริการกับข้อตกลงการให้บริการ</span><span class="sxs-lookup"><span data-stu-id="bd0cf-106">However, you can also invoice service order transactions directly through the project without first having to connect the service order to a service agreement.</span></span> <span data-ttu-id="bd0cf-107">คุณอาจตัดสินใจทำเช่นนี้ ถ้าใบสั่งบริการใช้สำหรับการให้บริการเพียงครั้งเดียว และความต้องการในการประมวลผลธุรกรรมการบริการเกินมากกว่าความต้องการอย่างรวดเร็ว ในการรักษาข้อมูลข้อตกลงการให้บริการโดยละเอียดเกี่ยวกับลูกค้าในรอบระยะเวลาหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="bd0cf-107">You might decide to do this if the service order is for a one-time-only service visit and the need for processing the service transactions quickly outweighs the need for maintaining detailed service-agreement information about the customer over a period of time.</span></span>

## <a name="service-agreement"></a><span data-ttu-id="bd0cf-108">ข้อตกลงการให้บริการ</span><span class="sxs-lookup"><span data-stu-id="bd0cf-108">Service agreement</span></span>

<span data-ttu-id="bd0cf-109">ในข้อตกลงการให้บริการแต่ละฉบับ คุณต้องระบุโครงการ รหัสข้อตกลงการให้บริการ และกลุ่มข้อตกลงการให้บริการ </span><span class="sxs-lookup"><span data-stu-id="bd0cf-109">In each service agreement, you must specify a project, a service-agreement ID, and a service-agreement group.</span></span> <span data-ttu-id="bd0cf-110">กลุ่มข้อตกลงการให้บริการสามารถใช้ในการเรียงลำดับและจัดระเบียบข้อตกลงการให้บริการ</span><span class="sxs-lookup"><span data-stu-id="bd0cf-110">The service-agreement group can be used to sort and organize service agreements.</span></span>

<span data-ttu-id="bd0cf-111">ส่วนหัวของข้อตกลงการให้บริการมีการตั้งค่าที่ใช้กับรายการข้อตกลงที่แนบทั้งหมด:</span><span class="sxs-lookup"><span data-stu-id="bd0cf-111">A service agreement header contains settings that apply to all attached agreement lines:</span></span>

-  <span data-ttu-id="bd0cf-112">ข้อตกลงการให้บริการจะถูกระงับไว้หรือไม่ </span><span class="sxs-lookup"><span data-stu-id="bd0cf-112">Whether the service agreement is suspended.</span></span> <span data-ttu-id="bd0cf-113">ถ้าข้อตกลงการให้บริการถูกระงับไว้ คุณไม่สามารถสร้างใบสั่งบริการจากข้อตกลงการให้บริการได้</span><span class="sxs-lookup"><span data-stu-id="bd0cf-113">If the service agreement is suspended, you cannot generate service orders from the service agreement.</span></span>
-  <span data-ttu-id="bd0cf-114">ช่วงเวลาของข้อตกลงการให้บริการ</span><span class="sxs-lookup"><span data-stu-id="bd0cf-114">The duration of the service agreement.</span></span>
-  <span data-ttu-id="bd0cf-115">วิธีการรวมบรรทัดใบสั่งบริการเข้าในใบสั่งบริการ</span><span class="sxs-lookup"><span data-stu-id="bd0cf-115">How service-order lines are to be combined into service orders.</span></span>
-  <span data-ttu-id="bd0cf-116">ข้อตกลงการให้บริการเป็นเท็มเพลตหรือไม่</span><span class="sxs-lookup"><span data-stu-id="bd0cf-116">Whether the service agreement is a template.</span></span>

<span data-ttu-id="bd0cf-117">ในส่วนหัวของข้อตกลงการให้บริการ คุณยังตั้งค่าออบเจ็กต์ที่ให้บริการและงานบริการทั้งหมดซึ่งสามารถใช้กับข้อตกลงการให้บริการได้ โดยการป้อนงานบริการเฉพาะหรือออบเจ็กต์ที่ให้บริการเฉพาะที่จะถูกแนบกับรายการที่หลากหลายของข้อตกลง</span><span class="sxs-lookup"><span data-stu-id="bd0cf-117">In the service-agreement header, you also set up all the service objects and service tasks that can be used with the service agreement by entering the specific service tasks or service objects that are to be attached to the various lines of the agreement.</span></span>

<span data-ttu-id="bd0cf-118">จากส่วนหัวของข้อตกลงการให้บริการ คุณยังสามารถคัดลอกรายการข้อตกลงการให้บริการหรือรายการเท็มเพลตการบริการเข้าในข้อตกลงการให้บริการฉบับปัจจุบันได้ด้วย</span><span class="sxs-lookup"><span data-stu-id="bd0cf-118">From the service-agreement header, you can also copy service-agreement lines or service-template lines into the current service agreement.</span></span>

<span data-ttu-id="bd0cf-119">คุณสามารถระงับข้อตกลงการให้บริการและหยุดบรรทัดข้อตกลงการให้บริการแต่ละบรรทัดได้</span><span class="sxs-lookup"><span data-stu-id="bd0cf-119">You can suspend service agreements and stop individual service agreement lines.</span></span>

<span data-ttu-id="bd0cf-120">ถ้าคุณเลือกกล่องกาเครื่องหมาย **ระงับ** ในข้อตกลงการให้บริการ คุณจะไม่สามารถ:</span><span class="sxs-lookup"><span data-stu-id="bd0cf-120">If you select the **Suspended** check box on a service agreement, you cannot:</span></span>

-    <span data-ttu-id="bd0cf-121">สร้างใบสั่งบริการโดยอัตโนมัติหรือด้วยตนเองจากข้อตกลงการให้บริการ</span><span class="sxs-lookup"><span data-stu-id="bd0cf-121">Create service orders automatically or manually from the service agreement.</span></span>

<span data-ttu-id="bd0cf-122">ถ้าคุณเลือกกล่องกาเครื่องหมาย **หยุด** ในข้อตกลงการให้บริการ คุณจะไม่สามารถ:</span><span class="sxs-lookup"><span data-stu-id="bd0cf-122">If you select the **Stopped** check box on a service agreement line, you cannot:</span></span>

-    <span data-ttu-id="bd0cf-123">สร้างใบสั่งบริการโดยอัตโนมัติหรือด้วยตนเองจากบรรทัดข้อตกลงการให้บริการ</span><span class="sxs-lookup"><span data-stu-id="bd0cf-123">Create service orders automatically or manually from the service agreement line.</span></span>
-    <span data-ttu-id="bd0cf-124">คัดลอกบรรทัดข้อตกลงการให้บริการไปยังข้อตกลงการให้บริการหรือใบสั่งบริการอื่น</span><span class="sxs-lookup"><span data-stu-id="bd0cf-124">Copy the service agreement line into another service agreement or service order.</span></span>


> [!NOTE]
> <span data-ttu-id="bd0cf-125">ถ้าข้อตกลงการให้บริการถูกระงับไว้ ระบบจะหยุดรายการที่แนบอยู่ทั้งหมด ไม่ว่าแต่ละรายการจะมีสถานะอย่างไรก็ตาม</span><span class="sxs-lookup"><span data-stu-id="bd0cf-125">If a service agreement is suspended, all the attached lines are stopped, regardless of their individual status.</span></span>

## <a name="service-agreement-lines"></a><span data-ttu-id="bd0cf-126">บรรทัดข้อตกลงการให้บริการ</span><span class="sxs-lookup"><span data-stu-id="bd0cf-126">Service-agreement lines</span></span>

<span data-ttu-id="bd0cf-127">รายการข้อตกลงการให้บริการแต่ละรายการแสดงรายละเอียดเนื้อหาของงานการบริการที่นำเสนอ</span><span class="sxs-lookup"><span data-stu-id="bd0cf-127">Each service-agreement line describes in detail the content of the proposed service work.</span></span> <span data-ttu-id="bd0cf-128">บรรทัดข้อตกลงการให้บริการมีการตั้งค่าต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="bd0cf-128">The lines contain the following settings:</span></span>

-  <span data-ttu-id="bd0cf-129">ชนิดธุรกรรมและคำอธิบายของชนิดธุรกรรม</span><span class="sxs-lookup"><span data-stu-id="bd0cf-129">The transaction type and the description of the transaction type.</span></span>
-  <span data-ttu-id="bd0cf-130">พนักงานที่ทำงานการบริการ</span><span class="sxs-lookup"><span data-stu-id="bd0cf-130">The employee who performs the service work.</span></span>
-  <span data-ttu-id="bd0cf-131">วัตถุซึ่งต้องทำการบริการสำหรับข้อตกลงการให้บริการ</span><span class="sxs-lookup"><span data-stu-id="bd0cf-131">The objects on which service must be performed for the service agreement.</span></span>
-  <span data-ttu-id="bd0cf-132">ความถี่ในการทำงานการบริการ และความถี่ในการลงทะเบียนธุรกรรมสินค้า ค่าใช้จ่าย และค่าธรรมเนียมที่เกี่ยวข้อง</span><span class="sxs-lookup"><span data-stu-id="bd0cf-132">The frequency with which work is performed and associated item, expense, and fee transactions are registered.</span></span>
-  <span data-ttu-id="bd0cf-133">กรอบเวลาในการจัดกลุ่มบรรทัดใบสั่งบริการเข้าในใบสั่งบริการ</span><span class="sxs-lookup"><span data-stu-id="bd0cf-133">The time window within which service-order lines can be grouped into a service order.</span></span>
-  <span data-ttu-id="bd0cf-134">งานบริการที่ใช้ในการจัดกลุ่มชุดของรายการข้อตกลงการให้บริการเข้าด้วยกันกับภารกิจเกี่ยวกับงาน และใช้เพื่อสรุปให้ช่างเทคนิคการบริการและลูกค้าทราบถึงงานบริการที่จะนำเสนอ</span><span class="sxs-lookup"><span data-stu-id="bd0cf-134">The service tasks that are used to group sets of agreement lines together into work tasks and to summarize for service technicians and customers what service task is to be provided.</span></span>
-  <span data-ttu-id="bd0cf-135">บรรทัดถูกหยุดหรือไม่ </span><span class="sxs-lookup"><span data-stu-id="bd0cf-135">Whether a line is stopped.</span></span> <span data-ttu-id="bd0cf-136">ถ้าบรรทัดถูกหยุด คุณไม่สามารถสร้างใบสั่งบริการสำหรับบรรทัดนั้นได้</span><span class="sxs-lookup"><span data-stu-id="bd0cf-136">If a line is stopped, you cannot create service orders for that individual line.</span></span>
-  <span data-ttu-id="bd0cf-137">การตั้งค่าโครงการ เช่น ประเภทและลักษณะของรายการ</span><span class="sxs-lookup"><span data-stu-id="bd0cf-137">Project settings, such as the category and the line property.</span></span>

## <a name="related-topics"></a><span data-ttu-id="bd0cf-138">หัวข้อที่เกี่ยวข้อง</span><span class="sxs-lookup"><span data-stu-id="bd0cf-138">Related topics</span></span>

[<span data-ttu-id="bd0cf-139">การสร้างข้อตกลงการให้บริการ</span><span class="sxs-lookup"><span data-stu-id="bd0cf-139">Create service agreements</span></span>](create-service-agreements.md)

