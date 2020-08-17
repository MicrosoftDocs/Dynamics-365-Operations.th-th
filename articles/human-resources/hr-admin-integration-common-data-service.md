---
title: ตั้งค่าคอนฟิกการรวม Common Data Service
description: คุณสามารถเปิดหรือปิดการรวม Common Data Service กับ Dynamics 365 Human Resources นอกจากนี้คุณยังสามารถดูรายละเอียดของการซิงโครไนส์ ลบข้อมูลการติดตาม และรีซิงค์เอนทิตี้เพื่อช่วยในการแก้ไขปัญหาข้อมูลระหว่างสภาพแวดล้อมของทั้งสองได้
author: andreabichsel
manager: AnnBe
ms.date: 07/27/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: CDSIntegrationAdministration
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 8cbead2961c4576a5394080aae2fec109bce3f10
ms.sourcegitcommit: 4a981ee4be6d7e6c0e55541535d386bce2565cba
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 07/27/2020
ms.locfileid: "3621315"
---
# <a name="configure-common-data-service-integration"></a>ตั้งค่าคอนฟิกการรวม Common Data Service

คุณสามารถเปิดหรือปิดการรวม Common Data Service กับ Dynamics 365 Human Resources นอกจากนี้คุณยังสามารถดูรายละเอียดของการซิงโครไนส์ ข้อมูลการติดตาม และรีซิงค์เอนทิตี้ที่จะช่วยในการแก้ไขปัญหาข้อมูลระหว่างสภาพแวดล้อมสองอย่างได้

เมื่อคุณปิดการรวม ผู้ใช้สามารถทำการเปลี่ยนแปลงในทรัพยากรบุคคลหรือ Common Data Service แต่การเปลี่ยนแปลงดังกล่าวจะไม่มีการซิงค์ระหว่างสภาพแวดล้อมทั้งสอง

ตามค่าเริ่มต้น การรวมข้อมูลระหว่างทรัพยากรบุคคลและ Common Data Service จะถูกปิดไว้

คุณอาจต้องการปิดการรวมในสถานการณ์เหล่านี้:

- คุณกำลังกรอกข้อมูลโดยใช้กรอบงานการจัดการข้อมูลและต้องนำเข้าข้อมูลหลายครั้งเพื่อให้ได้รับเป็นสถานะที่ถูกต้อง

- แต่ก็ยังมีปัญหากับข้อมูลในทรัพยากรบุคคลหรือ Common Data Service อย่างใดอย่างหนึ่ง ถ้าคุณปิดการรวมคุณสามารถลบเรกคอร์ดในสภาพแวดล้อมหนึ่งได้โดยไม่ต้องลบเรกคอร์ดนั้นออกจากเรกคอร์ดอื่น เมื่อคุณเปิดการรวมกลับขึ้นมา เรกคอร์ดในสภาพแวดล้อมที่ไม่มีการลบออกจะซิงค์กลับไปยังสภาพแวดล้อมที่มีการลบออก การซิงโครไนส์เริ่มต้นในครั้งถัดไปที่มีการรวม **Common Data Service ที่พลาดการซิงค์** การร้องขอรันชุดงาน

> [!WARNING]
> เมื่อคุณปิดการรวมข้อมูลโปรดตรวจสอบให้แน่ใจว่าคุณไม่ได้แก้ไขเรกคอร์ดที่เหมือนกันในสภาพแวดล้อมทั้งสอง เมื่อคุณเปิดการรวมกลับขึ้นมา เรกคอร์ดที่คุณแก้ไขครั้งสุดท้ายจะถูกซิงค์ ดังนั้น ถ้าคุณไม่ได้ทำการเปลี่ยนแปลงที่เหมือนกันบนเรกคอร์ดในสภาพแวดล้อมทั้งสอง การสูญเสียข้อมูลอาจเกิดขึ้น

## <a name="access-the-common-data-service-integration-page"></a>เข้าถึงหน้าการรวม Common Data Service

