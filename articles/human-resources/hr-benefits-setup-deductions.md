---
title: ตั้งค่าคอนฟิกรายการหัก
description: ใช้การหักลดใน Microsoft Dynamics 365 Human Resources เพื่อกำหนดจำนวนเงิน ถ้ามี เพื่อหักจากเงินเดือนของพนักงานสำหรับแต่ละสิทธิประโยชน์
author: andreabichsel
manager: AnnBe
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: a5287161f352b386ae4e13067f40228d7c1bce62
ms.sourcegitcommit: f38302b9430f2ab3efe91d0a7beff946bc610e8f
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 02/28/2020
ms.locfileid: "3092740"
---
# <a name="configure-deductions"></a><span data-ttu-id="86086-103">ตั้งค่าคอนฟิกรายการหัก</span><span class="sxs-lookup"><span data-stu-id="86086-103">Configure deductions</span></span>

[!include [banner](includes/preview-feature.md)]

<span data-ttu-id="86086-104">ใช้การหักลดใน Microsoft Dynamics 365 Human Resources เพื่อกำหนดจำนวนเงิน ถ้ามี เพื่อหักจากเงินเดือนของพนักงานสำหรับแต่ละสิทธิประโยชน์</span><span class="sxs-lookup"><span data-stu-id="86086-104">Use deductions in Microsoft Dynamics 365 Human Resources to determine how much, if any, to deduct from an employee’s paycheck for each benefit.</span></span> <span data-ttu-id="86086-105">การหักลดจะมีผลในวันที่บังคับใช้ ดังนั้นคุณจึงสามารถจัดเก็บบันทึกประวัติของข้อมูลการหักลดได้</span><span class="sxs-lookup"><span data-stu-id="86086-105">Deductions are date effective, so you can keep a historical record of deduction information.</span></span> 

1. <span data-ttu-id="86086-106">ในพื้นที่ทำงาน **การจัดการสิทธิประโยชน์** ภายใต้ **การตั้งค่า** ให้เลือก **การหักลด**</span><span class="sxs-lookup"><span data-stu-id="86086-106">In the **Benefits management** workspace, under **Setup**, select **Deductions**.</span></span>

2. <span data-ttu-id="86086-107">เลือก **ใหม่**</span><span class="sxs-lookup"><span data-stu-id="86086-107">Select **New**.</span></span>

