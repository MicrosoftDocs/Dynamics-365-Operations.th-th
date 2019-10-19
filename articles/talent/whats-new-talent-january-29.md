---
title: มีอะไรใหม่หรือการเปลี่ยนแปลงอะไรใน Dynamics 365 Talent (31 มกราคม 2019)
description: หัวข้อนี้อธิบายถึงคุณลักษณะที่ใหม่หรือที่มีการเปลี่ยนแปลง อย่างใดอย่างหนึ่งใน Microsoft Dynamics 365 Talent
author: Darinkramer
manager: AnnBe
ms.date: 01/31/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: dkrame
ms.search.validFrom: 2019-01-29
ms.dyn365.ops.version: Talent
ms.openlocfilehash: 6dcdb37ba7a423e54a641c1d123f563a59648d46
ms.sourcegitcommit: 434dd21450bddcd891aba0555b9853d9ba0afb6f
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 09/23/2019
ms.locfileid: "2010325"
---
# <a name="whats-new-or-changed-in-dynamics-365-talent-january-31-2019"></a><span data-ttu-id="2323a-103">มีอะไรใหม่หรือการเปลี่ยนแปลงอะไรใน Dynamics 365 Talent (31 มกราคม 2019)</span><span class="sxs-lookup"><span data-stu-id="2323a-103">What's new or changed in Dynamics 365 Talent (January 31, 2019)</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="2323a-104">หัวข้อนี้อธิบายถึงคุณลักษณะที่ใหม่หรือที่มีการเปลี่ยนแปลง อย่างใดอย่างหนึ่ง ใน Dynamics 365 Talent</span><span class="sxs-lookup"><span data-stu-id="2323a-104">This topic describes features that are either new or changed in Dynamics 365 Talent.</span></span>

<span data-ttu-id="2323a-105">**สร้าง 8.1.2128**</span><span class="sxs-lookup"><span data-stu-id="2323a-105">**Build 8.1.2128**</span></span>

## <a name="core-hr-changes"></a><span data-ttu-id="2323a-106">การเปลี่ยนแปลงของ Core HR</span><span class="sxs-lookup"><span data-stu-id="2323a-106">Core HR Changes</span></span>

### <a name="time-off-taken-on-leave-people-card-doesnt-consider-leave-plan-dates"></a><span data-ttu-id="2323a-107">บัตรบุคคลของเวลาหยุดพักที่ใช้ขณะลางานไม่ถือว่าเป็นวันที่ของแผนการลางาน</span><span class="sxs-lookup"><span data-stu-id="2323a-107">Time off taken on leave people card doesn't consider leave plan dates</span></span>
<span data-ttu-id="2323a-108">สำหรับชนิดของการลางานที่มีแผนซึ่งไม่ได้รันในปีปฏิทิน การ์ด **ใช้แล้ว** จะแสดงเวลาหยุดพักที่จะนำมานับในปีที่กำหนดแผนการลางานไว้</span><span class="sxs-lookup"><span data-stu-id="2323a-108">For those that have leave plans that don’t run on a calendar year, the **Taken** card now displays time off that’s been taken in the plan-defined leave year.</span></span> <span data-ttu-id="2323a-109">ตัวอย่างเช่น ถ้าปีหยุดงานขององค์กรเป็นวันที่ 1 มิถุนายนถึงวันที่ 30 พฤษภาคม และพนักงานใช้วันลาหยุดไป 3 วันแล้วในเดือนธันวาคม การ์ด **ใช้แล้ว** ในวันที่ 15 มกราคม จะแสดงเป็น 3 วัน</span><span class="sxs-lookup"><span data-stu-id="2323a-109">For example, if an organization’s leave year is June 1 through May 30 and an employee has taken 3 days off in December, the **Taken** card on January 15, will display 3 days.</span></span> 

### <a name="accrual-amounts-not-matching-tier-date-basis"></a><span data-ttu-id="2323a-110">ยอดเงินตามเกณฑ์คงค้างไม่ตรงกับพื้นฐานวันที่ของระดับ</span><span class="sxs-lookup"><span data-stu-id="2323a-110">Accrual amounts not matching tier date basis</span></span>
<span data-ttu-id="2323a-111">มีการเพิ่มตัวเลือกใหม่ในการลางานและการขาดงาน (พารามิเตอร์ **ทรัพยากรบุคคล**) เพื่อให้ลูกค้าสามารถกำหนดว่าเมื่อใดที่มีผลบังคับใช้ของเดือนของพนักงานของวันที่ให้บริการ</span><span class="sxs-lookup"><span data-stu-id="2323a-111">New options have been added to leave and absence (**Human resources** parameters) to enable customers to determine when employees’ months of service date are effective.</span></span> <span data-ttu-id="2323a-112">สำหรับบางองค์กร วันที่เป็นวันสิ้นสุดของเดือน แต่บางองค์กรอาจเป็นวันเริ่มต้นของเดือนถัดไป</span><span class="sxs-lookup"><span data-stu-id="2323a-112">For some organizations, the date is the end of the month, but for others it may be the start of the next month.</span></span> <span data-ttu-id="2323a-113">ตัวอย่างเช่น องค์กรหนึ่งอาจให้เวลาหยุดงานในวันที่ 31 ธันวาคม ในขณะที่อีกองค์กรหนึ่งอาจให้เวลาหยุดงานเป็นวันที่ 1 มกราคม</span><span class="sxs-lookup"><span data-stu-id="2323a-113">For example, one organization may award time off on December 31, while another may award time off on January 1.</span></span> <span data-ttu-id="2323a-114">ตัวเลือกนี้จะช่วยให้คุณสามารถเลือกได้ว่าควรมีการให้เวลาหยุดงานเมื่อใด</span><span class="sxs-lookup"><span data-stu-id="2323a-114">This option will allow you to choose when the award should occur.</span></span> 

### <a name="worker-hire-actions-are-stuck-in-workflow-complete-state"></a><span data-ttu-id="2323a-115">การดำเนินการจ้างงานของผู้ปฏิบัติงานติดอยู่ในสถานะ "ลำดับงานเสร็จสมบูรณ์"</span><span class="sxs-lookup"><span data-stu-id="2323a-115">Worker hire actions are stuck in "Workflow complete" state</span></span>
<span data-ttu-id="2323a-116">มีการเปลี่ยนแปลงเพื่อแก้ไขปัญหาที่มีลำดับงานจำนวนน้อยที่เสร็จสิ้นโดยมีสถานะเป็น "ลำดับงานเสร็จสมบูรณ์"</span><span class="sxs-lookup"><span data-stu-id="2323a-116">Changes have been made to correct an issue where a small number of workflows finished with a "Workflow complete" status.</span></span> <span data-ttu-id="2323a-117">ในตอนนี้ลำดับงานใหม่ควรย้ายไปเป็นสถานะ "เสร็จสมบูรณ์" เมื่อลำดับงานเสร็จสิ้น</span><span class="sxs-lookup"><span data-stu-id="2323a-117">New workflows should now move to a "Completed" state when the workflow finishes.</span></span> <span data-ttu-id="2323a-118">ลำดับงานใด ๆ ในสถานะลำดับงานที่เสร็จสมบูรณ์จะถูกเปลี่ยนเป็นสถานะข้อผิดพลาดเพื่ออนุญาตให้มีการอัพเดตหรือการลบถ้าจำเป็น</span><span class="sxs-lookup"><span data-stu-id="2323a-118">Any workflows in a workflow completed status will be transitioned to an error status to allow for updating or removal if required.</span></span> 
