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
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: b1d32d94daef570e37a1a36d948fe18cd4041e46
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 01/15/2021
ms.locfileid: "4966166"
---
# <a name="process-rebates-for-payment"></a><span data-ttu-id="2a608-103">กระบวนการเงินคืนสำหรับการชำระเงิน</span><span class="sxs-lookup"><span data-stu-id="2a608-103">Process rebates for payment</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="2a608-104">ขั้นตอนนี้อธิบายวิธีการแปลงเงินคืนของลูกค้าที่ได้รับการอนุมัติและดำเนินการไปสู่ใบลดหนี้ </span><span class="sxs-lookup"><span data-stu-id="2a608-104">This procedure demonstrates how to convert approved and processed customer rebates to credit notes.</span></span> <span data-ttu-id="2a608-105">คุณสามารถใช้คำแนะนำนี้ในบริษัทสาธิต USMF </span><span class="sxs-lookup"><span data-stu-id="2a608-105">You can use this guide in the USMF demo company.</span></span> <span data-ttu-id="2a608-106">เงื่อนไขเบื้องต้นสำหรับคำแนะนำนี้คือจะมีการอ้างสิทธิ์เงินคืนหนึ่งรายการหรือมากกว่าซึ่งมีสถานะการทำเครื่องหมาย </span><span class="sxs-lookup"><span data-stu-id="2a608-106">The precondition for this guide is to have one or more rebate claims which have a status of Mark.</span></span> <span data-ttu-id="2a608-107">ถ้าคุณใช้ USMF คุณควรรันคำแนะนำ " สร้างและประมวลผลเงินคืนของลูกค้า" ก่อนที่คุณจะเริ่มคำแนะนำนี้</span><span class="sxs-lookup"><span data-stu-id="2a608-107">If you're using USMF you should run the "Generate and process customer rebates" guide before you start this guide.</span></span>


## <a name="convert-rebate-claims-to-credit-note"></a><span data-ttu-id="2a608-108">แปลงการอ้างสิทธิ์เงินคืนไปเป็นใบลดหนี้</span><span class="sxs-lookup"><span data-stu-id="2a608-108">Convert rebate claims to credit note</span></span>
1. <span data-ttu-id="2a608-109">ไปที่ลูกค้าทั้งหมด</span><span class="sxs-lookup"><span data-stu-id="2a608-109">Go to All customers.</span></span>
2. <span data-ttu-id="2a608-110">ในรายการนี้ ให้ค้นหาและเลือกเรกคอร์ดที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="2a608-110">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="2a608-111">ในรายการนี้ ให้คลิกลิงค์ในแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="2a608-111">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="2a608-112">ในแผงการดำเนินการ คลิก รวบรวม</span><span class="sxs-lookup"><span data-stu-id="2a608-112">On the Action Pane, click Collect.</span></span>
5. <span data-ttu-id="2a608-113">คลิกธุรกรรมการชำระเงิน</span><span class="sxs-lookup"><span data-stu-id="2a608-113">Click Settle transactions.</span></span>
6. <span data-ttu-id="2a608-114">คลิกฟังก์ชัน</span><span class="sxs-lookup"><span data-stu-id="2a608-114">Click Functions.</span></span>
7. <span data-ttu-id="2a608-115">คลิกโปรแกรมเงินคืน</span><span class="sxs-lookup"><span data-stu-id="2a608-115">Click Rebate program.</span></span>
    * <span data-ttu-id="2a608-116">หน้ารายการเงินคืนการอ้างสิทธิ์เงินคืนที่คุณได้ดำเนินการแล้วในเวิร์กเบนซ์เงินคืนของลูกค้าและอยู่ในสถานะที่ทำเครื่องหมาย</span><span class="sxs-lookup"><span data-stu-id="2a608-116">The Rebate page lists the rebate claims that you have processed in the customer rebate workbench and that are in status Mark.</span></span>    
