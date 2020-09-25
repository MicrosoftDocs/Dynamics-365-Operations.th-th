---
title: ชนิดของปลายทาง ER ที่เก็บถาวร
description: หัวข้อนี้จะให้ข้อมูลเกี่ยวกับวิธีการตั้งค่าคอนฟิกปลายทางของที่เก็บถาวรสำหรับแต่ละโฟลเดอร์หรือส่วนประกอบของไฟล์ของรูปแบบการรายงานทางอิเล็กทรอนิกส์ (ER) ที่มีการตั้งค่าคอนฟิกเพื่อสร้างเอกสารขาออก
author: NickSelin
manager: AnnBe
ms.date: 01/27/2020
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
ms.search.validFrom: 2016-05-31
ms.dyn365.ops.version: AX 7.0.1
ms.openlocfilehash: 8797a68507a5116c6adbf1f2d805838fa507958c
ms.sourcegitcommit: 445f6d8d0df9f2cbac97e85e3ec3ed8b7d18d3a2
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 09/01/2020
ms.locfileid: "3745596"
---
# <a name="archive-destination"></a><span data-ttu-id="4d9cf-103">ปลายทางที่เก็บถาวร</span><span class="sxs-lookup"><span data-stu-id="4d9cf-103">Archive destination</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="4d9cf-104">คุณสามารถตั้งค่าคอนฟิกปลายทางที่เก็บถาวรของไฟล์สำหรับแต่ละโฟลเดอร์หรือส่วนประกอบของไฟล์ของรูปแบบการรายงานทางอิเล็กทรอนิกส์ (ER) ที่มีการตั้งค่าคอนฟิกเพื่อสร้างเอกสารขาออก</span><span class="sxs-lookup"><span data-stu-id="4d9cf-104">You can configure an archive destination for each FOLDER or FILE component of an Electronic reporting (ER) format that is configured to generate outbound documents.</span></span> <span data-ttu-id="4d9cf-105">เอกสารที่สร้างขึ้นจะถูกจัดเก็บเป็นเอกสารแนบของเรกคอร์ดของรายการงาน ER โดยยึดตามการตั้งค่าปลายทาง</span><span class="sxs-lookup"><span data-stu-id="4d9cf-105">Based on the destination setting, a generated document is stored as an attachment of a record of the ER jobs list.</span></span>

