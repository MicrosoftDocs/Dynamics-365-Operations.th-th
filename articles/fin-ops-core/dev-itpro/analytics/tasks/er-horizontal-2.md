---
title: ER ใช้ช่วงที่สามารถขยายได้ตามแนวนอน เพื่อเพิ่มคอลัมน์ลงในรายงาน Excel แบบไดนามิก (ส่วนที่ 2 - รันรูปแบบ)
description: หัวข้อนี้อธิบายวิธีการตั้งค่าคอนฟิกรูปแบบการรายงานทางอิเล็กทรอนิกส์ (ER) เพื่อสร้างรายงานเป็นไฟล์เวิร์กชีต OPENXML (Excel) (ส่วนที่ 2)
author: NickSelin
ms.date: 08/29/2018
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
ms.openlocfilehash: a62bad6ca241a2372a72e312ec5a707008a5fc09
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 03/31/2021
ms.locfileid: "5744998"
---
# <a name="er-use-horizontally-expandable-ranges-to-dynamically-add-columns-in-excel-reports-part-2---run-format"></a><span data-ttu-id="392f4-104">ER ใช้ช่วงที่สามารถขยายได้ตามแนวนอน เพื่อเพิ่มคอลัมน์ลงในรายงาน Excel แบบไดนามิก (ส่วนที่ 2 - รันรูปแบบ)</span><span class="sxs-lookup"><span data-stu-id="392f4-104">ER Use horizontally expandable ranges to dynamically add columns in Excel reports (Part 2 - Run format)</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="392f4-105">ขั้นตอนต่อไปนี้อธิบายวิธีกำหนดผู้ใช้ให้กับผู้ดูแลระบบหรือวิธีการที่บทบาทนักพัฒนาการรายงานทางอิเล็กทรอนิกส์สามารถตั้งค่าคอนฟิกรูปแบบการรายงานทางอิเล็กทรอนิกส์ (ER) เพื่อสร้างรายงานเป็นไฟล์แผ่นงาน (Excel) OPENXML โดยที่สามารถสร้างคอลัมน์ที่จำเป็นได้แบบไดนามิกเป็นช่วงที่สามารถขยายได้ในแนวนอน </span><span class="sxs-lookup"><span data-stu-id="392f4-105">The following steps explain how a user assigned to the system administrator or electronic reporting developer role can configure an Electronic reporting (ER) format to generate reports as OPENXML worksheets (Excel) files in which the required columns can be created dynamically as horizontally expandable ranges.</span></span> <span data-ttu-id="392f4-106">สามารถดำเนินการขั้นตอนเหล่านี้ได้ในบริษัท DEMF </span><span class="sxs-lookup"><span data-stu-id="392f4-106">These steps can be performed in the DEMF company.</span></span>

<span data-ttu-id="392f4-107">เพื่อทำให้ขั้นตอนเหล่านี้เสร็จสมบูรณ์ ก่อนอื่นคุณต้องดำเนินการตามขั้นตอนในกระบวนงาน "ER ใช้ช่วงที่สามารถขยายได้ตามแนวนอนเพื่อเพิ่มคอลัมน์ลงในรายงาน Excel แบบไดนามิก (ส่วนที่ 1: ออกแบบรูปแบบ)" ให้เสร็จสมบูรณ์</span><span class="sxs-lookup"><span data-stu-id="392f4-107">To complete these steps, you must first complete the steps in the "ER Use horizontally expandable ranges to dynamically add columns in Excel reports (Part 1: Design format)" procedure.</span></span>

<span data-ttu-id="392f4-108">กระบวนงานนี้ใช้สำหรับคุณลักษณะทั้ที่ถูกเพิ่มลงใน Dynamics 365 for Operations รุ่น 1611</span><span class="sxs-lookup"><span data-stu-id="392f4-108">This procedure is for a feature that was added in Dynamics 365 for Operations version 1611.</span></span>


## <a name="find-created-format"></a><span data-ttu-id="392f4-109">ค้นหารูปแบบที่สร้างขึ้น</span><span class="sxs-lookup"><span data-stu-id="392f4-109">Find created format</span></span>
1. <span data-ttu-id="392f4-110">ไปที่ การจัดการองค์กร > การรายงานทางอิเล็กทรอนิกส์ > การตั้งค่าคอนฟิก</span><span class="sxs-lookup"><span data-stu-id="392f4-110">Go to Organization administration > Electronic reporting > Configurations.</span></span>
2. <span data-ttu-id="392f4-111">ในแผนภูมิ ขยาย 'Financial dimensions sample model'</span><span class="sxs-lookup"><span data-stu-id="392f4-111">In the tree, expand 'Financial dimensions sample model'.</span></span>
3. <span data-ttu-id="392f4-112">ในแผนภูมิ เลือก 'Financial dimensions sample model\Sample report with horizontally expandable ranges'</span><span class="sxs-lookup"><span data-stu-id="392f4-112">In the tree, select 'Financial dimensions sample model\Sample report with horizontally expandable ranges'.</span></span>

