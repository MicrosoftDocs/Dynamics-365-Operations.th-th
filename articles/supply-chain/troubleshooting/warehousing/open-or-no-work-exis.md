---
title: คุณไม่สามารถยืนยันการจัดส่งได้ เนื่องจากงานที่ไม่สมบูรณ์หรือขาดหายไป
description: คุณไม่สามารถยืนยันการจัดส่งได้ เนื่องจากงานที่ไม่สมบูรณ์หรือขาดหายไป
author: perlynne
ms.date: 04/21/2021
ms.topic: troubleshooting
ms.search.form: WHSLoadTable_WHSShipConfirm,WHSLoadPlanningListPage_WHSShipConfirm,WHSLoadPlanningWorkbench_WHSShipConfirm,WHSTransportLoad_WHSShipConfirm,WHSShipPlanningListPage_WHSShipConfirm,WHSShipmentDetails_WHSShipConfirm,WHSWorkTable_WHSShipConfirm,WHSWorkTableListPage_WHSShipConfirm,Dialog_WHSOutboundShipConfirmController_WHSOutboundShipConfirm
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: lbc
ms.search.validFrom: 2021-04-21
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: da6388d433d6021a99840ae9781c717db1b540a9
ms.sourcegitcommit: cd9016e9787169cb800889d335b9c5919ddbe4af
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 04/23/2021
ms.locfileid: "5938561"
---
# <a name="you-cant-confirm-a-shipment-because-of-incomplete-or-missing-work"></a><span data-ttu-id="d8261-103">คุณไม่สามารถยืนยันการจัดส่งได้ เนื่องจากงานที่ไม่สมบูรณ์หรือขาดหายไป</span><span class="sxs-lookup"><span data-stu-id="d8261-103">You can't confirm a shipment because of incomplete or missing work</span></span>

<span data-ttu-id="d8261-104">รหัสข้อผิดพลาด: WAX515</span><span class="sxs-lookup"><span data-stu-id="d8261-104">Error code: WAX515</span></span>

## <a name="symptoms"></a><span data-ttu-id="d8261-105">อาการ</span><span class="sxs-lookup"><span data-stu-id="d8261-105">Symptoms</span></span>

<span data-ttu-id="d8261-106">เมื่อคุณพยายามยืนยันการจัดส่ง ระบบจะแสดงข้อความแสดงข้อผิดพลาดต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="d8261-106">When you try to confirm a shipment, the system shows the following error message:</span></span>

> <span data-ttu-id="d8261-107">การจัดส่งสำหรับจำนวนงานในศูนย์การผลิต %1 ไม่สามารถยืนยันได้เนื่องจากงานทั้งหมดสำหรับจำนวนงานในศูนย์การผลิตต้องเสร็จสมบูรณ์</span><span class="sxs-lookup"><span data-stu-id="d8261-107">The shipment for load %1 could not be confirmed because all work for the load must be complete.</span></span>

<span data-ttu-id="d8261-108">ดังนั้นคุณจึงไม่สามารถยืนยันการจัดส่งของสินค้าได้</span><span class="sxs-lookup"><span data-stu-id="d8261-108">Therefore, you can't confirm the shipment for the load.</span></span>

## <a name="cause"></a><span data-ttu-id="d8261-109">สาเหตุ</span><span class="sxs-lookup"><span data-stu-id="d8261-109">Cause</span></span>

<span data-ttu-id="d8261-110">สินค้าหรือการจัดส่งอยู่ในสถานะที่การยืนยันการจัดส่งล้มเหลว</span><span class="sxs-lookup"><span data-stu-id="d8261-110">The load or shipment is currently in a state where shipment confirmation fails.</span></span> <span data-ttu-id="d8261-111">ก่อนที่คุณจะสามารถยืนยันการจัดส่งได้ อย่างน้อยต้องมีงานบางอย่างอยู่ให้กับปริมาณงาน และงานทั้งหมดต้องมีสถานะเป็น *ปิด* หรือ *ยกเลิก*</span><span class="sxs-lookup"><span data-stu-id="d8261-111">Before you can confirm the shipment, at least some work must exist for the load, and all that work must have a status of *Closed* or *Canceled*.</span></span>

