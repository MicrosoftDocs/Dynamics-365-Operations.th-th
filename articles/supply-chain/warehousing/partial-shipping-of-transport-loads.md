---
title: การจัดส่งบางส่วนของการบรรทุกเพื่อขนส่ง
description: หัวข้อนี้อธิบายวิธีการที่คุณสามารถจัดส่งโหลดได้บางส่วน และเลื่อนการวางแผนกำลังการผลิตสำหรับโหลด
author: Mirzaab
manager: tfehr
ms.date: 03/15/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSTransportLoad
audience: Application User
ms.reviewer: kamaybac
ms.custom: 1705903
ms.assetid: 427e01b3-4968-4cff-9b85-1717530f72e4
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 8.0.0
ms.openlocfilehash: f12f1c08d4d04c284f0f927f99747e763696e43a
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 02/15/2021
ms.locfileid: "5234668"
---
# <a name="partial-shipment-of-a-transport-load"></a><span data-ttu-id="0d4d9-103">การจัดส่งบางส่วนของการบรรทุกเพื่อขนส่ง</span><span class="sxs-lookup"><span data-stu-id="0d4d9-103">Partial shipment of a transport load</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="0d4d9-104">ด้วยการตั้งค่าการจัดส่งบางส่วนของโหลด คุณสามารถจัดการกับโหลดที่ซึ่งไม่สามารถกำหนดกำลังการผลิตได้ จนกว่าจะมีการเพิ่มรายการการขายไปยังโหลด</span><span class="sxs-lookup"><span data-stu-id="0d4d9-104">By setting up partial shipment of loads, you can handle loads where the capacity can't be determined until all the sales lines have been added to a load.</span></span> <span data-ttu-id="0d4d9-105">จากนั้น กระบวนการสามารถได้รับการดำเนินการขั้นสุดท้าย เมื่อทราบจำนวนแท่นวางสินค้าที่แน่นอน</span><span class="sxs-lookup"><span data-stu-id="0d4d9-105">The process can then be finalized when the exact pallet count is known.</span></span> <span data-ttu-id="0d4d9-106">ดังนั้น คุณไม่ต้องตัดสินใจว่า แท่นวางสินค้าใดที่จะถูกกำหนดให้กับการขนส่งใด จนกว่าถึงช่วงเวลาที่การขนส่งกำลังโหลดสินค้าคงคลังที่แบ่งระยะตามจริง</span><span class="sxs-lookup"><span data-stu-id="0d4d9-106">Therefore, you don't have to decide which pallets will be assigned to which transport until the moment when a transport is being physically loaded out of the staged inventory.</span></span>

<span data-ttu-id="0d4d9-107">คุณลักษณะนี้ให้ทางเลือกในการบังคับโครงสร้างที่แข็งมากขึ้น ที่ซึ่งคุณต้องกำหนดว่าแท่นวางสินค้าใดที่จะถูกกำหนดให้กับการขนส่งใด ก่อนที่จะสร้างงานการเบิกสินค้าหรืองานการโหลด</span><span class="sxs-lookup"><span data-stu-id="0d4d9-107">This feature offers an alternative to the enforcement of a more rigid structure, where you must determine which pallets will be assigned to which transport before picking work or loading work can be created.</span></span> <span data-ttu-id="0d4d9-108">ผู้ใช้สามารถตั้งค่าคอนฟิกโหลดแต่ละรายการแทนได้ สำหรับการยืนยันการจัดส่งบางส่วน</span><span class="sxs-lookup"><span data-stu-id="0d4d9-108">Instead, users can configure individual loads for a partial shipment confirmation.</span></span> <span data-ttu-id="0d4d9-109">จากนั้น กระบวนการโหลดของการขนส่งสำหรับโหลดเหล่านั้นอาจเกิดขึ้นได้</span><span class="sxs-lookup"><span data-stu-id="0d4d9-109">The transport loading processes for those loads can then occur.</span></span> <span data-ttu-id="0d4d9-110">ดังนั้น แผนกการวางแผนการขนส่งสามารถวางแผนโหลดได้ โดยต้องไม่พิจารณาถึงกำลังการผลิตของการขนส่งแต่ละรายการ</span><span class="sxs-lookup"><span data-stu-id="0d4d9-110">Therefore, the transportation planning department can plan loads without having to consider the capacity of individual transports.</span></span>

