---
title: สร้างวิธีการให้คะแนนสำหรับ RFQ
description: 'กระบวนงานนี้แสดงวิธีการสร้างวิธีการให้คะแนน '
author: mkirknel
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: PurchRFQScoringMethod
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 98bcffdf63e20a0a620aa87b44449ce13a5df2fe
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 05/15/2019
ms.locfileid: "1565288"
---
# <a name="create-a-scoring-method-for-rfqs"></a><span data-ttu-id="d0b17-103">สร้างวิธีการให้คะแนนสำหรับ RFQ</span><span class="sxs-lookup"><span data-stu-id="d0b17-103">Create a scoring method for RFQs</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="d0b17-104">กระบวนงานนี้แสดงวิธีการสร้างวิธีการให้คะแนน </span><span class="sxs-lookup"><span data-stu-id="d0b17-104">This procedure shows you how to create a scoring method.</span></span> <span data-ttu-id="d0b17-105">วิธีการให้คะแนนคือชุดของเงื่อนไขที่สามารถใช้เพื่อเปรียบเทียบการประมูลที่ส่งในการตอบคำขอใบเสนอราคา (RFQ) </span><span class="sxs-lookup"><span data-stu-id="d0b17-105">A scoring method is a set of criteria that can be used to compare bids that are sent in reply to a request for quotation (RFQ).</span></span> <span data-ttu-id="d0b17-106">ตัวอย่างเช่น คุณอาจต้องการจัดอันดับผู้จัดจำหน่ายตามผลการปฏิบัติงานในอดีต หรือจัดอันดับว่าบริษัทเป็นมิตรต่อสิ่งแวดล้อม หรือเป็นผู้ให้ความร่วมมือที่ดีหรือไม่ หรือคุณอาจต้องการเปรียบเทียบการประมูลตามราคา</span><span class="sxs-lookup"><span data-stu-id="d0b17-106">For example, you might want to rate a vendor on past performance, or rate whether the company is environmentally friendly or a good collaborator, or you might want to compare bids based on price.</span></span> <span data-ttu-id="d0b17-107">วิธีการให้คะแนนสามารถเชื่อมโยงกับชนิดการร้องขอเป็นวิธีการให้คะแนนเริ่มต้นสำหรับ RFQ ชนิดนั้น</span><span class="sxs-lookup"><span data-stu-id="d0b17-107">The scoring method can be associated with a solicitation type as the default scoring method for RFQs of that type.</span></span> <span data-ttu-id="d0b17-108">โดยทั่วไปงานเหล่านี้จะดำเนินการโดยผู้จัดการฝ่ายจัดซื้อ</span><span class="sxs-lookup"><span data-stu-id="d0b17-108">These tasks would typically be carried out by a purchasing manager.</span></span> <span data-ttu-id="d0b17-109">คุณสามารถใช้ขั้นตอนนี้ในข้อมูลสาธิตบริษัท USMF หรือข้อมูลของคุณเอง </span><span class="sxs-lookup"><span data-stu-id="d0b17-109">You can use this procedure in demo data company USMF or on your own data.</span></span>

