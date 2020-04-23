---
title: สร้างแผนสวัสดิการของผู้ปฏิบัติงาน
description: คุณสามารถสร้างแผนสวัสดิการของผู้ปฏิบัติงานใน Microsoft Dynamics 365 Human Resources เพื่อเลือกแผนสวัสดิการสำหรับพนักงาน และเพื่อยืนยันการเลือกแผนสวัสดิการ
author: andreabichsel
manager: AnnBe
ms.date: 04/06/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: BenefitPlanEmployee
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 45b9a669d63620a15e6dc8047fed24c2db64438f
ms.sourcegitcommit: a9461650d11d6845e1942865ebf7e35f75f61ad3
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 04/06/2020
ms.locfileid: "3230050"
---
# <a name="create-worker-benefit-plans"></a><span data-ttu-id="f4f15-103">สร้างแผนสวัสดิการของผู้ปฏิบัติงาน</span><span class="sxs-lookup"><span data-stu-id="f4f15-103">Create worker benefit plans</span></span>

<span data-ttu-id="f4f15-104">คุณสามารถสร้างแผนสวัสดิการของผู้ปฏิบัติงานใน Microsoft Dynamics 365 Human Resources เพื่อเลือกแผนสวัสดิการสำหรับพนักงาน และเพื่อยืนยันการเลือกแผนสวัสดิการ</span><span class="sxs-lookup"><span data-stu-id="f4f15-104">You can create worker benefit plans in Microsoft Dynamics 365 Human Resources to select benefit plans for employees and to confirm benefit plan selections.</span></span> <span data-ttu-id="f4f15-105">โดยทั่วไป พนักงานเลือกแผนสวัสดิการด้วยตนเอง โดยใช้การบริการตนเองของพนักงาน แล้วผู้ดูแลระบบสวัสดิการจะยืนยันการเลือก</span><span class="sxs-lookup"><span data-stu-id="f4f15-105">Typically, employees select benefit plans themselves by using Employee self service, and then a benefits administrator confirms the selections.</span></span> 

1. <span data-ttu-id="f4f15-106">ในพื้นที่ทำงาน **การจัดการสิทธิประโยชน์** ภายใต้ **แผน** ให้เลือก **แผนสวัสดิการของผู้ปฏิบัติงาน**</span><span class="sxs-lookup"><span data-stu-id="f4f15-106">In the **Benefits management** workspace, under **Plans**, select **Worker benefit plans**.</span></span>

2. <span data-ttu-id="f4f15-107">เลือก **ใหม่**</span><span class="sxs-lookup"><span data-stu-id="f4f15-107">Select **New**.</span></span>

