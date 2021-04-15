---
title: เข้าใจฟิลด์วันที่และเวลา
description: ทำความเข้าใจสิ่งที่ควรคาดหวังเมื่อใช้ฟิลด์วันที่และเวลาใน Microsoft Dynamics 365 Human Resources
author: andreabichsel
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: HcmPersonnelManagementWorkspace
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: jaredha
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: efda2b54f9228ac539e6ba2d18f85bf3ad15a6ff
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 03/31/2021
ms.locfileid: "5802442"
---
# <a name="understand-date-and-time-fields"></a><span data-ttu-id="c130a-103">ทำความเข้าใจฟิลด์วันที่และเวลา</span><span class="sxs-lookup"><span data-stu-id="c130a-103">Understand Date and Time fields</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="c130a-104">ฟิลด์ **วันที่และเวลา** แนวคิดพื้นฐานใน Dynamics 365 Human Resources</span><span class="sxs-lookup"><span data-stu-id="c130a-104">**Date and Time** fields are a fundamental concept in Dynamics 365 Human Resources.</span></span> <span data-ttu-id="c130a-105">นับเป็นสิ่งสำคัญที่จะต้องทำความเข้าใจวิธีการทำงานกับข้อมูล **วันที่และเวลา** ในฟอร์ม Dataverse และแหล่งข้อมูลภายนอก</span><span class="sxs-lookup"><span data-stu-id="c130a-105">It's important to understand how to work with **Date and Time** data in forms, Dataverse, and external sources.</span></span>

## <a name="understanding-the-difference-between-date-and-date-and-time-field-data-types"></a><span data-ttu-id="c130a-106">การทำความเข้าใจความแตกต่างระหว่างชนิดของข้อมูลในฟิลด์วันที่และวันที่และเวลา</span><span class="sxs-lookup"><span data-stu-id="c130a-106">Understanding the difference between Date and Date and Time field data types</span></span>

<span data-ttu-id="c130a-107">ฟิลด์ **วันที่และเวลา** มีข้อมูลโซนเวลา ในขณะที่ฟิลด์ **วันที่** ไม่มี</span><span class="sxs-lookup"><span data-stu-id="c130a-107">**Date and Time** fields contain time zone information, while **Date** fields don't.</span></span> <span data-ttu-id="c130a-108">ฟิลด์ **วันที่** แสดงข้อมูลเดียวกันในสถานที่ใดๆ</span><span class="sxs-lookup"><span data-stu-id="c130a-108">**Date** fields display the same information in any location.</span></span> <span data-ttu-id="c130a-109">เมื่อคุณป้อนวันที่ลงในฟิลด์ **วันที่** ทรัพยากรบุคคลจะเขียนวันที่เดียวกันไปยังฐานข้อมูล</span><span class="sxs-lookup"><span data-stu-id="c130a-109">When you enter a date into a **Date** field, Human Resources writes that same date to the database.</span></span>

<span data-ttu-id="c130a-110">เมื่อแสดงข้อมูลในฟิลด์ **วันที่และเวลา** ทรัพยากรบุคคลจะปรับปรุงวันที่และเวลาตามโซนเวลาของผู้ใช้ที่ตั้งค่าไว้ในฟอร์ม **ตัวเลือกผู้ใช้** (**ทั่วไป > ตั้งค่า > ตัวเลือกผู้ใช้**)</span><span class="sxs-lookup"><span data-stu-id="c130a-110">When displaying data in a **Date and Time** field, Human Resources adjusts the date and time based on the user's time zone set in the **User Options** form (**Common > Setup > User Options**).</span></span> <span data-ttu-id="c130a-111">ข้อมูลวันที่และเวลาที่คุณป้อนในฟิลด์อาจไม่เหมือนกับข้อมูลที่เขียนลงในฐานข้อมูล</span><span class="sxs-lookup"><span data-stu-id="c130a-111">The date and time information you enter in the field might not be the same as the information written to the database.</span></span>

<span data-ttu-id="c130a-112">[![ฟอร์มตัวเลือกผู้ใช้](./media/useroptionsform.png)](./media/useroptionsform.png)</span><span class="sxs-lookup"><span data-stu-id="c130a-112">[![User options form](./media/useroptionsform.png)](./media/useroptionsform.png)</span></span>

## <a name="understanding-date-and-time-fields-in-forms"></a><span data-ttu-id="c130a-113">การทำความเข้าใจฟิลด์วันที่และเวลาในฟอร์ม</span><span class="sxs-lookup"><span data-stu-id="c130a-113">Understanding Date and Time fields in forms</span></span> 

