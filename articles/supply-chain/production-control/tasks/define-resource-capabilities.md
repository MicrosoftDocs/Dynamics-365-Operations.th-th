--- 
title: "กำหนดความสามารถของทรัพยากร"
description: "ความสามารถของทรัพยากรอธิบายสิ่งที่ทรัพยากรการดำเนินงานสามารถทำได้"
author: sorenva
manager: AnnBe
ms.date: 10/27/2016
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
ms.openlocfilehash: 94a1a6bf72a24549b29d24277e5524990b357074
ms.contentlocale: th-th
ms.lasthandoff: 05/08/2018

---
# <a name="define-resource-capabilities"></a><span data-ttu-id="7fe54-103">กำหนดความสามารถของทรัพยากร</span><span class="sxs-lookup"><span data-stu-id="7fe54-103">Define resource capabilities</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="7fe54-104">ความสามารถของทรัพยากรอธิบายสิ่งที่ทรัพยากรการดำเนินงานสามารถทำได้</span><span class="sxs-lookup"><span data-stu-id="7fe54-104">Resource capabilities describe what operations resources can do.</span></span> <span data-ttu-id="7fe54-105">ในระหว่างการวางแผน ความต้องการของแต่ละงานและการดำเนินงานจะถูกจับคู่กับความสามารถของทรัพยากรที่พร้อมใช้งาน</span><span class="sxs-lookup"><span data-stu-id="7fe54-105">During scheduling, the requirements of each job and operation are matched against the capabilities of the available resources.</span></span> <span data-ttu-id="7fe54-106">คู่มืองานนี้จะช่วยคุณสร้างความสามารถทรัพยากรและกำหนดให้กับทรัพยากร </span><span class="sxs-lookup"><span data-stu-id="7fe54-106">This task guide will help you create a resource capability and assign it to a resource.</span></span> <span data-ttu-id="7fe54-107">ข้อมูลสาธิตของบริษัทที่ใช้ในการสร้างงานนี้คือ USMF</span><span class="sxs-lookup"><span data-stu-id="7fe54-107">The demo data company used to create this task is USMF.</span></span>


## <a name="create-a-resource-capability"></a><span data-ttu-id="7fe54-108">สร้างความสามารถของทรัพยากร</span><span class="sxs-lookup"><span data-stu-id="7fe54-108">Create a resource capability</span></span>
1. <span data-ttu-id="7fe54-109">ไปที่ความสามารถของทรัพยากร</span><span class="sxs-lookup"><span data-stu-id="7fe54-109">Go to Resource capabilities.</span></span>
2. <span data-ttu-id="7fe54-110">คลิก สร้าง</span><span class="sxs-lookup"><span data-stu-id="7fe54-110">Click New.</span></span>
3. <span data-ttu-id="7fe54-111">ในฟิลด์ความสามารถ ให้พิมพ์รหัสของความสามารถของทรัพยากร</span><span class="sxs-lookup"><span data-stu-id="7fe54-111">In the Capability field, type the ID of the resource capability.</span></span>
    * <span data-ttu-id="7fe54-112">สำหรับการดำเนินงานที่ได้รับมอบหมาย คุณสามารถใช้รหัสความสามารถเพื่อระบุว่าทรัพยากรต้องมีความสามารถนี้เพื่อดำเนินการ</span><span class="sxs-lookup"><span data-stu-id="7fe54-112">For a given operation, you use the capability ID to specify that resources must have this capability to perform the operation.</span></span>  
4. <span data-ttu-id="7fe54-113">ในฟิลด์คำอธิบาย ให้ป้อนคำอธิบายของความสามารถ</span><span class="sxs-lookup"><span data-stu-id="7fe54-113">In the Description field, enter a description of the capability.</span></span>

