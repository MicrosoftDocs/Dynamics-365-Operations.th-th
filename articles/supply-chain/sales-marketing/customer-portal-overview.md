---
title: ภาพรวมพอร์ทัลลูกค้าสำหรับ Dynamics 365 Supply Chain Management
description: หัวข้อนี้จะแนะนำพอร์ทัลของลูกค้า และอธิบายว่าใครควรใช้ และวิธีการทำงานเป็นอย่างไร
author: dasani-madipalli
manager: tfehr
ms.date: 06/16/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: damadipa
ms.search.validFrom: 2020-04-22
ms.dyn365.ops.version: Release 10.0.13
ms.openlocfilehash: 25b1962af182fc2749fcd6ec0035613d8365deb1
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 01/15/2021
ms.locfileid: "4980817"
---
# <a name="customer-portal-for-dynamics-365-supply-chain-management-overview"></a>ภาพรวมพอร์ทัลลูกค้าสำหรับ Dynamics 365 Supply Chain Management

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

## <a name="what-is-the-customer-portal"></a>พอร์ทัลลูกค้าคืออะไร?

ระบบโซ่อุปทานยุคใหม่พึ่งพาการรวม ซึ่งจำเป็นจะต้องให้สินค้าคงคลัง ความต้องการของลูกค้า และแผนกขายรวมกัน แทนที่จะอยู่ต่างไซโลกัน พอร์ทัลลูกค้าจะช่วยให้องค์กรต่าง ๆ ที่ใช้ Microsoft Dynamics 365 Supply Chain Management เพิ่มประสิทธิภาพการรวมนี้ และให้ข้อมูลลูกค้าได้มีประสิทธิภาพยิ่งขึ้น

