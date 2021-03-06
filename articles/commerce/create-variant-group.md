---
title: การสร้างกลุ่มตัวแปร
description: หัวข้อนี้อธิบายวิธีสร้างกลุ่มตัวแปรขนาด ลักษณะ หรือสีของผลิตภัณฑ์ใน Microsoft Dynamics 365 Commerce
author: samjarawan
manager: annbe
ms.date: 01/27/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: RetailSizeGroupTable, ConfigGroupIdLookup, RetailStyleGroupTable
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: samjar
ms.search.validFrom: 2020-01-20
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: e19d9a2549fa9957126592f3db7e468147997261
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 01/15/2021
ms.locfileid: "4965164"
---
# <a name="create-a-variant-group"></a>การสร้างกลุ่มตัวแปร


[!include [banner](includes/banner.md)]

หัวข้อนี้อธิบายวิธีสร้างกลุ่มตัวแปรขนาด ลักษณะ หรือสีของผลิตภัณฑ์ใน Microsoft Dynamics 365 Commerce

## <a name="overview"></a>ภาพรวม

Dynamics 365 Commerce รองรับตัวแปรต่าง ๆ สำหรับผลิตภัณฑ์ เหมาะที่จะตั้งค่ากลุ่มตัวแปรสำหรับประเภทผลิตภัณฑ์ที่แตกต่างกัน ตัวอย่างเช่น สามารถสร้างกลุ่มขนาดสำหรับเสื้อยืดที่มีขนาดเล็กพิเศษ เล็ก กลาง ใหญ่ และใหญ่พิเศษ หรือสามารถสร้างกลุ่มสีเพื่อรวมสีที่มีทั้งหมดของผลิตภัณฑ์ ควรเพิ่มกลุ่มตัวแปรก่อนที่จะเพิ่มผลิตภัณฑ์

ในหัวข้อนี้ กลุ่มขนาดจะถูกสร้างขึ้นและกำหนดค่า กระบวนการที่คล้ายกันสามารถใช้สำหรับการเพิ่มและกำหนดค่ากลุ่มลักษณะและกลุ่มสี

## <a name="create-a-size-group"></a>การสร้างกลุ่มขนาด

ทำตามขั้นตอนเหล่านี้เพื่อสร้างกลุ่มขนาด
 
1. ในบานหน้าต่างนำทาง ไปที่ **โมดูล \> การขายปลีกและการค้า \> ผลิตภัณฑ์และประเภท \> กลุ่มตัวแปร \> กลุ่มขนาด**
1. บนหน้าต่างการดำเนินการ เลือก **สร้าง**
1. ในกล่อง **กลุ่มขนาด** ป้อนชื่อสำหรับกลุ่มขนาด
1. ในกล่อง **คำอธิบาย** ป้อนคำอธิบายที่เหมาะสมลงไป
1. บนบานหน้าต่างการดำเนินการ เลือก **บันทึก**

## <a name="add-attributes-to-the-size-group"></a>เพิ่มแอตทริบิวต์ในกลุ่มขนาด

เมื่อต้องการเพิ่มแอตทริบิวต์ไปยังกลุ่มขนาด ให้ทำตามขั้นตอนเหล่านี้

1. ในบานหน้าต่างนำทาง ไปที่ **โมดูล \> การขายปลีกและการค้า \> ผลิตภัณฑ์และประเภท \> กลุ่มตัวแปร \> กลุ่มขนาด**
1. ในบานหน้าต่างนำทาง ให้เลือกกลุ่มขนาด
1. ใต้ **บรรทัดกลุ่มขนาด** เลือก **เพิ่ม**
1. ในกล่อง **ขนาด** ป้อนสตริงที่แทนขนาด (ตัวอย่างเช่น "XL")
1. ในกล่อง **ชื่อขนาด** ป้อนชื่อสำหรับขนาด (ตัวอย่างเช่น "ใหญ่พิเศษ")
1. ในกล่อง **การเติมเต็มน้ำหนัก** ให้ป้อนตัวเลขที่แสดงถึงน้ำหนักการเติมเต็ม
1. ในกล่อง **หมายเลขในบาร์โค้ด** ให้ป้อนตัวเลขที่แสดงถึงบาร์โค้ด
1. ในกล่อง **ลำดับการแสดงผล** ให้ป้อนหมายเลขที่แทนลำดับการแสดงผล
1. เมื่อเพิ่มขนาดเสร็จแล้ว ให้เลือก **บันทึก** บนบานหน้าต่างการดำเนินการ

ภาพต่อไปนี้แสดงตัวอย่างของกลุ่มขนาดสำหรับ "ขนาดเสื้อเชิ้ตลำลอง"

![การสร้างกลุ่มขนาด](media/create-variant-group.png)

## <a name="additional-resources"></a>แหล่งข้อมูลเพิ่มเติม

[ภาพรวมของข้อมูลผลิตภัณฑ์](../supply-chain/pim/product-information.md?toc=/dynamics365/commerce/toc.json)

[ตั้งค่าผลิตภัณฑ์ขายปลีก](set-up-retail-products.md)

[มิติของผลิตภัณฑ์](../supply-chain/pim/product-dimensions.md?toc=/dynamics365/commerce/toc.json)
