---
title: การส่งข้อความทางอิเล็กทรอนิกส์
description: บทความนี้ให้ภาพรวมและข้อมูลการตั้งค่าสำหรับการส่งข้อความอิเล็กทรอนิกส์ใน Microsoft Dynamics 365 Finance
author: AdamTrukawka
ms.date: 01/04/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: atrukawk
ms.search.validFrom: 2018-10-28
ms.dyn365.ops.version: 8.0999999999999996
ms.openlocfilehash: 3e2fe6a70d449adea07f5aa0db9e625f0378d8c2
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 08/12/2022
ms.locfileid: "9283468"
---
# <a name="electronic-messaging"></a>การส่งข้อความทางอิเล็กทรอนิกส์

[!include [banner](../includes/banner.md)]

บทความนี้แสดงข้อมูลเกี่ยวกับภาพรวมและข้อมูลการตั้งค่าฟังก์ชัน **ข้อความทางอิเล็กทรอนิกส์** (EM)

ล่าสุด รัฐบาลและหน่วยงานทางกฎหมายของประเทศและภูมิภาคทั่วโลกต่างๆ มีการใช้ข้อกำหนดของรายงานสำหรับบริษัทที่ลงทะเบียนในประเทศหรือภูมิภาคเหล่านั้น วัตถุประสงค์ของข้อกำหนดคือ เพื่อเปิดใช้งานข้อมูลให้ได้รับจากบริษัทเหล่านั้นในรูปแบบอิเล็กทรอนิกส์ โดยตรงจากระบบที่จะถูกนำมาพิจารณา จัดเก็บ และประมวลผล

ฟังก์ชัน EM ใน Microsoft Dynamics 365 Finance รองรับกระบวนการต่างๆ สำหรับการดำเนินการระหว่างกันระหว่าง Finance และระบบที่รัฐบาลและหน่วยงานทางกฎหมายเสนอสำหรับการรายงาน การส่ง และการรับข้อมูลอย่างเป็นทางการ

มีการรวมฟังก์ชัน EM เข้ากับโมดูล **การรายงานทางอิเล็กทรอนิกส์** (ER) คุณสามารถตั้งค่ารูปแบบ ER สำหรับข้อความอิเล็กทรอนิกส์ได้ สำหรับข้อมูลเพิ่มเติม โปรดดู [การรายงานทางอิเล็กทรอนิกส์ (ER)](/dynamics365/unified-operations/dev-itpro/analytics/general-electronic-reporting)

## <a name="basic-concepts-for-em-functionality"></a>แนวคิดพื้นฐานเกี่ยวกับฟังก์ชัน EM

ฟังก์ชัน EM จะขึ้นอยู่กับเอนทิตีต่อไปนี้

- **ข้อความอิเล็กทรอนิกส์** – รายงานหรือการรายงานที่ควรรายงานหรือส่งผ่านเป็นการภายใน เช่น รายงานที่ส่งไปที่สํานักงานภาษี
- **รายการข้อความอิเล็กทรอนิกส์** – เรกคอร์ดที่ควรรวมอยู่ในข้อความที่มีการรายงาน
- **การประมวลผลข้อความอิเล็กทรอนิกส์** – ห่วงโซ่ของการดำเนินการที่ควรถูกรันให้สะสมข้อมูลที่ต้องการ สร้างรายงาน จัดเก็บข้อมูลในที่จัดเก็บ Azure Blob ส่งรายงานภายนอกระบบ รับการตอบจากภายนอกระบบ และเป็นไปตามข้อมูลที่ได้รับ ปรับปรุงฐานข้อมูล การดำเนินการในห่วงโซ่สามารถถูกเชื่อมโยง หรือไม่ถูกเชื่อมโยง

ภาพประกอบต่อไปนี้แสดงโฟลว์ข้อมูลของ EM

![โฟลว์ข้อมูลการส่งข้อความอิเล็กทรอนิกส์](media/electronic-messaging-data-flow.png)

## <a name="scenarios-supported-by-the-em-functionality"></a>สถานการณ์ที่สนับสนุนโดยฟังก์ชัน EM

ฟังก์ชันของข้อความอิเล็กทรอนิกส์สนับสนุนสถานการณ์จำลองต่อไปนี้:

