---
title: การแก้ไขปัญหาการจัดงบประมาณสำหรับตำแหน่ง
description: บทความนี้ให้คำตอบแก่คำถามที่คุณอาจมี เมื่อคุณตั้งค่าคอนฟิกการจัดทำงบประมาณของตำแหน่ง  จะเน้นคำถามที่ถูกถามบ่อยเกี่ยวกับวิธีการสร้างองค์ประกอบต้นทุนงบประมาณ กลุ่มค่าตอบแทน และกริดค่าตอบแทน
author: panolte
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: HcmBudgetPurposeType, HcmPositionForecast
audience: Application User
ms.reviewer: roschlom
ms.custom: 88253
ms.assetid: c44df01b-8700-4022-b4c6-c4b1cb84d31d
ms.search.region: Global
ms.author: panolte
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 8211c5bd4514bffbd001f9930859f777dac7f0e1
ms.sourcegitcommit: deac22ba5377a912d93fe408c5ae875706378c2d
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 01/16/2021
ms.locfileid: "5017628"
---
# <a name="position-budgeting-troubleshooting"></a><span data-ttu-id="d319d-104">การแก้ไขปัญหาการจัดงบประมาณสำหรับตำแหน่ง</span><span class="sxs-lookup"><span data-stu-id="d319d-104">Position budgeting troubleshooting</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="d319d-105">บทความนี้ให้คำตอบแก่คำถามที่คุณอาจมี เมื่อคุณตั้งค่าคอนฟิกการจัดทำงบประมาณของตำแหน่ง </span><span class="sxs-lookup"><span data-stu-id="d319d-105">This article provides answers to questions that you might have when you configure position budgeting.</span></span> <span data-ttu-id="d319d-106">จะเน้นคำถามที่ถูกถามบ่อยเกี่ยวกับวิธีการสร้างองค์ประกอบต้นทุนงบประมาณ กลุ่มค่าตอบแทน และกริดค่าตอบแทน</span><span class="sxs-lookup"><span data-stu-id="d319d-106">It addresses frequently asked questions about how to create budget cost elements, compensation groups, and compensation grids.</span></span> 

<a name="why-cant-i-find-the-forecast-position-page-in-human-resources"></a><span data-ttu-id="d319d-107">เหตุใดฉันจึงไม่พบหน้าตำแหน่งการคาดการณ์ในทรัพยากรบุคคล</span><span class="sxs-lookup"><span data-stu-id="d319d-107">Why can’t I find the forecast position page in Human resources?</span></span>
---------------------------------------------------------------

<span data-ttu-id="d319d-108">มีการย้ายตำแหน่งตามการคาดการณ์การจัดทำงบประมาณ</span><span class="sxs-lookup"><span data-stu-id="d319d-108">Forecast positions have been moved to Budgeting.</span></span>

## <a name="why-cant-i-delete-a-budget-cost-element"></a><span data-ttu-id="d319d-109">เหตุใดฉันจึงไม่สามารถลบองค์ประกอบต้นทุนงบประมาณการ</span><span class="sxs-lookup"><span data-stu-id="d319d-109">Why can’t I delete a budget cost element?</span></span>
<span data-ttu-id="d319d-110">คุณไม่สามารถลบองค์ประกอบต้นทุนงบประมาณที่กำหนดให้กับตำแหน่งตามการคาดการณ์ </span><span class="sxs-lookup"><span data-stu-id="d319d-110">You can’t delete a budget cost element that is assigned to a forecast position.</span></span> <span data-ttu-id="d319d-111">ก่อนที่คุณสามารถลบออกองค์ประกอบต้นทุนงบประมาณ คุณต้องลบออกจากตำแหน่งตามการคาดการณ์ทั้งหมดก่อน</span><span class="sxs-lookup"><span data-stu-id="d319d-111">Before you can delete a budget cost element, you must remove it from all forecast positions.</span></span> <span data-ttu-id="d319d-112">**คำแนะนำ:** ในการค้นหาตำแหน่งทั้งหมดที่องค์ประกอบต้นทุนงบประมาณถูกกำหนดให้ ให้เลือกองค์ประกอบต้นทุนในหน้า **องค์ประกอบต้นทุนงบประมาณ** และจากนั้น คลิก **อัพเดตตำแหน่ง**</span><span class="sxs-lookup"><span data-stu-id="d319d-112">**Tip:** To find all the positions that a budget cost element is assigned to, select the cost element on the **Budget cost elements** page, and then click **Update positions**.</span></span> <span data-ttu-id="d319d-113">ตำแหน่งที่ใช้องค์ประกอบต้นทุนถูกแสดงรายการอยู่ในกริดด้านบน</span><span class="sxs-lookup"><span data-stu-id="d319d-113">The positions that use the cost element are listed in the upper grid.</span></span>

