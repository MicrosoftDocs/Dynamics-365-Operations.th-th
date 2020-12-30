---
title: บันทึกบัญชีในสมุดรายวันเกี่ยวกับรายการสมุดรายวันที่ลงรายการบัญชี
description: 'กระบวนงานนี้แสดงวิธีการบันทึกบัญชีในสมุดรายวันที่มีการลงรายการบัญชีรายการสมุดรายวัน '
author: aprilolson
manager: AnnBe
ms.date: 08/09/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerParameters, SysQueryForm
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: f50ee568df492bcd811d2fefb1784bb55b50384b
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 10/13/2020
ms.locfileid: "4448340"
---
# <a name="journalize-posted-journal-entries"></a><span data-ttu-id="73226-103">บันทึกบัญชีในสมุดรายวันเกี่ยวกับรายการสมุดรายวันที่ลงรายการบัญชี</span><span class="sxs-lookup"><span data-stu-id="73226-103">Journalize posted journal entries</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="73226-104">กระบวนงานนี้แสดงวิธีการบันทึกบัญชีในสมุดรายวันที่มีการลงรายการบัญชีรายการสมุดรายวัน </span><span class="sxs-lookup"><span data-stu-id="73226-104">This procedure shows how to journalize posted journal entries.</span></span> <span data-ttu-id="73226-105">กระบวนงานนี้ใช้บริษัทข้อมูลสาธิต USMF</span><span class="sxs-lookup"><span data-stu-id="73226-105">This procedure uses the USMF demo data company.</span></span>

1. <span data-ttu-id="73226-106">ใน **บานหน้าต่างนำทาง** ไปที่ **โมดูล > บัญชีแยกประเภททั่วไป > การตั้งค่าบัญชีแยกประเภท > พารามิเตอร์บัญชีแยกประเภททั่วไป**</span><span class="sxs-lookup"><span data-stu-id="73226-106">In the **Navigation pane**, go to **Modules > General ledger > Ledger setup > General ledger parameters**.</span></span>
2. <span data-ttu-id="73226-107">สามารถตั้งค่าฟิลด์ **สมุดรายวันของบัญชีแยกประเภทแบบขยาย** เป็น ใช่ หรือ ไม่</span><span class="sxs-lookup"><span data-stu-id="73226-107">The **Extended ledger journal** field can be set to Yes or No.</span></span> <span data-ttu-id="73226-108">ถ้าตั้งค่าเป็น ใช่ ผลลัพธ์รายงานจะแตกต่างกัน</span><span class="sxs-lookup"><span data-stu-id="73226-108">If Yes, the report output will be different.</span></span>
3. <span data-ttu-id="73226-109">เลือกว่าสามารถปิดรอบระยะเวลาได้หรือไม่ถ้ายังไม่มีการดำเนินกระบวนการบันทึกบัญชีสมุดรายวัน</span><span class="sxs-lookup"><span data-stu-id="73226-109">Select whether the period can be closed if the journalizing process hasn't been run.</span></span> <span data-ttu-id="73226-110">ถ้าตัวเลือกนี้ตั้งค่าเป็น ใช่ จะไม่สามารถปิดรอบระยะเวลาได้จนกว่ากระบวนการบันทึกบัญชีในสมุดรายวันจะเสร็จสมบูรณ์สำหรับรอบระยะเวลานั้น</span><span class="sxs-lookup"><span data-stu-id="73226-110">If this option is set to Yes, the period cannot be closed until the journalizing process has been completed for that period.</span></span>  
4. <span data-ttu-id="73226-111">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="73226-111">Close the page.</span></span>
5. <span data-ttu-id="73226-112">ใน **บานหน้าต่างนำทาง** ไปที่ **โมดูล > บัญชีแยกประเภททั่วไป > งานประจำงวด > การบันทึกบัญชีในสมุดรายวัน**</span><span class="sxs-lookup"><span data-stu-id="73226-112">In the **Navigation pane**, go to **Modules > General ledger > Periodic tasks > Journalizing**.</span></span>
6. <span data-ttu-id="73226-113">คลิก **ตัวกรอง**</span><span class="sxs-lookup"><span data-stu-id="73226-113">Click **Filter**.</span></span>
7. <span data-ttu-id="73226-114">เน้นแถวที่มีเกณฑ์ตัวกรองที่คุณต้องการกำหนด</span><span class="sxs-lookup"><span data-stu-id="73226-114">Highlight the row with the filter criteria that you want to define.</span></span>
8. <span data-ttu-id="73226-115">ในฟิลด์ **เกณฑ์** ให้ป้อนหรือเลือกเกณฑ์ตัวกรอง..</span><span class="sxs-lookup"><span data-stu-id="73226-115">In the **Criteria** field, enter or select the filter criteria..</span></span>
9. <span data-ttu-id="73226-116">คลิก **ตกลง** เพื่อปิดหน้าตัวกรอง</span><span class="sxs-lookup"><span data-stu-id="73226-116">Click **OK** to close the filter page.</span></span>
10. <span data-ttu-id="73226-117">คลิก **ตกลง** เพื่อเริ่มต้นกระบวนการบันทึกบัญชีในสมุดรายวัน</span><span class="sxs-lookup"><span data-stu-id="73226-117">Click **OK** to start the journalizing process.</span></span> <span data-ttu-id="73226-118">ระบบจะสร้างรายงานหลังจากกระบวนการดังกล่าวเสร็จสมบูรณ์</span><span class="sxs-lookup"><span data-stu-id="73226-118">A report will be generated after the process is complete.</span></span>  

