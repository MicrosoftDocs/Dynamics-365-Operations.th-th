---
title: ปฏิทินและการจัดกำหนดการเจ้าหน้าที่บำรุงรักษา
description: หัวข้อนี้จะอธิบายถึงปฏิทินของเจ้าหน้าที่บำรุงรักษาโดยสัมพันธ์กับการจัดกำหนดการในการจัดการสินทรัพย์
author: josaw1
manager: AnnBe
ms.date: 08/19/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: aa2d50a976af7ee7dde5335f94336b995fdc2d11
ms.sourcegitcommit: fb66731f05207094149a6bc7b8549a4dabbb071a
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 10/22/2019
ms.locfileid: "2652068"
---
# <a name="maintenance-worker-calendar-and-scheduling"></a>ปฏิทินและการจัดกำหนดการเจ้าหน้าที่บำรุงรักษา

[!include [banner](../../includes/banner.md)]

 

เมื่อคุณจัดกำหนดการใบสั่งงาน คุณสร้างกำหนดการสำหรับเจ้าหน้าที่บำรุงรักษา เครื่องมือ และสินทรัพย์ เพื่อที่จะจัดกำหนดการเจ้าหน้าที่บำรุงรักษา จะต้องมีการตั้งค่าปฏิทินสำหรับเจ้าหน้าที่บำรุงรักษาแต่ละคน เจ้าหน้าที่บำรุงรักษาเกี่ยวข้องกับทรัพยากร และปฏิทินเวลาการทำงานถูกตั้งค่าสำหรับทรัพยากร คุณตั้งค่าทรัพยากรและปฏิทินใน **การจัดการสินทรัพย์** > **การตั้งค่า** > **ผู้ปฏิบัติงาน** > **ผู้ปฏิบัติงาน** ซึ่งอธิบายไว้ใน [เจ้าหน้าที่บำรุงรักษาและกลุ่มผู้ปฏิบัติงาน](../setup-for-objects/workers-and-worker-groups.md)

ภาพหน้าจอด้านล่างแสดงตัวอย่างของเจ้าหน้าที่บำรุงรักษาที่เกี่ยวข้องกับทรัพยากรที่ใช้ปฏิทินเวลาการทำงาน "การผลิต"

![รูปที่ 1](media/01-work-order-scheduling.png)

ไม่จำเป็นต้องมีการตั้งค่าปฏิทินสำหรับเครื่องมือและสินทรัพย์โดยสัมพันธ์กับการจัดกำหนดการใบสั่งงาน สมมติฐานคือ เครื่องมือและสินทรัพย์พร้อมใช้งาน 24 ชั่วโมงต่อวันสำหรับการบำรุงรักษา

