---
title: ภาพรวมของหลักการลงบัญชีพึงรับพึงจ่าย
description: บทความนี้อธิบายถึงการรับรู้ และแสดงข้อมูลเกี่ยวกับวิธีการตั้งค่า และสร้างธุรกรรม
author: aprilolson
manager: AnnBe
ms.date: 01/11/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerAccuralTable
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 14131
ms.assetid: 0489b59a-37a7-4a78-87bf-4b597e9efad9
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 4b97055f7eac12e3e82d028a0097ca926e5c355a
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 08/01/2019
ms.locfileid: "1839652"
---
# <a name="accruals-overview"></a><span data-ttu-id="9e23b-103">ภาพรวมของหลักการลงบัญชีพึงรับพึงจ่าย</span><span class="sxs-lookup"><span data-stu-id="9e23b-103">Accruals overview</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="9e23b-104">บทความนี้อธิบายถึงการรับรู้ และแสดงข้อมูลเกี่ยวกับวิธีการตั้งค่า และสร้างธุรกรรม</span><span class="sxs-lookup"><span data-stu-id="9e23b-104">This article describes accruals, and provides information about how to set them up and create transactions.</span></span>

<span data-ttu-id="9e23b-105">รายการคงค้างจะใช้ในการลงบัญชีพึงรับพึงจ่ายเพื่อติดตามรายได้ที่จะทราบในรอบระยะเวลาที่จะได้รับเงิน ไม่ใช่ตอนที่ชำระเงิน และเพื่อติดตามค่าใช้จ่ายต่างๆ (ต้นทุน) ซึ่งเป็นที่จะระลึกได้เมื่อเกิดขึ้น ไม่ใช่เมื่อชำระเงิน</span><span class="sxs-lookup"><span data-stu-id="9e23b-105">Accruals are used in accrual accounting to track revenue that is recognized in the period that it's earned in, not when payment is received, and to track expenses (costs) that are recognized when they occur, not when payment is made.</span></span>

## <a name="accrual-schemes"></a><span data-ttu-id="9e23b-106">แผนงานการค้างรับค้างจ่าย</span><span class="sxs-lookup"><span data-stu-id="9e23b-106">Accrual schemes</span></span>
<span data-ttu-id="9e23b-107">ใช้แผนงานการค้างรับค้างจ่ายในการตั้งค่ารายได้รอการตัดบัญชีและต้นทุน และสามารถใช้แผนงานการค้างรับค้างจ่ายเดียวกันสำหรับทั้งรายได้และต้นทุน</span><span class="sxs-lookup"><span data-stu-id="9e23b-107">Accrual schemes are used to set up the deferred revenue and costs, and the same accrual scheme can be used for both revenue and costs.</span></span> <span data-ttu-id="9e23b-108">การรับรู้บัญชีแยกประเภทจะกระจายต้นทุน หรือรายได้ของบรรทัดสมุดรายวันเพื่อที่จะได้จดจำต้นทุนและรายได้ในรอบระยะเวลาที่เหมาะสม</span><span class="sxs-lookup"><span data-stu-id="9e23b-108">Ledger accruals redistribute the costs or revenue of a journal line so that the costs and revenues are recognized in the appropriate periods.</span></span> <span data-ttu-id="9e23b-109">ในหน้า **แผนงานการค้างรับค้างจ่าย** คุณระบุเดบิตและบัญชีเครดิตที่จะใช้เมื่อได้ใช้แผนงานการค้างรับค้างจ่ายนั้น</span><span class="sxs-lookup"><span data-stu-id="9e23b-109">On the **Accrual scheme** page, you specify the debit and the credit accounts that will be used when the accrual scheme is applied.</span></span>

