---
title: วางแผนเส้นทางสำหรับการขนส่งค่าขนส่งที่มีจุดหยุดหลายแห่ง
description: บทความนี้อธิบายองค์ประกอบต่างๆ ที่คุณใช้วางแผนเส้นทางการเดินทางใน Dynamics 365 Supply Chain Management
author: Weijiesa
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: TMSHubMaster, TMSLoadBuildTemplates, TMSRateRouteWorkbench, TMSRouteGuide, TMSRoutePlan, TMSRouteWorkbench, WHSLoadTemplate, TMSRouteSchedule, TMSRouteRateDetail
audience: Application User
ms.reviewer: kamaybac
ms.custom: 90013
ms.assetid: 50d6f58c-f1c8-4321-9e83-8445cec57a85
ms.search.region: Global
ms.author: weijiesa
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 7e3d316b5bed67e84fdd5cec8b518069c053436d
ms.sourcegitcommit: 9166e531ae5773f5bc3bd02501b67331cf216da4
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 05/03/2022
ms.locfileid: "8671604"
---
# <a name="plan-freight-transportation-routes-with-multiple-stops"></a>วางแผนเส้นทางสำหรับการขนส่งค่าขนส่งที่มีจุดหยุดหลายแห่ง

[!include [banner](../includes/banner.md)]

บทความนี้อธิบายองค์ประกอบต่างๆ ที่คุณใช้วางแผนเส้นทางการเดินทางใน Dynamics 365 Supply Chain Management

คุณสามารถใช้แผนการกระบวนการผลิตและคู่มือกระบวนการผลิตสำหรับเส้นทางการขนส่งที่ซับซ้อนที่มีจุดหยุดหลายแห่ง ถ้าเส้นทางเดียวกันจะถูกนำมาใช้เป็นประจำ คุณสามารถตั้งค่ากระบวนการผลิตที่จัดกำหนดการ

## <a name="route-plans"></a>แผนกระบวนการผลิต
แผนการกระบวนการผลิตประกอบด้วยเซ็กเมนต์กระบวนการผลิตที่แสดงข้อมูลเกี่ยวกับจุดหยุดที่มีการเข้าชมในเส้นทางนั้นและผู้ขนส่งที่ใช้สำหรับแต่ละเซ็กเมนต์ คุณต้องกำหนดจุดหยุดในเส้นทางเป็นฮับ ฮับสามารถเป็นผู้จัดจำหน่าย คลังสินค้า ลูกค้า หรือแม้แต่เป็นเพียงสถานที่โหลดใหม่ซึ่งคุณสามารถเปลี่ยนผู้ขนส่งได้ สำหรับแต่ละเซ็กเมนต์ คุณสามารถกำหนด "ราคาซื้อขายทันที" สำหรับค่าธรรมเนียมต่างๆ ยกตัวอย่างเช่น

-   ค่าธรรมเนียมสำหรับการเดินทางไปยังเซ็กเมนต์ที่กำหนด
-   ค่าธรรมเนียมสำหรับการเบิกสินค้า
-   ค่าธรรมเนียมสำหรับการปล่อยสินค้า

แผนการกระบวนการผลิตแต่ละแผนจะต้องเชื่อมโยงกับคู่มือกระบวนการผลิต

## <a name="route-guides"></a>คำแนะนำกระบวนการผลิต
คู่มือกระบวนการผลิตเป็นตัวกำหนดเกณฑ์สำหรับการจับคู่การบรรทุกกับแผนการกระบวนการผลิตหนึ่งๆ ตัวอย่างเช่น คุณสามารถระบุฮับต้นทางและฮับปลายทาง ขีดจำกัดสำหรับปริมาณหรือน้ำหนักของตู้บรรจุสินค้า และผู้ขนส่งสินค้า บริการขนส่งสินค้า หรือกลุ่มขนส่งสินค้า สามารถดูคู่มือกระบวนการผลิตได้ในหน้า **เวิร์กเบนช์อัตราและกระบวนการผลิต** ซึ่งสามารถจับคู่การบรรทุกกับกระบวนการผลิตด้วยตนเองหรือโดยอัตโนมัติได้ ถ้าคู่มือกระบวนการผลิตมีไว้สำหรับกระบวนการผลิตที่จัดกำหนดการ จะมีอยู่ในหน้า **เวิร์กเบนช์การสร้างการบรรทุก** ด้วยเช่นกัน

