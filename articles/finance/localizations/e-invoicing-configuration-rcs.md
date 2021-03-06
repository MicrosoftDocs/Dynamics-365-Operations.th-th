---
title: ตั้งค่าคอนฟิก Add-on ของการออกใบแจ้งหนี้ทางอิเล็กทรอนิกส์ใน Regulatory Configuration Services (RCS)
description: หัวข้อนี้อธิบายวิธีการตั้งค่าคอนฟิก Add-on ของการออกใบแจ้งหนี้ทางอิเล็กทรอนิกส์ใน Dynamics 365 Regulatory Configuration Services (RCS)
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
ms.openlocfilehash: bb4a426bb54ee21197f9954d946d60ea55f5eb76
ms.sourcegitcommit: e88c96d1cb817a22db81856cadb563c095ab2671
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 02/02/2021
ms.locfileid: "5104446"
---
# <a name="configure-the-electronic-invoicing-add-on-in-regulatory-configuration-services-rcs"></a>ตั้งค่าคอนฟิก Add-on ของการออกใบแจ้งหนี้ทางอิเล็กทรอนิกส์ใน Regulatory Configuration Services (RCS)

[!include [banner](../includes/banner.md)]

[!include [banner](../includes/banner.md)]

หัวข้อนี้มีข้อมูลเกี่ยวกับความสามารถในการตั้งค่าคอนฟิกของ Add-on ของการออกใบแจ้งหนี้ทางอิเล็กทรอนิกส์ใน Dynamics 365 Regulatory Configuration Services (RCS)

ซึ่งจะผ่านความสามารถในการตั้งค่าคอนฟิกที่ Add-on ของการออกใบแจ้งหนี้ทางอิเล็กทรอนิกส์ ช่วยคุณในการปฏิบัติตามข้อกําหนดทางธุรกิจและระเบียบบังคับของใบแจ้งหนี้อิเล็กทรอนิกส์ โดยไม่ต้องกําหนดรหัสใดๆ และในสถานการณ์ที่ใบแจ้งหนี้ทางอิเล็กทรอนิกส์ต้องได้รับการอนุมัติทางอิเล็กทรอนิกส์โดยบริการเว็บ ความสามารถในการตั้งค่าคอนฟิกยังช่วยคุณในการปฏิบัติตามข้อกําหนดสำหรับการแลกเปลี่ยนข้อความกับบริการเว็บ โดยไม่ต้องกําหนดรหัสใดๆ

## <a name="electronic-reporting"></a>การรายงานทางอิเล็กทรอนิกส์

การรายงานทางอิเล็กทรอนิกส์ (ER) สนับสนุน Add-on ของการออกใบแจ้งหนี้ทางอิเล็กทรอนิกส์

การแม็ปรูปแบบข้อมูลและรูปแบบเป็นส่วนประกอบที่ตั้งค่าคอนฟิกได้ ซึ่งสร้างขึ้นและเก็บรักษาโดยใช้ ER และใช้ใน Add-on ของการออกใบแจ้งหนี้ทางอิเล็กทรอนิกส์ ตัวออกแบบรูปแบบ ER คือเครื่องมือในการสร้างและการรักษารูปแบบไฟล์ ซึ่งใช้ในการตั้งค่าคอนฟิกคุณลักษณะการออกใบแจ้งหนี้ทางอิเล็กทรอนิกส์

สำหรับข้อมูล ดู [ภาพรวมการรายงานทางอิเล็กทรอนิกส์ (ER)](../../fin-ops-core/dev-itpro/analytics/general-electronic-reporting.md)

## <a name="electronic-invoicing-features"></a>คุณลักษณะการออกใบแจ้งหนี้ทางอิเล็กทรอนิกส์

ลักษณะการออกใบแจ้งหนี้ทางอิเล็กทรอนิกส์จะรับผิดชอบในการสร้างใบแจ้งหนี้อิเล็กทรอนิกส์โดยผ่าน Add-on ของการออกใบแจ้งหนี้ทางอิเล็กทรอนิกส์ โดยจะสรุปกฎการตั้งค่าคอนฟิกและใช้กฎเหล่านั้นเพื่อประมวลผลข้อมูลที่ Microsoft Dynamics 365 Finance และ Dynamics 365 Supply Chain Management ส่งไปยัง Add-on ของการออกใบแจ้งหนี้ทางอิเล็กทรอนิกส์และไปยังใบแจ้งหนี้อิเล็กทรอนิกส์

นอกจากนี้ คุณลักษณะนี้ยังสนับสนุนสถานการณ์สมมติที่ซึ่งต้องปฏิบัติตามข้อมูลจำเพาะเกี่ยวกับรูปแบบไฟล์ และผลลัพธ์เป็นไฟล์อิเล็กทรอนิกส์แบบสแตนด์อโลน ในกรณีส่วนใหญ่ ข้อมูลจำเพาะเกี่ยวกับรูปแบบไฟล์จะถูกเผยแพร่โดยหน่วยงานจัดเก็บภาษี

