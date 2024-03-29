---
title: คุณลักษณะที่เอาออกหรือไม่สนับสนุนใน Dynamics 365 Commerce
description: บทความนี้อธิบายคุณลักษณะที่ถูกลบออก หรือที่ถูกวางแผนไว้สำหรับการลบจาก Dynamics 365 Commerce
author: josaw1
ms.date: 08/23/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: josaw
ms.search.region: Global
ms.author: josaw
ms.search.validFrom: 2020-04-30
ms.dyn365.ops.version: Platform update 33
ms.openlocfilehash: 59ffcc00d67f6538980dec8965f894eb51f7230d
ms.sourcegitcommit: 649f1db26da8f20602f11180fc565b7c59eaf545
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 08/23/2022
ms.locfileid: "9337608"
---
# <a name="removed-or-deprecated-features-in-dynamics-365-commerce"></a>คุณลักษณะที่เอาออกหรือไม่สนับสนุนใน Dynamics 365 Commerce

[!include [banner](../includes/banner.md)]

บทความนี้อธิบายคุณลักษณะที่ถูกลบออก หรือที่ถูกวางแผนไว้สำหรับการลบจาก Dynamics 365 Commerce

- คุณลักษณะที่ *ถูกลบ* จะไม่พร้อมใช้งานในผลิตภัณฑ์อีกต่อไป
- คุณลักษณะที่ *ถูกยกเลิกการใช้* ไม่ได้อยู่ในการพัฒนาที่ใช้งานอยู่ และอาจถูกลบออกในการปรับปรุงในอนาคต

รายการนี้มีไว้เพื่อช่วยคุณพิจารณาการลบออกและการยกเลิกการใช้งานเหล่านี้สำหรับการวางแผนของคุณเอง 

> [!NOTE]
> ข้อมูลโดยละเอียดเกี่ยวกับออบเจ็กต์ในแอปการเงินและการดำเนินงานสามารถพบได้ใน [รายงานอ้างอิงทางเทคนิค](/dynamics/s-e/) คุณสามารถเปรียบเทียบรุ่นต่างๆ ของรายงานเหล่านี้เพื่อเรียนรู้เกี่ยวกับออบเจ็กต์ที่มีการเปลี่ยนแปลง หรือโดนลบออกในแต่ละรุ่นของแอปการเงินและการดำเนินงาน

## <a name="features-removed-or-deprecated-in-the-commerce-10029-release"></a>คุณลักษณะที่เอาออกหรือที่เลิกสนับสนุนในการนำออกใช้ Commerce 10.0.29

### <a name="commerce-parameters-setting---allow-price-adjustments-to-increase-product-price"></a>การตั้งค่าพารามิเตอร์ Commerce - อนุญาตให้มีการปรับปรุงราคาเพื่อเพิ่มราคาของผลิตภัณฑ์

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **เหตุผลสำหรับการยกเลิกการใช้/การลบ** | เราได้ตั้งค่านี้เพื่อควบคุมว่าฟังก์ชันการปรับปรุงราคาอนุญาตให้เพิ่มราคาผลิตภัณฑ์หรือไม่ เมื่อพารามิเตอร์นี้ปิดอยู่ เมื่อใช้ฟังก์ชันฟังก์ชันการปรับปรุงราคาจะสามารถตั้งค่าราคาต่อหน่วยของผลิตภัณฑ์ให้ต่ำกว่าราคาพื้นฐาน และราคาขายตามข้อตกลงทางการค้าได้เท่านั้น เราไม่สนับสนุนการตั้งค่านี้ เนื่องจากฟังก์ชันการปรับปรุงราคาได้รับการอัปเดตเพื่อสนับสนุนการปรับปรุงสองทาง (เพิ่มหรือลด) แบบสำเร็จรูป |
| **แทนที่ด้วยลักษณะการทำงานอื่นหรือไม่**   | หมายเลข |
| **พื้นที่ของผลิตภัณฑ์ที่ได้รับผล**         | การกำหนดราคาและส่วนลด |
| **ตัวเลือกการปรับใช้**              | ทั้งหมด |
| **สถานะ**                         | ไม่สนับสนุน: การตั้งค่านี้เปิดอยู่ตามค่าเริ่มต้นเนื่องจาก Commerce เวอร์ชัน 10.0.29 และจะถูกลบออกในเดือนตุลาคม 2023 |

