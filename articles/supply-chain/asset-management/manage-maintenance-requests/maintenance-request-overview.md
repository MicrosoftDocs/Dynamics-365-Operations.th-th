---
title: คำขอการบำรุงรักษา
description: หัวข้อนี้แสดงภาพรวมเกี่ยวกับการจัดการคำขอการบำรุงรักษาในการจัดการสินทรัพย์
author: johanhoffmann
ms.date: 10/01/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: EntAssetRequestTable, EntAssetRequestWorkspace, EntAssetRequestActivePart, EntAssetRequestWorkOrderActive, EntAssetRequestType, EntAssetRequestTableCreateWO, EntAssetRequestTableLookup, EntAssetRequestTableActivePart, EntAssetMobileRequestDetails
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 3c72a16b8f3865129ad737c511e50eb34c9f2e91
ms.sourcegitcommit: 51cad1ce3ed44ebf7eb9bdf553ee2df4c1f03135
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 05/10/2021
ms.locfileid: "6015889"
---
# <a name="maintenance-requests"></a><span data-ttu-id="1a131-103">คำขอการบำรุงรักษา</span><span class="sxs-lookup"><span data-stu-id="1a131-103">Maintenance requests</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="1a131-104">คำขอการบำรุงรักษาเป็นบันทึกย่อหรือการรายงานที่สร้างขึ้นเพื่อแจ้งให้ผู้จัดการหรือผู้วางแผนทราบว่า สินทรัพย์อาจต้องการการบำรุงรักษาหรืองานซ่อมแซม แต่ไม่มีการสร้างใบสั่งงาน</span><span class="sxs-lookup"><span data-stu-id="1a131-104">Maintenance requests are notes or declarations that are created to notify a manager or planner that an asset might require a maintenance or repair job, but without creating a work order.</span></span> <span data-ttu-id="1a131-105">ถ้าเนื้อหาของคำขอการบำรุงรักษาถูกพิจารณาแล้วว่าถูกต้อง จากนั้น จะสามารถสร้างใบสั่งงานตามคำขอการบำรุงรักษาได้</span><span class="sxs-lookup"><span data-stu-id="1a131-105">If the contents of a maintenance request are considered valid, a work order can then be created based on the maintenance request.</span></span>

<span data-ttu-id="1a131-106">สามารถสร้างคำขอการบำรุงรักษาสำหรับสินทรัพย์ใดๆ ในการจัดการสินทรัพย์ได้</span><span class="sxs-lookup"><span data-stu-id="1a131-106">Maintenance requests can be created for any asset in Asset Management.</span></span> <span data-ttu-id="1a131-107">สามารถสร้างคำขอการบำรุงรักษาชนิดต่างๆ ได้ โดยขึ้นอยู่กับวิธีที่บริษัทของคุณใช้คำขอการบำรุงรักษา</span><span class="sxs-lookup"><span data-stu-id="1a131-107">Various types of maintenance requests can be created, depending on how your company uses maintenance requests.</span></span> <span data-ttu-id="1a131-108">ยกตัวอย่างเช่น</span><span class="sxs-lookup"><span data-stu-id="1a131-108">Here are some examples:</span></span>

- <span data-ttu-id="1a131-109">คำขอการบำรุงรักษา</span><span class="sxs-lookup"><span data-stu-id="1a131-109">Maintenance requests</span></span>
- <span data-ttu-id="1a131-110">บันทึกย่อ</span><span class="sxs-lookup"><span data-stu-id="1a131-110">Notes</span></span>
- <span data-ttu-id="1a131-111">การแก้ไขหรือการปรับปรุง</span><span class="sxs-lookup"><span data-stu-id="1a131-111">Corrections or enhancements</span></span>
- <span data-ttu-id="1a131-112">เงินลงทุน</span><span class="sxs-lookup"><span data-stu-id="1a131-112">Investments</span></span>
- <span data-ttu-id="1a131-113">การซ่อมแซมคลัง (ชนิดนี้จะใช้เมื่อคุณได้รับสินทรัพย์จากสถานที่อื่น เพื่อให้คุณสามารถทำงานการบำรุงรักษาหรือซ่อมแซม และจากนั้น คุณส่งคืนสินทรัพย์หลังจากที่งานเสร็จสมบูรณ์)</span><span class="sxs-lookup"><span data-stu-id="1a131-113">Depot repair (This type is used when you receive assets from another location so that you can do a maintenance or repair job, and you then return the asset after the job is completed.)</span></span>

## <a name="view-maintenance-requests"></a><span data-ttu-id="1a131-114">ดูคำขอการบำรุงรักษา</span><span class="sxs-lookup"><span data-stu-id="1a131-114">View maintenance requests</span></span>

