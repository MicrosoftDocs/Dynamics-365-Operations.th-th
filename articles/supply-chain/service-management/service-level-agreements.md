---
title: ภาพรวมของข้อตกลงระดับการให้บริการ
description: ในข้อตกลงระดับการให้บริการ ลูกค้าตกลงยอมรับเวลาการตอบสนองขั้นต่ำ ตามเวลาที่บริษัทที่ให้บริการบันทึกปัญหา และเวลาที่ปัญหานั้นได้รับการแก้ไข
author: ShylaThompson
manager: tfehr
ms.date: 07/25/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SMAServicelevelagreement
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 01cdfe519e55ca2a9aa17f4ac181ee675b2793cf
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 10/13/2020
ms.locfileid: "4438570"
---
# <a name="service-level-agreements-overview"></a><span data-ttu-id="696b7-103">ภาพรวมของข้อตกลงระดับการให้บริการ</span><span class="sxs-lookup"><span data-stu-id="696b7-103">Service level agreements overview</span></span>       

[!include [banner](../includes/banner.md)]


<span data-ttu-id="696b7-104">ข้อตกลงระดับการบริการ (SLA) คือข้อตกลงระหว่างบริษัทที่ให้บริการและลูกค้าที่รับบริการ </span><span class="sxs-lookup"><span data-stu-id="696b7-104">A service level agreement (SLA) is an agreement between a service company and a service customer.</span></span> <span data-ttu-id="696b7-105">ใน SLA ลูกค้าตกลงยอมรับเวลาการตอบสนองขั้นต่ำ ตามเวลาที่บริษัทที่ให้บริการบันทึกปัญหา และเวลาที่ปัญหานั้นได้รับการแก้ไข</span><span class="sxs-lookup"><span data-stu-id="696b7-105">In a SLA, the customer agrees to a minimum response time based on when the service company records the issue and when the issue is resolved.</span></span>

<span data-ttu-id="696b7-106">SLA จะบังคับระดับของการให้บริการมาตรฐานที่นำเสนอให้แก่ลูกค้า และยังทำให้ชัดเจนต่อบริษัทที่ให้บริการ เมื่องานบริการควรจะเสร็จสมบูรณ์</span><span class="sxs-lookup"><span data-stu-id="696b7-106">A SLA enforces a standard level of service that is offered to customers, and also makes it transparent to a service company when a service job should be completed.</span></span>

<span data-ttu-id="696b7-107">คุณสามารถสร้าง SLA ได้หลายฉบับเพื่อนำเสนอระดับของการให้บริการที่แตกต่างกันแก่ลูกค้าที่รับบริการ</span><span class="sxs-lookup"><span data-stu-id="696b7-107">Any number of SLAs can be created to offer service customers different levels of service.</span></span>

## <a name="create-a-service-level-agreement"></a><span data-ttu-id="696b7-108">การสร้างข้อตกลงระดับการบริการ</span><span class="sxs-lookup"><span data-stu-id="696b7-108">Create a service level agreement</span></span>

1.  <span data-ttu-id="696b7-109">คลิก **การจัดการบริการ** \> **ตั้งค่า** \> **ข้อตกลงการให้บริการ** \> **ข้อตกลงระดับการให้บริการ**</span><span class="sxs-lookup"><span data-stu-id="696b7-109">Click **Service management** \> **Setup** \> **Service agreements** \> **Service level agreements**.</span></span>

2.  <span data-ttu-id="696b7-110">พิมพ์ชื่อสำหรับข้อตกลงระดับการให้บริการในฟิลด์ **ข้อตกลงการให้บริการ**</span><span class="sxs-lookup"><span data-stu-id="696b7-110">Type a name for the service level agreement in the **Service level agreement** field.</span></span>

3.  <span data-ttu-id="696b7-111">พิมพ์เวลาที่คุณต้องการอนุญาตให้ความเสร็จสมบูรณ์ของการเรียกบริการ ที่ถูกแนบกับข้อตกลงระดับการให้บริการ</span><span class="sxs-lookup"><span data-stu-id="696b7-111">Type the time that you want to allow for completion of service calls that are attached to the service level agreement.</span></span> <span data-ttu-id="696b7-112">จากนั้น เลือกปฏิทิน ถ้าคุณต้องการใช้เป็นฐานของข้อตกลงระดับการให้บริการในปฏิทินเฉพาะ</span><span class="sxs-lookup"><span data-stu-id="696b7-112">Then select a calendar if you want to base the service level agreement on a specific calendar.</span></span>

## <a name="apply-a-service-level-agreement"></a><span data-ttu-id="696b7-113">การใช้ข้อตกลงระดับการบริการ</span><span class="sxs-lookup"><span data-stu-id="696b7-113">Apply a service level agreement</span></span>

<span data-ttu-id="696b7-114">SLA มีการใช้กับข้อตกลงการให้บริการโดยตรง</span><span class="sxs-lookup"><span data-stu-id="696b7-114">The SLA is applied directly to a service agreement.</span></span>

<span data-ttu-id="696b7-115">ใบสั่งบริการที่คุณสร้างขึ้นด้วยตนเองและแนบกับข้อตกลงการให้บริการที่มี SLA จะถูกประเมินผลโดยเปรียบเทียบกับ SLA นั้น</span><span class="sxs-lookup"><span data-stu-id="696b7-115">Service orders that you create manually and attach to a service agreement that has an SLA are measured against that SLA.</span></span>

