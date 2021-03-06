---
title: ปริมาณงานการดำเนินการผลิตสำหรับ Cloud และ edge scale unit
description: หัวข้อนี้จะอธิบายวิธีการทำงานของปริมาณงานการดำเนินการผลิตกับ Cloud และ edge scale unit
author: cabeln
manager: ''
ms.date: 10/06/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: SCM
ms.author: cabeln
ms.search.validFrom: 2020-10-06
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: 08c46655d3966ad1433935318c5e60667dd10bb6
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 01/15/2021
ms.locfileid: "4967787"
---
# <a name="manufacturing-execution-workloads-for-cloud-and-edge-scale-units"></a>ปริมาณงานการดำเนินการผลิตสำหรับ Cloud และ edge scale unit

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

> [!WARNING]
> ฟังก์ชันธุรกิจบางอย่างไม่ได้รับการสนับสนุนอย่างเต็มที่ในตัวอย่างสำหรับสาธารณะเมื่อมีการใช้ปริมาณงาน scale unit

ในการดำเนินการผลิต cloud and edge scale unit จัดส่งความสามารถต่อไปนี้ ถึงแม้ว่า edge unit จะไม่ได้เชื่อมต่อกับฮับ:

- ผู้ปฏิบัติงานเครื่องจักรและหัวหน้างานฝ่ายผลิตสามารถเข้าถึงแผนการผลิตที่มีการดำเนินงาน
- ผู้ปฏิบัติงานในเครื่องสามารถรักษาแผนให้ทันสมัยอยู่เสมอโดยการรันงานการผลิตที่แยกต่างหากและมีการประมวลผล
- หัวหน้างานฝ่ายผลิตสามารถปรับปรุงแผนการดำเนินงานได้
- ผู้ปฏิบัติงานสามารถเข้าถึงเวลาและการเข้างานสำหรับการตอกบัตรเข้าและการตอกบัตรออกบน edge เพื่อให้มั่นใจว่าการคำนวณการจ่ายค่าจ้างของผู้ปฏิบัติงานถูกต้อง

หัวข้อนี้จะอธิบายวิธีการทำงานของปริมาณงานการดำเนินการผลิตกับ Cloud และ edge scale unit

## <a name="the-manufacturing-lifecycle"></a>วงจรการผลิต

ดังภาพที่แสดงต่อไปนี้ วงจรการผลิตจะถูกแบ่งออกเป็นสามระยะ ได้แก่ *วางแผน* *ดำเนินการ* และ *จบการทำงาน*

[![ระยะการดำเนินการผลิตเมื่อมีการใช้สภาพแวดล้อมเดียว](media/mes-phases.png "ระยะการดำเนินการผลิตเมื่อมีการใช้สภาพแวดล้อมเดียว")](media/mes-phases-large.png)

ระยะของ _แผน_ รวมถึงข้อกำหนดผลิตภัณฑ์ การวางแผน การสร้างใบสั่งและการจัดกำหนดการ และการนำออกใช้ ขั้นตอนการนำออกใช้บ่งชี้การเปลี่ยนจากระยะ _แผน_ ไปยังระยะ _ดำเนินการ_ เมื่อมีการนำใบสั่งผลิตออกใช้ งานใบสั่งผลิตจะมองเห็นได้บนชั้นการผลิตและพร้อมสำหรับการดำเนินการ

เมื่องานการผลิตถูกทำเครื่องหมายเป็นเสร็จสมบูรณ์แล้ว จะย้ายระยะ _การดำเนินการ_ ไปยังระยะ _การเสร็จสิ้น_ ในระยะ _การเสร็จสิ้น_ การลงทะเบียนจากระยะ *การดำเนินการ* จะเป็นไปตามลำดับงานการอนุมัติ ซึ่งถูกคำนวณ อนุมัติ และโอนย้าย ในจุดนั้น ใบสั่งผลิตจะเสร็จสมบูรณ์ ดังนั้น เกณฑ์สำหรับการจ่ายค่าจ้างของผู้ปฏิบัติงานจะถูกสร้างขึ้น

## <a name="splitting-the-execute-phase-into-a-separate-workload"></a>การแบ่งระยะดำเนินการเป็นปริมาณงานที่แยกกัน

ดังภาพที่แสดงต่อไปนี้ เมื่อมีการใช้ scale unit ระยะ _การดำเนินการ_ จะถูกแบ่งออกเป็นปริมาณงานที่แยกกัน

