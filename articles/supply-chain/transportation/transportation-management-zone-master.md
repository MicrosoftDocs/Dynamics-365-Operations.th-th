---
title: ต้นแบบโซนการจัดการการขนส่ง
description: หัวข้อนี้อธิบายวิธีการจัดการการขนส่งที่ช่วยให้คุณสามารถแบ่งที่ตั้งทางภูมิศาสตร์ออกเป็นโซนได้
author: Henrikan
manager: ''
ms.date: 10/16/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TMSZoneMaster
audience: Application User
ms.reviewer: kamaybac
ms.custom: 12234
ms.assetid: b878478c-0e04-4a1e-a037-6fdbb345a9a3
ms.search.region: Global
ms.author: henrikan
ms.search.validFrom: 2020-01-09
ms.dyn365.ops.version: Release 10.0.14
ms.openlocfilehash: 28c0724a20199595b0e2c19867ccaa4876d37980
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 02/15/2021
ms.locfileid: "5233330"
---
# <a name="transportation-management-zone-master"></a>ต้นแบบโซนการจัดการการขนส่ง

[!include [banner](../includes/banner.md)]

การจัดการการขนส่งที่ช่วยให้คุณสามารถแบ่งที่ตั้งทางภูมิศาสตร์ออกเป็นโซนได้ การแบ่งที่ตั้งเป็นโซนสามารถช่วย:

- **ทำการกำหนดราคาการขนส่งให้ง่าย** – การกำหนดราคาตามโซนเรียบง่ายกว่าการกำหนดราคาตามแต่ละสถานที่ โดยเฉพาะเมื่อสถานที่ขนส่งกระจัดกระจาย
- **เพิ่มประสิทธิภาพการวางแผนการบรรทุก** – โดยการรวมบัญชีการโหลดตามโซน
- **เพิ่มประสิทธิภาพการวางแผนเส้นทาง** – โดยการกำหนดแผนเส้นทางเฉพาะเป็นโซนเฉพาะ

คุณกำหนดโซนตามค่าฟิลด์ข้อมูลเมตา (เช่น ประเทศ ช่วงรหัสไปรษณีย์ หรือบริการผู้ขนส่ง) ที่มีคุณสมบัติตรงตามแต่ละโซน ไม่จำเป็นต้องใช้คำนิยามของโซนถ้าการกำหนดราคาการขนส่งของคุณไม่ใช้แนวคิดเกี่ยวกับโซน


[!INCLUDE[footer-include](../../includes/footer-banner.md)]