<span data-ttu-id="696b7-116">ใบสั่งบริการที่คุณสร้างขึ้นโดยอัตโนมัติจะไม่มีการแนบกับ SLA</span><span class="sxs-lookup"><span data-stu-id="696b7-116">Service orders that you create automatically are not attached to an SLA.</span></span>

## <a name="apply-the-service-level-agreement-to-the-service-agreement"></a><span data-ttu-id="696b7-117">การใช้ข้อตกลงระดับการบริการกับข้อตกลงการให้บริการ</span><span class="sxs-lookup"><span data-stu-id="696b7-117">Apply the service level agreement to the service agreement</span></span>

1.  <span data-ttu-id="696b7-118">คลิก **การจัดการบริการ** \> **ทั่วไป** \> **ข้อตกลงการให้บริการ** \> **ข้อตกลงการให้บริการ**</span><span class="sxs-lookup"><span data-stu-id="696b7-118">Click **Service management** \> **Common** \> **Service agreements** \> **Service agreements**.</span></span> <span data-ttu-id="696b7-119">เลือกข้อตกลงการให้บริการที่คุณต้องการนำไปใช้กับ SLA แล้วคลิก **แก้ไข** ใน **บานหน้าต่างการดำเนินการ**</span><span class="sxs-lookup"><span data-stu-id="696b7-119">Select the service agreement that you want to apply the SLA to, and then click **Edit** on the **Action Pane**.</span></span>

2.  <span data-ttu-id="696b7-120">ในฟิลด์ **ข้อตกลงระดับการให้บริการ** เลือก SLA ที่คุณต้องการกำหนด</span><span class="sxs-lookup"><span data-stu-id="696b7-120">In the **Service level agreement** field, select the SLA that you want to assign.</span></span>

## <a name="apply-the-service-level-agreement-to-the-service-agreement-group"></a><span data-ttu-id="696b7-121">การใช้ข้อตกลงระดับการบริการกับกลุ่มข้อตกลงการให้บริการ</span><span class="sxs-lookup"><span data-stu-id="696b7-121">Apply the service level agreement to the service agreement group</span></span>

1.  <span data-ttu-id="696b7-122">คลิก **การจัดการบริการ** \> **ตั้งค่า** \> **ข้อตกลงการให้บริการ** \> **กลุ่มข้อตกลงการให้บริการ**</span><span class="sxs-lookup"><span data-stu-id="696b7-122">Click **Service management** \> **Setup** \> **Service agreements** \> **Service agreement groups**.</span></span>

2.  <span data-ttu-id="696b7-123">ในฟิลด์ **ข้อตกลงระดับการให้บริการ** เลือก SLA ที่คุณต้องการกำหนด</span><span class="sxs-lookup"><span data-stu-id="696b7-123">In the **Service level agreement** field, select the SLA that you want to assign.</span></span>

## <a name="track-time-on-a-service-order-against-an-sla"></a><span data-ttu-id="696b7-124">การติดตามเวลาบนใบสั่งบริการโดยเปรียบเทียบกับ SLA</span><span class="sxs-lookup"><span data-stu-id="696b7-124">Track time on a service order against an SLA</span></span>

<span data-ttu-id="696b7-125">เมื่อคุณสร้างใบสั่งบริการใหม่สำหรับข้อตกลงการให้บริการที่กำหนดให้กับ SLA จะมีการเริ่มต้นช่วงเวลาสำหรับการจัดส่งของบริการ และระบบเริ่มการติดตามเวลาจัดส่ง</span><span class="sxs-lookup"><span data-stu-id="696b7-125">When you create a new service order for a service agreement that an SLA is assigned to, the time interval for the delivery of the service is initiated, and the system starts to track the delivery time.</span></span> <span data-ttu-id="696b7-126">นอกจากนี้ คุณสามารถตั้งค่าตัวเลือกต่อไปนี้ได้:</span><span class="sxs-lookup"><span data-stu-id="696b7-126">Additionally, you can set the following options:</span></span>

  - <span data-ttu-id="696b7-127">คุณสามารถเริ่มต้นและหยุดการบันทึกเวลาบนใบสั่งบริการ เพื่อลงทะเบียนจำนวนเวลารวมที่ใช้บนใบสั่งบริการต่างๆ</span><span class="sxs-lookup"><span data-stu-id="696b7-127">You can start and stop time recording on the service order to register the total amount of time that is spent on service orders.</span></span>

  - <span data-ttu-id="696b7-128">คุณสามารถติดตามการปฏิบัติตามช่วงเวลาที่ตั้งค่าไว้ในข้อตกลงระดับการบริการ</span><span class="sxs-lookup"><span data-stu-id="696b7-128">You can monitor compliance with the time interval that is set in the service level agreement.</span></span>

  - <span data-ttu-id="696b7-129">คุณสามารถกำหนดรหัสเหตุผลที่ต้องถูกตั้งค่า ถ้ามีการใช้งานเกินกว่าช่วงเวลาของข้อตกลงระดับการบริการ</span><span class="sxs-lookup"><span data-stu-id="696b7-129">You can define reason codes that must be set if the time interval of the service level agreement is exceeded.</span></span>

## <a name="see-also"></a><span data-ttu-id="696b7-130">ดูเพิ่มเติมที่</span><span class="sxs-lookup"><span data-stu-id="696b7-130">See also</span></span>

[<span data-ttu-id="696b7-131">การดูการปฏิบัติตามข้อตกลงระดับการให้บริการ</span><span class="sxs-lookup"><span data-stu-id="696b7-131">View compliance with service level agreements</span></span>](view-compliance-with-service-level-agreements.md)

  


