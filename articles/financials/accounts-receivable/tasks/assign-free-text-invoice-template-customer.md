---
title: กำหนดเท็มเพลตใบแจ้งหนี้ข้อความอิสระของลูกค้า
description: 'การทำงานนี้จะแสดงวิธีการกำหนดเท็มเพลตใบแจ้งหนี้ข้อความอิสระให้กับลูกค้า '
author: ShivamPandey-msft
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CustTable, CustRecurrenceInvoice
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 317b3bd4c1f395987ef3dbbd268c40be5c688320
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 01/29/2019
ms.locfileid: "318936"
---
# <a name="assign-free-text-invoice-template-to-a-customer"></a><span data-ttu-id="c097a-103">กำหนดเท็มเพลตใบแจ้งหนี้ข้อความอิสระของลูกค้า</span><span class="sxs-lookup"><span data-stu-id="c097a-103">Assign free text invoice template to a customer</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="c097a-104">การทำงานนี้จะแสดงวิธีการกำหนดเท็มเพลตใบแจ้งหนี้ข้อความอิสระให้กับลูกค้า </span><span class="sxs-lookup"><span data-stu-id="c097a-104">This task demonstrates how to assign a free text invoice template to a customer.</span></span> <span data-ttu-id="c097a-105">การทำงานนี้ใช้บริษัทสาธิต USMF และมีไว้สำหรับผู้ใช้ที่รับผิดชอบการจัดการและประมวลผลใบแจ้งหนี้ A/R</span><span class="sxs-lookup"><span data-stu-id="c097a-105">This task uses the USMF demo company and is intended for the user who is responsible for managing and processing A/R invoices.</span></span>

1. <span data-ttu-id="c097a-106">ไปที่บัญชีลูกหนี้ > ลูกค้า > ลูกค้าทั้งหมด</span><span class="sxs-lookup"><span data-stu-id="c097a-106">Go to Accounts receivable > Customers > All customers.</span></span>
2. <span data-ttu-id="c097a-107">ในรายการนี้ ให้ค้นหาและเลือกเรกคอร์ดที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="c097a-107">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="c097a-108">ในบานหน้าต่างการดำเนินการ คลิก ใบแจ้งหนี้</span><span class="sxs-lookup"><span data-stu-id="c097a-108">On the Action Pane, click Invoice.</span></span>
4. <span data-ttu-id="c097a-109">คลิก รายการใบแจ้งหนี้ที่เกิดซ้ำ</span><span class="sxs-lookup"><span data-stu-id="c097a-109">Click Recurring invoices.</span></span>
    * <span data-ttu-id="c097a-110">ใช้หน้านี้เพื่อการกำหนดเท็มเพลตใบแจ้งหนี้ข้อความอิสระให้กับลูกค้า และระบุความถี่ในการส่งใบแจ้งหนี้ให้กับลูกค้า</span><span class="sxs-lookup"><span data-stu-id="c097a-110">Use this page to assign free text invoice templates to customers and specify how frequently invoices will be sent to the customer.</span></span>  
5. <span data-ttu-id="c097a-111">คลิก สร้างใหม่ เพื่อกำหนดเท็มเพลตใหม่ให้กับลูกค้า</span><span class="sxs-lookup"><span data-stu-id="c097a-111">Click New to assign a new template to the customer.</span></span>
6. <span data-ttu-id="c097a-112">เลือกเท็มเพลตใบแจ้งหนี้ข้อความอิสระที่คุณต้องการกำหนดให้กับลูกค้า</span><span class="sxs-lookup"><span data-stu-id="c097a-112">Select the free text invoice template you want to assign to the customer.</span></span>
7. <span data-ttu-id="c097a-113">ในรายการนี้ ให้ค้นหาและเลือกเรกคอร์ดที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="c097a-113">In the list, find and select the desired record.</span></span>
8. <span data-ttu-id="c097a-114">ในรายการนี้ ให้คลิกลิงค์ในแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="c097a-114">In the list, click the link in the selected row.</span></span>
9. <span data-ttu-id="c097a-115">ป้อนวันที่จะสร้างใบแจ้งหนี้ใบแรก</span><span class="sxs-lookup"><span data-stu-id="c097a-115">Enter the date when the first invoice will be generated.</span></span>
    * <span data-ttu-id="c097a-116">ป้อนวันสิ้นสุดที่เกิดซ้ำ</span><span class="sxs-lookup"><span data-stu-id="c097a-116">Enter a recurring end date.</span></span>  
    * <span data-ttu-id="c097a-117">เลือกอย่างใดอย่างหนึ่งต่อไปนี้: ไม่มีวันสิ้นสุด – ใบแจ้งหนี้จะถูกสร้างขึ้นอย่างไม่มีกำหนดจนกว่าเท็มเพลตที่จะถูกลบออกจากบัญชีลูกค้า</span><span class="sxs-lookup"><span data-stu-id="c097a-117">Select one of the following: No end date – Invoices will be generated indefinitely until the template is removed from the customer account.</span></span>  <span data-ttu-id="c097a-118">วันที่สิ้นสุดของการเรียกเก็บเงิน – เลือกตัวเลือกนี้ แล้วป้อนวันสุดท้ายที่สามารถสร้างใบแจ้งหนี้</span><span class="sxs-lookup"><span data-stu-id="c097a-118">Billing end date – Select this option and enter the last date that the invoice can be generated.</span></span>  
    * <span data-ttu-id="c097a-119">ยอดเงินสะสมสูงสุดหลังจากที่มีการสร้างใบแจ้งหนี้ใดๆ จะหยุดลง</span><span class="sxs-lookup"><span data-stu-id="c097a-119">Maximum cumulative amount after which invoice generation will stop.</span></span>  
    * <span data-ttu-id="c097a-120">ป้อนยอดเงินสะสมสูงสุดที่สามารถเข้าถึงได้โดยใช้เท็มเพลตที่เลือก </span><span class="sxs-lookup"><span data-stu-id="c097a-120">Enter the maximum cumulative amount that can be reached using the selected template.</span></span> <span data-ttu-id="c097a-121">ตัวอย่างเช่น ถ้าคุณป้อน 1,000.00 และสร้างใบแจ้งหนี้รายเดือน เดือนละ 100.00 ใบแจ้งหนี้จะหยุดการสร้างหลังจากมีสร้างใบแจ้งหนี้ครบสิบ</span><span class="sxs-lookup"><span data-stu-id="c097a-121">For example, if you enter 1,000.00 and generate monthly invoices for 100.00 each, invoices will stop generating after the tenth invoice is generated.</span></span>  
    * <span data-ttu-id="c097a-122">สร้างใบแจ้งหนี้ที่เกิดซ้ำ โดยใช้ค่าเริ่มต้นจากเท็มเพลใบแจ้งหนี้ข้อความอิสระหรือบัญชีลูกค้า</span><span class="sxs-lookup"><span data-stu-id="c097a-122">Generate recurring invoices by using the default values from either free text invoice template or the customer account.</span></span>  
    * <span data-ttu-id="c097a-123">เลือกว่าจะใช้เท็มเพลตใบแจ้งหนี้ข้อความอิสระหรือรหัสลูกค้าเพื่อกำหนดค่าเริ่มต้นสำหรับภาษาที่ใช้ การลงรายการบัญชีโพรไฟล์ กลุ่มภาษีขาย กลุ่มภาษีขายตามประเภทสินค้า รายการรหัส ประเทศ/ภูมิภาคสำหรับการจัดส่ง สกุลเงิน เงื่อนไขการชำระเงิน วิธีการชำระเงิน ข้อมูลจำเพาะเกี่ยวกับการชำระเงิน กำหนดการชำระเงิน ส่วนลดเงินสด มิติทางการเงิน และสลิปการโอนย้ายอดเงินเมื่อสร้างใบแจ้งหนี้</span><span class="sxs-lookup"><span data-stu-id="c097a-123">Select whether to use the free text invoice template or the customer account to determine the default values for the language, posting profile, sales tax group, item sales tax group, list code, country/region for delivery, currency, terms of payment, method of payment, payment specification, payment schedule, cash discount, financial dimensions, and giro money transfer slip when invoices are created.</span></span>  
