---
title: ER ใช้มิติทางการเงินเป็นแหล่งข้อมูล (ส่วนที่ 4 - รันรายงาน)
description: หัวข้อนี้อธิบายวิธีการตั้งค่าคอนฟิกแบบโมเดลการรายงานทางอิเล็กทรอนิกส์ (ER) เพื่อใช้มิติทางการเงินเป็นแหล่งข้อมูลของรายงาน ER (ส่วนที่ 4)
author: NickSelin
ms.date: 05/27/2020
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: ERSolutionTable, SysQueryForm
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 4a06936da71d7b05f312a99c8c11d148403d29c3
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 03/31/2021
ms.locfileid: "5752399"
---
# <a name="er-use-financial-dimensions-as-a-data-source-part-4---run-the-report"></a><span data-ttu-id="07149-104">ER ใช้มิติทางการเงินเป็นแหล่งข้อมูล (ส่วนที่ 4 - รันรายงาน)</span><span class="sxs-lookup"><span data-stu-id="07149-104">ER Use financial dimensions as a data source (Part 4 - Run the report)</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="07149-105">ขั้นตอนต่อไปนี้อธิบายวิธีการที่ผู้ใช้ที่ถูกกำหนดบทบาทผู้ดูแลระบบหรือนักพัฒนาการรายงานทางอิเล็กทรอนิกส์สามารถตั้งค่าคอนฟิกแบบจำลองการรายงานทางอิเล็กทรอนิกส์ (ER) (ER) เพื่อใช้มิติทางการเงินเป็นแหล่งข้อมูลสำหรับรายงาน ER </span><span class="sxs-lookup"><span data-stu-id="07149-105">The following steps explain how a user assigned to the system administrator or electronic reporting developer role can configure an Electronic reporting (ER) model to use financial dimensions as a data source for ER reports.</span></span> <span data-ttu-id="07149-106">สามารถดำเนินการขั้นตอนเหล่านี้ได้ในบริษัท DEMF </span><span class="sxs-lookup"><span data-stu-id="07149-106">These steps can be performed in the DEMF company.</span></span>

<span data-ttu-id="07149-107">เพื่อทำขั้นตอนเหล่านี้ให้เสร็จสมบูรณ์ อันดับแรกคุณต้องทำขั้นตอนต่างๆ ในกระบวนงาน "ER ใช้มิติทางการเงินเป็นแหล่งข้อมูล (ส่วนที่ 3: ออกแบบรายงาน)" ให้เสร็จสมบูรณ์</span><span class="sxs-lookup"><span data-stu-id="07149-107">To complete these steps, you must first complete the steps in the "ER Use financial dimensions as a data source (Part 3: Design the report)" procedure.</span></span> <span data-ttu-id="07149-108">นอกจากนี้คุณยังต้องตั้งค่าคอนฟิกชนิดเอกสารเริ่มต้นบนหน้าพารามิเตอร์การรายงานทางอิเล็กทรอนิกส์ </span><span class="sxs-lookup"><span data-stu-id="07149-108">You must also configure default document types on the Electronic reporting parameters page.</span></span> <span data-ttu-id="07149-109">ชนิดเอกสารเริ่มต้นจะถูกตั้งค่าเมื่อคุณดาวน์โหลดและนำเข้าการตั้งค่าคอนฟิก ER ใดๆ </span><span class="sxs-lookup"><span data-stu-id="07149-109">Default document types are also set when you download and import any ER configuration.</span></span> 


