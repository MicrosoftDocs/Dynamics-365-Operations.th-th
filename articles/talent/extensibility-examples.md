---
title: เพิ่มความสามารถ Talent โดยใช้ PowerApps และ Microsoft Flow - ตัวอย่างสถานการณ์จำลอง
description: หัวข้อนี้อธิบายถึงตัวอย่างบางอย่างของสถานการณ์สมมุติของการเพิ่มความสามารถของ Microsoft Dynamics 365 for Talent ที่ใช้ Microsoft PowerApps และ Microsoft Flow
author: negudava
manager: Annbe
ms.date: 05/01/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: Dynamics 365 for Talent;PowerApps;Flow;Common Data Service
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
ms.openlocfilehash: a9ebfd1f2621b8ad65d7623c37b6851cc0b5cb54
ms.sourcegitcommit: ffc37f7c2a63bada3055f37856a30424040bc9a3
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 05/16/2019
ms.locfileid: "1577806"
---
# <a name="extend-talent-by-using-powerapps-and-microsoft-flow---example-scenarios"></a><span data-ttu-id="6b89f-103">เพิ่มความสามารถ Talent โดยใช้ PowerApps และ Microsoft Flow - ตัวอย่างสถานการณ์จำลอง</span><span class="sxs-lookup"><span data-stu-id="6b89f-103">Extend Talent by using PowerApps and Microsoft Flow - Example scenarios</span></span>

<span data-ttu-id="6b89f-104">หัวข้อนี้อธิบายถึงตัวอย่างบางอย่างของสถานการณ์สมมุติของการเพิ่มความสามารถของ Microsoft Dynamics 365 for Talent ที่ใช้ Microsoft PowerApps และ Microsoft Flow</span><span class="sxs-lookup"><span data-stu-id="6b89f-104">This topic describes some examples of extensibility scenarios for Microsoft Dynamics 365 for Talent that use Microsoft PowerApps and Microsoft Flow.</span></span> <span data-ttu-id="6b89f-105">คุณสามารถนำเข้าโซลูชันแพคเกจที่เชื่อมโยงกับแต่ละตัวอย่างไปยังสภาพแวดล้อม PowerApps ของคุณ</span><span class="sxs-lookup"><span data-stu-id="6b89f-105">You can import the solution package that is associated with each example into your PowerApps environment.</span></span> <span data-ttu-id="6b89f-106">จากนั้นคุณสามารถใช้แพคเกจเป็นคำแนะนำหรือเป็นจุดเริ่มต้นเพื่อนำสถานการณ์ที่สามารถใช้ได้กับองค์กรของคุณไปใช้</span><span class="sxs-lookup"><span data-stu-id="6b89f-106">You can then use the packages either as guidance or as starting points to implement scenarios that are applicable to your organization.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="6b89f-107">ถ้าคุณต้องการใช้เท็มเพลตและแอพลิเคชันที่อธิบายไว้ในหัวข้อนี้ "ตามที่เป็น" ให้แน่ใจว่าได้ทดสอบแล้วเพื่อให้แน่ใจว่าจะครอบคลุมสถานการณ์จำลองทั้งหมดที่เกี่ยวข้องกับการนำไปใช้ของคุณโดยเฉพาะ</span><span class="sxs-lookup"><span data-stu-id="6b89f-107">If you want to use the templates and app that are described in this topic "as is," be sure to test them to make sure that they cover all the scenarios that are specific to your implementation.</span></span>


## <a name="prerequisites"></a><span data-ttu-id="6b89f-108">ข้อกำหนดเบื้องต้น</span><span class="sxs-lookup"><span data-stu-id="6b89f-108">Prerequisites</span></span>

- <span data-ttu-id="6b89f-109">เมื่อต้องการนำเข้าแพคเกจ ผู้ใช้ต้องมีสิทธิ์ **ผู้สร้างสภาพแวดล้อม**</span><span class="sxs-lookup"><span data-stu-id="6b89f-109">To import packages, users must have the **Environment Maker** permission.</span></span>
- <span data-ttu-id="6b89f-110">เมื่อต้องการส่งออกหรือนำเข้าแอป ผู้ใช้ต้องมีสิทธิ์ทดลองใช้ PowerApps Plan 2 หรือ PowerApps Plan 2</span><span class="sxs-lookup"><span data-stu-id="6b89f-110">To export or import apps, users must have a PowerApps Plan 2 license or a PowerApps Plan 2 trial license.</span></span>

