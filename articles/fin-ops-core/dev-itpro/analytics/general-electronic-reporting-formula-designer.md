---
title: โปรแกรมออกแบบสูตรในการรายงานทางอิเล็กทรอนิกส์ (ER)
description: หัวข้อนี้แสดงข้อมูลเกี่ยวกับวิธีการใช้โปรแกรมออกแบบสูตรในการรายงานทางอิเล็กทรอนิกส์ (ER)
author: NickSelin
manager: kfend
ms.date: 12/05/2019
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
ms.openlocfilehash: d96fe041fd0ffb292909c1e724068efebe0184b9
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 12/05/2020
ms.locfileid: "4682660"
---
# <a name="formula-designer-in-electronic-reporting-er"></a>โปรแกรมออกแบบสูตรในการรายงานทางอิเล็กทรอนิกส์ (ER)

[!include [banner](../includes/banner.md)]

หัวข้อนี้อธิบายวิธีการใช้โปรแกรมออกแบบสูตรในรายงานอิเล็กทรอนิกส์ (ER) เมื่อคุณออกแบบรูปแบบสำหรับเอกสารอิเล็กทรอนิกส์เฉพาะใน ER คุณสามารถใช้สูตรเพื่อแปลงข้อมูล เพื่อให้ตรงกับความต้องการสำหรับการเติมสินค้าและการจัดรูปแบบของเอกสาร สูตรเหล่านี้คล้ายกับสูตรใน Microsoft Excel ฟังก์ชันชนิดต่างๆ ได้รับการสนับสนุนในสูตร: ข้อความ วันที่และเวลา เชิงคณิตศาสตร์ เชิงตรรกะ ข้อมูล และฟังก์ชันการแปลงชนิดข้อมูล และฟังก์ชันเฉพาะโดเมนธุรกิจอื่นๆ อีกด้วย

## <a name="formula-designer-overview"></a>ภาพรวมผู้ออกแบบสูตร

ER สนับสนุนผู้ออกแบบสูตร ดังนั้น ในขณะออกแบบ คุณสามารถตั้งค่าคอนฟิกนิพจน์ที่สามารถใช้สำหรับงานต่อไปนี้ขณะรันไทม์ได้:

- แปลงข้อมูลที่ได้รับจากฐานข้อมูลของแอพลิเคชั่น และที่ควรถูกป้อนลงในแบบจำลองข้อมูล ER ที่ถูกออกแบบให้เป็นแหล่งข้อมูลสำหรับรูปแบบ ER (ตัวอย่างเช่น การแปลงเหล่านี้อาจมีการกรอง การจัดกลุ่ม และการแปลงชนิดข้อมูล)
- ข้อมูลรูปแบบที่ต้องส่งให้เอกสารอิเล็กทรอนิกส์ที่สร้างสอดคล้องกับโครงร่างและเงื่อนไขของรูปแบบ ER ที่ระบุ (ตัวอย่างเช่น การจัดรูปแบบอาจถูกทำให้สอดคล้องกับภาษาหรือวัฒนธรรมที่ร้องขอ หรือการเข้ารหัส)
- ควบคุมกระบวนการสร้างเอกสารอิเล็กทรอนิกส์ (ตัวอย่างเช่น นิพจน์สามารถเปิดหรือปิดใช้งานการแสดงผลขององค์ประกอบที่เฉพาะเจาะจงของรูปแบบ โดยขึ้นอยู่กับข้อมูลการประมวลผล พวกเขายังสามารถขัดจังหวะกระบวนการสร้างเอกสาร หรือส่งข้อความไปยังผู้ใช้ได้ด้วย)

คุณสามารถเปิดหน้า **โปรแกรมออกแบบสูตร** ได้ เมื่อคุณทำการดำเนินการอย่างใดอย่างหนึ่งต่อไปนี้:

