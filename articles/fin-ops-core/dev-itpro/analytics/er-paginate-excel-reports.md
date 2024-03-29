---
title: ออกแบบรูปแบบ ER เพื่อแบ่งหน้าเอกสารที่สร้างใน Excel
description: บทความนี้จะอธิบายถึงวิธีการออกแบบรูปแบบการรายงานทางอิเล็กทรอนิกส์ (ER) ที่แบ่งหน้าเอกสารที่สร้างใน Microsoft Excel
author: kfend
ms.date: 09/14/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.search.region: Global
ms.author: filatovm
ms.search.validFrom: 2021-08-01
ms.dyn365.ops.version: Version 10.0.22
ms.custom: 220314
ms.assetid: 2685df16-5ec8-4fd7-9495-c0f653e82567
ms.search.form: EROperationDesigner
ms.openlocfilehash: e4a34dffda9e9b95f5d6c7ee382723663817ec6b
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 08/12/2022
ms.locfileid: "9285015"
---
# <a name="design-an-er-format-to-paginate-generated-documents-in-excel"></a>ออกแบบรูปแบบ ER เพื่อแบ่งหน้าเอกสารที่สร้างใน Excel

[!include [banner](../includes/banner.md)]

บทความนี้อธิบายวิธีการของผู้ใช้ในบทบาทที่ปรึกษาด้านการทำงานการรายงานทางอิเล็กทรอนิกส์หรือผู้ดูแลระบบสามารถตั้งค่าคอนฟิกรูปแบบ [การรายงานทางอิเล็กทรอนิกส์ (ER)](general-electronic-reporting.md) เพื่อสร้างเอกสารขาออกใน Microsoft Excel และจัดการการแบ่งหน้าเอกสาร

ในตัวอย่างนี้ คุณจะปรับเปลี่ยนรูปแบบ ER ที่ Microsoft จัดเตรียมไว้ที่ใช้ในการพิมพ์รายงานการควบคุม เมื่อรายงานอินทราสแทต [สร้างขึ้น](../../../finance/localizations/tasks/eur-00002-eu-intrastat-declaration.md) รายงานนี้ช่วยให้คุณคำนึงถึงธุรกรรมอินทราสแทตที่รายงานแล้ว การปรับเปลี่ยนของคุณจะช่วยให้คุณสามารถจัดการการแบ่งหน้าของรายงานการควบคุมที่สร้างขึ้น

สามารถดำเนินงานกระบวนงานในบทความนี้ให้เสร็จสมบูรณ์ได้ ในบริษัท **DEMF** ไม่จำเป็นต้องมีการเขียนโค้ด ก่อนที่คุณจะเริ่มต้น ต้องดาวน์โหลดและบันทึกไฟล์ต่อไปนี้

