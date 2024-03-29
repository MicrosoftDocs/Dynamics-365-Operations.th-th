---
title: สินทรัพย์หลายระดับ
description: บทความนี้อธิบายวิธีการสร้างและลบสินทรัพย์หลายระดับ
author: johanhoffmann
ms.date: 06/26/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: CatProcureCatalogEdit, CatProcureCatalogListPage
audience: Application User
ms.reviewer: kamaybac
ms.custom: 2214
ms.assetid: 2f3e0441-414d-402b-b28b-7ab0d650d658
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 5b13db8b8b12aaef2e067f9a55eb8754333eb16b
ms.sourcegitcommit: cfe8fbc202c3eb05d894076fdf99e46704f17365
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 06/15/2022
ms.locfileid: "9017158"
---
# <a name="multi-level-assets"></a>สินทรัพย์หลายระดับ

[!include [banner](../../includes/banner.md)]

 

บทความนี้อธิบายวิธีการสร้างและลบสินทรัพย์หลายระดับ คุณสามารถสร้างสินทรัพย์และสินทรัพย์ย่อยที่เกี่ยวข้องในโครงสร้างแผนภูมิตามลำดับชั้น ด้วยวิธีนี้ คุณสามารถแสดงความสัมพันธ์และการอ้างอิงระหว่างสินทรัพย์ สามารถเชื่อมโยงงานบำรุงรักษากับทุกระดับของโครงสร้างแผนภูมิ นอกจากนี้ ยังสามารถสร้างสถิติสำหรับแต่ละระดับ หรือเป็นผลรวมของระดับสินทรัพย์ย่อยทั้งหมด

ในหน้ารายการ **สินทรัพย์ทั้งหมด** (**การจัดการสินทรัพย์** \> **สินทรัพย์** \> **สินทรัพย์ทั้งหมด**) คอลัมน์ **สินทรัพย์** แสดงรายการสินทรัพย์ตามลำดับชั้น คอลัมน์ **รายการหลัก** แสดงรายการหลักที่เกี่ยวข้อง นอกจากนี้ ถ้ามีการสร้างสินทรัพย์และสินทรัพย์ย่อยแล้ว ส่วน **แผนภูมิสินทรัพย์** ในบานหน้าต่าง **ข้อมูลที่เกี่ยวข้อง** จะแสดงสินทรัพย์ในโครงสร้างแผนภูมิ

สำหรับข้อมูลเกี่ยวกับวิธีการสร้างสินทรัพย์ ให้ดูที่ [สร้างสินทรัพย์](../objects/create-an-object.md) เมื่อต้องการสร้างสินทรัพย์ย่อย ให้เลือกสินทรัพย์หลักในฟิลด์ **หลัก** บนแท็บด่วน **ทั่วไป**

## <a name="copy-an-asset-or-asset-structure"></a>คัดลอกโครงสร้างสินทรัพย์หรือสินทรัพย์

ถ้าบริษัทของคุณมีโครงสร้างสินทรัพย์ที่คล้ายกันหลายรายการ คุณสามารถใช้ฟังก์ชันคัดลอกในการจัดการสินทรัพย์เพื่อสร้างอย่างรวดเร็ว

1. เลือก **การจัดการสินทรัพย์** \> **สินทรัพย์** \> **สินทรัพย์ทั้งหมด**
2. บนหน้ารายการ **สินทรัพย์ทั้งหมด** ให้เลือกสินทรัพย์ที่จะคัดลอก ตัวอย่างเช่น ถ้าคุณต้องการคัดลอกโครงสร้างสินทรัพย์ทั้งหมด ซึ่งรวมถึงสินทรัพย์ย่อย ให้เลือกสินทรัพย์หลัก
3. เลือก **คัดลอกสินทรัพย์** ในส่วน **คัดลอกจาก** ฟิลด์ **สินทรัพย์** จะถูกตั้งค่าเป็นสินทรัพย์ที่คุณเลือกบนหน้ารายการ
4. ในส่วน **คัดลอกไปยัง** ในฟิลด์ **สินทรัพย์** ให้ป้อนชื่อของสินทรัพย์ใหม่
5. ถ้าสินทรัพย์ที่คุณกำลังสร้างควรเป็นส่วนหนึ่งของโครงสร้างสินทรัพย์ที่มีอยู่ ในส่วน **สินทรัพย์หลัก** ในฟิลด์ **สินทรัพย์** ให้เลือกรหัสหลัก
6. เลือก **ตกลง** โครงสร้างสินทรัพย์ใหม่จะแสดงอยู่ในหน้ารายการ **สินทรัพย์ทั้งหมด** แอททริบิวต์สินทรัพย์ แผนการบำรุงรักษา และรอบการบำรุงรักษาทั้งหมดที่เกี่ยวข้องกับสินทรัพย์ที่คุณคัดลอก จะถูกโอนย้ายไปยังสินทรัพย์หรือโครงสร้างสินทรัพย์ใหม่

เมื่อคุณคัดลอกโครงสร้างสินทรัพย์ สินทรัพย์ย่อยในโครงสร้างใหม่จะมีชื่อเดียวกับสินทรัพย์ย่อยที่คุณคัดลอก หลังจากกระบวนงานคัดลอกเสร็จสมบูรณ์แล้ว คุณสามารถเปลี่ยนชื่อและการตั้งค่าอื่นๆ สำหรับสินทรัพย์ได้อย่างง่ายดาย เลือกสินทรัพย์ในหน้ารายการ **สินทรัพย์ทั้งหมด** แล้วจากนั้น เลือกปุ่ม **แก้ไข**

> [!NOTE]
> เมื่อคุณคัดลอกสินทรัพย์หรือโครงสร้างสินทรัพย์ สถานะของวงจรการใช้ของสินทรัพย์ใหม่จะถูกรีเซ็ตเป็นสถานะใดก็ตามที่คุณได้กำหนดเป็นสถานะของวงจรการใช้เริ่มต้นสำหรับสินทรัพย์ ตำแหน่งที่ทำงานถูกรีเซ็ตเป็นตำแหน่งที่ทำงานเริ่มต้น

## <a name="delete-an-asset-or-asset-structure"></a>ลบโครงสร้างสินทรัพย์หรือสินทรัพย์

ถ้าสินทรัพย์มีสินทรัพย์ย่อยที่เกี่ยวข้อง คุณสามารถลบได้เฉพาะเมื่อไม่มีคำขอการบำรุงรักษา งานในใบสั่งงาน การลงทะเบียนข้อบกพร่อง หรือการประเมินเงื่อนไข จะถูกลงทะเบียนไว้ในสินทรัพย์ใดๆ

1. บนหน้ารายการ **สินทรัพย์ทั้งหมด** ให้เลือกสินทรัพย์ที่จะลบ
2. เลือก **ลบ**

> [!NOTE]
> ถ้าคุณไม่สามารถลบสินทรัพย์โดยใช้กระบวนงานนี้ อีกวิธีหนึ่งในการจัดการการลบคือ การตั้งค่าสถานะของวงจรการใช้ของสินทรัพย์สำหรับวัตถุประสงค์นี้ ตัวอย่างเช่น คุณสามารถตั้งค่าสถานะของวงจรการใช้ **ตัดจำหน่ายเป็นเศษซาก** หรือ **ลบ** ในหน้า **สถานะของวงจรการใช้ของสินทรัพย์**


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]