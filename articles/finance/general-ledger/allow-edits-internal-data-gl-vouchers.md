---
title: อนุญาตให้แก้ไขข้อมูลภายในใบสำคัญของบัญชีแยกประเภททั่วไป
description: บทความนี้แสดงข้อมูลเกี่ยวกับวิธีการแก้ไขข้อมูลภายในใบสำคัญบัญชีแยกประเภททั่วไป
author: kweekley
ms.date: 08/01/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2022-08-01
ms.dyn365.ops.version: 10.0.29
ms.openlocfilehash: 6e346c6ff881d3a33743196b45247493fd19ed1d
ms.sourcegitcommit: adadbc6e355e2ad68a1f6af26a1be1f89dc8eec6
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 09/22/2022
ms.locfileid: "9573263"
---
# <a name="allow-edits-to-internal-data-on-general-ledger-vouchers"></a>อนุญาตให้แก้ไขข้อมูลภายในใบสำคัญของบัญชีแยกประเภททั่วไป

[!include[banner](../includes/banner.md)]


เมื่อคุณลงรายการบัญชีรายการบัญชีที่บัญชีแยกประเภททั่วไป ฟิลด์ **รายละเอียด** มักใช้ในการจัดเก็บบันทึกภายในหรือเอกสาร ถ้าข้อมูลไม่ถูกต้อง อาจทําให้เกิดความสับสนและทําให้การปิดบัญชีสิ้นงวดยุ่งยากมากขึ้น คุณลักษณะนี้ช่วยให้ผู้จัดการฝ่ายบัญชีหรือผู้ควบคุมงานฝ่ายบัญชีสามารถแก้ไขข้อผิดพลาดได้โดยการแก้ไขฟิลด์ **คำอธิบาย** ในใบสำคัญที่ลงรายการบัญชีในบัญชีแยกประเภททั่วไป

การเปลี่ยนแปลงใบสำคัญที่ลงรายการบัญชีในบัญชีแยกประเภททั่วไปจํากัดอยู่เฉพาะข้อมูลที่มีลักษณะภายใน คุณลักษณะนี้จะไม่อนุญาตให้คุณแก้ไขข้อมูล เช่น ยอดเงิน วันที่ลงรายการบัญชี บัญชีแยกประเภท และสกุลเงินของธุรกรรม การเปลี่ยนแปลงข้อมูลที่จะมีผลกระทบต่อการรายงานงบการเงินภายนอกและต้องผ่านใบสำคัญบัญชีแยกประเภททั่วไปใหม่เท่านั้น

> [!NOTE]
> หากต้องการแก้ไขข้อมูลทางการเงิน Dynamics 365 Finance รุ่น 10.0.29 คุณลักษณะนี้จํากัดอยู่เฉพาะการแก้ไขในฟิลด์ **รายละเอียด** เท่านั้น

## <a name="edit-internal-data-on-general-ledger-vouchers"></a>แก้ไขข้อมูลภายในใบสำคัญของบัญชีแยกประเภททั่วไป

ก่อนที่สามารถแก้ไขข้อมูลภายในใบสำคัญบัญชีแยกประเภททั่วไปได้ คุณต้องเปิดใช้งาน **อนุญาตให้แก้ไขข้อมูลภายในเกี่ยวกับใบสำคัญบัญชีแยกประเภททั่วไป** ในพื้นที่ทำงาน **การจัดการคุณลักษณะ**
หลังจากเปิดใช้งานคุณลักษณะแล้ว ผู้ใช้ที่จะแก้ไขใบสำคัญที่ลงรายการบัญชีต้องได้รับการมอบหมายให้กับบทบาทผู้จัดการฝ่ายบัญชีหรือหัวหน้างานฝ่ายบัญชี คุณสามารถเพิ่มสิทธิการได้รับอนุญาตให้กับบทบาทอื่นๆ ด้วยโดยการปรับแต่งบทบาทความปลอดภัย

สามารถแก้ไขกระบวนการได้เฉพาะจากหน้าธุรกรรมใบสำคัญเท่านั้น

1. ไปที่ **บัญชีแยกประเภททั่วไป** > **การสอบถามและการรายงาน** > **ธุรกรรมใบสำคัญ**
2. ในกล่องโต้ตอบ **SysQuery** ให้ป้อนเงื่อนไขการค้นหาเพื่อเลือกใบสำคัญ
3. เลือกบรรทัดที่ต้องการแก้ไขบรรทัดในใบสำคัญที่คุณต้องการแก้ไข แล้วเลือก **แก้ไขใบสำคัญ** > **แก้ไขข้อมูลใบสำคัญภายใน**

    [![หน้าธุรกรรมใบสำคัญ](./media/voucher-transactions-page.png)](./media/voucher-transactions-page.png)
    
บนหน้า **แก้ไขข้อมูลใบสำคัญภายใน** ข้อมูลต่อไปนี้จะแสดงไว้เฉพาะแต่ละบรรทัดที่คุณเลือกไว้
  
  - รหัสบัญชี
  - ชื่อบัญชี
  - ใบสำคัญ
  - คำอธิบายปัจจุบัน
  - คำอธิบายใหม่

    [![ใบสำคัญสมุดรายวัน](./media/edit-internal-voucher-data.png)](./media/edit-internal-voucher-data.png)
    
