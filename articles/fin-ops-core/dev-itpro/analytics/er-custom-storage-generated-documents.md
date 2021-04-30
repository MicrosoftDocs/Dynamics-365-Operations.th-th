---
title: ระบุตำแหน่งที่เก็บข้อมูลที่กำหนดเองสำหรับเอกสารที่สร้างขึ้น
description: หัวข้อนี้อธิบายวิธีการขยายรายการของสถานที่เก็บสำหรับเอกสารที่รูปแบบการรายงานทางอิเล็กทรอนิกส์ (ER) สร้างขึ้น
author: NickSelin
ms.date: 02/22/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2019-3-31
ms.dyn365.ops.version: 10
ms.openlocfilehash: ca50f030e67e517a227766f6a30d4bd4b345300b
ms.sourcegitcommit: 951393b05bf409333cb3c7ad977bcaa804aa801b
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 04/13/2021
ms.locfileid: "5894135"
---
# <a name="specify-a-custom-storage-location-for-generated-documents"></a><span data-ttu-id="fd445-103">ระบุตำแหน่งที่เก็บข้อมูลที่กำหนดเองสำหรับเอกสารที่สร้างขึ้น</span><span class="sxs-lookup"><span data-stu-id="fd445-103">Specify a custom storage location for generated documents</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="fd445-104">Application Programming Interface (API) ของกรอบงานการรายงานทางอิเล็กทรอนิกส์ (ER) ช่วยให้คุณสามารถขยายรายการของสถานที่เก็บสำหรับเอกสารที่รูปแบบ ER สร้าง</span><span class="sxs-lookup"><span data-stu-id="fd445-104">The application programming interface (API) of the Electronic reporting (ER) framework lets you extend the list of storage locations for documents that ER formats generate.</span></span> <span data-ttu-id="fd445-105">หัวข้อนี้มีภาพรวมของงานหลักที่คุณต้องดำเนินการเพิ่มสถานที่จัดเก็บที่กำหนดเองให้เสร็จสิ้น</span><span class="sxs-lookup"><span data-stu-id="fd445-105">This topic includes an overview of the main tasks that you must complete to add a custom storage location.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="fd445-106">ข้อกำหนดเบื้องต้น</span><span class="sxs-lookup"><span data-stu-id="fd445-106">Prerequisites</span></span>

<span data-ttu-id="fd445-107">คุณต้องปรับใช้โทโพโลยี ที่สนับสนุนการสร้างแบบต่อเนื่อง</span><span class="sxs-lookup"><span data-stu-id="fd445-107">You must deploy a topology that supports continuous build.</span></span> <span data-ttu-id="fd445-108">(สำหรับข้อมูลเพิ่มเติม ดู [ปรับใช้โทโพโลยีที่สนับสนุนการสร้างแบบต่อเนื่อง และการทำให้การทดสอบเป็นแบบอัตโนมัติ](/dynamics365/unified-operations/dev-itpro/perf-test/continuous-build-test-automation)) คุณต้องสามารถเข้าถึงโทโพโลยีนี้ สำหรับหนึ่งในบทบาทต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="fd445-108">(For more information, see [Deploy topologies that support continuous build and test automation](/dynamics365/unified-operations/dev-itpro/perf-test/continuous-build-test-automation).) You must have access to this topology for one of the following roles:</span></span>

- <span data-ttu-id="fd445-109">นักพัฒนาการรายงานทางอิเล็กทรอนิกส์</span><span class="sxs-lookup"><span data-stu-id="fd445-109">Electronic reporting developer</span></span>
- <span data-ttu-id="fd445-110">ที่ปรึกษาด้านการทำงานของการรายงานทางอิเล็กทรอนิกส์</span><span class="sxs-lookup"><span data-stu-id="fd445-110">Electronic reporting functional consultant</span></span>
- <span data-ttu-id="fd445-111">ผู้ดูแลระบบ</span><span class="sxs-lookup"><span data-stu-id="fd445-111">System administrator</span></span>

<span data-ttu-id="fd445-112">คุณต้องมีการเข้าถึงไปยังสภาพแวดล้อมการพัฒนาสำหรับโทโพโลยีนี้</span><span class="sxs-lookup"><span data-stu-id="fd445-112">You must also have access to the development environment for this topology.</span></span>

