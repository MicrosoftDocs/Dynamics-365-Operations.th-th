---
title: " สร้างใบสั่งศูนย์บริการ"
description: 'ขั้นตอนนี้จะสอนให้ค้นหาลูกค้า สร้างใบสั่งใหม่ ค้นหาผลิตภัณฑ์และรวบรวมการชำระเงินจากลูกค้า '
author: josaw1
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: MCRCustomerService, SalesTable, MCRSourceIdTargetLookup, MCRSalesQuickQuote, MCRSalesOrderRecap, MCRCustPaymDialog, MCRCustPaymLookup
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: c875eaa85d9da997b75b296ad9ace99ae1e91798
ms.sourcegitcommit: 597476103bb695e3cbe6d9ffcd7a466400346636
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 11/20/2020
ms.locfileid: "4594247"
---
# <a name="create-call-center-orders"></a><span data-ttu-id="41c94-103"> สร้างใบสั่งศูนย์บริการ</span><span class="sxs-lookup"><span data-stu-id="41c94-103">Create call center orders</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="41c94-104">ขั้นตอนนี้จะสอนให้ค้นหาลูกค้า สร้างใบสั่งใหม่ ค้นหาผลิตภัณฑ์และรวบรวมการชำระเงินจากลูกค้า </span><span class="sxs-lookup"><span data-stu-id="41c94-104">This procedure walks through looking up a customer, creating a new order, searching for a product, and collecting payment from the customer.</span></span> <span data-ttu-id="41c94-105">ขั้นตอนนี้ใช้บริษัทข้อมูลสาธิต USRT และมีไว้สำหรับเจ้าหน้าที่ดูแลใบสั่งขาย </span><span class="sxs-lookup"><span data-stu-id="41c94-105">This procedure uses demo data company USRT and is intended for the Sales Order Clerk.</span></span> <span data-ttu-id="41c94-106">ความต้องการเบื้องต้น:  ผู้ใช้ที่ดำเนินการขั้นตอนนี้จะต้องถูกตั้งค่าเป็นผู้ใช้ศูนย์บริการ และแค็ตตาล็อกประจำครึ่งปี Fabrikam จะถูกเผยแพร่พร้อมกับหนึ่งรหัสแหล่งที่เป็นอย่างต่ำ</span><span class="sxs-lookup"><span data-stu-id="41c94-106">Pre-requisites:  The user who completes the procedure is set up as a Call center user and the Fabrikam Semi-Annual Catalog is published with at least one Source code on it.</span></span>

1. <span data-ttu-id="41c94-107">ไปที่ **Retail และ Commerce \> ลูกค้า \> บริการลูกค้า**</span><span class="sxs-lookup"><span data-stu-id="41c94-107">Go to **Retail and Commerce \> Customers \> Customer service**.</span></span>
2. <span data-ttu-id="41c94-108">สำหรับ **คำที่ใช้ค้นหา** ให้ป้อนเงื่อนไขการค้นหาเพื่อค้นหาลูกค้า</span><span class="sxs-lookup"><span data-stu-id="41c94-108">For **SearchText**, enter the search criteria to look up the customer.</span></span>
    * <span data-ttu-id="41c94-109">สำหรับกระบวนงานตัวอย่างนี้ ให้พิมพ์ "Karen" และเลือก **แท็บ**</span><span class="sxs-lookup"><span data-stu-id="41c94-109">For this example procedure, enter "Karen" and select **Tab**.</span></span>  
3. <span data-ttu-id="41c94-110">เลือก ค้นหา</span><span class="sxs-lookup"><span data-stu-id="41c94-110">Select Search.</span></span>
    * <span data-ttu-id="41c94-111">เนื่องจากมีลูกค้าเพียงคนเดียวที่ชื่อ "Karen" ในข้อมูลสาธิต ผลลัพธ์จะถูกเลือกโดยอัตโนมัติ</span><span class="sxs-lookup"><span data-stu-id="41c94-111">Since there is only one customer named "Karen" in demo data, the result will be automatically selected.</span></span>  
4. <span data-ttu-id="41c94-112">เลือก **ใบสั่งขายใหม่**</span><span class="sxs-lookup"><span data-stu-id="41c94-112">Select **New sales order**.</span></span>
5. <span data-ttu-id="41c94-113">ขยายหรือยุบส่วนหัวของ **ใบสั่งขาย**</span><span class="sxs-lookup"><span data-stu-id="41c94-113">Expand or collapse the **Sales order** header section.</span></span>
6. <span data-ttu-id="41c94-114">เลือกรหัสแหล่งที่มาสำหรับแค็ตตาล็อก</span><span class="sxs-lookup"><span data-stu-id="41c94-114">Select the source code for the catalog.</span></span>
    * <span data-ttu-id="41c94-115">ถ้าหากว่าไม่มีรหัสแหล่งที่มาที่เปิดใช้งานอยู่ คุณสามารถข้ามขั้นตอนนี้ไปได้</span><span class="sxs-lookup"><span data-stu-id="41c94-115">If there are no active source codes you can skip this step.</span></span>  
