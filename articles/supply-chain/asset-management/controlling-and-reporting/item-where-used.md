---
title: สินค้าที่ใช้
description: หัวข้อนี้จะอธิบายถึงวิธีการเรียกดูภาพรวมของสถานที่ที่มีการใช้สินค้าในการจัดการสินทรัพย์
author: josaw1
manager: AnnBe
ms.date: 08/23/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 84ab803aedf5b803b6c5f39ff1907726335cb45d
ms.sourcegitcommit: 2292b54e2da96f71b59ec9ccf17cd32d3d1d8b21
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 08/23/2019
ms.locfileid: "1918337"
---
# <a name="item-where-used"></a><span data-ttu-id="fb9f4-103">สินค้าที่ใช้</span><span class="sxs-lookup"><span data-stu-id="fb9f4-103">Item where used</span></span>

[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]

<span data-ttu-id="fb9f4-104">คุณสามารถทำการคำนวณสำหรับสินค้าเฉพาะเพื่อดูภาพรวมของสถานที่ในการจัดการสินทรัพย์เมื่อสินค้าถูกใช้งานเเล้ว</span><span class="sxs-lookup"><span data-stu-id="fb9f4-104">You can make a calculation for a specific item to get an overview of where in Asset Management the item has been used.</span></span> <span data-ttu-id="fb9f4-105">ผลลัพธ์แสดงบริบทที่มีการใช้สินค้าในระหว่างอายุการใช้งาน</span><span class="sxs-lookup"><span data-stu-id="fb9f4-105">The results show the context in which the item has been used during its lifetime.</span></span> <span data-ttu-id="fb9f4-106">**สินค้า** ที่หน้าที่ใช้งานสามารถเปิดจากเมนูการจัดการสินทรัพย์หลัก เเละนอกจากนี้สามารถเข้าถึงหน้าต่อไปนี้ได้:</span><span class="sxs-lookup"><span data-stu-id="fb9f4-106">The **Item where used** page can be opened from the main Asset management menu, and it can also be accessed from the following pages:</span></span>

[<span data-ttu-id="fb9f4-107">BOM สินทรัพย์</span><span class="sxs-lookup"><span data-stu-id="fb9f4-107">Asset BOM</span></span>](../objects/object-BOM.md)

[<span data-ttu-id="fb9f4-108">อะไหล่สำรองในชนิดสินทรัพย์เริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="fb9f4-108">Spare parts on asset type defaults</span></span>](../setup-for-objects/object-types.md)

[<span data-ttu-id="fb9f4-109">การคาดการณ์สินค้าบนชนิดงานการบำรุงรักษาการคาดการณ์ค่าเริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="fb9f4-109">Item forecast on Maintenance job type defaults forecast</span></span>](../setup-for-work-orders/job-groups-and-job-types-variants-trades-and-checklists.md)

[<span data-ttu-id="fb9f4-110">การคาดการณ์ในการบำรุงรักษาของใบสั่งงาน</span><span class="sxs-lookup"><span data-stu-id="fb9f4-110">Work order maintenance forecast</span></span>](../work-orders/maintenance-forecasts.md)

[<span data-ttu-id="fb9f4-111">ใบขอซื้อของใบสั่งงาน</span><span class="sxs-lookup"><span data-stu-id="fb9f4-111">Work order purchase requisition</span></span>](../work-orders/procurement.md)

[<span data-ttu-id="fb9f4-112">การซื้อในใบสั่งงาน</span><span class="sxs-lookup"><span data-stu-id="fb9f4-112">Work order purchase</span></span>](../work-orders/procurement.md)

## <a name="make-an-item-where-used-calculation"></a><span data-ttu-id="fb9f4-113">สร้างสินค้าที่ใช้การคำนวณ</span><span class="sxs-lookup"><span data-stu-id="fb9f4-113">Make an item-where-used calculation</span></span>

1. <span data-ttu-id="fb9f4-114">คลิก **การจัดการสินค้า** > **การสอบถาม** > **สินค้าที่ใช้** หรือ เลือก **สินค้าที่ใช้** กับปุ่มบนหน้าใดหน้าหนึ่งที่กล่าวถึงข้างบน</span><span class="sxs-lookup"><span data-stu-id="fb9f4-114">Click **Asset management** > **Inquiries** > **Item where used**, or select the **Item where used** button on one of the pages mentioned above.</span></span>

2. <span data-ttu-id="fb9f4-115">ใน **สินค้าที่ใช้** กล่องโต้ตอบ เลือกสินค้าที่คุณต้องการทำการคำนวณในฟิลด์ **สินค้าหมายเลข**</span><span class="sxs-lookup"><span data-stu-id="fb9f4-115">In the **Item where used** dialog, select the item for which you want to make the calculation in the **Item number** field.</span></span>

