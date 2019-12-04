---
title: การยืนยันยอดอัตโนมัติด้วยการเพิ่มประสิทธิภาพการวางแผน
description: หัวข้อนี้จะอธิบายถึงวิธีการใช้การยืนยันยอดอัตโนมัติด้วยการเพิ่มประสิทธิภาพการวางแผน
author: ChristianRytt
manager: AnnBe
ms.date: 11/05/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReqCreatePlanWorkspace
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2019-11-30
ms.dyn365.ops.version: AX 10.0.7
ms.openlocfilehash: 90319222e7357d7c54243faa8c64575377348467
ms.sourcegitcommit: 0138b6c108a10f2bcb90c91205da8092917160d8
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 11/11/2019
ms.locfileid: "2783164"
---
# <a name="auto-firming-with-planning-optimization"></a><span data-ttu-id="0b9b4-103">การยืนยันยอดอัตโนมัติด้วยการเพิ่มประสิทธิภาพการวางแผน</span><span class="sxs-lookup"><span data-stu-id="0b9b4-103">Auto-firming with Planning Optimization</span></span>

[!include [banner](../../includes/preview-banner.md)]
[!include [banner](../../includes/banner.md)]

<span data-ttu-id="0b9b4-104">การยืนยันยอดอัตโนมัติช่วยให้คุณมั่นใจได้ว่าจะมีแผนการใบสั่งเป็นส่วนหนึ่งของกระบวนการวางแผนหลัก</span><span class="sxs-lookup"><span data-stu-id="0b9b4-104">Automatic firming lets you firm (that is, release) planned orders as part of the master planning process.</span></span> <span data-ttu-id="0b9b4-105">เมื่อมีการยืนยันแผนการใบสั่ง จะมีการเปลี่ยนแปลงเป็นใบสั่งซื้อจริงใบสั่งโอนย้ายหรือใบสั่งผลิต</span><span class="sxs-lookup"><span data-stu-id="0b9b4-105">When planned orders are firmed, they are transformed into actual purchase orders, transfer orders, or production orders.</span></span> <span data-ttu-id="0b9b4-106">เมื่อมีการใช้การเพิ่มประสิทธิภาพการวางแผน ใบสั่งที่วางแผนไว้จะได้รับการยืนยันในระหว่างการวางแผนหลักซึ่งรันเมื่อวันที่ในใบสั่ง (นั่นคือวันที่เริ่มต้น) อยู่ภายในกรอบเวลาสำหรับการยืนยันยอด</span><span class="sxs-lookup"><span data-stu-id="0b9b4-106">When Planning Optimization is used, planned orders are firmed during a master planning run when the order date (that is, the start date) is within the time fence for firming.</span></span>

> [!NOTE]
> <span data-ttu-id="0b9b4-107">การยืนยันยอดแบบอัตโนมัติของแผนการใบสั่งซื้อสามารถเกิดขึ้นได้ เฉพาะเมื่อสินค้าเชื่อมโยงกับผู้จัดจำหน่าย</span><span class="sxs-lookup"><span data-stu-id="0b9b4-107">Auto-firming of a planned purchase order can occur only if the item is associated with a vendor.</span></span>

## <a name="turn-on-auto-firming"></a><span data-ttu-id="0b9b4-108">เปิดการยืนยันยอดอัตโนมัติ</span><span class="sxs-lookup"><span data-stu-id="0b9b4-108">Turn on auto-firming</span></span>

<span data-ttu-id="0b9b4-109">เมื่อต้องการเปิดใช้งานการยืนยันยอดอัตโนมัติ ให้ทำตามขั้นตอนต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="0b9b4-109">To turn on auto-firming, follow these steps.</span></span>

