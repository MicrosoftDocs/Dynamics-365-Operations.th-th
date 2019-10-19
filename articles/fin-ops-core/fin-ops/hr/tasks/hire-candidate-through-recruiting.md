---
title: การจ้างงานผู้สมัครผ่านการสรรหาบุคลากร
description: 'ขั้นตอนนี้ช่วยให้ผู้สรรหาการจ้างงานผู้สมัครที่ส่งใบสมัครโดยใช้โครงการสรรหาบุคลากรที่เฉพาะเจาะจง '
author: andreabichsel
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: HRMApplication, HcmWorkerNewWorker, HcmPositionLookup, HcmWorker, HcmPosition, HcmPositionDateManager,  DefaultDashboard
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: f56769abb4da0068d6e2916df8dc782e662a2d56
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 09/27/2019
ms.locfileid: "2190407"
---
# <a name="hiring-candidate-through-recruiting"></a><span data-ttu-id="9b8e4-103">การจ้างงานผู้สมัครผ่านการสรรหาบุคลากร</span><span class="sxs-lookup"><span data-stu-id="9b8e4-103">Hiring candidate through recruiting</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="9b8e4-104">ขั้นตอนนี้ช่วยให้ผู้สรรหาการจ้างงานผู้สมัครที่ส่งใบสมัครโดยใช้โครงการสรรหาบุคลากรที่เฉพาะเจาะจง </span><span class="sxs-lookup"><span data-stu-id="9b8e4-104">This procedure enables a recruiter to hire an applicant who submitted an application through a specific recruitment project.</span></span> <span data-ttu-id="9b8e4-105">เมื่อคุณจ้างงานผู้สมัครผ่านทางโครงการสรรหาบุคลากร เรกคอร์ดผู้ปฏิบัติงานใหม่จะถูกสร้างขึ้น และเรกคอร์ดของผู้สมัครจะมีสถานะของการจ้างงาน </span><span class="sxs-lookup"><span data-stu-id="9b8e4-105">When you hire an applicant through a recruiting project, a new worker record will be created and the applicant’s record will have a status of Employed.</span></span> <span data-ttu-id="9b8e4-106">ข้อมูลบริษัทสาธิตที่ใช้ในการสร้างกระบวนงานนี้คือ USMF</span><span class="sxs-lookup"><span data-stu-id="9b8e4-106">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="9b8e4-107">เพื่อดำเนินกระบวนงานนี้ให้เสร็จสมบูรณ์ นำทางไปยังทรัพยากรบุคคล > การสรรหาบุคลากร > แอพลิเคชัน > แอพลิเคชัน</span><span class="sxs-lookup"><span data-stu-id="9b8e4-107">To complete this procedure, navigate to Human resources > Recruitment > Applications >Applications</span></span> 

1. <span data-ttu-id="9b8e4-108">เลือกใบสมัครสำหรับผู้สมัครภายนอก</span><span class="sxs-lookup"><span data-stu-id="9b8e4-108">Select an Application for an External applicant</span></span>
2. <span data-ttu-id="9b8e4-109">ในรายการนี้ ให้คลิกลิงค์ในแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="9b8e4-109">In the list, click the link in the selected row.</span></span>
3. <span data-ttu-id="9b8e4-110">คลิก สถานะใบสมัคร</span><span class="sxs-lookup"><span data-stu-id="9b8e4-110">Click Application status.</span></span>
4. <span data-ttu-id="9b8e4-111">คลิกการจ้างงานผู้ปฏิบัติงานใหม่</span><span class="sxs-lookup"><span data-stu-id="9b8e4-111">Click Hire new worker.</span></span>
5. <span data-ttu-id="9b8e4-112">ในฟิลด์วันที่เริ่มการจ้างงาน ให้ป้อนวันที่และเวลา</span><span class="sxs-lookup"><span data-stu-id="9b8e4-112">In the Employment start date field, enter a date and time.</span></span>
6. <span data-ttu-id="9b8e4-113">ในฟิลด์ตำแหน่ง ให้คลิกปุ่มดรอปดาวน์เพื่อเปิดการค้นหา</span><span class="sxs-lookup"><span data-stu-id="9b8e4-113">In the Position field, click the drop-down button to open the lookup.</span></span>
7. <span data-ttu-id="9b8e4-114">ในรายการนี้ ให้คลิกลิงค์ในแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="9b8e4-114">In the list, click the link in the selected row.</span></span>
8. <span data-ttu-id="9b8e4-115">ในฟิลด์การเริ่มหน้าที่ที่ได้รับมอบหมาย ให้ป้อนวันที่และเวลา</span><span class="sxs-lookup"><span data-stu-id="9b8e4-115">In the Assignment start field, enter a date and time.</span></span>
9. <span data-ttu-id="9b8e4-116">คลิกการจ้างงานผู้ปฏิบัติงานใหม่</span><span class="sxs-lookup"><span data-stu-id="9b8e4-116">Click Hire new worker.</span></span>
10. <span data-ttu-id="9b8e4-117">ขยายประวัติการจ้างงานของกล่องแสดงข้อมูลย่อ</span><span class="sxs-lookup"><span data-stu-id="9b8e4-117">Expand the Employment history FactBox.</span></span>
11. <span data-ttu-id="9b8e4-118">ขยายตำแหน่งปัจจุบันของกล่องแสดงข้อมูลย่อ</span><span class="sxs-lookup"><span data-stu-id="9b8e4-118">Expand the Current positions FactBox.</span></span>
12. <span data-ttu-id="9b8e4-119">ขยายประวัติการจ้างงานของกล่องแสดงข้อมูลย่อ</span><span class="sxs-lookup"><span data-stu-id="9b8e4-119">Expand the Employment history FactBox.</span></span>
13. <span data-ttu-id="9b8e4-120">ขยายตำแหน่งปัจจุบันของกล่องแสดงข้อมูลย่อ</span><span class="sxs-lookup"><span data-stu-id="9b8e4-120">Expand the Current positions FactBox.</span></span>
14. <span data-ttu-id="9b8e4-121">ขยายหรือยุบส่วนของที่อยู่ </span><span class="sxs-lookup"><span data-stu-id="9b8e4-121">Expand or collapse the Addresses section.</span></span>
15. <span data-ttu-id="9b8e4-122">ขยายหรือยุบส่วนของข้อมูลผู้ติดต่อ</span><span class="sxs-lookup"><span data-stu-id="9b8e4-122">Expand or collapse the Contact information section.</span></span>
16. <span data-ttu-id="9b8e4-123">ขยายหรือยุบส่วนของข้อมูลส่วนบุคคล</span><span class="sxs-lookup"><span data-stu-id="9b8e4-123">Expand or collapse the Personal information section.</span></span>

