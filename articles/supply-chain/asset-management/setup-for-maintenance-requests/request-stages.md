---
title: สถานะของวงจรการใช้ของคำขอการบำรุงรักษา
description: หัวข้อนี้อธิบายวิธีการตั้งค่าสถานะของวงจรการใช้ของคำขอการบำรุงรักษาในการจัดการสินทรัพย์
author: josaw1
manager: tfehr
ms.date: 07/26/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 9d1e4412af0619b57467b5bcba75ea7259604d1d
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 04/02/2020
ms.locfileid: "3209018"
---
# <a name="maintenance-request-lifecycle-states"></a><span data-ttu-id="c108b-103">สถานะของวงจรการใช้ของคำขอการบำรุงรักษา</span><span class="sxs-lookup"><span data-stu-id="c108b-103">Maintenance request lifecycle states</span></span>

[!include [banner](../../includes/banner.md)]

 


<span data-ttu-id="c108b-104">สถานะของวงจรการใช้ของคำขอการบำรุงรักษาจะกำหนดขั้นตอนที่คำขอสามารถผ่านไปได้</span><span class="sxs-lookup"><span data-stu-id="c108b-104">Maintenance request lifecycle states define the stages that a request can go through.</span></span> <span data-ttu-id="c108b-105">ตัวอย่างประกอบด้วย **สร้างแล้ว** **ใช้งานอยู่** และ **สิ้นสุดแล้ว**</span><span class="sxs-lookup"><span data-stu-id="c108b-105">Examples include **Created**, **Active**, and **Ended**.</span></span> <span data-ttu-id="c108b-106">เมื่อคำขอการบำรุงรักษาถูกแปลงเป็นใบสั่งงาน สถานะของวงจรการใช้ของคำขอการบำรุงรักษาควรถูกปรับปรุงเป็น **สิ้นสุดแล้ว** หรือ **ปิดแล้ว** เพื่อบ่งชี้ว่าไม่มีการใช้งานคำขอการบำรุงรักษาอีกต่อไป</span><span class="sxs-lookup"><span data-stu-id="c108b-106">When a maintenance request is converted to a work order, the maintenance request lifecycle state should be updated to **Ended** or **Closed** to indicate that the maintenance request is no longer active.</span></span> <span data-ttu-id="c108b-107">ในหน้ารายการ **คำขอการบำรุงรักษาทั้งหมด** คุณสามารถดูคำขอการบำรุงรักษาทั้งหมด โดยไม่คำนึงถึงสถานะของวงจรการใช้</span><span class="sxs-lookup"><span data-stu-id="c108b-107">On the **All maintenance requests** list page, you can view all maintenance requests, regardless of their lifecycle state.</span></span>

## <a name="set-up-maintenance-request-lifecycle-states"></a><span data-ttu-id="c108b-108">ตั้งค่าสถานะของวงจรการใช้ของคำขอการบำรุงรักษา</span><span class="sxs-lookup"><span data-stu-id="c108b-108">Set up maintenance request lifecycle states</span></span>

1. <span data-ttu-id="c108b-109">เลือก **การจัดการสินทรัพย์** \> **การตั้งค่า** \> **คำขอการบำรุงรักษา** \> **สถานะของวงจรการใช้**</span><span class="sxs-lookup"><span data-stu-id="c108b-109">Select **Asset management** \> **Setup** \> **Maintenance requests** \> **Lifecycle states**.</span></span>
2. <span data-ttu-id="c108b-110">เลือก **สร้าง** เพื่อสร้างสถานะของวงจรการใช้ของคำขอการบำรุงรักษา</span><span class="sxs-lookup"><span data-stu-id="c108b-110">Select **New** to create a maintenance request lifecycle state.</span></span>
3. <span data-ttu-id="c108b-111">ในฟิลด์ **สถานะของวงจรการใช้** ให้ป้อนรหัสสำหรับสถานะของวงจรการใช้</span><span class="sxs-lookup"><span data-stu-id="c108b-111">In the **Lifecycle state** field, enter an ID for the lifecycle state.</span></span>
4. <span data-ttu-id="c108b-112">ในฟิลด์ **ชื่อ** ป้อนชื่อ</span><span class="sxs-lookup"><span data-stu-id="c108b-112">In the **Name** field, enter a name.</span></span>

    <span data-ttu-id="c108b-113">บน FastTab **รายละเอียด** ฟิลด์ **แบบจำลองวงจรการใช้งาน** จะแสดงจำนวนของแบบจำลองวงจรการใช้งานของคำขอการบำรุงรักษาที่ใช้สถานะของวงจรการใช้นี้</span><span class="sxs-lookup"><span data-stu-id="c108b-113">On the **Details** FastTab, the **Lifecycle models** field shows the number of maintenance request lifecycle models that use this lifecycle state.</span></span>

