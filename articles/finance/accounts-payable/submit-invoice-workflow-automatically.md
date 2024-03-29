---
title: ส่งใบแจ้งหนี้ไปที่ระบบลำดับงานและจับคู่รายการใบรับสินค้า
description: บทความนี้อธิบายกระบวนการในการส่งใบแจ้งหนี้ของผู้จัดจำหน่ายไปยังระบบเวิร์กโฟลว์ และการจับคู่บรรทัดใบรับสินค้าที่ลงรายการบัญชีกับใบแจ้งหนี้ของผู้จัดจำหน่าย
author: abruer
ms.date: 02/11/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: twheeloc
ms.assetid: ''
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2017-09-08
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 960a08eb5e98cac034bbd41335b616ff41bf6fd4
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 06/03/2022
ms.locfileid: "8861631"
---
# <a name="submit-invoices-to-the-workflow-system-and-match-product-receipt-lines"></a>ส่งใบแจ้งหนี้ไปที่ระบบลำดับงานและจับคู่รายการใบรับสินค้า

[!include [banner](../includes/banner.md)]

บทความนี้อธิบายกระบวนการในการส่งใบแจ้งหนี้ของผู้จัดจำหน่ายไปยังระบบเวิร์กโฟลว์ และการจับคู่บรรทัดใบรับสินค้าที่ลงรายการบัญชีกับใบแจ้งหนี้ของผู้จัดจำหน่าย

## <a name="submitting-imported-vendor-invoices-to-the-workflow-system-and-matching-posted-product-receipt-lines-to-pending-vendor-invoice-lines"></a>การส่งใบแจ้งหนี้ของผู้จัดจำหน่ายที่นำเข้าไปยังระบบลำดับงาน และการจับคู่บรรทัดใบรับสินค้าที่ลงรายการบัญชีไปยังรายการใบแจ้งหนี้ของผู้จัดจำหน่าย

เนื่องจากเป็นส่วนหนึ่งของกระบวนการออกใบแจ้งหนี้ของบัญชีเจ้าหนี้ ใบแจ้งหนี้ที่นำเข้าสามารถส่งไปยังระบบลำดับงานโดยอัตโนมัติ คุณสามารถตั้งค่าคอนฟิกกระบวนการในการส่งใบแจ้งหนี้ที่นำเข้าไปยังระบบลำดับงานบนแท็บ **ระบบอัตโนมัติของใบแจ้งหนี้ของผู้จัดจำหน่าย** ของหน้า **พารามิเตอร์บัญชีเจ้าหนี้** (**บัญชีเจ้าหนี้ \> การตั้งค่า \> พารามิเตอร์บัญชีเจ้าหนี้**) กระบวนการส่งไปที่ลำดับงานจะรันในพื้นหลัง ที่ความถี่ที่คุณระบุ (รายชั่วโมง หรือรายวัน)

เมื่อคุณส่งใบแจ้งหนี้ไปยังระบบลำดับงานโดยอัตโนมัติ คุณต้องเริ่มต้นด้วยใบแจ้งหนี้ที่นำเข้า เพื่อให้แน่ใจว่าสามารถประมวลผลใบแจ้งหนี้ตั้งแต่เริ่มต้นจนเสร็จสิ้นได้โดยไม่มีการขัดจังหวะด้วยตนเอง คุณต้องรวมงานการลงรายการบัญชีแบบอัตโนมัติในการตั้งค่าคอนฟิกลำดับงาน ใบแจ้งหนี้ที่เกี่ยวข้องกับใบสั่งซื้อ (POs) และใบแจ้งหนี้ที่มีประเภทการจัดซื้อที่ไม่มี PO และรายการที่ไม่มีสต็อก จะถูกส่งไปยังระบบลำดับงานโดยอัตโนมัติ ใบแจ้งหนี้ที่ถูกป้อนด้วยตนเอง ต้องถูกส่งไปยังระบบลำดับงานด้วยตนเอง

ค่า **ถูกส่งโดย** ในลำดับงานคือ รหัสผู้ใช้ที่ถูกป้อนสำหรับงานพื้นหลัง **ส่งใบแจ้งหนี้ของผู้จัดจำหน่ายไปยังลำดับงาน** บนหน้า **ระบบอัตโนมัติของกระบวนการ** ผู้ใช้ที่มีรหัสผู้ใช้ที่จะสามารถเรียกคืนใบแจ้งหนี้จากระบบลำดับงานได้ตามต้องการ

