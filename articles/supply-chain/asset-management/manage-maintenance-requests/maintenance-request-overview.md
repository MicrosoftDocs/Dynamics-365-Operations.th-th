---
title: คำขอการบำรุงรักษา
description: หัวข้อนี้แสดงภาพรวมเกี่ยวกับการจัดการคำขอการบำรุงรักษาในการจัดการสินทรัพย์
author: josaw1
manager: tfehr
ms.date: 10/01/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EntAssetRequestTable, EntAssetRequestWorkspace, EntAssetRequestActivePart, EntAssetRequestWorkOrderActive, EntAssetRequestType, EntAssetRequestTableCreateWO, EntAssetRequestTableLookup, EntAssetRequestTableActivePart, EntAssetMobileRequestDetails
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 7038269c66092367a0faf147766cb45eb5364e1b
ms.sourcegitcommit: c986d5234b81d31cc6d054298be6f6ec92c1754c
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 09/25/2020
ms.locfileid: "3890140"
---
# <a name="maintenance-requests"></a><span data-ttu-id="435f5-103">คำขอการบำรุงรักษา</span><span class="sxs-lookup"><span data-stu-id="435f5-103">Maintenance requests</span></span>

[!include [banner](../../includes/banner.md)]

 

<span data-ttu-id="435f5-104">คำขอการบำรุงรักษาเป็นบันทึกย่อหรือการรายงานที่สร้างขึ้นเพื่อแจ้งให้ผู้จัดการหรือผู้วางแผนทราบว่า สินทรัพย์อาจต้องการการบำรุงรักษาหรืองานซ่อมแซม แต่ไม่มีการสร้างใบสั่งงาน</span><span class="sxs-lookup"><span data-stu-id="435f5-104">Maintenance requests are notes or declarations that are created to notify a manager or planner that an asset might require a maintenance or repair job, but without creating a work order.</span></span> <span data-ttu-id="435f5-105">ถ้าเนื้อหาของคำขอการบำรุงรักษาถูกพิจารณาแล้วว่าถูกต้อง จากนั้น จะสามารถสร้างใบสั่งงานตามคำขอการบำรุงรักษาได้</span><span class="sxs-lookup"><span data-stu-id="435f5-105">If the contents of a maintenance request are considered valid, a work order can then be created based on the maintenance request.</span></span>

<span data-ttu-id="435f5-106">สามารถสร้างคำขอการบำรุงรักษาสำหรับสินทรัพย์ใดๆ ในการจัดการสินทรัพย์ได้</span><span class="sxs-lookup"><span data-stu-id="435f5-106">Maintenance requests can be created for any asset in Asset Management.</span></span> <span data-ttu-id="435f5-107">สามารถสร้างคำขอการบำรุงรักษาชนิดต่างๆ ได้ โดยขึ้นอยู่กับวิธีที่บริษัทของคุณใช้คำขอการบำรุงรักษา</span><span class="sxs-lookup"><span data-stu-id="435f5-107">Various types of maintenance requests can be created, depending on how your company uses maintenance requests.</span></span> <span data-ttu-id="435f5-108">ยกตัวอย่างเช่น</span><span class="sxs-lookup"><span data-stu-id="435f5-108">Here are some examples:</span></span>

- <span data-ttu-id="435f5-109">คำขอการบำรุงรักษา</span><span class="sxs-lookup"><span data-stu-id="435f5-109">Maintenance requests</span></span>
- <span data-ttu-id="435f5-110">บันทึกย่อ</span><span class="sxs-lookup"><span data-stu-id="435f5-110">Notes</span></span>
- <span data-ttu-id="435f5-111">การแก้ไขหรือการปรับปรุง</span><span class="sxs-lookup"><span data-stu-id="435f5-111">Corrections or enhancements</span></span>
- <span data-ttu-id="435f5-112">เงินลงทุน</span><span class="sxs-lookup"><span data-stu-id="435f5-112">Investments</span></span>
- <span data-ttu-id="435f5-113">การซ่อมแซมคลัง (ชนิดนี้จะใช้เมื่อคุณได้รับสินทรัพย์จากสถานที่อื่น เพื่อให้คุณสามารถทำงานการบำรุงรักษาหรือซ่อมแซม และจากนั้น คุณส่งคืนสินทรัพย์หลังจากที่งานเสร็จสมบูรณ์)</span><span class="sxs-lookup"><span data-stu-id="435f5-113">Depot repair (This type is used when you receive assets from another location so that you can do a maintenance or repair job, and you then return the asset after the job is completed.)</span></span>

## <a name="view-maintenance-requests"></a><span data-ttu-id="435f5-114">ดูคำขอการบำรุงรักษา</span><span class="sxs-lookup"><span data-stu-id="435f5-114">View maintenance requests</span></span>