- ผูกรายการแหล่งข้อมูลให้ส่วนประกอบของแบบจำลองข้อมูล
- ผูกรายการแหล่งข้อมูลให้ส่วนประกอบของรูปแบบ
- ทำการบำรุงรักษาฟิลด์ที่คำนวณได้ซึ่งเป็นส่วนหนึ่งของแหล่งข้อมูลให้เสร็จสมบูรณ์
- กำหนดเงื่อนไขที่มองเห็นได้สำหรับพารามิเตอร์การป้อนของผู้ใช้
- ออกแบบการแปลงรูปแบบ
- กำหนดการเปิดใช้งานเงื่อนไขสำหรับส่วนประกอบของรูปแบบ
- กำหนดชื่อไฟล์สำหรับส่วนประกอบรูปแบบ FILE
- กำหนดเงื่อนไขสำหรับการตรวจสอบการควบคุมกระบวนการ
- กำหนดข้อความอักษรสำหรับการตรวจสอบการควบคุมกระบวนการ

## <a name="data-binding"></a><a name="Binding"></a>การรวมข้อมูล

โปรแกรมออกแบบสูตร ER สามารถถูกใช้เพื่อกำหนดนิพจน์ที่แปลงข้อมูลที่ได้รับจากแหล่งข้อมูลได้ เพื่อให้สามารถป้อนข้อมูลในผู้ใช้ข้อมูลในวิธีต่อไปนี้ที่รันไทม์:

- จากแหล่งข้อมูลของแอพพลิเคชั่นและเวลาการดำเนินงานของพารามิเตอร์เป็นแบบจำลองข้อมูล ER
- จากแบบจำลองข้อมูล ER เป็นรูปแบบ ER
- จากแหล่งข้อมูลของแอพพลิเคชั่นและเวลาการดำเนินงานของพารามิเตอร์เป็นรูปแบบ ER

ภาพต่อไปนี้แสดงการออกแบบนิพจน์ชนิดนี้ ในตัวอย่างนี้ นิพจน์ปัดเศษค่าของฟิลด์ **Intrastat.AmountMST** ในตาราง Intrastat เป็นทศนิยมสองตำแหน่ง และจากนั้น ส่งคืนค่าที่ถูกปัดเศษ

[![นิพจน์การผูกข้อมูล](./media/picture-expression-binding.jpg)](./media/picture-expression-binding.jpg)

ภาพต่อไปนี้แสดงวิธีการใช้นิพจน์ของชนิดนี้ ในตัวอย่างนี้ ผลลัพธ์ของนิพจน์ที่ได้รับการออกแบบจะถูกป้อนในส่วนประกอบ **Transaction.InvoicedAmount** ของแบบจำลองข้อมูล **แบบจำลองการรายงานภาษี**

[![มีการใช้นิพจน์การผูกข้อมูล](./media/picture-expression-binding2.jpg)](./media/picture-expression-binding2.jpg)

ในช่วงรันไทม์ สูตรที่ได้รับการออกแบบ `ROUND (Intrastat.AmountMST, 2)` ปัดเศษค่าของฟิลด์ **AmountMST** สำหรับแต่ละเรกคอร์ดในตารางอินทราสแทตเป็นทศนิยมสองตำแหน่ง จากนั้นจะป้อนค่าที่ปัดเศษในส่วนประกอบ **Transaction.InvoicedAmount** ของแบบจำลองข้อมูล **การรายงานภาษี**

## <a name="data-formatting"></a><a name="Transformation"></a>การจัดรูปแบบข้อมูล

ผู้ออกแบบสูตร ER สามารถใช้เพื่อกำหนดนิพจน์ที่แปลงรูปแบบข้อมูลที่ได้รับจากแหล่งข้อมูล เพื่อให้สามารถส่งข้อมูลเป็นเอกสารอิเล็กทรอนิกส์ คุณอาจมีการจัดรูปแบบที่ต้องใช้ ตามกฎทั่วไปที่ควรนำมาใช้ใหม่สำหรับรูปแบบ ในกรณีนี้ คุณสามารถแนะนำให้การจัดรูปแบบครั้งเดียวในการตั้งค่าคอนฟิกรูปแบบ เป็นการแปลงที่มีการตั้งชื่อที่มีนิพจน์การจัดรูปแบบ การแปลงข้อมูลที่มีการตั้งชื่อนี้สามารถเชื่อมโยงกับองค์ประกอบรูปแบบหลายองค์ประกอบ ที่ซึ่งผลลัพธ์ต้องถูกจัดรูปแบบตามนิพจน์การจัดรูปแบบทีคุณสร้างไว้