## <a name="scheduled-routes"></a>กระบวนการผลิตที่จัดกำหนดการ
กระบวนการผลิตที่จัดกำหนดการคือแผนการกระบวนการผลิตที่กำหนดไว้ล่วงหน้าที่มีกำหนดการสำหรับวันที่จัดส่ง กระบวนการผลิตที่จัดกำหนดการและกระบวนการผลิตที่ไม่ได้จัดกำหนดการมีความแตกต่างกันในลักษณะที่ว่ามีการบรรทุกที่ถูกกำหนดให้ ถ้าคุณกำหนดกระบวนการผลิตที่ไม่ได้จัดกำหนดการโดยใช้เวิร์กเบนช์อัตราและกระบวนการผลิต จะสามารถใช้ได้เฉพาะการบรรทุกและคู่มือกระบวนการผลิตเท่านั้น ถ้าคุณกำหนดกระบวนการผลิตที่จัดกำหนดการ จะพิจารณาวันและที่อยู่จากใบสั่งและฮับ และวันที่ในแผนการกระบวนการผลิตด้วย คุณไม่จำเป็นต้องใช้หน้าเวิร์กเบนช์อัตราและกระบวนการผลิตในการกำหนดการบรรทุกไปยังกระบวนการผลิตที่จัดกำหนดการด้วยตนเอง แต่คุณสามารถใช้เวิร์กเบนช์การสร้างการบรรทุกในการแนะนำให้การบรรทุกถูกสร้างขึ้นตามที่อยู่ของลูกค้าและวันจัดส่งจากใบสั่งขายสำหรับกระบวนการผลิตที่จัดกำหนดการที่ระบุ สำหรับกระบวนการผลิตที่จัดกำหนดการ แผนการกระบวนการผลิตจะมีฮับต้นทางและปลายทางที่แน่นอน โดยทั่วไป ผู้ขนส่งสินค้าและบริการขนส่งสินค้าจะเหมือนกันสำหรับเซ็กเมนต์ทั้งหมด แต่สามารถแตกต่างกันไปได้เช่นกัน ฮับปลายทางถูกสร้างขึ้นโดยใช้รหัสไปรษณีย์ของลูกค้าที่ได้เข้าเยี่ยมชมในกระบวนการผลิต คุณสามารถกำหนดกระบวนการผลิตที่จัดกำหนดการหลายรายการสำหรับแผนการกระบวนการผลิตเดียว แผนการกระบวนการผลิตนั้นๆ จะต้องเชื่อมโยงกับคู่มือกระบวนการผลิต อย่างไรก็ตาม สำหรับกระบวนการผลิตที่จัดกำหนดการ แผนการสามารถเชื่อมโยงกับคู่มือกระบวนการผลิตได้เพียงรายการเดียวเท่านั้น กำหนดการกระบวนการผลิตจะใช้เฉพาะในการสร้างกระบวนการผลิตที่เกิดขึ้นจริงในหน้า **กำหนดการกระบวนการผลิต** คุณสามารถใช้เท็มเพลตการบรรทุกเริ่มต้นเมื่อคุณเสนอการบรรทุกบนเวิร์กเบนช์การสร้างการบรรทุก

## <a name="load-building-workbench"></a>เวิร์กเบนช์การสร้างการบรรทุก
เวิร์กเบนช์การสร้างการบรรทุกใช้ที่อยู่ของลูกค้าและวันจัดส่งจากใบสั่งขาย และกระบวนการผลิตที่จัดกำหนดการที่พร้อมใช้งานในการเสนอการบรรทุก โดยค่าเริ่มต้น ค่าจากกระบวนการผลิตจะถูกป้อนในเวิร์กเบนช์ อย่างไรก็ตาม คุณสามารถเลือก "จาก" วันที่ที่อยู่ก่อนหน้า "จาก" วันที่ในกระบวนการผลิต เมื่อมีการเสนอการบรรทุก ที่อยู่ที่จัดส่งและวันที่จัดส่งของใบสั่งขายที่เปิดอยู่ทั้งหมดจะถูกตรวจสอบ ถ้ารหัสไปรษณีย์ของที่อยู่ที่จัดส่งตรงกับรหัสไปรษณีย์ของฮับในแผนการกระบวนการผลิต และถ้าวันที่จัดส่งอยู่ภายในช่วงที่เลือกในเกณฑ์ ใบสั่งขายจะถูกเสนอสำหรับการบรรทุก นอกจากนี้ยังพิจารณากำลังของเท็มเพลตการบรรทุกอีกด้วย มีการเสนอการบรรทุกเพียงครั้งเดียวเท่านั้นในแต่ละครั้ง ถ้าคุณมีใบสั่งขายที่ไม่ได้รวมอยู่ด้วย คุณอาจจำเป็นต้องใช้เท็มเพลตการบรรทุกอื่น (ตัวอย่างเช่น เท็มเพลตการบรรทุกสำหรับรถบรรทุกหรือคอนเทนเนอร์ที่มีขนาดใหญ่ขึ้น) หรือวางแผนการจัดส่งพิเศษ





[!INCLUDE[footer-include](../../includes/footer-banner.md)]