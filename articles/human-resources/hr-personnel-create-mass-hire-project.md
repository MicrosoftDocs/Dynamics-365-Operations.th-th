---
title: การสร้างโครงการจ้างงานโดยรวม
description: 'กระบวนการนี้จะนำคุณไปสู่กระบวนการตั้งค่าโครงการจ้างงานโดยรวม '
author: andreabichsel
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: HRMMassHireProject,  HRMMassHireLineCreate, HcmJobLookup
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 19d2f41f92aef7739e8e36012e207b96af155190
ms.sourcegitcommit: 40163705a134c9874fd33be80c7ae59ccce22c21
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 02/03/2020
ms.locfileid: "3010766"
---
# <a name="create-a-mass-hire-project"></a><span data-ttu-id="266ce-103">การสร้างโครงการจ้างงานโดยรวม</span><span class="sxs-lookup"><span data-stu-id="266ce-103">Create a mass hire project</span></span>



<span data-ttu-id="266ce-104">กระบวนการนี้จะนำคุณไปสู่กระบวนการตั้งค่าโครงการจ้างงานโดยรวม </span><span class="sxs-lookup"><span data-stu-id="266ce-104">This procedure walks through the process of setting up a mass hire project.</span></span> <span data-ttu-id="266ce-105">ผู้สรรหาสามารถใช้โครงการจ้างงานโดยรวมเพื่อให้ง่ายต่อการสร้างตำแหน่งงานหลายตำแหน่งและว่าจ้างผู้ปฏิบัติงานจำนวนหนึ่งในตำแหน่งเหล่านั้น </span><span class="sxs-lookup"><span data-stu-id="266ce-105">A recruiter can use mass hire projects to easily create multiple positions and hire a number of workers into those positions.</span></span> <span data-ttu-id="266ce-106">เพื่อเริ่มต้นขั้นตอนนี้ ให้ไปที่ฝ่ายทรัพยากรบุคคล > การสรรหาบุคลากร > โครงการจ้างงานโดยรวม</span><span class="sxs-lookup"><span data-stu-id="266ce-106">To begin this procedure, go to Human resources > Recruitment > Mass hire projects.</span></span> <span data-ttu-id="266ce-107">ข้อมูลบริษัทสาธิตที่ใช้ในการสร้างกระบวนงานนี้คือ USMF</span><span class="sxs-lookup"><span data-stu-id="266ce-107">The demo data company used to create this procedure is USMF.</span></span>

1. <span data-ttu-id="266ce-108">คลิก สร้าง</span><span class="sxs-lookup"><span data-stu-id="266ce-108">Click New.</span></span>
2. <span data-ttu-id="266ce-109">ในฟิลด์โครงการจ้างงานโดยรวม ให้พิมพ์ค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="266ce-109">In the Mass hire project field, type a value.</span></span>
3. <span data-ttu-id="266ce-110">ในฟิลด์ คำอธิบาย ให้พิมพ์ค่า</span><span class="sxs-lookup"><span data-stu-id="266ce-110">In the Description field, type a value.</span></span>
4. <span data-ttu-id="266ce-111">ในฟิลด์เริ่มต้นโครงการ ให้ป้อนวันที่</span><span class="sxs-lookup"><span data-stu-id="266ce-111">In the Project start field, enter a date.</span></span>
5. <span data-ttu-id="266ce-112">ในฟิลด์สิ้นสุดโครงการ ให้ป้อนวันที่</span><span class="sxs-lookup"><span data-stu-id="266ce-112">In the Project end field, enter a date.</span></span>
6. <span data-ttu-id="266ce-113">คลิก เปิดโครงการ</span><span class="sxs-lookup"><span data-stu-id="266ce-113">Click Open project.</span></span>
7. <span data-ttu-id="266ce-114">คลิก ใช่</span><span class="sxs-lookup"><span data-stu-id="266ce-114">Click Yes.</span></span>
8. <span data-ttu-id="266ce-115">คลิก สร้างตำแหน่ง</span><span class="sxs-lookup"><span data-stu-id="266ce-115">Click Create positions.</span></span>
9. <span data-ttu-id="266ce-116">ในฟิลด์ปริมาณ ให้ป้อนจำนวนของตำแหน่งที่คุณต้องการสร้าง</span><span class="sxs-lookup"><span data-stu-id="266ce-116">In the Quantity field, enter the number of positions that you want to create</span></span>
    * <span data-ttu-id="266ce-117">วันเริ่มต้นจะกลายเป็นวันจ้างงานสำหรับผู้ปฏิบัติงานใหม่</span><span class="sxs-lookup"><span data-stu-id="266ce-117">The Start date will become the Hire date for the new workers.</span></span>  
    * <span data-ttu-id="266ce-118">วันสิ้นสุดจะกลายเป็นวันสิ้นสุดการจ้างงานสำหรับผู้ปฏิบัติงานใหม่</span><span class="sxs-lookup"><span data-stu-id="266ce-118">The End date will be the Termination date for the new workers.</span></span>  
    * <span data-ttu-id="266ce-119">ระบุว่าผู้ปฏิบัติงานใหม่เป็นพนักงานหรือผู้รับเหมา</span><span class="sxs-lookup"><span data-stu-id="266ce-119">Specify whether the new workers will be Employees or Contractors.</span></span>  
10. <span data-ttu-id="266ce-120">ในฟิลด์งาน คลิกปุ่มดรอปดาวน์เพื่อเลือกงานสำหรับการสร้างตำแหน่ง</span><span class="sxs-lookup"><span data-stu-id="266ce-120">In the Job field, click the drop-down button to select the job to create the positions for.</span></span>
11. <span data-ttu-id="266ce-121">ในรายการนี้ ให้ค้นหาและเลือกเรกคอร์ดที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="266ce-121">In the list, find and select the desired record.</span></span>
12. <span data-ttu-id="266ce-122">ในรายการนี้ ให้คลิกลิงค์ในแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="266ce-122">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="266ce-123">ค่าเทียบเท่าเต็มเวลาเริ่มต้นจะมาจากงานที่เลือก </span><span class="sxs-lookup"><span data-stu-id="266ce-123">The default full-time equivalent value will come from the selected job.</span></span> <span data-ttu-id="266ce-124">คุณสามารถเปลี่ยนข้อมูลนี้ได้ถ้าจำเป็น</span><span class="sxs-lookup"><span data-stu-id="266ce-124">You can change this if needed.</span></span>  
    * <span data-ttu-id="266ce-125">อีกทางหนึ่งคือ เลือกแผนกสำหรับตำแหน่งใหม่</span><span class="sxs-lookup"><span data-stu-id="266ce-125">Optionally, select the Department for the new positions.</span></span>  
13. <span data-ttu-id="266ce-126">คลิก ตกลง</span><span class="sxs-lookup"><span data-stu-id="266ce-126">Click OK.</span></span>

