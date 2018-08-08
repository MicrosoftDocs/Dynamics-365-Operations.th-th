---
title: "สร้างใบสั่งบริการโดยอัตโนมัติ"
description: "คุณสามารถสร้างใบสั่งบริการสำหรับข้อตกลงการให้บริการหนึ่งรายการ หรือสำหรับข้อตกลงการให้บริการหลายรายการได้"
author: ShylaThompson
manager: AnnBe
ms.date: 05/01/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: SMAServiceOrderTable
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 
ms.assetid: 
ms.search.region: Global
ms.author: ShylaThompson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 1d98cbff30620256c9d13e7b4a90314db150e33e
ms.openlocfilehash: ee68190b117b974ff4131f5d2237d138cac1fda3
ms.contentlocale: th-th
ms.lasthandoff: 08/07/2018

---

# <a name="create-service-orders-automatically"></a><span data-ttu-id="a6e81-103">สร้างใบสั่งบริการโดยอัตโนมัติ</span><span class="sxs-lookup"><span data-stu-id="a6e81-103">Create service orders automatically</span></span>    

[!include [banner](../includes/banner.md)]


<span data-ttu-id="a6e81-104">คุณสามารถสร้างใบสั่งบริการสำหรับข้อตกลงการให้บริการหนึ่งรายการ หรือสำหรับข้อตกลงการให้บริการหลายรายการได้</span><span class="sxs-lookup"><span data-stu-id="a6e81-104">You can create service orders for one service agreement or for several service agreements.</span></span> <span data-ttu-id="a6e81-105">เมื่อมีการสร้างใบแล้ว คุณสามารถดูใบสั่งบริการของคุณได้ในแบบฟอร์ม **ใบสั่งบริการ**</span><span class="sxs-lookup"><span data-stu-id="a6e81-105">When they are created, you can view your service orders in the **Service orders** form.</span></span>

<span data-ttu-id="a6e81-106">ใบสั่งบริการจะถูกสร้างขึ้นสำหรับรอบระยะเวลาที่มีผลบังคับใช้ของข้อตกลงการให้บริการเท่านั้น</span><span class="sxs-lookup"><span data-stu-id="a6e81-106">Service orders are created only for the valid period of the service agreement.</span></span> <span data-ttu-id="a6e81-107">ถ้าช่วงเวลาที่คุณระบุในแบบฟอร์ม **สร้างใบสั่งบริการ** อยู่ก่อนวันที่เริ่มต้นหรือหลังจากวันที่สิ้นสุดของข้อตกลงการให้บริการ ใบสั่งบริการจะถูกสร้างขึ้นสำหรับส่วนของช่วงเวลา ที่อยู่ภายในข้อตกลงการให้บริการเท่านั้น</span><span class="sxs-lookup"><span data-stu-id="a6e81-107">If the interval that you specify in the **Create service orders** form is before the starting date or after the ending date of the service agreement, service orders are created only for the part of the interval that is within the service agreement dates.</span></span>

<span data-ttu-id="a6e81-108">เมื่อคุณสร้างใบสั่งบริการด้วยตนเองหรือโดยอัตโนมัติจากรายการข้อตกลงการให้บริการ ใบสั่งบริการต้องอยู่ในช่วงเวลาที่กำหนดโดยวันที่เริ่มต้นและวันที่สิ้นสุดสำหรับรายการ เว้นเสียแต่ว่าคุณไม่ได้ระบุวันที่สิ้นสุดในรายการ</span><span class="sxs-lookup"><span data-stu-id="a6e81-108">When you create service orders manually or automatically from the service agreement line, the service order must be in the time interval that is defined by the starting and ending dates for the line, unless you do not specify an ending date on the line.</span></span>

## <a name="create-service-orders-automatically-for-a-service-agreement"></a><span data-ttu-id="a6e81-109">การสร้างใบสั่งบริการโดยอัตโนมัติสำหรับข้อตกลงการให้บริการ</span><span class="sxs-lookup"><span data-stu-id="a6e81-109">Create service orders automatically for a service agreement</span></span>

1.  <span data-ttu-id="a6e81-110">คลิก **การจัดการบริการ** \> **ทั่วไป** \> **ข้อตกลงการให้บริการ** \> **ข้อตกลงการให้บริการ**</span><span class="sxs-lookup"><span data-stu-id="a6e81-110">Click **Service management** \> **Common** \> **Service agreements** \> **Service agreements**.</span></span>

2.  <span data-ttu-id="a6e81-111">เลือกข้อตกลงการให้บริการ</span><span class="sxs-lookup"><span data-stu-id="a6e81-111">Select a service agreement.</span></span>

