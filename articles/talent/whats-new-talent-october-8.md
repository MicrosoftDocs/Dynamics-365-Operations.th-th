---
title: มีอะไรใหม่หรือเปลี่ยนแปลงใน Dynamics 365 for Talent Core HR (8 ตุลาคม 2018)
description: หัวข้อนี้อธิบายคุณลักษณะที่ใหม่หรือเปลี่ยนแปลงใน Microsoft Dynamics 365 for Talent Core HR
author: Darinkramer
manager: AnnBe
ms.date: 10/07/2018
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
ms.search.validFrom: 2018-10-07
ms.dyn365.ops.version: Talent
ms.openlocfilehash: 34216e2181915cf615e6e77fa2a10d06a4e9db85
ms.sourcegitcommit: aec1dcd44274e9b8d0770836598fde5533b7b569
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 06/03/2019
ms.locfileid: "1617283"
---
# <a name="whats-new-or-changed-in-dynamics-365-for-talent-core-hr-october-8-2018"></a><span data-ttu-id="f59e1-103">มีอะไรใหม่หรือเปลี่ยนแปลงใน Dynamics 365 for Talent Core HR (8 ตุลาคม 2018)</span><span class="sxs-lookup"><span data-stu-id="f59e1-103">What's new or changed in Dynamics 365 for Talent Core HR (October 8, 2018)</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="f59e1-104">**สร้าง 8.1.1050.0**</span><span class="sxs-lookup"><span data-stu-id="f59e1-104">**Build 8.1.1050.0**</span></span>

<span data-ttu-id="f59e1-105">หัวข้อนี้อธิบายถึงคุณลักษณะที่ใหม่หรือที่มีการเปลี่ยนแปลง อย่างใดอย่างหนึ่งใน Core HR</span><span class="sxs-lookup"><span data-stu-id="f59e1-105">This topic describes features that are either new or changed in Core HR.</span></span>

## <a name="allow-other-dates-to-be-used-on-leave-tier-basis-leave-management"></a><span data-ttu-id="f59e1-106">อนุญาตให้วันที่อื่นๆ ถูกใช้ในเกณฑ์ระดับการลาหยุด (การจัดการการลางาน)</span><span class="sxs-lookup"><span data-stu-id="f59e1-106">Allow other dates to be used on leave tier basis (Leave Management)</span></span>

<span data-ttu-id="f59e1-107">เมื่อให้รางวัลการลางานแก่พนักงาน เกณฑ์ระดับรางวัลจะกำหนดระยะเวลาหยุดพักที่พนักงานค้างรับ</span><span class="sxs-lookup"><span data-stu-id="f59e1-107">When awarding leave to employees, the award tier basis determines how much time off an employee accrues.</span></span> <span data-ttu-id="f59e1-108">ในปัจจุบัน ระดับเหล่านี้จะยึดตามวันที่เริ่มต้นของพนักงานและวันที่อายุงาน</span><span class="sxs-lookup"><span data-stu-id="f59e1-108">Currently, these tiers are based on employee start date and seniority date.</span></span> <span data-ttu-id="f59e1-109">ในบางสถานการณ์ องค์กรต้องการให้ระดับเหล่านี้ขึ้นอยู่กับวันที่อื่นๆ เช่น วันที่ครบรอบปี หรือวันที่จ้างงานเดิม</span><span class="sxs-lookup"><span data-stu-id="f59e1-109">In some scenarios, organizations need these tiers to be based on other dates, like anniversary date or original hire date.</span></span> <span data-ttu-id="f59e1-110">วันที่ดังกล่าวถูกใช้ในแผนการลางานเรียบร้อยแล้ว เพื่อกำหนดเวลาที่จะเกิดการรับรู้ ความสามารถสำหรับวันที่เหมือนกันดังกล่าวจะถูกใช้เมื่อมีการลงทะเบียนพนักงานในแผน ถูกเพิ่มเพื่อกำหนดจำนวนเงินค้างรับค้างจ่าย</span><span class="sxs-lookup"><span data-stu-id="f59e1-110">These dates are already used on the leave plan to determine when accruals happen, the ability for these same dates to be used when an employee is enrolled in a plan have been added to determine the accrual amount.</span></span> 

## <a name="other-changes"></a><span data-ttu-id="f59e1-111">การเปลี่ยนแปลงอื่นๆ</span><span class="sxs-lookup"><span data-stu-id="f59e1-111">Other changes</span></span>
<span data-ttu-id="f59e1-112">การแก้ไขเบ็ดเตล็ดได้ถูกรวมไว้ในรุ่นนี้</span><span class="sxs-lookup"><span data-stu-id="f59e1-112">Miscellanous fixes have been included in this release.</span></span>

## <a name="known-issue"></a><span data-ttu-id="f59e1-113">ปัญหาที่ทราบ</span><span class="sxs-lookup"><span data-stu-id="f59e1-113">Known issue</span></span>

<span data-ttu-id="f59e1-114">**ปัญหา:** เมื่อเพิ่มสิ่งที่แนบมาใหม่ไปยังผู้ปฏิบัติงาน ปุ่ม **สร้าง** และ **แก้ไข** ถูกแรเงา **วิธีการแก้ไขปัญหา:** ก่อนที่จะเปิดหน้าเอกสารแนบ ให้แน่ใจว่า FactBoxes ในหน้า **ผู้ปฏิบัติงาน** ถูกปิดแล้ว</span><span class="sxs-lookup"><span data-stu-id="f59e1-114">**Issue:** When adding a new attachment to a worker, the **New** and **Edit** buttons are grayed out. **Workaround:** Before opening the attachment page, make sure that the FactBoxes on the **Worker** page are closed.</span></span> <span data-ttu-id="f59e1-115">ถ้า FactBoxes ถูกปิด เมื่อหน้า **ผู้ปฏิบัติงาน** ถูกโหลด ปุ่มเอกสารแนบจะถูกเปิดใช้งาน</span><span class="sxs-lookup"><span data-stu-id="f59e1-115">If the FactBoxes are closed when the **Worker** page is loaded, the attachments buttons will be enabled.</span></span> <span data-ttu-id="f59e1-116">(ปัญหานี้จะได้รับการแก้ไขในการปรับปรุงแพลตฟอร์มถัดไป)</span><span class="sxs-lookup"><span data-stu-id="f59e1-116">(This issue will be fixed in the next platform update.)</span></span>