[![ระยะการดำเนินการผลิตเมื่อมีการใช้ scale unit](media/mes-phases-workloads.png "ระยะการดำเนินการผลิตเมื่อมีการใช้ scale unit")](media/mes-phases-workloads-large.png)

แบบจำลองเดี๋ยวนี้จะมาจากการติดตั้งอินสแตนซ์เดียวกับแบบจำลองที่ยึดตามฮับและ scale unit ระยะ _แผน_ และ _การเสร็จสิ้น_ จะรันเป็นการดำเนินงานของฝ่ายสนับสนุนบนฮับ และปริมาณงานการดำเนินการผลิตจะรันบน scale unit ข้อมูลจะถูกโอนย้ายแบบอะซิงโครนัสระหว่างฮับและ scale unit

เมื่อมีการนำใบสั่งผลิตออกใช้บนฮับ ข้อมูลทั้งหมดที่จำเป็นต้องใช้ในการประมวลผลงานการผลิตจะถูกโอนย้ายไปยัง scale unit ข้อมูลนี้รวมถึง ใบสั่งผลิต กระบวนการผลิต รายการวัสดุ และผลิตภัณฑ์ ข้อมูลที่ไม่เกี่ยวข้องกับใบสั่งผลิต (เช่น กิจกรรมทางอ้อม รหัสการขาดงาน และพารามิเตอร์การผลิต) จะถูกโอนย้ายจากฮับไปยัง scale unit ในฐานะที่เป็นกฎ ข้อมูลที่มีต้นกำเนิดมาจากฮับและมีการโอนย้ายไปยัง scale unit. สามารถสร้างหรืออัปเดตได้บนฮับเท่านั้น ตัวอย่างเช่น รหัสการขาดงานใหม่หรือกิจกรรมทางอ้อมไม่สามารถสร้างขึ้นบน scale unit&mdash;สามารถใช้สำหรับการลงทะเบียนได้เท่านั้น การลงทะเบียนที่ทำบน scale unit ระหว่างการดำเนินการจะถูกโอนย้ายไปยังฮับ ซึ่งจะมีการประมวลผลการอนุมัติเวลาและการเข้างาน สินค้าคงคลัง และการอัปเดตทางการเงิน

## <a name="manufacturing-execution-tasks-that-can-be-run-on-workloads"></a>งานการดำเนินการผลิตที่สามารถรันบนปริมาณงาน

สามารถรันงานการดำเนินการผลิตต่อไปนี้บนปริมาณงานเมื่อมีการใช้ scale unit:

- การตอกบัตรเข้า ล็อกอิน การตอกบัตรออก และการขาดงาน
- เริ่มต้นงาน
- การรวมกลุ่มงาน
- ความคืบหน้าของรายงาน
- รายงานของเสีย
- กิจกรรมทางอ้อม
- ตัวแบ่ง

## <a name="working-with-manufacturing-execution-workloads-on-the-hub"></a>การทำงานกับปริมาณงานการดำเนินการผลิตบนฮับ

โดยทั่วไป กระบวนการที่จำเป็นในการรันปริมาณงานการดำเนินการผลิตจะรันโดยอัตโนมัติเพื่อเก็บฮับและ scale unit ทั้งหมดในการซิงค์ ตามต้องการ อย่างไรก็ตาม ถ้าคุณกำลังประสบปัญหา คุณสามารถทริกเกอร์การประมวลผลการลงทะเบียนดิบที่ได้รับจากปริมาณงาน และ/หรือ ตรวจสอบล็อกการประมวลผลการลงทะเบียนด้วยตนเองได้

### <a name="manually-process-raw-registrations"></a>ประมวลผลการลงทะเบียนดิบด้วยตนเอง

ชุดงานใน Supply Chain Management จะรันโดยอัตโนมัติเพื่อประมวลผลการลงทะเบียนทั้งหมดที่ได้รับมาจากปริมาณงาน งานนี้จะสร้างสมุดรายวันการผลิตที่จำเป็นและรายการบันทึกเมื่อมีการประมวลผลการลงทะเบียนสำหรับงานที่เสร็จสมบูรณ์แล้วในปริมาณงาน

ถึงแม้ว่างานจะรันโดยอัตโนมัติ คุณสามารถรันด้วยตนเองได้ตลอดเวลาด้วยการล็อกอินเข้าฮับและไปที่ **การควบคุมการผลิต \> งานประจำงวด \> การจัดการปริมาณงานของฝ่ายสนับสนุน \> ประมวลผลการลงทะเบียนดิบ**

