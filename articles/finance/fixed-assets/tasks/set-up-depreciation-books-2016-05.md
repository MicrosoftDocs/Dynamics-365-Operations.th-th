---
title: ตั้งค่าสมุดบัญชีค่าเสื่อมราคา
description: กระบวนงานนี้นำไปสู่กระบวนการสร้างสมุดบัญชีค่าเสื่อมราคาใหม่และเชื่อมโยงกับกลุ่มสินทรัพย์ถาวร
author: saraschi2
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: AssetDepBookTable, AssetGroupDepBookSetup
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 03f915fa91e0eeff2f26ab9a60bbd5118317e853
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 10/13/2020
ms.locfileid: "4448483"
---
# <a name="set-up-depreciation-books"></a><span data-ttu-id="7d9cd-103">ตั้งค่าสมุดบัญชีค่าเสื่อมราคา</span><span class="sxs-lookup"><span data-stu-id="7d9cd-103">Set up depreciation books</span></span> 

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="7d9cd-104">กระบวนงานนี้นำไปสู่กระบวนการสร้างสมุดบัญชีค่าเสื่อมราคาใหม่และเชื่อมโยงกับกลุ่มสินทรัพย์ถาวร</span><span class="sxs-lookup"><span data-stu-id="7d9cd-104">This procedure walks through the process of creating a new depreciation book and associate it with a fixed asset group.</span></span> 

## <a name="create-a-depreciation-book"></a><span data-ttu-id="7d9cd-105">สร้างสมุดบัญชีค่าเสื่อมราคา</span><span class="sxs-lookup"><span data-stu-id="7d9cd-105">Create a depreciation book</span></span>
1. <span data-ttu-id="7d9cd-106">ไปที่สินทรัพย์ถาวร > การติดตั้ง > สมุดบัญชีค่าเสื่อมราคา</span><span class="sxs-lookup"><span data-stu-id="7d9cd-106">Go to Fixed assets > Setup > Depreciation books.</span></span>
2. <span data-ttu-id="7d9cd-107">คลิก สร้าง</span><span class="sxs-lookup"><span data-stu-id="7d9cd-107">Click New.</span></span>
3. <span data-ttu-id="7d9cd-108">ในฟิลด์สมุดบัญชีค่าเสื่อมราคา พิมพ์ค่า</span><span class="sxs-lookup"><span data-stu-id="7d9cd-108">In the Depreciation book field, type a value.</span></span>
4. <span data-ttu-id="7d9cd-109">ในฟิลด์ คำอธิบาย ให้พิมพ์ค่า</span><span class="sxs-lookup"><span data-stu-id="7d9cd-109">In the Description field, type a value.</span></span>
5. <span data-ttu-id="7d9cd-110">เลือกหรือยกเลิกกล่องกาเครื่องหมายการคำนวณค่าเสื่อมราคา</span><span class="sxs-lookup"><span data-stu-id="7d9cd-110">Check or uncheck the Calculate depreciation checkbox.</span></span>
6. <span data-ttu-id="7d9cd-111">คลิกปุ่มดรอปดาวน์เพื่อเปิดการค้นหาในฟิลด์โพรไฟล์ค่าเสื่อมราคา</span><span class="sxs-lookup"><span data-stu-id="7d9cd-111">In the Depreciation profile field, click the drop-down button to open the lookup.</span></span>
7. <span data-ttu-id="7d9cd-112">ในรายการนี้ ให้ค้นหาและเลือกโพรไฟล์ค่าเสื่อมราคาที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="7d9cd-112">In the list, find and select the desired depreciation profile.</span></span>
8. <span data-ttu-id="7d9cd-113">ในรายการนี้ ให้คลิกลิงค์ในแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="7d9cd-113">In the list, click the link in the selected row.</span></span>
9. <span data-ttu-id="7d9cd-114">ในฟิลด์โพรไฟล์ค่าเสื่อมราคาสำรอง คลิกปุ่มดรอปดาวน์เพื่อเปิดการค้นหา </span><span class="sxs-lookup"><span data-stu-id="7d9cd-114">In the Alternative depreciation profile field, click the drop-down button to open the lookup.</span></span>
10. <span data-ttu-id="7d9cd-115">ในรายการนี้ ให้เลือกโพรไฟล์ค่าเสื่อมราคาที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="7d9cd-115">In the list, select the desired depreciation profile.</span></span>
11. <span data-ttu-id="7d9cd-116">ในรายการนี้ ให้คลิกลิงค์ในแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="7d9cd-116">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="7d9cd-117">โพรไฟล์ค่าเสื่อมราคาพิเศษใช้สำหรับค่าเสื่อมราคาเพิ่มเติมของสินทรัพย์ในสถานการณ์ที่ผิดปกติ </span><span class="sxs-lookup"><span data-stu-id="7d9cd-117">The Extraordinary depreciation profile is used for additional depreciation of an asset in unusual circumstances.</span></span> <span data-ttu-id="7d9cd-118">ตัวอย่างเช่น คุณอาจใช้สิ่งนี้เพื่อบันทึกการคิดค่าเสื่อมราคาซึ่งเป็นผลมาจากภัยพิบัติธรรมชาติ</span><span class="sxs-lookup"><span data-stu-id="7d9cd-118">For example, you might use this to record depreciation that results from a natural disaster.</span></span>  
12. <span data-ttu-id="7d9cd-119">เลือกหรือยกเลิกการสร้างการปรับปรุงค่าเสื่อมราคาที่มีการปรับปรุงช่องกาเครื่องหมายพื้นฐาน</span><span class="sxs-lookup"><span data-stu-id="7d9cd-119">Check or uncheck the Create depreciation adjustments with basis adjustments checkbox.</span></span>
13. <span data-ttu-id="7d9cd-120">ในฟิลด์ปฏิทิน คลิกปุ่มดรอปดาวน์เพื่อเปิดการค้นหา</span><span class="sxs-lookup"><span data-stu-id="7d9cd-120">In the Calendar field, click the drop-down button to open the lookup.</span></span>
14. <span data-ttu-id="7d9cd-121">ในรายการนี้ ให้คลิกลิงค์ในแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="7d9cd-121">In the list, click the link in the selected row.</span></span>

