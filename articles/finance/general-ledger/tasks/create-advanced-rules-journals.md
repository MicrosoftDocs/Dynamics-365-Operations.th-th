---
title: สร้างกฎขั้นสูงสำหรับสมุดรายวัน
description: 'กระบวนงานนี้ดำเนินการสร้างกฎขั้นสูงสำหรับสมุดรายวัน '
author: aprilolson
ms.date: 08/08/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: LedgerJournalSetup, LedgerJournalControl, CompanyLookup, LedgerJournalPostControl
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: cd753d521dc4ad4c1e46bf51d9c1e4aa0ba02721
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 04/01/2021
ms.locfileid: "5832813"
---
# <a name="create-advanced-rules-for-journals"></a><span data-ttu-id="74cbd-103">สร้างกฎขั้นสูงสำหรับสมุดรายวัน</span><span class="sxs-lookup"><span data-stu-id="74cbd-103">Create advanced rules for journals</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="74cbd-104">กระบวนงานนี้ดำเนินการสร้างกฎขั้นสูงสำหรับสมุดรายวัน </span><span class="sxs-lookup"><span data-stu-id="74cbd-104">This procedure steps through creating advanced rules for journals.</span></span> <span data-ttu-id="74cbd-105">ซึ่งรวมถึงการตั้งค่าการควบคุมสมุดรายวันและข้อจำกัดในการลงรายการบัญชีของผู้ใช้ </span><span class="sxs-lookup"><span data-stu-id="74cbd-105">This includes setting up journal control and user posting restrictions.</span></span> <span data-ttu-id="74cbd-106">กระบวนงานนี้ใช้บริษัทข้อมูลสาธิต USMF</span><span class="sxs-lookup"><span data-stu-id="74cbd-106">This procedure uses the USMF demo data company.</span></span>


