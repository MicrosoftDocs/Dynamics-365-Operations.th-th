---
title: ประมวลผลสมุดรายวันการปันส่วนบัญชีแยกประเภท
description: หัวข้อนี้จะอธิบายถึงวิธีการประมวลผลคำขอการปันส่วนใน Dynamics 365 Finance
author: aprilolson
manager: AnnBe
ms.date: 07/26/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerAllocationRequest, LedgerJournalTable, LedgerJournalTransAllocation
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 33e989d3641ae1eaa28a55398fcf51674ac1ed72
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 10/13/2020
ms.locfileid: "4448436"
---
# <a name="process-ledger-allocation-journal"></a><span data-ttu-id="1f83b-103">ประมวลผลสมุดรายวันการปันส่วนบัญชีแยกประเภท</span><span class="sxs-lookup"><span data-stu-id="1f83b-103">Process ledger allocation journal</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="1f83b-104">หัวข้อนี้จะอธิบายถึงวิธีการประมวลผลคำขอการปันส่วน</span><span class="sxs-lookup"><span data-stu-id="1f83b-104">This topic explains how to process an allocation request.</span></span> <span data-ttu-id="1f83b-105">ใช้หน้าคำขอขั้นตอนการปันส่วนเพื่อสร้างสมุดรายวันการปันส่วนที่สามารถตรวจทานได้ และอนุมัติก่อนลงรายการบัญชีแยกประเภททั่วไป หรือลงรายการบัญชีโดยตรงในบัญชีแยกประเภททั่วไป </span><span class="sxs-lookup"><span data-stu-id="1f83b-105">Use the Process allocation request page to create an allocation journal that can be reviewed and approved before posting to General ledger, or posted directly to General ledger.</span></span> <span data-ttu-id="1f83b-106">ก่อนที่คุณสามารถสร้างสมุดรายวันการปันส่วนได้ ต้องมีอย่างน้อยหนึ่งรายการที่ใช้งานบัญชีแยกประเภทกฎการปันส่วน </span><span class="sxs-lookup"><span data-stu-id="1f83b-106">Before you can create an allocations journal, there must be least one active Ledger allocation rule.</span></span> <span data-ttu-id="1f83b-107">งานนี้ใช้บริษัทสาธิต USMF </span><span class="sxs-lookup"><span data-stu-id="1f83b-107">This task uses the USMF demo company.</span></span>

1. <span data-ttu-id="1f83b-108">ในบานหน้าต่างนำทาง ไปที่ **โมดูล > บัญชีแยกประเภททั่วไป > การปันส่วน > ประมวลผลคำขอการปันส่วน**</span><span class="sxs-lookup"><span data-stu-id="1f83b-108">In the navigation pane, go to **Modules > General ledger > Allocations > Process allocation request**.</span></span>
2. <span data-ttu-id="1f83b-109">ในฟิลด์ **กฎ** ให้เลือกเรกคอร์ดที่ต้องการในเมนูแบบหล่นลง</span><span class="sxs-lookup"><span data-stu-id="1f83b-109">In the **Rule** field, select the desired record in the drop-down menu.</span></span>
3. <span data-ttu-id="1f83b-110">ในฟิลด์ **ณ วันที่** ให้ใส่วันที่</span><span class="sxs-lookup"><span data-stu-id="1f83b-110">In the **As of date** field, enter a date.</span></span>

    - <span data-ttu-id="1f83b-111">**ณ วันที่** เป็นสิ่งสำคัญมาก เมื่อบัญชีแยกประเภทเป็นแหล่งข้อมูลสำหรับกฎ</span><span class="sxs-lookup"><span data-stu-id="1f83b-111">The **As of Date** is very important when the Ledger is the Data source for the rule.</span></span> <span data-ttu-id="1f83b-112">วันที่นี้เป็นตัวควบคุมยอดดุลบัญชีแยกประเภทที่จะรวมไว้สำหรับการปันส่วน </span><span class="sxs-lookup"><span data-stu-id="1f83b-112">This date controls which ledger balances to include for allocation.</span></span>  
    - <span data-ttu-id="1f83b-113">ในฟิลด์ **ต้นทางเป็นศูนย์** ให้เลือก **หยุด**</span><span class="sxs-lookup"><span data-stu-id="1f83b-113">In the **Zero source** field select **Stop**.</span></span> <span data-ttu-id="1f83b-114">การดำเนินการนี้จะหยุดกระบวนการปันส่วน และแสดงข้อความที่แจ้งว่า มีการเลือกจำนวนเงินต้นทางเป็นศูนย์</span><span class="sxs-lookup"><span data-stu-id="1f83b-114">This will stop the allocation process and display a message that states that a zero source amount is selected.</span></span>  

4. <span data-ttu-id="1f83b-115">ในฟิลด์ **ตัวเลือกข้อเสนอ** เลือก **ข้อเสนอเท่านั้น**</span><span class="sxs-lookup"><span data-stu-id="1f83b-115">In the **Proposal options** field, select **Proposal only**.</span></span> <span data-ttu-id="1f83b-116">เลือก **ข้อเสนอเท่านั้น** เพื่อตรวจทานและอาจอนุมัติผลลัพธ์ในการปันส่วนสมุดรายวัน ก่อนการลงรายการบัญชีการปันส่วนไปยังบัญชีแยกประเภททั่วไป</span><span class="sxs-lookup"><span data-stu-id="1f83b-116">Select **Proposal only** to review and optionally approve the result in Allocation journals prior to posting the allocation to General ledger.</span></span>  
5. <span data-ttu-id="1f83b-117">ในฟิลด์วันที่ลงรายการบัญชีแยกประเภททั่วไป ให้ใส่วันที่</span><span class="sxs-lookup"><span data-stu-id="1f83b-117">In the GL posting date field, enter a date.</span></span>
6. <span data-ttu-id="1f83b-118">เลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="1f83b-118">Select **OK**.</span></span>
7. <span data-ttu-id="1f83b-119">ในบานหน้าต่างนำทาง ไปที่ **โมดูล > บัญชีแยกประเภททั่วไป > การปันส่วน > สมุดรายวันการปันส่วน**</span><span class="sxs-lookup"><span data-stu-id="1f83b-119">In the navigation pane, go to **Modules > General ledger > Allocations > Allocation journals**.</span></span>
8. <span data-ttu-id="1f83b-120">เลือก **รายการ**</span><span class="sxs-lookup"><span data-stu-id="1f83b-120">Select **Lines**.</span></span>
9. <span data-ttu-id="1f83b-121">เลือก **ลงรายการบัญชี**</span><span class="sxs-lookup"><span data-stu-id="1f83b-121">Select **Post**.</span></span>
10. <span data-ttu-id="1f83b-122">เลือก **ลงรายการบัญชี**</span><span class="sxs-lookup"><span data-stu-id="1f83b-122">Select **Post**.</span></span>

