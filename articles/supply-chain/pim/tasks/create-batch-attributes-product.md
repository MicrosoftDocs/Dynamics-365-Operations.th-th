---
title: สร้างแอททริบิวต์ของชุดงานสำหรับผลิตภัณฑ์
description: 'ขั้นตอนนี้แสดงวิธีการสร้างแอททริบิวต์ของชุดงาน กำหนดช่วงของค่าเริ่มต้น และรวมแอททริบิวต์ในกลุ่ม '
author: ShylaThompson
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: PdsBatchAttrib
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 5deb35028ee499633fb6b0bb5155df2fd91e643a
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 04/01/2021
ms.locfileid: "5820117"
---
# <a name="create-batch-attributes-for-a-product"></a><span data-ttu-id="9b6d4-103">สร้างแอททริบิวต์ของชุดงานสำหรับผลิตภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="9b6d4-103">Create batch attributes for a product</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="9b6d4-104">ขั้นตอนนี้แสดงวิธีการสร้างแอททริบิวต์ของชุดงาน กำหนดช่วงของค่าเริ่มต้น และรวมแอททริบิวต์ในกลุ่ม </span><span class="sxs-lookup"><span data-stu-id="9b6d4-104">This procedure shows how to create a batch attribute, assign default value ranges, and include the attribute in a group.</span></span> <span data-ttu-id="9b6d4-105">บริษัทข้อมูลสาธิตที่เคยสร้างขั้นตอนนี้คือบริษัท USP2</span><span class="sxs-lookup"><span data-stu-id="9b6d4-105">The demo data company used to create this procedure is the USP2 Company.</span></span>

1. <span data-ttu-id="9b6d4-106">ไปที่การบริหารสินค้าคงคลัง > การตั้งค่า > ชุดงาน > แอททริบิวต์ของชุดงาน</span><span class="sxs-lookup"><span data-stu-id="9b6d4-106">Go to Inventory management > Setup > Batch > Batch attributes.</span></span>
2. <span data-ttu-id="9b6d4-107">คลิก สร้าง</span><span class="sxs-lookup"><span data-stu-id="9b6d4-107">Click New.</span></span>
3. <span data-ttu-id="9b6d4-108">ในฟิลด์แอททริบิวท์ ให้พิมพ์ค่า</span><span class="sxs-lookup"><span data-stu-id="9b6d4-108">In the Attribute field, type a value.</span></span>
4. <span data-ttu-id="9b6d4-109">ในฟิลด์ คำอธิบาย ให้พิมพ์ค่า</span><span class="sxs-lookup"><span data-stu-id="9b6d4-109">In the Description field, type a value.</span></span>
5. <span data-ttu-id="9b6d4-110">ในฟิลด์ชนิดแอททริบิวต์ ให้เลือกเศษส่วน</span><span class="sxs-lookup"><span data-stu-id="9b6d4-110">In the Attribute type field, select 'Fraction'.</span></span>
    * <span data-ttu-id="9b6d4-111">ขั้นตอนนี้ใช้ชนิดเศษส่วนเพื่อเปิดใช้งานค่าทศนิยม </span><span class="sxs-lookup"><span data-stu-id="9b6d4-111">This procedure uses the Fraction type to enable decimal values.</span></span> <span data-ttu-id="9b6d4-112">คุณสามารถเลือกชนิดแอททริบิวต์อื่นๆ </span><span class="sxs-lookup"><span data-stu-id="9b6d4-112">You can select other attribute types.</span></span> <span data-ttu-id="9b6d4-113">ถ้าคุณเลือกชนิดการแจงนับ คุณต้องป้อนค่าในรายการแจงนับก่อนที่คุณจะสามารถป้อนค่าในฟิลด์เป้าหมาย</span><span class="sxs-lookup"><span data-stu-id="9b6d4-113">If you select the Enumeration type, you must enter values in the enumeration list before you can enter a value in the Target field.</span></span>  