<span data-ttu-id="1a131-115">หากต้องการดูคำขอการบำรุงรักษา เลือก **การจัดการสินทรัพย์** \> **ทั่วไป** \> **คำขอการบำรุงรักษา** \> **คำขอการบำรุงรักษาทั้งหมด** **คำขอการบำรุงรักษาที่ใช้งานอยู่** หรือ **คำขอการบำรุงรักษาของตำแหน่งที่ทำงานของฉัน**</span><span class="sxs-lookup"><span data-stu-id="1a131-115">To view maintenance requests, select **Asset management** \> **Common** \> **Maintenance requests** \> **All maintenance requests**, **Active maintenance requests**, or **My functional location maintenance requests**.</span></span> <span data-ttu-id="1a131-116">หน้ารายการแต่ละหน้าจะแสดงข้อมูลบางอย่างที่เกี่ยวข้องกับคำขอการบำรุงรักษา</span><span class="sxs-lookup"><span data-stu-id="1a131-116">Each list page shows some of the information that is related to a maintenance request.</span></span>

![ดูคำขอการบำรุงรักษา](media/01-manage-maintenance-requests.png)

> [!NOTE]
> <span data-ttu-id="1a131-118">ใช้หน้ารายการ **คำขอการบำรุงรักษาของตำแหน่งที่ทำงานของฉัน** เพื่อดูรายการของคำขอการบำรุงรักษาที่ประกอบด้วยตำแหน่งที่ทำงานที่คุณเกี่ยวข้องในฐานะผู้ปฏิบัติงาน หรือสินทรัพย์ที่ถูกติดตั้งในตำแหน่งที่ทำงานที่คุณเกี่ยวข้องในฐานะผู้ปฏิบัติงาน</span><span class="sxs-lookup"><span data-stu-id="1a131-118">Use the **My functional location maintenance requests** list page to view a list of maintenance requests that contain either functional locations that you're related to as a worker or assets that are installed on functional locations that you're related to as a worker.</span></span> <span data-ttu-id="1a131-119">(สำหรับข้อมูลเกี่ยวกับวิธีการตั้งค่าตำแหน่งที่ทำงานในเจ้าหน้าที่บำรุงรักษา ดู [เจ้าหน้าที่บำรุงรักษาและกลุ่มผู้ปฏิบัติงาน](../setup-for-objects/workers-and-worker-groups.md))</span><span class="sxs-lookup"><span data-stu-id="1a131-119">(For information about how to set up functional locations on maintenance workers, see [Maintenance workers and worker groups](../setup-for-objects/workers-and-worker-groups.md).)</span></span>
> 
> <span data-ttu-id="1a131-120">แม้ว่าข้อมูลบัญชีลูกค้าจะพร้อมใช้งานในการจัดการบริการสินทรัพย์ (การบำรุงรักษาภายนอก) แต่จะไม่พร้อมใช้งานในการจัดการสินทรัพย์ (การบำรุงรักษาภายใน)</span><span class="sxs-lookup"><span data-stu-id="1a131-120">Although customer account information is available in Asset Service Management (external maintenance), it isn't available in Asset Management (internal maintenance).</span></span>

<span data-ttu-id="1a131-121">เมื่อต้องการเปิดมุมมองรายละเอียดของเรกคอร์ดบนหน้ารายการ **คำขอการบำรุงรักษาทั้งหมด** ในมุมมองกริด ให้เลือกลิงค์ในคอลัมน์ **คำขอการบำรุงรักษา**</span><span class="sxs-lookup"><span data-stu-id="1a131-121">To open the details view of a record, on the **All maintenance requests** list page, in the grid view, select a link in the **Maintenance request** column.</span></span>

![ดูรายละเอียดของคำขอการบำรุงรักษา](media/02-manage-maintenance-requests.png)

<span data-ttu-id="1a131-123">ปุ่มบนบานหน้าต่างการดำเนินการจะถูกจัดระเบียบบนแท็บ</span><span class="sxs-lookup"><span data-stu-id="1a131-123">The buttons on the Action Pane are organized on tabs.</span></span> <span data-ttu-id="1a131-124">ตารางต่อไปนี้จะอธิบายถึงปุ่มที่เกี่ยวข้องกับการจัดการสินทรัพย์อย่างคร่าวๆ</span><span class="sxs-lookup"><span data-stu-id="1a131-124">The following table briefly describes the buttons that are related to Asset Management.</span></span>

