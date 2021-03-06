---
title: การค้นหาแอททริบิวต์ด้านวิศวกรรมและแอททริบิวต์ของวิศวกรรม
description: หัวข้อนี้อธิบายวิธีการที่คุณสามารถใช้แอททริบิวต์วิศวกรรมเพื่อระบุลักษณะที่ไม่ใช่มาตรฐานทั้งหมด เพื่อให้แน่ใจว่าข้อมูลของผลิตภัณฑ์หลักทั้งหมดสามารถลงทะเบียนในระบบได้ นอกจากนี้ ยังอธิบายถึงวิธีการที่คุณสามารถใช้การค้นหาแอททริบิวต์ของวิศวกรรมเพื่อค้นหาผลิตภัณฑ์ได้อย่างง่ายดาย โดยยึดตามลักษณะที่มีการลงทะเบียนเหล่านั้น
author: t-benebo
manager: tfehr
ms.date: 09/28/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EngChgProductAttributeSearch, EngChgMaintainAttributeInheritance, EngChgAttribute
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2020-09-28
ms.dyn365.ops.version: Release 10.0.15
ms.openlocfilehash: 32cd2c6d0915df1e48973a22a7d391eb8d62a072
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 01/15/2021
ms.locfileid: "4963699"
---
# <a name="engineering-attributes-and-engineering-attribute-search"></a>การค้นหาแอททริบิวต์ด้านวิศวกรรมและแอททริบิวต์ของวิศวกรรม

[!include [banner](../includes/banner.md)]

เพื่อให้แน่ใจว่าข้อมูลของผลิตภัณฑ์หลักทั้งหมดสามารถลงทะเบียนในระบบได้ คุณควรใช้แอททริบิวต์วิศวกรรมเพื่อระบุลักษณะที่ไม่ใช่มาตรฐานทั้งหมด จากนั้น คุณสามารถใช้การค้นหาแอททริบิวต์ของวิศวกรรมเพื่อค้นหาผลิตภัณฑ์ได้อย่างง่ายดาย โดยยึดตามลักษณะที่มีการลงทะเบียนเหล่านั้น

## <a name="engineering-attributes"></a>คุณลักษณะทางวิศวกรรม

โดยทั่วไป ผลิตภัณฑ์วิศวกรรมมีลักษณะและคุณสมบัติหลายอย่างที่คุณต้องบันทึก ถึงแม้ว่าคุณจะสามารถลงทะเบียนบางคุณสมบัติได้โดยใช้ฟิลด์ผลิตภัณฑ์มาตรฐาน คุณยังสามารถสร้างคุณสมบัติทางวิศวกรรมใหม่ได้ตามต้องการ คุณสามารถกำหนด *แอททริบิวต์ด้านวิศวกรรม* ของคุณเอง และทำให้เป็นส่วนหนึ่งของข้อกำหนดผลิตภัณฑ์

### <a name="create-engineering-attributes-and-attribute-types"></a>สร้างแอททริบิวต์ทางวิศวกรรมและชนิดแอททริบิวต์

แอททริบิวต์ของวิศวกรรมแต่ละรายการต้องเป็นของ *ชนิดของแอททริบิวต์* ข้อกำหนดนี้มีอยู่เนื่องจากแอททริบิวต์ของวิศวกรรมแต่ละรายการต้องมี *ชนิดข้อมูล* ซึ่งกำหนดชนิดของค่าที่สามารถจัดเก็บได้ ชนิดของแอททริบิวต์วิศวกรรมอาจเป็นชนิดมาตรฐาน (เช่น ข้อความอิสระ จำนวนเต็ม หรือทศนิยม) หรือชนิดที่กำหนดเอง (เช่น ข้อความที่มีชุดของค่าที่ระบุให้เลือก) คุณสามารถนำชนิดของแอททริบิวต์แต่ละชนิดมาใช้ใหม่ได้โดยใช้แอททริบิวต์ทางวิศวกรรมจำนวนเท่าใดก็ได้

#### <a name="set-up-engineering-attribute-types"></a>ตั้งค่าชนิดของแอททริบิวต์ทางวิศวกรรม

