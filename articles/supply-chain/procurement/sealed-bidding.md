---
title: การประมูลแบบเปิดสำหรับ RFQ
description: บทความนี้จะอธิบายวิธีตั้งค่าการประมูลที่ปิดผนึกเพื่อเก็บความลับในการตอบการประมูลให้แก่ผู้จัดจำหน่ายจนกว่าการประมูลจะถูกเปิดผนึกโดยบุคลากรจัดซื้อ
author: GalynaFedorova
ms.date: 08/02/2021
ms.topic: article
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: gfedorova
ms.search.validFrom: 2021-08-02
ms.dyn365.ops.version: 10.0.21
ms.openlocfilehash: 40f1735d7efa5131b1462963758b6b48eec78fea
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 06/03/2022
ms.locfileid: "8890899"
---
# <a name="sealed-bidding-for-rfqs"></a>การประมูลแบบเปิดสำหรับ RFQ

[!include [banner](../includes/banner.md)]

การประมูลที่ปิดผนึกเก็บความลับในการตอบการประมูลให้แก่ผู้จัดจำหน่ายจนกว่าการประมูลจะถูกเปิดผนึกโดยบุคลากรจัดซื้อ การประมูลทั้งหมดที่เกี่ยวข้องกับคําขอใบเสนอราคา (RFQ) จะพร้อมเปิดผนึกก่อนการประมูลหมดอายุ ก่อนที่การประมูลจะถูกเปิดออก เฉพาะผู้ใช้ที่มีบทบาทของผู้ใช้ที่ระบุและที่เป็นผู้จัดจำหน่ายเท่านั้นที่สามารถเข้าถึงการประมูลได้

> [!IMPORTANT]
> การปรับเปลี่ยนหรือการขยายฟอร์ม หรือการสร้างฟอร์มหรือตรรกะทางธุรกิจใหม่อาจครอบคลุมการปกป้องที่ Microsoft ให้ไว้เพื่อการประมูลที่ปิดผนึก คุณรับความเสี่ยงเกี่ยวกับการใช้การปรับเปลี่ยน ส่วนขยาย ฟอร์มใหม่ หรือตรรกะทางธุรกิจใดๆ หรือการไม่สามารถใช้งานคุณลักษณะการประมูลที่ปิดผนึกแล้วได้ เนื่องจากการแก้ไข ส่วนขยาย ฟอร์มใหม่ หรือตรรกะทางธุรกิจดังกล่าว  Microsoft จะไม่รับผิดชอบความเสียหายใด ๆ ที่เกิดขึ้นจากการปรับเปลี่ยนหรือส่วนขยายใด ๆ ไปยังฟอร์ม หรือฟอร์มใหม่หรือตรรกะทางธุรกิจใด ๆ ที่คุณสร้าง หรือบุคคลที่สามสร้างขึ้นเพื่อคุณ Microsoft ไม่ได้ให้การสนับสนุนทางเทคนิคหรืออื่น ๆ เกี่ยวกับการแก้ไข ส่วนขยาย ฟอร์มใหม่ หรือตรรกะทางธุรกิจใด ๆ ที่ทำโดยคุณหรือบุคคลที่สามในนามของคุณ คุณต้องรับผิดชอบในการปฏิบัติตามกฎหมายหรือข้อบังคับทั้งหมดที่เกี่ยวกับการประมูลที่ปิดผนึก

## <a name="how-bids-are-kept-secure"></a>วิธีรักษาความปลอดภัยของการประมูล

การประมูลที่ปิดผนึกแล้วจะใช้การเข้ารหัสแบบอสมมิติเพื่อเข้ารหัสคีย์การเข้ารหัสการประมูล (KEK) และการเข้ารหัสที่สมมาตรเพื่อเข้ารหัสการประมูลจริง ระบบจะรวม Microsoft Azure Key Vault เพื่อสร้างและจัดการคีย์การเข้ารหัสที่ใช้ในการเข้ารหัสการประมูลที่ปิดผนึก การประมูลแต่ละตัวจะมีคีย์การเข้ารหัสของตนเอง การเข้ารหัสนี้จะถูกเก็บรักษาไว้ใน Key Vault ซึ่งเป็นขององค์กรที่รัน Dynamics 365 Supply Chain Management ระบบเข้าถึง Key Vault ตามความต้องการ เมื่อใดก็ตามที่ต้องมีการเข้ารหัสและการถอดรหัส

