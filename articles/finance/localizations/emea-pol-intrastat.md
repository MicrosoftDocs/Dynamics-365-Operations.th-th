---
title: อินทราสแทตของโปแลนด์
description: บทความนี้มีข้อมูลเกี่ยวกับการรายงานอินทราสแทตในโปแลนด์
author: AdamTrukawka
ms.date: 11/09/2021
ms.topic: article
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: atrukawk
ms.search.validFrom: ''
ms.openlocfilehash: 473581fa4f3f1e8cac06d5748f28116e6615215e
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 08/12/2022
ms.locfileid: "9281656"
---
# <a name="polish-intrastat"></a>อินทราสแทตโปแลนด์

[!include[banner](../includes/banner.md)]

หน้า **อินทราสแทต** ใช้เพื่อสร้างและรายงานข้อมูลเกี่ยวกับการค้าระหว่างประเทศสหภาพยุโรป (EU) การรายงานภาษีอินทราสแทตภาษาโปแลนด์มีข้อมูลเกี่ยวกับการค้าขายสินค้าเพื่อการรายงาน

ฟิลด์ต่อไปนี้จะรวมอยู่ในการรายงานอินทราสแทตภาษาโปแลนด์: ฟิลด์ทั้งหมดจะรวมอยู่ในการมาถึงและการจัดส่ง ยกเว้น **RodzajTransportu** (โหมดการขนส่ง) และ **KrajPochodzenia** (ประเทศหรือภูมิภาคผู้ผลิต) ซึ่งไม่ได้รวมอยู่ในการจัดส่ง และ **IdKontrahenta** (หมายเลข VAT ต่างประเทศของลูกค้า) ซึ่งไม่ได้รวมไว้ในการมาถึง

| ชื่อฟิลด์ | คำอธิบาย |
|-------------------------|-------------------------|
| ข้อมูล Deklaracja | วันที่ที่สร้างเอกสาร |
| Miesiac | เดือนการอ้างอิงของการรายงานภาษี |
| Rok | ปีการอ้างอิงของการรายงานภาษี |
| Numer | หมายเลขการรายงานภาษีในรอบระยะเวลาการอ้างอิง |
| Wersja | หมายเลขรุ่นของการรายงานภาษี |
| NrWlasny | รหัสการรายงานภาษี ค่าจะถูกสร้างขึ้นโดยอัตโนมัติ |
| Typ | ทิศทางของรายงาน</br><li>สำหรับการมาถึง "P" จะถูกพิมพ์</li><li>สำหรับการจัดส่ง "W" จะถูกพิมพ์</li> |
| Rodzaj | ชนิดของการรายงานภาษี ค่านี้จะระบุว่ารายงานเป็นการรายงานภาษีต้นฉบับหรือการรายงานภาษีที่มีการแก้ไข |
| UC | รหัสหน่วยที่ใช้ระบุการรายงานภาษีอินทราสแทต ค่าระบุในฟิลด์ **หมายเลขยกเว้นภาษี** ในส่วน **ภาษีขาย** บนแท็บ **ตัวแทน** ของหน้า **พารามิเตอร์การค้าต่างประเทศ** |
| Nazwa | ชื่อของบริษัท |
| Miejscowosc, UlicaNumer, KodPocztowy | ที่อยู่เต็มของนิติบุคคล |
| Nip | หมายเลขรหัสภาษีโปแลนด์ (รหัสภาษีมูลค่าเพิ่ม [VAT]) |
| Regon | หมายเลขรหัสทางสถิติของโปแลนด์ (หมายเลของค์กร) |
| LacznaWartoscFaktur | ผลรวมของค่าใบแจ้งหนี้ |
| LacznaWartoscStatystyczna | ผลรวมของค่าทางสถิติ |
| LacznaLiczbaPozycji | จำนวนรวมของสินค้า |
| PozId | หมายเลขที่ต่อเนื่องกันของสินค้าที่ระบุ |
| OpisTowaru | ชื่อทางการค้าของโภคภัณฑ์ |
| KrajPochodzeniaWysylki | รหัสองค์การระหว่างประเทศว่าด้วยการมาตรฐาน (ISO) สำหรับประเทศหรือภูมิภาคของคู่สัญญา |
| WarunkiDostawy | รหัสอินทราสแทตสำหรับเงื่อนไขการจัดส่ง |
| RodzajTransakcji | รหัสที่ระบุลักษณะของธุรกรรม บริษัทโปแลนด์ใช้รหัสธุรกรรมที่มีตัวเลขสองหลัก |
| KodTowarowy | รหัสโภคภัณฑ์แปดหลักตามระบบการตั้งชื่อแบบรวม |
| RodzajTransportu | รหัสอินทราสแทตสำหรับโหมดการขนส่ง |
| KrajPochodzenia | รหัส ISO สำหรับประเทศหรือภูมิภาคที่สร้างหรือผลิตชุดสินค้า |
| MasaNetto | มวลสุทธิเป็นกิโลกรัมเต็ม |
| IloscUzupelniajacaJm | ปริมาณในหน่วยวัดเสริมเป็นตัวเลขเต็มจำนวน |
| WartoscFaktury | มูลค่าใบแจ้งหนี้ของธุรกรรมทั้งหมดที่ครอบคลุมโดยสินค้าหนึ่งๆ |
| WartoscStatystyczna | ค่าทางสถิติ |
| Wypelniajacy: NazwiskoImie, Telefon, Faks, Email | ชื่อและนามสกุล หมายเลขโทรศัพท์ หมายเลขโทรสาร และที่อยู่อีเมลของบุคคลที่ส่งการรายงานภาษี |
| IdKontrahenta | หมายเลข VAT ต่างประเทศของลูกค้าในรัฐสมาชิกประเทศของ EU |


## <a name="set-up-intrastat"></a>ตั้งค่าอินทราสแทต

จากที่เก็บข้อมูลส่วนกลาง นำเข้ารุ่นล่าสุดของการตั้งค่าคอนฟิกการรายงานทางอิเล็กทรอนิกส์ต่อไปนี้ (ER):

   - แบบจำลองอินทราสแทต
   - รายงานอินทราสแทต
   - อินทราสแทต (PL)

สำหรับข้อมูลเพิ่มเติม ดูที่ [ดาวน์โหลดการตั้งค่าคอนฟิก ER จากที่เก็บส่วนกลางของบริการการตั้งค่าคอนฟิก](../../fin-ops-core/dev-itpro/analytics/er-download-configurations-global-repo.md)

## <a name="set-up-a-vat-id-and-an-enterprise-number-for-your-company"></a>ตั้งค่ารหัส VAT และหมายเลของค์กรของบริษัทของคุณ

### <a name="create-registration-types-for-company-codes"></a>สร้างชนิดการลงทะเบียนของรหัสบริษัท

คุณต้องสร้างการลงทะเบียนสองชนิดในรหัสบริษัท โดยรหัสหนึ่งเป็นชนิดหนึ่งเป็นรหัส VAT (รหัส NIP) และอีกชนิดหนึ่งเป็นหมายเลของค์กร (รหัส Regon)

1. ไปที่ **การจัดการองค์กร** > **สมุดที่อยู่สากล** > **ชนิดการลงทะเบียน** > **ชนิดการลงทะเบียน**
2. ในบานหน้าต่างการดำเนินการ ให้เลือก **สร้าง** เพื่อสร้างชนิดการลงทะเบียนสำหรับรหัส VAT
3. ในกล่องโต้ตอบ **ป้อนรายละเอียดชนิดการลงทะเบียน** ในฟิลด์ **ชื่อ** ให้ป้อนชื่อสำหรับชนิดการลงทะเบียนใหม่ ตัวอย่างเช่น ป้อน **NIP**
4. ในฟิลด์ **ประเทศ/ภูมิภาค** ให้เลือก **POL**
5. เลือก **สร้าง**
6. ในบานหน้าต่างการดำเนินการ ให้เลือก **สร้าง** เพื่อสร้างชนิดการลงทะเบียนสำหรับหมายเลของค์กร
7. ในกล่องโต้ตอบ **ป้อนรายละเอียดชนิดการลงทะเบียน** ในฟิลด์ **ชื่อ** ให้ป้อนชื่อสำหรับชนิดการลงทะเบียนใหม่ ตัวอย่างเช่น ป้อน **Regon**
8. ในฟิลด์ **ประเทศ/ภูมิภาค** ให้เลือก **POL**
9. เลือก **สร้าง**

### <a name="match-the-registration-types-with-registration-categories"></a>จับคู่ชนิดการลงทะเบียนกับประเภทการลงทะเบียน

