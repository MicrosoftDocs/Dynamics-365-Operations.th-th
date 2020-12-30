---
title: ชนิดของปลายทาง ER ที่เก็บถาวร
description: หัวข้อนี้จะให้ข้อมูลเกี่ยวกับวิธีการตั้งค่าคอนฟิกปลายทางของที่เก็บถาวรสำหรับแต่ละโฟลเดอร์หรือส่วนประกอบของไฟล์ของรูปแบบการรายงานทางอิเล็กทรอนิกส์ (ER) ที่มีการตั้งค่าคอนฟิกเพื่อสร้างเอกสารขาออก
author: NickSelin
manager: AnnBe
ms.date: 11/30/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: DocuType, ERSolutionTable, ERFormatDestinationTable
audience: Application User
ms.reviewer: kfend
ms.custom: 97423
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-05-31
ms.dyn365.ops.version: AX 7.0.1
ms.openlocfilehash: 3dee7ec614ec1372feaa1150f5e4ebb14c32f60e
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 12/05/2020
ms.locfileid: "4679689"
---
# <a name="archive-er-destination-type"></a><span data-ttu-id="e0314-103">ชนิดของปลายทาง ER ที่เก็บถาวร</span><span class="sxs-lookup"><span data-stu-id="e0314-103">Archive ER destination type</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="e0314-104">คุณสามารถตั้งค่าคอนฟิกปลายทางที่เก็บถาวรของไฟล์สำหรับแต่ละ **โฟลเดอร์** หรือส่วนประกอบของ **ไฟล์** ของรูปแบบการรายงานทางอิเล็กทรอนิกส์ (ER) ที่มีการตั้งค่าคอนฟิกเพื่อสร้างเอกสารขาออก</span><span class="sxs-lookup"><span data-stu-id="e0314-104">You can configure an archive destination for each **Folder** or **File** component of an Electronic reporting (ER) format that is configured to generate outbound documents.</span></span> <span data-ttu-id="e0314-105">เอกสารที่สร้างขึ้นจะถูกจัดเก็บเป็นเอกสารแนบของเรกคอร์ดของรายการงาน ER โดยยึดตามการตั้งค่าปลายทาง</span><span class="sxs-lookup"><span data-stu-id="e0314-105">Based on the destination setting, a generated document is stored as an attachment of a record of the ER jobs list.</span></span> <span data-ttu-id="e0314-106">หากต้องการดูผลลัพธ์ ไปที่ **การจัดการองค์กร** \> **การรายงานทางอิเล็กทรอนิกส์** \> **งานของการรายงานทางอิเล็กทรอนิกส์**</span><span class="sxs-lookup"><span data-stu-id="e0314-106">To view the results, go to **Organization administration** \> **Electronic reporting** \> **Electronic reporting jobs**.</span></span>

