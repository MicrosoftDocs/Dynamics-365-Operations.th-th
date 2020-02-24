---
title: ชนิดของปลายทาง ER อีเมล
description: หัวข้อนี้จะให้ข้อมูลเกี่ยวกับวิธีการตั้งค่าคอนฟิกปลายทางของปลายทางอีเมลสำหรับแต่ละโฟลเดอร์หรือส่วนประกอบของไฟล์ของรูปแบบการรายงานทางอิเล็กทรอนิกส์ (ER) ที่มีการตั้งค่าคอนฟิกเพื่อสร้างเอกสารขาออก
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
ms.openlocfilehash: 086114d6a8d425ca01521d9607e4a70ec5aa766b
ms.sourcegitcommit: 54baab2a04e5c534fc2d1fd67b67e23a152d4e57
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 02/04/2020
ms.locfileid: "3020026"
---
# <a name="EmailDestinationType">ปลายทางของอีเมล</a>

[!include [banner](../includes/banner.md)]

คุณสามารถตั้งค่าคอนฟิกปลายทางอีเมลของไฟล์สำหรับแต่ละโฟลเดอร์หรือส่วนประกอบของไฟล์ของรูปแบบการรายงานทางอิเล็กทรอนิกส์ (ER) ที่มีการตั้งค่าคอนฟิกเพื่อสร้างเอกสารขาออก เอกสารที่สร้างขึ้นจะถูกส่งเป็นเอกสารแนบของข้อความทางอิเล็กทรอนิกส์ โดยยึดตามการตั้งค่าปลายทาง

ตั้งค่า **เปิดใช้งานอยู่**เป็น **ใช่** เพื่อส่งไฟล์เอาท์พุททางอีเมล หลังจากที่เปิดใช้งานตัวเลือกนี้ คุณสามารถระบุผู้รับอีเมลและแก้ไขชื่อเรื่องและเนื้อหาอีเมลได้ คุณสามารถตั้งค่าข้อความค่าคงที่สำหรับชื่อเรื่องและเนื้อหาอีเมล หรือคุณสามารถใช้ [สูตร](er-formula-language.md) ER เพื่อสร้างข้อความอีเมลแบบไดนามิกได้ 

คุณสามารถตั้งค่าคอนฟิกที่อยู่อีเมลสำหรับ ER ได้สองวิธี คุณสามารถดำเนินการตั้งค่าคอนฟิกให้เสร็จสมบูรณ์ได้ในลักษณะเดียวกับที่ใช้คุณสมบัติการจัดการการพิมพ์ หรือคุณสามารถแก้ไขที่อยู่อีเมลโดยใช้การอ้างอิงโดยตรงกับการตั้งค่าคอนฟิก ER ผ่านสูตร

[![เปิดใช้งานปลายทางของอีเมล](./media/ER_Destinations-EnableSingleDestination.png)](./media/ER_Destinations-EnableSingleDestination.png)

## <a name="email-address-types"></a>ชนิดของที่อยู่อีเมล

เมื่อคุณเลือก **แก้ไข** ในฟิลด์ **ถึง** หรือ **Cc** กล่องโต้ตอบ **อีเมลถึง** จะปรากฏขึ้น จากนั้นคุณสามารถเลือกชนิดของที่อยู่อีเมลที่จะใช้ **อีเมลการตั้งค่าคอนฟิก** และ **การจัดการการพิมพ์** ได้รับการสนับสนุนในขณะนี้

[![เลือกชนิดของอีเมล](./media/ER_Destinations-EmailSelectAddressType.png)](./media/ER_Destinations-EmailSelectAddressType.png)

### <a name="print-management"></a>การจัดการงานพิมพ์

ถ้าคุณเลือกชนิดอีเมล **การจัดการการพิมพ์** คุณสามารถป้อนที่อยู่อีเมลถาวรในฟิลด์ **ถึง** 

[![ตั้งค่าคอนฟิกที่อยู่อีเมลที่คงที่](./media/ER_Destinations-EmailFixedAddress.png)](./media/ER_Destinations-EmailFixedAddress.png)

