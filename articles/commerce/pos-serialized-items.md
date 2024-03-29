---
title: ทำงานกับสินค้าที่กำหนดหมายเลขลำดับประจำสินค้าใน POS
description: บทความนี้อธิบายวิธีการจัดการสินค้าที่ที่กำหนดหมายเลขลำดับประจำสินค้าในแอปพลิเคชันการขายหน้าร้านของ (POS)
author: boycezhu
ms.date: 01/08/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.region: global
ms.author: boycez
ms.search.validFrom: ''
ms.dyn365.ops.version: 10.0.11
ms.openlocfilehash: 8a715a9d025f36656506daeb9e611bfacdafa102
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 06/03/2022
ms.locfileid: "8880040"
---
# <a name="work-with-serialized-items-in-the-pos"></a>ทำงานกับสินค้าที่กำหนดหมายเลขลำดับประจำสินค้าใน POS

[!include [banner](includes/banner.md)]

ร้านค้าปลีกจํานวนมากขายผลิตภัณฑ์ที่จําเป็นต้องมีการควบคุมการกำหนดหมายเลขลำดับประจำสินค้า ผลิตภัณฑ์เหล่านี้เรียกว่า *สินค้าที่กำหนดหมายเลขลำดับประจำสินค้า* ผู้ค้าปลีกบางรายอาจต้องการรักษาหมายเลขลําดับประจําสินค้าในร้านค้าหรือสินค้าคงคลังของคลังสินค้าเพื่อวัตถุประสงค์ในการติดตาม ผู้ค้าปลีกรายอื่นๆ อาจต้องการเก็บหมายเลขลําดับประจําสินค้าในระหว่างกระบวนการขาย เพื่อวัตถุประสงค์ในการบริการและการรับประกัน บทความนี้อธิบายวิธีการจัดการสินค้าที่กำหนดหมายเลขลำดับประจำสินค้าในแอปพลิเคชันการขายหน้าร้านของ (POS) ของ Microsoft Dynamics 365 Commerce

## <a name="serial-number-configurations"></a>การตั้งค่าคอนฟิกหมายเลขลำดับประจำสินค้า

สินค้าจะถือเป็นสินค้าที่กำหนดหมายเลขลำดับประจำสินค้า ถ้าถูกกำหนดกลุ่มมิติการติดตามที่ตั้งค่าเพื่อให้ใช้หมายเลขลำดับประจำสินค้าได้ ในศูนย์ควบคุม Commerce บนหน้า **หน้ากลุ่มมิติการติดตาม** ให้เลือกตัวเลือก **ใช้งานอยู่** เพื่อเปิดใช้งานหมายเลขลำดับประจำสินค้าสำหรับกระบวนการสินค้าคงคลัง หรือเลือกตัวเลือก **ใช้งานอยู่ในกระบวนการขาย** เพื่อเปิดใช้งานหมายเลขลำดับประจำสินค้าสำหรับกระบวนการขาย

บนแท็บด่วน **มิติการติดตาม** ให้เปิดพารามิเตอร์ **การรับสินค้าที่ว่างเปล่า** เพื่อให้หมายเลขลําดับประจําสินค้าเป็นข้อมูลที่ไม่จำเป็นต้องระบุระหว่างกระบวนการรับสินค้าคงคลังของสินค้าที่กำหนดหมายเลขลำดับ การปิดพารามิเตอร์นี้บังคับใช้หมายเลขลำดับประจำสินค้าเป็นข้อมูลที่ต้องระบุ ในทำนองเดียวกัน พารามิเตอร์ **ใช้การตัดสินค้าที่ว่างเปล่าได้** ควบคุมว่าต้องใช้หมายเลขลำดับประจำสินค้าระหว่างกระบวนการจัดส่งสินค้าคงคลังหรือไม่

> [!NOTE]
> เมื่อต้องการใช้การดำเนินการ POS สำหรับ **สินค้าคงคลังขาเข้า** และ **สินค้าคงคลังขาออก** เพื่อลงทะเบียนหรือตรวจสอบความถูกต้องของหมายเลขลำดับประจำสินค้ากับสินค้าที่กำหนดหมายเลข คุณต้องตั้งค่าคอนฟิกสินค้าที่จะกำหนดกลุ่มมิติการติดตามที่ตั้งค่าเพื่อให้ใช้หมายเลขลำดับประจำสินค้าได้สำหรับตัวเลือก **ใช้งานอยู่** ไม่ใช่ตัวเลือก **ใช้งานอยู่ในกระบวนการขาย**

