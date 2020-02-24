---
title: ขยาย Talent ด้วย Power Apps และ Power Automate
description: บทความนี้อธิบายถึงตัวอย่างบางรายการของสถานการณ์การเพิ่มความสามารถของ Microsoft Dynamics 365 Talent - Attract ที่ใช้ Microsoft Power Apps และ Microsoft Power Automate
author: negudava
manager: Annbe
ms.date: 02/06/2020
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
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Talent October 2018 update
ms.openlocfilehash: 1051fa4db16bb94cc9d60a91fc3637d7e5305cc2
ms.sourcegitcommit: 13c4a6f98ccce243d6befde90992aefcf562bdab
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 02/06/2020
ms.locfileid: "3029922"
---
# <a name="extend-talent-with-power-apps-and-power-automate"></a><span data-ttu-id="5fb42-103">ขยาย Talent ด้วย Power Apps และ Power Automate</span><span class="sxs-lookup"><span data-stu-id="5fb42-103">Extend Talent with Power Apps and Power Automate</span></span>

<span data-ttu-id="5fb42-104">บทความนี้อธิบายถึงตัวอย่างบางรายการของสถานการณ์การเพิ่มความสามารถของ Microsoft Dynamics 365 Talent: Attract ที่ใช้ Microsoft Power Apps และ Microsoft Power Automate</span><span class="sxs-lookup"><span data-stu-id="5fb42-104">This article describes some examples of extensibility scenarios for Microsoft Dynamics 365 Talent: Attract that use Microsoft Power Apps and Microsoft Power Automate.</span></span> <span data-ttu-id="5fb42-105">คุณสามารถนำเข้าโซลูชันแพคเกจที่เชื่อมโยงกับแต่ละตัวอย่างไปยังสภาพแวดล้อม Power Apps ของคุณ</span><span class="sxs-lookup"><span data-stu-id="5fb42-105">You can import the solution package that is associated with each example into your Power Apps environment.</span></span> <span data-ttu-id="5fb42-106">จากนั้นคุณสามารถใช้แพคเกจเป็นคำแนะนำหรือเป็นจุดเริ่มต้นเพื่อนำสถานการณ์ที่สามารถใช้ได้กับองค์กรของคุณไปใช้</span><span class="sxs-lookup"><span data-stu-id="5fb42-106">You can then use the packages either as guidance or as starting points to implement scenarios that are applicable to your organization.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="5fb42-107">ถ้าคุณต้องการใช้เท็มเพลตและแอปที่อธิบายไว้ในบทความนี้ "ตามที่เป็น" ให้แน่ใจว่าได้ทดสอบแล้วเพื่อให้แน่ใจว่าจะครอบคลุมสถานการณ์จำลองทั้งหมดที่เกี่ยวข้องกับการนำไปใช้ของคุณโดยเฉพาะ</span><span class="sxs-lookup"><span data-stu-id="5fb42-107">If you want to use the templates and app that are described in this article "as is," be sure to test them to make sure that they cover all the scenarios that are specific to your implementation.</span></span>


## <a name="prerequisites"></a><span data-ttu-id="5fb42-108">ข้อกำหนดเบื้องต้น</span><span class="sxs-lookup"><span data-stu-id="5fb42-108">Prerequisites</span></span>

- <span data-ttu-id="5fb42-109">เมื่อต้องการนำเข้าแพคเกจ ผู้ใช้ต้องมีสิทธิ์ **ผู้สร้างสภาพแวดล้อม**</span><span class="sxs-lookup"><span data-stu-id="5fb42-109">To import packages, users must have the **Environment Maker** permission.</span></span>
- <span data-ttu-id="5fb42-110">เมื่อต้องการส่งออกหรือนำเข้าแอป ผู้ใช้ต้องมีใบอนุญาตใช้ Power Apps Plan 2 หรือใบอนุญาตในการทดลองใช้ Power Apps Plan 2</span><span class="sxs-lookup"><span data-stu-id="5fb42-110">To export or import apps, users must have a Power Apps Plan 2 license or a Power Apps Plan 2 trial license.</span></span>

