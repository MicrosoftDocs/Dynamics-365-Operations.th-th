---
title: คู่มือการแก้ไขปัญหาสำหรับการรวมข้อมูล
description: หัวข้อนี้แสดงข้อมูลการแก้ไขปัญหาเกี่ยวกับการรวมข้อมูลระหว่าง Microsoft Dynamics 365 for Finance and Operations และ Common Data Service
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
ms.openlocfilehash: ca62a6b3aa64ec2383ee3ded3b7bbf4650a41166
ms.sourcegitcommit: efcc0dee8bde5f8f93f6291e7f059ad426843e57
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 07/31/2019
ms.locfileid: "1797286"
---
# <a name="troubleshooting-guide-for-data-integration"></a>คู่มือการแก้ไขปัญหาสำหรับการรวมข้อมูล

## <a name="enable-plugin-trace-in-common-data-service-and-check-the-dual-write-plugin-error-details"></a>เปิดใช้งานการติดตามปลั๊กอินใน Common Data Service และตรวจสอบรายละเอียดข้อผิดพลาดปลั๊กอินการเขียนแบบคู่

หากคุณกำลังประสบปัญหาหรือข้อผิดพลาดกับการซิงโครไนส์การเขียนแบบคู่ คุณสามารถตรวจสอบข้อผิดพลาดในบันทึกการติดตาม:

1. ก่อนที่คุณจะสามารถตรวจสอบข้อผิดพลาด คุณต้องเปิดใช้งานการติดตามปลั๊กอินโดยใช้คำแนะนำใน [ลงทะเบียนปลั๊กอิน](https://docs.microsoft.com/en-us/powerapps/developer/common-data-service/tutorial-write-plug-in#view-trace-logs) เพื่อเปิดใช้งานการติดตามปลั๊กอิน ตอนนี้คุณสามารถตรวจสอบข้อผิดพลาดได้
2. ล็อกอินเข้าสู่ Dynamics 365 for Sales
3. คลิกที่ไอคอนการตั้งค่า (เกียร์) และเลือก **การตั้งค่าขั้นสูง**
4. ในเมนู **การตั้งค่า** เลือก **การเลือกกำหนด > ล็อกการติดตามปลั๊กอิน**
5. คลิกที่ชื่อชนิด **Microsoft.Dynamics.Integrator.CrmPlugins.Plugin** เพื่อแสดงรายละเอียดข้อผิดพลาด

## <a name="check-dual-write-synchronization-errors-in-finance-and-operations"></a>ตรวจสอบข้อผิดพลาดในการซิงโครไนส์การเขียนแบบคู่ใน Finance and Operations

คุณสามารถตรวจสอบข้อผิดพลาดในระหว่างการทดสอบได้โดยทำตามขั้นตอนเหล่านี้:

+ ล็อกอินเข้าสู่ LifeCycle Services (LCS)
+ เปิดโครงการ LCS ที่คุณเลือกเพื่อทำการทดสอบการเขียนแบบคู่
+ ไปยังสภาพแวดล้อมที่ใช้ Cloud
+ เดสก์ท็อประยะไกลไปยัง Finance and Operations VM โดยใช้บัญชีภายในเครื่องที่แสดงใน LCS
+ เปิดตัวแสดงเหตุการณ์ 
+ นำทางไปยัง **ล็อกของแอพลิเคชันและบริการ > Microsoft > Dynamics > AX-DualWriteSync > การดำเนินงาน** ข้อผิดพลาดและรายละเอียดจะแสดงขึ้น

## <a name="how-to-unlink-and-link-another-common-data-service-environment-from-finance-and-operations"></a>วิธียกเลิกการเชื่อมโยงและเชื่อมโยงสภาพแวดล้อม Common Data Service อื่นจาก Finance and Operations

คุณสามารถปรับปรุงการเชื่อมโยงโดยทำตามขั้นตอนเหล่านี้:

+ นำทางไปยังสภาพแวดล้อม Finance and Operations
+ เปิดการจัดการข้อมูล
+ คลิกที่ **ลิงค์ไปยัง CDS สำหรับแอป**
+ เลือกการแม็ปที่กำลังรันทั้งหมด และคลิก **หยุด** 
+ เลือกการแม็ปทั้งหมด และคลิก **ลบ**

    > [!NOTE]
    > ตัวเลือก **ลบ** จะไม่ปรากฏ ถ้ามีการเลือกเท็มเพลต **CustomerV3-Account** ยกเลิกการเลือก ถ้าจำเป็น **CustomerV3-Account** เป็นเทมเพลตที่เตรียมใช้งานที่เก่ากว่า และใช้ได้กับโซลูชันผู้ที่มีแนวโน้มจะเป็นลูกค้าเป็นเงินสด เพราะมีการนำออกใช้งานทั่วโลก ซึ่งแสดงขึ้นภายใต้เท็มเพลตทั้งหมด

+ คลิก **ยกเลิกการเชื่อมโยงสภาพแวดล้อม**
+ คลิก **ใช่** เพื่อยืนยัน
+ หากต้องการเชื่อมโยงสภาพแวดล้อมใหม่ ให้ทำตามขั้นตอนใน [คู่มือการติดตั้ง](https://aka.ms/dualwrite-docs)

