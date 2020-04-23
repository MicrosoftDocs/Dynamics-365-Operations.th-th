---
title: กลุ่มวัตถุที่ให้บริการ
description: กลุ่มออบเจ็กต์มีประโยชน์สำหรับการเรียงลำดับและการกรองข้อมูลเกี่ยวกับออบเจ็กต์สำหรับรายงานและสถิติ
author: ShylaThompson
manager: tfehr
ms.date: 05/11/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SMAServiceObjectGroups
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: ShylaThompson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: ca1ca177fe7048e5ff37a8058d00face4a8166f0
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 04/02/2020
ms.locfileid: "3215113"
---
# <a name="service-object-groups"></a><span data-ttu-id="be372-103">กลุ่มวัตถุที่ให้บริการ</span><span class="sxs-lookup"><span data-stu-id="be372-103">Service object groups</span></span> 

[!include [banner](../includes/banner.md)]

<span data-ttu-id="be372-104">กลุ่มออบเจ็กต์มีประโยชน์สำหรับการเรียงลำดับและการกรองข้อมูลเกี่ยวกับออบเจ็กต์สำหรับรายงานและสถิติ</span><span class="sxs-lookup"><span data-stu-id="be372-104">Object groups are useful for sorting and filtering the data about objects for reports and statistics.</span></span> <span data-ttu-id="be372-105">ตัวอย่างเช่น คุณสามารถจัดกลุ่มออบเจ็กต์ ตามที่ตั้งทางภูมิศาสตร์ หรือตามชนิด</span><span class="sxs-lookup"><span data-stu-id="be372-105">For example, you can group objects by geographical location or by type.</span></span>

## <a name="group-by-geographical-location"></a><span data-ttu-id="be372-106">การจัดกลุ่มตามที่ตั้งทางภูมิศาสตร์</span><span class="sxs-lookup"><span data-stu-id="be372-106">Group by geographical location</span></span>

<span data-ttu-id="be372-107">คุณสามารถใช้วิธีการจัดกลุ่มนี้เพื่อแสดงว่าวัตถุที่แตกต่างกันที่บริษัทของคุณให้บริการตั้งอยู่ที่ใด</span><span class="sxs-lookup"><span data-stu-id="be372-107">You can use this grouping method to show where the various different objects that your company services are located.</span></span> <span data-ttu-id="be372-108">การจัดกลุ่มออบเจ็กต์ตามที่ตั้งทางภูมิศาสตร์ยังมีประโยชน์อีกด้วย ตัวอย่างเช่น ถ้าคุณต้องระบุออบเจ็กต์ซึ่งบริษัทของคุณให้บริการอยู่แล้วสำหรับประเทศ/ภูมิภาคเฉพาะ</span><span class="sxs-lookup"><span data-stu-id="be372-108">Grouping objects by geographical location can also be useful if, for example, you must identify the objects that your company already provides services for in a particular country/region.</span></span>

## <a name="example"></a><span data-ttu-id="be372-109">ตัวอย่าง</span><span class="sxs-lookup"><span data-stu-id="be372-109">Example</span></span>

<span data-ttu-id="be372-110">ลูกค้าจากเบลเยียมโทรไปที่ศูนย์บริการ และต้องการสร้างข้อตกลงการให้บริการสำหรับวัตถุ ABC </span><span class="sxs-lookup"><span data-stu-id="be372-110">A customer from Belgium calls your service center and wants to create a service agreement for an object, ABC.</span></span> <span data-ttu-id="be372-111">คุณได้แนบกลุ่มออบเจ็กต์สำหรับที่ตั้งทางภูมิศาสตร์ ซึ่งคือ เบลเยียม กับออบเจ็กต์ทั้งหมดที่ได้รับบริการในเบลเยียม</span><span class="sxs-lookup"><span data-stu-id="be372-111">You have attached an object group for geographical location, Belgium, to all objects that are serviced in Belgium.</span></span> <span data-ttu-id="be372-112">โดยการใช้กลุ่มนี้เป็นตัวกรองข้อมูล คุณจึงสามารถค้นหาได้อย่างรวดเร็วเพื่อดูว่าคุณมีอยู่เรกคอร์ดสำหรับ ABC ในโปรแกรมแล้ว หรือคุณต้องตั้งค่าออบเจ็กต์ใหม่หรือไม่</span><span class="sxs-lookup"><span data-stu-id="be372-112">By using this group as a filter, you can quickly search to see whether you already have a record for ABC in the program, or whether you must set up a new object.</span></span> 

