---
title: "การชำระเงินคืนลูกค้า"
description: "บทความนี้อธิบายวิธีการสร้างธุรกรรมการชำระเงินคืนสำหรับกลุ่มลูกค้า  ถ้าลูกค้ามียอดดุลเครดิต คุณสามารถชำระเงินคืนลูกค้าเป็นจำนวนยอดดุล"
author: ShivamPandey-msft
manager: AnnBe
ms.date: 08/22/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: LedgerJournalTransCustPaym, LedgerJournalTransVendPaym
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 14191
ms.assetid: 53533ee3-470e-458a-ac8b-3815aa4cb502
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: c3bee87b1d82dbe3d1c6de78a26633f2e1f5e92f
ms.contentlocale: th-th
ms.lasthandoff: 05/08/2018

---

# <a name="reimburse-customers"></a><span data-ttu-id="46be0-104">การชำระเงินคืนลูกค้า</span><span class="sxs-lookup"><span data-stu-id="46be0-104">Reimburse customers</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="46be0-105">บทความนี้อธิบายวิธีการสร้างธุรกรรมการชำระเงินคืนสำหรับกลุ่มลูกค้า </span><span class="sxs-lookup"><span data-stu-id="46be0-105">This article explains how to create reimbursement transactions for a group of customers.</span></span> <span data-ttu-id="46be0-106">ถ้าลูกค้ามียอดดุลเครดิต คุณสามารถชำระเงินคืนลูกค้าเป็นจำนวนยอดดุล</span><span class="sxs-lookup"><span data-stu-id="46be0-106">If a customer has a credit balance, you can reimburse the customer for the amount of the balance.</span></span> 

<span data-ttu-id="46be0-107">ตารางต่อไปนี้แสดงข้อกำหนดเบื้องต้นที่ต้องมีก่อนที่คุณจะเริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="46be0-107">The following table shows the prerequisites that must be in place before you start.</span></span>

| <span data-ttu-id="46be0-108">ข้อกำหนดเบื้องต้น</span><span class="sxs-lookup"><span data-stu-id="46be0-108">Prerequisite</span></span>                                                            | <span data-ttu-id="46be0-109">คำอธิบาย</span><span class="sxs-lookup"><span data-stu-id="46be0-109">Description</span></span>                                                                                                                                                                                 |
|-------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="46be0-110">ระบุยอดเงินชำระคืนเงินขั้นต่ำสำหรับนิติบุคคล</span><span class="sxs-lookup"><span data-stu-id="46be0-110">Specify the minimum reimbursement amount for the legal entity.</span></span>          | <span data-ttu-id="46be0-111">ใน **หน้าพารามิเตอร์บัญชีลูกหนี้** ในพื้นที่ **ทั่วไป** ในฟิลด์ **ชำระคืนเงินต่ำสุด** ป้อนยอดเงินต่ำสุดที่สามารถชำระเงินคืนสำหรับลูกค้าที่ชำระเงินเกิน</span><span class="sxs-lookup"><span data-stu-id="46be0-111">On the **Accounts receivable parameters** page, in the **General** area, in the **Minimum reimbursement** field, enter the minimum amount that can be reimbursed for customer overpayments.</span></span> |
| <span data-ttu-id="46be0-112">ขั้นตอนนี้ไม่จำเป็น: เพิ่มบัญชีผู้จัดจำหน่ายให้แก่ลูกค้าแต่ละรายที่สามารถได้รับเงินคืน</span><span class="sxs-lookup"><span data-stu-id="46be0-112">Optional: Add a vendor account to each customer that can be reimbursed.</span></span> | <span data-ttu-id="46be0-113">ในหน้า **ลูกค้า** ในแท็บด่วน **รายละเอียดเบ็ดเตล็ด** ในฟิลด์ **บัญชีผู้จัดจำหน่าย** เลือกบัญชีผู้จัดจำหน่ายสำหรับลูกค้า</span><span class="sxs-lookup"><span data-stu-id="46be0-113">On the **Customers** page, on the **Miscellaneous details** FastTab, in the **Vendor account** field, select the vendor account for the customer.</span></span>                                           |

