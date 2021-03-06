---
title: ออกแบบการตั้งค่าคอนฟิก ER ใหม่ เพื่อสร้างรายงานในรูปแบบ Word
description: หัวข้อนี้อธิบายวิธีการที่ผู้ใช้สามารถตั้งค่าคอนฟิกรูปแบบการรายงานทางอิเล็กทรอนิกส์ (ER) เพื่อสร้างรายงานเป็นเอกสาร Microsoft Word
author: NickSelin
manager: AnnBe
ms.date: 12/17/2020
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ERWorkspace, ERSolutionTable, EROperationDesigner,  LedgerJournalTable, LedgerJournalTransVendPaym
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2020-01-01
ms.dyn365.ops.version: Version 10.0.6
ms.openlocfilehash: 535e46eb033bf2796ab8e4b0d2e29767ad0a8cdf
ms.sourcegitcommit: 5192cfaedfd861faea63d8954d7bcc500608a225
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 01/30/2021
ms.locfileid: "5094165"
---
# <a name="design-a-new-er-configuration-to-generate-reports-in-word-format"></a>ออกแบบการตั้งค่าคอนฟิก ER ใหม่ เพื่อสร้างรายงานในรูปแบบ Word

[!include [banner](../includes/banner.md)]

หากต้องการสร้างรายงานเป็นเอกสาร Microsoft Word คุณต้องออกแบบเท็มเพลตให้กับรายงาน โดยการใช้ ตัวอย่างเช่น แอพลิเคชันบนเดสก์ท็อปของ Word เป็นต้น รูปภาพประกอบต่อไปนี้จะแสดงเท็มเพลตตัวอย่างของรายงานการควบคุม ที่สามารถสร้างขึ้นเพื่อแสดงรายละเอียดของการชำระเงินให้แก่ผู้จัดจำหน่ายที่ประมวลผลแล้ว

![เท็มเพลตตัวอย่างเกี่ยวกับรายงานการควบคุมในแอพลิเคชันบนเดสก์ท็อปของ Word](./media/er-design-configuration-word-image1.png)

