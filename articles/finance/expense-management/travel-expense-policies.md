---
title: กำหนดนโยบายค่าใช้จ่าย
description: คุณสามารถกำหนดนโยบายค่าใช้จ่ายซึ่งผู้ปฏิบัติงานของคุณต้องปฏิบัติตาม เมื่อป้อนหรือส่งรายงานค่าใช้จ่ายและใบเบิกค่าเดินทางใน Microsoft Dynamics 365 Finance
author: suvaidya
manager: AnnBe
ms.date: 05/20/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SysPolicyListPage, TrvPolicyRule
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: ryansand
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 22504e0e26c025d117f29dee3b59b41d508e7724
ms.sourcegitcommit: 4f90b9ddedf312e75a714e0ec7f7ee5fd43cac6a
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 05/21/2020
ms.locfileid: "3389726"
---
# <a name="define-expense-policies"></a><span data-ttu-id="222e3-103">กำหนดนโยบายค่าใช้จ่าย</span><span class="sxs-lookup"><span data-stu-id="222e3-103">Define expense policies</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="222e3-104">คุณสามารถกำหนดนโยบายซึ่งผู้ปฏิบัติงานของคุณต้องปฏิบัติตามเมื่อป้อนหรือส่งรายงานค่าใช้จ่ายและใบเบิกค่าเดินทาง</span><span class="sxs-lookup"><span data-stu-id="222e3-104">You can define policies that your workers must follow when entering and submitting expense reports and travel requisitions.</span></span>         
<span data-ttu-id="222e3-105">การนำนโยบายค่าใช้จ่ายมาใช้สามารถช่วยให้คุณจัดการค่าใช้จ่ายได้อย่างมีประสิทธิภาพ</span><span class="sxs-lookup"><span data-stu-id="222e3-105">Implementing expense policies can help you manage expenses effectively.</span></span>         

<span data-ttu-id="222e3-106">ตัวอย่างเช่น คุณสามารถตั้งค่านโยบายสำหรับค่าใช้จ่ายโรงแรมในนิวยอร์ค ซึ่งแจ้งว่าค่าใช้จ่ายต่อคืนต้องไม่เกิน 250 ดอลลาร์สหรัฐฯ</span><span class="sxs-lookup"><span data-stu-id="222e3-106">For example, you can set a policy for hotel expenses in New York City, which states that the per night expense cannot exceed USD 250.</span></span>       
<span data-ttu-id="222e3-107">หากผู้ปฏิบัติงานส่งรายงานค่าใช้จ่ายหรือใบเบิกค่าเดินทางที่มีอัตราห้องพักเกินกว่ายอดเงินนี้ ระบบจะแจ้งเตือน</span><span class="sxs-lookup"><span data-stu-id="222e3-107">If a worker submits an expense report or a travel requisition in which the room rate exceeds this amount, the system will notify the</span></span>        
<span data-ttu-id="222e3-108">ผู้ปฏิบัติงานที่มีการเกินยอดเงินที่นโยบายสำหรับค่าใช้จ่าย</span><span class="sxs-lookup"><span data-stu-id="222e3-108">worker that the policy amount for the expense has been exceeded.</span></span> <span data-ttu-id="222e3-109">คุณสามารถตั้งค่าคอนฟิกข้อความที่ผู้ปฏิบัติงานจะได้รับ เมื่อคุณ</span><span class="sxs-lookup"><span data-stu-id="222e3-109">You can configure the message that the worker will receive when you</span></span>        
<span data-ttu-id="222e3-110">กำหนดนโยบาย</span><span class="sxs-lookup"><span data-stu-id="222e3-110">define the policy.</span></span>      
        
<span data-ttu-id="222e3-111">คุณสามารถกำหนดนโยบายสามชนิด:</span><span class="sxs-lookup"><span data-stu-id="222e3-111">You can define three types of policies:</span></span>         
        
- <span data-ttu-id="222e3-112">คำเตือน – อนุญาตให้ผู้ปฏิบัติงานสามารถส่งรายงานค่าใช้จ่าย หรือใบเบิกค่าเดินทางได้ แต่ค่าใช้จ่ายจะต้องถูกทำเครื่องหมายสำหรับผู้อนุมัติทั้งหมด และ</span><span class="sxs-lookup"><span data-stu-id="222e3-112">Warning – Allows the worker to submit an expense report or travel requisition but the expense will be marked for all approvers and</span></span>        
  <span data-ttu-id="222e3-113">สำหรับการรายงานภายหลัง</span><span class="sxs-lookup"><span data-stu-id="222e3-113">for later reporting.</span></span>        

- <span data-ttu-id="222e3-114">ข้อผิดพลาด – กำหนดให้ผู้ปฏิบัติงานต้องแก้ไขค่าใช้จ่ายเพื่อให้สอดคล้องกับนโยบายก่อนที่จะส่งรายงานค่าใช้จ่าย หรือใบเบิกค่าเดินทาง</span><span class="sxs-lookup"><span data-stu-id="222e3-114">Error – Requires the worker to revise the expense to comply with the policy before submitting the expense report or travel requisition.</span></span>       
 
 - <span data-ttu-id="222e3-115">เหตุผล – กำหนดให้ผู้ปฏิบัติงานหรือผู้จัดการต้องป้อนเหตุผลสำหรับการเกินยอดเงินนโยบายก่อนที่จะส่งรายงานค่าใช้จ่าย หรือใบเบิกค่าเดินทาง</span><span class="sxs-lookup"><span data-stu-id="222e3-115">Justification – Requires the worker or a manager to enter a justification for exceeding the policy amount before submitting the expense report or travel requisition.</span></span>        