## <a name="serial-number-management-page"></a>หน้าการจัดการหมายเลขลำดับประจำสินค้า

ในการดำเนินการ POS สำหรับ **สินค้าคงคลังขาเข้า** และ **สินค้าคงคลังขาออก** ถ้าสินค้าที่มีการเลือก การรับสินค้า หรือจัดส่งเป็นสินค้าที่กำหนดหมายเลข บานหน้าต่าง **รายละเอียด** จะมีตัวเลือก **จัดการหมายเลขลำดับประจำสินค้า** ที่เชื่อมโยงกับหน้า **จัดการหมายเลขลำดับประจำ สินค้า** ซึ่งคุณสามารถลงทะเบียนหรือตรวจสอบความถูกต้องของหมายเลขลำดับประจำสินค้าของสินค้าได้ อีกวิธีหนึ่งคือ คุณสามารถเปิดหน้า **การจัดการหมายเลขลำดับประจำสินค้า** โดยการเลือก **หมายเลขลำดับประจำสินค้า** บนแถบแอปของมุมมองรายละเอียดใบสั่ง หรือโดยการเลือกตัวเลือก **จัดการหมายเลขลำดับประจำสินค้า** ในกล่องโต้ตอบที่จะทำให้คุณในระหว่างกระบวนการรับ 

หน้า **การจัดการหมายเลขลําดับประจําสินค้า** จะแสดงรายการหมายเลขลําดับประจําสินค้าที่เปิดอยู่ทั้งหมดที่รอการลงทะเบียนหรือการตรวจสอบความถูกต้อง อาจมีแท็บสองแท็บบนหน้านี้: หนึ่งแท็บสําหรับรายการปัจจุบัน และหนึ่งแท็บสําหรับรายการที่กำหนดหมายเลขลำดับประจำสินค้าตามลําดับ

ฟิลด์ **สถานะ** บนหน้า **การจัดการหมายเลขลำดับประจำสินค้า** ให้ข้อมูลเกี่ยวกับระยะปัจจุบันที่แต่ละหมายเลขลําดับประจําสินค้าอยู่:

- **ไม่ได้ลงทะเบียน** – ไม่ได้ระบุหมายเลขลําดับประจําสินค้า หรือยังไม่ได้ตรวจสอบความถูกต้องของหมายเลขลําดับประจําสินค้าล่วงหน้า (ในกระบวนการรับสินค้า)
- **การลงทะเบียน** – หมายเลขลําดับประจําสินค้าได้รับการลงทะเบียน และบันทึกไว้ในฐานข้อมูลช่องทางของร้านค้า หรือมีการลงทะเบียนหมายเลขลําดับประจําสินค้าล่วงหน้า เฉพาะหมายเลขลำดับประจำสินค้าที่มีสถานะ **กำลังลงทะเบียน** เท่านั้นที่จะถูกส่งไปยังสํานักงานใหญ่ของ Commerce เมื่อคุณเสร็จสิ้นการรับหรือการเก็บแพคส่งสินค้า

## <a name="receive-serialized-items"></a>รับสินค้าที่กำหนดหมายเลข

การดําเนินการ POS สำหรับ **สินค้าคงคลังขาเข้า** ช่วยให้ผู้ใช้สามารถปฏิบัติงานต่อไปนี้สําหรับสินค้าที่กำหนดหมายเลขลำดับประจำสินค้า:

- ลงทะเบียนหมายเลขลำดับประจำสินค้ากับสินค้าที่กำหนดหมายเลขลำดับประจำสินค้า เมื่อได้รับสินค้าในร้านค้าผ่านใบสั่งซื้อ
- ตรวจสอบความถูกต้องหมายเลขลำดับประจำสินค้าที่ลงทะเบียนล่วงหน้ากับสินค้าที่กำหนดหมายเลขลำดับประจำสินค้า เมื่อได้รับสินค้าในร้านค้าผ่านใบสั่งซื้อหรือใบสั่งโอนย้าย

