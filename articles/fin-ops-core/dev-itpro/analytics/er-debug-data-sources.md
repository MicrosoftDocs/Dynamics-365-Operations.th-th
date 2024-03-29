---
title: ดีบักแหล่งข้อมูลของรูปแบบ ER ที่ดําเนินการ เพื่อวิเคราะห์การแปลงและลำดับของข้อมูล
description: บทความนี้อธิบายวิธีที่คุณสามารถดีบักแหล่งข้อมูลของรูปแบบ ER ที่ดําเนินการ เพื่อให้เข้าใจการแปลงและลำดับของข้อมูลที่กําหนดค่าดีขึ้น
author: kfend
ms.date: 04/22/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.search.region: Global
ms.author: filatovm
ms.search.validFrom: 2020-04-01
ms.dyn365.ops.version: Release 10.0.11
ms.custom: ''
ms.assetid: ''
ms.search.form: ERSolutionTable, EROperationDesigner
ms.openlocfilehash: 61bc5e3f36bd2ae6e38ed0f511d70a7ae62e045c
ms.sourcegitcommit: 0c927fcb3afd34d870391f05b5393a4673d916e5
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 12/08/2022
ms.locfileid: "9832043"
---
# <a name="debug-data-sources-of-an-executed-er-format-to-analyze-data-flow-and-transformation"></a>ดีบักแหล่งข้อมูลของรูปแบบ ER ที่ดําเนินการ เพื่อวิเคราะห์การแปลงและลำดับของข้อมูล

[!include[banner](../includes/banner.md)]

[!include[banner](../includes/preview-banner.md)]

เมื่อคุณ [ตั้งค่าคอนฟิก](tasks/er-format-configuration-2016-11.md) การรายงานทางอิเล็กทรอนิกส์ (ER) เพื่อสร้างเอกสารขาออก คุณกำหนดวิธีการที่จะใช้ในการดึงข้อมูลจากแอปพลิเคชัน และป้อนข้อมูลในผลลัพธ์ที่สร้างขึ้น เมื่อต้องการให้การสนับสนุนวงจรการใช้งานของโซลูชัน ER มีประสิทธิภาพมากขึ้น โซลูชันของคุณควรประกอบด้วย แบบจําลองข้อมูล ER และส่วนประกอบ การแม็ป และส่วนประกอบการแม็ป รูปแบบ ER เพื่อให้การแม็ปแบบจำลองเป็นแบบเฉพาะใบสมัคร ในขณะที่ส่วนประกอบอื่นๆ ยังคงไม่ระบุใบสมัครเหมือนเดิม ดังนั้น ส่วนประกอบ ER หลายตัวอาจ ส่งผลต่อ กระบวนการป้อนข้อมูลในผลลัพธ์ที่สร้างขึ้น

บางครั้ง ข้อมูลของผลลัพธ์ที่สร้างขึ้นมีลักษณะแตกต่างจากข้อมูลเดียวกันในฐานข้อมูลแอปพลิเคชัน ในกรณีเหล่านี้ คุณจะต้องกําหนดว่าส่วนประกอบ ER ใดที่รับผิดชอบการแปลงข้อมูล คุณลักษณะดีบักเกอร์แหล่งข้อมูล ER ช่วยลดเวลาและต้นทุนที่เกี่ยวข้องกับการตรวจสอบนี้อย่างมาก คุณสามารถยุติการดําเนินการของรูปแบบ ER และเปิดอินเทอร์เฟสดีบักเกอร์แหล่งข้อมูลได้ คุณสามารถเรียกดูแหล่งข้อมูลที่มีอยู่ และเลือกแหล่งข้อมูลแต่ละแหล่งสําหรับการดําเนินการ การดําเนินการด้วยตนเองนี้จําลองการดําเนินการของแหล่งข้อมูลในระหว่างการรันจริงของรูปแบบ ER ผลลัพธ์จะแสดงบนหน้าที่คุณสามารถวิเคราะห์ข้อมูลที่ได้รับ

