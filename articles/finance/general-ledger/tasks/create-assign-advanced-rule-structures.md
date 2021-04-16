---
title: สร้างและกำหนดโครงสร้างกฎขั้นสูง
description: หัวข้อนี้อธิบายวิธีการสร้างและกำหนดโครงสร้างกฎขั้นสูงให้กับโครงสร้างทางบัญชี
author: aprilolson
ms.date: 07/19/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: DimensionConfigureAccountRuleStructure, DimensionCreateAccountRuleStructure, DimensionHierarchyAddLevel, DimensionHierarchyConstraintActivate, DimensionConfigureAccountStructure, DimensionConfigureAccountRule, DimensionCreateAccountRule, DimensionSelectAccountRuleStructure
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 4b81e3cc169bf0164af0b9c4de4faeb936df6784
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 04/01/2021
ms.locfileid: "5837068"
---
# <a name="create-and-assign-advanced-rule-structures"></a><span data-ttu-id="604f8-103">สร้างและกำหนดโครงสร้างกฎขั้นสูง</span><span class="sxs-lookup"><span data-stu-id="604f8-103">Create and assign advanced rule structures</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="604f8-104">หัวข้อนี้อธิบายวิธีการสร้างและกำหนดโครงสร้างกฎขั้นสูงให้กับโครงสร้างทางบัญชี</span><span class="sxs-lookup"><span data-stu-id="604f8-104">This topic explains how to create and assign an advanced rule structure to an account structure.</span></span> <span data-ttu-id="604f8-105">คำแนะนำนี้ใช้บริษัทสาธิต USMF</span><span class="sxs-lookup"><span data-stu-id="604f8-105">This guide uses the USMF demo company.</span></span>

## <a name="create-an-advanced-rule-structure"></a><span data-ttu-id="604f8-106">สร้างโครงสร้างกฎขั้นสูง</span><span class="sxs-lookup"><span data-stu-id="604f8-106">Create an advanced rule structure</span></span>
1. <span data-ttu-id="604f8-107">ไปที่ **บานหน้าต่างนำทาง > โมดูล > บัญชีแยกประเภททั่วไป > ผังบัญชี > โครงสร้าง > โครงสร้างกฎขั้นสูง**</span><span class="sxs-lookup"><span data-stu-id="604f8-107">Go to **Navigation pane > Modules > General ledger > Chart of accounts > Structures > Advanced rule structures**.</span></span>
2. <span data-ttu-id="604f8-108">เลือก **สร้าง** เพื่อเปิดกล่องโต้ตอบการวาง</span><span class="sxs-lookup"><span data-stu-id="604f8-108">Select **New** to open the drop dialog.</span></span>
3. <span data-ttu-id="604f8-109">ในฟิลด์ **โครงสร้างกฎขั้นสูง** ให้พิมพ์ชื่อเพื่ออธิบายโครงสร้างกฎ</span><span class="sxs-lookup"><span data-stu-id="604f8-109">In the **Advanced rule structure** field, type a name to describe the rule structure.</span></span>
4. <span data-ttu-id="604f8-110">เลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="604f8-110">Select **OK**.</span></span>
5. <span data-ttu-id="604f8-111">เลือก **เพิ่มเซ็กเมนต์**</span><span class="sxs-lookup"><span data-stu-id="604f8-111">Select **Add segment**.</span></span>
6. <span data-ttu-id="604f8-112">ในรายการเซ็กเมนต์ ให้เลือกมิติทางการเงิน</span><span class="sxs-lookup"><span data-stu-id="604f8-112">In the list of segments, select a financial dimension.</span></span> <span data-ttu-id="604f8-113">ตัวอย่างเช่น **ร้านค้า**</span><span class="sxs-lookup"><span data-stu-id="604f8-113">For example, **Store**.</span></span>  
7. <span data-ttu-id="604f8-114">เลือก **เพิ่มเซ็กเมนต์**</span><span class="sxs-lookup"><span data-stu-id="604f8-114">Select **Add segment**.</span></span>
8. <span data-ttu-id="604f8-115">เลือก **เปิดใช้งาน**</span><span class="sxs-lookup"><span data-stu-id="604f8-115">Select **Activate**.</span></span>

