---
title: จัดการแหล่งข้อมูลสำหรับบัญชีแยกประเภทต้นทุน
description: ใช้กระบวนงานนี้ในการจัดการแหล่งข้อมูลบัญชีแยกประเภททั่วไปสำหรับบัญชีแยกประเภทสำหรับการลงบัญชีต้นทุน
author: ShylaThompson
manager: AnnBe
ms.date: 06/27/2017
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 543c1cd4bbb35e51e17d5e0c7c588d87fbe3c106
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 09/27/2019
ms.locfileid: "2187716"
---
# <a name="manage-a-data-source-for-the-cost-accounting-ledger"></a><span data-ttu-id="dc915-103">จัดการแหล่งข้อมูลสำหรับบัญชีแยกประเภทต้นทุน</span><span class="sxs-lookup"><span data-stu-id="dc915-103">Manage a data source for the cost accounting ledger</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="dc915-104">ใช้กระบวนงานนี้ในการจัดการแหล่งข้อมูลบัญชีแยกประเภททั่วไปสำหรับบัญชีแยกประเภทสำหรับการลงบัญชีต้นทุน</span><span class="sxs-lookup"><span data-stu-id="dc915-104">Use this procedure to manage the general ledger data source for a cost accounting ledger.</span></span> <span data-ttu-id="dc915-105">ก่อนที่คุณจะทำงานนี้ให้เสร็จสมบูรณ์ ให้ตรวจสอบให้แน่ใจว่าคุณได้เล่นคู่มืองาน "สร้างบัญชีแยกประเภทสำหรับการลงบัญชีต้นทุน" และ "กำหนดหน่วยการควบคุมต้นทุน" แล้ว</span><span class="sxs-lookup"><span data-stu-id="dc915-105">Before you complete this task, make sure that you play the "Create a cost accounting ledger" and "Define cost control units" task guides.</span></span> <span data-ttu-id="dc915-106">การบันทึกข้อมูลนี้ใช้บริษัทข้อมูลสาธิต USP2</span><span class="sxs-lookup"><span data-stu-id="dc915-106">This recording uses the USP2 demo data company.</span></span>

1. <span data-ttu-id="dc915-107">ไปที่ บัญชีต้นทุน > การตั้งค่าบัญชีแยกประเภท > บัญชีแยกประเภทสำหรับการบัญชีต้นทุน</span><span class="sxs-lookup"><span data-stu-id="dc915-107">Go to Cost accounting > Ledger setup > Cost accounting ledgers.</span></span>
2. <span data-ttu-id="dc915-108">ในรายการนี้ ให้ค้นหาและเลือกเรกคอร์ดที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="dc915-108">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="dc915-109">คลิก เวอร์ชันจริง</span><span class="sxs-lookup"><span data-stu-id="dc915-109">Click Actual versions.</span></span>
4. <span data-ttu-id="dc915-110">ในบานหน้าต่างการดำเนินการ คลิก จัดการ</span><span class="sxs-lookup"><span data-stu-id="dc915-110">On the Action Pane, click Manage.</span></span>
5. <span data-ttu-id="dc915-111">คลิก บัญชีแยกประเภททั่วไป</span><span class="sxs-lookup"><span data-stu-id="dc915-111">Click General ledger.</span></span>
6. <span data-ttu-id="dc915-112">คลิก สร้าง</span><span class="sxs-lookup"><span data-stu-id="dc915-112">Click New.</span></span>
7. <span data-ttu-id="dc915-113">ในฟิลด์ชื่อ ให้พิมพ์ค่า </span><span class="sxs-lookup"><span data-stu-id="dc915-113">In the Name field, type a value.</span></span>
8. <span data-ttu-id="dc915-114">ในฟิลด์ตัวให้บริการข้อมูล ให้ป้อนหรือเลือกค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="dc915-114">In the Data provider field, enter or select a value.</span></span>
    * <span data-ttu-id="dc915-115">ตัวอย่างนี้ เลือก Dynamics 365 Finance - รายการบัญชีแยกประเภททั่วไป</span><span class="sxs-lookup"><span data-stu-id="dc915-115">For this example, select Dynamics 365 Finance - General ledger entries.</span></span>  
9. <span data-ttu-id="dc915-116">ในฟิลด์มิติองค์ประกอบต้นทุน ให้ป้อนหรือเลือกค่า</span><span class="sxs-lookup"><span data-stu-id="dc915-116">In the Cost element dimension field, enter or select a value.</span></span>
    * <span data-ttu-id="dc915-117">สำหรับตัวอย่างนี้ ให้เลือก องค์ประกอบต้นทุน</span><span class="sxs-lookup"><span data-stu-id="dc915-117">For this example, select Cost elements.</span></span>  
10. <span data-ttu-id="dc915-118">คลิก บันทึก</span><span class="sxs-lookup"><span data-stu-id="dc915-118">Click Save.</span></span>
11. <span data-ttu-id="dc915-119">คลิก ตั้งค่าคอนฟิกตัวให้บริการข้อมูล</span><span class="sxs-lookup"><span data-stu-id="dc915-119">Click Configure data provider.</span></span>
12. <span data-ttu-id="dc915-120">ในฟิลด์ นิติบุคคล ให้ป้อนหรือเลือกค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="dc915-120">In the Legal entity field, enter or select a value.</span></span>
    * <span data-ttu-id="dc915-121">สำหรับตัวอย่างนี้ ให้เลือก USP2</span><span class="sxs-lookup"><span data-stu-id="dc915-121">For this example, select USP2.</span></span>  
13. <span data-ttu-id="dc915-122">คลิก สร้าง</span><span class="sxs-lookup"><span data-stu-id="dc915-122">Click New.</span></span>
14. <span data-ttu-id="dc915-123">ในฟิลด์ ชั้นของการลงรายการบัญชี เลือกปัจจุบัน</span><span class="sxs-lookup"><span data-stu-id="dc915-123">In the Posting layer field, select Current.</span></span>
15. <span data-ttu-id="dc915-124">คลิก ตกลง</span><span class="sxs-lookup"><span data-stu-id="dc915-124">Click OK.</span></span>

