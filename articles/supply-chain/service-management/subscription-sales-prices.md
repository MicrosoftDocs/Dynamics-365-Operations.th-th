---
title: ราคาขายสำหรับการบอกรับเป็นสมาชิก
description: เมื่อคุณสร้างการบอกรับเป็นสมาชิก คุณจะได้รับราคาขายจากการตั้งค่าราคาขายซึ่งถูกสร้างในแบบฟอร์มราคาขาย (การบอกรับเป็นสมาชิก)
author: ShylaThompson
manager: tfehr
ms.date: 05/01/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SMASalespriceSubscription
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 2ed8329e9da08fbe24d9b3982eee562974f0fb3b
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 02/15/2021
ms.locfileid: "5242312"
---
# <a name="subscription-sales-prices"></a><span data-ttu-id="49120-103">ราคาขายสำหรับการบอกรับเป็นสมาชิก</span><span class="sxs-lookup"><span data-stu-id="49120-103">Subscription sales prices</span></span>   

[!include [banner](../includes/banner.md)]


<span data-ttu-id="49120-104">เมื่อคุณสร้างการบอกรับเป็นสมาชิก คุณจะได้รับราคาขายจากการตั้งค่าราคาขายซึ่งถูกสร้างในแบบฟอร์ม **ราคาขาย (การบอกรับเป็นสมาชิก)**</span><span class="sxs-lookup"><span data-stu-id="49120-104">When you create a subscription, the sales price is derived from the sales price setup that was created in the **Sales price (subscription)** form.</span></span>

<span data-ttu-id="49120-105">ในแบบฟอร์ม **ราคาขาย (การบอกรับเป็นสมาชิก)** คุณสามารถสร้างราคาขายสำหรับการบอกรับสมาชิกที่กำหนดไว้ได้ หรือคุณอาจสร้างราคาขายที่นำไปใช้ได้อย่างกว้างขวางขึ้นได้</span><span class="sxs-lookup"><span data-stu-id="49120-105">In the **Sales price (subscription)** form, you can create sales prices for a specific subscription or you can create sales prices that apply more broadly.</span></span> <span data-ttu-id="49120-106">สำหรับราคาขายที่จะนำไปใช้ในการบอกรับเป็นสมาชิก รหัสรอบระยะเวลาและสกุลเงินของการบอกรับเป็นสมาชิก ต้องเหมือนกับรหัสรอบระยะเวลาและสกุลเงินของราคาขาย</span><span class="sxs-lookup"><span data-stu-id="49120-106">For a sales price to be applied to a subscription, the period code and the currency of the subscription must be identical to the period code and the currency of the sales price.</span></span>

