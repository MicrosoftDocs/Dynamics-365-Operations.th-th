---
title: กำหนดค่าการหักลด
description: ''
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
ms.openlocfilehash: 7ee9e8f3bc0e9027e41d3aa91bd097a3f046cbb4
ms.sourcegitcommit: 40163705a134c9874fd33be80c7ae59ccce22c21
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 02/03/2020
ms.locfileid: "3010752"
---
# <a name="configure-deductions"></a><span data-ttu-id="3a2af-102">กำหนดค่าการหักลด</span><span class="sxs-lookup"><span data-stu-id="3a2af-102">Configure deductions</span></span>

[!include [banner](includes/preview-feature.md)]

<span data-ttu-id="3a2af-103">ใช้การหักลดใน Microsoft Dynamics 365 Human Resources เพื่อกำหนดจำนวนเงิน ถ้ามี เพื่อหักจากเงินเดือนของพนักงานสำหรับแต่ละสิทธิประโยชน์</span><span class="sxs-lookup"><span data-stu-id="3a2af-103">Use deductions in Microsoft Dynamics 365 Human Resources to determine how much, if any, to deduct from an employee’s paycheck for each benefit.</span></span> <span data-ttu-id="3a2af-104">การหักลดจะมีผลในวันที่บังคับใช้ ดังนั้นคุณจึงสามารถจัดเก็บบันทึกประวัติของข้อมูลการหักลดได้</span><span class="sxs-lookup"><span data-stu-id="3a2af-104">Deductions are date effective, so you can keep a historical record of deduction information.</span></span> 

1. <span data-ttu-id="3a2af-105">ในพื้นที่ทำงาน **การจัดการสิทธิประโยชน์** ภายใต้ **การตั้งค่า** ให้เลือก **การหักลด**</span><span class="sxs-lookup"><span data-stu-id="3a2af-105">In the **Benefits management** workspace, under **Setup**, select **Deductions**.</span></span>

2. <span data-ttu-id="3a2af-106">เลือก **ใหม่**</span><span class="sxs-lookup"><span data-stu-id="3a2af-106">Select **New**.</span></span>