ภาพต่อไปนี้แสดงการออกแบบการแปลงชนิดนี้ ในตัวอย่างนี้ การแปลง **TrimmedString** ตัดทอนข้อมูลขาเข้าของชนิดข้อมูล *สตริง* โดยการลบช่องว่างนำหน้าและต่อท้าย จากนั้น จะส่งกลับค่าสตริงที่ถูกตัดทอนแล้ว

[![การแปลงข้อมูล](./media/picture-transformation-design.jpg)](./media/picture-transformation-design.jpg)

ภาพต่อไปนี้แสดงการใช้การแปลงชนิดนี้ ในตัวอย่างนี้ ส่วนประกอบของรูปแบบต่างๆ ส่งข้อความเป็นเอาท์พุตไปยังเอกสารอิเล็กทรอนิกส์ที่สร้างในช่วงรันไทม์ ส่วนประกอบรูปแบบเหล่านี้ทั้งหมดอ้างอิงถึงการแปลง **TrimmedString** ตามชื่อ

[![มีการใช้การแปลง](./media/picture-transformation-usage.jpg)](./media/picture-transformation-usage.jpg)

เมื่อส่วนประกอบของรูปแบบ เช่น ส่วนประกอบ **partyName** ในแผนภาพก่อนหน้านี้ อ้างอิงถึงการแปลง **TrimmedString** การแปลงจะส่งข้อความเป็นเอาท์พุตไปยังเอกสารอิเล็กทรอนิกส์ที่มีการสร้าง ข้อความนี้ไม่รวมช่องว่างนำหน้าและต่อท้าย

ถ้าคุณมีการจัดรูปแบบที่จำเป็นต้องใช้แต่ละรายการ คุณสามารถนำรูปแบบไปใช้เพื่อเป็นนิพจน์ของการผูกข้อมูลของส่วนประกอบรูปเฉพาะแบบแต่ละรายการได้ ภาพต่อไปนี้แสดงนิพจน์ชนิดนี้ ในตัวอย่างนี้ ส่วนประกอบรูปแบบ **partyType** ถูกผูกไว้กับแหล่งข้อมูลผ่านนิพจน์ที่แปลงข้อมูลขาเข้าจากฟิลด์ **Model.Company.RegistrationType** ในแหล่งข้อมูลเป็นข้อความตัวพิมพ์ใหญ่ แล้วนิพจน์จะส่งข้อความนั้นเป็นเอาท์พุตไปยังเอกสารอิเล็กทรอนิกส์

[![การใช้การจัดรูปแบบกับส่วนประกอบแต่ละรายการ](./media/picture-binding-with-formula.jpg)](./media/picture-binding-with-formula.jpg)

## <a name="process-flow-control"></a><a name="Validation"></a>กระบวนการควบคุมขั้นตอน

โปรแกรมออกแบบสูตร ER สามารถใช้เพื่อกำหนดนิพจน์ที่ควบคุมขั้นตอนกระบวนการของเอกสารอิเล็กทรอนิกส์ที่สร้าง: คุณสามารถจัดการงานต่อไปนี้

- เงื่อนไขที่กำหนดเมื่อกระบวนการสร้างเอกสารต้องถูกหยุด
- ระบุนิพจน์ที่จะสร้างข้อความสำหรับผู้ใช้เกี่ยวกับกระบวนการที่หยุด หรือส่งข้อความล็อกการดำเนินการเกี่ยวกับกระบวนการสร้างรายงานต่อเนื่อง อย่างใดอย่างหนึ่ง
- ระบุชื่อไฟล์ของการสร้างเอกสารอิเล็กทรอนิกส์ และควบคุมเงื่อนไขของการสร้างของพวกเขา

