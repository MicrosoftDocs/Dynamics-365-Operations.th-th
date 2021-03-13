---
title: เพิ่มลงในสมุดรายวันประสิทธิภาพของคุณ และส่งการชมเชยให้แก่บุคคลอื่น
description: 'สมุดรายวันประสิทธิภาพจะเก็บข้อมูลที่เกี่ยวข้องกับวิธีที่คุณดำเนินการตามเป้าหมายของคุณหรือวิธีที่คุณดำเนินการในระหว่างรอบระยะเวลา '
author: andreabichsel
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EssWorkspace, HcmPerfJournal, HcmPerfJournalAddLink, HcmPerfPraise, HcmWorkerLookUpByPerson, HcmPerfJournalAdd, HcmEmployeeDevelopmentWorkspace
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 574925f0e278ad7bd3c654432fd0f862fd3c3259
ms.sourcegitcommit: 18e626c49ccfdb12c1484b985e3a275e51f61320
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 02/04/2021
ms.locfileid: "5115883"
---
# <a name="add-to-your-performance-journal-and-send-praise-to-someone"></a><span data-ttu-id="26920-103">เพิ่มลงในสมุดรายวันประสิทธิภาพของคุณ และส่งการชมเชยให้แก่บุคคลอื่น</span><span class="sxs-lookup"><span data-stu-id="26920-103">Add to your performance journal and send praise to someone</span></span>

<span data-ttu-id="26920-104">สมุดรายวันประสิทธิภาพจะเก็บข้อมูลที่เกี่ยวข้องกับวิธีที่คุณดำเนินการตามเป้าหมายของคุณหรือวิธีที่คุณดำเนินการในระหว่างรอบระยะเวลา </span><span class="sxs-lookup"><span data-stu-id="26920-104">The performance journal holds information that relates to how you met your goals or how you performed during a period.</span></span> <span data-ttu-id="26920-105">นอกจากนี้คุณยังสามารถชมเชยการดำเนินการของผู้ปฏิบัติงานร่วมจากสมุดรายวัน </span><span class="sxs-lookup"><span data-stu-id="26920-105">You can also praise the actions of a co-worker from the journal.</span></span> <span data-ttu-id="26920-106">บริษัทข้อมูลสาธิตที่เคยสร้างกระบวนงานนี้คือ USMF</span><span class="sxs-lookup"><span data-stu-id="26920-106">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="26920-107">กระบวนงานนี้ใช้สำหรับคุณลักษณะทั้ที่ถูกเพิ่มลงใน Dynamics 365 for Operations รุ่น 1611</span><span class="sxs-lookup"><span data-stu-id="26920-107">This procedure is for a feature that was added in Dynamics 365 for Operations version 1611.</span></span>

1. <span data-ttu-id="26920-108">ไปที่ พื้นที่ทำงานทั้งหมด > ระบบลูกค้าบริการตนเอง</span><span class="sxs-lookup"><span data-stu-id="26920-108">Go to All workspaces > Employee self service.</span></span>
2. <span data-ttu-id="26920-109">คลิก สมุดรายวันประสิทธิภาพ</span><span class="sxs-lookup"><span data-stu-id="26920-109">Click Performance journal.</span></span>
3. <span data-ttu-id="26920-110">คลิก สร้าง</span><span class="sxs-lookup"><span data-stu-id="26920-110">Click New.</span></span>
4. <span data-ttu-id="26920-111">ในฟิลด์หัวข้อ ให้พิมพ์ค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="26920-111">In the Title field, type a value.</span></span>
5. <span data-ttu-id="26920-112">ในฟิลด์ คำอธิบาย ให้พิมพ์ค่า</span><span class="sxs-lookup"><span data-stu-id="26920-112">In the Description field, type a value.</span></span>
    * <span data-ttu-id="26920-113">วันที่ของสมุดรายวันประสิทธิภาพคือวันที่ที่สร้างสมุดรายวัน</span><span class="sxs-lookup"><span data-stu-id="26920-113">The performance journal date is the date that the journal was created.</span></span>  
    * <span data-ttu-id="26920-114">แหล่งข้อมูลจะแสดงที่มาของสมุดรายวันประสิทธิภาพ </span><span class="sxs-lookup"><span data-stu-id="26920-114">The source represents where the performance journal came from.</span></span> <span data-ttu-id="26920-115">เมื่อคุณสร้างแหล่งข้อมูลขึ้น แหล่งข้อมูลนั้นจะมาจาก สมุดรายวันของฉัน </span><span class="sxs-lookup"><span data-stu-id="26920-115">When you create one, it comes from My journal.</span></span> <span data-ttu-id="26920-116">ถ้าผู้จัดการของคุณสร้างแหล่งข้อมูลขึ้น แหล่งข้อมูลนั้นจะมาจากสมุดรายของวันผู้จัดการ</span><span class="sxs-lookup"><span data-stu-id="26920-116">If your manager creates one, it comes from the Manager journal.</span></span>  
    * <span data-ttu-id="26920-117">คุณสามารถใช้สมุดรายวันนี้ร่วมกับผู้จัดการของคุณ หรือทำให้สามารถดูได้สำหรับคุณเท่านั้น</span><span class="sxs-lookup"><span data-stu-id="26920-117">You can share this journal with your manager or make it only visible to you.</span></span>  