1. <span data-ttu-id="0b9b4-110">ในพื้นที่ทำงาน **การจัดการลักษณะ** บนแท็บ **ใหม่** ให้เลือก **การยืนยันอัตโนมัติสำหรับการเพิ่มประสิทธิภาพการวางแผน** ในรายการ</span><span class="sxs-lookup"><span data-stu-id="0b9b4-110">In the **Feature management** workspace, on the **New** tab, select **Auto-firming for Planning Optimization** in the list.</span></span> <span data-ttu-id="0b9b4-111">ถ้าคุณลักษณะไม่ปรากฏบนแท็บ **ใหม่** ให้ดูที่แท็บ **ไม่ได้เปิดใช้งาน** และ **ทั้งหมด**</span><span class="sxs-lookup"><span data-stu-id="0b9b4-111">If the feature doesn't appear on the **New** tab, look on the **Not enabled** and **All** tabs.</span></span>
1. <span data-ttu-id="0b9b4-112">เลือก **เปิดใช้งาน**</span><span class="sxs-lookup"><span data-stu-id="0b9b4-112">Select **Enable now**.</span></span> <span data-ttu-id="0b9b4-113">หรือเลือก **กำหนดการ** แล้วเลือกเวลาที่คุณต้องการเปิดใช้งานคุณลักษณะ</span><span class="sxs-lookup"><span data-stu-id="0b9b4-113">Alternatively, select **Schedule**, and then select the time when you want the feature to be turned on.</span></span>

## <a name="set-up-the-firming-time-fence"></a><span data-ttu-id="0b9b4-114">ตั้งค่ากรอบเวลาการยืนยัน</span><span class="sxs-lookup"><span data-stu-id="0b9b4-114">Set up the firming time fence</span></span>

<span data-ttu-id="0b9b4-115">กรอบเวลาการยืนยันจะคำนวณไปข้างหน้า จากวันที่ของการดำเนินการวางแผนหลัก</span><span class="sxs-lookup"><span data-stu-id="0b9b4-115">The firming time fence is calculated forward from the master planning run date.</span></span> <span data-ttu-id="0b9b4-116">จะถูกกำหนดโดยจำนวนวันปลอดหนี้ที่คุณกรอก</span><span class="sxs-lookup"><span data-stu-id="0b9b4-116">It's defined by the number of days that you enter.</span></span> <span data-ttu-id="0b9b4-117">คุณสามารถควบคุมกรอบเวลาการยืนยันได้ในลักษณะต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="0b9b4-117">You can control the firming time fence in the following ways:</span></span>

- <span data-ttu-id="0b9b4-118">เมื่อต้องการกำหนดค่าเริ่มต้นกรอบเวลาการยืนยันสำหรับกลุ่มความครอบคลุมให้ไปที่ **การวางแผนหลัก** \> **ตั้งค่า** \> **ความครอบคลุม** \> **กลุ่มความครอบคลุม** และเลือกกลุ่มความครอบคลุม</span><span class="sxs-lookup"><span data-stu-id="0b9b4-118">To define the default firming time fence for a coverage group, go to **Master planning** \> **Setup** \> **Coverage** \> **Coverage groups**, and select a coverage group.</span></span> <span data-ttu-id="0b9b4-119">จากนั้นบนแท็บด่วน **อื่น ๆ** ในฟิลด์ **กรอบเวลาการยืนยันเวลาอัตโนมัติ (วัน)** ให้ป้อนจำนวนวัน</span><span class="sxs-lookup"><span data-stu-id="0b9b4-119">Then, on the **Other** FastTab, in the **Automatic firming time fence (days)** field, enter the number of days.</span></span>
- <span data-ttu-id="0b9b4-120">เมื่อต้องการเขียนทับกรอบเวลาการยืนยันยอดที่กำหนดไว้ สำหรับกลุ่มความครอบคลุมสำหรับสินค้าเฉพาะให้ไปที่ **การจัดการข้อมูลผลิตภัณฑ์** \> **ผลิตภัณฑ์ที่นำออกใช้** แล้วจากบานหน้าต่างการดำเนินการ เลือก **แผน** แล้วเลือก **ความครอบคลุมสินค้า**</span><span class="sxs-lookup"><span data-stu-id="0b9b4-120">To overwrite the firming time fence that is defined for the coverage group for a specific item, go to **Product information management** \> **Released products**, then from the action pane select **Plan** and then select **Item coverage**.</span></span> <span data-ttu-id="0b9b4-121">จากนั้นบนแท็บ **ทั่วไป** เลือก **แทนที่กรอบเวลา** และในฟิลด์ **กรอบเวลาการยืนยันอัตโนมัติ (วัน)** ให้ป้อนจำนวนวัน</span><span class="sxs-lookup"><span data-stu-id="0b9b4-121">Then, on the **General** tab, select **Override time fence** and in the **Automatic firming time fence (days)** field, enter the number of days.</span></span>
- <span data-ttu-id="0b9b4-122">เมื่อต้องการเขียนทับกรอบเวลาการยืนยันยอดที่กำหนดไว้ สำหรับกลุ่มความครอบคลุม และความครอบคลุมสินค้า ให้ไปที่ **การวางแผนหลัก** \> **ตั้งค่า** \> **แผนหลัก** และเลือกแผนหลัก</span><span class="sxs-lookup"><span data-stu-id="0b9b4-122">To overwrite the firming time fence that is defined for the coverage group and item coverage for a specific master plan, go to **Master planning** \> **Setup** \> **Master plans**, and select a Master plan.</span></span> <span data-ttu-id="0b9b4-123">จากนั้นบนแท็บด่วน **กรอบเวลาในหน่วยวัน** ตั้งค่า **หยุด** เป็น **ใช่** และให้ป้อนจำนวนวัน</span><span class="sxs-lookup"><span data-stu-id="0b9b4-123">Then, on the **Time fence in days** FastTab, set **Freeze** to **Yes**, and enter the number of days.</span></span>

