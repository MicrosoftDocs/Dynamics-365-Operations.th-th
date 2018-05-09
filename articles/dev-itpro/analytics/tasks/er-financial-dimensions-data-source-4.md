--- 
title: "รันรายงานที่ใช้มิติทางการเงินเป็นแหล่งข้อมูล"
description: "ขั้นตอนต่อไปนี้อธิบายวิธีการที่ผู้ใช้ที่ถูกกำหนดบทบาทผู้ดูแลระบบหรือนักพัฒนาการรายงานทางอิเล็กทรอนิกส์สามารถตั้งค่าคอนฟิกแบบจำลองการรายงานทางอิเล็กทรอนิกส์ (ER) (ER) เพื่อใช้มิติทางการเงินเป็นแหล่งข้อมูลสำหรับรายงาน ER "
author: NickSelin
manager: AnnBe
ms.date: 11/02/2017
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
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: fefac4db9d6fec926068483bbe8ae91a6d5d6028
ms.contentlocale: th-th
ms.lasthandoff: 05/08/2018

---
# <a name="run-a-report-that-uses-financial-dimensions-as-a-data-source"></a><span data-ttu-id="60338-103">รันรายงานที่ใช้มิติทางการเงินเป็นแหล่งข้อมูล</span><span class="sxs-lookup"><span data-stu-id="60338-103">Run a report that uses financial dimensions as a data source</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="60338-104">ขั้นตอนต่อไปนี้อธิบายวิธีการที่ผู้ใช้ที่ถูกกำหนดบทบาทผู้ดูแลระบบหรือนักพัฒนาการรายงานทางอิเล็กทรอนิกส์สามารถตั้งค่าคอนฟิกแบบจำลองการรายงานทางอิเล็กทรอนิกส์ (ER) (ER) เพื่อใช้มิติทางการเงินเป็นแหล่งข้อมูลสำหรับรายงาน ER </span><span class="sxs-lookup"><span data-stu-id="60338-104">The following steps explain how a user assigned to the system administrator or electronic reporting developer role can configure an Electronic reporting (ER) model to use financial dimensions as a data source for ER reports.</span></span> <span data-ttu-id="60338-105">สามารถดำเนินการขั้นตอนเหล่านี้ได้ในบริษัท DEMF </span><span class="sxs-lookup"><span data-stu-id="60338-105">These steps can be performed in the DEMF company.</span></span>

<span data-ttu-id="60338-106">เพื่อทำขั้นตอนเหล่านี้ให้เสร็จสมบูรณ์ อันดับแรกคุณต้องทำขั้นตอนต่างๆ ในกระบวนงาน "ER ใช้มิติทางการเงินเป็นแหล่งข้อมูล (ส่วนที่ 3: ออกแบบรายงาน)"</span><span class="sxs-lookup"><span data-stu-id="60338-106">To complete these steps, you must first complete the steps in the “ER Use financial dimensions as a data source (Part 3: Design the report)” procedure.</span></span> <span data-ttu-id="60338-107">นอกจากนี้คุณยังต้องตั้งค่าคอนฟิกชนิดเอกสารเริ่มต้นบนหน้าพารามิเตอร์การรายงานทางอิเล็กทรอนิกส์ </span><span class="sxs-lookup"><span data-stu-id="60338-107">You must also configure default document types on the Electronic reporting parameters page.</span></span> <span data-ttu-id="60338-108">ชนิดเอกสารเริ่มต้นจะถูกตั้งค่าเมื่อคุณดาวน์โหลดและนำเข้าการตั้งค่าคอนฟิก ER ใดๆ </span><span class="sxs-lookup"><span data-stu-id="60338-108">Default document types are also set when you download and import any ER configuration.</span></span> 


