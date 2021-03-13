---
title: หน่วยวัดทางสินทรัพย์
description: หัวข้อจะอธิบายวิธีการสร้างชนิดหน่วยวัดทางสินทรัพย์ในการจัดการสินทรัพย์
author: josaw1
manager: tfehr
ms.date: 10/15/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EntAssetObjectCounterPart, EntAssetObjectCounterLookup, EntAssetCounterType, EntAssetObjectCounterTotals
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: riluan
ms.search.validFrom: 2019-09-30
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 37f47b3d9ba0344b96db5626359e2a99a1a40f9c
ms.sourcegitcommit: deac22ba5377a912d93fe408c5ae875706378c2d
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 01/16/2021
ms.locfileid: "5018532"
---
# <a name="counters"></a><span data-ttu-id="46af5-103">ตัวนับ</span><span class="sxs-lookup"><span data-stu-id="46af5-103">Counters</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="46af5-104">หัวข้อจะอธิบายวิธีการสร้างชนิดตัวนับในการจัดการสินทรัพย์</span><span class="sxs-lookup"><span data-stu-id="46af5-104">The topic explains how to create counter types in Asset Management.</span></span> <span data-ttu-id="46af5-105">ชนิดของตัวนับจะใช้เพื่อทำการลงทะเบียนตัวนับในสินทรัพย์ ตัวอย่างเช่น ซึ่งเกี่ยวข้องกับจำนวนของชั่วโมงการผลิตหรือปริมาณที่ผลิตในสินทรัพย์</span><span class="sxs-lookup"><span data-stu-id="46af5-105">Counter types are used to make counter registrations on assets, for example, regarding number of production hours, or quantity produced on the asset.</span></span> <span data-ttu-id="46af5-106">ชนิดของสินทรัพย์เกี่ยวข้องกับชนิดของตัวนับ</span><span class="sxs-lookup"><span data-stu-id="46af5-106">Asset types are related to the counter types.</span></span> <span data-ttu-id="46af5-107">นี่หมายความว่า สามารถใช้ตัวนับได้ในสินทรัพย์เท่านั้น ถ้ามีการตั้งค่าตัวนับในชนิดสินทรัพย์ที่ใช้ในสินทรัพย์</span><span class="sxs-lookup"><span data-stu-id="46af5-107">This means that a counter can only be used on an asset if the counter is set up on the asset type used on the asset.</span></span>

<span data-ttu-id="46af5-108">ก่อนที่คุณจะสามารถทำการลงทะเบียนตัววัดได้ ก่อนอื่นคุณต้องสร้างชนิดตัววัดที่คุณต้องการใช้ใน **ตัวนับ**</span><span class="sxs-lookup"><span data-stu-id="46af5-108">Before you can make counter registrations on assets, you first create the counter types you want to use in **Counters**.</span></span> <span data-ttu-id="46af5-109">ถัดไป คุณสามารถสร้างการลงทะเบียนตัวนับในสินทรัพย์ได้ใน **ตัวนับ**</span><span class="sxs-lookup"><span data-stu-id="46af5-109">Next, you can create counter registrations on assets in **Counters**.</span></span> 

<span data-ttu-id="46af5-110">สามารถใช้ตัวนับในแผนการบำรุงรักษาได้</span><span class="sxs-lookup"><span data-stu-id="46af5-110">Counters can be used on maintenance plans.</span></span> <span data-ttu-id="46af5-111">รายการแผนการบำรุงรักษาสามารถเป็นชนิด "ตัวนับ" ตัวอย่างเช่น ซึ่งเกี่ยวข้องกับจำนวนของชั่วโมงการผลิตหรือปริมาณที่ผลิต</span><span class="sxs-lookup"><span data-stu-id="46af5-111">A maintenance plan line can be of type "Counter", for example, relating to number of production hours or quantity produced.</span></span> 

