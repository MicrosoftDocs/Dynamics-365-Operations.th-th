---
title: ระบุตำแหน่งที่เก็บข้อมูลที่กำหนดเองสำหรับเอกสารที่สร้างขึ้น
description: หัวข้อนี้อธิบายวิธีการขยายรายการของสถานที่เก็บสำหรับเอกสารที่รูปแบบการรายงานทางอิเล็กทรอนิกส์ (ER) สร้างขึ้น
author: NickSelin
manager: AnnBe
ms.date: 02/22/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2019-3-31
ms.dyn365.ops.version: 10
ms.openlocfilehash: 45a2335d7a661ddc1d8907c56ae8193387f44e26
ms.sourcegitcommit: 4e62c22b53693c201baa646a8f047edb5a0a2747
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 02/07/2020
ms.locfileid: "3030877"
---
# <a name="specify-a-custom-storage-location-for-generated-documents"></a>ระบุตำแหน่งที่เก็บข้อมูลที่กำหนดเองสำหรับเอกสารที่สร้างขึ้น

[!include[banner](../includes/banner.md)]

Application Programming Interface (API) ของกรอบงานการรายงานทางอิเล็กทรอนิกส์ (ER) ช่วยให้คุณสามารถขยายรายการของสถานที่เก็บสำหรับเอกสารที่รูปแบบ ER สร้าง หัวข้อนี้มีภาพรวมของงานหลักที่คุณต้องดำเนินการเพิ่มสถานที่จัดเก็บที่กำหนดเองให้เสร็จสิ้น

## <a name="prerequisites"></a>ข้อกำหนดเบื้องต้น

คุณต้องปรับใช้โทโพโลยี ที่สนับสนุนการสร้างแบบต่อเนื่อง (สำหรับข้อมูลเพิ่มเติม ดู [ปรับใช้โทโพโลยีที่สนับสนุนการสร้างแบบต่อเนื่อง และการทำให้การทดสอบเป็นแบบอัตโนมัติ](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/perf-test/continuous-build-test-automation)) คุณต้องสามารถเข้าถึงโทโพโลยีนี้ สำหรับหนึ่งในบทบาทต่อไปนี้:

- นักพัฒนาการรายงานทางอิเล็กทรอนิกส์
- ที่ปรึกษาด้านการทำงานของการรายงานทางอิเล็กทรอนิกส์
- ผู้ดูแลระบบ

คุณต้องมีการเข้าถึงไปยังสภาพแวดล้อมการพัฒนาสำหรับโทโพโลยีนี้

## <a name="create-or-import-an-er-format-configuration"></a>สร้างหรือนำเข้าการตั้งค่าคอนฟิกรูปแบบ ER

ในโทโพโลยีปัจจุบัน [สร้างรูปแบบ ER ใหม่](tasks/er-format-configuration-2016-11.md) ในการสร้างเอกสารที่คุณวางแผนที่จะเพิ่มตำแหน่งที่เก็บแบบกำหนดเอง อีกทางหนึ่งคือ [นำเข้ารูปแบบ ER ที่มีอยู่ลงในโทโพโลยีนี้](general-electronic-reporting-manage-configuration-lifecycle.md)

![หน้าตัวออกแบบรูปแบบ](media/er-extend-file-storages-format.png)

> [!IMPORTANT]
> รูปแบบ ER ที่คุณสร้างหรือนำเข้า ต้องประกอบด้วยอย่างน้อยหนึ่งในองค์ประกอบรูปแบบต่อไปนี้:
>
> - ไฟล์
> - โฟลเดอร์
> - ตัวผสาน
> - สิ่งที่แนบมา

## <a name="create-a-new-document-type"></a>การสร้างชนิดเอกสารใหม่

