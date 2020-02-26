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
ms.openlocfilehash: 15611a4f0000ca5ccb0ac3f4012251d5bf5689ec
ms.sourcegitcommit: 54baab2a04e5c534fc2d1fd67b67e23a152d4e57
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 02/04/2020
ms.locfileid: "3020028"
---
# <a name="ArchiveDestinationType">ปลายทางที่เก็บถาวร</a>

[!include [banner](../includes/banner.md)]

คุณสามารถตั้งค่าคอนฟิกปลายทางที่เก็บถาวรของไฟล์สำหรับแต่ละโฟลเดอร์หรือส่วนประกอบของไฟล์ของรูปแบบการรายงานทางอิเล็กทรอนิกส์ (ER) ที่มีการตั้งค่าคอนฟิกเพื่อสร้างเอกสารขาออก เอกสารที่สร้างขึ้นจะถูกจัดเก็บเป็นเอกสารแนบของเรกคอร์ดของรายการงาน ER โดยยึดตามการตั้งค่าปลายทาง

คุณสามารถใช้ตัวเลือกนี้เพื่อส่งเอกสารที่สร้างขึ้นไปยังโฟลเดอร์ Microsoft SharePoint หรือที่จัดเก็บ Microsoft Azure ตั้งค่า **เปิดใช้งานอยู่** เป็น **ใช่**เพื่อส่งเอาท์พุทไปยังปลายทางที่กำหนดโดยชนิดเอกสารที่เลือก สามารถเลือกได้เฉพาะชนิดเอกสารที่กลุ่มที่ถูกตั้งค่าเป็น **ไฟล์** คุณกำหนด [ชนิด](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/organization-administration/configure-document-management#configure-document-types) เอกสารได้ที่ **การจัดการองค์กร** \> **การจัดการเอกสาร** \> **ชนิดเอกสาร** การตั้งค่าคอนฟิกปลายทาง ER เหมือนกับการตั้งค่าคอนฟิกระบบการจัดการเอกสาร

[![หน้าชนิดเอกสาร](./media/ER_Destinations-SharePointDocuType.png)](./media/ER_Destinations-SharePointDocuType.png)

ตำแหน่งที่ตั้งเป็นตัวกำหนดตำแหน่งที่บันทึกไฟล์ หลังจากที่เปิดใช้งานปลายทาง **ที่เก็บถาวร** แล้ว สามารถบันทึกผลลัพธ์ในที่เก็บถาวรของงาน คุณสามารถดูผลลัพธ์ได้ที่ **การจัดการองค์กร** \> **การรายงานทางอิเล็กทรอนิกส์** \> **ที่เก็บถาวรงานของการรายงานทางอิเล็กทรอนิกส์**

> [!NOTE]
> เลือกชนิดเอกสารสำหรับที่เก็บงานถาวรโดยนำทางไปยัง **การจัดการองค์กร** \> **พื้นที่ทำงาน** \> **การรายงานทางอิเล็กทรอนิกส์** \> **พารามิเตอร์การรายงานทางอิเล็กทรอนิกส์** สำหรับข้อมูลเพิ่มเติม โปรดดู [ตั้งค่าคอนฟิกกรอบงานของการรายงานทางอิเล็กทรอนิกส์ (ER)](electronic-reporting-er-configure-parameters.md#prerequisites-for-er-setup)

## <a name="sharepoint"></a>SharePoint

คุณสามารถบันทึกไฟล์ในโฟลเดอร์ SharePoint ที่กำหนด ในการกำหนดเซิร์ฟเวอร์ SharePoint เริ่มต้น ให้ไปที่ **การจัดการองค์กร** \> **การจัดการเอกสาร** \> **พารามิเตอร์การจัดการเอกสาร** บนแท็บ **SharePoint** ให้ตั้งค่าคอนฟิกโฟลเดอร์ SharePoint จากนั้นคุณสามารถเลือกเป็นโฟลเดอร์ที่จะมีการบันทึกผลลัพธ์ของ ER ที่ตั้งของ **SharePoint** ต้องถูกเลือกในชนิดเอกสารนี้

[![การเลือกโฟลเดอร์ SharePoint](./media/ER_Destinations-SharePointDocuTypeLocation.png)](./media/ER_Destinations-SharePointDocuTypeLocation.png)

## <a name="azure-storage"></a>ที่เก็บข้อมูล Azure

เมื่อตำแหน่งที่ตั้งชนิดเอกสารถูกตั้งค่าเป็น **ที่เก็บข้อมูล Azure** คุณสามารถบันทึกไฟล์ไปยังที่เก็บข้อมูล Azure ได้

## <a name="additional-resources"></a>แหล่งข้อมูลเพิ่มเติม

- [ภาพรวมการรายงานทางอิเล็กทรอนิกส์ (ER)](general-electronic-reporting.md)
- [ปลายทางการรายงานทางอิเล็กทรอนิกส์ (ER)](electronic-reporting-destinations.md)
- [ตั้งค่าคอนฟิกการจัดการเอกสาร](../../fin-ops/organization-administration/configure-document-management.md)