### <a name="commerce-parameters-setting---enable-price-report-for-retail-store"></a>การตั้งค่าพารามิเตอร์ Commerce - เปิดใช้งานรายงานราคาในร้านค้าปลีก

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **เหตุผลสำหรับการยกเลิกการใช้/การลบ** | เราได้ตั้งค่านี้เพื่อควบคุมว่าฟังก์ชันรายงานราคาพร้อมใช้งานบนแบบฟอร์มการตั้งค่าคอนฟิกของร้านค้าหรือไม่ เรายกเลิกการตั้งค่านี้ เนื่องจากแบบฟอร์มการตั้งค่าคอนฟิกร้านค้ามีการอัปเดตเพื่อให้ฟังก์ชันรายงานราคาที่มีให้ เป็นฟังก์ชันมาตรฐานเสมอ |
| **แทนที่ด้วยลักษณะการทำงานอื่นหรือไม่**   | หมายเลข |
| **พื้นที่ของผลิตภัณฑ์ที่ได้รับผล**         | การกำหนดราคาและส่วนลด |
| **ตัวเลือกการปรับใช้**              | ทั้งหมด |
| **สถานะ**                         | ไม่สนับสนุน: การตั้งค่านี้จะถูกลบออกในเดือนตุลาคม 2023 |

### <a name="commerce-parameters-setting---use-todays-date-to-calculate-prices"></a>การตั้งค่าพารามิเตอร์ Commerce - ใช้วันที่วันนี้เพื่อคํานวณราคา

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **เหตุผลสำหรับการยกเลิกการใช้/การลบ** | กลไกจัดการการกำหนดราคาของ Supply Chain Management (SCM) สนับสนุนการคำนวณการกำหนดราคาตาม วันที่จัดส่งที่ร้องขอ หรือ วันที่รับสินค้าที่ร้องขอ พร้อมกับวันที่วันนี้ กลไกจัดการกําหนดราคา Commerce จะสนับสนุนการคํานวณการกําหนดราคาตามวันที่วันนี้เท่านั้น สำหรับลูกค้าที่ใช้ทั้งความสามารถ SCM และ Commerce เราได้จัดเตรียมการตั้งค่านี้ไว้ และขอแนะนาว่าลูกค้าควรตั้งค่าเป็น **ใช่** เสมอ เพื่อให้กลไกจัดการการกําหนดราคาสองอย่างสามารถร่วมกันได้ เรายกเลิกการสนับสนุนการตั้งค่านี้ เนื่องจากจะไม่เปลี่ยนลักษณะการคํานวณและซ้ำซ้อน |
| **แทนที่ด้วยลักษณะการทำงานอื่นหรือไม่**   | หมายเลข |
| **พื้นที่ของผลิตภัณฑ์ที่ได้รับผล**         | การกำหนดราคาและส่วนลด |
| **ตัวเลือกการปรับใช้**              | ทั้งหมด |
| **สถานะ**                         | ไม่สนับสนุน: การตั้งค่านี้เปิดอยู่ตามค่าเริ่มต้นเนื่องจาก Commerce เวอร์ชัน 10.0.29 และจะถูกลบออกในเดือนตุลาคม 2023 |

## <a name="feature-deprecation-effective-july-2022"></a>การเลิกใช้คุณลักษณะมีผลบังคับเมื่อเดือนกรกฎมคม 2022

### <a name="commerce-analytics-preview"></a>การวิเคราะห์ของ Commerce (พรีวิว)

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **เหตุผลสำหรับการยกเลิกการใช้/การลบ** | ทีมงาน Dynamics 365 Commerce ได้วิเคราะห์การใช้งานและการใช้คุณลักษณะ Commerce analytics (พรีวิว) และได้ตัดสินใจที่จะไม่มีการเลื่อนไปข้างหน้าในคุณลักษณะมาที่ความพร้อมใช้งานทั่วไปอีกต่อไป   |
| **แทนที่ด้วยลักษณะการทำงานอื่นหรือไม่**   | ขณะนี้ Commerce analytics (พรีวิว) จะไม่ถูกแทนที่ด้วยคุณลักษณะ หรือโซลูชันอื่น การส่งออกธุรกรรมดิบและข้อมูลหลักจากแอปการเงินและการดําเนินงานไปยัง Azure Data Lake ดําเนินการต่อไปตามที่อธิบายไว้ใน [การส่งออกไปยัง Data Lake ในแอปการเงินและการดําเนินงาน](../../fin-ops-core/dev-itpro/data-entities/finance-data-azure-data-lake.md) คู่ค้าและลูกค้าสามารถใช้สตรีมข้อมูล เพื่อสร้างรายงานการวิเคราะห์ที่ต้องการตามความต้องการทางธุรกิจได้
| **พื้นที่ของผลิตภัณฑ์ที่ได้รับผล**         | การวิเคราะห์ของ Commerce (พรีวิว) |
| **ตัวเลือกการปรับใช้**              | ทั้งหมด |
| **สถานะ**                         | เราจะพิจารณาการปิดใช้งานคุณลักษณะนี้ในวันที่ 30 สิงหาคม 2022  จากวันนี้ไปข้างหน้า จะไม่มีการรีเฟรชเกิดขึ้นในรายงาน Power BI ปัจจุบัน จาก Commerce analytics (พรีวิว)     |

