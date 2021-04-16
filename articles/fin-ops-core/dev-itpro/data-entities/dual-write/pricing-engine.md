---
title: ซิงค์ตามต้องการกับกลไกจัดการการกำหนดราคา Supply Chain Management
description: หัวข้อนี้จะอธิบายวิธีการใช้กลไกการกำหนดราคาใน Microsoft Dynamics 365 Supply Chain Management จาก Dynamics 365 Sales
author: RamaKrishnamoorthy
ms.date: 03/10/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-03-10
ms.openlocfilehash: bf4154816f01040a236dde77b92ee69396158614
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 03/31/2021
ms.locfileid: "5750775"
---
# <a name="sync-on-demand-with-the-supply-chain-management-pricing-engine"></a><span data-ttu-id="f31c8-103">ซิงค์ตามต้องการกับกลไกจัดการการกำหนดราคา Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="f31c8-103">Sync on-demand with the Supply Chain Management pricing engine</span></span>

[!include [banner](../../includes/banner.md)]



<span data-ttu-id="f31c8-104">Microsoft Dynamics 365 Supply Chain Management รวมกลไกการกำหนดราคาที่จัดการข้อตกลงทางการค้า รายการราคา โปรแกรมตอบแทนลูกค้าสมาชิก โปรโมชัน และส่วนลด</span><span class="sxs-lookup"><span data-stu-id="f31c8-104">Microsoft Dynamics 365 Supply Chain Management includes a pricing engine that handles trade agreements, price lists, customer loyalty programs, promotions, and discounts.</span></span> <span data-ttu-id="f31c8-105">กลไกการกำหนดราคาจะใช้กฎที่ซับซ้อนเพื่อกำหนดราคาที่ดีที่สุดสำหรับใบเสนอราคาหรือใบสั่งที่กำหนด</span><span class="sxs-lookup"><span data-stu-id="f31c8-105">The pricing engine uses complex rules to determine the best price for a given quotation or order.</span></span> <span data-ttu-id="f31c8-106">เมื่อคุณใช้การรวมแบบสองทิศทาง คุณใช้การกำหนดราคาแบบคงที่ หรือกลไกจัดการการกำหนดราคาจาก Dynamics 365 Supply Chain Management บนหน้าใบเสนอราคาและใบสั่งใน Dynamics 365 Sales</span><span class="sxs-lookup"><span data-stu-id="f31c8-106">When you use dual-write, you use either static pricing or the pricing engine from Dynamics 365 Supply Chain Management on the Quote and Order pages in Dynamics 365 Sales.</span></span>

## <a name="use-the-pricing-engine-from-supply-chain-management-in-sales"></a><span data-ttu-id="f31c8-107">ใช้กลไกการกำหนดราคาจาก Supply Chain Management ใน Sales</span><span class="sxs-lookup"><span data-stu-id="f31c8-107">Use the pricing engine from Supply Chain Management in Sales</span></span>

