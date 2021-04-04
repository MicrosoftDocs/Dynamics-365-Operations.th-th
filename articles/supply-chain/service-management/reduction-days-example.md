---
title: ตัวอย่างวันในการลด
description: ตัวอย่างวันในการลด
author: ShylaThompson
manager: tfehr
ms.date: 05/01/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SMASubscriptionTable
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: df528bf7e95ee7ea74a792894b5e1c2f50c57730
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 02/15/2021
ms.locfileid: "5234764"
---
# <a name="reduction-days-example"></a><span data-ttu-id="536dd-103">ตัวอย่างวันในการลด</span><span class="sxs-lookup"><span data-stu-id="536dd-103">Reduction days example</span></span> 

[!include [banner](../includes/banner.md)]


<span data-ttu-id="536dd-104">คุณได้สร้างธุรกรรมการบอกรับสมัครสมาชิกสำหรับการบอกรับสมัครสมาชิกการบำรุงรักษาของลูกค้า ตามที่อธิบายในตารางดังต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="536dd-104">You have created a subscription transaction for a customer's maintenance subscription, as described in the following table.</span></span>

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
<th><p><span data-ttu-id="536dd-105">วันที่เริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="536dd-105">From date</span></span></p></th>
<th><p><span data-ttu-id="536dd-106">วันที่สิ้นสุด</span><span class="sxs-lookup"><span data-stu-id="536dd-106">To date</span></span></p></th>
<th><p><span data-ttu-id="536dd-107">การบอกรับเป็นสมาชิก</span><span class="sxs-lookup"><span data-stu-id="536dd-107">Subscription</span></span></p></th>
<th><p><span data-ttu-id="536dd-108">ชนิดของการบอกรับเป็นสมาชิก</span><span class="sxs-lookup"><span data-stu-id="536dd-108">Subscription type</span></span></p></th>
<th><p><span data-ttu-id="536dd-109">Project</span><span class="sxs-lookup"><span data-stu-id="536dd-109">Project</span></span></p></th>
<th><p><span data-ttu-id="536dd-110">ประเภท</span><span class="sxs-lookup"><span data-stu-id="536dd-110">Category</span></span></p></th>
<th><p><span data-ttu-id="536dd-111">สกุลเงินที่ใช้ในการขาย</span><span class="sxs-lookup"><span data-stu-id="536dd-111">Sales currency</span></span></p></th>
<th><p><span data-ttu-id="536dd-112">ราคาขาย</span><span class="sxs-lookup"><span data-stu-id="536dd-112">Sales price</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="536dd-113">01 มีนาคม 2011</span><span class="sxs-lookup"><span data-stu-id="536dd-113">March 01, 2011</span></span></p></td>
<td><p><span data-ttu-id="536dd-114">31 มีนาคม 2011</span><span class="sxs-lookup"><span data-stu-id="536dd-114">March 31, 2011</span></span></p></td>
<td><p><span data-ttu-id="536dd-115">NR-2</span><span class="sxs-lookup"><span data-stu-id="536dd-115">NR-2</span></span></p></td>
<td><p><span data-ttu-id="536dd-116"><strong>เป็นประจำ</strong></span><span class="sxs-lookup"><span data-stu-id="536dd-116"><strong>Regular</strong></span></span></p></td>
<td><p><span data-ttu-id="536dd-117">9013</span><span class="sxs-lookup"><span data-stu-id="536dd-117">9013</span></span></p></td>
<td><p><span data-ttu-id="536dd-118">SubCat2</span><span class="sxs-lookup"><span data-stu-id="536dd-118">SubCat2</span></span></p></td>
<td><p><span data-ttu-id="536dd-119">EUR</span><span class="sxs-lookup"><span data-stu-id="536dd-119">EUR</span></span></p></td>
<td><p><span data-ttu-id="536dd-120">200.00</span><span class="sxs-lookup"><span data-stu-id="536dd-120">200.00</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="536dd-121">ลูกค้ารายงานว่าไม่จำเป็นต้องใช้การครอบคลุมบริการเป็นเวลาสองวัน (10 มีนาคม</span><span class="sxs-lookup"><span data-stu-id="536dd-121">The customer reports that it does not need service coverage for two days (March 10 and March 11).</span></span> <span data-ttu-id="536dd-122">และ 11 มีนาคม) คุณตกลงลดการสมัครสมาชิกในเวลาสองวันนี้</span><span class="sxs-lookup"><span data-stu-id="536dd-122">You agree to reduce the subscription by these two days.</span></span>

