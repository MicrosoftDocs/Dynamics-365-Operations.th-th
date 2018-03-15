--- 
title: " สร้างกลุ่มสิทธิ์ของ POS"
description: "ขั้นตอนนี้จะแสดงวิธีการสร้างกลุ่มสิทธิ์ของ POS "
author: scott-tucker
manager: AnnBe
ms.date: 03/02/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations, Retail
ms.search.region: Global
ms.search.industry: Retail
ms.author: scotttuc
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: ea07d8e91c94d9fdad4c2d05533981e254420188
ms.openlocfilehash: bcda7c3a5c2cc97fbc6e4945e4d5f0ec42a7a478
ms.contentlocale: th-th
ms.lasthandoff: 02/07/2018

---
# <a name="create-pos-permission-groups"></a><span data-ttu-id="3223f-103"> สร้างกลุ่มสิทธิ์ของ POS</span><span class="sxs-lookup"><span data-stu-id="3223f-103">Create POS permission groups</span></span>

[!include[task guide banner](../includes/task-guide-banner.md)]

<span data-ttu-id="3223f-104">ขั้นตอนนี้จะแสดงวิธีการสร้างกลุ่มสิทธิ์ของ POS </span><span class="sxs-lookup"><span data-stu-id="3223f-104">This procedure will show how to create a POS permission group.</span></span> <span data-ttu-id="3223f-105">ข้อมูลบริษัทสาธิตที่ใช้ในการสร้างงานนี้คือ USRT </span><span class="sxs-lookup"><span data-stu-id="3223f-105">The demo data company used to create this task is USRT.</span></span> <span data-ttu-id="3223f-106">งานนี้มีไว้สำหรับบทบาทผู้จัดการการดำเนินงานขายปลีก</span><span class="sxs-lookup"><span data-stu-id="3223f-106">This task is intended for the Retail operations manager role.</span></span>

1. <span data-ttu-id="3223f-107">ไปที่กลุ่มสิทธิ์</span><span class="sxs-lookup"><span data-stu-id="3223f-107">Go to Permission groups.</span></span>
2. <span data-ttu-id="3223f-108">คลิก สร้าง</span><span class="sxs-lookup"><span data-stu-id="3223f-108">Click New.</span></span>
3. <span data-ttu-id="3223f-109">ในฟิลด์รหัสกลุ่มสิทธิ์ของ POS ให้พิมพ์ค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="3223f-109">In the POS permission group ID field, type a value.</span></span>
4. <span data-ttu-id="3223f-110">ในฟิลด์ คำอธิบาย ให้พิมพ์ค่า</span><span class="sxs-lookup"><span data-stu-id="3223f-110">In the Description field, type a value.</span></span>
5. <span data-ttu-id="3223f-111">เลือกใช่ในฟิลด์ดูรายการของนาฬิกาตอกบัตร</span><span class="sxs-lookup"><span data-stu-id="3223f-111">Select Yes in the View time clock entries field.</span></span>
    * <span data-ttu-id="3223f-112">ขณะนี้คุณสามารถเปิดใช้งานหรือปิดใช้งานสิทธิ์ต่างๆ สำหรับกลุ่มสิทธิ์ของ POS ของคุณ </span><span class="sxs-lookup"><span data-stu-id="3223f-112">You can now enable or disable various permissions for your POS Permission group.</span></span> <span data-ttu-id="3223f-113">สำหรับบางสิทธิ์คุณสามารถตั้งค่าที่จะใช้เพื่อประเมินว่าผู้ใช้ POS สามารถดำเนินการได้หรือไม่ </span><span class="sxs-lookup"><span data-stu-id="3223f-113">For some permission you can set a value that will be used to evaluate if the POS user can perform the action.</span></span>  <span data-ttu-id="3223f-114">คำแนะนำของงานนี้เปิดใช้งานสิทธิ์ส่วนหนึ่งที่อาจโอนให้กับพนักงานเก็บเงิน</span><span class="sxs-lookup"><span data-stu-id="3223f-114">This task guide enables a few permission that might be given to a cashier.</span></span>  
