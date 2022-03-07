---
title: ตั้งค่าสภาพแวดล้อมการค้นหาข้อมูลหลัก
description: หัวข้อนี้อธิบายวิธีการตั้งค่าสภาพแวดล้อมของคุณเพื่อใช้ฟังก์ชันการค้นหาข้อมูลหลักของการคํานวณภาษี
author: kai-cloud
ms.date: 10/26/2021
ms.topic: article
ms.prod: ''
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
ms.openlocfilehash: 901f8bcb0220355866952b68e92bc2dd906bb430
ms.sourcegitcommit: 2113678369f47944f8725ca656f461fa159f87f6
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 10/27/2021
ms.locfileid: "7700415"
---
# <a name="set-up-an-environment-for-master-data-lookup"></a>ตั้งค่าสภาพแวดล้อมการค้นหาข้อมูลหลัก

[!include [banner](../includes/banner.md)]

หัวข้อนี้อธิบายวิธีการตั้งค่าสภาพแวดล้อมของคุณเพื่อใช้ฟังก์ชันการค้นหาข้อมูลหลักของการคํานวณภาษี

1. ตั้งค่าการรวม Microsoft Power Platform ใน Microsoft Dynamics Lifecycle Services (LCS) สำหรับข้อมูลเพิ่มเติม ให้ดูที่ [การรวม Microsoft Power Platform - ภาพรวม Add-in](../../fin-ops-core/dev-itpro/power-platform/add-ins-overview.md) หลังจากที่คุณขั้นตอนนี้เสร็จสมบูรณ์แล้ว ชื่อของสภาพแวดล้อม Microsoft Power Platform จะปรากฏในส่วน **การรวม Power Platform**
2. ไปที่ [ศูนย์การจัดการ Microsoft Power Platform](https://admin.powerplatform.microsoft.com/environments) และเลือกชื่อสภาพแวดล้อม มีการระบุ URL ของสภาพแวดล้อม
3. ตั้งค่า Dynamics 365 Finance และ Dataverse สำหรับข้อมูลเพิ่มเติม โปรดดูที่ [การรับโซลูชันเอนทิตีเสมือน](../../fin-ops-core/dev-itpro/power-platform/admin-reference.md#get-virtual-entity-solution) และ [การรับรองความถูกต้องและการตรวจสอบความถูกต้อง](../../fin-ops-core/dev-itpro/power-platform/admin-reference.md#authentication-and-authorization)
4. ตั้งค่าเอนทิตีต่อไปนี้ สำหรับข้อมูลเพิ่มเติม ให้ดู [เปิดใช้งานเอนทิตีเสมือน Microsoft Dataverse](../../fin-ops-core/dev-itpro/power-platform/enable-virtual-entities.md)

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

5. ตั้งค่า Regulatory Configuration Service (RCS) เปิดพื้นที่ทำงาน **การจัดการคุณลักษณะ** และเปิดใช้งานคุณลักษณะต่อไปนี้

    - การสนับสนุนแหล่งข้อมูล Dataverse การรายงานทางอิเล็กทรอนิกส์
    - การสนับสนุนแหล่งข้อมูล Dataverse สำหรับบริการด้านภาษี
    - คุณลักษณะที่ใช้ทั่วโลก

6. เข้าสู่ระบบ RCS โดยใช้บัญชีผู้ดูแลระบบของผู้เช่า
7. ไปที่ **การรายงานทางอิเล็กทรอนิกส์** > **โปรแกรมประยุกต์ที่เชื่อมต่อ** 
8. เลือก **สร้าง** เพื่อเพิ่มเรกคอร์ด และป้อนข้อมูลฟิลด์ต่อไปนี้ 

    - ในฟิลด์ **ชื่อ** ป้อนชื่อ
    - ในฟิลด์ **ชนิด** เลือก **Dataverse**
    - ในฟิลด์ **โปรแกรมประยุกต์** ให้ป้อน URL ของ Dataverse ของคุณ
    - ในฟิลด์ **ผู้เช่า** ป้อนผู้เช่าของคุณ
    - ในฟิลด์ **URL แบบกำหนดเอง** ให้ป้อน URL Dataverse ของคุณและผนวก URL ด้วย "/api/ข้อมูล/v9.1"

9. เลือก **ตรวจสอบการเชื่อมต่อ** และเสร็จสิ้นกระบวนการเชื่อมต่อ 

    [![ปุ่มตรวจสอบการเชื่อมต่อ](./media/tax-service-setup-environment-for-mater-date-pic1.png)](./media/tax-service-setup-environment-for-mater-date-pic1.png)

10. ไปที่ **การรายงานทางอิเล็กทรอนิกส์** > **การตั้งค่าคอนฟิกภาษี** และนําเข้าการตั้งค่าคอนฟิกภาษีจาก [การตั้งค่าคอนฟิกภาษี](https://go.microsoft.com/fwlink/?linkid=2158352)

    [![หน้าการตั้งค่าคอนฟิกภาษี, แผนภูมิรูปแบบข้อมูลภาษี](./media/tax-service-setup-environment-for-mater-date-pic2.png)](./media/tax-service-setup-environment-for-mater-date-pic2.png)

11. ไปที่ **การแม็ปแบบจำลองเอกสารต้องเสียภาษี** หรือ **การแม็ปแบบจำลอง Dataverse** ถ้าคุณใช้การตั้งค่าคอนฟิก Microsoft และในฟิลด์ **โปรแกรมประยุกต์ที่เชื่อมต่อ** ให้เลือกเรกคอร์ดที่คุณสร้างไว้ในขั้นตอนที่ 7
12. ตั้งค่า **ค่าเริ่มต้นสำหรับการแม็ปแบบจำลอง** เป็น **ใช่**

    [![หน้าการแม็ปแบบจำลอง](./media/tax-service-setup-environment-for-mater-date-pic3.png)](./media/tax-service-setup-environment-for-mater-date-pic3.png)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