## <a name="features-removed-or-deprecated-in-the-commerce-10021-release"></a>คุณลักษณะที่เอาออกหรือที่เลิกสนับสนุนในการนำออกใช้ Commerce 10.0.21

[!include [banner](../includes/preview-banner.md)]

### <a name="overlapping-discounts-handling-setting-in-commerce-parameters"></a>การตั้งค่าการจัดการส่วนลดที่ซ้อนทับกันในพารามิเตอร์ Commerce

การตั้งค่า **การจัดการส่วนลดที่ซ้อนทับกัน** ในหน้า **พารามิเตอร์ Commerce** เลิกสนับสนุนในผลิตภัณฑ์ Commerce รุ่น 10.0.21 ไปข้างหน้า กลไกจัดการกําหนดราคา Commerce จะใช้อัลกอริทึมเดียวเพื่อกําหนดชุดที่เหมาะสมของส่วนลดที่ทับซ้อนกัน

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **เหตุผลสำหรับการยกเลิกการใช้/การลบ** | <p>การตั้งค่า **การจัดการส่วนลดที่ทับซ้อนกัน** ในพารามิเตอร์ Commerce จะควบคุมวิธีค้นหากลไกจัดการการกําหนดราคา Commerce และกําหนดชุดที่เหมาะสมของส่วนลดที่ทับซ้อนกัน ขณะนี้มีตัวเลือกสามตัว:<p><ul><li> **ประสิทธิภาพสูงสุด** – ตัวเลือกนี้จะใช้อัลกอริทึมการวิเคราะห์ขั้นสูงและวิธีการ [จัดอันดับค่ากําไรเบื้องต้น](../optimal-combination-overlapping-discounts.md) เพื่อจัดระดับความส่าดับ ประเมิน และระบุชุดส่วนลดที่ดีที่สุดได้ทันเวลา</li><li>**การคํานวณแบบสมดุล** – ในฐานรหัสปัจจุบัน ตัวเลือกนี้จะใช้ได้กับตัวเลือก **ประสิทธิภาพสูงสุด** ดังนั้น จึงควรเป็นตัวเลือกที่คัดลอกมา</li><li>**การคํานวณที่ไม่ครอบคลุม** – ตัวเลือกนี้ใช้อัลกอริทึมเก่าที่จะผ่านชุดส่วนลดที่เป็นไปได้ทั้งหมดในระหว่างการคํานวณราคา สำหรับใบสั่งที่มีรายการและปริมาณขนาดมาก ตัวเลือกนี้อาจทําให้เกิดปัญหาด้านประสิทธิภาพ</li></ul><p>เพื่อช่วยให้การตั้งค่าคอนฟิกง่ายขึ้น ให้ปรับปรุงประสิทธิภาพ และลดเหตุการณ์ที่เกิดจากอัลกอริทึมเก่า เราจะลบการตั้งค่า **การจัดการส่วนลดที่ทับซ้อนกัน** ออกโดยสมบูรณ์ และอัปเดตตรรกะภายในของกลไกจัดการการกําหนดราคา Commerce เพื่อให้ขณะนี้ใช้เฉพาะอัลกอริทึมขั้นสูง (นั่นคืออัลกอริทึมที่อยู่เบื้องหลังตัวเลือก **ประสิทธิภาพสูงสุด**)</p> |
| **แทนที่ด้วยลักษณะการทำงานอื่นหรือไม่**   | ไม่ เราขอแนะนำว่าองค์กรที่ใช้ **การคํานวณแบบสมดุล** หรือ **การคํานวณที่ไม่ครอบคลุม** สลับเป็น **ประสิทธิภาพสูงสุด** ก่อนที่จะลบคุณลักษณะนี้ออก |
| **พื้นที่ของผลิตภัณฑ์ที่ได้รับผล**         | การกำหนดราคาและส่วนลด |
| **ตัวเลือกการปรับใช้**              | ทั้งหมด |
| **สถานะ**                         | ณ รุ่น 10.0.21 การตั้งค่า **การจัดการส่วนลดที่ทับซ้อนกัน** จะถูกลบออกจากพารามิเตอร์ Commerce ในเดือนตุลาคม 2022 |

### <a name="retail-sdk-distributed-by-using-lifecycle-services"></a>Retail SDK ที่กระจายโดยใช้ Lifecycle Services