-   <span data-ttu-id="9e23b-110">**เดบิต**– บัญชีหลักที่คุณกำหนดจะแทนบัญชีเดบิตหลักในบรรทัดสมุดรายวันใบสำคัญ</span><span class="sxs-lookup"><span data-stu-id="9e23b-110">**Debit** – The main account that you define will replace the debit main account on the journal voucher line.</span></span> <span data-ttu-id="9e23b-111">บัญชีนี้จะใช้สำหรับการกลับรายการยืดเวลา ขึ้นอยู่กับธุรกรรมค้างรับค้างจ่ายในบัญชีแยกประเภท</span><span class="sxs-lookup"><span data-stu-id="9e23b-111">This account will also be used for the reversal of the deferral, based on the ledger accrual transactions.</span></span>
-   <span data-ttu-id="9e23b-112">**เครดิต**– บัญชีหลักที่คุณกำหนดจะแทนบัญชีเครดิตหลักในบรรทัดสมุดรายวันใบสำคัญ</span><span class="sxs-lookup"><span data-stu-id="9e23b-112">**Credit** – the main account that you define will replace the credit main account on the journal voucher line.</span></span> <span data-ttu-id="9e23b-113">บัญชีนี้จะใช้สำหรับการกลับรายการยืดเวลา ขึ้นอยู่กับธุรกรรมค้างรับค้างจ่ายในบัญชีแยกประเภท</span><span class="sxs-lookup"><span data-stu-id="9e23b-113">This account will also be used for the reversal of the deferral, based on the ledger accrual transactions.</span></span>

<span data-ttu-id="9e23b-114">หลังจากที่คุณกำหนดว่าจะใช้บัญชีใด คุณสามารถระบุวิธีสร้างหมายเลขใบสำคัญเมื่อสร้างสร้างธุรกรรมคงค้าง</span><span class="sxs-lookup"><span data-stu-id="9e23b-114">After you determine which accounts to use, you can specify how the voucher number is created when accrual transactions are created.</span></span> <span data-ttu-id="9e23b-115">คุณยังสามารถระบุว่า ธุรกรรมที่เกิดขึ้น จำนวนครั้งที่สร้างธุรกรรม และตอนธุรกรรมที่จะลงรายการบัญชีนั้นบ่อยครั้งเพียงใด</span><span class="sxs-lookup"><span data-stu-id="9e23b-115">You can also specify how often the transactions occur, the number of times that the transactions are created, and when the transactions are posted.</span></span> <span data-ttu-id="9e23b-116">หลังจากที่มีการสร้างแผนงานการค้างรับค้างจ่าย คุณสามารถใช้สมุดรายวันบางเล่มโดยการใช้ฟังก์ชันการรับรู้บัญชีแยกประเภทได้</span><span class="sxs-lookup"><span data-stu-id="9e23b-116">After the accrual scheme has been created, you can use it in some of the journals by using the Ledger accruals function.</span></span>