เมื่อต้องการระบุวิธีการเวียนส่งเอกสารที่สร้างรูปแบบการ ER คุณต้องตั้งค่าคอนฟิก [ปลายทางการรายงานทางอิเล็กทรอนิกส์ (ER)](electronic-reporting-destinations.md) ในปลายทาง ER แต่ละแห่งที่ถูกตั้งค่าคอนฟิกให้จัดเก็บเอกสารที่สร้างขึ้นเป็นไฟล์ คุณต้องระบุชนิดเอกสารของกรอบงานการจัดการเอกสาร ชนิดเอกสารต่างๆ สามารถใช้กับเอกสารกระบวนการผลิตที่รูปแบบ ER ที่แตกต่างกันสร้างขึ้น

1. เพิ่ม [ชนิดเอกสาร](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/organization-administration/configure-document-management) ใหม่ สำหรับรูปแบบ ER ที่คุณสร้าง หรือนำเข้ามาก่อนหน้านี้ ในภาพประกอบต่อไปนี้ ชนิดเอกสารคือ **FileX**
2. เพื่อแบ่งแยกชนิดเอกสารนี้จากชนิดเอกสารอื่นๆ รวมคำสำคัญเฉพาะในชื่อ ตัวอย่างเช่น ในภาพประกอบต่อไปนี้ ชื่อคือ **โฟลเดอร์ (LOCAL)**
3. ในฟิลด์ **คลาส** ระบุ **แนบแฟ้ม**
4. ในฟิลด์ **กลุ่ม** ระบุ **แฟ้ม**

![หน้าชนิดเอกสาร](media/er-extend-file-storages-document-type.png)

> [!NOTE]
> ชนิดเอกสารเป็นแบบเฉพาะบริษัท ในการใช้รูปแบบ ER กับปลายทางที่ตั้งค่าคอนฟิกในหลายบริษัท คุณต้องตั้งค่าคอนฟิกชนิดเอกสารที่แยกต่างหากในแต่ละบริษัท

## <a name="review-source-code"></a>ตรวจสอบโค้ดต้นฉบับ

ทบทวนรหัสของวิธีการ **insertFile()** ของคลาส **ERDocuManagement** สังเกตว่า เหตุการณ์ **AttachingFile()** ปรากฏขึ้น ขณะที่แนบไฟล์ที่สร้างไปยังเรกคอร์ด

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

เหตุการณ์ **AttachingFile()** ปรากฏขึ้น เมื่อมีการประมวลผลปลายทาง ER ต่อไปนี้:

- **เก็บถาวร** – เมื่อมีการใช้ปลายทางนี้ จะมีการสร้างเรกคอร์ดใหม่สำหรับรูปแบบ ER ที่รันในตาราง ERFormatMappingRunJobTable ฟิลด์ **ที่เก็บถาวร** ในเรกคอร์ดนี้ถูกตั้งค่าเป็น **เท็จ** ถ้ารูปแบบ ER รันเสร็จเรียบร้อยแล้ว เอกสารที่สร้างขึ้นจะถูกแนบกับเรกคอร์ดนี้ และเหตุการณ์ **AttachingFile()** ปรากฏขึ้น ชนิดเอกสารที่ถูกเลือกในปลายทาง ER นี้ กำหนดสถานที่เก็บสำหรับไฟล์ที่แนบ (Microsoft Azure Storage หรือโฟลเดอร์ Microsoft SharePoint)
- **ที่เก็บถาวรงาน** – เมื่อมีการใช้ปลายทางนี้ จะมีการสร้างเรกคอร์ดใหม่สำหรับฟอร์ม ER ที่รันในตาราง ERFormatMappingRunJobTable ฟิลด์ **ที่เก็บถาวร** ในเรกคอร์ดนี้ถูกตั้งค่าเป็น **จริง** ถ้ารูปแบบ ER รันเสร็จเรียบร้อยแล้ว เอกสารที่สร้างขึ้นจะถูกแนบกับเรกคอร์ดนี้ และเหตุการณ์ **AttachingFile()** ปรากฏขึ้น ชนิดเอกสารที่ถูกตั้งค่าคอนฟิกในพารามิเตอร์ ER กำหนดสถานที่เก็บสำหรับไฟล์ที่แนบ (Azure Storage หรือโฟลเดอร์ SharePoint)

