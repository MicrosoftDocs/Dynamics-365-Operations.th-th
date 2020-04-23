---
title: ตรวจสอบคุณภาพของสินค้า
description: หัวข้อนี้อธิบายวิธีการประมวลผลใบสั่งตรวจสอบคุณภาพ
author: perlynne
manager: tfehr
ms.date: 08/01/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventQualityOrderTable, InventQualityOrderLineResults, HcmWorkerLookUp
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: ee5f83b2dad60567341f33a73ce63d01e9da8289
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 04/02/2020
ms.locfileid: "3213986"
---
# <a name="inspect-the-quality-of-goods"></a><span data-ttu-id="180ab-103">ตรวจสอบคุณภาพของสินค้า</span><span class="sxs-lookup"><span data-stu-id="180ab-103">Inspect the quality of goods</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="180ab-104">หัวข้อนี้อธิบายวิธีการประมวลผลใบสั่งตรวจสอบคุณภาพ</span><span class="sxs-lookup"><span data-stu-id="180ab-104">This topic explains how to process a quality order.</span></span> <span data-ttu-id="180ab-105">คุณสามารถรันคำแนะนำนี้ในบริษัทข้อมูลสาธิต USMF</span><span class="sxs-lookup"><span data-stu-id="180ab-105">You can run this guide in demo data company USMF.</span></span> <span data-ttu-id="180ab-106">ก่อนที่คุณเริ่มกระบวนงานตัวอย่างนี้ คุณจำเป็นต้องยืนยันใบสั่งซื้อ "000016" และลงรายการบัญชีใบรับสินค้า</span><span class="sxs-lookup"><span data-stu-id="180ab-106">Before you start this example procedure, you need to confirm purchase order "000016" and post a product receipt.</span></span> <span data-ttu-id="180ab-107">ซึ่งจะสร้างใบสั่งตรวจสอบคุณภาพโดยอัตโนมัติ</span><span class="sxs-lookup"><span data-stu-id="180ab-107">This will automatically create a quality order.</span></span> <span data-ttu-id="180ab-108">ตรวจสอบคุณภาพจะโดยทั่วไปจะดำเนินการโดยเจ้าหน้าที่ตรวจสอบคุณภาพ</span><span class="sxs-lookup"><span data-stu-id="180ab-108">Quality inspections are typically carried out by a quality clerk.</span></span>


## <a name="select-a-quality-order"></a><span data-ttu-id="180ab-109">เลือกใบสั่งตรวจสอบคุณภาพ</span><span class="sxs-lookup"><span data-stu-id="180ab-109">Select a quality order</span></span>
1. <span data-ttu-id="180ab-110">ในบานหน้าต่างนำทาง ไปที่ **โมดูล > การจัดการสินค้าคงคลัง > งานประจำงวด > การจัดการคุณภาพ > ใบสั่งตรวจสอบคุณภาพ**</span><span class="sxs-lookup"><span data-stu-id="180ab-110">In the navigation pane, go to **Modules > Inventory management > Periodic tasks > Quality management > Quality orders**.</span></span>
2. <span data-ttu-id="180ab-111">เลือกใบสั่งตรวจสอบคุณภาพที่สร้างขึ้นก่อนที่คุณเริ่มต้นขั้นตอนนี้</span><span class="sxs-lookup"><span data-stu-id="180ab-111">Select the quality order that was created before you started this procedure.</span></span>  

## <a name="record-test-results"></a><span data-ttu-id="180ab-112">บันทึกผลการทดสอบ</span><span class="sxs-lookup"><span data-stu-id="180ab-112">Record test results</span></span>
1. <span data-ttu-id="180ab-113">เลือก **ผลลัพธ์**</span><span class="sxs-lookup"><span data-stu-id="180ab-113">Select **Results**.</span></span>
2. <span data-ttu-id="180ab-114">เลือก **แก้ไข**</span><span class="sxs-lookup"><span data-stu-id="180ab-114">Select **Edit**.</span></span>
3. <span data-ttu-id="180ab-115">ในฟิลด์ **ปริมาณผลลัพธ์** ให้ป้อนตัวเลข</span><span class="sxs-lookup"><span data-stu-id="180ab-115">In the **Result quantity** field, enter a number.</span></span>
4. <span data-ttu-id="180ab-116">ในฟิลด์ **ผลลัพธ์** ให้เลือกเรกคอร์ดที่ต้องการในเมนูแบบหล่นลง</span><span class="sxs-lookup"><span data-stu-id="180ab-116">In the **Outcome** field, select the desired record in the drop-down menu.</span></span>  
- <span data-ttu-id="180ab-117">ในตัวอย่างนี้ ผลลัพธ์จะขึ้นอยู่กับผลลัพธ์กำหนดไว้ </span><span class="sxs-lookup"><span data-stu-id="180ab-117">In this example the result is based on a pre-defined outcome.</span></span> <span data-ttu-id="180ab-118">โดยปกติแล้วคุณจะบันทึกผลการทดสอบเฉพาะเจาะจงยิ่งขึ้น ตัวอย่างเช่นขนาดหรือมิติอื่น</span><span class="sxs-lookup"><span data-stu-id="180ab-118">Normally you would record a more specific test result, for example a size or other dimension.</span></span>  
5. <span data-ttu-id="180ab-119">เลือก **บันทึก**</span><span class="sxs-lookup"><span data-stu-id="180ab-119">Select **Save**.</span></span>
6. <span data-ttu-id="180ab-120">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="180ab-120">Close the page.</span></span>

## <a name="validate-the-quality-order"></a><span data-ttu-id="180ab-121">ตรวจสอบความถูกต้องของใบสั่งตรวจสอบคุณภาพ</span><span class="sxs-lookup"><span data-stu-id="180ab-121">Validate the quality order</span></span>
1. <span data-ttu-id="180ab-122">เลือก **ตรวจสอบความถูกต้อง**</span><span class="sxs-lookup"><span data-stu-id="180ab-122">Select **Validate**.</span></span>
2. <span data-ttu-id="180ab-123">ในฟิลด์ **ตรวจสอบความถูกต้องตาม** ให้เลือกผู้ใช้ที่ดำเนินการตรวจสอบจากเมนูแบบหล่นลง</span><span class="sxs-lookup"><span data-stu-id="180ab-123">In the **Validated by** field, select the user performing the inspection from the drop-down menu.</span></span>  
3. <span data-ttu-id="180ab-124">คลิก **เลือก**</span><span class="sxs-lookup"><span data-stu-id="180ab-124">Click **Select**.</span></span>
4. <span data-ttu-id="180ab-125">เลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="180ab-125">Select **OK**.</span></span>
5. <span data-ttu-id="180ab-126">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="180ab-126">Close the page.</span></span>

