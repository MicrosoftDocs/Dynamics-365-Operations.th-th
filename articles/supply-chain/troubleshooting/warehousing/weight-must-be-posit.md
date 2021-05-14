---
title: น้ำหนักต้องเป็นค่าบวก
description: น้ำหนักต้องเป็นค่าบวก
author: perlynne
ms.date: 04/15/2021
ms.topic: troubleshooting
ms.search.form: WHSContainerCloseDiag_canClose
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2021-05-15
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: dcbcde3143cb509b68b277cb7c709263e2659b5b
ms.sourcegitcommit: 5f5afb46431e1abd8fb6e92e0189914b598dc7fd
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 04/21/2021
ms.locfileid: "5924314"
---
# <a name="weight-must-be-positive"></a>น้ำหนักต้องเป็นค่าบวก

รหัสข้อผิดพลาด: WeightMustBePositive

## <a name="symptoms"></a>อาการ

ระบบแสดงข้อความแสดงข้อผิดพลาดต่อไปนี้:

> น้ำหนักต้องเป็นค่าบวก

## <a name="cause"></a>สาเหตุ

ฟิลด์ **น้ําหนักรวม** จะถูกตั้งค่าเป็น *0* (ศูนย์) หรือค่าลบ

## <a name="resolution"></a>ความละเอียด

เมื่อต้องการระบุน้ำหนัก ให้ทำตามขั้นตอนเหล่านี้

- ในฟิลด์ **น้ําหนักรวม** ให้ตั้งค่า จากนั้นเลือกหน่วยในรายการแบบหล่นลง
- เลือก **ดูน้ําหนักของระบบ** เพื่อคํานวณค่า **น้ําหนักรวม**
