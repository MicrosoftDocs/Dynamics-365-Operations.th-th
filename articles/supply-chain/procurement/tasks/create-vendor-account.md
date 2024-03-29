---
title: การสร้างบัญชีผู้จัดจำหน่าย
description: 'ขั้นตอนนี้แสดงวิธีการสร้างบัญชีผู้จัดจำหน่าย และเพิ่มอยู่และข้อมูลผู้ติดต่อ '
author: GalynaFedorova
ms.date: 06/26/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: VendTable, LogisticsPostalAddressGrid, DirPartyLookup, LogisticsPostalAddress, SysLookupMultiSelectGrid, WHSFilterGenerallyAvail
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: gfedorova
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 34c6d14923bcfdbcbeffc44a5fd08286c60bfc13
ms.sourcegitcommit: 9166e531ae5773f5bc3bd02501b67331cf216da4
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 05/03/2022
ms.locfileid: "8673899"
---
# <a name="create-a-vendor-account"></a>การสร้างบัญชีผู้จัดจำหน่าย

[!include [banner](../../includes/banner.md)]

ขั้นตอนนี้แสดงวิธีการสร้างบัญชีผู้จัดจำหน่าย และเพิ่มอยู่และข้อมูลผู้ติดต่อ  ขั้นตอนจะไม่แสดงวิธีการเติมข้อมูลในฟิลด์ทั้งหมดสำหรับการซื้อ และวัตถุประสงค์ทางการเงิน เมื่อต้องการเรียนรู้เพิ่มเติมเกี่ยวกับฟิลด์ดังกล่าว โปรดอ่านคำอธิบายฟิลด์ คุณสามารถใช้กระบวนงานนี้ในบริษัทข้อมูลสาธิต USMF หรือข้อมูลของคุณเองได้ บัญชีผู้จัดจำหน่ายโดยทั่วไปจะสร้างขึ้นโดยผู้เชี่ยวชาญด้านการจัดซื้อจัดหาหรือบุคลากรลูกหนี้บัญชี


## <a name="create-a-vendor-account"></a>สร้างบัญชีผู้จัดจำหน่าย
1. ไปที่ **บานหน้าต่างการนำทาง > โมดูล > การจัดซื้อและการจัดหา > ผู้จัดจำหน่าย > ผู้จัดจำหน่ายทั้งหมด**
2. คลิก **สร้าง**
3. ในฟิลด์ **บัญชีผู้จัดจำหน่าย** ให้พิมพ์ค่า
    - ค่าอาจถูกเติมโดยอัตโนมัติ  ถ้าเป็นเช่นนั้นคุณสามารถข้ามขั้นตอนนี้  
    - คุณสามารถสร้างบัญชีผู้จัดจำหน่ายสำหรับบุคคลหรือองค์กร  สิ่งนี้จะกระทบฟิลด์ที่พร้อมใช้งานอยู่  ในตัวอย่างนี้ เราจะสร้างบัญชีผู้จัดจำหน่ายสำหรับองค์กร   
4. ในฟิลด์ **ชื่อ** ป้อนหรือเลือกค่า ถ้าผู้จัดจำหน่ายของคุณเป็นฝ่ายที่ลงทะเบียนไว้ในระบบของคุณอยู่แล้ว คุณสามารถใช้ดร็อปดาวน์และเลือกในฟิลด์นี้ และบัญชีผู้จัดจำหน่ายใหม่จะรับช่วงข้อมูลที่อยู่และข้อมูลผู้ติดต่อที่ลงทะเบียนไว้แล้ว
5. ในฟิลด์ **กลุ่ม** ให้ป้อนหรือเลือกค่าใดค่าหนึ่ง กลุ่มผู้จัดจำหน่ายถูกใช้เพื่อจัดกลุ่มผู้จัดจำหน่ายที่มีพารามิเตอร์ต่อไปนี้ร่วมกัน: เงื่อนไขการชำระเงิน รอบระยะเวลาชำระ บัญชีแยกประเภทของการลงรายการสินค้าคงคลัง ซึ่งรวมถึงกลุ่มภาษีขาย บัญชีแยกประเภทเริ่มต้น รหัสตัวกรองผลิตภัณฑ์ หรือการตั้งค่าคอนฟิกการคาดการณ์การจัดหาวัสดุ
6. ในฟิลด์ **จำนวนพนักงาน** ให้ป้อนหมายเลข
7. ในฟิลด์ **หมายเลของค์กร** ให้พิมพ์ค่าใดค่าหนึ่ง

## <a name="add-an-address"></a>เพิ่มที่อยู่
1. ขยายส่วน **ที่อยู่**
2. คลิก **เพิ่ม**
3. ในฟิลด์ **วัตถุประสงค์** ให้ป้อนหรือเลือกค่าใดค่าหนึ่ง คุณสามารถเลือกวัตถุประสงค์หนึ่งรายการหรือมากกว่า  ซึ่งจะถูกใช้เพื่อเลือกที่อยู่ที่ถูกต้องสำหรับวัตถุประสงค์ที่กำหนดไว้  ตัวอย่างเช่น ถ้าวัตถุประสงค์คือ "ใบแจ้งหนี้" ซึ่งที่อยู่ที่จะถูกใช้ เมื่อคุณส่งใบแจ้งหนี้
4. ในฟิลด์ **ชื่อหรือคำอธิบาย** ให้พิมพ์ค่า
5. ในฟิลด์ **ประเทศ/ภูมิภาค**  ให้ป้อนหรือเลือกค่าใดค่าหนึ่ง ป้อนรายละเอียดที่อยู่  ประเทศ/ภูมิภาคที่คุณเลือกจะกำหนดว่าฟิลด์คุณจะถูกแสดงอยู่ด้วย สอดคล้องกับรูปแบบที่อยู่สำหรับประเทศ/ภูมิภาค 
6. คลิก **ตกลง**

## <a name="add-contact-information"></a>เพิ่มข้อมูลผู้ติดต่อ
1. ขยายส่วน **ข้อมูลผู้ติดต่อ**
2. คลิก **เพิ่ม**
3. ในฟิลด์ **คำอธิบาย** ให้พิมพ์ค่าใดค่าหนึ่ง
4. ในฟิลด์ **ชนิด**  ให้เลือกหนึ่งตัวเลือก
5. ในฟิลด์ **หมายเลข/ที่อยู่ผู้ติดต่อ** ให้พิมพ์ค่าใดค่าหนึ่ง คุณสามารถเลือกกล่องกาเครื่องหมายหลักได้ ถ้านี่เป็นผู้ติดต่อหลัก  
6. คลิก **บันทึก**
7. ปิดหน้า
8. ปิดหน้า



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]