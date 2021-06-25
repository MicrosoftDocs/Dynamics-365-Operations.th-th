---
title: คุณไม่สามารถยืนยันการจัดส่งได้ เนื่องจากงานที่ไม่สมบูรณ์หรือขาดหายไป
description: คุณไม่สามารถยืนยันการจัดส่งได้ เนื่องจากงานที่ไม่สมบูรณ์หรือขาดหายไป
author: perlynne
ms.date: 04/21/2021
ms.topic: troubleshooting
ms.search.form: WHSLoadTable_WHSShipConfirm,WHSLoadPlanningListPage_WHSShipConfirm,WHSLoadPlanningWorkbench_WHSShipConfirm,WHSTransportLoad_WHSShipConfirm,WHSShipPlanningListPage_WHSShipConfirm,WHSShipmentDetails_WHSShipConfirm,WHSWorkTable_WHSShipConfirm,WHSWorkTableListPage_WHSShipConfirm,Dialog_WHSOutboundShipConfirmController_WHSOutboundShipConfirm, WHSContainerCloseDiag_WHSShipConfirm
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: lbc
ms.search.validFrom: 2021-04-21
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: beef0909d41e69f3e7bcc1021527be35b7e6fd44
ms.sourcegitcommit: c2c6d687a89bc1534c029109315c23e92865b63b
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 05/31/2021
ms.locfileid: "6123854"
---
# <a name="you-cant-confirm-a-shipment-because-of-incomplete-or-missing-work"></a><span data-ttu-id="37ee7-103">คุณไม่สามารถยืนยันการจัดส่งได้ เนื่องจากงานที่ไม่สมบูรณ์หรือขาดหายไป</span><span class="sxs-lookup"><span data-stu-id="37ee7-103">You can't confirm a shipment because of incomplete or missing work</span></span>

<span data-ttu-id="37ee7-104">รหัสข้อผิดพลาด: WAX515</span><span class="sxs-lookup"><span data-stu-id="37ee7-104">Error code: WAX515</span></span>

## <a name="symptoms"></a><span data-ttu-id="37ee7-105">อาการ</span><span class="sxs-lookup"><span data-stu-id="37ee7-105">Symptoms</span></span>

<span data-ttu-id="37ee7-106">เมื่อคุณพยายามยืนยันการจัดส่ง ระบบจะแสดงข้อความแสดงข้อผิดพลาดต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="37ee7-106">When you try to confirm a shipment, the system shows the following error message:</span></span>

> <span data-ttu-id="37ee7-107">การจัดส่งสำหรับจำนวนงานในศูนย์การผลิต %1 ไม่สามารถยืนยันได้เนื่องจากงานทั้งหมดสำหรับจำนวนงานในศูนย์การผลิตต้องเสร็จสมบูรณ์</span><span class="sxs-lookup"><span data-stu-id="37ee7-107">The shipment for load %1 could not be confirmed because all work for the load must be complete.</span></span>

<span data-ttu-id="37ee7-108">ดังนั้นคุณจึงไม่สามารถยืนยันการจัดส่งของสินค้าได้</span><span class="sxs-lookup"><span data-stu-id="37ee7-108">Therefore, you can't confirm the shipment for the load.</span></span>

## <a name="cause"></a><span data-ttu-id="37ee7-109">สาเหตุ</span><span class="sxs-lookup"><span data-stu-id="37ee7-109">Cause</span></span>

<span data-ttu-id="37ee7-110">สินค้าหรือการจัดส่งอยู่ในสถานะที่การยืนยันการจัดส่งล้มเหลว</span><span class="sxs-lookup"><span data-stu-id="37ee7-110">The load or shipment is currently in a state where shipment confirmation fails.</span></span> <span data-ttu-id="37ee7-111">ก่อนที่คุณจะสามารถยืนยันการจัดส่งได้ อย่างน้อยต้องมีงานบางอย่างอยู่ให้กับปริมาณงาน และงานทั้งหมดต้องมีสถานะเป็น *ปิด* หรือ *ยกเลิก*</span><span class="sxs-lookup"><span data-stu-id="37ee7-111">Before you can confirm the shipment, at least some work must exist for the load, and all that work must have a status of *Closed* or *Canceled*.</span></span>

