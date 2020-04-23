---
title: รายงานเมื่อเสร็จไปยังสถานที่ที่ควบคุมป้ายทะเบียนจากอุปกรณ์สำหรับบัตรงาน
description: หัวข้อนี้อธิบายกระบวนการสำหรับการดำเนินการผลิตภัณฑ์สำเร็จรูปให้เสร็จสมบูรณ์ในใบสั่งผลิตไปยังสินค้าคงคลัง เมื่อป้ายทะเบียนควบคุมสถานที่
author: johanhoffmann
manager: tfehr
ms.date: 01/06/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: JmgRegistration, ProdJournalTransJob, ProdJournalTransRoute, ProdParmReportFinished
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 19351
ms.assetid: bcc9e242-b4b8-4144-b14d-c3c106fb40ec
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2019-09-06
ms.dyn365.ops.version: AX 10.0.6
ms.openlocfilehash: f5863202facc83afb91b380ba5666334783ccbcf
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 04/02/2020
ms.locfileid: "3211180"
---
[!include [banner](../includes/banner.md)]

# <a name="report-as-finished-to-a-license-plate-controlled-location-from-the-job-card-device"></a>รายงานเมื่อเสร็จไปยังสถานที่ที่ควบคุมป้ายทะเบียนจากอุปกรณ์สำหรับบัตรงาน 

กระบวนการที่เรียกว่ารายงานเมื่อผลิตภัณฑ์สำเร็จรูปในใบสั่งผลิตเสร็จสมบูรณ์จนส่งไปยังสินค้าคงคลัง ถ้าผลิตภัณฑ์สำเร็จรูปถูกเปิดใช้งานสำหรับกระบวนการคลังสินค้าขั้นสูง ผลิตภัณฑ์จะถูกรายงานว่าสำเร็จไปยังสถานที่ที่เรียกว่าที่สถานที่ผลิตผลผลิต สำหรับข้อมูลเพิ่มเติมเกี่ยวกับการตั้งค่าสถานที่ผลิตผลผลิต กรุณาดูที่ [สถานที่ผลิตผลผลิต](https://docs.microsoft.com/dynamics365/unified-operations/supply-chain/production-control/production-output-location)

ถ้าที่ตั้งเอาท์พุทการผลิตเป็นป้ายทะเบียนที่ควบคุม ต้องมีการระบุป้ายทะเบียนเมื่อมีการรายงานเป็นเสร็จสิ้น ฟิลด์ **ป้ายทะเบียน** จะปรากฏทันทีบน **รายงานความคืบหน้า** บนหน้า **อุปกรณ์สำหรับบัตรงาน** ฟิลด์จะปรากฏเฉพาะในพร้อมต์ **ความคืบหน้าของรายงาน** เมื่อรายงานเกี่ยวกับการดำเนินงานสุดท้ายของใบสั่งผลิตและสินค้าสำหรับใบสั่งผลิตถูกเปิดใช้งานสำหรับกระบวนการจัดการคลังสินค้า 

มีตัวเลือกสองตัวเลือกสำหรับการให้ป้ายทะเบียน
- ผู้ใช้กำลังเลือกป้ายทะเบียนที่มีอยู่ในฟิลด์ป้ายทะเบียน
- ป้ายทะเบียนจะถูกสร้างขึ้นโดยอัตโนมัติจากลำดับหมายเลขและถูกกำหนดเป็นค่าเริ่มต้นไปยังฟิลด์ป้ายทะเบียน

ตัวเลือกที่มีป้ายทะเบียนที่สร้างขึ้นโดยอัตโนมัติถูกตั้งค่าคอนฟิกโดยการเลือกตัวเลือก **สร้างป้ายทะเบียน** บนหน้า **ตั้งค่าคอนฟิกบัตรงานสำหรับอุปกรณ์**
