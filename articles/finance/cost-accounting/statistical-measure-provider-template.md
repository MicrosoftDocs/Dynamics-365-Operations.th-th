---
title: ตัวให้บริการแม่แบบสำหรับสมาชิกมิติทางสถิติและตัวให้บริการการประเมินทางสถิติ
description: บทความนี้ให้ข้อมูลเกี่ยวกับสมาชิกมิติทางสถิติและเท็มเพลตผู้ให้บริการการประเมินทางสถิติ
author: AndersGirke
ms.date: 06/16/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: CAMCostAccountingLedgerSourceEntryProvider, CAMStatisticalDimension, CAMAXStatisticalMeasureProviderTemplate, CAMAXStatisticalMeasureProviderConfiguration, CAMStatisticalDimensionMember, CAMDataConnectorStatisticalMeasure, CAMImportedStatisticalMeasure, CAMImportedStatisticalMeasureProviderConfiguration
audience: Application User
ms.reviewer: twheeloc
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: twheeloc
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 55f4f1e93eb45530bed886bc46acd1420160eb38
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 06/03/2022
ms.locfileid: "8904656"
---
# <a name="provider-templates-for-statistical-dimension-members-and-measure-providers"></a>ตัวให้บริการแม่แบบสำหรับสมาชิกมิติทางสถิติและตัวให้บริการการประเมินทางสถิติ

[!include [banner](../includes/banner.md)]

มิติทางสถิติและสมาชิกถูกใช้ในการลงทะเบียน และควบคุมรายการที่ไม่ใช่เงินตราในการบัญชีต้นทุน สมาชิกของมิติทางสถิติสามารถถูกใช้สำหรับวัตถุประสงค์สองประการ:

- เป็นฐานการปันส่วนในนโยบาย เช่น การปันส่วนต้นทุน หรือการกระจายต้นทุน
- สำหรับการรายงานปริมาณการใช้ที่ไม่เกี่ยวกับเงินตรา

## <a name="statistical-dimension"></a>มิติทางสถิติ

มิติทางสถิติมีชื่อเฉพาะและชุดของสมาชิกมิติเฉพาะ มิติทางสถิติถูกกำหนดให้กับรหัสบัญชีแยกประเภทของการบัญชีต้นทุน ความสัมพันธ์นี้ผนวกสมาชิกมิติทางสถิติที่เกี่ยวข้องทั้งหมดไว้ในบัญชีแยกประเภทในการบัญชีต้นทุน ดังนั้น รายการสถิติทั้งหมดจะถูกสร้างในบริบทของบัญชีแยกประเภทของการบัญชีต้นทุน

> [!NOTE]
> มิติทางสถิติสามารถถูกกำหนดให้กับบัญชีแยกประเภทของการบัญชีต้นทุนมากกว่าหนึ่งรายการได้

นี่เป็นตัวอย่างของมิติทางสถิติ

| ชื่อ                        | ตัวเชื่อมต่อข้อมูลสำหรับสมาชิกมิติ |
|-----------------------------|--------------------------------------|
| องค์ประกอบทางสถิติที่ใช้ร่วมกัน | สมาชิกมิติที่นำเข้า           |

นี่เป็นตัวอย่างของมิติทางสถิติที่ได้มีการกำหนดให้กับบัญชีแยกประเภทในการบัญชีต้นทุน

| ชื่อ                  | สกุลเงินทางบัญชี | ชนิดอัตราแลกเปลี่ยน | ปฏิทินทางการเงิน | มิติองค์ประกอบต้นทุน | มิติทางสถิติ       |
|-----------------------|---------------------|--------------------|-----------------|------------------------|-----------------------------|
| การบัญชีด้านการจัดการ | USD                 | สกุลเงินคงที่  | รอบระยะเวลาทางบัญชี   | องค์ประกอบต้นทุนที่ใช้ร่วมกัน   | องค์ประกอบทางสถิติที่ใช้ร่วมกัน |

## <a name="statistical-dimension-members"></a>สมาชิกมิติทางสถิติ

สมาชิกของมิติทางสถิติแสดงถึงเอนทิตี้ที่คุณต้องการลงทะเบียนให้กับหน่วยวัดที่ไม่เกี่ยวกับเงินตรา หน่วยวัดเหล่านี้สามารถใช้เป็นฐานของการปันส่วน หรือเพื่อรายงานค่าที่ไม่เกี่ยวกับเงินตรา