3. <span data-ttu-id="3a2af-107">ระบุค่าสำหรับฟิลด์ต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="3a2af-107">Specify values for the following fields:</span></span>

   | <span data-ttu-id="3a2af-108">ฟิลด์</span><span class="sxs-lookup"><span data-stu-id="3a2af-108">Field</span></span> | <span data-ttu-id="3a2af-109">คำอธิบาย</span><span class="sxs-lookup"><span data-stu-id="3a2af-109">Description</span></span> |
   | --- | --- |
   | <span data-ttu-id="3a2af-110">การหักลด</span><span class="sxs-lookup"><span data-stu-id="3a2af-110">Deduction</span></span> | <span data-ttu-id="3a2af-111">รหัสเฉพาะที่ใช้ในการระบุการหักลดสิทธิประโยชน์</span><span class="sxs-lookup"><span data-stu-id="3a2af-111">A unique ID that is used to identify the benefit deduction.</span></span> |
   | <span data-ttu-id="3a2af-112">คำอธิบาย</span><span class="sxs-lookup"><span data-stu-id="3a2af-112">Description</span></span> | <span data-ttu-id="3a2af-113">คำอธิบายสำหรับการหักลด</span><span class="sxs-lookup"><span data-stu-id="3a2af-113">A description for the deduction.</span></span> |
   | <span data-ttu-id="3a2af-114">มีผลบังคับใช้</span><span class="sxs-lookup"><span data-stu-id="3a2af-114">Effective</span></span> | <span data-ttu-id="3a2af-115">วันที่เริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="3a2af-115">The start date.</span></span> <span data-ttu-id="3a2af-116">ค่าเริ่มต้นคือวันที่ปัจจุบันของระบบ</span><span class="sxs-lookup"><span data-stu-id="3a2af-116">The default value is the current system date.</span></span> |
   | <span data-ttu-id="3a2af-117">การหมดอายุ</span><span class="sxs-lookup"><span data-stu-id="3a2af-117">Expiration</span></span> | <span data-ttu-id="3a2af-118">วันที่สิ้นสุด</span><span class="sxs-lookup"><span data-stu-id="3a2af-118">The end date.</span></span> <span data-ttu-id="3a2af-119">ค่าเริ่มต้นคือ 12/31/2154 ซึ่งไม่เคยระบุ</span><span class="sxs-lookup"><span data-stu-id="3a2af-119">The default value is 12/31/2154, which signifies never.</span></span> |
   | <span data-ttu-id="3a2af-120">หัวเรื่อง</span><span class="sxs-lookup"><span data-stu-id="3a2af-120">Heading</span></span> | <span data-ttu-id="3a2af-121">รหัสหัวข้อจากระบบการจ่ายเงินเดือนที่การหักลดนี้จะใช้สำหรับส่วนของพนักงานของการหักลดเมื่อมีการประมวลผลสิทธิประโยชน์ให้กับค่าจ้าง</span><span class="sxs-lookup"><span data-stu-id="3a2af-121">The heading code from the payroll system that this deduction will use for the employee portion of the deduction when processing the benefits to payroll.</span></span> <span data-ttu-id="3a2af-122">วิธีการนี้จะใช้เมื่อคุณใช้บริการของผู้ให้บริการการจ่ายเงินเดือนที่เป็นบุคคลที่สาม</span><span class="sxs-lookup"><span data-stu-id="3a2af-122">This is used when you use a third party payroll provider.</span></span> |
   | <span data-ttu-id="3a2af-123">การอ้างอิงรายการหักค่าจ้างสำหรับพนักงาน</span><span class="sxs-lookup"><span data-stu-id="3a2af-123">Employee payroll deduction reference</span></span> | <span data-ttu-id="3a2af-124">รหัสรายการหักจากระบบค่าจ้างที่จะใช้รายการหักนี้สำหรับรายการหักในส่วนของพนักงานเมื่อประมวลผลสวัสดิการกับค่าจ้าง</span><span class="sxs-lookup"><span data-stu-id="3a2af-124">The deduction code from the payroll system that this deduction will use for the employee portion of the deduction when processing the benefits to payroll.</span></span> |
   | <span data-ttu-id="3a2af-125">หัวข้อจำนวนเงิน</span><span class="sxs-lookup"><span data-stu-id="3a2af-125">Amount heading</span></span> | <span data-ttu-id="3a2af-126">รหัสหัวข้อจากระบบการจ่ายเงินเดือนที่จำนวนการหักลดนี้จะใช้สำหรับส่วนของพนักงานของการหักลดเมื่อมีการประมวลผลสิทธิประโยชน์ต่อเงินเดือน</span><span class="sxs-lookup"><span data-stu-id="3a2af-126">The heading code from the payroll system that this deduction amount will use for the employee portion of the deduction when processing the benefits to payroll.</span></span> <span data-ttu-id="3a2af-127">โดยปกติจะใช้วิธีการนี้เมื่อคุณใช้บริการผู้ให้บริการการจ่ายเงินเดือนที่เป็นบุคคลที่สาม</span><span class="sxs-lookup"><span data-stu-id="3a2af-127">This is normally used when you use a third party payroll provider.</span></span> |
   | <span data-ttu-id="3a2af-128">สามารถลบได้</span><span class="sxs-lookup"><span data-stu-id="3a2af-128">Can delete</span></span> | <span data-ttu-id="3a2af-129">ระบุว่าค่าที่ส่งออกจาก Dynamics 365 for Finance and Operations จะทำให้ค่าที่อยู่ในระบบการจ่ายเงินเดือนถูกลบออกหรือไม่</span><span class="sxs-lookup"><span data-stu-id="3a2af-129">Specifies whether an exported value from Dynamics 365 for Finance and Operations can cause the value to be deleted in the payroll system.</span></span> |
   | <span data-ttu-id="3a2af-130">คอลัมน์ที่ถูกจับคู่</span><span class="sxs-lookup"><span data-stu-id="3a2af-130">Paired columns</span></span> | <span data-ttu-id="3a2af-131">ระบุว่าจะส่งออกหัวข้อและยอดการหักลดในคอลัมน์คู่ที่อยู่ติดกันกับระบบการจ่ายเงินเดือนหรือไม่</span><span class="sxs-lookup"><span data-stu-id="3a2af-131">Specifies whether to export heading and deduction amount in paired adjacent columns to the payroll system.</span></span> |
   | <span data-ttu-id="3a2af-132">วันที่มีผลของการเปลี่ยนแปลง</span><span class="sxs-lookup"><span data-stu-id="3a2af-132">Change effective date</span></span> | <span data-ttu-id="3a2af-133">วันที่ที่มีการเปลี่ยนแปลงการหักลดจะเริ่มมีผลบังคับใช้</span><span class="sxs-lookup"><span data-stu-id="3a2af-133">The date when the benefit deduction change will become effective.</span></span> <span data-ttu-id="3a2af-134">ในวันที่มีผลบังคับใช้ระบบจะเปลี่ยนการหักเงินสิทธิประโยชน์และอัพเดตแผนผลประโยชน์ทั้งหมดที่เกี่ยวข้องกับการหักลดนี้โดยอัตโนมัติ ตราบใดที่คุณดำเนินการประมวลผลการอัพเดตการหักลด</span><span class="sxs-lookup"><span data-stu-id="3a2af-134">On this date the system will automatically change the benefit deduction and update all benefit plans associated with this deduction, as long as you run Deduction change update processing.</span></span> |
   | <span data-ttu-id="3a2af-135">การเปลี่ยนแปลงรายการหักเสร็จสมบูรณ์แล้ว</span><span class="sxs-lookup"><span data-stu-id="3a2af-135">Deduction change completed</span></span> | <span data-ttu-id="3a2af-136">กล่องกาเครื่องหมายการเปลี่ยนแปลงการหักลดที่เสร็จสมบูรณ์จะถูกเลือกโดยอัตโนมัติเมื่อการเปลี่ยนแปลงการหักเงินสิทธิประโยชน์เสร็จสมบูรณ์แล้วโดยการประมวลผลการอัพเดตความเปลี่ยนแปลงของการหักลด</span><span class="sxs-lookup"><span data-stu-id="3a2af-136">The Deduction change completed check box will be automatically selected once the benefit deduction changes have been completed by Deduction update change processing.</span></span> |
   
4. <span data-ttu-id="3a2af-137">การติดตามและรักษาการเปลี่ยนแปลงการตั้งค่าอัตราสิทธิประโยชน์ ให้เลือก **ดำเนินการ** จากนั้นเลือก **รักษาเวอร์ชัน**</span><span class="sxs-lookup"><span data-stu-id="3a2af-137">To track and maintain changes to the benefit rate setup, select **Actions**, and then select **Maintain versions**.</span></span>

5. <span data-ttu-id="3a2af-138">เลือก **บันทึก**</span><span class="sxs-lookup"><span data-stu-id="3a2af-138">Select **Save**.</span></span> 
