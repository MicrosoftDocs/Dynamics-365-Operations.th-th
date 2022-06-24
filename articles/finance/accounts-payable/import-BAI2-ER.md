---
title: ตั้งค่าการนำเข้าการกระทบยอดบัญชีธนาคารขั้นสูงโดยใช้การรายงานทางอิเล็กทรอนิกส์
description: บทความนี้อธิบายวิธีใช้การรายงานทางอิเล็กทรอนิกส์เพื่อตั้งค่ากระบวนการนำเข้าการกระทบยอดบัญชีธนาคารขั้นสูง
author: panolte
ms.date: 03/30/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: BankStatementFormat
audience: Application User
ms.reviewer: twheeloc
ms.custom: 88433
ms.assetid: 73f3dcf6-040a-44ad-9512-7b3e0d17a571
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-05-31
ms.dyn365.ops.version: AX 10.0.25
ms.openlocfilehash: 2ac8811a5c10490d90f782472d3c198474c7edc0
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 06/03/2022
ms.locfileid: "8889133"
---
# <a name="set-up-advanced-bank-reconciliation-import-by-using-electronic-reporting"></a>ตั้งค่าการนำเข้าการกระทบยอดบัญชีธนาคารขั้นสูงโดยใช้การรายงานทางอิเล็กทรอนิกส์

[!include [banner](../includes/banner.md)]

คุณลักษณะการกระทบยอดธนาคารขั้นสูงอนุญาตให้คุณสามารถนำเข้าใบแจ้งยอดจากธนาคารอิเล็กทรอนิกส์ได้ และกระทบยอดกับธุรกรรมธนาคารได้โดยอัตโนมัติใน Microsoft Dynamics 365 Finance บทความนี้อธิบายวิธีการตั้งค่าฟังก์ชันการนำเข้าสำหรับใบแจ้งยอดจากธนาคารของคุณ การตั้งค่าสำหรับการนำเข้าใบแจ้งยอดจากธนาคารแตกต่างกันไปขึ้นอยู่กับรูปแบบของใบแจ้งยอดจากธนาคารอิเล็กทรอนิกส์ของคุณ Microsoft Dynamics 365 Finance รองรับรูปแบบใบแจ้งยอดจากธนาคารสามรายการทั้งหมด: ISO20022, MT940 และ BAI2 

## <a name="set-up-the-electronic-reporting-configuration"></a>สร้างการตั้งค่าคอนฟิกการรายงานทางอิเล็กทรอนิกส์

1. ไปที่ **พื้นที่ทำงาน \> การรายงานทางอิเล็กทรอนิกส์**
2. บนไทล์สำหรับผู้ให้บริการตั้งค่าคอนฟิก **Microsoft** ให้เลือก **ที่เก็บ**
3. เลือก **ส่วนกลาง** แล้วเลือก **เปิด**
4. ถ้าต้องสร้างการเชื่อมต่อกับที่เก็บ ให้เลือกลิงก์สีเงินในกล่องโต้ตอบ
5. ในรายการการตั้งค่าคอนฟิก ให้ค้นหา **รูปแบบใบแจ้งยอดจากธนาคาร \> รูปแบบใบแจ้งยอดจากธนาคาร BAI2**
6. เลือกรูปแบบ **BAI2**
7. บนแท็บด่วน **รุ่น** ให้เลือกรุ่นล่าสุด แล้วเลือก **นำเข้า**

## <a name="set-up-the-bank-statement-format"></a>ตั้งค่ารูปแบบใบแจ้งยอดจากธนาคาร

1. ไปที่ **การจัดการเงินสดและธนาคาร \> การตั้งค่า \> การตั้งค่าการกระทบยอดบัญชีธนาคารขั้นสูง \> รูปแบบใบแจ้งยอดจากธนาคาร**
2. เลือก **ใหม่**
3. ตั้งค่าฟิลด์ **รูปแบบใบแจ้งยอด** และ **ชื่อ**
4. เลือกกล่องกาเครื่องหมาย **รูปแบบการนำเข้าทางอิเล็กทรอนิกส์ทั่วไป**
5. ตั้งค่าฟิลด์ **นำเข้าการตั้งค่าคอนฟิกรูปแบบ** เป็นรูปแบบ **BAI2**

