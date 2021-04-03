---
title: ประมวลผลการมีสิทธิ์ในเหตุการณ์ของชีวิต
description: บทความนี้แสดงวิธีการรันกระบวนการสำหรับการมีสิทธิ์ในเหตุการณ์ของชีวิต
author: andreabichsel
manager: tfehr
ms.date: 04/06/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: BenefitWorkspace, HcmBenefitSummaryPart, BenefitLifeEventTypes, BenefitEligibilityProcessResultViewer
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: fdb2f00675fa5191e05dcb99525c1ec9a8b16bd2
ms.sourcegitcommit: 6affb3316be757c99e1fe9c7c7b312b93c483408
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 02/17/2021
ms.locfileid: "5466289"
---
# <a name="process-life-event-eligibility"></a><span data-ttu-id="43107-103">ประมวลผลการมีสิทธิ์ในเหตุการณ์ของชีวิต</span><span class="sxs-lookup"><span data-stu-id="43107-103">Process life event eligibility</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="43107-104">บทความนี้แสดงวิธีการรันกระบวนการสำหรับการมีสิทธิ์ในเหตุการณ์ของชีวิต</span><span class="sxs-lookup"><span data-stu-id="43107-104">This article shows you how to run the process for life event eligibility.</span></span>

1. <span data-ttu-id="43107-105">ในพื้นที่ทำงาน **การจัดการสวัสดิการ** ภายใต้ **กำลังประมวลผล** ให้เลือก **กำลังประมวลผลการมีสิทธิ์ในเหตุการณ์ของชีวิต**</span><span class="sxs-lookup"><span data-stu-id="43107-105">In the **Benefits management** workspace, under **Processing**, select **Life event eligibility processing**.</span></span>

2. <span data-ttu-id="43107-106">ในกล่องโต้ตอบ **ดำเนินการประมวลผลสิทธิ์เหตุการณ์ของชีวิต** ให้ระบุค่าสำหรับฟิลด์ต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="43107-106">In the **Run life event eligibility process** dialog box, specify values for the following fields:</span></span>

   | <span data-ttu-id="43107-107">ฟิลด์</span><span class="sxs-lookup"><span data-stu-id="43107-107">Field</span></span> | <span data-ttu-id="43107-108">คำอธิบาย</span><span class="sxs-lookup"><span data-stu-id="43107-108">Description</span></span> |
   | --- | --- |
   | <span data-ttu-id="43107-109">**รอบระยะเวลาการลงทะเบียน**</span><span class="sxs-lookup"><span data-stu-id="43107-109">**Enrollment period**</span></span> | <span data-ttu-id="43107-110">รอบระยะเวลาการลงทะเบียนที่จะประมวลผลการมีสิทธิ์ในเหตุการณ์ของชีวิต</span><span class="sxs-lookup"><span data-stu-id="43107-110">The enrollment period to process life event eligibility for.</span></span> |

3. <span data-ttu-id="43107-111">ถ้าคุณต้องการดำเนินการกระบวนการในพื้นหลัง ให้เลือก **ดำเนินการในพื้นหลัง** และงานต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="43107-111">If you want to run the process in the background, select **Run in the background** and do the following tasks:</span></span>

   1. <span data-ttu-id="43107-112">ป้อนข้อมูลสำหรับกระบวนการ</span><span class="sxs-lookup"><span data-stu-id="43107-112">Enter information for the process.</span></span>

   2. <span data-ttu-id="43107-113">หากต้องการตั้งค่าให้มีการรันงานนั้นซ้ำ เลือก **การเกิดซ้ำ** ป้อนข้อมูลการเกิดซ้ำ และเลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="43107-113">To set up a recurring job, select **Recurrence**, enter the recurrence information, and the select **OK**.</span></span>

   3. <span data-ttu-id="43107-114">เมื่อต้องการตั้งค่าการแจ้งเตือนงาน เลือก **การแจ้งเตือน** เลือกการแจ้งเตือนที่จะรับ และจากนั้นเลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="43107-114">To set up a job alert, select **Alerts**, select the alerts to receive, and then select **OK**.</span></span>

   4. <span data-ttu-id="43107-115">เลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="43107-115">Select **OK**.</span></span> <span data-ttu-id="43107-116">กระบวนการจะดำเนินการกับพารามิเตอร์ที่คุณตั้งไว้</span><span class="sxs-lookup"><span data-stu-id="43107-116">The process will run with the parameters you set.</span></span>

4. <span data-ttu-id="43107-117">เลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="43107-117">Select **OK**.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]