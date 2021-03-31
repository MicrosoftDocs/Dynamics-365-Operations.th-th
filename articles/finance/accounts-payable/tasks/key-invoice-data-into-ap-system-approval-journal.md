---
title: ข้อมูลใบแจ้งหนี้ที่สำคัญในบัญชีเจ้าหนี้โดยใช้สมุดรายวันการอนุมัติ
description: หัวข้อนี้จะอธิบายวิธีการใช้ทะเบียนใบแจ้งหนี้เพื่อสร้างใบแจ้งหนี้ และจากนั้น ใช้สมุดรายวันการอนุมัติสำหรับการปรับปรุงบัญชีค่าใช้จ่าย
author: abruer
manager: AnnBe
ms.date: 08/08/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerJournalTable, LedgerJournalTransInvoiceRegister, HcmWorkerLookUp, LedgerJournalTransApprove, LedgerJournalTransApproveFetchVouchers, LedgerTransVoucher
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: abruer
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: f0fee32d9fd1ab89b1a8cedb2e1965674586d4e7
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 02/15/2021
ms.locfileid: "5227195"
---
# <a name="key-invoice-data-into-accounts-payable-using-an-approval-journal"></a><span data-ttu-id="4c1d6-103">ข้อมูลใบแจ้งหนี้ที่สำคัญในบัญชีเจ้าหนี้โดยใช้สมุดรายวันการอนุมัติ</span><span class="sxs-lookup"><span data-stu-id="4c1d6-103">Key invoice data into accounts payable using an approval journal</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="4c1d6-104">หัวข้อนี้จะอธิบายวิธีการใช้ทะเบียนใบแจ้งหนี้เพื่อสร้างใบแจ้งหนี้ และจากนั้น ใช้สมุดรายวันการอนุมัติสำหรับการปรับปรุงบัญชีค่าใช้จ่าย</span><span class="sxs-lookup"><span data-stu-id="4c1d6-104">This topic explains how to use the invoice register to create invoices and then use the approval journal to update the expense accounts.</span></span>

## <a name="create-and-post-and-invoice"></a><span data-ttu-id="4c1d6-105">สร้างและลงรายการบัญชีและใบแจ้งหนี้</span><span class="sxs-lookup"><span data-stu-id="4c1d6-105">Create and post and invoice</span></span>
1. <span data-ttu-id="4c1d6-106">ในบานหน้าต่างนำทาง ไปที่ **โมดูล > บัญชีเจ้าหนี้ > ใบแจ้งหนี้ > ทะเบียนใบแจ้งหนี้**</span><span class="sxs-lookup"><span data-stu-id="4c1d6-106">In the navigation pan, go to **Modules > Accounts payable > Invoices > Invoice register**.</span></span>
2. <span data-ttu-id="4c1d6-107">เลือก **ใหม่**</span><span class="sxs-lookup"><span data-stu-id="4c1d6-107">Select **New**.</span></span>
3. <span data-ttu-id="4c1d6-108">เลือกชื่อทะเบียนใบแจ้งหนี้ที่คุณต้องการจะใช้</span><span class="sxs-lookup"><span data-stu-id="4c1d6-108">Select the name of the invoice register that you want to use.</span></span>
4. <span data-ttu-id="4c1d6-109">เลือก **รายการ** เพื่อเปิดการลงทะเบียนและป้อนรายการค่าใช้จ่าย</span><span class="sxs-lookup"><span data-stu-id="4c1d6-109">Select **Lines** to open the register and enter expense lines.</span></span>
5. <span data-ttu-id="4c1d6-110">เลือกผู้จัดจำหน่าย</span><span class="sxs-lookup"><span data-stu-id="4c1d6-110">Select a vendor.</span></span> <span data-ttu-id="4c1d6-111">ตัวอย่างเช่น ป้อนหรือเลือก `US-104`</span><span class="sxs-lookup"><span data-stu-id="4c1d6-111">For example, enter or select `US-104`.</span></span>
6. <span data-ttu-id="4c1d6-112">ในฟิลด์ **ใบแจ้งหนี้** ให้พิมพ์ค่า</span><span class="sxs-lookup"><span data-stu-id="4c1d6-112">In the **Invoice** field, type a value.</span></span>
7. <span data-ttu-id="4c1d6-113">ในฟิลด์ **คำอธิบาย** ให้พิมพ์ค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="4c1d6-113">In the **Description** field, type a value.</span></span>
8. <span data-ttu-id="4c1d6-114">ในฟิลด์ **เครดิต** ให้ป้อนหมายเลข</span><span class="sxs-lookup"><span data-stu-id="4c1d6-114">In the **Credit** field, enter a number.</span></span>
9. <span data-ttu-id="4c1d6-115">ในฟิลด์ **อนุมัติโดย** ให้เลือกผู้อนุมัติจากเมนูแบบหล่นลง</span><span class="sxs-lookup"><span data-stu-id="4c1d6-115">In the **Approved by** field, select an approver from the drop-down menu.</span></span>
10. <span data-ttu-id="4c1d6-116">เลือก **ลงรายการบัญชี**</span><span class="sxs-lookup"><span data-stu-id="4c1d6-116">Select **Post**.</span></span>

