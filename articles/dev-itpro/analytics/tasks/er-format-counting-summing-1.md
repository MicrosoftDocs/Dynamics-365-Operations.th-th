---
title: ER ตั้งค่าคอนฟิกรูปแบบเพื่อทำการตรวจนับและสรุป (ส่วนที่ 1 - สร้างรูปแบบ)
description: 'ขั้นตอนต่อไปนี้อธิบายวิธีกำหนดผู้ใช้ให้กับผู้ดูแลระบบหรือวิธีการที่บทบาทนักพัฒนาการรายงานทางอิเล็กทรอนิกส์สามารถตั้งค่าคอนฟิกรูปแบบการรายงานทางอิเล็กทรอนิกส์ (ER) เพื่อทำการตรวจนับและสรุปตามข้อมูลของผลลัพธ์ข้อความที่สร้างขึ้นแล้ว '
author: NickSelin
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ERWorkspace, ERVendorPart, ERSolutionRepositoryTable, ERSolutionRepositoryCreateDropDialog, ERSolutionImport,  ERSolutionTable
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: d1f925ef8d772189a505f2793de1176756866bf4
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 01/29/2019
ms.locfileid: "362268"
---
# <a name="er-configure-format-to-do-counting-and-summing-part-1-create-format"></a><span data-ttu-id="bed09-103">ER ตั้งค่าคอนฟิกรูปแบบเพื่อทำการตรวจนับและสรุป (ส่วนที่ 1: สร้างรูปแบบ)</span><span class="sxs-lookup"><span data-stu-id="bed09-103">ER Configure format to do counting and summing (Part 1: Create format)</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="bed09-104">ขั้นตอนต่อไปนี้อธิบายวิธีกำหนดผู้ใช้ให้กับผู้ดูแลระบบหรือวิธีการที่บทบาทนักพัฒนาการรายงานทางอิเล็กทรอนิกส์สามารถตั้งค่าคอนฟิกรูปแบบการรายงานทางอิเล็กทรอนิกส์ (ER) เพื่อทำการตรวจนับและสรุปตามข้อมูลของผลลัพธ์ข้อความที่สร้างขึ้นแล้ว </span><span class="sxs-lookup"><span data-stu-id="bed09-104">The following steps explain how a user assigned to the system administrator or electronic reporting developer role can configure an Electronic reporting (ER) format to do counting and summing based on data of the already generated text output.</span></span> <span data-ttu-id="bed09-105">สามารถดำเนินการขั้นตอนเหล่านี้ได้ในบริษัทใดก็ได้ </span><span class="sxs-lookup"><span data-stu-id="bed09-105">These steps can be performed in any company.</span></span>

<span data-ttu-id="bed09-106">เพื่อทำตามขั้นตอนเหล่านี้ อันดับแรกคุณต้องทำตามขั้นตอนในกระบวนงาน "สร้างผู้ให้บริการการตั้งค่าคอนฟิก และทำเครื่องหมายว่าใช้งานอยู่"</span><span class="sxs-lookup"><span data-stu-id="bed09-106">To complete these steps, you must first complete the steps in the “Create a configuration provider and mark it as active” procedure.</span></span>

<span data-ttu-id="bed09-107">กระบวนงานนี้ใช้สำหรับคุณลักษณะทั้ที่ถูกเพิ่มลงใน Dynamics 365 for Operations รุ่น 1611</span><span class="sxs-lookup"><span data-stu-id="bed09-107">This procedure is for a feature that was added in Dynamics 365 for Operations version 1611.</span></span>


## <a name="get-access-to-the-list-of-configurations-provided-by-microsoft"></a><span data-ttu-id="bed09-108">เข้าถึงรายการของการตั้งค่าคอนฟิกที่จัดเตรียมให้โดย Microsoft</span><span class="sxs-lookup"><span data-stu-id="bed09-108">Get access to the list of configurations provided by Microsoft</span></span>
1. <span data-ttu-id="bed09-109">ไปที่การจัดการองค์กร > พื้นที่ทำงาน > การรายงานทางอิเล็กทรอนิกส์</span><span class="sxs-lookup"><span data-stu-id="bed09-109">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
    * <span data-ttu-id="bed09-110">ตรวจสอบให้แน่ใจว่า "Litware, Inc."</span><span class="sxs-lookup"><span data-stu-id="bed09-110">Make sure that the “Litware, Inc.”</span></span> <span data-ttu-id="bed09-111">พร้อมใช้งานและทำเครื่องหมายไว้เป็น เปิดใช้งาน</span><span class="sxs-lookup"><span data-stu-id="bed09-111">provider is available and marked as active.</span></span>  