ในตอนท้าย คุณลักษณะนี้สนับสนุนการแลกเปลี่ยนข้อความกับบริการเว็บภายนอกที่โฮสต์โดยหน่วยงานจัดเก็บภาษีหรือโดยบางฝ่ายที่ได้รับการรับรอง และร้องขอการตรวจสอบหรือตราประทับการอนุมัติในใบแจ้งหนี้อิเล็กทรอนิกส์

### <a name="availability-of-electronic-invoicing-features"></a>ความพร้อมใช้งานของคุณลักษณะการออกใบแจ้งหนี้ทางอิเล็กทรอนิกส์

ความพร้อมใช้งานของคุณลักษณะการออกใบแจ้งหนี้ทางอิเล็กทรอนิกส์ จะขึ้นอยู่กับประเทศหรือภูมิภาค ถึงแม้ว่าคุณลักษณะบางอย่างจะพร้อมใช้งานโดยทั่วไป แต่บางอย่างจะอยู่ในพรีวิว

#### <a name="preview-features"></a>คุณลักษณะรุ่นพรีวิว

ตารางต่อไปนี้แสดงคุณลักษณะการการออกใบแจ้งหนี้ทางอิเล็กทรอนิกส์ที่อยู่ในพรีวิวในปัจจุบัน

| ประเทศ/ภูมิภาค | ชื่อคุณลักษณะ                         | เอกสารทางธุรกิจ |
|----------------|--------------------------------------|-------------------|
| ออสเตรีย        | ใบแจ้งหนี้อิเล็กทรอนิกส์ออสเตรเลีย (AT)    | ใบแจ้งหนี้การขายและใบแจ้งหนี้โครงการ |
| เบลเยียม        | ใบแจ้งหนี้อิเล็กทรอนิกส์เบลเยียม (BE)      | ใบแจ้งหนี้การขายและใบแจ้งหนี้โครงการ |
| บราซิล         | NF-e (BR) ของบราซิล                  | แบบจำลองเอกสารทางการเงิน 55 จดหมายการแก้ไข การยกเลิก และการละทิ้ง |
| บราซิล         | NFS-e ABRASF Curitiba (BR) ของบราซิล | เอกสารทางการเงินของบริการ |
| บราซิล         | NFS-e São Paulo (BR) ของบราซิล       | เอกสารทางการเงินของบริการ |
| เดนมาร์ก        | ใบแจ้งหนี้อิเล็กทรอนิกส์เดนมาร์ก (DK)       | ใบแจ้งหนี้การขายและใบแจ้งหนี้โครงการ |
| อียิปต์          | ใบแจ้งหนี้อิเล็กทรอนิกส์ของอียิปต์ (EG) | ใบแจ้งหนี้การขายและใบแจ้งหนี้โครงการ |
| เอสโตเนีย        | ใบแจ้งหนี้อิเล็กทรอนิกส์เอสโตเนีย (EE)     | ใบแจ้งหนี้การขายและใบแจ้งหนี้โครงการ |
| ฟินแลนด์        | ใบแจ้งหนี้อิเล็กทรอนิกส์ฟินแลนด์ (FI)      | ใบแจ้งหนี้การขายและใบแจ้งหนี้โครงการ |
| ฝรั่งเศส         | ใบแจ้งหนี้อิเล็กทรอนิกส์ฝรั่งเศส (FR)       | ใบแจ้งหนี้การขายและใบแจ้งหนี้โครงการ |
| เยอรมนี        | ใบแจ้งหนี้อิเล็กทรอนิกส์เยอรมัน (DE)       | ใบแจ้งหนี้การขายและใบแจ้งหนี้โครงการ |
| อิตาลี          | FatturaPA (IT)                       | ใบแจ้งหนี้การขายและใบแจ้งหนี้โครงการ |
| เม็กซิโก         | CFDI (MX) ของเม็กซิโก                    | ใบแจ้งหนี้การขาย บันทึกการจัดส่ง การโอนย้ายสินค้าคงคลัง ส่วนเพิ่มเติมและการยกเลิกการจ่าย |
| เนเธอร์แลนด์    | ใบแจ้งหนี้อิเล็กทรอนิกส์ดัตช์ (NL)        | ใบแจ้งหนี้การขายและใบแจ้งหนี้โครงการ |
| นอร์เวย์         | ใบแจ้งหนี้อิเล็กทรอนิกส์นอร์เวย์ (NO)    | ใบแจ้งหนี้การขายและใบแจ้งหนี้โครงการ |
| สเปน          | ใบแจ้งหนี้อิเล็กทรอนิกส์สเปน (ES)      | ใบแจ้งหนี้การขายและใบแจ้งหนี้โครงการ |
| ยุโรป         | ใบแจ้งหนี้อิเล็กทรอนิกส์ PEPPOL            | ใบแจ้งหนี้การขายและใบแจ้งหนี้โครงการของ PEPPOL |

