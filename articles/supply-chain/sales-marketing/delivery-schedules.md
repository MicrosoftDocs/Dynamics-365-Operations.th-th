---
title: "กำหนดการจัดส่ง"
description: "กำหนดการจัดส่งช่วยให้คุณสามารถติดตามปริมาณในบรรทัดใบสั่งเมื่อคุณใช้การจัดส่งหลายครั้ง สำหรับใบสั่งขาย ใบเสนอราคาขาย ใบสั่งซื้อเดียว"
author: YuyuScheller
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: PurchDeliverySchedule, SalesDeliverySchedule, SalesQuotationDeliverySchedule
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 213984
ms.assetid: 44cac104-c36c-4371-a992-9178b3fd65e9
ms.search.region: Global
ms.author: omulvad
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: 08c38aada355583c5a6872f75b57db95d9b81786
ms.openlocfilehash: 84ae84a567e5f45bc0b20538d04917c6feb21336
ms.contentlocale: th-th
ms.lasthandoff: 07/18/2017

---

# <a name="delivery-schedules"></a><span data-ttu-id="fccd2-103">กำหนดการจัดส่ง</span><span class="sxs-lookup"><span data-stu-id="fccd2-103">Delivery schedules</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="fccd2-104">กำหนดการจัดส่งช่วยให้คุณสามารถติดตามปริมาณในบรรทัดใบสั่งเมื่อคุณใช้การจัดส่งหลายครั้ง สำหรับใบสั่งขาย ใบเสนอราคาขาย ใบสั่งซื้อเดียว</span><span class="sxs-lookup"><span data-stu-id="fccd2-104">Delivery schedules allow you to track order line quantity when you are using multiple deliveries for a single sales order, sales quotation, or purchase order.</span></span>

<span data-ttu-id="fccd2-105">ใช้กำหนดการจัดส่งเมื่อปริมาณในรายการใบสั่งหรือใบเสนอราคาทั้งหมดต้องถูกจัดส่งในการจัดส่งหลายครั้ง</span><span class="sxs-lookup"><span data-stu-id="fccd2-105">Use a delivery schedule when the total quantity on an order or quotation line must be delivered in multiple shipments.</span></span> <span data-ttu-id="fccd2-106">การจัดส่งแต่ละครั้งจะแสดงรายการจัดส่ง</span><span class="sxs-lookup"><span data-stu-id="fccd2-106">Individual shipments are represented by delivery lines.</span></span> <span data-ttu-id="fccd2-107">รายการการจัดส่งอย่างน้อยสองรายการจะทำให้เป็นกำหนดการการจัดส่งเดียว</span><span class="sxs-lookup"><span data-stu-id="fccd2-107">Two or more delivery lines make up one delivery schedule.</span></span> <span data-ttu-id="fccd2-108">รายการจัดส่งสามารถมีวันจัดส่ง ปริมาณ วิธีการจัดส่ง และมิติการจัดเก็บ ที่แตกต่างกัน เช่น ไซต์และคลังสินค้า</span><span class="sxs-lookup"><span data-stu-id="fccd2-108">The delivery lines can have different delivery dates, quantities, modes of delivery, and storage dimensions, such as site and warehouse.</span></span>  

<span data-ttu-id="fccd2-109">**ตัวอย่างของกำหนดการจัดส่ง**</span><span class="sxs-lookup"><span data-stu-id="fccd2-109">**Example of a delivery schedule**</span></span>