### <a name="register-serial-numbers-against-serialized-items"></a>ลงทะเบียนหมายเลขลําดับประจําสินค้าเทียบกับสินค้าที่กำหนดหมายเลขลำดับประจำสินค้า

สําหรับใบสั่งซื้อ คุณจะได้รับการแจ้งด้วยกล่องโต้ตอบที่มีตัวเลือก **จัดการหมายเลขลําดับประจําสินค้า** ในระหว่างกระบวนการรับสินค้าที่กำหนดหมายเลขลำดับ คุณสามารถเลือกตัวเลือกนั้นเพื่อเปิดหน้า **การจัดการหมายเลขลำดับประจำสินค้า** และเริ่มการลงทะเบียนหมายเลขลําดับประจําสินค้า คุณยังสามารถข้ามขั้นตอนนี้ในระหว่างกระบวนการรับ และใส่ข้อมูลในภายหลัง ก่อนการลงรายการบัญชีการรับสินค้า

โดยค่าเริ่มต้น จะมีการแสดงแท็บสำหรับสินค้าปัจจุบัน บรรทัดหมายเลขลำดับประจำสินค้าทั้งหมดมีค่าหมายเลขลำดับประจำสินค้าที่ว่างเปล่า และสถานะที่ **ไม่ได้ลงทะเบียน** คุณสามารถสแกนบาร์โค้ดหมายเลขลำดับประจำสินค้า หรือคุณสามารถเลือก **หมายเลขลำดับประจำสินค้า** บนแถบแอป เพื่อป้อนหมายเลขลำดับประจำสินค้าอย่างต่อเนื่อง หมายเลขลำดับประจำสินค้าที่คุณป้อนจะปรากฏในรายการ และสถานะมีการเปลี่ยนแปลงเป็น **กำลังลงทะเบียน** จำนวนสูงสุดของหมายเลขลำดับประจำสินค้าที่คุณสามารถลงทะเบียนในรายการเท่ากับปริมาณที่ได้รับ ถ้าคุณทำข้อผิดพลาด คุณสามารถเลือก **แก้ไข** หรือ **ล้าง** ในบานหน้าต่าง **รายละเอียด** เพื่อทำการเปลี่ยนแปลงหมายเลขลำดับประจำสินค้าที่คุณป้อน

นอกจากนี้ คุณยังสามารถลงทะเบียนหมายเลขลำดับประจำสินค้าบนแท็บ **สินค้าที่กำหนดหมายเลขลำดับประจำสินค้าทั้งหมด** ของหน้า **การจัดการหมายเลขลำดับประจำสินค้า** ในรายการนี้ ให้เลือกสินค้าที่คุณต้องการลงทะเบียนหมายเลขลำดับประจำสินค้าเทียบ

### <a name="validate-serial-numbers-on-serialized-items"></a>ตรวจสอบความถูกต้องของหมายเลขลำดับประจำสินค้าของสินค้าที่กำหนดหมายเลขลำดับประจำสินค้า

สำหรับใบสั่งโอนย้าย ด้านขาออกต้องลงทะเบียนล่วงหน้าหมายเลขลำดับประจำสินค้าของสินค้าที่กำหนดหมายเลขลำดับประจำสินค้าในระหว่างกระบวนการจัดส่ง สำหรับใบสั่งซื้อ ผู้จัดจำหน่ายอาจระบุข้อมูลหมายเลขลำดับประจำสินค้าโดยใช้การแจ้งเตือนการจัดส่งล่วงหน้า (ASN) และคุณสามารถลงทะเบียนล่วงหน้าหมายเลขของสินค้าที่จะจัดส่งได้ ในทั้งสองกรณี หมายเลขลำดับประจำสินค้าจะทราบก่อนการรับสินค้า ดังนั้น ในด้านขาเข้า คุณเพียงแค่ต้องตรวจสอบว่าคุณได้รับสิ่งที่คุณควรได้รับ

