---
title: กำหนดนโยบายค่าใช้จ่าย
description: คุณสามารถกำหนดนโยบายค่าใช้จ่ายซึ่งผู้ปฏิบัติงานของคุณต้องปฏิบัติตามเมื่อป้อนหรือส่งรายงานค่าใช้จ่ายและใบเบิกค่าเดินทางใน Microsoft Dynamics 365 for Finance and Operations
author: ryansandness
manager: AnnBe
ms.date: 04/26/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SysPolicyListPage, TrvPolicyRule
audience: Application User
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: ryansand
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 6923a4d5420cd768d1b0da24eab406033c17fd67
ms.sourcegitcommit: 06c8dc5bc4e1c41f68e1cda141d61529768be958
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 05/22/2019
ms.locfileid: "1594947"
---
# <a name="expense-policies"></a><span data-ttu-id="c0dc8-103">นโยบายค่าใช้จ่าย</span><span class="sxs-lookup"><span data-stu-id="c0dc8-103">Expense policies</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="c0dc8-104">คุณสามารถกำหนดนโยบายซึ่งผู้ปฏิบัติงานของคุณต้องปฏิบัติตามเมื่อป้อนหรือส่งรายงานค่าใช้จ่ายและใบเบิกค่าเดินทาง</span><span class="sxs-lookup"><span data-stu-id="c0dc8-104">You can define policies that your workers must follow when entering and submitting expense reports and travel requisitions.</span></span>         
<span data-ttu-id="c0dc8-105">การนำนโยบายค่าใช้จ่ายมาใช้สามารถช่วยให้คุณจัดการค่าใช้จ่ายได้อย่างมีประสิทธิภาพ</span><span class="sxs-lookup"><span data-stu-id="c0dc8-105">Implementing expense policies can help you manage expenses effectively.</span></span>         

<span data-ttu-id="c0dc8-106">ตัวอย่างเช่น คุณสามารถตั้งค่านโยบายสำหรับค่าใช้จ่ายโรงแรมในนิวยอร์ค ซึ่งแจ้งว่าค่าใช้จ่ายต่อคืนต้องไม่เกิน 250 ดอลลาร์สหรัฐฯ</span><span class="sxs-lookup"><span data-stu-id="c0dc8-106">For example, you can set a policy for hotel expenses in New York City, which states that the per night expense cannot exceed USD 250.</span></span>       
<span data-ttu-id="c0dc8-107">หากผู้ปฏิบัติงานส่งรายงานค่าใช้จ่ายหรือใบเบิกค่าเดินทางที่มีอัตราห้องพักเกินกว่ายอดเงินนี้ ระบบจะแจ้งเตือน</span><span class="sxs-lookup"><span data-stu-id="c0dc8-107">If a worker submits an expense report or a travel requisition in which the room rate exceeds this amount, the system will notify the</span></span>        
<span data-ttu-id="c0dc8-108">ผู้ปฏิบัติงานที่มีการเกินยอดเงินที่นโยบายสำหรับค่าใช้จ่าย</span><span class="sxs-lookup"><span data-stu-id="c0dc8-108">worker that the policy amount for the expense has been exceeded.</span></span> <span data-ttu-id="c0dc8-109">คุณสามารถตั้งค่าคอนฟิกข้อความที่ผู้ปฏิบัติงานจะได้รับ เมื่อคุณ</span><span class="sxs-lookup"><span data-stu-id="c0dc8-109">You can configure the message that the worker will receive when you</span></span>        
<span data-ttu-id="c0dc8-110">กำหนดนโยบาย</span><span class="sxs-lookup"><span data-stu-id="c0dc8-110">define the policy.</span></span>      
        
<span data-ttu-id="c0dc8-111">คุณสามารถกำหนดนโยบายสามชนิด:</span><span class="sxs-lookup"><span data-stu-id="c0dc8-111">You can define three types of policies:</span></span>         
        
- <span data-ttu-id="c0dc8-112">คำเตือน – อนุญาตให้ผู้ปฏิบัติงานสามารถส่งรายงานค่าใช้จ่าย หรือใบเบิกค่าเดินทางได้ แต่ค่าใช้จ่ายจะต้องถูกทำเครื่องหมายสำหรับผู้อนุมัติทั้งหมด และ</span><span class="sxs-lookup"><span data-stu-id="c0dc8-112">Warning – Allows the worker to submit an expense report or travel requisition but the expense will be marked for all approvers and</span></span>        
  <span data-ttu-id="c0dc8-113">สำหรับการรายงานภายหลัง</span><span class="sxs-lookup"><span data-stu-id="c0dc8-113">for later reporting.</span></span>        

- <span data-ttu-id="c0dc8-114">ข้อผิดพลาด – กำหนดให้ผู้ปฏิบัติงานต้องแก้ไขค่าใช้จ่ายเพื่อให้สอดคล้องกับนโยบายก่อนที่จะส่งรายงานค่าใช้จ่าย หรือใบเบิกค่าเดินทาง</span><span class="sxs-lookup"><span data-stu-id="c0dc8-114">Error – Requires the worker to revise the expense to comply with the policy before submitting the expense report or travel requisition.</span></span>       
 
 - <span data-ttu-id="c0dc8-115">เหตุผล – กำหนดให้ผู้ปฏิบัติงานหรือผู้จัดการต้องป้อนเหตุผลสำหรับการเกินยอดเงินนโยบายก่อนที่จะส่งรายงานค่าใช้จ่าย หรือใบเบิกค่าเดินทาง</span><span class="sxs-lookup"><span data-stu-id="c0dc8-115">Justification – Requires the worker or a manager to enter a justification for exceeding the policy amount before submitting the expense report or travel requisition.</span></span>        

