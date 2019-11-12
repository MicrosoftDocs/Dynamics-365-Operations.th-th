---
title: รายงานเมื่อเสร็จไปยังสถานที่ที่ควบคุมป้ายทะเบียนจากอุปกรณ์สำหรับบัตรงาน
description: หัวข้อนี้อธิบายกระบวนการสำหรับการดำเนินการผลิตภัณฑ์สำเร็จรูปในใบสั่งผลิตไปยังสินค้าคงคลังเมื่อป้ายทะเบียนควบคุมที่ตั้ง
author: johanhoffmann
manager: AnnBe
ms.date: 09/06/2019
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
ms.openlocfilehash: cb809e596fd6bf3030bcee460838798435512b95
ms.sourcegitcommit: d37fb09101c30858bcb975931b3d8f947d72017b
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 10/10/2019
ms.locfileid: "2572140"
---
[!include [banner](../includes/banner.md)]

# <a name="report-as-finished-to-a-license-plate-controlled-location-from-the-job-card-device"></a>รายงานเมื่อเสร็จไปยังสถานที่ที่ควบคุมป้ายทะเบียนจากอุปกรณ์สำหรับบัตรงาน 

กระบวนการที่เรียกว่ารายงานเมื่อผลิตภัณฑ์สำเร็จรูปในใบสั่งผลิตเสร็จสมบูรณ์จนส่งไปยังสินค้าคงคลัง ถ้าผลิตภัณฑ์สำเร็จรูปถูกเปิดใช้งานสำหรับกระบวนการคลังสินค้าขั้นสูง ผลิตภัณฑ์จะถูกรายงานว่าสำเร็จไปยังสถานที่ที่เรียกว่าที่สถานที่ผลิตผลผลิต สำหรับข้อมูลเพิ่มเติมเกี่ยวกับการตั้งค่าสถานที่ผลิตผลผลิต กรุณาดูที่ [สถานที่ผลิตผลผลิต](https://docs.microsoft.com/dynamics365/unified-operations/supply-chain/production-control/production-output-location)

คุณต้องเลือกหมายเลขป้ายทะเบียนที่มีอยู่เพื่อทำให้งานนี้เสร็จสมบูรณ์ ถ้าสถานที่ผลิตผลผลิตมีการตั้งค่าที่ตั้งไว้เพื่อติดตามโดยป้ายทะเบียน สถานที่ผลิตผลผลิตจะต้องระบุหมายเลขป้ายทะเบียนเมื่อรายงานสถานที่ผลิตผลผลิตเมื่อผลิตเสร็จสมบูรณ์ ฟิลด์ **ป้ายทะเบียน** จะปรากฏทันทีบน **รายงานความคืบหน้า** บนหน้า **อุปกรณ์สำหรับบัตรงาน** ฟิลด์นี้จะปรากฏทันที **รายงานความคืบหน้า** เมื่อรายงานเกี่ยวกับการดำเนินงานครั้งสุดท้ายของใบสั่งผลิต ฟิลด์นี้จะแสดงเฉพาะเมื่อสินค้าสำหรับใบสั่งผลิตถูกเปิดใช้งานสำหรับกระบวนการจัดการคลังสินค้า 