เมื่อต้องการตรวจสอบความถูกต้องของหมายเลขลำดับประจำสินค้า คุณสามารถเปิดหน้า **การจัดการหมายเลขลำดับประจำสินค้า** ระหว่างกระบวนการรับสินค้าหรือเมื่อใดก็ได้ก่อนที่จะมีการลงรายการบัญชีการรับสินค้า สำหรับสินค้าแต่ละรายการที่กำหนดหมายเลขลำดับประจำสินค้าที่ลงทะเบียนล่วงหน้า หมายเลขลำดับประจำสินค้าทั้งหมดจะได้รับการตั้งค่าเป็นสถานะเริ่มต้นที่ **ไม่ได้ลงทะเบียน** ในหน้านี้โดยอัตโนมัติ เมื่อต้องการตรวจสอบความถูกต้องของหมายเลขลำดับประจำสินค้า คุณสามารถสแกนหรือป้อนหมายเลขลำดับ เมื่อมีการป้อนหมายเลขลำดับประจำสินค้า ใบสมัครจะตรวจสอบว่ามีการจับคู่กับหมายเลขลำดับประจำสินค้าลงทะเบียนล่วงหน้าหรือไม่ ถ้าตรงกัน สถานะจะถูกเปลี่ยนเป็น **กำลังลงทะเบียน** มิฉะนั้น คุณได้รับข้อความแสดงข้อผิดพลาด อีกทางหนึ่งคือ คุณสามารถเลือกหมายเลขลำดับประจำสินค้าได้โดยตรง แล้วเลือก **ตรวจสอบความถูกต้องของหมายเลขลำดับประจำสินค้า** ในบานหน้าต่าง **รายละเอียด** เพื่อทำเครื่องหมายหมายเลขลำดับประจำสินค้าเป็นตรวจสอบความถูกต้องแล้วได้อย่างรวดเร็ว จำนวนสูงสุดของหมายเลขลำดับประจำสินค้าที่คุณสามารถตรวจสอบความถูกต้องในรายการเท่ากับปริมาณที่ได้รับ

นอกจากนี้ คุณยังสามารถตรวจสอบความถูกต้องหมายเลขลำดับประจำสินค้าบนแท็บ **สินค้าที่กำหนดหมายเลขลำดับประจำสินค้าทั้งหมด** ของหน้า **การจัดการหมายเลขลำดับประจำสินค้า** ในรายการนี้ ให้เลือกสินค้าที่คุณต้องการตรวจสอบความถูกต้องหมายเลขลำดับประจำสินค้าเทียบ

## <a name="ship-serialized-items"></a>จัดส่งสินค้าที่มีหมายเลขลำดับ

คุณสามารถใช้การดำเนินงาน POS สำหรับ **สินค้าคงคลังขาออก** เพื่อลงทะเบียนหมายเลขลำดับประจำสินค้ากับสินค้าที่กำหนดหมายเลขลำดับเมื่อจัดส่งสินค้าออกจากร้านค้าปัจจุบันผ่านทางใบสั่งโอนย้าย

### <a name="register-serial-numbers-against-serialized-items"></a>ลงทะเบียนหมายเลขลําดับประจําสินค้าเทียบกับสินค้าที่กำหนดหมายเลขลำดับประจำสินค้า

สําหรับใบสั่งโอนย้าย คุณจะได้รับการแจ้งด้วยกล่องโต้ตอบที่มีตัวเลือก **จัดการหมายเลขลําดับประจําสินค้า** ในระหว่างกระบวนการส่งสินค้าที่กำหนดหมายเลขลำดับประจำสินค้า คุณสามารถเลือกตัวเลือกเพื่อเปิดหน้า **การจัดการหมายเลขลำดับประจำสินค้า** และเริ่มการลงทะเบียนหมายเลขลําดับประจําสินค้า คุณยังสามารถข้ามขั้นตอนนี้ในระหว่างกระบวนการส่ง และใส่ข้อมูลในภายหลัง ก่อนการลงรายการบัญชีการส่งสินค้า