- สร้างข้อความด้วยตนเอง และสร้างรายงานที่ขึ้นอยู่กับรูปแบบ ER การส่งออกที่เกี่ยวข้องของชนิดที่หลากหลาย ชนิดต่างๆ เหล่านี้ เช่น Microsoft Excel, XML, JavaScript Object Notation (JSON), PDF, text และ Microsoft Word
- สร้างและประมวลผลข้อความโดยอัตโนมัติโดยขึ้นอยู่กับข้อมูลที่มีการร้องขอและได้รับจากหน่วยงาน โดยใช้รูปแบบ ER การนำเข้าซึ่งเชื่อมโยง
- รวบรวม และประมวลผลข้อมูลจากแหล่งข้อมูลเป็นรายการข้อความ แหล่งข้อมูลเป็นตาราง Finance
- เก็บข้อมูลเพิ่มเติม และประเมินค่าต่างๆ โดยการเรียกคลาสที่สามารถดำเนินการได้ที่กำหนดไว้โดยเฉพาะ ซึ่งสัมพันธ์กับข้อความหรือรายการข้อความ
- รวมข้อมูลที่รวบรวมในรายการข้อความ แบ่งข้อมูลนั้นตามข้อความ และสร้างรายงานที่อยู่ในรูปแบบ ER ที่ส่งออกซึ่งเชื่อมโยง
- ส่งรายงานที่ถูกสร้างไปยังเว็บเซอร์วิสโดยใช้ข้อมูลความปลอดภัยที่จัดเก็บใน Azure Key Vault
- รับการตอบสนองจากเว็บเซอร์วิส แปลการตอบสนอง และอัพเดตข้อมูลใน Finance ตามความเหมาะสม
- จัดเก็บ และตรวจทานรายงานทั้งหมดที่สร้างขึ้น
- จัดเก็บ และตรวจทานข้อมูลล็อกทั้งหมดที่เกี่ยวข้องกับการดำเนินการที่ทำงานให้ข้อความหรือรายการข้อความ
- ควบคุมการประมวลผลโดยใช้สถานะข้อความและสถานะรายการข้อความต่างๆ

## <a name="security-privileges"></a>สิทธิ์ความปลอดภัย

สิทธิ์ความปลอดภัยต่อไปนี้จะพร้อมใช้งานเฉพาะกับข้อความอิเล็กทรอนิกส์

| สิทธิ์ความปลอดภัย           | ระดับการเข้าถึง | การเชื่อมโยง |
|------------------------------|--------------|-------------|
| รักษาข้อความทางอิเล็กทรอนิกส์ | สิทธิ์นี้ให้สิทธิ์เข้าถึงฟังก์ชัน EM อย่างเต็มรูปแบบ ถ้าคุณมีสิทธิ์นี้ คุณสามารถตั้งค่าข้อความอิเล็กทรอนิกส์และเรียกใช้การประมวลผลทั้งหมดได้ | สิทธิ์นี้จะรวมอยู่ในหน้าที่ด้านความปลอดภัย **รักษาธุรกรรมภาษีขาย** หน้าที่นั้นรวมอยู่ในบทบาทความปลอดภัย **นักบัญชี** |
| ดูข้อความทางอิเล็กทรอนิกส์     | สิทธิ์นี้ให้สิทธิ์เข้าถึงฟังก์ชัน EM แบบอ่านอย่างเดียว ถ้าคุณมีสิทธิ์นี้ คุณสามารถดูการตั้งค่าการส่งข้อความทางอิเล็กทรอนิกส์และข้อความ อย่างไรก็ตาม คุณไม่สามารถตั้งค่าหรือเรียกใช้ใดๆ ได้ | สิทธิ์นี้จะรวมอยู่ในหน้าที่ด้านความปลอดภัย **สอบถามเกี่ยวกับสถานะธุรกรรมภาษีขาย** หน้าที่นั้นรวมอยู่ในบทบาทความปลอดภัยต่อไปนี้:<ul><li>ผู้จัดการฝ่ายเรียกเก็บเงิน</li><li>เจ้าหน้าที่บัญชีลูกหนี้</li><li>ผู้จัดการฝ่ายบัญชีลูกหนี้</li><li>นักบัญชีภาษี</li><li>นักบัญชี</li><li>ผู้จัดการฝ่ายบัญชี</li><li>หัวหน้างานฝ่ายบัญชี</li><li>ผู้จัดการฝ่ายขาย</li><li>เจ้าหน้าที่บัญชีเจ้าหนี้</li></ul> |
| ดำเนินงานข้อความทางอิเล็กทรอนิกส์  | สิทธิ์นี้จะให้สิทธิ์การเข้าถึงหน้า **ข้อความทางอิเล็กทรอนิกส์** และ **รายการข้อความทางอิเล็กทรอนิกส์** เท่านั้น ถ้าคุณมีสิทธิ์นี้ คุณสามารถเรียกใช้การประมวลผลทั้งหมดที่เรียกจากหน้าเหล่านั้น | สิทธิ์นี้รวมอยู่ในหน้าที่ด้านความปลอดภัย **ดำเนินการข้อความทางอิเล็กทรอนิกส์** หน้าที่นั้นรวมอยู่ในบทบาทความปลอดภัย **ตัวดำเนินการข้อความทางอิเล็กทรอนิกส์** |

