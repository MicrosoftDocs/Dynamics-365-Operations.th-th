---
title: คุณไม่สามารถยืนยันการจัดส่งได้ เนื่องจากสินค้ายังไม่ได้รับการเบิก
description: คุณไม่สามารถยืนยันการจัดส่งได้ เนื่องจากสินค้ายังไม่ได้รับการเบิก
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
ms.openlocfilehash: 23a517e7769dc86ebec30e4f17c62172a6ad8801
ms.sourcegitcommit: cd9016e9787169cb800889d335b9c5919ddbe4af
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 04/23/2021
ms.locfileid: "5938560"
---
# <a name="you-cant-confirm-a-shipment-because-items-havent-been-picked"></a><span data-ttu-id="6d13f-103">คุณไม่สามารถยืนยันการจัดส่งได้ เนื่องจากสินค้ายังไม่ได้รับการเบิก</span><span class="sxs-lookup"><span data-stu-id="6d13f-103">You can't confirm a shipment because items haven't been picked</span></span>

<span data-ttu-id="6d13f-104">รหัสข้อผิดพลาด: LoadNotPickedAndMovedToFinalShippingLocation</span><span class="sxs-lookup"><span data-stu-id="6d13f-104">Error code: LoadNotPickedAndMovedToFinalShippingLocation</span></span>

## <a name="symptoms"></a><span data-ttu-id="6d13f-105">อาการ</span><span class="sxs-lookup"><span data-stu-id="6d13f-105">Symptoms</span></span>

<span data-ttu-id="6d13f-106">เมื่อคุณพยายามยืนยันการจัดส่ง ระบบจะแสดงข้อความแสดงข้อผิดพลาดต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="6d13f-106">When you try to confirm a shipment, the system shows the following error message:</span></span>

> <span data-ttu-id="6d13f-107">สินค้าบางอย่างที่จำเป็นสำหรับจำนวนงานในศูนย์การผลิต %1 ยังไม่ได้รับการเบิกและเคลื่อนย้ายไปยังสถานที่จัดส่งขั้นสุดท้าย</span><span class="sxs-lookup"><span data-stu-id="6d13f-107">Some of the items that are needed for load %1 have not yet been picked and moved to the final shipping location.</span></span>

<span data-ttu-id="6d13f-108">ดังนั้นคุณจึงไม่สามารถยืนยันการจัดส่งของสินค้าได้</span><span class="sxs-lookup"><span data-stu-id="6d13f-108">Therefore, you can't confirm the shipment for the load.</span></span>

## <a name="cause"></a><span data-ttu-id="6d13f-109">สาเหตุ</span><span class="sxs-lookup"><span data-stu-id="6d13f-109">Cause</span></span>

<span data-ttu-id="6d13f-110">ไม่สามารถยืนยันสินค้าหรือการจัดส่งในสถานะปัจจุบันได้เนื่องจากอาจมีเงื่อนไขอย่างใดอย่างหนึ่งต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="6d13f-110">The load or shipment can't be confirmed in its current state because one of the following conditions might exist:</span></span>

- <span data-ttu-id="6d13f-111">ยังไม่ได้เบิกสินค้าและย้ายไปยังสถานที่จัดส่งสุดท้าย</span><span class="sxs-lookup"><span data-stu-id="6d13f-111">The related work hasn't yet been picked and moved to the final shipping location.</span></span>
- <span data-ttu-id="6d13f-112">ปริมาณงานที่เบิกไม่ตรงกับปริมาณงานที่สร้างบนรายการสินค้า</span><span class="sxs-lookup"><span data-stu-id="6d13f-112">The picked work quantity doesn't match the created work quantity on the load line.</span></span>

## <a name="resolution"></a><span data-ttu-id="6d13f-113">ความละเอียด</span><span class="sxs-lookup"><span data-stu-id="6d13f-113">Resolution</span></span>

<span data-ttu-id="6d13f-114">ตรวจสอบใบสั่งขายหรือใบสั่งโอนย้ายที่เกี่ยวข้องเกี่ยวกับสินค้าหรือการจัดส่ง</span><span class="sxs-lookup"><span data-stu-id="6d13f-114">Check the related sales orders or transfer orders for the load or shipment.</span></span> <span data-ttu-id="6d13f-115">ตรวจสอบให้แน่ใจว่างานที่เกี่ยวข้องทั้งหมดเสร็จสมบูรณ์แล้วในสถานที่จัดส่งสุดท้าย และปริมาณตรงกัน</span><span class="sxs-lookup"><span data-stu-id="6d13f-115">Make sure that all the related work has been completed at the final shipping location, and that the quantities match.</span></span>

1. <span data-ttu-id="6d13f-116">ไปที่ **การจัดการคลังสินค้า \> จำนวนงานในศูนย์การผลิต \> จำนวนงานในศูนย์การผลิตทั้งหมด**</span><span class="sxs-lookup"><span data-stu-id="6d13f-116">Go to **Warehouse management \> Loads \> All loads**.</span></span>
1. <span data-ttu-id="6d13f-117">เลือกสินค้าที่การจัดส่งไม่สามารถยืนยันได้</span><span class="sxs-lookup"><span data-stu-id="6d13f-117">Select the load that the shipment can't be confirmed for.</span></span>
1. <span data-ttu-id="6d13f-118">บนแท็บด่วน **รายการสินค้า** ให้เลือกรายการสินค้า</span><span class="sxs-lookup"><span data-stu-id="6d13f-118">On the **Load lines** FastTab, select the load line.</span></span>
1. <span data-ttu-id="6d13f-119">บันทึกค่าของฟิลด์ **ปริมาณที่สร้างขึ้นของงาน**</span><span class="sxs-lookup"><span data-stu-id="6d13f-119">Make a note of the value of the **Work created quantity** field.</span></span>
1. <span data-ttu-id="6d13f-120">บนบานหน้าต่างการดำเนินการ บนแท็บ **สินค้า** ในกลุ่ม **ข้อมูลที่เกี่ยวข้อง** ให้เลือก **งาน**</span><span class="sxs-lookup"><span data-stu-id="6d13f-120">On the Action Pane, on the **Loads** tab, in the **Related information** group, select **Work**.</span></span>
1. <span data-ttu-id="6d13f-121">ตรวจสอบว่างานเสร็จสมบูรณ์แล้วที่สถานที่จัดส่งสุดท้าย และปริมาณงานที่เบิกตรงกับปริมาณงานที่สร้างบนรายการสินค้า</span><span class="sxs-lookup"><span data-stu-id="6d13f-121">Verify that the work has been completed at the final shipping location, and that the picked work quantity matches the created work quantity on the load line.</span></span>
1. <span data-ttu-id="6d13f-122">ทําขั้นตอนนี้ซ้ํากับรายการสินค้าทั้งหมดเพื่อให้แน่ใจว่าตรงตามเกณฑ์ทั้งหมด</span><span class="sxs-lookup"><span data-stu-id="6d13f-122">Repeat this procedure for all load lines to make sure that all criteria are met.</span></span>