โดยค่าเริ่มต้น จะมีการแสดงแท็บสำหรับสินค้าปัจจุบัน บรรทัดหมายเลขลำดับประจำสินค้าทั้งหมดมีค่าหมายเลขลำดับประจำสินค้าที่ว่างเปล่า และสถานะที่ **ไม่ได้ลงทะเบียน** คุณสามารถสแกนบาร์โค้ดหมายเลขลำดับประจำสินค้า หรือคุณสามารถเลือก **หมายเลขลำดับประจำสินค้า** บนแถบแอป เพื่อป้อนหมายเลขลำดับประจำสินค้าอย่างต่อเนื่อง หมายเลขลำดับประจำสินค้าที่คุณป้อนจะปรากฏในรายการ และสถานะมีการเปลี่ยนแปลงเป็น **กำลังลงทะเบียน** จำนวนสูงสุดของหมายเลขลำดับประจำสินค้าที่คุณสามารถลงทะเบียนในรายการเท่ากับปริมาณที่จัดส่ง ถ้าคุณทำข้อผิดพลาด คุณสามารถเลือก **แก้ไข** หรือ **ล้าง** ในบานหน้าต่าง **รายละเอียด** เพื่อทำการเปลี่ยนแปลงหมายเลขลำดับประจำสินค้าที่คุณป้อน

นอกจากนี้ คุณยังสามารถลงทะเบียนหมายเลขลำดับประจำสินค้าบนแท็บ **สินค้าที่กำหนดหมายเลขลำดับประจำสินค้าทั้งหมด** ของหน้า **การจัดการหมายเลขลำดับประจำสินค้า** ในรายการนี้ ให้เลือกสินค้าที่คุณต้องการลงทะเบียนหมายเลขลำดับประจำสินค้าเทียบ

หรือคุณสามารถเปิดใช้งานการตรวจสอบความพร้อมใช้งานของหมายเลขลำดับประจำสินค้าในระหว่างการลงทะเบียนหมายเลขลำดับประจำสินค้ากับใบสั่งโอนย้ายขาออก เมื่อมีการตรวจสอบคามถูกต้อง ถ้าคุณพยายามจัดส่งหมายเลขลำดับประจำสินค้าที่ไม่มีอยู่ในสินค้าคงคลังของร้านค้าที่จัดส่ง คุณจะได้รับข้อความแสดงข้อผิดพลาดและต้องระบุหมายเลขอื่น

เมื่อต้องการเปิดใช้งานการตรวจสอบความถูกต้องดังกล่าวในฐานะที่เป็นข้อกำหนดเบื้องต้น คุณต้องจัดกำหนดการต่อไปนี้ให้เรียกใช้แบบการเกิดซ้ำ:

- **Retail และ Commerce** > **Retail และ Commerce IT** > **ผลิตภัณฑ์และสินค้าคงคลัง** > **ความพร้อมใช้งานของผลิตภัณฑ์ที่มีมิติการติดตาม**
- **Retail และ Commerce** > **กำหนดการกระจาย** > **1130** (**ความพร้อมใช้งานของผลิตภัณฑ์**)

## <a name="sell-serialized-items-in-pos"></a>ขายสินค้าที่มีหมายเลขลำดับใน POS

แม้ว่าแอปพลิเคชัน POS จะสนับสนุนการขายสินค้าที่มีหมายเลขลำดับเสมอใน Commerce รุ่น 10.0.17 และหลังจากนั้น องค์กรสามารถเปิดใช้งานฟังก์ชันที่ปรับปรุงตรรกะทางธุรกิจที่ทริกเกอร์เมื่อขายผลิตภัณฑ์ที่มีการตั้งค่าคอนฟิกไว้ให้กับการติดตามหมายเลขลำดับประจำสินค้า

เมื่อเปิดใช้งานคุณลักษณะ **การตรวจสอบความถูกต้องของหมายเลขหมายเลขลำดับประจำสินค้าในการบันทึกใบสั่ง POS และการเติมสินค้าตามใบสั่ง** การตั้งค่าคอนฟิกผลิตภัณฑ์ต่อไปนี้จะถูกประเมินเมื่อขายผลิตภัณฑ์ที่เป็นอนุกรมใน POS:

- การตั้งค่า **ชนิดลำดับประจำสินค้า** สำหรับผลิตภัณฑ์ (**ใช้งานอยู่** หรือ **ใช้งานอยู่ในการขาย**)
- การตั้งค่า **การตัดสินค้าที่ว่างเปล่าได้** สำหรับผลิตภัณฑ์
- การตั้งค่า **สินค้าคงคลังค่าลบทางกายภาพ** ของสินค้าและ/หรือคลังสินค้าขาย

### <a name="active-serial-configurations"></a>การตั้งค่าคอนฟิกหมายเลขลำดับประจำสินค้าที่ใช้งาน

