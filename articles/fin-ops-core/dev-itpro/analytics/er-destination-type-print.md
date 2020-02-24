---
title: ชนิดของปลายทาง ER เครื่องพิมพ์
description: หัวข้อนี้จะอธิบายวิธีการตั้งค่าคอนฟิกปลายทางเครื่องพิมพ์สำหรับแต่ละโฟลเดอร์หรือส่วนประกอบของไฟล์ของรูปแบบการรายงานทางอิเล็กทรอนิกส์ (ER) ที่มีการตั้งค่าคอนฟิกเพื่อสร้างเอกสารขาออก ทั้งในรูปแบบ PDF หรือ Microsoft Office (Excel\Word)
author: NickSelin
manager: AnnBe
ms.date: 01/16/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: DocuType, ERSolutionTable, ERFormatDestinationTable
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 97423
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2020-04-01
ms.dyn365.ops.version: AX 10.0.9
ms.openlocfilehash: 58e067baa130458e3a8e788d978604f208140a03
ms.sourcegitcommit: 54baab2a04e5c534fc2d1fd67b67e23a152d4e57
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 02/04/2020
ms.locfileid: "3020027"
---
# <a name="PrinterDestinationType"></a><span data-ttu-id="4775d-103">ปลายทางเครื่องพิมพ์</span><span class="sxs-lookup"><span data-stu-id="4775d-103">Printer destination</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="4775d-104">คุณสามารถส่งเอกสารที่สร้างขึ้นโดยตรงไปยังเครื่องพิมพ์บนเครือข่ายสำหรับการพิมพ์โดยตรง</span><span class="sxs-lookup"><span data-stu-id="4775d-104">You can send a generated document directly to a network printer for direct printing.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="4775d-105">ข้อกำหนดเบื้องต้น</span><span class="sxs-lookup"><span data-stu-id="4775d-105">Prerequisites</span></span>

<span data-ttu-id="4775d-106">ก่อนที่คุณจะเริ่มต้น คุณต้องติดตั้งและตั้งค่าคอนฟิกตัวแทนการกำหนดเส้นทางเอกสาร แล้วลงทะเบียนเครื่องพิมพ์บนเครือข่าย</span><span class="sxs-lookup"><span data-stu-id="4775d-106">Before you begin, you must install and configure the Document Routing Agent, and then register the network printers.</span></span> <span data-ttu-id="4775d-107">สำหรับข้อมูลเพิ่มเติม ดูที่ [ติดตั้งเอเจนต์การกำหนดเส้นทางเอกสารเพื่อเปิดใช้งานการพิมพ์ผ่านเครือข่าย](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/analytics/install-document-routing-agent)</span><span class="sxs-lookup"><span data-stu-id="4775d-107">For more information, see [Install the Document Routing Agent to enable network printing](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/analytics/install-document-routing-agent).</span></span>

## <a name="make-the-printer-destination-available"></a><span data-ttu-id="4775d-108">ทำให้การกำหนดปลายทางเครื่องพิมพ์พร้อมใช้งาน</span><span class="sxs-lookup"><span data-stu-id="4775d-108">Make the Printer destination available</span></span>

<span data-ttu-id="4775d-109">เมื่อต้องการเปิดใช้งานปลายทาง **เครื่องพิมพ์** ในอินสแตนซ์ปัจจุบันของ Microsoft Dynamics 365 Finance ไปที่ **การจัดการคุณลักษณะ** และเปิดใช้งานคุณลักษณะต่อไปนี้ในใบสั่งนี้:</span><span class="sxs-lookup"><span data-stu-id="4775d-109">To make the **Printer** destination available in the current instance of Microsoft Dynamics 365 Finance, go to the **Feature management** workspace, and turn on the following features, in this order:</span></span>