1. ไปที่ **การจัดการองค์กร** > **สมุดที่อยู่สากล** > **ชนิดการลงทะเบียน** > **ประเภทการลงทะเบียน**
2. ในบานหน้าต่างการดำเนินการ ให้เลือก **สร้าง** เพื่อสร้างลิงค์ระหว่างการลงทะเบียนแต่ละชนิดที่คุณสร้างขึ้นและประเภทการลงทะเบียน

    - เลือกชนิดการลงทะเบียนสำหรับรหัส VAT (รหัส NIP) แล้วเลือกประเภทการลงทะเบียน **รหัส VAT**
    - เลือกชนิดการลงทะเบียนสำหรับหมายเลของค์กร (รหัส Regon) แล้วเลือกประเภทการลงทะเบียน **รหัสองค์กร (COID)**

### <a name="set-up-a-vat-id-and-an-enterprise-number-for-your-company"></a>ตั้งค่ารหัส VAT และหมายเลของค์กรของบริษัทของคุณ

1. ไปที่ **การจัดการองค์กร** > **องค์กร** > **นิติบุคคล**
2. ในกริด เลือกบริษัทของคุณ
3. บนบานหน้าต่างการดำเนินการ เลือก **รหัสการลงทะเบียน**
4. บนแท็บด่วน **รหัสการลงทะเบียน** ให้เลือก **เพิ่ม**
5. ในฟิลด์ **ชนิดการลงทะเบียน** ให้เลือกหนึ่งในชนิดการลงทะเบียนที่คุณสร้างไว้ก่อนหน้านี้
6. ป้อนรหัส VAT (รหัส NIP) หรือหมายเลของค์กร (รหัส Regon) ของบริษัทคุณ ขึ้นอยู่กับชนิดการลงทะเบียนที่คุณเลือกในขั้นตอนก่อนหน้านี้
7. ทําขั้นตอนที่ 4 ถึง 6 ซ้ํากับชนิดการลงทะเบียนอื่นๆ ที่คุณสร้างไว้ก่อนหน้านี้

## <a name="set-up-a-company-address"></a>ตั้งค่าที่อยู่บริษัท

1. ไปที่ **การจัดการองค์กร** > **องค์กร** > **นิติบุคคล**
2. ในกริด เลือกบริษัทของคุณ
3. บนแท็บ **ที่อยู่** ให้เลือก **แก้ไข**
4. ในกล่องโต้ตอบ **แก้ไขที่อยู่** ในฟิลด์ **รหัสไปรษณีย์** ให้เลือกรหัสไปรษณีย์ของบริษัทของคุณ
5. ในฟิลด์ **ถนน** ให้ป้อนที่อยู่ของคุณ
6. ในฟิลด์ **เมือง** เลือกเมืองของคุณ

## <a name="set-up-foreign-trade-parameters"></a>ตั้งค่าพารามิเตอร์การค้าต่างประเทศ

1. ไปที่ **ภาษี** > **การตั้งค่า** > **พารามิเตอร์การค้าต่างประเทศ**
2. บนแท็บ **อินทราสแทต** บน FastTab **การรายงานทางอิเล็กทรอนิกส์** ในฟิลด์ **การแม็ปรูปแบบไฟล์** เลือก **อินทราสแทต (PL)**
3. ในฟิลด์ **การแม็ปรูปแบบรายงาน** เลือก **รายงานอินทราสแทต**
4. บนแท็บด่วน **รหัสโภคภัณฑ์ตามลำดับชั้น** ในฟิลด์ **การจัดประเภทตามลำดับชั้น** ให้เลือก **อินทราสแทต**
5. ในฟิลด์ **รหัสธุรกรรม** เลือกรหัสธุรกรรมสำหรับการโอนย้ายคุณสมบัติ คุณใช้รหัสนี้สำหรับธุรกรรมที่สร้างการโอนย้ายทรัพย์สินจริงหรือที่วางแผนไว้เทียบกับค่าตอบแทน (ทางการเงิน หรืออื่นๆ) นอกจากนี้ คุณยังใช้สำหรับการแก้ไขด้วย บริษัทในโปแลนด์ใช้รหัสธุรกรรมที่มีตัวเลขสองหลัก
6. ในฟิลด์ **ใบลดหนี้** เลือกรหัสธุรกรรมสำหรับการส่งคืนสินค้า
7. บนแท็บ **คุณสมบัติประเทศ/ภูมิภาค** ในฟิลด์ **ประเทศ/ภูมิภาค** ให้แสดงรายการประเทศหรือภูมิภาคทั้งหมดที่บริษัทของคุณประกอบธุรกิจด้วย สำหรับแต่ละประเทศที่เป็นส่วนหนึ่งของ EU ให้เลือก **EU** ในฟิลด์ **ชนิดประเทศ/ภูมิภาค** เพื่อให้ประเทศปรากฏบนรายงานอินทราสแทตของคุณ สำหรับโปแลนด์ ให้เลือก **ภายในประเทศ** ในฟิลด์ **ชนิดของประเทศ/ภูมิภาค**
8. บนแท็บ **ตัวแทน** บนแท็บด่วน **ตัวแทน** ในส่วน **ภาษีขาย** ในฟิลด์ **หมายเลขยกเว้นภาษี** ให้ป้อน **420000** เพื่อบ่งชี้รหัสหน่วยที่การรายงานอินทราสแทตระบุอยู่
9. บนแท็บ **ผู้ติดต่อ** ป้อนชื่อ หมายเลขโทรศัพท์ หมายเลขโทรสาร และที่อยู่อีเมลของบุคคลที่ส่งการรายงานภาษี
10. บนแท็บ **ลำดับหมายเลข** ในฟิลด์ **รหัสลำดับหมายเลข** สำหรับการอ้างอิง **หมายเลขไฟล์ XML** ให้ระบุลำดับหมายเลขที่ไม่ต่อเนื่องที่มีอักขระสูงสุดเก้าอักขระ ฟิลด์นี้ใช้เพื่อสร้างค่าโดยอัตโนมัติให้กับฟิลด์ **รหัสการรายงานภาษี** บนรายงานอินทราสแทต

## <a name="set-up-product-parameters-for-the-intrastat-declaration"></a>ตั้งค่าพารามิเตอร์ผลิตภัณฑ์สำหรับการรายงานภาษีอินทราสแทต

1. ไปยัง **การจัดการข้อมูลผลิตภัณฑ์** > **ผลิตภัณฑ์** > **ผลิตภัณฑ์ที่นำออกใช้**
2. ในกริด เลือกผลิตภัณฑ์
3. บนแท็บด่วน **การค้าต่างประเทศ** ในส่วน **อินทราสแทต** ในฟิลด์ **โภคภัณฑ์** ให้เลือกรหัสโภคภัณฑ์ที่เหมาะสม ชื่อของโภคภัณฑ์จะถูกพิมพ์ในฟิลด์ **คำอธิบายของโภคภัณฑ์** ในรายงานอินทราสแทต
4. ในส่วน **ผู้ผลิต** ในฟิลด์ **ประเทศ/ภูมิภาค** ให้เลือกประเทศหรือภูมิภาคผู้ผลิตของผลิตภัณฑ์
5. บนแท็บด่วน **จัดการสินค้าคงคลัง** ในฟิลด์ **น้ำหนักสุทธิ** ให้ป้อนน้ำหนักของผลิตภัณฑ์เป็นกิโลกรัม

## <a name="set-up-compression-of-intrastat"></a>ตั้งค่าการบีบอัดอินทราสแทต

-   ไปที่ **ภาษี** > **การตั้งค่า** > **การค้าต่างประเทศ** > **การบีบอัดของอินทราสแทต** และเลือกฟิลด์ที่ควรจะเปรียบเทียบ เมื่อมีการสรุปข้อมูลอินทราสแทต สำหรับอินทราสแทตภาษาโปแลนด์ เลือกฟิลด์ต่อไปนี้:

    - โภคภัณฑ์
    - รหัสธุรกรรม
    - ประเทศ/ภูมิภาคผู้ผลิต
    - การขนส่ง
    - เงื่อนไขการจัดส่ง
    - ประเทศ/ภูมิภาคของผู้ส่ง
    - ประเทศ/ภูมิภาค
    - การแก้ไข
    - หมายเลขยกเว้นภาษี
    - ทิศทาง
    - ใบแจ้งหนี้

## <a name="set-up-the-transport-method-and-delivery-terms"></a>การตั้งค่าวิธีการขนส่งและเงื่อนไขการจัดส่ง