6. <span data-ttu-id="9b6d4-114">ในฟิลด์ค่าน้อยที่สุด ให้ป้อนตัวเลข</span><span class="sxs-lookup"><span data-stu-id="9b6d4-114">In the Minimum field, enter a number.</span></span>
7. <span data-ttu-id="9b6d4-115">ในฟิลด์ค่าเยอะที่สุด ให้ป้อนตัวเลข</span><span class="sxs-lookup"><span data-stu-id="9b6d4-115">In the Maximum field, enter a number.</span></span>
8. <span data-ttu-id="9b6d4-116">ในฟิลด์การเพิ่ม ให้ป้อนตัวเลข</span><span class="sxs-lookup"><span data-stu-id="9b6d4-116">In the Increment field, enter a number.</span></span>
9. <span data-ttu-id="9b6d4-117">ในฟิลด์เป้าหมาย ให้พิมพ์ค่า</span><span class="sxs-lookup"><span data-stu-id="9b6d4-117">In the Target field, type a value.</span></span>
10. <span data-ttu-id="9b6d4-118">คลิก บันทึก</span><span class="sxs-lookup"><span data-stu-id="9b6d4-118">Click Save.</span></span>
11. <span data-ttu-id="9b6d4-119">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="9b6d4-119">Close the page.</span></span>
12. <span data-ttu-id="9b6d4-120">ไปที่การบริหารสินค้าคงคลัง > การตั้งค่า > ชุดงาน > กลุ่มแอททริบิวต์ของชุดงาน</span><span class="sxs-lookup"><span data-stu-id="9b6d4-120">Go to Inventory management > Setup > Batch > Batch attribute groups.</span></span>
13. <span data-ttu-id="9b6d4-121">คลิก สร้าง</span><span class="sxs-lookup"><span data-stu-id="9b6d4-121">Click New.</span></span>
14. <span data-ttu-id="9b6d4-122">ในฟิลด์กลุ่มแอททริบิวต์ ให้พิมพ์ค่า</span><span class="sxs-lookup"><span data-stu-id="9b6d4-122">In the Attribute group field, type a value.</span></span>
15. <span data-ttu-id="9b6d4-123">ในฟิลด์ คำอธิบาย ให้พิมพ์ค่า</span><span class="sxs-lookup"><span data-stu-id="9b6d4-123">In the Description field, type a value.</span></span>
16. <span data-ttu-id="9b6d4-124">คลิก บันทึก</span><span class="sxs-lookup"><span data-stu-id="9b6d4-124">Click Save.</span></span>
17. <span data-ttu-id="9b6d4-125">คลิกแอททริบิวต์กลุ่ม</span><span class="sxs-lookup"><span data-stu-id="9b6d4-125">Click Group attributes.</span></span>
18. <span data-ttu-id="9b6d4-126">คลิก สร้าง</span><span class="sxs-lookup"><span data-stu-id="9b6d4-126">Click New.</span></span>
19. <span data-ttu-id="9b6d4-127">ในฟิลด์แอททริบิวต์ ให้คลิกปุ่มดรอปดาวน์เพื่อเปิดการค้นหา</span><span class="sxs-lookup"><span data-stu-id="9b6d4-127">In the Attribute field, click the drop-down button to open the lookup.</span></span>
20. <span data-ttu-id="9b6d4-128">ในรายการนี้ ให้ค้นหาและเลือกเรกคอร์ดที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="9b6d4-128">In the list, find and select the desired record.</span></span>
21. <span data-ttu-id="9b6d4-129">ในรายการนี้ ให้คลิกลิงค์ในแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="9b6d4-129">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="9b6d4-130">แอททริบิวต์สามารถรวมอยู่ในกลุ่มใดก็ได้</span><span class="sxs-lookup"><span data-stu-id="9b6d4-130">An attribute can be included in any of the groups.</span></span>  
22. <span data-ttu-id="9b6d4-131">คลิก บันทึก</span><span class="sxs-lookup"><span data-stu-id="9b6d4-131">Click Save.</span></span>
23. <span data-ttu-id="9b6d4-132">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="9b6d4-132">Close the page.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]