1. ในอินสแตนซ์ทรัพยากรบุคคลซึ่งคุณต้องการดูหรือตั้งค่าคอนฟิกการตั้งค่าสำหรับการรวมกับ Common Data Service เลือกไทล์ **การจัดการระบบ**

    [![ไทล์การจัดการระบบ](./media/hr-select-system-administration.png)](./media/hr-select-system-administration.png)

2. เลือกแท็บ **ลิงค์**

    [![แท็บลิงค์](./media/hr-system-administration-links.png)](./media/hr-system-administration-links.png)

3. ภายใต้ **การรวม** เลือก **การตั้งค่าคอนฟิก Common Data Service**

    [![Common Data Service ลิงค์การตั้งค่าคอนฟิก](./media/hr-select-common-data-service-configuration.png)](./media/hr-select-common-data-service-configuration.png)

## <a name="turn-data-integration-between-human-resources-and-common-data-service-on-or-off"></a>เปิดหรือปิดการรวมข้อมูลระหว่างทรัพยากรบุคคลและ Common Data Service

- เมื่อต้องการเปิดการรวมให้ตั้งค่า **การเปิดใช้การรวมสำหรับตัวเลือก Common Data Service** เป็น **ใช่**

    > [!NOTE]
    > เมื่อคุณเปิดการรวม ข้อมูลจะถูกซิงค์ในครั้งถัดไปที่การรวม **Common Data Service พลาดการซิงค์** รันชุดงาน ข้อมูลทั้งหมดควรพร้อมใช้งานหลังจากชุดงานเสร็จสมบูรณ์

- เมื่อต้องการปิดใช้งานการรวมให้ตั้งตัวเลือกเป็น **ไม่**

[![การเปิดหรือปิด Common Data Service](./media/hr-enable-or-disable-common-data-service-integration.png)](./media/hr-enable-or-disable-common-data-service-integration.png)

> [!WARNING]
> เราขอแนะนำให้ปิดการรวม Common Data Service ในขณะที่ทำงานการย้ายข้อมูล การอัพโหลดข้อมูลขนาดใหญ่อาจส่งผลกระทบต่อประสิทธิภาพการทำงานได้อย่างมาก ตัวอย่างเช่นการอัพโหลดผู้ปฏิบัติงาน 2000 คน สามารถใช้เวลาหลายชั่วโมงเมื่อมีการเปิดใช้งานการรวม และน้อยกว่าหนึ่งชั่วโมงเมื่อปิดใช้งาน ตัวเลขที่ระบุในตัวอย่างนี้ใช้เพื่อวัตถุประสงค์ในการสาธิตเท่านั้น จำนวนเวลาที่ใช้ในการนำเข้าเรกคอร์ดมีความแตกต่างกันอย่างมากตามปัจจัยหลายอย่าง

## <a name="view-data-integration-details"></a>ภาพรวมของรายละเอียดการรวมข้อมูล

บนแท็บด่วน **การจัดการ** ของหน้า **การรวม Common Data Service** คุณสามารถดูวิธีการเชื่อมโยงเรกคอร์ดร่วมกันระหว่างทรัพยากรบุคคลและ Common Data Service

- ถ้าต้องการดูเรกคอร์ดสำหรับเอนทิตี้ให้เลือกเอนทิตี้ในฟิลด์ **ชื่อเอนทิตี้ CDS** กริดแสดงเรกคอร์ดทั้งหมดที่เชื่อมโยงกับเอนทิตี้ที่เลือก

[![การดูเรกคอร์ดสำหรับเอนทิตี้](./media/hr-common-data-service-configuration-view-entity.png)](./media/hr-common-data-service-configuration-view-entity.png)

> [!NOTE]
> ไม่ใช่เอนทิตี้ Common Data Service ทั้งหมดที่แสดงอยู่ในปัจจุบัน เฉพาะเอนทิตี้ที่สนับสนุนการใช้ฟิลด์ที่กำหนดเองเท่านั้นที่จะปรากฏในกริด เอนทิตี้ใหม่จะพร้อมใช้งานโดยผ่านการเผยแพร่ของทรัพยากรบุคคลอย่างต่อเนื่อง