3.  <span data-ttu-id="a6e81-112">คลิกแท็บ **ส่ง** และจากนั้นคลิก **ใบสั่งบริการที่วางแผนไว้**</span><span class="sxs-lookup"><span data-stu-id="a6e81-112">Click the **Deliver** tab, and then click **Planned service orders**.</span></span>

4.  <span data-ttu-id="a6e81-113">ระบุวันที่ในฟิลด์ **วันที่เริ่มต้น** และ **วันที่สิ้นสุด** เพื่อกำหนดรอบระยะเวลาการให้บริการ</span><span class="sxs-lookup"><span data-stu-id="a6e81-113">Specify dates in the **From date** and **To date** fields to define the service period.</span></span>

5.  <span data-ttu-id="a6e81-114">เลือกกล่องกาเครื่องหมาย **แสดง Infolog** เพื่อแสดงรายการของใบสั่งบริการที่สร้างขึ้น</span><span class="sxs-lookup"><span data-stu-id="a6e81-114">Select the **Show Infolog** check box to display a list of the service orders that are created.</span></span>

6.  <span data-ttu-id="a6e81-115">เลือกชนิดของธุรกรรมในกลุ่มฟิลด์ **รวมชนิดของธุรกรรม**</span><span class="sxs-lookup"><span data-stu-id="a6e81-115">Select transaction types in the **Include transaction types** field group.</span></span> <span data-ttu-id="a6e81-116">ชนิดธุรกรรมจะแสดงถึงบรรทัดที่สร้างขึ้นในข้อตกลงการให้บริการ และธุรกรรมแต่ละชนิดที่คุณเลือกจะสร้างใบสั่งบริการหลายใบ โดยขึ้นอยู่กับช่วงเวลาการให้บริการที่ระบุในบรรทัดข้อตกลงการให้บริการ</span><span class="sxs-lookup"><span data-stu-id="a6e81-116">The transaction types represent the lines that are created in the service agreement, and each transaction type that you select generates several service orders, depending on the service interval that is specified on the service agreement line.</span></span>

7.  <span data-ttu-id="a6e81-117">ในการสร้างใบสั่งบริการใดๆ ที่ขาดไปจากชุดใบสั่งบริการแบบต่อเนื่อง เลือกกล่องกาเครื่องหมาย **แบบต่อเนื่อง**</span><span class="sxs-lookup"><span data-stu-id="a6e81-117">To create any service orders that are missing from continuous series of service orders, select the **Continuous** check box.</span></span>

8.  <span data-ttu-id="a6e81-118">คลิก **ตกลง** </span><span class="sxs-lookup"><span data-stu-id="a6e81-118">Click **OK**.</span></span>

## <a name="create-service-orders-automatically-for-several-service-agreements"></a><span data-ttu-id="a6e81-119">การสร้างใบสั่งบริการโดยอัตโนมัติสำหรับข้อตกลงการให้บริการหลายฉบับ</span><span class="sxs-lookup"><span data-stu-id="a6e81-119">Create service orders automatically for several service agreements</span></span>

1.  <span data-ttu-id="a6e81-120">คลิก **การจัดการบริการ** \> **งานประจำงวด** \> **ใบสั่งบริการ** \> **สร้างใบสั่งบริการ**</span><span class="sxs-lookup"><span data-stu-id="a6e81-120">Click **Service management** \> **Periodic** \> **Service orders** \> **Create service orders**.</span></span>

2.  <span data-ttu-id="a6e81-121">คลิก **เลือก** เพื่อทำการเลือก เพื่อเพิ่มหรือลบเกณฑ์ที่จะใช้ในการสร้างใบสั่งบริการ</span><span class="sxs-lookup"><span data-stu-id="a6e81-121">Click **Select** to make selections to add or remove criteria to use to create service orders.</span></span>

3.  <span data-ttu-id="a6e81-122">คลิก **ตกลง** </span><span class="sxs-lookup"><span data-stu-id="a6e81-122">Click **OK**.</span></span>

## <a name="see-also"></a><span data-ttu-id="a6e81-123">ดูเพิ่มเติมที่</span><span class="sxs-lookup"><span data-stu-id="a6e81-123">See also</span></span>

[<span data-ttu-id="a6e81-124">ใบสั่งบริการ</span><span class="sxs-lookup"><span data-stu-id="a6e81-124">Service orders</span></span>](service-orders.md)

[<span data-ttu-id="a6e81-125">การสร้างใบสั่งบริการโดยอัตโนมัติ</span><span class="sxs-lookup"><span data-stu-id="a6e81-125">Automatically creating service orders</span></span>](auto-create-service-orders.md)

  



