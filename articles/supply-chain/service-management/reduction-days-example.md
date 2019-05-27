---
title: ตัวอย่างวันในการลด
description: ตัวอย่างวันในการลด
author: ShylaThompson
manager: AnnBe
ms.date: 05/01/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SMASubscriptionTable
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: ShylaThompson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 46b38579e8a6246476d0893e1a047ad434f6d399
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 05/15/2019
ms.locfileid: "1564519"
---
# <a name="reduction-days-example"></a><span data-ttu-id="526ea-103">ตัวอย่างวันในการลด</span><span class="sxs-lookup"><span data-stu-id="526ea-103">Reduction days example</span></span> 

[!include [banner](../includes/banner.md)]


<span data-ttu-id="526ea-104">คุณได้สร้างธุรกรรมการบอกรับสมัครสมาชิกสำหรับการบอกรับสมัครสมาชิกการบำรุงรักษาของลูกค้า ตามที่อธิบายในตารางดังต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="526ea-104">You have created a subscription transaction for a customer's maintenance subscription, as described in the following table.</span></span>

<table>
<colgroup>
<col style="width: 12%" />
<col style="width: 12%" />
<col style="width: 12%" />
<col style="width: 12%" />
<col style="width: 12%" />
<col style="width: 12%" />
<col style="width: 12%" />
<col style="width: 12%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="526ea-105">วันที่เริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="526ea-105">From date</span></span></p></th>
<th><p><span data-ttu-id="526ea-106">วันที่สิ้นสุด</span><span class="sxs-lookup"><span data-stu-id="526ea-106">To date</span></span></p></th>
<th><p><span data-ttu-id="526ea-107">การบอกรับเป็นสมาชิก</span><span class="sxs-lookup"><span data-stu-id="526ea-107">Subscription</span></span></p></th>
<th><p><span data-ttu-id="526ea-108">ชนิดของการบอกรับเป็นสมาชิก</span><span class="sxs-lookup"><span data-stu-id="526ea-108">Subscription type</span></span></p></th>
<th><p><span data-ttu-id="526ea-109">Project</span><span class="sxs-lookup"><span data-stu-id="526ea-109">Project</span></span></p></th>
<th><p><span data-ttu-id="526ea-110">ประเภท</span><span class="sxs-lookup"><span data-stu-id="526ea-110">Category</span></span></p></th>
<th><p><span data-ttu-id="526ea-111">สกุลเงินที่ใช้ในการขาย</span><span class="sxs-lookup"><span data-stu-id="526ea-111">Sales currency</span></span></p></th>
<th><p><span data-ttu-id="526ea-112">ราคาขาย</span><span class="sxs-lookup"><span data-stu-id="526ea-112">Sales price</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="526ea-113">01 มีนาคม 2011</span><span class="sxs-lookup"><span data-stu-id="526ea-113">March 01, 2011</span></span></p></td>
<td><p><span data-ttu-id="526ea-114">31 มีนาคม 2011</span><span class="sxs-lookup"><span data-stu-id="526ea-114">March 31, 2011</span></span></p></td>
<td><p><span data-ttu-id="526ea-115">NR-2</span><span class="sxs-lookup"><span data-stu-id="526ea-115">NR-2</span></span></p></td>
<td><p><span data-ttu-id="526ea-116"><strong>เป็นประจำ</strong></span><span class="sxs-lookup"><span data-stu-id="526ea-116"><strong>Regular</strong></span></span></p></td>
<td><p><span data-ttu-id="526ea-117">9013</span><span class="sxs-lookup"><span data-stu-id="526ea-117">9013</span></span></p></td>
<td><p><span data-ttu-id="526ea-118">SubCat2</span><span class="sxs-lookup"><span data-stu-id="526ea-118">SubCat2</span></span></p></td>
<td><p><span data-ttu-id="526ea-119">EUR</span><span class="sxs-lookup"><span data-stu-id="526ea-119">EUR</span></span></p></td>
<td><p><span data-ttu-id="526ea-120">200.00</span><span class="sxs-lookup"><span data-stu-id="526ea-120">200.00</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="526ea-121">ลูกค้ารายงานว่าไม่จำเป็นต้องใช้การครอบคลุมบริการเป็นเวลาสองวัน (10 มีนาคม</span><span class="sxs-lookup"><span data-stu-id="526ea-121">The customer reports that it does not need service coverage for two days (March 10 and March 11).</span></span> <span data-ttu-id="526ea-122">และ 11 มีนาคม) คุณตกลงลดการสมัครสมาชิกในเวลาสองวันนี้</span><span class="sxs-lookup"><span data-stu-id="526ea-122">You agree to reduce the subscription by these two days.</span></span>

