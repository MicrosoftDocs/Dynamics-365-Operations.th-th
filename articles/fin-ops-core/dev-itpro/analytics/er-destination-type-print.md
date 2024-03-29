---
title: ชนิดของปลายทาง ER เครื่องพิมพ์
description: บทความนี้อธิบายวิธีการตั้งค่าคอนฟิกปลายทางเครื่องพิมพ์ให้กับแต่ละส่วนประกอบโฟลเดอร์หรือไฟล์ ของรูปแบบการรายงานทางอิเล็กทรอนิกส์ (ER)
author: kfend
ms.date: 02/14/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: filatovm
ms.search.validFrom: 2020-04-01
ms.dyn365.ops.version: AX 10.0.9
ms.custom: 97423
ms.assetid: ''
ms.search.form: DocuType, ERSolutionTable, ERFormatDestinationTable
ms.openlocfilehash: 7e01476b85c6c35d7c36c90db4d64ab2a2930fec
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 08/12/2022
ms.locfileid: "9271748"
---
# <a name="printer-destination"></a><a name="PrinterDestinationType"></a>ปลายทางของเครื่องพิมพ์

[!include [banner](../includes/banner.md)]

คุณสามารถส่งเอกสารที่สร้างขึ้นโดยตรงไปยังเครื่องพิมพ์บนเครือข่ายสำหรับการพิมพ์โดยตรง

## <a name="prerequisites"></a>ข้อกำหนดเบื้องต้น

ก่อนที่คุณจะเริ่มต้น คุณต้องติดตั้งและตั้งค่าคอนฟิกตัวแทนการกำหนดเส้นทางเอกสาร แล้วลงทะเบียนเครื่องพิมพ์บนเครือข่าย สำหรับข้อมูลเพิ่มเติม ดูที่ [ติดตั้งเอเจนต์การกำหนดเส้นทางเอกสารเพื่อเปิดใช้งานการพิมพ์ผ่านเครือข่าย](./install-document-routing-agent.md)

## <a name="make-the-printer-destination-available"></a>ทำให้การกำหนดปลายทางเครื่องพิมพ์พร้อมใช้งาน

เมื่อต้องการเปิดใช้งานปลายทาง **เครื่องพิมพ์** ในอินสแตนซ์ปัจจุบันของ Microsoft Dynamics 365 Finance ไปที่ **การจัดการคุณลักษณะ** และเปิดใช้งานคุณลักษณะต่อไปนี้ในใบสั่งนี้:

1. แปลงเอกสารขาออกของการรายงานทางอิเล็กทรอนิกส์จากรูปแบบ Microsoft Office เป็น PDF
2. เอเจนต์การกำหนดเส้นทางเอกสารเป็นปลายทางการรายงานทางอิเล็กทรอนิกส์สำหรับเอกสารขาออก

[![การเปิดใช้งานคุณลักษณะปลายทางเครื่องพิมพ์ ER ในการจัดการคุณลักษณะ](./media/ER_Destinations-EnablePrinterDestinationFeature.png)](./media/ER_Destinations-EnablePrinterDestinationFeature.png)

### <a name="applicability"></a>การใช้งาน

#### <a name="pdf-printing"></a>การพิมพ์ PDF

ใน Finance รุ่นก่อนรุ่น 10.0.18 คุณสามารถตั้งค่าคอนฟิกปลายทาง **เครื่องพิมพ์** สำหรับส่วนประกอบของไฟล์ที่ใช้ในการสร้างผลลัพธ์ในรูปแบบไฟล์ PDF ที่พิมพ์ได้เท่านั้น (องค์ประกอบรูปแบบ **ตัวผสาน PDF** หรือ **ไฟล์ PDF**) หรือรูปแบบ Microsoft Office Excel และ Word (องค์ประกอบรูปแบบ **ไฟล์ Excel**) เมื่อมีการสร้างผลลัพธ์ในรูปแบบ PDF จะมีการส่งออกไปยังเครื่องพิมพ์ เมื่อมีการสร้างผลลัพธ์ในรูปแบบ Office โดยใช้องค์ประกอบรูปแบบ **ไฟล์ Excel** จะมีการแปลงเป็นรูปแบบ PDF โดยอัตโนมัติแล้วส่งไปยังเครื่องพิมพ์

