--- 
title: "ลงทะเบียนและลงรายการบัญชีเช็คลงวันที่ล่วงหน้าสำหรับลูกค้า"
description: "คุณสามารถลงทะเบียนรายละเอียดเกี่ยวกับเช็คลงวันที่ล่วงหน้าที่ได้รับจากลูกค้า"
author: kweekley
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Operations
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 1610036815349f625a67d5dd67260114d42fff97
ms.contentlocale: th-th
ms.lasthandoff: 09/29/2017

---
# <a name="register-and-post-a-postdated-check-for-a-customer"></a><span data-ttu-id="10eb2-103">ลงทะเบียนและลงรายการบัญชีเช็คลงวันที่ล่วงหน้าสำหรับลูกค้า</span><span class="sxs-lookup"><span data-stu-id="10eb2-103">Register and post a postdated check for a customer</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="10eb2-104">คุณสามารถลงทะเบียนรายละเอียดเกี่ยวกับเช็คลงวันที่ล่วงหน้าที่ได้รับจากลูกค้า</span><span class="sxs-lookup"><span data-stu-id="10eb2-104">You can register details of a postdated cheque received from a customer.</span></span> <span data-ttu-id="10eb2-105">คุณสามารถลงรายการบัญชีเช็คลงวันที่ล่วงหน้าและสร้างธุรกรรมทางการเงิน</span><span class="sxs-lookup"><span data-stu-id="10eb2-105">You can also post the postdated cheque and generate financial transactions.</span></span>   <span data-ttu-id="10eb2-106">ดำเนินงานต่อไปนี้ให้เสร็จสมบูรณ์ก่อนที่คุณจะลงทะเบียนและลงรายการบัญชีเช็คที่ได้รับจากลูกค้า:   • ตั้งค่าเช็คลงวันที่ล่วงหน้าในหน้าการจัดการเงินสดและธนาคาร • ตั้งค่าวิธีการชำระเงินสำหรับเช็คลงวันที่ล่วงหน้า บทบาทสำหรับกระบวนงานนี้คือฝ่ายการเงิน</span><span class="sxs-lookup"><span data-stu-id="10eb2-106">Complete the following tasks before you register and post a postdated cheque received from a customer:   • Set up postdated Cheques in the Cash and bank management page • Set up a method of payment for postdated Cheques   The role for this procedure is Treasurer.</span></span> <span data-ttu-id="10eb2-107">กระบวนงานนี้ใช้บริษัทสาธิต USMF</span><span class="sxs-lookup"><span data-stu-id="10eb2-107">This procedure uses the USMF demo company.</span></span>

1. <span data-ttu-id="10eb2-108">ไปที่บัญชีเจ้าหนี้ > การชำระเงิน > สมุดรายวันการชำระเงิน</span><span class="sxs-lookup"><span data-stu-id="10eb2-108">Go to Accounts receivable > Payments > Payment journal.</span></span>
2. <span data-ttu-id="10eb2-109">คลิก สร้าง</span><span class="sxs-lookup"><span data-stu-id="10eb2-109">Click New.</span></span>
3. <span data-ttu-id="10eb2-110">ในฟิลด์ชื่อ ให้พิมพ์ค่า </span><span class="sxs-lookup"><span data-stu-id="10eb2-110">In the Name field, type a value.</span></span>
4. <span data-ttu-id="10eb2-111">คลิก รายการ</span><span class="sxs-lookup"><span data-stu-id="10eb2-111">Click Lines.</span></span>
5. <span data-ttu-id="10eb2-112">ในรายการนี้ ให้ทำเครื่องหมายแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="10eb2-112">In the list, mark the selected row.</span></span>
6. <span data-ttu-id="10eb2-113">ในฟิลด์บัญชี ให้ระบุค่าที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="10eb2-113">In the Account field, specify the desired values.</span></span>
7. <span data-ttu-id="10eb2-114">ในฟิลด์เครดิต ให้ป้อนหมายเลข</span><span class="sxs-lookup"><span data-stu-id="10eb2-114">In the Credit field, enter a number.</span></span>
    * <span data-ttu-id="10eb2-115">ป้อนยอดเงินที่ระบุในเช็คลงวันที่ล่วงหน้า</span><span class="sxs-lookup"><span data-stu-id="10eb2-115">Enter the amount specified in the postdated cheque.</span></span>  
8. <span data-ttu-id="10eb2-116">คลิกแท็บการชำระเงิน</span><span class="sxs-lookup"><span data-stu-id="10eb2-116">Click the Payment tab.</span></span>
9. <span data-ttu-id="10eb2-117">ในฟิลด์วิธีการชำระเงิน ให้พิมพ์ค่า</span><span class="sxs-lookup"><span data-stu-id="10eb2-117">In the Method of payment field, type a value.</span></span>
    * <span data-ttu-id="10eb2-118">เลือกวิธีการชำระเงินสำหรับเช็คลงวันที่ล่วงหน้า</span><span class="sxs-lookup"><span data-stu-id="10eb2-118">Select the method of payment for the postdated cheque</span></span>  
10. <span data-ttu-id="10eb2-119">คลิกแท็บเช็คลงวันที่ล่วงหน้า</span><span class="sxs-lookup"><span data-stu-id="10eb2-119">Click the Postdated checks tab.</span></span>
11. <span data-ttu-id="10eb2-120">ในฟิลด์วันครบกำหนด ให้ป้อนวันที่</span><span class="sxs-lookup"><span data-stu-id="10eb2-120">In the Maturity date field, enter a date.</span></span>
    * <span data-ttu-id="10eb2-121">ป้อนวันที่ที่ครบกำหนดการชำระเงินสำหรับเช็คลงวันที่ล่วงหน้า</span><span class="sxs-lookup"><span data-stu-id="10eb2-121">Enter the date when the postdated cheque is due for payment.</span></span>  
12. <span data-ttu-id="10eb2-122">ในฟิลด์สาขาธนาคารผู้ออก ให้พิมพ์ค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="10eb2-122">In the Issuing bank branch field, type a value.</span></span>
    * <span data-ttu-id="10eb2-123">ป้อนรายละเอียดธนาคารของเช็คลงวันล่วงหน้า</span><span class="sxs-lookup"><span data-stu-id="10eb2-123">Enter the bank details of the postdated cheque.</span></span>  
13. <span data-ttu-id="10eb2-124">ในฟิลด์หมายเลขเช็ค ให้พิมพ์ค่า</span><span class="sxs-lookup"><span data-stu-id="10eb2-124">In the cheque number field, type a value.</span></span>
14. <span data-ttu-id="10eb2-125">ในฟิลด์ชื่อธนาคารผู้ออก ให้พิมพ์ค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="10eb2-125">In the Issuing bank name field, type a value.</span></span>
    * <span data-ttu-id="10eb2-126">ป้อนรายละเอียดธนาคารของเช็คลงวันล่วงหน้า</span><span class="sxs-lookup"><span data-stu-id="10eb2-126">Enter the bank details of the postdated check.</span></span>  
15. <span data-ttu-id="10eb2-127">คลิก ลงรายการบัญชี</span><span class="sxs-lookup"><span data-stu-id="10eb2-127">Click Post.</span></span>
16. <span data-ttu-id="10eb2-128">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="10eb2-128">Close the page.</span></span>


