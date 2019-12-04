---
title: ขยาย Talent ด้วย Power Apps และ Power Automate
description: หัวข้อนี้อธิบายถึงตัวอย่างบางอย่างของสถานการณ์สมมุติของการเพิ่มความสามารถของ Microsoft Dynamics 365 Talent ที่ใช้ Microsoft Power Apps และ Microsoft Power Automate
author: negudava
manager: Annbe
ms.date: 05/01/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: Dynamics 365 Talent;PowerApps;Flow;Common Data Service
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent;Core;Experience Apps
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: negudava
ms.search.validFrom: 2019-03-04
ms.dyn365.ops.version: Talent October 2018 update
ms.openlocfilehash: 3bb61297e294aa3f2d06f542bebe29d7afae9c3b
ms.sourcegitcommit: 9cc6a011bfdd1b0fe505760b6bf429eb6c65862a
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 11/25/2019
ms.locfileid: "2832849"
---
# <a name="extend-talent-with-power-apps-and-power-automate"></a><span data-ttu-id="8a2a5-103">ขยาย Talent ด้วย Power Apps และ Power Automate</span><span class="sxs-lookup"><span data-stu-id="8a2a5-103">Extend Talent with Power Apps and Power Automate</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="8a2a5-104">หัวข้อนี้อธิบายถึงตัวอย่างบางอย่างของสถานการณ์สมมุติของการเพิ่มความสามารถของ Microsoft Dynamics 365 Talent ที่ใช้ Microsoft Power Apps และ Microsoft Power Automate</span><span class="sxs-lookup"><span data-stu-id="8a2a5-104">This topic describes some examples of extensibility scenarios for Microsoft Dynamics 365 Talent that use Microsoft Power Apps and Microsoft Power Automate.</span></span> <span data-ttu-id="8a2a5-105">คุณสามารถนำเข้าโซลูชันแพคเกจที่เชื่อมโยงกับแต่ละตัวอย่างไปยังสภาพแวดล้อม Power Apps ของคุณ</span><span class="sxs-lookup"><span data-stu-id="8a2a5-105">You can import the solution package that is associated with each example into your Power Apps environment.</span></span> <span data-ttu-id="8a2a5-106">จากนั้นคุณสามารถใช้แพคเกจเป็นคำแนะนำหรือเป็นจุดเริ่มต้นเพื่อนำสถานการณ์ที่สามารถใช้ได้กับองค์กรของคุณไปใช้</span><span class="sxs-lookup"><span data-stu-id="8a2a5-106">You can then use the packages either as guidance or as starting points to implement scenarios that are applicable to your organization.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="8a2a5-107">ถ้าคุณต้องการใช้เท็มเพลตและแอพลิเคชันที่อธิบายไว้ในหัวข้อนี้ "ตามที่เป็น" ให้แน่ใจว่าได้ทดสอบแล้วเพื่อให้แน่ใจว่าจะครอบคลุมสถานการณ์จำลองทั้งหมดที่เกี่ยวข้องกับการนำไปใช้ของคุณโดยเฉพาะ</span><span class="sxs-lookup"><span data-stu-id="8a2a5-107">If you want to use the templates and app that are described in this topic "as is," be sure to test them to make sure that they cover all the scenarios that are specific to your implementation.</span></span>


## <a name="prerequisites"></a><span data-ttu-id="8a2a5-108">ข้อกำหนดเบื้องต้น</span><span class="sxs-lookup"><span data-stu-id="8a2a5-108">Prerequisites</span></span>

- <span data-ttu-id="8a2a5-109">เมื่อต้องการนำเข้าแพคเกจ ผู้ใช้ต้องมีสิทธิ์ **ผู้สร้างสภาพแวดล้อม**</span><span class="sxs-lookup"><span data-stu-id="8a2a5-109">To import packages, users must have the **Environment Maker** permission.</span></span>
- <span data-ttu-id="8a2a5-110">เมื่อต้องการส่งออกหรือนำเข้าแอป ผู้ใช้ต้องมีใบอนุญาตใช้ Power Apps Plan 2 หรือใบอนุญาตในการทดลองใช้ Power Apps Plan 2</span><span class="sxs-lookup"><span data-stu-id="8a2a5-110">To export or import apps, users must have a Power Apps Plan 2 license or a Power Apps Plan 2 trial license.</span></span>

