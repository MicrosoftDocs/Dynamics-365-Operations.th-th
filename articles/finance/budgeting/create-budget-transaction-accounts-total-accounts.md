---
title: สร้างงบประมาณจากบัญชีธุรกรรมและบัญชีผลรวม
description: บทความนี้แสดงภาพรวมของกระบวนการสร้างงบประมาณที่ขึ้นอยู่กับบัญชีผลรวม นอกจากนี้ยังอธิบายวิธีการเปิดการควบคุมงบประมาณสำหรับบัญชีผลรวม ถ้าจำเป็นต้องมีการควบคุมงบประมาณ
author: ShylaThompson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: BudgetControlConfiguration, BudgetPlanGenerate
audience: Application User
ms.reviewer: roschlom
ms.custom: 13051
ms.assetid: fb1bb2d3-445c-402f-a9a3-aa6503eed78e
ms.search.region: Global
ms.author: sigitac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 085bc12433616d2da2bda40a8412fb88e40db3b9
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 02/15/2021
ms.locfileid: "5210204"
---
# <a name="create-a-budget-from-transaction-accounts-and-total-accounts"></a><span data-ttu-id="514a6-104">สร้างงบประมาณจากบัญชีธุรกรรมและบัญชีผลรวม</span><span class="sxs-lookup"><span data-stu-id="514a6-104">Create a budget from transaction accounts and total accounts</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="514a6-105">บทความนี้แสดงภาพรวมของกระบวนการสร้างงบประมาณที่ขึ้นอยู่กับบัญชีผลรวม</span><span class="sxs-lookup"><span data-stu-id="514a6-105">This article provides an overview of the process for creating budgets based on total accounts.</span></span> <span data-ttu-id="514a6-106">นอกจากนี้ยังอธิบายวิธีการเปิดการควบคุมงบประมาณสำหรับบัญชีผลรวม ถ้าจำเป็นต้องมีการควบคุมงบประมาณ</span><span class="sxs-lookup"><span data-stu-id="514a6-106">It also explains how to turn on budget control for total accounts, if budget control is required.</span></span>

<span data-ttu-id="514a6-107">ทั้งเอกสารแผนงบประมาณและเอกสารรายการทะเบียนงบประมาณที่อนุญาตสำหรับการจัดทำงบประมาณบนบัญชีหลักที่มีชนิดบัญชีหลักของ **ผลรวม**</span><span class="sxs-lookup"><span data-stu-id="514a6-107">Both budget plan and budget register entry documents allow for budgeting on main accounts that have a main account type of **Total**.</span></span> <span data-ttu-id="514a6-108">สามารถลงรายการบัญชีที่เกิดขึ้นจริงกับธุรกรรมบัญชีหลักเท่านั้น</span><span class="sxs-lookup"><span data-stu-id="514a6-108">Actuals can be posted only to transactional main accounts.</span></span> 

<span data-ttu-id="514a6-109">สำหรับกระบวนการประจำงวด **การสร้างแผนงบประมาณจากบัญชีแยกประเภททั่วไป** บนแท็บ **แหล่งที่มา** คุณสามารถระบุชนิดบัญชีหลักเป็น **ผลรวม** เป็นเงื่อนไขได้</span><span class="sxs-lookup"><span data-stu-id="514a6-109">For the **Generate budget plan from General ledger** periodic process, on the **Source** tab, you can specify the **Total** main account type as a criterion.</span></span> <span data-ttu-id="514a6-110">ในกรณีนี้ แต่ละผลรวมบัญชีหลักจะรวมอยู่ในแผนงบประมาณเป้าหมาย และยอดเงินจะเท่ากับจำนวนรวมของช่วงบัญชีหลักที่เลือก</span><span class="sxs-lookup"><span data-stu-id="514a6-110">In this case, each total main account will be included in the target budget plan, and the amount will equal the total amount of the range of selected main accounts.</span></span> 

<span data-ttu-id="514a6-111">คุณสามารถเรียกใช้การควบคุมงบประมาณสำหรับบัญชีหลักของชนิด **ผลรวม**</span><span class="sxs-lookup"><span data-stu-id="514a6-111">You can activate budget control for main accounts of the **Total** type.</span></span> <span data-ttu-id="514a6-112">ฟังก์ชันนี้ได้รับการสนับสนุนผ่านการใช้กลุ่มงบประมาณ</span><span class="sxs-lookup"><span data-stu-id="514a6-112">This functionality is supported through the use of budget groups.</span></span> <span data-ttu-id="514a6-113">สำหรับแต่ละผลรวมบัญชีหลัก คุณต้องสร้างงบประมาณที่ควรถูกควบคุมสำหรับกลุ่มงบประมาณในหน้า **การตั้งค่าคอนฟิกการควบคุมงบประมาณ**</span><span class="sxs-lookup"><span data-stu-id="514a6-113">For each total main account, the budget that should be controlled for a budget group must be created on the \*\*Budget control configuration \*\*page.</span></span> <span data-ttu-id="514a6-114">เงื่อนไขที่คุณระบุต้องรวมผลรวมบัญชีหลักและช่วงของบัญชี</span><span class="sxs-lookup"><span data-stu-id="514a6-114">The criteria that you specify must include the total main account and the range of accounts.</span></span> <span data-ttu-id="514a6-115">เมื่อต้องการเพิ่มความเร็วกระบวนการการสร้างกลุ่มงบประมาณ คุณสามารถใช้ประโยชน์ของเอนทิตี้ข้อมูลของกลุ่มการควบคุมงบประมาณ</span><span class="sxs-lookup"><span data-stu-id="514a6-115">To speed up the process of creating budget groups, you can take advantage of the Budget control groups data entity.</span></span> 

<span data-ttu-id="514a6-116">เมื่อใช้งบประมาณในการรายงาน ตัวอย่างเช่น บนงบการเงิน ผลรวมของงบประมาณสำหรับบัญชีผลรวมจะประกอบด้วยจำนวนดังนี้:</span><span class="sxs-lookup"><span data-stu-id="514a6-116">When a budget is used in reporting, such as on a financial statement, the budget sum for the total account consists of the following amounts:</span></span>

-   <span data-ttu-id="514a6-117">งบประมาณที่ถูกสร้างจากธุรกรรมบัญชีแยกประเภทแต่ละบัญชีภายในช่วงของบัญชีผลรวม</span><span class="sxs-lookup"><span data-stu-id="514a6-117">The budgets that are created from each transaction ledger account in the interval of the total account.</span></span>
-   <span data-ttu-id="514a6-118">จำนวนเงินงบประมาณถูกป้อนโดยตรงในบัญชีผลรวม</span><span class="sxs-lookup"><span data-stu-id="514a6-118">The budget amount that is entered directly on the total account.</span></span>

<span data-ttu-id="514a6-119">ดังนั้น คุณสามารถสร้างงบประมาณที่แยกกันสำหรับบัญชีธุรกรรมที่สำคัญที่สุดในช่วงของบัญชีผลรวม และเพิ่มจำนวนเงินงบประมาณที่พร้อมใช้ให้กับบัญชีผลรวมได้</span><span class="sxs-lookup"><span data-stu-id="514a6-119">Therefore, you can create separate budgets for the most significant transaction accounts in the interval of the total account, and then add the available budget amount to the total account.</span></span>





[!INCLUDE[footer-include](../../includes/footer-banner.md)]