### <a name="configurable-components-of-electronic-invoicing-features"></a>ส่วนประกอบที่ตั้งค่าคอนฟิกได้ของคุณลักษณะการออกใบแจ้งหนี้อิเล็กทรอนิกส์

คุณลักษณะการออกใบแจ้งหนี้ทางอิเล็กทรอนิกส์ ประกอบด้วยกลุ่มของส่วนประกอบที่ตั้งค่าคอนฟิกได้ดังต่อไปนี้:

- **รูปแบบ** – รูปแบบช่วยให้คุณสามารถตั้งค่าคอนฟิกสิ่งที่ Add-on ของการออกใบแจ้งหนี้ทางอิเล็กทรอนิกส์ต้องสร้าง เมื่อเอกสารอิเล็กทรอนิกส์กลายเป็นใบแจ้งหนี้อิเล็กทรอนิกส์ รูปแบบจะรวมการตั้งค่าคอนฟิกรูปแบบของใบแจ้งหนี้อิเล็กทรอนิกส์ และสำหรับไฟล์และข้อความที่ใช้ในการส่งการร้องขอและรับการตอบสนอง เมื่อต้องมีการสื่อสารกับบริการเว็บภายนอก
- **การดำเนินการ** – การดำเนินการช่วยให้คุณสามารถตั้งค่าคอนฟิกวิธีการที่ Add-on ของการออกใบแจ้งหนี้ทางอิเล็กทรอนิกส์สร้างการแปลงเอกสารอิเล็กทรอนิกส์ที่ Finance and Supply Chain Management ส่งเข้าสู่ใบแจ้งหนี้อิเล็กทรอนิกส์
- **กฎการใช้งาน** – กฎการใช้งานช่วยให้คุณสามารถตั้งค่าคอนฟิกบริบทที่ Add-on ของการออกใบแจ้งหนี้ทางอิเล็กทรอนิกส์ต้องพิจารณา เพื่อประมวลผลคุณลักษณะการออกใบแจ้งหนี้ทางอิเล็กทรอนิกส์
- **ตัวแปร** – ตัวแปรช่วยให้คุณสามารถตั้งค่าคอนฟิกการสนับสนุนสำหรับการสร้างตรรกะการตั้งค่าคอนฟิกได้ ตัวแปรสามารถใช้เป็นข้อมูลป้อนเข้าของค่าเพื่อทำการดำเนินการเฉพาะ หรือสามารถทำงานเป็นการแลกเปลี่ยนค่าระหว่าง Finance และ Supply Chain Management และ add-on ของการออกใบแจ้งหนี้ทางอิเล็กทรอนิกส์
- **การแม็ปแบบจำลองเอกสารอิเล็กทรอนิกส์** – การแม็ปแบบจำลองเอกสารอิเล็กทรอนิกส์ช่วยให้คุณสามารถตั้งค่าคอนฟิกการแม็ปแบบจำลอง ER ได้ การแม็ปแบบจำลองจะกําหนดการแม็ปข้อมูลของใบแจ้งหนี้นามธรรม ที่ถูกรวมไว้ใน add-on ของการออกใบแจ้งหนี้ทางอิเล็กทรอนิกส์ เมื่อมีการส่งเอกสารอิเล็กทรอนิกส์
- **แบบจำลองบริบทใบแจ้งหนี้** – แบบจำลองบริบทใบแจ้งหนี้ช่วยให้คุณสามารถตั้งค่าคอนฟิกแบบจำลองบริบทใบแจ้งหนี้ ER และกําหนดบริบทของคุณลักษณะการออกใบแจ้งหนี้ทางอิเล็กทรอนิกส์
- **ชนิดการตอบสนอง** – ชนิดการตอบสนองช่วยให้คุณสามารถตั้งค่าคอนฟิกสิ่งที่ Add-on ของการออกใบแจ้งหนี้ทางอิเล็กทรอนิกส์ต้องอัปเดตใน Finance และ Supply Chain Management เป็นผลลัพธ์ของการประมวลผลใบแจ้งหนี้ทางอิเล็กทรอนิกส์

### <a name="formats"></a>รูปแบบ

รายการต่อไปนี้แสดงการตั้งค่าคอนฟิกรูปแบบ ER ที่พร้อมใช้งานสำหรับคุณลักษณะการออกใบแจ้งหนี้ทางอิเล็กทรอนิกส์

