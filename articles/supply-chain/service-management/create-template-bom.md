---
title: การสร้าง BOM เท็มเพลต
description: คุณสามารถสร้าง BOM เท็มเพลตได้โดยใช้วิธีที่หลากหลายต่อไปนี้
author: ShylaThompson
manager: tfehr
ms.date: 05/01/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SMATemplateBOMTable
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 5afcb8171b674281faf8100d5c01fdff8d6ff764
ms.sourcegitcommit: 34b8f6f5c6134b7b97a9fb41d0b2e63215c67062
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 02/17/2021
ms.locfileid: "5470796"
---
# <a name="create-a-template-bom"></a><span data-ttu-id="1c77c-103">การสร้าง BOM เท็มเพลต</span><span class="sxs-lookup"><span data-stu-id="1c77c-103">Create a template BOM</span></span>   

[!include [banner](../includes/banner.md)]


<span data-ttu-id="1c77c-104">คุณสามารถสร้าง BOM เท็มเพลตโดยใช้วิธีต่อไปนี้ </span><span class="sxs-lookup"><span data-stu-id="1c77c-104">You can create a template BOM by using any of the following methods.</span></span> <span data-ttu-id="1c77c-105">สำหรับวิธีต่างๆ ทั้งหมด ฟิลด์ **วันที่เริ่มต้น** และ **วันที่สิ้นสุด** จะเป็นตัวเลือก และเพื่อเป็นข้อมูลเท่านั้น</span><span class="sxs-lookup"><span data-stu-id="1c77c-105">For all methods, the **From date** and **To date** fields are optional and for information only.</span></span>

## <a name="create-a-template-bom-manually"></a><span data-ttu-id="1c77c-106">การสร้าง BOM เท็มเพลตด้วยตนเอง</span><span class="sxs-lookup"><span data-stu-id="1c77c-106">Create a template BOM manually</span></span>

1.  <span data-ttu-id="1c77c-107">ไปยัง **การจัดการบริการ** \> **ตั้งค่า** \> **วัตถุที่ให้บริการ** \> **BOMs เท็มเพลต**</span><span class="sxs-lookup"><span data-stu-id="1c77c-107">Go to **Service management** \> **Setup** \> **Service objects** \> **Template BOMs**.</span></span>

2.  <span data-ttu-id="1c77c-108">เลือก **สร้าง** เพื่อเปิดฟอร์ม **สร้าง BOM เท็มเพลต**</span><span class="sxs-lookup"><span data-stu-id="1c77c-108">Select **New** to open the **Create template BOM** form.</span></span>

3.  <span data-ttu-id="1c77c-109">ภายใต้ **คัดลอกรายการ BOM จากการอ้างอิง** เลือกตัวเลือก **แบบกำหนดเอง**</span><span class="sxs-lookup"><span data-stu-id="1c77c-109">Under **Copy BOM lines from reference**, select the **Manual** option.</span></span>

4.  <span data-ttu-id="1c77c-110">ในฟิลด์ **หมายเลขสินค้า** ให้ป้อนสินค้าของชนิด **BOM**</span><span class="sxs-lookup"><span data-stu-id="1c77c-110">In the **Item number** field, enter an item of the type **BOM**.</span></span>

5.  <span data-ttu-id="1c77c-111">ในฟิลด์ **ชื่อ** ให้ป้อนชื่อสำหรับเท็มเพลต</span><span class="sxs-lookup"><span data-stu-id="1c77c-111">In the **Name** field, enter a name for the template.</span></span>

6.  <span data-ttu-id="1c77c-112">ในฟิลด์ **วันที่เริ่มต้น** และ **วันที่สิ้นสุด** ให้ป้อนช่วงวันที่ที่ BOM เท็มเพลตมีการใช้งานอยู่</span><span class="sxs-lookup"><span data-stu-id="1c77c-112">In the **From date** and **To date** fields, enter a date interval in which the template BOM is active.</span></span>

7.  <span data-ttu-id="1c77c-113">เลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="1c77c-113">Select **OK**.</span></span>

<span data-ttu-id="1c77c-114">BOM เท็มเพลตเปล่าใหม่จะถูกสร้างขึ้น</span><span class="sxs-lookup"><span data-stu-id="1c77c-114">A new, blank template BOM is created.</span></span>

## <a name="create-a-template-bom-based-on-another-template-bom"></a><span data-ttu-id="1c77c-115">การสร้าง BOM เท็มเพลตโดยยึดตาม BOM เท็มเพลตอื่น</span><span class="sxs-lookup"><span data-stu-id="1c77c-115">Create a template BOM based on another template BOM</span></span>

