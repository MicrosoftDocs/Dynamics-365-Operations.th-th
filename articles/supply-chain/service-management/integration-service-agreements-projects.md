---
title: การรวมสำหรับข้อตกลงและโครงการการบริการ
description: เมื่อคุณทำงานกับข้อตกลงการให้บริการและรายการข้อตกลงการให้บริการ คุณใช้ข้อมูลที่ถูกตั้งค่าไว้ในพื้นที่ในการจัดการและการบัญชีโครงการ
author: ShylaThompson
manager: tfehr
ms.date: 05/01/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProjParameters
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 5eab6125dbca1568c06818c8528d1bee4ce6bf53
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 01/15/2021
ms.locfileid: "4974471"
---
# <a name="integration-for-service-agreements-and-projects"></a>การรวมสำหรับข้อตกลงและโครงการการบริการ 

[!include [banner](../includes/banner.md)]


เมื่อคุณทำงานกับข้อตกลงการให้บริการและรายการข้อตกลงการให้บริการ คุณใช้ข้อมูลที่ถูกตั้งค่าไว้ในพื้นที่ต่อไปนี้ใน **การจัดการและการบัญชีโครงการ**

## <a name="project-prices"></a>ราคาโครงการ

ต้นทุนและราคาขายสำหรับธุรกรรมข้อตกลงการให้บริการได้รับมาจากการตั้งค่าราคาต้นทุน ซึ่งนำไปใช้กับโครงการที่ถูกแนบกับข้อตกลงการให้บริการ สามารถตั้งค่าต้นทุนและราคาขายได้ตามโครงการ พนักงาน และประเภท 

## <a name="project-validation"></a>การตรวจสอบความถูกต้องของโครงการ

โครงการ พนักงาน และประเภทที่พร้อมให้เลือกในรายการข้อตกลงการให้บริการ สามารถถูกจำกัดได้โดยการตั้งค่าใน **การจัดการและการบัญชีโครงการ** โดยการใช้การตั้งค่าการตรวจสอบความถูกต้อง คุณสามารถรวมพนักงาน โครงการ และประเภท เพื่อควบคุมการเข้าถึงได้ 

## <a name="project-line-properties"></a>คุณสมบัติรายการของโครงการ

ลักษณะของรายการถูกป้อนโดยอัตโนมัติสำหรับรายการข้อตกลงการให้บริการ

ลักษณะของรายการจะถูกสร้างขึ้นในแบบฟอร์ม **คุณสมบัติรายการ** ใน **การจัดการและการบัญชีโครงการ** ลักษณะของรายการที่ถูกป้อนบนข้อตกลงการให้บริการ จะถูกแนบกับโครงการที่ถูกเลือกสำหรับข้อตกลงการให้บริการ และได้รับสืบทอดในลำดับต่อมาตามรายการข้อตกลงการให้บริการ 

## <a name="default-offset-accounts"></a>บัญชีตรงข้ามเริ่มต้น

ถ้าคุณป้อนธุรกรรมค่าใช้จ่าย บัญชีตรงข้ามของค่าใช้จ่ายเริ่มต้นจะถูกเลือกสำหรับธุรกรรมโดยอัตโนมัติ บัญชีค่าใช้จ่ายเริ่มต้นถูกตั้งค่าสำหรับโครงการที่ถูกแนบกับข้อตกลงการให้บริการปัจจุบัน

## <a name="project-categories"></a>ประเภทโครงการ

ประเภทที่พร้อมใช้งานสำหรับรายการข้อตกลงการให้บริการ จะถูกตั้งค่าในแบบฟอร์ม **ประเภทโครงการ** ใน **การจัดการและการบัญชีโครงการ** 

> [!NOTE]
> <P>ประเภทที่มีกล่องกาเครื่องหมาย <STRONG>เปิดใช้งานอยู่ในสมุดรายวัน</STRONG> ที่ถูกเลือกบนแท็บ <STRONG>โครงการ</STRONG> ในแบบฟอร์ม <STRONG>ประเภทโครงการ</STRONG> จะพร้อมใช้งานสำหรับการเลือก อย่างไรก็ตาม ถ้ากล่องกาเครื่องหมาย <STRONG>ประเภทที่ไม่ได้ใช้งาน</STRONG> ถูกเลือกบนแท็บ <STRONG>สมุดรายวัน</STRONG> ในแบบฟอร์ม <STRONG>พารามิเตอร์การจัดการและการบัญชีโครงการ</STRONG> ประเภททั้งหมดจะพร้อมใช้งานสำหรับการเลือก</P>

## <a name="project-parameters"></a>พารามิเตอร์โครงการ

ถ้าฟิลด์ **ผู้ปฏิบัติงานที่สิ้นสุดการจ้างงาน** บนแท็บ **สมุดรายวัน** ในฟอร์ม **พารามิเตอร์การจัดการและการบัญชีโครงการ** ถูกเลือก คุณสามารถเลือกพนักงานที่ไม่ได้ใช้งานและพนักงานที่ใช้งานในแบบฟอร์ม **ข้อตกลงการบริการ** และ **ใบสั่งบริการ** ได้

นอกจากนี้ คุณยังสามารถเปิดใช้งานฟิลด์ **เวลาเริ่มต้น** และ **เวลาสิ้นสุด** บนแท็บ **โครงการ** ในฟอร์ม **ใบสั่งบริการ** เพื่อป้อนเวลาเริ่มต้นและเวลาสิ้นสุดบนรายการใบสั่งบริการ

## <a name="enable-the-starting-and-ending-time-feature-for-service-orders"></a>เปิดใช้งานคุณลักษณะเวลาเริ่มต้นและเวลาสิ้นสุดสำหรับใบสั่งบริการ

1.  คลิก **การจัดการและการบัญชีโครงการ** \> **การตั้งค่า** \> **พารามิเตอร์การจัดการและการบัญชีโครงการ**

2.  คลิกแท็บ **สมุดรายวัน** และจากนั้นเลือกกล่องกาเครื่องหมาย **แสดงเวลาเริ่มต้น/เวลาสิ้นสุด**

3.  คลิก **การจัดการโครงการและการบัญชี** \> **ตั้งค่า** \> **สมุดรายวัน** \> **ชื่อสมุดรายวัน**

4.  เลือกชื่อสมุดรายวันที่ถูกแนบกับใบสั่งบริการ

5.  คลิกแท็บ **ทั่วไป** และจากนั้นเลือกกล่องกาเครื่องหมาย **แสดงเวลาเริ่มต้น/เวลาสิ้นสุด**


> [!NOTE]
> <P>เลือกชื่อสมุดรายวันสำหรับใบสั่งบริการในฟิลด์ <STRONG>ชั่วโมง</STRONG> บนแท็บ <STRONG>สมุดรายวัน</STRONG> ในฟอร์ม <STRONG>พารามิเตอร์การจัดการงานบริการ</STRONG></P>





