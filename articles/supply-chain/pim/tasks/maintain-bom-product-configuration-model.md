---
title: รักษา BOM สำหรับแบบจำลองการจัดโครงแบบผลิตภัณฑ์
description: 'การดำเนินขั้นตอนนี้จำเป็นต้องมีแบบจำลองการตั้งค่าคอนฟิกรุ่นผลิตภัณฑ์ที่มีอยู่ '
author: ShylaThompson
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: DefaultDashboard, EcoResProductVariantMaintainWorkspace, PCProductConfigurationModelListPage, PCProductConfigurationModelDetails, PCBOMLineDetails, InventItemIdLookupSimple
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: b4ad73265e321b6339c061a7866b55cb2769954b
ms.sourcegitcommit: fa99a36c3d30d0c0577fd3f63ed6bf2f71599e40
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 04/20/2021
ms.locfileid: "5921328"
---
# <a name="maintain-bom-for-a-product-configuration-model"></a><span data-ttu-id="a0e8c-103">รักษา BOM สำหรับแบบจำลองการจัดโครงแบบผลิตภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="a0e8c-103">Maintain BOM for a product configuration model</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="a0e8c-104">การดำเนินขั้นตอนนี้จำเป็นต้องมีแบบจำลองการตั้งค่าคอนฟิกรุ่นผลิตภัณฑ์ที่มีอยู่ </span><span class="sxs-lookup"><span data-stu-id="a0e8c-104">Running this procedure requires an existing product configuration model.</span></span> <span data-ttu-id="a0e8c-105">แบบจำลองลำโพงขีดขั้นสูงในบริษัทสาธิต USMF จะใช้เพื่อสร้างกระบวนงานนี้</span><span class="sxs-lookup"><span data-stu-id="a0e8c-105">The High end speaker model in the demo company USMF is used to create this procedure.</span></span>

## <a name="add-a-bom-line"></a><span data-ttu-id="a0e8c-106">เพิมรายการ BOM</span><span class="sxs-lookup"><span data-stu-id="a0e8c-106">Add a BOM line</span></span>

1. <span data-ttu-id="a0e8c-107">ไปที่ **การจัดการข้อมูลผลิตภัณฑ์ \> ผลิตภัณฑ์ \> แบบจำลองการจัดโครงแบบผลิตภัณฑ์**</span><span class="sxs-lookup"><span data-stu-id="a0e8c-107">Go to **Product information management \> Products \> Product configuration models**.</span></span>
1. <span data-ttu-id="a0e8c-108">ในรายการนี้ ให้ค้นหาและเลือกเรกคอร์ดที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="a0e8c-108">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="a0e8c-109">เลือกลำโพงขั้นสูงสำหรับกระบวนงานนี้</span><span class="sxs-lookup"><span data-stu-id="a0e8c-109">Select the High end speaker for this procedure.</span></span>  
1. <span data-ttu-id="a0e8c-110">ในรายการนี้ ให้เลือกลิงค์ในแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="a0e8c-110">In the list, select the link in the selected row.</span></span>
1. <span data-ttu-id="a0e8c-111">ขยายส่วน **รายการ BOM**</span><span class="sxs-lookup"><span data-stu-id="a0e8c-111">Expand the **BOM lines** section.</span></span>
1. <span data-ttu-id="a0e8c-112">เลือก **เพิ่ม**</span><span class="sxs-lookup"><span data-stu-id="a0e8c-112">Select **Add**.</span></span>
1. <span data-ttu-id="a0e8c-113">ในฟิลด์ **ชื่อ** ให้พิมพ์ค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="a0e8c-113">In the **Name** field, type a value.</span></span>
1. <span data-ttu-id="a0e8c-114">ในฟิลด์ **คำอธิบาย** ให้พิมพ์ค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="a0e8c-114">In the **Description** field, type a value.</span></span>
1. <span data-ttu-id="a0e8c-115">เลือก **บันทึก**</span><span class="sxs-lookup"><span data-stu-id="a0e8c-115">Select **Save**.</span></span>

## <a name="add-bom-line-details"></a><span data-ttu-id="a0e8c-116">เพิ่มรายละเอียดรายการ BOM</span><span class="sxs-lookup"><span data-stu-id="a0e8c-116">Add BOM line details</span></span>

