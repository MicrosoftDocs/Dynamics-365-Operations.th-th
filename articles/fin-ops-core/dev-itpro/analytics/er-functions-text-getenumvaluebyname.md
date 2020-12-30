---
title: ฟังก์ชัน GETENUMVALUEBYNAME ER
description: หัวข้อนี้แสดงข้อมูลเกี่ยวกับวิธีการใช้ฟังก์ชันการรายงานทางอิเล็กทรอนิกส์ GETENUMVALUEBYNAME (ER)
author: NickSelin
manager: kfend
ms.date: 09/23/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ERDataModelDesigner, ERExpressionDesignerFormula, ERMappedFormatDesigner, ERModelMappingDesigner
audience: Application User, IT Pro
ms.reviewer: kfend
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 29d7ec6498090ea47259303237c5a64a26e4926b
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 12/05/2020
ms.locfileid: "4685943"
---
# <a name="getenumvaluebyname-er-function"></a>ฟังก์ชัน GETENUMVALUEBYNAME ER

[!include [banner](../includes/banner.md)]

ฟังก์ชัน `GETENUMVALUEBYNAME` ค้นหาค่า *Enum* เฉพาะในแหล่งข้อมูลการแจงนับที่ระบุ โดยใช้ชื่อการแจงนับที่ระบุเป็นค่า *สตริง* ถ้าพบค่า *Enum* ฟังก์ชันจะส่งคืน มิฉะนั้น ฟังก์ชันจะส่งกลับค่าการแจงนับ **null**

## <a name="syntax"></a>ไวยากรณ์

```vb
GETENUMVALUEBYNAME (enumeration data source path, enumeration value text)
```

## <a name="arguments"></a>อาร์กิวเมนต์

`enumeration data source path`: *การแจงนับ*

พาธที่ถูกต้องของแหล่งข้อมูลของหนึ่งในชนิดการแจงนับต่อไปนี้:

- การแจงนับแบบจำลองการรายงานทางอิเล็กทรอนิกส์ (ER)
- การแจงนับรูปแบบ ER
- การแจงนับ Microsoft Dynamics 365 Finance

`enumeration value text`: *สตริง*

ค่าสตริงที่แสดงชื่อของค่าการแจงนับเดียว

## <a name="return-values"></a>ส่งคืนค่า

*Enum* ที่สามารถเว้นว่างได้

ค่าการแจงนับที่เป็นผลลัพธ์

## <a name="usage-notes"></a>บันทึกย่อการใช้งาน

ไม่มีข้อยกเว้น หากไม่พบค่า *Enum* โดยใช้ชื่อของค่าการแจงนับที่ระบุเป็นค่า *สตริง*

## <a name="example-1"></a>ตัวอย่างที่ 1

ในแผนภาพต่อไปนี้ การแจงนับ **ReportDirection** ถูกนำมาใช้ในรูปแบบข้อมูล โปรดทราบว่า ป้ายชื่อถูกกำหนดไว้สำหรับค่าแจงนับ

![ค่าที่พร้อมใช้งานสำหรับการแจงนับรูปแบบข้อมูล](./media/ER-data-model-enumeration-values.PNG)

ภาพประกอบต่อไปนี้แสดงรายละเอียดเหล่านี้:

- แหล่งข้อมูล **$ทิศทาง** ถูกตั้งค่าคอนฟิกในรายงาน ER แหล่งข้อมูลนี้ถูกตั้งค่าคอนฟิกตามการแจงนับแบบจำลอง **ReportDirection**
- นิพจน์ `$IsArrivals` ถูกออกแบบมาเพื่อใช้การแจงนับแบบจำลอง–ที่ขึ้นกับ **$ทิศทาง** เป็นพารามิเตอร์ของฟังก์ชันนี้
- ค่าของนิพจน์การเปรียบเทียบนี้คือ **จริง**

![ตัวอย่างของการแจงนับรูปแบบข้อมูล](./media/ER-data-model-enumeration-usage.PNG)

## <a name="example-2"></a>ตัวอย่างที่ 2

ฟังก์ชัน `GETENUMVALUEBYNAME` และ [`LISTOFFIELDS`](er-functions-list-listoffields.md) ช่วยให้คุณสามารถนำค่าและป้ายชื่อของการแจงนับที่ได้รับการสนับสนุนเป็นค่าข้อความ (การแจงนับได้รับการสนับสนุนเป็นการแจงนับแอปพลิเคชัน การแจงนับรูปแบบข้อมูล และรูปแบบการแจงนับ)

ในแผนภาพต่อไปนี้ แหล่งข้อมูล **TransType** ถูกนำมาใช้ในการแม็ปแบบจำลอง แหล่งข้อมูลนี้อ้างอิงถึงการแจงนับแอพลิเคชัน **LedgerTransType**

![แหล่งข้อมูลของการแม็ปแบบจำลองที่อ้างอิงถึงการแจงนับของแอพลิเคชัน](./media/er-functions-text-getenumvaluebyname-example2-1.png)