## <a name="create-or-import-an-er-format-configuration"></a><span data-ttu-id="fd445-113">สร้างหรือนำเข้าการตั้งค่าคอนฟิกรูปแบบ ER</span><span class="sxs-lookup"><span data-stu-id="fd445-113">Create or import an ER format configuration</span></span>

<span data-ttu-id="fd445-114">ในโทโพโลยีปัจจุบัน [สร้างรูปแบบ ER ใหม่](tasks/er-format-configuration-2016-11.md) ในการสร้างเอกสารที่คุณวางแผนที่จะเพิ่มตำแหน่งที่เก็บแบบกำหนดเอง</span><span class="sxs-lookup"><span data-stu-id="fd445-114">In the current topology, [create a new ER format](tasks/er-format-configuration-2016-11.md) to generate documents that you plan to add a custom storage location for.</span></span> <span data-ttu-id="fd445-115">อีกทางหนึ่งคือ [นำเข้ารูปแบบ ER ที่มีอยู่ลงในโทโพโลยีนี้](general-electronic-reporting-manage-configuration-lifecycle.md)</span><span class="sxs-lookup"><span data-stu-id="fd445-115">Alternatively, [import an existing ER format into this topology](general-electronic-reporting-manage-configuration-lifecycle.md).</span></span>

![หน้าตัวออกแบบรูปแบบ](media/er-extend-file-storages-format.png)

> [!IMPORTANT]
> <span data-ttu-id="fd445-117">รูปแบบ ER ที่คุณสร้างหรือนำเข้า ต้องประกอบด้วยอย่างน้อยหนึ่งในองค์ประกอบรูปแบบต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="fd445-117">The ER format that you create or import must contain at least one of the following format elements:</span></span>
>
> - <span data-ttu-id="fd445-118">ไฟล์</span><span class="sxs-lookup"><span data-stu-id="fd445-118">File</span></span>
> - <span data-ttu-id="fd445-119">โฟลเดอร์</span><span class="sxs-lookup"><span data-stu-id="fd445-119">Folder</span></span>
> - <span data-ttu-id="fd445-120">ตัวผสาน</span><span class="sxs-lookup"><span data-stu-id="fd445-120">Merger</span></span>
> - <span data-ttu-id="fd445-121">สิ่งที่แนบมา</span><span class="sxs-lookup"><span data-stu-id="fd445-121">Attachment</span></span>

## <a name="create-a-new-document-type"></a><span data-ttu-id="fd445-122">การสร้างชนิดเอกสารใหม่</span><span class="sxs-lookup"><span data-stu-id="fd445-122">Create a new document type</span></span>

<span data-ttu-id="fd445-123">เมื่อต้องการระบุวิธีการเวียนส่งเอกสารที่สร้างรูปแบบการ ER คุณต้องตั้งค่าคอนฟิก [ปลายทางการรายงานทางอิเล็กทรอนิกส์ (ER)](electronic-reporting-destinations.md)</span><span class="sxs-lookup"><span data-stu-id="fd445-123">To specify how documents that an ER format generates are routed, you must configure [Electronic reporting (ER) destinations](electronic-reporting-destinations.md).</span></span> <span data-ttu-id="fd445-124">ในปลายทาง ER แต่ละแห่งที่ถูกตั้งค่าคอนฟิกให้จัดเก็บเอกสารที่สร้างขึ้นเป็นไฟล์ คุณต้องระบุชนิดเอกสารของกรอบงานการจัดการเอกสาร</span><span class="sxs-lookup"><span data-stu-id="fd445-124">In each ER destination that is configured to store generated documents as files, you must specify a document type of the Document management framework.</span></span> <span data-ttu-id="fd445-125">ชนิดเอกสารต่างๆ สามารถใช้กับเอกสารกระบวนการผลิตที่รูปแบบ ER ที่แตกต่างกันสร้างขึ้น</span><span class="sxs-lookup"><span data-stu-id="fd445-125">Different document types can be used to route documents that different ER formats generate.</span></span>

