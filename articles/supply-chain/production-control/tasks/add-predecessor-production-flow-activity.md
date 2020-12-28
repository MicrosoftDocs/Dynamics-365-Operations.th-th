---
title: เพิ่มงานที่เกิดขึ้นก่อนหน้าในกิจกรรมขั้นตอนการผลิต
description: 'ในรุ่นขั้นตอนการผลิต กิจกรรมทั้งหมดต้องมีการจัดลำดับ '
author: cvocph
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LeanProductionFlow, PlanActivity, PlanActivityRelationNew, PlanActivityLookup
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: c39cef1174439b42a072bd7fc1ac29ef31ecf864
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 10/13/2020
ms.locfileid: "4438215"
---
# <a name="add-a-predecessor-to-a-production-flow-activity"></a><span data-ttu-id="82432-103">เพิ่มงานที่เกิดขึ้นก่อนหน้าในกิจกรรมขั้นตอนการผลิต</span><span class="sxs-lookup"><span data-stu-id="82432-103">Add a predecessor to a production flow activity</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="82432-104">ในรุ่นขั้นตอนการผลิต กิจกรรมทั้งหมดต้องมีการจัดลำดับ </span><span class="sxs-lookup"><span data-stu-id="82432-104">In a production flow version, all activities must be sequenced.</span></span> <span data-ttu-id="82432-105">กิจกรรมสามารถมีหนึ่งหรือหลายรายการก่อนหน้าหรืองานที่เกิดขึ้นตามมา</span><span class="sxs-lookup"><span data-stu-id="82432-105">An activity can have one or multiple predecessors or successors.</span></span> 

<span data-ttu-id="82432-106">กระบวนงานนี้แสดงวิธีการเชื่อมโยงงานที่เกิดขึ้นก่อนหน้ากับกิจกรรม</span><span class="sxs-lookup"><span data-stu-id="82432-106">This procedure shows how to associate a predecessor to an activity.</span></span> 

<span data-ttu-id="82432-107">คุณจำเป็นต้องใช้ขั้นตอนการผลิตที่มีรุ่นฉบับร่างที่มีกิจกรรมอย่างน้อยสองรายการที่สามารถเชื่อมต่อได้</span><span class="sxs-lookup"><span data-stu-id="82432-107">To perform this task, you need a production flow that has the Draft version with at least two activities that can be connected.</span></span> 

<span data-ttu-id="82432-108">ถ้าต้องการทราบข้อมูลเพิ่มเติม โปรดอ่านเอกสารทางเทคนิค "ขั้นตอนการผลิตและกิจกรรมใน Lean Manufacturing"</span><span class="sxs-lookup"><span data-stu-id="82432-108">To learn more, read the white paper "Production flows and activities in lean manufacturing."</span></span>


## <a name="find-the-production-flow-and-version"></a><span data-ttu-id="82432-109">ค้นหาขั้นตอนและรุ่นการผลิต</span><span class="sxs-lookup"><span data-stu-id="82432-109">Find the production flow and version</span></span>
1. <span data-ttu-id="82432-110">ไปที่การควบคุมการผลิต > การตั้งค่า > ขั้นตอนการผลิตแบบ lean > ขั้นตอนการผลิต</span><span class="sxs-lookup"><span data-stu-id="82432-110">Go to Production control > Setup > Lean production flow > Production flows.</span></span>
2. <span data-ttu-id="82432-111">ในรายการนี้ ให้ค้นหาและเลือกเรกคอร์ดที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="82432-111">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="82432-112">ในรายการนี้ ให้คลิกลิงค์ในแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="82432-112">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="82432-113">ในรายการนี้ ให้ค้นหาและเลือกเรกคอร์ดที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="82432-113">In the list, find and select the desired record.</span></span>
5. <span data-ttu-id="82432-114">คลิกกิจกรรม</span><span class="sxs-lookup"><span data-stu-id="82432-114">Click Activities.</span></span>

## <a name="select-an-activity-and-add-a-predecessor"></a><span data-ttu-id="82432-115">เลือกกิจกรรมและเพิ่มงานที่เกิดขึ้นก่อนหน้า</span><span class="sxs-lookup"><span data-stu-id="82432-115">Select an activity and add a predecessor</span></span>
1. <span data-ttu-id="82432-116">ในรายการนี้ ให้ค้นหาและเลือกเรกคอร์ดที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="82432-116">In the list, find and select the desired record.</span></span>
2. <span data-ttu-id="82432-117">คลิก เพิ่มงานที่เกิดขึ้นก่อนหน้า</span><span class="sxs-lookup"><span data-stu-id="82432-117">Click Add predecessor.</span></span>
3. <span data-ttu-id="82432-118">ในฟิลด์กิจกรรม ให้ป้อนหรือเลือกค่า</span><span class="sxs-lookup"><span data-stu-id="82432-118">In the Activity field, enter or select a value.</span></span>
4. <span data-ttu-id="82432-119">ในฟิลด์อัตราส่วนเวลาวงจร ให้ป้อนหมายเลข</span><span class="sxs-lookup"><span data-stu-id="82432-119">In the Cycle time ratio field, enter a number.</span></span>
    * <span data-ttu-id="82432-120">อัตราส่วนเวลาวงจรเริ่มต้นของความสัมพันธ์ของกิจกรรมคือ 1</span><span class="sxs-lookup"><span data-stu-id="82432-120">The default cycle time ratio of an activity relation is 1.</span></span> <span data-ttu-id="82432-121">โดยสมมติว่ากิจกรรมทั้งสองจะรันพร้อมกันหรือเวลาที่ใช้ในการผลิตแบบสมดุลเท่ากัน</span><span class="sxs-lookup"><span data-stu-id="82432-121">This assumes that both activities run at the same pace or takt time.</span></span> <span data-ttu-id="82432-122">ถ้ากิจกรรมที่เกิดขึ้นก่อนหน้ารันเร็วกว่า (เวลาที่ใช้ในการผลิตแบบสมดุลต่ำกว่า) อัตราส่วนควรจะน้อยกว่า 1 ถ้ากิจกรรมที่เกิดขึ้นก่อนหน้ารันช้ากว่า (เวลาที่ใช้ในการผลิตแบบสมดุลสูงกว่า) อัตราส่วนเวลาวงจรจะมากกว่า 1</span><span class="sxs-lookup"><span data-stu-id="82432-122">If the predecessor runs at a higher pace (lower takt time), the ratio should be lower than 1, if the predecessor runs at a slower pace (higher takt time) the cycle time ratio is greater than 1.</span></span>  
5. <span data-ttu-id="82432-123">คลิก ตกลง</span><span class="sxs-lookup"><span data-stu-id="82432-123">Click OK.</span></span>

