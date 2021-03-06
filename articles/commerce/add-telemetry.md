---
title: เพิ่มโค้ดสคริปต์ให้กับหน้าไซต์เพื่อสนับสนุนการตรวจวัดระยะไกล
description: หัวข้อนี้อธิบายวิธีการเพิ่มรหัสสคริปต์ฝั่งไคลเอนต์ไปยังหน้าไซต์ของคุณ เพื่อสนับสนุนการเรียกเก็บเงินของการตรวจวัดระยะไกลฝั่งไคลเอนต์
author: bicyclingfool
manager: annbe
ms.date: 09/29/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: StuHarg
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: dfebc6616186a3a8859b00e90c178129feaa324b
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 01/15/2021
ms.locfileid: "4980168"
---
# <a name="add-script-code-to-site-pages-to-support-telemetry"></a>เพิ่มโค้ดสคริปต์ให้กับหน้าไซต์เพื่อสนับสนุนการตรวจวัดระยะไกล

[!include [banner](includes/banner.md)]

หัวข้อนี้อธิบายวิธีการเพิ่มรหัสสคริปต์ฝั่งไคลเอนต์ไปยังหน้าไซต์ของคุณ เพื่อสนับสนุนการเรียกเก็บเงินของการตรวจวัดระยะไกลฝั่งไคลเอนต์

## <a name="overview"></a>ภาพรวม

Web analytics เป็นเครื่องมือที่จำเป็น เมื่อคุณต้องการทำความเข้าใจวิธีการที่ลูกค้าของคุณโต้ตอบกับไซต์ของคุณ และตัดสินใจที่จะช่วยปรับปรุงประสบการณ์สำหรับการแปลงสูงสุด แพคเกจการวิเคราะห์เว็บจำนวนมากพร้อมให้ความช่วยเหลือในการบรรลุเป้าหมายเหล่านี้ เช่น Google Analytics, Clicky, Moz Analytics และ KISSMetrics แพคเกจการวิเคราะห์เว็บส่วนใหญ่กำหนดให้คุณต้องเพิ่มรหัสสคริปต์ฝั่งไคลเอนต์ในองค์ประกอบที่เป็น **\<head\>** ของ HTML สำหรับทุกเพจของไซต์ของคุณ

> [!NOTE]
> คำแนะนำในหัวข้อนี้จะใช้กับฟังก์ชันฝั่งไคลเอนต์แบบกำหนดเองอื่นๆ ที่ Microsoft Dynamics 365 Commerce ไม่มีข้อเสนอโดยไม่ได้กล่าวถึง

## <a name="create-a-reusable-fragment-for-your-script-code"></a>สร้างส่วนที่สามารถใช้ซ้ำได้สำหรับรหัสสคริปต์ของคุณ

ส่วนย่อยจะช่วยให้คุณสามารถนำสคริปต์อินไลน์หรือภายนอกมาใช้ใหม่ผ่านหน้าทั้งหมดบนไซต์ของคุณได้ โดยไม่ต้องใช้เท็มเพลตที่มีการใช้

### <a name="create-a-reusable-fragment-for-your-inline-script-code"></a>สร้างส่วนย่อยที่สามารถใช้ซ้ำได้สำหรับรหัสสคริปต์อินไลน์ของคุณ

เมื่อต้องการสร้างส่วนย่อยที่สามารถใช้ซ้ำได้สำหรับรหัสสคริปต์แบบอินไลน์ของคุณในโปรแกรมสร้างไซต์ ให้ทำตามขั้นตอนเหล่านี้

1. ไปที่ **ส่วนย่อย** และให้เลือก **สร้าง**
1. ในกล่องโต้ตอบ **ส่วนย่อยใหม่** ให้เลือก **สคริปต์แบบอินไลน์**
1. ภายใต้ **ชื่อส่วนย่อย** ให้ป้อนชื่อสำหรับส่วน และจากนั้น เลือก **ตกลง**
1. ภายใต้ส่วนย่อยที่คุณสร้างขึ้น ให้เลือกโมดูล **สคริปต์แบบอินไลน์เริ่มต้น**
1. ในบานหน้าต่างคุณสมบัติทางด้านขวา ภายใต้ **สคริปต์แบบอินไลน์** ให้ป้อนสคริปต์ฝั่งไคลเอนต์ของคุณ จากนั้น ตั้งค่าคอนฟิกตัวเลือกอื่นๆ ตามที่คุณต้องการ
1. เลือก **บันทึก** และจากนั้น เลือก **แก้ไขให้เสร็จสิ้น**
1. เลือก **เผยแพร่**