เมื่อขายสินค้าใน POS ที่มีการตั้งค่าคอนฟิกด้วยมิติการติดตามหมายเลขลำดับประจำสินค้า **ที่ใช้งาน** POS จะเริ่มต้นตรรกะการตรวจสอบความถูกต้องซึ่งป้องกันไม่ให้ผู้ใช้การขายสินค้าที่กำหนดหมายเลขลำดับประจำสินค้าเสร็จสมบูรณ์ด้วยหมายเลขลำดับประจำสินค้าที่จะไม่พบในสินค้าคงคลังปัจจุบันของคลังสินค้าขาย มีข้อยกเว้นสองข้อยกเว้นของกฎการตรวจสอบความถูกต้องนี้:

- หากสินค้ามีการตั้งค่าคอนฟิกด้วยการเปิดใช้งาน **การตัดสินค้าที่ว่างเปล่าได้** ผู้ใช้สามารถข้ามรายการของหมายเลขลำดับประจำสินค้าและขายสินค้าที่ไม่มีการกำหนดหมายเลขลำดับประจำสินค้า
- หากสินค้าและ/หรือคลังสินค้าขายมีการตั้งค่าคอนฟิกด้วยการเปิดใช้งาน **สินค้าคงคลังค่าลบทางกายภาพ** แอปพลิเคชันจะยอมรับและขายหมายเลขลำดับประจำสินค้า ที่จะไม่สามารถยืนยันได้ให้อยู่ในสินค้าคงคลังที่คลังสินค้าที่สินค้านั้นจะถูกขายด้วย โครงแบบนี้อนุญาตให้รายการความเคลื่อนไหวของสินค้าคงคลังหมายเลขสินค้า/หมายเลขลำดับประจำสินค้าที่จะเป็นลบได้ ดังนั้นระบบจะอนุญาตให้ขายหหมายเลขลำดับประจำสินค้า ที่ไม่ทราบค่าได้

> [!IMPORTANT]
> เพื่อความแน่ใจว่าแอปพลิเคชัน POS สามารถตรวจสอบความถูกต้องได้อย่างถูกต้องว่าหมายเลขลำดับประจำสินค้าได้ขายให้กับสินค้าชนิดหมายเลขลำดับประจำสินค้า **ใช้งานอยู่** ยู่ในสินค้าคงคลังของคลังสินค้าขายหรือไม่ iจึงต้องให้องค์กรรันงาน **ความพร้อมใช้งานของผลิตภัณฑ์โดยมีงานมิติการติดตาม** ในศูนย์ควบคุม Commerce และงานการกระจายผลิตภัณฑ์ **1130** ที่มีอยู่ผ่านศูนย์ควบคุม Commerce บ่อยครั้ง เมื่อได้รับสินค้าคงคลังที่กำหนดหมายเลขลำดับประจำสินค้าใหม่เข้าในคลังสินค้าขาย เพื่อให้ POS ตรวจสอบความถูกต้องของความพร้อมของสินค้าคงคลังของหมายเลขลำดับประจำสินค้าชิ้นที่ขาย สินค้าคงคลังหลักต้องอัพเดตฐานข้อมูลช่องทางด้วยข้อมูลความพร้อมของสินค้าคงคลังล่าสุด งาน **ความพร้อมใช้งานของผลิตภัณฑ์โดยมีงานมิติการติดตาม** จะรับสแนปช็อตปัจจุบันของสินค้าคงคลังหลัก รวมถึงหมายเลขลำดับประจำสินค้า ในคลังสินค้าของบริษัททั้งหมด งานการกระจาย **1130** จะรับสแนปช็อตสินค้าคงคลังนั้นและแบ่งปันกับฐานข้อมูลช่องทางที่ตั้งค่าคอนฟิกไว้ทั้งหมด

### <a name="active-in-sales-process-serial-configurations"></a>ใช้งานในการตั้งค่าคอนฟิกหมายเลขลำดับประจำสินค้ากระบวนการขาย

