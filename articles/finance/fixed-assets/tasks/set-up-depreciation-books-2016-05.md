---
title: ตั้งค่าสมุดบัญชีค่าเสื่อมราคา
description: กระบวนงานนี้นำไปสู่กระบวนการสร้างสมุดบัญชีค่าเสื่อมราคาใหม่และเชื่อมโยงกับกลุ่มสินทรัพย์ถาวร
author: saraschi2
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: AssetDepBookTable, AssetGroupDepBookSetup
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: b0ab7f9332e3224c3dadd62aae532ccffb05c82a
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 04/01/2021
ms.locfileid: "5815607"
---
# <a name="set-up-depreciation-books"></a><span data-ttu-id="bdbba-103">ตั้งค่าสมุดบัญชีค่าเสื่อมราคา</span><span class="sxs-lookup"><span data-stu-id="bdbba-103">Set up depreciation books</span></span> 

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="bdbba-104">กระบวนงานนี้นำไปสู่กระบวนการสร้างสมุดบัญชีค่าเสื่อมราคาใหม่และเชื่อมโยงกับกลุ่มสินทรัพย์ถาวร</span><span class="sxs-lookup"><span data-stu-id="bdbba-104">This procedure walks through the process of creating a new depreciation book and associate it with a fixed asset group.</span></span> 

## <a name="create-a-depreciation-book"></a><span data-ttu-id="bdbba-105">สร้างสมุดบัญชีค่าเสื่อมราคา</span><span class="sxs-lookup"><span data-stu-id="bdbba-105">Create a depreciation book</span></span>
1. <span data-ttu-id="bdbba-106">ไปที่สินทรัพย์ถาวร > การติดตั้ง > สมุดบัญชีค่าเสื่อมราคา</span><span class="sxs-lookup"><span data-stu-id="bdbba-106">Go to Fixed assets > Setup > Depreciation books.</span></span>
2. <span data-ttu-id="bdbba-107">คลิก สร้าง</span><span class="sxs-lookup"><span data-stu-id="bdbba-107">Click New.</span></span>
3. <span data-ttu-id="bdbba-108">ในฟิลด์สมุดบัญชีค่าเสื่อมราคา พิมพ์ค่า</span><span class="sxs-lookup"><span data-stu-id="bdbba-108">In the Depreciation book field, type a value.</span></span>
4. <span data-ttu-id="bdbba-109">ในฟิลด์ คำอธิบาย ให้พิมพ์ค่า</span><span class="sxs-lookup"><span data-stu-id="bdbba-109">In the Description field, type a value.</span></span>
5. <span data-ttu-id="bdbba-110">เลือกหรือยกเลิกกล่องกาเครื่องหมายการคำนวณค่าเสื่อมราคา</span><span class="sxs-lookup"><span data-stu-id="bdbba-110">Check or uncheck the Calculate depreciation checkbox.</span></span>
6. <span data-ttu-id="bdbba-111">คลิกปุ่มดรอปดาวน์เพื่อเปิดการค้นหาในฟิลด์โพรไฟล์ค่าเสื่อมราคา</span><span class="sxs-lookup"><span data-stu-id="bdbba-111">In the Depreciation profile field, click the drop-down button to open the lookup.</span></span>
7. <span data-ttu-id="bdbba-112">ในรายการนี้ ให้ค้นหาและเลือกโพรไฟล์ค่าเสื่อมราคาที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="bdbba-112">In the list, find and select the desired depreciation profile.</span></span>
8. <span data-ttu-id="bdbba-113">ในรายการนี้ ให้คลิกลิงค์ในแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="bdbba-113">In the list, click the link in the selected row.</span></span>
9. <span data-ttu-id="bdbba-114">ในฟิลด์โพรไฟล์ค่าเสื่อมราคาสำรอง คลิกปุ่มดรอปดาวน์เพื่อเปิดการค้นหา </span><span class="sxs-lookup"><span data-stu-id="bdbba-114">In the Alternative depreciation profile field, click the drop-down button to open the lookup.</span></span>
10. <span data-ttu-id="bdbba-115">ในรายการนี้ ให้เลือกโพรไฟล์ค่าเสื่อมราคาที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="bdbba-115">In the list, select the desired depreciation profile.</span></span>
11. <span data-ttu-id="bdbba-116">ในรายการนี้ ให้คลิกลิงค์ในแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="bdbba-116">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="bdbba-117">โพรไฟล์ค่าเสื่อมราคาพิเศษใช้สำหรับค่าเสื่อมราคาเพิ่มเติมของสินทรัพย์ในสถานการณ์ที่ผิดปกติ </span><span class="sxs-lookup"><span data-stu-id="bdbba-117">The Extraordinary depreciation profile is used for additional depreciation of an asset in unusual circumstances.</span></span> <span data-ttu-id="bdbba-118">ตัวอย่างเช่น คุณอาจใช้สิ่งนี้เพื่อบันทึกการคิดค่าเสื่อมราคาซึ่งเป็นผลมาจากภัยพิบัติธรรมชาติ</span><span class="sxs-lookup"><span data-stu-id="bdbba-118">For example, you might use this to record depreciation that results from a natural disaster.</span></span>  
12. <span data-ttu-id="bdbba-119">เลือกหรือยกเลิกการสร้างการปรับปรุงค่าเสื่อมราคาที่มีการปรับปรุงช่องกาเครื่องหมายพื้นฐาน</span><span class="sxs-lookup"><span data-stu-id="bdbba-119">Check or uncheck the Create depreciation adjustments with basis adjustments checkbox.</span></span>
13. <span data-ttu-id="bdbba-120">ในฟิลด์ปฏิทิน คลิกปุ่มดรอปดาวน์เพื่อเปิดการค้นหา</span><span class="sxs-lookup"><span data-stu-id="bdbba-120">In the Calendar field, click the drop-down button to open the lookup.</span></span>
14. <span data-ttu-id="bdbba-121">ในรายการนี้ ให้คลิกลิงค์ในแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="bdbba-121">In the list, click the link in the selected row.</span></span>

