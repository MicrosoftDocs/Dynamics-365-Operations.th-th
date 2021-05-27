---
title: อัพเดตหมายเลขและวันที่ของใบรับรองสำหรับธุรกรรม TDS
description: หัวข้อนี้อธิบายวิธีการอัพเดตหมายเลขและวันที่ของใบรับรองที่จะได้รับคืน ซึ่งถูกบันทึกสำหรับผู้จัดจำหน่าย ลูกค้า และบัญชีแยกประเภท สำหรับภาษีที่หักที่ต้นทาง (TDS)
author: kailiang
ms.date: 02/12/2021
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
ms.openlocfilehash: 248de8e12703a84482b67d0899857a6efb33531c
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 05/11/2021
ms.locfileid: "6023624"
---
# <a name="update-certificate-numbers-and-dates-for-tds-transactions"></a><span data-ttu-id="8ae8c-103">อัพเดตหมายเลขและวันที่ของใบรับรองสำหรับธุรกรรม TDS</span><span class="sxs-lookup"><span data-stu-id="8ae8c-103">Update certificate numbers and dates for TDS transactions</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="8ae8c-104">หัวข้อนี้อธิบายวิธีการอัพเดตหมายเลขและวันที่ของใบรับรองที่จะได้รับคืน ซึ่งถูกบันทึกสำหรับผู้จัดจำหน่าย ลูกค้า และบัญชีแยกประเภท สำหรับภาษีที่หักที่ต้นทาง (TDS)</span><span class="sxs-lookup"><span data-stu-id="8ae8c-104">This topic explains how to update the recoverable certificate numbers and dates that were recorded for vendor, customer, and ledger accounts for Tax Deducted at Source (TDS).</span></span> <span data-ttu-id="8ae8c-105">คุณสามารถดูใบรับรองสำหรับธุรกรรม TDS ในหน้า **ใบรับรองที่จะได้รับคืน**</span><span class="sxs-lookup"><span data-stu-id="8ae8c-105">You can view the certificates for TDS transactions on the **Recoverable certificates** page.</span></span> <span data-ttu-id="8ae8c-106">คุณสามารถอัพเดตใบรับรองได้โดยใช้หน้า **อัพเดตใบรับรอง**</span><span class="sxs-lookup"><span data-stu-id="8ae8c-106">You can update the certificates by using the **Update Certificates** page.</span></span>

<span data-ttu-id="8ae8c-107">ปฏิบัติตามขั้นตอนเหล่านี้เพื่ออัพเดตหมายเลขและวันที่ใบรับรองสำหรับธุรกรรม TDS</span><span class="sxs-lookup"><span data-stu-id="8ae8c-107">Follow these steps to update certificate numbers and dates for TDS transactions.</span></span>

1. <span data-ttu-id="8ae8c-108">ไปที่ **ภาษี \> ประกาศต่างๆ \> ภาษีหัก ณ ที่จ่าย \> อัพเดตใบรับรอง**</span><span class="sxs-lookup"><span data-stu-id="8ae8c-108">Go to **Tax \> Declarations \> Withholding tax \> Update certificate**.</span></span>

    <span data-ttu-id="8ae8c-109">[![หน้าอัพเดตใบรับรอง](./media/apac-ind-TDS-45.png)](./media/apac-ind-TDS-45.png)</span><span class="sxs-lookup"><span data-stu-id="8ae8c-109">[![Update certificate page](./media/apac-ind-TDS-45.png)](./media/apac-ind-TDS-45.png)</span></span>

2. <span data-ttu-id="8ae8c-110">ในหน้า **อัพเดตใบรับรอง** ในส่วน **เลือก** ในฟิลด์ **ชนิดภาษี** ให้เลือก **TDS**</span><span class="sxs-lookup"><span data-stu-id="8ae8c-110">On the **Update certificate** page, in the **Select** section, in the **Tax type** field, select **TDS**.</span></span>
3. <span data-ttu-id="8ae8c-111">ในฟิลด์ **หมายเลขใบรับรอง** ให้เลือกหมายเลขใบรับรอง TDS ของลูกค้าหรือผู้จัดจำหน่าย</span><span class="sxs-lookup"><span data-stu-id="8ae8c-111">In the **Certificate number** field, select the customer's or vendor's TDS certificate number.</span></span>

    > [!NOTE]
    > <span data-ttu-id="8ae8c-112">ฟิลด์ **หมายเลขใบรับรอง** แสดงรายการเฉพาะหมายเลขใบรับรอง TDS ที่กล่องกาเครื่องหมาย **ปิด** ถูกยกเลิกการเลือก **ใบรับรองที่จะได้รับคืน**</span><span class="sxs-lookup"><span data-stu-id="8ae8c-112">The **Certificate number** field lists only TDS certificate numbers that the **Closed** check box is cleared for on the **Recoverable certificates** page.</span></span>

    <span data-ttu-id="8ae8c-113">ในฟิลด์ **วันที่ของใบรับรอง** แสดงวันที่ของใบรับรอง</span><span class="sxs-lookup"><span data-stu-id="8ae8c-113">The **Certificate date** field shows the certificate date.</span></span> <span data-ttu-id="8ae8c-114">ฟิลด์ **ชนิดบัญชี** แสดงชนิดของบัญชีที่ได้รับหมายเลขใบรับรอง TDS และฟิลด์ **ชื่อ** จะแสดงชื่อของบัญชี</span><span class="sxs-lookup"><span data-stu-id="8ae8c-114">The **Account type** field shows the type of account that the TDS certificate number is received for, and the **Name** field shows the name of the account.</span></span>

