---
title: "ความสัมพันธ์ของวัตถุที่ให้บริการ"
description: "คุณสามารถคความสัมพันธ์วัตถุที่ให้บริการระหว่างวัตถุที่ให้บริการกับข้อตกลงการให้บริการหรือใบสั่งบริการ "
author: YuyuScheller
manager: AnnBe
ms.date: 02/21/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: SMAServiceObjectRelation
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 
ms.assetid: 
ms.search.region: Global
ms.author: YuyuScheller
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: 90c16653dee0614beaad8e4693c012b67a54b297
ms.contentlocale: th-th
ms.lasthandoff: 05/08/2018

---

# <a name="service-object-relations"></a><span data-ttu-id="7cfd9-103">ความสัมพันธ์ของวัตถุที่ให้บริการ</span><span class="sxs-lookup"><span data-stu-id="7cfd9-103">Service object relations</span></span> 

[!include [banner](../includes/banner.md)]

<span data-ttu-id="7cfd9-104">คุณสามารถคความสัมพันธ์วัตถุที่ให้บริการระหว่างวัตถุที่ให้บริการกับข้อตกลงการให้บริการหรือใบสั่งบริการ </span><span class="sxs-lookup"><span data-stu-id="7cfd9-104">You can create service object relations between a service object and a service agreement or service order.</span></span> <span data-ttu-id="7cfd9-105">เมื่อคุณสร้างความสัมพันธ์ คุณจะแนบวัตถุที่ให้บริการกับข้อตกลงการให้บริการหรือใบสั่งบริการ</span><span class="sxs-lookup"><span data-stu-id="7cfd9-105">When you create a relation, you attach the service object to the service agreement or service order.</span></span>

<span data-ttu-id="7cfd9-106">หลังจากที่สร้างความสัมพันธ์ขึ้น คุณสามารถแนบออบเจ็กต์กับรายการใดๆ ในข้อตกลงการให้บริการหรือใบสั่งบริการ</span><span class="sxs-lookup"><span data-stu-id="7cfd9-106">After the relation is created, you can attach the service object to any lines on the service agreement or service order.</span></span>

## <a name="template-boms"></a><span data-ttu-id="7cfd9-107">BOM เท็มเพลต</span><span class="sxs-lookup"><span data-stu-id="7cfd9-107">Template BOMs</span></span>

<span data-ttu-id="7cfd9-108">คุณสามารถกำหนด BOM เท็มเพลตสำหรับความสัมพันธ์ของวัตถุได้ด้วย  BOM เท็มเพลตเป็นรายการวัสดุและส่วนประกอบของวัตถุที่คุณให้บริการ</span><span class="sxs-lookup"><span data-stu-id="7cfd9-108">You can also specify a template BOM for the object relation.</span></span> <span data-ttu-id="7cfd9-109">หากคุณเปลี่ยนส่วนประกอบของวัตถุที่ให้บริการระหว่างการตรวจเยี่ยมให้บริการ</span><span class="sxs-lookup"><span data-stu-id="7cfd9-109">The template BOM is a bill of materials for the object on which you perform service.</span></span> <span data-ttu-id="7cfd9-110">ถ้าคุณแทนที่ส่วนประกอบของออบเจ็กต์บริการในระหว่างการให้บริการ คุณสามารถลงทะเบียนการเปลี่ยนแปลงนี้ใน BOM การบริการโดยใช้แบบฟอร์มออบเจ็กต์บริการได้</span><span class="sxs-lookup"><span data-stu-id="7cfd9-110">If you replace a component part of the service object during a service visit, you can register this change in the service BOM by using the Service objects form.</span></span>

## <a name="example"></a><span data-ttu-id="7cfd9-111">ตัวอย่าง</span><span class="sxs-lookup"><span data-stu-id="7cfd9-111">Example</span></span>

