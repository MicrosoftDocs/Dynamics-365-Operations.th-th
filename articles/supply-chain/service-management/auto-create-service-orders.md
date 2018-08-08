---
title: "สร้างใบสั่งบริการโดยอัตโนมัติ"
description: "คุณสามารถสร้างใบสั่งบริการที่ขึ้นกับข้อตกลงการให้บริการได้ สำหรับรอบระยะเวลาที่มีผลบังคับใช้ของข้อตกลงการให้บริการ"
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
ms.openlocfilehash: 0189a9f99ffbb6ed2387211ba9e3b9f3bcdb3b52
ms.contentlocale: th-th
ms.lasthandoff: 08/07/2018

---

# <a name="automatically-create-service-orders"></a><span data-ttu-id="57e11-103">สร้างใบสั่งบริการโดยอัตโนมัติ</span><span class="sxs-lookup"><span data-stu-id="57e11-103">Automatically create service orders</span></span> 

[!include [banner](../includes/banner.md)]


<span data-ttu-id="57e11-104">คุณสามารถสร้างใบสั่งบริการที่ขึ้นกับข้อตกลงการให้บริการได้ สำหรับรอบระยะเวลาที่มีผลบังคับใช้ของข้อตกลงการให้บริการ</span><span class="sxs-lookup"><span data-stu-id="57e11-104">You can generate service orders that are based on a service agreement for the valid period of the service agreement.</span></span>

<span data-ttu-id="57e11-105">ใบสั่งบริการที่คุณสร้างจากข้อตกลงการให้บริการจะถูกแนบกับข้อตกลงการให้บริการทั้งหมด</span><span class="sxs-lookup"><span data-stu-id="57e11-105">The service orders that you generate from a service agreement are all attached to the service agreement.</span></span>

<span data-ttu-id="57e11-106">ใบสั่งบริการมีการสร้างขึ้นโดยอัตโนมัติจากการตั้งค่าต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="57e11-106">Service orders are generated automatically from the following settings:</span></span>

  - <span data-ttu-id="57e11-107">ช่วงเวลาของข้อตกลงการให้บริการที่ถูกตั้งค่าในรายการข้อตกลงการให้บริการ</span><span class="sxs-lookup"><span data-stu-id="57e11-107">The service agreement interval that is set up in the service agreement lines.</span></span> <span data-ttu-id="57e11-108">ช่วงเวลาของข้อตกลงการให้บริการบ่งชี้ความถี่ที่มีการสร้างรายการใบสั่งบริการ</span><span class="sxs-lookup"><span data-stu-id="57e11-108">The service agreement interval indicates the frequency that service-order lines are created.</span></span> <span data-ttu-id="57e11-109">สำหรับข้อมูลเพิ่มเติม ให้ดูที่ [ช่วงเวลาการให้บริการ](service-intervals.md)</span><span class="sxs-lookup"><span data-stu-id="57e11-109">For more information, see [Service intervals](service-intervals.md).</span></span>

  - <span data-ttu-id="57e11-110">รอบระยะเวลาที่คุณระบุเพื่อกำหนดรอบระยะเวลาการบริการในฟิลด์ **วันที่เริ่มต้น** และ **วันที่สิ้นสุด** ในแบบฟอร์ม **สร้างใบสั่งบริการ**</span><span class="sxs-lookup"><span data-stu-id="57e11-110">The period that you specify to define the service period in the **From date** and **To date** fields in the **Create service orders** form.</span></span> <span data-ttu-id="57e11-111">สำหรับข้อมูลเพิ่มเติม ให้ดูที่ [สร้างใบสั่งบริการโดยอัตโนมัติ](create-service-orders-automatically.md)</span><span class="sxs-lookup"><span data-stu-id="57e11-111">For more information, see [Create service orders automatically](create-service-orders-automatically.md).</span></span>

  - <span data-ttu-id="57e11-112">ตัวเลือก **รวมใบสั่งบริการ** บนส่วนหัวของข้อตกลงการให้บริการ</span><span class="sxs-lookup"><span data-stu-id="57e11-112">The **Combine service orders** option on the service agreement header.</span></span> <span data-ttu-id="57e11-113">ตัวเลือกนี้กำหนดว่าจะมีการสร้างรายการใบสั่งบริการจากข้อตกลงการให้บริการ จะรวมใบสั่งบริการตามพนักงาน ภารกิจการให้บริการ วัตถุที่ให้บริการ หรือข้อตกลงการให้บริการ</span><span class="sxs-lookup"><span data-stu-id="57e11-113">This option defines whether service order lines generated from a service agreement, combines service orders according to employee, service task, service object, or service agreement.</span></span> <span data-ttu-id="57e11-114">สำหรับข้อมูลเพิ่มเติม ให้ดูที่ [รวมใบสั่งบริการ](combine-service-orders.md)</span><span class="sxs-lookup"><span data-stu-id="57e11-114">For more information, see [Combine service orders](combine-service-orders.md).</span></span>

  - <span data-ttu-id="57e11-115">ตัวเลือก **กรอบเวลา** ในรายการข้อตกลงการให้บริการ</span><span class="sxs-lookup"><span data-stu-id="57e11-115">The **Time window** option on the service agreement line.</span></span> <span data-ttu-id="57e11-116">กรอบเวลากำหนดว่ารายการใบสั่งบริการสามารถย้ายไปได้ไกลเพียงใด เมื่อคำนึงถึงวันที่ที่คำนวณได้</span><span class="sxs-lookup"><span data-stu-id="57e11-116">The time window defines how far a service order line can move with regard to its calculated date.</span></span> <span data-ttu-id="57e11-117">สำหรับข้อมูลเพิ่มเติม ให้ดูที่ [หน้าต่างเวลา](time-windows.md)</span><span class="sxs-lookup"><span data-stu-id="57e11-117">For more information, see [Time windows](time-windows.md).</span></span>


