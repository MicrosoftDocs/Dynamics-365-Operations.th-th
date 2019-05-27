---
title: ประมวลผลสมุดรายวันการปันส่วนบัญชีแยกประเภท
description: 'ใช้หน้าคำขอขั้นตอนการปันส่วนเพื่อสร้างสมุดรายวันการปันส่วนที่สามารถตรวจทานได้ และอนุมัติก่อนลงรายการบัญชีแยกประเภททั่วไป หรือลงรายการบัญชีโดยตรงในบัญชีแยกประเภททั่วไป '
author: aprilolson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerAllocationRequest, LedgerJournalTable, LedgerJournalTransAllocation
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: d2046e25719c9023bee99736488a4ee6f22723fe
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 05/15/2019
ms.locfileid: "1550832"
---
# <a name="process-ledger-allocation-journal"></a><span data-ttu-id="60654-103">ประมวลผลสมุดรายวันการปันส่วนบัญชีแยกประเภท</span><span class="sxs-lookup"><span data-stu-id="60654-103">Process ledger allocation journal</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="60654-104">ใช้หน้าคำขอขั้นตอนการปันส่วนเพื่อสร้างสมุดรายวันการปันส่วนที่สามารถตรวจทานได้ และอนุมัติก่อนลงรายการบัญชีแยกประเภททั่วไป หรือลงรายการบัญชีโดยตรงในบัญชีแยกประเภททั่วไป </span><span class="sxs-lookup"><span data-stu-id="60654-104">Use the Process allocation request page to create an allocation journal that can be reviewed and approved before posting to General ledger, or posted directly to General ledger.</span></span> <span data-ttu-id="60654-105">ก่อนที่คุณสามารถสร้างสมุดรายวันการปันส่วนได้ ต้องมีอย่างน้อยหนึ่งรายการที่ใช้งานบัญชีแยกประเภทกฎการปันส่วน </span><span class="sxs-lookup"><span data-stu-id="60654-105">Before you can create an allocations journal, there must be least one active Ledger allocation rule.</span></span> <span data-ttu-id="60654-106">งานนี้ใช้บริษัทสาธิต USMF </span><span class="sxs-lookup"><span data-stu-id="60654-106">This task uses the USMF demo company.</span></span>

1. <span data-ttu-id="60654-107">ไปที่บัญชีแยกประเภททั่วไป > การปันส่วน > ประมวลผลคำขอการปันส่วน</span><span class="sxs-lookup"><span data-stu-id="60654-107">Go to General ledger > Allocations > Process allocation request.</span></span>
2. <span data-ttu-id="60654-108">ในฟิลด์กฎ ให้คลิกปุ่มดรอปดาวน์เพื่อเปิดการค้นหา</span><span class="sxs-lookup"><span data-stu-id="60654-108">In the Rule field, click the drop-down button to open the lookup.</span></span>
3. <span data-ttu-id="60654-109">ในรายการนี้ ให้ค้นหาและเลือกเรกคอร์ดที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="60654-109">In the list, find and select the desired record.</span></span>
4. <span data-ttu-id="60654-110">ในรายการนี้ ให้คลิกลิงค์ในแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="60654-110">In the list, click the link in the selected row.</span></span>
5. <span data-ttu-id="60654-111">ในฟิลด์ ณ วันที่ ให้ใส่วันที่</span><span class="sxs-lookup"><span data-stu-id="60654-111">In the As of date field, enter a date.</span></span>
    * <span data-ttu-id="60654-112">ณ วันที่ เป็นสิ่งสำคัญมาก เมื่อบัญชีแยกประเภทเป็นแหล่งข้อมูลสำหรับกฎ </span><span class="sxs-lookup"><span data-stu-id="60654-112">The As of Date is very important when the Ledger is the Data source for the rule.</span></span> <span data-ttu-id="60654-113">วันที่นี้เป็นตัวควบคุมยอดดุลบัญชีแยกประเภทที่จะรวมไว้สำหรับการปันส่วน </span><span class="sxs-lookup"><span data-stu-id="60654-113">This date controls which ledger balances to include for allocation.</span></span>     <span data-ttu-id="60654-114">ในฟิลด์ต้นทางเป็นศูนย์ให้เลือกหยุด </span><span class="sxs-lookup"><span data-stu-id="60654-114">In the Zero source field select Stop.</span></span> <span data-ttu-id="60654-115">การดำเนินการนี้จะหยุดกระบวนการปันส่วน และแสดงข้อความแจ้งว่า เลือกจำนวนเงินต้นทางเป็นศูนย์</span><span class="sxs-lookup"><span data-stu-id="60654-115">This will  Stop the allocation process and display a message that states that a zero source amount is selected.</span></span>  
6. <span data-ttu-id="60654-116">ในฟิลด์ตัวเลือกข้อเสนอ เลือก 'ข้อเสนอเท่านั้น'</span><span class="sxs-lookup"><span data-stu-id="60654-116">In the Proposal options field, select 'Proposal only'.</span></span>
    * <span data-ttu-id="60654-117">เลือกข้อเสนอเพื่อตรวจทาน และทางเลือกอนุมัติผลในการปันส่วนสมุดรายวันก่อนเพื่อลงรายการบัญชีการปันส่วนบัญชีแยกประเภททั่วไป</span><span class="sxs-lookup"><span data-stu-id="60654-117">Select Proposal only to review and optionally approve the result in Allocation journals prior to posting the allocation to General ledger.</span></span>  
7. <span data-ttu-id="60654-118">ในฟิลด์วันที่ลงรายการบัญชีแยกประเภททั่วไป ให้ใส่วันที่</span><span class="sxs-lookup"><span data-stu-id="60654-118">In the GL posting date field, enter a date.</span></span>
8. <span data-ttu-id="60654-119">คลิก ตกลง</span><span class="sxs-lookup"><span data-stu-id="60654-119">Click OK.</span></span>
9. <span data-ttu-id="60654-120">ไปที่บัญชีแยกประเภททั่วไป > การปันส่วน > สมุดรายวันการปันส่วน</span><span class="sxs-lookup"><span data-stu-id="60654-120">Go to General ledger > Allocations > Allocation journals.</span></span>
10. <span data-ttu-id="60654-121">คลิกรายการ</span><span class="sxs-lookup"><span data-stu-id="60654-121">Click Lines.</span></span>
11. <span data-ttu-id="60654-122">คลิก ลงรายการบัญชี</span><span class="sxs-lookup"><span data-stu-id="60654-122">Click Post.</span></span>
12. <span data-ttu-id="60654-123">คลิก ลงรายการบัญชี</span><span class="sxs-lookup"><span data-stu-id="60654-123">Click Post.</span></span>

