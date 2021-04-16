---
title: ใบสั่งคลังสินค้าสำหรับ scale unit ของระบบคลาวด์และ Edge
description: หัวข้อนี้มีข้อมูลเกี่ยวกับความสามารถด้านใบสั่งคลังสินค้าที่ใช้เป็นส่วนหนึ่งของปริมาณงานของ scale unit ของคลังสินค้า
author: perlynne
ms.date: 01/14/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WHSWarehouseOrderLine, WHSWarehouseReceiptEntry, PurchTable
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: SCM
ms.author: perlynne
ms.search.validFrom: 2021-01-14
ms.dyn365.ops.version: 10.0.17
ms.openlocfilehash: f2401102ab44f5c24f5cd6f545f30438db0a36cf
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 04/01/2021
ms.locfileid: "5836697"
---
# <a name="warehouse-orders-for-cloud-and-edge-scale-units"></a><span data-ttu-id="ae70b-103">ใบสั่งคลังสินค้าสำหรับ scale unit ของระบบคลาวด์และ Edge</span><span class="sxs-lookup"><span data-stu-id="ae70b-103">Warehouse orders for cloud and edge scale units</span></span>

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

> [!WARNING]
> <span data-ttu-id="ae70b-104">ฟังก์ชันธุรกิจบางอย่างไม่ได้รับการสนับสนุนอย่างเต็มที่ในพรีวิวสำหรับสาธารณะ เมื่อมีการใช้ปริมาณงานของ scale unit</span><span class="sxs-lookup"><span data-stu-id="ae70b-104">Not all business functionality is fully supported in the public preview when scale unit workloads are used.</span></span> <span data-ttu-id="ae70b-105">ถ้าคุณกำลังใช้ scale unit ตรวจสอบให้แน่ใจว่าได้ใช้เฉพาะกระบวนการเหล่านั้นที่หัวข้อนี้อธิบายไว้อย่างชัดแจ้งว่าได้รับการสนับสนุน</span><span class="sxs-lookup"><span data-stu-id="ae70b-105">If you're using scale units, be sure to use only those processes that this topic explicitly describes as supported.</span></span>

## <a name="what-are-warehouse-orders"></a><span data-ttu-id="ae70b-106">ใบสั่งของคลังสินค้าคืออะไร</span><span class="sxs-lookup"><span data-stu-id="ae70b-106">What are warehouse orders?</span></span>

<span data-ttu-id="ae70b-107">*ใบสั่งของคลังสินค้า* เป็นชนิดของใบสั่งที่สร้างขึ้นเพื่อสนับสนุนการปรับใช้คลังสินค้าของฮับและ scale unit</span><span class="sxs-lookup"><span data-stu-id="ae70b-107">*Warehouse orders* are a type of order that was created to support hub and scale unit warehouse deployments.</span></span> <span data-ttu-id="ae70b-108">ซึ่งช่วยให้คุณสามารถรับสินค้าคงคลัง เมื่อคุณรันปริมาณงานของคลังสินค้าบน scale unit</span><span class="sxs-lookup"><span data-stu-id="ae70b-108">They let you receive inventory when you're running a warehouse workload on a scale unit.</span></span> <span data-ttu-id="ae70b-109">ซึ่งในปัจจุบันจะใช้กับใบสั่งซื้อเท่านั้น</span><span class="sxs-lookup"><span data-stu-id="ae70b-109">They are currently used only with purchase orders.</span></span>

