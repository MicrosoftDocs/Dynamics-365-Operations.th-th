---
title: แก้ไขปัญหาตัวจัดโครงแบบผลิตภัณฑ์
description: หัวข้อนี้จะอธิบายวิธีการแก้ไขปัญหาที่คุณอาจพบขณะทำงานกับตัวจัดโครงแบบผลิตภัณฑ์
author: SmithaNataraj
manager: tfehr
ms.date: 11/04/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: smnatara
ms.search.validFrom: 2020-11-04
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: e6cfeb6a2b4166dfa9a5a5cc1b7d3d913b865ce2
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 01/15/2021
ms.locfileid: "4999617"
---
# <a name="troubleshoot-the-product-configurator"></a><span data-ttu-id="6a153-103">แก้ไขปัญหาตัวจัดโครงแบบผลิตภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="6a153-103">Troubleshoot the product configurator</span></span>

<span data-ttu-id="6a153-104">หัวข้อนี้จะอธิบายวิธีการแก้ไขปัญหาที่คุณอาจพบขณะทำงานกับตัวจัดโครงแบบผลิตภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="6a153-104">This topic describes how to fix issues that you might encounter while you work with the product configurator.</span></span>

## <a name="item-text-is-overwritten-when-i-configure-a-product-on-a-sales-order-line"></a><span data-ttu-id="6a153-105">ข้อความสินค้าจะถูกเขียนทับเมื่อตั้งค่าคอนฟิกผลิตภัณฑ์ในบรรทัดใบสั่งขาย</span><span class="sxs-lookup"><span data-stu-id="6a153-105">Item text is overwritten when I configure a product on a sales order line.</span></span>

### <a name="issue-description"></a><span data-ttu-id="6a153-106">คำอธิบายปัญหา</span><span class="sxs-lookup"><span data-stu-id="6a153-106">Issue description</span></span>

<span data-ttu-id="6a153-107">ปัญหานี้เกิดขึ้นเมื่อคุณสร้างบรรทัดใบสั่งขายสำหรับสินค้าที่จัดโครงแบบแล้วจึงปรับเปลี่ยนข้อความของสินค้า</span><span class="sxs-lookup"><span data-stu-id="6a153-107">This issue occurs when you create a sales order line for a configurable item and then modify the item text.</span></span> <span data-ttu-id="6a153-108">เมื่อคุณตั้งค่าคอนฟิกสินค้าแล้วเลือก **ตกลง** ข้อความจะถูกบันทึกทับด้วยข้อความมาตรฐาน</span><span class="sxs-lookup"><span data-stu-id="6a153-108">When you configure the item and then select **OK**, the text is overwritten with the standard text.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="6a153-109">การแก้ไขปัญหา</span><span class="sxs-lookup"><span data-stu-id="6a153-109">Issue resolution</span></span>

<span data-ttu-id="6a153-110">ลักษณะการทำงานนี้คาดการณ์ไว้</span><span class="sxs-lookup"><span data-stu-id="6a153-110">This behavior is expected.</span></span> <span data-ttu-id="6a153-111">ฟิลด์ข้อความประกอบด้วยชื่อตัวแปร ซึ่งจะถูกกรอกเฉพาะหลังจากที่คุณตั้งค่าคอนฟิกบรรทัด</span><span class="sxs-lookup"><span data-stu-id="6a153-111">The text field includes the variant name, which is filled in only after you configure the line.</span></span> <span data-ttu-id="6a153-112">ดังนั้น คุณต้องเปลี่ยนข้อความหลังจากที่คุณได้ตั้งค่าคอนฟิกบรรทัดแล้ว ไม่ใช่ก่อน</span><span class="sxs-lookup"><span data-stu-id="6a153-112">Therefore, you must change the text after you've configured the line, not before.</span></span>

## <a name="integer-attributes-are-incorrectly-rounded-when-product-configuration-models-are-calculated"></a><span data-ttu-id="6a153-113">แอททริบิวต์จำนวนเต็มจะถูกปัดเศษไม่ถูกต้องเมื่อคำนวณแบบจำลองการจัดโครงแบบผลิตภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="6a153-113">Integer attributes are incorrectly rounded when product configuration models are calculated.</span></span>

