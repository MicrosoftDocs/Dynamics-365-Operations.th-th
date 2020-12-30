---
title: ตั้งค่าสมุดบัญชีสัญญาเช่า
description: หัวข้อนี้อธิบายถึงข้อมูลที่เก็บรักษาไว้ในสมุดบัญชีสัญญาเช่า สมุดบัญชีสัญญาเช่ามีนโยบายการบัญชีที่กำหนดวิธีการลงบัญชีสัญญาเช่าในระบบ
author: moaamer
manager: Ann Beebe
ms.date: 10/28/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TaxTable
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations, Retail
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-10-28
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 28518341544327f1983e563b719b0f455b6e1c43
ms.sourcegitcommit: aeee39c01d3f93a6dfcf2013965fa975a740596a
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 10/28/2020
ms.locfileid: "4448609"
---
# <a name="set-up-lease-books"></a><span data-ttu-id="20dfc-104">ตั้งค่าสมุดบัญชีสัญญาเช่า</span><span class="sxs-lookup"><span data-stu-id="20dfc-104">Set up lease books</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="20dfc-105">สมุดบัญชีสัญญาเช่ามีนโยบายการบัญชีที่กำหนดวิธีการลงบัญชีสัญญาเช่าในระบบ</span><span class="sxs-lookup"><span data-stu-id="20dfc-105">Lease books contain the accounting policies that determine how a lease is accounted for in the system.</span></span> <span data-ttu-id="20dfc-106">นอกจากการบัญชีพื้นฐานเงินสด การเช่าสินทรัพย์รองรับมาตรฐานต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="20dfc-106">In addition to cash basis accounting, Asset leasing supports the following standards:</span></span>

- <span data-ttu-id="20dfc-107">หลักการบัญชีที่รับรองโดยทั่วไปในสหรัฐอเมริกา (US GAAP)</span><span class="sxs-lookup"><span data-stu-id="20dfc-107">Generally Accepted Accounting Principles in the United States (US GAAP)</span></span>
- <span data-ttu-id="20dfc-108">การเข้ารหัสมาตรฐานทางบัญชี หัวข้อ 842 (ASC 842)</span><span class="sxs-lookup"><span data-stu-id="20dfc-108">Accounting Standards Codification Topic 842 (ASC 842)</span></span>
- <span data-ttu-id="20dfc-109">ASC 840</span><span class="sxs-lookup"><span data-stu-id="20dfc-109">ASC 840</span></span>
- <span data-ttu-id="20dfc-110">มาตรฐาน Financial Reporting ระหว่างประเทศ 16 (IFRS 16)</span><span class="sxs-lookup"><span data-stu-id="20dfc-110">International Financial Reporting Standard 16 (IFRS 16)</span></span>
- <span data-ttu-id="20dfc-111">มาตรฐานการบัญชีระหว่างประเทศ 17 (IAS 17)</span><span class="sxs-lookup"><span data-stu-id="20dfc-111">International Accounting Standard 17 (IAS 17)</span></span>

<span data-ttu-id="20dfc-112">เมื่อต้องการสร้างสมุดบัญชีสัญญาเช่า ให้ทำตามขั้นตอนเหล่านี้</span><span class="sxs-lookup"><span data-stu-id="20dfc-112">To create a lease book, follow these steps.</span></span>

