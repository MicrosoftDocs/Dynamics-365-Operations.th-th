---
title: ตั้งค่า และประมวลผลใบแจ้งหนี้ที่เกิดซ้ำ
description: บทความนี้อธิบายวิธีการตั้งค่าและประมวลผลใบแจ้งหนี้ที่เกิดซ้ำ คุณสามารถใช้ใบแจ้งหนี้ที่เกิดซ้ำถ้าคุณต้องออกใบแจ้งหนี้ยอดเงินเดียวกันเป็นประจำให้ลูกค้า
author: ShivamPandey-msft
ms.date: 08/22/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: CustInvoiceTemplate
audience: Application User
ms.reviewer: kfend
ms.custom: 14011
ms.assetid: 9cc37003-adf1-413d-b2b2-2badcf512e3b
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: ce734567f0c5bf02e30c36484449c3869b82dc84
ms.sourcegitcommit: 631d2cea52590af15f208e9af584446e85540fcf
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 05/07/2022
ms.locfileid: "8724768"
---
# <a name="set-up-and-process-recurring-invoices"></a>ตั้งค่า และประมวลผลใบแจ้งหนี้ที่เกิดซ้ำ

[!include [banner](../includes/banner.md)]

บทความนี้อธิบายวิธีการตั้งค่าและประมวลผลใบแจ้งหนี้ที่เกิดซ้ำ คุณสามารถใช้ใบแจ้งหนี้ที่เกิดซ้ำถ้าคุณต้องออกใบแจ้งหนี้ยอดเงินเดียวกันเป็นประจำให้ลูกค้า

## <a name="create-a-recurring-free-text-invoice-template"></a>สร้างเท็มเพลตสำหรับใบแจ้งหนี้ข้อความอิสระที่เกิดซ้ำ

เมื่อมีการออกอินวอยซ์ลูกค้าสำหรับบริการเดียวกันเป็นประจำ คุณต้องกำหนดแม่แบบใบแจ้งหนี้ข้อความอิสระที่สามารถนำมาใช้ใหม่เพื่อสร้างใบแจ้งหนี้ เท็มเพลต #DEF ประกอบด้วยข้อมูลต่อไปนี้

-   ข้อมูลหัวข้อ เช่นกลุ่มภาษี เงื่อนไขการชำระเงิน และวิธีการชำระเงิน
-   ข้อมูลรายการ เช่นคำอธิบายการบริการ บัญชีรายได้ ราคาต่อหน่วย และยอดเงินใบแจ้งหนี้
-   ค่าธรรมเนียมสำหรับการจัดส่งหรือการจัดการ
-   การกระจายการลงบัญชีพร้อมกับรายละเอียดมิติทางการเงิน เช่นศูนย์ต้นทุนและหน่วยธุรกิจ

มีผลบังคับ คุณกำลังสร้างใบแจ้งหนี้ทั้งฉบับ และจะบันทึกเป็นเท็มเพลต คุณสามารถตั้งค่าเท็มเพลตด้วยการใช้หน้า **ใบแจ้งหนี้ที่เกิดซ้ำ** ได้

## <a name="assign-a-free-text-invoice-template-to-a-customer-and-enter-recurrence-details"></a>กำหนดเท็มเพลตใบแจ้งหนี้ข้อความอิสระให้กับลูกค้าและป้อนรายละเอียดการเกิดซ้ำ
หลังจากที่สร้างเท็มเพลต คุณต้องกำหนดเท็มเพลตให้แก่ลูกค้าที่คุณต้องการออกใบแจ้งหนี้ นอกจากนี้ คุณต้องระบุ เมื่อใด และบ่อยเพียงใด เพื่อที่จะใช้ใบแจ้งหนี้ได้ คุณสามารถกำหนดเท็มเพลตที่แท็บ **ใบแจ้งหนี้** ที่หน้าของ **ลูกค้า** ได้ เพิ่มเท็มเพลตในรายการ และอัพเดตข้อมูลต่อไปนี้:

-   วันที่เริ่มต้นและ อีกทางหนึ่งคือ วันที่สิ้นสุดสำหรับการเรียกเก็บเงินที่เกิดซ้ำ
-   ความถี่ของการเรียกเก็บเงินที่เกิดซ้ำ (ตัวอย่างเช่น ทุกวัน หรือ เดือนละครั้ง)
-   ยอดเงินการเรียกเก็บเงินสูงสุด (ถ้าจำเป็นต้องมีข้อมูลนี้)

ลูกค้าสามารถมีเท็มเพลตหลายเท็มเพลต ที่มีความถี่ที่แตกต่าง

## <a name="generate-the-recurring-invoices"></a>สร้างใบแจ้งหนี้ที่เกิดซ้ำ
ในหน้า **ใบแจ้งหนี้ที่เกิดซ้ำ**, จะมีงานที่ประมวลผลเท็มเพลใบแจ้งหนี้ที่เกิดซ้ำ ให้คุณระบุวันที่ในใบแจ้งหนี้และเท็มเพลตในการสร้างใบแจ้งหนี้ ใบแจ้งหนี้จะถูกสร้างขึ้น และกำหนดหมายเลขรหัสการเกิดซ้ำเดียวสำหรับใบแจ้งหนี้แต่ละกลุ่มที่ถูกประมวลผล

## <a name="post-recurring-free-text-invoices"></a>ลงรายการบัญชีใบแจ้งหนี้ข้อความอิสระ

หลังจากที่สร้างใบแจ้งหนี้ที่เกิดซ้ำ ใบแจ้งหนี้รหัสการเกิดซ้ำปรากฏในงานการลงรายการบัญชีในหน้า **ใบแจ้งหนี้ที่เกิดซ้ำ** คุณสามารถดูใบแจ้งหนี้ทั้งหมดสำหรับรหัสการเกิดซ้ำ โดยการคลิกลิงค์ ในระหว่างการตรวจทานใบแจ้งหนี้สำหรับรหัสการเกิดซ้ำ คุณสามารถลบใบแจ้งหนี้แต่ละรายการ การตั้งค่าการเกิดซ้ำของลูกค้าจะตั้งค่าสำหรับเท็มเพลตนั้นใหม่ เพื่อที่จะสามารถสร้างใหม่ได้ในภายหลัง คุณสามารถลงรายการบัญชีเดียว มาก หรือทั้งหมดของใบแจ้งหนี้สำหรับรหัสการเกิดซ้ำ ถ้าเปิดใช้งานลำดับงาน คุณต้องคลิก **ส่ง** ก่อนที่คุณสามารถลงรายการใบแจ้งหนี้

## <a name="print-recurring-free-text-invoices"></a>พิมพ์ใบแจ้งหนี้ข้อความอิสระที่เกิดซ้ำ

หลังจากที่ลงรายการบัญชีใบแจ้งหนี้ที่เกิดซ้ำ คุณสามารถพิมพ์ใบแจ้งหนี้จากหน้ารายการใบแจ้งหนี้ข้อความอิสระ คุณสามารถพิมพ์ใบแจ้งหนี้ที่เลือก หรือคุณสามารถเลือกช่วงของใบแจ้งหนี้ที่พิมพ์





[!INCLUDE[footer-include](../../includes/footer-banner.md)]