## <a name="how-can-i-remove-a-cost-element-from-multiple-forecast-positions-without-opening-each-one"></a><span data-ttu-id="d319d-114">ฉันสามารถลบเป็นองค์ประกอบต้นทุนจากตำแหน่งตามการคาดการณ์หลายรายการโดยไม่ต้องเปิดแต่ละรายการได้อย่างไร</span><span class="sxs-lookup"><span data-stu-id="d319d-114">How can I remove a cost element from multiple forecast positions without opening each one?</span></span>
<span data-ttu-id="d319d-115">คุณไม่สามารถลบองค์ประกอบต้นทุนได้ </span><span class="sxs-lookup"><span data-stu-id="d319d-115">You can’t remove a cost element.</span></span> <span data-ttu-id="d319d-116">อย่างไรก็ตาม ถ้าคุณเปลี่ยนวันที่เริ่มต้นและสิ้นสุด เพื่อให้อยู่นอกวันที่วงจรการวางแผนงบประมาณ องค์ประกอบต้นทุนจะไม่ถูกกำหนดให้กับตำแหน่งตามการคาดการณ์ในวงจรการวางแผนงบประมาณอีกต่อไป </span><span class="sxs-lookup"><span data-stu-id="d319d-116">However, if you change the start and end dates so that they are outside the budget planning cycle dates, the cost element will no longer be assigned to the forecast positions in that budget planning cycle.</span></span> <span data-ttu-id="d319d-117">เมื่อต้องการทำการเปลี่ยนแปลง เปิดองค์ประกอบต้นทุนงบประมาณ จากนั้น บน FastTab **การคำนวณต้นทุน** คลิก **เปลี่ยนวันที่** และเปลี่ยนแปลงวันที่มีผลบังคับใช้หรือวันที่หมดอายุ</span><span class="sxs-lookup"><span data-stu-id="d319d-117">To make this change, open the budget cost element, and then, on the **Cost calculation** FastTab, click **Change dates**, and change the effective date or expiration date.</span></span> <span data-ttu-id="d319d-118">แล้วคลิก **ตกลง** เพื่ออัพเดตตำแหน่งตามการคาดการณ์ทั้งหมด ที่องค์ประกอบต้นทุนถูกกำหนดให้โดยอัตโนมัติ</span><span class="sxs-lookup"><span data-stu-id="d319d-118">Then click **OK** to automatically update all forecast positions that the cost element is assigned to.</span></span> <span data-ttu-id="d319d-119">**คำแนะนำ:** ถ้าคุณใช้วิธีนี้ โปรดระวังว่า จะลบองค์ประกอบต้นทุนงบประมาณจากตำแหน่งตามการคาดการณ์ **ทั้งหมด** ที่วันที่เริ่มต้นและสิ้นสุดไม่อยู่ภายในช่วงที่เหมาะสมอีกต่อไป </span><span class="sxs-lookup"><span data-stu-id="d319d-119">**Tip:** If you use this method, be aware that it removes the budget cost element from **all** forecast positions where the start and end dates are no longer within the appropriate range.</span></span> <span data-ttu-id="d319d-120">ถ้าผลกระทบนี้ไม่ใช่สิ่งที่คุณต้องการ คุณต้องเปิดตำแหน่งตามการคาดการณ์แต่ละแห่งที่คุณต้องการลบองค์ประกอบต้นทุนงบประมาณ และทำการเปลี่ยนแปลงด้วยตนเอง</span><span class="sxs-lookup"><span data-stu-id="d319d-120">If this effect isn't what you intend, you must open each forecast position that you want to remove the budget cost element from and manually make the change.</span></span>