เมื่อต้องการดู สร้าง หรือแก้ไขชนิดของแอททริบิวต์ทางวิศวกรรม ให้ทำตามขั้นตอนต่อไปนี้

1. ไปที่ **การจัดการการเปลี่ยนแปลงวิศวกรรม \> การตั้งค่า \> แอททริบิวต์ \> ชนิดแอททริบิวต์**
1. เลือกชนิดของแอททริบิวต์ที่มีอยู่ในบานหน้าต่างรายการ หรือเลือก **สร้าง** ในบานหน้าต่างการดำเนินการเพื่อสร้างชนิดแอททริบิวต์ใหม่
1. ตั้งค่าฟิลด์เหล่านี้:

    - **ชื่อชนิดของแอททริบิวต์** – ให้ป้อนชื่อสำหรับชนิดของแอททริบิวต์
    - **ชนิด** – เลือกชนิดข้อมูลมาตรฐาน (*สกุลเงิน* *DateTime* *ทศนิยม* *จำนวนเต็ม* *ข้อความ* *บูลีน* หรือ *ข้อมูลอ้างอิง*)
    - **รายการคงที่** – ตัวเลือกนี้จะพร้อมใช้งานเฉพาะเมื่อคุณตั้งค่าฟิลด์ **ชนิด** เป็น *ข้อความ* ตั้งค่าเป็น *ใช่* เพื่อกำหนดค่าเฉพาะสำหรับแอททริบิวต์ของชนิดนี้ ในกรณีนี้ จะมีการสร้างรายการแบบหล่นลง คุณใช้ FastTab **ค่า** เพื่อสร้างค่าที่พร้อมใช้งานสำหรับชนิดของแอททริบิวต์นี้ กำหนดตัวเลือกนี้เป็น *ไม่* เพื่ออนุญาตให้ผู้ใช้ป้อนค่าใดๆ ในกรณีนี้ จะมีการสร้างฟิลด์ป้อนข้อมูล
    - **ช่วงของค่า** – ตัวเลือกนี้จะพร้อมใช้งานเฉพาะเมื่อคุณตั้งค่าฟิลด์ **ชนิด** เป็น *จำนวนเต็ม* *ทศนิยม* หรือ *สกุลเงิน* เท่านั้น ตั้งค่าเป็น *ใช่* เพื่อกำหนดค่าต่ำสุดและสูงสุดที่จะได้รับการยอมรับสำหรับแอททริบิวต์ของชนิดนี้ คุณใช้ FastTab **ช่วง** เพื่อกำหนดค่าต่ำสุดและสูงสุดและ (สำหรับสกุลเงิน) สกุลเงินที่ใช้สำหรับขีดจำกัดที่คุณป้อน กำหนดตัวเลือกนี้เป็น *ไม่* เพื่อยอมรับค่าใดๆ 
    - **หน่วยวัด** – ฟิลด์นี้จะพร้อมใช้งานเฉพาะเมื่อคุณตั้งค่าฟิลด์ **ชนิด** เป็น *จำนวนเต็ม* หรือ *ทศนิยม* เท่านั้น เลือกหน่วยวัดที่จะใช้สำหรับชนิดของแอททริบิวต์นี้ ถ้าไม่ต้องการหน่วย ให้ปล่อยฟิลด์นี้ว่างไว้

#### <a name="set-up-engineering-attributes"></a>ตั้งค่าแอททริบิวต์ทางวิศวกรรม

เมื่อต้องการดู สร้าง หรือแก้ไขแอททริบิวต์ทางวิศวกรรม ให้ทำตามขั้นตอนต่อไปนี้

