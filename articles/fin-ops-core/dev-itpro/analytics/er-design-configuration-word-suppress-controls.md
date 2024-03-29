---
title: ระงับการควบคุมเนื้อหา Word ในรายงานที่สร้างขึ้น
description: บทความนี้อธิบายวิธีการกำหนดค่าคอนฟิกรูปแบบการรายงานทางอิเล็กทรอนิกส์ (ER) เพื่อสร้างรายงานเป็นไฟล์ Microsoft Word ที่ถูกระงับตัวควบคุมเนื้อหา
author: kfend
ms.date: 02/11/2021
ms.topic: business-process
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: filatovm
ms.search.validFrom: 2020-01-01
ms.dyn365.ops.version: Version 10.0.6
ms.search.form:
- ERWorkspace, ERSolutionTable, EROperationDesigner
- LedgerJournalTable, LedgerJournalTransVendPaym
ms.openlocfilehash: 8787d43a0c453d49dd1d0efcbb7b5d276721be9e
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 08/12/2022
ms.locfileid: "9267328"
---
# <a name="suppress-word-content-controls-in-generated-reports"></a>ระงับการควบคุมเนื้อหา Word ในรายงานที่สร้างขึ้น

[!include [banner](../includes/banner.md)]

เพื่อสร้างรายงานเป็นเอกสาร Microsoft Word คุณต้องออกแบบเทมเพลตให้กับรายงานเป็นเอกสาร Word เทมเพลตนี้ต้องมีตัวควบคุมเนื้อหา Word เป็นตัวยึดข้อมูลซึ่งจะถูกเติมขณะรันไทม์ ในการใช้เอกสาร Word ที่สร้างเป็นเทมเพลตของรายงานของคุณ คุณจะสามารถ [กำหนดค่าคอนฟิก](er-design-configuration-word.md) [การรายงานทางอิเล็กทรอนิกส์ (ER)](general-electronic-reporting.md) [โซลูชัน](er-quick-start1-new-solution.md) ใหม่ได้ โซลูชันี้ต้องมี [การกำหนดค่าคอนฟิก](general-electronic-reporting.md#Configuration) ER ที่มีส่วนประกอบรูปแบบ ER ต้องกำหนดค่าคอนฟิกรูปแบบ ER นี้เพื่อใช้เทมเพลตที่ออกแบบไว้ในการสร้างรายงาน

ในรุ่น 10.0.6 และที่ใหม่กว่าของ Dynamics 365 Finance คุณสามารถกำหนดค่าคอนฟิกสูตรในรูปแบบ ER ของคุณเพื่อระงับการควบคุมเนื้อหา Word บางรายการในเอกสารที่สร้างขึ้น

ขั้นตอนต่อไปนี้จะอธิบายว่าผู้ใช้ที่ได้รับมอบหมายให้เป็นผู้ดูแลระบบหรือบทบาทที่ปรึกษาด้านฟังก์ชันการรายงานทางอิเล็กทรอนิกส์จะสามารถกำหนดค่ารูปแบบ ER ที่สร้างรายงานเป็นไฟล์ Word และยับยั้งการควบคุมเนื้อหาบางส่วนในรายงานที่สร้างขึ้นซึ่งได้รับการกำหนดค่าโดยใช้เทมเพลต Word ได้

คุณสามารถดำเนินการขั้นตอนเหล่านี้ได้ในบริษัท GBSI

## <a name="prerequisites"></a>ข้อกำหนดเบื้องต้น

เพื่อทำตามขั้นตอนเหล่านี้ คุณต้องดำเนินการตามคำแนะนำงานสามรายการนี้ก่อน

- [ออกแบบการตั้งค่าคอนฟิกสำหรับการสร้างรายงานในรูปแบบ OPENXML](./tasks/er-design-reports-openxml-2016-11.md)
- [นำการตั้งค่าคอนฟิกการรายงานทางอิเล็กทรอนิกส์ที่มีเทมเพลต Excel มาใช้ใหม่เพื่อสร้างรายงานในรูปแบบ Word](./tasks/er-design-configuration-word-2016-11.md)

เมื่อคุณทําขั้นตอนของคู่มืองานนี้แล้ว รายการต่อไปนี้จะถูกจัดเตรียมไว้

- รูปแบบ ER ของ **รายงานแผ่นงานตัวอย่าง** ที่ถูกกำหนดค่าคอนฟิกให้สร้างเอกสารในรูปแบบ Word
- รุ่นแบบร่างของรูปแบบ ER **รายงานแผ่นงานตัวอย่าง** ที่ทำเครื่องหมายเป็น **รันได้**
- วิธีการจ่ายเงินแบบ **อิเล็กทรอนิกส์** ที่ถูกกำหนดค่าคอนฟิกให้ใช้รูปแบบ ER ของ **รายงานแผ่นงานตัวอย่าง** เพื่อการดำเนินการจ่ายเงินของผู้จัดจำหน่าย

คุณยังต้องดาวน์โหลดและบันทึกเทมเพลตต่อไปนี้สำหรับรายงานตัวอย่าง

- [เทมเพลตถูกผูกไว้ 2 ของรายงานการชำระเงิน (SampleVendPaymDocReportBounded.docx)](https://download.microsoft.com/download/1/9/b/19b36e39-861a-414e-9150-9880d9d2487c/SampleVendPaymDocReportBounded2.docx)

## <a name="review-the-downloaded-word-template"></a><a id="tag-control"></a>ตรวจทานเทมเพลต Word ที่ดาวน์โหลด

1. ในแอพลิเคชันบนเดสก์ท็อปของ Word ให้เปิดไฟล์เทมเพลต **SampleVendPaymDocReportBounded2.docx** ที่คุณได้ดาวน์โหลดมาก่อนหน้านี้
2. ตรวจสอบว่าไฟล์เทมเพลตมีส่วนสรุปที่แสดงยอดการชำระเงินรวมของทุกรหัสสกุลเงินซึ่งตรงตามการชำระเงินที่ดำเนินการแล้ว

    - ส่วนสรุปจะอยู่ในตารางแยกต่างหากของเอกสาร Word
    - แถวแรกของตารางนี้จะถือส่วนหัวคอลัมน์ของตารางเป็นส่วนหัวของส่วน
    - แถวที่สองของตารางนี้จะถือตัวควบคุมเนื้อหาที่ทําซ้ำเป็นรายละเอียดของส่วน
    - ตัวควบคุมเนื้อหานี้จะถูกแมปกับเขตข้อมูล **SummaryLines** ของส่วน **รายงาน** XML ที่กำหนดเอง
    - ตามการแมปนี้ ตัวควบคุมเนื้อหาจะเชื่อมโยงกับองค์ประกอบ **SummaryLines** ของรูปแบบ ER ที่แก้ไขได้

    > [!NOTE]
    > ตัวควบคุมเนื้อหาการทําซ้ำจะถูกแท็กโดยคีย์ **SummaryLines** ที่ตรงกับเขตข้อมูลของส่วน XML ที่ศุลกากรซึ่งได้รับการแมป

    ![เค้าโครงเทมเพลต Word](./media/er-design-configuration-word-suppress-controls-image1.gif)

## <a name="select-the-existing-er-report-configuration"></a>เลือกการตั้งค่าคอนฟิกรายงาน ER ที่มีอยู่

สำหรับขั้นตอนต่อไปนี้ คุณจะสามารถนำการกำหนดค่าคอนฟิกของ ER ที่คุณกำหนดไว้กลับมาใช้ใหม่เมื่อคุณทำตามขั้นตอนในคู่มืองานที่กล่าวถึงก่อนหน้านี้ 

1. ไปที่ **การจัดการองค์กร** \> **พื้นที่ทำงาน** \> **การรายงานทางอิเล็กทรอนิกส์**
2. เลือก **การตั้งค่าคอนฟิกการรายงาน**
3. บนหน้า **การกำหนดค่าคอนฟิก** ในแผนภูมิการกำหนดค่าคอนฟิก ให้ขยาย **แบบจำลองการชำระเงิน** และเลือก **รายงานแผ่นงานตัวอย่าง**
4. เลือก **ตัวออกแบบ** เพื่อแก้ไขเวอร์ชันแบบร่างของรูปแบบ ER ที่เลือก

## <a name="replace-the-current-template-with-the-new-template"></a>แทนที่เทมเพลตปัจจุบันด้วยเทมเพลตใหม่

ปัจจุบัน ไฟล์ SampleVendPaymDocReportBounded.docx จะถูกนำไปใช้เป็นเทมเพลตเพื่อสร้างชิ้นงานในรูปแบบ Word ในขั้นตอนต่อไปนี้ คุณจะสามารถแทนที่เทมเพลต Word นี้ด้วยเทมเพลต Word ใหม่ SampleVendPaymDocReportBounded2.docx ที่คุณดาวน์โหลดไว้ก่อนหน้านี้ 

1. บหน้า **ตัวออกแบบรูปแบบ** เลือก **เอกสารแนบ**
2. บนหน้า **เอกสารแนบ** ให้เลือก **ลบ** เพื่อลบเทมเพลตที่มีอยู่
3. เลือก **ใช่** เพื่อยืนยันการลบ
4. เลือก **ใหม่** \> **ไฟล์**
5. เลือก **เรียกดู** แล้วเรียกดูและเลือกไฟล์ **SampleVendPaymDocReportBounded2.docx** ที่คุณดาวน์โหลดไว้ก่อนหน้านี้
6. เลือก **ตกลง**
7. ปิดหน้า **เอกสารแนบ**
8. บหน้า **ตัวออกแบบรูปแบบ** ในเขตข้อมูล **เทมเพลต** ให้ป้อนหรือเลือกไฟล์ **SampleVendPaymDocReportBounded2.docx**

## <a name="run-the-format-to-create-word-output"></a>ดำเนินการรูปแบบเพื่อสร้างชิ้นงานของ Word

1. ไปที่ **บัญชีเจ้าหนี้** \> **การชำระเงิน** \> **สมุดรายวันการชำระเงิน**
2. บนหน้า **การจ่ายเงินของผู้จัดจำหน่าย** บนแท็บ **รายการ** ให้เลือกการจ่ายเงินทั้งหมด
3. เลือก **สถานะการชำระเงิน** \> **ไม่มี**
4. เลือก **สร้างการชำระเงิน**
5. เลือกฟิลด์ **วิธีการชำระเงิน** เลือก **อิเล็กทรอนิกส์**
6. ในฟิลด์ **บัญชีธนาคาร** ให้เลือก **GBSI OPER**
7. เลือก **ตกลง**
8. ในกล่องโต้ตอบ **พารามิเตอร์รายงานอิเล็กทรอนิกส์** ให้เลือก **ตกลง** และวิเคราะห์ผลลัพธ์ที่สร้างขึ้น

    ![การชําระเงินสำหรับการดำเนินการ บนหน้าการชําระเงินให้แก่ผู้จัดจําหน่าย](./media/er-design-configuration-word-suppress-controls-image2.gif)

    ผลลัพธ์จะแสดงในรูปแบบ Word และมีส่วนสรุปด้วย

## <a name="configure-the-editable-format-to-suppress-the-summary-section"></a><a id="configure-to-suppress-control"></a>กำหนดค่าคอนฟิกรูปแบบที่แก้ไขได้เพื่อระงับส่วนสรุป

ถ้าคุณต้องการระงับส่วนสรุปในเอกสารที่สร้างขึ้น ตามการร้องขอของผู้ใช้ที่รันรูปแบบ ER นี้ คุณต้องแก้ไขรูปแบบ ER ที่แก้ไขได้

1. ไปที่ **การจัดการองค์กร** \> **พื้นที่ทำงาน** \> **การรายงานทางอิเล็กทรอนิกส์** และเปิดเวอร์ชันแบบร่างของรูปแบบ ER เพื่อแก้ไข
2. เลือก **การตั้งค่าคอนฟิกการรายงาน** 
3. บนหน้า **การกำหนดค่าคอนฟิก** ในแผนภูมิการกำหนดค่าคอนฟิก ให้ขยาย **แบบจำลองการชำระเงิน** \> **รายงานแผ่นงานตัวอย่าง**
4. เลือก **ตัวออกแบบ**
5. บนหน้า **ตัวออกแบบรูปแบบ** ให้ขยาย **Word** และเลือก **SummaryLines**
6. บนแท็บ **การแมป** ให้เพิ่มแหล่งข้อมูลใหม่เพื่อถามผู้ใช้ขณะรันไทม์ว่าควรระงับส่วนสรุปหรือไม่

    1. เลือก **เพิ่มราก**
    2. ในกล่องโต้ตอบ **เพิ่มแหล่งข้อมูล** ให้เลือก **อินพุทพารามิเตอร์ทั่วไป\ผู้ใช้** เพื่อเปิดกล่องโต้ตอบ **คุณสมบัติแหล่งข้อมูล 'ผู้ใช้อินพุทพารามิเตอร์**
    3. ในเขตข้อมูล **ชื่อ** ให้ป้อน **uipSuppress**
    4. ในเขตข้อมูล **ป้ายชื่อ** ให้ป้อน **ส่วนระงับการสรุป**
    5. ในเขตข้อมูล **ชื่อชนิดข้อมูลการดําเนินงาน** ให้เลือกหรือป้อน **NoYes**
    6. เลือก **ตกลง**

7. เพิ่มแหล่งข้อมูลใหม่ของชนิดประเภทการแจงนับแอปพลิเคชัน **NoYes**

    1. เลือก **เพิ่มราก**
    2. ในกล่องโต้ตอบ **เพิ่มแหล่งข้อมูล** ให้เลือก **Dynamics 365 for Operations\การแจงนับ** เพื่อเปิดกล่องโต้ตอบ **คุณสมบัติการแจงนับแหล่งข้อมูล**
    3. ในเขตข้อมูล **ชื่อ** ให้ป้อน **enumNoYes**
    4. ในเขตข้อมูล **ป้ายชื่อ** ให้ป้อน **ตัวเลือกการระงับ**
    5. ในเขตข้อมูล **ชื่อชนิดข้อมูลการดําเนินงาน** ให้เลือกหรือป้อน **NoYes**
    6. เลือก **ตกลง**

8. สำหรับส่วนประกอบรูปแบบที่ถูกเลือก **SummaryLines** กำหนดค่าสูตรเพื่อระบุว่าเมื่อใดควรระงับการควบคุมเนื้อหา Word ที่เชื่อมโยงกับองค์ประกอบรูปแบบที่เลือก

    1. บนแท็บ **การแมป** ในส่วน **ลบ** ให้เลือก **แก้ไข** เพื่อเปิดหน้า **[ผู้ออกแบบสูตร](general-electronic-reporting-formula-designer.md)**
    2. ในเขตข้อมูล **สูตร** ให้ป้อนสูตร `uipSuppress = enumNoYes.Yes`
    3. เลือก **บันทึก** และปิดหน้า **ตัวออกแบบสูตร**

        > [!NOTE]
        > สูตรนี้จะถูกนำไปใช้กับเอกสารที่สร้างขึ้น **หลังจากที่รันองค์ประกอบรูปแบบอื่นทั้งหมดแล้ว** เมื่อต้องการใช้สูตรนี้ ตัวควบคุมเนื้อหา Word ที่มีถูกแท็กเป็นองค์ประกอบรูปแบบที่มีการกำหนดค่าคอนฟิกสูตรไว้สำหรับ (**SummaryLines** ในกรณีนี้) จะพบไดในเอกสารที่สร้างขึ้น ตัวควบคุมเนื้อหานั้นจะถูกลบออกโดยสมบูรณ์ พร้อมกับแถวในตาราง Word ที่ระงับการควบคุมเนื้อหานั้น แถวรายละเอียดของส่วนสรุปจะถูกลบออกจากเอกสารที่สร้าง
        >
        > ในขณะที่ออกแบบ คุณอาจกำหนดค่าคอนฟิกสูตร **ลบ** ให้กับองค์ประกอบรูปแบบ ถึงแม้ว่าจะไม่มีการควบคุมเนื้อหาในเทมเพลต Word ที่คุณใช้อยู่จะมีแท็กที่ตรงกับชื่อขององค์ประกอบรูปแบบที่มีการกำหนดค่าคอนฟิกคุณสมบัติเป็น **ลบ** ไว้ เมื่อคุณตรวจสอบความถูกต้องของรูปแบบ ณ เวลาการออกแบบ คุณจะได้รับ [คำเตือน](er-components-inspections.md#i14) เกี่ยวกับความไม่สอดคล้องกันนี้
        >
        > ขณะรันไทม์ จะมีข้อยกเว้นเกิดขึ้น ถ้าไม่มีการควบคุมเนื้อหาในเทมเพลต Word ที่คุณใช้อยู่มีแท็กที่ตรงกับชื่อขององค์ประกอบรูปแบบที่มีการตั้งค่าคอนฟิกคุณสมบัติเป็น **ลบ** ไว้

    4. บนแท็บ **การแมป** ในส่วน **ลบ** ให้ตั้งค่าตัวเลือก **กับข้อมูลหลัก** เป็น **ใช่**

        > [!NOTE]
        > คุณต้องตั้งค่าตัวเลือกนี้เป็น **ใช่** เพื่อลบตาราง Word ทั้งหมดเป็นออบเจ็กต์หลักของแถวที่มีรายละเอียดส่วนสรุป ถ้าคุณตั้งค่าตัวเลือกนี้เป็น **ไม่** แถวส่วนหัวจะยังคงอยู่ในเอกสารที่สร้างขึ้น

9. เลือก **บันทึก** เพื่อบันทึกการเปลี่ยนแปลงของคุณไปรูปแบบที่แก้ไขได้

    ![ผลลัพธ์ที่สร้างขึ้นในรูปแบบ Word](./media/er-design-configuration-word-suppress-controls-image3.gif)

## <a name="run-the-modified-format-to-create-word-output"></a>ดำเนินการรูปแบบที่แก้ไขแล้วเพื่อสร้างชิ้นงานของ Word

1. ไปที่ **บัญชีเจ้าหนี้** \> **การชำระเงิน** \> **สมุดรายวันการชำระเงิน**
2. เลือกสมุดรายวันการชำระเงินที่คุณสร้างขึ้น แล้วเลือก **Lines**
3. บนหน้า **การชำระเงินของผู้จัดจำหน่าย** ให้เลือกแถวทั้งหมด แล้วเลือก **สถานะการชำระเงิน** \> **ไม่มี**
4. เลือก **สร้างการชำระเงิน**
5. เลือกฟิลด์ **วิธีการชำระเงิน** เลือก **อิเล็กทรอนิกส์**
6. ในฟิลด์ **บัญชีธนาคาร** ให้เลือก **GBSI OPER**
7. เลือก **ตกลง**
8. ในกล่องโต้ตอบ **พารามิเตอร์รายงานอิเล็กทรอนิกส์** ในเขตข้อมูล **ระงับส่วนสรุป** ให้เลือก **ใช่**
9. เลือก **ตกลง** และวิเคราะห์ผลลัพธ์ที่สร้าง

    ![ผลลัพธ์ที่สร้างขึ้นในรูปแบบ Word](./media/er-design-configuration-word-suppress-controls-image4.gif)

    โปรดสังเกตว่าผลลัพธ์จะไม่มีส่วนสรุป เนื่องจากถูกระงับไว้

## <a name="additional-resources"></a>ทรัพยากรเพิ่มเติม

- [ออกแบบการตั้งค่าคอนฟิกสำหรับการสร้างรายงานในรูปแบบ OPENXML](./tasks/er-design-reports-openxml-2016-11.md)
- [ออกแบบการตั้งค่าคอนฟิกการรายงานทางอิเล็กทรอนิกส์เพื่อสร้างรายงานในรูปแบบ Word](er-design-configuration-word.md)
- [นำการตั้งค่าคอนฟิกการรายงานทางอิเล็กทรอนิกส์ที่มีเทมเพลต Excel มาใช้ใหม่เพื่อสร้างรายงานในรูปแบบ Word](./tasks/er-design-configuration-word-2016-11.md)
- [ตรวจสอบส่วนประกอบ ER ที่ตั้งค่าคอนฟิกเพื่อป้องกันปัญหารันไทม์](er-components-inspections.md#i14)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
