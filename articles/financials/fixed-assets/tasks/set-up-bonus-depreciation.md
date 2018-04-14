--- 
title: "การตั้งค่าการคิดค่าเสื่อมราคาพิเศษ"
description: "กระบวนงานนี้จะแสดงวิธีการสร้างการหักค่าเสื่อมราคาพิเศษและเชื่อมโยงกับสมุดบัญชีสินทรัพย์ถาวร "
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
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: 3d78be58ee678dbe7a5b5c8798e626125e6a0755
ms.contentlocale: th-th
ms.lasthandoff: 04/13/2018

---
# <a name="set-up-bonus-depreciation"></a><span data-ttu-id="f3436-103">การตั้งค่าการคิดค่าเสื่อมราคาพิเศษ</span><span class="sxs-lookup"><span data-stu-id="f3436-103">Set up bonus depreciation</span></span>

[!INCLUDE [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="f3436-104">กระบวนงานนี้จะแสดงวิธีการสร้างการหักค่าเสื่อมราคาพิเศษและเชื่อมโยงกับสมุดบัญชีสินทรัพย์ถาวร </span><span class="sxs-lookup"><span data-stu-id="f3436-104">This procedure shows how to create a special depreciation allowance and associate it with a fixed asset book.</span></span> <span data-ttu-id="f3436-105">ซึ่งจะใช้บทบาทของนักบัญชีและข้อมูลสาธิตสำหรับนิติบุคคล USMF</span><span class="sxs-lookup"><span data-stu-id="f3436-105">It uses the accountant role and demo data for the USMF legal entity.</span></span>


## <a name="create-a-special-depreciation-allowance"></a><span data-ttu-id="f3436-106">สร้างการหักค่าเสื่อมราคาพิเศษ</span><span class="sxs-lookup"><span data-stu-id="f3436-106">Create a special depreciation allowance</span></span>
1. <span data-ttu-id="f3436-107">ไปที่สินทรัพย์ถาวร > การติดตั้ง > การหักค่าเสื่อมราคาพิเศษ</span><span class="sxs-lookup"><span data-stu-id="f3436-107">Go to Fixed assets > Setup > Special depreciation allowance.</span></span>
2. <span data-ttu-id="f3436-108">คลิก สร้าง</span><span class="sxs-lookup"><span data-stu-id="f3436-108">Click New.</span></span>
3. <span data-ttu-id="f3436-109">ในฟิลด์โพรไฟล์การหักค่าเสื่อมราคาพิเศษ พิมพ์ค่า</span><span class="sxs-lookup"><span data-stu-id="f3436-109">In the Special depreciation allowance field, type a value.</span></span>
4. <span data-ttu-id="f3436-110">ในฟิลด์ คำอธิบาย ให้พิมพ์ค่า</span><span class="sxs-lookup"><span data-stu-id="f3436-110">In the Description field, type a value.</span></span>
5. <span data-ttu-id="f3436-111">ในฟิลด์เปอร์เซ็นทร์ ป้อนจำนวน</span><span class="sxs-lookup"><span data-stu-id="f3436-111">In the Percentage field, enter a number.</span></span>
    * <span data-ttu-id="f3436-112">ถ้าไม่ระบุเป็นเปอร์เซ็นต์ ให้ตั้งค่าเป็นจำนวนเงิน</span><span class="sxs-lookup"><span data-stu-id="f3436-112">If a percentage was not indicated, set an amount.</span></span>  

## <a name="associate-a-special-depreciation-allowance-with-a-fixed-asset-group-book"></a><span data-ttu-id="f3436-113">เชื่อมโยงการหักค่าเสื่อมราคาพิเศษกับสมุดบัญชีกลุ่มสินทรัพย์ถาวร</span><span class="sxs-lookup"><span data-stu-id="f3436-113">Associate a special depreciation allowance with a fixed asset group book</span></span>
1. <span data-ttu-id="f3436-114">ไปที่สินทรัพย์ถาวร > การติดตั้ง > กลุ่มสินทรัพย์ถาวร</span><span class="sxs-lookup"><span data-stu-id="f3436-114">Go to Fixed assets > Setup > Fixed asset groups.</span></span>
2. <span data-ttu-id="f3436-115">ในรายการ ให้เลือกสินทรัพย์ถาวรที่เกี่ยวข้องกับการหักค่าเสื่อมราคาพิเศษ</span><span class="sxs-lookup"><span data-stu-id="f3436-115">In the list, select the fixed asset group associated with the special depreciation allowance.</span></span>
3. <span data-ttu-id="f3436-116">คลิก สมุดบัญชี</span><span class="sxs-lookup"><span data-stu-id="f3436-116">Click Books.</span></span>
4. <span data-ttu-id="f3436-117">ในรายการ ให้เลือกสมุดบัญชีที่เกี่ยวข้องกับการหักค่าเสื่อมราคาพิเศษ</span><span class="sxs-lookup"><span data-stu-id="f3436-117">In the list, select the book that is associated with the special depreciation allowance.</span></span>
5. <span data-ttu-id="f3436-118">คลิกการหักค่าเสื่อมราคาพิเศษ</span><span class="sxs-lookup"><span data-stu-id="f3436-118">Click Special depreciation allowance.</span></span>
6. <span data-ttu-id="f3436-119">คลิก สร้าง</span><span class="sxs-lookup"><span data-stu-id="f3436-119">Click New.</span></span>
7. <span data-ttu-id="f3436-120">ในฟิลด์โพรไฟล์การหักค่าเสื่อมราคาพิเศษ ให้ป้อนหรือเลือกค่า</span><span class="sxs-lookup"><span data-stu-id="f3436-120">In the Special depreciation allowance field, enter or select a value.</span></span>
    * <span data-ttu-id="f3436-121">ค่าเริ่มต้นของเปอร์เซ็นต์หรือยอดเงินมาจากการตั้งค่าการหักค่าเสื่อมราคาพิเศษ</span><span class="sxs-lookup"><span data-stu-id="f3436-121">The default for Percentage or Amount comes from the special depreciation allowance setup.</span></span>  
8. <span data-ttu-id="f3436-122">ในฟิลด์ระดับความสำคัญ ให้ป้อนตัวเลข</span><span class="sxs-lookup"><span data-stu-id="f3436-122">In the Priority field, enter a number.</span></span>


