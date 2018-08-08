--- 
title: "จัดประเภทสินทรัพย์ถาวรใหม่"
description: "เมื่อต้องการจัดประเภทสินทรัพย์ถาวรใหม่ คุณต้องโอนย้ายสินทรัพย์ถาวรนั้นไปยังกลุ่มสินทรัพย์ถาวร หรือกำหนดหมายเลขสินทรัพย์ถาวรใหม่ให้กับสินทรัพย์ถาวรนั้นในกลุ่มเดียวกัน"
author: saraschi2
manager: AnnBe
ms.date: 10/30/2017
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 1d98cbff30620256c9d13e7b4a90314db150e33e
ms.openlocfilehash: d8e289e2c18fd28829fb4b749933ae1d84e0b631
ms.contentlocale: th-th
ms.lasthandoff: 08/07/2018

---
# <a name="reclassify-fixed-assets"></a><span data-ttu-id="f4b57-103">จัดประเภทสินทรัพย์ถาวรใหม่</span><span class="sxs-lookup"><span data-stu-id="f4b57-103">Reclassify fixed assets</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="f4b57-104">เมื่อต้องการจัดประเภทสินทรัพย์ถาวรใหม่ คุณต้องโอนย้ายสินทรัพย์ถาวรนั้นไปยังกลุ่มสินทรัพย์ถาวร หรือกำหนดหมายเลขสินทรัพย์ถาวรใหม่ให้กับสินทรัพย์ถาวรนั้นในกลุ่มเดียวกัน</span><span class="sxs-lookup"><span data-stu-id="f4b57-104">To reclassify a fixed asset, you must transfer it to a new fixed asset group or assign a new fixed asset number to it in the same group.</span></span> 

<span data-ttu-id="f4b57-105">เมื่อมีการจัดประเภทสินทรัพย์ถาวรใหม่:</span><span class="sxs-lookup"><span data-stu-id="f4b57-105">When a fixed asset is reclassified:</span></span>

<span data-ttu-id="f4b57-106">• รูปแบบมูลค่าทั้งหมดสำหรับสินทรัพย์ถาวรที่มีอยู่ จะถูกสร้างขึ้นสำหรับสินทรัพย์ถาวรใหม่</span><span class="sxs-lookup"><span data-stu-id="f4b57-106">• All value models for the existing fixed asset are created for the new fixed asset.</span></span> <span data-ttu-id="f4b57-107">ข้อมูลใดๆ ที่มีการตั้งค่าไว้สำหรับสินทรัพย์ถาวรเดิมจะถูกคัดลอกไปยังสินทรัพย์ถาวรใหม่</span><span class="sxs-lookup"><span data-stu-id="f4b57-107">Any information that was set up for the original fixed asset is copied to the new fixed asset.</span></span> <span data-ttu-id="f4b57-108">สถานะของแบบจำลองมูลค่าสำหรับสินทรัพย์ถาวรเดิมคือ ปิด</span><span class="sxs-lookup"><span data-stu-id="f4b57-108">The status of the value models for the original fixed asset is Closed.</span></span> 

<span data-ttu-id="f4b57-109">• แบบจำลองมูลค่าใหม่ของสินทรัพย์ถาวรใหม่ประกอบด้วยวันที่ของการจัดประเภทใหม่ในฟิลด์วันที่ซื้อสินทรัพย์</span><span class="sxs-lookup"><span data-stu-id="f4b57-109">• The new value models of the new fixed asset contain the date of the reclassification in the Acquisition date field.</span></span> <span data-ttu-id="f4b57-110">วันที่ในฟิลด์วันที่คำนวณค่าเสื่อมราคาจะถูกคัดลอกจากข้อมูลสินทรัพย์เดิม</span><span class="sxs-lookup"><span data-stu-id="f4b57-110">The date in the Depreciation run date field is copied from the original asset information.</span></span> <span data-ttu-id="f4b57-111">ถ้าการคิดค่าเสื่อมราคาได้เริ่มขึ้นแล้ว ฟิลด์วันที่ที่คิดค่าเสื่อมราคาครั้งล่าสุดจะแสดงวันที่ของการจัดประเภทใหม่</span><span class="sxs-lookup"><span data-stu-id="f4b57-111">If the depreciation has already started, the Date when depreciation was last run field displays the date of the reclassification.</span></span> 