<span data-ttu-id="7cfd9-112">คุณสร้างข้อตกลงการให้บริการสำหรับการให้บริการลิฟต์สองตัวที่ไซต์ลูกค้า</span><span class="sxs-lookup"><span data-stu-id="7cfd9-112">You create a service agreement for servicing two elevators at a customer site.</span></span>
<span data-ttu-id="7cfd9-113">ข้อตกลงการให้บริการมีตัวระบุเป็น ID SAL-001</span><span class="sxs-lookup"><span data-stu-id="7cfd9-113">The service agreement has the identifier ID SAL-001.</span></span>

<span data-ttu-id="7cfd9-114">ลิฟท์ถูกตั้งค่าในแบบฟอร์มออบเจ็กต์บริการเป็นออบเจ็กต์ EL-S/1000 และ EL-L/1000</span><span class="sxs-lookup"><span data-stu-id="7cfd9-114">The elevators are set up in the Service objects form as objects, EL-S/1000 and EL-L/1000.</span></span>

<span data-ttu-id="7cfd9-115">คุณแนบออบเจ็กต์ที่ให้บริการ EL-S/1000 และ EL-L/1000 กับข้อตกลงการให้บริการ</span><span class="sxs-lookup"><span data-stu-id="7cfd9-115">You attach the service objects, EL-S/1000 and EL-L/1000, to the service agreement.</span></span>

<span data-ttu-id="7cfd9-116">คุณต้องการลงทะเบียนการเปลี่ยนแปลงใน BOM ของวัตถุที่ให้บริการเมื่อคุณเปลี่ยนส่วนประกอบของวัตถุ คุณจึงต้องแนบ BOM การบริการกับความสัมพันธ์วัตถุที่ให้บริการ ดังที่อธิบายไว้ในตารางดังนี้</span><span class="sxs-lookup"><span data-stu-id="7cfd9-116">You want to register changes in the BOM for the service object as you replace component parts of the object, so you attach a service BOM to the service object relation, as described in the following table.</span></span>

| <span data-ttu-id="7cfd9-117">วัตถุที่ให้บริการ</span><span class="sxs-lookup"><span data-stu-id="7cfd9-117">Service object</span></span> | <span data-ttu-id="7cfd9-118">ความสัมพันธ์ – ข้อตกลงการให้บริการ</span><span class="sxs-lookup"><span data-stu-id="7cfd9-118">Relation – Service agreement</span></span> | <span data-ttu-id="7cfd9-119">BOM การบริการ</span><span class="sxs-lookup"><span data-stu-id="7cfd9-119">Service BOM</span></span>   |
|----------------|------------------------------|---------------|
| <span data-ttu-id="7cfd9-120">EL-S/1000</span><span class="sxs-lookup"><span data-stu-id="7cfd9-120">EL-S/1000</span></span>      | <span data-ttu-id="7cfd9-121">ID SAL-001</span><span class="sxs-lookup"><span data-stu-id="7cfd9-121">ID SAL-001</span></span>                   | <span data-ttu-id="7cfd9-122">BOM-EL-S/1000</span><span class="sxs-lookup"><span data-stu-id="7cfd9-122">BOM-EL-S/1000</span></span> |
| <span data-ttu-id="7cfd9-123">EL-L/1000</span><span class="sxs-lookup"><span data-stu-id="7cfd9-123">EL-L/1000</span></span>      | <span data-ttu-id="7cfd9-124">ID SAL-001</span><span class="sxs-lookup"><span data-stu-id="7cfd9-124">ID SAL-001</span></span>                   | <span data-ttu-id="7cfd9-125">BOM-EL-L/1000</span><span class="sxs-lookup"><span data-stu-id="7cfd9-125">BOM-EL-L/1000</span></span> |

