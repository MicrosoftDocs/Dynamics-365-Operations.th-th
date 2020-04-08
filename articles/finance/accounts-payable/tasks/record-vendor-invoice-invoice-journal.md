---
title: บันทึกใบแจ้งหนี้ของผู้จัดจำหน่ายในสมุดรายวันใบแจ้งหนี้
description: 'คู่มือของงานนี้จะแสดงวิธีการบันทึกใบแจ้งหนี้ของผู้จัดจำหน่ายที่ไม่ได้เชื่อมโยงกับใบสั่งซื้อ '
author: abruer
manager: AnnBe
ms.date: 07/11/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: VendInvoiceWorkspace, LedgerJournalTable, LedgerJournalTransVendInvoice
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: abruer
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 5277081d9f7adcc43c30d30208d13c7e39d76118
ms.sourcegitcommit: 57e1dafa186fec77ddd8ba9425d238e36e0f0998
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 03/18/2020
ms.locfileid: "3140386"
---
# <a name="record-a-vendor-invoice-in-the-invoice-journal"></a><span data-ttu-id="66c12-103">บันทึกใบแจ้งหนี้ของผู้จัดจำหน่ายในสมุดรายวันใบแจ้งหนี้</span><span class="sxs-lookup"><span data-stu-id="66c12-103">Record a vendor invoice in the invoice journal</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="66c12-104">คู่มือของงานนี้จะแสดงวิธีการบันทึกใบแจ้งหนี้ของผู้จัดจำหน่ายที่ไม่ได้เชื่อมโยงกับใบสั่งซื้อ </span><span class="sxs-lookup"><span data-stu-id="66c12-104">This task guide will show how to record vendor invoices that are not associated with purchase orders.</span></span> <span data-ttu-id="66c12-105">ตัวอย่างของใบแจ้งหนี้ชนิดนี้รวมถึงค่าใช้จ่ายสำหรับวัตถุดิบหรือบริการ </span><span class="sxs-lookup"><span data-stu-id="66c12-105">Examples of this type of invoice include expenses for supplies or services.</span></span>  <span data-ttu-id="66c12-106">การบันทึกข้อมูลนี้ใช้บริษัทสาธิต USMF</span><span class="sxs-lookup"><span data-stu-id="66c12-106">This recording uses the USMF demo company.</span></span>

1. <span data-ttu-id="66c12-107">ไปที่ **บานหน้าต่างนำทาง > โมดูล > บัญชีเจ้าหนี้ >พื้นที่ทำงาน > รายการใบแจ้งหนี้ของผู้จัดจำหน่าย**</span><span class="sxs-lookup"><span data-stu-id="66c12-107">Go to **Navigation pane > Modules > Accounts payable > Workspaces > Vendor invoice entry**.</span></span>
2. <span data-ttu-id="66c12-108">บน **บานหน้าต่างการดำเนินการ** ให้คลิก **สมุดรายวันใบแจ้งหนี้ใหม่**</span><span class="sxs-lookup"><span data-stu-id="66c12-108">On the **Action pane**, click **New invoice journal**.</span></span>
3. <span data-ttu-id="66c12-109">คลิก **สร้าง**</span><span class="sxs-lookup"><span data-stu-id="66c12-109">Click **New**.</span></span>
4. <span data-ttu-id="66c12-110">ในฟิลด์ **ชื่อ** ให้ป้อนชื่อสมุดรายวัน หรือคลิกปุ่มดรอปดาวน์เพื่อเปิดการค้นหา</span><span class="sxs-lookup"><span data-stu-id="66c12-110">In the **Name** field, enter the journal name or click the drop down button to open the lookup.</span></span>
5. <span data-ttu-id="66c12-111">ในฟิลด์ **คำอธิบาย** ให้พิมพ์ค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="66c12-111">In the **Description** field, type a value.</span></span>
6. <span data-ttu-id="66c12-112">บน **บานหน้าต่างการดำเนินการ** คลิก **รายการ**</span><span class="sxs-lookup"><span data-stu-id="66c12-112">On the **Action pane**, click **Lines**.</span></span> <span data-ttu-id="66c12-113">ในฟิลด์ **วันที่** ให้ป้อนวันที่ลงรายการบัญชีที่จะปรับปรุงบัญชีแยกประเภททั่วไป</span><span class="sxs-lookup"><span data-stu-id="66c12-113">In the **Date** field, enter the posting date that will update General Ledger.</span></span>  
7. <span data-ttu-id="66c12-114">ในฟิลด์ **บัญชี** ให้ระบุ **บัญชีผู้จัดจำหน่าย**</span><span class="sxs-lookup"><span data-stu-id="66c12-114">In the **Account** field, specify the **Vendor account**.</span></span>
8. <span data-ttu-id="66c12-115">ในฟิลด์ **ใบแจ้งหนี้** ให้ป้อนหมายเลขใบแจ้งหนี้</span><span class="sxs-lookup"><span data-stu-id="66c12-115">In the **Invoice** field, enter the invoice number.</span></span>
9. <span data-ttu-id="66c12-116">ในฟิลด์ **คำอธิบาย** ให้พิมพ์ค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="66c12-116">In the **Description** field, type a value.</span></span>
10. <span data-ttu-id="66c12-117">ในฟิลด์ **เครดิต** ให้ป้อนหมายเลข</span><span class="sxs-lookup"><span data-stu-id="66c12-117">In the **Credit** field, enter a number.</span></span>
11. <span data-ttu-id="66c12-118">ในฟิลด์ **บัญชีตรงข้าม** ให้ป้อนหมายเลขบัญชี หรือคลิกปุ่มดรอปดาวน์เพื่อเปิดการค้นหา</span><span class="sxs-lookup"><span data-stu-id="66c12-118">In the **Offset account** field, enter the account number or click the drop down button to open the lookup</span></span>
    * <span data-ttu-id="66c12-119">**กลุ่มภาษีขาย** จะเป็นค่าเริ่มต้นจากบัญชีผู้จัดจำหน่าย</span><span class="sxs-lookup"><span data-stu-id="66c12-119">The **Sales tax group** will be default from the vendor account.</span></span>  
    * <span data-ttu-id="66c12-120">**กลุ่มภาษีขายตามประเภทสินค้า** จะเป็นค่าเริ่มต้นจากบัญชีหลักที่ระบุในฟิลด์ **บัญชีตรงข้าม**</span><span class="sxs-lookup"><span data-stu-id="66c12-120">The **Item sales tax group** will be default from the main account specified in the **Offset account** field.</span></span>  
    * <span data-ttu-id="66c12-121">**วันที่ครบกำหนด** จะถูกคำนวณตามเงื่อนไขการชำระเงิน</span><span class="sxs-lookup"><span data-stu-id="66c12-121">The **Due date** will be calculated based on the Terms of payment.</span></span>  
    * <span data-ttu-id="66c12-122">**ส่วนลดเงินสด** จะเป็นค่าเริ่มต้นจากบัญชีผู้จัดจำหน่าย</span><span class="sxs-lookup"><span data-stu-id="66c12-122">The **Cash discount** will default from the Vendor account.</span></span>  
12. <span data-ttu-id="66c12-123">คลิก **ลงรายการบัญชี**</span><span class="sxs-lookup"><span data-stu-id="66c12-123">Click **Post**.</span></span>
13. <span data-ttu-id="66c12-124">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="66c12-124">Close the page.</span></span>

