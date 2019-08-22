---
title: นำเข้าการตั้งค่าคอนฟิกการโอนย้ายเครดิต ISO20022
description: 'กระบวนงานนี้แสดงวิธีการนำเข้าการตั้งค่าคอนฟิกการรายงานทางอิเล็กทรอนิกส์การชำระเงินของผู้จัดจำหน่าย '
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
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mrolecki
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: ee7e69611d31d2577ebafdfc059b0936aef0520b
ms.sourcegitcommit: 16bfa0fd08feec1647829630401ce62ce2ffa1a4
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 08/02/2019
ms.locfileid: "1848802"
---
# <a name="import-iso20022-credit-transfer-configuration"></a>นำเข้าการตั้งค่าคอนฟิกการโอนย้ายเครดิต ISO20022

[!include [task guide banner](../../includes/task-guide-banner.md)]

กระบวนงานนี้แสดงวิธีการนำเข้าการตั้งค่าคอนฟิกการรายงานทางอิเล็กทรอนิกส์การชำระเงินของผู้จัดจำหน่าย  รูปแบบการโอนย้ายเครดิต ISO 20022 ของเยอรมันถูกใช้เป็นตัวอย่าง สามารถใช้กระบวนงานนี้สำหรับรูปแบบการรายงานทางอิเล็กทรอนิกส์อื่นๆ ที่พร้อมใช้งาน 

งานนี้ถูกสร้างขึ้นโดยใช้บริษัทข้อมูลสาธิต DEMF แต่คุณสามารถใช้บริษัทข้อมูลสาธิตใดก็ได้เพื่อทำให้งานนี้เสร็จสมบูรณ์

นี่คืองานแรกจากงานห้ารายการ ที่จะอธิบายกระบวนการชำระเงินของผู้จัดจำหน่ายโดยใช้การตั้งค่าคอนฟิกการรายงานทางอิเล็กทรอนิกส์ กระบวนงานนี้ใช้สำหรับคุณลักษณะทั้ที่ถูกเพิ่มลงใน Dynamics 365 for Operations รุ่น 1611

1. ไปที่การจัดการองค์กร > พื้นที่ทำงาน > การรายงานทางอิเล็กทรอนิกส์
2. ในรายการผู้ให้บริการการตั้งค่าคอนฟิกที่พร้อมใช้งาน เลือก Microsoft
3. คลิก กำหนดเป็นใช้งานอยู่
4. คลิก ที่เก็บ
5. คลิก เปิด
6. คลิกแสดงตัวกรอง
7. ใช้ตัวกรองต่อไปนี้: ป้อนค่าตัวกรอง "การโอนย้ายเครดิต ISO20022 (DE)" ในฟิลด์ "ชื่อการตั้งค่าคอนฟิก" โดยใช้ตัวดำเนินการตัวกรอง "เริ่มต้นด้วย"
    * อีกทางหนึ่งคือ คุณสามารถค้นหาการตั้งค่าคอนฟิกในรายการ เลือก และย้ายไปยังงานนำเข้า  
8. คลิก นำเข้า
    * ถ้าปุ่มการนำเข้าไม่พร้อมใช้งาน หมายความว่าการตั้งค่าคอนฟิกนี้ถูกนำเข้าเรียบร้อยแล้ว  
9. คลิก ใช่

