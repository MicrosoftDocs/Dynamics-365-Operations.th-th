---
title: คุณลักษณะที่เอาออกหรือเลิกสนับสนุนใน Dynamics 365 Commerce
description: หัวข้อนี้อธิบายคุณลักษณะที่ถูกลบออก หรือที่ถูกวางแผนไว้สำหรับการลบจาก Dynamics 365 Commerce
author: josaw
manager: AnnBe
ms.date: 05/04/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.author: josaw
ms.search.validFrom: 2020-04-30
ms.dyn365.ops.version: Platform update 33
ms.openlocfilehash: c47c5430a8f5d67e13c95db609a95d5ad66933ae
ms.sourcegitcommit: a8b6cd799eddaf5be9aec9ea3c2b55e2c3231652
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 05/05/2020
ms.locfileid: "3335287"
---
# <a name="removed-or-deprecated-features-in-dynamics-365-commerce"></a>คุณลักษณะที่เอาออกหรือเลิกสนับสนุนใน Dynamics 365 Commerce

[!include [banner](../includes/banner.md)]

หัวข้อนี้อธิบายคุณลักษณะที่ถูกลบออก หรือที่ถูกวางแผนไว้สำหรับการลบจาก Dynamics 365 Commerce

- คุณลักษณะที่ *ถูกลบ* จะไม่พร้อมใช้งานในผลิตภัณฑ์อีกต่อไป
- คุณลักษณะที่ *ถูกยกเลิกการใช้* ไม่ได้อยู่ในการพัฒนาที่ใช้งานอยู่ และอาจถูกลบออกในการปรับปรุงในอนาคต

รายการนี้มีไว้เพื่อช่วยคุณพิจารณาการลบออกและการยกเลิกการใช้งานเหล่านี้สำหรับการวางแผนของคุณเอง 

> [!NOTE]
> ข้อมูลโดยละเอียดเกี่ยวกับออบเจ็กต์ต่างๆ ในแอป Finance and Operations พบได้ใน [รายงานอ้างอิงทางเทคนิค](https://mbs.microsoft.com/customersource/northamerica/AX/downloads/reports/axtechrefrep) คุณสามารถเปรียบเทียบเวอร์ชันต่างๆ ของรายงานเหล่านี้ เพื่อเรียนรู้เกี่ยวกับออบเจ็กต์ที่เปลี่ยนแปลงหรือถูกลบออกในแต่ละรุ่นของแอป Finance and Operations

## <a name="features-removed-or-deprecated-in-the-commerce-10010-release"></a>คุณลักษณะที่เอาออกหรือที่เลิกสนับสนุนในการนำออกใช้ Commerce 10.0.10
### <a name="pos-operation-803---picking-and-receiving"></a>การดำเนินการ POS 803 - การเบิกสินค้าและการรับสินค้า
|   |  |
|------------|--------------------|
| **เหตุผลสำหรับการยกเลิกการใช้/การลบ** | การดำเนินการเบิกสินค้าและการรับสินค้าจะถูกยกเลิกการใช้งานเนื่องจากการออกแบบการดำเนินงานใหม่ |
| **แทนที่ด้วยลักษณะการทำงานอื่นหรือไม่**   | ใช่ จะถูกแทนที่ด้วยสองการดำเนินงาน POS ใหม่: การดำเนินงานขาเข้า (804) และการดำเนินงานขาออก (805)|
| **พื้นที่ของผลิตภัณฑ์ที่ได้รับผล**         | ใบสมัครสำหรับการขายหน้าร้าน (POS) |
| **ตัวเลือกการปรับใช้**              | ทั้งหมด |
| **สถานะ**                         | ไม่สนับสนุน: เมื่อนำรุ่น 10.0.10 ออกใช้ การดำเนินการเบิกสินค้าและการรับสินค้าจะไม่ได้รับการอัพเดทใดๆ ใหม่อีกต่อไป การแก้ไขข้อผิดพลาดที่สำคัญเท่านั้นที่จะดำเนินการสำหรับการดำเนินงานนี้ในรุ่นต่อๆ ไป ลูกค้าทั้งหมดจะได้รับการสนับสนุนให้ย้ายไปที่ [การดำเนินงานขาเข้าใหม่](https://docs.microsoft.com/dynamics365/commerce/pos-inbound-inventory-operation) และ [การดำเนินงานขาออก](https://docs.microsoft.com/dynamics365/commerce/pos-outbound-inventory-operation) ซึ่งจะยังคงเป็นส่วนหนึ่งของแผนงานผลิตภัณฑ์ระยะยาวของเรา |


## <a name="features-removed-or-deprecated-in-the-commerce-1007-release"></a>คุณลักษณะที่เอาออกหรือที่เลิกสนับสนุนในการนำออกใช้ Commerce 10.0.7
### <a name="commerce-getproductavailabilities-and-getavailableinventorynearby-apis"></a>API ของ Commerce GetProductAvailabilities และ GetAvailableInventoryNearby
|   |  |
|------------|--------------------|
| **เหตุผลสำหรับการยกเลิกการใช้/การลบ** | API ที่ปรับให้เหมาะสมใหม่ถูกสร้างเพื่อแทนที่ API ของ GetProductAvailabilities และ GetAvailableInventoryNearby |
| **แทนที่ด้วยลักษณะการทำงานอื่นหรือไม่**   | ใช่: ถูกแทนที่ด้วย API ของ GetEstimatedAvailability และ GetEstimatedProductWarehouseAvailability |
| **พื้นที่ของผลิตภัณฑ์ที่ได้รับผล**         | SDK แอปพลิเคชันอีคอมเมิร์ซ |
| **ตัวเลือกการปรับใช้**              | ทั้งหมด |
| **สถานะ**                         | ไม่ได้รับการสนับสนุน: รุ่น 10.0.7 ที่นำออกใช้จะไม่มีการลงทุนทางวิศวกรรมที่ทำสำหรับ GetProductAvailabilities และ GetAvailableInventoryNearby องค์กรที่ใช้ API เหล่านี้ในการปรับใช้อีคอมเมิร์ซของตนควรแปลงเป็น API ของ GetEstimatedAvailability และ GetEstimatedProductWarehouseAvailability ใหม่ และเปิดใช้งาน [คุณลักษณะการทำงานการคำนวณความพร้อมใช้งานของผลิตภัณฑ์ที่เหมาะสม](https://docs.microsoft.com/dynamics365/commerce/calculated-inventory-retail-channels)  |

## <a name="previous-announcements-about-removed-or-deprecated-features"></a>ประกาศก่อนหน้านี้เกี่ยวกับคุณลักษณะที่ถูกลบหรือเลิกสนับสนุน
เมื่อต้องการเรียนรู้เพิ่มเติมเกี่ยวกับคุณลักษณะที่ถูกลบออกหรือเลิกสนับสนุนในรุ่นก่อนหน้านี้ ให้ดูที่ [คุณลักษณะที่ถูกลบออกหรือเลิกสนับสนุนในรุ่นก่อนหน้านี้](../../fin-ops-core/dev-itpro/migration-upgrade/deprecated-features.md?toc=/dynamics365/commerce/toc.json)
