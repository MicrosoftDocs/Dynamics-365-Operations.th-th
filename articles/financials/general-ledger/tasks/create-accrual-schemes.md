--- 
title: "การสร้างแบบแผนการรับรู้"
description: "คำแนะนำงานนี้ระบุขั้นตอนในการสร้างแผนงานรายการคงค้าง "
author: aprilolson
manager: AnnBe
ms.date: 8/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: LedgerAccrualTable
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 32d71167fdad65cb1dec37671999a497759ca484
ms.openlocfilehash: b08f441d0dadf8ac33197188ba8aaf85db730e8f
ms.contentlocale: th-th
ms.lasthandoff: 09/11/2018

---
# <a name="create-accrual-schemes"></a><span data-ttu-id="f8138-103">การสร้างแบบแผนการรับรู้</span><span class="sxs-lookup"><span data-stu-id="f8138-103">Create accrual schemes</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="f8138-104">คำแนะนำงานนี้ระบุขั้นตอนในการสร้างแผนงานรายการคงค้าง </span><span class="sxs-lookup"><span data-stu-id="f8138-104">This task guide steps through creating an accrual scheme.</span></span> <span data-ttu-id="f8138-105">งานนี้ใช้บริษัทสาธิต USMF </span><span class="sxs-lookup"><span data-stu-id="f8138-105">This task uses the USMF demo company.</span></span>

1. <span data-ttu-id="f8138-106">ไปที่บัญชีแยกประเภททั่วไป > การตั้งค่าสมุดรายวัน > แผนงานการค้างรับค้างจ่าย</span><span class="sxs-lookup"><span data-stu-id="f8138-106">Go to General ledger > Journal setup > Accrual schemes.</span></span>
2. <span data-ttu-id="f8138-107">คลิก สร้าง</span><span class="sxs-lookup"><span data-stu-id="f8138-107">Click New.</span></span>
3. <span data-ttu-id="f8138-108">ในฟิลด์การระบุรายการคงค้าง ให้พิมพ์ค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="f8138-108">In the Accrual identification field, type a value.</span></span>
4. <span data-ttu-id="f8138-109">ในฟิลด์คำอธิบายเกี่ยวกับแผนงานรายการคงค้าง ให้พิมพ์ค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="f8138-109">In the Description of accrual scheme field, type a value.</span></span>
5. <span data-ttu-id="f8138-110">ในฟิลด์เดบิต ให้ระบุค่าที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="f8138-110">In the Debit field, specify the desired values.</span></span>
    * <span data-ttu-id="f8138-111">บัญชีหลักที่กำหนดไว้จะแทนเดบิตบัญชีหลักในบรรทัดสมุดรายวันใบสำคัญ และยังสามารถใช้สำหรับการกลับรายการยืดเวลาซึ่งขึ้นอยู่กับธุรกรรมการรับรู้บัญชีแยกประเภท</span><span class="sxs-lookup"><span data-stu-id="f8138-111">The main account defined will replace the debit main account on the journal voucher line and it will also be used for the reversal of the deferral based on the ledger accrual transactions.</span></span>  
6. <span data-ttu-id="f8138-112">ในฟิลด์เครดิต ให้ระบุค่าที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="f8138-112">In the Credit field, specify the desired values.</span></span>
    * <span data-ttu-id="f8138-113">บัญชีหลักที่กำหนดไว้จะแทนเครดิตบัญชีหลักในบรรทัดสมุดรายวันใบสำคัญ และยังจะสามารถใช้สำหรับการกลับรายการยืดเวลาขึ้นอยู่กับธุรกรรมการรับรู้บัญชีแยกประเภท</span><span class="sxs-lookup"><span data-stu-id="f8138-113">The main account defined will replace the credit main account on the journal voucher line and it will also be used for the reversal of the deferral based on the ledger accrual transactions.</span></span>  
7. <span data-ttu-id="f8138-114">ในฟิลด์ใบสำคัญ ให้เลือกวิธีที่คุณต้องการกำหนดใบสำคัญเมื่อลงรายการบัญชีธุรกรรมแล้ว</span><span class="sxs-lookup"><span data-stu-id="f8138-114">In the Voucher field, select how you want the voucher determined when the transactions are posted.</span></span>
8. <span data-ttu-id="f8138-115">ในฟิลด์คำอธิบาย ให้พิมพ์ค่าเพื่ออธิบายธุรกรรมที่จะลงรายการบัญชี</span><span class="sxs-lookup"><span data-stu-id="f8138-115">In the Description field, type a value to describe the transactions that will be posted.</span></span>
9. <span data-ttu-id="f8138-116">ในฟิลด์ความถี่ของรอบระยะเวลา ให้เลือกความถี่ที่มีธุรกรรมเกิดขึ้น</span><span class="sxs-lookup"><span data-stu-id="f8138-116">In the Period frequency field, select how often the transactions should occur.</span></span>
10. <span data-ttu-id="f8138-117">ในฟิลด์จำนวนครั้งที่เกิดขึ้นตามรอบระยะเวลา ให้ป้อนหมายเลข</span><span class="sxs-lookup"><span data-stu-id="f8138-117">In the Number of occurrences by period field, enter a number.</span></span>
11. <span data-ttu-id="f8138-118">ในฟิลด์ลงรายการบัญชีธุรกรรม ให้เลือกเมื่อควรจะลงการทำธุรกรรม เช่น รายเดือน</span><span class="sxs-lookup"><span data-stu-id="f8138-118">In the Post transactions field, select when the transactions should be posted, such as Monthly.</span></span>