## <a name="group-by-type"></a><span data-ttu-id="be372-113">การจัดกลุ่มตามชนิด</span><span class="sxs-lookup"><span data-stu-id="be372-113">Group by type</span></span>

<span data-ttu-id="be372-114">คุณสามารถใช้วิธีการจัดกลุ่มนี้เพื่อแสดงชนิดของออบเจ็กต์ที่บริษัทของคุณให้บริการ</span><span class="sxs-lookup"><span data-stu-id="be372-114">You can use this grouping method to show the types of objects that your company services.</span></span> <span data-ttu-id="be372-115">การจัดกลุ่มออบเจ็กต์ตามชนิดยังมีประโยชน์ ตัวอย่างเช่น ถ้าคุณต้องการสร้างออบเจ็กต์ใหม่ตามออบเจ็กต์ซึ่งคล้ายกันที่มีอยู่แล้วในโปรแกรม</span><span class="sxs-lookup"><span data-stu-id="be372-115">Grouping objects by type can also be useful if, for example, you want to create a new object based on similar objects that already exist in the program.</span></span>

## <a name="example"></a><span data-ttu-id="be372-116">ตัวอย่าง</span><span class="sxs-lookup"><span data-stu-id="be372-116">Example</span></span>

<span data-ttu-id="be372-117">ลูกค้าโทรมาและต้องการตั้งค่าข้อตกลงการให้บริการสำหรับเครื่องปรับอากาศ HIJ </span><span class="sxs-lookup"><span data-stu-id="be372-117">A customer calls and wants to set up a service agreement for an air conditioning machine, HIJ.</span></span> <span data-ttu-id="be372-118">คุณไม่ได้มีเรกคอร์ดสำหรับเครื่องนี้อยู่แล้ว</span><span class="sxs-lookup"><span data-stu-id="be372-118">You do not already have a record for this machine.</span></span> <span data-ttu-id="be372-119">อย่างไรก็ตาม คุณได้ตั้งค่ากลุ่มออบเจ็กต์ที่ชื่อว่า เครื่องปรับอากาศ และคุณได้แนบกลุ่มนี้กับออบเจ็กต์เครื่องปรับอากาศทั้งหมด</span><span class="sxs-lookup"><span data-stu-id="be372-119">However, you have set up an object group titled Air Conditioners, and you have attached this group to all air conditioning objects.</span></span> <span data-ttu-id="be372-120">ดังนั้น คุณจึงสามารถค้นหาได้อย่างรวดเร็ว และระบุเครื่องปรับอากาศเครื่องอื่นได้ทั้งหมด และใช้ข้อมูลเท็มเพลตจากออบเจ็กต์เหล่านี้เพื่อสร้างรายการข้อตกลงการให้บริการสำหรับ HIJ</span><span class="sxs-lookup"><span data-stu-id="be372-120">Therefore, you can quickly search for and identify all other air conditioning machines and use the template information from these objects to create service agreement lines for HIJ.</span></span> <span data-ttu-id="be372-121">โดยการใช้กลุ่มออบเจ็กต์ในวิธีนี้ คุณสามารถตั้งค่าออบเจ็กต์ใหม่ได้อย่างรวดเร็ว และกำหนดภารกิจการให้บริการที่ต้องดำเนินการกับออบเจ็กต์นั้น </span><span class="sxs-lookup"><span data-stu-id="be372-121">By using object groups in this manner, you can quickly set up new objects and determine the service tasks that must be performed on them.</span></span> 

