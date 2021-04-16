---
title: จัดการนโยบายการซื้อและการขายการลางาน
description: คุณสามารถเปิดใช้งานพนักงานเพื่อซื้อและขายการลางานใน Dynamics 365 Human Resources
author: andreabichsel
ms.date: 08/20/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: LeaveBuySellPolicy, LeavePlanFormPart, LeaveAbsenceWorkspace
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-06-01
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: f03d6055c407b2c3e13831c8b5a6f8b0d6c47897
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 03/31/2021
ms.locfileid: "5794720"
---
# <a name="manage-buy-and-sell-leave-policies"></a><span data-ttu-id="5d74b-103">จัดการนโยบายซื้อและขายวันลางาน</span><span class="sxs-lookup"><span data-stu-id="5d74b-103">Manage buy and sell leave policies</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="5d74b-104">คุณสามารถช่วยให้พนักงานซื้อและขายวันลาได้โดยการสร้างนโยบายการซื้อและการขายวันลา</span><span class="sxs-lookup"><span data-stu-id="5d74b-104">You can enable employees to buy and sell leave by creating a buy and sell leave policy.</span></span> <span data-ttu-id="5d74b-105">คุณสามารถตั้งค่าคอนฟิกนโยบายเหล่านี้เพื่อใช้ลำดับงานสำหรับการอนุมัติได้ กำหนดจำนวนเงิน และอัตราสูงสุด และตั้งค่าอัตราสำหรับการซื้อและการขาย</span><span class="sxs-lookup"><span data-stu-id="5d74b-105">You can configure these policies to use workflow for approvals, set maximum amounts and rates, and set rates for buying and selling.</span></span> 

## <a name="enable-employees-to-buy-and-sell-leave"></a><span data-ttu-id="5d74b-106">เปิดใช้งานให้พนักงานซื้อและขายการลางานได้</span><span class="sxs-lookup"><span data-stu-id="5d74b-106">Enable employees to buy and sell leave</span></span>

1. <span data-ttu-id="5d74b-107">บนหน้า **พารามิเตอร์การลางานและการขาดงาน** เลือก **ใช่** สำหรับ **อนุญาตให้พนักงานซื้อวันลา** และ **อนุญาตให้พนักงานขายวันลา**</span><span class="sxs-lookup"><span data-stu-id="5d74b-107">On the **Leave and absence parameters** page, select **Yes** for **Allow employees to buy leave** and **Allow employees to sell leave**.</span></span>

## <a name="create-a-buy-and-sell-leave-policy"></a><span data-ttu-id="5d74b-108">สร้างนโยบายการซื้อและการขายวันลา</span><span class="sxs-lookup"><span data-stu-id="5d74b-108">Create a buy and sell leave policy</span></span>

1. <span data-ttu-id="5d74b-109">ในหน้า **การขาดงานและการลางาน** โปรดเลือกแท็บ **ลิงค์**</span><span class="sxs-lookup"><span data-stu-id="5d74b-109">On the **Leave and absence** page, select the **Links** tab.</span></span> 

2. <span data-ttu-id="5d74b-110">เลือก **นโยบายการซื้อและการขายการลางาน**</span><span class="sxs-lookup"><span data-stu-id="5d74b-110">Select **Buy and sell leave policy**.</span></span>

3. <span data-ttu-id="5d74b-111">เลือก **ใหม่**</span><span class="sxs-lookup"><span data-stu-id="5d74b-111">Select **New**.</span></span>

4. <span data-ttu-id="5d74b-112">ป้อน **ชื่อ** และ **คำอธิบาย** สำหรับนโยบายภายใต้ **นโยบายการซื้อและการขายการลางาน**</span><span class="sxs-lookup"><span data-stu-id="5d74b-112">Enter a **Name** and **Description** for the policy under **Buy and sell leave policy**.</span></span> 