1. <span data-ttu-id="fd445-126">เพิ่ม [ชนิดเอกสาร](../../fin-ops/organization-administration/configure-document-management.md) ใหม่ สำหรับรูปแบบ ER ที่คุณสร้าง หรือนำเข้ามาก่อนหน้านี้</span><span class="sxs-lookup"><span data-stu-id="fd445-126">Add a new [document type](../../fin-ops/organization-administration/configure-document-management.md) for the ER format that you created or imported earlier.</span></span> <span data-ttu-id="fd445-127">ในภาพประกอบต่อไปนี้ ชนิดเอกสารคือ **FileX**</span><span class="sxs-lookup"><span data-stu-id="fd445-127">In the illustration that follows, the document type is **FileX**.</span></span>
2. <span data-ttu-id="fd445-128">เพื่อแบ่งแยกชนิดเอกสารนี้จากชนิดเอกสารอื่นๆ รวมคำสำคัญเฉพาะในชื่อ</span><span class="sxs-lookup"><span data-stu-id="fd445-128">To differentiate this document type from other document types, include a specific keyword in its name.</span></span> <span data-ttu-id="fd445-129">ตัวอย่างเช่น ในภาพประกอบต่อไปนี้ ชื่อคือ **โฟลเดอร์ (LOCAL)**</span><span class="sxs-lookup"><span data-stu-id="fd445-129">For example, in the illustration that follows, the name is **(LOCAL) folder**.</span></span>
3. <span data-ttu-id="fd445-130">ในฟิลด์ **คลาส** ระบุ **แนบแฟ้ม**</span><span class="sxs-lookup"><span data-stu-id="fd445-130">In the **Class** field, specify **Attach file**.</span></span>
4. <span data-ttu-id="fd445-131">ในฟิลด์ **กลุ่ม** ระบุ **แฟ้ม**</span><span class="sxs-lookup"><span data-stu-id="fd445-131">In the **Group** field, specify **File**.</span></span>

![หน้าชนิดเอกสาร](media/er-extend-file-storages-document-type.png)

> [!NOTE]
> <span data-ttu-id="fd445-133">ชนิดเอกสารเป็นแบบเฉพาะบริษัท</span><span class="sxs-lookup"><span data-stu-id="fd445-133">Document types are company-specific.</span></span> <span data-ttu-id="fd445-134">ในการใช้รูปแบบ ER กับปลายทางที่ตั้งค่าคอนฟิกในหลายบริษัท คุณต้องตั้งค่าคอนฟิกชนิดเอกสารที่แยกต่างหากในแต่ละบริษัท</span><span class="sxs-lookup"><span data-stu-id="fd445-134">To use an ER format with a configured destination in multiple companies, you must configure a separate document type in each company.</span></span>

## <a name="review-source-code"></a><span data-ttu-id="fd445-135">ตรวจสอบโค้ดต้นฉบับ</span><span class="sxs-lookup"><span data-stu-id="fd445-135">Review source code</span></span>

<span data-ttu-id="fd445-136">ทบทวนรหัสของวิธีการ **insertFile()** ของคลาส **ERDocuManagement**</span><span class="sxs-lookup"><span data-stu-id="fd445-136">Review the code of the **insertFile()** method of the **ERDocuManagement** class.</span></span> <span data-ttu-id="fd445-137">สังเกตว่า เหตุการณ์ **AttachingFile()** ปรากฏขึ้น ขณะที่แนบไฟล์ที่สร้างไปยังเรกคอร์ด</span><span class="sxs-lookup"><span data-stu-id="fd445-137">Notice that the **AttachingFile()** event is raised while the generated file is attached to a record.</span></span>


```xpp
/// <summary>
/// Inserts file as attachment in Document Management.
/// </summary>
/// <param name = "_owner">A record as the attachment owner.</param>
/// <param name = "_stream">The file stream.</param>
/// <param name = "_filePath">The file path with name.</param>
/// <param name = "_attachmentName">The name of file attachment.</param>
/// <returns>The reference to inserted file.</returns>
[Hookable(false)]
public DocuRef insertFile(
    Common _owner, 
    System.IO.Stream _stream, 
    str _filePath, 
    str _attachmentName, 
    DocuTypeId _docuTypeId)
{
    DocuRef docuRef;
    if (_stream)
    {
        DocuType::createDefaults();
        if (!this.isDocuTypeValid(_docuTypeId))
        {
            throw error(strFmt("@ElectronicReporting:DocuTypeIsNotValid", _docuTypeId));
        }
        var args = ERDocuManagementAttachingFileEventArgs::construct(_owner, _stream, _filePath, _attachmentName, _docuTypeId);
        ERDocuManagementEvents::onAttachingFile(args);
        if (args.isHandled())
        {
            docuRef = args.getDocuRef();
        }
        else
        {
            docuRef = this.attachFile(_owner, _stream, _filePath, _attachmentName, _docuTypeId);
        }
    }
    return docuRef;
}
```