หากต้องการใช้เอกสาร Word เป็นเท็มเพลตของรายงานในรูปแบบ Word คุณสามารถตั้งค่าคอนฟิก [การรายงานทางอิเล็กทรอนิกส์ (ER)](general-electronic-reporting.md) [โซลูชัน](er-quick-start1-new-solution.md) ใหม่ได้ โซลูชันนี้ต้องมี [การตั้งค่าคอนฟิก](general-electronic-reporting.md#Configuration) ของ ER ที่มีส่วนประกอบ [รูปแบบ](general-electronic-reporting.md#FormatComponentOutbound) ของ ER

> [!NOTE]
> เมื่อคุณสร้างการตั้งค่าคอนฟิกรูปแบบ ER ใหม่ เพื่อสร้างรายงานในรูปแบบ Word คุณต้องเลือก **Word** เป็นชนิดรูปแบบ ในกล่องโต้ตอบแบบหล่นลง **สร้างการตั้งค่าคอนฟิก** หรือปล่อยฟิลด์ **ชนิดรูปแบบ** ให้ว่างไว้

![การสร้างการตั้งค่าคอนฟิกรูปแบบในหน้าการตั้งค่าคอนฟิก](./media/er-design-configuration-word-image2.gif)

ส่วนประกอบรูปแบบ ER ของโซลูชัน ต้องมีองค์ประกอบรูปแบบ **Excel\\ไฟล์** และองค์ประกอบรูปแบบนั้นต้องเชื่อมโยงกับเอกสาร Word ที่จะใช้เป็นเท็มเพลตสำหรับรายงานที่สร้างขณะรันไทม์ เมื่อต้องการตั้งค่าคอนฟิกส่วนประกอบรูปแบบ ER คุณต้องเปิดเวอร์ชัน [แบบร่าง](general-electronic-reporting.md#component-versioning) ของการตั้งค่าคอนฟิก ER ที่สร้างขึ้นในโปรแกรมออกแบบรูปแบบ ER แล้วเพิ่มองค์ประกอบของ **Excel\\ไฟล์** ให้แนบเท็มเพลต Word ของคุณเข้ากับรูปแบบ ER ที่แก้ไขได้ และเชื่อมโยงเท็มเพลตนั้นกับองค์ประกอบ **Excel\\File** ที่คุณเพิ่ม

> [!NOTE]
> เมื่อคุณแนบเท็มเพลต คุณต้องใช้ [ชนิดเอกสาร](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/organization-administration/configure-document-management#configure-document-types) ที่ได้รับการ [ตั้งค่าคอนฟิก](electronic-reporting-er-configure-parameters.md#parameters-to-manage-documents) ก่อนหน้านี้ ในพารามิเตอร์ ER เพื่อเก็บเท็มเพลตของรูปแบบ ER

![การแนบเท็มเพลตบนหน้าโปรแกรมออกแบบรูปแบบ](./media/er-design-configuration-word-image3.gif)

คุณสามารถเพิ่มส่วนประกอบ **Excel\\ช่วง** และ **Excel\\เซลล์** ที่ซ้อนกันสำหรับองค์ประกอบ **Excel\\ไฟล์** เพื่อระบุโครงสร้างของข้อมูลที่จะป้อนในรายงานที่สร้างขึ้นในขณะรันไทม์ จากนั้นคุณต้องผูกองค์ประกอบเหล่านั้นกับแหล่งข้อมูลของรูปแบบ ER ที่แก้ไขได้ เพื่อระบุข้อมูลจริงที่จะป้อนในรายงานที่สร้างขึ้นขณะรันไทม์

![การเพิ่มองค์ประกอบที่ซ้อนกันบนหน้าตัวออกแบบรูปแบบ](./media/er-design-configuration-word-image4.gif)

เมื่อคุณบันทึกการเปลี่ยนแปลงของคุณไปยังรูปแบบ ER ณ เวลาการออกแบบ โครงสร้างรูปแบบตามลำดับจะจัดเก็บอยู่ในเท็มเพลต Word ที่แนบ เป็น [ส่วน XML แบบกำหนดเอง](https://docs.microsoft.com/visualstudio/vsto/custom-xml-parts-overview?view=vs-2019) ที่ชื่อ **รายงาน** คุณต้องเข้าถึงเท็มเพลตที่แก้ไข ดาวน์โหลดจาก Finance จัดเก็บภายในเครือง และเปิดเท็มเพลตนั้นในแอพลิเคชันบนเดสก์ท็อปของ Word ภาพต่อไปนี้จะแสดงเท็มเพลตตัวอย่างที่จัดเก็บภายในเครืองของรายงานการควบคุมที่มีส่วน XML แบบกำหนดเองของ **รายงาน**

![การแสดงตัวอย่างของเท็มเพลตรายงานตัวอย่าง ในแอพลิเคชันบนเดสก์ท็อปของ Word](./media/er-design-configuration-word-image5.gif)

เมื่อผูกข้อมูลขององค์ประกอบรูปแบบ **Excel\\ช่วง** และ **Excel\\เซลล์** จะรันในขณะรันไทม์ ข้อมูลที่การจัดส่งที่ผูกไว้ทุกรายการจะมาจากเอกสาร Word ที่สร้างขึ้นเป็นแต่ละฟิลด์ของส่วน XML แบบกำหนดเองของ **รายงาน** หากต้องการป้อนค่าในฟิลด์ของส่วน XML ที่กำหนดเองในเอกสารที่สร้างขึ้น คุณต้องเพิ่ม [ตัวควบคุมเนื้อหา](https://docs.microsoft.com/office/client-developer/word/content-controls-in-word) Word ที่เหมาะสม ลงในเท็มเพลต Word ของคุณ เพื่อใช้เป็นตัวยึดข้อมูลซึ่งจะถูกเติมขณะรันไทม์ หากต้องการระบุวิธีการกรอกข้อมูลตัวควบคุมเนื้อหา ให้แม็ปตัวควบคุมเนื้อหาทุกรายการกับฟิลด์ที่เหมาะสมของส่วน XML ที่กำหนดเองของ **รายงาน**

![การเพิ่มและการแม็ปตัวควบคุมเนื้อหาในแอพลิเคชันบนเดสก์ทอปของ Word](./media/er-design-configuration-word-image6.gif)

จากนั้นคุณต้องแทนที่เท็มเพลต Word ดั้งเดิมของรูปแบบ ER ที่แก้ไขได้ ด้วยเท็มเพลตที่แก้ไข ซึ่งขณะนี้มีตัวควบคุมเนื้อหา Word ที่ถูกแม็ปไปยังฟิลด์ของส่วน XML ที่กำหนดเองของ **รายงาน**

![การแทนที่เท็มเพลตบนหน้าโปรแกรมออกแบบรูปแบบ](./media/er-design-configuration-word-image7.gif)

เมื่อคุณรันรูปแบบ ER ที่ตั้งค่าคอนฟิก ระบบจะใช้เท็มเพลต Word ที่แนบเพื่อสร้างรายงานใหม่ ข้อมูลจริงจะจัดเก็บอยู่ในรายงาน Word เป็นส่วน XML ที่กำหนดเอง ชื่อว่า **รายงาน** เมื่อเปิดรายงานที่สร้างขึ้น ตัวควบคุมเนื้อหาของ Word จะเติมข้อมูลจากส่วน XML ที่กำหนดเองของ **รายงาน**

## <a name="frequently-asked-questions"></a>คำถามที่ถามบ่อย

**คําถาม:** ฉันตั้งค่าคอนฟิกรูปแบบ ER ให้พิมพ์เอกสาร Word ที่มีที่อยู่บริษัท ในเท็มเพลต Word ให้กับรูปแบบ ER นี้ ฉันแทรกตัวควบคุมเนื้อหารูปแบบ rich text เพื่อแสดงที่อยู่ของบริษัท ใน Finance ฉันป้อนที่อยู่บริษัทเป็นข้อความแบบหลายบรรทัด และเลือก **ป้อน** เพื่อเพิ่มการส่งคืนสินค้าให้กับทุกบรรทัดที่ฉันป้อน ดังนั้น ฉันคาดว่าที่อยู่บริษัทจะปรากฏเป็นข้อความแบบหลายบรรทัดในเอกสารที่สร้าง แต่ ที่อยู่ปรากฏเป็นข้อความบรรทัดเดียว ที่มีสัญลักษณ์พิเศษแทนการส่งคืนสินค้า การตั้งค่าของฉันมีอะไรที่ไม่ถูกต้อง

**คําตอบ:** แทนที่จะใช้ตัวควบคุมเนื้อหาข้อความแบบ Rich Text คุณต้องใช้ตัวควบคุมเนื้อหาข้อความธรรมดา และเลือกกล่องกาเครื่องหมาย **อนุญาตการส่งคืนสินค้า (หลายย่อหน้า)** ในคุณสมบัติของตัวควบคุม

## <a name="additional-resources"></a>ทรัพยากรเพิ่มเติม

- [ใช้การตั้งค่าคอนฟิก ER กับเท็มเพลต Excel มาใช้ใหม่เพื่อสร้างรายงานในรูปแบบ Word](./tasks/er-design-configuration-word-2016-11.md)
- [ฝังข้อมูลและรูปร่างในเอกสารที่คุณสร้างโดยใช้ ER](electronic-reporting-embed-images-shapes.md#embed-an-image-in-a-word-document)
