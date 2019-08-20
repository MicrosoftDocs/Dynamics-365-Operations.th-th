---
title: จัดประเภทสินทรัพย์ถาวรใหม่
description: เมื่อต้องการจัดประเภทสินทรัพย์ถาวรใหม่ คุณต้องโอนย้ายสินทรัพย์ถาวรนั้นไปยังกลุ่มสินทรัพย์ถาวร หรือกำหนดหมายเลขสินทรัพย์ถาวรใหม่ให้กับสินทรัพย์ถาวรนั้นในกลุ่มเดียวกัน
author: saraschi2
manager: AnnBe
ms.date: 05/14/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 47d8cf2ff1e275df0466a7fe327a3180c0399e49
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 08/01/2019
ms.locfileid: "1839940"
---
# <a name="reclassify-fixed-assets"></a><span data-ttu-id="93787-103">จัดประเภทสินทรัพย์ถาวรใหม่</span><span class="sxs-lookup"><span data-stu-id="93787-103">Reclassify fixed assets</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="93787-104">เมื่อต้องการจัดประเภทสินทรัพย์ถาวรใหม่ คุณต้องโอนย้ายสินทรัพย์ถาวรนั้นไปยังกลุ่มสินทรัพย์ถาวร หรือกำหนดหมายเลขสินทรัพย์ถาวรใหม่ให้กับสินทรัพย์ถาวรนั้นในกลุ่มเดียวกัน</span><span class="sxs-lookup"><span data-stu-id="93787-104">To reclassify a fixed asset, you must transfer it to a new fixed asset group or assign a new fixed asset number to it in the same group.</span></span> 

<span data-ttu-id="93787-105">เมื่อมีการจัดประเภทสินทรัพย์ถาวรใหม่:</span><span class="sxs-lookup"><span data-stu-id="93787-105">When a fixed asset is reclassified:</span></span>

<span data-ttu-id="93787-106">• สมุดบัญชีทั้งหมดสำหรับสินทรัพย์ถาวรที่มีอยู่ จะถูกสร้างขึ้นสำหรับสินทรัพย์ถาวรใหม่</span><span class="sxs-lookup"><span data-stu-id="93787-106">• All books for the existing fixed asset are created for the new fixed asset.</span></span> <span data-ttu-id="93787-107">ข้อมูลใดๆ ที่มีการตั้งค่าไว้สำหรับสินทรัพย์ถาวรเดิมจะถูกคัดลอกไปยังสินทรัพย์ถาวรใหม่</span><span class="sxs-lookup"><span data-stu-id="93787-107">Any information that was set up for the original fixed asset is copied to the new fixed asset.</span></span> <span data-ttu-id="93787-108">สถานะของสมุดบัญชีสำหรับสินทรัพย์ถาวรเดิมคือ ปิด</span><span class="sxs-lookup"><span data-stu-id="93787-108">The status of the books for the original fixed asset is Closed.</span></span> 

<span data-ttu-id="93787-109">• สมุดบัญชีใหม่ของสินทรัพย์ถาวรใหม่ ประกอบด้วยวันที่ของการจัดประเภทใหม่ในฟิลด์ **วันที่ซื้อสินทรัพย์**</span><span class="sxs-lookup"><span data-stu-id="93787-109">• The new books of the new fixed asset contain the date of the reclassification in the **Acquisition date** field.</span></span> <span data-ttu-id="93787-110">วันที่ในฟิลด์ **วันที่คำนวณค่าเสื่อมราคา** จะถูกคัดลอกจากข้อมูลสินทรัพย์เดิม</span><span class="sxs-lookup"><span data-stu-id="93787-110">The date in the **Depreciation run date** field is copied from the original asset information.</span></span> <span data-ttu-id="93787-111">ถ้าการคิดค่าเสื่อมราคาได้เริ่มขึ้นแล้ว ฟิลด์ **วันที่ที่มีการคิดค่าเสื่อมราคาครั้งล่าสุด** จะแสดงวันที่ของการจัดประเภทใหม่</span><span class="sxs-lookup"><span data-stu-id="93787-111">If the depreciation has already started, the **Date when depreciation was last run** field displays the date of the reclassification.</span></span> 

