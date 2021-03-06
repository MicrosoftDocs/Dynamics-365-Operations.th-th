---
title: จัดการแอททริบิวต์และกลุ่มแอททริบิวต์
description: หัวข้อนี้อธิบายวิธีการใช้แอททริบิวต์ เพื่อช่วยให้มีวิธีในการอธิบายผลิตภัณฑ์และลักษณะผ่านฟิลด์ที่ผู้ใช้กำหนด
author: ashishmsft
manager: AnnBe
ms.date: 04/28/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: EcoResCategoryAttribute, EcoResProductEntityAttributeTableFieldAssociation, EcoResCategorySearchList, EcoResAttribute, COODualUseCategories, EcoResAttributeType, EcoResAttributeValue, EcoResCategoryAttributeGroup, EcoResCategoryFriendlyName
audience: Application User
ms.reviewer: josaw
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail
ms.author: asharchw
ms.search.validFrom: 2018-03-30
ms.dyn365.ops.version: Application pdate 5, AX 8.0
ms.openlocfilehash: 70e2b52dd140660fe98c6ff07248a033ba4bd635
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 01/15/2021
ms.locfileid: "4979984"
---
# <a name="manage-attributes-and-attribute-groups"></a>จัดการแอททริบิวต์และกลุ่มแอททริบิวต์

[!include [banner](includes/banner.md)]

*แอททริบิวต์* จะกำหนดวิธีการอธิบายผลิตภัณฑ์และลักษณะเพิ่มเติมผ่านทางฟิลด์ที่กำหนดโดยผู้ใช้ (เช่น **ขนาดหน่วยความจำ** **กำลังการผลิตฮาร์ดดิสก์** **เป็นความสอดคล้องกันของ Energy star** ฯลฯ) แอททริบิวต์สามารถเชื่อมโยงกับเอนทิตี้ต่าง ๆ ของ Commerce เช่นประเภทผลิตภัณฑ์ และช่องทาง และสามารถตั้งค่าเริ่มต้นสำหรับอุปกรณ์เหล่านี้ จากนั้น ผลิตภัณฑ์จะสืบทอดแอททริบิวต์และค่าเริ่มต้น เมื่อได้ถูกเชื่อมโยงกับประเภทผลิตภัณฑ์และช่องทาง ค่าเริ่มต้นสามารถถูกแทนที่ได้ในระดับผลิตภัณฑ์แต่ละรายการ ที่ระดับช่องทาง หรือในแค็ตตาล็อก


ตัวอย่างเช่น ผลิตภัณฑ์โทรทัศน์ทั่วไปอาจมีแอททริบิวต์ต่อไปนี้

| ประเภท   | ลักษณะเฉพาะ                | ค่าที่ได้รับอนุญาต          | ค่าเริ่มต้น |
|------------|--------------------------|-----------------------------|---------------|
| โทรทัศน์ & วิดีโอ | ยี่ห้อ                    | ค่ายี่ห้อที่ถูกต้องใดๆ       | None          |
| โทรทัศน์         | ขนาดหน้าจอ              | 20–80 นิ้ว                | None          |
|            | vertical solution / ชุดซอฟต์แวร์ในแนวตั้ง      | 480i, 720p, 1080iหรือ 1080p | 1080p         |
|            | อัตราการรีเฟรชหน้าจอ      | 60 เฮิรตซ์, 120 เฮิรตซ์หรือ 240 เฮิรตซ์       | 60 เฮิรตซ์          |
|            | อินพุต HDMI              | 0–10                        | 3             |
|            | อินพุต DVI               | 0–10                        | 1             |
|            | ข้อมูลโดยรวม         | 0–10                        | 2             |
|            | อินพุตส่วนประกอบ         | 0–10                        | 1             |
| LCD        | 3D พร้อมแล้ว                 | ใช่ หรือ ไม่ใช่                   | ใช่           |
|            | 3D เปิดใช้งาน               | ใช่ หรือ ไม่ใช่                   | หมายเลข            |
| พลาสมา     | การดำเนินงานชั่วคราวจาก      | 32–110 ระดับการศึกษา              | 32            |
|            | การดำเนินงานชั่วคราวไปที่        | 32–110 ระดับการศึกษา              | 100           |
| โปรเจคชัน | การรับประกันท่อโปรเจคชัน | 6, 12หรือ 18 เดือน         | 12            |
|            | \# ของท่อโปรเจคชัน   | 1–5                         | 3             |

