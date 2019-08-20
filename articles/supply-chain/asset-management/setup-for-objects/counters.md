---
title: หน่วยวัดทางสินทรัพย์
description: หัวข้อจะอธิบายวิธีการสร้างชนิดหน่วยวัดทางสินทรัพย์ในการจัดการสินทรัพย์
author: josaw1
manager: AnnBe
ms.date: 06/26/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CatProcureCatalogEdit, CatProcureCatalogListPage
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 2214
ms.assetid: 2f3e0441-414d-402b-b28b-7ab0d650d658
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: d9c445832a649c4f6a6642036ecab325e8aa2079
ms.sourcegitcommit: 747bcd25ce7c6c20ce9eaa0027e730f74d4fd6aa
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 07/23/2019
ms.locfileid: "1783637"
---
# <a name="asset-measures"></a><span data-ttu-id="206d8-103">หน่วยวัดทางสินทรัพย์</span><span class="sxs-lookup"><span data-stu-id="206d8-103">Asset measures</span></span>

[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]

<span data-ttu-id="206d8-104">หัวข้อจะอธิบายวิธีการสร้างชนิดหน่วยวัดทางสินทรัพย์ในการจัดการสินทรัพย์</span><span class="sxs-lookup"><span data-stu-id="206d8-104">The topic explains how to create asset measure types in Asset Management.</span></span> <span data-ttu-id="206d8-105">ชนิดของหน่วยวัดทางสินทรัพย์จะใช้เพื่อทำการลงทะเบียนการวัดในสินทรัพย์ ตัวอย่างเช่น ซึ่งเกี่ยวข้องกับจำนวนของชั่วโมงการผลิตหรือปริมาณที่ผลิตในสินทรัพย์</span><span class="sxs-lookup"><span data-stu-id="206d8-105">Asset measure types are used to make measurement registrations on assets, for example, regarding number of production hours, or quantity produced on the asset.</span></span> <span data-ttu-id="206d8-106">ชนิดของสินทรัพย์เกี่ยวข้องกับชนิดของหน่วยวัดทางสินทรัพย์</span><span class="sxs-lookup"><span data-stu-id="206d8-106">Asset types are related to the asset measure types.</span></span> <span data-ttu-id="206d8-107">นี่หมายความว่า สามารถใช้หน่วยวัดทางสินทรัพย์ได้ในสินทรัพย์เท่านั้น ถ้ามีการตั้งค่าหน่วยวัดทางสินทรัพย์ในชนิดสินทรัพย์ที่ใช้ในสินทรัพย์</span><span class="sxs-lookup"><span data-stu-id="206d8-107">This means that an asset measure can only be used on an asset if the asset measure is set up on the asset type used on the asset.</span></span>

<span data-ttu-id="206d8-108">ก่อนที่คุณจะสามารถทำการลงทะเบียนการวัดในสินทรัพย์ได้ ก่อนอื่นคุณต้องสร้างชนิดหน่วยวัดทางสินทรัพย์ที่คุณต้องการใช้ใน **ตัวนับ**</span><span class="sxs-lookup"><span data-stu-id="206d8-108">Before you can make measurement registrations on assets, you first create the asset measure types you want to use in **Counters**.</span></span> <span data-ttu-id="206d8-109">ถัดไป คุณสามารถสร้างการลงทะเบียนการวัดในสินทรัพย์ได้ใน **หน่วยวัดทางสินทรัพย์**</span><span class="sxs-lookup"><span data-stu-id="206d8-109">Next, you can create measurement registrations on assets in **Asset measures**.</span></span> 

<span data-ttu-id="206d8-110">สามารถใช้หน่วยวัดทางสินทรัพย์ในแผนการบำรุงรักษาได้</span><span class="sxs-lookup"><span data-stu-id="206d8-110">Asset measures can be used on maintenance plans.</span></span> <span data-ttu-id="206d8-111">รายการแผนการบำรุงรักษาสามารถเป็นชนิด "ตัวนับ" ตัวอย่างเช่น ซึ่งเกี่ยวข้องกับจำนวนของชั่วโมงการผลิตหรือปริมาณที่ผลิต</span><span class="sxs-lookup"><span data-stu-id="206d8-111">A maintenance plan line can be of type "Counter", for example, relating to number of production hours or quantity produced.</span></span> 

