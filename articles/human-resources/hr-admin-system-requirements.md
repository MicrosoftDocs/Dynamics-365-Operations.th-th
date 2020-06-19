---
title: ความต้องการของระบบ
description: บทความนี้อธิบายถึงข้อกำหนดสำหรับ Microsoft Dynamics 365 Human Resources
author: andreabichsel
manager: AnnBe
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: SystemAdministrationWorkspaceForm
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: f68b8f642ada1345e7097b5e7220e222b132b1dd
ms.sourcegitcommit: ba340f836e472f13f263dec46a49847c788fca44
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 06/04/2020
ms.locfileid: "3431164"
---
# <a name="system-requirements"></a><span data-ttu-id="d678c-103">ความต้องการของระบบ</span><span class="sxs-lookup"><span data-stu-id="d678c-103">System requirements</span></span>

<span data-ttu-id="d678c-104">บทความนี้อธิบายถึงข้อกำหนดสำหรับ Microsoft Dynamics 365 Human Resources</span><span class="sxs-lookup"><span data-stu-id="d678c-104">This article describes requirements for Microsoft Dynamics 365 Human Resources.</span></span> <span data-ttu-id="d678c-105">นอกจากนี้ ยังกำหนดโครงร่างประเทศและภูมิภาคที่ทรัพยากรบุคคลพร้อมใช้งาน และข้อมูลเกี่ยวกับภาษาและการแปลสำหรับข้อมูลทรัพยากรบุคคล</span><span class="sxs-lookup"><span data-stu-id="d678c-105">It also outlines the countries and regions where Human Resources is available, and information about languages and localization for Human Resources data.</span></span>

## <a name="supported-web-browsers"></a><span data-ttu-id="d678c-106">เว็บเบราเซอร์ที่สนับสนุน</span><span class="sxs-lookup"><span data-stu-id="d678c-106">Supported web browsers</span></span>

<span data-ttu-id="d678c-107">ทรัพยากรบุคคลสามารถเรียกใช้ในเว็บเบราเซอร์ใดก็ได้ต่อไปนี้ที่ทำงานบนระบบปฏิบัติการที่ระบุ:</span><span class="sxs-lookup"><span data-stu-id="d678c-107">Human Resources can run in any of the following web browsers that run on the specified operating systems:</span></span> 

*   <span data-ttu-id="d678c-108">Microsoft Edge (รุ่นล่าสุดที่พร้อมใช้งานทั่วไป) บน Windows 10</span><span class="sxs-lookup"><span data-stu-id="d678c-108">Microsoft Edge (latest publicly available version) on Windows 10</span></span>
*   <span data-ttu-id="d678c-109">Internet Explorer 11 บน Windows 10, Windows 8.1 หรือ Windows 7</span><span class="sxs-lookup"><span data-stu-id="d678c-109">Internet Explorer 11 on Windows 10, Windows 8.1, or Windows 7</span></span>
*   <span data-ttu-id="d678c-110">Google Chrome (รุ่นล่าสุดที่พร้อมใช้งานทั่วไป)</span><span class="sxs-lookup"><span data-stu-id="d678c-110">Google Chrome (latest publicly available version)</span></span>
*   <span data-ttu-id="d678c-111">Apple Safari (รุ่นล่าสุดที่พร้อมใช้งานทั่วไป)</span><span class="sxs-lookup"><span data-stu-id="d678c-111">Apple Safari (latest publicly available version)</span></span>

<span data-ttu-id="d678c-112">เมื่อต้องการค้นหารุ่นล่าสุดของแต่ละเว็บเบราเซอร์ ไปที่เว็บไซต์ของผู้ผลิตซอฟต์แวร์</span><span class="sxs-lookup"><span data-stu-id="d678c-112">To find the latest release for each web browser, go to the software manufacturer’s website.</span></span> 

