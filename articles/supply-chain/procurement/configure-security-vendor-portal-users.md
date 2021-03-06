---
title: ความปลอดภัยของผู้ใช้พอร์ทัลของผู้จัดจำหน่าย
description: บทความนี้อธิบายวิธีการตั้งค่าความปลอดภัยสำหรับผู้จัดจำหน่ายภายนอกที่ใช้เว็บไซต์ของผู้จัดจำหน่าย ข้อมูลนี้ใช้กับเฉพาะรุ่นกุมภาพันธ์ 2016 &amp; พฤษภาคม 2016 ของ Dynamics AX
author: RichardLuan
manager: tfehr
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SysUserManagement
audience: Application User
ms.reviewer: kamaybac
ms.custom: 30231
ms.assetid: 3574db17-81c7-4c5a-999b-0098aa0b9cda
ms.search.region: Global
ms.author: riluan
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 1be210728a6d5fa9a26daf9f13865ff08de03d2d
ms.sourcegitcommit: deac22ba5377a912d93fe408c5ae875706378c2d
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 01/16/2021
ms.locfileid: "5018204"
---
# <a name="vendor-portal-user-security"></a>ความปลอดภัยของผู้ใช้พอร์ทัลของผู้จัดจำหน่าย

[!include [banner](../includes/banner.md)]

บทความนี้อธิบายวิธีการตั้งค่าความปลอดภัยสำหรับผู้จัดจำหน่ายภายนอกที่ใช้เว็บไซต์ของผู้จัดจำหน่าย ข้อมูลนี้ใช้กับเฉพาะรุ่นกุมภาพันธ์ 2016 &amp; พฤษภาคม 2016 ของ Dynamics AX

ฟังก์ชันพอร์ทัลผู้จัดจำหน่ายได้ถูกแทนที่โดยฟังก์ชันความร่วมมือของผู้จัดจำหน่ายที่ขยายใน Dynamics 365 for Operations รุ่น 1611 ดูข้อมูลเพิ่มเติมเกี่ยวกับการตั้งค่าการรักษาความปลอดภัยสำหรับการทำงานร่วมกันกับผู้จัดจำหน่าย ดู [ตั้งค่าและรักษาการทำงานร่วมกันกับผู้จัดจำหน่าย](set-up-maintain-vendor-collaboration.md) พอร์ทัลผู้จัดจำหน่ายแสดงถึงชุดที่จำกัดของข้อมูลเกี่ยวกับใบสั่งซื้อ (POs) กับผู้จัดจำหน่ายภายนอก เป็นสิ่งสำคัญที่คุณต้องตั้งค่าสิทธิ์ผู้ใช้อย่างถูกต้องสำหรับพอร์ทัลผู้จัดจำหน่ายใน Microsoft Dynamics AX เพื่อให้ผู้จัดจำหน่ายไม่มีการเข้าถึงที่ไม่ได้ตั้งใจไปยังข้อมูลเพิ่มเติมในการติดตั้ง Dynamics AX ของคุณ **สิ่งสำคัญ:** ไม่เหมือนกับผู้ใช้รายอื่น ผู้จัดจำหน่ายภายนอกไม่ควรมีบทบาท **SystemUser** บทบาท **SystemUser** ช่วยให้มีการเข้าถึงชุดของสิทธิ์ที่ไม่เหมาะสมสำหรับผู้ใช้ภายนอก

## <a name="setting-up-a-vendor-portal-user"></a>การตั้งค่าผู้ใช้พอร์ทัลผู้จัดจำหน่าย
ก่อนที่คุณจะสร้างบัญชีผู้ใช้สำหรับบุคคลที่จะใช้พอร์ทัลผู้จัดจำหน่าย คุณต้องตั้งค่าผู้จัดจำหน่ายเพื่ออนุญาตให้มีการทำงานร่วมกันของพอร์ทัลของผู้จัดจำหน่าย ใช้ฟิลด์ **การทำงานร่วมกันกับใบสั่งซื้อ** บนแท็บ **ทั่วไป** ในหน้า **ผู้จัดจำหน่าย** ผู้จัดจำหน่ายภายนอกที่ใช้พอร์ทัลผู้จัดจำหน่าย ต้องมีการตั้งค่าต่อไปนี้:

-   บัญชีผู้ใช้ Microsoft Azure Active Directory (AAD) ต้องถูกลงทะเบียนสำหรับผู้จัดจำหน่ายในหน้า **ผู้ใช้** ใน Dynamics AX
-   ผู้จัดจำหน่ายต้องมีบทบาทความปลอดภัย **ผู้จัดจำหน่าย (ภายนอก)** ไม่ใช่บทบาท **SystemUser** **หมายเหตุ:** มีการมอบบทบาท **SystemUser** ให้โดยอัตโนมัติ เมื่อคุณสร้างบัญชีผู้ใช้ใหม่ใน Dynamics AX ดังนั้น คุณต้องลบบทบาทนั้นและรับทราบข้อความเตือนที่คุณได้รับ
-   ผู้ใช้ผู้จัดจำหน่ายไม่ควรได้รับสิทธิ์ในการเพิ่มฟิลด์เพิ่มเติมจากตารางใบสั่งซื้อไปยังมุมมองของใบสั่งซื้อ บนแท็บ **การตั้งค่าส่วนบุคคล** บนแท็บ **ผู้ใช้** ให้ตั้งค่าตัวเลือก **อนุญาตการกำหนดเป็นแบบส่วนบุคคลแบบชัดแจ้ง** สำหรับผู้ใช้เป็น **ไม่ใช่**
-   บัญชีผู้ใช้ต้องเชื่อมโยงกับผู้ติดต่อที่ลงทะเบียนแล้ว ในหน้า **ผู้ใช้** ให้เลือกผู้ติดต่อในฟิลด์ **ชื่อ** บุคคลที่คุณเลือกควรมีบทบาท **ผู้ติดต่อ** สำหรับผู้จัดจำหน่ายที่เกี่ยวข้อง

ถ้าบุคคลเดียวกันต้องการเข้าถึงพอร์ทัลผู้จัดจำหน่ายสำหรับบัญชีผู้จัดจำหน่ายหลายบัญชี (อาจจะสำหรับนิติบุคคลอื่น) บัญชีผู้ใช้ของบุคคลนั้นแต่ละบัญชีต้องเชื่อมโยงกับผู้ติดต่อจดทะเบียนเดียวกัน บทบาท **ผู้จัดจำหน่าย (ภายนอก)** รวมความสามารถพื้นฐานทั้งหมดที่จำเป็นเพื่อให้สามารถใช้ฟังก์ชันที่พร้อมใช้งานในพอร์ทัลของผู้จัดจำหน่าย การตั้งค่านี้ช่วยรับประกันว่า อินเทอร์เฟสผู้ใช้ที่ผู้ใช้ภายนอกมองเห็นจะถูกโฟกัสไปที่สถานการณ์จำลองที่กำหนดไว้เท่านั้น

<a name="additional-resources"></a>แหล่งข้อมูลเพิ่มเติม
--------

[ทำงานร่วมกับผู้จัดจำหน่ายที่ใช้พอร์ทัลผู้จัดจำหน่าย](collaborate-vendors-vendor-portal.md)