#### <a name="austrian-at-electronic-invoices-sales-and-project-invoices-for-austria"></a>ใบแจ้งหนี้อิเล็กทรอนิกส์ของออสเตรีย (AT): ใบแจ้งหนี้การขายและโครงการสำหรับออสเตรีย

- ใบแจ้งหนี้การขาย OIOUBL
- ใบแจ้งหนี้โครงการ OIOUBL
- ใบลดหนี้การขาย OIOUBL
- ใบลดหนี้โครงการ OIOUBL

#### <a name="belgian-be-electronic-invoice-sales-and-project-invoices-for-belgium"></a>ใบแจ้งหนี้อิเล็กทรอนิกส์ของเบลเยียม (BE): ใบแจ้งหนี้การขายและโครงการสำหรับเบลเยียม

- UBL ใบแจ้งหนี้การขาย BE
- UBL ใบแจ้งหนี้โครงการ BE
- UBL ใบลดหนี้โครงการ BE
- UBL ใบลดหนี้การขาย BE

#### <a name="brazilian-br-nf-e-nf-e-federal-brazil"></a>NF-e ของบราซิล (BR): NF-e Federal (บราซิล)

- NF-e ส่งรูปแบบการส่งออก (BR)
- NF-e รูปแบบการส่งออกจดหมายการแก้ไข (BR)
- NF-e ยกเลิกรูปแบบการส่งออก (BR)
- NF-e ละเว้นรูปแบบการส่งออก (BR)

#### <a name="brazilian-nfs-e-br-nfs-e-abrasf-curitiba-city"></a>NFS-e ของบราซิล (BR): NFS-e ABRASF เมือง Curitiba

- NFS-e ABRASF Curitiba (BR)
- NFS-e ABRASF สอบถาม Curitiba (BR)

#### <a name="brazilian-br-nfs-e-nfs-e-so-paulo-city"></a>NFS-e ของบราซิล (BR): NFS-e เมือง São Paulo

- NFS-e Sao Paulo (BR)

#### <a name="danish-dk-electronic-invoice-sales-and-project-invoices-for-denmark"></a>ใบแจ้งหนี้อิเล็กทรอนิกส์ของเดนมาร์ก (DK): ใบแจ้งหนี้การขายและโครงการสำหรับเดนมาร์ก

- ใบแจ้งหนี้การขาย OIOUBL
- ใบแจ้งหนี้โครงการ OIOUBL
- ใบลดหนี้การขาย OIOUBL
- ใบลดหนี้โครงการ OIOUBL

#### <a name="dutch-nl-electronic-invoice-sales-and-project-invoices-for-netherlands"></a>ใบแจ้งหนี้อิเล็กทรอนิกส์ของดัตช์ (NL): ใบแจ้งหนี้การขายและโครงการสำหรับดัตช์

- UBL ใบแจ้งหนี้การขาย NL
- UBL ใบแจ้งหนี้ของโครงการ NL
- UBL ใบลดหนี้ของโครงการ NL
- UBL ใบลดหนี้การขาย NL

#### <a name="egyptian-eg-electronic-invoice-sales-and-project-invoices-for-egypt"></a>ใบแจ้งหนี้อิเล็กทรอนิกส์ของอียิปต์ (EG): ใบแจ้งหนี้การขายและโครงการสำหรับอียิปต์

- ใบแจ้งหนี้การขาย (EG)(การออกใบแจ้งหนี้)
- ใบแจ้งหนี้โครงการ (EG)(การออกใบแจ้งหนี้)

#### <a name="estonian-ee-electronic-invoice-sales-and-project-invoices-for-estonia"></a>ใบแจ้งหนี้อิเล็กทรอนิกส์ของเอสโตเนีย (EE): ใบแจ้งหนี้การขายและโครงการสำหรับเอสโตเนีย

- ใบแจ้งหนี้การขาย (EE)
- ใบแจ้งหนี้โครงการ (EE)

#### <a name="finnish-fi-electronic-invoice-sales-and-project-invoices-for-finland"></a>ใบแจ้งหนี้อิเล็กทรอนิกส์ของฟินแลนด์ (FI): ใบแจ้งหนี้การขายและโครงการสำหรับฟินแลนด์

- ใบแจ้งหนี้การขาย (FI)
- ใบแจ้งหนี้โครงการ (FI)

#### <a name="french-fr-electronic-invoice-sales-and-project-invoices-for-france"></a>ใบแจ้งหนี้อิเล็กทรอนิกส์ของฝรั่งเศส (FR): ใบแจ้งหนี้การขายและโครงการสำหรับฝรั่งเศส

- UBL ใบแจ้งหนี้การขาย FR
- UBL ใบแจ้งหนี้โครงการ FR
- UBL ใบลดหนี้โครงการ FR
- UBL ใบลดหนี้การขาย FR

