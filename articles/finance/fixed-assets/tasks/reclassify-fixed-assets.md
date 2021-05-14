---
title: จัดประเภทสินทรัพย์ถาวรใหม่
description: เมื่อต้องการจัดประเภทสินทรัพย์ถาวรใหม่ คุณต้องโอนย้ายสินทรัพย์ถาวรนั้นไปยังกลุ่มสินทรัพย์ถาวร หรือกำหนดหมายเลขสินทรัพย์ถาวรใหม่ให้กับสินทรัพย์ถาวรนั้นในกลุ่มเดียวกัน
author: saraschi2
ms.date: 05/14/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: fbfb754459fad1f3b1509f4f9c65c20e0385b013
ms.sourcegitcommit: ab3f5d0da6eb0177bbad720e73c58926d686f168
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 04/26/2021
ms.locfileid: "5944726"
---
# <a name="reclassify-fixed-assets"></a><span data-ttu-id="d0743-103">จัดประเภทสินทรัพย์ถาวรใหม่</span><span class="sxs-lookup"><span data-stu-id="d0743-103">Reclassify fixed assets</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="d0743-104">เมื่อต้องการจัดประเภทสินทรัพย์ถาวรใหม่ คุณต้องโอนย้ายสินทรัพย์ถาวรนั้นไปยังกลุ่มสินทรัพย์ถาวร หรือกำหนดหมายเลขสินทรัพย์ถาวรใหม่ให้กับสินทรัพย์ถาวรนั้นในกลุ่มเดียวกัน</span><span class="sxs-lookup"><span data-stu-id="d0743-104">To reclassify a fixed asset, you must transfer it to a new fixed asset group or assign a new fixed asset number to it in the same group.</span></span> 

<span data-ttu-id="d0743-105">เมื่อมีการจัดประเภทสินทรัพย์ถาวรใหม่:</span><span class="sxs-lookup"><span data-stu-id="d0743-105">When a fixed asset is reclassified:</span></span>

- <span data-ttu-id="d0743-106">สมุดบัญชีทั้งหมดสำหรับสินทรัพย์ถาวรที่มีอยู่จะถูกสร้างขึ้นสำหรับสินทรัพย์ถาวรใหม่</span><span class="sxs-lookup"><span data-stu-id="d0743-106">All books for the existing fixed asset are created for the new fixed asset.</span></span> <span data-ttu-id="d0743-107">ข้อมูลใดๆ ที่มีการตั้งค่าไว้สำหรับสินทรัพย์ถาวรเดิมจะถูกคัดลอกไปยังสินทรัพย์ถาวรใหม่</span><span class="sxs-lookup"><span data-stu-id="d0743-107">Any information that was set up for the original fixed asset is copied to the new fixed asset.</span></span> <span data-ttu-id="d0743-108">สถานะของสมุดบัญชีสำหรับสินทรัพย์ถาวรเดิมคือ ปิด</span><span class="sxs-lookup"><span data-stu-id="d0743-108">The status of the books for the original fixed asset is Closed.</span></span> 

- <span data-ttu-id="d0743-109">สมุดบัญชีใหม่ของสินทรัพย์ถาวรใหม่ ประกอบด้วยวันที่ของการจัดประเภทใหม่ในฟิลด์ **วันที่ซื้อสินทรัพย์**</span><span class="sxs-lookup"><span data-stu-id="d0743-109">The new books for the new fixed asset contain the date of the reclassification in the **Acquisition date** field.</span></span> <span data-ttu-id="d0743-110">วันที่ในฟิลด์ **วันที่คำนวณค่าเสื่อมราคา** จะถูกคัดลอกจากข้อมูลสินทรัพย์เดิม</span><span class="sxs-lookup"><span data-stu-id="d0743-110">The date in the **Depreciation run date** field is copied from the original asset information.</span></span> <span data-ttu-id="d0743-111">ถ้าการคิดค่าเสื่อมราคาได้เริ่มขึ้นแล้ว ฟิลด์ **วันที่ที่มีการคิดค่าเสื่อมราคาครั้งล่าสุด** จะแสดงวันที่ของการจัดประเภทใหม่</span><span class="sxs-lookup"><span data-stu-id="d0743-111">If the depreciation has already started, the **Date when depreciation was last run** field displays the date of the reclassification.</span></span> 

