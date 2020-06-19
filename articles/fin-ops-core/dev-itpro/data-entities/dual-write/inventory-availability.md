---
title: ความพร้อมของสินค้าคงคลังในการรวมแบบสองทิศทาง
description: หัวข้อนี้แสดงข้อมูลเกี่ยวกับการตรวบสอบความพร้อมของสินค้าคงคลังในการรวมแบบสองทิศทาง
author: yijialuan
manager: AnnBe
ms.date: 05/26/2020
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
ms.author: riluan
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-05-26
ms.openlocfilehash: dd0995eb8c70ed06cdc3c0f6a28b13b117297533
ms.sourcegitcommit: be7e4378c8122c6e7cfc4e7991efbdffee45e006
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 06/03/2020
ms.locfileid: "3426993"
---
# <a name="inventory-availability"></a>ความพร้อมของสินค้าคงคลัง

[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]

การใช้ความพร้อมของสินค้าคงคลัง คุณสามารถตรวจสอบสินค้าคงคลังของคุณก่อนที่คุณจะเพิ่มผลิตภัณฑ์ลงในฟอร์ม **ใบเสนอราคา** **ใบสั่ง** หรือ **ใบแจ้งหนี้** ในแอปที่เป็นแบบโมเดลใน Dynamics 365 ตัวอย่างเช่น การตรวจสอบสินค้าคงคลังและการกำหนดวันที่การเติมสินค้าเป็นงานหลักในกระบวนการ [ผู้ที่มีแนวโน้มจะเป็นลูกค้าจนถึงเงินสด](dual-write-prospect-to-cash.md) ถ้าคุณมีสินค้าคงคลังไม่เพียงพอ คุณสามารถประเมินวันที่จัดส่งตามการรับและปัญหาสินค้าคงคลังที่คาดการณ์ นอกจากนี้ คุณยังสามารถตรวจสอบข้อมูลที่สามารถสัญญาได้ (ATP) ของผลิตภัณฑ์ ซึ่งคุณสามารถค้นหาปริมาณ ATP ในกรอบเวลาที่กำหนดไว้ล่วงหน้า

## <a name="on-hand-inventory"></a>สินค้าคงคลังคงเหลือ 

ในส่วนหัวของฟอร์ม **ใบเสนอราคา** **ใบสั่ง** หรือ **ใบแจ้งหนี้** ใน Dynamics 365 Sales **สินค้าคงคลังคงเหลือ** ของปุ่มใหม่จะถูกเพิ่ม เมื่อคุณคลิกปุ่ม กล่องโต้ตอบจะปรากฏขึ้น และคุณสามารถระบุบริษัทและผลิตภัณฑ์ที่คุณต้องการตรวจสอบปริมาณคงคลังคงเหลือ ส่งคืนข้อมูลสินค้าคงคลังจาก Dynamics 365 Supply Chain Management และแสดงข้อมูลเดียวกันกับ [ปริมาณคงคลังคงเหลือ](../../../../supply-chain/inventory/tasks/check-availability-stock.md) ข้อมูลรวมถึงปริมาณเหล่านี้:

- **ปริมาณคงเหลือ**
- **ปริมาณคงเหลือที่จองไว้**
- **ปริมาณคงเหลือที่พร้อมใช้งาน**
- **ปริมาณที่สั่ง**
- **ปริมาณที่อยู่ระหว่างการสั่ง**
- **ปริมาณที่สั่งที่จองไว้**
- **ปริมาณที่พร้อมใช้งานรวม**

## <a name="atp-information"></a>ข้อมูล ATP

ในราบการบรรทัดของฟอร์ม **ใบเสนอราคา** **ใบสั่ง** หรือ **ใบแจ้งหนี้** ใน Dynamics 365 Sales **ข้อมูล ATP** ของปุ่มใหม่จะถูกเพิ่ม เมื่อคุณคลิกปุ่ม กล่องโต้ตอบจะปรากฏขึ้น และคุณสามารถระบุบริษัท ผลิตภัณฑ์ ไซต์สินค้าคงคลัง คลังสินค้า และปริมาณการสั่ง ส่งคืน **ข้อมูล ATP** จาก Supply Chain Management และแสดงการตั้งค่า descrbed ใน [สัญญาใบสั่ง](../../../../supply-chain/sales-marketing/delivery-dates-available-promise-calculations.md#atp-calculations) ข้อมูลรวมถึง **ปริมาณ ATP** **ปริมาณที่รับ** **ปริมาณการออกใช้** และ **ปริมาณคงเหลือ**