<span data-ttu-id="0b9b4-124">ถ้าเปิดใช้งานการยืนยันยอดอัตโนมัติสำหรับการรันการวางแผนหลักซึ่งใช้การเพิ่มประสิทธิภาพการวางแผน กระบวนการยืนยันอัตโนมัติจะทำตามการตั้งค่าการยืนยันโดยอัตโนมัติ</span><span class="sxs-lookup"><span data-stu-id="0b9b4-124">If auto-firming is turned on for a master planning run that uses Planning Optimization, the auto-firming process is done according to the auto-firming setup.</span></span> <span data-ttu-id="0b9b4-125">ถ้าไม่ได้เปิดใช้งานการยืนยันอัตโนมัติ หรือถ้าการวางแผนเริ่มต้นจากหน้า **ความต้องการสุทธิ** จะข้ามกระบวนการยืนยันอัตโนมัติ</span><span class="sxs-lookup"><span data-stu-id="0b9b4-125">If auto-firming isn't turned on, or if planning is started from the **Net requirements** page, the auto-firming process is skipped.</span></span>

## <a name="planning-optimization-vs-the-built-in-supply-chain-management-planning-engine"></a><span data-ttu-id="0b9b4-126">การเพิ่มประสิทธิภาพของการวางแผน เทียบกับกลไกการวางแผน Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="0b9b4-126">Planning Optimization vs. the built-in Supply Chain Management planning engine</span></span>