1. <span data-ttu-id="f31c8-108">ใน Sales ให้ไปที่ **Sales \> ใบสั่ง**</span><span class="sxs-lookup"><span data-stu-id="f31c8-108">In Sales, go to **Sales \> Orders**.</span></span>
2. <span data-ttu-id="f31c8-109">เลือก **สร้าง** เพื่อสร้างใบสั่งใหม่ หรือเลือกใบสั่งที่มีอยู่แล้วในรายการ **ใบสั่งของฉัน**</span><span class="sxs-lookup"><span data-stu-id="f31c8-109">Select **New** to create a new order, or select an existing order in the **My Orders** list.</span></span>
3. <span data-ttu-id="f31c8-110">เพิ่มรายการในใบสั่งใหม่</span><span class="sxs-lookup"><span data-stu-id="f31c8-110">Add a new order line.</span></span>
4. <span data-ttu-id="f31c8-111">ถ้าคุณกำลังสร้างใบสั่งใหม่ ให้เลือก **ใบสั่งราคา** ในบานหน้าต่างการดำเนินการ</span><span class="sxs-lookup"><span data-stu-id="f31c8-111">If you're creating a new order, select **Price Order** on the Action Pane.</span></span> <span data-ttu-id="f31c8-112">ถ้าคุณกำลังปรับปรุงใบสั่งที่มีอยู่ ให้เลือก **คำนวณใหม่** ในบานหน้าต่างการดำเนินการ</span><span class="sxs-lookup"><span data-stu-id="f31c8-112">If you're updating an existing order, select **Recalculate** on the Action Pane.</span></span>

    <span data-ttu-id="f31c8-113">คอลัมน์ต่อไปนี้จะถูกเติมโดยอัตโนมัติใน:</span><span class="sxs-lookup"><span data-stu-id="f31c8-113">The following columns are automatically filled in:</span></span>

    + <span data-ttu-id="f31c8-114">ยอดรายละเอียด</span><span class="sxs-lookup"><span data-stu-id="f31c8-114">Detail Amount</span></span>
    + <span data-ttu-id="f31c8-115">% ส่วนลด</span><span class="sxs-lookup"><span data-stu-id="f31c8-115">Discount %</span></span>
    + <span data-ttu-id="f31c8-116">ส่วนลด</span><span class="sxs-lookup"><span data-stu-id="f31c8-116">Discount</span></span>
    + <span data-ttu-id="f31c8-117">ยอดเงินก่อนการขนส่ง</span><span class="sxs-lookup"><span data-stu-id="f31c8-117">Pre-Freight Amount</span></span>
    + <span data-ttu-id="f31c8-118">ยอดเงินค่าขนส่ง</span><span class="sxs-lookup"><span data-stu-id="f31c8-118">Freight Amount</span></span>
    + <span data-ttu-id="f31c8-119">ภาษีรวม</span><span class="sxs-lookup"><span data-stu-id="f31c8-119">Total Tax</span></span>
    + <span data-ttu-id="f31c8-120">ยอดเงินรวม</span><span class="sxs-lookup"><span data-stu-id="f31c8-120">Total Amount</span></span>
    
5. <span data-ttu-id="f31c8-121">เพื่อให้แน่ใจว่าระบบจะพิจารณาข้อตกลงทางการค้าและการขายเพื่อคำนวณราคา:</span><span class="sxs-lookup"><span data-stu-id="f31c8-121">To ensure that the system considers trade and sales agreements to calculate the price:</span></span>
    1. <span data-ttu-id="f31c8-122">นำทางไปยังสภาพแวดล้อม Supply Chain Management ของคุณ</span><span class="sxs-lookup"><span data-stu-id="f31c8-122">Navigate to your Supply Chain Management environment.</span></span>
    2. <span data-ttu-id="f31c8-123">นำทางไปยัง **บัญชีลูกหนี้ \> การตั้งค่า \> พารามิเตอร์บัญชีลูกหนี้**</span><span class="sxs-lookup"><span data-stu-id="f31c8-123">Navigate to **Accounts receivable \> Setup \> Accounts receivable parameters**.</span></span>
    3. <span data-ttu-id="f31c8-124">เลือกแท็บ **ราคา** ในแถบนำทางด้านข้าง</span><span class="sxs-lookup"><span data-stu-id="f31c8-124">Select the **Prices** tab in the side navigation bar.</span></span>
    4. <span data-ttu-id="f31c8-125">ภายใต้ fastab **การประเมินข้อตกลงทางการค้า** ให้ยกเลิกการเลือกตัวเลือก **การป้อนข้อมูลด้วยตนเอง**</span><span class="sxs-lookup"><span data-stu-id="f31c8-125">Under the **Trade agreement evaluation** fastab, uncheck the **Manual entry** option.</span></span>