สมาชิกของมิติทางสถิติสามารถถูกสร้างได้ด้วยตนเอง อีกทางหนึ่งคือ สามารถนำเข้าได้จากไฟล์ โดยใช้เครื่องมือการนำเข้า/ส่งออกการจัดการข้อมูล

สมาชิกของมิติทางสถิติกลายเป็นฐานการปันส่วนล่วงหน้าโดยอัตโนมัติ ซึ่งสามารถใช้เป็นฐานในนโยบายการปันส่วน หรือเป็นอินพุทในฐานการปันส่วนชนิดอื่น ๆ ได้

นี่คือตัวอย่างของสมาชิกของมิติทางสถิติโดยทั่วไป

| ชื่อมิติทางสถิติ  | องค์ประกอบทางสถิติ | คำอธิบาย             | หน่วย |
|-----------------------------|----------------------|-------------------------|------|
| องค์ประกอบทางสถิติที่ใช้ร่วมกัน | FTE                  | พนักงานเต็มเวลา     | Ea  |
| องค์ประกอบทางสถิติที่ใช้ร่วมกัน | ไฟฟ้า          | ปริมาณการใช้ไฟฟ้า | kWh  |
| องค์ประกอบทางสถิติที่ใช้ร่วมกัน | แพ็ค CC              | ศูนย์ต้นทุนบรรจุภัณฑ์   | ชม. |

## <a name="statistical-measure-provider-template"></a>เท็มเพลตผู้ให้บริการการประเมินทางสถิติ

หน่วยวัดทางสถิติสามารถมีต้นกำเนิดมาจากแหล่งข้อมูลหลายชนิด Dynamics 365 Finance เป็นเครื่องมือที่ดีในการแยกหน่วยวัดทางสถิติออกมา คุณสามารถใช้เท็มเพลตผู้ให้บริการหน่วยวัดทางสถิติ เพื่อตั้งค่าคอนฟิกหน่วยวัดทางสถิติที่คุณต้องการดึงข้อมูลได้อย่างง่ายดาย

คำนิยามของเท็มเพลตผู้ให้บริการหน่วยวัดทางสถิติคือ ทั่วไป และสามารถนำมาใช้ใหม่ได้ในสมาชิกของมิติทางสถิติต่าง ๆ

> [!NOTE]
> ตารางทั้งหมดที่ประกอบด้วยมิติทางการเงิน สามารถใช้เป็นแหล่งข้อมูลสำหรับการประเมินทางสถิติได้

**ตัวอย่าง: จำนวนพนักงานสำหรับศูนย์ต้นทุนแต่ละศูนย์**

จำนวนพนักงานต่อศูนย์ต้นทุน เป็นหน่วยวัดทางสถิติที่สามารถใช้สำหรับวัตถุประสงค์ต่าง ๆ ที่มีข้อมูลเชิงลึกด้านการจัดการ:

- หน่วยวัดการรายงานสถิติ โดยศูนย์ต้นทุน
- ฐานการปันส่วนสำหรับค่าใช้จ่ายชนิดต่าง ๆ
- อัตราต้นทุนภายในโดยศูนย์ต้นทุน:

    - ต้นทุนโดยพนักงาน
    - รายได้โดยพนักงาน

ตาราง HcmEmployment จัดเก็บรายการของพนักงานทั้งหมดในอินสแตนซ์ ตารางนี้เป็นตารางสากล ดังนั้น เรกคอร์ดจึงไม่เกี่ยวข้องกับรหัสพื้นที่ของข้อมูลเฉพาะ

นี่เป็นตัวอย่างของพนักงานในตาราง HcmEmployment

| ชื่อ       | ศูนย์ต้นทุน | คำอธิบาย   | ชนิดผู้ปฏิบัติงาน |
|------------|-------------|----|-------------|
| พนักงาน 1 | CC001       | ทรัพยากรบุคคล | พนักงาน    |
| พนักงาน 2 | CC002       | FI | พนักงาน    |
| พนักงาน 3 | CC002       | FI | พนักงาน    |
| พนักงาน 4 | CC003       | ไอที | พนักงาน    |
| พนักงาน 5 | CC003       | ไอที | พนักงาน    |
| พนักงาน 6 | CC002       | FI | ผู้รับเหมา  |

