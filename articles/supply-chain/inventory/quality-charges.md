---
title: ค่าธรรมเนียมสำหรับการดำเนินการความไม่สอดคล้องกัน
description: หัวข้อนี้จะอธิบายวิธีการสร้างค่าธรรมเนียมคุณภาพเพื่อให้สามารถใช้กับการดำเนินการสำหรับความไม่สอดคล้องกัน
author: rachel-profitt
ms.date: 03/23/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: InventTestMiscCharges
audience: Application User
ms.reviewer: kamaybac
ms.custom: 94003
ms.assetid: a1d9417b-268f-4334-8ab6-8499d6c3acf0
ms.search.region: Global
ms.search.industry: Distribution
ms.author: raprofit
ms.search.validFrom: 2020-06-17
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 382890232bff47a885840af1eb7e91d27bb46cae
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 05/11/2021
ms.locfileid: "6022311"
---
# <a name="charges-for-nonconformance-operations"></a><span data-ttu-id="68585-103">ค่าธรรมเนียมสำหรับการดำเนินการความไม่สอดคล้องกัน</span><span class="sxs-lookup"><span data-stu-id="68585-103">Charges for nonconformance operations</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="68585-104">หัวข้อนี้จะอธิบายวิธีการสร้างค่าธรรมเนียมคุณภาพเพื่อให้สามารถใช้กับการดำเนินการสำหรับความไม่สอดคล้องกัน</span><span class="sxs-lookup"><span data-stu-id="68585-104">This topic describes how to create quality charges that can be used with operations for a nonconformance.</span></span>

<span data-ttu-id="68585-105">คุณใช้หน้า **ค่าธรรมเนียมเกี่ยวกับคุณภาพ** เพื่อกำหนดชนิดของค่าธรรมเนียมที่จะถูกเพิ่มในการดำเนินการสำหรับความไม่สอดคล้อง</span><span class="sxs-lookup"><span data-stu-id="68585-105">You use the **Quality charges** page to define the types of charges that can be added to operations for a nonconformance.</span></span> <span data-ttu-id="68585-106">ค่าธรรมเนียมช่วยให้คุณสามารถติดตามรายละเอียดเกี่ยวกับค่าธรรมเนียมหรือค่าบริการที่คุณค้างส่งให้ลูกค้าทราบเกี่ยวกับผลิตภัณฑ์ที่ไม่สอดคล้องกัน หรือที่ผู้จัดจำหน่ายค้างส่งผลิตภัณฑ์ที่ไม่สอดคล้องกันที่คุณได้รับ</span><span class="sxs-lookup"><span data-stu-id="68585-106">Charges let you track details about fees or charges that you owe to a customer for nonconforming products, or that a vendor owes to you for nonconforming products that you received.</span></span> <span data-ttu-id="68585-107">คุณยังอาจใช้ค่าธรรมเนียมเพื่อติดตามต้นทุนที่ผู้จัดจำหน่ายหรือบริการภายนอกต้องใช้เพื่อดําเนินงาน</span><span class="sxs-lookup"><span data-stu-id="68585-107">You might also use charges to track costs that are required for external vendors or services to perform an operation.</span></span>

## <a name="examples-of-quality-charges"></a><span data-ttu-id="68585-108">ตัวอย่างของค่าธรรมเนียมคุณภาพ</span><span class="sxs-lookup"><span data-stu-id="68585-108">Examples of quality charges</span></span>

<span data-ttu-id="68585-109">คุณร่วมงานกับบริษัทผู้ผลิต</span><span class="sxs-lookup"><span data-stu-id="68585-109">You work for a manufacturing company.</span></span> <span data-ttu-id="68585-110">บริษัทของคุณมีสัญญากับผู้จัดจำหน่ายหลายราย</span><span class="sxs-lookup"><span data-stu-id="68585-110">Your company has contracts with several vendors.</span></span> <span data-ttu-id="68585-111">สัญญาดังกล่าวจะระบุมาตรฐานของการจัดส่งตรงเวลา ความเสียหาย และคุณภาพผลิตภัณฑ์ของสินค้า</span><span class="sxs-lookup"><span data-stu-id="68585-111">Those contracts outline standards for on-time shipment, damages, and product quality for items.</span></span> <span data-ttu-id="68585-112">ในทำนองเดียวกัน ลูกค้าหลายรายของคุณมีข้อตกลงกับบริษัทของคุณเกี่ยวกับการส่งคืน ความเสียหาย และคุณภาพผลิตภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="68585-112">Likewise, several of your customers have agreements with your company about returns, damages, and product quality.</span></span>

<span data-ttu-id="68585-113">โครงสร้างค่าธรรมเนียมจะถูกกําหนดให้กับแต่ละสถานการณ์และระบุไว้ในสัญญา</span><span class="sxs-lookup"><span data-stu-id="68585-113">A fee structure is defined for each circumstance and specified in the contract.</span></span> <span data-ttu-id="68585-114">คุณสามารถตั้งค่าคอนฟิกค่าธรรมเนียมคุณภาพเพื่อกําหนดโครงร่างค่าธรรมเนียมชนิดต่าง ๆ เช่น *ความเสียหาย* *การจัดส่งสินค้าล่าช้า* และ *คุณภาพ*</span><span class="sxs-lookup"><span data-stu-id="68585-114">You can configure quality charges to outline the various types of charges, such as *Damages*, *Late shipment*, and *Quality*.</span></span> <span data-ttu-id="68585-115">จากนั้นเมื่อคุณสร้างความไม่สอดคล้องกัน คุณจะเพิ่มการดําเนินงานหนึ่งอย่างหรือมากกว่า</span><span class="sxs-lookup"><span data-stu-id="68585-115">Then, when you create a nonconformance, you add one or more operations.</span></span> <span data-ttu-id="68585-116">สำหรับแต่ละการดำเนินการ คุณเลือก **ค่าธรรมเนียม** เพื่อกําหนดรายละเอียดเกี่ยวกับค่าธรรมเนียมได้</span><span class="sxs-lookup"><span data-stu-id="68585-116">For each operation, you select **Charges** to define the details about the fees.</span></span>