<span data-ttu-id="f4b57-112">• ธุรกรรมสินทรัพย์ถาวรที่มีอยู่สำหรับสินทรัพย์ถาวรเดิม จะถูกยกเลิกและสร้างขึ้นใหม่สำหรับสินทรัพย์ถาวรใหม่อีกครั้ง</span><span class="sxs-lookup"><span data-stu-id="f4b57-112">• The existing fixed asset transactions for the original fixed asset are canceled and regenerated for the new fixed asset.</span></span>

1. <span data-ttu-id="f4b57-113">ไปที่ สินทรัพย์ถาวร > งานประจำงวด > การจัดประเภทใหม่</span><span class="sxs-lookup"><span data-stu-id="f4b57-113">Go to Fixed assets > Periodic tasks > Reclassification.</span></span>
2. <span data-ttu-id="f4b57-114">ในฟิลด์กลุ่มสินทรัพย์ถาวร ให้เลือกกลุ่มที่จะจัดประเภทใหม่</span><span class="sxs-lookup"><span data-stu-id="f4b57-114">In the Fixed asset group field, select the group to reclassify.</span></span>
3. <span data-ttu-id="f4b57-115">ในฟิลด์หมายเลขสินทรัพย์ถาวร ให้เลือกสินทรัพย์ถาวรที่จะจัดประเภทใหม่</span><span class="sxs-lookup"><span data-stu-id="f4b57-115">In the Fixed asset number field, select the fixed asset to reclassify.</span></span>
4. <span data-ttu-id="f4b57-116">ในฟิลด์กลุ่มสินทรัพย์ถาวรใหม่ ให้เลือกกลุ่มที่จะโอนสินทรัพย์ถาวร</span><span class="sxs-lookup"><span data-stu-id="f4b57-116">In the New fixed asset group field, select a group to transfer the fixed asset to.</span></span>
    * <span data-ttu-id="f4b57-117">ถ้ากลุ่มสินทรัพย์ถาวรใหม่แนบกับลำดับหมายเลข ฟิลด์หมายเลขสินทรัพย์ถาวรใหม่จะถูกอัพเดตด้วยหมายเลขจากลำดับหมายเลขของกลุ่มสินทรัพย์ถาวรใหม่</span><span class="sxs-lookup"><span data-stu-id="f4b57-117">If the new fixed asset group is attached to a number sequence, the New fixed asset number field is updated with the number from the new fixed asset group number sequence.</span></span> <span data-ttu-id="f4b57-118">มิฉะนั้น ฟิลด์หมายเลขสินทรัพย์ถาวรใหม่จะถูกอัพเดตด้วยหมายเลขจากลำดับหมายเลขที่ตั้งค่าไว้ในหน้าพารามิเตอร์สินทรัพย์ถาวร</span><span class="sxs-lookup"><span data-stu-id="f4b57-118">Otherwise, the New fixed asset number field is updated with the number from the number sequence that is set up in the Fixed asset parameters page.</span></span> <span data-ttu-id="f4b57-119">ถ้าไม่มีการตั้งค่าลำดับหมายเลขไว้ในหน้าพารามิเตอร์สินทรัพย์ถาวร ให้ป้อนหมายเลขในฟิลด์หมายเลขสินทรัพย์ถาวรใหม่</span><span class="sxs-lookup"><span data-stu-id="f4b57-119">If a number sequence is not set up in the Fixed asset parameters page, enter a number in the New fixed asset number field.</span></span>  
5. <span data-ttu-id="f4b57-120">ในฟิลด์วันที่จัดประเภทใหม่ ให้ป้อนวันที่</span><span class="sxs-lookup"><span data-stu-id="f4b57-120">In the Reclassification date field, enter a date.</span></span>
6. <span data-ttu-id="f4b57-121">ในฟิลด์ ชุดใบสำคัญ ให้ป้อนหรือเลือกค่า</span><span class="sxs-lookup"><span data-stu-id="f4b57-121">In the Voucher series field, enter or select a value.</span></span>
7. <span data-ttu-id="f4b57-122">คลิก ตกลง</span><span class="sxs-lookup"><span data-stu-id="f4b57-122">Click OK.</span></span>