<span data-ttu-id="e0314-107">คุณสามารถใช้ตัวเลือกนี้เพื่อส่งเอกสารที่สร้างขึ้นไปยังโฟลเดอร์ Microsoft SharePoint หรือที่จัดเก็บ Microsoft Azure</span><span class="sxs-lookup"><span data-stu-id="e0314-107">You can use this option to send the generated document to a Microsoft SharePoint folder or Microsoft Azure Storage.</span></span> <span data-ttu-id="e0314-108">ตั้งค่า **เปิดใช้งานอยู่** เป็น **ใช่** เพื่อส่งเอาท์พุทไปยังปลายทางที่กำหนดโดยชนิดเอกสารที่เลือก</span><span class="sxs-lookup"><span data-stu-id="e0314-108">Set **Enabled** to **Yes** to send output to a destination that is defined by the selected document type.</span></span> <span data-ttu-id="e0314-109">สามารถเลือกได้เฉพาะชนิดเอกสารที่กลุ่มที่ถูกตั้งค่าเป็น **ไฟล์**</span><span class="sxs-lookup"><span data-stu-id="e0314-109">Only document types where the group is set to **File** are available for selection.</span></span> <span data-ttu-id="e0314-110">คุณกำหนด [ชนิด](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/organization-administration/configure-document-management#configure-document-types) เอกสารได้ที่ **การจัดการองค์กร** \> **การจัดการเอกสาร** \> **ชนิดเอกสาร**</span><span class="sxs-lookup"><span data-stu-id="e0314-110">You define document [types](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/organization-administration/configure-document-management#configure-document-types) at **Organization administration** \> **Document management** \> **Document types**.</span></span> <span data-ttu-id="e0314-111">การตั้งค่าคอนฟิกปลายทาง ER เหมือนกับการตั้งค่าคอนฟิกระบบการจัดการเอกสาร</span><span class="sxs-lookup"><span data-stu-id="e0314-111">The configuration for ER destinations is the same as the configuration for the document management system.</span></span>

<span data-ttu-id="e0314-112">[![หน้าชนิดเอกสาร](./media/ER_Destinations-SharePointDocuType.png)](./media/ER_Destinations-SharePointDocuType.png)</span><span class="sxs-lookup"><span data-stu-id="e0314-112">[![Document types page](./media/ER_Destinations-SharePointDocuType.png)](./media/ER_Destinations-SharePointDocuType.png)</span></span>

<span data-ttu-id="e0314-113">ตำแหน่งที่ตั้งเป็นตัวกำหนดตำแหน่งที่บันทึกไฟล์</span><span class="sxs-lookup"><span data-stu-id="e0314-113">The location determines where the file is saved.</span></span> <span data-ttu-id="e0314-114">หลังจากที่เปิดใช้งานปลายทาง **ที่เก็บถาวร** แล้ว สามารถบันทึกผลลัพธ์ในที่เก็บถาวรของงาน</span><span class="sxs-lookup"><span data-stu-id="e0314-114">After the **Archive** destination is enabled, the results can be saved in the Job archive.</span></span> <span data-ttu-id="e0314-115">คุณสามารถดูผลลัพธ์ได้ที่ **การจัดการองค์กร** \> **การรายงานทางอิเล็กทรอนิกส์** \> **ที่เก็บถาวรงานของการรายงานทางอิเล็กทรอนิกส์**</span><span class="sxs-lookup"><span data-stu-id="e0314-115">You can view the results at **Organization administration** \> **Electronic reporting** \> **Electronic reporting archived jobs**.</span></span>

> [!NOTE]
> <span data-ttu-id="e0314-116">เลือกชนิดเอกสารสำหรับที่เก็บงานถาวรโดยนำทางไปยัง **การจัดการองค์กร** \> **พื้นที่ทำงาน** \> **การรายงานทางอิเล็กทรอนิกส์** \> **พารามิเตอร์การรายงานทางอิเล็กทรอนิกส์**</span><span class="sxs-lookup"><span data-stu-id="e0314-116">Select a document type for the Job archive by navigating to **Organization administration** \> **Workspaces** \> **Electronic reporting** \> **Electronic reporting parameters**.</span></span> <span data-ttu-id="e0314-117">สำหรับข้อมูลเพิ่มเติม โปรดดู [ตั้งค่าคอนฟิกกรอบงานของการรายงานทางอิเล็กทรอนิกส์ (ER)](electronic-reporting-er-configure-parameters.md#prerequisites-for-er-setup)</span><span class="sxs-lookup"><span data-stu-id="e0314-117">For more information, see [Configure the Electronic reporting (ER) framework](electronic-reporting-er-configure-parameters.md#prerequisites-for-er-setup).</span></span>

## <a name="sharepoint"></a><span data-ttu-id="e0314-118">SharePoint</span><span class="sxs-lookup"><span data-stu-id="e0314-118">SharePoint</span></span>

<span data-ttu-id="e0314-119">คุณสามารถบันทึกไฟล์ในโฟลเดอร์ SharePoint ที่กำหนด</span><span class="sxs-lookup"><span data-stu-id="e0314-119">You can save a file in a designated SharePoint folder.</span></span> <span data-ttu-id="e0314-120">ในการกำหนดเซิร์ฟเวอร์ SharePoint เริ่มต้น ให้ไปที่ **การจัดการองค์กร** \> **การจัดการเอกสาร** \> **พารามิเตอร์การจัดการเอกสาร**</span><span class="sxs-lookup"><span data-stu-id="e0314-120">To define the default SharePoint server, go to **Organization administration** \> **Document management** \> **Document management parameters**.</span></span> <span data-ttu-id="e0314-121">บนแท็บ **SharePoint** ให้ตั้งค่าคอนฟิกโฟลเดอร์ SharePoint</span><span class="sxs-lookup"><span data-stu-id="e0314-121">On the **SharePoint** tab, configure the SharePoint folder.</span></span> <span data-ttu-id="e0314-122">จากนั้นคุณสามารถเลือกเป็นโฟลเดอร์ที่จะมีการบันทึกผลลัพธ์ของ ER</span><span class="sxs-lookup"><span data-stu-id="e0314-122">Then, you can select it as the folder where the ER output will be saved.</span></span> <span data-ttu-id="e0314-123">ที่ตั้งของ **SharePoint** ต้องถูกเลือกในชนิดเอกสารนี้</span><span class="sxs-lookup"><span data-stu-id="e0314-123">The **SharePoint** location must be selected in this document type.</span></span>

<span data-ttu-id="e0314-124">[![การเลือกโฟลเดอร์ SharePoint](./media/ER_Destinations-SharePointDocuTypeLocation.png)](./media/ER_Destinations-SharePointDocuTypeLocation.png)</span><span class="sxs-lookup"><span data-stu-id="e0314-124">[![Selecting a SharePoint folder](./media/ER_Destinations-SharePointDocuTypeLocation.png)](./media/ER_Destinations-SharePointDocuTypeLocation.png)</span></span>

## <a name="azure-storage"></a><span data-ttu-id="e0314-125">ที่เก็บข้อมูล Azure</span><span class="sxs-lookup"><span data-stu-id="e0314-125">Azure Storage</span></span>

<span data-ttu-id="e0314-126">เมื่อตำแหน่งที่ตั้งชนิดเอกสารถูกตั้งค่าเป็น **ที่เก็บข้อมูล Azure** คุณสามารถบันทึกไฟล์ไปยังที่เก็บข้อมูล Azure ได้</span><span class="sxs-lookup"><span data-stu-id="e0314-126">When the document type location is set to **Azure storage**, you can save a file to Azure Storage.</span></span>

> [!NOTE] 
> <span data-ttu-id="e0314-127">กรอบงาน ER จัดเก็บไฟล์ใน Azure Blob จัดเก็บไฟล์อย่างถาวรซึ่งแตกต่างจากกรอบงานการจัดการข้อมูลที่ใช้นโยบายการเก็บข้อมูลแบบเจ็ดวันสำหรับเอกสารที่ต้องมีการประมวลผล</span><span class="sxs-lookup"><span data-stu-id="e0314-127">The ER framework permanently stores files in Azure Blob storage unlike the Data management framework that applies the seven-day retention policy for documents that must be processed.</span></span> <span data-ttu-id="e0314-128">สำหรับข้อมูลเพิ่มเติม ให้ดูที่ [API สำหรับการรับสถานะข้อความ](../data-entities/recurring-integrations.md#api-for-getting-message-status) และ [API การตรวจสอบสถานะ](../data-entities/data-management-api.md#status-check-api)</span><span class="sxs-lookup"><span data-stu-id="e0314-128">For more information, see [API for getting message status](../data-entities/recurring-integrations.md#api-for-getting-message-status) and [Status check API](../data-entities/data-management-api.md#status-check-api).</span></span> <span data-ttu-id="e0314-129">ไฟล์ที่เกี่ยวข้องกับ ER จะถูกจัดเก็บไว้ในที่จัดเก็บ Blob Azure เป็นเอกสารแนบของเรกคอร์ดตารางของโปรแกรมประยุกต์ตราบใดที่จำเป็น</span><span class="sxs-lookup"><span data-stu-id="e0314-129">The ER-related files will be stored in Azure Blob storage as attachments of application table records as long as necessary.</span></span> <span data-ttu-id="e0314-130">ไฟล์เดียวจะถูกลบออกจากพื้นที่จัดเก็บ Blob Azure พร้อมกับเรกคอร์ดตารางของโปรแกรมประยุกต์ที่ไฟล์นี้แนบอยู่</span><span class="sxs-lookup"><span data-stu-id="e0314-130">A single file will be deleted from Azure Blob storage along with the application table record that this file was attached to.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="e0314-131">ทรัพยากรเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="e0314-131">Additional resources</span></span>

- [<span data-ttu-id="e0314-132">ภาพรวมการรายงานทางอิเล็กทรอนิกส์ (ER)</span><span class="sxs-lookup"><span data-stu-id="e0314-132">Electronic reporting (ER) overview</span></span>](general-electronic-reporting.md)
- [<span data-ttu-id="e0314-133">ปลายทางการรายงานทางอิเล็กทรอนิกส์ (ER)</span><span class="sxs-lookup"><span data-stu-id="e0314-133">Electronic reporting (ER) destinations</span></span>](electronic-reporting-destinations.md)
- [<span data-ttu-id="e0314-134">ตั้งค่าคอนฟิกการจัดการเอกสาร</span><span class="sxs-lookup"><span data-stu-id="e0314-134">Configure document management</span></span>](../../fin-ops/organization-administration/configure-document-management.md)