### <a name="issue-description"></a><span data-ttu-id="6a153-114">คำอธิบายปัญหา</span><span class="sxs-lookup"><span data-stu-id="6a153-114">Issue description</span></span>

<span data-ttu-id="6a153-115">ปัญหานี้อาจเกิดขึ้นเมื่อคุณดำเนินการชุดของการดำเนินการต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="6a153-115">This issue can occur when you perform the following series of actions:</span></span>

1. <span data-ttu-id="6a153-116">ตั้งค่าแอททริบิวต์ต่อไปนี้ในแบบจำลองการจัดโครงแบบการผลิต:</span><span class="sxs-lookup"><span data-stu-id="6a153-116">Set up the following attributes on a production configuration model:</span></span>

    - <span data-ttu-id="6a153-117">อินพุต (จำนวนเต็ม)</span><span class="sxs-lookup"><span data-stu-id="6a153-117">Input (integer)</span></span>
    - <span data-ttu-id="6a153-118">เปอร์เซ็นต์ (ฐานสิบ)</span><span class="sxs-lookup"><span data-stu-id="6a153-118">Percent (decimal)</span></span>
    - <span data-ttu-id="6a153-119">ผลลัพธ์ (จำนวนเต็ม)</span><span class="sxs-lookup"><span data-stu-id="6a153-119">Result (integer)</span></span>

2. <span data-ttu-id="6a153-120">สร้างการคำนวณที่มีนิพจน์ต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="6a153-120">Create a calculation that has the following expression:</span></span>

    <span data-ttu-id="6a153-121">*ผลลัพธ์* = *อินพุต* × *เปอร์เซ็นต์* ÷ 100</span><span class="sxs-lookup"><span data-stu-id="6a153-121">*Result* = *Input* × *Percent* ÷ 100</span></span>

<span data-ttu-id="6a153-122">ในกรณีนี้ ผลลัพธ์ของเลขจำนวนเต็มจะไม่ถูกปัดเศษอย่างถูกต้องเสมอไป</span><span class="sxs-lookup"><span data-stu-id="6a153-122">In this case, the integer result isn't always correctly rounded.</span></span> <span data-ttu-id="6a153-123">ตัวอย่างเช่น ถ้าอินพุตคือ 1,000 และเปอร์เซ็นต์คือ 2.40</span><span class="sxs-lookup"><span data-stu-id="6a153-123">For example, the input is 1,000, and the percentage is 2.40.</span></span> <span data-ttu-id="6a153-124">ดังนั้น คุณจึงคาดหวังให้ผลลัพธ์เลขจำนวนเต็มเป็น 24 เนื่องจาก 2.40 เปอร์เซ็นต์ของ 1,000 คือ 24 (หรือ 24.00 ในฟอร์มทศนิยม)</span><span class="sxs-lookup"><span data-stu-id="6a153-124">Therefore, you expect the integer result to be 24, because 2.40 percent of 1,000 is 24 (or 24.00 in decimal form).</span></span> <span data-ttu-id="6a153-125">ผลลัพธ์จะแสดงเป็น 23</span><span class="sxs-lookup"><span data-stu-id="6a153-125">Instead, the result is shown as 23.</span></span> <span data-ttu-id="6a153-126">อย่างไรก็ตาม เมื่อเปอร์เซ็นต์เป็น 2.39 จะมีการปัดเศษการคำนวณเป็น 24 แทนที่จะเป็น 23</span><span class="sxs-lookup"><span data-stu-id="6a153-126">However, when the percentage is 2.39, the calculation is rounded to 24 instead of 23.</span></span> <span data-ttu-id="6a153-127">เมื่อเปอร์เซ็นต์เป็น 2.50 จะมีการปัดเศษการคำนวณเป็น 25 ตามที่คาด</span><span class="sxs-lookup"><span data-stu-id="6a153-127">When the percentage is 2.50, the calculation is rounded to 25, as expected.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="6a153-128">การแก้ไขปัญหา</span><span class="sxs-lookup"><span data-stu-id="6a153-128">Issue resolution</span></span>