5. <span data-ttu-id="c108b-114">บน FastTab **ทั่วไป** ให้ตั้งค่าตัวเลือก **ที่ใช้งานอยู่** เป็น **ใช่** ถ้าคำขอการบำรุงรักษาควรจะใช้งานอยู่ ในขณะที่อยู่ในสถานะของวงจรการใช้นี้</span><span class="sxs-lookup"><span data-stu-id="c108b-114">On the **General** FastTab, set the **Active** option to **Yes** if a maintenance request should be active while it's in this lifecycle state.</span></span>
6. <span data-ttu-id="c108b-115">ตั้งค่าตัวเลือก **ตั้งค่าจุดสิ้นสุดจริง** เป็น **ใช่** ถ้าวันที่และเวลาสิ้นสุดจริงควรถูกป้อนโดยอัตโนมัติในคำขอการบำรุงรักษาที่อยู่ในสถานะของวงจรการใช้นี้</span><span class="sxs-lookup"><span data-stu-id="c108b-115">Set he **Set actual end** option to **Yes** if an actual end date and time should automatically be entered on a maintenance request that is in this lifecycle state.</span></span>
7. <span data-ttu-id="c108b-116">ตั้งค่าตัวเลือก **สร้างใบสั่งงาน** เป็น **ใช่** ถ้าสามารถสร้างใบสั่งงานได้จากคำขอการบำรุงรักษาที่อยู่ในสถานะของวงจรการใช้นี้</span><span class="sxs-lookup"><span data-stu-id="c108b-116">Set the **Create work order** option to **Yes** if a work order can be created from a maintenance request that is in this lifecycle state.</span></span>
8. <span data-ttu-id="c108b-117">ตั้งค่าตัวเลือก **ลบ** เป็น **ใช่** ถ้าคำขอการบำรุงรักษาสามารถถูกลบได้ ในขณะที่อยู่ในสถานะของวงจรการใช้นี้</span><span class="sxs-lookup"><span data-stu-id="c108b-117">Set the **Delete** option to **Yes** if a maintenance request can be deleted while it's in this lifecycle state.</span></span>
9. <span data-ttu-id="c108b-118">บน FastTab **ปรับปรุง** ตัวเลือก **ขาเข้า** และ **ขาออก** ในส่วน **สินทรัพย์** จะเกี่ยวข้องกัน ถ้าคุณใช้การซ่อมแซมคลัง .cSet ตัวเลือกที่เหมาะสมเป็น **ใช่** ถ้าสถานะของวงจรการใช้สินทรัพย์ของสินทรัพย์ที่ถูกเลือกในคำขอบำรุงรักษาควรถูกปรับปรุงเป็น **ขาเข้า** หรือ **ขาออก** โดยอัตโนมัติ เมื่อสถานะของวงจรการใช้ของคำขอการบำรุงรักษาของคำขอการบำรุงรักษาถูกตั้งค่าเป็น **ขาเข้า** หรือ **ขาออก**</span><span class="sxs-lookup"><span data-stu-id="c108b-118">On the **Update** FastTab, the **Inbound** and **Outbound** options in the **Asset** section are relevant if you use depot repair.cSet the appropriate option to **Yes** if the asset lifecycle state of assets that are selected on a maintenance request should automatically be updated to **Inbound** or **Outbound** when the maintenance request lifecycle state of that maintenance request is set to **Inbound** or **Outbound**.</span></span>

<span data-ttu-id="c108b-119">ภาพประกอบต่อไปนี้แสดงตัวอย่างของหน้า **สถานะของวงจรการใช้ของคำขอการบำรุงรักษา**</span><span class="sxs-lookup"><span data-stu-id="c108b-119">The follow illustration shows an example of the **Maintenance request lifecycle states** page.</span></span>

![หน้าสถานะของวงจรการใช้ของคำขอการบำรุงรักษา](media/02-setup-for-requests.png)

> [!NOTE]
> <span data-ttu-id="c108b-121">สถานะของวงจรการใช้ของคำขอการบำรุงรักษา กลุ่มสถานะของวงจรการใช้ และชนิดต่างๆ เกี่ยวข้องและถูกใช้ในลักษณะเดียวกับสถานะของวงจรการใช้ของใบสั่งงาน กลุ่มสถานะของวงจรการใช้ และชนิดต่างๆ</span><span class="sxs-lookup"><span data-stu-id="c108b-121">Maintenance request lifecycle states, lifecycle state groups, and types are related to, and used in the same way as, work order lifecycle states, lifecycle state groups, and types.</span></span> 

