---
title: จัดการวันหมดอายุของสวัสดิการ
description: 'ขั้นตอนนี้แสดงวิธีการหมดอายุ หรือขยายสวัสดิการ และจัดการวันลงทะเบียนของผู้ปฏิบัติงานที่ลงทะเบียนในสวัสดิการ '
author: andreabichsel
manager: AnnBe
ms.date: 02/03/2020
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: HcmBenefit, HcmMassBenefitExpiration, HcmMassBenefitExpirationResults, HcmWorker, HcmWorkerEnrollment, BenefitWorkspace, HcmBenefitSummaryPart
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Core, Operations, Human Resources
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Version 7.0.0, Human Resources
ms.openlocfilehash: 7332a95e1cd558336dc19bcb269ef89ce3721aa9
ms.sourcegitcommit: ba340f836e472f13f263dec46a49847c788fca44
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 06/04/2020
ms.locfileid: "3429462"
---
# <a name="manage-benefit-expiration-dates"></a><span data-ttu-id="e4180-103">จัดการวันหมดอายุของสวัสดิการ</span><span class="sxs-lookup"><span data-stu-id="e4180-103">Manage benefit expiration dates</span></span>

<span data-ttu-id="e4180-104">ขั้นตอนนี้แสดงวิธีการหมดอายุ หรือขยายสวัสดิการ และจัดการวันลงทะเบียนของผู้ปฏิบัติงานที่ลงทะเบียนในสวัสดิการ </span><span class="sxs-lookup"><span data-stu-id="e4180-104">This procedure shows how you can expire or extend a benefit, and manage the enrollment dates of workers that are enrolled in the benefit.</span></span> <span data-ttu-id="e4180-105">ข้อมูลบริษัทสาธิตที่ใช้ในการสร้างกระบวนงานนี้คือ USMF</span><span class="sxs-lookup"><span data-stu-id="e4180-105">The demo data company used to create this procedure is USMF.</span></span>

## <a name="benefit-expiration-dates"></a><span data-ttu-id="e4180-106">วันหมดอายุของสวัสดิการ</span><span class="sxs-lookup"><span data-stu-id="e4180-106">Benefit expiration dates</span></span>

1. <span data-ttu-id="e4180-107">ไปที่ทรัพยากรบุคคล > สวัสดิการ > สวัสดิการ</span><span class="sxs-lookup"><span data-stu-id="e4180-107">Go to Human resources > Benefits > Benefits.</span></span>
2. <span data-ttu-id="e4180-108">ขยายกล่องแสดงข้อมูลย่อของผู้ปฏิบัติงานที่ลงทะเบียน</span><span class="sxs-lookup"><span data-stu-id="e4180-108">Expand the Enrolled workers FactBox.</span></span>
3. <span data-ttu-id="e4180-109">ในรายการนี้ ให้ค้นหาและเลือกเรกคอร์ดที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="e4180-109">In the list, find and select the desired record.</span></span>
4. <span data-ttu-id="e4180-110">ในบานหน้าต่างการดำเนินการ คลิกสวัสดิการ</span><span class="sxs-lookup"><span data-stu-id="e4180-110">On the Action Pane, click Benefit.</span></span>
5. <span data-ttu-id="e4180-111">คลิก หมดอายุหรือขยายสวัสดิการ</span><span class="sxs-lookup"><span data-stu-id="e4180-111">Click Expire or extend benefits.</span></span>
6. <span data-ttu-id="e4180-112">ในฟิลด์วันหมดอายุสวัสดิการใหม่ ป้อนวันและเวลา</span><span class="sxs-lookup"><span data-stu-id="e4180-112">In the New benefit expiration date field, enter a date and time.</span></span>
7. <span data-ttu-id="e4180-113">คลิก หมดอายุ</span><span class="sxs-lookup"><span data-stu-id="e4180-113">Click Expire.</span></span>
8. <span data-ttu-id="e4180-114">ในบานหน้าต่างการดำเนินการ คลิกสวัสดิการ </span><span class="sxs-lookup"><span data-stu-id="e4180-114">On the Action Pane, click Benefit.</span></span>
9. <span data-ttu-id="e4180-115">คลิก การหมดอายุของสวัสดิการและผลลัพธ์ของการขยาย</span><span class="sxs-lookup"><span data-stu-id="e4180-115">Click Benefit expiration and extension results.</span></span>
10. <span data-ttu-id="e4180-116">ในรายการนี้ ให้ทำเครื่องหมายแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="e4180-116">In the list, mark the selected row.</span></span>
11. <span data-ttu-id="e4180-117">ในรายการนี้ ให้คลิกลิงค์ผู้ปฏิบัติงานที่ได้รับผล</span><span class="sxs-lookup"><span data-stu-id="e4180-117">In the list, click the Workers affected link.</span></span>
12. <span data-ttu-id="e4180-118">ในรายการนี้ ให้ค้นหาและเลือกเรกคอร์ดที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="e4180-118">In the list, find and select the desired record.</span></span>
13. <span data-ttu-id="e4180-119">คลิกเพื่อติดตามลิงค์ในฟิลด์หมายเลขบุคคลากร </span><span class="sxs-lookup"><span data-stu-id="e4180-119">Click to follow the link in the Personnel number field.</span></span>
14. <span data-ttu-id="e4180-120">ขยายส่วนข้อมูลส่วนบุคคล</span><span class="sxs-lookup"><span data-stu-id="e4180-120">Expand the Personal information section.</span></span>
15. <span data-ttu-id="e4180-121">คลิก สวัสดิการ</span><span class="sxs-lookup"><span data-stu-id="e4180-121">Click Benefits.</span></span>
16. <span data-ttu-id="e4180-122">ในรายการ ค้นหาสวัสดิการและเลือกเรกคอร์ด </span><span class="sxs-lookup"><span data-stu-id="e4180-122">In the list, find the benefit and select the record.</span></span> <span data-ttu-id="e4180-123">หมายเหตุวันที่ที่สิ้นสุดความคุ้มครองใหม่</span><span class="sxs-lookup"><span data-stu-id="e4180-123">Note the new coverage end date.</span></span>