1. ไปที่ **การจัดการการเปลี่ยนแปลงวิศวกรรม \> การตั้งค่า \> แอททริบิวต์ \> แอททริบิวต์ทางวิศวกรรม**
1. เลือกแอททริบิวต์ที่มีอยู่ในบานหน้าต่างรายการ หรือเลือก **สร้าง** ในบานหน้าต่างการดำเนินการเพื่อสร้างแอททริบิวต์ใหม่
1. ตั้งค่าฟิลด์เหล่านี้:

    - **ชื่อ** – ป้อนชื่อสำหรับแอททริบิวต์ ชื่อนี้จะปรากฏบนหน้า **แอททริบิวต์ทางวิศวกรรม** เท่านั้น ที่อื่นๆ ในระบบ โดยปกติแล้วจะแสดงค่าของฟิลด์ **ชื่อที่จำง่าย** เพื่อระบุแอททริบิวต์
    - **ชนิดแอททริบิวต์** – เลือกชนิดของแอททริบิวต์ที่คุณกำหนดในส่วนก่อนหน้านี้
    - **ชื่อที่จำง่าย** – ป้อนชื่อที่จะระบุแอททริบิวต์ในระบบ (ยกเว้นบนหน้า **แอททริบิวต์ทางวิศวกรรม**) 
    - **คำอธิบาย** – ป้อนคำอธิบายของแอททริบิวต์
    - **ข้อความวิธีใช้** – ป้อนข้อความวิธีใช้ที่จะบอกผู้ใช้คนอื่นว่าแอททริบิวต์นี้ใช้สำหรับอะไร
    - **ค่าเริ่มต้น** – ป้อนค่าเริ่มต้นสำหรับแอททริบิวต์ ตัวเลือกที่แสดงอยู่จะขึ้นอยู่กับชนิดของแอททริบิวต์ที่คุณเลือกไว้
    - **สกุลเงิน** – ถ้าชนิดของแอททริบิวต์ที่คุณเลือกเป็นสกุลเงิน ให้เลือกสกุลเงินที่แอททริบิวต์จะยอมรับและแสดงค่าในนั้น

1. ถ้าชนิดของแอททริบิวต์ที่คุณเลือกเป็นจำนวนเต็มหรือทศนิยม FastTab **ช่วง** จะแสดงขึ้น บน FastTab นี้ ตั้งค่าฟิลด์ต่อไปนี้ตามต้องการ:

    - **การดำเนินการค่าเผื่อ** – เลือกวิธีการที่ระบบควรตอบสนอง ถ้าผู้ใช้ป้อนค่าภายนอกช่วงที่ระบุ ถ้าคุณเลือก *คำเตือน* คำเตือนจะแสดงขึ้น แต่ผู้ใช้สามารถบันทึกค่าได้ ถ้าคุณเลือก *ไม่อนุญาต* คำเตือนจะแสดงขึ้น และจะไม่สามารถบันทึกค่าได้จนกว่าผู้ใช้จะแก้ไข
    - **ต่ำสุด** – ป้อนค่าต่ำสุดที่แนะนำหรือที่ยอมรับ
    - **สูงสุด** – ป้อนค่าสูงสุดที่แนะนำหรือที่ยอมรับ

### <a name="connect-engineering-attributes-to-an-engineering-product-category"></a>เชื่อมต่อแอททริบิวต์วิศวกรรมกับประเภทผลิตภัณฑ์วิศวกรรม

แอททริบิวต์ทางวิศวกรรมบางอย่างใช้กับผลิตภัณฑ์ทั้งหมด ในขณะที่แอททริบิวต์ทางวิศวกรรมอื่นเฉพาะเจาะจงสำหรับผลิตภัณฑ์แต่ละรายการหรือผลิตภัณฑ์แต่ละประเภท ตัวอย่างเช่น ไม่จำเป็นต้องใช้แอททริบิวต์ไฟฟ้าสำหรับผลิตภัณฑ์เครื่องกล ดังนั้น คุณจึงสามารถตั้งค่า *ประเภทผลิตภัณฑ์วิศวกรรม* ประเภทผลิตภัณฑ์วิศวกรรมสร้างคอลเลกชันของแอททริบิวต์ทางวิศวกรรมที่ต้องเป็นส่วนหนึ่งของคำนิยามสำหรับผลิตภัณฑ์ที่เป็นของประเภทนั้น นอกจากนี้ คุณยังสามารถระบุว่าแอททริบิวต์ด้านวิศวกรรมใดเป็นข้อมูลบังคับ และมีค่าเริ่มต้นหรือไม่