<span data-ttu-id="fd445-138">เหตุการณ์ **AttachingFile()** ปรากฏขึ้น เมื่อมีการประมวลผลปลายทาง ER ต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="fd445-138">The **AttachingFile()** event is raised when the following ER destinations are processed:</span></span>

- <span data-ttu-id="fd445-139">**เก็บถาวร** – เมื่อมีการใช้ปลายทางนี้ จะมีการสร้างเรกคอร์ดใหม่สำหรับรูปแบบ ER ที่รันในตาราง ERFormatMappingRunJobTable</span><span class="sxs-lookup"><span data-stu-id="fd445-139">**Archive** – When this destination is used, a new record for the ER format that is run is created in the ERFormatMappingRunJobTable table.</span></span> <span data-ttu-id="fd445-140">ฟิลด์ **ที่เก็บถาวร** ในเรกคอร์ดนี้ถูกตั้งค่าเป็น **เท็จ**</span><span class="sxs-lookup"><span data-stu-id="fd445-140">The **Archived** field in this record is set to **False**.</span></span> <span data-ttu-id="fd445-141">ถ้ารูปแบบ ER รันเสร็จเรียบร้อยแล้ว เอกสารที่สร้างขึ้นจะถูกแนบกับเรกคอร์ดนี้ และเหตุการณ์ **AttachingFile()** ปรากฏขึ้น</span><span class="sxs-lookup"><span data-stu-id="fd445-141">If the ER format is successfully run, the generated document is attached to this record, and the **AttachingFile()** event is raised.</span></span> <span data-ttu-id="fd445-142">ชนิดเอกสารที่ถูกเลือกในปลายทาง ER นี้ กำหนดสถานที่เก็บสำหรับไฟล์ที่แนบ (Microsoft Azure Storage หรือโฟลเดอร์ Microsoft SharePoint)</span><span class="sxs-lookup"><span data-stu-id="fd445-142">The document type that is selected in this ER destination determines the storage location for the attached file (Microsoft Azure Storage or a Microsoft SharePoint folder).</span></span>
- <span data-ttu-id="fd445-143">**ที่เก็บถาวรงาน** – เมื่อมีการใช้ปลายทางนี้ จะมีการสร้างเรกคอร์ดใหม่สำหรับฟอร์ม ER ที่รันในตาราง ERFormatMappingRunJobTable</span><span class="sxs-lookup"><span data-stu-id="fd445-143">**Job archive** – When this destination is used, a new record for the ER form that is run is created in the ERFormatMappingRunJobTable table.</span></span> <span data-ttu-id="fd445-144">ฟิลด์ **ที่เก็บถาวร** ในเรกคอร์ดนี้ถูกตั้งค่าเป็น **จริง**</span><span class="sxs-lookup"><span data-stu-id="fd445-144">The **Archived** field in this record is set to **True**.</span></span> <span data-ttu-id="fd445-145">ถ้ารูปแบบ ER รันเสร็จเรียบร้อยแล้ว เอกสารที่สร้างขึ้นจะถูกแนบกับเรกคอร์ดนี้ และเหตุการณ์ **AttachingFile()** ปรากฏขึ้น</span><span class="sxs-lookup"><span data-stu-id="fd445-145">If the ER format is successfully run, the generated document is attached to this record, and the **AttachingFile()** event is raised.</span></span> <span data-ttu-id="fd445-146">ชนิดเอกสารที่ถูกตั้งค่าคอนฟิกในพารามิเตอร์ ER กำหนดสถานที่เก็บสำหรับไฟล์ที่แนบ (Azure Storage หรือโฟลเดอร์ SharePoint)</span><span class="sxs-lookup"><span data-stu-id="fd445-146">The document type that is configured in the ER parameters determines the storage location for the attached file (Azure Storage or a SharePoint folder).</span></span>

