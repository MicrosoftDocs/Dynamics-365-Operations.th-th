---
title: ออกแบบรายงานหลายภาษาในการรายงานทางอิเล็กทรอนิกส์
description: บทความนี้จะอธิบายถึงวิธีการที่คุณสามารถใช้ป้ายชื่อการรายงานทางอิเล็กทรอนิกส์ (ER) เพื่อออกแบบและสร้างรายงานหลายภาษา
author: kfend
ms.date: 05/31/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.search.region: Global
ms.author: filatovm
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.custom: ''
ms.assetid: ''
ms.search.form: ERDataModelDesigner, ERModelMappingDesigner, EROperationDesigner, ERExpressionDesignerFormula
ms.openlocfilehash: 5575ba3154521e3855ce6b97c5b37d3c4868e3e9
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 08/12/2022
ms.locfileid: "9285499"
---
# <a name="design-multilingual-reports-in-electronic-reporting"></a>ออกแบบรายงานหลายภาษาในการรายงานทางอิเล็กทรอนิกส์

[!include[banner](../includes/banner.md)]

## <a name="overview"></a>ภาพรวม

ในฐานะผู้ใช้ประเภทธุรกิจ คุณสามารถใช้กรอบงาน [การรายงานทางอิเล็กทรอนิกส์ (ER)](general-electronic-reporting.md) เพื่อตั้งค่าคอนฟิกรูปแบบสำหรับเอกสารขาออกที่ต้องถูกสร้างให้สอดคล้องกับข้อกำหนดตามกฎหมายของประเทศหรือภูมิภาคต่างๆ เมื่อข้อกำหนดเหล่านี้ต้องการให้มีการสร้างเอกสารขาออกในภาษาต่างๆ สำหรับประเทศหรือภูมิภาคต่างๆ คุณสามารถตั้งค่าคอนฟิก รูปแบบ ER เดียว ที่มีทรัพยากรที่ขึ้นอยู่กับภาษาได้ ในลักษณะดังกล่าว คุณสามารถนำรูปแบบมาใช้ใหม่เพื่อสร้างเอกสารขาออกสำหรับประเทศหรือภูมิภาคต่างๆ ได้ นอกจากนี้ คุณอาจต้องการใช้รูปแบบ ER เดียวเพื่อสร้างเอกสารขาออกในภาษาต่างๆ สำหรับลูกค้า ผู้จัดจำหน่าย บริษัทในเครือ หรือบุคคลอื่นๆ ที่เกี่ยวข้อง