| คำอธิบาย       | ชื่อไฟล์ |
|-------------------|-----------| 
| แม่แบบรายงาน 1 | [ERIntrastatReportDemo1.xlsx](https://download.microsoft.com/download/7/2/a/72ae292a-8bb2-4b9d-8397-9764218f6fa8/ERIntrastatReportDemo1%20.xlsx) |
| แม่แบบรายงาน 2 | [ERIntrastatReportDemo2.xlsx](https://download.microsoft.com/download/7/d/1/7d15858d-6260-4afa-9dda-d8b955e59b1a/ERIntrastatReportDemo2.xlsx) |

## <a name="configure-the-er-framework"></a>ตั้งค่าคอนฟิกกรอบงาน ER

ปฏิบัติตามขั้นตอนใน [ตั้งค่าคอนฟิกกรอบงาน ER](er-quick-start2-customize-report.md#ConfigureFramework) เพื่อตั้งค่าชุดที่น้อยที่สุดของพารามิเตอร์ ER คุณต้องเสร็จสิ้นการตั้งค่านี้ก่อนที่คุณจะเริ่มใช้กรอบงาน ER เพื่อออกแบบรุ่นที่กำหนดเองของรูปแบบ ER มาตรฐาน

## <a name="import-the-standard-er-format-configuration"></a>นำเข้าไฟล์การตั้งค่าคอนฟิกรูปแบบ ER มาตรฐาน

ปฏิบัติตามขั้นตอนใน [นําเข้าการตั้งค่าคอนฟิกรูปแบบ ER มาตรฐาน](er-quick-start2-customize-report.md#ImportERSolution1) เพื่อเพิ่มการตั้งค่าคอนฟิก ER มาตรฐานลงในอินสแตนซ์ Dynamics 365 Finance ปัจจุบันของคุณ นําเข้ารุ่น **1.9** ของการตั้งค่าคอนฟิกรูปแบบ **รายงานอินทราสแทต** รุ่นพื้นฐาน 1 ของการตั้งค่าคอนฟิก **แบบจำลองอินทราสแทต** พื้นฐานจะถูกนําเข้าโดยอัตโนมัติจากที่เก็บ

## <a name="customize-the-standard-er-format"></a>การเลือกกำหนดรูปแบบ ER มาตรฐาน

### <a name="create-the-custom-er-format"></a>สร้างรูปแบบ ER ที่กำหนดเอง

ในสถานการณ์นี้ คุณเป็นตัวแทนของ Litware, Inc. ซึ่งขณะนี้ถูกเลือกเป็นผู้ให้บริการการตั้งค่าคอนฟิก ER ที่ใช้งานอยู่ คุณต้องสร้างการตั้งค่าคอนฟิกรูปแบบ ER ใหม่โดยใช้การตั้งค่าคอนฟิก **รายงานอินทราสแทต** เป็นฐาน

1. ไปที่ **การจัดการองค์กร** \> **การรายงานทางอิเล็กทรอนิกส์** \> **การตั้งค่าคอนฟิก**
2. บนหน้า **การตั้งค่าคอนฟิก** ในแผนภูมิการตั้งค่าคอนฟิกในบานหน้าต่างด้านซ้าย ให้ขยาย **แบบจำลองอินทราสแทต** และเลือก **รายงานอินทราสแทต** Litware, Inc. จะใช้รุ่น 1.9 ของการตั้งค่าคอนฟิกรูปแบบ ER นี้เป็นพื้นฐานสำหรับรุ่นที่กำหนดเอง
3. เลือก **สร้างการตั้งค่าคอนฟิก** เพื่อเปิดกล่องโต้ตอบแบบหล่นลง คุณสามารถใช้กล่องโต้ตอบนี้ในการสร้างการตั้งค่าคอนฟิกใหม่สำหรับรูปแบบการชำระเงินที่กำหนดเอง
4. ในกลุ่มฟิลด์ **สร้าง** ให้เลือก **ได้รับมาจากชื่อ: รายงานอินทราสแทต Microsoft**
5. ในฟิลด์ **ชื่อ** ให้ป้อน **รายงานอินทราสแทต Litware**
6. เลือก **สร้างการตั้งค่าคอนฟิก** เพื่อสร้างรูปแบบใหม่

รุ่น 1.9.1 ของการตั้งค่าคอนฟิกรูปแบบ ER **รายงานอินทราสแทต Litware** ถูกสร้างขึ้น รุ่นนี้มีสถานะของ **แบบร่าง** และสามารถแก้ไขได้ เนื้อหาปัจจุบันของรูปแบบ ER แบบกำหนดเองของคุณตรงกับเนื้อหาของรูปแบบที่ Microsoft ให้ไว้

### <a name="make-the-custom-format-runnable"></a>ทำรูปแบบที่กำหนดเองเป็นที่สามารถรันได้

หลังจากที่มีการสร้างรูปแบบที่กำหนดเองของคุณรุ่นแรกแล้วและมีสถานะเป็น **แบบร่าง** คุณสามารถรันรูปแบบนี้เพื่อวัตถุประสงค์ในการทดสอบได้ เมื่อต้องการรันรายงาน ประมวลผลการชำระเงินให้แก่ผู้จัดจำหน่ายโดยใช้วิธีการชำระเงินที่อ้างอิงถึงรูปแบบ ER แบบกำหนดเองของคุณ โดยค่าเริ่มต้น เมื่อคุณเรียกใช้รูปแบบ ER จากแอปพลิเคชัน จะมีเฉพาะรุ่นที่มีสถานะเป็น **เสร็จสมบูรณ์** หรือ **ใช้ร่วมกัน** เท่านั้นที่ได้รับการพิจารณา ลักษณะการทำงานนี้ช่วยป้องกันไม่ให้มีการใช้รูปแบบ ER ที่มีการออกแบบที่ยังไม่เสร็จสิ้น อย่างไรก็ตามสำหรับการรันการทดสอบของคุณ คุณสามารถบังคับให้แอปพลิเคชันใช้เวอร์ชันของรูปแบบ ER ของคุณที่มีสถานะเป็น **แบบร่าง** ด้วยวิธีนี้คุณสามารถปรับรุ่นของรูปแบบปัจจุบันถ้าจำเป็นต้องมีการปรับเปลี่ยนใดๆ สำหรับข้อมูลเพิ่มเติม ให้ดูที่ [การใช้งาน](electronic-reporting-destinations.md#applicability)

หากต้องการใช้รุ่นแบบร่างของรูปแบบ ER คุณต้องทำเครื่องหมายรูปแบบ ER ให้ชัดเจน

1. ไปที่ **การจัดการองค์กร** \> **การรายงานทางอิเล็กทรอนิกส์** \> **การตั้งค่าคอนฟิก**
2. ในหน้า **การตั้งค่าคอนฟิก** บนบานหน้าต่างการดำเนินการ บนแท็บ **การตั้งค่าคอนฟิก** ในกลุ่ม **การตั้งค่าล่วงหน้า** เลือก **พารามิเตอร์ผู้ใช้**
3. ในกล่องโต้ตอบ **พารามิเตอร์ผู้ใช้** ให้ตั้งค่าตัวเลือก **เรียกใช้การตั้งค่า** เป็น **ใช่** และจากนั้น เลือก **ตกลง**
4. ให้เลือก **แก้ไข้** เพื่อทำให้หน้าปัจจุบันพร้อมสำหรับการแก้ไข หากจำเป็น
5. ในแผนภูมิการตั้งค่าคอนฟิกในบานหน้าต่างด้านซ้าย ให้เลือก **รายงานอินทราสแทต Litware**
6. ตั้งค่าตัวเลือก **เรียกใช้แบบร่าง** เป็น **ใช่** แล้วจากนั้น เลือก **บันทึก**

    ![รันตัวเลือกแบบร่างบนหน้าการตั้งค่าคอนฟิก](./media/er-paginate-excel-reports-derived-format-configuration.png)

## <a name="set-up-foreign-trade-parameters-to-use-the-custom-er-format"></a>ตั้งค่าพารามิเตอร์การค้าต่างประเทศเพื่อใช้รูปแบบ ER ที่กำหนดเอง

ปฏิบัติตามขั้นตอนต่อไปนี้เพื่อตั้งค่าคอนฟิกพารามิเตอร์การค้าต่างประเทศเพื่อให้คุณสามารถใช้รูปแบบที่กําหนดเองได้

1. ไปที่ **ภาษี** \> **การตั้งค่า** \> **การค้าต่างประเทศ** \> **พารามิเตอร์การค้าต่างประเทศ**
2. บนหน้า **พารามิเตอร์การค้าต่างประเทศ** บนแท็บด่วน **การรายงานทางอิเล็กทรอนิกส์** ในฟิลด์ **การแม็ปรูปแบบไฟล์** เลือก **รายงานอินทราสแทต Litware**
3. ในฟิลด์ **การแม็ปรูปแบบรายงาน** เลือก **รายงานอินทราสแทต Litware**
4. เลือก **บันทึก**

## <a name="configure-the-custom-format-to-use-the-downloaded-report-template"></a>ตั้งค่าคอนฟิกรูปแบบที่กําหนดเองเพื่อใช้แม่แบบรายงานที่ดาวน์โหลด

### <a name="review-the-first-downloaded-excel-template"></a>ทบทวนแม่แบบ Excel ที่ดาวน์โหลดครั้งแรก

1. ในแอพลิเคชันบนเดสก์ท็อปของ Excel ให้เปิดไฟล์แม่แบบ **ERIntrastatReportDemo1.xlsx** ที่คุณดาวน์โหลดก่อนหน้านี้
2. ตรวจสอบว่าแม่แบบมีช่วงที่มีการระบุชื่อเพื่อสร้างส่วนหัวรายงาน รายละเอียดรายงาน และส่วนท้ายของรายงานในเอกสารที่สร้างขึ้น

    ![โครงร่างของแม่แบบ Excel 1 ในแอพลิเคชันบนเดสก์ทอป](./media/er-paginate-excel-reports-template1.gif)

### <a name="replace-the-current-excel-template-in-the-custom-er-format"></a><a id="replace-template"></a>แทนที่แม่แบบ Excel ปัจจุบันในรูปแบบ ER ที่กำหนดเอง

คุณต้องเพิ่มแม่แบบ Excel ใหม่ในรูปแบบ ER ที่กำหนดเอง

1. ไปที่ **การจัดการองค์กร** \> **การรายงานทางอิเล็กทรอนิกส์** \> **การตั้งค่าคอนฟิก**
2. บนหน้า **การตั้งค่าคอนฟิก** ในแผนภูมิการตั้งค่าคอนฟิกในบานหน้าต่างด้านซ้าย ให้ขยาย **แบบจำลองอินทราสแทต** \> **รายงานอินทราสแทต** และเลือกการตั้งค่าคอนฟิก **รายงานอินทราสแทต Litware**
3. เลือก **ตัวออกแบบ**
4. บนหน้า **ตัวออกแบบรูปแบบ** บนบานหน้าต่างการดำเนินการ ให้เลือก **แสดงรายละเอียด**
5. โปรดตรวจสอบให้แน่ใจว่าได้เลือกส่วนประกอบรูปแบบรากของ **อินทราสแทต: Excel** แล้ว ในบานหน้าต่างการดำเนินการ บนแท็บ **นําเข้า** ในกลุ่ม **นําเข้า** ให้เลือก **อัปเดตจาก Excel**
6. ในกล่องโต้ตอบ **อัปเดตจาก Excel** ให้เลือก **อัปเดตแม่แบบ**
7. ในกล่องโต้ตอบ **เปิด** เรียกดูและเลือกไฟล์ **ERIntrastatReportDemo1.xlsx** ที่คุณดาวน์โหลดก่อนหน้านี้ จากนั้นเลือก **เปิด**
8. เลือก **ตกลง**
9. เลือก **บันทึก**

![โครงสร้างรูปแบบตัวออกแบบรูปแบบ ER หลังจากเพิ่มแม่แบบ Excel ใหม่แล้ว](./media/er-paginate-excel-reports-format1.png)

## <a name="change-the-data-binding-to-show-the-item-description-on-a-generated-report"></a>เปลี่ยนการผูกข้อมูลเพื่อแสดงคำอธิบายสินค้าในรายงานที่สร้างขึ้น

1. บนหน้า **ตัวออกแบบรูปแบบ** ให้เลือกแท็บ **การแม็ป**
2. ขยาย **อินทราสแทต** \> **บรรทัดรายงาน** และเลือกส่วนประกอบ **รหัสชุดสินค้า**
3. เลือก **แก้ไขสูตร**
4. เปลี่ยนสูตรที่ผูกไว้จาก `@.CommodityCode` เป็น `CONCATENATE(@.CommodityCode, " ", @.ProductName)`
5. เลือก **บันทึก**

![การผูกข้อมูลที่มีการตั้งค่าคอนฟิกไว้เพื่อแสดงคำอธิบายสินค้าในตัวออกแบบรูปแบบ ER](./media/er-paginate-excel-reports-format1a.png)

## <a name="generate-an-intrastat-declaration-control-report"></a><a id="generate-intrastat-control-report"></a>สร้างรายงานการควบคุมการรายงานภาษีอินทราสแทต

ก่อนอื่น ให้ตรวจสอบให้แน่ใจว่าคุณมีธุรกรรมอินทราสแทตเพื่อการรายงานบนหน้า **อินทราสแทต**

![ธุรกรรมบนหน้าอินทราสแทต](./media/er-paginate-excel-reports-transactions1.gif)

จากนั้นใช้รูปแบบ ER ที่กำหนดเองเพื่อสร้างรายงานการควบคุมของการรายงานภาษีอินทราสแทต

1. ไปที่ **ภาษี** \> **การรายงาน** \> **การค้าต่างประเทศ** \> **อินทราสแทต**
2. บนหน้า **อินทราสแทต** บนบานหน้าต่างการดำเนินการ ให้เลือก **ผลลัพธ์** \> **รายงาน**
3. ในกล่องโต้ตอบ **รายงานอินทราสแทต** ให้ปฏิบัติตามขั้นตอนต่อไปนี้เพื่อเรียกใช้รายงาน:

    1. ตั้งค่าฟิลด์ **วันที่เริ่มต้น** และ **วันที่สิ้นสุด** เพื่อรวมธุรกรรมอินทราสแทตเฉพาะไว้ในรายงาน
    2. ตั้งค่าตัวเลือก **สร้างไฟล์** เป็น **ไม่**
    3. ตั้งค่าตัวเลือก **สร้างรายงาน** เป็น **ใช่**
    4. เลือก **ตกลง**

4. ดาวน์โหลดและบันทึกเอกสารที่สร้างขึ้น
5. เปิดเอกสารใน Excel และตรวจสอบ

    ![เอกสาร Excel ที่สร้างในแอพลิเคชันบนเดสก์ท็อป](./media/er-paginate-excel-reports-document1.png)

## <a name="configure-the-custom-format-to-paginate-generated-documents"></a>ตั้งค่าคอนฟิกรูปแบบที่กําหนดเองเพื่อแบ่งหน้าเอกสารที่สร้าง

### <a name="review-the-second-downloaded-excel-template"></a>ทบทวนแม่แบบ Excel ที่ดาวน์โหลดครั้งที่สอง

1. ใน Excel ให้เปิดไฟล์แม่แบบ **ERIntrastatReportDemo2.xlsx** ที่คุณดาวน์โหลดก่อนหน้านี้
2. เปรียบเทียบแม่แบบนี้กับแม่แบบ **ERIntrastatReportDemo1.xlsx** และตรวจสอบว่าแม่แบบมีชื่อ Excel ใหม่หลายชื่อที่จะสร้างและกรอกข้อมูลในส่วนเฉพาะหน้าในเอกสารที่สร้างขึ้นดังนี้:

    - มีการเพิ่มช่วง **ReportPageHeader** เพื่อสร้างส่วนหัวของหน้า
    - มีการเพิ่มช่วง **ReportPageFooter** เพื่อสร้างส่วนท้ายของหน้า
    - เซลล์ **ReportPageFooter\_PageLines** ได้รับการตั้งค่าคอนฟิกให้แสดงจํานวนธุรกรรมต่อหน้า
    - เซลล์ **ReportPageFooter\_PageAmount** ได้รับการตั้งค่าคอนฟิกให้แสดงจํานวนรวมของธุรกรรมต่อหน้า
    - เซลล์ **ReportPageFooter\_PageWeight** ได้รับการตั้งค่าคอนฟิกให้แสดงน้ำหนักรวมของธุรกรรมต่อหน้า
    - เซลล์ **ReportPageFooter\_RunningCounterLines** ได้รับการตั้งค่าคอนฟิกเพื่อแสดงตัวนับที่กำลังทำงานของธุรกรรมตั้งแต่เริ่มต้นรายงานจนถึงหน้าปัจจุบัน
    - เซลล์ **ReportPageFooter\_RunningTotalAmount** ได้รับการตั้งค่าคอนฟิกเพื่อแสดงจำนวนรวมที่กำลังทำงานของธุรกรรมทั้งหมดตั้งแต่เริ่มต้นรายงานจนถึงหน้าปัจจุบัน
    - เซลล์ **ReportPageFooter\_RunningTotalWeight** ได้รับการตั้งค่าคอนฟิกเพื่อแสดงน้ำหนักรวมที่กำลังทำงานของธุรกรรมตั้งแต่เริ่มต้นรายงานจนถึงหน้าปัจจุบัน

    ![โครงร่างของแม่แบบ Excel 2 ในแอพลิเคชันบนเดสก์ทอป](./media/er-paginate-excel-reports-template2a.gif)

    เซลล์ **CommodityCode** ของแม่แบบนี้ได้รับการตั้งค่าคอนฟิกให้ตัดข้อความของเซลล์ เนื่องจากแถวรายละเอียดธุรกรรมมีการตั้งค่าคอนฟิกไว้เพื่อให้พอดีกับความสูงของแถวโดยอัตโนมัติ ความสูงของทั้งแถวต้องเปลี่ยนโดยอัตโนมัติเมื่อข้อความในเซลล์ **CommodityCode** ถูกตัด

    ![เซลล์ CommodityCode ที่ตั้งค่าคอนฟิกให้ตัดข้อความเซลล์](./media/er-paginate-excel-reports-template2b.gif)

### <a name="repeat-the-replacement-of-the-current-excel-template-in-the-custom-er-format"></a>ทำซ้ำการแทนที่แม่แบบ Excel ปัจจุบันในรูปแบบ ER ที่กำหนดเอง

1. ปฏิบัติตามขั้นตอนในส่วน [แทนที่แม่แบบ Excel ปัจจุบันในรูปแบบ ER ที่กำหนดเอง](#replace-template) ของบทความนี้ อย่างไรก็ตาม ในขั้นตอนที่ 7 ให้เลือกไฟล์ **ERIntrastatReportDemo2.xlsx**
2. บหน้า **ตัวออกแบบรูปแบบ** ขยาย **อินทราสแทต**
3. ตั้งชื่อส่วนประกอบรูปแบบ [ช่วง](er-fillable-excel.md#range-component) ที่ถูกเพิ่มในรูปแบบ ER ที่แก้ไขได้ เพื่อซิงค์โครงสร้างกับโครงสร้างของแม่แบบ Excel ที่ใช้งาน:

    1. เลือกส่วนประกอบ **ช่วง** ที่สัมพันธ์กับชื่อ Excel **ReportPageHeader**
    2. บนแท็บ **รูปแบบ** ในฟิลด์ **ชื่อ** ให้ป้อน **ส่วนหัวของหน้ารายงาน**
    3. เลือกส่วนประกอบ **ช่วง** ที่สัมพันธ์กับชื่อ Excel **ReportPageFooter**
    4. บนแท็บ **รูปแบบ** ในฟิลด์ **ชื่อ** ให้ป้อน **ส่วนท้ายของหน้ารายงาน**

4. เลือก **บันทึก**

![โครงสร้างรูปแบบตัวออกแบบรูปแบบ ER หลังจากแทนที่แม่แบบ Excel แล้ว](./media/er-paginate-excel-reports-format2.png)

### <a name="change-the-format-structure-to-implement-document-pagination"></a>เปลี่ยนโครงสร้างรูปแบบที่จะใช้การแบ่งหน้าเอกสาร

1. บนหน้า **ตัวออกแบบรูปแบบ** ในแผนผังรูปแบบในบานหน้าต่างด้านซ้าย ให้เลือกส่วนประกอบราก **อินทราสแทต**
2. เลือก **เพิ่ม**
3. ในกล่องโต้ตอบ **เพิ่ม** ให้เลือกส่วนประกอบ [หน้า](er-fillable-excel.md#page-component) ในกลุ่ม **Excel** ของส่วนประกอบ
4. ในกล่องโต้ตอบ **คุณสมบัติของส่วนประกอบ** ในฟิลด์ **ชื่อ** ให้ป้อน **หน้ารายงาน** จากนั้น เลือก **ตกลง**
5. เมื่อต้องการใช้ส่วนประกอบ **ส่วนหัวของหน้ารายงาน** เป็นส่วนหัวของหน้าในหน้าที่สร้างขึ้นทุกหน้า ให้ปฏิบัติตามขั้นตอนต่อไปนี้:

    1. เลือกส่วนประกอบ **ส่วนหัวของหน้ารายงาน** และจากนั้นเลือก **ตัด**
    2. เลือกส่วนประกอบ **หน้ารายงาน** และจากนั้นเลือก **วาง**
    3. ขยาย **หน้ารายงาน**
    4. เมื่อต้องการบังคับให้ส่วนประกอบ **หน้า** [พิจารณา](er-fillable-excel.md#page-component-structure) ช่วงนี้ของส่วนหัวของหน้า ให้เลือก **ส่วนหัวของหน้ารายงาน** แล้วบนแท็บ **รูปแบบ** ในฟิลด์ **ทิศทางการจำลองแบบ** ให้เลือก **ไม่มีการจำลองแบบ**

6. เมื่อต้องการแบ่งหน้าเอกสารที่สร้างขึ้นเพื่อให้มีการพิจารณาเนื้อหาในบรรทัดรายงาน ให้ปฏิบัติตามขั้นตอนต่อไปนี้:

    1. เลือกส่วนประกอบ **บรรทัดรายงาน** และจากนั้นเลือก **ตัด**
    2. เลือกส่วนประกอบ **หน้ารายงาน** และจากนั้นเลือก **วาง**

7. เมื่อต้องการรวมส่วนท้ายของรายงานไว้หลังบรรทัดรายงาน แต่อยู่ก่อนหน้าส่วนท้ายของหน้าสุดท้าย ให้ปฏิบัติตามขั้นตอนต่อไปนี้:

    1. เลือกส่วนประกอบ **ส่วนท้ายของรายงาน** และจากนั้นเลือก **ตัด**
    2. เลือกส่วนประกอบ **หน้ารายงาน** และจากนั้นเลือก **วาง**

8. เมื่อต้องการใช้ส่วนประกอบ **ส่วนท้ายของหน้ารายงาน** เป็นส่วนท้ายของหน้าในหน้าที่สร้างขึ้นทุกหน้า ให้ปฏิบัติตามขั้นตอนต่อไปนี้:

    1. เลือกส่วนประกอบ **ส่วนท้ายของหน้ารายงาน** และจากนั้นเลือก **ตัด**
    2. เลือกส่วนประกอบ **หน้ารายงาน** และจากนั้นเลือก **วาง**
    3. เมื่อต้องการบังคับให้ส่วนประกอบ **หน้า** [พิจารณา](er-fillable-excel.md#page-component-structure) ช่วงนี้ของส่วนท้ายของหน้า ให้เลือก **ส่วนท้ายของหน้ารายงาน** แล้วบนแท็บ **รูปแบบ** ในฟิลด์ **ทิศทางการจำลองแบบ** ให้เลือก **ไม่มีการจำลองแบบ**

![โครงสร้างรูปแบบตัวออกแบบรูปแบบ ER หลังจากใช้การแบ่งหน้าเอกสาร](./media/er-paginate-excel-reports-format3.png)

### <a name="add-data-sources-to-calculate-page-footer-totals"></a>เพิ่มแหล่งข้อมูลเพื่อคํานวณผลรวมส่วนท้ายของหน้า

คุณต้องตั้งค่าคอนฟิกแหล่งข้อมูลใหม่เพื่อคํานวณผลรวมของหน้า ตัวนับที่กำลังทำงาน และค่าผลรวมที่กำลังทำงาน และแสดงค่าในส่วนท้ายกระดาษของหน้า ขอแนะนำให้คุณใช้แหล่งข้อมูล [การรวบรวมข้อมูล](er-data-collection-data-sources.md) เพื่อวัตถุประสงค์นี้

1. บนหน้า **ตัวออกแบบรูปแบบ** ให้เลือกแท็บ **การแม็ป**
2. เลือก **เพิ่มราก** แล้วปฏิบัติตามขั้นตอนต่อไปนี้:

    1. ในกล่องโต้ตอบ **เพิ่มแหล่งข้อมูล** ในส่วน **ทั่วไป** ให้เลือก **คอนเทนเนอร์เปล่า**
    2. ในกล่องโต้ตอบ **คุณสมบัติแหล่งข้อมูล 'คอนเทนเนอร์เปล่า'** ในฟิลด์ **ชื่อ** ให้ป้อน **รวม**
    3. เลือก **ตกลง**

3. เลือกแหล่งข้อมูล **รวม** เลือก **เพิ่ม** แล้วปฏิบัติตามขั้นตอนต่อไปนี้:

    1. ในกล่องโต้ตอบ **เพิ่มแหล่งข้อมูล** ในส่วน **ทั่วไป** ให้เลือก **คอนเทนเนอร์เปล่า**
    2. ในกล่องโต้ตอบ **คุณสมบัติแหล่งข้อมูล 'คอนเทนเนอร์เปล่า'** ในฟิลด์ **ชื่อ** ให้ป้อน **หน้า**
    3. เลือก **ตกลง**

4. เลือก **เพิ่ม** อีกครั้ง แล้วปฏิบัติตามขั้นตอนต่อไปนี้

    1. ในกล่องโต้ตอบ **เพิ่มแหล่งข้อมูล** ในส่วน **ทั่วไป** ให้เลือก **คอนเทนเนอร์เปล่า**
    2. ในกล่องโต้ตอบ **คุณสมบัติแหล่งข้อมูล 'คอนเทนเนอร์เปล่า'** ในฟิลด์ **ชื่อ** ให้ป้อน **การรัน**
    3. เลือก **ตกลง**

5. เลือกแหล่งข้อมูล **Total.Page** เลือก **เพิ่ม** แล้วปฏิบัติตามขั้นตอนต่อไปนี้:

    1. ในกล่องโต้ตอบ **เพิ่มแหล่งข้อมูล** ในส่วน **ฟังก์ชัน** ให้เลือก **การรวบรวมข้อมูล**
    2. ในกล่องโต้ตอบ **คุณสมบัติแหล่งข้อมูล 'การรวบรวมข้อมูล'** ในฟิลด์ **ชื่อ** ให้ป้อน **จำนวน**
    3. ในฟิลด์ **ประเภทรายการ** ให้เลือก **จำนวนจริง**
    4. ตั้งค่าตัวเลือก **รวบรวมค่าทั้งหมด** เป็น **ใช่**
    5. เลือก **ตกลง**

6. เลือก **เพิ่ม** อีกครั้ง แล้วปฏิบัติตามขั้นตอนต่อไปนี้

    1. ในกล่องโต้ตอบ **เพิ่มแหล่งข้อมูล** ในส่วน **ฟังก์ชัน** ให้เลือก **การรวบรวมข้อมูล**
    2. ในกล่องโต้ตอบ **คุณสมบัติแหล่งข้อมูล 'การรวบรวมข้อมูล'** ในฟิลด์ **ชื่อ** ให้ป้อน **น้ำหนัก**
    3. ในฟิลด์ **ประเภทรายการ** ให้เลือก **จำนวนจริง**
    4. ตั้งค่าตัวเลือก **รวบรวมค่าทั้งหมด** เป็น **ใช่**
    5. เลือก **ตกลง**

7. เลือกแหล่งข้อมูล **Total.Running** เลือก **เพิ่ม** แล้วปฏิบัติตามขั้นตอนต่อไปนี้:

    1. ในกล่องโต้ตอบ **เพิ่มแหล่งข้อมูล** ในส่วน **ฟังก์ชัน** ให้เลือก **การรวบรวมข้อมูล**
    2. ในกล่องโต้ตอบ **คุณสมบัติแหล่งข้อมูล 'การรวบรวมข้อมูล'** ในฟิลด์ **ชื่อ** ให้ป้อน **จำนวน**
    3. ในฟิลด์ **ประเภทรายการ** ให้เลือก **จำนวนจริง**
    4. ตั้งค่าฟิลด์ **รวบรวมค่าทั้งหมด** เป็น **ใช่**
    5. เลือก **ตกลง**

8. เลือก **เพิ่ม** อีกครั้ง แล้วปฏิบัติตามขั้นตอนต่อไปนี้

    1. ในกล่องโต้ตอบ **เพิ่มแหล่งข้อมูล** ในส่วน **ฟังก์ชัน** ให้เลือก **การรวบรวมข้อมูล**
    2. ในกล่องโต้ตอบ **คุณสมบัติแหล่งข้อมูล 'การรวบรวมข้อมูล'** ในฟิลด์ **ชื่อ** ให้ป้อน **น้ำหนัก**
    3. ในฟิลด์ **ประเภทรายการ** ให้เลือก **จำนวนจริง**
    4. ตั้งค่าฟิลด์ **รวบรวมค่าทั้งหมด** เป็น **ใช่**
    5. เลือก **ตกลง**

9. เลือก **เพิ่ม** อีกครั้ง แล้วปฏิบัติตามขั้นตอนต่อไปนี้

    1. ในกล่องโต้ตอบ **เพิ่มแหล่งข้อมูล** ในส่วน **ฟังก์ชัน** ให้เลือก **การรวบรวมข้อมูล**
    2. ในกล่องโต้ตอบ **คุณสมบัติแหล่งข้อมูล 'การรวบรวมข้อมูล'** ในฟิลด์ **ชื่อ** ให้ป้อน **รายการ**
    3. ในฟิลด์ **ประเภทสินค้า** ให้เลือก **จำนวนเต็ม**
    4. ตั้งค่าฟิลด์ **รวบรวมค่าทั้งหมด** เป็น **ใช่**
    5. เลือก **ตกลง**

10. เลือก **บันทึก**

### <a name="add-data-sources-to-control-page-footer-visibility"></a>เพิ่มแหล่งข้อมูลเพื่อควบคุมความสามารถในการมองเห็นส่วนท้ายของหน้า

ถ้าคุณวางแผนที่จะควบคุมความสามารถในการมองเห็นส่วนท้ายของหน้า และคุณไม่ได้วางแผนจะรวมส่วนท้ายไว้ในหน้าสุดท้ายถ้ามีธุรกรรม ให้ตั้งค่าคอนฟิกแหล่งข้อมูลใหม่เพื่อคํานวณตัวนับที่กำลังทำงานที่ต้องการ

1. บนหน้า **ตัวออกแบบรูปแบบ** ให้เลือกแท็บ **การแม็ป**
2. เลือกแหล่งข้อมูล **Total.Running** ให้เลือก **เพิ่ม**
3. ในกล่องโต้ตอบ **เพิ่มแหล่งข้อมูล** ในส่วน **ฟังก์ชัน** ให้เลือก **การรวบรวมข้อมูล**
4. ในกล่องโต้ตอบ **คุณสมบัติแหล่งข้อมูล 'การรวบรวมข้อมูล'** ในฟิลด์ **ชื่อ** ให้ป้อน **รายการ2**
5. ในฟิลด์ **ประเภทสินค้า** ให้เลือก **จำนวนเต็ม**
6. ตั้งค่าตัวเลือก **รวบรวมค่าทั้งหมด** เป็น **ใช่**
7. เลือก **ตกลง**
8. เลือก **บันทึก**

![แหล่งข้อมูลที่เพิ่มตัวออกแบบรูปแบบ ER](./media/er-paginate-excel-reports-format4.png)

### <a name="configure-bindings-to-collect-total-values"></a>ตั้งค่าคอนฟิกการผูกข้อมูลเพื่อรวบรวมค่ารวม

1. บนหน้า **ตัวออกแบบรูปแบบ** ในแผนผังรูปแบบ ให้ขยายส่วนประกอบ **บรรทัดรายงาน** และเลือกส่วนประกอบ **ค่าใบแจ้งหนี้** ที่ซ้อนกัน
2. เลือก **แก้ไขสูตร**
3. เปลี่ยนสูตรที่ผูกไว้จาก `NUMBERVALUE(NUMBERFORMAT(@.InvoiceValue, "F"&TEXT(model.Parameters.IntrastatAmountDecimals)), ".", "")` เป็น `Total.Page.Amount.Collect(NUMBERVALUE(NUMBERFORMAT(@.InvoiceValue, "F"&TEXT(model.Parameters.IntrastatAmountDecimals)), ".", ""))`

    > [!NOTE]
    > นอกจากการรวมค่าของจํานวนลงในเซลล์ Excel ให้กับทุกธุรกรรมที่มีการรวมแล้ว การผูกข้อมูลนี้จะรวบรวมค่าในแหล่งข้อมูล **Total.Page.Amount** ของการรวบรวมข้อมูล

4. เลือกส่วนประกอบ **น้ำหนัก** ที่ซ้อนกัน
5. เลือก **แก้ไขสูตร**
6. เปลี่ยนสูตรที่ผูกไว้จาก `@.'$RoundedWeight'` เป็น `Total.Page.Weight.Collect(@.'$RoundedWeight')`

    > [!NOTE]
    > นอกจากการรวมค่าของน้ำหนักลงในเซลล์ Excel ให้กับทุกธุรกรรมที่มีการรวมแล้ว การผูกข้อมูลนี้จะรวบรวมค่าในแหล่งข้อมูล **Total.Page.Weight**

![การผูกข้อมูลที่มีการตั้งค่าคอนฟิกไว้เพื่อรวบรวมค่ารวมในตัวออกแบบรูปแบบ ER](./media/er-paginate-excel-reports-format5.png)

### <a name="configure-bindings-to-fill-in-page-footer-totals"></a>ตั้งค่าคอนฟิกการผูกข้อมูลเพื่อกรอกข้อมูลในผลรวมส่วนท้ายของหน้า

1. บนหน้า **ตัวออกแบบรูปแบบ** ในแผนผังรูปแบบ ให้ขยายส่วนประกอบ **ส่วนท้ายของหน้ารายงาน** เลือกส่วนประกอบ **ช่วง** ที่ซ้อนกันซึ่งอ้างอิงถึงเซลล์ **ReportPageFooter\_PageAmount** ของ Excel แล้วปฏิบัติตามขั้นตอนต่อไปนี้:

    1. ในแผนผังแหล่งข้อมูลในบานหน้าต่างด้านขวา ให้เลือกรายการ **Total.Page.Amount.Sum()**
    2. เลือก **ผูก**
    3. เลือก **แก้ไขสูตร**
    4. อัปเดตสูตรเป็น `Total.Page.Amount.Sum(false)`

    > [!NOTE]
    > คุณต้องระบุอาร์กิวเมนต์ของฟังก์ชันนี้เป็น **เท็จ** เพื่อเก็บข้อมูลที่รวบรวมไว้ของหน้าปัจจุบัน เนื่องจากข้อมูลนี้ต้องใช้เพื่อคํานวณจํานวนที่กำลังทำงานทั้งหมด จํานวนรวมของบรรทัดต่อหน้า และตัวนับของบรรทัดที่กำลังทำงานอยู่

2. ในแผนผังรูปแบบ ให้เลือกส่วนประกอบ **ช่วง** ที่ซ้อนกัน ซึ่งอ้างอิงถึงเซลล์ **ReportPageFooter\_PageWeight** ของ Excel แล้วปฏิบัติตามขั้นตอนต่อไปนี้:

    1. ในแผนผังแหล่งข้อมูลในบานหน้าต่างด้านขวา ให้เลือกรายการ **Total.Page.Weight.Sum()**
    2. เลือก **ผูก**
    3. เลือก **แก้ไขสูตร**
    4. อัปเดตสูตรเป็น `Total.Page.Weight.Sum(false)`

### <a name="configure-bindings-to-fill-in-page-running-totals"></a>ตั้งค่าคอนฟิกการผูกข้อมูลเพื่อกรอกข้อมูลในผลรวมการทำงานของหน้า

1. บนหน้า **ตัวออกแบบรูปแบบ** ในแผนผังรูปแบบ ให้ขยายส่วนประกอบ **ส่วนท้ายของหน้ารายงาน** เลือกส่วนประกอบ **ช่วง** ที่ซ้อนกันซึ่งอ้างอิงถึงเซลล์ **ReportPageFooter\_RunningTotalAmount** ของ Excel แล้วปฏิบัติตามขั้นตอนต่อไปนี้:

    1. ในแผนผังแหล่งข้อมูลในบานหน้าต่างด้านขวา ให้เลือกรายการ **Total.Running.Amount.Collect()**
    2. เลือก **ผูก**
    3. เลือก **แก้ไขสูตร**
    4. อัปเดตสูตรเป็น `Total.Running.Amount.Sum(false)+Total.Running.Amount.Collect(Total.Page.Amount.Sum(true))`

    > [!NOTE]
    > ตัวถูกดำเนินการ `Total.Running.Amount.Sum(false)` ถูกส่งคืนผลรวมการทำงานของจำนวนที่รวบรวมก่อนหน้านี้ ตัวถูกดำเนินการ `Total.Running.Amount.Collect(Total.Page.Amount.Sum(true))` ถูกส่งคืนผลรวมของหน้าปัจจุบัน คุณต้องระบุอาร์กิวเมนต์ของฟังก์ชันที่ซ้อนกันของตัวถูกดำเนินการที่สองเป็น **จริง** เพื่อรีเซ็ตการรวบรวมข้อมูล `Total.Page.Amount` ทันทีที่ค่านี้อยู่ในการรวบรวมข้อมูล `Total.Running.Amount` รวมที่ทำงานอยู่ อาร์กิวเมนต์ที่ระบุต้องเริ่มต้นรวบรวมผลรวมของหน้าถัดไปจากค่า 0 (ศูนย์)
    >
    > ฟังก์ชัน `Total.Running.Amount.Sum(false)` ถูกเรียกใช้เพื่อป้อนจำนวนรวมที่ทำงานในเซลล์ **ReportPageFooter\_RunningTotalAmount** ของ Excel ในหน้าปัจจุบัน

2. ในแผนผังรูปแบบ ให้เลือกส่วนประกอบ **ช่วง** ที่ซ้อนกัน ซึ่งอ้างอิงถึงเซลล์ **ReportPageFooter\_RunningTotalWeight** ของ Excel แล้วปฏิบัติตามขั้นตอนต่อไปนี้:

    1. ในแผนผังแหล่งข้อมูลในบานหน้าต่างด้านขวา ให้เลือกรายการ **Total.Running.Weight.Collect()**
    2. เลือก **ผูก**
    3. เลือก **แก้ไขสูตร**
    4. อัปเดตสูตรเป็น `Total.Running.Weight.Sum(false)+Total.Running.Weight.Collect(Total.Page.Weight.Sum(true))`

### <a name="configure-bindings-to-fill-in-the-page-running-counter"></a>ตั้งค่าคอนฟิกการผูกข้อมูลเพื่อกรอกข้อมูลในตัวนับการทำงานของหน้า

1. บนหน้า **ตัวออกแบบรูปแบบ** ในแผนผังรูปแบบ ให้ขยายส่วนประกอบ **ส่วนท้ายของหน้ารายงาน** และเลือกส่วนประกอบ **ช่วง** ที่ซ้อนกันซึ่งอ้างอิงถึงเซลล์ **ReportPageFooter\_RunningCounterLines** ของ Excel
2. เลือก **แก้ไขสูตร**
3. เพิ่มสูตร `Total.Running.Lines.Collect(COUNT(Total.Page.Amount.Result))`

    > [!NOTE]
    > สูตรนี้จะส่งคืนจํานวนที่รวบรวมไว้ของทั้งรายงาน จํานวนนี้จะเท่ากับจํานวนธุรกรรมที่มีการรวมในขณะนี้ ในขณะเดียวกัน สูตรจะรวบรวมค่าที่ส่งคืนในการรวบรวม **Total.Running.Lines**

### <a name="configure-bindings-to-fill-in-the-page-footer-counter"></a>ตั้งค่าคอนฟิกการผูกข้อมูลเพื่อกรอกข้อมูลในตัวนับส่วนท้ายของหน้า

1. บนหน้า **ตัวออกแบบรูปแบบ** ในแผนผังรูปแบบ ให้ขยายส่วนประกอบ **ส่วนท้ายของหน้ารายงาน** และเลือกส่วนประกอบ **ช่วง** ที่ซ้อนกันซึ่งอ้างอิงถึงเซลล์ **ReportPageFooter\_PageLines** ของ Excel
2. เลือก **แก้ไขสูตร**
3. เพิ่มสูตร `COUNT(Total.Page.Amount.Result)-Total.Running.Lines.Sum(false)`

    > [!NOTE]
    > สูตรนี้จะคํานวณจํานวนธุรกรรมในหน้าปัจจุบันเป็นผลต่างระหว่างจํานวนธุรกรรมที่รวบรวมใน **Total.Page.Amount.Result** สำหรับทั้งรายงานและจํานวนของธุรกรรมที่จัดเก็บในขั้นนี้ใน **Total.Running.Lines.Sum** เนื่องจากจํานวนธุรกรรมของหน้าปัจจุบันจัดเก็บอยู่ใน **Total.Running.Lines** ในการผูกข้อมูลของส่วนประกอบ **ช่วง** ที่อ้างอิงถึงเซลล์ **ReportPageFooter\_RunningCounterLines** ของ Excel จํานวนธุรกรรมในหน้าปัจจุบันยังไม่ได้รวมไว้ ดังนั้น ผลต่างนี้จะเท่ากับจํานวนของธุรกรรมในหน้าปัจจุบัน

![การผูกข้อมูลที่มีการตั้งค่าคอนฟิกไว้เพื่อกรอกข้อมูลในตัวนับส่วนท้ายของหน้าในตัวออกแบบรูปแบบ ER](./media/er-paginate-excel-reports-format6.png)

### <a name="configure-component-visibility"></a>ตั้งค่าคอนฟิกความสามารถในการมองเห็นของส่วนประกอบ

คุณสามารถเปลี่ยนความสามารถในการมองเห็นของส่วนหัวและส่วนท้ายของหน้าเฉพาะของเอกสารที่สร้างขึ้นเพื่อซ่อนองค์ประกอบต่อไปนี้:

- ส่วนหัวของหน้าในหน้าแรก เนื่องจากส่วนหัวของรายงานมีชื่อคอลัมน์อยู่แล้ว
- ส่วนหัวของหน้าในหน้าใดๆ ที่ไม่มีธุรกรรมซึ่งอาจเกิดขึ้นได้กับหน้าสุดท้าย
- ส่วนท้ายของหน้าในหน้าใดๆ ที่ไม่มีธุรกรรมซึ่งอาจเกิดขึ้นได้กับหน้าสุดท้าย

เมื่อต้องการเปลี่ยนแปลงความสามารถในการมองเห็น ให้อัปเดตคุณสมบัติ **เปิดใช้งาน** ของส่วนประกอบ **ส่วนหัวของหน้ารายงาน** และ **ส่วนท้ายของหน้ารายงาน**

1. บนหน้า **ตัวออกแบบรูปแบบ** ในแผนผังรูปแบบ ให้ขยายส่วนประกอบ **หน้ารายงาน** เลือกส่วนประกอบ **ส่วนหัวของหน้ารายงาน** แล้วปฏิบัติตามขั้นตอนเหล่านี้:

    1. เลือก **แก้ไข** เฉพาะฟิลด์ **ที่เปิดใช้งาน**
    2. ในหน้า **ตัวออกแบบสูตร** ในฟิลด์ **สูตร** ให้ป้อนนิพจน์ต่อไปนี้:

        `AND(`<br>
        `COUNT(Total.Page.Amount.Result)<>0,`<br>
        `COUNT(Total.Page.Amount.Result)<>COUNT(model.CommodityRecord)`<br>
        `)`

2. ในแผนผังรูปแบบ เลือกส่วนประกอบ **ส่วนท้ายของหน้ารายงาน** ที่ซ้อนกัน แล้วปฏิบัติตามขั้นตอนต่อไปนี้:

    1. เลือก **แก้ไข** เฉพาะฟิลด์ **ที่เปิดใช้งาน**
    2. ในหน้า **ตัวออกแบบสูตร** ในฟิลด์ **สูตร** ให้ป้อนนิพจน์ต่อไปนี้:

        `(`<br>
        `COUNT(Total.Page.Amount.Result)-Total.Running.Lines2.Sum(false)+`<br>
        `0*Total.Running.Lines2.Collect(COUNT(Total.Page.Amount.Result))`<br>
        `)<>0`

    > [!NOTE]
    > การจัดทำ `COUNT(Total.Page.Amount.Result)-Total.Running.Lines2.Sum(false)` ใช้ในการคํานวณจํานวนธุรกรรมบนหน้าปัจจุบัน การจัดทำ `0*Total.Running.Lines2.Collect(COUNT(Total.Page.Amount.Result)` จะใช้เพื่อเพิ่มจํานวนธุรกรรมในหน้าปัจจุบันไปยังการรวบรวม เพื่อจัดการกับความสามารถในการมองเห็นของส่วนท้ายของหน้าถัดไปอย่างถูกต้อง
    >
    > การรวบรวม `Total.Running.Lines` ไม่สามารถใช้อีกครั้งที่นี่ได้ เนื่องจากคุณสมบัติ **เปิดใช้งาน** ของส่วนประกอบพื้นฐานจะได้รับการประมวลผล **หลังจาก** ประมวลผลการผูกส่วนประกอบที่ซ้อนกัน เมื่อประมวลผลคุณสมบัติ **เปิดใช้งาน** การรวบรวม `Total.Running.Lines` จะเพิ่มขึ้นตามจํานวนธุรกรรมในหน้าปัจจุบัน

3. เลือก **บันทึก**

## <a name="generate-an-intrastat-declaration-control-report-updated"></a>สร้างรายงานการควบคุมการรายงานภาษีอินทราสแทต (อัปเดต)

1. ให้ตรวจสอบให้แน่ใจว่าคุณมี 24 ธุรกรรมบนหน้า **อินทราสแทต** ทำซ้ำขั้นตอนในส่วน [สร้างรายงานการควบคุมการรายงานภาษีอินทราสแทต](#generate-intrastat-control-report) ของบทความนี้ เพื่อสร้างและตรวจสอบรายงานการควบคุม

    ธุรกรรมทั้งหมดจะแสดงอยู่ในหน้าแรก ผลรวมของหน้าและตัวนับจะเท่ากับผลรวมของรายงานและตัวนับ ช่วงของส่วนหัวของหน้าถูกซ่อนในหน้าแรก เนื่องจากส่วนหัวของรายงานมีชื่อคอลัมน์อยู่แล้ว ส่วนหัวและส่วนท้ายของหน้าถูกซ่อนในหน้าที่สอง เนื่องจากหน้านั้นไม่มีธุรกรรม

    ![เอกสาร Excel ที่สร้างในแอพลิเคชันบนเดสก์ท็อป](./media/er-paginate-excel-reports-document2.gif)

2. อัปเดตธุรกรรมสองรายการในหน้า **อินทราสแทต** ด้วยการเปลี่ยนรหัส **หมายเลขสินค้า** จาก **D00006** เป็น **L0010** โปรดสังเกตว่าชื่อผลิตภัณฑ์ของสินค้าใหม่ **ลําโพงสเตอริโอคู่ที่ใช้งานอยู่** ยาวกว่าชื่อผลิตภัณฑ์ของสินค้าเดิม **ลําโพงมาตรฐาน** สถานการณ์นี้จะบังคับให้ข้อความถูกตัดในเซลล์ที่สอดคล้องกันของเอกสารที่สร้างขึ้น ขณะนี้ต้องอัปเดตการแบ่งหน้าเอกสาร และการรวมและการตรวจนับที่เกี่ยวข้องกับหน้า ทำซ้ำขั้นตอนในส่วน [สร้างรายงานการควบคุมการรายงานภาษีอินทราสแทต](#generate-intrastat-control-report) เพื่อสร้างและตรวจสอบรายงานการควบคุม

    ปัจจุบัน มีการแสดงธุรกรรมบนหน้าสองหน้า และคํานวณผลรวมของหน้าและตัวนับอย่างถูกต้อง ช่วงของส่วนหน้าถูกซ่อนอย่างถูกต้องในหน้าแรกและมองเห็นได้ในหน้าที่สอง ส่วนท้ายของหน้าจะมองเห็นได้ทั้งสองหน้า เนื่องจากมีธุรกรรมอยู่

    ![เอกสาร Excel ที่อัปเดตในแอพลิเคชันบนเดสก์ท็อป](./media/er-paginate-excel-reports-document3.gif)

## <a name="frequently-asked-questions"></a>คำถามที่ถามบ่อย

### <a name="is-there-any-way-to-recognize-when-the-final-page-is-processed-by-the-page-format-component"></a>จะมีวิธีที่รับรู้เมื่อประมวลผลหน้าสุดท้ายโดยส่วนประกอบรูปแบบหน้าหรือไม่

ส่วนประกอบ **หน้า** [ไม่แสดง](er-fillable-excel.md#page-component-limitations) ข้อมูลเกี่ยวกับจํานวนของหน้าที่ประมวลผลและจํานวนทั้งหมดของหน้าในเอกสารที่สร้างขึ้น อย่างไรก็ตาม คุณสามารถตั้งค่าคอนฟิก [สูตร](er-formula-language.md) ER เพื่อรับรู้หน้าสุดท้ายได้ นี่คือตัวอย่าง:

- คํานวณจํานวนธุรกรรมรวมที่ประมวลผลแล้วโดยใช้ส่วนประกอบ **หน้ารายงาน** คุณสามารถทำการคำนวณนี้ได้โดยใช้สูตร `COUNT(Total.Page.Amount.Result)` 
- คํานวณจํานวนรวมของธุรกรรมที่ต้องประมวลผลตามการผูกข้อมูล `model.CommodityRecord` ที่ตั้งค่าคอนฟิกไว้สำหรับส่วนประกอบ **บรรทัดรายงาน** คุณสามารถทำการคำนวณนี้ได้โดยใช้สูตร `COUNT(model.CommodityRecord)`
- เปรียบเทียบตัวเลขสองตัวเพื่อรับรู้หน้าสุดท้าย เมื่อค่าทั้งสองมีค่าเท่ากัน หน้าสุดท้ายจะถูกสร้างขึ้น

> [!NOTE]
> ขอแนะนำให้คุณใช้วิธีการนี้เฉพาะเมื่อคุณสมบัติ **เปิดใช้งาน** ของส่วนประกอบ **บรรทัดรายงาน** ไม่มีสูตรใดที่อาจส่งคืนค่า [เท็จ](er-formula-supported-data-types-primitive.md#boolean) ขณะรันไทม์ของบาง [เรกคอร์ด](er-formula-supported-data-types-composite.md#record) ที่รวมของ [รายการเรกคอร์ด](er-formula-supported-data-types-composite.md#record-list) ที่ผูกไว้

## <a name="additional-resources"></a>ทรัพยากรเพิ่มเติม

- [ออกแบบการตั้งค่าคอนฟิกสำหรับการสร้างเอกสารในรูปแบบ Excel](er-fillable-excel.md)
- [ใช้แหล่งข้อมูล DATA COLLECTION ในรูปแบบการรายงานทางอิเล็กทรอนิกส์ (ER)](er-data-collection-data-sources.md)

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