<span data-ttu-id="49120-107">หากรหัสรอบระยะเวลาและสกุลเงินของทั้งการบอกรับเป็นสมาชิกและราคาขายเหมือนกัน จะมีการเลือกราคาขายสำหรับการบอกรับเป็นสมาชิกตามระดับความสำคัญที่แสดงรายการในตารางต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="49120-107">If the period code and currency are identical for the subscription and the sales price, subscription sales prices are selected on the basis of the priorities listed in the following table.</span></span> <span data-ttu-id="49120-108">เซลล์ว่างในตารางจะหมายถึงฟิลด์ว่าง และ X หมายถึงค่าที่เท่ากับค่าในการบอกรับเป็นสมาชิกจากธุรกรรมที่สร้างขึ้น</span><span class="sxs-lookup"><span data-stu-id="49120-108">A blank cell in the table indicates an empty field and an X indicates a value that is equal to the value in the subscription from which the transaction is generated.</span></span>

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
<th><p><span data-ttu-id="49120-109">ระดับความสำคัญ </span><span class="sxs-lookup"><span data-stu-id="49120-109">Priority</span></span></p></th>
<th><p><span data-ttu-id="49120-110"><strong>ประเภท</strong></span><span class="sxs-lookup"><span data-stu-id="49120-110"><strong>Category</strong></span></span></p></th>
<th><p><span data-ttu-id="49120-111"><strong>รหัสโครงการ</strong></span><span class="sxs-lookup"><span data-stu-id="49120-111"><strong>Project ID</strong></span></span></p></th>
<th><p><span data-ttu-id="49120-112"><strong>การสั่งซื้อโดยบอกรับเป็นสมาชิก</strong></span><span class="sxs-lookup"><span data-stu-id="49120-112"><strong>Subscription</strong></span></span></p></th>
<th><p><span data-ttu-id="49120-113"><strong>สกุลเงินที่ใช้ในการขาย</strong></span><span class="sxs-lookup"><span data-stu-id="49120-113"><strong>Sales currency</strong></span></span></p></th>
<th><p><span data-ttu-id="49120-114"><strong>ชนิดรอบระยะเวลาบัญชี</strong></span><span class="sxs-lookup"><span data-stu-id="49120-114"><strong>Period code</strong></span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="49120-115">1</span><span class="sxs-lookup"><span data-stu-id="49120-115">1</span></span></p></td>
<td><p><span data-ttu-id="49120-116">X</span><span class="sxs-lookup"><span data-stu-id="49120-116">X</span></span></p></td>
<td><p><span data-ttu-id="49120-117">X</span><span class="sxs-lookup"><span data-stu-id="49120-117">X</span></span></p></td>
<td><p><span data-ttu-id="49120-118">X</span><span class="sxs-lookup"><span data-stu-id="49120-118">X</span></span></p></td>
<td><p><span data-ttu-id="49120-119">X</span><span class="sxs-lookup"><span data-stu-id="49120-119">X</span></span></p></td>
<td><p><span data-ttu-id="49120-120">X</span><span class="sxs-lookup"><span data-stu-id="49120-120">X</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="49120-121">2</span><span class="sxs-lookup"><span data-stu-id="49120-121">2</span></span></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="49120-122">X</span><span class="sxs-lookup"><span data-stu-id="49120-122">X</span></span></p></td>
<td><p><span data-ttu-id="49120-123">X</span><span class="sxs-lookup"><span data-stu-id="49120-123">X</span></span></p></td>
<td><p><span data-ttu-id="49120-124">X</span><span class="sxs-lookup"><span data-stu-id="49120-124">X</span></span></p></td>
<td><p><span data-ttu-id="49120-125">X</span><span class="sxs-lookup"><span data-stu-id="49120-125">X</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="49120-126">3</span><span class="sxs-lookup"><span data-stu-id="49120-126">3</span></span></p></td>
<td><p><span data-ttu-id="49120-127">X</span><span class="sxs-lookup"><span data-stu-id="49120-127">X</span></span></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="49120-128">X</span><span class="sxs-lookup"><span data-stu-id="49120-128">X</span></span></p></td>
<td><p><span data-ttu-id="49120-129">X</span><span class="sxs-lookup"><span data-stu-id="49120-129">X</span></span></p></td>
<td><p><span data-ttu-id="49120-130">X</span><span class="sxs-lookup"><span data-stu-id="49120-130">X</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="49120-131">4 ชั่วโมง</span><span class="sxs-lookup"><span data-stu-id="49120-131">4</span></span></p></td>
<td><p></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="49120-132">X</span><span class="sxs-lookup"><span data-stu-id="49120-132">X</span></span></p></td>
<td><p><span data-ttu-id="49120-133">X</span><span class="sxs-lookup"><span data-stu-id="49120-133">X</span></span></p></td>
<td><p><span data-ttu-id="49120-134">X</span><span class="sxs-lookup"><span data-stu-id="49120-134">X</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="49120-135">5</span><span class="sxs-lookup"><span data-stu-id="49120-135">5</span></span></p></td>
<td><p><span data-ttu-id="49120-136">X</span><span class="sxs-lookup"><span data-stu-id="49120-136">X</span></span></p></td>
<td><p><span data-ttu-id="49120-137">X</span><span class="sxs-lookup"><span data-stu-id="49120-137">X</span></span></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="49120-138">X</span><span class="sxs-lookup"><span data-stu-id="49120-138">X</span></span></p></td>
<td><p><span data-ttu-id="49120-139">X</span><span class="sxs-lookup"><span data-stu-id="49120-139">X</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="49120-140">6 ชั่วโมง</span><span class="sxs-lookup"><span data-stu-id="49120-140">6</span></span></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="49120-141">X</span><span class="sxs-lookup"><span data-stu-id="49120-141">X</span></span></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="49120-142">X</span><span class="sxs-lookup"><span data-stu-id="49120-142">X</span></span></p></td>
<td><p><span data-ttu-id="49120-143">X</span><span class="sxs-lookup"><span data-stu-id="49120-143">X</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="49120-144">7</span><span class="sxs-lookup"><span data-stu-id="49120-144">7</span></span></p></td>
<td><p><span data-ttu-id="49120-145">X</span><span class="sxs-lookup"><span data-stu-id="49120-145">X</span></span></p></td>
<td><p></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="49120-146">X</span><span class="sxs-lookup"><span data-stu-id="49120-146">X</span></span></p></td>
<td><p><span data-ttu-id="49120-147">X</span><span class="sxs-lookup"><span data-stu-id="49120-147">X</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="49120-148">8</span><span class="sxs-lookup"><span data-stu-id="49120-148">8</span></span></p></td>
<td><p></p></td>
<td><p></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="49120-149">X</span><span class="sxs-lookup"><span data-stu-id="49120-149">X</span></span></p></td>
<td><p><span data-ttu-id="49120-150">X</span><span class="sxs-lookup"><span data-stu-id="49120-150">X</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="49120-151">เมื่อมีการสร้างค่าธรรมเนียมการบอกรับเป็นสมาชิก ราคาขายที่มีระดับรายละเอียดมากที่สุด (ตามที่ระบุไว้ในตารางข้างต้น) จะถูกเลือกเป็นราคาขายสำหรับการบอกรับเป็นสมาชิก</span><span class="sxs-lookup"><span data-stu-id="49120-151">When a subscription fee is created, the sales price with the greatest level of detail, as noted in the table above, is selected as the subscription sales price.</span></span>

