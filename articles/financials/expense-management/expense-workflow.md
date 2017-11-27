---
title: "ลำดับงานค่าใช้จ่าย"
description: "หัวข้อนี้อธิบายวิธีที่คุณสามารถใช้ระบบลำดับงานใน Microsoft Dynamics 365 for Finance and Operations, Enterprise edition เพื่อตั้งค่ากระบวนการตรวจทานสำหรับรายงานค่าใช้จ่ายในการจัดการค่าใช้จ่าย"
author: saraschi2
manager: AnnBe
ms.date: 09/13/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: saraschi2
ms.search.validFrom:
- month/year of release that feature was introduced in
- in format yyyy-mm-dd
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: d60d2f462a1fd27d4655e68aab7f96fb28a34b77
ms.contentlocale: th-th
ms.lasthandoff: 11/03/2017

---

# <a name="expense-workflow"></a><span data-ttu-id="f865c-103">ลำดับงานค่าใช้จ่าย</span><span class="sxs-lookup"><span data-stu-id="f865c-103">Expense workflow</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="f865c-104">คุณสามารถใช้ระบบลำดับงานใน Microsoft Dynamics 365 for Finance and Operations, Enterprise edition เพื่อตั้งค่ากระบวนการตรวจทานสำหรับรายงานค่าใช้จ่ายในการจัดการค่าใช้จ่าย</span><span class="sxs-lookup"><span data-stu-id="f865c-104">You can use the workflow system in Microsoft Dynamics 365 for Finance and Operations, Enterprise edition, to set up a review process for expense reports in Expense management.</span></span> <span data-ttu-id="f865c-105">คุณสามารถตั้งค่าลำดับงานที่ใช้เงื่อนไขต่อไปนี้เพื่อกำหนดผู้อนุมัติรายงานค่าใช้จ่าย:</span><span class="sxs-lookup"><span data-stu-id="f865c-105">You can set up a workflow that uses the following criteria to determine who approves expense reports:</span></span>

- <span data-ttu-id="f865c-106">พนักงานที่รายงานลำดับชั้นและขีดจำกัดการอนุมัติที่กำหนดไว้ล่วงหน้า</span><span class="sxs-lookup"><span data-stu-id="f865c-106">The employee reporting hierarchy and predefined approval limits</span></span>
- <span data-ttu-id="f865c-107">การอนุมัติแบบหลายระดับที่สนับสนุนผู้อนุมัติชั่วคราวและผู้อนุมัติขั้นสุดท้าย</span><span class="sxs-lookup"><span data-stu-id="f865c-107">Multi-level approval that supports interim approvers and a final approver</span></span>
- <span data-ttu-id="f865c-108">มิติทางการเงินและความรับผิดชอบของโครงการ</span><span class="sxs-lookup"><span data-stu-id="f865c-108">Financial dimensions and project responsibility</span></span>
- <span data-ttu-id="f865c-109">การกำหนดให้กับผู้ใช้หรือกลุ่มผู้ใช้</span><span class="sxs-lookup"><span data-stu-id="f865c-109">Assignment to specific users or user groups</span></span>

<span data-ttu-id="f865c-110">คุณสามารถสร้างการอนุมัติลำดับงานสำหรับรายงานค่าใช้จ่าย ใบเบิกค่าเดินทาง เงินทดรองจ่าย และการขอคืนภาษีมูลค่าเพิ่ม (VAT)</span><span class="sxs-lookup"><span data-stu-id="f865c-110">Workflow approvals can be created for expense reports, travel requisitions, cash advances, and value-added tax (VAT) recovery.</span></span>

<span data-ttu-id="f865c-111">**ตัวอย่าง**</span><span class="sxs-lookup"><span data-stu-id="f865c-111">**Example**</span></span>

<span data-ttu-id="f865c-112">กระบวนการต่อไปนี้เป็นตัวอย่างของลำดับงานการจัดการค่าใช้จ่ายของรายงานค่าใช้จ่าย</span><span class="sxs-lookup"><span data-stu-id="f865c-112">The following process is an example of the expense management workflow for an expense report.</span></span>

