---
title: ทำงานกับวันที่และเวลาใน Microsoft Dynamics 365 for Talent
description: ทำความเข้าใจสิ่งที่ควรคาดหวังเมื่อใช้ฟิลด์วันที่และเวลาใน Microsoft Dynamics 365 for Talent ทำให้ชัดเจนมากขึ้นในสิ่งที่คาดหวังเมื่อโต้ตอบกับข้อมูลวันที่และเวลาในฟอร์มใน Dynamics 365 for Talent แหล่งที่มาภายนอกหรือ Common Data Service
author: Darinkramer
manager: AnnBe
ms.date: 06/24/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: dkrame
ms.search.validFrom: 2019-06-06
ms.dyn365.ops.version: Talent
ms.openlocfilehash: b4c652992272ed1a5aecbb4c78f0d11f077149d1
ms.sourcegitcommit: 46bded82aa072adfedcf443629c2adc69f512c09
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 07/26/2019
ms.locfileid: "1791234"
---
# <a name="date-and-time-fields-in-talent"></a><span data-ttu-id="d4dd4-104">ฟิลด์วันที่และเวลาใน Talent</span><span class="sxs-lookup"><span data-stu-id="d4dd4-104">Date and Time fields in Talent</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="d4dd4-105">ฟิลด์ **วันที่และเวลา** แนวคิดพื้นฐานใน Dynamics 365 for Talent</span><span class="sxs-lookup"><span data-stu-id="d4dd4-105">**Date and Time** fields are a fundamental concept in Dynamics 365 for Talent.</span></span> <span data-ttu-id="d4dd4-106">นับเป็นสิ่งสำคัญที่จะต้องทำความเข้าใจวิธีการทำงานกับข้อมูล **วันที่และเวลา** ในฟอร์ม Dynamics 365, Common Data Service และแหล่งข้อมูลภายนอก</span><span class="sxs-lookup"><span data-stu-id="d4dd4-106">It's important to understand how to work with **Date and Time** data in a Dynamics 365 form, Common Data Service, and external sources.</span></span>

## <a name="understanding-the-difference-between-date-and-date-and-time-field-data-types"></a><span data-ttu-id="d4dd4-107">การทำความเข้าใจความแตกต่างระหว่างชนิดของข้อมูลในฟิลด์วันที่และวันที่และเวลา</span><span class="sxs-lookup"><span data-stu-id="d4dd4-107">Understanding the difference between Date and Date and Time field data types</span></span>

<span data-ttu-id="d4dd4-108">ฟิลด์ **วันที่และเวลา** มีข้อมูลโซนเวลา ในขณะที่ฟิลด์ **วันที่** ไม่มี</span><span class="sxs-lookup"><span data-stu-id="d4dd4-108">**Date and Time** fields contain time zone information, while **Date** fields don't.</span></span> <span data-ttu-id="d4dd4-109">ฟิลด์ **วันที่** แสดงข้อมูลเดียวกันในสถานที่ใดๆ</span><span class="sxs-lookup"><span data-stu-id="d4dd4-109">**Date** fields display the same information in any location.</span></span> <span data-ttu-id="d4dd4-110">เมื่อคุณป้อนวันที่ลงในฟิลด์ **วันที่** ผู้มีความสามารถพิเศษจะเขียนวันที่เดียวกันไปยังฐานข้อมูล</span><span class="sxs-lookup"><span data-stu-id="d4dd4-110">When you enter a date into a **Date** field, Talent writes that same date to the database.</span></span>

<span data-ttu-id="d4dd4-111">เมื่อแสดงข้อมูลในฟิลด์ **วันที่และเวลา** ผู้มีความสามารถพิเศษจะปรับปรุงวันที่และเวลาตามโซนเวลาของผู้ใช้ที่ตั้งค่าไว้ในฟอร์ม **ตัวเลือกผู้ใช้** (**ทั่วไป > การตั้งค่า > ตัวเลือกผู้ใช้**)</span><span class="sxs-lookup"><span data-stu-id="d4dd4-111">When displaying data in a **Date and Time** field, Talent adjusts the date and time based on the user's time zone set in the **User Options** form (**Common > Setup > User Options**).</span></span> <span data-ttu-id="d4dd4-112">ข้อมูลวันที่และเวลาที่คุณป้อนในฟิลด์อาจไม่เหมือนกับข้อมูลที่เขียนลงในฐานข้อมูล</span><span class="sxs-lookup"><span data-stu-id="d4dd4-112">The date and time information you enter in the field might not be the same as the information written to the database.</span></span>

<span data-ttu-id="d4dd4-113">[![ฟอร์มตัวเลือกผู้ใช้](./media/useroptionsform.png)](./media/useroptionsform.png)</span><span class="sxs-lookup"><span data-stu-id="d4dd4-113">[![User options form](./media/useroptionsform.png)](./media/useroptionsform.png)</span></span>

