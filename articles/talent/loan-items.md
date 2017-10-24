---
title: "จัดการสินค้าที่ให้ยืมแก่ผู้ปฏิบัติงาน"
description: "สินค้าที่กู้ยืมมีเรกคอร์ดซึ่งช่วยให้ผู้จัดการติดตามสินค้าทางกายภาพที่บริษัทของคุณให้ผู้ปฏิบัติงานยืม"
author: kherr75
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-talent
ms.technology: 
ms.search.form: HcmLoanItem, HcmLoanType, HcmPersonLoan
audience: Application User
ms.reviewer: rschloma
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 3581
ms.assetid: b14bdddb-f10e-4619-9f91-8c88439da862
ms.search.region: Global
ms.author: kherr
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Talent July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 17fb54c07f817b6f4a65c01cd0277c8d677e2e78
ms.contentlocale: th-th
ms.lasthandoff: 09/29/2017

---

# <a name="manage-items-lent-to-workers"></a><span data-ttu-id="b2054-103">จัดการสินค้าที่ให้ยืมแก่ผู้ปฏิบัติงาน</span><span class="sxs-lookup"><span data-stu-id="b2054-103">Manage items lent to workers</span></span>

[!include[banner](includes/banner.md)]


<span data-ttu-id="b2054-104">สินค้าที่กู้ยืมมีเรกคอร์ดซึ่งช่วยให้ผู้จัดการติดตามสินค้าทางกายภาพที่บริษัทของคุณให้ผู้ปฏิบัติงานยืม</span><span class="sxs-lookup"><span data-stu-id="b2054-104">Loan items are records that help managers track the physical items that your company lends to its workers.</span></span> 

<span data-ttu-id="b2054-105">เนื้อหาต่อไปนี้แสดงรายการตัวอย่างของสินค้าที่บริษัทอาจให้ผู้ปฏิบัติงานยืม:</span><span class="sxs-lookup"><span data-stu-id="b2054-105">The following points list examples of items that a company might lend to workers:</span></span>
-   <span data-ttu-id="b2054-106">โทรศัพท์มือถือ</span><span class="sxs-lookup"><span data-stu-id="b2054-106">Mobile telephones</span></span>
-   <span data-ttu-id="b2054-107">รถยนต์</span><span class="sxs-lookup"><span data-stu-id="b2054-107">Automobiles</span></span>
-   <span data-ttu-id="b2054-108">อุปกรณ์คอมพิวเตอร์</span><span class="sxs-lookup"><span data-stu-id="b2054-108">Computer equipment</span></span>

<span data-ttu-id="b2054-109">สินค้าที่มีอยู่จริงแต่ละรายการต้องมีสินค้าให้กู้ยืมที่สอดคล้องกัน</span><span class="sxs-lookup"><span data-stu-id="b2054-109">Each physical item must have a corresponding loan item.</span></span> <span data-ttu-id="b2054-110">แต่ละเรกคอร์ดสินค้ากู้ยืมควรอธิบายถึงสิ่งที่ให้ยืม ใครที่รับผิดชอบสำหรับการกู้ยืม และจำนวนวันที่สินค้าสามารถให้กู้ยืมแก่ผู้ปฏิบัติงาน</span><span class="sxs-lookup"><span data-stu-id="b2054-110">Each loan item record should describe what is being loaned, who is responsible for the loan, and the number of days the item can loaned to a worker.</span></span> <span data-ttu-id="b2054-111">คุณสามารถสร้างรายการกู้ยืมหลายรายการ สำหรับรายการต่าง ๆ เช่น กุญแจ บัตรผ่าน หรือ เครื่องแบบ ในเวลาเดียวกัน</span><span class="sxs-lookup"><span data-stu-id="b2054-111">You can create multiple loan items, for items such as keys, access cards or uniforms, at the same time.</span></span> 

