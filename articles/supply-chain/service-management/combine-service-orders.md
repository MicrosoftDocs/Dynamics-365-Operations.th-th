---
title: รวมใบสั่งบริการ
description: คุณสามารถรวมใบสั่งบริการได้
author: ShylaThompson
ms.date: 05/01/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: SMAServiceOrderTable
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 41b4a3234e4104372f1052d89c2417984e9cd10d
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 04/01/2021
ms.locfileid: "5840568"
---
# <a name="combine-service-orders"></a><span data-ttu-id="8791c-103">รวมใบสั่งบริการ</span><span class="sxs-lookup"><span data-stu-id="8791c-103">Combine service orders</span></span>   

[!include [banner](../includes/banner.md)]


<span data-ttu-id="8791c-104">เมื่อคุณสร้างรายการใบสั่งบริการได้โดยอัตโนมัติในแบบฟอร์ม **ข้อตกลงการให้บริการ** คุณสามารถเลือกหนึ่งในตัวเลือกต่อไปนี้เพื่อระบุวิธีที่คุณต้องการจัดกลุ่ม:</span><span class="sxs-lookup"><span data-stu-id="8791c-104">When you create service order lines automatically in the **Service agreements** form, you can choose one of the following options to specify how you want to group them:</span></span>

  - <span data-ttu-id="8791c-105">**โดยเรียงตามข้อตกลงการให้บริการ**</span><span class="sxs-lookup"><span data-stu-id="8791c-105">**By service agreement**</span></span>

  - <span data-ttu-id="8791c-106">**โดยเรียงตามงานบริการ**</span><span class="sxs-lookup"><span data-stu-id="8791c-106">**By service task**</span></span>

  - <span data-ttu-id="8791c-107">**โดยเรียงตามพนักงาน**</span><span class="sxs-lookup"><span data-stu-id="8791c-107">**By employee**</span></span>

  - <span data-ttu-id="8791c-108">**โดยเรียงตามวัตถุที่ให้บริการ**</span><span class="sxs-lookup"><span data-stu-id="8791c-108">**By service object**</span></span>

## <a name="example"></a><span data-ttu-id="8791c-109">ตัวอย่าง</span><span class="sxs-lookup"><span data-stu-id="8791c-109">Example</span></span>

<span data-ttu-id="8791c-110">คุณสร้างข้อตกลงการให้บริการที่มีวันที่เริ่มต้นในวันที่ 31-03-2007</span><span class="sxs-lookup"><span data-stu-id="8791c-110">You create a service agreement that has a start date on 03-31-2007.</span></span> <span data-ttu-id="8791c-111">ในฟิลด์ **รวมใบสั่งบริการ** คุณระบุ **ตามวัตถุที่ให้บริการ**</span><span class="sxs-lookup"><span data-stu-id="8791c-111">In the **Combine service orders** field, you specify **By service object**.</span></span> <span data-ttu-id="8791c-112">จากนั้นคุณก็สร้างบรรทัดข้อตกลงการให้บริการต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="8791c-112">You then create the following service agreement lines:</span></span>

<table style="width:100%;">
<colgroup>
<col style="width: 16%" />
<col style="width: 16%" />
<col style="width: 16%" />
<col style="width: 16%" />
<col style="width: 16%" />
<col style="width: 16%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="8791c-113">หมายเลขรายการข้อตกลง</span><span class="sxs-lookup"><span data-stu-id="8791c-113">Agreement line number</span></span></p></th>
<th><p><span data-ttu-id="8791c-114">ชนิดธุรกรรม</span><span class="sxs-lookup"><span data-stu-id="8791c-114">Transaction type</span></span></p></th>
<th><p><span data-ttu-id="8791c-115">คำอธิบาย</span><span class="sxs-lookup"><span data-stu-id="8791c-115">Description</span></span></p></th>
<th><p><span data-ttu-id="8791c-116">ช่วงเวลา</span><span class="sxs-lookup"><span data-stu-id="8791c-116">Interval</span></span></p></th>
<th><p><span data-ttu-id="8791c-117">วัตถุที่ให้บริการ</span><span class="sxs-lookup"><span data-stu-id="8791c-117">Service object</span></span></p></th>
<th><p><span data-ttu-id="8791c-118">วันที่เริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="8791c-118">Start date</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="8791c-119">1</span><span class="sxs-lookup"><span data-stu-id="8791c-119">1</span></span></p></td>
<td><p><span data-ttu-id="8791c-120"><strong>ชั่วโมง</strong></span><span class="sxs-lookup"><span data-stu-id="8791c-120"><strong>Hour</strong></span></span></p></td>
<td><p><span data-ttu-id="8791c-121">SAL1</span><span class="sxs-lookup"><span data-stu-id="8791c-121">SAL1</span></span></p></td>
<td><p><span data-ttu-id="8791c-122">รายสัปดาห์</span><span class="sxs-lookup"><span data-stu-id="8791c-122">Weekly</span></span></p></td>
<td><p><span data-ttu-id="8791c-123">X-1</span><span class="sxs-lookup"><span data-stu-id="8791c-123">X-1</span></span></p></td>
<td><p><span data-ttu-id="8791c-124">วันที่ 04-01-2007</span><span class="sxs-lookup"><span data-stu-id="8791c-124">04-01-2007</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8791c-125">2</span><span class="sxs-lookup"><span data-stu-id="8791c-125">2</span></span></p></td>
<td><p><span data-ttu-id="8791c-126"><strong>ชั่วโมง</strong></span><span class="sxs-lookup"><span data-stu-id="8791c-126"><strong>Hour</strong></span></span></p></td>
<td><p><span data-ttu-id="8791c-127">SAL2</span><span class="sxs-lookup"><span data-stu-id="8791c-127">SAL2</span></span></p></td>
<td><p><span data-ttu-id="8791c-128">ทุกสองสัปดาห์</span><span class="sxs-lookup"><span data-stu-id="8791c-128">Biweekly</span></span></p></td>
<td><p><span data-ttu-id="8791c-129">X-2</span><span class="sxs-lookup"><span data-stu-id="8791c-129">X-2</span></span></p></td>
<td><p><span data-ttu-id="8791c-130">วันที่ 04-01-2007</span><span class="sxs-lookup"><span data-stu-id="8791c-130">04-01-2007</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8791c-131">3</span><span class="sxs-lookup"><span data-stu-id="8791c-131">3</span></span></p></td>
<td><p><span data-ttu-id="8791c-132"><strong>ชั่วโมง</strong></span><span class="sxs-lookup"><span data-stu-id="8791c-132"><strong>Hour</strong></span></span></p></td>
<td><p><span data-ttu-id="8791c-133">SAL3</span><span class="sxs-lookup"><span data-stu-id="8791c-133">SAL3</span></span></p></td>
<td><p><span data-ttu-id="8791c-134">รายสัปดาห์</span><span class="sxs-lookup"><span data-stu-id="8791c-134">Weekly</span></span></p></td>
<td><p><span data-ttu-id="8791c-135">X-2</span><span class="sxs-lookup"><span data-stu-id="8791c-135">X-2</span></span></p></td>
<td><p><span data-ttu-id="8791c-136">วันที่ 04-01-2007</span><span class="sxs-lookup"><span data-stu-id="8791c-136">04-01-2007</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="8791c-137">คุณไม่ได้ระบุหน้าต่างเวลาสำหรับบรรทัดใดๆ ของข้อตกลงการให้บริการ </span><span class="sxs-lookup"><span data-stu-id="8791c-137">You do not specify time windows for any of the service agreement lines.</span></span> <span data-ttu-id="8791c-138">ดังนั้น รายการใบสั่งบริการจะไม่ย้ายจากวันที่ที่คำนวณไว้ซึ่งมีรายการเหล่านั้นอยู่</span><span class="sxs-lookup"><span data-stu-id="8791c-138">Therefore, the service order lines will not move from the calculated day on which they fall.</span></span>