<span data-ttu-id="0d4d9-111">ในขณะที่กำลังโหลด ผู้ปฏิบัติงานสามารถกำหนดโหลดการขนส่งใหม่ที่มีการโหลดแท่นวางสินค้า</span><span class="sxs-lookup"><span data-stu-id="0d4d9-111">At the time of loading, workers can define a new transport load that a pallet can be loaded to.</span></span> <span data-ttu-id="0d4d9-112">อีกทางหนึ่งคือ สามารถระบุโหลดการขนส่งที่มีอยู่ได้</span><span class="sxs-lookup"><span data-stu-id="0d4d9-112">Alternatively, they can identify an existing transport load.</span></span> <span data-ttu-id="0d4d9-113">ข้อมูลนี้สามารถบันทึกได้ผ่านอุปกรณ์เคลื่อนที่</span><span class="sxs-lookup"><span data-stu-id="0d4d9-113">This data can be recorded via a mobile device.</span></span> <span data-ttu-id="0d4d9-114">ดังนั้น ผู้ปฏิบัติงานคลังสินค้าหลายรายสามารถโหลดสินค้าคงคลังจากโหลดเดียวกัน หรือโหลดที่แตกต่างกันไปยังรถบรรทุกเดียวกันได้</span><span class="sxs-lookup"><span data-stu-id="0d4d9-114">Therefore, several warehouse workers can load inventory from the same loads or different loads onto the same truck.</span></span> <span data-ttu-id="0d4d9-115">จากนั้น สามารถจัดส่งโหลดทั้งหมดหรือบางส่วนได้</span><span class="sxs-lookup"><span data-stu-id="0d4d9-115">The loads can then be fully or partially shipped.</span></span>

> [!NOTE] 
> <span data-ttu-id="0d4d9-116">เพื่อที่จะโหลดสินค้าคงคลังจากโหลดไปยังโหลดการขนส่งเฉพาะ และจัดส่งสินค้าบางส่วน งานต้องถูกสร้างขึ้น โดยใช้คลาสการโหลดในเท็มเพลตงาน</span><span class="sxs-lookup"><span data-stu-id="0d4d9-116">In order to load inventory from a load to a specific transport load and partially ship the load, work must be generated by using a loading class in a work template.</span></span> <span data-ttu-id="0d4d9-117">งานของการเบิกสินค้าแบบธรรมดาของชนิด **การเบิกสินค้า** ไม่สามารถโหลดไปยังโหลดการขนส่งได้ เช่น รถบรรทุก</span><span class="sxs-lookup"><span data-stu-id="0d4d9-117">Ordinary picking work of the **Picking** type can't be loaded to a transport load such as a truck.</span></span>

## <a name="set-up-transport-loads-for-partial-shipment"></a><span data-ttu-id="0d4d9-118">ตั้งค่าโหลดการขนส่งสำหรับการจัดส่งเป็นบางส่วน</span><span class="sxs-lookup"><span data-stu-id="0d4d9-118">Set up transport loads for partial shipment</span></span>

<span data-ttu-id="0d4d9-119">การตั้งค่าสำหรับการจัดส่งบางส่วนในโหลด ประกอบด้วยกระบวนงานสองรายการต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="0d4d9-119">The setup for partial shipment of loads consists of the following two procedures.</span></span>

### <a name="set-the-loading-strategy"></a><span data-ttu-id="0d4d9-120">ตั้งค่ากลยุทธ์การโหลด</span><span class="sxs-lookup"><span data-stu-id="0d4d9-120">Set the loading strategy</span></span>

<span data-ttu-id="0d4d9-121">คุณต้องเปิดใช้งานการโหลดบางส่วน โดยการตั้งค่ากลยุทธ์การโหลด</span><span class="sxs-lookup"><span data-stu-id="0d4d9-121">You must enable partial loading by setting the loading strategy.</span></span> <span data-ttu-id="0d4d9-122">คุณสามารถตั้งค่ากลยุทธ์การโหลดได้ หลังจากที่คุณสร้างโหลด</span><span class="sxs-lookup"><span data-stu-id="0d4d9-122">You can set the loading strategy after you've created a load.</span></span>

1. <span data-ttu-id="0d4d9-123">เลือก **การบริหารคลังสินค้า** \> **โหลด** \> **โหลดทั้งหมด**</span><span class="sxs-lookup"><span data-stu-id="0d4d9-123">Select **Warehouse management** \> **Loads** \> **All loads**.</span></span>
2. <span data-ttu-id="0d4d9-124">เลือกโหลด แล้วจากนั้นคลิก **ส่วนหัว**</span><span class="sxs-lookup"><span data-stu-id="0d4d9-124">Select a load, and then click **Header**.</span></span>
3. <span data-ttu-id="0d4d9-125">ในฟิลด์ **กลยุทธ์การโหลด** เลือก **การจัดส่งโหลดบางส่วนที่ได้รับอนุญาต**</span><span class="sxs-lookup"><span data-stu-id="0d4d9-125">In the **Loading strategy** field, select **Partial load shipping allowed**.</span></span>

