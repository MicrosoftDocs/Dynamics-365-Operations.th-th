---
title: รายงานค่าใช้จ่ายและผู้อนุมัติหลายราย
description: หัวข้อนี้แสดงข้อมูลเกี่ยวกับรายงานค่าใช้จ่ายที่ต้องการการอนุมัติโดยบุคคลมากกว่าหนึ่งราย
author: saraschi2
manager: AnnBe
ms.date: 02/23/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TrvExpensesReportList
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 2d83a473e2e894856c12b36b4d005c6cb06b765a
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 09/27/2019
ms.locfileid: "2180152"
---
# <a name="expense-reports-and-multiple-approvers"></a><span data-ttu-id="d4762-103">รายงานค่าใช้จ่ายและผู้อนุมัติหลายราย</span><span class="sxs-lookup"><span data-stu-id="d4762-103">Expense reports and multiple approvers</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="d4762-104">โดยขึ้นอยู่กับนโยบายการอนุมัติค่าใช้จ่ายขององค์กรของคุณ บุคคลมากกว่าหนึ่งรายอาจต้องอนุมัติรายงานค่าใช้จ่ายที่ถูกส่งโดยพนักงาน</span><span class="sxs-lookup"><span data-stu-id="d4762-104">Depending on your organization's expense approval policies, more than one person might have to approve an expense report that is submitted by an employee.</span></span> <span data-ttu-id="d4762-105">เมื่อคุณตั้งค่ากระบวนการลำดับงานสำหรับการอนุมัติรายงานค่าใช้จ่าย คุณสามารถเพิ่มองค์ประกอบลำดับงานที่มีงานหรือขั้นตอนสำหรับผู้อนุมัติรายงานค่าใช้จ่ายหนึ่งรายขึ้นไป</span><span class="sxs-lookup"><span data-stu-id="d4762-105">When you set up the workflow process for expense report approval, you can add workflow elements that include tasks or steps for one or more expense report approvers.</span></span> <span data-ttu-id="d4762-106">ตัวอย่างเช่น คุณอาจต้องการให้รายงานค่าใช้จ่ายทั้งหมดได้รับการอนุมัติก่อน โดยผู้จัดการของพนักงานที่ส่งรายงานแล้ว และจากนั้นโดยผู้ประสานงานบัญชีเจ้าหนี้</span><span class="sxs-lookup"><span data-stu-id="d4762-106">For example, you might require that all expense reports be approved first by the manager of the employee who submitted the report and then by the Accounts payable coordinator.</span></span>

<span data-ttu-id="d4762-107">ถ้าคุณตัดสินใจที่จะมีผู้อนุมัติรายงานค่าใช้จ่ายหลายราย คุณสามารถเพิ่มองค์ประกอบลำดับงานในลักษณะใดๆ ต่อไปนี้ได้:</span><span class="sxs-lookup"><span data-stu-id="d4762-107">If you decide to require multiple expense report approvers, you can add the workflow elements in any of the following ways:</span></span>

- <span data-ttu-id="d4762-108">เพิ่มองค์ประกอบการอนุมัติหนึ่งรายการที่มีขั้นตอนเดียว</span><span class="sxs-lookup"><span data-stu-id="d4762-108">Add one approval element that has one step.</span></span> <span data-ttu-id="d4762-109">ตัวอย่างเช่น ขั้นตอนอาจต้องการให้รายงานค่าใช้จ่ายถูกกำหนดให้กับกลุ่มผู้ใช้ และให้ได้รับการอนุมัติโดย 50 เปอร์เซ็นต์ของสมาชิกของกลุ่มผู้ใช้</span><span class="sxs-lookup"><span data-stu-id="d4762-109">For example, the step might require that an expense report be assigned to a user group, and that it be approved by 50 percent of the user group's members.</span></span>
- <span data-ttu-id="d4762-110">เพิ่มองค์ประกอบการอนุมัติหนึ่งรายการที่มีขั้นตอนหลายขั้นตอน</span><span class="sxs-lookup"><span data-stu-id="d4762-110">Add one approval element that has multiple steps.</span></span> <span data-ttu-id="d4762-111">ตัวอย่างเช่น องค์ประกอบการอนุมัติอาจมีขั้นตอนต่างๆ ต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="d4762-111">For example, the approval element might have the following steps:</span></span>

    1. <span data-ttu-id="d4762-112">ผู้จัดการของพนักงานที่ส่งรายงานค่าใช้จ่ายเป็นผู้อนุมัติ</span><span class="sxs-lookup"><span data-stu-id="d4762-112">The manager of the employee who submitted the expense report approves it.</span></span>
    2. <span data-ttu-id="d4762-113">เจ้าหน้าที่บัญชีเจ้าหนี้ตรวจสอบใบเสร็จและรายการในรายงานค่าใช้จ่าย</span><span class="sxs-lookup"><span data-stu-id="d4762-113">The Accounts payable clerk verifies the receipts and the expense report items.</span></span>
    3. <span data-ttu-id="d4762-114">เจ้าของงบประมาณอนุมัติรายงานค่าใช้จ่าย</span><span class="sxs-lookup"><span data-stu-id="d4762-114">The budget owner approves the expense report.</span></span>

- <span data-ttu-id="d4762-115">เพิ่มองค์ประกอบการอนุมัติหลายรายการ แต่ละรายการจะมีหนึ่งขั้นตอน</span><span class="sxs-lookup"><span data-stu-id="d4762-115">Add multiple approval elements, each of which has one step.</span></span> <span data-ttu-id="d4762-116">ตัวอย่างเช่น คุณอาจเพิ่มองค์ประกอบการอนุมัติแยกต่างหากสำหรับแต่ละขั้นตอนต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="d4762-116">For example, you might add a separate approval element for each of the following steps:</span></span>

    1. <span data-ttu-id="d4762-117">ผู้จัดการของพนักงานอนุมัติรายงานค่าใช้จ่าย</span><span class="sxs-lookup"><span data-stu-id="d4762-117">The employee's manager approves the expense report.</span></span>
    2. <span data-ttu-id="d4762-118">เจ้าของงบประมาณอนุมัติรายงานค่าใช้จ่าย</span><span class="sxs-lookup"><span data-stu-id="d4762-118">The budget owner approves the expense report.</span></span>
