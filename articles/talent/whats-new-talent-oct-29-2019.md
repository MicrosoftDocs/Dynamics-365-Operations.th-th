---
title: มีอะไรใหม่หรือเปลี่ยนไปอย่างไรบ้างใน Dynamics 365 Talent (29 ตุลาคม 2019)
description: หัวข้อนี้อธิบายถึงคุณลักษณะที่ใหม่หรือที่มีการเปลี่ยนแปลง อย่างใดอย่างหนึ่งใน Microsoft Dynamics 365 Talent
author: Darinkramer
manager: AnnBe
ms.date: 10/29/2019
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
ms.search.validFrom: 2019-10-29
ms.dyn365.ops.version: Talent
ms.openlocfilehash: 09d53c82b4244f20d0d7f301691b01263258a32f
ms.sourcegitcommit: e89bb3e5420a6ece84f4e80c11e360b4a042f59d
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 11/17/2020
ms.locfileid: "4529695"
---
# <a name="whats-new-or-changed-in-dynamics-365-talent-october-29-2019"></a><span data-ttu-id="c608b-103">มีอะไรใหม่หรือเปลี่ยนไปอย่างไรบ้างใน Dynamics 365 Talent (29 ตุลาคม 2019)</span><span class="sxs-lookup"><span data-stu-id="c608b-103">What's new or changed in Dynamics 365 Talent (October 29, 2019)</span></span>

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="c608b-104">หัวข้อนี้อธิบายถึงคุณลักษณะที่ใหม่หรือที่มีการเปลี่ยนแปลง อย่างใดอย่างหนึ่ง ใน Dynamics 365 Talent</span><span class="sxs-lookup"><span data-stu-id="c608b-104">This topic describes features that are either new or changed in Dynamics 365 Talent.</span></span>

## <a name="changes-in-attract"></a><span data-ttu-id="c608b-105">การเปลี่ยนแปลงใน Attract</span><span class="sxs-lookup"><span data-stu-id="c608b-105">Changes in Attract</span></span>

<span data-ttu-id="c608b-106">รุ่นนี้ประกอบด้วยการแก้ไขบักรองสำหรับ Dynamics 365 Talent: Attract</span><span class="sxs-lookup"><span data-stu-id="c608b-106">This release includes minor bug fixes for Dynamics 365 Talent: Attract.</span></span>

## <a name="changes-in-onboard"></a><span data-ttu-id="c608b-107">การเปลี่ยนแปลงในการเตรียมความพร้อม</span><span class="sxs-lookup"><span data-stu-id="c608b-107">Changes in Onboard</span></span>

<span data-ttu-id="c608b-108">รุ่นนี้ประกอบด้วยการแก้ไขบักรองสำหรับ Dynamics 365 Talent: Onboard</span><span class="sxs-lookup"><span data-stu-id="c608b-108">This release includes minor bug fixes for Dynamics 365 Talent: Onboard.</span></span>

## <a name="changes-in-core-hr"></a><span data-ttu-id="c608b-109">การเปลี่ยนแปลงใน Core HR</span><span class="sxs-lookup"><span data-stu-id="c608b-109">Changes in Core HR</span></span>

<span data-ttu-id="c608b-110">การเปลี่ยนแปลงที่อธิบายไว้ในส่วนนี้นำไปใช้กับการสร้างหมายเลข 8.1.2586</span><span class="sxs-lookup"><span data-stu-id="c608b-110">Changes described in this section apply to build number 8.1.2586.</span></span> <span data-ttu-id="c608b-111">ตัวเลขในวงเล็บในส่วนหัวบางส่วนอ้างอิงถึงหมายเลขที่สนับสนุนใน Microsoft Dynamics Lifecycle Services (LCS)</span><span class="sxs-lookup"><span data-stu-id="c608b-111">The numbers in parentheses in some headings refer to support numbers in Microsoft Dynamics Lifecycle Services (LCS).</span></span>

### <a name="delete-parties-with-no-roles-should-be-on-by-default-371233"></a><span data-ttu-id="c608b-112">ลบฝ่ายที่ไม่มีบทบาทตามค่าเริ่มต้น (371233)</span><span class="sxs-lookup"><span data-stu-id="c608b-112">Delete parties with no roles should be on by default (371233)</span></span>

