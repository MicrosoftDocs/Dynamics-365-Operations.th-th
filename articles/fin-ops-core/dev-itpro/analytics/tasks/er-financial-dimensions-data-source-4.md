---
title: ER ใช้มิติทางการเงินเป็นแหล่งข้อมูล (ส่วนที่ 4 - รันรายงาน)
description: 'ขั้นตอนต่อไปนี้อธิบายวิธีการที่ผู้ใช้ที่ถูกกำหนดบทบาทผู้ดูแลระบบหรือนักพัฒนาการรายงานทางอิเล็กทรอนิกส์สามารถตั้งค่าคอนฟิกแบบจำลองการรายงานทางอิเล็กทรอนิกส์ (ER) (ER) เพื่อใช้มิติทางการเงินเป็นแหล่งข้อมูลสำหรับรายงาน ER '
author: NickSelin
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ERSolutionTable, SysQueryForm
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 7ae9f72df5d6ff6add4eb97836cf32509aebd511
ms.sourcegitcommit: 57e1dafa186fec77ddd8ba9425d238e36e0f0998
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 03/18/2020
ms.locfileid: "3141982"
---
# <a name="er-use-financial-dimensions-as-a-data-source-part-4---run-the-report"></a><span data-ttu-id="71d6e-103">ER ใช้มิติทางการเงินเป็นแหล่งข้อมูล (ส่วนที่ 4 - รันรายงาน)</span><span class="sxs-lookup"><span data-stu-id="71d6e-103">ER Use financial dimensions as a data source (Part 4 - Run the report)</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="71d6e-104">ขั้นตอนต่อไปนี้อธิบายวิธีการที่ผู้ใช้ที่ถูกกำหนดบทบาทผู้ดูแลระบบหรือนักพัฒนาการรายงานทางอิเล็กทรอนิกส์สามารถตั้งค่าคอนฟิกแบบจำลองการรายงานทางอิเล็กทรอนิกส์ (ER) (ER) เพื่อใช้มิติทางการเงินเป็นแหล่งข้อมูลสำหรับรายงาน ER </span><span class="sxs-lookup"><span data-stu-id="71d6e-104">The following steps explain how a user assigned to the system administrator or electronic reporting developer role can configure an Electronic reporting (ER) model to use financial dimensions as a data source for ER reports.</span></span> <span data-ttu-id="71d6e-105">สามารถดำเนินการขั้นตอนเหล่านี้ได้ในบริษัท DEMF </span><span class="sxs-lookup"><span data-stu-id="71d6e-105">These steps can be performed in the DEMF company.</span></span>

<span data-ttu-id="71d6e-106">เพื่อทำขั้นตอนเหล่านี้ให้เสร็จสมบูรณ์ อันดับแรกคุณต้องทำขั้นตอนต่างๆ ในกระบวนงาน "ER ใช้มิติทางการเงินเป็นแหล่งข้อมูล (ส่วนที่ 3: ออกแบบรายงาน)" ให้เสร็จสมบูรณ์</span><span class="sxs-lookup"><span data-stu-id="71d6e-106">To complete these steps, you must first complete the steps in the "ER Use financial dimensions as a data source (Part 3: Design the report)" procedure.</span></span> <span data-ttu-id="71d6e-107">นอกจากนี้คุณยังต้องตั้งค่าคอนฟิกชนิดเอกสารเริ่มต้นบนหน้าพารามิเตอร์การรายงานทางอิเล็กทรอนิกส์ </span><span class="sxs-lookup"><span data-stu-id="71d6e-107">You must also configure default document types on the Electronic reporting parameters page.</span></span> <span data-ttu-id="71d6e-108">ชนิดเอกสารเริ่มต้นจะถูกตั้งค่าเมื่อคุณดาวน์โหลดและนำเข้าการตั้งค่าคอนฟิก ER ใดๆ </span><span class="sxs-lookup"><span data-stu-id="71d6e-108">Default document types are also set when you download and import any ER configuration.</span></span> 


