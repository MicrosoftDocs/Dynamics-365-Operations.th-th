---
title: ตั้งค่าคอนฟิกเหตุการณ์ของชีวิตในอนาคต
description: คุณสามารถจัดกำหนดการเหตุการณ์ของชีวิตอนาคตใน Dynamics 365 Human Resources
author: andreabichsel
manager: AnnBe
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: BenefitFutureLifeEvents
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 655070e52e3d1f43ca6904ce3218582868f193fe
ms.sourcegitcommit: 40163705a134c9874fd33be80c7ae59ccce22c21
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 02/03/2020
ms.locfileid: "3010745"
---
# <a name="configure-future-life-events"></a><span data-ttu-id="576ef-103">ตั้งค่าคอนฟิกเหตุการณ์ของชีวิตในอนาคต</span><span class="sxs-lookup"><span data-stu-id="576ef-103">Configure future life events</span></span>

[!include [banner](includes/preview-feature.md)]

<span data-ttu-id="576ef-104">คุณสามารถจัดกำหนดการเหตุการณ์ของชีวิตอนาคตใน Dynamics 365 Human Resources</span><span class="sxs-lookup"><span data-stu-id="576ef-104">You can schedule future life events in Dynamics 365 Human Resources.</span></span>

1. <span data-ttu-id="576ef-105">ในพื้นที่ทำงาน **การจัดการสวัสดิการ** ภายใต้ **การตั้งค่า** ให้เลือก **เหตุการณ์ของชีวิตในอนาคต**</span><span class="sxs-lookup"><span data-stu-id="576ef-105">In the **Benefits management** workspace, under **Setup**, select **Future life events**.</span></span>

2. <span data-ttu-id="576ef-106">เลือก **ใหม่**</span><span class="sxs-lookup"><span data-stu-id="576ef-106">Select **New**.</span></span>

3. <span data-ttu-id="576ef-107">ระบุค่าสำหรับฟิลด์ต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="576ef-107">Specify values for the following fields:</span></span>

   | <span data-ttu-id="576ef-108">ฟิลด์</span><span class="sxs-lookup"><span data-stu-id="576ef-108">Field</span></span> | <span data-ttu-id="576ef-109">คำอธิบาย</span><span class="sxs-lookup"><span data-stu-id="576ef-109">Description</span></span> |
   | --- | --- |
   | <span data-ttu-id="576ef-110">วันที่เหตุการณ์ของชีวิต</span><span class="sxs-lookup"><span data-stu-id="576ef-110">Life event date</span></span> | <span data-ttu-id="576ef-111">ระบบประมวลผลเหตุการณ์ทั้งหมดในระหว่างรอบระยะเวลาของการลงทะเบียนที่เกิดขึ้นจนถึงวันนี้</span><span class="sxs-lookup"><span data-stu-id="576ef-111">The system processes all events during the enrollment period that occur up until this date.</span></span> |
   | <span data-ttu-id="576ef-112">ลงบันทึกเหตุการณ์ของชีวิตแล้ว</span><span class="sxs-lookup"><span data-stu-id="576ef-112">Life event logged</span></span> | <span data-ttu-id="576ef-113">วันที่และเวลาเมื่อมีการบันทึกล็อกเหตุการณ์ของชีวิต</span><span class="sxs-lookup"><span data-stu-id="576ef-113">Date and time when the life event is logged.</span></span> |
   | <span data-ttu-id="576ef-114">ชนิดการล็อก</span><span class="sxs-lookup"><span data-stu-id="576ef-114">Log type</span></span> | <span data-ttu-id="576ef-115">แสดงว่าการดำเนินการเป็นอย่างใดอย่างหนึ่งต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="576ef-115">Shows whether the action is one of the following:</span></span></br></br><span data-ttu-id="576ef-116">- **การอัพเดต** – การเปลี่ยนแปลงที่เกิดขึ้นกับเรกคอร์ดที่ติดตามเหตุการณ์ของชีวิต</span><span class="sxs-lookup"><span data-stu-id="576ef-116">- **Update** – a change to an existing record that is tracking life events</span></span></br></br><span data-ttu-id="576ef-117">- **การแทรก** – การสร้างเรกคอร์ดเหตุการณ์ของชีวิตใหม่</span><span class="sxs-lookup"><span data-stu-id="576ef-117">- **Insert** – the creation of a new life event record</span></span> |
   | <span data-ttu-id="576ef-118">รหัสชนิดเหตุการณ์ของชีวิต</span><span class="sxs-lookup"><span data-stu-id="576ef-118">Life event type ID</span></span> | <span data-ttu-id="576ef-119">ตัวระบุเฉพาะของชนิดเหตุการณ์ของชีวิต</span><span class="sxs-lookup"><span data-stu-id="576ef-119">The life event type unique identifier.</span></span> |
   | <span data-ttu-id="576ef-120">ชนิดเหตุการณ์ของชีวิต</span><span class="sxs-lookup"><span data-stu-id="576ef-120">Life event type</span></span> | <span data-ttu-id="576ef-121">ตัวเร่งเพื่ออัพเดตการลงทะเบียนสวัสดิการของพนักงาน</span><span class="sxs-lookup"><span data-stu-id="576ef-121">A catalyst to updating an employee’s benefits enrollment.</span></span> <span data-ttu-id="576ef-122">สำหรับรายละเอียดเพิ่มเติม ให้ดูที่ส่วนทริกเกอร์เหตุการณ์ของชีวิต</span><span class="sxs-lookup"><span data-stu-id="576ef-122">For more details, see the Life event triggers section.</span></span> |
   | <span data-ttu-id="576ef-123">สถานะ</span><span class="sxs-lookup"><span data-stu-id="576ef-123">Status</span></span> | <span data-ttu-id="576ef-124">มีการประมวลผลเหตุการณ์ของชีวิตแล้วหรือไม่</span><span class="sxs-lookup"><span data-stu-id="576ef-124">Whether the life event has been processed or not.</span></span> |
   | <span data-ttu-id="576ef-125">บรรทัด</span><span class="sxs-lookup"><span data-stu-id="576ef-125">Line</span></span> | <span data-ttu-id="576ef-126">หมายเลขบรรทัดของเหตุการณ์ของชีวิตในอนาคต</span><span class="sxs-lookup"><span data-stu-id="576ef-126">The line number of the future life event.</span></span> |

4. <span data-ttu-id="576ef-127">เลือก **บันทึก**</span><span class="sxs-lookup"><span data-stu-id="576ef-127">Select **Save**.</span></span> 