กฏแต่ละกฏของการควบคุมขั้นตอนการประมวลผลถูกออกแบบให้เป็นการตรวจสอบเดี่ยว ภาพต่อไปนี้แสดงการตรวจสอบความถูกต้องชนิดนี้ นี่เป็นคำอธิบายเกี่ยวกับการตั้งค่าคอนฟิกในตัวอย่างนี้:

- การตรวจสอบถูกประเมิน เมื่อโหนด **INSTAT** ถูกสร้างในระหว่างการสร้างไฟล์ XML
- เมื่อรายการธุรกรรมว่างเปล่าs การการประมวลผลจะหยุดการดำเนินและส่งกลับค่า **FALSE**
- การตรวจสอบส่งคืนข้อผิดพลาดที่มีข้อความของป้ายชื่อ SYS70894 ในภาษาที่ผู้ใช้ต้องการ

[![การตรวจสอบความถูกต้อง](./media/picture-validation.jpg)](./media/picture-validation.jpg)

นอกจากนี้ โปรแกรมออกแบบสูตร ER ยังสามารถใช้เพื่อสร้างชื่อไฟล์สำหรับเอกสารทางอิเล็กทรอนิกส์ที่สร้าง และเพื่อควบคุมกระบวนการสร้างไฟล์อีกด้วย ภาพต่อไปนี้แสดงกฏของการควบคุมขั้นตอนการประมวลผลชนิดนี้ นี่เป็นคำอธิบายเกี่ยวกับการตั้งค่าคอนฟิกในตัวอย่างนี้:

- รายการของเรกคอร์ดจากแหล่งข้อมูล **แบบจำลอง.อินทราสแทต** ถูกแบ่งออกเป็นชุดงาน ชุดงานแต่ละชุดประกอบด้วยเรกคอร์ดได้มากถึง 1000 รายการ
- ผลลัพธ์สร้างไฟล์ zip ที่ประกอบด้วยไฟล์หนึ่งไฟล์ในรูปแบบ XML สำหรับชุดงานทั้งหมดที่สร้างขึ้น
- นิพจน์ส่งกลับชื่อไฟล์สำหรับการสร้างเอกสารอิเล็กทรอนิกส์โดยการเชื่อมชื่อไฟล์และนามสกุลไฟล์ สำหรับชุดงานที่สองและชุดงานในลำดับต่อมาทั้งหมด ชื่อไฟล์จะประกอบด้วยรหัสชุดงานเป็นคำต่อท้าย
- นิพจน์เปิดใช้งาน (โดยการคืนค่า **จริง**) กระบวนการสร้างไฟล์ สำหรับชุดงานซึ่งประกอบด้วยอย่างน้อยหนึ่งเรกคอร์ด

[![กระบวนการควบคุมขั้นตอน](./media/picture-file-control.jpg)](./media/picture-file-control.jpg)

## <a name="document-content-control"></a><a name="Enabled"></a> การควบคุมเนื้อหาเอกสาร

โปรแกรมออกแบบสูตร ER สามารถใช้เพื่อตั้งค่าคอนฟิกนิพจน์ซึ่งควบคุมว่าข้อมูลจะถูกวางในเอกสารอิเล็กทรอนิกส์ที่สร้างในขณะรันไทม์ นิพจน์สามารถเปิด หรือปิดใช้งานกผลลัพธ์ขององค์ประกอบเฉพาะของรูปแบบ ขึ้นอยู่กับการประมวลผลข้อมูล เเละตรรกะคอนฟิก นิพจน์เหล่านี้สามารถป้อนสำหรับองค์ประกอบรูปแบบเดียวในฟิล์ด์ **ที่เปิดใช้งาน** บนเเท็บ **การเเม็บ** ของหน้า **ผู้ออกเเบบการดำเนินการ** คุณสามารถป้อนนิพจน์เป็นเงื่อนไขตรรกะที่ส่งกลับค่า *บูลีน*:

- ถ้าเงื่อนไขส่งกลับค่า **จริง** องค์ประกอบรูปแบบปัจจุบันจะถูกเรียกใช้
- ถ้าเงื่อนไขส่งกลับค่า **เท็จ** องค์ประกอบรูปแบบปัจจุบันจะถูกข้าม