<span data-ttu-id="7cfd9-126">เนื่องจากมีความสัมพันธ์ของออบเจ็กต์ที่ให้บริการสำหรับข้อตกลง ตอนนี้ คุณจึงสามารถสร้างรายการข้อตกลงการให้บริการได้ด้วยออบเจ็กต์เหล่านี้ ตามที่แสดงไว้ในตารางต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="7cfd9-126">Because there are service object relations for the agreement, you can now create service agreement lines with these objects, as shown in the following table.</span></span>

| <span data-ttu-id="7cfd9-127">ชนิดธุรกรรม</span><span class="sxs-lookup"><span data-stu-id="7cfd9-127">Transaction type</span></span> | <span data-ttu-id="7cfd9-128">ประเภท</span><span class="sxs-lookup"><span data-stu-id="7cfd9-128">Category</span></span>           | <span data-ttu-id="7cfd9-129">วัตถุที่ให้บริการ</span><span class="sxs-lookup"><span data-stu-id="7cfd9-129">Service object</span></span> |
|------------------|--------------------|----------------|
| <span data-ttu-id="7cfd9-130">ชั่วโมง</span><span class="sxs-lookup"><span data-stu-id="7cfd9-130">Hour</span></span>             | <span data-ttu-id="7cfd9-131">การตรวจสอบ</span><span class="sxs-lookup"><span data-stu-id="7cfd9-131">Inspection</span></span>         | <span data-ttu-id="7cfd9-132">EL-S/1000</span><span class="sxs-lookup"><span data-stu-id="7cfd9-132">EL-S/1000</span></span>      |
| <span data-ttu-id="7cfd9-133">ชั่วโมง</span><span class="sxs-lookup"><span data-stu-id="7cfd9-133">Hour</span></span>             | <span data-ttu-id="7cfd9-134">การทำความสะอาดกระปุกเกียร์</span><span class="sxs-lookup"><span data-stu-id="7cfd9-134">Gear box cleaning</span></span>  | <span data-ttu-id="7cfd9-135">EL-S/1000</span><span class="sxs-lookup"><span data-stu-id="7cfd9-135">EL-S/1000</span></span>      |
| <span data-ttu-id="7cfd9-136">สินค้า</span><span class="sxs-lookup"><span data-stu-id="7cfd9-136">Item</span></span>             | <span data-ttu-id="7cfd9-137">การทำความสะอาดวัสดุ</span><span class="sxs-lookup"><span data-stu-id="7cfd9-137">Cleaning materials</span></span> | <span data-ttu-id="7cfd9-138">EL-S/1000</span><span class="sxs-lookup"><span data-stu-id="7cfd9-138">EL-S/1000</span></span>      |
| <span data-ttu-id="7cfd9-139">ชั่วโมง</span><span class="sxs-lookup"><span data-stu-id="7cfd9-139">Hour</span></span>             | <span data-ttu-id="7cfd9-140">การตรวจสอบ</span><span class="sxs-lookup"><span data-stu-id="7cfd9-140">Inspection</span></span>         | <span data-ttu-id="7cfd9-141">EL-L/1000</span><span class="sxs-lookup"><span data-stu-id="7cfd9-141">EL-L/1000</span></span>      |
| <span data-ttu-id="7cfd9-142">ชั่วโมง</span><span class="sxs-lookup"><span data-stu-id="7cfd9-142">Hour</span></span>             | <span data-ttu-id="7cfd9-143">การทำความสะอาดกระปุกเกียร์</span><span class="sxs-lookup"><span data-stu-id="7cfd9-143">Gearbox cleaning</span></span>   | <span data-ttu-id="7cfd9-144">EL-L/1000</span><span class="sxs-lookup"><span data-stu-id="7cfd9-144">EL-L/1000</span></span>      |
| <span data-ttu-id="7cfd9-145">สินค้า</span><span class="sxs-lookup"><span data-stu-id="7cfd9-145">Item</span></span>             | <span data-ttu-id="7cfd9-146">การทำความสะอาดวัสดุ</span><span class="sxs-lookup"><span data-stu-id="7cfd9-146">Cleaning materials</span></span> | <span data-ttu-id="7cfd9-147">EL-L/1000</span><span class="sxs-lookup"><span data-stu-id="7cfd9-147">EL-L/1000</span></span>      |

