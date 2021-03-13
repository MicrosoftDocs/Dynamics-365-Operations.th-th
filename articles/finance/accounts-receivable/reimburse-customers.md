---
title: การชำระเงินคืนลูกค้า
description: บทความนี้อธิบายวิธีการสร้างธุรกรรมการชำระเงินคืนสำหรับกลุ่มลูกค้า  ถ้าลูกค้ามียอดดุลเครดิต คุณสามารถชำระเงินคืนลูกค้าเป็นจำนวนยอดดุล
author: JodiChristiansen
manager: AnnBe
ms.date: 09/09/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerJournalTransCustPaym, LedgerJournalTransVendPaym
audience: Application User
ms.reviewer: roschlom
ms.custom: 14191
ms.assetid: 53533ee3-470e-458a-ac8b-3815aa4cb502
ms.search.region: Global
ms.author: jchrist
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: ae6a3078743fc9cd43c71bc1d4531c0553ee53bb
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 01/15/2021
ms.locfileid: "5012150"
---
# <a name="reimburse-customers"></a><span data-ttu-id="7df47-104">การชำระเงินคืนลูกค้า</span><span class="sxs-lookup"><span data-stu-id="7df47-104">Reimburse customers</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="7df47-105">บทความนี้อธิบายวิธีการสร้างธุรกรรมการชำระเงินคืนสำหรับกลุ่มลูกค้า </span><span class="sxs-lookup"><span data-stu-id="7df47-105">This article explains how to create reimbursement transactions for a group of customers.</span></span> <span data-ttu-id="7df47-106">ถ้าลูกค้ามียอดดุลเครดิต คุณสามารถชำระเงินคืนลูกค้าเป็นจำนวนยอดดุล</span><span class="sxs-lookup"><span data-stu-id="7df47-106">If a customer has a credit balance, you can reimburse the customer for the amount of the balance.</span></span> 

<span data-ttu-id="7df47-107">ตารางต่อไปนี้แสดงข้อกำหนดเบื้องต้นที่ต้องมีก่อนที่คุณจะเริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="7df47-107">The following table shows the prerequisites that must be in place before you start.</span></span>

| <span data-ttu-id="7df47-108">ข้อกำหนดเบื้องต้น</span><span class="sxs-lookup"><span data-stu-id="7df47-108">Prerequisite</span></span>                                                            | <span data-ttu-id="7df47-109">คำอธิบาย</span><span class="sxs-lookup"><span data-stu-id="7df47-109">Description</span></span> |
|-------------------------------------------------------------------------|-------------|
| <span data-ttu-id="7df47-110">ระบุยอดเงินชำระคืนเงินขั้นต่ำสำหรับนิติบุคคล</span><span class="sxs-lookup"><span data-stu-id="7df47-110">Specify the minimum reimbursement amount for the legal entity.</span></span>          | <span data-ttu-id="7df47-111">ใน **หน้าพารามิเตอร์บัญชีลูกหนี้** ในพื้นที่ **ทั่วไป** ในฟิลด์ **ชำระคืนเงินต่ำสุด** ป้อนยอดเงินต่ำสุดที่สามารถชำระเงินคืนสำหรับลูกค้าที่ชำระเงินเกิน</span><span class="sxs-lookup"><span data-stu-id="7df47-111">On the **Accounts receivable parameters** page, in the **General** area, in the **Minimum reimbursement** field, enter the minimum amount that can be reimbursed for customer overpayments.</span></span> |
| <span data-ttu-id="7df47-112">ขั้นตอนนี้ไม่จำเป็น: เพิ่มบัญชีผู้จัดจำหน่ายให้แก่ลูกค้าแต่ละรายที่สามารถได้รับเงินคืน</span><span class="sxs-lookup"><span data-stu-id="7df47-112">Optional: Add a vendor account to each customer that can be reimbursed.</span></span> | <span data-ttu-id="7df47-113">ในหน้า **ลูกค้า** ในแท็บด่วน **รายละเอียดเบ็ดเตล็ด** ในฟิลด์ **บัญชีผู้จัดจำหน่าย** เลือกบัญชีผู้จัดจำหน่ายสำหรับลูกค้า</span><span class="sxs-lookup"><span data-stu-id="7df47-113">On the **Customers** page, on the **Miscellaneous details** FastTab, in the **Vendor account** field, select the vendor account for the customer.</span></span> |

<span data-ttu-id="7df47-114">เมื่อคุณสร้างธุรกรรมการจ่ายคืนเงิน ใบแจ้งหนี้ของผู้จัดจำหน่ายจะถูกสร้างขึ้นเพื่อจำนวนยอดดุลของเครดิต</span><span class="sxs-lookup"><span data-stu-id="7df47-114">When you create reimbursement transactions, a vendor invoice is created for the amount of the credit balance.</span></span> <span data-ttu-id="7df47-115">กระบวนการชำระคืนเงินจะลบยอดดุลเครดิตสำหรับบัญชีลูกค้าออก และสร้างยอดดุลครบกำหนดสำหรับบัญชีผู้จัดจำหน่ายที่เกี่ยวข้องกับลูกค้า</span><span class="sxs-lookup"><span data-stu-id="7df47-115">The reimbursement process removes the credit balance for the customer account and creates a balance due for the vendor account that corresponds to the customer.</span></span>