<span data-ttu-id="c608b-113">เมื่อคุณจัดเตรียมสภาพแวดล้อมใหม่ใน Talent **ให้ลบฝ่ายออกถ้าไม่มีบทบาท** เปิดอยู่ตามค่าเริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="c608b-113">When you provision a new environment in Talent, **Delete parties if no roles exist** is turned on by default.</span></span> <span data-ttu-id="c608b-114">เมื่อคุณลบผู้ปฏิบัติงาน ฝ่ายที่เชื่อมโยงกับผู้ปฏิบัติงานจะไม่ถูกลบออกเว้นแต่การตั้งค่านี้เปิดอยู่</span><span class="sxs-lookup"><span data-stu-id="c608b-114">When you delete a worker, the party associated with the worker is not removed unless this setting is on.</span></span> <span data-ttu-id="c608b-115">การเปลี่ยนแปลงนี้จะจำกัดเรกคอร์ดที่ซ้ำกันในสมุดที่อยู่สากลเมื่อคุณต้องการนำเข้า เปลี่ยนแปลง หรือนำเข้าผู้ปฏิบัติงานอีกครั้ง</span><span class="sxs-lookup"><span data-stu-id="c608b-115">This change limits duplicate records in the global address book when you need to import, change, or reimport workers.</span></span>

### <a name="draft-and-cancelled-leave-requests-should-be-allowed-to-be-deleted-in-common-data-service-376999"></a><span data-ttu-id="c608b-116">การร้องขอการลางานแบบร่างและการยกเลิกควรถูกลบใน Common Data Service (376999)</span><span class="sxs-lookup"><span data-stu-id="c608b-116">Draft and cancelled leave requests should be allowed to be deleted in Common Data Service (376999)</span></span>

<span data-ttu-id="c608b-117">เมื่อมีการเปลี่ยนแปลงนี้คุณสามารถลบการร้องขอที่มีสถานะเป็น **แบบร่าง** หรือ **ถูกยกเลิก** ใน Common Data Service</span><span class="sxs-lookup"><span data-stu-id="c608b-117">With this change, you can now delete leave requests with a status of **Draft** or **Cancelled** in Common Data Service.</span></span>

### <a name="additional-list-values-in-custom-fields-arent-reflected-in-common-data-service-after-clicking-apply-on-the-custom-fields-form-379599"></a><span data-ttu-id="c608b-118">ค่ารายการเพิ่มเติมในฟิลด์ที่กำหนดเองจะไม่มีผลใน Common Data Service หลังจากที่คลิกใช้บนแบบฟอร์มฟิลด์ที่กำหนดเอง (379599)</span><span class="sxs-lookup"><span data-stu-id="c608b-118">Additional list values in custom fields aren't reflected in Common Data Service after clicking Apply on the Custom fields form (379599)</span></span>

<span data-ttu-id="c608b-119">เมื่อคุณเพิ่มค่ารายการใหม่ไปยังฟิลด์แบบกำหนดเองที่มีอยู่ ซึ่งมีการซิงโครไนส์อยู่แล้วกับ Common Data Service ขณะนี้มีอยู่ใน Common Data Serivce หลังจากที่คุณใช้การเปลี่ยนแปลงในแบบฟอร์ม **ฟิลด์ที่กำหนดเอง**</span><span class="sxs-lookup"><span data-stu-id="c608b-119">When you add new list values to an existing custom field that has already synchronized with Common Data Service, they're now available in Common Data Serivce after you apply your changes in the **Custom fields** form.</span></span>

### <a name="apply-onboarding-checklists-across-legal-entities-when-more-than-one-employment-exists-371270"></a><span data-ttu-id="c608b-120">ใช้รายการตรวจสอบความพร้อมสำหรับนิติบุคคลเมื่อมีการจ้างงานมากกว่าหนึ่งรายการ (371270)</span><span class="sxs-lookup"><span data-stu-id="c608b-120">Apply onboarding checklists across legal entities when more than one employment exists (371270)</span></span>

<span data-ttu-id="c608b-121">ในการนำออกใช้ของสัปดาห์นี้ คุณสามารถใช้รายการตรวจสอบกับพนักงานที่มีการจ้างงานมากกว่าหนึ่งใน **แบบฟอร์มผู้ปฏิบัติงาน > การตรวจสอบ**</span><span class="sxs-lookup"><span data-stu-id="c608b-121">In this week's release, you can apply checklists to employees with more than one employment in **Worker form > Checklists**.</span></span>

### <a name="benefits-open-enrollment-preview-feature-has-been-removed"></a><span data-ttu-id="c608b-122">คุณลักษณะการแสดงตัวอย่างของการลงทะเบียนแบบเปิดของผลประโยชน์ถูกลบออกแล้ว</span><span class="sxs-lookup"><span data-stu-id="c608b-122">Benefits open enrollment preview feature has been removed</span></span>