## <a name="resolution"></a><span data-ttu-id="d8261-112">ความละเอียด</span><span class="sxs-lookup"><span data-stu-id="d8261-112">Resolution</span></span>

<span data-ttu-id="d8261-113">ตรวจสอบใบสั่งขายหรือใบสั่งโอนย้ายที่เกี่ยวข้องสำหรับสินค้าหรือการจัดส่ง และตรวจสอบให้แน่ใจว่างานที่เกี่ยวข้องทั้งหมดเสร็จสมบูรณ์แล้วหรือยกเลิกแล้ว</span><span class="sxs-lookup"><span data-stu-id="d8261-113">Check the related sales orders or transfer orders for the load or shipment, and make sure that all the related work has been completed or canceled.</span></span>

<span data-ttu-id="d8261-114">คุณสามารถใช้งานการจัดส่งและสินค้าบนหน้าหลายหน้าได้</span><span class="sxs-lookup"><span data-stu-id="d8261-114">You can work with shipments and loads on several pages.</span></span> <span data-ttu-id="d8261-115">ส่วนย่อยต่อไปนี้แสดงตัวอย่าง</span><span class="sxs-lookup"><span data-stu-id="d8261-115">The following subsections provide a few examples.</span></span>

### <a name="all-loads-page"></a><span data-ttu-id="d8261-116">หน้าสินค้าทั้งหมด</span><span class="sxs-lookup"><span data-stu-id="d8261-116">All loads page</span></span>

1. <span data-ttu-id="d8261-117">ไปที่ **การจัดการคลังสินค้า \> จำนวนงานในศูนย์การผลิต \> จำนวนงานในศูนย์การผลิตทั้งหมด**</span><span class="sxs-lookup"><span data-stu-id="d8261-117">Go to **Warehouse management \> Loads \> All loads**.</span></span>
1. <span data-ttu-id="d8261-118">เลือกสินค้าที่การจัดส่งไม่สามารถยืนยันได้</span><span class="sxs-lookup"><span data-stu-id="d8261-118">Select the load that the shipment can't be confirmed for.</span></span>
1. <span data-ttu-id="d8261-119">บนบานหน้าต่างการดำเนินการ บนแท็บ **สินค้า** ในกลุ่ม **ข้อมูลที่เกี่ยวข้อง** ให้เลือก **งาน**</span><span class="sxs-lookup"><span data-stu-id="d8261-119">On the Action Pane, on the **Loads** tab, in the **Related information** group, select **Work**.</span></span>
1. <span data-ttu-id="d8261-120">ตรวจสอบสถานะของรหัสงานแต่ละรหัส</span><span class="sxs-lookup"><span data-stu-id="d8261-120">Inspect the status of each work ID.</span></span> <span data-ttu-id="d8261-121">ติดตามแต่ละรหัสงานที่ไม่มีสถานะเป็น *ปิด* หรือ *ยกเลิก*</span><span class="sxs-lookup"><span data-stu-id="d8261-121">Follow up on each work ID that doesn't have a status of *Closed* or *Canceled*.</span></span>
1. <span data-ttu-id="d8261-122">เมื่อรหัสงานทุกรายการมีสถานะ *ปิด* หรือ *ยกเลิก* แล้วลองอีกครั้งเพื่อยืนยันการจัดส่ง</span><span class="sxs-lookup"><span data-stu-id="d8261-122">When every work ID has a status of *Closed* or *Canceled*, try again to confirm the shipment.</span></span>

### <a name="all-shipments-page"></a><span data-ttu-id="d8261-123">หน้าการจัดส่งทั้งหมด</span><span class="sxs-lookup"><span data-stu-id="d8261-123">All shipments page</span></span>

