---
title: รายการคุณลักษณะภาษีว่างเปล่าในพารามิเตอร์การคำนวณภาษี
description: หัวข้อนี้อธิบายวิธีการแก้ไขปัญหาที่รายการของคุณลักษณะภาษีของหน้าพารามิเตอร์การคํานวณภาษีว่างเปล่า
author: wangchen
ms.date: 03/04/2022
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: TaxIntegrationTaxServiceParameters
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: wangchen
ms.search.validFrom: 2021-10-26
ms.dyn365.ops.version: Version 10.0.21
ms.openlocfilehash: ef8158c2ada18e7d132eebbedef559b3f80ab19f
ms.sourcegitcommit: 2977e92a76211875421e608555311c363cfbdc25
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 04/16/2022
ms.locfileid: "8612302"
---
# <a name="empty-tax-feature-list-in-tax-calculation-parameters"></a>รายการคุณลักษณะภาษีว่างเปล่าในพารามิเตอร์การคำนวณภาษี

[!include [banner](../includes/banner.md)]


## <a name="symptom"></a>อาการ

คุณได้เผยแพร่คุณลักษณะใน Regulatory Configuration Service (RCS) เพื่อให้คุณสามารถใช้คุณลักษณะใน Microsoft Dynamics 365 Finance อย่างไรก็ตาม เมื่อคุณเปิด Finance ให้ไปที่ **ภาษี** \> **การตั้งค่า** \> **การตั้งค่าคอนฟิกภาษี** \> **พารามิเตอร์การคำนวณภาษี** และลองเลือกค่าในฟิลด์ **ชื่อการตั้งค่าคุณลักษณะ** รายการของค่าจะว่างเปล่า

## <a name="reason"></a>เหตุผล

โดยปกติแล้ว ปัญหานี้จะเกิดขึ้นเนื่องจากสภาพแวดล้อม Finance และสภาพแวดล้อม RCS ของคุณไม่อยู่ภายใต้ผู้เช่าเดียวกัน

### <a name="rcs-tenant"></a>ผู้เช่า RCS

ปฏิบัติตามขั้นตอนต่อไปนี้เพื่อค้นหารหัสของผู้เช่าใน RCS ของคุณ

1. คัดลอก URL แบบเต็มของ RCS ตัวอย่างเช่น URL อาจเป็น `https://rcs-rts-sf-ed22b5aeea8-int-westus2.configure.global.int.dynamics.com/namespaces/817ff7a0-0d77-4aba-9360-3c9749e2c5de/?cmp=dat&mi=RCSFeatureDomainsWorkspace`
2. เปิดหน้าต่างเบราว์เซอร์ InPrivate วาง URL ของ RCS ลงในแถบที่อยู่ แล้วเลือก **Enter** ระบบจะนำคุณไปยังหน้าลงชื่อเข้าใช้ซึ่งคุณสามารถค้นหารหัสผู้เช่า RCS ได้ ตัวอย่างเช่น ถ้า URL ของหน้าลงชื่อเข้าใช้คือ `https://login.microsoftonline.com/d335a570-a05b-4bc5-8eb3-c42c65f9560d` รหัสผู้เช่าคือข้อมูลที่ปรากฏหลัง `https://login.microsoftonline.com/` หรือ **d335a570-a05b-4bc5-8eb3-c42c65f9560d**

### <a name="finance-environment-tenant-id"></a>รหัสผู้เช่าสภาพแวดล้อม Finance

เมื่อต้องการค้นหารหัสผู้เช่าให้กับสภาพแวดล้อม Finance ของคุณ ให้ปฏิบัติตามขั้นตอนเดียวกันกับที่คุณปฏิบัติตามเพื่อค้นหาผู้เช่า RCS อย่างไรก็ตาม ให้คัดลอกและวาง URL แบบเต็มของสภาพแวดล้อม Finance ของคุณ แทน URL แบบเต็มของ RCS

## <a name="resolution"></a>การแก้ปัญหา

ถ้ารหัสผู้เช่าสองรหัสแตกต่างกัน แสดงว่าคุณพบปัญหาที่อธิบายไว้ในหัวข้อนี้ ถ้ารหัสเหล่านั้นเหมือนกัน แสดงว่าคุณพบปัญหาที่ไม่เกี่ยวข้อง ในกรณีนี้ เราขอแนะนำให้คุณติดต่อฝ่ายสนับสนุนของ Microsoft

### <a name="solution-1"></a>วิธีการแก้ไข 1

ลงชื่อเข้าใช้สภาพแวดล้อม RCS ของคุณในผู้เช่าเดียวกันกับสภาพแวดล้อม Finance ที่ลงชื่อเข้าใช้ จากนั้นสร้างและเผยแพร่คุณลักษณะภาษี

### <a name="solution-2"></a>วิธีการแก้ไข 2

ใช้คุณลักษณะภาษีกับผู้เช่า Finance ใน RCS ร่วมกัน

1. ใน RCS ให้ไปที่ **คุณลักษณะมาตรฐานโลก** \> **การคํานวณภาษี**
2. เลือกคุณลักษณะที่จะใช้ร่วมกัน จากนั้นบนแท็บ **องค์กร** ให้เลือก **แชร์กับ**
3. ในฟิลด์ **ชื่อโดเมนองค์กร** ให้ป้อนชื่อ ตัวอย่างเช่น ป้อน **contoso.onmicrosoft.com**
4. เลือก **ใช้ร่วมกัน**

![กล่องโต้ตอบดรอปดาวน์ใช้ร่วมกับองค์กรภายนอก](media/ShareTaxFeature.png)
