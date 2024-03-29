---
title: สร้างและตั้งค่าคอนฟิกการขยายเวลาการรับประกัน
description: บทความนี้ครอบคลุมถึงการรับประกันแบบขยาย และอธิบายวิธีการสร้างและตั้งค่าคอนฟิกใน Microsoft Dynamics 365 Commerce
author: josaw1
ms.date: 06/08/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: josaw
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: ''
ms.custom: ''
ms.assetid: ''
ms.search.industry: ''
ms.openlocfilehash: 3754de54763be52c9090596fac0e170b0c5fc520
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 08/12/2022
ms.locfileid: "9268380"
---
# <a name="create-and-configure-extended-warranties"></a>สร้างและตั้งค่าคอนฟิกการขยายเวลาการรับประกัน

[!include [banner](includes/banner.md)]

บทความนี้ครอบคลุมถึงการรับประกันแบบขยาย และอธิบายวิธีการสร้างและตั้งค่าคอนฟิกใน Microsoft Dynamics 365 Commerce

## <a name="overview"></a>ภาพรวม

ลูกค้ามีการเลือกบริการและการสนับสนุนแบบขยายเพิ่มเติม เมื่อพวกเขาซื้อผลิตภัณฑ์ โดยเฉพาะผลิตภัณฑ์อุปโภคบริโภคซึ่งขายที่จุดราคาพิเศษ เช่น โทรศัพท์ และคอมพิวเตอร์ โดยการให้การรับประกันแบบขยายสำหรับการซื้อ ร้านค้าปลีกสามารถช่วยสร้างความภักดีของลูกค้า การรับประกันแบบขยายช่วยให้ลูกค้าทราบว่าสามารถไปที่บริการและการสนับสนุนได้ที่ใด ดังนั้น พวกเขาจึงมีความมั่นใจว่าจะมีการจัดการปัญหาของพวกเขาอย่างมีประสิทธิภาพ

การรับประกันแบบขยายสามารถขายให้กับลูกค้าในช่องทางการขายปลีกระหว่างการซื้อผลิตภัณฑ์เริ่มต้น นอกจากนี้ ยังสามารถขายได้เป็นเวลาที่จำกัด หลังจากการซื้อครั้งแรก

### <a name="warranty-item-setup"></a>การตั้งค่าสินค้าที่มีการรับประกัน

Dynamics 365 Commerce แสดงฟังก์ชันที่ช่วยให้คุณสามารถสร้างสินค้าที่มีการรับประกันและตั้งค่าแอตทริบิวต์สำหรับใบรับประกัน แอตทริบิวต์เหล่านี้รวมถึงการเชื่อมโยงระหว่างผลิตภัณฑ์และสินค้าที่มีการรับประกัน ราคาของการรับประกัน และระยะเวลาของการรับประกัน หลังจากที่มีการตั้งค่าคอนฟิกสินค้าที่มีการรับประกันและนำออกใช้ในหน่วยขององค์กร ผู้ค้าปลีกสามารถขายการรับประกันผ่านการขายหน้าร้านสมัยใหม่ (MPOS) ร้านค้าออนไลน์ และช่องทางการขายปลีกอื่นๆ

### <a name="warranty-item-sales"></a>การขายสินค้าที่มีการรับประกัน

การรับประกันแบบขยายถูกขายให้กับลูกค้าในช่องทางการขายปลีกระหว่างการซื้อผลิตภัณฑ์เริ่มต้น นอกจากนี้ ยังสามารถขายได้เป็นเวลาที่จำกัด หลังจากการซื้อครั้งแรก

ในการขายหน้าร้าน (POS) บริษัทผู้ขายจะได้รับการแจ้งเตือนให้เพิ่มการรับประกันแบบขยาย เมื่อมีการเพิ่มผลิตภัณฑ์ที่เกี่ยวข้องไปยังรถเข็นของลูกค้า ดังนั้น โอกาสสำหรับการขายสินค้าต่อเนื่องและการขายสินค้าชนิดอื่นจะถูกแสดงต่อบริษัทผู้ขายโดยเป็นส่วนหนึ่งของโฟลว์การขาย

นอกจากนี้ ลูกค้ายังสามารถส่งคืนในภายหลัง และซื้อการรับประกันแบบขยายสำหรับผลิตภัณฑ์ที่พวกเขาซื้อมาก่อนหน้านี้ ในกรณีเหล่านี้ บริษัทผู้ขายสามารถค้นหาธุรกรรมเดิมและขายสินค้าที่มีการรับประกันแบบขยายที่เกี่ยวข้องแก่ลูกค้า

