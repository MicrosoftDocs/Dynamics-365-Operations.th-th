--- 
title: "สร้างใบสั่งซื้อสำหรับซัพพลายเออร์ขาจร"
description: "กระบวนงานนี้แสดงวิธีการสร้างใบสั่งซื้อสำหรับซัพพลายเออร์ขาจร "
author: FrankDahl
manager: AnnBe
ms.date: 08/23/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: bis
ms.search.scope: Operations
ms.search.region: Global
ms.author: fdahl
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: e068105bcd5983220c43613569f80700922360e5
ms.contentlocale: th-th
ms.lasthandoff: 04/13/2018

---
# <a name="create-a-purchase-order-for-a-one-time-supplier"></a><span data-ttu-id="2fa37-103">สร้างใบสั่งซื้อสำหรับซัพพลายเออร์ขาจร</span><span class="sxs-lookup"><span data-stu-id="2fa37-103">Create a purchase order for a one-time supplier</span></span>

[!INCLUDE [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="2fa37-104">กระบวนงานนี้แสดงวิธีการสร้างใบสั่งซื้อสำหรับซัพพลายเออร์ขาจร </span><span class="sxs-lookup"><span data-stu-id="2fa37-104">This procedure shows you how to create a purchase order for a one-time supplier.</span></span> <span data-ttu-id="2fa37-105">ซัพพลายเออร์จะถูกสร้างขึ้นโดยอัตโนมัติพร้อมกับใบสั่งซื้อ แทนที่จะต้องสร้างบัญชีผู้จัดจำหน่ายด้วยตนเอง</span><span class="sxs-lookup"><span data-stu-id="2fa37-105">The supplier is created automatically with the purchase order, rather than having to create the vendor account manually.</span></span> <span data-ttu-id="2fa37-106">โดยทั่วไป ใบสั่งซื้อจะถูกสร้างโดยเจ้าหน้าที่จัดซื้อ</span><span class="sxs-lookup"><span data-stu-id="2fa37-106">Purchase orders are typically created by a purchasing agent.</span></span> <span data-ttu-id="2fa37-107">ตัวอย่างที่แสดงในคำแนะนำนี้สามารถใช้ในบริษัทข้อมูลสาธิต USMF</span><span class="sxs-lookup"><span data-stu-id="2fa37-107">The example shown in this guide can be used in the USMF demo data company.</span></span> <span data-ttu-id="2fa37-108">ข้อกำหนดเบื้องต้นคือให้มีการตั้งค่าบัญชีผู้จัดจำหน่ายขาจรในหน้าพารามิเตอร์บัญชีเจ้าหนี้</span><span class="sxs-lookup"><span data-stu-id="2fa37-108">It is a prerequisite that a one-time vendor account has been set up in the Account payable parameters page.</span></span>


## <a name="create-a-purchase-order-for-a-one-time-supplier"></a><span data-ttu-id="2fa37-109">สร้างใบสั่งซื้อสำหรับซัพพลายเออร์ขาจร</span><span class="sxs-lookup"><span data-stu-id="2fa37-109">Create a purchase order for a one-time supplier</span></span>
1. <span data-ttu-id="2fa37-110">ไปที่การจัดซื้อและการจัดหา > ใบสั่งซื้อ > ใบสั่งซื้อทั้งหมด</span><span class="sxs-lookup"><span data-stu-id="2fa37-110">Go to Procurement and sourcing > Purchase orders > All purchase orders.</span></span>
2. <span data-ttu-id="2fa37-111">คลิก สร้าง</span><span class="sxs-lookup"><span data-stu-id="2fa37-111">Click New.</span></span>
3. <span data-ttu-id="2fa37-112">เลือกใช่ในฟิลด์ซัพพลายเออร์ขาจร</span><span class="sxs-lookup"><span data-stu-id="2fa37-112">Select Yes in the One-time supplier field.</span></span>
    * <span data-ttu-id="2fa37-113">บัญชีผู้จัดจำหน่ายถูกสร้างขึ้นโดยอัตโนมัติ และกำหนดให้กับใบสั่งซื้อ </span><span class="sxs-lookup"><span data-stu-id="2fa37-113">A vendor account is automatically created and assigned to the purchase order.</span></span> <span data-ttu-id="2fa37-114">บัญชีผู้จัดจำหน่ายจะสร้างขึ้นตามเท็มเพลที่ระบุบนแท็บทั่วไปในหน้าพารามิเตอร์บัญชีเจ้าหนี้</span><span class="sxs-lookup"><span data-stu-id="2fa37-114">The vendor account is created based on the template that is specified on the General tab in the Accounts payable parameters page.</span></span>  
4. <span data-ttu-id="2fa37-115">ในฟิลด์ชื่อ ให้พิมพ์ชื่อสำหรับซัพพลายเออร์</span><span class="sxs-lookup"><span data-stu-id="2fa37-115">In the Name field, type a name for the supplier.</span></span>
5. <span data-ttu-id="2fa37-116">คลิก ตกลง</span><span class="sxs-lookup"><span data-stu-id="2fa37-116">Click OK.</span></span>
    * <span data-ttu-id="2fa37-117">ขณะนี้สามารถทำใบสั่งซื้อให้เสร็จสมบูรณ์และดำเนินการเช่นเดียวกับใบสั่งอื่น ๆ </span><span class="sxs-lookup"><span data-stu-id="2fa37-117">The purchase order can now be completed and processed like any other order.</span></span> <span data-ttu-id="2fa37-118">ในการดำเนินการนี้ไม่มีลักษณะพิเศษใดๆ ที่เกี่ยวข้อง</span><span class="sxs-lookup"><span data-stu-id="2fa37-118">There are no special characteristics related to how this is done.</span></span> <span data-ttu-id="2fa37-119">ใบแจ้งหนี้จะแสดงธุรกรรมที่ครบกำหนดในบัญชีผู้จัดจำหน่ายที่มีการสร้างพร้อมกับใบสั่ง และจึงจะมีการประมวลผลการชำระเงิน</span><span class="sxs-lookup"><span data-stu-id="2fa37-119">The invoice will account a due transaction on the vendor account that was created with the order, and payment will then be processed.</span></span> <span data-ttu-id="2fa37-120">เมื่อดำเนินการเสร็จสมบูรณ์ สามารถลบบัญชีผู้จัดจำหน่ายได้</span><span class="sxs-lookup"><span data-stu-id="2fa37-120">When this is completed, the vendor account can be deleted.</span></span> <span data-ttu-id="2fa37-121">ซึ่งโดยทั่วไปจะดำเนินการโดยแผนกบัญชีเจ้าหนี้</span><span class="sxs-lookup"><span data-stu-id="2fa37-121">This is typically done by the accounts payable department.</span></span>  


