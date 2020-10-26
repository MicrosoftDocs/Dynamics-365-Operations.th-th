---
title: ตั้งค่าภาษีหัก ณ ที่จ่าย
description: หัวข้อนี้อธิบายวิธีการตั้งค่าภาษีหัก ณ ที่จ่าย
author: twheeloc
manager: AnnBe
ms.date: 07/11/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TaxWithholdTable, TaxWithholdData, TaxWithholdGroup
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: bfa1b9e43a5745eb5b5c442998597319f196f23f
ms.sourcegitcommit: 708ca25687a4e48271cdcd6d2d22d99fb94cf140
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 10/10/2020
ms.locfileid: "3976756"
---
# <a name="set-up-withholding-tax"></a><span data-ttu-id="07ad8-103">ตั้งค่าภาษีหัก ณ ที่จ่าย</span><span class="sxs-lookup"><span data-stu-id="07ad8-103">Set up withholding tax</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="07ad8-104">หัวข้อนี้อธิบายวิธีการตั้งค่าภาษีหัก ณ ที่จ่าย</span><span class="sxs-lookup"><span data-stu-id="07ad8-104">This topic explains how to set up withholding tax.</span></span> <span data-ttu-id="07ad8-105">*ภาษีหัก ณ ที่จ่าย* คือภาษีสำหรับผู้จัดจำหน่ายที่ไม่ได้สร้างธุรกรรมภาษีขาย</span><span class="sxs-lookup"><span data-stu-id="07ad8-105">*Withholding tax* is a tax on vendors that does not create sales tax transactions.</span></span> <span data-ttu-id="07ad8-106">ภาษีหัก ณ ที่จ่ายที่มีการคำนวณจากการชำระเงินของผู้จัดจำหน่ายถือเป็นหนี้สิน </span><span class="sxs-lookup"><span data-stu-id="07ad8-106">Withholding tax that is calculated on vendor payments is a liability.</span></span> <span data-ttu-id="07ad8-107">ดังนั้น เฉพาะบัญชีงบดุลหรือบัญชีหนี้สินเท่านั้นที่เป็นบัญชีที่ใช้ได้สำหรับการลงบัญชีภาษีหัก ณ ที่จ่าย </span><span class="sxs-lookup"><span data-stu-id="07ad8-107">Therefore, only balance sheet accounts or liability accounts are valid accounts for posting withholding tax.</span></span> <span data-ttu-id="07ad8-108">คู่มืองานนี้แสดงวิธีการตั้งค่าภาษี ณ ที่จ่าย</span><span class="sxs-lookup"><span data-stu-id="07ad8-108">This task guide demonstrates how to set up withholding tax.</span></span>

