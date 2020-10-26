---
title: สถานะการให้บริการและการโต้ตอบของฟิลด์ความก้าวหน้า
description: ในแบบฟอร์มใบสั่งบริการ ฟิลด์กระบวนการบนส่วนหัวจะแสดงสถานะของใบสั่งบริการทั้งหมด และสถานะจะรายงานสถานะของรายการของใบสั่งบริการแต่ละรายการ
author: ShylaThompson
manager: tfehr
ms.date: 05/01/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SMAServiceOrderTable
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: a94f2df6a4ddb71a29ff951dfe38618ac7762783
ms.sourcegitcommit: 708ca25687a4e48271cdcd6d2d22d99fb94cf140
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 10/10/2020
ms.locfileid: "3975499"
---
# <a name="service-status-and-progress-field-interaction"></a><span data-ttu-id="c9ffc-103">สถานะการให้บริการและการโต้ตอบของฟิลด์ความก้าวหน้า</span><span class="sxs-lookup"><span data-stu-id="c9ffc-103">Service status and progress field interaction</span></span> 

[!include [banner](../includes/banner.md)]


<span data-ttu-id="c9ffc-104">ในแบบฟอร์ม **ใบสั่งบริการ** ฟิลด์ **กระบวนการ** บนส่วนหัวของใบสั่งบริการ จะแสดงสถานะของใบสั่งบริการทั้งหมด และ **สถานะ** จะรายงานสถานะของรายการของใบสั่งบริการแต่ละรายการ</span><span class="sxs-lookup"><span data-stu-id="c9ffc-104">In the **Service orders** form, the **Progress** field on the service order header reflects the status of the whole service order, and the **Status** reports the status of individual service order lines.</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="c9ffc-105">ความคืบหน้า</span><span class="sxs-lookup"><span data-stu-id="c9ffc-105">Progress</span></span></p></th>
<th><p><span data-ttu-id="c9ffc-106">สถานะบรรทัด 1</span><span class="sxs-lookup"><span data-stu-id="c9ffc-106">Line 1 Status</span></span></p></th>
<th><p><span data-ttu-id="c9ffc-107">สถานะบรรทัด 2</span><span class="sxs-lookup"><span data-stu-id="c9ffc-107">Line 2 Status</span></span></p></th>
<th><p><span data-ttu-id="c9ffc-108">สถานะบรรทัด 3</span><span class="sxs-lookup"><span data-stu-id="c9ffc-108">Line 3 Status</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="c9ffc-109"><strong>อยู่ระหว่างดำเนินการ</strong></span><span class="sxs-lookup"><span data-stu-id="c9ffc-109"><strong>In process</strong></span></span></p></td>
<td><p><span data-ttu-id="c9ffc-110"><strong>สร้างแล้ว</strong></span><span class="sxs-lookup"><span data-stu-id="c9ffc-110"><strong>Created</strong></span></span></p></td>
<td><p><span data-ttu-id="c9ffc-111"><strong>สร้างแล้ว</strong></span><span class="sxs-lookup"><span data-stu-id="c9ffc-111"><strong>Created</strong></span></span></p></td>
<td><p><span data-ttu-id="c9ffc-112"><strong>สร้างแล้ว</strong></span><span class="sxs-lookup"><span data-stu-id="c9ffc-112"><strong>Created</strong></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c9ffc-113"><strong>อยู่ระหว่างดำเนินการ</strong></span><span class="sxs-lookup"><span data-stu-id="c9ffc-113"><strong>In process</strong></span></span></p></td>
<td><p><span data-ttu-id="c9ffc-114"><strong>ยกเลิก</strong></span><span class="sxs-lookup"><span data-stu-id="c9ffc-114"><strong>Canceled</strong></span></span></p></td>
<td><p><span data-ttu-id="c9ffc-115"><strong>สร้างแล้ว</strong></span><span class="sxs-lookup"><span data-stu-id="c9ffc-115"><strong>Created</strong></span></span></p></td>
<td><p><span data-ttu-id="c9ffc-116"><strong>สร้างแล้ว</strong></span><span class="sxs-lookup"><span data-stu-id="c9ffc-116"><strong>Created</strong></span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c9ffc-117"><strong>อยู่ระหว่างดำเนินการ</strong></span><span class="sxs-lookup"><span data-stu-id="c9ffc-117"><strong>In process</strong></span></span></p></td>
<td><p><span data-ttu-id="c9ffc-118"><strong>สร้างแล้ว</strong></span><span class="sxs-lookup"><span data-stu-id="c9ffc-118"><strong>Created</strong></span></span></p></td>
<td><p><span data-ttu-id="c9ffc-119"><strong>ยกเลิก</strong></span><span class="sxs-lookup"><span data-stu-id="c9ffc-119"><strong>Canceled</strong></span></span></p></td>
<td><p><span data-ttu-id="c9ffc-120"><strong>ประกาศแล้ว</strong></span><span class="sxs-lookup"><span data-stu-id="c9ffc-120"><strong>Posted</strong></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c9ffc-121"><strong>ยกเลิก</strong></span><span class="sxs-lookup"><span data-stu-id="c9ffc-121"><strong>Canceled</strong></span></span></p></td>
<td><p><span data-ttu-id="c9ffc-122"><strong>ยกเลิก</strong></span><span class="sxs-lookup"><span data-stu-id="c9ffc-122"><strong>Canceled</strong></span></span></p></td>
<td><p><span data-ttu-id="c9ffc-123"><strong>ยกเลิก</strong></span><span class="sxs-lookup"><span data-stu-id="c9ffc-123"><strong>Canceled</strong></span></span></p></td>
<td><p><span data-ttu-id="c9ffc-124"><strong>ยกเลิก</strong></span><span class="sxs-lookup"><span data-stu-id="c9ffc-124"><strong>Canceled</strong></span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c9ffc-125"><strong>ประกาศแล้ว</strong></span><span class="sxs-lookup"><span data-stu-id="c9ffc-125"><strong>Posted</strong></span></span></p></td>
<td><p><span data-ttu-id="c9ffc-126"><strong>ประกาศแล้ว</strong></span><span class="sxs-lookup"><span data-stu-id="c9ffc-126"><strong>Posted</strong></span></span></p></td>
<td><p><span data-ttu-id="c9ffc-127"><strong>ประกาศแล้ว</strong></span><span class="sxs-lookup"><span data-stu-id="c9ffc-127"><strong>Posted</strong></span></span></p></td>
<td><p><span data-ttu-id="c9ffc-128"><strong>ประกาศแล้ว</strong></span><span class="sxs-lookup"><span data-stu-id="c9ffc-128"><strong>Posted</strong></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c9ffc-129"><strong>ประกาศแล้ว</strong></span><span class="sxs-lookup"><span data-stu-id="c9ffc-129"><strong>Posted</strong></span></span></p></td>
<td><p><span data-ttu-id="c9ffc-130"><strong>ประกาศแล้ว</strong></span><span class="sxs-lookup"><span data-stu-id="c9ffc-130"><strong>Posted</strong></span></span></p></td>
<td><p><span data-ttu-id="c9ffc-131"><strong>ยกเลิก</strong></span><span class="sxs-lookup"><span data-stu-id="c9ffc-131"><strong>Canceled</strong></span></span></p></td>
<td><p><span data-ttu-id="c9ffc-132"><strong>ยกเลิก</strong></span><span class="sxs-lookup"><span data-stu-id="c9ffc-132"><strong>Canceled</strong></span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="c9ffc-133">ความก้าวหน้าของใบสั่งบริการอยู่ระหว่างดำเนินการ หากทุกรายการมีสถานะ **สร้างแล้ว**; ใบสั่งนั้นยังอยู่ระหว่างดำเนินการ หากบางรายการมีสถานะเป็น **ยกเลิกแล้ว** หรือ **ลงรายการบัญชีแล้ว**</span><span class="sxs-lookup"><span data-stu-id="c9ffc-133">The progress of a service order is in process if all lines have the status **Created**; it is still in process if some of the lines have a status of **Canceled** or **Posted**.</span></span>

<span data-ttu-id="c9ffc-134">ถ้าทุกรายการใบสั่งบริการถูกทำเครื่องหมายเป็น **ลงรายการบัญชีแล้ว** ความก้าวหน้าของใบสั่งสถานะจะเป็น **ลงรายการบัญชีแล้ว**</span><span class="sxs-lookup"><span data-stu-id="c9ffc-134">If all lines in a service order are marked as **Posted**, the progress of the status order is **Posted**.</span></span> <span data-ttu-id="c9ffc-135">ถ้าบางรายการเป็น **ลงรายการบัญชีแล้ว** และบางรายการเป็น **ยกเลิกแล้ว** ความก้าวหน้าจะยังคงเป็น **ลงรายการบัญชีแล้ว**</span><span class="sxs-lookup"><span data-stu-id="c9ffc-135">If some lines are **Posted** and some are **Canceled**, the progress is still **Posted**.</span></span>

  


