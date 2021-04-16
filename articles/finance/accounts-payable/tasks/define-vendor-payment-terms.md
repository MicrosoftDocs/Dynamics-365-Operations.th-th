---
title: กำหนดเงื่อนไขการชำระเงินให้แก่ผู้จัดจำหน่าย
description: หัวข้อนี้จะอธิบายวิธีการตั้งค่าเงื่อนไขการชำระเงินสำหรับใบแจ้งหนี้ของผู้จัดจำหน่าย
author: abruer
ms.date: 07/09/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: PaymTerm, CashDisc
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: abruer
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: f47fc0cd67cddef3c73f9c4c6b8dd6f41bbe85ec
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 04/01/2021
ms.locfileid: "5838920"
---
# <a name="define-vendor-payment-terms"></a><span data-ttu-id="11733-103">กำหนดเงื่อนไขการชำระเงินให้แก่ผู้จัดจำหน่าย</span><span class="sxs-lookup"><span data-stu-id="11733-103">Define vendor payment terms</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="11733-104">หัวข้อนี้จะอธิบายวิธีการตั้งค่าเงื่อนไขการชำระเงินสำหรับใบแจ้งหนี้ของผู้จัดจำหน่าย</span><span class="sxs-lookup"><span data-stu-id="11733-104">This topic explains how to set up payment terms for vendor invoices.</span></span> <span data-ttu-id="11733-105">งานนี้ใช้บริษัทสาธิต USMF </span><span class="sxs-lookup"><span data-stu-id="11733-105">This task uses the USMF demo company.</span></span>