#### <a name="german-de-electronic-invoice-sales-and-project-invoices-for-germany"></a>ใบแจ้งหนี้อิเล็กทรอนิกส์ของเยอรมัน (DE): ใบแจ้งหนี้การขายและโครงการสำหรับเยอรมนี

- ใบแจ้งหนี้การขาย (DE)
- ใบแจ้งหนี้โครงการ (DE)

#### <a name="italian-it-electronic-invoice-sales-and-project-invoices-for-italy"></a>ใบแจ้งหนี้อิเล็กทรอนิกส์ของอิตาลี (IT): ใบแจ้งหนี้การขายและโครงการสำหรับอิตาลี

- ใบแจ้งหนี้การขาย (IT)
- ใบแจ้งหนี้ของโครงการ (IT)

#### <a name="mexican-mx-cfdi-cfdi-for-mexico"></a>CFDI ของเม็กซิโก (MX) : CFDI สำหรับเม็กซิโก

- รูปแบบใบแจ้งหนี้ CFDI (MX)
- บันทึกการจัดส่ง CFDI (MX)
- การโอนย้ายสินค้าคงคลัง CFDI (MX)
- รูปแบบการชำระเงิน CFDI (MX)
- รูปแบบการยกเลิกใบแจ้งหนี้ CFDI (MX)

#### <a name="norwegian-no-electronic-invoice-sales-and-project-invoices-for-norway"></a>ใบแจ้งหนี้อิเล็กทรอนิกส์ของนอร์เวย์ (NO): ใบแจ้งหนี้การขายและโครงการสำหรับนอร์เวย์

- ใบแจ้งหนี้การขาย OIOUBL
- ใบแจ้งหนี้โครงการ OIOUBL
- ใบลดหนี้การขาย OIOUBL
- ใบลดหนี้โครงการ OIOUBL

#### <a name="peppol-electronic-invoice-peppol-sales-and-project-invoices"></a>ใบแจ้งหนี้อิเล็กทรอนิกส์ PEPPOL: การขายและใบแจ้งหนี้โครงการของ PEPPOL

- ใบแจ้งหนี้การขาย PEPPOL
- ใบแจ้งหนี้โครงการ PEPPOL
- ใบลดหนี้การขาย PEPPOL
- ใบลดหนี้ของโครงการ PEPPOL

#### <a name="spanish-es-electronic-invoice-sales-and-project-invoices-for-spain"></a>ใบแจ้งหนี้อิเล็กทรอนิกส์ของสเปน (ES): ใบแจ้งหนี้การขายและโครงการสำหรับสเปน

- ใบแจ้งหนี้การขาย (ES)
- ใบแจ้งหนี้โครงการ (ES)

### <a name="actions"></a>การดำเนินการ

ตารางต่อไปนี้จะแสดงรายการการดำเนินการที่พร้อมใช้งาน และในขณะนี้จะพร้อมใช้งานโดยทั่วไป หรือยังอยู่ในพรีวิว

| การดำเนินการ                                        | คำอธิบาย                                                                  | ความพร้อมใช้งาน         |
|-----------------------------------------------|------------------------------------------------------------------------------|----------------------|
| แปลงเอกสาร                            | เรียกใช้รูปแบบการรายงานทางอิเล็กทรอนิกส์เพื่อแปลงเอกสาร                   | พร้อมใช้งานโดยทั่วไป  |
| ลงชื่อในเอกสาร xml                             | ลงชื่อในเอกสาร xml พร้อมด้วยลายเซ็นดิจิทัล                                   | ในการแสดงตัวอย่าง           |
| ลงชื่อในเอกสาร json สำหรับหน่วยงานจัดเก็บภาษีของอียิปต์ | ลงชื่อในเอกสาร json พร้อมด้วยลายเซ็นดิจิทัลสำหรับหน่วยงานจัดเก็บภาษีของอียิปต์       | พร้อมใช้งานโดยทั่วไป  |
| รวมกับบริการ ETA ของอียิปต์           | สื่อสารกับหน่วยงานจัดเก็บภาษีของอียิปต์                                     | พร้อมใช้งานโดยทั่วไป  |
| เรียกบริการ Brazilian SEFAZ                  | รวมกับบริการ SEFAZ ของบราซิลเพื่อการส่งเอกสารทางการเงิน       | ในการแสดงตัวอย่าง           |
| เรียกบริการ Mexican PAC                      | รวมกับบริการ PAC ของเม็กซิโกสำหรับการส่ง CFDI                      | ในการแสดงตัวอย่าง           |
| ประมวลผลการตอบสนอง                              | วิเคราะห์การตอบสนองที่ได้รับจากการเรียกบริการเว็บ                     | พร้อมใช้งานโดยทั่วไป  |
| ใช้ MS Power Automate                         | รวมกับโฟลว์ที่สร้างใน Microsoft Power Automate                       | ในการแสดงตัวอย่าง           |