3. <span data-ttu-id="f4f15-108">ระบุค่าสำหรับฟิลด์ต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="f4f15-108">Specify values for the following fields:</span></span>

   | <span data-ttu-id="f4f15-109">ฟิลด์</span><span class="sxs-lookup"><span data-stu-id="f4f15-109">Field</span></span> | <span data-ttu-id="f4f15-110">คำอธิบาย</span><span class="sxs-lookup"><span data-stu-id="f4f15-110">Description</span></span> |
   | --- | --- |
   | <span data-ttu-id="f4f15-111">รอบระยะเวลา</span><span class="sxs-lookup"><span data-stu-id="f4f15-111">Period</span></span> | <span data-ttu-id="f4f15-112">ระบุรอบระยะเวลาสวัสดิการที่จะใช้ในการกรองข้อมูลแผนในแท็บด่วนของแผน กรองแผนเพื่อช่วยให้คุณเลือกชุดย่อยของเรกคอร์ดแผนทั้งหมด เพื่อให้คุณสามารถยืนยันชุดย่อยได้</span><span class="sxs-lookup"><span data-stu-id="f4f15-112">Specifies a benefits period to use to filter the plans in the Plans fast tab. Filter the plans to help you select a subset of all the plan records so that you can confirm the subset.</span></span> <span data-ttu-id="f4f15-113">ตัวอย่างเช่น เลือกรอบระยะเวลาที่คุณสร้างขึ้นเรียกว่า 2015 เพื่อยืนยันการเลือกการลงทะเบียนสวัสดิการทั้งหมดสำหรับ 2015</span><span class="sxs-lookup"><span data-stu-id="f4f15-113">For example, select a period you created called 2015 to confirm all the benefit enrollment selections for 2015.</span></span> |
   | <span data-ttu-id="f4f15-114">ผู้ปฏิบัติงาน</span><span class="sxs-lookup"><span data-stu-id="f4f15-114">Worker</span></span> | <span data-ttu-id="f4f15-115">ระบุผู้ปฏิบัติงานของผลประโยชน์ที่จะใช้ในการกรองข้อมูลแผนในแท็บแผนด่วนกรองแผนที่จะช่วยให้คุณเลือกชุดย่อยของเรกคอร์ดการวางแผนทั้งหมดเพื่อให้คุณสามารถยืนยันชุดย่อยได้</span><span class="sxs-lookup"><span data-stu-id="f4f15-115">Specifies a worker to use to filter the plans in the Plans fast tab. Filter the plans to help you select a subset of all the plan records so that you can confirm the subset.</span></span> |
   | <span data-ttu-id="f4f15-116">นิติบุคคล</span><span class="sxs-lookup"><span data-stu-id="f4f15-116">Legal entity</span></span> | <span data-ttu-id="f4f15-117">ระบุนิติบุคคลของผลประโยชน์ที่จะใช้ในการกรองข้อมูลแผนในแท็บแผนด่วนกรองแผนที่จะช่วยให้คุณเลือกชุดย่อยของเรกคอร์ดการวางแผนทั้งหมดเพื่อให้คุณสามารถยืนยันชุดย่อยได้</span><span class="sxs-lookup"><span data-stu-id="f4f15-117">Specifies a legal entity to use to filter the plans in the Plans fast tab. Filter the plans to help you select a subset of all the plan records so that you can confirm the subset.</span></span> |
   | <span data-ttu-id="f4f15-118">ตัวเลือกความคุ้มครอง</span><span class="sxs-lookup"><span data-stu-id="f4f15-118">Coverage option</span></span> | <span data-ttu-id="f4f15-119">ระบุตัวเลือกความคุ้มครองของผลประโยชน์ที่จะใช้ในการกรองข้อมูลแผนในแท็บแผนด่วนกรองแผนที่จะช่วยให้คุณเลือกชุดย่อยของเรกคอร์ดการวางแผนทั้งหมดเพื่อให้คุณสามารถยืนยันชุดย่อยได้</span><span class="sxs-lookup"><span data-stu-id="f4f15-119">Specifies a coverage option to use to filter the plans in the Plans fast tab. Filter the plans to help you select a subset of all the plan records so that you can confirm the subset.</span></span> |
   | <span data-ttu-id="f4f15-120">ค่าเริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="f4f15-120">Default</span></span> | <span data-ttu-id="f4f15-121">กรองแผนสวัสดิการโดยพิจารณาว่าข้อมูลเป็นแผนเริ่มต้นหรือไม่</span><span class="sxs-lookup"><span data-stu-id="f4f15-121">Filters the benefit plans based on whether they are a default plan.</span></span> <span data-ttu-id="f4f15-122">กรองแผนที่ช่วยให้คุณเลือกชุดย่อยของเรกคอร์ดแผนทั้งหมด เพื่อให้คุณสามารถยืนยันชุดย่อยได้</span><span class="sxs-lookup"><span data-stu-id="f4f15-122">Filter the plans to help you select a subset of all the plan records so that you can confirm the subset.</span></span> |
   | <span data-ttu-id="f4f15-123">สถานะ</span><span class="sxs-lookup"><span data-stu-id="f4f15-123">Status</span></span> | <span data-ttu-id="f4f15-124">กรองแผนสวัสดิการตามสถานะของพนักงาน</span><span class="sxs-lookup"><span data-stu-id="f4f15-124">Filters benefit plans based on their status.</span></span> <span data-ttu-id="f4f15-125">กรองแผนที่ช่วยให้คุณเลือกชุดย่อยของเรกคอร์ดแผนทั้งหมด เพื่อให้คุณสามารถยืนยันชุดย่อยได้</span><span class="sxs-lookup"><span data-stu-id="f4f15-125">Filter the plans to help you select a subset of all the plan records so that you can confirm the subset.</span></span> |
   | <span data-ttu-id="f4f15-126">ใบสั่งขาย</span><span class="sxs-lookup"><span data-stu-id="f4f15-126">Confirmation</span></span> | <span data-ttu-id="f4f15-127">ระบุสถานะการยืนยันของผลประโยชน์ที่จะใช้ในการกรองข้อมูลแผนในแท็บแผนด่วนกรองแผนที่จะช่วยให้คุณเลือกชุดย่อยของเรกคอร์ดการวางแผนทั้งหมดเพื่อให้คุณสามารถยืนยันชุดย่อยได้</span><span class="sxs-lookup"><span data-stu-id="f4f15-127">Specifies the confirmation status to use to filter the plans in the Plans fast tab. Filter the plans to help you select a subset of all the plan records so that you can confirm the subset.</span></span> |
   | <span data-ttu-id="f4f15-128">การยกเลิก</span><span class="sxs-lookup"><span data-stu-id="f4f15-128">Cancellation</span></span> | <span data-ttu-id="f4f15-129">ระบุสถานะการยกเลิกของผลประโยชน์ที่จะใช้ในการกรองข้อมูลแผนในแท็บแผนด่วนกรองแผนที่จะช่วยให้คุณเลือกชุดย่อยของเรกคอร์ดการวางแผนทั้งหมดเพื่อให้คุณสามารถยืนยันชุดย่อยได้</span><span class="sxs-lookup"><span data-stu-id="f4f15-129">Specifies the cancellation status to use to filter the plans in the Plans fast tab. Filter the plans to help you select a subset of all the plan records so that you can confirm the subset.</span></span> |
   | <span data-ttu-id="f4f15-130">ตัวกรองวันที่มีผลบังคับใช้</span><span class="sxs-lookup"><span data-stu-id="f4f15-130">Effective date filter</span></span> | <span data-ttu-id="f4f15-131">กรองแผนโดยพิจารณาว่าผู้ใช้เหล่านั้นหมดอายุ ไม่ใช้งานอยู่ หรือจะเปิดใช้งานในอนาคต</span><span class="sxs-lookup"><span data-stu-id="f4f15-131">Filters the plans based on whether they’re expired, active, or will be active in the future.</span></span> <span data-ttu-id="f4f15-132">เลือกกล่องกาเครื่องหมายที่ตรงกับแผนที่คุณต้องการดูในแท็บด่วนของ Plans</span><span class="sxs-lookup"><span data-stu-id="f4f15-132">Select the check boxes that correspond to the plans you want to see in the Plans fast tab.</span></span> |
   | <span data-ttu-id="f4f15-133">แผน</span><span class="sxs-lookup"><span data-stu-id="f4f15-133">Plans</span></span> | <span data-ttu-id="f4f15-134">แท็บด่วนของ Plans มีแผนที่ตรงกับเกณฑ์ตัวกรองที่คุณระบุ</span><span class="sxs-lookup"><span data-stu-id="f4f15-134">The Plans fast tab contains the plans that meet the filter criteria you specified.</span></span> <span data-ttu-id="f4f15-135">ตัวเลือกการตั้งค่าคอนฟิกที่เกี่ยวข้องซึ่งตั้งค่าโดยเจ้าหน้าที่ฝ่ายทรัพยากรบุคคล และการเลือกการลงทะเบียนที่ถูกเลือกโดยพนักงานจะรวมไว้ในแต่ละบรรทัด</span><span class="sxs-lookup"><span data-stu-id="f4f15-135">The relevant configuration options that were set by HR staff and the enrollment selections that were chosen by employees are included on each line.</span></span> <span data-ttu-id="f4f15-136">ฟิลด์ที่เข้าเกณฑ์ระบุว่ามีความขัดแย้งในการตรวจสอบความถูกต้องกับการเลือกแผนหรือไม่</span><span class="sxs-lookup"><span data-stu-id="f4f15-136">The Qualified field specifies whether there is a validation conflict with the plan selection.</span></span> |

4. <span data-ttu-id="f4f15-137">เลือก **บันทึก**</span><span class="sxs-lookup"><span data-stu-id="f4f15-137">Select **Save**.</span></span>
