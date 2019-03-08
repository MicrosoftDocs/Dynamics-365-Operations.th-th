---
title: เพิ่มการคำนวณไปยังแบบจำลองการจัดโครงแบบผลิตภัณฑ์
description: 'กระบวนงานนี้แสดงวิธีการเพิ่มการคำนวณใหม่ไปยังแบบจำลองการจัดโครงแบบผลิตภัณฑ์ '
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: DefaultDashboard, EcoResProductVariantMaintainWorkspace, PCProductConfigurationModelListPage, PCProductConfigurationModelDetails, PCConstraintEditor, PCRuntimeConfiguratorValidate
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 9754c46010e7bbdb2edef0d6e68162f344bb1257
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 01/29/2019
ms.locfileid: "343178"
---
# <a name="add-a-calculation-to-a-product-configuration-model"></a>เพิ่มการคำนวณไปยังแบบจำลองการจัดโครงแบบผลิตภัณฑ์

[!include [task guide banner](../../includes/task-guide-banner.md)]

กระบวนงานนี้แสดงวิธีการเพิ่มการคำนวณใหม่ไปยังแบบจำลองการจัดโครงแบบผลิตภัณฑ์  แสดงว่าคุณสามารถสร้างนิพจน์ตรรกะโดยใช้ตัวดำเนินการ "ถ้า" เพื่อตั้งค่าความสูงของลำโพงที่ 10 สำหรับลำโพงสีขาวและ 15 สำหรับ cabinet อื่นๆที่จะเสร็จสิ้น  กระบวนงานใช้ส่วนประกอบลำโพงขั้นสูงในบริษัทสาธิต USMF


## <a name="add-a-calculation"></a>เพิ่มการคำนวณ

## <a name="create-calculation-expression"></a>สร้างนิพจน์การคำนวณ
1. คลิกแก้ไขนิพจน์
2. ในฟิลด์ ConstraintBody ให้ป้อน ' ถ้า[CabinetFinish == "ขาว" 10, 15]'
3. คลิก ตรวจสอบความถูกต้อง
4. คลิก ปิด
5. คลิก ตกลง