กริดประกอบด้วยฟิลด์ต่อไปนี้:

- **ชื่อของเอนทิตี้ CDS** – ชื่อของเอนทิตี้ใน Common Data Service
- **การอ้างอิงเอนทิตี้ CDS** – ตัวระบุที่ Common Data Service ใช้ในการระบุเรกคอร์ด ค่านี้เทียบเท่ากับค่า **RecId** ของทรัพยากรบุคคล คุณสามารถค้นหาตัวระบุเมื่อคุณเปิดเอนทิตี้ Common Data Service ใน Microsoft Excel
- **ชื่อเอนทิตี้ทรัพยากรบุคคล** – เอนทิตี้ที่มีการซิงค์ข้อมูลครั้งล่าสุดกับ Common Data Service เอนทิตี้สามารถมีคำนำหน้า Common Data Service หรือคำนำหน้าอื่น
- **การอ้างอิงทรัพยากรบุคคล** – ค่า **RecId** ที่เชื่อมโยงกับเรกคอร์ดในทรัพยากรบุคคล
- **ลบออกจาก CDS แล้ว** – ค่าที่บ่งชี้ว่าเรกคอร์ดถูกลบออกจาก Common Data Service หรือไม่

## <a name="remove-the-association-of-a-record-in-human-resources-from-common-data-service"></a>ลบการเชื่อมโยงของเรกคอร์ดในทรัพยากรบุคคลออกจาก Common Data Service

ถ้าคุณประสบปัญหาในระหว่างการซิงโครไนส์ข้อมูลระหว่างทรัพยากรบุคคลและ Common Data Service คุณอาจสามารถแก้ไขปัญหาเหล่านั้นได้ด้วยการล้างการติดตามและปล่อยให้ตารางการติดตามถูกรีซิงค์ ถ้าคุณลบการเชื่อมโยงออกแล้วเปลี่ยนหรือลบเรกคอร์ดใน Common Data Service การเปลี่ยนแปลงจะไม่ถูกซิงค์กับทรัพยากรบุคคล ถ้าคุณทำการเปลี่ยนแปลงในทรัพยากรบุคคลเรกคอร์ดการติดตามใหม่จะถูกสร้างขึ้นและเรกคอร์จะถูกอัพเดตใน Common Data Service

- เมื่อต้องการลบการเชื่อมโยงของเรกคอร์ดระหว่างทรัพยากรบุคคลและ Common Data Service เลือกเอนทิตี้ในฟิลด์ **ชื่อเอนทิตี้ CDS** แล้วเลือก **ล้างข้อมูลการติดตาม**

[![การล้างข้อมูลการติดตาม](./media/hr-common-data-service-configuration-clear-tracking.png)](./media/hr-common-data-service-configuration-clear-tracking.png)

เมื่อต้องการรันการซิงโครไนส์แบบสมบูรณ์บนเอนทิตี้หลังจากที่คุณล้างการติดตามแล้วให้ดูที่กระบวนงานถัดไป

## <a name="sync-an-entity-between-human-resources-and-common-data-service"></a>ซิงค์เอนทิตี้ระหว่างทรัพยากรบุคคลและ Common Data Service

ใช้ขั้นตอนนี้เมื่อ:

- การเปลี่ยนแปลงจาก Common Data Service ใช้เวลานานเกินไปกว่าที่จะปรากฏในทรัพยากรบุคคล

- คุณต้องรีเฟรชตารางการติดตามหลังจากล้างการติดตาม

เมื่อต้องการรันการซิงโครไนส์ทั้งหมดในเอนทิตี้ระหว่างทรัพยากรบุคคลและ Common Data Service:

1. เลือกเอนทิตี้ในฟิลด์ **ชื่อเอนทิตี้ CDS**

2. เลือก **ซิงค์เดี๋ยวนี้**

[![การรันการซิงโครไนส์แบบสมบูรณ์](./media/hr-common-data-service-configuration-sync-now.png)](./media/hr-common-data-service-configuration-sync-now.png)


