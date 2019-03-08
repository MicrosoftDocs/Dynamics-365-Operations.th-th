---
title: การตั้งค่าการคิดค่าเสื่อมราคาพิเศษ
description: 'กระบวนงานนี้จะแสดงวิธีการสร้างการหักค่าเสื่อมราคาพิเศษและเชื่อมโยงกับสมุดบัญชีสินทรัพย์ถาวร '
author: saraschi2
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: AssetBonus, AssetGroup, AssetGroupBookSetup, AssetGroupSetupBonus
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 6bbd6b78d05fcc9d95f6e6409db2619a210ad760
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 01/29/2019
ms.locfileid: "339222"
---
# <a name="set-up-bonus-depreciation"></a><span data-ttu-id="a1556-103">การตั้งค่าการคิดค่าเสื่อมราคาพิเศษ</span><span class="sxs-lookup"><span data-stu-id="a1556-103">Set up bonus depreciation</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="a1556-104">กระบวนงานนี้จะแสดงวิธีการสร้างการหักค่าเสื่อมราคาพิเศษและเชื่อมโยงกับสมุดบัญชีสินทรัพย์ถาวร </span><span class="sxs-lookup"><span data-stu-id="a1556-104">This procedure shows how to create a special depreciation allowance and associate it with a fixed asset book.</span></span> <span data-ttu-id="a1556-105">ซึ่งจะใช้บทบาทของนักบัญชีและข้อมูลสาธิตสำหรับนิติบุคคล USMF</span><span class="sxs-lookup"><span data-stu-id="a1556-105">It uses the accountant role and demo data for the USMF legal entity.</span></span>


## <a name="create-a-special-depreciation-allowance"></a><span data-ttu-id="a1556-106">สร้างการหักค่าเสื่อมราคาพิเศษ</span><span class="sxs-lookup"><span data-stu-id="a1556-106">Create a special depreciation allowance</span></span>
1. <span data-ttu-id="a1556-107">ไปที่สินทรัพย์ถาวร > การติดตั้ง > การหักค่าเสื่อมราคาพิเศษ</span><span class="sxs-lookup"><span data-stu-id="a1556-107">Go to Fixed assets > Setup > Special depreciation allowance.</span></span>
2. <span data-ttu-id="a1556-108">คลิก สร้าง</span><span class="sxs-lookup"><span data-stu-id="a1556-108">Click New.</span></span>
3. <span data-ttu-id="a1556-109">ในฟิลด์โพรไฟล์การหักค่าเสื่อมราคาพิเศษ พิมพ์ค่า</span><span class="sxs-lookup"><span data-stu-id="a1556-109">In the Special depreciation allowance field, type a value.</span></span>
4. <span data-ttu-id="a1556-110">ในฟิลด์ คำอธิบาย ให้พิมพ์ค่า</span><span class="sxs-lookup"><span data-stu-id="a1556-110">In the Description field, type a value.</span></span>
5. <span data-ttu-id="a1556-111">ในฟิลด์เปอร์เซ็นทร์ ป้อนจำนวน</span><span class="sxs-lookup"><span data-stu-id="a1556-111">In the Percentage field, enter a number.</span></span>
    * <span data-ttu-id="a1556-112">ถ้าไม่ระบุเป็นเปอร์เซ็นต์ ให้ตั้งค่าเป็นจำนวนเงิน</span><span class="sxs-lookup"><span data-stu-id="a1556-112">If a percentage was not indicated, set an amount.</span></span>  

## <a name="associate-a-special-depreciation-allowance-with-a-fixed-asset-group-book"></a><span data-ttu-id="a1556-113">เชื่อมโยงการหักค่าเสื่อมราคาพิเศษกับสมุดบัญชีกลุ่มสินทรัพย์ถาวร</span><span class="sxs-lookup"><span data-stu-id="a1556-113">Associate a special depreciation allowance with a fixed asset group book</span></span>
1. <span data-ttu-id="a1556-114">ไปที่สินทรัพย์ถาวร > การติดตั้ง > กลุ่มสินทรัพย์ถาวร</span><span class="sxs-lookup"><span data-stu-id="a1556-114">Go to Fixed assets > Setup > Fixed asset groups.</span></span>
2. <span data-ttu-id="a1556-115">ในรายการ ให้เลือกสินทรัพย์ถาวรที่เกี่ยวข้องกับการหักค่าเสื่อมราคาพิเศษ</span><span class="sxs-lookup"><span data-stu-id="a1556-115">In the list, select the fixed asset group associated with the special depreciation allowance.</span></span>
3. <span data-ttu-id="a1556-116">คลิก สมุดบัญชี</span><span class="sxs-lookup"><span data-stu-id="a1556-116">Click Books.</span></span>
4. <span data-ttu-id="a1556-117">ในรายการ ให้เลือกสมุดบัญชีที่เกี่ยวข้องกับการหักค่าเสื่อมราคาพิเศษ</span><span class="sxs-lookup"><span data-stu-id="a1556-117">In the list, select the book that is associated with the special depreciation allowance.</span></span>
5. <span data-ttu-id="a1556-118">คลิกการหักค่าเสื่อมราคาพิเศษ</span><span class="sxs-lookup"><span data-stu-id="a1556-118">Click Special depreciation allowance.</span></span>
6. <span data-ttu-id="a1556-119">คลิก สร้าง</span><span class="sxs-lookup"><span data-stu-id="a1556-119">Click New.</span></span>
7. <span data-ttu-id="a1556-120">ในฟิลด์โพรไฟล์การหักค่าเสื่อมราคาพิเศษ ให้ป้อนหรือเลือกค่า</span><span class="sxs-lookup"><span data-stu-id="a1556-120">In the Special depreciation allowance field, enter or select a value.</span></span>
    * <span data-ttu-id="a1556-121">ค่าเริ่มต้นของเปอร์เซ็นต์หรือยอดเงินมาจากการตั้งค่าการหักค่าเสื่อมราคาพิเศษ</span><span class="sxs-lookup"><span data-stu-id="a1556-121">The default for Percentage or Amount comes from the special depreciation allowance setup.</span></span>  
8. <span data-ttu-id="a1556-122">ในฟิลด์ระดับความสำคัญ ให้ป้อนตัวเลข</span><span class="sxs-lookup"><span data-stu-id="a1556-122">In the Priority field, enter a number.</span></span>