## <a name="power-automate--form-connect"></a><span data-ttu-id="5fb42-111">Power Automate – การเชื่อมต่อฟอร์ม</span><span class="sxs-lookup"><span data-stu-id="5fb42-111">Power Automate – Form Connect</span></span>

<span data-ttu-id="5fb42-112">แม่แบบ **Power Automate – การเชื่อมต่อฟอร์ม** สามารถนำมาใช้เพื่ออ่านข้อมูลจาก Microsoft Forms และจัดเก็บไว้ในเอนทิตี Common Data Service ได้</span><span class="sxs-lookup"><span data-stu-id="5fb42-112">The **Power Automate – Form Connect** template can be used to read data from Microsoft Forms and store it in a Common Data Service entity.</span></span>

<span data-ttu-id="5fb42-113">เท็มเพลตนี้สามารถขยายได้เพื่อให้สามารถใช้สำหรับสถานการณ์จำลองอื่น ๆ</span><span class="sxs-lookup"><span data-stu-id="5fb42-113">This template can be extended so that it can be used for other scenarios.</span></span> <span data-ttu-id="5fb42-114">ยกตัวอย่างเช่น</span><span class="sxs-lookup"><span data-stu-id="5fb42-114">Here are some examples:</span></span>

- <span data-ttu-id="5fb42-115">รวบรวมการประเมินผู้สมัคร</span><span class="sxs-lookup"><span data-stu-id="5fb42-115">Capture candidate assessments.</span></span>
- <span data-ttu-id="5fb42-116">รวบรวมผลลัพธ์จากแบบสอบถามของหลักสูตร</span><span class="sxs-lookup"><span data-stu-id="5fb42-116">Capture results from course questionnaires.</span></span>
- <span data-ttu-id="5fb42-117">คอมไพล์ไลบรารีของคำถามสัมภาษณ์สำหรับผู้ดูแลฝ่ายทรัพยากรบุคคล (HR)</span><span class="sxs-lookup"><span data-stu-id="5fb42-117">Compile a library of interview questions for Human resources (HR) administrators.</span></span>
- <span data-ttu-id="5fb42-118">เก็บรวบรวมการประเมินของผู้สมัครของกระบวนการสัมภาษณ์</span><span class="sxs-lookup"><span data-stu-id="5fb42-118">Capture a candidate's evaluation of the interview process</span></span>

<span data-ttu-id="5fb42-119">ใน Microsoft Dynamics 365: Attract คุณสามารถใช้ฟอร์มในพอร์ทัลของผู้สมัคร ที่ซึ่งผู้สมัครสามารถกรอกข้อมูลโดยใส่รายละเอียดได้</span><span class="sxs-lookup"><span data-stu-id="5fb42-119">In Microsoft Dynamics 365: Attract, you can use forms in the candidate portal, where candidates fill in details.</span></span> <span data-ttu-id="5fb42-120">นอกจากนี้ คุณยังสามารถฝังฟอร์มเป็นกิจกรรมในเท็มเพลตงานได้อีกด้วย</span><span class="sxs-lookup"><span data-stu-id="5fb42-120">You can also embed forms as activities in a job template.</span></span>

<span data-ttu-id="5fb42-121">เมื่อผู้สมัครส่งฟอร์ม Microsoft Power Automate จะเก็บรวบรวมการส่งฟอร์ม อ่านข้อมูล และเก็บไว้ในเอนทิตี Common Data Service</span><span class="sxs-lookup"><span data-stu-id="5fb42-121">When a candidate submits a form, Microsoft Power Automate captures the form submission, reads the data, and stores it in the Common Data Service entity.</span></span>