<span data-ttu-id="c130a-114">ข้อมูล **วันที่และเวลา** ที่แสดงบนหน้าจอจะไม่เหมือนกับข้อมูลที่จัดเก็บไว้ในฐานข้อมูล ถ้าโซนเวลาของผู้ใช้ไม่ได้รับการตั้งค่าเป็นเวลามาตรฐานสากล (UTC)</span><span class="sxs-lookup"><span data-stu-id="c130a-114">**Date and Time** data displayed on the screen isn't the same as the data stored in the database if the user's time zone isn't set to Coordinated Universal Time (UTC).</span></span> <span data-ttu-id="c130a-115">ข้อมูลในฟิลด์ **วันที่และเวลา** จะถูกจัดเก็บเป็น UTC เสมอ</span><span class="sxs-lookup"><span data-stu-id="c130a-115">Data in **Date and Time** fields is always stored as UTC.</span></span>

<span data-ttu-id="c130a-116">[![UTC ฟอร์มผู้ปฏิบัติงาน](./media/worker-form.png)](./media/worker-form.png)</span><span class="sxs-lookup"><span data-stu-id="c130a-116">[![Worker form UTC](./media/worker-form.png)](./media/worker-form.png)</span></span>

## <a name="understand-date-and-time-fields-in-the-database"></a><span data-ttu-id="c130a-117">ทำความเข้าใจฟิลด์วันที่และเวลาในฐานข้อมูล</span><span class="sxs-lookup"><span data-stu-id="c130a-117">Understand Date and Time fields in the database</span></span> 

<span data-ttu-id="c130a-118">เมื่อทรัพยากรบุคคลเขียนค่า **วันที่และเวลา** ไปยังฐานข้อมูล วันที่และเวลาจะจัดเก็บข้อมูลใน UTC</span><span class="sxs-lookup"><span data-stu-id="c130a-118">When Human Resources writes a **Date and Time** value to the database, it stores the data in UTC.</span></span> <span data-ttu-id="c130a-119">การทำเช่นนี้จะช่วยให้ผู้ใช้สามารถดูข้อมูล **วันที่และเวลา** ใดๆ ที่เกี่ยวข้องกับโซนเวลาที่กำหนดไว้ในตัวเลือกผู้ใช้ของตนเองได้</span><span class="sxs-lookup"><span data-stu-id="c130a-119">This allows users to see any **Date and Time** data relative to the time zone defined in their user options.</span></span>
 
<span data-ttu-id="c130a-120">ในตัวอย่างข้างต้น เวลาเริ่มต้นคือเวลาที่ไม่ใช่วันที่เฉพาะ</span><span class="sxs-lookup"><span data-stu-id="c130a-120">In the example above, the start time is a point in time, not a particular date.</span></span> <span data-ttu-id="c130a-121">เมื่อเปลี่ยนโซนเวลาของผู้ใช้ที่ล็อกอินจาก GMT +12:00 เป็น GMT UTC เรกคอร์ดเดียวกันจะแสดง 04/30/2019 12:00:00 แทน 05/01/2019 12:00:00</span><span class="sxs-lookup"><span data-stu-id="c130a-121">By changing the time zone of the logged in user from GMT +12:00 to GMT UTC, the same record shows 04/30/2019 12:00:00 instead of 05/01/2019 12:00:00.</span></span>
  
<span data-ttu-id="c130a-122">ในตัวอย่างด้านล่าง การจ้างงานของพนักงาน 000724 จะกลายเป็นใช้งานอยู่ในเวลาเดียวกัน ไม่ว่าจะเป็นโซนเวลาใด</span><span class="sxs-lookup"><span data-stu-id="c130a-122">In the example below, employee 000724’s employment becomes active at the same time regardless of time zone.</span></span> <span data-ttu-id="c130a-123">พนักงานจะกลายเป็นใช้งานอยู่เมื่อ 04/30/2019 ในโซนเวลา GMT ซึ่งเหมือนกับ 05/01/2019 ในโซนเวลา GMT +12:00</span><span class="sxs-lookup"><span data-stu-id="c130a-123">The employee will be active on 04/30/2019 in the GMT time zone, which is the same as 05/01/2019 in GMT+12:00 time zone.</span></span> <span data-ttu-id="c130a-124">ทั้งสองอย่างอ้างอิงถึงช่วงเวลาเดียวกัน ไม่ใช่วันที่เฉพาะ</span><span class="sxs-lookup"><span data-stu-id="c130a-124">Both refer to the same point in time and not a particular date.</span></span> 