### <a name="create-a-reusable-fragment-for-your-external-script-code"></a>สร้างส่วนย่อยที่สามารถใช้ซ้ำได้สำหรับรหัสสคริปต์ภายนอกของคุณ

เมื่อต้องการสร้างส่วนย่อยที่สามารถใช้ซ้ำได้สำหรับรหัสสคริปต์ภายนอกของคุณในโปรแกรมสร้างไซต์ ให้ทำตามขั้นตอนเหล่านี้

1. ไปที่ **ส่วนย่อย** และให้เลือก **สร้าง**
1. ในกล่องโต้ตอบ **ส่วนย่อยใหม่** ให้เลือก **สคริปต์ภายนอก**
1. ภายใต้ **ชื่อส่วนย่อย** ให้ป้อนชื่อสำหรับส่วน และจากนั้น เลือก **ตกลง**
1. ภายใต้ส่วนย่อยที่คุณสร้างขึ้น ให้เลือกโมดูล **สคริปต์ภายนอกเริ่มต้น**
1. ในบานหน้าต่างคุณสมบัติทางด้านขวา ภายใต้ **แหล่งที่มาของสคริปต์** ให้เพิ่ม URL ภายนอกหรือที่เกี่ยวข้องสำหรับแหล่งที่มาของสคริปต์ภายนอก จากนั้น ตั้งค่าคอนฟิกตัวเลือกอื่นๆ ตามที่คุณต้องการ
1. เลือก **บันทึก** และจากนั้น เลือก **แก้ไขให้เสร็จสิ้น**
1. เลือก **เผยแพร่**

> [!NOTE]
> ถ้ามีการเปิดใช้งานนโยบายความปลอดภัยของเนื้อหา (CSP) สำหรับไซต์ของคุณ ให้ตรวจสอบให้แน่ใจว่ามีการเพิ่ม Url ภายนอกทั้งหมดลงในคำสั่ง CSP **script-src** ในตัวสร้างไซต์ Commerce สำหรับข้อมูลเพิ่มเติม ให้ดู [จัดการนโยบายความปลอดภัยของเนื้อหา (CSP)](manage-csp.md)

## <a name="add-a-fragment-that-includes-script-code-to-a-template"></a>เพิ่มส่วนย่อยซึ่งรวมถึงรหัสสคริปต์ให้กับเท็มเพลต

เมื่อต้องการเพิ่มส่วนย่อยที่รวมรหัสสคริปต์ไปยังเท็มเพลตในโปรแกรมสร้างไซต์ ให้ทำตามขั้นตอนเหล่านี้

1. ไปที่ **แม่แบบ** และเปิดแม่แบบสำหรับเพจที่คุณต้องการเพิ่มรหัสสคริปต์ของคุณ
1. ในบานหน้าต่างด้านซ้าย ให้ขยายลำดับชั้นแม่แบบเพื่อแสดงช่อง **ส่วนหัวของ HTML**
1. ในช่อง **ส่วนหัวของ HTML** เลือก ปุ่มจุดไข่ปลา (**...**) แล้วจากนั้น เลือก **เพิ่มส่วนย่อย**
1. เลือกส่วนที่คุณสร้างสำหรับรหัสสคริปต์ของคุณ
1. เลือก **บันทึก** และจากนั้น เลือก **แก้ไขให้เสร็จสิ้น**
1. เลือก **เผยแพร่**

## <a name="add-an-external-script-or-inline-script-directly-to-a-template"></a>เพิ่มสคริปต์ภายนอกหรือสคริปต์อินไลน์ไปยังเท็มเพลตโดยตรง

