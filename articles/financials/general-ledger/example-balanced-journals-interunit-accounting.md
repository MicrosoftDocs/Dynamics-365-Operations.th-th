---
title: "สมุดรายวันสมดุลสำหรับการบัญชีระหว่างหน่วย"
description: "บทความนี้แสดงวิธีที่สมุดรายวันกำหนดยอดดุลโดยอัตโนมัติ เมื่อเลือกมิติทางการเงินยอดดุลในหน้าบัญชีแยกประเภท"
author: twheeloc
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: LedgerParameters
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 15791
ms.assetid: 301bd80e-f8b1-4f12-8194-e6d7de736084
ms.search.region: Global
ms.author: peakerbl
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: f45d180dc8dcafb0579e76b890dd5d516df5b8c0
ms.contentlocale: th-th
ms.lasthandoff: 09/29/2017

---

# <a name="balanced-journals-for-interunit-accounting"></a>สมุดรายวันสมดุลสำหรับการบัญชีระหว่างหน่วย

[!include[banner](../includes/banner.md)]


บทความนี้แสดงวิธีที่สมุดรายวันกำหนดยอดดุลโดยอัตโนมัติ เมื่อเลือกมิติทางการเงินยอดดุลในหน้าบัญชีแยกประเภท 

ถ้ารายการบัญชีไม่สมดุลในระดับของค่ามิติทางการเงิน รายการบัญชีเพิ่มเติมจะถูกสร้างขึ้นโดยอัตโนมัติในดุลสมุดรายวัน รายการบัญชีเหล่านี้ใช้ **ระหว่างหน่วย - เดบิต** และ**ระหว่างหน่วย - เครดิต** การลงชนิดรายการบัญชีในหน้า **สำหรับหน้าธุรกรรมอัตโนมัติ** เพื่อกำหนดบัญชีหลัก ตัวอย่างเช่น สาขา ซึ่งเป็นส่วนที่สองของบัญชีแยกประเภท ถูกเลือกเป็นมิติทางการเงินของยอดดุล และมีสร้างรายการบัญชีต่อไปนี้

|                      |           |
|----------------------|-----------|
| 6100 – MSP – OU\_256 | 100.00 DR |
| 6100 – NY – OU\_249  | 100.00 DR |
| 2100 – MSP – OU\_256 | 200.00 CR |

ในกรณีนี้ มีกำหนดยอดดุลต่อไปนี้:

-   สำหรับสาขา MSP = 100.00 CR
-   สำหรับสาขา NY = 100.00 DR

ดังนั้น รายการบัญชีต่อไปนี้จะสร้างขึ้นโดยอัตโนมัติ เพื่อให้รายการสมุดรายวันนี้สมดุลที่ระดับค่ามิติทางการเงิน

|                                   |           |
|-----------------------------------|-----------|
| (ระหว่างหน่วยเดบิต) – MSP – OU\_256 | 100.00 DR |
| (ระหว่างหน่วยเครดิต) – NY – OU\_249 | 100.00 CR |






