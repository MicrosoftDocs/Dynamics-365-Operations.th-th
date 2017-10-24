--- 
title: "บันทึกบัญชีในสมุดรายวันเกี่ยวกับรายการสมุดรายวันที่ลงรายการบัญชี"
description: "กระบวนงานนี้แสดงวิธีการบันทึกบัญชีในสมุดรายวันที่มีการลงรายการบัญชีรายการสมุดรายวัน "
author: aprilolson
manager: AnnBe
ms.date: 10/24/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Operations
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 490e9a4beda43f6e32b87792b11153c3e8e322d6
ms.contentlocale: th-th
ms.lasthandoff: 09/29/2017

---
# <a name="journalize-posted-journal-entries"></a><span data-ttu-id="7e327-103">บันทึกบัญชีในสมุดรายวันเกี่ยวกับรายการสมุดรายวันที่ลงรายการบัญชี</span><span class="sxs-lookup"><span data-stu-id="7e327-103">Journalize posted journal entries</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="7e327-104">กระบวนงานนี้แสดงวิธีการบันทึกบัญชีในสมุดรายวันที่มีการลงรายการบัญชีรายการสมุดรายวัน </span><span class="sxs-lookup"><span data-stu-id="7e327-104">This procedure shows how to journalize posted journal entries.</span></span> <span data-ttu-id="7e327-105">กระบวนงานนี้ใช้บริษัทข้อมูลสาธิต USMF</span><span class="sxs-lookup"><span data-stu-id="7e327-105">This procedure uses the USMF demo data company.</span></span>

1. <span data-ttu-id="7e327-106">ตรวจสอบการตั้งค่าสำหรับการบันทึกบัญชีในสมุดรายวันภายใต้พารามิเตอร์ บัญชีแยกประเภททั่วไป > การตั้งค่าบัญชีแยกประเภท > บัญชีแยกประเภททั่วไป</span><span class="sxs-lookup"><span data-stu-id="7e327-106">Validate the settings for journalizing under General ledger > Ledger setup > General ledger parameters.</span></span>
2. <span data-ttu-id="7e327-107">สามารถกำหนดฟิลด์สมุดรายวันของบัญชีแยกประเภทแบบขยายเป็น ใช่ หรือ ไม่</span><span class="sxs-lookup"><span data-stu-id="7e327-107">The Extended ledger journal field can be set to Yes or No.</span></span> <span data-ttu-id="7e327-108">ถ้าตั้งค่าเป็น ใช่ ผลลัพธ์รายงานจะแตกต่างกัน</span><span class="sxs-lookup"><span data-stu-id="7e327-108">If Yes, the report output will be different.</span></span>
3. <span data-ttu-id="7e327-109">เลือกว่าสามารถปิดรอบระยะเวลาได้หรือไม่ถ้ายังไม่มีการดำเนินกระบวนการบันทึกบัญชีสมุดรายวัน</span><span class="sxs-lookup"><span data-stu-id="7e327-109">Select whether the period can be closed if the journalizing process hasn't been run.</span></span>
    * <span data-ttu-id="7e327-110">ถ้าตัวเลือกนี้ตั้งค่าเป็น ใช่ จะไม่สามารถปิดรอบระยะเวลาได้จนกว่ากระบวนการบันทึกบัญชีในสมุดรายวันจะเสร็จสมบูรณ์สำหรับรอบระยะเวลานั้น</span><span class="sxs-lookup"><span data-stu-id="7e327-110">If this option is set to Yes, the period cannot be closed until the journalizing process has been completed for that period.</span></span>  
4. <span data-ttu-id="7e327-111">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="7e327-111">Close the page.</span></span>
5. <span data-ttu-id="7e327-112">ไปที่บัญชีแยกประเภททั่วไป > งานประจำงวด > การบันทึกบัญชีในสมุดรายวัน</span><span class="sxs-lookup"><span data-stu-id="7e327-112">Go to General ledger > Periodic tasks > Journalizing.</span></span>
6. <span data-ttu-id="7e327-113">คลิกตัวกรอง </span><span class="sxs-lookup"><span data-stu-id="7e327-113">Click Filter.</span></span>
7. <span data-ttu-id="7e327-114">เน้นแถวที่มีเกณฑ์ตัวกรองที่คุณต้องการกำหนด</span><span class="sxs-lookup"><span data-stu-id="7e327-114">Highlight the row with the filter criteria that you want to define.</span></span>
8. <span data-ttu-id="7e327-115">ในฟิลด์เกณฑ์ ให้ป้อนหรือเลือกเกณฑ์ตัวกรอง..</span><span class="sxs-lookup"><span data-stu-id="7e327-115">In the Criteria field, enter or select the filter criteria..</span></span>
9. <span data-ttu-id="7e327-116">คลิกตกลง เพื่อปิดหน้าตัวกรอง</span><span class="sxs-lookup"><span data-stu-id="7e327-116">Click OK to close the filter page.</span></span>
10. <span data-ttu-id="7e327-117">คลิก ตกลง เพื่อเริ่มต้นกระบวนการบันทึกบัญชีสมุดรายวัน</span><span class="sxs-lookup"><span data-stu-id="7e327-117">Click OK to start the journalizing process.</span></span>
    * <span data-ttu-id="7e327-118">ระบบจะสร้างรายงานหลังจากกระบวนการดังกล่าวเสร็จสมบูรณ์</span><span class="sxs-lookup"><span data-stu-id="7e327-118">A report will be generated after the process is complete.</span></span>  


