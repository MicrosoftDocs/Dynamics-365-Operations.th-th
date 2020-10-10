---
title: ภาพรวมของการพิมพ์เอกสาร
description: คุณสามารถพิมพ์เอกสารได้โดยใช้เครื่องพิมพ์ของไซต์นั้นหรืออุปกรณ์ที่เชื่อมต่อเครือข่าย อย่างใดอย่างหนึ่ง บทความนี้แสดงภาพรวมของวิธีการพิมพ์เอกสาร
author: TJVass
manager: AnnBe
ms.date: 07/25/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: IT Pro, Application User
ms.reviewer: kfend
ms.search.scope: Operations, Core
ms.custom: 69161
ms.assetid: 7815bddd-c4f4-4bc3-a29b-315458065374
ms.search.region: Global
ms.author: tjvass
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 25996cbccf3e9eec6fc29b80b8241e89b5b6b4a5
ms.sourcegitcommit: 71ec2f48185b8104ca52ff70df52263ce5f87f26
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 09/25/2020
ms.locfileid: "3893290"
---
# <a name="document-printing-overview"></a><span data-ttu-id="be1e8-104">ภาพรวมของการพิมพ์เอกสาร</span><span class="sxs-lookup"><span data-stu-id="be1e8-104">Document printing overview</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="be1e8-105">คุณสามารถพิมพ์เอกสารได้โดยใช้เครื่องพิมพ์ของไซต์นั้นหรืออุปกรณ์ที่เชื่อมต่อเครือข่าย อย่างใดอย่างหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="be1e8-105">You can print documents by using either a local printer or a network-connected device.</span></span> <span data-ttu-id="be1e8-106">บทความนี้แสดงภาพรวมของวิธีการพิมพ์เอกสาร</span><span class="sxs-lookup"><span data-stu-id="be1e8-106">This article provides an overview of how documents are printed.</span></span>

## <a name="printing-overview"></a><span data-ttu-id="be1e8-107">ภาพรวมของการพิมพ์</span><span class="sxs-lookup"><span data-stu-id="be1e8-107">Printing overview</span></span>

<span data-ttu-id="be1e8-108">แอพลิเคชันให้การบริการแบบรวมและแอพลิเคชันไคลเอนต์ที่ทำให้ง่ายต่อการสร้าง จัดเก็บ และกระจายเอกสารที่สนับสนุนกิจกรรมทางธุรกิจ</span><span class="sxs-lookup"><span data-stu-id="be1e8-108">The application provides integrated services and client applications that make it easy to generate, store, and distribute documents that support business activity.</span></span> <span data-ttu-id="be1e8-109">คุณสามารถพิมพ์เอกสารได้โดยใช้เครื่องพิมพ์ของไซต์นั้นหรืออุปกรณ์ที่เชื่อมต่อเครือข่าย อย่างใดอย่างหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="be1e8-109">You can print documents by using either a local printer or a network-connected device.</span></span> <span data-ttu-id="be1e8-110">นอกจากนี้ คุณสามารถส่งออกหน้าและรายงานโดยตรงได้จากไคลเอ็นต์ เป็นไฟล์ PDF หรือเอกสาร Microsoft Office</span><span class="sxs-lookup"><span data-stu-id="be1e8-110">In addition, you can export pages and reports directly from the client, as PDF files or Microsoft Office documents.</span></span> <span data-ttu-id="be1e8-111">ในตอนท้าย ปริมาณแบบกระจายช่วยให้คุณสามารถพิมพ์เอกสารทางธุรกิจได้โดยตรงจากอุปกรณ์เคลื่อนที่ โดยใช้ทรัพยากรเครือข่าย</span><span class="sxs-lookup"><span data-stu-id="be1e8-111">Finally, the distributed workload lets you print business documents directly from a mobile device by using network resources.</span></span> <span data-ttu-id="be1e8-112">แม้ว่าความต้องการในการพิมพ์อาจแตกต่างกันไป โดยทั่วไปอุตสาหกรรมทั้งหมดจะต้องสร้างสำเนาของเอกสารทางธุรกิจโดยใช้แอพลิเคชั่น</span><span class="sxs-lookup"><span data-stu-id="be1e8-112">Although printing requirements might vary, all industries typically must create hard copies of business documents by using the application.</span></span> <span data-ttu-id="be1e8-113">การพิมพ์เอกสารบนอุปกรณ์เครือข่ายจากแอพลิเคชันที่เป็นโฮสต์ แสดงชุดเฉพาะของสิ่งที่ท้าทาย</span><span class="sxs-lookup"><span data-stu-id="be1e8-113">Printing documents on network devices from hosted applications presents a unique set of challenges.</span></span> <span data-ttu-id="be1e8-114">ยกตัวอย่างเช่น</span><span class="sxs-lookup"><span data-stu-id="be1e8-114">Here are some examples:</span></span>

