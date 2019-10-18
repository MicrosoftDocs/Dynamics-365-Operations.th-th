---
title: ค่าใช้จ่ายส่วนบุคคลในรายงานค่าใช้จ่าย
description: หัวข้อนี้อธิบายวิธีสองวิธีในการจัดการค่าใช้จ่ายส่วนบุคคลของผู้ปฏิบัติงานใน Microsoft Dynamics 365 Finance
author: saraschi2
manager: AnnBe
ms.date: 02/23/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TrvParameters
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 825b6c131c8a65b99d5b7ebdadcd6389886f2d11
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 09/27/2019
ms.locfileid: "2180148"
---
# <a name="personal-expenses-on-an-expense-report"></a>ค่าใช้จ่ายส่วนบุคคลในรายงานค่าใช้จ่าย

[!include [banner](../includes/banner.md)]

ระหว่างการเดินทางเพื่อไปทำธุรกิจของบริษัท บางครั้งพนักงานอาจชำระค่าใช้จ่ายส่วนตัวโดยใช้บัตรเครดิตของบริษัทของพวกเขา ถ้าคุณไม่กำหนดกระบวนการสำหรับการจัดการค่าใช้จ่ายส่วนบุคคล กระบวนการอนุมัติสำหรับรายงานค่าใช้จ่ายอาจจะหยุดชะงัก เมื่อพนักงานส่งรายงานค่าใช้จ่ายที่แสดงรายการของพวกเขา 

มีวิธีสองวิธีในการจัดการค่าใช้จ่ายส่วนบุคคลของผู้ปฏิบัติงาน:

- **ชำระโดยพนักงาน** – องค์กรของคุณไม่ชำระค่าใช้จ่ายส่วนบุคคลที่ปรากฏในบิลสำหรับบัตรเครดิตของบริษัท จะสร้างรายงานที่แสดงรายจ่ายส่วนตัวร่วมกับรายจ่ายของบริษัท ซึ่งถูกเรียกเก็บไปยังบัตรเครดิตของบริษัทแทน
- **ชำระโดยบริษัท** – บริษัทของคุณชำระบิลทั้งหมดสำหรับบัตรเครดิตของบริษัท และจากนั้นหักบัญชีของพนักงานในส่วนที่เป็นรายจ่ายส่วนตัว

คุณสามารถเลือกวิธีการที่องค์กรของคุณใช้ในหน้า **พารามิเตอร์การจัดการค่าใช้จ่าย** ได้