## <a name="run-report"></a><span data-ttu-id="60338-109">รันรายงาน</span><span class="sxs-lookup"><span data-stu-id="60338-109">Run report</span></span>
1. <span data-ttu-id="60338-110">ไปที่ การจัดการองค์กร > การรายงานทางอิเล็กทรอนิกส์ > การตั้งค่าคอนฟิก</span><span class="sxs-lookup"><span data-stu-id="60338-110">Go to Organization administration > Electronic reporting > Configurations.</span></span>
2. <span data-ttu-id="60338-111">ในแผนภูมิ ขยาย 'Financial dimensions sample model'</span><span class="sxs-lookup"><span data-stu-id="60338-111">In the tree, expand 'Financial dimensions sample model'.</span></span>
3. <span data-ttu-id="60338-112">ในแผนภูมิ เลือก 'แบบจำลองตัวอย่างมิติทางการเงิน\รายงานสมุดรายวันบัญชีแยกประเภท'</span><span class="sxs-lookup"><span data-stu-id="60338-112">In the tree, select 'Financial dimensions sample model\Ledger journal report'.</span></span>
4. <span data-ttu-id="60338-113">คลิกดำเนินการ</span><span class="sxs-lookup"><span data-stu-id="60338-113">Click Run.</span></span>
5. <span data-ttu-id="60338-114">ในฟิลด์ชื่อมิติ ในฟิลด์ชื่อมิติ ป้อนหรือเลือกค่า</span><span class="sxs-lookup"><span data-stu-id="60338-114">In the Dimension name field, In the Dimension name field, enter or select a value.</span></span>
    * <span data-ttu-id="60338-115">เมื่อต้องการเลือกมิติทั้งหมดในบริษัทปัจจุบัน ให้ป้อนข้อมูลต่อไปนี้: BusinessUnit;CostCenter;Department;ItemGroup;MainAccount;Project</span><span class="sxs-lookup"><span data-stu-id="60338-115">To select all dimensions in the current company, enter the following:  BusinessUnit;CostCenter;Department;ItemGroup;MainAccount;Project</span></span>  
6. <span data-ttu-id="60338-116">ขยายเรกคอร์ดเพื่อที่จะรวมส่วน</span><span class="sxs-lookup"><span data-stu-id="60338-116">Expand the Records to include section.</span></span>
7. <span data-ttu-id="60338-117">คลิกตัวกรอง </span><span class="sxs-lookup"><span data-stu-id="60338-117">Click Filter.</span></span>
8. <span data-ttu-id="60338-118">เลือกแถวสำหรับตารางสมุดรายวันบัญชีแยกประเภทและฟิลด์หมายเลขชุดงานสมุดรายวัน</span><span class="sxs-lookup"><span data-stu-id="60338-118">Select the row for the Ledger journal table and the Journal batch number field.</span></span>
9. <span data-ttu-id="60338-119">ในฟิลด์เกณฑ์ ให้พิมพ์ '00057'</span><span class="sxs-lookup"><span data-stu-id="60338-119">In the Criteria field, type '00057'.</span></span>
10. <span data-ttu-id="60338-120">คลิก ตกลง</span><span class="sxs-lookup"><span data-stu-id="60338-120">Click OK.</span></span>
11. <span data-ttu-id="60338-121">คลิก ตกลง</span><span class="sxs-lookup"><span data-stu-id="60338-121">Click OK.</span></span>
    * <span data-ttu-id="60338-122">ตรวจทานผลลัพธ์ที่สร้างขึ้น </span><span class="sxs-lookup"><span data-stu-id="60338-122">Review the generated output.</span></span> <span data-ttu-id="60338-123">โปรดทราบว่าสำหรับแต่ละธุรกรรมของชุดงานที่เลือก มิติทางการเงินจากชุดมิติที่สอดคล้องกันจะแสดงขึ้น </span><span class="sxs-lookup"><span data-stu-id="60338-123">Note that for each transaction of the selected batch, the financial dimensions from the corresponding dimensions set are presented.</span></span> <span data-ttu-id="60338-124">รันรายงานนี้และเลือกมิติต่างๆ เพื่อดูว่ารายงานไม่ขึ้นอยู่กับจำนวนของมิติที่เลือก หรือจำนวนของมิติที่ตั้งค่าคอนฟิกสำหรับอินสแตนซ์ Dynamics 365 for Finance and Operations นี้</span><span class="sxs-lookup"><span data-stu-id="60338-124">Run this report and select different dimensions to see that the report is not dependent on the number of selected dimensions or the number of dimensions configured for this Dynamics 365 for Finance and Operations instance.</span></span>  


