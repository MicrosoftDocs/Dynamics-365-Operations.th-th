---
title: ย้ายไฟล์ XML ของ NF-e เป็นสิ่งที่แนบ
description: บทความนี้อธิบายวิธีการย้ายไฟล์ XML ของ NF-e ออกจาก Microsoft Dynamics 365 Finance หรือฐานข้อมูล Dynamics 365 Supply Chain Management ของคุณ และช่วยให้ไฟล์นั้นพร้อมใช้งานในฐานะสิ่งที่แนบแทน
author: gionoder
ms.date: 11/11/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.custom: 97423
ms.assetid: ''
ms.search.region: Global
ms.author: janeaug
ms.search.validFrom: 2022-01-27
ms.dyn365.ops.version: 10.0.25
ms.openlocfilehash: ce9061896759efeb8e8960e84656d5fc1f0616ae
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 06/03/2022
ms.locfileid: "8877910"
---
# <a name="move-nf-e-xml-files-as-attachments"></a>ย้ายไฟล์ XML ของ NF-e เป็นสิ่งที่แนบ

[!include [banner](../includes/banner.md)] 


เมื่อมีการออกเอกสารทางการเงินอิเล็กทรอนิกส์ (NF-e) ไฟล์ XML จะถูกสร้างขึ้น และจัดเก็บไว้ใน Microsoft Dynamics 365 Finance และฐานข้อมูล Dynamics 365 Supply Chain Management ในการแปลเป็นภาษาบราซิล คุณสามารถใช้คุณลักษณะ **XML ของ NF-e ย้ายเป็นสิ่งที่แนบ** เพื่อให้มีพื้นที่ว่างในฐานข้อมูลที่ไฟล์ XML เหล่านั้นใช้

ในช่วงวันที่และที่ตั้งทางการเงินหนึ่งๆ คุณลักษณะจะย้ายไฟล์ XML ของ NF-e จากฐานข้อมูล Finance หรือฐานข้อมูล Supply Chain Management ไปยังการจัดเก็บ Blob จากการบอกรับเป็นสมาชิก Azure ของคุณ การเคลื่อนย้ายนี้ช่วยให้ไฟล์พร้อมใช้งานเฉพาะเป็นสิ่งที่แนบเท่านั้น หลังจากที่ย้ายไฟล์ XML ไปยังที่จัดเก็บ Blob เสร็จเรียบร้อยแล้ว ไฟล์เดิมจะถูกลบออกจากฐานข้อมูล Finance หรือฐานข้อมูล Supply Chain Management ดังนั้น พื้นที่ในฐานข้อมูลที่ไฟล์เหล่านั้นใช้จะถูกปล่อย

ทำตามขั้นตอนเหล่านี้เพื่อเปิดใช้งานคุณลักษณะ **NF-e XML move as attachment**

1. ใน Finance หรือ Supply Chain Management ให้เปิดพื้นที่ทำงาน **การจัดการคุณลักษณะ**
2. บนแท็บ **ทั้งหมด** ให้ค้นหา และเลือกคุณลักษณะ **NF-e XML เป็นสิ่งที่แนบ**
3. เลือก **เปิดใช้งาน**

ปฏิบัติตามขั้นตอนต่อไปนี้ เพื่อย้ายไฟล์ XML ของ NF-e เป็นสิ่งที่แนบ

1. ไปที่ **บัญชีลูกหนี้** \> **เอกสารทางการเงิน** \> **เอกสารทางการเงินอิเล็กทรอนิกส์** \> **ให้ย้าย NF-e XML เป็นสิ่งที่แนบ**
2. ในฟิลด์ **วันที่เริ่มต้น** และ **วันที่สิ้นสุด** ให้เลือกวันที่เริ่มต้นและวันที่สิ้นสุด
3. ในฟิลด์ **รหัสที่ตั้งทางการเงิน** ให้เลือกค่า
4. เลือก **ตกลง**

> [!IMPORTANT]
> กระบวนการนี้ไม่สามารถย้อนกลับได้ หลังจากที่คุณย้ายไฟล์ XML ของ NF-e แล้ว ผู้ใช้สามารถดูไฟล์ได้โดยการเลือก **สิ่งที่แนบ** ที่ด้านบนของหน้า **เอกสารทางการเงิน** เท่านั้น

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
