---
title: ER ตั้งค่าคอนฟิกรูปแบบเพื่อทำการตรวจนับและสรุป (ส่วนที่ 1 - สร้างรูปแบบ)
description: หัวข้อนี้อธิบายวิธีการตั้งค่าคอนฟิกรูปแบบการรายงานทางอิเล็กทรอนิกส์ เพื่อตรวจนับและรวมตามข้อมูลของผลลัพธ์ข้อความที่สร้างขึ้นแล้ว (ส่วนที่ 1)
author: NickSelin
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: ERWorkspace, ERVendorPart, ERSolutionRepositoryTable, ERSolutionRepositoryCreateDropDialog, ERSolutionImport,  ERSolutionTable
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 3f1db144b2bfafa72abeaa92c6b21de717e4acbf
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 03/31/2021
ms.locfileid: "5749056"
---
# <a name="er-configure-format-to-do-counting-and-summing-part-1---create-format"></a><span data-ttu-id="d79fb-104">ER ตั้งค่าคอนฟิกรูปแบบเพื่อทำการตรวจนับและสรุป (ส่วนที่ 1 - สร้างรูปแบบ)</span><span class="sxs-lookup"><span data-stu-id="d79fb-104">ER Configure format to do counting and summing (Part 1 - Create format)</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="d79fb-105">ขั้นตอนต่อไปนี้อธิบายวิธีกำหนดผู้ใช้ให้กับผู้ดูแลระบบหรือวิธีการที่บทบาทนักพัฒนาการรายงานทางอิเล็กทรอนิกส์สามารถตั้งค่าคอนฟิกรูปแบบการรายงานทางอิเล็กทรอนิกส์ (ER) เพื่อทำการตรวจนับและสรุปตามข้อมูลของผลลัพธ์ข้อความที่สร้างขึ้นแล้ว </span><span class="sxs-lookup"><span data-stu-id="d79fb-105">The following steps explain how a user assigned to the system administrator or electronic reporting developer role can configure an Electronic reporting (ER) format to do counting and summing based on data of the already generated text output.</span></span> <span data-ttu-id="d79fb-106">สามารถดำเนินการขั้นตอนเหล่านี้ได้ในบริษัทใดก็ได้ </span><span class="sxs-lookup"><span data-stu-id="d79fb-106">These steps can be performed in any company.</span></span>

<span data-ttu-id="d79fb-107">เพื่อทำขั้นตอนเหล่านี้ให้เสร็จสมบูรณ์ อันดับแรกคุณต้องทำขั้นตอนต่างๆ ในกระบวนงาน "สร้างผู้ให้บริการการตั้งค่าคอนฟิก และทำเครื่องหมายเป็น ใช้งานอยู่" ให้เสร็จสมบูรณ์</span><span class="sxs-lookup"><span data-stu-id="d79fb-107">To complete these steps, you must first complete the steps in the "Create a configuration provider and mark it as active" procedure.</span></span>

<span data-ttu-id="d79fb-108">กระบวนงานนี้ใช้สำหรับคุณลักษณะทั้ที่ถูกเพิ่มลงใน Dynamics 365 for Operations รุ่น 1611</span><span class="sxs-lookup"><span data-stu-id="d79fb-108">This procedure is for a feature that was added in Dynamics 365 for Operations version 1611.</span></span>


## <a name="get-access-to-the-list-of-configurations-provided-by-microsoft"></a><span data-ttu-id="d79fb-109">เข้าถึงรายการของการตั้งค่าคอนฟิกที่จัดเตรียมให้โดย Microsoft</span><span class="sxs-lookup"><span data-stu-id="d79fb-109">Get access to the list of configurations provided by Microsoft</span></span>
1. <span data-ttu-id="d79fb-110">ไปที่การจัดการองค์กร > พื้นที่ทำงาน > การรายงานทางอิเล็กทรอนิกส์</span><span class="sxs-lookup"><span data-stu-id="d79fb-110">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
    * <span data-ttu-id="d79fb-111">ตรวจสอบให้แน่ใจว่า "Litware, Inc."</span><span class="sxs-lookup"><span data-stu-id="d79fb-111">Make sure that the "Litware, Inc."</span></span> <span data-ttu-id="d79fb-112">พร้อมใช้งานและทำเครื่องหมายไว้เป็น เปิดใช้งาน</span><span class="sxs-lookup"><span data-stu-id="d79fb-112">provider is available and marked as active.</span></span>  
