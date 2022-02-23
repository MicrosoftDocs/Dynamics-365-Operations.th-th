---
title: โมดูลตัวเลือกไซต์
description: หัวข้อนี้ครอบคลุมถึงโมดูลตัวเลือกไซต์และอธิบายวิธีการเพิ่มลงในเพจของไซต์ใน Microsoft Dynamics 365 Commerce
author: anupamar-ms
manager: annbe
ms.date: 10/20/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: ''
ms.author: anupamar
ms.search.validFrom: 2020-02-10
ms.dyn365.ops.version: Release 10.0.13
ms.openlocfilehash: b4e5f715efcac7f883df99508d282db904be0d80
ms.sourcegitcommit: 9c05d48f6e03532aa711e1d89d0b2981e9d37200
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 12/03/2020
ms.locfileid: "4665234"
---
# <a name="site-selector-module"></a>โมดูลตัวเลือกไซต์

[!include [banner](includes/banner.md)]

หัวข้อนี้ครอบคลุมถึงโมดูลตัวเลือกไซต์และอธิบายวิธีการเพิ่มลงในเพจของไซต์ใน Microsoft Dynamics 365 Commerce

## <a name="overview"></a>ภาพรวม

เมื่อธุรกิจมีไซต์ที่แตกต่างกันในตลาด ภูมิภาค และตำแหน่งที่ตั้ง ผู้ใช้เว็บไซต์ต้องมีวิธีการง่ายๆ ในการสลับไปมาระหว่างไซต์ต่างๆ และเลือกไซต์การซื้อสินค้าที่ต้องการ เพื่อให้ตอบรับกับสถานการณ์จำลองนี้ โมดูลของตัวเลือกไซต์จะช่วยให้ผู้ใช้สามารถเรียกดูระหว่างไซต์ต่างๆ ได้

โมดูลการเลือกไซต์ต้องมีการตั้งค่าคอนฟิกกับรายการไซต์ (ตลาด ภูมิภาค หรือสถานที่ตั้ง) ซึ่งผู้ใช้ไซต์สามารถเลือกดูได้

> [!NOTE]
> โมดูลตัวเลือกไซต์มีอยู่ใน Dynamics 365 Commerce รุ่น 10.0.14

ภาพประกอบต่อไปนี้แสดงตัวอย่างของโมดูลตัวเลือกไซต์ที่แนะนำในส่วนหัวของหน้าไซต์

![ตัวอย่างของโมดูลตัวเลือกไซต์ในส่วนหัวของหน้าไซต์](./media/ecommerce-sitepicker.PNG)

## <a name="site-selector-module-properties"></a>คุณสมบัติของโมดูลตัวเลือกไซต์

| ชื่อคุณสมบัติ | มูลค่า                 | คำอธิบาย |
|---------------|-----------------------|-------------|
| หัวข้อ       | ข้อความ                  | หัวข้อสำหรับโมดูล |
| ตัวเลือกของไซต์  | ชื่อ รูปภาพ URL      | คุณสมบัตินี้จะระบุชื่อ ลิงก์ไปยังโฮมเพจของไซต์ และรูปภาพเสริมที่จะแสดงสำหรับแต่ละไซต์ที่รวมอยู่ในโมดูล รูปอาจเป็นแฟล็กหรือบางอย่างที่เป็นตัวแทนของตลาด ภูมิภาค หรือตำแหน่งที่ตั้ง |

## <a name="add-a-site-selector-module-to-a-page"></a>เพิ่มโมดูลตัวเลือกไซต์ไปที่หน้า

โมดูลตัวเลือกไซต์สามารถเพิ่มเข้าไปใน [โมดูลของส่วนหัว](author-header-module.md) ภายใต้ช่องตัวเลือกไซต์ หลังจากที่เพิ่มแล้ว คุณสามารถกำหนดส่วนหัวของโมดูลและตัวเลือกไซต์

## <a name="additional-resources"></a>ทรัพยากรเพิ่มเติม

[ภาพรวมของไลบรารีโมดูล](starter-kit-overview.md)

[โมดูลส่วนหัว](author-header-module.md)

[โมดูลการแสดงเส้นทาง](add-breadcrumb.md)

[โมดูลเมนูนำทาง](nav-menu-module.md)
