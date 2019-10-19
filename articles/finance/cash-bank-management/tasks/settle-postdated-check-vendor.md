---
title: ชำระเช็คลงวันที่ล่วงหน้าสำหรับผู้จัดจำหน่าย
description: 'ชำระเช็คลงวันที่ล่วงหน้าที่ออกให้กับผู้จัดจำหน่ายเมื่อธุรกรรมเช็คได้ถูกล้างโดยธนาคารแล้ว หลังจากเช็คได้พ้นกำหนดและถูกล้างโดยธนาคาร '
author: kweekley
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: VendPostDatedChecks, LedgerJournalTable, LedgerJournalTransDaily, LedgerTransVoucher
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 6d935ec24d97ca76a088cbe41d57c12c6e8a6689
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 09/27/2019
ms.locfileid: "2188061"
---
# <a name="settle-a-postdated-check-for-a-vendor"></a><span data-ttu-id="16db2-103">ชำระเช็คลงวันที่ล่วงหน้าสำหรับผู้จัดจำหน่าย</span><span class="sxs-lookup"><span data-stu-id="16db2-103">Settle a postdated check for a vendor</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="16db2-104">ชำระเช็คลงวันที่ล่วงหน้าที่ออกให้กับผู้จัดจำหน่ายเมื่อธุรกรรมเช็คได้ถูกล้างโดยธนาคารแล้ว หลังจากเช็คได้พ้นกำหนดและถูกล้างโดยธนาคาร </span><span class="sxs-lookup"><span data-stu-id="16db2-104">Settle a postdated check issued to a vendor when the bank has cleared the check transaction after the check has been overdue and cleared by the bank.</span></span> 

<span data-ttu-id="16db2-105">กระบวนงานต่อไปนี้ต้องเสร็จสมบูรณ์ก่อนที่คุณเริ่มการทำงานนี้ </span><span class="sxs-lookup"><span data-stu-id="16db2-105">Complete the following procedures before you start this one.</span></span>

1) <span data-ttu-id="16db2-106">ตั้งค่าเช็คลงวันที่ล่วงหน้า</span><span class="sxs-lookup"><span data-stu-id="16db2-106">Set up postdated checks</span></span>

2) <span data-ttu-id="16db2-107">ลงทะเบียนและลงรายการบัญชีเช็คลงวันที่ล่วงหน้าสำหรับผู้จัดจำหน่าย</span><span class="sxs-lookup"><span data-stu-id="16db2-107">Register and post a postdated check for a vendor</span></span>



<span data-ttu-id="16db2-108">บทบาทของกระบวนงานนี้คือเจ้าหน้าที่ฝ่ายบริหารเงิน </span><span class="sxs-lookup"><span data-stu-id="16db2-108">The role of this procedure is Treasurer.</span></span> <span data-ttu-id="16db2-109">กระบวนงานนี้ใช้บริษัทสาธิต USMF</span><span class="sxs-lookup"><span data-stu-id="16db2-109">This procedure uses the USMF demo company.</span></span>

1. <span data-ttu-id="16db2-110">ไปที่บัญชีเจ้าหนี้ > การชำระเงิน > เช็คลงวันที่ล่วงหน้าของผู้จัดจำหน่าย</span><span class="sxs-lookup"><span data-stu-id="16db2-110">Go to Accounts payable > Payments > Vendor postdated checks.</span></span>
2. <span data-ttu-id="16db2-111">คลิกการชำระเงิน</span><span class="sxs-lookup"><span data-stu-id="16db2-111">Click Settle.</span></span>
3. <span data-ttu-id="16db2-112">คลิกการชำระรายการหักบัญชี</span><span class="sxs-lookup"><span data-stu-id="16db2-112">Click Settle clearing entries.</span></span>
    * <span data-ttu-id="16db2-113">ชำระบัญชีผู้จัดจำหน่ายสำหรับธุรกรรมเช็ค</span><span class="sxs-lookup"><span data-stu-id="16db2-113">Settle the vendor account for the check transaction.</span></span>  
4. <span data-ttu-id="16db2-114">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="16db2-114">Close the page.</span></span>
5. <span data-ttu-id="16db2-115">ไปที่บัญชีแยกประเภททั่วไป > รายการสมุดรายวัน > สมุดรายวันทั่วไป</span><span class="sxs-lookup"><span data-stu-id="16db2-115">Go to General ledger > Journal entries > General journals.</span></span>
6. <span data-ttu-id="16db2-116">ในฟิลด์แสดง ให้เลือก "ทั้งหมด"</span><span class="sxs-lookup"><span data-stu-id="16db2-116">In the Show field, select 'All'.</span></span>
7. <span data-ttu-id="16db2-117">เลือกหรือยกเลิกกล่องกาเครื่องหมายการแสดงเฉพาะที่ผู้ใช้ที่สร้างขึ้นเท่านั้น</span><span class="sxs-lookup"><span data-stu-id="16db2-117">Select or clear the Show user-created only check box.</span></span>
8. <span data-ttu-id="16db2-118">ในรายการนี้ ให้ทำเครื่องหมายแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="16db2-118">In the list, mark the selected row.</span></span>
9. <span data-ttu-id="16db2-119">คลิกรายการ</span><span class="sxs-lookup"><span data-stu-id="16db2-119">Click Lines.</span></span>
10. <span data-ttu-id="16db2-120">คลิกใบสำคัญ</span><span class="sxs-lookup"><span data-stu-id="16db2-120">Click Voucher.</span></span>
11. <span data-ttu-id="16db2-121">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="16db2-121">Close the page.</span></span>

