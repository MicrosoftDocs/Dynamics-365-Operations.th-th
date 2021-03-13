---
title: การลงทะเบียนพนักงานในแผนค่าตอบแทนคงที่
description: 'ผู้จัดการฝ่ายค่าตอบแทนและสวัสดิการสามารถกำหนดพนักงานไปยังแผนค่าตอบแทนคงที่เพื่อจัดการค่าจ้างพื้นฐานของพวกเขา '
author: andreabichsel
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: HRMCompFixedEmpl, HRMCompFixedEmplActionDialog, HcmPositionLookup, HRMCompRefPointLookup, HcmCompensationWorkspace
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: bc8373a4a39a1a212ab445b2b300fbddfe0e4a39
ms.sourcegitcommit: ea2d652867b9b83ce6e5e8d6a97d2f9460a84c52
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 02/03/2021
ms.locfileid: "5114455"
---
# <a name="enroll-an-employee-in-a-fixed-compensation-plan"></a><span data-ttu-id="57c5c-103">การลงทะเบียนพนักงานในแผนค่าตอบแทนคงที่</span><span class="sxs-lookup"><span data-stu-id="57c5c-103">Enroll an employee in a fixed compensation plan</span></span>

<span data-ttu-id="57c5c-104">ผู้จัดการฝ่ายค่าตอบแทนและสวัสดิการสามารถกำหนดพนักงานไปยังแผนค่าตอบแทนคงที่เพื่อจัดการค่าจ้างพื้นฐานของพวกเขา </span><span class="sxs-lookup"><span data-stu-id="57c5c-104">The compensation and benefits manager can assign employees to fixed compensation plans to manage their base pay.</span></span> <span data-ttu-id="57c5c-105">ขั้นตอนนี้ถือว่าแผนถาวรถูกสร้างขึ้นแล้วและกำลังเปิดใช้งานอยู่ และถือว่าได้ตั้งกฎการมีสิทธิ์สำหรับแผนไว้แล้ว </span><span class="sxs-lookup"><span data-stu-id="57c5c-105">This procedure assumes that a fixed plan has been created and is active, and that eligibility rules have been set for the plan.</span></span> <span data-ttu-id="57c5c-106">ข้อมูลบริษัทสาธิตที่ใช้ในการสร้างกระบวนงานนี้คือ USMF</span><span class="sxs-lookup"><span data-stu-id="57c5c-106">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="57c5c-107">หากจะเริ่มต้นกระบวนการ ให้ไปที่ ทรัพยากรบุคคล > ผู้ปฏิบัติงาน > พนักงาน > ค่าตอบแทน > แผนคงที่</span><span class="sxs-lookup"><span data-stu-id="57c5c-107">To begin the procedure, go to Human resources > Workers > Employees > Compensation > Fixed plan</span></span>

