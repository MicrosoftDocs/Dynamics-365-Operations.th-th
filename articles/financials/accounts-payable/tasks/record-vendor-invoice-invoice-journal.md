--- 
title: "บันทึกใบแจ้งหนี้ของผู้จัดจำหน่ายในสมุดรายวันใบแจ้งหนี้"
description: "คู่มือของงานนี้จะแสดงวิธีการบันทึกใบแจ้งหนี้ของผู้จัดจำหน่ายที่ไม่ได้เชื่อมโยงกับใบสั่งซื้อ "
author: abruer
manager: AnnBe
ms.date: 11/15/2016
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
ms.openlocfilehash: 26515140b020d824f99441b9f1ee560a44e28f8f
ms.contentlocale: th-th
ms.lasthandoff: 05/08/2018

---
# <a name="record-a-vendor-invoice-in-the-invoice-journal"></a><span data-ttu-id="dd538-103">บันทึกใบแจ้งหนี้ของผู้จัดจำหน่ายในสมุดรายวันใบแจ้งหนี้</span><span class="sxs-lookup"><span data-stu-id="dd538-103">Record a vendor invoice in the invoice journal</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="dd538-104">คู่มือของงานนี้จะแสดงวิธีการบันทึกใบแจ้งหนี้ของผู้จัดจำหน่ายที่ไม่ได้เชื่อมโยงกับใบสั่งซื้อ </span><span class="sxs-lookup"><span data-stu-id="dd538-104">This task guide will show how to record vendor invoices that are not associated with purchase orders.</span></span> <span data-ttu-id="dd538-105">ตัวอย่างของใบแจ้งหนี้ชนิดนี้รวมถึงค่าใช้จ่ายสำหรับวัตถุดิบหรือบริการ </span><span class="sxs-lookup"><span data-stu-id="dd538-105">Examples of this type of invoice include expenses for supplies or services.</span></span>  <span data-ttu-id="dd538-106">การบันทึกข้อมูลนี้ใช้บริษัทสาธิต USMF</span><span class="sxs-lookup"><span data-stu-id="dd538-106">This recording uses the USMF demo company.</span></span>

1. <span data-ttu-id="dd538-107">ไปที่บัญชีเจ้าหนี้ > พื้นที่ทำงาน > รายการใบแจ้งหนี้ของผู้จัดจำหน่าย</span><span class="sxs-lookup"><span data-stu-id="dd538-107">Go to Accounts payable > Workspaces > Vendor invoice entry.</span></span>
2. <span data-ttu-id="dd538-108">คลิกที่สมุดรายวันใบแจ้งหนี้ใหม่</span><span class="sxs-lookup"><span data-stu-id="dd538-108">Click New invoice journal.</span></span>
3. <span data-ttu-id="dd538-109">คลิก สร้าง</span><span class="sxs-lookup"><span data-stu-id="dd538-109">Click New.</span></span>
4. <span data-ttu-id="dd538-110">ในฟิลด์ชื่อ ให้ป้อนชื่อสมุดรายวันหรือคลิกปุ่มดรอปดาวน์เพื่อเปิดการค้นหา</span><span class="sxs-lookup"><span data-stu-id="dd538-110">In the Name field, enter the journal name or click the drop down button to open the lookup.</span></span>
5. <span data-ttu-id="dd538-111">ในฟิลด์ คำอธิบาย ให้พิมพ์ค่า</span><span class="sxs-lookup"><span data-stu-id="dd538-111">In the Description field, type a value.</span></span>
6. <span data-ttu-id="dd538-112">คลิก รายการ</span><span class="sxs-lookup"><span data-stu-id="dd538-112">Click Lines.</span></span>
    * <span data-ttu-id="dd538-113">ในฟิลด์วันที่ ให้ป้อนวันที่ลงรายการบัญชีที่จะอัพเดตบัญชีแยกประเภททั่วไป</span><span class="sxs-lookup"><span data-stu-id="dd538-113">In the Date field, enter the posting date that will update General Ledger.</span></span>  
7. <span data-ttu-id="dd538-114">ในฟิลด์บัญชี ให้ระบุบัญชีผู้จัดจำหน่าย</span><span class="sxs-lookup"><span data-stu-id="dd538-114">In the Account field, specify the Vendor account.</span></span>
8. <span data-ttu-id="dd538-115">ในฟิลด์ใบแจ้งหนี้ ให้ป้อนหมายเลขใบแจ้งหนี้</span><span class="sxs-lookup"><span data-stu-id="dd538-115">In the Invoice field, enter the invoice number.</span></span>
9. <span data-ttu-id="dd538-116">ในฟิลด์คำอธิบาย ให้พิมพ์ค่า</span><span class="sxs-lookup"><span data-stu-id="dd538-116">In the Description field, type a value.</span></span>
10. <span data-ttu-id="dd538-117">ในฟิลด์เครดิต ให้ป้อนหมายเลข</span><span class="sxs-lookup"><span data-stu-id="dd538-117">In the Credit field, enter a number.</span></span>
11. <span data-ttu-id="dd538-118">ในฟิลด์บัญชีตรงข้าม ให้ป้อนหมายเลขบัญชีหรือคลิกปุ่มดรอปดาวน์เพื่อเปิดการค้นหา</span><span class="sxs-lookup"><span data-stu-id="dd538-118">In the Offset account field, enter the account number or click the drop down button to open the lookup</span></span>
    * <span data-ttu-id="dd538-119">กลุ่มภาษีขายจะใช้ค่าเริ่มต้นจากบัญชีผู้จัดจำหน่าย</span><span class="sxs-lookup"><span data-stu-id="dd538-119">The Sales tax group will default from the vendor account.</span></span>  
    * <span data-ttu-id="dd538-120">กลุ่มภาษีขายตามประเภทสินค้าจะใช้ค่าเริ่มต้นจากบัญชีหลักที่ระบุในฟิลด์บัญชีตรงข้าม</span><span class="sxs-lookup"><span data-stu-id="dd538-120">The Item sales tax group will default from the main account specified in the Offset account field.</span></span>  
    * <span data-ttu-id="dd538-121">วันที่ครบกำหนดจะถูกคำนวณตามเงื่อนไขการชำระเงิน</span><span class="sxs-lookup"><span data-stu-id="dd538-121">The Due date will be calculated based on the Terms of payment.</span></span>  
    * <span data-ttu-id="dd538-122">ส่วนลดเงินสดจะใช้ค่าเริ่มต้นจากบัญชีผู้จัดจำหน่าย</span><span class="sxs-lookup"><span data-stu-id="dd538-122">The Cash discount will default from the Vendor account.</span></span>  
12. <span data-ttu-id="dd538-123">คลิก ลงรายการบัญชี</span><span class="sxs-lookup"><span data-stu-id="dd538-123">Click Post.</span></span>
13. <span data-ttu-id="dd538-124">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="dd538-124">Close the page.</span></span>