ถ้าคุณต้องการแทรกสคริปต์แบบอินไลน์หรือภายนอกโดยตรงลงในชุดของหน้าที่ถูกควบคุมโดยเท็มเพลตเดียว คุณไม่จำเป็นต้องสร้างส่วนย่อยก่อน

### <a name="add-an-inline-script-directly-to-a-template"></a>เพิ่มสคริปต์อินไลน์ไปยังเท็มเพลตโดยตรง

เมื่อต้องการเพิ่มสคริปต์แบบอินไลน์ให้กับเท็มเพลตในโปรแกรมสร้างไซต์โดยตรง ให้ทำตามขั้นตอนเหล่านี้

1. ไปที่ **แม่แบบ** และเปิดแม่แบบสำหรับเพจที่คุณต้องการเพิ่มรหัสสคริปต์ของคุณ
1. ในบานหน้าต่างด้านซ้าย ให้ขยายลำดับชั้นแม่แบบเพื่อแสดงช่อง **ส่วนหัวของ HTML**
1. ในช่อง **ส่วนหัวของ HTML** เลือก ปุ่มจุดไข่ปลา (**...**) แล้วจากนั้น เลือก **เพิ่มโมดูล**
1. ในกล่องโต้ตอบ **เพิ่มโมดูล** ให้เลือก **สคริปต์แบบอินไลน์**
1. ในบานหน้าต่างคุณสมบัติทางด้านขวา ภายใต้ **สคริปต์แบบอินไลน์** ให้ป้อนสคริปต์ฝั่งไคลเอนต์ของคุณ จากนั้น ตั้งค่าคอนฟิกตัวเลือกอื่นๆ ตามที่คุณต้องการ
1. เลือก **บันทึก** และจากนั้น เลือก **แก้ไขให้เสร็จสิ้น**
1. เลือก **เผยแพร่**

### <a name="add-an-external-script-directly-to-a-template"></a>เพิ่มสคริปต์ภายนอกไปยังเท็มเพลตโดยตรง

เมื่อต้องการเพิ่มสคริปต์ภายนอกให้กับเท็มเพลตในโปรแกรมสร้างไซต์โดยตรง ให้ทำตามขั้นตอนเหล่านี้

1. ไปที่ **แม่แบบ** และเปิดแม่แบบสำหรับเพจที่คุณต้องการเพิ่มรหัสสคริปต์ของคุณ
1. ในบานหน้าต่างด้านซ้าย ให้ขยายลำดับชั้นแม่แบบเพื่อแสดงช่อง **ส่วนหัวของ HTML**
1. ในช่อง **ส่วนหัวของ HTML** เลือก ปุ่มจุดไข่ปลา (**...**) แล้วจากนั้น เลือก **เพิ่มโมดูล**
1. ในกล่องโต้ตอบ **เพิ่มโมดูล** ให้เลือก **สคริปต์ภายนอก**
1. ในบานหน้าต่างคุณสมบัติทางด้านขวา ภายใต้ **แหล่งที่มาของสคริปต์** ให้เพิ่ม URL ภายนอกหรือที่เกี่ยวข้องสำหรับแหล่งที่มาของสคริปต์ภายนอก จากนั้น ตั้งค่าคอนฟิกตัวเลือกอื่นๆ ตามที่คุณต้องการ
1. เลือก **บันทึก** และจากนั้น เลือก **แก้ไขให้เสร็จสิ้น**
1. เลือก **เผยแพร่**

## <a name="additional-resources"></a>ทรัพยากรเพิ่มเติม

[เพิ่มโลโก้](add-logo.md)

[เลือกชุดรูปแบบของไซต์](select-site-theme.md)

[ทำงานกับไฟล์การแก้ไข CSS](css-override-files.md)

[เพิ่มไอคอนประจำไซต์](add-favicon.md)

[เพิ่มข้อความต้อนรับ](add-welcome-message.md)

[เพิ่มข้อความสงวนลิขสิทธิ์](add-copyright-notice.md)

[เพิ่มภาษาลงในไซต์ของคุณ](add-languages-to-site.md)
