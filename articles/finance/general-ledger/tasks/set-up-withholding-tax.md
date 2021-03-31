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
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 7ae7b13f743336e01f17248c8d6492b31e8044ef
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 02/15/2021
ms.locfileid: "5222322"
---
# <a name="set-up-withholding-tax"></a><span data-ttu-id="27e1e-103">ตั้งค่าภาษีหัก ณ ที่จ่าย</span><span class="sxs-lookup"><span data-stu-id="27e1e-103">Set up withholding tax</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="27e1e-104">หัวข้อนี้อธิบายวิธีการตั้งค่าภาษีหัก ณ ที่จ่าย</span><span class="sxs-lookup"><span data-stu-id="27e1e-104">This topic explains how to set up withholding tax.</span></span> <span data-ttu-id="27e1e-105">*ภาษีหัก ณ ที่จ่าย* คือภาษีสำหรับผู้จัดจำหน่ายที่ไม่ได้สร้างธุรกรรมภาษีขาย</span><span class="sxs-lookup"><span data-stu-id="27e1e-105">*Withholding tax* is a tax on vendors that does not create sales tax transactions.</span></span> <span data-ttu-id="27e1e-106">ภาษีหัก ณ ที่จ่ายที่มีการคำนวณจากการชำระเงินของผู้จัดจำหน่ายถือเป็นหนี้สิน </span><span class="sxs-lookup"><span data-stu-id="27e1e-106">Withholding tax that is calculated on vendor payments is a liability.</span></span> <span data-ttu-id="27e1e-107">ดังนั้น เฉพาะบัญชีงบดุลหรือบัญชีหนี้สินเท่านั้นที่เป็นบัญชีที่ใช้ได้สำหรับการลงบัญชีภาษีหัก ณ ที่จ่าย </span><span class="sxs-lookup"><span data-stu-id="27e1e-107">Therefore, only balance sheet accounts or liability accounts are valid accounts for posting withholding tax.</span></span> <span data-ttu-id="27e1e-108">คู่มืองานนี้แสดงวิธีการตั้งค่าภาษี ณ ที่จ่าย</span><span class="sxs-lookup"><span data-stu-id="27e1e-108">This task guide demonstrates how to set up withholding tax.</span></span>

1. <span data-ttu-id="27e1e-109">ไปที่ **บานหน้าต่างนำทาง > โมดูล > ภาษี > ภาษีทางอ้อม > ภาษีหัก ณ ที่จ่าย > รหัสภาษีหัก ณ ที่จ่าย**</span><span class="sxs-lookup"><span data-stu-id="27e1e-109">Go to **Navigation pane > Modules > Tax > Indirect taxes > Withholding tax > Withholding tax codes**.</span></span>
2. <span data-ttu-id="27e1e-110">เลือก **ใหม่**</span><span class="sxs-lookup"><span data-stu-id="27e1e-110">Select **New**.</span></span>
3. <span data-ttu-id="27e1e-111">ในฟิลด์ **รหัสภาษีหัก ณ ที่จ่าย** ให้พิมพ์ค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="27e1e-111">In the **Withholding tax code** field, type a value.</span></span>
4. <span data-ttu-id="27e1e-112">ในฟิลด์ **ชื่อของภาษีหัก ณ ที่จ่าย** ให้ป้อนชื่อของรหัสภาษีหัก ณ ที่จ่าย</span><span class="sxs-lookup"><span data-stu-id="27e1e-112">In the **Withholding tax name** field, enter the name of the withholding tax code.</span></span>
5. <span data-ttu-id="27e1e-113">ในฟิลด์ **บัญชีหลัก** ให้เลือกบัญชีหลักสำหรับการลงรายการบัญชีภาระภาษีหัก ณ ที่จ่าย</span><span class="sxs-lookup"><span data-stu-id="27e1e-113">In the **Main account** field, select the main account for posting the withholding tax liability.</span></span>
6. <span data-ttu-id="27e1e-114">เลือก **บันทึก**</span><span class="sxs-lookup"><span data-stu-id="27e1e-114">Select **Save**.</span></span>
7. <span data-ttu-id="27e1e-115">เลือก **ค่า** และทำเครื่องหมายเรกคอร์ดที่ต้องการในรายการ</span><span class="sxs-lookup"><span data-stu-id="27e1e-115">Select **Values** and mark the desired record in the list.</span></span>
8. <span data-ttu-id="27e1e-116">ในฟิลด์ **ค่า** ให้ป้อนเปอร์เซ็นต์ที่ใช้สำหรับการคำนวณภาษีหัก ณ ที่จ่าย</span><span class="sxs-lookup"><span data-stu-id="27e1e-116">In the **Value** field, enter a percentage used for the calculation of the withholding tax.</span></span>
9. <span data-ttu-id="27e1e-117">เลือก **บันทึก**</span><span class="sxs-lookup"><span data-stu-id="27e1e-117">Select **Save**.</span></span>
10. <span data-ttu-id="27e1e-118">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="27e1e-118">Close the page.</span></span>
11. <span data-ttu-id="27e1e-119">เลือก **บันทึก**</span><span class="sxs-lookup"><span data-stu-id="27e1e-119">Select **Save**.</span></span>
12. <span data-ttu-id="27e1e-120">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="27e1e-120">Close the page.</span></span>
13. <span data-ttu-id="27e1e-121">ไปที่ **บานหน้าต่างนำทาง > โมดูล > ภาษี > ภาษีทางอ้อม > ภาษีหัก ณ ที่จ่าย > กลุ่มรหัสภาษีหัก ณ ที่จ่าย**</span><span class="sxs-lookup"><span data-stu-id="27e1e-121">Go to **Navigation pane > Modules > Tax > Indirect taxes > Withholding tax > Withholding tax groups**.</span></span>
14. <span data-ttu-id="27e1e-122">เลือก **ใหม่**</span><span class="sxs-lookup"><span data-stu-id="27e1e-122">Select **New**.</span></span>
15. <span data-ttu-id="27e1e-123">ในฟิลด์ **กลุ่มภาษีหัก ณ ที่จ่าย** ให้ป้อนตัวระบุของกลุ่มภาษีหัก ณ ที่จ่าย</span><span class="sxs-lookup"><span data-stu-id="27e1e-123">In the **Withholding tax group** field, enter the identifier of the withholding tax group.</span></span>
16. <span data-ttu-id="27e1e-124">ในฟิลด์ **คำอธิบาย** ให้ป้อนชื่อของกลุ่มภาษีหัก ณ ที่จ่าย</span><span class="sxs-lookup"><span data-stu-id="27e1e-124">In the **Description** field, enter the name of the withholding tax group.</span></span>
17. <span data-ttu-id="27e1e-125">ในฟิลด์ **รหัสภาษีหัก ณ ที่จ่าย** ให้เลือกรหัสภาษีหัก ณ ที่จ่าย</span><span class="sxs-lookup"><span data-stu-id="27e1e-125">In the **Withholding tax code** field, select the withholding tax code.</span></span>
18. <span data-ttu-id="27e1e-126">เลือก **บันทึก**</span><span class="sxs-lookup"><span data-stu-id="27e1e-126">Select **Save**.</span></span>
19. <span data-ttu-id="27e1e-127">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="27e1e-127">Close the page.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]