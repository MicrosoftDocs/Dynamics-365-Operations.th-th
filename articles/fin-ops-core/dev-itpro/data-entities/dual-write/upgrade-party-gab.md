---
title: อัปเกรดเป็นรูปแบบสมุดที่อยู่ของฝ่ายและสมุดที่อยู่สากล
description: หัวข้อนี้จะอธิบายวิธีการอัปเกรดข้อมูลแบบสองทิศทางให้กับรูปแบบสมุดที่อยู่ของฝ่ายและสมุดที่อยู่สากล
author: RamaKrishnamoorthy
ms.date: 03/31/2021
ms.topic: article
audience: Application User, IT Pro
ms.reviewer: tfehr
ms.search.region: global
ms.author: ramasri
ms.search.validFrom: 2021-03-31
ms.openlocfilehash: 579a7d19ee7196d3242c78bd9915df24ec479c31
ms.sourcegitcommit: 4be1473b0a4ddfc0ba82c07591f391e89538f1c3
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 01/31/2022
ms.locfileid: "8060496"
---
# <a name="upgrade-to-the-party-and-global-address-book-model"></a>อัปเกรดเป็นรูปแบบสมุดที่อยู่ของฝ่ายและสมุดที่อยู่สากล

[!include [banner](../../includes/banner.md)]