## <a name="power-automate--form-connect"></a><span data-ttu-id="8a2a5-111">Power Automate – การเชื่อมต่อฟอร์ม</span><span class="sxs-lookup"><span data-stu-id="8a2a5-111">Power Automate – Form Connect</span></span>

<span data-ttu-id="8a2a5-112">แม่แบบ **Power Automate – การเชื่อมต่อฟอร์ม** สามารถนำมาใช้เพื่ออ่านข้อมูลจาก Microsoft Forms และจัดเก็บไว้ในเอนทิตี Common Data Service ได้</span><span class="sxs-lookup"><span data-stu-id="8a2a5-112">The **Power Automate – Form Connect** template can be used to read data from Microsoft Forms and store it in a Common Data Service entity.</span></span>

<span data-ttu-id="8a2a5-113">เท็มเพลตนี้สามารถขยายได้เพื่อให้สามารถใช้สำหรับสถานการณ์จำลองอื่น ๆ</span><span class="sxs-lookup"><span data-stu-id="8a2a5-113">This template can be extended so that it can be used for other scenarios.</span></span> <span data-ttu-id="8a2a5-114">ยกตัวอย่างเช่น</span><span class="sxs-lookup"><span data-stu-id="8a2a5-114">Here are some examples:</span></span>

- <span data-ttu-id="8a2a5-115">รวบรวมการประเมินผู้สมัคร</span><span class="sxs-lookup"><span data-stu-id="8a2a5-115">Capture candidate assessments.</span></span>
- <span data-ttu-id="8a2a5-116">รวบรวมผลลัพธ์จากแบบสอบถามของหลักสูตร</span><span class="sxs-lookup"><span data-stu-id="8a2a5-116">Capture results from course questionnaires.</span></span>
- <span data-ttu-id="8a2a5-117">คอมไพล์ไลบรารีของคำถามสัมภาษณ์สำหรับผู้ดูแลฝ่ายทรัพยากรบุคคล (HR)</span><span class="sxs-lookup"><span data-stu-id="8a2a5-117">Compile a library of interview questions for Human resources (HR) administrators.</span></span>
- <span data-ttu-id="8a2a5-118">เก็บรวบรวมการประเมินของผู้สมัครของกระบวนการสัมภาษณ์</span><span class="sxs-lookup"><span data-stu-id="8a2a5-118">Capture a candidate's evaluation of the interview process</span></span>

<span data-ttu-id="8a2a5-119">ใน Microsoft Dynamics 365: Attract แบบฟอร์มสามารถปรากฏอยู่ในพอร์ทัลของผู้สมัคร และผู้สมัครสามารถกรอกข้อมูลโดยใส่รายละเอียดได้</span><span class="sxs-lookup"><span data-stu-id="8a2a5-119">In Microsoft Dynamics 365: Attract, forms can appear in Candidate portal, and candidates can fill in details.</span></span> <span data-ttu-id="8a2a5-120">นอกจากนี้คุณยังสามารถฝังแบบฟอร์มเป็นกิจกรรมในเท็มเพลตงานได้อีกด้วย</span><span class="sxs-lookup"><span data-stu-id="8a2a5-120">Forms can also be embedded as activities in a job template.</span></span>

<span data-ttu-id="8a2a5-121">เมื่อผู้สมัครส่งฟอร์ม Microsoft Power Automate จะเก็บรวบรวมการส่งฟอร์ม อ่านข้อมูล และเก็บไว้ในเอนทิตี Common Data Service</span><span class="sxs-lookup"><span data-stu-id="8a2a5-121">When a candidate submits a form, Microsoft Power Automate captures the form submission, reads the data, and stores it in the Common Data Service entity.</span></span>

