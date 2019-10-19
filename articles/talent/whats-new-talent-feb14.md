---
title: มีอะไรใหม่หรือการเปลี่ยนแปลงอะไรใน Dynamics 365 Talent (14 กุมภาพันธ์ 2019)
description: หัวข้อนี้อธิบายถึงคุณลักษณะที่ใหม่หรือที่มีการเปลี่ยนแปลง อย่างใดอย่างหนึ่งใน Microsoft Dynamics 365 Talent
author: Darinkramer
manager: AnnBe
ms.date: 02/14/2019
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
ms.search.validFrom: 2019-02-14
ms.dyn365.ops.version: Talent
ms.openlocfilehash: 9f3fa269217bc03a15fde6ee0fc9d0c502c17b3e
ms.sourcegitcommit: 434dd21450bddcd891aba0555b9853d9ba0afb6f
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 09/23/2019
ms.locfileid: "2009133"
---
# <a name="whats-new-or-changed-in-dynamics-365-talent-february-14-2019"></a><span data-ttu-id="0e5c7-103">มีอะไรใหม่หรือการเปลี่ยนแปลงอะไรใน Dynamics 365 Talent (14 กุมภาพันธ์ 2019)</span><span class="sxs-lookup"><span data-stu-id="0e5c7-103">What's new or changed in Dynamics 365 Talent (February 14, 2019)</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="0e5c7-104">หัวข้อนี้อธิบายถึงคุณลักษณะที่ใหม่หรือที่มีการเปลี่ยนแปลง อย่างใดอย่างหนึ่งใน Talent</span><span class="sxs-lookup"><span data-stu-id="0e5c7-104">This topic describes features that are either new or changed in Talent.</span></span>

## <a name="changes-in-attract"></a><span data-ttu-id="0e5c7-105">การเปลี่ยนแปลงใน Attract</span><span class="sxs-lookup"><span data-stu-id="0e5c7-105">Changes in Attract</span></span>
<span data-ttu-id="0e5c7-106">มีการแก้ไขบักรองที่รวมอยู่กับรุ่นนี้</span><span class="sxs-lookup"><span data-stu-id="0e5c7-106">There are minor bug fixes included with this release.</span></span>

## <a name="changes-in-onboarding"></a><span data-ttu-id="0e5c7-107">การเปลี่ยนแปลงในการเตรียมความพร้อม</span><span class="sxs-lookup"><span data-stu-id="0e5c7-107">Changes in Onboarding</span></span>
<span data-ttu-id="0e5c7-108">มีการแก้ไขบักรองที่รวมอยู่กับรุ่นนี้</span><span class="sxs-lookup"><span data-stu-id="0e5c7-108">There are minor bug fixes included with this release.</span></span>
 
## <a name="changes-in-core-hr"></a><span data-ttu-id="0e5c7-109">การเปลี่ยนแปลงใน Core HR</span><span class="sxs-lookup"><span data-stu-id="0e5c7-109">Changes in Core HR</span></span> 
<span data-ttu-id="0e5c7-110">**สร้าง 8.1.2146**</span><span class="sxs-lookup"><span data-stu-id="0e5c7-110">**Build 8.1.2146**</span></span>

### <a name="employee-fixed-compensation-entity-doesnt-export-all-records"></a><span data-ttu-id="0e5c7-111">เอนทิตีค่าตอบแทนคงที่ของพนักงานไม่ส่งออกเรกคอร์ดทั้งหมด</span><span class="sxs-lookup"><span data-stu-id="0e5c7-111">Employee fixed compensation entity doesn't export all records</span></span>
<span data-ttu-id="0e5c7-112">ด้วยการเปลี่ยนแปลงนี้ เอนทิตี **ค่าตอบแทนคงที่ของพนักงาน** จะส่งออกเรกคอร์ดทั้งหมดในขณะนี้</span><span class="sxs-lookup"><span data-stu-id="0e5c7-112">With this change, the **Employee fixed compensation** entity will now export all records.</span></span> <span data-ttu-id="0e5c7-113">เอนทิตีสามารถถูกใช้เพื่อสร้าง และอัพเดตเรกคอร์ดค่าตอบแทนคงที่ที่มีอยู่สำหรับพนักงาน</span><span class="sxs-lookup"><span data-stu-id="0e5c7-113">The entity can be used to create and update existing fixed compensation records for employees.</span></span> 

