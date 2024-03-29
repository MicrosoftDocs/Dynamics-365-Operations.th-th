---
title: การประมวลผลสมุดรายวันทั่วไป
description: บทความนี้อธิบายความสามารถของ Microsoft Dynamics 365 Finance ที่สามารถช่วยทำให้การประมวลผลสมุดรายวันทั่วไปง่ายขึ้น และยังสามารถช่วยให้มั่นใจว่าข้อมูลที่ถูกต้องได้รับการจัดเก็บและการควบคุมภายในไม่ได้ถูกลดทอน
author: kweekley
ms.date: 02/28/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: LedgerJournalSetup, LedgerJournalTable
audience: Application User
ms.reviewer: kfend
ms.custom: 15721
ms.assetid: b4b406fa-b772-44ec-8dd8-8eb818a921ef
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 2055c028f7bfe8edc9faec8f791fff2fbfe08bfa
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 06/03/2022
ms.locfileid: "8896389"
---
# <a name="general-journal-processing"></a>การประมวลผลสมุดรายวันทั่วไป

[!include [banner](../includes/banner.md)]

บทความนี้อธิบายความสามารถที่จะช่วยทำให้การประมวลผลสมุดรายวันทั่วไปง่ายขึ้น และยังช่วยให้มั่นใจได้ว่าข้อมูลที่ถูกต้องได้รับการถูกจัดเก็บและการควบคุมภายในไม่ได้ถูกลดทอน  

## <a name="journal-names"></a>ชื่อสมุดรายวัน

สิ่งที่สำคัญที่สุดในการตั้งค่าอย่างใดอย่างหนึ่งคือชื่อสมุดรายวัน ควรกำหนดชื่อสมุดรายวันสำหรับแต่ละวัตถุประสงค์ เช่นระหว่างบริษัท ปรับปรุงตามเกณฑ์คงค้าง และแก้ไขข้อผิดพลาดได้ คุณสามารถกำหนดชื่อสมุดรายวันแต่ละรายการเพื่ิอช่วยให้การป้อนข้อมูลสำหรับแต่ละวัตถุประสงค์ได้โดยง่าย และปลอดภัย 

ในหน้า **ชื่อสมุดรายวัน** คุณสามารถตั้งค่าองค์ประกอบต่อไปนี้:

-   **การอนุมัติลำดับงาน**– เมื่อต้องการเพิ่มตัวควบคุมภายใน กำหนดลำดับงานสมุดรายวันที่สร้างข้อจำกัดสาระทางบัญชี สำหรับการตรวจทานและอนุมัติขั้นตอน ขึ้นอยู่กับเงื่อนไขเช่นยอดเงินเดบิตรวม คุณตั้งค่าลำดับงานสำหรับสมุดรายวันทั่วไปในหน้า **ลำดับงานบัญชีแยกประเภททั่วไป**
-   **ค่าเริ่มต้น**– เลือกค่าเริ่มต้นสำหรับบัญชีตรงข้าม สกุลเงิน และมิติทางการเงิน
-   **การควบคุมสมุดรายวัน**– คุณสามารถตั้งข้อจำกัดเกี่ยวกับบริษัท และชนิดบัญชี และค่าเซ็กเมนต์ได้ 

**ตัวอย่าง**

ชื่อสมุดรายวันหนึ่งๆสามารถใช้ได้เฉพาะสำหรับการปรับปรุงใดๆเท่านั้น ในกรณีนี้ คุณสามารถระบุเป็นชนิด **บัญชีแยกประเภทเท่านั้น** ที่ใช้ระหว่างบริษัททั้งหมดได้ 

[![ชนิดบัญชีควบคุมสมุดรายวัน](./media/journal-control-account-types1.png)](./media/journal-control-account-types1.png)

ชื่อสมุดรายวันสามารถใช้สำหรับเซกเมนต์เฉพาะ หรือช่วงสำหรับบัญชีหลักเท่านั้น 

[![เซ็กเมนต์การควบคุมสมุดรายวัน](./media/journal-control-segment1.png)](./media/journal-control-segment1.png)

ตัวเลือก **กลับรายการอัตโนมัติ** จะพร้อมใช้งานในสมุดรายวันทั่วไป ตัวอย่างเช่น คุณมีการปรับปรุงตามเกณฑ์คงค้างที่เอกสารจริงยังไม่มีการประมวลผล ดังที่แสดงในภาพประกอบต่อไปนี้
[![กลับรายการสมุดรายวันทั่วไป](./media/general-journal-reversing1.png)](./media/general-journal-reversing1.png) 