1. <span data-ttu-id="20dfc-113">ไปที่ **การเช่าสินทรัพย์ \> การตั้งค่า \> สมุดบัญชีสัญญาเช่า**</span><span class="sxs-lookup"><span data-stu-id="20dfc-113">Go to **Asset leasing \> Setup \> Lease books**.</span></span>
2. <span data-ttu-id="20dfc-114">ให้เลือก **สร้าง** เพื่อเพิ่มสมุดบัญชี</span><span class="sxs-lookup"><span data-stu-id="20dfc-114">Select **New** to add a book.</span></span>
3. <span data-ttu-id="20dfc-115">ตั้งค่าฟิลด์เหล่านี้</span><span class="sxs-lookup"><span data-stu-id="20dfc-115">Set the following fields.</span></span>

    | <span data-ttu-id="20dfc-116">ชื่อ</span><span class="sxs-lookup"><span data-stu-id="20dfc-116">Name</span></span>                                     | <span data-ttu-id="20dfc-117">คำอธิบาย</span><span class="sxs-lookup"><span data-stu-id="20dfc-117">Description</span></span> |
    |------------------------------------------|-------------|
    | <span data-ttu-id="20dfc-118">ชั้นของการลงรายการบัญชี</span><span class="sxs-lookup"><span data-stu-id="20dfc-118">Posting layer</span></span>                            | <span data-ttu-id="20dfc-119">เลือกชั้นของการลงรายการบัญชีที่จะใช้</span><span class="sxs-lookup"><span data-stu-id="20dfc-119">Select the posting layer to use.</span></span> <span data-ttu-id="20dfc-120">แต่ละสมุดบัญชีที่แนบกับสัญญาเช่าจะมีการตั้งค่าสำหรับชั้นของการลงรายการบัญชีเฉพาะ</span><span class="sxs-lookup"><span data-stu-id="20dfc-120">Each book that is attached to a lease is set up for a specific posting layer.</span></span> <span data-ttu-id="20dfc-121">ชั้นของการลงรายการบัญชีแต่ละชั้นมีวัตถุประสงค์ในการลงรายการบัญชีต่างกัน</span><span class="sxs-lookup"><span data-stu-id="20dfc-121">Each posting layer has different posting purposes.</span></span> |
    | <span data-ttu-id="20dfc-122">ชนิดสัญญาเช่า</span><span class="sxs-lookup"><span data-stu-id="20dfc-122">Lease type</span></span>                               | <span data-ttu-id="20dfc-123">เลือกว่าควรมีการจัดประเภทสัญญาเช่าโดยอัตโนมัติหรือไม่ หรือควรจะกำหนดไว้ล่วงหน้าเป็นสัญญาเช่าการเงินหรือสัญญาเช่าดำเนินงาน</span><span class="sxs-lookup"><span data-stu-id="20dfc-123">Select whether the lease should be classified automatically, or whether it should be predefined as a finance or operating lease.</span></span> |
    | <span data-ttu-id="20dfc-124">แม่บทการบัญชี</span><span class="sxs-lookup"><span data-stu-id="20dfc-124">Accounting framework</span></span>                     | <span data-ttu-id="20dfc-125">เลือกกรอบงานที่เชื่อมโยงกับสมุดบัญชี</span><span class="sxs-lookup"><span data-stu-id="20dfc-125">Select the framework that is associated with the book.</span></span> |
    | <span data-ttu-id="20dfc-126">การตั้งค่าระยะเวลาของสัญญาเช่า / อายุการใช้งาน</span><span class="sxs-lookup"><span data-stu-id="20dfc-126">Lease term/Useful life Set Up</span></span>          | <span data-ttu-id="20dfc-127">ระบบจะจัดประเภทการเช่าเป็นสัญญาเช่าการเงินถ้ามีการตั้งค่าชนิดสัญญาเช่าเป็น **อัตโนมัติ** และถ้าระยะเวลาของสัญญาเช่าเหนือการใช้งานของสินทรัพย์มากกว่าหรือเท่ากับเปอร์เซ็นต์ที่ป้อนไว้ในฟิลด์นี้</span><span class="sxs-lookup"><span data-stu-id="20dfc-127">The system will classify the lease as a finance lease if the lease type is set to **Automatic**, and if the lease term over useful life of the asset is greater than or equal to the percentage entered in this field.</span></span>  |
    | <span data-ttu-id="20dfc-128">การตั้งค่ามูลค่าปัจจุบัน / มูลค่ายุติธรรมของสินทรัพย์</span><span class="sxs-lookup"><span data-stu-id="20dfc-128">Present value / Asset fair value setup</span></span>   | <span data-ttu-id="20dfc-129">ป้อนจำนวนทั้งหมดเพื่อกำหนดขีดจำกัดที่จะกำหนดชนิดสัญญาเช่า</span><span class="sxs-lookup"><span data-stu-id="20dfc-129">Enter a whole number to define the threshold that will determine the lease type.</span></span> <span data-ttu-id="20dfc-130">ถ้ามูลค่าปัจจุบันของการชำระเงินค่าเช่าขั้นต่ำในอนาคตมากกว่าค่าที่กำหนดโดยผู้ใช้จากการตั้งค่าสมุดบัญชี และถ้ามีการตั้งค่าการจัดประเภทสัญญาเช่าของสมุดบัญชีเป็นอัตโนมัติ ระบบจะจัดประเภทสัญญาเช่าเป็นสัญญาเช่าทางการเงิน</span><span class="sxs-lookup"><span data-stu-id="20dfc-130">If the present value of future minimum lease payments is more than the user-defined value from the book setup, and if the book's lease classification is set to automatic, the system will classify the lease as a finance lease.</span></span> |
    | <span data-ttu-id="20dfc-131">ขีดจำกัดระยะสั้น</span><span class="sxs-lookup"><span data-stu-id="20dfc-131">Short-term threshold</span></span>                     | <span data-ttu-id="20dfc-132">ป้อนจำนวนเดือนที่จะใช้เป็นขีดจำกัดสำหรับสัญญาเช่าระยะสั้น</span><span class="sxs-lookup"><span data-stu-id="20dfc-132">Enter the number of months to use as a threshold for short-term leases.</span></span> <span data-ttu-id="20dfc-133">ถ้าระยะเวลาของสัญญาเช่ามีค่าน้อยกว่าหรือเท่ากับจำนวนเดือนที่คุณป้อนที่นี่ ระบบจะจัดประเภทสัญญาเช่าเป็นสัญญาเช่าระยะสั้น และการรักษาสัญญาเช่าที่รอการตัดบัญชีจะถูกนำไปใช้</span><span class="sxs-lookup"><span data-stu-id="20dfc-133">If the lease term is less than or equal to the number of months that you enter here, the system will classify the lease as a short-term lease, and the deferred rent treatment will be applied.</span></span> |
    | <span data-ttu-id="20dfc-134">เกณฑ์มูลค่าต่ำ</span><span class="sxs-lookup"><span data-stu-id="20dfc-134">Low value threshold</span></span>                      | <span data-ttu-id="20dfc-135">ป้อนยอดเงินที่จะใช้เป็นขีดจำกัดสำหรับสัญญาเช่ามูลค่าต่ำ</span><span class="sxs-lookup"><span data-stu-id="20dfc-135">Enter an amount to use as a threshold for low-value leases.</span></span> <span data-ttu-id="20dfc-136">ถ้ามูลค่ายุติธรรมของสินทรัพย์มีค่าน้อยกว่าหรือเท่ากับค่าที่คุณป้อนที่นี่ ระบบจะจัดประเภทสัญญาเช่าเป็นสัญญาเช่ามูลค่าต่ำ และการรักษาสัญญาเช่าที่รอการตัดบัญชีจะถูกนำไปใช้</span><span class="sxs-lookup"><span data-stu-id="20dfc-136">If the fair value of the asset is less than or equal or the value that you enter here, the system will classify the lease as a low-value lease, and the deferred rent treatment will be applied.</span></span> |
    | <span data-ttu-id="20dfc-137">จ่ายให้ผู้จัดจำหน่าย</span><span class="sxs-lookup"><span data-stu-id="20dfc-137">Pay to vendor</span></span>                            | <span data-ttu-id="20dfc-138">กำหนดตัวเลือกนี้เป็น **ใช่** เพื่ออนุญาตให้มีการลงรายการบัญชีการชำระเงิน ตามใบแจ้งหนี้ สำหรับบัญชีผู้จัดจำหน่ายที่ระบุไว้ในแต่ละสัญญาเช่า</span><span class="sxs-lookup"><span data-stu-id="20dfc-138">Set this option to **Yes** to allow lease payments to be posted, as an invoice, to the vendor account that is specified on each lease.</span></span> <span data-ttu-id="20dfc-139">เมื่อมีการลงรายการบัญชีการชำระค่าเช่า บัญชีผู้จัดจำหน่ายจะถูกเครดิต</span><span class="sxs-lookup"><span data-stu-id="20dfc-139">When a lease payment is posted, the vendor account will be credited.</span></span> <span data-ttu-id="20dfc-140">ถ้ามีการตั้งค่าตัวเลือกนี้เป็น **ไม่** บัญชีที่ระบุไว้สำหรับชนิดการลงรายการบัญชี **การชำระค่าเช่า** ในหน้า **พารามิเตอร์การลงรายการบัญชีสัญญาเช่า** จะถูกเครดิตแทน</span><span class="sxs-lookup"><span data-stu-id="20dfc-140">If this option is set to **No**, the account that is specified for the **Lease payment** posting type on the **Lease posting parameters** page will be credited instead.</span></span> |
