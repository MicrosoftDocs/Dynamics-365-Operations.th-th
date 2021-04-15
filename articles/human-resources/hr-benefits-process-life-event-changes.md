---
title: ประมวลผลการเปลี่ยนแปลงในเหตุการณ์ของชีวิต
description: ประมวลผลการเปลี่ยนแปลงในเหตุการณ์ของชีวิตใน Microsoft Dynamics 365 Human Resources สำหรับการเปลี่ยนแปลงเหตุการณ์ของชีวิต
author: andreabichsel
ms.date: 04/06/2020
ms.topic: article
ms.prod: ''
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
ms.openlocfilehash: a3cddc6205660b48abd9067bfdcaa04c9d2ba541
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 03/31/2021
ms.locfileid: "5790919"
---
# <a name="process-life-event-changes"></a><span data-ttu-id="1ae07-103">ประมวลผลการเปลี่ยนแปลงในเหตุการณ์ของชีวิต</span><span class="sxs-lookup"><span data-stu-id="1ae07-103">Process life event changes</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="1ae07-104">ประมวลผลการเปลี่ยนแปลงในเหตุการณ์ของชีวิตใน Microsoft Dynamics 365 Human Resources สำหรับสองการเปลี่ยนแปลงเหตุการณ์ของชีวิต</span><span class="sxs-lookup"><span data-stu-id="1ae07-104">Process life event changes in Microsoft Dynamics 365 Human Resources for two life event changes:</span></span>

- <span data-ttu-id="1ae07-105">การเปลี่ยนแปลงวันเกิด</span><span class="sxs-lookup"><span data-stu-id="1ae07-105">Birthday changes</span></span>
- <span data-ttu-id="1ae07-106">กฎการใช้สิทธิ์แทนที่การเปลี่ยนการหมดอายุ</span><span class="sxs-lookup"><span data-stu-id="1ae07-106">Eligibility rule override expiration changes</span></span> 

1. <span data-ttu-id="1ae07-107">ในพื้นที่ทำงาน **การจัดการสวัสดิการ** ภายใต้ **กำลังประมวลผล** ให้เลือก **กำลังประมวลผลการเปลี่ยนแปลงในเหตุการณ์ของชีวิต**</span><span class="sxs-lookup"><span data-stu-id="1ae07-107">In the **Benefits management** workspace, under **Processing**, select **Life event change processing**.</span></span>

2. <span data-ttu-id="1ae07-108">ในกล่องโต้ตอบ **ดำเนินการประมวลผลการเปลี่ยนแปลงเหตุการณ์ของชีวิต** ให้ระบุค่าสำหรับฟิลด์ต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="1ae07-108">In the **Run life event change process** dialog box, specify values for the following fields:</span></span>

   | <span data-ttu-id="1ae07-109">ฟิลด์</span><span class="sxs-lookup"><span data-stu-id="1ae07-109">Field</span></span> | <span data-ttu-id="1ae07-110">คำอธิบาย</span><span class="sxs-lookup"><span data-stu-id="1ae07-110">Description</span></span> |
   | --- | --- |
   | <span data-ttu-id="1ae07-111">รอบระยะเวลาการลงทะเบียน</span><span class="sxs-lookup"><span data-stu-id="1ae07-111">Enrollment period</span></span> | <span data-ttu-id="1ae07-112">รอบระยะเวลาการลงทะเบียนที่จะประมวลผลการเปลี่ยนแปลงในเหตุการณ์ของชีวิต</span><span class="sxs-lookup"><span data-stu-id="1ae07-112">The enrollment period to process life event changes for.</span></span> |
   | <span data-ttu-id="1ae07-113">นิติบุคคล</span><span class="sxs-lookup"><span data-stu-id="1ae07-113">Legal entity</span></span> | <span data-ttu-id="1ae07-114">นิติบุคคลที่จะประมวลผลการเปลี่ยนแปลงในเหตุการณ์ของชีวิต</span><span class="sxs-lookup"><span data-stu-id="1ae07-114">The legal entity to process life event changes for.</span></span> |

3. <span data-ttu-id="1ae07-115">ถ้าคุณต้องการดำเนินการกระบวนการในพื้นหลัง ให้เลือก **ดำเนินการในพื้นหลัง** และงานต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="1ae07-115">If you want to run the process in the background, select **Run in the background** and do the following tasks:</span></span>

   1. <span data-ttu-id="1ae07-116">ป้อนข้อมูลสำหรับกระบวนการ</span><span class="sxs-lookup"><span data-stu-id="1ae07-116">Enter information for the process.</span></span>

   2. <span data-ttu-id="1ae07-117">หากต้องการตั้งค่าให้มีการรันงานนั้นซ้ำ เลือก **การเกิดซ้ำ** ป้อนข้อมูลการเกิดซ้ำ และเลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="1ae07-117">To set up a recurring job, select **Recurrence**, enter the recurrence information, and the select **OK**.</span></span>

   3. <span data-ttu-id="1ae07-118">เมื่อต้องการตั้งค่าการแจ้งเตือนงาน เลือก **การแจ้งเตือน** เลือกการแจ้งเตือนที่จะรับ และจากนั้นเลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="1ae07-118">To set up a job alert, select **Alerts**, select the alerts to receive, and then select **OK**.</span></span>

   4. <span data-ttu-id="1ae07-119">เลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="1ae07-119">Select **OK**.</span></span> <span data-ttu-id="1ae07-120">กระบวนการจะดำเนินการกับพารามิเตอร์ที่คุณตั้งไว้</span><span class="sxs-lookup"><span data-stu-id="1ae07-120">The process will run with the parameters you set.</span></span>

4. <span data-ttu-id="1ae07-121">เลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="1ae07-121">Select **OK**.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]