<span data-ttu-id="206d8-112">การลงทะเบียนหน่วยวัดทางสินทรัพย์สามารถปรับปรุงได้ด้วยตนเองหรือโดยอัตโนมัติตามชั่วโมงการผลิตหรือปริมาณที่ผลิต</span><span class="sxs-lookup"><span data-stu-id="206d8-112">An asset measurement registration can be updated manually or automatically based on production hours or quantity produced.</span></span> <span data-ttu-id="206d8-113">คุณสามารถตั้งค่าหน่วยวัดทางสินทรัพย์เพื่อใช้วิธีการปรับปรุงหนึ่งในสามวิธีนี้ (ซึ่งเลือกในฟิลด์ **ปรับปรุง** ใน **ตัวนับ**):</span><span class="sxs-lookup"><span data-stu-id="206d8-113">An asset measure can be set up to use one of three update methods (selected in the **Update** field in **Counters**):</span></span>
  
- <span data-ttu-id="206d8-114">ด้วยตนเอง - คุณต้องลงทะเบียนมูลค่าหน่วยวัดทางสินทรัพย์ด้วยตนเอง</span><span class="sxs-lookup"><span data-stu-id="206d8-114">Manual - you must manually register asset measurement values.</span></span>  
- <span data-ttu-id="206d8-115">ชั่วโมงการผลิต - จะปรับปรุงตัวนับโดยอัตโนมัติตามจำนวนของชั่วโมงการผลิต</span><span class="sxs-lookup"><span data-stu-id="206d8-115">Production hours - the counter is automatically updated based on number of production hours.</span></span>  
- <span data-ttu-id="206d8-116">ปริมาณการผลิต - จะปรับปรุงตัวนับโดยอัตโนมัติตามจำนวนของปริมาณที่ผลิต</span><span class="sxs-lookup"><span data-stu-id="206d8-116">Production quantity - the counter is automatically updated based on number of quantity produced.</span></span>  

>[!NOTE]
><span data-ttu-id="206d8-117">ถ้าปริมาณที่ผลิตถูกใช้ สินค้าที่ลงทะเบียนทั้งหมด *ทั้งหมด* จะถูกรวมอยู่ในการลงทะเบียนการวัด ปริมาณที่ดี และปริมาณสินค้าที่บกพร่อง</span><span class="sxs-lookup"><span data-stu-id="206d8-117">If quantity produced is used, *all* registered items are included in the measurement registration, good quantity as well as error quantity.</span></span> <span data-ttu-id="206d8-118">เป็นไปได้เสมอที่จะทำการลงทะเบียนหน่วยวัดทางสินทรัพย์ด้วยตนเอง ถ้าจำเป็น</span><span class="sxs-lookup"><span data-stu-id="206d8-118">It is always possible to make manual asset measurement registrations, if required.</span></span>

## <a name="create-counter-types-for-asset-counter-registrations"></a><span data-ttu-id="206d8-119">สร้างชนิดของตัวนับสำหรับการลงทะเบียนตัวนับสินทรัพย์</span><span class="sxs-lookup"><span data-stu-id="206d8-119">Create counter types for asset counter registrations</span></span>