พอร์ทัลของลูกค้าคือแม่แบบ [พอร์ทัล Power Apps](https://docs.microsoft.com/powerapps/maker/portals/overview) ซึ่งทำให้บริษัทสร้างเว็บไซต์ที่เชื่อมโยงกับธุรกิจกับธุรกิจ (B2B) สำหรับสถานการณ์ที่เกี่ยวข้องกับการดำเนินการของใบสั่งขาย แม่แบบจะใช้ Supply Chain Management แบบ [การการรวมแบบสองทิศทาง](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-home-page) และพอร์ทัล Power Apps เพื่อให้ลูกค้าองค์กรภายนอกสามารถดูและสร้างข้อมูลจากสภาพแวดล้อม Dynamics 365 ของบริษัทได้

แม่แบบบนพอร์ทัลต์ลูกค้ามีความสามารถในการกำหนดเองทั้งหมดเหมือนที่ Power Apps มี แม่แบบจะปรับเปลี่ยนได้ง่ายเพื่อแสดงถึงแบรนด์ของบริษัท เพิ่มฟังก์ชันที่เพิ่มขึ้น และเปลี่ยนประสบการณ์การใช้งานของผู้ใช้ ฟังก์ชันทั้งหมดที่แม่แบบมีให้ตั้งแต่ต้น สามารถปรับเปลี่ยนได้ตามต้องการ

> [!IMPORTANT]
> โดยตัวแม่แบบเอง ไม่ได้ถูกคาดหวังว่าจะทำงานได้อย่างสมบูรณ์ แม่แบบทำหน้าที่เป็นเพียงตัวเริ่มต้น สำหรับลูกค้าที่ต้องการสร้างเว็บไซต์ที่เชื่อมต่อกับภายนอก เพื่อให้ลูกค้าองค์กรสามารถมีส่วนร่วมกับข้อมูลจากการบริหาร Supply Chain Management

> [!NOTE]
> เอกสารประกอบของพอร์ทัลลูกค้ามีไว้สำหรับผู้ดูแลระบบ ผู้เลือกกำหนด และผู้ติดตั้งระบบซึ่งจะตั้งค่าพอร์ทัลของลูกค้าสำหรับการติดตั้ง Supply Chain Management ใช้คำนิยาม _ลูกค้า_ และ _ผู้ใช้_ เพื่ออธิบายถึงบุคคลที่เป็นลูกค้าขององค์กรที่กำลังใช้งาน Supply Chain Management และผู้ใช้ที่จะใช้พอร์ทัลสุดท้ายเอง

## <a name="video"></a>วีดิทัศน์

> [!VIDEO https://www.microsoft.com/videoplayer/embed/RE4ylwW]

[ภาพรวมของเท็มเพลพอร์ทัลลูกค้าในวิดีโอ Dynamics 365 Supply Chain Management](https://youtu.be/nPrqoLuHfV8) (แสดงไว้ข้างบน) จะรวมอยู่ใน [เพลย์ลิสต์ Finance and Operations](https://www.youtube.com/playlist?list=PLcakwueIHoT_SYfIaPGoOhloFoCXiUSyW) ที่พร้อมใช้งานใน YouTube

## <a name="who-should-use-it"></a>ใครควรใช้งาน

พอร์ทัลลูกค้าถูกออกแบบมาสำหรับบริษัทที่ใช้ Supply Chain Management และมีลักษณะดังนี้:

- ต้องการสร้างเว็บไซต์ที่เชื่อมต่อกับภายนอก ซึ่งสื่อสารข้อมูลการประมวลผลใบสั่ง (เช่น สถานะของใบสั่งหรือข้อมูลบัญชี) โดยตรงจาก Supply Chain Management ของตนให้กับลูกค้าองค์กรของตน
- พวกเขากำลังเปลี่ยนจาก Dynamics AX 2012 ไปยัง Supply Chain Management และก่อนหน้านี้ใช้ [พอร์ทัล AX 2012 Customer self-service](https://docs.microsoft.com/dynamicsax-2012/appuser-itpro/about-the-customer-self-service-portal)

ชนิดขององค์กรต่อไปนี้ **ไม่** ได้เป็นชนิดที่ดีสำหรับการใช้งานพอร์ทัลลูกค้า:

- บริษัทที่ต้องการสร้างเว็บไซต์สำหรับลูกค้าที่ไม่ใช่องค์กร บริษัทเหล่านี้ควรพิจารณาการสร้าง [เว็บไซต์อีคอมเมิร์ซ Dynamics 365 Commerce](https://docs.microsoft.com/dynamics365/commerce/create-ecommerce-site)
- บริษัทที่ใช้เว็บไซต์พอร์ทัล Power Apps อยู่แล้วสำหรับวัตถุประสงค์ที่คล้ายกัน บริษัทเหล่านี้จะไม่ได้รับผลประโยชน์เพิ่มเติมจากพอร์ทัลของลูกค้า พอร์ทัลลูกค้ามีการจัดส่งเป็นแม่แบบที่ทำหน้าที่เป็นคำแนะนำ และจุดเริ่มต้นสำหรับลูกค้าที่ต้องการ "เชื่อมต่อจุด" ระหว่างการรวมแบบสองทิศทาง Supply Chain Management และพอร์ทัล Power Apps หากคุณติดตั้งเว็บไซต์ที่ทำหน้าที่เป็นจุดประสงค์นี้ไว้แล้ว คุณอาจไม่ได้รับประโยชน์มากนักจากการใช้แม่แบบพอร์ทัลลูกค้า เพื่อจัดเตรียมเว็บไซต์นั้นใหม่อีกครั้ง

## <a name="how-does-it-work"></a>สิ่งนี้ทำงานอย่างไร

พอร์ทัลลูกค้าถูกส่งมาในรูปแม่แบบพอร์ทัล Power Apps ขึ้นอยู่กับพอร์ทัล Power Apps และการรวมแบบสองทิศทาง

[พอร์ทัล Power Apps](https://docs.microsoft.com/powerapps/maker/portals/overview) คือคุณลักษณะที่ช่วยให้ผู้ใช้สามารถสร้างเว็บไซต์ที่เชื่อมต่อกับภายนอก ที่ผู้ใช้จากภายนอกองค์กรสามารถล็อกอินเข้าได้ แทบจะไม่จำเป็นต้องมีการเขียนโค้ดเพื่อสร้างพอร์ทัล พอร์ทัลลูกค้าเป็นหนึ่งใน [แม่แบบ Dynamics 365](https://docs.microsoft.com/powerapps/maker/portals/portal-templates#environment-with-model-driven-apps-in-dynamics-365) ซึ่งพร้อมใช้งานจาก Microsoft

[การรวมแบบสองทิศทาง](https://docs.microsoft.com/powerapps/maker/portals/overview) เป็นผลิตภัณฑ์โครงสร้างพื้นฐานแบบสำเร็จรูปที่ให้การโต้ตอบแบบใกล้เรียลไทม์ระหว่างแอป Customer Engagement และแอป Finance and Operations การรวมแบบสองทิศทางมอบการรวมแบบสองทิศทางระหว่างแอป Finance and Operations และ Microsoft Dataverse ดังนั้น นี่จะให้ประสบการณ์ผู้ใช้แบบรวมทั่วทั้งแอป พอร์ทัลลูกค้าจะขึ้นอยู่กับตารางที่ซิงค์กับการรวมแบบสองทิศทาง ก่อนที่จะมีการใช้ข้อมูลจาก Supply Chain Management ในพอร์ทัลของลูกค้า จะต้องมีการเปิดใช้งานการรวมแบบสองทิศทางสำหรับตารางที่เหมาะสมทั้งหมด

![ความเชื่อมโยงของพอร์ทัลลูกค้า](media/customer-portal-elements.png "ความเชื่อมโยงของพอร์ทัลลูกค้า")

พอร์ทัลลูกค้าทำหน้าที่เป็นจุดเริ่มต้นสำหรับองค์กรที่ต้องการใช้พอร์ทัล Power Apps เพื่อสร้างเว็บไซต์ที่เชื่อมต่อกับภายนอก ซึ่งใช้ข้อมูลจากการติดตั้ง Supply Chain Management โดยจะช่วยให้องค์กรเชื่อมโยง การรวมแบบสองทิศทาง Supply Chain Management และพอร์ทัล Power Apps
