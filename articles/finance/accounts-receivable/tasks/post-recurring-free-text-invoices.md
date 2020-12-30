---
title: สร้างและลงรายการบัญชีใบแจ้งหนี้ข้อความอิสระที่เกิดซ้ำ
description: 'ใบแจ้งหนี้ที่เกิดซ้ำจะถูกใช้เพื่อออกใบแจ้งหนี้ของลูกค้าประจำสำหรับยอดเงินเดียวกัน '
author: ShivamPandey-msft
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SysLookupMultiSelectGrid, CustRecurrenceInvoiceGroup, CustFreeInvoice, CustRecurrenceInvoiceTotals
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: f3b31dbf296a06ea6253a8ae71bfea6193a1e03e
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 10/13/2020
ms.locfileid: "4448400"
---
# <a name="generate-and-post-recurring-free-text-invoices"></a><span data-ttu-id="454c4-103">สร้างและลงรายการบัญชีใบแจ้งหนี้ข้อความอิสระที่เกิดซ้ำ</span><span class="sxs-lookup"><span data-stu-id="454c4-103">Generate and post recurring free text invoices</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="454c4-104">ใบแจ้งหนี้ที่เกิดซ้ำจะถูกใช้เพื่อออกใบแจ้งหนี้ของลูกค้าประจำสำหรับยอดเงินเดียวกัน </span><span class="sxs-lookup"><span data-stu-id="454c4-104">Recurring invoices are used to invoice customers regularly for the same amount.</span></span> <span data-ttu-id="454c4-105">การบันทึกข้อมูลนี้ใช้บริษัทสาธิต USMF</span><span class="sxs-lookup"><span data-stu-id="454c4-105">This recording uses the USMF demo company.</span></span> <span data-ttu-id="454c4-106">การบันทึกมีไว้สำหรับบุคคลที่รับผิดชอบการจัดการ และประมวลผลใบแจ้งหนี้ A/R</span><span class="sxs-lookup"><span data-stu-id="454c4-106">The recording is intended for the person responsible for managing and processing A/R invoices.</span></span>


## <a name="generate-recurring-invoices"></a><span data-ttu-id="454c4-107">สร้างใบแจ้งหนี้ที่เกิดซ้ำ</span><span class="sxs-lookup"><span data-stu-id="454c4-107">Generate recurring invoices</span></span>

## <a name="post-recurring-invoices"></a><span data-ttu-id="454c4-108">ลงรายการบัญชีใบแจ้งหนี้ที่เกิดซ้ำ</span><span class="sxs-lookup"><span data-stu-id="454c4-108">Post recurring invoices</span></span>
1. <span data-ttu-id="454c4-109">ไปที่บัญชีลูกหนี้ > ใบแจ้งหนี้ > ใบแจ้งหนี้ที่เกิดซ้ำ > ลงรายการบัญชีใบแจ้งหนี้ที่เกิดซ้ำ</span><span class="sxs-lookup"><span data-stu-id="454c4-109">Go to Accounts receivable > Invoices > Recurring invoices > Post recurring invoices.</span></span>
    * <span data-ttu-id="454c4-110">ใช้หน้านี้เพื่อดู และพิมพ์ใบแจ้งหนี้ที่เกิดซ้ำที่ถูกสร้างแล้ว</span><span class="sxs-lookup"><span data-stu-id="454c4-110">Use this page to view and print recurring invoices that have already been generated.</span></span>  
2. <span data-ttu-id="454c4-111">ในรายการนี้ ให้คลิกลิงค์ในแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="454c4-111">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="454c4-112">เลือกกลุ่มใบแจ้งหนี้ที่เกิดซ้ำ</span><span class="sxs-lookup"><span data-stu-id="454c4-112">Select the recurring invoice group.</span></span>  
3. <span data-ttu-id="454c4-113">คลิก ผลรวม</span><span class="sxs-lookup"><span data-stu-id="454c4-113">Click Totals.</span></span>
    * <span data-ttu-id="454c4-114">ตรวจสอบผลรวมสำหรับกลุ่มใบแจ้งหนี้ที่เกิดซ้ำ</span><span class="sxs-lookup"><span data-stu-id="454c4-114">Verify totals for the recurring invoice group.</span></span>  
4. <span data-ttu-id="454c4-115">คลิก ปิด</span><span class="sxs-lookup"><span data-stu-id="454c4-115">Click Close.</span></span>
    * <span data-ttu-id="454c4-116">แต่ละรายการข้างล่างคือ ใบแจ้งหนี้ข้อความอิสระที่เกิดซ้ำ </span><span class="sxs-lookup"><span data-stu-id="454c4-116">Each line below is a recurring free text invoice.</span></span> <span data-ttu-id="454c4-117">คุณสามารถเลือกรายการ และคลิกปุ่ม 'รายละเอียด' เพื่อดูรายละเอียดใบแจ้งหนี้ข้อความอิสระ</span><span class="sxs-lookup"><span data-stu-id="454c4-117">You can select a line and click 'Details' button to view free text invoice details.</span></span>  
5. <span data-ttu-id="454c4-118">คลิก ตรวจสอบความถูกต้อง</span><span class="sxs-lookup"><span data-stu-id="454c4-118">Click Validate.</span></span>
    * <span data-ttu-id="454c4-119">ตรวจสอบว่า ใบแจ้งหนี้ที่เลือกไม่มีข้อผิดพลาด แต่ไม่ได้ลงรายการบัญชีใบแจ้งหนี้</span><span class="sxs-lookup"><span data-stu-id="454c4-119">Verify that the selected invoices do not have errors, but do not post the invoices.</span></span>  
6. <span data-ttu-id="454c4-120">คลิก ลงรายการบัญชี</span><span class="sxs-lookup"><span data-stu-id="454c4-120">Click Post.</span></span>
    * <span data-ttu-id="454c4-121">ลงรายการบัญชีใบแจ้งหนี้ที่เลือก</span><span class="sxs-lookup"><span data-stu-id="454c4-121">Post the selected invoices.</span></span>  