## <a name="attributes-and-attribute-types"></a>แอททริบิวต์และชนิดแอททริบิวต์

แอททริบิวต์จะขึ้นอยู่กับ *ชนิดแอททริบิวต์* ชนิดของแอททริบิวต์จะระบุชนิดของข้อมูลที่สามารถป้อนให้กับแอททริบิวต์เฉพาะ  ชนิดแอททริบิวต์ที่สนับสนุนมีดังต่อไปนี้:

- **สกุลเงิน** – ชนิดนี้สนับสนุนค่าสกุลเงิน ซึ่งสามารถถูกกำหนดขอบเขต (นั่นคือ สามารถสนับสนุนช่วงของค่า) หรือสามารถเปิดทิ้งไว้ได้
- **วันที่และเวลา** – ชนิดนี้สนับสนุนค่าวันที่และเวลา ซึ่งสามารถถูกกำหนดขอบเขตหรือเปิดทิ้งไว้ได้
- **ทศนิยม** – ชนิดนี้สนับสนุนค่าตัวเลขที่รวมถึงตำแหน่งทศนิยม นอกจากนี้ ยังสนับสนุนหน่วยวัดอีกด้วย ซึ่งสามารถถูกกำหนดขอบเขตหรือเปิดทิ้งไว้ได้
- **เลขจำนวนเต็ม** – ชนิดนี้สนับสนุนค่าตัวเลข นอกจากนี้ ยังสนับสนุนหน่วยวัดอีกด้วย ซึ่งสามารถถูกกำหนดขอบเขตหรือเปิดทิ้งไว้ได้
- **ข้อความ** – ชนิดนี้สนับสนุนค่าข้อความ ซึ่งสนับสนุนชุดที่กำหนดไว้ล่วงหน้าของค่าที่เป็นไปได้ (ซึ่งคือ *การแจงนับ*)
- **บูลีน** – ชนิดนี้สนับสนุนค่าไบนารี (**จริง** หรือ **เท็จ**)
- **การอ้างอิง** – ชนิดนี้อ้างอิงแอททริบิวต์อื่นๆ

### <a name="set-up-attribute-types"></a>ตั้งค่าชนิดของแอททริบิวต์

1. ลงชื่อเข้าใช้ไคลเอนต์ฝ่ายสนับสนุนเป็นผู้จัดการฝ่ายจัดซื้อสินค้า
2. ไปที่ **การจัดการข้อมูลผลิตภัณฑ์** &gt; **การตั้งค่า** &gt; **ประเภทและแอททริบิวต์** &gt; **ชนิดแอททริบิวต์**
3. สร้างชนิดแอททริบิวต์สองชนิดของชนิด **ข้อความ** ตั้งค่าตัวเลือก **รายการคงที่** เป็น **ใช่** แล้วเพิ่มรายการของค่า:

    - ตั้งชื่อชนิดแอททริบิวต์หนึ่งชนิด **รูปร่างเลนส์** และเพิ่มค่าต่อไปนี้: **วงรี** **สี่เหลี่ยม** และ **สามเหลี่ยม**
    - ตั้งชื่อชนิดแอททริบิวต์อื่นๆ **แบรนด์แว่นกันแดด** และเพิ่มค่าต่อไปนี้: **Ray ban** **Aviator** และ **Oakley**

![ชนิดแอททริบิวต์](media/AttributeType.png)

### <a name="set-up-an-attribute"></a>ตั้งค่าแอททริบิวต์

