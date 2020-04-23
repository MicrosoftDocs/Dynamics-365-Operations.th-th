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
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: ShylaThompson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 815b6b726e9a76a9294995bc5689b030cf623ec0
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 04/02/2020
ms.locfileid: "3202594"
---
# <a name="create-a-template-bom"></a><span data-ttu-id="dd01f-103">การสร้าง BOM เท็มเพลต</span><span class="sxs-lookup"><span data-stu-id="dd01f-103">Create a template BOM</span></span>   

[!include [banner](../includes/banner.md)]


<span data-ttu-id="dd01f-104">คุณสามารถสร้าง BOM เท็มเพลตโดยใช้วิธีต่อไปนี้ </span><span class="sxs-lookup"><span data-stu-id="dd01f-104">You can create a template BOM by using any of the following methods.</span></span> <span data-ttu-id="dd01f-105">สำหรับวิธีต่างๆ ทั้งหมด ฟิลด์ **วันที่เริ่มต้น** และ **วันที่สิ้นสุด** จะเป็นตัวเลือก และเพื่อเป็นข้อมูลเท่านั้น</span><span class="sxs-lookup"><span data-stu-id="dd01f-105">For all methods, the **From date** and **To date** fields are optional and for information only.</span></span>

## <a name="create-a-template-bom-manually"></a><span data-ttu-id="dd01f-106">การสร้าง BOM เท็มเพลตด้วยตนเอง</span><span class="sxs-lookup"><span data-stu-id="dd01f-106">Create a template BOM manually</span></span>

1.  <span data-ttu-id="dd01f-107">คลิก **การจัดการบริการ** \> **ตั้งค่า** \> **วัตถุที่ให้บริการ** \> **BOMs เท็มเพลต**</span><span class="sxs-lookup"><span data-stu-id="dd01f-107">Click **Service management** \> **Setup** \> **Service objects** \> **Template BOMs**.</span></span>

2.  <span data-ttu-id="dd01f-108">กด CTRL+N เพื่อเปิดแบบฟอร์ม **สร้าง BOM เท็มเพลต**</span><span class="sxs-lookup"><span data-stu-id="dd01f-108">Press CTRL+N to open the **Create template BOM** form.</span></span>

3.  <span data-ttu-id="dd01f-109">ภายใต้ **คัดลอกรายการ BOM จากการอ้างอิง** เลือกตัวเลือก **แบบกำหนดเอง**</span><span class="sxs-lookup"><span data-stu-id="dd01f-109">Under **Copy BOM lines from reference**, select the **Manual** option.</span></span>

4.  <span data-ttu-id="dd01f-110">ในฟิลด์ **หมายเลขสินค้า** ให้ป้อนสินค้าของชนิด **BOM**</span><span class="sxs-lookup"><span data-stu-id="dd01f-110">In the **Item number** field, enter an item of the type **BOM**.</span></span>

5.  <span data-ttu-id="dd01f-111">ในฟิลด์ **ชื่อ** ให้ป้อนชื่อสำหรับเท็มเพลต</span><span class="sxs-lookup"><span data-stu-id="dd01f-111">In the **Name** field, enter a name for the template.</span></span>

6.  <span data-ttu-id="dd01f-112">ในฟิลด์ **วันที่เริ่มต้น** และ **วันที่สิ้นสุด** ให้ป้อนช่วงวันที่ที่ BOM เท็มเพลตมีการใช้งานอยู่</span><span class="sxs-lookup"><span data-stu-id="dd01f-112">In the **From date** and **To date** fields, enter a date interval in which the template BOM is active.</span></span>

7.  <span data-ttu-id="dd01f-113">คลิก **ตกลง** ระบบจะนำเข้าข้อมูลการชำระเงิน</span><span class="sxs-lookup"><span data-stu-id="dd01f-113">Click **OK**.</span></span>

<span data-ttu-id="dd01f-114">BOM เท็มเพลตเปล่าใหม่จะถูกสร้างขึ้น</span><span class="sxs-lookup"><span data-stu-id="dd01f-114">A new, blank template BOM is created.</span></span>

## <a name="create-a-template-bom-based-on-another-template-bom"></a><span data-ttu-id="dd01f-115">การสร้าง BOM เท็มเพลตโดยยึดตาม BOM เท็มเพลตอื่น</span><span class="sxs-lookup"><span data-stu-id="dd01f-115">Create a template BOM based on another template BOM</span></span>

1.  <span data-ttu-id="dd01f-116">คลิก **การจัดการบริการ** \> **ตั้งค่า** \> **วัตถุที่ให้บริการ** \> **BOMs เท็มเพลต**</span><span class="sxs-lookup"><span data-stu-id="dd01f-116">Click **Service management** \> **Setup** \> **Service objects** \> **Template BOMs**.</span></span>