## <a name="run-report"></a><span data-ttu-id="71d6e-109">รันรายงาน</span><span class="sxs-lookup"><span data-stu-id="71d6e-109">Run report</span></span>
1. <span data-ttu-id="71d6e-110">ไปที่ การจัดการองค์กร > การรายงานทางอิเล็กทรอนิกส์ > การตั้งค่าคอนฟิก</span><span class="sxs-lookup"><span data-stu-id="71d6e-110">Go to Organization administration > Electronic reporting > Configurations.</span></span>
2. <span data-ttu-id="71d6e-111">ในแผนภูมิ ขยาย 'Financial dimensions sample model'</span><span class="sxs-lookup"><span data-stu-id="71d6e-111">In the tree, expand 'Financial dimensions sample model'.</span></span>
3. <span data-ttu-id="71d6e-112">ในแผนภูมิ เลือก 'แบบจำลองตัวอย่างมิติทางการเงิน\รายงานสมุดรายวันบัญชีแยกประเภท'</span><span class="sxs-lookup"><span data-stu-id="71d6e-112">In the tree, select 'Financial dimensions sample model\Ledger journal report'.</span></span>
4. <span data-ttu-id="71d6e-113">คลิกดำเนินการ</span><span class="sxs-lookup"><span data-stu-id="71d6e-113">Click Run.</span></span>
5. <span data-ttu-id="71d6e-114">ในฟิลด์ชื่อมิติ ในฟิลด์ชื่อมิติ ป้อนหรือเลือกค่า</span><span class="sxs-lookup"><span data-stu-id="71d6e-114">In the Dimension name field, In the Dimension name field, enter or select a value..</span></span>
    * <span data-ttu-id="71d6e-115">เมื่อต้องการเลือกมิติทั้งหมดในบริษัทปัจจุบัน ให้ป้อนข้อมูลต่อไปนี้: BusinessUnit;CostCenter;Department;ItemGroup;MainAccount;Project</span><span class="sxs-lookup"><span data-stu-id="71d6e-115">To select all dimensions in the current company, enter the following:  BusinessUnit;CostCenter;Department;ItemGroup;MainAccount;Project</span></span>  
6. <span data-ttu-id="71d6e-116">ขยายเรกคอร์ดเพื่อที่จะรวมส่วน</span><span class="sxs-lookup"><span data-stu-id="71d6e-116">Expand the Records to include section.</span></span>
7. <span data-ttu-id="71d6e-117">คลิกตัวกรอง </span><span class="sxs-lookup"><span data-stu-id="71d6e-117">Click Filter.</span></span>
8. <span data-ttu-id="71d6e-118">เลือกแถวสำหรับตารางสมุดรายวันบัญชีแยกประเภทและฟิลด์หมายเลขชุดงานสมุดรายวัน</span><span class="sxs-lookup"><span data-stu-id="71d6e-118">Select the row for the Ledger journal table and the Journal batch number field.</span></span>
9. <span data-ttu-id="71d6e-119">ในฟิลด์เกณฑ์ ให้พิมพ์ '00057'</span><span class="sxs-lookup"><span data-stu-id="71d6e-119">In the Criteria field, type '00057'.</span></span>
10. <span data-ttu-id="71d6e-120">คลิก ตกลง</span><span class="sxs-lookup"><span data-stu-id="71d6e-120">Click OK.</span></span>
11. <span data-ttu-id="71d6e-121">คลิก ตกลง</span><span class="sxs-lookup"><span data-stu-id="71d6e-121">Click OK.</span></span>
    * <span data-ttu-id="71d6e-122">ตรวจทานผลลัพธ์ที่สร้างขึ้น </span><span class="sxs-lookup"><span data-stu-id="71d6e-122">Review the generated output.</span></span> <span data-ttu-id="71d6e-123">โปรดทราบว่าสำหรับแต่ละธุรกรรมของชุดงานที่เลือก มิติทางการเงินจากชุดมิติที่สอดคล้องกันจะแสดงขึ้น </span><span class="sxs-lookup"><span data-stu-id="71d6e-123">Note that for each transaction of the selected batch, the financial dimensions from the corresponding dimensions set are presented.</span></span> <span data-ttu-id="71d6e-124">รันรายงานนี้และเลือกมิติต่างๆ เพื่อดูว่ารายงานไม่ขึ้นอยู่กับจำนวนของมิติที่เลือกหรือจำนวนของมิติที่ตั้งค่าคอนฟิกสำหรับอินสแตนซ์ นี้</span><span class="sxs-lookup"><span data-stu-id="71d6e-124">Run this report and select different dimensions to see that the report is not dependent on the number of selected dimensions or the number of dimensions configured for this instance.</span></span>  