## <a name="understanding-date-and-time-fields-in-forms"></a><span data-ttu-id="d4dd4-114">การทำความเข้าใจฟิลด์วันที่และเวลาในฟอร์ม</span><span class="sxs-lookup"><span data-stu-id="d4dd4-114">Understanding Date and Time fields in forms</span></span> 

<span data-ttu-id="d4dd4-115">เมื่อป้อนข้อมูลในฟิลด์ **วันที่และเวลา** ข้อมูลที่แสดงบนหน้าจอจะไม่เหมือนกับข้อมูลที่จัดเก็บไว้ในฐานข้อมูล ถ้าโซนเวลาของผู้ใช้ไม่ได้รับการตั้งค่าเป็นเวลามาตรฐานสากล (UTC)</span><span class="sxs-lookup"><span data-stu-id="d4dd4-115">When entering data in a **Date and Time** field, the data displayed on the screen isn't the same as the data stored in the database if the user's time zone isn't set to Coordinated Universal Time (UTC).</span></span> <span data-ttu-id="d4dd4-116">ข้อมูลในฟิลด์ **วันที่และเวลา** จะถูกจัดเก็บเป็น UTC เสมอ</span><span class="sxs-lookup"><span data-stu-id="d4dd4-116">Data in **Date and Time** fields is always stored as UTC.</span></span>

<span data-ttu-id="d4dd4-117">[![ฟอร์มผู้ปฏิบัติงาน](./media/worker-form.png)](./media/worker-form.png)</span><span class="sxs-lookup"><span data-stu-id="d4dd4-117">[![Worker form](./media/worker-form.png)](./media/worker-form.png)</span></span>

## <a name="understand-date-and-time-fields-in-the-database"></a><span data-ttu-id="d4dd4-118">ทำความเข้าใจฟิลด์วันที่และเวลาในฐานข้อมูล</span><span class="sxs-lookup"><span data-stu-id="d4dd4-118">Understand Date and Time fields in the database</span></span> 

<span data-ttu-id="d4dd4-119">เมื่อผู้มีความสามารถพิเศษเขียนค่า **วันที่และเวลา** ไปยังฐานข้อมูล จะมีการจัดเก็บข้อมูลเป็น UTC</span><span class="sxs-lookup"><span data-stu-id="d4dd4-119">When Talent writes a **Date and time** value to the database, it stores the data in UTC.</span></span> <span data-ttu-id="d4dd4-120">การทำเช่นนี้จะช่วยให้ผู้ใช้สามารถดูข้อมูล **วันที่และเวลา** ใดๆ ที่เกี่ยวข้องกับโซนเวลาที่กำหนดไว้ในตัวเลือกผู้ใช้ของตนเองได้</span><span class="sxs-lookup"><span data-stu-id="d4dd4-120">This allows users to see any **Date and Time** data relative to the time zone defined in their user options.</span></span>
 
<span data-ttu-id="d4dd4-121">ในตัวอย่างข้างต้น เวลาเริ่มต้นคือเวลาที่ไม่ใช่วันที่เฉพาะ</span><span class="sxs-lookup"><span data-stu-id="d4dd4-121">In the example above, the start time is a point in time, not a particular date.</span></span> <span data-ttu-id="d4dd4-122">เมื่อเปลี่ยนโซนเวลาของผู้ใช้ที่ล็อกอินจาก GMT +12:00 เป็น GMT UTC เรกคอร์ดเดียวกันที่เพิ่งสร้างขึ้นจะแสดง 04/30/2019 12:00:00 แทน 05/01/2019 12:00:00</span><span class="sxs-lookup"><span data-stu-id="d4dd4-122">By changing the time zone of the logged in user from GMT +12:00 to GMT UTC, the same record just created shows 04/30/2019 12:00:00 instead of 05/01/2019 12:00:00.</span></span>
  
<span data-ttu-id="d4dd4-123">ในตัวอย่างด้านล่าง การจ้างงานของพนักงาน 000724 จะกลายเป็นใช้งานอยู่ในเวลาเดียวกัน ไม่ว่าจะเป็นโซนเวลาใด</span><span class="sxs-lookup"><span data-stu-id="d4dd4-123">In the example below, employee 000724’s employment becomes active at the same time regardless of time zone.</span></span> <span data-ttu-id="d4dd4-124">พนักงานจะกลายเป็นใช้งานอยู่เมื่อ 04/30/2019 ในโซนเวลา GMT ซึ่งเหมือนกับ 05/01/2019 ในโซนเวลา GMT +12:00</span><span class="sxs-lookup"><span data-stu-id="d4dd4-124">The employee will be active on 04/30/2019 in the GMT time zone, which is the same as 05/01/2019 in GMT+12:00 time zone.</span></span> <span data-ttu-id="d4dd4-125">ทั้งสองอย่างอ้างอิงถึงช่วงเวลาเดียวกัน ไม่ใช่วันที่เฉพาะ</span><span class="sxs-lookup"><span data-stu-id="d4dd4-125">Both refer to the same point in time and not a particular date.</span></span> 

