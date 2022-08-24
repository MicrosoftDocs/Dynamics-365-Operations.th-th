---
title: การแก้ไขปัญหาการตั้งค่าและการติดตั้ง Store Commerce
description: บทความนี้จะอธิบายวิธีการแก้ไขปัญหาการตั้งค่าและการติดตั้งในแอป Store Commerce ของ Microsoft Dynamics 365 Commerce
author: josaw1
ms.date: 06/01/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: rassadi
ms.search.validFrom: 2017-06-20
ms.openlocfilehash: e3d115e84af1aaf5266eff6588ca6996a333e51a
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 08/12/2022
ms.locfileid: "9286342"
---
# <a name="troubleshoot-store-commerce-setup-and-installation-issues"></a>การแก้ไขปัญหาการตั้งค่าและการติดตั้ง Store Commerce

[!include [banner](../includes/banner.md)]

บทความนี้จะอธิบายวิธีการแก้ไขปัญหาการตั้งค่าและการติดตั้งในแอป Store Commerce ของ Microsoft Dynamics 365 Commerce

## <a name="i-cant-activate-the-app-and-i-receive-a-connectivity-error-message"></a>ฉันไม่สามารถเรียกใช้แอปได้ และได้รับข้อความแสดงข้อผิดพลาดการเชื่อมต่อ

หลังจากที่คุณป้อน URL ของ Cloud Point of Sale (CPOS) ที่ถูกต้องแล้ว คุณอาจได้รับข้อความแสดงข้อผิดพลาดเกี่ยวกับการเชื่อมต่อซึ่งคล้ายกับตัวอย่างต่อไปนี้:

> เกิดข้อผิดพลาดในการเชื่อมต่อ และอุปกรณ์ของคุณไม่สามารถเชื่อมต่อกับ CPOS ได้ ชนิด URL ของ CPOS อาจมีบางปัญหา

ในกรณีนี้ ให้ทบทวน URL เพื่อหาข้อผิดพลาดทางการพิมพ์ หรือระบุว่าไม่สามารถใช้งาน CPOS ได้เนื่องจากออฟไลน์

นอกจากนี้ ให้ตรวจสอบว่ารุ่น Cloud Scale Unit (CSU) ใช้10.0.25 (9.35.\*.\*) หรือใหม่กว่า ต้องใช้ CPOS รุ่น 10.0.25 หรือใหม่กว่าเพื่อใช้งานแอป Store Commerce

## <a name="i-cant-install-the-app-because-modern-pos-is-already-installed"></a>ฉันไม่สามารถติดตั้งแอปได้ เนื่องจาก Pos สมัยใหม่ได้รับการติดตั้งแล้ว

ในระหว่างการติดตั้ง คุณอาจได้รับข้อความแสดงข้อผิดพลาด เช่น ตัวอย่างต่อไปนี้:

> รุ่น (9.\*.\*.\*) ของผลิตภัณฑ์นี้ (POS สมัยใหม่) ได้รับการติดตั้งแล้วก่อนหน้านี้โดยผ่านตัวติดตั้งดั้งเดิม

หากต้องการแก้ไขข้อผิดพลาด คุณต้องถอนการติดตั้งแอป Modern Point of Sale (MPOS) ให้กับผู้ใช้ทั้งหมดในเครื่องแล้วลองอีกครั้ง คุณสามารถยืนยันว่า MPOS ถูกลบออกโดยผู้ใช้ทั้งหมดแล้วหรือไม่โดยการรันสั่ง PowerShell ต่อไปนี้

```PowerShell
Get-AppxPackage | Where-Object {$_.PackageFullName -like "Microsoft.Dynamics.*.Pos"} | Remove-AppxPackage -Allusers
```

## <a name="i-cant-activate-the-app-because-of-an-invalid-url-or-an-error-state"></a>ฉันไม่สามารถเรียกใช้แอปได้เนื่องจาก URL ไม่ถูกต้องหรือสถานะข้อผิดพลาด

หาก URL CPOS ที่คุณป้อนไม่ถูกต้องและคุณต้องการเปลี่ยนแปลง หรือหากแอป Store Commerce อยู่ในสถานะข้อผิดพลาดระหว่างการเรียกใช้ คุณสามารถเริ่มกระบวนการใหม่ได้โดยรีเซ็ตแอป แอป Store Commerce จะบันทึกเฉพาะ URL CPOS ที่ถูกต้องเท่านั้น

หากต้องการรีเซ็ตแอป Store Commerce ให้ปฏิบัติตามขั้นตอนต่อไปนี้

1. บนเมนู **เริ่มต้น** ของ Windows ให้เลือกและกดค้าง (หรือคลิกขวา) แอป แล้วเลือก **เพิ่มเติม \> การตั้งค่าแอป**
2. เลื่อนหน้าการตั้งค่าแอปลงจนกว่าคุณจะพบปุ่ม **รีเซ็ต**
3. เลือก **รีเซ็ต** จากนั้น เมื่อคุณได้รับพร้อมท์ ยืนยันว่าคุณต้องการรีเซ็ตแอป
