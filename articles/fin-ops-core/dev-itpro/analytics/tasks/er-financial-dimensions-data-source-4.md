---
title: ER ใช้มิติทางการเงินเป็นแหล่งข้อมูล (ส่วนที่ 4 - รันรายงาน)
description: 'ขั้นตอนต่อไปนี้อธิบายวิธีการที่ผู้ใช้ที่ถูกกำหนดบทบาทผู้ดูแลระบบหรือนักพัฒนาการรายงานทางอิเล็กทรอนิกส์สามารถตั้งค่าคอนฟิกแบบจำลองการรายงานทางอิเล็กทรอนิกส์ (ER) (ER) เพื่อใช้มิติทางการเงินเป็นแหล่งข้อมูลสำหรับรายงาน ER '
author: NickSelin
manager: AnnBe
ms.date: 05/27/2020
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ERSolutionTable, SysQueryForm
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: fb7f49310aa25ff7c17ab4bcd50e1842be84fe2d
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 12/05/2020
ms.locfileid: "4684750"
---
# <a name="er-use-financial-dimensions-as-a-data-source-part-4---run-the-report"></a><span data-ttu-id="70746-103">ER ใช้มิติทางการเงินเป็นแหล่งข้อมูล (ส่วนที่ 4 - รันรายงาน)</span><span class="sxs-lookup"><span data-stu-id="70746-103">ER Use financial dimensions as a data source (Part 4 - Run the report)</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="70746-104">ขั้นตอนต่อไปนี้อธิบายวิธีการที่ผู้ใช้ที่ถูกกำหนดบทบาทผู้ดูแลระบบหรือนักพัฒนาการรายงานทางอิเล็กทรอนิกส์สามารถตั้งค่าคอนฟิกแบบจำลองการรายงานทางอิเล็กทรอนิกส์ (ER) (ER) เพื่อใช้มิติทางการเงินเป็นแหล่งข้อมูลสำหรับรายงาน ER </span><span class="sxs-lookup"><span data-stu-id="70746-104">The following steps explain how a user assigned to the system administrator or electronic reporting developer role can configure an Electronic reporting (ER) model to use financial dimensions as a data source for ER reports.</span></span> <span data-ttu-id="70746-105">สามารถดำเนินการขั้นตอนเหล่านี้ได้ในบริษัท DEMF </span><span class="sxs-lookup"><span data-stu-id="70746-105">These steps can be performed in the DEMF company.</span></span>

<span data-ttu-id="70746-106">เพื่อทำขั้นตอนเหล่านี้ให้เสร็จสมบูรณ์ อันดับแรกคุณต้องทำขั้นตอนต่างๆ ในกระบวนงาน "ER ใช้มิติทางการเงินเป็นแหล่งข้อมูล (ส่วนที่ 3: ออกแบบรายงาน)" ให้เสร็จสมบูรณ์</span><span class="sxs-lookup"><span data-stu-id="70746-106">To complete these steps, you must first complete the steps in the "ER Use financial dimensions as a data source (Part 3: Design the report)" procedure.</span></span> <span data-ttu-id="70746-107">นอกจากนี้คุณยังต้องตั้งค่าคอนฟิกชนิดเอกสารเริ่มต้นบนหน้าพารามิเตอร์การรายงานทางอิเล็กทรอนิกส์ </span><span class="sxs-lookup"><span data-stu-id="70746-107">You must also configure default document types on the Electronic reporting parameters page.</span></span> <span data-ttu-id="70746-108">ชนิดเอกสารเริ่มต้นจะถูกตั้งค่าเมื่อคุณดาวน์โหลดและนำเข้าการตั้งค่าคอนฟิก ER ใดๆ </span><span class="sxs-lookup"><span data-stu-id="70746-108">Default document types are also set when you download and import any ER configuration.</span></span> 


