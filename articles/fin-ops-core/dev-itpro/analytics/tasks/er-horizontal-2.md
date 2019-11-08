---
title: ER ใช้ช่วงที่สามารถขยายได้ตามแนวนอน เพื่อเพิ่มคอลัมน์ลงในรายงาน Excel แบบไดนามิก (ส่วนที่ 2 - รันรูปแบบ)
description: 'ขั้นตอนต่อไปนี้อธิบายวิธีกำหนดผู้ใช้ให้กับผู้ดูแลระบบหรือวิธีการที่บทบาทนักพัฒนาการรายงานทางอิเล็กทรอนิกส์สามารถตั้งค่าคอนฟิกรูปแบบการรายงานทางอิเล็กทรอนิกส์ (ER) เพื่อสร้างรายงานเป็นไฟล์แผ่นงาน (Excel) OPENXML โดยที่สามารถสร้างคอลัมน์ที่จำเป็นได้แบบไดนามิกเป็นช่วงที่สามารถขยายได้ในแนวนอน '
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
ms.openlocfilehash: b76a2df5cd7714ffda6d0563d3d9013f032db7c2
ms.sourcegitcommit: 75db3b75d35d27034f9b56e7119c9d0cb7666830
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 10/03/2019
ms.locfileid: "2550893"
---
# <a name="er-use-horizontally-expandable-ranges-to-dynamically-add-columns-in-excel-reports-part-2---run-format"></a><span data-ttu-id="b08f0-103">ER ใช้ช่วงที่สามารถขยายได้ตามแนวนอน เพื่อเพิ่มคอลัมน์ลงในรายงาน Excel แบบไดนามิก (ส่วนที่ 2 - รันรูปแบบ)</span><span class="sxs-lookup"><span data-stu-id="b08f0-103">ER Use horizontally expandable ranges to dynamically add columns in Excel reports (Part 2 - Run format)</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="b08f0-104">ขั้นตอนต่อไปนี้อธิบายวิธีกำหนดผู้ใช้ให้กับผู้ดูแลระบบหรือวิธีการที่บทบาทนักพัฒนาการรายงานทางอิเล็กทรอนิกส์สามารถตั้งค่าคอนฟิกรูปแบบการรายงานทางอิเล็กทรอนิกส์ (ER) เพื่อสร้างรายงานเป็นไฟล์แผ่นงาน (Excel) OPENXML โดยที่สามารถสร้างคอลัมน์ที่จำเป็นได้แบบไดนามิกเป็นช่วงที่สามารถขยายได้ในแนวนอน </span><span class="sxs-lookup"><span data-stu-id="b08f0-104">The following steps explain how a user assigned to the system administrator or electronic reporting developer role can configure an Electronic reporting (ER) format to generate reports as OPENXML worksheets (Excel) files in which the required columns can be created dynamically as horizontally expandable ranges.</span></span> <span data-ttu-id="b08f0-105">สามารถดำเนินการขั้นตอนเหล่านี้ได้ในบริษัท DEMF </span><span class="sxs-lookup"><span data-stu-id="b08f0-105">These steps can be performed in the DEMF company.</span></span>

<span data-ttu-id="b08f0-106">เพื่อทำตามขั้นตอนเหล่านี้ ก่อนอื่นคุณต้องดำเนินการตามขั้นตอนกระบวนการ: "ER ใช้ช่วงที่สามารถขยายได้ตามแนวนอนเพื่อเพิ่มคอลัมน์ลงในรายงาน Excel แบบไดนามิก (ส่วนที่ 1: ออกแบบรูปแบบ)"</span><span class="sxs-lookup"><span data-stu-id="b08f0-106">To complete these steps, you must first complete the steps in the “ER Use horizontally expandable ranges to dynamically add columns in Excel reports (Part 1: Design format)” procedure.</span></span>

<span data-ttu-id="b08f0-107">กระบวนงานนี้ใช้สำหรับคุณลักษณะทั้ที่ถูกเพิ่มลงใน Dynamics 365 for Operations รุ่น 1611</span><span class="sxs-lookup"><span data-stu-id="b08f0-107">This procedure is for a feature that was added in Dynamics 365 for Operations version 1611.</span></span>


## <a name="find-created-format"></a><span data-ttu-id="b08f0-108">ค้นหารูปแบบที่สร้างขึ้น</span><span class="sxs-lookup"><span data-stu-id="b08f0-108">Find created format</span></span>
1. <span data-ttu-id="b08f0-109">ไปที่ การจัดการองค์กร > การรายงานทางอิเล็กทรอนิกส์ > การตั้งค่าคอนฟิก</span><span class="sxs-lookup"><span data-stu-id="b08f0-109">Go to Organization administration > Electronic reporting > Configurations.</span></span>
2. <span data-ttu-id="b08f0-110">ในแผนภูมิ ขยาย 'Financial dimensions sample model'</span><span class="sxs-lookup"><span data-stu-id="b08f0-110">In the tree, expand 'Financial dimensions sample model'.</span></span>
3. <span data-ttu-id="b08f0-111">ในแผนภูมิ เลือก 'Financial dimensions sample model\Sample report with horizontally expandable ranges'</span><span class="sxs-lookup"><span data-stu-id="b08f0-111">In the tree, select 'Financial dimensions sample model\Sample report with horizontally expandable ranges'.</span></span>

