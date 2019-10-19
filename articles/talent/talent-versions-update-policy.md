---
title: ความต้องการของระบบ Talent และนโยบายการอัพเดต
description: หัวข้อนี้แสดงความต้องการสำหรับ Dynamics 365 Talent นอกจากนี้ยังระบุนโยบายการอัพเดตด้วย
author: andreabichsel
manager: AnnBe
ms.date: 05/02/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: anbichse
ms.search.scope: Core, Operations, Talent
ms.custom: 63213
ms.assetid: 5dbc62fc-0184-4c0e-9856-e735fc68799e
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: July 2017 update
ms.openlocfilehash: b8bf44fc76be968b0b04fd894c39b4c19fd374ce
ms.sourcegitcommit: f87de0f949b5d60993b19e0f61297f02d42b5bef
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 09/24/2019
ms.locfileid: "2024171"
---
# <a name="talent-system-requirements-and-update-policy"></a><span data-ttu-id="fb5f4-104">ความต้องการของระบบ Talent และนโยบายการอัพเดต</span><span class="sxs-lookup"><span data-stu-id="fb5f4-104">Talent system requirements and update policy</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="fb5f4-105">หัวข้อนี้จะอธิบายถึงข้อกำหนดสำหรับ Microsoft Dynamics 365 Talent ซึ่งรวมถึง Attract Onboard และ Core HR</span><span class="sxs-lookup"><span data-stu-id="fb5f4-105">This topic describes requirements for Microsoft Dynamics 365 Talent, including Attract, Onboard, and Core HR.</span></span> <span data-ttu-id="fb5f4-106">นอกจากนี้ ยังกำหนดโครงร่างประเทศและภูมิภาคที่ Talent พร้อมใช้งาน รวมถึงข้อมูลเกี่ยวกับภาษาและการแปลสำหรับข้อมูล Talent</span><span class="sxs-lookup"><span data-stu-id="fb5f4-106">It also outlines the countries and regions where Talent is available, plus information about languages and localization for Talent data.</span></span> <span data-ttu-id="fb5f4-107">นอกจากนี้ หัวข้อนี้จะแสดงนโยบายการอัพเดตสำหรับ Talent</span><span class="sxs-lookup"><span data-stu-id="fb5f4-107">In additions, this topic provides the update policy for Talent.</span></span>

## <a name="supported-web-browsers"></a><span data-ttu-id="fb5f4-108">เว็บเบราเซอร์ที่สนับสนุน</span><span class="sxs-lookup"><span data-stu-id="fb5f4-108">Supported web browsers</span></span>

<span data-ttu-id="fb5f4-109">Microsoft Dynamics 365 Talent สามารถเรียกใช้ในเว็บเบราเซอร์ใดก็ได้ต่อไปนี้ที่ทำงานบนระบบปฏิบัติการที่ระบุ:</span><span class="sxs-lookup"><span data-stu-id="fb5f4-109">Microsoft Dynamics 365 Talent can run in any of the following web browsers that run on the specified operating systems:</span></span> 

*   <span data-ttu-id="fb5f4-110">Microsoft Edge (รุ่นล่าสุดที่พร้อมใช้งานทั่วไป) บน Windows 10</span><span class="sxs-lookup"><span data-stu-id="fb5f4-110">Microsoft Edge (latest publicly available version) on Windows 10</span></span>
*   <span data-ttu-id="fb5f4-111">Internet Explorer 11 บน Windows 10, Windows 8.1 หรือ Windows 7</span><span class="sxs-lookup"><span data-stu-id="fb5f4-111">Internet Explorer 11 on Windows 10, Windows 8.1, or Windows 7</span></span>
*   <span data-ttu-id="fb5f4-112">Google Chrome (รุ่นล่าสุดที่พร้อมใช้งานทั่วไป)</span><span class="sxs-lookup"><span data-stu-id="fb5f4-112">Google Chrome (latest publicly available version)</span></span>
*   <span data-ttu-id="fb5f4-113">Apple Safari (รุ่นล่าสุดที่พร้อมใช้งานทั่วไป)</span><span class="sxs-lookup"><span data-stu-id="fb5f4-113">Apple Safari (latest publicly available version)</span></span>

