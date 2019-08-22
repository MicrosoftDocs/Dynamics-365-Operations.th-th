---
title: สร้างใบสั่งขายสำหรับผลิตภัณฑ์ที่จัดโครงแบบได้
description: 'กระบวนงานนี้แสดงวิธีการใช้เท็มเพลตการจัดโครงแบบผลิตภัณฑ์ในใบสั่งขาย '
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: DefaultDashboard, SalesOrderProcessingWorkspace, SalesCreateOrder, SalesTable, PCRuntimeConfigurator, PCTemplateConfigurationSelection
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 39ccb68ba76cd710412df6a46fc624608d02902b
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 08/01/2019
ms.locfileid: "1844548"
---
# <a name="create-a-sales-order-for-a-configurable-product"></a>สร้างใบสั่งขายสำหรับผลิตภัณฑ์ที่จัดโครงแบบได้

[!include [task guide banner](../../includes/task-guide-banner.md)]

กระบวนงานนี้แสดงวิธีการใช้เท็มเพลตการจัดโครงแบบผลิตภัณฑ์ในใบสั่งขาย  ตัวอย่างนี้ใช้แบบจำลองลำโพง D0006 ในบริษัทข้อมูลสาธิต USMF  โดยทั่วไป ตัวประมวลผลใบสั่งขายจะใช้กระบวนงานนี้


## <a name="create-a-sales-order"></a>สร้างใบสั่งขาย
1. คลิกที่การประมวลผลและการสอบถามใบสั่งขาย 
2. คลิก สร้าง
3. คลิกที่ใบสั่งขาย 
4. ในฟิลด์บัญชีลูกค้า เลือก US-001 
5. คลิก ตกลง
6. ในฟิลด์หมายเลขสินค้า ให้เลือก D0006
    * สำหรับงานนี้ คุณต้องเลือกผลิตภัณฑ์ที่จัดโครงแบบได้  
7. คลิกที่ผลิตภัณฑ์และการจัดหาวัสดุ
8. คลิกตั้งค่าคอนฟิกรายการ
    * โปรดทราบว่ามีการเปลี่ยนแปลงราคาตามการจัดโครงแบบที่เลือก และขณะนี้ฟิลด์รวมเคเบิลถูกตั้งค่าเป็น จริง  
    * สังเกตดูราคาและการตั้งค่าเริ่มต้นที่เลือกสำหรับเคเบิลดังกล่าว  
9. คลิกโหลดเท็มเพลต
    * ตัวอย่างนี้แสดงวิธีที่คุณสามารถใช้เท็มเพลตเพื่อเลือกการจัดโครงแบบที่กำหนดไว้ล่วงหน้า  ถ้าคุณกำลังใช้กระบวนงานนี้เป็นคู่มืองาน และต้องการดูค่าแอททริบิวต์อื่นๆ ที่มีอยู่ คุณจะต้องคลิกปุ่ม ปลดล็อค  
10. คลิก ตกลง
11. คลิก ตกลง
12. ขยายส่วน รายละเอียดของรายการ
13. คลิกแท็บผลิตภัณฑ์
    * ขณะนี้มีการแสดงรายการการจัดโครงแบบของสินค้าภายใต้มิติของผลิตภัณฑ์  
14. ปิดหน้า

## <a name="select-the-product-configuration"></a>เลือกการจัดโครงแบบผลิตภัณฑ์

