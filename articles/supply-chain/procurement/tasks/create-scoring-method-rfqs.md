---
title: สร้างวิธีการให้คะแนนสำหรับ RFQ
description: 'กระบวนงานนี้แสดงวิธีการสร้างวิธีการให้คะแนน '
author: RichardLuan
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: PurchRFQScoringMethod
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: riluan
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: ba3f0b2be16c02129616025c0ee6258996189c6a
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 02/15/2021
ms.locfileid: "5211825"
---
# <a name="create-a-scoring-method-for-rfqs"></a><span data-ttu-id="502c1-103">สร้างวิธีการให้คะแนนสำหรับ RFQ</span><span class="sxs-lookup"><span data-stu-id="502c1-103">Create a scoring method for RFQs</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="502c1-104">กระบวนงานนี้แสดงวิธีการสร้างวิธีการให้คะแนน </span><span class="sxs-lookup"><span data-stu-id="502c1-104">This procedure shows you how to create a scoring method.</span></span> <span data-ttu-id="502c1-105">วิธีการให้คะแนนคือชุดของเงื่อนไขที่สามารถใช้เพื่อเปรียบเทียบการประมูลที่ส่งในการตอบคำขอใบเสนอราคา (RFQ) </span><span class="sxs-lookup"><span data-stu-id="502c1-105">A scoring method is a set of criteria that can be used to compare bids that are sent in reply to a request for quotation (RFQ).</span></span> <span data-ttu-id="502c1-106">ตัวอย่างเช่น คุณอาจต้องการจัดอันดับผู้จัดจำหน่ายตามผลการปฏิบัติงานในอดีต หรือจัดอันดับว่าบริษัทเป็นมิตรต่อสิ่งแวดล้อม หรือเป็นผู้ให้ความร่วมมือที่ดีหรือไม่ หรือคุณอาจต้องการเปรียบเทียบการประมูลตามราคา</span><span class="sxs-lookup"><span data-stu-id="502c1-106">For example, you might want to rate a vendor on past performance, or rate whether the company is environmentally friendly or a good collaborator, or you might want to compare bids based on price.</span></span> <span data-ttu-id="502c1-107">วิธีการให้คะแนนสามารถเชื่อมโยงกับชนิดการร้องขอเป็นวิธีการให้คะแนนเริ่มต้นสำหรับ RFQ ชนิดนั้น</span><span class="sxs-lookup"><span data-stu-id="502c1-107">The scoring method can be associated with a solicitation type as the default scoring method for RFQs of that type.</span></span> <span data-ttu-id="502c1-108">โดยทั่วไปงานเหล่านี้จะดำเนินการโดยผู้จัดการฝ่ายจัดซื้อ</span><span class="sxs-lookup"><span data-stu-id="502c1-108">These tasks would typically be carried out by a purchasing manager.</span></span> <span data-ttu-id="502c1-109">คุณสามารถใช้ขั้นตอนนี้ในข้อมูลสาธิตบริษัท USMF หรือข้อมูลของคุณเอง </span><span class="sxs-lookup"><span data-stu-id="502c1-109">You can use this procedure in demo data company USMF or on your own data.</span></span>