![หน้าพารามิเตอร์การรายงานทางอิเล็กทรอนิกส์](media/er-extend-file-storages-parameters.png)

## <a name="configure-an-er-destination"></a><span data-ttu-id="fd445-148">ตั้งค่าคอนฟิกปลายทาง ER</span><span class="sxs-lookup"><span data-stu-id="fd445-148">Configure an ER destination</span></span>

1. <span data-ttu-id="fd445-149">ตั้งค่าคอนฟิกปลายทางที่เก็บถาวรสำหรับหนึ่งในองค์ประกอบที่กล่าวไว้ก่อนหน้านี้ (ไฟล์ โฟลเดอร์ ตัวผนวก หรือสิ่งที่แนบมา) ของรูปแบบ ER ที่คุณสร้างขึ้นหรือนำเข้า</span><span class="sxs-lookup"><span data-stu-id="fd445-149">Configure the archived destination for one of the previously mentioned elements (file, folder, merger, or attachment) of the ER format that you created or imported.</span></span> <span data-ttu-id="fd445-150">สำหรับคำแนะนำ ดู [ER ตั้งค่าคอนฟิกปลายทาง](/dynamics365/unified-operations/dev-itpro/analytics/tasks/er-destinations-2016-11)</span><span class="sxs-lookup"><span data-stu-id="fd445-150">For guidance, see [ER Configure destinations](/dynamics365/unified-operations/dev-itpro/analytics/tasks/er-destinations-2016-11).</span></span>
2. <span data-ttu-id="fd445-151">ใช้ชนิดเอกสารที่คุณเพิ่มก่อนหน้านี้สำหรับปลายทางที่ตั้งค่าคอนฟิก</span><span class="sxs-lookup"><span data-stu-id="fd445-151">Use the document type that you added earlier for the configured destination.</span></span> <span data-ttu-id="fd445-152">(สำหรับตัวอย่างในหัวข้อนี้ ชนิดเอกสารคือ **FileX**)</span><span class="sxs-lookup"><span data-stu-id="fd445-152">(For the example in this topic, the document type is **FileX**.)</span></span>

![กล่องโต้ตอบการตั้งค่าปลายทาง](media/er-extend-file-storages-destination.png)

## <a name="modify-source-code"></a><span data-ttu-id="fd445-154">ปรับเปลี่ยนโค้ดต้นฉบับ</span><span class="sxs-lookup"><span data-stu-id="fd445-154">Modify source code</span></span>