> [!NOTE]
> * <span data-ttu-id="d678c-113">เมื่อต้องการจับภาพรูปที่สร้างขึ้นจากตัวบันทึกงาน และรวมค่าเหล่านั้นไว้ในเอกสาร Microsoft Word คุณต้องติดตั้งส่วนขยาย Chrome ไว้</span><span class="sxs-lookup"><span data-stu-id="d678c-113">To capture images that are generated from Task Recorder and include them in Microsoft Word documents, you must have a Chrome extension installed.</span></span> 
> * <span data-ttu-id="d678c-114">ตัวแก้ไขเวิร์กโฟลว์จะเริ่มต้นการใช้งานเป็นแอพลิเคชัน ClickOnce</span><span class="sxs-lookup"><span data-stu-id="d678c-114">The Workflow Editor is started as a ClickOnce application.</span></span> <span data-ttu-id="d678c-115">เฉพาะ Microsoft Edge และ Internet Explorer (บนเวอร์ชันที่สนับสนุน Microsoft Windows) สนับสนุนแอพลิเคชัน ClickOnce</span><span class="sxs-lookup"><span data-stu-id="d678c-115">Only Microsoft Edge and Internet Explorer (on a supported version of Microsoft Windows) support ClickOnce applications.</span></span> <span data-ttu-id="d678c-116">แอพลิเคชัน ClickOnce โปรแกรมแก้ไขลำดับงานต้องมีระบบปฏิบัติการที่เข้ากันกับงาน 64 บิต</span><span class="sxs-lookup"><span data-stu-id="d678c-116">The Workflow Editor ClickOnce application requires a 64-bit compatible operating system.</span></span>
> * <span data-ttu-id="d678c-117">เมื่อต้องการแสดงตัวอย่างไฟล์ PDF เราขอแนะนำให้คุณใช้เบราว์เซอร์ที่ทันสมัย เช่น Microsoft Edge (รุ่นล่าสุดที่พร้อมใช้งานทั่วไป) บน Windows 10 หรือ Google Chrome (รุ่นล่าสุดที่พร้อมใช้งานทั่วไป) บนแท็บเล็ต Windows 10, Windows 8.1, Windows 8, Windows 7 หรือ Google Nexus 10</span><span class="sxs-lookup"><span data-stu-id="d678c-117">To preview PDF files, we recommend that you use modern browsers like Microsoft Edge (latest publicly available version) on Windows 10, or Google Chrome (latest publicly available version) on Windows 10, Windows 8.1, Windows 8, Windows 7, or Google Nexus 10 tablet.</span></span>
>   <span data-ttu-id="d678c-118">ข้อกำหนดของเครือข่าย</span><span class="sxs-lookup"><span data-stu-id="d678c-118">Network requirements</span></span>
> * <span data-ttu-id="d678c-119">ทรัพยากรบุคคลได้รับการออกแบบมาสำหรับเครือข่ายที่มีเวลาแฝง 250-300 มิลลิวินาที (ms) หรือน้อยกว่า</span><span class="sxs-lookup"><span data-stu-id="d678c-119">Human Resources is designed for networks with latency of 250-300 milliseconds (ms) or less.</span></span> <span data-ttu-id="d678c-120">นี่คือเวลาแฝงจากไคลเอนต์เบราว์เซอร์ไปยังศูนย์ข้อมูล Microsoft Azure ที่โฮสต์ทรัพยากรบุคคล</span><span class="sxs-lookup"><span data-stu-id="d678c-120">This is the latency from a browser client to the Microsoft Azure data center that hosts Human Resources.</span></span> <span data-ttu-id="d678c-121">เราขอแนะนำให้คุณทดสอบเวลาแฝงบนเครือข่ายที่ [www.azurespeed.com](https://www.azurespeed.com "การทดสอบเวลาแฝง Azure")</span><span class="sxs-lookup"><span data-stu-id="d678c-121">We recommend that you test network latency at [www.azurespeed.com](https://www.azurespeed.com "Azure Latency Test").</span></span>
> * <span data-ttu-id="d678c-122">ข้อกำหนดของแบนด์วิธสำหรับทรัพยากรบุคคลขึ้นอยู่กับสถานการณ์ของคุณ</span><span class="sxs-lookup"><span data-stu-id="d678c-122">Bandwidth requirements for Human Resources depend on your scenario.</span></span> <span data-ttu-id="d678c-123">สถานการณ์ทั่วไปส่วนใหญ่จำเป็นต้องมีแบนด์วิดท์ที่มากกว่า 50 กิโลไบต์ต่อวินาที (KBps)</span><span class="sxs-lookup"><span data-stu-id="d678c-123">Most typical scenarios require a bandwidth of more than 50 kilobytes per second (KBps).</span></span>
> 
> [!WARNING]
> <span data-ttu-id="d678c-124">อย่าคำนวณข้อกำหนดของแบนด์วิดท์จากตำแหน่งที่ตั้งของไคลเอนต์ โดยการคูณจำนวนผู้ใช้กับข้อกำหนดของแบนด์วิดท์ต่ำสุด</span><span class="sxs-lookup"><span data-stu-id="d678c-124">Don't compute bandwidth requirements from a client location by multiplying the number of users by the minimum bandwidth requirements.</span></span> <span data-ttu-id="d678c-125">การใช้งานที่เกิดขึ้นพร้อมกันของตำแหน่งที่ตั้งที่กำหนดเป็นสิ่งที่คำนวณได้ยาก</span><span class="sxs-lookup"><span data-stu-id="d678c-125">The concurrent usage of a given location is very difficult to calculate.</span></span> <span data-ttu-id="d678c-126">สำหรับลูกค้าที่มีความกังวลเกี่ยวกับข้อกำหนดของแบนด์วิธ ให้ใช้ทรัพยากรบุคคลรุ่นทดลองใช้</span><span class="sxs-lookup"><span data-stu-id="d678c-126">For customers who are concerned about bandwidth requirements, use a trial version of Human Resources.</span></span>

## <a name="supported-microsoft-office-applications"></a><span data-ttu-id="d678c-127">แอพลิเคชัน Microsoft Office ที่สนับสนุน</span><span class="sxs-lookup"><span data-stu-id="d678c-127">Supported Microsoft Office applications</span></span>

* <span data-ttu-id="d678c-128">เมื่อต้องการเรียกใช้ Add-in ของ Microsoft Excel และ Word คุณจะต้องตั้งค่า Microsoft Office 2016 สำหรับ Windows หรือ Mac ไว้</span><span class="sxs-lookup"><span data-stu-id="d678c-128">To run the Microsoft Excel and Word add-ins, you must have Microsoft Office 2016 for Windows or Mac installed.</span></span> <span data-ttu-id="d678c-129">สำหรับรายละเอียดเพิ่มเติมเกี่ยวกับข้อกำหนดเวอร์ชัน ให้ดูที่ [การแก้ไขปัญหาการรวม Office](../dev-itpro/office-integration/office-integration-troubleshooting.md "การแก้ไขปัญหาการรวม Office")</span><span class="sxs-lookup"><span data-stu-id="d678c-129">For more details about version requirements, see [Office integration troubleshooting](../dev-itpro/office-integration/office-integration-troubleshooting.md "Office integration troubleshooting").</span></span>
* <span data-ttu-id="d678c-130">เมื่อต้องการดูเอกสารที่สร้างขึ้นโดยฟังก์ชันส่งออกไปที่ Excel หรือส่งออกไปที่ Word คุณต้องติดตั้ง Microsoft Office 2007 หรือรุ่นที่ใหม่กว่าไว้</span><span class="sxs-lookup"><span data-stu-id="d678c-130">To view documents that are generated by the Export to Excel or Export to Word functionality, you must have Microsoft Office 2007 or later installed.</span></span>

## <a name="regional-availability-languages-and-localization"></a><span data-ttu-id="d678c-131">ความพร้อมใช้งานของภูมิภาค ภาษา และการแปลภาษา</span><span class="sxs-lookup"><span data-stu-id="d678c-131">Regional availability, languages, and localization</span></span>

<span data-ttu-id="d678c-132">คุณสามารถดาวน์โหลดไฟล์ PDF ของประเทศ ภูมิภาค และภาษาที่ทรัพยากรบุคคลสนับสนุนที่ [ความพร้อมใช้งานระหว่างประเทศของ Microsoft Dynamics 365](https://docs.microsoft.com/dynamics365/get-started/availability)</span><span class="sxs-lookup"><span data-stu-id="d678c-132">You can download a PDF file of the countries, regions, and languages Human Resources supports at [International availability of Microsoft Dynamics 365](https://docs.microsoft.com/dynamics365/get-started/availability).</span></span> 

> [!NOTE]
> <span data-ttu-id="d678c-133">ในขณะที่อินเทอร์เฟสผู้ใช้ถูกแปลเป็นภาษาอื่นๆ ข้อมูลผู้ใช้ทั้งหมดจะถูกจัดเก็บอยู่ในภาษาที่ป้อนไว้</span><span class="sxs-lookup"><span data-stu-id="d678c-133">While the user interface is localized into other languages, all user data is stored in the language in which it was entered.</span></span> <span data-ttu-id="d678c-134">คุณสามารถสร้างอีเมลและเท็มเพลตในภาษาอื่นๆ ได้ แต่ข้อมูล เช่น ข้อมูลการจัดกำหนดการพร้อมใช้งานเฉพาะในภาษาอังกฤษเท่านั้นในขณะนี้</span><span class="sxs-lookup"><span data-stu-id="d678c-134">You can create emails and templates in other languages, but data such as scheduling information is only available in English at this time.</span></span>

<span data-ttu-id="d678c-135">ถ้าคุณเป็นนักพัฒนาที่สนใจในการสร้างการเลือกกำหนดเฉพาะประเทศหรือภูมิภาค หรือในการสร้างโซลูชันสำหรับประเทศหรือภูมิภาคที่ Microsoft ไม่สนับสนุนในขณะนี้ โปรดดู [โลกาภิวัตน์](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/lcs-solutions/country-region)</span><span class="sxs-lookup"><span data-stu-id="d678c-135">If you're a developer interested in creating country- or region-specific customizations, or in creating a solution for a country or region not currently supported by Microsoft, see [Globalization](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/lcs-solutions/country-region).</span></span>
