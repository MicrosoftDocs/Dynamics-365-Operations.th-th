--- 
title: "กำหนดกลุ่มทรัพยากรผู้ผลิตแยกกัน"
description: "กลุ่มทรัพยากรคือ ชุดของทรัพยากรการดำเนินงานที่โดยปกติจะสอดคล้องกับองค์กรจริงของเซลล์ทำงาน ซึ่งกำหนดโดยบรรทัดสีเหลืองบนการผลิตผลิตภัณฑ์ "
author: sorenva
manager: AnnBe
ms.date: 11/03/2017
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: sorenand
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: 9572886eb6bcf954566e8893e116d2237a74326d
ms.contentlocale: th-th
ms.lasthandoff: 05/08/2018

---
# <a name="define-discrete-manufacturing-resource-group"></a><span data-ttu-id="cca5b-103">กำหนดกลุ่มทรัพยากรผู้ผลิตแยกกัน</span><span class="sxs-lookup"><span data-stu-id="cca5b-103">Define discrete manufacturing resource group</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="cca5b-104">กลุ่มทรัพยากรคือ ชุดของทรัพยากรการดำเนินงานที่โดยปกติจะสอดคล้องกับองค์กรจริงของเซลล์ทำงาน ซึ่งกำหนดโดยบรรทัดสีเหลืองบนการผลิตผลิตภัณฑ์ </span><span class="sxs-lookup"><span data-stu-id="cca5b-104">A resource group is a set of operations resources that typically correspond to the physical organization of work cells, defined by yellow lines on the production shop floor.</span></span> <span data-ttu-id="cca5b-105">กระบวนงานนี้แสดงวิธีการกำหนดกลุ่มทรัพยากรสำหรับใช้ในการผลิตที่แยกกัน </span><span class="sxs-lookup"><span data-stu-id="cca5b-105">This procedure shows you how to define a resource group for use in discrete production.</span></span> <span data-ttu-id="cca5b-106">คุณสามารถดำเนินกระบวนงานนี้ในบริษัทข้อมูลสาธิต USMF หรือใช้ข้อมูลของคุณเอง</span><span class="sxs-lookup"><span data-stu-id="cca5b-106">You can walk through this procedure in demo data company USMF, or use your own data.</span></span>

1. <span data-ttu-id="cca5b-107">ไปที่กลุ่มทรัพยากร </span><span class="sxs-lookup"><span data-stu-id="cca5b-107">Go to Resource groups.</span></span>
2. <span data-ttu-id="cca5b-108">คลิก สร้าง</span><span class="sxs-lookup"><span data-stu-id="cca5b-108">Click New.</span></span>
3. <span data-ttu-id="cca5b-109">ในฟิลด์กลุ่มทรัพยากร ให้พิมพ์ค่า</span><span class="sxs-lookup"><span data-stu-id="cca5b-109">In the Resource group field, type a value.</span></span>
4. <span data-ttu-id="cca5b-110">ในฟิลด์ คำอธิบาย ให้พิมพ์ค่า</span><span class="sxs-lookup"><span data-stu-id="cca5b-110">In the Description field, type a value.</span></span>
5. <span data-ttu-id="cca5b-111">ในฟิลด์ไซต์ ให้ป้อนหรือเลือกค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="cca5b-111">In the Site field, enter or select a value.</span></span>
6. <span data-ttu-id="cca5b-112">ในฟิลด์หน่วยการผลิต ให้ป้อนหรือเลือกค่า </span><span class="sxs-lookup"><span data-stu-id="cca5b-112">In the Production unit field, enter or select a value.</span></span>

## <a name="define-default-operational-parameters"></a><span data-ttu-id="cca5b-113">กำหนดพารามิเตอร์ในการดำเนินงานเริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="cca5b-113">Define default operational parameters</span></span>
1. <span data-ttu-id="cca5b-114">ขยายส่วนการดำเนินงาน</span><span class="sxs-lookup"><span data-stu-id="cca5b-114">Expand the Operation section.</span></span>
2. <span data-ttu-id="cca5b-115">ในฟิลด์เปอร์เซ็นต์ของเสีย ให้ป้อนหมายเลข </span><span class="sxs-lookup"><span data-stu-id="cca5b-115">In the Scrap percentage field, enter a number.</span></span>
3. <span data-ttu-id="cca5b-116">ในฟิลด์ประเภทการตั้งค่า ให้ป้อนหรือเลือกค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="cca5b-116">In the Setup category field, enter or select a value.</span></span>
4. <span data-ttu-id="cca5b-117">ในฟิลด์ประเภทเวลาที่ใช้ในการผลิต ให้ป้อนหรือเลือกค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="cca5b-117">In the Run time category field, enter or select a value.</span></span>
5. <span data-ttu-id="cca5b-118">ในฟิลด์เปอร์เซ็นต์การจัดตารางการผลิตระดับการดำเนินงาน ให้ป้อนหมายเลข </span><span class="sxs-lookup"><span data-stu-id="cca5b-118">In the Operations scheduling percentage field, enter a number.</span></span>

## <a name="define-operating-hours"></a><span data-ttu-id="cca5b-119">กำหนดชั่วโมงการดำเนินงาน</span><span class="sxs-lookup"><span data-stu-id="cca5b-119">Define operating hours</span></span>
1. <span data-ttu-id="cca5b-120">ขยายส่วนปฏิทิน</span><span class="sxs-lookup"><span data-stu-id="cca5b-120">Expand the Calendars section.</span></span>
2. <span data-ttu-id="cca5b-121">คลิก เพิ่ม</span><span class="sxs-lookup"><span data-stu-id="cca5b-121">Click Add.</span></span>
3. <span data-ttu-id="cca5b-122">ในฟิลด์ปฏิทิน ให้ป้อนหรือเลือกค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="cca5b-122">In the Calendar field, enter or select a value.</span></span>

## <a name="add-operations-resources"></a><span data-ttu-id="cca5b-123">เพิ่มทรัพยากรการดำเนินงาน</span><span class="sxs-lookup"><span data-stu-id="cca5b-123">Add operations resources</span></span>
1. <span data-ttu-id="cca5b-124">ขยายส่วนทรัพยากร </span><span class="sxs-lookup"><span data-stu-id="cca5b-124">Expand the Resources section.</span></span>
2. <span data-ttu-id="cca5b-125">คลิก เพิ่ม</span><span class="sxs-lookup"><span data-stu-id="cca5b-125">Click Add.</span></span>
3. <span data-ttu-id="cca5b-126">ในฟิลด์ทรัพยากร ให้ป้อนหรือเลือกค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="cca5b-126">In the Resource field, enter or select a value.</span></span>
4. <span data-ttu-id="cca5b-127">คลิก เพิ่ม</span><span class="sxs-lookup"><span data-stu-id="cca5b-127">Click Add.</span></span>
5. <span data-ttu-id="cca5b-128">ในฟิลด์ทรัพยากร ให้ป้อนหรือเลือกค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="cca5b-128">In the Resource field, enter or select a value.</span></span>
6. <span data-ttu-id="cca5b-129">ในรายการนี้ ให้ค้นหาและเลือกเรกคอร์ดที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="cca5b-129">In the list, find and select the desired record.</span></span>
7. <span data-ttu-id="cca5b-130">ในรายการนี้ ให้คลิกลิงค์ในแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="cca5b-130">In the list, click the link in the selected row.</span></span>


