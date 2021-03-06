---
title: ตั้งค่าประเภทบัญชีหลัก
description: หัวข้อนี้อธิบายวิธีการตั้งค่าประเภทบัญชีหลักใน Dynamics 365 Finance
author: aprilolson
manager: AnnBe
ms.date: 08/08/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: MainAccountCategory, MainAccountCategoryLink
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 0d53181d63f7b362662d993e21671e9b685b5dfe
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 01/15/2021
ms.locfileid: "4968438"
---
# <a name="set-up-main-account-categories"></a>ตั้งค่าประเภทบัญชีหลัก

[!include [banner](../../includes/banner.md)]

หัวข้อนี้อธิบายวิธีการตั้งค่าประเภทบัญชีหลัก ประเภทลูกค้าองค์กรหลักถูกใช้สำหรับรายงานเริ่มต้นในการรายงานทางการเงินและใน Power BI ประเภทบัญชีหลักที่ถูกสร้างขึ้น ตามค่าเริ่มต้นสามารถเปลี่ยนชื่อ แต่จะไม่ถูกไม่ลบ  ประเภทบัญชีหลักเพิ่มเติมสามารถสร้างขึ้นได้และใช้เพื่อการรายงานและการวิเคราะห์วัตถุประสงค์  หัวข้อนี้ใช้บริษัทสาธิต USMF

## <a name="create-a-main-account-category"></a>สร้างประเภทบัญชีหลัก
1. ในบานหน้าต่างนำทาง ไปที่ **โมดูล > บัญชีแยกประเภททั่วไป > ผังบัญชี > บัญชี > ประเภทบัญชีหลัก**
2. เลือก **ใหม่**
3. ในฟิลด์ **ประเภทบัญชีหลัก** ป้อนชื่อเฉพาะ
4. ใน **ฟิลด์คำอธิบาย** ให้ป้อนคำอธิบายสำหรับประเภทบัญชีหลัก
5. ใน **ชนิดบัญชีหลัก** ให้เลือกชนิดบัญชีหลักที่จะเชื่อมโยงกับประเภท

## <a name="link-main-accounts-to-account-category"></a>เชื่อมโยงบัญชีหลักกับประเภทบัญชี
1. คลิก **เชื่อมโยงบัญชีหลัก**
2. ในรายการ ให้เลือกบัญชีหลักที่จะกำหนดให้กับประเภทบัญชีหลักโดยการเลือกกล่องกาเครื่องหมายในคอลัมน์ **ที่เชื่อมโยง** การกำหนดบัญชีหลักให้กับประเภทบัญชีหลักจะรวมยอดดุลของบัญชีเมื่อใช้ประเภทสำหรับการวิเคราะห์และการรายงานทางการเงิน  
3. เลือกหรือล้างตัวเลือก **ที่เชื่อมโยง** ให้เลือกบัญชีหลัก
4. เลือก **ตกลง**
5. เลือก **ใช่**