<span data-ttu-id="ae70b-110">ใบสั่งคลังสินค้าจะถูกใช้เป็นส่วนหนึ่งของการประมวลผลการจัดการคลังสินค้า เช่น เมื่อแอปการจัดการคลังสินค้าบนมือถือถูกใช้เพื่อลงทะเบียนปริมาณคงคลังคงเหลือทางกายภาพ ในระหว่างการประมวลผลใบสั่งซื้อขาเข้า</span><span class="sxs-lookup"><span data-stu-id="ae70b-110">Warehouse orders are used as part of warehouse management processing, such as when the Warehouse Management mobile app is used to register physical on-hand inventory during processing of an inbound purchase order.</span></span> <span data-ttu-id="ae70b-111">ใบสั่งของคลังสินค้าถูกสร้างขึ้นเป็นส่วนหนึ่งของกระบวนการ *นำออกใช้ไปยังคลังสินค้า* ซึ่งพร้อมใช้งานสำหรับใบสั่งซื้อที่ระบุคลังสินค้า scale unit และสินค้าที่ถูกเปิดใช้งานเพื่อใช้กระบวนการจัดการคลังสินค้า</span><span class="sxs-lookup"><span data-stu-id="ae70b-111">Warehouse orders are created as part of the *Release to warehouse* process that is available for purchase orders that specify a scale unit warehouse and items that are enabled to use warehouse management processes.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="ae70b-112">ใบสั่งคลังสินค้าพร้อมใช้งานเฉพาะในการปรับใช้งานที่ใช้ [ปริมาณงานการจัดการคลังสินค้าสำหรับ scale unit ของระบบคลาวด์และ Edge](cloud-edge-workload-warehousing.md)</span><span class="sxs-lookup"><span data-stu-id="ae70b-112">Warehouse orders are available only in deployments that use [warehouse management workloads for cloud and edge scale units](cloud-edge-workload-warehousing.md).</span></span>

## <a name="create-a-warehouse-order"></a><span data-ttu-id="ae70b-113">สร้างใบสั่งของคลังสินค้า</span><span class="sxs-lookup"><span data-stu-id="ae70b-113">Create a warehouse order</span></span>

<span data-ttu-id="ae70b-114">ในการสร้างใบสั่งของคลังสินค้า ให้ปฏิบัติดังนี้</span><span class="sxs-lookup"><span data-stu-id="ae70b-114">To create a warehouse order, follow these steps.</span></span>