## <a name="update-and-index-subscription-sales-prices"></a><span data-ttu-id="49120-152">การอัพเดตและการจัดดัชนีราคาขายของการสั่งซื้อโดยบอกรับเป็นสมาชิก</span><span class="sxs-lookup"><span data-stu-id="49120-152">Update and index subscription sales prices</span></span>

<span data-ttu-id="49120-153">คุณสามารถอัพเดตราคาขายสำหรับการสั่งซื้อโดยบอกรับเป็นสมาชิกโดยการอัพเดตราคาหรือดัชนีพื้นฐาน</span><span class="sxs-lookup"><span data-stu-id="49120-153">You can update the subscription sales price by updating the base price or the index.</span></span> <span data-ttu-id="49120-154">คุณสามารถอัพเดตตามเปอร์เซ็นต์หรือค่าใหม่ได้</span><span class="sxs-lookup"><span data-stu-id="49120-154">You can update by a percentage or to a new value.</span></span>

## <a name="subscription-fee-sales-prices"></a><span data-ttu-id="49120-155">ราคาขายสำหรับค่าธรรมเนียมการสั่งซื้อโดยบอกรับเป็นสมาชิก</span><span class="sxs-lookup"><span data-stu-id="49120-155">Subscription fee sales prices</span></span>

<span data-ttu-id="49120-156">เมื่อคุณสร้างค่าธรรมเนียมการสั่งซื้อโดยบอกรับเป็นสมาชิก ราคาขายจะขึ้นอยู่กับการตั้งค่าราคาขายของการบอกรับเป็นสมาชิก </span><span class="sxs-lookup"><span data-stu-id="49120-156">When you create a subscription fee, the sales price is based on the sales price setup of the subscription.</span></span> <span data-ttu-id="49120-157">คุณสามารถใช้ราคาพื้นฐานจากการตั้งค่าราคาการบอกรับเป็นสมาชิก หรือคุณอาจสร้างราคาขายที่มีการจัดทำดัชนีขึ้นก็ได้ อย่างใดอย่างหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="49120-157">You can either use the base price from the subscription price setup or create indexed sales prices.</span></span>

## <a name="example"></a><span data-ttu-id="49120-158">ตัวอย่าง</span><span class="sxs-lookup"><span data-stu-id="49120-158">Example</span></span>

<span data-ttu-id="49120-159">คุณต้องการตั้งค่าราคาขายของการสั่งซื้อโดยบอกรับเป็นสมาชิกเป็นจำนวนเงิน  EUR 500 สำหรับโครงการใหม่</span><span class="sxs-lookup"><span data-stu-id="49120-159">You want to set up subscription sales prices of EUR 500 for a new project 9030.</span></span> <span data-ttu-id="49120-160">ในแบบฟอร์ม **ราคาขาย (การบอกรับเป็นสมาชิก)** คุณสร้างรายการราคาขายการบอกรับเป็นสมาชิกตามที่ระบุไว้ในตารางต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="49120-160">In the **Sales price (subscription)** form, you create a subscription sales price line as indicated in the following table.</span></span>

