---
title: ประมวลผลการมีสิทธิ์ในเหตุการณ์ของชีวิต
description: บทความนี้แสดงวิธีการรันกระบวนการสำหรับการมีสิทธิ์ในเหตุการณ์ของชีวิต
author: andreabichsel
ms.date: 04/06/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: BenefitWorkspace, HcmBenefitSummaryPart, BenefitLifeEventTypes, BenefitEligibilityProcessResultViewer
audience: Application User
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 20b458e67b6504ca1c3efce6b40d1cea4faa7193
ms.sourcegitcommit: 879ee8a10e6158885795dce4b3db5077540eec41
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 05/18/2021
ms.locfileid: "6058523"
---
# <a name="process-life-event-eligibility"></a><span data-ttu-id="43d5c-103">ประมวลผลการมีสิทธิ์ในเหตุการณ์ของชีวิต</span><span class="sxs-lookup"><span data-stu-id="43d5c-103">Process life event eligibility</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="43d5c-104">บทความนี้แสดงวิธีการรันกระบวนการสำหรับการมีสิทธิ์ในเหตุการณ์ของชีวิต</span><span class="sxs-lookup"><span data-stu-id="43d5c-104">This article shows you how to run the process for life event eligibility.</span></span>

1. <span data-ttu-id="43d5c-105">ในพื้นที่ทำงาน **การจัดการสวัสดิการ** ภายใต้ **กำลังประมวลผล** ให้เลือก **กำลังประมวลผลการมีสิทธิ์ในเหตุการณ์ของชีวิต**</span><span class="sxs-lookup"><span data-stu-id="43d5c-105">In the **Benefits management** workspace, under **Processing**, select **Life event eligibility processing**.</span></span>

2. <span data-ttu-id="43d5c-106">ในกล่องโต้ตอบ **ดำเนินการประมวลผลสิทธิ์เหตุการณ์ของชีวิต** ให้ระบุค่าสำหรับฟิลด์ต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="43d5c-106">In the **Run life event eligibility process** dialog box, specify values for the following fields:</span></span>

   | <span data-ttu-id="43d5c-107">ฟิลด์</span><span class="sxs-lookup"><span data-stu-id="43d5c-107">Field</span></span> | <span data-ttu-id="43d5c-108">คำอธิบาย</span><span class="sxs-lookup"><span data-stu-id="43d5c-108">Description</span></span> |
   | --- | --- |
   | <span data-ttu-id="43d5c-109">**รอบระยะเวลาการลงทะเบียน**</span><span class="sxs-lookup"><span data-stu-id="43d5c-109">**Enrollment period**</span></span> | <span data-ttu-id="43d5c-110">รอบระยะเวลาการลงทะเบียนที่จะประมวลผลการมีสิทธิ์ในเหตุการณ์ของชีวิต</span><span class="sxs-lookup"><span data-stu-id="43d5c-110">The enrollment period to process life event eligibility for.</span></span> |

3. <span data-ttu-id="43d5c-111">ถ้าคุณต้องการดำเนินการกระบวนการในพื้นหลัง ให้เลือก **ดำเนินการในพื้นหลัง** และงานต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="43d5c-111">If you want to run the process in the background, select **Run in the background** and do the following tasks:</span></span>

   1. <span data-ttu-id="43d5c-112">ป้อนข้อมูลสำหรับกระบวนการ</span><span class="sxs-lookup"><span data-stu-id="43d5c-112">Enter information for the process.</span></span>

   2. <span data-ttu-id="43d5c-113">หากต้องการตั้งค่าให้มีการรันงานนั้นซ้ำ เลือก **การเกิดซ้ำ** ป้อนข้อมูลการเกิดซ้ำ และเลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="43d5c-113">To set up a recurring job, select **Recurrence**, enter the recurrence information, and the select **OK**.</span></span>

   3. <span data-ttu-id="43d5c-114">เมื่อต้องการตั้งค่าการแจ้งเตือนงาน เลือก **การแจ้งเตือน** เลือกการแจ้งเตือนที่จะรับ และจากนั้นเลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="43d5c-114">To set up a job alert, select **Alerts**, select the alerts to receive, and then select **OK**.</span></span>

   4. <span data-ttu-id="43d5c-115">เลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="43d5c-115">Select **OK**.</span></span> <span data-ttu-id="43d5c-116">กระบวนการจะดำเนินการกับพารามิเตอร์ที่คุณตั้งไว้</span><span class="sxs-lookup"><span data-stu-id="43d5c-116">The process will run with the parameters you set.</span></span>

4. <span data-ttu-id="43d5c-117">เลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="43d5c-117">Select **OK**.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]