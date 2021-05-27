---
title: ผู้ปฏิบัติงานที่รับผิดชอบการอนุมัติความไม่สอดคล้องกัน
description: หัวข้อนี้อธิบายวิธีการตั้งค่าคอนฟิกผู้ปฏิบัติงานที่รับผิดชอบการอนุมัติความไม่สอดคล้องกัน
author: rachel-profitt
ms.date: 03/23/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: InventTestTable
audience: Application User
ms.reviewer: kamaybac
ms.custom: 94003
ms.assetid: a1d9417b-268f-4334-8ab6-8499d6c3acf0
ms.search.region: Global
ms.search.industry: Distribution
ms.author: raprofit
ms.search.validFrom: 2020-06-17
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 2d3f647de2c188661c2c9c5f31e2642c3f8ca0b5
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 05/11/2021
ms.locfileid: "6021791"
---
# <a name="workers-responsible-for-approving-nonconformances"></a><span data-ttu-id="cd5f8-103">ผู้ปฏิบัติงานที่รับผิดชอบการอนุมัติความไม่สอดคล้องกัน</span><span class="sxs-lookup"><span data-stu-id="cd5f8-103">Workers responsible for approving nonconformances</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="cd5f8-104">หัวข้อนี้อธิบายวิธีการตั้งค่าคอนฟิกผู้ปฏิบัติงานที่รับผิดชอบการอนุมัติความไม่สอดคล้องกัน</span><span class="sxs-lookup"><span data-stu-id="cd5f8-104">This topic describes how to configure workers that are responsible for approving nonconformances.</span></span>

<span data-ttu-id="cd5f8-105">ความไม่สอดคล้องกันต้องอนุมัติก่อนที่ผู้ใช้จะสามารถเริ่มป้อนรายละเอียด เช่น การแก้ไขหรือการดําเนินงานได้</span><span class="sxs-lookup"><span data-stu-id="cd5f8-105">Nonconformances must be approved before users can start to enter details such as corrections or operations.</span></span> <span data-ttu-id="cd5f8-106">ก่อนที่ผู้ใช้จะสามารถอนุมัติหรือปฏิเสธความไม่สอดคล้องกันได้ รหัสผู้ใช้ต้องเชื่อมโยงกับเรกคอร์ดผู้ปฏิบัติงานก่อน</span><span class="sxs-lookup"><span data-stu-id="cd5f8-106">Before users can approve or reject nonconformances, their user ID (user record) must be linked to a worker record.</span></span> <span data-ttu-id="cd5f8-107">คุณสามารถเลือกตั้งค่าคอนฟิกผู้ปฏิบัติงานที่รับผิดชอบด้านคุณภาพ แล้วอนุญาตให้ผู้ปฏิบัติงานหนึ่งอนุมัติงานในนามของผู้ปฏิบัติงานคนอื่นได้</span><span class="sxs-lookup"><span data-stu-id="cd5f8-107">You can optionally configure workers that are responsible for quality and then allow one worker to approve work on behalf of another worker.</span></span>

## <a name="enable-a-user-for-nonconformance-processing"></a><span data-ttu-id="cd5f8-108">เปิดใช้งานผู้ใช้สำหรับการประมวลผลความไม่สอดคล้องกัน</span><span class="sxs-lookup"><span data-stu-id="cd5f8-108">Enable a user for nonconformance processing</span></span>

<span data-ttu-id="cd5f8-109">ก่อนที่ผู้ใช้จะสามารถอนุมัติหรือปฏิเสธความไม่สอดคล้องกันได้ คุณต้องเชื่อมโยงเรกคอร์ดกับเรกคอร์ดผู้ปฏิบัติงานก่อน</span><span class="sxs-lookup"><span data-stu-id="cd5f8-109">Before a user can approve or reject nonconformances, you must link their user record to a worker record.</span></span> <span data-ttu-id="cd5f8-110">จากนั้นจะสามารถตั้งค่าฟิลด์การอนุมัติโดยอัตโนมัติ และผู้ใช้สามารถกรอกข้อมูลในแผ่นเวลาโดยอัตโนมัติได้</span><span class="sxs-lookup"><span data-stu-id="cd5f8-110">The approval fields can then be automatically set, and the current user can be automatically filled in for the timesheet.</span></span> <span data-ttu-id="cd5f8-111">ก่อนที่ผู้ใช้สามารถใช้บันทึกเอกสาร คุณต้องเรียกใช้งานการจัดการเอกสารในตัวเลือกผู้ใช้</span><span class="sxs-lookup"><span data-stu-id="cd5f8-111">Before the user can use the document notes, you must activate document handling in their user options.</span></span>