<table style="width:100%;">
<colgroup>
<col style="width: 14%" />
<col style="width: 14%" />
<col style="width: 14%" />
<col style="width: 14%" />
<col style="width: 14%" />
<col style="width: 14%" />
<col style="width: 14%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="49120-161">ใช้ได้ตั้งแต่</span><span class="sxs-lookup"><span data-stu-id="49120-161">Valid from</span></span></p></th>
<th><p><span data-ttu-id="49120-162">ประเภท</span><span class="sxs-lookup"><span data-stu-id="49120-162">Category</span></span></p></th>
<th><p><span data-ttu-id="49120-163">Project</span><span class="sxs-lookup"><span data-stu-id="49120-163">Project</span></span></p></th>
<th><p><span data-ttu-id="49120-164">การบอกรับเป็นสมาชิก</span><span class="sxs-lookup"><span data-stu-id="49120-164">Subscription</span></span></p></th>
<th><p><span data-ttu-id="49120-165">ชนิดรอบระยะเวลาบัญชี</span><span class="sxs-lookup"><span data-stu-id="49120-165">Period code</span></span></p></th>
<th><p><span data-ttu-id="49120-166">สกุลเงินที่ใช้ในการขาย</span><span class="sxs-lookup"><span data-stu-id="49120-166">Sales currency</span></span></p></th>
<th><p><span data-ttu-id="49120-167">ราคาขาย</span><span class="sxs-lookup"><span data-stu-id="49120-167">Sales price</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="49120-168">วันที่ 28-08-2006</span><span class="sxs-lookup"><span data-stu-id="49120-168">28-08-2006</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="49120-169">9030</span><span class="sxs-lookup"><span data-stu-id="49120-169">9030</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="49120-170">เดือน</span><span class="sxs-lookup"><span data-stu-id="49120-170">Month</span></span></p></td>
<td><p><span data-ttu-id="49120-171">EUR</span><span class="sxs-lookup"><span data-stu-id="49120-171">EUR</span></span></p></td>
<td><p><span data-ttu-id="49120-172">500</span><span class="sxs-lookup"><span data-stu-id="49120-172">500</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="49120-173">โปรดจำไว้ว่าฟิลด์ **ประเภท** และ **การบอกรับเป็นสมาชิก** ว่าง</span><span class="sxs-lookup"><span data-stu-id="49120-173">Note that the **Category** and **Subscription** fields are empty.</span></span>

<span data-ttu-id="49120-174">จากนั้น คุณสร้างการบอกรับเป็นสมาชิกดังนี้</span><span class="sxs-lookup"><span data-stu-id="49120-174">You then create the following subscriptions.</span></span>

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
<th><p><span data-ttu-id="49120-175">การบอกรับเป็นสมาชิกการบริการ</span><span class="sxs-lookup"><span data-stu-id="49120-175">Service subscription</span></span></p></th>
<th><p><span data-ttu-id="49120-176">Project</span><span class="sxs-lookup"><span data-stu-id="49120-176">Project</span></span></p></th>
<th><p><span data-ttu-id="49120-177">ประเภทของการบอกรับเป็นสมาชิก</span><span class="sxs-lookup"><span data-stu-id="49120-177">Subscription group</span></span></p></th>
<th><p><span data-ttu-id="49120-178">ประเภท</span><span class="sxs-lookup"><span data-stu-id="49120-178">Category</span></span></p></th>
<th><p><span data-ttu-id="49120-179">สกุลเงิน</span><span class="sxs-lookup"><span data-stu-id="49120-179">Currency</span></span></p></th>
<th><p><span data-ttu-id="49120-180">รหัสรอบระยะเวลา</span><span class="sxs-lookup"><span data-stu-id="49120-180">Period code</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="49120-181">00020_135</span><span class="sxs-lookup"><span data-stu-id="49120-181">00020_135</span></span></p></td>
<td><p><span data-ttu-id="49120-182">9030</span><span class="sxs-lookup"><span data-stu-id="49120-182">9030</span></span></p></td>
<td><p><span data-ttu-id="49120-183">Sub1</span><span class="sxs-lookup"><span data-stu-id="49120-183">Sub1</span></span></p></td>
<td><p><span data-ttu-id="49120-184">SubCat1</span><span class="sxs-lookup"><span data-stu-id="49120-184">SubCat1</span></span></p></td>
<td><p><span data-ttu-id="49120-185">EUR</span><span class="sxs-lookup"><span data-stu-id="49120-185">EUR</span></span></p></td>
<td><p><span data-ttu-id="49120-186">รายเดือน</span><span class="sxs-lookup"><span data-stu-id="49120-186">Monthly</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="49120-187">00021_135</span><span class="sxs-lookup"><span data-stu-id="49120-187">00021_135</span></span></p></td>
<td><p><span data-ttu-id="49120-188">9030</span><span class="sxs-lookup"><span data-stu-id="49120-188">9030</span></span></p></td>
<td><p><span data-ttu-id="49120-189">Sub1</span><span class="sxs-lookup"><span data-stu-id="49120-189">Sub1</span></span></p></td>
<td><p><span data-ttu-id="49120-190">SubCat2</span><span class="sxs-lookup"><span data-stu-id="49120-190">SubCat2</span></span></p></td>
<td><p><span data-ttu-id="49120-191">EUR</span><span class="sxs-lookup"><span data-stu-id="49120-191">EUR</span></span></p></td>
<td><p><span data-ttu-id="49120-192">รายเดือน</span><span class="sxs-lookup"><span data-stu-id="49120-192">Monthly</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="49120-193">ตอนนี้คุณสร้างค่าธรรมเนียมการสั่งซื้อโดยบอกรับเป็นสมาชิกสำหรับการบอกรับเป็นสมาชิกทั้งสองในประเภทของการบอกรับเป็นสมาชิก Sub1:</span><span class="sxs-lookup"><span data-stu-id="49120-193">Now you create subscription fees for both subscriptions in the subscription group Sub1:</span></span>