<span data-ttu-id="4d9cf-106">คุณสามารถใช้ตัวเลือกนี้เพื่อส่งเอกสารที่สร้างขึ้นไปยังโฟลเดอร์ Microsoft SharePoint หรือที่จัดเก็บ Microsoft Azure</span><span class="sxs-lookup"><span data-stu-id="4d9cf-106">You can use this option to send the generated document to a Microsoft SharePoint folder or Microsoft Azure Storage.</span></span> <span data-ttu-id="4d9cf-107">ตั้งค่า **เปิดใช้งานอยู่** เป็น **ใช่**เพื่อส่งเอาท์พุทไปยังปลายทางที่กำหนดโดยชนิดเอกสารที่เลือก</span><span class="sxs-lookup"><span data-stu-id="4d9cf-107">Set **Enabled** to **Yes** to send output to a destination that is defined by the selected document type.</span></span> <span data-ttu-id="4d9cf-108">สามารถเลือกได้เฉพาะชนิดเอกสารที่กลุ่มที่ถูกตั้งค่าเป็น **ไฟล์**</span><span class="sxs-lookup"><span data-stu-id="4d9cf-108">Only document types where the group is set to **File** are available for selection.</span></span> <span data-ttu-id="4d9cf-109">คุณกำหนด [ชนิด](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/organization-administration/configure-document-management#configure-document-types) เอกสารได้ที่ **การจัดการองค์กร** \> **การจัดการเอกสาร** \> **ชนิดเอกสาร**</span><span class="sxs-lookup"><span data-stu-id="4d9cf-109">You define document [types](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/organization-administration/configure-document-management#configure-document-types) at **Organization administration** \> **Document management** \> **Document types**.</span></span> <span data-ttu-id="4d9cf-110">การตั้งค่าคอนฟิกปลายทาง ER เหมือนกับการตั้งค่าคอนฟิกระบบการจัดการเอกสาร</span><span class="sxs-lookup"><span data-stu-id="4d9cf-110">The configuration for ER destinations is the same as the configuration for the document management system.</span></span>

<span data-ttu-id="4d9cf-111">[![หน้าชนิดเอกสาร](./media/ER_Destinations-SharePointDocuType.png)](./media/ER_Destinations-SharePointDocuType.png)</span><span class="sxs-lookup"><span data-stu-id="4d9cf-111">[![Document types page](./media/ER_Destinations-SharePointDocuType.png)](./media/ER_Destinations-SharePointDocuType.png)</span></span>

<span data-ttu-id="4d9cf-112">ตำแหน่งที่ตั้งเป็นตัวกำหนดตำแหน่งที่บันทึกไฟล์</span><span class="sxs-lookup"><span data-stu-id="4d9cf-112">The location determines where the file is saved.</span></span> <span data-ttu-id="4d9cf-113">หลังจากที่เปิดใช้งานปลายทาง **ที่เก็บถาวร** แล้ว สามารถบันทึกผลลัพธ์ในที่เก็บถาวรของงาน</span><span class="sxs-lookup"><span data-stu-id="4d9cf-113">After the **Archive** destination is enabled, the results can be saved in the Job archive.</span></span> <span data-ttu-id="4d9cf-114">คุณสามารถดูผลลัพธ์ได้ที่ **การจัดการองค์กร** \> **การรายงานทางอิเล็กทรอนิกส์** \> **ที่เก็บถาวรงานของการรายงานทางอิเล็กทรอนิกส์**</span><span class="sxs-lookup"><span data-stu-id="4d9cf-114">You can view the results at **Organization administration** \> **Electronic reporting** \> **Electronic reporting archived jobs**.</span></span>

> [!NOTE]
> <span data-ttu-id="4d9cf-115">เลือกชนิดเอกสารสำหรับที่เก็บงานถาวรโดยนำทางไปยัง **การจัดการองค์กร** \> **พื้นที่ทำงาน** \> **การรายงานทางอิเล็กทรอนิกส์** \> **พารามิเตอร์การรายงานทางอิเล็กทรอนิกส์**</span><span class="sxs-lookup"><span data-stu-id="4d9cf-115">Select a document type for the Job archive by navigating to **Organization administration** \> **Workspaces** \> **Electronic reporting** \> **Electronic reporting parameters**.</span></span> <span data-ttu-id="4d9cf-116">สำหรับข้อมูลเพิ่มเติม โปรดดู [ตั้งค่าคอนฟิกกรอบงานของการรายงานทางอิเล็กทรอนิกส์ (ER)](electronic-reporting-er-configure-parameters.md#prerequisites-for-er-setup)</span><span class="sxs-lookup"><span data-stu-id="4d9cf-116">For more information, [Configure the Electronic reporting (ER) framework](electronic-reporting-er-configure-parameters.md#prerequisites-for-er-setup).</span></span>

## <a name="sharepoint"></a><span data-ttu-id="4d9cf-117">SharePoint</span><span class="sxs-lookup"><span data-stu-id="4d9cf-117">SharePoint</span></span>

<span data-ttu-id="4d9cf-118">คุณสามารถบันทึกไฟล์ในโฟลเดอร์ SharePoint ที่กำหนด</span><span class="sxs-lookup"><span data-stu-id="4d9cf-118">You can save a file in a designated SharePoint folder.</span></span> <span data-ttu-id="4d9cf-119">ในการกำหนดเซิร์ฟเวอร์ SharePoint เริ่มต้น ให้ไปที่ **การจัดการองค์กร** \> **การจัดการเอกสาร** \> **พารามิเตอร์การจัดการเอกสาร**</span><span class="sxs-lookup"><span data-stu-id="4d9cf-119">To define the default SharePoint server, go to **Organization administration** \> **Document management** \> **Document management parameters**.</span></span> <span data-ttu-id="4d9cf-120">บนแท็บ **SharePoint** ให้ตั้งค่าคอนฟิกโฟลเดอร์ SharePoint</span><span class="sxs-lookup"><span data-stu-id="4d9cf-120">On the **SharePoint** tab, configure the SharePoint folder.</span></span> <span data-ttu-id="4d9cf-121">จากนั้นคุณสามารถเลือกเป็นโฟลเดอร์ที่จะมีการบันทึกผลลัพธ์ของ ER</span><span class="sxs-lookup"><span data-stu-id="4d9cf-121">Then, you can select it as the folder where the ER output will be saved.</span></span> <span data-ttu-id="4d9cf-122">ที่ตั้งของ **SharePoint** ต้องถูกเลือกในชนิดเอกสารนี้</span><span class="sxs-lookup"><span data-stu-id="4d9cf-122">The **SharePoint** location must be selected in this document type.</span></span>

<span data-ttu-id="4d9cf-123">[![การเลือกโฟลเดอร์ SharePoint](./media/ER_Destinations-SharePointDocuTypeLocation.png)](./media/ER_Destinations-SharePointDocuTypeLocation.png)</span><span class="sxs-lookup"><span data-stu-id="4d9cf-123">[![Selecting a SharePoint folder](./media/ER_Destinations-SharePointDocuTypeLocation.png)](./media/ER_Destinations-SharePointDocuTypeLocation.png)</span></span>

## <a name="azure-storage"></a><span data-ttu-id="4d9cf-124">ที่เก็บข้อมูล Azure</span><span class="sxs-lookup"><span data-stu-id="4d9cf-124">Azure Storage</span></span>

<span data-ttu-id="4d9cf-125">เมื่อตำแหน่งที่ตั้งชนิดเอกสารถูกตั้งค่าเป็น **ที่เก็บข้อมูล Azure** คุณสามารถบันทึกไฟล์ไปยังที่เก็บข้อมูล Azure ได้</span><span class="sxs-lookup"><span data-stu-id="4d9cf-125">When the document type location is set to **Azure storage**, you can save a file to Azure Storage.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="4d9cf-126">แหล่งข้อมูลเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="4d9cf-126">Additional resources</span></span>

- [<span data-ttu-id="4d9cf-127">ภาพรวมการรายงานทางอิเล็กทรอนิกส์ (ER)</span><span class="sxs-lookup"><span data-stu-id="4d9cf-127">Electronic reporting (ER) overview</span></span>](general-electronic-reporting.md)
- [<span data-ttu-id="4d9cf-128">ปลายทางการรายงานทางอิเล็กทรอนิกส์ (ER)</span><span class="sxs-lookup"><span data-stu-id="4d9cf-128">Electronic reporting (ER) destinations</span></span>](electronic-reporting-destinations.md)
- [<span data-ttu-id="4d9cf-129">ตั้งค่าคอนฟิกการจัดการเอกสาร</span><span class="sxs-lookup"><span data-stu-id="4d9cf-129">Configure document management</span></span>](../../fin-ops/organization-administration/configure-document-management.md)