ภาพประกอบต่อไปนี้แสดงนิพจน์ของชนิดนี้ (รุ่น11.12.11 ของการตั้งค่าคอนฟิกรูปแบบ **ISO20022 การโอนย้ายเครดิต (ไม่)** ที่ให้ไว้โดย Microsoft จะถูกใช้เป็นตัวอย่าง) ส่วนประกอบรูปแบบ **XMLHeader** ถูกตั้งค่าคอนฟิกเพื่ออธิบายโครงสร้างของข้อความการโอนย้ายเครดิตตามมาตรฐาน ISO 20022 ข้อความ XML ส่วนประกอบของรูปแบบ **XMLHeader/Document/CstmrCdtTrfInitn/PmtInf/CdtTrfTxInf/RmtInf/Ustrd** ถูกตั้งค่าคอนฟิกเพื่อเพิ่มองค์ประกอบ XML **Ustrd** ไปยังข้อความที่สร้าง เเละวางข้อมูลการชำระเงินในรูปแบบที่ไม่มีโครงสร้างเป็นข้อความขององค์ประกอบ XML ต่อไปนี้:

- ส่วนประกอบ **PaymentNotes** ถูกใช้ในการสร้างข้อความของบันทึกการชำระเงิน
- ส่วนประกอบ **DelimitedSequence** สร้างหมายเลขใบเเจ้งหนี้ที่แบ่งด้วยเครื่องหมายจุลภาค ซึ่งถูกใช้ในการชำระการโอนย้ายเครดิตปัจจุบัน

[![ส่วนประกอบของ PaymentNotes และ DelimitedSequence](./media/GER-FormulaEditor-ControlContent-1.png)](./media/GER-FormulaEditor-ControlContent-1.png)

> [!NOTE]
> ส่วนประกอบ **PaymentNotes** เเละ **DelimitedSequence** จะมีการกำกับชื่อโดยใช้เครื่องหมายคำถาม เครื่องหมายคำถามบ่งชี้ว่าการใช้ส่วนประกอบมีเงื่อนไข ในกรณีนี้ การใช้ส่วนประกอบจะขึ้นอยู่กับเงื่อนไขต่อไปนี้:
>
> - นิพจน์ `@.PaymentsNotes <> ""` ที่ถูกกำหนดสำหรับส่วนประกอบของ **PaymentNotes** เปิดใช้งาน (โดยส่งคืนค่า **จริง**) องค์ประกอบ XML ของ **Ustrd** ที่จะถูกเติมข้อมูลด้วยข้อความของบันทึกการชำระเงิน ถ้าข้อความนั้นไม่ว่างเปล่าสำหรับการโอนย้ายเครดิตปัจจุบัน
>
>    [![นิพจน์สำหรับส่วนประกอบของ PaymentNotes](./media/GER-FormulaEditor-ControlContent-2.png)](./media/GER-FormulaEditor-ControlContent-2.png)
>
> - นิพจน์ `@.PaymentsNotes = ""` ที่ถูกกำหนดสำหรับส่วนประกอบของ **DelimitedSequence** เปิดใช้งาน (โดยส่งคืนค่า **จริง**) องค์ประกอบ XML ของ **Ustrd** ที่จะถูกเติมข้อมูลด้วยรายการที่คั่นด้วยเครื่องหมายจุลภาคของหมายเลขใบแจ้งหนี้ที่ถูกใช้ในการชำระการโอนย้ายเครดิตปัจจุบัน ถ้าข้อความของบันทึกการชำระเงินสำหรับการโอนย้ายเครดิตนั้นว่างเปล่า
>
>    [![นิพจน์สำหรับส่วนประกอบของ DelimitedSequence](./media/GER-FormulaEditor-ControlContent-3.png)](./media/GER-FormulaEditor-ControlContent-3.png)
> 
> ตามการตั้งค่านี้ มีการสร้างข้อความสำหรับการชำระของลูกหนี้เเต่ละรายการ องค์ประกอบ XML ของ **Ustrd** จะมีข้อความของบันทึกการชำระเงิน หรือเมื่อข้อความดังกล่าวว่างเปล่า รายการที่คั่นด้วยเครื่องหมายจุลภาคของหมายเลขใบแจ้งหนี้ที่ถูกใช้เพื่อชำระเงิน

