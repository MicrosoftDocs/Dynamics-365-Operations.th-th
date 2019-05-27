---
title: ประมวลผลและติดตามข้อมูลต้นทาง
description: การประมวลผลข้อมูลทั้งหมดจะถูกเรียกใช้โดยเรียงตามงาน
author: ShylaThompson
manager: AnnBe
ms.date: 06/27/2017
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: e476416420875ba0f2401cf251d34977ae84b8f5
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 05/15/2019
ms.locfileid: "1546535"
---
# <a name="process-and-trace-source-data"></a><span data-ttu-id="d065c-103">ประมวลผลและติดตามข้อมูลต้นทาง</span><span class="sxs-lookup"><span data-stu-id="d065c-103">Process and trace source data</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="d065c-104">การประมวลผลข้อมูลทั้งหมดจะถูกเรียกใช้โดยเรียงตามงาน</span><span class="sxs-lookup"><span data-stu-id="d065c-104">All data processing is run by jobs.</span></span> <span data-ttu-id="d065c-105">สำหรับตัวให้บริการข้อมูลและงานแต่ละรายการ ระบบจะสร้างสมุดรายวันให้กับเอกสารที่มีการรันกระบวนการ และที่มีการประมวลผลรายการในงานปัจจุบัน</span><span class="sxs-lookup"><span data-stu-id="d065c-105">For each job and data provider, a journal is created to document that the process has been run, and that the entries were processed in the current job.</span></span> <span data-ttu-id="d065c-106">ใช้กระบวนงานนี้เพื่อตั้งค่าแหล่งข้อมูลและจากนั้นสืบค้นจุดเริ่มต้นของรายการต้นทุนที่ระบุ</span><span class="sxs-lookup"><span data-stu-id="d065c-106">Use this procedure to set up a data source and then  trace the origin of a specific cost entry.</span></span> <span data-ttu-id="d065c-107">การบันทึกข้อมูลนี้ใช้บริษัทข้อมูลสาธิต USP2</span><span class="sxs-lookup"><span data-stu-id="d065c-107">This recording uses the USP2 demo data company USP2.</span></span> <span data-ttu-id="d065c-108">ก่อนที่คุณจะทำงานนี้ให้เสร็จสมบูรณ์ ให้ตรวจสอบให้แน่ใจว่าคุณได้เล่นคู่มืองานต่อไปนี้ "สร้างบัญชีแยกประเภทสำหรับการลงบัญชีต้นทุน" "กำหนดหน่วยการควบคุมต้นทุน" และ "จัดการแหล่งข้อมูลสำหรับบัญชีแยกประเภทการบัญชีต้นทุน" แล้ว</span><span class="sxs-lookup"><span data-stu-id="d065c-108">Before you complete this task, make sure that you play the following task guides: "Create a cost accounting ledger," "Define cost control units," and "Manage data source for the cost accounting ledger."</span></span>

1. <span data-ttu-id="d065c-109">ไปที่ บัญชีต้นทุน > การตั้งค่าบัญชีแยกประเภท > บัญชีแยกประเภทสำหรับการบัญชีต้นทุน</span><span class="sxs-lookup"><span data-stu-id="d065c-109">Go to Cost accounting > Ledger setup > Cost accounting ledgers.</span></span>
2. <span data-ttu-id="d065c-110">ในรายการนี้ ให้ค้นหาและเลือกเรกคอร์ดที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="d065c-110">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="d065c-111">เลือกบัญชีแยกประเภทการบัญชีต้นทุนที่คุณสร้างไว้ก่อนหน้านี้</span><span class="sxs-lookup"><span data-stu-id="d065c-111">Select the cost accounting ledger that you created earlier.</span></span>  
3. <span data-ttu-id="d065c-112">คลิก เวอร์ชันจริง</span><span class="sxs-lookup"><span data-stu-id="d065c-112">Click Actual versions.</span></span>
4. <span data-ttu-id="d065c-113">ในบานหน้าต่างการดำเนินการ คลิก การประมวลผลแหล่งข้อมูล</span><span class="sxs-lookup"><span data-stu-id="d065c-113">On the Action Pane, click Source data processing.</span></span>
5. <span data-ttu-id="d065c-114">คลิก สมุดรายวันการโอนย้ายรายการบัญชีแยกประเภททั่วไป</span><span class="sxs-lookup"><span data-stu-id="d065c-114">Click General ledger entry transfer journals.</span></span>
6. <span data-ttu-id="d065c-115">ในรายการนี้ ให้ค้นหาและเลือกเรกคอร์ดที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="d065c-115">In the list, find and select the desired record.</span></span>
7. <span data-ttu-id="d065c-116">คลิก รายการสมุดรายวัน</span><span class="sxs-lookup"><span data-stu-id="d065c-116">Click Journal entries.</span></span>
8. <span data-ttu-id="d065c-117">ในรายการนี้ ให้ทำเครื่องหมายแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="d065c-117">In the list, mark the selected row.</span></span>
9. <span data-ttu-id="d065c-118">คลิกรายการต้นทุน</span><span class="sxs-lookup"><span data-stu-id="d065c-118">Click Cost entries.</span></span>
10. <span data-ttu-id="d065c-119">คลิก รายการต้นทาง</span><span class="sxs-lookup"><span data-stu-id="d065c-119">Click Source entry.</span></span>
11. <span data-ttu-id="d065c-120">ในบานหน้าต่างการดำเนินการ คลิก การประมวลผลแหล่งข้อมูล</span><span class="sxs-lookup"><span data-stu-id="d065c-120">On the Action Pane, click Source data processing.</span></span>
12. <span data-ttu-id="d065c-121">คลิก บัญชีแยกประเภททั่วไป</span><span class="sxs-lookup"><span data-stu-id="d065c-121">Click General ledger.</span></span>
13. <span data-ttu-id="d065c-122">ในฟิลด์รอบระยะเวลาปฏิทินทางการเงิน ให้ป้อนหรือเลือกค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="d065c-122">In the Fiscal calendar period field, enter or select a value.</span></span>
    * <span data-ttu-id="d065c-123">สำหรับตัวอย่างนี้ เลือก ทางการเงิน 2017 รอบระยะเวลา 9</span><span class="sxs-lookup"><span data-stu-id="d065c-123">For this example, select Fiscal 2017 Period 9.</span></span>  
14. <span data-ttu-id="d065c-124">คลิก ตกลง</span><span class="sxs-lookup"><span data-stu-id="d065c-124">Click OK.</span></span>