> [!NOTE]
> <P><span data-ttu-id="57e11-118">ถ้าวันที่ถูกระบุสำหรับใบสั่งบริการไม่เปิดขึ้นในปฏิทินที่คุณได้เลือกไว้ในแบบฟอร์ม <STRONG>พารามิเตอร์การจัดการงานบริการ</STRONG> ข้อความจะแจ้งว่า มีความขัดแย้งของปฏิทิน</span><span class="sxs-lookup"><span data-stu-id="57e11-118">If the day that is specified for a service order is not open in the calendar that you have selected in the <STRONG>Service management parameters</STRONG> form, a message will indicate that there is a calendar conflict.</span></span> <span data-ttu-id="57e11-119">คุณสามารถละเว้นข้อความนี้ได้อย่างปลอดภัย; และจะมีการสร้างใบสั่งบริการขึ้น แม้ว่าวันจะปิดอยู่ในปฏิทิน</span><span class="sxs-lookup"><span data-stu-id="57e11-119">You can safely ignore the message; the service order will be created, even though the day is closed on the calendar.</span></span></P>

## <a name="example-1"></a><span data-ttu-id="57e11-120">ตัวอย่างที่ 1</span><span class="sxs-lookup"><span data-stu-id="57e11-120">Example 1</span></span>

<span data-ttu-id="57e11-121">ข้อตกลงการให้บริการมีผลตั้งแต่วันที่ 1 มกราคม 2012 จนถึงวันที่ 31 ธันวาคม 2012</span><span class="sxs-lookup"><span data-stu-id="57e11-121">The service agreement lasts from January 1, 2012 until December 31, 2012.</span></span> <span data-ttu-id="57e11-122">ถ้ารอบระยะเวลาการให้บริการที่คุณระบุในแบบฟอร์ม **สร้างใบสั่งบริการ** เริ่มตั้งแต่ 1 พฤศจิกายน 2012 จนถึงวันที่ 1 กุมภาพันธ์ 2013 จะมีการสร้างใบสั่งบริการตั้งแต่ 1 พฤศจิกายน 2012 จนถึงวันที่ 31 ธันวาคม 2012</span><span class="sxs-lookup"><span data-stu-id="57e11-122">If the service period that you specify in the **Create service orders** form is from November 1, 2012 until February 1, 2013, service orders are created from November 1, 2012 until December 31, 2012.</span></span>

## <a name="example-2"></a><span data-ttu-id="57e11-123">ตัวอย่างที่ 2</span><span class="sxs-lookup"><span data-stu-id="57e11-123">Example 2</span></span>

<span data-ttu-id="57e11-124">ข้อตกลงการให้บริการมีผลตั้งแต่วันที่ 1 มกราคม 2012 จนถึงวันที่ 31 ธันวาคม 2012</span><span class="sxs-lookup"><span data-stu-id="57e11-124">The service agreement lasts from January 1, 2012 until December 31, 2012.</span></span> <span data-ttu-id="57e11-125">รายการข้อตกลงการให้บริการสองรายการถูกแนบไปยังข้อตกลงการให้บริการ</span><span class="sxs-lookup"><span data-stu-id="57e11-125">Two service agreement lines are attached to the service agreement.</span></span> <span data-ttu-id="57e11-126">รายการข้อตกลงการให้บริการแรกมีวันที่เริ่มต้นเมื่อวันที่ 2 มกราคม 2012 และวันที่สิ้นสุดเมื่อวันที่ 1 มีนาคม 2012</span><span class="sxs-lookup"><span data-stu-id="57e11-126">The first service agreement line has a starting date on January 2, 2012 and an ending date on March 1, 2012.</span></span> <span data-ttu-id="57e11-127">รายการข้อตกลงการให้บริการที่สองมีวันที่เริ่มต้นเมื่อวันที่ 1 เมษายน 2012 และวันที่สิ้นสุดเมื่อวันที่ 31 ธันวาคม 2012</span><span class="sxs-lookup"><span data-stu-id="57e11-127">The second service agreement line has a starting date on April 1, 2012 and an ending date on December 31, 2012.</span></span> <span data-ttu-id="57e11-128">คุณระบุรอบระยะเวลาในแบบฟอร์ม **สร้างใบสั่งบริการ** ที่เริ่มตั้งแต่วันที่ 1 ตุลาคม 2012 จนถึงวันที่ 31 ธันวาคม 2012</span><span class="sxs-lookup"><span data-stu-id="57e11-128">You specify a period in the **Create service orders** form that is from October 1, 2012 until December 31, 2012.</span></span> <span data-ttu-id="57e11-129">ดังนั้น ใบสั่งบริการจะถูกสร้างสำหรับรายการข้อตกลงที่สองเท่านั้น เนื่องจากวันที่เริ่มต้นและวันที่สิ้นสุดของรายการข้อตกลงแรกสิ้นสุดก่อนรอบระยะเวลาที่คุณระบุไว้สำหรับใบสั่งบริการ</span><span class="sxs-lookup"><span data-stu-id="57e11-129">Therefore, service orders are generated only for the second agreement line, because the starting date and ending date of the first agreement line are before the period that you specified for the service order.</span></span>

  