3. <span data-ttu-id="86086-108">ระบุค่าสำหรับฟิลด์ต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="86086-108">Specify values for the following fields:</span></span>

   | <span data-ttu-id="86086-109">ฟิลด์</span><span class="sxs-lookup"><span data-stu-id="86086-109">Field</span></span> | <span data-ttu-id="86086-110">คำอธิบาย</span><span class="sxs-lookup"><span data-stu-id="86086-110">Description</span></span> |
   | --- | --- |
   | <span data-ttu-id="86086-111">การหักลด</span><span class="sxs-lookup"><span data-stu-id="86086-111">Deduction</span></span> | <span data-ttu-id="86086-112">รหัสเฉพาะที่ใช้ในการระบุการหักลดสิทธิประโยชน์</span><span class="sxs-lookup"><span data-stu-id="86086-112">A unique ID that is used to identify the benefit deduction.</span></span> |
   | <span data-ttu-id="86086-113">คำอธิบาย</span><span class="sxs-lookup"><span data-stu-id="86086-113">Description</span></span> | <span data-ttu-id="86086-114">คำอธิบายสำหรับการหักลด</span><span class="sxs-lookup"><span data-stu-id="86086-114">A description for the deduction.</span></span> |
   | <span data-ttu-id="86086-115">มีผลบังคับใช้</span><span class="sxs-lookup"><span data-stu-id="86086-115">Effective</span></span> | <span data-ttu-id="86086-116">วันที่เริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="86086-116">The start date.</span></span> <span data-ttu-id="86086-117">ค่าเริ่มต้นคือวันที่ปัจจุบันของระบบ</span><span class="sxs-lookup"><span data-stu-id="86086-117">The default value is the current system date.</span></span> |
   | <span data-ttu-id="86086-118">การหมดอายุ</span><span class="sxs-lookup"><span data-stu-id="86086-118">Expiration</span></span> | <span data-ttu-id="86086-119">วันที่สิ้นสุด</span><span class="sxs-lookup"><span data-stu-id="86086-119">The end date.</span></span> <span data-ttu-id="86086-120">ค่าเริ่มต้นคือ 12/31/2154 ซึ่งไม่เคยระบุ</span><span class="sxs-lookup"><span data-stu-id="86086-120">The default value is 12/31/2154, which signifies never.</span></span> |
   | <span data-ttu-id="86086-121">หัวเรื่อง</span><span class="sxs-lookup"><span data-stu-id="86086-121">Heading</span></span> | <span data-ttu-id="86086-122">รหัสหัวข้อจากระบบการจ่ายเงินเดือนที่การหักลดนี้จะใช้สำหรับส่วนของพนักงานของการหักลดเมื่อมีการประมวลผลสิทธิประโยชน์ให้กับค่าจ้าง</span><span class="sxs-lookup"><span data-stu-id="86086-122">The heading code from the payroll system that this deduction will use for the employee portion of the deduction when processing the benefits to payroll.</span></span> <span data-ttu-id="86086-123">วิธีการนี้จะใช้เมื่อคุณใช้บริการของผู้ให้บริการการจ่ายเงินเดือนที่เป็นบุคคลที่สาม</span><span class="sxs-lookup"><span data-stu-id="86086-123">This is used when you use a third party payroll provider.</span></span> |
   | <span data-ttu-id="86086-124">การอ้างอิงรายการหักค่าจ้างสำหรับพนักงาน</span><span class="sxs-lookup"><span data-stu-id="86086-124">Employee payroll deduction reference</span></span> | <span data-ttu-id="86086-125">รหัสรายการหักจากระบบค่าจ้างที่จะใช้รายการหักนี้สำหรับรายการหักในส่วนของพนักงานเมื่อประมวลผลสวัสดิการกับค่าจ้าง</span><span class="sxs-lookup"><span data-stu-id="86086-125">The deduction code from the payroll system that this deduction will use for the employee portion of the deduction when processing the benefits to payroll.</span></span> |
   | <span data-ttu-id="86086-126">หัวข้อจำนวนเงิน</span><span class="sxs-lookup"><span data-stu-id="86086-126">Amount heading</span></span> | <span data-ttu-id="86086-127">รหัสหัวข้อจากระบบการจ่ายเงินเดือนที่จำนวนการหักลดนี้จะใช้สำหรับส่วนของพนักงานของการหักลดเมื่อมีการประมวลผลสิทธิประโยชน์ต่อเงินเดือน</span><span class="sxs-lookup"><span data-stu-id="86086-127">The heading code from the payroll system that this deduction amount will use for the employee portion of the deduction when processing the benefits to payroll.</span></span> <span data-ttu-id="86086-128">โดยปกติจะใช้วิธีการนี้เมื่อคุณใช้บริการผู้ให้บริการการจ่ายเงินเดือนที่เป็นบุคคลที่สาม</span><span class="sxs-lookup"><span data-stu-id="86086-128">This is normally used when you use a third party payroll provider.</span></span> |
   | <span data-ttu-id="86086-129">สามารถลบได้</span><span class="sxs-lookup"><span data-stu-id="86086-129">Can delete</span></span> | <span data-ttu-id="86086-130">ระบุว่าค่าที่ส่งออกจาก Dynamics 365 for Finance and Operations จะทำให้ค่าที่อยู่ในระบบการจ่ายเงินเดือนถูกลบออกหรือไม่</span><span class="sxs-lookup"><span data-stu-id="86086-130">Specifies whether an exported value from Dynamics 365 for Finance and Operations can cause the value to be deleted in the payroll system.</span></span> |
   | <span data-ttu-id="86086-131">คอลัมน์ที่ถูกจับคู่</span><span class="sxs-lookup"><span data-stu-id="86086-131">Paired columns</span></span> | <span data-ttu-id="86086-132">ระบุว่าจะส่งออกหัวข้อและยอดการหักลดในคอลัมน์คู่ที่อยู่ติดกันกับระบบการจ่ายเงินเดือนหรือไม่</span><span class="sxs-lookup"><span data-stu-id="86086-132">Specifies whether to export heading and deduction amount in paired adjacent columns to the payroll system.</span></span> |
   | <span data-ttu-id="86086-133">วันที่มีผลของการเปลี่ยนแปลง</span><span class="sxs-lookup"><span data-stu-id="86086-133">Change effective date</span></span> | <span data-ttu-id="86086-134">วันที่ที่มีการเปลี่ยนแปลงการหักลดจะเริ่มมีผลบังคับใช้</span><span class="sxs-lookup"><span data-stu-id="86086-134">The date when the benefit deduction change will become effective.</span></span> <span data-ttu-id="86086-135">ในวันที่มีผลบังคับใช้ระบบจะเปลี่ยนการหักเงินสิทธิประโยชน์และอัพเดตแผนผลประโยชน์ทั้งหมดที่เกี่ยวข้องกับการหักลดนี้โดยอัตโนมัติ ตราบใดที่คุณดำเนินการประมวลผลการอัพเดตการหักลด</span><span class="sxs-lookup"><span data-stu-id="86086-135">On this date the system will automatically change the benefit deduction and update all benefit plans associated with this deduction, as long as you run Deduction change update processing.</span></span> |
   | <span data-ttu-id="86086-136">การเปลี่ยนแปลงรายการหักเสร็จสมบูรณ์แล้ว</span><span class="sxs-lookup"><span data-stu-id="86086-136">Deduction change completed</span></span> | <span data-ttu-id="86086-137">กล่องกาเครื่องหมายการเปลี่ยนแปลงการหักลดที่เสร็จสมบูรณ์จะถูกเลือกโดยอัตโนมัติเมื่อการเปลี่ยนแปลงการหักเงินสิทธิประโยชน์เสร็จสมบูรณ์แล้วโดยการประมวลผลการอัพเดตความเปลี่ยนแปลงของการหักลด</span><span class="sxs-lookup"><span data-stu-id="86086-137">The Deduction change completed check box will be automatically selected once the benefit deduction changes have been completed by Deduction update change processing.</span></span> |
   
4. <span data-ttu-id="86086-138">การติดตามและรักษาการเปลี่ยนแปลงการตั้งค่าอัตราสิทธิประโยชน์ ให้เลือก **ดำเนินการ** จากนั้นเลือก **รักษาเวอร์ชัน**</span><span class="sxs-lookup"><span data-stu-id="86086-138">To track and maintain changes to the benefit rate setup, select **Actions**, and then select **Maintain versions**.</span></span>

5. <span data-ttu-id="86086-139">เลือก **บันทึก**</span><span class="sxs-lookup"><span data-stu-id="86086-139">Select **Save**.</span></span> 
