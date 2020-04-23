---
title: การสร้างความสัมพันธ์ของวัตถุที่ให้บริการ
description: 'หัวข้อนี้อธิบายวิธีการสร้างความสัมพันธ์ของวัตถุที่ให้บริการสำหรับข้อตกลงการให้บริการและใบสั่งบริการ '
author: ShylaThompson
manager: tfehr
ms.date: 05/01/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SMAServiceOrderTable, SMAAgreementTable
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: ShylaThompson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: ab5de850ef40c26e447b96d8f42ccf83fb490818
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 04/02/2020
ms.locfileid: "3202778"
---
# <a name="create-service-object-relations"></a><span data-ttu-id="392cd-103">การสร้างความสัมพันธ์ของวัตถุที่ให้บริการ</span><span class="sxs-lookup"><span data-stu-id="392cd-103">Create service object relations</span></span> 

[!include [banner](../includes/banner.md)]


<span data-ttu-id="392cd-104">หัวข้อนี้อธิบายวิธีการสร้างความสัมพันธ์ของวัตถุที่ให้บริการสำหรับข้อตกลงการให้บริการและใบสั่งบริการ </span><span class="sxs-lookup"><span data-stu-id="392cd-104">This topic describes how to create service object relations for a service agreement and a service order.</span></span> <span data-ttu-id="392cd-105">เมื่อคุณสร้างตัวให้บริการความสัมพันธ์ของวัตถุ คุณเชื่อมโยงวัตถุที่ให้บริการกับข้อตกลงการให้บริการหรือใบสั่งบริการ </span><span class="sxs-lookup"><span data-stu-id="392cd-105">When you a create service object relation, you associate the service object to a service agreement or service order.</span></span> <span data-ttu-id="392cd-106">เมื่อบริการคำขอของลูกค้าสำหรับสินค้าที่มีวัตถุที่ให้บริการ คุณสามารถเลือกวัตถุที่ให้บริการจากรายการของความสัมพันธ์ของวัตถุที่ให้บริการ</span><span class="sxs-lookup"><span data-stu-id="392cd-106">When a customer requests service for an item that is a service object, you can select the service object from the list of service object relations.</span></span>

## <a name="create-a-service-object-relation-for-a-service-agreement"></a><span data-ttu-id="392cd-107">การสร้างความสัมพันธ์ของบริการออบเจ็กต์สำหรับข้อตกลงการให้บริการ</span><span class="sxs-lookup"><span data-stu-id="392cd-107">Create a service object relation for a service agreement</span></span>

<span data-ttu-id="392cd-108">ใช้ขั้นตอนต่อไปนี้เพื่อสร้างความสัมพันธ์ของบริการออบเจ็กต์สำหรับข้อตกลงการให้บริการ</span><span class="sxs-lookup"><span data-stu-id="392cd-108">Use the following steps to create a service object relation for a service agreement:</span></span>

1.  <span data-ttu-id="392cd-109">คลิก **การจัดการบริการ** \> **ทั่วไป** \> **ข้อตกลงการให้บริการ** \> **ข้อตกลงการให้บริการ**</span><span class="sxs-lookup"><span data-stu-id="392cd-109">Click **Service management** \> **Common** \> **Service agreements** \> **Service agreements**.</span></span>

2.  <span data-ttu-id="392cd-110">ในรายการ **ข้อตกลงการให้บริการ** ให้เลือกข้อตกลงการให้บริการที่มีอยู่ หรือคลิก **สร้าง** เพื่อสร้างข้อตกลงการให้บริการใหม่</span><span class="sxs-lookup"><span data-stu-id="392cd-110">In the **Service agreements** list, select an existing service agreement, or click **New** to create a new service agreement.</span></span>

3.  <span data-ttu-id="392cd-111">ในฟอร์ม **ข้อตกลงการให้บริการ** บน **บานหน้าต่างการดำเนินการ** บนแท็บ **ข้อตกลงการให้บริการ** ในกลุ่ม **ความสัมพันธ์** คลิก **วัตถุที่ให้บริการ**</span><span class="sxs-lookup"><span data-stu-id="392cd-111">In the **Service agreements** form, on the **Action Pane**, on the **Service agreement** tab, in the **Relations** group, click **Service objects**.</span></span>

4.  <span data-ttu-id="392cd-112">ในแบบฟอร์ม **วัตถุที่ให้บริการ** คลิก **สร้าง** แล้วเลือกวัตถุที่ให้บริการสำหรับข้อตกลงการให้บริการนี้</span><span class="sxs-lookup"><span data-stu-id="392cd-112">In the **Service objects** form, click **New**, and then select a service object for this service agreement.</span></span>