6. <span data-ttu-id="3223f-115">เลือกใช่ในฟิลด์อนุญาตให้สร้างใบสั่ง</span><span class="sxs-lookup"><span data-stu-id="3223f-115">Select Yes in the Allow create order field.</span></span>
7. <span data-ttu-id="3223f-116">เลือกใช่ในฟิลด์อนุญาตให้แก้ไขใบสั่ง</span><span class="sxs-lookup"><span data-stu-id="3223f-116">Select Yes in the Allow edit order field.</span></span>
8. <span data-ttu-id="3223f-117">เลือกใช่ในฟิลด์อนุญาตให้ดึงข้อมูลใบสั่ง</span><span class="sxs-lookup"><span data-stu-id="3223f-117">Select Yes in the Allow retrieve order field.</span></span>
9. <span data-ttu-id="3223f-118">เลือกใช่ในฟิลด์อนุญาตให้แก้ไขรหัสผ่าน</span><span class="sxs-lookup"><span data-stu-id="3223f-118">Select Yes in the Allow password change field.</span></span>
10. <span data-ttu-id="3223f-119">เลือกใช่ในฟิลด์อนุญาตให้ปิดซ่อน</span><span class="sxs-lookup"><span data-stu-id="3223f-119">Select Yes in the Allow blind close field.</span></span>
11. <span data-ttu-id="3223f-120">คลิก บันทึก</span><span class="sxs-lookup"><span data-stu-id="3223f-120">Click Save.</span></span>
    * <span data-ttu-id="3223f-121">หลังจากที่มีบันทึกการเปลี่ยนแปลง คุณต้องรันกำหนดการกระจายพนักงานเพื่อผลักดันการเปลี่ยนแปลงไปยังช่องทางการขายปลีก</span><span class="sxs-lookup"><span data-stu-id="3223f-121">After your changes are saved you need to run the Staff distribution schedule to push the changes to retail channels.</span></span>  
12. <span data-ttu-id="3223f-122">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="3223f-122">Close the page.</span></span>
13. <span data-ttu-id="3223f-123">ไปที่งาน</span><span class="sxs-lookup"><span data-stu-id="3223f-123">Go to Jobs.</span></span>
    * <span data-ttu-id="3223f-124">ถัดไป เราจะกำหนดกลุ่มสิทธิ์ของ POS ให้กับงาน</span><span class="sxs-lookup"><span data-stu-id="3223f-124">Next we will assign the POS permission group to a Job.</span></span>  
14. <span data-ttu-id="3223f-125">ในรายการนี้ ให้ค้นหาและเลือกเรกคอร์ดที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="3223f-125">In the list, find and select the desired record.</span></span>
15. <span data-ttu-id="3223f-126">ในรายการนี้ ให้คลิกลิงค์ในแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="3223f-126">In the list, click the link in the selected row.</span></span>
16. <span data-ttu-id="3223f-127">คลิกแก้ไข</span><span class="sxs-lookup"><span data-stu-id="3223f-127">Click Edit.</span></span>
17. <span data-ttu-id="3223f-128">ขยายส่วนการจัดประเภทงาน</span><span class="sxs-lookup"><span data-stu-id="3223f-128">Expand the Job classification section.</span></span>
18. <span data-ttu-id="3223f-129">ในฟิลด์สิทธิ์ของ POS ให้ป้อนหรือเลือกค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="3223f-129">In the POS permission group field, enter or select a value.</span></span>
    * <span data-ttu-id="3223f-130">ผู้ปฏิบัติงานทั้งหมดในตำแหน่งงานนี้จะใช้การตั้งค่าของกลุ่มสิทธิ์ของ POS ยกเว้นว่ามีการแทนสิทธิ์ของ POS ของผู้ปฏิบัติงานในระดับของตำแหน่งงาน</span><span class="sxs-lookup"><span data-stu-id="3223f-130">All Workers in Positions for this Job will use this POS permission group’s settings unless the workers POS permissions have been overridden at their Position level.</span></span>  
19. <span data-ttu-id="3223f-131">คลิก บันทึก</span><span class="sxs-lookup"><span data-stu-id="3223f-131">Click Save.</span></span>
    * <span data-ttu-id="3223f-132">หลังจากที่มีบันทึกการเปลี่ยนแปลง คุณต้องรันกำหนดการกระจายพนักงานเพื่อผลักดันการเปลี่ยนแปลงไปยังช่องทางการขายปลีก</span><span class="sxs-lookup"><span data-stu-id="3223f-132">After your changes are saved you need to run the Staff distribution schedule to push the changes to retail channels.</span></span>  


