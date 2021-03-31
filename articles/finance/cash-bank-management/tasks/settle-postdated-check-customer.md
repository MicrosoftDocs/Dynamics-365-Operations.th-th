---
title: ชำระเช็คลงวันที่ล่วงหน้าจากลูกค้า
description: 'คุณสามารถชำระเช็คลงวันที่ล่วงหน้าได้หลังจากที่เช็คได้ถูกล้างข้อมูลโดยธนาคารแล้ว '
author: kweekley
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CustPostDatedChecks, SystemDate, LedgerJournalTable, LedgerJournalTransDaily, LedgerTransVoucher
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: abcd6532c294223e768d1a01d97309e35c30edbe
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 02/15/2021
ms.locfileid: "5217421"
---
# <a name="settle-a-postdated-check-from-a-customer"></a><span data-ttu-id="f4b93-103">ชำระเช็คลงวันที่ล่วงหน้าจากลูกค้า</span><span class="sxs-lookup"><span data-stu-id="f4b93-103">Settle a postdated check from a customer</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="f4b93-104">คุณสามารถชำระเช็คลงวันที่ล่วงหน้าได้หลังจากที่เช็คได้ถูกล้างข้อมูลโดยธนาคารแล้ว </span><span class="sxs-lookup"><span data-stu-id="f4b93-104">You can settle a postdated check after the check has been cleared by the bank.</span></span> <span data-ttu-id="f4b93-105">นอกจากนี้ธุรกรรมทางการเงินนี้จะล้างข้อมูลธุรกรรมข้ามบัญชีสำหรับเช็คลงวันล่วงหน้าอีกด้วย </span><span class="sxs-lookup"><span data-stu-id="f4b93-105">This financial transaction also clears the bridge account transaction for the postdated check.</span></span> 

<span data-ttu-id="f4b93-106">งานต่อไปนี้ต้องเสร็จสมบูรณ์ก่อนที่คุณเริ่มการทำงานนี้ </span><span class="sxs-lookup"><span data-stu-id="f4b93-106">The following tasks must be complete before you start this one.</span></span>

1) <span data-ttu-id="f4b93-107">ตั้งค่าเช็คลงวันที่ล่วงหน้า</span><span class="sxs-lookup"><span data-stu-id="f4b93-107">Set up postdated checks</span></span>

2) <span data-ttu-id="f4b93-108">ลงทะเบียนและลงรายการบัญชีเช็คลงวันที่ล่วงหน้าสำหรับลูกค้า</span><span class="sxs-lookup"><span data-stu-id="f4b93-108">Register and post a postdated check for a customer</span></span> 



<span data-ttu-id="f4b93-109">บทบาทสำหรับกระบวนงานนี้คือฝ่ายการเงิน </span><span class="sxs-lookup"><span data-stu-id="f4b93-109">The role of this task guides is Treasurer.</span></span>



<span data-ttu-id="f4b93-110">กระบวนงานนี้ใช้บริษัทสาธิต USMF</span><span class="sxs-lookup"><span data-stu-id="f4b93-110">This procedure uses the USMF demo company.</span></span>

1. <span data-ttu-id="f4b93-111">ไปที่สินเชื่อและการเรียกเก็บเงิน > การสอบถามและรายงาน > การชำระเงิน > เช็คลงวันที่ล่วงหน้าของลูกค้า</span><span class="sxs-lookup"><span data-stu-id="f4b93-111">Go to Credit and collections > Inquiries and reports > Payments > Customer postdated checks.</span></span>
2. <span data-ttu-id="f4b93-112">คลิกการชำระเงิน</span><span class="sxs-lookup"><span data-stu-id="f4b93-112">Click Settle.</span></span>
3. <span data-ttu-id="f4b93-113">คลิกการชำระรายการหักบัญชี</span><span class="sxs-lookup"><span data-stu-id="f4b93-113">Click Settle clearing entries.</span></span>
    * <span data-ttu-id="f4b93-114">ชำระบัญชีลูกค้าสำหรับธุรกรรมเช็ค</span><span class="sxs-lookup"><span data-stu-id="f4b93-114">Settle the customer account for the check transaction.</span></span>  
4. <span data-ttu-id="f4b93-115">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="f4b93-115">Close the page.</span></span>
5. <span data-ttu-id="f4b93-116">ไปที่บัญชีแยกประเภททั่วไป > รายการสมุดรายวัน > สมุดรายวันทั่วไป</span><span class="sxs-lookup"><span data-stu-id="f4b93-116">Go to General ledger > Journal entries > General journals.</span></span>
6. <span data-ttu-id="f4b93-117">ในฟิลด์แสดง ให้เลือกหนึ่งตัวเลือก</span><span class="sxs-lookup"><span data-stu-id="f4b93-117">In the Show field, select an option.</span></span>
7. <span data-ttu-id="f4b93-118">เลือกหรือยกเลิกกล่องกาเครื่องหมายการแสดงเฉพาะที่ผู้ใช้ที่สร้างขึ้นเท่านั้น</span><span class="sxs-lookup"><span data-stu-id="f4b93-118">Select or clear the Show user-created only check box.</span></span>
8. <span data-ttu-id="f4b93-119">ในรายการนี้ ให้ค้นหาและเลือกเรกคอร์ดที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="f4b93-119">In the list, find and select the desired record.</span></span>
9. <span data-ttu-id="f4b93-120">คลิกรายการ</span><span class="sxs-lookup"><span data-stu-id="f4b93-120">Click Lines.</span></span>
10. <span data-ttu-id="f4b93-121">คลิกใบสำคัญ</span><span class="sxs-lookup"><span data-stu-id="f4b93-121">Click Voucher.</span></span>
11. <span data-ttu-id="f4b93-122">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="f4b93-122">Close the page.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]