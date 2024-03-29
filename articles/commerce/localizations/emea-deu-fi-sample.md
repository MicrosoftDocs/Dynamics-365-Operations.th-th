---
title: ตัวอย่างการรวมบริการลงทะเบียนทางการเงินสำหรับเยอรมนี
description: บทความนี้อธิบายภาพรวมของตัวอย่างการรวมทางบัญชีสำหรับเยอรมนีใน Microsoft Dynamics 365 Commerce
author: EvgenyPopovMBS
ms.date: 10/04/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: josaw
ms.search.validFrom: 2020-05-29
ms.openlocfilehash: a725badbce498e4e7b35aecb2500e273586c7b77
ms.sourcegitcommit: 2bc6680dc6b12d20532d383a0edb84d180885b62
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 10/06/2022
ms.locfileid: "9631465"
---
# <a name="fiscal-registration-service-integration-sample-for-germany"></a>ตัวอย่างการรวมบริการลงทะเบียนทางการเงินสำหรับเยอรมนี

[!include [banner](../includes/banner.md)]
[!include [banner](../includes/preview-banner.md)]

บทความนี้อธิบายภาพรวมของตัวอย่างการรวมทางบัญชีสำหรับเยอรมนีใน Microsoft Dynamics 365 Commerce

เพื่อตอบสนองความต้องการทางการเงินท้องถิ่นของเครื่องบันทึกเงินสดในเยอรมนี ฟังก์ชัน Dynamics 365 Commerce ของเยอรมนีรวมถึงการรวมตัวอย่างของการขายหน้าร้าน (POS) กับบริการลงทะเบียนทางการเงินภายนอก ตัวอย่างจะขยาย [ฟังก์ชันการรวมทางการเงิน](fiscal-integration-for-retail-channel.md) โดยยึดตามโซลูชัน [EFR (ทะเบียนทางการเงินทางอิเล็กทรอนิกส์)](https://www.efsta.eu/de/fiskalloesungen/deutschland) จาก [EFSTA](https://www.efsta.eu/de/) และเปิดใช้งานการสื่อสารกับบริการ EFR ผ่านทางโปรโทคอล HTTPS บริการ EFR ควรโฮสต์ในสถานีฮาร์ดแวร์ของ Retail หรือคอมพิวเตอร์แยกต่างหากที่สามารถเชื่อมต่อได้จากสถานีฮาร์ดแวร์ ตัวอย่างมีให้ในรูปแบบของรหัสต้นฉบับ และเป็นส่วนหนึ่งของชุดการพัฒนาซอฟต์แวร์ (SDK) ของ Commerce

Microsoft ไม่ได้ปล่อยฮาร์ดแวร์ ซอฟต์แวร์ หรือเอกสารใดๆ จาก EFSTA หากต้องการทราบข้อมูลเพิ่มเติมเกี่ยวกับวิธีใช้งานโซลูชัน EFR และดําเนินงาน ให้ติดต่อ [EFSTA](https://www.efsta.eu/de/kontakt/kontakt)

## <a name="scenarios"></a>สถานการณ์จำลอง

สถานการณ์ต่อไปนี้ครอบคลุมอยู่ในตัวอย่างการรวมบริการลงทะเบียนทางการเงินสำหรับเยอรมนี

### <a name="sales-operations"></a>การดำเนินการขาย

- **การลงทะเบียนของการขายและคืนสินค้าด้วยเงินสดและการส่งคืนในบริการลงทะเบียนทางการเงิน:**

    การลงทะเบียนการดําเนินการขายประกอบด้วยขั้นตอนต่อไปนี้:

    1. การขึ้้นทะเบียนข้อมูลเริ่มต้นธุรกรรม

        การเริ่มต้นของแต่ละธุรกรรมจะถูกลงทะเบียนในองค์ประกอบความปลอดภัยทางเทคนิค (TSE) ที่เชื่อมต่อกับบริการ EFR เนื่องจากการลงทะเบียน TSE จะกําหนดรหัสธุรกรรม (TID)

    2. การขึ้้นทะเบียนข้อมูลสิ้นสุดธุรกรรม

        เมื่อธุรกรรมสรุปที่ POS จะลงทะเบียนโดยใช้ TID เดียวกันซึ่งถูกมอบหมายในระหว่างการลงทะเบียนการเริ่มต้นธุรกรรม ในขณะนั้น รายละเอียดข้อมูลธุรกรรมจะถูกส่งไปยังบริการลงทะเบียนทางการเงิน ข้อมูลนี้ประกอบด้วยข้อมูลบรรทัดการขาย และข้อมูลเกี่ยวกับส่วนลด การชำระเงิน และภาษี

    3. การรวบรวมการตอบสนองจากบริการลงทะเบียนทางการเงิน

        ข้อมูลความปลอดภัยได้รับจาก TSE ซึ่งเป็นส่วนหนึ่งของการตอบสนองและบันทึกไว้ในธุรกรรมในฐานข้อมูลช่องทาง ข้อมูลด้านความปลอดภัยประกอบด้วยข้อมูลต่อไปนี้:

        - TID
        - วันที่และเวลาเริ่มต้นของธุรกรรม
        - วันที่และเวลาสิ้นสุดของธุรกรรม
        - ตัวนับลายเซ็น
        - ตรวจสอบค่า
        - หมายเลขลำดับของสินค้าของ TSE

- **การลงทะเบียนใบสั่งของลูกค้าในบริการลงทะเบียนทางการเงิน:** กระบวนการลงทะเบียนเหมือนกับกระบวนการของการขายเงินสดและการขนส่งและการส่งกลับสินค้า
- **การลงทะเบียนของการดำเนินการที่เกี่ยวข้องกับบัตรของขวัญและการฝากเงิน:** กระบวนการลงทะเบียนเหมือนกับกระบวนการของการขายและการส่งคืนเงินสดและการคืนสินค้า

#### <a name="notifying-users-about-fiscal-registration-failures"></a>การแจ้งให้ผู้ใช้ทราบเกี่ยวกับความล้มเหลวของการลงทะเบียนทางการเงิน

บริการลงทะเบียนทางการเงินสามารถแจ้งเตือนผู้ใช้เกี่ยวกับความล้มเหลวที่เกิดขึ้นในระหว่างการลงทะเบียนทางการเงินได้สองวิธี:

- พิมพ์ข้อมูลเพิ่มเติมจากการตอบสนองในฟิลด์ **ข้อความข้อมูล** บนใบเสร็จ
- แสดงการแจ้งเตือนจากบริการทางการเงินเป็นข้อความของผู้ใช้ที่ POS

    > [!NOTE]
    > กลไกการแจ้งเตือนนี้ต้องการให้เปิดพารามิเตอร์ **แสดงการแจ้งเตือนการลงทะเบียนทางการเงิน** ในหน้า **โปรไฟล์ทางเทคนิคของตัวเชื่อมต่อ**

#### <a name="printing-receipts"></a>กำลังพิมพ์ใบเสร็จ

การพิมพ์ใบเสร็จเป็นข้อบังคับในเยอรมนี ใบเสร็จทั้งหมดต้องมีข้อมูลต่อไปนี้เป็นอย่างน้อย:

- ชื่อและที่อยู่ของบริษัท
- ข้อมูลเกี่ยวกับสินค้า รวมถึงราคาและปริมาณ
- ข้อมูลเกี่ยวกับการชำระเงินที่ได้รับ
- ข้อมูลเกี่ยวกับภาษี รวมถึงยอดเงินรวมต่ออัตราภาษี
- ข้อมูลความปลอดภัย:

    - TID
    - วันที่และเวลาเริ่มต้นของธุรกรรม
    - วันที่และเวลาสิ้นสุดของธุรกรรม
    - ตัวนับลายเซ็น
    - ตรวจสอบค่า
    - หมายเลขลำดับของสินค้าของ TSE

- ข้อความที่ให้ข้อมูล

> [!NOTE]
> คิวอาร์โค้ดยังสามารถพิมพ์บนใบเสร็จได้ แม้ว่าคิวอาร์โค้ดนั้นไม่บังคับ แต่แนะนำเป็นอย่างยิ่ง สำหรับข้อมูลเพิ่มเติมเกี่ยวกับวิธีการเรียกใช้คิวอาร์โค้ดเป็นส่วนหนึ่งขอองการตอบสนองจากบริการลงทะเบียนทางการเงิน ดูที่เอกสาร "EFR Guide \[DE\]" ที่เผยแพร่บนเว็บไซต์ [คู่มือ EFSTA](https://public.efsta.net/efr/)
>
> ฟิลด์ **ข้อความข้อมูล** ในใบเสร็จแสดงการแจ้งเตือนจากบริการลงทะเบียนทางการเงิน ตัวอย่างเช่น ถ้าอุปกรณ์ลายเซ็นเสียหาย คุณสามารถพิมพ์ข้อความพิเศษบนใบเสร็จได้

#### <a name="voided-suspended-and-recalled-transactions"></a>ธุรกรรมถูกยกเลิก ที่ระงับและเรียกคืนแล้ว

- มีการลงทะเบียนธุรกรรมที่ถูกยกเลิกเป็นคำขอเพื่อสิ้นสุดธุรกรรมในบริการลงทะเบียนทางการเงิน
- มีการลงทะเบียนธุรกรรมที่ถูกระงับเป็นคำขอเพื่อสิ้นสุดธุรกรรมในบริการลงทะเบียนทางการเงิน
- การเรียกคืนของมีการลงทะเบียนธุรกรรมที่ถูกระงับเป็นการเริ่มต้นของธุรกรรมใหม่ในบริการลงทะเบียนทางการเงิน

### <a name="non-sales-transactions-and-shift-closing"></a>ธุรกรรมที่ไม่เกี่ยวกับการขายและการปิดกะ

ธุรกรรมที่ไม่ใช่การขายต่อไปนี้มีการลงทะเบียนเป็นการดําเนินงานที่ไม่ใช่ทางการเงินในบริการลงทะเบียนทางการเงินโดยใช้แท็ก **NFS**:

- ตรวจนับยอดเงินเริ่มต้น
- การป้อนข้อมูลเศษเงินทอน
- การเอาเงินออก
- การนำเงินฝากเข้าเซฟ
- การนำเงินฝากเข้าธนาคาร
- บัญชีรายได้
- บัญชีค่าใช้จ่าย

การดําเนินงาน **ปิดกะ** ยังลงทะเบียนเป็นการดําเนินงานที่ไม่ใช่ทางการเงินในบริการลงทะเบียนทางการเงินโดยใช้แท็ก **NFS**:

### <a name="data-export-and-audit"></a>การส่งออกข้อมูลการตรวจสอบ

ธุรกรรมทั้งหมดต้องได้รับการลงชื่อโดย TSE เพื่อให้แน่ใจถึงการตรวจสอบความถูกต้อง ความถูกต้อง และความสมบูรณ์ของธุรกรรมนั้น และช่วยป้องกันการจัดการข้อมูลที่บันทึก

> [!WARNING]
> สามารถใช้ได้เฉพาะ TSE ที่ได้รับการรับรองเท่านั้น หากต้องการทราบข้อมูลเกี่ยวกับชนิดและรุ่นของ TSE ที่ได้รับการสนับสนุนในโซลูชัน EFR โปรดดูที่เอกสาร "EFR Guide \[DE\]" ที่เผยแพร่บนเว็บไซต์ [คู่มือ EFSTA](https://public.efsta.net/efr/) หากต้องการทราบข้อมูลเพิ่มเติมเกี่ยวกับวิธีเลือกและขอ TSA โปรดติดต่อ [EFSTA](https://www.efsta.eu/at/kontakt)

ข้อบังคับในเยอรมนีต้องการการสนับสนุนการส่งออก DSFinV-K การส่งออก DSFinV-K สามารถทริกเกอร์ในโซลูชัน EFR หากต้องการทราบข้อมูลเพิ่มเติมเกี่ยวกับการส่งออก DSFinV-K โปรดดูที่เอกสาร "EFR Guide \[DE\]" ที่เผยแพร่ในเว็บไซต์ [คู่มือ EFSTA](https://public.efsta.net/efr/)

### <a name="limitations-of-the-sample"></a>ข้อจํากัดของตัวอย่าง

บริการลงทะเบียนทางการเงินสนับสนุนเฉพาะสถานการณ์ที่ภาษีขายรวมอยู่ในราคาเท่านั้น ดังนั้น ต้องตั้งค่าตัวเลือก **ราคารวมภาษีขาย** เป็น **ใช่** ให้กับทั้งร้านค้าและลูกค้า

บริการทางการเงินไม่สนับสนุนสถานการณ์ที่มีการใช้รหัสภาษีขายมากกว่าหนึ่งรหัสกับรายการธุรกรรมเดียวกัน

กรอบงานการรวมทางการเงินไม่สนับสนุนใบเสนอราคาขาย ดังนั้น การดําเนินงานเหล่านั้นยังไม่ได้ลงทะเบียนในบริการทางการเงิน

## <a name="set-up-commerce-for-germany"></a>ตั้งค่า Commerce สำหรับเยอรมนี

ส่วนนี้อธิบายการตั้งค่า Commerce เฉพาะและที่แนะนำให้เลือกสำหรับเยอรมนี สำหรับข้อมูลการตั้งค่าเพิ่มเติม ดูที่ [โฮมเพจ Commerce](../index.md)

เพื่อใช้ฟังก์ชันเฉพาะของเยอรมนี คุณต้องระบุการตั้งค่าต่อไปนี้

- ในที่อยู่หลักของนิติบุคคล ให้ตั้งค่าฟิลด์ **ประเทศ/ภูมิภาค** เป็น **DEU** (เยอรมนี)
- ในโปรไฟล์ฟังก์ชัน POS ทุกร้านที่ตั้งอยู่ในเยอรมนี ให้ตั้งค่าฟิลด์รหัส **รหัส ISO** เป็น **DE** (เยอรมนี)

คุณต้องระบุการตั้งค่าต่อไปนี้สำหรับเยอรมนี ตรวจสอบให้แน่ใจว่าได้เรียกใช้งานการกระจายที่เหมาะสมหลังจากที่คุณเสร็จสิ้นการตั้งค่า

### <a name="set-up-vat-per-german-requirements"></a>การตั้งค่า VAT ต่อข้อกำหนดภาษาเยอรมัน

คุณต้องสร้างภาษีขาย กลุ่มภาษีขาย และกลุ่มภาษีขายของสินค้า คุณต้องตั้งค่าข้อมูลภาษีขายเกี่ยวกับผลิตภัณฑ์และบริการด้วย สำหรับข้อมูลเพิ่มเติมเกี่ยวกับวิธีการตั้งค่าและใช้คุณลักษณะภาษีขาย ดูที่ [ภาพรวมของภาษีขาย](../../finance/general-ledger/indirect-taxes-overview.md)

ในใบเสร็จการขาย คุณสามารถพิมพ์รหัสย่อของรหัสภาษีขาย (ตัวอย่างเช่น "A" หรือ "B") เมื่อต้องการให้ฟังก์ชันนี้พร้อมใช้งาน ให้ตั้งค่าฟิลด์ **รหัสสำหรับการพิมพ์** บนหน้า **รหัสภาษีขาย**

### <a name="set-up-stores"></a>ตั้งค่าร้านค้า

ในหน้า **ร้านค้าทั้งหมด** ให้อัปเดตรายละเอียดร้านค้า ตั้งค่าพารามิเตอร์ต่อไปนี้โดยเฉพาะ:

- ในฟิลด์ **กลุ่มภาษีขาย** ให้ระบุกลุ่มภาษีขายที่ควรจะใช้สำหรับการขายให้กับลูกค้าเริ่มต้น
- ตั้งค่าตัวเลือก **ราคารวมภาษีขาย** เป็น **ใช่**
- ตั้งค่าฟิลด์ **ชื่อ** เป็นชื่อบริษัท การเปลี่ยนแปลงนี้ช่วยให้มั่นใจว่าชื่อบริษัทจะปรากฏในใบเสร็จ หรือคุณสามารถเพิ่มชื่อบริษัทในโครงร่างใบเสร็จการขายเป็นข้อความรูปแบบอิสระ
- ตั้งค่าฟิลด์ **หมายเลขรหัสภาษี (TIN)** เป็นหมายเลขรหัสบริษัท การเปลี่ยนแปลงนี้ช่วยให้มั่นใจว่าหมายเลขรหัสการชำระเงินของบริษัทจะปรากฏในใบเสร็จ หรือคุณสามารถเพิ่มหมายเลขประจำตัวผู้เสียภาษีบริษัทในโครงร่างใบเสร็จการขายเป็นข้อความรูปแบบอิสระ

### <a name="set-up-functionality-profiles"></a>ตั้งค่าโพรไฟล์ฟังก์ชัน

ตั้งค่าโปรไฟล์ฟังก์ชัน POS บน FastTab **การกำหนดหมายเลขใบเสร็จ** ให้ตั้งค่าการกำหนดหมายเลขใบเสร็จโดยการสร้างหรืออัปเดตเรกคอร์ดสำหรับชนิดของธุรกรรมใบเสร็จ **การขาย** **ใบสั่งขาย** และ **การส่งคืน**

### <a name="configure-custom-fields-so-that-they-can-be-used-in-receipt-formats-for-sales-receipts"></a>ตั้งค่าคอนฟิกฟิลด์ที่กําหนดเองเพื่อให้สามารถใช้ฟิลด์เหล่านั้นในรูปแบบใบเสร็จของใบเสร็จได้

คุณสามารถตั้งค่าคอนฟิกข้อความภาษาและฟิลด์ที่กําหนดเองที่ใช้ในรูปแบบใบเสร็จ POS ได้ บริษัทเริ่มต้นของผู้ใช้ที่สร้างการตั้งค่าใบเสร็จควรเป็นนิติบุคคลเดียวกันที่มีการสร้างการตั้งค่าข้อความภาษาขึ้น หรือควรสร้างข้อความภาษาเดียวกันในทั้งบริษัทเริ่มต้นของผู้ใช้และนิติบุคคลของร้านค้าที่มีการสร้างการตั้งค่าให้

ในหน้า **ข้อความภาษา** ให้เพิ่มเรกคอร์ดต่อไปนี้ของป้ายชื่อของฟิลด์แบบกำหนดเองเป็นโครงร่างของใบเสร็จ โปรดทราบว่ามีเพียงค่า **รหัสภาษา** **รหัสข้อความ** และ **ข้อความ** ที่แสดงในตารางเท่านั้น คุณสามารถเปลี่ยนเพื่อให้ตรงกับความต้องการของคุณได้ อย่างไรก็ตาม ค่า **รหัสข้อความ** ที่คุณใช้ต้องเป็นค่าเฉพาะ และต้องเท่ากับหรือมากกว่า 900001

เพิ่มป้ายชื่อ POS ต่อไปนี้ลงในส่วน **POS** ของหน้า **ข้อความภาษา**

| รหัสภาษา | รหัสข้อความ | ข้อความ                                  |
|-------------|---------|---------------------------------------|
| th       | 900001  | คิวอาร์โค้ด                               |
| th       | 900002  | รหัสธุรกรรม                        |
| th       | 900003  | รหัสการพิมพ์การขายปลีกภาษี                 |
| th       | 900004  | ยอดเงินภาษี (การขาย)                    |
| th       | 900005  | ฐานภาษี (การขาย)                     |
| th       | 900006  | วันที่/เวลาเริ่มต้นของธุรกรรม           |
| th       | 900007  | วันที่/เวลาสิ้นสุดของธุรกรรม             |
| th       | 900008  | หมายเลขลำดับประจำสินค้าขององค์ประกอบความปลอดภัย |
| th       | 900009  | ตัวนับลายเซ็น                     |
| th       | 900010  | ตรวจสอบค่า                           |
| th       | 900011  | ข้อความข้อมูล                          |

ในหน้า **ฟิลด์ที่กำหนดเอง** ให้เพิ่มเรกคอร์ดต่อไปนี้ของฟิลด์แบบกำหนดเองเป็นโครงร่างของใบเสร็จ โปรดทราบว่าค่า **รหัสข้อความคำอธิบาย** ต้องสอดคล้องกับค่า **รหัสข้อความ** ที่คุณระบุไว้ในหน้า **ข้อความภาษา**

| ชื่อ                            | ชนิด    | รหัสข้อความของคำอธิบาย |
|---------------------------------|---------|-----------------|
| QRCODE\_DE                      | ใบเสร็จรับเงิน | 900001          |
| TRANSACTIONID\_DE               | ใบเสร็จรับเงิน | 900002          |
| RETAILPRINTCODE\_DE             | ใบเสร็จรับเงิน | 900003          |
| SALESTAXAMOUNT\_DE              | ใบเสร็จรับเงิน | 900004          |
| SALESTAXBASIS\_DE               | ใบเสร็จรับเงิน | 900005          |
| TRANSACTIONSTARTDATETIME\_DE    | ใบเสร็จรับเงิน | 900006          |
| TRANSACTIONENDDATETIME\_DE      | ใบเสร็จรับเงิน | 900007          |
| SECURITYELEMENTSERIALNUMBER\_DE | ใบเสร็จรับเงิน | 900008          |
| SIGNCOUNTER\_DE                 | ใบเสร็จรับเงิน | 900009          |
| SIGN\_DE                        | ใบเสร็จรับเงิน | 900010          |
| INFOMESSAGE\_DE                 | ใบเสร็จรับเงิน | 900011          |

> [!NOTE]
> คุณควรระบุชื่อฟิลด์ที่ศุลกากรซึ่งถูกต้อง ตามที่แสดงรายการไว้ในตารางก่อนหน้า ชื่อฟิลด์ที่กำหนดเองไม่ถูกต้องจะทําให้เกิดข้อมูลที่ขาดหายไปในใบเสร็จ

### <a name="configure-receipt-formats"></a>ตั้งค่าคอนฟิกรูปแบบใบเสร็จ

สำหรับรูปแบบใบเสร็จที่จำเป็นทั้งหมด ให้เปลี่ยนค่าของฟิลด์ **ลักษณะการพิมพ์** เป็น **พิมพ์เสมอ**

ในตัวออกแบบรูปแบบใบเสร็จ ให้เพิ่มฟิลด์ที่กำหนดเองต่อไปนี้ลงในส่วนใบเสร็จที่เหมาะสม โปรดสังเกตว่าชื่อฟิลด์จะตรงกับข้อความภาษาที่คุณกําหนดไว้ในส่วนก่อนหน้านี้

- **ชื่อเรื่อง:** เพิ่มฟิลด์ต่อไปนี้:

    - ฟิลด์ **ชื่อร้านค้า** และ **หมายเลขประจำตัวผู้เสียภาษี** ซึ่งจะใช้พิมพ์ชื่อบริษัทและหมายเลขประจำตัวผู้เสียภาษีบนใบเสร็จ หรือคุณสามารถเพิ่มชื่อบริษัทและหมายเลขประจำตัวผู้เสียภาษีในโครงร่างเป็นข้อความรูปแบบอิสระ
    - ฟิลด์ **ที่อยู่ร้านค้า** **วันที่** **เวลา 24 ชั่วโมง** **หมายเลขใบเสร็จ** และ **หมายเลขลงทะเบียน**

- **รายการ:** เพิ่มฟิลด์ต่อไปนี้:

    - ฟิลด์ **ชื่อรายการ**
    - ฟิลด์ **ปริมาณ**
    - ฟิลด์ **ราคารวมพร้อมภาษี**
    - ฟิลด์ **รหัสการพิมพ์การขายปลีกภาษี** ซึ่งจะใช้พิมพ์รหัสย่อที่ตรงกับรหัสภาษีขายที่ใช้กับสินค้า

- **ส่วนท้าย:** เพิ่มฟิลด์ต่อไปนี้:

    - ฟิลด์การชำระเงิน ดังนั้นมีการพิมพ์ยอดการชำระเงินของวิธีการชำระเงินแต่ละวิธี ตัวอย่างเช่น เพิ่มฟิลด์ **ชื่อการชำระเงิน** และ **ยอดการชำระเงิน** ลงในบรรทัดใดบรรทัดหนึ่งของโครงร่าง
    - ฟิลด์ในกลุ่มฟิลด์ **การแบ่งภาษี** ฟิลด์ทั้งหมดในกลุ่มฟิลด์นี้ต้องพิมพ์บนบรรทัดที่แยกต่างหาก

        - ฟิลด์ **รหัสภาษี** ซึ่งเป็นฟิลด์มาตรฐานที่เปิดใช้งานสรุปภาษีขายที่จะพิมพ์ให้กับแต่ละรหัสภาษีขาย ฟิลด์ต้องมีการเพิ่มบรรทัดใหม่
        - ฟิลด์ **เปอร์เซ็นต์ภาษี** ซึ่งเป็นฟิลด์มาตรฐานที่ใช้พิมพ์อัตราภาษีที่มีผลบังคับของรหัสภาษีขาย
        - ฟิลด์ **ฐานภาษี (การขาย)** ใช้พิมพ์ยอดขายเงินสดรวมของใบเสร็จรับเงินสำหรับรหัสภาษีขาย การชำระเงินล่วงหน้าและการดําเนินงานบัตรของขวัญจะไม่รวม
        - ฟิลด์ **ยอดเงินภาษี (การขาย)** ใช้พิมพ์ยอดเงินภาษีของใบเสร็จรับเงินสำหรับการขายเงินสดสำหรับรหัสภาษีขาย
        - ฟิลด์ **รหัสการพิมพ์การขายปลีกภาษี** ซึ่งจะใช้พิมพ์รหัสย่อที่ตรงกับรหัสภาษีขาย

    - ฟิลด์ที่มีข้อมูลธุรกรรมที่มีการรักษาความปลอดภัยซึ่งส่งคืนโดยบริการลงทะเบียนทางการเงิน

        - ฟิลด์ **รหัสธุรกรรม** ซึ่งระบุหมายเลขของธุรกรรมเงินสดในบริการลงทะเบียนทางการเงิน
        - ฟิลด์ **วันที่และเวลาเริ่มต้นของธุรกรรม**
        - ฟิลด์ **วันที่และเวลาสิ้นสุดของธุรกรรม**
        - ฟิลด์ **หมายเลขลำดับประจำสินค้าขององค์ประกอบความปลอดภัย**
        - ฟิลด์ **ตัวนับลายเซ็น**
        - ฟิลด์ **ตรวจสอบค่า**
        - ฟิลด์ **คิวอาร์โค้ด** ซึ่งใช้ในการพิมพ์การอ้างอิงถึงธุรกรรมเงินสดที่ลงทะเบียนไว้ในรูปแบบของรหัส IN

        > [!NOTE]
        > ค่า **คิวอาร์โค้ด** จะถูกดึงมาจากการตอบสนองทะเบียนทางการเงิน EFR ส่งคืนคิวอาร์โค้ดในการตอบสนองของรหัสนั้นเฉพาะเมื่อค่าของฟิลด์ **แอตทริบิวต์** ในการตั้งค่าคอนฟิก EFR มีอธิบายอยู่ในคู่มือ EFSTA รูปแบบคิวอาร์โค้ดในฟิลด์ **แอตทริบิวต์** ในการตั้งค่าคอนฟิก EFR ต้องถูกกําหนดเป็น **BMP**

    - ฟิลด์ **ข้อความข้อมูล** เพื่อให้ข้อความการแจ้งเตือนจากบริการลงทะเบียนทางการเงินสามารถแสดงในใบเสร็จ ตัวอย่างเช่น ถ้าอุปกรณ์ลายเซ็นเสียหาย คุณสามารถพิมพ์ข้อความพิเศษบนใบเสร็จได้

หากต้องการทราบข้อมูลเพิ่มเติมเกี่ยวกับวิธีการใช้งานรูปแบบใบเสร็จ โปรดดูที่ [การตั้งค่าและออกแบบรูปแบบใบเสร็จ](../receipt-templates-printing.md)

## <a name="set-up-fiscal-integration-for-germany"></a>ตั้งค่าการรวมทางการเงินสำหรับเยอรมนี

ตัวอย่างการรวมบริการลงทะเบียนทางการเงินของเยอรมนียึดตาม [ฟังก์ชันการรวมทางการเงิน](fiscal-integration-for-retail-channel.md) และเป็นส่วนหนึ่งของ Commerce SDK ตัวอย่างอยู่ในโฟลเดอร์ **src\\FiscalIntegration\\Efr** ของที่เก็บ [โซลูชัน Dynamics 365 Commerce](https://github.com/microsoft/Dynamics365Commerce.Solutions/) [ตัวอย่าง](fiscal-integration-for-retail-channel.md#fiscal-registration-process-and-fiscal-integration-samples-for-fiscal-devices-and-services) ประกอบด้วยตัวให้บริการเอกสารทางการเงิน ซึ่งเป็นส่วนขยายของ Commerce Runtime (CRT) และตัวเชื่อมต่อทางการเงิน ซึ่งเป็นส่วนขยายของ Commerce Hardware Station สำหรับข้อมูลเพิ่มเติมเกี่ยวกับวิธีการใช้ Commerce SDK ให้ดูที่ [ดาวน์โหลดตัวอย่าง Commerce SDK และแพคเกจการอ้างอิงจาก GitHub NuGet](../dev-itpro/retail-sdk/sdk-github.md) และ [ตั้งค่าไปป์ไลน์การสร้างให้กับ SDK การจัดทำแพคเกจแบบอิสระ](../dev-itpro/build-pipeline.md)

> [!NOTE]
> ตัวอย่างการรวมบริการลงทะเบียนทางการเงินของเยอรมนี มีอยู่ใน Commerce SDK ณ Commerce เวอร์ชัน 10.0.29 ใน Commerce เวอร์ชัน 10.0.28 หรือก่อนหน้านั้น คุณต้องใช้รุ่นก่อนหน้าของ Retail SDK บนเครื่องเสมือนของนักพัฒนา (VM) ใน Microsoft Dynamics Lifecycle Services (LCS) หากต้องการข้อมูลเพิ่มเติม โปรดดูที่ [แนวทางการปรับใช้งานตัวอย่างการรวมทางการเงินของเยอรมนี (ดั้งเดิม)](emea-deu-fi-sample-sdk.md)

ปฏิบัติตามขั้นตอนการตั้งค่าการรวมทางการเงินตามที่อธิบายไว้ใน [การตั้งค่าการรวมทางการเงินของช่องทาง Commerce](setting-up-fiscal-integration-for-retail-channel.md):

1. [ตั้งค่ากระบวนการการลงทะเบียนทางการเงิน](setting-up-fiscal-integration-for-retail-channel.md#set-up-a-fiscal-registration-process) นอกจากนี้ ให้จดบันทึกการตั้งค่าต่างๆ ของกระบวนการลงทะเบียนทางการเงินที่ใช้กับ [ตัวอย่างการรวมบริการลงทะเบียนทางการเงินนี้โดยเฉพาะ](#set-up-the-registration-process)
1. [กำหนดการตั้งค่าการจัดการข้อผิดพลาด](setting-up-fiscal-integration-for-retail-channel.md#set-error-handling-settings)

    > [!WARNING]
    > ข้อผิดพลาดในการจัดการความสามารถของกรอบงานการรวมทางการเงิน อาจไม่สอดคล้องกับข้อบังคับทางการเงินเฉพาะที่
    >
    > - เราขอแนะนำให้คุณปิดตัวเลือก **ดำเนินการต่อเมื่อมีข้อผิดพลาด** บนหน้า **กระบวนการลงทะเบียนทางการเงิน** เนื่องจากธุรกรรมทั้งหมดต้องลงทะเบียนอย่างถูกต้อง แม้ว่าความพยายามครั้งแรกในการลงทะเบียนทางการเงินจะไม่ประสบความสาเร็จ
    > - ก่อนที่คุณจะเปิดตัวเลือก **ข้าม** หรือ **เลือกเป็นลงทะเบียน** บนหน้า **กระบวนการลงทะเบียนทางการเงิน** คุณควรอธิบายการเปลี่ยนแปลงเหล่านี้ต่อกระบวนการลงทะเบียนทางการเงินกับที่ปรึกษาภาษีของคุณหรือสํานักงานภาษีท้องถิ่น

1. [เปิดใช้งานการดำเนินการด้วยตนเองของการลงทะเบียนทางการเงินที่ถูกเลื่อน](setting-up-fiscal-integration-for-retail-channel.md#enable-manual-execution-of-deferred-fiscal-registration)
1. [ตั้งค่าคอนฟิกส่วนประกอบช่องทาง](#configure-channel-components)

### <a name="set-up-the-registration-process"></a>ตั้งค่ากระบวนการลงทะเบียน

เมื่อต้องการเปิดใช้งานกระบวนการการลงทะเบียน ให้ทําตามขั้นตอนต่อไปนี้เพื่อตั้งค่า Commerce headquarters สำหรับข้อมูลเพิ่มเติม ดูที่ [ตั้งค่าการรวมทางการเงินสำหรับช่องทาง Commerce](setting-up-fiscal-integration-for-retail-channel.md#set-up-a-fiscal-registration-process)

1. ดาวน์โหลดไฟล์การตั้งค่าคอนฟิกสำหรับผู้ให้บริการเอกสารทางการเงินและตัวเชื่อมต่อทางการเงิน:

    1. เปิดที่เก็บ [โซลูชัน Dynamics 365 Commerce](https://github.com/microsoft/Dynamics365Commerce.Solutions/)
    1. เลือกรุ่นสาขาที่นำออกใช้ที่ถูกต้องตามรุ่น SDK/แอปพลิเคชันของคุณ
    1. เปิด **src \> FiscalIntegration \> Efr**
    1. ดาวน์โหลดไฟล์การตั้งค่าคอนฟิกผู้ให้บริการเอกสารทางการเงินที่ **Configurations \> DocumentProviders \> DocumentProviderFiscalEFRSampleGermany.xml**
    1. ดาวน์โหลดไฟล์การตั้งค่าคอนฟิกตัวเชื่อมต่อทางการเงินที่ **Configurations \> Connectors \> ConnectorEFRSample.xml**

    > [!NOTE]
    > ใน Commerce เวอร์ชัน 10.0.28 หรือก่อนหน้า คุณต้องใช้เวอร์ชันก่อนหน้าของ Retail SDK บน VM สำหรับนักพัฒนาใน LCS ไฟล์การตั้งค่าคอนฟิกของตัวอย่างการรวมทางการเงินนี้อยู่ในโฟลเดอร์ต่อไปนี้ของ Retail SDK บน VM สำหรับนักพัฒนาใน LCS:
    >
    > - **ไฟล์การตั้งค่าคอนฟิกผู้ให้บริการเอกสารทางการเงิน:** RetailSdk\\SampleExtensions\\CommerceRuntime\\Extensions.DocumentProvider.EFRSample\\Configuration\\DocumentProviderFiscalEFRSampleGermany.xml
    > - **ไฟล์การตั้งค่าคอนฟิกตัวเชื่อมต่อทางการเงิน:** RetailSdk\\SampleExtensions\\HardwareStation\\Extension.EFRSample\\Configuration\\ConnectorEFRSample.xml

1. ไปที่ **Retail และ Commerce \> การตั้งค่าศูนย์ควบคุม \> พารามิเตอร์ \> พารามิเตอร์ที่ใช้ร่วมกันของ Commerce** บนแท็บ **ทั่วไป** ให้ตั้งค่าตัวเลือก **เปิดใช้งานการรวมทางการเงิน** เป็น **ใช่**
1. ไปที่ **การขายปลีกและการค้า \> การตั้งค่าช่องทาง \> การรวมทางการเงิน \> ผู้ให้บริการเอกสารทางการเงิน** และโหลดไฟล์การตั้งค่าคอนฟิกผู้ให้บริการเอกสารทางการเงินที่คุณดาวน์โหลดก่อนหน้านี้
1. ไปที่ **การขายปลีกและการค้า \> การตั้งค่าช่องทาง \> การรวมทางการเงิน \> ตัวเชื่อมต่อทางการเงิน** และโหลดไฟล์การตั้งค่าคอนฟิกตัวเชื่อมต่อทางการเงินที่คุณดาวน์โหลดก่อนหน้านี้
1. ไปที่ **การขายปลีกและการพาณิชย์ \> การตั้งค่าช่องทางการขาย \> การรวมทางการเงิน \> โปรไฟล์ฟังก์ชันของตัวเชื่อมต่อ** สร้างโปรไฟล์ฟังก์ชันของตัวเชื่อมต่อใหม่ เลือกผู้ให้บริการเอกสารและตัวเชื่อมต่อที่คุณโหลดไว้ก่อนหน้านี้ อัปเดต [การตั้งค่าการแมปข้อมูล](#default-data-mapping) ตามที่ต้องการ
1. ไปที่ **การขายปลีกและการพาณิชย์ \> การตั้งค่าช่องทางการขาย \> การรวมทางการเงิน \> โปรไฟล์ทางเทคนิคของตัวเชื่อมต่อ** สร้างโปรไฟล์ทางเทคนิคของตัวเชื่อมต่อใหม่ และเลือกตัวเชื่อมต่อทางการเงินที่คุณโหลดไว้ก่อนหน้านี้ อัปเดต [การตั้งค่าตัวเชื่อมต่อ](#fiscal-connector-settings) ตามที่ต้องการ
1. ไปที่ **การขายปลีกและการพาณิชย์ \> การตั้งค่าช่องทางการขาย \> การรวมทางการเงิน \> กลุ่มตัวเชื่อมต่อทางการเงิน** สร้างกลุ่มตัวเชื่อมต่อทางการเงินใหม่สำหรับโปรไฟล์ฟังก์ชันของตัวเชื่อมต่อที่คุณสร้างไว้ก่อนหน้านี้
1. ไปที่ **การขายปลีกและการพาณิชย์ \> การตั้งค่าช่องทางการขาย \> การรวมทางการเงิน \> กระบวนการลงทะเบียนทางการเงิน** สร้างกระบวนการลงทะเบียนทางการเงินใหม่และขั้นตอนกระบวนการลงทะเบียนทางการเงิน และเลือกกลุ่มตัวเชื่อมต่อทางการเงินที่คุณสร้างก่อนหน้านี้
1. ไปที่ **การขายปลีกและการค้า \> การตั้งค่าช่องทาง \> การตั้งค่า POS \> โพรไฟล์POS \> โพรไฟล์ฟังก์ชัน** เลือกโปรไฟล์ฟังก์ชันที่เชื่อมโยงกับร้านค้าที่ควรมีการเรียกใช้งานกระบวนการลงทะเบียน บน FastTab **กระบวนการลงทะเบียนทางการเงิน** ให้เลือกกระบวนการลงทะเบียนทางการเงินที่คุณสร้างไว้ก่อนหน้านี้
1. ไปที่ **การขายปลีกและการค้า \> การตั้งค่าช่องทาง \> การตั้งค่า POS \> โพรไฟล์POS \> โปรไฟล์ฮาร์ดแวร์** เลือกโปรไฟล์ฮาร์ดแวร์ที่เชื่อมโยงกับสถานีฮาร์ดแวร์ที่บริการลงทะเบียนทางการเงินจะเชื่อมต่อด้วย บน FastTab **อุปกรณ์ต่อพ่วงทางการเงิน** ให้เลือกโปรไฟล์ทางเทคนิคของตัวเชื่อมต่อที่คุณสร้างก่อนหน้านี้
1. เปิดกำหนดการจัดจำหน่าย (**การขายปลีกและการค้า \> การขายปลีกและการค้าไอที \> กำหนดการจัดจำหน่าย**) และเลือกงาน **1070** และ **1090** เพื่อโอนย้ายข้อมูลไปยังฐานข้อมูลช่องทาง

#### <a name="default-data-mapping"></a>การแมปข้อมูลเริ่มต้น

การแมปข้อมูลเริ่มต้นต่อไปนี้รวมอยู่ในการตั้งค่าคอนฟิกผู้ให้บริการเอกสารทางการเงินที่ให้ไว้โดยเป็นส่วนหนึ่งของตัวอย่างการรวมทางการเงิน:

- **การแมปชนิดการชำระเงิน** – การแมปวิธีการชำระเงินกับค่าของแอตทริบิวต์ **PayG** (กลุ่มการเงิน) ในคําขอที่ส่งให้กับบริการทางการเงิน ต่อไปนี้เป็นการแมปเริ่มต้น:

    ```
    1: 0; 2: 1; 3: 3; 4: 8; 5: 2; 6: 0; 7: 7; 8: 6; 9: 0; 10: 8; 11: 1
    ```

    ส่วนประกอบแรกในแต่ละคู่แสดงวิธีการชำระเงินที่ตั้งค่าไว้ให้กับร้านค้า ส่วนประกอบที่สองจะแสดงถึงกลุ่มการชำระเงินที่ตรงกันซึ่งบริการลงทะเบียนทางการเงิน EFR รองรับ หากต้องการทราบข้อมูลเพิ่มเติมเกี่ยวกับกลุ่มการชำระเงินที่ EFR สนับสนุนสำหรับเยอรมนี โปรดดูที่ [ข้อมูลอ้างอิง EFR](https://public.efsta.net/efr/)

    การแมปตัวอย่างของวิธีการชำระเงินจะตรงกับวิธีการชำระเงินของร้านค้าที่ตั้งค่าคอนฟิกในข้อมูลสาธิตมาตรฐาน

    | วิธีการชำระเงิน | ชื่อวิธีการชำระเงิน |
    |----------------|---------------------|
    | 1              | เงินสด                |
    | 2              | ตรวจสอบ               |
    | 3              | บัตร                |
    | 4              | บัญชีลูกค้า    |
    | 5              | อื่นๆ               |
    | 6 ชั่วโมง              | สกุลเงิน            |
    | 7              | ใบสำคัญ             |
    | 8              | บัตรของขวัญ           |
    | 9              | เอาเงิน/เศษเงินทอนออก |
    | 10             | บัตรสมาชิก       |
    | 11             | การตรวจสอบที่ไม่ใช่เฉพาะที่    |

    ดังนั้น คุณต้องปรับเปลี่ยนการแมปตัวอย่างตามวิธีการชำระเงินที่ตั้งค่าคอนฟิกในแอปพลิเคชันของคุณ

- **รวมข้อมูลลูกค้า** – ถ้าพารามิเตอร์นี้เปิดอยู่ คำขอไปยังบริการทางการเงินจะมีข้อมูลลูกค้า เช่น ชื่อและที่อยู่ ในกรณีที่มีการเพิ่มลูกค้าให้กับธุรกรรม
- **ภาษีมูลค่าเพิ่ม (VAT)** – การแมปค่าเปอร์เซ็นต์ภาษีที่ตั้งค่าไว้ให้กับรหัสภาษีขายกับค่าของแอตทริบิวต์ **TaxG** (กลุ่มภาษี) ในคำขอที่ส่งไปยังบริการทางการเงิน ต่อไปนี้เป็นการแมปเริ่มต้น:

    ```
    A: 19.00; B: 7.00; C: 10.70; D: 5.50; E: 0.00
    ```

    ส่วนประกอบที่แรกในแต่ละคู่จะแสดงถึงกลุ่มภาษี VAT ซึ่งบริการลงทะเบียนทางการเงิน EFR รองรับ ส่วนประกอบที่สองจะแสดงถึงอัตรา VAT ที่เกี่ยวข้อง หากต้องการทราบข้อมูลเพิ่มเติมเกี่ยวกับกลุ่มภาษี VAT ที่ EFR สนับสนุนสำหรับเยอรมนี โปรดดูที่ [ข้อมูลอ้างอิง EFR](https://public.efsta.net/efr/)

- **กลุ่มภาษีของบัตรของขวัญและเงินฝาก** – มูลค่าของแอตทริบิวต์ **TaxG** ในคำขอที่ส่งไปยังบริการทางการเงิน ตามการดําเนินงานที่เกี่ยวข้องกับบัตรของขวัญหรือเงินฝาก ต่อไปนี้เป็นการแมปเริ่มต้น:

    ```
    G
    ```

- **กลุ่มภาษีการยกเว้น VAT** – มูลค่าของแอตทริบิวต์ **TaxG** ในคำขอที่ส่งไปยังบริการทางการเงินตามการดําเนินงานที่ได้รับยกเว้นจากข้อผูกมัดภาษี ต่อไปนี้เป็นการแมปเริ่มต้น:

    ```
    F
    ```

> [!NOTE]
> การตั้งค่าภาษีในการแมปข้อมูลเริ่มต้นจะรับผิดชอบการตั้งค่าภาษีที่ตรงกันในระบบและกลุ่มภาษีในบริการ EFR กลุ่มภาษีสามารถพิมพ์บนใบเสร็จได้เฉพาะเมื่อตั้งค่าฟิลด์ **รหัสสำหรับการพิมพ์** บนหน้า **รหัสภาษีขาย** เท่านั้น

#### <a name="fiscal-connector-settings"></a>การตั้งค่าตัวเชื่อมต่อทางการเงิน

การตั้งค่าต่อไปนี้รวมอยู่ในการตั้งค่าคอนฟิกตัวเชื่อมต่อทางการเงินที่ให้ไว้โดยเป็นส่วนหนึ่งของตัวอย่างการรวมทางการเงิน:

- **ที่อยู่ปลายทาง** – URL ของบริการลงทะเบียนทางการเงิน
- **การหมดเวลา** – จํานวนเวลาเป็นมิลลิวินาที ซึ่งตัวเชื่อมต่อทางการเงินจะรอการตอบสนองจากบริการลงทะเบียนทางการเงิน
- **แสดงการแจ้งเตือนการลงทะเบียนทางการเงิน** – แฟล็กนี้จะควบคุมว่าควรจะแสดงการส่งคืนบริการลงทะเบียนทางการเงินต่อผู้ปฏิบัติงานหรือไม่

### <a name="configure-channel-components"></a>ตั้งค่าคอนฟิกส่วนประกอบช่องทาง

> [!NOTE]
> - ตัวอย่างการรวมบริการลงทะเบียนทางการเงินของเยอรมนี มีอยู่ใน Commerce SDK ณ Commerce เวอร์ชัน 10.0.29 ใน Commerce เวอร์ชัน 10.0.28 หรือก่อนหน้า คุณต้องใช้เวอร์ชันก่อนหน้าของ Retail SDK บน VM สำหรับนักพัฒนาใน LCS หากต้องการข้อมูลเพิ่มเติม โปรดดูที่ [แนวทางการปรับใช้งานตัวอย่างการรวมทางการเงินของเยอรมนี (ดั้งเดิม)](emea-deu-fi-sample-sdk.md)
> - ตัวอย่าง Commerce ที่มีการปรับใช้ในสภาพแวดล้อมของคุณ ไม่ได้รับการอัปเดตโดยอัตโนมัติเมื่อคุณใช้การอัปเดตบริการหรือคุณภาพกับส่วนประกอบของ Commerce คุณต้องอัปเดตตัวอย่างที่ต้องใช้ด้วยตนเอง

#### <a name="set-up-the-development-environment"></a>ตั้งค่าสภาพแวดล้อมการพัฒนา

หากต้องการตั้งค่าสภาพแวดล้อมการพัฒนาเพื่อทดสอบและขยายตัวอย่าง ให้ปฏิบัติตามขั้นตอนต่อไปนี้

1. ลอกแบบหรือดาวน์โหลดที่เก็บ [โซลูชัน Dynamics 365 Commerce](https://github.com/microsoft/Dynamics365Commerce.Solutions) เลือกรุ่นสาขาที่นำออกใช้ที่ถูกต้องตามรุ่น SDK/แอปพลิเคชันของคุณ สำหรับข้อมูลเพิ่มเติม โปรดดูที่ [ดาวน์โหลดตัวอย่าง Commerce SDK และแพคเกจอ้างอิงจาก GitHub และ NuGet](../dev-itpro/retail-sdk/sdk-github.md)
1. เปิดโซลูชัน EFR ที่ **Dynamics365Commerce.Solutions\\FiscalIntegration\\Efr\\EFR.sln** แล้วสร้างโซลูชันนี้
1. ติดตั้งส่วนขยาย Commerce Runtime:

    1. ค้นหาตัวติดตั้งส่วนขยาย CRT:

        - **Commerce Scale Unit:** ในโฟลเดอร์ **Efr\\ScaleUnit\\ScaleUnit.EFR.Installer\\bin\\Debug\\net461** ให้ค้นหาตัวติดตั้ง **ScaleUnit.EFR.Installer**
        - **CRT เฉพาะที่บน Modern POS:** ในโฟลเดอร์ **Efr\\ModernPOS\\ModernPOS.EFR.Installer\\bin\\Debug\\net461** ให้ค้นหาตัวติดตั้ง **ModernPOS.EFR.Installer**

    1. เริ่มต้นตัวติดตั้งส่วนขยาย CRT จากบรรทัดใบสั่ง:

        - **Commerce Scale Unit:**

            ```Console
            ScaleUnit.EFR.Installer.exe install --verbosity 0
            ```

        - **CRT เฉพาะที่บน Modern POS:**

            ```Console
            ModernPOS.EFR.Installer.exe install --verbosity 0
            ```

1. ติดตั้งส่วนขยายของตัวเชื่อมต่อทางการเงิน:

    คุณสามารถติดตั้งส่วนขยายของตัวเชื่อมต่อทางการเงินบน [สถานีฮาร์ดแวร์](fiscal-integration-for-retail-channel.md#fiscal-registration-is-done-via-a-device-connected-to-the-hardware-station) หรือ [เครื่องบันทึกเงินสด POS](fiscal-integration-for-retail-channel.md#fiscal-registration-is-done-via-a-device-or-service-in-the-local-network)

    1. ติดตั้งส่วนขยายสถานีฮาร์ดแวร์:

        1. ในโฟลเดอร์ **Efr\\HardwareStation\\HardwareStation.EFR.Installer\\bin\\Debug\\net461** ให้ค้นหาตัวติดตั้ง **HardwareStation.EFR.Installer**
        1. เริ่มต้นตัวติดตั้งส่วนขยายจากบรรทัดใบสั่งโดยเรียกใช้คำสั่งต่อไปนี้

            ```Console
            HardwareStation.EFR.Installer.exe install --verbosity 0
            ```

    1. ติดตั้งส่วนขยาย POS:

        1. เปิดโซลูชันตัวอย่างตัวเชื่อมต่อทางการเงิน POS ที่ **Dynamics365Commerce.Solutions\\FiscalIntegration\\PosFiscalConnectorSample\\Contoso.PosFiscalConnectorSample.sln** และสร้าง
        1. ในโฟลเดอร์ **PosFiscalConnectorSample\\StoreCommerce.Installer\\bin\\Debug\\net461** ให้ค้นหาตัวติดตั้ง **Contoso.PosFiscalConnectorSample.StoreCommerce.Installer**
        1. เริ่มต้นตัวติดตั้งส่วนขยายจากบรรทัดใบสั่งโดยเรียกใช้คำสั่งต่อไปนี้

            ```Console
            Contoso.PosFiscalConnectorSample.StoreCommerce.Installer.exe install --verbosity 0
            ```

#### <a name="production-environment"></a>สภาพแวดล้อมการทำงานจริง

ปฏิบัติตามขั้นตอนต่างๆ ใน [การตั้งค่าไปป์ไลน์การสร้างตัวอย่างการรวมทางการเงิน](fiscal-integration-sample-build-pipeline.md) เพื่อสร้างและปล่อย Cloud Scale Unit และแพคเกจที่ปรับใช้ได้แบบบริการตนเองในตัวอย่างการรวมทางการเงิน ไฟล์ YAML เทมเพลต **EFR build-pipeline.yml** สามารถพบได้ในโฟลเดอร์ **Pipeline\\YAML_Files** ของที่เก็บ [Dynamics 365 Commerce Solutions](https://github.com/microsoft/Dynamics365Commerce.Solutions)

## <a name="design-of-extensions"></a>การออกแบบของส่วนขยาย

ตัวอย่างการรวมบริการลงทะเบียนทางการเงินของเยอรมนียึดตาม [ฟังก์ชันการรวมทางการเงิน](fiscal-integration-for-retail-channel.md) และเป็นส่วนหนึ่งของ Commerce SDK ตัวอย่างอยู่ในโฟลเดอร์ **src\\FiscalIntegration\\Efr** ของที่เก็บ [โซลูชัน Dynamics 365 Commerce](https://github.com/microsoft/Dynamics365Commerce.Solutions/) [ตัวอย่าง](fiscal-integration-for-retail-channel.md#fiscal-registration-process-and-fiscal-integration-samples-for-fiscal-devices-and-services) ประกอบด้วยตัวให้บริการเอกสารทางการเงิน ซึ่งเป็นส่วนขยายของ CRT และตัวเชื่อมต่อทางการเงิน ซึ่งเป็นส่วนขยายของ Commerce Hardware Station สำหรับข้อมูลเพิ่มเติมเกี่ยวกับวิธีการใช้ Commerce SDK ให้ดูที่ [ดาวน์โหลดตัวอย่าง Commerce SDK และแพคเกจการอ้างอิงจาก GitHub NuGet](../dev-itpro/retail-sdk/retail-sdk-overview.md) และ [ตั้งค่าไปป์ไลน์การสร้างให้กับ SDK การจัดทำแพคเกจแบบอิสระ](../dev-itpro/build-pipeline.md)

> [!NOTE]
> ตัวอย่างการรวมบริการลงทะเบียนทางการเงินของเยอรมนี มีอยู่ใน Commerce SDK ณ Commerce เวอร์ชัน 10.0.29 ใน Commerce เวอร์ชัน 10.0.28 หรือก่อนหน้า คุณต้องใช้เวอร์ชันก่อนหน้าของ Retail SDK บน VM สำหรับนักพัฒนาใน LCS หากต้องการข้อมูลเพิ่มเติม โปรดดูที่ [แนวทางการปรับใช้งานตัวอย่างการรวมทางการเงินของเยอรมนี (ดั้งเดิม)](emea-deu-fi-sample-sdk.md)

### <a name="crt-extension-design"></a>การออกแบบของส่วนขยาย CRT

วัตถุประสงค์ของส่วนขยายที่เป็นผู้ให้บริการเอกสารทางการเงินคือการสร้างเอกสารเฉพาะบริการ และจัดการการตอบสนองจากบริการลงทะเบียนทางการเงิน

#### <a name="request-handler"></a>ตัวจัดการคำขอ

มีตัวจัดการคำขอหนึ่งตัวจัดการสำหรับตัวจัดการเอกสาร **DocumentProviderEFRFiscalDEU** ตัวจัดการนี้ใช้ในการสร้างเอกสารทางการเงินเกี่ยวกับบริการลงทะเบียนทางการเงิน ซึ่งสืบทอดมาจากอินเทอร์เฟส **INamedRequestHandler** วิธีการ **HandlerName** จะรับผิดชอบการส่งคืนชื่อของตัวจัดการ ชื่อตัวจัดการควรตรงกับชื่อผู้ให้บริการเอกสารตัวเชื่อมต่อที่ระบุใน Commerce headquarters

ตัวเชื่อมต่อสนับสนุนคำขอต่อไปนี้:

- **GetFiscalDocumentDocumentProviderRequest** – คำขอนี้จะมีข้อมูลเกี่ยวกับเอกสารใดที่ควรถูกสร้างขึ้น โดยจะส่งคืนเอกสารเฉพาะบริการที่ควรลงทะเบียนในบริการลงทะเบียนทางการเงิน
- **GetFiscalTransactionExtendedDataDocumentProviderRequest** – คำขอนี้จะส่งคืนการตอบสนองพร้อมกับข้อมูลแบบขยาย

#### <a name="configuration"></a>การกำหนดค่า

ไฟล์การตั้งค่าคอนฟิกสำหรับผู้ให้บริการเอกสารทางการเงินอยู่ที่ **src\\FiscalIntegration\\Efr\\Configurations\\DocumentProviders\\DocumentProviderFiscalEFRSampleGermany.xml** ในที่เก็บ [โซลูชัน Dynamics 365 Commerce](https://github.com/microsoft/Dynamics365Commerce.Solutions/) วัตถุประสงค์ของไฟล์คือเพื่อเปิดใช้งานการตั้งค่าของผู้ให้บริการเอกสารทางการเงินที่จะตั้งค่าคอนฟิกจาก Commerce headquarters รูปแบบไฟล์จะสอดคล้องกับข้อกําหนดของการตั้งค่าคอนฟิกการรวมทางการเงิน

### <a name="hardware-station-extension-design"></a>การออกแบบส่วนขยายสถานีฮาร์ดแวร์

วัตถุประสงค์ของส่วนขยายที่เป็นตัวเชื่อมต่อทางการเงินคือเพื่อสื่อสารกับบริการลงทะเบียนทางการเงิน

ส่วนขยายของสถานีฮาร์ดแวร์คือ **HardwareStation.Extension.EFRSample** ส่วนขยายนี้ใช้โปรโทคอล HTTP เพื่อส่งเอกสารที่ส่วนขยาย CRT สร้างขึ้นไปยังบริการลงทะเบียนทางการเงิน และยังจัดการการตอบสนองที่ได้รับจากบริการลงทะเบียนทางการเงินด้วย

#### <a name="request-handler"></a>ตัวจัดการคำขอ

ตัวจัดการคำขอ **EFRHandler** เป็นจุดเข้าใช้งานเพื่อจัดการคำขอไปยังบริการลงทะเบียนทางการเงิน ตัวจัดการสืบทอดมาจากอินเทอร์เฟส **INamedRequestHandler** วิธีการ **HandlerName** จะรับผิดชอบการส่งคืนชื่อของตัวจัดการ ชื่อตัวจัดการควรตรงกับชื่อตัวเชื่อมต่อทางการเงินที่ระบุใน Commerce headquarters

ตัวเชื่อมต่อสนับสนุนคำขอต่อไปนี้:

- **SubmitDocumentFiscalDeviceRequest** – คำขอนี้จะส่งเอกสารไปยังบริการลงทะเบียนทางการเงินและส่งคืนการตอบสนองจากบริการลงทะเบียนทางการเงิน
- **IsReadyFiscalDeviceRequest** – คำขอนี้ใช้เพื่อตรวจสอบความสมบูรณ์ของบริการลงทะเบียนทางการเงิน
- **InitializeFiscalDeviceRequest** – คำขอนี้ใช้สำหรับการเริ่มต้นบริการลงทะเบียนทางการเงิน

#### <a name="configuration"></a>การกำหนดค่า

ไฟล์การตั้งค่าคอนฟิกของตัวเชื่อมต่อทางการเงินอยู่ที่ **src\\FiscalIntegration\\Efr\\Configurations\\Connectors\\ConnectorEFRSample.xml** ในที่เก็บ [โซลูชัน Dynamics 365 Commerce](https://github.com/microsoft/Dynamics365Commerce.Solutions/) วัตถุประสงค์ของไฟล์คือเพื่อเปิดใช้งานการตั้งค่าของตัวเชื่อมต่อทางการเงินที่จะตั้งค่าคอนฟิกจาก Commerce headquarters รูปแบบไฟล์จะสอดคล้องกับข้อกําหนดของการตั้งค่าคอนฟิกการรวมทางการเงิน

### <a name="pos-fiscal-connector-extension-design"></a>การออกแบบส่วนขยายของตัวเชื่อมต่อทางการเงิน POS

วัตถุประสงค์ของส่วนขยายตัวเชื่อมต่อทางการเงิน POS คือเพื่อสื่อสารกับบริการลงทะเบียนทางการเงินจาก POS โดยจะใช้โพรโทคอล HTTPS สำหรับการสื่อสาร

#### <a name="fiscal-connector-factory"></a>แฟคทอรีตัวเชื่อมต่อทางการเงิน

แฟกทอรีตัวเชื่อมต่อทางการเงินจะแมปชื่อตัวเชื่อมต่อกับการใช้งานตัวเชื่อมต่อทางการเงิน และอยู่ในไฟล์ **Pos.Extension\\Connectors\\FiscalConnectorFactory.ts** ชื่อตัวเชื่อมต่อควรตรงกับชื่อตัวเชื่อมต่อทางการเงินที่ระบุใน Commerce headquarters

#### <a name="efr-fiscal-connector"></a>ตัวเชื่อมต่อทางการเงิน EFR

ตัวเชื่อมต่อทางการเงิน EFR อยู่ในไฟล์ **Pos.Extension\\Connectors\\Efr\\EfrFiscalConnector.ts** โดยจะใช้อินเทอร์เฟส **IFiscalConnector** ที่รองรับคำขอต่อไปนี้

- **FiscalRegisterSubmitDocumentClientRequest** – คำขอนี้จะส่งเอกสารไปยังบริการลงทะเบียนทางการเงินและส่งคืนการตอบสนองจากบริการลงทะเบียนทางการเงิน
- **FiscalRegisterIsReadyClientRequest** – คำขอนี้ใช้เพื่อตรวจสอบความสมบูรณ์ของบริการลงทะเบียนทางการเงิน
- **FiscalRegisterInitializeClientRequest** – คำขอนี้ใช้สำหรับการเริ่มต้นบริการลงทะเบียนทางการเงิน

#### <a name="configuration"></a>โครงแบบ

ไฟล์การตั้งค่าคอนฟิกอยู่ในโฟลเดอร์ **src\\FiscalIntegration\\Efr\\Configurations\\Connectors** ของที่เก็บ [โซลูชัน Dynamics 365 Commerce](https://github.com/microsoft/Dynamics365Commerce.Solutions/) วัตถุประสงค์ของไฟล์คือเพื่อเปิดใช้งานการตั้งค่าของตัวเชื่อมต่อทางการเงินที่จะตั้งค่าคอนฟิกจาก Commerce headquarters รูปแบบไฟล์จะสอดคล้องกับข้อกําหนดของการตั้งค่าคอนฟิกการรวมทางการเงิน มีการเพิ่มการตั้งค่ามีดังต่อไปนี้:

- **ที่อยู่ปลายทาง** – URL ของบริการลงทะเบียนทางการเงิน
- **การหมดเวลา** – จํานวนเวลาเป็นมิลลิวินาที ซึ่งตัวเชื่อมต่อจะรอการตอบสนองจากบริการลงทะเบียนทางการเงิน

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
