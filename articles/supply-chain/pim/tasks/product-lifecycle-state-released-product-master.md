---
title: มอบหมายสถานะรอบการขายของผลิตภัณฑ์ให้กับผลิตภัณฑ์หลักที่นำออกใช้
description: กระบวนงานนี้แสดงวิธีการกำหนดสถานะรอบการขายของผลิตภัณฑ์ให้กับผลิตภัณฑ์หลักที่นำออกใช้และตัวแปร
author: cvocph
manager: tfehr
ms.date: 12/05/2017
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Operations
ms.search.region: Global
ms.author: conradv
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: ab8c4e02a064fe84446fa54cc05b9a6a902c1860
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 04/02/2020
ms.locfileid: "3213158"
---
# <a name="assign-a-product-lifecycle-state-to-a-released-product-master"></a><span data-ttu-id="cb125-103">มอบหมายสถานะรอบการขายของผลิตภัณฑ์ให้กับผลิตภัณฑ์หลักที่นำออกใช้</span><span class="sxs-lookup"><span data-stu-id="cb125-103">Assign a product lifecycle state to a released product master</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="cb125-104">กระบวนงานนี้แสดงวิธีการกำหนดสถานะรอบการขายของผลิตภัณฑ์ให้กับผลิตภัณฑ์หลักที่นำออกใช้และตัวแปร</span><span class="sxs-lookup"><span data-stu-id="cb125-104">This procedure shows how to assign a product lifecycle state to a released product master and its variants.</span></span> <span data-ttu-id="cb125-105">ข้อกำหนดเบื้องต้น: คุณต้องเล่นคู่มืองาน "สร้างสถานะรอบการขายของผลิตภัณฑ์ใหม่" ก่อน เพื่อให้แน่ใจว่า คุณมีสถานะรอบการขายของผลิตภัณฑ์อย่างน้อยหนึ่งสถานะที่สร้างขึ้นก่อนที่คุณจะสามารถเล่นคู่มืองานนี้ได้</span><span class="sxs-lookup"><span data-stu-id="cb125-105">Prerequisite: You need to play the task guide "Create a new product lifecycle state" first to make sure that you have at least one product lifecycle state created before you can play this task guide.</span></span>


## <a name="find-a-released-product-master"></a><span data-ttu-id="cb125-106">ค้นหาผลิตภัณฑ์หลักที่นำออกใช้</span><span class="sxs-lookup"><span data-stu-id="cb125-106">Find a released product master</span></span>
1. <span data-ttu-id="cb125-107">ไปที่การจัดการข้อมูลผลิตภัณฑ์ > ผลิตภัณฑ์ > ผลิตภัณฑ์ที่นำออกใช้ </span><span class="sxs-lookup"><span data-stu-id="cb125-107">Go to Product information management > Products > Released products.</span></span>
2. <span data-ttu-id="cb125-108">ในรายการนี้ ให้ค้นหาและเลือกเรกคอร์ดที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="cb125-108">In the list, find and select the desired record.</span></span>

> [!NOTE]
> <span data-ttu-id="cb125-109">ผลิตภัณฑ์หลักมีผลิตภัณฑ์ที่เป็นชนิดย่อยของผลิตภัณฑ์หลัก</span><span class="sxs-lookup"><span data-stu-id="cb125-109">A product master has the Product subtype Product master.</span></span>  

## <a name="update-the-lifecycle-state"></a><span data-ttu-id="cb125-110">อัพเดตสถานะรอบการขาย</span><span class="sxs-lookup"><span data-stu-id="cb125-110">Update the lifecycle state</span></span>
1. <span data-ttu-id="cb125-111">คลิก แก้ไข</span><span class="sxs-lookup"><span data-stu-id="cb125-111">Click Edit.</span></span>
2. <span data-ttu-id="cb125-112">ในฟิลด์สถานะรอบการขายของผลิตภัณฑ์ ให้ป้อนหรือเลือกค่า</span><span class="sxs-lookup"><span data-stu-id="cb125-112">In the Product lifecycle state field, enter or select a value.</span></span>
3. <span data-ttu-id="cb125-113">คลิก บันทึก</span><span class="sxs-lookup"><span data-stu-id="cb125-113">Click Save.</span></span>
4. <span data-ttu-id="cb125-114">คลิก ใช่</span><span class="sxs-lookup"><span data-stu-id="cb125-114">Click Yes.</span></span>

> [!NOTE]
> <span data-ttu-id="cb125-115">ถ้ามีการเลือก ใช่ ผลิตภัณฑ์ย่อยที่นำออกใช้ซึ่งเกี่ยวข้องทั้งหมดที่มีสถานะเป็นต้นฉบับเดียวกันกับผลิตภัณฑ์หลักที่นำออกใช้ จะถูกปรับปรุงเป็นสถานะรอบการขายของผลิตภัณฑ์ใหม่อีกด้วย</span><span class="sxs-lookup"><span data-stu-id="cb125-115">If Yes is selected, all the related released product variants that have the same original status as the released product master are also updated to the new product lifecycle state.</span></span> <span data-ttu-id="cb125-116">ถ้ามีการเลือก ไม่ ผลิตภัณฑ์ย่อยทั้งหมดจะรักษาสถานะที่แท้จริง</span><span class="sxs-lookup"><span data-stu-id="cb125-116">If No is selected, all variants keep their actual state.</span></span> <span data-ttu-id="cb125-117">ไม่มีการอัพเดตผลิตภัณฑ์ย่อยที่มีสถานะรอบการขายของผลิตภัณฑ์ที่แตกต่างจากข้อมูลหลักของผลิตภัณฑ์ที่นำออกใช้</span><span class="sxs-lookup"><span data-stu-id="cb125-117">Variants that have a different product lifecycle state from the released product master are not updated.</span></span>  

## <a name="verify-the-lifecycle-state-of-the-variants"></a><span data-ttu-id="cb125-118">ตรวจสอบสถานะรอบการขายของผลิตภัณฑ์ย่อย</span><span class="sxs-lookup"><span data-stu-id="cb125-118">Verify the lifecycle state of the variants</span></span>
1. <span data-ttu-id="cb125-119">คลิก ผลิตภัณฑ์ย่อยที่นำออกใช้</span><span class="sxs-lookup"><span data-stu-id="cb125-119">Click Released product variants.</span></span>

> [!NOTE]
> <span data-ttu-id="cb125-120">โปรดทราบว่า ผลิตภัณฑ์ย่อยทั้งหมดมีการสืบทอดสถานะรอบการขายที่เลือกจากข้อมูลหลักของผลิตภัณฑ์ที่นำออกใช้</span><span class="sxs-lookup"><span data-stu-id="cb125-120">Note that all variants have inherited the selected lifecycle state from the released product master.</span></span>  

2. <span data-ttu-id="cb125-121">ในรายการนี้ ให้ทำเครื่องหมายแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="cb125-121">In the list, mark the selected row.</span></span>
3. <span data-ttu-id="cb125-122">ในฟิลด์สถานะรอบการขายของผลิตภัณฑ์ ให้ป้อนหรือเลือกค่า</span><span class="sxs-lookup"><span data-stu-id="cb125-122">In the Product lifecycle state field, enter or select a value.</span></span>

