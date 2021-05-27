---
title: บันทึกหมายเลขใบรับรองที่จะได้รับคืน TDS
description: หัวข้อนี้อธิบายวิธีการใช้หน้าใบรับรองที่จะได้รับคืน เพื่อบันทึกหมายเลขและวันที่ใบรับรองของใบรับรองภาษี ณ ที่จ่าย (TDS) ที่ได้รับจากผู้จัดจำหน่าย ลูกค้า หรือบัญชีแยกประเภทที่ระบุ
author: kailiang
mms.date: 02/12/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 15721
ms.assetid: b4b406fa-b772-44ec-8dd8-8eb818a921ef
ms.search.region: Global
ms.author: kailiang
ms.search.validFrom: 2021-02-12
ms.dyn365.ops.version: AX 10.0.17
ms.openlocfilehash: b501c331cccc6d030f36d0a13ba0a6a13c08c733
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 05/11/2021
ms.locfileid: "6023614"
---
# <a name="record-tds-recoverable-certificate-numbers"></a><span data-ttu-id="c9da6-103">บันทึกหมายเลขใบรับรองที่จะได้รับคืน TDS</span><span class="sxs-lookup"><span data-stu-id="c9da6-103">Record TDS recoverable certificate numbers</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="c9da6-104">หัวข้อนี้อธิบายวิธีการใช้หน้า **ใบรับรองที่จะได้รับคืน** เพื่อบันทึกหมายเลขและวันที่ใบรับรองของใบรับรองภาษี ณ ที่จ่าย (TDS) ที่ได้รับจากผู้จัดจำหน่าย ลูกค้า หรือบัญชีแยกประเภทที่ระบุ</span><span class="sxs-lookup"><span data-stu-id="c9da6-104">This topic explains how to use the **Recoverable certificates** page to record the certificate numbers and dates for Tax Deducted at Source (TDS) certificates that are received for a specific vendor, customer, or ledger.</span></span> <span data-ttu-id="c9da6-105">เมื่อต้องการอัปเดตหมายเลขและวันที่ในใบรับรอง TDS ที่บันทึกให้กับธุรกรรม TDS บนหน้านี้ ให้ใช้หน้า **อัปเดตใบรับรอง** (**บัญชีแยกประเภททั่วไป \> ประจำงวด \> ภาษีหัก ณ ที่จ่าย \> อัปเดตใบรับรอง**)</span><span class="sxs-lookup"><span data-stu-id="c9da6-105">To update the TDS certificate numbers and dates that are recorded for TDS transactions on this page, use the **Update certificate** page (**General ledger \> Periodic \> Withholding tax \> Update certificate**).</span></span> <span data-ttu-id="c9da6-106">หลังจากที่คุณอัปเดตหมายเลขใบรับรอง TDS เสร็จสิ้นแล้ว ให้ปิด</span><span class="sxs-lookup"><span data-stu-id="c9da6-106">After you've finished updating TDS certificate numbers, close them.</span></span>

<span data-ttu-id="c9da6-107">ปฏิบัติตามขั้นตอนเหล่านี้ เพื่อบันทึกหมายเลขและวันที่ใบรับรอง TDS</span><span class="sxs-lookup"><span data-stu-id="c9da6-107">Follow these steps to record the TDS certificate numbers and dates.</span></span>

1. <span data-ttu-id="c9da6-108">ไปที่ **ภาษี \> ภาษีทางอ้อม \> ภาษีหัก ณ ที่จ่าย \> ใบรับรองที่จะได้รับคืน**</span><span class="sxs-lookup"><span data-stu-id="c9da6-108">Go to **Tax \> Indirect tax \> Withholding tax \> Recoverable certificates**.</span></span>

    <span data-ttu-id="c9da6-109">[![หน้าใบรับรองที่จะได้รับคืน](./media/apac-ind-TDS-49.png)](./media/apac-ind-TDS-49.png)</span><span class="sxs-lookup"><span data-stu-id="c9da6-109">[![Recoverable certificates page](./media/apac-ind-TDS-49.png)](./media/apac-ind-TDS-49.png)</span></span> 