## <a name="execute-format-to-create-excel-output"></a><span data-ttu-id="392f4-113">ดำเนินการรูปแบบเพื่อสร้างผลลัพธ์ Excel</span><span class="sxs-lookup"><span data-stu-id="392f4-113">Execute format to create Excel output</span></span>
1. <span data-ttu-id="392f4-114">คลิก เรียกใช้</span><span class="sxs-lookup"><span data-stu-id="392f4-114">Click Run.</span></span>
2. <span data-ttu-id="392f4-115">ในฟิลด์ชื่อมิติ พิมพ์ 'BusinessUnit;CostCenter;Department'</span><span class="sxs-lookup"><span data-stu-id="392f4-115">In the Dimension name field, type 'BusinessUnit;CostCenter;Department'.</span></span>
    * <span data-ttu-id="392f4-116">ในฟิลด์ชื่อมิติ ให้ป้อนหรือเลือกค่า </span><span class="sxs-lookup"><span data-stu-id="392f4-116">In the Dimension name field, enter or select a value.</span></span>  <span data-ttu-id="392f4-117">เมื่อต้องการเลือกมิติทั้งหมดสำหรับบริษัทปัจจุบัน ให้ป้อนข้อมูลต่อไปนี้: BusinessUnit;CostCenter;Department;ItemGroup;MainAccount;Project</span><span class="sxs-lookup"><span data-stu-id="392f4-117">To select all dimensions for the current company, enter the following:  BusinessUnit;CostCenter;Department;ItemGroup;MainAccount;Project</span></span>  
3. <span data-ttu-id="392f4-118">ขยายเรกคอร์ดเพื่อที่จะรวมส่วน</span><span class="sxs-lookup"><span data-stu-id="392f4-118">Expand the Records to include section.</span></span>
4. <span data-ttu-id="392f4-119">คลิกตัวกรอง </span><span class="sxs-lookup"><span data-stu-id="392f4-119">Click Filter.</span></span>
5. <span data-ttu-id="392f4-120">เลือกแถวสำหรับตารางสมุดรายวันบัญชีแยกประเภทและฟิลด์หมายเลขชุดงานสมุดรายวัน</span><span class="sxs-lookup"><span data-stu-id="392f4-120">Select the row for the Ledger journal table and the Journal batch number field.</span></span>
6. <span data-ttu-id="392f4-121">ในฟิลด์เกณฑ์ ให้พิมพ์ '00057..00058'</span><span class="sxs-lookup"><span data-stu-id="392f4-121">In the Criteria field, type '00057..00058'.</span></span>
    * <span data-ttu-id="392f4-122">00057..00058</span><span class="sxs-lookup"><span data-stu-id="392f4-122">00057..00058</span></span>  
7. <span data-ttu-id="392f4-123">คลิก ตกลง</span><span class="sxs-lookup"><span data-stu-id="392f4-123">Click OK.</span></span>
8. <span data-ttu-id="392f4-124">คลิก ตกลง</span><span class="sxs-lookup"><span data-stu-id="392f4-124">Click OK.</span></span>
    * <span data-ttu-id="392f4-125">ตรวจทานผลลัพธ์ที่สร้างขึ้น </span><span class="sxs-lookup"><span data-stu-id="392f4-125">Review the generated output.</span></span> <span data-ttu-id="392f4-126">โปรดทราบว่าไฟล์ Excel ที่สร้างขึ้นใหม่มีจำนวนคอลัมน์ที่เลือกสำหรับมิติทางการเงินเท่ากัน </span><span class="sxs-lookup"><span data-stu-id="392f4-126">Note that the newly created Excel file contains the same number of columns that were selected for financial dimensions.</span></span> <span data-ttu-id="392f4-127">ส่วนหัวของรายงานในคอลัมน์เหล่านั้นแสดงถึงชื่อของมิติทางการเงิน</span><span class="sxs-lookup"><span data-stu-id="392f4-127">The report header in those columns represents financial dimensions' names.</span></span> <span data-ttu-id="392f4-128">รายการของธุรกรรมในคอลัมน์เหล่านั้นแสดงถึงมิติทางการเงิน</span><span class="sxs-lookup"><span data-stu-id="392f4-128">The transactions' lines in those columns represent financial dimensions.</span></span> <span data-ttu-id="392f4-129">รันรายงานนี้และเลือกมิติต่างๆ เพื่อดูว่ารายงานไม่ขึ้นอยู่กับจำนวนของมิติที่เลือกหรือจำนวนของมิติที่ตั้งค่าคอนฟิกสำหรับอินสแตนซ์ นี้</span><span class="sxs-lookup"><span data-stu-id="392f4-129">Run this report and select different dimensions to see that the report is not dependent on the number of selected dimensions or the number of dimensions configured for this instance.</span></span>  



[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]