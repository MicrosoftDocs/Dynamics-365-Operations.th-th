---
title: ตั้งค่าคอนฟิกเหตุการณ์ของชีวิตในอนาคต
description: คุณสามารถจัดกำหนดการเหตุการณ์ของชีวิตอนาคตใน Dynamics 365 Human Resources
author: andreabichsel
manager: tfehr
ms.date: 04/06/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: BenefitFutureLifeEvents, BenefitWorkspace, HcmBenefitSummaryPart
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: f10d7b6c9b45f6cedc16972fb157e43b7e0c40b3
ms.sourcegitcommit: ea2d652867b9b83ce6e5e8d6a97d2f9460a84c52
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 02/03/2021
ms.locfileid: "5114485"
---
# <a name="configure-future-life-events"></a><span data-ttu-id="55b06-103">ตั้งค่าคอนฟิกเหตุการณ์ของชีวิตในอนาคต</span><span class="sxs-lookup"><span data-stu-id="55b06-103">Configure future life events</span></span>

<span data-ttu-id="55b06-104">คุณสามารถจัดกำหนดการเหตุการณ์ของชีวิตอนาคตใน Dynamics 365 Human Resources</span><span class="sxs-lookup"><span data-stu-id="55b06-104">You can schedule future life events in Dynamics 365 Human Resources.</span></span>

1. <span data-ttu-id="55b06-105">ในพื้นที่ทำงาน **การจัดการสวัสดิการ** ภายใต้ **การตั้งค่า** ให้เลือก **เหตุการณ์ของชีวิตในอนาคต**</span><span class="sxs-lookup"><span data-stu-id="55b06-105">In the **Benefits management** workspace, under **Setup**, select **Future life events**.</span></span>

2. <span data-ttu-id="55b06-106">เลือก **ใหม่**</span><span class="sxs-lookup"><span data-stu-id="55b06-106">Select **New**.</span></span>

3. <span data-ttu-id="55b06-107">ระบุค่าสำหรับฟิลด์ต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="55b06-107">Specify values for the following fields:</span></span>

   | <span data-ttu-id="55b06-108">ฟิลด์</span><span class="sxs-lookup"><span data-stu-id="55b06-108">Field</span></span> | <span data-ttu-id="55b06-109">คำอธิบาย</span><span class="sxs-lookup"><span data-stu-id="55b06-109">Description</span></span> |
   | --- | --- |
   | <span data-ttu-id="55b06-110">วันที่เหตุการณ์ของชีวิต</span><span class="sxs-lookup"><span data-stu-id="55b06-110">Life event date</span></span> | <span data-ttu-id="55b06-111">ระบบประมวลผลเหตุการณ์ทั้งหมดในระหว่างรอบระยะเวลาของการลงทะเบียนที่เกิดขึ้นจนถึงวันนี้</span><span class="sxs-lookup"><span data-stu-id="55b06-111">The system processes all events during the enrollment period that occur up until this date.</span></span> |
   | <span data-ttu-id="55b06-112">ลงบันทึกเหตุการณ์ของชีวิตแล้ว</span><span class="sxs-lookup"><span data-stu-id="55b06-112">Life event logged</span></span> | <span data-ttu-id="55b06-113">วันที่และเวลาเมื่อมีการบันทึกล็อกเหตุการณ์ของชีวิต</span><span class="sxs-lookup"><span data-stu-id="55b06-113">Date and time when the life event is logged.</span></span> |
   | <span data-ttu-id="55b06-114">ชนิดการล็อก</span><span class="sxs-lookup"><span data-stu-id="55b06-114">Log type</span></span> | <span data-ttu-id="55b06-115">แสดงว่าการดำเนินการเป็นอย่างใดอย่างหนึ่งต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="55b06-115">Shows whether the action is one of the following:</span></span></br></br><span data-ttu-id="55b06-116">- **การอัพเดต** – การเปลี่ยนแปลงที่เกิดขึ้นกับเรกคอร์ดที่ติดตามเหตุการณ์ของชีวิต</span><span class="sxs-lookup"><span data-stu-id="55b06-116">- **Update** – a change to an existing record that is tracking life events</span></span></br></br><span data-ttu-id="55b06-117">- **การแทรก** – การสร้างเรกคอร์ดเหตุการณ์ของชีวิตใหม่</span><span class="sxs-lookup"><span data-stu-id="55b06-117">- **Insert** – the creation of a new life event record</span></span> |
   | <span data-ttu-id="55b06-118">รหัสชนิดเหตุการณ์ของชีวิต</span><span class="sxs-lookup"><span data-stu-id="55b06-118">Life event type ID</span></span> | <span data-ttu-id="55b06-119">ตัวระบุเฉพาะของชนิดเหตุการณ์ของชีวิต</span><span class="sxs-lookup"><span data-stu-id="55b06-119">The life event type unique identifier.</span></span> |
   | <span data-ttu-id="55b06-120">ชนิดเหตุการณ์ของชีวิต</span><span class="sxs-lookup"><span data-stu-id="55b06-120">Life event type</span></span> | <span data-ttu-id="55b06-121">ตัวเร่งเพื่ออัพเดตการลงทะเบียนสวัสดิการของพนักงาน</span><span class="sxs-lookup"><span data-stu-id="55b06-121">A catalyst to updating an employee’s benefits enrollment.</span></span> <span data-ttu-id="55b06-122">สำหรับรายละเอียดเพิ่มเติม ให้ดูที่ส่วนทริกเกอร์เหตุการณ์ของชีวิต</span><span class="sxs-lookup"><span data-stu-id="55b06-122">For more details, see the Life event triggers section.</span></span> |
   | <span data-ttu-id="55b06-123">สถานะ</span><span class="sxs-lookup"><span data-stu-id="55b06-123">Status</span></span> | <span data-ttu-id="55b06-124">มีการประมวลผลเหตุการณ์ของชีวิตแล้วหรือไม่</span><span class="sxs-lookup"><span data-stu-id="55b06-124">Whether the life event has been processed or not.</span></span> |
   | <span data-ttu-id="55b06-125">บรรทัด</span><span class="sxs-lookup"><span data-stu-id="55b06-125">Line</span></span> | <span data-ttu-id="55b06-126">หมายเลขบรรทัดของเหตุการณ์ของชีวิตในอนาคต</span><span class="sxs-lookup"><span data-stu-id="55b06-126">The line number of the future life event.</span></span> |

4. <span data-ttu-id="55b06-127">เลือก **บันทึก**</span><span class="sxs-lookup"><span data-stu-id="55b06-127">Select **Save**.</span></span> 
