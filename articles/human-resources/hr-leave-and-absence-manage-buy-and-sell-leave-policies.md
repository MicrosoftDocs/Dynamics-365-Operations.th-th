---
title: จัดการนโยบายการซื้อและการขายการลางาน
description: คุณสามารถเปิดใช้งานพนักงานเพื่อซื้อและขายการลางานใน Dynamics 365 Human Resources
author: andreabichsel
manager: AnnBe
ms.date: 06/01/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
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
ms.openlocfilehash: 859445f2b6e980b5960e512e69129f6a8fc6df2b
ms.sourcegitcommit: ba340f836e472f13f263dec46a49847c788fca44
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 06/04/2020
ms.locfileid: "3429024"
---
# <a name="manage-buy-and-sell-leave-policies"></a><span data-ttu-id="05bfa-103">จัดการนโยบายการซื้อและการขายการลางาน</span><span class="sxs-lookup"><span data-stu-id="05bfa-103">Manage buy and sell leave policies</span></span>

[!include [banner](includes/preview-feature.md)]

<span data-ttu-id="05bfa-104">คุณสามารถเปิดใช้งานให้พนักงานซื้อการลางานได้โดยการสร้างนโยบายการซื้อการลางาน</span><span class="sxs-lookup"><span data-stu-id="05bfa-104">You can enable employees to buy leave by creating a buy leave policy.</span></span>  

## <a name="enable-employees-to-buy-and-sell-leave"></a><span data-ttu-id="05bfa-105">เปิดใช้งานให้พนักงานซื้อและขายการลางานได้</span><span class="sxs-lookup"><span data-stu-id="05bfa-105">Enable employees to buy and sell leave</span></span>

1. <span data-ttu-id="05bfa-106">บนหน้า **พารามิเตอร์การลางานและการขาดงาน** ให้เลือก **ใช่** สำหรับ **อนุญาตให้พนักงานซื้อการลางาน**</span><span class="sxs-lookup"><span data-stu-id="05bfa-106">On the **Leave and absence parameters** page, select **Yes** for **Allow employees to buy leave**.</span></span> 

## <a name="create-a-buy-leave-policy"></a><span data-ttu-id="05bfa-107">สร้างนโยบายการซื้อการลางาน</span><span class="sxs-lookup"><span data-stu-id="05bfa-107">Create a buy leave policy</span></span>

1. <span data-ttu-id="05bfa-108">ในหน้า **การขาดงานและการลางาน** โปรดเลือกแท็บ **ลิงค์**</span><span class="sxs-lookup"><span data-stu-id="05bfa-108">On the **Leave and absence** page, select the **Links** tab.</span></span> 

2. <span data-ttu-id="05bfa-109">เลือก **นโยบายการซื้อและการขายการลางาน**</span><span class="sxs-lookup"><span data-stu-id="05bfa-109">Select **Buy and sell leave policy**.</span></span>

3. <span data-ttu-id="05bfa-110">เลือก **ใหม่**</span><span class="sxs-lookup"><span data-stu-id="05bfa-110">Select **New**.</span></span>

4. <span data-ttu-id="05bfa-111">ป้อน **ชื่อ** และ **คำอธิบาย** สำหรับนโยบายภายใต้ **นโยบายการซื้อและการขายการลางาน**</span><span class="sxs-lookup"><span data-stu-id="05bfa-111">Enter a **Name** and **Description** for the policy under **Buy and sell leave policy**.</span></span> 

5. <span data-ttu-id="05bfa-112">เลือก **ชนิดนโยบาย**</span><span class="sxs-lookup"><span data-stu-id="05bfa-112">Select a **Policy type**.</span></span> 

   <span data-ttu-id="05bfa-113">ชนิดนโยบายที่พร้อมใช้งาน ได้แก่ **จำนวน** และ **ชั่วโมงต่อสัปดาห์**</span><span class="sxs-lookup"><span data-stu-id="05bfa-113">The available policy types are **Amount** and **Hours per week**.</span></span> <span data-ttu-id="05bfa-114">เลือก **จำนวน** ที่จะป้อน **ยอดเงินคงที่** สำหรับจำนวนสูงสุดที่พนักงานสามารถซื้อและขายได้</span><span class="sxs-lookup"><span data-stu-id="05bfa-114">Select **Amount** to enter a **Fixed amount** for the maximum amounts employees can buy and sell.</span></span> <span data-ttu-id="05bfa-115">ถ้าคุณเลือก **ชั่วโมงต่อสัปดาห์** เวลาการทำงานที่กำหนดในปฏิทินเวลาการทำงานที่กำหนดของพนักงาน จะถูกใช้เพื่อกำหนดจำนวนสูงสุดของนโยบาย</span><span class="sxs-lookup"><span data-stu-id="05bfa-115">If you select **Hours per week**, the working time defined in the employee's assigned working time calendar is used to determine the maximum amount of the policy.</span></span> 

6. <span data-ttu-id="05bfa-116">เลือก **วันที่เริ่มต้น** และ **วันที่สิ้นสุด** สำหรับนโยบาย</span><span class="sxs-lookup"><span data-stu-id="05bfa-116">Select a **Start date** and **End date** for the policy.</span></span> <span data-ttu-id="05bfa-117">คำขอในการซื้อหรือการขายการลางานจะพร้อมใช้งานสำหรับการส่งในระหว่างกรอบเวลานี้เท่านั้น</span><span class="sxs-lookup"><span data-stu-id="05bfa-117">Requests to buy or sell leave will only be available for submission during this time frame.</span></span> 