5. <span data-ttu-id="5d74b-113">เลือก **ชนิดนโยบาย**</span><span class="sxs-lookup"><span data-stu-id="5d74b-113">Select a **Policy type**.</span></span> 

   <span data-ttu-id="5d74b-114">ชนิดนโยบายที่พร้อมใช้งาน ได้แก่ **จำนวน** และ **ชั่วโมงต่อสัปดาห์**</span><span class="sxs-lookup"><span data-stu-id="5d74b-114">The available policy types are **Amount** and **Hours per week**.</span></span> <span data-ttu-id="5d74b-115">เลือก **จำนวน** ที่จะป้อน **ยอดเงินคงที่** สำหรับจำนวนสูงสุดที่พนักงานสามารถซื้อและขายได้</span><span class="sxs-lookup"><span data-stu-id="5d74b-115">Select **Amount** to enter a **Fixed amount** for the maximum amounts employees can buy and sell.</span></span> <span data-ttu-id="5d74b-116">ถ้าคุณเลือก **ชั่วโมงต่อสัปดาห์** เวลาการทำงานที่กำหนดในปฏิทินเวลาการทำงานที่กำหนดของพนักงาน จะถูกใช้เพื่อกำหนดจำนวนสูงสุดของนโยบาย</span><span class="sxs-lookup"><span data-stu-id="5d74b-116">If you select **Hours per week**, the working time defined in the employee's assigned working time calendar is used to determine the maximum amount of the policy.</span></span> 

6. <span data-ttu-id="5d74b-117">เลือก **วันที่เริ่มต้น** และ **วันที่สิ้นสุด** สำหรับนโยบาย</span><span class="sxs-lookup"><span data-stu-id="5d74b-117">Select a **Start date** and **End date** for the policy.</span></span> <span data-ttu-id="5d74b-118">คำขอในการซื้อหรือการขายการลางานจะพร้อมใช้งานสำหรับการส่งในระหว่างกรอบเวลานี้เท่านั้น</span><span class="sxs-lookup"><span data-stu-id="5d74b-118">Requests to buy or sell leave will only be available for submission during this time frame.</span></span> 

7. <span data-ttu-id="5d74b-119">เลือก **รหัสลำดับงาน** สำหรับนโยบาย</span><span class="sxs-lookup"><span data-stu-id="5d74b-119">Select a **Workflow ID** for the policy.</span></span> <span data-ttu-id="5d74b-120">คำขอซื้อและขายจะใช้ลำดับงานนี้เพื่อการตรวจทานและการอนุมัติ</span><span class="sxs-lookup"><span data-stu-id="5d74b-120">Any buy and sell requests will use this workflow for review and approval.</span></span> 

8. <span data-ttu-id="5d74b-121">ภายใต้ **นโยบายการซื้อ** ให้เลือก **การทำงานเทียบเท่าบุคลากรเต็มเวลา** (FTE) เพื่อแบ่งตามสัดส่วนจำนวนสูงสุดตาม FTE ที่กำหนดไว้ในตำแหน่งของพนักงาน</span><span class="sxs-lookup"><span data-stu-id="5d74b-121">Under **Buy policy**, select **Full time equivalency** (FTE) to prorate the maximum amount based on the FTE defined on the employee's position.</span></span> <span data-ttu-id="5d74b-122">ถ้าชนิดนโยบายเป็น **จำนวน** ให้ป้อน **จำนวนคงที่สูงสุด**</span><span class="sxs-lookup"><span data-stu-id="5d74b-122">If the policy type is **Amount**, enter a **Maximum fixed amount**.</span></span> 

9. <span data-ttu-id="5d74b-123">เลือก **เพิ่ม** เพื่อเพิ่มชนิดการลางานสำหรับพนักงานที่จะซื้อการลางาน</span><span class="sxs-lookup"><span data-stu-id="5d74b-123">Select **Add** to add the leave types for employees to buy leave.</span></span> <span data-ttu-id="5d74b-124">คุณสามารถเพิ่มชนิดการลางานหลายชนิดไปยังนโยบายได้</span><span class="sxs-lookup"><span data-stu-id="5d74b-124">You can add multiple leave types to the policy.</span></span> 

10. <span data-ttu-id="5d74b-125">ป้อน **เดือนของการบริการ** สำหรับชนิดการลางานเพื่อเปิดใช้งานเดือนต่างๆ ของบริการเพื่อกำหนดจำนวนสูงสุดที่พนักงานสามารถซื้อได้</span><span class="sxs-lookup"><span data-stu-id="5d74b-125">Enter the **Months of service** for the leave type to enable different months of service to determine the maximum amount an employee can buy.</span></span> 

