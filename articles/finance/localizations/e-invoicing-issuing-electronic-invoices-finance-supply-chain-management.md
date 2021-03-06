---
title: การออกใบแจ้งหนี้อิเล็กทรอนิกส์ใน Finance and Supply Chain Management
description: หัวข้อนี้จะอธิบายวิธีการออกใบแจ้งหนี้อิเล็กทรอนิกส์ใน Microsoft Dynamics 365 Finance และ Dynamics 365 Supply Chain Management ผ่านส่วนเสริมการออกใบแจ้งหนี้อิเล็กทรอนิกส์
author: gionoder
manager: AnnBe
ms.date: 01/28/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.custom: 97423
ms.assetid: ''
ms.search.region: Global
ms.author: janeaug
ms.search.validFrom: 2020-07-08
ms.dyn365.ops.version: AX 10.0.12
ms.openlocfilehash: 187f5a20d088b4fcd7af2a6576357a69c2efc2c6
ms.sourcegitcommit: e88c96d1cb817a22db81856cadb563c095ab2671
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 02/02/2021
ms.locfileid: "5104444"
---
# <a name="issue-electronic-invoices-in-finance-and-supply-chain-management"></a>การออกใบแจ้งหนี้อิเล็กทรอนิกส์ใน Finance and Supply Chain Management

[!include [banner](../includes/banner.md)]

[!include [banner](../includes/preview-banner.md)]

หัวข้อนี้จะอธิบายวิธีการออกใบแจ้งหนี้อิเล็กทรอนิกส์ใน Microsoft Dynamics 365 Finance และ Dynamics 365 Supply Chain Management ผ่านส่วนเสริมการออกใบแจ้งหนี้อิเล็กทรอนิกส์


## <a name="feature-activation"></a>การเปิดใช้งานคุณลักษณะ

เมื่อต้องการเริ่มต้นการออกใบแจ้งหนี้ทางอิเล็กทรอนิกส์โดยใช้ส่วนเสริมการออกใบแจ้งหนี้ทางอิเล็กทรอนิกส์ คุณจําเป็นต้องเรียกใช้การอ้างอิงคุณลักษณะใน Finance and Supply Chain Management.

ข้อมูลอ้างอิงคุณลักษณะแต่ละข้อมูลจะสอดคล้องกับคุณลักษณะการออกใบแจ้งหนี้ทางอิเล็กทรอนิกส์เฉพาะ ซึ่งเป็นไปตามข้อกำหนดของการออกใบแจ้งหนี้ทางอิเล็กทรอนิกส์จากประเทศ/ภูมิภาคหนึ่งๆ

ตารางต่อไปนี้แสดงรายการคุณลักษณะ References ที่โปรแกรมเสริมการออกใบแจ้งหนี้อิเล็กทรอนิกส์รองรับ

| การอ้างอิงคุณลักษณะ | ชื่อ                                              | ประเทศ/ภูมิภาค |
|-------------------|---------------------------------------------------|----------------|
| BR-00053          | NF-e Federal - ใบแจ้งหนี้อิเล็กทรอนิกส์ของบราซิล       | บราซิล         |
| BR-00095          | ใบแจ้งหนี้อิเล็กทรอนิกส์ของบราซิล NFS-e               | บราซิล         |
| DK-00001          | การออกใบแจ้งหนี้อิเล็กทรอนิกส์ให้กับภาครัฐ (OIOUBL) - DK    | เดนมาร์ก        |
| EG-00008          | การออกใบแจ้งหนี้อิเล็กทรอนิกส์สำหรับอียิปต์                             | อียิปต์          |
| ES-00025          | ใบแจ้งหนี้ทางอิเล็กทรอนิกส์ไปยังภาครัฐ           | สเปน          |
| EUR-00023         | การออกใบแจ้งหนี้อิเล็กทรอนิกส์ของสหภาพยุโรปให้กับภาครัฐ       | ยุโรป         |
| ITA-00036         | IT - การออกใบแจ้งหนี้อิเล็กทรอนิกส์สู่ภาครัฐ (FatturaPA) | อิตาลี          |
| MX-00010          | การออกใบแจ้งหนี้อิเล็กทรอนิกส์ CFDIE                                  | เม็กซิโก         |
| MX-00016          | E-invoicing CFDI - กระบวนการยกเลิก           | เม็กซิโก         |

ในกรณีที่มีคุณลักษณะการออกใบแจ้งหนี้ทางอิเล็กทรอนิกส์แบบเดิมที่สนับสนุนขอบเขตการแปลเป็นภาษาท้องถิ่น การเรียกใช้งานข้อมูลอ้างอิงคุณลักษณะจะะช่วยให้สามารถออกใบแจ้งหนี้อิเล็กทรอนิกส์ผ่านส่วนเสริมการออกใบแจ้งหนี้อิเล็กทรอนิกส์และปิดคุณลักษณะก่อนหน้า

## <a name="submit-electronic-documents"></a>ส่งเอกสารอิเล็กทรอนิกส์