## <a name="why-cant-i-enter-an-annual-amount-on-the-cost-calculation-fasttab-for-the-budget-cost-element"></a><span data-ttu-id="d319d-121">เหตุใดฉันจึงไม่สามารถป้อนยอดเงินประจำปีใน FastTab การคำนวณต้นทุนสำหรับองค์ประกอบต้นทุนงบประมาณได้</span><span class="sxs-lookup"><span data-stu-id="d319d-121">Why can’t I enter an annual amount on the Cost calculation FastTab for the budget cost element?</span></span>
<span data-ttu-id="d319d-122">คุณไม่สามารถป้อนยอดเงินประจำปีถ้ามีองค์ประกอบต้นทุนงบประมาณใน FastTab **ฐานการคำนวณ** เนื่องจากระบบต้องการเปอร์เซ็นต์ เพื่อคำนวณมูลค่า</span><span class="sxs-lookup"><span data-stu-id="d319d-122">You can’t enter an annual amount if there are budget cost elements on the **Calculation basis** FastTab, because the system requires a percentage in order to calculate the value.</span></span> <span data-ttu-id="d319d-123">เพื่อเปลี่ยนแปลงค่านี้ ลบองค์ประกอบต้นทุนงบประมาณทั้งหมดจาก FastTab **ฐานการคำนวณ**</span><span class="sxs-lookup"><span data-stu-id="d319d-123">To change the value, remove all budget cost elements from the **Calculation basis** FastTab.</span></span>

## <a name="why-cant-i-change-the-budget-cost-type-from-earning-to-another-budget-cost-type"></a><span data-ttu-id="d319d-124">เหตุใดฉันจึงไม่สามารถเปลี่ยนชนิดของต้นทุนงบประมาณจาก รายได้ เป็นชนิดต้นทุนงบประมาณอื่น</span><span class="sxs-lookup"><span data-stu-id="d319d-124">Why can’t I change the budget cost type from earning to another budget cost type?</span></span>
<span data-ttu-id="d319d-125">บางองค์ประกอบต้นทุนงบประมาณใช้องค์ประกอบต้นทุนของรายได้เป็นพื้นฐานการคำนวณ </span><span class="sxs-lookup"><span data-stu-id="d319d-125">Some budget cost elements use the earning cost element as a calculation basis.</span></span> <span data-ttu-id="d319d-126">เมื่อต้องการเปลี่ยนแปลงฟิลด์ **ชนิดต้นทุนงบประมาณ** ลบองค์ประกอบต้นทุนรายได้ออกจาก FastTab **ฐานการคำนวณ** ขององค์ประกอบต้นทุนงบประมาณทั้งหมด</span><span class="sxs-lookup"><span data-stu-id="d319d-126">To change the **Budget cost type** field, remove the earning cost element from the **Calculation basis** FastTab of all budget cost elements.</span></span>