## <a name="setup-and-configuration"></a>การตั้งค่าและการตั้งค่าคอนฟิก

ส่วนนี้จะอธิบายข้อกำหนดเบื้องต้นที่ต้องมีก่อนที่คุณจะสามารถส่งออก RFQ ที่ต้องใช้การประมูลที่ปิดผนึก

### <a name="step-1-set-up-user-access-to-sealed-bidding"></a>ขั้นตอนที่ 1: ตั้งค่าการเข้าถึงการประมูลที่ปิดผนึกของผู้ใช้

เมื่อคุณใช้การประมูลที่ปิดผนึก เฉพาะผู้ใช้ที่ตั้งค่าเป็นผู้ติดต่อสำหรับผู้จัดจำหน่ายเท่านั้นที่สามารถดู แก้ไข และส่งการประมูลให้กับผู้จัดจำหน่ายรายนั้นจนกว่ารอบระยะเวลาการการประมูลจะหมดอายุ ผู้ใช้เหล่านี้ต้องมีบทบาท **ผู้จัดจำหน่าย (ภายนอก)** และต้องมีการตั้งค่าเป็นผู้ติดต่อของบัญชีผู้จัดจำหน่าย ผู้ติดต่อต้องมีสิทธิ์ในการทำงานร่วมกันกับผู้จัดจำหน่าย ตามที่อธิบายไว้ใน [การตั้งค่าและรักษาการทำงานร่วมกันกับผู้จัดจำหน่าย](set-up-maintain-vendor-collaboration.md)

เนื่องจากผู้ใช้มีสิทธิ์ที่เหมาะสมและผู้ที่ตั้งค่าเป็นผู้ติดต่อของผู้จัดจำหน่ายสามารถเข้าถึงการประมูลที่ปิดผนึกไว้ของผู้ใช้ ดังนั้นจึงควรติดตามว่าผู้ใช้คือใคร ผู้ดูแลระบบที่ตั้งค่าผู้ใช้และบทบาทความปลอดภัยจะรับผิดชอบการจํากัดการเข้าถึงการประมูลที่ปิดผนึกไว้ให้กับผู้ใช้เหล่านั้นจริงๆ ที่ได้รับอนุญาตให้ดูได้

### <a name="step-2-enable-the-sealed-bidding-feature"></a>ขั้นตอนที่ 2: เปิดใช้งานคุณลักษณะการประมูลที่ปิดผนึก

ก่อนที่คุณจะเริ่มต้นการตั้งค่าหรือใช้คุณลักษณะนี้ คุณต้องตรวจสอบให้แน่ใจว่าพร้อมใช้งานในระบบของคุณ ผู้ดูแลระบบสามารถใช้พื้นที่ทำงาน **[การจัดการคุณลักษณะ](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md)** เพื่อตรวจสอบสถานะของคุณลักษณะ และเปิดใช้งาน ในพื้นที่ทำงาน **การจัดการคุณลักษณะ** มีการแสดงรายการคุณลักษณะในวิธีต่อไปนี้:

- **โมดูล:** *การจัดซื้อและการจัดหา*
- **ชื่อคุณลักษณะ:** *การประมูลที่ปิดผนึกของ RFQ*

### <a name="step-3-set-up-azure-key-vault"></a>ขั้นตอนที่ 3: ตั้งค่า Azure Key Vault

Supply Chain Management ใช้คีย์การเข้ารหัสเพื่อป้องกันการประมูลที่ปิดผนึกไว้ทั้งหมดและเก็บการประมูลเหล่านั้นไว้เป็นความลับจนกว่าจะถึงเวลาที่เหมาะสม ใช้ประโยชน์จากความสามารถหลักของ Key Vault เพื่อสร้างและจัดการคีย์ที่ต้องใช้ ดังนั้น คุณจึงต้องตั้งค่าการเชื่อมต่อจาก Supply Chain Management ไปยังคีย์หนึ่งๆ เพื่อเปิดใช้งานระบบ