## <a name="set-up-maintenance-request-lifecycle-models"></a><span data-ttu-id="c108b-122">ตั้งค่าแบบจำลองวงจรการใช้งานของคำขอการบำรุงรักษา</span><span class="sxs-lookup"><span data-stu-id="c108b-122">Set up maintenance request lifecycle models</span></span>

<span data-ttu-id="c108b-123">หลังจากที่คุณได้สร้างสถานะของวงจรการใช้ที่จำเป็นสำหรับคำขอการบำรุงรักษาของคุณแล้ว จะสามารถแบ่งออกเป็นกลุ่มสถานะของวงจรการใช้ หรือแบบจำลองวงจรการใช้งานได้</span><span class="sxs-lookup"><span data-stu-id="c108b-123">After you've created the lifecycle states that are required for your maintenance requests, they can be divided into lifecycle state groups, or lifecycle models.</span></span> <span data-ttu-id="c108b-124">แบบจำลองวงจรการใช้งานของคำขอการบำรุงรักษาจะถูกใช้เพื่อสร้างโฟลว์ที่สามารถใช้สำหรับคำขอการบำรุงรักษาชนิดต่างๆ</span><span class="sxs-lookup"><span data-stu-id="c108b-124">Maintenance request lifecycle models are used to create the flow that can be used for different types of maintenance requests.</span></span> <span data-ttu-id="c108b-125">อย่างน้อยที่สุด ควรมีการสร้างแบบจำลองวงจรการใช้งานของคำขอการบำรุงรักษามาตรฐานหนึ่งรายการ</span><span class="sxs-lookup"><span data-stu-id="c108b-125">At a minimum, one standard maintenance request lifecycle model should be created.</span></span>

1. <span data-ttu-id="c108b-126">เลือก **การจัดการสินทรัพย์** \> **การตั้งค่า** \> **คำขอการบำรุงรักษา** \> **แบบจำลองวงจรการใช้งาน**</span><span class="sxs-lookup"><span data-stu-id="c108b-126">Select **Asset management** \> **Setup** \> **Maintenance requests** \> **Lifecycle models**.</span></span>
2. <span data-ttu-id="c108b-127">เลือก **สร้าง** เพื่อสร้างแบบจำลองวงจรการใช้งานของคำขอการบำรุงรักษา</span><span class="sxs-lookup"><span data-stu-id="c108b-127">Select **New** to create a maintenance request lifecycle model.</span></span>
3. <span data-ttu-id="c108b-128">ในฟิลด์ **แบบจำลองวงจรการใช้งาน** ให้ป้อนรหัสสำหรับแบบจำลองวงจรการใช้งาน</span><span class="sxs-lookup"><span data-stu-id="c108b-128">In the **Lifecycle model** field, enter an ID for the lifecycle model.</span></span>
4. <span data-ttu-id="c108b-129">ในฟิลด์ **ชื่อ** ป้อนชื่อ</span><span class="sxs-lookup"><span data-stu-id="c108b-129">In the **Name** field, enter a name.</span></span>

    <span data-ttu-id="c108b-130">บน FastTab **รายละเอียด** ฟิลด์ **สถานะของวงจรการใช้** จะแสดงจำนวนของสถานะของวงจรการใช้ที่ถูกเลือกในแบบจำลองวงจรการใช้งานนี้</span><span class="sxs-lookup"><span data-stu-id="c108b-130">On the **Details** FastTab, the **Lifecycle states** shows the number of lifecycle states that are selected in this lifecycle model.</span></span> <span data-ttu-id="c108b-131">ฟิลด์ **ชนิดคำขอการบำรุงรักษา** จะแสดงจำนวนของชนิดคำขอการบำรุงรักษาที่ใช้แบบจำลองวงจรการใช้งานนี้</span><span class="sxs-lookup"><span data-stu-id="c108b-131">The **Maintenance request types** field shows the number of maintenance request types that use this lifecycle model.</span></span>