1. <span data-ttu-id="f865c-113">พนักงานสร้างและบันทึกรายงานค่าใช้จ่าย</span><span class="sxs-lookup"><span data-stu-id="f865c-113">An employee creates and saves an expense report.</span></span>
2. <span data-ttu-id="f865c-114">พนักงานส่งรายงานค่าใช้จ่ายเพื่อขออนุมัติ</span><span class="sxs-lookup"><span data-stu-id="f865c-114">The employee submits the expense report for approval.</span></span> <span data-ttu-id="f865c-115">มีการระบุผู้อนุมัติตามกฎที่กำหนดเมื่อมีการตั้งค่าลำดับงาน</span><span class="sxs-lookup"><span data-stu-id="f865c-115">The approver is identified based on the rules that were defined when the workflow was set up.</span></span>
3. <span data-ttu-id="f865c-116">ผู้อนุมัติได้รับการแจ้งเตือนว่ารายงานค่าใช้จ่ายพร้อมสำหรับการอนุมัติ</span><span class="sxs-lookup"><span data-stu-id="f865c-116">The approver receives a notification that an expense report is ready for approval.</span></span> <span data-ttu-id="f865c-117">ผู้อนุมัติตรวจทานรายงานค่าใช้จ่าย และตรวจสอบว่าเป็นไปตามเงื่อนไขต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="f865c-117">The approver reviews the expense report and verifies that the following conditions are met:</span></span>

    - <span data-ttu-id="f865c-118">ค่าใช้จ่ายไม่ละเมิดนโยบายค่าใช้จ่ายใด ๆ</span><span class="sxs-lookup"><span data-stu-id="f865c-118">The expenses don't violate any expense policies.</span></span> <span data-ttu-id="f865c-119">ถ้าค่าใช้จ่ายละเมิดนโยบาย ผู้อนุมัติจะต้องตรวจสอบว่ารายงานค่าใช้จ่ายมีการให้เหตุผลทางธุรกิจที่ถูกต้อง</span><span class="sxs-lookup"><span data-stu-id="f865c-119">If an expense violates a policy, the approver verifies that the expense report includes a valid business justification.</span></span>
    - <span data-ttu-id="f865c-120">มีการแนบใบเสร็จรับเงินกับรายงานค่าใช้จ่าย</span><span class="sxs-lookup"><span data-stu-id="f865c-120">Electronic receipts are attached to the expense report.</span></span>

4. <span data-ttu-id="f865c-121">ผู้อนุมัติอนุมัติรายงานค่าใช้จ่าย</span><span class="sxs-lookup"><span data-stu-id="f865c-121">The approver approves the expense report.</span></span>
5. <span data-ttu-id="f865c-122">จะมีการกำหนดรายงานค่าใช้จ่ายให้กับผู้ประสานงานบัญชีเจ้าหนี้เพื่อการลงรายการบัญชี</span><span class="sxs-lookup"><span data-stu-id="f865c-122">The expense report is assigned to the Accounts payable coordinator for posting.</span></span>
6. <span data-ttu-id="f865c-123">หนึ่งในขั้นตอนต่อไปนี้จะเกิดขึ้นโดยขึ้นอยู่กับว่ามีการกำหนดค่าการลงรายการบัญชีอัตโนมัติหรือไม่:</span><span class="sxs-lookup"><span data-stu-id="f865c-123">One of the following steps occurs, depending on whether automatic posting is configured:</span></span>

    - <span data-ttu-id="f865c-124">ถ้ามีการกำหนดค่าการลงรายการบัญชีโดยอัตโนมัติ รายงานค่าใช้จ่ายจะมีการประมวลผลสำหรับการชำระเงิน และจะมีการปรับปรุงสถานะของรายงานค่าใช้จ่าย</span><span class="sxs-lookup"><span data-stu-id="f865c-124">If automatic posting is configured, the expense report is processed for payment, and the status of the expense report is updated.</span></span>
    - <span data-ttu-id="f865c-125">ถ้าไม่มีการกำหนดค่าการลงรายการบัญชีโดยอัตโนมัติ ผู้ประสานงานบัญชีเจ้าหนี้จะตรวจสอบว่ามีการส่งใบเสร็จรับเงินต้นฉบับทั้งหมดหรือไม่ และการรับสินค้าสอดคล้องกับค่าใช้จ่ายในรายงานค่าใช้จ่ายหรือไม่</span><span class="sxs-lookup"><span data-stu-id="f865c-125">If automatic posting isn't configured, the Accounts payable coordinator verifies that all original receipts have been submitted, and that the receipts are aligned with the expenses on the expense report.</span></span> <span data-ttu-id="f865c-126">นอกจากนี้ยังต้องสามารถตรวจสอบว่ารหัสภาษีทั้งหมดที่ป้อนในรายงานค่าใช้จ่ายถูกต้องอีกด้วย</span><span class="sxs-lookup"><span data-stu-id="f865c-126">All tax codes that are entered on the expense report must also be verified as correct.</span></span>

<span data-ttu-id="f865c-127">หลังจากที่มีการตรวจสอบข้อกำหนดเหล่านี้ จะมีการลงรายการรายงานค่าใช้จ่าย</span><span class="sxs-lookup"><span data-stu-id="f865c-127">After these requirements are verified, the expense report is posted.</span></span>

<span data-ttu-id="f865c-128">หลังจากที่ลงรายการบัญชีรายงานค่าใช้จ่าย การชำระเงินจะได้รับอนุมัติสำหรับรายงานค่าใช้จ่าย และพนักงานจะได้รับการชำระเงินคืน</span><span class="sxs-lookup"><span data-stu-id="f865c-128">After the expense report is posted, payment is authorized for the expense report, and the employee is reimbursed.</span></span>

