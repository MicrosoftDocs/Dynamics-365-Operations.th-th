---
title: พื้นที่ทำงานการออกใบแจ้งหนี้การทำงานร่วมกันกับผู้จัดจำหน่าย
description: หัวข้อนี้อธิบายวิธีการดูใบแจ้งหนี้ของผู้จัดจำหน่ายและส่งใบแจ้งหนี้จากพื้นที่ทำงานการออกใบแจ้งหนี้การทำงานร่วมกันกับผู้จัดจำหน่าย
author: abruer
manager: AnnBe
ms.date: 08/22/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: VendInvoiceWorkspace
audience: Application User
ms.reviewer: roschlom
ms.custom: 221534
ms.assetid: c4ed62f3-d351-41d7-a2ad-790576cde4ab
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: ddb9d561e9785ee744c49d7fe03128102e77e9d3
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 02/15/2021
ms.locfileid: "5248218"
---
# <a name="vendor-collaboration-invoicing-workspace"></a><span data-ttu-id="7a8a7-103">พื้นที่ทำงานการออกใบแจ้งหนี้การทำงานร่วมกันกับผู้จัดจำหน่าย</span><span class="sxs-lookup"><span data-stu-id="7a8a7-103">Vendor collaboration invoicing workspace</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="7a8a7-104">หัวข้อนี้อธิบายวิธีการดูใบแจ้งหนี้ของผู้จัดจำหน่ายและส่งใบแจ้งหนี้จากพื้นที่ทำงานการออกใบแจ้งหนี้การทำงานร่วมกันกับผู้จัดจำหน่าย</span><span class="sxs-lookup"><span data-stu-id="7a8a7-104">This topic explains how you can view vendor invoices and submit invoices from the vendor collaboration invoicing workspace.</span></span>

<span data-ttu-id="7a8a7-105">พื้นที่ทำงาน **การออกใบแจ้งหนี้การทำงานร่วมกันกับผู้จัดจำหน่าย** สามารถถูกใช้เพื่อดูข้อมูลใบแจ้งหนี้ผู้จัดจำหน่าย และเพื่อส่งใบแจ้งหนี้ไปยังระบบโดยใช้ความสามารถเวิร์กโฟลว์</span><span class="sxs-lookup"><span data-stu-id="7a8a7-105">The **Vendor collaboration invoicing** workspace can be used to view vendor invoice information and to submit invoices to the system using workflow capabilities.</span></span>


<a name="vendor-collaboration-invoicing-workspace"></a><span data-ttu-id="7a8a7-106">พื้นที่ทำงานการออกใบแจ้งหนี้การทำงานร่วมกันกับผู้จัดจำหน่าย</span><span class="sxs-lookup"><span data-stu-id="7a8a7-106">Vendor collaboration invoicing workspace</span></span>
----------------------------------------

### <a name="summary-tiles"></a><span data-ttu-id="7a8a7-107">สรุปไทล์</span><span class="sxs-lookup"><span data-stu-id="7a8a7-107">Summary tiles</span></span>