## <a name="country-specific-regulatory-features-supported-by-the-em-functionality"></a>คุณลักษณะการทำงานบังคับเฉพาะประเทศที่สนับสนุนโดยฟังก์ชัน EM

ตารางต่อไปนี้แสดงข้อมูลเกี่ยวกับคุณลักษณะการทำงานบังคับเฉพาะประเทศที่สนับสนุนโดยฟังก์ชัน EM

| ประเทศ     | ชื่อคุณลักษณะ | การบันทึกสาธิตคุณลักษณะการทำงาน |
|-------------|--------------|------------------------|
| สเปน       | [การจัดหาข้อมูลเกี่ยวกับ VAT ทันที (Summediato de Información del IVA, SII)](../localizations/emea-esp-sii.md) | |
| ฮังการี     | [ระบบออกใบแจ้งหนี้ออนไลน์](../localizations/emea-hun-online-invoicing.md) | |
| สหราชอาณาจักร | [การทำภาษีดิจิทัล (MTD) - การส่งใบแจ้งยอด VAT](../localizations/emea-gbr-mtd-vat-integration.md) | [การเงินและการดำเนินงาน: UK Digital Tax - VAT Declaration In Dynamics 365](https://community.dynamics.com/365/b/techtalks/posts/finance-and-operations-uk-digital-tax-vat-declaration-in-dynamics-365) |
| ลิทัวเนีย   | [การรายงาน i.SAF](../localizations/emea-ltu-isaf.md) | |
| โปแลนด์      | [การรายงานภาษี VAT ที่มีทะเบียน (JPK_V7M, VDEK)](../localizations/emea-pol-vdek.md) | [Dynamics 365 Finance: SAF/JPK VAT Audit Registers](https://community.dynamics.com/365/b/techtalks/posts/dynamics-365-finance-saf-jpk-vat-audit-registers-june-4-2020) |
| เนเธอร์แลนด์ | [การรายงานภาษี VAT สำหรับประเทศเนเธอร์แลนด์](../localizations/emea-nl-vat-declaration-netherlands.md) | |
| สาธารณรัฐเช็ก | [การรายงานภาษี VAT](../localizations/emea-cze-vat-declaration-tax-declaration-model.md) | |
| บราซิล      | [SPED-Reinf](../localizations/latam-bra-sped-reinf-overview.md) | |
| รัสเซีย      | [การรายงานภาษี VAT](../localizations/rus-vat-declaration.md) | |
| รัสเซีย      | [การรายงานการบัญชีในรูปแบบอิเล็กทรอนิกส์](../localizations/rus-accounting-reporting.md) | |
| รัสเซีย      | [การรายงานภาษีกำไร](../localizations/rus-profit-tax-declaration.md) | |
| รัสเซีย      | [การรายงานภาษีที่ประเมิน](../localizations/rus-assessed-tax-declaration.md) | |
| รัสเซีย      | [การรายงานภาษีการขนส่ง](../localizations/rus-transport-tax-declaration.md) | |
| รัสเซีย      | [การรายงานภาษีที่ดิน](../localizations/rus-land-tax-declaration.md) | |
| นอร์เวย์      | [การส่งคืน VAT พร้อมด้วยการส่งโดยตรงไปที่ Altinn](../localizations/emea-nor-vat-return.md) | [การส่งคืน VAT ใหม่ที่มีการส่งโดยตรงไปที่ Altinn ใน Dynamics 365 Finance](https://community.dynamics.com/365/dynamics-365-fasttrack/b/techtalks/posts/new-vat-return-with-direct-submission-to-altinn-in-dynamics-365-finance-december-1-2021) |
| ฝรั่งเศส      | [การรายงานภาษี VAT (ฝรั่งเศส)](../localizations/emea-fra-VAT-declaration-preview-France.md) | |
| ออสเตรีย     | [การรายงานภาษี VAT (ออสเตรีย)](../localizations/emea-aut-vat-declaration-austria.md) | |
| เยอรมนี     | [การรายงานภาษี VAT (เยอรมนี)](../localizations/emea-deu-vat-declaration-germany.md) | |
| เนเธอร์แลนด์ | [การรายงานภาษี VAT สำหรับประเทศเนเธอร์แลนด์](../localizations/emea-nl-vat-declaration-netherlands.md) | |
| สวีเดน      | [การรายงานภาษี VAT (สวีเดน)](../localizations/emea-swe-VAT-declaration-Sweden.md) | |
| สวิตเซอร์แลนด์ | [การรายงานภาษี VAT (สวิตเซอร์แลนด์)](../localizations/emea-che-vat-declaration-switzerland.md) | |

[!INCLUDE[footer-include](../../includes/footer-banner.md)]