<span data-ttu-id="7cfd9-148">ในการตรวจเยี่ยมให้บริการ คุณต้องเปลี่ยนกระปุกเกียร์สำหรับลิฟต์ EL-S/1000</span><span class="sxs-lookup"><span data-stu-id="7cfd9-148">On a service visit, you have to replace the gearbox for elevator EL-S/1000.</span></span> <span data-ttu-id="7cfd9-149">ในการเปลี่ยนส่วนประกอบของออบเจ็กต์ คุณสามารถเข้าใช้งานผู้ออกแบบ BOM ได้โดยใช้ความสัมพันธ์ของออบเจ็กต์ที่ให้บริการซึ่งคุณตั้งค่าไว้สำหรับข้อตกลงการให้บริการปัจจุบัน</span><span class="sxs-lookup"><span data-stu-id="7cfd9-149">To replace a component part of the object, you can access the BOM Designer by using the service object relation that you set up for the current service agreement.</span></span>

<span data-ttu-id="7cfd9-150">การเข้าใช้งานผู้ออกแบบ BOM โดยใช้ความสัมพันธ์วัตถุที่ให้บริการ</span><span class="sxs-lookup"><span data-stu-id="7cfd9-150">Access the BOM Designer by using a service object relation</span></span>

1. <span data-ttu-id="7cfd9-151">ข้อตกลงการให้บริการ</span><span class="sxs-lookup"><span data-stu-id="7cfd9-151">Service agreements</span></span>
2. <span data-ttu-id="7cfd9-152">ดับเบิลคลิกที่ข้อตกลงการให้บริการ หรือคลิกข้อตกลงการให้บริการ เพื่อสร้างข้อตกลงการให้บริการ</span><span class="sxs-lookup"><span data-stu-id="7cfd9-152">Double-click a service agreement, or click Service agreement to create a service agreement.</span></span>
3. <span data-ttu-id="7cfd9-153">คลิกแท็บ การตั้งค่า</span><span class="sxs-lookup"><span data-stu-id="7cfd9-153">Click the Setup tab.</span></span>
4. <span data-ttu-id="7cfd9-154">คลิกออบเจ็กต์ที่ให้บริการเพื่อแนบ BOM เท็มเพลตกับข้อตกลงการให้บริการ</span><span class="sxs-lookup"><span data-stu-id="7cfd9-154">Click Service objects to attach a template BOM to the service agreement.</span></span>
5. <span data-ttu-id="7cfd9-155">ในแบบฟอร์มวัตถุที่ให้บริการ คลิกโปรแกรมออกแบบเพื่อเปิดแบบฟอร์มโปรแกรมออกแบบเพื่อแก้ไข BOM เท็มเพลต</span><span class="sxs-lookup"><span data-stu-id="7cfd9-155">In the Service objects form, click Designer to open the Designer form to modify the template BOM.</span></span>

## <a name="automatically-created-service-orders"></a><span data-ttu-id="7cfd9-156">ใบสั่งบริการที่สร้างโดยอัตโนมัติ</span><span class="sxs-lookup"><span data-stu-id="7cfd9-156">Automatically created service orders</span></span>

<span data-ttu-id="7cfd9-157">ถ้าคุณสร้างใบสั่งบริการสำหรับข้อตกลงการให้บริการโดยอัตโนมัติ ความสัมพันธ์ของออบเจ็กต์ที่ให้บริการในข้อตกลงจะถูกสร้างในใบสั่งบริการด้วย</span><span class="sxs-lookup"><span data-stu-id="7cfd9-157">If you automatically create service orders for a service agreement, the service object relations in the agreement are also created in the service orders.</span></span>