<span data-ttu-id="b2054-112">เมื่อให้กู้ยืมสินค้า ป้อนวันที่มีการกู้ยืมสินค้า และวันส่งคืนที่วางแผนไว้</span><span class="sxs-lookup"><span data-stu-id="b2054-112">When loaning an item, enter the date that the item was loaned, and the planned return date.</span></span> <span data-ttu-id="b2054-113">เมื่อมีการส่งคืนสินค้า ป้อนวันส่งคืนจริง</span><span class="sxs-lookup"><span data-stu-id="b2054-113">When the item is returned, enter the actual return date.</span></span>

<span data-ttu-id="b2054-114">พนักงานสามารถดูเรกคอร์ดของสินค้าที่กู้ยืมได้โดยใช้พื้นที่ทำงานการบริการตนเองของพนักงานได้</span><span class="sxs-lookup"><span data-stu-id="b2054-114">Employees can view the records of the items that have been loaned to them using the Employee self-service workspace.</span></span> <span data-ttu-id="b2054-115">พวกเขาสามารถแก้ไขเรกคอร์ดที่มีอยู่ หรือป้อนสินค้ากู้ยืมใหม่ถ้าพวกเขาได้รับสินค้าทางกายภาพที่เพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="b2054-115">They can also edit the existing records or enter new loan items, if they've received additional physical items.</span></span>  <span data-ttu-id="b2054-116">ลำดับงานสามารถถูกตั้งค่าเป็นการเปลี่ยนแปลงเส้นทางของสินค้าที่ให้กู้ยืมใหม่หรือที่มีอยู่ภายในกระบวนการอนุมัติ</span><span class="sxs-lookup"><span data-stu-id="b2054-116">Workflow can be set up to route changes to new or existing loan items through an approval process.</span></span> 

<span data-ttu-id="b2054-117">ผู้จัดการสามารถดูสินค้าที่ให้ยืมสำหรับรายงานโดยตรงของพวกเขา</span><span class="sxs-lookup"><span data-stu-id="b2054-117">Managers can view loaned items for their direct reports.</span></span> <span data-ttu-id="b2054-118">พวกเขาจะได้รับสิทธิ์ในการเพิ่มสินค้าที่ให้กู้ยืมใหม่ในนามของพนักงานของพวกเขา</span><span class="sxs-lookup"><span data-stu-id="b2054-118">They can also be granted permission to add new loan items on behalf of their employees.</span></span>

 <a name="account-for-lost-or-misplaced-loan-items"></a><span data-ttu-id="b2054-119"> บัญชีสำหรับสินค้าที่ให้กู้ยืมที่สูญหายหรือหาไม่พบ</span><span class="sxs-lookup"><span data-stu-id="b2054-119">Account for lost or misplaced loan items</span></span>
-----------------------------------------

<span data-ttu-id="b2054-120">ถ้าสินค้าชำรุดเสียหายหรือหาไม่พบ ป้อนเรกคอร์ดที่ส่งสมมติ</span><span class="sxs-lookup"><span data-stu-id="b2054-120">If an item becomes damaged or misplaced, enter a fictitious return record.</span></span> <span data-ttu-id="b2054-121">แล้วลบสินค้านั้นหรือเก็บสินค้านั้นไว้ในภาพรวมและเปลี่ยนคำอธิบายเพื่อบ่งชี้ว่าไม่มีสินค้านั้นแล้ว</span><span class="sxs-lookup"><span data-stu-id="b2054-121">Then either delete the item or keep it in the overview and change the description to indicate that the item is not available.</span></span>

 
<a name="see-also"></a><span data-ttu-id="b2054-122">ดูเพิ่มเติมที่</span><span class="sxs-lookup"><span data-stu-id="b2054-122">See also</span></span>
--------

[<span data-ttu-id="b2054-123">ทรัพยากรบุคคล</span><span class="sxs-lookup"><span data-stu-id="b2054-123">Human resources</span></span>](index.md)