<span data-ttu-id="5fb42-122">เมื่อต้องการดาวน์โหลดแม่แบบ **Power Automate – การเชื่อมต่อฟอร์ม** และโครงสร้างการกำหนดเอนทิตีด้วยตนเอง ไปที่ [Power Automate – การเชื่อมต่อฟอร์ม](https://go.microsoft.com/fwlink/?linkid=2081988) บนศูนย์ดาวน์โหลด Microsoft</span><span class="sxs-lookup"><span data-stu-id="5fb42-122">To download the **Power Automate – Form Connect** template and Custom Entity Structure, go to [Power Automate – Form Connect](https://go.microsoft.com/fwlink/?linkid=2081988) on the Microsoft Download Center.</span></span>

## <a name="power-automate--sharepoint-integration"></a><span data-ttu-id="5fb42-123">Power Automate – การรวม SharePoint</span><span class="sxs-lookup"><span data-stu-id="5fb42-123">Power Automate – SharePoint Integration</span></span>

<span data-ttu-id="5fb42-124">คุณสามารถใช้แม่แบบ **Power Automate – การรวม SharePoint** เพื่ออ่านข้อมูลจากรายการ Microsoft SharePoint เปรียบเทียบรายการที่มีค่าฟิลด์สำหรับเอนทิตี Common Data Service ใด ๆ และส่งผลลัพธ์ของการเปรียบเทียบเป็นอีเมลการแจ้งเตือนได้</span><span class="sxs-lookup"><span data-stu-id="5fb42-124">The **Power Automate – SharePoint Integration** template can be used to read data from a Microsoft SharePoint list, compare the list with field values for any Common Data Service entity, and send the results of the comparison as a notification email.</span></span> 

<span data-ttu-id="5fb42-125">องค์กรอาจมีชุดของทักษะที่ต้องใช้โดยทันที</span><span class="sxs-lookup"><span data-stu-id="5fb42-125">An organization might have a set of skills that it urgently requires.</span></span> <span data-ttu-id="5fb42-126">คุณสามารถจัดเก็บทักษะเหล่านี้ใน SharePoint เป็นรายการ SharePoint</span><span class="sxs-lookup"><span data-stu-id="5fb42-126">These skills can be stored in SharePoint as a SharePoint list.</span></span> <span data-ttu-id="5fb42-127">เมื่อผู้สมัครสมัครสำหรับงานใด ๆ ที่มีแสดงรายการชุดของทักษะที่จำเป็น ถ้ามีการจับคู่ที่มีนัยสำคัญระหว่างทักษะของผู้สมัครและทักษะที่เก็บไว้ใน SharePoint จะมีการส่งอีเมลการแจ้งเตือน</span><span class="sxs-lookup"><span data-stu-id="5fb42-127">When a candidate applies for any job that a set of required skills is listed for, if there is a significant match between the candidate's skill and the skills that are stored in SharePoint, a notification email is sent.</span></span> <span data-ttu-id="5fb42-128">นี่จะช่วยในการกรอกข้อมูลตำแหน่งที่จำเป็นต้องจัดหาโดยเร่งด่วน เนื่องจากการแจ้งเตือนจะช่วยให้ผู้สรรหาสามารถว่าจ้างผู้สมัครได้ทั่วทั้งองค์กร</span><span class="sxs-lookup"><span data-stu-id="5fb42-128">This helps fill positions that are urgently required faster, because the notifications help recruiters cross-hire candidates throughout the organization.</span></span>

<span data-ttu-id="5fb42-129">คุณสามารถขยายเท็มเพลตนี้เพื่อให้สามารถใช้สำหรับสถานการณ์จำลองใด ๆ ที่เกี่ยวข้องกับการรวม SharePoint ได้</span><span class="sxs-lookup"><span data-stu-id="5fb42-129">This template can be extended so that it can be used for any scenario that involves SharePoint integration.</span></span>

<span data-ttu-id="5fb42-130">เมื่อต้องการดาวน์โหลดแม่แบบ **Power Automate – การรวม SharePoint** ไปที่ [Power Automate – กาารรวม SharePoint](https://go.microsoft.com/fwlink/?linkid=2082109) บนศูนย์ดาวน์โหลด Microsoft</span><span class="sxs-lookup"><span data-stu-id="5fb42-130">To download the **Power Automate – SharePoint Integration** template, go to [Power Automate – SharePoint Integration](https://go.microsoft.com/fwlink/?linkid=2082109) on the Microsoft Download Center.</span></span>

## <a name="referral-app"></a><span data-ttu-id="5fb42-131">แอปการอ้างอิง</span><span class="sxs-lookup"><span data-stu-id="5fb42-131">Referral App</span></span>

<span data-ttu-id="5fb42-132">คุณสามารถใช้แอปการอ้างอิงเพื่อเพิ่มผู้สมัครในกลุ่มผู้มีความสามารถพิเศษที่ใช้ร่วมกัน</span><span class="sxs-lookup"><span data-stu-id="5fb42-132">You can use the Referral App to add candidates to a shared talent pool.</span></span> <span data-ttu-id="5fb42-133">การอ้างอิงสามารถป้อน **Firstname** **Lastname** **อีเมล** และ **URL ของ LinkedIn** เมื่อส่งผู้สมัคร</span><span class="sxs-lookup"><span data-stu-id="5fb42-133">The referrer can enter **Firstname**, **Lastname**, **Email**, and **LinkedIn URL** when submitting a candidate.</span></span> <span data-ttu-id="5fb42-134">ข้อมูลเมตาของแหล่งที่มาของผู้สมัครจะถูกเติมด้วยข้อมูลของบุคคลอ้างอิง</span><span class="sxs-lookup"><span data-stu-id="5fb42-134">The candidate source metadata is then populated with the referrer’s information.</span></span>

<span data-ttu-id="5fb42-135">คุณสามารถฝังแอปนี้ในระบบบริการตนเองของพนักงานสำหรับการส่งการอ้างอิง หรือคุณสามารถใช้เป็นไฮเปอร์ลิงค์ในพอร์ทัลองค์กรและรันเป็นแอปที่ทำงานแยกต่างหาก</span><span class="sxs-lookup"><span data-stu-id="5fb42-135">You can embed this app in Employee self service for submitting referrals, or you can use it as a hyperlink in the corporate portal and run it as a stand-alone app.</span></span>

<span data-ttu-id="5fb42-136">เมื่อต้องการดาวน์โหลด **แอปการอ้างอิง** ไปที่ [โซลูชันความสามารถในการเพิ่มฟังก์ชัน Dynamics 365 Talent : แอปการอ้างอิง](https://www.microsoft.com/download/details.aspx?id=58497) บนศูนย์การดาวน์โหลดของ Microsoft</span><span class="sxs-lookup"><span data-stu-id="5fb42-136">To download **Referral App**, go to [Dynamics 365 Talent extensibility solution: Referral App](https://www.microsoft.com/download/details.aspx?id=58497) on the Microsoft Download Center.</span></span> <span data-ttu-id="5fb42-137">คุณสามารถนำเข้าแอปนี้และเลือกกำหนดเพื่อเพิ่มฟังก์ชันเพิ่มเติมได้</span><span class="sxs-lookup"><span data-stu-id="5fb42-137">You can import this app and customize it to add additional functionality.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="5fb42-138">แหล่งข้อมูลเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="5fb42-138">Additional resources</span></span>

[<span data-ttu-id="5fb42-139">Microsoft Power Platform</span><span class="sxs-lookup"><span data-stu-id="5fb42-139">The Microsoft Power Platform</span></span>](https://docs.microsoft.com/power-platform/admin/admin-documentation)</br>
[<span data-ttu-id="5fb42-140">ย้ายแอประหว่างผู้เช่าและสภาพแวดล้อม</span><span class="sxs-lookup"><span data-stu-id="5fb42-140">Migrate app between tenants and environments</span></span>](https://docs.microsoft.com/power-platform/admin/environment-and-tenant-migration)
