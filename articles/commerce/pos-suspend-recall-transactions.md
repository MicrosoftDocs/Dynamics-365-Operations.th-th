---
title: ระงับและดำเนินการธุรกรรมต่อในจุดขายหน้าร้าน (POS)
description: บทความนี้อธิบายวิธีการที่ผู้ใช้สามารถระงับธุรกรรมที่กำลังดำเนินการ และจากนั้นดำเนินการต่อในภายหลัง หรือในการลงทะเบียนที่แตกต่างกันโดยการใช้ Dynamics 365 Commerce
author: josaw1
ms.date: 11/27/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.region: global
ms.author: josaw
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.custom: 261234
ms.assetid: 7cd68ecc-cc09-48ab-8cb8-48d5c304effa
ms.search.industry: Retail
ms.openlocfilehash: 0b85bdb043e0bffed83ad6ffcb9269773c89facf
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 08/12/2022
ms.locfileid: "9269093"
---
# <a name="suspend-and-resume-a-transaction-in-the-point-of-sale-pos"></a>ระงับและดำเนินการธุรกรรมต่อในจุดขายหน้าร้าน (POS)

[!include [banner](includes/banner.md)]


ผู้ใช้จุดขายหน้าร้าน (POS) สามารถระงับธุรกรรมที่อยู่ระหว่างดำเนินการ และจากนั้นดำเนินการต่อในภายหลัง หรือบนเครื่องบันทึกเงินสดอื่น ธุรกรรมมักจะถูกระงับเพื่อทำให้เครื่องบันทึกเงินสดว่างอย่างรวดเร็วสำหรับงานอื่น โดยไม่สูญเสียความคืบหน้าใดๆ บนธุรกรรมปัจจุบัน ตัวอย่างเช่น การเชื่อมโยงร้านค้าเริ่มต้นการประมวลผลธุรกรรมของลูกค้าบนอุปกรณ์เคลื่อนที่ แต่ต้องทำให้สมบูรณ์บนเครื่องบันทึกเงินสดที่มีลิ้นชักเงินสด ในกรณีนี้ การเชื่อมโยงร้านค้าสามารถระงับธุรกรรมบนอุปกรณ์เคลื่อนที่ และจากนั้นเรียกคืน และดำเนินการต่อไปบนเครื่องบันทึกเงินสดได้

## <a name="configure-suspend-and-resume-functionality"></a>ตั้งค่าคอนฟิกการระงับ และดำเนินการฟังก์ชันต่อ

### <a name="pos-operations"></a>การดำเนินงานของ POS

[การดำเนินงาน POS](pos-operations.md) สองรายการ อนุญาตให้การสนับสนุน POS หยุดชั่วคราว และดำเนินการสถานการณ์จำลองต่อไป คุณสามารถกำหนดการดำเนินการเหล่านี้ให้กับ [กริดปุ่ม](pos-screen-layouts.md) บนหน้าธุรกรรมหรือหน้าต้อนรับได้

- 503: ระงับธุรกรรม
- 504: เรียกคืนธุรกรรม

### <a name="receipt-template"></a>เท็มเพลตใบเสร็จ

สามารถตั้งค่าคอนฟิก POS เพื่อสร้างบันทึกที่จัดพิมพ์ เมื่อธุรกรรมถูกพักชั่วคราว จากนั้น สามารถใช้บันทึกนั้นเพื่อระบุ และเรียกคืนธุรกรรมในภายหลังได้อย่างรวดเร็ว

เมื่อต้องการเปิดใช้งาน POS เพื่อพิมพ์บันทึก คุณต้องเพิ่มรูปแบบใบเสร็จ **ระงับธุรกรรม** ไปยังโพรไฟล์ใบเสร็จของร้านค้า คุณสามารถออกแบบรูปแบบใบเสร็จ เพื่อให้มีการรวมหรือไม่รวมรายละเอียดเฉพาะเกี่ยวกับธุรกรรม ตัวอย่างเช่น รูปแบบสามารถมีบาร์โค้ดเพื่อสนับสนุนการสแกน

### <a name="receipt-numbering"></a>การกำหนดหมายเลขใบเสร็จ

เช่นกันกับชนิดของธุรกรรมอื่นๆ ของ POS ที่สร้างใบเสร็จที่พิมพ์ คุณสามารถกำหนดลำดับหมายเลขสำหรับธุรกรรมที่ระงับในส่วน **การกำหนดหมายเลขใบเสร็จ** ของโพรไฟล์ฟังก์ชันของร้านค้า

### <a name="void-when-closing-shift"></a>เป็นโมฆะเมื่อปิดกะ