## <a name="set-up-journal-control"></a><span data-ttu-id="74cbd-107">ตั้งค่าการควบคุมสมุดรายวัน</span><span class="sxs-lookup"><span data-stu-id="74cbd-107">Set up journal control</span></span>
1. <span data-ttu-id="74cbd-108">ใน **บานหน้าต่างนำทาง** ไปที่ **โมดูล > บัญชีแยกประเภททั่วไป > การตั้งค่าสมุดรายวัน > ชื่อสมุดรายวัน**</span><span class="sxs-lookup"><span data-stu-id="74cbd-108">In the **Navigation pane**, go to **Modules > General ledger > Journal setup > Journal names**.</span></span>
2. <span data-ttu-id="74cbd-109">ในรายการนี้ ให้ค้นหาและเลือกเรกคอร์ดที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="74cbd-109">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="74cbd-110">บน **บานหน้าต่างการดำเนินการ** ให้คลิก **การควบคุมสมุดรายวัน**</span><span class="sxs-lookup"><span data-stu-id="74cbd-110">On the **Action pane**, click **Journal control**.</span></span>
4. <span data-ttu-id="74cbd-111">ใน fastTab **ชนิดบัญชีที่สามารถลงรายการบัญชีได้** ให้คลิก **เพิ่ม**</span><span class="sxs-lookup"><span data-stu-id="74cbd-111">In the **Which account types can be posted** fastTab, click **Add**.</span></span>
5. <span data-ttu-id="74cbd-112">ในฟิลด์ **บัญชีบริษัท** ให้คลิกปุ่มดรอปดาวน์เพื่อเปิดการค้นหา</span><span class="sxs-lookup"><span data-stu-id="74cbd-112">In the **Company accounts** field, click the drop-down button to open the lookup.</span></span>
6. <span data-ttu-id="74cbd-113">ในรายการนี้ ให้ค้นหาและเลือกเรกคอร์ดที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="74cbd-113">In the list, find and select the desired record.</span></span>
7. <span data-ttu-id="74cbd-114">ในรายการนี้ ให้คลิกลิงค์ในแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="74cbd-114">In the list, click the link in the selected row.</span></span>
8. <span data-ttu-id="74cbd-115">ใน fastTab **ค่าเซ็กเมนต์ที่มีผลบังคับใช้สำหรับสมุดรายวันนี้** คลิก **เพิ่ม**</span><span class="sxs-lookup"><span data-stu-id="74cbd-115">In the **Which segment values are valid for this journal** fastTab, click **Add**.</span></span>
9. <span data-ttu-id="74cbd-116">ในฟิลด์ **โครงสร้างทางบัญชี** ให้คลิกปุ่มดรอปดาวน์เพื่อเปิดการค้นหา</span><span class="sxs-lookup"><span data-stu-id="74cbd-116">In the **Account structure** field, click the drop-down button to open the lookup.</span></span>
10. <span data-ttu-id="74cbd-117">ในรายการนี้ ให้ค้นหาและเลือกเรกคอร์ดที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="74cbd-117">In the list, find and select the desired record.</span></span>
11. <span data-ttu-id="74cbd-118">ในรายการนี้ ให้คลิกลิงค์ในแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="74cbd-118">In the list, click the link in the selected row.</span></span>
12. <span data-ttu-id="74cbd-119">ในฟิลด์ **เซ็กเมนต์** ให้คลิกปุ่มดรอปดาวน์เพื่อเปิดการค้นหา</span><span class="sxs-lookup"><span data-stu-id="74cbd-119">In the **Segment** field, click the drop-down button to open the lookup.</span></span>
13. <span data-ttu-id="74cbd-120">ในรายการนี้ ให้คลิกลิงค์ในแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="74cbd-120">In the list, click the link in the selected row.</span></span>
14. <span data-ttu-id="74cbd-121">ในฟิลด์ **จากค่า** ให้คลิกปุ่มดรอปดาวน์เพื่อเปิดการค้นหา</span><span class="sxs-lookup"><span data-stu-id="74cbd-121">In the **From value** field, click the drop-down button to open the lookup.</span></span>
15. <span data-ttu-id="74cbd-122">ในรายการนี้ ให้ค้นหาและเลือกเรกคอร์ดที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="74cbd-122">In the list, find and select the desired record.</span></span>
16. <span data-ttu-id="74cbd-123">ในรายการนี้ ให้คลิกลิงค์ในแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="74cbd-123">In the list, click the link in the selected row.</span></span>
17. <span data-ttu-id="74cbd-124">ในฟิลด์ **ไปที่ค่า** ให้คลิกปุ่มดรอปดาวน์เพื่อเปิดการค้นหา</span><span class="sxs-lookup"><span data-stu-id="74cbd-124">In the **To value** field, click the drop-down button to open the lookup.</span></span>
18. <span data-ttu-id="74cbd-125">ในรายการนี้ ให้ค้นหาและเลือกเรกคอร์ดที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="74cbd-125">In the list, find and select the desired record.</span></span>
19. <span data-ttu-id="74cbd-126">ในรายการนี้ ให้คลิกลิงค์ในแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="74cbd-126">In the list, click the link in the selected row.</span></span>

## <a name="set-up-posting-restrictions"></a><span data-ttu-id="74cbd-127">การตั้งค่าข้อจำกัดการลงรายการบัญชี</span><span class="sxs-lookup"><span data-stu-id="74cbd-127">Set up posting restrictions</span></span>
1. <span data-ttu-id="74cbd-128">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="74cbd-128">Close the page.</span></span>
2. <span data-ttu-id="74cbd-129">คลิก **ข้อจำกัดในการลงรายการบัญชี**</span><span class="sxs-lookup"><span data-stu-id="74cbd-129">Click **Posting restrictions**.</span></span>
3. <span data-ttu-id="74cbd-130">ใน **คุณต้องการตั้งค่าข้อจำกัดในการลงรายการบัญชีอย่างไร** ให้เลือก 'โดยกลุ่มผู้ใช้'</span><span class="sxs-lookup"><span data-stu-id="74cbd-130">In the **How do you want to set up posting restrictions** field, select 'By user group'.</span></span>
4. <span data-ttu-id="74cbd-131">ในแผนภูมิ ให้ตรวจสอบ 'กลุ่มที่คุณต้องการอนุญาตให้มีการลงรายการบัญชีสำหรับชื่อสมุดรายวัน'</span><span class="sxs-lookup"><span data-stu-id="74cbd-131">In the tree, check 'the group that you want to allow posting for this journal name.'.</span></span>
5. <span data-ttu-id="74cbd-132">คลิก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="74cbd-132">Click **OK**.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]