--- 
title: "เรียกใช้รูปแบบเพื่อเพิ่มคอลัมน์ในรายงาน Excel แบบไดนามิกเป็นช่วงแบบขยายได้ในแนวนอน"
description: "ขั้นตอนต่อไปนี้อธิบายวิธีกำหนดผู้ใช้ให้กับผู้ดูแลระบบหรือวิธีการที่บทบาทนักพัฒนาการรายงานทางอิเล็กทรอนิกส์สามารถตั้งค่าคอนฟิกรูปแบบการรายงานทางอิเล็กทรอนิกส์ (ER) เพื่อสร้างรายงานเป็นไฟล์แผ่นงาน (Excel) OPENXML โดยที่สามารถสร้างคอลัมน์ที่จำเป็นได้แบบไดนามิกเป็นช่วงที่สามารถขยายได้ในแนวนอน "
author: NickSelin
manager: AnnBe
ms.date: 10/28/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: kfend
ms.search.scope: Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: e782d33f3748524491dace28008cd9148ae70529
ms.openlocfilehash: c7d563da9a02c91cce17cfa1d4a6915dd768ac3d
ms.contentlocale: th-th
ms.lasthandoff: 08/09/2018

---
# <a name="run-formats-to-dynamically-add-columns-to-excel-reports-as-horizontally-expandable-ranges"></a><span data-ttu-id="d2114-103">เรียกใช้รูปแบบเพื่อเพิ่มคอลัมน์ในรายงาน Excel แบบไดนามิกเป็นช่วงแบบขยายได้ในแนวนอน</span><span class="sxs-lookup"><span data-stu-id="d2114-103">Run formats to dynamically add columns to Excel reports as horizontally expandable ranges</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="d2114-104">ขั้นตอนต่อไปนี้อธิบายวิธีกำหนดผู้ใช้ให้กับผู้ดูแลระบบหรือวิธีการที่บทบาทนักพัฒนาการรายงานทางอิเล็กทรอนิกส์สามารถตั้งค่าคอนฟิกรูปแบบการรายงานทางอิเล็กทรอนิกส์ (ER) เพื่อสร้างรายงานเป็นไฟล์แผ่นงาน (Excel) OPENXML โดยที่สามารถสร้างคอลัมน์ที่จำเป็นได้แบบไดนามิกเป็นช่วงที่สามารถขยายได้ในแนวนอน </span><span class="sxs-lookup"><span data-stu-id="d2114-104">The following steps explain how a user assigned to the system administrator or electronic reporting developer role can configure an Electronic reporting (ER) format to generate reports as OPENXML worksheets (Excel) files in which the required columns can be created dynamically as horizontally expandable ranges.</span></span> <span data-ttu-id="d2114-105">สามารถดำเนินการขั้นตอนเหล่านี้ได้ในบริษัท DEMF </span><span class="sxs-lookup"><span data-stu-id="d2114-105">These steps can be performed in the DEMF company.</span></span>

<span data-ttu-id="d2114-106">เพื่อทำตามขั้นตอนเหล่านี้ ก่อนอื่นคุณต้องดำเนินการตามขั้นตอนกระบวนการ: "ER ใช้ช่วงที่สามารถขยายได้ตามแนวนอนเพื่อเพิ่มคอลัมน์ลงในรายงาน Excel แบบไดนามิก (ส่วนที่ 1: ออกแบบรูปแบบ)"</span><span class="sxs-lookup"><span data-stu-id="d2114-106">To complete these steps, you must first complete the steps in the “ER Use horizontally expandable ranges to dynamically add columns in Excel reports (Part 1: Design format)” procedure.</span></span>

<span data-ttu-id="d2114-107">กระบวนงานนี้ใช้สำหรับลักษณะการทำงานที่ถูกเพิ่มลงใน Dynamics 365 for Operations รุ่น 1611</span><span class="sxs-lookup"><span data-stu-id="d2114-107">This procedure is for a feature that was added in Dynamics 365 for Operations version 1611.</span></span>


## <a name="find-created-format"></a><span data-ttu-id="d2114-108">ค้นหารูปแบบที่สร้างขึ้น</span><span class="sxs-lookup"><span data-stu-id="d2114-108">Find created format</span></span>
1. <span data-ttu-id="d2114-109">ไปที่ การจัดการองค์กร > การรายงานทางอิเล็กทรอนิกส์ > การตั้งค่าคอนฟิก</span><span class="sxs-lookup"><span data-stu-id="d2114-109">Go to Organization administration > Electronic reporting > Configurations.</span></span>
2. <span data-ttu-id="d2114-110">ในแผนภูมิ ขยาย 'Financial dimensions sample model'</span><span class="sxs-lookup"><span data-stu-id="d2114-110">In the tree, expand 'Financial dimensions sample model'.</span></span>
3. <span data-ttu-id="d2114-111">ในแผนภูมิ เลือก 'Financial dimensions sample model\Sample report with horizontally expandable ranges'</span><span class="sxs-lookup"><span data-stu-id="d2114-111">In the tree, select 'Financial dimensions sample model\Sample report with horizontally expandable ranges'.</span></span>

