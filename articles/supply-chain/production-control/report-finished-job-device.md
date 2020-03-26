---
title: รายงานเมื่อเสร็จไปยังสถานที่ที่ควบคุมป้ายทะเบียนจากอุปกรณ์สำหรับบัตรงาน
description: หัวข้อนี้อธิบายกระบวนการสำหรับการดำเนินการผลิตภัณฑ์สำเร็จรูปให้เสร็จสมบูรณ์ในใบสั่งผลิตไปยังสินค้าคงคลัง เมื่อป้ายทะเบียนควบคุมสถานที่
author: johanhoffmann
manager: AnnBe
ms.date: 01/06/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: JmgRegistration, ProdJournalTransJob, ProdJournalTransRoute, ProdParmReportFinished
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 19351
ms.assetid: bcc9e242-b4b8-4144-b14d-c3c106fb40ec
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2019-09-06
ms.dyn365.ops.version: AX 10.0.6
ms.openlocfilehash: 5f61c1abfb115f02e6ff314f6a3e42bb1d3b543f
ms.sourcegitcommit: f38302b9430f2ab3efe91d0a7beff946bc610e8f
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 02/28/2020
ms.locfileid: "3092579"
---
[!include [banner](../includes/banner.md)]

# <a name="report-as-finished-to-a-license-plate-controlled-location-from-the-job-card-device"></a>รายงานเมื่อเสร็จไปยังสถานที่ที่ควบคุมป้ายทะเบียนจากอุปกรณ์สำหรับบัตรงาน 

กระบวนการที่เรียกว่ารายงานเมื่อผลิตภัณฑ์สำเร็จรูปในใบสั่งผลิตเสร็จสมบูรณ์จนส่งไปยังสินค้าคงคลัง ถ้าผลิตภัณฑ์สำเร็จรูปถูกเปิดใช้งานสำหรับกระบวนการคลังสินค้าขั้นสูง ผลิตภัณฑ์จะถูกรายงานว่าสำเร็จไปยังสถานที่ที่เรียกว่าที่สถานที่ผลิตผลผลิต สำหรับข้อมูลเพิ่มเติมเกี่ยวกับการตั้งค่าสถานที่ผลิตผลผลิต กรุณาดูที่ [สถานที่ผลิตผลผลิต](https://docs.microsoft.com/dynamics365/unified-operations/supply-chain/production-control/production-output-location)

ถ้าที่ตั้งเอาท์พุทการผลิตเป็นป้ายทะเบียนที่ควบคุม ต้องมีการระบุป้ายทะเบียนเมื่อมีการรายงานเป็นเสร็จสิ้น ฟิลด์ **ป้ายทะเบียน** จะปรากฏทันทีบน **รายงานความคืบหน้า** บนหน้า **อุปกรณ์สำหรับบัตรงาน** ฟิลด์จะปรากฏเฉพาะในพร้อมต์ **ความคืบหน้าของรายงาน** เมื่อรายงานเกี่ยวกับการดำเนินงานสุดท้ายของใบสั่งผลิตและสินค้าสำหรับใบสั่งผลิตถูกเปิดใช้งานสำหรับกระบวนการจัดการคลังสินค้า 

มีตัวเลือกสองตัวเลือกสำหรับการให้ป้ายทะเบียน
- ผู้ใช้กำลังเลือกป้ายทะเบียนที่มีอยู่ในฟิลด์ป้ายทะเบียน
- ป้ายทะเบียนจะถูกสร้างขึ้นโดยอัตโนมัติจากลำดับหมายเลขและถูกกำหนดเป็นค่าเริ่มต้นไปยังฟิลด์ป้ายทะเบียน

ตัวเลือกที่มีป้ายทะเบียนที่สร้างขึ้นโดยอัตโนมัติถูกตั้งค่าคอนฟิกโดยการเลือกตัวเลือก **สร้างป้ายทะเบียน** บนหน้า **ตั้งค่าคอนฟิกบัตรงานสำหรับอุปกรณ์**