1.  <span data-ttu-id="49120-194">คลิก **การจัดการงานบริการ** \> **การตั้งค่า** \> **การบอกรับเป็นสมาชิกการบริการ** \> **กลุ่มการบอกรับเป็นสมาชิก**</span><span class="sxs-lookup"><span data-stu-id="49120-194">Click **Service management** \> **Setup** \> **Service subscriptions** \> **Subscription groups**.</span></span>

2.  <span data-ttu-id="49120-195">ในฟอร์ม **กลุ่มการบอกรับเป็นสมาชิก** คลิก **ฟังก์ชัน** \> **สร้างค่าธรรมเนียมการบอกรับเป็นสมาชิก**</span><span class="sxs-lookup"><span data-stu-id="49120-195">In the **Subscription groups** form, click **Function** \> **Create subscription fee**.</span></span>

3.  <span data-ttu-id="49120-196">ในแบบฟอร์ม **สร้างค่าธรรมเนียมการบอกรับเป็นสมาชิก** ให้ป้อนข้อมูลที่เหมาะสม</span><span class="sxs-lookup"><span data-stu-id="49120-196">In the **Create subscription fee** form, enter the appropriate information.</span></span> <span data-ttu-id="49120-197">สำหรับข้อมูลเพิ่มเติม ให้ดูที่ [สร้างธุรกรรมค่าธรรมเนียมสำหรับการบอกรับเป็นสมาชิก](create-subscription-fee-transactions.md)</span><span class="sxs-lookup"><span data-stu-id="49120-197">For more information, see [Create subscription fee transactions](create-subscription-fee-transactions.md).</span></span>