สินค้าที่จัดโครงแบบด้วยมิติลหมายเลขลำดับประจำสินค้าโครงแบบเป็น **ใช้งานอยู่ในกระบวนการขาย** ไม่ผ่านตรรกะการตรวจสอบความถูกต้องของสินค้าคงคลังใดๆ เนื่องจากการตั้งค่าคอนฟิกนี้หมายความว่าหมายเลขลำดับประจำสินค้าของสินค้าคงคลังไม่ได้ถูกลงทะเบียนล่วงหน้าเข้าในสินค้าคงคลังและหมายเลขลำดับประจำสินค้า จะถูกรวบรวมไว้ในเวลาที่ขาย เท่านั้น  

ถ้ามีการตั้งค่าคอนฟิก **การตัดสินค้าที่ว่างเปล่าได้** สำหรับสินค้าที่ตั้งค่า **ใช้งานอยู่ในกระบวนการขาย** หมายเลขลำดับประจำสินค้าสามารถข้ามได้ หากไม่ได้ตั้งค่าคอนฟิก **การตัดสินค้าที่ว่างเปล่าได้** แอปพลิเคชันจะกําหนดให้ผู้ใช้ป้อนหมายเลขลำดับประจำสินค้า แม้ว่าจะไม่มีการตรวจสอบความถูกต้องกับสินค้าคงคลังที่มีอยู่

### <a name="apply-serial-numbers-during-creation-of-pos-transactions"></a>ใช้หมายเลขลำดับประจำสินค้าระหว่างการสร้างธุรกรรม POS

แอปพลิเคชัน POS จะแจ้งให้ผู้ใช้ทราบหมายเลขลำดับประจำสินค้าทันทีเมื่อขายสินค้าที่กำหนดหมายเลขลำดับประจำสินค้า แต่แอปพลิเคชันจะอนุญาตให้ผู้ใช้ข้ามรายการหมายเลขลำดับประจำสินค้าไปยังจุดใดจุดหนึ่งในกระบวนการขาย เมื่อผู้ใช้เริ่มรวบรวมข้อมูลการเบิกสินค้า แอปพลิเคชันจะบังคับใช้และกําหนดให้ต้องมีการป้อนหมายเลขลำดับประจำสินค้าให้กับสินค้าใด ๆ ที่ไม่ได้ตั้งค่าคอนฟิกให้ตอบสนองโดยผ่านการจัดส่งหรือการเบิกสินค้าในอนาคต สินค้าที่มีหมายเลขลำดับใดๆ ที่ตั้งค่าคอนฟิกไว้ว่าการเติมสินค้าด้วยเงินสดและสินค้ายกไปหรือยกไปที่กําหนดให้ผู้ใช้ต้องเก็บหมายเลขลำดับประจำสินค้า (หรือตกลงที่จะปล่อยว่างไว้หากการตั้งค่าสินค้าอนุญาต) ก่อนที่จะขายให้เสร็จสิ้น

สำหรับสินค้าที่มีหมายเลขลำดับที่ขายเพื่อเบิกสินค้าหรือจัดส่งสินค้าในอนาคต ผู้ใช้ POS สามารถข้ามการป้อนหหมายเลขลำดับประจำสินค้าได้เริ่มแรก และยังคงสร้างใบสั่งของลูกค้าให้เสร็จสมบูรณ์   

> [!NOTE]
> เมื่อขายหรือเติมสินค้าที่มีหมายเลขลำดับผ่านแอปพลิเคชัน POS จะบังคับใช้ปริมาณ "1" กับสินค้าที่มีหมายเลขลำดับในธุรกรรมการขาย นี่เป็นผลที่ได้ของวิธีการติดตามข้อมูลหมายเลขลำดับประจำสินค้าในบรรทัดการขาย เมื่อขายหรือตอบสนองธุรกรรมเกี่ยวกับสินค้าที่มีหมายเลขลำดับหลายรายการผ่าน POS รายการขายแต่ละรายการจะต้องได้รับการตั้งค่าคอนฟิกด้วยปริมาณ "1" เท่านั้น 

### <a name="apply-serial-numbers-during-customer-order-fulfillment-or-pickup"></a>ใช้หมายเลขลำดับประจำสินค้าระหว่างการเติมสินค้าตามใบสั่งของลูกค้าหรือการเบิกสินค้า