1.  ตั้งค่ารหัสการขนส่ง

    1. ไปที่ **ภาษี** > **การตั้งค่า** > **การค้าต่างประเทศ** > **วิธีการขนส่ง**
    2. บนบานหน้าต่างการดำเนินการ เลือก **สร้าง**
    3. ในฟิลด์ **การขนส่ง** ให้ป้อนรหัสเฉพาะ บริษัทโปแลนด์ใช้รหัสการขนส่งที่มีตัวเลขหนึ่งหลัก

2.  ตั้งค่ารหัสอินทราสแทตของโหมดการจัดส่ง

    1. ไปที่ **การจัดซื้อและการจัดหา** > **การตั้งค่า** > **การกระจาย** > **เงื่อนไขการจัดส่ง**
    2. ในกริด เลือกชุดของเงื่อนไขการจัดส่ง
    3. บนแท็บด่วน **ทั่วไป** ในฟิลด์ **รหัสอินทราสแทต** ป้อนรหัสเฉพาะ

## <a name="intrastat-transfer"></a>การโอนย้ายอินทราสแทต

บนหน้า **อินทราสแทต** ในบานหน้าต่างการดำเนินการ คุณสามารถเลือก **โอนย้าย** เพื่อโอนย้ายข้อมูลเกี่ยวกับการค้าภายในการค้ากับการค้าภายในบริษัทจากใบสั่งขาย ใบแจ้งหนี้ข้อความอิสระ ใบสั่งซื้อ ใบแจ้งหนี้ผู้จัดซื้อ ใบรับสินค้าผู้จัดซื้อ ใบแจ้งหนี้โครงการ และใบสั่งโอนย้ายโดยอัตโนมัติ เฉพาะเอกสารที่มีประเทศใน EU เป็นประเทศหรือภูมิภาคปลายทางหรือการส่งสินค้าเท่านั้นจะโอนย้าย

คุณยังสามารถป้อนธุรกรรมด้วยตนเองโดยการเลือก **สร้าง** ในบานหน้าต่างการดำเนินการ

### <a name="generate-an-intrastat-report"></a>สร้างรายงานอินทราสแทต

1. ไปที่ **ภาษี** > **การรายงาน** > **การค้าต่างประเทศ** > **อินทราสแทต**
2. ในบานหน้าต่างการดำเนินการ เลือก **ผลลัพธ์** &gt; **รายงาน**
3. ในกล่องโต้ตอบ **รายงานอินทราสแทต** ตั้งค่าฟิลด์ต่อไปนี้

    | ฟิลด์ | คำอธิบาย |
    |-------------------------|-------------------------|
    | วันที่เริ่มต้น | เลือกวันที่เริ่มต้นสำหรับรายงาน |
    | สร้างไฟล์ | ตั้งค่าตัวเลือกนี้เป็น **ใช่** เพื่อสร้างไฟล์ .xml สำหรับรายงานอินทราสแทตของคุณ |
    | ชื่อไฟล์ | ป้อนชื่อของไฟล์ .xml |
    | สร้างรายงาน | ตั้งค่าตัวเลือกนี้เป็น **ใช่** เพื่อสร้างไฟล์ .xlsx สำหรับรายงานอินทราสแทตของคุณ |
    | ชื่อไฟล์รายงาน | ป้อนชื่อของไฟล์ .xlsx |
    | ทิศทาง | เลือก **การมาถึง** ของรายงานเกี่ยวกับบัญชีขาเข้าภายในประชาคม</br>เลือก **การจัดส่ง** ของรายงานเกี่ยวกับการจัดส่งภายในประชาคม |
    | รหัสการรายงานภาษี | รหัสเอกสารจะถูกสร้างขึ้นโดยอัตโนมัติและสามารถอัปเดตได้ |
    | ชนิดของการรายงานภาษี | เลือก **การรายงานภาษี** ของการรายงานภาษีต้นฉบับ</br>เลือก **การแก้ไขการรายงานภาษี – การเปลี่ยน** สำหรับการรายงานภาษีที่มีการแก้ไขเพื่อแทนที่ต้นฉบับหรือการรายงานภาษีการแก้ไขที่มีอยู่ ซึ่งส่งไว้ก่อนหน้านี้ทั้งหมด |
    | เมืองของการสร้างเอกสาร | ป้อนค่าที่ควรพิมพ์ในฟิลด์ **Miejscowosc** ในการรายงานภาษีอินทราสแทต |
    | วันที่ของการสร้างเอกสาร | ป้อนค่าที่ควรพิมพ์ในฟิลด์ **ข้อมูล Deklaracja** ในการรายงานภาษีอินทราสแทต |
    | เอกสารเลขที่ | ป้อนค่าที่ควรพิมพ์ในฟิลด์ **Numer** ในการรายงานภาษีอินทราสแทต |
    | รุ่นของเอกสาร | ป้อนค่าที่ควรพิมพ์ในฟิลด์ **Wersja** ในการรายงานภาษีอินทราสแทต |

4. เลือก **ตกลง** และรีวิวรายงานที่สร้างขึ้น

## <a name="example"></a>ตัวอย่าง

ตัวอย่างนี้แสดงวิธีการลงรายการบัญชีการมาถึงและการจัดส่งสำหรับอินทราสแทตโดยการใช้นิติบุคคล **DEMF**

### <a name="preliminary-setup"></a>การตั้งค่าเบื้องต้น

นําเข้าการตั้งค่าคอนฟิก (ER) ต่อไปนี้เวอร์ชันล่าสุด:

   - แบบจำลองอินทราสแทต
   - รายงานอินทราสแทต
   - อินทราสแทต (PL)

### <a name="set-up-a-company-address"></a>ตั้งค่าที่อยู่บริษัท

1. ไปที่ **การจัดการองค์กร** > **สมุดที่อยู่สากล** > **ที่อยู่** > **การตั้งค่าที่อยู่**
2. บนแท็บ **เมือง** ให้เลือก **สร้าง**
3. ในฟิลด์ **ประเทศ/ภูมิภาค** ให้เลือก **POL**
4. ในฟิลด์ **เมือง** ให้ป้อน **วอร์ซอ**
5. บนแท็บ **รหัสไปรษณีย์** ให้เลือก **สร้าง**
6. ในฟิลด์ **ประเทศ/ภูมิภาค** ให้เลือก **POL**
7. ในฟิลด์ **เมือง** เลือก **วอร์ซอ**
8. ในฟิลด์ **รหัสไปรษณีย์** ให้ป้อน **00-844**
9. ไปที่ **การจัดการองค์กร** > **องค์กร** > **นิติบุคคล** และเลือกนิติบุคคล **DEMF**
10. บน FastTab **ที่อยู่** ให้เลือก **แก้ไข**
11. ในฟิลด์ **ประเทศ/ภูมิภาค** ให้เลือก **POL**
12. ในฟิลด์ **รหัสไปรษณีย์** ให้เลือก **31-111**
13. ในฟิลด์ **ถนน** ให้ป้อน **Statystyczna 22/1**
14. ในฟิลด์ **เมือง** เลือก **วอร์ซอ**
15. เลือก **ตกลง**

## <a name="set-up-a-vat-id-and-an-enterprise-number-code-for-your-company"></a>ตั้งค่ารหัส VAT และรหัสหมายเลของค์กรของบริษัทของคุณ

### <a name="create-registration-types-for-company-codes"></a>สร้างชนิดการลงทะเบียนของรหัสบริษัท

1. ไปที่ **การจัดการองค์กร** > **สมุดที่อยู่สากล** > **ชนิดการลงทะเบียน** > **ชนิดการลงทะเบียน**
2. ในบานหน้าต่างการดำเนินการ ให้เลือก **สร้าง** เพื่อสร้างชนิดการลงทะเบียนสำหรับรหัส VAT (รหัส NIP)
3. ในกล่องโต้ตอบ **ป้อนรายละเอียดชนิดการลงทะเบียน** ในฟิลด์ **ชื่อ** ให้ป้อน **NIP**
4. ในฟิลด์ **ประเทศ/ภูมิภาค** ให้เลือก **POL**
5. เลือก **สร้าง**
6. ในบานหน้าต่างการดำเนินการ ให้เลือก **สร้าง** เพื่อสร้างชนิดการลงทะเบียนสำหรับหมายเลของค์กร (รหัส Regon)
7. ในกล่องโต้ตอบ **ป้อนรายละเอียดชนิดการลงทะเบียน** ในฟิลด์ **ชื่อ** ให้ป้อน **Regon**
8. ในฟิลด์ **ประเทศ/ภูมิภาค** ให้เลือก **POL**
9. เลือก **สร้าง**

### <a name="match-the-registration-types-with-registration-categories"></a>จับคู่ชนิดการลงทะเบียนกับประเภทการลงทะเบียน

