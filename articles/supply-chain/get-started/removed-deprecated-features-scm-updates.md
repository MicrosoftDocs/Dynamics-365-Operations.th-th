---
title: คุณลักษณะที่เอาออกหรือเลิกสนับสนุนใน Dynamics 365 Supply Chain Management
description: หัวข้อนี้อธิบายคุณลักษณะที่ถูกลบออก หรือที่ถูกวางแผนไว้ว่าจะลบใน Dynamics 365 Supply Chain Management
author: kamaybac
manager: tfehr
ms.date: 04/30/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2020-03-03
ms.dyn365.ops.version: Platform update 33
ms.openlocfilehash: 07f37488747766dcca96884e204339b425bbd201
ms.sourcegitcommit: f64fce03ec52f844b05a9e8cac286cb201385002
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 07/16/2020
ms.locfileid: "3597127"
---
# <a name="removed-or-deprecated-features-in-dynamics-365-supply-chain-management"></a>คุณลักษณะที่เอาออกหรือเลิกสนับสนุนใน Dynamics 365 Supply Chain Management

[!include [banner](../includes/banner.md)]

หัวข้อนี้จะได้รับการปรับปรุง เมื่อมีการจัดทำเอกสารคุณลักษณะที่เอาออกหรือเลิกสนับสนุนใหม่สำหรับ Dynamics 365 Supply Chain Management

- คุณลักษณะที่ *ถูกลบ* จะไม่พร้อมใช้งานในผลิตภัณฑ์อีกต่อไป
- คุณลักษณะที่ *ถูกยกเลิกการใช้* ไม่ได้อยู่ในการพัฒนาที่ใช้งานอยู่ และอาจถูกลบออกในการปรับปรุงในอนาคต

รายการนี้มีไว้เพื่อช่วยคุณพิจารณาการลบออกและการยกเลิกการใช้งานเหล่านี้สำหรับการวางแผนของคุณเอง

> [!NOTE]
> ข้อมูลโดยละเอียดเกี่ยวกับออบเจ็กต์ต่างๆ ในแอป Finance and Operations พบได้ใน [รายงานอ้างอิงทางเทคนิค](https://mbs.microsoft.com/customersource/northamerica/AX/downloads/reports/axtechrefrep) คุณสามารถเปรียบเทียบเวอร์ชันต่างๆ ของรายงานเหล่านี้ เพื่อเรียนรู้เกี่ยวกับออบเจ็กต์ที่เปลี่ยนแปลงหรือถูกลบออกในแต่ละรุ่นของแอป Finance and Operations

## <a name="features-removed-or-deprecated-in-the-supply-chain-management-10011-release"></a>คุณลักษณะที่เอาออกหรือที่เลิกสนับสนุนในการนำออกใช้ Supply Chain Management 10.0.11

### <a name="use-of-built-in-supply-chain-management-master-planning-engine-for-distribution-scenarios"></a>การใช้กลไกจัดการการวางแผนหลักของ Supply Chain Management ในตัวสำหรับสถานการณ์จำลองการกระจาย

|   |  |
|------------|--------------------|
| **เหตุผลสำหรับการยกเลิกการใช้/การลบ** | เมื่อต้องการปรับปรุงประสิทธิภาพการทำงานและลดการโหลดฐานข้อมูล SQL ในระหว่างการรันการวางแผนหลัก ระบบการวางแผนหลักของ Supply Chain Management ที่มีอยู่แล้วจะถูกแทนที่ด้วยการเพิ่มประสิทธิภาพการวางแผน การเพิ่มประสิทธิภาพการวางแผนช่วยให้สามารถทำงานได้อย่างรวดเร็ว ซึ่งสามารถดำเนินการได้แม้กระทั่งในเวลาทำการ การทำเช่นนี้จะช่วยให้ผู้วางแผนสามารถตอบสนองต่อการเปลี่ยนแปลงในความต้องการหรือพารามิเตอร์การวางแผนได้ทันที |
| **แทนที่ด้วยลักษณะการทำงานอื่นหรือไม่**   | ใช่ การเพิ่มประสิทธิภาพของการวางแผนจะแทนที่กลไกจัดการการวางแผนหลักของ Supply Chain Management ในตัวที่มีอยู่แล้ว |
| **พื้นที่ของผลิตภัณฑ์ที่ได้รับผล**         | Supply Chain Management - การวางแผนหลัก |
| **ตัวเลือกการปรับใช้**              | ระบบ Cloud เท่านั้น การเพิ่มประสิทธิภาพการวางแผนไม่สนับสนุนการปรับใช้ในสถานที่ |
| **สถานะ**                         | ยกเลิกการใช้งาน ในเดือนเมษายน 2021 สถานการณ์จำลองการกระจายจะไม่ได้รับการสนับสนุนอีกต่อไปด้วยกลไกจัดการการวางแผนหลักของ Dynamics 365 Supply Chain Management ในตัว สำหรับสถานการณ์จำลองการกระจาย ลูกค้าต้องใช้การเพิ่มประสิทธิภาพการวางแผนสำหรับการคำนวณการวางแผนหลัก สำหรับข้อมูลเพิ่มเติมให้ดูที่ [เอกสารประกอบการปรับการเพิ่มประสิทธิภาพการวางแผน](https://go.microsoft.com/fwlink/?linkid=2105830) ลูกค้าที่มีการปรับใช้ในสถานที่ของ Dynamics 365 Supply Chain Management อาจดำเนินการต่อไปเพื่อใช้กลไกจัดการการวางแผนหลักของ Supply Chain Management สำหรับสถานการณ์การกระจายหลังจากเดือนเมษายน 2021 อย่างไรก็ตาม จะไม่มีการปรับปรุงลักษณะการทำงานเพิ่มเติม |

## <a name="previous-announcements-about-removed-or-deprecated-features"></a>ประกาศก่อนหน้านี้เกี่ยวกับคุณลักษณะที่ถูกลบหรือเลิกสนับสนุน

เมื่อต้องการเรียนรู้เพิ่มเติมเกี่ยวกับคุณลักษณะที่ถูกลบออกหรือเลิกสนับสนุนในรุ่นก่อนหน้านี้ ให้ดูที่ [คุณลักษณะที่ถูกลบออกหรือเลิกสนับสนุนในรุ่นก่อนหน้านี้](../../fin-ops-core/dev-itpro/migration-upgrade/deprecated-features.md)