1. <span data-ttu-id="11733-106">ไปที่ **บานหน้าต่างนำทาง > โมดูล > บัญชีเจ้าหนี้ > การตั้งค่าการชำระเงิน > เงื่อนไขการชำระเงิน**</span><span class="sxs-lookup"><span data-stu-id="11733-106">Go to **Navigation pane > Modules > Accounts payable > Payment setup > Terms of payment**.</span></span>
2. <span data-ttu-id="11733-107">เลือก **ใหม่**</span><span class="sxs-lookup"><span data-stu-id="11733-107">Select **New**.</span></span> <span data-ttu-id="11733-108">หน้าเงื่อนไขการชำระเงินใช้เพื่อกำหนดการคำนวณวันครบกำหนดชำระ </span><span class="sxs-lookup"><span data-stu-id="11733-108">The Terms of payment page is used to define how the due date will be calculated.</span></span> <span data-ttu-id="11733-109">มันจะไม่กำหนดการคำนวณส่วนลดเงินสด</span><span class="sxs-lookup"><span data-stu-id="11733-109">It is not used to define how the cash discount date will be calculated.</span></span>  
3. <span data-ttu-id="11733-110">ในฟิลด์ **เงื่อนไขการชำระเงิน** ให้พิมพ์ค่า</span><span class="sxs-lookup"><span data-stu-id="11733-110">In the **Terms of payment** field, type a value.</span></span>
4. <span data-ttu-id="11733-111">ใน **ฟิลด์คำอธิบาย** ให้พิมพ์ค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="11733-111">In the **Description field**, type a value.</span></span>
5. <span data-ttu-id="11733-112">ในฟิลด์ **จำนวนวัน** ป้อนตัวเลข</span><span class="sxs-lookup"><span data-stu-id="11733-112">In the **Days** field, enter a number.</span></span> <span data-ttu-id="11733-113">หมายเลขที่ป้อนไว้ที่นี่จะใช้ในการเพิ่มวันครบกำหนดชำระ หรือสิ้นสุดรอบระยะเวลาการชำระเงินในวิธีการชำระเงิน </span><span class="sxs-lookup"><span data-stu-id="11733-113">The number entered here will be used to add to the due date, or to the end of the period identified in the Payment method.</span></span> <span data-ttu-id="11733-114">ตัวอย่างเช่น ถ้าคุณเลือก **สุทธิ** หมายเลขจะถูกเพิ่มลงในวันครบกำหนด</span><span class="sxs-lookup"><span data-stu-id="11733-114">For example, if you select **Net**, the number will be added to the due date.</span></span> <span data-ttu-id="11733-115">ถ้าคุณเลือก **เดือนปัจจุบัน** หมายเลขจะถูกเพิ่มไปวันสุดท้ายของเดือนปัจจุบันเพื่อคำนวณวันครบกำหนดชำระ</span><span class="sxs-lookup"><span data-stu-id="11733-115">If you select **Current month**, it will add the number to the last day of the current month to calculate the due date.</span></span>  
6. <span data-ttu-id="11733-116">เลือก **บันทึก**</span><span class="sxs-lookup"><span data-stu-id="11733-116">Select **Save**.</span></span>
7. <span data-ttu-id="11733-117">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="11733-117">Close the page.</span></span>
8. <span data-ttu-id="11733-118">ไปที่ **บัญชีเจ้าหนี้ > การตั้งค่าการชำระเงิน > ส่วนลดเงินสด**</span><span class="sxs-lookup"><span data-stu-id="11733-118">Go to **Accounts payable > Payment setup > Cash discounts**.</span></span>
9. <span data-ttu-id="11733-119">เลือก **ใหม่**</span><span class="sxs-lookup"><span data-stu-id="11733-119">Select **New**.</span></span>
10. <span data-ttu-id="11733-120">ในฟิลด์ **ส่วนลดเงินสด** ป้อนรหัส</span><span class="sxs-lookup"><span data-stu-id="11733-120">In the **Cash discount** field, enter an ID.</span></span>
11. <span data-ttu-id="11733-121">ในฟิลด์ **คำอธิบาย** ให้พิมพ์ค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="11733-121">In the **Description** field, type a value.</span></span>
12. <span data-ttu-id="11733-122">ถ้าผู้จัดจำหน่ายเสนอส่วนลดที่จัดระดับ เลือกส่วนลดเงินสดถัดไปหลังจากอันปัจจุบันหมดอายุ</span><span class="sxs-lookup"><span data-stu-id="11733-122">If the vendor offers a tiered discount, select the next cash discount after the current one is expired.</span></span>
13. <span data-ttu-id="11733-123">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="11733-123">Close the page.</span></span>
14. <span data-ttu-id="11733-124">ในฟิลด์ **จำนวนวัน** ป้อนตัวเลข</span><span class="sxs-lookup"><span data-stu-id="11733-124">In the **Days** field, enter a number.</span></span> <span data-ttu-id="11733-125">ปริมาณที่ป้อนในฟิลด์ **จำนวนวัน** จะใช้ในการคำนวณวันที่ให้ส่วนลดเงินสด โดยอาศัยตัวเลือกที่เลือกไว้ในฟิลด์ **สุทธิ/ปัจจุบัน**</span><span class="sxs-lookup"><span data-stu-id="11733-125">The quantity entered in the **Days** field will be used to calculate the Cash discount date, based on what option was selected in the **Net/Current** field.</span></span> <span data-ttu-id="11733-126">ถ้ามีการเลือก **สุทธิ** ปริมาณจะถูกเพิ่มในวันที่ในใบแจ้งหนี้เพื่อกำหนดวันที่ให้ส่วนลดเงินสด</span><span class="sxs-lookup"><span data-stu-id="11733-126">If **Net** was selected, the quantity will be added to the invoice date to determine the cash discount date.</span></span> <span data-ttu-id="11733-127">ถ้ามีการเลือก **เดือนปัจจุบัน** ปริมาณจะถูกเพิ่มไปที่วันสุดท้ายของเดือนสกุลเงินเพื่อกำหนดวันที่ให้ส่วนลดเงินสด</span><span class="sxs-lookup"><span data-stu-id="11733-127">If **Current month** was selected, the quantity will be added to the end of the currency month to determine the cash discount date.</span></span>  
15. <span data-ttu-id="11733-128">ป้อนเปอร์เซ็นต์ของส่วนลดเงินสดในฟิลด์ **ส่วนลด**</span><span class="sxs-lookup"><span data-stu-id="11733-128">Enter the percentage of the cash discount in the **Discount** field.</span></span> 
16. <span data-ttu-id="11733-129">ป้อนบัญชีหลักที่จะลงรายการบัญชีส่วนลดเงินสดสำหรับใบแจ้งหนี้ของลูกค้า จากนั้น ป้อนบัญชีหลักที่จะลงรายการบัญชีส่วนลดเงินสดสำหรับใบแจ้งหนี้ของผู้จัดจำหน่าย</span><span class="sxs-lookup"><span data-stu-id="11733-129">Enter the main account to which the cash discount will be posted for customer invoices, then enter the main account to which the cash discount will be posted for vendor invoices.</span></span> <span data-ttu-id="11733-130">ถ้า **บัญชีตรงข้ามส่วนลด** ถูกกำหนดเป็น **ใช้บัญชีหลักสำหรับส่วนลดของผู้จัดจำหน่าย** จากนั้นบัญชีหลักจะถูกใช้</span><span class="sxs-lookup"><span data-stu-id="11733-130">If **Discount offset accounts** is set to **Use main account for vendor discount**, then the Main account will be used.</span></span> <span data-ttu-id="11733-131">ถ้าตัวเลือกถูกตั้งเป็น **บัญชีในรายการใบแจ้งหนี้** ส่วนลดเงินสดจะถูกลงรายการบัญชีสินทรัพย์/ค่าใช้จ่ายในรายการของใบแจ้งหนี้</span><span class="sxs-lookup"><span data-stu-id="11733-131">If the option is set to **Accounts on the invoice lines**, the cash discount will be posted to the asset/expense accounts on the invoice's lines.</span></span>  
17. <span data-ttu-id="11733-132">เลือก **บันทึก**</span><span class="sxs-lookup"><span data-stu-id="11733-132">Select **Save**.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]