1. ลงชื่อเข้าใช้ไคลเอนต์ฝ่ายสนับสนุนเป็นผู้จัดการฝ่ายจัดซื้อสินค้า
2. ไปที่ **การจัดการข้อมูลผลิตภัณฑ์** &gt; **การตั้งค่า** &gt; **ประเภทและแอททริบิวต์** &gt; **แอททริบิวต์**
3. สร้างแอททริบิวต์ที่มีชื่อว่า **เลนส์**
4. ตั้งค่าฟิลด์ **ชนิดแอตทริบิวต์** เป็น **รูปร่างเลนส์**

![ลักษณะเฉพาะ](media/Attribute.png)

## <a name="attribute-metadata"></a>ข้อมูลเมตาของแอททริบิวต์

*ข้อมูลเมตาของแอททริบิวต์* อนุญาตให้คุณเลือกตัวเลือกเพื่อระบุว่า แอททริบิวต์สำหรับผลิตภัณฑ์แต่ละรายการควรทำงานอย่างไร ตัวอย่างเช่น คุณสามารถระบุว่าแอททริบิวต์จำเป็นหรือไม่ สามารถใช้สำหรับการค้นหาได้หรือไม่ และสามารถใช้เป็นตัวกรองข้อมูลได้หรือไม่

สำหรับผลิตภัณฑ์ การตั้งค่าข้อมูลเมตาของแอททริบิวต์สามารถถูกแทนที่ได้ที่ระดับช่องทาง ความสามารถนี้จะถูกกล่าวถึงในหัวข้อนี้ในภายหลัง

ตามที่คุณอาจสังเกตเห็น หน้า **แอททริบิวต์** ประกอบด้วยตัวเลือกที่เกี่ยวข้องกับข้อมูลเมตาของแอททริบิวต์ ภายใต้ **ข้อมูลเมตาของแอททริบิวต์สำหรับ POS** ตัวเลือกหนึ่งตัวเลือกที่ชื่อ **สามารถถูกจำกัดได้** มีผลต่อลักษณะการทำงานของค่าแอททริบิวต์ในการขายหน้าร้าน (POS) หรือวิธีที่ระบบจัดการกับค่าแอททริบิวต์เหล่านั้น เฉพาะแอททริบิวต์สำหรับรายการซึ่งคุณอาจตั้งค่าตัวเลือก **สามารถถูกจำกัดได้** เป็น **ใช่** จะแสดงขึ้นสำหรับการปรับปรุง หรือการกรองข้อมูลของผลิตภัณฑ์ใน POS ได้

ต่อไปนี้เป็นตัวเลือกข้อมูลเมตาของแอททริบิวต์ที่เหลือในหน้า **แอททริบิวต์** :

- สามารถค้นหาได้
- สามารถดึงข้อมูลได้
- สามารถสอบถามได้
- สามารถเรียงลำดับได้
- อนุญาตให้ใช้หลายค่า
- ละเว้นตัวพิมพ์และรูปแบบ
- การจับคู่เสร็จสมบูรณ์

ในตอนแรก ตัวเลือกเหล่านี้มีเป้าหมายเพื่อปรับปรุงฟังก์ชันการค้นหาสำหรับ storefront ออนไลน์ ถึงแม้ว่า Commerce ไม่มีหน้าร้านออนไลน์แบบใช้ได้ทันทีมาให้ แต่ยังมีชุดเครื่องมือพัฒนาซอฟต์แวร์การเผยแพร่ (SDK) ของ eCommerce ให้ใช้งาน ลูกค้าสามารถใช้ SDK นี้เพื่อใส่ผลิตภัณฑ์ลงในดัชนีการค้นหาที่พวกเขาเลือก ถึงแม้ว่าจะมีการนำเข้าข้อมูลผลิตภัณฑ์ ลูกค้ายังควรสามารถแยกแยะข้อมูลที่สามารถค้นหาได้ ข้อมูลที่สามารถสอบถามได้ และอื่นๆ ในวิธีนั้น พวกเขาสามารถสร้างดัชนีที่ดีที่สุดเพื่อให้แน่ใจว่า พวกเขาจัดดัชนีเฉพาะแอททริบิวต์ที่ *ในความคิดเห็นของพวกเขา* ควรจะถูกจัดทำดัชนี