<span data-ttu-id="7a8a7-108">ไทล์ **สรุป** แสดงภาพรวมของใบแจ้งหนี้ของผู้จัดจำหน่ายที่เลือก</span><span class="sxs-lookup"><span data-stu-id="7a8a7-108">The **Summary** tiles give an overview of the invoices for the selected vendor.</span></span> <span data-ttu-id="7a8a7-109">คุณสามารถดูใบแจ้งหนี้โดยเรียงตามสถานะได้</span><span class="sxs-lookup"><span data-stu-id="7a8a7-109">You can view invoices by their state.</span></span>
-   <span data-ttu-id="7a8a7-110">ยังไม่ได้ส่งใบแจ้งหนี้ฉบับร่างไปยังลำดับงาน</span><span class="sxs-lookup"><span data-stu-id="7a8a7-110">Draft invoices have not been submitted to workflow.</span></span>
-   <span data-ttu-id="7a8a7-111">ใบแจ้งหนี้ที่ส่งแล้วแต่ยังไม่ได้รับการอนุมัติคือใบแจ้งหนี้ที่ผู้จัดจำหน่ายส่งแล้ว แต่ยังไม่ได้ลงรายการบัญชีในแอพลิเคชัน</span><span class="sxs-lookup"><span data-stu-id="7a8a7-111">Submitted, not approved invoices are those invoices that the vendor has submitted, but they have not been posted in the application.</span></span>
-   <span data-ttu-id="7a8a7-112">ใบแจ้งหนี้ที่ส่งแล้วแต่ยังไม่ได้ชำระเงินคือใบแจ้งหนี้ที่ลงรายการบัญชีแล้ว แต่ยังชำระเงินไม่ครบ</span><span class="sxs-lookup"><span data-stu-id="7a8a7-112">Approved, not paid invoices are those that have been posted, but they have not yet been fully paid.</span></span>
-   <span data-ttu-id="7a8a7-113">ใบแจ้งหนี้ที่ชำระเงินแล้วคือใบแจ้งหนี้ที่ชำระเงินครบแล้วในแอพลิเคชัน</span><span class="sxs-lookup"><span data-stu-id="7a8a7-113">Paid invoices are those that have been fully paid in the application.</span></span>

<span data-ttu-id="7a8a7-114">เมื่อคลิกที่ไทล์ ระบบจะเปิดมุมมองที่กรองข้อมูลของหน้า **รายการใบแจ้งหนี้**</span><span class="sxs-lookup"><span data-stu-id="7a8a7-114">Clicking on a tile will open a filtered view of the **Invoices list** page.</span></span>

### <a name="tabular-lists"></a><span data-ttu-id="7a8a7-115">รายการตาราง</span><span class="sxs-lookup"><span data-stu-id="7a8a7-115">Tabular lists</span></span>

<span data-ttu-id="7a8a7-116">ในส่วน **รายการตาราง** สถานะของการออกใบแจ้งหนี้จะแบ่งออกในลักษณะที่คล้ายกันกับไทล์สรุป: รายการฉบับร่าง รายการที่ส่งแล้ว และรายการที่อนุมัติ</span><span class="sxs-lookup"><span data-stu-id="7a8a7-116">In the **Tabular lists** section, the status of the invoicing is broken down in similar ways as the summary tiles: Draft and Submitted, not approved lists.</span></span> <span data-ttu-id="7a8a7-117">ขณะที่อยู่ในสถานะฉบับร่าง สามารถส่งใบแจ้งหนี้ไปยังลำดับงานหรือลบออกได้</span><span class="sxs-lookup"><span data-stu-id="7a8a7-117">While in the Draft state, an invoice can be submitted to workflow or deleted.</span></span> <span data-ttu-id="7a8a7-118">รายการตารางสุดท้ายคือตัวเลือกในการค้นหาใบแจ้งหนี้</span><span class="sxs-lookup"><span data-stu-id="7a8a7-118">The last tabular list is an option to find invoices.</span></span> <span data-ttu-id="7a8a7-119">คุณสามารถกรองข้อมูลตามที่คุณค้นหาเพื่ออนุญาตสำหรับการค้นหาที่เร็วขึ้น</span><span class="sxs-lookup"><span data-stu-id="7a8a7-119">You can filter as you search, to allow for faster searches.</span></span>

### <a name="all-vendor-invoices-list-page"></a><span data-ttu-id="7a8a7-120">หน้ารายการใบแจ้งหนี้ของผู้จัดจำหน่ายทั้งหมด</span><span class="sxs-lookup"><span data-stu-id="7a8a7-120">All vendor invoices list page</span></span>

