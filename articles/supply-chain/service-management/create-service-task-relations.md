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
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 1e50b4322c65097ab4f8aba9c36e4d5e6cc4c01b
ms.sourcegitcommit: 708ca25687a4e48271cdcd6d2d22d99fb94cf140
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 10/10/2020
ms.locfileid: "3978641"
---
# <a name="create-service-task-relations"></a><span data-ttu-id="1b1f2-103">การสร้างความสัมพันธ์ของภารกิจการให้บริการ</span><span class="sxs-lookup"><span data-stu-id="1b1f2-103">Create service task relations</span></span>    

[!include [banner](../includes/banner.md)]

<span data-ttu-id="1b1f2-104">คุณสามารถเชื่อมโยงภารกิจการให้บริการกับข้อตกลงการให้บริการหรือใบสั่งบริการได้ เพื่ออธิบายภารกิจการให้บริการที่จะเสร็จสมบูรณ์สำหรับข้อตกลงหรือใบสั่ง</span><span class="sxs-lookup"><span data-stu-id="1b1f2-104">You can associate service tasks with service agreements or service orders in order to describe the service task to be completed for the agreement or order.</span></span> <span data-ttu-id="1b1f2-105">ข้อมูลนี้พร้อมใช้งานสำหรับช่างเทคนิคและลูกค้า</span><span class="sxs-lookup"><span data-stu-id="1b1f2-105">This information is available to service technicians and customers.</span></span>

## <a name="create-a-relation-with-a-service-agreement"></a><span data-ttu-id="1b1f2-106">สร้างความสัมพันธ์กับข้อตกลงการให้บริการ</span><span class="sxs-lookup"><span data-stu-id="1b1f2-106">Create a relation with a service agreement</span></span>

1.  <span data-ttu-id="1b1f2-107">คลิก **การจัดการบริการ** \> **ทั่วไป** \> **ข้อตกลงการให้บริการ** \> **ข้อตกลงการให้บริการ**</span><span class="sxs-lookup"><span data-stu-id="1b1f2-107">Click **Service management** \> **Common** \> **Service agreements** \> **Service agreements**.</span></span>

2.  <span data-ttu-id="1b1f2-108">เลือกข้อตกลงการให้บริการที่มีอยู่ หรือสร้างข้อตกลงการให้บริการใหม่</span><span class="sxs-lookup"><span data-stu-id="1b1f2-108">Select an existing service agreement, or create a new service agreement.</span></span>

3.  <span data-ttu-id="1b1f2-109">บนบานหน้าต่างการดำเนินงาน คลิกปุ่ม **ภารกิจการให้บริการ**</span><span class="sxs-lookup"><span data-stu-id="1b1f2-109">On the Action Pane, click the **Service tasks** button.</span></span>

4.  <span data-ttu-id="1b1f2-110">ในฟอร์ม **ภารกิจการให้บริการ** กด CTRL + N เพื่อสร้างรายการใหม่ และจากนั้น เลือกภารกิจการให้บริการจากรายการ **ภารกิจการให้บริการ** เพื่อแนบภารกิจการให้บริการกับข้อตกลงการให้บริการ</span><span class="sxs-lookup"><span data-stu-id="1b1f2-110">On the **Service tasks** form, press CTRL+N to create a new line, and then select a service task from the **Service task** list to attach the service task to the service agreement.</span></span>

5.  <span data-ttu-id="1b1f2-111">บนแท็บ **คำอธิบาย** ป้อนคำอธิบายหมายเหตุภายในหรือภายนอกใดๆ ในฟิลด์ข้อความอิสระ</span><span class="sxs-lookup"><span data-stu-id="1b1f2-111">On the **Description** tab, enter any internal or external note descriptions in the free text fields.</span></span>

6.  <span data-ttu-id="1b1f2-112">ปิดแบบฟอร์มเพื่อบันทึกเรกคอร์ด</span><span class="sxs-lookup"><span data-stu-id="1b1f2-112">Close the form to save the record.</span></span>

<span data-ttu-id="1b1f2-113">ทำขั้นตอนนี้ซ้ำจนกระทั่งคุณได้สร้างความสัมพันธ์ของภารกิจการให้บริการทั้งหมดที่จำเป็นสำหรับข้อตกลงการให้บริการ </span><span class="sxs-lookup"><span data-stu-id="1b1f2-113">Repeat this procedure until you have created all the necessary service task relations for the service agreement.</span></span> <span data-ttu-id="1b1f2-114">ขณะนี้คุณสามารถระบุภารกิจการให้บริการเหล่านี้สำหรับบรรทัดข้อตกลงใดๆ ที่แนบได้</span><span class="sxs-lookup"><span data-stu-id="1b1f2-114">You can now specify these service tasks for any attached agreement lines.</span></span>

