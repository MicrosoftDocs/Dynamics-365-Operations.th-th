---
title: ภาพรวมของ Positive pay
description: บทความนี้แสดงข้อมูลเกี่ยวกับ positive pay ซึ่งถูกใช้ในการสร้างรายการอิเล็กทรอนิกส์ของเช็คที่สามารถแสดงให้กับธนาคารได้
author: abruer
manager: AnnBe
ms.date: 08/22/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: BankPositivePaySummary
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 88463
ms.assetid: 1e3a39d3-f9b3-4073-9730-c96a607243e2
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-05-31
ms.dyn365.ops.version: AX 7.0.1
ms.openlocfilehash: 2ba23cf5afe9f007f5e32a75e918595929ad79a1
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 08/01/2019
ms.locfileid: "1834620"
---
# <a name="positive-pay-overview"></a>ภาพรวมของ Positive pay

[!include [banner](../includes/banner.md)]

บทความนี้แสดงข้อมูลเกี่ยวกับ positive pay ซึ่งถูกใช้ในการสร้างรายการอิเล็กทรอนิกส์ของเช็คที่สามารถแสดงให้กับธนาคารได้ 

Positive pay ถูกใช้ในการสร้างรายการอิเล็กทรอนิกส์ของเช็คที่สามารถแสดงให้กับธนาคาร  ไฟล์ Positive pay สามารถช่วยธนาคารป้องกันการฉ้อโกงเช็ค  คุณตั้งค่า Positive pay เพื่อสร้างรายการอิเล็กทรอนิกส์ของเช็คทุกครั้งที่มีการพิมพ์เช็ค  แล้วจากนั้นเมื่อมีการนำเสนอเช็คให้กับธนาคาร ธนาคารจะเปรียบเทียบเช็คกับรายการเช็คที่คุณส่งไปก่อนหน้านี้  ถ้าเช็คตรงกับเช็คในรายการ ธนาคารจะเคลียร์เช็ค  ถ้าเช็คไม่ตรงกัน ธนาคารจะระงับเช็คไว้เพื่อตรวจสอบ

Positive pay ถูกเรียกอีกอย่างว่า SafePay  

ไฟล์ positive pay สามารถประกอบด้วยข้อมูลที่สำคัญเกี่ยวกับผู้จ่าย และยอดเงินเช็ค  ดังนั้นตรวจสอบให้แน่ใจว่า คุณใช้มาตรการด้านความปลอดภัยที่เหมาะสมจากเวลาที่มีการสร้างไฟล์ จนกระทั่งได้รับโดยธนาคาร  ไฟล์ Positive pay จะถูกดาวน์โหลดตามคำแนะนำในการดาวน์โหลดสำหรับเว็บเบราเซอร์  

มีสร้างไฟล์ positive pay โดยการใช้เอนทิตีข้อมูล  ก่อนที่คุณสร้างไฟล์ Positive pay คุณต้องตั้งค่ารูปแบบของการแปลงสำหรับ XML ที่แปลข้อมูลเป็นรูปแบบที่ธนาคารสามารถใช้ได้  

สำหรับแต่ละบัญชีธนาคารที่คุณต้องการสร้างข้อมูล Positive pay ให้ คุณต้องกำหนดรูปแบบ Positive pay  หลังจากที่คุณได้สร้างการชำระเงิน คุณสามารถสร้างไฟ Positive pay สำหรับนิติบุคคลเดี่ยวและบัญชีธนาคารเดี่ยวได้  อีกทางหนึ่งคือ คุณสามารถสร้างไฟล์ Positive pay สำหรับหลายนิติบุคคลและหลายบัญชีธนาคารในเวลาเดียวกันได้  

หลังจากที่เช็คที่ถูกรายการในไฟล์ positive pay ได้ถูกชำระ คุณจะได้รับหมายเลขการยืนยันจากธนาคารของคุณ  จากนั้น คุณสามารถยืนยันไฟล์ค่าจ้างเชิงบวกได้ใน Microsoft Dynamics 365 for Finance and Operations 

ถ้าคุณต้องเปลี่ยนไฟล์ positive pay คุณสามารถเรียกคืนได้  จากนั้นสำหรับเช็คแต่ละรายการในไฟล์ Positive pay ฟิลด์ที่บ่งชี้ว่าเช็คได้ถูกรวมอยู่ในไฟล์ Positive pay หรือไม่ จะถูกรีเซ็ต

สำหรับข้อมูลเพิ่มเติม ดู [ตั้งค่าและสร้างไฟล์ Positive Pay](set-up-generate-positive-pay-files.md)



