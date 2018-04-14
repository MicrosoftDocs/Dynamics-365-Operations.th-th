--- 
title: "ตั้งค่าลำดับหมายเลขโดยใช้วิซาร์ด"
description: "ลำดับหมายเลขถูกใช้ในการสร้างรหัสที่สามารถอ่านได้ รหัสเฉพาะสำหรับเร็กคอร์ดข้อมูลหลักและเรกคอร์ดธุรกรรมที่ต้องการ "
author: sericks007
manager: AnnBe
ms.date: 11/10/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: sericks
ms.search.scope: Operations
ms.search.region: Global
ms.author: sericks
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: e7d988cd1261c00925ad7ae612a947a0083028ee
ms.contentlocale: th-th
ms.lasthandoff: 04/13/2018

---
# <a name="set-up-number-sequences-by-using-a-wizard"></a><span data-ttu-id="43626-103">ตั้งค่าลำดับหมายเลขโดยใช้วิซาร์ด</span><span class="sxs-lookup"><span data-stu-id="43626-103">Set up number sequences by using a wizard</span></span>

[!INCLUDE [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="43626-104">ลำดับหมายเลขถูกใช้ในการสร้างรหัสที่สามารถอ่านได้ รหัสเฉพาะสำหรับเร็กคอร์ดข้อมูลหลักและเรกคอร์ดธุรกรรมที่ต้องการ </span><span class="sxs-lookup"><span data-stu-id="43626-104">Number sequences are used to generate readable, unique identifiers for master data records and transaction records that require them.</span></span> <span data-ttu-id="43626-105">ข้อมูลหลักหรือเรกคอร์ดธุรกรรมที่จำเป็นต้องมีตัวระบุจะอ้างเป็นการอ้างอิง</span><span class="sxs-lookup"><span data-stu-id="43626-105">A master data or transaction record that requires an identifier is referred to as a reference.</span></span> <span data-ttu-id="43626-106">ก่อนที่คุณจะสามารถสร้างเรกคอร์ดใหม่สำหรับการอ้างอิง คุณต้องตั้งค่าลำดับหมายเลขและเชื่อมโยงกับการอ้างอิงนั้น </span><span class="sxs-lookup"><span data-stu-id="43626-106">Before you can create new records for a reference, you must set up a number sequence and associate it with the reference.</span></span> <span data-ttu-id="43626-107">ขั้นตอนนี้อธิบายวิธีการตั้งค่าลำดับหมายเลขที่จำเป็นทั้งหมดพร้อมกันโดยใช้วิซาร์ด </span><span class="sxs-lookup"><span data-stu-id="43626-107">This procedure explains how to set up all required number sequences at the same time by using a wizard.</span></span> <span data-ttu-id="43626-108">ข้อมูลบริษัทสาธิตที่ใช้ในการสร้างกระบวนงานนี้คือ USMF</span><span class="sxs-lookup"><span data-stu-id="43626-108">The demo data company used to create this procedure is USMF.</span></span>

1. <span data-ttu-id="43626-109">ไปที่จัดการองค์กร > ลำดับหมายเลข > ลำดับหมายเลข</span><span class="sxs-lookup"><span data-stu-id="43626-109">Go to Organization administration > Number sequences > Number sequences.</span></span>
2. <span data-ttu-id="43626-110">คลิก สร้าง</span><span class="sxs-lookup"><span data-stu-id="43626-110">Click Generate.</span></span>
3. <span data-ttu-id="43626-111">คลิก ถัดไป</span><span class="sxs-lookup"><span data-stu-id="43626-111">Click Next.</span></span>
    * <span data-ttu-id="43626-112">บนหน้านี้คุณจะสามารถแก้ไขรหัสประจำตัว ค่าต่ำสุดและค่าสูงสุดได้</span><span class="sxs-lookup"><span data-stu-id="43626-112">On this page, you can modify the identification code, the lowest value, and the highest value.</span></span> <span data-ttu-id="43626-113">นอกจากนี้คุณยังสามารถระบุได้ว่าลำดับหมายเลขต้องต่อเนื่องกันหรือไม่</span><span class="sxs-lookup"><span data-stu-id="43626-113">In addition, you can indicate whether the number sequence must be continuous.</span></span>   
    * <span data-ttu-id="43626-114">อย่าเลือกตัวเลือกต่อเนื่องถ้าคุณต้องปันส่วนหมายเลขล่วงหน้าสำหรับลำดับหมายเลข </span><span class="sxs-lookup"><span data-stu-id="43626-114">Do not select the Continuous option if you must preallocate numbers for the number sequence.</span></span>     <span data-ttu-id="43626-115">เมื่อต้องการเพิ่มเซ็กเมนต์ขอบเขตในรูปแบบลำดับหมายเลขให้เลือกรูปแบบในรายการจากนั้นคลิก รวมขอบเขตในรูปแบบ </span><span class="sxs-lookup"><span data-stu-id="43626-115">To add a scope segment to the format of a number sequence, select the format in the list, and then click Include scope in format.</span></span>     <span data-ttu-id="43626-116">การลบเซ็กเมนต์ขอบเขตออกจากรูปแบบของลำดับหมายเลขให้เลือกรูปแบบในรายการ จากนั้นคลิกลบขอบเขตออกจากรูปแบบ </span><span class="sxs-lookup"><span data-stu-id="43626-116">To remove a scope segment from the format of a number sequence, select the format in the list, and then click Remove scope from format.</span></span>     <span data-ttu-id="43626-117">การไม่รวมลำดับหมายเลขจากการสร้างโดยอัตโนมัติ ให้เลือกลำดับหมายเลขในรายการจากนั้นคลิกลบ</span><span class="sxs-lookup"><span data-stu-id="43626-117">To exclude a number sequence from automatic generation, select the number sequence in the list, and then click Delete.</span></span>  
4. <span data-ttu-id="43626-118">คลิก ถัดไป</span><span class="sxs-lookup"><span data-stu-id="43626-118">Click Next.</span></span>
5. <span data-ttu-id="43626-119">คลิก Finish</span><span class="sxs-lookup"><span data-stu-id="43626-119">Click Finish.</span></span>