## <a name="validation-of-configured-formulas"></a><a name="TestFormula"></a> การตรวจสอบความถูกต้องของสูตรที่ตั้งค่าคอนฟิก

บนหน้า **โปรแกรมออกแบบสูตร** ให้เลือก **การทดสอบ** เพื่อตรวจสอบความถูกต้องของวิธ๊ที่สูตรที่ตั้งค่าคอนฟิกทำงาน

[![การเลือกการทดสอบเพื่อตรวจสอบความถูกต้องของสูตร](./media/ER-FormulaTest-Start.png)](./media/ER-FormulaTest-Start.png)

เมื่อจำเป็นต้องใช้ค่าของอาร์กิวเมนต์สูตร คุณสามารถเปิดกล่องโต้ตอบ **นิพจน์การทดสอบ** จากหน้า **โปรแกรมออกแบบสูตร** ในกรณีส่วนใหญ่ อาร์กิวเมนต์เหล่านี้ต้องถูกกำหนดด้วยตนเอง เนื่องจากการผูกข้อมูลที่ถูกตั้งค่าคอนฟิกไว้ไม่ทำงานในขณะออกแบบ แท็บ **ผลการทดสอบ** บนหน้า **โปรแกรมออกแบบสูตร** แสดงผลลัพธ์จากการดำเนินการของสูตรที่ตั้งค่าคอนฟิก

ตัวอย่างต่อไปนี้แสดงให้เห็นว่าคุณสามารถทดสอบสูตรที่ถูกตั้งค่าคอนฟิกสำหรับโดเมนการค้าในต่างประเทศ เพื่อให้แน่ใจว่ารหัสโภคภัณฑ์อินทราสแทตมีเฉพาะตัวเลขเท่านั้น

เมื่อคุณทดสอบสูตรนี้ คุณสามารถใช้กล่องโต้ตอบ **นิพจน์การทดสอบ** เพื่อระบุค่าของรหัสโภคภัณฑ์อินทราสแทตสำหรับการทดสอบ

[![การระบุรหัสโภคภัณฑ์อินทราสแทตสำหรับการทดสอบ](./media/ER-FormulaTest-Start-EnterArguments.png)](./media/ER-FormulaTest-Start-EnterArguments.png)

หลังจากที่คุณระบุรหัสโภคภัณฑ์อินทราสแทต และเลือก **ตกลง** แท็บ **ผลการทดสอบ** บนหน้า **โปรแกรมออกแบบสูตร** แสดงผลลัพธ์ของการดำเนินการของสูตรที่ตั้งค่าคอนฟิก จากนั้น คุณสามารถประเมินได้ว่าผลลัพธ์เป็นที่ยอมรับหรือไม่ ถ้าไม่สามารถยอมรับผลลัพธ์ได้ คุณสามารถปรับปรุงสูตรและทดสอบอีกครั้ง

[![ผลการทดสอบ](./media/ER-FormulaTest-Result.png)](./media/ER-FormulaTest-Result.png)

ไม่สามารถทดสอบสูตรบางอย่างในขณะออกแบบ ตัวอย่างเช่น สูตรอาจส่งกลับผลลัพธ์ของชนิดข้อมูลที่ไม่สามารถแสดงบนแท็บ **ผลการทดสอบ** ในกรณีนี้ คุณได้รับข้อความแสดงข้อผิดพลาดที่ระบุว่าไม่สามารถทดสอบสูตรได้

[![ข้อความแสดงข้อผิดพลาด](./media/ER-FormulaTest-Error.png)](./media/ER-FormulaTest-Error.png)

## <a name="additional-resources"></a>แหล่งข้อมูลเพิ่มเติม

- [ภาพรวมการรายงานทางอิเล็กทรอนิกส์](general-electronic-reporting.md)
- [ภาษาสูตรในการรายงานทางอิเล็กทรอนิกส์](er-formula-language.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]