## <a name="run-report"></a><span data-ttu-id="07149-110">รันรายงาน</span><span class="sxs-lookup"><span data-stu-id="07149-110">Run report</span></span>
1. <span data-ttu-id="07149-111">ไปที่ การจัดการองค์กร > การรายงานทางอิเล็กทรอนิกส์ > การตั้งค่าคอนฟิก</span><span class="sxs-lookup"><span data-stu-id="07149-111">Go to Organization administration > Electronic reporting > Configurations.</span></span>
2. <span data-ttu-id="07149-112">ในแผนภูมิ ขยาย 'Financial dimensions sample model'</span><span class="sxs-lookup"><span data-stu-id="07149-112">In the tree, expand 'Financial dimensions sample model'.</span></span>
3. <span data-ttu-id="07149-113">ในแผนภูมิ เลือก 'แบบจำลองตัวอย่างมิติทางการเงิน\รายงานสมุดรายวันบัญชีแยกประเภท'</span><span class="sxs-lookup"><span data-stu-id="07149-113">In the tree, select 'Financial dimensions sample model\Ledger journal report'.</span></span>
4. <span data-ttu-id="07149-114">คลิกดำเนินการ</span><span class="sxs-lookup"><span data-stu-id="07149-114">Click Run.</span></span>
<span data-ttu-id="07149-115">![หน้าการตั้งค่าคอนฟิก ER](../media/er-financial-dimensions-guides-run1.png)</span><span class="sxs-lookup"><span data-stu-id="07149-115">![ER configurations page](../media/er-financial-dimensions-guides-run1.png)</span></span>
5. <span data-ttu-id="07149-116">ในฟิลด์ชื่อมิติ ให้ป้อนหรือเลือกค่า </span><span class="sxs-lookup"><span data-stu-id="07149-116">In the Dimension name field, enter or select a value.</span></span>
    * <span data-ttu-id="07149-117">เมื่อต้องการเลือกมิติทั้งหมดในบริษัทปัจจุบัน ให้ป้อนข้อมูลต่อไปนี้: BusinessUnit;CostCenter;Department;ItemGroup;MainAccount;Project</span><span class="sxs-lookup"><span data-stu-id="07149-117">To select all dimensions in the current company, enter the following information:  BusinessUnit;CostCenter;Department;ItemGroup;MainAccount;Project</span></span>  
![หน้าการตั้งค่าคอนฟิก ER](../media/er-financial-dimensions-guides-run2.png)
6. <span data-ttu-id="07149-119">ขยายเรกคอร์ดเพื่อที่จะรวมส่วน</span><span class="sxs-lookup"><span data-stu-id="07149-119">Expand the Records to include section.</span></span>
7. <span data-ttu-id="07149-120">คลิกที่ตัวกรองข้อมูล</span><span class="sxs-lookup"><span data-stu-id="07149-120">Click Filter.</span></span>
8. <span data-ttu-id="07149-121">เลือกแถวสำหรับตารางสมุดรายวันบัญชีแยกประเภทและฟิลด์หมายเลขชุดงานสมุดรายวัน</span><span class="sxs-lookup"><span data-stu-id="07149-121">Select the row for the Ledger journal table and the Journal batch number field.</span></span>
9. <span data-ttu-id="07149-122">ในฟิลด์เกณฑ์ ให้พิมพ์ '00057'</span><span class="sxs-lookup"><span data-stu-id="07149-122">In the Criteria field, type '00057'.</span></span>
10. <span data-ttu-id="07149-123">คลิก ตกลง </span><span class="sxs-lookup"><span data-stu-id="07149-123">Click OK.</span></span>
11. <span data-ttu-id="07149-124">คลิก ตกลง </span><span class="sxs-lookup"><span data-stu-id="07149-124">Click OK.</span></span>
<span data-ttu-id="07149-125">![หน้าการตั้งค่าคอนฟิก ER](../media/er-financial-dimensions-guides-run3.png)</span><span class="sxs-lookup"><span data-stu-id="07149-125">![ER configurations page](../media/er-financial-dimensions-guides-run3.png)</span></span>
    * <span data-ttu-id="07149-126">ตรวจทานผลลัพธ์ที่สร้างขึ้น </span><span class="sxs-lookup"><span data-stu-id="07149-126">Review the generated output.</span></span> <span data-ttu-id="07149-127">สำหรับธุรกรรมแต่ละรายการของชุดงานที่เลือก มิติทางการเงินจากชุดมิติที่สอดคล้องกันจะแสดงขึ้น</span><span class="sxs-lookup"><span data-stu-id="07149-127">For each transaction of the selected batch, the financial dimensions from the corresponding dimensions set are presented.</span></span> <span data-ttu-id="07149-128">รันรายงานนี้และเลือกมิติต่างๆ เพื่อดูว่ารายงานไม่ขึ้นอยู่กับจำนวนของมิติที่เลือกหรือจำนวนของมิติที่ตั้งค่าคอนฟิกสำหรับอินสแตนซ์ นี้</span><span class="sxs-lookup"><span data-stu-id="07149-128">Run this report and select different dimensions to see that the report is not dependent on the number of selected dimensions or the number of dimensions configured for this instance.</span></span>  
![หน้าการตั้งค่าคอนฟิก ER](../media/er-financial-dimensions-guides-run4.png)


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]