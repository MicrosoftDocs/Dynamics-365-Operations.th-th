--- 
title: "คำนวณค่าเสื่อมราคาสินทรัพย์ถาวรในนิติบุคคล"
description: "ใช้กระบวนงานนี้ในการเปลี่ยนกลุ่มสินทรัพย์ถาวรที่กำหนดให้กับสินทรัพย์ถาวร "
author: saraschi2
manager: AnnBe
ms.date: 10/11/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Operations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: f1e065ad8b18d6d0871f6127daec2d4f46f094e5
ms.contentlocale: th-th
ms.lasthandoff: 08/29/2017

---
# <a name="calculate-fixed-asset-depreciation-across-legal-entities"></a><span data-ttu-id="82ef6-103">คำนวณค่าเสื่อมราคาสินทรัพย์ถาวรในนิติบุคคล</span><span class="sxs-lookup"><span data-stu-id="82ef6-103">Calculate fixed asset depreciation across legal entities</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="82ef6-104">ใช้กระบวนงานนี้ในการเปลี่ยนกลุ่มสินทรัพย์ถาวรที่กำหนดให้กับสินทรัพย์ถาวร </span><span class="sxs-lookup"><span data-stu-id="82ef6-104">Use this procedure to change the fixed asset group that a fixed asset is assigned to.</span></span> <span data-ttu-id="82ef6-105">ควรจะกำหนดสินทรัพย์ถาวรในกลุ่มสินทรัพย์ถาวรที่ถูกต้อง </span><span class="sxs-lookup"><span data-stu-id="82ef6-105">Fixed assets should be assigned to the correct fixed asset group.</span></span> <span data-ttu-id="82ef6-106">กลุ่มสินทรัพย์ถาวรจะถูกนำไปใช้เมื่อคุณสร้างการสอบถามและรายงาน ตั้งค่าสินทรัพย์ถาวรใหม่ และรวมบัญชีแยกประเภทและลงรายการบัญชีธุรกรรมสินทรัพย์ถาวรกับบัญชีแยกประเภทที่เหมาะสม </span><span class="sxs-lookup"><span data-stu-id="82ef6-106">The fixed asset group is used when you create inquiries and reports, set up new fixed assets, and integrate ledgers and post fixed asset transactions to the appropriate ledger accounts.</span></span>

<span data-ttu-id="82ef6-107">การบันทึกข้อมูลนี้ใช้บริษัทสาธิต USMF</span><span class="sxs-lookup"><span data-stu-id="82ef6-107">This recording uses the USMF demo company.</span></span>

1. <span data-ttu-id="82ef6-108">ไปที่ สินทรัพย์ถาวร > สินทรัพย์ถาวร > สินทรัพย์ถาวร</span><span class="sxs-lookup"><span data-stu-id="82ef6-108">Go to Fixed assets > Fixed assets > Fixed assets.</span></span>
2. <span data-ttu-id="82ef6-109">เลือกสินทรัพย์ถาวรที่จะเปลี่ยนกลุ่มสินทรัพย์ถาวร</span><span class="sxs-lookup"><span data-stu-id="82ef6-109">Select the fixed asset to change the fixed asset group for.</span></span>
3. <span data-ttu-id="82ef6-110">คลิก เปลี่ยนกลุ่มสินทรัพย์ถาวร</span><span class="sxs-lookup"><span data-stu-id="82ef6-110">Click Change fixed asset group.</span></span>
4. <span data-ttu-id="82ef6-111">ในฟิลด์กลุ่มใหม่ ให้ป้อนหรือเลือกค่า</span><span class="sxs-lookup"><span data-stu-id="82ef6-111">In the New group field, enter or select a value.</span></span>
5. <span data-ttu-id="82ef6-112">ตั้งค่าตัวเลือกหมายเลขสินทรัพย์ถาวรใหม่เป็น ใช่ เพื่อกำหนดหมายเลขสินทรัพย์ถาวรให้กับสินทรัพย์ถาวรที่เลือก</span><span class="sxs-lookup"><span data-stu-id="82ef6-112">Set the New fixed asset number option to Yes to assign a fixed asset number to the selected fixed asset.</span></span>
    * <span data-ttu-id="82ef6-113">ฟิลด์หมายเลขสินทรัพย์ถาวรจะกลายเป็นพร้อมใช้งานเมื่อคุณตั้งค่าตัวเลือกหมายเลขสินทรัพย์ถาวรใหม่เป็น ใช่ </span><span class="sxs-lookup"><span data-stu-id="82ef6-113">The Fixed asset number field becomes available when the New fixed asset number option is set to Yes.</span></span>   <span data-ttu-id="82ef6-114">ถ้าการกำหนดหมายเลขอัตโนมัติถูกตั้งค่าสำหรับสินทรัพย์ถาวร ฟิลด์นี้จะแสดงหมายเลขสินทรัพย์ถาวรที่พร้อมใช้งานถัดไป </span><span class="sxs-lookup"><span data-stu-id="82ef6-114">If automatic numbering is set up for fixed assets, this field shows the next available fixed asset number.</span></span> <span data-ttu-id="82ef6-115">คุณสามารถเปลี่ยนหมายเลขได้ </span><span class="sxs-lookup"><span data-stu-id="82ef6-115">You can change the number.</span></span>   <span data-ttu-id="82ef6-116">ถ้ามีการตั้งค่าการกำหนดหมายเลขด้วยตนเองสำหรับสินทรัพย์ถาวร ฟิลด์นี้จะว่างและคุณต้องป้อนหมายเลขสินทรัพย์ถาวรใหม่</span><span class="sxs-lookup"><span data-stu-id="82ef6-116">If manual numbering is set up for fixed assets, this field is blank, and you must enter the new fixed asset number.</span></span>  
6. <span data-ttu-id="82ef6-117">คลิก ตกลง</span><span class="sxs-lookup"><span data-stu-id="82ef6-117">Click OK.</span></span>
7. <span data-ttu-id="82ef6-118">คลิก ใช่</span><span class="sxs-lookup"><span data-stu-id="82ef6-118">Click Yes.</span></span>