> [!NOTE]
> สามารถแก้ไขได้เฉพาะฟิลด์ **รายละเอียดใหม่** เท่านั้น โดยค่าเริ่มต้น ค่าจะตรงกับค่าของฟิลด์ **คำอธิบายปัจจุบัน** เพื่อให้คุณสามารถแก้ไขข้อผิดพลาดเล็กน้อยในข้อความอธิบายได้อย่างรวดเร็ว

4. ปรับเปลี่ยนฟิลด์ **คำอธิบายใหม่** บนแต่ละแถว หรือลบข้อความอธิบายออกจากแต่ละแถว

   หรือถ้าต้องอัปเดตหลายแถวด้วยค่าเดียวกัน ให้ปฏิบัติตามขั้นตอนต่อไปนี้

      1. เลือกแถวที่จะแก้ไข แล้วเลือก **อัปเดตเรกคอร์ดที่เลือกจำนวนมาก**
      2. ในฟิลด์ **ฟิลด์ที่จะแก้ไข** ให้เลือกฟิลด์ที่จะแก้ไข ปัจจุบัน การค้นหาจะรวมเฉพาะฟิลด์ **คำอธิบายใหม่** เท่านั้น
      3. ในฟิลด์ **ค่าใหม่** ให้ป้อนคำอธิบายใหม่
      4. เลือก **ปรับปรุง** เรกคอร์ดที่เลือกทั้งหมดจะถูกอัปเดตด้วยค่าใหม่

      [![กล่องโต้ตอบการอัปเดตเรกคอร์ดที่เลือกจำนวนมาก](./media/bulk-update-selected-records.png)](./media/bulk-update-selected-records.png)
    
5. ในฟิลด์ **เหตุผลการแก้ไข** ให้ป้อนหมายเหตุเพื่ออธิบายเหตุผลในการแก้ไข หมายเหตุนี้จะแสดงขึ้นบนหน้า **บันทึกการตรวจสอบของการแก้ไขใบสำคัญ**

   คุณสามารถแก้ไขใบสำคัญใบเดียวกันได้หลายรายการ และการแก้ไขแต่ละครั้งจะถูกติดตาม

## <a name="audit-trail-of-voucher-edits"></a>บันทึกการตรวจสอบของการแก้ไขใบสำคัญ

บันทึกการตรวจสอบบัญชีจะถูกรักษาไว้โดยเฉพาะ เพื่อติดตามการเปลี่ยนแปลงที่กิจกรรมโดยผ่านลักษณะนี้ คุณสามารถเข้าถึงบันทึกการตรวจสอบบัญชีของการแก้ไขใบสำคัญได้สองวิธีดังนี้

  - ไปที่ **บัญชีแยกประเภททั่วไป** > **การสอบถามและการรายงาน** > **ธุรกรรมใบสำคัญ** บนหน้า **การสอบถามใบสำคัญ** ให้เลือก **แก้ไขใบสำคัญ** > **บันทึกการตรวจสอบของการแก้ไขใบสำคัญ** บันทึกการตรวจสอบบัญชีจะแสดงขึ้นเฉพาะเมื่อแสดงเรกคอร์ดใบสำคัญที่เลือกเท่านั้น 
   
    โดยการเปิดการสอบถามด้วยวิธีนี้ คุณสามารถโฟกัสที่การแก้ไขทั้งหมดที่ได้กับเรกคอร์ดใบสำคัญเดียวได้
  
  - ไปที่ **บัญชีแยกประเภททั่วไป** > **งานประจำงวด** > **บันทึกการตรวจสอบของการแก้ไขใบสำคัญ** ในกล่องโต้ตอบ ให้ป้อนเงื่อนไขเพื่อระบุใบสำคัญที่คุณต้องการดูบันทึกการตรวจสอบบัญชีของการแก้ไข เมื่อต้องการดูบันทึกการตรวจสอบบัญชีของใบสำคัญทั้งหมด ให้ปล่อยเงื่อนไขว่างไว้ และเลือก **ตกลง** 
    
    โดยการเปิดการสอบถามด้วยวิธีนี้ คุณสามารถกรองข้อมูลการแก้ไขที่ได้มาจากวันที่ที่ระบุหรือโดยผู้ใช้เฉพาะ

หน้า **บันทึกการตรวจสอบของการแก้ไข** แสดงข้อมูลต่อไปนี้

- **วันที่และเวลาที่สร้าง** – วันที่และเวลาของการแก้ไข
- **เหตุผลการแก้ไข** – เหตุผลที่ผู้ใช้ป้อนไว้ในการแก้ไข
- **สร้างโดย** – ผู้ใช้ที่ทำการแก้ไข

หากต้องการดูรายละเอียดของแต่ละบันทึกการตรวจสอบบัญชี ให้ดูรายละเอียดแนวลึกของค่า **วันที่และเวลาที่สร้าง** หน้า **ดูคุณสมบัติใบสำคัญที่แก้ไข** แสดงข้อมูลเดียวกับหน้าแก้ไขเดิม รวมถึงข้อความอธิบายก่อนหน้านี้และคำอธิบายที่อัปเดต


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