กระบวนการส่งเอกสารอิเล็กทรอนิกส์แสดงถึงการสื่อสารจุดเดียวระหว่างการจัดการด้านการเงินและซัพพลายเชนและส่วนเสริมของการออกใบแจ้งหนี้ทางอิเล็กทรอนิกส์ ระหว่างเหตุการณ์การส่งแต่ละเหตุการณ์ ขั้นตอนการสื่อสารในทั้งสองทิศทาง

- **จากการจัดการด้านการเงินและซัพพลายเชนไปยัง Add-on การออกใบแจ้งหนี้ทางอิเล็กทรอนิกส์** - การจัดการด้านการเงินและซัพพลายเชนส่งใบแจ้งหนี้ที่เป็นนามธรรมไปยังส่วนเสริมการออกใบแจ้งหนี้อิเล็กทรอนิกส์ นอกจากนี้ ยังมีการส่งเนื้อหาของตัวแปรที่ตั้งค่าคอนฟิกไว้เป็นส่วนหนึ่งของคุณลักษณะการออกใบแจ้งหนี้ทางอิเล็กทรอนิกส์ตามที่ต้องการด้วย
- **จาก Add-on การออกใบแจ้งหนี้ทางอิเล็กทรอนิกส์ไปยังการจัดการด้านการเงินและซัพพลายเชน** –ขึ้นอยู่กับคุณลักษณะของใบแจ้งหนี้ทางอิเล็กทรอนิกส์ การจัดการด้านการเงินและซัพพลายเชน จะได้รับการอัพเดตจากส่วนเสริมการออกใบแจ้งหนี้ทางอิเล็กทรอนิกส์เกี่ยวกับผลการประมวลผลของใบแจ้งหนี้ที่ส่งไปก่อนหน้านี้ นอกจากนี้ ยังได้รับเนื้อหาของตัวแปรที่ตั้งค่าคอนฟิกไว้เป็นส่วนหนึ่งของคุณลักษณะการออกใบแจ้งหนี้ทางอิเล็กทรอนิกส์ตามที่ต้องการด้วย

เมื่อต้องการส่งเอกสารอิเล็กทรอนิกส์ไปยังส่วนเสริมการออกใบแจ้งหนี้ทางอิเล็กทรอนิกส์ ในการจัดการด้านการเงินและซัพพลายเชน ให้ไป ที่ **การจัดการองค์กร &gt; เป็นระยะ &gt; เอกสารอิเล็กทรอนิกส์ &gt; ส่งเอกสารอิเล็กทรอนิกส์**

จุดเริ่มต้นคือใบแจ้งหนี้ที่ลงรายการบัญชีแล้ว ใบแจ้งหนี้นี้สามารถมาจากจุดเริ่มต้นที่ต่างกัน เช่น ใบสั่งขาย ใบแจ้งหนี้โครงการ หรือใบแจ้งหนี้ข้อความอิสระ

กระบวนการส่งสามารถดำเนินการด้วยตนเองหรือตามขั้นตอนได้

- **การดำเนินการด้วยตนเอง** – หากต้องการปฏิบัติการด้วยตนเอง คุณต้องใช้ตัวเลือก **ตัวกรอง** เพื่อกำหนดขอบเขตของเอกสารที่ต้องส่ง ในหน้า **ตัวกรอง** คุณสามารถตั้งค่าคอนฟิกการสอบถามของคุณเองเพื่อเลือกใบแจ้งหนี้ที่ลงรายการบัญชีซึ่งต้องส่ง หลังจากเลือกแล้ว คุณต้องเริ่มต้นการดำเนินการประมวลผลด้วยตนเองและรอให้การดำเนินการเสร็จสิ้น เมื่อการประมวลผลเสร็จสมบูรณ์แล้ว ข้อความในศูนย์การดำเนินการจะแสดงจํานวนของเอกสารอิเล็กทรอนิกส์ที่ส่งเรียบร้อยแล้ว
- **การดำเนินการบนพื้นหลัง** – การดำเนินการตามขั้นตอนสามารถทำได้โดยที่คุณไม่จำเป็นต้องล็อกอิน หรือเปิดกล่องโต้ตอบการส่งไว้ คุณสามารถจัดกําหนดการกระบวนการที่จะดำเนินการและกําหนดความถี่ของการดำเนินการได้

## <a name="view-the-submission-logs"></a>ดูล็อกการส่ง

ใน Finance and Supply Chain Management คุณสามารถใช้ล็อกการส่งเพื่อดูผลลัพธ์ของการประมวลผลที่ส่งไปยังส่วนเสริมการออกใบแจ้งหนี้ทางอิเล็กทรอนิกส์ได้ ไปที่ **การจัดการองค์กร &gt; เป็นระยะ &gt; เอกสารอิเล็กทรอนิกส์ &gt; การส่งเอกสารอิเล็กทรอนิกส์** และจากนั้น ในฟิลด์ **ประเภทเอกสาร** เลือกค่าเพื่อกรองชนิดของใบแจ้งหนี้ที่ล็อกแสดง

