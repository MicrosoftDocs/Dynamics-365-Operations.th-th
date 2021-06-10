---
title: การลงทะเบียนพนักงานในแผนค่าตอบแทนผันแปร
description: 'ผู้จัดการฝ่ายค่าตอบแทนและสวัสดิการสามารถลงทะเบียนพนักงานในแผนค่าตอบแทนผันแปรเพื่อคำนวณรางวัลที่เป็นเงินสดและที่ไม่ใช่เงินสดให้กับพนักงาน '
author: andreabichsel
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: HRMCompVarEnrollEmpl, HcmCompensationWorkspace
audience: Application User
ms.search.scope: Human Resources
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: c2da79af8ab311cb41d62bff0e976ea76d2682e4
ms.sourcegitcommit: 879ee8a10e6158885795dce4b3db5077540eec41
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 05/18/2021
ms.locfileid: "6054199"
---
# <a name="enroll-an-employee-in-a-variable-compensation-plan"></a><span data-ttu-id="f9e5c-103">การลงทะเบียนพนักงานในแผนค่าตอบแทนผันแปร</span><span class="sxs-lookup"><span data-stu-id="f9e5c-103">Enroll an employee in a variable compensation plan</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="f9e5c-104">ผู้จัดการฝ่ายค่าตอบแทนและสวัสดิการสามารถลงทะเบียนพนักงานในแผนค่าตอบแทนผันแปรเพื่อคำนวณรางวัลที่เป็นเงินสดและที่ไม่ใช่เงินสดให้กับพนักงาน </span><span class="sxs-lookup"><span data-stu-id="f9e5c-104">The Compensation and Benefits manager can enroll employees in variable compensation plans to calculate cash and non-cash awards for employees.</span></span> <span data-ttu-id="f9e5c-105">ขั้นตอนนี้จะสมมุติว่า มีการสร้างแผนค่าตอบแทนผันแปรไว้แล้ว พร้อมด้วยฟิลด์ลงทะเบียนที่เปิดใช้ที่ตั้งค่าเป็นใช่ และมีการสร้างกฎการมีสิทธิ์สำหรับแผนค่าตอบแทนผันแปร</span><span class="sxs-lookup"><span data-stu-id="f9e5c-105">This procedure assumes that a variable compensation plan has been created with the Enable enrolment field set to Yes, and that eligibility rules have been created for that variable compensation plan.</span></span> <span data-ttu-id="f9e5c-106">ข้อมูลบริษัทสาธิตที่ใช้ในการสร้างกระบวนงานนี้คือ USMF</span><span class="sxs-lookup"><span data-stu-id="f9e5c-106">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="f9e5c-107">หากจะเริ่มต้นขั้นตอนนี้ ให้ไปที่ทรัพยากรบุคคล > ผู้ปฏิบัติงาน > พนักงาน > ค่าตอบแทน > การลงทะเบียนแผนผันแปร</span><span class="sxs-lookup"><span data-stu-id="f9e5c-107">To begin this procedure, go to Human resources > Workers > Employees > Compensation > Variable plan enrolment</span></span>

