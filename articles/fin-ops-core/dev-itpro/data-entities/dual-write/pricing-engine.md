---
title: ซิงค์กับกลไกจัดการการกำหนดราคาของ Dynamics 365 Supply Chain Management
description: หัวข้อนี้จะอธิบายวิธีการใช้กลไกการกำหนดราคาใน Microsoft Dynamics 365 Supply Chain Management จาก Dynamics 365 Sales
author: RamaKrishnamoorthy
manager: AnnBe
ms.date: 03/10/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-03-10
ms.openlocfilehash: 5ffc0358ff58b2a05aa84b4467a27d88b5e1ec42
ms.sourcegitcommit: 984604fd651d74aa49a2d7513f096faaf49f9f27
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 04/18/2020
ms.locfileid: "3270347"
---
# <a name="sync-with-the-dynamics-365-supply-chain-management-pricing-engine-on-demand"></a><span data-ttu-id="57585-103">ซิงค์กับกลไกจัดการการกำหนดราคาของ Dynamics 365 Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="57585-103">Sync with the Dynamics 365 Supply Chain Management pricing engine on demand</span></span>

[!include [banner](../../includes/banner.md)]



<span data-ttu-id="57585-104">Microsoft Dynamics 365 Supply Chain Management รวมกลไกการกำหนดราคาที่จัดการข้อตกลงทางการค้า รายการราคา โปรแกรมตอบแทนลูกค้าสมาชิก โปรโมชัน และส่วนลด</span><span class="sxs-lookup"><span data-stu-id="57585-104">Microsoft Dynamics 365 Supply Chain Management includes a pricing engine that handles trade agreements, price lists, customer loyalty programs, promotions, and discounts.</span></span> <span data-ttu-id="57585-105">กลไกการกำหนดราคาจะใช้กฎที่ซับซ้อนเพื่อกำหนดราคาที่ดีที่สุดสำหรับใบเสนอราคาหรือใบสั่งที่กำหนด</span><span class="sxs-lookup"><span data-stu-id="57585-105">The pricing engine uses complex rules to determine the best price for a given quotation or order.</span></span> <span data-ttu-id="57585-106">เมื่อคุณใช้การรวมแบบสองทิศทาง คุณใช้การกำหนดราคาแบบคงที่ หรือกลไกจัดการการกำหนดราคาจาก Dynamics 365 Supply Chain Management บนหน้าใบเสนอราคาและใบสั่งใน Dynamics 365 Sales</span><span class="sxs-lookup"><span data-stu-id="57585-106">When you use dual-write, you use either static pricing or the pricing engine from Dynamics 365 Supply Chain Management on the Quote and Order pages in Dynamics 365 Sales.</span></span>

## <a name="use-the-pricing-engine-from-supply-chain-management-in-sales"></a><span data-ttu-id="57585-107">ใช้กลไกการกำหนดราคาจาก Supply Chain Management ใน Sales</span><span class="sxs-lookup"><span data-stu-id="57585-107">Use the pricing engine from Supply Chain Management in Sales</span></span>

1. <span data-ttu-id="57585-108">ใน Sales ให้ไปที่ **Sales \> ใบสั่ง**</span><span class="sxs-lookup"><span data-stu-id="57585-108">In Sales, go to **Sales \> Orders**.</span></span>
2. <span data-ttu-id="57585-109">เลือก **สร้าง** เพื่อสร้างใบสั่งใหม่ หรือเลือกใบสั่งที่มีอยู่แล้วในรายการ **ใบสั่งของฉัน**</span><span class="sxs-lookup"><span data-stu-id="57585-109">Select **New** to create a new order, or select an existing order in the **My Orders** list.</span></span>
3. <span data-ttu-id="57585-110">เพิ่มรายการในใบสั่งใหม่</span><span class="sxs-lookup"><span data-stu-id="57585-110">Add a new order line.</span></span>
4. <span data-ttu-id="57585-111">ถ้าคุณกำลังสร้างใบสั่งใหม่ ให้เลือก **ใบสั่งราคา** ในบานหน้าต่างการดำเนินการ</span><span class="sxs-lookup"><span data-stu-id="57585-111">If you're creating a new order, select **Price Order** on the Action Pane.</span></span> <span data-ttu-id="57585-112">ถ้าคุณกำลังปรับปรุงใบสั่งที่มีอยู่ ให้เลือก **คำนวณใหม่** ในบานหน้าต่างการดำเนินการ</span><span class="sxs-lookup"><span data-stu-id="57585-112">If you're updating an existing order, select **Recalculate** on the Action Pane.</span></span>

    <span data-ttu-id="57585-113">ฟิลด์ต่อไปนี้จะถูกเติมโดยอัตโนมัติใน:</span><span class="sxs-lookup"><span data-stu-id="57585-113">The following fields are automatically filled in:</span></span>

    + <span data-ttu-id="57585-114">ยอดรายละเอียด</span><span class="sxs-lookup"><span data-stu-id="57585-114">Detail Amount</span></span>
    + <span data-ttu-id="57585-115">% ส่วนลด</span><span class="sxs-lookup"><span data-stu-id="57585-115">Discount %</span></span>
    + <span data-ttu-id="57585-116">ส่วนลด</span><span class="sxs-lookup"><span data-stu-id="57585-116">Discount</span></span>
    + <span data-ttu-id="57585-117">ยอดเงินก่อนการขนส่ง</span><span class="sxs-lookup"><span data-stu-id="57585-117">Pre-Freight Amount</span></span>
    + <span data-ttu-id="57585-118">ยอดเงินค่าขนส่ง</span><span class="sxs-lookup"><span data-stu-id="57585-118">Freight Amount</span></span>
    + <span data-ttu-id="57585-119">ภาษีรวม</span><span class="sxs-lookup"><span data-stu-id="57585-119">Total Tax</span></span>
    + <span data-ttu-id="57585-120">ยอดเงินรวม</span><span class="sxs-lookup"><span data-stu-id="57585-120">Total Amount</span></span>
    