## <a name="ledger-accruals"></a><span data-ttu-id="9e23b-117">รายการค้างรับค้างจ่ายในบัญชีแยกประเภท</span><span class="sxs-lookup"><span data-stu-id="9e23b-117">Ledger accruals</span></span>
<span data-ttu-id="9e23b-118">เมื่อคุณป้อนสมุดรายวัน คุณสามารถคลิก **การรับรู้บัญชีแยกประเภท** ในเมนู **ฟังก์ชัน** ได้</span><span class="sxs-lookup"><span data-stu-id="9e23b-118">When you enter a journal, you can click **Ledger accruals** on the **Functions** menu.</span></span> <span data-ttu-id="9e23b-119">จากนั้น เมื่อคุณเลือกแบบแผนการรับรู้ คุณจะเห็นฐานจำนวนเงินจากสมุดรายวันที่จะครอบคลุมรอบระยะเวลา ตามที่กำหนดตามแผนงานการค้างรับค้างจ่าย</span><span class="sxs-lookup"><span data-stu-id="9e23b-119">Then, when you select the accrual scheme, you will see the base amount from the journal that will be spread over the period, as determined by the accrual scheme.</span></span> <span data-ttu-id="9e23b-120">ตัวอย่างเช่น ถ้าคุณชำระเงินประกันภัยของพนักงานสำหรับตลอดทั้งปีในเดือนมกราคม และยอดเงินเป็น 12,000 คุณต้องจำค่าใช้จ่ายในแต่ละเดือน</span><span class="sxs-lookup"><span data-stu-id="9e23b-120">For example, if you pay an employee's insurance for the whole year in January, and the amount is 12,000, you must recognize that expense each month.</span></span> <span data-ttu-id="9e23b-121">คุณสามารถเลือกวันที่เริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="9e23b-121">You can select the start date.</span></span> <span data-ttu-id="9e23b-122">คุณยังสามารถระบุว่า ยอดเงินสะสมนั้นขึ้นกับบัญชีหรือบัญชีตรงข้าม</span><span class="sxs-lookup"><span data-stu-id="9e23b-122">You can also specify whether the amount that is accrued is based on the account or the offset account.</span></span> <span data-ttu-id="9e23b-123">หลังจากที่คุณทางการเลือกของคุณ คลิก **ธุรกรรม** เพื่อดูธุรกรรมทั้งหมดที่สร้างขึ้นโดยยึดตามแผนงานการค้างรับค้างจ่าย</span><span class="sxs-lookup"><span data-stu-id="9e23b-123">After you make your selections, click **Transactions** to view all the transactions that have been created based on the accrual scheme.</span></span> <span data-ttu-id="9e23b-124">ตัวอย่างเช่น ถ้าคุณกระจายยอดเงิน 12,000 ในการใช้จ่ายค่าประกันภัยมากกว่าปี ในแต่ละเดือนคุณจะเห็นยอด 1,000</span><span class="sxs-lookup"><span data-stu-id="9e23b-124">For example, if you spread the 12,000 in insurance expenses over the year, you will see 1,000 for each month.</span></span> <span data-ttu-id="9e23b-125">หลังจากที่คุณลงรายการบัญชีสมุดรายวัน คุณสามารถดูธุรกรรม โดยการใช้หน้าการสอบถาม **ธุรกรรมใบสำคัญ** ได้</span><span class="sxs-lookup"><span data-stu-id="9e23b-125">After you post the journal, you can view the transactions by using the **Voucher transactions** inquiry page.</span></span> <span data-ttu-id="9e23b-126">ถ้าไม่สามารถใช้แผนงานการค้างรับค้างจ่าย (ตัวอย่างเช่น เมื่อใบแจ้งหนี้ใบสั่งขายหรือใบแจ้งหนี้ใบสั่งซื้อที่เกี่ยวข้องกัน) คุณสามารถเครดิตยอดเงินจ่ายล่วงหน้า และเดบิตยอดค่าใช้จ่าย</span><span class="sxs-lookup"><span data-stu-id="9e23b-126">If an accrual scheme can't be applied (for example, when a sales order invoice or purchase order invoice is involved), you can credit the prepaid amount and debit the expense amount.</span></span> <span data-ttu-id="9e23b-127">คุณสามารถเลือก **ออฟเซ็ต** เมื่อคุณใช้แผนงานการค้างรับค้างจ่ายได้</span><span class="sxs-lookup"><span data-stu-id="9e23b-127">You can then select **Offset** when you apply the accrual scheme.</span></span>


<span data-ttu-id="9e23b-128">สำหรับข้อมูลเพิ่มเติม โปรดดู [สร้างแผนงานการค้างรับค้างจ่าย](tasks/create-accrual-schemes.md) และ [สร้างธุรกรรมค้างรับค้างจ่ายในบัญชีแยกประเภท](tasks/create-ledger-accrual-transactions.md)</span><span class="sxs-lookup"><span data-stu-id="9e23b-128">For more information, see [Create accrual schemes](tasks/create-accrual-schemes.md) and [Create ledger accrual transactions](tasks/create-ledger-accrual-transactions.md).</span></span>
