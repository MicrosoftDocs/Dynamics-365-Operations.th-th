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
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 56600abe791c2a299f6c8f77398e0e5ac51710a3
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 02/15/2021
ms.locfileid: "5220190"
---
# <a name="generate-and-post-recurring-free-text-invoices"></a><span data-ttu-id="566ea-103">สร้างและลงรายการบัญชีใบแจ้งหนี้ข้อความอิสระที่เกิดซ้ำ</span><span class="sxs-lookup"><span data-stu-id="566ea-103">Generate and post recurring free text invoices</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="566ea-104">ใบแจ้งหนี้ที่เกิดซ้ำจะถูกใช้เพื่อออกใบแจ้งหนี้ของลูกค้าประจำสำหรับยอดเงินเดียวกัน </span><span class="sxs-lookup"><span data-stu-id="566ea-104">Recurring invoices are used to invoice customers regularly for the same amount.</span></span> <span data-ttu-id="566ea-105">การบันทึกข้อมูลนี้ใช้บริษัทสาธิต USMF</span><span class="sxs-lookup"><span data-stu-id="566ea-105">This recording uses the USMF demo company.</span></span> <span data-ttu-id="566ea-106">การบันทึกมีไว้สำหรับบุคคลที่รับผิดชอบการจัดการ และประมวลผลใบแจ้งหนี้ A/R</span><span class="sxs-lookup"><span data-stu-id="566ea-106">The recording is intended for the person responsible for managing and processing A/R invoices.</span></span>


## <a name="generate-recurring-invoices"></a><span data-ttu-id="566ea-107">สร้างใบแจ้งหนี้ที่เกิดซ้ำ</span><span class="sxs-lookup"><span data-stu-id="566ea-107">Generate recurring invoices</span></span>

## <a name="post-recurring-invoices"></a><span data-ttu-id="566ea-108">ลงรายการบัญชีใบแจ้งหนี้ที่เกิดซ้ำ</span><span class="sxs-lookup"><span data-stu-id="566ea-108">Post recurring invoices</span></span>
1. <span data-ttu-id="566ea-109">ไปที่บัญชีลูกหนี้ > ใบแจ้งหนี้ > ใบแจ้งหนี้ที่เกิดซ้ำ > ลงรายการบัญชีใบแจ้งหนี้ที่เกิดซ้ำ</span><span class="sxs-lookup"><span data-stu-id="566ea-109">Go to Accounts receivable > Invoices > Recurring invoices > Post recurring invoices.</span></span>
    * <span data-ttu-id="566ea-110">ใช้หน้านี้เพื่อดู และพิมพ์ใบแจ้งหนี้ที่เกิดซ้ำที่ถูกสร้างแล้ว</span><span class="sxs-lookup"><span data-stu-id="566ea-110">Use this page to view and print recurring invoices that have already been generated.</span></span>  
2. <span data-ttu-id="566ea-111">ในรายการนี้ ให้คลิกลิงค์ในแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="566ea-111">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="566ea-112">เลือกกลุ่มใบแจ้งหนี้ที่เกิดซ้ำ</span><span class="sxs-lookup"><span data-stu-id="566ea-112">Select the recurring invoice group.</span></span>  
3. <span data-ttu-id="566ea-113">คลิก ผลรวม</span><span class="sxs-lookup"><span data-stu-id="566ea-113">Click Totals.</span></span>
    * <span data-ttu-id="566ea-114">ตรวจสอบผลรวมสำหรับกลุ่มใบแจ้งหนี้ที่เกิดซ้ำ</span><span class="sxs-lookup"><span data-stu-id="566ea-114">Verify totals for the recurring invoice group.</span></span>  
4. <span data-ttu-id="566ea-115">คลิก ปิด</span><span class="sxs-lookup"><span data-stu-id="566ea-115">Click Close.</span></span>
    * <span data-ttu-id="566ea-116">แต่ละรายการข้างล่างคือ ใบแจ้งหนี้ข้อความอิสระที่เกิดซ้ำ </span><span class="sxs-lookup"><span data-stu-id="566ea-116">Each line below is a recurring free text invoice.</span></span> <span data-ttu-id="566ea-117">คุณสามารถเลือกรายการ และคลิกปุ่ม 'รายละเอียด' เพื่อดูรายละเอียดใบแจ้งหนี้ข้อความอิสระ</span><span class="sxs-lookup"><span data-stu-id="566ea-117">You can select a line and click 'Details' button to view free text invoice details.</span></span>  
5. <span data-ttu-id="566ea-118">คลิก ตรวจสอบความถูกต้อง</span><span class="sxs-lookup"><span data-stu-id="566ea-118">Click Validate.</span></span>
    * <span data-ttu-id="566ea-119">ตรวจสอบว่า ใบแจ้งหนี้ที่เลือกไม่มีข้อผิดพลาด แต่ไม่ได้ลงรายการบัญชีใบแจ้งหนี้</span><span class="sxs-lookup"><span data-stu-id="566ea-119">Verify that the selected invoices do not have errors, but do not post the invoices.</span></span>  
6. <span data-ttu-id="566ea-120">คลิก ลงรายการบัญชี</span><span class="sxs-lookup"><span data-stu-id="566ea-120">Click Post.</span></span>
    * <span data-ttu-id="566ea-121">ลงรายการบัญชีใบแจ้งหนี้ที่เลือก</span><span class="sxs-lookup"><span data-stu-id="566ea-121">Post the selected invoices.</span></span>  



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]