10. <span data-ttu-id="c097a-124">เลือกรูปแบบการเกิดซ้ำ </span><span class="sxs-lookup"><span data-stu-id="c097a-124">Select the recurrence pattern.</span></span>
    * <span data-ttu-id="c097a-125">รายวัน - เลือกตัวเลือกนี้และป้อนจำนวนวันในฟิลด์ ต่อ </span><span class="sxs-lookup"><span data-stu-id="c097a-125">Daily – Select this option and enter the number of days in the Per field.</span></span> <span data-ttu-id="c097a-126">ตัวอย่างเช่น ถ้าคุณป้อนเลข 15 ใบแจ้งหนี้จะถูกสร้างทุกๆ 15 วันสำหรับลูกค้ารายนี้ </span><span class="sxs-lookup"><span data-stu-id="c097a-126">For example, if you enter 15, an invoice will be generated every 15 days for this customer.</span></span>  <span data-ttu-id="c097a-127">รายสัปดาห์ - เลือกตัวเลือกนี้และป้อนจำนวนสัปดาห์ในฟิลด์ ต่อ </span><span class="sxs-lookup"><span data-stu-id="c097a-127">Weekly - Select this option and enter the number of weeks in the Per field.</span></span> <span data-ttu-id="c097a-128">ตัวอย่างเช่น ถ้าคุณป้อนเลข 2 ใบแจ้งหนี้จะถูกสร้างทุกๆสองสัปดาห์สำหรับลูกค้ารายนี้ </span><span class="sxs-lookup"><span data-stu-id="c097a-128">For example, if you enter 2, an invoice will be generated every two weeks for this customer.</span></span>  <span data-ttu-id="c097a-129">รายเดือน - เลือกตัวเลือกนี้ แล้วป้อนจำนวนเดือนในฟิลด์ ต่อ </span><span class="sxs-lookup"><span data-stu-id="c097a-129">Monthly - Select this option and enter the number of months in the Per field.</span></span> <span data-ttu-id="c097a-130">ตัวอย่างเช่น ถ้าคุณป้อนเลข 6 ใบแจ้งหนี้จะถูกสร้างทุกๆหกเดือนสำหรับลูกค้ารายนี้ </span><span class="sxs-lookup"><span data-stu-id="c097a-130">For example, if you enter 6, an invoice will be generated every six months for this customer.</span></span>  <span data-ttu-id="c097a-131">รายปี - เลือกตัวเลือกนี้และป้อนจำนวนปีในฟิลด์ ต่อ </span><span class="sxs-lookup"><span data-stu-id="c097a-131">Yearly – Select this option and enter the number of years in the Per field.</span></span> <span data-ttu-id="c097a-132">ตัวอย่างเช่น ถ้าคุณป้อนเลข 2 ใบแจ้งหนี้จะถูกสร้างทุกๆสองปีสำหรับลูกค้ารายนี้</span><span class="sxs-lookup"><span data-stu-id="c097a-132">For example, if you enter 2, an invoice will be generated every two years for this customer.</span></span>  
11. <span data-ttu-id="c097a-133">ในฟิลด์ ต่อ ให้ป้อนตัวเลข </span><span class="sxs-lookup"><span data-stu-id="c097a-133">In the Per field, enter a number.</span></span>