## <a name="configuration-providers"></a>ผู้ให้บริการการตั้งค่าคอนฟิก

ผู้ให้บริการการตั้งค่าคอนฟิกจะให้คุณลักษณะการออกใบแจ้งหนี้ทางอิเล็กทรอนิกส์และส่วนประกอบ ER เช่น การแม็ปแบบจำลอง การตั้งค่าคอนฟิกรูปแบบ และแบบจำลองบริบท ซึ่งจะเผยแพร่คุณลักษณะการออกใบแจ้งหนี้ทางอิเล็กทรอนิกส์และส่วนประกอบ ER ในที่เก็บส่วนกลางที่เกี่ยวข้อง จากที่นั่น องค์กรอื่นสามารถดาวน์โหลดได้

ก่อนที่คุณจะตั้งค่าคอนฟิกคุณลักษณะการออกใบแจ้งหนี้ทางอิเล็กทรอนิกส์ผ่าน RCS คุณต้องตั้งค่าคอนฟิกองค์กรของคุณเองเป็นผู้ให้บริการการตั้งค่าคอนฟิกในโมดูล **การรายงานทางอิเล็กทรอนิกส์** สำหรับข้อมูลเกี่ยวกับวิธีการตั้งค่าผู้ให้บริการการตั้งค่าคอนฟิกเป็น **ใช้งานอยู่** ให้ดู [สร้างผู้ให้บริการการตั้งค่าคอนฟิก และทำเครื่องหมายเป็นใช้งานอยู่](../../fin-ops-core/dev-itpro/analytics/tasks/er-configuration-provider-mark-it-active-2016-11.md)

## <a name="viewing-electronic-invoicing-features-in-the-global-repository"></a>การดูคุณลักษณะการออกใบแจ้งหนี้ทางอิเล็กทรอนิกส์ในที่เก็บส่วนกลาง

หากต้องการเลือกดูคุณลักษณะการออกใบแจ้งหนี้ทางอิเล็กทรอนิกส์ที่พร้อมใช้งานในที่เก็บส่วนกลางสำหรับผู้ให้บริการการตั้งค่าคอนฟิกหนึ่งๆ ให้ซิงค์อินสแตนซ์ RCS ขององค์กรของคุณ หลังจากซิงโครไนส์เสร็จสิ้นแล้ว รายการของคุณลักษณะการออกใบแจ้งหนี้ทางอิเล็กทรอนิกส์ที่พร้อมใช้งานจะถูกอัปเดต

## <a name="importing-electronic-invoicing-features"></a>การนำเข้าคุณลักษณะการออกใบแจ้งหนี้ทางอิเล็กทรอนิกส์

ก่อนที่คุณจะใช้หรือตั้งค่าคอนฟิกคุณลักษณะการออกใบแจ้งหนี้ทางอิเล็กทรอนิกส์ คุณต้องนําเข้าไปยังอินสแตนซ์ RCS ขององค์กรของคุณ การดําเนินการนําเข้าจะสร้างสําเนาเฉพาะที่ของคุณลักษณะ และคัดลอกสิ่งประดิษฐ์ ER ทั้งหมดที่คุณลักษณะใช้ (ตัวอย่างเช่น จัดรูปแบบการตั้งค่าคอนฟิกและการตั้งค่าคอนฟิกแบบจำลอง) ไปยังอินสแตนซ์ RCS ขององค์กรของคุณ

คุณสามารถนําเข้าคุณลักษณะการออกใบแจ้งหนี้ทางอิเล็กทรอนิกส์จากผู้ให้บริการการตั้งค่าคอนฟิกใดๆ

## <a name="creating-electronic-invoicing-features"></a>การสร้างคุณลักษณะการออกใบแจ้งหนี้ทางอิเล็กทรอนิกส์

คุณสามารถสร้างคุณลักษณะการออกใบแจ้งหนี้ทางอิเล็กทรอนิกส์ได้ตั้งแต่เริ่มต้น หรือคุณสามารถสืบทอดมาจากคุณลักษณะการออกใบแจ้งหนี้ทางอิเล็กทรอนิกส์อื่น

เมื่อคุณสร้างคุณลักษณะการออกใบแจ้งหนี้ทางอิเล็กทรอนิกส์ตั้งแต่ต้น คุณต้องเพิ่มส่วนประกอบ ER ด้วยตนเอง (ตัวอย่างเช่น การตั้งค่าคอนฟิกรุ่นของคุณลักษณะและการตั้งค่าคอนฟิกอื่นๆ เช่น การตั้งค่ารุ่นของคุณลักษณะและการตั้งค่าแอปพลิเคชัน) เมื่อคุณสร้างคุณลักษณะโดยได้รับมาจากคุณลักษณะอื่น คุณลักษณะใหม่จะสืบทอดการตั้งค่าคอนฟิกทั้งหมดจากคุณลักษณะเดิม 