## <a name="how-it-works"></a><span data-ttu-id="f31c8-126">วิธีการทำงาน</span><span class="sxs-lookup"><span data-stu-id="f31c8-126">How it works</span></span>

<span data-ttu-id="f31c8-127">เมื่อคุณเลือก **ใบสั่งราคา** ในการขาย ฟังก์ชัน **ยอดรวม** บนแท็บ **ใบสั่งขาย \> มุมมอง** ใน Supply Chain Management ถูกเรียกสำหรับใบสั่งขายที่เกี่ยวข้อง</span><span class="sxs-lookup"><span data-stu-id="f31c8-127">When you select **Price Order** in Sales, the **Totals** function on the **Sales Order \> View** tab in Supply Chain Management is called for the associated sales order.</span></span> <span data-ttu-id="f31c8-128">ค่าในยอดรวมของใบสั่งใน Sales จะใช้ในการกรอกข้อมูลในคอลัมน์ที่เกี่ยวข้องใน Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="f31c8-128">The values in the order total in Sales are used to fill in the corresponding columns in Supply Chain Management.</span></span>

<span data-ttu-id="f31c8-129">เมื่อมีการคำนวณผลรวมของใบสั่งขายใน Supply Chain Management การคำนวณจะประเมินข้อตกลงทางการค้าที่มีอยู่และข้อตกลงการขายสำหรับลูกค้าและผลิตภัณฑ์ที่แสดงรายการอยู่ในใบสั่งขาย</span><span class="sxs-lookup"><span data-stu-id="f31c8-129">When the sales order total is calculated in Supply Chain Management, the calculation evaluates the existing trade agreements and sales agreements for the customer and the products that are listed in the sales order.</span></span> <span data-ttu-id="f31c8-130">ข้อมูลนี้จะใช้เพื่อคำนวณผลรวม</span><span class="sxs-lookup"><span data-stu-id="f31c8-130">This information is used to calculate the totals.</span></span> <span data-ttu-id="f31c8-131">เมื่อมีการเลือก **ใบสั่งราคา** Sales จะสะท้อนถึงการตั้งค่าทั้งหมดที่มีการดำเนินการใน Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="f31c8-131">When **Price Order** is selected, Sales automatically reflects all the setup that has been done in Supply Chain Management.</span></span>

## <a name="limitations"></a><span data-ttu-id="f31c8-132">การจำกัด</span><span class="sxs-lookup"><span data-stu-id="f31c8-132">Limitations</span></span>

<span data-ttu-id="f31c8-133">เมื่อมีการกรอกข้อมูลในคอลัมน์ใน Sales จะมีการใช้ข้อจำกัดต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="f31c8-133">When the columns in Sales are filled in, the following limitations apply:</span></span>

+ <span data-ttu-id="f31c8-134">การตั้งค่าค่าธรรมเนียมและการปันส่วนค่าธรรมเนียมใน Supply Chain Management ไม่ถูกคัดลอกใน Sales</span><span class="sxs-lookup"><span data-stu-id="f31c8-134">The setup of charges and charge allocations in Supply Chain Management isn't replicated in Sales.</span></span>
+ <span data-ttu-id="f31c8-135">การกำหนดราคาไม่ได้พิจารณาการกำหนดราคาขายปลีกพิเศษที่ระบุไว้ในคอลัมน์ **ช่องทางการขายปลีก** บนหน้ารายการใบสั่งขายใน Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="f31c8-135">Pricing doesn't consider special retail pricing that is specified in the **Retail Channel** column on the sales order line page in Supply Chain Management.</span></span>
+ <span data-ttu-id="f31c8-136">ส่วนลดที่กำหนดในส่วน **การจัดการการให้ส่วนลดทางการค้า** ของ Supply Chain Management ไม่ได้รับการพิจารณา</span><span class="sxs-lookup"><span data-stu-id="f31c8-136">Discounts that are defined in the **Trade Allowance Management** section of Supply Chain Management aren't considered.</span></span>


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]