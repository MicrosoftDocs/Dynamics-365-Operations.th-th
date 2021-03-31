---
title: สร้างกฎขั้นสูงสำหรับสมุดรายวัน
description: 'กระบวนงานนี้ดำเนินการสร้างกฎขั้นสูงสำหรับสมุดรายวัน '
author: aprilolson
manager: AnnBe
ms.date: 08/08/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerJournalSetup, LedgerJournalControl, CompanyLookup, LedgerJournalPostControl
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: e61ed731c4040e7351e20421f6cf217ae9a4641d
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 02/15/2021
ms.locfileid: "5222370"
---
# <a name="create-advanced-rules-for-journals"></a><span data-ttu-id="73fcb-103">สร้างกฎขั้นสูงสำหรับสมุดรายวัน</span><span class="sxs-lookup"><span data-stu-id="73fcb-103">Create advanced rules for journals</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="73fcb-104">กระบวนงานนี้ดำเนินการสร้างกฎขั้นสูงสำหรับสมุดรายวัน </span><span class="sxs-lookup"><span data-stu-id="73fcb-104">This procedure steps through creating advanced rules for journals.</span></span> <span data-ttu-id="73fcb-105">ซึ่งรวมถึงการตั้งค่าการควบคุมสมุดรายวันและข้อจำกัดในการลงรายการบัญชีของผู้ใช้ </span><span class="sxs-lookup"><span data-stu-id="73fcb-105">This includes setting up journal control and user posting restrictions.</span></span> <span data-ttu-id="73fcb-106">กระบวนงานนี้ใช้บริษัทข้อมูลสาธิต USMF</span><span class="sxs-lookup"><span data-stu-id="73fcb-106">This procedure uses the USMF demo data company.</span></span>