### <a name="warranty-terminology"></a>คำศัพท์ของการรับประกัน

ตารางต่อไปนี้กำหนดเงื่อนไขบางอย่างที่เกี่ยวข้องกับการรับประกัน

| เงื่อนไข | คำอธิบาย |
|------------------------------|--------------|
| การรับประกันแบบขยาย/การรับประกัน | *การรับประกันแบบขยาย* อ้างอิงถึงข้อตกลงการให้บริการหรือสัญญาที่ให้การรับประกันแบบขยายแก่ลูกค้า การรับประกันแบบขยายรวมถึงบริการเพิ่มเติมของการแทนที่หรือซ่อมแซมสินค้า ในระหว่างรอบระยะเวลาความครอบคลุมของการรับประกันแบบขยาย |
| การรับประกันของผู้ผลิต | *การรับประกันของผู้ผลิต* (โดยทั่วไปจะเรียกว่า *การรับประกันแบบจำกัด*) คือการรับประกันที่ลูกค้าจะได้รับ เมื่อพวกเขาซื้อผลิตภัณฑ์ คุณลักษณะบางอย่างของการรับประกันของผู้ผลิตมีดังนี้:<ul><li>ต้นทุนการรับประกันจะรวมอยู่ในต้นทุนของผลิตภัณฑ์ ลูกค้าไม่ต้องชำระเงินเพิ่มเติมใดๆ สำหรับการรับประกันของผู้ผลิต</li><li>ทั้งนี้ขึ้นอยู่กับประเภทผลิตภัณฑ์ โดยทั่วไปแล้วการรับประกันของผู้ผลิตจะมีอายุ 30 วัน 6 เดือน หรือหนึ่งปี (สำหรับเครื่องใช้ไฟฟ้าของผู้บริโภคส่วนใหญ่ การรับประกันมีระยะเวลาหนึ่งปี)</li><li>การรับประกันครอบคลุมข้อบกพร่องใดๆ ที่เกิดขึ้นจากความล้มเหลวทางกลหรือทางอิเล็กทรอนิกส์ ความคุ้มครองมีจำกัด และไม่รวมความเสียหายโดยไม่ได้ตั้งใจใดๆ กับผลิตภัณฑ์ที่ซื้อ ลูกค้าที่ต้องการป้องกันผลิตภัณฑ์ที่พวกเขาซื้อจากความเสียหายในชีวิตประจำวัน ควรลงทุนในการรับประกันแบบขยาย การรับประกันแบบขยายมีอายุสองถึงสิบปี ทั้งนี้ขึ้นอยู่กับประเภทผลิตภัณฑ์ นอกจากนี้ ยังมีความครอบคลุมที่กว้างขึ้นและครอบคลุมอุบัติเหตุประจำวัน เช่น หยด รั่ว และคราบ</li></ul> |
| สินค้าการรับประกัน | *สินค้าที่มีการรับประกัน* เป็นสินค้าที่มีการรับประกันแบบขยายที่ขายสำหรับสินค้าที่สามารถรับประกันได้ ตัวอย่างได้แก่ แผนการป้องกันด้านอุบัติเหตุสองปีสำหรับแล็ปท็อป |
| สินค้าที่สามารถรับประกันได้ | *สินค้าที่สามารถรับประกันได้* เป็นผลิตภัณฑ์ที่กำหนดหมายเลขลำดับประจำสินค้าที่มีการขายการรับประกันให้ ตัวอย่างเช่น แล็ปท็อปเป็นสินค้าที่สามารถรับประกันได้ที่มีการขายการรับประกันแบบขยายสองปีและสามปีให้ |
| กลุ่มการรับประกัน | *กลุ่มการรับประกัน* คือความสัมพันธ์ระหว่างสินค้าที่มีการรับประกันและสินค้าที่สามารถรับประกันได้ POS ใช้กลุ่มการรับประกันเพื่อตรวจสอบว่า ควรมีการแจ้งเตือนบริษัทผู้ขายสินค้าที่สามารถรับประกันได้ใดให้มีการเพิ่มสินค้าที่สามารถรับประกันได้ในรถเข็นของลูกค้า |
| นโยบายการรับประกัน | *นโยบายการรับประกัน* คือเอนทิตีที่สร้างขึ้นใน Commerce เมื่อมีการขายนโยบายการรับประกัน นโยบายการรับประกันรวมถึงข้อมูล เช่น วันที่เริ่มต้นและวันที่สิ้นสุดของสินค้าที่มีการรับประกันที่ซื้อ ข้อกำหนดและเงื่อนไข และหมายเลขลำดับประจำสินค้าของผลิตภัณฑ์ที่ได้รับการประกัน หมายเลขนโยบายการรับประกันสามารถใช้ร่วมกันกับลูกค้า เพื่อให้พวกเขามีการอ้างอิงสำหรับสินค้าที่มีการรับประกันแบบขยายที่พวกเขาซื้อ |