### <a name="check-the-raw-registration-processing-log"></a>ตรวจสอบล็อกการประมวลผลการลงทะเบียนดิบ

เมื่อต้องการตรวจสอบล็อกการประมวลผลการลงทะเบียน ให้ล็อกอินเข้าฮับ และไปที่ **การควบคุมการผลิต \> งานประจำงวด \> การจัดการปริมาณงานของฝ่ายสนับสนุน \> ล็อกการประมวลผลการลงทะเบียนดิบ** หน้า **ล็อกการประมวลผลการลงทะเบียนดิบ** จะแสดงรายการการลงทะเบียนดิบที่ประมวลผลและสถานะของการลงทะเบียนแต่ละรายการ

![หน้าล็อกการประมวลผลการลงทะเบียนดิบ](media/mes-processing-log.png "หน้าล็อกการประมวลผลการลงทะเบียนดิบ")

คุณสามารถทำงานกับการลงทะเบียนใดก็ได้ในรายการ โดยเลือกการลงทะเบียน แล้วเลือกปุ่มอย่างใดอย่างหนึ่งต่อไปนี้ในบานหน้าต่างการดำเนินการ:

- **กระบวนการ** – ประมวลผลการลงทะเบียนที่เลือกด้วยตนเอง การดำเนินการนี้อาจเป็นประโยชน์ถ้างาน _ประมวลผลการลงทะเบียนดิบ_ ไม่ได้รันอยู่ หรือถ้าล้มเหลว
- **ยกเลิก** – ยกเลิกการลงทะเบียนที่เลือก

## <a name="working-with-manufacturing-execution-workloads-on-a-scale-unit"></a>การทำงานกับปริมาณงานการดำเนินการผลิตบน scale unit

โดยทั่วไป กระบวนการที่จำเป็นในการรันปริมาณงานการดำเนินการผลิตจะรันโดยอัตโนมัติเพื่อเก็บฮับและ scale unit ทั้งหมดในการซิงค์ ตามต้องการ อย่างไรก็ตาม ถ้าคุณกำลังประสบปัญหา คุณสามารถตรวจสอบประวัติของใบสั่งที่มีการประมวลผลไว้ใน scale unit หรือรันงาน _ตัวประมวลผลข้อความของฮับการดำเนินการผลิตไปยัง scale unit_

### <a name="view-the-history-of-manufacturing-jobs-that-have-been-processed-on-a-scale-unit"></a>ดูประวัติของงานการผลิตที่มีการประมวลผลไว้ใน scale unit

เมื่อต้องการตรวจสอบประวัติของงานการผลิตที่มีการประมวลผลไว้ใน scale unit ให้ล็อกอินเข้าสู่เครื่องจักร scale unit และไปที่ **การควบคุมการผลิต \> งานประจำงวด \> การจัดการปริมาณงานของฝ่ายสนับสนุน \> ประวัติการประมวลผลงานการผลิต** หน้า **ประวัติการประมวลผลงานการผลิต** จะแสดงประวัติการประมวลผลของใบสั่งผลิตใน scale unit คุณสามารถทำงานกับใบสั่งผลิตใดก็ได้ในรายการ โดยเลือกการลงทะเบียน แล้วเลือกปุ่มอย่างใดอย่างหนึ่งต่อไปนี้ในบานหน้าต่างการดำเนินการ:

- **กระบวนการ** – ประมวลผลใบสั่งผลิตที่เลือกด้วยตนเอง
- **ยกเลิก** – ยกเลิกใบสั่งผลิตที่เลือก

### <a name="manufacturing-hub-to-scale-unit-message-processor-job"></a>งานตัวประมวลผลข้อความของฮับการผลิตไปยัง scale unit

งาน _ตัวประมวลผลข้อความของฮับการผลิตไปยัง scale unit_ ประมวลผลข้อมูลจากฮับไปยัง scale unit งานนี้จะเริ่มต้นโดยอัตโนมัติเมื่อมีการปรับใช้ปริมาณงานการดำเนินการผลิต อย่างไรก็ตาม คุณสามารถรันด้วยตนเองได้ตลอดเวลา โดยไปที่ **การควบคุมการผลิต \> งานประจำงวดของ \> การจัดการปริมาณงานของฝ่ายสนับสนุน \> ตัวประมวลผลข้อความของฮับการผลิตไปยัง scale unit**
