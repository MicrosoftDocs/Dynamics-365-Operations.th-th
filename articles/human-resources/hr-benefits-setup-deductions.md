---
title: ตั้งค่าคอนฟิกรายการหัก
description: ใช้การหักลดใน Microsoft Dynamics 365 Human Resources เพื่อกำหนดจำนวนเงิน ถ้ามี เพื่อหักจากเงินเดือนของพนักงานสำหรับแต่ละสิทธิประโยชน์
author: andreabichsel
ms.date: 04/06/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: BenefitWorkspace, HcmBenefitSummaryPart
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 4a916ca2d0d47407ff0d8cc2cc7ca179ecb59bae
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 03/31/2021
ms.locfileid: "5803668"
---
# <a name="configure-deductions"></a><span data-ttu-id="e1785-103">ตั้งค่าคอนฟิกรายการหัก</span><span class="sxs-lookup"><span data-stu-id="e1785-103">Configure deductions</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="e1785-104">ใช้การหักลดใน Microsoft Dynamics 365 Human Resources เพื่อกำหนดจำนวนเงิน ถ้ามี เพื่อหักจากเงินเดือนของพนักงานสำหรับแต่ละสิทธิประโยชน์</span><span class="sxs-lookup"><span data-stu-id="e1785-104">Use deductions in Microsoft Dynamics 365 Human Resources to determine how much, if any, to deduct from an employee’s paycheck for each benefit.</span></span> <span data-ttu-id="e1785-105">การหักลดจะมีผลในวันที่บังคับใช้ ดังนั้นคุณจึงสามารถจัดเก็บบันทึกประวัติของข้อมูลการหักลดได้</span><span class="sxs-lookup"><span data-stu-id="e1785-105">Deductions are date-effective, so you can keep a historical record of deduction information.</span></span> 

1. <span data-ttu-id="e1785-106">ในพื้นที่ทำงาน **การจัดการสิทธิประโยชน์** ภายใต้ **การตั้งค่า** ให้เลือก **การหักลด**</span><span class="sxs-lookup"><span data-stu-id="e1785-106">In the **Benefits management** workspace, under **Setup**, select **Deductions**.</span></span>

2. <span data-ttu-id="e1785-107">เลือก **ใหม่**</span><span class="sxs-lookup"><span data-stu-id="e1785-107">Select **New**.</span></span>

