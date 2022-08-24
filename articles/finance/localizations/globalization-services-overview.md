---
title: บริการแบบสากล Dynamics 365
description: บทความนี้แสดงภาพรวมของบริการแบบสากล Microsoft Dynamics 365
author: kfend
ms.date: 04/12/2021
ms.topic: overview
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: filatovm
ms.search.validFrom: 2020-02-01
ms.dyn365.ops.version: AX 10.0.9
ms.custom: 97423,  ""intro-internal
ms.assetid: ''
ms.search.form: RCS, Regulatory Configuration Services, Localization, Electronic invoicing, Tax calculation
ms.openlocfilehash: eebf74ab30a544f6561cf5782148d12b58d9c4b7
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 08/12/2022
ms.locfileid: "9278246"
---
# <a name="dynamics-365-globalization-services"></a>บริการแบบสากล Dynamics 365

[!include [banner](../includes/banner.md)]

บริการสากลต่อไปนี้สามารถตั้งค่าคอนฟิกเพื่อขยายความสามารถที่มีอยู่ในบริการออนไลน์ Microsoft Dynamics 365 บางบริการ:

- **Regulatory Configuration Service (RCS)** สนับสนุนการตั้งค่าคอนฟิกของเอกสารและรายงานอิเล็กทรอนิกส์ชนิดต่างๆ RCS ให้โปรแกรมออกแบบการรายงานทางอิเล็กทรอนิกส์ (ER) ขั้นสูง ซึ่งที่เก็บการตั้งค่าคอนฟิกคือบริการแบบสแตนด์อโลนอยู่ สำหรับข้อมูลเพิ่มเติม ให้ดูที่ [Regulatory Configuration Service](rcs-overview.md)
- **การออกใบแจ้งหนี้ทางอิเล็กทรอนิกส์** จะรวมรูปแบบที่ตั้งค่าคอนฟิกได้ไว้ด้วยกันสากการแปลง ลายเซ็นดิจิทัล และการรวมที่ตั้งค่าคอนฟิกได้ เพื่อการเชื่อมต่อกับเว็บเซอร์วิสภายนอก รวมถึงการจัดการใบรับรองและการตอบสนอง สำหรับข้อมูลเพิ่มเติม โปรดดู [การออกใบแจ้งหนี้ทางอิเล็กทรอนิกส์](e-invoicing-service-overview.md)
- **การคํานวณภาษี** ให้ความยืดหยุ่นเพิ่มขึ้นโดยสนับสนุนหลายรหัสภาษี การกําหนดรหัสภาษี โปรแกรมออกแบบการคํานวณภาษี และกลไกจัดการรันไทม์เพื่อให้เป็นไปตามข้อบังคับด้านภาษีที่ซับซ้อนทั่วโลก หากต้องการทราบข้อมูลเพิ่มเติมเกี่ยวกับการคำนวณ โปรดดูที่ [การคํานวณภาษี](global-tax-calcuation-service-overview.md)

บริการสากลเหล่านี้ให้การรวมแบบสำเร็จรูปกับบริการออนไลน์ของ Dynamics 365 ต่อไปนี้

| บริการออนไลน์ | RCS | การออกใบแจ้งหนี้อิเล็กทรอนิกส์ | การคำนวณภาษี (พรีวิว) |
|----------------|-----|----------------------|---------------------------|
| Dynamics 365 Finance | ใช่ | ใช่ | ใช่ | 
| Dynamics 365 Supply Chain Management | ใช่ | ใช่ | ใช่ | 
| Dynamics 365 Project Operations | ใช่ | ใช่ | ใช้ไม่ได้ | 
| Dynamics 365 Commerce | ใช่ | ใช้ไม่ได้ | ใช้ไม่ได้ | 

> [!NOTE]
> เนื่องจากความแตกต่างในความพร้อมใช้งานของที่ตั้งทางภูมิศาสตร์ของ Azure (ภูมิศาสตร์) ของ RCS จึงทําให้การตั้งค่าคอนฟิกของบริการนี้อาจทําให้คุณสามารถโอนย้ายข้อมูลของลูกค้าที่เป็นบุคคลภายนอกพื้นที่ที่เลือกไว้สำหรับบริการออนไลน์ของ Dynamics 365 ที่เกี่ยวข้องได้ สำหรับข้อมูลเพิ่มเติม โปรดดูที่ [Dynamics 365 และ Power Platform: ความพร้อมใช้งาน ที่ตั้งข้อมูล ภาษา และการแปลเป็นภาษาท้องถิ่น](https://aka.ms/rcs/D365Productavailabilityguide)