## <a name="associate-the-depreciation-book-with-a-fixed-asset-group"></a><span data-ttu-id="bdbba-122">เชื่อมโยงสมุดบัญชีค่าเสื่อมราคากับสินทรัพย์ถาวร</span><span class="sxs-lookup"><span data-stu-id="bdbba-122">Associate the depreciation book with a fixed asset group</span></span>
1. <span data-ttu-id="bdbba-123">คลิกสินทรัพย์ถาวร</span><span class="sxs-lookup"><span data-stu-id="bdbba-123">Click Fixed asset groups.</span></span>
2. <span data-ttu-id="bdbba-124">ในฟิลด์สินทรัพย์ถาวร ให้คลิกปุ่มดรอปดาวน์เพื่อเปิดการค้นหา</span><span class="sxs-lookup"><span data-stu-id="bdbba-124">In the Fixed asset group field, click the drop-down button to open the lookup.</span></span>
3. <span data-ttu-id="bdbba-125">ในรายการนี้ ให้ค้นหาและเลือกเรกคอร์ดที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="bdbba-125">In the list, find and select the desired record.</span></span>
4. <span data-ttu-id="bdbba-126">ในรายการนี้ ให้คลิกลิงค์ในแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="bdbba-126">In the list, click the link in the selected row.</span></span>
5. <span data-ttu-id="bdbba-127">ในฟิลด์การประชุมการเสื่อมราคา ให้เลือกหนึ่งตัวเลือก</span><span class="sxs-lookup"><span data-stu-id="bdbba-127">In the Depreciation convention field, select an option.</span></span>
6. <span data-ttu-id="bdbba-128">ในฟิลด์อายุการใช้งาน ป้อนจำนวน</span><span class="sxs-lookup"><span data-stu-id="bdbba-128">In the Service life field, enter a number.</span></span>
    * <span data-ttu-id="bdbba-129">สังเกตมูลค่าของฟิลด์รอบระยะเวลาการคิดค่าเสื่อมราคาหลังจากการตั้งค่าอายุการใช้งาน</span><span class="sxs-lookup"><span data-stu-id="bdbba-129">Notice the Depreciation periods field value is calculated after setting the Service life.</span></span>  



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]