2. <span data-ttu-id="d79fb-113">เลือก "Litware, Inc."</span><span class="sxs-lookup"><span data-stu-id="d79fb-113">Select the "Litware, Inc."</span></span> <span data-ttu-id="d79fb-114">ผู้ให้บริการ</span><span class="sxs-lookup"><span data-stu-id="d79fb-114">provider.</span></span>
3. <span data-ttu-id="d79fb-115">คลิก ที่เก็บ</span><span class="sxs-lookup"><span data-stu-id="d79fb-115">Click Repositories.</span></span>
    * <span data-ttu-id="d79fb-116">ถ้ามีที่เก็บชนิด "ทรัพยากรการดำเนินงาน" อยู่แล้ว ให้ข้ามขั้นตอนที่เหลือของงานย่อยปัจจุบัน</span><span class="sxs-lookup"><span data-stu-id="d79fb-116">If a repository of the "Operations resources" type already exists, skip the remaining steps of the current sub-task.</span></span>  
4. <span data-ttu-id="d79fb-117">คลิกเพิ่ม เพื่อเปิดกล่องโต้ตอบการวาง</span><span class="sxs-lookup"><span data-stu-id="d79fb-117">Click Add to open the drop dialog.</span></span>
5. <span data-ttu-id="d79fb-118">ในฟิลด์ชนิดที่เก็บของการตั้งค่าคอนฟิก ป้อน 'ทรัพยากรการดำเนินงาน'</span><span class="sxs-lookup"><span data-stu-id="d79fb-118">In the Configuration repository type field, enter 'Operations resources'.</span></span>
6. <span data-ttu-id="d79fb-119">คลิกสร้างที่จัดเก็บ</span><span class="sxs-lookup"><span data-stu-id="d79fb-119">Click Create repository.</span></span>
7. <span data-ttu-id="d79fb-120">คลิก ตกลง</span><span class="sxs-lookup"><span data-stu-id="d79fb-120">Click OK.</span></span>

## <a name="get-the-intrastat-configurations-provided-by-microsoft"></a><span data-ttu-id="d79fb-121">เรียกการตั้งค่าคอนฟิกอินทราสแทตที่จัดเตรียมให้โดย Microsoft</span><span class="sxs-lookup"><span data-stu-id="d79fb-121">Get the Intrastat configurations provided by Microsoft</span></span>
1. <span data-ttu-id="d79fb-122">คลิก เปิด</span><span class="sxs-lookup"><span data-stu-id="d79fb-122">Click Open.</span></span>
2. <span data-ttu-id="d79fb-123">ในแผนภูมิ เลือก 'Intrastat model\Intrastat (DE)'</span><span class="sxs-lookup"><span data-stu-id="d79fb-123">In the tree, select 'Intrastat model\Intrastat (DE)'.</span></span>
3. <span data-ttu-id="d79fb-124">คลิก นำเข้า</span><span class="sxs-lookup"><span data-stu-id="d79fb-124">Click Import.</span></span>
    * <span data-ttu-id="d79fb-125">คลิก นำเข้าสำหรับรุ่น 1.1 ของการจัดโครงแบบที่เลือก</span><span class="sxs-lookup"><span data-stu-id="d79fb-125">Click Import for version 1.1 of the selected configuration.</span></span>  
4. <span data-ttu-id="d79fb-126">คลิก ใช่</span><span class="sxs-lookup"><span data-stu-id="d79fb-126">Click Yes.</span></span>
5. <span data-ttu-id="d79fb-127">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="d79fb-127">Close the page.</span></span>
6. <span data-ttu-id="d79fb-128">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="d79fb-128">Close the page.</span></span>
7. <span data-ttu-id="d79fb-129">คลิก การตั้งค่าคอนฟิกการรายงาน</span><span class="sxs-lookup"><span data-stu-id="d79fb-129">Click Reporting configurations.</span></span>
8. <span data-ttu-id="d79fb-130">ในแผนภูมิ ขยาย 'Intrastat model'</span><span class="sxs-lookup"><span data-stu-id="d79fb-130">In the tree, expand 'Intrastat model'.</span></span>
9. <span data-ttu-id="d79fb-131">ในแผนภูมิ เลือก 'Intrastat model\Intrastat (DE)'</span><span class="sxs-lookup"><span data-stu-id="d79fb-131">In the tree, select 'Intrastat model\Intrastat (DE)'.</span></span>



[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]