<span data-ttu-id="435f5-115">หากต้องการดูคำขอการบำรุงรักษา เลือก **การจัดการสินทรัพย์** \> **ทั่วไป** \> **คำขอการบำรุงรักษา** \> **คำขอการบำรุงรักษาทั้งหมด** **คำขอการบำรุงรักษาที่ใช้งานอยู่** หรือ **คำขอการบำรุงรักษาของตำแหน่งที่ทำงานของฉัน**</span><span class="sxs-lookup"><span data-stu-id="435f5-115">To view maintenance requests, select **Asset management** \> **Common** \> **Maintenance requests** \> **All maintenance requests**, **Active maintenance requests**, or **My functional location maintenance requests**.</span></span> <span data-ttu-id="435f5-116">หน้ารายการแต่ละหน้าจะแสดงข้อมูลบางอย่างที่เกี่ยวข้องกับคำขอการบำรุงรักษา</span><span class="sxs-lookup"><span data-stu-id="435f5-116">Each list page shows some of the information that is related to a maintenance request.</span></span>

![ดูคำขอการบำรุงรักษา](media/01-manage-maintenance-requests.png)

> [!NOTE]
> <span data-ttu-id="435f5-118">ใช้หน้ารายการ **คำขอการบำรุงรักษาของตำแหน่งที่ทำงานของฉัน** เพื่อดูรายการของคำขอการบำรุงรักษาที่ประกอบด้วยตำแหน่งที่ทำงานที่คุณเกี่ยวข้องในฐานะผู้ปฏิบัติงาน หรือสินทรัพย์ที่ถูกติดตั้งในตำแหน่งที่ทำงานที่คุณเกี่ยวข้องในฐานะผู้ปฏิบัติงาน</span><span class="sxs-lookup"><span data-stu-id="435f5-118">Use the **My functional location maintenance requests** list page to view a list of maintenance requests that contain either functional locations that you're related to as a worker or assets that are installed on functional locations that you're related to as a worker.</span></span> <span data-ttu-id="435f5-119">(สำหรับข้อมูลเกี่ยวกับวิธีการตั้งค่าตำแหน่งที่ทำงานในเจ้าหน้าที่บำรุงรักษา ดู [เจ้าหน้าที่บำรุงรักษาและกลุ่มผู้ปฏิบัติงาน](../setup-for-objects/workers-and-worker-groups.md))</span><span class="sxs-lookup"><span data-stu-id="435f5-119">(For information about how to set up functional locations on maintenance workers, see [Maintenance workers and worker groups](../setup-for-objects/workers-and-worker-groups.md).)</span></span>
> 
> <span data-ttu-id="435f5-120">แม้ว่าข้อมูลบัญชีลูกค้าจะพร้อมใช้งานในการจัดการบริการสินทรัพย์ (การบำรุงรักษาภายนอก) แต่จะไม่พร้อมใช้งานในการจัดการสินทรัพย์ (การบำรุงรักษาภายใน)</span><span class="sxs-lookup"><span data-stu-id="435f5-120">Although customer account information is available in Asset Service Management (external maintenance), it isn't available in Asset Management (internal maintenance).</span></span>

<span data-ttu-id="435f5-121">เมื่อต้องการเปิดมุมมองรายละเอียดของเรกคอร์ดบนหน้ารายการ **คำขอการบำรุงรักษาทั้งหมด** ในมุมมองกริด ให้เลือกลิงค์ในคอลัมน์ **คำขอการบำรุงรักษา**</span><span class="sxs-lookup"><span data-stu-id="435f5-121">To open the details view of a record, on the **All maintenance requests** list page, in the grid view, select a link in the **Maintenance request** column.</span></span>

![ดูรายละเอียดของคำขอการบำรุงรักษา](media/02-manage-maintenance-requests.png)

<span data-ttu-id="435f5-123">ปุ่มบนบานหน้าต่างการดำเนินการจะถูกจัดระเบียบบนแท็บ</span><span class="sxs-lookup"><span data-stu-id="435f5-123">The buttons on the Action Pane are organized on tabs.</span></span> <span data-ttu-id="435f5-124">ตารางต่อไปนี้จะอธิบายถึงปุ่มที่เกี่ยวข้องกับการจัดการสินทรัพย์อย่างคร่าวๆ</span><span class="sxs-lookup"><span data-stu-id="435f5-124">The following table briefly describes the buttons that are related to Asset Management.</span></span>

