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
ms.author: ShylaThompson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: bd70d00f7ce531b225362065dfd9f1f5c1adc754
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 04/02/2020
ms.locfileid: "3207335"
---
# <a name="service-status-and-progress-field-interaction"></a><span data-ttu-id="cb3f1-103">สถานะการให้บริการและการโต้ตอบของฟิลด์ความก้าวหน้า</span><span class="sxs-lookup"><span data-stu-id="cb3f1-103">Service status and progress field interaction</span></span> 

[!include [banner](../includes/banner.md)]


<span data-ttu-id="cb3f1-104">ในแบบฟอร์ม **ใบสั่งบริการ** ฟิลด์ **กระบวนการ** บนส่วนหัวของใบสั่งบริการ จะแสดงสถานะของใบสั่งบริการทั้งหมด และ **สถานะ** จะรายงานสถานะของรายการของใบสั่งบริการแต่ละรายการ</span><span class="sxs-lookup"><span data-stu-id="cb3f1-104">In the **Service orders** form, the **Progress** field on the service order header reflects the status of the whole service order, and the **Status** reports the status of individual service order lines.</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="cb3f1-105">ความคืบหน้า</span><span class="sxs-lookup"><span data-stu-id="cb3f1-105">Progress</span></span></p></th>
<th><p><span data-ttu-id="cb3f1-106">สถานะบรรทัด 1</span><span class="sxs-lookup"><span data-stu-id="cb3f1-106">Line 1 Status</span></span></p></th>
<th><p><span data-ttu-id="cb3f1-107">สถานะบรรทัด 2</span><span class="sxs-lookup"><span data-stu-id="cb3f1-107">Line 2 Status</span></span></p></th>
<th><p><span data-ttu-id="cb3f1-108">สถานะบรรทัด 3</span><span class="sxs-lookup"><span data-stu-id="cb3f1-108">Line 3 Status</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="cb3f1-109"><strong>อยู่ระหว่างดำเนินการ</strong></span><span class="sxs-lookup"><span data-stu-id="cb3f1-109"><strong>In process</strong></span></span></p></td>
<td><p><span data-ttu-id="cb3f1-110"><strong>สร้างแล้ว</strong></span><span class="sxs-lookup"><span data-stu-id="cb3f1-110"><strong>Created</strong></span></span></p></td>
<td><p><span data-ttu-id="cb3f1-111"><strong>สร้างแล้ว</strong></span><span class="sxs-lookup"><span data-stu-id="cb3f1-111"><strong>Created</strong></span></span></p></td>
<td><p><span data-ttu-id="cb3f1-112"><strong>สร้างแล้ว</strong></span><span class="sxs-lookup"><span data-stu-id="cb3f1-112"><strong>Created</strong></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cb3f1-113"><strong>อยู่ระหว่างดำเนินการ</strong></span><span class="sxs-lookup"><span data-stu-id="cb3f1-113"><strong>In process</strong></span></span></p></td>
<td><p><span data-ttu-id="cb3f1-114"><strong>ยกเลิก</strong></span><span class="sxs-lookup"><span data-stu-id="cb3f1-114"><strong>Canceled</strong></span></span></p></td>
<td><p><span data-ttu-id="cb3f1-115"><strong>สร้างแล้ว</strong></span><span class="sxs-lookup"><span data-stu-id="cb3f1-115"><strong>Created</strong></span></span></p></td>
<td><p><span data-ttu-id="cb3f1-116"><strong>สร้างแล้ว</strong></span><span class="sxs-lookup"><span data-stu-id="cb3f1-116"><strong>Created</strong></span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cb3f1-117"><strong>อยู่ระหว่างดำเนินการ</strong></span><span class="sxs-lookup"><span data-stu-id="cb3f1-117"><strong>In process</strong></span></span></p></td>
<td><p><span data-ttu-id="cb3f1-118"><strong>สร้างแล้ว</strong></span><span class="sxs-lookup"><span data-stu-id="cb3f1-118"><strong>Created</strong></span></span></p></td>
<td><p><span data-ttu-id="cb3f1-119"><strong>ยกเลิก</strong></span><span class="sxs-lookup"><span data-stu-id="cb3f1-119"><strong>Canceled</strong></span></span></p></td>
<td><p><span data-ttu-id="cb3f1-120"><strong>ประกาศแล้ว</strong></span><span class="sxs-lookup"><span data-stu-id="cb3f1-120"><strong>Posted</strong></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cb3f1-121"><strong>ยกเลิก</strong></span><span class="sxs-lookup"><span data-stu-id="cb3f1-121"><strong>Canceled</strong></span></span></p></td>
<td><p><span data-ttu-id="cb3f1-122"><strong>ยกเลิก</strong></span><span class="sxs-lookup"><span data-stu-id="cb3f1-122"><strong>Canceled</strong></span></span></p></td>
<td><p><span data-ttu-id="cb3f1-123"><strong>ยกเลิก</strong></span><span class="sxs-lookup"><span data-stu-id="cb3f1-123"><strong>Canceled</strong></span></span></p></td>
<td><p><span data-ttu-id="cb3f1-124"><strong>ยกเลิก</strong></span><span class="sxs-lookup"><span data-stu-id="cb3f1-124"><strong>Canceled</strong></span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cb3f1-125"><strong>ประกาศแล้ว</strong></span><span class="sxs-lookup"><span data-stu-id="cb3f1-125"><strong>Posted</strong></span></span></p></td>
<td><p><span data-ttu-id="cb3f1-126"><strong>ประกาศแล้ว</strong></span><span class="sxs-lookup"><span data-stu-id="cb3f1-126"><strong>Posted</strong></span></span></p></td>
<td><p><span data-ttu-id="cb3f1-127"><strong>ประกาศแล้ว</strong></span><span class="sxs-lookup"><span data-stu-id="cb3f1-127"><strong>Posted</strong></span></span></p></td>
<td><p><span data-ttu-id="cb3f1-128"><strong>ประกาศแล้ว</strong></span><span class="sxs-lookup"><span data-stu-id="cb3f1-128"><strong>Posted</strong></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cb3f1-129"><strong>ประกาศแล้ว</strong></span><span class="sxs-lookup"><span data-stu-id="cb3f1-129"><strong>Posted</strong></span></span></p></td>
<td><p><span data-ttu-id="cb3f1-130"><strong>ประกาศแล้ว</strong></span><span class="sxs-lookup"><span data-stu-id="cb3f1-130"><strong>Posted</strong></span></span></p></td>
<td><p><span data-ttu-id="cb3f1-131"><strong>ยกเลิก</strong></span><span class="sxs-lookup"><span data-stu-id="cb3f1-131"><strong>Canceled</strong></span></span></p></td>
<td><p><span data-ttu-id="cb3f1-132"><strong>ยกเลิก</strong></span><span class="sxs-lookup"><span data-stu-id="cb3f1-132"><strong>Canceled</strong></span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="cb3f1-133">ความก้าวหน้าของใบสั่งบริการอยู่ระหว่างดำเนินการ หากทุกรายการมีสถานะ **สร้างแล้ว**; ใบสั่งนั้นยังอยู่ระหว่างดำเนินการ หากบางรายการมีสถานะเป็น **ยกเลิกแล้ว** หรือ **ลงรายการบัญชีแล้ว**</span><span class="sxs-lookup"><span data-stu-id="cb3f1-133">The progress of a service order is in process if all lines have the status **Created**; it is still in process if some of the lines have a status of **Canceled** or **Posted**.</span></span>

<span data-ttu-id="cb3f1-134">ถ้าทุกรายการใบสั่งบริการถูกทำเครื่องหมายเป็น **ลงรายการบัญชีแล้ว** ความก้าวหน้าของใบสั่งสถานะจะเป็น **ลงรายการบัญชีแล้ว**</span><span class="sxs-lookup"><span data-stu-id="cb3f1-134">If all lines in a service order are marked as **Posted**, the progress of the status order is **Posted**.</span></span> <span data-ttu-id="cb3f1-135">ถ้าบางรายการเป็น **ลงรายการบัญชีแล้ว** และบางรายการเป็น **ยกเลิกแล้ว** ความก้าวหน้าจะยังคงเป็น **ลงรายการบัญชีแล้ว**</span><span class="sxs-lookup"><span data-stu-id="cb3f1-135">If some lines are **Posted** and some are **Canceled**, the progress is still **Posted**.</span></span>

  