<span data-ttu-id="46af5-112">การลงทะเบียนตัวนับสามารถอัพเดตได้ด้วยตนเองหรือโดยอัตโนมัติตามชั่วโมงการผลิตหรือปริมาณที่ผลิต</span><span class="sxs-lookup"><span data-stu-id="46af5-112">A counter registration can be updated manually or automatically based on production hours or quantity produced.</span></span> <span data-ttu-id="46af5-113">คุณสามารถตั้งค่าตัวนับเพื่อใช้วิธีการอัพเดตหนึ่งในสามวิธีนี้ (ซึ่งเลือกในฟิลด์ **อัพเดต** ใน **ตัวนับ**):</span><span class="sxs-lookup"><span data-stu-id="46af5-113">A counter can be set up to use one of three update methods (selected in the **Update** field in **Counters**):</span></span>
  
- <span data-ttu-id="46af5-114">ด้วยตนเอง - คุณต้องลงทะเบียนมูลค่าตัวนับด้วยตนเอง</span><span class="sxs-lookup"><span data-stu-id="46af5-114">Manual - you must manually register counter values.</span></span>  
- <span data-ttu-id="46af5-115">ชั่วโมงการผลิต - จะปรับปรุงตัวนับโดยอัตโนมัติตามจำนวนของชั่วโมงการผลิต</span><span class="sxs-lookup"><span data-stu-id="46af5-115">Production hours - the counter is automatically updated based on number of production hours.</span></span>  
- <span data-ttu-id="46af5-116">ปริมาณการผลิต - จะปรับปรุงตัวนับโดยอัตโนมัติตามจำนวนของปริมาณที่ผลิต</span><span class="sxs-lookup"><span data-stu-id="46af5-116">Production quantity - the counter is automatically updated based on number of quantity produced.</span></span>  

>[!NOTE]
><span data-ttu-id="46af5-117">ถ้าปริมาณที่ผลิตถูกใช้ สินค้าที่ลงทะเบียนทั้งหมด *ทั้งหมด* จะถูกรวมอยู่ในการลงทะเบียนตัวนับ ปริมาณที่ดี และปริมาณสินค้าที่บกพร่อง</span><span class="sxs-lookup"><span data-stu-id="46af5-117">If quantity produced is used, *all* registered items are included in the counter registration, good quantity as well as error quantity.</span></span> <span data-ttu-id="46af5-118">เป็นไปได้เสมอที่จะทำการลงทะเบียนตัววัดด้วยตนเอง ถ้าจำเป็น</span><span class="sxs-lookup"><span data-stu-id="46af5-118">It is always possible to make manual counter registrations, if required.</span></span>

## <a name="create-counter-types-for-asset-counter-registrations"></a><span data-ttu-id="46af5-119">สร้างชนิดของตัวนับสำหรับการลงทะเบียนตัวนับสินทรัพย์</span><span class="sxs-lookup"><span data-stu-id="46af5-119">Create counter types for asset counter registrations</span></span>

