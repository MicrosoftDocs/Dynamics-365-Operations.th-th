--- 
title: "จัดการวันหมดอายุของสวัสดิการ"
description: "ขั้นตอนนี้แสดงวิธีการหมดอายุ หรือขยายสวัสดิการ และจัดการวันลงทะเบียนของผู้ปฏิบัติงานที่ลงทะเบียนในสวัสดิการ "
author: ShielaSogge
manager: AnnBe
ms.date: 8/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: HcmBenefit, HcmMassBenefitExpiration, HcmMassBenefitExpirationResults, HcmWorker, HcmWorkerEnrollment
audience: Application User
ms.reviewer: rschloma
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shielas
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 32d71167fdad65cb1dec37671999a497759ca484
ms.openlocfilehash: a06022ba097341066c2b44ce8b14ac990a41a088
ms.contentlocale: th-th
ms.lasthandoff: 09/11/2018

---
# <a name="manage-benefit-expiration-dates"></a><span data-ttu-id="3067f-103">จัดการวันหมดอายุของสวัสดิการ</span><span class="sxs-lookup"><span data-stu-id="3067f-103">Manage benefit expiration dates</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="3067f-104">ขั้นตอนนี้แสดงวิธีการหมดอายุ หรือขยายสวัสดิการ และจัดการวันลงทะเบียนของผู้ปฏิบัติงานที่ลงทะเบียนในสวัสดิการ </span><span class="sxs-lookup"><span data-stu-id="3067f-104">This procedure shows how you can expire or extend a benefit, and manage the enrollment dates of workers that are enrolled in the benefit.</span></span> <span data-ttu-id="3067f-105">ข้อมูลบริษัทสาธิตที่ใช้ในการสร้างกระบวนงานนี้คือ USMF</span><span class="sxs-lookup"><span data-stu-id="3067f-105">The demo data company used to create this procedure is USMF.</span></span>


## <a name="benefit-expiration-dates"></a><span data-ttu-id="3067f-106">วันหมดอายุของสวัสดิการ</span><span class="sxs-lookup"><span data-stu-id="3067f-106">Benefit expiration dates</span></span>
1. <span data-ttu-id="3067f-107">ไปที่ทรัพยากรบุคคล > สวัสดิการ > สวัสดิการ</span><span class="sxs-lookup"><span data-stu-id="3067f-107">Go to Human resources > Benefits > Benefits.</span></span>
2. <span data-ttu-id="3067f-108">ขยายกล่องแสดงข้อมูลย่อของผู้ปฏิบัติงานที่ลงทะเบียน</span><span class="sxs-lookup"><span data-stu-id="3067f-108">Expand the Enrolled workers FactBox.</span></span>
3. <span data-ttu-id="3067f-109">ในรายการนี้ ให้ค้นหาและเลือกเรกคอร์ดที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="3067f-109">In the list, find and select the desired record.</span></span>
4. <span data-ttu-id="3067f-110">ในบานหน้าต่างการดำเนินการ คลิกสวัสดิการ</span><span class="sxs-lookup"><span data-stu-id="3067f-110">On the Action Pane, click Benefit.</span></span>
5. <span data-ttu-id="3067f-111">คลิก หมดอายุหรือขยายสวัสดิการ</span><span class="sxs-lookup"><span data-stu-id="3067f-111">Click Expire or extend benefits.</span></span>
6. <span data-ttu-id="3067f-112">ในฟิลด์วันหมดอายุสวัสดิการใหม่ ป้อนวันและเวลา</span><span class="sxs-lookup"><span data-stu-id="3067f-112">In the New benefit expiration date field, enter a date and time.</span></span>
7. <span data-ttu-id="3067f-113">คลิก หมดอายุ</span><span class="sxs-lookup"><span data-stu-id="3067f-113">Click Expire.</span></span>
8. <span data-ttu-id="3067f-114">ในบานหน้าต่างการดำเนินการ คลิกสวัสดิการ </span><span class="sxs-lookup"><span data-stu-id="3067f-114">On the Action Pane, click Benefit.</span></span>
9. <span data-ttu-id="3067f-115">คลิก การหมดอายุของสวัสดิการและผลลัพธ์ของการขยาย</span><span class="sxs-lookup"><span data-stu-id="3067f-115">Click Benefit expiration and extension results.</span></span>
10. <span data-ttu-id="3067f-116">ในรายการนี้ ให้ทำเครื่องหมายแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="3067f-116">In the list, mark the selected row.</span></span>
11. <span data-ttu-id="3067f-117">ในรายการนี้ ให้คลิกลิงค์ผู้ปฏิบัติงานที่ได้รับผล</span><span class="sxs-lookup"><span data-stu-id="3067f-117">In the list, click the Workers affected link.</span></span>
12. <span data-ttu-id="3067f-118">ในรายการนี้ ให้ค้นหาและเลือกเรกคอร์ดที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="3067f-118">In the list, find and select the desired record.</span></span>
13. <span data-ttu-id="3067f-119">คลิกเพื่อติดตามลิงค์ในฟิลด์หมายเลขบุคคลากร </span><span class="sxs-lookup"><span data-stu-id="3067f-119">Click to follow the link in the Personnel number field.</span></span>
14. <span data-ttu-id="3067f-120">ขยายส่วนข้อมูลส่วนบุคคล</span><span class="sxs-lookup"><span data-stu-id="3067f-120">Expand the Personal information section.</span></span>
15. <span data-ttu-id="3067f-121">คลิก สวัสดิการ</span><span class="sxs-lookup"><span data-stu-id="3067f-121">Click Benefits.</span></span>
16. <span data-ttu-id="3067f-122">ในรายการ ค้นหาสวัสดิการและเลือกเรกคอร์ด </span><span class="sxs-lookup"><span data-stu-id="3067f-122">In the list, find the benefit and select the record.</span></span> <span data-ttu-id="3067f-123">หมายเหตุวันที่ที่สิ้นสุดความคุ้มครองใหม่</span><span class="sxs-lookup"><span data-stu-id="3067f-123">Note the new coverage end date.</span></span>