## <a name="electronic-invoicing-feature-version"></a>รุ่นของคุณลักษณะการออกใบแจ้งหนี้ทางอิเล็กทรอนิกส์

คุณลักษณะการออกใบแจ้งหนี้ทางอิเล็กทรอนิกส์ถูกกำหนดรุ่น เมื่อมีการสร้างรุ่นใหม่ จะมีการเพิ่มหมายเลขรุ่นโดยอัตโนมัติ วันที่ "มีผลบังคับ" สามารถกําหนดเป็นรุ่นใหม่ได้

รุ่นของคุณลักษณะการออกใบแจ้งหนี้ทางอิเล็กทรอนิกส์เป็นไปตามวงจรชีวิตที่มีสถานะสูงสุดสามสถานะดังนี้:

- **ร่าง** – ถ้ารุ่นของคุณลักษณะอยู่ในสถานะนี้ คุณสามารถแก้ไขแอททริบิวต์การตั้งค่าคอนฟิกและสิ่งประดิษฐ์ใดๆ (ตัวอย่างเช่น การตั้งค่าคอนฟิกรูปแบบไฟล์) ได้
- **เสร็จสมบูรณ์** – ถ้ารุ่นของคุณลักษณะอยู่ในสถานะนี้ ได้มีการเผยแพร่ไปยังที่เก็บส่วนกลางที่สัมพันธ์กับองค์กรของคุณแล้ว คุณไม่สามารถแก้ไขรุ่นของคุณลักษณะหรือส่วนประกอบ ER ใดๆ ได้อีกต่อไป
- **เผยแพร่แล้ว** – ถ้ารุ่นของคุณลักษณะอยู่ในสถานะนี้ ได้มีการเผยแพร่ไปยัง add-on ของการออกใบแจ้งหนี้ทางอิเล็กทรอนิกส์แล้ว คุณไม่สามารถแก้ไขรุ่นของคุณลักษณะหรือส่วนประกอบ ER ใดๆ ได้อีกต่อไป

### <a name="feature-configurations"></a>การตั้งค่าคอนฟิกคุณลักษณะ

การตั้งค่าคอนฟิกคุณลักษณะจัดเก็บการตั้งค่าคอนฟิกรูปแบบ ER ทั้งหมดที่คุณลักษณะการออกใบแจ้งหนี้ทางอิเล็กทรอนิกส์ใช้ ไฟล์อิเล็กทรอนิกส์ทั้งหมดที่ใช้คุณลักษณะการออกใบแจ้งหนี้ทางอิเล็กทรอนิกส์ในระหว่างการประมวลผล มาจากการตั้งค่าคอนฟิกรูปแบบที่ถูกเพิ่มในการตั้งค่าคอนฟิกคุณลักษณะของคุณลักษณะนั้น

จากการตั้งค่าคอนฟิกคุณลักษณะ คุณสามารถเข้าถึงตัวออกแบบรูปแบบ ER ซึ่งเป็นเครื่องมือ ER ที่ใช้ในการสร้างการตั้งค่าคอนฟิกรูปแบบ

### <a name="feature-setup"></a>การตั้งค่าคุณลักษณะ

การตั้งค่าคุณลักษณะถูกใช้ร่วมกับการตั้งค่าคอนฟิกคุณลักษณะต่างๆ การตั้งค่าคุณลักษณะแต่ละรายการจะสรุปชุดของการดำเนินการ กฎการใช้งาน และตัวแปรที่ให้พฤติกรรมที่คาดไว้ เพื่อให้คุณลักษณะการออกใบแจ้งหนี้ทางอิเล็กทรอนิกส์สามารถตอบสนองความต้องการเฉพาะของใบแจ้งหนี้อิเล็กทรอนิกส์

### <a name="application-setup"></a>การตั้งค่าแอปพลิเคชัน

การตั้งค่าแอปพลิเคชันต้องถูกเชื่อมโยงกับแอปพลิเคชันที่เชื่อมต่อที่สร้างไว้ก่อนหน้านี้

โดยผ่านการตั้งค่าแอปพลิเคชัน คุณสามารถตั้งค่าคอนฟิกส่วนของคุณลักษณะการออกใบแจ้งหนี้ทางอิเล็กทรอนิกส์ซึ่งต้องมีการดำเนินการใน Finance และ Supply Chain Management ส่วนประกอบที่ตั้งค่าคอนฟิกได้อย่างน้อยสามส่วนเป็นแบบบังคับ โดยไม่พิจารณาถึงคุณลักษณะการออกใบแจ้งหนี้ทางอิเล็กทรอนิกส์