ในแผนภาพต่อไปนี้แสเงแหล่งข้อมูล **TransTypeList** ที่ถูกตั้งค่าคอนฟิกในการแม็ปแบบจำลอง แหล่งข้อมูลนี้ถูกตั้งค่าคอนฟิกตามการแจงนับแอพลิเคชัน **TransType** ฟังก์ชัน `LISTOFFIELDS` ใช้เพื่อส่งคืนค่าการแจงนับทั้งหมดเป็นรายการเรกคอร์ดที่มีฟิลด์ ในลักษณะนี้ จะมีการเปิดเผยรายละเอียดของค่าการแจงนับทั้งหมด

> [!NOTE]
> ฟิลด์ **EnumValue** ถูกตั้งค่าคอนฟิกสำหรับแหล่งข้อมูล **TransTypeList** โดยใช้นิพจน์ `GETENUMVALUEBYNAME(TransType, TransTypeList.Name)` ฟิลด์นี้ส่งคืนค่าการแจงนับสำหรับเร็กคอร์ดทั้งหมดในรายการนี้

![แหล่งข้อมูลของการแม็ปแบบจำลองที่ส่งคืนค่าการแจงนับทั้งหมดของการแจงนับที่เลือกเป็นรายการของเรกคอร์ด](./media/er-functions-text-getenumvaluebyname-example2-2.png)

ในแผนภาพต่อไปนี้แสเงแหล่งข้อมูล **VendTrans** ที่ถูกตั้งค่าคอนฟิกในการแม็ปแบบจำลอง แหล่งข้อมูลนี้ส่งคืนเรกคอร์ดธุรกรรมผู้จัดจำหน่ายจากตารางแอพลิเคชัน **VendTrans** ชนิดบัญชีแยกประเภทของธุรกรรมทั้งหมดจะถูกกำหนดโดยค่าของฟิลด์ **TransType**

> [!NOTE]
> ฟิลด์ **TransTypeTitle** ถูกตั้งค่าคอนฟิกสำหรับแหล่งข้อมูล **VendTrans** โดยใช้นิพจน์ `FIRSTORNULL(WHERE(TransTypeList, TransTypeList.EnumValue = @.TransType)).Label` ฟิลด์นี้จะส่งคืนป้ายชื่อของค่าการแจงนับของธุรกรรมปัจจุบันเป็นข้อความ ถ้าค่าการแจงนับนี้พร้อมใช้งาน มิฉะนั้น จะส่งกลับค่าสตริงที่ว่างเปล่า
>
> ฟิลด์ **TransTypeTitle** ถูกผูกไว้กับฟิลด์ **LedgerType** ของรูปแบบข้อมูลซึ่งช่วยให้สามารถใช้ข้อมูลนี้ในทุกรูปแบบ ER ซึ่งใช้รูปแบบข้อมูลเป็นแหล่งที่มาของข้อมูล

![แหล่งข้อมูลของการแม็ปแบบจำลองที่ส่งคืนธุรกรรมผู้จัดจำหน่าย](./media/er-functions-text-getenumvaluebyname-example2-3.png)

ภาพประกอบต่อไปนี้แสดงวิธีการที่คุณสามารถใช้ [ดีบักเกอร์แหล่งข้อมูล](er-debug-data-sources.md) เพื่อทดสอบการแม็ปแบบจำลองที่ตั้งค่าคอนฟิก

![การใช้ดีบักเกอร์แหล่งข้อมูลเพื่อทดสอบการแม็ปแบบจำลองที่ตั้งค่าคอนฟิก](./media/er-functions-text-getenumvaluebyname-example2-4.gif)

ฟิลด์ **LedgerType** ของป้ายชื่อที่แสดงรูปแบบข้อมูลของชนิดธุรกรรมตามที่คาดไว้

ถ้าคุณวางแผนที่จะใช้วิธีการนี้สำหรับข้อมูลของธุรกรรมจำนวนมาก คุณต้องพิจารณาประสิทธิภาพของการดำเนินการ สำหรับข้อมูลเพิ่มเติม ให้ดู [ติดตามการดำเนินการของรูปแบบ ER เพื่อแก้ไขปัญหาประสิทธิภาพ](trace-execution-er-troubleshoot-perf.md)

## <a name="additional-resources"></a>ทรัพยากรเพิ่มเติม

[ฟังก์ชันข้อความ](er-functions-category-text.md)

[ติดตามการดำเนินการของรูปแบบ ER เพื่อแก้ไขปัญหาประสิทธิภาพ](trace-execution-er-troubleshoot-perf.md)

[ฟังก์ชัน LISTOFFIELDS ER](er-functions-list-listoffields.md)

[ฟังก์ชัน FIRSTORNULL ER](er-functions-list-firstornull.md)

[ฟังก์ชั่น WHERE ER](er-functions-list-where.md)
