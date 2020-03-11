---
title: คุณลักษณะแพลตฟอร์มที่ถูกลบออกหรือเลิกสนับสนุน
description: หัวข้อนี้อธิบายคุณลักษณะที่ถูกลบออก หรือที่วางแผนไว้ว่าจะลบออกจากการอัปเดตแพลตฟอร์มของแอป Finance and Operations
author: sericks007
manager: AnnBe
ms.date: 02/25/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: sericks
ms.search.scope: Operations
ms.search.region: Global
ms.author: sericks
ms.search.validFrom: 2020-02-29
ms.dyn365.ops.version: Platform update 33
ms.openlocfilehash: 66e1420c7053c0df9f42b15c55aba1a8c869f02a
ms.sourcegitcommit: 2cc3b89efdd90f8d80883b7a271d7885282ba3e8
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 02/26/2020
ms.locfileid: "3087894"
---
# <a name="removed-or-deprecated-platform-features"></a>คุณลักษณะแพลตฟอร์มที่ถูกลบออกหรือเลิกสนับสนุน

[!include [banner](../includes/banner.md)]

หัวข้อนี้อธิบายคุณลักษณะที่ถูกลบออก หรือที่วางแผนไว้ว่าจะลบออกจากการอัปเดตแพลตฟอร์มของแอป Finance and Operations

- คุณลักษณะที่ *ถูกลบ* จะไม่พร้อมใช้งานในผลิตภัณฑ์อีกต่อไป
- คุณลักษณะที่ *ถูกยกเลิกการใช้* ไม่ได้อยู่ในการพัฒนาที่ใช้งานอยู่ และอาจถูกลบออกในการปรับปรุงในอนาคต

รายการนี้มีไว้เพื่อช่วยคุณพิจารณาการลบออกและการยกเลิกการใช้งานเหล่านี้สำหรับการวางแผนของคุณเอง 

> [!NOTE]
> ข้อมูลโดยละเอียดเกี่ยวกับออบเจ็กต์ต่างๆ ในแอป Finance and Operations พบได้ใน [รายงานอ้างอิงทางเทคนิค](https://mbs.microsoft.com/customersource/northamerica/AX/downloads/reports/axtechrefrep) คุณสามารถเปรียบเทียบเวอร์ชันต่างๆ ของรายงานเหล่านี้ เพื่อเรียนรู้เกี่ยวกับออบเจ็กต์ที่เปลี่ยนแปลงหรือถูกลบออกในแต่ละรุ่นของแอป Finance and Operations

## <a name="platform-update-32"></a>แพลตฟอร์ม update 32

### <a name="workflow-request-change-dialog-box-no-longer-includes-user-selection-drop-down-list"></a>กล่องโต้ตอบการเปลี่ยนแปลงคำขอของลำดับงานไม่รวมรายการแบบหล่นลงของการเลือกผู้ใช้ไว้อีกต่อไป
|   |  |
|------------|--------------------|
| **เหตุผลสำหรับการยกเลิกการใช้/การลบ** | นี่เป็นปัญหาด้านความปลอดภัยเนื่องจากไม่สามารถส่งคำขอเปลี่ยนแปลงไปยังผู้ใช้ที่ไม่ได้จัดทำขึ้น นี่ยังเป็นปัญหาของการใช้ เนื่องจากมีการนำผู้ใช้นี้ไปใช้ในการกำหนดผู้ริเริ่มลำดับงานและเลือกด้วยตนเอง  |
| **แทนที่ด้วยลักษณะการทำงานอื่นหรือไม่**   | ไม่ |
| **พื้นที่ของผลิตภัณฑ์ที่ได้รับผล**         | ลำดับงาน |
| **ตัวเลือกการปรับใช้**              | ทั้งหมด |
| **สถานะ**                         | รายการแบบหล่นลงของการเลือกผู้ใช้ถูกลบออกจากกล่องโต้ตอบการเปลี่ยนแปลงคำขอในการอัปเดตแพลตฟอร์มที่ 32 การร้องขอการเปลี่ยนแปลงคำขอจะถูกส่งไปยังผู้ริเริ่มโดยอัตโนมัติตามที่จัดทำขึ้นไว้ สำหรับข้อมูลเพิ่มเติมเกี่ยวกับฟังก์ชันนี้ ให้ดูที่ [การดำเนินการในกระบวนการอนุมัติลำดับงาน](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/organization-administration/workflow-actions?toc=%2Fdynamics365%2Fcommerce%2Ftoc.json#request-change) |

## <a name="previous-announcements-about-removed-or-deprecated-features"></a>ประกาศก่อนหน้านี้เกี่ยวกับคุณลักษณะที่ถูกลบหรือเลิกสนับสนุน
เมื่อต้องการเรียนรู้เพิ่มเติมเกี่ยวกับคุณลักษณะที่ถูกลบออกหรือเลิกสนับสนุนในรุ่นก่อนหน้านี้ ให้ดูที่ [คุณลักษณะที่ถูกลบออกหรือเลิกสนับสนุนในรุ่นก่อนหน้านี้](../migration-upgrade/deprecated-features.md)

