---
title: ใบรับรองและข้อมูลลับของลูกค้า
description: บทความนี้จะอธิบายวิธีการตั้งค่าใบรับรองและข้อมูลลับของลูกค้าในใบแจ้งหนี้อิเล็กทรอนิกส์
author: gionoder
ms.date: 02/07/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: gionoder
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.custom: ''
ms.assetid: ''
ms.search.form: ''
ms.openlocfilehash: 3943e7cb43cc6bf93995f0b3957766227cc3ec99
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 08/12/2022
ms.locfileid: "9279854"
---
# <a name="customer-certificates-and-secrets"></a>ใบรับรองและข้อมูลลับของลูกค้า

[!include [banner](../includes/banner.md)]

ถ้าคุณมีการอ้างอิง Microsoft Azure Key Azure ใน Regulatory Configuration Service (RCS) อยู่แล้ว คุณสามารถสร้างการอ้างอิงไปยังใบรับรองและข้อมูลลับของ Key Vault หากคุณยังไม่มีการอ้างอิง Key Vault ดูที่ [สภาพแวดล้อมการบริการ](e-invoicing-service-environments.md) เพื่อดูข้อมูลเกี่ยวกับวิธีการสร้าง

## <a name="create-certificates-and-secrets"></a>สร้างใบรับรองและข้อมูลลับ

หากต้องการสร้างและตั้งค่าใบรับรองและข้อมูลลับ ทำตามขั้นตอนเหล่านี้

1. ลงชื่อเข้าใช้บัญชี RCS ของคุณ
2. ในพื้นที่ทำงาน **คุณลักษณะมาตรฐานโลก** ในส่วน **สภาพแวดล้อม** ให้เลือกไทล์ **การออกใบแจ้งหนี้อิเล็กทรอนิกส์**
3. บนหน้า **การตั้งค่าสภาพแวดล้อม** บนบานหน้าต่างการดำเนินการ ให้เลือก **สภาพแวดล้อมการบริการ**
4. บนหน้า **สภาพแวดล้อมการบริการ** บนบานหน้าต่างการดำเนินการ ให้เลือก **พารามิเตอร์ Key Vault**
5. บนหน้า **พารามิเตอร์ Key Vault** ให้เลือก การอ้างอิง Key Vault จากนั้นในส่วน **ใบรับรอง** ให้เลือก **เพิ่ม**
6. ในฟิลด์ **ชื่อ** ป้อนชื่อสำหรับใบรับรองหรือข้อมูลลับของ Key Vault สำหรับข้อมูลเพิ่มเติม ดูที่ [สร้างบัญชีที่เก็บข้อมูล Azure ในพอร์ทัล Azure](e-invoicing-create-azure-storage-account-azure-portal.md)
7. ในฟิลด์ **คำอธิบาย** ให้ป้อนคำอธิบาย
8. ในฟิลด์ **ชนิด** ให้เลือก **ใบรับรอง** ถ้าคุณอ้างอิงถึงใบรับรองที่จัดเก็บอยู่ใน Key Vault เลือก **ข้อมูลลับ** ถ้าคุณอ้างอิงข้อมูลลับที่จัดเก็บอยู่ใน Key Vault
9. เลือก **บันทึก**

> [!NOTE]
> ในบางสถานการณ์ คุณต้องใช้ใบรับรองสาธารณะที่มีนามสกุลไฟล์ .cer อย่างไรก็ตาม Key Vault ไม่รองรับการนําเข้าและจัดเก็บใบรับรองชนิดนี้เป็นใบรับรอง Key Vault ในสถานการณ์เหล่านี้ คุณควรบันทึกไฟล์ .cer เป็นสตริง X.509 (.CER) ที่มีการเข้ารหัส Base-64 จากนั้นในข้อมูลลับของ Key Vault ให้จัดเก็บสตริงที่ปรากฏระหว่างบรรทัด **BEGIN CERTIFICATE** กับบรรทัด **END CERTIFICATE** ในไฟล์ ในสภาพแวดล้อมการบริการ คุณยังควรสร้างการอ้างอิงไปยังเรกคอร์ด Key Vault และตั้งค่าฟิลด์ **ชนิด** เป็น **ใบรับรอง**

## <a name="create-a-chain-of-certificates"></a>สร้างกลุ่มใบรับรอง

หากใบแจ้งหนี้เฉพาะประเทศ/ภูมิภาคของคุณต้องใช้กลุ่มใบรับรองเพื่อใช้ลายเซ็นดิจิทัลหรือสร้างการเชื่อมต่อที่ปลอดภัย (Secure Sockets Layer \[SSL\]) กับบริการเว็บภายนอก ให้สร้างกลุ่มใบรับรองที่มีใบรับรองอยู่ในลำดับต่อไปนี้

1. ใบรับรองหลัก
2. ใบรับรองตัวกลาง
3. ใบรับรองของผู้ใช้ปลายทาง

หน่วยงานใบรับรองหลัก (CA) เป็นแหล่งที่มาของใบรับรองที่น่าเชื่อถือ ใบรับรอง CA ตัวกลางคือตัวกลางที่เชื่อมโยงใบรับรองของผู้ใช้ปลายทางกับใบรับรอง CA หลัก

หากต้องการสร้างและตั้งค่ากลุ่มใบรับรอง ทำตามขั้นตอนเหล่านี้

1. บนหน้า **พารามิเตอร์ Key Vault** บนบานหน้าต่างการดำเนินการ ให้เลือก **กลุ่มของใบรับรอง**
2. เลือก **สร้าง** เพื่อสร้างกลุ่มของใบรับรอง
3. ในฟิลด์ **ชื่อ** ป้อนชื่อของกลุ่มของใบรับรอง
4. ในฟิลด์ **คำอธิบาย** ให้ป้อนคำอธิบาย
5. ในส่วน **ใบรับรอง** ให้เลือก **เพิ่ม** เพื่อเพิ่มใบรับรองให้กับกลุ่ม
6. ใช้ปุ่ม **ขึ้น** หรือ **ลง** เพื่อเปลี่ยนตําแหน่งของใบรับรองในกลุ่ม เก็บใบรับรองหลักของ CA ไว้ที่ด้านบนของรายการและใบรับรองของผู้ใช้ปลายทางไว้ที่ด้านล่าง
7. เลือก **บันทึก**

คุณสามารถสร้างการอ้างอิง Key Vault ใน RCS ได้มากตามต้องการ โปรดอย่าลืมว่ามีการใช้ข้อมูลลับสำหรับโทเค็นลายเซ็นการเข้าถึงที่ใช้ร่วมกัน (SAS) ของที่เก็บข้อมูลเพื่อเชื่อมโยงสภาพแวดล้อมการบริการที่กำหนดกับการอ้างอิง Key Vault คุณสามารถอ้างอิงใบรับรอง Key Vault และข้อมูลลับที่มีการจัดเก็บอยู่ใน Key Vault ซึ่งประกอบด้วยข้อมูลลับของโทเคน SAS ของที่เก็บข้อมูลที่คุณใช้เมื่อคุณตั้งค่าสภาพแวดล้อมการบริการ