3. <span data-ttu-id="fb9f4-116">คุณสามารถใช้ฟิลด์ **ระดับ** เพื่อระบุรายละเอียดที่คุณต้องการให้สินค้าเกี่ยวกับตำเเหน่งที่ทำงานมากเพียงใด</span><span class="sxs-lookup"><span data-stu-id="fb9f4-116">You can use the **Level** field to indicate how detailed you want the item lines to be regarding functional locations.</span></span> <span data-ttu-id="fb9f4-117">ตัวอย่างเช่น ถ้าคุณแทรกหมายเลข "1" ในฟิลด์ และคุณมีโครงสร้างสถานที่ทำงานหลายระดับรายการสินค้าทั้งหมดสำหรับสถานที่ทำงานจะแสดงอยู่ในระดับบนสุด</span><span class="sxs-lookup"><span data-stu-id="fb9f4-117">For example, if you insert the number "1" in the field, and you have a multi-level functional location structure, all item lines for a functional location will be shown on the top level.</span></span> <span data-ttu-id="fb9f4-118">ดังนั้น ความสัมพันธ์/ปริมาณในรายการอาจถูกเพิ่มขึ้นจากสถานที่ทำงานที่อยู่ในระดับที่ต่ำกว่า</span><span class="sxs-lookup"><span data-stu-id="fb9f4-118">Therefore, relation/quantity on a line may be added up from functional locations located at a lower level.</span></span> <span data-ttu-id="fb9f4-119">หากคุณแทรกหมายเลข "0" ในฟิลด์ **ระดับ** คุณจะเห็นผลลัพธ์โดยละเอียดแสดงรายการการสินค้าทั้งหมดบนระดับตำเเหน่งที่ทำงานทั้งหมดที่เกี่ยวข้อง</span><span class="sxs-lookup"><span data-stu-id="fb9f4-119">If you insert the number "0" in the **Level** field, you will see a detailed result showing all item lines on all the functional location levels to which they are related.</span></span>

4. <span data-ttu-id="fb9f4-120">ในส่วน **รวม** เลือก "ใช่" บนปุ่มสลับที่คุณต้องการรวมในการคำนวณ</span><span class="sxs-lookup"><span data-stu-id="fb9f4-120">In the **Include** section, select "Yes" on the toggle buttons that you want to include in the calculation.</span></span>

5. <span data-ttu-id="fb9f4-121">คลิก **ตกลง** เพื่อเริ่มต้นการคำนวณ</span><span class="sxs-lookup"><span data-stu-id="fb9f4-121">Click **OK** to start the calculation.</span></span>

6. <span data-ttu-id="fb9f4-122">บนเเท็บ **สินค้าที่ใช้** tab > **กลุ่มโดย...** บานหน้าต่างการดำเนินการ เลือกปุ่มที่เกี่ยวข้องเพื่อเเสดงระดับรายละเอียดที่จำเป็นของการคำนวณ</span><span class="sxs-lookup"><span data-stu-id="fb9f4-122">On the **Item where used** tab > **Group by...** action pane groups, select the relevant buttons to show the required detail level of the calculation.</span></span> <span data-ttu-id="fb9f4-123">ปุ่มบานหน้าต่างการดำเนินการที่เลือกจะถูกเน้น</span><span class="sxs-lookup"><span data-stu-id="fb9f4-123">The selected action pane buttons are highlighted.</span></span> <span data-ttu-id="fb9f4-124">คลิกบนปุ่มเพื่อเรียกใช้งานหรือยกเลิกการเรียกใช้งาน</span><span class="sxs-lookup"><span data-stu-id="fb9f4-124">Click on a button to activate or deactivate it.</span></span>

7. <span data-ttu-id="fb9f4-125">ถ้าคุณต้องการแสดงมิติที่เกี่ยวข้องกับสินค้า คลิก **เเสดงมิติ** และเลือกมิติที่จะแสดง</span><span class="sxs-lookup"><span data-stu-id="fb9f4-125">If you want to show dimensions related to the item, click **Display dimensions**, and select the dimensions to be shown.</span></span>

<span data-ttu-id="fb9f4-126">ในรูปด้านล่าง คุณจะเห็นตัวอย่างของการคำนวณสินค้าที่ใช้สำหรับหมายเลขสินค้า "1000"</span><span class="sxs-lookup"><span data-stu-id="fb9f4-126">In the figure below, you see an example of an item-where-used calculation for item number "1000".</span></span>

![รูปที่ 1](media/12-controlling-and-reporting.png)

