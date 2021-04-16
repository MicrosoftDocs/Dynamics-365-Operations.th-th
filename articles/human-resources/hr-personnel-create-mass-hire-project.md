---
title: การสร้างโครงการจ้างงานโดยรวม
description: 'กระบวนการนี้จะนำคุณไปสู่กระบวนการตั้งค่าโครงการจ้างงานโดยรวม '
author: andreabichsel
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: HRMMassHireProject,  HRMMassHireLineCreate, HcmJobLookup, HcmPersonnelManagementWorkspace
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 353bfe6c9a79db91a86e612737ea7705c8cdaeb8
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 03/31/2021
ms.locfileid: "5800224"
---
# <a name="create-a-mass-hire-project"></a><span data-ttu-id="6a5d9-103">การสร้างโครงการจ้างงานโดยรวม</span><span class="sxs-lookup"><span data-stu-id="6a5d9-103">Create a mass hire project</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]



<span data-ttu-id="6a5d9-104">กระบวนการนี้จะนำคุณไปสู่กระบวนการตั้งค่าโครงการจ้างงานโดยรวม </span><span class="sxs-lookup"><span data-stu-id="6a5d9-104">This procedure walks through the process of setting up a mass hire project.</span></span> <span data-ttu-id="6a5d9-105">ผู้สรรหาสามารถใช้โครงการจ้างงานโดยรวมเพื่อให้ง่ายต่อการสร้างตำแหน่งงานหลายตำแหน่งและว่าจ้างผู้ปฏิบัติงานจำนวนหนึ่งในตำแหน่งเหล่านั้น </span><span class="sxs-lookup"><span data-stu-id="6a5d9-105">A recruiter can use mass hire projects to easily create multiple positions and hire a number of workers into those positions.</span></span> <span data-ttu-id="6a5d9-106">เพื่อเริ่มต้นขั้นตอนนี้ ให้ไปที่ฝ่ายทรัพยากรบุคคล > การสรรหาบุคลากร > โครงการจ้างงานโดยรวม</span><span class="sxs-lookup"><span data-stu-id="6a5d9-106">To begin this procedure, go to Human resources > Recruitment > Mass hire projects.</span></span> <span data-ttu-id="6a5d9-107">ข้อมูลบริษัทสาธิตที่ใช้ในการสร้างกระบวนงานนี้คือ USMF</span><span class="sxs-lookup"><span data-stu-id="6a5d9-107">The demo data company used to create this procedure is USMF.</span></span>

1. <span data-ttu-id="6a5d9-108">คลิก สร้าง</span><span class="sxs-lookup"><span data-stu-id="6a5d9-108">Click New.</span></span>
2. <span data-ttu-id="6a5d9-109">ในฟิลด์โครงการจ้างงานโดยรวม ให้พิมพ์ค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="6a5d9-109">In the Mass hire project field, type a value.</span></span>
3. <span data-ttu-id="6a5d9-110">ในฟิลด์ คำอธิบาย ให้พิมพ์ค่า</span><span class="sxs-lookup"><span data-stu-id="6a5d9-110">In the Description field, type a value.</span></span>
4. <span data-ttu-id="6a5d9-111">ในฟิลด์เริ่มต้นโครงการ ให้ป้อนวันที่</span><span class="sxs-lookup"><span data-stu-id="6a5d9-111">In the Project start field, enter a date.</span></span>
5. <span data-ttu-id="6a5d9-112">ในฟิลด์สิ้นสุดโครงการ ให้ป้อนวันที่</span><span class="sxs-lookup"><span data-stu-id="6a5d9-112">In the Project end field, enter a date.</span></span>
6. <span data-ttu-id="6a5d9-113">คลิก เปิดโครงการ</span><span class="sxs-lookup"><span data-stu-id="6a5d9-113">Click Open project.</span></span>
7. <span data-ttu-id="6a5d9-114">คลิก ใช่</span><span class="sxs-lookup"><span data-stu-id="6a5d9-114">Click Yes.</span></span>
8. <span data-ttu-id="6a5d9-115">คลิก สร้างตำแหน่ง</span><span class="sxs-lookup"><span data-stu-id="6a5d9-115">Click Create positions.</span></span>
9. <span data-ttu-id="6a5d9-116">ในฟิลด์ปริมาณ ให้ป้อนจำนวนของตำแหน่งที่คุณต้องการสร้าง</span><span class="sxs-lookup"><span data-stu-id="6a5d9-116">In the Quantity field, enter the number of positions that you want to create</span></span>
    * <span data-ttu-id="6a5d9-117">วันเริ่มต้นจะกลายเป็นวันจ้างงานสำหรับผู้ปฏิบัติงานใหม่</span><span class="sxs-lookup"><span data-stu-id="6a5d9-117">The Start date will become the Hire date for the new workers.</span></span>  
    * <span data-ttu-id="6a5d9-118">วันสิ้นสุดจะกลายเป็นวันสิ้นสุดการจ้างงานสำหรับผู้ปฏิบัติงานใหม่</span><span class="sxs-lookup"><span data-stu-id="6a5d9-118">The End date will be the Termination date for the new workers.</span></span>  
    * <span data-ttu-id="6a5d9-119">ระบุว่าผู้ปฏิบัติงานใหม่เป็นพนักงานหรือผู้รับเหมา</span><span class="sxs-lookup"><span data-stu-id="6a5d9-119">Specify whether the new workers will be Employees or Contractors.</span></span>  
10. <span data-ttu-id="6a5d9-120">ในฟิลด์งาน คลิกปุ่มดรอปดาวน์เพื่อเลือกงานสำหรับการสร้างตำแหน่ง</span><span class="sxs-lookup"><span data-stu-id="6a5d9-120">In the Job field, click the drop-down button to select the job to create the positions for.</span></span>
11. <span data-ttu-id="6a5d9-121">ในรายการนี้ ให้ค้นหาและเลือกเรกคอร์ดที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="6a5d9-121">In the list, find and select the desired record.</span></span>
12. <span data-ttu-id="6a5d9-122">ในรายการนี้ ให้คลิกลิงค์ในแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="6a5d9-122">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="6a5d9-123">ค่าเทียบเท่าเต็มเวลาเริ่มต้นจะมาจากงานที่เลือก </span><span class="sxs-lookup"><span data-stu-id="6a5d9-123">The default full-time equivalent value will come from the selected job.</span></span> <span data-ttu-id="6a5d9-124">คุณสามารถเปลี่ยนข้อมูลนี้ได้ถ้าจำเป็น</span><span class="sxs-lookup"><span data-stu-id="6a5d9-124">You can change this if needed.</span></span>  
    * <span data-ttu-id="6a5d9-125">อีกทางหนึ่งคือ เลือกแผนกสำหรับตำแหน่งใหม่</span><span class="sxs-lookup"><span data-stu-id="6a5d9-125">Optionally, select the Department for the new positions.</span></span>  
13. <span data-ttu-id="6a5d9-126">คลิก ตกลง</span><span class="sxs-lookup"><span data-stu-id="6a5d9-126">Click OK.</span></span>



[!INCLUDE[footer-include](../includes/footer-banner.md)]