1. <span data-ttu-id="4775d-110">แปลงเอกสารขาออกของการรายงานทางอิเล็กทรอนิกส์จากรูปแบบ Microsoft Office เป็น PDF</span><span class="sxs-lookup"><span data-stu-id="4775d-110">Convert Electronic Reporting outbound documents from Microsoft Office formats to PDF</span></span>
2. <span data-ttu-id="4775d-111">เอเจนต์การกำหนดเส้นทางเอกสารเป็นปลายทางการรายงานทางอิเล็กทรอนิกส์สำหรับเอกสารขาออก</span><span class="sxs-lookup"><span data-stu-id="4775d-111">Document Routing Agent as Electronic Reporting destination for outbound documents</span></span>

<span data-ttu-id="4775d-112">[![การเปิดใช้งานคุณลักษณะปลายทางเครื่องพิมพ์ ER ในการจัดการคุณลักษณะ](./media/ER_Destinations-EnablePrinterDestinationFeature.png)](./media/ER_Destinations-EnablePrinterDestinationFeature.png)</span><span class="sxs-lookup"><span data-stu-id="4775d-112">[![Turning on the ER printer destination feature in Feature management](./media/ER_Destinations-EnablePrinterDestinationFeature.png)](./media/ER_Destinations-EnablePrinterDestinationFeature.png)</span></span>

### <a name="applicability"></a><span data-ttu-id="4775d-113">การมีผลบังคับใช้</span><span class="sxs-lookup"><span data-stu-id="4775d-113">Applicability</span></span>

<span data-ttu-id="4775d-114">ปลายทาง **เครื่องพิมพ์** สามารถตั้งค่าคอนฟิกสำหรับส่วนประกอบของไฟล์ที่ใช้ในการสร้างผลลัพธ์ในรูปแบบไฟล์ PDF ที่พิมพ์ได้ (ตัวผสาน PDF หรือองค์ประกอบไฟล์ PDF) หรือ Microsoft Office Excel /Word (ไฟล์ Excel) เท่านั้น</span><span class="sxs-lookup"><span data-stu-id="4775d-114">The **Printer** destination can be configured only for file components that are used to generate output in either printable PDF format (PDF Merger or PDF file format elements) or Microsoft Office Excel/Word format (Excel file).</span></span> <span data-ttu-id="4775d-115">เมื่อมีการสร้างผลลัพธ์ในรูปแบบ PDF จะมีการส่งออกไปยังเครื่องพิมพ์</span><span class="sxs-lookup"><span data-stu-id="4775d-115">When output is generated in PDF format, it's sent to a printer.</span></span> <span data-ttu-id="4775d-116">เมื่อมีการสร้างผลลัพธ์ในรูปแบบ Microsoft Office โดยอัตโนมัติ จะมีการแปลงเป็นรูปแบบ PDF แล้วส่งไปยังเครื่องพิมพ์</span><span class="sxs-lookup"><span data-stu-id="4775d-116">When output is generated in Microsoft Office format, it's automatically converted to PDF format and then sent to a printer.</span></span>

### <a name="limitations"></a><span data-ttu-id="4775d-117">การจำกัด</span><span class="sxs-lookup"><span data-stu-id="4775d-117">Limitations</span></span>