เมื่อคุณสร้างเรกคอร์ด **เท็มเพลตผู้ให้บริการหน่วยวัดทางสถิติ** คุณต้องตัดสินใจเลือกฟังก์ชันที่จะใช้:

- **การตรวจนับ** – จำนวนเรกคอร์ดต่อออบเจ็กต์ต้นทุนจะถูกโอนย้าย
- **ผลรวม** – ผลรวมสำหรับเรกคอร์ดต่อออบเจ็กต์ต้นทุนจะถูกโอนย้าย (ฟิลด์ **ผลรวม** และฟิลด์ **วันที่** จำเป็นต้องมี)

## <a name="using-the-count-function"></a>การใช้ฟังก์ชันการตรวจนับ

ตัวอย่างเช่น เท็มเพลตผู้ให้บริการหน่วยวัดทางสถิติสามารถถูกตั้งค่าเป็นดังนี้

| ชื่อ  | ฟังก์ชัน | ตารางต้นทาง  | ฟิลด์ผลรวม      | ฟิลด์วันที่     |
|-------|----------|---------------|----------------|----------------|
| FTEs  | จำนวน    | HcmEmployment | ใช้ไม่ได้ | ใช้ไม่ได้ |

คุณยังสามารถเพิ่มช่วงอย่างน้อยหนึ่งช่วง เพื่อจำกัดหน่วยวัดจากตารางต้นทาง

ในตัวอย่างนี้ ถ้าคุณต้องการนับจำนวนของพนักงานเต็มเวลาทั้งหมด (FTEs) คุณสามารถเพิ่มช่วงในฟิลด์ **ชนิดผู้ปฏิบัติงาน** ได้ ในฟิลด์ **เกณฑ์** เลือก **พนักงาน** เพื่อจำกัดช่วงของผลลัพธ์ดังต่อไปนี้

**ช่วง**

| ตารางต้นทาง  | ฟิลด์       | เกณฑ์ |
|---------------|-------------|----------|
| HcmEmployment | ชนิดผู้ปฏิบัติงาน | พนักงาน |

ก่อนที่คุณจะสามารถนำหน่วยวัดทางสถิติไปยังการบัญชีต้นทุนได้ คุณต้องสร้างความสัมพันธ์ระหว่างเท็มเพลตผู้ให้บริการการประเมินทางสถิติและสมาชิกมิติทางสถิติ ความสัมพันธ์นี้ถูกสร้างขึ้นสำหรับบัญชีแยกประเภทในการบัญชีต้นทุนและเวอร์ชันแต่ละรายการ ความสัมพันธ์ประกอบด้วย ตัวเชื่อมต่อข้อมูลและตัวให้บริการข้อมูล คุณสามารถมีตัวเชื่อมต่อข้อมูลและผู้ให้บริการข้อมูลได้หลายรายการสำหรับสมาชิกของมิติทางสถิติแต่ละราย

> [!NOTE]
> ในตัวอย่างนี้ เราจะสร้างความสัมพันธ์เฉพาะสำหรับ **เวอร์ชันจริง**

ไปยัง **บัญชีแยกประเภทในการบัญชีต้นทุน** \> **เวอร์ชันจริง** \> **จัดการ** \> **หน่วยวัดทางสถิติ** เพื่อสร้างความสัมพันธ์ สำหรับสถานการณ์จำลองนี้ เลือกตัวเชื่อมต่อ **Dynamics 365 Finance – การวัดทางสถิติ** เนื่องจากเราต้องการแยะข้อมูลออกมาจาก Finance

**แหล่งข้อมูล**

| ชื่อ        | ตัวเชื่อมต่อข้อมูล                                                                     | สมาชิกมิติทางสถิติ |
|-------------|------------------------------------------------------------------------------------|------------------------------|
| FTEs D365FO | Dynamics 365 Finance – การวัดทางสถิติ | FTEs                         |

**การตั้งค่าคอนฟิกผู้ให้บริการข้อมูล**

| ชื่อของเท็มเพลตทางสถิติ |
|---------------------------|
| FTEs                      |

หลังจากที่มีการประมวลผลข้อมูลแหล่งที่มาสำหรับหน่วยวัดทางสถิติ รายการทางสถิติต่อไปนี้จะถูกสร้างขึ้นในการบัญชีต้นทุน

