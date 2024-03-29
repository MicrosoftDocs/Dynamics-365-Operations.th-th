---
title: แก้ไขปัญหาการรวมแบบสองทิศทางในแอปการเงินและการดำเนินงาน
description: บทความนี้จะให้ข้อมูลเกี่ยวกับการแก้ไขปัญหาซึ่งช่วยให้คุณสามารถแก้ไขปัญหาด้วยโมดูลการรวมแบบสองทิศทางในแอปการเงินและการดำเนินงาน
author: RamaKrishnamoorthy
ms.date: 04/18/2022
ms.topic: article
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.region: global
ms.author: ramasri
ms.search.validFrom: 2020-03-16
ms.openlocfilehash: 5678cd38e48eb5226e36851679436d3b6c117cf9
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 08/12/2022
ms.locfileid: "9289588"
---
# <a name="troubleshoot-dual-write-issues-in-finance-and-operations-apps"></a>แก้ไขปัญหาการรวมแบบสองทิศทางในแอปการเงินและการดำเนินงาน

[!include [banner](../../includes/banner.md)]



บทความนี้แสดงข้อมูลการแก้ไขปัญหาสำหรับการรวมข้อมูลด้วยการรวมแบบสองทิศทางระหว่างแอปการเงินและการดำเนินงานกับ Dataverse กล่าวคือ จะให้ข้อมูลซึ่งช่วยให้คุณสามารถแก้ไขปัญหาด้วยโมดูล **การรวมแบบสองทิศทาง** ในแอปการเงินและการดำเนินงาน

> [!IMPORTANT]
> ปัญหาบางอย่างที่ที่อยู่ของบทความนี้ อาจจำเป็นต้องใช้บทบาทผู้ดูแลระบบ หรือข้อมูลประจำตัวผู้ดูแลระบบของผู้เช่า Microsoft Azure Active Directory (Azure AD) ส่วนสำหรับปัญหาแต่ละอย่างอธิบายว่าจำเป็นต้องมีบทบาทเฉพาะหรือข้อมูลประจำตัวหรือไม่

## <a name="you-cant-load-the-dual-write-module-in-a-finance-and-operations-app"></a>คุณไม่สามารถโหลดโมดูลการรวมแบบสองทิศทางในแอปการเงินและการดำเนินงาน

หากคุณไม่สามารถเปิดหน้า **การรวมแบบสองทิศทาง** โดยการเลือกไทล์ **การรวมแบบสองทิศทาง** ในพื้นที่ทำงาน **การจัดการข้อมูล** บริการการรวมข้อมูลอาจหยุดทำงานได้ สร้างบัตรผ่านการสนับสนุนเพื่อร้องขอการรีสตาร์ทของบริการการรวมข้อมูล

## <a name="error-when-you-try-to-create-a-new-table-map"></a>ข้อผิดพลาดเมื่อคุณพยายามสร้างแผนที่ตารางใหม่

**ข้อมูลประจำตัวที่จำเป็นในการแก้ไขปัญหา:** ผู้ใช้เดียวกันที่ตั้งค่าการรวมแบบสองทิศทาง

คุณอาจได้รับข้อความแสดงข้อผิดพลาดต่อไปนี้ เมื่อคุณพยายามตั้งค่าคอนฟิกตารางใหม่สำหรับการรวมแบบสองทิศทาง ผู้ใช้เท่านั้นที่สามารถสร้างแผนที่ได้คือ ผู้ใช้ที่ตั้งค่าการเชื่อมต่อการรวมแบบสองทิศทาง

*รหัสสถานะการตอบสนองไม่บ่งชี้ความสำเร็จ: 401 (ไม่ได้รับอนุมัติ)*

## <a name="error-when-you-open-the-dual-write-user-interface"></a>ข้อผิดพลาดเมื่อคุณเปิดอินเทอร์เฟสผู้ใช้การรวมแบบสองทิศทาง

คุณอาจได้รับข้อความแสดงข้อผิดพลาดต่อไปนี้ เมื่อคุณพยายามเข้าถึงการรวมแบบสองทิศทางจากพื้นที่ทำงาน **การจัดการข้อมูล**:

*login.microsoftonline.com ปฏิเสธที่จะเชื่อมต่อ*

เมื่อต้องการแก้ไขปัญหานี้ ให้ลงชื่อเข้าใช้โดยใช้หน้าต่างแบบ InPrivate ใน Microsoft Edge หน้าต่างที่ไม่ระบุตัวตนใน Chromium หรือหน้าต่างที่ไม่ระบุตัวตนใน Google Chrome นอกจากนี้ คุณยังต้องยกเลิกการบล็อคหรือล้างคุกกี้ของบุคคลที่สาม