1. ไปที่ **การจัดการองค์กร** > **สมุดที่อยู่สากล** > **ชนิดการลงทะเบียน** > **ประเภทการลงทะเบียน**
2. ในบานหน้าต่างการดำเนินการ ให้เลือก **สร้าง** เพื่อสร้างลิงค์ระหว่างการลงทะเบียนแต่ละชนิดที่คุณสร้างขึ้นและประเภทการลงทะเบียน

    - สำหรับชนิดการลงทะเบียน **NIP** ให้เลือกประเภทการลงทะเบียน **รหัส VAT**
    - สำหรับชนิดการลงทะเบียน **Regon** ให้เลือกประเภทการลงทะเบียน **รหัสองค์กร (COID)**

### <a name="set-up-a-vat-id-and-an-enterprise-number-for-your-company"></a>ตั้งค่ารหัส VAT และหมายเลของค์กรของบริษัทของคุณ

1. ไปที่ **การจัดการองค์กร** > **องค์กร** > **นิติบุคคล**
2. ในกริด ให้เลือก **DEMF**
3. บนบานหน้าต่างการดำเนินการ เลือก **รหัสการลงทะเบียน**
4. บนแท็บด่วน **รหัสการลงทะเบียน** ให้เลือก **เพิ่ม**
5. ในฟิลด์ **ชนิดของการลงทะเบียน** ให้เลือก **NIP**
6. ในฟิลด์ **หมายเลขการลงทะเบียน** ให้ป้อน **1234567890**
7. เลือก **เพิ่ม**
8. ในฟิลด์ **ชนิดของการลงทะเบียน** ให้เลือก **Regon**
9. ในฟิลด์ **หมายเลขการลงทะเบียน** ให้ป้อน **12345678901234**

### <a name="set-up-a-number-sequence-code"></a>ตั้งค่ารหัสลำดับหมายเลข

1. ไปที่ **การจัดการองค์กร** > **ลำดับหมายเลข** > **ลำดับหมายเลข**
2. บนบานหน้าต่างการดำเนินการ บนแท็บ **ลำดับหมายเลข** ในกลุ่ม **ใหม่** ให้เลือก **ลำดับหมายเลข**
3. บนแท็บด่วน **รหัส** ในฟิลด์ **รหัสลำดับหมายเลข** ให้ป้อน **ไฟล์\_XML**
4. บนแท็บด่วน **พารามิเตอร์ขอบเขต** ในฟิลด์ **ขอบเขต** ให้เลือก **บริษัท**
5. ในฟิลด์ **บริษัท** เลือก **DEMF**
6. บนแท็บด่วน **เซ็กเมนต์** ในฟิลด์ **ความยาว** สำหรับเซกเมนต์ **ตัวอักษรและตัวเลข** ให้ป้อน **4**
7. บน FastTab **ทั่วไป** ในส่วน **การตั้งค่า** ตั้งค่าตัวเลือก **แบบต่อเนื่อง** เป็น **ไม่**
8. ในส่วน **การปันส่วนหมายเลข** ในฟิลด์ **ค่ามากสุด** ให้ป้อน **9999**

### <a name="set-up-foreign-trade-parameters"></a>ตั้งค่าพารามิเตอร์การค้าต่างประเทศ

1. ไปที่ **ภาษี** > **การตั้งค่า** > **การค้าต่างประเทศ** > **พารามิเตอร์การค้าต่างประเทศ**
2. บนแท็บ **อินทราสแทต** บนแท็บด่วน **ทั่วไป** ในฟิลด์ **รหัส** **ธุรกรรม** ให้เลือก **11**
3. บน FastTab **การรายงานทางอิเล็กทรอนิกส์** ในฟิลด์ **การแม็ปรูปแบบไฟล์** เลือก **อินทราสแทต (PL)**
4. ในฟิลด์ **การแม็ปรูปแบบรายงาน** เลือก **รายงานอินทราสแทต**
5. บนแท็บด่วน **รหัสชุดสินค้าตามลำดับชั้น** ตรวจสอบว่าฟิลด์ **การจัดประเภทตามลำดับชั้น** ตั้งค่าเป็น **อินทราสแทต**
6. บนแท็บ **คุณสมบัติประเทศ/ภูมิภาค** เลือก **สร้าง**
7. ในฟิลด์ **ประเทศ/ภูมิภาคของฝ่าย** ให้เลือก **POL** จากนั้น ในฟิลด์ **ชนิดของประเทศ/ภูมิภาค** ให้เลือก **ภายในประเทศ**
8. ในฟิลด์ **ประเทศ/ภูมิภาคของฝ่าย** ให้เลือก **DEU** จากนั้น ในฟิลด์ **ชนิดของประเทศ/ภูมิภาค** ให้เลือก **EU**
9. บนแท็บ **ตัวแทน** บนแท็บด่วน **ตัวแทน** ในส่วน **ภาษีขาย** ในฟิลด์ **หมายเลขยกเว้นภาษี** ให้ป้อน **420000**
10. บนแท็บ **ผู้ติดต่อ** ในฟิลด์ **ชื่อ** ให้ป้อน **Manish Chopra**
11. ในฟิลด์ **โทรศัพท์** ให้ป้อน **425-555-5068**
12. ในฟิลด์ **หมายเลขโทรสาร** ให้ป้อน **425-555-5049**
13. ในฟิลด์ **อีเมล** ให้ป้อน **manishc@contoso.com**
14. บนแท็บ **ลำดับหมายเลข** ในฟิลด์ **รหัสลำดับหมายเลข** สำหรับการอ้างอิง **หมายเลขไฟล์ XML** ให้เลือก **ไฟล์\_XML**

### <a name="set-up-product-information"></a>ตั้งค่าข้อมูลผลิตภัณฑ์

1. ไปที่ **การจัดการข้อมูลผลิตภัณฑ์** > **ผลิตภัณฑ์** > **ผลิตภัณฑ์** **ที่นำออกใช้**
2. ในกริด ให้เลือก **D0001**
3. บนแท็บด่วน **การค้าต่างประเทศ** ในส่วน **อินทราสแทต** ในฟิลด์ **โภคภัณฑ์** ให้เลือก **100 200 30**
4. บนแท็บด่วน **จัดการสินค้าคงคลัง** ในส่วน **การวัดน้ำหนัก** ในฟิลด์ **น้ำหนักสุทธิ** ให้ป้อน **2**
5. บนบานหน้าต่างการดำเนินการ เลือก **บันทึก**
6. ในกริด ให้เลือก **D0003**
7. บนแท็บด่วน **การค้าต่างประเทศ** ในส่วน **อินทราสแทต** ในฟิลด์ **โภคภัณฑ์** ให้เลือก **100 200 30**
8. ในส่วน **จุดเริ่มต้น** ในฟิลด์ **ประเทศ/ภูมิภาค** เลือก **DEU**
9. บนแท็บด่วน **จัดการสินค้าคงคลัง** ในส่วน **การวัดน้ำหนัก** ในฟิลด์ **น้ำหนักสุทธิ** ให้ป้อน **5**
10. บนบานหน้าต่างการดำเนินการ เลือก **บันทึก**

### <a name="change-the-site-address"></a>การเปลี่ยนที่อยู่ไซต์

1. ไปที่ **การจัดการคลังสินค้า** > **การตั้งค่า** > **คลังสินค้า** > **ไซต์**
2. ในกริด ให้เลือก **1**
3. บน FastTab **ที่อยู่** ให้เลือก **แก้ไข**
4. ในกล่องโต้ตอบ **แก้ไขที่อยู่** ในฟิลด์ **ประเทศ/ภูมิภาค** ให้เลือก **POL**
5. เลือก **ตกลง**

### <a name="set-up-a-transport-method"></a>ตั้งค่าวิธีการขนส่ง

1. สร้างวิธีการขนส่ง

    1. ไปที่ **ภาษี** > **การตั้งค่า** > **การค้าต่างประเทศ** > **วิธีการขนส่ง**
    2. บนบานหน้าต่างการดำเนินการ เลือก **สร้าง**
    3. ในฟิลด์ **การขนส่ง** ให้ป้อน **3**
    4. ในฟิลด์ **คำอธิบาย** ให้ป้อน **การขนส่งทางถนน**

2. กำหนดวิธีการขนส่งใหม่ให้กับโหมดการจัดส่ง ด้วยวิธีนี้ ให้คุณตั้งค่าเริ่มต้นที่จะใช้ในวิธีการขนส่งเมื่อมีการเลือกวิธีการจัดส่งที่ตรงกัน

    1. ไปที่ **การจัดซื้อและการจัดหา** > **การตั้งค่า** > **การกระจาย** > **โหมดของการจัดส่ง**
    2. ในกริด ให้เลือก **10**
    3. บนแท็บด่วน **การค้าต่างประเทศ** ในฟิลด์ **การขนส่ง** เลือก **3**