1. <span data-ttu-id="206d8-120">เลือก **การจัดการสินทรัพย์** > **การตั้งค่า** > **ชนิดสินทรัพย์** > **ตัวนับ**</span><span class="sxs-lookup"><span data-stu-id="206d8-120">Select **Asset management** > **Setup** > **Asset types** > **Counters**.</span></span>
2. <span data-ttu-id="206d8-121">เลือก **สร้าง** เพื่อสร้างชนิดของหน่วยวัดทางสินทรัพย์ใหม่</span><span class="sxs-lookup"><span data-stu-id="206d8-121">Select **New** to create a new asset measure type.</span></span>
3. <span data-ttu-id="206d8-122">แทรกรหัสลงในฟิลด์ **ตัวนับ** และชื่อตัวนับในฟิลด์ **ชื่อ**</span><span class="sxs-lookup"><span data-stu-id="206d8-122">Insert an ID in the **Counter** field, and a counter name in the **Name** field.</span></span>
4. <span data-ttu-id="206d8-123">บน FastTab **ทั่วไป** ให้เลือกหน่วยการวัดในฟิลด์ **หน่วย**</span><span class="sxs-lookup"><span data-stu-id="206d8-123">On the **General** FastTab, select a measurement unit in the **Unit** field.</span></span>
5. <span data-ttu-id="206d8-124">ในฟิลด์ **ปรับปรุง** ให้เลือกวิธีการปรับปรุงที่จะใช้สำหรับหน่วยวัดทางสินทรัพย์</span><span class="sxs-lookup"><span data-stu-id="206d8-124">In the **Update** field, select the update method to be used for the asset measure.</span></span>
6. <span data-ttu-id="206d8-125">เลือก "ใช่" บนปุ่มสลับ **สืบทอดค่าตัวนับ** ถ้าสินทรัพย์รองในโครงสร้างสินทรัพย์ควรสืบทอดการลงทะเบียนหน่วยวัดทางสินทรัพย์ที่ทำบนสินทรัพย์หลักโดยอัตโนมัติ</span><span class="sxs-lookup"><span data-stu-id="206d8-125">Select "Yes" on the **Inherit counter values** toggle button if child assets in an asset structure should automatically inherit asset measure registrations made on the parent asset.</span></span>
7. <span data-ttu-id="206d8-126">ในฟิลด์ **ผลรวมทั้งหมด** ให้เลือกวิธีการรวมที่จะใช้สำหรับหน่วยวัดทางสินทรัพย์โดยใช้ชนิดหน่วยวัดทางสินทรัพย์นี้</span><span class="sxs-lookup"><span data-stu-id="206d8-126">In the **Total aggregate** field, select the summation method to be used for an asset measure using this asset measure type.</span></span> <span data-ttu-id="206d8-127">"รวม" คือตัวเลือกมาตรฐานที่ใช้ในการเพิ่มค่าที่ลงทะเบียนไปยังมูลค่ารวมอย่างต่อเนื่อง</span><span class="sxs-lookup"><span data-stu-id="206d8-127">"Sum" is the standard selection used to continuously add registered values to the total value.</span></span> <span data-ttu-id="206d8-128">"ค่าเฉลี่ย" สามารถใช้ได้ ถ้ามีการตั้งค่าหน่วยวัดทางสินทรัพย์เพื่อตรวจสอบขีดจำกัด ตัวอย่างเช่น ซึ่งเกี่ยวกับอุณหภูมิ การสั่นสะเทือน หรือการสึกหรอและการฉีกขาดของสินทรัพย์</span><span class="sxs-lookup"><span data-stu-id="206d8-128">"Average" can be used if an asset measure is set up to monitor a threshold, for example, regarding temperature, vibrations, or wear and tear on an asset.</span></span> 
8. <span data-ttu-id="206d8-129">ในฟิลด์ **ความเบี่ยงเบนสูงกว่า** ให้แทรกระดับบนเป็นเปอร์เซ็นต์สำหรับการตรวจสอบความถูกต้อง ถ้าการลงทะเบียนหน่วยวัดทางสินทรัพย์ด้วยตนเองอยู่ภายในช่วงที่คาดไว้</span><span class="sxs-lookup"><span data-stu-id="206d8-129">In the **Deviation over** field, insert the upper level in percent for validating if manual asset measure registrations are within an expected range.</span></span> <span data-ttu-id="206d8-130">การตรวจสอบความถูกต้องจะขึ้นอยู่กับการเพิ่มขึ้นเชิงเส้นในการลงทะเบียนหน่วยวัดทางสินทรัพย์ที่มีอยู่</span><span class="sxs-lookup"><span data-stu-id="206d8-130">The validation is based on a linear increase in existing asset measure registrations.</span></span>
9. <span data-ttu-id="206d8-131">ในฟิลด์ **ความเบี่ยงเบนต่ำกว่า** ให้แทรกระดับล่างเป็นเปอร์เซ็นต์สำหรับการตรวจสอบความถูกต้อง ถ้าการลงทะเบียนหน่วยวัดทางสินทรัพย์ด้วยตนเองอยู่ภายในช่วงที่คาดไว้</span><span class="sxs-lookup"><span data-stu-id="206d8-131">In the **Deviation under** field, insert the lower level in percent for validating if manual asset measure registrations are within an expected range.</span></span> <span data-ttu-id="206d8-132">การตรวจสอบความถูกต้องจะขึ้นอยู่กับการลดลงเชิงเส้นในการลงทะเบียนหน่วยวัดทางสินทรัพย์ที่มีอยู่</span><span class="sxs-lookup"><span data-stu-id="206d8-132">The validation is based on a linear decrease in existing asset measure registrations.</span></span>
10. <span data-ttu-id="206d8-133">ในฟิลด์ **ชนิด** ให้เลือกชนิดของข้อความ (ข้อมูล คำเตือน ข้อผิดพลาด) ที่จะถูกแสดง ถ้าส่วนเบี่ยงเบนนอกช่วงที่กำหนดเกิด เมื่อคุณทำการลงทะเบียนหน่วยวัดทางสินทรัพย์ด้วยตนเอง</span><span class="sxs-lookup"><span data-stu-id="206d8-133">In the **Type** field, select the type of message (information, warning, error) to be shown if deviations outside the defined range occur when you make manual asset measure registrations.</span></span>
11. <span data-ttu-id="206d8-134">บน FastTab **ชนิดสินทรัพย์** ให้เพิ่มชนิดสินทรัพย์ที่ควรสามารถใช้หน่วยวัดทางสินทรัพย์ได้</span><span class="sxs-lookup"><span data-stu-id="206d8-134">On the **Asset types** FastTab, add the asset types that should be able to use the asset measure.</span></span>
12. <span data-ttu-id="206d8-135">บน FastTab **หน่วยวัดทางสินทรัพย์ที่เกี่ยวข้อง** ให้เพิ่มหน่วยวัดทางสินทรัพย์ที่คุณต้องการได้รับการปรับปรุงโดยอัตโนมัติ เมื่อมีการปรับปรุงหน่วยวัดทางสินทรัพย์นี้</span><span class="sxs-lookup"><span data-stu-id="206d8-135">On the **Related asset measures** FastTab, add the asset measures that you want to be automatically updated when this asset measure is updated.</span></span>