2. <span data-ttu-id="c9da6-110">บนหน้า **ใบรับรองที่จะได้รับคืน** ในฟิลด์ **ชนิดภาษี** ให้เลือก **TDS**</span><span class="sxs-lookup"><span data-stu-id="c9da6-110">On the **Recoverable certificates** page, in the **Tax type** field, select **TDS**.</span></span>
3. <span data-ttu-id="c9da6-111">เลือก **สร้าง** เพื่อสร้างเรกคอร์ด</span><span class="sxs-lookup"><span data-stu-id="c9da6-111">Select **New** to create a record.</span></span>
4. <span data-ttu-id="c9da6-112">ในฟิลด์ **หมายเลขใบรับรอง** ป้อนหมายเลขใบรับรอง TDS</span><span class="sxs-lookup"><span data-stu-id="c9da6-112">In the **Certificate number** field, enter the TDS certificate number.</span></span>
5. <span data-ttu-id="c9da6-113">ในฟิลด์ **ชนิดบัญชี** ให้เลือกชนิดของบัญชีที่จะรับใบรับรอง TDS ได้แก่ **ผู้จัดจำหน่าย** **ลูกค้า** หรือ **บัญชีแยกประเภท**</span><span class="sxs-lookup"><span data-stu-id="c9da6-113">In the **Account type** field, select the type of account that the TDS certificate is received for: **Vendor**, **Customer**, or **Ledger**.</span></span>
6. <span data-ttu-id="c9da6-114">ในฟิลด์ **บัญชี** ให้เลือกหมายเลขบัญชีผู้จัดจำหน่าย ลูกค้า หรือบัญชีแยกประเภท ทั้งนี้ขึ้นอยู่กับชนิดบัญชีที่คุณเลือกไว้</span><span class="sxs-lookup"><span data-stu-id="c9da6-114">In the **Account** field, select the vendor, customer, or ledger account number, depending on the account type that you selected.</span></span> <span data-ttu-id="c9da6-115">ฟิลด์ **ชื่อ** จะแสดงชื่อของบัญชีผู้จัดจำหน่าย ลูกค้า หรือบัญชีแยกประเภท</span><span class="sxs-lookup"><span data-stu-id="c9da6-115">The **Name** field shows the name of the vendor, customer, or ledger account.</span></span>
7. <span data-ttu-id="c9da6-116">ในฟิลด์ **จำนวนเงินที่รับรอง** ป้อนชื่จำนวนของใบรับรอง TDS</span><span class="sxs-lookup"><span data-stu-id="c9da6-116">In the **Certificate amount** field, enter the amount of the TDS certificate.</span></span>
8. <span data-ttu-id="c9da6-117">ในฟิลด์ **วันที่** ป้อนวันที่รับรองของหมายเลขใบรับรอง</span><span class="sxs-lookup"><span data-stu-id="c9da6-117">In the **Date** field, enter the certificate date for the certificate number.</span></span>
9. <span data-ttu-id="c9da6-118">เลือก **การสอบถาม** เพื่อเปิดหน้า **ธุรกรรมใบรับรอง** ซึ่งคุณสามารถดูธุรกรรม TDS ที่มีการอัปเดตหมายเลขและวันที่ใบรับรอง TDS</span><span class="sxs-lookup"><span data-stu-id="c9da6-118">Select **Inquiries** to open the **Certificate transactions** page, where you can view the TDS transactions that the TDS certificate number and date are updated for.</span></span> <span data-ttu-id="c9da6-119">คุณสามารถอัปเดตข้อมูลนี้ในหน้า **อัปเดตใบรับรอง** (**ภาษี \> ประกาศต่างๆ \> ภาษีหัก ณ ที่จ่าย \> อัปเดตใบรับรอง**)</span><span class="sxs-lookup"><span data-stu-id="c9da6-119">This information can be updated on the **Update certificate** page (**Tax \> Declarations \> Withholding tax \> Update certificate**).</span></span>

    <span data-ttu-id="c9da6-120">แท็บ **อับเดตใบรับรอง** แสดงข้อมูลต่อไปนี้ของธุรกรรม TDS แต่ละธุรกรรม:</span><span class="sxs-lookup"><span data-stu-id="c9da6-120">The **Update certificate** page shows the following information for each TDS transaction:</span></span>

    - <span data-ttu-id="c9da6-121">**วันที่** – วันที่ลงรายการบัญชีของธุรกรรม</span><span class="sxs-lookup"><span data-stu-id="c9da6-121">**Date** – The posting date of the TDS transaction.</span></span>
    - <span data-ttu-id="c9da6-122">**ใบสำคัญ** – หมายเลขใบสำคัญของธุรกรรม TDS</span><span class="sxs-lookup"><span data-stu-id="c9da6-122">**Voucher** – The voucher number of the TDS transaction.</span></span>
    - <span data-ttu-id="c9da6-123">**แหล่งที่มา** – โมดูลที่มีการสร้างธุรกรรม TDS</span><span class="sxs-lookup"><span data-stu-id="c9da6-123">**Source** – The module that the TDS transaction was created in.</span></span>
    - <span data-ttu-id="c9da6-124">**บัญชี** – หมายเลขผู้จัดจำหน่าย ลูกค้า หรือบัญชีแยกประเภท ที่มีการสร้างธุรกรรม TDS ให้</span><span class="sxs-lookup"><span data-stu-id="c9da6-124">**Account** – The vendor, customer, or ledger account number that the TDS transaction was created for.</span></span>
    - <span data-ttu-id="c9da6-125">**ชื่อ** – ชื่อผู้จัดจำหน่าย ลูกค้า หรือบัญชีแยกประเภท ที่มีการสร้างธุรกรรม TDS ให้</span><span class="sxs-lookup"><span data-stu-id="c9da6-125">**Name** – The name of the vendor, customer, or ledger account that the TDS transaction was created for.</span></span>
    - <span data-ttu-id="c9da6-126">**จำนวน** – ยอดที่ TDS คำนวณได้จากยอดเงินใบแจ้งหนี้</span><span class="sxs-lookup"><span data-stu-id="c9da6-126">**Amount** – The invoice amount that the TDS was calculated on.</span></span>
    - <span data-ttu-id="c9da6-127">**ยอดภาษี** – ยอดภาษี TDS ที่คํานวณได้สำหรับธุรกรรม</span><span class="sxs-lookup"><span data-stu-id="c9da6-127">**Tax amount** – The TDS tax amount that was calculated for the transaction.</span></span>
    - <span data-ttu-id="c9da6-128">**วันที่ในใบรับรอง** – วันที่ในใบรับรอง TDS ที่ได้รับการอัปเดตแล้วของธุรกรรม TDS</span><span class="sxs-lookup"><span data-stu-id="c9da6-128">**Certificate date** – The TDS certificate date that was updated for the TDS transaction.</span></span>
    - <span data-ttu-id="c9da6-129">**หมายเลขใบรับรอง** – หมายเลขใบรับรอง TDS ที่ได้รับการอัปเดตแล้วของธุรกรรม TDS</span><span class="sxs-lookup"><span data-stu-id="c9da6-129">**Certificate number** – TDS certificate number that was updated for the TDS transaction.</span></span>

