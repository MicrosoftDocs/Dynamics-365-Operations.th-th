---
title: ฟังก์ชั่น REPEAT ER
description: บทความนี้แสดงข้อมูลเกี่ยวกับวิธีการใช้ฟังก์ชันการรายงานทางอิเล็กทรอนิกส์ REPEAT (ER)
author: NickSelin
ms.date: 08/01/2022
ms.prod: ''
ms.technology: ''
ms.search.form: ERDataModelDesigner, ERExpressionDesignerFormula, ERMappedFormatDesigner, ERModelMappingDesigner
audience: Application User, IT Pro
ms.reviewer: kfend
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2022-06-01
ms.dyn365.ops.version: AX 10.0.29
ms.openlocfilehash: c56139a3c63b03f907b1dcbf4365990d2a13c35a
ms.sourcegitcommit: c98d55a4a6e27239ae6b317872332f01cbe8b875
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 08/02/2022
ms.locfileid: "9220701"
---
# <a name="repeat-er-function"></a>ฟังก์ชั่น REPEAT ER

[!include [banner](../includes/banner.md)]
[!include [banner](../includes/preview-banner.md)]

ฟังก์ชัน `REPEAT` สร้างเรกคอร์ดที่ประกอบด้วยฟิลด์มีค่าที่ตรงกับอินพุทที่ระบุ จากนั้นจะส่งคืน *รายการเรกคอร์ด* ใหม่ของเรกคอร์ดที่ซ้ํากันในจํานวนครั้งที่ระบุ

## <a name="syntax"></a>ไวยากรณ์

```vb
REPEAT (item, number)
```

## <a name="arguments"></a>อาร์กิวเมนต์

`item`: ชนิดข้อมูล [ดั้งเดิม](er-formula-supported-data-types-primitive.md) หรือชนิดข้อมูล [โดยรวม](er-formula-supported-data-types-composite.md) ที่สนับสนุนใดๆ

ค่าที่จะทําซ้ํา

`number`: *เลขจำนวนเต็ม*

จำนวนของการทำซ้ำ

## <a name="return-values"></a>ค่าที่ส่งคืน

*รายการเรกคอร์ด*

รายการผลลัพธ์ของเรกคอร์ด

## <a name="usage-notes"></a>บันทึกย่อการใช้งาน

รายการของเรกคอร์ดที่ทำซำที่ถูกส่งกลับแสดงฟิลด์ต่อไปนี้:

- ค่าที่ระบุ (ฟิลด์ `Item`)
- ดัชนีเรกคอร์ดปัจจุบัน (ฟิลด์ `Number`)

> [!NOTE]
> เนื่องจากมีการใช้การระบุหมายเลขที่ใช้หนึ่งฟังก์ชันนี้ ฟิลด์ `Number` มีค่า **1** ของเรกคอร์ดแรกของรายการผลลัพธ์

คุณสามารถใช้ฟังก์ชันนี้คูณข้อมูลที่มีอยู่ เพื่อให้คุณสามารถทดสอบประสิทธิภาพและการทดสอบปริมาณของโซลูชัน [การรายงานทางอิเล็กทรอนิกส์ (ER)](general-electronic-reporting.md) ได้โดยใช้ [Regression Suite Automation Tool (RSAT)](../perf-test/rsat/rsat-overview.md)

## <a name="example"></a>ตัวอย่าง

คุณต้องการสร้างเอกสารในรูปแบบ XML ที่ต้องประกอบด้วยองค์ประกอบ `Party` XML มากเท่าที่คุณระบุในฟิลด์การป้อนข้อมูลในกล่องโต้ตอบรันไทม์ ก่อนที่การปฏิบัติการรูปแบบ ER จะเริ่มต้นขึ้น

ภาพประกอบต่อไปนี้แสดง [รูปแบบ](er-overview-components.md#format-component) ER ในรูปแบบนี้ องค์ประกอบ `Party` XML เดียวจะถูกเพิ่มเพื่อแสดงคุณสมบัติของฝ่ายเดียว

<a href="./media/er-repeat-function-1.png"><img src="./media/er-repeat-function-1.png" alt="Format structure on the Format tab of the Format designer page." class="alignnone size-full" width="929" height="548" /></a>

รูปภาพประกอบถัดไปจะแสดงแหล่งข้อมูลที่ตั้งค่าคอนฟิกต่อไปนี้

- แหล่งข้อมูล `Party` ที่แสดงถึงฝ่ายเดียว ฟิลด์ `Party.Value` ใช้ในการแสดงค่าข้อความเดียว
- [แหล่งข้อมูล](er-user-input-parameter-data-sources.md) `NumberOfRepeats` ที่ใช้ในการเสนอฟิลด์การป้อนข้อมูลในกล่องโต้ตอบรันไทม์ เพื่อให้คุณสามารถระบุจํานวนฝ่ายที่ควรจะป้อนในเอกสารที่สร้างขึ้นได้
- แหล่งข้อมูล `Party2` ที่ทําซ้ําเรกคอร์ด `Party` จํานวนครั้งที่คุณระบุไว้ในแหล่งข้อมูล `NumberOfRepeats`

<a href="./media/er-repeat-function-2.png"><img src="./media/er-repeat-function-2.png" alt="Configured data sources on the Mapping tab of the Format designer page." class="alignnone size-full" width="1044" height="411" /></a>

ภาพประกอบถัดไปจะแสดงการผูกข้อมูลของรูปแบบ ER ที่แก้ไขได้ ซึ่งสร้างขึ้นเพื่อสร้างผลลัพธ์ในรูปแบบ XML เอาท์พุทนี้แสดงฝ่ายแต่ละรายเป็นโหนดที่ระบุ

<a href="./media/er-repeat-function-3.png"><img src="./media/er-repeat-function-3.png" alt="Configured data bindings on the Mapping tab of the Format designer page." class="alignnone size-full" width="1051" height="417" /></a>

รูปภาพประกอบต่อไปนี้จะแสดงผลลัพธ์เมื่อรันรูปแบบที่ออกแบบและค่าของแหล่งข้อมูล `NumberOfRepeats` จะระบุเป็น **5**

<a href="./media/er-repeat-function-4.png"><img src="./media/er-repeat-function-4.png" alt="Result of running the format on a new web browser tab." class="alignnone wp-image-290711 size-full" width="400" height="380" /></a>

## <a name="additional-resources"></a>ทรัพยากรเพิ่มเติม

[ฟังก์ชันรายการ](er-functions-category-list.md)

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