<span data-ttu-id="49120-198">ค่าธรรมเนียมการบอกรับเป็นสมาชิกที่มีราคาขาย EUR 500 จะถูกสร้างขึ้นสำหรับการบอกรับเป็นสมาชิกทั้งสองรายการ ดังที่แสดงในตารางต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="49120-198">Subscription fees that have a sales price of EUR 500 are created for both subscriptions, as shown in the following table.</span></span>

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
<th><p><span data-ttu-id="49120-199">วันที่โครงการ</span><span class="sxs-lookup"><span data-stu-id="49120-199">Project date</span></span></p></th>
<th><p><span data-ttu-id="49120-200">การบอกรับเป็นสมาชิกการบริการ</span><span class="sxs-lookup"><span data-stu-id="49120-200">Service subscription</span></span></p></th>
<th><p><span data-ttu-id="49120-201">Project</span><span class="sxs-lookup"><span data-stu-id="49120-201">Project</span></span></p></th>
<th><p><span data-ttu-id="49120-202">ประเภท</span><span class="sxs-lookup"><span data-stu-id="49120-202">Category</span></span></p></th>
<th><p><span data-ttu-id="49120-203">วันที่เริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="49120-203">Start date</span></span></p></th>
<th><p><span data-ttu-id="49120-204">วันที่สิ้นสุด</span><span class="sxs-lookup"><span data-stu-id="49120-204">End date</span></span></p></th>
<th><p><span data-ttu-id="49120-205">สกุลเงินที่ใช้ในการขาย</span><span class="sxs-lookup"><span data-stu-id="49120-205">Sales currency</span></span></p></th>
<th><p><span data-ttu-id="49120-206">ราคาขาย</span><span class="sxs-lookup"><span data-stu-id="49120-206">Sales price</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="49120-207">วันที่ 28-08-2006</span><span class="sxs-lookup"><span data-stu-id="49120-207">28-08-2006</span></span></p></td>
<td><p><span data-ttu-id="49120-208">00020_135</span><span class="sxs-lookup"><span data-stu-id="49120-208">00020_135</span></span></p></td>
<td><p><span data-ttu-id="49120-209">9030</span><span class="sxs-lookup"><span data-stu-id="49120-209">9030</span></span></p></td>
<td><p><span data-ttu-id="49120-210">SubCat1</span><span class="sxs-lookup"><span data-stu-id="49120-210">SubCat1</span></span></p></td>
<td><p><span data-ttu-id="49120-211">วันที่ 01-01-2007</span><span class="sxs-lookup"><span data-stu-id="49120-211">01-01-2007</span></span></p></td>
<td><p><span data-ttu-id="49120-212">วันที่ 31-03-2007</span><span class="sxs-lookup"><span data-stu-id="49120-212">31-03-2007</span></span></p></td>
<td><p><span data-ttu-id="49120-213">EUR</span><span class="sxs-lookup"><span data-stu-id="49120-213">EUR</span></span></p></td>
<td><p><span data-ttu-id="49120-214">500</span><span class="sxs-lookup"><span data-stu-id="49120-214">500</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="49120-215">วันที่ 28-08-2006</span><span class="sxs-lookup"><span data-stu-id="49120-215">28-08-2006</span></span></p></td>
<td><p><span data-ttu-id="49120-216">00021_135</span><span class="sxs-lookup"><span data-stu-id="49120-216">00021_135</span></span></p></td>
<td><p><span data-ttu-id="49120-217">9030</span><span class="sxs-lookup"><span data-stu-id="49120-217">9030</span></span></p></td>
<td><p><span data-ttu-id="49120-218">SubCat2</span><span class="sxs-lookup"><span data-stu-id="49120-218">SubCat2</span></span></p></td>
<td><p><span data-ttu-id="49120-219">วันที่ 01-01-2007</span><span class="sxs-lookup"><span data-stu-id="49120-219">01-01-2007</span></span></p></td>
<td><p><span data-ttu-id="49120-220">วันที่ 31-03-2007</span><span class="sxs-lookup"><span data-stu-id="49120-220">31-03-2007</span></span></p></td>
<td><p><span data-ttu-id="49120-221">EUR</span><span class="sxs-lookup"><span data-stu-id="49120-221">EUR</span></span></p></td>
<td><p><span data-ttu-id="49120-222">500</span><span class="sxs-lookup"><span data-stu-id="49120-222">500</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="49120-223">จากนั้น</span><span class="sxs-lookup"><span data-stu-id="49120-223">Later, you decide that you want to specify sales prices for the category SubCat1 for project 9030.</span></span> <span data-ttu-id="49120-224">ดังนั้น คุณสร้างรายการราคาขายใหม่ที่มีราคาขายเป็น EUR 550 สำหรับการรวมของโครงการ 9030 และประเภทค่าธรรมเนียม SubCat1</span><span class="sxs-lookup"><span data-stu-id="49120-224">Therefore, you create a new sales price line that has a sales price of EUR 550 for the combination of project 9030 and fee category SubCat1.</span></span> <span data-ttu-id="49120-225">ตอนนี้ จึงมีรายการราคาขายการบอกรับเป็นสมาชิกสองรายการสำหรับโครงการ 9030 ดังที่แสดงอยู่ในตารางต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="49120-225">There are now two subscription sales price lines for project 9030, as shown in the following table.</span></span>