- <span data-ttu-id="d0743-112">ธุรกรรมสินทรัพย์ถาวรที่มีอยู่สำหรับสินทรัพย์ถาวรเดิม จะถูกยกเลิกและสร้างขึ้นอีกครั้งสำหรับสินทรัพย์ถาวรใหม่</span><span class="sxs-lookup"><span data-stu-id="d0743-112">The existing fixed asset transactions for the original fixed asset are canceled and regenerated for the new fixed asset.</span></span>

- <span data-ttu-id="d0743-113">เมื่อสินทรัพย์ที่มีธุรกรรมการโอนย้ายมีการจัดประเภทใหม่แล้ว ระบบจะแสดงข้อความใน **ศูนย์การดำเนินการ** เพื่อบ่งชี้ว่าธุรกรรมการโอนย้ายไม่เสร็จสมบูรณ์ในระหว่างกระบวนการจัดประเภทใหม่</span><span class="sxs-lookup"><span data-stu-id="d0743-113">When an asset that has a transfer transaction has been reclassified, the system will display a message in the **Action center** to indicate that a transfer transaction wasn't completed during the reclassification process.</span></span> <span data-ttu-id="d0743-114">จําเป็นต้องกรอกข้อมูลธุรกรรมการโอนย้ายเพื่อย้ายธุรกรรมการจัดประเภทใหม่ที่มีอยู่ไปยังมิติทางการเงินที่เหมาะสม</span><span class="sxs-lookup"><span data-stu-id="d0743-114">It's necessary to complete a transfer transaction to move the existing reclassification transactions to the appropriate financial dimensions.</span></span> 

   <span data-ttu-id="d0743-115">ในระหว่างกระบวนการจัดประเภทใหม่ ระบบจะรันการขั้นตอนต่อไปนี้เพื่อจัดประเภทยอดดุลสินทรัพย์ใหม่จากสินทรัพย์เดิมไปยังสินทรัพย์ใหม่</span><span class="sxs-lookup"><span data-stu-id="d0743-115">During the reclassification process, the system runs the following actions to reclassify the asset balance from the original asset to the new asset.</span></span> 
   
   - <span data-ttu-id="d0743-116">กระบวนการจัดประเภทใหม่จะคัดลอกข้อมูลจากสมุดบัญชีสินทรัพย์ถาวรเดิมไปที่สมุดบัญชีสินทรัพย์ถาวรใหม่</span><span class="sxs-lookup"><span data-stu-id="d0743-116">The reclassification process copies the data from the original fixed asset book to the new fixed asset book.</span></span>

   - <span data-ttu-id="d0743-117">ธุรกรรมการจัดประเภทใหม่จะใช้ข้อมูลจากการซื้อสินทรัพย์ที่ลงรายการบัญชีเดิมที่รวมข้อมูลมิติทางการเงินที่รวมอยู่ในธุรกรรมการซื้อสินทรัพย์</span><span class="sxs-lookup"><span data-stu-id="d0743-117">The reclassification transaction uses information from the original posted acquisition that includes financial dimension information that is included in the acquisition transaction.</span></span>  
   
   - <span data-ttu-id="d0743-118">ในขณะเดียวกัน กระบวนการจัดประเภทใหม่จะกลับรายการธุรกรรมการซื้อสินทรัพย์และธุรกรรมการโอนย้ายสินทรัพย์เดิม</span><span class="sxs-lookup"><span data-stu-id="d0743-118">At the same time, the reclassification process reverses the original asset acquisition and asset transfer transaction.</span></span> 

<span data-ttu-id="d0743-119">แผนภาพและขั้นตอนต่อไปนี้แสดงตัวอย่างกระบวนการจัดประเภทใหม่</span><span class="sxs-lookup"><span data-stu-id="d0743-119">The following diagram and procedure provide an example of the reclassification process.</span></span> 

<span data-ttu-id="d0743-120">[![ไดอะแกรมที่แสดงกระบวนการจัดประเภทใหม่](../media/reclassification-process-01.png)](../media/reclassification-process-01.png)</span><span class="sxs-lookup"><span data-stu-id="d0743-120">[![Diagram showing the reclassicification process](../media/reclassification-process-01.png)](../media/reclassification-process-01.png)</span></span>

