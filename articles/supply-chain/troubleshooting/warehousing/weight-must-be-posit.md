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
ms.openlocfilehash: 27ec37e0c0644ff10ece4626d5c136bca3c52ef12f1c6de947afd03003a5368a
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 08/05/2021
ms.locfileid: "6776787"
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
