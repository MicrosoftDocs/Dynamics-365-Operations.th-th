---
title: เลือกธีมของไซต์
description: หัวข้อนี้จะอธิบายวิธีการตั้งค่า หรือเปลี่ยนชุดรูปแบบไซต์ของคุณใน Microsoft Dynamics 365 Commerce
author: bicyclingfool
ms.date: 09/15/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: StuHarg
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: cd110a94991659036ac5cee1cd5f77e0cd3ba7356be902bdae37e957247535ea
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 08/05/2021
ms.locfileid: "6737541"
---
# <a name="select-a-site-theme"></a>เลือกธีมของไซต์

[!include [banner](includes/banner.md)]

หัวข้อนี้จะอธิบายวิธีการตั้งค่า หรือเปลี่ยนชุดรูปแบบไซต์ของคุณใน Microsoft Dynamics 365 Commerce

โครงร่างและลักษณะของไซต์ (ตัวอย่างเช่น แบบอักษร ขนาด และสี) จะถูกกำหนดโดยชุดรูปแบบที่คุณเลือกและนำไปใช้กับไซต์ ชุดรูปแบบจะถูกสร้างขึ้น และใช้งานโดยนักพัฒนาที่บริษัทของคุณ สำหรับภาพรวมของชุดรูปแบบโปรดดู [ภาพรวมของชุดรูปแบบ](e-commerce-extensibility/theming.md) สำหรับข้อมูลเพิ่มเติมเกี่ยวกับวิธีสร้างและปรับใช้ชุดรูปแบบ โปรดดู [สร้างชุดรูปแบบใหม่](e-commerce-extensibility/create-theme.md)

โดยค่าเริ่มต้น เมื่อคุณสร้างไซต์เป็นครั้งแรกระบบจะใช้ชุดรูปแบบที่ชื่อ **Fabrikam** ธีมเริ่มต้นนี้ให้ไว้เป็นส่วนหนึ่งของไลบรารีโมดูล Commerce หลังจากที่คุณได้ปรับใช้ชุดรูปแบบเพิ่มเติมสำหรับไซต์ของคุณแล้ว คุณสามารถตั้งค่าคอนฟิกไซต์ดังกล่าวเพื่อให้ใช้งานได้อย่างใดอย่างหนึ่งแทน

## <a name="select-the-site-theme"></a>เลือกชุดรูปแบบของไซต์

เมื่อต้องการเลือกชุดรูปแบบที่จะใช้กับไซต์ของคุณ ให้ทำตามขั้นตอนต่อไปนี้

1. ในสภาพแวดล้อมการสร้างและแก้ไขไซต์ ให้ไปที่ไซต์ของคุณ
1. ไปที่ **การจัดการไซต์** \> **เพิ่มความสามารถ**
1. ภายใต้ **ชุดรูปแบบ** ให้เลือกชุดรูปแบบในเมนูแบบหล่นลง
1. เมื่อต้องการใช้ชุดรูปแบบที่เลือกกับไซต์ของคุณให้เลือก **บันทึกและเผยแพร่**

> [!NOTE]
> ชุดรูปแบบที่คุณเลือกเผยแพร่ไปยังไซต์ของคุณ ทันทีที่คุณเลือก **บันทึกและเผยแพร่** บนหน้า **เพิ่มความสามารถ** เมื่อต้องการแสดงตัวอย่างชุดรูปแบบบนไซต์ของคุณก่อนที่จะใช้งาน คุณสามารถใช้สภาพแวดล้อมการพัฒนาหรือ Sandbox ของคุณได้

## <a name="additional-resources"></a>แหล่งข้อมูลเพิ่มเติม

[เพิ่มโลโก้](add-logo.md)

[ทำงานกับไฟล์การแก้ไข CSS](css-override-files.md)

[เพิ่มไอคอนประจำไซต์](add-favicon.md)

[เพิ่มข้อความต้อนรับ](add-welcome-message.md)

[เพิ่มข้อความสงวนลิขสิทธิ์](add-copyright-notice.md)

[เพิ่มภาษาลงในไซต์ของคุณ](add-languages-to-site.md)

[เพิ่มโค้ดสคริปต์ให้กับหน้าไซต์เพื่อสนับสนุนการตรวจวัดระยะไกล](add-telemetry.md)

[ภาพรวมการกำหนดธีม](e-commerce-extensibility/theming.md)

[สร้างธีมใหม่](e-commerce-extensibility/create-theme.md)



[!INCLUDE[footer-include](../includes/footer-banner.md)]