2. <span data-ttu-id="bed09-112">เลือก “Litware, Inc.“</span><span class="sxs-lookup"><span data-stu-id="bed09-112">Select the “Litware, Inc.”</span></span> <span data-ttu-id="bed09-113">ผู้ให้บริการ</span><span class="sxs-lookup"><span data-stu-id="bed09-113">provider.</span></span>
3. <span data-ttu-id="bed09-114">คลิก ที่เก็บ</span><span class="sxs-lookup"><span data-stu-id="bed09-114">Click Repositories.</span></span>
    * <span data-ttu-id="bed09-115">ถ้ามีที่เก็บชนิด "ทรัพยากรการดำเนินงาน" อยู่แล้ว ให้ข้ามขั้นตอนที่เหลือของงานย่อยปัจจุบัน</span><span class="sxs-lookup"><span data-stu-id="bed09-115">If a repository of the "Operations resources" type already exists, skip the remaining steps of the current sub-task.</span></span>  
4. <span data-ttu-id="bed09-116">คลิกเพิ่ม เพื่อเปิดกล่องโต้ตอบการวาง</span><span class="sxs-lookup"><span data-stu-id="bed09-116">Click Add to open the drop dialog.</span></span>
5. <span data-ttu-id="bed09-117">ในฟิลด์ชนิดที่เก็บของการตั้งค่าคอนฟิก ป้อน 'ทรัพยากรการดำเนินงาน'</span><span class="sxs-lookup"><span data-stu-id="bed09-117">In the Configuration repository type field, enter 'Operations resources'.</span></span>
6. <span data-ttu-id="bed09-118">คลิกสร้างที่จัดเก็บ</span><span class="sxs-lookup"><span data-stu-id="bed09-118">Click Create repository.</span></span>
7. <span data-ttu-id="bed09-119">คลิก ตกลง</span><span class="sxs-lookup"><span data-stu-id="bed09-119">Click OK.</span></span>

## <a name="get-the-intrastat-configurations-provided-by-microsoft"></a><span data-ttu-id="bed09-120">เรียกการตั้งค่าคอนฟิกอินทราสแทตที่จัดเตรียมให้โดย Microsoft</span><span class="sxs-lookup"><span data-stu-id="bed09-120">Get the Intrastat configurations provided by Microsoft</span></span>
1. <span data-ttu-id="bed09-121">คลิก เปิด</span><span class="sxs-lookup"><span data-stu-id="bed09-121">Click Open.</span></span>
2. <span data-ttu-id="bed09-122">ในแผนภูมิ เลือก 'Intrastat model\Intrastat (DE)'</span><span class="sxs-lookup"><span data-stu-id="bed09-122">In the tree, select 'Intrastat model\Intrastat (DE)'.</span></span>
3. <span data-ttu-id="bed09-123">คลิก นำเข้า</span><span class="sxs-lookup"><span data-stu-id="bed09-123">Click Import.</span></span>
    * <span data-ttu-id="bed09-124">คลิก นำเข้าสำหรับรุ่น 1.1 ของการจัดโครงแบบที่เลือก</span><span class="sxs-lookup"><span data-stu-id="bed09-124">Click Import for version 1.1 of the selected configuration.</span></span>  
4. <span data-ttu-id="bed09-125">คลิก ใช่</span><span class="sxs-lookup"><span data-stu-id="bed09-125">Click Yes.</span></span>
5. <span data-ttu-id="bed09-126">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="bed09-126">Close the page.</span></span>
6. <span data-ttu-id="bed09-127">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="bed09-127">Close the page.</span></span>
7. <span data-ttu-id="bed09-128">คลิก การตั้งค่าคอนฟิกการรายงาน</span><span class="sxs-lookup"><span data-stu-id="bed09-128">Click Reporting configurations.</span></span>
8. <span data-ttu-id="bed09-129">ในแผนภูมิ ขยาย 'Intrastat model'</span><span class="sxs-lookup"><span data-stu-id="bed09-129">In the tree, expand 'Intrastat model'.</span></span>
9. <span data-ttu-id="bed09-130">ในแผนภูมิ เลือก 'Intrastat model\Intrastat (DE)'</span><span class="sxs-lookup"><span data-stu-id="bed09-130">In the tree, select 'Intrastat model\Intrastat (DE)'.</span></span>

