---
title: การตั้งค่าการคิดค่าเสื่อมราคาพิเศษ
description: 'กระบวนงานนี้จะแสดงวิธีการสร้างการหักค่าเสื่อมราคาพิเศษและเชื่อมโยงกับสมุดบัญชีสินทรัพย์ถาวร '
author: saraschi2
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: AssetBonus, AssetGroup, AssetGroupBookSetup, AssetGroupSetupBonus
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 7fed9f09b4e37da00a5d78fa088e8814db48456b
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 01/15/2021
ms.locfileid: "4968940"
---
# <a name="set-up-bonus-depreciation"></a>การตั้งค่าการคิดค่าเสื่อมราคาพิเศษ

[!include [banner](../../includes/banner.md)]

กระบวนงานนี้จะแสดงวิธีการสร้างการหักค่าเสื่อมราคาพิเศษและเชื่อมโยงกับสมุดบัญชีสินทรัพย์ถาวร  ซึ่งจะใช้บทบาทของนักบัญชีและข้อมูลสาธิตสำหรับนิติบุคคล USMF


## <a name="create-a-special-depreciation-allowance"></a>สร้างการหักค่าเสื่อมราคาพิเศษ
1. ไปที่สินทรัพย์ถาวร > การติดตั้ง > การหักค่าเสื่อมราคาพิเศษ
2. คลิก สร้าง
3. ในฟิลด์โพรไฟล์การหักค่าเสื่อมราคาพิเศษ พิมพ์ค่า
4. ในฟิลด์ คำอธิบาย ให้พิมพ์ค่า
5. ในฟิลด์เปอร์เซ็นทร์ ป้อนจำนวน
    * ถ้าไม่ระบุเป็นเปอร์เซ็นต์ ให้ตั้งค่าเป็นจำนวนเงิน  

## <a name="associate-a-special-depreciation-allowance-with-a-fixed-asset-group-book"></a>เชื่อมโยงการหักค่าเสื่อมราคาพิเศษกับสมุดบัญชีกลุ่มสินทรัพย์ถาวร
1. ไปที่สินทรัพย์ถาวร > การติดตั้ง > กลุ่มสินทรัพย์ถาวร
2. ในรายการ ให้เลือกสินทรัพย์ถาวรที่เกี่ยวข้องกับการหักค่าเสื่อมราคาพิเศษ
3. คลิก สมุดบัญชี
4. ในรายการ ให้เลือกสมุดบัญชีที่เกี่ยวข้องกับการหักค่าเสื่อมราคาพิเศษ
5. คลิกการหักค่าเสื่อมราคาพิเศษ
6. คลิก สร้าง
7. ในฟิลด์โพรไฟล์การหักค่าเสื่อมราคาพิเศษ ให้ป้อนหรือเลือกค่า
    * ค่าเริ่มต้นของเปอร์เซ็นต์หรือยอดเงินมาจากการตั้งค่าการหักค่าเสื่อมราคาพิเศษ  
8. ในฟิลด์ระดับความสำคัญ ให้ป้อนตัวเลข