|                                   |                                          |
|-----------------------------------|------------------------------------------|
| <span data-ttu-id="fccd2-110">ใบสั่งรวม (รายการใบสั่งต้นฉบับ)</span><span class="sxs-lookup"><span data-stu-id="fccd2-110">Total order (original order line)</span></span> | <span data-ttu-id="fccd2-111">เก้าอี้ 600 ตัว</span><span class="sxs-lookup"><span data-stu-id="fccd2-111">600 chairs</span></span>                               |
| <span data-ttu-id="fccd2-112">กำหนดวันจัดส่งที่ร้องขอ:</span><span class="sxs-lookup"><span data-stu-id="fccd2-112">Requested delivery schedule</span></span>       | <span data-ttu-id="fccd2-113">เก้าอี้ 100 ตัวต่อเดือน</span><span class="sxs-lookup"><span data-stu-id="fccd2-113">100 chairs per month</span></span>                     |
| <span data-ttu-id="fccd2-114">กรอบเวลาจัดส่งที่ร้องขอ</span><span class="sxs-lookup"><span data-stu-id="fccd2-114">Requested time frame for delivery</span></span> | <span data-ttu-id="fccd2-115">6 เดือน ในวันแรกของแต่ละเดือน</span><span class="sxs-lookup"><span data-stu-id="fccd2-115">6 months, on the first day of each month</span></span> |

<span data-ttu-id="fccd2-116">ในสถานการณ์นี้ ลูกค้าร้องขอการจัดส่งของเก้าอี้ 600 ตัว ในชุดงานของเก้าอี้ 100 ตัว เกินรอบระยะเวลาหกเดือน</span><span class="sxs-lookup"><span data-stu-id="fccd2-116">In this scenario, the customer requests delivery of 600 chairs in batches of 100 chairs over a period of six months.</span></span> <span data-ttu-id="fccd2-117">การติดตามความต้องการจัดส่ง คุณต้องสร้างกำหนดการจัดส่ง</span><span class="sxs-lookup"><span data-stu-id="fccd2-117">To keep track of the delivery requirements, you create a delivery schedule.</span></span> <span data-ttu-id="fccd2-118">ในหน้ากำหนดการจัดส่ง คุณสร้างรายการจัดส่งแยกต่างหากหกรายการ</span><span class="sxs-lookup"><span data-stu-id="fccd2-118">On the delivery schedule page, you create six separate delivery lines.</span></span> <span data-ttu-id="fccd2-119">แต่ละรายการการจัดส่งประกอบด้วยเก้าอี้ 100 ตัว และระบุวันจัดส่งสำหรับเก้าอี้ 100 ตัวเหล่านั้น</span><span class="sxs-lookup"><span data-stu-id="fccd2-119">Each delivery line contains 100 chairs and indicates the delivery date for those 100 chairs.</span></span> <span data-ttu-id="fccd2-120">ในกรณีนี้ แต่ละรายการออฟเซ็ตในวันที่หนึ่งของเดือนสำหรับหกเดือนที่ต่อเนื่องกัน</span><span class="sxs-lookup"><span data-stu-id="fccd2-120">In this case, each line is offset on the first of the month for six consecutive months.</span></span>  

<span data-ttu-id="fccd2-121">เมื่อคุณสร้างการจัดกำหนดการจัดส่ง ชนิดของรายการใบสั่งดั้งเดิมจะถูกเปลี่ยนโดยอัตโนมัติเป็น **รายการสั่งที่มีการจัดส่งหลายครั้ง**</span><span class="sxs-lookup"><span data-stu-id="fccd2-121">When you create a delivery schedule, the type of the original order line is automatically changed to **Order line with multiple deliveries**.</span></span> <span data-ttu-id="fccd2-122">รายการชนิดนี้จะถูกอ้างถึงเป็นรายการการค้า และถูกทำเครื่องหมายด้วยไอคอน</span><span class="sxs-lookup"><span data-stu-id="fccd2-122">A line of this type is referred to as a commercial line and is marked by an icon.</span></span> <span data-ttu-id="fccd2-123">รายการจัดส่งถูกทำเครื่องหมายด้วยไอคอน</span><span class="sxs-lookup"><span data-stu-id="fccd2-123">The delivery line is marked by a different icon.</span></span> <span data-ttu-id="fccd2-124">ถ้าคุณเปลี่ยนปริมาณในรายการจัดส่ง รายการการค้าถูกอัพเดตเป็นปริมาณรวมของกำหนดการจัดส่ง</span><span class="sxs-lookup"><span data-stu-id="fccd2-124">If you change a quantity on a delivery line, the commercial line is updated to the total quantity of the delivery schedule.</span></span> <span data-ttu-id="fccd2-125">ถ้าข้อตกลงทางการค้ามีกำหนดส่วนลดรวมสำหรับใบสั่ง กำหนดการจัดส่งจะช่วยให้มั่นใจว่าใบสั่งของคุณมีสิทธิ์ได้รับส่วนลดรวมในใบสั่ง แม้ว่าใบสั่งจะมีการแยกการจัดส่งก็ตาม</span><span class="sxs-lookup"><span data-stu-id="fccd2-125">If a trade agreement has defined a total discount for the order, the delivery schedule ensures that your order is eligible for the total order discount, even when the order is split into separate deliveries.</span></span>  