| <span data-ttu-id="1a131-125">ชื่อปุ่ม</span><span class="sxs-lookup"><span data-stu-id="1a131-125">Button name</span></span>                      | <span data-ttu-id="1a131-126">คำอธิบาย</span><span class="sxs-lookup"><span data-stu-id="1a131-126">Description</span></span> |
|----------------------------------|-------------|
| <span data-ttu-id="1a131-127">แก้ไข</span><span class="sxs-lookup"><span data-stu-id="1a131-127">Edit</span></span>                             | <span data-ttu-id="1a131-128">แก้ไขคำขอการบำรุงรักษาที่เลือก</span><span class="sxs-lookup"><span data-stu-id="1a131-128">Edit the selected maintenance request.</span></span> |
| <span data-ttu-id="1a131-129">สร้าง </span><span class="sxs-lookup"><span data-stu-id="1a131-129">New</span></span>                              | <span data-ttu-id="1a131-130">สร้างคำขอการบำรุงรักษาใหม่</span><span class="sxs-lookup"><span data-stu-id="1a131-130">Create a new maintenance request.</span></span> |
| <span data-ttu-id="1a131-131">ลบ</span><span class="sxs-lookup"><span data-stu-id="1a131-131">Delete</span></span>                           | <span data-ttu-id="1a131-132">ลบคำขอการบำรุงรักษาที่เลือก</span><span class="sxs-lookup"><span data-stu-id="1a131-132">Delete the selected maintenance request.</span></span> |
| <span data-ttu-id="1a131-133">กลุ่มใบสั่งงาน</span><span class="sxs-lookup"><span data-stu-id="1a131-133">Work order pool</span></span>                  | <span data-ttu-id="1a131-134">เชื่อมโยงคำขอการบำรุงรักษาที่เลือกกับกลุ่มใบสั่งงาน</span><span class="sxs-lookup"><span data-stu-id="1a131-134">Connect the selected maintenance request to a work order pool.</span></span> |
| <span data-ttu-id="1a131-135">ใบสั่งงาน</span><span class="sxs-lookup"><span data-stu-id="1a131-135">Work order</span></span>                       | <span data-ttu-id="1a131-136">สร้างใบสั่งงาน ตามคำขอการบำรุงรักษาที่เลือก</span><span class="sxs-lookup"><span data-stu-id="1a131-136">Create a work order, based on the selected maintenance request.</span></span> |
| <span data-ttu-id="1a131-137">ข้อบกพร่องของสินทรัพย์</span><span class="sxs-lookup"><span data-stu-id="1a131-137">Asset fault</span></span>                      | <span data-ttu-id="1a131-138">คลิก **ข้อบกพร่องของสินทรัพย์** ซึ่งคุณสามารถสร้างการลงทะเบียนข้อบกพร่องได้ในคำขอการบำรุงรักษาที่เลือก</span><span class="sxs-lookup"><span data-stu-id="1a131-138">Click **Asset faults**, where you can create a fault registration on the selected maintenance request.</span></span> |
| <span data-ttu-id="1a131-139">ใบสั่งงาน</span><span class="sxs-lookup"><span data-stu-id="1a131-139">Work orders</span></span>                      | <span data-ttu-id="1a131-140">แสดงรายการของใบสั่งงานทั้งหมดที่เชื่อมโยงกับคำขอการบำรุงรักษาที่เลือก</span><span class="sxs-lookup"><span data-stu-id="1a131-140">Show a list of all work orders that are connected to the selected maintenance request.</span></span> |
| <span data-ttu-id="1a131-141">ปรับปรุงสถานะคำขอการบำรุงรักษา</span><span class="sxs-lookup"><span data-stu-id="1a131-141">Update maintenance request state</span></span> | <span data-ttu-id="1a131-142">ปรับปรุงสถานะคำขอการบำรุงรักษา</span><span class="sxs-lookup"><span data-stu-id="1a131-142">Update the maintenance request state.</span></span> |
| <span data-ttu-id="1a131-143">ล็อกสถานะของวงจรการใช้</span><span class="sxs-lookup"><span data-stu-id="1a131-143">Lifecycle state log</span></span>              | <span data-ttu-id="1a131-144">ดูล็อกที่แสดงสถานะของวงจรการใช้ของคำขอการบำรุงรักษาที่เลือก</span><span class="sxs-lookup"><span data-stu-id="1a131-144">View a log that shows the lifecycle states of the selected maintenance request.</span></span> |
| <span data-ttu-id="1a131-145">รายละเอียดคำขอการบำรุงรักษา</span><span class="sxs-lookup"><span data-stu-id="1a131-145">Maintenance request details</span></span>      | <span data-ttu-id="1a131-146">พิมพ์รายงานที่แสดงรายละเอียดของคำขอการบำรุงรักษาที่เลือก</span><span class="sxs-lookup"><span data-stu-id="1a131-146">Print a report that shows details of the selected maintenance request.</span></span> |
| <span data-ttu-id="1a131-147">ส่งสินทรัพย์ที่ให้ยืม</span><span class="sxs-lookup"><span data-stu-id="1a131-147">Send loan asset</span></span>                  | <span data-ttu-id="1a131-148">เลือกสินทรัพย์ที่ให้ยืมที่ควรจะเป็นการแทนที่แบบชั่วคราวสำหรับสินทรัพย์ที่เลือกบนคำขอการบำรุงรักษาที่เลือก</span><span class="sxs-lookup"><span data-stu-id="1a131-148">Select a loan asset that should be a temporary replacement for the asset that is selected on the selected maintenance request.</span></span> |
| <span data-ttu-id="1a131-149">ส่งคืนสินทรัพย์ที่ให้ยืม</span><span class="sxs-lookup"><span data-stu-id="1a131-149">Return loan asset</span></span>                | <span data-ttu-id="1a131-150">ลงทะเบียนสินทรัพย์ที่ให้ยืมเป็นส่งคืนแล้ว</span><span class="sxs-lookup"><span data-stu-id="1a131-150">Register the loan asset as returned.</span></span> |



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]