[เทมเพลต Microsoft Azure Data Factory](https://github.com/microsoft/Dynamics-365-FastTrack-Implementation-Assets/tree/master/Dual-write/Upgrade%20data%20to%20dual-write%20Party-GAB%20schema) ช่วยคุณอัปเกรดข้อมูลที่มีอยู่ต่อไปนี้ในการรวมแบบสองทิศทางเป็นรูปแบบสมุดที่อยู่ของฝ่ายและสมุดที่อยู่สากล: ข้อมูลในตาราง **บัญชี**, **ผู้ติดต่อ** และ **ผู้จัดจำหน่าย** และรหัสไปรษณีย์และที่อยู่อิเล็กทรอนิกส์

เทมเพลต Data Factory ที่ให้มาพร้อมกันมีสามแบบต่อไปนี้ เทมเพลตจะช่วยกระทบยอดข้อมูลจากทั้งแอปการเงินและการดำเนินงานและแอปการมีส่วนร่วมของลูกค้า

- **[เทมเพลตของฝ่าย](https://github.com/microsoft/Dynamics-365-FastTrack-Implementation-Assets/blob/master/Dual-write/Upgrade%20data%20to%20dual-write%20Party-GAB%20schema/arm_template.json) (อัปเกรดข้อมูลที่จะรวมแบบสองทิศทางแบบแผนฝ่าย-GAB/arm_template.json)** – เทมเพลตช่วยอัปเกรดข้อมูล **ฝ่าย** และ **ผู้ติดต่อ** ที่เชื่อมโยงกับข้อมูล **บัญชี**, **ผู้ติดต่อ** และ **ผู้จัดจำหน่าย**
- **[เทมเพลตที่อยู่ทางไปรษณีย์ของฝ่าย](https://github.com/microsoft/Dynamics-365-FastTrack-Implementation-Assets/blob/master/Dual-write/Upgrade%20data%20to%20dual-write%20Party-GAB%20schema/Upgrade%20to%20Party%20Postal%20Address%20-%20GAB/arm_template.json) (อัปเกรดข้อมูลที่จะรวมแบบสองทิศทางแบบแผนฝ่าย-GAB/อัปเกรดเป็นที่อยู่ทางไปรษณีย์ของฝ่าย - GAB/arm_template.json)** – เทมเพลตนี้ช่วยอัปเกรดที่อยู่ทางไปรษณีย์ของฝ่ายที่เชื่อมโยงกับข้อมูล **บัญชี**, **ผู้ติดต่อ** และ **ผู้จัดจำหน่าย**
- **[เทมเพลตที่อยู่อิเล็กทรอนิกส์ของฝ่าย](https://github.com/microsoft/Dynamics-365-FastTrack-Implementation-Assets/blob/master/Dual-write/Upgrade%20data%20to%20dual-write%20Party-GAB%20schema/Upgrade%20to%20Party%20Electronic%20Address%20-%20GAB/arm_template.json) (อัปเกรดข้อมูลที่จะรวมแบบสองทิศทางแบบแผนฝ่าย-GAB/อัปเกรดเป็นที่อยู่อิเล็กทรอนิกส์ของฝ่าย - GAB/arm_template.json)** – เทมเพลตนี้ช่วยอัปเกรดที่อยู่อิเล็กทรอนิกส์ของฝ่ายที่เชื่อมโยงกับข้อมูล **บัญชี**, **ผู้ติดต่อ** และ **ผู้จัดจำหน่าย**

เมื่อสิ้นสุดกระบวนการ ระบบจะสร้างไฟล์ค่าที่คั่นด้วยเครื่องหมายจุลภาค (.csv) ต่อไปนี้

| ชื่อไฟล์ | วัตถุประสงค์ |
|---|---|
| FONewParty.csv | ไฟล์นี้จะช่วยสร้างเรกคอร์ด **ฝ่าย** ใหม่ภายในแอปการเงินและการดำเนินงาน |
| ImportFONewPostalAddressLocation.csv | ไฟล์นี้ช่วยสร้างเรกคอร์ด **ตำแหน่งที่อยู่ทางไปรษณีย์** ใหม่ในแอปการเงินและการดำเนินงาน |
| ImportFONewPartyPostalAddress.csv | ไฟล์นี้ช่วยสร้างเรกคอร์ด **ที่อยู่ทางไปรษณีย์ของฝ่าย** ใหม่ในแอปการเงินและการดำเนินงาน |
| ImportFONewPostalAddress.csv | ไฟล์นี้ช่วยสร้างเรกคอร์ด **ที่อยู่ทางไปรษณีย์** ใหม่ในแอปการเงินและการดำเนินงาน |
| ImportFONewElectronicAddress.csv | ไฟล์นี้ช่วยสร้างเรกคอร์ด **ที่อยู่ทางอิเล็กทรอนิกส์** ใหม่ในแอปการเงินและการดำเนินงาน |

หัวข้อนี้อธิบายวิธีการใช้เทมเพลต Data Factory และอัปเกรดข้อมูลของคุณ ถ้าคุณไม่มีการปรับแต่งใด ๆ คุณสามารถใช้เทมเพลตตามที่เป็นได้ แต่ถ้าคุณมีการปรับแต่งสำหรับข้อมูล **บัญชี** **ผู้ติดต่อ** และ **ผู้จัดจำหน่าย** คุณต้องปรับเปลี่ยนเทมเพลตตามที่อธิบายไว้ในหัวข้อนี้

> [!IMPORTANT]
> มีคําแนะนําพิเศษสำหรับการเรียกใช้เทมเพลตที่อยู่ทางไปรษณีย์ของฝ่ายและที่อยู่อิเล็กทรอนิกส์ของฝ่าย คุณต้องเรียกใช้เทมเพลตของฝ่ายก่อน แล้วจึงตามด้วยเทมเพลตที่อยู่ทางไปรษณีย์ของฝ่าย แล้วจึงตามด้วยเทมเพลตที่อยู่อิเล็กทรอนิกส์ของฝ่าย แต่ละเทมเพลตได้รับการออกแบบมาเพื่อนําเข้าในแฟกทอรีข้อมูลแยกต่างหาก

## <a name="prerequisites"></a>ข้อกำหนดเบื้องต้น

ต้องมีข้อกำหนดเบื้องต้นต่อไปนี้ก่อนคุณจึงจะสามารถอัปเกรดเป็นรูปแบบสมุดที่อยู่ของฝ่ายและสมุดที่อยู่สากล:

+ คุณต้องมี [การสมัครใช้งาน Azure](https://portal.azure.com/)
+ คุณต้องมีสิทธิ์เข้าถึง [เทมเพลต](https://github.com/microsoft/Dynamics-365-FastTrack-Implementation-Assets/tree/master/Dual-write/Upgrade%20data%20to%20dual-write%20Party-GAB%20schema)
+ คุณต้องเป็นลูกค้าการรวมแบบสองทิศทางที่มีอยู่

## <a name="prepare-for-the-upgrade"></a>จัดเตรียมสำหรับการอัปเกรด

การอัปเกรดต้องมีการจัดเตรียมต่อไปนี้

+ **การซิงโครไนซ์ทั้งหมด:** ทั้งสภาพแวดล้อมการเงินและการดำเนินงานและการมีส่วนร่วมของลูกค้าอยู่ในสถานะที่ซิงค์โดยสมบูรณ์สำหรับตาราง **บัญชี (ลูกค้า)**, **ผู้ติดต่อ** และ **ผู้จัดจำหน่าย**
+ **คีย์การรวม**: ตาราง **บัญชี (ลูกค้า)** **ผู้ติดต่อ** และ **ผู้จัดจำหน่าย** ในแอปการมีส่วนร่วมของลูกค้าใช้คีย์การรวมแบบสำเร็จรูป ถ้าคุณเลือกกำหนดคีย์การรวมเอง คุณต้องเลือกกำหนดเทมเพลตเอง
+ **หมายเลขฝ่าย:** เรกคอร์ด **บัญชี (ลูกค้า)**, **ผู้ติดต่อ** และ **ผู้จัดจำหน่าย** ทั้งหมดจะได้รับการอัปเกรดให้มีหมายเลขฝ่าย เรกคอร์ดที่ไม่มีหมายเลขฝ่ายจะถูกละเว้น ถ้าคุณต้องการอัปเกรดเรกคอร์ดเหล่านั้น ให้เพิ่มหมายเลขฝ่ายก่อนที่คุณจะเริ่มกระบวนการอัปเกรด
+ **ความขัดข้องของระบบ:** ในระหว่างกระบวนการอัปเกรด คุณจะต้องใช้ทั้งสภาพแวดล้อมการเงินและการดำเนินงานและการมีส่วนร่วมของลูกค้าแบบออฟไลน์
+ **สแนปช็อต:** ถ่ายภาพสแนปช็อตของทั้งแอปการเงินและการดำเนินงานและแอปการมีส่วนร่วมของลูกค้า คุณสามารถใช้สแนปช็อตเพื่อคืนสถานะก่อนหน้าได้ถ้าคุณต้องการ

## <a name="deployment"></a>การจัดวาง

1. ดาวน์โหลดเทมเพลตจาก [Dynamics-365-FastTrack-Implementation-Assets](https://github.com/microsoft/Dynamics-365-FastTrack-Implementation-Assets/tree/master/Dual-write/Upgrade%20data%20to%20dual-write%20Party-GAB%20schema)
2. ลงชื่อเข้าใช้ [พอร์ทัล Azure](https://portal.azure.com/)
3. สร้าง [กลุ่มทรัพยากร](/azure/azure-resource-manager/management/manage-resource-groups-portal)
4. สร้าง [บัญชีการจัดเก็บ](/azure/storage/common/storage-account-create?tabs=azure-portal) ในกลุ่มทรัพยากรที่คุณสร้างขึ้น
5. สร้าง [Data Factory](/azure/data-factory/quickstart-create-data-factory-portal) ในกลุ่มทรัพยากรที่คุณสร้างขึ้น
6. เปิด Data Factory และเลือกไทล์ **สร้างและตรวจสอบ**
7. บนแท็บ **จัดการ** ให้เลือก **เทมเพลต ARM**
8. เลือก **นำเข้าเทมเพลต ARM** เพื่อนําเข้าเทมเพลต **ฝ่าย**
9. นําเข้าเทมเพลตไปยัง Data Factory ป้อนค่าต่อไปนี้ให้กับ **รายละเอียดโครงการ** และ **รายละเอียดอินสแตนซ์**

    | ฟิลด์ | ค่า |
    |---|---|
    | การสมัครใช้งาน | การสมัครใช้งาน Azure |
    | กลุ่มทรัพยากร | ระบุทรัพยากรเดียวกันกับที่มีการสร้างบัญชีการจัดเก็บ |
    | ภูมิภาค | ภูมิภาค |
    | ชื่อโรงงาน | ชื่อคลัง |
    | คีย์หลัก FO ที่เชื่อมโยง Service_service | คีย์ของแอปพลิเคชัน |
    | ที่เก็บข้อมูล Azure Blob_สตริงการเชื่อมต่อ | สตริงการเชื่อมต่อที่เก็บข้อมูล Azure Blob |
    | Dynamics Crm ที่เชื่อมโยง Service_password | รหัสผ่านของบัญชีผู้ใช้ที่คุณระบุเป็นชื่อผู้ใช้ |
    | FO Linked Service_properties_type Properties_url | `https://sampledynamics.sandbox-operationsdynamics.com/data` |
    | FO Linked Service_properties_type Properties_tenant | ข้อมูล (ชื่อโดเมนหรือรหัสผู้เช่า) เกี่ยวกับผู้เช่าที่แอปพลิเคชันของคุณมีอยู่ |
    | FO Linked Service_properties_type Properties_aad Resource Id | `https://sampledynamics.sandboxoperationsdynamics.com` |
    | FO Linked Service_properties_type Properties_service Principal Id | รหัสไคลเอนต์ของแอปพลิเคชัน |
    | Dynamics Crm Linked Service_properties_type Properties_username | ชื่อผู้ใช้ที่ใช้ในการเชื่อมต่อกับ Dynamics 365 |

    สำหรับข้อมูลเพิ่มเติม ให้ดูหัวข้อต่อไปนี้:

    - [เลื่อนระดับเทมเพลต Resource Manager ด้วยตนเองในแต่ละสภาพแวดล้อม](/azure/data-factory/continuous-integration-deployment#manually-promote-a-resource-manager-template-for-each-environment)
    - [คุณสมบัติของบริการที่เชื่อมโยง](/azure/data-factory/connector-dynamics-ax#linked-service-properties)
    - [คัดลอกข้อมูลโดยใช้ Azure Data Factory](/azure/data-factory/connector-dynamics-crm-office-365#dynamics-365-and-dynamics-crm-online)

10. หลังจากใช้งานแล้ว ให้ตรวจสอบความถูกต้องของชุดข้อมูล ลำดับข้อมูล และบริการที่เชื่อมโยงของ Data Factory

    ![ชุดข้อมูล ลำดับข้อมูล และบริการที่เชื่อมโยง](media/data-factory-validate.png)

11. ไปยัง **จัดการ** ภายใต้ **การเชื่อมต่อ** ให้เลือก **บริการที่เชื่อมโยง** จากนั้นเลือก **DynamicsCrmLinkedService** ในกล่องโต้ตอบ **แก้ไขบริการที่เชื่อมโยง (Dynamics CRM)** ให้ป้อนค่าต่อไปนี้

    | ฟิลด์ | ค่า |
    |---|---|
    | ชื่อ | DynamicsCrmLinkedService |
    | คำอธิบาย | บริการที่เชื่อมโยงเพื่อเชื่อมต่อกับอินสแตนซ์ CRM เพื่อดึงข้อมูลเอนทิตีมาใช้ |
    | เชื่อมต่อผ่าน Integration Runtime | AutoResolvelntegrationRuntime |
    | ชนิดการปรับใช้ | ออนไลน์ |
    | Uri ของการบริการ | `https://<organization-name>.crm[x].dynamics.com` |
    | ชนิดการรับรองความถูกต้อง | Office365 |
    | ชื่อผู้ใช้ | |
    | รหัสผ่านหรือ Azure Key Vault | รหัสผ่าน |
    | รหัสผ่าน | |

## <a name="prepare-to-run-the-data-factory-templates"></a>การเตรียมการเพื่อเรียกใช้เทมเพลต Data Factory

ในหัวข้อนี้จะอธิบายการตั้งค่าที่ต้องใช้ก่อนที่คุณจะเรียกใช้เทมเพลต Data Factory สำหรับที่อยู่ทางไปรษณีย์ของฝ่ายและที่อยู่อิเล็กทรอนิกส์ของฝ่าย

### <a name="setup-to-run-the-party-postal-address-template"></a>การตั้งค่าเพื่อเรียกใช้เทมเพลตที่อยู่ทางไปรษณีย์ของฝ่าย

1. ลงชื่อเข้าใช้แอปการมีส่วนร่วมของลูกค้าและไปที่ **การตั้งค่า** \> **การตั้งค่าส่วนบุคคล** จากนั้นบนแท็บ **ทั่วไป** ให้ตั้งค่าคอนฟิกการตั้งค่าโซนเวลาสำหรับบัญชีผู้ดูแลระบบ โซนเวลาต้องอยู่ในเวลามาตรฐานสากล (UTC) เพื่ออัปเดตวันที่ "ใช้ได้ตั้งแต่" และ "ใช้ได้จนถึง" ของที่อยู่ทางไปรษณีย์จากแอปการเงินและการดำเนินงาน

    ![การตั้งค่าโซนเวลาของบัญชีผู้ดูแลระบบ](media/ADF-1.png)

2. ใน Data Factory บนแท็บ **จัดการ** ภายใต้ **พารามิเตอร์ส่วนกลาง** ให้สร้างพารามิเตอร์ส่วนกลางต่อไปนี้

    | ไม่ | ชื่อ | ชนิด | ค่า |
    |---|---|---|---|
    | 1 | PostalAddressIdPrefix | สตริง | พารามิเตอร์นี้จะผนวกหมายเลขลำดับกับที่อยู่ทางไปรษณีย์ที่สร้างขึ้นใหม่เป็นหมายเลขนําหน้า ตรวจสอบให้แน่ใจว่าได้ระบุสตริงที่ไม่ขัดแย้งกับที่อยู่ทางไปรษณีย์ในแอปการเงินและการดำเนินงานและแอปการมีส่วนร่วมของลูกค้า ตัวอย่างเช่น ใช้ **ADF-PAD-** |

    ![พารามิเตอร์ส่วนกลาง PostalAddressIdPrefix ที่สร้างบนแท็บ จัดการ](media/ADF-2.png)

3. เมื่อคุณได้ทำเสร็จสิ้นแล้ว เลือก **เผยแพร่ทั้งหมด**

    ![ปุ่มเผยแพร่ทั้งหมด](media/ADF-3.png)

### <a name="setup-to-run-the-party-electronic-address-template"></a>การตั้งค่าเพื่อเรียกใช้เทมเพลตที่อยู่อิเล็กทรอนิกส์ของฝ่าย

1. ใน Data Factory บนแท็บ **จัดการ** ภายใต้ **พารามิเตอร์ส่วนกลาง** ให้สร้างพารามิเตอร์ส่วนกลางต่อไปนี้

    | ไม่ | ชื่อ | ชนิด | ค่า |
    |---|---|---|---|
    | 1 | IsFOSource | ค่าบูลีน | พารามิเตอร์นี้จะระบุว่าที่อยู่ระบบหลักใดถูกแทนที่ในเหตุการณ์ที่มีความขัดแย้ง หากค่านี้เป็น **จริง** ที่อยู่หลักในแอปการเงินและการดำเนินงานจะแทนที่ที่อยู่หลักในแอปการมีส่วนร่วมของลูกค้า หากค่านี้เป็น **เท็จ** ที่อยู่หลักในแอปการมีส่วนร่วมของลูกค้าจะแทนที่ที่อยู่หลักในแอปการเงินและการดำเนินงาน |
    | 2 | ElectronicAddressIdPrefix | สตริง | พารามิเตอร์นี้จะผนวกหมายเลขลำดับกับที่อยู่อิเล็กทรอนิกส์ที่สร้างขึ้นใหม่เป็นหมายเลขนําหน้า ตรวจสอบให้แน่ใจว่าได้ระบุสตริงที่ไม่ขัดแย้งกับที่อยู่ทางอิเล็กทรอนิกส์ในแอปการเงินและการดำเนินงานและแอปการมีส่วนร่วมของลูกค้า ตัวอย่างเช่น ใช้ **ADF-EAD-** |

    ![พารามิเตอร์ส่วนกลาง IsFOSource และ ElectronicAddressIdPrefix global ที่สร้างบนแท็บ จัดการ](media/ADF-4.png)

2. เมื่อคุณได้ทำเสร็จสิ้นแล้ว เลือก **เผยแพร่ทั้งหมด**

## <a name="run-the-templates"></a>เรียกใช้เทมเพลต

1. หยุดแมปการรวมแบบสองทิศทาง **บัญชี**, **ผู้ติดต่อ** และ **ผู้จัดจำหน่าย** ต่อไปนี้ที่ใช้แอปการเงินและการดำเนินงาน:

    + Customers V3 (บัญชี)
    + ลูกค้า V3(ผู้ติดต่อ)
    + ผู้ติดต่อของ CDS V2(ผู้ติดต่อ)
    + ผู้ติดต่อของ CDS V2(ผู้ติดต่อ)
    + ผู้จัดจำหน่าย V2 (msdyn_vendor)

2. ตรวจสอบให้แน่ใจว่าแผนที่ถูกลบออกจากตาราง **msdy_dualwriteruntimeconfig** ใน Dataverse
3. ติดตั้ง [ฝ่ายการรวมแบบสองทิศทางและโซลูชันสมุดที่อยู่สากล](https://aka.ms/dual-write-gab) จาก AppSource
4. ในแอปการเงินและการดำเนินงาน ให้เรียกใช้ **การซิงค์ครั้งแรก** หากตารางต่อไปนี้มีข้อมูล:

    + คำขึ้นต้น
    + ชนิดลักษณะส่วนบุคคล
    + คำลงท้าย
    + ตำแหน่งของผู้ติดต่อ
    + บทบาทในการตัดสินใจ
    + ระดับของสมาชิก

5. ในแอปการมีส่วนร่วมของลูกค้าให้ปิดใช้งานขั้นตอนปลั๊กอินต่อไปนี้

    + การอัปเดตบัญชี

        + Microsoft.Dynamics.GABExtended.Gabs.UpdatePartyAttributesFromAccountEntity: อัปเดตบัญชี
        + Microsoft.Dynamics.FinanceExtended.Plugins.TriggerNotesForCustomerTypeCodes: อัปเดตบัญชี

    + การอัปเดตผู้ติดต่อ

        + Microsoft.Dynamics.GABExtended.Gabs.UpdatePartyAttributesFromContactEntity: อัปเดตผู้ติดต่อ
        + Microsoft.Dynamics.FinanceExtended.Plugins.TriggerNotesForSellableContact: อัปเดตผู้ติดต่อ

    + อัปเดต msdyn_party

        + Microsoft.Dynamics.GABExtended.Gabs.UpdatePartyAttributesFromPartyEntity: การอัปเดต msdyn_party

    + การอัปเดต msdyn_vendor

        + Microsoft.Dynamics.GABExtended.Gabs.UpdatePartyAttributesFromVendorEntity: การอัปเดต msdyn_vendor

    + Customeraddress

        + สร้าง

            + Microsoft.Dynamics.GABExtended.Plugins.CreatePartyAddress: การสร้าง customeraddress

        + อัปเดต

            + Microsoft.Dynamics.GABExtended.Plugins.CreatePartyAddress: การอัปเดต customeraddress

        + ลบ

            + Microsoft.Dynamics.GABExtended.Plugins.DeleteCustomerAddress: การลบ customeraddress

    + msdyn_partypostaladdress

        + สร้าง

            + Microsoft.Dynamics.GABExtended.Plugins.CreateCustomerAddress: การสร้าง msdyn_partypostaladdress
            + Microsoft.Dynamics.GABExtended.Plugins.PartyPostalAddress: การสร้าง msdyn_partypostaladdress

        + อัปเดต

            + Microsoft.Dynamics.GABExtended.Plugins.CreateCustomerAddress: การอัปเดต msdyn_partypostaladdress
            + Microsoft.Dynamics.GABExtended.Plugins.PartyPostalAddress: การอัปเดต msdyn_partypostaladdress

    + msdyn_postaladdress

        + สร้าง

            + Microsoft.Dynamics.GABExtended.Plugins.PostalAddress: การสร้าง msdyn_postaladdress
            + Microsoft.Dynamics.GABExtended.Plugins.PostalAddressPostCreate: การสร้าง msdyn_postaladdress
            + Microsoft.Dynamics.GABExtended.Plugins.UpdateCustomerAddress: การสร้าง msdyn_postaladdress

        + อัปเดต

            + Microsoft.Dynamics.GABExtended.Plugins.PostalAddressUpdate: การอัปเดต msdyn_postaladdress
            + Microsoft.Dynamics.GABExtended.Plugins.UpdateCustomerAddress: การอัปเดต msdyn_postaladdress

    + msdyn_partyelectronicaddress

        + สร้าง

            + Microsoft.Dynamics.GABExtended.Plugins.PartyElectronicAddressSync: การสร้าง msdyn_partyelectronicaddress

        + อัปเดต

            + Microsoft.Dynamics.GABExtended.Plugins.PartyElectronicAddressSync: การอัปเดต msdyn_partyelectronicaddress

        + ลบ

            + Microsoft.Dynamics.GABExtended.Plugins.DeletePartyElectronicAddressSync: การลบ msdyn_partyelectronicaddress

6. ในแอปการมีส่วนร่วมของลูกค้าให้ปิดใช้งานลำดับงานต่อไปนี้:

    + สร้างผู้จัดจำหน่ายในตารางบัญชี
    + สร้างผู้จัดจำหน่ายในตารางบัญชี
    + สร้างผู้จัดจำหน่ายชนิดบุคคลในตารางผู้ติดต่อ
    + สร้างผู้จัดจำหน่ายชนิดบุคคลในตารางผู้จัดจำหน่าย
    + อัปเดตผู้จัดจำหน่ายในตารางบัญชี
    + อัปเดตผู้จัดจำหน่ายในตารางผู้จัดจำหน่าย
    + อัปเดตผู้จัดจำหน่ายชนิดบุคคลในตารางผู้ติดต่อ
    + อัปเดตผู้จัดจำหน่ายชนิดบุคคลในตารางผู้จัดจำหน่าย

7. ใน Data Factory ให้เรียกใช้เทมเพลตโดยการเลือก **ทริกเกอร์ตอนนี้** ดังที่แสดงในภาพประกอบต่อไปนี้ กระบวนการนี้อาจใช้เวลาสักครู่เพื่อกรอกข้อมูลตามปริมาณข้อมูล

    ![การเรียกใช้เทมเพลต](media/data-factory-trigger.png)

    > [!NOTE]
    > ถ้าคุณมีการปรับแต่งสำหรับ **บัญชี** **ผู้ติดต่อ** และ **ผู้จัดจำหน่าย** คุณต้องปรับเปลี่ยนเทมเพลต

8. นําเข้าเรกคอร์ด **ฝ่าย** ลงในแอปการเงินและการดำเนินงาน

    1. ดาวน์โหลดไฟล์ **FONewParty.csv** จากที่เก็บข้อมูล Azure Blob พาธคือ **partybootstrapping/output/FONewParty.csv**
    2. แปลงไฟล์ **FONewParty.csv** เป็นไฟล์ Excel และนําเข้าไฟล์ Excel ไปยังแอปการเงินและการดำเนินงาน หรือหากการนําเข้า CSV ใช้ได้ คุณสามารถนําเข้าไฟล์ .csv ได้โดยตรง ขั้นตอนนี้อาจใช้เวลาสองสามชั่วโมงจึงจะเสร็จ ขึ้นอยู่กับปริมาณข้อมูล สำหรับข้อมูลเพิ่มเติม ให้ดูที่ [ภาพรวมของงานนำเข้าและส่งออกข้อมูล](../data-import-export-job.md)

    ![การนําเข้าเรกคอร์ดฝ่ายของ Dataverse](media/data-factory-import-party.png)

9. ใน Data Factory ให้เรียกใช้เทมเพลตที่อยู่ทางไปรษณีย์ของฝ่ายและที่อยู่อิเล็กทรอนิกส์ของฝ่าย เทมเพลตหนึ่งอยู่หลังอีกเทมเพลต

    + เทมเพลตที่อยู่ทางไปรษณีย์ของฝ่ายจะส่งเรกคอร์ดที่อยู่ทางไปรษณีย์ทั้งหมดลงในแอปการมีส่วนร่วมของลูกค้าและเชื่อมโยงกับเรกคอร์ด **บัญชี**, **ผู้ติดต่อ** และ **ผู้จัดจำหน่าย** โดยยังสร้างไฟล์ .csv สามไฟล์: ImportFONewPostalAddressLocation.csv, ImportFONewPartyPostalAddress.csv และ ImportFONewPostalAddress.csv
    + เทมเพลตที่อยู่อิเล็กทรอนิกส์ของฝ่ายจะส่งเรกคอร์ดที่อยู่อิเล็กทรอนิกส์ทั้งหมดลงในแอปการมีส่วนร่วมของลูกค้าและเชื่อมโยงกับเรกคอร์ด **บัญชี**, **ผู้ติดต่อ** และ **ผู้จัดจำหน่าย** โดยยังสร้างไฟล์ .csv หนึ่งไฟล์: ImportFONewElectronicAddress.csv

    ![การเรียกใช้เทมเพลตที่อยู่ทางไปรษณีย์ของฝ่ายและที่อยู่อิเล็กทรอนิกส์ของฝ่าย](media/ADF-7.png)

10. เมื่อต้องการอัปเดตแอปการเงินและการดำเนินงานด้วยข้อมูลนี้ คุณต้องแปลงไฟล์ .csv เป็นเวิร์กบุ๊ก Excel และ [นําเข้าไปยังแอปการเงินและการดำเนินงาน](/data-entities/data-import-export-job) หรือหากการนําเข้า CSV ใช้ได้ คุณสามารถนําเข้าไฟล์ .csv ได้โดยตรง ขั้นตอนนี้อาจใช้เวลาสองสามชั่วโมงจึงจะเสร็จ ขึ้นอยู่กับปริมาณ

    ![การนำเข้าสำเร็จ](media/ADF-8.png)

11. ในแอปการมีส่วนร่วมของลูกค้าให้เปิดใช้งานขั้นตอนปลั๊กอินต่อไปนี้:

    + การอัปเดตบัญชี

        + Microsoft.Dynamics.GABExtended.Gabs.UpdatePartyAttributesFromAccountEntity: อัปเดตบัญชี
        + Microsoft.Dynamics.FinanceExtended.Plugins.TriggerNotesForCustomerTypeCodes: อัปเดตบัญชี

    + การอัปเดตผู้ติดต่อ

        + Microsoft.Dynamics.GABExtended.Gabs.UpdatePartyAttributesFromContactEntity: อัปเดตผู้ติดต่อ
        + Microsoft.Dynamics.FinanceExtended.Plugins.TriggerNotesForSellableContact: อัปเดตผู้ติดต่อ

    + อัปเดต msdyn_party

        + Microsoft.Dynamics.GABExtended.Gabs.UpdatePartyAttributesFromPartyEntity: การอัปเดต msdyn_party

    + การอัปเดต msdyn_vendor

        + Microsoft.Dynamics.GABExtended.Gabs.UpdatePartyAttributesFromVendorEntity: การอัปเดต msdyn_vendor

    + msdyn_partypostaladdress

        + สร้าง

            + Microsoft.Dynamics.GABExtended.Plugins.CreateCustomerAddress: การสร้าง msdyn_partypostaladdress
            + Microsoft.Dynamics.GABExtended.Plugins.PartyPostalAddress: การสร้าง msdyn_partypostaladdress

        + อัปเดต

            + Microsoft.Dynamics.GABExtended.Plugins.CreateCustomerAddress: การอัปเดต msdyn_partypostaladdress
            + Microsoft.Dynamics.GABExtended.Plugins.PartyPostalAddress: การอัปเดต msdyn_partypostaladdress

    + msdyn_postaladdress

        + สร้าง

            + Microsoft.Dynamics.GABExtended.Plugins.PostalAddress: การสร้าง msdyn_postaladdress
            + Microsoft.Dynamics.GABExtended.Plugins.PostalAddressPostCreate: การสร้าง msdyn_postaladdress
            + Microsoft.Dynamics.GABExtended.Plugins.UpdateCustomerAddress: การสร้าง msdyn_postaladdress

        + อัปเดต

            + Microsoft.Dynamics.GABExtended.Plugins.PostalAddressUpdate: การอัปเดต msdyn_postaladdress
            + Microsoft.Dynamics.GABExtended.Plugins.UpdateCustomerAddress: การอัปเดต msdyn_postaladdress
 
    + msdyn_partyelectronicaddress

        + สร้าง

            + Microsoft.Dynamics.GABExtended.Plugins.PartyElectronicAddressSync: การสร้าง msdyn_partyelectronicaddress

        + อัปเดต

            + Microsoft.Dynamics.GABExtended.Plugins.PartyElectronicAddressSync: การอัปเดต msdyn_partyelectronicaddress

        + ลบ

            + Microsoft.Dynamics.GABExtended.Plugins.DeletePartyElectronicAddressSync: การลบ msdyn_partyelectronicaddress

12. ในแอปการมีส่วนร่วมของลูกค้าให้เรียกใช้ลำดับงานต่อไปนี้หากคุณยกเลิกการเรียกใช้ก่อนหน้า:

    + สร้างผู้จัดจำหน่ายในตารางบัญชี
    + สร้างผู้จัดจำหน่ายในตารางบัญชี
    + สร้างผู้จัดจำหน่ายชนิดบุคคลในตารางผู้ติดต่อ
    + สร้างผู้จัดจำหน่ายชนิดบุคคลในตารางผู้จัดจำหน่าย
    + อัปเดตผู้จัดจำหน่ายในตารางบัญชี
    + อัปเดตผู้จัดจำหน่ายในตารางผู้จัดจำหน่าย
    + อัปเดตผู้จัดจำหน่ายชนิดบุคคลในตารางผู้ติดต่อ
    + อัปเดตผู้จัดจำหน่ายชนิดบุคคลในตารางผู้จัดจำหน่าย

13. เรียกใช้แผนผังที่เกี่ยวข้องกับเรกคอร์ด **ฝ่าย** ตามที่อธิบายไว้ใน [สมุดที่อยู่ของฝ่ายและสมุดที่อยู่สากล](party-gab.md)

## <a name="explanation-of-the-data-factory-templates"></a>คําอธิบายเกี่ยวกับเทมเพลต Data Factory

ส่วนนี้จะแสดงขั้นตอนต่างๆ ในเทมเพลต Data Factory แต่ละเทมเพลต

### <a name="steps-in-the-party-template"></a>ขั้นตอนในเทมเพลตของฝ่าย

1. ขั้นตอนที่ 1 ถึง 6 ระบุบริษัทที่เปิดใช้งานการรวมแบบสองทิสทางและสร้างคำสั่งตัวกรองสำหรับบริษัท
2. ขั้นตอนที่ 7-1 ถึง 7-9 จะเรียกข้อมูลจากทั้งแอปการเงินและการดำเนินงานและแอปการมีส่วนร่วมของลูกค้าและลำดับขั้นข้อมูลสำหรับการอัปเกรด
3. ขั้นตอนที่ 8 ถึง 9 จะเปรียบเทียบหมายเลขฝ่ายสำหรับเรกคอร์ด **บัญชี**, **ผู้ติดต่อ** และ **ผู้จัดจำหน่าย** ระหว่างแอปการเงินและการดำเนินงานกับแอปการมีส่วนร่วมของลูกค้า เรกคอร์ดที่ไม่มีหมายเลขฝ่ายจะถูกข้าม
4. ขั้นตอนที่ 10 จะสร้างไฟล์ .csv สองไฟล์ต่อเรกคอร์ดฝ่ายที่ต้องสร้างในแอปการมีส่วนร่วมของลูกค้าและแอปการเงินและการดำเนินงาน

    - **FOCDSParty.csv** – ไฟล์นี้มีเรกคอร์ดทั้งหมดของฝ่ายในทั้งสองระบบ โดยไม่พิจารณาว่าบริษัทเปิดใช้งานการรวมแบบสองทิศทางหรือไม่
    - **FONewParty.csv** – ไฟล์นี้มีชุดย่อยของเรกคอร์ดฝ่ายที่ Dataverse ทราบ (ตัวอย่างเช่น บัญชีของชนิด **ผู้ที่มีแนวโน้มจะเป็นลูกค้า**)

5. ขั้นตอนที่ 11 สร้างฝ่ายในแอปการมีส่วนร่วมของลูกค้า
6. ขั้นตอนที่ 12 เรียกข้อมูลรหัสเฉพาะสากล (GUID) ของแอปการมีส่วนร่วมของลูกค้าและลำดับขั้นเพื่อให้สามารถเชื่อมโยงกับเรกคอร์ด **บัญชี**, **ผู้ติดต่อ** และ **ผู้จัดจำหน่าย** ในขั้นตอนต่อไป
7. ขั้นตอนที่ 13 เชื่อมโยงเรกคอร์ด **บัญชี**, **ผู้ติดต่อ** และ **ผู้จัดจำหน่าย** กับ GUID ของฝ่าย
8. ขั้นตอนที่ 14-1 ถึง 14-3 อัปเดตเรกคอร์ด **บัญชี**, **ผู้ติดต่อ** และ **ผู้จัดจำหน่าย** ในแอปการมีส่วนร่วมของลูกค้าด้วย GUID ของฝ่าย
9. ขั้นตอนที่ 15-1 ถึง 15-3 จัดเตรียมเรกคอร์ด **ผู้ติดต่อของฝ่าย** สำหรับเรกคอร์ด **บัญชี**, **ผู้ติดต่อ** และ **ผู้จัดจำหน่าย**
10. ขั้นตอนที่ 16-1 ถึง 16-7 จะเรียกข้อมูลอ้างอิง เช่น การทักทายและชนิดบุคลิกส่วนตัว และเชื่อมโยงกับเรกคอร์ด **ผู้ติดต่อของฝ่าย**
11. ขั้นตอนที่ 17 รวมเรกคอร์ด **ผู้ติดต่อของฝ่าย** สำหรับเรกคอร์ด **บัญชี**, **ผู้ติดต่อ** และ **ผู้จัดจำหน่าย**
12. ขั้นตอนที่ 18 นําเข้าเรกคอร์ด **ผู้ติดต่อของฝ่าย** ไปยังแอปการมีส่วนร่วมของลูกค้า

### <a name="steps-in-the-party-postal-address-template"></a>ขั้นตอนในเทมเพลตที่อยู่ทางไปรษณีย์ของฝ่าย

1. ขั้นตอนที่ 1-1 ถึง 1-10 จะเรียกข้อมูลจากทั้งแอปการเงินและการดำเนินงานและแอปการมีส่วนร่วมของลูกค้าและลำดับขั้นข้อมูลสำหรับการอัปเกรด
2. ขั้นตอนที่ 2 ดีนอร์มัลไลซ์ข้อมูลที่อยู่ทางไปรษณีย์ในแอปการเงินและการดำเนินงานด้วยการรวมที่อยู่ทางไปรษณีย์และที่อยู่ทางไปรษณีย์ของฝ่าย
3. ขั้นตอนที่ 3 ขจัดรายการซ้ำและผสานข้อมูลบัญชี ผู้ติดต่อ และผู้จัดจำหน่ายจากแอปการมีส่วนร่วมของลูกค้า
4. ขั้นตอนที่ 4 สร้างไฟล์ .csv สำหรับแอปการเงินและการดำเนินงานเพื่อสร้างข้อมูลที่อยู่ใหม่ที่อิงกับที่อยู่ของบัญชี ผู้ติดต่อ และผู้จัดจำหน่าย
5. ขั้นตอนที่ 5-1 สร้างไฟล์ .csv สำหรับแอปการมีส่วนร่วมของลูกค้าเพื่อสร้างข้อมูลที่อยู่ทั้งหมดตามแอปการเงินและการดำเนินงานและแอปการมีส่วนร่วมของลูกค้า
6. ขั้นตอนที่ 5-2 แปลงไฟล์ .csv เป็นรูปแบบการนำเข้าของการเงินและการดำเนินงานสำหรับการนําเข้าด้วยตนเอง

    - ImportFONewPostalAddressLocation.csv
    - ImportFONewPartyPostalAddress.csv
    - ImportFONewPostalAddress.csv

7. ขั้นตอนที่ 6 นําเข้าข้อมูลคอลเลกชันที่อยู่ทางไปรษณีย์ไปยังแอปการมีส่วนร่วมของลูกค้า
8. ขั้นตอนที่ 7 เรียกข้อมูลคอลเลกชันที่อยู่ทางไปรษณีย์จากแอปการมีส่วนร่วมของลูกค้า
9. ขั้นตอนที่ 8 สร้างข้อมูลที่อยู่ของลูกค้าและเชื่อมโยงรหัสคอลเลกชันที่อยู่ทางไปรษณีย์
10. ขั้นตอนที่ 9-1 ถึง 9-2 เชื่อมโยงรหัสคอลเลกชันที่อยู่ทางไปรษณีย์ของฝ่ายและคอลเลกชันที่อยู่ทางไปรษณีย์กับที่อยู่ทางไปรษณีย์และที่อยู่ทางไปรษณีย์ของฝ่าย
11. ขั้นตอนที่ 10-1 ถึง 10-3 นําเข้าที่อยู่ของลูกค้า ที่อยู่ทางไปรษณีย์ และที่อยู่ทางไปรษณีย์ของฝ่ายไปยังในแอปการมีส่วนร่วมของลูกค้า

### <a name="steps-in-the-party-electronic-address-template"></a>ขั้นตอนในเทมเพลตที่อยู่อิเล็กทรอนิกส์ของฝ่าย

1. ขั้นตอนที่ 1-1 ถึง 1-5 จะเรียกข้อมูลจากทั้งแอปการเงินและการดำเนินงานและแอปการมีส่วนร่วมของลูกค้าและลำดับขั้นข้อมูลสำหรับการอัปเกรด
2. ขั้นตอนที่ 2 รวมที่อยู่อิเล็กทรอนิกส์ในแอปการมีส่วนร่วมของลูกค้าจากเอนทิตี้บัญชี ผู้ติดต่อ และผู้จัดจำหน่าย
3. ขั้นตอนที่ 3 ผสานข้อมูลที่อยู่อิเล็กทรอนิกส์หลักจากแอปการมีส่วนร่วมของลูกค้าและแอปการเงินและการดำเนินงาน
4. ขั้นตอนที่ 4 สร้างไฟล์ .csv

    - สร้างข้อมูลที่อยู่อิเล็กทรอนิกส์ใหม่สำหรับแอปการเงินและการดำเนินงานโดยยึดตามบัญชี ผู้ติดต่อ และผู้จัดจำหน่าย
    - สร้างข้อมูลที่อยู่อิเล็กทรอนิกส์ใหม่สำหรับแอปการมีส่วนร่วมของลูกค้าโดยยึดตามที่อยู่อิเล็กทรอนิกส์ ที่อยู่ของบัญชี ผู้ติดต่อ และผู้จัดส่งในแอปการเงินและการดำเนินงาน

5. ขั้นตอนที่ 5-1 นําเข้าที่อยู่อิเล็กทรอนิกส์ไปยังแอปการมีส่วนร่วมของลูกค้า
6. ขั้นตอนที่ 5-2 สร้างไฟล์ .csv เพื่ออัปเดตที่อยู่หลักสำหรับบัญชีและผู้ติดต่อในแอปการมีส่วนร่วมของลูกค้า
7. ขั้นตอนที่ 6-1 ถึง 6-2 นำเข้าที่อยู่หลักของบัญชีและผู้ติดต่อไปยังแอปการมีส่วนร่วมของลูกค้า

## <a name="troubleshooting"></a>การแก้ไขปัญหา

1. ถ้ากระบวนการล้มเหลว ให้เรียกใช้ Data Factory ใหม่ เริ่มต้นจากกิจกรรมที่ล้มเหลว
2. บางไฟล์ที่สร้างขึ้นโดย Data Factory สามารถใช้เพื่อการตรวจสอบความถูกต้องของข้อมูล
3. Data Factory จะเรียกใช้ตามไฟล์ .csv ดังนั้น ถ้ามีเครื่องหมายจุลภาคอยู่ในฟิลด์ใดๆ อาจใช้เฉพาะกับผลลัพธ์ คุณต้องลบเครื่องหมายจุลภาคทั้งหมดออกจากค่าฟิลด์
4. แท็บ **การตรวจสอบ** แสดงข้อมูลเกี่ยวกับขั้นตอนและข้อมูลทั้งหมดที่มีการประมวลผล เลือกขั้นตอนเฉพาะเพื่อดีบักขั้นตอนนั้น

    ![แท็บการตรวจสอบ](media/data-factory-monitor.png)

## <a name="learn-more-about-the-template"></a>เรียนรู้เพิ่มเติมเกี่ยวกับเทมเพลต

สำหรับข้อมูลเพิ่มเติมเกี่ยวกับเทมเพลต ดูที่ [ข้อคิดเห็นสำหรับ readme ของเทมเพลต Azure Data Factory](https://github.com/microsoft/Dynamics-365-FastTrack-Implementation-Assets/blob/master/Dual-write/Upgrade%20data%20to%20dual-write%20Party-GAB%20schema/readme.md)
