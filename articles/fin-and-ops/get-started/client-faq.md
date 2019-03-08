---
title: FAQ ไคลเอนต์ Finance and Operations
description: บทความนี้ให้คำตอบของคำถามที่ถามบ่อยเกี่ยวกับไคลเอ็นต์ Microsoft Dynamics 365 for Finance and Operations
author: jasongre
manager: AnnBe
ms.date: 10/23/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.custom: 12334
ms.assetid: a9a57f0e-a67c-46b1-83c9-5d6350fb3b86
ms.search.region: Global
ms.author: jasongre
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 74f85f7a1c390d1f21d0423a794ff16c7250d9fa
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 01/29/2019
ms.locfileid: "316728"
---
# <a name="finance-and-operations-client-faq"></a>FAQ ไคลเอนต์ Finance and Operations

[!include [banner](../includes/banner.md)]

บทความนี้ให้คำตอบของคำถามที่ถามบ่อยเกี่ยวกับไคลเอ็นต์ Microsoft Dynamics 365 for Finance and Operations

## <a name="why-arent-symbols-loaded-when-i-use-finance-and-operations"></a>เพราะเหตุใดสัญลักษณ์จึงไม่โหลดเมื่อฉันใช้ Finance and Operations

การตั้งค่าความปลอดภัยในเบราเซอร์ของคุณอาจป้องกันสัญลักษณ์จากการถูกโหลดอย่างถูกต้อง เพื่อแก้ไขปัญหานี้ ทำตามขั้นตอนต่อไปนี้:

- ถ้าคุณกำลังพบกับปัญหานี้ใน Internet Explorer คลิก **เครื่องมือ** และจากนั้น คลิก **ตัวเลือกอินเตอร์เน็ต** ในกล่องโต้ตอบตัวเลือกอินเทอร์เน็ต บนแท็บ **ความเป็นส่วนตัว** คลิก **ระดับแบบกำหนดเอง** และตรวจสอบให้แน่ใจว่าตัวเลือก **ดาวน์โหลดแบบอักษร** ได้ถูกเลือก
- มิฉะนั้น คุณอาจต้องเพิ่มไซต์ Finance and Operations ลงในรายการไซต์ที่เชื่อถือ

## <a name="i-miss-the-ribbon-from-dynamics-ax-2012-can-i-keep-action-pane-tabs-open-all-the-time"></a>ฉันคิดถึงริบบอนจาก Dynamics AX 2012 ฉันสามารถรักษาแท็บบานหน้าต่างการดำเนินการให้เปิดตลอดเวลาได้หรือไม่

เรากำลังวางแผนจะใช้คุณลักษณะนี้ในเร็วๆ นี้ ผู้ใช้สามารถเลือกเพื่อรักษาแท็บในบานหน้าต่างการดำเนินการเปิดตลอดเวลา มิฉะนั้น แท็บจะสามารถยุบเมื่อไม่ได้กำลังใช้งาน เพื่อเข้าใช้พื้นที่หน้าจอเพิ่มเติมสำหรับหน้านั้น

## <a name="why-do-i-sometimes-see-different-shortcut-menus-when-i-right-click"></a>เหตุใดบางครั้งฉันเห็นเมนูทางลัดที่แตกต่างกัน เมื่อฉันคลิกขวา?

ถ้าคุณคลิกขวาในฟิลด์แก้ไขได้ (หรือ ถ้าข้อความถูกเลือก), เมนูทางลัดของเบราเซอร์จะแสดงขึ้น เมนูนี้ช่วยให้คุณเข้าถึงคำสั่ง **ตัด**, **สำเนา**และ **วาง** เราไม่สามารถฝังคำสั่งเหล่านี้ลงในเมนูทางลัด Finance and Operations ได้ เนื่องจากเหตุผลด้านความปลอดภัย เบราเซอร์ไม่อนุญาตให้เราเข้าถึงคลิปบอร์ดระบบทางโปรแกรม

ถ้าคุณคลิกขวาที่ป้ายชื่อฟิลด์หรือค่าของตัวควบคุมแบบอ่านอย่างเดียว คุณจะเห็นเมนูทางลัด Finance and Operations

เพื่อให้เข้าถึงแป้นพิมพ์ได้ง่าย เราวางแผนจะใช้แป้นพิมพ์ลัดในอนาคตซึ่งจะเปิดเมนูทางลัด Finance and Operations

## <a name="where-is-the-view-details-functionality-in-finance-and-operations"></a>ฟังก์ชันดูรายละเอียดใน Finance and Operations อยู่ที่ใด

ตัวเลือก **ดูรายละเอียด** จะพร้อมใช้งานในสองวิธี:

- หากส่วนควบคุมมีความสามารถในการ **ดูรายละเอียด**และถ้าตัวควบคุมมีค่า ค่านั้นจะแสดงเป็นไฮเปอร์ลิงค์ คุณสามารถคลิกไฮเปอร์ลิงค์เพื่อเปิดหน้าซึ่งประกอบด้วยรายละเอียดเพิ่มเติม
- **ดูรายละเอียด** เป็นตัวเลือกบนเมนูทางลัด Finance and Operations สำหรับข้อมูลเพิ่มเติมเกี่ยวกับเมนูทางลัด Finance and Operations จะแสดงขึ้นเมื่อคุณคลิกขวา โปรดดูส่วนก่อนหน้านี้
