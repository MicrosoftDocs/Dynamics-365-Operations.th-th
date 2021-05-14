---
title: รักษากระบวนการผลิตสำหรับรุ่นผลิตภัณฑ์
description: 'การดำเนินกระบวนงานนี้จำเป็นต้องมีแบบจำลองการตั้งค่าคอนฟิกรุ่นผลิตภัณฑ์ที่มีอยู่ '
author: ShylaThompson
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: DefaultDashboard, EcoResProductVariantMaintainWorkspace, PCProductConfigurationModelListPage, PCProductConfigurationModelDetails, PCRouteOperationDetails, WrkCtrCapabilityLookUp
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 45c6b1e6e75645bb17ce4defa0bca0e6d2131b6e
ms.sourcegitcommit: fa99a36c3d30d0c0577fd3f63ed6bf2f71599e40
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 04/20/2021
ms.locfileid: "5921276"
---
# <a name="maintain-route-for-a-product-model"></a><span data-ttu-id="81dac-103">รักษากระบวนการผลิตสำหรับรุ่นผลิตภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="81dac-103">Maintain route for a product model</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="81dac-104">การดำเนินกระบวนงานนี้จำเป็นต้องมีแบบจำลองการตั้งค่าคอนฟิกรุ่นผลิตภัณฑ์ที่มีอยู่ </span><span class="sxs-lookup"><span data-stu-id="81dac-104">Running this procedure requires that a product configuration model exists.</span></span> <span data-ttu-id="81dac-105">กระบวนงานนี้ใช้แบบจำลองลำโพงขั้นสูงในบริษัทสาธิต USMF เพื่อดำเนินกระบวนการ</span><span class="sxs-lookup"><span data-stu-id="81dac-105">This procedure uses the High end speaker model in the demo company USMF to walk you through the process.</span></span>

## <a name="add-a-route-operation"></a><span data-ttu-id="81dac-106">เพิ่มขั้นตอนของกระบวนการผลิต</span><span class="sxs-lookup"><span data-stu-id="81dac-106">Add a route operation</span></span>

1. <span data-ttu-id="81dac-107">ไปที่ **การจัดการข้อมูลผลิตภัณฑ์ \> ผลิตภัณฑ์ \> แบบจำลองการจัดโครงแบบผลิตภัณฑ์**</span><span class="sxs-lookup"><span data-stu-id="81dac-107">Go to **Product information management \> Products \> Product configuration models**.</span></span>
1. <span data-ttu-id="81dac-108">ในรายการนี้ ให้ค้นหาและเลือกเรกคอร์ดที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="81dac-108">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="81dac-109">เลือกแบบจำลองลำโพงขั้นสูงสำหรับงานนี้</span><span class="sxs-lookup"><span data-stu-id="81dac-109">Select the High end speaker model for this exercise.</span></span>  
1. <span data-ttu-id="81dac-110">ในรายการนี้ ให้เลือกลิงค์ในแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="81dac-110">In the list, select the link in the selected row.</span></span>
1. <span data-ttu-id="81dac-111">ขยายส่วน **ดำเนินงานในกระบวนการผลิต**</span><span class="sxs-lookup"><span data-stu-id="81dac-111">Expand the **Route operations** section.</span></span>
1. <span data-ttu-id="81dac-112">เลือก **เพิ่ม**</span><span class="sxs-lookup"><span data-stu-id="81dac-112">Select **Add**.</span></span>
1. <span data-ttu-id="81dac-113">ในฟิลด์ **ชื่อ** ให้พิมพ์ค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="81dac-113">In the **Name** field, type a value.</span></span>
1. <span data-ttu-id="81dac-114">ในฟิลด์ **คำอธิบาย** ให้พิมพ์ค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="81dac-114">In the **Description** field, type a value.</span></span>
1. <span data-ttu-id="81dac-115">เลือก **บันทึก**</span><span class="sxs-lookup"><span data-stu-id="81dac-115">Select **Save**.</span></span>

## <a name="enter-route-operation-details"></a><span data-ttu-id="81dac-116">ป้อนรายละเอียดขั้นตอนของกระบวนการผลิต</span><span class="sxs-lookup"><span data-stu-id="81dac-116">Enter route operation details</span></span>

1. <span data-ttu-id="81dac-117">เลือก **รายละเอียดการดำเนินการในกระบวนการผลิต**</span><span class="sxs-lookup"><span data-stu-id="81dac-117">Select **Route operation details**.</span></span>
1. <span data-ttu-id="81dac-118">ในฟิลด์ **การดำเนินงาน** ให้ป้อนหรือเลือกค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="81dac-118">In the **Operation** field, enter or select a value.</span></span>
1. <span data-ttu-id="81dac-119">ใน **หมายเลขการดำเนินงาน**</span><span class="sxs-lookup"><span data-stu-id="81dac-119">In the **Oper. No.**</span></span> <span data-ttu-id="81dac-120">ป้อนหมายเลข</span><span class="sxs-lookup"><span data-stu-id="81dac-120">field, enter a number.</span></span>
    * <span data-ttu-id="81dac-121">หมายเลขการดำเนินงานกำหนดลำดับในกระบวนการผลิต</span><span class="sxs-lookup"><span data-stu-id="81dac-121">Operation numbers determine the route sequence.</span></span>  
    * <span data-ttu-id="81dac-122">แต่ละคุณสมบัติในกระบวนการผลิตสามารถมีค่าคงที่หรือถูกแม็ปกับคุณลักษณะ </span><span class="sxs-lookup"><span data-stu-id="81dac-122">Each property on a route operation can get a static value or be mapped to an attribute.</span></span> <span data-ttu-id="81dac-123">การแม็ปไปยังคุณลักษณะจะมีผลกับค่าที่ถูกตั้งค่าเป็นส่วนหนึ่งของการตั้งค่าคอนฟิก</span><span class="sxs-lookup"><span data-stu-id="81dac-123">Mapping to an attribute will result in the value being set as part of the configuration.</span></span>  