>[!NOTE]
><span data-ttu-id="206d8-136">หน่วยวัดทางสินทรัพย์ที่เกี่ยวข้องจะถูกปรับปรุงโดยอัตโนมัติ เฉพาะเมื่อหน่วยวัดทางสินทรัพย์ที่เกี่ยวข้องมีชนิดสินทรัพย์ซึ่งเกี่ยวข้องในการตั้งค่าหน่วยวัดทางสินทรัพย์</span><span class="sxs-lookup"><span data-stu-id="206d8-136">A related asset measure is automatically updated only if the related asset measure has the asset type, to which it is related, in the asset measure setup.</span></span> <span data-ttu-id="206d8-137">ตัวอย่างเช่น: คุณตั้งค่าหน่วยวัดทางสินทรัพย์สำหรับ "ชั่วโมงการผลิต" และเพิ่มประเภทสินทรัพย์ "เครื่องยนต์รถบรรทุก"</span><span class="sxs-lookup"><span data-stu-id="206d8-137">For example: You set up an asset measure for "Production hours" and add the asset type "Truck Engine".</span></span> <span data-ttu-id="206d8-138">เมื่อมีการปรับปรุงหน่วยวัดทางสินทรัพย์ จะมีการปรับปรุงตัวนับ "น้ำมัน" ที่เกี่ยวข้องด้วยมูลค่าหน่วยวัดทางสินทรัพย์เดียวกัน</span><span class="sxs-lookup"><span data-stu-id="206d8-138">When that asset measure is updated, a related counter "Oil" is also updated with the same asset measure values.</span></span> <span data-ttu-id="206d8-139">การตั้งค่าใน **ตัวนับ** รวมการตั้งค่าใน "ชั่วโมง"</span><span class="sxs-lookup"><span data-stu-id="206d8-139">The setup in **Counters** includes the setup on "Hours".</span></span> <span data-ttu-id="206d8-140">นอกจากนี้ ในหน่วยวัดทางสินทรัพย์ "น้ำมัน" ประเภทสินทรัพย์ "เครื่องยนต์รถบรรทุก" ควรจะถูกเพิ่มลงใน FastTab **ชนิดของสินทรัพย์** เพื่อให้แน่ใจในความสัมพันธ์ของหน่วยวัดทางสินทรัพย์</span><span class="sxs-lookup"><span data-stu-id="206d8-140">Also, on the "Oil" asset measure, the asset type "Truck Engine" should be added to the **Asset types** FastTab to ensure the asset measure relation.</span></span> <span data-ttu-id="206d8-141">ดูภาพหน้าจอด้านล่างสำหรับตัวอย่างของการตั้งค่าในหน่วยวัดทางสินทรัพย์ของชั่วโมงและน้ำมัน</span><span class="sxs-lookup"><span data-stu-id="206d8-141">See the screenshots below for an example of the setup on the Hours and Oil asset measures.</span></span>

<span data-ttu-id="206d8-142">เมื่อมีการเพิ่มชนิดสินทรัพย์ลงในชนิดหน่วยวัดทางสินทรัพย์ใน **ตัวนับ** จะมีการเพิ่มหน่วยวัดทางสินทรัพย์ลงในชนิดสินทรัพย์บน FastTab **ตัวนับ** ใน [ชนิดสินทรัพย์](../setup-for-objects/object-types.md) โดยอัตโนมัติ</span><span class="sxs-lookup"><span data-stu-id="206d8-142">When asset types are added to an asset measure type in **Counters**, that asset measure is automatically added to the asset types on the **Counters** FastTab in [Asset types](../setup-for-objects/object-types.md).</span></span>

![รูปที่ 1](media/071-setup-for-objects.png)