1. <span data-ttu-id="cd5f8-112">ไปที่ **การจัดการระบบ \> ผู้ใช้ \> ผู้ใช้**</span><span class="sxs-lookup"><span data-stu-id="cd5f8-112">Go to **System administration \> Users \> Users**.</span></span>
1. <span data-ttu-id="cd5f8-113">ค้นหาและเปิดผู้ใช้ที่ควรจะสามารถอนุมัติหรือปฏิเสธความไม่สอดคล้องกัน</span><span class="sxs-lookup"><span data-stu-id="cd5f8-113">Find and open the user who should be able to approve or reject nonconformances.</span></span>
1. <span data-ttu-id="cd5f8-114">ตั้งค่าฟิลด์ **บุคคล** เป็นชื่อของผู้ปฏิบัติงานที่เกี่ยวข้องกับเรกคอร์ดผู้ใช้ปัจจุบัน</span><span class="sxs-lookup"><span data-stu-id="cd5f8-114">Set the **Person** field to the name of the worker that is related to the current user record.</span></span>
1. <span data-ttu-id="cd5f8-115">ในบานหน้าต่างการดำเนินการ เลือก **ตัวเลือกผู้ใช้**</span><span class="sxs-lookup"><span data-stu-id="cd5f8-115">On the Action Pane, select **User options**.</span></span>
1. <span data-ttu-id="cd5f8-116">ในหน้า **ตัวเลือก** ของเรกคอร์ดผู้ใช้ปัจจุบัน บนแท็บ **การกำหนดลักษณะ** ให้ตั้งค่าตัวเลือก **เปิดใช้งานการจัดการเอกสาร** เป็น *ใช่*</span><span class="sxs-lookup"><span data-stu-id="cd5f8-116">On the **Options** page for the current user record, on the **Preferences** tab, set the **Enable document handling** option to *Yes*.</span></span>
1. <span data-ttu-id="cd5f8-117">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="cd5f8-117">Close the pages.</span></span>

## <a name="define-workers-that-are-responsible-for-quality"></a><span data-ttu-id="cd5f8-118">กําหนดผู้ปฏิบัติงานที่รับผิดชอบด้านคุณภาพ</span><span class="sxs-lookup"><span data-stu-id="cd5f8-118">Define workers that are responsible for quality</span></span>

1. <span data-ttu-id="cd5f8-119">ไปที่ **การจัดการสินค้าคงคลัง \> การตั้งค่า \> การควบคุมคุณภาพ \> ผู้ปฏิบัติงานที่รับผิดชอบด้านคุณภาพ**</span><span class="sxs-lookup"><span data-stu-id="cd5f8-119">Go to **Inventory management \> Setup \> Quality control \> Workers responsible for quality**.</span></span>
2. <span data-ttu-id="cd5f8-120">บนบานหน้าต่างการดำเนินการ เลือก **สร้าง**</span><span class="sxs-lookup"><span data-stu-id="cd5f8-120">On the Action Pane, select **New**.</span></span>
3. <span data-ttu-id="cd5f8-121">ในฟิลด์ **ผู้ปฏิบัติงาน** ให้เลือกผู้ปฏิบัติงานที่ป้อนข้อมูลคุณภาพ</span><span class="sxs-lookup"><span data-stu-id="cd5f8-121">In the **Worker** field, select the worker that enters quality data.</span></span>
4. <span data-ttu-id="cd5f8-122">ในฟิลด์ **ผู้ปฏิบัติงานที่รับผิดชอบ** ให้เลือกผู้ปฏิบัติงานที่ผู้ปฏิบัติงานที่เลือกป้อนงานในนาม</span><span class="sxs-lookup"><span data-stu-id="cd5f8-122">In the **Worker responsible** field, select the worker that the selected worker enters work on behalf of.</span></span> <span data-ttu-id="cd5f8-123">เมื่อมีการสร้างและอัปพเดตความไม่สอดคล้องกัน ผู้ปฏิบัติงานนี้จะถูกป้อนโดยค่าเริ่มต้นในฟิลด์ **ผู้ปฏิบัติงาน**</span><span class="sxs-lookup"><span data-stu-id="cd5f8-123">When nonconformances are created and updated, this worker will be entered by default in **Worker** fields.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="cd5f8-124">ทรัพยากรเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="cd5f8-124">Additional resources</span></span>

- [<span data-ttu-id="cd5f8-125">ภาพรวมของการจัดการคุณภาพ</span><span class="sxs-lookup"><span data-stu-id="cd5f8-125">Quality management overview</span></span>](quality-management-processes.md)
- [<span data-ttu-id="cd5f8-126">เปิดใช้งานการจัดการคุณภาพและความไม่สอดคล้องกัน</span><span class="sxs-lookup"><span data-stu-id="cd5f8-126">Enable quality and nonconformance management</span></span>](enable-quality-management.md)
- [<span data-ttu-id="cd5f8-127">ค่าธรรมเนียมเกี่ยวกับคุณภาพ</span><span class="sxs-lookup"><span data-stu-id="cd5f8-127">Quality charges</span></span>](quality-charges.md)
- [<span data-ttu-id="cd5f8-128">โซนตรวจสอบสินค้าสำหรับความไม่สอดคล้องกัน</span><span class="sxs-lookup"><span data-stu-id="cd5f8-128">Quarantine zones for nonconformances</span></span>](quality-quarantine-zones.md)
- [<span data-ttu-id="cd5f8-129">ชนิดของการวินิจฉัยสำหรับความไม่สอดคล้องกัน</span><span class="sxs-lookup"><span data-stu-id="cd5f8-129">Diagnostic types for nonconformances</span></span>](quality-diagnostic-types.md)
- [<span data-ttu-id="cd5f8-130">ค่าธรรมเนียมคุณภาพสำหรับความไม่สอดคล้องกัน</span><span class="sxs-lookup"><span data-stu-id="cd5f8-130">Quality charges for nonconformances</span></span>](quality-charges.md)
- [<span data-ttu-id="cd5f8-131">การดำเนินงานสำหรับความไม่สอดคล้องกัน</span><span class="sxs-lookup"><span data-stu-id="cd5f8-131">Operations for nonconformances</span></span>](quality-operations.md)
- [<span data-ttu-id="cd5f8-132">การจัดการคุณภาพสำหรับกระบวนการคลังสินค้า</span><span class="sxs-lookup"><span data-stu-id="cd5f8-132">Quality management for warehouse processes</span></span>](quality-management-for-warehouses-processes.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