3. <span data-ttu-id="e1785-108">ระบุค่าสำหรับฟิลด์ต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="e1785-108">Specify values for the following fields:</span></span>

   | <span data-ttu-id="e1785-109">ฟิลด์</span><span class="sxs-lookup"><span data-stu-id="e1785-109">Field</span></span> | <span data-ttu-id="e1785-110">คำอธิบาย</span><span class="sxs-lookup"><span data-stu-id="e1785-110">Description</span></span> |
   | --- | --- |
   | <span data-ttu-id="e1785-111">**การหักลด**</span><span class="sxs-lookup"><span data-stu-id="e1785-111">**Deduction**</span></span> | <span data-ttu-id="e1785-112">รหัสเฉพาะที่ใช้ในการระบุการหักลดสิทธิประโยชน์</span><span class="sxs-lookup"><span data-stu-id="e1785-112">A unique ID that is used to identify the benefit deduction.</span></span> |
   | <span data-ttu-id="e1785-113">**คำอธิบาย**</span><span class="sxs-lookup"><span data-stu-id="e1785-113">**Description**</span></span> | <span data-ttu-id="e1785-114">คำอธิบายสำหรับการหักลด</span><span class="sxs-lookup"><span data-stu-id="e1785-114">A description for the deduction.</span></span> |
   | <span data-ttu-id="e1785-115">**มีผลบังคับใช้**</span><span class="sxs-lookup"><span data-stu-id="e1785-115">**Effective**</span></span> | <span data-ttu-id="e1785-116">วันที่เริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="e1785-116">The start date.</span></span> <span data-ttu-id="e1785-117">ค่าเริ่มต้นคือวันที่ปัจจุบันของระบบ</span><span class="sxs-lookup"><span data-stu-id="e1785-117">The default value is the current system date.</span></span> |
   | <span data-ttu-id="e1785-118">**การหมดอายุ**</span><span class="sxs-lookup"><span data-stu-id="e1785-118">**Expiration**</span></span> | <span data-ttu-id="e1785-119">วันที่สิ้นสุด</span><span class="sxs-lookup"><span data-stu-id="e1785-119">The end date.</span></span> <span data-ttu-id="e1785-120">ค่าเริ่มต้นคือ 12/31/2154 ซึ่งไม่เคยระบุ</span><span class="sxs-lookup"><span data-stu-id="e1785-120">The default value is 12/31/2154, which signifies never.</span></span> |
   | <span data-ttu-id="e1785-121">**หัวเรื่อง**</span><span class="sxs-lookup"><span data-stu-id="e1785-121">**Heading**</span></span> | <span data-ttu-id="e1785-122">รหัสหัวข้อจากระบบการจ่ายเงินเดือนที่การหักลดนี้จะใช้สำหรับส่วนของพนักงานของการหักลดเมื่อมีการประมวลผลสิทธิประโยชน์ให้กับค่าจ้าง</span><span class="sxs-lookup"><span data-stu-id="e1785-122">The heading code from the payroll system that this deduction will use for the employee portion of the deduction when processing the benefits to payroll.</span></span> <span data-ttu-id="e1785-123">วิธีการนี้จะใช้เมื่อคุณใช้บริการของผู้ให้บริการการจ่ายเงินเดือนที่เป็นบุคคลที่สาม</span><span class="sxs-lookup"><span data-stu-id="e1785-123">This is used when you use a third-party payroll provider.</span></span> |
   | <span data-ttu-id="e1785-124">**การอ้างอิงรายการหักค่าจ้างสำหรับพนักงาน**</span><span class="sxs-lookup"><span data-stu-id="e1785-124">**Employee payroll deduction reference**</span></span> | <span data-ttu-id="e1785-125">รหัสรายการหักจากระบบค่าจ้างที่จะใช้รายการหักนี้สำหรับรายการหักในส่วนของพนักงานเมื่อประมวลผลสวัสดิการกับค่าจ้าง</span><span class="sxs-lookup"><span data-stu-id="e1785-125">The deduction code from the payroll system that this deduction will use for the employee portion of the deduction when processing the benefits to payroll.</span></span> |
   | <span data-ttu-id="e1785-126">**หัวข้อจำนวนเงิน**</span><span class="sxs-lookup"><span data-stu-id="e1785-126">**Amount heading**</span></span> | <span data-ttu-id="e1785-127">รหัสหัวข้อจากระบบการจ่ายเงินเดือนที่จำนวนการหักลดนี้จะใช้สำหรับส่วนของพนักงานของการหักลดเมื่อมีการประมวลผลสิทธิประโยชน์ต่อเงินเดือน</span><span class="sxs-lookup"><span data-stu-id="e1785-127">The heading code from the payroll system that this deduction amount will use for the employee portion of the deduction when processing the benefits to payroll.</span></span> <span data-ttu-id="e1785-128">โดยปกติจะใช้วิธีการนี้เมื่อคุณใช้บริการผู้ให้บริการการจ่ายเงินเดือนที่เป็นบุคคลที่สาม</span><span class="sxs-lookup"><span data-stu-id="e1785-128">This is normally used when you use a third-party payroll provider.</span></span> |
   | <span data-ttu-id="e1785-129">**สามารถลบได้**</span><span class="sxs-lookup"><span data-stu-id="e1785-129">**Can delete**</span></span> | <span data-ttu-id="e1785-130">ระบุว่าค่าที่ส่งออกจาก Dynamics 365 for Finance and Operations จะทำให้ค่าที่อยู่ในระบบการจ่ายเงินเดือนถูกลบออกหรือไม่</span><span class="sxs-lookup"><span data-stu-id="e1785-130">Specifies whether an exported value from Dynamics 365 for Finance and Operations can cause the value to be deleted in the payroll system.</span></span> |
   | <span data-ttu-id="e1785-131">**คอลัมน์ที่ถูกจับคู่**</span><span class="sxs-lookup"><span data-stu-id="e1785-131">**Paired columns**</span></span> | <span data-ttu-id="e1785-132">ระบุว่าจะส่งออกหัวข้อและยอดการหักลดในคอลัมน์คู่ที่อยู่ติดกันกับระบบการจ่ายเงินเดือนหรือไม่</span><span class="sxs-lookup"><span data-stu-id="e1785-132">Specifies whether to export heading and deduction amount in paired adjacent columns to the payroll system.</span></span> |
   | <span data-ttu-id="e1785-133">**วันที่มีผลของการเปลี่ยนแปลง**</span><span class="sxs-lookup"><span data-stu-id="e1785-133">**Change effective date**</span></span> | <span data-ttu-id="e1785-134">วันที่ที่มีการเปลี่ยนแปลงการหักลดจะเริ่มมีผลบังคับใช้</span><span class="sxs-lookup"><span data-stu-id="e1785-134">The date when the benefit deduction change will become effective.</span></span> <span data-ttu-id="e1785-135">ในวันที่มีผลบังคับใช้ ระบบจะเปลี่ยนการหักเงินสิทธิประโยชน์และอัพเดตแผนสวัสดิการทั้งหมดที่เกี่ยวข้องกับการหักลดนี้โดยอัตโนมัติ ตราบใดที่คุณดำเนินการประมวลผล **การอัพเดตการหักลด**</span><span class="sxs-lookup"><span data-stu-id="e1785-135">On this date, the system automatically changes the benefit deduction and updates all benefit plans associated with this deduction, as long as you run **Deduction change update** processing.</span></span> |
   | <span data-ttu-id="e1785-136">**การเปลี่ยนแปลงรายการหักเสร็จสมบูรณ์แล้ว**</span><span class="sxs-lookup"><span data-stu-id="e1785-136">**Deduction change completed**</span></span> | <span data-ttu-id="e1785-137">กล่องกาเครื่องหมาย **การเปลี่ยนแปลงการหักลดที่เสร็จสมบูรณ์** จะถูกเลือกโดยอัตโนมัติเมื่อการเปลี่ยนแปลงการหักเงินสิทธิประโยชน์เสร็จสมบูรณ์แล้วโดยการประมวลผลการอัพเดตความเปลี่ยนแปลงของการหักลด</span><span class="sxs-lookup"><span data-stu-id="e1785-137">The **Deduction change completed** check box will be automatically selected once the benefit deduction changes have been completed by Deduction update change processing.</span></span> |
   
4. <span data-ttu-id="e1785-138">การติดตามและรักษาการเปลี่ยนแปลงการตั้งค่าอัตราสิทธิประโยชน์ ให้เลือก **ดำเนินการ** จากนั้นเลือก **รักษาเวอร์ชัน**</span><span class="sxs-lookup"><span data-stu-id="e1785-138">To track and maintain changes to the benefit rate setup, select **Actions**, and then select **Maintain versions**.</span></span>

5. <span data-ttu-id="e1785-139">เลือก **บันทึก**</span><span class="sxs-lookup"><span data-stu-id="e1785-139">Select **Save**.</span></span> 


[!INCLUDE[footer-include](../includes/footer-banner.md)]