6. <span data-ttu-id="26920-118">ในฟิลด์วันที่เริ่มต้น ให้ป้อนวันที่ </span><span class="sxs-lookup"><span data-stu-id="26920-118">In the Start date field, enter a date.</span></span>
7. <span data-ttu-id="26920-119">ในฟิลด์วันที่เสร็จสมบูรณ์ ให้ป้อนวันที่</span><span class="sxs-lookup"><span data-stu-id="26920-119">In the Date completed field, enter a date.</span></span>
8. <span data-ttu-id="26920-120">เลือก ใช่ ในฟิลด์แผนการพัฒนา</span><span class="sxs-lookup"><span data-stu-id="26920-120">Select Yes in the Development plan field.</span></span>
9. <span data-ttu-id="26920-121">ในฟิลด์คำสำคัญ ให้พิมพ์ค่า</span><span class="sxs-lookup"><span data-stu-id="26920-121">In the Keywords field, type a value.</span></span>
10. <span data-ttu-id="26920-122">คลิก เพิ่มการเชื่อมโยงภายนอก</span><span class="sxs-lookup"><span data-stu-id="26920-122">Click Add external link.</span></span>
11. <span data-ttu-id="26920-123">ในฟิลด์คำอธิบาย พิมพ์ 'การมองเห็น'</span><span class="sxs-lookup"><span data-stu-id="26920-123">In the Description field, type 'Envision'.</span></span>
12. <span data-ttu-id="26920-124">ในฟิลด์ที่อยู่อินเทอร์เน็ต ให้พิมพ์ 'https://www.microsoft.com/en/envision/default'</span><span class="sxs-lookup"><span data-stu-id="26920-124">In the Internet address field, type 'https://www.microsoft.com/en/envision/default'.</span></span>
13. <span data-ttu-id="26920-125">คลิกคำอธิบายใต้ปุ่มบันทึกที่ระบุว่า "สมุดรายวันประสิทธิภาพ" เพื่อกลับไปยังกริด</span><span class="sxs-lookup"><span data-stu-id="26920-125">Click on the caption below the Save button called "Performance journal" to return to the grid.</span></span>
    * <span data-ttu-id="26920-126">คุณสามารถเพิ่มสมุดรายวันที่เลือกอย่างน้อยหนึ่งรายการให้กับเป้าหมายเพื่อให้ปรากฏขึ้นเมื่อคุณเปิดเป้าหมาย </span><span class="sxs-lookup"><span data-stu-id="26920-126">You can add the selected journal or journals to a goal so that it appears when you open the goal.</span></span> <span data-ttu-id="26920-127">การเชื่อมโยงจะถูกเพิ่มลงในแท็บด่วนการเชื่อมโยง ถ้าคุณเพิ่มสมุดรายวันให้กับเป้าหมาย และเพิ่มเป้าหมายให้กับการตรวจทาน สมุดรายวันจะปรากฏในการตรวจทานโดยอัตโนมัติ</span><span class="sxs-lookup"><span data-stu-id="26920-127">A link will be added in the Links fast tab.    If you add a journal to a goal and then add the goal to a review, the journal will appear on the review automatically.</span></span>  
    * <span data-ttu-id="26920-128">คุณสามารถเพิ่มสมุดรายวันที่เลือกอย่างน้อยหนึ่งรายการให้กับเป้าหมายเพื่อให้ปรากฏขึ้นเมื่อคุณเปิดเป้าหมาย </span><span class="sxs-lookup"><span data-stu-id="26920-128">You can add the selected journal or journals to a review so that it appears when you open the review.</span></span>    <span data-ttu-id="26920-129">การเชื่อมโยงจะถูกเพิ่มลงในแท็บด่วนการเชื่อมโยง</span><span class="sxs-lookup"><span data-stu-id="26920-129">A link will be added in the Links fast tab.</span></span>  
14. <span data-ttu-id="26920-130">คลิก การเพิ่มด่วน</span><span class="sxs-lookup"><span data-stu-id="26920-130">Click Quick add.</span></span>
15. <span data-ttu-id="26920-131">ในฟิลด์หัวข้อ ให้พิมพ์ค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="26920-131">In the Title field, type a value.</span></span>
16. <span data-ttu-id="26920-132">ในฟิลด์ คำอธิบาย ให้พิมพ์ค่า</span><span class="sxs-lookup"><span data-stu-id="26920-132">In the Description field, type a value.</span></span>
17. <span data-ttu-id="26920-133">คลิกบันทึก</span><span class="sxs-lookup"><span data-stu-id="26920-133">Click Save.</span></span>
18. <span data-ttu-id="26920-134">คลิก ส่งการชมเชย</span><span class="sxs-lookup"><span data-stu-id="26920-134">Click Send praise.</span></span>
19. <span data-ttu-id="26920-135">เลือกบุคคลจากรายชื่อพนักงานในบริษัท</span><span class="sxs-lookup"><span data-stu-id="26920-135">Select a person from the list of employees in the company.</span></span>
20. <span data-ttu-id="26920-136">ในฟิลด์คำอธิบาย ป้อน 'ขอบคุณสำหรับความช่วยเหลือทั้งหมดในการประชุม'</span><span class="sxs-lookup"><span data-stu-id="26920-136">In the Description field, enter 'Thanks for all the help at the conference!'.</span></span>
21. <span data-ttu-id="26920-137">คลิก ส่ง</span><span class="sxs-lookup"><span data-stu-id="26920-137">Click Send.</span></span>