1.  <span data-ttu-id="1c77c-116">เลือก **การจัดการบริการ** \> **ตั้งค่า** \> **วัตถุที่ให้บริการ** \> **BOMs เท็มเพลต**</span><span class="sxs-lookup"><span data-stu-id="1c77c-116">Select **Service management** \> **Setup** \> **Service objects** \> **Template BOMs**.</span></span>

2.  <span data-ttu-id="1c77c-117">เลือก **สร้าง** เพื่อเปิดฟอร์ม **สร้าง BOM เท็มเพลต**</span><span class="sxs-lookup"><span data-stu-id="1c77c-117">Select **New** to open the **Create template BOM** form.</span></span>

3.  <span data-ttu-id="1c77c-118">ภายใต้ **คัดลอกรายการ BOM จากการอ้างอิง** เลือกตัวเลือก **BOM เท็มเพลต**</span><span class="sxs-lookup"><span data-stu-id="1c77c-118">Under **Copy BOM lines from reference**, select the **Template BOM** option.</span></span>

4.  <span data-ttu-id="1c77c-119">ในฟิลด์ **หมายเลขอ้างอิง** เลือก BOM เท็มเพลตที่มีอยู่ เพื่อคัดลอกไปยัง BOM เท็มเพลตใหม่ของคุณ</span><span class="sxs-lookup"><span data-stu-id="1c77c-119">In the **Reference number** field, select an existing template BOM to copy to your new template BOM.</span></span>

5.  <span data-ttu-id="1c77c-120">ในฟิลด์ **ชื่อ** ให้ป้อนชื่อสำหรับเท็มเพลต</span><span class="sxs-lookup"><span data-stu-id="1c77c-120">In the **Name** field, enter a name for the template.</span></span>

6.  <span data-ttu-id="1c77c-121">ในฟิลด์ **วันที่เริ่มต้น** และ **วันที่สิ้นสุด** ให้ป้อนช่วงวันที่ที่ BOM เท็มเพลตมีการใช้งานอยู่</span><span class="sxs-lookup"><span data-stu-id="1c77c-121">In the **From date** and **To date** fields, enter a date interval in which the template BOM is active.</span></span>

7.  <span data-ttu-id="1c77c-122">เลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="1c77c-122">Select **OK**.</span></span>

<span data-ttu-id="1c77c-123">BOM เท็มเพลตใหม่ที่รายการที่สอดคล้องกับบรรทัดใน BOM เท็มเพลตเดิมจะถูกสร้างขึ้น</span><span class="sxs-lookup"><span data-stu-id="1c77c-123">A new template BOM is created by using lines that correspond to the lines in the original template BOM.</span></span>

## <a name="create-a-template-bom-based-on-an-item-bom"></a><span data-ttu-id="1c77c-124">การสร้าง BOM เท็มเพลตโดยยึดตาม BOM สินค้า</span><span class="sxs-lookup"><span data-stu-id="1c77c-124">Create a template BOM based on an item BOM</span></span>

1.  <span data-ttu-id="1c77c-125">เลือก **การจัดการบริการ** \> **ตั้งค่า** \> **วัตถุที่ให้บริการ** \> **BOMs เท็มเพลต**</span><span class="sxs-lookup"><span data-stu-id="1c77c-125">Select **Service management** \> **Setup** \> **Service objects** \> **Template BOMs**.</span></span>

2.  <span data-ttu-id="1c77c-126">เลือก **สร้าง** เพื่อเปิดฟอร์ม **สร้าง BOM เท็มเพลต**</span><span class="sxs-lookup"><span data-stu-id="1c77c-126">Select **New** to open the **Create template BOM** form.</span></span>

3.  <span data-ttu-id="1c77c-127">ภายใต้ **คัดลอกรายการ BOM จากการอ้างอิง** เลือก **BOM**</span><span class="sxs-lookup"><span data-stu-id="1c77c-127">Under **Copy BOM lines from reference**, select **BOM**.</span></span>

4.  <span data-ttu-id="1c77c-128">ในฟิลด์ **หมายเลขอ้างอิง** ให้เลือกเวอร์ชัน BOM</span><span class="sxs-lookup"><span data-stu-id="1c77c-128">In the **Reference number** field, select a BOM version.</span></span> <span data-ttu-id="1c77c-129">สินค้าของ BOM ชนิดจะถูกคัดลอกไปยัง **หมายเลขสินค้า**</span><span class="sxs-lookup"><span data-stu-id="1c77c-129">An item of the type BOM is copied to the **Item number**.</span></span>