เมื่อต้องการเปิดคุณลักษณะการดีบักแหล่งข้อมูล ให้ตั้งค่าตัวเลือก **เปิดใช้งานการดีบักข้อมูลเมื่อเรียกใช้รูปแบบ** เป็น **ใช่** ในพารามิเตอร์ผู้ใช้ ER จากนั้น คุณสามารถเริ่มต้นการดีบักแหล่งข้อมูล ในขณะที่คุณเรียกใช้รูปแบบ ER เพื่อสร้างเอกสารขาออก คุณยังสามารถใช้ตัวเลือก **เริ่มต้นการดีบัก** เพื่อเริ่มต้นการดีบักแหล่งข้อมูลสําหรับรูปแบบ ER ที่มีการตั้งค่าคอนฟิกไว้ใน [โปรแกรมออกแบบการดําเนินการ ER](./tasks/er-format-configuration-2016-11.md#design-the-format-of-an-electronic-document)

บทความนี้แสดงแนวทางสําหรับการเริ่มการดีบักแหล่งข้อมูลสําหรับรูปแบบ ER ที่ดําเนินการ โดยอธิบายถึงวิธีที่ข้อมูลสามารถช่วยให้คุณเข้าใจและลำดับข้อมูลและการแปลงข้อมูล ตัวอย่างในบทความนี้ ใช้กระบวนการทางธุรกิจสําหรับการประมวลผลการชําระเงินให้แก่ผู้จัดจําหน่าย

## <a name="limitations"></a>การจำกัด

ดีบักเกอร์แหล่งข้อมูลสามารถใช้เพื่อเข้าถึงข้อมูลของแหล่งข้อมูลที่ใช้ในรูปแบบ ER ที่เรียกใช้เพื่อสร้างเอกสารขาออก ไม่สามารถใช้เพื่อดีบักแหล่งข้อมูลของรูปแบบ ER ที่ออกแบบมาเพื่อวิเคราะห์เอกสารขาเข้า

การตั้งค่ารูปแบบ ER ต่อไปนี้ไม่สามารถเข้าถึงได้ในปัจจุบันสําหรับการดีบักแหล่งข้อมูล:

- การแปลงรูปแบบ
- กฎการตรวจสอบความถูกต้องของรูปแบบและการแมป
- การเปิดใช้งานนิพจน์
- รายละเอียดของการรวบรวมข้อมูลในหน่วยความจํา

## <a name="prerequisites"></a>ข้อกำหนดเบื้องต้น

- เมื่อต้องการดำเนินการตัวอย่างในบทความนี้ให้เสร็จสมบูรณ์ คุณต้องเข้าถึงหนึ่งใน [บทบาท](../sysadmin/tasks/assign-users-security-roles.md) ต่อไปนี้:

    - นักพัฒนาการรายงานทางอิเล็กทรอนิกส์
    - ที่ปรึกษาด้านการทำงานของการรายงานทางอิเล็กทรอนิกส์
    - ผู้ดูแลระบบ

- บริษัทต้องตั้งค่าเป็น **DEMF**

- ทําตามขั้นตอนใน [ภาคผนวก 1](#appendix1) ของบทความนี้ เพื่อดาวน์โหลดส่วนประกอบของโซลูชัน Microsoft ER ที่จําเป็นเพื่อประมวลผลการชําระเงินให้แก่ผู้จัดจําหน่าย
- ทําตามขั้นตอนใน [ภาคผนวก 2](#appendix2) ของบทความนี้ เพื่อจัดเตรียมบัญชีเจ้าหนี้สําหรับการประมวลผลการชําระเงินของผู้จัดจําหน่าย โดยใช้โซลูชัน ER ที่คุณจะดาวน์โหลด

## <a name="process-a-vendor-payment-to-get-a-payment-file"></a>ประมวลผลการชําระเงินให้แก่ผู้จัดจําหน่ายเพื่อรับไฟล์การชําระเงิน

1. ทําตามขั้นตอนใน [ภาคผนวก 3](#appendix3) ของบทความนี้ เพื่อประมวลผลการชําระเงินให้แก่ผู้จัดจําหน่าย

    ![การประมวลผลการชําระเงินให้แก่ผู้จัดจําหน่ายอยู่ระหว่างการดำเนินการ](./media/er-data-debugger-process-payment.png)

2. ดาวน์โหลดและบันทึกไฟล์ zip ลงในคอมพิวเตอร์ของคุณ
3. แยกไฟล์การชําระเงิน **ISO20022 Credit transfer.xml** จากไฟล์ zip
4. เปิดไฟล์การชําระเงินที่แยกออกมา โดยใช้ตัวแสดงไฟล์ XML

    ในไฟล์การชําระเงิน รหัสหมายเลขบัญชีธนาคารระหว่างประเทศ (IBAN) ของบัญชีธนาคารของผู้จัดจําหน่ายไม่มีช่องว่าง ดังนั้น จะแตกต่างจากค่าที่ถูก [ป้อน](#enteredIBANcode) บนหน้า **บัญชีธนาคาร**

    ![รหัส IBAN ไม่มีช่องว่าง](./media/er-data-debugger-payment-file.png)

    คุณสามารถใช้ดีบักเกอร์แหล่งข้อมูล ER เพื่อเรียนรู้ว่าส่วนประกอบของโซลูชัน ER ใดที่จะถูกใช้เพื่อตัดช่องว่างในรหัส IBAN

## <a name="turn-on-data-source-debugging"></a>เปิดการดีบักแหล่งข้อมูล

1. ไปที่ **การจัดการองค์กร** \> **การรายงานทางอิเล็กทรอนิกส์** \> **การตั้งค่าคอนฟิก**
2. ในหน้า **การตั้งค่าคอนฟิก** บนบานหน้าต่างการดำเนินการ บนแท็บ **การตั้งค่าคอนฟิก** ในกลุ่ม **การตั้งค่าล่วงหน้า** เลือก **พารามิเตอร์ผู้ใช้**
3. ตั้งค่าตัวเลือก **เปิดใช้งานการดีบักข้อมูลเมื่อเรียกใช้รูปแบบ** เป็น **ใช่**

    > [!NOTE]
    > พารามิเตอร์นี้เฉพาะผู้ใช้และเฉพาะบริษัท

    ![กล่องโต้ตอบพารามิเตอร์ผู้ใช้](./media/er-data-debugger-user-parameters.png)

## <a name="process-a-vendor-payment-for-debugging"></a>ประมวลผลการชําระเงินให้แก่ผู้จัดจําหน่ายสําหรับการดีบัก

1. ทําตามขั้นตอนใน [ภาคผนวก 3](#appendix3) ของบทความนี้ เพื่อประมวลผลการชําระเงินให้แก่ผู้จัดจําหน่าย
2. ในกล่องข้อความ ให้เลือก **ใช่** เพื่อยืนยันว่าคุณต้องการยุติการประมวลผลการชําระเงินของผู้จัดจําหน่าย และเริ่มต้นการดีบักแหล่งข้อมูลแทนบนหน้า **ดีบักแหล่งข้อมูล**

    ![กล่องข้อความการยืนยัน](./media/er-data-debugger-start-debugging.png)

## <a name="debug-data-sources-that-are-used-in-payment-processing"></a>ดีบักแหล่งข้อมูลที่ใช้ในการประมวลผลการชําระเงิน

### <a name="debug-the-model-mapping"></a>ดีบักการแมปแบบจําลอง

1. บนหน้า **ดีบักแหล่งข้อมูล** บนบานหน้าต่างการดําเนินการ เลือก **การแมปแบบจําลอง** เพื่อเริ่มดีบักจากส่วนประกอบ ER นี้
2. ในบานหน้าต่างแหล่งข้อมูลทางด้านซ้าย ให้เลือกแหล่งข้อมูล **\$notSentTransactions** แล้วเลือก **อ่านเรกคอร์ดทั้งหมด**

    คุณสามารถเลือก **อ่าน 1 เรกคอร์ด** **อ่าน 10 เรกคอร์ด** **อ่าน 100 เรกคอร์ด** หรือ **อ่านเรกคอร์ดทั้งหมด** เพื่อบังคับให้มีการอ่านเรกคอร์ดจํานวนที่เหมาะสมจากแหล่งข้อมูลที่เลือก ด้วยวิธีนี้ คุณสามารถจําลองการเข้าถึงแหล่งข้อมูลจากรูปแบบ ER ที่เรียกใช้อยู่ได้

3. ในบานหน้าต่างข้อมูลทางด้านขวา ให้เลือก **ขยายทั้งหมด**

    คุณจะเห็นว่าแหล่งข้อมูลที่เลือกของชนิด **รายการเรกคอร์ด** มีเรกคอร์ดเดียว

4. ขยายแหล่งข้อมูล **\$notSentTransactions** และเลือกวิธีการ **vendBankAccountInTransactionCompany()** ที่ซ้อนกัน
5. ขยายวิธีการ **vendBankAccountInTransactionCompany()** และเลือกฟิลด์ **IBAN** ที่ซ้อนกัน
6. เลือก **รับค่า**

    คุณสามารถเลือก **รับค่า** เพื่อบังคับให้ค่าของฟิลด์ที่เลือกของแหล่งข้อมูลที่เลือกสามารถอ่านได้ ด้วยวิธีนี้ คุณสามารถจําลองการเข้าถึงฟิลด์นี้จากรูปแบบ ER ที่เรียกใช้อยู่ได้

7. เลือก **ขยายทั้งหมด**

    ![ค่าของฟิลด์ IBAN ในการแมปแบบจำลอง](./media/er-data-debugger-debugging-model-mapping.png)

    ดังเช่นที่คุณสามารถเห็นได้ การแมปแบบจําลองไม่รับผิดชอบพื้นที่ที่ถูกตัด เนื่องจากรหัส IBAN ที่ส่งกลับบัญชีธนาคารของผู้จัดจําหน่ายมีช่องว่าง ดังนั้น คุณต้องดําเนินการดีบักแหล่งข้อมูลต่อไป

### <a name="debug-the-format-mapping"></a>ดีบักการแมปรูปแบบ

1. บนหน้า **ดีบักแหล่งข้อมูล** บนบานหน้าต่างการดําเนินการ เลือก **การแมปรูปแบบ** เพื่อดําเนินการดีบักจากส่วนประกอบ ER นี้ต่อไป
2. เลือกแหล่งข้อมูล **\$PaymentByDebtor** แล้วเลือก **อ่านเรกคอร์ดทั้งหมด**
3. ขยาย **\$PaymentByDebtor**
4. ขยาย **\$PaymentByDebtor.Lines** แล้วเลือก **อ่านเรกคอร์ดทั้งหมด**
5. ขยาย **\$PaymentByDebtor.Lines.CreditorAccount**
6. ขยาย **\$PaymentByDebtor.Lines.CreditorAccount.Identification** แล้วเลือก **\$PaymentByDebtor.Lines.CreditorAccount.Identification.IBAN**
7. เลือก **รับค่า**
8. เลือก **ขยายทั้งหมด**

    ![ค่าของฟิลด์ IBAN ในการแมปรูปแบบ](./media/er-data-debugger-debugging-format-mapping.png)

    ดังเช่นที่คุณสามารถเห็นได้ แหล่งข้อมูลของรูปแบบไม่รับผิดชอบพื้นที่ที่ถูกตัด เนื่องจากรหัส IBAN ที่ส่งกลับบัญชีธนาคารของผู้จัดจําหน่ายมีช่องว่าง ดังนั้น คุณต้องดําเนินการดีบักแหล่งข้อมูลต่อไป

### <a name="debug-the-format"></a>ดีบักรูปแบบ

1. บนหน้า **ดีบักแหล่งข้อมูล** บนบานหน้าต่างการดําเนินการ เลือก **รูปแบบ** เพื่อดําเนินการดีบักจากส่วนประกอบ ER นี้ต่อไป
2. ขยายองค์ประกอบรูปแบบเพื่อเลือก **ISO20022CTReports** \> **XMLHeader** \> **เอกสาร** \> **CstmrCdtrfInitn** \> **Pmtinf** แล้วเลือก **อ่านเรกคอร์ดทั้งหมด**
3. ขยายองค์ประกอบรูปแบบเพื่อเลือก **ISO20022CTReports** \> **XMLHeader** \> **เอกสารt** \> **CstmrCdtTrfInitn** \> **PmtInf** \> **CdtTrfTxInf** แล้วเลือก **อ่านเรกคอร์ดทั้งหมด**
4. ขยายองค์ประกอบรูปแบบเพื่อเลือก **ISO20022CTReports** \> **XMLHeader** \> **เอกสาร** \> **CstmrCdtTrfInitn** \> **PmtInf** \> **CdtTrfTxInf** \> **CdtrAcct** \> **Id** \> **IBAN** \> **BankIBAN** แล้วเลือก **รับค่า**
5. เลือก **ขยายทั้งหมด**

    ![ค่าของฟิลด์ IBAN ในรูปแบบ](./media/er-data-debugger-debugging-format.png)

   ดังเช่นที่คุณสามารถเห็นได้ การผูกรูปแบบไม่รับผิดชอบพื้นที่ที่ถูกตัด เนื่องจากรหัส IBAN ที่ส่งกลับบัญชีธนาคารของผู้จัดจําหน่ายมีช่องว่าง ดังนั้น องค์ประกอบ **BankIBAN** ถูกตั้งค่าคอนฟิกให้ใช้การแปลงรูปแบบที่ตัดทอนช่องว่าง

6. ปิดดีบักเกอร์แหล่งข้อมูล

### <a name="review-the-format-transformations"></a>ตรวจทานการแปลงรูปแบบ

1. ไปที่ **การจัดการองค์กร** \> **การรายงานทางอิเล็กทรอนิกส์** \> **การตั้งค่าคอนฟิก**
2. บนหน้า **การตั้งค่าคอนฟิก** ให้เลือก **รูปแบบการชําระเงิน** \> **การโอนย้ายเครดิต ISO20022**
3. เลือก **โปรแกรมออกแบบ** และจากนั้นขยายองค์ประกอบเพื่อเลือก **เอกสาร** \> **CstmrCdtTrfInitn** \> **PmtInf** \> **CdtTrfTxInf** \> **CdtrAcct** \> **Id** \> **IBAN** \> **BankIBAN**

    ![องค์ประกอบ BankIBAN บนหน้าโปรแกรมออกแบบรูปแบบ](./media/er-data-debugger-referred-transformation.png)

    ดังเช่นที่คุณสามารถเห็นได้ องค์ประกอบ **BankIBAN** ถูกตั้งค่าคอนฟิกให้ใช้การแปลงข้อมูล **ลบที่ไม่ใช่ตัวอักษรและตัวเลข**

4. เลือกแท็บ **การแปลงข้อมูล**

    ![แท็บการแปลงสําหรับองค์ประกอบ BankIBAN](./media/er-data-debugger-transformation.png)

    ดังเช่นที่คุณสามารถเห็นได้ การแปลง **ลบที่ไม่ใช่ตัวอักษรและตัวเลข** ถูกตั้งค่าคอนฟิกให้ใช้นิพจน์ที่ตัดทอนช่องว่างจากสตริงข้อความที่ให้ไว้

## <a name="start-to-debug-in-the-operation-designer"></a>เริ่มดีบักในโปรแกรมออกแบบการดําเนินงาน

เมื่อคุณตั้งค่าคอนฟิกรุ่นแบบร่างของรูปแบบ ER ที่สามารถเรียกใช้ได้โดยตรงจากโปรแกรมออกแบบการดําเนินงาน คุณสามารถเข้าถึงดีบักเกอร์แหล่งข้อมูล โดยการเลือก **เริ่มการดีบัก** บนบานหน้าต่างการดําเนินการ

![ปุ่ม เริ่มการดีบัก บนหน้าโปรแกรมออกแบบรูปแบบ](./media/er-data-debugger-run-from-designer.png)

การแมปรูปแบบและส่วนประกอบของรูปแบบของรูปแบบ ER ที่กําลังแก้ไขจะพร้อมใช้งานสําหรับการดีบัก

## <a name="start-to-debug-in-the-model-mapping-designer"></a>เริ่มดีบักในโปรแกรมออกแบบการแมปแบบจำลอง

เมื่อคุณตั้งค่าคอนฟิกการแมปแบบจำลอง ER ที่สามารถเรียกใช้ได้จากหน้า **การแมปแบบจำลอง** คุณสามารถเข้าถึงดีบักเกอร์แหล่งข้อมูล โดยการเลือก **เริ่มการดีบัก** บนบานหน้าต่างการดําเนินการ

![ปุ่ม เริ่มการดีบัก บนหน้าโปรแกรมออกแบบการแมปแบบจำลอง](./media/er-data-debugger-run-from-designer-mapping.png)

ส่วนประกอบการแมปแบบจําลองของการแมป ER ที่กําลังแก้ไขจะพร้อมใช้งานสําหรับการดีบัก

## <a name="appendix-1-get-an-er-solution"></a><a name="appendix1"></a>ภาคผนวก 1: รับโซลูชัน ER

### <a name="download-an-er-solution"></a>ดาวน์โหลดโซลูชัน ER

ถ้าคุณต้องการใช้โซลูชัน ER เพื่อสร้างไฟล์การชําระเงินทางอิเล็กทรอนิกส์สําหรับการชําระเงินของผู้จัดจําหน่ายที่มีการประมวลผล คุฯสามารถ [ดาวน์โหลด](download-electronic-reporting-configuration-lcs.md) รูปแบบการชำระเงิน ER **การโอนย้ายเครดิต ISO20022** ที่พร้อมใช้งานจากไลบรารีสินทรัพย์ที่ใช้ร่วมกันใน Microsoft Dynamics Lifecycle Services (LCS) หรือจากที่เก็บส่วนกลาง

![การนําเข้ารูปแบบการชําระเงิน ER บนหน้าที่เก็บการตั้งค่าคอนฟิก](./media/er-data-debugger-import-from-repo.png)

นอกเหนือจากรูปแบบ ER ที่เลือก [การตั้งค่าคอนฟิก](general-electronic-reporting.md#Configuration) ต่อไปนี้ต้องนําเข้าในอินสแตนซ์ของ Microsoft Dynamics 365 Finance ของคุณโดยอัตโนมัติ โดยเป็นส่วนหนึ่งของโซลูชัน ER **การโอนย้ายเครดิต ISO20022**:

- **รูปแบบการชำระเงิน** การตั้งค่าคอนฟิกแบบจำลองข้อมูล ER
- **การโอนย้ายเครดิต ISO20022** การตั้งค่าคอนฟิกรูปแบบ ER
- การตั้งค่าคอนฟิกการแมปแบบจำลอง ER ของ **การแมปแบบจำลองการชำระเงิน 1611**
- การตั้งค่าคอนฟิกการแมปแบบจำลอง ER ของ **การแมปแบบจำลองการชำระเงินไปยังจุดปลายทาง ISO20022**

คุณสามารถค้นหาการตั้งค่าคอนฟิกเหล่านี้ได้บนหน้า **การตั้งค่าคอนฟิก** ของกรอบงาน ER (**การจัดการองค์กร** \> **การรายงานทางอิเล็กทรอนิกส์** \> **การตั้งค่าคอนฟิก**)

![การตั้งค่าคอนฟิกที่นำเข้าบนหน้าการตั้งค่าคอนฟิก](./media/er-data-debugger-configurations.png)

ถ้ามีการตั้งค่าคอนฟิกที่แสดงไว้ก่อนหน้านี้ใด ๆ ในแผนภูมิการตั้งค่าคอนฟิก คุณต้องดาวน์โหลดจากไลบรารีสินทรัพย์ LCS ที่ใช้ร่วมกันด้วยตนเองในลักษณะเดียวกับที่คุณดาวน์โหลดรูปแบบการชําระเงิน ER **การโอนย้ายเครดิต ISO20022**

### <a name="analyze-the-downloaded-er-solution"></a>วิเคราะห์โซลูชัน ER ที่ดาวน์โหลด

#### <a name="review-the-model-mapping"></a>ตรวจทานการแมปแบบจำลอง

1. ไปที่ **การจัดการองค์กร** \> **การรายงานทางอิเล็กทรอนิกส์** \> **การตั้งค่าคอนฟิก**
2. เลือก **รูปแบบการชําระเงิน** \> **การแมปแบบจําลองการชําระเงิน 1611**
3. เลือก **ตัวออกแบบ**
4. เลือกเรกคอร์ดการแมป **การแมปรูปแบบการชำระเงิน CT ISO20022**
5. เลือก **โปรแกรมออกแบบ** แล้วตรวจทานการแมปแบบจําลองที่เปิด

    โปรดสังเกตว่าฟิลด์ **การชําระเงิน** ของแบบจําลองข้อมูลถูกผูกไว้กับแหล่งข้อมูล **\$notSentTransactions** ที่ส่งกลับรายการของบรรทัดการชําระเงินของผู้จัดจําหน่ายที่กําลังประมวลผล

    ![ฟิลด์การชําระเงินบนหน้าโปรแกรมออกแบบการแมปแบบจําลอง](./media/er-data-debugger-model-mapping.png)

#### <a name="review-the-format-mapping"></a>ตรวจทานการแมปรูปแบบ

1. ไปที่ **การจัดการองค์กร** \> **การรายงานทางอิเล็กทรอนิกส์** \> **การตั้งค่าคอนฟิก**
2. เลือก **รูปแบบการชําระเงิน** \> **การโอนย้ายเครดิต ISO20022**
3. เลือก **ตัวออกแบบ**
4. บนแท็บ **การแมป** ให้ตรวจทานการแมปรูปแบบที่เปิด

    โปรดสังเกตว่า **เอกสาร** \> **CstmrCdtTrfInitn** \> องค์ประกอบ **PmtInf** ของ **ISO20022CTReports** \> ไฟล์ **XMLHeader** ถูกผูกไว้กับแหล่งข้อมูล **\$PaymentByDebtor** ที่ถูกตั้งค่าคอนฟิกเพื่อจัดกลุ่มเรกคอร์ดของฟิลด์ **การชำระเงิน** ของแบบจำลองข้อมูล

    ![องค์ประกอบ PmtInf บนหน้าโปรแกรมออกแบบรูปแบบ](./media/er-data-debugger-format-mapping.png)

#### <a name="review-the-format"></a>ตรวจทานรูปแบบ

1. ไปที่ **การจัดการองค์กร** \> **การรายงานทางอิเล็กทรอนิกส์** \> **การตั้งค่าคอนฟิก**
2. เลือก **รูปแบบการชําระเงิน** \> **การโอนย้ายเครดิต ISO20022**
3. เลือก **โปรแกรมออกแบบ** แล้วตรวจทานรูปแบบที่เปิด

    โปรดสังเกตว่าองค์ประกอบรูปแบบภายใต้ **เอกสาร** \> **CstmrCdtTrfInitn** \> **PmtInf** \> **CdtTrfTxInf** \> **CdtrAcct** \> **Id** \> **IBAN** \> **BankIBAN** ถูกกําหนดค่าให้ป้อนรหัส IBAN ของบัญชีผู้จัดจําหน่ายในไฟล์การชําระเงิน

    ![องค์ประกอบรูปแบบ BankIBAN บนหน้าตัวออกแบบรูปแบบ](./media/er-data-debugger-format.png)

## <a name="appendix-2-configure-accounts-payable"></a><a name="appendix2"></a>ภาคผนวก 2: ตั้งค่าคอนฟิกบัญชีเจ้าหนี้

### <a name="modify-a-vendor-property"></a>ปรับเปลี่ยนคุณสมบัติของผู้จัดจําหน่าย

1. ไปที่ **บัญชีของเจ้าหนี้** \> **ผู้จัดจำหน่าย** \> **ผู้จัดจำหน่ายทั้งหมด**
2. เลือกผู้จัดจำหน่าย **DE-01002** และจากนั้น บนบานหน้าต่างการดำเนินการ บนแท็บ **ผู้จัดจำหน่าย** ในกลุ่ม **ตั้งค่า** เลือก **บัญชีธนาคาร**
3. บนแท็บด่วน **การระบุรหัสประจำตัว** ในฟิลด์ **IBAN** <a name="enteredIBANcode"></a>ให้ป้อน **GB33 BUKB 2020 1555 5555 55**
4. เลือก **บันทึก**

![ฟิลด์ IBAN จะตั้งค่าบนหน้าบัญชีธนาคารของผู้จัดจำหน่าย](./media/er-data-debugger-iban.png)

### <a name="set-up-a-method-of-payment"></a>ตั้งค่าวิธีการชำระเงิน

1. ไปที่ **บัญชีเจ้าหนี้** \> **การตั้งค่าการชำระเงิน** \> **วิธีการชำระเงิน**
2. เลือกวิธีการชำระเงิน **SEPA CT**
3. บนแท็บด่วน **รูปแบบไฟล์** ในส่วน **รูปแบบไฟล์** ให้ตั้งค่าตัวเลือก **รูปแบบการส่งออกทางอิเล็กทรอนิกส์ทั่วไป** เป็น **ใช่**
4. ในฟิลด์ **การตั้งค่าคอนฟิกรูปแบบการส่งออก** ให้เลือกรูปแบบ ER **การโอนย้ายเครดิต ISO20022**
5. เลือก **บันทึก**

![การตั้งค่ารูปแบบไฟล์ในหน้าวิธีการชําระเงิน](./media/er-data-debugger-payment-method.png)

### <a name="add-a-vendor-payment"></a>เพิ่มรายการชำระเงินให้แก่ผู้จัดจำหน่าย

1. ไปที่ **บัญชีเจ้าหนี้** \> **การชำระเงิน** \> **สมุดรายวันการชำระเงินผู้จัดจำหน่าย**
2. เพิ่มสมุดรายวันการชำระเงินใหม่
3. เลือก **บรรทัด** และเพิ่มบรรทัดการชําระเงินใหม่
4. ในฟิลด์ **บัญชี** ให้เลือกผู้จัดจำหน่าย **DE-01002**
5. ในฟิลด์ **เดบิต** ให้ป้อนค่า
6. ในฟิลด์ **วิธีการชำระเงิน** ให้เลือก **SEPA CT**
7. เลือก **บันทึก**

![การชําระเงินให้แก่ผู้จัดจําหน่ายที่เพิ่มบนหน้าการชําระเงินให้แก่ผู้จัดจําหน่าย](./media/er-data-debugger-payment-journal.png)

## <a name="appendix-3-process-a-vendor-payment"></a><a name="appendix3"></a>ภาคผนวก 3: ดำเนินการการชำระเงินให้แก่ผู้จัดจำหน่าย

1. ไปที่ **บัญชีเจ้าหนี้** \> **การชำระเงิน** \> **สมุดรายวันการชำระเงินผู้จัดจำหน่าย**
2. บนหน้า **สมุดรายวันการชำระเงินให้แก่ผู้จัดจำหน่าย** เลือกสมุดรายวันการชำระเงินที่คุณเพิ่งสร้าง และจากนั้นเลือก **บรรทัด**
3. เลือกรายการการชำระเงิน แล้วเลือก **สถานะการชำระเงิน** \> **ไม่มี**
4. เลือก **สร้างการชำระเงิน**
5. ในฟิลด์ **วิธีการชำระเงิน** ให้เลือก **SEPA CT**
6. ในฟิลด์ **บัญชีธนาคาร** ให้เลือก **DEMF OPER**
7. ในกล่องโต้ตอบ **สร้างการชําระเงิน** ให้เลือก **ตกลง**
8. ในกล่องโต้ตอบ **พารามิเตอร์ของรายงานทางอิเล็กทรอนิกส์** เลือก **ตกลง**


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