## <a name="create-a-warranty-item"></a>สร้างสินค้าที่มีการรับประกัน

เมื่อต้องการสร้างสินค้าที่มีการรับประกันใน Commerce ให้ทำตามขั้นตอนต่อไปนี้

1. ไปยัง **Retail และ Commerce \> ผลิตภัณฑ์และประเภท \> ผลิตภัณฑ์**
1. เลือก **สร้าง** เพื่อสร้างสินค้าที่มีการรับประกัน
1. ในกล่องโต้ตอบ **ผลิตภัณฑ์ใหม่** ในฟิลด์ **ชนิดผลิตภัณฑ์** ให้เลือก **บริการ**
1. ในฟิลด์ **ชนิดย่อยของผลิตภัณฑ์** เลือก **ผลิตภัณฑ์**
1. ในฟิลด์ **ชนิดบริการของผลิตภัณฑ์** เลือก **บริการ**
1. ในฟิลด์ **ชื่อผลิตภัณฑ์** ให้ป้อนชื่อผลิตภัณฑ์
1. ในฟิลด์ **ประเภท Retail** ให้เลือกค่าในกล่องโต้ตอบแบบหล่นลง แล้วจากนั้น เลือก **ตกลง**
1. ในฟิลด์ **หมายเลขผลิตภัณฑ์** ให้ป้อนหมายเลขผลิตภัณฑ์
1. เลือก **ตกลง**
1. บนหน้า **รายละเอียดผลิตภัณฑ์** บน FastTab **การรับประกัน** ให้ตั้งค่าฟิลด์ **หน่วยเวลา** และ **ระยะเวลา**

    | ชื่อฟิลด์ | มูลค่า | คำอธิบาย |
    |------------|-------|-------------|
    | หน่วยของเวลา | **วัน** **สัปดาห์** **เดือน** หรือ **ปี** | ฟิลด์นี้จะระบุหน่วยเวลาที่จะใช้สำหรับการรับประกัน |
    | ช่วงของเวลา | ค่าจำนวนเต็มบวก | ฟิลด์นี้จะระบุระยะเวลาของการรับประกันในหน่วยเวลาที่เลือก |

    ตัวอย่างเช่น สำหรับการรับประกันสองปี ให้ตั้งค่าฟิลด์ **หน่วยของเวลา** เป็น **ปี** และฟิลด์ **ระยะเวลา** เป็น **2** หรือให้ตั้งค่าฟิลด์ **หน่วยของเวลา** เป็น **เดือน** และฟิลด์ **ระยะเวลา** เป็น **24** ดังที่แสดงในภาพประกอบต่อไปนี้

    ![หน้ารายละเอียดผลิตภัณฑ์สำหรับสินค้าที่มีการรับประกัน](./media/ew-time-properties.png)