## <a name="assign-capability-to-a-resource"></a><span data-ttu-id="7fe54-114">กำหนดความสามารถให้กับทรัพยากร</span><span class="sxs-lookup"><span data-stu-id="7fe54-114">Assign capability to a resource</span></span>
1. <span data-ttu-id="7fe54-115">คลิก เพิ่ม</span><span class="sxs-lookup"><span data-stu-id="7fe54-115">Click Add.</span></span>
2. <span data-ttu-id="7fe54-116">ในฟิลด์ทรัพยากร ให้พิมพ์รหัสของทรัพยากร</span><span class="sxs-lookup"><span data-stu-id="7fe54-116">In the Resource field, type the ID of the resource.</span></span>
    * <span data-ttu-id="7fe54-117">ความสามารถของทรัพยากรสามารถถูกกำหนดให้กับทรัพยากรอีกหนึ่งรายการหรือมากกว่า</span><span class="sxs-lookup"><span data-stu-id="7fe54-117">A resource capability can be assigned to one or more resources.</span></span>  
3. <span data-ttu-id="7fe54-118">ในฟิลด์การหมดอายุ ให้ป้อนวันที่</span><span class="sxs-lookup"><span data-stu-id="7fe54-118">In the Expiration field, enter a date.</span></span>
    * <span data-ttu-id="7fe54-119">คุณสามารถใช้ฟิลด์นี้เพื่อระบุว่าทรัพยากรมีความสามารถสำหรับเฉพาะเวลาที่จำกัดเท่านั้น</span><span class="sxs-lookup"><span data-stu-id="7fe54-119">You can use this field to specify that a resource has the capability for only a limited time.</span></span>  
4. <span data-ttu-id="7fe54-120">ในฟิลด์ระดับความสำคัญ ให้ป้อนตัวเลข</span><span class="sxs-lookup"><span data-stu-id="7fe54-120">In the Priority field, enter a number.</span></span>
    * <span data-ttu-id="7fe54-121">เมื่อคุณจัดกำหนดการงานและการดำเนินงาน คุณสามารถระบุว่าจะเลือกทรัพยากรตามระดับความสำคัญหรือไม่ </span><span class="sxs-lookup"><span data-stu-id="7fe54-121">When you schedule jobs and operations, you can specify whether to select resources by priority.</span></span> <span data-ttu-id="7fe54-122">ถ้าคุณเลือกที่จะดำเนินการนี้ และทรัพยากรมากกว่าหนึ่งสามารถทำงานหรือการดำเนินงานโดยเรียงตามวันร้องขอ จะมีการเลือกทรัพยากรที่มีระดับความสำคัญต่ำสุดที่เกี่ยวข้องกับความสามารถที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="7fe54-122">If you choose to do this, and more than one resource can perform the job or operation by the requested date, the resource that has the lowest priority with respect to the required capability is selected.</span></span>  
5. <span data-ttu-id="7fe54-123">ในฟิลด์ระดับ ให้ป้อนตัวเลข</span><span class="sxs-lookup"><span data-stu-id="7fe54-123">In the Level field, enter a number.</span></span>
    * <span data-ttu-id="7fe54-124">เมื่อคุณระบุว่างานหรือการดำเนินงานต้องการความสามารถเฉพาะ คุณยังสามารถระบุระดับต่ำสุดที่ต้องการได้อีกด้วย </span><span class="sxs-lookup"><span data-stu-id="7fe54-124">When you specify that a job or operation requires a particular capability, you can also specify the minimum level that is required.</span></span> <span data-ttu-id="7fe54-125">ใช้ระดับความสามารถเพื่อแยกความแตกต่างของทรัพยากรที่สามารถทำงานเดียวกันได้ แต่ที่ความเร็ว จุดแข็ง ขนาด และอื่นๆ ที่แตกต่างกัน</span><span class="sxs-lookup"><span data-stu-id="7fe54-125">Use the capability level to differentiate resources that can perform the same job, but at different speeds, strengths, sizes, and so on.</span></span>  