## <a name="set-up-the-bank-account"></a>ตั้งค่าบัญชีธนาคาร

1. ไปที่ **การจัดการเงินสดและธนาคาร \> บัญชีธนาคาร \> บัญชีธนาคาร**
2. เปิดบัญชีธนาคาร
3. ในแท็บด่วน **การกระทบยอด** ตั้งค่าตัวเลือก **การกระทบยอดบัญชีธนาคารขั้นสูง** เป็น **ใช่**
4. ตั้งค่าฟิลด์ **รูปแบบบใแจ้งยอด** เป็นรูปแบบ **BAI2** ที่คุณสร้างไว้ก่อนหน้า

## <a name="import-the-bank-statement"></a>นำเข้าใบแจ้งยอดจากธนาคาร

1. ไปที่ **การจัดการเงินสดและธนาคาร \> การกระทบยอดใบแจ้งยอดจากธนาคาร \> ใบแจ้งยอดจากธนาคาร**
2. ที่ด้านบนของหน้า **ใบแจ้งยอดจากธนาคาร** ให้เลือก **นำเข้าใบแจ้งยอด**
3. ตั้งค่าฟิลด์ **บัญชีธนาคาร** เป็นบัญชีธนาคารในใบแจ้งยอด
4. ตั้งค่าฟิลด์ **รูปแบบบใแจ้งยอด** เป็นรูปแบบ **BAI2** ที่คุณสร้างไว้ก่อนหน้า
5. เลือก **เรียกดู** แล้วเลือกไฟล์ **BAI**
6. เลือก **อัปโหลด**
7. เลือก **ตกลง** เพื่อนำเข้าไฟล์ที่เลือก


## <a name="examples-of-bank-statement-formats-and-technical-layouts"></a>ตัวอย่างรูปแบบและโครงร่างทางเทคนิคของใบแจ้งยอดจากธนาคาร
ต่อไปนี้เป็นตัวอย่างคำนิยามของโครงร่างทางเทคนิคของไฟล์การนำเข้าการกระทบยอดบัญชีธนาคารขั้นสูง และไฟล์ตัวอย่างของใบแจ้งยอดจากธนาคารที่เกี่ยวข้องสามรายการ: [ตัวอย่างไฟล์นำเข้า](//download.microsoft.com/download/8/e/c/8ec8d2d0-eb8c-41fb-ad8c-f01a4d670a44/Dynamics365FinanceAdvancedBankStatementLayouts.xlsx)  

| คำนิยามโครงร่างทางเทคนิค                             | ไฟล์ตัวอย่างใบแจ้งยอดจากธนาคาร          |
|---------------------------------------------------------|--------------------------------------|
| DynamicsAXMT940Layout | [MT940StatementExample](//download.microsoft.com/download/2/d/c/2dcc4e55-ddc8-4a74-b79c-250fae201c3c/mt940StatementExample.txt)     |
| DynamicsAXISO20022Layout | [ISO20022StatementExample](https://nam06.safelinks.protection.outlook.com/?url=https%3A%2F%2Fdownload.microsoft.com%2Fdownload%2F1%2F5%2F5%2F155d84ed-c250-48f3-b0b1-c5a431e7855b%2FISO20022-MultipleStatements.xml&data=04%7C01%7CRobert.Schlomann%40microsoft.com%7C30d0c233cb6546547d0a08d8f4965edc%7C72f988bf86f141af91ab2d7cd011db47%7C1%7C0%7C637528273956712775%7CUnknown%7CTWFpbGZsb3d8eyJWIjoiMC4wLjAwMDAiLCJQIjoiV2luMzIiLCJBTiI6Ik1haWwiLCJXVCI6Mn0%3D%7C1000&sdata=3VzvLZK%2BO8PjuI7XVdC6rD2j3nUJfteo7zFp%2B1s9BwM%3D&reserved=0)             |
| DynamicsAXBAI2Layout    | [BAI2StatementExample](//download.microsoft.com/download/1/1/6/11693f57-bfc1-4993-a274-5fb978be70fa/BAI2StatementExample.txt)     |

