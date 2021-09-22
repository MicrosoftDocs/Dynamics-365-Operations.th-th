---
title: ส่วนประกอบการจัดการการออกใบแจ้งหนี้อิเล็กทรอนิกส์
description: หัวข้อนี้ให้ข้อมูลเกี่ยวกับส่วนประกอบที่เกี่ยวข้องกับการจัดการของการออกใบแจ้งหนี้ทางอิเล็กทรอนิกส์
author: gionoder
ms.date: 08/31/2021
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
ms.search.validFrom: 2020-07-08
ms.dyn365.ops.version: AX 10.0.12
ms.openlocfilehash: d187e8a03552258099d7021ff056d0726ea60ca1
ms.sourcegitcommit: baf82100f0aa7d5f5f47c7f54bc155d8a07beab5
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 08/31/2021
ms.locfileid: "7463892"
---
# <a name="electronic-invoicing-administration-components"></a>ส่วนประกอบการจัดการการออกใบแจ้งหนี้อิเล็กทรอนิกส์

[!include [banner](../includes/banner.md)]


หัวข้อนี้ให้ข้อมูลเกี่ยวกับส่วนประกอบที่เกี่ยวข้องกับการจัดการของการออกใบแจ้งหนี้ทางอิเล็กทรอนิกส์ นอกจากนี้ ยังแสดงข้อมูลเกี่ยวกับวิธีการตั้งค่าคอนฟิกบริการของการออกใบแจ้งหนี้ทางอิเล็กทรอนิกส์

## <a name="azure"></a>Azure

ใช้ Microsoft Azure เพื่อสร้างข้อมูลลับสำหรับ Key Vault และตั้งค่าบัญชีการจัดเก็บ แล้วใช้ข้อมูลลับ Key Vault และโทเค็น SAS ของบัญชีการจัดเก็บในการตั้งค่าคอนฟิกการออกใบแจ้งหนี้ทางอิเล็กทรอนิกส์

## <a name="lifecycle-services"></a>Lifecycle Services

ใช้ Microsoft Dynamics Lifecycle Services (LCS) เพื่อเปิดใช้งาน Add-in การออกใบแจ้งหนี้อิเล็กทรอนิกส์สำหรับโครงการการปรับใช้ LCS ของคุณ

> [!NOTE]
> การติดตั้ง Add-in ใน LCS จำเป็นต้องใช้ **สภาพแวดล้อมระดับ 2** เป็นอย่างน้อย สำหรับข้อมูลเพิ่มเติมเกี่ยวกับการวางแผนสภาพแวดล้อม ดูที่ [การวางแผนสภาพแวดล้อม](../../fin-ops-core/fin-ops/imp-lifecycle/environment-planning.md)
 

## <a name="regulatory-configuration-services"></a>Regulatory Configuration Services

Dynamics 365 Regulatory Configuration Services (RCS) เป็นอินเทอร์เฟซที่ถูกใช้ในการตั้งค่าคอนฟิกการออกใบแจ้งหนี้อิเล็กทรอนิกส์ ทรัพยากร เช่น สภาพแวดล้อมและคุณลักษณะการออกใบแจ้งหนี้ทางอิเล็กทรอนิกส์จะถูกสร้าง เก็บรักษา และโฮสต์ใน RCS เมื่อทรัพยากรพร้อมแล้ว จะมีการเผยแพร่ไปยังบริการการออกใบแจ้งหนี้ทางอิเล็กทรอนิกส์