1. <span data-ttu-id="57c5c-108">คลิก สร้าง</span><span class="sxs-lookup"><span data-stu-id="57c5c-108">Click New.</span></span>
2. <span data-ttu-id="57c5c-109">ในฟิลด์การดำเนินการ เลือกการดำเนินการค่าตอบแทนคงที่ของชนิดการจ้างงาน/จ้างงานใหม่เพื่ออธิบายการเปลี่ยนแปลงในค่าตอบแทนของพนักงาน</span><span class="sxs-lookup"><span data-stu-id="57c5c-109">In the Action field, select a Fixed compensation action of type Hire/Rehire to describe the change in the employee's compensation.</span></span>
3. <span data-ttu-id="57c5c-110">ในรายการนี้ ให้คลิกลิงค์ในแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="57c5c-110">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="57c5c-111">ในฟิลด์ตำแหน่ง ให้คลิกปุ่มดรอปดาวน์เพื่อเปิดการค้นหา</span><span class="sxs-lookup"><span data-stu-id="57c5c-111">In the Position field, click the drop-down button to open the lookup.</span></span>
5. <span data-ttu-id="57c5c-112">ในรายการนี้ ให้คลิกลิงค์ในแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="57c5c-112">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="57c5c-113">ระดับที่ถูกแสดงนั้นมาจากระดับค่าตอบแทนของงานในตำแหน่งนั้น </span><span class="sxs-lookup"><span data-stu-id="57c5c-113">The level that's displayed is from the Compensation Level of the Job on the Position.</span></span> <span data-ttu-id="57c5c-114">ระดับต้องถูกตั้งค่าบนงานก่อนที่คุณจะสามารถกำหนดค่าตอบแทนให้กับพนักงาน</span><span class="sxs-lookup"><span data-stu-id="57c5c-114">The level must be set on the Job before compensation can be assigned to the employee.</span></span>  
6. <span data-ttu-id="57c5c-115">ในฟิลด์แผน เลือกแผนค่าตอบแทนคงที่สำหรับพนักงาน </span><span class="sxs-lookup"><span data-stu-id="57c5c-115">In the Plan field, select the fixed compensation plan for the employee.</span></span> <span data-ttu-id="57c5c-116">การค้นหาแผนจะถูกกรองเพื่อแสดงเฉพาะแผนที่พนักงานมีสิทธิตามกฎการมีสิทธิ์</span><span class="sxs-lookup"><span data-stu-id="57c5c-116">The Plan lookup is filtered to show only the plans that the employee is eligible for based on the Eligibility rules.</span></span>
7. <span data-ttu-id="57c5c-117">ในรายการนี้ ให้ค้นหาและเลือกเรกคอร์ดที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="57c5c-117">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="57c5c-118">วันหมดอายุและวันที่มีผลบังคับใช้สำหรับค่าตอบแทนจะตั้งต้นจากวันเริ่มต้นและวันสิ้นสุดสำหรับการมอบหมายตำแหน่งงานของผู้ปฏิบัติงาน </span><span class="sxs-lookup"><span data-stu-id="57c5c-118">The Effective and Expiration dates for the compensation default from the start and end dates for the worker's position assignment.</span></span> <span data-ttu-id="57c5c-119">คุณสามารถปรับเปลี่ยนวันเหล่านี้ตามความจำเป็น</span><span class="sxs-lookup"><span data-stu-id="57c5c-119">You can adjust these dates as needed.</span></span>  
    * <span data-ttu-id="57c5c-120">ถ้าแผนค่าตอบแทนคงที่เป็นแผนขั้นตอน เลือกขั้นตอนที่ประกอบด้วยอัตราค่าจ้างที่ถูกต้องสำหรับพนักงาน </span><span class="sxs-lookup"><span data-stu-id="57c5c-120">If the Fixed compensation plan is a step plan, select the step containing the correct pay rate for the employee.</span></span> <span data-ttu-id="57c5c-121">ถ้าแผนค่าตอบแทนคงที่เป็นแผนระดับหรือแถบ ให้ป้อนอัตราค่าจ้างสำหรับพนักงาน </span><span class="sxs-lookup"><span data-stu-id="57c5c-121">If the fixed compensation plan is a grade or a band plan, enter the pay rate for the employee.</span></span> <span data-ttu-id="57c5c-122">อัตราค่าจ้างจะถูกตรวจสอบโดยเทียบกับการตั้งค่าค่าเผื่อสำหรับแผน และจุดอ้างอิงค่าต่ำสุดและสูงสุดสำหรับระดับค่าตอบแทนของงาน</span><span class="sxs-lookup"><span data-stu-id="57c5c-122">The pay rate will be validated against the tolerance settings for the plan, and the minimum and maximum reference points for the job's compensation level.</span></span>  
8. <span data-ttu-id="57c5c-123">คลิก ตกลง</span><span class="sxs-lookup"><span data-stu-id="57c5c-123">Click OK.</span></span>