> [!IMPORTANT]
> Key Vault ที่คุณใช้เพื่อการประมูลที่ปิดผนึกต้องเป็นไปตามข้อความต้องการต่อไปนี้:
>
> - ถ้าคุณใช้ Sandbox เพื่อการพัฒนาและการทดสอบ คุณจะต้องมี key vault เฉพาะหนึ่งๆ ให้กับ Sandbox และแยกอีกหนึ่งคีย์เป็นการใช้งานจริง
> - แต่ละ Key Vault ต้องสร้างขึ้นในการบอกรับเป็นสมาชิก Azure ที่เป็นขององค์กรของคุณ (ไม่ใช่การบอกรับเป็นสมาชิกที่คุณกำลังเรียกใช้ Supply Chain Management)
> - แต่ละ key vault ต้องใช้เฉพาะกับการประมูลที่ปิดผนึกแล้วเท่านั้น คุณต้องไม่ใช้ key vault การประมูลที่ปิดผนึกของคุณเพื่อวัตถุประสงค์อื่นใด

การประมูลทุกรายการจะดึงคีย์ข้อมูลลับของตนเอง คีย์นี้จะใช้ทุกครั้งที่ผู้ใช้ดู อัปเดต หรือเปิดการประมูล

Key Key สร้างคีย์ที่ใช้เพื่อดึงข้อมูลลับเมื่อผู้จัดจำหน่ายเลือก **การประมูล** ในอินเทอร์เฟสการทำงานร่วมกันกับผู้จัดจำหน่าย จากนั้น คีย์จะหมดอายุหลังจากเวลาที่กำหนดที่ผู้จัดการฝ่ายจัดซื้อตั้งค่าบนหน้า **พารามิเตอร์การจัดซื้อและการจัดหา** ใน Supply Chain Management หลังจากคีย์หมดอายุ ไม่มีใครสามารถดู แก้ไข หรือเปิดผนึกการประมูลได้ ดังนั้น จึงควรตั้งค่าคอนฟิกการหมดอายุของคีย์ให้มีเวลาเพียงพอที่จะให้กระบวนการการประมูลเสร็จสมบูรณ์

ในสามขั้นตอนถัดไป คุณจะตั้งค่าการเชื่อมต่อกับ Key Vault ก่อนอื่น คุณจะต้องตั้งค่า Key Vault เพื่อใช้กับการประมูลที่ปิดผนึก จากนั้น คุณจะตั้งค่าคอนฟิก Supply Chain Management เพื่อสื่อสารกับ Key Vault สุดท้าย คุณจะตั้งค่าเวลาหมดอายุของคีย์

### <a name="step-4-set-up-a-key-vault-to-use-with-sealed-bidding"></a>ขั้นตอนที่ 4: ตั้งค่า Key Vault เพื่อใช้กับการประมูลที่ปิดผนึก

หากต้องการตั้งค่า Key Vault ของคุณ ให้ทำตามขั้นตอนต่อไปนี้ ลำดับของขั้นตอนมีความสําคัญมาก