1. เลือก **บันทึก** เพื่อบันทึกสินค้าที่มีการรับประกัน
1. นำผลิตภัณฑ์ที่มีการรับประกันไปใช้กับบริษัท เพื่อให้สามารถขายได้ สำหรับข้อมูลเพิ่มเติม โปรดดู [ตั้งค่าผลิตภัณฑ์ขายปลีก](set-up-retail-products.md)
1. บนหน้า **รายละเอียดผลิตภัณฑ์ที่นำออกใช้** บน FastTab **การรับประกัน** ให้ตั้งค่าฟิลด์ **ฐานของช่วงราคา** **ขีดจำกัดล่าง** และ **ขีดจำกัดบน**

    | ชื่อฟิลด์ | มูลค่า | คำอธิบาย |
    |------------|-------|-------------|
    | ฐานช่วงราคา | **ไม่มี** **ราคาฐาน** หรือ **ราคาขาย** | <ul><li>**ไม่มี** – ค่า **ขีดจำกัดล่าง** และ **ขีดจำกัดบน** ของช่วงราคาไม่สามารถใช้ได้</li><li>**ราคาฐาน** – การรับประกันที่กำหนดจะสามารถใช้ได้ ถ้าราคาฐาน (กล่าวคือ ราคาที่ไม่มีส่วนลด) ของสินค้าที่สามารถรับประกันได้อยู่ระหว่างค่า **ขีดจำกัดล่าง** และ **ขีดจำกัดบน** ที่ระบุไว้ที่นี่ โดยยึดตามราคาของสินค้าที่สามารถรับประกันได้</li><li>**ราคาขาย** – ค่านี้สงวนไว้สำหรับการใช้ในอนาคต</li></ul> |
    | ขีดจำกัดล่าง ขีดจำกัดบน | ค่าจำนวนเต็มบวก | ฟิลด์เหล่านี้จะกำหนดขีดจำกัดราคาบนและล่างของสินค้าที่สามารถรับประกันได้ และวิธีการที่สินค้าที่มีการรับประกันปัจจุบันเกี่ยวข้องกับสินค้าที่มีการรับประกัน ขีดจำกัดเหล่านี้จะขึ้นอยู่กับราคาฐานของสินค้าที่สามารถรับประกันได้ (หรือที่เรียกอีกอย่างหนึ่งว่า ราคาขายปลีกที่แนะนำของผู้ผลิต \[MSRP\]) ถ้าฟิลด์ **ฐานของช่วงราคา** ได้รับการตั้งค่าเป็น **ราคาฐาน** เฉพาะสินค้าที่สามารถรับประกันได้ (ผลิตภัณฑ์) ที่มีราคาฐานระหว่างค่า **ขีดจำกัดล่าง** และ **ขีดจำกัดบน** จะทริกเกอร์พร้อมท์เพื่อเพิ่มสินค้าที่สามารถรับประกันได้ที่ POS |

    ตัวอย่างเช่น ภาพประกอบต่อไปนี้แสดงฟิลด์ **ฐานของช่วงราคา** ที่ตั้งค่าเป็น **ราคาฐาน** ฟิลด์ **ขีดจำกัดล่าง** ที่ถูกตั้งค่าเป็น $500 และฟิลด์ **ขีดจำกัดบน** ที่ถูกตั้งค่าเป็น $1000
    
    ![หน้ารายละเอียดผลิตภัณฑ์ที่นำออกใช้สำหรับสินค้าที่มีการรับประกัน](./media/ew-release-product-details.png)

1. จัดประเภทสินค้าที่มีการรับประกันไปยังช่องทางที่จะมีการขาย สำหรับข้อมูลเพิ่มเติม โปรดดู [ตั้งค่าการจัดประเภท](set-up-assortments.md)

### <a name="example"></a>ตัวอย่าง

สินค้าที่สามารถรับประกันได้ของแล็ปท็อป (ผลิตภัณฑ์) มีราคาฐานเป็น $999 และมีสินค้าที่มีการรับประกันสำหรับแล็ปท็อปสองรายการ:

- การรับประกัน\_1 มีขีดจำกัดล่างเป็น $500 และขีดจำกัดบนเป็น $1,000 และฟิลด์ **ฐานของช่วงราคา** ถูกตั้งค่าเป็น **ราคาฐาน**
- การรับประกัน\_2 มีขีดจำกัดล่างเป็น $1,001 และขีดจำกัดบนเป็น $2,000 และฟิลด์ **ฐานของช่วงราคา** ถูกตั้งค่าเป็น **ราคาฐาน**

ในกรณีนี้ เมื่อมีการเพิ่มสินค้าที่สามารถรับประกันได้ของแล็ปท็อปไปยังรถเข็นของลูกค้า จะมีการแสดงพร้อมท์เพื่อเพิ่มการรับประกัน\_1 ที่ POS เนื่องจากราคาของแล็ปท็อปอยู่ระหว่างขีดจำกัดล่างและขีดจำกัดบนสำหรับการรับประกัน\_1

