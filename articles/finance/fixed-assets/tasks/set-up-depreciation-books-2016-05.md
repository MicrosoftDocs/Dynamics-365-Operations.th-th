---
title: การตั้งค่าสมุดบัญชีค่าเสื่อมราคา (พฤษภาคม 2016)
description: 'คำแนะนำของงานนี้จะสร้างสมุดค่าเสื่อมราคาใหม่และเชื่อมโยงกับสินทรัพย์ถาวร '
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
ms.openlocfilehash: 6840e211847494598a81cd3228dbd3796447e18c
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 09/27/2019
ms.locfileid: "2186911"
---
# <a name="set-up-depreciation-books-may-2016"></a><span data-ttu-id="16123-103">การตั้งค่าสมุดบัญชีค่าเสื่อมราคา (พฤษภาคม 2016)</span><span class="sxs-lookup"><span data-stu-id="16123-103">Set up depreciation books (May 2016)</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="16123-104">คำแนะนำของงานนี้จะสร้างสมุดค่าเสื่อมราคาใหม่และเชื่อมโยงกับสินทรัพย์ถาวร </span><span class="sxs-lookup"><span data-stu-id="16123-104">This task guide will create a new depreciation book and associate it with a fixed asset group.</span></span>  <span data-ttu-id="16123-105">ใช้บทบาทของนักบัญชีและข้อมูลสาธิตสำหรับนิติบุคคล USMF</span><span class="sxs-lookup"><span data-stu-id="16123-105">It uses the Accountant role and demo data for the USMF legal entity.</span></span>


## <a name="create-a-depreciation-book"></a><span data-ttu-id="16123-106">สร้างสมุดบัญชีค่าเสื่อมราคา</span><span class="sxs-lookup"><span data-stu-id="16123-106">Create a depreciation book</span></span>
1. <span data-ttu-id="16123-107">ไปที่สินทรัพย์ถาวร > การติดตั้ง > สมุดบัญชีค่าเสื่อมราคา</span><span class="sxs-lookup"><span data-stu-id="16123-107">Go to Fixed assets > Setup > Depreciation books.</span></span>
2. <span data-ttu-id="16123-108">คลิก สร้าง</span><span class="sxs-lookup"><span data-stu-id="16123-108">Click New.</span></span>
3. <span data-ttu-id="16123-109">ในฟิลด์สมุดบัญชีค่าเสื่อมราคา พิมพ์ค่า</span><span class="sxs-lookup"><span data-stu-id="16123-109">In the Depreciation book field, type a value.</span></span>
4. <span data-ttu-id="16123-110">ในฟิลด์ คำอธิบาย ให้พิมพ์ค่า</span><span class="sxs-lookup"><span data-stu-id="16123-110">In the Description field, type a value.</span></span>
5. <span data-ttu-id="16123-111">เลือกหรือยกเลิกกล่องกาเครื่องหมายการคำนวณค่าเสื่อมราคา</span><span class="sxs-lookup"><span data-stu-id="16123-111">Check or uncheck the Calculate depreciation checkbox.</span></span>
6. <span data-ttu-id="16123-112">คลิกปุ่มดรอปดาวน์เพื่อเปิดการค้นหาในฟิลด์โพรไฟล์ค่าเสื่อมราคา</span><span class="sxs-lookup"><span data-stu-id="16123-112">In the Depreciation profile field, click the drop-down button to open the lookup.</span></span>
7. <span data-ttu-id="16123-113">ในรายการนี้ ให้ค้นหาและเลือกโพรไฟล์ค่าเสื่อมราคาที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="16123-113">In the list, find and select the desired depreciation profile.</span></span>
8. <span data-ttu-id="16123-114">ในรายการนี้ ให้คลิกลิงค์ในแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="16123-114">In the list, click the link in the selected row.</span></span>
9. <span data-ttu-id="16123-115">ในฟิลด์โพรไฟล์ค่าเสื่อมราคาสำรอง คลิกปุ่มดรอปดาวน์เพื่อเปิดการค้นหา </span><span class="sxs-lookup"><span data-stu-id="16123-115">In the Alternative depreciation profile field, click the drop-down button to open the lookup.</span></span>
10. <span data-ttu-id="16123-116">ในรายการนี้ ให้เลือกโพรไฟล์ค่าเสื่อมราคาที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="16123-116">In the list, select the desired depreciation profile.</span></span>
11. <span data-ttu-id="16123-117">ในรายการนี้ ให้คลิกลิงค์ในแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="16123-117">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="16123-118">โพรไฟล์ค่าเสื่อมราคาพิเศษใช้สำหรับค่าเสื่อมราคาเพิ่มเติมของสินทรัพย์ในสถานการณ์ที่ผิดปกติ </span><span class="sxs-lookup"><span data-stu-id="16123-118">The Extraordinary depreciation profile is used for additional depreciation of an asset in unusual circumstances.</span></span> <span data-ttu-id="16123-119">ตัวอย่างเช่น คุณอาจใช้สิ่งนี้เพื่อบันทึกการคิดค่าเสื่อมราคาซึ่งเป็นผลมาจากภัยพิบัติธรรมชาติ</span><span class="sxs-lookup"><span data-stu-id="16123-119">For example, you might use this to record depreciation that results from a natural disaster.</span></span>  
12. <span data-ttu-id="16123-120">เลือกหรือยกเลิกการสร้างการปรับปรุงค่าเสื่อมราคาที่มีการปรับปรุงช่องกาเครื่องหมายพื้นฐาน</span><span class="sxs-lookup"><span data-stu-id="16123-120">Check or uncheck the Create depreciation adjustments with basis adjustments checkbox.</span></span>
13. <span data-ttu-id="16123-121">ในฟิลด์ปฏิทิน คลิกปุ่มดรอปดาวน์เพื่อเปิดการค้นหา</span><span class="sxs-lookup"><span data-stu-id="16123-121">In the Calendar field, click the drop-down button to open the lookup.</span></span>
14. <span data-ttu-id="16123-122">ในรายการนี้ ให้คลิกลิงค์ในแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="16123-122">In the list, click the link in the selected row.</span></span>