## <a name="error-when-you-link-the-environment-for-dual-write-or-add-a-new-table-mapping"></a>ข้อผิดพลาดเมื่อคุณเชื่อมโยงสภาพแวดล้อมสำหรับการรวมแบบสองทิศทาง หรือเพิ่มการแมปตารางใหม่

**บทบาทที่จำเป็นในการแก้ไขปัญหา** ผู้ดูแลระบบสำหรับแอปการเงินและการดำเนินงานและ Dataverse

คุณอาจพบข้อผิดพลาดต่อไปนี้ เมื่อเชื่อมโยงหรือสร้างแผนที่:

```dos
Response status code does not indicate success: 403 (tokenexchange).
Session ID: \<your session id\>
Root activity ID: \<your root activity\> id
```

ข้อผิดพลาดนี้อาจเกิดขึ้นได้ ถ้าคุณไม่มีสิทธิ์เพียงพอที่จะเชื่อมโยงการรวมแบบสองทิศทาง หรือสร้างแผนที่ นอกจากนี้ ข้อผิดพลาดนี้ยังอาจเกิดขึ้น ถ้าสภาพแวดล้อม Dataverse ถูกรีเซ็ตโดยไม่มีการยกเลิกการเชื่อมโยงการรวมแบบสองทิศทาง ผู้ใช้ที่มีบทบาทผู้ดูแลระบบในทั้งแอปการเงินและการดำเนินงานและ Dataverse สามารถเชื่อมโยงสภาพแวดล้อมได้ เฉพาะผู้ใช้ที่ตั้งค่าการเชื่อมต่อการรวมแบบสองทิศทางเท่านั้นที่สามารถเพิ่มแผนที่ตารางใหม่ได้ หลังจากการตั้งค่า ผู้ใช้ใดๆ ที่มีบทบาทผู้ดูแลระบบสามารถตรวจสอบสถานะและแก้ไขการแมปได้

## <a name="error-when-you-stop-the-table-mapping"></a>ข้อผิดพลาดเมื่อคุณหยุดการแมปตาราง

คุณอาจได้รับข้อความแสดงข้อผิดพลาดต่อไปนี้ เมื่อคุณพยายามที่จะหยุดการแมปตาราง:

*\[ไม่ได้รับอนุญาต\] \[{"สถานะ":403,"แหล่งข้อมูล":"","ข้อความ":"ข้อผิดพลาดจากการแลกเปลี่ยนโทเคน: ผู้ใช้ไม่ได้รับอนุญาตให้เข้าถึงการเชื่อมต่อ dynamicscrmonline/xxxxxx-xxxx-xxxx-xxxxxxxx"}\] เซิร์ฟเวอร์ระยะไกลส่งคืนข้อผิดพลาด: (403) ไม่ได้รับอนุญาต*

ข้อผิดพลาดนี้จะเกิดขึ้น เมื่อสภาพแวดล้อม Dataverse ที่มีการเชื่อมโยงไม่พร้อมใช้งาน

เมื่อต้องการแก้ไขปัญหา ให้สร้างตั๋วสำหรับทีมงานการรวมข้อมูล แนบการสืบค้นกลับเครือข่ายเพื่อให้ทีมงานการรวมข้อมูลสามารถทำเครื่องหมายแผนที่เป็น **ไม่ได้เรียกใช้อยู่** ในแบ็คเอนด์

## <a name="enable-parallel-processing-in-finance-and-operations-apps-to-improve-performance"></a>เปิดใช้งานประมวลผลพร้อมกันในแอปการเงินและการดำเนินงานเพื่อปรับปรุงประสิทธิภาพ

การเปิดใช้งานการประมวลผลพร้อมกันจะสามารถลดเวลาที่ต้องใช้ในการนําเข้าข้อมูลจากแอป Dynamics 365 customer engagement และ Microsoft Dataverse ไปยังแอปการเงินและการดำเนินงาน 

หากต้องการเปิดใช้งานประมวลผลพร้อมกันในแอปการเงินและการดำเนินงาน ให้ทำตามขั้นตอนต่อไปนี้

1. เข้าสู่ระบบสภาพแวดล้อมแอปการเงินและการดำเนินงานของคุณ
2. ไปยัง **การจัดการข้อมูล > พารามิเตอร์ของกรอบงาน**
3. เลือก **การตั้งค่าเอนทิตี** และเลือกพารามิเตอร์ **ตั้งค่าคอนฟิกพารามิเตอร์การดำเนินการกับเอนทิตี**
4. เพิ่มพารามิเตอร์เพื่อการประมวลผลพร้อมกัน:
    - **จำนวนเรกคอร์ดที่เป็นขีดจำกัดการนำเข้า** – จํานวนของเรกคอร์ดที่ต้องเป็นไปตามกำหนดก่อนที่จะเปิดใช้งานการประมวลผลพร้อมกัน
    - **จำนวนงานนำเข้า** – จํานวนเธรด (งาน) ที่จะทำงานพร้อมกัน
