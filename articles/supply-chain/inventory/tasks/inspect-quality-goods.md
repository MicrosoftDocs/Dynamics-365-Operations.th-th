---
title: ตรวจสอบคุณภาพของสินค้า
description: หัวข้อนี้อธิบายวิธีการประมวลผลใบสั่งตรวจสอบคุณภาพ
author: perlynne
ms.date: 03/23/2021
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: InventQualityOrderTable, InventQualityOrderLineResults, HcmWorkerLookUp
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: ec67e7864db12178c0f3cfe8b93d510a46e8a0d4
ms.sourcegitcommit: 8362f3bd32ce8b9a5af93c8e57daef732a93b19e
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 04/28/2021
ms.locfileid: "5956145"
---
# <a name="inspect-the-quality-of-goods"></a><span data-ttu-id="02bf4-103">ตรวจสอบคุณภาพของสินค้า</span><span class="sxs-lookup"><span data-stu-id="02bf4-103">Inspect the quality of goods</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="02bf4-104">หัวข้อนี้อธิบายวิธีการประมวลผลใบสั่งตรวจสอบคุณภาพ</span><span class="sxs-lookup"><span data-stu-id="02bf4-104">This topic describes how to process quality orders.</span></span> <span data-ttu-id="02bf4-105">โดยทั่วไปการตรวจสอบคุณภาพจะดำเนินการโดยเจ้าหน้าที่ตรวจสอบคุณภาพ</span><span class="sxs-lookup"><span data-stu-id="02bf4-105">Quality inspections are typically done by a quality clerk.</span></span>

<span data-ttu-id="02bf4-106">ถ้ามีการติดตั้งข้อมูลสาธิตมาตรฐานแล้ว คุณสามารถใช้ข้อมูลสาธิตนั้นเพื่อปฏิบัติตามกระบวนงานต่างๆ ในหัวข้อนี้ให้เสร็จสมบูรณ์</span><span class="sxs-lookup"><span data-stu-id="02bf4-106">If the standard demo data is installed, you can use it to complete the procedures in this topic.</span></span> <span data-ttu-id="02bf4-107">เพื่อใช้ข้อมูลสาธิตนั้น เลือกนิติบุคคล *USMF* ก่อนที่คุณจะเริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="02bf4-107">To use the demo data, select the *USMF* legal entity before you begin.</span></span> <span data-ttu-id="02bf4-108">จากนั้น คุณต้องยืนยันใบสั่งซื้อ *000016* และลงรายการบัญชีใบรับสินค้า</span><span class="sxs-lookup"><span data-stu-id="02bf4-108">You must then confirm purchase order *000016* and post a product receipt.</span></span> <span data-ttu-id="02bf4-109">ใบสั่งตรวจสอบคุณภาพถูกสร้างขึ้นโดยอัตโนมัติ</span><span class="sxs-lookup"><span data-stu-id="02bf4-109">A quality order is automatically generated.</span></span>

## <a name="step-1-select-a-quality-order"></a><span data-ttu-id="02bf4-110">ขั้นตอนที่ 1: เลือกใบสั่งตรวจสอบคุณภาพ</span><span class="sxs-lookup"><span data-stu-id="02bf4-110">Step 1: Select a quality order</span></span>

<span data-ttu-id="02bf4-111">เพื่อเลือกใบสั่งตรวจสอบคุณภาพ ให้ปฏิบัติตามขั้นตอนเหล่านี้</span><span class="sxs-lookup"><span data-stu-id="02bf4-111">To select a quality order, follow these steps.</span></span>

1. <span data-ttu-id="02bf4-112">ไปที่ **การจัดการสินค้าคงคลัง \> งานประจำงวด \> การจัดการคุณภาพ \> ใบสั่งตรวจสอบคุณภาพ**</span><span class="sxs-lookup"><span data-stu-id="02bf4-112">Go to **Inventory management \> Periodic tasks \> Quality management \> Quality orders**.</span></span>
1. <span data-ttu-id="02bf4-113">เลือกใบสั่งตรวจสอบคุณภาพที่ถูกสร้างขึ้นก่อนที่จะคุณเริ่มต้นกระบวนงานนี้</span><span class="sxs-lookup"><span data-stu-id="02bf4-113">Select the quality order that was generated before you started this procedure.</span></span>