1. <span data-ttu-id="46af5-120">เลือก **การจัดการสินทรัพย์** > **การตั้งค่า** > **ชนิดสินทรัพย์** > **ตัวนับ**</span><span class="sxs-lookup"><span data-stu-id="46af5-120">Select **Asset management** > **Setup** > **Asset types** > **Counters**.</span></span>
2. <span data-ttu-id="46af5-121">เลือก **สร้าง** เพื่อสร้างชนิดตัววัดใหม่</span><span class="sxs-lookup"><span data-stu-id="46af5-121">Select **New** to create a new counter type.</span></span>
3. <span data-ttu-id="46af5-122">แทรกรหัสลงในฟิลด์ **ตัวนับ** และชื่อตัวนับในฟิลด์ **ชื่อ**</span><span class="sxs-lookup"><span data-stu-id="46af5-122">Insert an ID in the **Counter** field, and a counter name in the **Name** field.</span></span>
4. <span data-ttu-id="46af5-123">บนแท็บด่วน **ทั่วไป** ให้เลือกหน่วยตัววัดในฟิลด์ **หน่วย**</span><span class="sxs-lookup"><span data-stu-id="46af5-123">On the **General** FastTab, select a counter unit in the **Unit** field.</span></span>
5. <span data-ttu-id="46af5-124">ในฟิลด์ **อัพเดต** ให้เลือกวิธีการอัพเดตที่จะใช้สำหรับตัวนับ</span><span class="sxs-lookup"><span data-stu-id="46af5-124">In the **Update** field, select the update method to be used for the counter.</span></span>
6. <span data-ttu-id="46af5-125">เลือก "ใช่" บนปุ่มสลับ **สืบทอดค่าตัวนับ** ถ้าสินทรัพย์รองในโครงสร้างสินทรัพย์ควรสืบทอดการลงทะเบียนตัวนับที่ทำบนสินทรัพย์หลักโดยอัตโนมัติ</span><span class="sxs-lookup"><span data-stu-id="46af5-125">Select "Yes" on the **Inherit counter values** toggle button if child assets in an asset structure should automatically inherit counter registrations made on the parent asset.</span></span>
7. <span data-ttu-id="46af5-126">ในฟิลด์ **ผลรวมทั้งหมด** ให้เลือกวิธีการรวมที่จะใช้สำหรับตัวนับโดยใช้ชนิดตัวนับนี้</span><span class="sxs-lookup"><span data-stu-id="46af5-126">In the **Total aggregate** field, select the summation method to be used for a counter using this counter type.</span></span> <span data-ttu-id="46af5-127">"รวม" คือตัวเลือกมาตรฐานที่ใช้ในการเพิ่มค่าที่ลงทะเบียนไปยังมูลค่ารวมอย่างต่อเนื่อง</span><span class="sxs-lookup"><span data-stu-id="46af5-127">"Sum" is the standard selection used to continuously add registered values to the total value.</span></span> <span data-ttu-id="46af5-128">"ค่าเฉลี่ย" สามารถใช้ได้ ถ้ามีการตั้งค่าตัวนับเพื่อตรวจสอบขีดจำกัด ตัวอย่างเช่น ซึ่งเกี่ยวกับอุณหภูมิ การสั่นสะเทือน หรือการสึกหรอและการฉีกขาดของสินทรัพย์</span><span class="sxs-lookup"><span data-stu-id="46af5-128">"Average" can be used if a counter is set up to monitor a threshold, for example, regarding temperature, vibrations, or wear and tear on an asset.</span></span> 
8. <span data-ttu-id="46af5-129">ในฟิลด์ **ความเบี่ยงเบนสูงกว่า** ให้แทรกระดับบนเป็นเปอร์เซ็นต์สำหรับการตรวจสอบความถูกต้อง ถ้าการลงทะเบียนตัวนับด้วยตนเองอยู่ภายในช่วงที่คาดไว้</span><span class="sxs-lookup"><span data-stu-id="46af5-129">In the **Deviation over** field, insert the upper level in percent for validating if manual counter registrations are within an expected range.</span></span> <span data-ttu-id="46af5-130">การตรวจสอบความถูกต้องจะขึ้นอยู่กับการเพิ่มขึ้นเชิงเส้นในการลงทะเบียนตัวนับที่มีอยู่</span><span class="sxs-lookup"><span data-stu-id="46af5-130">The validation is based on a linear increase in existing counter registrations.</span></span>
9. <span data-ttu-id="46af5-131">ในฟิลด์ **ความเบี่ยงเบนต่ำกว่า** ให้แทรกระดับล่างเป็นเปอร์เซ็นต์สำหรับการตรวจสอบความถูกต้อง ถ้าการลงทะเบียนตัวนับด้วยตนเองอยู่ภายในช่วงที่คาดไว้</span><span class="sxs-lookup"><span data-stu-id="46af5-131">In the **Deviation under** field, insert the lower level in percent for validating if manual counter registrations are within an expected range.</span></span> <span data-ttu-id="46af5-132">การตรวจสอบความถูกต้องจะขึ้นอยู่กับการลดลงเชิงเส้นในการลงทะเบียนตัวนับที่มีอยู่</span><span class="sxs-lookup"><span data-stu-id="46af5-132">The validation is based on a linear decrease in existing counter registrations.</span></span>
10. <span data-ttu-id="46af5-133">ในฟิลด์ **ชนิด** ให้เลือกชนิดของข้อความ (ข้อมูล คำเตือน ข้อผิดพลาด) ที่จะถูกแสดง ถ้าส่วนเบี่ยงเบนนอกช่วงที่กำหนดเกิด เมื่อคุณทำการลงทะเบียนตัวนับด้วยตนเอง</span><span class="sxs-lookup"><span data-stu-id="46af5-133">In the **Type** field, select the type of message (information, warning, error) to be shown if deviations outside the defined range occur when you make manual counter registrations.</span></span>
11. <span data-ttu-id="46af5-134">บนแท็บด่วน **ชนิดสินทรัพย์** ให้เพิ่มชนิดสินทรัพย์ที่ควรสามารถใช้ตัวนับได้</span><span class="sxs-lookup"><span data-stu-id="46af5-134">On the **Asset types** FastTab, add the asset types that should be able to use the counter.</span></span>
12. <span data-ttu-id="46af5-135">บนแท็บด่วน **ตัวนับทางสินทรัพย์ที่เกี่ยวข้อง** ให้เพิ่มตัวนับที่คุณต้องการได้รับการอัพเดตโดยอัตโนมัติ เมื่อมีการอัพเดตตัวนับนี้</span><span class="sxs-lookup"><span data-stu-id="46af5-135">On the **Related asset counters** FastTab, add the counter that you want to be automatically updated when this counter is updated.</span></span>