- **ชื่อตาราง** – เอนทิตีใน Finance และ Supply Chain Management ซึ่งเก็บใบแจ้งหนี้ที่ลงรายการบัญชีไว้ และคุณลักษณะการออกใบแจ้งหนี้ทางอิเล็กทรอนิกส์อ้างอิง
- **บริบท** – ชื่อของแบบจำลองบริบทใบแจ้งหนี้ที่ตั้งค่าคอนฟิกโดยผ่าน ER
- **การแม็ปเอกสารทางธุรกิจ** – ชื่อของแบบจำลองการแม็ปใบแจ้งหนี้ที่ตั้งค่าคอนฟิกโดยผ่าน ER

> [!IMPORTANT]
> คุณสามารถดูการตั้งค่าคอนฟิกที่ป้อนในการตั้งค่าแอปพลิเคชันใน Finance และ Supply Chain Management ไปที่ **การจัดการองค์กร \> การตั้งค่า \> พารามิเตอร์เอกสารอิเล็กทรอนิกส์** บนแท็บ **เอกสารอิเล็กทรอนิกส์** ให้เลือก **ปรับใช้** แล้วจากนั้น เลือกตัวเลือก **แอปพลิเคชันที่เชื่อมต่อ**

### <a name="deploying-feature-versions"></a>การปรับใช้รุ่นของคุณลักษณะ

ใน RCS คุณใช้คำสั่ง **ปรับใช้** กับเป้าหมาย-เผยแพร่รุ่นของคุณลักษณะการออกใบแจ้งหนี้ทางอิเล็กทรอนิกส์ เลือก **ปรับใช้** แล้วจากนั้น เลือกตัวเลือกใดตัวเลือกหนึ่งต่อไปนี้ เพื่อกําหนดเป้าหมายของการปรับใช้ 

- **สภาพแวดล้อมบริการ** – เมื่อเป้าหมายของการปรับใช้เป็นสภาพแวดล้อมบริการ รุ่นของคุณลักษณะการออกใบแจ้งหนี้ทางอิเล็กทรอนิกส์จะถูกเผยแพร่ไปยังสภาพแวดล้อมบริการ Add-on ของการออกใบแจ้งหนี้ทางอิเล็กทรอนิกส์พร้อมแล้วที่จะรับและประมวลผลเอกสารอิเล็กทรอนิกส์ที่ Finance และ Supply Chain Management ส่ง
- **แอปพลิเคชันที่เชื่อมต่อ** – เมื่อเป้าหมายของการปรับใช้เป็นแอปพลิเคชันที่เชื่อมต่อ การตั้งค่าคอนฟิกที่การตั้งค่าแอปพลิเคชันให้ไว้จะถูกเขียนในอินสแตนซ์ Finance และ Supply Chain Management ที่เชื่อมโยงไว้ก่อนหน้านี้

เฉพาะรุ่นของคุณลักษณะการออกใบแจ้งหนี้ทางอิเล็กทรอนิกส์ที่มีสถานะเป็น **เสร็จสมบูรณ์** เท่านั้นที่สามารถปรับใช้กับสภาพแวดล้อมบริการ หรือแอปพลิเคชันที่เชื่อมต่อ

### <a name="removing-feature-versions"></a>การลบรุ่นของคุณลักษณะ

ใน RCS คุณใช้คำสั่ง **ยกเลิกปรับใช้** เพื่อลบรุ่นของคุณลักษณะการออกใบแจ้งหนี้ทางอิเล็กทรอนิกส์เฉพาะออกจากสภาพแวดล้อมบริการใน Add-on ของการออกใบแจ้งหนี้ทางอิเล็กทรอนิกส์

> [!IMPORTANT]
> คำสั่ง **ยกเลิกปรับใช้** ใช้ได้เฉพาะในสภาพแวดล้อมบริการเท่านั้น แต่จะไม่ลบรุ่นของคุณลักษณะการออกใบแจ้งหนี้ทางอิเล็กทรอนิกส์ออกจากแอปพลิเคชันที่เชื่อมต่อ

### <a name="rebasing-electronic-invoicing-features"></a>การปรับใช้ซ้ำรุ่นของคุณลักษณะการออกใบแจ้งหนี้ทางอิเล็กทรอนิกส์

เมื่อคุณลักษณะการออกใบแจ้งหนี้ทางอิเล็กทรอนิกส์หนึ่งรายการได้รับมาจากอีกคุณลักษณะหนึ่ง คำสั่ง **ปรับใช้ซ้ำ** จะอัปเดตคุณลักษณะที่ได้รับพร้อมกับการเปลี่ยนแปลงที่ได้รับการแนะนำในคุณลักษณะเดิม

## <a name="additional-resources"></a>ทรัพยากรเพิ่มเติม

- [การออกใบแจ้งหนี้อิเล็กทรอนิกส์ในการเงิน และ Supply Chain Management](e-invoicing-issuing-electronic-invoices-finance-supply-chain-management.md)
