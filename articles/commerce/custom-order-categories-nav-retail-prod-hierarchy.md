---
title: เปลี่ยนลำดับการจัดเรียงสำหรับการจัดซื้อสินค้าเอนทิตี้
description: หัวข้อนี้อธิบายแนวคิดที่เกี่ยวข้องกับการควบคุมลำดับการแสดงผลสำหรับการจัดซื้อสินค้าที่เกี่ยวข้องกับเอนทิตี้อื่นๆใน Dynamics 365 Commerce
author: josaw1
manager: AnnBe
ms.date: 08/05/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: Category, Retail product hierarchy, Navigation hierarchy
audience: Application User, Merchandising manager, Catalog manager
ms.reviewer: josaw
ms.custom: 268444
ms.search.region: global
ms.search.industry: Retail
ms.author: rubendel
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 694f95e274dc068cba02a2a519c1ce3ed186eaf0
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 01/15/2021
ms.locfileid: "4976774"
---
# <a name="change-the-sort-order-for-merchandising-entities"></a>เปลี่ยนลำดับการจัดเรียงสำหรับการจัดซื้อสินค้าเอนทิตี้


[!include [banner](includes/banner.md)]

ผู้ค้าปลีกพิจารณาการค้นพบผลิตภัณฑ์เป็นเครื่องมือหลักสำหรับการโต้ตอบกับลูกค้าในทุกช่องทาง ฟังก์ชันต่างๆสามารถช่วยลูกค้าในการค้นหาผลิตภัณฑ์ได้อย่างง่ายดาย ตัวอย่างเช่น ลูกค้าสามารถเรียกดูประเภท การค้นหา เเละตัวกรองข้อมูลได้

หัวข้อนี้อธิบายแนวคิดที่เกี่ยวข้องกับการควบคุมลำดับการแสดงผลสำหรับการจัดซื้อสินค้าที่เกี่ยวข้องกับเอนทิตี้อื่นๆใน นอกจากนี้ยังอธิบายวิธีการเปลี่ยนลำดับการเรียงลำดับ

## <a name="overview"></a>ภาพรวม

การสนับสนุนสำหรับการเรียงลำดับเอนทิตี้ที่เกี่ยวข้องกับการจัดซื้อสินค้าที่หลายรายการได้รับการปรับปรุงแล้ว ขณะนี้การสนับสนุนนี้มีความสอดคล้องดีขึ้นกับสถานการณ์จำลองของลูกค้าที่มีอยู่ซึ่งเป็นส่วนขยายที่จำเป็นก่อนหน้านี้สำหรับการใช้งานของคู่ค้า

ในรุ่น Retail ที่เก่ากว่ารุ่น 10.0.5 การจัดเรียงลำดับสำหรับประเภทในลำดับชั้นการนำทางจะจัดลำดับตามลำดับตัวอักษร ฟังก์ชันลำดับการเรียงใหม่แบบกำหนดเองช่วยให้ผู้จัดการฝ่ายจัดซื้อการจัดโครงแบบการเรียงสำหรับเอนทิตี้ที่เกี่ยวข้องกับการจัดซื้อสินค้าต่างๆไปยังไคลเอนต์ผู้ใช้ปลายทาง ไคลเอนต์เหล่านี้รวมถึงสำนักงานใหญ่ (HQ) และศูนย์บริการ

## <a name="configure-the-display-order-for-categories-in-the-product-hierarchy"></a>กำหนดค่าลำดับการแสดงผลสำหรับประเภทในลำดับชั้นผลิตภัณฑ์

ก่อนที่คุณจะสามารถทำกระบวนงานนี้ให้เสร็จสมบูรณ์ได้ ข้อมูลสาธิตต้องถูกติดตั้งในสภาพแวดล้อมของคุณ