5. เลือก **บันทึก**


## <a name="errors-while-trying-to-start-a-table-mapping"></a>เกิดข้อผิดพลาดในขณะที่พยายามเริ่มต้นการแมปตาราง

### <a name="unable-to-complete-initial-data-sync"></a>ไม่สามารถซิงค์ข้อมูลเริ่มต้นให้เสร็จสมบูรณ์

คุณอาจได้รับข้อผิดพลาดต่อไปนี้ เมื่อคุณพยายามเรียกใช้การซิงโครไนส์เริ่มต้น:

*ไม่สามารถทำการซิงค์ข้อมูลเริ่มต้นให้เสร็จสมบูรณ์ได้ ข้อผิดพลาด: ความล้มเหลวในการรวมแบบสองทิศทาง - การลงทะเบียนปลั๊กอินล้มเหลว: ไม่สามารถสร้างข้อมูลเมตาในการค้นหาการรวมแบบสองทิศทางได้ ไม่ได้ตั้งค่าการอ้างอิงอ็อบเจกต์ข้อผิดพลาดให้กับอินสแตนซ์ของอ็อบเจ็กต์*

เมื่อคุณพยายามตั้งค่าสถานะดังกล่าวของการแมปเป็น **กำลังเรียกใช้** คุณอาจได้รับข้อผิดพลาดนี้ การแก้ไขจะขึ้นอยู่กับสาเหตุของข้อผิดพลาด:

+ ถ้าการแมปมีการแมปที่ไม่ขึ้นต่อกัน ให้ตรวจสอบให้แน่ใจว่าได้เปิดใช้งานการแมปที่ไม่ขึ้นต่อกันของการแมปตารางนี้
+ การแมปอาจขาดคอลัมน์ต้นทางหรือปลายทาง ถ้าคอลัมน์ในแอปการเงินและการดำเนินงานขาดหายไป ให้ทำตามขั้นตอนในส่วน [ปัญหาคอลัมน์ตารางที่หายไปบนแผนผัง](dual-write-troubleshooting-finops-upgrades.md#missing-table-columns-issue-on-maps) ถ้าคอลัมน์ใน Dataverse ขาดหายไป ให้คลิกปุ่ม **รีเฟรชตาราง** บนการแมป เพื่อให้มีการเติมข้อมูลในคอลัมน์โดยอัตโนมัติกลับไปยังการแมป

### <a name="version-mismatch-error-and-upgrading-dual-write-solutions"></a>ข้อผิดพลาดของรุ่นไม่ตรงกันและการอัปเกรดโซลูชันการรวมแบบสองทิศทาง

คุณอาจได้รับข้อความแสดงข้อผิดพลาดต่อไปนี้ เมื่อคุณพยายามที่จะเรียกใช้การแมปตาราง:

+ *กลุ่มลูกค้า (msdyn_customergroups) : การรวมแบบสองทิศทางล้มเหลว - โซลูชัน Dynamics 365 for Sales 'Dynamics365Company' มีรุ่นที่ไม่ตรงกัน รุ่น: '2.0.2.10' รุ่นที่ต้องการ: '2.0.133'*
+ *โซลูชัน Dynamics 365 for Sales 'Dynamics365FinanceExtended' มีรุ่นที่ไม่ตรงกัน รุ่น: '1.0.0.0' รุ่น: '2.0.227'*
+ *โซลูชัน Dynamics 365 for Sales 'Dynamics365FinanceAndOperationsCommon' มีรุ่นที่ไม่ตรงกัน รุ่น: '1.0.0.0' รุ่น: '2.0.133'*
+ *โซลูชัน Dynamics 365 for Sales 'CurrencyExchangeRates' มีรุ่นที่ไม่ตรงกัน รุ่น: '1.0.0.0' รุ่น: '2.0.133'*
+ *โซลูชัน Dynamics 365 for Sales 'Dynamics365SupplyChainExtended' มีรุ่นที่ไม่ตรงกัน รุ่น: '1.0.0.0' รุ่น: '2.0.227'*

เมื่อต้องการแก้ไขปัญหา ให้อัปเดตโซลูชันการรวมแบบสองทิศทางใน Dataverse ตรวจสอบให้แน่ใจว่าได้อัปเกรดเป็นโซลูชันล่าสุดที่ตรงกับรุ่นโซลูชันที่ต้องใช้

[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]

