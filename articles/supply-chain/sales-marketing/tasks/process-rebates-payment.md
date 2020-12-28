---
title: กระบวนการเงินคืนสำหรับการชำระเงิน
description: 'ขั้นตอนนี้อธิบายวิธีการแปลงเงินคืนของลูกค้าที่ได้รับการอนุมัติและดำเนินการไปสู่ใบลดหนี้ '
author: omulvad
manager: tfehr
ms.date: 11/10/2016
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Operations
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 981068d26d232b10efd8d7288daaf7358aee3728
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 10/13/2020
ms.locfileid: "4438608"
---
# <a name="process-rebates-for-payment"></a><span data-ttu-id="0b1d2-103">กระบวนการเงินคืนสำหรับการชำระเงิน</span><span class="sxs-lookup"><span data-stu-id="0b1d2-103">Process rebates for payment</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="0b1d2-104">ขั้นตอนนี้อธิบายวิธีการแปลงเงินคืนของลูกค้าที่ได้รับการอนุมัติและดำเนินการไปสู่ใบลดหนี้ </span><span class="sxs-lookup"><span data-stu-id="0b1d2-104">This procedure demonstrates how to convert approved and processed customer rebates to credit notes.</span></span> <span data-ttu-id="0b1d2-105">คุณสามารถใช้คำแนะนำนี้ในบริษัทสาธิต USMF </span><span class="sxs-lookup"><span data-stu-id="0b1d2-105">You can use this guide in the USMF demo company.</span></span> <span data-ttu-id="0b1d2-106">เงื่อนไขเบื้องต้นสำหรับคำแนะนำนี้คือจะมีการอ้างสิทธิ์เงินคืนหนึ่งรายการหรือมากกว่าซึ่งมีสถานะการทำเครื่องหมาย </span><span class="sxs-lookup"><span data-stu-id="0b1d2-106">The precondition for this guide is to have one or more rebate claims which have a status of Mark.</span></span> <span data-ttu-id="0b1d2-107">ถ้าคุณใช้ USMF คุณควรรันคำแนะนำ " สร้างและประมวลผลเงินคืนของลูกค้า" ก่อนที่คุณจะเริ่มคำแนะนำนี้</span><span class="sxs-lookup"><span data-stu-id="0b1d2-107">If you're using USMF you should run the "Generate and process customer rebates" guide before you start this guide.</span></span>


## <a name="convert-rebate-claims-to-credit-note"></a><span data-ttu-id="0b1d2-108">แปลงการอ้างสิทธิ์เงินคืนไปเป็นใบลดหนี้</span><span class="sxs-lookup"><span data-stu-id="0b1d2-108">Convert rebate claims to credit note</span></span>
1. <span data-ttu-id="0b1d2-109">ไปที่ลูกค้าทั้งหมด</span><span class="sxs-lookup"><span data-stu-id="0b1d2-109">Go to All customers.</span></span>
2. <span data-ttu-id="0b1d2-110">ในรายการนี้ ให้ค้นหาและเลือกเรกคอร์ดที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="0b1d2-110">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="0b1d2-111">ในรายการนี้ ให้คลิกลิงค์ในแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="0b1d2-111">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="0b1d2-112">ในแผงการดำเนินการ คลิก รวบรวม</span><span class="sxs-lookup"><span data-stu-id="0b1d2-112">On the Action Pane, click Collect.</span></span>
5. <span data-ttu-id="0b1d2-113">คลิกธุรกรรมการชำระเงิน</span><span class="sxs-lookup"><span data-stu-id="0b1d2-113">Click Settle transactions.</span></span>
6. <span data-ttu-id="0b1d2-114">คลิกฟังก์ชัน</span><span class="sxs-lookup"><span data-stu-id="0b1d2-114">Click Functions.</span></span>
7. <span data-ttu-id="0b1d2-115">คลิกโปรแกรมเงินคืน</span><span class="sxs-lookup"><span data-stu-id="0b1d2-115">Click Rebate program.</span></span>
    * <span data-ttu-id="0b1d2-116">หน้ารายการเงินคืนการอ้างสิทธิ์เงินคืนที่คุณได้ดำเนินการแล้วในเวิร์กเบนซ์เงินคืนของลูกค้าและอยู่ในสถานะที่ทำเครื่องหมาย</span><span class="sxs-lookup"><span data-stu-id="0b1d2-116">The Rebate page lists the rebate claims that you have processed in the customer rebate workbench and that are in status Mark.</span></span>    