7. <span data-ttu-id="41c94-116">เลือก **เพิ่มรายการ**</span><span class="sxs-lookup"><span data-stu-id="41c94-116">Select **Add line**.</span></span>
8. <span data-ttu-id="41c94-117">สำหรับ **หมายเลขสินค้า** ให้ป้อนเงื่อนไขการค้นหาสินค้า</span><span class="sxs-lookup"><span data-stu-id="41c94-117">For **Item number**, enter the item search term.</span></span>
    * <span data-ttu-id="41c94-118">สำหรับกระบวนงานตัวอย่างนี้ ให้ป้อนหมายเลขสินค้าบางส่วนเป็น '8111' และกดแท็บ การดำเนินการนี้จะทำให้หน้าต่างการค้นหาสินค้าเด้งขึ้นมา</span><span class="sxs-lookup"><span data-stu-id="41c94-118">For this sample procedure, enter a partial item number of '8111' and press tab. This action will bring up the item search window.</span></span>  
9. <span data-ttu-id="41c94-119">เลือกผลิตภัณฑ์ที่จะเพิ่มในใบสั่งขาย</span><span class="sxs-lookup"><span data-stu-id="41c94-119">Select the product to add to the sales order.</span></span>
10. <span data-ttu-id="41c94-120">ป้อนปริมาณการขาย</span><span class="sxs-lookup"><span data-stu-id="41c94-120">Enter the sales quantity.</span></span>
11. <span data-ttu-id="41c94-121">เลือก **สร้าง**</span><span class="sxs-lookup"><span data-stu-id="41c94-121">Select **Create**.</span></span>
12. <span data-ttu-id="41c94-122">เลือก **เสร็จสมบูรณ์** เพื่อรวบรวมข้อมูลการชำระเงินของลูกค้า</span><span class="sxs-lookup"><span data-stu-id="41c94-122">Select **Complete** to capture the customer payment.</span></span>
13. <span data-ttu-id="41c94-123">เลือก **เพิ่ม**</span><span class="sxs-lookup"><span data-stu-id="41c94-123">Select **Add**.</span></span>
    * <span data-ttu-id="41c94-124">เพิ่มการเชื่อมโยง จะอยู่ในแท็บการชำระเงิน ให้ขยายแท็บการชำระเงินถ้ามันถูกยุบอยู่</span><span class="sxs-lookup"><span data-stu-id="41c94-124">The Add link is in the Payments tab. Expand the Payments tab if it is collapsed.</span></span>  
14. <span data-ttu-id="41c94-125">เลือกวิธีการชำระเงิน</span><span class="sxs-lookup"><span data-stu-id="41c94-125">Select the payment method.</span></span>
    * <span data-ttu-id="41c94-126">สำหรับขั้นตอนนี้ ให้เลือกวิธีการชำระเงินสด</span><span class="sxs-lookup"><span data-stu-id="41c94-126">For this procedure, select the cash payment method.</span></span>  
15. <span data-ttu-id="41c94-127">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="41c94-127">Close the page.</span></span>
16. <span data-ttu-id="41c94-128">ป้อนจำนวน</span><span class="sxs-lookup"><span data-stu-id="41c94-128">Enter the amount.</span></span>
    * <span data-ttu-id="41c94-129">สำหรับกระบวนงานนี้ ให้ป้อนยอดเงินเท่ากับยอดดุลใบสั่งซึ่งสามารถดูได้ในหน้าสรุปใบสั่งขายทางด้านซ้ายของฟิลด์ยอดเงิน</span><span class="sxs-lookup"><span data-stu-id="41c94-129">For this procedure, enter an amount equal to the order balance that can be seen in the Sales order summary page to the left of the amount field.</span></span> <span data-ttu-id="41c94-130">การดำเนินการนี้จะทำให้คุณสามารถดำเนินการใบสั่งจนเสร็จสิ้นเป็นชำระครบถ้วนแล้ว</span><span class="sxs-lookup"><span data-stu-id="41c94-130">This action will allow you to complete the order as fully paid.</span></span>  
17. <span data-ttu-id="41c94-131">เลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="41c94-131">Select **OK**.</span></span>
18. <span data-ttu-id="41c94-132">เลือก **ส่ง**</span><span class="sxs-lookup"><span data-stu-id="41c94-132">Select **Submit**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="41c94-133">ทรัพยากรเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="41c94-133">Additional resources</span></span>

[<span data-ttu-id="41c94-134">กำหนดอีเมลของธุรกรรมตามวิธีการจัดส่ง</span><span class="sxs-lookup"><span data-stu-id="41c94-134">Customize transactional emails by mode of delivery</span></span>](../customize-email-delivery-mode.md)

[<span data-ttu-id="41c94-135">เปลี่ยนวิธีการจัดส่งใน POS</span><span class="sxs-lookup"><span data-stu-id="41c94-135">Change mode of delivery in POS</span></span>](../pos-change-delivery-mode.md)