5. <span data-ttu-id="57585-121">เพื่อให้แน่ใจว่าระบบจะพิจารณาข้อตกลงทางการค้าและการขายเพื่อคำนวณราคา:</span><span class="sxs-lookup"><span data-stu-id="57585-121">To ensure that the system considers trade and sales agreements to calculate the price:</span></span>
    1. <span data-ttu-id="57585-122">นำทางไปยังสภาพแวดล้อม Supply Chain Management ของคุณ</span><span class="sxs-lookup"><span data-stu-id="57585-122">Navigate to your Supply Chain Management environment.</span></span>
    2. <span data-ttu-id="57585-123">นำทางไปยัง **บัญชีลูกหนี้ \> การตั้งค่า \> พารามิเตอร์บัญชีลูกหนี้**</span><span class="sxs-lookup"><span data-stu-id="57585-123">Navigate to **Accounts receivable \> Setup \> Accounts receivable parameters**.</span></span>
    3. <span data-ttu-id="57585-124">เลือกแท็บ **ราคา** ในแถบนำทางด้านข้าง</span><span class="sxs-lookup"><span data-stu-id="57585-124">Select the **Prices** tab in the side navigation bar.</span></span>
    4. <span data-ttu-id="57585-125">ภายใต้ fastab **การประเมินข้อตกลงทางการค้า** ให้ยกเลิกการเลือกตัวเลือก **การป้อนข้อมูลด้วยตนเอง**</span><span class="sxs-lookup"><span data-stu-id="57585-125">Under the **Trade agreement evaluation** fastab, uncheck the **Manual entry** option.</span></span>

## <a name="how-it-works"></a><span data-ttu-id="57585-126">วิธีการทำงาน</span><span class="sxs-lookup"><span data-stu-id="57585-126">How it works</span></span>

<span data-ttu-id="57585-127">เมื่อคุณเลือก **ใบสั่งราคา** ในการขาย ฟังก์ชัน **ยอดรวม** บนแท็บ **ใบสั่งขาย \> มุมมอง** ใน Supply Chain Management ถูกเรียกสำหรับใบสั่งขายที่เกี่ยวข้อง</span><span class="sxs-lookup"><span data-stu-id="57585-127">When you select **Price Order** in Sales, the **Totals** function on the **Sales Order \> View** tab in Supply Chain Management is called for the associated sales order.</span></span> <span data-ttu-id="57585-128">ค่าในยอดรวมของใบสั่งใน Sales จะใช้ในการกรอกข้อมูลในฟิลด์ที่เกี่ยวข้องใน Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="57585-128">The values in the order total in Sales are used to fill in the corresponding fields in Supply Chain Management.</span></span>

<span data-ttu-id="57585-129">เมื่อมีการคำนวณผลรวมของใบสั่งขายใน Supply Chain Management การคำนวณจะประเมินข้อตกลงทางการค้าที่มีอยู่และข้อตกลงการขายสำหรับลูกค้าและผลิตภัณฑ์ที่แสดงรายการอยู่ในใบสั่งขาย</span><span class="sxs-lookup"><span data-stu-id="57585-129">When the sales order total is calculated in Supply Chain Management, the calculation evaluates the existing trade agreements and sales agreements for the customer and the products that are listed in the sales order.</span></span> <span data-ttu-id="57585-130">ข้อมูลนี้จะใช้เพื่อคำนวณผลรวม</span><span class="sxs-lookup"><span data-stu-id="57585-130">This information is used to calculate the totals.</span></span> <span data-ttu-id="57585-131">เมื่อมีการเลือก **ใบสั่งราคา** Sales จะสะท้อนถึงการตั้งค่าทั้งหมดที่มีการดำเนินการใน Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="57585-131">When **Price Order** is selected, Sales automatically reflects all the setup that has been done in Supply Chain Management.</span></span>

## <a name="limitations"></a><span data-ttu-id="57585-132">การจำกัด</span><span class="sxs-lookup"><span data-stu-id="57585-132">Limitations</span></span>

<span data-ttu-id="57585-133">เมื่อมีการกรอกข้อมูลในฟิลด์ใน Sales จะมีการใช้ข้อจำกัดต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="57585-133">When the fields in Sales are filled in, the following limitations apply:</span></span>

+ <span data-ttu-id="57585-134">การตั้งค่าค่าธรรมเนียมและการปันส่วนค่าธรรมเนียมใน Supply Chain Management ไม่ถูกคัดลอกใน Sales</span><span class="sxs-lookup"><span data-stu-id="57585-134">The setup of charges and charge allocations in Supply Chain Management isn't replicated in Sales.</span></span>
+ <span data-ttu-id="57585-135">การกำหนดราคาไม่ได้พิจารณาการกำหนดราคาขายปลีกพิเศษที่ระบุไว้ในฟิลด์ **ช่องทางการขายปลีก** บนหน้ารายการใบสั่งขายใน Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="57585-135">Pricing doesn't consider special retail pricing that is specified in the **Retail Channel** field on the sales order line page in Supply Chain Management.</span></span>
+ <span data-ttu-id="57585-136">ส่วนลดที่กำหนดในส่วน **การจัดการการให้ส่วนลดทางการค้า** ของ Supply Chain Management ไม่ได้รับการพิจารณา</span><span class="sxs-lookup"><span data-stu-id="57585-136">Discounts that are defined in the **Trade Allowance Management** section of Supply Chain Management aren't considered.</span></span>
