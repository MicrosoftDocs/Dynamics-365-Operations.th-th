---
title: โมดูลแท็บ
description: หัวข้อนี้ครอบคลุมถึงโมดูลแท็บ และอธิบายวิธีการเพิ่มลงในหน้าของไซต์ใน Microsoft Dynamics 365 Commerce
author: anupamar-ms
manager: annbe
ms.date: 09/15/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: ''
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: ''
ms.openlocfilehash: 42c3cd99897627dbcdbdec91cfdb03d5743f7388
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 01/15/2021
ms.locfileid: "4980193"
---
# <a name="tab-module"></a>โมดูลแท็บ

[!include [banner](includes/banner.md)]

หัวข้อนี้ครอบคลุมถึงโมดูลแท็บ และอธิบายวิธีการเพิ่มลงในหน้าของไซต์ใน Microsoft Dynamics 365 Commerce

## <a name="overview"></a>ภาพรวม

โมดูลแท็บเป็นโมดูลที่เหมือนกับคอนเทนเนอร์ที่ใช้ในการจัดระเบียบข้อมูลบนหน้าไซต์บนแท็บ ผู้ใช้สามารถใช้ในหน้าใดก็ได้ที่ต้องแสดงข้อมูลบนแท็บ

ภายในโมดูลแท็บทั้งหมด สามารถเพิ่มโมดูลรายการแท็บได้ตั้งแต่หนึ่งรายการขึ้นไป แต่ละโมดูลของรายการแท็บจะแสดงถึงแท็บเดียว ในแต่ละโมดูลแท็บจะสามารถเพิ่มโมดูลอย่างน้อยหนึ่งรายการ ไม่มีข้อจำกัดสำหรับชนิดของโมดูลที่สามารถเพิ่มเข้าในโมดูลแท็บได้

รูปภาพต่อไปนี้แสดงตัวอย่างของโมดูลแท็บบนหน้าไซต์ ในตัวอย่างนี้ แท็บ **การจัดส่ง** ถูกเลือก

![ตัวอย่างของโมดูลแท็บ](./media/ecommerce-tab.PNG)

## <a name="tab-module-properties"></a>คุณสมบัติของโมดูลแท็บ

| ชื่อคุณสมบัติ | มูลค่า | คำอธิบาย |
|---------------|--------|-------------|
| หัวข้อ | ข้อความ | คุณสมบัตินี้จะระบุส่วนหัวของข้อความที่ไม่บังคับสำหรับโมดูลแท็บ |
| ดัชนีแท็บที่ใช้งานอยู่ | ลำดับ | คุณสมบัตินี้ระบุแท็บที่ควรเปิดใช้งานโดยค่าเริ่มต้นเมื่อมีการโหลดหน้า ถ้าไม่มีการระบุค่า รายการแท็บแรกจะใช้งานโดยค่าเริ่มต้น |

## <a name="tab-item-module-properties"></a>คุณสมบัติของโมดูลรายการแท็บ

| ชื่อคุณสมบัติ | มูลค่า | คำอธิบาย |
|---------------|--------|-------------|
| ชื่อตำแหน่ง | ข้อความ | คุณสมบัตินี้จะระบุชื่อเรื่องของข้อความสำหรับโมดูลรายการแท็บ |

## <a name="add-a-tab-module-to-a-page"></a>เพิ่มโมดูลแท็บไปยังหน้า

การเพิ่มโมดูลแท็บไปยังหน้า และตั้งค่าคุณสมบัติ ให้ทำตามขั้นตอนต่อไปนี้

1. ใช้เท็มเพลตการตลาด Fabrikam (หรือเท็มเพลตที่ไม่มีข้อจำกัด) เพื่อสร้างหน้าใหม่ที่ชื่อ **หน้านโยบายร้านค้า**
1. ในช่อง **หลัก** ของ **หน้าเริ่มต้น** เลือกปุ่มจุดไข่ปลา (**...**) แล้วเลือก **เพิ่มโมดูล**
1. ในกล่องโต้ตอบ **เพิ่มโมดูล** ให้เลือกโมดูล **คอนเทนเนอร์** แล้วเลือก **ตกลง**
1. ในช่อง **คอนเทนเนอร์** เลือกจุดไข่ปลา (**...**) แล้วจากนั้นเลือก **เพิ่มโมดูล**
1. ในกล่องโต้ตอบ **เพิ่มโมดูล** ให้เลือกโมดูล **แท็บ** แล้วเลือก **ตกลง**
1. ในบานหน้าต่างคุณสมบัติของโมดูลแท็บ ให้เลือก **ส่วนหัว** ถัดจากสัญลักษณ์ดินสอ
1. ในกล่องโต้ตอบ **หัวเรื่อง** ภายใต้ **ข้อความส่วนหัว** ให้ป้อนข้อความส่วนหัว (ตัวอย่างเช่น **นโยบาย**) จากนั้น เลือก **ตกลง**
1. ในช่อง **แท็บ** เลือกจุดไข่ปลา (**...**) แล้วจากนั้น เลือก **เพิ่มโมดูล**
1. ในกล่องโต้ตอบ **เพิ่มโมดูล** ให้เลือกโมดูล **รายการแท็บ** แล้วเลือก **ตกลง**
1. ในบานหน้าต่างคุณสมบัติของโมดูลรายการแท็บที่อยู่ภายใต้ **ชื่อเรื่อง** ให้ป้อนข้อความชื่อเรื่อง (ตัวอย่างเช่น **การส่งคืน**)
1. ในช่อง **รายการแท็บ** เลือกจุดไข่ปลา (**...**) แล้วจากนั้น เลือก **เพิ่มโมดูล**
1. ในกล่องโต้ตอบ **เพิ่มโมดูล** ให้เลือกโมดูล **บล็อกข้อความ** แล้วเลือก **ตกลง**
1. ในบานหน้าต่างคุณสมบัติของโมดูลบล็อกข้อความ ภายใต้ **ข้อความตกแต่ง** ให้ป้อนย่อหน้าของข้อความ
1. ในช่อง **แท็บ** ให้เพิ่มโมดูลของรายการแท็บเพิ่มเติมที่มีชื่อเรื่อง ในแต่ละโมดูลรายการแท็บ ให้เพิ่มโมดูลบล็อกข้อความที่มีเนื้อหา
1. เลือก **บันทึก** และจากนั้น เลือก **แสดงตัวอย่าง** เพื่อแสดงตัวอย่างหน้า หน้าจะแสดงโมดูลแท็บที่มีโมดูลแท็บรายการแท็บที่มีเนื้อหาที่คุณเพิ่ม
1. เลือก **แก้ไขให้เสร็จสิ้น** เพื่อตรวจสอบในหน้า และจากนั้น เลือก **เผยแพร่** เพื่อเผยแพร่

## <a name="additional-resources"></a>ทรัพยากรเพิ่มเติม

[ภาพรวมของไลบรารีโมดูล](starter-kit-overview.md)

[โมดูลคอนเทนเนอร์](add-container-module.md)

[โมดูล Accordion](add-accordion.md)

[โมดูลบล็อกข้อความ](add-content-rich-block.md)