<span data-ttu-id="1b1f2-115">ความสัมพันธ์ของภารกิจการให้บริการที่สร้างในข้อตกลงการให้บริการสามารถใช้งานได้จากใบสั่งบริการทั้งหมดที่แนบกับข้อตกลงการให้บริการ</span><span class="sxs-lookup"><span data-stu-id="1b1f2-115">A service tasks relation that is created on a service agreement is available from all service orders that are attached to the service agreement.</span></span>

## <a name="create-a-relation-with-a-service-order"></a><span data-ttu-id="1b1f2-116">สร้างความสัมพันธ์กับใบสั่งบริการ</span><span class="sxs-lookup"><span data-stu-id="1b1f2-116">Create a relation with a service order</span></span>

1.  <span data-ttu-id="1b1f2-117">คลิก **การจัดการบริการ** \> **ทั่วไป** \> **ใบสั่งบริการ** \> **ใบสั่งบริการ**</span><span class="sxs-lookup"><span data-stu-id="1b1f2-117">Click **Service management** \> **Common** \> **Service orders** \> **Service orders**.</span></span>

2.  <span data-ttu-id="1b1f2-118">เลือกใบสั่งบริการที่มีอยู่แล้ว หรือสร้างใบสั่งบริการใหม่</span><span class="sxs-lookup"><span data-stu-id="1b1f2-118">Select an existing service order, or create a new service order.</span></span>

3.  <span data-ttu-id="1b1f2-119">บนบานหน้าต่างการดำเนินงาน คลิกปุ่ม **ภารกิจการให้บริการ**</span><span class="sxs-lookup"><span data-stu-id="1b1f2-119">On the Action Pane, click the **Service tasks** button.</span></span>

4.  <span data-ttu-id="1b1f2-120">จากฟอร์ม **ภารกิจการให้บริการ** กด CTRL + N เพื่อสร้างรายการใหม่ และจากนั้น เลือกภารกิจการให้บริการจากรายการ **ภารกิจการให้บริการ** เพื่อแนบภารกิจการให้บริการกับข้อตกลงการให้บริการ</span><span class="sxs-lookup"><span data-stu-id="1b1f2-120">From the **Service tasks** form, press CTRL+N to create a new line, and then select a service task from the **Service task** list to attach the service tasks to the service order.</span></span>

5.  <span data-ttu-id="1b1f2-121">บนแท็บ **คำอธิบาย** ป้อนคำอธิบายหมายเหตุภายในหรือภายนอกใดๆ ในฟิลด์ข้อความอิสระ</span><span class="sxs-lookup"><span data-stu-id="1b1f2-121">On the **Description** tab, enter any internal or external note descriptions in the free text fields.</span></span>

6.  <span data-ttu-id="1b1f2-122">ปิดแบบฟอร์มเพื่อบันทึกเรกคอร์ด</span><span class="sxs-lookup"><span data-stu-id="1b1f2-122">Close the form to save the record.</span></span>

<span data-ttu-id="1b1f2-123">ทำขั้นตอนนี้ซ้ำจนกระทั่งคุณได้สร้างความสัมพันธ์ของภารกิจการให้บริการทั้งหมดที่จำเป็นสำหรับใบสั่งบริการ</span><span class="sxs-lookup"><span data-stu-id="1b1f2-123">Repeat this procedure until you have created all the necessary service task relations for the service order.</span></span> <span data-ttu-id="1b1f2-124">ขณะนี้คุณสามารถเลือกภารกิจการให้บริการที่คุณได้สร้างความสัมพันธ์ให้เมื่อคุณสร้างบรรทัดใบสั่งบริการ</span><span class="sxs-lookup"><span data-stu-id="1b1f2-124">You can now select the service task for which you have created the relation when you create service order lines.</span></span>

<span data-ttu-id="1b1f2-125">ความสัมพันธ์ของภารกิจการให้บริการที่สร้างในใบสั่งบริการจะสามารถใช้งานได้ในใบสั่งบริการที่ระบุ</span><span class="sxs-lookup"><span data-stu-id="1b1f2-125">Service task relations that are created on a service order are available on the specific service order.</span></span>

## <a name="see-also"></a><span data-ttu-id="1b1f2-126">ดูเพิ่มเติมที่</span><span class="sxs-lookup"><span data-stu-id="1b1f2-126">See also</span></span>

[<span data-ttu-id="1b1f2-127">ภาพรวมของงานบริการ</span><span class="sxs-lookup"><span data-stu-id="1b1f2-127">Service tasks overview</span></span>](service-tasks.md)


  


