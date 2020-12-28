---
title: ยืนยันการจัดส่งขาออกจากชุดงาน
description: หัวข้อนี้จะอธิบายวิธีการตั้งค่าชุดงานที่ยืนยันการจัดส่งสินค้าตามใบสั่งโอนย้ายขาออกโดยอัตโนมัติสำหรับโหลดงานที่พร้อมในการจัดส่ง
author: perlynne
manager: tfehr
ms.date: 07/31/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2020-07-31
ms.dyn365.ops.version: Release 10.0.13
ms.openlocfilehash: 41dbfb90b7b19c964e725ee0a4c769402414fb17
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 10/13/2020
ms.locfileid: "4438248"
---
# <a name="confirm-outbound-shipments-from-batch-jobs"></a><span data-ttu-id="6238e-103">ยืนยันการจัดส่งขาออกจากชุดงาน</span><span class="sxs-lookup"><span data-stu-id="6238e-103">Confirm outbound shipments from batch jobs</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="6238e-104">หัวข้อนี้จะอธิบายวิธีการตั้งค่าชุดงานที่ยืนยันการจัดส่งสินค้าตามใบสั่งโอนย้ายขาออกโดยอัตโนมัติสำหรับโหลดงานที่พร้อมในการจัดส่ง</span><span class="sxs-lookup"><span data-stu-id="6238e-104">This topic describes how to set up a batch job that automatically confirms outbound transfer-order shipments for ready-to-ship loads.</span></span> <span data-ttu-id="6238e-105">ชุดงานที่อธิบายไว้ที่นี่ใช้กับการจัดส่งตามใบสั่งโอนย้ายเท่านั้น ไม่ใช่สำหรับใบสั่งขาย</span><span class="sxs-lookup"><span data-stu-id="6238e-105">The batch job described here only applies to transfer order shipments, not to sales orders.</span></span>

## <a name="enable-the-confirm-outbound-shipments-from-batch-jobs-feature"></a><span data-ttu-id="6238e-106">เปิดใช้งานการยืนยันการจัดส่งขาออกจากคุณลักษณะชุดงาน</span><span class="sxs-lookup"><span data-stu-id="6238e-106">Enable the Confirm outbound shipments from batch jobs feature</span></span>

<span data-ttu-id="6238e-107">ก่อนที่คุณจะสามารถใช้คุณลักษณะนี้ได้ ต้องเปิดใช้งานในระบบของคุณ</span><span class="sxs-lookup"><span data-stu-id="6238e-107">Before you can use this feature, it must be enabled on your system.</span></span> <span data-ttu-id="6238e-108">ผู้ดูแลระบบสามารถใช้หน้า [การจัดการคุณลักษณะ](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) เพื่อตรวจสอบสถานะของคุณลักษณะ และเปิดใช้งานได้ ถ้าจำเป็น</span><span class="sxs-lookup"><span data-stu-id="6238e-108">Administrators can use the [Feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) page to check the feature status and enable it if needed.</span></span> <span data-ttu-id="6238e-109">คุณลักษณะนี้มีการลิสต์ไว้เป็น:</span><span class="sxs-lookup"><span data-stu-id="6238e-109">The feature is listed as:</span></span>

- <span data-ttu-id="6238e-110">**โมดูล** - *การจัดการคลังสินค้า*</span><span class="sxs-lookup"><span data-stu-id="6238e-110">**Module** - *Warehouse management*</span></span>
- <span data-ttu-id="6238e-111">**ชื่อคุณลักษณะ** - *ยืนยันการจัดส่งขาออกจากชุดงาน*</span><span class="sxs-lookup"><span data-stu-id="6238e-111">**Feature name** - *Confirm outbound shipments from batch jobs*</span></span>

## <a name="process-outbound-shipments"></a><span data-ttu-id="6238e-112">ประมวลผลการจัดส่งขาออก</span><span class="sxs-lookup"><span data-stu-id="6238e-112">Process outbound shipments</span></span>

<span data-ttu-id="6238e-113">เมื่อต้องการตั้งค่าชุดงานที่จัดกำหนดการไว้เพื่อรันการยืนยันการจัดส่งขาออกสำหรับการโหลดงานที่พร้อมในการจัดส่ง:</span><span class="sxs-lookup"><span data-stu-id="6238e-113">To set up a scheduled batch job to run the outbound shipment confirmation for loads that are ready to ship:</span></span>