## <a name="resolution"></a><span data-ttu-id="37ee7-112">ความละเอียด</span><span class="sxs-lookup"><span data-stu-id="37ee7-112">Resolution</span></span>

<span data-ttu-id="37ee7-113">ตรวจสอบใบสั่งขายหรือใบสั่งโอนย้ายที่เกี่ยวข้องสำหรับสินค้าหรือการจัดส่ง และตรวจสอบให้แน่ใจว่างานที่เกี่ยวข้องทั้งหมดเสร็จสมบูรณ์แล้วหรือยกเลิกแล้ว</span><span class="sxs-lookup"><span data-stu-id="37ee7-113">Check the related sales orders or transfer orders for the load or shipment, and make sure that all the related work has been completed or canceled.</span></span>

<span data-ttu-id="37ee7-114">คุณสามารถใช้งานการจัดส่งและสินค้าบนหน้าหลายหน้าได้</span><span class="sxs-lookup"><span data-stu-id="37ee7-114">You can work with shipments and loads on several pages.</span></span> <span data-ttu-id="37ee7-115">ส่วนย่อยต่อไปนี้แสดงตัวอย่าง</span><span class="sxs-lookup"><span data-stu-id="37ee7-115">The following subsections provide a few examples.</span></span>

### <a name="all-loads-page"></a><span data-ttu-id="37ee7-116">หน้าสินค้าทั้งหมด</span><span class="sxs-lookup"><span data-stu-id="37ee7-116">All loads page</span></span>

1. <span data-ttu-id="37ee7-117">ไปที่ **การจัดการคลังสินค้า \> จำนวนงานในศูนย์การผลิต \> จำนวนงานในศูนย์การผลิตทั้งหมด**</span><span class="sxs-lookup"><span data-stu-id="37ee7-117">Go to **Warehouse management \> Loads \> All loads**.</span></span>
1. <span data-ttu-id="37ee7-118">เลือกสินค้าที่การจัดส่งไม่สามารถยืนยันได้</span><span class="sxs-lookup"><span data-stu-id="37ee7-118">Select the load that the shipment can't be confirmed for.</span></span>
1. <span data-ttu-id="37ee7-119">บนบานหน้าต่างการดำเนินการ บนแท็บ **สินค้า** ในกลุ่ม **ข้อมูลที่เกี่ยวข้อง** ให้เลือก **งาน**</span><span class="sxs-lookup"><span data-stu-id="37ee7-119">On the Action Pane, on the **Loads** tab, in the **Related information** group, select **Work**.</span></span>
1. <span data-ttu-id="37ee7-120">ตรวจสอบสถานะของรหัสงานแต่ละรหัส</span><span class="sxs-lookup"><span data-stu-id="37ee7-120">Inspect the status of each work ID.</span></span> <span data-ttu-id="37ee7-121">ติดตามแต่ละรหัสงานที่ไม่มีสถานะเป็น *ปิด* หรือ *ยกเลิก*</span><span class="sxs-lookup"><span data-stu-id="37ee7-121">Follow up on each work ID that doesn't have a status of *Closed* or *Canceled*.</span></span>
1. <span data-ttu-id="37ee7-122">เมื่อรหัสงานทุกรายการมีสถานะ *ปิด* หรือ *ยกเลิก* แล้วลองอีกครั้งเพื่อยืนยันการจัดส่ง</span><span class="sxs-lookup"><span data-stu-id="37ee7-122">When every work ID has a status of *Closed* or *Canceled*, try again to confirm the shipment.</span></span>

### <a name="all-shipments-page"></a><span data-ttu-id="37ee7-123">หน้าการจัดส่งทั้งหมด</span><span class="sxs-lookup"><span data-stu-id="37ee7-123">All shipments page</span></span>

