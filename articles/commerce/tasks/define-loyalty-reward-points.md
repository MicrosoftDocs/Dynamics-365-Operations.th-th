---
title: " กำหนดคะแนนรางวัลสำหรับสมาชิก"
description: 'กระบวนการนี้จะแนะนำวิธีกำหนดคะแนนรางวัลสำหรับสมาชิก '
author: scott-tucker
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: RetailLoyaltyRewardPoints
audience: Application User
ms.reviewer: josaw
ms.search.region: Global
ms.search.industry: Retail
ms.author: scotttuc
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: af217a5e756db571e3e351b743aa44b842f478f1
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 01/15/2021
ms.locfileid: "5000495"
---
# <a name="define-loyalty-reward-points"></a><span data-ttu-id="6d4e1-103"> กำหนดคะแนนรางวัลสำหรับสมาชิก</span><span class="sxs-lookup"><span data-stu-id="6d4e1-103">Define loyalty reward points</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="6d4e1-104">กระบวนการนี้จะแนะนำวิธีกำหนดคะแนนรางวัลสำหรับสมาชิก </span><span class="sxs-lookup"><span data-stu-id="6d4e1-104">This procedure walks through defining loyalty reward points.</span></span> <span data-ttu-id="6d4e1-105">คุณควรตั้งค่าคะแนนรางวัลสำหรับสมาชิกก่อนที่คุณจะตั้งค่าโปรแกรมตอบแทนลูกค้าสมาชิก </span><span class="sxs-lookup"><span data-stu-id="6d4e1-105">You should set up loyalty reward points before you set up a loyalty program.</span></span> <span data-ttu-id="6d4e1-106">ขั้นตอนนี้ใช้บริษัทข้อมูลสาธิต USRT</span><span class="sxs-lookup"><span data-stu-id="6d4e1-106">This procedure uses the USRT demo data company.</span></span>

1. <span data-ttu-id="6d4e1-107">ไปยัง การขายปลีกและการค้า > ลูกค้า > ความภักดี > คะแนนสะสมที่เป็นรางวัลจากความภักดี </span><span class="sxs-lookup"><span data-stu-id="6d4e1-107">Go to Retail and Commerce > Customers > Loyalty > Loyalty reward points.</span></span>
2. <span data-ttu-id="6d4e1-108">คลิก สร้าง</span><span class="sxs-lookup"><span data-stu-id="6d4e1-108">Click New.</span></span>
3. <span data-ttu-id="6d4e1-109">ในฟิลด์รหัสคะแนนรางวัล ให้พิมพ์ค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="6d4e1-109">In the Reward point ID field, type a value.</span></span>
4. <span data-ttu-id="6d4e1-110">ในฟิลด์ คำอธิบาย ให้พิมพ์ค่า</span><span class="sxs-lookup"><span data-stu-id="6d4e1-110">In the Description field, type a value.</span></span>
5. <span data-ttu-id="6d4e1-111">ในฟิลด์ประเภทคะแนนรางวัล ให้เลือกตัวเลือกหนึ่งตัวเลือก</span><span class="sxs-lookup"><span data-stu-id="6d4e1-111">In the Reward point type field, select an option.</span></span>
    * <span data-ttu-id="6d4e1-112">เลือกปริมาณถ้าคุณต้องการจะให้คะแนนรางวัลถูกปัดเศษเป็นเลขจำนวนเต็มที่ใกล้ที่สุด </span><span class="sxs-lookup"><span data-stu-id="6d4e1-112">Select Quantity if you want the reward points to be rounded to the nearest integer.</span></span> <span data-ttu-id="6d4e1-113">เลือกยอดเงินถ้าคุณต้องการให้คะแนนรางวัลถูกปัดเศษตามกฎการปัดเศษสกุลเงิน</span><span class="sxs-lookup"><span data-stu-id="6d4e1-113">Select Amount if you want the reward points to be rounded according to currency rounding rules.</span></span> <span data-ttu-id="6d4e1-114">ถ้าคุณเลือกปริมาณ ให้ข้ามขั้นตอนถัดไปของกระบวนการนี้...</span><span class="sxs-lookup"><span data-stu-id="6d4e1-114">If you select Quantity, skip the next step of this procedure..</span></span>  
