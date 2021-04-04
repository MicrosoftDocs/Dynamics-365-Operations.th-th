---
title: ชนิดของปลายทาง ER เครื่องพิมพ์
description: หัวข้อนี้อธิบายวิธีการตั้งค่าคอนฟิกปลายทางเครื่องพิมพ์ให้กับแต่ละส่วนประกอบโฟลเดอร์หรือไฟล์ ของรูปแบบการรายงานทางอิเล็กทรอนิกส์ (ER)
author: NickSelin
manager: AnnBe
ms.date: 02/24/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: DocuType, ERSolutionTable, ERFormatDestinationTable
audience: Application User
ms.reviewer: kfend
ms.custom: 97423
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2020-04-01
ms.dyn365.ops.version: AX 10.0.9
ms.openlocfilehash: 19613d9dfba21d591d96a2df45bedb80c043b3a7
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 03/09/2021
ms.locfileid: "5561961"
---
# <a name="printer-destination"></a><a name="PrinterDestinationType"></a><span data-ttu-id="6127c-103">ปลายทางของเครื่องพิมพ์</span><span class="sxs-lookup"><span data-stu-id="6127c-103">Printer destination</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="6127c-104">คุณสามารถส่งเอกสารที่สร้างขึ้นโดยตรงไปยังเครื่องพิมพ์บนเครือข่ายสำหรับการพิมพ์โดยตรง</span><span class="sxs-lookup"><span data-stu-id="6127c-104">You can send a generated document directly to a network printer for direct printing.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="6127c-105">ข้อกำหนดเบื้องต้น</span><span class="sxs-lookup"><span data-stu-id="6127c-105">Prerequisites</span></span>

<span data-ttu-id="6127c-106">ก่อนที่คุณจะเริ่มต้น คุณต้องติดตั้งและตั้งค่าคอนฟิกตัวแทนการกำหนดเส้นทางเอกสาร แล้วลงทะเบียนเครื่องพิมพ์บนเครือข่าย</span><span class="sxs-lookup"><span data-stu-id="6127c-106">Before you begin, you must install and configure the Document Routing Agent, and then register the network printers.</span></span> <span data-ttu-id="6127c-107">สำหรับข้อมูลเพิ่มเติม ดูที่ [ติดตั้งเอเจนต์การกำหนดเส้นทางเอกสารเพื่อเปิดใช้งานการพิมพ์ผ่านเครือข่าย](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/analytics/install-document-routing-agent)</span><span class="sxs-lookup"><span data-stu-id="6127c-107">For more information, see [Install the Document Routing Agent to enable network printing](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/analytics/install-document-routing-agent).</span></span>

## <a name="make-the-printer-destination-available"></a><span data-ttu-id="6127c-108">ทำให้การกำหนดปลายทางเครื่องพิมพ์พร้อมใช้งาน</span><span class="sxs-lookup"><span data-stu-id="6127c-108">Make the Printer destination available</span></span>

<span data-ttu-id="6127c-109">เมื่อต้องการเปิดใช้งานปลายทาง **เครื่องพิมพ์** ในอินสแตนซ์ปัจจุบันของ Microsoft Dynamics 365 Finance ไปที่ **การจัดการคุณลักษณะ** และเปิดใช้งานคุณลักษณะต่อไปนี้ในใบสั่งนี้:</span><span class="sxs-lookup"><span data-stu-id="6127c-109">To make the **Printer** destination available in the current instance of Microsoft Dynamics 365 Finance, go to the **Feature management** workspace, and turn on the following features, in this order:</span></span>

1. <span data-ttu-id="6127c-110">แปลงเอกสารขาออกของการรายงานทางอิเล็กทรอนิกส์จากรูปแบบ Microsoft Office เป็น PDF</span><span class="sxs-lookup"><span data-stu-id="6127c-110">Convert Electronic Reporting outbound documents from Microsoft Office formats to PDF</span></span>
2. <span data-ttu-id="6127c-111">เอเจนต์การกำหนดเส้นทางเอกสารเป็นปลายทางการรายงานทางอิเล็กทรอนิกส์สำหรับเอกสารขาออก</span><span class="sxs-lookup"><span data-stu-id="6127c-111">Document Routing Agent as Electronic Reporting destination for outbound documents</span></span>

