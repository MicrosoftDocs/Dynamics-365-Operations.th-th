---
title: ลงทะเบียนการเช็คอินและเช็คเอาท์ของพนักงานขนส่งสำหรับการนัดหมาย
description: 'กระบวนงานนี้แสดงวิธีการลงทะเบียนการเช็คอินและการเช็คเอาท์ของพนักงานขนส่ง '
author: ShylaThompson
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TMSDriverLogListPage, TMSDriverCheckIn
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 2baa5e6bce3fa16199e97bf87ea03fa9a55a681a
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 04/02/2020
ms.locfileid: "3206161"
---
# <a name="register-driver-check-in-and-check-out-for-an-appointment"></a>ลงทะเบียนการเช็คอินและเช็คเอาท์ของพนักงานขนส่งสำหรับการนัดหมาย

[!include [banner](../../includes/banner.md)]

กระบวนงานนี้แสดงวิธีการลงทะเบียนการเช็คอินและการเช็คเอาท์ของพนักงานขนส่ง ซึ่งปกติจะดำเนินการโดยผู้ประสานงานการขนส่ง คุณสามารถใช้กระบวนงานนี้ในบริษัทข้อมูลสาธิต USMF ก่อนจะเริ่ม ต้องมีการตั้งค่าการนัดหมายที่ตั้งค่าสำหรับโหลดเสียก่อน เมื่อต้องการสร้างการนัดหมาย คุณสามารถรันกระบวนงาน "กำหนดการนัดหมายสำหรับจำนวนงานในศูนย์การผลิต" เป็นข้อกำหนดเบื้องต้น


## <a name="select-an-appointment"></a>เลือกการนัดหมาย
1. ไปที่ การจัดการการขนส่ง > การวางแผน > การจัดกำหนดการนัดหมายที่ท่าสินค้า > การเช็คอินและเช็คเอาท์ของพนักงานขนส่ง
2. เลือกการนัดหมาย

## <a name="register-driver-check-in"></a>ลงทะเบียนการเช็คอินของพนักงานขนส่ง
1. คลิก การเช็คอินของพนักงานขนส่ง
2. ในฟิลด์หมายเลขปิดท้าย ให้พิมพ์ค่า
3. ในฟิลด์ชื่อพนักงานขนส่ง ให้พิมพ์ค่า
4. ในฟิลด์ใบอนุญาตพนักงานขนส่ง ให้พิมพ์ค่า
5. คลิก ตกลง

## <a name="register-driver-check-out"></a>ลงทะเบียนการเช็คเอาท์ของพนักงานขนส่ง
1. คลิก การเช็คเอาท์ของพนักงานขนส่ง
2. คลิก ตกลง

