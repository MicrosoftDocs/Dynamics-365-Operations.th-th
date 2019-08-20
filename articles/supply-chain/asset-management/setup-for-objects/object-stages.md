---
title: สถานะของวงจรการใช้ของสินทรัพย์
description: หัวข้อนี้จะอธิบายถึงสถานะของวงจรการใช้และแบบจำลองวงจรการใช้งานของสินทรัพย์ในการจัดการสินทรัพย์
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
ms.openlocfilehash: 2dc72c61ed4dbb04122c6859123307dc79f2b233
ms.sourcegitcommit: 747bcd25ce7c6c20ce9eaa0027e730f74d4fd6aa
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 07/23/2019
ms.locfileid: "1783619"
---
# <a name="asset-lifecycle-states"></a><span data-ttu-id="6924b-103">สถานะของวงจรการใช้ของสินทรัพย์</span><span class="sxs-lookup"><span data-stu-id="6924b-103">Asset lifecycle states</span></span>

[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]

<span data-ttu-id="6924b-104">หัวข้อนี้จะอธิบายถึงสถานะของวงจรการใช้และแบบจำลองวงจรการใช้งานของสินทรัพย์ในการจัดการสินทรัพย์</span><span class="sxs-lookup"><span data-stu-id="6924b-104">This topic explains asset lifecycle states and lifecycle models in Asset Management.</span></span> <span data-ttu-id="6924b-105">สถานะของวงจรการใช้ของสินทรัพย์ถูกใช้ในการกำหนดว่าสินทรัพย์นั้นใช้งานอยู่ หรือไม่ได้ใช้งานอยู่</span><span class="sxs-lookup"><span data-stu-id="6924b-105">Asset lifecycle states are used to define whether an asset is active or inactive.</span></span> <span data-ttu-id="6924b-106">ตัวอย่างเช่น คุณสามารถตั้งค่าสถานะของวงจรการใช้ของสินทรัพย์ได้ เช่น **สร้างแล้ว** **ใช้งานอยู่** และ **สิ้นสุดแล้ว**</span><span class="sxs-lookup"><span data-stu-id="6924b-106">For example, you can set up asset lifecycle states such as **Created**, **Active**, and **Terminated**.</span></span>

> [!NOTE]
> - <span data-ttu-id="6924b-107">สถานะของวงจรการใช้ของคำขอจะเชื่อมโยงกับสถานะของวงจรการใช้ของสินทรัพย์</span><span class="sxs-lookup"><span data-stu-id="6924b-107">Request lifecycle states are linked to asset lifecycle states.</span></span> <span data-ttu-id="6924b-108">ดังนั้น เมื่อมีการเปลี่ยนแปลงคำขอไปยังสถานะของวงจรการใช้ของคำขอใหม่ จะมีการเปลี่ยนแปลงสินทรัพย์ที่ถูกแนบกับคำขอเป็นสถานะของวงจรการใช้ของสินทรัพย์ใหม่</span><span class="sxs-lookup"><span data-stu-id="6924b-108">Therefore, when a request is changed to a new request lifecycle state, the asset that is attached to the request is changed to a new asset lifecycle state.</span></span> <span data-ttu-id="6924b-109">ตัวอย่างเช่น ถ้าสถานะของวงจรการใช้ของคำขอถูกเปลี่ยนเป็น **ขาเข้า** สถานะของวงจรการใช้ของสินทรัพย์ที่แนบจะถูกเปลี่ยนเป็นสถานะของวงจรการใช้ที่เลือกไว้ในฟิลด์ **สถานะของวงจรการใช้ขาเข้า** บน FastTab **สถานะของวงจรการใช้ของสินทรัพย์** ของหน้า **แบบจำลองสถานะของวงจรการใช้ของสินทรัพย์**</span><span class="sxs-lookup"><span data-stu-id="6924b-109">For example, if the lifecycle state of a request is changed to **Inbound**, the lifecycle state of the attached asset is changed to the lifecycle state that is selected in the **Inbound lifecycle state** field on the **Asset lifecycle state** FastTab of the **Asset lifecycle state models** page.</span></span> 