<span data-ttu-id="fccd2-126">ใบสั่งที่มีกำหนดการจัดส่งทีถูกประมวลผลแล้วสำหรับรายการการจัดส่ง</span><span class="sxs-lookup"><span data-stu-id="fccd2-126">Orders that have a delivery schedule are processed against the delivery lines.</span></span> <span data-ttu-id="fccd2-127">การประมวลผลรวมถึงการลงรายการบัญชีบันทึกการจัดส่ง ใบรับสินค้า และการออกใบแจ้งหนี้</span><span class="sxs-lookup"><span data-stu-id="fccd2-127">Processing includes the posting of packing slips, product receipts, and invoicing.</span></span>  

<span data-ttu-id="fccd2-128">พิมพ์เอกสารของใบสั่งและใบเสนอราคาที่มีกำหนดการจัดส่งแสดงเฉพาะรายการจัดส่ง</span><span class="sxs-lookup"><span data-stu-id="fccd2-128">Document printouts of orders and quotations that have a delivery schedule show only the delivery lines.</span></span> <span data-ttu-id="fccd2-129">ซึงจะไม่แสดงรายการเดิม (รายการการค้า)</span><span class="sxs-lookup"><span data-stu-id="fccd2-129">They don't show the original lines (commercial lines).</span></span> <span data-ttu-id="fccd2-130">**หมายเหตุ:** นอกจากนี้ ระบบจะแสดงเฉพาะรายการจัดส่งเมื่อคุณทำการดำเนินการเหล่านี้:</span><span class="sxs-lookup"><span data-stu-id="fccd2-130">**Note:** In addition, only the delivery lines are shown when you perform these actions:</span></span>

-   <span data-ttu-id="fccd2-131">โพสต์</span><span class="sxs-lookup"><span data-stu-id="fccd2-131">Post</span></span>
-   <span data-ttu-id="fccd2-132">คัดลอกหน้า</span><span class="sxs-lookup"><span data-stu-id="fccd2-132">Copy pages</span></span>
-   <span data-ttu-id="fccd2-133">เลือกดูหน้ารายการและรายงาน</span><span class="sxs-lookup"><span data-stu-id="fccd2-133">Browse list pages and reports</span></span>

<span data-ttu-id="fccd2-134">เมื่อคุณยืนยันใบเสนอราคาขาย ผลลัพธ์ใบสั่งขายจะแสดงกำหนดการจัดส่งทั้งหมด แม้แต่รายการใบสั่งที่มีการจัดส่งหลายครั้ง</span><span class="sxs-lookup"><span data-stu-id="fccd2-134">When you confirm sales quotations, the resulting sales orders show the whole delivery schedule, even the order lines that have multiple deliveries.</span></span> <span data-ttu-id="fccd2-135">นอกจากนี้ กำหนดการจัดส่งทั้งหมดจะแสดงขึ้นในหน้าทั้งหมดหลัก เช่น ใบสั่งขาย ใบเสนอราคาขาย ใบสั่งซื้อ</span><span class="sxs-lookup"><span data-stu-id="fccd2-135">In addition, the whole delivery schedule is shown on all the major pages, such as sales orders, sales quotations, and purchase orders.</span></span>