เมื่อเติมสินค้าตามรายการใบสั่งของลูกค้าเพื่อให้ผลิตภัณฑ์ที่มีหมายเลขลำดับโดยใช้การดําเนิน **การเติมสินค้าตามใบสั่ง** ใน POS POS จะบังคับใช้การรวบรวมข้อมูลหมายเลขลำดับประจำสินค้าก่อนการเติมสินค้าขั้นสุดท้าย ดังนั้น หากไม่มีการจัดเตรียมหมายเลขลำดับประจำสินค้าในระหว่างกระบวนการรวบรวมใบสั่งครั้งแรก หมายเลขลำดับประจำสินค้าต้องรวบรวมระหว่างกระบวนการเบิกสินค้า แพ็ค หรือจัดส่งใน POS มีการตรวจสอบความถูกต้องในแต่ละขั้นตอน และผู้ใช้จะได้รับการขอข้อมูลหมายเลขลำดับประจำสินค้าเท่านั้นถ้าข้อมูลหมายเลขลำดับประจำสินค้าขาดหายไปหรือไม่ถูกต้องอีกต่อไป ตัวอย่างเช่น หากผู้ใช้ข้ามขั้นตอนการเบิกสินค้าหรือแพ็คและเริ่มต้นการจัดส่งสินค้าทันที และยังไม่ได้ลงทะเบียนหมายเลขลำดับประจำสินค้าให้กับรายการ POS จะต้องป้อนหมายเลขลำดับประจำสินค้าก่อนทําให้ขั้นตอนใบแจ้งหนี้ขั้นสุดท้ายเสร็จสมบูรณ์ เมื่อบังคับการรวบรวมข้อมูลหมายเลขลำดับประจำสินค้าในระหว่างการดําเนินการเติมสินค้าตามใบสั่งใน POS กฎทั้งหมดที่กล่าวถึงก่อนหน้านี้ในบทความนี้จะยังคงมีผลบังคับ เฉพาะสินค้าที่มีหมายเลขลำดับที่ตั้งค่าคอนฟิกไว้เป็น **ใช้งานอยู่** เท่านั้น ที่จะผ่านการตรวจสอบความถูกต้องของสินค้าคงคลังตามหมายเลขลำดับประจำสินค้า สินค้าที่กำหนดเป็น **ใช้งานอยู่ในกระบวนการขาย** จะไม่ได้รับการตรวจสอบความถูกต้อง ถ้าสามารถใช้ **สินค้าคงคลังค่าลบทางกายภาพ** ได้กับผลิตภัณฑ์ **ที่ใช้งานอยู่** หมายเลขลำดับประจำสินค้าจะได้รับการยอมรับ ไม่ว่าสต็อกที่มีอยู่จะเป็นอย่างไรก็ตาม ทั้งสินค้า **ที่ใช้งานอยู่** และสินค้า **ที่ใช้งานอยู่ในกระบวนการขาย** หาก **การตัดสินค้าจากคลังที่ว่างเปล่าได้** สามารถตั้งค่าคอนฟิก ผู้ใช้สามารถปล่อยหมายเลขลำดับประจำสินค้าชนิดว่างไว้ได้ถ้าต้องการในระหว่างขั้นตอนการเบิกสินค้า แพ็ค และจัดส่ง

การตรวจสอบความถูกต้องหหมายเลขลำดับประจำสินค้าจะเกิดขึ้นเมื่อผู้ใช้ดําเนินงานเบิกสินค้าบนใบสั่งของลูกค้าใน POS ด้วย แอปพลิเคชัน POS ไม่อนุญาตให้เบิกสินค้าเพื่อสรุปเกี่ยวกับผลิตภัณฑ์ที่เป็นอนุกรม เว้นแต่จะผ่านการตรวจสอบความถูกต้องตามที่กล่าวไว้ก่อนหน้านี้ การตรวจสอบความถูกต้องจะเป็นไปตามมิติการติดตามและการตั้งค่าคอนฟิกคลังสินค้าขายของผลิตภัณฑ์เสมอ 

## <a name="additional-resources"></a>ทรัพยากรเพิ่มเติม

[การดำเนินงานของสินค้าคงคลังขาเข้าใน POS](./pos-inbound-inventory-operation.md)

[การดำเนินงานของสินค้าคงคลังขาออกใน POS](./pos-outbound-inventory-operation.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]