**สมุดรายวัน**

| สมุดรายวัน | ชนิดสมุดรายวัน                       | รอบระยะเวลาปฏิทินทางการเงิน | ปี   |  รอบระยะเวลา  |  เวอร์ชัน | รายการต้นทางของตัวเชื่อมต่อข้อมูล|
|---------|------------------------------------|------------------------|--------|----------|----------|------------------------------|
| 00001   | สมุดรายวันการโอนย้ายรายการทางสถิติ | ทางการเงิน                 | 2017   | รอบระยะเวลา 1 | บัญชีแยกประเภทของ CA USMF | FTEs                   |

**รายการสมุดรายวันการโอนย้ายรายการทางสถิติ**

| วันที่ลงบัญชี | ขนาด | องค์ประกอบทางสถิติ |   คำอธิบาย       | ศูนย์ต้นทุน |
|-----------------|-----------|---------------------|---------------------|-------------|
| วันที่ 31-01-2017      | 1.00      | FTEs                | พนักงานเต็มเวลา | CC001       |
| วันที่ 31-01-2017      | 2.00      | FTEs                | พนักงานเต็มเวลา | CC002       |
| วันที่ 31-01-2017      | 2.00      | FTEs                | พนักงานเต็มเวลา | CC003       |

**รายการทางสถิติ**

| ออบเจ็กต์ต้นทุน |  คำอธิบาย  | วันที่ลงบัญชี | สมาชิกมิติทางสถิติ |  คำอธิบาย        | ขนาด |
|-------------|----|-----------------|------------------------------|---------------------|-----------|
| CC001       | ทรัพยากรบุคคล | วันที่ 31-01-2017      | FTEs                         | พนักงานเต็มเวลา | 1.00      |
| CC002       | FI | วันที่ 31-01-2017      | FTEs                         | พนักงานเต็มเวลา | 2.00      |
| CC003       | ไอที | วันที่ 31-01-2017      | FTEs                         | พนักงานเต็มเวลา | 2.00      |

ถ้ามีการมอบหมายฐานการปันส่วนสมาชิกของมิติที่กำหนดไว้ล่วงหน้าของ FTEs เป็นฐานการปันส่วนในกฎการกระจายต้นทุน จะมีการกระจายต้นทุนโดยใช้ตัวคูณการปันส่วนต่อไปนี้

| ออบเจ็กต์ต้นทุน | คำอธิบาย    | ขนาด | ตัวคูณการปันส่วน |
|-------------|----|-----------|-------------------|
| CC001       | ทรัพยากรบุคคล | 1.00      | (1/5) × ปริมาณ    |
| CC002       | FI | 2.00      | (2/5) × ปริมาณ    |
| CC003       | ไอที | 2.00      | (2/5) × ปริมาณ    |

## <a name="using-the-sum-function"></a>การใช้ฟังก์ชันผลรวม

ศูนย์ต้นทุนการผลิต CC010 (บรรจุภัณฑ์) รับผิดชอบการบรรจุผลิตภัณฑ์ก่อนมีการจัดส่งให้แก่ลูกค้า ต้นทุนค่าแรงโดยตรงจะถูกเพิ่มไปยังผลิตภัณฑ์ ผ่านทางรายการวัสดุและส่วนประกอบ (BOM) และกระบวนการผลิต ต้นทุนทางอ้อมของการรันศูนย์ต้นทุนต้องถูกปันส่วนไปยังผลิตภัณฑ์ที่ผลิตอีกด้วย หน่วยวัดทางสถิติที่ดีที่สุดสำหรับการปันส่วนนั้น มักจะเป็นจำนวนชั่วโมงการผลิตที่ลงทะเบียนสำหรับแต่ละผลิตภัณฑ์ ภายในรอบระยะเวลาที่กำหนด

ตาราง ProdRouteTrans จัดเก็บธุรกรรมแรงงานในการผลิตทั้งหมดต่อนิติบุคคล DataAreadID

นี่เป็นตัวอย่างของตาราง ProdRouteTrans