| <span data-ttu-id="435f5-125">ชื่อปุ่ม</span><span class="sxs-lookup"><span data-stu-id="435f5-125">Button name</span></span>                      | <span data-ttu-id="435f5-126">คำอธิบาย</span><span class="sxs-lookup"><span data-stu-id="435f5-126">Description</span></span> |
|----------------------------------|-------------|
| <span data-ttu-id="435f5-127">แก้ไข</span><span class="sxs-lookup"><span data-stu-id="435f5-127">Edit</span></span>                             | <span data-ttu-id="435f5-128">แก้ไขคำขอการบำรุงรักษาที่เลือก</span><span class="sxs-lookup"><span data-stu-id="435f5-128">Edit the selected maintenance request.</span></span> |
| <span data-ttu-id="435f5-129">สร้าง </span><span class="sxs-lookup"><span data-stu-id="435f5-129">New</span></span>                              | <span data-ttu-id="435f5-130">สร้างคำขอการบำรุงรักษาใหม่</span><span class="sxs-lookup"><span data-stu-id="435f5-130">Create a new maintenance request.</span></span> |
| <span data-ttu-id="435f5-131">ลบ</span><span class="sxs-lookup"><span data-stu-id="435f5-131">Delete</span></span>                           | <span data-ttu-id="435f5-132">ลบคำขอการบำรุงรักษาที่เลือก</span><span class="sxs-lookup"><span data-stu-id="435f5-132">Delete the selected maintenance request.</span></span> |
| <span data-ttu-id="435f5-133">กลุ่มใบสั่งงาน</span><span class="sxs-lookup"><span data-stu-id="435f5-133">Work order pool</span></span>                  | <span data-ttu-id="435f5-134">เชื่อมโยงคำขอการบำรุงรักษาที่เลือกกับกลุ่มใบสั่งงาน</span><span class="sxs-lookup"><span data-stu-id="435f5-134">Connect the selected maintenance request to a work order pool.</span></span> |
| <span data-ttu-id="435f5-135">ใบสั่งงาน</span><span class="sxs-lookup"><span data-stu-id="435f5-135">Work order</span></span>                       | <span data-ttu-id="435f5-136">สร้างใบสั่งงาน ตามคำขอการบำรุงรักษาที่เลือก</span><span class="sxs-lookup"><span data-stu-id="435f5-136">Create a work order, based on the selected maintenance request.</span></span> |
| <span data-ttu-id="435f5-137">ข้อบกพร่องของสินทรัพย์</span><span class="sxs-lookup"><span data-stu-id="435f5-137">Asset fault</span></span>                      | <span data-ttu-id="435f5-138">คลิก **ข้อบกพร่องของสินทรัพย์** ซึ่งคุณสามารถสร้างการลงทะเบียนข้อบกพร่องได้ในคำขอการบำรุงรักษาที่เลือก</span><span class="sxs-lookup"><span data-stu-id="435f5-138">Click **Asset faults**, where you can create a fault registration on the selected maintenance request.</span></span> |
| <span data-ttu-id="435f5-139">ใบสั่งงาน</span><span class="sxs-lookup"><span data-stu-id="435f5-139">Work orders</span></span>                      | <span data-ttu-id="435f5-140">แสดงรายการของใบสั่งงานทั้งหมดที่เชื่อมโยงกับคำขอการบำรุงรักษาที่เลือก</span><span class="sxs-lookup"><span data-stu-id="435f5-140">Show a list of all work orders that are connected to the selected maintenance request.</span></span> |
| <span data-ttu-id="435f5-141">ปรับปรุงสถานะคำขอการบำรุงรักษา</span><span class="sxs-lookup"><span data-stu-id="435f5-141">Update maintenance request state</span></span> | <span data-ttu-id="435f5-142">ปรับปรุงสถานะคำขอการบำรุงรักษา</span><span class="sxs-lookup"><span data-stu-id="435f5-142">Update the maintenance request state.</span></span> |
| <span data-ttu-id="435f5-143">ล็อกสถานะของวงจรการใช้</span><span class="sxs-lookup"><span data-stu-id="435f5-143">Lifecycle state log</span></span>              | <span data-ttu-id="435f5-144">ดูล็อกที่แสดงสถานะของวงจรการใช้ของคำขอการบำรุงรักษาที่เลือก</span><span class="sxs-lookup"><span data-stu-id="435f5-144">View a log that shows the lifecycle states of the selected maintenance request.</span></span> |
| <span data-ttu-id="435f5-145">รายละเอียดคำขอการบำรุงรักษา</span><span class="sxs-lookup"><span data-stu-id="435f5-145">Maintenance request details</span></span>      | <span data-ttu-id="435f5-146">พิมพ์รายงานที่แสดงรายละเอียดของคำขอการบำรุงรักษาที่เลือก</span><span class="sxs-lookup"><span data-stu-id="435f5-146">Print a report that shows details of the selected maintenance request.</span></span> |
| <span data-ttu-id="435f5-147">ส่งสินทรัพย์ที่ให้ยืม</span><span class="sxs-lookup"><span data-stu-id="435f5-147">Send loan asset</span></span>                  | <span data-ttu-id="435f5-148">เลือกสินทรัพย์ที่ให้ยืมที่ควรจะเป็นการแทนที่แบบชั่วคราวสำหรับสินทรัพย์ที่เลือกบนคำขอการบำรุงรักษาที่เลือก</span><span class="sxs-lookup"><span data-stu-id="435f5-148">Select a loan asset that should be a temporary replacement for the asset that is selected on the selected maintenance request.</span></span> |
| <span data-ttu-id="435f5-149">ส่งคืนสินทรัพย์ที่ให้ยืม</span><span class="sxs-lookup"><span data-stu-id="435f5-149">Return loan asset</span></span>                | <span data-ttu-id="435f5-150">ลงทะเบียนสินทรัพย์ที่ให้ยืมเป็นส่งคืนแล้ว</span><span class="sxs-lookup"><span data-stu-id="435f5-150">Register the loan asset as returned.</span></span> |