6. <span data-ttu-id="6d4e1-115">ในฟิลด์สกุลเงิน ให้พิมพ์ค่า</span><span class="sxs-lookup"><span data-stu-id="6d4e1-115">In the Currency field, type a value.</span></span>
    * <span data-ttu-id="6d4e1-116">สำหรับคะแนนรางวัลประเภทยอดเงิน คะแนนทั้งหมดจะมีสกุลเงินที่เลือก </span><span class="sxs-lookup"><span data-stu-id="6d4e1-116">For Amount type reward points, all points issued will have the selected currency.</span></span> <span data-ttu-id="6d4e1-117">สำหรับคะแนนรางวัลประเภทปริมาณ ฟิลด์นี้ไม่สามารถใช้ได้ — ข้ามขั้นตอนนี้</span><span class="sxs-lookup"><span data-stu-id="6d4e1-117">For Quantity type reward points, this field doesn't apply—skip this step.</span></span>  
7. <span data-ttu-id="6d4e1-118">เลือกหรือยกเลิกการเลือกกล่องกาเครื่องหมายแลกได้</span><span class="sxs-lookup"><span data-stu-id="6d4e1-118">Check or uncheck the Redeemable checkbox.</span></span>
8. <span data-ttu-id="6d4e1-119">ในฟิลด์การจัดอันดับการแลก ให้ป้อนตัวเลข</span><span class="sxs-lookup"><span data-stu-id="6d4e1-119">In the Redeem ranking field, enter a number.</span></span>
    * <span data-ttu-id="6d4e1-120">การจัดอันดับการแลกจะถูกใช้เมื่อคะแนนรางวัลที่สามารถแลกได้อย่างน้อยสองอันดับสามารถใช้ชำระผลิตภัณฑ์ได้ </span><span class="sxs-lookup"><span data-stu-id="6d4e1-120">Redeem ranking is used when two or more redeemable reward points can be used to pay for products.</span></span> <span data-ttu-id="6d4e1-121">ถ้ามีคะแนนรางวัลสองอันดับมีการจัดอันดับการแลกเหมือนกัน อันที่ต้องการเลขคะแนนต่ำกว่าจะถูกใช้</span><span class="sxs-lookup"><span data-stu-id="6d4e1-121">If the two reward points have the same redeem ranking, then the one that needs to lower number of points will be used.</span></span>  
9. <span data-ttu-id="6d4e1-122">ในฟิลด์ค่าเวลาหมดอายุ ให้ป้อนตัวเลข</span><span class="sxs-lookup"><span data-stu-id="6d4e1-122">In the Expiration time value field, enter a number.</span></span>
    * <span data-ttu-id="6d4e1-123">คะแนนรางวัลจะหมดอายุในจำนวนวัน เดือน หรือปีที่ระบุหลังจากออก</span><span class="sxs-lookup"><span data-stu-id="6d4e1-123">The reward points will expire the specified number of days, months, or years after when the points are issued.</span></span> <span data-ttu-id="6d4e1-124">ค่า '0' หมายถึง คะแนนรางวัลสำหรับสมาชิกจะไม่มีวันหมดอายุ</span><span class="sxs-lookup"><span data-stu-id="6d4e1-124">A value of '0' means the loyalty reward points will never expire.</span></span>  
10. <span data-ttu-id="6d4e1-125">ในฟิลด์หน่วยเวลาหมดอายุ ให้เลือกหนึ่งตัวเลือก</span><span class="sxs-lookup"><span data-stu-id="6d4e1-125">In the Expiration time unit field, select an option.</span></span>
11. <span data-ttu-id="6d4e1-126">คลิก บันทึก</span><span class="sxs-lookup"><span data-stu-id="6d4e1-126">Click Save.</span></span>