## <a name="run-report"></a><span data-ttu-id="70746-109">รันรายงาน</span><span class="sxs-lookup"><span data-stu-id="70746-109">Run report</span></span>
1. <span data-ttu-id="70746-110">ไปที่ การจัดการองค์กร > การรายงานทางอิเล็กทรอนิกส์ > การตั้งค่าคอนฟิก</span><span class="sxs-lookup"><span data-stu-id="70746-110">Go to Organization administration > Electronic reporting > Configurations.</span></span>
2. <span data-ttu-id="70746-111">ในแผนภูมิ ขยาย 'Financial dimensions sample model'</span><span class="sxs-lookup"><span data-stu-id="70746-111">In the tree, expand 'Financial dimensions sample model'.</span></span>
3. <span data-ttu-id="70746-112">ในแผนภูมิ เลือก 'แบบจำลองตัวอย่างมิติทางการเงิน\รายงานสมุดรายวันบัญชีแยกประเภท'</span><span class="sxs-lookup"><span data-stu-id="70746-112">In the tree, select 'Financial dimensions sample model\Ledger journal report'.</span></span>
4. <span data-ttu-id="70746-113">คลิกดำเนินการ</span><span class="sxs-lookup"><span data-stu-id="70746-113">Click Run.</span></span>
<span data-ttu-id="70746-114">![หน้าการตั้งค่าคอนฟิก ER](../media/er-financial-dimensions-guides-run1.png)</span><span class="sxs-lookup"><span data-stu-id="70746-114">![ER configurations page](../media/er-financial-dimensions-guides-run1.png)</span></span>
5. <span data-ttu-id="70746-115">ในฟิลด์ชื่อมิติ ให้ป้อนหรือเลือกค่า </span><span class="sxs-lookup"><span data-stu-id="70746-115">In the Dimension name field, enter or select a value.</span></span>
    * <span data-ttu-id="70746-116">เมื่อต้องการเลือกมิติทั้งหมดในบริษัทปัจจุบัน ให้ป้อนข้อมูลต่อไปนี้: BusinessUnit;CostCenter;Department;ItemGroup;MainAccount;Project</span><span class="sxs-lookup"><span data-stu-id="70746-116">To select all dimensions in the current company, enter the following information:  BusinessUnit;CostCenter;Department;ItemGroup;MainAccount;Project</span></span>  
![หน้าการตั้งค่าคอนฟิก ER](../media/er-financial-dimensions-guides-run2.png)
6. <span data-ttu-id="70746-118">ขยายเรกคอร์ดเพื่อที่จะรวมส่วน</span><span class="sxs-lookup"><span data-stu-id="70746-118">Expand the Records to include section.</span></span>
7. <span data-ttu-id="70746-119">คลิกที่ตัวกรองข้อมูล</span><span class="sxs-lookup"><span data-stu-id="70746-119">Click Filter.</span></span>
8. <span data-ttu-id="70746-120">เลือกแถวสำหรับตารางสมุดรายวันบัญชีแยกประเภทและฟิลด์หมายเลขชุดงานสมุดรายวัน</span><span class="sxs-lookup"><span data-stu-id="70746-120">Select the row for the Ledger journal table and the Journal batch number field.</span></span>
9. <span data-ttu-id="70746-121">ในฟิลด์เกณฑ์ ให้พิมพ์ '00057'</span><span class="sxs-lookup"><span data-stu-id="70746-121">In the Criteria field, type '00057'.</span></span>
10. <span data-ttu-id="70746-122">คลิก ตกลง </span><span class="sxs-lookup"><span data-stu-id="70746-122">Click OK.</span></span>
11. <span data-ttu-id="70746-123">คลิก ตกลง </span><span class="sxs-lookup"><span data-stu-id="70746-123">Click OK.</span></span>
<span data-ttu-id="70746-124">![หน้าการตั้งค่าคอนฟิก ER](../media/er-financial-dimensions-guides-run3.png)</span><span class="sxs-lookup"><span data-stu-id="70746-124">![ER configurations page](../media/er-financial-dimensions-guides-run3.png)</span></span>
    * <span data-ttu-id="70746-125">ตรวจทานผลลัพธ์ที่สร้างขึ้น </span><span class="sxs-lookup"><span data-stu-id="70746-125">Review the generated output.</span></span> <span data-ttu-id="70746-126">สำหรับธุรกรรมแต่ละรายการของชุดงานที่เลือก มิติทางการเงินจากชุดมิติที่สอดคล้องกันจะแสดงขึ้น</span><span class="sxs-lookup"><span data-stu-id="70746-126">For each transaction of the selected batch, the financial dimensions from the corresponding dimensions set are presented.</span></span> <span data-ttu-id="70746-127">รันรายงานนี้และเลือกมิติต่างๆ เพื่อดูว่ารายงานไม่ขึ้นอยู่กับจำนวนของมิติที่เลือกหรือจำนวนของมิติที่ตั้งค่าคอนฟิกสำหรับอินสแตนซ์ นี้</span><span class="sxs-lookup"><span data-stu-id="70746-127">Run this report and select different dimensions to see that the report is not dependent on the number of selected dimensions or the number of dimensions configured for this instance.</span></span>  
![หน้าการตั้งค่าคอนฟิก ER](../media/er-financial-dimensions-guides-run4.png)