5.  <span data-ttu-id="392cd-113">เมื่อต้องการกำหนดสูตรการผลิตเท็มเพลต (BOM) ให้กับข้อตกลงการให้บริการ คลิก **ฟังก์ชัน** แล้วเลือก **แนบ BOM เท็มเพลต**</span><span class="sxs-lookup"><span data-stu-id="392cd-113">To assign a template bill of materials (BOM) to the service agreement, click **Functions**, and then select **Attach template BOM**.</span></span> <span data-ttu-id="392cd-114">ในแบบฟอร์ม **เลือก BOM เท็มเพลต** ในฟิลด์ **BOM เท็มเพลต** เลือกเท็มเพลต</span><span class="sxs-lookup"><span data-stu-id="392cd-114">In the **Select template BOM** form, in the **Template BOM** field, select a template.</span></span> 

## <a name="create-a-service-object-relation-for-a-service-order"></a><span data-ttu-id="392cd-115">การสร้างความสัมพันธ์ของบริการออบเจ็กต์สำหรับใบสั่งบริการ</span><span class="sxs-lookup"><span data-stu-id="392cd-115">Create a service object relation for a service order</span></span>

<span data-ttu-id="392cd-116">ใช้ขั้นตอนต่อไปนี้เพื่อสร้างความสัมพันธ์ของบริการออบเจ็กต์สำหรับใบสั่งบริการ</span><span class="sxs-lookup"><span data-stu-id="392cd-116">Use the following steps to create a service object relation for a service order:</span></span>

1.  <span data-ttu-id="392cd-117">คลิก **การจัดการบริการ** \> **ทั่วไป** \> **ใบสั่งบริการ** \> **ใบสั่งบริการ**</span><span class="sxs-lookup"><span data-stu-id="392cd-117">Click **Service management** \> **Common** \> **Service orders** \> **Service orders**.</span></span>

2.  <span data-ttu-id="392cd-118">ในรายการ **ใบสั่งบริการ** เลือกใบสั่งบริการที่มีอยู่แล้ว หรือสร้างใบสั่งบริการใหม่</span><span class="sxs-lookup"><span data-stu-id="392cd-118">In the **Service orders** list, select an existing service order, or create a new service order.</span></span>

3.  <span data-ttu-id="392cd-119">ในฟอร์ม **ใบสั่งบริการ** บน **บานหน้าต่างการดำเนินการ** บนแท็บ **ใบสั่งบริการ** ในกลุ่ม **ความสัมพันธ์** คลิก **วัตถุที่ให้บริการ**</span><span class="sxs-lookup"><span data-stu-id="392cd-119">In the **Service orders** form, on the **Action Pane**, on the **Service order** tab, in the **Relations** group, click **Service objects**.</span></span>

4.  <span data-ttu-id="392cd-120">ในแบบฟอร์ม **วัตถุที่ให้บริการ** คลิก **สร้าง** แล้วเลือกวัตถุที่ให้บริการสำหรับใบสั่งบริการนี้</span><span class="sxs-lookup"><span data-stu-id="392cd-120">In the **Service objects** form, click **New**, and then select a service object for this service order.</span></span>

5.  <span data-ttu-id="392cd-121">เมื่อต้องการกำหนด BOM เท็มเพลตให้กับข้อตกลงการให้บริการ คลิก **ฟังก์ชัน** แล้วเลือก **แนบ BOM เท็มเพลต**</span><span class="sxs-lookup"><span data-stu-id="392cd-121">To assign a template BOM to the service agreement, click **Functions**, and then select **Attach template BOM**.</span></span> <span data-ttu-id="392cd-122">ในแบบฟอร์ม **เลือก BOM เท็มเพลต** ในฟิลด์ **BOM เท็มเพลต** เลือกเท็มเพลต</span><span class="sxs-lookup"><span data-stu-id="392cd-122">In the **Select template BOM** form, in the **Template BOM** field, select a template.</span></span> 


## <a name="see-also"></a><span data-ttu-id="392cd-123">ดูเพิ่มเติมที่</span><span class="sxs-lookup"><span data-stu-id="392cd-123">See also</span></span>

[<span data-ttu-id="392cd-124">ภาพรวมของวัตถุที่ให้บริการ</span><span class="sxs-lookup"><span data-stu-id="392cd-124">Service objects overview</span></span>](service-objects.md)

[<span data-ttu-id="392cd-125">ความสัมพันธ์ของวัตถุที่ให้บริการ</span><span class="sxs-lookup"><span data-stu-id="392cd-125">Service object relations</span></span>](service-object-relations.md)

[<span data-ttu-id="392cd-126">BOM เท็มเพลต</span><span class="sxs-lookup"><span data-stu-id="392cd-126">Template BOMs</span></span>](template-boms.md)

  