<table style="width:100%;">
<colgroup>
<col style="width: 14%" />
<col style="width: 14%" />
<col style="width: 14%" />
<col style="width: 14%" />
<col style="width: 14%" />
<col style="width: 14%" />
<col style="width: 14%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="49120-226">ใช้ได้ตั้งแต่</span><span class="sxs-lookup"><span data-stu-id="49120-226">Valid from</span></span></p></th>
<th><p><span data-ttu-id="49120-227">ประเภท</span><span class="sxs-lookup"><span data-stu-id="49120-227">Category</span></span></p></th>
<th><p><span data-ttu-id="49120-228">Project</span><span class="sxs-lookup"><span data-stu-id="49120-228">Project</span></span></p></th>
<th><p><span data-ttu-id="49120-229">การบอกรับเป็นสมาชิก</span><span class="sxs-lookup"><span data-stu-id="49120-229">Subscription</span></span></p></th>
<th><p><span data-ttu-id="49120-230">ชนิดรอบระยะเวลาบัญชี</span><span class="sxs-lookup"><span data-stu-id="49120-230">Period code</span></span></p></th>
<th><p><span data-ttu-id="49120-231">สกุลเงิน</span><span class="sxs-lookup"><span data-stu-id="49120-231">Currency</span></span></p></th>
<th><p><span data-ttu-id="49120-232">ราคาขาย</span><span class="sxs-lookup"><span data-stu-id="49120-232">Sales price</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="49120-233">วันที่ 28-08-2007</span><span class="sxs-lookup"><span data-stu-id="49120-233">28-08-2007</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="49120-234">9030</span><span class="sxs-lookup"><span data-stu-id="49120-234">9030</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="49120-235">เดือน</span><span class="sxs-lookup"><span data-stu-id="49120-235">Month</span></span></p></td>
<td><p><span data-ttu-id="49120-236">EUR</span><span class="sxs-lookup"><span data-stu-id="49120-236">EUR</span></span></p></td>
<td><p><span data-ttu-id="49120-237">500</span><span class="sxs-lookup"><span data-stu-id="49120-237">500</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="49120-238">วันที่ 28-08-2007</span><span class="sxs-lookup"><span data-stu-id="49120-238">28-08-2007</span></span></p></td>
<td><p><span data-ttu-id="49120-239">SubCat1</span><span class="sxs-lookup"><span data-stu-id="49120-239">SubCat1</span></span></p></td>
<td><p><span data-ttu-id="49120-240">9030</span><span class="sxs-lookup"><span data-stu-id="49120-240">9030</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="49120-241">เดือน</span><span class="sxs-lookup"><span data-stu-id="49120-241">Month</span></span></p></td>
<td><p><span data-ttu-id="49120-242">EUR</span><span class="sxs-lookup"><span data-stu-id="49120-242">EUR</span></span></p></td>
<td><p><span data-ttu-id="49120-243">550</span><span class="sxs-lookup"><span data-stu-id="49120-243">550</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="49120-244">คุณทำขั้นตอนที่อธิบายไว้ข้างต้นซ้ำเพื่อสร้างค่าธรรมเนียมการสั่งซื้อโดยบอกรับเป็นสมาชิกสำหรับการบอกรับเป็นสมาชิกทั้งสองในประเภทของการบอกรับเป็นสมาชิก Sub1 ธุรกรรมสองรายการจะถูกสร้างขึ้น</span><span class="sxs-lookup"><span data-stu-id="49120-244">You repeat the procedure described above to create subscription fees for both subscriptions in the subscription group Sub1.</span></span> <span data-ttu-id="49120-245">ตารางต่อไปนี้แสดงธุรกรรมที่ถูกสร้างขึ้นสำหรับการบอกรับเป็นสมาชิกแต่ละรายการ ที่ถูกแนบกับกลุ่มการบอกรับเป็นสมาชิก</span><span class="sxs-lookup"><span data-stu-id="49120-245">The following table shows the transactions that are created for each subscription that is attached to the subscription group.</span></span>

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
<th><p><span data-ttu-id="49120-246">วันที่โครงการ</span><span class="sxs-lookup"><span data-stu-id="49120-246">Project date</span></span></p></th>
<th><p><span data-ttu-id="49120-247">การบอกรับเป็นสมาชิก</span><span class="sxs-lookup"><span data-stu-id="49120-247">Subscription</span></span></p></th>
<th><p><span data-ttu-id="49120-248">Project</span><span class="sxs-lookup"><span data-stu-id="49120-248">Project</span></span></p></th>
<th><p><span data-ttu-id="49120-249">ประเภท</span><span class="sxs-lookup"><span data-stu-id="49120-249">Category</span></span></p></th>
<th><p><span data-ttu-id="49120-250">วันที่เริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="49120-250">Start date</span></span></p></th>
<th><p><span data-ttu-id="49120-251">วันที่สิ้นสุด</span><span class="sxs-lookup"><span data-stu-id="49120-251">End date</span></span></p></th>
<th><p><span data-ttu-id="49120-252">สกุลเงินที่ใช้ในการขาย</span><span class="sxs-lookup"><span data-stu-id="49120-252">Sales currency</span></span></p></th>
<th><p><span data-ttu-id="49120-253">ราคาขาย</span><span class="sxs-lookup"><span data-stu-id="49120-253">Sales price</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="49120-254">วันที่ 28-07-2007</span><span class="sxs-lookup"><span data-stu-id="49120-254">28-07-2007</span></span></p></td>
<td><p><span data-ttu-id="49120-255">00020_135</span><span class="sxs-lookup"><span data-stu-id="49120-255">00020_135</span></span></p></td>
<td><p><span data-ttu-id="49120-256">9030</span><span class="sxs-lookup"><span data-stu-id="49120-256">9030</span></span></p></td>
<td><p><span data-ttu-id="49120-257">SubCat1</span><span class="sxs-lookup"><span data-stu-id="49120-257">SubCat1</span></span></p></td>
<td><p><span data-ttu-id="49120-258">วันที่ 01-01-2008</span><span class="sxs-lookup"><span data-stu-id="49120-258">01-01-2008</span></span></p></td>
<td><p><span data-ttu-id="49120-259">วันที่ 31-03-2008</span><span class="sxs-lookup"><span data-stu-id="49120-259">31-03-2008</span></span></p></td>
<td><p><span data-ttu-id="49120-260">EUR</span><span class="sxs-lookup"><span data-stu-id="49120-260">EUR</span></span></p></td>
<td><p><span data-ttu-id="49120-261">550</span><span class="sxs-lookup"><span data-stu-id="49120-261">550</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="49120-262">วันที่ 28-07-2008</span><span class="sxs-lookup"><span data-stu-id="49120-262">28-07-2008</span></span></p></td>
<td><p><span data-ttu-id="49120-263">00021_135</span><span class="sxs-lookup"><span data-stu-id="49120-263">00021_135</span></span></p></td>
<td><p><span data-ttu-id="49120-264">9030</span><span class="sxs-lookup"><span data-stu-id="49120-264">9030</span></span></p></td>
<td><p><span data-ttu-id="49120-265">SubCat2</span><span class="sxs-lookup"><span data-stu-id="49120-265">SubCat2</span></span></p></td>
<td><p><span data-ttu-id="49120-266">วันที่ 01-01-2008</span><span class="sxs-lookup"><span data-stu-id="49120-266">01-01-2008</span></span></p></td>
<td><p><span data-ttu-id="49120-267">วันที่ 31-03-2008</span><span class="sxs-lookup"><span data-stu-id="49120-267">31-03-2008</span></span></p></td>
<td><p><span data-ttu-id="49120-268">EUR</span><span class="sxs-lookup"><span data-stu-id="49120-268">EUR</span></span></p></td>
<td><p><span data-ttu-id="49120-269">500</span><span class="sxs-lookup"><span data-stu-id="49120-269">500</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="49120-270">ในธุรกรรมแรกของการบอกรับเป็นสมาชิก 00020\_135 ราคาขายจำนวน EUR 550 ได้มาจากราคาขายสำหรับการบอกรับเป็นสมาชิกที่ถูกตั้งค่าสำหรับชุดโครงการและประเภทที่กำหนดไว้</span><span class="sxs-lookup"><span data-stu-id="49120-270">In the first transaction for subscription 00020\_135, the sales price of EUR 550 derives from the subscription sales price that is set up for the combination of the specific project and category.</span></span> <span data-ttu-id="49120-271">ในธุรกรรมที่สองสำหรับการบอกรับเป็นสมาชิก 00021\_135 มีการใช้ราคาขายจำนวน EUR 500 เป็นราคาขายสำหรับการบอกรับเป็นสมาชิกของโครงการ เนื่องจากไม่มีการตั้งค่าราคาสำหรับชุดโครงการ 9030 และประเภท SubCat2</span><span class="sxs-lookup"><span data-stu-id="49120-271">In the second transaction for subscription 00021\_135, the sales price of EUR 500 is used as the project subscription sales price because there is no price set up for the combination of project 9030 and category SubCat2.</span></span>

## <a name="see-also"></a><span data-ttu-id="49120-272">ดูเพิ่มเติมที่</span><span class="sxs-lookup"><span data-stu-id="49120-272">See also</span></span>

[<span data-ttu-id="49120-273">การอัพเดตและการจัดดัชนีราคาขายของการสั่งซื้อโดยบอกรับเป็นสมาชิก</span><span class="sxs-lookup"><span data-stu-id="49120-273">Update and index subscription sales prices</span></span>](update-and-index-subscription-sales-prices.md)

  




[!INCLUDE[footer-include](../../includes/footer-banner.md)]