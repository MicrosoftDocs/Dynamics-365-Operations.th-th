---
title: จัดการกับการลาหยุด
description: 'กระบวนงานนี้นำไปสู่การสร้างเรกคอร์ดการลางานของพนักงาน '
author: ShielaSogge
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: HcmWorker, HcmEmploymentLeave
audience: Application User
ms.reviewer: rschloma
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shielas
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 7687d31fbf73a02b1b924d092e77ac28b573e694
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 01/29/2019
ms.locfileid: "337980"
---
# <a name="manage-leave-of-absence"></a><span data-ttu-id="26e2f-103">จัดการกับการลาหยุด</span><span class="sxs-lookup"><span data-stu-id="26e2f-103">Manage leave of absence</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="26e2f-104">กระบวนงานนี้นำไปสู่การสร้างเรกคอร์ดการลางานของพนักงาน </span><span class="sxs-lookup"><span data-stu-id="26e2f-104">This procedure walks through the creation of employee leave records.</span></span> <span data-ttu-id="26e2f-105">คุณสามารถติดตามเวลาลางานสำหรับเหตุผลที่รวมถึงกิจกรรมทางการแพทย์ ทางการศึกษา หรือกิจกรรมหลักอื่นๆ </span><span class="sxs-lookup"><span data-stu-id="26e2f-105">You can track leave time for reasons that include medical, educational, or parental activities.</span></span> <span data-ttu-id="26e2f-106">ข้อมูลบริษัทสาธิตที่ใช้ในการสร้างกระบวนงานนี้คือ USMF</span><span class="sxs-lookup"><span data-stu-id="26e2f-106">The demo data company used to create this procedure is USMF.</span></span>

1. <span data-ttu-id="26e2f-107">ไปที่ทรัพยากรบุคคล > ผู้ปฏิบัติงาน > พนักงาน</span><span class="sxs-lookup"><span data-stu-id="26e2f-107">Go to Human resources > Workers > Employees.</span></span>
2. <span data-ttu-id="26e2f-108">ในรายการ ให้เลือกพนักงาน</span><span class="sxs-lookup"><span data-stu-id="26e2f-108">In the list, select an employee.</span></span>
3. <span data-ttu-id="26e2f-109">แสดงข้อมูลรายละเอียดสำหรับพนักงานที่เลือก โดยการเลือกชื่อของพนักงาน</span><span class="sxs-lookup"><span data-stu-id="26e2f-109">Display detailed information for the selected employee by selecting the employee's name.</span></span>
4. <span data-ttu-id="26e2f-110">คลิกแท็บการจ้างงาน</span><span class="sxs-lookup"><span data-stu-id="26e2f-110">Click the Employment tab.</span></span>
5. <span data-ttu-id="26e2f-111">คลิกที่ลางาน</span><span class="sxs-lookup"><span data-stu-id="26e2f-111">Click Leave.</span></span>
6. <span data-ttu-id="26e2f-112">คลิก สร้าง</span><span class="sxs-lookup"><span data-stu-id="26e2f-112">Click New.</span></span>
7. <span data-ttu-id="26e2f-113">ในฟิลด์ชนิดการลางาน ให้คลิกปุ่มดรอปดาวน์เพื่อเปิดการค้นหา</span><span class="sxs-lookup"><span data-stu-id="26e2f-113">In the Leave type field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="26e2f-114">คุณสามารถเชื่อมโยงชนิดการลางานกับรหัสการรายได้ในแบบฟอร์มชนิดการลางาน </span><span class="sxs-lookup"><span data-stu-id="26e2f-114">You can associate a leave type to an earning code in the Leave types form.</span></span> <span data-ttu-id="26e2f-115">ถ้าชนิดการลางานเชื่อมโยงกับรหัสการรายได้ รายการรายได้จะถูกสร้างขึ้น ด้วยรหัสรายได้ที่เชื่อมโยงกันในระหว่างรอบระยะเวลาการลางานที่คุณป้อน</span><span class="sxs-lookup"><span data-stu-id="26e2f-115">If a leave type is associated with an earning code, an earning line will be generated with the associated earning code during the leave period that you enter.</span></span>  
8. <span data-ttu-id="26e2f-116">ในรายการ เลือกชนิดของการลางาน</span><span class="sxs-lookup"><span data-stu-id="26e2f-116">In the list, select a leave type.</span></span> 
    * <span data-ttu-id="26e2f-117">ตัวอย่างเช่น การนำมาใช้</span><span class="sxs-lookup"><span data-stu-id="26e2f-117">For example: Adoption</span></span>  
9. <span data-ttu-id="26e2f-118">ป้อนวันที่โดยประมาณที่จะเริ่มต้นการลางาน</span><span class="sxs-lookup"><span data-stu-id="26e2f-118">Enter the date that the leave will start.</span></span> <span data-ttu-id="26e2f-119">ตัวอย่าง: '2015-10-26'</span><span class="sxs-lookup"><span data-stu-id="26e2f-119">Example: '2015-10-26'</span></span>
    * <span data-ttu-id="26e2f-120">ตัวอย่างเช่น: 26 ตุลาคม 2558</span><span class="sxs-lookup"><span data-stu-id="26e2f-120">For example:  2015-10-26</span></span>  
10. <span data-ttu-id="26e2f-121">ป้อนวันที่โดยประมาณที่จะเริ่มต้นการลางาน</span><span class="sxs-lookup"><span data-stu-id="26e2f-121">Enter the date that the leave will start.</span></span> 
    * <span data-ttu-id="26e2f-122">ตัวอย่างเช่น: 20 พฤศจิกายน 2558</span><span class="sxs-lookup"><span data-stu-id="26e2f-122">For example:  2015-11-20</span></span>  
11. <span data-ttu-id="26e2f-123">ในฟิลด์บันทึก ให้ป้อนคำอธิบาย</span><span class="sxs-lookup"><span data-stu-id="26e2f-123">In the note field, enter a description.</span></span>
    * <span data-ttu-id="26e2f-124">ตัวอย่างเช่น: ยกเลิกการนำไปใช้</span><span class="sxs-lookup"><span data-stu-id="26e2f-124">For example: Leave for adoption</span></span>  
12. <span data-ttu-id="26e2f-125">คลิก บันทึก</span><span class="sxs-lookup"><span data-stu-id="26e2f-125">Click Save.</span></span>