## <a name="execute-format-to-create-excel-output"></a><span data-ttu-id="d2114-112">ดำเนินการรูปแบบเพื่อสร้างผลลัพธ์ Excel</span><span class="sxs-lookup"><span data-stu-id="d2114-112">Execute format to create Excel output</span></span>
1. <span data-ttu-id="d2114-113">คลิก เรียกใช้</span><span class="sxs-lookup"><span data-stu-id="d2114-113">Click Run.</span></span>
2. <span data-ttu-id="d2114-114">ในฟิลด์ชื่อมิติ พิมพ์ 'BusinessUnit;CostCenter;Department'</span><span class="sxs-lookup"><span data-stu-id="d2114-114">In the Dimension name field, type 'BusinessUnit;CostCenter;Department'.</span></span>
    * <span data-ttu-id="d2114-115">ในฟิลด์ชื่อมิติ ให้ป้อนหรือเลือกค่า </span><span class="sxs-lookup"><span data-stu-id="d2114-115">In the Dimension name field, enter or select a value.</span></span>  <span data-ttu-id="d2114-116">เมื่อต้องการเลือกมิติทั้งหมดสำหรับบริษัทปัจจุบัน ให้ป้อนข้อมูลต่อไปนี้: BusinessUnit;CostCenter;Department;ItemGroup;MainAccount;Project</span><span class="sxs-lookup"><span data-stu-id="d2114-116">To select all dimensions for the current company, enter the following:  BusinessUnit;CostCenter;Department;ItemGroup;MainAccount;Project</span></span>  
3. <span data-ttu-id="d2114-117">ขยายเรกคอร์ดเพื่อที่จะรวมส่วน</span><span class="sxs-lookup"><span data-stu-id="d2114-117">Expand the Records to include section.</span></span>
4. <span data-ttu-id="d2114-118">คลิกตัวกรอง </span><span class="sxs-lookup"><span data-stu-id="d2114-118">Click Filter.</span></span>
5. <span data-ttu-id="d2114-119">เลือกแถวสำหรับตารางสมุดรายวันบัญชีแยกประเภทและฟิลด์หมายเลขชุดงานสมุดรายวัน</span><span class="sxs-lookup"><span data-stu-id="d2114-119">Select the row for the Ledger journal table and the Journal batch number field.</span></span>
6. <span data-ttu-id="d2114-120">ในฟิลด์เกณฑ์ ให้พิมพ์ '00057..00058'</span><span class="sxs-lookup"><span data-stu-id="d2114-120">In the Criteria field, type '00057..00058'.</span></span>
    * <span data-ttu-id="d2114-121">00057..00058</span><span class="sxs-lookup"><span data-stu-id="d2114-121">00057..00058</span></span>  
7. <span data-ttu-id="d2114-122">คลิก ตกลง</span><span class="sxs-lookup"><span data-stu-id="d2114-122">Click OK.</span></span>
8. <span data-ttu-id="d2114-123">คลิก ตกลง</span><span class="sxs-lookup"><span data-stu-id="d2114-123">Click OK.</span></span>
    * <span data-ttu-id="d2114-124">ตรวจทานผลลัพธ์ที่สร้างขึ้น </span><span class="sxs-lookup"><span data-stu-id="d2114-124">Review the generated output.</span></span> <span data-ttu-id="d2114-125">โปรดทราบว่าไฟล์ Excel ที่สร้างขึ้นใหม่มีจำนวนคอลัมน์ที่เลือกสำหรับมิติทางการเงินเท่ากัน </span><span class="sxs-lookup"><span data-stu-id="d2114-125">Note that the newly created Excel file contains the same number of columns that were selected for financial dimensions.</span></span> <span data-ttu-id="d2114-126">ส่วนหัวของรายงานในคอลัมน์เหล่านั้นแสดงถึงชื่อมิติทางการเงิน </span><span class="sxs-lookup"><span data-stu-id="d2114-126">The report header in those columns represents financial dimensions’ names.</span></span> <span data-ttu-id="d2114-127">บรรทัดของธุรกรรมในคอลัมน์เหล่านั้นแสดงถึงมิติทางการเงิน </span><span class="sxs-lookup"><span data-stu-id="d2114-127">The transactions’ lines in those columns represent financial dimensions.</span></span> <span data-ttu-id="d2114-128">รันรายงานนี้และเลือกมิติต่างๆ เพื่อดูว่ารายงานไม่ขึ้นอยู่กับจำนวนของมิติที่เลือก หรือจำนวนของมิติที่ตั้งค่าคอนฟิกสำหรับอินสแตนซ์ Dynamics 365 for Finance and Operations นี้</span><span class="sxs-lookup"><span data-stu-id="d2114-128">Run this report and select different dimensions to see that the report is not dependent on the number of selected dimensions or the number of dimensions configured for this Dynamics 365 for Finance and Operations instance.</span></span>  