สำหรับการสมัคร RCS ดูที่ [Regulatory services](https://marketing.configure.global.dynamics.com/)

สำหรับข้อมูลเพิ่มเติมเกี่ยวกับ RCS ดู [Regulatory Configuration Services (RCS) - คุณลักษณะมาตรฐานโลก](rcs-globalization-feature.md)

### <a name="integration-with-electronic-invoicing"></a>การรวมกับการออกใบแจ้งหนี้ทางอิเล็กทรอนิกส์ 

ก่อนที่คุณจะสามารถใช้ RCS เพื่อตั้งค่าคอนฟิกใบแจ้งหนี้อิเล็กทรอนิกส์ คุณจะต้องตั้งค่าคอนฟิก RCS เพื่ออนุญาตให้การสื่อสารกับการออกใบแจ้งหนี้ทางอิเล็กทรอนิกส์ คุณทำการตั้งค่าคอนฟิกนี้ให้เสร็จสมบูรณ์บนแท็บ **การออกใบแจ้งหนี้อิเล็กทรอนิกส์** ของหน้า **พารามิเตอร์การรายงานทางอิเล็กทรอนิกส์**

#### <a name="service-endpoint"></a><a id='svc-endpoint-uris'></a>ปลายทางของบริการ

การออกใบแจ้งหนี้อิเล็กทรอนิกส์พร้อมใช้งานในภูมิศาสตร์ศูนย์ข้อมูล Azure หลายแห่ง ตารางต่อไปนี้จะแสดงรายการความพร้อมใช้งานตามภูมิภาค


| ภูมิศาสตร์ของ Datacenter Azure | URI ปลายทางของบริการ                                                       |
|----------------------------|----------------------------------------------------------------------------|
| สหรัฐ              | <p>https://gw.us-il101.gateway.prod.island.powerapps.com/electronicinvoicing/</p><p>https://gw.us-il102.gateway.prod.island.powerapps.com/electronicinvoicing/</p><p>https://gw.us-il103.gateway.prod.island.powerapps.com/electronicinvoicing/</p><p>https://gw.us-il104.gateway.prod.island.powerapps.com/electronicinvoicing/</p><p>https://gw.us-il105.gateway.prod.island.powerapps.com/electronicinvoicing/</p><p>https://gw.us-il106.gateway.prod.island.powerapps.com/electronicinvoicing/</p><p>https://gw.us-il107.gateway.prod.island.powerapps.com/electronicinvoicing/</p><p>https://gw.us-il108.gateway.prod.island.powerapps.com/electronicinvoicing/</p><p>https://gw.us-il109.gateway.prod.island.powerapps.com/electronicinvoicing</p> |
| ยุโรป                     | <p>https://gw.eu-il101.gateway.prod.island.powerapps.com/electronicinvoicing/</p><p>https://gw.eu-il102.gateway.prod.island.powerapps.com/electronicinvoicing/</p><p>https://gw.eu-il103.gateway.prod.island.powerapps.com/electronicinvoicing/</p><p>https://gw.eu-il104.gateway.prod.island.powerapps.com/electronicinvoicing/</p><p>https://gw.eu-il105.gateway.prod.island.powerapps.com/electronicinvoicing/</p><p>https://gw.eu-il106.gateway.prod.island.powerapps.com/electronicinvoicing/</p><p>https://gw.eu-il107.gateway.prod.island.powerapps.com/electronicinvoicing/</p><p>https://gw.eu-il108.gateway.prod.island.powerapps.com/electronicinvoicing/</p><p>https://gw.eu-il109.gateway.prod.island.powerapps.com/electronicinvoicing/</p><p>https://gw.eu-il110.gateway.prod.island.powerapps.com/electronicinvoicing/</p> |
| สหราชอาณาจักร             | <p>https://gw.uk-il101.gateway.prod.island.powerapps.com/electronicinvoicing/</p><p>https://gw.uk-il102.gateway.prod.island.powerapps.com/electronicinvoicing/</p> |
| เอเชีย                       | <p>https://gw.as-il101.gateway.prod.island.powerapps.com/electronicinvoicing/</p><p>https://gw.as-il102.gateway.prod.island.powerapps.com/electronicinvoicing/</p> |

### <a name="service-environments"></a>สภาพแวดล้อมของบริการ

สภาพแวดล้อมของบริการคือ พาร์ติชันเชิงตรรกะที่ถูกสร้างขึ้นเพื่อสนับสนุนการปฏิบัติการของคุณลักษณะแบบโลกาภิวัฒน์ในการออกใบแจ้งหนี้ทางอิเล็กทรอนิกส์ ความลับด้านความปลอดภัยและใบรับรองดิจิทัล และการควบคุม (คือการให้สิทธิการเข้าถึง) ต้องตั้งค่าคอนฟิกที่ระดับสภาพแวดล้อมการให้บริการ

ลูกค้าสามารถสร้างสภาพแวดล้อมในการให้บริการได้มากเท่าที่ต้องการ สภาพแวดล้อมการบริการทั้งหมดที่ลูกค้าสร้างจะไม่ขึ้นต่อกัน

คุณต้องสร้างและรักษาสภาพแวดล้อมการให้บริการใน RCS เมื่อทรัพยากรบริการพร้อมแล้ว ต้องมีการเผยแพร่ไปยังการออกใบแจ้งหนี้ทางอิเล็กทรอนิกส์

#### <a name="service-environment-status"></a>สถานะสภาพแวดล้อมการให้บริการ

สภาพแวดล้อมการให้บริการสามารถจัดการผ่านสถานะได้ ตัวเลือกที่เป็นไปได้มีดังนี้

- **ไมได้เผยแพร่** – สร้างสภาพแวดล้อมแล้ว แต่ยังไม่ได้เผยแพร่
- **เผยแพร่แล้ว** – สภาพแวดล้อมได้รับการเผยแพร่ไปยังการออกใบแจ้งหนี้ทางอิเล็กทรอนิกส์เแล้ว
- **มีการเปลี่ยนแปลง** – แอททริบิวต์ของสภาพแวดล้อมที่เผยแพร่มีการเปลี่ยนแปลง แต่การเปลี่ยนแปลงยังไม่ได้รับการเผยแพร่

#### <a name="customer-secrets"></a>ช้อมูลลับของลูกค้า

บริการการออกใบแจ้งหนี้อิเล็กทรอนิกส์มีหน้าที่จัดเก็บข้อมูลทางธุรกิจทั้งหมดของคุณในทรัพยากร Azure ที่บริษัทของคุณเป็นเจ้าของ เพื่อให้แน่ใจว่าการบริการทำงานได้อย่างถูกต้อง และมีการเข้าถึงข้อมูลทางธุรกิจทั้งหมดที่จำเป็นและถูกสร้างขึ้นโดยการออกใบแจ้งหนี้อิเล็กทรอนิกส์อย่างเหมาะสม คุณต้องสร้างทรัพยากร Azure หลักสองอย่าง:

- บัญชีการจัดเก็บข้อมูล Azure (การจัดเก็บ Blob) ที่จะจัดเก็บเอกสารอิเล็กทรอนิกส์ รวมถึงใบแจ้งหนี้อิเล็กทรอนิกส์ ผลลัพธ์ของการแปลงเอกสาร และการตอบสนองจากบริการเว็บภายนอก
- Azure Key Vault ที่จะจัดเก็บใบรับรองและตัวระบุทรัพยากรที่เหมือนกัน (URI) ของบัญชีการจัดเก็บ (โทเค็น SAS)


ต้องมีการปันส่วน Key Vault ที่จัดสรรไว้และบัญชีการจัดเก็บของลูกค้า โดยเฉพาะสำหรับการใช้กับการออกใบแจ้งหนี้อิเล็กทรอนิกส์ สำหรับข้อมูลเพิ่มเติม ดู [สร้างบัญชีการจัดเก็บของ Azure และ Key Vault](e-invoicing-create-azure-storage-account-key-vault.md)

เมื่อต้องการตรวจสอบความสมบูรณ์ของ Key Azure และรับการแจ้งเตือน ให้ตั้งค่าคอนฟิก Azure Monitor for key Vault โดยการเปิดใช้การบันทึก Key Vault คุณสามารถตรวจสอบวิธีการ เวลา และผู้ที่เข้าถึง Key Vaults ของคุณ สำหรับข้อมูลเพิ่มเติม โปรดดูที่ [การตรวจสอบและการแจ้งเตือนของ Azure Key Vault](/azure/key-vault/general/alert) และ [วิธีเปิดใช้งานการบันทึก Key Vault](/azure/key-vault/general/howto-logging?tabs=azure-cli)

ตามแนวทางที่พึงปฏิบัติ ให้หมุนข้อมูลลับเป็นระยะๆ สำหรับข้อมูลเพิ่มเติม ให้ดูที่ [คู่มือข้อมูลลับ](/azure/key-vault/secrets/)

#### <a name="users"></a>ผู้ใช้

สภาพแวดล้อมการบริการแต่ละรายการต้องแสดงรายชื่อผู้ใช้ที่สามารถเชื่อมต่อจาก Dynamics 365 Finance และ Dynamics 365 Supply Chain Management ในการออกใบแจ้งหนี้ทางอิเล็กทรอนิกส์

#### <a name="publication"></a>การเผยแพร่

สภาพแวดล้อมของบริการจะต้องถูกเผยแพร่ไปยังการออกใบแจ้งหนี้อิเล็กทรอนิกส์ ก่อนที่จะนำไปใช้ เฉพาะสภาพแวดล้อมที่เผยแพร่เท่านั้นที่สามารถเข้าถึงโดย Finance and Supply Chain Management นอกจากนี้ ต้องมีการเผยแพร่สภาพแวดล้อมการบริการก่อนที่การอัพเดตแอททริบิวต์จะมีผลกับบริการออกใบแจ้งหนี้ทางอิเล็กทรอนิกส์

### <a name="connected-applications"></a>แอพลิเคชันที่เชื่อมต่อ

แอพลิเคชันที่เชื่อมต่อคืออินสแตนซ์ของ Finance and Supply Chain Management ที่คุณอาจต้องดำเนินการผ่าน RCS นอกจาก URL แอพลิเคชันและผู้เช่าแล้ว แอพลิเคชันที่เชื่อมต่อยังประกอบด้วยข้อมูลอ้างอิงที่ทำให้ RCS สามารถเชื่อมต่อกับสภาพแวดล้อมได้

คุณสามารถตั้งค่าคอนฟิกส่วนของคุณลักษณะการออกใบแจ้งหนี้ทางอิเล็กทรอนิกส์ใน Finance and Supply Chain Management เพื่อใช้งานลักษณะการออกใบแจ้งหนี้ทางอิเล็กทรอนิกส์ทั้งหมดได้โดยผ่านแอพลิเคชันที่เชื่อมต่อ

## <a name="finance-and-supply-chain-management"></a>Finance and Supply Chain Management

### <a name="integration-with-electronic-invoicing"></a>การรวมกับการออกใบแจ้งหนี้ทางอิเล็กทรอนิกส์

ก่อนที่คุณจะสามารถใช้ Finance และ Supply Chain Management เพื่อออกใบแจ้งหนี้อิเล็กทรอนิกส์โดยใช้การออกใบแจ้งหนี้อิเล็กทรอนิกส์ ต้องมีการตั้งค่าคอนฟิกเพื่ออนุญาตให้มีการสื่อสารกับบริการได้

#### <a name="electronic-invoicing-integration-feature"></a>คุณลักษณะการรวมของการออกใบแจ้งหนี้อิเล็กทรอนิกส์

เมื่อต้องการเปิดใช้งานการสื่อสารระหว่าง Finance และ Supply Chain Management และการออกใบแจ้งหนี้ทางอิเล็กทรอนิกส์ คุณต้องเปิดใช้คุณลักษณะ **การรวมการออกใบแจ้งหนี้อิเล็กทรอนิกส์** ในพื้นที่ทำงาน **การจัดการคุณลักษณะ**

#### <a name="service-endpoint"></a>ปลายทางของบริการ

ปลายทางของบริการคือ URL ที่เป็นที่ตั้งของการออกใบแจ้งหนี้ทางอิเล็กทรอนิกส์ ก่อนที่คุณจะสามารถ ใช้ออกใบแจ้งหนี้อิเล็กทรอนิกส์ได้ ต้องกำหนดค่าคอนฟิกจุดสิ้นสุดในการจัดการด้านการเงินและซัพพลายเชนเพื่อให้สามารถสื่อสารกับบริการได้

เมื่อต้องการตั้งค่าคอนฟิกปลายทางของบริการ ไปที่ **การจัดการองค์กร \> ตั้งค่า \> พารามิเตอร์เอกสารอิเล็กทรอนิกส์** จากนั้น บนแท็บ **การออกใบแจ้งหนี้อิเล็กทรอนิกส์** ในฟิลด์ **URL ปลายทาง** ป้อน URL ที่เหมาะสมจากตารางในส่วน [จุดสิ้นสุดบริการ](#svc-endpoint-uris) จากคำอธิบายก่อนหน้านี้ในหัวข้อนี้

#### <a name="environments"></a>สภาพแวดล้อม

ชื่อของสภาพแวดล้อมที่ถูกป้อนใน Finance และ Supply Chain Management หมายถึงชื่อของสภาพแวดล้อมที่ถูกสร้างขึ้นใน RCS และถูกเผยแพร่ไปยังการออกใบแจ้งหนี้ทางอิเล็กทรอนิกส์

สภาพแวดล้อมต้องได้รับการตั้งค่าคอนฟิกบนแท็บ **การออกใบแจ้งหนี้อิเล็กทรอนิกส์** ของหน้า **พารามิเตอร์เอกสารอิเล็กทรอนิกส์** ในลักษณะดังกล่าว ทุกคำขอเพื่อออกใบแจ้งหนี้อิเล็กทรอนิกส์จะมีสภาพแวดล้อมที่การออกใบแจ้งหนี้ทางอิเล็กทรอนิกส์สามารถระบุว่าคุณลักษณะการออกใบแจ้งหนี้ทางอิเล็กทรอนิกส์ใดต้องประมวลผลคำขอ

## <a name="additional-resources"></a>ทรัพยากรเพิ่มเติม

- [ตั้งค่าคอนฟิกใบแจ้งหนี้ทางอิเล็กทรอนิกส์ใน RCS](e-invoicing-configuration-rcs.md)
- [การออกใบแจ้งหนี้อิเล็กทรอนิกส์ในการเงิน และ Supply Chain Management](e-invoicing-issuing-electronic-invoices-finance-supply-chain-management.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