3. เลือกวิธีการจัดส่งเริ่มต้นของลูกค้า

    1. ไปที่ **บัญชีลูกหนี้** > **ลูกค้า** > **ลูกค้าทั้งหมด**
    2. ในกริด ให้เลือก **DE-016**
    3. บน FastTab **ใบแจ้งหนี้และการจัดส่ง** ในฟิลด์ **โหมดการจัดส่ง** เลือก **10**

4. เลือกวิธีการจัดส่งเริ่มต้นของผู้จัดจำหน่าย

    1. ไปที่ **บัญชีเจ้าหนี้** > **ผู้จัดจำหน่าย** > **ผู้จัดจำหน่ายทั้งหมด**
    2. ในกริด ให้เลือก **DE-001**
    3. บน FastTab **ใบแจ้งหนี้และการจัดส่ง** ในฟิลด์ **โหมดการจัดส่ง** เลือก **10**

### <a name="set-up-codes-for-terms-of-delivery"></a>การตั้งค่ารหัสเงื่อนไขการจัดส่ง

1. การตั้งค่ารหัสอินทราสแทตสำหรับเงื่อนไขการจัดส่ง

    1. ไปที่ **การจัดซื้อและการจัดหา** > **การตั้งค่า** > **การกระจาย** > **เงื่อนไขการจัดส่ง**
    2. ในกริด ให้เลือก **CIF**
    3. บน FastTab **ทั่วไป** ในฟิลด์ **รหัสอินทราสแทต** ให้ป้อน **CIF**

2. เลือกเงื่อนไขการจัดส่งเริ่มต้นของลูกค้า

    1. ไปที่ **บัญชีลูกหนี้** > **ลูกค้า** > **ลูกค้าทั้งหมด**
    2. ในกริด ให้เลือก **DE-016**
    3. บน FastTab **ใบแจ้งหนี้และการจัดส่ง** ในฟิลด์ **เงื่อนไขการจัดส่ง** เลือก **CIF**

3. เลือกเงื่อนไขการจัดส่งเริ่มต้นของผู้จัดจำหน่าย

    1. ไปที่ **บัญชีเจ้าหนี้** > **ผู้จัดจำหน่าย** > **ผู้จัดจำหน่ายทั้งหมด**
    2. ในกริด ให้เลือก **DE-001**
    3. บน FastTab **ใบแจ้งหนี้และการจัดส่ง** ในฟิลด์ **เงื่อนไขการจัดส่ง** เลือก **CIF**

### <a name="verify-an-eu-customers-tax-exempt-number-code"></a>ตรวจสอบรหัสหมายเลขยกเว้นภาษี EU ของลูกค้า

1. ไปที่ **บัญชีลูกหนี้** > **ลูกค้า** > **ลูกค้าทั้งหมด**
2. ในกริด ให้เลือก **DE-016**
3. บนแท็บด่วน **ใบแจ้งหนี้และการจัดส่ง** ในส่วน **ภาษีขาย** ตรวจสอบว่าฟิลด์ **หมายเลขยกเว้นภาษี** ได้รับการตั้งค่าเป็น **DE9012**

### <a name="create-a-sales-order-with-an-eu-customer"></a>สร้างใบสั่งขายที่มีลูกค้าใน EU

1. ไปที่ **บัญชีลูกหนี้** > **ใบสั่ง** > **ใบสั่งขายทั้งหมด**
2. บนบานหน้าต่างการดำเนินการ เลือก **สร้าง**
3. ในกล่องโต้ตอบ **สร้างใบสั่งขาย** บนแท็บด่วน **ลูกค้า** ในส่วน **ลูกค้า** ในฟิลด์ **บัญชีลูกค้า** ให้เลือก **DE-016**
4. บนแท็บด่วน **ทั่วไป** ในส่วน **มิติการจัดเก็บ** ในฟิลด์ **ไซต์** ให้เลือก **1**
5. ในฟิลด์  **คลังสินค้า** เลือก **11**
6. บนแท็บ **ที่อยู่** ให้ตรวจสอบว่ามีการตั้งค่าฟิลด์ **ที่อยู่** เป็น **Teichgasse 12, Kiel, 24103, DEU** เนื่องจากลูกค้ามาจากเยอรมนี
7. เลือก **ตกลง**
8. บนแท็บ **ส่วนหัว** บน FastTab **การจัดส่ง** ตรวจสอบว่ามีการตั้งค่าฟิลด์ **เงื่อนไขการจัดส่ง** เป็น **CIF** และได้ตั้งค่าฟิลด์ **โหมดการจัดส่ง** เป็น **10**
9. บนแท็บ **รายการ** บน FastTab **รายการใบสั่งขาย** ในฟิลด์ **หมายเลขสินค้า** ให้เลือก **D0001** จากนั้น ในฟิลด์ **ปริมาณ** ให้ป้อน **8**
10. บน FastTab **รายละเอียดรายการ** บนแท็บ **การค้าต่างประเทศ** ตรวจสอบว่ามีการตั้งค่าฟิลด์ **รหัสธุรกรรม** เป็น **11** มีการตั้งค่าฟิลด์ **โภคภัณฑ์** เป็น **100 200 30** และตั้งค่าฟิลด์ **ประเทศ/ภูมิภาคต้นทาง** เป็น **POL**
11. บนบานหน้าต่างการดำเนินการ เลือก **บันทึก**
12. ในบานหน้าต่างการดำเนินการ บนแท็บ **ใบแจ้งหนี้** ในกลุ่ม **สร้าง** ให้เลือก **ใบแจ้งหนี้**
13. ในกล่องโต้ตอบ **การลงรายการบัญชีใบแจ้งหนี้** บนแท็บด่วน **พารามิเตอร์** ในส่วน **พารามิเตอร์** ในฟิลด์ **ปริมาณ** ให้เลือก **ทั้งหมด**
14. บน FastTab **การตั้งค่า** ในฟิลด์ **วันที่ขาย** ให้เลือก **10/18/2021** (18 ตุลาคม 2021)
15. เลือก **ตกลง** เพื่อลงรายการบัญชีใบแจ้งหนี้

### <a name="transfer-the-transaction-to-the-intrastat-journal-and-review-the-result"></a>โอนย้ายธุรกรรมไปยังสมุดรายวันอินทราสแทต และรีวิวผลลัพธ์

1. ไปที่ **ภาษี** > **การรายงาน** > **การค้าต่างประเทศ** > **อินทราสแทต**
2. บนบานหน้าต่างการดำเนินการ เลือก **โอนย้าย**
3. ในกล่องโต้ตอบ **อินทราสแทต (โอนย้าย)** ในส่วน **พารามิเตอร์** ให้ตั้งค่าตัวเลือก **ใบแจ้งหนี้ของลูกค้า** เป็น **ใช่**
4. เลือก **ตัวกรอง**
5. ในกล่องโต้ตอบ **ตัวกรองข้อมูลอินทราสแทต** บนแท็บ **ช่วง** ให้เลือกบรรทัดแรก และตรวจสอบว่ามีการตั้งค่าฟิลด์ **ฟิลด์** เป็น **วันที่**
6. ในฟิลด์ **เงื่อนไข** ให้เลือกวันที่ปัจจุบัน
7. เลือก **ตกลง** เพื่อปิดกล่องโต้ตอบ **ตัวกรองข้อมูลอินทราสแทต**
8. เลือก **ตกลง** เพื่อปิดกล่องโต้ตอบ **อินทราสแทต (การโอนย้าย)** และรีวิวผลลัพธ์ รายการนี้แสดงถึงใบสั่งขายที่คุณสร้างก่อนหน้านี้

    ![รายการนี้แสดงถึงใบสั่งขายในหน้าอินทราสแทต](media/intrastat_pl_1.png)

9. เลือกรายการธุรกรรม แล้วจากนั้น เลือกแท็บ **ทั่วไป** เพื่อดูรายละเอียดเพิ่มเติม

    ![รายละเอียดใบสั่งขายบนแท็บทั่วไปของหน้าอินทราสแทต](media/intrastat_pl_2.png)