2.  <span data-ttu-id="dd01f-117">กด CTRL+N เพื่อเปิดแบบฟอร์ม **สร้าง BOM เท็มเพลต**</span><span class="sxs-lookup"><span data-stu-id="dd01f-117">Press CTRL+N to open the **Create template BOM** form.</span></span>

3.  <span data-ttu-id="dd01f-118">ภายใต้ **คัดลอกรายการ BOM จากการอ้างอิง** เลือกตัวเลือก **BOM เท็มเพลต**</span><span class="sxs-lookup"><span data-stu-id="dd01f-118">Under **Copy BOM lines from reference**, select the **Template BOM** option.</span></span>

4.  <span data-ttu-id="dd01f-119">ในฟิลด์ **หมายเลขอ้างอิง** เลือก BOM เท็มเพลตที่มีอยู่ เพื่อคัดลอกไปยัง BOM เท็มเพลตใหม่ของคุณ</span><span class="sxs-lookup"><span data-stu-id="dd01f-119">In the **Reference number** field, select an existing template BOM to copy to your new template BOM.</span></span>

5.  <span data-ttu-id="dd01f-120">ในฟิลด์ **ชื่อ** ให้ป้อนชื่อสำหรับเท็มเพลต</span><span class="sxs-lookup"><span data-stu-id="dd01f-120">In the **Name** field, enter a name for the template.</span></span>

6.  <span data-ttu-id="dd01f-121">ในฟิลด์ **วันที่เริ่มต้น** และ **วันที่สิ้นสุด** ให้ป้อนช่วงวันที่ที่ BOM เท็มเพลตมีการใช้งานอยู่</span><span class="sxs-lookup"><span data-stu-id="dd01f-121">In the **From date** and **To date** fields, enter a date interval in which the template BOM is active.</span></span>

7.  <span data-ttu-id="dd01f-122">คลิก **ตกลง** ระบบจะนำเข้าข้อมูลการชำระเงิน</span><span class="sxs-lookup"><span data-stu-id="dd01f-122">Click **OK**.</span></span>

<span data-ttu-id="dd01f-123">BOM เท็มเพลตใหม่ที่รายการที่สอดคล้องกับบรรทัดใน BOM เท็มเพลตเดิมจะถูกสร้างขึ้น</span><span class="sxs-lookup"><span data-stu-id="dd01f-123">A new template BOM is created by using lines that correspond to the lines in the original template BOM.</span></span>

## <a name="create-a-template-bom-based-on-an-item-bom"></a><span data-ttu-id="dd01f-124">การสร้าง BOM เท็มเพลตโดยยึดตาม BOM สินค้า</span><span class="sxs-lookup"><span data-stu-id="dd01f-124">Create a template BOM based on an item BOM</span></span>

1.  <span data-ttu-id="dd01f-125">คลิก **การจัดการบริการ** \> **ตั้งค่า** \> **วัตถุที่ให้บริการ** \> **BOMs เท็มเพลต**</span><span class="sxs-lookup"><span data-stu-id="dd01f-125">Click **Service management** \> **Setup** \> **Service objects** \> **Template BOMs**.</span></span>

2.  <span data-ttu-id="dd01f-126">กด CTRL+N เพื่อเปิดแบบฟอร์ม **สร้าง BOM เท็มเพลต**</span><span class="sxs-lookup"><span data-stu-id="dd01f-126">Press CTRL+N to open the **Create template BOM** form.</span></span>

3.  <span data-ttu-id="dd01f-127">ภายใต้ **คัดลอกรายการ BOM จากการอ้างอิง** เลือก **BOM**</span><span class="sxs-lookup"><span data-stu-id="dd01f-127">Under **Copy BOM lines from reference**, select **BOM**.</span></span>

4.  <span data-ttu-id="dd01f-128">ในฟิลด์ **หมายเลขอ้างอิง** ให้เลือกเวอร์ชัน BOM</span><span class="sxs-lookup"><span data-stu-id="dd01f-128">In the **Reference number** field, select a BOM version.</span></span> <span data-ttu-id="dd01f-129">สินค้าของ BOM ชนิดจะถูกคัดลอกไปยัง **หมายเลขสินค้า**</span><span class="sxs-lookup"><span data-stu-id="dd01f-129">An item of the type BOM is copied to the **Item number**.</span></span>