<span data-ttu-id="6924b-110">คุณสามารถตั้งค่าสถานะของวงจรการใช้ของสินทรัพย์ในแบบจำลองวงจรการใช้งานของสินทรัพย์ ที่ซึ่งคุณสามารถกำหนดสถานะของวงจรการใช้ที่จำเป็นสำหรับสินทรัพย์ชนิดต่างๆ ได้</span><span class="sxs-lookup"><span data-stu-id="6924b-110">Asset lifecycle states can be set up in asset lifecycle models, where you can define the required lifecycle states for various types of assets.</span></span> <span data-ttu-id="6924b-111">คุณต้องตั้งค่าสถานะของวงจรการใช้ก่อน</span><span class="sxs-lookup"><span data-stu-id="6924b-111">You first set up lifecycle states.</span></span> <span data-ttu-id="6924b-112">จากนั้น คุณสร้างแบบจำลองวงจรการใช้งาน และเลือกสถานะของวงจรการใช้สำหรับรายการนั้น</span><span class="sxs-lookup"><span data-stu-id="6924b-112">You then create a lifecycle model and select lifecycle states for it.</span></span>

1. <span data-ttu-id="6924b-113">เลือก **การจัดการสินทรัพย์** \> **การตั้งค่า** \> **สินทรัพย์** \> **สถานะของวงจรการใช้**</span><span class="sxs-lookup"><span data-stu-id="6924b-113">Select **Asset management** \> **Setup** \> **Assets** \> **Lifecycle states**.</span></span>
2. <span data-ttu-id="6924b-114">เลือก **สร้าง** เพื่อสร้างสถานะของวงจรการใช้ของสินทรัพย์ใหม่</span><span class="sxs-lookup"><span data-stu-id="6924b-114">Select **New** to create a new asset lifecycle state.</span></span>
3. <span data-ttu-id="6924b-115">ในฟิลด์ **สถานะของวงจรการใช้** ให้ป้อนรหัสสถานะของวงจรการใช้</span><span class="sxs-lookup"><span data-stu-id="6924b-115">In the **Lifecycle state** field, enter the lifecycle state ID.</span></span>
4. <span data-ttu-id="6924b-116">ในฟิลด์ **ชื่อ** ให้ป้อนคำอธิบาย</span><span class="sxs-lookup"><span data-stu-id="6924b-116">In the **Name** field, enter a description.</span></span>

    <span data-ttu-id="6924b-117">ฟิลด์ **แบบจำลองวงจรการใช้งาน** จะแสดงจำนวนของแบบจำลองวงจรการใช้งานของสินทรัพย์ที่ใช้ในสถานะของวงจรการใช้ของสินทรัพย์</span><span class="sxs-lookup"><span data-stu-id="6924b-117">The **Lifecycle models** field shows the number of asset lifecycle models that use the asset lifecycle state.</span></span>

5. <span data-ttu-id="6924b-118">ตั้งค่าตัวเลือก **ใช้งานอยู่** เป็น **ใช่** ถ้าสถานะของวงจรการใช้นี้ควรจะเป็นสถานะของวงจรการใช้ที่ใช้งานอยู่ (กล่าวคือ ถ้าสามารถสร้างใบสั่งงานสำหรับสินทรัพย์ที่อยู่ในสถานะของวงจรการใช้นี้ได้)</span><span class="sxs-lookup"><span data-stu-id="6924b-118">Set the **Active** option to **Yes** if this lifecycle state should be an active lifecycle state (in other words, if work orders can be created for assets that are in this lifecycle state).</span></span>
6. <span data-ttu-id="6924b-119">ตั้งค่าตัวเลือก **ลบรายการปฏิทินที่เปิด** เป็น **ใช่** ถ้ารายการปฏิทินสินทรัพย์ที่เปิดที่มีสถานะของวงจรการใช้ของสินทรัพย์เป็น **สร้างแล้ว** ควรถูกลบ เมื่ออยู่ในสถานะของวงจรการใช้นี้</span><span class="sxs-lookup"><span data-stu-id="6924b-119">Set the **Delete open calendar lines** option to **Yes** if open asset calendar lines that have an asset lifecycle state of **Created** should be deleted when they are in this lifecycle state.</span></span> <span data-ttu-id="6924b-120">การตั้งค่านี้มีประโยชน์ ถ้าคุณต้องการล้างข้อมูลกำหนดการบำรุงรักษาที่เปิดค้างไว้ใดๆ ซึ่งไม่เกี่ยวข้องกับสินทรัพย์อีกต่อไป (ตัวอย่างเช่น ถ้าสินทรัพย์ไม่มีการใช้งานอีกต่อไป)</span><span class="sxs-lookup"><span data-stu-id="6924b-120">This setting is useful if you want to clean up any open maintenance schedules that are no longer relevant for the asset (for example, if the asset is no longer active).</span></span>