สถานะการส่งมีสามสถานะดังนี้

- **มีกำหนดการอยู่** – คุณได้รับการออกใบแจ้งหนี้ทางอิเล็กทรอนิกส์ส่วนเสริมที่ส่งมาจาก Finance and Supply Chain Management และกระบวนการออกใบแจ้งหนี้ทางอิเล็กทรอนิกส์ตามคุณลักษณะจะเริ่มต้นขึ้น
- **เสร็จสมบูรณ์** – การออกใบแจ้งหนี้ทางอิเล็กทรอนิกส์ส่วนเสริมได้ดำเนินการเสร็จเรียบร้อยแล้ว ตามคุณลักษณะการออกใบแจ้งหนี้ทางอิเล็กทรอนิกส์ที่ตั้งค่าคอนฟิกไว้
- **ล้มเหลว** – การออกใบแจ้งหนี้ทางอิเล็กทรอนิกส์ส่วนเสริมเกิดข้อผิดพลาดหรือหยุดทำงานโดยข้อยกเว้นในระหว่างการดำเนินการตามคุณลักษณะการออกใบแจ้งหนี้ทางอิเล็กทรอนิกส์

> [!IMPORTANT]
> สถานะการส่งหมายถึงสถานะของขั้นตอนที่การออกใบแจ้งหนี้ทางอิเล็กทรอนิกส์ส่วนเสริมใช้ตามคุณลักษณะการออกใบแจ้งหนี้ทางอิเล็กทรอนิกส์ การดำเนินการนี้ไม่ได้เป็นสถานะสุดท้ายของใบแจ้งหนี้อิเล็กทรอนิกส์
>
> ตัวอย่างเช่น ถ้าต้องส่งใบแจ้งหนี้อิเล็กทรอนิกส์ไปที่เว็บเซอร์วิสภายนอกเพื่อการอนุมัติ สถานะการส่งอาจเป็น **เสร็จสมบูรณ์** แต่สถานะของใบแจ้งหนี้อิเล็กทรอนิกส์อาจเป็น **ปฏิเสธแล้ว** ในกรณีนี้ การออกใบแจ้งหนี้อิเล็กทรอนิกส์ส่วนเสริมจะสามารถออกใบแจ้งหนี้อิเล็กทรอนิกส์ได้โดยสมบูรณ์เสมือนมีการตั้งค่าการดำเนินการนั้นไว้ อย่างไรก็ตาม ใบแจ้งหนี้อิเล็กทรอนิกส์จะถูกปฏิเสธได้จากสาเหตุที่ใบแจ้งหนี้นั้นไม่ตรงกับเกณฑ์ที่บริการเว็บตั้งค่าไว้เพื่อการอนุมัติใบแจ้งหนี้

ล็อกการส่งมีฟังก์ชันเพิ่มเติมดังต่อไปนี้:

- **รายละเอียดการส่ง** – ดูรายละเอียดของการส่งหลัก การแสดงภาพจะแสดงล็อกการปฏิบัติการที่สมบูรณ์ของการปฏิบัติการที่ตั้งค่าคอนฟิกไว้ในคุณลักษณะการออกใบแจ้งหนี้ทางอิเล็กทรอนิกส์ และยังอนุญาตให้ผู้ใช้ดาวน์โหลดไฟล์ที่สร้างขึ้นในระหว่างการดำเนินการได้ ในสถานการณ์ที่ใบแจ้งหนี้ต้องได้รับการอนุมัติจากเว็บเซอร์วิสภายนอก ขั้นตอนนี้จะเปิดโอกาสให้ผู้ใช้สามารถดูสถานะของใบแจ้งหนี้ได้
- **การส่งที่เกี่ยวข้อง** – ดูรายละเอียดของการส่งข้อมูลรอง
- **ยกเลิกการส่ง** – ฟังก์ชันนี้จะเปิดใช้งานกระบวนการส่งพิเศษในสถานการณ์ที่ใบแจ้งหนี้อิเล็กทรอนิกส์ต้องได้รับอนุมัติโดยบริการเว็บภายนอก กระบวนการนี้จะสั่งให้การออกใบแจ้งหนี้ทางอิเล็กทรอนิกส์ส่วนเพิ่มส่งข้อความเฉพาะไปยังบริการเว็บ เพื่อยกเลิกสถานะของใบแจ้งหนี้อิเล็กทรอนิกส์ที่อนุมัติแล้วในฐานข้อมูลของบริการเว็บ
- **ส่งเอกสารอีกครั้ง** – ส่งเอกสารอิเล็กทรอนิกส์ที่ส่งไปยังการออกใบแจ้งหนี้ทางอิเล็กทรอนิกส์ส่วนเพิ่มแล้วอีกครั้ง ล็อกใหม่ทั้งหมดจะถูกสร้างขึ้นในหน้า **รายละเอียดการส่ง**
- **ส่งการส่งที่เกี่ยวข้อง**