<span data-ttu-id="c130a-125">[![GMT ฟอร์มผู้ปฏิบัติงาน](./media/worker-form2.png)](./media/worker-form2.png)</span><span class="sxs-lookup"><span data-stu-id="c130a-125">[![Worker form GMT](./media/worker-form2.png)](./media/worker-form2.png)</span></span>

## <a name="date-and-time-data-in-data-management-framework-excel-dataverse-and-power-bi"></a><span data-ttu-id="c130a-126">ข้อมูลวันที่และเวลาในกรอบงานการจัดการข้อมูล, Excel, Dataverse, and Power BI</span><span class="sxs-lookup"><span data-stu-id="c130a-126">Date and Time data in Data Management Framework, Excel, Dataverse, and Power BI</span></span> 

<span data-ttu-id="c130a-127">การรายงานของกรอบงานการจัดการข้อมูล, Excel Add-In Dataverse และ Power BI ทั้งหมดได้รับการออกแบบมาเพื่อโต้ตอบกับข้อมูลในระดับฐานข้อมูลโดยตรง</span><span class="sxs-lookup"><span data-stu-id="c130a-127">The Data Management Framework, Excel Add-In, Dataverse, and Power BI reporting are all designed to interact with data directly on the database level.</span></span> <span data-ttu-id="c130a-128">เนื่องจากไม่มีไคลเอนต์ที่จะปรับปรุงข้อมูล **วันที่และเวลา** ไปยังโซนเวลาของผู้ใช้ ค่า **วันที่และเวลา** ทั้งหมดจะเป็น UTC ซึ่งอาจทำให้เกิดข้อสมมติฐานบางอย่างที่ไม่ถูกต้องเมื่อป้อนหรือดูข้อมูล</span><span class="sxs-lookup"><span data-stu-id="c130a-128">Since there's no client to adjust **Date and Time** data to the time zone of the user, all **Date and Time** values are in UTC, which can lead to some incorrect assumptions when entering or viewing data.</span></span>  
 
<span data-ttu-id="c130a-129">ข้อมูล **วันที่และเวลา** ที่ถูกส่งผ่าน DMF, Excel หรือ Dataverse จะถูกคาดว่าเป็น UTC โดยฐานข้อมูล</span><span class="sxs-lookup"><span data-stu-id="c130a-129">**Date and Time** data submitted via DMF, Excel, or Dataverse is assumed to be in UTC by the database.</span></span> <span data-ttu-id="c130a-130">ซึ่งอาจทำให้เกิดความสับสนได้เมื่อค่า **วันที่และเวลา** ที่ถูกส่งไม่แสดงตามที่คาดไว้เนื่องจากผู้ใช้ที่ดูข้อมูลไม่ได้ตั้งค่าโซนเวลาของผู้ใช้เป็น UTC</span><span class="sxs-lookup"><span data-stu-id="c130a-130">This can cause some confusion when the submitted **Date and Time** value doesn't display as expected because the user viewing the data doesn't have their user time zone  set to UTC.</span></span> 
 
<span data-ttu-id="c130a-131">สิ่งเดียวกันอาจเกิดขึ้นในทางกลับกันเมื่อมีการส่งออกข้อมูล</span><span class="sxs-lookup"><span data-stu-id="c130a-131">The same thing can happen in reverse when data is exported.</span></span> <span data-ttu-id="c130a-132">ข้อมูล **วันที่และเวลา** ในเอนทิตี้ DMF ที่ส่งออกอาจแตกต่างจากที่แสดงอยู่ในไคลเอนต์ Dynamics</span><span class="sxs-lookup"><span data-stu-id="c130a-132">The **Date and Time** data in the exported DMF entity can be different than what is displayed in the Dynamics client.</span></span> 
 
<span data-ttu-id="c130a-133">เมื่อใช้แหล่งข้อมูลภายนอกอย่าง DMF เพื่อดูหรือเขียนข้อมูล จะต้องคำนึงถึงว่าค่า **วันที่และเวลา** ถูกพิจารณาเป็นค่าเริ่มต้นเป็น UTC โดยไม่คำนึงถึงโซนเวลาของคอมพิวเตอร์ของผู้ใช้หรือการตั้งค่าโซนเวลาของผู้ใช้ปัจจุบัน</span><span class="sxs-lookup"><span data-stu-id="c130a-133">When using external sources like DMF to view or author data, keep in mind that the **Date and Time** values are considered by default to be in UTC regardless of the time zone of the user's computer or their current user time zone settings.</span></span> 