<span data-ttu-id="4775d-118">คุณลักษณะนี้เป็นคุณลักษณะของการแสดงตัวอย่างและอยู่ภายใต้เงื่อนไขการใช้งานที่อธิบายใน [ข้อกำหนดการใช้งานเพิ่มเติมสำหรับการแสดงตัวอย่าง Microsoft Dynamics 365](https://go.microsoft.com/fwlink/?linkid=2105274)</span><span class="sxs-lookup"><span data-stu-id="4775d-118">This feature is a preview feature and is subject to the terms of use that are described in [Supplemental Terms of Use for Microsoft Dynamics 365 Previews](https://go.microsoft.com/fwlink/?linkid=2105274).</span></span>

<span data-ttu-id="4775d-119">ปลายทาง **เครื่องพิมพ์** ใช้ในการปรับใช้สำหรับ cloud เท่านั้น</span><span class="sxs-lookup"><span data-stu-id="4775d-119">The **Printer** destination is implemented only for cloud deployments.</span></span>

### <a name="use-the-printer-destination"></a><span data-ttu-id="4775d-120">ใช้ปลายทางเครื่องพิมพ์</span><span class="sxs-lookup"><span data-stu-id="4775d-120">Use the Printer destination</span></span>

1. <span data-ttu-id="4775d-121">ตั้งค่าตัวเลือก **เปิดใช้งาน** เป็น **ใช่** เพื่อส่งเอกสารที่สร้างขึ้นไปยังเครื่องพิมพ์</span><span class="sxs-lookup"><span data-stu-id="4775d-121">Set the **Enabled** option to **Yes** to send a generated document to a printer.</span></span>
2. <span data-ttu-id="4775d-122">ในฟิลด์ **ชื่อเครื่องพิมพ์** ให้เลือกเครื่องพิมพ์บนเครือข่ายที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="4775d-122">In the **Printer name** field, select the required network printer.</span></span>
3. <span data-ttu-id="4775d-123">ตั้งค่าตัวเลือก **บันทึกในที่เก็บถาวรของการพิมพ์หรือไม่** เป็น **ใช่** เพื่อจัดเก็บผลลัพธ์ที่สร้างไว้ในที่เก็บถาวรของการพิมพ์ เพื่อให้พร้อมใช้สำหรับการพิมพ์เพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="4775d-123">Set the **Save in print archive?** option to **Yes** to store the generated output in the print archive, so that it's available for further printing.</span></span> <span data-ttu-id="4775d-124">หากต้องการเข้าถึงผลลัพธ์ที่เก็บเก็บถาวร ให้ไปที่ **การจัดการองค์กร** \> **การสอบถามและรายงาน** \> **ที่เก็บถาวรของรายงาน**</span><span class="sxs-lookup"><span data-stu-id="4775d-124">To access archived output later, go to **Organization administration** \> **Inquiries and reports** \> **Report archive**.</span></span>

<span data-ttu-id="4775d-125">[![การใช้ปลายทางเครื่องพิมพ์](./media/ER_Destinations-PrinterDestination.png)](./media/ER_Destinations-PrinterDestination.png)</span><span class="sxs-lookup"><span data-stu-id="4775d-125">[![Using the Printer destination](./media/ER_Destinations-PrinterDestination.png)](./media/ER_Destinations-PrinterDestination.png)</span></span>

> [!NOTE]
> <span data-ttu-id="4775d-126">ไม่จำเป็นต้องเปิดใช้งานตัวเลือก **แปลงเป็น PDF** เมื่อคุณตั้งค่าคอนฟิกปลายทาง **เครื่องพิมพ์**</span><span class="sxs-lookup"><span data-stu-id="4775d-126">The **Convert to PDF** option doesn't have to be turned on when you configure the **Printer** destination.</span></span> <span data-ttu-id="4775d-127">การแปลง PDF สำหรับวัตถุประสงค์ในการพิมพ์จะเกิดขึ้นแม้ว่าตัวเลือกนี้จะถูกปิดใช้งาน</span><span class="sxs-lookup"><span data-stu-id="4775d-127">The PDF conversion for printing purposes will occur even if the option is turned off.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="4775d-128">แหล่งข้อมูลเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="4775d-128">Additional resources</span></span>

- [<span data-ttu-id="4775d-129">ภาพรวมการรายงานทางอิเล็กทรอนิกส์ (ER)</span><span class="sxs-lookup"><span data-stu-id="4775d-129">Electronic reporting (ER) overview</span></span>](general-electronic-reporting.md)
- [<span data-ttu-id="4775d-130">ปลายทางการรายงานทางอิเล็กทรอนิกส์ (ER)</span><span class="sxs-lookup"><span data-stu-id="4775d-130">Electronic reporting (ER) destinations</span></span>](electronic-reporting-destinations.md)