> [!NOTE]
> สำหรับตัวอย่างนี้ ถ้าคุณต้องการแสดงพร้อมต์สำหรับทั้งการรับประกัน\_1 และการรับประกัน\_2 โดยไม่คำนึงถึงราคาของสินค้าที่สามารถรับประกันได้ ให้ตั้งค่าฟิลด์ **ฐานของช่วงราคา** เป็น **ไม่มี**

## <a name="configure-channel-specific-settings"></a>ตั้งค่าคอนฟิกการตั้งค่าเฉพาะช่องทาง

การตั้งค่าเฉพาะช่องทางจะช่วยให้คุณสามารถระบุว่า จะมีการแสดงพร้อมท์เพื่อเพิ่มสินค้าที่มีการรับประกันที่ POS หรือไม่ เมื่อมีการเพิ่มสินค้าที่สามารถรับประกันได้ไปยังรถเข็นของลูกค้า

เมื่อต้องการตั้งค่าคอนฟิกการตั้งค่าเฉพาะช่องทางใน Commerce ให้ทำตามขั้นตอนต่อไปนี้

1. ไปยัง **Retail และ Commerce \> ผลิตภัณฑ์และประเภท \> การรับประกัน \> การตั้งค่าการรับประกัน**
1. บนแท็บ **เฉพาะช่องทาง** ในคอลัมน์ **พร้อมต์สำหรับการรับประกัน** สำหรับช่องทางของคุณ ให้ทำตามขั้นตอนใดขั้นตอนหนึ่งต่อไปนี้:

    - เลือกกล่องกาเครื่องหมายนี้ ถ้าควรแสดงพร้อมต์สำหรับสินค้าที่มีการรับประกันที่ POS เมื่อมีการเพิ่มสินค้าที่สามารถรับประกันได้ในรถเข็น
    - ล้างกล่องกาเครื่องหมาย ถ้าไม่ควรแสดงพร้อมต์สำหรับสินค้าที่มีการรับประกันที่ POS เมื่อมีการเพิ่มสินค้าที่สามารถรับประกันได้ในรถเข็น

1. รันงาน **1070** เพื่อซิงค์ข้อมูลไปยังช่องทาง

## <a name="configure-a-number-sequence-for-warranty-policies"></a>ตั้งค่าคอนฟิกลำดับหมายเลขสำหรับนโยบายการรับประกัน

นโยบายการรับประกันแต่ละนโยบายจะถูกระบุโดยไม่ซ้ำกันโดยหมายเลขนโยบายการรับประกันซึ่งสร้างขึ้นโดยลำดับหมายเลข สำหรับข้อมูลเพิ่มเติมเกี่ยวกับลำดับหมายเลข ให้ดู [ภาพรวมลำดับหมายเลข](../fin-ops-core/fin-ops/organization-administration/number-sequence-overview.md)

เมื่อต้องการตั้งค่าคอนฟิกลำดับหมายเลขสำหรับนโยบายการรับประกันใน Commerce ให้ทำตามขั้นตอนต่อไปนี้

1. ไปยัง **Retail และ Commerce \> ผลิตภัณฑ์และประเภท \> การรับประกัน \> การตั้งค่าการรับประกัน**
1. บนแท็บ **ลำดับหมายเลข** ในแถวสำหรับการอ้างอิง **นโยบายการรับประกัน** ให้ป้อนหรือเลือกค่าในฟิลด์ **รหัสลำดับหมายเลข**

## <a name="set-up-a-warranty-group"></a>ตั้งค่ากลุ่มการรับประกัน

กลุ่มการรับประกันคือ ความสัมพันธ์ระหว่างสินค้าที่มีการรับประกันและสินค้าที่สามารถรับประกันได้ POS ใช้กลุ่มการรับประกันเพื่อตรวจสอบว่า ควรมีการแจ้งเตือนบริษัทผู้ขายสินค้าที่สามารถรับประกันได้ใดให้มีการเพิ่มสินค้าที่สามารถรับประกันได้ในรถเข็นของลูกค้า

ในการตั้งค่าการกำหนดกลุ่มการรับประกันใน Commerce ให้ทำตามขั้นตอนเหล่านี้

