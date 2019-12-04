---
title: การรวมข้อมูลแบบใกล้เวลาจริงกับ Common Data Service
description: หัวข้อนี้จะแสดงภาพรวมของการรวมของข้อมูลผลิตภัณฑ์ระหว่างแอป Finance and Operations และ Common Data Service
author: RamaKrishnamoorthy
manager: AnnBe
ms.date: 07/15/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2019-07-15
ms.openlocfilehash: 11a5792c9c039eb76337309ef2fdb2b994ce191a
ms.sourcegitcommit: fbc106af09bdadb860677f590464fb93223cbf65
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 11/06/2019
ms.locfileid: "2772398"
---
# <a name="near-real-time-data-integration-with-common-data-service"></a>การรวมข้อมูลแบบใกล้เวลาจริงกับ Common Data Service

[!include [banner](../includes/banner.md)]

ในโลกดิจิทัลปัจจุบัน ระบบนิเวศธุรกิจใช้แอปพลิเคชัน Microsoft Dynamics 365 ทั้งหมด เนื่องจากข้อมูลจากบุคคล ลูกค้า การดำเนินงาน และอุปกรณ์ Internet of Things (IoT) จะไหลเข้ามายังแหล่งเดียว มีโอกาสสำหรับลูปผลป้อนกลับดิจิทัล เพื่อให้ประสบการณ์นี้บรรลุผลสำเร็จ การรวมระหว่างแอพลิเคชัน Finance and Operations และแอพลิเคชั่น Dynamics 365 อื่น ๆ เป็นสิ่งจำเป็น แอพลิเคชันบางส่วนถูกสร้างขึ้นบน Common Data Service การรวมกันของข้อมูลระหว่างแอพลิเคชัน Finance and Operations กับ Common Data Service อนุญาตให้แอพลิเคชันอื่น ๆ สามารถสื่อสารได้อย่างสอดคล้องกันและได้อย่างคล่องแคล่วกับ Finance and Operations

แอพลิเคชัน Finance and Operations และ Common Data Service ให้การซิงโครไนส์ข้อมูลแบบใกล้เรียลไทม์ระหว่างแอพลิเคชัน Finance and Operations และแอพลิเคชัน Dynamics 365 อื่น ๆ ผ่านกรอบงานการเขียนแบบคู่ ความครอบคลุมกว้างและครอบคลุมถึง 28 พื้นที่ผิวของแอพลิเคชัน เป้าหมายคือเพื่อให้ประสบการณ์ผู้ใช้งาน "Dynamics 365 หนึ่งรายการ" ผ่านโฟลว์ข้อมูลแบบราบรื่นที่เชื่อมต่อกระบวนการทางธุรกิจระหว่างแอพลิเคชัน

![ไดอะแกรมภาพรวมของสถาปัตยกรรม](media/dual-write-overview.jpg)

ข้อเสนอของค่าต่อไปนี้จะพร้อมใช้งาน:

+ [ลำดับชั้นขององค์กรใน Common Data Service](dual-write-organization.md)
+ [แนวคิดของบริษัทใน Common Data Service](dual-write-company.md)
+ [ข้อมูลหลักของลูกค้าแบบรวม](dual-write-customer.md)
+ [บัญชีแยกประเภทที่รวม](dual-write-ledger.md)
+ [ประสบการณ์ใช้งานผลิตภัณฑ์แบบครบวงจร](dual-write-product.md)
+ [ข้อมูลหลักของผู้จัดจำหน่ายแบบรวม](dual-write-vendor.md)
+ [ไซต์และคลังสินค้าแบบรวม](dual-write-sites-and-warehouses.md)
+ [ข้อมูลหลักของภาษีรวม](dual-write-tax.md)

## <a name="system-requirements"></a>ความต้องการของระบบ

โฟลว์ข้อมูลแบบใกล้เรียลไทม์ สองทิศทาง แบบซิงโครนัส จำเป็นต้องมีรุ่นต่อไปนี้:

+ Microsoft Dynamics 365 for Finance and Operations รุ่น 10.0.4 (กรกฎาคม 2019) ที่มีการปรับปรุงแพลตฟอร์ม 28 หรือสูงกว่า
+ Microsoft Dynamics 365 for Customer Engagement รุ่นแพลตฟอร์ม 9.1 (4.2) หรือใหม่กว่า

## <a name="setup-instructions"></a>คำแนะนำในการตั้งค่า

ทำตามขั้นตอนเหล่านี้เพื่อตั้งค่าการรวมระหว่างแอพลิเคชัน Finance and Operations และ Common Data Service
    
1. สำหรับการตั้งค่าของระบบการเขียนแบบคู่ ให้ดูที่ [คำแนะนำทีละขั้นตอน](https://aka.ms/dualwrite-docs) ในการประกาศการแสดงตัวอย่างการเขียนแบบคู่
2. ดาวน์โหลดและติดตั้งโซลูชันจากกลุ่ม [Finance and Operations Common Data Service และการรวม Customer Engagement](https://www.yammer.com/dynamicsaxfeedbackprograms/#/threads/inGroup?type=in_group&feedId=66052096) Yammer แพคเกจประกอบด้วยโซลูชันห้ารายการ:

    + Dynamics365Company
    + CurrencyExchangeRates
    + Dynamics365FinanceAndOperationsCommon
    + Dynamics365FinanceCommon
    + Dynamics365SupplyChainCommon

3. ทำตามลำดับการดำเนินการสำหรับ [การซิงโครไนซ์ข้อมูลอ้างอิงเริ่มต้น](dual-write-initial.md)
4. หากคุณพบปัญหาการซิงโครไนส์การเขียนแบบคู่ ให้ดูที่ [คู่มือการแก้ไขปัญหาสำหรับการรวมข้อมูล](dual-write-troubleshooting.md)

> [!IMPORTANT]
> คุณไม่สามารถเรียกใช้การเขียนแบบคู่และ [ผู้ที่มีแนวโน้มจะเป็นลูกค้าเป็นเงินสด](https://docs.microsoft.com/dynamics365/unified-operations/supply-chain/sales-marketing/accounts-template-mapping-direct) แบบเคียงข้างกันได้ ถ้าคุณกำลังเรียกใช้โซลูชันผู้ที่มีแนวโน้มจะเป็นลูกค้าเป็นเงินสด คุณต้องถอนการติดตั้ง นอกจากนี้ คุณต้องปิดใช้งานเท็มเพลตการเขียนแบบคู่ของลูกค้าและผู้จัดจำหน่ายที่เป็นส่วนหนึ่งของโซลูชันผู้ที่มีแนวโน้มจะเป็นลูกค้าเป็นเงินสด