<span data-ttu-id="46be0-114">เมื่อคุณสร้างธุรกรรมการจ่ายคืนเงิน ใบแจ้งหนี้ของผู้จัดจำหน่ายจะถูกสร้างขึ้นเพื่อจำนวนยอดดุลของเครดิต</span><span class="sxs-lookup"><span data-stu-id="46be0-114">When you create reimbursement transactions, a vendor invoice is created for the amount of the credit balance.</span></span> <span data-ttu-id="46be0-115">กระบวนการชำระคืนเงินจะลบยอดดุลเครดิตสำหรับบัญชีลูกค้าออก และสร้างยอดดุลครบกำหนดสำหรับบัญชีผู้จัดจำหน่ายที่เกี่ยวข้องกับลูกค้า</span><span class="sxs-lookup"><span data-stu-id="46be0-115">The reimbursement process removes the credit balance for the customer account and creates a balance due for the vendor account that corresponds to the customer.</span></span>

1.  <span data-ttu-id="46be0-116">ในบัญชีลูกหนี้ ดำเนินกระบวนการ **การชำระคืนเงิน** ได้</span><span class="sxs-lookup"><span data-stu-id="46be0-116">In Accounts receivable, run the **Reimbursement** process.</span></span>
2.  <span data-ttu-id="46be0-117">ทำตามขั้นตอนเหล่านี้</span><span class="sxs-lookup"><span data-stu-id="46be0-117">Follow one of these steps:</span></span>
    -   <span data-ttu-id="46be0-118">เมื่อต้องการจ่ายคืนเงินบัญชีลูกค้าเฉพาะ ให้คลิก **เลือก**, และระบุบัญชีลูกค้าในแบบสอบถาม</span><span class="sxs-lookup"><span data-stu-id="46be0-118">To reimburse specific customer accounts, click **Select**, and specify the customer accounts in the query.</span></span>
    -   <span data-ttu-id="46be0-119">เมื่อต้องการจ่ายคืนเงินบัญชีลูกค้าทั้งหมด คลิก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="46be0-119">To reimburse all customer accounts, click **OK**.</span></span>

    <span data-ttu-id="46be0-120">จำนวนเครดิตมีการโอนไปยังบัญชีผู้ขายของลูกค้าและดำเนินการเป็นการชำระเงินแบบปกติ</span><span class="sxs-lookup"><span data-stu-id="46be0-120">The credit amounts are transferred to the vendor accounts of the customers and are processed as ordinary payments.</span></span> <span data-ttu-id="46be0-121">ถ้าลูกค้าไม่มีบัญชีผู้ขาย โปรแกรมจะสร้างบัญชีผู้ขายครั้งเดียวสำหรับลูกค้าโดยอัตโนมัติ</span><span class="sxs-lookup"><span data-stu-id="46be0-121">If a customer doesn't have a vendor account, a one-time vendor account is automatically created for the customer.</span></span>
3.  <span data-ttu-id="46be0-122">ดูธุรกรรมการจ่ายคืนเงินที่สร้างขึ้น ใช้หน้า **การจ่ายคืนเงิน** ได้</span><span class="sxs-lookup"><span data-stu-id="46be0-122">To view the reimbursement transactions that were created, use the **Reimbursement** page.</span></span>
4.  <span data-ttu-id="46be0-123">ในบัญชีเจ้าหนี้ ให้สร้างการชำระเงินสำหรับใบแจ้งหนี้ของผู้จัดจำหน่ายที่สร้างขึ้นจากกระบวนการชำระคืนเงิน</span><span class="sxs-lookup"><span data-stu-id="46be0-123">In Accounts payable, create a payment for the vendor invoices that were created by the reimbursement process.</span></span>