1. ไปยัง **Retail และ Commerce \> ผลิตภัณฑ์และประเภท \> การรับประกัน \> กลุ่มการรับประกัน**
1. เลือก **สร้าง** เพื่อสร้างกลุ่มการรับประกัน
1. ในฟิลด์ **ชื่อ** ให้ป้อนชื่อสำหรับกลุ่มใหม่
1. บน FastTab **ทั่วไป** ในฟิลด์ **คำอธิบาย** ให้ป้อนคำอธิบายของกลุ่ม
1. บน FastTab **ผลิตภัณฑ์การรับประกัน** ให้เลือก **เพิ่มบรรทัด** เพื่อเพิ่มสินค้าที่มีการรับประกัน
1. ในฟิลด์ **ลำดับการแสดงผล** ให้ป้อนหมายเลขเพื่อจัดอันดับกลุ่มการรับประกันที่ POS POS จะแสดงสินค้าที่มีการรับประกันตามลำดับจากน้อยไปหามากในพร้อมต์การรับประกัน
1. บน FastTab **ผลิตภัณฑ์ที่สามารถรับประกันได้** ให้เลือก **เพิ่มบรรทัด** เพื่อเพิ่มผลิตภัณฑ์ที่สามารถรับประกันได้
1. ถ้าสินค้าที่มีการรับประกันเกี่ยวข้องกับประเภทสินค้าที่สามารถรับประกันได้ทั้งหมด (ผลิตภัณฑ์) ให้เลือกประเภทในฟิลด์ **ประเภท** ถ้าสินค้าที่มีการรับประกันเกี่ยวข้องกับสินค้าที่สามารถรับประกันได้เฉพาะ (ผลิตภัณฑ์) ให้เลือกผลิตภัณฑ์ในฟิลด์ **ผลิตภัณฑ์**
1. บน FastTab **ช่องทางที่เกี่ยวข้อง** ให้เลือก **เพิ่มบรรทัด** เพื่อเพิ่มช่องทางที่คุณต้องการขายสินค้าที่มีการรับประกัน
1. เลือก **บันทึก** เพื่อบันทึกการตั้งค่าคอนฟิก
1. เลือก **เผยแพร่** เพื่อเผยแพร่กลุ่มการรับประกัน
1. รันงาน **1040** เพื่อซิงค์ข้อมูลไปยังช่องทาง

## <a name="sell-warranty-items-at-the-pos"></a>ขายสินค้าที่มีการรับประกันที่ POS

การดำเนินงานของ POS สองรายการช่วยให้บริษัทผู้ขายสามารถขายสินค้าที่มีการรับประกันได้ในระหว่างเวิร์กโฟลว์สำหรับการซื้อของลูกค้า:

- **เพิ่มการรับประกัน** – การดำเนินงานนี้ทริกเกอร์พร้อมต์ที่แสดงการรับประกันที่เกี่ยวข้องสำหรับสินค้าที่สามารถรับประกันได้ซึ่งถูกเลือกไว้ในรถเข็น
- **เพิ่มการรับประกันไปยังธุรกรรมที่มีอยู่** – การดำเนินงานนี้อนุญาตให้บริษัทผู้ขายสามารถขายการรับประกันสำหรับสินค้าที่สามารถรับประกันได้ที่ถูกขายก่อนหน้านี้ บริษัทผู้ขายสามารถค้นหาธุรกรรมเดิมสำหรับสินค้าที่สามารถรับประกันได้ โดยการป้อนหมายเลขใบเสร็จของธุรกรรม

ภาพประกอบต่อไปนี้แสดงตัวอย่างของหน้าเทอร์มินัล POS ที่มีพร้อมต์เพื่อเพิ่มสินค้าที่มีการรับประกันสำหรับการซื้อสินค้าปัจจุบันของสินค้าที่สามารถรับประกันได้

![ตัวอย่างของพร้อมต์เพื่อเพิ่มสินค้าที่มีการรับประกันสำหรับการซื้อปัจจุบัน](./media/ew-sell-warranty.png)

ภาพประกอบต่อไปนี้แสดงตัวอย่างของคุณลักษณะสำหรับการเพิ่มสินค้าที่มีการรับประกันสำหรับสินค้าที่สามารถรับประกันได้ที่ถูกขายก่อนหน้านี้

![ตัวอย่างของคุณลักษณะสำหรับการเพิ่มสินค้าที่มีการรับประกันสำหรับสินค้าที่สามารถรับประกันได้ที่ถูกขายก่อนหน้านี้](./media/ew-add-warranty-existing.png)

## <a name="process-warranty-transactions"></a>ประมวลผลธุรกรรมการรับประกัน