## <a name="associate-the-depreciation-book-with-a-fixed-asset-group"></a><span data-ttu-id="7d9cd-122">เชื่อมโยงสมุดบัญชีค่าเสื่อมราคากับสินทรัพย์ถาวร</span><span class="sxs-lookup"><span data-stu-id="7d9cd-122">Associate the depreciation book with a fixed asset group</span></span>
1. <span data-ttu-id="7d9cd-123">คลิกสินทรัพย์ถาวร</span><span class="sxs-lookup"><span data-stu-id="7d9cd-123">Click Fixed asset groups.</span></span>
2. <span data-ttu-id="7d9cd-124">ในฟิลด์สินทรัพย์ถาวร ให้คลิกปุ่มดรอปดาวน์เพื่อเปิดการค้นหา</span><span class="sxs-lookup"><span data-stu-id="7d9cd-124">In the Fixed asset group field, click the drop-down button to open the lookup.</span></span>
3. <span data-ttu-id="7d9cd-125">ในรายการนี้ ให้ค้นหาและเลือกเรกคอร์ดที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="7d9cd-125">In the list, find and select the desired record.</span></span>
4. <span data-ttu-id="7d9cd-126">ในรายการนี้ ให้คลิกลิงค์ในแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="7d9cd-126">In the list, click the link in the selected row.</span></span>
5. <span data-ttu-id="7d9cd-127">ในฟิลด์การประชุมการเสื่อมราคา ให้เลือกหนึ่งตัวเลือก</span><span class="sxs-lookup"><span data-stu-id="7d9cd-127">In the Depreciation convention field, select an option.</span></span>
6. <span data-ttu-id="7d9cd-128">ในฟิลด์อายุการใช้งาน ป้อนจำนวน</span><span class="sxs-lookup"><span data-stu-id="7d9cd-128">In the Service life field, enter a number.</span></span>
    * <span data-ttu-id="7d9cd-129">สังเกตมูลค่าของฟิลด์รอบระยะเวลาการคิดค่าเสื่อมราคาหลังจากการตั้งค่าอายุการใช้งาน</span><span class="sxs-lookup"><span data-stu-id="7d9cd-129">Notice the Depreciation periods field value is calculated after setting the Service life.</span></span>  