## <a name="step-2-record-test-results"></a><span data-ttu-id="02bf4-114">ขั้นตอนที่ 2: บันทึกผลการทดสอบ</span><span class="sxs-lookup"><span data-stu-id="02bf4-114">Step 2: Record test results</span></span>

<span data-ttu-id="02bf4-115">หากต้องการบันทึกผลการทดสอบ ให้ปฏิบัติตามขั้นตอนต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="02bf4-115">To record test results, follow these steps.</span></span>

1. <span data-ttu-id="02bf4-116">เลือก **ผลลัพธ์**</span><span class="sxs-lookup"><span data-stu-id="02bf4-116">Select **Results**.</span></span>
1. <span data-ttu-id="02bf4-117">เลือก **แก้ไข**</span><span class="sxs-lookup"><span data-stu-id="02bf4-117">Select **Edit**.</span></span>
1. <span data-ttu-id="02bf4-118">ในฟิลด์ **ปริมาณผลลัพธ์** ให้ป้อนตัวเลข</span><span class="sxs-lookup"><span data-stu-id="02bf4-118">In the **Result quantity** field, enter a number.</span></span>
1. <span data-ttu-id="02bf4-119">ในฟิลด์ **ผลลัพธ์** เลือกเรกคอร์ดที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="02bf4-119">In the **Outcome** field, select the desired record.</span></span> <span data-ttu-id="02bf4-120">ในตัวอย่างนี้ ผลลัพธ์จะขึ้นอยู่กับผลลัพธ์ที่กำหนดไว้ล่วงหน้า</span><span class="sxs-lookup"><span data-stu-id="02bf4-120">In this example, the result is based on a predefined outcome.</span></span> <span data-ttu-id="02bf4-121">โดยปกติแล้ว คุณจะบันทึกผลการทดสอบที่เฉพาะเจาะจงยิ่งขึ้น ตัวอย่างเช่น ขนาด หรือมิติอื่น</span><span class="sxs-lookup"><span data-stu-id="02bf4-121">Usually, you will record a more specific test result, such as a size or other dimension.</span></span>
1. <span data-ttu-id="02bf4-122">เลือก **บันทึก**</span><span class="sxs-lookup"><span data-stu-id="02bf4-122">Select **Save**.</span></span>
1. <span data-ttu-id="02bf4-123">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="02bf4-123">Close the page.</span></span>

## <a name="step-3-validate-the-quality-order"></a><span data-ttu-id="02bf4-124">ขั้นตอนที่ 3: ตรวจสอบความถูกต้องใบสั่งตรวจสอบคุณภาพ</span><span class="sxs-lookup"><span data-stu-id="02bf4-124">Step 3: Validate the quality order</span></span>

<span data-ttu-id="02bf4-125">เพื่อตรวจสอบความถูกต้องใบสั่งตรวจสอบคุณภาพ ให้ปฏิบัติตามขั้นตอนเหล่านี้</span><span class="sxs-lookup"><span data-stu-id="02bf4-125">To validate the quality order, follow these steps.</span></span>

1. <span data-ttu-id="02bf4-126">เลือก **ตรวจสอบความถูกต้อง**</span><span class="sxs-lookup"><span data-stu-id="02bf4-126">Select **Validate**.</span></span>
1. <span data-ttu-id="02bf4-127">ในฟิลด์ **ตรวจสอบความถูกต้องโดย** ให้เลือกผู้ใช้ที่เป็นผู้ตรวจสอบ</span><span class="sxs-lookup"><span data-stu-id="02bf4-127">In the **Validated by** field, select the user who is doing the inspection.</span></span>
1. <span data-ttu-id="02bf4-128">เลือก **เลือก**</span><span class="sxs-lookup"><span data-stu-id="02bf4-128">Select **Select**.</span></span>
1. <span data-ttu-id="02bf4-129">เลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="02bf4-129">Select **OK**.</span></span>
1. <span data-ttu-id="02bf4-130">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="02bf4-130">Close the page.</span></span>

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
