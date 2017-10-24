--- 
title: "ตั้งค่าชนิดเอกสาร I-9"
description: "ขั้นตอนนี้แสดงวิธีการดูและตั้งค่าชนิดเอกสารที่จะใช้สำหรับการตรวจสอบ I-9 "
author: ShielaSogge
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: rschloma
ms.search.scope: Operations
ms.search.region: Global
ms.author: shielas
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 3b0e7f09994367f5683ed5c6d1f3b3ba3d550cc7
ms.contentlocale: th-th
ms.lasthandoff: 09/29/2017

---
# <a name="set-up-i-9-document-types"></a><span data-ttu-id="d0f3d-103">ตั้งค่าชนิดเอกสาร I-9</span><span class="sxs-lookup"><span data-stu-id="d0f3d-103">Set up I-9 document types</span></span>

[!include[task guide banner](../../../includes/task-guide-banner.md)]

<span data-ttu-id="d0f3d-104">ขั้นตอนนี้แสดงวิธีการดูและตั้งค่าชนิดเอกสารที่จะใช้สำหรับการตรวจสอบ I-9 </span><span class="sxs-lookup"><span data-stu-id="d0f3d-104">This procedure shows how to view and set up document types that are used for I-9 verification.</span></span> <span data-ttu-id="d0f3d-105">ก่อนที่คุณตั้งค่าชนิดเอกสาร I-9 คุณต้องตั้งค่าหน่วยงานที่ออกเอกสารและชนิดข้อมูลประจำตัว </span><span class="sxs-lookup"><span data-stu-id="d0f3d-105">Before you set up I-9 document types, you must also set up the issuing agencies and identification types.</span></span> <span data-ttu-id="d0f3d-106">บริษัทข้อมูลสาธิตเคยสร้างขั้นตอนนี้คือ USMF ซึ่งรวมตัวอย่างของหน่วยงานที่ออกเอกสารและชนิดข้อมูลประจำตัวที่จำเป็นสำหรับใช้ดำเนินการขั้นตอนให้เสร็จสมบูรณ์ไว้ด้วย</span><span class="sxs-lookup"><span data-stu-id="d0f3d-106">The demo data company used to create this procedure is USMF, which includes examples of the issue agencies and identification types that are needed to complete the procedure.</span></span>

1. <span data-ttu-id="d0f3d-107">ไปที่ทรัพยากรบุคคล > ผู้ปฏิบัติงาน > I-9 > ชนิดเอกสาร I-9</span><span class="sxs-lookup"><span data-stu-id="d0f3d-107">Go to Human resources > Workers > I-9 > I-9 document types.</span></span>
2. <span data-ttu-id="d0f3d-108">คลิก สร้าง</span><span class="sxs-lookup"><span data-stu-id="d0f3d-108">Click New.</span></span>
3. <span data-ttu-id="d0f3d-109">ในฟิลด์ชนิดเอกสาร I-9 ให้พิมพ์ค่า</span><span class="sxs-lookup"><span data-stu-id="d0f3d-109">In the I-9 document type field, type a value.</span></span>
    * <span data-ttu-id="d0f3d-110">ตัวอย่าง: รหัสโรงเรียน</span><span class="sxs-lookup"><span data-stu-id="d0f3d-110">Example: School ID.</span></span>  
4. <span data-ttu-id="d0f3d-111">เลือกชนิดการยืนยันตัวตน </span><span class="sxs-lookup"><span data-stu-id="d0f3d-111">Select the identification type.</span></span>  <span data-ttu-id="d0f3d-112">ตัวอย่าง: รหัสโรงเรียน</span><span class="sxs-lookup"><span data-stu-id="d0f3d-112">Example:  School ID</span></span>
    * <span data-ttu-id="d0f3d-113">ตัวอย่างของชนิดการยืนยันตัวตนรวมถึงหมายเลขประกันสังคม (SSN), หมายเลขวีซ่า รหัส passport หรือใบอนุญาตขับขี่รถยนต์ด้วย</span><span class="sxs-lookup"><span data-stu-id="d0f3d-113">Examples of identification types include a Social Security number (SSN), visa number, passport ID, or driver's licence.</span></span>  