<span data-ttu-id="93787-112">• ธุรกรรมสินทรัพย์ถาวรที่มีอยู่สำหรับสินทรัพย์ถาวรเดิม จะถูกยกเลิกและสร้างขึ้นใหม่สำหรับสินทรัพย์ถาวรใหม่อีกครั้ง</span><span class="sxs-lookup"><span data-stu-id="93787-112">• The existing fixed asset transactions for the original fixed asset are canceled and regenerated for the new fixed asset.</span></span>

<span data-ttu-id="93787-113">ทำตามขั้นตอนต่อไปนี้เพื่อจัดประเภทสินทรัพย์ถาวรใหม่:</span><span class="sxs-lookup"><span data-stu-id="93787-113">Follow these steps to reclassify a fixed asset:</span></span>

1. <span data-ttu-id="93787-114">ไปที่ **สินทรัพย์ถาวร > งานประจำงวด > การจัดประเภทใหม่**</span><span class="sxs-lookup"><span data-stu-id="93787-114">Go to **Fixed assets > Periodic tasks > Reclassification.**</span></span>
2. <span data-ttu-id="93787-115">ในฟิลด์ **กลุ่มสินทรัพย์ถาวร** ให้เลือกกลุ่มที่จะจัดประเภทใหม่</span><span class="sxs-lookup"><span data-stu-id="93787-115">In the **Fixed asset group** field, select the group to reclassify.</span></span>
3. <span data-ttu-id="93787-116">ในฟิลด์ **หมายเลขสินทรัพย์ถาวร** ให้เลือกสินทรัพย์ถาวรที่จะจัดประเภทใหม่</span><span class="sxs-lookup"><span data-stu-id="93787-116">In the **Fixed asset number** field, select the fixed asset to reclassify.</span></span>
4. <span data-ttu-id="93787-117">ในฟิลด์ **กลุ่มสินทรัพย์ถาวรใหม่** ให้เลือกกลุ่มที่จะโอนสินทรัพย์ถาวรไป</span><span class="sxs-lookup"><span data-stu-id="93787-117">In the **New fixed asset group** field, select a group to transfer the fixed asset to.</span></span>
    * <span data-ttu-id="93787-118">ถ้ากลุ่มสินทรัพย์ถาวรใหม่ถูกแนบกับลำดับหมายเลข ฟิลด์ **หมายเลขสินทรัพย์ถาวรใหม่** จะถูกอัพเดตด้วยหมายเลขจากลำดับหมายเลขของกลุ่มสินทรัพย์ถาวรใหม่</span><span class="sxs-lookup"><span data-stu-id="93787-118">If the new fixed asset group is attached to a number sequence, the **New fixed asset number** field is updated with the number from the new fixed asset group number sequence.</span></span> <span data-ttu-id="93787-119">มิฉะนั้น ฟิลด์ **หมายเลขสินทรัพย์ถาวรใหม่** จะถูกอัพเดตด้วยหมายเลขจากลำดับหมายเลขที่ตั้งค่าไว้ในหน้า **พารามิเตอร์สินทรัพย์ถาวร**</span><span class="sxs-lookup"><span data-stu-id="93787-119">Otherwise, the **New fixed asset number** field is updated with the number from the number sequence that is set up on the **Fixed asset parameters** page.</span></span> <span data-ttu-id="93787-120">ถ้าไม่มีการตั้งค่าลำดับหมายเลขไว้ในหน้า **พารามิเตอร์สินทรัพย์ถาวร** ให้ป้อนหมายเลขในฟิลด์ **หมายเลขสินทรัพย์ถาวรใหม่**</span><span class="sxs-lookup"><span data-stu-id="93787-120">If a number sequence is not set up on the **Fixed asset parameters** page, enter a number in the **New fixed asset number** field.</span></span>  
5. <span data-ttu-id="93787-121">ในฟิลด์ **วันที่จัดประเภทใหม่** ให้ป้อนวันที่</span><span class="sxs-lookup"><span data-stu-id="93787-121">In the **Reclassification date** field, enter a date.</span></span>
6. <span data-ttu-id="93787-122">ในฟิลด์ **ชุดใบสำคัญ** ให้ป้อนหรือเลือกค่า</span><span class="sxs-lookup"><span data-stu-id="93787-122">In the **Voucher series** field, enter or select a value.</span></span>
7. <span data-ttu-id="93787-123">คลิก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="93787-123">Click **OK**.</span></span>
