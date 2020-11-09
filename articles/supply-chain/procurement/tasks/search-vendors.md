---
title: ค้นหาผู้จัดจำหน่าย
description: 'เรียนรู้วิธีการค้นหาผู้จัดจำหน่ายตามเงื่อนไขที่ระบุ '
author: mkirknel
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: VendSearchCriterion, VendSearchAddCategory, VendSearchAddReviewCriterionGroup, VendSearchResults, VendSearchAddReviewCriterion
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: bc28deb979fe8dc4e31befe6d4d5f6f91388f13e
ms.sourcegitcommit: e3f4dd2257a3255c2982f4fc7b72a1121275b88a
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 10/16/2020
ms.locfileid: "4018063"
---
# <a name="search-for-vendors"></a>ค้นหาผู้จัดจำหน่าย

[!include [banner](../../includes/banner.md)]

เรียนรู้วิธีการค้นหาผู้จัดจำหน่ายตามเงื่อนไขที่ระบุ  ตัวอย่างนี้แสดงวิธีการค้นหาผู้จัดจำหน่ายที่ได้รับอนุมัติสำหรับประเภทการจัดซื้อเฉพาะ และมีที่อยู่หลักของพวกเขาในประเทศเฉพาะ คุณสามารถรันขั้นตอนนี้ในบริษัทข้อมูลสาธิต USMF หรือข้อมูลของคุณเอง งานนี้อาจมักจะถูกดำเนินการโดยผู้เชี่ยวชาญด้านการจัดซื้อจัดหา

1. ไปที่การจัดซื้อและการจัดหา > ผู้จัดจำหน่าย > การค้นหาผู้จัดจำหน่าย
2. คลิกที่ไอคอนบวกเพื่อเปิดหน้าการเลือกประเภทการจัดซื้อ  
3. ในแผนภูมิ เลือก 'CORP PROCUREMENT CATEGORIES\OFFICE MACHINES'
    * ถ้าคุณกำลังใช้งานขั้นตอนนี้เป็นคู่มืองาน คุณอาจจะต้องคลิกปุ่มปลดล็อกก่อนที่จะเลือกโหนดที่ถูกต้อง ถ้าคุณไม่ได้ใช้ USMF เลือกหนึ่งในประเภทที่คุณมี  
4. คลิก เพิ่ม
    * สามารถเลือกมากกว่าหนึ่งประเภทที่นี่ ถ้าคุณทำเช่นนั้น การค้นหาจะค้นหาผู้จัดจำหน่ายที่ได้รับการอนุมัติอย่างน้อยหนึ่งประเภท  
5. คลิก ตกลง
6. ในฟิลด์ประเทศ/ภูมิภาค ให้พิมพ์ค่าใดค่าหนึ่ง
7. คลิก ตกลง