7. <span data-ttu-id="05bfa-118">ภายใต้ **นโยบายการซื้อ** ให้เลือก **การทำงานเทียบเท่าบุคลากรเต็มเวลา** (FTE) เพื่อแบ่งตามสัดส่วนจำนวนสูงสุดตาม FTE ที่กำหนดไว้ในตำแหน่งของพนักงาน</span><span class="sxs-lookup"><span data-stu-id="05bfa-118">Under **Buy policy**, select **Full time equivalency** (FTE) to prorate the maximum amount based on the FTE defined on the employee's position.</span></span> <span data-ttu-id="05bfa-119">ถ้าชนิดนโยบายเป็น **จำนวน** ให้ป้อน **จำนวนคงที่สูงสุด**</span><span class="sxs-lookup"><span data-stu-id="05bfa-119">If the policy type is **Amount**, enter a **Maximum fixed amount**.</span></span> 

8. <span data-ttu-id="05bfa-120">เลือก **เพิ่ม** เพื่อเพิ่มชนิดการลางานสำหรับพนักงานที่จะซื้อการลางาน</span><span class="sxs-lookup"><span data-stu-id="05bfa-120">Select **Add** to add the leave types for employees to buy leave.</span></span> <span data-ttu-id="05bfa-121">คุณสามารถเพิ่มชนิดการลางานหลายชนิดไปยังนโยบายได้</span><span class="sxs-lookup"><span data-stu-id="05bfa-121">You can add multiple leave types to the policy.</span></span> 

9. <span data-ttu-id="05bfa-122">ป้อน **เดือนของการบริการ** สำหรับชนิดการลางานเพื่อเปิดใช้งานเดือนต่างๆ ของบริการเพื่อกำหนดจำนวนสูงสุดที่พนักงานสามารถซื้อได้</span><span class="sxs-lookup"><span data-stu-id="05bfa-122">Enter the **Months of service** for the leave type to enable different months of service to determine the maximum amount an employee can buy.</span></span> 

10. <span data-ttu-id="05bfa-123">ป้อน **จำนวนสูงสุด** สำหรับชนิดการลางาน</span><span class="sxs-lookup"><span data-stu-id="05bfa-123">Enter the **Maximum amount** for the leave type.</span></span> 

11. <span data-ttu-id="05bfa-124">ป้อน **อัตรา** ที่พนักงานจะซื้อการลางาน</span><span class="sxs-lookup"><span data-stu-id="05bfa-124">Enter the **Rate** at which the employee will buy the leave.</span></span> 

12. <span data-ttu-id="05bfa-125">หรือป้อน **รหัสรายได้** ที่จะใช้สำหรับการซื้อการลางาน</span><span class="sxs-lookup"><span data-stu-id="05bfa-125">Optionally enter the **Earning code** to be used for buying leave.</span></span> 

13. <span data-ttu-id="05bfa-126">หรือตั้งค่าว่าจะใช้ FTE เพื่อกำหนดจำนวนสูงสุดสำหรับชนิดการลางานหรือไม่</span><span class="sxs-lookup"><span data-stu-id="05bfa-126">Optionally set whether to use FTE to determine the maximum amount for the leave type.</span></span> 

## <a name="add-the-buy-and-sell-leave-policy-to-a-leave-and-absence-plan"></a><span data-ttu-id="05bfa-127">เพิ่มนโยบายการซื้อและการขายการลางานไปยังแผนการลางานและการขาดงาน</span><span class="sxs-lookup"><span data-stu-id="05bfa-127">Add the buy and sell leave policy to a leave and absence plan</span></span>

1. <span data-ttu-id="05bfa-128">บนหน้า **การลางานและการขาดงาน** ให้เลือกแผนการลางานและการขาดงาน</span><span class="sxs-lookup"><span data-stu-id="05bfa-128">On the **Leave and absence** page, select a leave and absence plan.</span></span>

2. <span data-ttu-id="05bfa-129">ภายใต้ **กฎ** เลือก **นโยบายการซื้อและการขายการลางาน**</span><span class="sxs-lookup"><span data-stu-id="05bfa-129">Under **Rules**, select **Buy and sell leave policy**.</span></span>

## <a name="see-also"></a><span data-ttu-id="05bfa-130">ดูเพิ่มเติมที่</span><span class="sxs-lookup"><span data-stu-id="05bfa-130">See also</span></span>

[<span data-ttu-id="05bfa-131">ภาพรวมการลางานและการขาดงาน</span><span class="sxs-lookup"><span data-stu-id="05bfa-131">Leave and absence overview</span></span>](hr-leave-and-absence-overview.md)</br>
[<span data-ttu-id="05bfa-132">ตั้งค่าคอนฟิกชนิดการลางานและการขาดงาน</span><span class="sxs-lookup"><span data-stu-id="05bfa-132">Configure leave and absence types</span></span>](hr-leave-and-absence-types.md)</br>
[<span data-ttu-id="05bfa-133">ตั้งรายการค้างรับแผนการลางานและการขาดงาน</span><span class="sxs-lookup"><span data-stu-id="05bfa-133">Accrue leave and absence plans</span></span>](hr-leave-and-absence-accrue.md)</br>
[<span data-ttu-id="05bfa-134">ซื้อและขายวันลางาน</span><span class="sxs-lookup"><span data-stu-id="05bfa-134">Buy and sell leave</span></span>](hr-employee-self-service-buy-sell-leave.md)