## <a name="approve-an-invoice"></a><span data-ttu-id="4c1d6-117">อนุมัติใบแจ้งหนี้</span><span class="sxs-lookup"><span data-stu-id="4c1d6-117">Approve an invoice</span></span>
1. <span data-ttu-id="4c1d6-118">ในบานหน้าต่างนำทาง ไปที่ **โมดูล > บัญชีเจ้าหนี้ > ใบแจ้งหนี้ > การอนุมัติใบแจ้งหนี้**</span><span class="sxs-lookup"><span data-stu-id="4c1d6-118">In the navigation pane, go to **Modules > Accounts payable > Invoices > Invoice approval**.</span></span>
2. <span data-ttu-id="4c1d6-119">เลือก **ใหม่**</span><span class="sxs-lookup"><span data-stu-id="4c1d6-119">Select **New**.</span></span>
3. <span data-ttu-id="4c1d6-120">เลือกชื่อสมุดรายวันการอนุมัติใบแจ้งหนี้ที่คุณต้องการจะใช้</span><span class="sxs-lookup"><span data-stu-id="4c1d6-120">Select the name of the invoice approval journal that you want to use.</span></span>
4. <span data-ttu-id="4c1d6-121">เลือก **รายการ** เพื่อแสดงหน้าที่คุณจะสามารถเลือกใบแจ้งหนี้ที่คุณต้องการอนุมัติ</span><span class="sxs-lookup"><span data-stu-id="4c1d6-121">Select **Lines** to display a page where you will be able to select the invoices that you want to approve.</span></span>
5. <span data-ttu-id="4c1d6-122">เลือก **ค้นหาใบสำคัญ** เพื่อแสดงใบแจ้งหนี้ทั้งหมดที่พร้อมสำหรับการอนุมัติ</span><span class="sxs-lookup"><span data-stu-id="4c1d6-122">Select **Find Vouchers** to display all of the invoices that are ready for approval.</span></span>
6. <span data-ttu-id="4c1d6-123">ทำเครื่องหมายใบแจ้งหนี้ที่คุณสร้าง จากนั้น คลิก **เลือก**</span><span class="sxs-lookup"><span data-stu-id="4c1d6-123">Mark the invoice that you created, then click **Select**.</span></span> <span data-ttu-id="4c1d6-124">ใบสำคัญที่คุณเลือกไว้ด้านบนจะถูกย้ายไปยังรายการนี้หลังจากที่คุณทำการเลือก</span><span class="sxs-lookup"><span data-stu-id="4c1d6-124">The vouchers that you selected above are moved to this list after you select them.</span></span>  
7. <span data-ttu-id="4c1d6-125">เลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="4c1d6-125">Select **OK**.</span></span>
8. <span data-ttu-id="4c1d6-126">เลือกฟิลด์ **หมายเลขบัญชี** เพื่อเพิ่มบัญชีค่าใช้จ่ายในใบแจ้งหนี้</span><span class="sxs-lookup"><span data-stu-id="4c1d6-126">Select the **account number** field to add an expense account to the invoice.</span></span>
9. <span data-ttu-id="4c1d6-127">ป้อนหมายเลขบัญชีและปิดฟิลด์ </span><span class="sxs-lookup"><span data-stu-id="4c1d6-127">Enter an account number and tab off of the field.</span></span> <span data-ttu-id="4c1d6-128">ตัวอย่างเช่น ป้อน `600120`</span><span class="sxs-lookup"><span data-stu-id="4c1d6-128">For example, enter `600120`.</span></span>
10. <span data-ttu-id="4c1d6-129">เลือก **ลงรายการบัญชี**</span><span class="sxs-lookup"><span data-stu-id="4c1d6-129">Select **Post**.</span></span>
11. <span data-ttu-id="4c1d6-130">เลือก **ใบสำคัญ** เพื่อดูรายการที่ลงรายการบัญชีไว้</span><span class="sxs-lookup"><span data-stu-id="4c1d6-130">Select **Voucher** to view the entries that were posted.</span></span> <span data-ttu-id="4c1d6-131">บัญชีการอนุมัติใบแจ้งหนี้ที่ค้างอยู่เป็นการกลับรายการและแทนที่ด้วยบัญชีค่าใช้จ่ายจริง</span><span class="sxs-lookup"><span data-stu-id="4c1d6-131">The Invoice Pending Approval account is reversed and replaced with the actual expense account.</span></span>  



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]