สำหรับข้อมูลเพิ่มเติมเกี่ยวกับวิธีการทำงานกับประเภทผลิตภัณฑ์วิศวกรรม ซึ่งรวมถึงข้อมูลเกี่ยวกับวิธีการเชื่อมต่อแอททริบิวต์เข้ากับประเภท โปรดดู [รุ่นวิศวกรรมและประเภทผลิตภัณฑ์วิศวกรรม ](engineering-versions-product-category.md)

### <a name="set-values-for-engineering-attributes"></a>ตั้งค่าสำหรับแอททริบิวต์วิศวกรรม

แอททริบิวต์วิศวกรรมที่เชื่อมโยงกับประเภทของผลิตภัณฑ์วิศวกรรมจะแสดงขึ้น เมื่อคุณสร้างผลิตภัณฑ์วิศวกรรมใหม่ที่ยึดตามประเภทนั้น คุณสามารถตั้งค่าสำหรับแอททริบิวต์ได้ในขณะนั้น หลังจากนั้น ค่าเหล่านั้นสามารถเปลี่ยนแปลงได้ในหน้า **รุ่นวิศวกรรม** หรือเป็นส่วนหนึ่งของการจัดการการเปลี่ยนแปลงทางวิศวกรรมในใบสั่งเปลี่ยนแปลงทางวิศวกรรม สำหรับข้อมูลเพิ่มเติม ให้ดูที่ [จัดการการเปลี่ยนแปลงที่เกิดขึ้นกับผลิตภัณฑ์วิศวกรรม](engineering-change-management.md)

### <a name="create-an-engineering-product"></a>สร้างผลิตภัณฑ์วิศวกรรม

เมื่อต้องการสร้างผลิตภัณฑ์วิศวกรรม ให้เปิดหน้า **ผลิตภัณฑ์ที่นำออกใช้** จากนั้น บนบานหน้าต่างการดำเนินการ บนแท็บ **ผลิตภัณฑ์** ในกลุ่ม **สร้าง** ให้เลือก **ผลิตภัณฑ์วิศวกรรม**

คุณต้องระบุประเภทวิศวกรรมที่ผลิตภัณฑ์เป็นสมาชิกอยู่ ประเภทจะกำหนดค่าเริ่มต้นและลักษณะทั้งหมดสำหรับผลิตภัณฑ์ นอกจากนี้ ยังจะตั้งค่าแอททริบิวต์ที่สามารถใช้ได้กับผลิตภัณฑ์ด้วย หลังจากที่เลือกประเภทแล้ว ค่าจะถูกตั้งค่าสำหรับแอททริบิวต์ จากนั้น คุณจะสามารถแก้ไขค่าเหล่านั้นได้

## <a name="search-for-products-by-using-engineering-attribute-values"></a>ค้นหาผลิตภัณฑ์โดยใช้ค่าแอททริบิวต์วิศวกรรม

คุณสามารถใช้การค้นหาแอททริบิวต์วิศวกรรมเพื่อค้นหาผลิตภัณฑ์โดยการค้นหาค่าแอททริบิวต์วิศวกรรม ดังนั้น คุณสามารถค้นหาผลิตภัณฑ์วิศวกรรมตามลักษณะของผลิตภัณฑ์ได้อย่างง่ายดาย คุณสามารถค้นหาในผลิตภัณฑ์ที่เป็นของประเภทผลิตภัณฑ์วิศวกรรม หรือคุณสามารถค้นหาในผลิตภัณฑ์วิศวกรรมทั้งหมดได้

การค้นหาจะพร้อมใช้งานบนหน้าข้อมูลหลักของผลิตภัณฑ์ และจากสินค้าของธุรกรรมในระบบ เช่น ใบสั่งขาย สำหรับรายการธุรกรรม คุณสามารถใช้หน้า **การค้นหาแอททริบิวต์วิศวกรรม** เพื่อค้นหาผลิตภัณฑ์ คุณสามารถใช้ปุ่ม **เพิ่มเป็นบรรทัดใหม่** เพื่อเพิ่มผลิตภัณฑ์ลงในบรรทัดใบสั่งขาย นอกจากนี้ คุณยังสามารถเพิ่มผลิตภัณฑ์ในผลการค้นหาโดยตรงไปยังใบสั่ง
