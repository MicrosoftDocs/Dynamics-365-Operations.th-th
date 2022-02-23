---
title: มีอะไรใหม่หรือเปลี่ยนแปลงใน Dynamics 365 Talent - Core HR (กรกฎาคม 2018)
description: หัวข้อนี้อธิบายคุณลักษณะใหม่หรือถูกเปลี่ยนแปลงใน Microsoft Dynamics 365 Talent - Core HR
author: andreabichsel
manager: AnnBe
ms.date: 07/31/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: kherr
ms.search.validFrom: 2018-07-31
ms.dyn365.ops.version: Talent July 2018 update
ms.openlocfilehash: 546ec5a77d566b6f5739a604e26c0a60c5ff289a
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 10/13/2020
ms.locfileid: "4462761"
---
# <a name="whats-new-or-changed-in-dynamics-365-talent---core-hr-july-2018"></a>มีอะไรใหม่หรือเปลี่ยนแปลงใน Dynamics 365 Talent - Core HR (กรกฎาคม 2018)

หัวข้อนี้อธิบายถึงคุณลักษณะที่ใหม่หรือที่มีการเปลี่ยนแปลง อย่างใดอย่างหนึ่งใน Microsoft Dynamics 365 Talent: Core HR

## <a name="power-apps-personalization"></a>การกำหนดเป็นแบบส่วนบุคคล Power Apps

Talent สนับสนุนการรวมกับบริการ Microsoft Power Apps Power Apps อนุญาตให้ทั้งนักพัฒนาและผู้ใช้ที่ไม่ใช่ทางเทคนิคสามารถสร้างแอปทางธุรกิจที่กำหนดเองได้สำหรับอุปกรณ์เคลื่อนที่ แท็บเล็ต และเว็บ โดยไม่ต้องเขียนรหัส แอปที่คุณ องค์กรของคุณ หรือระบบแวดล้อมที่กว้างขึ้น พัฒนาโดยใช้ Power Apps สามารถถูกฝังได้ในไคลเอนต์ Talent เพื่อเสริมฟังก์ชันของผลิตภัณฑ์ ตัวอย่างเช่น คุณอาจสร้างแอปที่เสริม Talent ด้วยข้อมูลที่ถูกดึงมาจากระบบอื่น

สำหรับข้อมูลเพิ่มเติม ดู [ฝังแอป Power Apps](../fin-and-ops/get-started/embed-power-apps.md)

## <a name="ceridian-payroll-integration"></a>การรวมระบบค่าจ้าง Ceridian

การรวมระหว่าง Talent และ Ceridian Dayforce พร้อมใช้งานแล้วในขณะนี้ สำหรับสหรัฐอเมริกา แคนาดา และเม็กซิโกรวม การรวมใช้ประเภทที่กว้างของข้อมูล ยกตัวอย่างเช่น

- ข้อมูลทรัพยากรบุคคล
- ข้อมูลค่าตอบแทน
- ข้อมูลค่าจ้าง เช่น รอบการชำระค่าจ้าง รอบระยะเวลาการชำระค่าจ้าง และรหัสรายได้
- ข้อมูลของผู้ปฏิบัติงาน

ดูข้อมูลเพิ่มเติมที่ [ตั้งค่าคอนฟิกการรวมระบบค่าจ้างระหว่าง Talent และ Dayforce](configure-payroll-integration.md)

## <a name="worker-tax-regions-have-been-expanded-beyond-the-us"></a>ภูมิภาคการเก็บภาษีของผู้ปฏิบัติงานถูกขยายไปนอกเหนือจากสหรัฐอเมริกา

มีการเพิ่มการสนับสนุนสำหรับภูมิภาคการเก็บภาษีภายนอกสหรัฐอเมริกา เมื่อภูมิภาคการเก็บภาษีถูกกำหนดให้กับผู้ปฏิบัติงาน จะสามารถไดรฟ์การคำนวณภาษี และสามารถถูกใช้ในการรวมกับโซลูชันระบบค่าจ้างภายนอกได้

## <a name="the-title-field-has-been-expanded-in-talent"></a>ฟิลด์ชื่อได้ถูกขยายใน Talent

ชื่อเรื่องถูกขยายในการอัพเดตนี้ ขณะนี้ฟิลด์คือ 65 อักขระ การเปลี่ยนแปลงนี้มีการใช้งานทุกที่ ที่ชื่อเรื่องถูกเลือกไว้ เช่น ผู้ปฏิบัติงาน ตำแหน่งงาน และงาน

## <a name="benefit-enrollment-status-report"></a>รายงานสถานะการลงทะเบียนสวัสดิการ

การรายงานภายในเกี่ยวกับการเปิดการลงทะเบียนสำหรับสวัสดิการ จะช่วยให้คุณเข้าใจที่ซึ่งพนักงานของคุณอยู่ในกระบวนการเปิดลงทะเบียนได้ง่าย คุณสามารถเรียนรู้จำนวนพนักงานที่เสร็จสิ้นกระบวนการ ขณะนี้จะอยู่ในกำลังดำเนินการให้สำเร็จ และยังไม่ได้เริ่มต้น นอกจากนี้ คุณสามารถดูปัญหาใดๆ ที่เกิดขึ้นในระหว่างการลงทะเบียนสำหรับพนักงาน และบันทึกเต็มของการส่งซ้ำของพนักงานทั้งหมด ดังนั้น คุณสามารถตรวจสอบ และตรวจสอบการส่งซ้ำของพนักงานได้อย่างง่ายดาย
