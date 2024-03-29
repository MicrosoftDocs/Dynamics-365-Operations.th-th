---
title: ส่งคืนผลิตภัณฑ์ที่ควบคุมด้วยหมายเลขลำดับประจําสินค้าใน POS
description: บทความนี้อธิบายความสามารถเกี่ยวกับการตรวจสอบความถูกต้องของสินค้าที่เป็นอนุกรม ซึ่งเป็นส่วนหนึ่งของกระบวนการส่งคืนในแอปพลิเคชันการขายหน้าร้าน Microsoft Dynamics 365 Commerce (POS)
author: hhainesms
ms.date: 06/01/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgriffin
ms.search.region: global
ms.author: hhaines
ms.search.validFrom: ''
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 9fa7e47b6d650370afe4b98d7eca01253bd1bc36
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 08/12/2022
ms.locfileid: "9268486"
---
# <a name="return-serial-numbercontrolled-products-in-pos"></a>ส่งคืนผลิตภัณฑ์ที่ควบคุมหมายเลขลำดับประจำสินค้าใน POS

[!include [banner](includes/banner.md)]

บทความนี้อธิบายความสามารถเกี่ยวกับการตรวจสอบความถูกต้องของสินค้าที่เป็นอนุกรม ซึ่งเป็นส่วนหนึ่งของกระบวนการส่งคืนในแอปพลิเคชันการขายหน้าร้าน Microsoft Dynamics 365 Commerce (POS)

> [!NOTE]
> ใน Commerce รุ่น 10.0.20 และใหม่กว่า จะมีคุณลักษณะใหม่ที่ชื่อ **ประสบการณ์การประมวลผลการส่งคืนแบบรวมใน POS** พร้อมใช้งาน เมื่อต้องการใช้การตรวจสอบความถูกต้องของหมายเลขลำดับประจำสินค้าระหว่างการประมวลผลใบสั่งส่งคืนสินค้าใน POS คุณต้องเปิดคุณลักษณะนี้ หากต้องการข้อมูลเกี่ยวกับความสามารถอื่นๆ ที่มีคุณลักษณะนี้เมื่อเปิดคุณสมบัตินี้ โปรดดูที่ [สร้างการส่งคืนใน POS)](POS-returns.md)
>
> หลังจากเปิดคุณลักษณะแล้ว ไม่สามารถปิดได้

## <a name="options-for-validating-serialized-returns"></a>ตัวเลือกการตรวจสอบความถูกต้องของการส่งคืนฑ์ที่กำหนดหมายเลขลำดับประจำสินค้าแล้ว

เมื่อเปิดคุณลักษณะ **ประสบการณ์การประมวลผลการส่งคืนแบบรวมใน POS** องค์กรสามารถตรวจสอบความถูกต้องของการส่งคืนสินค้าที่มีการควบคุมหมายเลขลำดับประจำสินค้าโดยผ่าน POS ได้ ความสามารถนี้สามารถแจ้งเตือนผู้ใช้ได้ ถ้าหมายเลขหมายเลขลำดับประจำสินค้าที่ส่งคืนแตกต่างจากหมายเลขหมายเลขลำดับประจำสินค้าที่ขาย ใน Commerce รุ่น 10.0.20 และใหม่กว่า ข้อความที่ผู้ใช้ได้รับคือข้อความเตือนเท่านั้น ผู้ใช้สามารถประมวลผลการส่งคืนกับหมายเลขหมายเลขลำดับประจำสินค้าที่แตกต่างจากหมายเลขหมายเลขลำดับประจำสินค้าที่ขายครั้งแรกได้

เมื่อต้องการตั้งค่าคอนฟิกการตรวจสอบความถูกต้องของหมายเลขหมายเลขลำดับประจำสินค้าขององค์กรหลังจากคุณลักษณะ **ประสบการณ์การประมวลผลการส่งคืนแบบรวมใน POS** เปิดอยู่ ไปที่ **Retail และ Commerce \> การตั้งค่าศูนย์ควบคุม \> พารามิเตอร์ \> พารามิเตอร์ Commerce** ใน Commerce headquarters บนแท็บ **สินค้าคงคลัง** บนแท็บด่วน **การดําเนินงานสินค้าคงคลังของร้านค้า** ให้ตั้งค่าตัวเลือก **เปิดใช้งาน การตรวจสอบความถูกต้องของหมายเลขลำดับประจำสินค้าบนการส่งคืน POS** เป็น **ใช่**

## <a name="process-returns-for-serialized-items-in-pos"></a>ประมวลผลการส่งคืนสินค้าที่กำหนดหมายเลขลำดับประจำสินค้าแล้วใน POS

หากตัวเลือก **เปิดใช้การตรวจสอบความถูกต้องของหมายเลขลำดับประจำสินค้าบนการส่งคืน POS** ได้รับการตั้งค่าเป็น **ใช่** เมื่อมีการส่งคืนสินค้าที่ควบคุมหมายเลขลำดับประจำสินค้าผ่านทาง POS ผู้ใช้สามารถป้อนหมายเลขลำดับประจำสินค้า ให้กับรายการส่งคืนในบานหน้าต่างรายละเอียดในหน้า **ผลิตภัณฑ์ที่สามารถส่งคืนได้** ถ้าหมายเลขลำดับประจำสินค้าที่ป้อนไม่ตรงกับหมายเลขลำดับประจำสินค้าเดิมที่ขายให้กับธุรกรรมการขาย ผู้ใช้จะได้รับข้อความเตือน อย่างไรก็ตาม แอปพลิเคชันไม่ได้ป้องกันไม่ให้ผู้ใช้ลงรายการบัญชีการส่งคืนต่อไป

> [!NOTE]
> ปัจจุบัน POS สนับสนุนการตรวจสอบความถูกต้องของหมายเลขลำดับประจำสินค้ารายการส่งคืนที่มีปริมาณที่สั่งไม่เกินหนึ่งรายการ ถ้ารายการใบสั่งขายดั้งเดิมถูกสร้างขึ้นในช่องทางที่ไม่ใช่ POS และหากปริมาณที่สั่งไว้ของสินค้าที่กำหนดหมายเลขลำดับประจำสินค้าแล้วในรายการขายที่ระบุว่ามีมากกว่าหนึ่งรายการ สินค้านั้นจะสามารถส่งคืนโดยผ่าน POS ได้อย่างถูกต้อง

## <a name="additional-resources"></a>ทรัพยากรเพิ่มเติม

[สร้างการส่งคืนใน POS](POS-returns.md)