<span data-ttu-id="526ea-123">คุณสร้างธุรกรรมใหม่ของชนิด **จำนวนวันที่ลด** ดังที่อธิบายในตารางดังต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="526ea-123">You create a new transaction of the **Reduction days** type, as described in the following table.</span></span>

<table>
<colgroup>
<col style="width: 12%" />
<col style="width: 12%" />
<col style="width: 12%" />
<col style="width: 12%" />
<col style="width: 12%" />
<col style="width: 12%" />
<col style="width: 12%" />
<col style="width: 12%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="526ea-124">วันที่เริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="526ea-124">From date</span></span></p></th>
<th><p><span data-ttu-id="526ea-125">วันที่สิ้นสุด</span><span class="sxs-lookup"><span data-stu-id="526ea-125">To date</span></span></p></th>
<th><p><span data-ttu-id="526ea-126">การบอกรับเป็นสมาชิก</span><span class="sxs-lookup"><span data-stu-id="526ea-126">Subscription</span></span></p></th>
<th><p><span data-ttu-id="526ea-127">ชนิดของการบอกรับเป็นสมาชิก</span><span class="sxs-lookup"><span data-stu-id="526ea-127">Subscription type</span></span></p></th>
<th><p><span data-ttu-id="526ea-128">Project</span><span class="sxs-lookup"><span data-stu-id="526ea-128">Project</span></span></p></th>
<th><p><span data-ttu-id="526ea-129">ประเภท</span><span class="sxs-lookup"><span data-stu-id="526ea-129">Category</span></span></p></th>
<th><p><span data-ttu-id="526ea-130">สกุลเงินที่ใช้ในการขาย</span><span class="sxs-lookup"><span data-stu-id="526ea-130">Sales currency</span></span></p></th>
<th><p><span data-ttu-id="526ea-131">ราคาขาย</span><span class="sxs-lookup"><span data-stu-id="526ea-131">Sales price</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="526ea-132">10 มีนาคม 2011</span><span class="sxs-lookup"><span data-stu-id="526ea-132">March 10, 2011</span></span></p></td>
<td><p><span data-ttu-id="526ea-133">11 มีนาคม 2011</span><span class="sxs-lookup"><span data-stu-id="526ea-133">March 11, 2011</span></span></p></td>
<td><p><span data-ttu-id="526ea-134">NR-2</span><span class="sxs-lookup"><span data-stu-id="526ea-134">NR-2</span></span></p></td>
<td><p><span data-ttu-id="526ea-135"><strong>จำนวนวันที่ลด</strong></span><span class="sxs-lookup"><span data-stu-id="526ea-135"><strong>Reduction days</strong></span></span></p></td>
<td><p><span data-ttu-id="526ea-136">9013</span><span class="sxs-lookup"><span data-stu-id="526ea-136">9013</span></span></p></td>
<td><p><span data-ttu-id="526ea-137">SubCat2</span><span class="sxs-lookup"><span data-stu-id="526ea-137">SubCat2</span></span></p></td>
<td><p><span data-ttu-id="526ea-138">EUR</span><span class="sxs-lookup"><span data-stu-id="526ea-138">EUR</span></span></p></td>
<td><p><span data-ttu-id="526ea-139">-12.90</span><span class="sxs-lookup"><span data-stu-id="526ea-139">-12.90</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="526ea-140">เมื่อธุรกรรมสำหรับเดือนมีนาคม 2011 มีการออกใบแจ้งหนี้แล้ว ราคาขาย EUR 200 จะถูกลดลง EUR 12.90</span><span class="sxs-lookup"><span data-stu-id="526ea-140">When the transactions for March 2011 are invoiced, the sales price of EUR 200 is reduced by EUR 12.90.</span></span> <span data-ttu-id="526ea-141">ราคาขาย EUR 200 จะลดลงจำนวน EUR 12.90 จำนวนที่คิดค่าธรรมเนียมได้ของธุรกรรมการบอกรับการสมัครสมาชิกดังนั้นก็จะเป็น EUR 187.10 และสองธุรกรรมจะออกใบแจ้งหนี้ที่ยอด EUR 187.10</span><span class="sxs-lookup"><span data-stu-id="526ea-141">The chargeable amount for the subscription transaction is therefore EUR 187.10, and two transactions are invoiced at a total of EUR 187.10.</span></span>

## <a name="see-also"></a><span data-ttu-id="526ea-142">ดูเพิ่มเติมที่</span><span class="sxs-lookup"><span data-stu-id="526ea-142">See also</span></span>

[<span data-ttu-id="526ea-143">การลดจำนวนวันของค่าธรรมเนียมการสั่งซื้อโดยบอกรับเป็นสมาชิก</span><span class="sxs-lookup"><span data-stu-id="526ea-143">Reduce the days on subscription fees</span></span>](reduce-the-days-on-subscription-fees.md)

  