<span data-ttu-id="0b9b4-127">การเพิ่มประสิทธิภาพการวางแผนและกลไกจัดการการวางแผน ที่มีอยู่แล้วภายใน Microsoft Dynamics 365 Supply Chain Management สามารถใช้เพื่อกำหนดแผนการใบสั่งโดยอัตโนมัติได้</span><span class="sxs-lookup"><span data-stu-id="0b9b4-127">Both Planning Optimization and the planning engine that is built into Microsoft Dynamics 365 Supply Chain Management can be used to auto-firm planned orders.</span></span> <span data-ttu-id="0b9b4-128">อย่างไรก็ตาม มีความแตกต่างที่สำคัญบางประการ</span><span class="sxs-lookup"><span data-stu-id="0b9b4-128">However, there are some important differences.</span></span> <span data-ttu-id="0b9b4-129">ตัวอย่างเช่น ในขณะที่การเพิ่มประสิทธิภาพการวางแผนจะใช้วันที่ในใบสั่ง (นั่นคือวันที่เริ่มต้น) เพื่อกำหนดแผนการใบสั่งที่จะยืนยัน กดลไกการวางแผน Supply Chain Management ที่มีอยู่แล้วใช้วันที่ของความต้องการ (นั่นคือวันที่สิ้นสุด)</span><span class="sxs-lookup"><span data-stu-id="0b9b4-129">For example, whereas Planning Optimization uses the order date (that is, the start date) to determine which planned orders to firm, the built-in Supply Chain Management planning engine uses the requirement date (that is, the end date).</span></span> <span data-ttu-id="0b9b4-130">นี่คือสรุปของความแตกต่าง</span><span class="sxs-lookup"><span data-stu-id="0b9b4-130">Here is a summary of the differences.</span></span>

<span data-ttu-id="0b9b4-131">**การเพิ่มประสิทธิภาพการวางแผน**</span><span class="sxs-lookup"><span data-stu-id="0b9b4-131">**Planning Optimization**</span></span>

- <span data-ttu-id="0b9b4-132">การยืนยันโดยอัตโนมัติจะขึ้นอยู่กับวันที่ในใบสั่ง (วันที่เริ่มต้น)</span><span class="sxs-lookup"><span data-stu-id="0b9b4-132">Auto-firming is based on the order date (start date).</span></span>
- <span data-ttu-id="0b9b4-133">เนื่องจากวันที่ในใบสั่ง (วันที่เริ่มต้น) ทริกเกอร์การยืนยันคุณไม่จำเป็นต้องพิจารณาระยะเวลารอคอยสินค้าเป็นส่วนหนึ่งของกรอบเวลาการยืนยันยอด</span><span class="sxs-lookup"><span data-stu-id="0b9b4-133">Because the order date (start date) triggers the firming, you don't have to consider the lead time as part of the firming time fence.</span></span>
- <span data-ttu-id="0b9b4-134">ถ้าคุณต้องการยืนยันใบสั่งทั้งหมดที่ต้องเริ่มต้นระหว่างสัปดาห์ปัจจุบัน กรอบเวลาการยืนยันต้องเป็นหนึ่งสัปดาห์</span><span class="sxs-lookup"><span data-stu-id="0b9b4-134">If you want to firm all orders that must start during the current week, the firming time fence must be one week.</span></span>

<span data-ttu-id="0b9b4-135">**กลไกการวางแผน Supply Chain Management ที่มีอยู่**</span><span class="sxs-lookup"><span data-stu-id="0b9b4-135">**Built-in Supply Chain Management planning engine**</span></span>

- <span data-ttu-id="0b9b4-136">การยืนยันโดยอัตโนมัติจะขึ้นอยู่กับวันที่ตามความต้องการ (วันที่สิ้นสุด)</span><span class="sxs-lookup"><span data-stu-id="0b9b4-136">Auto-firming is based on the requirement date (end date).</span></span>
- <span data-ttu-id="0b9b4-137">เพื่อช่วยรับประกันว่าใบสั่งจะได้รับการยืนยันในเวลาครบกำหนด กรอบเวลาการยืนยันต้องยาวกว่าระยะเวลารอคอยสินค้า</span><span class="sxs-lookup"><span data-stu-id="0b9b4-137">To help guarantee that orders are firmed in due time, the firming time fence must be longer than the lead time.</span></span>
- <span data-ttu-id="0b9b4-138">ถ้าคุณต้องการยืนยันใบสั่งทั้งหมดที่ต้องเริ่มต้นระหว่างสัปดาห์ปัจจุบัน กรอบเวลาการยืนยันต้องเป็นระยะเวลารอคอยสินค้า บวกหนึ่งสัปดาห์</span><span class="sxs-lookup"><span data-stu-id="0b9b4-138">If you want to firm all orders that must start during the current week, the firming time fence must be the lead time plus one week.</span></span>