>[!NOTE]
><span data-ttu-id="46af5-136">ตัวนับที่เกี่ยวข้องจะมีการอัพเดตโดยอัตโนมัติ เฉพาะเมื่อตัวนับที่เกี่ยวข้องมีชนิดสินทรัพย์ซึ่งเกี่ยวข้องในการตั้งค่าตัวนับ</span><span class="sxs-lookup"><span data-stu-id="46af5-136">A related counter is automatically updated only if the related counter has the asset type, to which it is related, in the counter setup.</span></span> <span data-ttu-id="46af5-137">ตัวอย่างเช่น: คุณตั้งค่าตัวนับสำหรับ "ชั่วโมงการผลิต" และเพิ่มประเภทสินทรัพย์ "เครื่องยนต์รถบรรทุก"</span><span class="sxs-lookup"><span data-stu-id="46af5-137">For example: You set up a counter for "Production hours" and add the asset type "Truck Engine".</span></span> <span data-ttu-id="46af5-138">เมื่อมีการอัพเดตตัวนับ จะมีการอัพเดตตัวนับ "น้ำมัน" ที่เกี่ยวข้องด้วยมูลค่าตัวนับเดียวกัน</span><span class="sxs-lookup"><span data-stu-id="46af5-138">When that counter is updated, a related counter "Oil" is also updated with the same counter values.</span></span> <span data-ttu-id="46af5-139">การตั้งค่าใน **ตัวนับ** รวมการตั้งค่าใน "ชั่วโมง"</span><span class="sxs-lookup"><span data-stu-id="46af5-139">The setup in **Counters** includes the setup on "Hours".</span></span> <span data-ttu-id="46af5-140">นอกจากนี้ ในตัวนับ "น้ำมัน" ประเภทสินทรัพย์ "เครื่องยนต์รถบรรทุก" ควรจะถูกเพิ่มลงในแท็บด่วน **ชนิดของสินทรัพย์** เพื่อให้แน่ใจในความสัมพันธ์ของตัวนับ</span><span class="sxs-lookup"><span data-stu-id="46af5-140">Also, on the "Oil" counter, the asset type "Truck Engine" should be added to the **Asset types** FastTab to ensure the counter relation.</span></span> <span data-ttu-id="46af5-141">ดูภาพหน้าจอด้านล่างสำหรับตัวอย่างของการตั้งค่าในตัวนับของชั่วโมงและน้ำมัน</span><span class="sxs-lookup"><span data-stu-id="46af5-141">See the screenshots below for an example of the setup on the Hours and Oil counters.</span></span>

<span data-ttu-id="46af5-142">เมื่อมีการเพิ่มชนิดสินทรัพย์ลงในชนิดตัวนับใน **ตัวนับ** จะมีการเพิ่มตัวนับลงในชนิดสินทรัพย์บนแท็บด่วน **ตัวนับ** ใน [ชนิดสินทรัพย์](../setup-for-objects/object-types.md) โดยอัตโนมัติ</span><span class="sxs-lookup"><span data-stu-id="46af5-142">When asset types are added to a counter type in **Counters**, that counter is automatically added to the asset types on the **Counters** FastTab in [Asset types](../setup-for-objects/object-types.md).</span></span>

![รูปที่ 1](media/071-setup-for-objects.png)