## <a name="flow--form-connect"></a><span data-ttu-id="6b89f-111">การเชื่อมต่อขั้นตอน - แบบฟอร์ม</span><span class="sxs-lookup"><span data-stu-id="6b89f-111">Flow – Form Connect</span></span>

<span data-ttu-id="6b89f-112">เท็มเพลต **การเชื่อมต่อขั้นตอน – แบบฟอร์ม** สามารถนำมาใช้เพื่ออ่านข้อมูลจาก Microsoft Forms และจัดเก็บไว้ในเอนทิตี้ Common Data Service ได้</span><span class="sxs-lookup"><span data-stu-id="6b89f-112">The **Flow – Form Connect** template can be used to read data from Microsoft Forms and store it in a Common Data Service entity.</span></span>

<span data-ttu-id="6b89f-113">เท็มเพลตนี้สามารถขยายได้เพื่อให้สามารถใช้สำหรับสถานการณ์จำลองอื่น ๆ</span><span class="sxs-lookup"><span data-stu-id="6b89f-113">This template can be extended so that it can be used for other scenarios.</span></span> <span data-ttu-id="6b89f-114">ยกตัวอย่างเช่น</span><span class="sxs-lookup"><span data-stu-id="6b89f-114">Here are some examples:</span></span>

- <span data-ttu-id="6b89f-115">รวบรวมการประเมินผู้สมัคร</span><span class="sxs-lookup"><span data-stu-id="6b89f-115">Capture candidate assessments.</span></span>
- <span data-ttu-id="6b89f-116">รวบรวมผลลัพธ์จากแบบสอบถามของหลักสูตร</span><span class="sxs-lookup"><span data-stu-id="6b89f-116">Capture results from course questionnaires.</span></span>
- <span data-ttu-id="6b89f-117">คอมไพล์ไลบรารีของคำถามสัมภาษณ์สำหรับผู้ดูแลฝ่ายทรัพยากรบุคคล (HR)</span><span class="sxs-lookup"><span data-stu-id="6b89f-117">Compile a library of interview questions for Human resources (HR) administrators.</span></span>
- <span data-ttu-id="6b89f-118">เก็บรวบรวมการประเมินของผู้สมัครของกระบวนการสัมภาษณ์</span><span class="sxs-lookup"><span data-stu-id="6b89f-118">Capture a candidate's evaluation of the interview process</span></span>

<span data-ttu-id="6b89f-119">ใน Microsoft Dynamics 365: Attract แบบฟอร์มสามารถปรากฏอยู่ในพอร์ทัลของผู้สมัคร และผู้สมัครสามารถกรอกข้อมูลโดยใส่รายละเอียดได้</span><span class="sxs-lookup"><span data-stu-id="6b89f-119">In Microsoft Dynamics 365: Attract, forms can appear in Candidate portal, and candidates can fill in details.</span></span> <span data-ttu-id="6b89f-120">นอกจากนี้คุณยังสามารถฝังแบบฟอร์มเป็นกิจกรรมในเท็มเพลตงานได้อีกด้วย</span><span class="sxs-lookup"><span data-stu-id="6b89f-120">Forms can also be embedded as activities in a job template.</span></span>

<span data-ttu-id="6b89f-121">เมื่อผู้สมัครส่งแบบฟอร์ม Microsoft Flow จะเก็บรวบรวมการส่งแบบฟอร์ม อ่านข้อมูล และเก็บไว้ในเอนทิตี้ Common Data Service</span><span class="sxs-lookup"><span data-stu-id="6b89f-121">When a candidate submits a form, Microsoft Flow captures the form submission, reads the data, and stores it in the Common Data Service entity.</span></span>

