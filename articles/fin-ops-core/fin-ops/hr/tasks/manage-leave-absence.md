---
title: จัดการกับการลาหยุด
description: 'กระบวนงานนี้นำไปสู่การสร้างเรกคอร์ดการลางานของพนักงาน '
author: andreabichsel
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: HcmWorker, HcmEmploymentLeave
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 002700ae7f6474b48fbe09cb3aaa72e9516b8224
ms.sourcegitcommit: 57e1dafa186fec77ddd8ba9425d238e36e0f0998
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 03/18/2020
ms.locfileid: "3143577"
---
# <a name="manage-leave-of-absence"></a><span data-ttu-id="199c0-103">จัดการกับการลาหยุด</span><span class="sxs-lookup"><span data-stu-id="199c0-103">Manage leave of absence</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="199c0-104">กระบวนงานนี้นำไปสู่การสร้างเรกคอร์ดการลางานของพนักงาน </span><span class="sxs-lookup"><span data-stu-id="199c0-104">This procedure walks through the creation of employee leave records.</span></span> <span data-ttu-id="199c0-105">คุณสามารถติดตามเวลาลางานสำหรับเหตุผลที่รวมถึงกิจกรรมทางการแพทย์ ทางการศึกษา หรือกิจกรรมหลักอื่นๆ </span><span class="sxs-lookup"><span data-stu-id="199c0-105">You can track leave time for reasons that include medical, educational, or parental activities.</span></span> <span data-ttu-id="199c0-106">ข้อมูลบริษัทสาธิตที่ใช้ในการสร้างกระบวนงานนี้คือ USMF</span><span class="sxs-lookup"><span data-stu-id="199c0-106">The demo data company used to create this procedure is USMF.</span></span>

1. <span data-ttu-id="199c0-107">ไปที่ทรัพยากรบุคคล > ผู้ปฏิบัติงาน > พนักงาน</span><span class="sxs-lookup"><span data-stu-id="199c0-107">Go to Human resources > Workers > Employees.</span></span>
2. <span data-ttu-id="199c0-108">ในรายการ ให้เลือกพนักงาน</span><span class="sxs-lookup"><span data-stu-id="199c0-108">In the list, select an employee.</span></span>
3. <span data-ttu-id="199c0-109">แสดงข้อมูลรายละเอียดสำหรับพนักงานที่เลือก โดยการเลือกชื่อของพนักงาน</span><span class="sxs-lookup"><span data-stu-id="199c0-109">Display detailed information for the selected employee by selecting the employee's name.</span></span>
4. <span data-ttu-id="199c0-110">คลิกแท็บการจ้างงาน</span><span class="sxs-lookup"><span data-stu-id="199c0-110">Click the Employment tab.</span></span>
5. <span data-ttu-id="199c0-111">คลิกที่ลางาน</span><span class="sxs-lookup"><span data-stu-id="199c0-111">Click Leave.</span></span>
6. <span data-ttu-id="199c0-112">คลิก สร้าง</span><span class="sxs-lookup"><span data-stu-id="199c0-112">Click New.</span></span>
7. <span data-ttu-id="199c0-113">ในฟิลด์ชนิดการลางาน ให้คลิกปุ่มดรอปดาวน์เพื่อเปิดการค้นหา</span><span class="sxs-lookup"><span data-stu-id="199c0-113">In the Leave type field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="199c0-114">คุณสามารถเชื่อมโยงชนิดการลางานกับรหัสการรายได้ในแบบฟอร์มชนิดการลางาน </span><span class="sxs-lookup"><span data-stu-id="199c0-114">You can associate a leave type to an earning code in the Leave types form.</span></span> <span data-ttu-id="199c0-115">ถ้าชนิดการลางานเชื่อมโยงกับรหัสการรายได้ รายการรายได้จะถูกสร้างขึ้น ด้วยรหัสรายได้ที่เชื่อมโยงกันในระหว่างรอบระยะเวลาการลางานที่คุณป้อน</span><span class="sxs-lookup"><span data-stu-id="199c0-115">If a leave type is associated with an earning code, an earning line will be generated with the associated earning code during the leave period that you enter.</span></span>  
8. <span data-ttu-id="199c0-116">ในรายการ เลือกชนิดของการลางาน</span><span class="sxs-lookup"><span data-stu-id="199c0-116">In the list, select a leave type.</span></span> 
    * <span data-ttu-id="199c0-117">ตัวอย่างเช่น การนำมาใช้</span><span class="sxs-lookup"><span data-stu-id="199c0-117">For example: Adoption</span></span>  
9. <span data-ttu-id="199c0-118">ป้อนวันที่โดยประมาณที่จะเริ่มต้นการลางาน</span><span class="sxs-lookup"><span data-stu-id="199c0-118">Enter the date that the leave will start.</span></span> <span data-ttu-id="199c0-119">ตัวอย่าง: '2015-10-26'</span><span class="sxs-lookup"><span data-stu-id="199c0-119">Example: '2015-10-26'</span></span>
    * <span data-ttu-id="199c0-120">ตัวอย่างเช่น: 26 ตุลาคม 2558</span><span class="sxs-lookup"><span data-stu-id="199c0-120">For example:  2015-10-26</span></span>  
10. <span data-ttu-id="199c0-121">ป้อนวันที่โดยประมาณที่จะเริ่มต้นการลางาน</span><span class="sxs-lookup"><span data-stu-id="199c0-121">Enter the date that the leave will start.</span></span> 
    * <span data-ttu-id="199c0-122">ตัวอย่างเช่น: 20 พฤศจิกายน 2558</span><span class="sxs-lookup"><span data-stu-id="199c0-122">For example:  2015-11-20</span></span>  
11. <span data-ttu-id="199c0-123">ในฟิลด์บันทึก ให้ป้อนคำอธิบาย</span><span class="sxs-lookup"><span data-stu-id="199c0-123">In the note field, enter a description.</span></span>
    * <span data-ttu-id="199c0-124">ตัวอย่างเช่น: ยกเลิกการนำไปใช้</span><span class="sxs-lookup"><span data-stu-id="199c0-124">For example: Leave for adoption</span></span>  
12. <span data-ttu-id="199c0-125">คลิก บันทึก</span><span class="sxs-lookup"><span data-stu-id="199c0-125">Click Save.</span></span>