เมื่อต้องการใช้ที่อยู่อีเมลที่คุณยังไม่ได้แก้ไข คุณต้องเลือกชนิดแหล่งที่มาของอีเมลสำหรับปลายทางของไฟล์ ค่าต่อไปนี้ได้รับการสนับสนุน: **ลูกค้า** **ผู้จัดจำหน่าย** **ผู้ที่มีแนวโน้มจะเป็นลูกค้า** **ผู้ติดต่อ** **คู่แข่ง** **ผู้ปฏิบัติงาน** **ผู้สมัคร** **ผู้ที่มีแนวโน้มจะเป็นผู้จัดจำหน่าย**และ **ผู้จัดจำหน่ายที่ไม่ได้รับอนุญาต** หลังจากที่คุณเลือกชนิดแหล่งที่มาของอีเมลแล้ว ให้ใช้ปุ่มที่อยู่ติดกับฟิลด์ **อีเมลบัญชีต้นทาง** เพื่อเปิดแบบฟอร์ม **โปรแกรมออกแบบสูตร** คุณสามารถใช้แบบฟอร์มนี้เพื่อแนบสูตรที่ส่งคืนขณะรันไทม์ **บัญชีฝ่าย** ของชนิดแหล่งที่มาที่เลือกจากเอกสารที่ประมวลผลไปยังปลายทางอีเมล

[![ตั้งค่าคอนฟิกบัญชีแหล่งที่มาของอีเมล](./media/ER_Destinations-EmailDefineAddressSource.png)](./media/ER_Destinations-EmailDefineAddressSource.png)

สูตรการตั้งค่าคอนฟิก ER โดยเฉพาะ ในฟิลด์ **สูตร** ให้ป้อนการอ้างอิงเฉพาะเอกสารไปยังลูกค้าหรือชนิดของฝ่ายผู้จัดจำหน่าย แทนที่จะพิมพ์ คุณสามารถค้นหาโหนดแหล่งข้อมูลที่แสดงถึงบัญชีลูกค้าหรือผู้จัดจำหน่าย และจากนั้น เลือก **เพิ่มแหล่งข้อมูล** เพื่อปรับปรุงสูตร ตัวอย่างเช่น ถ้าคุณใช้การตั้งค่าคอนฟิก **การโอนย้ายเครดิต ISO 20022** โหนดที่แสดงบัญชีผู้จัดจำหน่ายคือ `'\$PaymentsForCoveringLetter'.Creditor.Identification.SourceID`

ถ้าคุณป้อนค่าสตริงเช่น `"DE-001"` และบันทึกสูตร จะมีการส่งอีเมลไปยังผู้ติดต่อของผู้จัดจำหน่าย **DE-001**


[![หน้าตัวออกแบบสูตร ER](./media/ER_Destinations-EmailDefineAddressSourceFormula.png)](./media/ER_Destinations-EmailDefineAddressSourceFormula.png)

[![ตั้งค่าคอนฟิกบัญชีแหล่งที่มาของอีเมล](./media/ER_Destinations-EmailDefineAddressSourceAttributes.png)](./media/ER_Destinations-EmailDefineAddressSourceAttributes.png)



### <a name="configuration-email"></a>อีเมลการตั้งค่าคอนฟิก

ใช้ชนิดอีเมลนี้ถ้าการตั้งค่าคอนฟิกที่คุณใช้มีโหนดในแหล่งมาของข้อมูลที่ส่งคืน **ที่อยู่อีเมล** คุณสามารถใช้แหล่งข้อมูลและฟังก์ชันในโปรแกรมออกแบบสูตรเพื่อดูที่อยู่อีเมลที่จัดรูปแบบอย่างถูกต้อง ตัวอย่างเช่น ถ้าคุณใช้การตั้งค่าคอนฟิก **การโอนย้ายเครดิต ISO 20022** โหนดที่แสดงที่อยู่อีเมลของผู้ติดต่อของผู้จัดจำหน่าย คือ `'$PaymentsForCoveringLetter'.Creditor.ContactDetails.Email`

[![ตั้งค่าคอนฟิกแหล่งที่มาของอีเมล](./media/ER_Destinations-EmailDefineAddressSource2.png)](./media/ER_Destinations-EmailDefineAddressSource2.png)

## <a name="additional-resources"></a>แหล่งข้อมูลเพิ่มเติม

- [ภาพรวมการรายงานทางอิเล็กทรอนิกส์ (ER)](general-electronic-reporting.md)
- [ปลายทางการรายงานทางอิเล็กทรอนิกส์ (ER)](electronic-reporting-destinations.md)
- [โปรแกรมออกแบบสูตรในการรายงานทางอิเล็กทรอนิกส์ (ER)](general-electronic-reporting-formula-designer.md)
