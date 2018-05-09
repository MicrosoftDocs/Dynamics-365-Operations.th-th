--- 
title: "กำหนดเงื่อนไขการชำระเงินให้แก่ผู้จัดจำหน่าย"
description: "ตั้งค่าเงื่อนไขการชำระเงินสำหรับใบแจ้งหนี้ของผู้จัดจำหน่าย "
author: abruer
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Operations
ms.search.region: Global
ms.author: abruer
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: 28de122f8742e16731387a63beb12ae774d4d9c1
ms.contentlocale: th-th
ms.lasthandoff: 05/08/2018

---
# <a name="define-vendor-payment-terms"></a><span data-ttu-id="ea408-103">กำหนดเงื่อนไขการชำระเงินให้แก่ผู้จัดจำหน่าย</span><span class="sxs-lookup"><span data-stu-id="ea408-103">Define vendor payment terms</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="ea408-104">ตั้งค่าเงื่อนไขการชำระเงินสำหรับใบแจ้งหนี้ของผู้จัดจำหน่าย </span><span class="sxs-lookup"><span data-stu-id="ea408-104">Set up payment terms for vendor invoices.</span></span> <span data-ttu-id="ea408-105">งานนี้ใช้บริษัทสาธิต USMF </span><span class="sxs-lookup"><span data-stu-id="ea408-105">This task uses the USMF demo company.</span></span>

1. <span data-ttu-id="ea408-106">ไปที่บัญชีเจ้าหนี้ > การตั้งค่าการชำระเงิน > เงื่อนไขการชำระเงิน</span><span class="sxs-lookup"><span data-stu-id="ea408-106">Go to Accounts payable > Payment setup > Terms of payment.</span></span>
2. <span data-ttu-id="ea408-107">คลิก สร้าง</span><span class="sxs-lookup"><span data-stu-id="ea408-107">Click New.</span></span>
    * <span data-ttu-id="ea408-108">หน้าเงื่อนไขการชำระเงินใช้เพื่อกำหนดการคำนวณวันครบกำหนดชำระ </span><span class="sxs-lookup"><span data-stu-id="ea408-108">The Terms of payment page is used to define how the due date will be calculated.</span></span> <span data-ttu-id="ea408-109">มันจะไม่กำหนดการคำนวณส่วนลดเงินสด</span><span class="sxs-lookup"><span data-stu-id="ea408-109">It is not used to define how the cash discount date will be calculated.</span></span>  
3. <span data-ttu-id="ea408-110">ในฟิลด์เงื่อนไขการชำระเงิน ให้พิมพ์ค่า</span><span class="sxs-lookup"><span data-stu-id="ea408-110">In the Terms of payment field, type a value.</span></span>
4. <span data-ttu-id="ea408-111">ในฟิลด์ คำอธิบาย ให้พิมพ์ค่า</span><span class="sxs-lookup"><span data-stu-id="ea408-111">In the Description field, type a value.</span></span>
5. <span data-ttu-id="ea408-112">ในฟิลด์จำนวนวัน ป้อนตัวเลข</span><span class="sxs-lookup"><span data-stu-id="ea408-112">In the Days field, enter a number.</span></span>
    * <span data-ttu-id="ea408-113">หมายเลขที่ป้อนไว้ที่นี่จะใช้ในการเพิ่มวันครบกำหนดชำระ หรือสิ้นสุดรอบระยะเวลาการชำระเงินในวิธีการชำระเงิน </span><span class="sxs-lookup"><span data-stu-id="ea408-113">The number entered here will be used to add to the due date, or to the end of the period identified in the Payment method.</span></span> <span data-ttu-id="ea408-114">ตัวอย่างเช่น ถ้าคุณเลือกสุทธิ หมายเลขจะถูกเพิ่มลงในวันครบกำหนด </span><span class="sxs-lookup"><span data-stu-id="ea408-114">For example, if you select Net, the number will be added to the due date.</span></span> <span data-ttu-id="ea408-115">ถ้าคุณเลือกเดือนปัจจุบัน หมายเลขจะถูกเพิ่มไปวันสุดท้ายของเดือนปัจจุบันเพื่อคำนวณวันครบกำหนดชำระ</span><span class="sxs-lookup"><span data-stu-id="ea408-115">If you select Current month, it will add the number to the last day of the current month to calculate the due date.</span></span>  