## <a name="matching-posted-product-receipts-to-invoice-lines-that-have-a-three-way-matching-policy"></a>การจับคู่ใบรับสินค้าที่ลงรายการบัญชีกับบรรทัดใบแจ้งหนี้ที่มีนโยบายการจับคู่แบบสามทาง

โดยเป็นส่วนหนึ่งของกระบวนการออกใบแจ้งหนี้ของบัญชีเจ้าหนี้ระยะไกล ระบบสามารถจับคู่การรับสินค้าที่ลงรายการบัญชีกับรายการใบแจ้งหนี้โดยอัตโนมัติ ต้องมีการกำหนดนโยบายการจับคู่แบบสามทางสำหรับงานนี้ คุณลักษณะนี้จะพร้อมใช้งาน ถ้าคุณลักษณะ **ระบบอัตโนมัติของใบแจ้งหนี้ของผู้จัดจำหน่าย** ถูกเปิดใช้งานบนหน้า **การจัดการคุณลักษณะ**

กระบวนการนี้จะรันจนกว่าปริมาณในใบรับสินค้าที่ตรงกันเท่ากับปริมาณใบแจ้งหนี้ อย่างไรก็ตาม หากมีใบรับสินค้าหลายใบสำหรับบรรทัดใบแจ้งหนี้เดียว คุณจะต้องรันกระบวนการนี้หลายครั้งเพื่อให้ได้ปริมาณที่ตรงกันทั้งหมด คุณสามารถระบุจำนวนครั้งสูงสุดที่ระบบควรพยายามจับคู่ใบรับสินค้ากับบรรทัดใบแจ้งหนี้ ก่อนที่จะสรุปว่ากระบวนการล้มเหลว กระบวนการนี้จะรันในพื้นหลัง ทั้งรายชั่วโมงหรือรายวัน 

คุณสามารถรันกระบวนการจับคู่อัตโนมัติโดยเป็นส่วนหนึ่งของกระบวนการสำหรับการส่งใบแจ้งหนี้ไปยังระบบลำดับงาน อีกทางหนึ่ง คือคุณสามารถรันเป็นกระบวนการแบบสแตนด์อโลน คุณสามารถตั้งค่าคอนฟิกการตั้งค่าสำหรับกระบวนการจับคู่ใบรับสินค้ากับรายการใบแจ้งหนี้บนแท็บ **ระบบอัตโนมัติของใบแจ้งหนี้ของผู้จัดจำหน่าย** ของหน้า **พารามิเตอร์บัญชีเจ้าหนี้** (**บัญชีเจ้าหนี้ \> การตั้งค่า \> พารามิเตอร์บัญชีเจ้าหนี้**)

บรรทัดใบแจ้งหนี้ที่มีนโยบายการจับคู่แบบสามทาง ที่ซึ่งปริมาณการรับสินค้าที่ตรงกันน้อยกว่าปริมาณในใบแจ้งหนี้ จะถูกรวมอยู่ในกระบวนจับคู่กับใบรับสินค้าแบบอัตโนมัติ

เมื่อต้องการดูสถานะ **การจับคู่ล่าสุด** สำหรับใบแจ้งหนี้ที่ไม่ได้เป็นส่วนหนึ่งของกระบวนการส่งไปยังลำดับงานแบบอัตโนมัติ ให้เปิดใบแจ้งหนี้จากหน้า **ใบแจ้งหนี้ของผู้จัดจำหน่าย** เมื่อคุณดูใบแจ้งหนี้ จะมีการอัปเดตข้อมูลการตรวจสอบความถูกต้องของการจับคู่ สถานะ **การจับคู่ล่าสุด** โดยอัตโนมัติโดยใช้งานพื้นหลัง **ตรวจสอบความถูกต้องของการจับคู่ใบแจ้งหนี้** คุณสามารถตั้งค่าคอนฟิกกระบวนการอัปเดตสถานะ **การจับคู่ล่าสุด** บนแท็บ **กระบวนการพื้นหลัง** ของหน้า **ระบบอัตโนมัติของกระบวนการ** (**การดูแลระบบ\> การตั้งค่า\> ระบบอัตโนมัติของกระบวนการ**)

บรรทัดใบแจ้งหนี้จะถูกแยกออกจากการประมวลผลแบบอัตโนมัติ ถ้าเป็นไปตามเงื่อนไขใดๆ ต่อไปนี้:

- ค่า **สถานะการจับคู่การรับสินค้าแบบอัตโนมัติ** ของบรรทัดใบแจ้งหนี้ **ล้มเหลว**
- มีการใช้ใบแจ้งหนี้
- ใบแจ้งหนี้อยู่ในระบบลำดับงาน


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
