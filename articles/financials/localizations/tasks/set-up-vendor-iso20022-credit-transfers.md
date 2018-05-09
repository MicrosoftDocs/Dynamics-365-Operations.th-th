--- 
title: "ตั้งค่าผู้จัดจำหน่ายและบัญชีธนาคารของผู้จัดจำหน่ายสำหรับการโอนย้ายเครดิต ISO20022"
description: "กระบวนงานนี้แสดงวิธีการตั้งค่าข้อมูลของผู้จัดจำหน่ายและข้อมูลของบัญชีธนาคารของผู้จัดจำหน่ายเฉพาะที่จำเป็นสำหรับการโอนย้ายเครดิต ISO20022 หรือการสร้างไฟล์การชำระเงินของผู้จัดจำหน่ายอื่นใดๆ "
author: mrolecki
manager: AnnBe
ms.date: 10/24/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Operations
ms.search.region: Global
ms.author: mrolecki
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: 7b489587097f2f10663a7cfb745ce1d17985b432
ms.contentlocale: th-th
ms.lasthandoff: 05/08/2018

---
# <a name="set-up-vendors-and-vendor-bank-accounts-for-iso20022-credit-transfers"></a><span data-ttu-id="032e7-103">ตั้งค่าผู้จัดจำหน่ายและบัญชีธนาคารของผู้จัดจำหน่ายสำหรับการโอนย้ายเครดิต ISO20022</span><span class="sxs-lookup"><span data-stu-id="032e7-103">Set up vendors and vendor bank accounts for ISO20022 credit transfers</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="032e7-104">กระบวนงานนี้แสดงวิธีการตั้งค่าข้อมูลของผู้จัดจำหน่ายและข้อมูลของบัญชีธนาคารของผู้จัดจำหน่ายเฉพาะที่จำเป็นสำหรับการโอนย้ายเครดิต ISO20022 หรือการสร้างไฟล์การชำระเงินของผู้จัดจำหน่ายอื่นใดๆ </span><span class="sxs-lookup"><span data-stu-id="032e7-104">This procedure demonstrates how to set up the vendor and vendor specific bank account information required for ISO20022 Credit transfer or any other vendor payment file generation.</span></span> 

<span data-ttu-id="032e7-105">บริษัทข้อมูลสาธิตที่ใช้สร้างกระบวนการนี้คือ DEMF</span><span class="sxs-lookup"><span data-stu-id="032e7-105">The demo data company used to create this procedure is DEMF.</span></span>
<span data-ttu-id="032e7-106">นี่คือกระบวนงานที่สี่จากกระบวนงานห้ารายการที่อธิบายกระบวนการชำระเงินของผู้จัดจำหน่ายโดยใช้การตั้งค่าคอนฟิกการรายงานทางอิเล็กทรอนิกส์ </span><span class="sxs-lookup"><span data-stu-id="032e7-106">This is the fourth procedure, out of five, that illustrates the vendor payment process using electronic reporting configurations.</span></span> <span data-ttu-id="032e7-107">กระบวนงานนี้ใช้สำหรับลักษณะการทำงานที่ถูกเพิ่มลงใน Dynamics 365 for Operations รุ่น 1611</span><span class="sxs-lookup"><span data-stu-id="032e7-107">This procedure is for a feature that was added in Dynamics 365 for Operations version 1611.</span></span>