## <a name="associate-the-depreciation-book-with-a-fixed-asset-group"></a><span data-ttu-id="16123-123">เชื่อมโยงสมุดบัญชีค่าเสื่อมราคากับสินทรัพย์ถาวร</span><span class="sxs-lookup"><span data-stu-id="16123-123">Associate the depreciation book with a fixed asset group</span></span>
1. <span data-ttu-id="16123-124">คลิกสินทรัพย์ถาวร</span><span class="sxs-lookup"><span data-stu-id="16123-124">Click Fixed asset groups.</span></span>
2. <span data-ttu-id="16123-125">ในฟิลด์สินทรัพย์ถาวร ให้คลิกปุ่มดรอปดาวน์เพื่อเปิดการค้นหา</span><span class="sxs-lookup"><span data-stu-id="16123-125">In the Fixed asset group field, click the drop-down button to open the lookup.</span></span>
3. <span data-ttu-id="16123-126">ในรายการนี้ ให้ค้นหาและเลือกเรกคอร์ดที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="16123-126">In the list, find and select the desired record.</span></span>
4. <span data-ttu-id="16123-127">ในรายการนี้ ให้คลิกลิงค์ในแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="16123-127">In the list, click the link in the selected row.</span></span>
5. <span data-ttu-id="16123-128">ในฟิลด์การประชุมการเสื่อมราคา ให้เลือกหนึ่งตัวเลือก</span><span class="sxs-lookup"><span data-stu-id="16123-128">In the Depreciation convention field, select an option.</span></span>
6. <span data-ttu-id="16123-129">ในฟิลด์อายุการใช้งาน ป้อนจำนวน</span><span class="sxs-lookup"><span data-stu-id="16123-129">In the Service life field, enter a number.</span></span>
    * <span data-ttu-id="16123-130">สังเกตมูลค่าของฟิลด์รอบระยะเวลาการคิดค่าเสื่อมราคาหลังจากการตั้งค่าอายุการใช้งาน</span><span class="sxs-lookup"><span data-stu-id="16123-130">Notice the Depreciation periods field value is calculated after setting the Service life.</span></span>  

