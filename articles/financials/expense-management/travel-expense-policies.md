---
title: "กำหนดนโยบายค่าใช้จ่าย"
description: "คุณสามารถกำหนดนโยบายค่าใช้จ่ายที่พนักงานของคุณต้องปฏิบัติตามเมื่อป้อนหรือส่งรายงานค่าใช้จ่ายและใบเบิกค่าเดินทางใน Microsoft Dynamics 365 for Finance and Operations, Enterprise edition"
author: saraschi2
manager: AnnBe
ms.date: 02/23/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: SysPolicyListPage, TrvPolicyRule
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 25fa39dc81fc721d7593a25a102ce47041ebc5f0
ms.openlocfilehash: b52fe81015a324bde07f387b42b834b79dc7c2da
ms.contentlocale: th-th
ms.lasthandoff: 03/13/2018

---

# <a name="expense-policies"></a><span data-ttu-id="df6a1-103">นโยบายค่าใช้จ่าย</span><span class="sxs-lookup"><span data-stu-id="df6a1-103">Expense policies</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="df6a1-104">คุณสามารถกำหนดนโยบายซึ่งผู้ปฏิบัติงานของคุณต้องปฏิบัติตามเมื่อป้อนหรือส่งรายงานค่าใช้จ่ายและใบเบิกค่าเดินทาง</span><span class="sxs-lookup"><span data-stu-id="df6a1-104">You can define policies that your workers must follow when entering and submitting expense reports and travel requisitions.</span></span>         
<span data-ttu-id="df6a1-105">การนำนโยบายค่าใช้จ่ายมาใช้สามารถช่วยให้คุณจัดการค่าใช้จ่ายได้อย่างมีประสิทธิภาพ</span><span class="sxs-lookup"><span data-stu-id="df6a1-105">Implementing expense policies can help you manage expenses effectively.</span></span>         

<span data-ttu-id="df6a1-106">ตัวอย่างเช่น คุณสามารถตั้งค่านโยบายสำหรับค่าใช้จ่ายโรงแรมในนิวยอร์ค ซึ่งแจ้งว่าค่าใช้จ่ายต่อคืนต้องไม่เกิน 250 ดอลลาร์สหรัฐฯ</span><span class="sxs-lookup"><span data-stu-id="df6a1-106">For example, you can set a policy for hotel expenses in New York City, which states that the per night expense cannot exceed USD 250.</span></span>       
<span data-ttu-id="df6a1-107">หากผู้ปฏิบัติงานส่งรายงานค่าใช้จ่ายหรือใบเบิกค่าเดินทางที่มีอัตราห้องพักเกินกว่ายอดเงินนี้ ระบบจะแจ้งเตือน</span><span class="sxs-lookup"><span data-stu-id="df6a1-107">If a worker submits an expense report or a travel requisition in which the room rate exceeds this amount, the system will notify the</span></span>        
<span data-ttu-id="df6a1-108">ผู้ปฏิบัติงานที่มีการเกินยอดเงินที่นโยบายสำหรับค่าใช้จ่าย</span><span class="sxs-lookup"><span data-stu-id="df6a1-108">worker that the policy amount for the expense has been exceeded.</span></span> <span data-ttu-id="df6a1-109">คุณสามารถตั้งค่าคอนฟิกข้อความที่ผู้ปฏิบัติงานจะได้รับ เมื่อคุณ</span><span class="sxs-lookup"><span data-stu-id="df6a1-109">You can configure the message that the worker will receive when you</span></span>        
<span data-ttu-id="df6a1-110">กำหนดนโยบาย</span><span class="sxs-lookup"><span data-stu-id="df6a1-110">define the policy.</span></span>      
        
<span data-ttu-id="df6a1-111">คุณสามารถกำหนดนโยบายสามชนิด:</span><span class="sxs-lookup"><span data-stu-id="df6a1-111">You can define three types of policies:</span></span>         
        
- <span data-ttu-id="df6a1-112">คำเตือน – อนุญาตให้ผู้ปฏิบัติงานสามารถส่งรายงานค่าใช้จ่าย หรือใบเบิกค่าเดินทางได้ แต่ค่าใช้จ่ายจะต้องถูกทำเครื่องหมายสำหรับผู้อนุมัติทั้งหมด และ</span><span class="sxs-lookup"><span data-stu-id="df6a1-112">Warning – Allows the worker to submit an expense report or travel requisition but the expense will be marked for all approvers and</span></span>        
<span data-ttu-id="df6a1-113">สำหรับการรายงานภายหลัง</span><span class="sxs-lookup"><span data-stu-id="df6a1-113">for later reporting.</span></span>        

- <span data-ttu-id="df6a1-114">ข้อผิดพลาด – กำหนดให้ผู้ปฏิบัติงานต้องแก้ไขค่าใช้จ่ายเพื่อให้สอดคล้องกับนโยบายก่อนที่จะส่งรายงานค่าใช้จ่าย หรือใบเบิกค่าเดินทาง</span><span class="sxs-lookup"><span data-stu-id="df6a1-114">Error – Requires the worker to revise the expense to comply with the policy before submitting the expense report or travel requisition.</span></span>       
 
 - <span data-ttu-id="df6a1-115">เหตุผล – กำหนดให้ผู้ปฏิบัติงานหรือผู้จัดการต้องป้อนเหตุผลสำหรับการเกินยอดเงินนโยบายก่อนที่จะส่งรายงานค่าใช้จ่าย หรือใบเบิกค่าเดินทาง</span><span class="sxs-lookup"><span data-stu-id="df6a1-115">Justification – Requires the worker or a manager to enter a justification for exceeding the policy amount before submitting the expense report or travel requisition.</span></span>        
 
 <span data-ttu-id="df6a1-116">และคุณยังสามารถตั้งค่าช่วงวันที่ที่นโยบายค่าใช้จ่ายมีผลบังคับใช้ได้ด้วย </span><span class="sxs-lookup"><span data-stu-id="df6a1-116">You can also set up a date range for which expense policies are in effect.</span></span> <span data-ttu-id="df6a1-117">ตัวอย่างเช่น ค่าธรรมเนียมสายการบินสำหรับเที่ยวบินระหว่างเดนมาร์ก</span><span class="sxs-lookup"><span data-stu-id="df6a1-117">For example, airline fares for flights between Denmark</span></span>      
 <span data-ttu-id="df6a1-118">และนิวยอร์คจะมีราคาสูงในช่วงฤดูกาลท่องเที่ยวที่มีวันหยุดยาว</span><span class="sxs-lookup"><span data-stu-id="df6a1-118">and New York City can be expensive during the peak holiday travel season.</span></span> <span data-ttu-id="df6a1-119">คุณสามารถกำหนดกฎค่าใช้จ่ายเที่ยวบินที่จำกัด</span><span class="sxs-lookup"><span data-stu-id="df6a1-119">You can define a flight expense rule that restricts the</span></span>      
 <span data-ttu-id="df6a1-120">ต้นทุนเที่ยวบินไปยังนิวยอร์คถึงขีดจำกัด DKK 5000 และคุณสามารถระบุว่า กฎนี้มีผลบังคับใช้ระหว่างวันที่ 15 มีนาคม และ</span><span class="sxs-lookup"><span data-stu-id="df6a1-120">cost of flights to New York City to a limit of DKK 5000, and you can specify that this rule be in effect between March 15 and</span></span>      
 <span data-ttu-id="df6a1-121">วันที่ 15 กันยายน</span><span class="sxs-lookup"><span data-stu-id="df6a1-121">September 15.</span></span>