<span data-ttu-id="8a2a5-122">เมื่อต้องการดาวน์โหลดแม่แบบ **Power Automate – การเชื่อมต่อฟอร์ม** และโครงสร้างการกำหนดเอนทิตีด้วยตนเอง ไปที่ [Power Automate – การเชื่อมต่อฟอร์ม](https://go.microsoft.com/fwlink/?linkid=2081988) บนศูนย์ดาวน์โหลด Microsoft</span><span class="sxs-lookup"><span data-stu-id="8a2a5-122">To download the **Power Automate – Form Connect** template and Custom Entity Structure, go to [Power Automate – Form Connect](https://go.microsoft.com/fwlink/?linkid=2081988) on the Microsoft Download Center.</span></span>

## <a name="initiate-and-extract-parameters-passed-to-power-apps"></a><span data-ttu-id="8a2a5-123">เริ่มต้นและแยกพารามิเตอร์ที่ส่งผ่านไปยัง Power Apps</span><span class="sxs-lookup"><span data-stu-id="8a2a5-123">Initiate and Extract Parameters Passed to Power Apps</span></span>

<span data-ttu-id="8a2a5-124">คุณสามารถใช้แม่แบบ **เริ่มต้นและแยกพารามิเตอร์ที่ส่งผ่านไปยัง Power Apps** โดยเป็นจุดเริ่มต้นสำหรับสถานการณ์จำลองของ Power Apps ที่เกี่ยวข้องกับ Attract โดยเฉพาะได้</span><span class="sxs-lookup"><span data-stu-id="8a2a5-124">The **Initiate and Extract Parameters Passed to Power Apps** template can be used as a starting point for any Power Apps scenario that is specific to Attract.</span></span> <span data-ttu-id="8a2a5-125">ซึ่งประกอบด้วยพารามิเตอร์เริ่มต้นทั้งหมดที่ถูกส่งผ่านโดย Attract เช่น **ใบสมัครงาน**, **รหัสผู้สมัคร** และ **JobID**</span><span class="sxs-lookup"><span data-stu-id="8a2a5-125">It includes all the default parameters that are passed by Attract, such as **Job Application**, **Candidate ID**, and **JobID**.</span></span>

<span data-ttu-id="8a2a5-126">คุณสามารถใช้เท็มเพลตนี้เพื่อดึงข้อมูลแบบฟอร์มการประเมินผู้สมัครเพื่อให้ผู้จัดการที่ว่าจ้างสามารถดูการประเมินที่ผู้สมัครกรอกไว้ได้</span><span class="sxs-lookup"><span data-stu-id="8a2a5-126">This template can be used to retrieve a candidate assessment form, so that a hiring manager can view the assessment that a candidate filled in.</span></span>

<span data-ttu-id="8a2a5-127">แอปที่สร้างขึ้นโดยใช้ Power Apps สามารถฝังไว้ในเท็มเพลตงานใน Attract ได้</span><span class="sxs-lookup"><span data-stu-id="8a2a5-127">Apps that are created by using Power Apps can be embedded into the job template in Attract.</span></span>

<span data-ttu-id="8a2a5-128">เมื่อต้องการดาวน์โหลดแม่แบบ **เริ่มต้นและแยกพารามิเตอร์ที่ส่งผ่านไปยัง Power Apps** และโครงสร้างการกำหนดเอนทิตีด้วยตนเอง ไปที่ [เริ่มต้นและแยกพารามิเตอร์ที่ส่งผ่านไปยัง Power Apps](https://go.microsoft.com/fwlink/?linkid=2081991) บนศูนย์ดาวน์โหลด Microsoft</span><span class="sxs-lookup"><span data-stu-id="8a2a5-128">To download the **Initiate and Extract Parameters Passed to Power Apps** template and Custom Entity Structure, go to [Initiate and Extract Parameters Passed to Power Apps](https://go.microsoft.com/fwlink/?linkid=2081991) on the Microsoft Download Center.</span></span>

## <a name="integration-with-office-365"></a><span data-ttu-id="8a2a5-129">การรวมกับ Office 365</span><span class="sxs-lookup"><span data-stu-id="8a2a5-129">Integration with Office 365</span></span>

<span data-ttu-id="8a2a5-130">คุณสามารถใช้แอป **การรวมกับ Office 365** ในการดึงข้อมูลของทีมงานสำหรับผู้ใช้ที่ลงชื่อเข้าใช้จาก Microsoft Office 365 ได้</span><span class="sxs-lookup"><span data-stu-id="8a2a5-130">The **Integration with Office 365** app can be used to extract team information for signed-in users from Microsoft Office 365.</span></span> <span data-ttu-id="8a2a5-131">ซึ่งจะอ้างอิงถึงผู้ปฏิบัติงานใน Talent เพื่อแยกรายละเอียดการตอกบัตรเข้าและตอกบัตรออกและการบันทึกข้อยกเว้น</span><span class="sxs-lookup"><span data-stu-id="8a2a5-131">It references workers in Talent to extract clock-in and clock-out details and exception recordings.</span></span> <span data-ttu-id="8a2a5-132">รายละเอียดการตอกบัตรเข้าและตอกบัตรออกถูกจัดเก็บไว้ในเอนทิตี้ Common Data Service แบบกำหนดเอง</span><span class="sxs-lookup"><span data-stu-id="8a2a5-132">Clock-in and Clock-out details are stored in custom Common Data Service entities.</span></span> <span data-ttu-id="8a2a5-133">ข้อสมมติฐานคือว่ารายละเอียดเหล่านี้จะถูกกรอกข้อมูลจากระบบภายนอกผ่านการรวม</span><span class="sxs-lookup"><span data-stu-id="8a2a5-133">The assumption is that these details are filled in from third-party systems via integration.</span></span>

<span data-ttu-id="8a2a5-134">แอปนี้สามารถขยายได้เพื่อให้สามารถใช้สำหรับสถานการณ์จำลองอื่น ๆ</span><span class="sxs-lookup"><span data-stu-id="8a2a5-134">This app can be extended so that it can be used for other scenarios.</span></span> <span data-ttu-id="8a2a5-135">ตัวอย่างเช่น สามารถใช้เพื่อแสดงข้อมูลวันหยุดพักผ่อนของทีมงาน ปฏิทินเหตุการณ์ และเหตุการณ์เฉพาะทีมงานใด ๆ</span><span class="sxs-lookup"><span data-stu-id="8a2a5-135">For example, it can be used to show team vacation information, calendar events, and any team-specific events.</span></span>

<span data-ttu-id="8a2a5-136">เมื่อต้องการดาวน์โหลดแอป **การรวมกับ Office 365** และโครงสร้างของเอนทิตี้แบบกำหนดเอง ไปที่ [การรวมกับ Office 365](https://go.microsoft.com/fwlink/?linkid=2081787) บนศูนย์ดาวน์โหลด Microsoft</span><span class="sxs-lookup"><span data-stu-id="8a2a5-136">To download the **Integration with Office 365** app and Custome Entity Structure, go to [Integration with Office 365](https://go.microsoft.com/fwlink/?linkid=2081787) on the Microsoft Download Center.</span></span>

## <a name="power-automate--email-notification"></a><span data-ttu-id="8a2a5-137">Power Automate– การแจ้งเตือนทางอีเมล</span><span class="sxs-lookup"><span data-stu-id="8a2a5-137">Power Automate – Email Notification</span></span>

<span data-ttu-id="8a2a5-138">คุณสามารถใช้แม่แบบ **Power Automate – การแจ้งเตือนทางอีเมล** สำหรับสถานการณ์จำลองการแจ้งเตือนทางอีเมล</span><span class="sxs-lookup"><span data-stu-id="8a2a5-138">The **Power Automate – Email Notification** template can be used for email notification scenarios.</span></span> <span data-ttu-id="8a2a5-139">ซึ่งสามารถใช้เพื่อทริกเกอร์อีเมลแจ้งเตือนให้กับผู้สมัครที่ทีมการว่าจ้างปฏิเสธในระหว่างขั้นใดๆ ของกระบวนการสรรหาบุคลากร</span><span class="sxs-lookup"><span data-stu-id="8a2a5-139">It can be used to trigger notification emails to candidates that the hiring team rejects during any stage of the recruiting process.</span></span>

<span data-ttu-id="8a2a5-140">คุณสามารถขยายเท็มเพลตนี้เพื่อติดตามการเปลี่ยนแปลงขั้นของผู้สมัครตลอดทั้งกระบวนการสรรหาบุคลากร และเพื่อส่งการแจ้งเตือนไปยังทีมงานการจ้างงานและผู้สมัคร</span><span class="sxs-lookup"><span data-stu-id="8a2a5-140">This template can be extended to track changes to the candidate stage throughout the recruiting process, and to send notifications to the hiring team and candidate.</span></span>

<span data-ttu-id="8a2a5-141">โดยทั่วไป สำหรับเอนทิตีที่จัดเก็บใน Common Data Service สามารถตั้งค่าขั้นตอนเพื่อส่งการแจ้งเตือนสำหรับเหตุการณ์ที่เกิดขึ้นใน Core HR, Attract หรือ Onboard</span><span class="sxs-lookup"><span data-stu-id="8a2a5-141">In general, for entities that are stored in Common Data Service, flows can be set up to send notifications for events that occur in Core HR, Attract, or Onboard.</span></span>

<span data-ttu-id="8a2a5-142">เมื่อต้องการดาวน์โหลดแม่แบบ **Power Automate – การแจ้งเตือนทางอีเมล** ไปที่ [Power Automate – การแจ้งเตือนทางอีเมล](https://go.microsoft.com/fwlink/?linkid=2082103) บนศูนย์ดาวน์โหลด Microsoft</span><span class="sxs-lookup"><span data-stu-id="8a2a5-142">To download the **Power Automate – Email Notification** template, go to [Power Automate – Email Notification](https://go.microsoft.com/fwlink/?linkid=2082103) on the Microsoft Download Center.</span></span>

## <a name="power-automate--sql-connect-and-execute"></a><span data-ttu-id="8a2a5-143">Power Automate – การเชื่อมต่อและดำเนินการ SQL</span><span class="sxs-lookup"><span data-stu-id="8a2a5-143">Power Automate – SQL Connect and execute</span></span>

<span data-ttu-id="8a2a5-144">แม่แบบ **Power Automate – การเชื่อมต่อและดำเนินการ SQL** เชื่อมต่อกับ Microsoft SQL Server และเปิดใช้งานให้การสอบถาม SQL รัน</span><span class="sxs-lookup"><span data-stu-id="8a2a5-144">The **Power Automate – SQL Connect and execute** template connects to Microsoft SQL Server and enables SQL queries to be run.</span></span>

<span data-ttu-id="8a2a5-145">ถึงแม้ว่าเท็มเพลตนี้จะมีวัตถุประสงค์เพื่ออ่านและอัพเดตตาราง SQL แต่ก็ยังสามารถขยายเพื่อให้สามารถใช้สำหรับสถานการณ์จำลองอื่น ๆ ได้</span><span class="sxs-lookup"><span data-stu-id="8a2a5-145">Although this template is designed to read and update SQL tables, it can be extended so that it can be used for other scenarios.</span></span> <span data-ttu-id="8a2a5-146">ตัวอย่างเช่น สามารถใช้เพื่อกรอกข้อมูลในตารางการจัดเตรียมใน Common Data Service ด้วยเรกคอร์ดจาก SQL Server และเพื่อซิงโครไนส์ตารางการจัดเตรียมเป็นระยะ ๆ โดยใช้พุชส่วนเพิ่มจาก SQL Server</span><span class="sxs-lookup"><span data-stu-id="8a2a5-146">For example, it can be used to fill a staging table in Common Data Service with records from SQL Server, and to periodically synchronize the staging table by using an incremental push from SQL Server.</span></span>

<span data-ttu-id="8a2a5-147">เมื่อต้องการดาวน์โหลดแม่แบบ **Power Automate – การเชื่อมต่อและดำเนินการ SQL** ไปที่ [Power Automate – การเชื่อมต่อและดำเนินการ SQL](https://go.microsoft.com/fwlink/?linkid=2081789) บนศูนย์ดาวน์โหลด Microsoft</span><span class="sxs-lookup"><span data-stu-id="8a2a5-147">To download the **Power Automate – SQL Connect and execute** template, go to [Power Automate – SQL Connect and execute](https://go.microsoft.com/fwlink/?linkid=2081789) on the Microsoft Download Center.</span></span>

## <a name="power-automate--sharepoint-integration"></a><span data-ttu-id="8a2a5-148">Power Automate – การรวม SharePoint</span><span class="sxs-lookup"><span data-stu-id="8a2a5-148">Power Automate – SharePoint Integration</span></span>

<span data-ttu-id="8a2a5-149">คุณสามารถใช้แม่แบบ **Power Automate – การรวม SharePoint** เพื่ออ่านข้อมูลจากรายการ Microsoft SharePoint เปรียบเทียบรายการที่มีค่าฟิลด์สำหรับเอนทิตี Common Data Service ใด ๆ และส่งผลลัพธ์ของการเปรียบเทียบเป็นอีเมลการแจ้งเตือนได้</span><span class="sxs-lookup"><span data-stu-id="8a2a5-149">The **Power Automate – SharePoint Integration** template can be used to read data from a Microsoft SharePoint list, compare the list with field values for any Common Data Service entity, and send the results of the comparison as a notification email.</span></span> 

<span data-ttu-id="8a2a5-150">องค์กรอาจมีชุดของทักษะที่ต้องใช้โดยทันที</span><span class="sxs-lookup"><span data-stu-id="8a2a5-150">An organization might have a set of skills that it urgently requires.</span></span> <span data-ttu-id="8a2a5-151">คุณสามารถจัดเก็บทักษะเหล่านี้ใน SharePoint เป็นรายการ SharePoint</span><span class="sxs-lookup"><span data-stu-id="8a2a5-151">These skills can be stored in SharePoint as a SharePoint list.</span></span> <span data-ttu-id="8a2a5-152">เมื่อผู้สมัครสมัครสำหรับงานใด ๆ ที่มีแสดงรายการชุดของทักษะที่จำเป็น ถ้ามีการจับคู่ที่มีนัยสำคัญระหว่างทักษะของผู้สมัครและทักษะที่เก็บไว้ใน SharePoint จะมีการส่งอีเมลการแจ้งเตือน</span><span class="sxs-lookup"><span data-stu-id="8a2a5-152">When a candidate applies for any job that a set of required skills is listed for, if there is a significant match between the candidate's skill and the skills that are stored in SharePoint, a notification email is sent.</span></span> <span data-ttu-id="8a2a5-153">ด้วยวิธีนี้ ตำแหน่งที่จำเป็นต้องจัดหาโดยทันทีจะได้รับการจัดหารวดเร็วขึ้น เนื่องจากการแจ้งเตือนจะช่วยให้ผู้สรรหาสามารถติดต่อและว่าจ้างผู้สมัครได้ทั่วทั้งองค์กร</span><span class="sxs-lookup"><span data-stu-id="8a2a5-153">In this way, positions that are urgently required are filled faster, because the notifications help recruiters reach out and cross-hire candidates throughout the organization.</span></span>

<span data-ttu-id="8a2a5-154">คุณสามารถขยายเท็มเพลตนี้เพื่อให้สามารถใช้สำหรับสถานการณ์จำลองใด ๆ ที่เกี่ยวข้องกับการรวม SharePoint ได้</span><span class="sxs-lookup"><span data-stu-id="8a2a5-154">This template can be extended so that it can be used for any scenario that involves SharePoint integration.</span></span>

<span data-ttu-id="8a2a5-155">เมื่อต้องการดาวน์โหลดแม่แบบ **Power Automate – การรวม SharePoint** ไปที่ [Power Automate – กาารรวม SharePoint](https://go.microsoft.com/fwlink/?linkid=2082109) บนศูนย์ดาวน์โหลด Microsoft</span><span class="sxs-lookup"><span data-stu-id="8a2a5-155">To download the **Power Automate – SharePoint Integration** template, go to [Power Automate – SharePoint Integration](https://go.microsoft.com/fwlink/?linkid=2082109) on the Microsoft Download Center.</span></span>

## <a name="referral-app"></a><span data-ttu-id="8a2a5-156">แอปการอ้างอิง</span><span class="sxs-lookup"><span data-stu-id="8a2a5-156">Referral App</span></span>
<span data-ttu-id="8a2a5-157">คุณสามารถใช้แอปการอ้างอิงเพื่อเพิ่มผู้สมัครในกลุ่มผู้มีความสามารถพิเศษที่ใช้ร่วมกัน</span><span class="sxs-lookup"><span data-stu-id="8a2a5-157">You can use the Referral App to add candidates to a shared talent pool.</span></span> <span data-ttu-id="8a2a5-158">การอ้างอิงสามารถป้อน **Firstname** **Lastname** **อีเมล** และ **URL ของ LinkedIn** เมื่อส่งผู้สมัคร</span><span class="sxs-lookup"><span data-stu-id="8a2a5-158">The referrer can enter **Firstname**, **Lastname**, **Email**, and **Linkedln URL** when submitting a candidate.</span></span> <span data-ttu-id="8a2a5-159">ข้อมูลเมตาของแหล่งที่มาของผู้สมัครจะถูกเติมด้วยข้อมูลของบุคคลอ้างอิง</span><span class="sxs-lookup"><span data-stu-id="8a2a5-159">The candidate source metadata is then populated with the referrer’s information.</span></span>

<span data-ttu-id="8a2a5-160">คุณสามารถฝังแอปนี้ในระบบพนักงานบริการตนเอง (ESS) สำหรับการส่งการอ้างอิง หรือคุณสามารถใช้เป็นไฮเปอร์ลิงค์ในเว็บไซต์องค์กรและรันเป็นแอปเอกเทศ</span><span class="sxs-lookup"><span data-stu-id="8a2a5-160">You can embed this app in Employee self-service (ESS) for submitting referrals, or you can be use it as a hyperlink in the Corporate Portal and run as a stand-alone app.</span></span>

<span data-ttu-id="8a2a5-161">เมื่อต้องการดาวน์โหลด **แอปการอ้างอิง** ไปที่ [โซลูชันความสามารถในการเพิ่มฟังก์ชัน Dynamics 365 Talent : แอปการอ้างอิง](http://www.microsoft.com/downloads/details.aspx?FamilyID=9a59c9d1-f8a1-4d4d-b768-cfc4f4eb9d0d) บนศูนย์การดาวน์โหลดของ Microsoft</span><span class="sxs-lookup"><span data-stu-id="8a2a5-161">To download **Referral App**, go to [Dynamics 365 Talent extensibility solution: Referral App](http://www.microsoft.com/downloads/details.aspx?FamilyID=9a59c9d1-f8a1-4d4d-b768-cfc4f4eb9d0d) on the Microsoft Download Center.</span></span> <span data-ttu-id="8a2a5-162">คุณสามารถนำเข้าแอปนี้และเลือกกำหนดเพื่อเพิ่มฟังก์ชันเพิ่มเติมได้</span><span class="sxs-lookup"><span data-stu-id="8a2a5-162">You can import this app and customize it to add additional functionality.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="8a2a5-163">แหล่งข้อมูลเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="8a2a5-163">Additional resources</span></span>

[<span data-ttu-id="8a2a5-164">Microsoft Power Platform</span><span class="sxs-lookup"><span data-stu-id="8a2a5-164">The Microsoft Power Platform</span></span>](https://docs.microsoft.com/power-platform/admin/admin-documentation)

[<span data-ttu-id="8a2a5-165">ย้ายแอประหว่างผู้เช่าและสภาพแวดล้อม</span><span class="sxs-lookup"><span data-stu-id="8a2a5-165">Migrate app between tenants and environments</span></span>](https://docs.microsoft.com/power-platform/admin/environment-and-tenant-migration)