11. <span data-ttu-id="5d74b-126">ป้อน **จำนวนสูงสุด** สำหรับชนิดการลางาน</span><span class="sxs-lookup"><span data-stu-id="5d74b-126">Enter the **Maximum amount** for the leave type.</span></span> 

12. <span data-ttu-id="5d74b-127">ป้อน **อัตรา** ที่พนักงานจะซื้อการลางาน</span><span class="sxs-lookup"><span data-stu-id="5d74b-127">Enter the **Rate** at which the employee will buy the leave.</span></span> 

13. <span data-ttu-id="5d74b-128">หรือป้อน **รหัสรายได้** ที่จะใช้สำหรับการซื้อการลางาน</span><span class="sxs-lookup"><span data-stu-id="5d74b-128">Optionally enter the **Earning code** to be used for buying leave.</span></span> 

14. <span data-ttu-id="5d74b-129">หรือตั้งค่าว่าจะใช้ FTE เพื่อกำหนดจำนวนสูงสุดสำหรับชนิดการลางานหรือไม่</span><span class="sxs-lookup"><span data-stu-id="5d74b-129">Optionally set whether to use FTE to determine the maximum amount for the leave type.</span></span> 

15. <span data-ttu-id="5d74b-130">เมื่อต้องการสร้างนโยบายการขาย ให้ทำตามขั้นตอนที่ 8 ถึง 14 ภายใต้ **นโยบายการขาย**</span><span class="sxs-lookup"><span data-stu-id="5d74b-130">To create a sell policy, follow steps 8 through 14 under **Sell policy**.</span></span> 

## <a name="add-the-buy-and-sell-leave-policy-to-a-leave-and-absence-plan"></a><span data-ttu-id="5d74b-131">เพิ่มนโยบายการซื้อและการขายการลางานไปยังแผนการลางานและการขาดงาน</span><span class="sxs-lookup"><span data-stu-id="5d74b-131">Add the buy and sell leave policy to a leave and absence plan</span></span>

1. <span data-ttu-id="5d74b-132">บนหน้า **การลางานและการขาดงาน** ให้เลือกแผนการลางานและการขาดงาน</span><span class="sxs-lookup"><span data-stu-id="5d74b-132">On the **Leave and absence** page, select a leave and absence plan.</span></span>

2. <span data-ttu-id="5d74b-133">ภายใต้ **กฎ** เลือก **นโยบายการซื้อและการขายการลางาน**</span><span class="sxs-lookup"><span data-stu-id="5d74b-133">Under **Rules**, select **Buy and sell leave policy**.</span></span>

## <a name="see-also"></a><span data-ttu-id="5d74b-134">ดูเพิ่มเติมที่</span><span class="sxs-lookup"><span data-stu-id="5d74b-134">See also</span></span>

[<span data-ttu-id="5d74b-135">ภาพรวมการลางานและการขาดงาน</span><span class="sxs-lookup"><span data-stu-id="5d74b-135">Leave and absence overview</span></span>](hr-leave-and-absence-overview.md)</br>
[<span data-ttu-id="5d74b-136">ตั้งค่าคอนฟิกชนิดการลางานและการขาดงาน</span><span class="sxs-lookup"><span data-stu-id="5d74b-136">Configure leave and absence types</span></span>](hr-leave-and-absence-types.md)</br>
[<span data-ttu-id="5d74b-137">ตั้งรายการค้างรับแผนการลางานและการขาดงาน</span><span class="sxs-lookup"><span data-stu-id="5d74b-137">Accrue leave and absence plans</span></span>](hr-leave-and-absence-accrue.md)</br>
[<span data-ttu-id="5d74b-138">ซื้อและขายวันลางาน</span><span class="sxs-lookup"><span data-stu-id="5d74b-138">Buy and sell leave</span></span>](hr-employee-self-service-buy-sell-leave.md)



[!INCLUDE[footer-include](../includes/footer-banner.md)]