1. หากคุณยังไม่ได้ตั้งค่าการบอกรับเป็นสมาชิก Azure ซึ่งแยกต่างหากจากการสั่งซื้อโดยบอกรับเป็นสมาชิกที่คุณรัน Supply Chain Management อยู่ ให้ตั้งค่า
1. ตั้งค่า Key Vault ในพื้นที่เก็บข้อมูลของ Azure แยกต่างหากของคุณ สำหรับข้อมูลเพิ่มเติม ให้ดู [การรักษาพื้นที่เก็บข้อมูลของ Azure Key Vault](https://support.microsoft.com/help/4040294/maintaining-azure-key-vault-storage)
1. ตั้งค่าแอป Supply Chain Management เพื่อใช้งานเป็นไคลเอนต์ของ Key Vault ของคุณ สำหรับข้อมูลเพิ่มเติม ให้ดู [การตั้งค่าไคลเอนต์ของ Azure Key Vault](https://support.microsoft.com/help/4040305/setting-up-azure-key-vault-client)

### <a name="step-5-configure-key-vault-parameters-in-supply-chain-management"></a>ขั้นตอนที่ 5: ตั้งค่าคอนฟิกพารามิเตอร์ Key Vault ใน Supply Chain Management

เมื่อต้องการตั้งค่าคอนฟิก Supply Chain Management เพื่อสื่อสารกับ Key Vault ระหว่างการประมูลที่ปิดผนึก ให้ปฏิบัติตามขั้นตอนเหล่านี้

1. เข้าสู่ระบบ Supply Chain Management และไปที่ **การจัดการระบบ \> การตั้งค่า \> พารามิเตอร์ Key Vault**
1. เลือก **สร้าง** เพื่อสร้างเรกคอร์ด และตั้งค่าฟิลด์ต่อไปนี้:

    - **ชื่อ** – ให้ป้อนชื่อ
    - **คำอธิบาย** – ให้ป้อนคำอธิบาย
    - **URL ของ Key Vault** – ป้อน URL เริ่มต้นสำหรับ Key Vault ของคุณ
    - **ไคลเอนต์ Key Key** – ป้อนรหัสไคลเอนต์เชิงโต้ตอบของโปรแกรมประยุกต์ Active Directory ที่เชื่อมโยงกับ Key Vault เพื่อรับรองความถูกต้อง
    - **รหัสลับ Key Vault** – ป้อนข้อมูลอ้างอิงลับของใบรับรอง
    - **เปิดใช้งานการประมูลที่ปิดผนึก** – ตั้งค่าตัวเลือกนี้เป็น *ใช่*

![หน้าพารามิเตอร์ Key Vault](media/sealed-bidding-key-vault-param.png "หน้าพารามิเตอร์ Key Vault")

> [!NOTE]
> คุณสามารถเปิดใช้งานการตั้งค่าคอนฟิกหลักหนึ่ง Key Vault เท่านั้นในการประมูลที่ปิดผนึกในครั้งหนึ่งๆ ก่อนที่คุณจะปิดใช้งานการตั้งค่าคอนฟิก Key Vault ที่มีอยู่ คุณต้องตรวจสอบให้แน่ใจว่าการประมูลที่ปิดผนึกที่ใช้การตั้งค่าคอนฟิกนั้นเปิดผนึกทั้งหมด ตรวจสอบกรณี RFQ ทุกกรณีของชนิด *ที่ปิดผนึก* และตรวจสอบให้แน่ใจว่าการตอบทั้งหมดได้รับการเปิดผนึก

### <a name="step-6-set-the-key-expiration-time"></a>ขั้นตอนที่ 6: ตั้งค่าเวลาหมดอายุของคีย์

หากต้องการตั้งค่าเวลาหมดอายุที่ใช้กับคีย์ที่สร้างไว้ของการประมูลใหม่ทุกรายการ ให้ปฏิบัติตามขั้นตอนต่อไปนี้

1. ไปที่ **พารามิเตอร์การจัดซื้อและการจัดหา \> การตั้งค่า \> พารามิเตอร์การจัดซื้อและการจัดหา**
1. บนแท็บ **คำขอใบเสนอราคา** ในฟิลด์ **ออฟเซ็ตวัน** ป้อนจํานวนวันที่รอบระยะเวลา RFQ จะสิ้นสุด เมื่อมีการสร้าง RFQ จํานวนวันที่คุณป้อนที่นี่จะถูกบวกเพิ่มเข้าไปในวันที่ของระบบเพื่อกําหนดวันหมดอายุเริ่มต้นใน RFQ
1. ในฟิลด์ **ออฟเซ็ตวันหมดอายุของคีย์การเข้ารหัส** ให้ป้อนจํานวนวันที่คีย์การเข้ารหัสทุกรายการควรถูกต้อง หลังจากที่ออกคีย์นี้ หลังจากคีย์การเข้ารหัสหมดอายุ ไม่มีใครสามารถดู แก้ไข หรือเปิดผนึกการประมูลที่ปิดผนึกที่ใช้ได้

> [!TIP]
> ค่าของฟิลด์ **ออฟเซ็ตวันหมดอายุของคีย์การเข้ารหัส** ไม่ควรน้อยกว่าค่าของฟิลด์ **ออฟเซ็ตวัน**

### <a name="step-7-set-the-default-bid-type"></a><a name="set-default-bid-type"></a>ขั้นตอนที่ 7: ตั้งค่าชนิดการประมูลเริ่มต้น

ทุกกรณี RFQ จะมีชนิดการประมูล ชนิดการประมูลจะกําหนดว่ากรณี RFQ จะแสดงการประมูลแบบเปิดหรือที่ปิดผนึก

#### <a name="rfq-cases-that-dont-have-a-solicitation-type"></a>กรณี RFQ ที่ไม่ได้มีชนิดการร้องขอ

เมื่อต้องการตั้งค่าชนิดการประมูลเริ่มต้นที่จะมอบหมายให้กับกรณี RFQ ใหม่ที่ไม่ได้กำหนดชนิดการร้องขอเมื่อสร้างขึ้น ให้ปฏิบัติตามขั้นตอนต่อไปนี้

1. ไปที่ **พารามิเตอร์การจัดซื้อและการจัดหา \> การตั้งค่า \> พารามิเตอร์การจัดซื้อและการจัดหา**
1. บนแท็บ **ขอใบเสนอราคา** ให้ตั้งค่าฟิลด์ **ชนิดการประมูล** เป็น *ปิดผนึก*

#### <a name="rfq-cases-that-have-a-solicitation-type"></a>กรณี RFQ ที่มีชนิดการร้องขอ

เมื่อต้องการตั้งค่าชนิดการประมูลเริ่มต้นที่จะมอบหมายให้กับกรณี RFQ ใหม่ที่กำหนดชนิดการร้องขอเมื่อสร้างขึ้น ให้ปฏิบัติตามขั้นตอนต่อไปนี้

1. ไปที่ **การจัดซื้อและการจัดหา \> การตั้งค่า \> คำขอใบเสนอราคา \> ชนิดการร้องขอ**
1. สร้างชนิดการร้องขอใหม่ หรือเลือกชนิดการร้องขอที่มีอยู่ซึ่งคุณต้องการใช้ชนิดการประมูล *ปิดผนึก*
1. ตั้งค่าฟิลด์ **ชนิดการประมูล** เป็น *ปิดผนึก*
1. ทําขั้นตอนเหล่านี้ซ้ำกับทุกชนิดการร้องขอเพิ่มเติมที่คุณต้องการใช้การประมูลที่ปิดผนึก

> [!TIP]
> ชนิดการร้องขอไม่ต้องได้รับการมอบหมายเมื่อสร้าง RFQ ใหม่ ถ้ามีการมอบหมายชนิดการร้องขอ ชนิดการประมูลเริ่มต้นของ RFQ สามารถดึงข้อมูลได้ หรือสามารถใช้ชนิดการร้องขอเริ่มต้นที่กําหนดไว้ในพารามิเตอร์การจัดซื้อและการจัดหา

## <a name="the-sealed-bidding-process"></a>กระบวนการการประมูลที่ปิดผนึก

การประมูลที่ปิดผนึกแล้วจะเป็นไปตามกระบวนการตามที่อธิบายใน [ภาพรวมคําขอใบเสนอราคา (RFQ)](request-quotations.md) ความแตกต่างหลักคือข้อมูลการประมูลและเอกสารแนบจะถูกเข้ารหัสจนกว่าจะเปิดผนึกการประมูล

> [!IMPORTANT]
> [แบบสอบถาม](/dynamicsax-2012/appuser-itpro/view-and-respond-to-questionnaires) ไม่มีการเข้ารหัสและไม่ควรใช้ในการรวบรวมข้อมูลที่อ่อนไหว

นี่คือขั้นตอนสำของกระบวนการ:

1. คุณสามารถสร้างและส่ง RFQ ให้กับผู้จัดจำหน่ายหนึ่งรายขึ้นไป
1. ผู้จัดจำหน่ายตอบกลับโดยส่งการประมูลที่ปิดผนึกแล้ว
1. คุณเปิดผนึกการการประมูลหลังจากเวลาหมดอายุของรายการการประมูล
1. การประมูลจะปรากฏขึ้น และคุณสามารถประเมินและเปรียบเทียบการประมูลได้
1. เมื่อยอมรับการประมูลแล้ว คุณสร้างใบสั่งซื้อ สร้างข้อตกลงการซื้อ หรืออัปเดตใบขอซื้อ

### <a name="create-an-rfq-case-that-uses-sealed-bidding"></a>สร้างกรณี RFQ ที่ใช้การประมูลที่ปิดผนึก

กระบวนการสร้างกรณี RFQ ของการประมูลที่ปิดผนึกเกือบจะเหมือนกับกระบวนการของการประมูลที่ไม่ปิดผนึก สำหรับข้อมูลเพิ่มเติมเกี่ยวกับวิธีสร้างกรณี RFQ ทั้งสองชนิด โปรดดูที่ [สร้างคําขอใบเสนอราคา](tasks/create-request-quotation.md) ส่วนนี้จะเน้นข้อควรพิจารณาที่สําคัญสองสามอย่างเมื่อคุณสร้าง RFQ เพื่อการประมูลที่ปิดผนึก

กรณี RFQ ของการประมูลที่ปิดผนึกต้องมีค่า **ชนิดการประมูล** เป็น *ปิดผนึก* คุณสามารถกําหนดค่านี้ให้กับกรณี RFQ ได้สามวิธี:

- ตั้งค่าโดยตรงในกรณี RFQ หลังจากที่คุณสร้าง
- กําหนดการประมูลที่ปิดผนึกเป็นชนิดการประมูลเริ่มต้นส่งในกรณี RFQ ทั้งหมดในพารามิเตอร์การจัดซื้อและการจัดหา (ดูส่วน [ตั้งค่าชนิดการประมูลเริ่มต้น](#set-default-bid-type) ก่อนหน้าในบทความนี้)
- เมื่อคุณสร้างกรณี RFQ ใหม่ ให้เลือกชนิดการร้องขอที่ตั้งค่าไว้เพื่อการประมูลที่ปิดผนึก (ดูส่วน [ตั้งค่าชนิดการประมูลเริ่มต้น](#set-default-bid-type))

สำหรับการประมูลที่ปิดผนึก ค่า **วันและเวลาหมดอายุของกรณี RFQ** จะกําหนดขึ้นเมื่อสามารถเปิดผนึกการประมูลที่ส่ง ค่า **วันที่และเวลาหมดอายุ** ในแต่ละบรรทัดจะตรงกับค่าในส่วนหัว

คุณไม่สามารถเปลี่ยนชนิดการประมูลได้หลังจากส่งกรณี RFQ

### <a name="vendors-respond-to-an-rfq"></a>ผู้จัดจำหน่ายตอบกลับ RFQ

ผู้จัดจำหน่ายที่ตอบกลับการประมูลที่ปิดผนึกจะใช้กระบวนงานเดียวกันกับที่ใช้เพื่อตอบสนองต่อการประมูลที่เปิดอยู่ ตามที่อธิบายไว้ใน [การใช้งาน RFQ ในพื้นที่ทำงานการประมูลของผู้จัดจำหน่าย](vendor-collaboration-work-customers-dynamics-365-operations.md#working-with-rfqs-in-the-vendor-bidding-workspace) สำหรับคําแนะนําในรายละเอียดเกี่ยวกับวิธีการใช้งานทั้งการประมูลที่เปิดและการประมูลที่ปิดผนึก โปรดดูที่ [ป้อนและเปรียบเทียบการประมูล RFQ และสัญญารางวัล](tasks/enter-compare-rfq-bids-award-contracts.md) ความแตกต่างเพียงอย่างเดียวระหว่างการประมวลผลการประมูลที่ปิดผนึกและการประมวลผลการประมูลแบบเปิดคือ จนกว่ารอบระยะเวลาการประมูลจะหมดอายุลง ผู้เชี่ยวชาญด้านการจัดซื้อไม่สามารถเปิดการประมูลที่ปิดผนึกแล้วจากผู้จัดจำหน่ายได้ เฉพาะผู้ติดต่อสำหรับผู้จัดจำหน่ายเท่านั้นที่สามารถเปิดการประมูลที่ปิดผนึกแล้วของบุคคลนั้น

> [!IMPORTANT]
> สำหรับการประมูลที่ปิดผนึกแล้ว ผู้จัดจำหน่ายสามารถอัปโหลดเอกสารแนบในรูปแบบ PDF เท่านั้น รูปแบบอื่นจะไม่ได้รับการยอมรับ

หลังจากที่ผู้ใช้ที่เป็นผู้จัดจำหน่ายที่ลงทะเบียนไว้เลือก **ประมูล** ใน RFQ การประมูลที่ปิดผนึกแล้ว ผู้ใช้จะสามารถป้อนข้อมูลการประมูลของพวกเขาและข้อมูลนั้นจะถูกรักษาความปลอดภัย ผู้จัดจำหน่ายสามารถบันทึกงานของพวกเขาขณะที่จัดเตรียมการประมูล ส่งคืนไปบ่อยครั้งเท่าที่ต้องการ แล้วส่งงานเมื่อพร้อม ผู้จัดจำหน่ายสามารถดูการประมูลของพวกเขาหลังจากที่ส่งการประมูลแล้วได้ หากผู้จัดจำหน่ายต้องเปลี่ยนการประมูลหลังจากที่ส่งแล้ว พวกเขาสามารถเรียกคืน อัปเดต และส่งใหม่ได้ตลอดเวลาจนกว่ารอบระยะเวลาการการประมูลจะหมดอายุ

เงื่อนไขต่อไปนี้จะใช้ระหว่างการประมูลที่ปิดผนึกแล้ว:

- ระหว่างการประมูลที่ปิดผนึก ระบบจะสร้างสมุดรายวัน *คำขอใบเสนอราคา*
- เมื่อผู้จัดจำหน่ายส่งการประมูล สมุดรายวัน RFQ ที่ไม่มีรายการจะถูกสร้างขึ้นที่มีราคาที่ปิดผนึก
- หลังจากเปิดผนึกกรณีแล้ว สมุดรายวัน RFQ จะถูกสร้างขึ้นที่มีราคาและยอดเงิน คุณสามารถเข้าถึงสมุดรายวันนี้โดยเลือก **สมุดรายวันคำขอใบเสนอราคา** ในหน้า **คำขอใบเสนอราคาทั้งหมด**
- ระบบจัดเก็บบันทึกของแต่ละการดำเนินการที่ผู้ใช้ปฏิบัติการในการประมูลที่ปิดผนึก การดำเนินการเหล่านี้ได้แก่ การดู การแก้ไข และการบันทึกการประมูล บันทึกนี้จะปรากฏทั้งต่อผู้จัดจำหน่ายและต่อผู้เชี่ยวชาญด้านการจัดซื้อที่สามารถเข้าถึงการประมูลได้
- ขณะที่การประมูลมีความคืบหน้า ผู้เชี่ยวชาญด้านการจัดซื้อจะสามารถดูสถานะของการประมูลได้ จากนั้น สถานะจะเป็น *ผู้จัดจำหน่ายกำลังอัปเดต* หรือ *ส่งโดยผู้จัดจำหน่าย*
- สถานะของรายการในการประมูลที่ปิดผนึกจะเป็น *ส่งแล้ว* จนกว่าการประมูลจะถูกเปิดผนึก
- หากผู้จัดจำหน่ายเลือกที่จะปฏิเสธการประมูล การประมูลจะมีสถานะ **ความคืบหน้าของการตอบ** เป็น *ถูกปฏิเสธโดยผู้จัดจำหน่าย* บุคลากรจัดซื้อจะมองเห็นสถานะนี้ได้
- คําตอบในแบบสอบถาม **ไม่** จัดเก็บอยู่ในฟอร์มที่เข้ารหัสในฐานข้อมูล ดังนั้น จึงไม่ปิดผนึก อย่างไรก็ตาม การประมูลจะไม่สามารถมองเห็นได้ในอินเทอร์เฟสผู้ใช้ RFQ จนกว่ากรณีจะถูกเปิด

### <a name="all-sealed-bid-activities-are-logged"></a>บันทึกกิจกรรมการประมูลที่ปิดผนึกแล้วทั้งหมด

บันทึกโดยละเอียดจะบันทึกกิจกรรมและการดำเนินการทั้งหมดสำหรับการประมูล ล็อกกิจกรรมช่วยให้องค์กรสามารถระบุผู้ที่อัปเดตการประมูลในระหว่างอายุการใช้งานของการประมูลนั้น และเป็นการอัปเดตใด นอกจากนี้ องค์กรยังช่วยให้องค์กรสามารถยืนยันว่าเฉพาะบุคคลที่ได้รับอนุมัติเท่านั้นที่เข้าถึงการประมูลที่ปิดผนึก ล็อกกิจกรรมพร้อมใช้งานในหน้า **กิจกรรม** ของทุกการประมูล

### <a name="review-rfq-activity"></a>ตรวจทานกิจกรรม RFQ

ทุกการโต้ตอบกับการประมูลจะได้รับการบันทึกและสามารถดูบนหน้า **กิจกรรม** ได้ ในแผนภาพต่อไปนี้แสดงตัวอย่าง

![ตัวอย่างของหน้ากิจกรรม](media/sealed-bidding-rfq-activity.png "ตัวอย่างของหน้ากิจกรรม")

ผู้จัดจำหน่ายสามารถเข้าถึงหน้า **กิจกรรม** ได้โดยเลือก **กิจกรรม** ในหน้า **การประมูลที่ปิดผนึกแล้วของคำขอใบเสนอราคา** บุคลากรการจัดซื้อสามารถเข้าถึงได้โดยเลือก **กิจกรรม** ในหน้า **คำขอใบเสนอราคา** ล็อกกิจกรรมจะให้ความสามารถในการมองเห็นทั้งหมดระหว่างผู้จัดจำหน่ายและบุคลากรการจัดซื้อที่เข้าถึงการประมูลได้ ดังนั้น จึงสามารถแสดงการเข้าถึงโดยไม่ได้รับอนุญาตได้

### <a name="unseal-sealed-bids"></a>เปิดการประมูลที่ปิดผนึก

เมื่อค่า **วันที่และเวลาหมดอายุ** ที่ตั้งค่าคอนฟิกไว้ของกรณี RFQ การประมูลที่ปิดผนึกได้ผ่านแล้ว ปุ่ม **เปิดผนึก** จะพร้อมใช้งาน เลือก **เปิดผนึก** เพื่อเปิดผนึกการประมูลทั้งหมดให้กับกรณี RFQ ที่เลือก จากนั้น ข้อมูลการประมูลและเอกสารแนบทั้งหมดจะปรากฏเพื่อให้สามารถจัดการการตอบกรณีได้ นอกจากนี้ สมุดรายวันยังสร้างขึ้น ซึ่งประกอบด้วยข้อมูลการประมูลที่ส่งอีกด้วย

เหตุการณ์การเปิดผนึกจะได้รับการบันทึกและสามารถดูบนหน้า **กิจกรรม** ได้

### <a name="process-accepted-bids"></a>ประมวลผลการประมูลที่ยอมรับ

กระบวนการเปรียบเทียบและอนุมัติการประมูลที่ปิดผนึกไว้ก่อนหน้านี้เหมือนกับกระบวนการของการประมูลแบบเปิด สำหรับข้อมูลเพิ่มเติมเกี่ยวกับวิธีให้คะแนน เปรียบเทียบ ปฏิเสธ และยอมรับการประมูลที่ยังเปิดผนึก โปรดดูที่ [ป้อนและเปรียบเทียบการประมูล RFQ และสัญญารางวัล](tasks/enter-compare-rfq-bids-award-contracts.md)

## <a name="the-rfq-activity-log-can-never-be-deleted"></a>ล็อกกิจกรรม RFQ ไม่สามารถลบได้

ไม่มีใครสามารถทำได้ ไม่แม้กระทั่งผู้ดูแลระบบและฝ่ายสนับสนุนของ Microsoft สามารถแก้ไขหรือลบล็อกกิจกรรม RFQ ได้ ข้อจํากัดนี้ช่วยให้มั่นใจถึงความเป็นธรรมของกระบวนการการประมูลที่ปิดผนึก และยังช่วยให้มั่นใจว่าเก็บรักษาบันทึกการตรวจสอบบัญชีที่ถูกต้องไว้
