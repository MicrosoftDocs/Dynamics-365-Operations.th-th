---
title: ติดตั้งธีม Adventure Works
description: บทความนี้จะอธิบายวิธีการติดตั้งธีม Adventure Works ใน Microsoft Dynamics 365 Commerce
author: anupamar-ms
ms.date: 12/10/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.8
ms.search.industry: ''
ms.search.form: ''
ms.openlocfilehash: f5c195694633c96a473f0f824c1f182903082bff
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 08/12/2022
ms.locfileid: "9274298"
---
# <a name="install-the-adventure-works-theme"></a>ติดตั้งธีม Adventure Works

[!include [banner](includes/banner.md)]

บทความนี้จะอธิบายวิธีการติดตั้งธีม Adventure Works ใน Microsoft Dynamics 365 Commerce 

> [!IMPORTANT]
> ธีม Adventure Works และโมดูลพร้อมใช้งาน ณ การเริ่มใช้งาน Dynamics 365 Commerce รุ่น 10.0.20 ซึ่งจะพร้อมใช้งานจาก Microsoft AppSource

## <a name="prerequisites"></a>ข้อกำหนดเบื้องต้น

ก่อนที่คุณจะติดตั้งธีม Adventure Works คุณต้องมีสภาพแวดล้อม Dynamics 365 Commerce (Commerce รุ่น 10.0.20 หรือใหม่กว่า) ที่มี Retail Cloud Scale Unit (RCSU) ชุดการพัฒนาซอฟต์แวร์ออนไลน์ของ Commerce (SDK) และไลบรารีโมดูล Commerce สำหรับข้อมูลเกี่ยวกับวิธีการติดตั้ง Commerce SDK และไลบรารีโมดูล ดูที่ [ตั้งค่าสภาพแวดล้อมการพัฒนา](e-commerce-extensibility/setup-dev-environment.md) 

## <a name="installation-steps"></a>ขั้นตอนการติดตั้ง

### <a name="install-the-adventure-works-theme-in-your-application"></a>การติดตั้งธีม Adventure Works ในโปรแกรมประยุกต์ของคุณ

แพคเกจธีม Adventure Works พร้อมใช้งานในฟีด **dynamics365-commerce** เช่น **@msdyn365-commerce-theme/adventureworks-theme-kit** อย่างไรก็ตาม แม้ว่าแพคเกจธีม Adventure Works จะเป็นส่วนหนึ่งของฟีดนั้น แต่อยู่ภายใต้ชื่ออื่น ดังนั้น คุณต้องปฏิบัติตามขั้นตอนต่อไปนี้เพื่อเพิ่มรายการทะเบียนสำหรับชื่อ

1. อัปเดตไฟล์ **.npmrc** เพื่อให้มีรายการทะเบียนต่อไปนี้ (ถ้ายังไม่ได้รวมรายการ):

    `@msdyn365-commerce-theme:registry=https://pkgs.dev.azure.com/commerce-partner/Registry/_packaging/dynamics365-commerce/npm/registry/`

1. อัปเดตไฟล์ **.yarnrc** เพื่อให้มีรายการทะเบียนต่อไปนี้ (ถ้ายังไม่ได้รวมรายการ):

    `"@msdyn365-commerce-theme:registry" "https://pkgs.dev.azure.com/commerce-partner/Registry/_packaging/dynamics365-commerce/npm/registry/"`  
    
เมื่อต้องการติดตั้งแพคเกจในสภาพแวดล้อมเฉพาะที่ของคุณ ให้เรียกใช้คำสั่ง `yarn add THEME_PACKAGE@VERSION` จากพร้อมท์คำสั่ง โดยที่ **THEME_PACKAGE** เป็นแพคเกจชุดรูปแบบ (@msdyn365-commerce-theme/adventureworks-theme-kit) และ **VERSION** เป็นหมายเลขรุ่นของไลบรารีโมดูลที่ถูกใช้อยู่ รุ่นของแพคเกจชุดรูปแบบและไลบรารีโมดูลต้องตรงกัน เมื่อต้องการค้นหาหมายเลขรุ่นของไลบรารีโมดูลที่ถูกต้องที่จะใช้ ให้เปิดไฟล์ package.json และระบุค่า **starter-pack** ในส่วน **การขึ้นต่อกัน** ในตัวอย่างต่อไปนี้ ไฟล์ package.json จะใช้รุ่น 9.32 ของไลบรารีโมดูลซึ่งแมปไปยังรีลีส Dynamics 365 Commerce รุ่น 10.0.22  

```json
"dependencies": {
    "@msdyn365-commerce-modules/starter-pack": "9.32",
}
```

ตัวอย่างต่อไปนี้แสดงวิธีการเรียกใช้คำสั่ง `yarn add` เพื่อเพิ่มรุ่น 9.32 ของธีม Adventure Works คำสั่งดังกล่าวจะอัปเดตไฟล์ package.json โดยอัตโนมัติ เพื่อให้รวมการขึ้นต่อกัน

`yarn add @msdyn365-commerce-theme/adventureworks-theme-kit@9.32`

สำหรับข้อมูลเพิ่มเติมเกี่ยวกับการอัปเดตรุ่นของไลบรารีโมดูล ดูที่ [การอัปเดต SDK และไลบรารีโมดูล](e-commerce-extensibility/sdk-updates.md) 

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
