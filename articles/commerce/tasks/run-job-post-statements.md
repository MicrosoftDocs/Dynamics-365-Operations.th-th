---
title: ตั้งค่าคอนฟิก และดำเนินงานเพื่อการคำนวณใบแจ้งยอด
description: 'กระบวนการนี้นำไปสู่การตั้งค่าคอนฟิกและการรันงานในชุดงานที่เกิดซ้ำ เพื่อการคำนวณใบแจ้งยอดสำหรับร้านค้าหรือกลุ่มของร้านค้าที่เลือก '
author: josaw1
manager: AnnBe
ms.date: 07/29/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: RetailChannelOperationsWorkspace, RetailOperatingUnitPicker, SysRecurrence
audience: Application User
ms.reviewer: josaw
ms.search.region: Global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: bed4cfb4875231d11ad76e4403c7995519d56e73
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 01/15/2021
ms.locfileid: "5003689"
---
# <a name="configure-and-run-job-to-post-statements"></a>ตั้งค่าคอนฟิก และดำเนินงานเพื่อการคำนวณใบแจ้งยอด

[!include [banner](../includes/banner.md)]

กระบวนการนี้นำไปสู่การตั้งค่าคอนฟิกและการรันงานในชุดงานที่เกิดซ้ำ เพื่อการคำนวณใบแจ้งยอดสำหรับร้านค้าหรือกลุ่มของร้านค้าที่เลือก  กระบวนงานนี้ใช้บริษัท USRT ในข้อมูลสาธิต

1. ไปที่ พื้นที่ทำงานทั้งหมด > .. > การเงินของร้านค้า
2. คลิกลงรายการบัญชีใบแจ้งยอดในชุดงาน
    * เลือกลำดับชั้นขององค์กร จากนั้นเลือกร้านค้าแต่ละรายหรือโหนดในแผนภูมิโหนดองค์กร เลือกโหนด  ถ้าคุณต้องการสร้างชุดงานสำหรับกลุ่มร้านค้า  
    * คลิกลูกศรเพื่อเพิ่มสิ่งที่คุณเลือก   
3. คลิกที่แท็บดำเนินการในเบื้องหลัง ![ดำเนินการในเบื้องหลังรันในเบื้องหลัง](../dev-itpro/media/runbackground.png "รันในแบบเบื้องหลัง") 
4. เลือกหรือไม่เลือกกล่องกาเครื่องหมายการประมวลผลชุดงาน
![การประมวลผลชุดงาน](../dev-itpro/media/batchprocessing.png "ชุดงานการประมวณผล & การเกิดซ้ำ ") 
5. คลิกการเกิดซ้ำ
6. ในฟิลด์วันที่เริ่มต้น ให้ป้อนวันที่
7. ในฟิลด์เวลาเริ่มต้น ให้ป้อนเวลา 
    * เลือกว่าคุณต้องการหยุดการเกิดซ้ำหลังจากการรันได้จำนวนหนึ่ง, ณ วันหนึ่ง, หรือไม่  จากนั้นเลือกตัวเลือกต่างๆ เพื่อกำหนดความถี่ที่คุณต้องการรันงาน  
8. คลิก ตกลง 
9. คลิก ตกลง 