5.  <span data-ttu-id="dd01f-130">ในฟิลด์ **ชื่อ** ให้ป้อนชื่อสำหรับเท็มเพลต</span><span class="sxs-lookup"><span data-stu-id="dd01f-130">In the **Name** field, enter a name for the template.</span></span>

6.  <span data-ttu-id="dd01f-131">ในฟิลด์ **วันที่เริ่มต้น** และ **วันที่สิ้นสุด** ให้ป้อนช่วงวันที่ที่ BOM เท็มเพลตมีการใช้งานอยู่</span><span class="sxs-lookup"><span data-stu-id="dd01f-131">In the **From date** and **To date** fields, enter a date interval in which the template BOM is active.</span></span>

7.  <span data-ttu-id="dd01f-132">คลิก **ตกลง** ระบบจะนำเข้าข้อมูลการชำระเงิน</span><span class="sxs-lookup"><span data-stu-id="dd01f-132">Click **OK**.</span></span>

<span data-ttu-id="dd01f-133">BOM เท็มเพลตใหม่จะถูกสร้างขึ้นโดยใช้รายการที่สอดคล้องกับรายการของ BOM ที่แสดงรายการใน **สูตรการผลิต**</span><span class="sxs-lookup"><span data-stu-id="dd01f-133">A new template BOM is created by using lines that correspond to the lines of the BOM listed in **Bills of materials**.</span></span>

## <a name="create-a-template-bom-based-on-a-production-bom"></a><span data-ttu-id="dd01f-134">การสร้าง BOM เท็มเพลตโดยยึดตาม BOM การผลิต</span><span class="sxs-lookup"><span data-stu-id="dd01f-134">Create a template BOM based on a production BOM</span></span>

1.  <span data-ttu-id="dd01f-135">คลิก **การจัดการบริการ** \> **ตั้งค่า** \> **วัตถุที่ให้บริการ** \> **BOMs เท็มเพลต**</span><span class="sxs-lookup"><span data-stu-id="dd01f-135">Click **Service management** \> **Setup** \> **Service objects** \> **Template BOMs**.</span></span>

2.  <span data-ttu-id="dd01f-136">กด CTRL+N เพื่อเปิดแบบฟอร์ม **สร้าง BOM เท็มเพลต**</span><span class="sxs-lookup"><span data-stu-id="dd01f-136">Press CTRL+N to open the **Create template BOM** form.</span></span>

3.  <span data-ttu-id="dd01f-137">ภายใต้ **คัดลอกรายการ BOM จากการอ้างอิง** เลือก **การผลิต**</span><span class="sxs-lookup"><span data-stu-id="dd01f-137">Under **Copy BOM lines from reference**, select **Production**.</span></span>

4.  <span data-ttu-id="dd01f-138">ในฟิลด์ **หมายเลขอ้างอิง** ให้เลือก BOM การผลิต</span><span class="sxs-lookup"><span data-stu-id="dd01f-138">In the **Reference number** field, select a production BOM.</span></span>

5.  <span data-ttu-id="dd01f-139">ในฟิลด์ **ชื่อ** ให้ป้อนชื่อสำหรับเท็มเพลต</span><span class="sxs-lookup"><span data-stu-id="dd01f-139">In the **Name** field, enter a name for the template.</span></span>

6.  <span data-ttu-id="dd01f-140">ในฟิลด์ **วันที่เริ่มต้น** และ **วันที่สิ้นสุด** ให้ป้อนช่วงวันที่ที่ BOM เท็มเพลตมีการใช้งานอยู่</span><span class="sxs-lookup"><span data-stu-id="dd01f-140">In the **From date** and **To date** fields, enter a date interval in which the template BOM is active.</span></span>

7.  <span data-ttu-id="dd01f-141">คลิก **ตกลง** ระบบจะนำเข้าข้อมูลการชำระเงิน</span><span class="sxs-lookup"><span data-stu-id="dd01f-141">Click **OK**.</span></span>

<span data-ttu-id="dd01f-142">BOM เท็มเพลตใหม่จะถูกสร้างขึ้นโดยใช้รายการที่สอดคล้องกับรายการของ BOM ที่แสดงรายการใน **BOM**</span><span class="sxs-lookup"><span data-stu-id="dd01f-142">A new template BOM is created by using lines that correspond to the lines of the BOM listed in **BOM**.</span></span>

## <a name="see-also"></a><span data-ttu-id="dd01f-143">ดูเพิ่มเติมที่</span><span class="sxs-lookup"><span data-stu-id="dd01f-143">See also</span></span>

[<span data-ttu-id="dd01f-144">BOM เท็มเพลต</span><span class="sxs-lookup"><span data-stu-id="dd01f-144">Template BOMs</span></span>](template-boms.md)

  