| ข้อมูลอ้างอิง        | หมายเลข | การดำเนินงาน | ชนิดข้อมูล | เวลา  | วันที่ตามจริง | กลุ่มผลิตภัณฑ์ (มิติทางการเงิน) | นิติบุคคล |
|------------------|--------|-----------|------|-------|---------------|-------------------------------------|--------------|
| ใบสั่งผลิต | P0001  | บรรจุภัณฑ์ | เวลา | 8.00  | วันที่ 01-01-2017    | น้ำส้ม B2B                    | USMF         |
| ใบสั่งผลิต | P0001  | บรรจุภัณฑ์ | เวลา | 8.00  | วันที่ 02-01-2017    | น้ำส้ม B2B                    | USMF         |
| ใบสั่งผลิต | P0002  | บรรจุภัณฑ์ | เวลา | 4.00  | วันที่ 03-01-2017    | ผู้บริโภคน้ำส้ม               | USMF         |
| ใบสั่งผลิต | P0003  | บรรจุภัณฑ์ | เวลา | 4.00  | วันที่ 03-01-2017    | ผู้บริโภคน้ำส้ม               | USMF         |
| ใบสั่งผลิต | P0004  | Reconst  | เวลา | 10.00 | วันที่ 03-01-2017    | ผู้บริโภคน้ำส้ม               | USMF         |

เมื่อคุณสร้างเรกคอร์ด **เท็มเพลตผู้ให้บริการหน่วยวัดทางสถิติ** คุณต้องตัดสินใจเลือกฟังก์ชันที่จะใช้:

- **การตรวจนับ** – จำนวนเรกคอร์ดต่อออบเจ็กต์ต้นทุนจะถูกโอนย้าย
- **ผลรวม** – ผลรวมสำหรับเรกคอร์ดต่อออบเจ็กต์ต้นทุนจะถูกโอนย้าย (ฟิลด์ **ผลรวม** และฟิลด์ **วันที่** จำเป็นต้องมี)

เท็มเพลตผู้ให้บริการหน่วยวัดทางสถิติสามารถถูกตั้งค่าเป็นดังต่อไปนี้

| ชื่อ    | ฟังก์ชัน | ตารางต้นทาง   | ฟิลด์ผลรวม | ฟิลด์วันที่    |
|---------|----------|----------------|-----------|---------------|
| แพ็ค CC | ผลรวม      | ProdRouteTrans | ชั่วโมง     | วันที่ตามจริง |

คุณยังสามารถเพิ่มช่วงได้อย่างน้อยหนึ่งช่วง เพื่อจำกัดหน่วยวัดจากตารางต้นทาง

ในตัวอย่างนี้ ถ้าคุณต้องการผลรวมของชั่วโมงที่เกี่ยวข้องกับศูนย์ต้นทุนบรรจุภัณฑ์ CC010 คุณสามารถเพิ่มช่วงในฟิลด์ **การดำเนินงาน** ได้ ในฟิลด์ **เกณฑ์** เลือก **บรรจุภัณฑ์** เพื่อจำกัดช่วงของผลลัพธ์

**ช่วง**

| ตารางต้นทาง   | ฟิลด์     | เกณฑ์  |
|----------------|-----------|-----------|
| ProdRouteTrans | การดำเนินงาน | บรรจุภัณฑ์ |

ก่อนที่คุณจะสามารถนำหน่วยวัดทางสถิติไปยังการบัญชีต้นทุนได้ คุณต้องสร้างความสัมพันธ์ระหว่างเท็มเพลตผู้ให้บริการการประเมินทางสถิติและสมาชิกมิติทางสถิติ ความสัมพันธ์นี้ถูกสร้างขึ้นสำหรับบัญชีแยกประเภทในการบัญชีต้นทุนและเวอร์ชันแต่ละรายการ ความสัมพันธ์ประกอบด้วย ตัวเชื่อมต่อข้อมูลและตัวให้บริการข้อมูล คุณสามารถมีตัวเชื่อมต่อข้อมูลและผู้ให้บริการข้อมูลได้หลายรายการสำหรับสมาชิกของมิติทางสถิติแต่ละราย

> [!NOTE]
> ในตัวอย่างนี้ เราจะสร้างความสัมพันธ์เฉพาะสำหรับ **เวอร์ชันจริง**

ไปยัง **บัญชีแยกประเภทในการบัญชีต้นทุน** \> **เวอร์ชันจริง** \> **จัดการ** \> **หน่วยวัดทางสถิติ** เพื่อสร้างความสัมพันธ์ สำหรับสถานการณ์จำลองนี้ เลือกตัวเชื่อมต่อ **Dynamics 365 Finance – การวัดทางสถิติ** เนื่องจากเราต้องการแยะข้อมูลออกมาจาก Finance