## <a name="examples-of-the-same-record-being-displayed-in-different-product-areas"></a><span data-ttu-id="c130a-134">ตัวอย่างของเรกคอร์ดชนิดเดียวกันที่แสดงอยู่ในพื้นที่ผลิตภัณฑ์ที่แตกต่างกัน</span><span class="sxs-lookup"><span data-stu-id="c130a-134">Examples of the same record being displayed in different product areas</span></span> 

<span data-ttu-id="c130a-135">**ทรัพยากรบุคคลกับโซนเวลาของผู้ใช้ตั้งค่าเป็น UTC**</span><span class="sxs-lookup"><span data-stu-id="c130a-135">**Human Resources with user time zone set to UTC**</span></span>

<span data-ttu-id="c130a-136">[![ฟอร์มผู้ปฏิบัติงานที่ตั้งค่าเป็น UTC](./media/worker-form3.png)](./media/worker-form3.png)</span><span class="sxs-lookup"><span data-stu-id="c130a-136">[![Worker form set to UTC](./media/worker-form3.png)](./media/worker-form3.png)</span></span>

<span data-ttu-id="c130a-137">**ทรัพยากรบุคคลกับโซนเวลาของผู้ใช้ตั้งค่าเป็น GMT+12:00**</span><span class="sxs-lookup"><span data-stu-id="c130a-137">**Human Resources with user time zone set to GMT +12:00**</span></span> 

<span data-ttu-id="c130a-138">[![ฟอร์มผู้ปฏิบัติงานที่ตั้งค่าเป็น GMT](./media/worker-form4.png)](./media/worker-form4.png)</span><span class="sxs-lookup"><span data-stu-id="c130a-138">[![Worker form set to GMT](./media/worker-form4.png)](./media/worker-form4.png)</span></span>

<span data-ttu-id="c130a-139">**Excel ผ่าน OData**</span><span class="sxs-lookup"><span data-stu-id="c130a-139">**Excel Via OData**</span></span>

<span data-ttu-id="c130a-140">[![Excel ผ่าน OData](./media/Excelviaodata.png)](./media/Excelviaodata.png)</span><span class="sxs-lookup"><span data-stu-id="c130a-140">[![Excel Via OData](./media/Excelviaodata.png)](./media/Excelviaodata.png)</span></span>

<span data-ttu-id="c130a-141">**การแบ่งระยะ DMF**</span><span class="sxs-lookup"><span data-stu-id="c130a-141">**DMF Staging**</span></span>

<span data-ttu-id="c130a-142">[![การแบ่งระยะ DMF](./media/DMFStaging.png)](./media/DMFStaging.png)</span><span class="sxs-lookup"><span data-stu-id="c130a-142">[![DMF Staging](./media/DMFStaging.png)](./media/DMFStaging.png)</span></span>

<span data-ttu-id="c130a-143">**ส่งออก DMF**</span><span class="sxs-lookup"><span data-stu-id="c130a-143">**DMF Export**</span></span>

<span data-ttu-id="c130a-144">[![ส่งออก DMF](./media/DMFexport.png)](./media/DMFexport.png)</span><span class="sxs-lookup"><span data-stu-id="c130a-144">[![DMF Export](./media/DMFexport.png)](./media/DMFexport.png)</span></span>

<span data-ttu-id="c130a-145">**Excel ผ่าน Dataverse**</span><span class="sxs-lookup"><span data-stu-id="c130a-145">**Excel via Dataverse**</span></span>

<span data-ttu-id="c130a-146">[![Excel ผ่าน Dataverse](./media/ExcelCDS.png)](./media/ExcelCDS.png)</span><span class="sxs-lookup"><span data-stu-id="c130a-146">[![Excel via Dataverse](./media/ExcelCDS.png)](./media/ExcelCDS.png)</span></span>

## <a name="see-also"></a><span data-ttu-id="c130a-147">ดูเพิ่มเติมที่</span><span class="sxs-lookup"><span data-stu-id="c130a-147">See also</span></span>

[<span data-ttu-id="c130a-148">ข้อมูลวันที่และเวลา</span><span class="sxs-lookup"><span data-stu-id="c130a-148">Date and time data</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/organization-administration/date-time-zones)<br></br>
[<span data-ttu-id="c130a-149">โซนเวลาที่ผู้ใช้ต้องการ</span><span class="sxs-lookup"><span data-stu-id="c130a-149">User preferred time zones</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/organization-administration/tasks/set-users-preferred-time-zone) 


[!INCLUDE[footer-include](../includes/footer-banner.md)]