> [!NOTE]
> <span data-ttu-id="6924b-121">สถานะของวงจรการใช้ของสินทรัพย์ แบบจำลองวงจรการใช้งานของสินทรัพย์ และชนิดของสินทรัพย์ เกี่ยวข้องกัน</span><span class="sxs-lookup"><span data-stu-id="6924b-121">Asset lifecycle states, asset lifecycle models, and asset types are related.</span></span> <span data-ttu-id="6924b-122">จะมีการใช้ในลักษณะเดียวกับสถานะของวงจรการใช้ของใบสั่งงาน แบบจำลองวงจรการใช้งานของใบสั่งงาน และชนิดใบสั่งงาน</span><span class="sxs-lookup"><span data-stu-id="6924b-122">They are used in the same way as work order lifecycle states, work order lifecycle models, and work order types.</span></span> 


<span data-ttu-id="6924b-123">หลังจากที่คุณได้สร้างสถานะของวงจรการใช้ของสินทรัพย์ที่ต้องการแล้ว คุณสามารถตั้งค่าสถานะของวงจรการใช้ในแบบจำลองวงจรการใช้งานของสินทรัพย์ได้</span><span class="sxs-lookup"><span data-stu-id="6924b-123">After you've created the required asset lifecycle states, you can set up lifecycle states in asset lifecycle models.</span></span>

1. <span data-ttu-id="6924b-124">เลือก **การจัดการสินทรัพย์** \> **การตั้งค่า** \> **สินทรัพย์** \> **แบบจำลองวงจรการใช้งาน**</span><span class="sxs-lookup"><span data-stu-id="6924b-124">Select **Asset management** \> **Setup** \> **assets** \> **lifecycle models**.</span></span>
2. <span data-ttu-id="6924b-125">เลือก **สร้าง** เพื่อสร้างแบบจำลองวงจรการใช้งานของสินทรัพย์ใหม่</span><span class="sxs-lookup"><span data-stu-id="6924b-125">Select **New** to create a new asset lifecycle model.</span></span>
3. <span data-ttu-id="6924b-126">ในฟิลด์ **แบบจำลองวงจรการใช้งาน** ให้ป้อนรหัสแบบจำลองวงจรการใช้งาน</span><span class="sxs-lookup"><span data-stu-id="6924b-126">In the **Lifecycle model** field, enter the lifecycle model ID.</span></span>
4. <span data-ttu-id="6924b-127">ในฟิลด์ **ชื่อ** ให้ป้อนคำอธิบาย</span><span class="sxs-lookup"><span data-stu-id="6924b-127">In the **Name** field, enter a description.</span></span>

    <span data-ttu-id="6924b-128">ฟิลด์ **สถานะของวงจรการใช้** จะแสดงจำนวนของสถานะของวงจรการใช้ของสินทรัพย์ที่ถูกเลือกในแบบจำลองวงจรการใช้งานของสินทรัพย์</span><span class="sxs-lookup"><span data-stu-id="6924b-128">The **Lifecycle states** field shows the number of asset lifecycle states that are selected in the asset lifecycle model.</span></span> <span data-ttu-id="6924b-129">ฟิลด์ **ชนิดสินทรัพย์** จะแสดงจำนวนของชนิดสินทรัพย์ที่ใช้แบบจำลองวงจรการใช้งาน</span><span class="sxs-lookup"><span data-stu-id="6924b-129">The **Asset types** field shows the number of asset types that use the lifecycle model.</span></span>

