---
title: การสร้างความสัมพันธ์ของภารกิจการให้บริการ
description: คุณสามารถเชื่อมโยงภารกิจการให้บริการกับข้อตกลงการให้บริการหรือใบสั่งบริการได้ เพื่ออธิบายภารกิจการให้บริการที่จะเสร็จสมบูรณ์สำหรับข้อตกลงหรือใบสั่ง
author: ShylaThompson
manager: tfehr
ms.date: 05/01/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SMAServiceOrderTable, SMAAgreementTable
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: ea5952376fe30f489d385c8f8295fbf86f2af085
ms.sourcegitcommit: 34b8f6f5c6134b7b97a9fb41d0b2e63215c67062
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 02/17/2021
ms.locfileid: "5470748"
---
# <a name="create-service-task-relations"></a><span data-ttu-id="b812d-103">การสร้างความสัมพันธ์ของภารกิจการให้บริการ</span><span class="sxs-lookup"><span data-stu-id="b812d-103">Create service task relations</span></span>    

[!include [banner](../includes/banner.md)]

<span data-ttu-id="b812d-104">คุณสามารถเชื่อมโยงภารกิจการให้บริการกับข้อตกลงการให้บริการหรือใบสั่งบริการได้ เพื่ออธิบายภารกิจการให้บริการที่จะเสร็จสมบูรณ์สำหรับข้อตกลงหรือใบสั่ง</span><span class="sxs-lookup"><span data-stu-id="b812d-104">You can associate service tasks with service agreements or service orders in order to describe the service task to be completed for the agreement or order.</span></span> <span data-ttu-id="b812d-105">ข้อมูลนี้พร้อมใช้งานสำหรับช่างเทคนิคและลูกค้า</span><span class="sxs-lookup"><span data-stu-id="b812d-105">This information is available to service technicians and customers.</span></span>

## <a name="create-a-relation-with-a-service-agreement"></a><span data-ttu-id="b812d-106">สร้างความสัมพันธ์กับข้อตกลงการให้บริการ</span><span class="sxs-lookup"><span data-stu-id="b812d-106">Create a relation with a service agreement</span></span>

1.  <span data-ttu-id="b812d-107">ไปยัง **การจัดการบริการ** \> **ทั่วไป** \> **ข้อตกลงการให้บริการ** \> **ข้อตกลงการให้บริการ**</span><span class="sxs-lookup"><span data-stu-id="b812d-107">Go to **Service management** \> **Common** \> **Service agreements** \> **Service agreements**.</span></span>

2.  <span data-ttu-id="b812d-108">เลือกข้อตกลงการให้บริการที่มีอยู่ หรือสร้างข้อตกลงการให้บริการใหม่</span><span class="sxs-lookup"><span data-stu-id="b812d-108">Select an existing service agreement, or create a new service agreement.</span></span>

3.  <span data-ttu-id="b812d-109">บนบานหน้าต่างการดำเนินงาน เลือกปุ่ม **งานบริการ**</span><span class="sxs-lookup"><span data-stu-id="b812d-109">On the Action Pane, select the **Service tasks** button.</span></span>

4.  <span data-ttu-id="b812d-110">ในฟอร์ม **งานบริการ** เลือก **สร้าง** เพื่อสร้างรายการใหม่ และจากนั้น เลือกงานบริการจากรายการ **งานบริการ** เพื่อแนบงานบริการกับข้อตกลงการให้บริการ</span><span class="sxs-lookup"><span data-stu-id="b812d-110">On the **Service tasks** form, select **New** to create a new line, and then select a service task from the **Service task** list to attach the service task to the service agreement.</span></span>

5.  <span data-ttu-id="b812d-111">บนแท็บ **คำอธิบาย** ป้อนคำอธิบายหมายเหตุภายในหรือภายนอกใดๆ ในฟิลด์ข้อความอิสระ</span><span class="sxs-lookup"><span data-stu-id="b812d-111">On the **Description** tab, enter any internal or external note descriptions in the free text fields.</span></span>

6.  <span data-ttu-id="b812d-112">ปิดแบบฟอร์มเพื่อบันทึกเรกคอร์ด</span><span class="sxs-lookup"><span data-stu-id="b812d-112">Close the form to save the record.</span></span>

<span data-ttu-id="b812d-113">ทำขั้นตอนนี้ซ้ำจนกระทั่งคุณได้สร้างความสัมพันธ์ของภารกิจการให้บริการทั้งหมดที่จำเป็นสำหรับข้อตกลงการให้บริการ </span><span class="sxs-lookup"><span data-stu-id="b812d-113">Repeat this procedure until you have created all the necessary service task relations for the service agreement.</span></span> <span data-ttu-id="b812d-114">ขณะนี้คุณสามารถระบุภารกิจการให้บริการเหล่านี้สำหรับบรรทัดข้อตกลงใดๆ ที่แนบได้</span><span class="sxs-lookup"><span data-stu-id="b812d-114">You can now specify these service tasks for any attached agreement lines.</span></span>