- <span data-ttu-id="be1e8-115">โปรแกรมควบคุมการพิมพ์อาจไม่พร้อมใช้งานบนอุปกรณ์ของผู้ใช้</span><span class="sxs-lookup"><span data-stu-id="be1e8-115">Print drivers might not be available on the user's device.</span></span>
- <span data-ttu-id="be1e8-116">อุปกรณ์ของผู้ใช้อาจไม่สามารถเชื่อมต่อกับเครือข่ายของบริษัทได้</span><span class="sxs-lookup"><span data-stu-id="be1e8-116">The user's device might not be connected to the corporate network.</span></span>

<span data-ttu-id="be1e8-117">โดยใช้โฮสต์ที่จัดสรรไว้และทำตามขั้นตอนง่ายๆ ไม่กี่ขั้นตอน ผู้ดูแลระบบสามารถตั้งค่าคอนฟิกการปรับใช้ได้ เพื่อให้ผู้ใช้สามารถพิมพ์ได้โดยตรงจากแอพลิเคชันทางธุรกิจบนอุปกรณ์เครือข่าย</span><span class="sxs-lookup"><span data-stu-id="be1e8-117">By using a dedicated host and following a few easy steps, system administrators can configure deployments so that users can print directly from business applications on network devices.</span></span>

### <a name="application-printing-scenarios"></a><span data-ttu-id="be1e8-118">สถานการณ์จำลองการพิมพ์ของแอพลิเคชัน</span><span class="sxs-lookup"><span data-stu-id="be1e8-118">Application printing scenarios</span></span> 

<span data-ttu-id="be1e8-119">ตารางต่อไปนี้จะอธิบายสถานการณ์การพิมพ์หลักสามสถานการณ์</span><span class="sxs-lookup"><span data-stu-id="be1e8-119">The following table describes the three primary printing scenarios.</span></span>

| <span data-ttu-id="be1e8-120">สถานการณ์จำลอง</span><span class="sxs-lookup"><span data-stu-id="be1e8-120">Scenario</span></span>                        | <span data-ttu-id="be1e8-121">เป้าหมาย</span><span class="sxs-lookup"><span data-stu-id="be1e8-121">Goal</span></span>                                                      | <span data-ttu-id="be1e8-122">โซลูชัน</span><span class="sxs-lookup"><span data-stu-id="be1e8-122">Solution</span></span> |
|---------------------------------|-----------------------------------------------------------|----------|
| <span data-ttu-id="be1e8-123">1. การพิมพ์สิ่งที่คุณเห็น</span><span class="sxs-lookup"><span data-stu-id="be1e8-123">1. Printing what you see</span></span>        | <span data-ttu-id="be1e8-124">พิมพ์สิ่งที่แสดงขึ้นในเบราเซอร์ในขณะนี้</span><span class="sxs-lookup"><span data-stu-id="be1e8-124">Print what is currently shown in the browser.</span></span>             | <span data-ttu-id="be1e8-125">เว็บเพจรุ่น "พิมพ์ได้โดยง่าย" ถูกสร้างขึ้นสำหรับเบราเซอร์</span><span class="sxs-lookup"><span data-stu-id="be1e8-125">A "print-friendly" version of the webpage is generated for the browser.</span></span> |
| <span data-ttu-id="be1e8-126">2. การพิมพ์เชิงโต้ตอบ</span><span class="sxs-lookup"><span data-stu-id="be1e8-126">2. Interactive printing</span></span>         | <span data-ttu-id="be1e8-127">พิมพ์เอกสารความแม่นยำบนอุปกรณ์เชื่อมต่อเฉพาะที่</span><span class="sxs-lookup"><span data-stu-id="be1e8-127">Print a precision document on a locally connected device.</span></span> | <span data-ttu-id="be1e8-128">คุณสามารถส่งออกรายงานรุ่น PDF และดาวน์โหลดไปยังเบราเซอร์ได้</span><span class="sxs-lookup"><span data-stu-id="be1e8-128">You can export a PDF version of the report and download it to the browser.</span></span> |
| <span data-ttu-id="be1e8-129">3. การพิมพ์บนอุปกรณ์เครือข่าย</span><span class="sxs-lookup"><span data-stu-id="be1e8-129">3. Printing on a network device</span></span> | <span data-ttu-id="be1e8-130">ส่งเอกสารความแม่นยำไปยังอุปกรณ์เครื่องพิมพ์โดเมน</span><span class="sxs-lookup"><span data-stu-id="be1e8-130">Send a precision document to a domain printer device.</span></span>     | <span data-ttu-id="be1e8-131">เอกสารแบบความแม่นยำถูกส่งไปที่แอพลิเคชันไคลเอนต์ที่รันบนเซิร์ฟเวอร์ที่โฮสต์ในโดเมนของลูกค้า</span><span class="sxs-lookup"><span data-stu-id="be1e8-131">A precision document is sent to a client application that runs on a server that is hosted in the customer's domain.</span></span> |

