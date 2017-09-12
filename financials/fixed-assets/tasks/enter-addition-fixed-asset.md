--- 
title: "การป้อนสินทรัพย์ถาวรที่ได้มาเพิ่มลงในสินทรัพย์ถาวร"
description: "กระบวนการนี้จะแสดงวิธีการเพิ่มรายการเพิ่มเติมไปยังทรัพย์สินถาวรที่มีอยู่ "
author: saraschi2
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Operations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: 4c22fb105d0deedda1b7dbfdd919d1745ad0ca2f
ms.contentlocale: th-th
ms.lasthandoff: 08/29/2017

---
# <a name="enter-an-addition-to-a-fixed-asset"></a><span data-ttu-id="b7db8-103">การป้อนสินทรัพย์ถาวรที่ได้มาเพิ่มลงในสินทรัพย์ถาวร</span><span class="sxs-lookup"><span data-stu-id="b7db8-103">Enter an addition to a fixed asset</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="b7db8-104">กระบวนการนี้จะแสดงวิธีการเพิ่มรายการเพิ่มเติมไปยังทรัพย์สินถาวรที่มีอยู่ </span><span class="sxs-lookup"><span data-stu-id="b7db8-104">This procedure shows how to add an addition to an existing fixed asset.</span></span> <span data-ttu-id="b7db8-105">วัตถุประสงค์ของส่วนเพิ่มเติมของสินทรัพย์ถาวรเพื่อติดตามการเพิ่มรายการ การบำรุงรักษา หรือการปรับปรุงสำหรับสินทรัพย์ และให้ข้อมูลเท่านั้น </span><span class="sxs-lookup"><span data-stu-id="b7db8-105">The purpose of Fixed asset additions is to track item additions, maintenance, or improvements for an asset, and is informational only.</span></span> <span data-ttu-id="b7db8-106">การเปลี่ยนแปลใดๆ กับมูลค่าสินทรัพย์ถาวรหรืออายุการใช้งานจะต้องทำแยกต่างหาก </span><span class="sxs-lookup"><span data-stu-id="b7db8-106">Any changes to the fixed asset value or service life must be made separately.</span></span>   



<span data-ttu-id="b7db8-107">กระบวนการใช้บทบาทของนักบัญชีและข้อมูลสาธิตสำหรับนิติบุคคล USMF</span><span class="sxs-lookup"><span data-stu-id="b7db8-107">The procedure uses the Accountant role and demo data for the USMF legal entity.</span></span>

1. <span data-ttu-id="b7db8-108">ไปที่ สินทรัพย์ถาวร > สินทรัพย์ถาวร > สินทรัพย์ถาวร</span><span class="sxs-lookup"><span data-stu-id="b7db8-108">Go to Fixed assets > Fixed assets > Fixed assets.</span></span>
2. <span data-ttu-id="b7db8-109">ในรายการ ค้นหาและเลือกสินทรัพย์ถาวรสำหรับเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="b7db8-109">In the list, find and select the fixed asset for the addition.</span></span>
3. <span data-ttu-id="b7db8-110">ในรายการนี้ ให้คลิกลิงค์ในแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="b7db8-110">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="b7db8-111">ในบานหน้าต่างการดำเนินการ คลิกสินทรัพย์ถาวร</span><span class="sxs-lookup"><span data-stu-id="b7db8-111">On the Action Pane, click Fixed asset.</span></span>
5. <span data-ttu-id="b7db8-112">คลิกเพิ่มเติมสินทรัพย์ถาวร</span><span class="sxs-lookup"><span data-stu-id="b7db8-112">Click Fixed asset additions.</span></span>
6. <span data-ttu-id="b7db8-113">คลิก สร้าง</span><span class="sxs-lookup"><span data-stu-id="b7db8-113">Click New.</span></span>
7. <span data-ttu-id="b7db8-114">ในฟิลด์ชื่อ ให้พิมพ์ค่า </span><span class="sxs-lookup"><span data-stu-id="b7db8-114">In the Name field, type a value.</span></span>
8. <span data-ttu-id="b7db8-115">ตั้งค่าวันที่ของการซื้อเพิ่มหรือบริการ</span><span class="sxs-lookup"><span data-stu-id="b7db8-115">Set the date of the addition purchase or service.</span></span>
9. <span data-ttu-id="b7db8-116">ป้อนต้นทุนของสินค้า การบำรุงรักษา หรือการปรับปรุงอื่นสำหรับสินทรัพย์</span><span class="sxs-lookup"><span data-stu-id="b7db8-116">Enter the cost of the item, maintenance, or other improvement for the asset.</span></span>
10. <span data-ttu-id="b7db8-117">ในฟิลด์ ปริมาณ ให้ป้อนตัวเลข</span><span class="sxs-lookup"><span data-stu-id="b7db8-117">In the Quantity field, enter a number.</span></span>
    * <span data-ttu-id="b7db8-118">ต้นทุนทั้งหมดจะไม่มีผลกระทบบนค่าของสินทรัพย์ถาวร และการติดตาม และแจ้งให้ทราบเท่านั้น </span><span class="sxs-lookup"><span data-stu-id="b7db8-118">The total cost will have no impact on the value of the fixed asset and is for tracking and informational purposes only.</span></span> <span data-ttu-id="b7db8-119">ถ้าต้นทุนจะถูกบันทึกเป็นสินทรัพย์ ธุรกรรมการปรับปรุงจะต้องเขียนขึ้นและลงรายการบัญชีแยกต่างหาก</span><span class="sxs-lookup"><span data-stu-id="b7db8-119">If the cost will be capitalized, then a write-up adjustment transaction must be posted separately.</span></span>  
11. <span data-ttu-id="b7db8-120">คลิกแท็บ ทั่วไป</span><span class="sxs-lookup"><span data-stu-id="b7db8-120">Click the General tab.</span></span>
    * <span data-ttu-id="b7db8-121">ตั้งค่าการเพิ่มอายุการใช้งาน ถ้าส่วนเพิ่มเติมจะทำให้อายุการใช้งานของสินทรัพย์เพิ่มขึ้น</span><span class="sxs-lookup"><span data-stu-id="b7db8-121">Set Increases service life if the addition increases the service life of the asset.</span></span>  
    * <span data-ttu-id="b7db8-122">ฟิลด์นี้มีไว้เพื่อให้ข้อมูลเท่านั้น </span><span class="sxs-lookup"><span data-stu-id="b7db8-122">This field is informational only.</span></span> <span data-ttu-id="b7db8-123">เพื่อเพิ่มอายุการใช้งาน แก้ไขอายุการใช้งานบนรูปแบบมูลค่าและ/หรือ สมุดบัญชีค่าเสื่อมราคาสำหรับสินทรัพย์</span><span class="sxs-lookup"><span data-stu-id="b7db8-123">To increase the service life, modify the Service life on the Value models and/or Depreciation books for the asset.</span></span>  