## <a name="create-a-quality-charge"></a><span data-ttu-id="68585-117">สร้างค่าธรรมเนียมคุณภาพ</span><span class="sxs-lookup"><span data-stu-id="68585-117">Create a quality charge</span></span>

1. <span data-ttu-id="68585-118">ไปที่ **การบริหารสินค้าคงคลัง \> การตั้งค่า \> การจัดการคุณภาพ \> ค่าธรรมเนียมเกี่ยวกับคุณภาพ**</span><span class="sxs-lookup"><span data-stu-id="68585-118">Go to **Inventory management \> Setup \> Quality management \> Quality charges**.</span></span>
1. <span data-ttu-id="68585-119">ในบานหน้าต่างการดำเนินการ ให้เลือก **สร้าง** เพื่อเพิ่มแถวไปยังกริด</span><span class="sxs-lookup"><span data-stu-id="68585-119">On the Action Pane, select **New** to add a row to the grid.</span></span> <span data-ttu-id="68585-120">จากนั้นให้กำหนดฟิลด์ดังต่อไปนี้สำหรับแถวใหม่:</span><span class="sxs-lookup"><span data-stu-id="68585-120">Then set the following fields for the new row:</span></span>

    - <span data-ttu-id="68585-121">**รหัสค่าธรรมเนียม** – ป้อนรหัสหรือชื่อเฉพาะของค่าธรรมเนียมคุณภาพ</span><span class="sxs-lookup"><span data-stu-id="68585-121">**Charges code** – Enter a unique ID or name for the quality charge.</span></span>
    - <span data-ttu-id="68585-122">**คำอธิบาย** – ป้อนคำอธิบายโดยละเอียดของค่าธรรมเนียมคุณภาพ</span><span class="sxs-lookup"><span data-stu-id="68585-122">**Description** – Enter a detailed description of the quality charge.</span></span>

1. <span data-ttu-id="68585-123">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="68585-123">Close the page.</span></span>

## <a name="add-a-quality-charge-to-an-operation-for-a-nonconformance"></a><span data-ttu-id="68585-124">เพิ่มค่าธรรมเนียมคุณภาพที่การดําเนินงานของความไม่สอดคล้องกัน</span><span class="sxs-lookup"><span data-stu-id="68585-124">Add a quality charge to an operation for a nonconformance</span></span>

<span data-ttu-id="68585-125">สำหรับรายละเอียดเกี่ยวกับวิธีการเพิ่มการดําเนินงานในความไม่สอดคล้องกันและใช้ค่าธรรมเนียม ดูที่ [การดำเนินงานสำหรับความไม่สอดคล้องกัน](quality-operations.md)</span><span class="sxs-lookup"><span data-stu-id="68585-125">For details about how to add operations to a nonconformance and apply charges to them, see [Operations for nonconformances](quality-operations.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="68585-126">ทรัพยากรเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="68585-126">Additional resources</span></span>

- [<span data-ttu-id="68585-127">ภาพรวมของการจัดการคุณภาพ</span><span class="sxs-lookup"><span data-stu-id="68585-127">Quality management overview</span></span>](quality-management-processes.md)
- [<span data-ttu-id="68585-128">เปิดใช้งานการจัดการคุณภาพและความไม่สอดคล้องกัน</span><span class="sxs-lookup"><span data-stu-id="68585-128">Enable quality and nonconformance management</span></span>](enable-quality-management.md)
- [<span data-ttu-id="68585-129">ผู้ปฏิบัติงานที่รับผิดชอบการอนุมัติความไม่สอดคล้องกัน</span><span class="sxs-lookup"><span data-stu-id="68585-129">Workers responsible for approving nonconformances</span></span>](quality-responsible-workers.md)
- [<span data-ttu-id="68585-130">โซนตรวจสอบสินค้าสำหรับความไม่สอดคล้องกัน</span><span class="sxs-lookup"><span data-stu-id="68585-130">Quarantine zones for nonconformances</span></span>](quality-quarantine-zones.md)
- [<span data-ttu-id="68585-131">ชนิดของการวินิจฉัยสำหรับความไม่สอดคล้องกัน</span><span class="sxs-lookup"><span data-stu-id="68585-131">Diagnostic types for nonconformances</span></span>](quality-diagnostic-types.md)
- [<span data-ttu-id="68585-132">ค่าธรรมเนียมคุณภาพสำหรับความไม่สอดคล้องกัน</span><span class="sxs-lookup"><span data-stu-id="68585-132">Quality charges for nonconformances</span></span>](quality-charges.md)
- [<span data-ttu-id="68585-133">การดำเนินงานสำหรับความไม่สอดคล้องกัน</span><span class="sxs-lookup"><span data-stu-id="68585-133">Operations for nonconformances</span></span>](quality-operations.md)
- [<span data-ttu-id="68585-134">การจัดการคุณภาพสำหรับกระบวนการคลังสินค้า</span><span class="sxs-lookup"><span data-stu-id="68585-134">Quality management for warehouse processes</span></span>](quality-management-for-warehouses-processes.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