## <a name="create-service-object-groups"></a><span data-ttu-id="be372-122">การสร้างกลุ่มวัตถุที่ให้บริการ</span><span class="sxs-lookup"><span data-stu-id="be372-122">Create service object groups</span></span>

<span data-ttu-id="be372-123">สร้างกลุ่มที่คุณสามารถกำหนดให้กับวัตถุที่ให้บริการ</span><span class="sxs-lookup"><span data-stu-id="be372-123">Create groups that you can assign service objects to.</span></span> <span data-ttu-id="be372-124">วัตถุที่ให้บริการคือสินค้าคงคลังและผลิตภัณฑ์อื่นๆ ซึ่งจะดำเนินการบริการ </span><span class="sxs-lookup"><span data-stu-id="be372-124">Service objects are inventory items and other products for which services are performed.</span></span> <span data-ttu-id="be372-125">โดยการจัดกลุ่มวัตถุที่ให้บริการ คุณสามารถสร้างรายงานสำหรับวัตถุที่ให้บริการที่เกี่ยวข้องและคล้ายคลึงกัน </span><span class="sxs-lookup"><span data-stu-id="be372-125">By grouping service objects, you can create reports for similar and related service objects.</span></span> <span data-ttu-id="be372-126">ตัวอย่างเช่น กลุ่มวัตถุที่ให้บริการอาจประกอบด้วยสองวัตถุที่ให้บริการ: วัตถุที่ให้บริการหนึ่งรายการเป็นชุด และวัตถุที่ให้บริการที่สองเป็นบริการที่จะติดตั้งชุด</span><span class="sxs-lookup"><span data-stu-id="be372-126">For example, a service object group might consist of two service objects: One service object is a kit, and the second service object is the service to install the kit.</span></span>

<span data-ttu-id="be372-127">การสร้างกลุ่มวัตถุที่ให้บริการ ให้ทำตามขั้นตอนเหล่านี้</span><span class="sxs-lookup"><span data-stu-id="be372-127">To create service object groups, follow these steps:</span></span>

1. <span data-ttu-id="be372-128">คลิก **การจัดการบริการ > ตั้งค่า > วัตถุที่ให้บริการ > กลุ่มวัตถุที่ให้บริการ**</span><span class="sxs-lookup"><span data-stu-id="be372-128">Click **Service management > Setup > Service objects > Service object groups**.</span></span>

2. <span data-ttu-id="be372-129">คลิก **สร้าง** เพื่อสร้างกลุ่มวัตถุที่ให้บริการใหม่</span><span class="sxs-lookup"><span data-stu-id="be372-129">Click **New** to create a new service object group.</span></span>

3. <span data-ttu-id="be372-130">ป้อนชื่อเฉพาะของกลุ่มวัตถุที่ให้บริการ และคำอธิบายหากต้องการ</span><span class="sxs-lookup"><span data-stu-id="be372-130">Enter a unique name for the service object group and, optionally, a description.</span></span>

<span data-ttu-id="be372-131">คุณสามารถกำหนดวัตถุที่ให้บริการให้กับกลุ่มได้โดยใช้แบบฟอร์ม **วัตถุที่ให้บริการ**</span><span class="sxs-lookup"><span data-stu-id="be372-131">You can assign service objects to the group by using the **Service objects** form.</span></span> 

## <a name="see-also"></a><span data-ttu-id="be372-132">ดูเพิ่มเติมที่</span><span class="sxs-lookup"><span data-stu-id="be372-132">See also</span></span>

[<span data-ttu-id="be372-133">การสร้างวัตถุที่ให้บริการ</span><span class="sxs-lookup"><span data-stu-id="be372-133">Create service objects</span></span>](create-service-objects.md)