<span data-ttu-id="d4dd4-126">[![ฟอร์มผู้ปฏิบัติงาน](./media/worker-form2.png)](./media/worker-form2.png)</span><span class="sxs-lookup"><span data-stu-id="d4dd4-126">[![Worker form](./media/worker-form2.png)](./media/worker-form2.png)</span></span>

## <a name="date-and-time-data-in-data-management-framework-excel-common-data-service-and-power-bi"></a><span data-ttu-id="d4dd4-127">ข้อมูลวันที่และเวลาในกรอบงานการจัดการข้อมูล, Excel, Common Data Service, and Power BI</span><span class="sxs-lookup"><span data-stu-id="d4dd4-127">Date and Time data in Data Management Framework, Excel, Common Data Service, and Power BI</span></span> 

<span data-ttu-id="d4dd4-128">การรายงานของกรอบงานการจัดการข้อมูล, Excel Add-In Common Data Service และ Power BI ทั้งหมดได้รับการออกแบบมาเพื่อโต้ตอบกับข้อมูลในระดับฐานข้อมูลโดยตรง</span><span class="sxs-lookup"><span data-stu-id="d4dd4-128">The Data Management Framework, Excel Add-In, Common Data Service, and Power BI reporting are all designed to interact with data directly on the database level.</span></span> <span data-ttu-id="d4dd4-129">เนื่องจากไม่มีไคลเอนต์ที่จะปรับปรุงข้อมูล **วันที่และเวลา** ไปยังโซนเวลาของผู้ใช้ ค่า **วันที่และเวลา** ทั้งหมดจะเป็น UTC ซึ่งอาจทำให้เกิดข้อสมมติฐานบางอย่างที่ไม่ถูกต้องเมื่อป้อนหรือดูข้อมูล</span><span class="sxs-lookup"><span data-stu-id="d4dd4-129">Since there is no client to adjust **Date and Time** data to the time zone of the user, all **Date and Time** values are in UTC, which can lead to some incorrect assumptions when entering or viewing data.</span></span>  
 
<span data-ttu-id="d4dd4-130">ข้อมูล **วันที่และเวลา** ที่ถูกส่งผ่าน DMF, Excel หรือ Common Data Service จะถูกคาดว่าเป็น UTC โดยฐานข้อมูล</span><span class="sxs-lookup"><span data-stu-id="d4dd4-130">**Date and Time** data that is submitted via DMF, Excel, or Common Data Service is assumed to be in UTC by the database.</span></span> <span data-ttu-id="d4dd4-131">ซึ่งอาจทำให้เกิดความสับสนได้เมื่อค่า **วันที่และเวลา** ที่ถูกส่งไม่แสดงตามที่คาดไว้เนื่องจากผู้ใช้ที่ดูข้อมูลไม่ได้ตั้งค่าโซนเวลาของผู้ใช้เป็น UTC</span><span class="sxs-lookup"><span data-stu-id="d4dd4-131">This can cause some confusion when the submitted **Date and Time** value doesn't display as expected because the user viewing the data doesn't have their user time zone  set to UTC.</span></span> 
 
<span data-ttu-id="d4dd4-132">สิ่งเดียวกันอาจเกิดขึ้นในทางกลับกันเมื่อมีการส่งออกข้อมูล</span><span class="sxs-lookup"><span data-stu-id="d4dd4-132">The same thing can happen in reverse when data is exported.</span></span> <span data-ttu-id="d4dd4-133">ข้อมูล **วันที่และเวลา** ในเอนทิตี้ DMF ที่ส่งออกอาจแตกต่างจากที่แสดงอยู่ในไคลเอนต์ Dynamics</span><span class="sxs-lookup"><span data-stu-id="d4dd4-133">The **Date and Time** data in the exported DMF entity can be different then what is displayed in the Dynamics client.</span></span> 
 
<span data-ttu-id="d4dd4-134">เมื่อใช้แหล่งข้อมูลภายนอกอย่าง DMF เพื่อดูหรือเขียนข้อมูล จะต้องคำนึงถึงว่าค่า **วันที่และเวลา** ถูกพิจารณาเป็นค่าเริ่มต้นเป็น UTC โดยไม่คำนึงถึงโซนเวลาของคอมพิวเตอร์ของผู้ใช้หรือการตั้งค่าโซนเวลาของผู้ใช้ปัจจุบัน</span><span class="sxs-lookup"><span data-stu-id="d4dd4-134">When using external sources like DMF to view or author data, it is important to keep in mind that the **Date and Time** values are considered by default to be in UTC regardless of the time zone of the user's computer or their current user time zone settings.</span></span> 

