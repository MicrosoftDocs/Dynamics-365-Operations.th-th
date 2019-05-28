---
title: กำหนดตัวคั่นผังบัญชีไม่ซ้ำกัน
description: ใน Dynamics 365 for Finance and Operations คุณไม่สามารถมีตัวคั่นเดียวกันได้สำหรับแผนภูมิของลูกค้าองค์กรและค่ามิติ คุณต้องเปลี่ยนค่าตัวคั่นหลังจากการอัพเกรด
author: ryansandness
manager: AnnBe
ms.date: 03/30/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 265364
ms.assetid: c61391e4-c4bf-4f09-bd18-8107a1bf055e
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: 8
ms.openlocfilehash: e197a1b44e038a97b8bf6db692dcc2eef2bc5f7b
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 05/15/2019
ms.locfileid: "1559539"
---
# <a name="make-the-chart-of-accounts-delimiter-unique"></a>กำหนดตัวคั่นผังบัญชีไม่ซ้ำกัน

[!include [banner](../includes/banner.md)]

ใน Microsoft Dynamics AX 2012 คุณสามารถใช้ตัวคั่นเดียวกันได้สำหรับแผนภูมิของลูกค้าองค์กรและค่ามิติของคุณ ใน Dynamics 365 for Finance and Operations คุณไม่สามารถมีตัวคั่นเดียวกันได้สำหรับแผนภูมิของลูกค้าองค์กรและค่ามิติ ถ้าไม่มีตัวคั่นซ้ำ คุณสามารถเปลี่ยนได้หลังจากการอัพเกรด 

คุณลักษณะนี้จะพร้อมใช้งานใน:
- Dynamics 365 for Finance and Operations รุ่น 8.0
- Dynamics 365 for Finance and Operations รุ่น 7.1 KB 4094701 ไม่สามารถป้อนมิติทางการเงินได้ เมื่อค่ามิติประกอบด้วยตัวคั่นแผนภูมิของลูกค้าองค์กร
- Dynamics 365 for Finance and Operations รุ่น 7.2 KB 4092967 ไม่สามารถเลือกโครงการย่อยเป็นมิติได้ เมื่อรูปแบบโครงการย่อยประกอบด้วยตัวคั่นมิติ

## <a name="update-delimiter"></a>อัพเดตตัวคั่น
ถ้ามีความขัดแย้งกับผังบัญชี สามารถเปลี่ยนตัวคั่นผังบัญชีตัวและรูปแบบรหัสโครงการ/โครงการย่อยได้ ไม่มีตัวคั่นมิติอื่นๆ ที่สามารถเปลี่ยนได้ 
- คุณสามารถเปลี่ยนตัวคั่นผังบัญชีได้ หลังจากการอัพเกรดเป็น Finance and Operations ใน **พารามิเตอร์บัญชีแยกประเภททั่วไป** > **ผังบัญชีและมิติ** > **เปลี่ยนตัวคั่น** 
- ถ้ามีเฉพาะความขัดแย้งอยู่กับรูปแบบรหัสโครงการ/โครงการย่อย คุณสามารถเปลี่ยนค่านั้นได้ใน **พารามิเตอร์การจัดการและการบัญชีโครงการ** > **ทั่วไป** > **ปรับเปลี่ยนรูปแบบโครงการย่อย** 

## <a name="how-to-determine-if-your-environment-requires-updated-delimiters"></a>วิธีการตรวจสอบว่า สภาพแวดล้อมของคุณต้องใช้ตัวคั่นที่มีการปรับปรุงหรือไม่ 
ถ้าตัวคั่นในสภาพแวดล้อมที่มีการอัพเกรดของคุณขัดแย้งกัน คุณอาจพบความไม่มีเสถียรภาพ เมื่อป้อนค่าในตัวควบคุมรายการที่มีการแบ่งส่วนหรือตัวควบคุมรายการมิติ ซึ่งหมายความว่า คุณจะต้องใช้การใช้การค้นหาหรือเมนูแบบลอยขึ้นเสมอ เมื่อป้อนชุดบัญชีและมิติ