8. <span data-ttu-id="2a608-117">คลิก แก้ไข</span><span class="sxs-lookup"><span data-stu-id="2a608-117">Click Edit.</span></span>
    * <span data-ttu-id="2a608-118">ตั้งค่าตรวจสอบเครื่องหมายในฟิลด์ทำเครื่องหมายสำหรับการอ้างสิทธิ์ที่คุณต้องการรวมไว้ในใบลดหนี้</span><span class="sxs-lookup"><span data-stu-id="2a608-118">Set checkmarks in the Mark field for the claims that you want to include into credit note.</span></span>   
9. <span data-ttu-id="2a608-119">คลิกฟังก์ชัน</span><span class="sxs-lookup"><span data-stu-id="2a608-119">Click Functions.</span></span>
10. <span data-ttu-id="2a608-120">คลิกสร้างใบลดหนี้</span><span class="sxs-lookup"><span data-stu-id="2a608-120">Click Create credit note.</span></span>
    * <span data-ttu-id="2a608-121">ข้อความปรากฏขึ้นเพื่อแจ้งให้คุณทราบว่ามีการลงรายการสมุดรายวัน (นี่คือบัญชีลูกหนี้ปริมาณการใช้สมุดรายวันตามที่ระบุในพารามิเตอร์บัญชีลูกหนี้บัญชี) </span><span class="sxs-lookup"><span data-stu-id="2a608-121">A message appears to inform you that a journal has been posted (This is the Accounts receivable consumption journal, as specified in the Accounts receivable parameters page).</span></span> <span data-ttu-id="2a608-122">ซึ่งทำให้หนี้สินจริง (เครดิต) ยอดเงินที่จะย้ายไปเป็นยอดดุลลูกค้า</span><span class="sxs-lookup"><span data-stu-id="2a608-122">This causes the real liability (credit) amount to be moved to the customer balance.</span></span> <span data-ttu-id="2a608-123">นี่หมายความว่าบัญชีของลูกค้าถูกหักเงินและมีการหักเงินบัญชีเงินคืนคงค้าง</span><span class="sxs-lookup"><span data-stu-id="2a608-123">This means that the customer's account has been credited, and the Rebate accrual account has been debited.</span></span>  
11. <span data-ttu-id="2a608-124">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="2a608-124">Close the page.</span></span>
12. <span data-ttu-id="2a608-125">คลิก ยกเลิก</span><span class="sxs-lookup"><span data-stu-id="2a608-125">Click Cancel.</span></span>
    * <span data-ttu-id="2a608-126">รีเฟรชหน้านี่เพื่อให้คุณสามารถดูการปรับปรุง</span><span class="sxs-lookup"><span data-stu-id="2a608-126">This refreshes the page so that you can see the updates.</span></span>  
13. <span data-ttu-id="2a608-127">ในแผงการดำเนินการ คลิก รวบรวม</span><span class="sxs-lookup"><span data-stu-id="2a608-127">On the Action Pane, click Collect.</span></span>
14. <span data-ttu-id="2a608-128">คลิกธุรกรรมการชำระเงิน</span><span class="sxs-lookup"><span data-stu-id="2a608-128">Click Settle transactions.</span></span>
    * <span data-ttu-id="2a608-129">โปรดทราบว่ามีการทำธุรกรรมสำหรับจำนวนเงินค่าลบที่แสดงจำนวนเงินคืนรวมโดยไม่มีการใส่การอ้างอิงใบแจ้งหนี้ในยอดดุลลูกค้า</span><span class="sxs-lookup"><span data-stu-id="2a608-129">Note that a transaction for negative amount, representing the total rebate amount, without invoice reference has been added to the customer balance.</span></span>   
15. <span data-ttu-id="2a608-130">คลิก ยกเลิก</span><span class="sxs-lookup"><span data-stu-id="2a608-130">Click Cancel.</span></span>

