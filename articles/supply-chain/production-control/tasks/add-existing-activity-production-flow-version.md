---
title: เพิ่มกิจกรรมที่มีอยู่ไปยังรุ่นขั้นตอนการผลิต
description: 'ในขณะที่สร้างขั้นตอนการผลิตรุ่นใหม่ คุณสามารถเลือกที่จะเพิ่มกิจกรรมที่สร้างขึ้นสำหรับรุ่นที่เก่ากว่าไปยังรุ่นใหม่ได้ '
author: cvocph
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LeanProductionFlow, PlanActivity, PlanActivityAddExisting, PlanActivityAddExistingLookup
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: conradv
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: c01d988469ead4ab09d69b1cb6e2f9b417080c69
ms.sourcegitcommit: fcb27d6a46cd544feef34f6ec7607bdd46b0c12b
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 03/18/2020
ms.locfileid: "3149423"
---
# <a name="add-an-existing-activity-to-a-production-flow-version"></a><span data-ttu-id="8a3d6-103">เพิ่มกิจกรรมที่มีอยู่ไปยังรุ่นขั้นตอนการผลิต</span><span class="sxs-lookup"><span data-stu-id="8a3d6-103">Add an existing activity to a production flow version</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="8a3d6-104">ในขณะที่สร้างขั้นตอนการผลิตรุ่นใหม่ คุณสามารถเลือกที่จะเพิ่มกิจกรรมที่สร้างขึ้นสำหรับรุ่นที่เก่ากว่าไปยังรุ่นใหม่ได้ </span><span class="sxs-lookup"><span data-stu-id="8a3d6-104">When creating new versions of production flows, you can choose to add activities created for the older versions, to the new version.</span></span> <span data-ttu-id="8a3d6-105">กระบวนงานนี้แสดงวิธีการสร้างรุ่นใหม่สำหรับขั้นตอนการผลิตที่มีอยู่โดยไม่ต้องคัดลอกกิจกรรม</span><span class="sxs-lookup"><span data-stu-id="8a3d6-105">This procedure shows how a new version is created for an existing production flow, without copying the activities.</span></span> <span data-ttu-id="8a3d6-106">ในขั้นตอนถัดไป กิจกรรมที่มีอยู่จะถูกเพิ่มไปยังรุ่นใหม่</span><span class="sxs-lookup"><span data-stu-id="8a3d6-106">In the next step, an existing activity is added to the new version.</span></span> 

<span data-ttu-id="8a3d6-107">งานนี้จำเป็นต้องใช้ขั้นตอนการผลิตที่มีรุ่นและกิจกรรมที่สร้างขึ้นแล้ว</span><span class="sxs-lookup"><span data-stu-id="8a3d6-107">This task requires production flow with version and activities already created.</span></span>


## <a name="create-a-new-production-flow-version"></a><span data-ttu-id="8a3d6-108">สร้างเวอร์ชันขั้นตอนการผลิตใหม่</span><span class="sxs-lookup"><span data-stu-id="8a3d6-108">Create a new production flow version</span></span>
1. <span data-ttu-id="8a3d6-109">ไปที่การควบคุมการผลิต > การตั้งค่า > ขั้นตอนการผลิตแบบ lean > ขั้นตอนการผลิต</span><span class="sxs-lookup"><span data-stu-id="8a3d6-109">Go to Production control > Setup > Lean production flow > Production flows.</span></span>
2. <span data-ttu-id="8a3d6-110">ในรายการนี้ ให้ค้นหาและเลือกเรกคอร์ดที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="8a3d6-110">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="8a3d6-111">ในรายการนี้ ให้คลิกลิงค์ในแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="8a3d6-111">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="8a3d6-112">คลิกแก้ไข</span><span class="sxs-lookup"><span data-stu-id="8a3d6-112">Click Edit.</span></span>
5. <span data-ttu-id="8a3d6-113">ในรายการนี้ ให้ทำเครื่องหมายแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="8a3d6-113">In the list, mark the selected row.</span></span>
6. <span data-ttu-id="8a3d6-114">ในฟิลด์วันหมดอายุ ให้ป้อนวันที่และเวลา</span><span class="sxs-lookup"><span data-stu-id="8a3d6-114">In the Expiration date field, enter a date and time.</span></span>
    * <span data-ttu-id="8a3d6-115">โปรดทราบว่าก่อนที่คุณจะสร้างรุ่นขั้นตอนการผลิตใหม่ ตรวจสอบให้แน่ใจว่าได้ตรวจสอบวันและเวลาหมดอายุของรุ่นที่ใช้งานอยู่ </span><span class="sxs-lookup"><span data-stu-id="8a3d6-115">Note that before you create a new production flow version, make sure to check the expiration date and time of the active version.</span></span> <span data-ttu-id="8a3d6-116">จะมีการสร้างรุ่นใหม่ที่มีวันที่เริ่มต้นที่มีผลบังคับใช้ซึ่งต่อจากวันหมดอายุของรุ่นที่เลือก</span><span class="sxs-lookup"><span data-stu-id="8a3d6-116">The new version will be created with an effective start date, which connects to the expiry date of the selected version.</span></span>  
