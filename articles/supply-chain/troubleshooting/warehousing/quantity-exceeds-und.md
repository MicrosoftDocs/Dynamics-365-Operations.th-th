---
title: คุณไม่สามารถยืนยันการจัดส่งได้ เนื่องจากปริมาณเกินเปอร์เซ็นต์การจัดส่งน้อยกว่าปริมาณที่สั่ง
description: คุณไม่สามารถยืนยันการจัดส่งได้ เนื่องจากปริมาณเกินเปอร์เซ็นต์การจัดส่งน้อยกว่าปริมาณที่สั่ง
author: perlynne
ms.date: 04/21/2021
ms.topic: troubleshooting
ms.search.form: WHSLoadTable_WHSShipConfirm,WHSLoadPlanningListPage_WHSShipConfirm,WHSLoadPlanningWorkbench_WHSShipConfirm,WHSTransportLoad_WHSShipConfirm,WHSShipPlanningListPage_WHSShipConfirm,WHSShipmentDetails_WHSShipConfirm,WHSWorkTable_WHSShipConfirm,WHSWorkTableListPage_WHSShipConfirm,Dialog_WHSOutboundShipConfirmController_WHSOutboundShipConfirm,WHSContainerCloseDiag_WHSShipConfirm
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: lbc
ms.search.validFrom: 2021-04-21
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: 625003731485329b93f5f9454ccece580c889613
ms.sourcegitcommit: c2c6d687a89bc1534c029109315c23e92865b63b
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 05/31/2021
ms.locfileid: "6123830"
---
# <a name="you-cant-confirm-a-shipment-because-the-quantity-exceeds-the-underdelivery-percentage"></a><span data-ttu-id="e15c4-103">คุณไม่สามารถยืนยันการจัดส่งได้ เนื่องจากปริมาณเกินเปอร์เซ็นต์การจัดส่งน้อยกว่าปริมาณที่สั่ง</span><span class="sxs-lookup"><span data-stu-id="e15c4-103">You can't confirm a shipment because the quantity exceeds the underdelivery percentage</span></span>

<span data-ttu-id="e15c4-104">รหัสข้อผิดพลาด: WAX1686</span><span class="sxs-lookup"><span data-stu-id="e15c4-104">Error code: WAX1686</span></span>

## <a name="symptoms"></a><span data-ttu-id="e15c4-105">อาการ</span><span class="sxs-lookup"><span data-stu-id="e15c4-105">Symptoms</span></span>

<span data-ttu-id="e15c4-106">เมื่อคุณพยายามยืนยันการจัดส่ง ระบบจะแสดงข้อความแสดงข้อผิดพลาดต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="e15c4-106">When you try to confirm a shipment, the system shows the following error message:</span></span>

> <span data-ttu-id="e15c4-107">การจัดส่งปริมาณงานในศูนย์การผลิต %1 ไม่สามารถยืนยันได้เนื่องจากปริมาณของสินค้า %2 เกินกว่าเปอร์เซ็นต์ที่กําหนดไว้เกี่ยวกับการจัดส่งน้อยกว่าปริมาณที่กําหนด</span><span class="sxs-lookup"><span data-stu-id="e15c4-107">The shipment for load %1 could not be confirmed because the quantity for item %2 exceeds the percentage that is defined for underdelivery.</span></span>

<span data-ttu-id="e15c4-108">ดังนั้นคุณจึงไม่สามารถยืนยันการจัดส่งของสินค้าได้</span><span class="sxs-lookup"><span data-stu-id="e15c4-108">Therefore, you can't confirm the shipment for the load.</span></span>

## <a name="cause"></a><span data-ttu-id="e15c4-109">สาเหตุ</span><span class="sxs-lookup"><span data-stu-id="e15c4-109">Cause</span></span>

<span data-ttu-id="e15c4-110">ปริมาณของสินค้าหรือการจัดส่งมีการเบิกเพียงบางส่วนเท่านั้น</span><span class="sxs-lookup"><span data-stu-id="e15c4-110">The quantity of the load or shipment has been only partially picked.</span></span> <span data-ttu-id="e15c4-111">ปริมาณปัจจุบันน้อยกว่าปริมาณที่เบิกสินค้าตามเปอร์เซ็นต์ที่อยู่นอกเปอร์เซ็นต์การจัดส่งน้อยกว่าปริมาณที่กำหนดที่อนุญาต</span><span class="sxs-lookup"><span data-stu-id="e15c4-111">The quantity is currently less than the picked quantity by a percentage that is outside the allowed underdelivery percentage.</span></span>

## <a name="resolution"></a><span data-ttu-id="e15c4-112">ความละเอียด</span><span class="sxs-lookup"><span data-stu-id="e15c4-112">Resolution</span></span>

<span data-ttu-id="e15c4-113">เมื่อต้องการแก้ไขปัญหานี้ ให้ทำหนึ่งในงานต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="e15c4-113">To fix this issue, complete one of the following tasks:</span></span>

- <span data-ttu-id="e15c4-114">ตั้งค่าปริมาณรายการสินค้า</span><span class="sxs-lookup"><span data-stu-id="e15c4-114">Set the load line quantity.</span></span>
- <span data-ttu-id="e15c4-115">ตั้งค่าเปอร์เซ็นต์การจัดส่งน้อยกว่าปริมาณที่กำหนด</span><span class="sxs-lookup"><span data-stu-id="e15c4-115">Set the underdelivery percentage.</span></span>