**แหล่งข้อมูล**

| ชื่อ           | ตัวเชื่อมต่อข้อมูล                                                                     | สมาชิกมิติทางสถิติ |
|----------------|------------------------------------------------------------------------------------|------------------------------|
| แพ็ค CC D365FO | Dynamics 365 Finance – การวัดทางสถิติ | แพ็ค CC                      |

ระบบรับรู้ว่า ProdRouteTrans เป็นตารางที่แต่ละเรกคอร์ดเป็นของนิติบุคคลที่แยกต่างหากกัน ดังนั้น ระบบจะขอให้คุณเลือกนิติบุคคลที่ควรนำเข้าธุรกรรม

**การตั้งค่าคอนฟิกผู้ให้บริการข้อมูล**

| ชื่อของเท็มเพลตทางสถิติ | นิติบุคคล |
|---------------------------|--------------|
| แพ็ค CC                   | USMF         |

หลังจากที่มีการประมวลผลข้อมูลแหล่งที่มาสำหรับการประเมินทางสถิติ รายการทางสถิติต่อไปนี้จะถูกสร้างขึ้นในการบัญชีต้นทุน

**สมุดรายวัน**

| สมุดรายวัน | ชนิดสมุดรายวัน                     | รอบระยะเวลาปฏิทินทางการเงิน | ปี   | รอบระยะเวลา | เวอร์ชัน   |   รายการต้นทางของตัวเชื่อมต่อข้อมูล  |
|---------|----------------------------------|------------------------|--------|---------|----------------|---------|
| 00002   | สมุดรายวันการโอนย้ายรายการทางสถิติ | ทางการเงิน               | 2017    | รอบระยะเวลา 1  | บัญชีแยกประเภทของ CA USMF | แพ็ค CC |

**รายการสมุดรายวันการโอนย้ายรายการทางสถิติ**

| วันที่ลงบัญชี | ขนาด | องค์ประกอบทางสถิติ |  คำอธิบาย          | กลุ่มผลิตภัณฑ์         |
|-----------------|-----------|---------------------|-----------------------|-----------------------|
| วันที่ 31-01-2017      | 16.00     | แพ็ค CC             | ศูนย์ต้นทุนบรรจุภัณฑ์ | น้ำส้ม B2B      |
| วันที่ 31-01-2017      | 8.00      | แพ็ค CC             | ศูนย์ต้นทุนบรรจุภัณฑ์ | ผู้บริโภคน้ำส้ม |

**รายการทางสถิติ**

| ออบเจ็กต์ต้นทุน           | วันที่ลงบัญชี | สมาชิกมิติทางสถิติ |    คำอธิบาย        | ขนาด |
|-----------------------|-----------------|------------------------------|-----------------------|-----------|
| น้ำส้ม B2B      | วันที่ 31-01-2017      | แพ็ค CC                      | ศูนย์ต้นทุนบรรจุภัณฑ์ | 16.00     |
| ผู้บริโภคน้ำส้ม | วันที่ 31-01-2017      | แพ็ค CC                      | ศูนย์ต้นทุนบรรจุภัณฑ์ | 8.00      |

ถ้ามีการมอบหมายฐานการปันส่วนสมาชิกของมิติที่กำหนดไว้ล่วงหน้าของแพ็ค CC เป็นฐานการปันส่วนในกฎการกระจายต้นทุน จะมีการกระจายต้นทุนโดยใช้ตัวคูณการปันส่วนต่อไปนี้

| ออบเจ็กต์ต้นทุน           | ขนาด | ตัวคูณการปันส่วน  |
|-----------------------|-----------|--------------------|
| น้ำส้ม B2B      | 16.00     | (16 ÷ 24) × ปริมาณ |
| ผู้บริโภคน้ำส้ม | 8.00      | (8 ÷ 24) × ปริมาณ  |

## <a name="imported-statistical-measures"></a>การประเมินทางสถิติที่นำเข้า

คุณสามารถนำเข้าหน่วยวัดทางสถิติไปในการบัญชีต้นทุน โดยใช้เครื่องมือการนำเข้า/ส่งออกการจัดการข้อมูล