<span data-ttu-id="6a153-129">ปัญหานี้เกิดขึ้นเนื่องจากวิธีการที่ Microsoft Solver Foundation ภายในแสดงตัวเลขโดยใช้เศษส่วน</span><span class="sxs-lookup"><span data-stu-id="6a153-129">This issue occurs because of the way that Microsoft Solver Foundation internally represents numbers by using fractions.</span></span> <span data-ttu-id="6a153-130">สำหรับตัวอย่างก่อนหน้านี้ผลลัพธ์ของการคำนวณที่มีเปอร์เซ็นต์เป็น 2.40 แสดงเป็น 27021597764222975 ÷ 1125899906842624 = 23.99999999999999911182158029987476766109466552734375</span><span class="sxs-lookup"><span data-stu-id="6a153-130">For the preceding example, the result of the calculation where the percentage is 2.40 is represented as 27021597764222975 ÷ 1125899906842624 = 23.99999999999999911182158029987476766109466552734375.</span></span> <span data-ttu-id="6a153-131">เมื่อ .net เมื่อต้องการใช้ค่านี้เป็นจำนวนเต็ม จะมีการส่งคืน 23</span><span class="sxs-lookup"><span data-stu-id="6a153-131">When .NET casts this value as an integer, it will return 23.</span></span>

<span data-ttu-id="6a153-132">ลักษณะการทำงานนี้จะไม่มีการเปลี่ยนแปลง เนื่องจากสถานการณ์อื่น ๆ จะขึ้นอยู่กับสถานการณ์ดังกล่าว</span><span class="sxs-lookup"><span data-stu-id="6a153-132">This behavior won't be changed, because other scenarios depend on it.</span></span> <span data-ttu-id="6a153-133">สำหรับตัวอย่างก่อนหน้านี้ คุณสามารถแก้ไขปัญหานี้ได้โดยการแนะนำแอททริบิวต์ทศนิยมเพิ่มเติมและการคำนวณ</span><span class="sxs-lookup"><span data-stu-id="6a153-133">For the preceding example, you can fix the issue by introducing an additional decimal attribute and a calculation.</span></span>

<span data-ttu-id="6a153-134">ตัวอย่างคือ คุณสามารถตั้งค่าแอททริบิวต์ต่อไปนี้ในแบบจำลองการจัดโครงแบบการผลิต:</span><span class="sxs-lookup"><span data-stu-id="6a153-134">For example, you can set up the following attributes on a production configuration model:</span></span>

- <span data-ttu-id="6a153-135">อินพุต (จำนวนเต็ม)</span><span class="sxs-lookup"><span data-stu-id="6a153-135">Input (integer)</span></span>
- <span data-ttu-id="6a153-136">เปอร์เซ็นต์ (ฐานสิบ)</span><span class="sxs-lookup"><span data-stu-id="6a153-136">Percent (decimal)</span></span>
- <span data-ttu-id="6a153-137">ResultDecimal (ฐานสิบ)</span><span class="sxs-lookup"><span data-stu-id="6a153-137">ResultDecimal (decimal)</span></span>
- <span data-ttu-id="6a153-138">ResultInteger (จำนวนเต็ม)</span><span class="sxs-lookup"><span data-stu-id="6a153-138">ResultInteger (integer)</span></span>

<span data-ttu-id="6a153-139">คุณสามารถเพิ่มการคำนวณต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="6a153-139">You can then add the following calculations:</span></span>

- <span data-ttu-id="6a153-140">*ResultDecimal* = *อินพุต* × *เปอร์เซ็นต์* ÷ 100</span><span class="sxs-lookup"><span data-stu-id="6a153-140">*ResultDecimal* = *Input* × *Percent* ÷ 100</span></span>
- <span data-ttu-id="6a153-141">*ResultInteger* = *ResultDecimal*</span><span class="sxs-lookup"><span data-stu-id="6a153-141">*ResultInteger* = *ResultDecimal*</span></span>
