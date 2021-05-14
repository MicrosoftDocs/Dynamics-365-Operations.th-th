---
title: ตั้งค่าสภาพแวดล้อมการค้นหาข้อมูลหลัก
description: หัวข้อนี้อธิบายวิธีการตั้งค่าสภาพแวดล้อมของคุณเพื่อใช้ฟังก์ชันการค้นหาข้อมูลหลักของการคํานวณภาษี
author: kai-cloud
ms.date: 04/21/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application user
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: ''
ms.search.region: Global
ms.author: pashao
ms.search.validFrom: 2021-04-01
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: 9f9b385df1db60b27698d90281c43fabb574af49
ms.sourcegitcommit: 5f5afb46431e1abd8fb6e92e0189914b598dc7fd
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 04/21/2021
ms.locfileid: "5924165"
---
# <a name="set-up-an-environment-for-master-data-lookup"></a>ตั้งค่าสภาพแวดล้อมการค้นหาข้อมูลหลัก

[!include [banner](../includes/banner.md)]

หัวข้อนี้อธิบายวิธีการตั้งค่าสภาพแวดล้อมของคุณเพื่อใช้ฟังก์ชันการค้นหาข้อมูลหลักของการคํานวณภาษี

1. ตั้งค่าการรวม Power Platform ใน Lifecycle Services (LCS) สำหรับข้อมูลเพิ่มเติม ให้ดูที่ [การรวม Microsoft Power Platform - ภาพรวม Add-in](../../fin-ops-core/dev-itpro/power-platform/add-ins-overview.md)
2. ตั้งค่า Dynamics 365 Finance และ Microsoft Dataverse สำหรับข้อมูลเพิ่มเติม โปรดดูที่ [การรับโซลูชัน](../../fin-ops-core/dev-itpro/power-platform/admin-reference.md#getting-the-solution) และ [การรับรองความถูกต้องและการตรวจสอบความถูกต้อง](../../fin-ops-core/dev-itpro/power-platform/admin-reference.md#authentication-and-authorization)
3. ตั้งค่าเอนทิตีต่อไปนี้ สำหรับข้อมูลเพิ่มเติม ให้ดู [เปิดใช้งานเอนทิตีเสมือน](../../fin-ops-core/dev-itpro/power-platform/admin-reference.md#enabling-virtual-entities)
      - CompanyInfoEntity
      - CurrencyEntity
      - CustCustomerV3Entity
      - DeliveryTermsEntity
      - EcoResProductCategoryEntity
      - EcoResReleasedProductV2Entity
      - LogisticsAddressTarEntity
      - LogisticsAddressCountryRegionTranslationEntity
      - LogisticsAddressStateEntity
      - PurchProcurementChargeCDSEntity
      - SalesChargeCDSEntity
      - TaxGroupEntity
      - TaxItemGroupHeadingEntity
      - VendVendorV2Entity
4. ตั้งค่า Dynamics 365 Regulatory Configuration Service (RCS) 
5. สร้างคำขอบริการเพื่อให้ Microsoft สามารถเปิดใช้งานเที่ยวบินของคุณลักษณะต่อไปนี้:

      - ERCdsFeature
      - TaxServiceCDSFeature

6. ไปที่พื้นที่ทำงาน **การจัดการคุณลักษณะ** และเปิดใช้งานคุณลักษณะต่อไปนี้

      - (การแสดงตัวอย่าง) การสนับสนุนแหล่งข้อมูล Dataverse การรายงานทางอิเล็กทรอนิกส์
      - (พรีวิว) การสนับสนุนแหล่งข้อมูล Dataverse สำหรับบริการด้านภาษี
      - (การแสดงตัวอย่าง) คุณลักษณะที่ใช้ทั่วโลก

5. เข้าสู่ระบบ RCS โดยใช้บัญชีผู้ดูแลระบบของผู้เช่า
6. ไปที่ **การรายงานทางอิเล็กทรอนิกส์** > **โปรแกรมประยุกต์ที่เชื่อมต่อ** 
7. เลือก **สร้าง** เพื่อเพิ่มเรกคอร์ด และป้อนข้อมูลฟิลด์ต่อไปนี้ 

   - ในฟิลด์ **ชื่อ** ป้อนชื่อ
   - ในฟิลด์ **ชนิด** เลือก **Dataverse**
   - ในฟิลด์ **โปรแกรมประยุกต์** ให้ป้อน URL ของ Dataverse ของคุณ
   - ในฟิลด์ **ผู้เช่า** ป้อนผู้เช่าของคุณ
   - ในฟิลด์ **URL แบบกำหนดเอง** ให้ป้อน URL Dataverse ของคุณและผนวก URL ด้วย "/api/ข้อมูล/v9.1"

8. เลือก **ตรวจสอบการเชื่อมต่อ** และเสร็จสิ้นกระบวนการเชื่อมต่อ 

   [![ตรวจสอบปุ่มการเชื่อมต่อ](./media/tax-service-setup-environment-for-mater-date-pic1.png)](./media/tax-service-setup-environment-for-mater-date-pic1.png)

9. ไปที่ **การรายงานทางอิเล็กทรอนิกส์** > **การตั้งค่าคอนฟิกภาษี** และนําเข้าการตั้งค่าคอนฟิกภาษีจาก [การตั้งค่าคอนฟิกภาษี](https://go.microsoft.com/fwlink/?linkid=2158352)

   [![หน้าการตั้งค่าคอนฟิกภาษี แผนภูมิรูปแบบข้อมูลภาษี](./media/tax-service-setup-environment-for-mater-date-pic2.png)](./media/tax-service-setup-environment-for-mater-date-pic2.png)

10. ไปที่ **การแม็ปแบบจำลองเอกสารต้องเสียภาษี** หรือ **การแม็ปแบบจำลอง Dataverse** ถ้าคุณใช้การตั้งค่าคอนฟิก Microsoft และในฟิลด์ **โปรแกรมประยุกต์ที่เชื่อมต่อ** ให้เลือกเรกคอร์ดที่คุณสร้างไว้ในขั้นตอนที่ 7
11. ตั้งค่า **ค่าเริ่มต้นสำหรับการแม็ปแบบจำลอง** เป็น **ใช่**

   [![หน้าการแม็ปแบบจำลอง](./media/tax-service-setup-environment-for-mater-date-pic3.png)](./media/tax-service-setup-environment-for-mater-date-pic3.png)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