เอนทิตี้ข้อมูลที่ถูกใช้สำหรับการนำเข้า จะถูกตั้งชื่อว่าหน่วยวัดทางสถิติที่นำเข้า

> [!NOTE]
> เอนทิตี้ข้อมูลนี้ถูกออกแบบมาเพื่ออนุญาตค่ามิติไม่ซ้ำกันสูงสุดห้าค่าสำหรับแต่ละรายการ

มีการบันทึกการใช้ไฟฟ้าในใน Microsoft Excel โดยใช้รูปแบบที่กำหนดไว้ของข้อมูลเอนทิตี นี่คือตัวอย่าง

| วันที่ลงบัญชี | ชื่อสมาชิกมิติ 1 | ชื่อสมาชิกมิติ 2 | ชื่อสมาชิกมิติ 5 | ขนาด  | ตัวระบุแหล่งที่มา |
|-----------------|------------------------|------------------------|------------------------|------------|-------------------|
| วันที่ 31-01-2017      | CC001                  |                        |                        | 2,450.00   | ไฟฟ้า       |
| วันที่ 31-01-2017      | CC002                  |                        |                        | 4,100.00   | ไฟฟ้า       |
| วันที่ 31-01-2017      | CC003                  |                        |                        | 15,000.00  | ไฟฟ้า       |

เมื่อคุณนำเข้าข้อมูลของคุณโดยใช้การจัดการข้อมูล ข้อมูลจะถูกเก็บไว้ในตารางการจัดเตรียมการบัญชีต้นทุน ดังนั้น ข้อมูลที่นำเข้าสามารถถูกใช้ในบัญชีแยกประเภทสำหรับการบัญชีต้นทุนหลายรายการ ไม่จำเป็นต้องมีการโหลดข้อมูลซ้ำ

เมื่อต้องการนำเข้าข้อมูล ไปที่ **ข้อมูลที่นำเข้า** \> **เอนทิตี้ข้อมูล** \> **หน่วยวัดทางสถิติที่นำเข้า**

| ตัวระบุแหล่งที่มา | วันที่ลงบัญชี | ขนาด  | ชื่อสมาชิกมิติ 1 | ชื่อสมาชิกมิติ 2 | ชื่อสมาชิกมิติ 5 |
|-------------------|-----------------|------------|------------------------|------------------------|------------------------|
| ไฟฟ้า       | วันที่ 31-01-2017      | 2,450.00   | CC001                  |                        |                        |
| ไฟฟ้า       | วันที่ 31-01-2017      | 4,100.00   | CC002                  |                        |                        |
| ไฟฟ้า       | วันที่ 31-01-2017      | 15,000.00  | CC003                  |                        |                        |

ก่อนที่คุณจะสามารถนำหน่วยวัดทางสถิติไปยังการบัญชีต้นทุน คุณต้องสร้างความสัมพันธ์ระหว่างตัวระบุแหล่งและสมาชิกมิติทางสถิติ ความสัมพันธ์นี้ถูกสร้างขึ้นสำหรับบัญชีแยกประเภทในการบัญชีต้นทุนและเวอร์ชันแต่ละรายการ ความสัมพันธ์ประกอบด้วย ตัวเชื่อมต่อข้อมูลและตัวให้บริการข้อมูล คุณสามารถมีตัวเชื่อมต่อข้อมูลและผู้ให้บริการข้อมูลได้หลายรายการสำหรับสมาชิกของมิติทางสถิติแต่ละราย

> [!NOTE]
> ในตัวอย่างนี้ เราจะสร้างความสัมพันธ์เฉพาะสำหรับ **เวอร์ชันจริง**

ไปยัง **บัญชีแยกประเภทในการบัญชีต้นทุน** \> **เวอร์ชันจริง** \> **จัดการ** \> **หน่วยวัดทางสถิติ** เพื่อสร้างความสัมพันธ์ สำหรับสถานการณ์จำลองนี้ เลือกตัวเชื่อมต่อข้อมูล **หน่วยวัดทางสถิติที่นำเข้า** เนื่องจากมีการนำเข้าข้อมูลเข้ามาจากระบบของบุคคลที่สามไปยังการบัญชีต้นทุนผ่านทาง Excel

**แหล่งข้อมูล**

