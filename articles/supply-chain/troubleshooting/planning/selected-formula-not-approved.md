---
title: หมายเลขสูตรที่เลือกไม่ได้รับการอนุมัติในใบสั่งชุดงาน
description: เมื่อคุณพยายามยืนยันแผนการใบสั่ง คุณจะได้รับข้อความแสดงข้อผิดพลาดที่ระบุว่าหมายเลขสูตรที่เลือกไม่ได้รับอนุมัติให้กับใบสั่งชุดงาน
author: ankubik
ms.date: 06/10/2021
ms.topic: troubleshooting
ms.search.form: ReqTransPo
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: ankubik
ms.search.validFrom: 2021-06-10
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 4f993c92ca0a2f8f79e4b0e0eda43904529163f8
ms.sourcegitcommit: 18ca2df785e9656fdd4e8c0734eca2b2624fda10
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 06/22/2021
ms.locfileid: "6294187"
---
# <a name="selected-formula-number-isnt-approved-for-a-batch-order"></a><span data-ttu-id="0dde5-103">หมายเลขสูตรที่เลือกไม่ได้รับการอนุมัติในใบสั่งชุดงาน</span><span class="sxs-lookup"><span data-stu-id="0dde5-103">Selected formula number isn't approved for a batch order</span></span>

<span data-ttu-id="0dde5-104">รหัสข้อผิดพลาด: PRO2614</span><span class="sxs-lookup"><span data-stu-id="0dde5-104">Error code: PRO2614</span></span>

## <a name="symptoms"></a><span data-ttu-id="0dde5-105">อาการ</span><span class="sxs-lookup"><span data-stu-id="0dde5-105">Symptoms</span></span>

<span data-ttu-id="0dde5-106">เมื่อคุณพยายามยืนยันแผนการใบสั่ง คุณจะได้รับข้อความแสดงข้อผิดพลาดต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="0dde5-106">When you try to firm a planned order, you receive the following error message:</span></span>

> <span data-ttu-id="0dde5-107">หมายเลขสูตรที่เลือกไม่ได้รับการอนุมัติสำหรับใบสั่งชุดงาน</span><span class="sxs-lookup"><span data-stu-id="0dde5-107">The selected formula number is not approved for a batch order.</span></span>

## <a name="cause"></a><span data-ttu-id="0dde5-108">สาเหตุ</span><span class="sxs-lookup"><span data-stu-id="0dde5-108">Cause</span></span>

<span data-ttu-id="0dde5-109">ระบบจะตรวจสอบความถูกต้องของการดําเนินการยืนยันเพื่อให้แน่ใจว่าสูตรที่ได้รับอนุมัติแล้วพร้อมใช้งานของสินค้าที่ใช้งานอยู่</span><span class="sxs-lookup"><span data-stu-id="0dde5-109">The system validates the firming operation to make sure that an approved formula is available for the active item.</span></span> <span data-ttu-id="0dde5-110">คุณอาจต้องอนุมัติสูตร</span><span class="sxs-lookup"><span data-stu-id="0dde5-110">You must probably approve the formula.</span></span>

## <a name="resolution"></a><span data-ttu-id="0dde5-111">การแก้ปัญหา</span><span class="sxs-lookup"><span data-stu-id="0dde5-111">Resolution</span></span>

<span data-ttu-id="0dde5-112">หากต้องการอนุมัติสูตร ให้ทำตามขั้นตอนเหล่านี้:</span><span class="sxs-lookup"><span data-stu-id="0dde5-112">To approve a formula, follow these steps.</span></span>

1. <span data-ttu-id="0dde5-113">ไปที่ **การจัดการข้อมูลผลิตภัณฑ์ \> สูตรการผลิตและสูตร \> สูตร**</span><span class="sxs-lookup"><span data-stu-id="0dde5-113">Go to **Product information management \> Bills of materials and formulas \> Formulas**.</span></span>
1. <span data-ttu-id="0dde5-114">เลือกสูตรที่เกี่ยวข้อง</span><span class="sxs-lookup"><span data-stu-id="0dde5-114">Select the relevant formula.</span></span>
1. <span data-ttu-id="0dde5-115">ในบานหน้าต่างการดำเนินการ บนแท็บ **สูตร** ในกลุ่ม **รักษา** ให้เลือก **อนุมัติสูตร**</span><span class="sxs-lookup"><span data-stu-id="0dde5-115">On the Action Pane, on the **Formula** tab, in the **Maintain** group, select **Approve formula**.</span></span>
1. <span data-ttu-id="0dde5-116">ในกล่องโต้ตอบ **อนุมัติ BOM หรือสูตร** ให้เลือกผู้อนุมัติ แล้วเลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="0dde5-116">In the **Approve BOM or formula** dialog box, select an approver, and then select **OK**.</span></span>
