---
title: การแก้ไขปัญหาส่วนขยายของ Store Commerce
description: บทความนี้จะอธิบายวิธีการแก้ไขปัญหาส่วนขยายในแอป Store Commerce ของ Microsoft Dynamics 365 Commerce
author: josaw1
ms.date: 06/01/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: rassadi
ms.search.validFrom: 2017-06-20
ms.openlocfilehash: 1a2d6a68b7556d8b4d05529efd90f9e66f0c5925
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 08/12/2022
ms.locfileid: "9269793"
---
# <a name="troubleshoot-store-commerce-extension-issues"></a>การแก้ไขปัญหาส่วนขยายของ Store Commerce

[!include [banner](../includes/banner.md)]

บทความนี้จะอธิบายวิธีการแก้ไขปัญหาส่วนขยายในแอป Store Commerce ของ Microsoft Dynamics 365 Commerce

## <a name="extensions-packages-arent-loaded"></a>ไม่ได้โหลดแพคเกจส่วนขยาย

### <a name="extensions-packages-dont-appear-on-the-pos--settings-page"></a>แพคเกจส่วนขยายจะไม่ปรากฏในหน้า POS \> การตั้งค่า

ทริกเกอร์ Commerce Runtime (CRT) อาจไม่ได้รับการอัปเดตเพื่อรวมแพคเกจส่วนขยาย หรือไม่ได้ปรับใช้ สำหรับข้อมูลเพิ่มเติม ดูที่ [ความสามารถในการเพิ่มฟังก์ชันของ Commerce runtime (CRT) และทริกเกอร์](../dev-itpro/commerce-runtime-extensibility-trigger.md)

### <a name="extensions-packages-appear-on-the-pos--settings-page-but-the-manifest-isnt-loaded"></a>แพคเกจส่วนขยายจะปรากฏในหน้า POS \> การตั้งค่า แต่ไม่มีการโหลดรายการ

ยืนยันว่าแพคเกจส่วนขยายมีอยู่ในโฟลเดอร์ **C:\\Program Files\\Microsoft Dynamics 365\\10.0\\Store Commerce\\Extensions** ถ้ามีแพคเกจอยู่ ควรจะมีโฟลเดอร์ **POS** ที่มีรายการอยู่

หากไม่มีโฟลเดอร์ **POS** ให้ยืนยันว่าโครงการ Store Commerce อ้างอิงโครงการขยายการขายหน้าร้าน (POS) อย่างถูกต้อง ตรวจสอบความถูกต้องของพาธการอ้างอิงโครงการ และตรวจสอบให้แน่ใจว่ามีพาธนั้นอยู่ 

ในภาพประกอบตัวอย่างต่อไปนี้ โครงการโปรแกรมติดตั้งมีปัญหาในการใช้โครงการขยายที่อ้างอิง

![การอ้างอิงโครงการของตัวติดตั้ง Store Commerce ไม่ถูกต้อง](media/ReferenceNotValid.png)

ถ้ามีการเพิ่มการอ้างอิงของโครงการส่วนขยายอย่างถูกต้อง จะไม่มีคําเตือนหรือปัญหาการขึ้นต่อกันในโครงการโปรแกรมติดตั้ง ดังที่แสดงในภาพประกอบตัวอย่างต่อไปนี้

![การอ้างอิงโครงการของตัวติดตั้ง Store Commerce ถูกต้อง](media/ReferenceValid.png)