<span data-ttu-id="c608b-123">ในการเข้าร่วมกับการประกาศของเราในประกาศบล็อก [การลงทุนเชิงกลยุทธ์ในความยอดเยี่ยมในการดำเนินงานของไดรฟ์ Core HR](https://cloudblogs.microsoft.com/dynamics365/bdm/2019/10/02/strategic-investments-in-core-hr-drive-operational-excellence) Microsoft ได้ลบคุณลักษณะการลงทะเบียนแบบเปิดของผลประโยชน์ออกจากการแสดงตัวอย่างสาธารณะ</span><span class="sxs-lookup"><span data-stu-id="c608b-123">In conjunction with our announcement in the [Strategic investments in core HR drive operational excellence](https://cloudblogs.microsoft.com/dynamics365/bdm/2019/10/02/strategic-investments-in-core-hr-drive-operational-excellence) blog post, Microsoft has removed the benefits open enrollment feature from public preview.</span></span> <span data-ttu-id="c608b-124">ฟังก์ชันใหม่จะถูกนำออกใช้ในอนาคตแทน</span><span class="sxs-lookup"><span data-stu-id="c608b-124">New functionality will be released in the future.</span></span> <span data-ttu-id="c608b-125">การใช้งานการผลิตของลักษณะการทำงานที่เปิดรับผลประโยชน์ไม่ได้รับการสนับสนุน</span><span class="sxs-lookup"><span data-stu-id="c608b-125">Production use of the benefits open enrollment feature isn't be supported.</span></span>

## <a name="coming-soon"></a><span data-ttu-id="c608b-126">เร็วๆ นี้</span><span class="sxs-lookup"><span data-stu-id="c608b-126">Coming soon</span></span>

### <a name="print-performance-reviews"></a><span data-ttu-id="c608b-127">พิมพ์การตรวจทานประสิทธิภาพ</span><span class="sxs-lookup"><span data-stu-id="c608b-127">Print performance reviews</span></span>

<span data-ttu-id="c608b-128">ให้ดูที่ [พิมพ์การตรวจทานประสิทธิภาพ](https://docs.microsoft.com/dynamics365-release-plan/2019wave2/dynamics365-talent/print-performance-reviews) ใน Dynamics 365: 2019 แผนเวฟการออกใช้ 2</span><span class="sxs-lookup"><span data-stu-id="c608b-128">See [Print performance reviews](https://docs.microsoft.com/dynamics365-release-plan/2019wave2/dynamics365-talent/print-performance-reviews) in the Dynamics 365: 2019 release wave 2 plan.</span></span>

### <a name="feature-management-workspace"></a><span data-ttu-id="c608b-129">พื้นที่ทำงานการจัดการคุณลักษณะ</span><span class="sxs-lookup"><span data-stu-id="c608b-129">Feature management workspace</span></span>

<span data-ttu-id="c608b-130">จะมีการเพิ่มเติมและปรับปรุงคุณลักษณะทุกครั้งที่นำไปใช้</span><span class="sxs-lookup"><span data-stu-id="c608b-130">Features are added and updated in every release.</span></span> <span data-ttu-id="c608b-131">ประสบการณ์การจัดการคุณลักษณะให้พื้นที่ทำงานที่คุณสามารถดูรายการของคุณลักษณะที่ได้ถูกจัดส่งในการนำออกใช้แต่ละครั้ง</span><span class="sxs-lookup"><span data-stu-id="c608b-131">The feature management experience provides a workspace where you can view a list of features that have been delivered in each release.</span></span> <span data-ttu-id="c608b-132">ตามค่าเริ่มต้น คุณลักษณะใหม่จะถูกปิด</span><span class="sxs-lookup"><span data-stu-id="c608b-132">By default, new features are turned off.</span></span> <span data-ttu-id="c608b-133">คุณสามารถใช้พื้นที่ทำงานเพื่อเปิดและดูเอกสารประกอบได้</span><span class="sxs-lookup"><span data-stu-id="c608b-133">You can use the workspace to turn them on and view the documentation for them.</span></span>

<span data-ttu-id="c608b-134">เมื่อต้องการเรียนรู้เพิ่มเติมเกี่ยวกับการเปลี่ยนแปลงที่มากับการจัดการคุณลักษณะ โปรดดู [ภาพรวมของการจัดการคุณลักษณะ](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview)</span><span class="sxs-lookup"><span data-stu-id="c608b-134">To learn more about the changes coming with feature management, see [Feature management overview](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview).</span></span>