คุณสามารถตั้งค่าคอนฟิกแบบจำลองข้อมูล ER และการแมปแบบจำลองเป็นแหล่งข้อมูลของรูปแบบ ER ที่ตั้งค่าคอนฟิก เพื่อกำหนดโฟลว์ข้อมูลที่ระบุข้อมูลของแอปพลิเคชันที่จะถูกนำไปวางไว้ในเอกสารที่สร้างขึ้น ในฐานะที่เป็น [ผู้ให้บริการ](general-electronic-reporting.md#Provider) การตั้งค่าคอนฟิก ER คุณสามารถ [เผยแพร่](tasks/er-upload-configuration-into-lifecycle-services.md#upload-a-configuration-into-lcs) แบบจำลองข้อมูลที่ตั้งค่าคอนฟิก การแมปแบบจำลอง และรูปแบบเป็นส่วนประกอบของโซลูชัน ER เพื่อสร้างเอกสารขาออกเฉพาะ นอกจากนี้ คุณยังสามารถอนุญาตให้ลูกค้าสามารถ [อัปโหลด](general-electronic-reporting-manage-configuration-lifecycle.md) โซลูชัน ER ที่เผยแพร่ เพื่อให้สามารถใช้และกำหนดเองได้ ถ้าคุณคาดว่าลูกค้าอาจพูดภาษาอื่น คุณสามารถตั้งค่าคอนฟิกส่วนประกอบ ER เพื่อให้มีทรัพยากรที่ขึ้นอยู่กับภาษาได้ ในลักษณะดังกล่าว เนื้อหาของส่วนประกอบ ER ที่สามารถแก้ไขได้จะแสดงขึ้นในภาษาที่ผู้ใช้ต้องการของลูกค้าในเวลาที่ออกแบบ

คุณสามารถตั้งค่าคอนฟิกทรัพยากรที่ขึ้นอยู่กับภาษาเป็นป้ายชื่อ ER จากนั้น คุณสามารถใช้ป้ายชื่อเหล่านี้เพื่อตั้งค่าคอนฟิกส่วนประกอบ ER สำหรับวัตถุประสงค์ต่อไปนี้:

- ในขณะออกแบบ:

    - แสดงเนื้อหาของส่วนประกอบ ER ที่ตั้งค่าคอนฟิกในภาษาที่ผู้ใช้ต้องการ

- ขณะรันไทม์:

    - สร้างเนื้อหาที่ขึ้นอยู่กับภาษาสำหรับเอกสารขาออก
    - แสดงข้อความแจ้งเตือนและข้อความแสดงข้อผิดพลาดในภาษาที่ผู้ใช้ต้องการ
    - พร้อมต์สำหรับฟิลด์ที่จำเป็นในภาษาที่ผู้ใช้ต้องการ

คุณสามารถตั้งค่าคอนฟิกป้ายชื่อ ER ใน [การตั้งค่าคอนฟิก](general-electronic-reporting.md#Configuration) ER ทุกรายการที่มีส่วนประกอบต่างๆ ได้ ป้ายชื่อสามารถเก็บรักษาได้โดยอิสระจากตรรกะที่ตั้งค่าคอนฟิกของแบบจำลองข้อมูล ER การแมปแบบจำลอง ER และส่วนประกอบรูปแบบ ER

มีการระบุป้ายชื่อ ER ทุกรายการโดยรหัสที่ไม่ซ้ำกันในขอบเขตของการตั้งค่าคอนฟิก ER ซึ่งเก็บป้ายชื่อนั้น ป้ายชื่อทั้งหมดอาจประกอบด้วยข้อความป้ายชื่อสำหรับภาษาทั้งหมดที่ได้รับการสนับสนุนในอินสแตนซ์ปัจจุบันของ Microsoft Dynamics 365 Finance ภาษาที่ได้รับการสนับสนุนเหล่านี้รวมถึงภาษาของการเลือกกำหนดที่ปรับใช้

## <a name="entry"></a>รายการบัญชี

เมื่อคุณออกแบบแบบจำลองข้อมูล ER การแมปแบบจำลอง ER หรือรูปแบบ ER ตัวเลือก **แปลภาษา** จะปรากฏขึ้นเมื่อใดก็ตามที่คุณเลือกฟิลด์ที่อาจมีบริบทที่สามารถแปลได้ เมื่อคุณเลือกตัวเลือกนี้ คุณสามารถเชื่อมโยงฟิลด์ที่เลือกกับป้ายชื่อ ER บน <a name="TextTranslationPane">บานหน้าต่าง</a> **การแปลข้อความ** คุณสามารถเลือกป้ายชื่อ ER ที่มีอยู่ หรือคุณสามารถเพิ่มป้ายชื่อ ER ใหม่ ถ้ายังไม่พร้อมใช้งาน เมื่อคุณเลือกหรือเพิ่มป้ายชื่อ ER คุณสามารถเพิ่มข้อความที่เกี่ยวข้องสำหรับภาษาทั้งหมดที่ได้รับการสนับสนุนในอินสแตนซ์ Finance ปัจจุบัน

ภาพประกอบต่อไปนี้แสดงวิธีการดำเนินการแปลนี้ในแบบจำลองข้อมูล ER ที่สามารถแก้ไขได้ ในตัวอย่างนี้ จะมีการแปลแอตทริบิวต์ **คำอธิบาย** ของฟิลด์ **PurchaseOrder** สำหรับ **แบบจำลองใบแจ้งหนี้** ที่สามารถแก้ไขได้ เป็นภาษาเยอรมันภาษาออสเตรีย (DE-AT) และภาษาญี่ปุ่น (JA)

![การให้คำแปลของป้ายชื่อ ER ในโปรแกรมออกแบบแบบจำลองข้อมูล ER](./media/er-multilingual-labels-refer.png)

สามารถแปลเฉพาะข้อความป้ายชื่อสำหรับป้ายชื่อที่อยู่ในส่วนประกอบ ER ที่แก้ไขได้เท่านั้น ตัวอย่างเช่น ถ้าคุณเลือก **แปล** สำหรับแอตทริบิวต์ของป้ายชื่อของแหล่งข้อมูลการแมปแบบจำลอง ER แล้วจากนั้น คุณเลือกป้ายชื่อ ER ที่อยู่ในแบบจำลองข้อมูล ER หลัก คุณจะเห็นเนื้อหาของป้ายชื่อ แต่คุณจะไม่สามารถเปลี่ยนแปลงได้ ในกรณีเหล่านี้ ฟิลด์ **ข้อความที่แปล** จะไม่พร้อมใช้งาน ดังที่แสดงในภาพประกอบต่อไปนี้

![การตรวจสอบคำแปลที่มีให้ของป้ายชื่อ ER ในตัวออกแบบการแมปแบบจำลอง ER](./media/er-multilingual-labels-refer-mapping.png)

> [!NOTE]
> คุณไม่สามารถใช้โปรแกรมออกแบบเพื่อลบป้ายชื่อที่ป้อนไว้ในส่วนประกอบ ER ที่แก้ไขได้

## <a name="scope"></a>ขอบเขต

ป้ายชื่อ ER สามารถอ้างอิงถึงในแอตทริบิวต์ที่แปลได้ต่างๆ ของส่วนประกอบ ER

### <a name="data-model-component"></a>ส่วนประกอบแบบจำลองข้อมูล

เมื่อคุณตั้งค่าคอนฟิกแบบจำลองข้อมูล ER คุณสามารถเพิ่มป้ายชื่อ ER ได้ แอตทริบิวต์ **ป้ายชื่อ** และ **คำอธิบาย** ของรายการแบบจำลอง ฟิลด์ของแบบจำลองทั้งหมด และค่าการแจงนับแบบจำลอง <a id="LinkModelEnum"></a>ทั้งหมดสามารถเชื่อมโยงกับป้ายชื่อ ER ซึ่งถูกเพิ่มเข้าในแบบจำลองข้อมูล ER ได้

![การให้การแปลสำหรับแอตทริบิวต์คำอธิบายในโปรแกรมออกแบบแบบจำลองข้อมูล ER](./media/er-multilingual-labels-refer.png)

เมื่อมีการตั้งค่าคอนฟิกแบบจำลองข้อมูล ER ในลักษณะนี้ เนื้อหาจะแสดงต่อผู้ใช้ของโปรแกรมออกแบบแบบจำลองข้อมูล ER ในภาษาที่ผู้ใช้แต่ละคนต้องการ ดังนั้น การบำรุงรักษาแบบจำลองจะลดความยุ่งยากลง ภาพประกอบต่อไปนี้แสดงวิธีการทำงานของฟังก์ชันนี้สำหรับผู้ใช้ที่มี DE-AT และ JA ที่ตั้งค่าเป็นภาษาที่ต้องการ

![โครงร่างของตัวออกแบบแบบจำลองข้อมูล ER สำหรับผู้ใช้ที่มี DE-AT ที่กำหนดเป็นภาษาที่ต้องการ](./media/er-multilingual-labels-refer-de.png)

![โครงร่างของตัวออกแบบแบบจำลองข้อมูล ER สำหรับผู้ใช้ที่มี JA ที่กำหนดเป็นภาษาที่ต้องการ](./media/er-multilingual-labels-refer-ja.png)

### <a name="model-mapping-component"></a>ส่วนประกอบการแมปแบบจำลอง

เนื่องจากการแมปแบบจำลอง ER จะขึ้นอยู่กับแบบจำลองข้อมูล ER ป้ายชื่อขององค์ประกอบแบบจำลองข้อมูลที่อ้างถึงจะปรากฏในภาษาที่ต้องการของผู้ใช้ในโปรแกรมออกแบบการแมปแบบจำลอง ภาพประกอบต่อไปนี้แสดงวิธีการอธิบายความหมายของฟิลด์ **PurchaseOrder** ในการแมปแบบจำลองที่แก้ไขได้ โดยใช้ป้ายชื่อของแอตทริบิวต์ **คำอธิบาย** ที่มีการเพิ่มลงในแบบจำลองข้อมูลที่ตั้งค่าคอนฟิก โปรดสังเกตว่าป้ายชื่อนี้แสดงอยู่ในภาษาที่ผู้ใช้ต้องการ (DE-AT ในตัวอย่างนี้)

![โครงร่างของตัวออกแบบการแมปแบบจำลอง ER สำหรับผู้ใช้ที่มี DE-AT ที่กำหนดเป็นภาษาที่ต้องการ](./media/er-multilingual-labels-show-mapping.png)

เมื่อมีการตั้งค่าคอนฟิกแอตทริบิวต์ **ป้ายชื่อ** ของแหล่งข้อมูล **พารามิเตอร์ป้อนเข้าของผู้ใช้** เป็นเชื่อมโยงกับป้ายชื่อ ER ฟิลด์พารามิเตอร์ที่สอดคล้องกับแหล่งข้อมูลนี้จะถูกแสดงอยู่ในกล่องโต้ตอบผู้ใช้ที่รันไทม์แก่ผู้ใช้ในภาษาที่พวกเขาต้องการ

### <a name="format-component"></a>ส่วนประกอบรูปแบบ

เมื่อคุณตั้งค่าคอนฟิกรูปแบบ ER คุณสามารถเพิ่มป้ายชื่อ ER ได้ แอตทริบิวต์ **ป้ายชื่อ** และ **ข้อความวิธีใช้** ของแหล่งข้อมูลที่ตั้งค่าคอนฟิกทั้งหมด สามารถเชื่อมโยงกับป้ายชื่อ ER ซึ่งถูกเพิ่มลงในรูปแบบ ER แอตทริบิวต์ **ป้ายชื่อ** และ **คำอธิบาย** ของ <a id="LinkFormatEnum"></a>ค่าการแจงนับรูปแบบทั้งหมด สามารถเชื่อมโยงไปยังป้ายชื่อ ER ซึ่งสามารถเข้าถึงได้จากรูปแบบ ER ที่แก้ไขได้

> [!NOTE]
> นอกจากนี้ คุณยังสามารถเชื่อมโยงแอตทริบิวต์เหล่านี้ไปยังป้ายชื่อ ER ของแบบจำลองข้อมูล ER หลัก ซึ่งใช้ป้ายชื่อของแบบจำลองซ้ำในรูปแบบ ER ทุกรูปแบบที่มีการตั้งค่าคอนฟิกสำหรับแบบจำลองข้อมูล ER นี้

เมื่อมีการตั้งค่าคอนฟิกรูปแบบ ER ในลักษณะนี้ เนื้อหาของรูปแบบจะแสดงต่อผู้ใช้ของโปรแกรมออกแบบการดำเนินการ ER ในภาษาที่ผู้ใช้แต่ละคนต้องการ ดังนั้น การบำรุงรักษารูปแบบและการวิเคราะห์ของตรรกะที่ตั้งค่าคอนฟิกจึงเป็นแบบง่าย

เนื่องจากรูปแบบ ER ขึ้นอยู่กับแบบจำลองข้อมูล ER ป้ายชื่อที่อ้างอิงถึงในองค์ประกอบแบบจำลองข้อมูลจะถูกแสดงในโปรแกรมออกแบบรูปแบบ ER ในภาษาที่ผู้ใช้ต้องการ

เมื่อแอตทริบิวต์ **ป้ายชื่อ** ของแหล่งข้อมูล **พารามิเตอร์ป้อนเข้าของผู้ใช้** ถูกเชื่อมโยงกับป้ายชื่อ ER ฟิลด์ที่สอดคล้องกับพารามิเตอร์ในกล่องโต้ตอบผู้ใช้จะถูกแสดงต่อผู้ใช้เป็นพร้อมต์ ภาพประกอบต่อไปนี้แสดงวิธีการที่คุณสามารถเชื่อมโยงแอตทริบิวต์ **ป้ายชื่อ** ของแหล่งข้อมูล **พารามิเตอร์ข้อมูลป้อนเข้าของผู้ใช้** ในเวลาที่ออกแบบไปยังป้ายชื่อ ER เพื่อให้ผู้ใช้ได้รับการพร้อมต์สำหรับพารามิเตอร์ในภาษาที่แตกต่างกันที่ผู้ใช้ต้องการ (ซึ่งแสดงไว้สำหรับภาษาอังกฤษสหรัฐอเมริกาและภาษา DE-AT) ขณะรันไทม์

![การให้คำแปลของแอตทริบิวต์ของพารามิเตอร์ป้อนเข้าของผู้ใช้ในตัวออกแบบการดำเนินงาน ER](./media/er-multilingual-labels-refer-format.png)

![การประมวลผลการชำระเงินให้แก่ผู้จัดจำหน่ายของ ER เมื่อรันไทม์ สำหรับภาษาที่ผู้ใช้ต้องการแบบ EN-US](./media/er-multilingual-labels-show-runtime-en.png)

![การประมวลผลการชำระเงินให้แก่ผู้จัดจำหน่ายของ ER เมื่อรันไทม์ สำหรับภาษาที่ผู้ใช้ต้องการแบบ DE-AT](./media/er-multilingual-labels-show-runtime-de.png)

### <a name="expressions"></a>นิพจน์

เมื่อต้องการใช้ป้ายชื่อใน [นิพจน์](er-formula-language.md) ER คุณต้องใช้ไวยากรณ์ **@"GER\_LABEL:X"** ซึ่งคำนำหน้า **@** บ่งชี้ว่าตัวถูกดำเนินการอ้างอิงถึงป้ายชื่อ **GER\_LABEL** บ่งชี้ว่ามีป้ายชื่อ ER เกี่ยวข้อง และ **X** คือรหัสป้ายชื่อ ER

![การตั้งค่าคอนฟิกนิพจน์ ER ที่มีการอ้างอิงไปยังป้ายชื่อ ER ในโปรแกรมออกแบบสูตร ER](./media/er-multilingual-labels-expression1.png)

เมื่อต้องการอ้างอิงไปยังป้ายชื่อระบบ (แอปพลิเคชัน) ให้ใช้ไวยากรณ์ **@ "X"** ที่ซึ่งคำนำหน้า **@** บ่งชี้ว่าตัวถูกดำเนินการอ้างอิงถึงป้ายชื่อ และ **X** คือรหัสป้ายชื่อของระบบ

![การตั้งค่าคอนฟิกนิพจน์ ER ที่มีการอ้างอิงไปยังป้ายชื่อแอปพลิเคชันในโปรแกรมออกแบบสูตร ER](./media/er-multilingual-labels-expression2.png)

#### <a name="model-mapping"></a>การแมปแบบจำลอง

คุณสามารถตั้งค่าคอนฟิกนิพจน์ของการแมปแบบจำลอง ER โดยใช้ป้ายชื่อ เมื่อมีการเรียกใช้การแมปนี้โดยรูปแบบ ER ซึ่งถูกเรียกใช้เพื่อสร้างเอกสารขาออก บริบทของการดำเนินการรวมถึงรหัสภาษา ป้ายชื่อนิพจน์ที่ตั้งค่าคอนฟิกจะถูกเติมด้วยข้อความป้ายชื่อที่ได้รับการตั้งค่าคอนฟิกสำหรับภาษาของบริบทนั้น

ถ้าป้ายชื่อที่อ้างอิงไม่มีการแปลสำหรับภาษาของบริบทการดำเนินการรูปแบบที่เรียกการแมปแบบจำลอง ข้อความป้ายชื่อในภาษา EN-US จะถูกใช้แทน

#### <a name="format"></a>รูปแบบ

คุณสามารถตั้งค่าคอนฟิกนิพจน์ ER ของรูปแบบ ER โดยใช้ป้ายชื่อ เมื่อมีการเรียกใช้รูปแบบนี้เพื่อสร้างเอกสารขาออก บริบทของการดำเนินการรวมถึงรหัสภาษา ป้ายชื่อนิพจน์ที่ตั้งค่าคอนฟิกจะถูกเติมด้วยข้อความป้ายชื่อที่ได้รับการตั้งค่าคอนฟิกสำหรับภาษาของบริบทนั้น

![การให้คำแปลของป้ายชื่อ ER ของนิพจน์ ER ที่แก้ไขได้ในโปรแกรมออกแบบสูตร ER](./media/er-multilingual-labels-refer-in-expression.png)

![ตัวอย่างของการผูกข้อมูลที่อ้างอิงถึงป้ายชื่อ ER ในตัวออกแบบการดำเนินงาน ER](./media/er-multilingual-labels-refer-in-binding.png)

คุณสามารถตั้งค่าคอนฟิกส่วนประกอบ **FILE** ของรูปแบบ ER เพื่อสร้างรายงานในภาษาที่ผู้ใช้ต้องการ

![ตั้งค่าส่วนประกอบ FILE ในตัวออกแบบการดำเนินงาน ER เพื่อสร้างรายงานในภาษาที่ผู้ใช้ต้องการ](./media/er-multilingual-labels-language-context-user.png)

ถ้าคุณตั้งค่าคอนฟิกรูปแบบ ER ด้วยวิธีนี้ รายงานจะถูกสร้างขึ้นโดยใช้ข้อความที่สอดคล้องกันของป้ายชื่อ ER ภาพประกอบต่อไปนี้แสดงตัวอย่างของรายงานสำหรับภาษาของผู้ใช้แบบ EN-US และ DE-AT

![พรีวิวของรายงานที่สร้างขึ้นในภาษาที่ผู้ใช้ต้องการแบบ EN-US](./media/er-multilingual-labels-report-preview-en.png)

![พรีวิวของรายงานที่สร้างขึ้นในภาษาที่ผู้ใช้ต้องการแบบ DE-AT](./media/er-multilingual-labels-report-preview-de.png)

ถ้าป้ายชื่อที่อ้างอิงไม่มีการแปลสำหรับภาษาของบริบทการดำเนินการของรูปแบบ ข้อความป้ายชื่อในภาษา EN-US จะถูกใช้แทน

> [!TIP]
> คุณสามารถใช้ **โฟลเดอร์** และส่วนประกอบของ **ไฟล์** ชนิดเฉพาะ ในรูปแบบ ER ที่แก้ไขได้ เพื่อระบุวิธีการสร้างไฟล์ขาออก เมื่อต้องการตั้งชื่อไฟล์ที่สร้างขึ้น ให้ตั้งค่าคอนฟิก [นิพจน์](er-formula-language.md) ER ของพารามิเตอร์ **ชื่อไฟล์** ของส่วนประกอบ คุณสามารถใช้ป้ายชื่อในนิพจน์ที่ตั้งค่าคอนฟิก เนื่องจากพารามิเตอร์ **ชื่อไฟล์** เป็นการวินิจฉัยภาษาโดยค่าเริ่มต้น ข้อความของป้ายชื่อทั้งหมดที่คุณอ้างอิงถึงในนิพจน์นี้จึงแสดงในภาษา EN-US เริ่มต้น ที่รันไทม์ อย่างไรก็ตาม ในเวอร์ชัน 10.0.28 และเวอร์ชันต่อมา คุณสามารถเปิดใช้งานคุณลักษณะ **ใช้พารามิเตอร์ 'การกำหนดลักษณะภาษา' กับนิพจน์ 'ชื่อไฟล์'** นิพจน์ **ชื่อไฟล์** จะใช้พารามิเตอร์ **การกำหนดลักษณะภาษา** กับบัญชี เมื่อถูกคำนวณ

## <a name="language"></a>ภาษา

ER สนับสนุนวิธีการที่แตกต่างกันในการระบุภาษาสำหรับรายงานที่สร้างขึ้น ในฟิลด์ **การกำหนดลักษณะภาษา** บนแท็บ **รูปแบบ** คุณสามารถเลือกค่าต่อไปนี้:

- **การกำหนดลักษณะของบริษัท** – สร้างรายงานในภาษาที่บริษัทระบุ

    ![ระบุภาษาที่บริษัทต้องการในตัวออกแบบการดำเนินงาน ER เป็นภาษาของรายงานที่สร้าง](./media/er-multilingual-labels-language-context-company.png)

- **การกำหนดลักษณะของผู้ใช้** – สร้างรายงานในภาษาที่ผู้ใช้ต้องการ
- **กำหนดอย่างชัดแจ้ง** – สร้างรายงานในภาษาที่ระบุในเวลาการออกแบบ

    ![ระบุภาษาที่ระบุในเวลาการออกแบบในตัวออกแบบการดำเนินงาน ER เป็นภาษาของรายงานที่สร้าง](./media/er-multilingual-labels-language-context-fixed.png)

- **กำหนดที่รันไทม์** – สร้างรายงานในภาษาที่ระบุที่รันไทม์ ถ้าคุณเลือกค่านี้ ในฟิลด์ **ภาษา** ให้ตั้งค่าคอนฟิกนิพจน์ ER ซึ่งส่งคืนรหัสภาษาสำหรับภาษา เช่น ภาษาของลูกค้าที่เกี่ยวข้อง

    ![ระบุภาษาที่ระบุที่รันไทม์ในตัวออกแบบการดำเนินงาน ER เป็นภาษาของรายงานที่สร้าง](./media/er-multilingual-labels-language-context-runtime.png)

## <a name="culture-specific-formatting"></a>การจัดรูปแบบเฉพาะวัฒนธรรม

ER สนับสนุนวิธีการที่แตกต่างกันในการระบุวัฒนธรรมสำหรับรายงานที่สร้างขึ้น ดังนั้น การจัดรูปแบบเฉพาะ Culture ที่ถูกต้องจึงสามารถใช้กับวันที่ เวลา และค่าตัวเลขได้ เมื่อคุณออกแบบรูปแบบ ER บนแท็บ **รูปแบบ** ในฟิลด์ **การกำหนดลักษณะวัฒนธรรม** คุณสามารถเลือกค่าใดค่าหนึ่งต่อไปนี้สำหรับทุกๆ ส่วนประกอบรูปแบบของชนิด **ทั่วไป\\ไฟล์**, **Excel\\ไฟล์**, **PDF\\ไฟล์** หรือ **PDF\\ตัวผสาน**:

- **การกำหนดลักษณะของผู้ใช้** – จัดรูปแบบค่าตามวัฒนธรรมที่ผู้ใช้ต้องการ วัฒนธรรมนั้นจะถูกกําหนดในฟิลด์ **วันที่ เวลา และรูปแบบตัวเลข** บนแท็บ **การกําหนดลักษณะ** ของหน้า **ตัวเลือกผู้ใช้**

    ![การนิยามวัฒนธรรมที่ผู้ใช้ต้องการเป็นวัฒนธรรมของรายงานที่สร้างขึ้นในโปรแกรมออกแบบการดําเนินงาน ER](./media/er-multilingual-labels-culture-context-user-preferred.png)

- **กําหนดอย่างชัดแจ้ง** – จัดรูปแบบค่าตามวัฒนธรรมที่ระบุในเวลาการออกแบบ

    ![การนิยามวัฒนธรรมที่ระบุในเวลาการออกแบบเป็นวัฒนธรรมของรายงานที่สร้างขึ้นในโปรแกรมออกแบบการดําเนินงาน ER](./media/er-multilingual-labels-culture-context-fixed.png)

- **กำหนดที่รันไทม์** – จัดรูปแบบค่าตามวัฒนธรรมที่ระบุที่รันไทม์ ถ้าคุณเลือกค่านี้ บนแท็บ **การแมป** ในฟิลด์ **วันที่ เวลา และรูปแบบหมายเลข** ให้ตั้งค่าคอนฟิกนิพจน์ ER ที่จะส่งคืนรหัสขวัฒนธรรมสำหรับวัฒนธรรม เช่น วัฒนธรรมของลูกค้าที่สอดคล้องกัน

    ![การนิยามวัฒนธรรมที่กำหนดที่รันไทม์เป็นวัฒนธรรมของรายงานที่สร้างขึ้นในโปรแกรมออกแบบการดําเนินงาน ER](./media/er-multilingual-labels-culture-context-runtime.png)

> [!NOTE]
> ส่วนประกอบ ER ที่คุณกําหนดวัฒนธรรมเฉพาะให้ อาจมีส่วนประกอบ ER รองที่ตั้งค่าคอนฟิกไว้เพื่อเติมค่าข้อความ ตามค่าเริ่มต้น วัฒนธรรมของส่วนประกอบหลักจะถูกใช้เพื่อจัดรูปแบบค่าของส่วนประกอบเหล่านั้น คุณสามารถใช้ฟังก์ชัน ER ในตัวต่อไปนี้ เพื่อตั้งค่าคอนฟิกการผูกข้อมูลสำหรับส่วนประกอบเหล่านั้น และใช้วัฒนธรรมอื่นในการจัดรูปแบบค่า:
>
> - [DATEFORMAT](er-functions-datetime-dateformat.md#syntax-2)
> - [DATETIMEFORMAT](er-functions-datetime-datetimeformat.md#syntax-2)
> - [NUMBERFORMAT](er-functions-text-numberformat.md#syntax-2)
>
> ในรุ่น 10.0.20 และรุ่นต่อมา ตำแหน่งที่ตั้งของส่วนประกอบรูปแบบของชนิด **ทั่วไป\\ไฟล์** และ **Excel\\ไฟล์** จะใช้ในการจัดรูปแบบค่าระหว่าง [การแปลง PDF](electronic-reporting-destinations.md#OutputConversionToPDF) ของเอกสารที่สร้างขึ้น

## <a name="translation"></a>การแปล

คุณสามารถเพิ่มป้ายชื่อ ER ที่จำเป็นต้องมีส่วนประกอบ ER ที่แก้ไขได้ เมื่อมีการเพิ่มป้ายชื่อ ER จะสามารถแปลได้สองวิธี: ด้วยตนเอง และโดยอัตโนมัติ

### <a name="manual-translation"></a>การแปลด้วยตนเอง

เมื่อคุณเพิ่มป้ายชื่อ ER บน **การแปลข้อความ** [บานหน้าต่าง](#TextTranslationPane) คุณสามารถแปลด้วยตนเองเป็นภาษาทั้งหมดที่ได้รับการสนับสนุนในอินสแตนซ์ Finance ปัจจุบัน คุณสามารถเลือกภาษาที่ต้องการในฟิลด์ **ภาษา** ในส่วน **ภาษาของระบบ** หรือ **ภาษาของผู้ใช้** ให้ป้อนข้อความที่เหมาะสมในฟิลด์ **ข้อความที่มีการแปล** ที่สอดคล้องกัน และจากนั้น เลือก **แปล** กระบวนการนี้ต้องถูกทำซ้ำสำหรับภาษาที่จำเป็นทั้งหมดและป้ายชื่อทั้งหมดที่คุณเพิ่ม

### <a name="automatic-translation"></a>การแปลอัตโนมัติ

มีการดำเนินการตั้งค่าคอนฟิกของส่วนประกอบ ER ในการตั้งค่าคอนฟิก ER รุ่นแบบร่าง ซึ่งส่วนประกอบ ER ที่แก้ไขได้อยู่

![หน้าการตั้งค่าคอนฟิก ER เสนอการเข้าถึงรุ่นของการตั้งค่าคอนฟิกในสถานะแบบร่าง](./media/er-multilingual-labels-configurations.png)

ตามที่อธิบายไว้ก่อนหน้านี้ในบทความนี้ คุณสามารถเพิ่มป้ายชื่อ ER ที่จำเป็นต้องมีส่วนประกอบ ER ที่แก้ไขได้ ด้วยวิธีนี้ คุณสามารถระบุข้อความของป้ายชื่อ ER ได้ในภาษา EN-US จากนั้น คุณสามารถส่งออกป้ายชื่อของส่วนประกอบ ER ได้โดยใช้ฟังก์ชัน ER ภายใน เลือกการตั้งค่าคอนฟิก ER รุ่นแบบร่างที่มีส่วนประกอบ ER ที่แก้ไขได้ แล้วจากนั้น เลือก **Exchange \> ป้ายชื่อการส่งออก**

![หน้าการตั้งค่าคอนฟิก ER ที่อนุญาตให้ส่งออกป้ายชื่อ ER จากรุ่นการตั้งค่าคอนฟิกที่เลือก](./media/er-multilingual-labels-export.png)

คุณสามารถส่งออกป้ายชื่อทั้งหมด หรือป้ายชื่อทั้งหมดสำหรับภาษาเดียวที่คุณระบุที่จุดเริ่มต้นของการส่งออก มีการส่งออกป้ายชื่อเป็นไฟล์ zip ที่มีไฟล์ XML ไฟล์ XML ทุกไฟล์มีป้ายชื่อสำหรับภาษาเดียว

![ตัวอย่างของไฟล์ที่ส่งออกที่มีป้ายชื่อ ER สำหรับภาษา DE-AT](./media/er-multilingual-labels-in-xml.png)

รูปแบบนี้ใช้สำหรับการแปลป้ายชื่อโดยอัตโนมัติโดย Translation service ภายนอก เช่น [Dynamics 365 Translation Service](../lifecycle-services/translation-service-overview.md) เมื่อคุณได้รับป้ายชื่อที่แปล คุณสามารถนำเข้าป้ายชื่อเหล่านั้นกลับเข้าไปในการตั้งค่าคอนฟิก ER รุ่นแบบร่างที่มีส่วนประกอบ ER ซึ่งเป็นเจ้าของป้ายชื่อเหล่านั้นได้ เลือกการตั้งค่าคอนฟิก ER รุ่นแบบร่างที่มีส่วนประกอบ ER ที่แก้ไขได้ และเลือก **Exchange \> โหลดป้ายชื่อ**

![หน้าการตั้งค่าคอนฟิก ER ที่อนุญาตให้นำเข้าป้ายชื่อ ER ไปยังรุ่นการตั้งค่าคอนฟิกที่เลือก](./media/er-multilingual-labels-load.png)

ป้ายชื่อที่แปลจะถูกนำเข้าไปยังการตั้งค่าคอนฟิก ER ที่เลือก มีการแทนที่ป้ายชื่อที่มีการแปลที่มีอยู่ในการตั้งค่าคอนฟิก ER นี้ ถ้าป้ายชื่อที่แปลใดๆ ขาดหายไปในการตั้งค่าคอนฟิก ER จะมีการผนวกเข้าไป

## <a name="lifecycle"></a>Lifecycle

ป้ายชื่อของส่วนประกอบ ER ที่สามารถแก้ไขได้จะถูกเก็บไว้ พร้อมกับเนื้อหาอื่นๆ สำหรับส่วนประกอบ ในการตั้งค่าคอนฟิก ER รุ่นที่เหมาะสม

ป้ายชื่อของส่วนประกอบ ER ฐานสามารถอ้างอิงถึงในรุ่นที่สืบทอดมาของส่วนประกอบ ER ที่คุณสร้างขึ้นเพื่อแนะนำการปรับเปลี่ยนของคุณ

> [!TIP]
> เมื่อคุณออกแบบโซลูชัน ER คุณสามารถได้รับส่วนประกอบ [รูปแบบข้อมูล](er-overview-components.md#data-model-component) ER ของคุณเอง จากส่วนประกอบที่จัดเตรียมไว้ ในรูปแบบข้อมูลที่ได้รับนี้ คุณสามารถแนะนำป้ายชื่อ ER ของคุณเองและใช้ป้ายชื่อเหล่านั้นในรูปแบบ ER ทั้งหมดที่จะใช้รูปแบบข้อมูลเป็นแหล่งข้อมูล จากนั้น คุณสามารถได้รับส่วนประกอบ [รูปแบบ](er-overview-components.md#format-component) ER ของคุณเองจากส่วนประกอบที่ระบุโดยการเลือกรูปแบบข้อมูล ER ที่ได้รับของคุณแทนรูปแบบที่ระบุ ในรุ่น 10.0.28 และรุ่นที่ใหม่กว่า คุณสามารถเปิดใช้งานคุณลักษณะ **ปรับปรุงการเข้าถึงป้ายชื่อของแบบจำลองข้อมูล ER ที่สูงขึ้น** เพื่อเข้าถึงป้ายชื่อของแบบจำลองข้อมูล ER ที่สูงขึ้นในส่วนประกอบรูปแบบ ER ที่ได้รับมา แม้เมื่อแบบจำลองข้อมูล ER ที่คุณเลือกสำหรับส่วนประกอบ ER ที่ได้รับมาแตกต่างจากที่ใช้ในส่วนประกอบ ER ฐาน
>
> เมื่อใช้ชื่อป้ายชื่อเดียวกันในส่วนประกอบที่ได้รับและส่วนประกอบที่สูงขึ้น การแปลของป้ายชื่อนั้นของคุณจะถูกใช้เป็นองค์ประกอบที่เกี่ยวข้องมากที่สุด

การกำหนดรุ่น ER ควบคุมการกำหนดป้ายชื่อให้กับแอตทริบิวต์ใดๆ ในส่วนประกอบ ER มีการบันทึกการเปลี่ยนแปลงไปยังการกำหนดป้ายชื่อในรายการของการเปลี่ยนแปลง (เดลต้า) ของส่วนประกอบ ER ที่แก้ไขได้ ซึ่งสร้างขึ้นเป็นรุ่นที่สืบทอดมาจากส่วนประกอบ ER ที่ระบุ การเปลี่ยนแปลงเหล่านี้จะถูกตรวจสอบความถูกต้อง เมื่อรุ่นที่สืบทอดมาถูกปรับใช้ซ้ำไปยังรุ่นฐานใหม่

## <a name="functions"></a>ฟังก์ชัน

ฟังก์ชัน ER ของ [LISTOFFIELDS](er-functions-list-listoffields.md) ภายใน สามารถเข้าถึงป้ายชื่อ ER ที่ได้รับการตั้งค่าคอนฟิกสำหรับบางรายการของส่วนประกอบ ER

ดังที่อธิบายไว้ก่อนหน้านี้ในบทความนี้ จะมีการเชื่อมโยงแอตทริบิวต์ **ป้ายชื่อ** และ **คำอธิบาย** ของค่าของการแจงนับ ER ของ [แบบจำลอง](#LinkModelEnum) หรือ [รูปแบบ](#LinkFormatEnum) ทั้งหมดไปยังป้ายชื่อ ER ที่เข้าถึงได้ในส่วนประกอบ ER ที่เหมาะสม คุณสามารถตั้งค่าคอนฟิกนิพจน์ ER ซึ่งคุณเรียกใช้ฟังก์ชัน **LISTOFFIELDS** โดยใช้การแจงนับ ER เป็นอาร์กิวเมนต์ นิพจน์นี้ส่งคืนรายการที่ประกอบด้วยเรกคอร์ดสำหรับค่าทั้งหมดของการแจงนับ ER ซึ่งถูกกำหนดเป็นอาร์กิวเมนต์ของฟังก์ชันนี้ เรกคอร์ดทั้งหมดมีค่าของป้ายชื่อ ER ซึ่งเชื่อมโยงกับค่าการแจงนับ ER:

- ค่าของป้ายชื่อ ER ที่เชื่อมโยงกับแอตทริบิวต์ **ป้ายชื่อ** ถูกจัดเก็บไว้ในฟิลด์ **ป้ายชื่อ** ของเรกคอร์ดที่ส่งคืน
- ค่าของป้ายชื่อ ER ที่เชื่อมโยงกับแอตทริบิวต์ **คำอธิบาย** ถูกจัดเก็บไว้ในฟิลด์ **คำอธิบาย** ของเรกคอร์ดที่ส่งคืน

## <a name="performance"></a><a name=performance></a>ประสิทธิภาพการทำงาน

เมื่อคุณตั้งค่าคอนฟิกส่วนประกอบรูปแบบ ER เพื่อสร้างรายงานใน [ภาษา](#language) ที่คุณต้องการ หรือเพื่อนําเข้าเอกสารขาเข้าที่เนื้อหาจะถูกแยกวิเคราะห์ตามภาษาที่คุณต้องการ เราขอแนะนําให้คุณเปิดใช้งานคุณลักษณะ **แคชภาษาที่ต้องการของผู้ใช้ปัจจุบันเพื่อให้ ER ทำงาน** ในพื้นที่ทำงาน [การจัดการคุณลักษณะ](../../fin-ops/get-started/feature-management/feature-management-overview.md) คุณลักษณะนี้จะช่วยปรับปรุงประสิทธิภาพ โดยเฉพาะอย่างยิ่งกับส่วนประกอบรูปแบบ ER ที่มีการอ้างอิงหลายการอ้างอิงไปยังป้ายชื่อในสูตร ER และการผูกข้อมูล และกฎ [การตรวจสอบความถูกต้อง](general-electronic-reporting-formula-designer.md#TestFormula) ต่างๆ เพื่อสร้างข้อความของผู้ใช้ในภาษาที่ต้องการของคุณ

เมื่อคุณเปลี่ยนสถานะของรุ่นการตั้งค่าคอนฟิก ER จาก **แบบร่าง** ไปเป็น **เสร็จสมบูรณ์** ถ้ารุ่นการตั้งค่าคอนฟิกมีป้ายชื่อ ER ป้ายชื่อเหล่านั้นจะจัดเก็บไว้ในฐานข้อมูลแอปพลิเคชัน Schema การจัดเก็บจะขึ้นอยู่กับสถานะของคุณลักษณะ **เร่งเวลาการจัดเก็บป้ายชื่อ ER**

- ถ้าไม่ได้เปิดใช้งานคุณลักษณะ ป้ายชื่อทั้งหมดจะจัดเก็บในฟิลด์ **LABELXML** ของตาราง **ERSOLUTIONVERSIONTABLE** เป็นส่วนย่อยเดียวของ XML
- ถ้าเปิดใช้งานลักษณะ ระบบจะสร้างเรกคอร์ดที่แยกต่างหากสำหรับแต่ละภาษาในตาราง **ERSOLUTIONVERSIONLABELSTABLE** ฟิลด์ **CONTENTS** ของตารางนี้จัดเก็บป้ายชื่อต่อภาษาเป็นส่วนย่อยของ XML ที่บีบอัด

เราขอแนะนำให้คุณเปิดใช้งานคุณลักษณะ **เร่งเวลาการจัดเก็บป้ายชื่อ ER** ในพื้นที่ทำงาน **การจัดการคุณลักษณะ** คุณลักษณะนี้จะช่วยปรับปรุงการใช้แบนด์วิธของเครือข่ายและประสิทธิภาพของระบบโดยรวม เนื่องจากส่วนใหญ่ ป้ายชื่อ ER ของภาษาเดียวจะใช้เมื่อคุณใช้งานการตั้งค่าคอนฟิก ER เดียว

เมื่อต้องการใช้ Schema การจัดเก็บที่เลือกเพื่อเก็บป้ายชื่อของการตั้งค่าคอนฟิก ER ทั้งหมดในอินสแตนซ์ Finance ปัจจุบัน ให้ปฏิบัติตามขั้นตอนต่อไปนี้

1. ไปที่ **การจัดการองค์กร** > **งานประจำงวด** > **ใช้ Schema การจัดเก็บป้ายชื่อที่เลือกกับการตั้งค่าคอนฟิก ER ทั้งหมด**
2. เลือก **ตกลง**


## <a name="additional-resources"></a>ทรัพยากรเพิ่มเติม

- [ภาพรวมการรายงานทางอิเล็กทรอนิกส์](general-electronic-reporting.md)
- [ฟังก์ชันการรายงานทางอิเล็กทรอนิกส์](er-formula-language.md#Functions)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