1. <span data-ttu-id="502c1-110">ไปที่การจัดซื้อและการจัดหา > การตั้งค่า > คำขอใบเสนอราคา > วิธีการให้คะแนน</span><span class="sxs-lookup"><span data-stu-id="502c1-110">Go to Procurement and sourcing > Setup > Request for quotation > Scoring method.</span></span>
2. <span data-ttu-id="502c1-111">คลิก สร้าง</span><span class="sxs-lookup"><span data-stu-id="502c1-111">Click New.</span></span>
3. <span data-ttu-id="502c1-112">ในฟิลด์ชื่อ ให้พิมพ์ค่า </span><span class="sxs-lookup"><span data-stu-id="502c1-112">In the Name field, type a value.</span></span>
4. <span data-ttu-id="502c1-113">ในฟิลด์ คำอธิบาย ให้พิมพ์ค่า</span><span class="sxs-lookup"><span data-stu-id="502c1-113">In the Description field, type a value.</span></span>
5. <span data-ttu-id="502c1-114">คลิก บันทึก</span><span class="sxs-lookup"><span data-stu-id="502c1-114">Click Save.</span></span>
6. <span data-ttu-id="502c1-115">คลิก สร้าง</span><span class="sxs-lookup"><span data-stu-id="502c1-115">Click New.</span></span>
7. <span data-ttu-id="502c1-116">ในฟิลด์ชื่อ ให้พิมพ์ค่า </span><span class="sxs-lookup"><span data-stu-id="502c1-116">In the Name field, type a value.</span></span>
8. <span data-ttu-id="502c1-117">ในฟิลด์ คำอธิบาย ให้พิมพ์ค่า</span><span class="sxs-lookup"><span data-stu-id="502c1-117">In the Description field, type a value.</span></span>
    * <span data-ttu-id="502c1-118">คำอธิบายนี้จะแสดงขึ้นพร้อมกับชื่อวิธีการให้คะแนนเมื่อมีการเลือกวิธีการให้คะแนนสำหรับ RFQ</span><span class="sxs-lookup"><span data-stu-id="502c1-118">This description is shown along with the scoring method name when a scoring method is selected for an RFQ.</span></span>  
9. <span data-ttu-id="502c1-119">ในฟิลด์ช่วงเริ่มต้น ให้ป้อนตัวเลข</span><span class="sxs-lookup"><span data-stu-id="502c1-119">In the Range from field, enter a number.</span></span>
    * <span data-ttu-id="502c1-120">ช่วงจำกัดสิ่งที่ผู้เชี่ยวชาญด้านการจัดซื้อสามารถป้อนเป็นคะแนน </span><span class="sxs-lookup"><span data-stu-id="502c1-120">The range limits what the procurement professional can enter as a score.</span></span> <span data-ttu-id="502c1-121">เมื่อมีเกณฑ์การให้คะแนนหลายรายการใน RFQ คะแนนที่ป้อนจะถูกรวมเข้าด้วยกัน และผลรวมจะถูกทำให้พร้อมใช้งานเพื่ออนุญาตให้มีการเปรียบเทียบการประมูล</span><span class="sxs-lookup"><span data-stu-id="502c1-121">When there are multiple scoring criteria on an RFQ, the scores that have been entered are added to each other and the sum is made available to allow the bids to be compared.</span></span>  
10. <span data-ttu-id="502c1-122">ในฟิลด์ช่วงสิ้นสุด ให้ป้อนตัวเลข</span><span class="sxs-lookup"><span data-stu-id="502c1-122">In the Range to field, enter a number.</span></span>
11. <span data-ttu-id="502c1-123">คลิก สร้าง</span><span class="sxs-lookup"><span data-stu-id="502c1-123">Click New.</span></span>
12. <span data-ttu-id="502c1-124">ในฟิลด์ชื่อ ให้พิมพ์ค่า </span><span class="sxs-lookup"><span data-stu-id="502c1-124">In the Name field, type a value.</span></span>
13. <span data-ttu-id="502c1-125">ในฟิลด์ คำอธิบาย ให้พิมพ์ค่า</span><span class="sxs-lookup"><span data-stu-id="502c1-125">In the Description field, type a value.</span></span>
14. <span data-ttu-id="502c1-126">ในฟิลด์ช่วงเริ่มต้น ให้ป้อนตัวเลข</span><span class="sxs-lookup"><span data-stu-id="502c1-126">In the Range from field, enter a number.</span></span>
15. <span data-ttu-id="502c1-127">ในฟิลด์ช่วงสิ้นสุด ให้ป้อนตัวเลข</span><span class="sxs-lookup"><span data-stu-id="502c1-127">In the Range to field, enter a number.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]