### <a name="set-the-load-line-quantity"></a><span data-ttu-id="e15c4-116">ตั้งค่าปริมาณรายการสินค้า</span><span class="sxs-lookup"><span data-stu-id="e15c4-116">Set the load line quantity</span></span>

<span data-ttu-id="e15c4-117">ในการกําหนดการตั้งค่าปริมาณสินค้า ให้ปฏิบัติตามขั้นตอนต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="e15c4-117">To set the load line quantity, follow these steps.</span></span>

1. <span data-ttu-id="e15c4-118">ไปที่ **การจัดการคลังสินค้า \> จำนวนงานในศูนย์การผลิต \> จำนวนงานในศูนย์การผลิตทั้งหมด**</span><span class="sxs-lookup"><span data-stu-id="e15c4-118">Go to **Warehouse management \> Loads \> All loads**.</span></span>
1. <span data-ttu-id="e15c4-119">เลือกสินค้าที่การจัดส่งไม่สามารถยืนยันได้</span><span class="sxs-lookup"><span data-stu-id="e15c4-119">Select the load that the shipment can't be confirmed for.</span></span>
1. <span data-ttu-id="e15c4-120">บนแท็บด่วน **รายการสินค้า** ให้เลือกรายการสินค้าที่เกินกว่าเปอร์เซ็นต์การจัดส่งน้อยกว่าปริมาณที่กำหนด</span><span class="sxs-lookup"><span data-stu-id="e15c4-120">On the **Load lines** FastTab, select the load line for the item that exceeds the underdelivery percentage.</span></span>
1. <span data-ttu-id="e15c4-121">บนแท็บด่วน **รายละเอียดของรายการ** เลือก **ใบสั่ง**</span><span class="sxs-lookup"><span data-stu-id="e15c4-121">On the **Line details** FastTab, select **Order**.</span></span>
1. <span data-ttu-id="e15c4-122">ในฟิลด์ **ปริมาณ** ให้ตั้งค่าเป็นปริมาณที่เบิกสินค้า (นั่นคือค่า **ปริมาณที่สร้างขึ้นของงาน**) เพื่อให้การยืนยันการจัดส่งสามารถเกิดขึ้นได้</span><span class="sxs-lookup"><span data-stu-id="e15c4-122">In the **Quantity** field, set the value to the picked quantity (that is, to the **Work created quantity** value), so that shipment confirmation can occur.</span></span>

### <a name="set-the-underdelivery-percentage"></a><span data-ttu-id="e15c4-123">ตั้งค่าเปอร์เซ็นต์การจัดส่งน้อยกว่าปริมาณที่กำหนด</span><span class="sxs-lookup"><span data-stu-id="e15c4-123">Set the underdelivery percentage</span></span>

<span data-ttu-id="e15c4-124">ในการกําหนดเปอร์เซ็นต์การจัดส่งน้อยกว่าปริมาณที่กำหนด ให้ปฏิบัติตามขั้นตอนต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="e15c4-124">To set the underdelivery percentage, follow these steps.</span></span>

1. <span data-ttu-id="e15c4-125">ไปที่ **การจัดการคลังสินค้า \> จำนวนงานในศูนย์การผลิต \> จำนวนงานในศูนย์การผลิตทั้งหมด**</span><span class="sxs-lookup"><span data-stu-id="e15c4-125">Go to **Warehouse management \> Loads \> All loads**.</span></span>
1. <span data-ttu-id="e15c4-126">เลือกสินค้าที่การจัดส่งไม่สามารถยืนยันได้</span><span class="sxs-lookup"><span data-stu-id="e15c4-126">Select the load that the shipment can't be confirmed for.</span></span>
1. <span data-ttu-id="e15c4-127">บนแท็บด่วน **รายการสินค้า** ให้เลือกรายการสินค้าที่เกินกว่าเปอร์เซ็นต์การจัดส่งน้อยกว่าปริมาณที่กำหนด</span><span class="sxs-lookup"><span data-stu-id="e15c4-127">On the **Load lines** FastTab, select the load line for the item that exceeds the underdelivery percentage.</span></span>
1. <span data-ttu-id="e15c4-128">บนแท็บด่วน **รายละเอียดของรายการ** เลือก **ทั่วไป**</span><span class="sxs-lookup"><span data-stu-id="e15c4-128">On the **Line details** FastTab, select **General**.</span></span>
1. <span data-ttu-id="e15c4-129">ในฟิลด์ **การจัดส่งน้อยกว่าปริมาณที่กำหนด** ให้ตั้งค่าเป็นเปอร์เซ็นต์ที่มากกว่าปริมาณที่สั่ง ซึ่งสามารถรองรับปริมาณที่เบิกแล้วเทียบกับปริมาณสินค้า เพื่อให้การยืนยันการจัดส่งสามารถเกิดขึ้นได้</span><span class="sxs-lookup"><span data-stu-id="e15c4-129">In the **Underdelivery** field, set the value to a larger percentage that accommodates the quantity that has been picked against the load quantity, so that shipment confirmation can occur.</span></span>