### <a name="create-a-menu-item-for-loading-of-transport-loads"></a><span data-ttu-id="0d4d9-126">สร้างรายการเมนูสำหรับการโหลดที่โหลดการขนส่ง</span><span class="sxs-lookup"><span data-stu-id="0d4d9-126">Create a menu item for loading of transport loads</span></span>

<span data-ttu-id="0d4d9-127">คุณต้องสร้างรายการเมนูใหม่ที่เปิดใช้งานโหลดการขนส่งที่จะถูกโหลด</span><span class="sxs-lookup"><span data-stu-id="0d4d9-127">You must create a new menu item that enables transport loads to be loaded.</span></span> <span data-ttu-id="0d4d9-128">โหลดการขนส่งช่วยให้คุณสามารถจัดกลุ่มรายการงานได้จากโหลดหนึ่งหรือหลายการ</span><span class="sxs-lookup"><span data-stu-id="0d4d9-128">A transport load lets you group work lines from one load or multiple loads.</span></span> <span data-ttu-id="0d4d9-129">จากนั้น ทุกสิ่งที่เพิ่มเข้าไปยังโหลดการขนส่งสามารถจัดส่งได้ โดยใช้เครื่องสแกนเคลื่อนที่</span><span class="sxs-lookup"><span data-stu-id="0d4d9-129">Everything that is added to the transport load can then be shipped by using a mobile scanner.</span></span>

1. <span data-ttu-id="0d4d9-130">เลือก **การจัดการคลังสินค้า** \> **การตั้งค่า** \> **อุปกรณ์เคลื่อนที่** \> **รายการเมนูอุปกรณ์เคลื่อนที่**</span><span class="sxs-lookup"><span data-stu-id="0d4d9-130">Select **Warehouse management** \> **Setup** \> **Mobile device** \> **Mobile device menu items**.</span></span>
2. <span data-ttu-id="0d4d9-131">เลือก **สร้าง** และจากนั้นในฟิลด์ **โหมด** เลือก **งาน**</span><span class="sxs-lookup"><span data-stu-id="0d4d9-131">Select **New**, and then, in the **Mode** field, select **Work**.</span></span>
3. <span data-ttu-id="0d4d9-132">ตั้งค่าตัวเลือก **ใช้งานที่มีอยู่** เป็น **ใช่**</span><span class="sxs-lookup"><span data-stu-id="0d4d9-132">Set the **Use existing work** option to **Yes**.</span></span>
4. <span data-ttu-id="0d4d9-133">บนแท็บ **ทั่วไป** ในฟิลด์ **สั่งการโดย** เลือก **การโหลดการขนส่ง**</span><span class="sxs-lookup"><span data-stu-id="0d4d9-133">On the **General** tab, in the **Directed by** field, select **Transport loading**.</span></span>
5. <span data-ttu-id="0d4d9-134">ในการยืนยันการจัดส่งบนสแกนเนอร์เคลื่อนที่ ในฟิลด์ **ชนิดการยืนยันการจัดส่งที่ได้รับอนุญาต** เลือก **โหลดการขนส่ง**</span><span class="sxs-lookup"><span data-stu-id="0d4d9-134">To enable shipment confirmation on a mobile scanner, in the **Allowed ship confirmation type** field, select **Transport load**.</span></span>

## <a name="confirm-shipment-of-a-transport-load-from-the-client"></a><span data-ttu-id="0d4d9-135">ยืนยันการจัดส่งของโหลดการขนส่งจากไคลเอนต์</span><span class="sxs-lookup"><span data-stu-id="0d4d9-135">Confirm shipment of a transport load from the client</span></span>

<span data-ttu-id="0d4d9-136">การตั้งค่านี้ช่วยให้สามารถคุณยืนยันโหลดการขนส่ง ที่มีการโหลดเต็มจำนวนหรือโหลดที่มีการโหลดบางส่วนที่จะจัดส่ง</span><span class="sxs-lookup"><span data-stu-id="0d4d9-136">This setup lets you confirm a transport load that includes a full load or a partially loaded load to be shipped.</span></span>

1. <span data-ttu-id="0d4d9-137">เลือก **การบริหารคลังสินค้า** \> **โหลด** \> **โหลดการขนส่ง**</span><span class="sxs-lookup"><span data-stu-id="0d4d9-137">Select **Warehouse management** \> **Loads** \> **Transport loads**.</span></span>
2. <span data-ttu-id="0d4d9-138">บนบานหน้าต่างการดำเนินการ บนแท็บ **จัดส่งและรับ** ในกลุ่ม **ยืนยัน** เลือก **การขนส่ง**</span><span class="sxs-lookup"><span data-stu-id="0d4d9-138">On the Action Pane, on the **Ship and receive** tab, in the **Confirm** group, select **Transport**.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]