7. <span data-ttu-id="8a3d6-117">คลิก เพิ่ม</span><span class="sxs-lookup"><span data-stu-id="8a3d6-117">Click Add.</span></span>
8. <span data-ttu-id="8a3d6-118">เลือก ไม่ ในฟิลด์ คัดลอกจากรุ่น</span><span class="sxs-lookup"><span data-stu-id="8a3d6-118">Select No in the Copy from version field.</span></span>
    * <span data-ttu-id="8a3d6-119">เลือก ไม่ เพื่อเริ่มต้นใช้รุ่นที่ว่างอยู่ถ้ากิจกรรมของรุ่นที่คัดลอกส่วนใหญ่จะถูกแทนที่ด้วยกิจกรรมใหม่ </span><span class="sxs-lookup"><span data-stu-id="8a3d6-119">Select No to start with an empty version if most of the activities of the copied version will be replaced by new activities.</span></span> <span data-ttu-id="8a3d6-120">เพิ่มกิจกรรมที่ไม่มีการเปลี่ยนแปลงไปยังฟังก์ชัน เพิ่มรายการที่มีอยู่ ในแบบฟอร์มกิจกรรมด้วยตนเอง</span><span class="sxs-lookup"><span data-stu-id="8a3d6-120">Add the unchanged activities to the Add existing function in the activity form manually.</span></span>  
9. <span data-ttu-id="8a3d6-121">เลือก ไม่ ในฟิลด์ ทำซ้ำกฎคัมบัง</span><span class="sxs-lookup"><span data-stu-id="8a3d6-121">Select No in the Duplicate kanban rules field.</span></span>
    * <span data-ttu-id="8a3d6-122">เมื่อกิจกรรมไม่ได้ถูกคัดลอกไปยังรุ่นใหม่ จะไม่สามารถคัดลอกกฎคัมบังในขณะที่สร้างรุ่นใหม่ได้ </span><span class="sxs-lookup"><span data-stu-id="8a3d6-122">When the activities are not copied to the new version, it is not possible to copy the kanban rules at the time of creation of the new version.</span></span>   <span data-ttu-id="8a3d6-123">แต่คุณจะใช้ฟังก์ชัน สร้างคัมบังการแทนที่ในภายหลังในแบบฟอร์มกฎคัมบัง เพื่อแทนที่กฎคัมบังของรุ่นขั้นตอนการผลิตเดิมที่มีกฎคัมบังที่ใช้กิจกรรมของรุ่นใหม่</span><span class="sxs-lookup"><span data-stu-id="8a3d6-123">Instead you will use the create replacement kanban function later in the kanban rule form, to replace kanban rules of the old production flow version with kanban rules using the activities of the new version.</span></span>  
10. <span data-ttu-id="8a3d6-124">คลิก ตกลง</span><span class="sxs-lookup"><span data-stu-id="8a3d6-124">Click OK.</span></span>
11. <span data-ttu-id="8a3d6-125">ในรายการนี้ ให้ค้นหาและเลือกเรกคอร์ดที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="8a3d6-125">In the list, find and select the desired record.</span></span>

## <a name="add-an-existing-activity"></a><span data-ttu-id="8a3d6-126">เพิ่มกิจกรรมที่มีอยู่</span><span class="sxs-lookup"><span data-stu-id="8a3d6-126">Add an existing activity</span></span>
1. <span data-ttu-id="8a3d6-127">คลิกกิจกรรม</span><span class="sxs-lookup"><span data-stu-id="8a3d6-127">Click Activities.</span></span>
2. <span data-ttu-id="8a3d6-128">คลิกเพิ่มรายการที่มีอยู่เพื่อเปิดกล่องโต้ตอบการวาง</span><span class="sxs-lookup"><span data-stu-id="8a3d6-128">Click Add existing to open the drop dialog.</span></span>
    * <span data-ttu-id="8a3d6-129">ค้นหาและเลือกกิจกรรมที่มีอยู่ที่จะเพิ่มในรุ่นขั้นตอนการผลิตใหม่ </span><span class="sxs-lookup"><span data-stu-id="8a3d6-129">Find and select an existing activity to be added to the new production flow version.</span></span>  <span data-ttu-id="8a3d6-130">โปรดทราบว่ารายการจะแสดงกิจกรรมทั้งหมดที่ถูกสร้างขึ้นสำหรับขั้นตอนการผลิตนี้สำหรับรุ่นก่อนหน้านี้ทั้งหมดของขั้นตอน</span><span class="sxs-lookup"><span data-stu-id="8a3d6-130">Note that the list shows all activities that have been created for this production flow for all previous versions of the flow.</span></span>  
3. <span data-ttu-id="8a3d6-131">ในฟิลด์กิจกรรม ให้ป้อนหรือเลือกค่า</span><span class="sxs-lookup"><span data-stu-id="8a3d6-131">In the Activity field, enter or select a value.</span></span>
4. <span data-ttu-id="8a3d6-132">คลิก ตกลง</span><span class="sxs-lookup"><span data-stu-id="8a3d6-132">Click OK.</span></span>