5. <span data-ttu-id="8ae8c-115">ในฟิลด์ **วันที่เริ่มต้น** เเละ **วันที่สิ้นสุด** เลือกวันที่เริ่มต้นและวันที่สิ้นสุดของรอบระยะเวลาเพื่อแสดงธุรกรรม TDS</span><span class="sxs-lookup"><span data-stu-id="8ae8c-115">In the **From date** and **To date** fields, select the start and end dates of the period to show the TDS transactions for.</span></span>
6. <span data-ttu-id="8ae8c-116">เลือก **แสดงข้อมูล** เพื่อดูธุรกรรม TDS ที่ถูกลงรายการบัญชีในระหว่างรอบระยะเวลาที่เลือก</span><span class="sxs-lookup"><span data-stu-id="8ae8c-116">Select **Show data** to view the TDS transactions that were posted during the selected period.</span></span>

    <span data-ttu-id="8ae8c-117">บนแท็บ **ภาพรวม** กริดในบานหน้าต่างด้านบนจะแสดงข้อมูลต่อไปนี้เกี่ยวกับธุรกรรม TDS แต่ละรายการที่ลงรายการบัญชีไว้สำหรับผู้จัดจำหน่ายหรือลูกค้าในระหว่างรอบระยะเวลาที่เลือก:</span><span class="sxs-lookup"><span data-stu-id="8ae8c-117">On the **Overview** tab, the grid in the upper pane shows the following information about each TDS transaction that was posted for the vendor or customer during the selected period:</span></span>

    - <span data-ttu-id="8ae8c-118">**ใบสำคัญ** – หมายเลขใบสำคัญของธุรกรรม TDS</span><span class="sxs-lookup"><span data-stu-id="8ae8c-118">**Voucher** – The voucher number of the TDS transaction.</span></span>
    - <span data-ttu-id="8ae8c-119">**วันที่** – วันที่ของธุรกรรม TDS</span><span class="sxs-lookup"><span data-stu-id="8ae8c-119">**Date** – The date of the TDS transaction.</span></span>
    - <span data-ttu-id="8ae8c-120">**จำนวน** – ยอดที่ TDS คำนวณได้จากยอดเงินใบแจ้งหนี้</span><span class="sxs-lookup"><span data-stu-id="8ae8c-120">**Amount** – The invoice amount that the TDS was calculated on.</span></span>
    - <span data-ttu-id="8ae8c-121">**ยอดภาษี** – ยอดภาษี TDS ที่คํานวณได้สำหรับธุรกรรม</span><span class="sxs-lookup"><span data-stu-id="8ae8c-121">**Tax amount** – The TDS tax amount that was calculated for the transaction.</span></span>

7. <span data-ttu-id="8ae8c-122">เมื่อต้องการย้ายธุรกรรม TDS เฉพาะจากกริดด้านบนไปยังกริดด้านล่าง ให้เลือกธุรกรรม แล้วจากนั้น เลือก **รวม**</span><span class="sxs-lookup"><span data-stu-id="8ae8c-122">To move specific TDS transactions from the upper grid to the lower grid, select the transactions, and then select **Include**.</span></span> <span data-ttu-id="8ae8c-123">หรือเลือก **รวมทั้งหมด** เพื่อย้ายธุรกรรม TDS ทั้งหมดจากกริดด้านบนไปยังกริดด้านล่าง</span><span class="sxs-lookup"><span data-stu-id="8ae8c-123">Alternatively, select **Include all** to move all TDS transactions from the upper grid to the lower grid.</span></span>

    <span data-ttu-id="8ae8c-124">เมื่อต้องการย้ายธุรกรรม TDS เฉพาะหรือธุรกรรม TDS ทั้งหมดจากกริดด้านล่างไปยังกริดด้านบน ให้ใช้ปุ่ม **ไม่รวม** หรือ **ไม่รวมทั้งหมด**</span><span class="sxs-lookup"><span data-stu-id="8ae8c-124">To move specific TDS transactions or all TDS transactions from the lower grid to the upper grid, use the **Exclude** or **Exclude all** button.</span></span>

8. <span data-ttu-id="8ae8c-125">เลือก **อัพเดต** เพื่ออัพเดตฟิลด์ **หมายเลขใบรับรอง** และ **วันที่ของใบรับรอง** สำหรับธุรกรรม TDS ในกริดด้านล่าง</span><span class="sxs-lookup"><span data-stu-id="8ae8c-125">Select **Update** to update the **Certificate number** and **Certificate date** fields for TDS transactions in the lower grid.</span></span>
10. <span data-ttu-id="8ae8c-126">ไปที่ **ภาษี \> ภาษีทางอ้อม \> ภาษีหัก ณ ที่จ่าย \> ใบรับรองที่จะได้รับคืน** และเลือก **การสอบถาม** เพื่อดูรายการธุรกรรมที่อัพเดตซึ่งมีหมายเลขใบรับรองใหม่บนหน้า **ธุรกรรมใบรับรอง**</span><span class="sxs-lookup"><span data-stu-id="8ae8c-126">Go to **Tax \> Indirect taxes \> Withholding tax \> Recoverable certificate**, and select **Inquiry** to view the updated transaction lines that have the new certificate numbers on the **Certificate transactions** page.</span></span>

    <span data-ttu-id="8ae8c-127">[![หน้าธุรกรรมใบรับรอง](./media/apac-ind-TDS-46.png)](./media/apac-ind-TDS-46.png)</span><span class="sxs-lookup"><span data-stu-id="8ae8c-127">[![Certificate transactions page](./media/apac-ind-TDS-46.png)](./media/apac-ind-TDS-46.png)</span></span>