5. <span data-ttu-id="6924b-130">บน FastTab **สถานะของวงจรการใช้** ให้เลือกสถานะของวงจรการใช้ของสินทรัพย์ที่ควรถูกรวมไว้ในแบบจำลองวงจรการใช้งานของสินทรัพย์:</span><span class="sxs-lookup"><span data-stu-id="6924b-130">On the **Lifecycle states** FastTab, select the asset lifecycle states that should be included in the asset lifecycle model:</span></span>

    - <span data-ttu-id="6924b-131">ถ้าต้องการใช้สถานะของวงจรการใช้สำหรับแบบจำลอง ให้เลือกในส่วน **สถานะของวงจรการใช้ที่เหลือ** และจากนั้น เลือกปุ่มลูกศรขวา ![ลูกศรขวา](media/15-setup-for-objects.png) เพื่อย้ายไปยังส่วน **สถานะของวงจรการใช้ที่เลือก**</span><span class="sxs-lookup"><span data-stu-id="6924b-131">To use a lifecycle state for the model, select it in the **Lifecycle states remaining** section, and then select the right arrow button ![Right arrow](media/15-setup-for-objects.png) to move it to the **Lifecycle states selected** section.</span></span>
    - <span data-ttu-id="6924b-132">เพื่อใช้สถานะของวงจรการใช้ที่พร้อมใช้งานทั้งหมดสำหรับแบบจำลอง ให้เลือกปุ่ม **สถานะของวงจรการใช้ทั้งหมดที่พร้อมใช้งาน** ![สถานะของวงจรการใช้ทั้งหมดที่พร้อมใช้งาน](media/20-setup-for-objects.png)</span><span class="sxs-lookup"><span data-stu-id="6924b-132">To use all the available lifecycle states for the model, select the **All available lifecycle states** button ![All available lifecycle states](media/20-setup-for-objects.png).</span></span> <span data-ttu-id="6924b-133">สถานะของวงจรการใช้ทั้งหมดจะถูกโอนย้ายไปยังส่วน **สถานะของวงจรการใช้ที่เลือก**</span><span class="sxs-lookup"><span data-stu-id="6924b-133">All lifecycle states are transferred to the **Lifecycle states selected** section.</span></span>
    - <span data-ttu-id="6924b-134">ถ้าต้องการลบสถานะของวงจรการใช้ออกจากแบบจำลอง ให้เลือกในส่วน **สถานะของวงจรการใช้ที่เลือก** และจากนั้น เลือกปุ่มลูกศรซ้าย ![ลูกศรซ้าย](media/16-setup-for-objects.png) เพื่อย้ายไปยังส่วน **สถานะของวงจรการใช้ที่เหลือ**</span><span class="sxs-lookup"><span data-stu-id="6924b-134">To remove a lifecycle state from the model, select it in the **lifecycle states selected** section, and then select the left arrow button ![Left arrow](media/16-setup-for-objects.png) to move it to the **Lifecycle states remaining** section.</span></span>

6. <span data-ttu-id="6924b-135">เลือก **การปรับปรุงสถานะของวงจรการใช้** เพื่อกำหนดสถานะของวงจรการใช้สินทรัพย์ที่สามารถทำตามสถานะของวงจรการใช้ที่เลือกได้</span><span class="sxs-lookup"><span data-stu-id="6924b-135">Select **Lifecycle state updates** to define the asset lifecycle states that can follow a selected lifecycle state.</span></span>
7. <span data-ttu-id="6924b-136">คุณใช้ FastTab **สถานะสินทรัพย์** ถ้าคุณจัดการกับสินทรัพย์ที่คุณได้รับสำหรับการซ่อมแซม</span><span class="sxs-lookup"><span data-stu-id="6924b-136">You use the **Asset state** FastTab if you handle assets that you receive for repair.</span></span> <span data-ttu-id="6924b-137">ในส่วน **ขาเข้า/ขาออก** คุณสามารถเลือกสถานะของวงจรการใช้ของสินทรัพย์เพื่อบ่งชี้ลำดับงานของสินทรัพย์ที่คุณได้รับสำหรับการซ่อมแซม</span><span class="sxs-lookup"><span data-stu-id="6924b-137">In the **Inbound/outbound** section, you can select asset lifecycle states to indicate the workflow of an asset that you receive for repair.</span></span> <span data-ttu-id="6924b-138">หากคุณมีสินทรัพย์ที่ให้ยืมแก่ลูกค้าหรือแผนกในส่วน **การกู้ยืม** คุณสามารถเลือกสถานะของวงจรการใช้สำหรับสินทรัพย์ที่ให้ยืมได้</span><span class="sxs-lookup"><span data-stu-id="6924b-138">If you offer loan assets to customers or departments, in the **Loan** section, you can select lifecycle states for loan assets.</span></span>