<span data-ttu-id="536dd-123">คุณสร้างธุรกรรมใหม่ของชนิด **จำนวนวันที่ลด** ดังที่อธิบายในตารางดังต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="536dd-123">You create a new transaction of the **Reduction days** type, as described in the following table.</span></span>

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
<th><p><span data-ttu-id="536dd-124">วันที่เริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="536dd-124">From date</span></span></p></th>
<th><p><span data-ttu-id="536dd-125">วันที่สิ้นสุด</span><span class="sxs-lookup"><span data-stu-id="536dd-125">To date</span></span></p></th>
<th><p><span data-ttu-id="536dd-126">การบอกรับเป็นสมาชิก</span><span class="sxs-lookup"><span data-stu-id="536dd-126">Subscription</span></span></p></th>
<th><p><span data-ttu-id="536dd-127">ชนิดของการบอกรับเป็นสมาชิก</span><span class="sxs-lookup"><span data-stu-id="536dd-127">Subscription type</span></span></p></th>
<th><p><span data-ttu-id="536dd-128">Project</span><span class="sxs-lookup"><span data-stu-id="536dd-128">Project</span></span></p></th>
<th><p><span data-ttu-id="536dd-129">ประเภท</span><span class="sxs-lookup"><span data-stu-id="536dd-129">Category</span></span></p></th>
<th><p><span data-ttu-id="536dd-130">สกุลเงินที่ใช้ในการขาย</span><span class="sxs-lookup"><span data-stu-id="536dd-130">Sales currency</span></span></p></th>
<th><p><span data-ttu-id="536dd-131">ราคาขาย</span><span class="sxs-lookup"><span data-stu-id="536dd-131">Sales price</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="536dd-132">10 มีนาคม 2011</span><span class="sxs-lookup"><span data-stu-id="536dd-132">March 10, 2011</span></span></p></td>
<td><p><span data-ttu-id="536dd-133">11 มีนาคม 2011</span><span class="sxs-lookup"><span data-stu-id="536dd-133">March 11, 2011</span></span></p></td>
<td><p><span data-ttu-id="536dd-134">NR-2</span><span class="sxs-lookup"><span data-stu-id="536dd-134">NR-2</span></span></p></td>
<td><p><span data-ttu-id="536dd-135"><strong>จำนวนวันที่ลด</strong></span><span class="sxs-lookup"><span data-stu-id="536dd-135"><strong>Reduction days</strong></span></span></p></td>
<td><p><span data-ttu-id="536dd-136">9013</span><span class="sxs-lookup"><span data-stu-id="536dd-136">9013</span></span></p></td>
<td><p><span data-ttu-id="536dd-137">SubCat2</span><span class="sxs-lookup"><span data-stu-id="536dd-137">SubCat2</span></span></p></td>
<td><p><span data-ttu-id="536dd-138">EUR</span><span class="sxs-lookup"><span data-stu-id="536dd-138">EUR</span></span></p></td>
<td><p><span data-ttu-id="536dd-139">-12.90</span><span class="sxs-lookup"><span data-stu-id="536dd-139">-12.90</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="536dd-140">เมื่อธุรกรรมสำหรับเดือนมีนาคม 2011 มีการออกใบแจ้งหนี้แล้ว ราคาขาย EUR 200 จะถูกลดลง EUR 12.90</span><span class="sxs-lookup"><span data-stu-id="536dd-140">When the transactions for March 2011 are invoiced, the sales price of EUR 200 is reduced by EUR 12.90.</span></span> <span data-ttu-id="536dd-141">ราคาขาย EUR 200 จะลดลงจำนวน EUR 12.90 จำนวนที่คิดค่าธรรมเนียมได้ของธุรกรรมการบอกรับการสมัครสมาชิกดังนั้นก็จะเป็น EUR 187.10 และสองธุรกรรมจะออกใบแจ้งหนี้ที่ยอด EUR 187.10</span><span class="sxs-lookup"><span data-stu-id="536dd-141">The chargeable amount for the subscription transaction is therefore EUR 187.10, and two transactions are invoiced at a total of EUR 187.10.</span></span>

## <a name="see-also"></a><span data-ttu-id="536dd-142">ดูเพิ่มเติมที่</span><span class="sxs-lookup"><span data-stu-id="536dd-142">See also</span></span>

[<span data-ttu-id="536dd-143">การลดจำนวนวันของค่าธรรมเนียมการสั่งซื้อโดยบอกรับเป็นสมาชิก</span><span class="sxs-lookup"><span data-stu-id="536dd-143">Reduce the days on subscription fees</span></span>](reduce-the-days-on-subscription-fees.md)

  




[!INCLUDE[footer-include](../../includes/footer-banner.md)]