1. <span data-ttu-id="ae70b-115">ลงชื่อเข้าใช้อินสแตนซ์ของ Microsoft Dynamics 365 Supply Chain Management ซึ่งกำลังรันบนฮับ</span><span class="sxs-lookup"><span data-stu-id="ae70b-115">Sign in to the instance of Microsoft Dynamics 365 Supply Chain Management that is running on the hub.</span></span> <span data-ttu-id="ae70b-116">(คุณต้องเริ่มต้นกระบวนการ *นำออกใช้ไปยังคลังสินค้า* ในขณะที่คุณลงชื่อเข้าใช้บนฮับ)</span><span class="sxs-lookup"><span data-stu-id="ae70b-116">(You must initiate the *Release to warehouse* process while you're signed in on the hub.)</span></span>
1. <span data-ttu-id="ae70b-117">ไปที่ **การจัดซื้อและการจัดหา \> ใบสั่งซื้อ \> ใบสั่งซื้อทั้งหมด**</span><span class="sxs-lookup"><span data-stu-id="ae70b-117">Go to **Procurement and sourcing \> Purchase orders \> All purchase orders**.</span></span>
1. <span data-ttu-id="ae70b-118">บนบานหน้าต่างการดำเนินการ บนแท็บ **คลังสินค้า** ในกลุ่ม **การดำเนินการ** ให้เลือก **นำออกใช้ไปยังคลังสินค้า**</span><span class="sxs-lookup"><span data-stu-id="ae70b-118">On the Action Pane, on the **Warehouse** tab, in the **Actions** group, select **Release to warehouse**.</span></span>
1. <span data-ttu-id="ae70b-119">เมื่อต้องการดูรายการใบสั่งของคลังสินค้าที่เกี่ยวข้อง ให้เปิดใบสั่งซื้อที่เกี่ยวข้อง เลือกรายการในส่วน **รายการใบสั่งซื้อ** และจากนั้น บนแถบเครื่องมือ ให้เลือก **คลังสินค้า \> รายการใบสั่งของคลังสินค้า**</span><span class="sxs-lookup"><span data-stu-id="ae70b-119">To view the related warehouse order lines, open the relevant purchase order, select a line in the **Purchase order lines** section, and then, on the toolbar, select **Warehouse \> Warehouse order lines**.</span></span> <span data-ttu-id="ae70b-120">เมื่อต้องการดูรายการทั้งหมด ให้ไปที่ **การจัดการคลังสินค้า \> การสอบถามและรายงาน \> รายการใบสั่งของคลังสินค้า**</span><span class="sxs-lookup"><span data-stu-id="ae70b-120">To view all the lines, go to **Warehouse management \> Inquiries and reports \> Warehouse order lines**.</span></span>

<span data-ttu-id="ae70b-121">นอกจากนี้ คุณยังสามารถทริกเกอร์กระบวนการ *นำออกใช้ไปยังคลังสินค้า* จากชุดงานได้โดยไปที่ **การจัดการคลังสินค้า > นำออกใช้ไปยังคลังสินค้า > การนำออกใช้อัตโนมัติของใบสั่งซื้อ**</span><span class="sxs-lookup"><span data-stu-id="ae70b-121">You can also trigger the *Release to warehouse* process from a batch job by going to **Warehouse management > Release to warehouse > Automatic release of purchase orders**.</span></span> <span data-ttu-id="ae70b-122">เมื่อตั้งค่าชุดงาน คุณสามารถเลือกบรรทัดใบสั่งซื้อเฉพาะได้โดยยึดตามการสอบถาม</span><span class="sxs-lookup"><span data-stu-id="ae70b-122">When setting up the batch job, you can select specific purchase order lines based on a query.</span></span> <span data-ttu-id="ae70b-123">สถานการณ์ทั่วไปจะถูกตั้งค่าชุดงานที่เกิดซ้ำ ซึ่งนำออกใช้รายการใบสั่งซื้อที่ยืนยันแล้วทั้งหมดซึ่งคาดว่าจะมาถึงในวันถัดไป</span><span class="sxs-lookup"><span data-stu-id="ae70b-123">A typical scenario would be to set up a recurrent batch job that releases all the confirmed purchase order lines expected to arrive the next day.</span></span>

## <a name="cancel-a-warehouse-order"></a><span data-ttu-id="ae70b-124">ยกเลิกใบสั่งของคลังสินค้า</span><span class="sxs-lookup"><span data-stu-id="ae70b-124">Cancel a warehouse order</span></span>

<span data-ttu-id="ae70b-125">ในฐานะที่เป็นส่วนหนึ่งของกระบวนการ *นำออกใช้ไปยังคลังสินค้า* ธุรกรรมสินค้าคงคลังตามใบสั่งซื้อจะเชื่อมโยงกับใบสั่งของคลังสินค้าและถูกล็อคอยู่จากการอัพเดตโดยฮับ</span><span class="sxs-lookup"><span data-stu-id="ae70b-125">As part of the *Release to warehouse* process, purchase order inventory transactions are linked to warehouse orders and locked from being updated by the hub.</span></span> <span data-ttu-id="ae70b-126">ถ้าคุณนำออกใช้ไปยังคลังสินค้าโดยไม่ได้ตั้งใจ หรือถ้าคุณมีเหตุผลอื่นที่จะกลับการสร้างรายการใบสั่งของคลังสินค้า คุณสามารถร้องขอให้ยกเลิกรายการใบสั่งของคลังสินค้าได้</span><span class="sxs-lookup"><span data-stu-id="ae70b-126">If you released to the warehouse by mistake, or if you have some other reason to reverse the creation of warehouse order lines, you can request to cancel warehouse order lines.</span></span>

<span data-ttu-id="ae70b-127">ในการยกเลิกรายการใบสั่งของคลังสินค้า ให้ปฏิบัติดังนี้</span><span class="sxs-lookup"><span data-stu-id="ae70b-127">To cancel warehouse order lines, follow these steps.</span></span>

1. <span data-ttu-id="ae70b-128">ลงชื่อเข้าใช้อินสแตนซ์ของ Supply Chain Management ซึ่งกำลังรันบนฮับ</span><span class="sxs-lookup"><span data-stu-id="ae70b-128">Sign in to the Supply Chain Management instance that is running on the hub.</span></span>
1. <span data-ttu-id="ae70b-129">ไปที่ **การจัดการคลังสินค้า \> การสอบถามและรายงาน \> รายการใบสั่งของคลังสินค้า**</span><span class="sxs-lookup"><span data-stu-id="ae70b-129">Go to **Warehouse management \> Inquiries and reports \> Warehouse order lines**.</span></span>
1. <span data-ttu-id="ae70b-130">เลือกรายการที่เกี่ยวข้อง</span><span class="sxs-lookup"><span data-stu-id="ae70b-130">Select the relevant line.</span></span>
1. <span data-ttu-id="ae70b-131">ในบานหน้าต่างการดำเนินการ ให้เลือก **ยกเลิกรายการใบสั่งของคลังสินค้า**</span><span class="sxs-lookup"><span data-stu-id="ae70b-131">On the Action Pane, select **Cancel warehouse order lines**.</span></span>

> [!NOTE]
> <span data-ttu-id="ae70b-132">คำขอเพื่อยกเลิกรายการจะถูกปฏิเสธสำหรับรายการใดๆ ที่มีการยกเลิกที่ค้างอยู่หรือที่กำลังประมวลผลที่ใช้งานอยู่ที่คลังสินค้าที่รันปริมาณงานใน scale unit</span><span class="sxs-lookup"><span data-stu-id="ae70b-132">The request to cancel lines will be denied for any lines that are already pending cancellation or that are actively being processed at a warehouse that is running its workload on a scale unit.</span></span>

## <a name="monitor-a-warehouse-order"></a><span data-ttu-id="ae70b-133">ตรวจสอบใบสั่งของคลังสินค้า</span><span class="sxs-lookup"><span data-stu-id="ae70b-133">Monitor a warehouse order</span></span>

<span data-ttu-id="ae70b-134">ในมุมมอง **รายการใบสั่งของคลังสินค้า** คุณสามารถตรวจสอบความคืบหน้าของการรับสินค้าขาเข้าได้โดยการตรวจทานค่าในคอลัมน์ **ปริมาณที่เหลืออยู่ที่จะรับ**</span><span class="sxs-lookup"><span data-stu-id="ae70b-134">In the **Warehouse order lines** view, you can monitor the progress of inbound receiving by reviewing the values in the **Quantity left to receive** column.</span></span> <span data-ttu-id="ae70b-135">หากต้องการดูรายละเอียดเกี่ยวกับงานต่างๆ ที่เสร็จสิ้นโดยการใช้แอปการจัดการคลังสินค้าบนมือถือ ให้ปฏิบัติตามขั้นตอนใดขั้นตอนหนึ่งดังต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="ae70b-135">To view details that are related to work that is done by using the Warehouse Management mobile app, follow one of these steps.</span></span>

- <span data-ttu-id="ae70b-136">ไปที่ **การจัดการคลังสินค้า \> การสอบถามและรายงาน \> รายการใบสั่งของคลังสินค้า** และใช้ตัวกรองข้อมูลเพื่อค้นหารายการที่คุณค้นหาอยู่</span><span class="sxs-lookup"><span data-stu-id="ae70b-136">Go to **Warehouse management \> Inquiries and reports \> Warehouse order lines**, and use the filter to find the lines that you're looking for.</span></span>
- <span data-ttu-id="ae70b-137">ไปที่ **การจัดซื้อและการจัดหา \> ใบสั่งซื้อ \> ใบสั่งซื้อทั้งหมด** และเปิดใบสั่งซื้อที่เกี่ยวข้อง</span><span class="sxs-lookup"><span data-stu-id="ae70b-137">Go to **Procurement and sourcing \> Purchase orders \> All purchase orders**, and open the relevant purchase order.</span></span> <span data-ttu-id="ae70b-138">ในส่วน **รายการใบสั่งซื้อ** ให้เลือกรายการหนึ่งรายการหรือมากกว่า และจากนั้น บนแถบเครื่องมือ ให้เลือก **คลังสินค้า \> รายการรับสินค้าของคลังสินค้า**</span><span class="sxs-lookup"><span data-stu-id="ae70b-138">In the **Purchase order lines** section, select one or more lines, and then, on the toolbar, select **Warehouse \> Warehouse receipt entries**.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]