<span data-ttu-id="d0743-121">ทำตามขั้นตอนต่อไปนี้เพื่อจัดประเภทสินทรัพย์ถาวรใหม่:</span><span class="sxs-lookup"><span data-stu-id="d0743-121">Follow these steps to reclassify a fixed asset:</span></span>

1. <span data-ttu-id="d0743-122">ไปที่ **สินทรัพย์ถาวร > งานประจำงวด > การจัดประเภทใหม่**</span><span class="sxs-lookup"><span data-stu-id="d0743-122">Go to **Fixed assets > Periodic tasks > Reclassification.**</span></span>
2. <span data-ttu-id="d0743-123">ในฟิลด์ **กลุ่มสินทรัพย์ถาวร** ให้เลือกกลุ่มที่จะจัดประเภทใหม่</span><span class="sxs-lookup"><span data-stu-id="d0743-123">In the **Fixed asset group** field, select the group to reclassify.</span></span>
3. <span data-ttu-id="d0743-124">ในฟิลด์ **หมายเลขสินทรัพย์ถาวร** ให้เลือกสินทรัพย์ถาวรที่จะจัดประเภทใหม่</span><span class="sxs-lookup"><span data-stu-id="d0743-124">In the **Fixed asset number** field, select the fixed asset to reclassify.</span></span>
4. <span data-ttu-id="d0743-125">ในฟิลด์ **กลุ่มสินทรัพย์ถาวรใหม่** ให้เลือกกลุ่มที่จะโอนสินทรัพย์ถาวรไป</span><span class="sxs-lookup"><span data-stu-id="d0743-125">In the **New fixed asset group** field, select a group to transfer the fixed asset to.</span></span>
    * <span data-ttu-id="d0743-126">ถ้ากลุ่มสินทรัพย์ถาวรใหม่ถูกแนบกับลำดับหมายเลข ฟิลด์ **หมายเลขสินทรัพย์ถาวรใหม่** จะถูกอัพเดตด้วยหมายเลขจากลำดับหมายเลขของกลุ่มสินทรัพย์ถาวรใหม่</span><span class="sxs-lookup"><span data-stu-id="d0743-126">If the new fixed asset group is attached to a number sequence, the **New fixed asset number** field is updated with the number from the new fixed asset group number sequence.</span></span> <span data-ttu-id="d0743-127">มิฉะนั้น ฟิลด์ **หมายเลขสินทรัพย์ถาวรใหม่** จะถูกอัพเดตด้วยหมายเลขจากลำดับหมายเลขที่ตั้งค่าไว้ในหน้า **พารามิเตอร์สินทรัพย์ถาวร**</span><span class="sxs-lookup"><span data-stu-id="d0743-127">Otherwise, the **New fixed asset number** field is updated with the number from the number sequence that is set up on the **Fixed asset parameters** page.</span></span> <span data-ttu-id="d0743-128">ถ้าไม่มีการตั้งค่าลำดับหมายเลขไว้ในหน้า **พารามิเตอร์สินทรัพย์ถาวร** ให้ป้อนหมายเลขในฟิลด์ **หมายเลขสินทรัพย์ถาวรใหม่**</span><span class="sxs-lookup"><span data-stu-id="d0743-128">If a number sequence is not set up on the **Fixed asset parameters** page, enter a number in the **New fixed asset number** field.</span></span>  
5. <span data-ttu-id="d0743-129">ในฟิลด์ **วันที่จัดประเภทใหม่** ให้ป้อนวันที่</span><span class="sxs-lookup"><span data-stu-id="d0743-129">In the **Reclassification date** field, enter a date.</span></span>
6. <span data-ttu-id="d0743-130">ในฟิลด์ **ชุดใบสำคัญ** ให้ป้อนหรือเลือกค่า</span><span class="sxs-lookup"><span data-stu-id="d0743-130">In the **Voucher series** field, enter or select a value.</span></span>
7. <span data-ttu-id="d0743-131">เลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="d0743-131">Select **OK**.</span></span>


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