คุณสามารถใช้ตัวเลือก **ยกเลิกเมื่อปิดกะ** เพื่อกำหนดให้ผู้ใช้ทำให้เสร็จสมบูรณ์ หรือยกเลิกธุรกรรมที่ระงับใดๆ ก่อนที่พวกเขาจะปิดกะของพวกเขาได้ ในระหว่างการดำเนินงาน **ปิดกะ** POS จะพร้อมต์ผู้ใช้ให้ดู หรือยกเลิกธุรกรรมที่ระงับคงค้างใดๆ

## <a name="suspend-and-resume-a-transaction"></a>ระงับและดำเนินการธุรกรรมต่อ

### <a name="suspend-a-transaction"></a>ระงับธุรกรรม

ผู้ใช้ที่มีสิทธิ์เพียงพอ และที่มีโครงร่างหน้าจอที่มีการดำเนินงาน **ระงับธุรกรรม** สามารถระงับธุรกรรม เพื่อให้สามารถเรียกได้ในภายหลัง หรือบนเครื่องบันทึกเงินสดอื่น

สามารถระงับธุรกรรมได้เฉพาะเมื่อ **ไม่** ประกอบด้วยชนิดของรายการต่อไปนี้:

- รายการการชำระเงินที่ใช้งานอยู่
- รายการบัตรของขวัญ (อาจออกบัตรของขวัญ หรือเพิ่มไปยังยอดดุลของบัตรของขวัญ)

ธุรกรรมที่ระงับไม่มีผลต่อข้อมูลการขายหรือข้อมูลความพร้อมใช้งานสินค้าคงคลังสำหรับร้านค้า

### <a name="resume-a-suspended-transaction"></a>ดำเนินงานธุรกรรมที่ระงับต่อ

สามารถเรียกคืนและดำเนินการธุรกรรมที่ระงับต่อในร้านค้าเดียวกันได้ โดยผู้ใช้ใดๆ ที่มีสิทธิ์เพียงพอ และที่มีโครงร่างที่รวมการดำเนินงาน **เรียกคืนธุรกรรม** ได้

เมื่อต้องการเรียกคืนธุรกรรมที่ระงับอย่างรวดเร็วและง่ายดาย สแกนบาร์โค้ดในบันทึกที่พิมพ์ ขณะที่คุณกำลังดูรายการของธุรกรรมจากการดำเนินงาน **เรียกคืนธุรกรรม**

### <a name="considerations-for-offline-mode"></a>ข้อควรพิจารณาสำหรับโหมดออฟไลน์

- ไม่สามารถดำเนินการธุรกรรมที่ถูกพักชั่วคราวใดๆ ต่อในโหมดออฟไลน์ได้ ขณะที่ POS อยู่ในโหมดออนไลน์ เนื่องจากข้อมูลไม่ตรงกับฐานข้อมูลแบบออฟไลน์
- ถ้าคุณระงับธุรกรรม ขณะที่ POS อยู่ในโหมดออฟไลน์ คุณสามารถเรียกคืนได้ในโหมดออฟไลน์ โดยที่ POS ไม่สลับไปยังโหมดออนไลน์ตลอดเวลานับตั้งแต่คุณระงับธุรกรรม เมื่อ POS ถูกสลับไปยังโหมดออนไลน์ ข้อมูลเกี่ยวกับธุรกรรมที่ระงับจะมีการย้ายไปยังฐานข้อมูลออนไลน์ และถูกลบออกจากฐานข้อมูลออฟไลน์ ดังนั้น ธุรกรรมที่สามารถดำเนินต่อได้ในโหมดออนไลน์เท่านั้น ถ้าคุณสลับ POS กลับไปยังโหมดออฟไลน์ คุณจะไม่สามารถกลับมาทำงานดังกล่าวธุรกรรมที่ระงับได้ เนื่องจากรายการเหล่านั้นถูกลบออกจากฐานข้อมูลออฟไลน์แล้ว

### <a name="void-a-suspended-transaction"></a>ยกเลิกธุรกรรมที่ระงับ

คุณสามารถยกเลิกธุรกรรมที่ระงับได้ โดยการเรียกคืนธุรกรรม และจากนั้น ดำเนินการดำเนินงาน **ยกเลิกธุรกรรม** หรือโดยการเลือกธุรกรรมในรายการ **เรียกคืนธุรกรรม** และเลือก **ยกเลิก** บนแถบแอป อีกทางหนึ่งคือ คุณสามารถตั้งค่าคอนฟิกร้านค้าเพื่อพร้อมท์ผู้ใช้ให้ยกเลิกธุรกรรมที่ระงับ เมื่อพวกเขาปิดกะของพวกเขา


[!INCLUDE[footer-include](../includes/footer-banner.md)]