| ชื่อ        | ตัวเชื่อมต่อข้อมูล                | สมาชิกมิติทางสถิติ |
|-------------|-------------------------------|------------------------------|
| ไฟฟ้า | การประเมินทางสถิติที่นำเข้า | ไฟฟ้า                  |

**การตั้งค่าคอนฟิกผู้ให้บริการข้อมูล**

| นำเข้ารหัสต้นทาง | ฟังก์ชัน | มิติ1   | มิติ2 | มิติ5 |
|--------------------------|----------|--------------|------------|------------|
| ไฟฟ้า              | ผลรวม      | ศูนย์ต้นทุน |            |            |

> [!NOTE]
> เมื่อคุณกำหนดการตั้งค่าคอนฟิกของผู้ให้บริการข้อมูล คุณต้องระบุว่ามิติของออบเจ็กต์ต้นทุนใดที่จะจับคู่กับธุรกรรมที่นำเข้า หลังจากที่มีการประมวลผลข้อมูลแหล่งที่มาสำหรับหน่วยวัดทางสถิติ รายการทางสถิติต่อไปนี้จะถูกสร้างขึ้นในการบัญชีต้นทุน

**สมุดรายวัน**

| สมุดรายวัน | ชนิดสมุดรายวัน                       | รอบระยะเวลาปฏิทินทางการเงิน | ปี  | รอบระยะเวลา  |เวอร์ชัน      |รายการต้นทางของตัวเชื่อมต่อข้อมูล |
|---------|------------------------------------|------------------------|-------|--------|---------------|-------------|
| 00002   | สมุดรายวันการโอนย้ายรายการทางสถิติ | ทางการเงิน                 | 2017  | รอบระยะเวลา 1 | บัญชีแยกประเภทของ CA USMF | ไฟฟ้า |

**รายการสมุดรายวันการโอนย้ายรายการทางสถิติ**

| วันที่ลงบัญชี | ขนาด  | องค์ประกอบต้นทุน |   คำอธิบาย           | ศูนย์ต้นทุน |
|-----------------|------------|--------------|-------------------------|-------------|
| วันที่ 31-01-2017      | 2,450.00   | ไฟฟ้า  | ปริมาณการใช้ไฟฟ้า | CC001       |
| วันที่ 31-01-2017      | 4,100.00   | ไฟฟ้า  | ปริมาณการใช้ไฟฟ้า | CC002       |
| วันที่ 31-01-2017      | 15,000.00  | ไฟฟ้า  | ปริมาณการใช้ไฟฟ้า | CC003       |

**รายการทางสถิติ**

| ออบเจ็กต์ต้นทุน | คำอธิบาย | วันที่ลงบัญชี | สมาชิกมิติทางสถิติ |      คำอธิบาย                   | ขนาด  |
|-------------|----|-----------------|------------------------------|-------------------------|------------|
| CC001       | ทรัพยากรบุคคล | วันที่ 31-01-2017      | ไฟฟ้า                  | ปริมาณการใช้ไฟฟ้า | 2,450.00   |
| CC002       | FI | วันที่ 31-01-2017      | ไฟฟ้า                  | ปริมาณการใช้ไฟฟ้า | 4,100.00   |
| CC003       | ไอที | วันที่ 31-01-2017      | ไฟฟ้า                  | ปริมาณการใช้ไฟฟ้า | 15,000.00  |

ถ้ามีการมอบหมายฐานการปันส่วนสมาชิกของมิติที่กำหนดไว้ล่วงหน้าเดิมของไฟฟ้า ให้เป็นฐานการปันส่วนในกฎการกระจายต้นทุน จะมีกระจายต้นทุนโดยใช้ตัวคูณการปันส่วนต่อไปนี้

| ออบเจ็กต์ต้นทุน | คำอธิบาย   | ขนาด | ตัวคูณการปันส่วน          |
|-------------|---------------|-----------|----------------------------|
| CC001       | ทรัพยากรบุคคล            | 2,450.00  | (2,450 ÷ 21,550) × ปริมาณ  |
| CC002       | FI            | 4,100.00  | (4,100 ÷ 21,550) × ปริมาณ  |
| CC003       | ไอที            | 15,000.00 | (15,000 ÷ 21,550) × ปริมาณ |

## <a name="additional-resources"></a>ทรัพยากรเพิ่มเติม

[ฐานของการปันส่วน](allocation-bases.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