8. <span data-ttu-id="0b1d2-117">คลิก แก้ไข</span><span class="sxs-lookup"><span data-stu-id="0b1d2-117">Click Edit.</span></span>
    * <span data-ttu-id="0b1d2-118">ตั้งค่าตรวจสอบเครื่องหมายในฟิลด์ทำเครื่องหมายสำหรับการอ้างสิทธิ์ที่คุณต้องการรวมไว้ในใบลดหนี้</span><span class="sxs-lookup"><span data-stu-id="0b1d2-118">Set checkmarks in the Mark field for the claims that you want to include into credit note.</span></span>   
9. <span data-ttu-id="0b1d2-119">คลิกฟังก์ชัน</span><span class="sxs-lookup"><span data-stu-id="0b1d2-119">Click Functions.</span></span>
10. <span data-ttu-id="0b1d2-120">คลิกสร้างใบลดหนี้</span><span class="sxs-lookup"><span data-stu-id="0b1d2-120">Click Create credit note.</span></span>
    * <span data-ttu-id="0b1d2-121">ข้อความปรากฏขึ้นเพื่อแจ้งให้คุณทราบว่ามีการลงรายการสมุดรายวัน (นี่คือบัญชีลูกหนี้ปริมาณการใช้สมุดรายวันตามที่ระบุในพารามิเตอร์บัญชีลูกหนี้บัญชี) </span><span class="sxs-lookup"><span data-stu-id="0b1d2-121">A message appears to inform you that a journal has been posted (This is the Accounts receivable consumption journal, as specified in the Accounts receivable parameters page).</span></span> <span data-ttu-id="0b1d2-122">ซึ่งทำให้หนี้สินจริง (เครดิต) ยอดเงินที่จะย้ายไปเป็นยอดดุลลูกค้า</span><span class="sxs-lookup"><span data-stu-id="0b1d2-122">This causes the real liability (credit) amount to be moved to the customer balance.</span></span> <span data-ttu-id="0b1d2-123">นี่หมายความว่าบัญชีของลูกค้าถูกหักเงินและมีการหักเงินบัญชีเงินคืนคงค้าง</span><span class="sxs-lookup"><span data-stu-id="0b1d2-123">This means that the customer's account has been credited, and the Rebate accrual account has been debited.</span></span>  
11. <span data-ttu-id="0b1d2-124">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="0b1d2-124">Close the page.</span></span>
12. <span data-ttu-id="0b1d2-125">คลิก ยกเลิก</span><span class="sxs-lookup"><span data-stu-id="0b1d2-125">Click Cancel.</span></span>
    * <span data-ttu-id="0b1d2-126">รีเฟรชหน้านี่เพื่อให้คุณสามารถดูการปรับปรุง</span><span class="sxs-lookup"><span data-stu-id="0b1d2-126">This refreshes the page so that you can see the updates.</span></span>  
13. <span data-ttu-id="0b1d2-127">ในแผงการดำเนินการ คลิก รวบรวม</span><span class="sxs-lookup"><span data-stu-id="0b1d2-127">On the Action Pane, click Collect.</span></span>
14. <span data-ttu-id="0b1d2-128">คลิกธุรกรรมการชำระเงิน</span><span class="sxs-lookup"><span data-stu-id="0b1d2-128">Click Settle transactions.</span></span>
    * <span data-ttu-id="0b1d2-129">โปรดทราบว่ามีการทำธุรกรรมสำหรับจำนวนเงินค่าลบที่แสดงจำนวนเงินคืนรวมโดยไม่มีการใส่การอ้างอิงใบแจ้งหนี้ในยอดดุลลูกค้า</span><span class="sxs-lookup"><span data-stu-id="0b1d2-129">Note that a transaction for negative amount, representing the total rebate amount, without invoice reference has been added to the customer balance.</span></span>   
15. <span data-ttu-id="0b1d2-130">คลิก ยกเลิก</span><span class="sxs-lookup"><span data-stu-id="0b1d2-130">Click Cancel.</span></span>

