---
title: ชนิดของปลายทาง ER เครื่องพิมพ์
description: หัวข้อนี้จะอธิบายวิธีการตั้งค่าคอนฟิกปลายทางเครื่องพิมพ์สำหรับแต่ละโฟลเดอร์หรือส่วนประกอบของไฟล์ของรูปแบบการรายงานทางอิเล็กทรอนิกส์ (ER) ที่มีการตั้งค่าคอนฟิกเพื่อสร้างเอกสารขาออก ทั้งในรูปแบบ PDF หรือ Microsoft Office (Excel\Word)
author: NickSelin
manager: AnnBe
ms.date: 03/17/2020
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
ms.openlocfilehash: 148da191ce4ea99c237895c40ec007a1aa0cd537
ms.sourcegitcommit: 0d9ca44b48fb2e33d8160faccc1e6bd932e58934
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 03/18/2020
ms.locfileid: "3150803"
---
# <a name="printer-destination"></a><a name="PrinterDestinationType"></a>ปลายทางเครื่องพิมพ์

[!include [banner](../includes/banner.md)]

คุณสามารถส่งเอกสารที่สร้างขึ้นโดยตรงไปยังเครื่องพิมพ์บนเครือข่ายสำหรับการพิมพ์โดยตรง

## <a name="prerequisites"></a>ข้อกำหนดเบื้องต้น

ก่อนที่คุณจะเริ่มต้น คุณต้องติดตั้งและตั้งค่าคอนฟิกตัวแทนการกำหนดเส้นทางเอกสาร แล้วลงทะเบียนเครื่องพิมพ์บนเครือข่าย สำหรับข้อมูลเพิ่มเติม ดูที่ [ติดตั้งเอเจนต์การกำหนดเส้นทางเอกสารเพื่อเปิดใช้งานการพิมพ์ผ่านเครือข่าย](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/analytics/install-document-routing-agent)

## <a name="make-the-printer-destination-available"></a>ทำให้การกำหนดปลายทางเครื่องพิมพ์พร้อมใช้งาน

เมื่อต้องการเปิดใช้งานปลายทาง **เครื่องพิมพ์** ในอินสแตนซ์ปัจจุบันของ Microsoft Dynamics 365 Finance ไปที่ **การจัดการคุณลักษณะ** และเปิดใช้งานคุณลักษณะต่อไปนี้ในใบสั่งนี้:

1. แปลงเอกสารขาออกของการรายงานทางอิเล็กทรอนิกส์จากรูปแบบ Microsoft Office เป็น PDF
2. เอเจนต์การกำหนดเส้นทางเอกสารเป็นปลายทางการรายงานทางอิเล็กทรอนิกส์สำหรับเอกสารขาออก

[![การเปิดใช้งานคุณลักษณะปลายทางเครื่องพิมพ์ ER ในการจัดการคุณลักษณะ](./media/ER_Destinations-EnablePrinterDestinationFeature.png)](./media/ER_Destinations-EnablePrinterDestinationFeature.png)

### <a name="applicability"></a>การมีผลบังคับใช้

ปลายทาง **เครื่องพิมพ์** สามารถตั้งค่าคอนฟิกสำหรับส่วนประกอบของไฟล์ที่ใช้ในการสร้างผลลัพธ์ในรูปแบบไฟล์ PDF ที่พิมพ์ได้ (ตัวผสาน PDF หรือองค์ประกอบไฟล์ PDF) หรือ Microsoft Office Excel /Word (ไฟล์ Excel) เท่านั้น เมื่อมีการสร้างผลลัพธ์ในรูปแบบ PDF จะมีการส่งออกไปยังเครื่องพิมพ์ เมื่อมีการสร้างผลลัพธ์ในรูปแบบ Microsoft Office โดยอัตโนมัติ จะมีการแปลงเป็นรูปแบบ PDF แล้วส่งไปยังเครื่องพิมพ์

### <a name="limitations"></a>การจำกัด

คุณลักษณะนี้เป็นคุณลักษณะของการแสดงตัวอย่างและอยู่ภายใต้เงื่อนไขการใช้งานที่อธิบายใน [ข้อกำหนดการใช้งานเพิ่มเติมสำหรับการแสดงตัวอย่าง Microsoft Dynamics 365](https://go.microsoft.com/fwlink/?linkid=2105274)

ปลายทาง **เครื่องพิมพ์** ใช้ในการปรับใช้สำหรับ cloud เท่านั้น

### <a name="use-the-printer-destination"></a>ใช้ปลายทางเครื่องพิมพ์

1. ตั้งค่าตัวเลือก **เปิดใช้งาน** เป็น **ใช่** เพื่อส่งเอกสารที่สร้างขึ้นไปยังเครื่องพิมพ์
2. ในฟิลด์ **ชื่อเครื่องพิมพ์** ให้เลือกเครื่องพิมพ์บนเครือข่ายที่ต้องการ
3. ตั้งค่าตัวเลือก **บันทึกในที่เก็บถาวรของการพิมพ์หรือไม่** เป็น **ใช่** เพื่อจัดเก็บผลลัพธ์ที่สร้างไว้ในที่เก็บถาวรของการพิมพ์ เพื่อให้พร้อมใช้สำหรับการพิมพ์เพิ่มเติม หากต้องการเข้าถึงผลลัพธ์ที่เก็บเก็บถาวร ให้ไปที่ **การจัดการองค์กร** \> **การสอบถามและรายงาน** \> **ที่เก็บถาวรของรายงาน**

[![การใช้ปลายทางเครื่องพิมพ์](./media/ER_Destinations-PrinterDestination.png)](./media/ER_Destinations-PrinterDestination.png)

> [!NOTE]
> ไม่จำเป็นต้องเปิดใช้งานตัวเลือก **แปลงเป็น PDF** เมื่อคุณตั้งค่าคอนฟิกปลายทาง **เครื่องพิมพ์** การแปลง PDF สำหรับวัตถุประสงค์ในการพิมพ์จะเกิดขึ้นแม้ว่าตัวเลือกนี้จะถูกปิดใช้งาน

เมื่อต้องการใช้ [การจัดวางหน้า](electronic-reporting-destinations.md#SelectPdfPageOrientation) เฉพาะ เมื่อคุณพิมพ์เอกสารขาออกในรูปแบบ Excel คุณต้องเปิดใช้งานตัวเลือก **แปลงเป็น PDF** เมื่อคุณตั้งค่าตัวเลือก **แปลงเป็น PDF** เป็น **ใช่** ฟิลด์ **การจัดวางหน้า** จะพร้อมใช้งาน ในฟิลด์ **การจัดวางหน้า** คุณสามารถเลือกการจัดวางหน้าได้

## <a name="additional-resources"></a>ทรัพยากรเพิ่มเติม

- [ภาพรวมการรายงานทางอิเล็กทรอนิกส์ (ER)](general-electronic-reporting.md)
- [ปลายทางการรายงานทางอิเล็กทรอนิกส์ (ER)](electronic-reporting-destinations.md)