## <a name="set-up-bank-details"></a><span data-ttu-id="032e7-108">ตั้งค่าข้อมูลธนาคาร</span><span class="sxs-lookup"><span data-stu-id="032e7-108">Set up bank details</span></span>
1. <span data-ttu-id="032e7-109">ไปที่บัญชีเจ้าหนี้ > ผู้จัดจำหน่าย > ผู้จัดจำหน่ายทั้งหมด</span><span class="sxs-lookup"><span data-stu-id="032e7-109">Go to Accounts payable > Vendors > All vendors.</span></span>
2. <span data-ttu-id="032e7-110">ใช้ตัวกรองข้อมูลด่วนเพื่อค้นหาเรกคอร์ด </span><span class="sxs-lookup"><span data-stu-id="032e7-110">Use the Quick Filter to find records.</span></span> <span data-ttu-id="032e7-111">เช่น กรองข้อมูลในฟิลด์บัญชีผู้จัดจำหน่าย ด้วยค่า 'DE-001'</span><span class="sxs-lookup"><span data-stu-id="032e7-111">For example, filter on the Vendor account field with a value of 'DE-001'.</span></span>
3. <span data-ttu-id="032e7-112">คลิก DE-001 เพื่อเปิดรายละเอียดผู้จัดจำหน่าย</span><span class="sxs-lookup"><span data-stu-id="032e7-112">Click DE-001 to open vendor details.</span></span>
4. <span data-ttu-id="032e7-113">ในบานหน้าต่างการดำเนินการ คลิกผู้จัดจำหน่าย</span><span class="sxs-lookup"><span data-stu-id="032e7-113">On the Action Pane, click Vendor.</span></span>
5. <span data-ttu-id="032e7-114">คลิก บัญชีธนาคาร</span><span class="sxs-lookup"><span data-stu-id="032e7-114">Click Bank accounts.</span></span>
6. <span data-ttu-id="032e7-115">คลิก แก้ไข</span><span class="sxs-lookup"><span data-stu-id="032e7-115">Click Edit.</span></span>
    * <span data-ttu-id="032e7-116">ถ้าไม่มีบัญชีธนาคารที่ใช้งานได้ คุณต้องสร้างบัญชีใหม่</span><span class="sxs-lookup"><span data-stu-id="032e7-116">If there is no bank account available, you need to create a new one.</span></span>  
7. <span data-ttu-id="032e7-117">ในฟิลด์รหัส SWIFT ให้พิมพ์ 'COBADEFFXXX'</span><span class="sxs-lookup"><span data-stu-id="032e7-117">In the SWIFT code field, type 'COBADEFFXXX'.</span></span>
8. <span data-ttu-id="032e7-118">ในฟิลด์ IBAN ให้พิมพ์ 'DE36200400000628808808'</span><span class="sxs-lookup"><span data-stu-id="032e7-118">In the IBAN field, type 'DE36200400000628808808'.</span></span>
9. <span data-ttu-id="032e7-119">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="032e7-119">Close the page.</span></span>

## <a name="set-up-a-method-of-payment-for-the-vendor"></a><span data-ttu-id="032e7-120">ตั้งค่าวิธีการชำระเงินสำหรับผู้จัดจำหน่าย</span><span class="sxs-lookup"><span data-stu-id="032e7-120">Set up a method of payment for the vendor</span></span>
1. <span data-ttu-id="032e7-121">คลิก แก้ไข</span><span class="sxs-lookup"><span data-stu-id="032e7-121">Click Edit.</span></span>
2. <span data-ttu-id="032e7-122">ขยายหรือยุบส่วนการชำระเงิน</span><span class="sxs-lookup"><span data-stu-id="032e7-122">Expand or collapse the Payment section.</span></span>
3. <span data-ttu-id="032e7-123">ในฟิลด์วิธีการชำระเงิน ให้คลิกปุ่มดรอปดาวน์เพื่อเปิดการค้นหา</span><span class="sxs-lookup"><span data-stu-id="032e7-123">In the Method of payment field, click the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="032e7-124">ในรายการนี้ ให้คลิกลิงค์ในแถว SEPA CT</span><span class="sxs-lookup"><span data-stu-id="032e7-124">In the list, click the link in the SEPA CT row.</span></span>
5. <span data-ttu-id="032e7-125">คลิก บันทึก</span><span class="sxs-lookup"><span data-stu-id="032e7-125">Click Save.</span></span>


