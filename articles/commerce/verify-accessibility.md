---
title: ตรวจสอบความสามารถในการเข้าถึงเนื้อหาของหน้า
description: หัวข้อนี้จะอธิบายวิธีการตรวจสอบความสามารถในการเข้าถึงเนื้อหาของหน้าใน Microsoft Dynamics 365 Commerce
author: arotkin
manager: annbe
ms.date: 01/08/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.search.region: Global
ms.search.industry: retail
ms.author: arotkin
ms.search.validFrom: 2019-12-19
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: 70604ed16d72e519724aeb2c33bd4a91a8b26c8c
ms.sourcegitcommit: ef3a1d7527311d00b69a1072ae5eb021ce68034c
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 01/09/2020
ms.locfileid: "2946087"
---
# <a name="verify-page-content-accessibility"></a>ตรวจสอบความสามารถในการเข้าถึงเนื้อหาของหน้า

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

หัวข้อนี้จะอธิบายวิธีการตรวจสอบความสามารถในการเข้าถึงเนื้อหาของหน้าใน Microsoft Dynamics 365 Commerce

## <a name="overview"></a>ภาพรวม

เมื่อคุณเปลี่ยนหน้าเสร็จแล้ว คุณควรตรวจสอบให้แน่ใจว่าเนื้อหานั้นสามารถเข้าถึงได้สำหรับทุกคนบนเว็บ ในเครื่องมือการสร้าง Commerce คุณสามารถตรวจสอบความสามารถในการเข้าถึงเนื้อหาของหน้าได้อย่างง่ายดายโดยใช้บริการ [Microsoft Accessibility Insights](https://accessibilityinsights.io/) บริการนี้จะตรวจสอบเนื้อหาของเพจของคุณเทียบกับแนวทาง [ความสามารถในการเข้าถึง World Wide Web Consortium (W3C)](https://www.w3.org/standards/webdesign/accessibility) ล่าสุด

การรวม [Microsoft Accessibility Insights](https://accessibilityinsights.io/) ต้องถูกเปิดอยู่ที่ระดับผู้เช่าหรือระดับไซต์ ก่อนที่คุณจะสามารถใช้งานได้

## <a name="turn-on-microsoft-accessibility-insights-for-all-the-sites-in-your-tenant"></a>เปิดใช้งาน Microsoft Accessibility Insights สำหรับไซต์ทั้งหมดในผู้เช่าของคุณ

เมื่อต้องการเปิดใช้งานการรวม [Microsoft Accessibility Insights](https://accessibilityinsights.io/) สำหรับไซต์ Commerce ทั้งหมดในผู้เช่าของคุณ ให้ทำตามขั้นตอนเหล่านี้

> [!NOTE]
> เมื่อต้องการเข้าถึงการตั้งค่าผู้เช่า คุณต้องลงชื่อเข้าใช้ Commerce ในฐานะผู้ดูแลระบบ

1. ลงชื่อเข้าใช้ Commerce ในฐานะผู้ดูแลระบบ
1. ในบานหน้าต่างนำทางด้านซ้าย ให้เลือก **การตั้งค่าผู้เช่า** (ถัดจากสัญลักษณ์เกียร์) เพื่อขยาย
1. ภายใต้ **การตั้งค่าผู้เช่า** ให้เลือก **คุณลักษณะ**
1. ตั้งค่าตัวเลือก **ตรวจสอบความสามารถในการเข้าถึง** เป็น **เปิด**

## <a name="turn-on-microsoft-accessibility-insights-for-a-single-site"></a>เปิดใช้งาน Microsoft Accessibility Insights สำหรับไซต์เดียว

เมื่อต้องการเปิดใช้งานการรวม [Microsoft Accessibility Insights](https://accessibilityinsights.io/) สำหรับไซต์ Commerce เดียว ให้ทำตามขั้นตอนเหล่านี้

1. ภายใต้ **ไซต์** ให้เลือก **Fabrikam** (หรือชื่อไซต์ของคุณ)
1. ในบานหน้าต่างนำทางด้านซ้าย ให้เลือก **การตั้งค่าไซต์** เพื่อขยาย
1. ภายใต้ **การตั้งค่าไซต์** ให้เลือก **คุณลักษณะ**
1. ตั้งค่าตัวเลือก **ตรวจสอบความสามารถในการเข้าถึง** เป็น **เปิด**

## <a name="verify-the-accessibility-of-the-content-on-the-home-page"></a>ตรวจสอบความสามารถในการเข้าถึงเนื้อหาบนโฮมเพจ

หากต้องการใช้บริการ [Microsoft Accessibility Insights](https://accessibilityinsights.io/) แบบรวม เพื่อสแกนและตรวจสอบเนื้อหาของโฮมเพจของคุณใน Commerce ให้ทำตามขั้นตอนเหล่านี้

1. ภายใต้ **ไซต์** ให้เลือก **Fabrikam** (หรือชื่อไซต์ของคุณ)
1. ในบานหน้าต่างนำทางด้านซ้าย ให้เลือก **หน้า**
1. ค้นหาและเลือกหน้าหลัก เพื่อเปิดในโปรแกรมแก้ไขหน้า
1. บนแถบคำสั่ง ให้เลือก **ตรวจสอบความสามารถในการเข้าถึง** หน้า **ตรวจสอบความสามารถในการเข้าถึง** จะปรากฏขึ้น
1. หลังจากการสแกนเสร็จสมบูรณ์ ให้ตรวจทานเนื้อหาของรายงาน
1. ถ้าการตรวจสอบใดๆ ล้มเหลว ให้เลือกรายการตรวจสอบที่ล้มเหลวแต่ละรายการเพื่อขยาย เพื่อให้คุณสามารถดูรายละเอียดเพิ่มเติมได้
1. หากต้องการปิดรายงานหลังจากที่คุณตรวจทานเสร็จแล้ว ให้เลื่อนไปที่ด้านล่างของหน้า **ตรวจสอบความสามารถในการเข้าถึง** และเลือก **ตกลง**

## <a name="additional-resources"></a>แหล่งข้อมูลเพิ่มเติม

[ปรับเปลี่ยนหน้าไซต์ที่มีอยู่](modify-existing-page.md)

[เพิ่มหน้าไซต์ใหม่](add-new-page.md)

[เลือกเค้าโครงหน้า](select-page-layouts.md)

[จัดการข้อมูลเมตา SEO](manage-seo-metadata.md)

[บันทึก แสดงตัวอย่าง และเผยแพร่หน้า](save-preview-publish-page.md)

[ทำให้หน้าผลิตภัณฑ์สมบูรณ์](enrich-product-page.md)

[ทำให้หน้าเริ่มต้นของประเภทสมบูรณ์](enrich-category-page.md)