### <a name="employment-end-date-doesnt-honor-employee-preferred-time-zone-settings"></a><span data-ttu-id="0e5c7-114">วันสิ้นสุดการจ้างงานไม่ใช้การตั้งค่าโซนเวลาที่ต้องการของพนักงาน</span><span class="sxs-lookup"><span data-stu-id="0e5c7-114">Employment end date doesn't honor employee preferred time zone settings</span></span>
<span data-ttu-id="0e5c7-115">ตอนนี้วันสิ้นสุดการจ้างงานกำลังใช้โซนเวลาที่ต้องการของผู้ใช้ เมื่อสร้างหรือสิ้นสุดการจ้างงานกับบริษัท</span><span class="sxs-lookup"><span data-stu-id="0e5c7-115">Employment end dates are now honoring the user-preferred time zone when creating or ending employment with a company.</span></span>
 
### <a name="uk-addresses-display-in-analytics-as-eastern-switzerland-addresses"></a><span data-ttu-id="0e5c7-116">ที่อยู่ในสหราชอาณาจักรแสดงผลในการวิเคราะห์เป็นที่อยู่ในสวิตเซอร์แลนด์ตะวันออก</span><span class="sxs-lookup"><span data-stu-id="0e5c7-116">UK addresses display in Analytics as Eastern Switzerland addresses</span></span>
<span data-ttu-id="0e5c7-117">ในรุ่นนี้ มีการทำการเปลี่ยนแปลงเพื่อแก้ไขการไม่ตรงแนวในที่อยู่ในรายงาน **การจัดการบุคลากร** "จำนวนพนักงานตามที่ตั้ง"</span><span class="sxs-lookup"><span data-stu-id="0e5c7-117">In this release, a change has been made to correct misalignment in addresses in the **Personnel Management** "Headcount by location" report.</span></span>
 
### <a name="termination-code-is-not-populated-on-the-worker-position-assignment-record-when-ending-the-position"></a><span data-ttu-id="0e5c7-118">ไม่มีการเติมข้อมูลรหัสการเลิกจ้างในเรกคอร์ดการมอบหมายตำแหน่งงานของผู้ปฏิบัติงาน เมื่อสิ้นสุดตำแหน่ง</span><span class="sxs-lookup"><span data-stu-id="0e5c7-118">Termination code is not populated on the worker position assignment record when ending the position</span></span>
<span data-ttu-id="0e5c7-119">มีการทำการเปลี่ยนแปลงเป็นค่าเริ่มต้นของรหัส "เหตุผลการสิ้นสุดการจ้างงาน" เมื่อสิ้นสุดการมอบหมายตำแหน่งงานของผู้ปฏิบัติงาน</span><span class="sxs-lookup"><span data-stu-id="0e5c7-119">A change has been made to default the "Termination reason" code when ending the employees position assignment.</span></span>

### <a name="new-entity-created-for-job-compensation-levels"></a><span data-ttu-id="0e5c7-120">เอนทิตีใหม่ที่สร้างขึ้นสำหรับระดับค่าตอบแทนของงาน</span><span class="sxs-lookup"><span data-stu-id="0e5c7-120">New entity created for job compensation levels</span></span>
<span data-ttu-id="0e5c7-121">เอนทิตีกรอบงานการจัดการข้อมูลใหม่ (DMF) ถูกสร้างขึ้น</span><span class="sxs-lookup"><span data-stu-id="0e5c7-121">A new data management framework (DMF) entity was created.</span></span> <span data-ttu-id="0e5c7-122">เอนทิตีแสดงสำหรับการสร้างและการปรับปรุงไปยังระดับค่าตอบแทน มูลค่าตลาด และข้อมูลการสำรวจความคิดเห็น สำหรับงานแต่ละงานที่กำหนดไว้ในระบบ</span><span class="sxs-lookup"><span data-stu-id="0e5c7-122">The entity provides for creation and updates to compensation levels, market values, and survey information for each job defined in the system.</span></span>