1. <span data-ttu-id="f9e5c-108">คลิก สร้าง</span><span class="sxs-lookup"><span data-stu-id="f9e5c-108">Click New.</span></span>
2. <span data-ttu-id="f9e5c-109">ในฟิลด์แผน ให้คลิกที่ปุ่มดรอปดาวน์เพื่อเปิดการค้นหา </span><span class="sxs-lookup"><span data-stu-id="f9e5c-109">In the Plan field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="f9e5c-110">การค้นหาแผนจะถูกกรองเพื่อแสดงเฉพาะแผนค่าตอบแทนผันแปรที่พนักงานมีสิทธิตามกฎการมีสิทธิ์</span><span class="sxs-lookup"><span data-stu-id="f9e5c-110">The plan lookup will be filtered to only show the variable compensation plans that the employee is eligible for based on the eligibility rules.</span></span>  
3. <span data-ttu-id="f9e5c-111">ในรายการนี้ ให้คลิกลิงค์ในแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="f9e5c-111">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="f9e5c-112">เปิดปิดการขยายของส่วนทั่วไป</span><span class="sxs-lookup"><span data-stu-id="f9e5c-112">Toggle the expansion of the General section.</span></span>
5. <span data-ttu-id="f9e5c-113">ในฟิลด์วันที่มีผลบังคับใช้ ให้ป้อนวันที่</span><span class="sxs-lookup"><span data-stu-id="f9e5c-113">In the Effective date field, enter a date.</span></span>
6. <span data-ttu-id="f9e5c-114">คลิก บันทึก</span><span class="sxs-lookup"><span data-stu-id="f9e5c-114">Click Save.</span></span>
7. <span data-ttu-id="f9e5c-115">เปิดปิดการขยายของส่วนแทนที่</span><span class="sxs-lookup"><span data-stu-id="f9e5c-115">Toggle the expansion of the Overrides section.</span></span>
    * <span data-ttu-id="f9e5c-116">อีกทางหนึ่งคือสามารถตั้งวันของกฎการจ้างงานเพื่อแทนที่วันจ้างงานสำหรับพนักงาน เมื่อกฎการจ้างงานที่ระบุไว้สำหรับแผนผันแปรที่ถูกเลือกเป็นเปอร์เซ็นต์</span><span class="sxs-lookup"><span data-stu-id="f9e5c-116">Optionally, a hire rule date can be set to override the hire date for an employee when the hire rule specified for the selected variable plan is Percent.</span></span>  
    * <span data-ttu-id="f9e5c-117">ถ้าแผนผันแปรเป็นเปอร์เซ็นต์ของแผนพื้นฐาน เปอร์เซ็นต์รางวัลสามารถถูกแทนที่สำหรับพนักงาน </span><span class="sxs-lookup"><span data-stu-id="f9e5c-117">If the variable plan is a percent of basis plan, the award percentage can be overridden for the employee.</span></span> <span data-ttu-id="f9e5c-118">ถ้าแผนค่าตอบแทนผันแปรเป็นหมายเลขของแผนหน่วย จำนวนหน่วยสามารถถูกแทนที่สำหรับพนักงาน</span><span class="sxs-lookup"><span data-stu-id="f9e5c-118">If the variable compensation plan is a number of units plan, the number of units can be overridden for the employee.</span></span>  
    * <span data-ttu-id="f9e5c-119">ถ้าพนักงานควรจะได้รับยอดเงินคงที่สำหรับรางวัล ยอดเงินสามารถกำหนดได้ที่นี่</span><span class="sxs-lookup"><span data-stu-id="f9e5c-119">If the employee should be given a flat amount for their award, the amount can be set here.</span></span>  
8. <span data-ttu-id="f9e5c-120">เปิดปิดการขยายของส่วนแทนที่ประจำองค์กร</span><span class="sxs-lookup"><span data-stu-id="f9e5c-120">Toggle the expansion of the Organizational overrides section.</span></span>
    * <span data-ttu-id="f9e5c-121">ถ้าประสิทธิภาพของพนักงานควรนำมาพิจารณา ประสิทธิภาพของแผนกต่างๆ หรือแผนกอื่นนอกเหนือจากที่กำหนดให้กับตำแหน่งงานของพนักงาน แผนกสามารถถูกแทนที่ได้ </span><span class="sxs-lookup"><span data-stu-id="f9e5c-121">If the employee's performance should take into consideration, the performance of different departments, or a department other than the one assigned on the employee's position, the department can be overridden.</span></span> <span data-ttu-id="f9e5c-122">คอลัมน์เปอร์เซ็นต์ควรมีผลรวมเป็น 100</span><span class="sxs-lookup"><span data-stu-id="f9e5c-122">The Percent column should total 100.</span></span>  



[!INCLUDE[footer-include](../includes/footer-banner.md)]