1. <span data-ttu-id="37ee7-124">ไปที่ **การจัดการคลังสินค้า \> การจัดส่ง \> การจัดส่งทั้งหมด**</span><span class="sxs-lookup"><span data-stu-id="37ee7-124">Go to **Warehouse management \> Shipments\> All shipments**.</span></span>
1. <span data-ttu-id="37ee7-125">เลือกการจัดส่งที่ไม่สามารถยืนยันได้</span><span class="sxs-lookup"><span data-stu-id="37ee7-125">Select the shipment that can't be confirmed.</span></span>
1. <span data-ttu-id="37ee7-126">บนบานหน้าต่างการดำเนินการ ในแท็บ **การจัดส่ง** ในกลุ่ม **งาน** เลือก **รายละเอียดงาน**</span><span class="sxs-lookup"><span data-stu-id="37ee7-126">On the Action Pane, on the **Shipments** tab, in the **Work** group, select **Work details**.</span></span>
1. <span data-ttu-id="37ee7-127">ตรวจสอบสถานะของรหัสงานแต่ละรหัส</span><span class="sxs-lookup"><span data-stu-id="37ee7-127">Inspect the status of each work ID.</span></span> <span data-ttu-id="37ee7-128">ติดตามแต่ละรหัสงานที่ไม่มีสถานะเป็น *ปิด* หรือ *ยกเลิก*</span><span class="sxs-lookup"><span data-stu-id="37ee7-128">Follow up on each work ID that doesn't have a status of *Closed* or *Canceled*.</span></span>
1. <span data-ttu-id="37ee7-129">เมื่อรหัสงานทุกรายการมีสถานะ *ปิด* หรือ *ยกเลิก* แล้วลองอีกครั้งเพื่อยืนยันการจัดส่ง</span><span class="sxs-lookup"><span data-stu-id="37ee7-129">When every work ID has a status of *Closed* or *Canceled*, try again to confirm the shipment.</span></span>

### <a name="all-work-page"></a><span data-ttu-id="37ee7-130">หน้างานทั้งหมด</span><span class="sxs-lookup"><span data-stu-id="37ee7-130">All work page</span></span>

1. <span data-ttu-id="37ee7-131">ไปที่ **การจัดการคลังสินค้า \> งาน \> งานทั้งหมด**</span><span class="sxs-lookup"><span data-stu-id="37ee7-131">Go to **Warehouse management \> Work\> All work**.</span></span>
1. <span data-ttu-id="37ee7-132">เลือกงานให้กับหมายเลขใบสั่งที่การจัดส่งไม่สามารถยืนยันได้</span><span class="sxs-lookup"><span data-stu-id="37ee7-132">Select the work for the order number that the shipment can't be confirmed for.</span></span>
1. <span data-ttu-id="37ee7-133">บนบานหน้าต่างการดำเนินการ บนแท็บ **การจัดส่ง** ในกลุ่ม **การจัดส่ง** เลือก **ยืนยันการจัดส่ง**</span><span class="sxs-lookup"><span data-stu-id="37ee7-133">On the Action Pane, on the **Shipment** tab, in the **Shipment** group, select **Confirm shipment**.</span></span>
1. <span data-ttu-id="37ee7-134">ตรวจสอบสถานะของรหัสงานแต่ละรหัส</span><span class="sxs-lookup"><span data-stu-id="37ee7-134">Inspect the status of each work ID.</span></span> <span data-ttu-id="37ee7-135">ติดตามแต่ละรหัสงานที่ไม่มีสถานะเป็น *ปิด* หรือ *ยกเลิก*</span><span class="sxs-lookup"><span data-stu-id="37ee7-135">Follow up on each work ID that doesn't have a status of *Closed* or *Canceled*.</span></span>
1. <span data-ttu-id="37ee7-136">เมื่อรหัสงานทุกรายการมีสถานะ *ปิด* หรือ *ยกเลิก* แล้วลองอีกครั้งเพื่อยืนยันการจัดส่ง</span><span class="sxs-lookup"><span data-stu-id="37ee7-136">When every work ID has a status of *Closed* or *Canceled*, try again to confirm the shipment.</span></span>