<span data-ttu-id="be1e8-132">เนื่องจากโซลูชันแตกต่างกันไป ขึ้นอยู่กับสถานการณ์จำลอง แอพลิเคชันให้บริการภายในและเครื่องมือ เพื่อช่วยผู้ใช้ให้บรรลุถึงเป้าหมายของผู้ใช้:</span><span class="sxs-lookup"><span data-stu-id="be1e8-132">Because the solution varies, depending on the scenario, applications provide built-in services and tooling to help users accomplish their goals:</span></span>

- <span data-ttu-id="be1e8-133">**สถานการณ์จำลอง 1** ได้รับการสนับสนุนโดยการแสดงผลของเบราเซอร์ของไคลเอนต์ HTML5</span><span class="sxs-lookup"><span data-stu-id="be1e8-133">**Scenario 1** is supported by the browser's rendering of the HTML5 client.</span></span>
- <span data-ttu-id="be1e8-134">**สถานการณ์จำลอง 2** ใช้แอปพลิเคชันไคลเอนต์และบริการ Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="be1e8-134">**Scenario 2** uses client applications and Microsoft 365 services.</span></span>
- <span data-ttu-id="be1e8-135">**สถานการณ์สมมติที่ 3** ต้องการการสนับสนุนจากแอพพลิเคชันไคลเอ็นต์และจากบริการที่มีการโฮสต์ใน Microsoft Azure</span><span class="sxs-lookup"><span data-stu-id="be1e8-135">**Scenario 3** requires support from client applications and from services that are hosted in Microsoft Azure.</span></span>

<span data-ttu-id="be1e8-136">นอกเหนือจากแท่นวางที่ปรับใช้ในการบอกรับเป็นสมาชิก Azure แอปพลิเคชัน Finance and Operations จะให้ลูกค้ามีแอปพลิเคชัน Azure ฝ่ายแรกแบบรวม ที่ช่วยให้พวกเขาใช้งานอุปกรณ์ที่เป็นโฮสต์โดเมนเพื่อพิมพ์เอกสารได้ง่ายขึ้น</span><span class="sxs-lookup"><span data-stu-id="be1e8-136">In addition to the platform that is deployed to the Azure subscription, Finance and Operations applications provide customers with an integrated, first-party Azure application that helps them more easily use domain-hosted devices to print documents.</span></span>

## <a name="service-overview"></a><span data-ttu-id="be1e8-137">ภาพรวมของการบริการ</span><span class="sxs-lookup"><span data-stu-id="be1e8-137">Service overview</span></span>
<span data-ttu-id="be1e8-138">ในขณะที่เอกสารที่สร้างขึ้นโดยแอพลิเคชันที่เป็นโฮสต์กำลังรอที่จะถูกพิมพ์บนอุปกรณ์ที่เชื่อมต่อเครือข่าย เอกสารจะถูกจัดเก็บใน Azure blob storage</span><span class="sxs-lookup"><span data-stu-id="be1e8-138">While documents that are produced by the hosted applications are waiting to be printed on a network-connected device, they are stored in Azure blob storage.</span></span> <span data-ttu-id="be1e8-139">[ติดตั้งเอเจนต์การกำหนดเส้นทางเอกสารเพื่อเปิดใช้งานการพิมพ์ผ่านเครือข่าย](install-document-routing-agent.md) ใช้การรับรองความถูกต้อง Azure เพื่อสร้างช่องทางที่ปลอดภัยไปยังบริการ Azure</span><span class="sxs-lookup"><span data-stu-id="be1e8-139">The [Install the Document Routing Agent to enable network printing](install-document-routing-agent.md) uses Azure authentication to establish a secure channel to the Azure services.</span></span>

<span data-ttu-id="be1e8-140">**ลำดับการดำเนินการ**</span><span class="sxs-lookup"><span data-stu-id="be1e8-140">**Execution sequence**</span></span>