สำหรับข้อมูลเพิ่มเติมเกี่ยวกับวัตถุประสงค์ของตัวเลือกที่เหลือเหล่านี้ ดู [ภาพรวมของ Schema การค้นหาในเซิร์ฟเวอร์ SharePoint 2013](https://technet.microsoft.com/library/jj219669.aspx)

## <a name="filter-settings-for-attributes"></a>การตั้งค่าตัวกรองสำหรับแอททริบิวต์

การตั้งค่าตัวกรองสำหรับแอททริบิวต์ช่วยให้คุณสามารถกำหนดวิธีการแสดงตัวกรองสำหรับแอททริบิวต์ใน POS ในการเข้าถึงการตั้งค่าตัวกรองสำหรับแอททริบิวต์ บนเพจ **แอททริบิวต์** เลือกแอททริบิวต์ และจากนั้น บนบานหน้าต่างการดำเนินการ เลือก **การตั้งค่าตัวกรอง**

หน้า **การกำหนดลักษณะการแสดงผลตัวกรอง** รวมฟิลด์ต่อไปนี้:

- **ชื่อ** – ตามค่าเริ่มต้น ฟิลด์นี้ถูกกำหนดเป็นชื่อของแอททริบิวต์ อย่างไรก็ตาม คุณสามารถเปลี่ยนค่าได้
- **ตัวเลือกการแสดงผล** – ตัวเลือกต่อไปนี้พร้อมใช้งาน:

    - **ค่าเดี่ยว** – ตัวเลือกนี้จะพร้อมใช้งานสำหรับชนิดแอททริบิวต์ต่อไปนี้: **บูลีน** **สกุลเงิน** **ทศนิยม** **จำนวนเต็ม** และ **ข้อความ** ตัวเลือกนี้เปิดใช้งานการเลือกค่าเดียวสำหรับแอททริบิวต์เหล่านี้ในไคลเอนต์สำหรับการปรับปรุง
    - **ค่าที่หลากหลาย** – ตัวเลือกนี้จะพร้อมใช้งานสำหรับชนิดแอททริบิวต์ต่อไปนี้: **สกุลเงิน** **ทศนิยม** **จำนวนเต็ม** และ **ข้อความ** ตัวเลือกนี้เปิดใช้งานการเลือกค่าที่หลากหลายสำหรับแอททริบิวต์นี้ในไคลเอนต์สำหรับการปรับปรุง

- **การควบคุมการแสดงผล** – ตัวเลือกต่อไปนี้พร้อมใช้งาน:

    - **รายการ** – ตัวเลือกนี้จะพร้อมใช้งานสำหรับชนิดแอททริบิวต์ทั้งหมด
    - **ช่วง** – ตัวเลือกนี้จะพร้อมใช้งานสำหรับชนิดแอททริบิวต์ต่อไปนี้: **สกุลเงิน** **ทศนิยม** และ **จำนวนเต็ม**
    - **ตัวเลื่อน** – ตัวเลือกนี้จะพร้อมใช้งานสำหรับชนิดแอททริบิวต์ต่อไปนี้: **สกุลเงิน** **ทศนิยม** และ **จำนวนเต็ม**
    - **ตัวเลื่อนที่มีแถบ** – ตัวเลือกนี้จะพร้อมใช้งานสำหรับชนิดแอททริบิวต์ต่อไปนี้: **สกุลเงิน** **ทศนิยม** และ **จำนวนเต็ม**

- **ค่าขีดจำกัด** – การตั้งค่านี้จำเป็น ถ้าคุณเลือก **ช่วง** เป็นชนิดการควบคุมการแสดงผล คุณสามารถกำหนดค่าได้โดยใช้เครื่องหมายอัฒภาค (;) เป็นตัวกำหนดเขต

    ตัวอย่างเช่น สำหรับตัวกรองเช่น **ปริมาตรถุง** ค่าขีดจำกัดอาจเป็น **10; 20; 50; 100; 200; 500; 1000; 5000** ในกรณีนี้ POS จะแสดงช่วงต่อไปนี้ ช่วงใดๆ ที่ไม่มีผลิตภัณฑ์ใดๆ ในผลลัพธ์ ชุดจะปรากฏเป็นจางลง

    - น้อยกว่า 10
    - 10 – 20
    - 20 – 50
    - 50 – 100
    - 100 – 200
    - 200 – 500
    - 500 ครั้งขึ้นไป

![การตั้งค่าตัวกรองแอททริบิวต์](media/AttributeFilterSettings.PNG)

## <a name="attribute-groups"></a>กลุ่มแอททริบิวต์

หลังจากที่มีการกำหนดแอททริบิวต์ จะสามารถถูกกำหนดให้กลุ่มแอททริบิวต์ได้ *กลุ่มแอททริบิวต์* ถูกใช้เพื่อจัดกลุ่มแอททริบิวต์แต่ละรายการสำหรับส่วนประกอบหรือส่วนประกอบย่อยในแบบจำลองการจัดโครงแบบผลิตภัณฑ์ คุณสามารถใส่แอททริบิวต์ในกลุ่มของแอททริบิวต์มากกว่าหนึ่งกลุ่มได้ กลุ่มแอททริบิวต์สามารถช่วยให้ผู้ใช้สามารถจัดโครงแบบผลิตภัณฑ์ได้ เนื่องจากการเลือกต่างๆ จะถูกจัดเรียงอยู่ในบริบทเฉพาะเจาะจง คุณสามารถกำหนดกลุ่มของแอททริบิวต์ให้กับประเภทหรือช่องทางได้

คุณยังสามารถตั้งค่าเริ่มต้นสำหรับแอตทริบิวต์ที่รวมอยู่ในกลุ่มแอททริบิวต์ได้ด้วย ตัวอย่างเช่น คุณเพิ่มแอททริบิวต์สำหรับสีไปยังกลุ่มแอททริบิวต์ และเลือก **สีน้ำเงิน** เป็นค่าแอททริบิวต์เริ่มต้น ในกรณีนี้ เมื่อกลุ่มแอททริบิวต์ถูกเพิ่มไปยังผลิตภัณฑ์ที่มีสีเป็นหนึ่งในแอททริบิวต์ **สีน้ำเงิน** จะปรากฏเป็นสีเริ่มต้นสำหรับผลิตภัณฑ์นั้น

![กลุ่มแอททริบิวต์](media/AttributeGroup.png)

### <a name="create-an-attribute-group"></a>สร้างกลุ่มแอททริบิวต์

1. ลงชื่อเข้าใช้ไคลเอนต์ฝ่ายสนับสนุนเป็นผู้จัดการฝ่ายจัดซื้อสินค้า
2. ไปที่ **การจัดการข้อมูลผลิตภัณฑ์** &gt; **การตั้งค่า** &gt; **ประเภทและแอททริบิวต์** &gt; **กลุ่มแอททริบิวต์**
3. สร้างกลุ่มแอททริบิวต์ที่มีชื่อว่า **แว่นกันแดดแฟชั่น**
4. เพิ่มแอททริบิวต์ต่อไปนี้: **รูปร่างเลนส์** และ **แบรนด์แว่นกันแดด**

### <a name="assign-attribute-groups-to-categories"></a>กำหนดกลุ่มแอททริบิวต์ให้กับประเภท

กลุ่มแอททริบิวต์หนึ่งรายการขึ้นไปสามารถเชื่อมโยงกับโหนดประเภทในชนิดต่อไปนี้ของลำดับชั้นประเภท: ลำดับชั้นของผลิตภัณฑ์การค้า ลำดับชั้นประเภทการนำทางช่องทาง และลำดับชั้นประเภทผลิตภัณฑ์เพิ่มเติม จากนั้น เมื่อมีการจัดประเภทผลิตภัณฑ์ จะสืบทอดแอททริบิวต์ที่รวมอยู่ในกลุ่มแอททริบิวต์

![ลำดับชั้นของผลิตภัณฑ์ – กลุ่มแอททริบิวต์ผลิตภัณฑ์](media/AGRetailProdHierarchy.PNG)

ทำตามขั้นตอนเหล่านี้เพื่อกำหนดกลุ่มแอททริบิวต์ให้กับประเภทในลำดับชั้นของผลิตภัณฑ์การค้า

1. ลงชื่อเข้าใช้ไคลเอนต์ฝ่ายสนับสนุนเป็นผู้จัดการฝ่ายจัดซื้อสินค้า
2. ไปยัง **Retail และ Commerce** &gt; **การจัดการประเภทและผลิตภัณฑ์** &gt; **ลำดับชั้นของผลิตภัณฑ์การค้า**
3. เลือก **ลำดับชั้นการนำทางแฟชั่น**
4. ภายใต้ **Menswear** เลือกประเภท **Pants** และจากนั้นบน FastTab **กลุ่มแอททริบิวต์ผลิตภัณฑ์** เพิ่มกลุ่มที่มีแอททริบิวต์ที่ชื่อ **เข็มขัดของผู้ชาย**
5. เลือกประเภท **แว่นกันแดดแฟชั่น** และตรวจสอบแอททริบิวต์ใหม่ในกลุ่มแอททริบิวต์ **แว่นกันแดดแฟชั่น** โดยการเลือก **ดูแอททริบิวต์**

    กลุ่มแอททริบิวต์ควรแสดง **รูปร่างเลนส์** ใหม่ และแอตทริบิวต์ **แบรนด์แว่นกันแดด**

6. ภายใต้ **Menswear** เลือกประเภท **กางเกง** และตรวจสอบแอททริบิวต์สำหรับกลุ่มแอททริบิวต์ **เข็มขัดของผู้ชาย** โดยการเลือก **ดูแอททริบิวต์**

    กลุ่มแอททริบิวต์ควรแสดงแอตทริบิวต์ของ **แบรนด์เข็มขัดของผู้ชาย** **เนื้อผ้าของเข็มขัด** และ **ขนาดเข็มขัด**

> [!NOTE]
> ยังสามารถใช้กระบวนงานนี้เพื่อกำหนดกลุ่มแอททริบิวต์ให้กับประเภทในลำดับชั้นประเภทการนำทางของช่อง และลำดับชั้นประเภทผลิตภัณฑ์เพิ่มเติมได้อีกด้วย ในขั้นตอนที่ 2 ใช้พาธการนำทางต่อไปนี้:
>
> - Retail และ Commerce &gt; การจัดการประเภทและผลิตภัณฑ์ &gt; ประเภทการนำทางช่องทาง
> - Retail และ Commerce &gt; การจัดการประเภทและผลิตภัณฑ์ &gt; ประเภทของผลิตภัณฑ์เพิ่มเติม

### <a name="assign-attribute-groups-to-stores"></a>กำหนดกลุ่มแอททริบิวต์ให้กับร้าน

กลุ่มแอททริบิวต์หนึ่งกลุ่มขึ้นไป สามารถถูกเชื่อมโยงกับร้านค้าหนึ่งร้านขึ้นไปได้ในลำดับชั้นของร้านค้า จากนั้น เมื่อผลิตภัณฑ์ถูกทำให้สมบูรณ์สำหรับร้านค้าเฉพาะ จะมีการสืบทอดแอททริบิวต์ที่รวมอยู่ในกลุ่มแอททริบิวต์

1. ลงชื่อเข้าใช้ไคลเอนต์ฝ่ายสนับสนุนเป็นผู้จัดการฝ่ายจัดซื้อสินค้า
2. ไปยัง **Retail และ Commerce** &gt; **การตั้งค่าช่องทาง** &gt; **ประเภทช่องทางและคุณลักษณะของผลิตภัณฑ์**
3. กำหนดกลุ่มแอททริบิวต์ไปยังช่อง Houston:

    1. เลือกช่อง **Houston**
    2. บน FastTab **กลุ่มแอททริบิวต์** เลือก **เพิ่ม** และจากนั้น ในฟิลด์ **ชื่อ** เลือก **SharePointProvisionedProductAttributeGroup**
    3. เลือก **เพิ่ม** อีกครั้ง และจากนั้น ในฟิลด์ **ชื่อ** เลือก **เข็มขัดของผู้ชาย**
    4. เลือก **เพิ่ม** อีกครั้ง และจากนั้น ในฟิลด์ **ชื่อ** เลือก **แว่นกันแดดแฟชั่น**

        > [!NOTE]
        > ตัวเลือกช่วยให้คุณสามารถระบุว่า ช่องทางนี้ควรสืบทอดกลุ่มแอททริบิวต์จากช่องทางของข้อมูลหลักในลำดับชั้น ถ้าคุณตั้งค่าตัวเลือก **สืบทอด** เป็น **ใช่** โหนดช่องสัญญาณรองจะสืบทอดกลุ่มแอททริบิวต์ทั้งหมด และแอททริบิวต์ในกลุ่มแอททริบิวต์เหล่านั้น

4. เปิดใช้งานแอททริบิวต์เพื่อให้พร้อมใช้งานในช่อง Houston:

    1. ในบานหน้าต่างการดำเนินการ เลือก **ตั้งค่าข้อมูลเมตาของแอททริบิวต์**
    2. เลือกโหนดประเภท **แฟชั่น** และจากนั้น บน FastTab **คุณลักษณะของผลิตภัณฑ์ในช่องทาง** เลือก **รวมแอททริบิวต์** สำหรับแต่ละแอตทริบิวต์
    3. เลือกโหนดประเภท **เครื่องประดับแฟชั่น** เลือกประเภท **แว่นกันแดดแฟชั่น** และจากนั้น บน FastTab **คุณลักษณะของผลิตภัณฑ์ในช่องทาง** เลือก **รวมแอททริบิวต์** สำหรับแต่ละแอตทริบิวต์
    4. เลือกโหนดประเภท **Menswear** เลือกประเภท **กางเกง** และจากนั้น บน FastTab **คุณลักษณะของผลิตภัณฑ์ในช่องทาง** เลือก **รวมแอททริบิวต์** สำหรับแต่ละแอตทริบิวต์

![ประเภทช่องทางและคุณลักษณะของผลิตภัณฑ์ – กลุ่มแอตทริบิวต์](media/CCPAttrGrp.png)

## <a name="overriding-attribute-values"></a>ค่าแอททริบิวต์ที่แทนที่

สามารถแทนที่ค่าเริ่มต้นของแอททริบิวต์สำหรับผลิตภัณฑ์แต่ละรายการที่ระดับผลิตภัณฑ์ได้ นอกจากนี้ ยังสามารถแทนค่าเริ่มต้นสำหรับผลิตภัณฑ์แต่ละรายการในแค็ตตาล็อกเฉพาะ ซึ่งถูกกำหนดเป้าหมายที่ช่องทางเฉพาะได้

### <a name="override-the-attribute-values-of-an-individual-product"></a>แทนที่ค่าแอททริบิวต์ของผลิตภัณฑ์แต่ละผลิตภัณฑ์

1. ลงชื่อเข้าใช้ไคลเอนต์ฝ่ายสนับสนุนเป็นผู้จัดการฝ่ายจัดซื้อสินค้า
2. ไปยัง **Retail และ Commerce** &gt; **การจัดการประเภทและผลิตภัณฑ์** &gt; **ผลิตภัณฑ์ที่นำออกใช้ตามประเภท**
3. เลือกโหนดประเภท **แฟชั่น** &gt; **เครื่องประดับแฟชั่น** &gt; **แว่นกันแดดแฟชั่น**
4. เลือกผลิตภัณฑ์จำเป็นในกริด จากนั้น บนบานหน้าต่างการดำเนินการ บนแท็บ **ผลิตภัณฑ์** ในกลุ่ม **การตั้งค่า** ให้เลือก **คุณลักษณะของผลิตภัณฑ์**
5. เลือกแอททริบิวต์ในบานหน้าต่างด้านซ้าย และจากนั้น ปรับปรุงค่าในบานหน้าต่างด้านขวา

![หน้ารายละเอียดผลิตภัณฑ์ – กลุ่มคุณลักษณะของผลิตภัณฑ์](media/ProdDetailsProdAttrValues.png)

### <a name="override-the-attribute-values-of-products-in-a-catalog"></a>แทนที่ค่าแอททริบิวต์ของผลิตภัณฑ์ในแค็ตตาล็อก

1. ลงชื่อเข้าใช้ไคลเอนต์ฝ่ายสนับสนุนเป็นผู้จัดการฝ่ายจัดซื้อสินค้า
2. ไปยัง **Retail และ Commerce** &gt; **การจัดการแค็ตตาล็อก** &gt; **แค็ตตาล็อกทั้งหมด**
3. เลือกแค็ตตาล็อก **แค็ตตาล็อกฐานของ Fabrikam**
4. เลือกโหนดประเภท **แฟชั่น** &gt; **เครื่องประดับแฟชั่น** &gt; **แว่นกันแดดแฟชั่น**
5. บน FastTab **ผลิตภัณฑ์** เลือกผลิตภัณฑ์ที่จำเป็น และจากนั้นเลือก **แอททริบิวต์** เหนือกริดของผลิตภัณฑ์
6. บน FastTab ต่อไปนี้ อัพเดตค่าของแอททริบิวต์ที่จำเป็น:

    - สื่อผลิตภัณฑ์ที่ใช้ร่วมกัน
    - แอททริบิวต์ผลิตภัณฑ์ที่ใช้ร่วมกัน
    - สื่อที่เป็นช่องทาง
    - แอททริบิวต์ผลิตภัณฑ์ในช่องทาง

    > [!NOTE]
    > ถ้ามีการสร้างสื่อผลิตภัณฑ์ที่ใช้ร่วมกัน และคุณลักษณะของผลิตภัณฑ์ที่ใช้ร่วมกัน จะมีการนำไปใช้กับผลิตภัณฑ์ทั้งหมด

![กลุ่มคุณลักษณะของผลิตภัณฑ์ในแค็ตตาล็อก](media/CatalogProdAttrValues.png)

### <a name="override-the-attribute-values-of-products-in-a-channel"></a>แทนที่ค่าแอททริบิวต์ของผลิตภัณฑ์ในช่องทาง

1. ลงชื่อเข้าใช้ไคลเอนต์ฝ่ายสนับสนุนเป็นผู้จัดการฝ่ายจัดซื้อสินค้า
2. ไปยัง **Retail และ Commerce** &gt; **การตั้งค่าช่องทาง** &gt; **ประเภทช่องทางและคุณลักษณะของผลิตภัณฑ์**
3. เลือกช่อง **Houston**
4. บน FastTab **ผลิตภัณฑ์** เลือกผลิตภัณฑ์ที่จำเป็น และจากนั้นเลือก **แอททริบิวต์** เหนือกริดของผลิตภัณฑ์

    > [!NOTE]
    > ถ้าไม่มีผลิตภัณฑ์ที่พร้อมใช้งาน เพิ่มผลิตภัณฑ์โดยการเลือก  **เพิ่ม** บน FastTab **ผลิตภัณฑ์** และจากนั้นเลือกผลิตภัณฑ์ที่จำเป็นในกล่องโต้ตอบ **เพิ่มผลิตภัณฑ์**

5. บน FastTab ต่อไปนี้ อัพเดตค่าของแอททริบิวต์ที่จำเป็น:

    - สื่อผลิตภัณฑ์ที่ใช้ร่วมกัน
    - แอททริบิวต์ผลิตภัณฑ์ที่ใช้ร่วมกัน
    - สื่อที่เป็นช่องทาง
    - แอททริบิวต์ผลิตภัณฑ์ในช่องทาง

    > [!NOTE]
    > ถ้ามีการสร้างสื่อผลิตภัณฑ์ที่ใช้ร่วมกัน และคุณลักษณะของผลิตภัณฑ์ที่ใช้ร่วมกัน จะมีการนำไปใช้กับผลิตภัณฑ์ทั้งหมด
