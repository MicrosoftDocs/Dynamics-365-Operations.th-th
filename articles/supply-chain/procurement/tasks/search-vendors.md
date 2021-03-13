---
title: ค้นหาผู้จัดจำหน่าย
description: 'เรียนรู้วิธีการค้นหาผู้จัดจำหน่ายตามเงื่อนไขที่ระบุ '
author: RichardLuan
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: VendSearchCriterion, VendSearchAddCategory, VendSearchAddReviewCriterionGroup, VendSearchResults, VendSearchAddReviewCriterion
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: riluan
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 7caa146532d2bce06b009c45da635327766a88d1
ms.sourcegitcommit: deac22ba5377a912d93fe408c5ae875706378c2d
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 01/16/2021
ms.locfileid: "5020716"
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