<span data-ttu-id="8791c-139">จากนั้น คุณสร้างรายการใบสั่งบริการจากแบบฟอร์ม **สร้างใบสั่งบริการ** ตั้งแต่วันที่ 01-04-2007 จนถึงวันที่ 30-04-2007</span><span class="sxs-lookup"><span data-stu-id="8791c-139">Next, you generate service order lines from the **Create service orders** form from 04-01-2007 until 04-30-2007.</span></span>

<span data-ttu-id="8791c-140">คุณสร้างใบสั่งบริการรวมทั้งสิ้น 10 ฉบับ </span><span class="sxs-lookup"><span data-stu-id="8791c-140">In total, 10 service orders are created.</span></span> <span data-ttu-id="8791c-141">เนื่องจากการตั้งค่ารวมที่คุณเลือกไว้คือ **โดยเรียงตามวัตถุที่ให้บริการ** ใบสั่งบริการทั้งหมดที่ถูกสร้างขึ้นจึงมีเฉพาะรายการใบสั่งบริการที่มีวัตถุที่ให้บริการรายการเดียว</span><span class="sxs-lookup"><span data-stu-id="8791c-141">Because the combined setting that you selected was **By service object**, all service orders that are created have only service order lines with one specific service object.</span></span> <span data-ttu-id="8791c-142">รายการใบสั่งบริการที่ถูกสร้างขึ้นจากข้อตกลงการให้บริการ และมีวันที่ให้บริการเดียวกัน และวัตถุที่ให้บริการจะถูกรวมไว้ในใบสั่งบริการเดียวกัน</span><span class="sxs-lookup"><span data-stu-id="8791c-142">Service order lines that are generated from the service agreement and have the same service date and object are combined on the same service order.</span></span>


> [!NOTE]
> <P><span data-ttu-id="8791c-143">ในตัวอย่างนี้ ปฏิทินที่ถูกระบุไว้ในแบบฟอร์ม <STRONG>พารามิเตอร์การจัดการงานบริการ</STRONG> ไม่มีวันที่ปิด</span><span class="sxs-lookup"><span data-stu-id="8791c-143">In this example, the calendar that is specified in the <STRONG>Service management parameters</STRONG> form has no closed days.</span></span></P>



<span data-ttu-id="8791c-144">การจัดกลุ่มรายการใบสั่งบริการเพิ่มเติมเป็นใบสั่งบริการ จะเกิดขึ้นตามกรอบเวลาใดๆ ที่คุณระบุในรายการข้อตกลงการให้บริการ</span><span class="sxs-lookup"><span data-stu-id="8791c-144">Additional grouping of service order lines into service orders occurs according to any time window that you specify on the service agreement lines.</span></span>

## <a name="see-also"></a><span data-ttu-id="8791c-145">ดูเพิ่มเติมที่</span><span class="sxs-lookup"><span data-stu-id="8791c-145">See also</span></span>

[<span data-ttu-id="8791c-146">สร้างใบสั่งบริการโดยอัตโนมัติ</span><span class="sxs-lookup"><span data-stu-id="8791c-146">Create service orders automatically</span></span>](create-service-orders-automatically.md)

  




[!INCLUDE[footer-include](../../includes/footer-banner.md)]