<span data-ttu-id="fb5f4-114">เมื่อต้องการค้นหารุ่นล่าสุดของแต่ละเว็บเบราเซอร์ ไปที่เว็บไซต์ของผู้ผลิตซอฟต์แวร์</span><span class="sxs-lookup"><span data-stu-id="fb5f4-114">To find the latest release for each web browser, go to the software manufacturer’s website.</span></span> 

> [!NOTE]
> * <span data-ttu-id="fb5f4-115">เมื่อต้องการจับภาพรูปที่สร้างขึ้นจากตัวบันทึกงาน และรวมค่าเหล่านั้นไว้ในเอกสาร Microsoft Word คุณต้องติดตั้งส่วนขยาย Chrome ไว้</span><span class="sxs-lookup"><span data-stu-id="fb5f4-115">To capture images that are generated from Task Recorder and include them in Microsoft Word documents, you must have a Chrome extension installed.</span></span> 
> * <span data-ttu-id="fb5f4-116">ตัวแก้ไขเวิร์กโฟลว์จะเริ่มต้นการใช้งานเป็นแอพลิเคชัน ClickOnce</span><span class="sxs-lookup"><span data-stu-id="fb5f4-116">The Workflow Editor is started as a ClickOnce application.</span></span> <span data-ttu-id="fb5f4-117">เฉพาะ Microsoft Edge และ Internet Explorer (บนเวอร์ชันที่สนับสนุน Microsoft Windows) สนับสนุนแอพลิเคชัน ClickOnce</span><span class="sxs-lookup"><span data-stu-id="fb5f4-117">Only Microsoft Edge and Internet Explorer (on a supported version of Microsoft Windows) support ClickOnce applications.</span></span> <span data-ttu-id="fb5f4-118">แอพลิเคชัน ClickOnce โปรแกรมแก้ไขลำดับงานต้องมีระบบปฏิบัติการที่เข้ากันกับงาน 64 บิต</span><span class="sxs-lookup"><span data-stu-id="fb5f4-118">The Workflow Editor ClickOnce application requires a 64-bit compatible operating system.</span></span>
> * <span data-ttu-id="fb5f4-119">เมื่อต้องการแสดงตัวอย่างไฟล์ PDF เราขอแนะนำให้คุณใช้เบราว์เซอร์ที่ทันสมัย เช่น Microsoft Edge (รุ่นล่าสุดที่พร้อมใช้งานทั่วไป) บน Windows 10 หรือ Google Chrome (รุ่นล่าสุดที่พร้อมใช้งานทั่วไป) บนแท็บเล็ต Windows 10, Windows 8.1, Windows 8, Windows 7 หรือ Google Nexus 10</span><span class="sxs-lookup"><span data-stu-id="fb5f4-119">To preview PDF files, we recommend that you use modern browsers like Microsoft Edge (latest publicly available version) on Windows 10, or Google Chrome (latest publicly available version) on Windows 10, Windows 8.1, Windows 8, Windows 7, or Google Nexus 10 tablet.</span></span>
>   <span data-ttu-id="fb5f4-120">ข้อกำหนดของเครือข่าย</span><span class="sxs-lookup"><span data-stu-id="fb5f4-120">Network requirements</span></span>
> * <span data-ttu-id="fb5f4-121">Dynamics 365 Talent ได้รับการออกแบบมาสำหรับเครือข่ายที่มีเวลาแฝง 250-300 มิลลิวินาที (ms) หรือน้อยกว่า</span><span class="sxs-lookup"><span data-stu-id="fb5f4-121">Dynamics 365 Talent is designed for networks with latency of 250-300 milliseconds (ms) or less.</span></span> <span data-ttu-id="fb5f4-122">นี่คือเวลาแฝงจากไคลเอนต์เบราว์เซอร์ไปยังศูนย์ข้อมูล Microsoft Azure ที่โฮสต์ Talent</span><span class="sxs-lookup"><span data-stu-id="fb5f4-122">This is the latency from a browser client to the Microsoft Azure data center that hosts Talent.</span></span> <span data-ttu-id="fb5f4-123">เราขอแนะนำให้คุณทดสอบเวลาแฝงบนเครือข่ายที่ [www.azurespeed.com](https://www.azurespeed.com "Azure Latency Test")</span><span class="sxs-lookup"><span data-stu-id="fb5f4-123">We recommend that you test network latency at [www.azurespeed.com](https://www.azurespeed.com "Azure Latency Test").</span></span>
> * <span data-ttu-id="fb5f4-124">ข้อกำหนดของแบนด์วิธสำหรับ Talent ขึ้นอยู่กับสถานการณ์ของคุณ</span><span class="sxs-lookup"><span data-stu-id="fb5f4-124">Bandwidth requirements for Talent depend on your scenario.</span></span> <span data-ttu-id="fb5f4-125">สถานการณ์ทั่วไปส่วนใหญ่จำเป็นต้องมีแบนด์วิดท์ที่มากกว่า 50 กิโลไบต์ต่อวินาที (KBps)</span><span class="sxs-lookup"><span data-stu-id="fb5f4-125">Most typical scenarios require a bandwidth of more than 50 kilobytes per second (KBps).</span></span>
> 
> [!WARNING]
> <span data-ttu-id="fb5f4-126">อย่าคำนวณข้อกำหนดของแบนด์วิดท์จากตำแหน่งที่ตั้งของไคลเอนต์ โดยการคูณจำนวนผู้ใช้กับข้อกำหนดของแบนด์วิดท์ต่ำสุด</span><span class="sxs-lookup"><span data-stu-id="fb5f4-126">Don't compute bandwidth requirements from a client location by multiplying the number of users by the minimum bandwidth requirements.</span></span> <span data-ttu-id="fb5f4-127">การใช้งานที่เกิดขึ้นพร้อมกันของตำแหน่งที่ตั้งที่กำหนดเป็นสิ่งที่คำนวณได้ยาก</span><span class="sxs-lookup"><span data-stu-id="fb5f4-127">The concurrent usage of a given location is very difficult to calculate.</span></span> <span data-ttu-id="fb5f4-128">สำหรับลูกค้าที่มีความกังวลเกี่ยวกับข้อกำหนดของแบนด์วิธ ให้ใช้ Talent รุ่นทดลองใช้</span><span class="sxs-lookup"><span data-stu-id="fb5f4-128">For customers who are concerned about bandwidth requirements, use a trial version of Talent.</span></span>

## <a name="supported-microsoft-office-applications"></a><span data-ttu-id="fb5f4-129">แอพลิเคชัน Microsoft Office ที่สนับสนุน</span><span class="sxs-lookup"><span data-stu-id="fb5f4-129">Supported Microsoft Office applications</span></span>

* <span data-ttu-id="fb5f4-130">เมื่อต้องการเรียกใช้ Add-in ของ Microsoft Excel และ Word คุณจะต้องตั้งค่า Microsoft Office 2016 สำหรับ Windows หรือ Mac ไว้</span><span class="sxs-lookup"><span data-stu-id="fb5f4-130">To run the Microsoft Excel and Word add-ins, you must have Microsoft Office 2016 for Windows or Mac installed.</span></span> <span data-ttu-id="fb5f4-131">สำหรับรายละเอียดเพิ่มเติมเกี่ยวกับข้อกำหนดของเวอร์ชัน ให้ดูที่ [การแก้ไขปัญหาการรวมของ Office](../dev-itpro/office-integration/office-integration-troubleshooting.md "การแก้ไขปัญหาการรวมของ Office")</span><span class="sxs-lookup"><span data-stu-id="fb5f4-131">For more details about version requirements, see [Office integration troubleshooting](../dev-itpro/office-integration/office-integration-troubleshooting.md "Office integration troubleshooting").</span></span>
* <span data-ttu-id="fb5f4-132">เมื่อต้องการดูเอกสารที่สร้างขึ้นโดยฟังก์ชันส่งออกไปที่ Excel หรือส่งออกไปที่ Word คุณต้องติดตั้ง Microsoft Office 2007 หรือรุ่นที่ใหม่กว่าไว้</span><span class="sxs-lookup"><span data-stu-id="fb5f4-132">To view documents that are generated by the Export to Excel or Export to Word functionality, you must have Microsoft Office 2007 or later installed.</span></span>

## <a name="regional-availability-languages-and-localization"></a><span data-ttu-id="fb5f4-133">ความพร้อมใช้งานของภูมิภาค ภาษา และการแปลภาษา</span><span class="sxs-lookup"><span data-stu-id="fb5f4-133">Regional availability, languages, and localization</span></span>

<span data-ttu-id="fb5f4-134">คุณสามารถดาวน์โหลดไฟล์ PDF ของประเทศ ภูมิภาค และภาษา ที่ Talent สนับสนุนที่ [ความพร้อมใช้งานระหว่างประเทศของ Microsoft Dynamics 365](https://docs.microsoft.com/dynamics365/get-started/availability)</span><span class="sxs-lookup"><span data-stu-id="fb5f4-134">You can download a PDF file of the countries, regions, and languages Talent supports at [International availability of Microsoft Dynamics 365](https://docs.microsoft.com/dynamics365/get-started/availability).</span></span> 

> [!NOTE]
> <span data-ttu-id="fb5f4-135">ในขณะที่อินเทอร์เฟสผู้ใช้ถูกแปลเป็นภาษาอื่นๆ ข้อมูลผู้ใช้ทั้งหมดจะถูกจัดเก็บอยู่ในภาษาที่ป้อนไว้</span><span class="sxs-lookup"><span data-stu-id="fb5f4-135">While the user interface is localized into other languages, all user data is stored in the language in which it was entered.</span></span> <span data-ttu-id="fb5f4-136">คุณสามารถสร้างอีเมลและเท็มเพลตในภาษาอื่นๆ ได้ แต่ข้อมูล เช่น ข้อมูลการจัดกำหนดการพร้อมใช้งานเฉพาะในภาษาอังกฤษเท่านั้นในขณะนี้</span><span class="sxs-lookup"><span data-stu-id="fb5f4-136">You can create emails and templates in other languages, but data such as scheduling information is only available in English at this time.</span></span>

<span data-ttu-id="fb5f4-137">ถ้าคุณเป็นนักพัฒนาที่สนใจในการสร้างการเลือกกำหนดเฉพาะประเทศหรือภูมิภาค หรือในการสร้างโซลูชันสำหรับประเทศหรือภูมิภาคที่ Microsoft ไม่สนับสนุนในขณะนี้ โปรดดู [โลกาภิวัตน์](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/lcs-solutions/country-region)</span><span class="sxs-lookup"><span data-stu-id="fb5f4-137">If you're a developer interested in creating country- or region-specific customizations, or in creating a solution for a country or region not currently supported by Microsoft, see [Globalization](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/lcs-solutions/country-region).</span></span>

## <a name="update-policy"></a><span data-ttu-id="fb5f4-138">นโยบายการอัพเดต</span><span class="sxs-lookup"><span data-stu-id="fb5f4-138">Update policy</span></span>

<span data-ttu-id="fb5f4-139">Talent ทำหน้าที่เหมือนกับการเสนอของ Cloud</span><span class="sxs-lookup"><span data-stu-id="fb5f4-139">Talent is serviced as a cloud offering.</span></span> <span data-ttu-id="fb5f4-140">การอัพเดตของ Talent เป็นแบบต่อเนื่อง และถูกนำไปใช้โดยอัตโนมัติโดย Microsoft</span><span class="sxs-lookup"><span data-stu-id="fb5f4-140">Talent updates are continuous and applied automatically by Microsoft.</span></span>

<span data-ttu-id="fb5f4-141">การอัพเดตจะถูกนำออกใช้เป็นช่วงเวลาตามปกติ และจะนำไปใช้กับสภาพแวดล้อมทั้งหมด</span><span class="sxs-lookup"><span data-stu-id="fb5f4-141">Updates are released on a regular cadence and will be made to all environments.</span></span> <span data-ttu-id="fb5f4-142">Talent ได้รับการสนับสนุนตาม [นโยบายของ Microsoft Support Lifecycle](https://support.microsoft.com/gp/lifecycle#gp/OSSLpolicy "Microsoft Support Lifecycle") ซึ่งให้คำแนะนำอย่างต่อเนื่องและคาดการณ์ได้สำหรับความพร้อมในการสนับสนุนผลิตภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="fb5f4-142">Talent is supported according to the [Microsoft Support Lifecycle policy](https://support.microsoft.com/gp/lifecycle#gp/OSSLpolicy "Microsoft Support Lifecycle"), which provides consistent and predictable guidelines for product support availability.</span></span>