## <a name="apply-an-advanced-rule-structure-to-an-account-structure"></a><span data-ttu-id="604f8-116">ใช้โครงสร้างกฎขั้นสูงเพื่อโครงสร้างทางบัญชี</span><span class="sxs-lookup"><span data-stu-id="604f8-116">Apply an advanced rule structure to an account structure</span></span>
1. <span data-ttu-id="604f8-117">ไปที่ **บานหน้าต่างนำทาง > โมดูล > บัญชีแยกประเภททั่วไป > ผังบัญชี > โครงสร้าง > ตั้งค่าคอนฟิกโครงสร้างทางบัญชี**</span><span class="sxs-lookup"><span data-stu-id="604f8-117">Go to **navigation pane > Modules > General ledger > Chart of accounts > Structures > Configure account structures**.</span></span>
2. <span data-ttu-id="604f8-118">ในรายการ ให้ค้นหาและเลือกโครงสร้างทางบัญชีที่คุณต้องการนำกฎขั้นสูงไปใช้</span><span class="sxs-lookup"><span data-stu-id="604f8-118">In the list, find and select the account structure you want to apply the advanced rule to.</span></span>
3. <span data-ttu-id="604f8-119">เลือก **แก้ไข**</span><span class="sxs-lookup"><span data-stu-id="604f8-119">Select **Edit**.</span></span> <span data-ttu-id="604f8-120">นอกจากนี้ คุณสามารถเลือก **กฎขั้นสูง** และระบบจะขอให้คุณวางโครงสร้างทางบัญชีใน **โหมดแบบร่าง**</span><span class="sxs-lookup"><span data-stu-id="604f8-120">You can also select **Advanced rules** and you will be prompted to put the account structure in **Draft mode**.</span></span>  
4. <span data-ttu-id="604f8-121">เลือก **กฎขั้นสูง**</span><span class="sxs-lookup"><span data-stu-id="604f8-121">Select **Advanced rules**.</span></span>
5. <span data-ttu-id="604f8-122">เลือก **สร้าง** เพื่อเปิดกล่องโต้ตอบการวาง</span><span class="sxs-lookup"><span data-stu-id="604f8-122">Select **New** to open the drop dialog.</span></span>
6. <span data-ttu-id="604f8-123">ในฟิลด์ **กฎชั้นสูง** ให้พิมพ์ค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="604f8-123">In the **Advanced rule** field, type a value.</span></span>
7. <span data-ttu-id="604f8-124">ในฟิลด์ **ชื่อ** ให้พิมพ์ค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="604f8-124">In the **Name** field, type a value.</span></span>
8. <span data-ttu-id="604f8-125">เลือก **สร้าง**</span><span class="sxs-lookup"><span data-stu-id="604f8-125">Select **Create**.</span></span>
9. <span data-ttu-id="604f8-126">คลิก **เพิ่มเกณฑ์ใหม่**</span><span class="sxs-lookup"><span data-stu-id="604f8-126">Select **Add new criteria**.</span></span>
10. <span data-ttu-id="604f8-127">ในฟิลด์ **สถานที่** ให้เลือกบัญชีหลักหรือมิติทางการเงิน</span><span class="sxs-lookup"><span data-stu-id="604f8-127">In the **Where** field, select main account or a financial dimension.</span></span>
11. <span data-ttu-id="604f8-128">ในฟิลด์ **ผู้ปฏิบัติงาน** ให้เลือกตัวเลือก เช่น **อยู่ระหว่าง** และ **ประกอบด้วย**</span><span class="sxs-lookup"><span data-stu-id="604f8-128">In the **Operator** field, select an option, such as **is between** and **includes**.</span></span>
12. <span data-ttu-id="604f8-129">ในฟิลด์ **ค่า** ให้พิมพ์ค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="604f8-129">In the **Value** field, type a value.</span></span>
13. <span data-ttu-id="604f8-130">ในฟิลด์ **ผ่าน** ให้พิมพ์ค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="604f8-130">In the **through** field, type a value.</span></span>
14. <span data-ttu-id="604f8-131">เลือก **เพิ่ม** เพื่อเปิดกล่องโต้ตอบการวาง</span><span class="sxs-lookup"><span data-stu-id="604f8-131">Select **Add** to open the drop dialog.</span></span>
15. <span data-ttu-id="604f8-132">ในรายการ ให้ค้นหาโครงสร้างกฎขั้นสูงที่คุณต้องการใช้เมื่อคุณพบเงื่อนไขที่ป้อนเข้าไป</span><span class="sxs-lookup"><span data-stu-id="604f8-132">In the list, find the advanced rule structure you want to use when the criteria you entered is met.</span></span>
16. <span data-ttu-id="604f8-133">เลือก **เพิ่ม**</span><span class="sxs-lookup"><span data-stu-id="604f8-133">Select **Add**.</span></span>
17. <span data-ttu-id="604f8-134">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="604f8-134">Close the page.</span></span>
18. <span data-ttu-id="604f8-135">เลือก **เปิดใช้งาน**</span><span class="sxs-lookup"><span data-stu-id="604f8-135">Select **Activate**.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]