## <a name="examples-of-the-same-record-being-displayed-in-different-product-areas"></a><span data-ttu-id="d4dd4-135">ตัวอย่างของเรกคอร์ดชนิดเดียวกันที่แสดงอยู่ในพื้นที่ผลิตภัณฑ์ที่แตกต่างกัน</span><span class="sxs-lookup"><span data-stu-id="d4dd4-135">Examples of the same record being displayed in different product areas</span></span> 

<span data-ttu-id="d4dd4-136">**ผู้มีความสามารถพิเศษที่ตั้งค่าโซนเวลาของผู้ใช้เป็น UTC**</span><span class="sxs-lookup"><span data-stu-id="d4dd4-136">**Talent with user time zone set to UTC**</span></span>

<span data-ttu-id="d4dd4-137">[![ฟอร์มผู้ปฏิบัติงาน](./media/worker-form3.png)](./media/worker-form3.png)</span><span class="sxs-lookup"><span data-stu-id="d4dd4-137">[![Worker form](./media/worker-form3.png)](./media/worker-form3.png)</span></span>

<span data-ttu-id="d4dd4-138">**ผู้มีความสามารถพิเศษที่ตั้งค่าโซนเวลาของผู้ใช้เป็น GMT +12:00**</span><span class="sxs-lookup"><span data-stu-id="d4dd4-138">**Talent with user time zone set to GMT +12:00**</span></span> 

<span data-ttu-id="d4dd4-139">[![ฟอร์มผู้ปฏิบัติงาน](./media/worker-form4.png)](./media/worker-form4.png)</span><span class="sxs-lookup"><span data-stu-id="d4dd4-139">[![Worker form](./media/worker-form4.png)](./media/worker-form4.png)</span></span>

<span data-ttu-id="d4dd4-140">**Excel ผ่าน OData**</span><span class="sxs-lookup"><span data-stu-id="d4dd4-140">**Excel Via OData**</span></span>

<span data-ttu-id="d4dd4-141">[![Excel ผ่าน OData](./media/Excelviaodata.png)](./media/Excelviaodata.png)</span><span class="sxs-lookup"><span data-stu-id="d4dd4-141">[![Excel Via OData](./media/Excelviaodata.png)](./media/Excelviaodata.png)</span></span>

<span data-ttu-id="d4dd4-142">**การแบ่งระยะ DMF**</span><span class="sxs-lookup"><span data-stu-id="d4dd4-142">**DMF Staging**</span></span>

<span data-ttu-id="d4dd4-143">[![การแบ่งระยะ DMF](./media/DMFStaging.png)](./media/DMFStaging.png)</span><span class="sxs-lookup"><span data-stu-id="d4dd4-143">[![DMF Staging](./media/DMFStaging.png)](./media/DMFStaging.png)</span></span>

<span data-ttu-id="d4dd4-144">**ส่งออก DMF**</span><span class="sxs-lookup"><span data-stu-id="d4dd4-144">**DMF Export**</span></span>

<span data-ttu-id="d4dd4-145">[![การแบ่งระยะ DMF](./media/DMFexport.png)](./media/DMFexport.png)</span><span class="sxs-lookup"><span data-stu-id="d4dd4-145">[![DMF Staging](./media/DMFexport.png)](./media/DMFexport.png)</span></span>

<span data-ttu-id="d4dd4-146">**Excel ผ่าน Common Data Service**</span><span class="sxs-lookup"><span data-stu-id="d4dd4-146">**Excel via Common Data Service**</span></span>

<span data-ttu-id="d4dd4-147">[![Excel ผ่าน Common Data Service](./media/ExcelCDS.png)](./media/ExcelCDS.png)</span><span class="sxs-lookup"><span data-stu-id="d4dd4-147">[![Excel via Common Data Service](./media/ExcelCDS.png)](./media/ExcelCDS.png)</span></span>

### <a name="see-also"></a><span data-ttu-id="d4dd4-148">ดูเพิ่มเติมที่</span><span class="sxs-lookup"><span data-stu-id="d4dd4-148">See also</span></span>

[<span data-ttu-id="d4dd4-149">ข้อมูลวันที่และเวลา</span><span class="sxs-lookup"><span data-stu-id="d4dd4-149">Date and time data</span></span>](https://docs.microsoft.com/en-us/dynamics365/unified-operations/fin-and-ops/organization-administration/date-time-zones)<br></br>
[<span data-ttu-id="d4dd4-150">โซนเวลาที่ผู้ใช้ต้องการ</span><span class="sxs-lookup"><span data-stu-id="d4dd4-150">User preferred time zones</span></span>](https://docs.microsoft.com/en-us/dynamics365/unified-operations/fin-and-ops/organization-administration/tasks/set-users-preferred-time-zone) 