1. ไปยัง **การขายปลีกและการค้า \> ผลิตภัณฑ์และประเภท \> ลำดับชั้นผลิตภัณฑ์เชิงพาณิชย์**
2. คลิก **แก้ไขการจัดประเภทตามลำดับชั้น**
3. คลิก **แก้ไข**
4. ในเเผนภูมิ ขยาย **ALL \> Action Sports**
5. ในเเผนภูมิ ขยาย **ALL \> Team Sports**
6. ในฟิลด์ **ลำดับการเเสดงผล** ให้ป้อนตัวเลข (ตัวเลขสามารถเป็นค่าลบ)
7. ทำซ้ำขั้นตอนที่4ถึง6สำหรับประเภทเพิ่มเติมใดๆที่คุณต้องการเปลี่ยนแปลงลำดับ

ลำดับการแสดงผลสำหรับลำดับชั้นการนำทางของช่องทางจะปรากฏใน HQ สำหรับลำดับชั้นของผลิตภัณฑ์เชิงพาณิชย์และผลิตภัณฑ์ที่วางจำหน่ายตามประเภท

![ลำดับชั้นผลิตภัณฑ์ที่กำหนดเองเรียงลำดับด้วยค่าลบ](./media/RetailProductHierarchyCustomSortedWithNegativeValues.png)

![เปิดตัวผลิตภัณฑ์ตามประเภทที่กำหนดเองเรียงลำดับตามลำดับชั้นของผลิตภัณฑ์](./media/ReleasedProductsByCategoryCustomSortedBasedOnRetailProductHierarchy.png)

## <a name="configure-the-display-order-for-categories-in-the-channel-navigation-hierarchy"></a>ตั้งค่าคอนฟิกลำดับการแสดงผลสำหรับประเภทในลำดับชั้นของช่องทางการนำทาง

ก่อนที่คุณจะสามารถทำกระบวนงานนี้ให้เสร็จสมบูรณ์ได้ ข้อมูลสาธิตต้องถูกติดตั้งในสภาพแวดล้อมของคุณ

1. ไปยัง **การขายปลีกและการค้า \> ผลิตภัณฑ์และประเภท \> ประเภทการนำทางของช่องทาง**
2. ในรายการ เลือก **ลำดับชั้นการนำทางแฟชั่น** 
3. คลิก **แก้ไขการจัดประเภทตามลำดับชั้น**
4. คลิก **แก้ไข**
5. ในแผนภูมิ เลือก **Fashion \> Womenswear \> Womens Shoes**
6. ในฟิลด์ **ลำดับการเเสดงผล** ให้ป้อนตัวเลข
7. ในแผนภูมิ เลือก **Fashion \> Womenswear \> Tops**

    เช่นเดียวกัน คุณยังสามารถกำหนดลำดับการจัดเรียงสำหรับประเภทย่อยได้

8. ในแผนภูมิ เลือก **Fashion \> Menswear \> Womens Shoes**
9. ในฟิลด์ **ลำดับการเเสดงผล** ให้ป้อนตัวเลข
10. ในแผนภูมิ เลือก **Fashion \> Menswear \> Coats & Jackets**
11. ในฟิลด์ **ลำดับการเเสดงผล** ให้ป้อนตัวเลข
12. ทำซ้ำสำหรับประเภทเพิ่มเติมใดๆที่คุณต้องการเปลี่ยนแปลงลำดับ

ลำดับการแสดงผลสำหรับลำดับชั้นการนำทางของช่องทางปรากฏใน HQ แค็ตตาล็อก และช่องทาง

![ลำดับชั้นการนำทางของช่องทางเเบบกำหนดเองตามลำดับ](./media/ChannelNavCustomSorted.png)

![แค็ตตาล็อกการนำทางของช่องทางเรียงเเบบกำหนดเองตามลำดับชั้นการนำทางของช่องทาง](./media/CatalogNavHierarchyCustomSortedBasedOnChannelNav.png)

![POS ที่มีประเภทการเรียงลำดับแบบกำหนดเอง](./media/POSChannelCategoriesCustomSorted.png)

> [!NOTE]
> ตามค่าเริ่มต้น คุณลักษณะการเรียงลำดับเเบบกำหนดเองจะถูกปิด เมื่อต้องการเรียนรู้วิธีการเปิดใช้งานลักษณะ เเละคุณลักษณะอื่นๆ ดูที่ [การจัดการคุณลักษณะ](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/get-started/feature-management/feature-management-overview)