add-in ของ Microsoft Excel สำหรับรายการสมุดรายวัน ให้ระดับเพิ่มเติมของการทำให้เป็นอัตโนมัติและทำให้การป้อนข้อมูลง่ายขึ้น **บรรทัดที่เปิดค้างไว้ในการดำเนินการ Excel** ที่มีอยู่ในหน้า **สมุดรายวันทั่วไป** และ **ใบสำคัญสมุดรายวัน** 

ในหน้า **สมุดรายวันประจำงวด** คุณสามารถตั้งค่าสมุดรายวันที่เกิดซ้ำเพื่อทำการประมวลผลสมุดรายวันได้ 

คุณสามารถใช้เทมเพลตใบสำคัญได้ตลอดเวลา ในหน้า **สมุดรายวันทั่วไป** พบการดำเนินการ **บันทึก** และการดำเนินการ **เลือกเทมเพลตใบสำคัญ** ได้ในหน้า  **ใบสำคัญสมุดรายวัน** ภายใต้ **ฟังก์ชัน** สำหรับบรรทัดใบสำคัญ

## <a name="related-setup"></a>ตั้งค่าที่เกี่ยวข้อง
การตั้งค่าต่อไปนี้ไม่ใช่เฉพาะสำหรับสมุดรายวันทั่วไป แต่จะช่วยรับประกันว่า การป้อนข้อมูลเป็นข้อมูลที่ถูกต้องและง่าย

### <a name="main-account"></a>บัญชีหลัก

การตั้งค่าบัญชีหลักแสดงหลายตัวเลือกสำหรับการประมวลผลสมุดรายวันทั่วไป:

-   **ข้อกำหนด DC/CR** – ใช้ตัวเลือกนี้ถ้าบัญชีหลักถูกจำกัดโดยธุรกรรมเดบิตหรือเครดิต การตั้งค่าจะตรวจสอบเมื่อมีการตรวจสอบ หรือการลงรายการบัญชีสมุดรายวัน

-   **บัญชีตรงข้ามเริ่มต้น**
-   **ระงับแล้ว** – ระงับบัญชีหลัก สำหรับการป้อนข้อมูลระหว่างบริษัททั้งหมด หรือสำหรับบริษัท/นิติบุคคลเฉพาะราย
-   **ไม่อนุญาตป้อนข้อมูลด้วยตนเอง**– ป้องกันไม่ให้ผู้ใช้ป้อนค่าสำหรับบัญชีในสมุดรายวันด้วยตนเอง
-   **เริ่มต้น/ตรวจสอบความถูกต้องของรหัสสกุลเงิน**
-   **แทนนิติบุคคล**– ตั้งค่านี้เป็นข้อมูลเฉพาะ บริษัท/นิติบุคคล เฉพาะรายที่กำหนดไว้
    -   **เริ่มต้น/ตรวจสอบความถูกต้องของกลุ่มภาษีขาย**
    -   **มิติเริ่มต้น**– **ไม่คงที่** หรือ **ค่าคงที่** **ค่าคงที่** จะช่วยรับประกันว่า การลงรายการบัญชีทั้งหมดสำหรับบัญชีหลักนี้ใช้ค่ามิติใดๆ ที่ถูกตั้งค่าเป็น **คงที่** เสมอ
-   **การตรวจสอบความถูกต้องของการลงรายการบัญชี**
    -   **ตรวจสอบผู้ใช้**– ตัวเลือกนี้ควบคุมผู้ใช้ที่ได้รับอนุญาตให้ลงรายการบัญชีไปยังบัญชีหลัก
    -   **การลงชนิดการตรวจสอบความถูกต้อง**– ตัวเลือกนี้ควบคุมผู้ใช้ที่ได้รับอนุญาตให้ลงรายการบัญชีไปยังบัญชีหลัก

### <a name="accounting-structures-and-advanced-rules-structures"></a>โครงสร้างทางบัญชีและโครงสร้างกฎขั้นสูง

โครงสร้างการบัญชีและโครงสร้างกฎขั้นสูงเป็นเรื่องสำคัญอย่างยิ่งในการรับประกันว่า มีการรวบรวมข้อมูลที่จำเป็นสำหรับการรายงานทางการเงินและการติดตามประสิทธิภาพทางการเงิน ในระหว่างการประมวลผลสมุดรายวันทั่วไปและเอกสารใดๆ โครงสร้างทางบัญชีและโครงสร้างกฎขั้นสูงช่วยให้คุณสามารถปรับแต่งประสบการณ์การป้อนข้อมูล คุณสามารถอนุญาติการป้อนข้อมูลสำหรับมิติทางการเงินที่เกี่ยวข้องในสถานการณ์แต่ละสถานการณ์ และยังสามารถบังคับความต้องการที่มีการรวบรวมข้อมูลที่ต้องการและแม่นยำอยู่เสมอ