<span data-ttu-id="b812d-115">ความสัมพันธ์ของภารกิจการให้บริการที่สร้างในข้อตกลงการให้บริการสามารถใช้งานได้จากใบสั่งบริการทั้งหมดที่แนบกับข้อตกลงการให้บริการ</span><span class="sxs-lookup"><span data-stu-id="b812d-115">A service tasks relation that is created on a service agreement is available from all service orders that are attached to the service agreement.</span></span>

## <a name="create-a-relation-with-a-service-order"></a><span data-ttu-id="b812d-116">สร้างความสัมพันธ์กับใบสั่งบริการ</span><span class="sxs-lookup"><span data-stu-id="b812d-116">Create a relation with a service order</span></span>

1.  <span data-ttu-id="b812d-117">ไปที่ **การจัดการบริการ** \> **ทั่วไป** \> **ใบสั่งบริการ** \> **ใบสั่งบริการ**</span><span class="sxs-lookup"><span data-stu-id="b812d-117">Go to **Service management** \> **Common** \> **Service orders** \> **Service orders**.</span></span>

2.  <span data-ttu-id="b812d-118">เลือกใบสั่งบริการที่มีอยู่แล้ว หรือสร้างใบสั่งบริการใหม่</span><span class="sxs-lookup"><span data-stu-id="b812d-118">Select an existing service order, or create a new service order.</span></span>

3.  <span data-ttu-id="b812d-119">บนบานหน้าต่างการดำเนินงาน เลือกปุ่ม **งานบริการ**</span><span class="sxs-lookup"><span data-stu-id="b812d-119">On the Action Pane, select the **Service tasks** button.</span></span>

4.  <span data-ttu-id="b812d-120">จากฟอร์ม **งานบริการ** เลือก **สร้าง** เพื่อสร้างรายการใหม่ และจากนั้น เลือกงานบริการจากรายการ **งานบริการ** เพื่อแนบงานบริการกับใบสั่งบริการ</span><span class="sxs-lookup"><span data-stu-id="b812d-120">From the **Service tasks** form, select **New** to create a new line, and then select a service task from the **Service task** list to attach the service tasks to the service order.</span></span>

5.  <span data-ttu-id="b812d-121">บนแท็บ **คำอธิบาย** ป้อนคำอธิบายหมายเหตุภายในหรือภายนอกใดๆ ในฟิลด์ข้อความอิสระ</span><span class="sxs-lookup"><span data-stu-id="b812d-121">On the **Description** tab, enter any internal or external note descriptions in the free text fields.</span></span>

6.  <span data-ttu-id="b812d-122">ปิดแบบฟอร์มเพื่อบันทึกเรกคอร์ด</span><span class="sxs-lookup"><span data-stu-id="b812d-122">Close the form to save the record.</span></span>

<span data-ttu-id="b812d-123">ทำขั้นตอนนี้ซ้ำจนกระทั่งคุณได้สร้างความสัมพันธ์ของภารกิจการให้บริการทั้งหมดที่จำเป็นสำหรับใบสั่งบริการ</span><span class="sxs-lookup"><span data-stu-id="b812d-123">Repeat this procedure until you have created all the necessary service task relations for the service order.</span></span> <span data-ttu-id="b812d-124">ขณะนี้คุณสามารถเลือกภารกิจการให้บริการที่คุณได้สร้างความสัมพันธ์ให้เมื่อคุณสร้างบรรทัดใบสั่งบริการ</span><span class="sxs-lookup"><span data-stu-id="b812d-124">You can now select the service task for which you have created the relation when you create service order lines.</span></span>

<span data-ttu-id="b812d-125">ความสัมพันธ์ของภารกิจการให้บริการที่สร้างในใบสั่งบริการจะสามารถใช้งานได้ในใบสั่งบริการที่ระบุ</span><span class="sxs-lookup"><span data-stu-id="b812d-125">Service task relations that are created on a service order are available on the specific service order.</span></span>

## <a name="see-also"></a><span data-ttu-id="b812d-126">ดูเพิ่มเติมที่</span><span class="sxs-lookup"><span data-stu-id="b812d-126">See also</span></span>

[<span data-ttu-id="b812d-127">ภาพรวมของงานบริการ</span><span class="sxs-lookup"><span data-stu-id="b812d-127">Service tasks overview</span></span>](service-tasks.md)


  




[!INCLUDE[footer-include](../../includes/footer-banner.md)]