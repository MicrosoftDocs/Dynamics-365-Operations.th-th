---
title: คู่มือการแก้ไขปัญหาสำหรับการรวมข้อมูล
description: ในหัวข้อนี้แสดงข้อมูลเกี่ยวกับการแก้ไขปัญหาในการรวมข้อมูลระหว่างแอป Finance and Operations กับ Common Data Service.
author: RamaKrishnamoorthy
manager: AnnBe
ms.date: 07/25/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2019-07-15
ms.openlocfilehash: 87bdb72024c1c3844ff61e832a92f7edcc77c5d6
ms.sourcegitcommit: 54baab2a04e5c534fc2d1fd67b67e23a152d4e57
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 02/04/2020
ms.locfileid: "3020041"
---
# <a name="troubleshooting-guide-for-data-integration"></a>คู่มือการแก้ไขปัญหาสำหรับการรวมข้อมูล

[!include [banner](../../includes/banner.md)]

[!include [preview-banner](../../includes/preview-banner.md)]

## <a name="enable-plug-in-trace-logs-in-common-data-service-and-inspect-the-dual-write-plug-in-error-details"></a>เปิดใช้ล็อกการติดตามปลั๊กอินใน Common Data Service และตรวจสอบรายละเอียดข้อผิดพลาดปลั๊กอินการเขียนแบบคู่

ถ้าคุณพบปัญหาหรือข้อผิดพลาดระหว่างการซิงโครไนส์การเขียนแบบคู่ ให้ทำตามขั้นตอนต่อไปนี้เพื่อตรวจสอบข้อผิดพลาดในล็อกการติดตาม

1. ก่อนที่คุณจะสามารถตรวจสอบข้อผิดพลาดได้ คุณต้องเปิดใช้งานล็อกการติดตามปลั๊กอิน สำหรับคำแนะนำ ให้ดูที่ส่วน "ดูล็อกการติดตาม" ของ [บทช่วยสอน: เขียนและลงทะเบียนปลั๊กอิน](https://docs.microsoft.com/powerapps/developer/common-data-service/tutorial-write-plug-in#view-trace-logs)

    ตอนนี้คุณสามารถตรวจสอบข้อผิดพลาดได้

2. ลงชื่อเข้าใช้ Microsoft Dynamics 365 Sales
3. เลือกปุ่ม **การตั้งค่า** (สัญลักษณ์เกียร์) แล้วจากนั้น เลือก **การตั้งค่าขั้นสูง**
4. ในเมนู **การตั้งค่า** เลือก **การเลือกกำหนด \> ล็อกการติดตามปลั๊กอิน**
5. เลือก **Microsoft.Dynamics.Integrator.CrmPlugins.Plugin** เป็นชื่อชนิด เพื่อแสดงรายละเอียดข้อผิดพลาด

## <a name="inspect-dual-write-synchronization-errors"></a>ตรวจสอบข้อผิดพลาดของการซิงโครไนส์การเขียนแบบสองครั้ง

ทำตามขั้นตอนต่อไปนี้เพื่อตรวจสอบข้อผิดพลาดในระหว่างการทดสอบ

1. ลงชื่อเข้าใช้ Microsoft Dynamics Lifecycle Services (LCS)
2. เปิดโครงการ LCS เพื่อทำการทดสอบการเขียนแบบคู่
3. เลือก **สภาพแวดล้อมที่โฮสต์ระบบคลาวด์**
4. ทำการเชื่อมต่อเดสก์ท็อประยะไกลกับแอพลิเคชั่นเครื่องเสมือน (VM) โดยใช้บัญชีภายในเครื่องที่แสดงอยู่ใน LCS
5. เปิดตัวแสดงเหตุการณ์ 
6. ไปยัง **ล็อกของแอพลิเคชันและบริการ \> Microsoft \> Dynamics \> AX-DualWriteSync \> การดำเนินงาน** ข้อผิดพลาดและรายละเอียดจะแสดงขึ้น

## <a name="unlink-one-common-data-service-environment-from-the-application-and-link-another-environment"></a>ยกเลิกการเชื่อมโยงสภาพแวดล้อม Common Data Service หนึ่งรายการจากแอพลิเคชันและเชื่อมโยงสภาพแวดล้อมอื่น

ทำตามขั้นตอนเหล่านี้เพื่อปรับปรุงการเชื่อมโยง

1. ไปที่ สภาพแวดล้องแอพลิเคชัน
2. เปิดการจัดการข้อมูล
3. เลือก **ลิงค์ไปยัง CDS สำหรับแอป**
4. เลือกการแม็ปทั้งหมดที่กำลังรัน แล้วจากนั้น เลือก **หยุด**
5. เลือกการแม็ปทั้งหมด และจากนั้น เลือก **ลบ**

    > [!NOTE]
    > ตัวเลือก **ลบ** จะไม่พร้อมใช้งาน ถ้ามีการเลือกเท็มเพลต **CustomerV3-Account** ยกเลิกการเลือกเท็มเพลตนี้ตามต้องการ **CustomerV3-Account** เป็นเทมเพลตที่เตรียมใช้งานที่เก่ากว่า และใช้ได้กับโซลูชันผู้ที่มีแนวโน้มจะเป็นลูกค้าเป็นเงินสด เพราะมีการนำออกใช้งานทั่วโลก ซึ่งแสดงขึ้นภายใต้เท็มเพลตทั้งหมด

6. เลือก **ยกเลิกการเชื่อมโยงสภาพแวดล้อม**
7. เลือก **ใช่** เพื่อยืนยันการดำเนินงาน
8. หากต้องการเชื่อมโยงสภาพแวดล้อมใหม่ ให้ทำตามขั้นตอนใน [คู่มือการติดตั้ง](https://aka.ms/dualwrite-docs)