6. <span data-ttu-id="ea408-116">คลิก บันทึก</span><span class="sxs-lookup"><span data-stu-id="ea408-116">Click Save.</span></span>
7. <span data-ttu-id="ea408-117">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="ea408-117">Close the page.</span></span>
8. <span data-ttu-id="ea408-118">ไปที่บัญชีลูกหนี้ > การตั้งค่าการชำระเงิน > ส่วนลดเงินสด</span><span class="sxs-lookup"><span data-stu-id="ea408-118">Go to Accounts payable > Payment setup > Cash discounts.</span></span>
9. <span data-ttu-id="ea408-119">คลิก สร้าง</span><span class="sxs-lookup"><span data-stu-id="ea408-119">Click New.</span></span>
10. <span data-ttu-id="ea408-120">ในฟิลด์ส่วนลดเงินสด ป้อน ID</span><span class="sxs-lookup"><span data-stu-id="ea408-120">In the Cash discount field, enter an ID.</span></span>
11. <span data-ttu-id="ea408-121">ในฟิลด์ คำอธิบาย ให้พิมพ์ค่า</span><span class="sxs-lookup"><span data-stu-id="ea408-121">In the Description field, type a value.</span></span>
12. <span data-ttu-id="ea408-122">ถ้าผู้จัดจำหน่ายเสนอส่วนลดที่จัดระดับ เลือกส่วนลดเงินสดถัดไปหลังจากอันปัจจุบันหมดอายุ</span><span class="sxs-lookup"><span data-stu-id="ea408-122">If the vendor offers a tiered discount, select the next cash discount after the current one is expired.</span></span>
13. <span data-ttu-id="ea408-123">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="ea408-123">Close the page.</span></span>
14. <span data-ttu-id="ea408-124">ในฟิลด์จำนวนวัน ป้อนตัวเลข</span><span class="sxs-lookup"><span data-stu-id="ea408-124">In the Days field, enter a number.</span></span>
    * <span data-ttu-id="ea408-125">ปริมาณที่ป้อนในฟิลด์จำนวนวันจะใช้ในการคำนวณวันที่ให้ส่วนลดเงินสด โดยอาศัยตัวเลือกที่เลือกไว้ในฟิลด์สุทธิ/ปัจจุบัน </span><span class="sxs-lookup"><span data-stu-id="ea408-125">The quantity entered in the Days field will be used to calculate the Cash discount date, based on what option was selected in the Net/Current field.</span></span> <span data-ttu-id="ea408-126">ถ้าเลือกสุทธิ ปริมาณจะเพิ่มในวันที่ใบแจ้งหนี้เพื่อกำหนดวันที่ให้ส่วนลดเงินสด </span><span class="sxs-lookup"><span data-stu-id="ea408-126">If Net was selected, the quantity will be added to the invoice date to determine the cash discount date.</span></span> <span data-ttu-id="ea408-127">ถ้าเลือกเดือนปัจจุบัน ปริมาณจะถูกเพิ่มไปที่วันสุดท้ายของเดือนสกุลเงินเพื่อกำหนดวันที่ให้ส่วนลดเงินสด</span><span class="sxs-lookup"><span data-stu-id="ea408-127">If Current month was selected, the quantity will be added to the end of the currency month to determine the cash discount date.</span></span>  
15. <span data-ttu-id="ea408-128">ป้อนเปอร์เซ็นต์ของส่วนลดเงินสดในฟิลด์ส่วนลด</span><span class="sxs-lookup"><span data-stu-id="ea408-128">Enter the percentage of the cash discount in the Discount field.</span></span> 
16. <span data-ttu-id="ea408-129">ป้อนบัญชีหลักที่ส่วนลดเงินสดจะลงรายการบัญชีสำหรับใบแจ้งหนี้ของลูกค้า</span><span class="sxs-lookup"><span data-stu-id="ea408-129">Enter the main account to which the cash discount will be posted for customer invoices.</span></span>
17. <span data-ttu-id="ea408-130">ป้อนบัญชีหลักที่ส่วนลดเงินสดจะลงรายการบัญชีสำหรับใบแจ้งหนี้ของลูกค้า</span><span class="sxs-lookup"><span data-stu-id="ea408-130">Enter the main account to which the cash discount will be posted for vendor invoices.</span></span>
    * <span data-ttu-id="ea408-131">ถ้า 'บัญชีตรงข้ามส่วนลด' ถูกกำหนดเป็นการใช้บัญชีหลักสำหรับส่วนลดของผู้จัดจำหน่าย จากนั้นบัญชีหลักจะถูกใช้ </span><span class="sxs-lookup"><span data-stu-id="ea408-131">If 'Discount offset accounts' is set to Use main account for vendor discount, then the Main account will be used.</span></span>  <span data-ttu-id="ea408-132">ถ้าตัวเลือกถูกตั้งเป็นบัญชีในรายการใบแจ้งหนี้ ส่วนลดเงินสดจะถูกลงรายการบัญชีสินทรัพย์/ค่าใช้จ่ายในรายการใบแจ้งหนี้</span><span class="sxs-lookup"><span data-stu-id="ea408-132">If the option is set to Accounts on the invoice lines, the cash discount will be posted to the asset/expense accounts on the invoice's lines.</span></span>  
18. <span data-ttu-id="ea408-133">คลิก บันทึก</span><span class="sxs-lookup"><span data-stu-id="ea408-133">Click Save.</span></span>