เมื่อการรับประกันถูกขายในธุรกรรมเงินสดและการขนส่ง หลังจากที่มีการลงรายการบัญชีธุรกรรมใน Commerce headquarters ผู้ใช้ Commerce สามารถรันงาน **ประมวลผลธุรกรรมการรับประกัน** เพื่อประมวลผลธุรกรรมการรับประกัน และสร้างนโยบายการรับประกัน

เมื่อต้องการประมวลผลธุรกรรมการรับประกันใน Commerce headquarters ให้ทำตามขั้นตอนเหล่านี้

1. ไปยัง **Retail และ Commerce \> ผลิตภัณฑ์และประเภท \> การรับประกัน \> ประมวลผลธุรกรรมการรับประกัน**
1. ในกล่องโต้ตอบ **เลือกโหนดขององค์กร** ในฟิลด์ **ลำดับชั้นขององค์กร** ให้เลือกค่า
1. ในรายการ **โหนดขององค์กรที่พร้อมใช้งาน** ให้เลือกร้านค้าแต่ละร้าน หรือถ้าคุณต้องการสร้างชุดงานสำหรับกลุ่มของร้านค้า โหนด
1. เลือกปุ่มลูกศรขวาเพื่อเพิ่มการเลือกของคุณไปยังรายการ **โหนดขององค์กรที่เลือก**
1. เลือกแท็บ **รันในเบื้องหลัง**
1. ตั้งค่าตัวเลือก **การประมวลผลชุดงาน** เป็น **ใช่** แล้วจากนั้น เลือก **การเกิดซ้ำ**
1. ในกล่องโต้ตอบ **กำหนดการเกิดซ้ำ** ในฟิลด์ **วันที่เริ่มต้น** ให้เลือกหรือป้อนวันที่เริ่มต้นสำหรับการเกิดซ้ำ
1. ในฟิลด์ **เวลาเริ่มต้น** ให้เลือกหรือป้อนเวลาเริ่มต้นสำหรับการเกิดซ้ำ
1. ทำตามขั้นตอนเหล่านี้

    - เลือกตัวเลือก **ไม่มีวันที่สิ้นสุด** ถ้าการเกิดซ้ำไม่ควรสิ้นสุด
    - เลือกตัวเลือก **สิ้นสุดหลังจาก** ถ้าการเกิดซ้ำควรสิ้นสุด หลังจากที่มีการรันได้จำนวนหนึ่ง ถ้าคุณเลือกตัวเลือกนี้ ให้ป้อนจำนวนของการรัน
    - เลือกตัวเลือก **สิ้นสุดเมื่อ** ถ้าการเกิดซ้ำควรสิ้นสุดภายในวันที่เฉพาะ ถ้าคุณเลือกตัวเลือกนี้ ให้เลือกหรือป้อนวันที่

1. เลือก **ตกลง**
1. เลือก **ตกลง**

## <a name="warranty-policies"></a>นโยบายการรับประกัน

เมื่อมีการขายการรับประกันแบบขยาย จะมีการสร้างเอนทิตีนโยบายการรับประกันโดยอัตโนมัติ หมายเลขนโยบายการรับประกันสามารถใช้ร่วมกันกับลูกค้า เพื่อให้พวกเขามีการอ้างอิงสำหรับสินค้าที่มีการรับประกันที่พวกเขาซื้อ คุณสมบัติของนโยบายการรับประกันรวมถึงวันที่เริ่มต้นที่มีผลบังคับใช้และวันหมดอายุของการรับประกัน ข้อกำหนดและเงื่อนไข และหมายเลขลำดับประจำสินค้าของสินค้าที่สามารถรับประกันได้ที่มีการขายการรับประกันให้

> [!NOTE]
> จะมีการสร้างคุณสมบัตินโยบายการรับประกันโดยอัตโนมัติ เมื่อมีการสร้างเอนทิตีนโยบายการรับประกัน ในปัจจุบัน จะไม่สามารถถูกตั้งค่าหรือถูกแก้ไขด้วยตนเองได้

ตารางต่อไปนี้จะอธิบายคุณสมบัตินโยบายการรับประกันและค่า ใน Commerce headquarters ตารางฐานข้อมูลจะมีชื่อว่า WARRANTYPOLICY