![หน้าพารามิเตอร์การรายงานทางอิเล็กทรอนิกส์](media/er-extend-file-storages-parameters.png)

## <a name="configure-an-er-destination"></a>ตั้งค่าคอนฟิกปลายทาง ER

1. ตั้งค่าคอนฟิกปลายทางที่เก็บถาวรสำหรับหนึ่งในองค์ประกอบที่กล่าวไว้ก่อนหน้านี้ (ไฟล์ โฟลเดอร์ ตัวผนวก หรือสิ่งที่แนบมา) ของรูปแบบ ER ที่คุณสร้างขึ้นหรือนำเข้า สำหรับคำแนะนำ ดู [ER ตั้งค่าคอนฟิกปลายทาง](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/analytics/tasks/er-destinations-2016-11)
2. ใช้ชนิดเอกสารที่คุณเพิ่มก่อนหน้านี้สำหรับปลายทางที่ตั้งค่าคอนฟิก (สำหรับตัวอย่างในหัวข้อนี้ ชนิดเอกสารคือ **FileX**)

![กล่องโต้ตอบการตั้งค่าปลายทาง](media/er-extend-file-storages-destination.png)

## <a name="modify-source-code"></a>ปรับเปลี่ยนโค้ดต้นฉบับ

1. เพิ่มคลาสใหม่ไปยังโครงการ Microsoft Visual Studio ของคุณ และเขียนโค้ดเพื่อสมัครสมาชิกไปยังเหตุการณ์ **AttachingFile()** ที่มีการกล่าวถึงก่อนหน้านี้ (สำหรับข้อมูลเพิ่มเติมเกี่ยวกับรูปแบบความสามารถในการเพิ่มที่ถูกใช้ ดู [ตอบสนองโดยใช้ EventHandlerResult](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/extensibility/respond-event-handler-result)) ตัวอย่างเช่น ในคลาสใหม่ เขียนรหัสที่ทำการดำเนินการต่อไปนี้:

    1. จัดเก็บไฟล์ที่สร้างขึ้นในโฟลเดอร์ของระบบไฟล์ในเครื่องของเซิร์ฟเวอร์ที่รันบริการ Application Object Server (AOS)
    2. จัดเก็บไฟล์ที่สร้างขึ้นเหล่านี้ เฉพาะเมื่อชนิดของเอกสารใหม่ (ตัวอย่างเช่น ชนิด **FileX** ที่มีคำสำคัญ "(LOCAL)" ในชื่อ) ถูกใช้ในขณะที่แฟ้มถูกแนบกับเรกคอร์ดในล็อกงานการดำเนินการ ER

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

2. สร้างโครงการของคุณใหม่

## <a name="run-the-er-format-that-you-created-or-imported"></a>เรียกใช้รูปแบบ ER ที่คุณสร้างหรือนำเข้า

1. ดำเนินการรูปแบบ ER ที่คุณสร้างหรือนำเข้า
2. ไปที่ **การจัดการองค์กร \> การรายงานทางอิเล็กทรอนิกส์ \> งานการรายงานทางอิเล็กทรอนิกส์** ค้นหาเรกคอร์ดที่มีการสร้างสำหรับงานการดำเนินงานนี้ และที่มีการแนบไฟล์ที่สร้าง
3. สำรวจโฟลเดอร์ **c:\\0** ท้องถิ่น เพื่อค้นหาไฟล์ที่สร้างเดียวกัน

## <a name="additional-resources"></a>แหล่งข้อมูลเพิ่มเติม

- [ปลายทางการรายงานทางอิเล็กทรอนิกส์ (ER)](electronic-reporting-destinations.md)
- [หน้าแรกของความสามารถในการเพิ่มฟังก์ชัน](../extensibility/extensibility-home-page.md)