1. <span data-ttu-id="fd445-155">เพิ่มคลาสใหม่ไปยังโครงการ Microsoft Visual Studio ของคุณ และเขียนโค้ดเพื่อสมัครสมาชิกไปยังเหตุการณ์ **AttachingFile()** ที่มีการกล่าวถึงก่อนหน้านี้</span><span class="sxs-lookup"><span data-stu-id="fd445-155">Add a new class to your Microsoft Visual Studio project, and write code to subscribe to the **AttachingFile()** event that was mentioned earlier.</span></span> <span data-ttu-id="fd445-156">(สำหรับข้อมูลเพิ่มเติมเกี่ยวกับรูปแบบความสามารถในการเพิ่มที่ถูกใช้ ดู [ตอบสนองโดยใช้ EventHandlerResult](/dynamics365/unified-operations/dev-itpro/extensibility/respond-event-handler-result)) ตัวอย่างเช่น ในคลาสใหม่ เขียนรหัสที่ทำการดำเนินการต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="fd445-156">(For more information about the extensibility pattern that is used, see [Respond by using EventHandlerResult](/dynamics365/unified-operations/dev-itpro/extensibility/respond-event-handler-result).) For example, in the new class, write code that performs the following actions:</span></span>

    1. <span data-ttu-id="fd445-157">จัดเก็บไฟล์ที่สร้างขึ้นในโฟลเดอร์ของระบบไฟล์ในเครื่องของเซิร์ฟเวอร์ที่รันบริการ Application Object Server (AOS)</span><span class="sxs-lookup"><span data-stu-id="fd445-157">Store generated files in a folder of the local file system of the server that runs the Application Object Server (AOS) service.</span></span>
    2. <span data-ttu-id="fd445-158">จัดเก็บไฟล์ที่สร้างขึ้นเหล่านี้ เฉพาะเมื่อชนิดของเอกสารใหม่ (ตัวอย่างเช่น ชนิด **FileX** ที่มีคำสำคัญ "(LOCAL)" ในชื่อ) ถูกใช้ในขณะที่แฟ้มถูกแนบกับเรกคอร์ดในล็อกงานการดำเนินการ ER</span><span class="sxs-lookup"><span data-stu-id="fd445-158">Store these generated files only when the new document type (for example, the **FileX** type that has the "(LOCAL)" keyword in its name) is used while a file is attached to the record in the ER execution job log.</span></span>

    ```xpp
    class ERDocuSubscriptionSample
    {
        void new()
        {
        }
        [SubscribesTo(classStr(ERDocuManagementEvents), 
        staticDelegateStr(ERDocuManagementEvents, 
        attachingFile))]
        public static void ERDocuManagementEvents_attachingFile(ERDocuManagementAttachingFileEventArgs _args)
        {
            if (!_args.isHandled())
            {
                DocuType docuType = DocuType::find(_args.getDocuTypeId());
                if (strContains(docuType.Name, '(LOCAL)'))
                {
                    _args.markAsHandled();
                    var stream = _args.getStream();
                    if (stream.CanSeek)
                    {
                        stream.Seek(0, System.IO.SeekOrigin::Begin);
                    }
                    using (var localStream = System.IO.File::OpenWrite(@'c:\0\' + _args.getAttachmentName()))
                    {
                        stream.CopyTo(localStream);
                    }
                }
            }
        }
    }
    ```

2. <span data-ttu-id="fd445-159">สร้างโครงการของคุณใหม่</span><span class="sxs-lookup"><span data-stu-id="fd445-159">Rebuild your project.</span></span>

## <a name="run-the-er-format-that-you-created-or-imported"></a><span data-ttu-id="fd445-160">เรียกใช้รูปแบบ ER ที่คุณสร้างหรือนำเข้า</span><span class="sxs-lookup"><span data-stu-id="fd445-160">Run the ER format that you created or imported</span></span>

1. <span data-ttu-id="fd445-161">ดำเนินการรูปแบบ ER ที่คุณสร้างหรือนำเข้า</span><span class="sxs-lookup"><span data-stu-id="fd445-161">Execute the ER format that you created or imported.</span></span>
2. <span data-ttu-id="fd445-162">ไปที่ **การจัดการองค์กร \> การรายงานทางอิเล็กทรอนิกส์ \> งานการรายงานทางอิเล็กทรอนิกส์**</span><span class="sxs-lookup"><span data-stu-id="fd445-162">Go to **Organization administration \> Electronic reporting \> Electronic reporting jobs**.</span></span> <span data-ttu-id="fd445-163">ค้นหาเรกคอร์ดที่มีการสร้างสำหรับงานการดำเนินงานนี้ และที่มีการแนบไฟล์ที่สร้าง</span><span class="sxs-lookup"><span data-stu-id="fd445-163">Find the record that was created for this execution job, and that has the generated file attached to it.</span></span>
3. <span data-ttu-id="fd445-164">สำรวจโฟลเดอร์ **c:\\0** ท้องถิ่น เพื่อค้นหาไฟล์ที่สร้างเดียวกัน</span><span class="sxs-lookup"><span data-stu-id="fd445-164">Explore the local **C:\\0** folder to find same generated file.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="fd445-165">แหล่งข้อมูลเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="fd445-165">Additional resources</span></span>

- [<span data-ttu-id="fd445-166">ปลายทางการรายงานทางอิเล็กทรอนิกส์ (ER)</span><span class="sxs-lookup"><span data-stu-id="fd445-166">Electronic reporting (ER) destinations</span></span>](electronic-reporting-destinations.md)
- [<span data-ttu-id="fd445-167">หน้าแรกของความสามารถในการเพิ่มฟังก์ชัน</span><span class="sxs-lookup"><span data-stu-id="fd445-167">Extensibility home page</span></span>](../extensibility/extensibility-home-page.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]