<span data-ttu-id="6127c-112">[![การเปิดใช้งานคุณลักษณะปลายทางเครื่องพิมพ์ ER ในการจัดการคุณลักษณะ](./media/ER_Destinations-EnablePrinterDestinationFeature.png)](./media/ER_Destinations-EnablePrinterDestinationFeature.png)</span><span class="sxs-lookup"><span data-stu-id="6127c-112">[![Turning on the ER printer destination feature in Feature management](./media/ER_Destinations-EnablePrinterDestinationFeature.png)](./media/ER_Destinations-EnablePrinterDestinationFeature.png)</span></span>

### <a name="applicability"></a><span data-ttu-id="6127c-113">การมีผลบังคับใช้</span><span class="sxs-lookup"><span data-stu-id="6127c-113">Applicability</span></span>

<span data-ttu-id="6127c-114">ปลายทาง **เครื่องพิมพ์** สามารถตั้งค่าคอนฟิกสำหรับส่วนประกอบของไฟล์ที่ใช้ในการสร้างผลลัพธ์ในรูปแบบไฟล์ PDF ที่พิมพ์ได้ (ตัวผสาน PDF หรือองค์ประกอบไฟล์ PDF) หรือ Microsoft Office Excel /Word (ไฟล์ Excel) เท่านั้น</span><span class="sxs-lookup"><span data-stu-id="6127c-114">The **Printer** destination can be configured only for file components that are used to generate output in either printable PDF format (PDF Merger or PDF file format elements) or Microsoft Office Excel/Word format (Excel file).</span></span> <span data-ttu-id="6127c-115">เมื่อมีการสร้างผลลัพธ์ในรูปแบบ PDF จะมีการส่งออกไปยังเครื่องพิมพ์</span><span class="sxs-lookup"><span data-stu-id="6127c-115">When output is generated in PDF format, it's sent to a printer.</span></span> <span data-ttu-id="6127c-116">เมื่อมีการสร้างผลลัพธ์ในรูปแบบ Microsoft Office โดยอัตโนมัติ จะมีการแปลงเป็นรูปแบบ PDF แล้วส่งไปยังเครื่องพิมพ์</span><span class="sxs-lookup"><span data-stu-id="6127c-116">When output is generated in Microsoft Office format, it's automatically converted to PDF format and then sent to a printer.</span></span>

### <a name="limitations"></a><span data-ttu-id="6127c-117">การจำกัด</span><span class="sxs-lookup"><span data-stu-id="6127c-117">Limitations</span></span>

<span data-ttu-id="6127c-118">ปลายทาง **เครื่องพิมพ์** ใช้ในการปรับใช้สำหรับ cloud เท่านั้น</span><span class="sxs-lookup"><span data-stu-id="6127c-118">The **Printer** destination is implemented only for cloud deployments.</span></span>

### <a name="use-the-printer-destination"></a><span data-ttu-id="6127c-119">ใช้ปลายทางเครื่องพิมพ์</span><span class="sxs-lookup"><span data-stu-id="6127c-119">Use the Printer destination</span></span>

