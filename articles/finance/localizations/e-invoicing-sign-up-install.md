---
title: ลงทะเบียนและติดตั้งบริการออกใบแจ้งหนี้อิเล็กทรอนิกส์
description: บทความนี้มีข้อมูลเกี่ยวกับวิธีการลงทะเบียนและติดตั้งบริการออกใบแจ้งหนี้อิเล็กทรอนิกส์
author: dkalyuzh
ms.date: 02/07/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: dkalyuzh
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: 57314058883e60599bc51d91a65b0daeae724bb7
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 06/03/2022
ms.locfileid: "8865539"
---
# <a name="sign-up-for-and-install-the-electronic-invoicing-service"></a>ลงทะเบียนและติดตั้งบริการออกใบแจ้งหนี้อิเล็กทรอนิกส์

[!include [banner](../includes/banner.md)]

บทความนี้มีข้อมูลเกี่ยวกับวิธีการลงทะเบียนและติดตั้งบริการออกใบแจ้งหนี้อิเล็กทรอนิกส์ กระบวนการนี้มีอยู่สี่ขั้นตอน ขั้นตอนที่ 1 ถึง 3 เป็นขั้นตอนบังคับ และขั้นตอนที่ 4 ไม่บังคับ

### <a name="step-1-sign-up-for-regulatory-configuration-service"></a>ขั้นตอนที่ 1: ลงทะเบียน Regulatory Configuration Service

Regulatory Configuration Service (RCS) มีประสบการณ์การตั้งค่าคอนฟิกและออกแบบที่ใช้ในการตั้งค่าคอนฟิกการออกใบแจ้งหนี้อิเล็กทรอนิกส์ ทรัพยากร เช่น สภาพแวดล้อมและคุณลักษณะการออกใบแจ้งหนี้อิเล็กทรอนิกส์จะถูกสร้าง เก็บรักษา และจัดการใน RCS เมื่อทรัพยากรพร้อมแล้ว จะมีการเผยแพร่ไปยังบริการออกใบแจ้งหนี้อิเล็กทรอนิกส์

สำหรับข้อมูลเพิ่มเติมเกี่ยวกับ RCS ดูที่ [Regulatory Configuration Services (RCS) - คุณลักษณะมาตรฐานโลก](rcs-globalization-feature.md)

การลงทะเบียนสำหรับ RCS ไปที่หน้า [Regulatory Configuration Service](https://marketing.configure.global.dynamics.com/)

### <a name="step-2-install-the-add-in-for-microservices-in-microsoft-dynamics-lifecycle-services"></a>ขั้นตอนที่ 2: ติดตั้ง Add-in สำหรับไมโครเซอร์วิสใน Microsoft Dynamics Lifecycle Services

บริการออกใบแจ้งหนี้อิเล็กทรอนิกส์เป็นชุดของไมโครเซอร์วิสที่โฮสต์ในศูนย์ข้อมูลของ Microsoft ตามค่าเริ่มต้น ลูกค้าของ Dynamics 365 Finance และ Dynamics 365 Supply Chain Management จะไม่มีสิทธิ์เข้าถึงบริการออกใบแจ้งหนี้อิเล็กทรอนิกส์ คุณต้องติดตั้งเป็น Add-in ใน Microsoft Dynamics Lifecycle Services (LCS) เมื่อคุณติดตั้ง Add-in สภาพแวดล้อม Finance หรือ Supply Chain Management จะถูกลงทะเบียนในทะเบียนของแอปพลิเคชันที่ได้รับอนุญาตให้เชื่อมต่อกับบริการออกใบแจ้งหนี้อิเล็กทรอนิกส์

การทำตามขั้นตอนนี้ ดูที่ [ติดตั้ง Add-in สำหรับไมโครเซอร์วิสใน Lifecycle Services](e-invoicing-install-add-in-microservices-lcs.md)

### <a name="step-3-set-up-rcs"></a>ขั้นตอนที่ 3: ตั้งค่า RCS

คุณต้องตั้งค่าการรวมระหว่าง RCS กับบริการออกใบแจ้งหนี้อิเล็กทรอนิกส์ คุณต้องตั้งค่าส่วนประกอบหลักด้วย

การทำตามขั้นตอนนี้ ดูที่ [ตั้งค่า Regulatory Configuration Service (RCS)](e-invoicing-set-up-rcs.md)

### <a name="step-4-microsoft-power-platform-plug-in-admin-reference"></a>ขั้นตอนที่ 4: ข้อมูลอ้างอิงการจัดการปลั๊กอิน Microsoft Power Platform

บางสถานการณ์ต้องมีการรวมกับ Dataverse ในขอบเขตของ Microsoft Power Platform

ปัจจุบัน การตั้งค่านี้เป็นการตั้งค่าที่บังคับถ้าคุณจะใช้โซลูชันการออกใบแจ้งหนี้อิเล็กทรอนิกส์สำหรับการออกใบแจ้งหนี้อิเล็กทรอนิกส์ของอินโดนีเซีย อย่างไรก็ตาม คุณสามารถเลือกได้สำหรับกรณีการออกใบแจ้งหนี้อิเล็กทรอนิกส์ของซาอุดีอาระเบีย สำหรับข้อมูลเพิ่มเติม ดูที่ [ความพร้อมใช้งานของคุณลักษณะการออกใบแจ้งหนี้อิเล็กทรอนิกส์ตามประเทศหรือภูมิภาค](e-invoicing-country-specific-availability.md)

การทำตามขั้นตอนนี้ ดูที่ [ข้อมูลอ้างอิงการจัดการปลั๊กอิน Microsoft Power Platform](e-invoicing-power-platform-plug-in.md)