1. <span data-ttu-id="a0e8c-117">เลือก **รายละเอียดรายการ BOM**</span><span class="sxs-lookup"><span data-stu-id="a0e8c-117">Select **BOM line details**.</span></span>
2. <span data-ttu-id="a0e8c-118">ในฟิลด์ **หมายเลขสินค้า** ให้ป้อนหรือเลือกค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="a0e8c-118">In the **Item number** field, enter or select a value.</span></span>
    * <span data-ttu-id="a0e8c-119">ตัวอย่างเช่น คุณสามารถเลือกสินค้า M0055</span><span class="sxs-lookup"><span data-stu-id="a0e8c-119">For example, you can select the item M0055.</span></span>  
    * <span data-ttu-id="a0e8c-120">สำหรับแต่ละคุณสมบัติของรายการ BOM คุณสามารถเลือกได้ว่าจะเป็นค่าคงที่หรือมีการแม็ปไปที่คุณลักษณะ</span><span class="sxs-lookup"><span data-stu-id="a0e8c-120">For each BOM line property, you can select if it takes a fixed value or is mapped to an attribute.</span></span>  
3. <span data-ttu-id="a0e8c-121">เลือกกล่องกาเครื่องหมาย **การตั้งค่า**</span><span class="sxs-lookup"><span data-stu-id="a0e8c-121">Select the **Set** check box.</span></span>
4. <span data-ttu-id="a0e8c-122">เลือก *ใช่* ในฟิลด์ **การคำนวณ**</span><span class="sxs-lookup"><span data-stu-id="a0e8c-122">Select *Yes* in the **Calculation** field.</span></span>
    * <span data-ttu-id="a0e8c-123">การตั้งค่าคุณสมบัติ **การคำนวณ** เป็น *ใช่* ช่วยให้มั่นใจว่ารายการ BOM จะถูกรวมอยู่ในการคำนวณต้นทุน</span><span class="sxs-lookup"><span data-stu-id="a0e8c-123">Setting the **Calculation** property to *Yes* ensures that the BOM line is included in cost calculations.</span></span>  
5. <span data-ttu-id="a0e8c-124">เลือกแท็บ **การตั้งค่า**</span><span class="sxs-lookup"><span data-stu-id="a0e8c-124">Select the **Setup** tab.</span></span>
6. <span data-ttu-id="a0e8c-125">เลือกกล่องกาเครื่องหมาย **การตั้งค่า**</span><span class="sxs-lookup"><span data-stu-id="a0e8c-125">Select the **Set** check box.</span></span>
7. <span data-ttu-id="a0e8c-126">ในฟิลด์ **ปริมาณ** ให้ป้อนตัวเลข</span><span class="sxs-lookup"><span data-stu-id="a0e8c-126">In the **Quantity** field, enter a number.</span></span>
    * <span data-ttu-id="a0e8c-127">ฟิลด์ปริมาณกำหนดจำนวนของสินค้าที่จะรวมอยู่ใน BOM </span><span class="sxs-lookup"><span data-stu-id="a0e8c-127">The quantity field determines how much of the item that will be included in the BOM.</span></span> <span data-ttu-id="a0e8c-128">นี่อาจเป็นตัวเลือกที่ชัดเจนสำหรับการแม็ปคุณลักษณะ</span><span class="sxs-lookup"><span data-stu-id="a0e8c-128">This could be an obvious candidate for an attribute mapping.</span></span>  
8. <span data-ttu-id="a0e8c-129">เลือกแท็บ **มิติ**</span><span class="sxs-lookup"><span data-stu-id="a0e8c-129">Select the **Dimension** tab.</span></span>
    * <span data-ttu-id="a0e8c-130">ตรวจสอบถ้ามีมิติของผลิตภัณฑ์ใดๆมีการใช้งานอยู่ และดังนั้น ต้องมีค่าหรือคุณลักษณะที่กำหนดให้</span><span class="sxs-lookup"><span data-stu-id="a0e8c-130">Verify if any of the product dimensions are active,  and therefore must have a value or attribute assigned.</span></span>  
9. <span data-ttu-id="a0e8c-131">เลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="a0e8c-131">Select **OK**.</span></span>


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]