1. <span data-ttu-id="be1e8-141">รายงานถูกสร้างขึ้นโดย Microsoft SQL Server Reporting Services (SSRS) และจัดเก็บในที่จัดเก็บ Azure blob</span><span class="sxs-lookup"><span data-stu-id="be1e8-141">The report is generated by Microsoft SQL Server Reporting Services (SSRS) and stored in Azure blob storage.</span></span> <span data-ttu-id="be1e8-142">การตั้งค่าเครื่องพิมพ์ที่แนบถูกเก็บไว้พร้อมกับเอกสาร</span><span class="sxs-lookup"><span data-stu-id="be1e8-142">Attached printer settings are stored together with the document.</span></span>
2. <span data-ttu-id="be1e8-143">เอเจนต์การกำหนดเส้นทางเอกสารสอบถามคิว Azure Service Bus สำหรับงานที่ใช้งานอยู่</span><span class="sxs-lookup"><span data-stu-id="be1e8-143">The Document Routing Agent queries the Azure Service Bus queue for active jobs.</span></span>
3. <span data-ttu-id="be1e8-144">เอกสารจะถูกดาวน์โหลดโดยเอเจนต์การกำหนดเส้นทางเอกสาร และเก็บพักไปยังเครื่องพิมพ์บนเครือข่าย</span><span class="sxs-lookup"><span data-stu-id="be1e8-144">The document is downloaded by the Document Routing Agent and spooled to the network printer.</span></span>

<span data-ttu-id="be1e8-145">โซลูชันบนไคลเอ็นต์ทำให้ลูกค้าสามารถจัดการระดับของความต้องการพิมพ์ของพวกเขาได้</span><span class="sxs-lookup"><span data-stu-id="be1e8-145">The client-based solution lets customers manage the scale of their printing needs.</span></span> <span data-ttu-id="be1e8-146">ลูกค้าที่มีปริมาณงานพิมพ์ในปริมาณมาก สามารถติดตั้งเอเจนต์การกำหนดเส้นทางเอกสารได้หลายรายการ เพื่อเพิ่มจำนวนของการพิมพ์ที่เกิดขึ้นพร้อมกัน</span><span class="sxs-lookup"><span data-stu-id="be1e8-146">Customers who have heavy-volume printing workloads can install many Document Routing Agents to increase the number of concurrent printing operations.</span></span> <span data-ttu-id="be1e8-147">อีกทางหนึ่งคือ ลูกค้าบางรายต้องการติดตั้งของเอเจนต์การกำหนดเส้นทางเอกสารที่ไม่มากนัก เพื่อจัดการความต้องการในการพิมพ์ที่คาดไว้ของพวกเขา</span><span class="sxs-lookup"><span data-stu-id="be1e8-147">Alternatively, some customers require very few installations of the Document Routing Agent to handle their anticipated printing needs.</span></span>

### <a name="service-components-for-network-printing"></a><span data-ttu-id="be1e8-148">ส่วนประกอบของบริการสำหรับการพิมพ์บนเครือข่าย</span><span class="sxs-lookup"><span data-stu-id="be1e8-148">Service components for network printing</span></span>

<span data-ttu-id="be1e8-149">แผนภาพต่อไปนี้แสดงส่วนประกอบพื้นฐานซึ่งช่วยสนับสนุนการดำเนินงานพิมพ์บนเครือข่าย</span><span class="sxs-lookup"><span data-stu-id="be1e8-149">The following diagram shows the basic components that help support network printing operations.</span></span>

<span data-ttu-id="be1e8-150">[![ส่วนประกอบของบริการสำหรับการพิมพ์บนเครือข่าย\_2016](./media/service-components-for-network-printing_2016.png)](./media/service-components-for-network-printing_2016.png)</span><span class="sxs-lookup"><span data-stu-id="be1e8-150">[![service-components-for-network-printing\_2016](./media/service-components-for-network-printing_2016.png)](./media/service-components-for-network-printing_2016.png)</span></span>

<span data-ttu-id="be1e8-151">โปรดสังเกตว่า เครื่องพิมพ์เดียวสามารถลงทะเบียนกับตัวแทนการกำหนดเส้นทางเอกสารหลายรายการได้</span><span class="sxs-lookup"><span data-stu-id="be1e8-151">Note that a single printer can be registered with multiple Document Routing Agents.</span></span> <span data-ttu-id="be1e8-152">เมื่อต้องการแก้ไขการกำหนดลักษณะเครื่องพิมพ์ บริการที่เป็นโฮสต์ใช้พาธของเครือข่ายที่ระบุเครื่องพิมพ์บนเครือข่ายทุกเครื่องโดยเฉพาะ</span><span class="sxs-lookup"><span data-stu-id="be1e8-152">To resolve the printer preferences, the hosted service uses the network path that uniquely identifies every network printer.</span></span> <span data-ttu-id="be1e8-153">ดังนั้น แม้ว่าเมื่อมีการลงทะเบียนเครื่องพิมพ์โดยไคลเอนต์หลายรายการ จะปรากฏเป็นการเลือกเดียวในรายการของเครื่องพิมพ์ที่พร้อมใช้งานในแอพลิเคชัน</span><span class="sxs-lookup"><span data-stu-id="be1e8-153">As a result, even when a printer is registered by multiple clients, it appears as a single selection in the list of printers available in applications.</span></span>