## <a name="policy-tips"></a><span data-ttu-id="c0dc8-116">เคล็ดลับนโยบาย</span><span class="sxs-lookup"><span data-stu-id="c0dc8-116">Policy tips</span></span>
<span data-ttu-id="c0dc8-117">ต่อไปนี้เป็นคำแนะนำบางอย่างที่สามารถช่วยคุณในการสร้างนโยบายใหม่สำหรับการจัดการค่าใช้จ่าย</span><span class="sxs-lookup"><span data-stu-id="c0dc8-117">Here are a few suggestions that can assist you whe creating new policies for expense management.</span></span> 
* <span data-ttu-id="c0dc8-118">นโยบายเป็นวันที่มีผลบังคับใช้ และจะไม่มีผลบังคับใช้ถ้ามีการสร้างนโยบายด้วยวันที่หลังจากวันที่ที่มีค่าใช้จ่ายเกิดขึ้น</span><span class="sxs-lookup"><span data-stu-id="c0dc8-118">Policies are date effective and won't take effect if the policy is created with a date after the date that the expense occurred.</span></span> <span data-ttu-id="c0dc8-119">ตัวอย่างเช่น ถ้าคุณกำลังสร้างนโยบายใหม่วันนี้เพื่อบังคับใช้ค่าอาหารสูงสุดเป็น $50 ค่าใช้จ่ายที่มีอยู่ใดๆ ที่ป้อนเมื่อวานนี้จะไม่ถูกตรวจสอบเทียบกับนโยบายนี้</span><span class="sxs-lookup"><span data-stu-id="c0dc8-119">For example, if you are creating a new policy today to enforce a maximum meal expense of $50, then any existing expenses entered as of yesterday won't be checked against this policy.</span></span>
* <span data-ttu-id="c0dc8-120">เมื่อสร้างนโยบายสำหรับประเภทค่าใช้จ่ายที่สามารถแสดงรายการได้ ให้พิจารณาการเพิ่มเงื่อนไขสำหรับชนิดของรายการค่าใช้จ่าย</span><span class="sxs-lookup"><span data-stu-id="c0dc8-120">When creating a policy for an expense category that can be itemized, consider adding a condition for expense line type.</span></span> <span data-ttu-id="c0dc8-121">มีนโยบายบางอย่าง เช่น การกำหนดให้การรับสินค้าอาจไม่เหมาะสมสำหรับรายการที่แสดงรายการ และควรใช้กับรายการส่วนหัวหรือรายการที่ไม่มีการแสดงรายการเท่านั้น</span><span class="sxs-lookup"><span data-stu-id="c0dc8-121">Some policies such as requiring a receipt may not make sense for itemized lines and should only be applied to the header line or a non-itemized line.</span></span> 

## <a name="when-to-evaluate-policies"></a><span data-ttu-id="c0dc8-122">เวลาที่จะประเมินนโยบาย</span><span class="sxs-lookup"><span data-stu-id="c0dc8-122">When to evaluate policies</span></span>

<span data-ttu-id="c0dc8-123">ในพารามิเตอร์การจัดการค่าใช้จ่าย จะมีตัวเลือกในการประเมินนโยบายการจัดการค่าใช้จ่าย เมื่อมีการบันทึกรายการ หรือเมื่อมีการส่งรายงานค่าใช้จ่าย</span><span class="sxs-lookup"><span data-stu-id="c0dc8-123">In expense management parameters, there is an option to either evaluate expense management policies when a line is saved or when an expense report is submitted.</span></span> <span data-ttu-id="c0dc8-124">ถ้าคุณเลือกที่จะประเมินเวลาที่มีการบันทึกรายการ นี่จะทำให้แน่ใจว่าผู้ใช้มีความสามารถในการมองเห็นก่อนหน้านี้ถึงสิ่งที่พวกเขาจำเป็นต้องทำ เพื่อให้รายงานค่าใช้จ่ายทั้งหมดของพวกเขาเสร็จสมบูรณ์ในครั้งเดียว</span><span class="sxs-lookup"><span data-stu-id="c0dc8-124">If you choose to evaluate when a line is saved this ensures that users have earlier visibility into what they need to do to complete their expense report all at once.</span></span> <span data-ttu-id="c0dc8-125">มิฉะนั้น คุณสามารถหน่วงเวลาการประเมินนโยบายและประหยัดเวลาได้ ถ้าคุณมีการตรวจสอบความถูกต้องเกิดขึ้นในตอนท้าย ในระหว่างการส่งไปที่ลำดับงาน</span><span class="sxs-lookup"><span data-stu-id="c0dc8-125">Otherwise, you can delay policy evaluation and save time if you have validation occur at the end, during submission to workflow.</span></span>