1. <span data-ttu-id="d0b17-110">ไปที่การจัดซื้อและการจัดหา > การตั้งค่า > คำขอใบเสนอราคา > วิธีการให้คะแนน</span><span class="sxs-lookup"><span data-stu-id="d0b17-110">Go to Procurement and sourcing > Setup > Request for quotation > Scoring method.</span></span>
2. <span data-ttu-id="d0b17-111">คลิก สร้าง</span><span class="sxs-lookup"><span data-stu-id="d0b17-111">Click New.</span></span>
3. <span data-ttu-id="d0b17-112">ในฟิลด์ชื่อ ให้พิมพ์ค่า </span><span class="sxs-lookup"><span data-stu-id="d0b17-112">In the Name field, type a value.</span></span>
4. <span data-ttu-id="d0b17-113">ในฟิลด์ คำอธิบาย ให้พิมพ์ค่า</span><span class="sxs-lookup"><span data-stu-id="d0b17-113">In the Description field, type a value.</span></span>
5. <span data-ttu-id="d0b17-114">คลิก บันทึก</span><span class="sxs-lookup"><span data-stu-id="d0b17-114">Click Save.</span></span>
6. <span data-ttu-id="d0b17-115">คลิก สร้าง</span><span class="sxs-lookup"><span data-stu-id="d0b17-115">Click New.</span></span>
7. <span data-ttu-id="d0b17-116">ในฟิลด์ชื่อ ให้พิมพ์ค่า </span><span class="sxs-lookup"><span data-stu-id="d0b17-116">In the Name field, type a value.</span></span>
8. <span data-ttu-id="d0b17-117">ในฟิลด์ คำอธิบาย ให้พิมพ์ค่า</span><span class="sxs-lookup"><span data-stu-id="d0b17-117">In the Description field, type a value.</span></span>
    * <span data-ttu-id="d0b17-118">คำอธิบายนี้จะแสดงขึ้นพร้อมกับชื่อวิธีการให้คะแนนเมื่อมีการเลือกวิธีการให้คะแนนสำหรับ RFQ</span><span class="sxs-lookup"><span data-stu-id="d0b17-118">This description is shown along with the scoring method name when a scoring method is selected for an RFQ.</span></span>  
9. <span data-ttu-id="d0b17-119">ในฟิลด์ช่วงเริ่มต้น ให้ป้อนตัวเลข</span><span class="sxs-lookup"><span data-stu-id="d0b17-119">In the Range from field, enter a number.</span></span>
    * <span data-ttu-id="d0b17-120">ช่วงจำกัดสิ่งที่ผู้เชี่ยวชาญด้านการจัดซื้อสามารถป้อนเป็นคะแนน </span><span class="sxs-lookup"><span data-stu-id="d0b17-120">The range limits what the procurement professional can enter as a score.</span></span> <span data-ttu-id="d0b17-121">เมื่อมีเกณฑ์การให้คะแนนหลายรายการใน RFQ คะแนนที่ป้อนจะถูกรวมเข้าด้วยกัน และผลรวมจะถูกทำให้พร้อมใช้งานเพื่ออนุญาตให้มีการเปรียบเทียบการประมูล</span><span class="sxs-lookup"><span data-stu-id="d0b17-121">When there are multiple scoring criteria on an RFQ, the scores that have been entered are added to each other and the sum is made available to allow the bids to be compared.</span></span>  
10. <span data-ttu-id="d0b17-122">ในฟิลด์ช่วงสิ้นสุด ให้ป้อนตัวเลข</span><span class="sxs-lookup"><span data-stu-id="d0b17-122">In the Range to field, enter a number.</span></span>
11. <span data-ttu-id="d0b17-123">คลิก สร้าง</span><span class="sxs-lookup"><span data-stu-id="d0b17-123">Click New.</span></span>
12. <span data-ttu-id="d0b17-124">ในฟิลด์ชื่อ ให้พิมพ์ค่า </span><span class="sxs-lookup"><span data-stu-id="d0b17-124">In the Name field, type a value.</span></span>
13. <span data-ttu-id="d0b17-125">ในฟิลด์ คำอธิบาย ให้พิมพ์ค่า</span><span class="sxs-lookup"><span data-stu-id="d0b17-125">In the Description field, type a value.</span></span>
14. <span data-ttu-id="d0b17-126">ในฟิลด์ช่วงเริ่มต้น ให้ป้อนตัวเลข</span><span class="sxs-lookup"><span data-stu-id="d0b17-126">In the Range from field, enter a number.</span></span>
15. <span data-ttu-id="d0b17-127">ในฟิลด์ช่วงสิ้นสุด ให้ป้อนตัวเลข</span><span class="sxs-lookup"><span data-stu-id="d0b17-127">In the Range to field, enter a number.</span></span>