<span data-ttu-id="6b89f-122">เมื่อต้องการดาวน์โหลดเท็มเพลต **การเชื่อมต่อขั้นตอน – แบบฟอร์ม** และกำหนดโครงสร้างของเอนทิตีด้วยตนเอง ไปที่ [การเชื่อมต่อขั้นตอน – แบบฟอร์ม](https://go.microsoft.com/fwlink/?linkid=2081988) บนศูนย์ดาวน์โหลด Microsoft</span><span class="sxs-lookup"><span data-stu-id="6b89f-122">To download the **Flow – Form Connect** template and Custom Entity Structure, go to [Flow – Form Connect](https://go.microsoft.com/fwlink/?linkid=2081988) on the Microsoft Download Center.</span></span>

## <a name="initiate-and-extract-parameters-passed-to-powerapps"></a><span data-ttu-id="6b89f-123">เริ่มต้นและแยกพารามิเตอร์ที่ส่งผ่านไปยัง Powerapps</span><span class="sxs-lookup"><span data-stu-id="6b89f-123">Initiate and Extract Parameters Passed to Powerapps</span></span>

<span data-ttu-id="6b89f-124">คุณสามารถใช้เท็มเพลต **เริ่มต้นและแยกพารามิเตอร์ที่ส่งผ่านไปยัง Powerapps** โดยเป็นจุดเริ่มต้นสำหรับสถานการณ์จำลอง PowerApps ที่เกี่ยวข้องกับ Attract โดยเฉพาะได้</span><span class="sxs-lookup"><span data-stu-id="6b89f-124">The **Initiate and Extract Parameters Passed to Powerapps** template can be used as a starting point for any PowerApps scenario that is specific to Attract.</span></span> <span data-ttu-id="6b89f-125">ซึ่งประกอบด้วยพารามิเตอร์เริ่มต้นทั้งหมดที่ถูกส่งผ่านโดย Attract เช่น **ใบสมัครงาน**, **รหัสผู้สมัคร** และ **JobID**</span><span class="sxs-lookup"><span data-stu-id="6b89f-125">It includes all the default parameters that are passed by Attract, such as **Job Application**, **Candidate ID**, and **JobID**.</span></span>

<span data-ttu-id="6b89f-126">คุณสามารถใช้เท็มเพลตนี้เพื่อดึงข้อมูลแบบฟอร์มการประเมินผู้สมัครเพื่อให้ผู้จัดการที่ว่าจ้างสามารถดูการประเมินที่ผู้สมัครกรอกไว้ได้</span><span class="sxs-lookup"><span data-stu-id="6b89f-126">This template can be used to retrieve a candidate assessment form, so that a hiring manager can view the assessment that a candidate filled in.</span></span>

<span data-ttu-id="6b89f-127">คุณสามารถฝังแอปที่สร้างขึ้นโดยใช้ PowerApps ไว้ในเท็มเพลตงานใน Attract</span><span class="sxs-lookup"><span data-stu-id="6b89f-127">Apps that are created by using PowerApps can be embedded into the job template in Attract.</span></span>

<span data-ttu-id="6b89f-128">เมื่อต้องการดาวน์โหลดเท็มเพลต **เริ่มต้นและแยกพารามิเตอร์ที่ส่งผ่านไปยัง Powerapps** และกำหนดโครงสร้างของเอนทิตีด้วยตนเอง ไปที่ [เริ่มต้นและแยกพารามิเตอร์ที่ส่งผ่านไปยัง Powerapps](https://go.microsoft.com/fwlink/?linkid=2081991) บนศูนย์ดาวน์โหลด Microsoft</span><span class="sxs-lookup"><span data-stu-id="6b89f-128">To download the **Initiate and Extract Parameters Passed to Powerapps** template and Custom Entity Structure, go to [Initiate and Extract Parameters Passed to Powerapps](https://go.microsoft.com/fwlink/?linkid=2081991) on the Microsoft Download Center.</span></span>

## <a name="integration-with-office-365"></a><span data-ttu-id="6b89f-129">การรวมกับ Office 365</span><span class="sxs-lookup"><span data-stu-id="6b89f-129">Integration with Office 365</span></span>

<span data-ttu-id="6b89f-130">คุณสามารถใช้แอป **การรวมกับ Office 365** ในการดึงข้อมูลของทีมงานสำหรับผู้ใช้ที่ลงชื่อเข้าใช้จาก Microsoft Office 365 ได้</span><span class="sxs-lookup"><span data-stu-id="6b89f-130">The **Integration with Office 365** app can be used to extract team information for signed-in users from Microsoft Office 365.</span></span> <span data-ttu-id="6b89f-131">ซึ่งจะอ้างอิงถึงผู้ปฏิบัติงานใน Talent เพื่อแยกรายละเอียดการตอกบัตรเข้าและตอกบัตรออกและการบันทึกข้อยกเว้น</span><span class="sxs-lookup"><span data-stu-id="6b89f-131">It references workers in Talent to extract clock-in and clock-out details and exception recordings.</span></span> <span data-ttu-id="6b89f-132">รายละเอียดการตอกบัตรเข้าและตอกบัตรออกถูกจัดเก็บไว้ในเอนทิตี้ Common Data Service แบบกำหนดเอง</span><span class="sxs-lookup"><span data-stu-id="6b89f-132">Clock-in and Clock-out details are stored in custom Common Data Service entities.</span></span> <span data-ttu-id="6b89f-133">ข้อสมมติฐานคือว่ารายละเอียดเหล่านี้จะถูกกรอกข้อมูลจากระบบภายนอกผ่านการรวม</span><span class="sxs-lookup"><span data-stu-id="6b89f-133">The assumption is that these details are filled in from third-party systems via integration.</span></span>

<span data-ttu-id="6b89f-134">แอปนี้สามารถขยายได้เพื่อให้สามารถใช้สำหรับสถานการณ์จำลองอื่น ๆ</span><span class="sxs-lookup"><span data-stu-id="6b89f-134">This app can be extended so that it can be used for other scenarios.</span></span> <span data-ttu-id="6b89f-135">ตัวอย่างเช่น สามารถใช้เพื่อแสดงข้อมูลวันหยุดพักผ่อนของทีมงาน ปฏิทินเหตุการณ์ และเหตุการณ์เฉพาะทีมงานใด ๆ</span><span class="sxs-lookup"><span data-stu-id="6b89f-135">For example, it can be used to show team vacation information, calendar events, and any team-specific events.</span></span>

<span data-ttu-id="6b89f-136">เมื่อต้องการดาวน์โหลดแอป **การรวมกับ Office 365** และโครงสร้างของเอนทิตี้แบบกำหนดเอง ไปที่ [การรวมกับ Office 365](https://go.microsoft.com/fwlink/?linkid=2081787) บนศูนย์ดาวน์โหลด Microsoft</span><span class="sxs-lookup"><span data-stu-id="6b89f-136">To download the **Integration with Office 365** app and Custome Entity Structure, go to [Integration with Office 365](https://go.microsoft.com/fwlink/?linkid=2081787) on the Microsoft Download Center.</span></span>

## <a name="flow--email-notification"></a><span data-ttu-id="6b89f-137">ขั้นตอน - การแจ้งเตือนทางอีเมล</span><span class="sxs-lookup"><span data-stu-id="6b89f-137">Flow – Email Notification</span></span>

<span data-ttu-id="6b89f-138">คุณสามารถใช้เท็มเพลต **ขั้นตอน - การแจ้งเตือนทางอีเมล** สำหรับสถานการณ์จำลองการแจ้งเตือนทางอีเมล</span><span class="sxs-lookup"><span data-stu-id="6b89f-138">The **Flow – Email Notification** template can be used for email notification scenarios.</span></span> <span data-ttu-id="6b89f-139">ซึ่งสามารถใช้เพื่อทริกเกอร์อีเมลแจ้งเตือนให้กับผู้สมัครที่ทีมการว่าจ้างปฏิเสธในระหว่างขั้นใดๆ ของกระบวนการสรรหาบุคลากร</span><span class="sxs-lookup"><span data-stu-id="6b89f-139">It can be used to trigger notification emails to candidates that the hiring team rejects during any stage of the recruiting process.</span></span>

<span data-ttu-id="6b89f-140">คุณสามารถขยายเท็มเพลตนี้เพื่อติดตามการเปลี่ยนแปลงขั้นของผู้สมัครตลอดทั้งกระบวนการสรรหาบุคลากร และเพื่อส่งการแจ้งเตือนไปยังทีมงานการจ้างงานและผู้สมัคร</span><span class="sxs-lookup"><span data-stu-id="6b89f-140">This template can be extended to track changes to the candidate stage throughout the recruiting process, and to send notifications to the hiring team and candidate.</span></span>

<span data-ttu-id="6b89f-141">โดยทั่วไป สำหรับเอนทิตีที่จัดเก็บใน Common Data Service คุณสามารถตั้งค่าขั้นตอนเพื่อส่งการแจ้งเตือนสำหรับเหตุการณ์ที่เกิดขึ้นใน Core HR, Attract หรือ Dynamics 365 Talent: Onboard</span><span class="sxs-lookup"><span data-stu-id="6b89f-141">In general, for entities that are stored in Common Data Service, flows can be set up to send notifications for events that occur in Core HR, Attract, or Dynamics 365 Talent: Onboard.</span></span>

<span data-ttu-id="6b89f-142">เมื่อต้องการดาวน์โหลดเท็มเพลต **ขั้นตอน - การแจ้งเตือนทางอีเมล** ไปที่ [ขั้นตอน - การแจ้งเตือนทางอีเมล](https://go.microsoft.com/fwlink/?linkid=2082103) บนศูนย์ดาวน์โหลด Microsoft</span><span class="sxs-lookup"><span data-stu-id="6b89f-142">To download the **Flow – Email Notification** template, go to [Flow – Email Notification](https://go.microsoft.com/fwlink/?linkid=2082103) on the Microsoft Download Center.</span></span>

## <a name="flow--sql-connect-and-execute"></a><span data-ttu-id="6b89f-143">ขั้นตอน – SQL เชื่อมต่อและดำเนินการ</span><span class="sxs-lookup"><span data-stu-id="6b89f-143">Flow – SQL Connect and execute</span></span>

<span data-ttu-id="6b89f-144">เท็มเพลต **ขั้นตอน – SQL เชื่อมต่อและดำเนินการ** เชื่อมต่อกับ Microsoft SQL Server และเปิดใช้งานให้ การสอบถาม SQL รัน</span><span class="sxs-lookup"><span data-stu-id="6b89f-144">The **Flow – SQL Connect and execute** template connects to Microsoft SQL Server and enables SQL queries to be run.</span></span>

<span data-ttu-id="6b89f-145">ถึงแม้ว่าเท็มเพลตนี้จะมีวัตถุประสงค์เพื่ออ่านและอัพเดตตาราง SQL แต่ก็ยังสามารถขยายเพื่อให้สามารถใช้สำหรับสถานการณ์จำลองอื่น ๆ ได้</span><span class="sxs-lookup"><span data-stu-id="6b89f-145">Although this template is designed to read and update SQL tables, it can be extended so that it can be used for other scenarios.</span></span> <span data-ttu-id="6b89f-146">ตัวอย่างเช่น สามารถใช้เพื่อกรอกข้อมูลในตารางการจัดเตรียมใน Common Data Service ด้วยเรกคอร์ดจาก SQL Server และเพื่อซิงโครไนส์ตารางการจัดเตรียมเป็นระยะ ๆ โดยใช้พุชส่วนเพิ่มจาก SQL Server</span><span class="sxs-lookup"><span data-stu-id="6b89f-146">For example, it can be used to fill a staging table in Common Data Service with records from SQL Server, and to periodically synchronize the staging table by using an incremental push from SQL Server.</span></span>

<span data-ttu-id="6b89f-147">เมื่อต้องการดาวน์โหลดเท็มเพลต **การเชื่อมต่อขั้นตอน – SQL** และกำหนดโครงสร้างของเอนทิตีด้วยตนเอง ไปที่ [การเชื่อมต่อขั้นตอน – SQL](https://go.microsoft.com/fwlink/?linkid=2081789) บนศูนย์ดาวน์โหลด Microsoft</span><span class="sxs-lookup"><span data-stu-id="6b89f-147">To download the **Flow – SQL Connect and execute** template, go to [Flow – SQL Connect and execute](https://go.microsoft.com/fwlink/?linkid=2081789) on the Microsoft Download Center.</span></span>

## <a name="flow--sharepoint-integration"></a><span data-ttu-id="6b89f-148">การรวมขั้นตอน – SharePoint</span><span class="sxs-lookup"><span data-stu-id="6b89f-148">Flow – SharePoint Integration</span></span>

<span data-ttu-id="6b89f-149">คุณสามารถใช้เท็มเพลต **การรวมขั้นตอน – SharePoint** เพื่ออ่านข้อมูลจากรายการ Microsoft SharePoint เปรียบเทียบรายการที่มีค่าฟิลด์สำหรับเอนทิตี้ Common Data Service ใด ๆ และส่งผลลัพธ์ของการเปรียบเทียบเป็นอีเมลการแจ้งเตือนได้</span><span class="sxs-lookup"><span data-stu-id="6b89f-149">The **Flow – SharePoint Integration** template can be used to read data from a Microsoft SharePoint list, compare the list with field values for any Common Data Service entity, and send the results of the comparison as a notification email.</span></span> 

<span data-ttu-id="6b89f-150">องค์กรอาจมีชุดของทักษะที่ต้องใช้โดยทันที</span><span class="sxs-lookup"><span data-stu-id="6b89f-150">An organization might have a set of skills that it urgently requires.</span></span> <span data-ttu-id="6b89f-151">คุณสามารถจัดเก็บทักษะเหล่านี้ใน SharePoint เป็นรายการ SharePoint</span><span class="sxs-lookup"><span data-stu-id="6b89f-151">These skills can be stored in SharePoint as a SharePoint list.</span></span> <span data-ttu-id="6b89f-152">เมื่อผู้สมัครสมัครสำหรับงานใด ๆ ที่มีแสดงรายการชุดของทักษะที่จำเป็น ถ้ามีการจับคู่ที่มีนัยสำคัญระหว่างทักษะของผู้สมัครและทักษะที่เก็บไว้ใน SharePoint จะมีการส่งอีเมลการแจ้งเตือน</span><span class="sxs-lookup"><span data-stu-id="6b89f-152">When a candidate applies for any job that a set of required skills is listed for, if there is a significant match between the candidate's skill and the skills that are stored in SharePoint, a notification email is sent.</span></span> <span data-ttu-id="6b89f-153">ด้วยวิธีนี้ ตำแหน่งที่จำเป็นต้องจัดหาโดยทันทีจะได้รับการจัดหารวดเร็วขึ้น เนื่องจากการแจ้งเตือนจะช่วยให้ผู้สรรหาสามารถติดต่อและว่าจ้างผู้สมัครได้ทั่วทั้งองค์กร</span><span class="sxs-lookup"><span data-stu-id="6b89f-153">In this way, positions that are urgently required are filled faster, because the notifications help recruiters reach out and cross-hire candidates throughout the organization.</span></span>

<span data-ttu-id="6b89f-154">คุณสามารถขยายเท็มเพลตนี้เพื่อให้สามารถใช้สำหรับสถานการณ์จำลองใด ๆ ที่เกี่ยวข้องกับการรวม SharePoint ได้</span><span class="sxs-lookup"><span data-stu-id="6b89f-154">This template can be extended so that it can be used for any scenario that involves SharePoint integration.</span></span>

<span data-ttu-id="6b89f-155">เมื่อต้องการดาวน์โหลดเท็มเพลต **การรวมขั้นตอน - SharePoint** ไปที่ [การรวมขั้นตอน - SharePoint](https://go.microsoft.com/fwlink/?linkid=2082109) บนศูนย์ดาวน์โหลด Microsoft</span><span class="sxs-lookup"><span data-stu-id="6b89f-155">To download the **Flow – SharePoint Integration** template, go to [Flow – SharePoint Integration](https://go.microsoft.com/fwlink/?linkid=2082109) on the Microsoft Download Center.</span></span>

## <a name="admin-console-to-manage-talent-pools"></a><span data-ttu-id="6b89f-156">คอนโซลผู้ดูแลระบบเพื่อจัดการกลุ่ม talent</span><span class="sxs-lookup"><span data-stu-id="6b89f-156">Admin console to manage talent pools</span></span>

<span data-ttu-id="6b89f-157">เมื่อคุณเปิดใช้งานการรวมกับ LinkedIn Attract จะสร้างกลุ่ม talent ของ LinkedIn โดยอัตโนมัติ</span><span class="sxs-lookup"><span data-stu-id="6b89f-157">When you enable integration with LinkedIn, Attract automatically createas a LinkedIn talent pool.</span></span> <span data-ttu-id="6b89f-158">เมื่อผู้สรรหาแลกเปลี่ยน InMail กับการสรรหาผ่านทาง LinkedIn Attract จะสร้างโพรไฟล์สำหรับการสรรหา และการสรรหาจะกลายเป็นสมาชิกของกลุ่ม talent ของ LinkedIn</span><span class="sxs-lookup"><span data-stu-id="6b89f-158">When a recruiter exchanges InMail with a recruit through LinkedIn, Attract creates a profile for the recruit, and the recruit becomes a member of the LinkedIn talent pool.</span></span> <span data-ttu-id="6b89f-159">แอป PowerApps นี้มีประโยชน์สำหรับการจัดระเบียบผู้สมัครใหม่ในกลุ่ม talent ตามทักษะ</span><span class="sxs-lookup"><span data-stu-id="6b89f-159">This PowerApps app is useful for reorganizing candidates in talent pools based on skill.</span></span>

<span data-ttu-id="6b89f-160">รันแอพลิเคชัน PowerApps นี้เป็นคอนโซลผู้ดูแลระบบเพื่อดำเนินการงานต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="6b89f-160">Run this PowerApps app as an admin console to perform the following tasks:</span></span>

- <span data-ttu-id="6b89f-161">แสดงรายการผู้สมัครในกลุ่ม talent</span><span class="sxs-lookup"><span data-stu-id="6b89f-161">List candidates in a talent pool</span></span>
- <span data-ttu-id="6b89f-162">เพิ่มและลบผู้สมัครจากกลุ่ม talent</span><span class="sxs-lookup"><span data-stu-id="6b89f-162">Add and remove candidates from a talent pool</span></span>
- <span data-ttu-id="6b89f-163">ย้ายผู้สมัครจากกลุ่ม talent หนึ่งไปยังอีกกลุ่มหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="6b89f-163">Move candidates from one talent pool to another</span></span>
- <span data-ttu-id="6b89f-164">ตรวจสอบว่าผู้สมัครเป็นส่วนหนึ่งของกลุ่ม talent อยู่แล้วหรือไม่ ก่อนที่จะเคลื่อนย้าย</span><span class="sxs-lookup"><span data-stu-id="6b89f-164">Determine whether candidates are already part of a talent pool before moving them</span></span>
- <span data-ttu-id="6b89f-165">ตรวจสอบทักษะของผู้สมัครก่อนที่จะเคลื่อนย้ายไปที่กลุ่ม talent อื่นๆ</span><span class="sxs-lookup"><span data-stu-id="6b89f-165">Check the skills of candidates before moving them to other talent pools</span></span>

<span data-ttu-id="6b89f-166">แอป PowerApps นี้ใช้ความสัมพันธ์แบบกลุ่มต่อกลุ่ม ดังนั้นคุณจึงสามารถใช้เป็นเท็มเพลตสำหรับสถานการณ์อื่นๆ ที่คุณจำเป็นต้องแยกเรกคอร์ดที่มีความสัมพันธ์แบบกลุ่มต่อกลุ่ม</span><span class="sxs-lookup"><span data-stu-id="6b89f-166">This PowerApps app uses many-to-many relationships, so you can use it as a template for other scenarios where you need to extract records that have many-to-many relationships.</span></span>

<span data-ttu-id="6b89f-167">เมื่อต้องการดาวน์โหลดเท็มเพลต **คอนโซลผู้ดูแลระบบเพื่อจัดการกลุ่ม talent** ไปยัง [คอนโซลผู้ดูแลระบบเพื่อจัดการกลุ่ม talent](https://www.microsoft.com/downloads/details.aspx?FamilyID=780a5eee-0e2a-4159-9a83-009f9ccdc469) ใน Microsoft Download Center</span><span class="sxs-lookup"><span data-stu-id="6b89f-167">To download the **Admin console to manage talent pools** template,  go to [Admin console to manage talent pools](https://www.microsoft.com/downloads/details.aspx?FamilyID=780a5eee-0e2a-4159-9a83-009f9ccdc469) on the Microsoft Download Center.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="6b89f-168">แหล่งข้อมูลเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="6b89f-168">Additional resources</span></span>

[<span data-ttu-id="6b89f-169">Microsoft Power Platform</span><span class="sxs-lookup"><span data-stu-id="6b89f-169">The Microsoft Power Platform</span></span>](https://docs.microsoft.com/power-platform/admin/admin-documentation)

[<span data-ttu-id="6b89f-170">ย้ายแอประหว่างผู้เช่าและสภาพแวดล้อม</span><span class="sxs-lookup"><span data-stu-id="6b89f-170">Migrate app between tenants and environments</span></span>](https://docs.microsoft.com/en-us/power-platform/admin/environment-and-tenant-migration)
