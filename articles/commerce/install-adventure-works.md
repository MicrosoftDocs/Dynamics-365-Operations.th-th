---
title: ติดตั้งธีม Adventure Works
description: หัวข้อนี้จะอธิบายวิธีการติดตั้งธีม Adventure Works ใน Microsoft Dynamics 365 Commerce
author: anupamar-ms
ms.date: 07/21/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.region: Global
ms.search.industry: ''
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: 9c94dd8ead32f58a25a396376840101d9c2c9b08
ms.sourcegitcommit: 0c77dbb8547cd36fce3977ca9515fa1474efa77a
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 07/22/2021
ms.locfileid: "6655859"
---
# <a name="install-the-adventure-works-theme"></a>ติดตั้งธีม Adventure Works

[!include [banner](includes/banner.md)]

หัวข้อนี้จะอธิบายวิธีการติดตั้งธีม Adventure Works ใน Microsoft Dynamics 365 Commerce 

> [!IMPORTANT]
> ธีม Adventure Works และโมดูลพร้อมใช้งาน ณ การเริ่มใช้งาน Dynamics 365 Commerce รุ่น 10.0.20 ซึ่งจะพร้อมใช้งานจาก Microsoft AppSource

## <a name="prerequisites"></a>ข้อกำหนดเบื้องต้น

ก่อนที่คุณจะติดตั้งธีม Adventure Works คุณต้องมีสภาพแวดล้อม Dynamics 365 Commerce (Commerce รุ่น 10.0.20 หรือใหม่กว่า) ที่มี Retail Cloud Scale Unit (RCSU) ชุดการพัฒนาซอฟต์แวร์ออนไลน์ของ Commerce (SDK) และไลบรารีโมดูล Commerce สำหรับข้อมูลเกี่ยวกับวิธีการติดตั้ง Commerce SDK และไลบรารีโมดูล ดูที่ [การอัปเดตและไลบรารีโมดูล SDK](e-commerce-extensibility/sdk-updates.md) 

## <a name="installation-steps"></a>ขั้นตอนการติดตั้ง

### <a name="install-the-adventure-works-theme-in-your-application"></a>การติดตั้งธีม Adventure Works ในโปรแกรมประยุกต์ของคุณ

แพคเกจธีม Adventure Works พร้อมใช้งานในฟีด **dynamics365-commerce** เช่น **@msdyn365-commerce-theme/adventureworks-theme-kit** อย่างไรก็ตาม แม้ว่าแพคเกจธีม Adventure Works จะเป็นส่วนหนึ่งของฟีดนั้น แต่อยู่ภายใต้ชื่ออื่น ดังนั้น คุณต้องปฏิบัติตามขั้นตอนต่อไปนี้เพื่อเพิ่มรายการทะเบียนสำหรับชื่อ

1. อัปเดตไฟล์ **.npmrc** เพื่อให้มีรายการทะเบียนต่อไปนี้ (ถ้ายังไม่ได้รวมรายการ):

    `@msdyn365-commerce-theme:registry=https://pkgs.dev.azure.com/commerce-partner/Registry/_packaging/dynamics365-commerce/npm/registry/`

1. อัปเดตไฟล์ **.yarnrc** เพื่อให้มีรายการทะเบียนต่อไปนี้ (ถ้ายังไม่ได้รวมรายการ):

    `"@msdyn365-commerce-theme:registry" "https://pkgs.dev.azure.com/commerce-partner/Registry/_packaging/dynamics365-commerce/npm/registry/"`  
    
เมื่อต้องการติดตั้งแพคเกจในสภาพแวดล้อมเฉพาะที่ของคุณ ให้รันคำสั่งต่อไปนี้จากพร้อมต์คำสั่ง ไฟล์ package.json จะอัปเดตไฟล์ package.json โดยอัตโนมัติ เพื่อให้รวมการดำเนินการที่เชื่อมโยงกัน