1. <span data-ttu-id="d8261-124">ไปที่ **การจัดการคลังสินค้า \> การจัดส่ง \> การจัดส่งทั้งหมด**</span><span class="sxs-lookup"><span data-stu-id="d8261-124">Go to **Warehouse management \> Shipments\> All shipments**.</span></span>
1. <span data-ttu-id="d8261-125">เลือกการจัดส่งที่ไม่สามารถยืนยันได้</span><span class="sxs-lookup"><span data-stu-id="d8261-125">Select the shipment that can't be confirmed.</span></span>
1. <span data-ttu-id="d8261-126">บนบานหน้าต่างการดำเนินการ ในแท็บ **การจัดส่ง** ในกลุ่ม **งาน** เลือก **รายละเอียดงาน**</span><span class="sxs-lookup"><span data-stu-id="d8261-126">On the Action Pane, on the **Shipments** tab, in the **Work** group, select **Work details**.</span></span>
1. <span data-ttu-id="d8261-127">ตรวจสอบสถานะของรหัสงานแต่ละรหัส</span><span class="sxs-lookup"><span data-stu-id="d8261-127">Inspect the status of each work ID.</span></span> <span data-ttu-id="d8261-128">ติดตามแต่ละรหัสงานที่ไม่มีสถานะเป็น *ปิด* หรือ *ยกเลิก*</span><span class="sxs-lookup"><span data-stu-id="d8261-128">Follow up on each work ID that doesn't have a status of *Closed* or *Canceled*.</span></span>
1. <span data-ttu-id="d8261-129">เมื่อรหัสงานทุกรายการมีสถานะ *ปิด* หรือ *ยกเลิก* แล้วลองอีกครั้งเพื่อยืนยันการจัดส่ง</span><span class="sxs-lookup"><span data-stu-id="d8261-129">When every work ID has a status of *Closed* or *Canceled*, try again to confirm the shipment.</span></span>

### <a name="all-work-page"></a><span data-ttu-id="d8261-130">หน้างานทั้งหมด</span><span class="sxs-lookup"><span data-stu-id="d8261-130">All work page</span></span>

1. <span data-ttu-id="d8261-131">ไปที่ **การจัดการคลังสินค้า \> งาน \> งานทั้งหมด**</span><span class="sxs-lookup"><span data-stu-id="d8261-131">Go to **Warehouse management \> Work\> All work**.</span></span>
1. <span data-ttu-id="d8261-132">เลือกงานให้กับหมายเลขใบสั่งที่การจัดส่งไม่สามารถยืนยันได้</span><span class="sxs-lookup"><span data-stu-id="d8261-132">Select the work for the order number that the shipment can't be confirmed for.</span></span>
1. <span data-ttu-id="d8261-133">บนบานหน้าต่างการดำเนินการ บนแท็บ **การจัดส่ง** ในกลุ่ม **การจัดส่ง** เลือก **ยืนยันการจัดส่ง**</span><span class="sxs-lookup"><span data-stu-id="d8261-133">On the Action Pane, on the **Shipment** tab, in the **Shipment** group, select **Confirm shipment**.</span></span>
1. <span data-ttu-id="d8261-134">ตรวจสอบสถานะของรหัสงานแต่ละรหัส</span><span class="sxs-lookup"><span data-stu-id="d8261-134">Inspect the status of each work ID.</span></span> <span data-ttu-id="d8261-135">ติดตามแต่ละรหัสงานที่ไม่มีสถานะเป็น *ปิด* หรือ *ยกเลิก*</span><span class="sxs-lookup"><span data-stu-id="d8261-135">Follow up on each work ID that doesn't have a status of *Closed* or *Canceled*.</span></span>
1. <span data-ttu-id="d8261-136">เมื่อรหัสงานทุกรายการมีสถานะ *ปิด* หรือ *ยกเลิก* แล้วลองอีกครั้งเพื่อยืนยันการจัดส่ง</span><span class="sxs-lookup"><span data-stu-id="d8261-136">When every work ID has a status of *Closed* or *Canceled*, try again to confirm the shipment.</span></span>