สำหรับข้อมูลเพิ่มเติม ให้ดูหัวข้อต่อไปนี้:
- [วางแผนชื่อผังบัญชีของคุณ](plan-chart-of-accounts.md) 
- [สร้างกฎขั้นสูงสำหรับสมุดรายวัน](tasks/create-advanced-rules-journals.md)
- [สร้างรายการสมุดรายวันโดยใช้เทมเพลต](tasks/create-journal-entry-template.md)
- [สร้างตรวจสอบความถูกต้องของสมุดรายวัน](tasks/create-validate-journals.md)
- [ลงรายการบัญชีสมุดรายวันประจำงวด](tasks/post-periodic-journals.md)
- [ประมวลผลสมุดรายวันการปันส่วนบัญชีแยกประเภท](tasks/process-ledger-allocation-journal.md)

## <a name="simulate-posting"></a>การลงรายการบัญชีทันที
คุณสามารถค้นหา **จำลองการลงรายการบัญชี** ในเมนู **ตรวจสอบ** สำหรับสมุดรายวันส่วนใหญ่ได้ เมื่อคุณตรวจสอบสมุดรายวันที่ใช้ฟังก์ชัน **ตรวจสอบ** ระบบจะทดสอบสมุดรายวันสำหรับเงื่อนไขข้อผิดพลาดที่เฉพาะเจาะจง ถ้าคุณใช้ฟังก์ชัน **จำลองการลงรายการบัญชี** ระบบจะเรียกใช้กระบวนการเดียวกันทั้งหมดที่ถูกรันในระหว่างการลงรายการบัญชี โดยไม่มีการลงรายการบัญชีสมุดรายวันจริง คุณสามารถทบทวนข้อความการลงรายการบัญชีที่แสดงอยู่ แก้ไขข้อผิดพลาดใดๆ ที่คุณพบ จากนั้น คลิกเมนู **ลงรายการบัญชี** เพื่อลงรายการบัญชีสมุดรายวัน 

**จำลองการลงรายการบัญชี** ไม่พร้อมใช้งานสำหรับการประมวลผลชุดงาน อย่างไรก็ตาม ไม่มีรหัสที่พร้อมใช้งานในการจำลองการลงรายการบัญชีในชุดงาน และนักพัฒนาสามารถขยายรหัสเพื่อเพิ่มฟังก์ชันการทำงานนั้นได้  

## <a name="journal-unlock"></a>ปลดล็อกสมุดรายวัน
มีปุ่มอยู่ในหน้าสมุดรายวันเพื่อปลดล็อคสมุดรายวันที่อยู่ในสถานะ "ล็อคโดยระบบ" ตั้งค่าเป็น ใช่ การปลดล็อคนี้สามารถดำเนินการโดยผู้ดูแลระบบที่ได้วิเคราะห์การดำเนินการของชุดงานและยืนยันว่าสมุดรายวันนี้ไม่ได้รับการประมวลผลโดยชุดงานอีกต่อไป ปุ่มนี้จะใช้งานได้โดยคำสั่ง **ปุ่มปลดล็อคสมุดรายวัน** บนหน้า **การจัดการลักษณะการทำงาน** 

## <a name="workflow-recall"></a>การเรียกคืนลำดับงาน 
คุณสามารถเรียกคืนสมุดรายวันในลำดับงานที่มีสถานะเป็น "ไม่สามารถแก้ไขได้" โดยการใช้ปุ่ม **ลำดับงาน** บนสมุดรายวัน และบนหน้า **ประวัติลำดับงาน** คุณสามารถทำเช่นนี้ได้โดยใช้คำสั่ง **แก้ไขสถานะลำดับงานของสมุดรายวัน** บนหน้า **การจัดการลักษณะการทำงาน**

## <a name="delete-journal-lines"></a>การลบรายการสมุดรายวัน
คุณสามารถลบรายการทั้งหมดในสมุดรายวันอย่างเร็วได้โดยคลิก **ฟังก์ชั่น** > **ลบรายการสมุดรายวัน** เมื่อต้องการทำรายการนี้ คลิก **การจัดการลักษณะงาน** เลือก **ลบการเพิ่มประสิทธิภาพของสมุดรายวัน** คุณลักษณะนี้มีผลกระทบต่อส่วนขยายในตาราง **LedgerJournalTrans** และวิธีการ **ลบ** เนื่องจากชุดรายการถูกลบออกโดยไม่มีการเรียกวิธีการ **ลบ** ของแต่ละรายการ 


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