10. ในบานหน้าต่างการดำเนินการ เลือก **ผลลัพธ์** > **รายงาน**
11. ในกล่องโต้ตอบ **รายงานอินทราสแทต** บน FastTab **พารามิเตอร์** ในส่วน **วันที่** ในฟิลด์ **จากวันที่** ให้เลือกวันแรกของเดือนปัจจุบัน
12. ในส่วน **ตัวเลือก** **การส่งออก** ให้ตั้งค่าตัวเลือก **สร้างไฟล์** เป็น **ใช่** จากนั้น ในฟิลด์ **ชื่อไฟล์** ให้ป้อนชื่อที่ต้องการ
13. ตั้งค่าตัวเลือก **สร้างรายงาน** เป็น **ใช่** จากนั้น ในฟิลด์ **ชื่อไฟล์รายงาน** ให้ป้อนชื่อที่ต้องการ
14. ในฟิลด์ **ทิศทาง** ให้เลือก **การจัดส่ง**
15. ในส่วน **การแม็ปรูปแบบไฟล์** ให้ตรวจสอบว่ามีการตั้งค่าฟิลด์ **ชนิดของการรายงาน** เป็น **การรายงานภาษี**
16. ในฟิลด์ **เมืองของการสร้างเอกสาร** ให้ป้อน **Krakow**
17. ในฟิลด์ **วันที่สร้างเอกสาร** ให้เลือก **10/19/2021** (19 ตุลาคม 2021)
18. ในฟิลด์ **หมายเลขเอกสาร** ให้ป้อน **11**
19. ในฟิลด์ **รุ่นเอกสาร** ให้ป้อน **22**
20. เลือก **ตกลง** และรีวิวรายงานในรูปแบบ XML ที่สร้างขึ้น ตารางต่อไปนี้แสดงค่าในรายงานตัวอย่าง

    <table>
    <tbody>
    <tr>
    <td>
    <p><strong>ชื่อฟิลด์</strong></p>
    </td>
    <td>
    <p><strong>คำอธิบายฟิลด์</strong></p>
    </td>
    <td>
    <p><strong>มูลค่า</strong></p>
    </td>
    </tr>
    <tr>
    <td colspan="3">
    <p><strong>ข้อมูลเกี่ยวกับเอกสาร</strong></p>
    </td>
    </tr>
    <tr>
    <td>
    <p>ข้อมูล Deklaracja</p>
    </td>
    <td>
    <p>วันที่สร้างเอกสาร</p>
    </td>
    <td>
    <p>วันที่ 2021-10-19</p>
    </td>
    </tr>
    <tr>
    <td>
    <p>Miejscowosc</p>
    </td>
    <td>
    <p>เมืองที่สร้างเอกสาร</p>
    </td>
    <td>
    <p>Krakow</p>
    </td>
    </tr>
    <tr>
    <td>
    <p>LacznaLiczbaPozycji</p>
    </td>
    <td>
    <p>จำนวนรวมของสินค้า</p>
    </td>
    <td>
    <p>1</p>
    </td>
    </tr>
    <tr>
    <td>
    <p>LacznaWartoscStatystyczna</p>
    </td>
    <td>
    <p>ค่ารวมทางสถิติ</p>
    </td>
    <td>
    <p>2632</p>
    </td>
    </tr>
    <tr>
    <td>
    <p>LacznaWartoscFaktur</p>
    </td>
    <td>
    <p>ค่ารวมในใบแจ้งหนี้</p>
    </td>
    <td>
    <p>2632</p>
    </td>
    </tr>
    <tr>
    <td>
    <p>UC</p>
    </td>
    <td>
    <p>รหัสหน่วย</p>
    </td>
    <td>
    <p>420000</p>
    </td>
    </tr>
    <tr>
    <td>
    <p>Rodzaj</p>
    </td>
    <td>
    <p>ชนิดของการรายงานภาษี</p>
    </td>
    <td>
    <p>D</p>
    </td>
    </tr>
    <tr>
    <td>
    <p>Wersja</p>
    </td>
    <td>
    <p>รุ่นของเอกสาร</p>
    </td>
    <td>
    <p>22</p>
    </td>
    </tr>
    <tr>
    <td>
    <p>Numer</p>
    </td>
    <td>
    <p>หมายเลขเอกสาร</p>
    </td>
    <td>
    <p>11</p>
    </td>
    </tr>
    <tr>
    <td width="191">
    <p>Miesiac</p>
    </td>
    <td width="330">
    <p>เดือนที่อ้างอิง</p>
    </td>
    <td>
    <p>10</p>
    </td>
    </tr>
    <tr>
    <td width="191">
    <p>Rok</p>
    </td>
    <td width="330">
    <p>ปีที่อ้างอิง</p>
    </td>
    <td>
    <p>2021</p>
    </td>
    </tr>
    <tr>
    <td width="191">
    <p>Typ</p>
    </td>
    <td width="330">
    <p>ทิศทางของรายงาน</p>
    </td>
    <td>
    <p>พ.</p>
    </td>
    </tr>
    <tr>
    <td width="191">
    <p>NrWlasny</p>
    </td>
    <td width="330">
    <p>รหัสการรายงานภาษี</p>
    </td>
    <td>
    <p>21ISTDEMF-0001</p>
    </td>
    </tr>
    <tr>
    <td colspan="3">
    <p><strong>ข้อมูลเกี่ยวกับบริษัท</strong></p>
    </td>
    </tr>
    <tr>
    <td width="191">
    <p>Miejscowosc</p>
    </td>
    <td width="330">
    <p>เมืองที่บริษัทตั้งอยู่ </p>
    </td>
    <td>
    <p>วอร์ซอ</p>
    </td>
    </tr>
    <tr>
    <td width="191">
    <p>Regon</p>
    </td>
    <td width="330">
    <p>รหัสภูมิภาคของบริษัท</p>
    </td>
    <td>
    <p>12345678901234</p>
    </td>
    </tr>
    <tr>
    <td>
    <p>Nip</p>
    </td>
    <td>
    <p>รหัส NIP ของบริษัท</p>
    </td>
    <td>
    <p>1234567890</p>
    </td>
    </tr>
    <tr>
    <td>
    <p>KodPocztowy</p>
    </td>
    <td>
    <p>รหัสไปรษณีย์ของบริษัท</p>
    </td>
    <td>
    <p>31-111</p>
    </td>
    </tr>
    <tr>
    <td>
    <p>UlicaNumer</p>
    </td>
    <td>
    <p>ถนนที่ตั้งของบริษัท </p>
    </td>
    <td>
    <p>Statystyczna 22/1</p>
    </td>
    </tr>
    <tr>
    <td>
    <p>Nazwa</p>
    </td>
    <td>
    <p>ชื่อของบริษัท</p>
    </td>
    <td>
    <p>Contoso Entertainment System Germany</p>
    </td>
    </tr>
    <tr>
    <td colspan="3">
    <p><strong>ข้อมูลเกี่ยวกับสินค้า</strong></p>
    </td>
    </tr>
    <tr>
    <td>
    <p>WartoscStatystyczna</p>
    </td>
    <td>
    <p>ค่าทางสถิติ</p>
    </td>
    <td>
    <p>2632</p>
    </td>
    </tr>
    <tr>
    <td>
    <p>WartoscFaktury</p>
    </td>
    <td>
    <p>มูลค่าในใบแจ้งหนี้</p>
    </td>
    <td>
    <p>2632</p>
    </td>
    </tr>
    <tr>
    <td>
    <p>MasaNetto</p>
    </td>
    <td>
    <p>มวลสุทธิ</p>
    </td>
    <td>
    <p>16</p>
    </td>
    </tr>
    <tr>
    <td>
    <p>IdKontrahenta</p>
    </td>
    <td>
    <p>หมายเลขภาษีมูลค่าเพิ่มของลูกค้า</p>
    </td>
    <td>
    <p>DE9012</p>
    </td>
    </tr>
    <tr>
    <td>
    <p>KodTowarowy</p>
    </td>
    <td>
    <p>รหัสโภคภัณฑ์</p>
    </td>
    <td>
    <p>10020030</p>
    </td>
    </tr>
    <tr>
    <td>
    <p>RodzajTransakcji</p>
    </td>
    <td>
    <p>รหัสธุรกรรม</p>
    </td>
    <td>
    <p>11</p>
    </td>
    </tr>
    <tr>
    <td>
    <p>WarunkiDostawy</p>
    </td>
    <td>
    <p>โหมดเงื่อนไขการจัดส่ง</p>
    </td>
    <td>
    <p>CIF</p>
    </td>
    </tr>
    <tr>
    <td>
    <p>KrajPochodzeniaWysylki</p>
    </td>
    <td>
    <p>รหัสประเทศหรือภูมิภาคของการจัดส่ง/ปลายทาง</p>
    </td>
    <td>
    <p>DE</p>
    </td>
    </tr>
    <tr>
    <td>
    <p>OpisTowaru</p>
    </td>
    <td>
    <p>คำอธิบายของโภคภัณฑ์</p>
    </td>
    <td>
    <p>ฮาร์ดแวร์</p>
    </td>
    </tr>
    <tr>
    <td>
    <p>PozId</p>
    </td>
    <td>
    <p>หมายเลขสินค้า </p>
    </td>
    <td>
    <p>1</p>
    </td>
    </tr>
    <tr>
    <td colspan="3">
    <p><strong>ข้อมูลการติดต่อ</strong></p>
    </td>
    </tr>
    <tr>
    <td>
    <p>อีเมล</p>
    </td>
    <td>
    <p>ที่อยู่อีเมลของผู้ส่ง</p>
    </td>
    <td>
    <p>manishc@contoso.com</p>
    </td>
    </tr>
    <tr>
    <td>
    <p>Faks</p>
    </td>
    <td>
    <p>หมายเลขโทรสารของผู้ส่ง</p>
    </td>
    <td>
    <p>วันที่ 425-555-5049</p>
    </td>
    </tr>
    <tr>
    <td>
    <p>Telefon</p>
    </td>
    <td>
    <p>หมายเลขโทรศัพท์ของผู้ส่ง</p>
    </td>
    <td>
    <p>วันที่ 425-555-5068</p>
    </td>
    </tr>
    <tr>
    <td>
    <p>NazwiskoImie</p>
    </td>
    <td>
    <p>ชื่อผู้ส่ง</p>
    </td>
    <td>
    <p>Manish Chopra</p>
    </td>
    </tr>
    </tbody>
    </table>