<span data-ttu-id="7a8a7-121">คุณสามารถดูใบแจ้งหนี้ของผู้จัดจำหน่ายที่ลงรายการบัญชีแล้วและที่ไม่ได้ลงรายการบัญชีทั้งหมดได้บนหน้ารายการ **ใบแจ้งหนี้การทำงานร่วมกันกับผู้จัดจำหน่าย**</span><span class="sxs-lookup"><span data-stu-id="7a8a7-121">You can view all posted and unposted vendor invoices on the **Vendor collaboration invoices** list page.</span></span> <span data-ttu-id="7a8a7-122">คุณสามารถใช้หน้ารายการนี้เพื่อดูสถานะการชำระเงินของใบแจ้งหนี้</span><span class="sxs-lookup"><span data-stu-id="7a8a7-122">You can use this list page to view the payment status of the invoices.</span></span> <span data-ttu-id="7a8a7-123">สถานะการชำระเงินรวมถึง ยังไม่ได้ลงรายการบัญชี ยังไม่ได้ชำระเงิน ชำระเงินบางส่วน และชำระเงินครบถ้วน</span><span class="sxs-lookup"><span data-stu-id="7a8a7-123">The payment statuses include Unposted, Unpaid, Partially paid, and Fully paid.</span></span>
<span data-ttu-id="7a8a7-124">การสร้างใบแจ้งหนี้ของผู้จัดจำหน่ายใหม่จากใบสั่งซื้อ</span><span class="sxs-lookup"><span data-stu-id="7a8a7-124">Creating a new invoice from a purchase order</span></span>

<span data-ttu-id="7a8a7-125">คุณสามารถสร้างใบแจ้งหนี้ของผู้จัดจำหน่ายใหม่โดยการเลือกการดำเนินการ **ใหม่** บนพื้นที่ทำงาน **การออกใบแจ้งหนี้การทำงานร่วมกันกับผู้จัดจำหน่าย**</span><span class="sxs-lookup"><span data-stu-id="7a8a7-125">You can create a new vendor invoice by selecting the **New** action on the **Vendor collaboration invoicing** workspace.</span></span> <span data-ttu-id="7a8a7-126">ผู้จัดจำหน่ายจำเป็นต้องระบุหมายเลขใบสั่งซื้อและหมายเลขใบแจ้งหนี้</span><span class="sxs-lookup"><span data-stu-id="7a8a7-126">The purchase order number and invoice number must be provided by the vendor.</span></span> <span data-ttu-id="7a8a7-127">โดยค่าเริ่มต้น รายการจากใบสั่งซื้อของผู้จัดจำหน่ายทั้งหมดจะปรากฏในใบแจ้งหนี้ใหม่</span><span class="sxs-lookup"><span data-stu-id="7a8a7-127">By default, all of the lines from the vendor's purchase order will appear on the new invoice.</span></span> <span data-ttu-id="7a8a7-128">คุณสามารถแก้ไขข้อมูลปริมาณและต้นทุนได้ก่อนที่จะส่งใบแจ้งหนี้ของผู้จัดจำหน่ายไปยังลำดับงาน</span><span class="sxs-lookup"><span data-stu-id="7a8a7-128">The quantity and cost information can be edited prior to submitting the vendor invoice to workflow.</span></span> <span data-ttu-id="7a8a7-129">คุณสามารถแนบไฟล์ บันทึก รูปภาพ และ URL ให้กับใบแจ้งหนี้ได้ก่อนที่จะส่ง</span><span class="sxs-lookup"><span data-stu-id="7a8a7-129">You can attach files, notes, images, and URLs to an invoice before submitting it.</span></span>

<span data-ttu-id="7a8a7-130">สำหรับข้อมูลเพิ่มเติม ดู [การทำงานร่วมกับผู้จัดจำหน่ายที่มีผู้จัดจำหน่ายภายนอก](../../supply-chain/procurement/vendor-collaboration-work-external-vendors.md)</span><span class="sxs-lookup"><span data-stu-id="7a8a7-130">For more information, see [Vendor collaboration with external vendors](../../supply-chain/procurement/vendor-collaboration-work-external-vendors.md)</span></span>





[!INCLUDE[footer-include](../../includes/footer-banner.md)]