10. <span data-ttu-id="c9da6-130">บนหน้า **ใบรับรองที่จะได้รับคืน** ให้เลือกกล่องกาเครื่องหมาย **ปิด** เพื่อปิดหมายเลขใบรับรอง TDS หลังจากที่คุณเสร็จสิ้นการอัปเดตหมายเลขใบรับรองให้กับธุรกรรม TDS บนหน้า **อัปเดตใบรับรอง**</span><span class="sxs-lookup"><span data-stu-id="c9da6-130">On the **Recoverable certificates** page, select the **Closed** check box to close the TDS certificate number after you've finished updating it for TDS transactions on the **Update certificate** page.</span></span>

    <span data-ttu-id="c9da6-131">เมื่อต้องการเลือกกล่องกาเครื่องหมาย **ปิด** ให้กับเรกคอร์ดทั้งหมดในหน้า ให้เลือก **เลือกทั้งหมด**</span><span class="sxs-lookup"><span data-stu-id="c9da6-131">To select the **Closed** check box for all records on the page, select **Mark all**.</span></span>

    > [!NOTE]
    > <span data-ttu-id="c9da6-132">หมายเลขใบรับรอง TDS ที่มีการเลือกกล่องกาเครื่องหมาย **ปิด** ไว้ ไม่มีอยู่ในหน้า **อัปเดตใบรับรอง**</span><span class="sxs-lookup"><span data-stu-id="c9da6-132">TDS certificate numbers that the **Closed** check box is selected for aren't available on the **Update certificate** page.</span></span>