5.  <span data-ttu-id="1c77c-130">ในฟิลด์ **ชื่อ** ให้ป้อนชื่อสำหรับเท็มเพลต</span><span class="sxs-lookup"><span data-stu-id="1c77c-130">In the **Name** field, enter a name for the template.</span></span>

6.  <span data-ttu-id="1c77c-131">ในฟิลด์ **วันที่เริ่มต้น** และ **วันที่สิ้นสุด** ให้ป้อนช่วงวันที่ที่ BOM เท็มเพลตมีการใช้งานอยู่</span><span class="sxs-lookup"><span data-stu-id="1c77c-131">In the **From date** and **To date** fields, enter a date interval in which the template BOM is active.</span></span>

7.  <span data-ttu-id="1c77c-132">เลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="1c77c-132">Select **OK**.</span></span>

<span data-ttu-id="1c77c-133">BOM เท็มเพลตใหม่จะถูกสร้างขึ้นโดยใช้รายการที่สอดคล้องกับรายการของ BOM ที่แสดงรายการใน **สูตรการผลิต**</span><span class="sxs-lookup"><span data-stu-id="1c77c-133">A new template BOM is created by using lines that correspond to the lines of the BOM listed in **Bills of materials**.</span></span>

## <a name="create-a-template-bom-based-on-a-production-bom"></a><span data-ttu-id="1c77c-134">การสร้าง BOM เท็มเพลตโดยยึดตาม BOM การผลิต</span><span class="sxs-lookup"><span data-stu-id="1c77c-134">Create a template BOM based on a production BOM</span></span>

1.  <span data-ttu-id="1c77c-135">เลือก **การจัดการบริการ** \> **ตั้งค่า** \> **วัตถุที่ให้บริการ** \> **BOMs เท็มเพลต**</span><span class="sxs-lookup"><span data-stu-id="1c77c-135">Select **Service management** \> **Setup** \> **Service objects** \> **Template BOMs**.</span></span>

2.  <span data-ttu-id="1c77c-136">เลือก **สร้าง** เพื่อเปิดฟอร์ม **สร้าง BOM เท็มเพลต**</span><span class="sxs-lookup"><span data-stu-id="1c77c-136">Select **New** to open the **Create template BOM** form.</span></span>

3.  <span data-ttu-id="1c77c-137">ภายใต้ **คัดลอกรายการ BOM จากการอ้างอิง** เลือก **การผลิต**</span><span class="sxs-lookup"><span data-stu-id="1c77c-137">Under **Copy BOM lines from reference**, select **Production**.</span></span>

4.  <span data-ttu-id="1c77c-138">ในฟิลด์ **หมายเลขอ้างอิง** ให้เลือก BOM การผลิต</span><span class="sxs-lookup"><span data-stu-id="1c77c-138">In the **Reference number** field, select a production BOM.</span></span>

5.  <span data-ttu-id="1c77c-139">ในฟิลด์ **ชื่อ** ให้ป้อนชื่อสำหรับเท็มเพลต</span><span class="sxs-lookup"><span data-stu-id="1c77c-139">In the **Name** field, enter a name for the template.</span></span>

6.  <span data-ttu-id="1c77c-140">ในฟิลด์ **วันที่เริ่มต้น** และ **วันที่สิ้นสุด** ให้ป้อนช่วงวันที่ที่ BOM เท็มเพลตมีการใช้งานอยู่</span><span class="sxs-lookup"><span data-stu-id="1c77c-140">In the **From date** and **To date** fields, enter a date interval in which the template BOM is active.</span></span>

7.  <span data-ttu-id="1c77c-141">เลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="1c77c-141">Select **OK**.</span></span>

<span data-ttu-id="1c77c-142">BOM เท็มเพลตใหม่จะถูกสร้างขึ้นโดยใช้รายการที่สอดคล้องกับรายการของ BOM ที่แสดงรายการใน **BOM**</span><span class="sxs-lookup"><span data-stu-id="1c77c-142">A new template BOM is created by using lines that correspond to the lines of the BOM listed in **BOM**.</span></span>

## <a name="see-also"></a><span data-ttu-id="1c77c-143">ดูเพิ่มเติมที่</span><span class="sxs-lookup"><span data-stu-id="1c77c-143">See also</span></span>

[<span data-ttu-id="1c77c-144">BOM เท็มเพลต</span><span class="sxs-lookup"><span data-stu-id="1c77c-144">Template BOMs</span></span>](template-boms.md)

  




[!INCLUDE[footer-include](../../includes/footer-banner.md)]