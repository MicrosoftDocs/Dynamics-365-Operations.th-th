---
title: ปัญหาที่พบเกี่ยวกับการผสานโครงสร้างพื้นฐาน Dynamics 365 Human Resources
description: บทความนี้แสดงรายการปัญหาที่อาจเกิดขึ้นในระหว่างการผสานโครงสร้างพื้นฐานของ Microsoft Dynamics 365 Human Resources
author: twheeloc
ms.date: 10/27/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-10-13
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 5f5981801317ad9647f57a0f68f9b67b592256ab
ms.sourcegitcommit: f96e5dec5a808d9819d2a23b8e15ce00aeff475b
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 11/10/2022
ms.locfileid: "9752702"
---
# <a name="dynamics-365-human-resources-infrastructure-merge-known-issues"></a>ปัญหาที่พบเกี่ยวกับการผสานโครงสร้างพื้นฐาน Dynamics 365 Human Resources

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]
[!include [preview banner](../includes/preview-banner.md)]

## <a name="shared-dataverse-environments"></a>สภาพแวดล้อม Dataverse ที่แบ่งปัน

กรอบงานการรวมแบบสองทิศทางไม่สนับสนุนการเชื่อมโยงสภาพแวดล้อมแอปการเงินและการดําเนินงานสองสภาพแวดล้อมกับสภาพแวดล้อม Dataverse เดียวกัน ถ้าคุณมีสภาพแวดล้อม Dataverse ที่ใช้ร่วมกันกับรายการทั้งสองรายการต่อไปนี้ คุณต้องคัดลอกสภาพแวดล้อม Dataverse หรือแบ่ง:

- แอปการเงินและการดำเนินงาน
- สภาพแวดล้อม Human Resources ปัจจุบัน

## <a name="environment-type-requirements"></a>ความต้องการชนิดสภาพแวดล้อม

ชนิดของสภาพแวดล้อมต่อไปนี้จำเป็นต้องระบุก่อนจึงจะสามารถทำการย้ายได้:

- ถ้าคุณไม่มีสภาพแวดล้อมแบบสแตนด์อโลนแบบ Sandbox คุณต้องสร้างใหม่เพื่อตรวจสอบความถูกต้องของการย้าย
- ถ้าคุณมีสภาพแวดล้อมแบบสแตนด์อโลนของการทำงานจริงหลายสภาพแวดล้อม คุณสามารถย้ายสภาพแวดล้อมใดสภาพแวดล้อมหนึ่งได้ ติดต่อฝ่ายสนับสนุนของ Microsoft เพื่ออให้ทำเครื่องหมายสภาพแวดล้อมเป็น Sandbox

## <a name="teams-integration"></a>การรวม Teams

แอป Human Resources ที่มีอยู่ใน Teams ที่กำลังเลื่อนไปยังโซลูชัน Microsoft Power Platform อยู่ในขณะนี้ สำหรับข้อมูลเพิ่มเติม ดูที่ [แอป Human Resources ใน Teams](hr-admin-teams-leave-app.md)