## <a name="execute-format-to-create-excel-output"></a><span data-ttu-id="b08f0-112">ดำเนินการรูปแบบเพื่อสร้างผลลัพธ์ Excel</span><span class="sxs-lookup"><span data-stu-id="b08f0-112">Execute format to create Excel output</span></span>
1. <span data-ttu-id="b08f0-113">คลิก เรียกใช้</span><span class="sxs-lookup"><span data-stu-id="b08f0-113">Click Run.</span></span>
2. <span data-ttu-id="b08f0-114">ในฟิลด์ชื่อมิติ พิมพ์ 'BusinessUnit;CostCenter;Department'</span><span class="sxs-lookup"><span data-stu-id="b08f0-114">In the Dimension name field, type 'BusinessUnit;CostCenter;Department'.</span></span>
    * <span data-ttu-id="b08f0-115">ในฟิลด์ชื่อมิติ ให้ป้อนหรือเลือกค่า </span><span class="sxs-lookup"><span data-stu-id="b08f0-115">In the Dimension name field, enter or select a value.</span></span>  <span data-ttu-id="b08f0-116">เมื่อต้องการเลือกมิติทั้งหมดสำหรับบริษัทปัจจุบัน ให้ป้อนข้อมูลต่อไปนี้: BusinessUnit;CostCenter;Department;ItemGroup;MainAccount;Project</span><span class="sxs-lookup"><span data-stu-id="b08f0-116">To select all dimensions for the current company, enter the following:  BusinessUnit;CostCenter;Department;ItemGroup;MainAccount;Project</span></span>  
3. <span data-ttu-id="b08f0-117">ขยายเรกคอร์ดเพื่อที่จะรวมส่วน</span><span class="sxs-lookup"><span data-stu-id="b08f0-117">Expand the Records to include section.</span></span>
4. <span data-ttu-id="b08f0-118">คลิกตัวกรอง </span><span class="sxs-lookup"><span data-stu-id="b08f0-118">Click Filter.</span></span>
5. <span data-ttu-id="b08f0-119">เลือกแถวสำหรับตารางสมุดรายวันบัญชีแยกประเภทและฟิลด์หมายเลขชุดงานสมุดรายวัน</span><span class="sxs-lookup"><span data-stu-id="b08f0-119">Select the row for the Ledger journal table and the Journal batch number field.</span></span>
6. <span data-ttu-id="b08f0-120">ในฟิลด์เกณฑ์ ให้พิมพ์ '00057..00058'</span><span class="sxs-lookup"><span data-stu-id="b08f0-120">In the Criteria field, type '00057..00058'.</span></span>
    * <span data-ttu-id="b08f0-121">00057..00058</span><span class="sxs-lookup"><span data-stu-id="b08f0-121">00057..00058</span></span>  
7. <span data-ttu-id="b08f0-122">คลิก ตกลง</span><span class="sxs-lookup"><span data-stu-id="b08f0-122">Click OK.</span></span>
8. <span data-ttu-id="b08f0-123">คลิก ตกลง</span><span class="sxs-lookup"><span data-stu-id="b08f0-123">Click OK.</span></span>
    * <span data-ttu-id="b08f0-124">ตรวจทานผลลัพธ์ที่สร้างขึ้น </span><span class="sxs-lookup"><span data-stu-id="b08f0-124">Review the generated output.</span></span> <span data-ttu-id="b08f0-125">โปรดทราบว่าไฟล์ Excel ที่สร้างขึ้นใหม่มีจำนวนคอลัมน์ที่เลือกสำหรับมิติทางการเงินเท่ากัน </span><span class="sxs-lookup"><span data-stu-id="b08f0-125">Note that the newly created Excel file contains the same number of columns that were selected for financial dimensions.</span></span> <span data-ttu-id="b08f0-126">ส่วนหัวของรายงานในคอลัมน์เหล่านั้นแสดงถึงชื่อมิติทางการเงิน </span><span class="sxs-lookup"><span data-stu-id="b08f0-126">The report header in those columns represents financial dimensions’ names.</span></span> <span data-ttu-id="b08f0-127">บรรทัดของธุรกรรมในคอลัมน์เหล่านั้นแสดงถึงมิติทางการเงิน </span><span class="sxs-lookup"><span data-stu-id="b08f0-127">The transactions’ lines in those columns represent financial dimensions.</span></span> <span data-ttu-id="b08f0-128">รันรายงานนี้และเลือกมิติต่างๆ เพื่อดูว่ารายงานไม่ขึ้นอยู่กับจำนวนของมิติที่เลือกหรือจำนวนของมิติที่ตั้งค่าคอนฟิกสำหรับอินสแตนซ์ นี้</span><span class="sxs-lookup"><span data-stu-id="b08f0-128">Run this report and select different dimensions to see that the report is not dependent on the number of selected dimensions or the number of dimensions configured for this instance.</span></span>  

