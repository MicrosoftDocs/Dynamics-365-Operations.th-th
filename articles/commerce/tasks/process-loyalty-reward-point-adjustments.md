---
title: " ดำเนินการปรับปรุงคะแนนรางวัลสำหรับสมาชิก"
description: 'ขั้นตอนนี้แสดงวิธีการค้นหาข้อมูลบัตรสมาชิกและปรับปรุงคะแนนรางวัลสำหรับสมาชิก '
author: scott-tucker
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: RetailLoyaltyCards, RetailLoyaltyCardRewardPointTrans, RetailLoyaltyCardRewardPointAdjustment, RetailAffiliationLookup
audience: Application User
ms.reviewer: josaw
ms.search.region: Global
ms.search.industry: Retail
ms.author: scotttuc
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 7eae943985cc2bd706c0c3c4ec7b0470e3a54bff
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 03/31/2021
ms.locfileid: "5802634"
---
# <a name="process-loyalty-reward-point-adjustments"></a><span data-ttu-id="8154f-103"> ดำเนินการปรับปรุงคะแนนรางวัลสำหรับสมาชิก</span><span class="sxs-lookup"><span data-stu-id="8154f-103">Process loyalty reward point adjustments</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="8154f-104">ขั้นตอนนี้แสดงวิธีการค้นหาข้อมูลบัตรสมาชิกและปรับปรุงคะแนนรางวัลสำหรับสมาชิก </span><span class="sxs-lookup"><span data-stu-id="8154f-104">This procedure demonstrates how to look up loyalty card information and adjust loyalty reward points.</span></span> <span data-ttu-id="8154f-105">ข้อมูลบริษัทสาธิตที่ใช้ในการสร้างงานนี้คือ USRT </span><span class="sxs-lookup"><span data-stu-id="8154f-105">The demo data company used to create this task is USRT.</span></span> <span data-ttu-id="8154f-106">งานนี้เจาะจงสำหรับบทบาทผู้จัดการฝ่ายปฏิบัติการในเชิงพาณิชย์ หรือบทบาทผู้จัดการฝ่ายบริการลูกค้า</span><span class="sxs-lookup"><span data-stu-id="8154f-106">This task is intended for the Commerce operations manager role or a Customer service manager role.</span></span>

1. <span data-ttu-id="8154f-107">ไปยังบัตรสมาชิก</span><span class="sxs-lookup"><span data-stu-id="8154f-107">Go to Loyalty cards.</span></span>
2. <span data-ttu-id="8154f-108">ในรายการนี้ ให้ค้นหาและเลือกเรกคอร์ดที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="8154f-108">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="8154f-109">ในรายการนี้ ให้คลิกลิงค์ในแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="8154f-109">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="8154f-110">คลิกธุรกรรมบัตร</span><span class="sxs-lookup"><span data-stu-id="8154f-110">Click Card transactions.</span></span>
    * <span data-ttu-id="8154f-111">บนหน้านี้ คุณสามารถดูธุรกรรมทั้งหมดของสมาชิกสำหรับบัตรสมาชิกที่เลือก</span><span class="sxs-lookup"><span data-stu-id="8154f-111">On this page you can view all loyalty transactions for the selected loyalty card.</span></span>  
5. <span data-ttu-id="8154f-112">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="8154f-112">Close the page.</span></span>
6. <span data-ttu-id="8154f-113">คลิกการปรับปรุงบัตร</span><span class="sxs-lookup"><span data-stu-id="8154f-113">Click Card adjustments.</span></span>
7. <span data-ttu-id="8154f-114">คลิก สร้าง</span><span class="sxs-lookup"><span data-stu-id="8154f-114">Click New.</span></span>
8. <span data-ttu-id="8154f-115">ในฟิลด์คะแนนรางวัล ให้ป้อนหรือเลือกค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="8154f-115">In the Reward point field, enter or select a value.</span></span>
9. <span data-ttu-id="8154f-116">ในฟิลด์จำนวนและปริมาณ ให้ป้อนค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="8154f-116">In the Amount or quantity field, enter a number.</span></span>
    * <span data-ttu-id="8154f-117">คุณสามารถเพิ่มหรือลบคะแนนจากบัตรสมาชิก โดยการใช้ยอดเงินค่าบวกหรือค่าลบ</span><span class="sxs-lookup"><span data-stu-id="8154f-117">You can add or remove points from the loyalty card by using positive or negative amounts.</span></span>  
10. <span data-ttu-id="8154f-118">ในฟิลด์โปรแกรมสมาชิก ให้ป้อนหรือเลือกค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="8154f-118">In the Loyalty program field, enter or select a value.</span></span>
11. <span data-ttu-id="8154f-119">ในฟิลด์ข้อคิดเห็น ให้พิมพ์ค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="8154f-119">In the Comment field, type a value.</span></span>
12. <span data-ttu-id="8154f-120">คลิกลงรายการบัญชีการปรับปรุง</span><span class="sxs-lookup"><span data-stu-id="8154f-120">Click Post adjustment.</span></span>
13. <span data-ttu-id="8154f-121">คลิก ใช่</span><span class="sxs-lookup"><span data-stu-id="8154f-121">Click Yes.</span></span>
14. <span data-ttu-id="8154f-122">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="8154f-122">Close the page.</span></span>
    * <span data-ttu-id="8154f-123">โดยปกติแล้ว ณ จุดนี้ คุณต้องกดรีเฟรชหน้าเพื่อดูผลลัพธ์ของการปรับปรุงคะแนนรางวัลในแท็บสรุปคะแนนรางวัล แต่ถ้าคุณกำลังรันงานนี้ให้เป็นคู่มืองาน อย่ากดรีเฟรชตอนนี้ เพราะถ้าคุณกด คู่มืองานจะหยุดทำงาน</span><span class="sxs-lookup"><span data-stu-id="8154f-123">Normally at this point you'd refresh the page to see the result of the reward points adjustment in the Reward point summary tab. But if you are running this as a task guide, don't refresh now because if you do, the task guide will stop.</span></span>  
15. <span data-ttu-id="8154f-124">คลิกธุรกรรมบัตร</span><span class="sxs-lookup"><span data-stu-id="8154f-124">Click Card transactions.</span></span>
16. <span data-ttu-id="8154f-125">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="8154f-125">Close the page.</span></span>



[!INCLUDE[footer-include](../../includes/footer-banner.md)]