21. ตรวจทานรายงานในรูปแบบ Excel ที่สร้าง

    ![รายงานอินทราสแทตสำหรับการจัดส่ง](media/intrastat_pl_3.png)

### <a name="create-a-purchase-order"></a>สร้างใบสั่งซื้อ

1. ไปที่ **บัญชีเจ้าหนี้** > **ใบสั่งซื้อ** > **ใบสั่งซื้อทั้งหมด**
2. บนบานหน้าต่างการดำเนินการ เลือก **สร้าง**
3. ในกล่องโต้ตอบ **สร้างใบสั่งซื้อ** ในฟิลด์ **บัญชีผู้จัดจำหน่าย** ให้เลือก **DE-001**
4. ในฟิลด์ **ไซต์** ให้เลือก **1**
5. ในฟิลด์ **คลังสินค้า** เลือก **11**
6. เลือก **ตกลง**
7. บนแท็บ **ส่วนหัว** บน FastTab **การจัดส่ง** ตรวจสอบว่ามีการตั้งค่าฟิลด์ **โหมดการจัดส่ง** เป็น **10** และได้ตั้งค่าฟิลด์ **เงื่อนไขการจัดส่ง** เป็น **CIF**
8. บนแท็บ **รายการ** บนแท็บด่วน **รายการใบสั่งซื้อ** ในฟิลด์ **หมายเลขสินค้า** ให้เลือก **D0003** จากนั้น ในฟิลด์ **ปริมาณ** ให้ป้อน **6**
9. บน FastTab **รายละเอียดรายการ** บนแท็บ **การค้าต่างประเทศ** ตรวจสอบว่ามีการตั้งค่าฟิลด์  **รหัสธุรกรรม** เป็น **11** มีการตั้งค่าฟิลด์ **การขนส่ง** เป็น **3** ตั้งค่าฟิลด์ **โภคภัณฑ์** เป็น **100 200 30** และตั้งค่าฟิลด์ **ประเทศ/ภูมิภาคต้นทาง** เป็น **DEU**
10. ในบานหน้าต่างการดำเนินการ บนแท็บ **การซื้อ** ในกลุ่ม **การดำเนินการ** ให้เลือก **ยืนยัน**
11. ในบานหน้าต่างการดำเนินการ บนแท็บ **ใบแจ้งหนี้** ในกลุ่ม **สร้าง** ให้เลือก **ใบแจ้งหนี้**
12. ในบานหน้าต่างการดำเนินการ ให้เลือก **ค่าเริ่มต้นจาก** ในฟิลด์ **ปริมาณรายการเริ่มต้น** และจากนั้นให้เลือก **ปริมาณที่สั่ง** จากนั้น เลือก **ตกลง**
13. บน FastTab **ส่วนหัวของใบแจ้งหนี้ของผู้จัดจำหน่าย** ในส่วน **การระบุรหัสประจำตัวใบแจ้งหนี้** ในฟิลด์ **หมายเลข** ให้ป้อน **00010**
14. ในส่วน **วันที่ในใบแจ้งหนี้** ในฟิลด์ **วันที่ของใบแจ้งหนี้** ให้เลือกวันที่ปัจจุบัน วันที่นี้จะนำไปใช้กับการโอนย้ายอินทราสแทต
15. ในฟิลด์ **วันที่ได้รับเอกสาร** ให้เลือก **10/18/2021** (18 ตุลาคม 2021)
16. บนบานหน้าต่างการดำเนินการ ให้เลือก **ลงรายการบัญชี** เพื่อลงรายการบัญชีใบแจ้งหนี้

### <a name="create-an-intrastat-declaration-for-arrivals"></a>สร้างการรายงานภาษีอินทราสแทตสำหรับการมาถึง

1. ไปที่ **ภาษี** > **การรายงาน** > **การค้าต่างประเทศ** > **อินทราสแทต**
2. บนบานหน้าต่างการดำเนินการ เลือก **โอนย้าย**
3. ในกล่องโต้ตอบ **อินทราสแทต (การโอนย้าย)** ให้ตั้งค่าตัวเลือก **ใบแจ้งหนี้ของผู้จัดจำหน่าย** เป็น **ใช่**
4. เลือก **ตกลง** เพื่อโอนย้ายธุรกรรม และจากนั้น รีวิวสมุดรายวันอินทราสแทต

    ![รายการนี้แสดงถึงใบสั่งซื้อในหน้าอินทราสแทต](media/intrastat_pl_4.png)

5. ตรวจสอบข้อมูลในแท็บ **ทั่วไป** เกี่ยวกับใบสั่งซื้อ

    ![รายละเอียดใบสั่งซื้อบนแท็บทั่วไปของหน้าอินทราสแทต](media/intrastat_pl_5.png)