Retail SDK จัดส่งใน Lifecycle Services (LCS) วิธีการกระจายนี้ไม่สนับสนุนในรุ่น 10.0.21 ไปข้างหน้า แพคเกจการอ้างอิงของ Retail SDK ไลบรารี และตัวอย่างจะถูกเผยแพร่ในที่เก็บสาธารณะบน GitHub

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **เหตุผลสำหรับการยกเลิกการใช้/การลบ** | การจัดส่ง Retail SDK ใน LCS กระบวนการ LCS จะใช้เวลาสองสามชั่วโมงในการเสร็จสิ้น และต้องซ้ำกระบวนการในการอัปเดตทุกครั้ง ไปข้างหน้า แพคเกจการอ้างอิงของ Retail SDK ไลบรารี และตัวอย่างจะถูกเผยแพร่ในที่เก็บสาธารณะบน GitHub ตัวอย่างการเพิ่มเติมและแพคเกจอ้างอิงสามารถใช้ได้ง่าย และการอัปเดตจะเสร็จสิ้นในอีกสองสามนาที |
| **แทนที่ด้วยลักษณะการทำงานอื่นหรือไม่**   |  [ดาวน์โหลดตัวอย่าง Retail SDK และแพคเกจอ้างอิงจาก GitHub และ NuGet](../dev-itpro/retail-sdk/sdk-github.md) |
| **พื้นที่ของผลิตภัณฑ์ที่ได้รับผล**         | Retail SDK |
| **ตัวเลือกการปรับใช้**              | ทั้งหมด |
| **สถานะ**                         | ไม่สนับสนุน: ณ รุ่น 10.0.21 SDK ที่จัดส่งผ่านทาง LCS VMs จะถูกลบออกในเดือนตุลาคม 2023 |

### <a name="retail-deployable-package-and-combined-pos-hardware-station-and-cloud-scale-unit-installers"></a>แพคเกจที่ปรับใช้ได้ของ Retail และรวม POS สถานีฮาร์ดแวร์ และตัวติดตั้งสเกลยูนิตในระบบคลาวด์

แพคเกจที่สามารถปรับใช้ Retail ที่สร้างโดยใช้ Retail SDK MSBuild ไม่สนับสนุนใน 10.0.21 นับจากนี้ ให้ใช้แพคเกจ Cloud Scale Unit (CSU) ของส่วนขยายหน่วย Cloud Scale (Commerce Runtime ฐานข้อมูลช่องทาง API พาณิชย์แบบไม่มีข้อมูล การชำระเงิน และการขายหน้าร้านระบบคลาวด์ (POS)) ใช้ตัวติดตั้งเฉพาะส่วนขยายของ POS สถานีฮาร์ดแวร์ และสเกลยูนิตในระบบคลาวด์ที่โฮสต์เอง

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **เหตุผลสำหรับการยกเลิกการใช้/การลบ** | แพคเกจที่ปรับใช้ได้ของ Retail เป็นแพคเกจรวมที่มีชุดแพคเกจและตัวติดตั้งส่วนขยายที่สมบูรณ์ แพคเกจรวมนี้ช่วยให้การปรับใช้ซับซ้อน เนื่องจากส่วนขยายของ CSU ให้ไปที่สเกลยูนิตในระบบคลาวด์และโปรแกรมติดตั้งถูกปรับใช้ในร้านค้า โปรแกรมติดตั้งรวมถึงส่วนขยายและผลิตภัณฑ์พื้นฐาน ซึ่งทำให้การอัปเดตยุ่งยาก เมื่ออัปเกรดทุกครั้ง จะต้องสร้างการรวมรหัสและการสร้างแพคเกจ เมื่อต้องการให้กระบวนการนี้ง่ายขึ้น ขณะนี้แพคเกจส่วนขยายจะถูกแยกออกเป็นส่วนประกอบต่างๆ เพื่อให้การปรับใช้และการจัดการง่ายขึ้น ด้วยวิธีการใหม่ ส่วนขยาย และตัวติดตั้งผลิตภัณฑ์พื้นฐานจะถูกแยกออก และสามารถให้บริการและอัปเกรดอย่างอิสระโดยไม่มีการรวมรหัสหรือบรรจุใหม่|
| **แทนที่ด้วยลักษณะการทำงานอื่นหรือไม่**   | ส่วนขยาย CSU ตัวติดตั้งส่วนขยาย POS ตัวติดตั้งส่วนขยายสถานีฮาร์ดแวร์ |
| **พื้นที่ของผลิตภัณฑ์ที่ได้รับผล**         | การปรับใช้และส่วนขยาย Dynamics 365 Commerce |
| **ตัวเลือกการปรับใช้**              | ทั้งหมด |
| **สถานะ**                         | ไม่สนับสนุน: ณ รุ่น 10.0.21 การสนับสนุนการปรับใช้ RetailDeployablePackage ใน LCS จะถูกลบออกในเดือนตุลาคม 2022 |

