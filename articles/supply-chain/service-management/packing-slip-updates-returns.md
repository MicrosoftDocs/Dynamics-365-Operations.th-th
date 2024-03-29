---
title: การอัพเดตบันทึกการจัดส่งสำหรับการส่งคืนสินค้า
description: 'ก่อนที่สามารถรับสินค้าที่ส่งคืนเข้าไว้ในสินค้าคงคลังได้ ต้องอัพเดตบันทึกการจัดส่งสำหรับใบสั่งที่สินค้านั้นเป็นส่วนประกอบอยู่ '
author: sorenva
ms.date: 05/01/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: CustPackingSlipJournalHistory, SalesParmPackingSlipTrackingInformation
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: sorenand
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 021cf6c0ff606e4b5a7139285fe7508283fb9fe2
ms.sourcegitcommit: 9166e531ae5773f5bc3bd02501b67331cf216da4
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 05/03/2022
ms.locfileid: "8675696"
---
# <a name="packing-slip-updates-for-returns"></a>การอัพเดตบันทึกการจัดส่งสำหรับการส่งคืนสินค้า  

[!include [banner](../includes/banner.md)]


ก่อนที่สามารถรับสินค้าที่ส่งคืนเข้าไว้ในสินค้าคงคลังได้ ต้องอัพเดตบันทึกการจัดส่งสำหรับใบสั่งที่สินค้านั้นเป็นส่วนประกอบอยู่  เช่นเดียวกับที่กระบวนการอัพเดตใบแจ้งหนี้คือการอัพเดตธุรกรรมทางการเงิน กระบวนการอัพเดตบันทึกการจัดส่งคือการอัพเดตทางกายภาพของเรกคอร์ดสินค้าคงคลัง ซึ่งหมายถึงว่าได้การยืนยันการเปลี่ยนแปลงที่สินค้าคงคลัง ในกรณีของการส่งคืน มีการใช้ขั้นตอนที่กำหนดให้กับการดำเนินการโอนการครอบครองในระหว่างการอัพเดตบันทึกการจัดส่ง

การอัพเดตบันทึกการจัดส่งสามารถประมวลผลในสมุดรายวันการมาถึงของสินค้าหรือในใบสั่งส่งคืนสินค้า

ในฐานะที่เป็นส่วนหนึ่งของการลงรายการบัญชีบันทึกการจัดส่ง คุณสามารถเชื่อมโยงหมายเลขอ้างอิงบันทึกการจัดส่งจากเอกสารการจัดส่งของลูกค้ากับรายการใบสั่งได้ ความสัมพันธ์นี้ไม่จำเป็น และใช้สำหรับการอ้างอิงเท่านั้น จะไม่สร้างการอัพเดตทางธุรกรรมใดๆ

ถ้าสินค้าที่ส่งคืนมาถึงไม่ครบตามจำนวนทั้งหมดที่คาดไว้ คุณควรรวมเฉพาะปริมาณที่ได้รับแล้วในการอัพเดตบันทึกการจัดส่งเท่านั้น ให้ปล่อยสินค้าส่วนที่เหลือไว้ในใบสั่ง จนกว่าส่วนที่เหลือของการจัดส่งคืนจะมาถึง

ถ้าสินค้าถูกส่งคืนจากฝ่ายตรวจสอบกลับไปยังแผนกจัดส่งและรับสินค้า เช่น เมื่อผู้ตรวจสอบสินค้าอย่างละเอียดไม่ทราบว่าจะจัดเก็บสินค้าไว้ที่ใดในสินค้าคงคลัง ต้องมีการอัพเดตบันทึกการจัดส่งที่สอดคล้องกันเพื่อให้ลงทะเบียนได้อย่างถูกต้อง และดำเนินการตามรหัสการโอนการครอบครองที่ระบุไว้ ตามผลการตรวจสอบสินค้า

เมื่อคุณอัพเดตบันทึกการจัดส่งสำหรับสินค้าที่ส่งคืนที่จะมาจากข้อตกลงการขาย ข้อผูกมัดเกี่ยวกับข้อตกลงการขายสำหรับสินค้าจะมีการอัพเดตโดยอัตโนมัติ เพื่อสะท้อนการเปลี่ยนแปลงในปริมาณหรือยอดเงิน 

## <a name="see-also"></a>ดูเพิ่มเติมที่

[ทำการอัพเดตใบแจ้งหนี้สำหรับการส่งคืนสินค้า](perform-invoice-updates-for-returns.md)

  




[!INCLUDE[footer-include](../../includes/footer-banner.md)]