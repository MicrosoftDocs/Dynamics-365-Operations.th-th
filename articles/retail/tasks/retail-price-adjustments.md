---
title: " การปรับปรุงราคาในการขายปลีก"
description: 'ขั้นตอนนี้จะนำไปสู่การสร้างการปรับปรุงราคาขายปลีก '
author: josaw1
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: DefaultDashboard, RetailDiscountPricingWorkspace, RetailPeriodicDiscount, RetailDiscountPriceGroup
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 9427d3955e5442e301c416e2960e071ca5d85a3c
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 05/15/2019
ms.locfileid: "1550052"
---
# <a name="retail-price-adjustments"></a> การปรับปรุงราคาในการขายปลีก

[!include[task guide banner](../includes/task-guide-banner.md)]

ขั้นตอนนี้จะนำไปสู่การสร้างการปรับปรุงราคาขายปลีก  การปรับปรุงราคาขายปลีกสามารถตั้งค่าราคาขายของสินค้าโดยตรง หรือปรับเปลี่ยนราคาขายพื้นฐานหรือราคาขายตามข้อตกลงทางการค้าได้  ขั้นตอนนี้ใช้บริษัทข้อมูลสาธิต USRT

1. คลิกการจัดการการกำหนดราคาและส่วนลด
2. คลิกแท็บการปรับปรุงราคา
3. คลิก สร้าง
    * จากที่นี่ คุณสามารถสร้างกฎราคาและส่วนลดที่ใช้กันมากที่สุดได้ทั้งหมด รวมถึง ส่วนลดการขายปลีก การปรับปรุงราคา สมุดรายวันข้อตกลงทางการค้า และกฎการกำหนดราคาประเภท  
4. คลิกการปรับปรุงราคา
5. ในฟิลด์ชื่อ ให้พิมพ์ค่า 
6. ขยายส่วนรายการ
7. คลิก เพิ่ม
    * สำหรับตัวอย่างนี้ ป้อน '81126' ในฟิลด์ผลิตภัณฑ์     จากนั้น ป้อน '10.0' ในฟิลด์เปอร์เซ็นต์ส่วนลด  
    * การปรับปรุงราคาส่วนลดชนิดเปอร์เซ็นต์จะลดฐานราคาขายหรือราคาขายตามข้อตกลงทางการค้า  
8. คลิก เพิ่ม
    * สำหรับตัวอย่างนี้ ป้อน '81125' ในฟิลด์ผลิตภัณฑ์     จากนั้น เลือก 'ยอดส่วนลดเงินสด' ในฟิลด์วิธีการให้ส่วนลดนั้น     ในตอนท้าย ป้อน '5.0' ในฟิลด์ยอดส่วนลดเงินสด  
    * ชนิดส่วนลดแบบยอดส่วนลดเงินสดเป็นยอดเงินที่นำออกจากราคาฐานหรือราคาข้อตกลงทางการค้าแล้ว  
9. คลิกกลุ่มราคา
    * เลือก 'RP-Houston' ในฟิลด์กลุ่มราคา  
    * ซึ่งนี่จะเชื่อมโยงการปรับปรุงราคาไปยังร้านค้า Houston  
10. คลิก บันทึก
11. ปิดหน้า
12. ในฟิลด์สถานะ เลือก 'เปิดใช้งานแล้ว'
13. คลิก บันทึก
14. ปิดหน้า
15. รีเฟรชหน้า