1. <span data-ttu-id="7df47-116">ในบัญชีลูกหนี้ ให้รันกระบวนการ **การชำระคืนเงิน** (**บัญชีลูกหนี้ \> งานประจำงวด \> การชำระคืนเงิน**)</span><span class="sxs-lookup"><span data-stu-id="7df47-116">In Accounts receivable, run the **Reimbursement** process (**Accounts receivable \> Periodic tasks \> Reimbursement**).</span></span>
2. <span data-ttu-id="7df47-117">ถ้าต้องการจัดกลุ่มธุรกรรมทั้งหมด โดยไม่คำนึงถึงมิติบัญชีแยกประเภท ให้ตั้งค่าตัวเลือก **สรุปของลูกค้า** เป็น **ใช่**</span><span class="sxs-lookup"><span data-stu-id="7df47-117">To group all transactions, regardless of ledger dimensions, set the **Summarize customer** option to **Yes**.</span></span> <span data-ttu-id="7df47-118">ถ้าต้องการจัดกลุ่มเฉพาะธุรกรรมที่มีมิติบัญชีแยกประเภทที่คล้ายกัน ให้ตั้งค่าตัวเลือกเป็น **ไม่**</span><span class="sxs-lookup"><span data-stu-id="7df47-118">To group only transactions that have similar ledger dimensions, set the option to **No**.</span></span>
3. <span data-ttu-id="7df47-119">เลือก **รวมลูกค้าที่มีธุรกรรมยอดเดบิตคงค้าง** เพื่อเลือกลูกค้าที่มียอดเดบิตที่ยังไม่ได้ชำระ</span><span class="sxs-lookup"><span data-stu-id="7df47-119">Select **Include customers with outstanding debit transactions** to select customers who have unsettled debit amounts.</span></span>
4. <span data-ttu-id="7df47-120">เมื่อต้องการชำระคืนเงินให้กับบัญชีลูกค้าเฉพาะ บนแท็บด่วน **เรกคอร์ดเพื่อรวม** ให้เลือก **ตัวกรอง** แล้วจากนั้นระบุบัญชีลูกค้าในการสอบถาม</span><span class="sxs-lookup"><span data-stu-id="7df47-120">To reimburse specific customer accounts, on the **Records to include** FastTab, select **Filter**, and then specify the customer accounts in the query.</span></span>

    <span data-ttu-id="7df47-121">จำนวนเครดิตมีการโอนไปยังบัญชีผู้ขายของลูกค้าและดำเนินการเป็นการชำระเงินแบบปกติ</span><span class="sxs-lookup"><span data-stu-id="7df47-121">The credit amounts are transferred to the vendor accounts of the customers and are processed as ordinary payments.</span></span> <span data-ttu-id="7df47-122">ถ้าลูกค้าไม่มีบัญชีผู้ขาย โปรแกรมจะสร้างบัญชีผู้ขายครั้งเดียวสำหรับลูกค้าโดยอัตโนมัติ</span><span class="sxs-lookup"><span data-stu-id="7df47-122">If a customer doesn't have a vendor account, a one-time vendor account is automatically created for the customer.</span></span>

5. <span data-ttu-id="7df47-123">ถ้าต้องการดูธุรกรรมการชำระคืนเงินที่สร้างขึ้น ให้ใช้รายงาน **การชำระคืนเงิน** (**บัญชีลูกหนี้ \> การสอบถามและรายงาน \> รายงานการชำระคืนเงิน**)</span><span class="sxs-lookup"><span data-stu-id="7df47-123">To view the reimbursement transactions that were created, use the **Reimbursement** report (**Accounts Receivable \> Inquiries and reports \> Reimbursement report**).</span></span>
6. <span data-ttu-id="7df47-124">ในบัญชีเจ้าหนี้ ให้สร้างการชำระเงินสำหรับใบแจ้งหนี้ของผู้จัดจำหน่ายที่สร้างขึ้นจากกระบวนการชำระคืนเงิน</span><span class="sxs-lookup"><span data-stu-id="7df47-124">In Accounts payable, create a payment for the vendor invoices that were created by the reimbursement process.</span></span> <span data-ttu-id="7df47-125">สำหรับข้อมูลเกี่ยวกับวิธีการชำระเงินให้แก่ผู้จัดจำหน่าย โปรดดู [ภาพรวมการชำระเงินของผู้จัดจำหน่าย](../accounts-payable/Vendor-payments-workspace.md)</span><span class="sxs-lookup"><span data-stu-id="7df47-125">For information about how to pay vendors, see [Vendor payment overview](../accounts-payable/Vendor-payments-workspace.md).</span></span>
