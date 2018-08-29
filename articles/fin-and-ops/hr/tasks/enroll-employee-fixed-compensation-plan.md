--- 
title: "การลงทะเบียนพนักงานในแผนค่าตอบแทนคงที่"
description: "ผู้จัดการฝ่ายค่าตอบแทนและสวัสดิการสามารถกำหนดพนักงานไปยังแผนค่าตอบแทนคงที่เพื่อจัดการค่าจ้างพื้นฐานของพวกเขา "
author: kherr75
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-365-talent
ms.technology: 
audience: Application User
ms.reviewer: rschloma
ms.search.scope: Operations, Talent
ms.search.region: Global
ms.author: kherr
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 764d4c9049d94ebcd55c61654aa2f4133b35bae6
ms.openlocfilehash: d84567f0d74b2ab0078eaeda622768e241332043
ms.contentlocale: th-th
ms.lasthandoff: 08/09/2018

---
# <a name="enroll-employees-in-a-fixed-compensation-plan"></a><span data-ttu-id="807ba-103">การลงทะเบียนพนักงานในแผนค่าตอบแทนคงที่</span><span class="sxs-lookup"><span data-stu-id="807ba-103">Enroll employees in a fixed compensation plan</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="807ba-104">ผู้จัดการฝ่ายค่าตอบแทนและสวัสดิการสามารถกำหนดพนักงานไปยังแผนค่าตอบแทนคงที่เพื่อจัดการค่าจ้างพื้นฐานของพวกเขา </span><span class="sxs-lookup"><span data-stu-id="807ba-104">The compensation and benefits manager can assign employees to fixed compensation plans to manage their base pay.</span></span> <span data-ttu-id="807ba-105">ขั้นตอนนี้ถือว่าแผนถาวรถูกสร้างขึ้นแล้วและกำลังเปิดใช้งานอยู่ และถือว่าได้ตั้งกฎการมีสิทธิ์สำหรับแผนไว้แล้ว </span><span class="sxs-lookup"><span data-stu-id="807ba-105">This procedure assumes that a fixed plan has been created and is active, and that eligibility rules have been set for the plan.</span></span> <span data-ttu-id="807ba-106">ข้อมูลบริษัทสาธิตที่ใช้ในการสร้างกระบวนงานนี้คือ USMF</span><span class="sxs-lookup"><span data-stu-id="807ba-106">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="807ba-107">หากจะเริ่มต้นกระบวนการ ให้ไปที่ ทรัพยากรบุคคล > ผู้ปฏิบัติงาน > พนักงาน > ค่าตอบแทน > แผนคงที่</span><span class="sxs-lookup"><span data-stu-id="807ba-107">To begin the procedure, go to Human resources > Workers > Employees > Compensation > Fixed plan</span></span>

1. <span data-ttu-id="807ba-108">คลิก สร้าง</span><span class="sxs-lookup"><span data-stu-id="807ba-108">Click New.</span></span>
2. <span data-ttu-id="807ba-109">ในฟิลด์การดำเนินการ เลือกการดำเนินการค่าตอบแทนคงที่ของชนิดการจ้างงาน/จ้างงานใหม่เพื่ออธิบายการเปลี่ยนแปลงในค่าตอบแทนของพนักงาน</span><span class="sxs-lookup"><span data-stu-id="807ba-109">In the Action field, select a Fixed compensation action of type Hire/Rehire to describe the change in the employee's compensation.</span></span>
3. <span data-ttu-id="807ba-110">ในรายการนี้ ให้คลิกลิงค์ในแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="807ba-110">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="807ba-111">ในฟิลด์ตำแหน่ง ให้คลิกปุ่มดรอปดาวน์เพื่อเปิดการค้นหา</span><span class="sxs-lookup"><span data-stu-id="807ba-111">In the Position field, click the drop-down button to open the lookup.</span></span>
5. <span data-ttu-id="807ba-112">ในรายการนี้ ให้คลิกลิงค์ในแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="807ba-112">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="807ba-113">ระดับที่ถูกแสดงนั้นมาจากระดับค่าตอบแทนของงานในตำแหน่งนั้น </span><span class="sxs-lookup"><span data-stu-id="807ba-113">The level that's displayed is from the Compensation Level of the Job on the Position.</span></span> <span data-ttu-id="807ba-114">ระดับต้องถูกตั้งค่าบนงานก่อนที่คุณจะสามารถกำหนดค่าตอบแทนให้กับพนักงาน</span><span class="sxs-lookup"><span data-stu-id="807ba-114">The level must be set on the Job before compensation can be assigned to the employee.</span></span>  
6. <span data-ttu-id="807ba-115">ในฟิลด์แผน เลือกแผนค่าตอบแทนคงที่สำหรับพนักงาน </span><span class="sxs-lookup"><span data-stu-id="807ba-115">In the Plan field, select the fixed compensation plan for the employee.</span></span> <span data-ttu-id="807ba-116">การค้นหาแผนจะถูกกรองเพื่อแสดงเฉพาะแผนที่พนักงานมีสิทธิตามกฎการมีสิทธิ์</span><span class="sxs-lookup"><span data-stu-id="807ba-116">The Plan lookup is filtered to show only the plans that the employee is eligible for based on the Eligibility rules.</span></span>
7. <span data-ttu-id="807ba-117">ในรายการนี้ ให้ค้นหาและเลือกเรกคอร์ดที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="807ba-117">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="807ba-118">วันหมดอายุและวันที่มีผลบังคับใช้สำหรับค่าตอบแทนจะตั้งต้นจากวันเริ่มต้นและวันสิ้นสุดสำหรับการมอบหมายตำแหน่งงานของผู้ปฏิบัติงาน </span><span class="sxs-lookup"><span data-stu-id="807ba-118">The Effective and Expiration dates for the compensation default from the start and end dates for the worker's position assignment.</span></span> <span data-ttu-id="807ba-119">คุณสามารถปรับเปลี่ยนวันเหล่านี้ตามความจำเป็น</span><span class="sxs-lookup"><span data-stu-id="807ba-119">You can adjust these dates as needed.</span></span>  
    * <span data-ttu-id="807ba-120">ถ้าแผนค่าตอบแทนคงที่เป็นแผนขั้นตอน เลือกขั้นตอนที่ประกอบด้วยอัตราค่าจ้างที่ถูกต้องสำหรับพนักงาน </span><span class="sxs-lookup"><span data-stu-id="807ba-120">If the Fixed compensation plan is a step plan, select the step containing the correct pay rate for the employee.</span></span> <span data-ttu-id="807ba-121">ถ้าแผนค่าตอบแทนคงที่เป็นแผนระดับหรือแถบ ให้ป้อนอัตราค่าจ้างสำหรับพนักงาน </span><span class="sxs-lookup"><span data-stu-id="807ba-121">If the fixed compensation plan is a grade or a band plan, enter the pay rate for the employee.</span></span> <span data-ttu-id="807ba-122">อัตราค่าจ้างจะถูกตรวจสอบโดยเทียบกับการตั้งค่าค่าเผื่อสำหรับแผน และจุดอ้างอิงค่าต่ำสุดและสูงสุดสำหรับระดับค่าตอบแทนของงาน</span><span class="sxs-lookup"><span data-stu-id="807ba-122">The pay rate will be validated against the tolerance settings for the plan, and the minimum and maximum reference points for the job's compensation level.</span></span>  
8. <span data-ttu-id="807ba-123">คลิก ตกลง</span><span class="sxs-lookup"><span data-stu-id="807ba-123">Click OK.</span></span>