| ชื่อคุณสมบัติ | มูลค่า | คำอธิบาย |
|---------------|-------|-------------|
| PolicyNumber | สตริงของอักขระ (สูงสุด 20 อักขระ) | หมายเลขนโยบายการรับประกัน |
| WarrantiedItemId | สตริงของอักขระ (สูงสุด 20 อักขระ) | รหัสของสินค้าที่สามารถรับประกันได้ |
| WarrantiedInventoryLotId | สตริงของอักขระ (สูงสุด 20 อักขระ) | รหัสของล็อตสินค้าคงคลังของสินค้าที่สามารถรับประกันได้ |
| WarrantiedSerialNumber | สตริงของอักขระ (สูงสุด 20 อักขระ) | หมายเลขลำดับประจำสินค้าของสินค้าที่สามารถรับประกันได้ |
| WarrantiedFulfilledDate | วันที่ | วันเติมสินค้าของสินค้าที่สามารถรับประกันได้ |
| WarrantyItemId | สตริงของอักขระ (สูงสุด 20 อักขระ) | รหัสของสินค้าที่มีการรับประกัน |
| WarrantyInventoryLotId | สตริงของอักขระ (สูงสุด 20 อักขระ) | รหัสของล็อตสินค้าคงคลังของสินค้าที่มีการรับประกัน |
| WarrantySalesDate | วันที่ | วันที่ขายของสินค้าที่มีการรับประกัน |
| WarrantyEffectiveDate | วันที่ | วันที่มีผลบังคับใช้ของนโยบายการรับประกัน |
| WarrantyExpirationDate | วันที่ | วันหมดอายุของนโยบายการรับประกัน |
| CustAccount | สตริงของอักขระ (สูงสุด 20 อักขระ) | หมายเลขบัญชีลูกค้า |
| สถานะ | **สร้าง** **ยกเลิก** **มีผลบังคับใช้** หรือ **หมดอายุ** | สถานะของนโยบายการรับประกัน |
| บันทึกย่อ | สตริงของอักขระ (สูงสุด 255 อักขระ) | หมายเหตุเกี่ยวกับนโยบายการรับประกัน เช่น ข้อกำหนดและเงื่อนไข |

## <a name="frequently-asked-questions-faq"></a>คำถามที่ถามบ่อย (FAQ)

**เพราะเหตุใดฉันจึงไม่เห็นพร้อมท์การรับประกันใน POS**

ตรวจสอบให้แน่ใจว่าสินค้าที่มีการรับประกันถูกจัดประเภทไปยังช่องทาง นอกจากนี้ โปรดตรวจสอบให้แน่ใจว่ามีการตั้งค่าคอนฟิกกลุ่มการรับประกัน เพื่อให้มีช่องทางที่เกี่ยวข้อง

**เมื่อฉันพยายามเพิ่มการรับประกันไปยังธุรกรรมที่มีอยู่และป้อนหมายเลขใบรับสินค้าตามใบสั่งของลูกค้า ทำไมฉันจึงไม่เห็นสินค้าในบรรทัดธุรกรรมใดๆ**

คุณสามารถค้นหาใบรับสินค้าได้เฉพาะเมื่อมีการรันงานการดึง (งาน P) เพื่ออัพโหลดใบรับสินค้าไปยัง Commerce headquarters เมื่อต้องการรันงาน P ให้ไปที่ **Retail และ Commerce \> Retail และ Commerce IT \> กำหนดการการกระจาย** เลือกงาน **P-0001** และจากนั้น เลือก **เรียกใช้เดี๋ยวนี้**

**ทำไมคุณลักษณะการรับประกันจึงใช้ได้กับผลิตภัณฑ์ที่กำหนดหมายเลขลำดับประจำสินค้าเท่านั้น**

การรับประกันเป็นบริการที่มีให้สำหรับผลิตภัณฑ์เฉพาะที่ไม่ซ้ำกัน ใน Dynamics 365 อาจมีการระบุผลิตภัณฑ์โดยไม่ซ้ำกันโดยหมายเลขลำดับประจำสินค้าเท่านั้น

## <a name="additional-resources"></a>ทรัพยากรเพิ่มเติม

[ตั้งค่าผลิตภัณฑ์ขายปลีก](set-up-retail-products.md)

[ตั้งค่าการจัดประเภท](set-up-assortments.md)

[ภาพรวมของลำดับหมายเลข](../fin-ops-core/fin-ops/organization-administration/number-sequence-overview.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