1. <span data-ttu-id="81dac-124">ในฟิลด์ **กลุ่มกระบวนการผลิต** ให้ป้อนหรือเลือกค่า</span><span class="sxs-lookup"><span data-stu-id="81dac-124">In the **Route group** field, enter or select a value.</span></span>
    * <span data-ttu-id="81dac-125">กลุ่มกระบวนการผลิตกำหนดลักษณะการทำงานที่จำเป็นสำหรับการคิดต้นทุน ปริมาณการใช้วัสดุ และการตั้งค่า</span><span class="sxs-lookup"><span data-stu-id="81dac-125">The route group determines essential behavior for costing, consumption, and setup.</span></span>  
1. <span data-ttu-id="81dac-126">เลือกแท็บ **การตั้งค่า**</span><span class="sxs-lookup"><span data-stu-id="81dac-126">Select the **Setup** tab.</span></span>
1. <span data-ttu-id="81dac-127">เลือกแท็บ **เวลา**</span><span class="sxs-lookup"><span data-stu-id="81dac-127">Select the **Times** tab.</span></span>
1. <span data-ttu-id="81dac-128">ในฟิลด์ **ปริมาณกระบวนการ** ให้ป้อนตัวเลข</span><span class="sxs-lookup"><span data-stu-id="81dac-128">In the **Process qty.** field, enter a number.</span></span>
    * <span data-ttu-id="81dac-129">กำหนดจำนวนที่จะถูกประมวลผลในระหว่างการดำเนินงานหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="81dac-129">Determine how many will be processed during one operation.</span></span>  
1. <span data-ttu-id="81dac-130">ในฟิลด์ **ชั่วโมง/เวลา** ให้ป้อนหมายเลข</span><span class="sxs-lookup"><span data-stu-id="81dac-130">In the **Hours/time** field, enter a number.</span></span>
    * <span data-ttu-id="81dac-131">ป้อนอัตราส่วนเวลา</span><span class="sxs-lookup"><span data-stu-id="81dac-131">Enter the time ratio.</span></span>  
1. <span data-ttu-id="81dac-132">เลือกกล่องกาเครื่องหมาย **การตั้งค่า**</span><span class="sxs-lookup"><span data-stu-id="81dac-132">Select the **Set** check box.</span></span>
1. <span data-ttu-id="81dac-133">ในฟิลด์ **เวลาที่ใช้ในการผลิต** ให้ป้อนหมายเลข</span><span class="sxs-lookup"><span data-stu-id="81dac-133">In the **Run time** field, enter a number.</span></span>
    * <span data-ttu-id="81dac-134">กำหนดเวลาการประมวลผลสำหรับปริมาณที่คุณระบุ</span><span class="sxs-lookup"><span data-stu-id="81dac-134">Determine the processing time for the quantity that you have specified.</span></span>  
1. <span data-ttu-id="81dac-135">เลือกแท็บ **ความต้องการทรัพยากร**</span><span class="sxs-lookup"><span data-stu-id="81dac-135">Select the **Resource requirements** tab.</span></span>
1. <span data-ttu-id="81dac-136">เลือก **เพิ่ม**</span><span class="sxs-lookup"><span data-stu-id="81dac-136">Select **Add**.</span></span>
1. <span data-ttu-id="81dac-137">ในรายการนี้ ให้ทำเครื่องหมายแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="81dac-137">In the list, mark the selected row.</span></span>
1. <span data-ttu-id="81dac-138">ในฟิลด์ **ชนิดความต้องการ** ให้เลือกตัวเลือกหนึ่งตัวเลือก</span><span class="sxs-lookup"><span data-stu-id="81dac-138">In the **Requirement type** field, select an option.</span></span>
    * <span data-ttu-id="81dac-139">ตัดสินใจว่าคุณต้องการระบุทรัพยากรที่เฉพาะเจาะจงหรือความสามารถที่ต้องมีอยู่หรือไม่</span><span class="sxs-lookup"><span data-stu-id="81dac-139">Decide if you want to specify specific resources or capabilities that they must possess.</span></span>  
1. <span data-ttu-id="81dac-140">ในฟิลด์ **ความต้องการ** ให้ป้อนหรือเลือกค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="81dac-140">In the **Requirement** field, enter or select a value.</span></span>
1. <span data-ttu-id="81dac-141">เลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="81dac-141">Select **OK**.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]