5. <span data-ttu-id="c108b-132">บน FastTab **สถานะของวงจรการใช้** ให้เลือกสถานะของวงจรการใช้ที่ควรถูกรวมไว้ในแบบจำลองวงจรการใช้งาน:</span><span class="sxs-lookup"><span data-stu-id="c108b-132">On the **Lifecycle states** FastTab, select the lifecycle states that should be included in the lifecycle model:</span></span>

    - <span data-ttu-id="c108b-133">ถ้าต้องการรวมสถานะของวงจรการใช้ในแบบจำลองวงจรการใช้งาน ให้เลือกในส่วน **สถานะของวงจรการใช้ที่เหลือ** และจากนั้น เลือกปุ่มลูกศรขวา ![ลูกศรขวา](media/03-setup-for-requests.png) เพื่อย้ายไปยังส่วน **สถานะของวงจรการใช้ที่เลือก**</span><span class="sxs-lookup"><span data-stu-id="c108b-133">To include a lifecycle state in the lifecycle model, select it in the **Lifecycle states remaining** section, and then select the right arrow button ![Right arrow](media/03-setup-for-requests.png) to move it to the **Lifecycle states selected** section.</span></span>
    - <span data-ttu-id="c108b-134">เพื่อรวมสถานะของวงจรการใช้ที่พร้อมใช้งานทั้งหมดในแบบจำลองวงจรการใช้งาน ให้เลือกปุ่ม **เลือกสถานะทั้งหมดที่พร้อมใช้งาน** ![เลือกสถานะทั้งหมดที่พร้อมใช้งาน](media/04-setup-for-requests.png)</span><span class="sxs-lookup"><span data-stu-id="c108b-134">To include all the available lifecycle states in the lifecycle model, select the **Select all available states** button ![Select all available states](media/04-setup-for-requests.png).</span></span> <span data-ttu-id="c108b-135">สถานะของวงจรการใช้ทั้งหมดจะถูกย้ายไปยังส่วน **สถานะของวงจรการใช้ที่เลือก**</span><span class="sxs-lookup"><span data-stu-id="c108b-135">All lifecycle states are moved to the **Lifecycle states selected** section.</span></span>
    - <span data-ttu-id="c108b-136">ถ้าต้องการลบสถานะของวงจรการใช้ออกจากแบบจำลองวงจรการใช้งาน ให้เลือกในส่วน **สถานะของวงจรการใช้ที่เลือก** และจากนั้น เลือกปุ่มลูกศรซ้าย ![ลูกศรซ้าย](media/05-setup-for-requests.png) เพื่อย้ายไปยังส่วน **สถานะของวงจรการใช้ที่เหลือ**</span><span class="sxs-lookup"><span data-stu-id="c108b-136">To remove a lifecycle state from the lifecycle model, select it in the **Lifecycle states selected** section, and then select the left arrow button ![Left arrow](media/05-setup-for-requests.png) to move it to the **Lifecycle states remaining** section.</span></span>

6. <span data-ttu-id="c108b-137">บน FastTab **ทั่วไป** ฟิลด์ในส่วน **การปรับปรุง** จะเกี่ยวข้อง ถ้าคุณใช้การซ่อมแซมคลัง</span><span class="sxs-lookup"><span data-stu-id="c108b-137">On the **General** FastTab, the fields in the **Updates** section are relevant if you use depot repair.</span></span>

    - <span data-ttu-id="c108b-138">ในฟิลด์ **สถานะของวงจรการใช้สำหรับสินทรัพย์ที่ได้รับ** ให้เลือกสถานะของวงจรการใช้ของสินทรัพย์ที่มีการเลือกในคำขอการบำรุงรักษา ควรจะได้รับการปรับปรุงโดยอัตโนมัติ เมื่อได้รับการซ่อมแซมคลัง</span><span class="sxs-lookup"><span data-stu-id="c108b-138">In the **Lifecycle state for asset received** field, select the asset lifecycle state that assets that are selected on a maintenance request should automatically be updated to when they are received for depot repair.</span></span>
    - <span data-ttu-id="c108b-139">ในฟิลด์ **สถานะของวงจรการใช้สำหรับสินทรัพย์ที่จัดส่ง** ให้เลือกสถานะของวงจรการใช้ของสินทรัพย์ที่มีการเลือกในคำขอการบำรุงรักษา ควรจะได้รับการปรับปรุงโดยอัตโนมัติ เมื่อมีการส่งคืนหลังจากการซ่อมแซม</span><span class="sxs-lookup"><span data-stu-id="c108b-139">In the **Lifecycle state for asset delivered** field, select the lifecycle state that assets that are selected on a maintenance request should automatically be updated to when they are returned after repair.</span></span>

<span data-ttu-id="c108b-140">ภาพประกอบต่อไปนี้แสดงตัวอย่างของหน้า **แบบจำลองวงจรการใช้งานของคำขอการบำรุงรักษา**</span><span class="sxs-lookup"><span data-stu-id="c108b-140">The following illustration shows an example of the **Maintenance request lifecycle models** page.</span></span>

![หน้าแบบจำลองวงจรการใช้งานของคำขอการบำรุงรักษา](media/06-setup-for-requests.png)