1. <span data-ttu-id="07ad8-109">ไปที่ **บานหน้าต่างนำทาง > โมดูล > ภาษี > ภาษีทางอ้อม > ภาษีหัก ณ ที่จ่าย > รหัสภาษีหัก ณ ที่จ่าย**</span><span class="sxs-lookup"><span data-stu-id="07ad8-109">Go to **Navigation pane > Modules > Tax > Indirect taxes > Withholding tax > Withholding tax codes**.</span></span>
2. <span data-ttu-id="07ad8-110">เลือก **ใหม่**</span><span class="sxs-lookup"><span data-stu-id="07ad8-110">Select **New**.</span></span>
3. <span data-ttu-id="07ad8-111">ในฟิลด์ **รหัสภาษีหัก ณ ที่จ่าย** ให้พิมพ์ค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="07ad8-111">In the **Withholding tax code** field, type a value.</span></span>
4. <span data-ttu-id="07ad8-112">ในฟิลด์ **ชื่อของภาษีหัก ณ ที่จ่าย** ให้ป้อนชื่อของรหัสภาษีหัก ณ ที่จ่าย</span><span class="sxs-lookup"><span data-stu-id="07ad8-112">In the **Withholding tax name** field, enter the name of the withholding tax code.</span></span>
5. <span data-ttu-id="07ad8-113">ในฟิลด์ **บัญชีหลัก** ให้เลือกบัญชีหลักสำหรับการลงรายการบัญชีภาระภาษีหัก ณ ที่จ่าย</span><span class="sxs-lookup"><span data-stu-id="07ad8-113">In the **Main account** field, select the main account for posting the withholding tax liability.</span></span>
6. <span data-ttu-id="07ad8-114">เลือก **บันทึก**</span><span class="sxs-lookup"><span data-stu-id="07ad8-114">Select **Save**.</span></span>
7. <span data-ttu-id="07ad8-115">เลือก **ค่า** และทำเครื่องหมายเรกคอร์ดที่ต้องการในรายการ</span><span class="sxs-lookup"><span data-stu-id="07ad8-115">Select **Values** and mark the desired record in the list.</span></span>
8. <span data-ttu-id="07ad8-116">ในฟิลด์ **ค่า** ให้ป้อนเปอร์เซ็นต์ที่ใช้สำหรับการคำนวณภาษีหัก ณ ที่จ่าย</span><span class="sxs-lookup"><span data-stu-id="07ad8-116">In the **Value** field, enter a percentage used for the calculation of the withholding tax.</span></span>
9. <span data-ttu-id="07ad8-117">เลือก **บันทึก**</span><span class="sxs-lookup"><span data-stu-id="07ad8-117">Select **Save**.</span></span>
10. <span data-ttu-id="07ad8-118">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="07ad8-118">Close the page.</span></span>
11. <span data-ttu-id="07ad8-119">เลือก **บันทึก**</span><span class="sxs-lookup"><span data-stu-id="07ad8-119">Select **Save**.</span></span>
12. <span data-ttu-id="07ad8-120">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="07ad8-120">Close the page.</span></span>
13. <span data-ttu-id="07ad8-121">ไปที่ **บานหน้าต่างนำทาง > โมดูล > ภาษี > ภาษีทางอ้อม > ภาษีหัก ณ ที่จ่าย > กลุ่มรหัสภาษีหัก ณ ที่จ่าย**</span><span class="sxs-lookup"><span data-stu-id="07ad8-121">Go to **Navigation pane > Modules > Tax > Indirect taxes > Withholding tax > Withholding tax groups**.</span></span>
14. <span data-ttu-id="07ad8-122">เลือก **ใหม่**</span><span class="sxs-lookup"><span data-stu-id="07ad8-122">Select **New**.</span></span>
15. <span data-ttu-id="07ad8-123">ในฟิลด์ **กลุ่มภาษีหัก ณ ที่จ่าย** ให้ป้อนตัวระบุของกลุ่มภาษีหัก ณ ที่จ่าย</span><span class="sxs-lookup"><span data-stu-id="07ad8-123">In the **Withholding tax group** field, enter the identifier of the withholding tax group.</span></span>
16. <span data-ttu-id="07ad8-124">ในฟิลด์ **คำอธิบาย** ให้ป้อนชื่อของกลุ่มภาษีหัก ณ ที่จ่าย</span><span class="sxs-lookup"><span data-stu-id="07ad8-124">In the **Description** field, enter the name of the withholding tax group.</span></span>
17. <span data-ttu-id="07ad8-125">ในฟิลด์ **รหัสภาษีหัก ณ ที่จ่าย** ให้เลือกรหัสภาษีหัก ณ ที่จ่าย</span><span class="sxs-lookup"><span data-stu-id="07ad8-125">In the **Withholding tax code** field, select the withholding tax code.</span></span>
18. <span data-ttu-id="07ad8-126">เลือก **บันทึก**</span><span class="sxs-lookup"><span data-stu-id="07ad8-126">Select **Save**.</span></span>
19. <span data-ttu-id="07ad8-127">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="07ad8-127">Close the page.</span></span>