1. <span data-ttu-id="6127c-120">ตั้งค่าตัวเลือก **เปิดใช้งาน** เป็น **ใช่** เพื่อส่งเอกสารที่สร้างขึ้นไปยังเครื่องพิมพ์</span><span class="sxs-lookup"><span data-stu-id="6127c-120">Set the **Enabled** option to **Yes** to send a generated document to a printer.</span></span>
2. <span data-ttu-id="6127c-121">ในฟิลด์ **ชื่อเครื่องพิมพ์** ให้เลือกเครื่องพิมพ์บนเครือข่ายที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="6127c-121">In the **Printer name** field, select the required network printer.</span></span>
3. <span data-ttu-id="6127c-122">ตั้งค่าตัวเลือก **บันทึกในที่เก็บถาวรของการพิมพ์หรือไม่** เป็น **ใช่** เพื่อจัดเก็บผลลัพธ์ที่สร้างไว้ในที่เก็บถาวรของการพิมพ์ เพื่อให้พร้อมใช้สำหรับการพิมพ์เพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="6127c-122">Set the **Save in print archive?** option to **Yes** to store the generated output in the print archive, so that it's available for further printing.</span></span> <span data-ttu-id="6127c-123">หากต้องการเข้าถึงผลลัพธ์ที่เก็บเก็บถาวร ให้ไปที่ **การจัดการองค์กร** \> **การสอบถามและรายงาน** \> **ที่เก็บถาวรของรายงาน**</span><span class="sxs-lookup"><span data-stu-id="6127c-123">To access archived output later, go to **Organization administration** \> **Inquiries and reports** \> **Report archive**.</span></span>

<span data-ttu-id="6127c-124">[![การใช้ปลายทางเครื่องพิมพ์](./media/ER_Destinations-PrinterDestination.png)](./media/ER_Destinations-PrinterDestination.png)</span><span class="sxs-lookup"><span data-stu-id="6127c-124">[![Using the Printer destination](./media/ER_Destinations-PrinterDestination.png)](./media/ER_Destinations-PrinterDestination.png)</span></span>

> [!NOTE]
> <span data-ttu-id="6127c-125">ไม่จำเป็นต้องเปิดใช้งานตัวเลือก **แปลงเป็น PDF** เมื่อคุณตั้งค่าคอนฟิกปลายทาง **เครื่องพิมพ์**</span><span class="sxs-lookup"><span data-stu-id="6127c-125">The **Convert to PDF** option doesn't have to be turned on when you configure the **Printer** destination.</span></span> <span data-ttu-id="6127c-126">การแปลง PDF สำหรับวัตถุประสงค์ในการพิมพ์จะเกิดขึ้นแม้ว่าตัวเลือกนี้จะถูกปิดใช้งาน</span><span class="sxs-lookup"><span data-stu-id="6127c-126">The PDF conversion for printing purposes will occur even if the option is turned off.</span></span>

<span data-ttu-id="6127c-127">เมื่อต้องการใช้ [การจัดวางหน้า](electronic-reporting-destinations.md#SelectPdfPageOrientation) เฉพาะ เมื่อคุณพิมพ์เอกสารขาออกในรูปแบบ Excel คุณต้องเปิดใช้งานตัวเลือก **แปลงเป็น PDF**</span><span class="sxs-lookup"><span data-stu-id="6127c-127">To use a specific [page orientation](electronic-reporting-destinations.md#SelectPdfPageOrientation) when you print an outbound document in Excel format, you must turn on the **Convert to PDF** option.</span></span> <span data-ttu-id="6127c-128">เมื่อคุณตั้งค่าตัวเลือก **แปลงเป็น PDF** เป็น **ใช่** ฟิลด์ **การจัดวางหน้า** จะพร้อมใช้งาน</span><span class="sxs-lookup"><span data-stu-id="6127c-128">When you set the **Convert to PDF** option to **Yes**, the **Page orientation** field becomes available.</span></span> <span data-ttu-id="6127c-129">ในฟิลด์ **การจัดวางหน้า** คุณสามารถเลือกการจัดวางหน้าได้</span><span class="sxs-lookup"><span data-stu-id="6127c-129">In the **Page orientation** field, you can select a page orientation.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="6127c-130">ทรัพยากรเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="6127c-130">Additional resources</span></span>

- [<span data-ttu-id="6127c-131">ภาพรวมการรายงานทางอิเล็กทรอนิกส์ (ER)</span><span class="sxs-lookup"><span data-stu-id="6127c-131">Electronic reporting (ER) overview</span></span>](general-electronic-reporting.md)
- [<span data-ttu-id="6127c-132">ปลายทางการรายงานทางอิเล็กทรอนิกส์ (ER)</span><span class="sxs-lookup"><span data-stu-id="6127c-132">Electronic reporting (ER) destinations</span></span>](electronic-reporting-destinations.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