อย่างไรก็ตาม ในรุ่น 10.0.18 คุณสามารถตั้งค่าคอนฟิกปลายทาง **เครื่องพิมพ์** สำหรับองค์ประกอบรูปแบบ **ไฟล์ทั่วไป** ส่วนใหญ่แล้วองค์ประกอบรูปแบบนี้จะใช้ในการสร้างผลลัพธ์ในรูปแบบ TXT หรือ XML คุณสามารถตั้งค่าคอนฟิกรูปแบบ ER ที่มีองค์ประกอบรูปแบบ **ไฟล์ทั่วไป** เป็นองค์ประกอบรูปแบบรากและองค์ประกอบรูปแบบ **เนื้อหาไบนารี** เมื่อมีองค์ประกอบที่ซ้อนกันภายใต้รูปแบบเท่านั้น ในกรณีนี้ องค์ประกอบรูปแบบ **ไฟล์ทั่วไป** จะสร้างผลลัพธ์ในรูปแบบที่ระบุโดยการผูกข้อมูลที่คุณตั้งค่าคอนฟิกสำหรับองค์ประกอบรูปแบบ **เนื้อหาไบนารี** ตัวอย่างเช่น คุณสามารถตั้งค่าคอนฟิกการผูกข้อมูลนี้ให้ [เติม](tasks/er-document-management-files-5.md#modify-the-format-to-populate-attachments-into-generating-messages-in-binary-format) องค์ประกอบนี้ด้วยเนื้อหาของการแนบ [การจัดการเอกสาร](../../fin-ops/organization-administration/configure-document-management.md) ในรูปแบบ PDF หรือ Office (Excel หรือ Word) คุณสามารถพิมพ์ผลลัพธ์โดยใช้ปลายทาง **เครื่องพิมพ์** ที่ตั้งค่าคอนฟิก 

> [!NOTE]
> เมื่อคุณเลือกองค์ประกอบรูปแบบ **Common\\File** เพื่อตั้งค่าคอนฟิกปลายทาง **เครื่องพิมพ์** ไม่มีวิธีการรับประกันในเวลาการออกแบบว่าองค์ประกอบที่เลือกจะสร้างผลลัพธ์ในรูปแบบ PDF หรือผลลัพธ์ที่สามารถแปลงเป็นรูปแบบ PDF ดังนั้น คุณจะได้รับข้อความเตือนต่อไปนี้: "โปรดตรวจสอบให้แน่ใจว่าผลลัพธ์ที่สร้างขึ้นโดยส่วนประกอบรูปแบบที่เลือกสามารถแปลงเป็น PDF ได้ ไม่เช่นนั้น ให้ยกเลิกการเลือกตัวเลือก 'แปลงเป็น PDF' คุณต้องปฏิบัติตามขั้นตอนต่างๆ เพื่อป้องกันไม่ให้เกิดปัญหารันไทม์เมื่อมีการระบุผลลัพธ์ที่ไม่ใช่ PDF หรือไม่สามารถแปลงเป็น PDF สำหรับการพิมพ์ขณะรันไทม์ ถ้าคุณคาดว่าจะได้รับผลลัพธ์ในรูปแบบ Office (Excel หรือ Word) คุณต้องเลือกตัวเลือก **แปลงเป็น PDF**
>
> ในรุ่น 10.0.26 และที่ใหม่กว่า เพื่อใช้ตัวเลือก **แปลงเป็น PDF** คุณต้องเลือก **PDF** สำหรับพารามิเตอร์ **ชนิดการกำหนดเส้นทางเอกสาร** ของปลายทาง **เครื่องพิมพ์** ที่ตั้งค่าคอนฟิก

#### <a name="zpl-printing"></a>การพิมพ์ ZPL

ในรุ่น 10.0.26 และที่ใหม่กว่า คุณสามารถตั้งค่าคอนฟิกปลายทาง **เครื่องพิมพ์** สำหรับองค์ประกอบรูปแบบ **Common\\File** โดยเลือก **ZPL** สำหรับพารามิเตอร์ **ชนิดการกำหนดเส้นทางเอกสาร** ในกรณีนี้ ตัวเลือก **แปลงเป็น PDF** จะถูกละเว้นขณะรันไทม์ และส่งผลลัพธ์ TXT หรือ XML ไปยังเครื่องพิมพ์ที่เลือกโดยตรงโดยใช้สัญญา Zebra Programming Language (ZPL) ของ [เอเจนต์การกำหนดเส้นทางเอกสาร (DRA)](install-document-routing-agent.md) ใช้คุณลักษณะนี้กับรูปแบบ ER ที่แสดงถึงโครงร่างป้ายชื่อ ZPL II เพื่อพิมพ์ป้ายชื่อต่างๆ

[![การตั้งค่าพารามิเตอร์ชนิดการกำหนดเส้นทางเอกสารในกล่องโต้ตอบการตั้งค่าปลายทาง](./media/ER_Destinations-SetDocumentRoutingType.png)](./media/ER_Destinations-SetDocumentRoutingType.png)

สำหรับข้อมูลเพิ่มเติมเกี่ยวกับคุณลักษณะนี้ ดูที่ [ออกแบบโซลูชัน ER ใหม่เพื่อพิมพ์ป้ายชื่อ ZPL](er-design-zpl-labels.md)

### <a name="limitations"></a>การจำกัด

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


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