## <a name="policy-tips"></a><span data-ttu-id="222e3-116">เคล็ดลับนโยบาย</span><span class="sxs-lookup"><span data-stu-id="222e3-116">Policy tips</span></span>
<span data-ttu-id="222e3-117">ต่อไปนี้เป็นคำแนะนำบางอย่างที่สามารถช่วยคุณในการสร้างนโยบายใหม่สำหรับการจัดการค่าใช้จ่าย</span><span class="sxs-lookup"><span data-stu-id="222e3-117">Here are a few suggestions that can assist you when creating new policies for expense management.</span></span> 
* <span data-ttu-id="222e3-118">นโยบายเป็นวันที่มีผลบังคับใช้ และจะไม่มีผลบังคับใช้ถ้ามีการสร้างนโยบายด้วยวันที่หลังจากวันที่ที่มีค่าใช้จ่ายเกิดขึ้น</span><span class="sxs-lookup"><span data-stu-id="222e3-118">Policies are date effective and won't take effect if the policy is created with a date after the date that the expense occurred.</span></span> <span data-ttu-id="222e3-119">ตัวอย่างเช่น ถ้าคุณกำลังสร้างนโยบายใหม่วันนี้เพื่อบังคับใช้ค่าอาหารสูงสุดเป็น $50 ค่าใช้จ่ายที่มีอยู่ใดๆ ที่ป้อนเมื่อวานนี้จะไม่ถูกตรวจสอบเทียบกับนโยบายนี้</span><span class="sxs-lookup"><span data-stu-id="222e3-119">For example, if you are creating a new policy today to enforce a maximum meal expense of $50, then any existing expenses entered as of yesterday won't be checked against this policy.</span></span>
* <span data-ttu-id="222e3-120">เมื่อสร้างนโยบายสำหรับประเภทค่าใช้จ่ายที่สามารถแสดงรายการได้ ให้พิจารณาการเพิ่มเงื่อนไขสำหรับชนิดของรายการค่าใช้จ่าย</span><span class="sxs-lookup"><span data-stu-id="222e3-120">When creating a policy for an expense category that can be itemized, consider adding a condition for expense line type.</span></span> <span data-ttu-id="222e3-121">มีนโยบายบางอย่าง เช่น การกำหนดให้การรับสินค้าอาจไม่เหมาะสมสำหรับรายการที่แสดงรายการ และควรใช้กับรายการส่วนหัวหรือรายการที่ไม่มีการแสดงรายการเท่านั้น</span><span class="sxs-lookup"><span data-stu-id="222e3-121">Some policies such as requiring a receipt may not make sense for itemized lines and should only be applied to the header line or a non-itemized line.</span></span> 
* <span data-ttu-id="222e3-122">นโยบายการจัดการค่าใช้จ่ายจะถูกประเมินโดยใช้เอนทิตีต้นทางตามค่าเริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="222e3-122">Expense management policies are evaluated against the source entity by default.</span></span> <span data-ttu-id="222e3-123">สำหรับสถานการณ์จำลองระหว่างบริษัท คุณสามารถตั้งค่านโยบายที่จะประเมินโดยใช้เอนทิตีปลายทาง (เอนทิตีขอยืม) แทน</span><span class="sxs-lookup"><span data-stu-id="222e3-123">For intercompany scenarios, you can set the policy to be evaluated against the destination entity (borrowing entity) instead.</span></span> <span data-ttu-id="222e3-124">เมื่อต้องการรันนโยบายสำหรับเอนทิตีปลายทาง ให้เปิดคุณลักษณะ "ประเมินนโยบายค่าใช้จ่ายกับนิติบุคคลที่ขอยืม" ในพื้นที่ทำงาน **การจัดการลักษณะการทำงาน**</span><span class="sxs-lookup"><span data-stu-id="222e3-124">To run the policies against the destination entity, turn on the "Evaluate Expense policy against borrowing legal entity" feature in the **Feature Management** workspace.</span></span>

## <a name="when-to-evaluate-policies"></a><span data-ttu-id="222e3-125">เวลาที่จะประเมินนโยบาย</span><span class="sxs-lookup"><span data-stu-id="222e3-125">When to evaluate policies</span></span>

<span data-ttu-id="222e3-126">ในพารามิเตอร์การจัดการค่าใช้จ่าย จะมีตัวเลือกในการประเมินนโยบายการจัดการค่าใช้จ่าย เมื่อมีการบันทึกรายการ หรือเมื่อมีการส่งรายงานค่าใช้จ่าย</span><span class="sxs-lookup"><span data-stu-id="222e3-126">In expense management parameters, there is an option to either evaluate expense management policies when a line is saved or when an expense report is submitted.</span></span> <span data-ttu-id="222e3-127">ถ้าคุณเลือกที่จะประเมินเวลาที่มีการบันทึกรายการ นี่จะทำให้แน่ใจว่าผู้ใช้มีความสามารถในการมองเห็นก่อนหน้านี้ถึงสิ่งที่พวกเขาจำเป็นต้องทำ เพื่อให้รายงานค่าใช้จ่ายทั้งหมดของพวกเขาเสร็จสมบูรณ์ในครั้งเดียว</span><span class="sxs-lookup"><span data-stu-id="222e3-127">If you choose to evaluate when a line is saved this ensures that users have earlier visibility into what they need to do to complete their expense report all at once.</span></span> <span data-ttu-id="222e3-128">มิฉะนั้น คุณสามารถหน่วงเวลาการประเมินนโยบายและประหยัดเวลาได้ ถ้าคุณมีการตรวจสอบความถูกต้องเกิดขึ้นในตอนท้าย ในระหว่างการส่งไปที่ลำดับงาน</span><span class="sxs-lookup"><span data-stu-id="222e3-128">Otherwise, you can delay policy evaluation and save time if you have validation occur at the end, during submission to workflow.</span></span>
