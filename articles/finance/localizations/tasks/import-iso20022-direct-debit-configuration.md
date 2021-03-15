---
title: นำเข้าการตั้งค่าคอนฟิกการหักบัญชีเงินฝากอัตโนมัติ ISO20022
description: 'กระบวนงานนี้อธิบายวิธีการนำเข้าการตั้งค่าคอนฟิกการรายงานทางอิเล็กทรอนิกส์การชำระเงินของลูกค้า '
author: mrolecki
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ERWorkspace, ERVendorPart, ERSolutionRepositoryTable, ERSolutionImport
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: mrolecki
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: d68e5a63ea3b037cc111d6732857f0aae1ce7e5d
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 01/15/2021
ms.locfileid: "4989966"
---
# <a name="import-iso20022-direct-debit-configuration"></a>นำเข้าการตั้งค่าคอนฟิกการหักบัญชีเงินฝากอัตโนมัติ ISO20022

[!include [banner](../../includes/banner.md)]

กระบวนงานนี้อธิบายวิธีการนำเข้าการตั้งค่าคอนฟิกการรายงานทางอิเล็กทรอนิกส์การชำระเงินของลูกค้า  กระบวนงานนี้ใช้รูปแบบการหักบัญชีเงินฝากอัตโนมัติ ISO 20022 เป็นตัวอย่าง 



กระบวนงานนี้ถูกสร้างขึ้นโดยใช้บริษัทข้อมูลสาธิต DEMF แต่คุณสามารถใช้บริษัทข้อมูลสาธิตใดก็ได้สำหรับวัตถุประสงค์นี้



นี่คือกระบวนงานแรกจากกระบวนงานห้ารายการที่แสดงให้เห็นถึงขั้นตอนการชำระเงินโดยใช้การตั้งค่าคอนฟิกการรายงานทางอิเล็กทรอนิกส์

1. ไปที่การจัดการองค์กร > พื้นที่ทำงาน > การรายงานทางอิเล็กทรอนิกส์
2. ในรายการผู้ให้บริการการตั้งค่าคอนฟิกที่พร้อมใช้งาน เลือก Microsoft
3. คลิก กำหนดเป็นใช้งานอยู่
4. คลิก ที่เก็บ
5. คลิก เปิด
6. คลิกแสดงตัวกรอง
7. ใช้ตัวกรองต่อไปนี้: ป้อนค่าตัวกรอง "การหักบัญชีเงินฝากอัตโนมัติ ISO20022 (DE)" ในฟิลด์ "ชื่อการตั้งค่าคอนฟิก" โดยใช้ตัวดำเนินการตัวกรอง "เริ่มต้นด้วย"
    * อีกทางหนึ่งคือ คุณสามารถหาการตั้งค่าคอนฟิกในรายการ เลือก และข้ามขั้นตอนนี้  
8. คลิก นำเข้า
    * ถ้าปุ่มการนำเข้าไม่พร้อมใช้งาน หมายความว่าการตั้งค่าคอนฟิกนี้ถูกนำเข้าเรียบร้อยแล้ว  
9. คลิก ใช่



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]