`yarn add @msdyn365-commerce-theme/adventureworks-theme-kit`

ในไฟล์ **package.json** คุณควรอัปเดตรุ่นธีมเป็นรุ่นเฉพาะ

> [!IMPORTANT]
> - รุ่นธีมควรตรงกับรุ่นไลบรารีโมดูลเพื่อให้แน่ใจว่าคุณลักษณะทั้งหมดจะทำงานตามที่คาดไว้ 
> - รุ่นขั้นต่ำของไลบรารีโมดูล Commerce และ SDK ควรเป็น 10.0.20 (9.31) 

### <a name="add-the-font-files-for-the-adventure-works-theme"></a>เพิ่มไฟล์แบบอักษรของธีม Adventure Works

หลังจากที่ติดตั้งธีม Adventure Works ในแอปของคุณแล้ว คุณต้องเพิ่มไฟล์แบบอักษรที่ใช้ได้กับธีมนี้ เมื่อต้องการขั้นตอนนี้ให้สมบูรณ์ ให้คัดลอกไฟล์แบบอักษรทั้งหมดจาก **\node_modules@msdyn365-commerce-theme\adventureworks-theme-kit\src\modules\adventureworks\public\webfonts** ไปยังพาธไดเรกทอรีสาธารณะของโปรแกรมประยุกต์คู่ค้า **\public\webfonts**

### <a name="set-up-the-resources-for-the-adventure-works-theme"></a>ตั้งค่าทรัพยากรของธีม Adventure Works

ขั้นตอนต่อไปคือการอัปเดตทรัพยากรเริ่มต้นที่ต้องใช้ในธีม เมื่อต้องการขั้นตอนนี้ให้สมบูรณ์ ให้คัดลอกเนื้อหาจากไฟล์ global.json ภายใต้ **\node_modules@msdyn365-commerce-theme\adventureworks-theme-kit\src\modules\adventureworks\resources\modules** ไปยังไฟล์ global.json ของโปรแกรมประยุกต์คู่ค้าภายใต้ **\src\resources\modules** ถ้าไม่มีไดเรกทอรีเป้าหมาย **\src\resources** อยู่ จะสามารถคัดลอกได้ทั้งหมดจากไดเรกทอรีต้นทาง **\node_modules@msdyn365-commerce-theme\adventureworks-theme-kit\src\modules\adventureworks** ไปยังไดเรกทอรีเป้าหมาย **\src**

### <a name="pull-updates-and-validate-the-theme"></a>ดึงข้อมูลการอัปเดตและตรวจสอบความถูกต้องของธีม

สำหรับข้อมูลเกี่ยวกับวิธีการดึง SDK ไลบรารีโมดูล และการอัปเดตการดำเนินการที่เชื่อมโยงกันอื่นๆ ดูที่ส่วน "ดึงการอัปเดต" ของ [SDK และการอัปเดตไลบรารีโมดูล](e-commerce-extensibility/sdk-updates.md#pull-updates)

หลังจากดึงการดำเนินการที่เชื่อมโยงกันล่าสุดแล้ว คุณสามารถรันคำสั่ง **yarn start** เพื่อเริ่มต้นเซิร์ฟเวอร์โหนดในสภาพแวดล้อมการพัฒนาของคุณ และทดสอบชุดธีม Adventure Works ใหม่ได้ เลือกดูโปรแกรมประยุกต์เฉพาะที่โดยใช้พารามิเตอร์สตริงการสอบถาม `?theme=adventureworks` (ตัวอย่างเช่น `https://localhost:4000/?theme=adventureworks`)

## <a name="additional-resources"></a>ทรัพยากรเพิ่มเติม

[ธีม Adventure Works](adventure-works-theme.md)

[ภาพรวมของไลบรารีโมดูล](starter-kit-overview.md)

[การอัปเดต SDK และไลบรารีโมดูล](e-commerce-extensibility/sdk-updates.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