## <a name="set-up-journal-control"></a><span data-ttu-id="73fcb-107">ตั้งค่าการควบคุมสมุดรายวัน</span><span class="sxs-lookup"><span data-stu-id="73fcb-107">Set up journal control</span></span>
1. <span data-ttu-id="73fcb-108">ใน **บานหน้าต่างนำทาง** ไปที่ **โมดูล > บัญชีแยกประเภททั่วไป > การตั้งค่าสมุดรายวัน > ชื่อสมุดรายวัน**</span><span class="sxs-lookup"><span data-stu-id="73fcb-108">In the **Navigation pane**, go to **Modules > General ledger > Journal setup > Journal names**.</span></span>
2. <span data-ttu-id="73fcb-109">ในรายการนี้ ให้ค้นหาและเลือกเรกคอร์ดที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="73fcb-109">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="73fcb-110">บน **บานหน้าต่างการดำเนินการ** ให้คลิก **การควบคุมสมุดรายวัน**</span><span class="sxs-lookup"><span data-stu-id="73fcb-110">On the **Action pane**, click **Journal control**.</span></span>
4. <span data-ttu-id="73fcb-111">ใน fastTab **ชนิดบัญชีที่สามารถลงรายการบัญชีได้** ให้คลิก **เพิ่ม**</span><span class="sxs-lookup"><span data-stu-id="73fcb-111">In the **Which account types can be posted** fastTab, click **Add**.</span></span>
5. <span data-ttu-id="73fcb-112">ในฟิลด์ **บัญชีบริษัท** ให้คลิกปุ่มดรอปดาวน์เพื่อเปิดการค้นหา</span><span class="sxs-lookup"><span data-stu-id="73fcb-112">In the **Company accounts** field, click the drop-down button to open the lookup.</span></span>
6. <span data-ttu-id="73fcb-113">ในรายการนี้ ให้ค้นหาและเลือกเรกคอร์ดที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="73fcb-113">In the list, find and select the desired record.</span></span>
7. <span data-ttu-id="73fcb-114">ในรายการนี้ ให้คลิกลิงค์ในแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="73fcb-114">In the list, click the link in the selected row.</span></span>
8. <span data-ttu-id="73fcb-115">ใน fastTab **ค่าเซ็กเมนต์ที่มีผลบังคับใช้สำหรับสมุดรายวันนี้** คลิก **เพิ่ม**</span><span class="sxs-lookup"><span data-stu-id="73fcb-115">In the **Which segment values are valid for this journal** fastTab, click **Add**.</span></span>
9. <span data-ttu-id="73fcb-116">ในฟิลด์ **โครงสร้างทางบัญชี** ให้คลิกปุ่มดรอปดาวน์เพื่อเปิดการค้นหา</span><span class="sxs-lookup"><span data-stu-id="73fcb-116">In the **Account structure** field, click the drop-down button to open the lookup.</span></span>
10. <span data-ttu-id="73fcb-117">ในรายการนี้ ให้ค้นหาและเลือกเรกคอร์ดที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="73fcb-117">In the list, find and select the desired record.</span></span>
11. <span data-ttu-id="73fcb-118">ในรายการนี้ ให้คลิกลิงค์ในแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="73fcb-118">In the list, click the link in the selected row.</span></span>
12. <span data-ttu-id="73fcb-119">ในฟิลด์ **เซ็กเมนต์** ให้คลิกปุ่มดรอปดาวน์เพื่อเปิดการค้นหา</span><span class="sxs-lookup"><span data-stu-id="73fcb-119">In the **Segment** field, click the drop-down button to open the lookup.</span></span>
13. <span data-ttu-id="73fcb-120">ในรายการนี้ ให้คลิกลิงค์ในแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="73fcb-120">In the list, click the link in the selected row.</span></span>
14. <span data-ttu-id="73fcb-121">ในฟิลด์ **จากค่า** ให้คลิกปุ่มดรอปดาวน์เพื่อเปิดการค้นหา</span><span class="sxs-lookup"><span data-stu-id="73fcb-121">In the **From value** field, click the drop-down button to open the lookup.</span></span>
15. <span data-ttu-id="73fcb-122">ในรายการนี้ ให้ค้นหาและเลือกเรกคอร์ดที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="73fcb-122">In the list, find and select the desired record.</span></span>
16. <span data-ttu-id="73fcb-123">ในรายการนี้ ให้คลิกลิงค์ในแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="73fcb-123">In the list, click the link in the selected row.</span></span>
17. <span data-ttu-id="73fcb-124">ในฟิลด์ **ไปที่ค่า** ให้คลิกปุ่มดรอปดาวน์เพื่อเปิดการค้นหา</span><span class="sxs-lookup"><span data-stu-id="73fcb-124">In the **To value** field, click the drop-down button to open the lookup.</span></span>
18. <span data-ttu-id="73fcb-125">ในรายการนี้ ให้ค้นหาและเลือกเรกคอร์ดที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="73fcb-125">In the list, find and select the desired record.</span></span>
19. <span data-ttu-id="73fcb-126">ในรายการนี้ ให้คลิกลิงค์ในแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="73fcb-126">In the list, click the link in the selected row.</span></span>

## <a name="set-up-posting-restrictions"></a><span data-ttu-id="73fcb-127">การตั้งค่าข้อจำกัดการลงรายการบัญชี</span><span class="sxs-lookup"><span data-stu-id="73fcb-127">Set up posting restrictions</span></span>
1. <span data-ttu-id="73fcb-128">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="73fcb-128">Close the page.</span></span>
2. <span data-ttu-id="73fcb-129">คลิก **ข้อจำกัดในการลงรายการบัญชี**</span><span class="sxs-lookup"><span data-stu-id="73fcb-129">Click **Posting restrictions**.</span></span>
3. <span data-ttu-id="73fcb-130">ใน **คุณต้องการตั้งค่าข้อจำกัดในการลงรายการบัญชีอย่างไร** ให้เลือก 'โดยกลุ่มผู้ใช้'</span><span class="sxs-lookup"><span data-stu-id="73fcb-130">In the **How do you want to set up posting restrictions** field, select 'By user group'.</span></span>
4. <span data-ttu-id="73fcb-131">ในแผนภูมิ ให้ตรวจสอบ 'กลุ่มที่คุณต้องการอนุญาตให้มีการลงรายการบัญชีสำหรับชื่อสมุดรายวัน'</span><span class="sxs-lookup"><span data-stu-id="73fcb-131">In the tree, check 'the group that you want to allow posting for this journal name.'.</span></span>
5. <span data-ttu-id="73fcb-132">คลิก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="73fcb-132">Click **OK**.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]