6. ในบานหน้าต่างการดำเนินการ เลือก **ผลลัพธ์** > **รายงาน**
7. ในกล่องโต้ตอบ **รายงานอินทราสแทต** บน FastTab **พารามิเตอร์** ในส่วน **วันที่** ในฟิลด์ **จากวันที่** ให้เลือกวันแรกของเดือนปัจจุบัน
8. ในส่วน **ตัวเลือก** **การส่งออก** ให้ตั้งค่าตัวเลือก **สร้างไฟล์** เป็น **ใช่** จากนั้น ในฟิลด์ **ชื่อไฟล์** ให้ป้อนชื่อที่ต้องการ
9. ตั้งค่าตัวเลือก **สร้างรายงาน** เป็น **ใช่** จากนั้น ในฟิลด์ **ชื่อไฟล์รายงาน** ให้ป้อนชื่อที่ต้องการ
10. ในฟิลด์ **ทิศทาง** ให้เลือก **การมาถึง**
11. ในส่วน **การแม็ปรูปแบบไฟล์** ให้ตรวจสอบว่ามีการตั้งค่าฟิลด์ **ชนิดของการรายงาน** เป็น **การรายงานภาษี**
12. ในฟิลด์ **เมืองของการสร้างเอกสาร** ให้ป้อน **Krakow**
13. ในฟิลด์ **วันที่สร้างเอกสาร** ให้เลือก **10/19/2021** (19 ตุลาคม 2021)
14. ในฟิลด์ **หมายเลขเอกสาร** ให้ป้อน **11**
15. ในฟิลด์ **รุ่นเอกสาร** ให้ป้อน **22**
16. เลือก **ตกลง** และรีวิวรายงานในรูปแบบ XML ที่สร้างขึ้น ตารางต่อไปนี้แสดงค่าในรายงานตัวอย่าง

    <table>
    <tbody>
    <tr>
    <td>
    <p><strong>ชื่อฟิลด์</strong></p>
    </td>
    <td>
    <p><strong>คำอธิบายฟิลด์</strong></p>
    </td>
    <td>
    <p><strong>มูลค่า</strong></p>
    </td>
    </tr>
    <tr>
    <td colspan="3">
    <p align=center><strong>ข้อมูลเกี่ยวกับเอกสาร</strong></p>
    </td>
    </tr>
    <tr>
    <td>
    <p>ข้อมูล Deklaracja</p>
    </td>
    <td>
    <p>วันที่สร้างเอกสาร</p>
    </td>
    <td>
    <p>วันที่ 2021-10-19</p>
    </td>
    </tr>
    <tr>
    <td>
    <p>Miejscowosc</p>
    </td>
    <td>
    <p>เมืองที่สร้างเอกสาร</p>
    </td>
    <td>
    <p>Krakow</p>
    </td>
    </tr>
    <tr>
    <td>
    <p>LacznaLiczbaPozycji</p>
    </td>
    <td>
    <p>จำนวนรวมของสินค้า</p>
    </td>
    <td>
    <p>1</p>
    </td>
    </tr>
    <tr>
    <td>
    <p>LacznaWartoscStatystyczna</p>
    </td>
    <td>
    <p>ค่ารวมทางสถิติ</p>
    </td>
    <td>
    <p>965</p>
    </td>
    </tr>
    <tr>
    <td>
    <p>LacznaWartoscFaktur</p>
    </td>
    <td>
    <p>ค่ารวมในใบแจ้งหนี้</p>
    </td>
    <td>
    <p>965</p>
    </td>
    </tr>
    <tr>
    <td>
    <p>UC</p>
    </td>
    <td>
    <p>รหัสหน่วย</p>
    </td>
    <td>
    <p>420000</p>
    </td>
    </tr>
    <tr>
    <td>
    <p>Rodzaj</p>
    </td>
    <td>
    <p>ชนิดของการรายงานภาษี</p>
    </td>
    <td>
    <p>D</p>
    </td>
    </tr>
    <tr>
    <td>
    <p>Wersja</p>
    </td>
    <td>
    <p>รุ่นของเอกสาร</p>
    </td>
    <td>
    <p>22</p>
    </td>
    </tr>
    <tr>
    <td>
    <p>Numer</p>
    </td>
    <td>
    <p>หมายเลขเอกสาร</p>
    </td>
    <td>
    <p>11</p>
    </td>
    </tr>
    <tr>
    <td width="191">
    <p>Miesiac</p>
    </td>
    <td width="332">
    <p>เดือนที่อ้างอิง</p>
    </td>
    <td>
    <p>10</p>
    </td>
    </tr>
    <tr>
    <td width="191">
    <p>Rok</p>
    </td>
    <td width="332">
    <p>ปีที่อ้างอิง</p>
    </td>
    <td>
    <p>2021</p>
    </td>
    </tr>
    <tr>
    <td width="191">
    <p>Typ</p>
    </td>
    <td width="332">
    <p>ทิศทางของรายงาน</p>
    </td>
    <td>
    <p>P</p>
    </td>
    </tr>
    <tr>
    <td width="191">
    <p>NrWlasny</p>
    </td>
    <td width="332">
    <p>รหัสการรายงานภาษี</p>
    </td>
    <td>
    <p>21ISTDEMF-0002</p>
    </td>
    </tr>
    <tr>
    <td colspan="3">
    <p align=center><strong>ข้อมูลเกี่ยวกับบริษัท</strong></p>
    </td>
    </tr>
    <tr>
    <td width="191">
    <p>Miejscowosc</p>
    </td>
    <td width="332">
    <p>เมืองที่บริษัทตั้งอยู่ </p>
    </td>
    <td>
    <p>วอร์ซอ</p>
    </td>
    </tr>
    <tr>
    <td width="191">
    <p>Regon</p>
    </td>
    <td width="332">
    <p>รหัสภูมิภาคของบริษัท</p>
    </td>
    <td>
    <p>12345678901234</p>
    </td>
    </tr>
    <tr>
    <td>
    <p>Nip</p>
    </td>
    <td>
    <p>รหัส NIP ของบริษัท</p>
    </td>
    <td>
    <p>1234567890</p>
    </td>
    </tr>
    <tr>
    <td>
    <p>KodPocztowy</p>
    </td>
    <td>
    <p>รหัสไปรษณีย์ของบริษัท</p>
    </td>
    <td>
    <p>31-111</p>
    </td>
    </tr>
    <tr>
    <td>
    <p>UlicaNumer</p>
    </td>
    <td>
    <p>ถนนที่ตั้งของบริษัท </p>
    </td>
    <td>
    <p>Statystyczna 22/1</p>
    </td>
    </tr>
    <tr>
    <td>
    <p>Nazwa</p>
    </td>
    <td>
    <p>ชื่อของบริษัท</p>
    </td>
    <td>
    <p>Contoso Entertainment System Germany</p>
    </td>
    </tr>
    <tr>
    <td colspan="3">
    <p align=center><strong>ข้อมูลเกี่ยวกับสินค้า</strong></p>
    </td>
    </tr>
    <tr>
    <td>
    <p>WartoscStatystyczna</p>
    </td>
    <td>
    <p>ค่าทางสถิติ</p>
    </td>
    <td>
    <p>965</p>
    </td>
    </tr>
    <tr>
    <td>
    <p>WartoscFaktury</p>
    </td>
    <td>
    <p>มูลค่าในใบแจ้งหนี้</p>
    </td>
    <td>
    <p>965</p>
    </td>
    </tr>
    <tr>
    <td>
    <p>MasaNetto</p>
    </td>
    <td>
    <p>มวลสุทธิ</p>
    </td>
    <td>
    <p>30</p>
    </td>
    </tr>
    <tr>
    <td>
    <p>KrajPochodzenia</p>
    </td>
    <td>
    <p>หรัสประเทศ/ภูมิภาคผู้ผลิตของสินค้า</p>
    </td>
    <td>
    <p>DE</p>
    </td>
    </tr>
    <tr>
    <td>
    <p>RodzajTransportu</p>
    </td>
    <td>
    <p>โหมดรหัสการขนส่ง</p>
    </td>
    <td>
    <p>3</p>
    </td>
    </tr>
    <tr>
    <td>
    <p>KodTowarowy</p>
    </td>
    <td>
    <p>รหัสโภคภัณฑ์</p>
    </td>
    <td>
    <p>10020030</p>
    </td>
    </tr>
    <tr>
    <td>
    <p>RodzajTransakcji</p>
    </td>
    <td>
    <p>รหัสธุรกรรม</p>
    </td>
    <td>
    <p>11</p>
    </td>
    </tr>
    <tr>
    <td>
    <p>WarunkiDostawy</p>
    </td>
    <td>
    <p>โหมดเงื่อนไขการจัดส่ง</p>
    </td>
    <td>
    <p>CIF</p>
    </td>
    </tr>
    <tr>
    <td>
    <p>KrajPochodzeniaWysylki</p>
    </td>
    <td>
    <p>รหัสประเทศหรือภูมิภาคของการจัดส่ง/ปลายทาง</p>
    </td>
    <td>
    <p>DE</p>
    </td>
    </tr>
    <tr>
    <td>
    <p>OpisTowaru</p>
    </td>
    <td>
    <p>คำอธิบายของโภคภัณฑ์</p>
    </td>
    <td>
    <p>ฮาร์ดแวร์</p>
    </td>
    </tr>
    <tr>
    <td>
    <p>PozId</p>
    </td>
    <td>
    <p>หมายเลขสินค้า </p>
    </td>
    <td>
    <p>1</p>
    </td>
    </tr>
    <tr>
    <td colspan="3">
    <p align=center><strong>ข้อมูลการติดต่อ</strong></p>
    </td>
    </tr>
    <tr>
    <td>
    <p>อีเมล</p>
    </td>
    <td>
    <p>ที่อยู่อีเมลของผู้ส่ง</p>
    </td>
    <td>
    <p>manishc@contoso.com</p>
    </td>
    </tr>
    <tr>
    <td>
    <p>Faks</p>
    </td>
    <td>
    <p>หมายเลขโทรสารของผู้ส่ง</p>
    </td>
    <td>
    <p>วันที่ 425-555-5049</p>
    </td>
    </tr>
    <tr>
    <td>
    <p>Telefon</p>
    </td>
    <td>
    <p>หมายเลขโทรศัพท์ของผู้ส่ง</p>
    </td>
    <td>
    <p>วันที่ 425-555-5068</p>
    </td>
    </tr>
    <tr>
    <td>
    <p>NazwiskoImie</p>
    </td>
    <td>
    <p>ชื่อผู้ส่ง</p>
    </td>
    <td>
    <p>Manish Chopra</p>
    </td>
    </tr>
    </tbody>
    </table>

17. ตรวจทานรายงานในรูปแบบ Excel ที่สร้าง

    ![รายงานการมาถึงของอินทราสแทต](media/intrastat_pl_6.png)