## <a name="why-cant-i-change-the-date-on-budget-cost-element-lines-for-a-budget-cost-element"></a><span data-ttu-id="d319d-127">เพราะไม่สามารถเปลี่ยนวันที่ในรายการองค์ประกอบต้นทุนงบประมาณสำหรับองค์ประกอบต้นทุนงบประมาณ</span><span class="sxs-lookup"><span data-stu-id="d319d-127">Why can’t I change the date on budget cost element lines for a budget cost element?</span></span>
<span data-ttu-id="d319d-128">คุณไม่สามารถเปลี่ยนวันที่ในรายการองค์ประกอบต้นทุนงบประมาณได้ เมื่อองค์ประกอบต้นทุนงบประมาณถูกใช้โดยตำแหน่งตามการคาดการณ์ </span><span class="sxs-lookup"><span data-stu-id="d319d-128">You can’t change the date on the budget cost element line when a budget cost element is used by a forecast position.</span></span> <span data-ttu-id="d319d-129">การจำกัดนี้ช่วยรับรองว่าตำแหน่งตามการคาดการณ์อยู่ภายในคำแนะนำขององค์ประกอบต้นทุนงบประมาณเสมอ </span><span class="sxs-lookup"><span data-stu-id="d319d-129">This limitation helps guarantee that the forecast positions are always within the guidelines of the budget cost element.</span></span> <span data-ttu-id="d319d-130">เมื่อต้องการเปลี่ยนวันที่ บน FastTab **การคำนวณต้นทุน** คลิก **เปลี่ยนวันที่** และป้อนวันที่ใหม่</span><span class="sxs-lookup"><span data-stu-id="d319d-130">To change the date, on the **Cost calculation** FastTab, click **Change dates**, and enter the new dates.</span></span> <span data-ttu-id="d319d-131">แล้วคลิก **ตกลง** เพื่ออัพเดตตำแหน่งที่มีกำหนดองค์ประกอบต้นทุน</span><span class="sxs-lookup"><span data-stu-id="d319d-131">Then click **OK** to update the positions that the cost element is assigned to.</span></span>

## <a name="why-cant-i-change-the-costs-for-a-budget-cost-element-on-the-compensation-group-page"></a><span data-ttu-id="d319d-132">เหตุใดฉันจึงไม่สามารถเปลี่ยนต้นทุนสำหรับองค์ประกอบต้นทุนงบประมาณบนหน้ากลุ่มค่าตอบแทนได้</span><span class="sxs-lookup"><span data-stu-id="d319d-132">Why can’t I change the costs for a budget cost element on the Compensation group page?</span></span>
<span data-ttu-id="d319d-133">คุณสามารถสร้างและเปลี่ยนแปลงองค์ประกอบต้นทุนงบประมาณเท่านั้น ในหน้า **องค์ประกอบต้นทุนงบประมาณ** ได้</span><span class="sxs-lookup"><span data-stu-id="d319d-133">You can create and change budget cost elements only on the **Budget cost elements** page.</span></span>

## <a name="why-do-i-receive-an-error-message-when-i-change-the-dates-for-a-cost-element-on-a-forecast-position"></a><span data-ttu-id="d319d-134">เหตุใดฉันจึงได้รับข้อความแสดงข้อผิดพลาด เมื่อฉันเปลี่ยนแปลงวันที่สำหรับองค์ประกอบต้นทุนในตำแหน่งตามการคาดการณ์</span><span class="sxs-lookup"><span data-stu-id="d319d-134">Why do I receive an error message when I change the dates for a cost element on a forecast position?</span></span>
<span data-ttu-id="d319d-135">วันที่บนรายการองค์ประกอบต้นทุนของตำแหน่งการคาดการณ์ต้องอยู่ภายในช่วงต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="d319d-135">The dates on the forecast position cost element line must be within the following ranges:</span></span>

-   <span data-ttu-id="d319d-136">วันเปิดใช้งานและพ้นจากตำแหน่ง</span><span class="sxs-lookup"><span data-stu-id="d319d-136">The activation and retirement dates of the position.</span></span>
-   <span data-ttu-id="d319d-137">วันเปิดใช้งานและหมดอายุขององค์ประกอบต้นทุนงบประมาณ</span><span class="sxs-lookup"><span data-stu-id="d319d-137">The activation and expiration dates of the budget cost element.</span></span>
-   <span data-ttu-id="d319d-138">วันที่เริ่มต้นและสิ้นสุดของวงจรงบประมาณ ที่เชื่อมโยงกับกระบวนการการวางแผนงบประมาณของตำแหน่งตามการคาดการณ์</span><span class="sxs-lookup"><span data-stu-id="d319d-138">The start and end dates of the budget cycle that is associated with the budget planning process of the forecast position.</span></span>