5. <span data-ttu-id="d0f3d-114">เลือกรายการเอกสาร I-9 ที่ใช้สำหรับชนิดเอกสาร</span><span class="sxs-lookup"><span data-stu-id="d0f3d-114">Select the I-9 document list that is used for the document type.</span></span>
    * <span data-ttu-id="d0f3d-115">เนื่องจากเป็นส่วนหนึ่งของกระบวนการ I-9 พนักงานต้องแสดงเอกสารที่แสดงถึงการชี้บ่งข้อมูลประจำตัวและการตรวจสอบการจ้างงาน </span><span class="sxs-lookup"><span data-stu-id="d0f3d-115">As part of the I-9 process, employees must present documentation that shows the employer their identity and employment authorization.</span></span> <span data-ttu-id="d0f3d-116">เว็บไซต์ที่ให้บริการข้อมูลการอพยพและการเป็นพลเมืองอเมริกันมีข้อมูลเกี่ยวกับเอกสารที่เป็นที่ยอมรับ และข้อมูลนั้นเป็นของรายการใด</span><span class="sxs-lookup"><span data-stu-id="d0f3d-116">The US Citizenship and Immigration Services website contains information about which documents are acceptable, and which list they belong to.</span></span>  <span data-ttu-id="d0f3d-117">http://www.uscis.gov</span><span class="sxs-lookup"><span data-stu-id="d0f3d-117">http://www.uscis.gov</span></span>  
6. <span data-ttu-id="d0f3d-118">ในฟิลด์แบบฟอร์ม ป้อนหมายเลขแบบฟอร์มอย่างเป็นทางการสำหรับชนิดเอกสาร </span><span class="sxs-lookup"><span data-stu-id="d0f3d-118">In the Form field, Enter the official form number for the document type.</span></span> <span data-ttu-id="d0f3d-119">ตัวอย่าง: รหัสโรงเรียน</span><span class="sxs-lookup"><span data-stu-id="d0f3d-119">Example: School ID.</span></span>
    * <span data-ttu-id="d0f3d-120">สามารถพบหมายเลขแบบฟอร์มที่เป็นทางการในเว็บไซต์ที่ให้บริการการอพยพและการเป็นพลเมืองอเมริกัน</span><span class="sxs-lookup"><span data-stu-id="d0f3d-120">The official form numbers can be found on the US Citizenship and Immigration Services website.</span></span>  <span data-ttu-id="d0f3d-121">http://www.uscis.gov</span><span class="sxs-lookup"><span data-stu-id="d0f3d-121">http://www.uscis.gov</span></span>  
7. <span data-ttu-id="d0f3d-122">เลือกหรือยกเลิกการเลือกกล่องกาเครื่องหมายแอคทีฟ </span><span class="sxs-lookup"><span data-stu-id="d0f3d-122">Check or uncheck the Active checkbox.</span></span>
8. <span data-ttu-id="d0f3d-123">ในฟิลด์หมดอายุ ตั้งค่าวันที่เป็น ' 2019-10-27'</span><span class="sxs-lookup"><span data-stu-id="d0f3d-123">In the Expire field, set the date to '2019-10-27'.</span></span>
    * <span data-ttu-id="d0f3d-124">วันหมดอายุเป็นตัวเลือก</span><span class="sxs-lookup"><span data-stu-id="d0f3d-124">The expiration date is optional.</span></span>  
9. <span data-ttu-id="d0f3d-125">เลือกหน่วยงานที่ออกชนิดเอกสาร </span><span class="sxs-lookup"><span data-stu-id="d0f3d-125">Select the agency that issued the document type.</span></span> <span data-ttu-id="d0f3d-126">ตัวอย่าง: จังหวัด/เขต</span><span class="sxs-lookup"><span data-stu-id="d0f3d-126">Example: Province/territory</span></span>
10. <span data-ttu-id="d0f3d-127">คลิก บันทึก</span><span class="sxs-lookup"><span data-stu-id="d0f3d-127">Click Save.</span></span>