1. <span data-ttu-id="6238e-114">ไปที่งานประจำงวด **การจัดการคลังสินค้า \> \>ประมวลผลการจัดส่งขาออก**</span><span class="sxs-lookup"><span data-stu-id="6238e-114">Go to **Warehouse management \> Periodic tasks \> Process outbound shipments**.</span></span>
1. <span data-ttu-id="6238e-115">กล่องโต้ตอบ **ยืนยันการจัดส่ง** จะเปิดขึ้น</span><span class="sxs-lookup"><span data-stu-id="6238e-115">The **Confirm shipment** dialog box opens.</span></span> <span data-ttu-id="6238e-116">บนแท็บด่วน **เรกคอร์ดที่จะรวม** ให้เลือก **ตัวกรองข้อมูล**</span><span class="sxs-lookup"><span data-stu-id="6238e-116">On the **Records to include** FastTab, select **Filter**.</span></span>
1. <span data-ttu-id="6238e-117">กล่องโต้ตอบตัวแก้ไขการสอบถามจะเปิดขึ้น</span><span class="sxs-lookup"><span data-stu-id="6238e-117">The query editor dialog box opens.</span></span> <span data-ttu-id="6238e-118">บนแท็บ **ช่วง** เพิ่มแถวที่มีค่าต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="6238e-118">On the **Range** tab, add a row with the following values:</span></span>
    - <span data-ttu-id="6238e-119">**ตาราง** - *โหลด*</span><span class="sxs-lookup"><span data-stu-id="6238e-119">**Table** - *Loads*</span></span>
    - <span data-ttu-id="6238e-120">**ตารางสืบทอด** - *โหลด*</span><span class="sxs-lookup"><span data-stu-id="6238e-120">**Derived table** - *Loads*</span></span>
    - <span data-ttu-id="6238e-121">**ฟิลด์** - *สถานะการโหลด*</span><span class="sxs-lookup"><span data-stu-id="6238e-121">**Field** - *Load status*</span></span>
    - <span data-ttu-id="6238e-122">**เงื่อนไข** - *โหลด*</span><span class="sxs-lookup"><span data-stu-id="6238e-122">**Criteria** - *Loaded*</span></span>
1. <span data-ttu-id="6238e-123">เลือก **ตกลง** เพื่อกลับไปที่กล่องโต้ตอบ **การยืนยันการจัดส่ง**</span><span class="sxs-lookup"><span data-stu-id="6238e-123">Select **OK** to return to the **Confirm shipment** dialog box.</span></span>
1. <span data-ttu-id="6238e-124">บนแท็บด่วน **การรันในส่วนเบื้องหลัง** ให้ตั้งค่า **การประมวลผลชุดงาน** เป็น **ใช่**</span><span class="sxs-lookup"><span data-stu-id="6238e-124">On the **Run in the background** FastTab, set **Batch processing** to **Yes**.</span></span>
1. <span data-ttu-id="6238e-125">บนแท็บด่วน **การรันในส่วนเบื้องหลัง** เลือก **การเกิดซ้ำ**</span><span class="sxs-lookup"><span data-stu-id="6238e-125">On the **Run in the background** FastTab, select **Recurrence**.</span></span>
1. <span data-ttu-id="6238e-126">กล่องโต้ตอบ **กำหนดการเกิดซ้ำ** จะเปิดขึ้น</span><span class="sxs-lookup"><span data-stu-id="6238e-126">The **Define recurrence** dialog box opens.</span></span> <span data-ttu-id="6238e-127">ตั้งค่ากำหนดการรันตามที่จำเป็นสำหรับธุรกิจของคุณ</span><span class="sxs-lookup"><span data-stu-id="6238e-127">Set the run schedule as needed for your business.</span></span>
1. <span data-ttu-id="6238e-128">เลือก **ตกลง** เพื่อกลับไปที่กล่องโต้ตอบ **การยืนยันการจัดส่ง**</span><span class="sxs-lookup"><span data-stu-id="6238e-128">Select **OK** to return to the **Confirm shipment** dialog box.</span></span>
1. <span data-ttu-id="6238e-129">เลือก **ตกลง** บนกล่องโต้ตอบ **ยืนยันการจัดส่ง** เพื่อเพิ่มชุดงานเข้าในคิวชุดงาน</span><span class="sxs-lookup"><span data-stu-id="6238e-129">Select **OK** on the **Confirm shipment** dialog box to add the batch job to the batch queue.</span></span>

<span data-ttu-id="6238e-130">สำหรับข้อมูลเพิ่มเติม ให้ดูที่ [ภาพรวมของการประมวลผลชุดงาน](../../fin-ops-core/dev-itpro/sysadmin/batch-processing-overview.md)</span><span class="sxs-lookup"><span data-stu-id="6238e-130">For more information, see [Batch processing overview](../../fin-ops-core/dev-itpro/sysadmin/batch-processing-overview.md).</span></span>