สำหรับข้อมูลเพิ่มเติม ดูที่ 

+ [สร้างแพคเกจแยกต่างหากของ Commerce Cloud Scale Unit (CSU)](../dev-itpro/retail-sdk/retail-sdk-packaging.md#generate-a-separate-package-for-commerce-cloud-scale-unit-csu)
+ [สร้างแพคเกจส่วนขยาย Modern POS](../dev-itpro/pos-extension/mpos-extension-packaging.md)
+ [รวม POS กับอุปกรณ์ฮาร์ดแวร์ใหม่](../dev-itpro/hardware-device-extension.md)
+ ตัวอย่างรหัส
    + [Cloud Scale Unit](https://github.com/microsoft/Dynamics365Commerce.ScaleUnit)
    + [POS, CSU และสถานีฮาร์ดแวร์](https://github.com/microsoft/Dynamics365Commerce.InStore)

### <a name="modernpossln-and-cloudpossln-in-the-retail-sdk"></a>ModernPos.Sln และ CloudPos.sln ใน Retail SDK

การพัฒนาส่วนขยายของ POS โดยใช้ ModernPos.sln, CloudPos.sln, POS Extension.csproj และไม่ได้สนับสนุนโฟลเดอร์ POS ในรุ่น 10.0.21 ไปข้างหน้า ให้ใช้ SDK แพคเกจอิสระของ POS ในส่วนขยายของ POS

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **เหตุผลสำหรับการยกเลิกการใช้/การลบ** | ใน Retail SDK รุ่นก่อนหน้านี้ ถ้ามีส่วนขยายของ POS ต้องมีการรวมรหัสและบรรจุใหม่เพื่ออัปเดตเป็น POS รุ่นล่าสุด การรวมรหัสเป็นกระบวนการอัปเกรดที่ใช้เวลานานและคุณต้องรักษา Retail SDK แบบเต็มในที่เก็บ และคุณต้องคอมไพล์ POS.App project. หลัก โดยการใช้รูปแบบการจัดทำแพคเกจแบบอิสระ คุณต้องรักษาไว้เฉพาะส่วนขยายของคุณเท่านั้น กระบวนการอัปเดตเป็นส่วนขยาย POS รุ่นล่าสุดจะง่ายเช่นเดียวกับการอัปเดตรุ่นของแพคเกจ NuGet ที่โครงการของคุณใช้ คุณสามารถปรับใช้ส่วนขยายอย่างอิสระและบริการต่างๆ จะใช้ตัวติดตั้งส่วนขยาย POS พื้นฐานสามารถปรับใช้และรักษาแยกต่างหากได้ และไม่ต้องรวมหรือแยกรหัสใหม่กับตัวติดตั้งพื้นฐานหรือรหัส |
| **แทนที่ด้วยลักษณะการทำงานอื่นหรือไม่**   | [SDK การจัดทำแพคเกจแบบอิสระของ POS](../dev-itpro/pos-extension/pos-extension-getting-started.md) |
| **พื้นที่ของผลิตภัณฑ์ที่ได้รับผล**         | การปรับใช้และส่วนขยาย POS ของ Dynamics 365 Commerce |
| **ตัวเลือกการปรับใช้**              | ทั้งหมด |
| **สถานะ**                         | ไม่สนับสนุน: ณ รุ่น 10.0.21 การสนับสนุนแพคเกจ POS และรูปแบบส่วนขยายรวมโดยใช้ ModernPos.Sln, CloudPOs.sln และ POS Extensons.csproj ใน Retail SDK จะถูกลบออกในเดือนตุลาคม 2023 |

## <a name="features-removed-or-deprecated-in-the-commerce-10017-release"></a>คุณลักษณะที่เอาออกหรือที่เลิกสนับสนุนในการนำออกใช้ Commerce 10.0.17

### <a name="full-dataset-generation-interval-is-deprecated"></a>ไม่สนับสนุนช่วงการสร้างชุดข้อมูลแบบเต็ม

|  &nbsp; | &nbsp; |
|------------|--------------------|
| **เหตุผลสำหรับการยกเลิกการใช้/การลบ** | โดยเริ่มต้นในผลิตภัณฑ์รุ่นนี้ ในฟอร์ม **พารามิเตอร์ตัวจัดตาราง Commerce** ในศูนย์ควบคุม Dynamics 365 ในฟิลด์ **ช่วงเวลาการสร้างชุดข้อมูลแบบเต็มเป็นวัน** จะถูกไม่สนับสนุน นอกจากนี้ ให้เริ่มต้นในการเผยแพร่นี้ ฟิลด์จะถูกลบออกด้วยภาพเพื่อให้ไม่สามารถแก้ไขค่าได้ ค่านี้จะอยู่เป็นค่า **0** |
| **แทนที่ด้วยลักษณะการทำงานอื่นหรือไม่**   | ไม่ |
| **พื้นที่ของผลิตภัณฑ์ที่ได้รับผล**         | Dynamics 365 Commerce |
| **ตัวเลือกการปรับใช้**              | ทั้งหมด|
| **สถานะ**                         | ยกเลิกการใช้งาน อย่าใช้ฟิลด์นี้หรือเปลี่ยนค่าในฟิลด์นี้|

## <a name="features-removed-or-deprecated-in-the-commerce-10015-release"></a>คุณลักษณะที่เอาออกหรือที่เลิกสนับสนุนในการนำออกใช้ Commerce 10.0.15

### <a name="internet-explorer-11-support-for-dynamics-365-is-deprecated"></a>การสนับสนุน Internet Explorer 11 สำหรับ Dynamics 365 ไม่สนับสนุน

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **เหตุผลสำหรับการยกเลิกการใช้/การลบ** | มีผลบังคับใช้ตั้งแต่เดือนธันวาคม 2020 การสนับสนุนของ Microsoft Internet Explorer 11 สำหรับผลิตภัณฑ์ Dynamics 365 ทั้งหมดจะไม่ได้รับการสนับสนุน และ Internet Explorer 11 จะไม่ได้รับการสนับสนุนหลังจากสิงหาคม 2021<br><br>การทำเช่นนี้จะส่งผลกระทบต่อลูกค้าที่ใช้ผลิตภัณฑ์ Dynamics 365 ที่ได้รับการออกแบบมาให้ใช้ผ่านอินเทอร์เฟส Internet Explorer 11 หลังจากสิงหาคม 2021 Internet Explorer 11 จะไม่ได้รับการสนับสนุนสำหรับผลิตภัณฑ์ Dynamics 365 ดังกล่าว |
| **แทนที่ด้วยลักษณะการทำงานอื่นหรือไม่**   | เราขอแนะนำให้ลูกค้าเปลี่ยนไปใช้ Microsoft Edge|
| **พื้นที่ของผลิตภัณฑ์ที่ได้รับผล**         | ผลิตภัณฑ์ของ Dynamics 365 ทั้งหมด |
| **ตัวเลือกการปรับใช้**              | ทั้งหมด|
| **สถานะ**                         | ยกเลิกการใช้งาน Internet Explorer 11 จะไม่ได้รับการสนับสนุนหลังจากสิงหาคม 2021|

## <a name="features-removed-or-deprecated-in-the-commerce-10011-release"></a>คุณลักษณะที่เอาออกหรือที่เลิกสนับสนุนในการนำออกใช้ Commerce 10.0.11
### <a name="data-action-hooks"></a>จุดเชื่อมต่อการดำเนินการกับข้อมูล
| &nbsp;  | &nbsp; |
|------------|--------------------|
| **เหตุผลสำหรับการยกเลิกการใช้/การลบ** | จุดเชื่อมต่อการดำเนินการกับข้อมูลไม่ได้รับการสนับสนุน เนื่องจากปัญหาประสิทธิภาพการทำงาน |
| **แทนที่ด้วยลักษณะการทำงานอื่นหรือไม่**   | เราขอแนะนำให้ใช้ [การแทนที่การดำเนินการกับข้อมูล](../e-commerce-extensibility/data-action-overrides.md) เพื่อปรับเปลี่ยนตรรกะทางธุรกิจในเลเยอร์การดำเนินการข้อมูล|
| **พื้นที่ของผลิตภัณฑ์ที่ได้รับผล**         | การดำเนินการข้อมูลเกี่ยวกับความสามารถในการเพิ่มฟังก์ชันของอีคอมเมิร์ซ |
| **ตัวเลือกการปรับใช้**              | ทั้งหมด |
| **สถานะ**                         | ไม่สนับสนุน: ณ วันที่ของการนำออกใช้ 10.0.11 |

### <a name="retail-sdk-support-for-visual-studio-2015-msbuild-140-and-retail-sdkreference-libraries-and-tools"></a>การสนับสนุน Retail SDK สำหรับ Visual Studio 2015, msbuild 14.0 และไลบรารีและเครื่องมือ Retail SDK\Reference
| &nbsp;  | &nbsp; |
|------------|--------------------|
| **เหตุผลสำหรับการยกเลิกการใช้/การลบ** | การสนับสนุน SDK การขายปลีกสำหรับ Visual Studio 2015 ถูกเลิกใช้งานและได้รับการปรับปรุงเพื่อสนับสนุน VS 2017 msbuild 15.0 และไลบรารีการอ้างอิงและเครื่องมือตัวสร้างพร็อกซีของ commerce ทั้งหมด ในโฟลเดอร์ RetailSDK\References ที่ถูกย้ายไปยังแพคเกจ NuGet เพื่อทำให้แบบจำลองส่วนขยายและกระบวนการปรับรุ่น SDK ง่ายขึ้น|
| **แทนที่ด้วยลักษณะการทำงานอื่นหรือไม่**   | เราขอแนะนำให้คุณปฏิบัติตามข้อมูลใน [โยกย้าย Retail SDK จาก Visual Studio 2015 เป็น Visual Studio 2017](../dev-itpro/retail-sdk/migrate-sdk.md) เพื่อปร้บปรุงระบบของคุณ |
| **พื้นที่ของผลิตภัณฑ์ที่ได้รับผล**         | ส่วนขยายของ Retail SDK |
| **ตัวเลือกการปรับใช้**              | ทั้งหมด |
| **สถานะ**                         | ไม่สนับสนุน: ณ วันที่ของการนำออกใช้ 10.0.11 |

### <a name="retail-server-extension-using-iedmmodelextender-and-commercecontroller"></a>ส่วนขยายของ Retail Server ที่ใช้ IEdmModelExtender และ CommerceController
| &nbsp;  | &nbsp; |
|------------|--------------------|
| **เหตุผลสำหรับการยกเลิกการใช้/การลบ** | ส่วนขยายของ Retail Server ที่ใช้ IEdmModelExtender และ CommerceController ถูกเลิกใช้งาน เพื่อให้แบบจำลองส่วนขยายแบบง่าย การใช้งานใหม่จะมีเฉพาะคลาสตัวควบคุมโดยไม่มีการใช้งานคลาส IEdmModelExtender เพิ่มเติมใดๆ นอกจากนี้ ยังหลีกเลี่ยงการอ้างอิงกับรุ่น OData เฉพาะ (ถ้ามีการปรับปรุงรุ่น OData อาจมีการแบ่งส่วนขยาย) |
| **แทนที่ด้วยลักษณะการทำงานอื่นหรือไม่**   |  เราขอแนะนำให้คุณใช้แบบจำลองส่วนขยายคลาส IController โดยการนำเข้าแพคเกจ NuGet (Microsoft.Dynamics.Commerce.Hosting.Contracts) |
| **พื้นที่ของผลิตภัณฑ์ที่ได้รับผล**         | ส่วนขยายของ Retail Server |
| **ตัวเลือกการปรับใช้**              | ทั้งหมด |
| **สถานะ**                         | ไม่สนับสนุน: ณ วันที่ของการนำออกใช้ 10.0.11 |

### <a name="hardware-station-extension-using-ihardwarestationcontroller"></a>ส่วนขยายของสถานีฮาร์ดแวร์ที่ใช้ IHardwareStationController
| &nbsp;  | &nbsp; |
|------------|--------------------|
| **เหตุผลสำหรับการยกเลิกการใช้/การลบ** | ส่วนขยายของสถานีฮาร์ดแวร์ที่ใช้ IHardwareStationController ถูกเลิกใช้ เพื่อให้แบบจำลองส่วนขยายแบบง่าย การดำเนินการใหม่จะมีเฉพาะคลาส IController โดยไม่มีการใช้งานคลาสเพิ่มเติมใดๆ และเพื่อหลีกเลี่ยงการอ้างอิงที่มีไลบรารีสถานีฮาร์ดแวร์หลัก ก่อนหน้านี้ส่วนขยายจำเป็นต้องใช้ในการอ้างอิงไลบรารีจำนวนมาก) |
| **แทนที่ด้วยลักษณะการทำงานอื่นหรือไม่**   | ขอแนะนำให้ใช้แบบจำลองส่วนขยายคลาส IController โดยการนำเข้าแพคเกจ NuGet (Microsoft.Dynamics.Commerce.Hosting.Contracts) |
| **พื้นที่ของผลิตภัณฑ์ที่ได้รับผล**         | ส่วนขยายสถานีฮาร์ดแวร์ |
| **ตัวเลือกการปรับใช้**              | ทั้งหมด |
| **สถานะ**                         | ไม่สนับสนุน: ณ วันที่ของการนำออกใช้ 10.0.11 |

## <a name="features-removed-or-deprecated-in-the-commerce-10010-release"></a>คุณลักษณะที่เอาออกหรือที่เลิกสนับสนุนในการนำออกใช้ Commerce 10.0.10
### <a name="pos-operation-803---picking-and-receiving"></a>การดำเนินการ POS 803 - การเบิกสินค้าและการรับสินค้า
| &nbsp;  | &nbsp; |
|------------|--------------------|
| **เหตุผลสำหรับการยกเลิกการใช้/การลบ** | การดำเนินการเบิกสินค้าและการรับสินค้าจะถูกยกเลิกการใช้งานเนื่องจากการออกแบบการดำเนินงานใหม่ |
| **แทนที่ด้วยลักษณะการทำงานอื่นหรือไม่**   | ใช่ จะถูกแทนที่ด้วยสองการดำเนินงาน POS ใหม่: การดำเนินงานขาเข้า (804) และการดำเนินงานขาออก (805)|
| **พื้นที่ของผลิตภัณฑ์ที่ได้รับผล**         | ใบสมัครสำหรับการขายหน้าร้าน (POS) |
| **ตัวเลือกการปรับใช้**              | ทั้งหมด |
| **สถานะ**                         | ไม่สนับสนุน: เมื่อนำรุ่น 10.0.10 ออกใช้ การดำเนินการเบิกสินค้าและการรับสินค้าจะไม่ได้รับการอัพเดทใดๆ ใหม่อีกต่อไป การแก้ไขข้อผิดพลาดที่สำคัญเท่านั้นที่จะดำเนินการสำหรับการดำเนินงานนี้ในรุ่นต่อๆ ไป ลูกค้าทั้งหมดจะได้รับการสนับสนุนให้ย้ายไปที่ [การดำเนินงานขาเข้าใหม่](../pos-inbound-inventory-operation.md) และ [การดำเนินงานขาออก](../pos-outbound-inventory-operation.md) ซึ่งจะยังคงเป็นส่วนหนึ่งของแผนงานผลิตภัณฑ์ระยะยาวของเรา |


## <a name="features-removed-or-deprecated-in-the-commerce-1007-release"></a>คุณลักษณะที่เอาออกหรือที่เลิกสนับสนุนในการนำออกใช้ Commerce 10.0.7
### <a name="commerce-getproductavailabilities-and-getavailableinventorynearby-apis"></a>API ของ Commerce GetProductAvailabilities และ GetAvailableInventoryNearby
| &nbsp;  | &nbsp; |
|------------|--------------------|
| **เหตุผลสำหรับการยกเลิกการใช้/การลบ** | API ที่ปรับให้เหมาะสมใหม่ถูกสร้างเพื่อแทนที่ API ของ GetProductAvailabilities และ GetAvailableInventoryNearby |
| **แทนที่ด้วยลักษณะการทำงานอื่นหรือไม่**   | ใช่: ถูกแทนที่ด้วย API ของ GetEstimatedAvailability และ GetEstimatedProductWarehouseAvailability |
| **พื้นที่ของผลิตภัณฑ์ที่ได้รับผล**         | SDK แอปพลิเคชันอีคอมเมิร์ซ |
| **ตัวเลือกการปรับใช้**              | ทั้งหมด |
| **สถานะ**                         | ไม่ได้รับการสนับสนุน: รุ่น 10.0.7 ที่นำออกใช้จะไม่มีการลงทุนทางวิศวกรรมที่ทำสำหรับ GetProductAvailabilities และ GetAvailableInventoryNearby องค์กรที่ใช้ API เหล่านี้ในการปรับใช้อีคอมเมิร์ซของตนควรแปลงเป็น API ของ GetEstimatedAvailability และ GetEstimatedProductWarehouseAvailability ใหม่ และเปิดใช้งาน [คุณลักษณะการทำงานการคำนวณความพร้อมใช้งานของผลิตภัณฑ์ที่เหมาะสม](../calculated-inventory-retail-channels.md)  |

## <a name="previous-announcements-about-removed-or-deprecated-features"></a>ประกาศก่อนหน้านี้เกี่ยวกับคุณลักษณะที่ถูกลบหรือเลิกสนับสนุน
เมื่อต้องการเรียนรู้เพิ่มเติมเกี่ยวกับคุณลักษณะที่ถูกลบออกหรือเลิกสนับสนุนในรุ่นก่อนหน้านี้ ดูที่ [คุณลักษณะที่ถูกลบออกหรือเลิกสนับสนุนในรุ่นก่อนหน้านี้](../../fin-ops-core/dev-itpro/migration-upgrade/deprecated-features.md?toc=/dynamics365/commerce/toc.json)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]

